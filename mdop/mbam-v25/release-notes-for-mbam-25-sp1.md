---
title: Заметки о выпуске MBAM 2.5 с пакетом обновления 1 (SP1)
description: Заметки о выпуске MBAM 2.5 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824989"
---
# <span data-ttu-id="4c90d-103">Заметки о выпуске MBAM 2.5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="4c90d-103">Release Notes for MBAM 2.5 SP1</span></span>


<span data-ttu-id="4c90d-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="4c90d-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="4c90d-105">Внимательно прочитайте эти заметки о выпуске, прежде чем устанавливать администрирование и мониторинг Microsoft BitLocker (MBAM) 2,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4c90d-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="4c90d-106">Эти заметки о выпуске содержат сведения, необходимые для успешной установки MBAM и могут содержать сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="4c90d-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="4c90d-107">Если эти заметки о выпуске отличаются от других документов MBAM 2,5 с пакетом обновления 1 (SP1), примите последние изменения в качестве удостоверяющих.</span><span class="sxs-lookup"><span data-stu-id="4c90d-107">If these release notes differ from other MBAM 2.5 SP1 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="4c90d-108">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="4c90d-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> <span data-ttu-id="4c90d-109">Известные проблемы с MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="4c90d-109">MBAM 2.5 SP1 known issues</span></span>


<span data-ttu-id="4c90d-110">В этом разделе содержатся замечания о выпуске MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="4c90d-110">This section contains release notes for MBAM 2.5 SP1.</span></span>

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a><span data-ttu-id="4c90d-111">Командлеты PowerShell Read-AD \ \* не предоставляют отзыв, если пользователь не имеет достаточных прав</span><span class="sxs-lookup"><span data-stu-id="4c90d-111">PowerShell Read-AD\* cmdlets do not provide feedback if user does not have sufficient rights</span></span>

<span data-ttu-id="4c90d-112">Если пользователь пытается использовать командлеты PowerShell Read-AD \ \* для сервера MBAM не имеет прав пользователя на чтение сведений о восстановлении Active Directory или чтении сведений о TPM, командлеты не будут предоставлять пользователю сообщение об ошибке или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="4c90d-112">If a user trying to use the PowerShell Read-AD\* cmdlets for the MBAM Server does not have user rights to read the Active Directory recovery information or to read the TPM information, the cmdlets will not provide the user with any error or warning.</span></span>

<span data-ttu-id="4c90d-113">**Временное решение:** Используйте командлеты PowerShell Read-AD \ \* только в том случае, если у вас есть необходимые права пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c90d-113">**Workaround:** Only use the PowerShell Read-AD\* cmdlets if you have the required user rights.</span></span>

### <span data-ttu-id="4c90d-114">Командлеты миграции MBAM Active Directory (AD) не извлекают сведения о восстановлении тома</span><span class="sxs-lookup"><span data-stu-id="4c90d-114">MBAM Active Directory (AD) Migration cmdlets do not retrieve volume recovery information</span></span>

<span data-ttu-id="4c90d-115">Командлетам миграции MBAM Active Directory (AD) не удается получить сведения о восстановлении тома для компьютеров в организационных подразделениях (OU), если знак косой черты (/) является частью имени подразделения.</span><span class="sxs-lookup"><span data-stu-id="4c90d-115">MBAM Active Directory (AD) Migration cmdlets fail to retrieve volume recovery information for computers in organizational units (OUs) if the forward slash character (/) is part of the OU name.</span></span> <span data-ttu-id="4c90d-116">При возникновении этой ошибки повторяющиеся рекламные объявления завершатся сбоем из-за ошибки конвейера.</span><span class="sxs-lookup"><span data-stu-id="4c90d-116">Repeated AD pulls will fail with a pipeline terminating error when this error is encountered.</span></span>

<span data-ttu-id="4c90d-117">**Технические сведения.** Это сообщение об ошибке появляется при запуске команды:</span><span class="sxs-lookup"><span data-stu-id="4c90d-117">**Technical Details:** You will see this error when running the command:</span></span>

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

<span data-ttu-id="4c90d-118">Кроме того, трассировка стека исключений `Error[0].Exception.StackTrace` будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="4c90d-118">In addition, the Exception stack trace `Error[0].Exception.StackTrace` will look like this:</span></span>

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

<span data-ttu-id="4c90d-119">**Временное решение:** Чтобы решить эту проблему, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="4c90d-119">**Workaround:** Perform one of these tasks to resolve this situation:</span></span>

-   <span data-ttu-id="4c90d-120">Переименуйте подразделение, чтобы удалить символ косой черты, а затем запустите сценарий.</span><span class="sxs-lookup"><span data-stu-id="4c90d-120">Rename the OU to remove the forward slash character and then run the script.</span></span>

