---
title: Новые возможности в UE-V 2.1 с пакетом обновления 1 (SP1)
description: Новые возможности в UE-V 2.1 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827429"
---
# <span data-ttu-id="d203e-103">Новые возможности в UE-V 2.1 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="d203e-103">What's New in UE-V 2.1 SP1</span></span>


<span data-ttu-id="d203e-104">Виртуализация взаимодействия с пользователем 2,1 SP1 предоставляет новые функции и возможности по сравнению с UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="d203e-104">User Experience Virtualization 2.1 SP1 provides these new features and functionality compared to UE-V 2.1.</span></span> <span data-ttu-id="d203e-105">В [заметках о выпуске пакета обновления 1 (SP1) для Microsoft User Experience Virtualization (UE-v) 2,1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) , более подробная информация о выпуске UE-v 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="d203e-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) provide more information about the UE-V 2.1 SP1 release.</span></span>

## <span data-ttu-id="d203e-106">Поддержка в Windows 10</span><span class="sxs-lookup"><span data-stu-id="d203e-106">Support for Windows 10</span></span>


<span data-ttu-id="d203e-107">UE-V 2,1 SP1 добавляет поддержку для Windows 10 в дополнение к тому же программному обеспечению, которое поддерживается в более ранних версиях UE-V.</span><span class="sxs-lookup"><span data-stu-id="d203e-107">UE-V 2.1 SP1 adds support for Windows 10, in addition to the same software that is supported in earlier versions of UE-V.</span></span>

### <span data-ttu-id="d203e-108">Совместимость с Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="d203e-108">Compatibility with Microsoft Azure</span></span>

<span data-ttu-id="d203e-109">Windows 10 позволяет корпоративным пользователям синхронизировать параметры приложений Windows и операционной системы Windows с Azure вместо OneDrive.</span><span class="sxs-lookup"><span data-stu-id="d203e-109">Windows 10 lets enterprise users synchronize Windows app settings and Windows operating system settings to Azure instead of to OneDrive.</span></span> <span data-ttu-id="d203e-110">Вы можете использовать функциональные возможности Windows 10 Enterprise Sync вместе с UE-V для локальных компьютеров, подключенных к домену.</span><span class="sxs-lookup"><span data-stu-id="d203e-110">You can use the Windows 10 enterprise sync functionality together with UE-V for on-premises domain-joined computers only.</span></span> <span data-ttu-id="d203e-111">Для включения сосуществования между Windows 10 и UE-V необходимо отключить следующие шаблоны UE-V с помощью PowerShell для каждой клиентской или групповой политики.</span><span class="sxs-lookup"><span data-stu-id="d203e-111">To enable coexistence between Windows 10 and UE-V, you must disable the following UE-V templates using either PowerShell on each client or Group Policy.</span></span>

<span data-ttu-id="d203e-112">В групповой политике в разделе виртуализация взаимодействия с пользователем (Майкрософт) настройте следующие параметры политики.</span><span class="sxs-lookup"><span data-stu-id="d203e-112">In Group Policy, under the Microsoft User Experience Virtualization node, configure these policy settings:</span></span>

-   <span data-ttu-id="d203e-113">Включить параметр "не синхронизировать приложения для Windows"</span><span class="sxs-lookup"><span data-stu-id="d203e-113">Enable “Do Not Synchronize Windows Apps”</span></span>

-   <span data-ttu-id="d203e-114">Отключение параметра "Синхронизация параметров Windows"</span><span class="sxs-lookup"><span data-stu-id="d203e-114">Disable “Sync Windows Settings”</span></span>

### <span data-ttu-id="d203e-115">Изменение поведения синхронизации параметров для поддержки Windows 10</span><span class="sxs-lookup"><span data-stu-id="d203e-115">Settings Synchronization Behavior Changed for Windows 10 Support</span></span>

<span data-ttu-id="d203e-116">UE-V 2,1 SP1 перемещает параметры панели задач между устройствами с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d203e-116">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="d203e-117">Однако UE-V не синхронизирует параметры панели задач между устройствами и устройствами с Windows 10, работающими на предыдущих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="d203e-117">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>

<span data-ttu-id="d203e-118">Кроме того, UE-V 2,1 SP1 не синхронизирует параметры между Microsoft калькулятором в Windows 10 и калькулятором Microsoft в предыдущих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="d203e-118">In addition, UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>

## <span data-ttu-id="d203e-119">Добавлена поддержка для сетевых принтеров с роумингом</span><span class="sxs-lookup"><span data-stu-id="d203e-119">Support Added for Roaming Network Printers</span></span>


