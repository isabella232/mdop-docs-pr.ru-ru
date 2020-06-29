---
title: Создание отчетов MBAM
description: Создание отчетов MBAM
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824529"
---
# <span data-ttu-id="5811f-103">Создание отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="5811f-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="5811f-104">Средства администрирования и мониторинга Microsoft BitLocker (MBAM) создают различные отчеты, чтобы отслеживать использование шифрования BitLocker и соответствие требованиям.</span><span class="sxs-lookup"><span data-stu-id="5811f-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="5811f-105">В этой статье описано, как открыть веб-сайт администрирования MBAM и как создавать отчеты MBAM на соответствие требованиям в масштабах предприятия, отдельных компьютерах, совместимости оборудования и действиях по восстановлению ключей.</span><span class="sxs-lookup"><span data-stu-id="5811f-105">This topic describes how to open the MBAM administration website and how to generate MBAM reports on enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span> <span data-ttu-id="5811f-106">Дополнительные сведения о MBAM отчетах можно найти в статьях [сведения о MBAM отчетах](understanding-mbam-reports-mbam-1.md).</span><span class="sxs-lookup"><span data-stu-id="5811f-106">For more information about MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-1.md).</span></span>

<span data-ttu-id="5811f-107">**Примечание**  Для работы с отчетами необходимо быть участником роли **Пользователи отчета** на компьютерах, на которых установлены функции администрирования и мониторинга сервера, база данных соответствия требованиям и проверки соответствия требованиям, а также отчеты о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="5811f-107">**Note** To run the reports, you must be a member of the **Report Users** role on the computers where you have installed the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports.</span></span>

 

**<span data-ttu-id="5811f-108">Открытие веб-сайта администрирования MBAM</span><span class="sxs-lookup"><span data-stu-id="5811f-108">To open the MBAM Administration website</span></span>**

1.  <span data-ttu-id="5811f-109">Откройте веб-браузер и перейдите на веб-сайт MBAM.</span><span class="sxs-lookup"><span data-stu-id="5811f-109">Open a web browser and navigate to the MBAM website.</span></span> <span data-ttu-id="5811f-110">URL-адресом по умолчанию для веб-сайта является \*http:// &lt; ComputerName &gt; \* сервера администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5811f-110">The default URL for the website is *http://&lt;computername&gt;* of the Microsoft BitLocker Administration and Monitoring server.</span></span>

    <span data-ttu-id="5811f-111">**Примечание**  Если веб-сайт MBAMadministration был установлен на порт, отличный от порта 80, необходимо указать этот номер порта в URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="5811f-111">**Note** If the MBAMadministration website was installed on a port other than port 80, you must specify that port number in the URL.</span></span> <span data-ttu-id="5811f-112">Например, \*http:// &lt; имя_компьютера &gt; : &lt; порт &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="5811f-112">For example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="5811f-113">Если во время установки вы указали имя узла для веб-сайта MBAMadministration, URL-адрес *будет &lt; http:// &gt; именем узла*.</span><span class="sxs-lookup"><span data-stu-id="5811f-113">If you specified a Host Name for the MBAMadministration website during the installation, the URL would be *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="5811f-114">В области навигации выберите пункт **отчеты**.</span><span class="sxs-lookup"><span data-stu-id="5811f-114">In the navigation pane, click **Reports**.</span></span> <span data-ttu-id="5811f-115">В основной области щелкните вкладку с типом отчета: **отчет о соответствии требованиям предприятия**, **отчет**об **оборудовании, отчет аудита оборудования**или **отчет аудита восстановления**.</span><span class="sxs-lookup"><span data-stu-id="5811f-115">In the main pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

    <span data-ttu-id="5811f-116">**Примечание**  Исторические данные клиента MBAM хранятся в базе данных соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="5811f-116">**Note** Historical MBAM Client data is retained in the compliance database.</span></span> <span data-ttu-id="5811f-117">Эти данные могут быть необходимы в случае потери или кражи компьютера.</span><span class="sxs-lookup"><span data-stu-id="5811f-117">This retained data may be needed in case a computer is lost or stolen.</span></span> <span data-ttu-id="5811f-118">При работе с корпоративными отчетами следует использовать соответствующие даты начала и окончания, чтобы определить временные интервалы для отчетов в отчете от одной до двух недель, чтобы улучшить точность данных в отчете.</span><span class="sxs-lookup"><span data-stu-id="5811f-118">When running enterprise reports, you should use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase the reporting data accuracy.</span></span>

     

