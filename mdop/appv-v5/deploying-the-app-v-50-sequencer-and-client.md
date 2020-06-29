---
title: Развертывание программы Sequencer и клиента App-V 5.0
description: Развертывание программы Sequencer и клиента App-V 5.0
author: dansimp
ms.assetid: 84cc84bd-5bc0-41aa-9519-0ded2932c078
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 647ea12018bf966592b9e831d532c7c08093d367
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814597"
---
# <span data-ttu-id="c065e-103">Развертывание программы Sequencer и клиента App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c065e-103">Deploying the App-V 5.0 Sequencer and Client</span></span>


<span data-ttu-id="c065e-104">Приложение App-V 5,0 и клиент позволяют администраторам виртуализировать и запускать виртуализированные приложения.</span><span class="sxs-lookup"><span data-stu-id="c065e-104">The App-V 5.0 Sequencer and client enable administrators to virtualize and run virtualized applications.</span></span>

## <span data-ttu-id="c065e-105">Развертывание клиента</span><span class="sxs-lookup"><span data-stu-id="c065e-105">Deploy the client</span></span>


<span data-ttu-id="c065e-106">Клиент App-V 5,0 является компонентом, который запускает виртуализированное приложение на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="c065e-106">The App-V 5.0 client is the component that runs a virtualized application on a target computer.</span></span> <span data-ttu-id="c065e-107">Клиент позволяет пользователям взаимодействовать со значками и дважды щелкать типы файлов, чтобы они могли запускать виртуализированное приложение.</span><span class="sxs-lookup"><span data-stu-id="c065e-107">The client enables users to interact with icons and to double-click file types, so that they can start a virtualized application.</span></span> <span data-ttu-id="c065e-108">Клиент также может получить содержимое виртуального приложения с сервера управления.</span><span class="sxs-lookup"><span data-stu-id="c065e-108">The client can also obtain the virtual application content from the management server.</span></span>

[<span data-ttu-id="c065e-109">Развертывание клиента App-V</span><span class="sxs-lookup"><span data-stu-id="c065e-109">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)

