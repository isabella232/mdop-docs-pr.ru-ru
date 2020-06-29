---
title: Планирование использования App-V с Office
description: Планирование использования App-V с Office
author: dansimp
ms.assetid: c4371869-4bfc-4d13-9198-ef19f99fc192
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff523c8f8827e295c8fb9a2d9fd0e02d5b019aa8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813424"
---
# <span data-ttu-id="c461a-103">Планирование использования App-V с Office</span><span class="sxs-lookup"><span data-stu-id="c461a-103">Planning for Using App-V with Office</span></span>


<span data-ttu-id="c461a-104">Используйте следующие сведения, чтобы спланировать развертывание Office с помощью App-V.</span><span class="sxs-lookup"><span data-stu-id="c461a-104">Use the following information to plan how to deploy Office by using App-V.</span></span> <span data-ttu-id="c461a-105">В этой статье рассматриваются следующие статьи:</span><span class="sxs-lookup"><span data-stu-id="c461a-105">This article includes:</span></span>

-   [<span data-ttu-id="c461a-106">Поддержка языковых пакетов для App-V</span><span class="sxs-lookup"><span data-stu-id="c461a-106">App-V support for Language Packs</span></span>](#bkmk-lang-pack)

-   [<span data-ttu-id="c461a-107">Поддерживаемые версии Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="c461a-107">Supported versions of Microsoft Office</span></span>](#bkmk-office-vers-supp-appv)

-   [<span data-ttu-id="c461a-108">Планирование использования App-V с помощью косуществующих версий Office</span><span class="sxs-lookup"><span data-stu-id="c461a-108">Planning for using App-V with coexisting versions of Office</span></span>](#bkmk-plan-coexisting)

-   [<span data-ttu-id="c461a-109">Интеграция Office с Windows при развертывании Office с помощью App-V</span><span class="sxs-lookup"><span data-stu-id="c461a-109">How Office integrates with Windows when you deploy use App-V to deploy Office</span></span>](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a><span data-ttu-id="c461a-110">Поддержка языковых пакетов для App-V</span><span class="sxs-lookup"><span data-stu-id="c461a-110">App-V support for Language Packs</span></span>


<span data-ttu-id="c461a-111">С помощью секвенсора App-V 5,0 вы можете создавать пакеты для языков, языковых интерфейсов, средств проверки правописания и языков всплывающих подсказок.</span><span class="sxs-lookup"><span data-stu-id="c461a-111">You can use the App-V 5.0 Sequencer to create plug-in packages for Language Packs, Language Interface Packs, Proofing Tools and ScreenTip Languages.</span></span> <span data-ttu-id="c461a-112">Затем вы можете включить пакеты плагинов в группу соединения вместе с пакетом Office 2013, созданным с помощью набора средств развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="c461a-112">You can then include the plug-in packages in a Connection Group, along with the Office 2013 package that you create by using the Office Deployment Toolkit.</span></span> <span data-ttu-id="c461a-113">Приложения Office и языковые пакеты с поддержкой плагинов легко взаимодействуют в одной группе, так же как и любые другие пакеты, сгруппированные вместе в группу подключений.</span><span class="sxs-lookup"><span data-stu-id="c461a-113">The Office applications and the plug-in Language Packs interact seamlessly in the same connection group, just like any other packages that are grouped together in a connection group.</span></span>

<span data-ttu-id="c461a-114">**Примечание**  Microsoft Visio и Microsoft Project не предоставляют поддержку для языкового пакета на тайском языке.</span><span class="sxs-lookup"><span data-stu-id="c461a-114">**Note** Microsoft Visio and Microsoft Project do not provide support for the Thai Language Pack.</span></span>

 

## <a href="" id="bkmk-office-vers-supp-appv"></a><span data-ttu-id="c461a-115">Поддерживаемые версии Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="c461a-115">Supported versions of Microsoft Office</span></span>


<span data-ttu-id="c461a-116">В следующей таблице перечислены версии Microsoft Office, которые поддерживаются приложением App-V, методы создания пакетов Office, поддерживаемые лицензированные и поддерживаемые развертывания.</span><span class="sxs-lookup"><span data-stu-id="c461a-116">The following table lists the versions of Microsoft Office that App-V supports, methods of Office package creation, supported licensing, and supported deployments.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c461a-117">Поддерживаемая версия Office</span><span class="sxs-lookup"><span data-stu-id="c461a-117">Supported Office Version</span></span></th>
<th align="left"><span data-ttu-id="c461a-118">Поддерживаемые версии App-V</span><span class="sxs-lookup"><span data-stu-id="c461a-118">Supported App-V Versions</span></span></th>
<th align="left"><span data-ttu-id="c461a-119">Создание пакета</span><span class="sxs-lookup"><span data-stu-id="c461a-119">Package Creation</span></span></th>
<th align="left"><span data-ttu-id="c461a-120">Поддерживаемое лицензирование</span><span class="sxs-lookup"><span data-stu-id="c461a-120">Supported Licensing</span></span></th>
<th align="left"><span data-ttu-id="c461a-121">Поддерживаемые развертывания</span><span class="sxs-lookup"><span data-stu-id="c461a-121">Supported Deployments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c461a-122">Приложения Microsoft 365 для предприятий</span><span class="sxs-lookup"><span data-stu-id="c461a-122">Microsoft 365 Apps for enterprise</span></span></p>
<p><span data-ttu-id="c461a-123">Также поддерживаются следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="c461a-123">Also supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="c461a-124">Visio Pro для Office 365</span><span class="sxs-lookup"><span data-stu-id="c461a-124">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="c461a-125">Project Pro для Office 365</span><span class="sxs-lookup"><span data-stu-id="c461a-125">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c461a-126">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c461a-126">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="c461a-127">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c461a-127">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="c461a-128">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="c461a-128">App-V 5.0 SP2</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="c461a-129">Средство развертывания Office</span><span class="sxs-lookup"><span data-stu-id="c461a-129">Office Deployment Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-130">Подписка</span><span class="sxs-lookup"><span data-stu-id="c461a-130">Subscription</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c461a-131">Desktop</span><span class="sxs-lookup"><span data-stu-id="c461a-131">Desktop</span></span></p></li>
<li><p><span data-ttu-id="c461a-132">Персональный VDI</span><span class="sxs-lookup"><span data-stu-id="c461a-132">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="c461a-133">VDI из пула</span><span class="sxs-lookup"><span data-stu-id="c461a-133">Pooled VDI</span></span></p></li>
<li><p><span data-ttu-id="c461a-134">СЛУЖБ</span><span class="sxs-lookup"><span data-stu-id="c461a-134">RDS</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c461a-135">Office профессиональный плюс 2013</span><span class="sxs-lookup"><span data-stu-id="c461a-135">Office Professional Plus 2013</span></span></p>
<p><span data-ttu-id="c461a-136">Также поддерживаются следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="c461a-136">Also supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="c461a-137">Visio профессиональный 2013</span><span class="sxs-lookup"><span data-stu-id="c461a-137">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="c461a-138">Project профессиональный 2013</span><span class="sxs-lookup"><span data-stu-id="c461a-138">Project Professional 2013</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c461a-139">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c461a-139">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="c461a-140">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c461a-140">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="c461a-141">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="c461a-141">App-V 5.0 SP2</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="c461a-142">Средство развертывания Office</span><span class="sxs-lookup"><span data-stu-id="c461a-142">Office Deployment Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-143">Корпоративное лицензирование</span><span class="sxs-lookup"><span data-stu-id="c461a-143">Volume Licensing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c461a-144">Desktop</span><span class="sxs-lookup"><span data-stu-id="c461a-144">Desktop</span></span></p></li>
<li><p><span data-ttu-id="c461a-145">Персональный VDI</span><span class="sxs-lookup"><span data-stu-id="c461a-145">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="c461a-146">VDI из пула</span><span class="sxs-lookup"><span data-stu-id="c461a-146">Pooled VDI</span></span></p></li>
<li><p><span data-ttu-id="c461a-147">СЛУЖБ</span><span class="sxs-lookup"><span data-stu-id="c461a-147">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-plan-coexisting"></a><span data-ttu-id="c461a-148">Планирование использования App-V с помощью косуществующих версий Office</span><span class="sxs-lookup"><span data-stu-id="c461a-148">Planning for using App-V with coexisting versions of Office</span></span>


<span data-ttu-id="c461a-149">Вы можете установить более одной версии Microsoft Office на одном компьютере, используя "Microsoft Office сосуществование".</span><span class="sxs-lookup"><span data-stu-id="c461a-149">You can install more than one version of Microsoft Office side by side on the same computer by using “Microsoft Office coexistence.”</span></span> <span data-ttu-id="c461a-150">Вы можете реализовать сосуществование Office со всеми основными версиями Office и методами установки, как это применимо с помощью установщика Windows (MSi), технологии "нажми и работай" и App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="c461a-150">You can implement Office coexistence with combinations of all major versions of Office and with installation methods, as applicable, by using the Windows Installer-based (MSi) version of Office, Click-to-Run, and App-V 5.0 SP2.</span></span> <span data-ttu-id="c461a-151">Тем не менее использование сосуществования Office не рекомендуется корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c461a-151">However, using Office coexistence is not recommended by Microsoft.</span></span>

<span data-ttu-id="c461a-152">Рекомендуется не допустить проблем с совместимостью, но корпорация Майкрософт рекомендует избегать сосуществования Office полностью.</span><span class="sxs-lookup"><span data-stu-id="c461a-152">Microsoft’s recommended best practice is to avoid Office coexistence completely to prevent compatibility issues.</span></span> <span data-ttu-id="c461a-153">Однако при переходе на более новую версию Office иногда возникают проблемы, которые не удается устранить немедленно, поэтому вы можете временно реализовать сосуществование, чтобы упростить миграцию в последнюю версию продукта.</span><span class="sxs-lookup"><span data-stu-id="c461a-153">However, when you are migrating to a newer version of Office, issues occasionally arise that can’t be resolved immediately, so you can temporarily implement coexistence to help facilitate a faster migration to the latest product version.</span></span> <span data-ttu-id="c461a-154">Использование сосуществования Office на долгосрочной основе не рекомендуется, и ваша организация должна иметь план на полную смену в будущем.</span><span class="sxs-lookup"><span data-stu-id="c461a-154">Using Office coexistence on a long-term basis is never recommended, and your organization should have a plan to fully transition in the immediate future.</span></span>

### <span data-ttu-id="c461a-155">Перед реализацией сосуществования Office</span><span class="sxs-lookup"><span data-stu-id="c461a-155">Before you implement Office coexistence</span></span>

<span data-ttu-id="c461a-156">Перед реализацией сосуществования Office ознакомьтесь со следующей документацией по Office.</span><span class="sxs-lookup"><span data-stu-id="c461a-156">Before implementing Office coexistence, review the following Office documentation.</span></span> <span data-ttu-id="c461a-157">Выберите статью, соответствующую последней версии Office, для которой вы планируете реализовать сосуществование.</span><span class="sxs-lookup"><span data-stu-id="c461a-157">Choose the article that corresponds to the newest version of Office for which you plan to implement coexistence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c461a-158">Версия Office</span><span class="sxs-lookup"><span data-stu-id="c461a-158">Office version</span></span></th>
<th align="left"><span data-ttu-id="c461a-159">Ссылка на руководство</span><span class="sxs-lookup"><span data-stu-id="c461a-159">Link to guidance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c461a-160">Office 2013</span><span class="sxs-lookup"><span data-stu-id="c461a-160">Office 2013</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)"><span data-ttu-id="c461a-161">Сведения об использовании наборов и программ Office 2013 (развертывание MSI) на компьютере, на котором работает другая версия Office</span><span class="sxs-lookup"><span data-stu-id="c461a-161">Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c461a-162">Office 2010</span><span class="sxs-lookup"><span data-stu-id="c461a-162">Office 2010</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)"><span data-ttu-id="c461a-163">Сведения об использовании наборов и программ Office 2010 на компьютере под управлением другой версии Office</span><span class="sxs-lookup"><span data-stu-id="c461a-163">Information about how to use Office 2010 suites and programs on a computer that is running another version of Office</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c461a-164">Документация по Office содержит обширные рекомендации по сосуществованию установщика Windows (MSi) и установке Office нажми и работай.</span><span class="sxs-lookup"><span data-stu-id="c461a-164">The Office documentation provides extensive guidance on coexistence for Windows Installer-based (MSi) and Click-to-Run installations of Office.</span></span> <span data-ttu-id="c461a-165">Этот раздел App-V в сосуществовании дополняет Руководство по Office информацией, более специфичной для развертывания App-V.</span><span class="sxs-lookup"><span data-stu-id="c461a-165">This App-V topic on coexistence supplements the Office guidance with information that is more specific to App-V deployments.</span></span>

### <span data-ttu-id="c461a-166">Поддерживаемые сценарии сосуществования Office</span><span class="sxs-lookup"><span data-stu-id="c461a-166">Supported Office coexistence scenarios</span></span>

<span data-ttu-id="c461a-167">В приведенных ниже таблицах перечислены поддерживаемые сценарии сосуществования.</span><span class="sxs-lookup"><span data-stu-id="c461a-167">The following tables summarize the supported coexistence scenarios.</span></span> <span data-ttu-id="c461a-168">Они организованы в соответствии с версией и развертыванием, с которым вы работаете, и версией и методом развертывания, на которые вы мигрируют.</span><span class="sxs-lookup"><span data-stu-id="c461a-168">They are organized according to the version and deployment method you’re starting with and the version and deployment method you are migrating to.</span></span> <span data-ttu-id="c461a-169">Обязательно протестируйте все решения сосуществования перед развертыванием их в рабочую аудиторию.</span><span class="sxs-lookup"><span data-stu-id="c461a-169">Be sure to fully test all coexistence solutions before deploying them to a production audience.</span></span>

<span data-ttu-id="c461a-170">**Примечание**  Корпорация Microsoft не поддерживает использование нескольких версий Office в средах Windows Server, в которых включена служба роли узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c461a-170">**Note** Microsoft does not support the use of multiple versions of Office in Windows Server environments that have the Remote Desktop Session Host role service enabled.</span></span> <span data-ttu-id="c461a-171">Для запуска сценариев сосуществования Office необходимо отключить эту службу роли.</span><span class="sxs-lookup"><span data-stu-id="c461a-171">To run Office coexistence scenarios, you must disable this role service.</span></span>

 

### <span data-ttu-id="c461a-172">Интеграция с Windows & сосуществования Office</span><span class="sxs-lookup"><span data-stu-id="c461a-172">Windows integrations & Office coexistence</span></span>

<span data-ttu-id="c461a-173">Средства установки Office, созданные с помощью установщика Windows, интегрируются с определенными точками базовой операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="c461a-173">The Windows Installer-based and Click-to-Run Office installation methods integrate with certain points of the underlying Windows operating system.</span></span> <span data-ttu-id="c461a-174">При использовании сосуществования распространенная интеграция операционной системы между двумя версиями Office может привести к конфликтам, которые приводят к возникновению проблем с совместимостью и взаимодействии с пользователем.</span><span class="sxs-lookup"><span data-stu-id="c461a-174">When you use coexistence, common operating system integrations between two Office versions can conflict, causing compatibility and user experience issues.</span></span> <span data-ttu-id="c461a-175">С помощью App-V вы можете поочередно использовать определенные версии Office для исключения интеграции, тем самым "изолировать" их от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c461a-175">With App-V, you can sequence certain versions of Office to exclude integrations, thereby “isolating” them from the operating system.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="c461a-176">Режим, в котором App-V может поочередно последовательностей в этой версии Office</span><span class="sxs-lookup"><span data-stu-id="c461a-176">Mode in which App-V can sequence this version of Office</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c461a-177">Office 2007</span><span class="sxs-lookup"><span data-stu-id="c461a-177">Office 2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-178">Всегда не интегрированы.</span><span class="sxs-lookup"><span data-stu-id="c461a-178">Always non-integrated.</span></span> <span data-ttu-id="c461a-179">Приложение App-V не предлагает интеграции операционной системы с виртуализированной версией Office 2007.</span><span class="sxs-lookup"><span data-stu-id="c461a-179">App-V does not offer any operating system integrations with a virtualized version of Office 2007.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c461a-180">Office 2010</span><span class="sxs-lookup"><span data-stu-id="c461a-180">Office 2010</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-181">Интегрированный и не интегрированный режим.</span><span class="sxs-lookup"><span data-stu-id="c461a-181">Integrated and non-integrated mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c461a-182">Office 2013</span><span class="sxs-lookup"><span data-stu-id="c461a-182">Office 2013</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-183">Всегда интегрируются.</span><span class="sxs-lookup"><span data-stu-id="c461a-183">Always integrated.</span></span> <span data-ttu-id="c461a-184">Интеграция с операционной системой Windows не может быть отключена.</span><span class="sxs-lookup"><span data-stu-id="c461a-184">Windows operating system integrations cannot be disabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c461a-185">Корпорация Microsoft рекомендует развертывать сосуществование Office только с помощью одного из встроенных экземпляров Office.</span><span class="sxs-lookup"><span data-stu-id="c461a-185">Microsoft recommends that you deploy Office coexistence with only one integrated Office instance.</span></span> <span data-ttu-id="c461a-186">Например, если вы используете App-V для развертывания Office 2010 и Office 2013, вы должны поочередно использовать Office 2010 в неинтегрированном режиме.</span><span class="sxs-lookup"><span data-stu-id="c461a-186">For example, if you’re using App-V to deploy Office 2010 and Office 2013, you should sequence Office 2010 in non-integrated mode.</span></span> <span data-ttu-id="c461a-187">Дополнительные сведения о том, как последовательное использование Office в режиме без интеграции (изолированном), описаны в разделе [как пошаговые инструкции для Microsoft Office 2010 в Microsoft Application Virtualization 5,0](https://support.microsoft.com/kb/2830069).</span><span class="sxs-lookup"><span data-stu-id="c461a-187">For more information about sequencing Office in non-integration (isolated) mode, see [How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0](https://support.microsoft.com/kb/2830069).</span></span>

### <span data-ttu-id="c461a-188">Известные ограничения сценариев сосуществования Office</span><span class="sxs-lookup"><span data-stu-id="c461a-188">Known limitations of Office coexistence scenarios</span></span>

<span data-ttu-id="c461a-189">В следующих разделах описаны некоторые проблемы, которые могут возникнуть при использовании App-V для реализации сосуществования с помощью Office.</span><span class="sxs-lookup"><span data-stu-id="c461a-189">The following sections describe some issues that you might encounter when using App-V to implement coexistence with Office.</span></span>

### <span data-ttu-id="c461a-190">Ограничения, характерные для сценариев совместного существования с помощью установщика Windows, а затем — для выполнения и App-V.</span><span class="sxs-lookup"><span data-stu-id="c461a-190">Limitations common to Windows Installer-based/Click-to-Run and App-V Office coexistence scenarios</span></span>

<span data-ttu-id="c461a-191">При установке следующих версий Office на одном компьютере могут возникать указанные ниже ограничения.</span><span class="sxs-lookup"><span data-stu-id="c461a-191">The following limitations can occur when you install the following versions of Office on the same computer:</span></span>

-   <span data-ttu-id="c461a-192">Office 2010 с помощью установщика Windows</span><span class="sxs-lookup"><span data-stu-id="c461a-192">Office 2010 by using the Windows Installer-based version</span></span>

-   <span data-ttu-id="c461a-193">Office 2013 с помощью App-V</span><span class="sxs-lookup"><span data-stu-id="c461a-193">Office 2013 by using App-V</span></span>

<span data-ttu-id="c461a-194">После публикации Office 2013 с помощью приложения-V рядом с более ранней версией 2010 Office, основанной на установщике Windows, может также быть запуск установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="c461a-194">After you publish Office 2013 by using App-V side by side with an earlier version of the Windows Installer-based Office 2010 might also cause the Windows Installer to start.</span></span> <span data-ttu-id="c461a-195">Это происходит из-за того, что версия Office 2010, основанная на установщиках Windows или "нажми и работай", пытается автоматически зарегистрироваться на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c461a-195">This is because the Windows Installer-based or Click-to-Run version of Office 2010 is trying to automatically register itself to the computer.</span></span>

<span data-ttu-id="c461a-196">Чтобы отключить автоматическую регистрацию для приложения Word 2010, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c461a-196">To bypass the auto-registration operation for native Word 2010, follow these steps:</span></span>

1.  <span data-ttu-id="c461a-197">Закройте приложение Word 2010.</span><span class="sxs-lookup"><span data-stu-id="c461a-197">Exit Word 2010.</span></span>

2.  <span data-ttu-id="c461a-198">Запустите редактор реестра, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c461a-198">Start the Registry Editor by doing the following:</span></span>

    -   <span data-ttu-id="c461a-199">В Windows 7: нажмите кнопку **Пуск**, введите **regedit** в поле начать поиск и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="c461a-199">In Windows 7: Click **Start**, type **regedit** in the Start Search box, and then press Enter.</span></span>

    -   <span data-ttu-id="c461a-200">В Windows 8 введите **regedit** нажмите клавишу ВВОД на начальной странице и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="c461a-200">In Windows 8, type **regedit** press Enter on the Start page and then press Enter.</span></span>

    <span data-ttu-id="c461a-201">Если вам будет предложено ввести пароль администратора или подтверждение, введите пароль или нажмите кнопку **продолжить**.</span><span class="sxs-lookup"><span data-stu-id="c461a-201">If you are prompted for an administrator password or for a confirmation, type the password, or click **Continue**.</span></span>

3.  <span data-ttu-id="c461a-202">Найдите и выделите следующий подраздел реестра:</span><span class="sxs-lookup"><span data-stu-id="c461a-202">Locate and then select the following registry subkey:</span></span>

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  <span data-ttu-id="c461a-203">В меню **Правка** выберите пункт **создать**, а затем — параметр **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="c461a-203">On the **Edit** menu, click **New**, and then click **DWORD Value**.</span></span>

5.  <span data-ttu-id="c461a-204">Введите **NoReReg**и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="c461a-204">Type **NoReReg**, and then press Enter.</span></span>

6.  <span data-ttu-id="c461a-205">Щелкните правой кнопкой мыши **NoReReg** и выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="c461a-205">Right-click **NoReReg** and then click **Modify**.</span></span>

7.  <span data-ttu-id="c461a-206">В поле **Valuedata** введите **1**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c461a-206">In the **Valuedata** box, type **1**, and then click **OK**.</span></span>

8.  <span data-ttu-id="c461a-207">В меню Файл выберите команду **выход** , чтобы закрыть редактор реестра.</span><span class="sxs-lookup"><span data-stu-id="c461a-207">On the File menu, click **Exit** to close Registry Editor.</span></span>

## <a href="" id="bkmk-office-integration-win"></a><span data-ttu-id="c461a-208">Интеграция Office с Windows с помощью App-V для развертывания Office</span><span class="sxs-lookup"><span data-stu-id="c461a-208">How Office integrates with Windows when you use App-V to deploy Office</span></span>


<span data-ttu-id="c461a-209">При развертывании Office 2013 с помощью App-V Office полностью интегрируется с операционной системой, которая обеспечивает конечным пользователям те же функции и функциональность, что и в Office, если он развернут без App-V.</span><span class="sxs-lookup"><span data-stu-id="c461a-209">When you deploy Office 2013 by using App-V, Office is fully integrated with the operating system, which provides end users with the same features and functionality as Office has when it is deployed without App-V.</span></span>

<span data-ttu-id="c461a-210">Пакет App-V для Office 2013 поддерживает следующие точки интеграции с операционной системой Windows:</span><span class="sxs-lookup"><span data-stu-id="c461a-210">The Office 2013 App-V package supports the following integration points with the Windows operating system:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c461a-211">Точка расширения</span><span class="sxs-lookup"><span data-stu-id="c461a-211">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="c461a-212">Описание</span><span class="sxs-lookup"><span data-stu-id="c461a-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c461a-213">Плагин присоединения к собранию Lync для Firefox и Chrome</span><span class="sxs-lookup"><span data-stu-id="c461a-213">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-214">Пользователь может присоединиться к собраниям Lync из Firefox и Chrome</span><span class="sxs-lookup"><span data-stu-id="c461a-214">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c461a-215">Отправлено в драйвер печати OneNote</span><span class="sxs-lookup"><span data-stu-id="c461a-215">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-216">Пользователь может печатать в OneNote</span><span class="sxs-lookup"><span data-stu-id="c461a-216">User can print to OneNote</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c461a-217">Связанные заметки OneNote</span><span class="sxs-lookup"><span data-stu-id="c461a-217">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-218">Связанные заметки OneNote</span><span class="sxs-lookup"><span data-stu-id="c461a-218">OneNote Linked Notes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c461a-219">Надстройка "отправить в OneNote" в Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c461a-219">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-220">Пользователь может отправлять сообщения в OneNote из браузера Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c461a-220">User can send to OneNote from IE</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c461a-221">Исключение брандмауэра для Lync и Outlook</span><span class="sxs-lookup"><span data-stu-id="c461a-221">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-222">Исключение брандмауэра для Lync и Outlook</span><span class="sxs-lookup"><span data-stu-id="c461a-222">Firewall Exception for Lync and Outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c461a-223">Клиент MAPI</span><span class="sxs-lookup"><span data-stu-id="c461a-223">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-224">Встроенные приложения и надстройки могут взаимодействовать с виртуальным приложением Outlook через MAPI</span><span class="sxs-lookup"><span data-stu-id="c461a-224">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c461a-225">Надстройка SharePoint для Firefox</span><span class="sxs-lookup"><span data-stu-id="c461a-225">SharePoint Plug-in for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-226">Пользователь может использовать возможности SharePoint в Firefox</span><span class="sxs-lookup"><span data-stu-id="c461a-226">User can use SharePoint features in Firefox</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c461a-227">Приложение панели управления "почта"</span><span class="sxs-lookup"><span data-stu-id="c461a-227">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-228">Пользователь получает панель управления "почта" в Outlook</span><span class="sxs-lookup"><span data-stu-id="c461a-228">User gets the mail control panel applet in Outlook</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c461a-229">Основные сборки взаимодействия</span><span class="sxs-lookup"><span data-stu-id="c461a-229">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-230">Поддержка управляемых надстроек</span><span class="sxs-lookup"><span data-stu-id="c461a-230">Support managed add-ins</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c461a-231">Обработчик кэша документов Office</span><span class="sxs-lookup"><span data-stu-id="c461a-231">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-232">Разрешение кэша документов для приложений Office</span><span class="sxs-lookup"><span data-stu-id="c461a-232">Allows Document Cache for Office applications</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c461a-233">Обработчик поиска протоколов Outlook</span><span class="sxs-lookup"><span data-stu-id="c461a-233">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-234">Пользователь может выполнять поиск в Outlook</span><span class="sxs-lookup"><span data-stu-id="c461a-234">User can search in outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c461a-235">Элементы управления ActiveX:</span><span class="sxs-lookup"><span data-stu-id="c461a-235">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-236">Дополнительные сведения об элементах ActiveX можно найти в <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> справочнике API элементов ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="c461a-236">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c461a-237">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="c461a-237">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-238">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-238">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c461a-239">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="c461a-239">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-240">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-240">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c461a-241">SharePoint. openDocument</span><span class="sxs-lookup"><span data-stu-id="c461a-241">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-242">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-242">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c461a-243">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="c461a-243">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-244">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-244">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c461a-245">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="c461a-245">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-246">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-246">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c461a-247">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="c461a-247">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-248">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-248">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c461a-249">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="c461a-249">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-250">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-250">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c461a-251">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="c461a-251">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-252">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-252">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c461a-253">SharePoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="c461a-253">Sharepoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-254">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-254">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c461a-255">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="c461a-255">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-256">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-256">Active X control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c461a-257">WinProj. активатор</span><span class="sxs-lookup"><span data-stu-id="c461a-257">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-258">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-258">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c461a-259">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="c461a-259">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-260">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-260">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c461a-261">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="c461a-261">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-262">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-262">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c461a-263">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="c461a-263">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-264">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-264">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c461a-265">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="c461a-265">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-266">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="c461a-266">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c461a-267">Вспомогательное приложение браузера OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="c461a-267">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-268">Элемент управления ActiveX]</span><span class="sxs-lookup"><span data-stu-id="c461a-268">Active X Control]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c461a-269">Наложения значков OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="c461a-269">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="c461a-270">Перекрытие значков оболочки в проводнике Windows при просмотре папок в папках OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="c461a-270">Windows Explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c461a-271">Расширения оболочки</span><span class="sxs-lookup"><span data-stu-id="c461a-271">Shell extensions</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c461a-272">Горячие</span><span class="sxs-lookup"><span data-stu-id="c461a-272">Shortcuts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c461a-273">Windows Search</span><span class="sxs-lookup"><span data-stu-id="c461a-273">Windows Search</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





