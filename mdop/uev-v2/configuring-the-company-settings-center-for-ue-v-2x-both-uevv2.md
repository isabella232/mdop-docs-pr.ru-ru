---
title: Настройка центра параметров компании для UE-V 2. x
description: Настройка центра параметров компании для UE-V 2. x
author: dansimp
ms.assetid: 48fadb0a-c0dc-4287-9474-f94ce1417003
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0226b3c156a6d6ca39b0214de8acf0c5990db349
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823292"
---
# <span data-ttu-id="64734-103">Настройка центра параметров компании для UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="64734-103">Configuring the Company Settings Center for UE-V 2.x</span></span>


<span data-ttu-id="64734-104">Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 и 2,1 SP1 включает новое приложение, центр параметров компании, который помогает пользователям управлять параметрами синхронизации.</span><span class="sxs-lookup"><span data-stu-id="64734-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 include a new application, the Company Settings Center, which helps users manage settings to synchronize.</span></span> <span data-ttu-id="64734-105">Центр параметров компании устанавливается с помощью агента UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="64734-105">The Company Settings Center is installed by using the UE-V Agent.</span></span> <span data-ttu-id="64734-106">Пользователи получают доступ к центру параметров компании на панели управления, в меню " **Пуск** " или на **начальном** экране, а также с помощью значка в области уведомлений UE-V.</span><span class="sxs-lookup"><span data-stu-id="64734-106">Users access the Company Settings Center in Control Panel, in the **Start** menu or on the **Start** screen, and via the UE-V notification area icon.</span></span> <span data-ttu-id="64734-107">Центр настройки компании показывает, какие параметры синхронизируются, и помогает пользователям видеть состояние синхронизации UE-V.</span><span class="sxs-lookup"><span data-stu-id="64734-107">Company Settings Center displays which settings are synchronized and helps users see the synchronization status of UE-V.</span></span> <span data-ttu-id="64734-108">Пользователи могут использовать центр параметров компании, чтобы выбрать, какие приложения или компоненты Windows будут синхронизировать параметры между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="64734-108">Users can use the Company Settings Center to select which applications or Windows features synchronize their settings between computers.</span></span> <span data-ttu-id="64734-109">Кроме того, они могут нажать кнопку " **Синхронизировать сейчас** ", чтобы немедленно синхронизировать все параметры.</span><span class="sxs-lookup"><span data-stu-id="64734-109">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span> <span data-ttu-id="64734-110">Администратор также может включить ссылку на службу поддержки в центре параметров компании.</span><span class="sxs-lookup"><span data-stu-id="64734-110">The administrator can also include a link for support in the Company Settings Center.</span></span>

## <span data-ttu-id="64734-111">Сведения о центре параметров компании</span><span class="sxs-lookup"><span data-stu-id="64734-111">About the Company Settings Center</span></span>


<span data-ttu-id="64734-112">Классическое приложение центра настройки компании предоставляет пользователям сведения о синхронизации параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="64734-112">The Company Settings Center desktop application provides users with information about UE-V settings synchronization.</span></span> <span data-ttu-id="64734-113">Центр настройки компании доступен различными способами:</span><span class="sxs-lookup"><span data-stu-id="64734-113">The Company Settings Center is accessible in several different ways:</span></span>

-   <span data-ttu-id="64734-114">Значок области уведомлений с параметром групповой политики **значка панели задач** или конфигурацией Windows PowerShell, в области уведомлений появится значок UE-V.</span><span class="sxs-lookup"><span data-stu-id="64734-114">Notification area icon – With the **Tray Icon** Group Policy setting or Windows PowerShell configuration enabled, the UE-V icon appears in the notification area.</span></span> <span data-ttu-id="64734-115">Щелкните значок UE-V, чтобы открыть центр настройки компании.</span><span class="sxs-lookup"><span data-stu-id="64734-115">Click the UE-V icon to open the Company Settings Center.</span></span>

    <span data-ttu-id="64734-116">**Примечание**  Значок области уведомлений можно отключить, используя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="64734-116">**Note** The notification area icon can be disabled by using the following settings:</span></span>

    -   <span data-ttu-id="64734-117">Параметр групповой политики:</span><span class="sxs-lookup"><span data-stu-id="64734-117">Group Policy setting:</span></span> `Policy Tray Icon`

    -   <span data-ttu-id="64734-118">Командлет Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="64734-118">Windows PowerShell cmdlet:</span></span> `TrayIconEnabled`

    -   <span data-ttu-id="64734-119">Элемент конфигурации в пакете конфигурации UE-V для SystemCenter2012 ConfigurationManager:</span><span class="sxs-lookup"><span data-stu-id="64734-119">Configuration item in the UE-V Configuration Pack for SystemCenter2012 ConfigurationManager:</span></span> `Tray icon enabled`

     