<span data-ttu-id="d203e-120">UE-V 2,1 SP1 позволяет сетевым принтерам перемещаться между устройствами, чтобы пользователь получил доступ к своим сетевым принтерам при входе на любое устройство в сети.</span><span class="sxs-lookup"><span data-stu-id="d203e-120">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="d203e-121">Это включает в себя перемещающий принтер, который они задали по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d203e-121">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="d203e-122">Для перемещения принтеров в UE-V требуется один из следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="d203e-122">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="d203e-123">Сервер печати может загрузить требуемый драйвер при перемещении на новое устройство.</span><span class="sxs-lookup"><span data-stu-id="d203e-123">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="d203e-124">Драйвер для перемещаемого сетевого принтера предварительно установлен на любом устройстве, которому нужен доступ к сетевому принтеру.</span><span class="sxs-lookup"><span data-stu-id="d203e-124">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="d203e-125">Драйвер принтера можно получить из центра обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="d203e-125">The printer driver can be obtained from Windows Update.</span></span>

<span data-ttu-id="d203e-126">**Примечание**  Функция роуминга принтеров UE-V **не** позволяет перемещать параметры принтера или настройки, например двустороннюю печать.</span><span class="sxs-lookup"><span data-stu-id="d203e-126">**Note** The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>

 

## <span data-ttu-id="d203e-127">Шаблон расположения параметров в Office 2013</span><span class="sxs-lookup"><span data-stu-id="d203e-127">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="d203e-128">UE-V 2,1 и 2,1 SP1 включают шаблон расположения параметров Microsoft Office 2013 с улучшенной поддержкой подписи Outlook.</span><span class="sxs-lookup"><span data-stu-id="d203e-128">UE-V 2.1 and 2.1 SP1 include the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="d203e-129">Добавлена синхронизация параметров подписи по умолчанию для новых, ответных и пересылаемых сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d203e-129">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="d203e-130">Пользователям больше не нужно выбирать параметры подписи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d203e-130">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="d203e-131">**Примечание**  Профиль Outlook должен быть создан для любого устройства, на котором пользователь хочет синхронизировать свою подпись Outlook.</span><span class="sxs-lookup"><span data-stu-id="d203e-131">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="d203e-132">Если профиль еще не создан, пользователь может создать его, а затем перезапустить Outlook на этом устройстве, чтобы включить синхронизацию подписей.</span><span class="sxs-lookup"><span data-stu-id="d203e-132">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="d203e-133">Ранее UE-V содержал шаблоны расположений параметров Microsoft Office 2010, которые были автоматически распределены и зарегистрированы в агенте UE-V.</span><span class="sxs-lookup"><span data-stu-id="d203e-133">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="d203e-134">UE-V 2,1 работает с Office 365, чтобы определить, будут ли параметры Office 2013 перемещены в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d203e-134">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="d203e-135">Если параметры перемещаются в Office 365, они не перемещаются UE-V.</span><span class="sxs-lookup"><span data-stu-id="d203e-135">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="d203e-136">[Общие сведения о параметрах пользователей и роуминга для Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) .</span><span class="sxs-lookup"><span data-stu-id="d203e-136">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="d203e-137">Чтобы включить синхронизацию параметров с помощью UE-V 2,1, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="d203e-137">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="d203e-138">Отключение синхронизации Office 365 с помощью групповой политики</span><span class="sxs-lookup"><span data-stu-id="d203e-138">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="d203e-139">Не включайте процесс синхронизации Office 365 во время установки Office 2013</span><span class="sxs-lookup"><span data-stu-id="d203e-139">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="d203e-140">UE-V 2,1 поставляется с [шаблонами office 2013 и office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="d203e-140">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="d203e-141">В этом выпуске удаляются шаблоны Office 2007.</span><span class="sxs-lookup"><span data-stu-id="d203e-141">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="d203e-142">Пользователи по-прежнему могут использовать шаблоны Office 2007 с UE-V 2,0 или более ранней версии, но по-прежнему смогут получать шаблоны из галереи шаблонов UE-V, расположенной [здесь](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="d203e-142">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>






## <span data-ttu-id="d203e-143">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d203e-143">Related topics</span></span>


[<span data-ttu-id="d203e-144">Начало работы с UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="d203e-144">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="d203e-145">Подготовка к развертыванию UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="d203e-145">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="d203e-146">Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.1 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="d203e-146">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





