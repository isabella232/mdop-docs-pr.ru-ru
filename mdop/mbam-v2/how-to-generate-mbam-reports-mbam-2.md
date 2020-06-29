---
title: Создание отчетов MBAM
description: Создание отчетов MBAM
author: dansimp
ms.assetid: 083550cb-8c3f-49b3-a30e-97d85374d2f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ccdc1a2cd69d8cc2e2c2823827f5ea43ad867a78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824092"
---
# <span data-ttu-id="63a6c-103">Создание отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="63a6c-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="63a6c-104">При установке системы администрирования и мониторинга Microsoft BitLocker (MBAM) с изолированной топологией вы можете создавать различные отчеты, чтобы отслеживать использование шифрования BitLocker и их соответствие требованиям.</span><span class="sxs-lookup"><span data-stu-id="63a6c-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate different reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="63a6c-105">В этой статье описаны действия, которые необходимо выполнить, чтобы открыть веб-сайт администрирования и наблюдения и шаги, необходимые для создания администраторов Microsoft BitLocker и наблюдения за отчетами о соответствии требованиям в масштабах предприятия, отдельных компьютерах и действиях по восстановлению ключей.</span><span class="sxs-lookup"><span data-stu-id="63a6c-105">The procedures in this topic describe how to open the Administration and Monitoring website and the steps that are needed to generate Microsoft BitLocker Administration and Monitoring reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="63a6c-106">Подробные сведения, помогающие понять MBAM отчеты, можно найти в разделе [Основные сведения о MBAM отчетах](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="63a6c-106">For detailed information to help understand MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

<span data-ttu-id="63a6c-107">**Примечание**  Для запуска отчетов необходимо быть участником **роли пользователи отчета** на компьютерах, на которых установлены функции администрирования и мониторинга сервера, база данных соответствия требованиям и аудита, а также отчеты о соответствии требованиям и аудите.</span><span class="sxs-lookup"><span data-stu-id="63a6c-107">**Note** To run the reports, you must be a member of the **Report Users Role** on the computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

 

