---
title: Заметки о выпуске для MBAM 2.5
description: Заметки о выпуске для MBAM 2.5
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824982"
---
# <span data-ttu-id="71af9-103">Заметки о выпуске для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="71af9-103">Release Notes for MBAM 2.5</span></span>


<span data-ttu-id="71af9-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="71af9-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="71af9-105">Внимательно прочтите эти заметки о выпуске, прежде чем устанавливать администрирование и мониторинг Microsoft BitLocker (MBAM) 2,5.</span><span class="sxs-lookup"><span data-stu-id="71af9-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5.</span></span> <span data-ttu-id="71af9-106">Эти заметки о выпуске содержат сведения, необходимые для успешной установки MBAM и могут содержать сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="71af9-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="71af9-107">Если эти заметки о выпуске отличаются от других 2,5 MBAMных документов, вы можете внести в полномочные изменения.</span><span class="sxs-lookup"><span data-stu-id="71af9-107">If these release notes differ from other MBAM 2.5 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="71af9-108">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="71af9-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-known-issues"></a> <span data-ttu-id="71af9-109">Известные проблемы с MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="71af9-109">MBAM 2.5 known issues</span></span>


<span data-ttu-id="71af9-110">В этом разделе содержатся заметки о выпуске для MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="71af9-110">This section contains release notes for MBAM 2.5.</span></span>

### <span data-ttu-id="71af9-111">Веб-браузер непреднамеренно запущен от имени администратора</span><span class="sxs-lookup"><span data-stu-id="71af9-111">Web browser unintentionally run as administrator</span></span>

<span data-ttu-id="71af9-112">Ссылки на справочные материалы в средстве настройки сервера MBAM могут привести к тому, что окна браузера будут открываться с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="71af9-112">Help links in the MBAM Server Configuration tool can cause browser windows to open with administrator rights.</span></span>

<span data-ttu-id="71af9-113">**Временное решение:** Включите конфигурацию усиленной безопасности Internet Explorer (IESC) или закройте веб-браузер, прежде чем переходить на другие сайты.</span><span class="sxs-lookup"><span data-stu-id="71af9-113">**Workaround:** Enable Internet Explorer Enhanced Security Configuration (IESC) or close your web browser before navigating to other sites.</span></span>

<span data-ttu-id="71af9-114">**Примечание**  Эта проблема исправлена в MBAM 2,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="71af9-114">**Note** This is fixed in MBAM 2.5 SP1.</span></span>

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> <span data-ttu-id="71af9-115">MBAM отчеты как несовместимые клиенты, зашифрованные с помощью ключей шифрования AES 256-bit и диффузора</span><span class="sxs-lookup"><span data-stu-id="71af9-115">MBAM reports as noncompliant a client encrypted with AES 256-bit encryption keys and Diffuser</span></span>

<span data-ttu-id="71af9-116">Если на компьютере установлено приложение MBAM 2,5 и оно зашифровано с помощью AES 256 bit с стойкость шифра, то клиент MBAM считается несоответствующим в отчетах о соответствии требованиям MBAM.</span><span class="sxs-lookup"><span data-stu-id="71af9-116">If a computer has the MBAM 2.5 client installed and is encrypted by using the AES 256-bit with Diffuser cipher strength, the MBAM client is reported as noncompliant in the MBAM compliance reports.</span></span>