-   <span data-ttu-id="4c90d-121">Чтобы исключить из процесса резервного копирования любое проблемное подразделение, найдите список подразделений, имена которых не содержат символа прямой косой черты.</span><span class="sxs-lookup"><span data-stu-id="4c90d-121">To exclude any problematic OU from the backup process, find a list of OUs whose names do not contain the forward slash character.</span></span> <span data-ttu-id="4c90d-122">Выполняйте сценарий в этих подразделениях по одной подразделению за один раз.</span><span class="sxs-lookup"><span data-stu-id="4c90d-122">Run the script on these OUs, one OU at a time.</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="4c90d-123">MBAM не смог зашифровать том и сообщит об ошибке, если установить предохранитель TPM + PIN-код на планшетном устройстве.</span><span class="sxs-lookup"><span data-stu-id="4c90d-123">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="4c90d-124">Если конечные пользователи пытаются установить предохранитель TPM + PIN-код на планшетном устройстве, MBAM не смог зашифроваться и сообщит об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4c90d-124">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="4c90d-125">Эта проблема возникает из-за того, что на планшетных устройствах не используется клавиатура с предварительной загрузкой.</span><span class="sxs-lookup"><span data-stu-id="4c90d-125">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="4c90d-126">**Временное решение:** Включите **использование проверки подлинности BitLocker, требующей предварительной загрузки ввода с клавиатуры для планшетных** ПК.</span><span class="sxs-lookup"><span data-stu-id="4c90d-126">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="4c90d-127">Этот параметр является параметром групповой политики BitLocker и недоступен в шаблонах групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="4c90d-127">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="4c90d-128">Имя субъекта-пользователя является обязательным для всех учетных записей служб.</span><span class="sxs-lookup"><span data-stu-id="4c90d-128">User principal name is required for all service accounts</span></span>

