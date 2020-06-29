---
title: Поддержка клиентской отчетности по протоколу HTTP
description: Поддержка клиентской отчетности по протоколу HTTP
author: dansimp
ms.assetid: 4a26ac80-1fb5-4c05-83de-4d06793f7bf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4e1759bb4df39ac403e2837c4083275a8b3436f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815289"
---
# <span data-ttu-id="e9c48-103">Поддержка клиентской отчетности по протоколу HTTP</span><span class="sxs-lookup"><span data-stu-id="e9c48-103">Support for Client Reporting over HTTP</span></span>


<span data-ttu-id="e9c48-104">Версия 4,6 клиента App-V теперь поддерживает использование межhttp-связи при отправке данных отчетов клиента на сервер публикаций.</span><span class="sxs-lookup"><span data-stu-id="e9c48-104">Version 4.6 of the App-V client now supports the use of HTTP communication when sending client reporting data to the publishing server.</span></span> <span data-ttu-id="e9c48-105">Эта функция поддерживает сценарии, в которых клиент реализовал пользовательский сервер публикаций HTTP (S), настроенный для сбора и обработки клиентских данных.</span><span class="sxs-lookup"><span data-stu-id="e9c48-105">This feature supports scenarios where a customer has implemented a custom HTTP(S) publishing server that is configured to collect and process client data.</span></span>

<span data-ttu-id="e9c48-106">Дополнительные сведения о серверах публикаций HTTP можно найти в разделе</span><span class="sxs-lookup"><span data-stu-id="e9c48-106">For more information on HTTP publishing servers, see</span></span> <https://go.microsoft.com/fwlink/?LinkId=157426>

## <span data-ttu-id="e9c48-107">Создание отчетов по протоколу HTTP для клиентов</span><span class="sxs-lookup"><span data-stu-id="e9c48-107">Client Reporting over HTTP</span></span>


<span data-ttu-id="e9c48-108">Клиент начинает собирать данные при получении атрибута "REPORTing =" TRUE "в XML ответа на обновление публикации с сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="e9c48-108">The client starts collecting data when it receives a “REPORTING=”TRUE””attribute in the publishing refresh response XML from the publishing server.</span></span> <span data-ttu-id="e9c48-109">При получении этого атрибута клиент отправляет все накопленные данные на сервер публикаций, который отправил обновление публикации.</span><span class="sxs-lookup"><span data-stu-id="e9c48-109">When this attribute is received, the client sends any accumulated data to the publishing server that sent the publishing refresh.</span></span> <span data-ttu-id="e9c48-110">Сведения об этом процессе описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="e9c48-110">The details of this process are as follows:</span></span>

-   <span data-ttu-id="e9c48-111">Клиент отправляет запрос HTTP GET на сервер публикаций для обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="e9c48-111">The client sends an HTTP GET request to the publishing server for a publishing refresh.</span></span> <span data-ttu-id="e9c48-112">Заголовок сообщения содержит настраиваемый заголовок AppV-Op: Refresh, который используется настраиваемым сервером публикаций HTTP (S) для определения типа сообщения.</span><span class="sxs-lookup"><span data-stu-id="e9c48-112">The header of this message contains an “AppV-Op:Refresh” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

-   <span data-ttu-id="e9c48-113">Затем сервер публикаций отправляет XML-сообщение ответа на обновление публикации, содержащее значение "REPORTing =" TRUE ".</span><span class="sxs-lookup"><span data-stu-id="e9c48-113">The publishing server then sends the publishing refresh response XML that contains a “REPORTING=”TRUE”” value.</span></span>

-   <span data-ttu-id="e9c48-114">Затем клиент отправляет запрос HTTP POST на сервер публикаций вместе с данными отчета, собранными с момента предыдущего обновления.</span><span class="sxs-lookup"><span data-stu-id="e9c48-114">The client then sends an HTTP POST request to the publishing server along with the reporting data that has been gathered since the previous refresh.</span></span> <span data-ttu-id="e9c48-115">Заголовок этого сообщения содержит настраиваемый заголовок "AppV-Op: отчет", который используется настраиваемым сервером публикации HTTP (S) для определения типа сообщения.</span><span class="sxs-lookup"><span data-stu-id="e9c48-115">The header of this message contains an “AppV-Op:Report” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

<span data-ttu-id="e9c48-116">В следующей схеме содержатся определенные сведения о пакете и данных приложения, которые отправляются на сервер.</span><span class="sxs-lookup"><span data-stu-id="e9c48-116">The following schema gives specific details of the package and the application data that is sent to the server.</span></span>

```xml
<?xml version="1.0"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:element name="CLIENT_DATA">
        <xs:complexType>
            <xs:all>
                <xs:element ref="PKG_LIST" minOccurs="1" maxOccurs="1"/>
                <xs:element ref="APP_RECORDS" minOccurs="1" maxOccurs="1"/>
            </xs:all>
            <!-- no regex for Ver because we want to allow tags like "Beta" -->
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Host" type="xs:token" use="required"/>
            <xs:attribute name="CacheSize" type="xs:nonNegativeInteger" use="required"/>
            <xs:attribute name="CacheUsed" type="xs:nonNegativeInteger" use="required"/>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_LIST">
        <xs:complexType>
            <xs:choice>
                <xs:element ref="PKG_DATA" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_DATA">
        <xs:complexType>
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Guid" type="xs:token" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="VerGuid" type="xs:token" use="required"/>
            <xs:attribute name="Source" type="xs:normalizedString" use="required"/>
            <xs:attribute name="PctCached" use="required">
                <xs:simpleType>
                    <xs:restriction base="xs:nonNegativeInteger">
                        <xs:minInclusive value="0"/>
                        <xs:maxInclusive value="100"/>
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:complexType>
    </xs:element>

    <xs:element name="APP_RECORDS">
         <xs:complexType>
            <xs:choice>
                <xs:element ref="APP_RECORD" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
   </xs:element>

    <xs:element name="APP_RECORD">
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Server" type="xs:normalizedString" use="required"/>
            <xs:attribute name="User" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Launched" type="xs:dateTime" use="required"/>
            <xs:attribute name="Shutdown" type="xs:dateTime" use="optional"/>
    </xs:element>

</xs:schema>
```

 

 





