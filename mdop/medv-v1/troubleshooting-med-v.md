---
title: Устранение неполадок MED-V
description: Устранение неполадок MED-V
author: dansimp
ms.assetid: f43dae36-6485-4e06-9c66-0a646e27079d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38d13be699a92368ff258026acd8e0d5f0e28cd6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825862"
---
# <span data-ttu-id="57a8b-103">Устранение неполадок MED-V</span><span class="sxs-lookup"><span data-stu-id="57a8b-103">Troubleshooting MED-V</span></span>


<span data-ttu-id="57a8b-104">В этом разделе приведены сведения, которые помогут вам устранить общие проблемы с виртуализацией классической версии Microsoft Enterprise (MED-V).</span><span class="sxs-lookup"><span data-stu-id="57a8b-104">This section provides information to help troubleshoot general issues with Microsoft Enterprise Desktop Virtualization (MED-V).</span></span>

## <span data-ttu-id="57a8b-105">Изменение разрешения узла и максимизация рабочей области MED-V приводит к тому, что настольный компьютер будет выглядеть черным</span><span class="sxs-lookup"><span data-stu-id="57a8b-105">Changing the host resolution and then maximizing the MED-V workspace causes the desktop to appear black</span></span>


<span data-ttu-id="57a8b-106">При работе в режиме полного рабочего стола, если изменить разрешение узла и затем развернуть окно рабочей области для MED-V, Рабочий стол будет черным, а рабочее пространство MED-v может не ответить.</span><span class="sxs-lookup"><span data-stu-id="57a8b-106">When working in full desktop mode, if you change the host resolution and then maximize the MED-V workspace window, the desktop appears black and the MED-V workspace might not respond.</span></span>

### <span data-ttu-id="57a8b-107">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-107">Solution</span></span>

<span data-ttu-id="57a8b-108">Остановите и запустите рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="57a8b-108">Stop and then start the MED-V workspace.</span></span>

## <span data-ttu-id="57a8b-109">Запуск рабочей области MED-V с отключенным сетевым адаптером и последующее включение адаптера не восстанавливает сетевое подключение</span><span class="sxs-lookup"><span data-stu-id="57a8b-109">Starting a MED-V workspace with a network adapter disabled and then later enabling the adapter does not restore network connectivity</span></span>


<span data-ttu-id="57a8b-110">Если вы настроили рабочую область MED-V в режиме моста и затем запускаете рабочую область MED-V, когда сетевой адаптер отключен, подключение к сети с помощью этого адаптера будет восстановлено.</span><span class="sxs-lookup"><span data-stu-id="57a8b-110">If you configure a MED-V workspace in bridge mode and then start the MED-V workspace while a network adapter is disabled, if the adapter is later enabled, the network connectivity through that adapter is not restored.</span></span>

### <span data-ttu-id="57a8b-111">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-111">Solution</span></span>

<span data-ttu-id="57a8b-112">Остановите и запустите рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="57a8b-112">Stop and then start the MED-V workspace.</span></span>

## <span data-ttu-id="57a8b-113">Изображение может использоваться только одним пользователем Windows на компьютере.</span><span class="sxs-lookup"><span data-stu-id="57a8b-113">An image can be used by only one Windows user per computer</span></span>


<span data-ttu-id="57a8b-114">Образ рабочей области MED-V может использоваться только тем пользователем Windows, который загрузил или импортировал изображение.</span><span class="sxs-lookup"><span data-stu-id="57a8b-114">A MED-V workspace image can be used only by the Windows user who downloaded or imported the image.</span></span> <span data-ttu-id="57a8b-115">Этот пользователь не является администратором, имеющим разрешения на доступ к папке, в которой находятся Скачанные изображения.</span><span class="sxs-lookup"><span data-stu-id="57a8b-115">This user is the only user aside from administrators who have permissions to the folder where the downloaded images are located.</span></span>

### <span data-ttu-id="57a8b-116">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-116">Solution</span></span>

<span data-ttu-id="57a8b-117">Вручную измените список управления доступом (ACL) в хранилище изображений.</span><span class="sxs-lookup"><span data-stu-id="57a8b-117">Manually change the access control list (ACL) on the image store.</span></span>

