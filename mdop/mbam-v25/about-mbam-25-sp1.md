---
title: Сведения о программе MBAM 2.5 с пакетом обновления 1 (SP1)
description: Сведения о программе MBAM 2.5 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: 6f12e605-44e6-4646-9c20-aee89c8ff0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 41e47e1561629c00d30b45ad2dcd94f37753af5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823782"
---
# <span data-ttu-id="c3635-103">Сведения о программе MBAM 2.5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="c3635-103">About MBAM 2.5 SP1</span></span>


<span data-ttu-id="c3635-104">MBAM 2,5 с пакетом обновления 1 (SP1) предоставляет упрощенный интерфейс администрирования для шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c3635-104">MBAM 2.5 SP1 provides a simplified administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="c3635-105">BitLocker поддерживает улучшенную защиту от кражи данных и уязвимости данных для потерянных или похищенных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c3635-105">BitLocker offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="c3635-106">BitLocker шифрует все данные, хранящиеся в операционной системе Windows и на дисках и на настроенных дисках данных.</span><span class="sxs-lookup"><span data-stu-id="c3635-106">BitLocker encrypts all data that is stored on the Windows operating system and drives and configured data drives.</span></span>

## <span data-ttu-id="c3635-107">Общие сведения о MBAM</span><span class="sxs-lookup"><span data-stu-id="c3635-107">Overview of MBAM</span></span>


<span data-ttu-id="c3635-108">MBAM 2,5 с пакетом обновления 1 (SP1) обладает следующими возможностями:</span><span class="sxs-lookup"><span data-stu-id="c3635-108">MBAM 2.5 SP1 has the following features:</span></span>

-   <span data-ttu-id="c3635-109">позволяет администраторам автоматизировать процедуру шифрования томов на клиентских компьютерах в организации;</span><span class="sxs-lookup"><span data-stu-id="c3635-109">Enables administrators to automate the process of encrypting volumes on client computers across the enterprise.</span></span>

-   <span data-ttu-id="c3635-110">позволяет специалистам по безопасности быстро определять состояние соответствия требованиям отдельных компьютеров или всей организации;</span><span class="sxs-lookup"><span data-stu-id="c3635-110">Enables security officers to quickly determine the compliance state of individual computers or even of the enterprise itself.</span></span>

-   <span data-ttu-id="c3635-111">обеспечивает возможность централизованного составления отчетности и управления оборудованием с использованием Microsoft System Center Configuration Manager;</span><span class="sxs-lookup"><span data-stu-id="c3635-111">Provides centralized reporting and hardware management with Microsoft System Center Configuration Manager.</span></span>

-   <span data-ttu-id="c3635-112">Сокращает рабочую нагрузку на службу поддержки, чтобы помочь конечным пользователям использовать ПИН-код BitLocker и ключи восстановления.</span><span class="sxs-lookup"><span data-stu-id="c3635-112">Reduces the workload on the Help Desk to assist end users with BitLocker PIN and recovery key requests.</span></span>

-   <span data-ttu-id="c3635-113">позволяет конечным пользователям восстанавливать зашифрованные устройства независимо, используя портал самообслуживания;</span><span class="sxs-lookup"><span data-stu-id="c3635-113">Enables end users to recover encrypted devices independently by using the Self-Service Portal.</span></span>

-   <span data-ttu-id="c3635-114">Позволяет подвергать аудиту безопасности доступ к восстановлению сведений о ключе.</span><span class="sxs-lookup"><span data-stu-id="c3635-114">Enables security officers to easily audit access to recover key information.</span></span>

-   <span data-ttu-id="c3635-115">позволяет пользователям Windows Корпоративная продолжать работать в любом месте, не беспокоясь о защите данных организации;</span><span class="sxs-lookup"><span data-stu-id="c3635-115">Empowers Windows Enterprise users to continue working anywhere with the assurance that their corporate data is protected.</span></span>

<span data-ttu-id="c3635-116">MBAM применяет параметры политики шифрования BitLocker, заданные для Организации, отслеживает соответствие клиентских компьютеров этим политикам и сообщает о состоянии шифрования компьютеров предприятия и индивидуальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="c3635-116">MBAM enforces the BitLocker encryption policy options that you set for your enterprise, monitors the compliance of client computers with those policies, and reports on the encryption status of the enterprise’s and individual’s computers.</span></span> <span data-ttu-id="c3635-117">Кроме того, MBAM позволяет получить доступ к сведениям о ключе восстановления, когда пользователь забыл свой PIN-код или пароль, а также при изменении BIOS или загрузочных записей.</span><span class="sxs-lookup"><span data-stu-id="c3635-117">In addition, MBAM lets you access the recovery key information when users forget their PIN or password, or when their BIOS or boot records change.</span></span>

