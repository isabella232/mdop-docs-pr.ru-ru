---
title: Планирование использования App-V с Office
description: Планирование использования App-V с Office
author: dansimp
ms.assetid: e7a19b43-1746-469f-bad6-8e75cf4b3f67
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/16/2017
ms.openlocfilehash: ae225db3c47faca5fba790fb9963bfd4dc2c66b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813413"
---
# <span data-ttu-id="9bf9c-103">Планирование использования App-V с Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-103">Planning for Using App-V with Office</span></span>


<span data-ttu-id="9bf9c-104">Чтобы спланировать развертывание Office с помощью Microsoft Application Virtualization (App-V) 5,1, воспользуйтесь приведенными ниже сведениями.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-104">Use the following information to plan how to deploy Office by using Microsoft Application Virtualization (App-V) 5.1.</span></span> <span data-ttu-id="9bf9c-105">В этой статье рассматриваются следующие статьи:</span><span class="sxs-lookup"><span data-stu-id="9bf9c-105">This article includes:</span></span>

-   [<span data-ttu-id="9bf9c-106">Поддержка языковых пакетов для App-V</span><span class="sxs-lookup"><span data-stu-id="9bf9c-106">App-V support for Language Packs</span></span>](#bkmk-lang-pack)

-   [<span data-ttu-id="9bf9c-107">Поддерживаемые версии Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-107">Supported versions of Microsoft Office</span></span>](#bkmk-office-vers-supp-appv)

-   [<span data-ttu-id="9bf9c-108">Планирование использования App-V с помощью косуществующих версий Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-108">Planning for using App-V with coexisting versions of Office</span></span>](#bkmk-plan-coexisting)

-   [<span data-ttu-id="9bf9c-109">Интеграция Office с Windows при развертывании Office с помощью App-V</span><span class="sxs-lookup"><span data-stu-id="9bf9c-109">How Office integrates with Windows when you deploy use App-V to deploy Office</span></span>](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a><span data-ttu-id="9bf9c-110">Поддержка языковых пакетов для App-V</span><span class="sxs-lookup"><span data-stu-id="9bf9c-110">App-V support for Language Packs</span></span>


<span data-ttu-id="9bf9c-111">С помощью секвенсора App-V 5,1 вы можете создавать пакеты для языков, языковых интерфейсов, средств проверки правописания и языков всплывающих подсказок.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-111">You can use the App-V 5.1 Sequencer to create plug-in packages for Language Packs, Language Interface Packs, Proofing Tools and ScreenTip Languages.</span></span> <span data-ttu-id="9bf9c-112">Затем вы можете включить пакеты плагинов в группу соединения вместе с пакетом Office 2013, созданным с помощью набора средств развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-112">You can then include the plug-in packages in a Connection Group, along with the Office 2013 package that you create by using the Office Deployment Toolkit.</span></span> <span data-ttu-id="9bf9c-113">Приложения Office и языковые пакеты с поддержкой плагинов легко взаимодействуют в одной группе, так же как и любые другие пакеты, сгруппированные вместе в группу подключений.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-113">The Office applications and the plug-in Language Packs interact seamlessly in the same connection group, just like any other packages that are grouped together in a connection group.</span></span>

><span data-ttu-id="9bf9c-114">**Примечание**  Microsoft Visio и Microsoft Project не предоставляют поддержку для языкового пакета на тайском языке.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-114">**Note** Microsoft Visio and Microsoft Project do not provide support for the Thai Language Pack.</span></span>

 

## <a href="" id="bkmk-office-vers-supp-appv"></a><span data-ttu-id="9bf9c-115">Поддерживаемые версии Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-115">Supported versions of Microsoft Office</span></span>

<span data-ttu-id="9bf9c-116">Ознакомьтесь с [идентификаторами продуктов Microsoft Office, которые поддерживаются приложением App-V,](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) для получения списка поддерживаемых продуктов Office.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-116">See [Microsoft Office Product IDs that App-V supports](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) for a list of supported Office products.</span></span>
><span data-ttu-id="9bf9c-117">**Note** &nbsp; Примечание &nbsp; Для создания пакетов App-V для приложений Microsoft 365 для предприятий необходимо использовать средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-117">**Note**&nbsp;&nbsp;You must use the Office Deployment Tool to create App-V packages for Microsoft 365 Apps for enterprise.</span></span> <span data-ttu-id="9bf9c-118">Создание пакетов для версий Office профессиональный плюс и Office Стандартный, лицензированных для корпоративных лицензий, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-118">Creating packages for the volume-licensed versions of Office Professional Plus or Office Standard is not supported.</span></span> <span data-ttu-id="9bf9c-119">Нельзя использовать секвенсор App-V.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-119">You cannot use the App-V Sequencer.</span></span>

 

## <a href="" id="bkmk-plan-coexisting"></a><span data-ttu-id="9bf9c-120">Планирование использования App-V с помощью косуществующих версий Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-120">Planning for using App-V with coexisting versions of Office</span></span>


<span data-ttu-id="9bf9c-121">Вы можете установить более одной версии Microsoft Office на одном компьютере, используя "Microsoft Office сосуществование".</span><span class="sxs-lookup"><span data-stu-id="9bf9c-121">You can install more than one version of Microsoft Office side by side on the same computer by using “Microsoft Office coexistence.”</span></span> <span data-ttu-id="9bf9c-122">Вы можете реализовать сосуществование Office со всеми основными версиями Office и методами установки, как это применимо с помощью установщика Windows (MSi), технологии "нажми и работай" и App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-122">You can implement Office coexistence with combinations of all major versions of Office and with installation methods, as applicable, by using the Windows Installer-based (MSi) version of Office, Click-to-Run, and App-V 5.1.</span></span> <span data-ttu-id="9bf9c-123">Тем не менее использование сосуществования Office не рекомендуется корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-123">However, using Office coexistence is not recommended by Microsoft.</span></span>

<span data-ttu-id="9bf9c-124">Рекомендуется не допустить проблем с совместимостью, но корпорация Майкрософт рекомендует избегать сосуществования Office полностью.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-124">Microsoft’s recommended best practice is to avoid Office coexistence completely to prevent compatibility issues.</span></span> <span data-ttu-id="9bf9c-125">Однако при переходе на более новую версию Office иногда возникают проблемы, которые не удается устранить немедленно, поэтому вы можете временно реализовать сосуществование, чтобы упростить миграцию в последнюю версию продукта.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-125">However, when you are migrating to a newer version of Office, issues occasionally arise that can’t be resolved immediately, so you can temporarily implement coexistence to help facilitate a faster migration to the latest product version.</span></span> <span data-ttu-id="9bf9c-126">Использование сосуществования Office на долгосрочной основе не рекомендуется, и ваша организация должна иметь план на полную смену в будущем.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-126">Using Office coexistence on a long-term basis is never recommended, and your organization should have a plan to fully transition in the immediate future.</span></span>

### <span data-ttu-id="9bf9c-127">Перед реализацией сосуществования Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-127">Before you implement Office coexistence</span></span>

<span data-ttu-id="9bf9c-128">Перед реализацией сосуществования Office ознакомьтесь со следующей документацией по Office.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-128">Before implementing Office coexistence, review the following Office documentation.</span></span> <span data-ttu-id="9bf9c-129">Выберите статью, соответствующую последней версии Office, для которой вы планируете реализовать сосуществование.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-129">Choose the article that corresponds to the newest version of Office for which you plan to implement coexistence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9bf9c-130">Версия Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-130">Office version</span></span></th>
<th align="left"><span data-ttu-id="9bf9c-131">Ссылка на руководство</span><span class="sxs-lookup"><span data-stu-id="9bf9c-131">Link to guidance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bf9c-132">Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bf9c-132">Office 2013</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)"><span data-ttu-id="9bf9c-133">Сведения об использовании наборов и программ Office 2013 (развертывание MSI) на компьютере, на котором работает другая версия Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-133">Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bf9c-134">Office 2010</span><span class="sxs-lookup"><span data-stu-id="9bf9c-134">Office 2010</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)"><span data-ttu-id="9bf9c-135">Сведения об использовании наборов и программ Office 2010 на компьютере под управлением другой версии Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-135">Information about how to use Office 2010 suites and programs on a computer that is running another version of Office</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9bf9c-136">Документация по Office содержит обширные рекомендации по сосуществованию установщика Windows (MSi) и установке Office нажми и работай.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-136">The Office documentation provides extensive guidance on coexistence for Windows Installer-based (MSi) and Click-to-Run installations of Office.</span></span> <span data-ttu-id="9bf9c-137">Этот раздел App-V в сосуществовании дополняет Руководство по Office информацией, более специфичной для развертывания App-V.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-137">This App-V topic on coexistence supplements the Office guidance with information that is more specific to App-V deployments.</span></span>

### <span data-ttu-id="9bf9c-138">Поддерживаемые сценарии сосуществования Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-138">Supported Office coexistence scenarios</span></span>

<span data-ttu-id="9bf9c-139">В приведенных ниже таблицах перечислены поддерживаемые сценарии сосуществования.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-139">The following tables summarize the supported coexistence scenarios.</span></span> <span data-ttu-id="9bf9c-140">Они организованы в соответствии с версией и развертыванием, с которым вы работаете, и версией и методом развертывания, на которые вы мигрируют.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-140">They are organized according to the version and deployment method you’re starting with and the version and deployment method you are migrating to.</span></span> <span data-ttu-id="9bf9c-141">Обязательно протестируйте все решения сосуществования перед развертыванием их в рабочую аудиторию.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-141">Be sure to fully test all coexistence solutions before deploying them to a production audience.</span></span>

><span data-ttu-id="9bf9c-142">**Примечание**  Корпорация Microsoft не поддерживает использование нескольких версий Office в средах Windows Server, в которых включена служба роли узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-142">**Note** Microsoft does not support the use of multiple versions of Office in Windows Server environments that have the Remote Desktop Session Host role service enabled.</span></span> <span data-ttu-id="9bf9c-143">Для запуска сценариев сосуществования Office необходимо отключить эту службу роли.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-143">To run Office coexistence scenarios, you must disable this role service.</span></span>

 

### <span data-ttu-id="9bf9c-144">Интеграция с Windows & сосуществования Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-144">Windows integrations & Office coexistence</span></span>

<span data-ttu-id="9bf9c-145">Средства установки Office, созданные с помощью установщика Windows, интегрируются с определенными точками базовой операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-145">The Windows Installer-based and Click-to-Run Office installation methods integrate with certain points of the underlying Windows operating system.</span></span> <span data-ttu-id="9bf9c-146">При использовании сосуществования распространенная интеграция операционной системы между двумя версиями Office может привести к конфликтам, которые приводят к возникновению проблем с совместимостью и взаимодействии с пользователем.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-146">When you use coexistence, common operating system integrations between two Office versions can conflict, causing compatibility and user experience issues.</span></span> <span data-ttu-id="9bf9c-147">С помощью App-V вы можете поочередно использовать определенные версии Office для исключения интеграции, тем самым "изолировать" их от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-147">With App-V, you can sequence certain versions of Office to exclude integrations, thereby “isolating” them from the operating system.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="9bf9c-148">Режим, в котором App-V может поочередно последовательностей в этой версии Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-148">Mode in which App-V can sequence this version of Office</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bf9c-149">Office 2007</span><span class="sxs-lookup"><span data-stu-id="9bf9c-149">Office 2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-150">Всегда не интегрированы.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-150">Always non-integrated.</span></span> <span data-ttu-id="9bf9c-151">Приложение App-V не предлагает интеграции операционной системы с виртуализированной версией Office 2007.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-151">App-V does not offer any operating system integrations with a virtualized version of Office 2007.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bf9c-152">Office 2010</span><span class="sxs-lookup"><span data-stu-id="9bf9c-152">Office 2010</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-153">Интегрированный и не интегрированный режим.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-153">Integrated and non-integrated mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bf9c-154">Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bf9c-154">Office 2013</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-155">Всегда интегрируются.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-155">Always integrated.</span></span> <span data-ttu-id="9bf9c-156">Интеграция с операционной системой Windows не может быть отключена.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-156">Windows operating system integrations cannot be disabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9bf9c-157">Корпорация Microsoft рекомендует развертывать сосуществование Office только с помощью одного из встроенных экземпляров Office.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-157">Microsoft recommends that you deploy Office coexistence with only one integrated Office instance.</span></span> <span data-ttu-id="9bf9c-158">Например, если вы используете App-V для развертывания Office 2010 и Office 2013, вы должны поочередно использовать Office 2010 в неинтегрированном режиме.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-158">For example, if you’re using App-V to deploy Office 2010 and Office 2013, you should sequence Office 2010 in non-integrated mode.</span></span> <span data-ttu-id="9bf9c-159">Дополнительные сведения о том, как последовательное использование Office в режиме без интеграции (изолированном), описаны в разделе [как пошаговые инструкции для Microsoft Office 2010 в Microsoft Application Virtualization 5,0](https://support.microsoft.com/kb/2830069).</span><span class="sxs-lookup"><span data-stu-id="9bf9c-159">For more information about sequencing Office in non-integration (isolated) mode, see [How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0](https://support.microsoft.com/kb/2830069).</span></span>

### <span data-ttu-id="9bf9c-160">Известные ограничения сценариев сосуществования Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-160">Known limitations of Office coexistence scenarios</span></span>

<span data-ttu-id="9bf9c-161">В следующих разделах описаны некоторые проблемы, которые могут возникнуть при использовании App-V для реализации сосуществования с помощью Office.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-161">The following sections describe some issues that you might encounter when using App-V to implement coexistence with Office.</span></span>

### <span data-ttu-id="9bf9c-162">Ограничения, характерные для сценариев совместного существования с помощью установщика Windows, а затем — для выполнения и App-V.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-162">Limitations common to Windows Installer-based/Click-to-Run and App-V Office coexistence scenarios</span></span>

<span data-ttu-id="9bf9c-163">При установке следующих версий Office на одном компьютере могут возникать указанные ниже ограничения.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-163">The following limitations can occur when you install the following versions of Office on the same computer:</span></span>

-   <span data-ttu-id="9bf9c-164">Office 2010 с помощью установщика Windows</span><span class="sxs-lookup"><span data-stu-id="9bf9c-164">Office 2010 by using the Windows Installer-based version</span></span>

-   <span data-ttu-id="9bf9c-165">Office 2013 с помощью App-V</span><span class="sxs-lookup"><span data-stu-id="9bf9c-165">Office 2013 by using App-V</span></span>

<span data-ttu-id="9bf9c-166">После публикации Office 2013 с помощью приложения-V рядом с более ранней версией 2010 Office, основанной на установщике Windows, может также быть запуск установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-166">After you publish Office 2013 by using App-V side by side with an earlier version of the Windows Installer-based Office 2010 might also cause the Windows Installer to start.</span></span> <span data-ttu-id="9bf9c-167">Это происходит из-за того, что версия Office 2010, основанная на установщиках Windows или "нажми и работай", пытается автоматически зарегистрироваться на компьютере.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-167">This is because the Windows Installer-based or Click-to-Run version of Office 2010 is trying to automatically register itself to the computer.</span></span>

<span data-ttu-id="9bf9c-168">Чтобы отключить автоматическую регистрацию для приложения Word 2010, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-168">To bypass the auto-registration operation for native Word 2010, follow these steps:</span></span>

1.  <span data-ttu-id="9bf9c-169">Закройте приложение Word 2010.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-169">Exit Word 2010.</span></span>

2.  <span data-ttu-id="9bf9c-170">Запустите редактор реестра, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-170">Start the Registry Editor by doing the following:</span></span>

    -   <span data-ttu-id="9bf9c-171">В Windows 7: нажмите кнопку **Пуск**, введите **regedit** в поле начать поиск и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-171">In Windows 7: Click **Start**, type **regedit** in the Start Search box, and then press Enter.</span></span>

    -   <span data-ttu-id="9bf9c-172">В Windows 8,1 или Windows 10 введите **regedit** нажмите клавишу ВВОД на начальной странице и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-172">In Windows 8.1 or Windows 10, type **regedit** press Enter on the Start page and then press Enter.</span></span>

    <span data-ttu-id="9bf9c-173">Если вам будет предложено ввести пароль администратора или подтверждение, введите пароль или нажмите кнопку **продолжить**.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-173">If you are prompted for an administrator password or for a confirmation, type the password, or click **Continue**.</span></span>

3.  <span data-ttu-id="9bf9c-174">Найдите и выделите следующий подраздел реестра:</span><span class="sxs-lookup"><span data-stu-id="9bf9c-174">Locate and then select the following registry subkey:</span></span>

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  <span data-ttu-id="9bf9c-175">В меню **Правка** выберите пункт **создать**, а затем — параметр **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-175">On the **Edit** menu, click **New**, and then click **DWORD Value**.</span></span>

5.  <span data-ttu-id="9bf9c-176">Введите **NoReReg**и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-176">Type **NoReReg**, and then press Enter.</span></span>

6.  <span data-ttu-id="9bf9c-177">Щелкните правой кнопкой мыши **NoReReg** и выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-177">Right-click **NoReReg** and then click **Modify**.</span></span>

7.  <span data-ttu-id="9bf9c-178">В поле **Valuedata** введите **1**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-178">In the **Valuedata** box, type **1**, and then click **OK**.</span></span>

8.  <span data-ttu-id="9bf9c-179">В меню Файл выберите команду **выход** , чтобы закрыть редактор реестра.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-179">On the File menu, click **Exit** to close Registry Editor.</span></span>

## <a href="" id="bkmk-office-integration-win"></a><span data-ttu-id="9bf9c-180">Интеграция Office с Windows с помощью App-V для развертывания Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-180">How Office integrates with Windows when you use App-V to deploy Office</span></span>


<span data-ttu-id="9bf9c-181">При развертывании Office 2013 с помощью App-V Office полностью интегрируется с операционной системой, которая обеспечивает конечным пользователям те же функции и функциональность, что и в Office, если он развернут без App-V.</span><span class="sxs-lookup"><span data-stu-id="9bf9c-181">When you deploy Office 2013 by using App-V, Office is fully integrated with the operating system, which provides end users with the same features and functionality as Office has when it is deployed without App-V.</span></span>

<span data-ttu-id="9bf9c-182">Пакет App-V для Office 2013 поддерживает следующие точки интеграции с операционной системой Windows:</span><span class="sxs-lookup"><span data-stu-id="9bf9c-182">The Office 2013 App-V package supports the following integration points with the Windows operating system:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9bf9c-183">Точка расширения</span><span class="sxs-lookup"><span data-stu-id="9bf9c-183">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="9bf9c-184">Описание</span><span class="sxs-lookup"><span data-stu-id="9bf9c-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bf9c-185">Плагин присоединения к собранию Lync для Firefox и Chrome</span><span class="sxs-lookup"><span data-stu-id="9bf9c-185">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-186">Пользователь может присоединиться к собраниям Lync из Firefox и Chrome</span><span class="sxs-lookup"><span data-stu-id="9bf9c-186">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bf9c-187">Отправлено в драйвер печати OneNote</span><span class="sxs-lookup"><span data-stu-id="9bf9c-187">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-188">Пользователь может печатать в OneNote</span><span class="sxs-lookup"><span data-stu-id="9bf9c-188">User can print to OneNote</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bf9c-189">Связанные заметки OneNote</span><span class="sxs-lookup"><span data-stu-id="9bf9c-189">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-190">Связанные заметки OneNote</span><span class="sxs-lookup"><span data-stu-id="9bf9c-190">OneNote Linked Notes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bf9c-191">Надстройка "отправить в OneNote" в Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="9bf9c-191">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-192">Пользователь может отправлять сообщения в OneNote из браузера Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="9bf9c-192">User can send to OneNote from IE</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bf9c-193">Исключение брандмауэра для Lync и Outlook</span><span class="sxs-lookup"><span data-stu-id="9bf9c-193">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-194">Исключение брандмауэра для Lync и Outlook</span><span class="sxs-lookup"><span data-stu-id="9bf9c-194">Firewall Exception for Lync and Outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bf9c-195">Клиент MAPI</span><span class="sxs-lookup"><span data-stu-id="9bf9c-195">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-196">Встроенные приложения и надстройки могут взаимодействовать с виртуальным приложением Outlook через MAPI</span><span class="sxs-lookup"><span data-stu-id="9bf9c-196">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bf9c-197">Надстройка SharePoint для Firefox</span><span class="sxs-lookup"><span data-stu-id="9bf9c-197">SharePoint Plug-in for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-198">Пользователь может использовать возможности SharePoint в Firefox</span><span class="sxs-lookup"><span data-stu-id="9bf9c-198">User can use SharePoint features in Firefox</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bf9c-199">Приложение панели управления "почта"</span><span class="sxs-lookup"><span data-stu-id="9bf9c-199">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-200">Пользователь получает панель управления "почта" в Outlook</span><span class="sxs-lookup"><span data-stu-id="9bf9c-200">User gets the mail control panel applet in Outlook</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bf9c-201">Основные сборки взаимодействия</span><span class="sxs-lookup"><span data-stu-id="9bf9c-201">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-202">Поддержка управляемых надстроек</span><span class="sxs-lookup"><span data-stu-id="9bf9c-202">Support managed add-ins</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bf9c-203">Обработчик кэша документов Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-203">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-204">Разрешение кэша документов для приложений Office</span><span class="sxs-lookup"><span data-stu-id="9bf9c-204">Allows Document Cache for Office applications</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bf9c-205">Обработчик поиска протоколов Outlook</span><span class="sxs-lookup"><span data-stu-id="9bf9c-205">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-206">Пользователь может выполнять поиск в Outlook</span><span class="sxs-lookup"><span data-stu-id="9bf9c-206">User can search in outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bf9c-207">Элементы управления ActiveX:</span><span class="sxs-lookup"><span data-stu-id="9bf9c-207">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-208">Дополнительные сведения об элементах ActiveX можно найти в <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> справочнике API элементов ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="9bf9c-208">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="9bf9c-209">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="9bf9c-209">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-210">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-210">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="9bf9c-211">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="9bf9c-211">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-212">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-212">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="9bf9c-213">SharePoint. openDocument</span><span class="sxs-lookup"><span data-stu-id="9bf9c-213">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-214">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-214">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="9bf9c-215">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="9bf9c-215">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-216">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-216">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="9bf9c-217">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="9bf9c-217">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-218">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-218">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="9bf9c-219">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="9bf9c-219">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-220">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-220">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="9bf9c-221">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="9bf9c-221">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-222">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-222">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="9bf9c-223">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="9bf9c-223">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-224">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-224">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="9bf9c-225">SharePoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="9bf9c-225">Sharepoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-226">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-226">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="9bf9c-227">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="9bf9c-227">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-228">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-228">Active X control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="9bf9c-229">WinProj. активатор</span><span class="sxs-lookup"><span data-stu-id="9bf9c-229">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-230">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-230">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="9bf9c-231">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="9bf9c-231">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-232">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-232">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="9bf9c-233">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="9bf9c-233">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-234">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-234">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="9bf9c-235">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="9bf9c-235">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-236">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-236">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="9bf9c-237">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="9bf9c-237">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-238">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="9bf9c-238">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="9bf9c-239">Вспомогательное приложение браузера OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="9bf9c-239">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-240">Элемент управления ActiveX]</span><span class="sxs-lookup"><span data-stu-id="9bf9c-240">Active X Control]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bf9c-241">Наложения значков OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="9bf9c-241">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bf9c-242">Перекрытие значков оболочки в проводнике Windows при просмотре папок в папках OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="9bf9c-242">Windows Explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bf9c-243">Расширения оболочки</span><span class="sxs-lookup"><span data-stu-id="9bf9c-243">Shell extensions</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bf9c-244">Горячие</span><span class="sxs-lookup"><span data-stu-id="9bf9c-244">Shortcuts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bf9c-245">Windows Search</span><span class="sxs-lookup"><span data-stu-id="9bf9c-245">Windows Search</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