<span data-ttu-id="71af9-117">**Временное решение:** Установите исправление на [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span><span class="sxs-lookup"><span data-stu-id="71af9-117">**Workaround:** Install the hotfix at [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="71af9-118">MBAM не смог зашифровать том и сообщит об ошибке, если установить предохранитель TPM + PIN-код на планшетном устройстве.</span><span class="sxs-lookup"><span data-stu-id="71af9-118">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="71af9-119">Если конечные пользователи пытаются установить предохранитель TPM + PIN-код на планшетном устройстве, MBAM не смог зашифроваться и сообщит об ошибке.</span><span class="sxs-lookup"><span data-stu-id="71af9-119">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="71af9-120">Эта проблема возникает из-за того, что на планшетных устройствах не используется клавиатура с предварительной загрузкой.</span><span class="sxs-lookup"><span data-stu-id="71af9-120">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="71af9-121">**Временное решение:** Включите **использование проверки подлинности BitLocker, требующей предварительной загрузки ввода с клавиатуры для планшетных** ПК.</span><span class="sxs-lookup"><span data-stu-id="71af9-121">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="71af9-122">Этот параметр является параметром групповой политики BitLocker и недоступен в шаблонах групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="71af9-122">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="71af9-123">Имя субъекта-пользователя является обязательным для всех учетных записей служб.</span><span class="sxs-lookup"><span data-stu-id="71af9-123">User principal name is required for all service accounts</span></span>

<span data-ttu-id="71af9-124">Для всех учетных записей служб в MBAM необходимо настроить имя участника-пользователя (UPN).</span><span class="sxs-lookup"><span data-stu-id="71af9-124">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="71af9-125">Если вы не можете создать UPN для учетной записи, в процессе настройки появляется сообщение об ошибке, в котором указано, что пользователь или группа не удается найти в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="71af9-125">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="71af9-126">**Временное решение:** Добавьте имя участника-пользователя в учетную запись службы.</span><span class="sxs-lookup"><span data-stu-id="71af9-126">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="71af9-127">На портале самообслуживания требуется дополнительная настройка, если клиентские компьютеры не могут получить доступ к сети доставки содержимого Microsoft AJAX</span><span class="sxs-lookup"><span data-stu-id="71af9-127">Self-Service Portal requires additional configuration if client computers cannot access Microsoft Ajax Content Delivery Network</span></span>

<span data-ttu-id="71af9-128">Если клиентские компьютеры не имеют доступа к сети доставки содержимого (CDN) Microsoft AJAX, которая предоставляет порталу самообслуживания доступ, необходимый для определенных файлов JavaScript, необходимо настроить портал самообслуживания таким образом, чтобы он ссылался на файлы JavaScript из доступного источника.</span><span class="sxs-lookup"><span data-stu-id="71af9-128">If your client computers do not have access to the Microsoft Ajax Content Delivery Network (CDN), which gives the Self-Service Portal the access that it requires to certain JavaScript files, you must configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span> <span data-ttu-id="71af9-129">Если вы не настраиваете портал самообслуживания, когда клиентские компьютеры не могут получить доступ к сети CDN, отобразится только название компании и учетная запись, под которой вы вошли в систему.</span><span class="sxs-lookup"><span data-stu-id="71af9-129">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which you logged on is displayed.</span></span> <span data-ttu-id="71af9-130">Сообщение об ошибке не отображается.</span><span class="sxs-lookup"><span data-stu-id="71af9-130">No error message appears.</span></span>

<span data-ttu-id="71af9-131">**Временное решение:** Установите MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="71af9-131">**Workaround:** Install MBAM 2.5 SP1.</span></span> <span data-ttu-id="71af9-132">или настройте портал самообслуживания, выполнив следующие инструкции: [Настройка портала самообслуживания, когда клиентские компьютеры не могут получить доступ к сети доставки содержимого Майкрософт](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span><span class="sxs-lookup"><span data-stu-id="71af9-132">or configure the Self-Service Portal by following these instructions: [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>

### <span data-ttu-id="71af9-133">Портал самообслуживания и веб-сайт администрирования и мониторинга не открываются после обновления IIS до .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="71af9-133">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="71af9-134">Когда вы обновляете службы IIS до Microsoft .NET Framework 4,5, портал самообслуживания и веб-сайт администрирования и мониторинга не открываются.</span><span class="sxs-lookup"><span data-stu-id="71af9-134">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="71af9-135">**Временное решение:** [После установки .NET Framework 4,0: "не удалось загрузить тип" System. ServiceModel. Activation. HttpModule ", появится сообщение об ошибке" статья "](https://go.microsoft.com/fwlink/?LinkId=393568).</span><span class="sxs-lookup"><span data-stu-id="71af9-135">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="71af9-136">На веб-сайте администрирования и мониторинга отображается сообщение об ошибке "не удается найти отчет", если отчет не настроен</span><span class="sxs-lookup"><span data-stu-id="71af9-136">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="71af9-137">Если настроить веб-сайт администрирования и мониторинга и попытаться просмотреть отчет, не настраивая предварительно функцию отчетов, сообщение об ошибке указывает на то, что отчет не удается найти.</span><span class="sxs-lookup"><span data-stu-id="71af9-137">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="71af9-138">**Временное решение:** Настройте компонент Reports перед настройкой веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="71af9-138">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="71af9-139">Отчеты на веб-сайте администрирования и мониторинга выводят предупреждение, если протокол SSL не настроен в SSRS</span><span class="sxs-lookup"><span data-stu-id="71af9-139">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="71af9-140">Если для служб SQL Server Reporting Services (SSRS) не настроено использование Secure Socket Layer (SSL), то при настройке сервера MBAM URL-адрес для компонента "отчеты" будет установлен в значение HTTP вместо HTTPS.</span><span class="sxs-lookup"><span data-stu-id="71af9-140">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="71af9-141">Если затем открыть веб-сайт администрирования и наблюдения и выбрать отчет, отобразится следующее сообщение об ошибке: "отображается только безопасное содержимое".</span><span class="sxs-lookup"><span data-stu-id="71af9-141">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="71af9-142">**Временное решение:** Чтобы отобразить отчет, выберите пункт **Показать весь контент**.</span><span class="sxs-lookup"><span data-stu-id="71af9-142">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="71af9-143">Чтобы устранить эту ошибку, перейдите на компьютер MBAM, на котором установлены службы SQL Server Reporting Services, запустите **Диспетчер конфигураций служб Reporting Services**и выберите **URL-адрес Web Service**.</span><span class="sxs-lookup"><span data-stu-id="71af9-143">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="71af9-144">Выберите необходимый SSL-сертификат для сервера, введите соответствующий порт SSL (порт по умолчанию — 443), а затем нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="71af9-144">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="71af9-145">При нажатии кнопки "назад" в отчете сводки соответствия требованиям BitLocker может возникнуть ошибка</span><span class="sxs-lookup"><span data-stu-id="71af9-145">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="71af9-146">При детализации отчета сводки соответствия требованиям BitLocker и нажатии **обратной** ссылки в отчете SSRS может возникать ошибка.</span><span class="sxs-lookup"><span data-stu-id="71af9-146">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="71af9-147">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="71af9-147">**Workaround:** None.</span></span>

### <span data-ttu-id="71af9-148">Шифрование только использованного пространства не работает должным образом</span><span class="sxs-lookup"><span data-stu-id="71af9-148">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="71af9-149">Если после установки клиента MBAM вы зашифруете компьютер в первый раз, и вы настроили параметры групповой политики, чтобы реализовать шифрование только занятого пространства, MBAM неправильно шифрует весь диск вместо того, чтобы шифровать только используемое место на диске.</span><span class="sxs-lookup"><span data-stu-id="71af9-149">If you encrypt a computer for the first time after you install the MBAM Client, and you have configured a Group Policy setting to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="71af9-150">Если компьютер уже зашифрован с использованием пространства только при установке клиента MBAM и вы настроили тот же параметр групповой политики, MBAM сообщает о том, что диск зашифрован правильно, и не пытается повторно зашифровать диск.</span><span class="sxs-lookup"><span data-stu-id="71af9-150">If a computer is already encrypted with Used Space Only when you install the MBAM Client, and you have configured the same Group Policy setting, MBAM reports that the drive is encrypted correctly, and does not try to re-encrypt the drive.</span></span>

<span data-ttu-id="71af9-151">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="71af9-151">**Workaround:** None.</span></span>

### <span data-ttu-id="71af9-152">Неправильное отображение стойкости шифра в отчете о соответствии компьютера BitLocker</span><span class="sxs-lookup"><span data-stu-id="71af9-152">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="71af9-153">Если вы не настроили определенную стойкость шифра в разделе **Выбор метода шифрования диска и объекта групповой политики стойкости шифра** , отчет о соответствии компьютера BitLocker в топологии интеграции Configuration Manager всегда отображается как "неизвестно" для стойкости шифра, даже если стойкость шифра использует значение по умолчанию для 128-битного шифрования.</span><span class="sxs-lookup"><span data-stu-id="71af9-153">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="71af9-154">В отчете показана правильная стойкость шифра, если в объекте групповой политики указана определенная стойкость шифра.</span><span class="sxs-lookup"><span data-stu-id="71af9-154">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="71af9-155">**Временное решение:** Вы всегда можете задать определенную стойкость шифра в разделе **Выбор метода шифрования диска и объекта групповой политики стойкости шифра** .</span><span class="sxs-lookup"><span data-stu-id="71af9-155">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="71af9-156">При распределении состояния соответствия по типу диска старые данные отображаются после обновления элементов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="71af9-156">Compliance Status Distribution by Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="71af9-157">После того как вы обновите элементы конфигурации MBAM в SystemCenter2012 ConfigurationManager, распределение состояния соответствия по типам дисков на панели мониторинга соответствия требованиям для предприятий BitLocker показывает данные, основанные на данных из старых версий элементов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="71af9-157">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="71af9-158">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="71af9-158">**Workaround:** None.</span></span> <span data-ttu-id="71af9-159">Изменение элементов конфигурации MBAM не поддерживается, и отчет может не отображаться должным образом.</span><span class="sxs-lookup"><span data-stu-id="71af9-159">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="71af9-160">Конфигурация усиленной безопасности может привести к тому, что отчеты выводят сообщение об ошибке неправильно</span><span class="sxs-lookup"><span data-stu-id="71af9-160">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="71af9-161">Если включена конфигурация усиленной безопасности Internet Explorer (ESC), при попытке просмотреть отчеты на сервере MBAM может появиться сообщение об ошибке "отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="71af9-161">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="71af9-162">По умолчанию функция ESC включена, чтобы защитить сервер, уменьшая уязвимость сервера для потенциальных атак, которые могут возникать в результате веб-содержимого и сценариев приложений.</span><span class="sxs-lookup"><span data-stu-id="71af9-162">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="71af9-163">**Временное решение:** Если при попытке просмотреть отчеты на сервере MBAM появляется сообщение об ошибке "отказано в доступе", вы можете настроить объект групповой политики или вручную изменить параметры по умолчанию на своем изображении, чтобы отключить конфигурацию усиленной безопасности.</span><span class="sxs-lookup"><span data-stu-id="71af9-163">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="71af9-164">Кроме того, вы можете просматривать отчеты с другого компьютера, на котором не включена ESC.</span><span class="sxs-lookup"><span data-stu-id="71af9-164">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a><span data-ttu-id="71af9-165">Исправления и статьи базы знаний для MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="71af9-165">Hotfixes and Knowledge Base articles for MBAM 2.5</span></span>


<span data-ttu-id="71af9-166">В этой таблице перечислены исправления и статьи базы знаний для MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="71af9-166">This table lists the hotfixes and KB articles for MBAM 2.5.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="71af9-167">Статья базы знаний</span><span class="sxs-lookup"><span data-stu-id="71af9-167">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="71af9-168">Title</span><span class="sxs-lookup"><span data-stu-id="71af9-168">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="71af9-169">Ссылка</span><span class="sxs-lookup"><span data-stu-id="71af9-169">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71af9-170">2975636</span><span class="sxs-lookup"><span data-stu-id="71af9-170">2975636</span></span></p></td>
<td align="left"><p><span data-ttu-id="71af9-171">Пакет исправлений 1 для администрирования Microsoft BitLocker и мониторинга 2,5</span><span class="sxs-lookup"><span data-stu-id="71af9-171">Hotfix Package 1 for Microsoft BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)"><span data-ttu-id="71af9-172">support.microsoft.com/kb/2975636/EN-US</span><span class="sxs-lookup"><span data-stu-id="71af9-172">support.microsoft.com/kb/2975636/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71af9-173">3015477</span><span class="sxs-lookup"><span data-stu-id="71af9-173">3015477</span></span></p></td>
<td align="left"><p><span data-ttu-id="71af9-174">Пакет исправлений 2 для администрирования и мониторинга BitLocker 2,5</span><span class="sxs-lookup"><span data-stu-id="71af9-174">Hotfix Package 2 for BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)"><span data-ttu-id="71af9-175">support.microsoft.com/kb/3015477</span><span class="sxs-lookup"><span data-stu-id="71af9-175">support.microsoft.com/kb/3015477</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71af9-176">3011022</span><span class="sxs-lookup"><span data-stu-id="71af9-176">3011022</span></span></p></td>
<td align="left"><p><span data-ttu-id="71af9-177">MBAM 2,5 Установка или Configuration Manager не получает сообщение об ошибке, если имя экземпляра службы SSRS имеет подчеркивание</span><span class="sxs-lookup"><span data-stu-id="71af9-177">MBAM 2.5 installation or Configuration Manager reporting fails if the name of SSRS instance contains an underscore</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)"><span data-ttu-id="71af9-178">support.microsoft.com/kb/3011022/EN-US</span><span class="sxs-lookup"><span data-stu-id="71af9-178">support.microsoft.com/kb/3011022/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71af9-179">2756402</span><span class="sxs-lookup"><span data-stu-id="71af9-179">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="71af9-180">Клиент MBAM в описании события не сможет выполнить событие с кодом 4 и кодом ошибки 0x8004100E</span><span class="sxs-lookup"><span data-stu-id="71af9-180">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="71af9-181">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="71af9-181">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71af9-182">2639518</span><span class="sxs-lookup"><span data-stu-id="71af9-182">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="71af9-183">Ошибка при открытии отчетов о соответствии требованиям предприятия или компьютера в MBAM</span><span class="sxs-lookup"><span data-stu-id="71af9-183">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="71af9-184">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="71af9-184">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71af9-185">2870842</span><span class="sxs-lookup"><span data-stu-id="71af9-185">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="71af9-186">Сбой программы установки MBAM 2,0 во время интеграции Configuration Manager с SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="71af9-186">MBAM 2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="71af9-187">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="71af9-187">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71af9-188">2975472</span><span class="sxs-lookup"><span data-stu-id="71af9-188">2975472</span></span></p></td>
<td align="left"><p><span data-ttu-id="71af9-189">Взаимоблокировки SQL при подключении большого количества клиентов MBAM к базе данных восстановления MBAM</span><span class="sxs-lookup"><span data-stu-id="71af9-189">SQL deadlocks when many MBAM clients connect to the MBAM recovery database</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)"><span data-ttu-id="71af9-190">support.microsoft.com/kb/2975472/EN-US</span><span class="sxs-lookup"><span data-stu-id="71af9-190">support.microsoft.com/kb/2975472/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="71af9-191">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="71af9-191">Related topics</span></span>


[<span data-ttu-id="71af9-192">О программе MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="71af9-192">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="71af9-193">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="71af9-193">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="71af9-194">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="71af9-194">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="71af9-195">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="71af9-195">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