**<span data-ttu-id="63a6c-108">Открытие веб-сайта администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="63a6c-108">To open the Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="63a6c-109">Откройте веб-браузер и перейдите на веб-сайт администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="63a6c-109">Open a web browser and navigate to the Administration and Monitoring website.</span></span> <span data-ttu-id="63a6c-110">URL-адресом по умолчанию для веб-сайта администрирования и мониторинга является \*http:// &lt; имя_компьютера &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="63a6c-110">The default URL for the Administration and Monitoring website is *http://&lt;computername&gt;*.</span></span>

    <span data-ttu-id="63a6c-111">**Примечание**  Если веб-сайт theAdministration и мониторинг установлены на порте, отличном от 80, необходимо указать порт в URL-адресе (например, \*http:// &lt; имя_компьютера &gt; : &lt; порт &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="63a6c-111">**Note** If theAdministration and Monitoring website was installed on a port other than 80, you have to specify the port in the URL (for example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="63a6c-112">Если вы указали имя узла для theAdministration и веб-сайта мониторинга во время установки, URL-адрес будет \*http:// &lt; именем узла &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="63a6c-112">If you specified a host name for theAdministration and Monitoring website during the installation, the URL is *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="63a6c-113">В левой области выберите пункт **отчеты** , а затем выберите отчет, который нужно выполнить, в верхней строке меню.</span><span class="sxs-lookup"><span data-stu-id="63a6c-113">In the left pane, click **Reports** and then select the report you want to run from the top menu bar.</span></span>

    <span data-ttu-id="63a6c-114">Исторические данные клиента MBAM хранятся в базе данных соответствия требованиям для исторических ссылок в случае потери или кражи компьютера.</span><span class="sxs-lookup"><span data-stu-id="63a6c-114">Historical MBAM client data is retained in the compliance database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="63a6c-115">При работе с корпоративными отчетами мы рекомендуем использовать соответствующие даты начала и окончания, чтобы определить временные интервалы для отчетов в отчете от одной до двух недель, чтобы улучшить отчет о точности данных.</span><span class="sxs-lookup"><span data-stu-id="63a6c-115">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="63a6c-116">**Примечание**  Если служба SSRS не настроена на использование Secure Socket Layer, то при установке сервера MBAM URL-адрес для отчетов будет установлен в значение HTTP вместо HTTPS.</span><span class="sxs-lookup"><span data-stu-id="63a6c-116">**Note** If SSRS was not configured to use Secure Socket Layer, the URL for the reports will be set to HTTP instead of to HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="63a6c-117">Если затем перейти на портал службы поддержки и выбрать отчет, появится следующее сообщение: "только безопасное содержимое отображается".</span><span class="sxs-lookup"><span data-stu-id="63a6c-117">If you then go to the Help Desk portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="63a6c-118">Чтобы отобразить отчет, выберите пункт **Показать весь контент**.</span><span class="sxs-lookup"><span data-stu-id="63a6c-118">To show the report, click **Show All Content**.</span></span>

     

**<span data-ttu-id="63a6c-119">Создание отчета о соответствии требованиям предприятия</span><span class="sxs-lookup"><span data-stu-id="63a6c-119">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="63a6c-120">На веб-сайте администрирования и мониторинга выберите узел **отчеты** в области навигации слева, выберите **отчет о корпоративном соответствии**и выберите Фильтры, которые вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="63a6c-120">From the Administration and Monitoring website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="63a6c-121">Ниже указаны доступные фильтры для отчета о соответствии требованиям предприятия.</span><span class="sxs-lookup"><span data-stu-id="63a6c-121">The available filters for the Enterprise Compliance Report are the following:</span></span>

    -   <span data-ttu-id="63a6c-122">**Состояние соответствия требованиям**.</span><span class="sxs-lookup"><span data-stu-id="63a6c-122">**Compliance Status**.</span></span> <span data-ttu-id="63a6c-123">Используйте этот фильтр, чтобы указать типы состояния соответствия (например, соответствие требованиям или несоответствующие требованиям) отчета.</span><span class="sxs-lookup"><span data-stu-id="63a6c-123">Use this filter to specify the compliance status types (for example, Compliant, or Noncompliant) of the report.</span></span>

    -   <span data-ttu-id="63a6c-124">**Состояние ошибки**.</span><span class="sxs-lookup"><span data-stu-id="63a6c-124">**Error State**.</span></span> <span data-ttu-id="63a6c-125">Используйте этот фильтр, чтобы указать типы состояния ошибки (например, нет ошибки или ошибки) отчета.</span><span class="sxs-lookup"><span data-stu-id="63a6c-125">Use this filter to specify the error state types (for example, No Error, or Error) of the report.</span></span>

2.  <span data-ttu-id="63a6c-126">Нажмите кнопку **Просмотр отчета** , чтобы отобразить выбранный отчет.</span><span class="sxs-lookup"><span data-stu-id="63a6c-126">Click **View Report** to display the selected report.</span></span>

    <span data-ttu-id="63a6c-127">Результаты можно сохранять в разных форматах, таких как HTML, Microsoft Word и Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="63a6c-127">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="63a6c-128">**Примечание**  Отчет о соответствии требованиям предприятия создается заданием SQL, которое выполняется каждые шесть часов.</span><span class="sxs-lookup"><span data-stu-id="63a6c-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="63a6c-129">Таким образом, при первом просмотре отчета могут возникнуть недостающие данные.</span><span class="sxs-lookup"><span data-stu-id="63a6c-129">Therefore, the first time you view the report, you may find that some data is missing.</span></span> <span data-ttu-id="63a6c-130">Вы можете создавать обновленные данные отчета вручную с помощью SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="63a6c-130">You can generate updated report data manually by using SQL Management Studio.</span></span> <span data-ttu-id="63a6c-131">В окне **обозревателя объектов** разверните узел **Агент SQL Server**, разверните **задания**, щелкните правой кнопкой мыши задание **CreateCache** и выберите команду **начать задание на шаге....**</span><span class="sxs-lookup"><span data-stu-id="63a6c-131">From the **Object Explorer** window, expand **SQL Server Agent**, expand **Jobs**, right-click the **CreateCache** job, and select **Start Job at Step….**</span></span>

     

3.  <span data-ttu-id="63a6c-132">Выберите имя компьютера, чтобы просмотреть сведения о нем в отчете о соответствии компьютера.</span><span class="sxs-lookup"><span data-stu-id="63a6c-132">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="63a6c-133">Щелкните знак "плюс" (+) рядом с именем компьютера, чтобы просмотреть сведения о томах на компьютере.</span><span class="sxs-lookup"><span data-stu-id="63a6c-133">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="63a6c-134">Создание отчета о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="63a6c-134">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="63a6c-135">На веб-сайте администрирования и мониторинга выберите узел **отчета** в области навигации слева, а затем выберите **отчет о соответствии компьютера**.</span><span class="sxs-lookup"><span data-stu-id="63a6c-135">In the Administration and Monitoring website, select the **Report** node from the left navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="63a6c-136">Используйте отчет о соответствии компьютера для поиска **имени пользователя** или **имени компьютера**.</span><span class="sxs-lookup"><span data-stu-id="63a6c-136">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="63a6c-137">Нажмите кнопку **Просмотр отчета** , чтобы просмотреть отчет о компьютере.</span><span class="sxs-lookup"><span data-stu-id="63a6c-137">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="63a6c-138">Результаты можно сохранять в разных форматах, таких как HTML, Microsoft Word и Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="63a6c-138">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="63a6c-139">Выберите имя компьютера, чтобы просмотреть дополнительные сведения о нем в отчете о соответствии компьютера.</span><span class="sxs-lookup"><span data-stu-id="63a6c-139">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="63a6c-140">Щелкните знак "плюс" (+) рядом с именем компьютера, чтобы просмотреть сведения о томах на компьютере.</span><span class="sxs-lookup"><span data-stu-id="63a6c-140">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="63a6c-141">**Примечание**  Клиентский компьютер MBAM считается совместимым, если компьютер соответствует требованиям, предъявляемым параметрами политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="63a6c-141">**Note** An MBAM client computer is considered compliant if the computer matches the requirements of the MBAM policy settings.</span></span>

     

**<span data-ttu-id="63a6c-142">Создание отчета об аудите ключа восстановления</span><span class="sxs-lookup"><span data-stu-id="63a6c-142">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="63a6c-143">На веб-сайте администрирования и мониторинга выберите узел **отчета** в области навигации слева, а затем выберите **отчет аудит восстановления**.</span><span class="sxs-lookup"><span data-stu-id="63a6c-143">From the Administration and Monitoring website, select the **Report** node in the left navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="63a6c-144">Выберите Фильтры для отчета об аудите ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="63a6c-144">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="63a6c-145">Ниже приведены доступные фильтры для аудита ключей восстановления.</span><span class="sxs-lookup"><span data-stu-id="63a6c-145">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="63a6c-146">**Инициатор запроса**.</span><span class="sxs-lookup"><span data-stu-id="63a6c-146">**Requestor**.</span></span> <span data-ttu-id="63a6c-147">С помощью этого фильтра пользователи смогут указать имя пользователя, который является инициатором запроса.</span><span class="sxs-lookup"><span data-stu-id="63a6c-147">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="63a6c-148">Автор запроса — это человек в службе поддержки, который получил доступ к ключу от имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="63a6c-148">The requester is the person in the Help Desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="63a6c-149">**Инициатор запроса**.</span><span class="sxs-lookup"><span data-stu-id="63a6c-149">**Requestee**.</span></span> <span data-ttu-id="63a6c-150">С помощью этого фильтра пользователи смогут указать имя пользователя, который является инициатором запроса.</span><span class="sxs-lookup"><span data-stu-id="63a6c-150">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="63a6c-151">Автор запроса — это человек, который позвонил в службу поддержки, чтобы получить ключ восстановления.</span><span class="sxs-lookup"><span data-stu-id="63a6c-151">The requestee is the person who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="63a6c-152">**Результат запроса**.</span><span class="sxs-lookup"><span data-stu-id="63a6c-152">**Request Result**.</span></span> <span data-ttu-id="63a6c-153">Этот фильтр позволяет пользователям указывать типы результатов запросов (например, успех или неудача), на основе которых будет основываться отчет.</span><span class="sxs-lookup"><span data-stu-id="63a6c-153">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="63a6c-154">Например, пользователи могут захочет просмотреть попытки доступа к Key с ошибками.</span><span class="sxs-lookup"><span data-stu-id="63a6c-154">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="63a6c-155">**Тип ключа**.</span><span class="sxs-lookup"><span data-stu-id="63a6c-155">**Key Type**.</span></span> <span data-ttu-id="63a6c-156">Этот фильтр позволяет пользователям указывать тип ключа (например, пароль ключа восстановления или хэш пароля доверенного платформенного модуля), для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="63a6c-156">This filter enables users to specify the Key Type (for example: Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="63a6c-157">**Дата начала**.</span><span class="sxs-lookup"><span data-stu-id="63a6c-157">**Start Date**.</span></span> <span data-ttu-id="63a6c-158">Этот фильтр используется для определения части даты начала диапазона дат, о котором пользователь хочет сообщить.</span><span class="sxs-lookup"><span data-stu-id="63a6c-158">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="63a6c-159">**Дата окончания**.</span><span class="sxs-lookup"><span data-stu-id="63a6c-159">**End Date**.</span></span> <span data-ttu-id="63a6c-160">Этот фильтр используется для определения части даты окончания диапазона дат, о котором вы хотите сообщить пользователям.</span><span class="sxs-lookup"><span data-stu-id="63a6c-160">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="63a6c-161">Нажмите кнопку **Просмотр отчета** , чтобы просмотреть отчет.</span><span class="sxs-lookup"><span data-stu-id="63a6c-161">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="63a6c-162">Результаты можно сохранять в разных форматах, таких как HTML, Microsoft Word и Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="63a6c-162">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="63a6c-163">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="63a6c-163">Related topics</span></span>


[<span data-ttu-id="63a6c-164">Мониторинг и создание отчетов по соответствию BitLocker с помощью MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="63a6c-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





