---
title: Развертывание Sequencer и клиента App-V 5.1
description: Развертывание Sequencer и клиента App-V 5.1
author: dansimp
ms.assetid: 74f32794-4c76-436f-a542-f9e95d89063d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3b78059e5005f563bb99d7e6f4b5fe0af2eae8d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814568"
---
# <span data-ttu-id="0cfc0-103">Развертывание Sequencer и клиента App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="0cfc0-103">Deploying the App-V 5.1 Sequencer and Client</span></span>


<span data-ttu-id="0cfc0-104">Microsoft Application Virtualization (App-V) 5,1 Sequencer и клиент позволяет администраторам виртуализировать и запускать виртуализированные приложения.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-104">The Microsoft Application Virtualization (App-V) 5.1 Sequencer and client enable administrators to virtualize and run virtualized applications.</span></span>

## <span data-ttu-id="0cfc0-105">Развертывание клиента</span><span class="sxs-lookup"><span data-stu-id="0cfc0-105">Deploy the client</span></span>


<span data-ttu-id="0cfc0-106">Клиент App-V 5,1 является компонентом, который запускает виртуализированное приложение на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-106">The App-V 5.1 client is the component that runs a virtualized application on a target computer.</span></span> <span data-ttu-id="0cfc0-107">Клиент позволяет пользователям взаимодействовать со значками и дважды щелкать типы файлов, чтобы они могли запускать виртуализированное приложение.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-107">The client enables users to interact with icons and to double-click file types, so that they can start a virtualized application.</span></span> <span data-ttu-id="0cfc0-108">Клиент также может получить содержимое виртуального приложения с сервера управления.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-108">The client can also obtain the virtual application content from the management server.</span></span>

[<span data-ttu-id="0cfc0-109">Развертывание клиента App-V</span><span class="sxs-lookup"><span data-stu-id="0cfc0-109">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-51gb18030.md)

[<span data-ttu-id="0cfc0-110">Удаление клиента App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="0cfc0-110">How to Uninstall the App-V 5.1 Client</span></span>](how-to-uninstall-the-app-v-51-client.md)

