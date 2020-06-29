---
title: Сведения о MBAM 2.0
description: Сведения о MBAM 2.0
author: dansimp
ms.assetid: b43a0ba9-1c83-4854-a2c5-14eea0070e36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7bdf24d1f375dd1fa8b18ac90c2fc49d2887c6c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824319"
---
# <span data-ttu-id="16cb6-103">Сведения о MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="16cb6-103">About MBAM 2.0</span></span>


<span data-ttu-id="16cb6-104">Microsoft BitLockerAdministration и мониторинг (MBAM) 2.0 — это упрощенный интерфейс администрирования для шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="16cb6-104">Microsoft BitLockerAdministration and Monitoring(MBAM)2.0 provides a simplified administrative interface to BitLocker drive encryption.</span></span> <span data-ttu-id="16cb6-105">BitLocker поддерживает улучшенную защиту от кражи данных и уязвимости данных для потерянных или похищенных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="16cb6-105">BitLocker offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="16cb6-106">BitLocker шифрует все данные, хранящиеся на томе операционной системы Windows и настроенные тома данных.</span><span class="sxs-lookup"><span data-stu-id="16cb6-106">BitLocker encrypts all data that is stored on the Windows operating system volume and configured data volumes.</span></span>

## <span data-ttu-id="16cb6-107">Сведения о MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="16cb6-107">About MBAM2.0</span></span>


<span data-ttu-id="16cb6-108">BitLockerAdministration и Monitor 2.0 обеспечивают соблюдение параметров политики шифрования BitLocker, заданных для предприятия, отслеживает соответствие клиентских компьютеров этим политикам и сообщает о состоянии шифрования как для предприятия, так и для отдельных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="16cb6-108">BitLockerAdministration and Monitoring2.0 enforces the BitLocker encryption policy options that you set for your enterprise, monitors the compliance of client computers with those policies, and reports on the encryption status of both the enterprise and the individual computers.</span></span> <span data-ttu-id="16cb6-109">Кроме того, MBAM позволяет получить доступ к сведениям о ключе восстановления, когда пользователь забыл свой PIN-код или пароль, а также при изменении BIOS или загрузочной записи.</span><span class="sxs-lookup"><span data-stu-id="16cb6-109">In addition, MBAM lets you access the recovery key information when users forget their PIN or password, or when their BIOS or boot record changes.</span></span>