## <span data-ttu-id="57a8b-118">При установке MED-V с помощью Configuration Manager с включенными правами пользователей не удается выполнить удаление</span><span class="sxs-lookup"><span data-stu-id="57a8b-118">When installing MED-V by using Configuration Manager with users rights enabled, uninstall fails</span></span>


<span data-ttu-id="57a8b-119">Если для установки MED-V используется Microsoft System Center Configuration Manager и режим выполнения пакета установлен в значение права пользователей, при удалении из него появляется сообщение об ошибке, в котором говорится, что только административные пользователи могут удалить MED-V.</span><span class="sxs-lookup"><span data-stu-id="57a8b-119">If MED-V is installed by using Microsoft System Center Configuration Manager and the run mode of the package is set to users rights, uninstall fails with an error message that says that only administrative users can uninstall MED-V.</span></span>

### <span data-ttu-id="57a8b-120">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-120">Solution</span></span>

<span data-ttu-id="57a8b-121">При создании пакета Configuration Manager для MED-V настройте режим выполнения для прав администратора.</span><span class="sxs-lookup"><span data-stu-id="57a8b-121">When creating a Configuration Manager package for MED-V, set the run mode to administrative rights.</span></span>

## <span data-ttu-id="57a8b-122">При установке MED-V с помощью корпоративной системы развертывания, где установка настроена для запуска клиента после установки, вы не сможете запустить клиент</span><span class="sxs-lookup"><span data-stu-id="57a8b-122">When installing MED-V by using a corporate deployment system, where the installation is configured to run the client following installation, you cannot run the client</span></span>


<span data-ttu-id="57a8b-123">Если для установки MED-V используется корпоративная система развертывания, а установочный пакет настроен на запуск клиента MED-V после установки, то после его запуска с помощью системной учетной записи вы не увидите, что клиент запущен (за исключением области уведомлений), и вы не можете взаимодействовать с ним.</span><span class="sxs-lookup"><span data-stu-id="57a8b-123">If MED-V is installed by using a corporate deployment system and the installation package is configured to run MED-V client following the installation, after the client is running under the system account, you cannot see that the client is running (except in the notification area), and you cannot interact with it.</span></span>

### <span data-ttu-id="57a8b-124">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-124">Solution</span></span>

<span data-ttu-id="57a8b-125">При установке MED-V с помощью корпоративной системы развертывания используйте параметр *Start \ _MEDV = 0* . msi.</span><span class="sxs-lookup"><span data-stu-id="57a8b-125">When installing MED-V by using a corporate deployment system, use the *START\_MEDV=0* .msi parameter.</span></span>

## <span data-ttu-id="57a8b-126">Не запускается тестовый образ для MED-V</span><span class="sxs-lookup"><span data-stu-id="57a8b-126">MED-V test image fails to start</span></span>


<span data-ttu-id="57a8b-127">Если изображение теста MED-V не запускается, оно не будет восстановлено, а все последующие запуска будут завершаться сбоем с сообщением об ошибке "GINA не удалось загрузить".</span><span class="sxs-lookup"><span data-stu-id="57a8b-127">If a MED-V test image fails to start, it will never recover and all future startups will fail with a “GINA fail to load” error message.</span></span>

### <span data-ttu-id="57a8b-128">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-128">Solution</span></span>

<span data-ttu-id="57a8b-129">Удалите существующее тестовое изображение и повторно создайте его.</span><span class="sxs-lookup"><span data-stu-id="57a8b-129">Delete the existing test image and then re-create it.</span></span>

## <span data-ttu-id="57a8b-130">При попытке присоединиться к домену с неверными учетными данными изображение не будет успешно присоединяться к домену.</span><span class="sxs-lookup"><span data-stu-id="57a8b-130">After attempting to join a domain with the wrong credentials, the image never succeeds in joining the domain</span></span>


<span data-ttu-id="57a8b-131">Если при попытке присоединиться к домену в стандартном блоке "присоединиться к домену" произошла ошибка конфигурации, которая является частью сценария настройки при первом запуске виртуальной машины, это приводит к сбою рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="57a8b-131">If there is a configuration error in the join domain building block, which is part of the virtual machine first-time setup script, it causes the MED-V workspace to fail when attempting to join a domain.</span></span> <span data-ttu-id="57a8b-132">После восстановления ошибки конфигурации образ, включенный в рабочую область MED-V, не может присоединиться к домену.</span><span class="sxs-lookup"><span data-stu-id="57a8b-132">After the configuration error is repaired, the image included in the MED-V workspace cannot join the domain.</span></span>