-   <span data-ttu-id="64734-120">Приложение панели управления — на панели управления выберите **Оформление и персонализация**, а затем щелкните **Центр настройки компании**.</span><span class="sxs-lookup"><span data-stu-id="64734-120">Control Panel application – In Control Panel, browse to **Appearance and Personalization**, and then click **Company Settings Center**.</span></span>

-   <span data-ttu-id="64734-121">Уведомление о первом использовании — если не отключено, агент UE-V Agent предупреждает пользователя о том, что параметры теперь синхронизируются, когда агент UE-V запускается в первый раз на компьютере.</span><span class="sxs-lookup"><span data-stu-id="64734-121">First use notification – Unless disabled, the UE-V Agent alerts the user that settings are now synchronized when the UE-V agent runs for the first time on a computer.</span></span> <span data-ttu-id="64734-122">Щелкните диалоговое окно уведомления, чтобы открыть центр настройки компании.</span><span class="sxs-lookup"><span data-stu-id="64734-122">Click the notification dialog box to open the Company Settings Center.</span></span>

-   <span data-ttu-id="64734-123">**Начальный** экран или меню " **Пуск** " содержит ссылку на центр параметров компании.</span><span class="sxs-lookup"><span data-stu-id="64734-123">The **Start** screen or **Start** menu includes a link to the Company Settings Center.</span></span> <span data-ttu-id="64734-124">Поиск приложения в центре параметров компании.</span><span class="sxs-lookup"><span data-stu-id="64734-124">A search for Company Settings Center finds the application.</span></span>

## <span data-ttu-id="64734-125">Настройка ссылки "поддержка" в центре параметров компании</span><span class="sxs-lookup"><span data-stu-id="64734-125">Configuring the support link in the Company Settings Center</span></span>


<span data-ttu-id="64734-126">Центр параметров компании может включать гиперссылку, которую пользователь может щелкнуть для получения поддержки с проблемами синхронизации параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="64734-126">The Company Settings Center can include a hyperlink that users can click to get support with UE-V settings synchronization problems.</span></span> <span data-ttu-id="64734-127">Эта ссылка может открыть любой допустимый протокол URL-адреса, например http://для веб-страницы или mailto://для электронной почты.</span><span class="sxs-lookup"><span data-stu-id="64734-127">This link can open any valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span> <span data-ttu-id="64734-128">Ссылку на службу поддержки можно настроить с помощью групповой политики, Windows PowerShell или пакета конфигурации System Center 2012 Configuration Manager UE-V.</span><span class="sxs-lookup"><span data-stu-id="64734-128">The support link can be configured by using Group Policy, Windows PowerShell, or the System Center 2012 Configuration Manager UE-V Configuration Pack.</span></span>

**<span data-ttu-id="64734-129">Настройка ссылки на службу поддержки центра параметров компании</span><span class="sxs-lookup"><span data-stu-id="64734-129">How to configure the Company Settings Center support link</span></span>**

