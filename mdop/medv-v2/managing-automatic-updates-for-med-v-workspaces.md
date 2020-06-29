---
title: Управление автоматическими обновлениями для рабочих областей MED-V
description: Управление автоматическими обновлениями для рабочих областей MED-V
author: dansimp
ms.assetid: 306f28a2-d653-480d-b737-4b8b3132de5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b22d3250db806e740c1d62da4fed98d5956b0eeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825292"
---
# <span data-ttu-id="9f2b5-103">Управление автоматическими обновлениями для рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="9f2b5-103">Managing Automatic Updates for MED-V Workspaces</span></span>


<span data-ttu-id="9f2b5-104">Рабочая область MED-V — это виртуальная машина, которая содержит отдельную операционную систему, в которой должен управлять процесс автоматического обновления программного обеспечения, как и физические компьютеры в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-104">The MED-V workspace is a virtual machine that contains a separate operating system, whose automatic software update process must be managed just like the physical computers in your enterprise.</span></span> <span data-ttu-id="9f2b5-105">Поскольку гостевая операционная система не всегда должна выполняться при запуске операционной системы узла, необходимо убедиться в том, что виртуальная машина MED-V настроена таким образом, что при необходимости можно применять обновления программного обеспечения к гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-105">Because the guest operating system is not always necessarily running when the host operating system is running, you must ensure that the MED-V virtual machine is configured in such a way that software updates can be applied to the guest operating system as required.</span></span> <span data-ttu-id="9f2b5-106">Решение для Microsoft Enterprise Virtualization (MED-V) 2,0 предоставляет функциональные возможности, позволяющие определить, как автоматические обновления программного обеспечения обрабатываются в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-106">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution provides the functionality that lets you determine how automatic software updates are processed in a MED-V workspace.</span></span>

## <span data-ttu-id="9f2b5-107">Управление политикой пробуждения MED-V в рабочей области</span><span class="sxs-lookup"><span data-stu-id="9f2b5-107">Managing MED-V Workspace Wake-Up Policy</span></span>


<span data-ttu-id="9f2b5-108">Политика пробуждения MED-V обеспечивает доступность виртуальной машины MED-V для обновлений в течение времени, указанного в параметрах конфигурации для MED-V.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-108">The MED-V workspace wake-up policy guarantees that the MED-V virtual machine is made available for updates for the time that you specify in your MED-V configuration settings.</span></span> <span data-ttu-id="9f2b5-109">Это относится к обновлениям, опубликованным из Microsoft с помощью центра обновления Windows, а также обновлений, развернутых и управляемых решениями сторонних разработчиков, например антивирусными приложениями.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-109">This applies to both updates that are published from Microsoft through Windows Update and updates deployed and controlled by non-Microsoft solutions, such as antivirus applications.</span></span>