<span data-ttu-id="4c90d-129">Для всех учетных записей служб в MBAM необходимо настроить имя участника-пользователя (UPN).</span><span class="sxs-lookup"><span data-stu-id="4c90d-129">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="4c90d-130">Если вы не можете создать UPN для учетной записи, в процессе настройки появляется сообщение об ошибке, в котором указано, что пользователь или группа не удается найти в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4c90d-130">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="4c90d-131">**Временное решение:** Добавьте имя участника-пользователя в учетную запись службы.</span><span class="sxs-lookup"><span data-stu-id="4c90d-131">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="4c90d-132">Портал самообслуживания и веб-сайт администрирования и мониторинга не открываются после обновления IIS до .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="4c90d-132">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="4c90d-133">Когда вы обновляете службы IIS до Microsoft .NET Framework 4,5, портал самообслуживания и веб-сайт администрирования и мониторинга не открываются.</span><span class="sxs-lookup"><span data-stu-id="4c90d-133">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="4c90d-134">**Временное решение:** [После установки .NET Framework 4,0: "не удалось загрузить тип" System. ServiceModel. Activation. HttpModule ", появится сообщение об ошибке" статья "](https://go.microsoft.com/fwlink/?LinkId=393568).</span><span class="sxs-lookup"><span data-stu-id="4c90d-134">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="4c90d-135">На веб-сайте администрирования и мониторинга отображается сообщение об ошибке "не удается найти отчет", если отчет не настроен</span><span class="sxs-lookup"><span data-stu-id="4c90d-135">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="4c90d-136">Если настроить веб-сайт администрирования и мониторинга и попытаться просмотреть отчет, не настраивая предварительно функцию отчетов, сообщение об ошибке указывает на то, что отчет не удается найти.</span><span class="sxs-lookup"><span data-stu-id="4c90d-136">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="4c90d-137">**Временное решение:** Настройте компонент Reports перед настройкой веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="4c90d-137">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="4c90d-138">Отчеты на веб-сайте администрирования и мониторинга выводят предупреждение, если протокол SSL не настроен в SSRS</span><span class="sxs-lookup"><span data-stu-id="4c90d-138">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="4c90d-139">Если для служб SQL Server Reporting Services (SSRS) не настроено использование Secure Socket Layer (SSL), то при настройке сервера MBAM URL-адрес для компонента "отчеты" будет установлен в значение HTTP вместо HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4c90d-139">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="4c90d-140">Если затем открыть веб-сайт администрирования и наблюдения и выбрать отчет, отобразится следующее сообщение об ошибке: "отображается только безопасное содержимое".</span><span class="sxs-lookup"><span data-stu-id="4c90d-140">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="4c90d-141">**Временное решение:** Чтобы отобразить отчет, выберите пункт **Показать весь контент**.</span><span class="sxs-lookup"><span data-stu-id="4c90d-141">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="4c90d-142">Чтобы устранить эту ошибку, перейдите на компьютер MBAM, на котором установлены службы SQL Server Reporting Services, запустите **Диспетчер конфигураций служб Reporting Services**и выберите **URL-адрес Web Service**.</span><span class="sxs-lookup"><span data-stu-id="4c90d-142">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="4c90d-143">Выберите необходимый SSL-сертификат для сервера, введите соответствующий порт SSL (порт по умолчанию — 443), а затем нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="4c90d-143">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="4c90d-144">При нажатии кнопки "назад" в отчете сводки соответствия требованиям BitLocker может возникнуть ошибка</span><span class="sxs-lookup"><span data-stu-id="4c90d-144">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="4c90d-145">При детализации отчета сводки соответствия требованиям BitLocker и нажатии **обратной** ссылки в отчете SSRS может возникать ошибка.</span><span class="sxs-lookup"><span data-stu-id="4c90d-145">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="4c90d-146">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="4c90d-146">**Workaround:** None.</span></span>

### <span data-ttu-id="4c90d-147">Неправильное отображение стойкости шифра в отчете о соответствии компьютера BitLocker</span><span class="sxs-lookup"><span data-stu-id="4c90d-147">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="4c90d-148">Если вы не настроили определенную стойкость шифра в разделе **Выбор метода шифрования диска и объекта групповой политики стойкости шифра** , отчет о соответствии компьютера BitLocker в топологии интеграции Configuration Manager всегда отображается как "неизвестно" для стойкости шифра, даже если стойкость шифра использует значение по умолчанию для 128-битного шифрования.</span><span class="sxs-lookup"><span data-stu-id="4c90d-148">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="4c90d-149">В отчете показана правильная стойкость шифра, если в объекте групповой политики указана определенная стойкость шифра.</span><span class="sxs-lookup"><span data-stu-id="4c90d-149">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="4c90d-150">**Временное решение:** Вы всегда можете задать определенную стойкость шифра в разделе **Выбор метода шифрования диска и объекта групповой политики стойкости шифра** .</span><span class="sxs-lookup"><span data-stu-id="4c90d-150">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="4c90d-151">При распределении состояния соответствия по типу диска старые данные отображаются после обновления элементов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4c90d-151">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="4c90d-152">После того как вы обновите элементы конфигурации MBAM в SystemCenter2012 ConfigurationManager, распределение состояния соответствия по типам дисков на панели мониторинга соответствия требованиям для предприятий BitLocker показывает данные, основанные на данных из старых версий элементов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4c90d-152">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="4c90d-153">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="4c90d-153">**Workaround:** None.</span></span> <span data-ttu-id="4c90d-154">Изменение элементов конфигурации MBAM не поддерживается, и отчет может не отображаться должным образом.</span><span class="sxs-lookup"><span data-stu-id="4c90d-154">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="4c90d-155">Конфигурация усиленной безопасности может привести к тому, что отчеты выводят сообщение об ошибке неправильно</span><span class="sxs-lookup"><span data-stu-id="4c90d-155">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="4c90d-156">Если включена конфигурация усиленной безопасности Internet Explorer (ESC), при попытке просмотреть отчеты на сервере MBAM может появиться сообщение об ошибке "отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="4c90d-156">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="4c90d-157">По умолчанию функция ESC включена, чтобы защитить сервер, уменьшая уязвимость сервера для потенциальных атак, которые могут возникать в результате веб-содержимого и сценариев приложений.</span><span class="sxs-lookup"><span data-stu-id="4c90d-157">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="4c90d-158">**Временное решение:** Если при попытке просмотреть отчеты на сервере MBAM появляется сообщение об ошибке "отказано в доступе", вы можете настроить объект групповой политики или вручную изменить параметры по умолчанию на своем изображении, чтобы отключить конфигурацию усиленной безопасности.</span><span class="sxs-lookup"><span data-stu-id="4c90d-158">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="4c90d-159">Кроме того, вы можете просматривать отчеты с другого компьютера, на котором не включена ESC.</span><span class="sxs-lookup"><span data-stu-id="4c90d-159">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="4c90d-160">Поддержка алгоритма шифрования BitLocker XTS-AES</span><span class="sxs-lookup"><span data-stu-id="4c90d-160">Support for Bitlocker XTS-AES encryption algorithm</span></span>
<span data-ttu-id="4c90d-161">Поддержка алгоритма шифрования XTS-AES в Windows 10 версии 1511 была добавлена в BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4c90d-161">Bitlocker added support for the XTS-AES encryption algorithm in Windows 10, version 1511.</span></span> <span data-ttu-id="4c90d-162">В HF02, MBAM добавлена поддержка клиента для этого параметра BitLocker и в HF04, была добавлена поддержка на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="4c90d-162">With HF02, MBAM added client support for this Bitlocker option and in HF04, the server-side support was added.</span></span> <span data-ttu-id="4c90d-163">Тем не менее, существует одно известное ограничение:</span><span class="sxs-lookup"><span data-stu-id="4c90d-163">However, there is one known limitation:</span></span>

* <span data-ttu-id="4c90d-164">Пользователи должны использовать одинаковые стойкости шифрования для ОС и тома данных на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4c90d-164">Customers must use the same encryption strength for OS and data volumes on the same machine.</span></span>
<span data-ttu-id="4c90d-165">Если используются разные уровни шифрования, MBAM сообщит о том, что компьютер **не соответствует требованиям**.</span><span class="sxs-lookup"><span data-stu-id="4c90d-165">If different encryption strengths are used, MBAM will report the machine as **non-compliant**.</span></span>

### <span data-ttu-id="4c90d-166">Портал самообслуживания автоматически добавляет "-" для идентификатора ключа</span><span class="sxs-lookup"><span data-stu-id="4c90d-166">Self-Service Portal automatically adds "-" on Key ID entry</span></span>
<span data-ttu-id="4c90d-167">По мере HF02 портал самообслуживания MBAM автоматически добавляет элемент "-" в качестве идентификатора ключа.</span><span class="sxs-lookup"><span data-stu-id="4c90d-167">As of HF02, the MBAM Self-Service Portal automatically adds the '-' on Key ID entry.</span></span>  
<span data-ttu-id="4c90d-168">**Примечание.** Чтобы JavaScript вступил в силу, необходимо перенастроить сервер.</span><span class="sxs-lookup"><span data-stu-id="4c90d-168">**Note:** The Server has to be reconfigured for the Javascript to take effect.</span></span>

### <span data-ttu-id="4c90d-169">Отчеты MBAM 2,5 SP1 не работают и отображаются неправильно</span><span class="sxs-lookup"><span data-stu-id="4c90d-169">MBAM 2.5 Sp1 Reports does not work / render properly</span></span>
<span data-ttu-id="4c90d-170">Страница "отчеты" не отображается должным образом при размещении служб SSRS на сервере SQL Server 2016 Edition.</span><span class="sxs-lookup"><span data-stu-id="4c90d-170">Reports Page does not render properly when SSRS is hosted on SQL Server 2016 edition.</span></span> 
<span data-ttu-id="4c90d-171">Например, просмотр службы поддержки — выбор пункта "отчеты" ("x") Digging дальше с помощью Fiddler — она будет выглядеть так, как если бы мы щелкать по отчетам — она вызывает страницу SSRS в формате HTML 4,0.</span><span class="sxs-lookup"><span data-stu-id="4c90d-171">For example – Browsing to Helpdesk – Clicking on Reports – ( Highlighted portion have “x” on it ) Digging this further with Fiddler – it does look like once we click on Reports – it calls the SSRS page with HTML 4.0 rendering format.</span></span>

<span data-ttu-id="4c90d-172">**Временное решение:** Взгляд на сайт. Главный код и замечено, что режим X-UA был определен как IE8.</span><span class="sxs-lookup"><span data-stu-id="4c90d-172">**Workaround:** Looking at the site.master code and noticed the X-UA mode was dictated as IE8.</span></span> <span data-ttu-id="4c90d-173">Так как IE8 — до окончания жизненного цикла, а клиент использует IE11.</span><span class="sxs-lookup"><span data-stu-id="4c90d-173">As IE8 is WAY past the end of life, and customer is using IE11.</span></span> <span data-ttu-id="4c90d-174">Обновите параметр, указав приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="4c90d-174">Update the setting to the below code.</span></span> <span data-ttu-id="4c90d-175">Это позволяет сайту использовать технологии рендеринга IE11</span><span class="sxs-lookup"><span data-stu-id="4c90d-175">This allows the site to utilize IE11 rendering technologies</span></span>

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

<span data-ttu-id="4c90d-176">Первоначальный параметр:</span><span class="sxs-lookup"><span data-stu-id="4c90d-176">Original setting is:</span></span> 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


<span data-ttu-id="4c90d-177">Это причина, по которой проблема не наблюдалась в других браузерах, таких как Chrome, Firefox и т. д.</span><span class="sxs-lookup"><span data-stu-id="4c90d-177">This is the reason why the issue was not seen with other browsers like Chrome, Firefox etc.</span></span>



## <span data-ttu-id="4c90d-178">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4c90d-178">Related topics</span></span>


[<span data-ttu-id="4c90d-179">О программе MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4c90d-179">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="4c90d-180">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="4c90d-180">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4c90d-181">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="4c90d-181">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4c90d-182">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4c90d-182">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





