---
title: Процедуры безопасности MBAM 2.5
description: Процедуры безопасности MBAM 2.5
author: dansimp
ms.assetid: f6613c63-b32b-45fb-a6e8-673d6dae7d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 86a756ab6f983fa1f22de6835b5993e1215d1dbe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826839"
---
# <span data-ttu-id="648e9-103">Процедуры безопасности MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="648e9-103">MBAM 2.5 Security Considerations</span></span>


<span data-ttu-id="648e9-104">В этой статье приведены сведения о том, как защитить администрирование и мониторинг Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="648e9-104">This topic contains the following information about how to secure Microsoft BitLocker Administration and Monitoring (MBAM):</span></span>

-   [<span data-ttu-id="648e9-105">Настройка MBAM для депонирования доверенного платформенного модуля и хранения паролей OwnerAuth</span><span class="sxs-lookup"><span data-stu-id="648e9-105">Configure MBAM to escrow the TPM and store OwnerAuth passwords</span></span>](#bkmk-tpm)

-   [<span data-ttu-id="648e9-106">Настройка MBAM для автоматической разблокировки доверенного платформенного модуля после блокировки</span><span class="sxs-lookup"><span data-stu-id="648e9-106">Configure MBAM to automatically unlock the TPM after a lockout</span></span>](#bkmk-autounlock)

-   [<span data-ttu-id="648e9-107">Безопасные соединения с SQL Server</span><span class="sxs-lookup"><span data-stu-id="648e9-107">Secure connections to SQL Server</span></span>](#bkmk-secure-databases)

-   [<span data-ttu-id="648e9-108">Создание учетных записей и групп</span><span class="sxs-lookup"><span data-stu-id="648e9-108">Create accounts and groups</span></span>](#bkmk-accts-groups)

-   [<span data-ttu-id="648e9-109">Использование файлов журнала MBAM</span><span class="sxs-lookup"><span data-stu-id="648e9-109">Use MBAM log files</span></span>](#bkmk-logfiles)

-   [<span data-ttu-id="648e9-110">Рассмотрение вопросов, которые следует учитывать при TDEии базы данных MBAM</span><span class="sxs-lookup"><span data-stu-id="648e9-110">Review MBAM database TDE considerations</span></span>](#bkmk-tde)

-   [<span data-ttu-id="648e9-111">Общие сведения о вопросах безопасности</span><span class="sxs-lookup"><span data-stu-id="648e9-111">Understand general security considerations</span></span>](#bkmk-general-security)

## <a href="" id="bkmk-tpm"></a><span data-ttu-id="648e9-112">Настройка MBAM для депонирования доверенного платформенного модуля и хранения паролей OwnerAuth</span><span class="sxs-lookup"><span data-stu-id="648e9-112">Configure MBAM to escrow the TPM and store OwnerAuth passwords</span></span>

<span data-ttu-id="648e9-113">**Примечание** В Windows 10 версии 1607 или более поздней права собственности на этот доверенный платформенный модуль могут получить только Windows.</span><span class="sxs-lookup"><span data-stu-id="648e9-113">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="648e9-114">Кроме того, Windows не сохранит пароль владельца доверенного платформенного модуля при подготовке доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="648e9-114">In addition, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="648e9-115">Дополнительные сведения приведены в разделе [пароль владельца доверенного платформенного модуля](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .</span><span class="sxs-lookup"><span data-stu-id="648e9-115">See [TPM owner password](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

<span data-ttu-id="648e9-116">В зависимости от конфигурации доверенный платформенный модуль (TPM) сам блокирует себя в некоторых ситуациях ─ (например, при вводе слишком большого количества недопустимых паролей ─) и может оставаться заблокированным в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="648e9-116">Depending on its configuration, the Trusted Platform Module (TPM) will lock itself in certain situations ─ such as when too many incorrect passwords are entered ─ and can remain locked for a period of time.</span></span> <span data-ttu-id="648e9-117">При блокировке доверенного платформенного модуля BitLocker не может получить доступ к ключам шифрования для выполнения операций разблокировки и расшифровки, требуя от пользователя ввода ключа восстановления BitLocker для доступа к диску операционной системы.</span><span class="sxs-lookup"><span data-stu-id="648e9-117">During TPM lockout, BitLocker cannot access the encryption keys to perform unlock or decryption operations, requiring the user to enter their BitLocker recovery key to access the operating system drive.</span></span> <span data-ttu-id="648e9-118">Чтобы сбросить блокировку доверенного платформенного модуля, необходимо предоставить пароль OwnerAuth доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="648e9-118">To reset TPM lockout, you must provide the TPM OwnerAuth password.</span></span>

<span data-ttu-id="648e9-119">MBAM может хранить пароль OwnerAuth доверенного платформенного модуля в базе данных MBAM, если он владеет доверенным платформенным модулем или его пароль.</span><span class="sxs-lookup"><span data-stu-id="648e9-119">MBAM can store the TPM OwnerAuth password in the MBAM database if it owns the TPM or if it escrows the password.</span></span> <span data-ttu-id="648e9-120">После этого на веб-сайте администрирования и мониторинга OwnerAuth пароли легко доступны для восстановления из блокировки доверенного платформенного модуля, что устраняет необходимость дождаться разрешения блокировки.</span><span class="sxs-lookup"><span data-stu-id="648e9-120">OwnerAuth passwords are then easily accessible on the Administration and Monitoring Website when you must recover from a TPM lockout, eliminating the need to wait for the lockout to resolve on its own.</span></span>

### <span data-ttu-id="648e9-121">Депонирование OwnerAuth TPM в Windows 8 и более новых версиях</span><span class="sxs-lookup"><span data-stu-id="648e9-121">Escrowing TPM OwnerAuth in Windows 8 and higher</span></span>

<span data-ttu-id="648e9-122">**Примечание** В Windows 10 версии 1607 или более поздней права собственности на этот доверенный платформенный модуль могут получить только Windows.</span><span class="sxs-lookup"><span data-stu-id="648e9-122">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="648e9-123">В addiiton при подготовке доверенного платформенного модуля Windows не сохранит пароль владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="648e9-123">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="648e9-124">Дополнительные сведения приведены в разделе [пароль владельца доверенного платформенного модуля](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .</span><span class="sxs-lookup"><span data-stu-id="648e9-124">See [TPM owner password](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

<span data-ttu-id="648e9-125">В Windows 8 или более новой версия MBAM больше не должна владеть TPM для хранения пароля OwnerAuth, если OwnerAuth доступен на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="648e9-125">In Windows 8 or higher, MBAM no longer must own the TPM to store the OwnerAuth password, as long as the OwnerAuth is available on the local machine.</span></span>

<span data-ttu-id="648e9-126">Чтобы включить MBAM в депонированный и сохранить пароли OwnerAuth доверенного платформенного модуля, необходимо настроить эти параметры групповой политики.</span><span class="sxs-lookup"><span data-stu-id="648e9-126">To enable MBAM to escrow and then store TPM OwnerAuth passwords, you must configure these Group Policy settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="648e9-127">Параметр групповой политики</span><span class="sxs-lookup"><span data-stu-id="648e9-127">Group Policy Setting</span></span></th>
<th align="left"><span data-ttu-id="648e9-128">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="648e9-128">Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="648e9-129">Включение резервного копирования доверенного платформенного модуля в доменные службы Active Directory</span><span class="sxs-lookup"><span data-stu-id="648e9-129">Turn on TPM backup to Active Directory Domain Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="648e9-130">Отключено или не настроено</span><span class="sxs-lookup"><span data-stu-id="648e9-130">Disabled or Not Configured</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="648e9-131">Настройка уровня доступности данных авторизации владельца доверенного платформенного модуля для операционной системы</span><span class="sxs-lookup"><span data-stu-id="648e9-131">Configure the level of TPM owner authorization information available to the operating system</span></span></p></td>
<td align="left"><p><span data-ttu-id="648e9-132">Делегированный/отсутствует или не настроен</span><span class="sxs-lookup"><span data-stu-id="648e9-132">Delegated/None or Not Configured</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="648e9-133">Расположение этих параметров групповой политики является **конфигурацией компьютера** &gt; **шаблоны** &gt; **System** &gt; **служб доверенных платформенных модулей**системы.</span><span class="sxs-lookup"><span data-stu-id="648e9-133">The location of these Group Policy settings is **Computer Configuration** &gt; **Administrative Templates** &gt; **System** &gt; **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="648e9-134">**Примечание**  Windows удаляет OwnerAuth локально после того, как MBAM успешно поменяет эти параметры.</span><span class="sxs-lookup"><span data-stu-id="648e9-134">**Note** Windows removes the OwnerAuth locally after MBAM successfully escrows it with these settings.</span></span>

 

### <span data-ttu-id="648e9-135">Депонирование OwnerAuth TPM в Windows 7</span><span class="sxs-lookup"><span data-stu-id="648e9-135">Escrowing TPM OwnerAuth in Windows 7</span></span>

<span data-ttu-id="648e9-136">В Windows 7 MBAM должен владеть доверенным платформенным модулем для автоматического депонирования OwnerAuth в базе данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-136">In Windows 7, MBAM must own the TPM to automatically escrow TPM OwnerAuth information in the MBAM database.</span></span> <span data-ttu-id="648e9-137">Если MBAM не владеет доверенным платформенным модулем, необходимо использовать командлеты импорта данных MBAM Active Directory (AD), чтобы скопировать OwnerAuth доверенного платформенного модуля из Active Directory в базу данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-137">If MBAM does not own the TPM, you must use the MBAM Active Directory (AD) Data Import cmdlets to copy TPM OwnerAuth from Active Directory into the MBAM database.</span></span>

### <span data-ttu-id="648e9-138">MBAM командлетов импорта данных Active Directory</span><span class="sxs-lookup"><span data-stu-id="648e9-138">MBAM Active Directory Data Import cmdlets</span></span>

<span data-ttu-id="648e9-139">Командлеты импорта данных MBAM Active Directory позволяют получить пакеты ключей восстановления и пароли OwnerAuth, которые хранятся в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="648e9-139">The MBAM Active Directory Data Import cmdlets let you retrieve recovery key packages and OwnerAuth passwords that are stored in Active Directory.</span></span>

<span data-ttu-id="648e9-140">Сервер MBAM 2,5 с пакетом обновления 1 (SP1) поставляется с четырьмя командлетами PowerShell, которые предварительно заполнили MBAM базы данных с данными о восстановлении тома и владельцами TPM, хранящимся в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="648e9-140">The MBAM 2.5 SP1 server ships with four PowerShell cmdlets that pre-populate MBAM databases with the Volume recovery and TPM owner information stored in Active Directory.</span></span>

<span data-ttu-id="648e9-141">Для ключей и пакетов восстановления тома:</span><span class="sxs-lookup"><span data-stu-id="648e9-141">For Volume Recovery keys and packages:</span></span>

-   <span data-ttu-id="648e9-142">Чтение и ADRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="648e9-142">Read-ADRecoveryInformation</span></span>

-   <span data-ttu-id="648e9-143">Write-MbamRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="648e9-143">Write-MbamRecoveryInformation</span></span>

<span data-ttu-id="648e9-144">Для сведений о владельце доверенного платформенного модуля:</span><span class="sxs-lookup"><span data-stu-id="648e9-144">For TPM Owner Information:</span></span>

-   <span data-ttu-id="648e9-145">Чтение и ADTpmInformation</span><span class="sxs-lookup"><span data-stu-id="648e9-145">Read-ADTpmInformation</span></span>

-   <span data-ttu-id="648e9-146">Write-MbamTpmInformation</span><span class="sxs-lookup"><span data-stu-id="648e9-146">Write-MbamTpmInformation</span></span>

<span data-ttu-id="648e9-147">Чтобы связать пользователей с компьютерами, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="648e9-147">For Associating Users to Computers:</span></span>

-   <span data-ttu-id="648e9-148">Write-MbamComputerUser</span><span class="sxs-lookup"><span data-stu-id="648e9-148">Write-MbamComputerUser</span></span>

<span data-ttu-id="648e9-149">Командлеты Read-AD \ \* читают данные из Active Directory.</span><span class="sxs-lookup"><span data-stu-id="648e9-149">The Read-AD\* cmdlets read information from Active Directory.</span></span> <span data-ttu-id="648e9-150">Командлеты Write-MBAM \ \* помещают данные в базы данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-150">The Write-Mbam\* cmdlets push the data into the MBAM databases.</span></span> <span data-ttu-id="648e9-151">Подробные сведения об этих командлетах, включая синтаксис, параметры и примеры, приведены в [справочнике по командлетам для администрирования Microsoft BitLocker и наблюдения за 2,5](https://technet.microsoft.com/library/dn459018.aspx) .</span><span class="sxs-lookup"><span data-stu-id="648e9-151">See [Cmdlet Reference for Microsoft Bitlocker Administration and Monitoring 2.5](https://technet.microsoft.com/library/dn459018.aspx) for detailed information about these cmdlets, including syntax, parameters, and examples.</span></span>

<span data-ttu-id="648e9-152">**Создание ассоциаций пользователей и компьютеров.** Командлеты импорта данных MBAM Active Directory собирают данные из Active Directory и вставляют их в базу данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-152">**Create user-to-computer associations:** The MBAM Active Directory Data Import cmdlets gather information from Active Directory and insert the data into MBAM database.</span></span> <span data-ttu-id="648e9-153">Однако они не связывают пользователей с томами.</span><span class="sxs-lookup"><span data-stu-id="648e9-153">However, they do not associate users to volumes.</span></span> <span data-ttu-id="648e9-154">Вы можете скачать Add-ComputerUser.ps1 сценарий PowerShell для создания ассоциаций пользователей и компьютеров, которые позволят пользователям восстановить доступ к компьютеру с помощью веб-сайта администрирования и мониторинга либо с помощью портала самообслуживания для восстановления.</span><span class="sxs-lookup"><span data-stu-id="648e9-154">You can download the Add-ComputerUser.ps1 PowerShell script to create user-to-machine associations, which let users regain access to a computer through the Administration and Monitoring Website or by using the Self-Service Portal for recovery.</span></span> <span data-ttu-id="648e9-155">Сценарий Add-ComputerUser.ps1 собирает данные из **управляемого** атрибута в Active Directory (AD), владельца объекта в AD или из настраиваемого CSV-файла.</span><span class="sxs-lookup"><span data-stu-id="648e9-155">The Add-ComputerUser.ps1 script gathers data from the **Managed By** attribute in Active Directory (AD), the object owner in AD, or from a custom CSV file.</span></span> <span data-ttu-id="648e9-156">Затем сценарий добавляет обнаруженные пользователи в объект конвейера данных для восстановления, который должен быть передан в MbamRecoveryInformation записи для вставки данных в базу данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="648e9-156">The script then adds the discovered users to the recovery information pipeline object, which must be passed to Write-MbamRecoveryInformation to insert the data into the recovery database.</span></span>

<span data-ttu-id="648e9-157">Скачайте сценарий PowerShell Add-ComputerUser.ps1 из [центра загрузки Майкрософт](https://go.microsoft.com/fwlink/?LinkId=613122).</span><span class="sxs-lookup"><span data-stu-id="648e9-157">Download the Add-ComputerUser.ps1 PowerShell script from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=613122).</span></span>

<span data-ttu-id="648e9-158">Вы можете указать **справку Add-ComputerUser.ps1** , чтобы получить справку по сценарию, в том числе примеры использования командлетов и сценария.</span><span class="sxs-lookup"><span data-stu-id="648e9-158">You can specify **help Add-ComputerUser.ps1** to get help for the script, including examples of how to use the cmdlets and the script.</span></span>

<span data-ttu-id="648e9-159">Для создания ассоциаций пользователей и компьютеров после установки сервера MBAM используйте командлет PowerShell Write-MbamComputerUser.</span><span class="sxs-lookup"><span data-stu-id="648e9-159">To create user-to-computer associations after you have installed the MBAM server, use the Write-MbamComputerUser PowerShell cmdlet.</span></span> <span data-ttu-id="648e9-160">Как и в случае с Add-ComputerUser.ps1 сценария PowerShell, этот командлет позволяет указать пользователей, которые могут использовать портал самообслуживания для получения информации о OwnerAuth доверенного платформенного модуля или паролях восстановления тома для указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="648e9-160">Similar to the Add-ComputerUser.ps1 PowerShell script, this cmdlet lets you specify users that can use the Self-Service Portal to get TPM OwnerAuth information or volume recovery passwords for the specified computer.</span></span>

<span data-ttu-id="648e9-161">**Примечание**  Агент MBAM переопределит сопоставления пользователей и компьютеров, когда компьютер начнет выводить отчет на сервер.</span><span class="sxs-lookup"><span data-stu-id="648e9-161">**Note** The MBAM agent will override user-to-computer associations when that computer begins reporting up to the server.</span></span>

 

<span data-ttu-id="648e9-162">**Необходимые условия:** С помощью командлетов Read-AD \ \* можно получать данные из AD только в том случае, если они работают как учетная запись пользователя с высокой привилегией, например администратор домена, или под учетной записью в пользовательской группе безопасности, которой предоставлен доступ на чтение данных (рекомендуемый вариант).</span><span class="sxs-lookup"><span data-stu-id="648e9-162">**Prerequisites:** The Read-AD\* cmdlets can retrieve information from AD only if they are either run as a highly privileged user account, such as a Domain Administrator, or run as an account in a custom security group granted read access to the information (recommended).</span></span>

<span data-ttu-id="648e9-163">[Руководство по работе с шифрованием диска BitLocker: восстановление зашифрованных томов в доменных службах Active](https://technet.microsoft.com/library/cc771778(WS.10).aspx) Directory предоставляет подробные сведения о создании настраиваемой группы безопасности (или нескольких групп) с правом на чтение сведений о рекламе.</span><span class="sxs-lookup"><span data-stu-id="648e9-163">[BitLocker Drive Encryption Operations Guide: Recovering Encrypted Volumes with AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) provides details about creating a custom security group (or multiple groups) with read access to the AD information.</span></span>

<span data-ttu-id="648e9-164">**MBAM и разрешения на запись веб-службы восстановления и оборудования.** Командлеты Write-MBAM \ \* допускают URL-адрес службы восстановления и оборудования MBAM, который используется для публикации сведений о восстановлении или TPM.</span><span class="sxs-lookup"><span data-stu-id="648e9-164">**MBAM Recovery and Hardware Web Service Write Permissions:** The Write-Mbam\* cmdlets accept the URL of the MBAM Recovery and Hardware Service, used to publish the recovery or TPM information.</span></span> <span data-ttu-id="648e9-165">Обычно только учетная запись службы компьютера домена может взаимодействовать со службой восстановления и оборудования MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-165">Typically, only a domain computer service account can communicate with the MBAM Recovery and Hardware Service.</span></span> <span data-ttu-id="648e9-166">В MBAM 2,5 с пакетом обновления 1 (SP1) можно настроить службу восстановления MBAM и оборудования с помощью группы безопасности DataMigrationAccessGroup, члены которой могут пропустить проверку учетной записи службы компьютера домена.</span><span class="sxs-lookup"><span data-stu-id="648e9-166">In MBAM 2.5 SP1, you can configure the MBAM Recovery and Hardware Service with a security group called DataMigrationAccessGroup whose members are allowed to bypass the domain computer service account check.</span></span> <span data-ttu-id="648e9-167">Командлеты Write-MBAM \ \* должны выполняться от имени пользователя, принадлежащего данной настроенной группе.</span><span class="sxs-lookup"><span data-stu-id="648e9-167">The Write-Mbam\* cmdlets must be run as a user belonging to this configured group.</span></span> <span data-ttu-id="648e9-168">(Кроме того, вы можете задать учетные данные отдельного пользователя в настроенной группе с помощью параметра – Credential в командлетах Write-MBAM \ \*.)</span><span class="sxs-lookup"><span data-stu-id="648e9-168">(Alternatively, the credentials of an individual user in the configured group can be specified by using the –Credential parameter in the Write-Mbam\* cmdlets.)</span></span>

<span data-ttu-id="648e9-169">Настроить MBAM и службу оборудования с именем этой группы безопасности можно одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="648e9-169">You can configure the MBAM Recovery and Hardware Service with the name of this security group in one of these ways:</span></span>

-   <span data-ttu-id="648e9-170">Укажите имя группы безопасности (или отдельного пользователя) в параметре-DataMigrationAccessGroup командлета PowerShell Enable-MbamWebApplication-AgentService.</span><span class="sxs-lookup"><span data-stu-id="648e9-170">Provide the name of the security group (or individual) in the -DataMigrationAccessGroup parameter of the Enable-MbamWebApplication –AgentService Powershell cmdlet.</span></span>

-   <span data-ttu-id="648e9-171">Настройте группу после установки MBAM восстановления и оборудования, изменив файл web.config в &lt; &gt; папке Inetpub \\Microsoft BitLocker Solution\\Recovery и Service\\ оборудования.</span><span class="sxs-lookup"><span data-stu-id="648e9-171">Configure the group after the MBAM Recovery and Hardware Service has been installed by editing the web.config file in the &lt;inetpub&gt;\\Microsoft Bitlocker Management Solution\\Recovery and Hardware Service\\ folder.</span></span>

    ```xml
    <add key="DataMigrationUsersGroupName" value="<groupName>|<empty>" />
    ```

    <span data-ttu-id="648e9-172">где &lt; GroupName &gt; заменяется доменом и именем группы (или отдельным пользователем), которое будет использоваться для миграции данных из Active Directory.</span><span class="sxs-lookup"><span data-stu-id="648e9-172">where &lt;groupName&gt; is replaced with the domain and the group name (or the individual user) that will be used to allow data migration from Active Directory.</span></span>

-   <span data-ttu-id="648e9-173">С помощью редактора конфигурации в диспетчере IIS измените этот appSetting.</span><span class="sxs-lookup"><span data-stu-id="648e9-173">Use the Configuration Editor in IIS Manager to edit this appSetting.</span></span>

<span data-ttu-id="648e9-174">В приведенном ниже примере команда, запускаемая как член группы "ADRecoveryInformation" и "Пользователи миграции данных", будет получать сведения о восстановлении тома с компьютеров в подразделении рабочих станций (OU) в домене contoso.com и записывать их в MBAM с помощью MBAM службы восстановления и оборудования, запущенного на сервере mbam.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="648e9-174">In the following example, the command, when run as a member of both the ADRecoveryInformation group and the Data Migration Users group, will pull the volume recovery information from computers in the WORKSTATIONS organizational unit (OU) in the contoso.com domain and write them to MBAM by using the MBAM Recovery and Hardware Service running on the mbam.contoso.com server.</span></span>

``` syntax
PS C:\> Read-ADRecoveryInformation -Server contoso.com -SearchBase "OU=WORKSTATIONS,DC=CONTOSO,DC=COM" | Write-MbamRecoveryInformation -RecoveryServiceEndPoint "https://mbam.contoso.com/MBAMRecoveryAndHardwareService/CoreService.svc"
```

<span data-ttu-id="648e9-175">\*\*Командлеты Read-AD \ \*\*\* допускают имя или IP-адрес компьютера, на котором размещается сервер службы каталогов Active Directory, для запроса сведений о восстановлении или TPM.</span><span class="sxs-lookup"><span data-stu-id="648e9-175">**Read-AD\* cmdlets** accept the name or IP address of an Active Directory hosting server machine to query for recovery or TPM information.</span></span> <span data-ttu-id="648e9-176">Мы рекомендуем указывать отличительные имена контейнеров Active Directory, в которых объект компьютера находится в качестве значения параметра SearchBase.</span><span class="sxs-lookup"><span data-stu-id="648e9-176">We recommend providing the distinguished names of the AD containers in which the computer object resides as the value of the SearchBase parameter.</span></span> <span data-ttu-id="648e9-177">Если компьютеры хранятся в нескольких подразделениях, командлеты могут допускать входные данные конвейера для выполнения для каждого контейнера.</span><span class="sxs-lookup"><span data-stu-id="648e9-177">If computers are stored across several OUs, the cmdlets can accept pipeline input to run once for each container.</span></span> <span data-ttu-id="648e9-178">Отличительное имя контейнера рекламных объявлений будет выглядеть примерно так, как OU = Machines, DC = contoso, DC = com.</span><span class="sxs-lookup"><span data-stu-id="648e9-178">The distinguished name of an AD container will look similar to OU=Machines,DC=contoso,DC=com.</span></span> <span data-ttu-id="648e9-179">Выполнение поиска, ориентированного на конкретные контейнеры, обеспечивает следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="648e9-179">Performing a search targeted to specific containers provides the following benefits:</span></span>

-   <span data-ttu-id="648e9-180">Уменьшает риск истечения времени ожидания при запросе большого набора данных рекламных объявлений для объектов компьютера.</span><span class="sxs-lookup"><span data-stu-id="648e9-180">Reduces the risk of timeout while querying a large AD dataset for computer objects.</span></span>

-   <span data-ttu-id="648e9-181">Можно опустить OU, содержащие серверы Datacenter или другие классы компьютеров, для которых резервная копия может быть нежелательным или необходимой.</span><span class="sxs-lookup"><span data-stu-id="648e9-181">Can omit OUs containing datacenter servers or other classes of computers for which the backup might not be desired or necessary.</span></span>

<span data-ttu-id="648e9-182">Кроме того, для поиска объектов компьютера по всем контейнерам, которые должны быть в указанном SearchBase или в целом домене, можно задать для параметра – рекурсивный флаг с необязательными SearchBase или без него.</span><span class="sxs-lookup"><span data-stu-id="648e9-182">Another option is to provide the –Recurse flag with or without the optional SearchBase to search for computer objects across all containers under the specified SearchBase or the entire domain respectively.</span></span> <span data-ttu-id="648e9-183">Если вы используете параметр-MaxPageSize, вы также можете использовать для управления объемом локальной и удаленной памяти, необходимой для обслуживания запроса.</span><span class="sxs-lookup"><span data-stu-id="648e9-183">When you use the -Recurse flag, you can also use the -MaxPageSize parameter to control the amount of local and remote memory required to service the query.</span></span>

<span data-ttu-id="648e9-184">Эти командлеты записываются в объекты конвейера типа PsObject.</span><span class="sxs-lookup"><span data-stu-id="648e9-184">These cmdlets write to the pipeline objects of type PsObject.</span></span> <span data-ttu-id="648e9-185">Каждый экземпляр PsObject имеет один ключ восстановления тома или строку владельца доверенного платформенного модуля с соответствующим именем компьютера, меткой времени и другими данными, необходимыми для ее публикации в хранилище данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-185">Each PsObject instance contains a single volume recovery key or TPM owner string with its associated computer name, timestamp, and other information required to publish it to the MBAM data store.</span></span>

<span data-ttu-id="648e9-186">\*\*Командлеты Write-MBAM \ \*\*\* допускают значения параметров сведений о восстановлении из конвейера по имени свойства.</span><span class="sxs-lookup"><span data-stu-id="648e9-186">**Write-Mbam\* cmdlets** accept recovery information parameter values from the pipeline by property name.</span></span> <span data-ttu-id="648e9-187">Это позволяет командлетам Write-MBAM \ \* допускать выходные данные конвейера для командлетов Read-AD (например, Read-ADRecoveryInformation – Server contoso.com — рекурсия | Пишите — MbamRecoveryInformation – RecoveryServiceEndpoint mbam.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="648e9-187">This allows the Write-Mbam\* cmdlets to accept the pipeline output of the Read-AD\* cmdlets (for example, Read-ADRecoveryInformation –Server contoso.com –Recurse | Write-MbamRecoveryInformation –RecoveryServiceEndpoint mbam.contoso.com).</span></span>

<span data-ttu-id="648e9-188">\*\*Командлеты Write-MBAM \ \*\*\* включают необязательные параметры, предоставляющие параметры для обеспечения отказоустойчивости, протоколирования и настройки для WhatIf и подтверждения.</span><span class="sxs-lookup"><span data-stu-id="648e9-188">The **Write-Mbam\* cmdlets** include optional parameters that provide options for fault tolerance, verbose logging, and preferences for WhatIf and Confirm.</span></span>

<span data-ttu-id="648e9-189">\*\*Командлеты Write-MBAM \ \*\*\* также включают дополнительный параметр *времени* , значение которого является объектом **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="648e9-189">The **Write-Mbam\* cmdlets** also include an optional *Time* parameter whose value is a **DateTime** object.</span></span> <span data-ttu-id="648e9-190">Этот объект содержит атрибут *типа* , для которого может быть задано значение `Local` , `UTC` или `Unspecified` .</span><span class="sxs-lookup"><span data-stu-id="648e9-190">This object includes a *Kind* attribute that can be set to `Local`, `UTC`, or `Unspecified`.</span></span> <span data-ttu-id="648e9-191">При заполнении параметра *time* из данных, полученных из службы каталогов Active Directory, время преобразуется в формат UTC, и *этот атрибут этого* свойства устанавливается автоматически `UTC` .</span><span class="sxs-lookup"><span data-stu-id="648e9-191">When the *Time* parameter is populated from data taken from the Active Directory, the time is converted to UTC and this *Kind* attribute is set automatically to `UTC`.</span></span> <span data-ttu-id="648e9-192">Однако при заполнении параметра *time* с помощью другого источника, такого как текстовый файл, необходимо явным образом задать для атрибута *типа* нужное значение.</span><span class="sxs-lookup"><span data-stu-id="648e9-192">However, when populating the *Time* parameter using another source, such as a text file, you must explicitly set the *Kind* attribute to its appropriate value.</span></span>

<span data-ttu-id="648e9-193">**Примечание**  Командлеты для чтения и AD не могут найти учетные записи пользователей, которые представляют пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="648e9-193">**Note** The Read-AD\* cmdlets do not have the ability to discover the user accounts that represent the computer users.</span></span> <span data-ttu-id="648e9-194">Сопоставления учетной записи пользователя необходимы для указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="648e9-194">User account associations are needed for the following:</span></span>

-   <span data-ttu-id="648e9-195">Восстановление паролей и пакетов тома с помощью портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="648e9-195">Users to recover volume passwords/packages by using the Self-Service portal</span></span>

-   <span data-ttu-id="648e9-196">Пользователи, которые не входят в группу безопасности "Расширенные справочные пользователи MBAM" в соответствии с определением во время установки, восстанавливая от имени других пользователей.</span><span class="sxs-lookup"><span data-stu-id="648e9-196">Users who are not in the MBAM Advanced Helpdesk Users security group as defined during installation, recovering on behalf of other users</span></span>

 

## <a href="" id="bkmk-autounlock"></a><span data-ttu-id="648e9-197">Настройка MBAM для автоматической разблокировки доверенного платформенного модуля после блокировки</span><span class="sxs-lookup"><span data-stu-id="648e9-197">Configure MBAM to automatically unlock the TPM after a lockout</span></span>


<span data-ttu-id="648e9-198">Вы можете настроить MBAM 2,5 с пакетом обновления 1 (SP1), чтобы автоматически разблокировать доверенный платформенный модуль в случае блокировки.</span><span class="sxs-lookup"><span data-stu-id="648e9-198">You can configure MBAM 2.5 SP1 to automatically unlock the TPM in case of a lockout.</span></span> <span data-ttu-id="648e9-199">Если функция автоматического сброса блокировки доверенного платформенного модуля включена, MBAM может определить, что пользователь заблокирован, и получить пароль OwnerAuth из базы данных MBAM для автоматической разблокировки доверенного платформенного модуля для пользователя.</span><span class="sxs-lookup"><span data-stu-id="648e9-199">If TPM lockout auto reset is enabled, MBAM can detect that a user is locked out and then get the OwnerAuth password from the MBAM database to automatically unlock the TPM for the user.</span></span> <span data-ttu-id="648e9-200">Функция автоматического сброса блокировки доверенного платформенного модуля доступна только в том случае, если ключ восстановления операционной системы для этого компьютера был получен с помощью портала самообслуживания или веб-сайта администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="648e9-200">TPM lockout auto reset is only available if the OS recovery key for that computer was retrieved by using the Self Service Portal or the Administration and Monitoring Website.</span></span>

<span data-ttu-id="648e9-201">**Важно!**  Чтобы включить Автосброс блокировки доверенного платформенного модуля, необходимо настроить эту функцию как на стороне сервера, так и в групповой политике на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="648e9-201">**Important** To enable TPM lockout auto reset, you must configure this feature on both the server side and in Group Policy on the client side.</span></span>

 

-   <span data-ttu-id="648e9-202">Чтобы включить Автосброс блокировки доверенного платформенного модуля на стороне клиента, настройте параметр групповой политики "Настройка автоматического сброса блокировки доверенного платформенного модуля" в разделе " **Конфигурация компьютера** " " &gt; **шаблоны** &gt; **Windows** для &gt; **MBAM** &gt; **управления клиентами**".</span><span class="sxs-lookup"><span data-stu-id="648e9-202">To enable TPM lockout auto reset on the client side, configure the Group Policy setting "Configure TPM lockout auto reset" located at **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM** &gt; **Client Management**.</span></span>

-   <span data-ttu-id="648e9-203">Чтобы включить функцию автоматического сброса блокировки доверенного платформенного модуля на стороне сервера, вы можете установить флажок "включить Автосброс блокировки доверенного платформенного модуля" в мастере настройки сервера MBAM во время установки.</span><span class="sxs-lookup"><span data-stu-id="648e9-203">To enable TPM lockout auto reset on the server side, you can check "Enable TPM lockout auto reset" in the MBAM Server Configuration wizard during setup.</span></span>

    <span data-ttu-id="648e9-204">Кроме того, вы можете включить функцию автоматического сброса блокировки доверенного платформенного модуля в PowerShell с помощью переключателя "-Автоматический сброс блокировки TPM" во время включения веб-компонента службы агента.</span><span class="sxs-lookup"><span data-stu-id="648e9-204">You can also enable TPM lockout auto reset in PowerShell by specifying the "-TPM lockout auto reset" switch while enabling the agent service web component.</span></span>

<span data-ttu-id="648e9-205">После того как пользователь введет ключ восстановления BitLocker, полученный на портале самообслуживания или на веб-сайте администрирования и мониторинга, агент MBAM определит, блокируется ли доверенный платформенный модуль. Если он заблокирован, он попытается получить OwnerAuth доверенного платформенного модуля для компьютера из базы данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-205">After a user enters the BitLocker recovery key they obtained from the Self Service Portal or the Administration and Monitoring Website, the MBAM agent will determine if the TPM is locked out. If it is locked out, it will attempt to retrieve the TPM OwnerAuth for the computer from the MBAM database.</span></span> <span data-ttu-id="648e9-206">Если доверенный платформенный модуль OwnerAuth успешно получен, он будет использоваться для разблокировки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="648e9-206">If the TPM OwnerAuth is successfully retrieved, it will be used to unlock the TPM.</span></span> <span data-ttu-id="648e9-207">При разблокировании ДОВЕРЕНного платформенного модуля доверенный ПЛАТФОРМЕНный модуль становится полнофункциональным, и пользователю не будет принудительно вводить пароль восстановления во время последующих перезагрузок из блокировки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="648e9-207">Unlocking the TPM makes the TPM fully functional and the user will not be forced to enter the recovery password during subsequent reboots from a TPM lockout.</span></span>

<span data-ttu-id="648e9-208">Функция автоматического сброса блокировки доверенного платформенного модуля отключена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="648e9-208">TPM lockout auto reset is disabled by default.</span></span>

<span data-ttu-id="648e9-209">**Примечание**  Функция автоматического сброса блокировки доверенного платформенного модуля поддерживается только на компьютерах с доверенным платформенным модулем версии 1,2.</span><span class="sxs-lookup"><span data-stu-id="648e9-209">**Note** TPM lockout auto reset is only supported on computers running TPM version 1.2.</span></span> <span data-ttu-id="648e9-210">Доверенный платформенный модуль 2,0 обеспечивает встроенную функцию автоматического сброса блокировки.</span><span class="sxs-lookup"><span data-stu-id="648e9-210">TPM 2.0 provides built-in lockout auto reset functionality.</span></span>

 

<span data-ttu-id="648e9-211">**Отчет аудита восстановления** содержит события, связанные с автоматическим сбросом блокировки ДОВЕРЕНного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="648e9-211">**The Recovery Audit Report** includes events related to TPM lockout auto reset.</span></span> <span data-ttu-id="648e9-212">Если запрос получен из клиента MBAM, чтобы получить пароль OwnerAuth TPM, событие заносится в журнал для указания на восстановление.</span><span class="sxs-lookup"><span data-stu-id="648e9-212">If a request is made from the MBAM client to retrieve a TPM OwnerAuth password, an event is logged to indicate recovery.</span></span> <span data-ttu-id="648e9-213">Записи аудита будут включать следующие события:</span><span class="sxs-lookup"><span data-stu-id="648e9-213">Audit entries will include the following events:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="648e9-214">Вход</span><span class="sxs-lookup"><span data-stu-id="648e9-214">Entry</span></span></th>
<th align="left"><span data-ttu-id="648e9-215">Значение</span><span class="sxs-lookup"><span data-stu-id="648e9-215">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="648e9-216">Источник запросов аудита</span><span class="sxs-lookup"><span data-stu-id="648e9-216">Audit Request Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="648e9-217">Разблокировка доверенного платформенного модуля агента</span><span class="sxs-lookup"><span data-stu-id="648e9-217">Agent TPM unlock</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="648e9-218">Тип ключа</span><span class="sxs-lookup"><span data-stu-id="648e9-218">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="648e9-219">Хеш пароля доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="648e9-219">TPM Password Hash</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="648e9-220">Описание причины</span><span class="sxs-lookup"><span data-stu-id="648e9-220">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="648e9-221">Сброс доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="648e9-221">TPM Reset</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-secure-databases"></a><span data-ttu-id="648e9-222">Безопасные соединения с SQL Server</span><span class="sxs-lookup"><span data-stu-id="648e9-222">Secure connections to SQL Server</span></span>


<span data-ttu-id="648e9-223">В MBAM SQL Server обменивается данными со службами отчетов SQL Server и веб-службами для веб-сайтов администрирования и мониторинга и портала самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="648e9-223">In MBAM, SQL Server communicates with SQL Server Reporting Services and with the web services for the Administration and Monitoring Website and Self-Service Portal.</span></span> <span data-ttu-id="648e9-224">Мы рекомендуем защитить связь с SQL Server.</span><span class="sxs-lookup"><span data-stu-id="648e9-224">We recommend that you secure the communication with SQL Server.</span></span> <span data-ttu-id="648e9-225">Дополнительные сведения можно найти [в разделе Шифрование подключений к SQL Server](https://technet.microsoft.com/library/ms189067.aspx).</span><span class="sxs-lookup"><span data-stu-id="648e9-225">For more information, see [Encrypting Connections to SQL Server](https://technet.microsoft.com/library/ms189067.aspx).</span></span>

<span data-ttu-id="648e9-226">Дополнительные сведения о защите веб-сайтов MBAM можно найти [в разделе Планирование безопасности веб-сайтов MBAM](planning-how-to-secure-the-mbam-websites.md).</span><span class="sxs-lookup"><span data-stu-id="648e9-226">For more information about securing the MBAM websites, see [Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md).</span></span>

## <a href="" id="bkmk-accts-groups"></a><span data-ttu-id="648e9-227">Создание учетных записей и групп</span><span class="sxs-lookup"><span data-stu-id="648e9-227">Create accounts and groups</span></span>


<span data-ttu-id="648e9-228">Рекомендации по управлению учетными записями пользователей — это создание глобальных групп домена и добавление в них учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="648e9-228">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="648e9-229">Описание рекомендуемых учетных записей и групп смотрите в разделе [планирование для групп и учетных записей MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="648e9-229">For a description of the recommended accounts and groups, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

## <a href="" id="bkmk-logfiles"></a><span data-ttu-id="648e9-230">Использование файлов журнала MBAM</span><span class="sxs-lookup"><span data-stu-id="648e9-230">Use MBAM log files</span></span>


<span data-ttu-id="648e9-231">В этом разделе описаны файлы журнала клиентов MBAM Server и MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-231">This section describes the MBAM Server and MBAM Client log files.</span></span>

**<span data-ttu-id="648e9-232">Файлы журнала установки MBAM Server</span><span class="sxs-lookup"><span data-stu-id="648e9-232">MBAM Server Setup log files</span></span>**

<span data-ttu-id="648e9-233">Файл **MBAMServerSetup.exe** создает следующие файлы журнала в папке **% TEMP%** во время установки MBAM:</span><span class="sxs-lookup"><span data-stu-id="648e9-233">The **MBAMServerSetup.exe** file generates the following log files in the user’s **%temp%** folder during the MBAM installation:</span></span>

-   **<span data-ttu-id="648e9-234">Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 числа &gt; . log</span><span class="sxs-lookup"><span data-stu-id="648e9-234">Microsoft\_BitLocker\_Administration\_and\_Monitoring\_&lt;14 numbers&gt;.log</span></span>**

    <span data-ttu-id="648e9-235">Записываются в журнал действия, выполненные во время настройки MBAM и конфигурации компонентов сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-235">Logs the actions taken during the MBAM setup and the MBAM Server feature configuration.</span></span>

-   **<span data-ttu-id="648e9-236">Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 \ _numbers &gt;\_0\_MBAMServer.msi. log</span><span class="sxs-lookup"><span data-stu-id="648e9-236">Microsoft\_BitLocker\_Administration\_and\_Monitoring\_&lt;14\_numbers&gt;\_0\_MBAMServer.msi.log</span></span>**

    <span data-ttu-id="648e9-237">Заносит в журнал дополнительные действия, выполненные во время установки.</span><span class="sxs-lookup"><span data-stu-id="648e9-237">Logs additional action taken during installation.</span></span>

**<span data-ttu-id="648e9-238">Файлы журнала конфигурации сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="648e9-238">MBAM Server Configuration log files</span></span>**

-   **<span data-ttu-id="648e9-239">Журналы приложений и служб/Microsoft Windows/MBAM-Setup</span><span class="sxs-lookup"><span data-stu-id="648e9-239">Applications and Services Logs/Microsoft Windows/MBAM-Setup</span></span>**

    <span data-ttu-id="648e9-240">Заносит в журнал ошибки, возникающие при использовании командлетов Windows PowerShell или мастера настройки сервера MBAM, для настройки функций сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-240">Logs the errors that occur when you are using Windows Powershell cmdlets or the MBAM Server Configuration wizard to configure the MBAM Server features.</span></span>

**<span data-ttu-id="648e9-241">Файлы журнала установки клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="648e9-241">MBAM Client setup log files</span></span>**

-   **<span data-ttu-id="648e9-242">MSI &lt; пять случайных знаков &gt; . log</span><span class="sxs-lookup"><span data-stu-id="648e9-242">MSI&lt;five random characters&gt;.log</span></span>**

    <span data-ttu-id="648e9-243">Записываются в журнал действия, которые выполняются во время установки клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-243">Logs the actions taken during the MBAM Client installation.</span></span>

**<span data-ttu-id="648e9-244">MBAM — файлы журнала веб-сайта</span><span class="sxs-lookup"><span data-stu-id="648e9-244">MBAM-Web log files</span></span>**

-   <span data-ttu-id="648e9-245">Показывает активность из веб-порталов и служб.</span><span class="sxs-lookup"><span data-stu-id="648e9-245">Shows activity from the web portals and services.</span></span>

## <a href="" id="bkmk-tde"></a><span data-ttu-id="648e9-246">Рассмотрение вопросов, которые следует учитывать при TDEии базы данных MBAM</span><span class="sxs-lookup"><span data-stu-id="648e9-246">Review MBAM database TDE considerations</span></span>


<span data-ttu-id="648e9-247">Функция шифрования прозрачных данных (TDE), доступная в SQL Server, является дополнительной установкой для экземпляров базы данных, на которых будут размещаться функции базы данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-247">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host the MBAM database features.</span></span>

<span data-ttu-id="648e9-248">С помощью TDE можно выполнять полное шифрование на уровне базы данных в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="648e9-248">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="648e9-249">TDE — это оптимальный вариант массового шифрования для соответствия требованиям законодательства и корпоративным стандартам безопасности данных.</span><span class="sxs-lookup"><span data-stu-id="648e9-249">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="648e9-250">TDE работает на уровне файлов, что аналогично двум функциям Windows: шифрованной файловой системе (EFS) и шифрованию диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="648e9-250">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption.</span></span> <span data-ttu-id="648e9-251">Обе функции также шифруют данные на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="648e9-251">Both features also encrypt data on the hard drive.</span></span> <span data-ttu-id="648e9-252">TDE не заменяет шифрование на уровне ячейки, EFS и BitLocker.</span><span class="sxs-lookup"><span data-stu-id="648e9-252">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="648e9-253">Если в базе данных включена TDE, все резервные копии шифруются.</span><span class="sxs-lookup"><span data-stu-id="648e9-253">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="648e9-254">Таким образом, чтобы убедиться в том, что сертификат, использовавшийся для защиты ключа шифрования базы данных, должен быть архивирован и поддерживаться с резервной копией базы данных.</span><span class="sxs-lookup"><span data-stu-id="648e9-254">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="648e9-255">Если сертификат (или сертификаты) теряется, данные не будут прочитаны.</span><span class="sxs-lookup"><span data-stu-id="648e9-255">If this certificate (or certificates) is lost, the data will be unreadable.</span></span>

<span data-ttu-id="648e9-256">Создавайте резервные копии сертификата вместе с базой данных.</span><span class="sxs-lookup"><span data-stu-id="648e9-256">Back up the certificate with the database.</span></span> <span data-ttu-id="648e9-257">Каждая резервная копия сертификата должна содержать два файла.</span><span class="sxs-lookup"><span data-stu-id="648e9-257">Each certificate backup should have two files.</span></span> <span data-ttu-id="648e9-258">Оба этих файла должны быть архивированы.</span><span class="sxs-lookup"><span data-stu-id="648e9-258">Both of these files should be archived.</span></span> <span data-ttu-id="648e9-259">В идеале для обеспечения безопасности их следует архивировать отдельно из файла резервной копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="648e9-259">Ideally for security, they should be backed up separately from the database backup file.</span></span> <span data-ttu-id="648e9-260">Вы также можете использовать функцию расширенного управления ключами (Extensible Key Management) (расширенное управление ключами) для хранения и обслуживания ключей, используемых для TDE.</span><span class="sxs-lookup"><span data-stu-id="648e9-260">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys that are used for TDE.</span></span>

<span data-ttu-id="648e9-261">Пример включения TDE для экземпляров базы данных MBAM можно найти в разделе [Общие сведения о шифровании прозрачных данных (TDE)](https://technet.microsoft.com/library/bb934049.aspx).</span><span class="sxs-lookup"><span data-stu-id="648e9-261">For an example of how to enable TDE for MBAM database instances, see [Understanding Transparent Data Encryption (TDE)](https://technet.microsoft.com/library/bb934049.aspx).</span></span>

## <a href="" id="bkmk-general-security"></a><span data-ttu-id="648e9-262">Общие сведения о вопросах безопасности</span><span class="sxs-lookup"><span data-stu-id="648e9-262">Understand general security considerations</span></span>


**<span data-ttu-id="648e9-263">Общие сведения о рисках для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="648e9-263">Understand the security risks.</span></span>** <span data-ttu-id="648e9-264">Наиболее серьезный риск при использовании администрирования Microsoft BitLocker и наблюдение за тем, что его функциональность может получить неавторизованный пользователь, который может затем повторно настроить шифрование диска BitLocker и получить данные ключа шифрования BitLocker на клиентах MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-264">The most serious risk when you use Microsoft BitLocker Administration and Monitoring is that its functionality could be compromised by an unauthorized user who could then reconfigure BitLocker Drive Encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="648e9-265">Тем не менее функция MBAM в течение короткого промежутка времени из-за атаки типа "отказ в обслуживании" обычно не имеет катастрофического воздействия, в отличие от того, например, потери электронной почты или сетевого соединения или Power.</span><span class="sxs-lookup"><span data-stu-id="648e9-265">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, losing e-mail or network communications, or power.</span></span>

<span data-ttu-id="648e9-266">**Физическая защита компьютеров**.</span><span class="sxs-lookup"><span data-stu-id="648e9-266">**Physically secure your computers**.</span></span> <span data-ttu-id="648e9-267">Безопасность не имеет физического уровня безопасности.</span><span class="sxs-lookup"><span data-stu-id="648e9-267">There is no security without physical security.</span></span> <span data-ttu-id="648e9-268">Злоумышленник, которому удается получить доступ к серверу MBAM, может использовать его для атаки на всю клиентскую базу.</span><span class="sxs-lookup"><span data-stu-id="648e9-268">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="648e9-269">Все потенциальные физическая атака должны считаться очень риском и соответствующим образом устранены.</span><span class="sxs-lookup"><span data-stu-id="648e9-269">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="648e9-270">Серверы MBAM должны храниться в надежной серверной комнате с управляемым доступом.</span><span class="sxs-lookup"><span data-stu-id="648e9-270">MBAM Servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="648e9-271">Защитите эти компьютеры, если администраторы не находятся в физическом режиме, с помощью операционной системы и запирания компьютера или защищенной экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="648e9-271">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="648e9-272">**Установка последних обновлений для системы безопасности на всех компьютерах**.</span><span class="sxs-lookup"><span data-stu-id="648e9-272">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="648e9-273">Получайте сведения о новых обновлениях для операционных систем Windows, SQL Server и MBAM, подписавшись на службу уведомлений безопасности на [техническом центре безопасности](https://go.microsoft.com/fwlink/?LinkId=28819).</span><span class="sxs-lookup"><span data-stu-id="648e9-273">Stay informed about new updates for Windows operating systems, SQL Server, and MBAM by subscribing to the Security Notification service at the [Security TechCenter](https://go.microsoft.com/fwlink/?LinkId=28819).</span></span>

<span data-ttu-id="648e9-274">**Используйте надежные пароли и передавайте фразы**.</span><span class="sxs-lookup"><span data-stu-id="648e9-274">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="648e9-275">Всегда используйте надежные пароли с 15 и более символами для всех учетных записей администраторов MBAM.</span><span class="sxs-lookup"><span data-stu-id="648e9-275">Always use strong passwords with 15 or more characters for all MBAM administrator accounts.</span></span> <span data-ttu-id="648e9-276">Никогда не используйте пустые пароли.</span><span class="sxs-lookup"><span data-stu-id="648e9-276">Never use blank passwords.</span></span> <span data-ttu-id="648e9-277">Дополнительные сведения о работе с паролями можно найти в разделе [Политика паролей](https://technet.microsoft.com/library/hh994572.aspx).</span><span class="sxs-lookup"><span data-stu-id="648e9-277">For more information about password concepts, see [Password Policy](https://technet.microsoft.com/library/hh994572.aspx).</span></span>



## <span data-ttu-id="648e9-278">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="648e9-278">Related topics</span></span>


[<span data-ttu-id="648e9-279">Планирование развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="648e9-279">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 
## <span data-ttu-id="648e9-280">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="648e9-280">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="648e9-281">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="648e9-281">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="648e9-282">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="648e9-282">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





