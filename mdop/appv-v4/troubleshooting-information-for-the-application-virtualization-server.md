---
title: Сведения об устранении неполадок на сервере Application Virtualization Server
description: Сведения об устранении неполадок на сервере Application Virtualization Server
author: dansimp
ms.assetid: e9d43d9b-84f2-4d1b-bb90-a13740151e0c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c98ad42a00e20900263d0598822a6381e2df1ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815189"
---
# <span data-ttu-id="7611d-103">Сведения об устранении неполадок на сервере Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="7611d-103">Troubleshooting Information for the Application Virtualization Server</span></span>


<span data-ttu-id="7611d-104">Этот раздел содержит сведения, которые можно использовать для устранения различных проблем на серверах Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="7611d-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Servers.</span></span>

## <span data-ttu-id="7611d-105">Сообщение об ошибке 25017 в журнале настройки после установки сервера</span><span class="sxs-lookup"><span data-stu-id="7611d-105">Warning Message 25017 in Setup Log After Installing the Server</span></span>


<span data-ttu-id="7611d-106">В журнале настройки сервера после установки может быть обнаружено следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="7611d-106">You might find the following message in the server setup log after installation.</span></span>

*<span data-ttu-id="7611d-107">Предупреждение 25017.</span><span class="sxs-lookup"><span data-stu-id="7611d-107">Warning 25017.</span></span> <span data-ttu-id="7611d-108">Программе установки не удалось создать объект маркера Active Directory для сервера.</span><span class="sxs-lookup"><span data-stu-id="7611d-108">The installation Program could not create the Active Directory marker object for the server.</span></span> <span data-ttu-id="7611d-109">Учетной записи, используемой для установки, не предоставлены необходимые права на запись в Active Directory или Active Directory, недоступна.</span><span class="sxs-lookup"><span data-stu-id="7611d-109">The account used to install did not have the sufficient rights to write to Active Directory or Active Directory was unavailable.</span></span>*

<span data-ttu-id="7611d-110">Установщик App-V или Streaming Server создает запись точки подключения к службе в объекте компьютера в доменных службах Active Directory (ADDS), соответствующем компьютеру, на котором установлен сервер, если учетная запись, используемая для запуска установщика, имеет соответствующие права.</span><span class="sxs-lookup"><span data-stu-id="7611d-110">The App-V Management or Streaming Server installer creates a Service Connection Point entry under the Computer object in Active Directory Domain Services (ADDS) that corresponds to the computer on which the server is installed if the account used to run the installer has the appropriate rights.</span></span> <span data-ttu-id="7611d-111">Ошибка при создании этой записи не приведет к сбою установки, и это не повлияет на работу продукта в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7611d-111">Failure to create this entry will not cause the install to fail and this should not otherwise affect the functioning of the product.</span></span> <span data-ttu-id="7611d-112">Вероятная причина любого сбоя заключается в том, что учетная запись пользователя, используемая для запуска установки, не имеет достаточных прав на запись для добавления.</span><span class="sxs-lookup"><span data-stu-id="7611d-112">The likely cause of any failure is that the user account used to run the install did not have sufficient rights to write to ADDS.</span></span> <span data-ttu-id="7611d-113">Несмотря на то, что регистрация сервера App-V в разделе "надстройки" не является обязательной, одним из преимуществ этого является использование средств централизованного управления для поиска сервера App-V для инвентаризации и целей управления.</span><span class="sxs-lookup"><span data-stu-id="7611d-113">Although registering the App-V server in ADDS is optional, one benefit of doing so enables centralized management tools to locate the App-V server for inventory and management purposes.</span></span>

## <span data-ttu-id="7611d-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7611d-114">Related topics</span></span>


[<span data-ttu-id="7611d-115">Сервер Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="7611d-115">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





