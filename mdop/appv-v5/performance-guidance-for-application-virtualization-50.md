---
title: Рекомендации по производительности для Application Virtualization 5.0
description: Рекомендации по производительности для Application Virtualization 5.0
author: dansimp
ms.assetid: 6b3a3255-b957-4b9b-8bfc-a93fe8438a81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b0f5ef07935fc34adce772e7b2fff85a12b01dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813536"
---
# <span data-ttu-id="fa9f3-103">Рекомендации по производительности для Application Virtualization 5.0</span><span class="sxs-lookup"><span data-stu-id="fa9f3-103">Performance Guidance for Application Virtualization 5.0</span></span>


<span data-ttu-id="fa9f3-104">В этой статье описано, как настроить App-V 5,0 для оптимальной производительности, оптимизировать пакеты виртуальных приложений и обеспечить более эффективное взаимодействие с пользователями с помощью RDS и VDI.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-104">Learn how to configure App-V 5.0 for optimal performance, optimize virtual app packages, and provide a better user experience with RDS and VDI.</span></span>

<span data-ttu-id="fa9f3-105">Реализация нескольких методов поможет вам улучшить взаимодействие с конечными пользователями.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-105">Implementing multiple methods can help you improve the end-user experience.</span></span> <span data-ttu-id="fa9f3-106">Однако ваша среда может не поддерживать все методы.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-106">However, your environment may not support all methods.</span></span>

<span data-ttu-id="fa9f3-107">Прежде чем читать этот документ, вы должны прочитать и понять следующие данные.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-107">You should read and understand the following information before reading this document.</span></span>

