---
title: Новые возможности в UE-V 2.0
description: Новые возможности в UE-V 2.0
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824962"
---
# <span data-ttu-id="e872f-103">Новые возможности в UE-V 2.0</span><span class="sxs-lookup"><span data-stu-id="e872f-103">What's New in UE-V 2.0</span></span>


<span data-ttu-id="e872f-104">Microsoft User Experience Virtualization (UE-V) 2,0 предоставляет эти новые функции и возможности по сравнению с UE-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="e872f-104">Microsoft User Experience Virtualization (UE-V) 2.0 provides these new features and functionality compared to UE-V 1.0.</span></span> <span data-ttu-id="e872f-105">В [заметках о выпуске Microsoft User Experience Virtualization (UE-v) 2,0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) содержатся дополнительные сведения о выпуске UE-v 2,0.</span><span class="sxs-lookup"><span data-stu-id="e872f-105">The [Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) provide more information about the UE-V 2.0 release.</span></span>

## <span data-ttu-id="e872f-106">Кэш на стороне клиента (CSC) больше не требуется</span><span class="sxs-lookup"><span data-stu-id="e872f-106">Client-side cache (CSC) no longer required</span></span>


<span data-ttu-id="e872f-107">В этой версии UE-V представлена **Служба синхронизации**, которая заменяет требование для автономных файлов Windows для поддержки кэша параметров на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="e872f-107">This version of UE-V introduces the **sync provider**, which replaces the requirement for the Windows Offline Files feature to support a client-side cache of settings.</span></span>

<span data-ttu-id="e872f-108">Несмотря на то, что UE-V используется для синхронизации параметров только в том случае, если приложение открыло, закрыто или не заблокировано, или при входе в систему или выходе из нее, поставщик синхронизации также...</span><span class="sxs-lookup"><span data-stu-id="e872f-108">Whereas UE-V used to synchronize settings only when an application opened, closed, or when Windows locked or unlocked, or at logon or logoff, the sync provider also …</span></span>

-   <span data-ttu-id="e872f-109">Синхронизирует локальные приложения и параметры Windows с использованием**событий триггеров**.</span><span class="sxs-lookup"><span data-stu-id="e872f-109">Synchronizes local application and Windows settings out-of-band using "**trigger events**"</span></span>