**<span data-ttu-id="5811f-119">Создание отчета о соответствии требованиям предприятия</span><span class="sxs-lookup"><span data-stu-id="5811f-119">To generate an enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="5811f-120">На веб-сайте MBAMadministration в области навигации нажмите кнопку **отчеты** , а затем откройте вкладку **Корпоративный отчет о соответствии требованиям** и выберите соответствующие фильтры.</span><span class="sxs-lookup"><span data-stu-id="5811f-120">On the MBAMadministration website, click **Reports** in the navigation pane, then click the **Enterprise Compliance Report** tab and select the appropriate filters for your report.</span></span> <span data-ttu-id="5811f-121">Для отчета "соответствие требованиям предприятия" можно настроить следующие фильтры.</span><span class="sxs-lookup"><span data-stu-id="5811f-121">For the Enterprise Compliance Report, you can set the following filters.</span></span>

    -   <span data-ttu-id="5811f-122">**Состояние соответствия требованиям**.</span><span class="sxs-lookup"><span data-stu-id="5811f-122">**Compliance Status**.</span></span> <span data-ttu-id="5811f-123">Используйте этот фильтр, чтобы указать типы состояния соответствия (например, "соответствует требованиям" или "не соответствует требованиям"), которые нужно включить в отчет.</span><span class="sxs-lookup"><span data-stu-id="5811f-123">Use this filter to specify the compliance status types (for example, Compliant or Noncompliant) to include in the report.</span></span>

    -   <span data-ttu-id="5811f-124">**Состояние ошибки**.</span><span class="sxs-lookup"><span data-stu-id="5811f-124">**Error State**.</span></span> <span data-ttu-id="5811f-125">Используйте этот фильтр, чтобы указать типы состояния ошибки (например, "нет ошибок" или "ошибка"), которые нужно включить в отчет.</span><span class="sxs-lookup"><span data-stu-id="5811f-125">Use this filter to specify the Error State types, such as No Error or Error, to include in the report.</span></span>

2.  <span data-ttu-id="5811f-126">Нажмите кнопку **Просмотр отчета** , чтобы отобразить указанный отчет.</span><span class="sxs-lookup"><span data-stu-id="5811f-126">Click **View Report** to display the specified report.</span></span>

    <span data-ttu-id="5811f-127">Результаты отчета можно сохранить в нескольких доступных форматах файлов, таких как HTML, Microsoft Word и Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5811f-127">The report results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="5811f-128">**Примечание**  Отчет о соответствии требованиям предприятия создается заданием SQL, которое выполняется каждые шесть часов.</span><span class="sxs-lookup"><span data-stu-id="5811f-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="5811f-129">Таким образом, при попытке просмотреть отчет в первый раз вы можете обнаружить, что некоторые данные отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="5811f-129">Therefore, the first time you try to view the report you may find that some data is missing.</span></span>

     