### <span data-ttu-id="57a8b-133">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-133">Solution</span></span>

<span data-ttu-id="57a8b-134">Если вы развернули изображение, перераспределите его.</span><span class="sxs-lookup"><span data-stu-id="57a8b-134">If the image was deployed, redistribute the image.</span></span> <span data-ttu-id="57a8b-135">Если изображением является тестовое изображение, повторно создайте изображение.</span><span class="sxs-lookup"><span data-stu-id="57a8b-135">If the image was a test image, re-create the image.</span></span>

## <span data-ttu-id="57a8b-136">MED-V не поддерживает несколько мониторов</span><span class="sxs-lookup"><span data-stu-id="57a8b-136">MED-V does not support multiple monitors</span></span>


<span data-ttu-id="57a8b-137">MED-V не поддерживает отображение опубликованных приложений на нескольких мониторах.</span><span class="sxs-lookup"><span data-stu-id="57a8b-137">MED-V does not support displaying published applications across multiple monitors.</span></span> <span data-ttu-id="57a8b-138">Опубликованные приложения и другие клиентские окна могут отображаться на неправильном экране, а иногда после отключения экрана приложение MED-V пытается отправить экран на монитор, чтобы подключенный монитор отображался пустым.</span><span class="sxs-lookup"><span data-stu-id="57a8b-138">Published applications and other client windows may be displayed in the wrong screen, and sometimes after a screen is disconnected, MED-V attempts to send the screen to the monitor so that the connected monitor appears blank.</span></span>

### <span data-ttu-id="57a8b-139">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-139">Solution</span></span>

<span data-ttu-id="57a8b-140">Отключите дополнительный экран и перезапустите клиент.</span><span class="sxs-lookup"><span data-stu-id="57a8b-140">Disconnect the additional screen, and restart the client.</span></span>

## <span data-ttu-id="57a8b-141">Рабочая область MED-V может не запуститься, если при запуске MED-V происходит сбой узла.</span><span class="sxs-lookup"><span data-stu-id="57a8b-141">MED-V workspace might fail to start if the host crashes during MED-V workspace startup</span></span>


<span data-ttu-id="57a8b-142">Если при запуске рабочей области MED-V происходит сбой узла и появляется сообщение об ошибке "корневой элемент отсутствует", Рабочая область MED-V может добавлять данные в пустой файл конфигурации виртуальных машин (VMC), что приводит к сбою процесса запуска.</span><span class="sxs-lookup"><span data-stu-id="57a8b-142">If the host crashes during the MED-V workspace startup process and an error message appears that says “Root element is missing,” the MED-V workspace might add data to an empty virtual machine configuration (VMC) file, which will cause the startup process to fail.</span></span>

### <span data-ttu-id="57a8b-143">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-143">Solution</span></span>

<span data-ttu-id="57a8b-144">Замените пустой файл VMC файлом VMC из базового образа.</span><span class="sxs-lookup"><span data-stu-id="57a8b-144">Replace the empty VMC file with a VMC file from the base image.</span></span>

## <span data-ttu-id="57a8b-145">Клавиатура не отвечает в опубликованных окнах приложений</span><span class="sxs-lookup"><span data-stu-id="57a8b-145">The keyboard does not respond in published application windows</span></span>


<span data-ttu-id="57a8b-146">Если в рабочей области MED-V вы нажмете клавишу с логотипом Windows, то клавиатура больше не отвечает на опубликованные окна приложений.</span><span class="sxs-lookup"><span data-stu-id="57a8b-146">In a MED-V workspace, if you press the Windows logo key when a published application is in focus, the keyboard no longer responds in published application windows.</span></span>

### <span data-ttu-id="57a8b-147">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-147">Solution</span></span>

<span data-ttu-id="57a8b-148">Нажмите клавишу с логотипом Windows, пока приложение находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="57a8b-148">Press the Windows logo key while a published application is in focus.</span></span>

## <span data-ttu-id="57a8b-149">Доменная область MED-V не обновляет учетные данные домена.</span><span class="sxs-lookup"><span data-stu-id="57a8b-149">A domain MED-V workspace does not update domain credentials</span></span>


