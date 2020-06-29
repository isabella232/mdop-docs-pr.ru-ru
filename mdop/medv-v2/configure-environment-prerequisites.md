---
title: Настройка необходимых компонентов среды
description: Настройка необходимых компонентов среды
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826449"
---
# <span data-ttu-id="9703c-103">Настройка необходимых компонентов среды</span><span class="sxs-lookup"><span data-stu-id="9703c-103">Configure Environment Prerequisites</span></span>


<span data-ttu-id="9703c-104">Прежде чем вы сможете развернуть и запустить виртуализацию классической версии Microsoft Enterprise (MED-V) 2,0, убедитесь, что ваша среда отвечает указанным ниже минимальным требованиям.</span><span class="sxs-lookup"><span data-stu-id="9703c-104">Before you can deploy and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you must ensure that your environment meets the following minimum prerequisites.</span></span>

**<span data-ttu-id="9703c-105">Windows 7;</span><span class="sxs-lookup"><span data-stu-id="9703c-105">Windows 7</span></span>**

<span data-ttu-id="9703c-106">Агент хоста MED-V и диспетчер рабочих областей MED-V поддерживаются только в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="9703c-106">The MED-V Host Agent and the MED-V Workspace Packager are only supported in Windows 7 or newer.</span></span>

**<span data-ttu-id="9703c-107">Windows XP SP3</span><span class="sxs-lookup"><span data-stu-id="9703c-107">Windows XP SP3</span></span>**

<span data-ttu-id="9703c-108">Гостевой агент MED-V поддерживается только в Windows XP с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="9703c-108">The MED-V Guest Agent is only supported in Windows XP SP3.</span></span>

**<span data-ttu-id="9703c-109">.NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="9703c-109">.NET Framework 3.5 SP1</span></span>**

<span data-ttu-id="9703c-110">Для агентов и виртуальных машин MED-V и "гость" и для диспетчера рабочих областей MED-V требуется Microsoft .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9703c-110">The MED-V Host and Guest agents and the MED-V Workspace Packager require the Microsoft .NET Framework 3.5 SP1.</span></span>

<span data-ttu-id="9703c-111">**Важно!**  Кроме того, необходимо установить обновление [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) , которое предназначено для устранения нескольких известных проблем с совместимостью приложений.</span><span class="sxs-lookup"><span data-stu-id="9703c-111">**Important** You must also install the update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950), which addresses several known application compatibility issues.</span></span>

 

<span data-ttu-id="9703c-112">**Примечание**  Необходимо вручную установить .NET Framework 3,5 SP1 и Update KB959209 в образ Windows Virtual PC, подготовленный для использования с MED-V.</span><span class="sxs-lookup"><span data-stu-id="9703c-112">**Note** You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="9703c-113">Однако по умолчанию платформа Microsoft .NET Framework 3,5 с пакетом обновления 1 (SP1) и обновление включается при установке Windows 7 на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9703c-113">However, by default, the Microsoft .NET Framework 3.5 SP1 and the update are included when you install Windows 7 on the host computer.</span></span>

 

**<span data-ttu-id="9703c-114">Инфраструктура службы каталогов Active Directory</span><span class="sxs-lookup"><span data-stu-id="9703c-114">An Active Directory Infrastructure</span></span>**

<span data-ttu-id="9703c-115">Групповая политика обеспечивает централизованное управление и настройку операционных систем, приложений и параметров пользователей в среде Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9703c-115">Group Policy provides the centralized management and configuration of operating systems, applications, and users' settings in an Active Directory environment.</span></span>

## <span data-ttu-id="9703c-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9703c-116">Related topics</span></span>


[<span data-ttu-id="9703c-117">Настройка необходимых компонентов для установки</span><span class="sxs-lookup"><span data-stu-id="9703c-117">Configure Installation Prerequisites</span></span>](configure-installation-prerequisites.md)

[<span data-ttu-id="9703c-118">Высокоуровневая архитектура</span><span class="sxs-lookup"><span data-stu-id="9703c-118">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="9703c-119">Поддерживаемые конфигурации MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="9703c-119">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





