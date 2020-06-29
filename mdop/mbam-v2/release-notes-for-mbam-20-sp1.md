---
title: Заметки о выпуске для MBAM 2.0 с пакетом обновления 1 (SP1)
description: Заметки о выпуске для MBAM 2.0 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: b39002ba-33c6-45ec-9d1b-464327b60f5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 54a77fc7a493b36217ae2cdc875226b25fdc6e7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825582"
---
# <span data-ttu-id="71e60-103">Заметки о выпуске для MBAM 2.0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="71e60-103">Release Notes for MBAM 2.0 SP1</span></span>


<span data-ttu-id="71e60-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="71e60-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="71e60-105">Внимательно прочтите эти заметки о выпуске, прежде чем устанавливать администрирование и мониторинг Microsoft BitLocker (MBAM) 2,0 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="71e60-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="71e60-106">Эти заметки о выпуске содержат сведения, необходимые для успешной установки средства администрирования BitLocker и мониторинга 2,0 с пакетом обновления 1 (SP1), и они содержат сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="71e60-106">These release notes contain information that is required to successfully install BitLocker Administration and Monitoring 2.0 SP1, and they contain information that is not available in the product documentation.</span></span> <span data-ttu-id="71e60-107">Если существует разница между этими заметками о выпуске и другой MBAM 2,0 SP1, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="71e60-107">If there is a difference between these release notes and other MBAM 2.0 SP1 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="71e60-108">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="71e60-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> <span data-ttu-id="71e60-109">Известные проблемы с MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="71e60-109">MBAM 2.0 SP1 known issues</span></span>


<span data-ttu-id="71e60-110">В этом разделе содержатся известные проблемы, возникающие при работе с MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="71e60-110">This section contains known issues for MBAM 2.0 SP1.</span></span>

### <span data-ttu-id="71e60-111">Для обновления MBAM с помощью интегрированной топологии Configuration Manager и MBAM 2,0 SP1 требуется удаление объектов Configuration Manager вручную.</span><span class="sxs-lookup"><span data-stu-id="71e60-111">Upgrade of MBAM with Configuration Manager Integrated topology to MBAM 2.0 SP1 requires manual removal of Configuration Manager objects</span></span>

<span data-ttu-id="71e60-112">Если вы используете MBAM в Configuration Manager и хотите перейти на MBAM 2,0 SP1, необходимо вручную удалить все объекты Configuration Manager, которые были установлены в Configuration Manager, в составе MBAM установки.</span><span class="sxs-lookup"><span data-stu-id="71e60-112">If you are using MBAM with Configuration Manager, and you want to upgrade to MBAM 2.0 SP1, you must manually remove all of the Configuration Manager objects that were installed into Configuration Manager as a part of the MBAM installation.</span></span> <span data-ttu-id="71e60-113">Объекты, которые необходимо удалить вручную, — это MBAM отчеты, MBAM поддерживаемые компьютеры, а также базовые параметры конфигурации защиты BitLocker и связанные с ними элементы конфигурации.</span><span class="sxs-lookup"><span data-stu-id="71e60-113">The objects that you must manually remove are the MBAM reports, MBAM Supported Computers collection, and the BitLocker Protection Configuration Baseline and its associated configuration items.</span></span>

<span data-ttu-id="71e60-114">**Временное решение**: обновите объекты Configuration Manager, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="71e60-114">**Workaround**: Upgrade the Configuration Manager objects by completing the following steps:</span></span>

