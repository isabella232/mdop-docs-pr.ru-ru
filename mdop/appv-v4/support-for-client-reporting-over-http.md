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
# Поддержка клиентской отчетности по протоколу HTTP


Версия 4,6 клиента App-V теперь поддерживает использование межhttp-связи при отправке данных отчетов клиента на сервер публикаций. Эта функция поддерживает сценарии, в которых клиент реализовал пользовательский сервер публикаций HTTP (S), настроенный для сбора и обработки клиентских данных.

Дополнительные сведения о серверах публикаций HTTP можно найти в разделе <https://go.microsoft.com/fwlink/?LinkId=157426>

## Создание отчетов по протоколу HTTP для клиентов


Клиент начинает собирать данные при получении атрибута "REPORTing =" TRUE "в XML ответа на обновление публикации с сервера публикаций. При получении этого атрибута клиент отправляет все накопленные данные на сервер публикаций, который отправил обновление публикации. Сведения об этом процессе описаны ниже.

-   Клиент отправляет запрос HTTP GET на сервер публикаций для обновления публикации. Заголовок сообщения содержит настраиваемый заголовок AppV-Op: Refresh, который используется настраиваемым сервером публикаций HTTP (S) для определения типа сообщения.

-   Затем сервер публикаций отправляет XML-сообщение ответа на обновление публикации, содержащее значение "REPORTing =" TRUE ".

-   Затем клиент отправляет запрос HTTP POST на сервер публикаций вместе с данными отчета, собранными с момента предыдущего обновления. Заголовок этого сообщения содержит настраиваемый заголовок "AppV-Op: отчет", который используется настраиваемым сервером публикации HTTP (S) для определения типа сообщения.

В следующей схеме содержатся определенные сведения о пакете и данных приложения, которые отправляются на сервер.

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

 

 