-   [<span data-ttu-id="fa9f3-108">Руководство администратора Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="fa9f3-108">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="fa9f3-109">Публикация приложений для App-V 5 SP2 и взаимодействие с клиентами</span><span class="sxs-lookup"><span data-stu-id="fa9f3-109">App-V 5 SP2 Application Publishing and Client Interaction</span></span>](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [<span data-ttu-id="fa9f3-110">Руководство по упорядочению приложений Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="fa9f3-110">Microsoft Application Virtualization 5.0 Sequencing Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=269953)

**<span data-ttu-id="fa9f3-111">Примечание.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-111">Note</span></span>**  
<span data-ttu-id="fa9f3-112">Некоторые термины, используемые в этом документе, могут иметь различные значения в зависимости от внешнего источника и контекста.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-112">Some terms used in this document may have different meanings depending on external source and context.</span></span> <span data-ttu-id="fa9f3-113">Для получения дополнительных сведений об условиях, используемых в этом документе, а также звездочки **\\** \*, ознакомьтесь с разделом терминология, посвященной [производительности виртуализации приложений](#bkmk-terms1) .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-113">For more information about terms used in this document followed by an asterisk **\\**\* review the [Application Virtualization Performance Guidance Terminology](#bkmk-terms1) section of this document.</span></span>



<span data-ttu-id="fa9f3-114">Наконец, этот документ предоставит вам информацию о том, как настроить компьютер под управлением клиента App-V 5,0 и среды для обеспечения оптимальной производительности.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-114">Finally, this document will provide you with the information to configure the computer running App-V 5.0 client and the environment for optimal performance.</span></span> <span data-ttu-id="fa9f3-115">Оптимизируйте виртуальные пакеты приложений для повышения производительности с помощью секвенсора и Узнайте, как использовать виртуализацию взаимодействия с пользователем (UE-V) или другие технологии управления пользовательской средой для обеспечения оптимального взаимодействия с пользователем с помощью App-V 5,0 в службах удаленных рабочих столов и неустойчивой инфраструктуры виртуальных рабочих столов (VDI).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-115">Optimize your virtual application packages for performance using the sequencer, and to understand how to use User Experience Virtualization (UE-V) or other user environment management technologies to provide the optimal user experience with App-V 5.0 in both Remote Desktop Services (RDS) and non-persistent virtual desktop infrastructure (VDI).</span></span>

<span data-ttu-id="fa9f3-116">Чтобы определить, какая информация важна для вашей среды, ознакомьтесь с кратким обзором и контрольным списком применимости каждого раздела.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-116">To help determine what information is relevant to your environment you should review each section’s brief overview and applicability checklist.</span></span>

## <a href="" id="---------app-v-5-0-in-stateful--non-persistent-deployments"></a> <span data-ttu-id="fa9f3-117">App-V 5,0 в неустойчивых развертываниях с сохранением состояния</span><span class="sxs-lookup"><span data-stu-id="fa9f3-117">App-V 5.0 in stateful\* non-persistent deployments</span></span>


<span data-ttu-id="fa9f3-118">В этом разделе приводятся сведения о том, как сделать так, чтобы пользователь получит доступ ко всем виртуальным приложениям в течение секунд после входа.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-118">This section provides information about an approach that helps ensure a user will have access to all virtual applications within seconds after logging in.</span></span> <span data-ttu-id="fa9f3-119">Это достигается посредством уникальной адресации часто выполняемого обновления публикации App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-119">This is achieved by uniquely addressing the often long-running App-V 5.0 publishing refresh.</span></span> <span data-ttu-id="fa9f3-120">Как вы узнаете о том, что самый быстрый обновленный вариант, но не обязательно ничего делать.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-120">As you will discover the basis of the approach, the fastest publishing refresh, is one that doesn’t have to actually do anything.</span></span> <span data-ttu-id="fa9f3-121">Для обеспечения оптимального взаимодействия с пользователем должны выполняться некоторые условия, а также пошаговые инструкции.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-121">A number of conditions must be met and steps followed to provide the optimal user experience.</span></span>

<span data-ttu-id="fa9f3-122">Чтобы получить дополнительные сведения, воспользуйтесь приведенными ниже сведениями.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-122">Use the information in the following section for more information:</span></span>

<span data-ttu-id="fa9f3-123">[Сценарии использования](#bkmk-us) : при просмотре двух сценариев имейте в виду, что эти подходы являются крайними.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-123">[Usage Scenarios](#bkmk-us) - As you review the two scenarios, keep in mind that these are the approach extremes.</span></span> <span data-ttu-id="fa9f3-124">В соответствии с требованиями к использованию вы можете применить эти действия к подмножеству пользователей и/или виртуальных пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-124">Based on your usage requirements, you may choose to apply these steps to a subset of users and/or virtual applications packages.</span></span>

-   <span data-ttu-id="fa9f3-125">Оптимизировано для повышения производительности – для обеспечения оптимального взаимодействия можно ожидать, что основной образ включает некоторые пакеты виртуальных приложений App-V.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-125">Optimized for Performance – To provide the optimal experience, you can expect the base image to include some of the App-V virtual application package.</span></span> <span data-ttu-id="fa9f3-126">Эти и другие требования обсуждаются.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-126">This and other requirements are discussed.</span></span>

-   <span data-ttu-id="fa9f3-127">Оптимизировано для хранения — если вы собираетесь повлиять на хранение, следует рассмотреть этот сценарий, который поможет вам решить эти проблемы.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-127">Optimized for Storage – If you are concerned with the storage impact, following this scenario will help address those concerns.</span></span>

[<span data-ttu-id="fa9f3-128">Подготовка среды</span><span class="sxs-lookup"><span data-stu-id="fa9f3-128">Preparing your Environment</span></span>](#bkmk-pe)

-   <span data-ttu-id="fa9f3-129">Действия для подготовки базового образа (в непостоянном окружении VDI или узлов сеансов удаленных рабочих столов) для включения этого подхода необходимо выполнить в базовом образе только несколько шагов.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-129">Steps to Prepare the Base Image – Whether in a non-persistent VDI or RDSH environment, only a few steps must be completed in the base image to enable this approach.</span></span>

-   <span data-ttu-id="fa9f3-130">Использование UE-V 2,0 в качестве решения для управления профилями пользователей (UPM) для подхода App-V — это возможность, с помощью которой можно сохранить содержимое всего лишь нескольких разделов реестра и файлов.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-130">Use UE-V 2.0 as the User Profile Management (UPM) solution for the App-V approach – the cornerstone of this approach is the ability of a UEM solution to persist the contents of just a few registry and file locations.</span></span> <span data-ttu-id="fa9f3-131">Эти расположения образуют пользовательские интеграции \ \*.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-131">These locations constitute the user integrations\*.</span></span> <span data-ttu-id="fa9f3-132">Не забудьте ознакомиться с определенными требованиями для решения UPM.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-132">Be sure to review the specific requirements for the UPM solution.</span></span>

[<span data-ttu-id="fa9f3-133">Руководство по работе с пользователем</span><span class="sxs-lookup"><span data-stu-id="fa9f3-133">User Experience Walk-through</span></span>](#bkmk-uewt)

-   <span data-ttu-id="fa9f3-134">Пошаговое руководство — это пошаговое руководство по операциям App-V и UE-V, а также ожиданиям пользователей.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-134">Walk-through – This is a step-by-step walk-through of the App-V and UE-V operations and the expectations users should have.</span></span>

-   <span data-ttu-id="fa9f3-135">Результат — описывает ожидаемые результаты.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-135">Outcome – This describes the expected results.</span></span>

[<span data-ttu-id="fa9f3-136">Влияние на жизненный цикл пакета</span><span class="sxs-lookup"><span data-stu-id="fa9f3-136">Impact to Package Lifecycle</span></span>](#bkmk-plc)

[<span data-ttu-id="fa9f3-137">Улучшение возможностей VDI с помощью оптимизации и настройки производительности</span><span class="sxs-lookup"><span data-stu-id="fa9f3-137">Enhancing the VDI Experience through Performance Optimization/Tuning</span></span>](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a><span data-ttu-id="fa9f3-138">Контрольный список применимости</span><span class="sxs-lookup"><span data-stu-id="fa9f3-138">Applicability Checklist</span></span>

<span data-ttu-id="fa9f3-139">Среда развертывания</span><span class="sxs-lookup"><span data-stu-id="fa9f3-139">Deployment Environment</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="fa9f3-140">Несохраняемый VDI или сеансы сеансов.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-140">Non-Persistent VDI or RDSH.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="fa9f3-141">Виртуализация взаимодействия с пользователем (UE-V), другие решения UPM или диски профилей пользователей (UPD).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-141">User Experience Virtualization (UE-V), other UPM solutions or User Profile Disks (UPD).</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="fa9f3-142">Ожидаемая конфигурация</span><span class="sxs-lookup"><span data-stu-id="fa9f3-142">Expected Configuration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="fa9f3-143">Виртуализация взаимодействия с пользователем (UE-V) с включенным шаблоном состояния пользователя App-V или программным обеспечением управления профилями пользователей (UPM).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-143">User Experience Virtualization (UE-V) with the App-V user state template enabled or User Profile Management (UPM) software.</span></span> <span data-ttu-id="fa9f3-144">Программное обеспечение, поддерживающее UE-V UPM, должно быть способно инициироваться при входе или запуске процесса/приложения и выходе из него.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-144">Non-UE-V UPM software must be capable of triggering on Login or Process/Application Start and Logoff.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="fa9f3-145">Для App-V (SCS) настроено или настроено хранилище общих данных.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-145">App-V Shared Content Store (SCS) is configured or can be configured.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="fa9f3-146">ИТ – администрирование</span><span class="sxs-lookup"><span data-stu-id="fa9f3-146">IT Administration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="fa9f3-147">Администратору может потребоваться регулярно обновлять базовое изображение виртуальной машины, чтобы обеспечить оптимальную производительность или администратору для управления несколькими изображениями для разных групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-147">Admin may need to update the VM base image regularly to ensure optimal performance or Admin may need to manage multiple images for different user groups.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a><span data-ttu-id="fa9f3-148">Сценарий использования</span><span class="sxs-lookup"><span data-stu-id="fa9f3-148">Usage Scenario</span></span>

<span data-ttu-id="fa9f3-149">При просмотре двух сценариев имейте в виду, что эти подходы являются крайними.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-149">As you review the two scenarios, keep in mind that these approach the extremes.</span></span> <span data-ttu-id="fa9f3-150">В соответствии с требованиями к использованию вы можете применить эти действия к подмножеству пользователей, виртуальным пакетам приложений или обоим требованиям.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-150">Based on your usage requirements, you may choose to apply these steps to a subset of users, virtual application packages, or both.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa9f3-151">Оптимизировано для повышения производительности</span><span class="sxs-lookup"><span data-stu-id="fa9f3-151">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-152">Оптимизировано для хранения</span><span class="sxs-lookup"><span data-stu-id="fa9f3-152">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa9f3-153">Для обеспечения оптимального взаимодействия с пользователем этот подход использует возможности решения UPM и требует дополнительной подготовки изображения и может привести к некоторым дополнительным издержкам на Управление изображениями.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-153">To provide the most optimal user experience, this approach leverages the capabilities of a UPM solution and requires additional image preparation and can incur some additional image management overhead.</span></span></p>
<p><span data-ttu-id="fa9f3-154">Ниже описано множество улучшений производительности для неустойчивых развертываний с сохранением состояния.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-154">The following describes many performance improvements in stateful non-persistent deployments.</span></span> <span data-ttu-id="fa9f3-155">Дополнительные сведения можно найти в <strong> разделе Упорядочение шагов, которые помогут вам оптимизировать пакеты для публикации </strong> , а также ссылку на <strong> руководство по упорядочению для App-V 5,0 </strong> на странице "ознакомьтесь с <strong> разделом" в этом документе </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-155">For more information, see the <strong>Sequencing Steps to Optimize Packages for Publishing Performance</strong> and reference to <strong>App-V 5.0 Sequencing Guide</strong> in the <strong>See Also section of this document</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-156">Общие предположения в предыдущем сценарии по-прежнему применимы.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-156">The general expectations of the previous scenario still apply here.</span></span> <span data-ttu-id="fa9f3-157">Однако имейте в виду, что образы виртуальных машин обычно хранятся в очень дорогостоящих массивах; для этого подхода была выполнена незначительная процедура изменения.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-157">However, keep in mind that VM images are typically stored in very costly arrays; a slight alteration has been made to the approach.</span></span> <span data-ttu-id="fa9f3-158">Не заполняйте предварительную настройку виртуальных пакетов приложений, предназначенных для пользователей, в базовом образе.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-158">Do not pre-configure user-targeted virtual application packages in the base image.</span></span></p>
<p><span data-ttu-id="fa9f3-159">Влияние этого изменения подробно описано в разделе Краткое руководство по работе с пользователем в этом документе.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-159">The impact of this alteration is detailed in the User Experience Walkthrough section of this document.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a><span data-ttu-id="fa9f3-160">Подготовка среды</span><span class="sxs-lookup"><span data-stu-id="fa9f3-160">Preparing your Environment</span></span>

<span data-ttu-id="fa9f3-161">В следующей таблице приведены необходимые шаги для подготовки базового образа и UE-V или другого решения UPM для этого подхода.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-161">The following table displays the required steps to prepare the base image and the UE-V or another UPM solution for the approach.</span></span>

**<span data-ttu-id="fa9f3-162">Подготовка базового образа</span><span class="sxs-lookup"><span data-stu-id="fa9f3-162">Prepare the Base Image</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa9f3-163">Оптимизировано для повышения производительности</span><span class="sxs-lookup"><span data-stu-id="fa9f3-163">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-164">Оптимизировано для хранения</span><span class="sxs-lookup"><span data-stu-id="fa9f3-164">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa9f3-165">Установите пакет исправлений 4 (SP4) для клиента Application Virtualization 5,0 версии клиента.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-165">Install the Hotfix Package 4 for Application Virtualization 5.0 SP2 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-166">Установите UE-V и скачайте шаблон параметров App-V из коллекции шаблонов UE-V, ознакомьтесь с приведенными ниже инструкциями.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-166">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-167">Настройка режима общего доступа к хранилищу контента (SCS).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-167">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="fa9f3-168">Дополнительные сведения можно найти в разделе <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> Установка клиента App-V 5,0 для общего режима хранения содержимого </a> .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-168">For more information see <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)">How to Install the App-V 5.0 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-169">Настройка сохранения интеграции пользователей в реестре для входа в систему с параметром DWORD.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-169">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-170">Предварительно настройте все пользовательские и глобальные целевые пакеты, например <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-170">Pre-configure all user- and global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-171">Предварительная настройка всех групп пользователей и глобальных целевых подключений, например <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-171">Pre-configure all user- and global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-172">Предварительно публикуйте все глобальные целевые пакеты.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-172">Pre-publish all global-targeted packages.</span></span></p>
<p></p>
<p><span data-ttu-id="fa9f3-173">Административ</span><span class="sxs-lookup"><span data-stu-id="fa9f3-173">Alternatively,</span></span></p>
<ul>
<li><p><span data-ttu-id="fa9f3-174">Выполнить глобальную публикацию или обновить.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-174">Perform a global publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-175">Выполнение публикации или обновления пользователем.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-175">Perform a user publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-176">Отмените публикацию всех пакетов, предназначенных для пользователей.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-176">Un-publish all user-targeted packages.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-177">Удалите записи, указанные ниже пользователем (VFS) виртуальной файловой системы (DNS).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-177">Delete the following user-Virtual File System (VFS) entries.</span></span></p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa9f3-178">Установите пакет исправлений 4 (SP4) для клиента Application Virtualization 5,0 версии клиента.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-178">Install the Hotfix Package 4 for Application Virtualization 5.0 SP2 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-179">Установите UE-V и скачайте шаблон параметров App-V из коллекции шаблонов UE-V, ознакомьтесь с приведенными ниже инструкциями.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-179">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-180">Настройка режима общего доступа к хранилищу контента (SCS).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-180">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="fa9f3-181">Дополнительные сведения можно найти в разделе <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> Установка клиента App-V 5,0 для общего режима хранения содержимого </a> .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-181">For more information see <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)">How to Install the App-V 5.0 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-182">Настройка сохранения интеграции пользователей в реестре для входа в систему с параметром DWORD.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-182">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-183">Предварительно настройте все глобальные целевые пакеты, например <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-183">Pre-configure all global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-184">Предварительная настройка всех глобальных целевых групп подключений например, <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-184">Pre-configure all global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-185">Предварительно публикуйте все глобальные целевые пакеты.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-185">Pre-publish all global-targeted packages.</span></span></p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="fa9f3-186">**Конфигурации** — для критически важных конфигураций клиента App-V и более подробного контекста и инструкции ознакомьтесь с приведенными ниже сведениями.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-186">**Configurations** - For critical App-V Client configurations and for a little more context and how-to, review the following information:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa9f3-187">Параметр конфигурации</span><span class="sxs-lookup"><span data-stu-id="fa9f3-187">Configuration Setting</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-188">Что это такое?</span><span class="sxs-lookup"><span data-stu-id="fa9f3-188">What does this do?</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-189">Как его использовать?</span><span class="sxs-lookup"><span data-stu-id="fa9f3-189">How should I use it?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa9f3-190">Режим общего хранилища содержимого (SCS)</span><span class="sxs-lookup"><span data-stu-id="fa9f3-190">Shared Content Store (SCS) Mode</span></span></p>
<ul>
<li><p><span data-ttu-id="fa9f3-191">Можно настроить в PowerShell с помощью <strong> Set-AppvClientConfiguration </strong> – <strong> SharedContentStoreMode </strong> или</span><span class="sxs-lookup"><span data-stu-id="fa9f3-191">Configurable in PowerShell using <strong>Set- AppvClientConfiguration</strong> –<strong>SharedContentStoreMode</strong>, or</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-192">Во время установки клиента App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-192">During installation of the App-V 5.0 client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="fa9f3-193">При запуске общего хранилища содержимого только публикуемые данные сохраняются на жестком диске. другие виртуальные ресурсы приложения поддерживаются в памяти (RAM).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-193">When running the shared content store only publishing data is maintained on hard disk; other virtual application assets are maintained in memory (RAM).</span></span></p>
<p><span data-ttu-id="fa9f3-194">Это позволяет экономить локальное хранилище и минимизировать количество дисковых операций ввода-вывода в секунду (I/O).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-194">This helps to conserve local storage and minimize disk I/O per second (IOPS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-195">Рекомендуется использовать это подключение при наличии подключений с малой задержкой между конечной точкой клиента App-V и сервером содержимого SCS, SAN.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-195">This is recommended when low-latency connections are available between the App-V Client endpoint and the SCS content server, SAN.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa9f3-196">PreserveUserIntegrationsOnLogin</span><span class="sxs-lookup"><span data-stu-id="fa9f3-196">PreserveUserIntegrationsOnLogin</span></span></p>
<ul>
<li><p><span data-ttu-id="fa9f3-197">Настройте в реестре в разделе <strong> HKEY_LOCAL_MACHINE </strong>  \  <strong> Программная </strong>  \  <strong> </strong>  \  <strong> интеграция Microsoft AppV </strong>  \  <strong> Client </strong>  \  <strong> Integration </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-197">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> \ <strong>Client</strong> \ <strong>Integration</strong>.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-198">Создайте значение DWORD <strong> PreserveUserIntegrationsOnLogin </strong> со значением <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-198">Create the DWORD value <strong>PreserveUserIntegrationsOnLogin</strong> with a value of <strong>1</strong>.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-199">Перезапустите клиентскую службу App-V или перезагрузите компьютер, на котором запущен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-199">Restart the App-V client service or restart the computer running the App-V Client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="fa9f3-200">Если вы не настроили ( <strong> Add-AppvClientPackage </strong> ) конкретный пакет и этот параметр не настроен, клиент App-V будет разинтегрироваться \* с сохраненной интеграцией пользователей, а затем снова интегрироваться в \*.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-200">If you have not pre-configured (<strong>Add-AppvClientPackage</strong>) a specific package and this setting is not configured, the App-V Client will de-integrate\* the persisted user integrations, then re-integrate\*.</span></span></p>
<p><span data-ttu-id="fa9f3-201">Для каждого пакета, удовлетворяющего описанным выше условиям, два раза в ходе публикации и обновления будут выполнять эти действия.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-201">For every package that meets the above conditions, effectively twice the work will be done during publishing/refresh.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-202">Если вы не планируете предварительно настроить все доступные пользовательские пакеты в базовом образе, используйте этот параметр.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-202">If you don’t plan to pre-configure every available user package in the base image, use this setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa9f3-203">MaxConcurrentPublishingRefresh</span><span class="sxs-lookup"><span data-stu-id="fa9f3-203">MaxConcurrentPublishingRefresh</span></span></p>
<ul>
<li><p><span data-ttu-id="fa9f3-204">Настройте в реестре в разделе <strong> HKEY_LOCAL_MACHINE </strong> &lt; надежная &gt; </strong>  \  <strong> </strong>  \  <strong> </strong> &lt; Публикация клиента Microsoft AppV strong &gt; </strong>  \  <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-204">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> &lt;strong&gt;Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> &lt;strong&gt;Client</strong> \ <strong>Publishing</strong>.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-205">Создайте значение DWORD <strong> MaxConcurrentPublishingrefresh </strong> с требуемым максимальным количеством параллельных обновлений публикации.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-205">Create the DWORD value <strong>MaxConcurrentPublishingrefresh</strong> with the desired maximum number of concurrent publishing refreshes.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-206">Не требуется перезапускать клиентскую службу App-V и компьютер.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-206">The App-V client service and computer do not need to be restarted.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="fa9f3-207">Этот параметр определяет количество пользователей, которые могут одновременно выполнять обновление публикации или синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-207">This setting determines the number of users that can perform a publishing refresh/sync at the same time.</span></span> <span data-ttu-id="fa9f3-208">Для параметра по умолчанию не задано ограничение.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-208">The default setting is no limit.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-209">Ограничение числа одновременных обновлений публикации предотвращает чрезмерное использование ЦП, что может повлиять на производительность компьютера.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-209">Limiting the number of concurrent publishing refreshes prevents excessive CPU usage that could impact computer performance.</span></span> <span data-ttu-id="fa9f3-210">Это ограничение рекомендовано в среде RDS, где несколько пользователей могут одновременно войти на один компьютер и выполнить синхронизацию для обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-210">This limit is recommended in an RDS environment, where multiple users can log in to the same computer at the same time and perform a publishing refresh sync.</span></span></p>
<p><span data-ttu-id="fa9f3-211">Если пороговое значение обновления параллельных публикаций достигнуто, время, необходимое для публикации новых приложений и получения доступа к ним для конечных пользователей, может занять неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-211">If the concurrent publishing refresh threshold is reached, the time required to publish new applications and make them available to end users after they log in could take an indeterminate amount of time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="fa9f3-212">Настройка решения UE-V для подхода App-V</span><span class="sxs-lookup"><span data-stu-id="fa9f3-212">Configure UE-V solution for App-V Approach</span></span>

<span data-ttu-id="fa9f3-213">Мы рекомендуем использовать Microsoft User Experience Virtualization (UE-V) для сбора и централизации параметров приложения и операционной системы Windows для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-213">We recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="fa9f3-214">Затем эти параметры применяются к разным компьютерам, к которым пользователь обращается, включая настольные компьютеры, Ноутбуки и сеансы инфраструктуры виртуальных рабочих столов (VDI).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-214">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span> <span data-ttu-id="fa9f3-215">UE-V оптимизирован для сценариев RDS и VDI.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-215">UE-V is optimized for RDS and VDI scenarios.</span></span>

<span data-ttu-id="fa9f3-216">Дополнительные сведения содержатся [в разделе Приступая к работе с виртуализацией взаимодействия с пользователем 2,0](https://technet.microsoft.com/library/dn458936.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa9f3-216">For more information see [Getting Started With User Experience Virtualization 2.0](https://technet.microsoft.com/library/dn458936.aspx)</span></span>

<span data-ttu-id="fa9f3-217">По сути, все, что нужно, — это установить клиент UE-V и загрузить следующий шаблон параметров Microsoft authored App-v из [коллекции шаблонов Microsoft User Experience Virtualization (UE-v)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-217">In essence all that is required is to install the UE-V client and download the following Microsoft authored App-V settings template from the [Microsoft User Experience Virtualization (UE-V) template gallery](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span></span> <span data-ttu-id="fa9f3-218">Зарегистрируйте шаблон.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-218">Register the template.</span></span> <span data-ttu-id="fa9f3-219">Дополнительные сведения о шаблонах UE-V см. [в разделе ресурс, специфический для UE-v, для приобретения и регистрации шаблона](https://technet.microsoft.com/library/dn458936.aspx).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-219">For more information around UE-V templates see [The UE-V specific resource for acquiring and registering the template](https://technet.microsoft.com/library/dn458936.aspx).</span></span>

**<span data-ttu-id="fa9f3-220">Примечание.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-220">Note</span></span>**  
<span data-ttu-id="fa9f3-221">Не выполняя дополнительные этапы настройки, Виртуализация среды пользователя Майкрософт (UE-V) не сможет синхронизировать ярлыки меню "Пуск" (lnk) на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-221">Without performing an additional configuration step, the Microsoft User Environment Virtualization (UE-V) will not be able to synchronize the Start menu shortcuts (.lnk files) on the target computer.</span></span> <span data-ttu-id="fa9f3-222">Тип файлов. lnk исключен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-222">The .lnk file type is excluded by default.</span></span>

<span data-ttu-id="fa9f3-223">UE-V поддерживает удаление файлов с расширением. lnk из списка исключений в сценариях RDS и VDI, где на каждом устройстве пользователя будет находиться один и тот же набор приложений, но каждый из файлов. lnk подходит для всех устройств пользователей.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-223">UE-V will only support removing the .lnk file type from the exclusion list in the RDS and VDI scenarios, where every user’s device will have the same set of applications installed to the same location and every .lnk file is valid for all the users’ devices.</span></span> <span data-ttu-id="fa9f3-224">Например, UE-V в настоящее время не поддерживает следующие 2 сценария, так как в этом случае вы увидите, что ярлык будет действителен на одном, но не на всех устройствах.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-224">For example, UE-V would not currently support the following 2 scenarios, because the net result will be that the shortcut will be valid on one but not all devices.</span></span>

-   <span data-ttu-id="fa9f3-225">Если у пользователя установлено приложение на одном устройстве с разделом LNK-файлы и оно установлено на другом устройстве в другой корневой каталог установки с поддержкой файлов. lnk.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-225">If a user has an application installed on one device with .lnk files enabled and the same native application installed on another device to a different installation root with .lnk files enabled.</span></span>

-   <span data-ttu-id="fa9f3-226">Если у пользователя установлено приложение на одном устройстве, но не другое, для которого включена поддержка LNK-файлов.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-226">If a user has an application installed on one device but not another with .lnk files enabled.</span></span>



**<span data-ttu-id="fa9f3-227">Важно.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-227">Important</span></span>**  
<span data-ttu-id="fa9f3-228">В этой статье описано, как изменить реестр Windows с помощью редактора реестра.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-228">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="fa9f3-229">Если изменить реестр Windows некорректно, это может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-229">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="fa9f3-230">Перед изменением реестра необходимо создать резервную копию файлов реестра (System. dat и User. dat).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-230">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="fa9f3-231">Корпорация Майкрософт не несет ответственности за то, что проблемы, которые могут возникнуть при изменении реестра, могут быть устранены.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-231">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="fa9f3-232">Изменение реестра на свой страх и риск.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-232">Change the registry at your own risk.</span></span>



<span data-ttu-id="fa9f3-233">С помощью редактора реестра Microsoft (regedit.exe) перейдите к разделу **hKey \ _LOCAL \ _MACHINE**  \\  **Программная**  \\  **Microsoft**  \\  **UEV**  \\  **Конфигурация агента**Microsoft UEV  \\  **Configuration**  \\  **ExcludedFileTypes** и удалите **. lnk** из исключенных типов файлов.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-233">Using the Microsoft Registry Editor (regedit.exe), navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **UEV** \\ **Agent** \\ **Configuration** \\ **ExcludedFileTypes** and remove **.lnk** from the excluded file types.</span></span>

**<span data-ttu-id="fa9f3-234">Настройка другого решения для управления профилями пользователей (UPM) для подхода App-V</span><span class="sxs-lookup"><span data-stu-id="fa9f3-234">Configure other User Profile Management (UPM) solution for App-V Approach</span></span>**

<span data-ttu-id="fa9f3-235">Предполагается, что в среде с сохранением состояния ожидается, что решение UPM реализовано и может поддерживать сохранение пользовательских данных во время сеансов и между входами.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-235">The expectation in a stateful environment is that a UPM solution is implemented and can support persistence of user data across sessions and between logins.</span></span>

<span data-ttu-id="fa9f3-236">Требования для решения UPM описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-236">The requirements for the UPM solution are as follows.</span></span>

<span data-ttu-id="fa9f3-237">Чтобы включить оптимизированное взаимодействие с входом, например приложение App-V 5,0 для пользователя, решение должно иметь возможность:</span><span class="sxs-lookup"><span data-stu-id="fa9f3-237">To enable an optimized login experience, for example the App-V 5.0 approach for the user, the solution must be capable of:</span></span>

-   <span data-ttu-id="fa9f3-238">Сохранение описанных ниже интеграционных компонентов в рамках профиля пользователя или персонажа.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-238">Persisting the below user integrations as part of the user profile/persona.</span></span>

-   <span data-ttu-id="fa9f3-239">Запуск синхронизации профилей пользователей при входе (или запуске приложения), что может гарантировать, что все интеграции пользователей будут применены перед публикацией или обновлением.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-239">Triggering a user profile sync on login (or application start), which can guarantee that all user integrations are applied before publishing/refresh begin, or,</span></span>

-   <span data-ttu-id="fa9f3-240">Присоединение и отсоединение диска профиля пользователя (UPD) или аналогичной технологии, которая включает в себя интеграцию пользователей.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-240">Attaching and detaching a user profile disk (UPD) or similar technology that contains the user integrations.</span></span>

-   <span data-ttu-id="fa9f3-241">Регистрация изменений в расположениях, которые составляют интеграцию пользователей перед выходом из сеанса.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-241">Capturing changes to the locations, which constitute the user integrations, prior to session logoff.</span></span>

<span data-ttu-id="fa9f3-242">С помощью App-V 5,0 при добавлении сервера публикаций (**Add-AppvPublishingServer**) можно настроить синхронизацию, например обновить при входе в систему и (или) после указанного интервала обновления.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-242">With App-V 5.0 when you add a publishing server (**Add-AppvPublishingServer**) you can configure synchronization, for example refresh during log on and/or after a specified refresh interval.</span></span> <span data-ttu-id="fa9f3-243">В обоих случаях создается запланированная задача.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-243">In both cases a scheduled task is created.</span></span>

<span data-ttu-id="fa9f3-244">В предыдущих версиях App-V 5,0 обе запланированные задачи были настроены с использованием сценария VBScript, который инициировал пользователю и глобальному обновлению.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-244">In previous versions of App-V 5.0, both scheduled tasks were configured using a VBScript that would initiate the user and global refresh.</span></span> <span data-ttu-id="fa9f3-245">В пакете исправлений 4 для Application Virtualization 5,0 с пакетом обновления 2 (SP2) обновление пользователей при входе инициируется **SyncAppvPublishingServer.exe**.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-245">With Hotfix Package 4 for Application Virtualization 5.0 SP2 the user refresh on log on is initiated by **SyncAppvPublishingServer.exe**.</span></span> <span data-ttu-id="fa9f3-246">Это изменение было введено для предоставления UPM решений в процессе запуска триггера.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-246">This change was introduced to provide UPM solutions a trigger process.</span></span> <span data-ttu-id="fa9f3-247">Этот процесс задерживает/Refresh публикации, чтобы позволить решению UPM применять интеграции пользователей.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-247">This process will delay the publish /refresh to allow the UPM solution to apply the user integrations.</span></span> <span data-ttu-id="fa9f3-248">После завершения публикации или обновления приложение завершит работу.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-248">It will exit once the publishing/refresh is complete.</span></span>

**<span data-ttu-id="fa9f3-249">Интеграция пользователей</span><span class="sxs-lookup"><span data-stu-id="fa9f3-249">User Integrations</span></span>**

<span data-ttu-id="fa9f3-250">Реестр — HKEY \ _CURRENT \ _USER</span><span class="sxs-lookup"><span data-stu-id="fa9f3-250">Registry – HKEY\_CURRENT\_USER</span></span>

-   <span data-ttu-id="fa9f3-251">Path — Software\\Classes</span><span class="sxs-lookup"><span data-stu-id="fa9f3-251">Path - Software\\Classes</span></span>

    <span data-ttu-id="fa9f3-252">Исключить: локальные параметры, ActivatableClasses, AppX \ \*</span><span class="sxs-lookup"><span data-stu-id="fa9f3-252">Exclude: Local Settings, ActivatableClasses, AppX\*</span></span>

-   <span data-ttu-id="fa9f3-253">Path — Software\\Microsoft\\AppV</span><span class="sxs-lookup"><span data-stu-id="fa9f3-253">Path - Software\\Microsoft\\AppV</span></span>

-   <span data-ttu-id="fa9f3-254">Пути — путь к Software\\Microsoft\\Windows\\CurrentVersion\\App</span><span class="sxs-lookup"><span data-stu-id="fa9f3-254">Path- Software\\Microsoft\\Windows\\CurrentVersion\\App Paths</span></span>

**<span data-ttu-id="fa9f3-255">Расположение файлов</span><span class="sxs-lookup"><span data-stu-id="fa9f3-255">File Locations</span></span>**

-   <span data-ttu-id="fa9f3-256">Root — "переменная среды" APPDATA</span><span class="sxs-lookup"><span data-stu-id="fa9f3-256">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="fa9f3-257">Path — Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="fa9f3-257">Path – Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="fa9f3-258">Root — "переменная среды" APPDATA</span><span class="sxs-lookup"><span data-stu-id="fa9f3-258">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="fa9f3-259">Path — Microsoft\\AppV\\Client\\Integration</span><span class="sxs-lookup"><span data-stu-id="fa9f3-259">Path – Microsoft\\AppV\\Client\\Integration</span></span>

-   <span data-ttu-id="fa9f3-260">Root — "переменная среды" APPDATA</span><span class="sxs-lookup"><span data-stu-id="fa9f3-260">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="fa9f3-261">Path — Microsoft\\Windows\\Start Menu\\Programs</span><span class="sxs-lookup"><span data-stu-id="fa9f3-261">Path - Microsoft\\Windows\\Start Menu\\Programs</span></span>

-   <span data-ttu-id="fa9f3-262">(Для сохранения всех ярлыков на рабочем столе, виртуальных и не виртуальных)</span><span class="sxs-lookup"><span data-stu-id="fa9f3-262">(To persist all desktop shortcuts, virtual and non-virtual)</span></span>

    <span data-ttu-id="fa9f3-263">Root-"KnownFolder" {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} FileMask-\ \*. lnk</span><span class="sxs-lookup"><span data-stu-id="fa9f3-263">Root - “KnownFolder” {B4BFCC3A-DB2C-424C-B029-7FE99A87C641}FileMask - \*.lnk</span></span>

**<span data-ttu-id="fa9f3-264">Microsoft User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="fa9f3-264">Microsoft User Experience Virtualization (UE-V)</span></span>**

<span data-ttu-id="fa9f3-265">Кроме того, мы рекомендуем использовать Microsoft User Experience Virtualization (UE-V) для сбора и централизации параметров приложения и операционной системы Windows для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-265">Additionally, we recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="fa9f3-266">Затем эти параметры применяются к разным компьютерам, к которым пользователь обращается, включая настольные компьютеры, Ноутбуки и сеансы инфраструктуры виртуальных рабочих столов (VDI).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-266">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="fa9f3-267">Дополнительные сведения приведены в разделе [Начало работы с интерфейсом виртуализации пользователей 1,0](https://technet.microsoft.com/library/jj680015.aspx) и [общим расположением параметров с помощью галереи шаблонов UE-V](https://technet.microsoft.com/library/jj679972.aspx).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-267">For more information see [Getting Started With User Experience Virtualization 1.0](https://technet.microsoft.com/library/jj680015.aspx) and [Sharing Settings Location Templates with the UE-V Template Gallery](https://technet.microsoft.com/library/jj679972.aspx).</span></span>

### <a href="" id="bkmk-uewt"></a><span data-ttu-id="fa9f3-268">Руководство по работе с пользователем</span><span class="sxs-lookup"><span data-stu-id="fa9f3-268">User Experience Walk-through</span></span>

<span data-ttu-id="fa9f3-269">Ниже приведены пошаговые инструкции по выполнению операций App-V и UPM, а также ожидаемые пользователи.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-269">This following is a step-by-step walk-through of the App-V and UPM operations and the expectations users should expect.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa9f3-270">Оптимизировано для повышения производительности</span><span class="sxs-lookup"><span data-stu-id="fa9f3-270">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-271">Оптимизировано для хранения</span><span class="sxs-lookup"><span data-stu-id="fa9f3-271">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa9f3-272">После реализации этого подхода в среде VDI или узлов сеансов удаленных рабочих столов при первом входе</span><span class="sxs-lookup"><span data-stu-id="fa9f3-272">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="fa9f3-273">Функционировани Инициируется публикация или обновление пользователем.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-273">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="fa9f3-274">Быстроте Если пользователь в первый раз опубликовал виртуальные приложения (например, не являющиеся постоянными), это займет обычное время публикации или обновления.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-274">(Expectation) If this is the first time a user has published virtual applications (e.g. non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-275">Функционировани После публикации/обновления решение UPM перехватывает пользовательские интеграции.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-275">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="fa9f3-276">Быстроте В зависимости от того, как настроено решение UPM, это может возникнуть в процессе выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-276">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="fa9f3-277">Это приведет к тому же или похожему расходу, как и при сохранении состояния пользователя.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-277">This will incur the same/similar overhead as persisting the user state.</span></span></p></li>
</ul>
<p><span data-ttu-id="fa9f3-278">При последующих входах:</span><span class="sxs-lookup"><span data-stu-id="fa9f3-278">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="fa9f3-279">Функционировани Решение UPM применяет к системе пользовательские интеграции перед публикацией и обновлением.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-279">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p>
<p><span data-ttu-id="fa9f3-280">Быстроте На рабочем столе есть ярлыки или в меню "Пуск", которое будет работать немедленно.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-280">(Expectation) There will be shortcuts present on the desktop, or in the start menu, which work immediately.</span></span> <span data-ttu-id="fa9f3-281">После завершения публикации/обновления (например, изменения в пакетных ресурсах) некоторые из них могут исчезнуть.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-281">When the publishing/refresh completes (i.e., package entitlements change), some may go away.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-282">Функционировани Публикация и обновление обрабатывают операции отмены публикации и публикации для изменений в целях обеспечения обслуживания пользовательских пакетов.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-282">(Operation) Publishing/refresh will process un-publish and publish operations for changes in user package entitlements.</span></span> <span data-ttu-id="fa9f3-283">Быстроте Если вы не намерены никаких изменений в отношении обслуживания, publishing1 закончится за считанные секунды.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-283">(Expectation) If there are no entitlement changes, publishing1 will complete in seconds.</span></span> <span data-ttu-id="fa9f3-284">В противном случае публикация/обновление будут увеличиваться относительно числа и сложности \* виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-284">Otherwise, the publishing/refresh will increase relative to the number and complexity\* of virtual applications</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-285">Функционировани Решение UPM повторно захватывает пользовательские интеграции при выходе из системы.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-285">(Operation) UPM solution will capture user integrations again at logoff.</span></span> <span data-ttu-id="fa9f3-286">Быстроте То же, что и в предыдущем.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-286">(Expectation) Same as previous.</span></span></p></li>
</ul>
<p><span data-ttu-id="fa9f3-287">¹ операция публикации ( <strong> Publish-AppVClientPackage </strong> ) добавляет записи в каталог пользователей, сопоставляет данные с пользователем, определяет локальное хранилище и завершает работу, выполняя все этапы интеграции.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-287">¹ The publishing operation (<strong>Publish-AppVClientPackage</strong>) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-288">После реализации этого подхода в среде VDI или узлов сеансов удаленных рабочих столов при первом входе</span><span class="sxs-lookup"><span data-stu-id="fa9f3-288">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="fa9f3-289">Функционировани Инициируется публикация или обновление пользователем.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-289">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="fa9f3-290">Быстроте</span><span class="sxs-lookup"><span data-stu-id="fa9f3-290">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="fa9f3-291">Если пользователь в первый раз опубликовал виртуальные приложения (например, не являющиеся постоянными), это займет обычное время публикации или обновления.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-291">If this is the first time a user has published virtual applications (e.g., non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-292">Первый и следующий входные имена будут затронуты предварительно настроенными пакетами (Добавить/обновить).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-292">First and subsequent logins will be impacted by pre-configuring of packages (add/refresh).</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="fa9f3-293">Функционировани После публикации/обновления решение UPM перехватывает пользовательские интеграции.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-293">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="fa9f3-294">Быстроте В зависимости от того, как настроено решение UPM, это может возникнуть в процессе выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-294">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="fa9f3-295">Это приведет к тому же или похожему расходу, как и при сохранении состояния пользователя</span><span class="sxs-lookup"><span data-stu-id="fa9f3-295">This will incur the same/similar overhead as persisting the user state</span></span></p></li>
</ul>
<p><span data-ttu-id="fa9f3-296">При последующих входах:</span><span class="sxs-lookup"><span data-stu-id="fa9f3-296">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="fa9f3-297">Функционировани Решение UPM применяет к системе пользовательские интеграции перед публикацией и обновлением.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-297">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-298">Функционировани Для добавления и обновления необходимо предварительно настроить все целевые приложения пользователей.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-298">(Operation) Add/refresh must pre-configure all user targeted applications.</span></span> <span data-ttu-id="fa9f3-299">Быстроте</span><span class="sxs-lookup"><span data-stu-id="fa9f3-299">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="fa9f3-300">Это может значительно увеличивать время доступности приложения (в порядке 10 секунд).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-300">This may increase the time to application availability significantly (on the order of 10’s of seconds).</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-301">Это увеличит время обновления публикации относительно числа и сложности \* виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-301">This will increase the publishing refresh time relative to the number and complexity\* of virtual applications.</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="fa9f3-302">Функционировани Публикация и обновление обрабатывают операции отмены публикации и публикации для изменения прав на пользовательские пакеты.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-302">(Operation) Publishing/refresh will process un-publish and publish operations for changes to user package entitlements.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa9f3-303">Результате</span><span class="sxs-lookup"><span data-stu-id="fa9f3-303">Outcome</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-304">Результате</span><span class="sxs-lookup"><span data-stu-id="fa9f3-304">Outcome</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa9f3-305">Так как интеграция пользователей полностью сохраняется, не будет работать, например, интеграция публикации/обновления для завершения.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-305">Because the user integrations are entirely preserved, there will be no work for example, integration for the publishing/refresh to complete.</span></span> <span data-ttu-id="fa9f3-306">Все виртуальные приложения будут доступны в течение секунд при входе.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-306">All virtual applications will be available within seconds of login.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-307">Публикация и обновление обрабатывают изменения пользователей, которые имеют право на работу с виртуальными приложениями, которые влияют на взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-307">The publishing/refresh will process changes to the users entitled virtual applications which impacts the experience.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="fa9f3-308">Так как добавление и обновление должны заново настроить все виртуальные приложения для виртуальной машины, будет расширено время обновления публикации при каждом входе.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-308">Because the add/refresh must re-configure all the virtual applications to the VM, the publishing refresh time on every login will be extended.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a><span data-ttu-id="fa9f3-309">Влияние на жизненный цикл пакета</span><span class="sxs-lookup"><span data-stu-id="fa9f3-309">Impact to Package Life Cycle</span></span>

<span data-ttu-id="fa9f3-310">Обновление пакета является важнейшим аспектом жизненного цикла пакета.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-310">Upgrading a package is a crucial aspect of the package lifecycle.</span></span> <span data-ttu-id="fa9f3-311">Чтобы гарантировать, что пользователи смогут получить доступ к соответствующим обновленным (опубликованным) пакетам виртуальных приложений, рекомендуется обновить базовое изображение, чтобы отразить эти изменения.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-311">To help guarantee users have access to the appropriate upgraded (published) or downgraded (un-published) virtual application packages, it is recommended you update the base image to reflect these changes.</span></span> <span data-ttu-id="fa9f3-312">Чтобы понять, Зачем просматривать следующий раздел:</span><span class="sxs-lookup"><span data-stu-id="fa9f3-312">To understand why review the following section:</span></span>

<span data-ttu-id="fa9f3-313">Приложение App-V 5,0 SP2 представил концепцию состояний "ожидание".</span><span class="sxs-lookup"><span data-stu-id="fa9f3-313">App-V 5.0 SP2 introduced the concept of pending states.</span></span> <span data-ttu-id="fa9f3-314">В прошлом</span><span class="sxs-lookup"><span data-stu-id="fa9f3-314">In the past,</span></span>

-   <span data-ttu-id="fa9f3-315">Если администратор изменил полномочия или создал новую версию пакета (обновлена), а также во время публикации или обновления этого пакета, то при выполнении операции отмены публикации или публикации, соответственно, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-315">If an administrator changed entitlements or created a new version of a package (upgraded) and during a publishing/refresh that package was in-use, the un-publish or publish operation, respectively, would fail.</span></span>

-   <span data-ttu-id="fa9f3-316">Теперь, если пакет используется, операция будет отложена.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-316">Now, if a package is in-use the operation will be pended.</span></span> <span data-ttu-id="fa9f3-317">Операции отмены публикации и публикации-отгрузки будут обрабатываться при перезапуске службы или при выполнении другой команды публикации или отмены публикации.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-317">The un-publish and publish-pend operations will be processed on service restart or if another publish or un-publish command is issued.</span></span> <span data-ttu-id="fa9f3-318">В последнем случае, если виртуальное приложение используется в противном случае, виртуальное приложение останется в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-318">In the latter case, if the virtual application is in-use otherwise, the virtual application will remain in a pending state.</span></span> <span data-ttu-id="fa9f3-319">Для глобально опубликованных пакетов часто требуется перезагрузка (или перезапуск службы).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-319">For globally published packages, a restart (or service restart) often needed.</span></span>

<span data-ttu-id="fa9f3-320">Маловероятно, что в непостоянной среде эти отложенные операции будут обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-320">In a non-persistent environment, it is unlikely these pended operations will be processed.</span></span> <span data-ttu-id="fa9f3-321">Отложенные операции, например задачи, регистрируются в разделе **hKey \ _CURRENT \ _USER**  \\  **программного обеспечения**  \\  **клиента Microsoft**  \\  **AppV**  \\  **Client**  \\  **PendingTasks**.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-321">The pended operations, for example tasks are captured under **HKEY\_CURRENT\_USER** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **PendingTasks**.</span></span> <span data-ttu-id="fa9f3-322">Несмотря на то, что это расположение сохраняется решением UPM, если оно не применяется к среде перед входом в систему, оно не будет обработано.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-322">Although this location is persisted by the UPM solution, if it is not applied to the environment prior to log on, it will not be processed.</span></span>

### <a href="" id="bkmk-evdi"></a><span data-ttu-id="fa9f3-323">Улучшение возможностей VDI с помощью настройки оптимизации производительности</span><span class="sxs-lookup"><span data-stu-id="fa9f3-323">Enhancing the VDI Experience through Performance Optimization Tuning</span></span>

<span data-ttu-id="fa9f3-324">В следующем разделе содержатся списки, содержащие сведения о документации и загружаемых файлах, которые могут быть полезны при оптимизации среды для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-324">The following section contains lists with information about Microsoft documentation and downloads that may be useful when optimizing your environment for performance.</span></span>

**<span data-ttu-id="fa9f3-325">Блог и сценарий NGEN .NET (настоятельно рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="fa9f3-325">.NET NGEN Blog and Script (Highly Recommended)</span></span>**

<span data-ttu-id="fa9f3-326">О технологии NGEN</span><span class="sxs-lookup"><span data-stu-id="fa9f3-326">About NGEN technology</span></span>

-   [<span data-ttu-id="fa9f3-327">Ускорение оптимизации NGEN</span><span class="sxs-lookup"><span data-stu-id="fa9f3-327">How to speed up NGEN optimization</span></span>](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [<span data-ttu-id="fa9f3-328">Сценарий</span><span class="sxs-lookup"><span data-stu-id="fa9f3-328">Script</span></span>](https://aka.ms/DrainNGenQueue)

**<span data-ttu-id="fa9f3-329">Сервер и роли сервера Windows</span><span class="sxs-lookup"><span data-stu-id="fa9f3-329">Windows Server and Server Roles</span></span>**

<span data-ttu-id="fa9f3-330">Рекомендации по настройке производительности сервера для</span><span class="sxs-lookup"><span data-stu-id="fa9f3-330">Server Performance Tuning Guidelines for</span></span>

-   [<span data-ttu-id="fa9f3-331">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fa9f3-331">Microsoft Windows Server 2012 R2</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [<span data-ttu-id="fa9f3-332">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fa9f3-332">Microsoft Windows Server 2012</span></span>](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [<span data-ttu-id="fa9f3-333">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fa9f3-333">Microsoft Windows Server 2008 R2</span></span>](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**<span data-ttu-id="fa9f3-334">Роли сервера</span><span class="sxs-lookup"><span data-stu-id="fa9f3-334">Server Roles</span></span>**

-   [<span data-ttu-id="fa9f3-335">Узел виртуализации удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="fa9f3-335">Remote Desktop Virtualization Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [<span data-ttu-id="fa9f3-336">Узел сеансов удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="fa9f3-336">Remote Desktop Session Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [<span data-ttu-id="fa9f3-337">Релевантность для IIS: управление App-V, публикация, веб-службы отчетов</span><span class="sxs-lookup"><span data-stu-id="fa9f3-337">IIS Relevance: App-V Management, Publishing, Reporting Web Services</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [<span data-ttu-id="fa9f3-338">Релевантность файлового сервера (SMB): Если используется для хранения содержимого App-V и доставки в режиме SCS</span><span class="sxs-lookup"><span data-stu-id="fa9f3-338">File Server (SMB) Relevance: If used for App-V Content Storage and Delivery in SCS Mode</span></span>](https://technet.microsoft.com/library/jj134210.aspx)

**<span data-ttu-id="fa9f3-339">Руководство по настройке производительности клиента Windows (гостевой ОС)</span><span class="sxs-lookup"><span data-stu-id="fa9f3-339">Windows Client (Guest OS) Performance Tuning Guidance</span></span>**

-   [<span data-ttu-id="fa9f3-340">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="fa9f3-340">Microsoft Windows 7</span></span>](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [<span data-ttu-id="fa9f3-341">Сценарий оптимизации: (предоставлено службой поддержки Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="fa9f3-341">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [<span data-ttu-id="fa9f3-342">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="fa9f3-342">Microsoft Windows 8</span></span>](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [<span data-ttu-id="fa9f3-343">Сценарий оптимизации: (предоставлено службой поддержки Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="fa9f3-343">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## <span data-ttu-id="fa9f3-344">Последовательность действий по оптимизации пакетов для повышения производительности публикации</span><span class="sxs-lookup"><span data-stu-id="fa9f3-344">Sequencing Steps to Optimize Packages for Publishing Performance</span></span>


<span data-ttu-id="fa9f3-345">App-V 5,0 и App-V 5,0 SP2 предоставляют значительные значения в соответствующих выпусках.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-345">App-V 5.0 and App-V 5.0 SP2 provide significant value in their respective releases.</span></span> <span data-ttu-id="fa9f3-346">Некоторые функции упрощают новые сценарии или включены новые сценарии развертывания клиентов.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-346">Several features facilitate new scenarios or enabled new customer deployment scenarios.</span></span> <span data-ttu-id="fa9f3-347">Следующие функции могут повлиять на производительность операций публикации и запуска.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-347">These following features can impact the performance of the publishing and launch operations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa9f3-348">Шаг</span><span class="sxs-lookup"><span data-stu-id="fa9f3-348">Step</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-349">Параметр</span><span class="sxs-lookup"><span data-stu-id="fa9f3-349">Consideration</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-350">Преимущества</span><span class="sxs-lookup"><span data-stu-id="fa9f3-350">Benefits</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-351">Необходимости компромиссов</span><span class="sxs-lookup"><span data-stu-id="fa9f3-351">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa9f3-352">Отсутствует блок компонентов 1 (FB1, также называемый основным FB)</span><span class="sxs-lookup"><span data-stu-id="fa9f3-352">No Feature Block 1 (FB1, also known as Primary FB)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-353">Нет FB1 означает, что приложение будет запущено немедленно и не попадет сообщение об ошибке потока (для работы приложения требуется файл, DLL и он должен переключаться по сети) во время запуска. Если у вас есть ограничения сети, FB1 будет:</span><span class="sxs-lookup"><span data-stu-id="fa9f3-353">No FB1 means the application will launch immediately and stream fault (application requires file, DLL and must pull down over the network) during launch.If there are network limitations, FB1 will:</span></span></p>
<ul>
<li><p><span data-ttu-id="fa9f3-354">Уменьшите количество сбоев потоков и пропускную способность сети, используемую при запуске приложения в первый раз.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-354">Reduce the number of stream faults and network bandwidth used when you launch an application for the first time.</span></span></p></li>
<li><p><span data-ttu-id="fa9f3-355">Задерживает запуск, пока не будет переFB1ся весь поток.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-355">Delay launch until the entire FB1 has been streamed.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="fa9f3-356">Сбой потока уменьшает время запуска.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-356">Stream faulting decreases the launch time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-357">Пакеты виртуальных приложений, для которых настроен FB1, должны быть повторно упорядочены.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-357">Virtual application packages with FB1 configured will need to be re-sequenced.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="fa9f3-358">Удаление FB1</span><span class="sxs-lookup"><span data-stu-id="fa9f3-358">Removing FB1</span></span>

<span data-ttu-id="fa9f3-359">Для удаления FB1 не требуется исходный установщик приложения.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-359">Removing FB1 does not require the original application installer.</span></span> <span data-ttu-id="fa9f3-360">После выполнения описанных ниже действий рекомендуется вернуть компьютер, на котором запущен секвенсор, в пустой снимок.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-360">After completing the following steps, it is suggested that you revert the computer running the sequencer to a clean snapshot.</span></span>

<span data-ttu-id="fa9f3-361">**Интерфейс Sequencer** — создание нового пакета виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-361">**Sequencer UI** - Create a New Virtual Application Package.</span></span>

1.  <span data-ttu-id="fa9f3-362">Завершите этапы последовательности, чтобы настроить &gt; потоковую передачу.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-362">Complete the sequencing steps up to Customize -&gt; Streaming.</span></span>

2.  <span data-ttu-id="fa9f3-363">При потоковой передаче не выбирайте параметр **оптимизировать пакет для развертывания в медленной или ненадежной сети**.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-363">At the Streaming step, do not select **Optimize the package for deployment over slow or unreliable network**.</span></span>

3.  <span data-ttu-id="fa9f3-364">При необходимости перейдите на **целевую операционную систему**.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-364">If desired, move on to **Target OS**.</span></span>

**<span data-ttu-id="fa9f3-365">Изменение существующего пакета виртуальных приложений</span><span class="sxs-lookup"><span data-stu-id="fa9f3-365">Modify an Existing Virtual Application Package</span></span>**

1.  <span data-ttu-id="fa9f3-366">Завершите этапы последовательности, чтобы переписать поток.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-366">Complete the sequencing steps up to Streaming.</span></span>

2.  <span data-ttu-id="fa9f3-367">Не выбирайте параметр **оптимизировать пакет для развертывания в медленной или ненадежной сети**.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-367">Do not select **Optimize the package for deployment over a slow or unreliable network**.</span></span>

3.  <span data-ttu-id="fa9f3-368">Переместить, чтобы **создать пакет**.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-368">Move to **Create Package**.</span></span>

<span data-ttu-id="fa9f3-369">**PowerShell** — обновите существующий виртуальный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-369">**PowerShell** - Update an Existing Virtual Application Package.</span></span>

1.  <span data-ttu-id="fa9f3-370">Откройте сеанс PowerShell с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-370">Open an elevated PowerShell session.</span></span>

2.  <span data-ttu-id="fa9f3-371">Import-Module **appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-371">Import-module **appvsequencer**.</span></span>

3.  <span data-ttu-id="fa9f3-372">**Update-AppvSequencerPackage**  -  **AppvPackageFilePath**</span><span class="sxs-lookup"><span data-stu-id="fa9f3-372">**Update-AppvSequencerPackage** - **AppvPackageFilePath**</span></span>

    <span data-ttu-id="fa9f3-373">"C:\\Packages\\MyPackage.appv" — установщик</span><span class="sxs-lookup"><span data-stu-id="fa9f3-373">"C:\\Packages\\MyPackage.appv" -Installer</span></span>

    <span data-ttu-id="fa9f3-374">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath</span><span class="sxs-lookup"><span data-stu-id="fa9f3-374">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe" -OutputPath</span></span>

    <span data-ttu-id="fa9f3-375">"C:\\UpgradedPackages"</span><span class="sxs-lookup"><span data-stu-id="fa9f3-375">"C:\\UpgradedPackages"</span></span>

    **<span data-ttu-id="fa9f3-376">Примечание.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-376">Note</span></span>**  
    <span data-ttu-id="fa9f3-377">Для этого командлета требуется исполняемый (exe) или пакетный файл (bat).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-377">This cmdlet requires an executable (.exe) or batch file (.bat).</span></span> <span data-ttu-id="fa9f3-378">Необходимо предоставить пустой (не имеющий ничего) исполняемый или пакетный файл.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-378">You must provide an empty (does nothing) executable or batch file.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa9f3-379">Шаг</span><span class="sxs-lookup"><span data-stu-id="fa9f3-379">Step</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-380">Довод</span><span class="sxs-lookup"><span data-stu-id="fa9f3-380">Considerations</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-381">Преимущества</span><span class="sxs-lookup"><span data-stu-id="fa9f3-381">Benefits</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-382">Необходимости компромиссов</span><span class="sxs-lookup"><span data-stu-id="fa9f3-382">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa9f3-383">Без установки SXS на этапе публикации (предварительно устанавливаемые сборки SxS)</span><span class="sxs-lookup"><span data-stu-id="fa9f3-383">No SXS Install at Publish (Pre-Install SxS assemblies)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-384">Виртуальные пакеты приложений не нуждаются в повторной последовательности.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-384">Virtual Application packages do not need to be re-sequenced.</span></span> <span data-ttu-id="fa9f3-385">Сборки SxS могут оставаться в виртуальном пакете приложений.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-385">SxS Assemblies can remain in the virtual application package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-386">Зависимости сборок SxS не будут устанавливаться во время публикации.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-386">The SxS Assembly dependencies will not install at publishing time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-387">Зависимости сборок SxS должны быть предварительно установлены.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-387">SxS Assembly dependencies must be pre-installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="fa9f3-388">Создание нового пакета виртуальных приложений в секвенсоре</span><span class="sxs-lookup"><span data-stu-id="fa9f3-388">Creating a new virtual application package on the sequencer</span></span>

<span data-ttu-id="fa9f3-389">Если во время наблюдения Sequencer сборка SxS (например, среда выполнения VC + +) устанавливается как часть установки приложения, сборка SxS будет автоматически обнаружена и включена в пакет.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-389">If, during sequencer monitoring, an SxS Assembly (such as a VC++ Runtime) is installed as part of an application’s installation, SxS Assembly will be automatically detected and included in the package.</span></span> <span data-ttu-id="fa9f3-390">Администратор будет уведомлен и будет иметь возможность исключить сборку SxS.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-390">The administrator will be notified and will have the option to exclude the SxS Assembly.</span></span>

<span data-ttu-id="fa9f3-391">На **стороне клиента**:</span><span class="sxs-lookup"><span data-stu-id="fa9f3-391">**Client Side**:</span></span>

<span data-ttu-id="fa9f3-392">При публикации пакета виртуальных приложений клиент App-V 5,0 с пакетом обновления 2 (SP2) обнаружит, была ли уже установлена нужная зависимость SxS.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-392">When publishing a virtual application package, the App-V 5.0 SP2 Client will detect if a required SxS dependency is already installed.</span></span> <span data-ttu-id="fa9f3-393">Если зависимость недоступна на компьютере и включена в пакет, это традиционный установщик Windows (.\*\* MSI\*\*) будет инициирована установка сборки SxS.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-393">If the dependency is unavailable on the computer and it is included in the package, a traditional Windows Installer (.**msi**) installation of the SxS assembly will be initiated.</span></span> <span data-ttu-id="fa9f3-394">Как описано выше, установите зависимость на компьютере, на котором запущен клиент, чтобы убедиться, что установка установщика Windows (MSI) не будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-394">As previously documented, simply install the dependency on the computer running the client to ensure that the Windows Installer (.msi) installation will not occur.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa9f3-395">Шаг</span><span class="sxs-lookup"><span data-stu-id="fa9f3-395">Step</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-396">Довод</span><span class="sxs-lookup"><span data-stu-id="fa9f3-396">Considerations</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-397">Преимущества</span><span class="sxs-lookup"><span data-stu-id="fa9f3-397">Benefits</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-398">Необходимости компромиссов</span><span class="sxs-lookup"><span data-stu-id="fa9f3-398">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa9f3-399">Выборочно использовать динамические файлы конфигурации</span><span class="sxs-lookup"><span data-stu-id="fa9f3-399">Selectively Employ Dynamic Configuration files</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-400">Клиент App-V 5,0 должен проанализировать и обработать эти динамические файлы конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-400">The App-V 5.0 client must parse and process these Dynamic Configuration files.</span></span></p>
<p><span data-ttu-id="fa9f3-401">Следует понимать размер и сложность (выполнение сценария, включение и исключение VREG) файла.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-401">Be conscious of size and complexity (script execution, VREG inclusions/exclusions) of the file.</span></span></p>
<p><span data-ttu-id="fa9f3-402">В многочисленных виртуальных пакетах приложений может быть уже есть файлы динамических конфигураций, определенные пользователем или компьютером.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-402">Numerous virtual application packages may already have User- or computer–specific dynamic configurations files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-403">Во всех случаях, когда эти файлы используются выборочно или вообще не поддерживаются, будет улучшено количество публикаций.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-403">Publishing times will improve if these files are used selectively or not at all.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-404">Для удаления связанных динамических файлов конфигурации необходимо настроить виртуальные пакеты приложений по отдельности или с помощью консоли управления сервером App-V.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-404">Virtual application packages would need to be reconfigured individually or via the App-V server management console to remove associated Dynamic Configuration files.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="fa9f3-405">Отключение динамической конфигурации с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa9f3-405">Disabling a Dynamic Configuration using Powershell</span></span>

-   <span data-ttu-id="fa9f3-406">Если вы уже опубликовали пакеты, вы можете использовать его `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` без</span><span class="sxs-lookup"><span data-stu-id="fa9f3-406">For already published packages, you can use `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` without</span></span>

    <span data-ttu-id="fa9f3-407">Параметр **-DynamicDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="fa9f3-407">**-DynamicDeploymentConfiguration** parameter</span></span>

-   <span data-ttu-id="fa9f3-408">Аналогичным образом, при добавлении новых пакетов с помощью `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` , не используйте</span><span class="sxs-lookup"><span data-stu-id="fa9f3-408">Similarly, when adding new packages using `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv`, do not use the</span></span>

    <span data-ttu-id="fa9f3-409">Параметр **-DynamicDeploymentConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-409">**-DynamicDeploymentConfiguration** parameter.</span></span>

<span data-ttu-id="fa9f3-410">Документацию по применению динамической конфигурации можно найти в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="fa9f3-410">For documentation on How to Apply a Dynamic Configuration, see:</span></span>

-   [<span data-ttu-id="fa9f3-411">Применение файла конфигурации пользователя с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa9f3-411">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell.md)

-   [<span data-ttu-id="fa9f3-412">Применение файла конфигурации развертывания с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa9f3-412">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa9f3-413">Шаг</span><span class="sxs-lookup"><span data-stu-id="fa9f3-413">Step</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-414">Довод</span><span class="sxs-lookup"><span data-stu-id="fa9f3-414">Considerations</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-415">Преимущества</span><span class="sxs-lookup"><span data-stu-id="fa9f3-415">Benefits</span></span></th>
<th align="left"><span data-ttu-id="fa9f3-416">Необходимости компромиссов</span><span class="sxs-lookup"><span data-stu-id="fa9f3-416">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa9f3-417">Учетная запись для выполнения синхронного сценария в течение жизненного цикла пакета.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-417">Account for Synchronous Script Execution during Package Lifecycle.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-418">Если в пакет внедрена сопутствующие сценарии, то добавить (PowerShell) может быть значительно медленнее.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-418">If script collateral is embedded in the package, Add (Powershell) may be significantly slower.</span></span></p>
<p><span data-ttu-id="fa9f3-419">Выполнение сценариев во время запуска виртуальных приложений (StartVirtualEnvironment, StartProcess) и/или добавления + публикации может повлиять на воспринимаемую производительность во время одной или нескольких из этих операций жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-419">Running of scripts during virtual application launch (StartVirtualEnvironment, StartProcess) and/or Add+Publish will impact the perceived performance during one or more of these lifecycle operations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-420">Использование асинхронных сценариев (без блокировки) гарантирует эффективное выполнение операций жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-420">Use of Asynchronous (Non-Blocking) Scripts will ensure that the lifecycle operations complete efficiently.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-421">На этом этапе требуется получить сведения о всех виртуальных пакетах приложений со встроенными материалами, связанными с динамическими настройками, а затем ссылаться и выполнять сценарии синхронно.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-421">This step requires working knowledge of all virtual application packages with embedded script collateral, which have associated dynamic configurations files and which reference and run scripts synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa9f3-422">Удалите из пакета внешние виртуальные шрифты.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-422">Remove Extraneous Virtual Fonts from Package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-423">Большинство приложений, изучающих группу разработчиков App-V, содержало небольшое количество шрифтов, обычно менее 20.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-423">The majority of applications investigated by the App-V product team contained a small number of fonts, typically fewer than 20.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-424">Виртуальные шрифты влияют на производительность обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-424">Virtual Fonts impact publishing refresh performance.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa9f3-425">Нужные шрифты должны быть включены и установлены в исходном виде.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-425">Desired fonts will need to be enabled/installed natively.</span></span> <span data-ttu-id="fa9f3-426">Инструкции можно найти в разделе Установка и удаление шрифтов.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-426">For instructions, see Install or uninstall fonts.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="fa9f3-427">Определение того, какие виртуальные шрифты есть в пакете</span><span class="sxs-lookup"><span data-stu-id="fa9f3-427">Determining what virtual fonts exist in the package</span></span>

-   <span data-ttu-id="fa9f3-428">Сделайте копию пакета.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-428">Make a copy of the package.</span></span>

-   <span data-ttu-id="fa9f3-429">Переименование пакета \ _copy. AppV в Package\_copy.zip</span><span class="sxs-lookup"><span data-stu-id="fa9f3-429">Rename Package\_copy.appv to Package\_copy.zip</span></span>

-   <span data-ttu-id="fa9f3-430">Откройте AppxManifest.xml и найдите следующее:</span><span class="sxs-lookup"><span data-stu-id="fa9f3-430">Open AppxManifest.xml and locate the following:</span></span>

    <span data-ttu-id="fa9f3-431">&lt;AppV: Extension Category = "AppV. шрифты"&gt;</span><span class="sxs-lookup"><span data-stu-id="fa9f3-431">&lt;appv:Extension Category="AppV.Fonts"&gt;</span></span>

    <span data-ttu-id="fa9f3-432">&lt;AppV: шрифты&gt;</span><span class="sxs-lookup"><span data-stu-id="fa9f3-432">&lt;appv:Fonts&gt;</span></span>

    <span data-ttu-id="fa9f3-433">&lt;AppV: font Path = "\ [{шрифты} \] \\private\\CalibriL.ttf" DelayLoad = "истина" &gt; &lt; /AppV: font&gt;</span><span class="sxs-lookup"><span data-stu-id="fa9f3-433">&lt;appv:Font Path="\[{Fonts}\]\\private\\CalibriL.ttf" DelayLoad="true"&gt;&lt;/appv:Font&gt;</span></span>

    **<span data-ttu-id="fa9f3-434">Примечание.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-434">Note</span></span>**  
    <span data-ttu-id="fa9f3-435">Если у вас есть шрифты, помеченные как **DelayLoad**, то они не повлияют на первый запуск.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-435">If there are fonts marked as **DelayLoad**, those will not impact first launch.</span></span>



~~~
&lt;/appv:Fonts&gt;
~~~

### <span data-ttu-id="fa9f3-436">Исключение виртуальных шрифтов из пакета</span><span class="sxs-lookup"><span data-stu-id="fa9f3-436">Excluding virtual fonts from the package</span></span>

<span data-ttu-id="fa9f3-437">Используйте динамический файл конфигурации, который лучше всего подходит для области "область пользователя — Конфигурация развертывания" для всех пользователей на компьютере, Конфигурация пользователя для определенного пользователя или пользователей.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-437">Use the dynamic configuration file that best suits the user scope – deployment configuration for all users on computer, user configuration for specific user or users.</span></span>

-   <span data-ttu-id="fa9f3-438">Отключите шрифты с помощью развертывания или конфигурации пользователя.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-438">Disable fonts with the deployment or user configuration.</span></span>

<span data-ttu-id="fa9f3-439">Шрифты</span><span class="sxs-lookup"><span data-stu-id="fa9f3-439">Fonts</span></span>

--&gt;

<span data-ttu-id="fa9f3-440">&lt;Шрифты разрешены = "ложь"/&gt;</span><span class="sxs-lookup"><span data-stu-id="fa9f3-440">&lt;Fonts Enabled="false" /&gt;</span></span>

<span data-ttu-id="fa9f3-441">&lt;!--</span><span class="sxs-lookup"><span data-stu-id="fa9f3-441">&lt;!--</span></span>

## <a href="" id="bkmk-terms1"></a> <span data-ttu-id="fa9f3-442">Терминология руководства по производительности App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="fa9f3-442">App-V 5.0 Performance Guidance Terminology</span></span>


<span data-ttu-id="fa9f3-443">Следующие термины используются для описания концепций и действий, связанных с оптимизацией производительности App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-443">The following terms are used when describing concepts and actions related to App-V 5.0 performance optimization.</span></span>

-   <span data-ttu-id="fa9f3-444">**Сложность** — относится к одной или нескольким характеристикам пакета, которые могут повлиять на производительность при предварительной настройке (**Add-AppvClientPackage**) или интеграции (**Publish-AppvClientPackage**).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-444">**Complexity** – Refers to the one or more package characteristics that may impact performance during pre-configure (**Add-AppvClientPackage**) or integration (**Publish-AppvClientPackage**).</span></span> <span data-ttu-id="fa9f3-445">Ниже приведены некоторые примеры характеристик: Размер манифеста, количество виртуальных шрифтов, количество файлов.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-445">Some example characteristics are: manifest size, number of virtual fonts, number of files.</span></span>

-   <span data-ttu-id="fa9f3-446">**De-интеграция** — удаляет пользовательские интеграции.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-446">**De-Integrate** – Removes the user integrations</span></span>

-   <span data-ttu-id="fa9f3-447">После **повторной интеграции** применяются пользовательские интеграции.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-447">**Re-Integrate** – Applies the user integrations.</span></span>

-   <span data-ttu-id="fa9f3-448">**Непостоянные, в** составе пула — создает компьютер под управлением виртуальной среды при каждом входе.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-448">**Non-Persistent, Pooled** – Creates a computer running a virtual environment each time they log in.</span></span>

-   <span data-ttu-id="fa9f3-449">**Постоянный, персональный** — компьютер под управлением виртуальной среды, который остается одинаковым для каждой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-449">**Persistent, Personal** – A computer running a virtual environment that remains the same for every login.</span></span>

-   <span data-ttu-id="fa9f3-450">С **сохранением состояния** для этого документа означает, что интеграция пользователей сохраняется между сеансами, а технология управления средой пользователя используется совместно с несохраняемыми или одновременными сеансовми удаленных рабочих столов или VDI.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-450">**Stateful** - For this document, implies that user integrations are persisted between sessions and a user environment management technology is used in conjunction with non-persistent RDSH or VDI.</span></span>

-   <span data-ttu-id="fa9f3-451">Без **сведений о состоянии** — представляет сценарий, если состояние пользователя не сохраняется между сеансами.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-451">**Stateless** – Represents a scenario when no user state is persisted between sessions.</span></span>

-   <span data-ttu-id="fa9f3-452">**Триггер** – (или триггеры собственных действий).</span><span class="sxs-lookup"><span data-stu-id="fa9f3-452">**Trigger** – (or Native Action Triggers).</span></span> <span data-ttu-id="fa9f3-453">UPM использует эти типы триггеров для запуска наблюдения или операций синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-453">UPM uses these types of triggers to initiate monitoring or synchronization operations.</span></span>

-   <span data-ttu-id="fa9f3-454">**Взаимодействие с пользователем** : в контексте App-V 5,0, пользовательским интерфейсом является сумма следующих частей.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-454">**User Experience** - In the context of App-V 5.0, the user experience, quantitatively, is the sum of the following parts:</span></span>

    -   <span data-ttu-id="fa9f3-455">С той точки, на которую пользователи начинают вход, когда они смогут управлять рабочим столом.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-455">From the point that users initiate a log-in to when they are able to manipulate the desktop.</span></span>

    -   <span data-ttu-id="fa9f3-456">С точки зрения того, на котором можно взаимодействовать с рабочим столом в точке, начиная с которой начинается обновление публикации (в терминах PowerShell, синхронизация) при использовании полной серверной инфраструктуры App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-456">From the point where the desktop can be interacted with to the point a publishing refresh begins (in PowerShell terms, sync) when using the App-V 5.0 full server infrastructure.</span></span> <span data-ttu-id="fa9f3-457">В отдельных экземплярах инициировано создание команд PowerShell **Add-AppVClientPackage** и **Publish-AppVClientPackage** .</span><span class="sxs-lookup"><span data-stu-id="fa9f3-457">In standalone instances, it is when the **Add-AppVClientPackage** and **Publish-AppVClientPackage Powershell** commands are initiated.</span></span>

    -   <span data-ttu-id="fa9f3-458">От начала до завершения обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-458">From start to completion of the publishing refresh.</span></span> <span data-ttu-id="fa9f3-459">В автономных экземплярах это первое и последнее опубликованное виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-459">In standalone instances, this is the first to last virtual application published.</span></span>

    -   <span data-ttu-id="fa9f3-460">С того места, где виртуальное приложение доступно для запуска из ярлыка.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-460">From the point where the virtual application is available to launch from a shortcut.</span></span> <span data-ttu-id="fa9f3-461">Кроме того, это происходит с того места, в котором зарегистрирована Ассоциация типа файла, и запустится указанное виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-461">Alternatively, it is from the point at which the file type association is registered and will launch a specified virtual application.</span></span>

-   <span data-ttu-id="fa9f3-462">**Управление профилями пользователей** — управляемый и структурированный подход к управлению пользовательскими компонентами, связанными с этой средой.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-462">**User Profile Management** – The controlled and structured approach to managing user components associated with the environment.</span></span> <span data-ttu-id="fa9f3-463">Например, профили пользователей, настройки и управление политиками, элементы управления приложениями и развертывание приложений.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-463">For example, user profiles, preference and policy management, application control and application deployment.</span></span> <span data-ttu-id="fa9f3-464">Вы можете использовать сценарии или решения сторонних разработчиков для настройки среды по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="fa9f3-464">You can use scripting or third-party solutions configure the environment as needed.</span></span>






## <span data-ttu-id="fa9f3-465">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="fa9f3-465">Related topics</span></span>


[<span data-ttu-id="fa9f3-466">Руководство администратора Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="fa9f3-466">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)









