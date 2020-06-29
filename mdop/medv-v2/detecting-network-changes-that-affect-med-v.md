---
title: Обнаружение изменений в сети, которые влияют на MED-V
description: Обнаружение изменений в сети, которые влияют на MED-V
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823372"
---
# <span data-ttu-id="ebced-103">Обнаружение изменений в сети, которые влияют на MED-V</span><span class="sxs-lookup"><span data-stu-id="ebced-103">Detecting Network Changes that Affect MED-V</span></span>


<span data-ttu-id="ebced-104">В решении Microsoft Enterprise Virtualization (MED-V) 2,0 можно настроить среду для обнаружения некоторых изменений в сети, которые могут возникать после развертывания рабочих областей MED-V и которые могут повлиять на работу MED-V.</span><span class="sxs-lookup"><span data-stu-id="ebced-104">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution lets you configure your environment to detect certain network changes that might occur after MED-V workspaces are deployed and that can affect MED-V.</span></span>

<span data-ttu-id="ebced-105">Эта функция включает компонент, который работает в операционной системе на виртуальной машине и уведомлен об изменениях конфигурации сети на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ebced-105">The feature includes a component running in the guest operating system that is notified of network configuration changes on the host computer.</span></span> <span data-ttu-id="ebced-106">Она позволяет использовать нестандартное или другое приложение, работающее в гостевой учетной записи, для устранения проблем с конечными точками сети, к которым они разрешаются с помощью ESD или приложения.</span><span class="sxs-lookup"><span data-stu-id="ebced-106">It allows a non-Microsoft ESD or other application that is running in the guest to resolve to the same network endpoints that the host ESD or application resolves to.</span></span>

<span data-ttu-id="ebced-107">**Примечание**  Эта функция доступна только в том случае, если виртуальная машина настроена для режима преобразования сетевых адресов (NAT).</span><span class="sxs-lookup"><span data-stu-id="ebced-107">**Note** This feature is only available if the virtual machine is configured for network address translation (NAT) mode.</span></span> <span data-ttu-id="ebced-108">Если виртуальная машина настроена для режима моста, никакие изменения не генерируются.</span><span class="sxs-lookup"><span data-stu-id="ebced-108">If the virtual machine is configured for BRIDGED mode, no change indications are generated.</span></span>

 

<span data-ttu-id="ebced-109">В этом разделе приводятся сведения и инструкции, которые помогут вам отслеживать изменения в сети, которые могут повлиять на работу MED-V.</span><span class="sxs-lookup"><span data-stu-id="ebced-109">This section provides information and instruction to assist you in monitoring those network changes that can affect MED-V.</span></span>

## <span data-ttu-id="ebced-110">Определение сетевых изменений для MED-V</span><span class="sxs-lookup"><span data-stu-id="ebced-110">To detect network changes for MED-V</span></span>


<span data-ttu-id="ebced-111">После развертывания рабочих областей MED-V вы можете отслеживать изменения в некоторых конфигурациях сети, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ebced-111">After you have deployed your MED-V workspaces, you can monitor changes to certain network configurations by preforming the following tasks:</span></span>

1. <span data-ttu-id="ebced-112">Создайте MOF-файл, который будет искать изменения конфигурации сети, которые вы хотите отслеживать.</span><span class="sxs-lookup"><span data-stu-id="ebced-112">Create a Managed Object Format (MOF) file that will look for the network configuration changes that you want to monitor.</span></span> <span data-ttu-id="ebced-113">В следующем коде показан пример MOF-файла, который можно создать.</span><span class="sxs-lookup"><span data-stu-id="ebced-113">The following code shows an example of the MOF file that you can create.</span></span>

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. <span data-ttu-id="ebced-114">Скомпилируйте MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="ebced-114">Compile the MOF file.</span></span>

3. <span data-ttu-id="ebced-115">Установите MOF-файл в гостевой учетной запись.</span><span class="sxs-lookup"><span data-stu-id="ebced-115">Install the MOF file in the guest.</span></span>

<span data-ttu-id="ebced-116">После установки MOF-файла вы можете создать подписку на события, подписку на создание, изменение или удаление событий инструментария управления Windows (WMI) для класса **CCM \ _NetworkAdapters** .</span><span class="sxs-lookup"><span data-stu-id="ebced-116">After you have installed the MOF file, you can create an event subscription that subscribes to Windows Management Instrumentation (WMI) creation, modification, or deletion events for the **CCM\_NetworkAdapters** class.</span></span> <span data-ttu-id="ebced-117">Это обнаруживает следующие изменения узла:</span><span class="sxs-lookup"><span data-stu-id="ebced-117">This detects the following changes to the host:</span></span>

<span data-ttu-id="ebced-118">Есть ли в сети изменения конфигурации, например изменения IP-адреса или сетевого адаптера?</span><span class="sxs-lookup"><span data-stu-id="ebced-118">Are there any configuration changes to the network, such as changes to the IP address or network adapter?</span></span>

<span data-ttu-id="ebced-119">Доступна ли сеть или недоступна?</span><span class="sxs-lookup"><span data-stu-id="ebced-119">Is the network available or unavailable?</span></span>

<span data-ttu-id="ebced-120">Была ли сетевая настройка изменена с режима моста на режим NAT?</span><span class="sxs-lookup"><span data-stu-id="ebced-120">Was the network setup changed from BRIDGED mode to NAT mode?</span></span>

<span data-ttu-id="ebced-121">Была ли сетевая настройка изменена из режима преобразования сетевых адресов в режим моста?</span><span class="sxs-lookup"><span data-stu-id="ebced-121">Was the network setup changed from NAT mode to BRIDGED mode?</span></span>

<span data-ttu-id="ebced-122">Компонент MED-V на главном компьютере отслеживает эти изменения в сети и оповещает гостя об изменении.</span><span class="sxs-lookup"><span data-stu-id="ebced-122">A MED-V component on the host monitors the network for these changes and then signals the guest of the change.</span></span> <span data-ttu-id="ebced-123">Компонент в гостевой системе создает экземпляр WMI для отслеживания изменений в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="ebced-123">A component in the guest creates a WMI instance to monitor the MED-V workspace for these changes.</span></span>

<span data-ttu-id="ebced-124">Созданная подписка на события обеспечивает уведомление в системе WMI, если выполняется одно или несколько из этих сетевых изменений: создание, изменение или удаление.</span><span class="sxs-lookup"><span data-stu-id="ebced-124">The event subscription you created provides notification through the WMI system when one or more of these network changes – creation, modification, or deletion – occurs.</span></span>

## <span data-ttu-id="ebced-125">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ebced-125">Related topics</span></span>


[<span data-ttu-id="ebced-126">Мониторинг рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="ebced-126">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="ebced-127">Управление параметрами рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="ebced-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