3.  <span data-ttu-id="5811f-130">Чтобы просмотреть сведения о компьютере в отчете соответствие требованиям компьютера, выберите имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="5811f-130">To view information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="5811f-131">Щелкните знак "плюс" (+) рядом с именем компьютера, чтобы просмотреть сведения о томах на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5811f-131">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="5811f-132">Создание отчета о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="5811f-132">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="5811f-133">На веб-сайте MBAMadministration выберите узел **отчета** в области навигации, а затем выберите **отчет о соответствии компьютера**.</span><span class="sxs-lookup"><span data-stu-id="5811f-133">In the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="5811f-134">Используйте отчет о соответствии компьютера для поиска **имени пользователя** или **имени компьютера**.</span><span class="sxs-lookup"><span data-stu-id="5811f-134">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="5811f-135">Нажмите кнопку **Просмотр отчета** , чтобы просмотреть отчет о компьютере.</span><span class="sxs-lookup"><span data-stu-id="5811f-135">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="5811f-136">Результаты можно сохранить в нескольких доступных форматах файлов, таких как HTML, Microsoft Word и Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5811f-136">Results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="5811f-137">Чтобы отобразить дополнительные сведения о компьютере в отчете соответствие требованиям компьютера, выберите имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="5811f-137">To display more information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="5811f-138">Щелкните знак "плюс" (+) рядом с именем компьютера, чтобы просмотреть сведения о томах на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5811f-138">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="5811f-139">**Примечание**  Клиентский компьютер MBAM считается совместимым, если компьютер соответствует требованиям параметров политики MBAM или аппаратной модели компьютера задано значение "несовместимо".</span><span class="sxs-lookup"><span data-stu-id="5811f-139">**Note** An MBAM Client computer is considered compliant if the computer matches the requirements of the MBAM policy settings or the computer’s hardware model is set to incompatible.</span></span> <span data-ttu-id="5811f-140">Таким образом, при просмотре подробных сведений о томах диска, связанных с компьютером, компьютеры, исключающие шифрование BitLocker из-за аппаратной совместимости, могут отображаться как совместимые, несмотря на то что их состояние шифрования тома не соответствует требованиям.</span><span class="sxs-lookup"><span data-stu-id="5811f-140">Therefore, when you are viewing detailed information about the disk volumes associated with the computer, computers that are exempt from BitLocker encryption due to hardware compatibility can be displayed as compliant even though their drive volume encryption status is displayed as noncompliant.</span></span>

     

**<span data-ttu-id="5811f-141">Создание отчета об аудите совместимости оборудования</span><span class="sxs-lookup"><span data-stu-id="5811f-141">To generate the Hardware Compatibility Audit Report</span></span>**

1.  <span data-ttu-id="5811f-142">На веб-сайте MBAMadministration выберите узел **отчета** в области навигации, а затем выберите **отчет об аудите оборудования**.</span><span class="sxs-lookup"><span data-stu-id="5811f-142">From the MBAMadministration website, select the **Report** node from the navigation pane, and then select the **Hardware Audit Report**.</span></span> <span data-ttu-id="5811f-143">Выберите нужные фильтры для вашего отчета об аудите оборудования.</span><span class="sxs-lookup"><span data-stu-id="5811f-143">Select the appropriate filters for your Hardware Audit report.</span></span> <span data-ttu-id="5811f-144">В отчете аудита оборудования предлагаются следующие доступные фильтры:</span><span class="sxs-lookup"><span data-stu-id="5811f-144">The Hardware Audit report offers the following available filters:</span></span>

    -   <span data-ttu-id="5811f-145">**User (Domain\\User)**.</span><span class="sxs-lookup"><span data-stu-id="5811f-145">**User (Domain\\User)**.</span></span> <span data-ttu-id="5811f-146">Указывает имя пользователя, который внес изменения.</span><span class="sxs-lookup"><span data-stu-id="5811f-146">Specifies the name of the user who made a change.</span></span>

    -   <span data-ttu-id="5811f-147">**Тип изменения**.</span><span class="sxs-lookup"><span data-stu-id="5811f-147">**Change Type**.</span></span> <span data-ttu-id="5811f-148">Определяет тип изменений, которые вы ищете.</span><span class="sxs-lookup"><span data-stu-id="5811f-148">Specifies the type of changes you are looking for.</span></span>

    -   <span data-ttu-id="5811f-149">**Дата начала**.</span><span class="sxs-lookup"><span data-stu-id="5811f-149">**Start Date**.</span></span> <span data-ttu-id="5811f-150">Указывает часть даты начала диапазона дат, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="5811f-150">Specifies the Start Date part of the date range that you want to report on.</span></span>

    -   <span data-ttu-id="5811f-151">**Дата окончания**.</span><span class="sxs-lookup"><span data-stu-id="5811f-151">**End Date**.</span></span> <span data-ttu-id="5811f-152">Задает конечную дату диапазона дат, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="5811f-152">Specifies the End Date part of the date range that you want to report on.</span></span>