1.  <span data-ttu-id="64734-130">Откройте предпочтительный инструмент управления:</span><span class="sxs-lookup"><span data-stu-id="64734-130">Open your preferred management tool:</span></span>

    -   <span data-ttu-id="64734-131">**Групповая политика** — если вы еще не сделали этого, скачайте шаблон ADMX для UE-V 2 из [административных шаблонов MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393941).</span><span class="sxs-lookup"><span data-stu-id="64734-131">**Group Policy** - If you have not already done so, download the ADMX template for UE-V 2 from [MDOP Administrative Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941).</span></span>

    -   <span data-ttu-id="64734-132">**Windows PowerShell** — на компьютере с установленным агентом UE-V откройте **Windows PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="64734-132">**Windows PowerShell** – On a computer with the UE-V Agent installed, open **Windows PowerShell**.</span></span> <span data-ttu-id="64734-133">Дополнительные сведения об администрировании UE-V с помощью Windows PowerShell можно найти в разделе [Администрирование UE-v 2. x с помощью Windows PowerShell и WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="64734-133">For more information about administering UE-V by using Windows PowerShell, see [Administering UE-V 2.x with Windows PowerShell and WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    -   <span data-ttu-id="64734-134">**Пакет конфигурации System Center 2012 для Microsoft User Experience Virtualization (UE-v)** — импортируйте пакет конфигурации UE-v и следуйте инструкциям по созданию элементов конфигурации в документации по пакету конфигурации.</span><span class="sxs-lookup"><span data-stu-id="64734-134">**System Center 2012 Configuration Pack for Microsoft User Experience Virtualization (UE-V)** – Import the UE-V Configuration Pack and follow the Configuration Pack documentation to create configuration items.</span></span> <span data-ttu-id="64734-135">Дополнительные сведения о пакете конфигурации UE-V можно найти в разделе [Настройка UE-v 2. x с помощью System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="64734-135">For more information about the UE-V Configuration Pack, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

2.  <span data-ttu-id="64734-136">Измените параметры для указанных ниже политик.</span><span class="sxs-lookup"><span data-stu-id="64734-136">Edit the settings for the following policies:</span></span>

    -   <span data-ttu-id="64734-137">**Текст ссылки для контакта** . Этот параметр указывает текст гиперссылки на URL-адрес контакта в центре параметров компании.</span><span class="sxs-lookup"><span data-stu-id="64734-137">**Contact IT Link Text** - This setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span> <span data-ttu-id="64734-138">Если этот параметр включен, в центре параметров компании отображается указанный текст в ссылке на URL-адрес контакта.</span><span class="sxs-lookup"><span data-stu-id="64734-138">If you enable this setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span>

        -   <span data-ttu-id="64734-139">Параметры групповой политики:</span><span class="sxs-lookup"><span data-stu-id="64734-139">Group Policy settings:</span></span> `Contact IT Link Text`

        -   <span data-ttu-id="64734-140">Командлет Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="64734-140">Windows PowerShell cmdlet:</span></span> `ContactITDescription`

        -   <span data-ttu-id="64734-141">Элемент конфигурации пакета конфигурации:</span><span class="sxs-lookup"><span data-stu-id="64734-141">Configuration Pack configuration item:</span></span> `IT contact descriptive text`

    -   <span data-ttu-id="64734-142">**Обратитесь к URL-адресу** . Этот параметр указывает URL-адрес ссылки на контакт в центре настройки компании в ДОПУСТИМОМ URL-протоколе, например http://для веб-страницы или mailto://для электронной почты.</span><span class="sxs-lookup"><span data-stu-id="64734-142">**Contact IT URL** - This setting specifies the URL for the Contact IT link in the Company Settings Center in a valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span>

        -   <span data-ttu-id="64734-143">Параметры групповой политики:</span><span class="sxs-lookup"><span data-stu-id="64734-143">Group Policy settings:</span></span> `Contact IT URL`

        -   <span data-ttu-id="64734-144">Командлет Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="64734-144">Windows PowerShell cmdlet:</span></span> `ContactITUrl`

        -   <span data-ttu-id="64734-145">Элемент конфигурации пакета конфигурации:</span><span class="sxs-lookup"><span data-stu-id="64734-145">Configuration Pack configuration item:</span></span> `IT contact URL`

3.  <span data-ttu-id="64734-146">Развертывание параметров на компьютерах пользователей с помощью средства управления.</span><span class="sxs-lookup"><span data-stu-id="64734-146">Deploy settings to users’ computers by using the management tool.</span></span>






 

 





