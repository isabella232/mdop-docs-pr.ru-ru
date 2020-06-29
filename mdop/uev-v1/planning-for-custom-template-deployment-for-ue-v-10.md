---
title: Планирование развертывания пользовательского шаблона для UE-V 1.0
description: Планирование развертывания пользовательского шаблона для UE-V 1.0
author: dansimp
ms.assetid: be76fc9a-31ca-4290-af11-7640dcb87d50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d17f058bff452f88003ab4488daa7afa846f688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821192"
---
# <span data-ttu-id="d98ab-103">Планирование развертывания пользовательского шаблона для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d98ab-103">Planning for Custom Template Deployment for UE-V 1.0</span></span>


<span data-ttu-id="d98ab-104">Виртуализация взаимодействия с пользователем Microsoft (UE-V) использует шаблоны расположений параметров (XML-файлы), которые определяют параметры, которые записываются и применяются UE-V.</span><span class="sxs-lookup"><span data-stu-id="d98ab-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="d98ab-105">Вы можете использовать генератор UE-V для создания настраиваемых шаблонов расположений параметров, которые позволяют пользователям перемещать параметры приложений, отличных от тех, которые включены в шаблоны по умолчанию UE-V.</span><span class="sxs-lookup"><span data-stu-id="d98ab-105">You can use the UE-V Generator to create custom settings location templates that let users roam the settings of applications other than those that are included in the default UE-V templates.</span></span> <span data-ttu-id="d98ab-106">После проверки настраиваемого шаблона для проверки правильности перемещения параметров приложения в тестовой среде вы можете развернуть эти шаблоны расположений параметров на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="d98ab-106">After you test the custom template to ensure that the application settings roam correctly in a test environment, you can deploy these settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="d98ab-107">Вы можете развернуть пользовательские шаблоны расположений с помощью существующей инфраструктуры развертывания, например для распространения программного обеспечения на предприятии (ESD), с помощью параметров групповой политики или настроив каталог шаблонов параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="d98ab-107">You can deploy your custom settings location templates with an existing deployment infrastructure, such as Enterprise Software Distribution (ESD), with Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="d98ab-108">Шаблоны, которые развертываются с помощью ESD или групповой политики, должны быть зарегистрированы на UE-V WMI или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d98ab-108">Templates that are deployed by using ESD or Group Policy must be registered with UE-V WMI or PowerShell.</span></span>

## <span data-ttu-id="d98ab-109">Каталог шаблонов параметров</span><span class="sxs-lookup"><span data-stu-id="d98ab-109">Settings template catalog</span></span>


<span data-ttu-id="d98ab-110">Каталог шаблонов параметров виртуализации пользователей — это путь к папке на компьютерах UE-V или сетевая папка SMB, в которой хранятся все пользовательские шаблоны расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="d98ab-110">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="d98ab-111">Агент UE-V извлекает из этого расположения новые или обновленные шаблоны.</span><span class="sxs-lookup"><span data-stu-id="d98ab-111">The UE-V agent retrieves new or updated templates from this location.</span></span> <span data-ttu-id="d98ab-112">Агент UE-V проверяет это расположение один раз в день и обновляет режим синхронизации на основе шаблонов в этой папке.</span><span class="sxs-lookup"><span data-stu-id="d98ab-112">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="d98ab-113">Шаблоны, добавленные или обновленные в этой папке с момента последней проверяются на наличие в ней агента UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d98ab-113">Templates that were added or updated in this folder since the last time that the folder was checked are registered by the UE-V agent.</span></span> <span data-ttu-id="d98ab-114">Агент UE-V отменяет регистрацию шаблонов, которые удаляются из этой папки.</span><span class="sxs-lookup"><span data-stu-id="d98ab-114">The UE-V agent deregisters templates that are removed from this folder.</span></span> <span data-ttu-id="d98ab-115">По умолчанию шаблоны регистрируются и отменяются один раз в день в 3:30 утра.</span><span class="sxs-lookup"><span data-stu-id="d98ab-115">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="d98ab-116">Локальное время планировщиком задач.</span><span class="sxs-lookup"><span data-stu-id="d98ab-116">local time by the task scheduler.</span></span> <span data-ttu-id="d98ab-117">Дополнительные сведения о задачах UE-V можно найти [в разделе Изменение частоты запланированных задач UE-v](changing-the-frequency-of-ue-v-scheduled-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="d98ab-117">For more information about the UE-V tasks, see [Changing the Frequency of UE-V Scheduled Tasks](changing-the-frequency-of-ue-v-scheduled-tasks.md).</span></span>

<span data-ttu-id="d98ab-118">Путь к каталогу шаблонов параметров можно настроить с помощью параметров командной строки установки, групповой политики, WMI или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d98ab-118">You can configure the settings template catalog path by using the install command-line options, Group Policy, WMI, or PowerShell.</span></span> <span data-ttu-id="d98ab-119">Шаблоны, которые хранятся в пути к каталогу шаблонов, автоматически регистрируются и отменяются с помощью запланированной задачи.</span><span class="sxs-lookup"><span data-stu-id="d98ab-119">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span> <span data-ttu-id="d98ab-120">Вы можете настроить это задание по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="d98ab-120">You can customize this scheduled task as needed.</span></span>