1.  <span data-ttu-id="71e60-115">Создавайте резервные копии существующих данных о соответствиях во внешнем файле, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="71e60-115">Back up existing compliance data to an external file, as described in the following steps.</span></span>

    <span data-ttu-id="71e60-116">**Примечание**  Все существующие данные о соответствии BitLocker будут удалены при удалении существующего базового плана в Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="71e60-116">**Note** All existing BitLocker compliance data will be deleted when you delete the existing baseline in Configuration Manager.</span></span> <span data-ttu-id="71e60-117">Данные будут повторно сформированы с течением времени, но рекомендуется сохранить копию данных в случае, если вам понадобятся данные о соответствии для определенного компьютера, прежде чем будут восстановлены данные о соответствии требованиям.</span><span class="sxs-lookup"><span data-stu-id="71e60-117">The data will be regenerated over time, but it is recommended that you save a copy of the data in case you need the compliance data for a particular computer before the compliance data has been regenerated.</span></span>

     

    1.  <span data-ttu-id="71e60-118">Чтобы сохранить данные о соответствии BitLocker с предысторией, откройте отчет **сведения о соответствии требованиям для программы BitLocker Enterprise** .</span><span class="sxs-lookup"><span data-stu-id="71e60-118">To save historical BitLocker compliance data, open the **BitLocker Enterprise Compliance Details** Report.</span></span>

    2.  <span data-ttu-id="71e60-119">Щелкните значок **сохранить** в отчете и выберите **Excel**.</span><span class="sxs-lookup"><span data-stu-id="71e60-119">Click the **Save** icon in the report and select **Excel**.</span></span>

        <span data-ttu-id="71e60-120">Сохраненный отчет содержит такие данные, как имя компьютера, имя домена, состояние соответствия требованиям, исключения, пользователи устройства, сведения о состоянии соответствия и Дата и время последнего контакта.</span><span class="sxs-lookup"><span data-stu-id="71e60-120">The saved report will contain data such as the computer name, domain name, compliance status, exemption, device users, compliance status details, and last contact date/time.</span></span> <span data-ttu-id="71e60-121">Некоторые сведения, такие как подробные сведения о Томе и стойкость шифрования, не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="71e60-121">Some information, such as detailed volume information and encryption strength, are not saved.</span></span>

2.  <span data-ttu-id="71e60-122">Удалите **MBAM** с сервера с помощью установщика **MBAM** .</span><span class="sxs-lookup"><span data-stu-id="71e60-122">Uninstall **MBAM** from the server by using the **MBAM** installer.</span></span>

3.  <span data-ttu-id="71e60-123">Вручную удалите следующие объекты из Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="71e60-123">Manually delete the following objects from Configuration Manager:</span></span>

    -   <span data-ttu-id="71e60-124">Семейство поддерживаемых компьютеров MBAM</span><span class="sxs-lookup"><span data-stu-id="71e60-124">MBAM Supported Computers collection</span></span>

    -   <span data-ttu-id="71e60-125">Базовые показатели защиты BitLocker</span><span class="sxs-lookup"><span data-stu-id="71e60-125">BitLocker Protection baseline</span></span>

    -   <span data-ttu-id="71e60-126">Элемент конфигурации защиты диска операционной системы BitLocker</span><span class="sxs-lookup"><span data-stu-id="71e60-126">BitLocker Operating System Drive Protection configuration item</span></span>

    -   <span data-ttu-id="71e60-127">Элемент конфигурации защиты фиксированных дисков с данными BitLocker</span><span class="sxs-lookup"><span data-stu-id="71e60-127">BitLocker Fixed Data Drives Protection configuration item</span></span>

4.  <span data-ttu-id="71e60-128">Вручную удалите папку "отчеты MBAM" на сайте служб SQL Server Reporting Services Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="71e60-128">Manually delete the MBAM Reports folder in the Configuration Manager SQL Server Reporting Services site.</span></span> <span data-ttu-id="71e60-129">Для этого выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="71e60-129">To do this:</span></span>

    1.  <span data-ttu-id="71e60-130">С помощью Internet Explorer найдите точку служб Reporting Services, например http:// &lt; yourcmserver &gt; /Reports.</span><span class="sxs-lookup"><span data-stu-id="71e60-130">Use Internet Explorer to browse to the reporting services point, for example, http://&lt;yourcmserver&gt;/reports.</span></span>

    2.  <span data-ttu-id="71e60-131">Щелкните соответствующую ссылку на код сайта Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="71e60-131">Click the appropriate Configuration Manager site code link.</span></span>

    3.  <span data-ttu-id="71e60-132">Удалите папку MBAM.</span><span class="sxs-lookup"><span data-stu-id="71e60-132">Delete the MBAM folder.</span></span>

5.  <span data-ttu-id="71e60-133">Используйте установщик сервера MBAM для переустановки объектов интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="71e60-133">Use the MBAM Server installer to reinstall the Configuration Manager Integration objects.</span></span> <span data-ttu-id="71e60-134">Клиентские компьютеры начинают заново отправлять данные о соответствии требованиям BitLocker с течением времени.</span><span class="sxs-lookup"><span data-stu-id="71e60-134">The client computers will begin to upload BitLocker compliance data again over time.</span></span>

### <span data-ttu-id="71e60-135">Кнопка "Отправить" на портале самообслуживания не работает в Internet Explorer10</span><span class="sxs-lookup"><span data-stu-id="71e60-135">Submit button on Self-Service Portal does not work in Internet Explorer10</span></span>