<span data-ttu-id="16cb6-110">**Примечание**  В этом руководстве шифрование BitLocker не рассматривается подробно.</span><span class="sxs-lookup"><span data-stu-id="16cb6-110">**Note** BitLocker is not covered in detail in this guide.</span></span> <span data-ttu-id="16cb6-111">Общие сведения о BitLocker можно найти в разделе [Общие сведения о шифровании диска BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span><span class="sxs-lookup"><span data-stu-id="16cb6-111">For an overview of BitLocker, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

<span data-ttu-id="16cb6-112">Управление BitLocker может заинтересовать следующие группы: MBAM</span><span class="sxs-lookup"><span data-stu-id="16cb6-112">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="16cb6-113">Администраторы, ИТ-специалисты и руководителей соответствия требованиям, ответственные за обеспечение того, что конфиденциальные данные не будут закрыты без авторизации.</span><span class="sxs-lookup"><span data-stu-id="16cb6-113">Administrators, IT security professionals, and compliance officers who are responsible for ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="16cb6-114">Администраторы, ответственные за безопасность компьютеров в удаленных и филиалах</span><span class="sxs-lookup"><span data-stu-id="16cb6-114">Administrators who are responsible for computer security in remote or branch offices</span></span>

-   <span data-ttu-id="16cb6-115">Администраторы, ответственные за клиентские компьютеры под управлением Windows</span><span class="sxs-lookup"><span data-stu-id="16cb6-115">Administrators who are responsible for client computers that are running Windows</span></span>

## <a href="" id="what-s-new-in-mbam-2-0"></a><span data-ttu-id="16cb6-116">Новые возможности MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="16cb6-116">What’s New in MBAM2.0</span></span>


<span data-ttu-id="16cb6-117">MBAM 2.0 предоставляет следующие новые функции и возможности.</span><span class="sxs-lookup"><span data-stu-id="16cb6-117">MBAM2.0 provides the following new features and functionality.</span></span>

### <span data-ttu-id="16cb6-118">Интеграция System Center Configuration Manager с MBAM</span><span class="sxs-lookup"><span data-stu-id="16cb6-118">Integration of System Center Configuration Manager with MBAM</span></span>

<span data-ttu-id="16cb6-119">MBAM теперь поддерживает интеграцию с System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="16cb6-119">MBAM now supports integration with System Center Configuration Manager.</span></span> <span data-ttu-id="16cb6-120">Эта интеграция перемещает инфраструктуру соответствия MBAM в собственную среду Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="16cb6-120">This integration moves the MBAM compliance infrastructure into the native environment of Configuration Manager.</span></span> <span data-ttu-id="16cb6-121">ИТ – администраторы, использующие Configuration Manager на своем предприятии, смогут просматривать состояние соответствия требованиям своей организации в консоли управления Microsoft и просматривать отчеты для просмотра отдельных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="16cb6-121">IT administrators who use Configuration Manager in their enterprise can now view the compliance status of their enterprise in the Microsoft Management Console and drill into reports to view individual computers.</span></span>

### <span data-ttu-id="16cb6-122">Совместимость оборудования доступна только в топологии интеграции Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="16cb6-122">Hardware Compatibility is Available Only in the Configuration Manager Integration Topology</span></span>

<span data-ttu-id="16cb6-123">Интеграция Configuration Manager с MBAM включает возможности Configuration Manager, которые разрешают или запрещает использование определенных типов оборудования с помощью MBAM, и обеспечивает большую гибкость, чем совместимость оборудования, доступную в MBAM 1,0.</span><span class="sxs-lookup"><span data-stu-id="16cb6-123">Integrating Configuration Manager with MBAM enables Configuration Manager capabilities that allow or prohibit the use of certain hardware types with MBAM and provides more flexibility than the hardware compatibility that was available in MBAM 1.0.</span></span> <span data-ttu-id="16cb6-124">ИТ администраторы могут создавать собственные коллекции для ограничения оборудования и разворачивать базовые параметры конфигурации MBAM для этих коллекций.</span><span class="sxs-lookup"><span data-stu-id="16cb6-124">IT administrators can create their own collections to limit hardware and can deploy the MBAM configuration baseline to those collections.</span></span> <span data-ttu-id="16cb6-125">MBAM совместимость оборудования, присутствующая в MBAM 1,0, теперь доступна только в топологии Configuration Manager MBAM и администрируется из Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="16cb6-125">The MBAM hardware compatibility that was present in MBAM 1.0 is now available only in the MBAM Configuration Manager topology and is administered from Configuration Manager.</span></span>

### <span data-ttu-id="16cb6-126">Гибкие политики для защиты</span><span class="sxs-lookup"><span data-stu-id="16cb6-126">Protectors Flexible Policy</span></span>

<span data-ttu-id="16cb6-127">Компьютеры, уже зашифрованные с помощью предохранителя (например, TPM + PIN-код или автоматическое снятие блокировки и пароль) и принимающей политику MBAM, для которой требуется подмножество этого шифрования (например, TPM или автоматическое снятие блокировки), считаются совместимыми.</span><span class="sxs-lookup"><span data-stu-id="16cb6-127">Computers that are already encrypted with a protector (for example, TPM + PIN or Auto-Unlock and password) and that receive an MBAM policy that requires a subset of that encryption (for example, TPM or Auto-Unlock) are considered compliant.</span></span> <span data-ttu-id="16cb6-128">В приведенном выше примере ПИН-код и пароль не удаляются автоматически, если администратор не определит эти функции, как только они больше не разрешены.</span><span class="sxs-lookup"><span data-stu-id="16cb6-128">In the example above, PIN and password would not be removed automatically unless the IT administrator specifically defines these features as no longer allowed.</span></span>

<span data-ttu-id="16cb6-129">Компьютеры, которые не шифруются и получают MBAM политику (например, TPM или автоматическое снятие блокировки), шифруются соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="16cb6-129">Computers that are not encrypted and that receive an MBAM policy (for example, TPM or Auto-Unlock) are encrypted accordingly.</span></span> <span data-ttu-id="16cb6-130">Пользователи локальных администраторов могут использовать средства BitLocker (шифрование диска BitLocker или Manage-bde) для добавления или изменения существующих предохранителей (например, TPM + PIN-код или автоматическое снятие блокировки и пароль).</span><span class="sxs-lookup"><span data-stu-id="16cb6-130">Users who are local administrators are allowed to use the BitLocker tools (Control Panel item BitLocker Drive Encryption or Manage-bde) to add or modify the existing protectors (for example, TPM + PIN or Auto-Unlock and password).</span></span> <span data-ttu-id="16cb6-131">Они будут соответствовать требованиям, если только они не определяются политиками MBAM.</span><span class="sxs-lookup"><span data-stu-id="16cb6-131">They remain compliant unless MBAM policies specifically define them.</span></span>

### <span data-ttu-id="16cb6-132">Возможность обновления клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="16cb6-132">Ability to Upgrade the MBAM Client</span></span>

<span data-ttu-id="16cb6-133">Установщик Windows клиента MBAM 2.0 определяет версию существующего клиента и выполняет необходимые действия по обновлению клиента MBAM 2.0 из предыдущих версий.</span><span class="sxs-lookup"><span data-stu-id="16cb6-133">The MBAM2.0 Client Windows Installer detects the version of the existing client and performs the required steps to upgrade to the MBAM2.0 Client from previous versions.</span></span>

### <span data-ttu-id="16cb6-134">Возможность обновления сервера MBAM из предыдущих версий</span><span class="sxs-lookup"><span data-stu-id="16cb6-134">Ability to Upgrade the MBAM Server from Previous Versions</span></span>

<span data-ttu-id="16cb6-135">Чтобы обновить инфраструктуру сервера MBAM 2.0 из предыдущих версий MBAM, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="16cb6-135">You can upgrade the MBAM2.0 Server infrastructure from previous versions of MBAM as follows:</span></span>

<span data-ttu-id="16cb6-136">**Замена сервера вручную** — необходимо вручную удалить существующую инфраструктуру сервера MBAM, а затем установить серверную инфраструктуру MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="16cb6-136">**Manual in-place server replacement** – You must manually uninstall the existing MBAM server infrastructure, and then install the MBAM 2.0 Server infrastructure.</span></span> <span data-ttu-id="16cb6-137">Вам не нужно удалять базы данных, чтобы выполнить обновление.</span><span class="sxs-lookup"><span data-stu-id="16cb6-137">You do not have to remove the databases to do the upgrade.</span></span> <span data-ttu-id="16cb6-138">Вместо этого вы выбираете существующие базы данных, которые создали предыдущую версию клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="16cb6-138">Instead, you select the existing databases, which the previous version of the MBAM Client created.</span></span> <span data-ttu-id="16cb6-139">После этого установка обновления MBAM 2.0 переносит существующие базы данных в MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="16cb6-139">The MBAM2.0 upgrade installation then migrates the existing databases to MBAM 2.0.</span></span>

<span data-ttu-id="16cb6-140">**Обновление распределенного клиента** — если вы используете автономную топологию MBAM, вы можете сразу обновить клиенты MBAM после установки инфраструктуры сервера MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="16cb6-140">**Distributed client upgrade** – If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 Server infrastructure.</span></span> <span data-ttu-id="16cb6-141">Сервер MBAM 2,0 определяет версию существующего клиента и выполняет необходимые действия по обновлению до клиента 2,0.</span><span class="sxs-lookup"><span data-stu-id="16cb6-141">The MBAM 2.0 Server detects the version of the existing Client and performs the required steps to upgrade to the 2.0 Client.</span></span>

<span data-ttu-id="16cb6-142">После обновления инфраструктуры сервера MBAM 2,0 клиенты MBAM 1,0 продолжают сообщать об этом на сервер MBAM 2,0, использующий данные для восстановления, но соответствие требованиям будет основываться на политиках в MBAM 1,0.</span><span class="sxs-lookup"><span data-stu-id="16cb6-142">After you upgrade the MBAM 2.0 Server infrastructure, MBAM 1.0 Clients continue to report to the MBAM 2.0 Server successfully, escrowing recovery data, but compliance will be based on the policies in MBAM 1.0.</span></span> <span data-ttu-id="16cb6-143">Чтобы клиентские компьютеры MBAM на соответствие требованиям политик MBAM 2,0, необходимо обновить клиенты до версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="16cb6-143">You must upgrade clients to MBAM 2.0 to have client computers accurately report compliance against the MBAM 2.0 policies.</span></span> <span data-ttu-id="16cb6-144">Вы можете обновить клиентские компьютеры до MBAM 2,0 без удаления прежнего клиента, после чего клиент начнет применять и сообщать о политиках MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="16cb6-144">You can upgrade the clients to the MBAM 2.0 Client without uninstalling the previous client, and the client will start to apply and report MBAM 2.0 policies.</span></span>

<span data-ttu-id="16cb6-145">Если вы используете MBAM с Configuration Manager, вы должны обновить клиенты MBAM 1,0 до MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="16cb6-145">If you are using MBAM with Configuration Manager, you must upgrade the MBAM 1.0 clients to MBAM 2.0.</span></span>

### <a href="" id="mbam-support-for-bitlocker-s-enterprise-scenarios-on-the-windows-8-platform"></a><span data-ttu-id="16cb6-146">MBAM поддержка корпоративных сценариев BitLocker на платформе Windows 8</span><span class="sxs-lookup"><span data-stu-id="16cb6-146">MBAM Support for BitLocker’s Enterprise Scenarios on the Windows 8 Platform</span></span>

<span data-ttu-id="16cb6-147">MBAM поддерживает операционную систему Windows 8 как целевую платформу для установки клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="16cb6-147">MBAM supports the Windows 8 operating system as a target platform for the MBAM Client installation.</span></span> <span data-ttu-id="16cb6-148">Эта поддержка позволяет администраторам устанавливать агент MBAM, зашифровывать диски операционной системы Windows 8, а также сообщать о соответствии компьютеров требованиям.</span><span class="sxs-lookup"><span data-stu-id="16cb6-148">This support enables IT administrators to install the MBAM agent, to encrypt Windows 8 operating system drives, and to report on the compliance of the computers.</span></span> <span data-ttu-id="16cb6-149">MBAM использует доверенный платформенный модуль и доверенный платформенный модуль и ПИН-код, чтобы управлять операционной системой Windows 8 точно так же, как и в операционной системе Windows 7.</span><span class="sxs-lookup"><span data-stu-id="16cb6-149">MBAM leverages the TPM and TPM+PIN protectors to manage the Windows 8 operating system just as it does the Windows 7 operating system.</span></span> <span data-ttu-id="16cb6-150">В MBAM 2.0 также добавлена поддержка шифрования клиентов Windows to go.</span><span class="sxs-lookup"><span data-stu-id="16cb6-150">MBAM2.0 also adds support for encrypting Windows To Go clients.</span></span>

### <span data-ttu-id="16cb6-151">Добавление портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="16cb6-151">Addition of the Self-Service Portal</span></span>

<span data-ttu-id="16cb6-152">Конечные пользователи теперь могут использовать портал самообслуживания для восстановления ключей восстановления.</span><span class="sxs-lookup"><span data-stu-id="16cb6-152">End users can now use the Self-Service Portal to recover their recovery keys.</span></span> <span data-ttu-id="16cb6-153">Портал самообслуживания может быть развернут на одном сервере с другими функциями MBAM или на отдельном сервере, который предоставляет ИТ-администраторам гибкие возможности для предоставления пользователям доступа к порталу с самостоятельным сервером.</span><span class="sxs-lookup"><span data-stu-id="16cb6-153">The Self-Service Portal can be deployed on a single server with the other MBAM features, or on a separate server that gives IT administrators the flexibility to expose the Self-Server Portal to users, as required.</span></span> <span data-ttu-id="16cb6-154">После того как портал самообслуживания удостоверяет подлинность пользователей, пользователи должны будут вводить только первые восемь цифр идентификатора ключа восстановления для получения ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="16cb6-154">After the Self-Service Portal authenticates users, users have to enter only the first eight digits of the recovery key ID to receive their recovery key.</span></span>

<span data-ttu-id="16cb6-155">MBAM также защищает ключ, позволяя пользователям восстанавливать ключи только для тех компьютеров, на которых они находятся, что снижает риск несанкционированного доступа других пользователей.</span><span class="sxs-lookup"><span data-stu-id="16cb6-155">MBAM also secures the key by allowing users to recover keys only for those computers on which they are users, which reduces the risk that other users gain unauthorized access.</span></span>

### <span data-ttu-id="16cb6-156">Возможность автоматического возобновления защиты BitLocker от приостановленного состояния</span><span class="sxs-lookup"><span data-stu-id="16cb6-156">Ability to Automatically Resume BitLocker Protection from a Suspended State</span></span>

<span data-ttu-id="16cb6-157">MBAM больше не разрешается, чтобы ИТ – администраторы были приостановлены и не защищены в течение длительного периода времени.</span><span class="sxs-lookup"><span data-stu-id="16cb6-157">MBAM no longer allows IT administrators to keep BitLocker suspended and unprotected for prolonged periods of time.</span></span> <span data-ttu-id="16cb6-158">Если ИТ-администратор приостанавливает BitLocker, MBAM повторно включает его автоматически при перезагрузке компьютера, что снижает риск для атаки компьютера.</span><span class="sxs-lookup"><span data-stu-id="16cb6-158">If an IT administrator suspends BitLocker, MBAM re-enables it automatically when the computer is rebooted, which reduces the risk that the computer can be attacked.</span></span>

### <span data-ttu-id="16cb6-159">Несъемные диски с данными можно настроить для автоматической разблокировки без пароля.</span><span class="sxs-lookup"><span data-stu-id="16cb6-159">Fixed Data Drives Can Be Configured to Automatically Unlock Without a Password</span></span>

<span data-ttu-id="16cb6-160">Теперь политика фиксированного диска с данными (FDD) может быть настроена на автоматическое снятие блокировки диска без пароля.</span><span class="sxs-lookup"><span data-stu-id="16cb6-160">A Fixed Data Drive (FDD) policy can now be configured to allow automatic unlocking of the drive without a password.</span></span> <span data-ttu-id="16cb6-161">Пользователи не получают запрос на ввод пароля перед шифрованием FDD, а FDD будет защищен и автоматически разблокирован с диском операционной системы.</span><span class="sxs-lookup"><span data-stu-id="16cb6-161">Users are not prompted for a password before the FDD is encrypted, and the FDD will be secured and auto-unlocked with the operating system drive.</span></span>

## <a href="" id="---------mbam-2-0-release-notes"></a> <span data-ttu-id="16cb6-162">Заметки о выпуске MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="16cb6-162">MBAM2.0 Release Notes</span></span>


<span data-ttu-id="16cb6-163">Чтобы получить дополнительные сведения и последние новости, не включенные в документацию, ознакомьтесь с [заметками о выпуске для MBAM 2,0](release-notes-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="16cb6-163">For more information, and for late-breaking news that is not included in the documentation, see the [Release Notes for MBAM 2.0](release-notes-for-mbam-20-mbam-2.md).</span></span>

## <span data-ttu-id="16cb6-164">Как получить MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="16cb6-164">How to Get MBAM2.0</span></span>


<span data-ttu-id="16cb6-165">Эта технология является частью пакета оптимизации рабочего стола Майкрософт (MDOP).</span><span class="sxs-lookup"><span data-stu-id="16cb6-165">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="16cb6-166">Корпоративные пользователи могут получить MDOP с помощью программы Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="16cb6-166">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="16cb6-167">Дополнительные сведения о Microsoft Software Assurance и приобретении MDOP можно найти в [статье как получить MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049)</span><span class="sxs-lookup"><span data-stu-id="16cb6-167">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049)</span></span>

## <span data-ttu-id="16cb6-168">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="16cb6-168">Related topics</span></span>


[<span data-ttu-id="16cb6-169">Начало работы с MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="16cb6-169">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