<span data-ttu-id="c3635-118">Управление BitLocker может заинтересовать следующие группы: MBAM</span><span class="sxs-lookup"><span data-stu-id="c3635-118">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="c3635-119">Администраторы, ИТ-специалисты и руководителей соответствия требованиям, ответственные за обеспечение того, что конфиденциальные данные не будут закрыты без авторизации.</span><span class="sxs-lookup"><span data-stu-id="c3635-119">Administrators, IT security professionals, and compliance officers who are responsible for ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="c3635-120">Администраторы, ответственные за безопасность компьютеров в удаленных и филиалах</span><span class="sxs-lookup"><span data-stu-id="c3635-120">Administrators who are responsible for computer security in remote or branch offices</span></span>

-   <span data-ttu-id="c3635-121">Администраторы, ответственные за клиентские компьютеры под управлением Windows</span><span class="sxs-lookup"><span data-stu-id="c3635-121">Administrators who are responsible for client computers that are running Windows</span></span>

<span data-ttu-id="c3635-122">**Примечание**  BitLocker не подробно описан в этой MBAM документации.</span><span class="sxs-lookup"><span data-stu-id="c3635-122">**Note** BitLocker is not explained in detail in this MBAM documentation.</span></span> <span data-ttu-id="c3635-123">Дополнительные сведения можно найти в разделе [Обзор шифрования диска BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span><span class="sxs-lookup"><span data-stu-id="c3635-123">For more information, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

## <a href="" id="what-s-new-in-mbam-2-5-sp1"></a><span data-ttu-id="c3635-124">Новые возможности MBAM 2,5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="c3635-124">What’s new in MBAM 2.5 SP1</span></span>


<span data-ttu-id="c3635-125">В этом разделе описаны новые возможности в MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="c3635-125">This section describes the new features in MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="c3635-126">Новые поддерживаемые языки для клиента MBAM 2,5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="c3635-126">Newly Supported Languages for the MBAM 2.5 SP1 Client</span></span>

<span data-ttu-id="c3635-127">Следующие дополнительные языки теперь поддерживаются в MBAM 2,5 с пакетом обновления 1 (SP1) только для клиента MBAM, включая портал самообслуживания:</span><span class="sxs-lookup"><span data-stu-id="c3635-127">The following additional languages are now supported in MBAM 2.5 SP1 for the MBAM Client only, including the Self-Service Portal:</span></span>

<span data-ttu-id="c3635-128">Чешский (Чешская Республика) cs-CZ</span><span class="sxs-lookup"><span data-stu-id="c3635-128">Czech (Czech Republic) cs-CZ</span></span>

<span data-ttu-id="c3635-129">Датский (Дания) da-DK</span><span class="sxs-lookup"><span data-stu-id="c3635-129">Danish (Denmark) da-DK</span></span>

<span data-ttu-id="c3635-130">Нидерландский (Нидерланды) nl-NL</span><span class="sxs-lookup"><span data-stu-id="c3635-130">Dutch (Netherlands) nl-NL</span></span>

<span data-ttu-id="c3635-131">Финский (Финляндия) Fi-FI</span><span class="sxs-lookup"><span data-stu-id="c3635-131">Finnish (Finland) fi-FI</span></span>

<span data-ttu-id="c3635-132">Греческий (Греция) Эль-GR</span><span class="sxs-lookup"><span data-stu-id="c3635-132">Greek (Greece) el-GR</span></span>

<span data-ttu-id="c3635-133">Венгерский (Венгрия) hu-HU</span><span class="sxs-lookup"><span data-stu-id="c3635-133">Hungarian (Hungary) hu-HU</span></span>

<span data-ttu-id="c3635-134">Норвежский (букмол, Норвегия) без датаграмм</span><span class="sxs-lookup"><span data-stu-id="c3635-134">Norwegian, Bokmål (Norway) nb-NO</span></span>

<span data-ttu-id="c3635-135">Польский (Польша) PL-PL</span><span class="sxs-lookup"><span data-stu-id="c3635-135">Polish (Poland) pl-PL</span></span>

<span data-ttu-id="c3635-136">Португальский (Португалия), пт</span><span class="sxs-lookup"><span data-stu-id="c3635-136">Portuguese (Portugal) pt-PT</span></span>

<span data-ttu-id="c3635-137">Словацкий (Словакия) sk-SK</span><span class="sxs-lookup"><span data-stu-id="c3635-137">Slovak (Slovakia) sk-SK</span></span>

<span data-ttu-id="c3635-138">Словенский (Словения) SL-SI</span><span class="sxs-lookup"><span data-stu-id="c3635-138">Slovenian (Slovenia) sl-SI</span></span>

<span data-ttu-id="c3635-139">Шведский (Швеция) SV-SE</span><span class="sxs-lookup"><span data-stu-id="c3635-139">Swedish (Sweden) sv-SE</span></span>

<span data-ttu-id="c3635-140">Турецкий (Турция) tr-TR</span><span class="sxs-lookup"><span data-stu-id="c3635-140">Turkish (Turkey) tr-TR</span></span>

<span data-ttu-id="c3635-141">Список всех языков, поддерживаемых клиентом и сервером в MBAM 2,5 и MBAM 2,5 SP1, можно найти в разделе [MBAM 2,5 Поддерживаемые конфигурации](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c3635-141">For a list of all languages supported for client and server in MBAM 2.5 and MBAM 2.5 SP1, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

### <span data-ttu-id="c3635-142">Поддержка в Windows 10</span><span class="sxs-lookup"><span data-stu-id="c3635-142">Support for Windows 10</span></span>

<span data-ttu-id="c3635-143">MBAM 2,5 SP1 добавляет поддержку для Windows 10 и Windows Server 2016 в дополнение к тому же программному обеспечению, которое поддерживается в более ранних версиях MBAM.</span><span class="sxs-lookup"><span data-stu-id="c3635-143">MBAM 2.5 SP1 adds support for Windows 10 and Windows Server 2016, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

<span data-ttu-id="c3635-144">Windows 10 поддерживается как для MBAM 2,5, так и для MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="c3635-144">Windows 10 is supported in both MBAM 2.5 and MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="c3635-145">Поддержка Microsoft SQL Server 2014 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="c3635-145">Support for Microsoft SQL Server 2014 SP1</span></span>

<span data-ttu-id="c3635-146">MBAM 2,5 с пакетом обновления 1 (SP1) добавляет поддержку для Microsoft SQL Server 2014 SP1 в дополнение к тому же программному обеспечению, которое поддерживается в более ранних версиях MBAM.</span><span class="sxs-lookup"><span data-stu-id="c3635-146">MBAM 2.5 SP1 adds support for Microsoft SQL Server 2014 SP1, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

### <span data-ttu-id="c3635-147">MBAM больше не поставляется с отдельным MSI</span><span class="sxs-lookup"><span data-stu-id="c3635-147">MBAM no longer ships with separate MSI</span></span>

<span data-ttu-id="c3635-148">Начиная с MBAM 2,5 с пакетом обновления 1 (SP1), отдельный MSI больше не входит в состав продукта MBAM.</span><span class="sxs-lookup"><span data-stu-id="c3635-148">Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="c3635-149">Тем не менее, вы можете извлечь MSI из исполняемого файла (exe), который входит в состав продукта.</span><span class="sxs-lookup"><span data-stu-id="c3635-149">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

### <span data-ttu-id="c3635-150">MBAM может условно OwnerAuth пароли без владельца TPM</span><span class="sxs-lookup"><span data-stu-id="c3635-150">MBAM can escrow OwnerAuth passwords without owning the TPM</span></span>

<span data-ttu-id="c3635-151">Ранее, если MBAM не владеет TPM, OwnerAuth доверенного платформенного модуля нельзя было полагать на базу данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="c3635-151">Previously, if MBAM did not own the TPM, the TPM OwnerAuth could not be escrowed to the MBAM database.</span></span> <span data-ttu-id="c3635-152">Чтобы настроить MBAM для владельца доверенного платформенного модуля и сохранить пароли, вам пришлось отключить автоматическое предоставление TPM и очистить доверенный платформенный модуль на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="c3635-152">To configure MBAM to own the TPM and to store the passwords, you had to disable TPM auto-provisioning and clear the TPM on the client computer.</span></span>

<span data-ttu-id="c3635-153">В Windows 8 и более новых версиях MBAM 2,5 с пакетом обновления 1 (SP1) может переключать пароли OwnerAuth, не прибегая к TPM.</span><span class="sxs-lookup"><span data-stu-id="c3635-153">In Windows 8 and higher, MBAM 2.5 SP1 can now escrow the OwnerAuth passwords without owning the TPM.</span></span> <span data-ttu-id="c3635-154">Во время запуска службы MBAM запросы о том, владеет ли доверенный платформенный модуль, и, если это так, он запрашивает пароли из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c3635-154">During service startup, MBAM queries to see if the TPM is already owned and if so, it requests the passwords from the operating system.</span></span> <span data-ttu-id="c3635-155">Пароли затем записываются в базу данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="c3635-155">The passwords are then escrowed to the MBAM database.</span></span> <span data-ttu-id="c3635-156">Кроме того, необходимо настроить групповую политику для предотвращения удаления OwnerAuth на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c3635-156">In addition, Group Policy must be set to prevent the OwnerAuth from being deleted locally.</span></span>

<span data-ttu-id="c3635-157">В Windows 7 MBAM должен владеть доверенным платформенным модулем для автоматического депонирования OwnerAuth в базе данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="c3635-157">In Windows 7, MBAM must own the TPM to automatically escrow TPM OwnerAuth information in the MBAM database.</span></span> <span data-ttu-id="c3635-158">Если MBAM не владеет доверенным платформенным модулем и резервной копией Active Directory (AD) доверенного платформенного модуля, вы должны использовать **командлеты импорта данных MBAM Active Directory (AD)** , чтобы скопировать OwnerAuth доверенного платформенного модуля из Active Directory в базу данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="c3635-158">If MBAM does not own the TPM and Active Directory (AD) backup of the TPM is configured through Group Policy, you must use the **MBAM Active Directory (AD) Data Import cmdlets** to copy TPM OwnerAuth from AD into the MBAM database.</span></span> <span data-ttu-id="c3635-159">Это пять новых командлетов PowerShell, которые предварительно заполнили MBAM базы данных с данными о восстановлении тома и владельцами доверенного платформенного модуля, хранящимися в службе каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c3635-159">These are five new PowerShell cmdlets that pre-populate MBAM databases with the Volume recovery and TPM owner information stored in Active Directory.</span></span>

<span data-ttu-id="c3635-160">Дополнительные сведения можно найти в разделе [рекомендации по безопасности в MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).</span><span class="sxs-lookup"><span data-stu-id="c3635-160">For more information, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm).</span></span>

### <span data-ttu-id="c3635-161">MBAM может автоматически разблокировать доверенный платформенный модуль после блокировки</span><span class="sxs-lookup"><span data-stu-id="c3635-161">MBAM can automatically unlock the TPM after a lockout</span></span>

<span data-ttu-id="c3635-162">На компьютерах, использующих доверенный платформенный модуль 1,2, теперь можно настроить MBAM для автоматической разблокировки доверенного платформенного модуля в случае блокировки.</span><span class="sxs-lookup"><span data-stu-id="c3635-162">On computers running TPM 1.2, you can now configure MBAM to automatically unlock the TPM in case of a lockout.</span></span> <span data-ttu-id="c3635-163">Если функция автоматического сброса блокировки доверенного платформенного модуля включена, MBAM может определить, что пользователь заблокирован, и получить пароль OwnerAuth из базы данных MBAM, чтобы автоматически разблокировать доверенный платформенный модуль для пользователя.</span><span class="sxs-lookup"><span data-stu-id="c3635-163">If the TPM lockout auto reset feature is enabled, MBAM can detect that a user is locked out and then get the OwnerAuth password from the MBAM database to automatically unlock the TPM for the user.</span></span>

<span data-ttu-id="c3635-164">Эта функция должна быть включена как на стороне сервера, так и в групповой политике на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="c3635-164">This feature must be enabled on both the server side and in Group Policy on the client side.</span></span> <span data-ttu-id="c3635-165">Дополнительные сведения можно найти в разделе [рекомендации по безопасности в MBAM 2,5](mbam-25-security-considerations.md#bkmk-autounlock).</span><span class="sxs-lookup"><span data-stu-id="c3635-165">For more information, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-autounlock).</span></span>

### <span data-ttu-id="c3635-166">Поддержка предохранителей цифровых паролей BitLocker, совместимых с FIPS</span><span class="sxs-lookup"><span data-stu-id="c3635-166">Support for FIPS-compliant BitLocker numerical password protectors</span></span>

<span data-ttu-id="c3635-167">В MBAM 2.5 добавлена поддержка для FIPS-совместимых ключей восстановления на устройствах с операционной системой Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="c3635-167">In MBAM2.5, support was added for Federal Information Processing Standard (FIPS)-compliant BitLocker recovery keys on devices running the Windows 8.1 operating system.</span></span> <span data-ttu-id="c3635-168">Однако Windows не реализовала ключи восстановления, соответствующие стандарту FIPS, в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c3635-168">However, Windows did not implement FIPS-compliant recovery keys in Windows 7.</span></span> <span data-ttu-id="c3635-169">Следовательно, устройствам Windows 7 и Windows 8 по-прежнему требуется предохранитель агента восстановления данных (DRA) для восстановления.</span><span class="sxs-lookup"><span data-stu-id="c3635-169">Therefore, Windows 7 and Windows 8 devices still required a Data Recovery Agent (DRA) protector for recovery.</span></span>

<span data-ttu-id="c3635-170">У группы Windows есть встроенные в стандарте FIPS ключи восстановления, которые можно получить с помощью исправления, а MBAM 2,5 SP1 также добавил поддержку для них.</span><span class="sxs-lookup"><span data-stu-id="c3635-170">The Windows team has backported FIPS-compliant recovery keys with a hotfix, and MBAM 2.5 SP1 has added support for them as well.</span></span>

<span data-ttu-id="c3635-171">**Примечание**  На клиентских компьютерах с операционной системой Windows8 по-прежнему требуется предохранитель агента DRA, так как это исправление не было проходило до этой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c3635-171">**Note** Client computers that are running the Windows8 operating system still require a DRA protector since the hotfix was not backported to that OS.</span></span> <span data-ttu-id="c3635-172">Чтобы скачать и установить исправление BitLocker для Windows 7 и Windows 8, ознакомьтесь с [пакетом исправлений 2 для администрирования BitLocker и мониторинга 2,5](https://support.microsoft.com/kb/3015477) .</span><span class="sxs-lookup"><span data-stu-id="c3635-172">See [Hotfix Package 2 for BitLocker Administration and Monitoring 2.5](https://support.microsoft.com/kb/3015477) to download and install the BitLocker hotfix for Windows 7 and Windows 8 computers.</span></span> <span data-ttu-id="c3635-173">Сведения о DRA см. в разделе [использование агентов восстановления данных с помощью BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span><span class="sxs-lookup"><span data-stu-id="c3635-173">For information about DRA, see [Using Data Recovery Agents with BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span></span>

 

<span data-ttu-id="c3635-174">Чтобы включить соответствие требованиям FIPS в вашей организации, необходимо настроить параметры групповой политики для федеральной обработки информации (FIPS).</span><span class="sxs-lookup"><span data-stu-id="c3635-174">To enable FIPS compliance in your organization, you must configure the Federal Information Processing Standard (FIPS) Group Policy settings.</span></span> <span data-ttu-id="c3635-175">Инструкции по настройке можно найти в разделе [Параметры групповой политики BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).</span><span class="sxs-lookup"><span data-stu-id="c3635-175">For configuration instructions, see [BitLocker Group Policy Settings](https://go.microsoft.com/fwlink/?LinkId=393560).</span></span>

### <span data-ttu-id="c3635-176">Настройка сообщения о восстановлении перед загрузкой и URL-адреса с помощью нового параметра групповой политики</span><span class="sxs-lookup"><span data-stu-id="c3635-176">Customize pre-boot recovery message and URL with new Group Policy setting</span></span>

<span data-ttu-id="c3635-177">Новый параметр групповой политики, **Настройка сообщения и URL-адрес для восстановления перед загрузкой**, позволяет настроить настраиваемое сообщение для восстановления или указать URL-адрес, который будет отображаться на экране восстановления BitLocker с предварительной загрузкой, если диск ОС заблокирован.</span><span class="sxs-lookup"><span data-stu-id="c3635-177">A new Group Policy setting, **Configure pre-boot recovery message and URL**, lets you configure a custom recovery message or specify a URL that is then displayed on the pre-boot BitLocker recovery screen when the OS drive is locked.</span></span> <span data-ttu-id="c3635-178">Этот параметр доступен только на клиентских компьютерах под управлением Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c3635-178">This setting is only available on client computers running Windows 10.</span></span>

<span data-ttu-id="c3635-179">Если вы включаете этот параметр политики, вы можете выбрать один из следующих параметров для сообщения о восстановлении перед загрузкой:</span><span class="sxs-lookup"><span data-stu-id="c3635-179">If you enable this policy setting, you can you can select one of these options for the pre-boot recovery message:</span></span>

-   <span data-ttu-id="c3635-180">**Использовать настраиваемое сообщение для восстановления**: Выберите этот параметр, чтобы включить настраиваемое сообщение в окно восстановления BitLocker с предварительной загрузкой.</span><span class="sxs-lookup"><span data-stu-id="c3635-180">**Use custom recovery message**: Select this option to include a custom message in the pre-boot BitLocker recovery screen.</span></span>

-   <span data-ttu-id="c3635-181">**Использовать настраиваемый URL-адрес восстановления**: Выберите этот параметр, чтобы заменить URL-адрес по умолчанию, который отображается на экране восстановления BitLocker с предварительной загрузкой.</span><span class="sxs-lookup"><span data-stu-id="c3635-181">**Use custom recovery URL**: Select this option to replace the default URL that is displayed in the pre-boot BitLocker recovery screen.</span></span>

-   <span data-ttu-id="c3635-182">**Использовать сообщение о восстановлении по умолчанию и URL-адрес**: Выберите этот параметр, чтобы отобразить сообщение восстановления BitLocker по умолчанию и URL-адрес на экране восстановления BitLocker с предварительной загрузкой.</span><span class="sxs-lookup"><span data-stu-id="c3635-182">**Use default recovery message and URL**: Select this option to display the default BitLocker recovery message and URL in the pre-boot BitLocker recovery screen.</span></span> <span data-ttu-id="c3635-183">Если вы ранее настроили настраиваемое сообщение или URL-адрес и хотите вернуться к сообщению по умолчанию, необходимо включить эту политику и выбрать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c3635-183">If you previously configured a custom recovery message or URL and want to revert to the default message, you must enable this policy and select this option.</span></span>

<span data-ttu-id="c3635-184">Параметр "Новая групповая политика" находится на следующем узле GPO: **политики конфигурации компьютера** . &gt; **Policies** &gt; **Административные шаблоны** &gt; **компоненты Windows** &gt; **MBAM (Управление BitLocker)** &gt; , **раздел "диск операционной системы**".</span><span class="sxs-lookup"><span data-stu-id="c3635-184">The new Group Policy setting is located in the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)** &gt; **Operating System Drive**.</span></span> <span data-ttu-id="c3635-185">Дополнительные сведения можно найти в разделе [Планирование требований к групповой политике MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c3635-185">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

### <span data-ttu-id="c3635-186">MBAM добавлена поддержка используемого шифрования в пространстве</span><span class="sxs-lookup"><span data-stu-id="c3635-186">MBAM added support for Used Space Encryption</span></span>

<span data-ttu-id="c3635-187">В MBAM 2,5 с пакетом обновления 1 (SP1) Если вы включите использование шифрования пространства с помощью групповой политики BitLocker, клиент MBAM учитывает его.</span><span class="sxs-lookup"><span data-stu-id="c3635-187">In MBAM 2.5 SP1, if you enable Used Space Encryption via BitLocker Group Policy, the MBAM Client honors it.</span></span>

<span data-ttu-id="c3635-188">Этот параметр групповой политики называется **принудительно использовать тип шифрования диска на дисках операционной системы** и находится в следующем узле GPO: **Параметры конфигурации компьютера** , &gt; **шаблоны** , &gt; **компоненты Windows** , &gt; диски операционной системы с **шифрованием диска BitLocker** &gt; **Operating System Drives**.</span><span class="sxs-lookup"><span data-stu-id="c3635-188">This Group Policy setting is called **Enforce drive encryption type on operating system drives** and is located in the following GPO node: **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **BitLocker Drive Encryption** &gt; **Operating System Drives**.</span></span> <span data-ttu-id="c3635-189">Если вы включите эту политику и выбрали тип шифрования " **шифрование только**занятого места", MBAM будет соблюдать политику, и BitLocker забудет только шифровать дисковое пространство, используемое на томе.</span><span class="sxs-lookup"><span data-stu-id="c3635-189">If you enable this policy and select the encryption type as **Used Space Only encryption**, MBAM will honor the policy and BitLocker will only encrypt disk space that is used on the volume.</span></span>

<span data-ttu-id="c3635-190">Дополнительные сведения можно найти в разделе [Планирование требований к групповой политике MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c3635-190">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

### <span data-ttu-id="c3635-191">Поддержка зашифрованных жестких дисков в клиенте MBAM</span><span class="sxs-lookup"><span data-stu-id="c3635-191">MBAM Client support for Encrypted Hard Drives</span></span>

<span data-ttu-id="c3635-192">MBAM поддерживает BitLocker на зашифрованных жестких дисках, отвечающих требованиям к спецификации TCG для Opalis и стандарту IEEE 1667.</span><span class="sxs-lookup"><span data-stu-id="c3635-192">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="c3635-193">Если на этих устройствах включена функция BitLocker, она будет создавать ключи и выполнять функции управления на зашифрованном диске.</span><span class="sxs-lookup"><span data-stu-id="c3635-193">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="c3635-194">Более подробную информацию вы видите на [жестком диске с шифрованием](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c3635-194">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>

### <span data-ttu-id="c3635-195">Настройка делегирования больше не требуется при регистрации SPN</span><span class="sxs-lookup"><span data-stu-id="c3635-195">Delegation configuration no longer required when registering SPNs</span></span>

<span data-ttu-id="c3635-196">Требование о настройке ограниченного делегирования для имен SPN, регистрируемых для учетной записи пула приложений, больше не требуется в MBAM 2,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c3635-196">The requirement to configure constrained delegation for SPNs that you register for the application pool account is no longer necessary in MBAM 2.5 SP1.</span></span> <span data-ttu-id="c3635-197">Тем не менее, она по-прежнему является обязательным требованием для MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="c3635-197">However, it is still a requirement for MBAM 2.5.</span></span>

### <span data-ttu-id="c3635-198">Включение BitLocker с использованием MBAM в рамках развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="c3635-198">Enable BitLocker using MBAM as Part of a Windows Deployment</span></span>

<span data-ttu-id="c3635-199">В MBAM 2,5 с пакетом обновления 1 (SP1) можно использовать сценарий PowerShell для настройки шифрования диска BitLocker и ключей подключы для депонирования на сервер MBAM.</span><span class="sxs-lookup"><span data-stu-id="c3635-199">In MBAM 2.5 SP1, you can use a PowerShell script to configure BitLocker drive encryption and escrow recovery keys to the MBAM Server.</span></span>

<span data-ttu-id="c3635-200">Дополнительные сведения о том, [как включить BitLocker с помощью MBAM, можно](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md) найти в разделе Развертывание Windows</span><span class="sxs-lookup"><span data-stu-id="c3635-200">For more information, see [How to Enable BitLocker by Using MBAM as Part of a Windows Deployment](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)</span></span>

### <span data-ttu-id="c3635-201">Портал самообслуживания можно настроить с помощью PowerShell либо мастера настройки поставщика общих служб.</span><span class="sxs-lookup"><span data-stu-id="c3635-201">Self-Service Portal can be customized by using either PowerShell or the SSP customization wizard</span></span>

<span data-ttu-id="c3635-202">MBAM 2,5 с пакетом обновления 1 (SP1), портал самообслуживания можно настроить с помощью мастера настройки, а также с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c3635-202">As of MBAM 2.5 SP1, the Self-Service Portal can be configured by using the customization wizard as well as by using PowerShell.</span></span> <span data-ttu-id="c3635-203">Узнайте [, как настроить веб-приложения MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="c3635-203">See [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

### <span data-ttu-id="c3635-204">Веб-браузер больше не запускается с правами администратора</span><span class="sxs-lookup"><span data-stu-id="c3635-204">Web browser no longer unintentionally runs as administrator</span></span>

<span data-ttu-id="c3635-205">Ошибка в MBAM 2,5 привела к тому, что ссылки на справку в средстве настройки сервера приводят к открытию окон браузера с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="c3635-205">An issue in MBAM 2.5 caused help links in the Server Configuration tool to cause browser windows to open with administrator rights.</span></span> <span data-ttu-id="c3635-206">Эта проблема исправлена в MBAM 2,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c3635-206">This issue is fixed in MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="c3635-207">Больше не нужно скачивать файлы JavaScript для настройки портала самообслуживания, когда сеть CDN недоступна</span><span class="sxs-lookup"><span data-stu-id="c3635-207">No longer need to download the JavaScript files to configure the Self-Service Portal when the CDN is inaccessible</span></span>

<span data-ttu-id="c3635-208">В MBAM 2,5 и более ранних версиях jQuery-файлы, используемые для настройки портала самообслуживания, пришлось загрузить из сети CDN заранее, если клиенты, обращающиеся к порталу самообслуживания, не имеют доступа к Интернету.</span><span class="sxs-lookup"><span data-stu-id="c3635-208">In MBAM 2.5 and earlier, the jQuery files used for configuration of the Self-Service Portal had to be downloaded from the CDN in advance if clients accessing the Self-Service Portal did not have internet access.</span></span> <span data-ttu-id="c3635-209">В MBAM 2,5 с пакетом обновления 1 (SP1) все файлы JavaScript включены в продукт, поэтому их загрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="c3635-209">In MBAM 2.5 SP1, all JavaScript files are included in the product, so downloading them is unnecessary.</span></span>

### <span data-ttu-id="c3635-210">Отчеты можно открывать в построителе отчетов 3,0</span><span class="sxs-lookup"><span data-stu-id="c3635-210">Reports can be opened in Report Builder 3.0</span></span>

<span data-ttu-id="c3635-211">В MBAM 2,5 с пакетом обновления 1 (SP1) отчеты обновлены до последней схемы языка определения отчетов, позволяя пользователям открывать и настраивать отчеты в построителе отчетов 3,0 и немедленно сохранять их, не нарушая файл отчета.</span><span class="sxs-lookup"><span data-stu-id="c3635-211">In MBAM 2.5 SP1, the reports have been updated to the latest report definition language schema, allowing users to open and customize the reports in Report Builder 3.0 and save them immediately without corrupting the report file.</span></span>

### <span data-ttu-id="c3635-212">Новые командлеты PowerShell</span><span class="sxs-lookup"><span data-stu-id="c3635-212">New PowerShell cmdlets</span></span>

<span data-ttu-id="c3635-213">Новые командлеты PowerShell для MBAM 2,5 с пакетом обновления 1 (SP1) позволяют настраивать и управлять различными функциями MBAM, включая базы данных, отчеты и веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c3635-213">New PowerShell cmdlets for MBAM 2.5 SP1 enable you to configure and manage different MBAM features, including databases, reports, and web applications.</span></span> <span data-ttu-id="c3635-214">Каждый компонент имеет соответствующий командлет PowerShell, который можно использовать для включения или отключения функций, а также для получения сведений о компоненте.</span><span class="sxs-lookup"><span data-stu-id="c3635-214">Each feature has a corresponding PowerShell cmdlet that you can use to enable or disable features, or to get information about the feature.</span></span>

<span data-ttu-id="c3635-215">Для MBAM 2,5 с пакетом обновления 1 (SP1) были реализованы следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="c3635-215">The following cmdlets have been implemented for MBAM 2.5 SP1:</span></span>

-   <span data-ttu-id="c3635-216">Write-MbamTpmInformation</span><span class="sxs-lookup"><span data-stu-id="c3635-216">Write-MbamTpmInformation</span></span>

-   <span data-ttu-id="c3635-217">Write-MbamRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="c3635-217">Write-MbamRecoveryInformation</span></span>

-   <span data-ttu-id="c3635-218">Чтение и ADTpmInformation</span><span class="sxs-lookup"><span data-stu-id="c3635-218">Read-ADTpmInformation</span></span>

-   <span data-ttu-id="c3635-219">Чтение и ADRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="c3635-219">Read-ADRecoveryInformation</span></span>

-   <span data-ttu-id="c3635-220">Write-MbamComputerUser</span><span class="sxs-lookup"><span data-stu-id="c3635-220">Write-MbamComputerUser</span></span>

<span data-ttu-id="c3635-221">В командлетах Enable-MbamWebApplication и Test-MbamWebApplication для MBAM 2,5 с пакетом обновления 1 (SP1) реализованы следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="c3635-221">The following parameters have been implemented in the Enable-MbamWebApplication and Test-MbamWebApplication cmdlets for MBAM 2.5 SP1:</span></span>

-   <span data-ttu-id="c3635-222">DataMigrationAccessGroup</span><span class="sxs-lookup"><span data-stu-id="c3635-222">DataMigrationAccessGroup</span></span>

-   <span data-ttu-id="c3635-223">TpmAutoUnlock</span><span class="sxs-lookup"><span data-stu-id="c3635-223">TpmAutoUnlock</span></span>

<span data-ttu-id="c3635-224">Дополнительные сведения о командлетах можно найти в разделе [вопросы безопасности MBAM 2,5](mbam-25-security-considerations.md) и [Справка по командлетам администрирования и мониторинга Microsoft BitLocker](https://technet.microsoft.com/library/dn720418.aspx).</span><span class="sxs-lookup"><span data-stu-id="c3635-224">For information about the cmdlets, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md) and [Microsoft Bitlocker Administration and Monitoring Cmdlet Help](https://technet.microsoft.com/library/dn720418.aspx).</span></span>

### <span data-ttu-id="c3635-225">Агент MBAM обнаруживает режим презентации</span><span class="sxs-lookup"><span data-stu-id="c3635-225">MBAM agent detects presentation mode</span></span>

<span data-ttu-id="c3635-226">Агент MBAM может определить, когда компьютер находится в режиме презентации, и избегать вызова MBAM пользовательского интерфейса в это время.</span><span class="sxs-lookup"><span data-stu-id="c3635-226">The MBAM agent can detect when the computer is in presentation mode and avoid invoking the MBAM UI at that time.</span></span>

### <span data-ttu-id="c3635-227">Служба агента MBAM теперь настроена на использование отложенного запуска</span><span class="sxs-lookup"><span data-stu-id="c3635-227">MBAM agent service now configured to use delayed start</span></span>

<span data-ttu-id="c3635-228">После установки служба сейчас будет настроена служба агента MBAM на использование отложенного запуска, уменьшая количество времени, затрачиваемого на запуск Windows.</span><span class="sxs-lookup"><span data-stu-id="c3635-228">After installation, the service will now set the MBAM agent service to use delayed start, decreasing the amount of time it takes to start Windows.</span></span>

### <span data-ttu-id="c3635-229">Заблокированные фиксированные тома данных теперь сообщаются как соответствующие требованиям</span><span class="sxs-lookup"><span data-stu-id="c3635-229">Locked Fixed Data volumes now report as Compliant</span></span>

<span data-ttu-id="c3635-230">Логика расчета соответствия для томов с заблокированными фиксированными данными была изменена, чтобы сообщить о том, что они соответствуют требованиям, но с состоянием предохранителя и состоянием шифрования "неизвестно", а также со сведениями о соответствии соответствия требованиям "том заблокирован".</span><span class="sxs-lookup"><span data-stu-id="c3635-230">The compliance calculation logic for "Locked Fixed Data" volumes has been changed to report the volumes as "Compliant," but with a Protector State and Encryption State of "Unknown" and with a Compliance Status Detail of "Volume is locked".</span></span> <span data-ttu-id="c3635-231">Ранее заблокированные тома были зарегистрированы как несоответствующие требованиям, состоянием предохранителя "encrypted", состоянием шифрования "неизвестно" и состоянием соответствия требованиям "Неизвестная ошибка".</span><span class="sxs-lookup"><span data-stu-id="c3635-231">Previously, locked volumes were reported as “Non-Compliant”, a Protector State of "Encrypted", an Encryption State of "Unknown", and a Compliance Status Detail of "An unknown error".</span></span>


## <span data-ttu-id="c3635-232">Получение технологий для MDOP</span><span class="sxs-lookup"><span data-stu-id="c3635-232">How to Get MDOP Technologies</span></span>


<span data-ttu-id="c3635-233">MBAM является частью пакета оптимизации рабочего стола Майкрософт (MDOP).</span><span class="sxs-lookup"><span data-stu-id="c3635-233">MBAM is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="c3635-234">MDOP является частью программы Software Assurance (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="c3635-234">MDOP is part of the Microsoft Software Assurance program.</span></span> <span data-ttu-id="c3635-235">Дополнительные сведения о программе Microsoft Software Assurance и о том, как приобрести MDOP, приведены в [статье как получить MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="c3635-235">For more information about the Microsoft Software Assurance program and how to acquire the MDOP, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="c3635-236">Заметки о выпуске MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="c3635-236">MBAM 2.5 SP1 Release Notes</span></span>


<span data-ttu-id="c3635-237">Дополнительные сведения и последние новости, не включенные в эту документацию, можно найти в статье [заметки о выпуске MBAM 2,5 SP1](release-notes-for-mbam-25-sp1.md).</span><span class="sxs-lookup"><span data-stu-id="c3635-237">For more information and late-breaking news that is not included in this documentation, see [Release Notes for MBAM 2.5 SP1](release-notes-for-mbam-25-sp1.md).</span></span>

## <span data-ttu-id="c3635-238">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="c3635-238">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="c3635-239">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="c3635-239">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="c3635-240">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="c3635-240">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="c3635-241">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c3635-241">Related topics</span></span>


[<span data-ttu-id="c3635-242">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="c3635-242">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="c3635-243">Начало работы с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c3635-243">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

 

 