[<span data-ttu-id="0cfc0-111">Развертывание приложения App-V 4,6 и клиента App-V 5,1 на том же компьютере</span><span class="sxs-lookup"><span data-stu-id="0cfc0-111">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

## <span data-ttu-id="0cfc0-112">Параметры конфигурации клиента</span><span class="sxs-lookup"><span data-stu-id="0cfc0-112">Client Configuration Settings</span></span>


<span data-ttu-id="0cfc0-113">Клиент App-V 5,1 хранит свою конфигурацию в реестре.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-113">The App-V 5.1 client stores its configuration in the registry.</span></span> <span data-ttu-id="0cfc0-114">Вы можете собрать полезные сведения о клиенте, если вы понимаете формат данных в реестре.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-114">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="0cfc0-115">Вы также можете настроить множество клиентских действий, изменяя записи в реестре.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-115">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="0cfc0-116">Сведения о параметрах конфигурации клиента</span><span class="sxs-lookup"><span data-stu-id="0cfc0-116">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

## <span data-ttu-id="0cfc0-117">Настройка клиента с помощью шаблона ADMX и групповой политики</span><span class="sxs-lookup"><span data-stu-id="0cfc0-117">Configure the client by using the ADMX template and Group Policy</span></span>


<span data-ttu-id="0cfc0-118">Вы можете использовать шаблон Microsoft ADMX для настройки клиентских параметров для клиента App-V 5,1 и клиента служб удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-118">You can use the Microsoft ADMX template to configure the client settings for the App-V 5.1 client and the Remote Desktop Services client.</span></span> <span data-ttu-id="0cfc0-119">Шаблон ADMX управляет распространенными конфигурациями клиентов с помощью существующей инфраструктуры групповой политики, которая включает параметры конфигурации клиента App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-119">The ADMX template manages common client configurations by using an existing Group Policy infrastructure and it includes settings for the App-V 5.1 client configuration.</span></span>

<span data-ttu-id="0cfc0-120">**Важно!**  Вы можете получить шаблон App-V 5,1 ADMX из центра загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-120">**Important** You can obtain the App-V 5.1 ADMX template from the Microsoft Download Center.</span></span>

 

<span data-ttu-id="0cfc0-121">После скачивания и установки шаблона ADMX выполните указанные ниже действия на компьютере, который будет использоваться для управления групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-121">After you download and install the ADMX template, perform the following steps on the computer that you will use to manage Group Policy.</span></span> <span data-ttu-id="0cfc0-122">Обычно это контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-122">This is typically the Domain Controller.</span></span>

1.  <span data-ttu-id="0cfc0-123">Сохраните **ADMX** файл в следующем каталоге: **Windows \ \ PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="0cfc0-123">Save the **.admx** file to the following directory: **Windows \\ PolicyDefinitions**</span></span>

2.  <span data-ttu-id="0cfc0-124">Сохраните файл **ADML** в следующей папке: **каталог Windows \ \ PolicyDefinitions \ \ &lt; Справочник &gt; по языку**</span><span class="sxs-lookup"><span data-stu-id="0cfc0-124">Save the **.adml** file to the following directory: **Windows \\ PolicyDefinitions \\ &lt;Language Directory&gt;**</span></span>

<span data-ttu-id="0cfc0-125">После выполнения описанных выше действий вы можете управлять параметрами конфигурации клиента App-V 5,1 с помощью консоли **управления групповыми политиками** .</span><span class="sxs-lookup"><span data-stu-id="0cfc0-125">After you have completed the preceding steps, you can manage the App-V 5.1 client configuration settings with the **Group Policy Management** console.</span></span>

<span data-ttu-id="0cfc0-126">Клиент App-V 5,1 также хранит конфигурацию в реестре.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-126">The App-V 5.1 client also stores its configuration in the registry.</span></span> <span data-ttu-id="0cfc0-127">Вы можете собрать полезные сведения о клиенте, если вы понимаете формат данных в реестре.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-127">You can gather some useful information about the client if you understand the format of the data in the registry.</span></span> <span data-ttu-id="0cfc0-128">Вы также можете настроить множество клиентских действий, изменяя записи в реестре.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-128">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="0cfc0-129">Изменение конфигурации клиента App-V 5.1 с помощью шаблона ADMX и групповой политики</span><span class="sxs-lookup"><span data-stu-id="0cfc0-129">How to Modify App-V 5.1 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

## <span data-ttu-id="0cfc0-130">Развертывание клиента с помощью режима хранилища общего содержимого</span><span class="sxs-lookup"><span data-stu-id="0cfc0-130">Deploy the client by using the Shared Content Store mode</span></span>


<span data-ttu-id="0cfc0-131">Режим хранилища общего содержимого (SCS) App-V 5,1 позволяет клиентам SCS App-V 5,1 запускать виртуализированные приложения, не сохраняя никакие связанные данные пакета локально.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-131">The App-V 5.1 Shared Content Store (SCS) mode enables the SCS App-V 5.1 clients to run virtualized applications without saving any of the associated package data locally.</span></span> <span data-ttu-id="0cfc0-132">Все необходимые виртуализированные данные пакета передаются по сети; Поэтому режим SCS следует использовать только в средах с быстрым подключением.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-132">All required virtualized package data is transmitted across the network; therefore, you should only use the SCS mode in environments with a fast connection.</span></span> <span data-ttu-id="0cfc0-133">Службы удаленных рабочих столов (RDS) и стандартная версия клиента App-V 5,1 поддерживаются в режиме SCS.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-133">Both the Remote Desktop Services (RDS) and the standard version of the App-V 5.1 client are supported with SCS mode.</span></span>

<span data-ttu-id="0cfc0-134">**Важно!**  Если клиент App-V 5,1 настроен для работы в режиме SCS, то расположение, в котором передаются пакеты приложения App-V 5,1, должно быть доступно, в противном случае виртуализированный пакет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-134">**Important** If the App-V 5.1 client is configured to run in the SCS mode, the location where the App-V 5.1 packages are streamed from must be available, otherwise, the virtualized package will fail.</span></span> <span data-ttu-id="0cfc0-135">Кроме того, мы не рекомендуем развертывать виртуализированные приложения на компьютерах, на которых запущен клиент App-V 5,1 в режиме SCS через Интернет.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-135">Additionally, we do not recommend deployment of virtualized applications to computers that run the App-V 5.1 client in the SCS mode across the internet.</span></span>

 

<span data-ttu-id="0cfc0-136">Кроме того, SCS не является физическим расположением, которое содержит виртуализированные пакеты.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-136">Additionally, the SCS is not a physical location that contains virtualized packages.</span></span> <span data-ttu-id="0cfc0-137">Это режим, позволяющий клиенту App-V 5,1 передавать необходимые виртуализованные данные пакета по сети.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-137">It is a mode that allows the App-V 5.1 client to stream the required virtualized package data across the network.</span></span>

<span data-ttu-id="0cfc0-138">Режим SCS полезен в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="0cfc0-138">The SCS mode is helpful in the following scenarios:</span></span>

-   <span data-ttu-id="0cfc0-139">Развертывание инфраструктуры виртуальных рабочих столов (VDI)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-139">Virtual desktop infrastructure (VDI) deployments</span></span>

-   <span data-ttu-id="0cfc0-140">Развертывания служб удаленных рабочих столов (RDS)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-140">Remote desktop services (RDS) deployments</span></span>

<span data-ttu-id="0cfc0-141">Чтобы использовать SCS в своей среде, необходимо включить клиент App-V 5,1 в режиме SCS.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-141">To use SCS in your environment, you must enable the App-V 5.1 client to run in SCS mode.</span></span> <span data-ttu-id="0cfc0-142">Этот параметр должен быть указан во время установки.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-142">This setting should be specified during installation.</span></span> <span data-ttu-id="0cfc0-143">По умолчанию клиент не настроен на использование режима SCS.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-143">By default, the client is not configured to use SCS mode.</span></span> <span data-ttu-id="0cfc0-144">Если вы планируете использовать SCS, вы должны установить клиент с помощью предлагаемой процедуры.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-144">You should install the client by using the suggested procedure if you plan to use SCS.</span></span> <span data-ttu-id="0cfc0-145">Однако вы можете настроить существующий клиент App-V 5,1 для работы в режиме SCS, введя следующую команду PowerShell на компьютере, на котором запущен клиент App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="0cfc0-145">However, you can configure an existing App-V 5.1 client to run in SCS mode by entering the following PowerShell command on the computer that runs the App-V 5.1 client:</span></span>

**<span data-ttu-id="0cfc0-146">Set-AppvClientConfiguration-SharedContentStoreMode 1</span><span class="sxs-lookup"><span data-stu-id="0cfc0-146">set-AppvClientConfiguration -SharedContentStoreMode 1</span></span>**

<span data-ttu-id="0cfc0-147">Могут возникнуть ситуации, когда администратор выполняет предварительную загрузку некоторых виртуальных приложений на компьютере, на котором запущен клиент App-V 5,1 в режиме SCS.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-147">There might be cases when the administrator pre-loads some virtual applications on the computer that runs the App-V 5.1 client in SCS mode.</span></span> <span data-ttu-id="0cfc0-148">Это можно сделать с помощью команд PowerShell, чтобы добавить, опубликовать и подключить пакет.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-148">This can be accomplished with PowerShell commands to add, publish, and mount the package.</span></span> <span data-ttu-id="0cfc0-149">Например, если пакет предварительно загружен на все компьютеры, администратор может добавить, опубликовать и подключить пакет с помощью команд PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-149">For example, if a package is pre-loaded on all computers, the administrator could add, publish, and mount the package by using PowerShell commands.</span></span> <span data-ttu-id="0cfc0-150">Пакет не помещается в поток по сети, так как он будет храниться локально.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-150">The package would not stream across the network because it would be locally stored.</span></span>

[<span data-ttu-id="0cfc0-151">Установка клиента App-V 5.1 для режима хранилища общего содержимого</span><span class="sxs-lookup"><span data-stu-id="0cfc0-151">How to Install the App-V 5.1 Client for Shared Content Store Mode</span></span>](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)

## <span data-ttu-id="0cfc0-152">Развертывание секвенсора</span><span class="sxs-lookup"><span data-stu-id="0cfc0-152">Deploy the Sequencer</span></span>


<span data-ttu-id="0cfc0-153">Секвенсор — это инструмент, который используется для преобразования стандартных приложений в виртуальные пакеты для развертывания на компьютеры, на которых запущен клиент App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-153">The Sequencer is a tool that is used to convert standard applications into virtual packages for deployment to computers that run the App-V 5.1 client.</span></span> <span data-ttu-id="0cfc0-154">Секвенсор помогает обеспечить простой и предсказуемый процесс преобразования с минимальными изменениями в предыдущих рабочих процессах последовательности.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-154">The Sequencer helps provide a simple and predictable conversion process with minimal changes to prior sequencing workflows.</span></span> <span data-ttu-id="0cfc0-155">Кроме того, секвенсор позволяет пользователям более легко настраивать приложения, чтобы обеспечить подключение виртуализованных приложений.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-155">In addition, the Sequencer allows users to more easily configure applications to enable connections of virtualized applications.</span></span>

<span data-ttu-id="0cfc0-156">Список изменений в секвенсоре App-V 5,1 можно найти в разделе [о приложении App-v 5,1](about-app-v-51.md).</span><span class="sxs-lookup"><span data-stu-id="0cfc0-156">For a list of changes in the App-V 5.1 Sequencer, see [About App-V 5.1](about-app-v-51.md).</span></span>

[<span data-ttu-id="0cfc0-157">Установка программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="0cfc0-157">How to Install the Sequencer</span></span>](how-to-install-the-sequencer-51beta-gb18030.md)

## <a href="" id="---------app-v-5-1-client-and-sequencer-logs"></a> <span data-ttu-id="0cfc0-158">Журналы клиентского и секвенсора App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="0cfc0-158">App-V 5.1 Client and Sequencer logs</span></span>


<span data-ttu-id="0cfc0-159">Данные журнала секвенсора App-V 5,1 можно использовать для устранения неполадок, связанных с установкой и функционированием секвенсора, при использовании App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-159">You can use the App-V 5.1 Sequencer log information to help troubleshoot the Sequencer installation and operational events while using App-V 5.1.</span></span> <span data-ttu-id="0cfc0-160">Данные журнала, связанные с секвенсором, можно просмотреть в **средстве просмотра событий**.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-160">The Sequencer-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="0cfc0-161">В следующей строке показан определенный путь для событий, связанных с секвенсором:</span><span class="sxs-lookup"><span data-stu-id="0cfc0-161">The following line displays the specific path for Sequencer-related events:</span></span>

<span data-ttu-id="0cfc0-162">**Окно просмотра событий \ \ журналы приложений и служб \ \ Microsoft \ \ приложение V**. События, связанные с секвенсором, добавляются в начале с помощью службы **AppV \ _Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-162">**Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V**. Sequencer-related events are prepended with **AppV\_Sequencer**.</span></span> <span data-ttu-id="0cfc0-163">События, связанные с клиентами, добавляются в начале с помощью службы **AppV \ _Client**.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-163">Client-related events are prepended with **AppV\_Client**.</span></span>

## <span data-ttu-id="0cfc0-164">Другие ресурсы для развертывания секвенсора и клиента</span><span class="sxs-lookup"><span data-stu-id="0cfc0-164">Other resources for deploying the Sequencer and client</span></span>


[<span data-ttu-id="0cfc0-165">Развертывание App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="0cfc0-165">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="0cfc0-166">Планирование использования App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="0cfc0-166">Planning for App-V 5.1</span></span>](planning-for-app-v-51.md)






 

 