<span data-ttu-id="57a8b-150">При использовании постоянной рабочей области MED-V в среде домена при изменении пароля домена клиент MED-V не обновляет учетные данные домена рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="57a8b-150">When using a persistent MED-V workspace in a domain environment, if you change your domain password, the MED-V client does not update the MED-V workspace domain credentials.</span></span> <span data-ttu-id="57a8b-151">Когда опубликованное приложение пытается получить доступ к сетевому ресурсу, появится сообщение об ошибке с уведомлением о том, что срок действия ваших учетных данных истек.</span><span class="sxs-lookup"><span data-stu-id="57a8b-151">When a published application attempts to access a network resource, you will receive an error message notifying you that your credentials expired.</span></span>

### <span data-ttu-id="57a8b-152">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-152">Solution</span></span>

<span data-ttu-id="57a8b-153">Перезапустите операционную систему MED-V Workspace.</span><span class="sxs-lookup"><span data-stu-id="57a8b-153">Restart the MED-V workspace operating system.</span></span>

## <span data-ttu-id="57a8b-154">Развернутые окна опубликованных приложений закрывают панель задач Hosting</span><span class="sxs-lookup"><span data-stu-id="57a8b-154">Maximized published application windows cover the host taskbar</span></span>


<span data-ttu-id="57a8b-155">Если окно опубликованного приложения развернуто на весь экран, оно может закрываются на панели задач Host.</span><span class="sxs-lookup"><span data-stu-id="57a8b-155">If you maximize a published application window to full screen, it might cover the host taskbar.</span></span>

### <span data-ttu-id="57a8b-156">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-156">Solution</span></span>

<span data-ttu-id="57a8b-157">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="57a8b-157">Do one of the following:</span></span>

<span data-ttu-id="57a8b-158">Сверните окно опубликованного приложения, чтобы получить доступ к области уведомлений, и перезапустите рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="57a8b-158">Minimize the published application window to gain access to the notification area, and restart the MED-V workspace.</span></span>

<span data-ttu-id="57a8b-159">Сверните окно опубликованного приложения, а затем восстановите его в развернутом состоянии.</span><span class="sxs-lookup"><span data-stu-id="57a8b-159">Minimize the published application window, and then restore the window to its maximized state.</span></span>

## <span data-ttu-id="57a8b-160">Не работает Добавление пользователей или групп в диспетчере конфигурации MED-V Server</span><span class="sxs-lookup"><span data-stu-id="57a8b-160">Adding users or groups in the MED-V Server Configuration Manager does not work</span></span>


<span data-ttu-id="57a8b-161">При добавлении пользователей или групп в диалоговом окне **Выбор пользователей или** групп выбранные пользователи или группы не добавляются в список управления доступом в диспетчере конфигураций MED-V Server.</span><span class="sxs-lookup"><span data-stu-id="57a8b-161">When adding users or groups in the **Select Users or Groups** dialog box, the selected users or groups are not added to the access control list in the MED-V Server Configuration Manager.</span></span>

### <span data-ttu-id="57a8b-162">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-162">Solution</span></span>

<span data-ttu-id="57a8b-163">Добавьте пользователей и группы с помощью диалогового окна " **Введите имена пользователей или групп** ".</span><span class="sxs-lookup"><span data-stu-id="57a8b-163">Add users or groups using the **Enter User or Group names** dialog box.</span></span> <span data-ttu-id="57a8b-164">Подробные сведения о том, [как установить и настроить серверный компонент MED-V, приведены в этой](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions)странице.</span><span class="sxs-lookup"><span data-stu-id="57a8b-164">For detailed information, see [How to Install and Configure the MED-V Server Component](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).</span></span>

## <span data-ttu-id="57a8b-165">Приложение MED-V не работает на компьютерах с Windows Virtual PC для Windows 7</span><span class="sxs-lookup"><span data-stu-id="57a8b-165">MED-V does not work on computers with Windows Virtual PC for Windows 7 installed</span></span>


<span data-ttu-id="57a8b-166">Для работы MED-V требуется Windows Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="57a8b-166">MED-V requires Windows Virtual PC2007.</span></span> <span data-ttu-id="57a8b-167">Windows Virtual PC для Windows7 и Virtual PC2007 SP1 нельзя установить на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="57a8b-167">Windows Virtual PC for Windows7 and Virtual PC2007 SP1 cannot be installed on the same computer.</span></span>