[<span data-ttu-id="c065e-110">Удаление клиента App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c065e-110">How to Uninstall the App-V 5.0 Client</span></span>](how-to-uninstall-the-app-v-50-client.md)

[<span data-ttu-id="c065e-111">Развертывание приложения App-V 4,6 и клиента App-V 5,0 на том же компьютере</span><span class="sxs-lookup"><span data-stu-id="c065e-111">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

## <span data-ttu-id="c065e-112">Параметры конфигурации клиента</span><span class="sxs-lookup"><span data-stu-id="c065e-112">Client Configuration Settings</span></span>


<span data-ttu-id="c065e-113">Клиент App-V 5,0 хранит свою конфигурацию в реестре.</span><span class="sxs-lookup"><span data-stu-id="c065e-113">The App-V 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="c065e-114">Вы можете собрать полезные сведения о клиенте, если вы понимаете формат данных в реестре.</span><span class="sxs-lookup"><span data-stu-id="c065e-114">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="c065e-115">Вы также можете настроить множество клиентских действий, изменяя записи в реестре.</span><span class="sxs-lookup"><span data-stu-id="c065e-115">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="c065e-116">Сведения о параметрах конфигурации клиента</span><span class="sxs-lookup"><span data-stu-id="c065e-116">About Client Configuration Settings</span></span>](about-client-configuration-settings.md)

## <span data-ttu-id="c065e-117">Настройка клиента с помощью шаблона ADMX и групповой политики</span><span class="sxs-lookup"><span data-stu-id="c065e-117">Configure the client by using the ADMX template and Group Policy</span></span>


<span data-ttu-id="c065e-118">Вы можете использовать шаблон Microsoft ADMX для настройки клиентских параметров для клиента App-V 5,0 и клиента служб удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c065e-118">You can use the Microsoft ADMX template to configure the client settings for the App-V 5.0 client and the Remote Desktop Services client.</span></span> <span data-ttu-id="c065e-119">Шаблон ADMX управляет распространенными конфигурациями клиентов с помощью существующей инфраструктуры групповой политики, которая включает параметры конфигурации клиента App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c065e-119">The ADMX template manages common client configurations by using an existing Group Policy infrastructure and it includes settings for the App-V 5.0 client configuration.</span></span>

<span data-ttu-id="c065e-120">**Важно!**  Вы можете получить шаблон App-V 5,0 ADMX из центра загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c065e-120">**Important** You can obtain the App-V 5.0 ADMX template from the Microsoft Download Center.</span></span>

 

<span data-ttu-id="c065e-121">После скачивания и установки шаблона ADMX выполните указанные ниже действия на компьютере, который будет использоваться для управления групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="c065e-121">After you download and install the ADMX template, perform the following steps on the computer that you will use to manage Group Policy.</span></span> <span data-ttu-id="c065e-122">Обычно это контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="c065e-122">This is typically the Domain Controller.</span></span>

1.  <span data-ttu-id="c065e-123">Сохраните **ADMX** файл в следующем каталоге: **Windows \ \ PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="c065e-123">Save the **.admx** file to the following directory: **Windows \\ PolicyDefinitions**</span></span>

2.  <span data-ttu-id="c065e-124">Сохраните файл **ADML** в следующей папке: **каталог Windows \ \ PolicyDefinitions \ \ &lt; Справочник &gt; по языку**</span><span class="sxs-lookup"><span data-stu-id="c065e-124">Save the **.adml** file to the following directory: **Windows \\ PolicyDefinitions \\ &lt;Language Directory&gt;**</span></span>

<span data-ttu-id="c065e-125">После выполнения описанных выше действий вы можете управлять параметрами конфигурации клиента App-V 5,0 с помощью консоли **управления групповыми политиками** .</span><span class="sxs-lookup"><span data-stu-id="c065e-125">After you have completed the preceding steps, you can manage the App-V 5.0 client configuration settings with the **Group Policy Management** console.</span></span>

<span data-ttu-id="c065e-126">Клиент App-V 5,0 также хранит конфигурацию в реестре.</span><span class="sxs-lookup"><span data-stu-id="c065e-126">The App-V 5.0 client also stores its configuration in the registry.</span></span> <span data-ttu-id="c065e-127">Вы можете собрать полезные сведения о клиенте, если вы понимаете формат данных в реестре.</span><span class="sxs-lookup"><span data-stu-id="c065e-127">You can gather some useful information about the client if you understand the format of the data in the registry.</span></span> <span data-ttu-id="c065e-128">Вы также можете настроить множество клиентских действий, изменяя записи в реестре.</span><span class="sxs-lookup"><span data-stu-id="c065e-128">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="c065e-129">Изменение конфигурации клиента App-V 5.0 с помощью шаблона ADMX и групповой политики</span><span class="sxs-lookup"><span data-stu-id="c065e-129">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

## <span data-ttu-id="c065e-130">Развертывание клиента с помощью режима хранилища общего содержимого</span><span class="sxs-lookup"><span data-stu-id="c065e-130">Deploy the client by using the Shared Content Store mode</span></span>


<span data-ttu-id="c065e-131">Режим хранилища общего содержимого (SCS) App-V 5,0 позволяет клиентам SCS App-V 5,0 запускать виртуализированные приложения, не сохраняя никакие связанные данные пакета локально.</span><span class="sxs-lookup"><span data-stu-id="c065e-131">The App-V 5.0 Shared Content Store (SCS) mode enables the SCS App-V 5.0 clients to run virtualized applications without saving any of the associated package data locally.</span></span> <span data-ttu-id="c065e-132">Все необходимые виртуализированные данные пакета передаются по сети; Поэтому режим SCS следует использовать только в средах с быстрым подключением.</span><span class="sxs-lookup"><span data-stu-id="c065e-132">All required virtualized package data is transmitted across the network; therefore, you should only use the SCS mode in environments with a fast connection.</span></span> <span data-ttu-id="c065e-133">Службы удаленных рабочих столов (RDS) и стандартная версия клиента App-V 5,0 поддерживаются в режиме SCS.</span><span class="sxs-lookup"><span data-stu-id="c065e-133">Both the Remote Desktop Services (RDS) and the standard version of the App-V 5.0 client are supported with SCS mode.</span></span>

<span data-ttu-id="c065e-134">**Важно!**  Если клиент App-V 5,0 настроен для работы в режиме SCS, то расположение, в котором передаются пакеты приложения App-V 5,0, должно быть доступно, в противном случае виртуализированный пакет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="c065e-134">**Important** If the App-V 5.0 client is configured to run in the SCS mode, the location where the App-V 5.0 packages are streamed from must be available, otherwise, the virtualized package will fail.</span></span> <span data-ttu-id="c065e-135">Кроме того, мы не рекомендуем развертывать виртуализированные приложения на компьютерах, на которых запущен клиент App-V 5,0 в режиме SCS через Интернет.</span><span class="sxs-lookup"><span data-stu-id="c065e-135">Additionally, we do not recommend deployment of virtualized applications to computers that run the App-V 5.0 client in the SCS mode across the internet.</span></span>

 

<span data-ttu-id="c065e-136">Кроме того, SCS не является физическим расположением, которое содержит виртуализированные пакеты.</span><span class="sxs-lookup"><span data-stu-id="c065e-136">Additionally, the SCS is not a physical location that contains virtualized packages.</span></span> <span data-ttu-id="c065e-137">Это режим, позволяющий клиенту App-V 5,0 передавать необходимые виртуализованные данные пакета по сети.</span><span class="sxs-lookup"><span data-stu-id="c065e-137">It is a mode that allows the App-V 5.0 client to stream the required virtualized package data across the network.</span></span>

<span data-ttu-id="c065e-138">Режим SCS полезен в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="c065e-138">The SCS mode is helpful in the following scenarios:</span></span>

-   <span data-ttu-id="c065e-139">Развертывание инфраструктуры виртуальных рабочих столов (VDI)</span><span class="sxs-lookup"><span data-stu-id="c065e-139">Virtual desktop infrastructure (VDI) deployments</span></span>

-   <span data-ttu-id="c065e-140">Развертывания служб удаленных рабочих столов (RDS)</span><span class="sxs-lookup"><span data-stu-id="c065e-140">Remote desktop services (RDS) deployments</span></span>

<span data-ttu-id="c065e-141">Чтобы использовать SCS в своей среде, необходимо включить клиент App-V 5,0 в режиме SCS.</span><span class="sxs-lookup"><span data-stu-id="c065e-141">To use SCS in your environment, you must enable the App-V 5.0 client to run in SCS mode.</span></span> <span data-ttu-id="c065e-142">Этот параметр должен быть указан во время установки.</span><span class="sxs-lookup"><span data-stu-id="c065e-142">This setting should be specified during installation.</span></span> <span data-ttu-id="c065e-143">По умолчанию клиент не настроен на использование режима SCS.</span><span class="sxs-lookup"><span data-stu-id="c065e-143">By default, the client is not configured to use SCS mode.</span></span> <span data-ttu-id="c065e-144">Если вы планируете использовать SCS, вы должны установить клиент с помощью предлагаемой процедуры.</span><span class="sxs-lookup"><span data-stu-id="c065e-144">You should install the client by using the suggested procedure if you plan to use SCS.</span></span> <span data-ttu-id="c065e-145">Однако вы можете настроить существующий клиент App-V 5,0 для работы в режиме SCS, введя следующую команду PowerShell на компьютере, на котором запущен клиент App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="c065e-145">However, you can configure an existing App-V 5.0 client to run in SCS mode by entering the following PowerShell command on the computer that runs the App-V 5.0 client:</span></span>

**<span data-ttu-id="c065e-146">Set-AppvClientConfiguration-SharedContentStoreMode 1</span><span class="sxs-lookup"><span data-stu-id="c065e-146">set-AppvClientConfiguration -SharedContentStoreMode 1</span></span>**

<span data-ttu-id="c065e-147">Могут возникнуть ситуации, когда администратор выполняет предварительную загрузку некоторых виртуальных приложений на компьютере, на котором запущен клиент App-V 5,0 в режиме SCS.</span><span class="sxs-lookup"><span data-stu-id="c065e-147">There might be cases when the administrator pre-loads some virtual applications on the computer that runs the App-V 5.0 client in SCS mode.</span></span> <span data-ttu-id="c065e-148">Это можно сделать с помощью команд PowerShell, чтобы добавить, опубликовать и подключить пакет.</span><span class="sxs-lookup"><span data-stu-id="c065e-148">This can be accomplished with PowerShell commands to add, publish, and mount the package.</span></span> <span data-ttu-id="c065e-149">Например, если пакет предварительно загружен на все компьютеры, администратор может добавить, опубликовать и подключить пакет с помощью команд PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c065e-149">For example, if a package is pre-loaded on all computers, the administrator could add, publish, and mount the package by using PowerShell commands.</span></span> <span data-ttu-id="c065e-150">Пакет не помещается в поток по сети, так как он будет храниться локально.</span><span class="sxs-lookup"><span data-stu-id="c065e-150">The package would not stream across the network because it would be locally stored.</span></span>

[<span data-ttu-id="c065e-151">Установка клиента App-V 5.0 для режима хранилища общего содержимого</span><span class="sxs-lookup"><span data-stu-id="c065e-151">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)

## <span data-ttu-id="c065e-152">Развертывание секвенсора</span><span class="sxs-lookup"><span data-stu-id="c065e-152">Deploy the Sequencer</span></span>


<span data-ttu-id="c065e-153">Секвенсор — это инструмент, который используется для преобразования стандартных приложений в виртуальные пакеты для развертывания на компьютеры, на которых запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c065e-153">The Sequencer is a tool that is used to convert standard applications into virtual packages for deployment to computers that run the App-V 5.0 client.</span></span> <span data-ttu-id="c065e-154">Секвенсор помогает обеспечить простой и предсказуемый процесс преобразования с минимальными изменениями в предыдущих рабочих процессах последовательности.</span><span class="sxs-lookup"><span data-stu-id="c065e-154">The Sequencer helps provide a simple and predictable conversion process with minimal changes to prior sequencing workflows.</span></span> <span data-ttu-id="c065e-155">Кроме того, секвенсор позволяет пользователям более легко настраивать приложения, чтобы обеспечить подключение виртуализованных приложений.</span><span class="sxs-lookup"><span data-stu-id="c065e-155">In addition, the Sequencer allows users to more easily configure applications to enable connections of virtualized applications.</span></span>

<span data-ttu-id="c065e-156">Список изменений в секвенсоре App-V 5,0 можно найти в разделе новые возможности [App-v 5,0](whats-new-in-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="c065e-156">For a list of changes in the App-V 5.0 Sequencer, see [What's New in App-V 5.0](whats-new-in-app-v-50.md).</span></span>

[<span data-ttu-id="c065e-157">Установка программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="c065e-157">How to Install the Sequencer</span></span>](how-to-install-the-sequencer-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-client-and-sequencer-logs"></a> <span data-ttu-id="c065e-158">Журналы клиентского и секвенсора App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c065e-158">App-V 5.0 Client and Sequencer logs</span></span>


<span data-ttu-id="c065e-159">Данные журнала секвенсора App-V 5,0 можно использовать для устранения неполадок, связанных с установкой и функционированием секвенсора, при использовании App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c065e-159">You can use the App-V 5.0 Sequencer log information to help troubleshoot the Sequencer installation and operational events while using App-V 5.0.</span></span> <span data-ttu-id="c065e-160">Данные журнала, связанные с секвенсором, можно просмотреть в **средстве просмотра событий**.</span><span class="sxs-lookup"><span data-stu-id="c065e-160">The Sequencer-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="c065e-161">В следующей строке показан определенный путь для событий, связанных с секвенсором:</span><span class="sxs-lookup"><span data-stu-id="c065e-161">The following line displays the specific path for Sequencer-related events:</span></span>

<span data-ttu-id="c065e-162">**Окно просмотра событий \ \ журналы приложений и служб \ \ Microsoft \ \ приложение V**. События, связанные с секвенсором, добавляются в начале с помощью службы **AppV \ _Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="c065e-162">**Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V**. Sequencer-related events are prepended with **AppV\_Sequencer**.</span></span> <span data-ttu-id="c065e-163">События, связанные с клиентами, добавляются в начале с помощью службы **AppV \ _Client**.</span><span class="sxs-lookup"><span data-stu-id="c065e-163">Client-related events are prepended with **AppV\_Client**.</span></span>

<span data-ttu-id="c065e-164">В приложении App-V 5,0 с пакетом обновления 3 (SP3) некоторые журналы были объединены.</span><span class="sxs-lookup"><span data-stu-id="c065e-164">In App-V 5.0 SP3, some logs have been consolidated.</span></span> <span data-ttu-id="c065e-165">Дополнительные [сведения о приложении App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="c065e-165">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <span data-ttu-id="c065e-166">Другие ресурсы для развертывания секвенсора и клиента</span><span class="sxs-lookup"><span data-stu-id="c065e-166">Other resources for deploying the Sequencer and client</span></span>


[<span data-ttu-id="c065e-167">Развертывание App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c065e-167">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="c065e-168">Планирование использования App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c065e-168">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)






 

 





