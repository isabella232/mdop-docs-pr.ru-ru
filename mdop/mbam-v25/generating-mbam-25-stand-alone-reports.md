---
title: Создание изолированных отчетов MBAM 2.5
description: Создание изолированных отчетов MBAM 2.5
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823122"
---
# <span data-ttu-id="a36f7-103">Создание изолированных отчетов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a36f7-103">Generating MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="a36f7-104">При настройке администрирования и мониторинга Microsoft BitLocker (MBAM) с изолированной топологией вы можете создавать отчеты, чтобы отслеживать использование и соответствие шифрования дисков BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a36f7-104">When you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate reports to monitor BitLocker drive encryption usage and compliance.</span></span> <span data-ttu-id="a36f7-105">В этой статье описаны следующие процедуры:</span><span class="sxs-lookup"><span data-stu-id="a36f7-105">This topic contains the following procedures:</span></span>

-   [<span data-ttu-id="a36f7-106">Открытие веб-сайта администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="a36f7-106">To open the Administration and Monitoring Website</span></span>](#bkmk-openadmin)

-   [<span data-ttu-id="a36f7-107">Создание отчета о соответствии требованиям предприятия</span><span class="sxs-lookup"><span data-stu-id="a36f7-107">To generate an Enterprise Compliance Report</span></span>](#bkmk-enterprise)

-   [<span data-ttu-id="a36f7-108">Создание отчета о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="a36f7-108">To generate a Computer Compliance Report</span></span>](#bkmk-computercomp)

-   [<span data-ttu-id="a36f7-109">Создание отчета об аудите ключа восстановления</span><span class="sxs-lookup"><span data-stu-id="a36f7-109">To generate a Recovery Key Audit Report</span></span>](#bkmk-recoverykey)

<span data-ttu-id="a36f7-110">Описания отдельных отчетов можно найти в разделе [Общие сведения о автономных отчетах о MBAM 2,5](understanding-mbam-25-stand-alone-reports.md).</span><span class="sxs-lookup"><span data-stu-id="a36f7-110">For descriptions of the Stand-alone reports, see [Understanding MBAM 2.5 Stand-alone Reports](understanding-mbam-25-stand-alone-reports.md).</span></span>

<span data-ttu-id="a36f7-111">**Примечание**  Для запуска отчетов необходимо быть участником группы **Пользователи отчетов MBAM** , которую вы настроили в доменных службах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a36f7-111">**Note** To run the reports, you must be a member of the **MBAM Report Users** group, which you configure in Active Directory Domain Services.</span></span> <span data-ttu-id="a36f7-112">Дополнительные сведения можно найти в разделе [планирование для групп MBAM 2,5 и учетных записей](planning-for-mbam-25-groups-and-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="a36f7-112">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

 

<a href="" id="bkmk-openadmin"></a>**<span data-ttu-id="a36f7-113">Открытие веб-сайта администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="a36f7-113">To open the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="a36f7-114">Откройте веб-браузер и перейдите на веб-сайт администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="a36f7-114">Open a web browser and navigate to the Administration and Monitoring Website.</span></span> <span data-ttu-id="a36f7-115">URL-адрес по умолчанию для веб-сайта администрирования и мониторинга:</span><span class="sxs-lookup"><span data-stu-id="a36f7-115">The default URL for the Administration and Monitoring Website is:</span></span>

    *<span data-ttu-id="a36f7-116">HTTP (s):// &lt; MBAMAdministrationServerName &gt; : &lt; Port &gt; /HelpDesk</span><span class="sxs-lookup"><span data-stu-id="a36f7-116">http(s)://&lt;MBAMAdministrationServerName&gt;:&lt;port&gt;/Helpdesk</span></span>*

2.  <span data-ttu-id="a36f7-117">В левой области выберите пункт **отчеты**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-117">In the left pane, click **Reports**.</span></span> <span data-ttu-id="a36f7-118">В верхней строке меню выберите отчет, который вы хотите выполнить.</span><span class="sxs-lookup"><span data-stu-id="a36f7-118">From the top menu bar, select the report you want to run.</span></span>

    <span data-ttu-id="a36f7-119">Данные клиента MBAM сохраняются в базе данных соответствия требованиям и аудита для исторических ссылок в случае потери или кражи компьютера.</span><span class="sxs-lookup"><span data-stu-id="a36f7-119">MBAM client data is retained in the Compliance and Audit Database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="a36f7-120">При работе с корпоративными отчетами мы рекомендуем использовать соответствующие даты начала и окончания, чтобы определить временные интервалы для отчетов в отчете от одной до двух недель, чтобы улучшить отчет о точности данных.</span><span class="sxs-lookup"><span data-stu-id="a36f7-120">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="a36f7-121">После создания отчета вы можете сохранить результаты в разных форматах, таких как HTML, Microsoft Word и Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a36f7-121">After you generate a report, you can save the results in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="a36f7-122">**Примечание**  Настройте службы SQL Server Reporting Services (SSRS) для использования протокола SSL (Secure Sockets Layer) перед настройкой веб-сайта администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="a36f7-122">**Note** Configure SQL Server Reporting Services (SSRS) to use Secure Sockets Layer (SSL) before configuring the Administration and Monitoring Website.</span></span> <span data-ttu-id="a36f7-123">Если по какой-либо причине служба SSRS не настроена на использование протокола SSL, при настройке веб-сайта администрирования и наблюдения для отчетов будет задано значение HTTP вместо HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a36f7-123">If, for any reason, SSRS is not configured to use SSL, the URL for the Reports will be set to HTTP instead of to HTTPS when you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="a36f7-124">Если затем перейти на веб-сайт администрирования и наблюдения и выбрать отчет, появится следующее сообщение: "только безопасное содержимое отображается".</span><span class="sxs-lookup"><span data-stu-id="a36f7-124">If you then go to the Administration and Monitoring Website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="a36f7-125">Чтобы отобразить отчет, выберите пункт **Показать весь контент**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-125">To show the report, click **Show All Content**.</span></span>

     

<a href="" id="bkmk-enterprise"></a>**<span data-ttu-id="a36f7-126">Создание отчета о соответствии требованиям предприятия</span><span class="sxs-lookup"><span data-stu-id="a36f7-126">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="a36f7-127">На веб-сайте администрирования и мониторинга выберите узел **отчеты** в области навигации слева, выберите **отчет о корпоративном соответствии**и выберите Фильтры, которые вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="a36f7-127">From the Administration and Monitoring Website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="a36f7-128">Доступные фильтры для отчета о соответствии требованиям предприятия:</span><span class="sxs-lookup"><span data-stu-id="a36f7-128">The available filters for the Enterprise Compliance Report are:</span></span>

    -   <span data-ttu-id="a36f7-129">**Состояние соответствия требованиям**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-129">**Compliance Status**.</span></span> <span data-ttu-id="a36f7-130">Используйте этот фильтр, чтобы указать типы состояния соответствия для отчета (например, совместимый или несоответствующий).</span><span class="sxs-lookup"><span data-stu-id="a36f7-130">Use this filter to specify the compliance status types of the report (for example, Compliant or Noncompliant).</span></span>

    -   <span data-ttu-id="a36f7-131">**Состояние ошибки**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-131">**Error State**.</span></span> <span data-ttu-id="a36f7-132">Используйте этот фильтр, чтобы указать типы состояния ошибки отчета (например, нет ошибки или ошибки).</span><span class="sxs-lookup"><span data-stu-id="a36f7-132">Use this filter to specify the error state types of the report (for example, No Error or Error).</span></span>

2.  <span data-ttu-id="a36f7-133">Нажмите кнопку **Просмотр отчета** , чтобы отобразить выбранный отчет.</span><span class="sxs-lookup"><span data-stu-id="a36f7-133">Click **View Report** to display the selected report.</span></span>

3.  <span data-ttu-id="a36f7-134">Выберите имя компьютера, чтобы просмотреть сведения о нем в отчете о соответствии компьютера.</span><span class="sxs-lookup"><span data-stu-id="a36f7-134">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="a36f7-135">Щелкните знак "плюс" (+) рядом с именем компьютера, чтобы просмотреть сведения о томах на компьютере.</span><span class="sxs-lookup"><span data-stu-id="a36f7-135">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

<a href="" id="bkmk-computercomp"></a>**<span data-ttu-id="a36f7-136">Создание отчета о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="a36f7-136">To generate a Computer Compliance Report</span></span>**

1.  <span data-ttu-id="a36f7-137">На веб-сайте администрирования и мониторинга выберите узел **отчета** в области навигации слева, а затем выберите **отчет о соответствии компьютера**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-137">From the Administration and Monitoring Website, select the **Report** node from the left navigation pane, and then select **Computer Compliance Report**.</span></span> <span data-ttu-id="a36f7-138">Используйте отчет о соответствии компьютера для поиска **имени пользователя** или **имени компьютера**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-138">Use the Computer Compliance Report to search for **User name** or **Computer name**.</span></span>

2.  <span data-ttu-id="a36f7-139">Нажмите кнопку **Просмотр отчета** , чтобы просмотреть отчет о соответствии компьютера.</span><span class="sxs-lookup"><span data-stu-id="a36f7-139">Click **View Report** to view the Computer Compliance Report.</span></span>

3.  <span data-ttu-id="a36f7-140">Выберите имя компьютера, чтобы просмотреть дополнительные сведения о нем в отчете о соответствии компьютера.</span><span class="sxs-lookup"><span data-stu-id="a36f7-140">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="a36f7-141">Щелкните знак "плюс" (+) рядом с именем компьютера, чтобы просмотреть сведения о томах на компьютере.</span><span class="sxs-lookup"><span data-stu-id="a36f7-141">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="a36f7-142">**Примечание**  Клиентский компьютер MBAM считается совместимым, если компьютер соответствует или превышает требования к параметрам групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="a36f7-142">**Note** An MBAM client computer is considered compliant if the computer matches or exceeds the requirements of the MBAM Group Policy settings.</span></span>

<a href="" id="bkmk-recoverykey"></a>**<span data-ttu-id="a36f7-143">Создание отчета об аудите ключа восстановления</span><span class="sxs-lookup"><span data-stu-id="a36f7-143">To generate a Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="a36f7-144">На веб-сайте администрирования и мониторинга выберите узел **отчета** в области навигации слева, а затем щелкните **отчет аудит восстановления**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-144">From the Administration and Monitoring Website, select the **Report** node in the left navigation pane, and then select **Recovery Audit Report**.</span></span> <span data-ttu-id="a36f7-145">Выберите Фильтры для отчета об аудите ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="a36f7-145">Select the filters for your Recovery Key Audit Report.</span></span> <span data-ttu-id="a36f7-146">Ниже приведены доступные фильтры для аудита ключей восстановления.</span><span class="sxs-lookup"><span data-stu-id="a36f7-146">The available filters for recovery key audits are as follows:</span></span>

    -   <span data-ttu-id="a36f7-147">**Пользователь службы поддержки**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-147">**Helpdesk User**.</span></span> <span data-ttu-id="a36f7-148">С помощью этого фильтра пользователи смогут указать имя пользователя, который является инициатором запроса.</span><span class="sxs-lookup"><span data-stu-id="a36f7-148">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="a36f7-149">Инициатор запроса — это человек в службе поддержки, который получил доступ к ключу от имени конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="a36f7-149">The requester is the person in the Help Desk who accessed the key on behalf of an end user.</span></span>

    -   <span data-ttu-id="a36f7-150">**Конечным пользователем**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-150">**End User**.</span></span> <span data-ttu-id="a36f7-151">С помощью этого фильтра пользователи смогут указать имя пользователя, который является инициатором запроса.</span><span class="sxs-lookup"><span data-stu-id="a36f7-151">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="a36f7-152">Инициатор запроса — это конечный пользователь, который вызвал службу поддержки, чтобы получить ключ восстановления.</span><span class="sxs-lookup"><span data-stu-id="a36f7-152">The requestee is the end user who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="a36f7-153">**Результат запроса**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-153">**Request Result**.</span></span> <span data-ttu-id="a36f7-154">Этот фильтр позволяет пользователям указывать типы результатов запросов (например, успех или неудача), на основе которых будет основываться отчет.</span><span class="sxs-lookup"><span data-stu-id="a36f7-154">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="a36f7-155">Например, пользователи могут захочет просмотреть попытки доступа к Key с ошибками.</span><span class="sxs-lookup"><span data-stu-id="a36f7-155">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="a36f7-156">**Тип ключа**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-156">**Key Type**.</span></span> <span data-ttu-id="a36f7-157">Этот фильтр позволяет пользователям указывать тип ключа (например, пароль ключа восстановления или хэш пароля доверенного платформенного модуля), на котором будет основываться отчет.</span><span class="sxs-lookup"><span data-stu-id="a36f7-157">This filter enables users to specify the key type (for example, Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="a36f7-158">**Дата начала**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-158">**Start Date**.</span></span> <span data-ttu-id="a36f7-159">Этот фильтр используется для определения части даты начала диапазона дат, о котором пользователь хочет сообщить.</span><span class="sxs-lookup"><span data-stu-id="a36f7-159">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="a36f7-160">**Дата окончания**.</span><span class="sxs-lookup"><span data-stu-id="a36f7-160">**End Date**.</span></span> <span data-ttu-id="a36f7-161">Этот фильтр используется для определения части даты окончания диапазона дат, о котором вы хотите сообщить пользователям.</span><span class="sxs-lookup"><span data-stu-id="a36f7-161">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="a36f7-162">Нажмите кнопку **Просмотр отчета** , чтобы просмотреть отчет.</span><span class="sxs-lookup"><span data-stu-id="a36f7-162">Click **View Report** to view the report.</span></span>



## <span data-ttu-id="a36f7-163">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a36f7-163">Related topics</span></span>


[<span data-ttu-id="a36f7-164">Мониторинг и создание отчетов по соответствию BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a36f7-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="a36f7-165">Общие сведения об изолированных отчетах MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a36f7-165">Understanding MBAM 2.5 Stand-alone Reports</span></span>](understanding-mbam-25-stand-alone-reports.md)

 

## <span data-ttu-id="a36f7-166">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="a36f7-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a36f7-167">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="a36f7-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a36f7-168">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a36f7-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





