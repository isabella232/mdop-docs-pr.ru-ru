---
title: Безопасность классического клиента App-V
description: Безопасность классического клиента App-V
author: dansimp
ms.assetid: 216b9c16-7bb4-4f94-b9d8-810501285008
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 26add6f855780113613cf1591c41722643954477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822319"
---
# <span data-ttu-id="c9bfb-103">Безопасность классического клиента App-V</span><span class="sxs-lookup"><span data-stu-id="c9bfb-103">App-V Desktop Client Security</span></span>


<span data-ttu-id="c9bfb-104">Классическое приложение App-V предоставляет множество улучшений системы безопасности, недоступных в предыдущих версиях продукта.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-104">The App-V Desktop Client provides many security enhancements that were not available in previous versions of the product.</span></span> <span data-ttu-id="c9bfb-105">Эти изменения обеспечивают более высокий уровень безопасности по умолчанию и настройкой параметров клиента.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-105">These changes provide higher levels of security by default and through configuration of the client settings.</span></span>

<span data-ttu-id="c9bfb-106">**Примечание**  При установке клиента App-V на компьютере по умолчанию используется наиболее безопасный параметр.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-106">**Note** When you install the App-V Desktop Client on a computer, the software defaults to the most secure settings.</span></span> <span data-ttu-id="c9bfb-107">Однако при обновлении предыдущие параметры клиента сохраняются.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-107">However, when upgrading, the previous settings of the client persist.</span></span>

 

<span data-ttu-id="c9bfb-108">По умолчанию классическое приложение App-V настраивается только с разрешениями, необходимыми для того, чтобы пользователи без прав администратора могли выполнять публикации и приложения-потоки.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-108">By default, the App-V Desktop Client is configured only with the permissions required to allow a non-administrative user to perform a publishing refresh and stream applications.</span></span> <span data-ttu-id="c9bfb-109">В классическом клиенте App-V включены следующие дополнительные возможности обеспечения безопасности:</span><span class="sxs-lookup"><span data-stu-id="c9bfb-109">Additional security enhancements provided in the App-V Desktop Client include the following:</span></span>

-   <span data-ttu-id="c9bfb-110">По умолчанию обновление кэша OSD разрешено только процессом обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-110">By default, an OSD cache update is allowed only by the publishing refresh process.</span></span>

-   <span data-ttu-id="c9bfb-111">Файл журнала ( `sftlog.txt` ) доступен только для учетных записей, которые имеют локальный административный доступ к клиенту.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-111">The log file (`sftlog.txt`) is accessible only by accounts with local administrative access to the client.</span></span>

-   <span data-ttu-id="c9bfb-112">Файл журнала теперь имеет максимальный размер.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-112">The log file now has a maximum size.</span></span>

-   <span data-ttu-id="c9bfb-113">Управление файлами журнала осуществляется с помощью параметров архива.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-113">The log files are managed through archive settings.</span></span>

-   <span data-ttu-id="c9bfb-114">Ведение журнала системных событий теперь выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-114">System Event logging is now performed.</span></span>

## <span data-ttu-id="c9bfb-115">Разрешения</span><span class="sxs-lookup"><span data-stu-id="c9bfb-115">Permissions</span></span>


<span data-ttu-id="c9bfb-116">После установки клиента для настольных компьютеров вы можете настроить другие параметры безопасности с помощью консоли управления (MMC) или отдельного клиента, используя реестр или шаблон ADM, предоставленный корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-116">After you install the Desktop Client, you can configure other security settings through the MMC, or on an individual client by using the registry or the ADM Template provided by Microsoft.</span></span> <span data-ttu-id="c9bfb-117">У клиента App-V есть разрешения, которые можно задать, чтобы запретить пользователям, не являющимся администраторами, доступ ко всем функциям настольного клиента.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-117">The App-V Desktop Client has permissions that you can set to restrict non-administrative users from accessing all the features of the Desktop Client.</span></span> <span data-ttu-id="c9bfb-118">Полный список разрешений можно найти в файле справки клиента App-V или в руководстве по работе с App-V.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-118">For a full list of permissions, please see the App-V Client Help file or App-V Operations Guide.</span></span>

<span data-ttu-id="c9bfb-119">**Важно!**  Тщательно изучите последствия изменения прав доступа, особенно на компьютерах, совместно используемых несколькими пользователями, например на серверах терминалов.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-119">**Important** Carefully consider the consequences of changing access rights, especially on systems that are shared by multiple users, such as Terminal Servers.</span></span>

 

<span data-ttu-id="c9bfb-120">**Примечание**  Если у пользователей в среде есть права локального администратора для своих компьютеров, эти разрешения игнорируются.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-120">**Note** If users in the environment have local administrator privileges for their computers, the permissions are ignored.</span></span>

 

### <span data-ttu-id="c9bfb-121">Шаблон ADM</span><span class="sxs-lookup"><span data-stu-id="c9bfb-121">ADM Template</span></span>

<span data-ttu-id="c9bfb-122">Microsoft Application Virtualization (App-V) предлагает шаблон ADM, который можно использовать для настройки наиболее распространенных параметров клиента с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-122">Microsoft Application Virtualization (App-V) introduces an ADM Template that you can use to configure the most common client settings through Group Policies.</span></span> <span data-ttu-id="c9bfb-123">Этот шаблон позволяет администраторам реализовывать и изменять многие параметры клиента с помощью централизованной модели администрирования.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-123">This template enables administrators to implement and change many of the client settings through a centralized administration model.</span></span> <span data-ttu-id="c9bfb-124">Некоторые параметры, доступные в шаблоне ADM, являются параметрами безопасности.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-124">Some of the settings available in the ADM Template are security settings.</span></span>

<span data-ttu-id="c9bfb-125">**Важно!**  При использовании шаблона ADM следует помнить, что параметры являются параметрами настройки групповой политики, а не полностью управляемыми групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-125">**Important** When using the ADM Template, remember that the settings are Group Policy preference settings and not fully managed Group Policies.</span></span>

 

<span data-ttu-id="c9bfb-126">Полное описание шаблона ADM, определенные параметры и руководство по развертыванию клиентов в среде можно найти в статье шаблон ADM App-V [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063) .</span><span class="sxs-lookup"><span data-stu-id="c9bfb-126">For a full description of the ADM Template, the specific settings, and guidance to successfully deploy clients in your environment, see the App-V ADM Template white paper at [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063).</span></span>

## <span data-ttu-id="c9bfb-127">Удаление сопоставлений типов файлов OSD</span><span class="sxs-lookup"><span data-stu-id="c9bfb-127">Removing OSD File Type Associations</span></span>


<span data-ttu-id="c9bfb-128">Если в вашей организации не требуется открывать приложения непосредственно из OSD, вы можете повысить уровень безопасности путем удаления сопоставлений типов файлов на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-128">If your organization does not require users to open applications directly from an OSD file, you can enhance security by removing the file type associations on the client.</span></span> <span data-ttu-id="c9bfb-129">Удалите `HKEY_CURRENT_USERS` клавиши для OSD и `Softgird.osd.file` с помощью редактора реестра.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-129">Remove the `HKEY_CURRENT_USERS` keys for OSD and `Softgird.osd.file` by using the registry editor.</span></span> <span data-ttu-id="c9bfb-130">Вы можете добавить этот процесс в сценарий входа или в сценарий после установки, чтобы автоматизировать эти изменения.</span><span class="sxs-lookup"><span data-stu-id="c9bfb-130">You can put this process into a logon script or into a post-installation script to automate these changes.</span></span>

 

 