## <span data-ttu-id="d98ab-121">Замена шаблонов Microsoft по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d98ab-121">Replace the default Microsoft templates</span></span>


<span data-ttu-id="d98ab-122">Агент UE-V добавляет стандартную группу шаблонов расположения параметров для распространенных приложений Майкрософт и параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="d98ab-122">The UE-V agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="d98ab-123">Если в вашей организации необходимо настроить собственные версии этих шаблонов, агент UE-V Agent можно настроить на использование каталога шаблонов параметров, а затем заменить стандартные шаблоны Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d98ab-123">If your enterprise needs customized versions of these templates, the UE-V agent can be configured to use a settings template catalog and you should then replace the default Microsoft templates.</span></span>

<span data-ttu-id="d98ab-124">При установке агента UE-V можно использовать параметр командной строки, `RegisterMSTemplates` чтобы отключить регистрацию шаблонов Microsoft по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d98ab-124">During the installation of the UE-V agent, the command-line parameter, `RegisterMSTemplates`, can be used to disable the registration of the default Microsoft templates.</span></span> <span data-ttu-id="d98ab-125">Дополнительные сведения о том, как настроить параметры UE-V, приведены в разделе [Планирование методов настройки UE-v](planning-for-ue-v-configuration-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d98ab-125">For more information about how to set the UE-V parameters, see [Planning for UE-V Configuration Methods](planning-for-ue-v-configuration-methods.md).</span></span>

<span data-ttu-id="d98ab-126">Если вы используете групповую политику для настройки пути к каталогу шаблонов параметров, вы можете заменить стандартные шаблоны Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d98ab-126">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="d98ab-127">Если вы настроили параметры политики для замены шаблонов Microsoft по умолчанию, все шаблоны Microsoft, установленные по умолчанию агентом UE-V, будут удалены с компьютера, а только шаблоны, которые находятся в каталоге шаблонов параметров, будут использоваться.</span><span class="sxs-lookup"><span data-stu-id="d98ab-127">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V agent will be deleted from the computer, and only the templates that are located in the settings template catalog will be used.</span></span> <span data-ttu-id="d98ab-128">`RegisterMSTemplates`Для того чтобы переопределить шаблон Microsoft по умолчанию, необходимо задать для параметра конфигурации агента UE-V значение true.</span><span class="sxs-lookup"><span data-stu-id="d98ab-128">The UE-V Agent configuration setting `RegisterMSTemplates` must be set to true in order to override the default Microsoft template.</span></span>

<span data-ttu-id="d98ab-129">**Примечание**  Если отключить этот параметр политики после включения, агент UE-V Agent не восстановит шаблоны Microsoft по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d98ab-129">**Note** If you disable this policy setting after it has been enabled, the UE-V agent will not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="d98ab-130">Если в каталоге шаблонов параметров есть настраиваемые шаблоны, которые используют тот же идентификатор, что и в шаблонах Microsoft по умолчанию, а агент UE-V не настроен на замену шаблонов Microsoft по умолчанию, шаблоны Microsoft в каталоге будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="d98ab-130">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V agent is not configured to replace the default Microsoft templates, the Microsoft templates in the catalog will be ignored.</span></span>

<span data-ttu-id="d98ab-131">Кроме того, вы можете заменить шаблоны по умолчанию с помощью функций UE-V PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d98ab-131">You can also replace the default templates by using the UE-V PowerShell features.</span></span> <span data-ttu-id="d98ab-132">Чтобы заменить шаблон Microsoft по умолчанию на PowerShell, отмените регистрацию всех шаблонов Microsoft, используемых по умолчанию, а затем зарегистрируйте пользовательские шаблоны.</span><span class="sxs-lookup"><span data-stu-id="d98ab-132">To replace the default Microsoft Template with PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="d98ab-133">**Примечание**  Старые пакеты параметров остаются в местоположении хранения параметров, даже если для приложения развернуты новые шаблоны параметров.</span><span class="sxs-lookup"><span data-stu-id="d98ab-133">**Note** Old settings packages remain in the settings storage location even if new settings templates are deployed for an application.</span></span> <span data-ttu-id="d98ab-134">Эти пакеты не прочтены агентом, но ни один из них не удаляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="d98ab-134">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <span data-ttu-id="d98ab-135">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d98ab-135">Related topics</span></span>


[<span data-ttu-id="d98ab-136">Планирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d98ab-136">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="d98ab-137">Планирование того, какие приложения необходимо синхронизировать с UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d98ab-137">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

[<span data-ttu-id="d98ab-138">Планирование методов конфигурации UE-V</span><span class="sxs-lookup"><span data-stu-id="d98ab-138">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

<span data-ttu-id="d98ab-139">Планирование развертывания настраиваемого шаблона</span><span class="sxs-lookup"><span data-stu-id="d98ab-139">Planning for Custom Template Deployment</span></span>
 

 