<span data-ttu-id="71e60-136">При использовании Internet Explorer10 для доступа к веб-сайту администрирования и наблюдения кнопка " **Отправить** " на веб-сайте не работает.</span><span class="sxs-lookup"><span data-stu-id="71e60-136">When you use Internet Explorer10 to access the Administration and Monitoring Website, the **Submit** button on the website does not work.</span></span>

<span data-ttu-id="71e60-137">**Временное решение**: на сервере, на котором установлен веб-сайт администрирования и наблюдения, установите [исправление для файлов описания браузеров ASP.NET](https://go.microsoft.com/fwlink/?LinkId=317798).</span><span class="sxs-lookup"><span data-stu-id="71e60-137">**Workaround**: On the server where you installed the Administration and Monitoring Website, install [Hotfix for ASP.NET browser definition files](https://go.microsoft.com/fwlink/?LinkId=317798).</span></span>

### <span data-ttu-id="71e60-138">Международные доменные имена не поддерживаются</span><span class="sxs-lookup"><span data-stu-id="71e60-138">International domain names are not supported</span></span>

<span data-ttu-id="71e60-139">MBAM 2,0 с пакетом обновления 1 (SP1) не поддерживает международные доменные имена.</span><span class="sxs-lookup"><span data-stu-id="71e60-139">MBAM 2.0 SP1 does not support international domain names.</span></span>

<span data-ttu-id="71e60-140">**Временное решение**: нет.</span><span class="sxs-lookup"><span data-stu-id="71e60-140">**Workaround**: None.</span></span>

### <span data-ttu-id="71e60-141">Отчеты на веб-сайте администрирования и мониторинга выводят предупреждение, если протокол SSL не настроен в SSRS</span><span class="sxs-lookup"><span data-stu-id="71e60-141">Reports in the Administration and Monitoring website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="71e60-142">Если службы отчетов SQLServer (SSRS) не настроены на использование Secure Socket Layer (SSL), при установке сервера MBAM URL-адрес для отчетов будет установлен в значение HTTP вместо HTTPS.</span><span class="sxs-lookup"><span data-stu-id="71e60-142">If SQLServer Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="71e60-143">Если затем перейти на веб-сайт администрирования и наблюдения и выбрать отчет, появится следующее сообщение: "только безопасное содержимое отображается".</span><span class="sxs-lookup"><span data-stu-id="71e60-143">If you then browse to the Administration and Monitoring website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="71e60-144">**Временное решение**: чтобы устранить эту проблему, настройте SSL в **диспетчере конфигурации служб Reporting Services** на сервере MBAM, на котором установлены службы отчетов SQLServer.</span><span class="sxs-lookup"><span data-stu-id="71e60-144">**Workaround**: To correct this issue, configure SSL in **Reporting Services Configuration Manager** on the MBAM server where SQLServer Reporting Services is installed.</span></span> <span data-ttu-id="71e60-145">Удалите и повторно установите веб-сайт сервера администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="71e60-145">Uninstall and then reinstall the Administration and Monitoring Server website.</span></span>

### <span data-ttu-id="71e60-146">При нажатии кнопки "назад" в отчете "Сводка соответствия требованиям" может возникнуть ошибка</span><span class="sxs-lookup"><span data-stu-id="71e60-146">Clicking Back in the Compliance Summary report might create an error</span></span>

<span data-ttu-id="71e60-147">При детализации отчета "Сводка соответствия требованиям" и нажатии **обратной** ссылки в отчете SSRS может возникнуть ошибка.</span><span class="sxs-lookup"><span data-stu-id="71e60-147">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might occur.</span></span>

<span data-ttu-id="71e60-148">**Временное решение**: нет.</span><span class="sxs-lookup"><span data-stu-id="71e60-148">**Workaround**: None.</span></span>

### <span data-ttu-id="71e60-149">Шифрование только использованного пространства не работает должным образом</span><span class="sxs-lookup"><span data-stu-id="71e60-149">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="71e60-150">Если после установки клиента MBAM вы зашифруете компьютер в первый раз, а вы настроили объект групповой политики, чтобы реализовать шифрование только занятого пространства, MBAM ошибочно шифрует весь диск вместо того, чтобы шифровать использованное место на диске.</span><span class="sxs-lookup"><span data-stu-id="71e60-150">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only Encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="71e60-151">Если на компьютере уже установлено шифрование только с помощью шифрования "занято", а не установлен клиент MBAM, то MBAM распознает этот параметр и сообщит о том, что шифрование правильно используется в отчетах о соответствии.</span><span class="sxs-lookup"><span data-stu-id="71e60-151">If a computer is already encrypted with Used Space Only Encryption before you install the MBAM Client, and you have set the same Used Space Only Encryption Group Policy Object, MBAM recognizes the setting and reports the encryption correctly in the compliance reports.</span></span>

<span data-ttu-id="71e60-152">**Временное решение**: нет.</span><span class="sxs-lookup"><span data-stu-id="71e60-152">**Workaround**: None.</span></span>

### <span data-ttu-id="71e60-153">Неправильное отображение стойкости шифра в отчете о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="71e60-153">Cipher strength displays incorrectly in the Computer Compliance report</span></span>

<span data-ttu-id="71e60-154">Если вы не настроили определенную стойкость шифра в разделе **Выбор метода шифрования диска и объекта групповой политики стойкости шифра** , то отчет о соответствии компьютера в топологии Configuration Manager всегда будет отображаться как **неизвестный** для стойкости шифра, даже если стойкость шифра использует значение по умолчанию 128-битного шифрования.</span><span class="sxs-lookup"><span data-stu-id="71e60-154">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager integrated topology always displays **Unknown** for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="71e60-155">В отчете показана правильная стойкость шифра, если в объекте групповой политики указана определенная стойкость шифра.</span><span class="sxs-lookup"><span data-stu-id="71e60-155">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="71e60-156">**Временное решение**: всегда устанавливайте определенную стойкость шифра в разделе **Выбор метода шифрования диска и объекта групповой политики стойкости шифра** .</span><span class="sxs-lookup"><span data-stu-id="71e60-156">**Workaround**: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="71e60-157">При распределении состояния соответствия по типу диска старые данные отображаются после обновления элементов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="71e60-157">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="71e60-158">После того как вы обновите элементы конфигурации MBAM в SystemCenter2012 ConfigurationManager, распределение состояния соответствия по типам дисков на панели мониторинга соответствия требованиям для предприятий BitLocker показывает данные, основанные на данных из старых версий элементов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="71e60-158">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="71e60-159">**Временное решение**: нет.</span><span class="sxs-lookup"><span data-stu-id="71e60-159">**Workaround**: None.</span></span> <span data-ttu-id="71e60-160">Изменение элементов конфигурации MBAM не поддерживается, и отчет может не отображаться должным образом.</span><span class="sxs-lookup"><span data-stu-id="71e60-160">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="71e60-161">Конфигурация усиленной безопасности может привести к тому, что отчеты отображаются неправильно</span><span class="sxs-lookup"><span data-stu-id="71e60-161">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="71e60-162">Если включена конфигурация усиленной безопасности Internet Explorer (ESC), при попытке просмотреть отчеты на сервере MBAM может появиться сообщение об **отказе в доступе** .</span><span class="sxs-lookup"><span data-stu-id="71e60-162">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an **Access Denied** message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="71e60-163">По умолчанию конфигурация усиленной безопасности включена для защиты сервера путем уменьшения уязвимости сервера до возможных атак, которые могут возникать в веб-контенте и сценариях приложений.</span><span class="sxs-lookup"><span data-stu-id="71e60-163">By default, Enhanced Security Configuration is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="71e60-164">**Временное решение**: Если при попытке просмотреть отчеты на сервере MBAM появляется сообщение " **отказано в доступе** ", вы можете настроить объект групповой политики или изменить параметры по умолчанию вручную в своем изображении, чтобы отключить конфигурацию усиленной безопасности.</span><span class="sxs-lookup"><span data-stu-id="71e60-164">**Workaround**: If the **Access Denied** message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="71e60-165">Кроме того, вы можете просматривать отчеты с другого компьютера, на котором не включена конфигурация усиленной безопасности.</span><span class="sxs-lookup"><span data-stu-id="71e60-165">You can also alternatively view the reports from another computer on which Enhanced Security Configuration is not enabled.</span></span>

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> <span data-ttu-id="71e60-166">Установка сервера MBAM завершается сбоем при переходе с SQLServer2008 на SQLServer2012</span><span class="sxs-lookup"><span data-stu-id="71e60-166">MBAM Server installation fails when you upgrade from SQLServer2008 to SQLServer2012</span></span>

<span data-ttu-id="71e60-167">Если вы обновите приложение с SQLServer2008 на SQLServer2012 и попытаетесь установить базу данных соответствия требованиям и аудита или базу данных восстановления, установка завершается сбоем и откатывается назад.</span><span class="sxs-lookup"><span data-stu-id="71e60-167">If you upgrade from SQLServer2008 to SQLServer2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="71e60-168">Эта проблема возникает из-за того, что необходимый файл SQLCMD.exe был удален во время обновления SQLServer и не может быть найден установщиком MBAM.</span><span class="sxs-lookup"><span data-stu-id="71e60-168">The failure occurs because the required SQLCMD.exe file was removed during the SQLServer upgrade, and it cannot be found by the MBAM installer.</span></span> <span data-ttu-id="71e60-169">Строки в файле журнала MSI могут выглядеть примерно следующим образом:</span><span class="sxs-lookup"><span data-stu-id="71e60-169">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="71e60-170">Центр восстановления RunDbInstallScript: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery DB: dbInstance-xxxxxx\\I01RunDbInstallScript DB: sqlScript-c:\\program Files Files\\Microsoft\\Microsoft DB: dbname-Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript \ _Recovery \ _and \ _HardwareRunDbInstallScript восстановления базы данных ЦС: MBAM defaultFileName \ _Recovery \ _and \ _HardwareRunDbInstallScript центра восстановления базы данных ЦС: MBAM-defaultDataPath Центр восстановления I01\\MSSQL\\DATA\\RunDbInstallScript: defaultLogPath-K:\\MSSQL\\MSSQL10. Центр восстановления I01\\MSSQL\\Data\\RunDbInstallScript: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\program Files Files\\Microsoft\\Microsoft, администрирование BitLocker и Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript Recovery DB: Начало работы с базой данных восстановления. После этого файл журнала восстановления для Jet-файла будет находиться в разделе" журнал "базы данных ЦС для восстановления:</span><span class="sxs-lookup"><span data-stu-id="71e60-170">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="71e60-171">Установщик Windows MBAM Server имеет закодированный текст, чтобы найти путь SQLCMD.exe, просматривая строковое значение пути в реестре в разделе HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span><span class="sxs-lookup"><span data-stu-id="71e60-171">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="71e60-172">Ключ по-прежнему отображается во время миграции из SQLServer2008 в SQLServer2012, но путь, на который ссылается значение данных, не содержит SQLCMD.exe файл, так как процесс SQLupgrade удалил файл.</span><span class="sxs-lookup"><span data-stu-id="71e60-172">The key is still present during the migration from SQLServer2008 to SQLServer2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQLupgrade process removed the file.</span></span>

<span data-ttu-id="71e60-173">Временное **решение**: временно переименуйте строковое значение HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup Path на **path \ _OLD**, а затем снова запустите УСТАНОВЩИК Windows на сервере MBAM.</span><span class="sxs-lookup"><span data-stu-id="71e60-173">**Workaround**: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup path string value to **Path\_old**, and then run Windows Installer on the MBAM Server again.</span></span> <span data-ttu-id="71e60-174">После того как установка завершится успешно и создаст базу данных в SQLServer2012, переименуйте **путь \ _OLD** в **путь**.</span><span class="sxs-lookup"><span data-stu-id="71e60-174">When the installation completes successfully and creates the databases in SQLServer2012, rename **Path\_old** to **Path**.</span></span>

## <span data-ttu-id="71e60-175">Исправления и статьи базы знаний для MBAM 2,0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="71e60-175">Hotfixes and Knowledge Base articles for MBAM 2.0 SP1</span></span>


<span data-ttu-id="71e60-176">В этом разделе содержатся исправления и статьи базы знаний для MBAM 2,0 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="71e60-176">This section contains hotfixes and KB articles for MBAM 2.0 SP1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="71e60-177">Статья базы знаний</span><span class="sxs-lookup"><span data-stu-id="71e60-177">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="71e60-178">Title</span><span class="sxs-lookup"><span data-stu-id="71e60-178">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="71e60-179">Ссылка</span><span class="sxs-lookup"><span data-stu-id="71e60-179">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71e60-180">2831166</span><span class="sxs-lookup"><span data-stu-id="71e60-180">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-181">Установка системы администрирования и наблюдения (MBAM 2,0) для Microsoft BitLocker завершается сбоем, если &quot; уже установлены объекты System Center cm&quot;</span><span class="sxs-lookup"><span data-stu-id="71e60-181">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="71e60-182">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-182">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71e60-183">2870849</span><span class="sxs-lookup"><span data-stu-id="71e60-183">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-184">Пользователи не могут получить ключ восстановления BitLocker с помощью портала самообслуживания MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="71e60-184">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="71e60-185">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-185">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71e60-186">2756402</span><span class="sxs-lookup"><span data-stu-id="71e60-186">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-187">Клиент MBAM в описании события не сможет выполнить событие с кодом 4 и кодом ошибки 0x8004100E</span><span class="sxs-lookup"><span data-stu-id="71e60-187">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="71e60-188">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-188">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71e60-189">2620287</span><span class="sxs-lookup"><span data-stu-id="71e60-189">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-190">Сообщение об ошибке "ошибка сервера в"/Reports "приложение" при выборе вкладки "отчеты" в MBAM</span><span class="sxs-lookup"><span data-stu-id="71e60-190">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="71e60-191">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-191">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71e60-192">2639518</span><span class="sxs-lookup"><span data-stu-id="71e60-192">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-193">Ошибка при открытии отчетов о соответствии требованиям предприятия или компьютера в MBAM</span><span class="sxs-lookup"><span data-stu-id="71e60-193">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="71e60-194">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-194">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71e60-195">2620269</span><span class="sxs-lookup"><span data-stu-id="71e60-195">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-196">Корпоративная отчетность MBAM не обновляется</span><span class="sxs-lookup"><span data-stu-id="71e60-196">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="71e60-197">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-197">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71e60-198">2712461</span><span class="sxs-lookup"><span data-stu-id="71e60-198">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-199">Установка MBAM на контроллере домена не поддерживается</span><span class="sxs-lookup"><span data-stu-id="71e60-199">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="71e60-200">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-200">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71e60-201">2876732</span><span class="sxs-lookup"><span data-stu-id="71e60-201">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-202">Сообщение об ошибке с кодом 0x80071a90 во время отдельного процесса или настройки интеграции Configuration Manager для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="71e60-202">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="71e60-203">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-203">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71e60-204">2754259</span><span class="sxs-lookup"><span data-stu-id="71e60-204">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-205">MBAM и безопасная сетевая связь</span><span class="sxs-lookup"><span data-stu-id="71e60-205">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="71e60-206">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-206">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71e60-207">2870842</span><span class="sxs-lookup"><span data-stu-id="71e60-207">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-208">Установка MBAM 2.0 завершается сбоем во время интеграции Configuration Manager с SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="71e60-208">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="71e60-209">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-209">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71e60-210">2668533</span><span class="sxs-lookup"><span data-stu-id="71e60-210">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-211">Установка MBAM завершается сбоем, если неправильно настроена служба SSRS SQL</span><span class="sxs-lookup"><span data-stu-id="71e60-211">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="71e60-212">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-212">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71e60-213">2870847</span><span class="sxs-lookup"><span data-stu-id="71e60-213">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-214">Программа установки MBAM 2,0 завершает работу с &quot; ошибкой при получении параметров роли сервера Configuration Manager для &#39;точки служб Reporting Services&#39; роли&quot;</span><span class="sxs-lookup"><span data-stu-id="71e60-214">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="71e60-215">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-215">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71e60-216">2870839</span><span class="sxs-lookup"><span data-stu-id="71e60-216">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-217">Корпоративные отчеты MBAM 2.0 не обновляются в автономной топологии MBAM 2.0 из-за сбоя в работе CreateCache задания SQL</span><span class="sxs-lookup"><span data-stu-id="71e60-217">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="71e60-218">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-218">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71e60-219">2620269</span><span class="sxs-lookup"><span data-stu-id="71e60-219">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-220">Корпоративная отчетность MBAM не обновляется</span><span class="sxs-lookup"><span data-stu-id="71e60-220">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="71e60-221">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-221">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71e60-222">2935997</span><span class="sxs-lookup"><span data-stu-id="71e60-222">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-223">MBAM поддерживаемые компьютеры с неправильными отчетами о соответствия требованиям включают Неподдерживаемые продукты</span><span class="sxs-lookup"><span data-stu-id="71e60-223">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="71e60-224">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-224">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71e60-225">2612822</span><span class="sxs-lookup"><span data-stu-id="71e60-225">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="71e60-226">Запись компьютера отклонена в MBAM</span><span class="sxs-lookup"><span data-stu-id="71e60-226">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="71e60-227">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="71e60-227">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="71e60-228">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="71e60-228">Related topics</span></span>


[<span data-ttu-id="71e60-229">Сведения о MBAM 2.0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="71e60-229">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)

 

 