-   <span data-ttu-id="e872f-110">С помощью **запланированной задачи** синхронизируйте пакет хранилища параметров с любым интервалом, выбранным для корпоративных требований (каждые 30 минут по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="e872f-110">Uses a **scheduled task** to sync the settings storage package in any interval you choose for your enterprise requirements (every 30 minutes by default)</span></span>

<span data-ttu-id="e872f-111">Некоторые условия обеспечивают более частую синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="e872f-111">Certain conditions provide more frequent synchronization.</span></span>

-   <span data-ttu-id="e872f-112">Параметры синхронизируются, когда пользователь нажимает кнопку " **Синхронизировать сейчас** " в новом приложении центра параметров компании.</span><span class="sxs-lookup"><span data-stu-id="e872f-112">Settings synchronize when the user clicks the **Sync Now** button in the new Company Settings Center application.</span></span>

-   <span data-ttu-id="e872f-113">Поставщик синхронизации также может начинаться для одного приложения, не дожидаясь запланированной задачи синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e872f-113">The sync provider can also start for a single application without waiting for the scheduled synchronization task.</span></span> <span data-ttu-id="e872f-114">Например, если приложение закрыто, любые изменения параметров записываются в локальный кэш, а процесс поставщика синхронизации выполняется асинхронно, чтобы переместить эти новые параметры в место хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="e872f-114">For example, when an application is closed, any settings changes are written to the local cache, and the sync provider process runs asynchronously to move those new settings changes to the settings storage location.</span></span>

## <span data-ttu-id="e872f-115">Синхронизация приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="e872f-115">Windows app synchronization</span></span>


<span data-ttu-id="e872f-116">Разработчик приложения для Windows может определить, какие параметры следует синхронизировать, и эти параметры теперь можно записать и синхронизировать с UE-V.</span><span class="sxs-lookup"><span data-stu-id="e872f-116">The developer of a Windows app can define which settings, if any, are to be synchronized, and these settings can now be captured and synchronized with UE-V.</span></span>

<span data-ttu-id="e872f-117">По умолчанию UE-V синхронизирует параметры многих приложений для Windows, включенных в Windows 8 и Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="e872f-117">By default, UE-V synchronizes the settings of many of the Windows apps included in Windows 8 and Windows 8.1.</span></span> <span data-ttu-id="e872f-118">Вы можете изменить список синхронизированных приложений с помощью Windows PowerShell, инструментария управления Windows (WMI) или групповой политики.</span><span class="sxs-lookup"><span data-stu-id="e872f-118">You can modify the list of synchronized apps with Windows PowerShell, Windows Management Instrumentation (WMI), or Group Policy.</span></span>

<span data-ttu-id="e872f-119">**Примечание**  UE-V не синхронизирует параметры приложения для Windows, если пользователи домена связывают свои учетные данные для входа в свою учетную запись Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e872f-119">**Note** UE-V does not synchronize Windows app settings if the domain users link their sign-in credentials to their Microsoft account.</span></span> <span data-ttu-id="e872f-120">Это связывание синхронизирует параметры в Microsoft OneDrive, поэтому UE-V синхронизирует только классическое приложение.</span><span class="sxs-lookup"><span data-stu-id="e872f-120">This linking synchronizes settings to Microsoft OneDrive so UE-V only synchronizes the desktop applications.</span></span>

 

## <span data-ttu-id="e872f-121">Связывание учетной записи Майкрософт</span><span class="sxs-lookup"><span data-stu-id="e872f-121">Microsoft account linking</span></span>


<span data-ttu-id="e872f-122">Синхронизация параметров с помощью OneDrive — это новая возможность для Windows 8 при входе в учетную запись Майкрософт или связывание учетной записи Майкрософт с учетной записью домена.</span><span class="sxs-lookup"><span data-stu-id="e872f-122">Settings synchronization via OneDrive is new to Windows 8 when you are signed in with a Microsoft account or if you link your Microsoft account to your domain account.</span></span> <span data-ttu-id="e872f-123">Если пользователь домена использует UE-V и выполнил вход в учетную запись Майкрософт, то...</span><span class="sxs-lookup"><span data-stu-id="e872f-123">If a domain user uses UE-V and has signed in to a Microsoft account, then…</span></span>

-   <span data-ttu-id="e872f-124">UE-V синхронизирует только параметры для классических приложений</span><span class="sxs-lookup"><span data-stu-id="e872f-124">UE-V only synchronizes settings for desktop applications</span></span>

-   <span data-ttu-id="e872f-125">Учетная запись Майкрософт обрабатывает параметры приложения для Windows и параметры рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="e872f-125">Microsoft account handles Windows app settings and Windows desktop settings</span></span>

## <span data-ttu-id="e872f-126">Центр параметров компании</span><span class="sxs-lookup"><span data-stu-id="e872f-126">Company Settings Center</span></span>


<span data-ttu-id="e872f-127">Вы можете предоставить пользователям доступ к параметрам, которые будут синхронизироваться с помощью приложения в UE-V 2, именуемом центром настроек компании.</span><span class="sxs-lookup"><span data-stu-id="e872f-127">You can provide your users with some control over which settings are synchronized through an application in UE-V 2 called Company Settings Center.</span></span> <span data-ttu-id="e872f-128">Центр параметров компании устанавливается вместе с агентом UE-V и пользователи могут получать доступ к нему с помощью панели управления, **меню "Пуск"** или **начального** экрана, а также с помощью значка "область уведомлений UE-v".</span><span class="sxs-lookup"><span data-stu-id="e872f-128">Company Settings Center is installed along with the UE-V Agent, and users can access it from Control Panel, the **Start** menu or **Start** screen, and from the UE-V notification area icon.</span></span>

<span data-ttu-id="e872f-129">Центр настройки компании показывает, какие параметры синхронизируются, и позволяет пользователям видеть состояние синхронизации UE-V.</span><span class="sxs-lookup"><span data-stu-id="e872f-129">Company Settings Center displays which settings are synchronized and lets users see the synchronization status of UE-V.</span></span> <span data-ttu-id="e872f-130">Если вы разрешаете им, пользователи могут выбрать параметры для синхронизации с помощью центра параметров компании.</span><span class="sxs-lookup"><span data-stu-id="e872f-130">If you let them, users can use Company Settings Center to select which settings to synchronize.</span></span> <span data-ttu-id="e872f-131">Кроме того, они могут нажать кнопку " **Синхронизировать сейчас** ", чтобы немедленно синхронизировать все параметры.</span><span class="sxs-lookup"><span data-stu-id="e872f-131">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span>






## <span data-ttu-id="e872f-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e872f-132">Related topics</span></span>


[<span data-ttu-id="e872f-133">Начало работы с UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="e872f-133">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="e872f-134">Подготовка к развертыванию UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="e872f-134">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="e872f-135">Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.0</span><span class="sxs-lookup"><span data-stu-id="e872f-135">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 