<span data-ttu-id="9f2b5-110">**Важно!**  Политика пробуждения для рабочей области MED-V оптимизирована для инфраструктуры центра обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-110">**Important** The MED-V workspace wake-up policy is optimized for the Microsoft Update infrastructure.</span></span> <span data-ttu-id="9f2b5-111">Если вы используете Microsoft System Center Configuration Manager для развертывания обновлений, не относящихся к корпорации Майкрософт, рекомендуется также использовать приложение System Center Updates Publisher, которое использует преимущества той же инфраструктуры, что и центр обновления Майкрософт, и, следовательно, преимущества из политики пробуждения MED-V.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-111">If you are using Microsoft System Center Configuration Manager to deploy non-Microsoft updates, we recommend that you also use the System Center Updates Publisher, which takes advantage of the same infrastructure as Microsoft Update and therefore benefits from the MED-V workspace wake-up policy.</span></span> <span data-ttu-id="9f2b5-112">Дополнительные сведения можно найти в разделе [Microsoft System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) ( https://go.microsoft.com/fwlink/?LinkId=200035) .</span><span class="sxs-lookup"><span data-stu-id="9f2b5-112">For more information, see [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) (https://go.microsoft.com/fwlink/?LinkId=200035).</span></span>

 

<span data-ttu-id="9f2b5-113">Когда вы создаете пакет рабочей области для MED-V, вы настроили время и способ начала работы, когда пользователь входит в систему (**Быстрый запуск**) или когда пользователь впервые открывает опубликованное приложение (**обычное начало**).</span><span class="sxs-lookup"><span data-stu-id="9f2b5-113">When you created your MED-V workspace package, you configured when and how it starts, either when the end user logs on (**Fast Start**) or when the end user first opens a published application (**Normal Start**).</span></span> <span data-ttu-id="9f2b5-114">Или установите флажок, чтобы конечный пользователь мог управлять этим параметром.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-114">Or you set the option to let the end user control this setting.</span></span>

<span data-ttu-id="9f2b5-115">В обоих случаях, когда выбран параметр **быстрого запуска** , виртуальная машина продолжает работать, пока узел MED-V вошел в систему как пользователь.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-115">Either way, whenever the **Fast Start** option is selected, the virtual machine continues to run as long as the MED-V host is logged on as User.</span></span> <span data-ttu-id="9f2b5-116">В этой конфигурации, так как MED-V активна, если узел активен, автоматические обновления применяются без необходимости дополнительной обработки из MED-V.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-116">In this configuration, because MED-V is active when the host is active, automatic updates are applied without requiring any extra processing from MED-V.</span></span>

<span data-ttu-id="9f2b5-117">Однако для тех случаев, когда **быстрое начало** не задано или переход на другой компьютер или спящий режим из рабочей области MED-v гарантирует, что операционная система на виртуальной машине регулярно обновляется даже в том случае, если med-v не используется регулярно.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-117">However, for those cases in which **Fast Start** is not specified or the virtual machine hibernates or stops, MED-V guarantees through its MED-V workspace wake-up policy that the guest operating system is being regularly updated even when MED-V is not used regularly.</span></span> <span data-ttu-id="9f2b5-118">MED-V выполняет эту функцию путем регулярного пробуждения виртуальной машины в соответствии с указанными параметрами конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-118">MED-V performs this function by regularly waking up the virtual machine based on the configuration settings that you specify.</span></span> <span data-ttu-id="9f2b5-119">Это позволит выполнять клиенты автоматических обновлений на виртуальной машине в соответствии с их конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-119">This enables the automatic update clients in the virtual machine to execute based on their configurations.</span></span><span data-ttu-id="9f2b5-120">По истечении периода времени, определенного параметром конфигурации MED-V, MED-V возвращает виртуальную машину в предыдущее состояние.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-120">After the time period defined by the MED-V configuration setting elapses, MED-V returns the virtual machine to its previous state.</span></span>

<span data-ttu-id="9f2b5-121">**Примечание**  Если конечный пользователь открывает опубликованное приложение в течение периода обновления, применяются необходимые обновления, но MED-V не переключается в спящий режим и не закрывается по окончании срока действия обновления.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-121">**Note** If the end user opens a published application during the update period, the required updates are applied, but MED-V is not automatically hibernated or shut down after the update period ends.</span></span> <span data-ttu-id="9f2b5-122">Вместо этого MED-V продолжает работу.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-122">Instead, MED-V continues running.</span></span>

 

<span data-ttu-id="9f2b5-123">Политика пробуждения для рабочей области MED-V включает три основных компонента:</span><span class="sxs-lookup"><span data-stu-id="9f2b5-123">The MED-V workspace wake-up policy includes three main components:</span></span>

**<span data-ttu-id="9f2b5-124">Диспетчер гостевых обновлений</span><span class="sxs-lookup"><span data-stu-id="9f2b5-124">Guest Update Manager</span></span>**

<span data-ttu-id="9f2b5-125">Этот автономный исполняемый файл, находящийся на узле MED-V, отвечает за пробуждение виртуальной машины в соответствии с предопределенным настраиваемым расписанием.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-125">Residing on the MED-V host, this stand-alone executable program is responsible for waking up the virtual machine according to a predefined, configurable schedule.</span></span> <span data-ttu-id="9f2b5-126">Укажите параметры конфигурации, указывающие, когда диспетчер обновлений должен выводить виртуальную машину каждый день, а также время, в течение которого виртуальная машина должна находиться в спящем режиме (в минутах), чтобы разрешить применение обновлений.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-126">Specify the configuration settings to indicate at what time the update manager should wake up the virtual machine every day, and how long the virtual machine should be kept awake (in minutes) to allow for updates to be applied.</span></span> <span data-ttu-id="9f2b5-127">После того как указанное количество минут было достигнуто, диспетчер гостевых обновлений переводит виртуальную машину в спящий режим, подготовленный для следующего использования.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-127">After the number of minutes specified has been reached, the guest update manager puts the virtual machine into hibernation, prepared for the next use.</span></span> <span data-ttu-id="9f2b5-128">Вы можете запланировать выполнение исполняемой программы с помощью диспетчера задач Windows.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-128">You can schedule the execution of this executable program through the Windows Task Manager.</span></span>

**<span data-ttu-id="9f2b5-129">Служба управления перезапуском гостя</span><span class="sxs-lookup"><span data-stu-id="9f2b5-129">Guest Restart Management Service</span></span>**

<span data-ttu-id="9f2b5-130">У этой услуги есть три основные обязанности, находящиеся на узле MED-V.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-130">Residing on the MED-V host, this service has three primary responsibilities.</span></span> <span data-ttu-id="9f2b5-131">Кроме того, с помощью гостевого центра обновления вы управляете перезапуском виртуальной машины при входе пользователя, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-131">Along with the Guest Update Manager, it manages the restart of the virtual machine at user logon, if it is required.</span></span> <span data-ttu-id="9f2b5-132">Она обнаруживает, когда требуется перезагрузка виртуальной машины из – за установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-132">It detects when virtual machine restarts are required caused by updates being installed.</span></span> <span data-ttu-id="9f2b5-133">Кроме того, это гарантирует, что задача для диспетчера гостевых обновлений будет всегда планироваться согласно настройке.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-133">And it ensures that the task for the Guest Update Manager is always scheduled according to configuration.</span></span>

**<span data-ttu-id="9f2b5-134">Служба гостевых обновлений</span><span class="sxs-lookup"><span data-stu-id="9f2b5-134">Guest Update Service</span></span>**

<span data-ttu-id="9f2b5-135">На виртуальной машине MED-V эта служба Windows несет ответственность за наблюдение за установкой обновлений, требующих перезапуска.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-135">Residing on the MED-V virtual machine, this Windows service has the responsibility of monitoring when installed updates require a restart.</span></span> <span data-ttu-id="9f2b5-136">После того как служба сознает необходимость перезапуска, она уведомляет службу управления перезапуском гостя на узле.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-136">After the service becomes aware of the need for a restart, it notifies the guest restart management service on the host.</span></span>

### <span data-ttu-id="9f2b5-137">Параметры конфигурации для политики пробуждения рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="9f2b5-137">Configuration Settings for MED-V Workspace Wake-Up Policy</span></span>

<span data-ttu-id="9f2b5-138">Вы можете управлять тем, когда и как долго виртуальная машина должна получать автоматические обновления, определяя следующие два значения конфигурации в реестре.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-138">You control when and for how long the virtual machine awakens to receive automatic updates by defining the following two configuration values in the registry.</span></span> <span data-ttu-id="9f2b5-139">Оба этих значения находятся под ключом HKLM\\Software\\Microsoft\\MEDV\\v2\\VM.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-139">Both of these values are located under the HKLM\\Software\\Microsoft\\MEDV\\v2\\VM key.</span></span>

<span data-ttu-id="9f2b5-140">**GuestUpdateTime** — настраивается час и минута, когда MED-V должен пробудить виртуальную машину для обновления, основываясь на стандарте 24-часового времени.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-140">**GuestUpdateTime** – Configures the hour and minute each day when MED-V must wake up the virtual machine for updating, based on the 24-hour clock standard.</span></span> <span data-ttu-id="9f2b5-141">Укажите время в формате чч: мм.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-141">Specify the time in the format HH:MM.</span></span> <span data-ttu-id="9f2b5-142">Значение по умолчанию — 00:00 (полночь).</span><span class="sxs-lookup"><span data-stu-id="9f2b5-142">The default value is 00:00 (midnight).</span></span>

<span data-ttu-id="9f2b5-143">**GuestUpdateDuration** — настраивает количество минут, в течение которых MED-V должен поддерживать обновление виртуальной машины в спящем режиме для обновления, начиная с указанного в параметре GuestUpdateTime конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-143">**GuestUpdateDuration** – Configures the number of minutes that MED-V must keep the virtual machine awake for updating, starting at the time specified in the GuestUpdateTime configuration setting.</span></span> <span data-ttu-id="9f2b5-144">Значение по умолчанию — 240 (4 часа).</span><span class="sxs-lookup"><span data-stu-id="9f2b5-144">The default value is 240 (4 hours).</span></span> <span data-ttu-id="9f2b5-145">Установка этого значения равным нулю (0) отключает политику пробуждения MED-V.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-145">Setting this value to zero (0) disables the MED-V workspace wake-up policy.</span></span>

<span data-ttu-id="9f2b5-146">Дополнительные сведения о том, как определить значения конфигурации MED-V, можно найти в разделе [Управление параметрами конфигурации в рабочей области для MED-v](managing-med-v-workspace-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="9f2b5-146">For more information about how to define your MED-V configuration values, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="9f2b5-147">**Примечание**  Для работы с помощью MED-V рекомендуется настроить интервал пробуждения таким образом, чтобы он соответствовал времени, в течение которого виртуальные машины MED-V планируется обновлять регулярно.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-147">**Note** A MED-V best practice is to set your wake up interval to match the time when MED-V virtual machines are planned to be updated regularly.</span></span> <span data-ttu-id="9f2b5-148">Кроме того, рекомендуется настроить эти параметры таким образом, чтобы они соответствовали поведению хост-компьютера.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-148">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

 

### <span data-ttu-id="9f2b5-149">Уведомление о перезагрузке с использованием системы ESD</span><span class="sxs-lookup"><span data-stu-id="9f2b5-149">Reboot Notification Using your ESD System</span></span>

<span data-ttu-id="9f2b5-150">Вы можете настроить систему ESD для уведомления MED-V каждый раз, когда требуется перезагрузка для рабочей области MED-V после применения автоматических обновлений.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-150">You can configure your ESD system to notify MED-V whenever a restart is required for the MED-V workspace after automatic updates have been applied.</span></span> <span data-ttu-id="9f2b5-151">При применении автоматических обновлений с помощью системы ESD, для которой требуется перезагрузка, необходимо написать сценарий, сообщающий о следующем глобальном событии в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-151">When you apply automatic updates through your ESD system that you know require a restart, you should write a script to signal the following global event on the MED-V workspace:</span></span>

<span data-ttu-id="9f2b5-152">**Важно!**  Вы должны открыть событие с правами только на изменение и подать ему сигнал.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-152">**Important** You must open the event with Modify Only rights and then signal it.</span></span> <span data-ttu-id="9f2b5-153">Если вы не откроете его с правильными разрешениями, это не повлияет на работу.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-153">If you do not open it with the correct permissions, it does not work.</span></span>

 

``` syntax
/// <summary>
/// The guest is required to be restarted due to an ESD update.
/// </summary>
public const string MedvGuestRebootRequiredEventName = @"Global\MedvGuestRebootRequiredEvent";
using (EventWaitHandle notificationEvent = 
EventWaitHandle.OpenExisting(eventName, EventWaitHandleRights.Modify))
{
notificationEvent.Set();
}
```

<span data-ttu-id="9f2b5-154">Когда вы сообщаете о событии, MED-V захватывает его и информирует виртуальную машину о необходимости перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="9f2b5-154">When you signal this event, MED-V captures it and informs the virtual machine that a restart is required.</span></span>

## <span data-ttu-id="9f2b5-155">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9f2b5-155">Related topics</span></span>


[<span data-ttu-id="9f2b5-156">Управление обновлениями программного обеспечения для рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="9f2b5-156">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

 

 