2.  <span data-ttu-id="5811f-153">Нажмите кнопку **Просмотр отчета** , чтобы просмотреть отчет.</span><span class="sxs-lookup"><span data-stu-id="5811f-153">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="5811f-154">Результаты можно сохранить в нескольких доступных форматах файлов, таких как HTML, Microsoft Word и Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5811f-154">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

**<span data-ttu-id="5811f-155">Создание отчета об аудите ключа восстановления</span><span class="sxs-lookup"><span data-stu-id="5811f-155">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="5811f-156">На веб-сайте MBAMadministration выберите узел **отчета** в области навигации, а затем выберите **отчет аудита восстановления**.</span><span class="sxs-lookup"><span data-stu-id="5811f-156">From the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="5811f-157">Выберите Фильтры для отчета об аудите ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="5811f-157">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="5811f-158">Ниже приведены доступные фильтры для аудита ключей восстановления.</span><span class="sxs-lookup"><span data-stu-id="5811f-158">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="5811f-159">**Инициатор запроса**.</span><span class="sxs-lookup"><span data-stu-id="5811f-159">**Requestor**.</span></span> <span data-ttu-id="5811f-160">Указывает имя пользователя, который является инициатором запроса.</span><span class="sxs-lookup"><span data-stu-id="5811f-160">Specifies the user name of the requestor.</span></span> <span data-ttu-id="5811f-161">Инициатор запроса — это человек в службе поддержки, который получил доступ к ключу от имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="5811f-161">The requestor is the person in the help desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="5811f-162">**Инициатор запроса**.</span><span class="sxs-lookup"><span data-stu-id="5811f-162">**Requestee**.</span></span> <span data-ttu-id="5811f-163">Указывает имя пользователя, который является инициатором запроса.</span><span class="sxs-lookup"><span data-stu-id="5811f-163">Specifies the user name of the requestee.</span></span> <span data-ttu-id="5811f-164">Автор запроса — это человек, который позвонил в службу поддержки, чтобы получить ключ восстановления.</span><span class="sxs-lookup"><span data-stu-id="5811f-164">The requestee is the person who called the help desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="5811f-165">**Результат запроса** Указывает типы результатов запроса, например: успешно или не пройдена.</span><span class="sxs-lookup"><span data-stu-id="5811f-165">**Request Result** Specifies the request result types, such as: Success or Failed.</span></span> <span data-ttu-id="5811f-166">Например, может возникнуть необходимость просмотреть попытки доступа к ключам с ошибками.</span><span class="sxs-lookup"><span data-stu-id="5811f-166">For example, you may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="5811f-167">**Тип ключа**.</span><span class="sxs-lookup"><span data-stu-id="5811f-167">**Key Type**.</span></span> <span data-ttu-id="5811f-168">Задает тип ключа, например: пароль ключа восстановления или хэш пароля TPM.</span><span class="sxs-lookup"><span data-stu-id="5811f-168">Specifies the Key Type, such as: Recovery Key Password or TPM Password Hash.</span></span>

    -   <span data-ttu-id="5811f-169">**Дата начала**.</span><span class="sxs-lookup"><span data-stu-id="5811f-169">**Start Date**.</span></span> <span data-ttu-id="5811f-170">Указывает часть даты начала диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="5811f-170">Specifies the Start Date part of the date range.</span></span>

    -   <span data-ttu-id="5811f-171">**Дата окончания**.</span><span class="sxs-lookup"><span data-stu-id="5811f-171">**End Date**.</span></span> <span data-ttu-id="5811f-172">Указывает часть даты окончания диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="5811f-172">Specifies the End Date part of the date range.</span></span>

2.  <span data-ttu-id="5811f-173">Нажмите кнопку **Просмотр отчета** , чтобы отобразить отчет.</span><span class="sxs-lookup"><span data-stu-id="5811f-173">Click **View Report** to display the report.</span></span>

    <span data-ttu-id="5811f-174">Результаты можно сохранить в нескольких доступных форматах файлов, таких как HTML, Microsoft Word и Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5811f-174">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="5811f-175">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5811f-175">Related topics</span></span>


[<span data-ttu-id="5811f-176">Мониторинг и создание отчетов по соответствию BitLocker с помощью MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5811f-176">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