### <span data-ttu-id="57a8b-168">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-168">Solution</span></span>

<span data-ttu-id="57a8b-169">Удалите Virtual PC для Windows7 перед установкой виртуальных PC2007 SP1 и MED-V.</span><span class="sxs-lookup"><span data-stu-id="57a8b-169">Uninstall Virtual PC for Windows7 before installing Virtual PC2007 SP1 and MED-V.</span></span>

## <a href="" id="med-v-does-not-support-virtual-pc-and-windows-xp-mode-images-"></a><span data-ttu-id="57a8b-170">MED-V не поддерживает виртуальные компьютеры и режимы режима WindowsXP</span><span class="sxs-lookup"><span data-stu-id="57a8b-170">MED-V does not support Virtual PC and WindowsXP Mode images</span></span>


<span data-ttu-id="57a8b-171">Приложение MED-V 1.0 SP1 не поддерживает образы, созданные Windows Virtual PC для Windows7.</span><span class="sxs-lookup"><span data-stu-id="57a8b-171">MED-V1.0 SP1 does not support images created by Windows Virtual PC for Windows7.</span></span> <span data-ttu-id="57a8b-172">При использовании Virtual PC для Windows7 Image происходит сбой клиента во время запуска.</span><span class="sxs-lookup"><span data-stu-id="57a8b-172">If a Virtual PC for Windows7 image is used, the client will fail during startup.</span></span>

### <span data-ttu-id="57a8b-173">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-173">Solution</span></span>

<span data-ttu-id="57a8b-174">Создавайте образы MED-V с помощью Virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="57a8b-174">Create MED-V images by using Virtual PC2007 SP1.</span></span>

## <span data-ttu-id="57a8b-175">Брандмауэр Windows блокирует виртуальную сетевую активность PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="57a8b-175">Windows firewall blocks Virtual PC2007 SP1 network activity</span></span>


<span data-ttu-id="57a8b-176">По умолчанию брандмауэр Windows блокирует активность виртуальных PC2007 пакета обновления 1 (SP1) и, когда виртуальный PC2007 SP1 инициируется на клиентском компьютере, есть сообщение брандмауэра, блокирующее последовательность запуска и весь доступ к сети.</span><span class="sxs-lookup"><span data-stu-id="57a8b-176">By default, Windows firewall blocks Virtual PC2007 SP1 network activity, and when Virtual PC2007 SP1 initiates on the client computer, there is a firewall message that blocks its startup sequence and all network access.</span></span>

### <span data-ttu-id="57a8b-177">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-177">Solution</span></span>

<span data-ttu-id="57a8b-178">Обновите исключение брандмауэра с помощью групповой политики, прежде чем MED-V используется конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="57a8b-178">Update the firewall exception by using Group Policy before MED-V is used by the end user.</span></span>

## <span data-ttu-id="57a8b-179">При обновлении клиента появляется сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="57a8b-179">When upgrading the client an error message appears</span></span>


<span data-ttu-id="57a8b-180">При обновлении клиента из MED-V 1.0 на MED-V 1.0 с пакетом обновления 1 (SP1) может появиться сообщение о том, что Рабочая область MED-V не определена.</span><span class="sxs-lookup"><span data-stu-id="57a8b-180">When upgrading the client from MED-V1.0 to MED-V1.0 SP1, a message may appear notifying you that no MED-V workspace is defined.</span></span>

### <span data-ttu-id="57a8b-181">Решение</span><span class="sxs-lookup"><span data-stu-id="57a8b-181">Solution</span></span>

<span data-ttu-id="57a8b-182">Закройте клиент и перезапустите его.</span><span class="sxs-lookup"><span data-stu-id="57a8b-182">Close the client and restart it.</span></span>

## <span data-ttu-id="57a8b-183">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="57a8b-183">Related topics</span></span>


[<span data-ttu-id="57a8b-184">Заметки о выпуске MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="57a8b-184">MED-V 1.0 Release Notes</span></span>](med-v-10-release-notesmedv-10.md)

[<span data-ttu-id="57a8b-185">Заметки о выпуске для MED-V 1.0 с пакетом обновления 1 (SP1) и пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="57a8b-185">MED-V 1.0 SP1 and SP2 Release Notes</span></span>](med-v-10-sp1-and-sp2-release-notesmedv-10-sp1.md)

 

 





