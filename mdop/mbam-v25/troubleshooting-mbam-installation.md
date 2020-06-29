---
title: Устранение неполадок, возникающих при установке MBAM 2.5
description: В этой статье объясняется, как устранить проблемы с установкой MBAM 2,5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812864"
---
# <span data-ttu-id="608f5-103">Устранение неполадок, возникающих при установке MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="608f5-103">Troubleshooting MBAM 2.5 installation problems</span></span>

<span data-ttu-id="608f5-104">В этой статье объясняется, как устранить проблемы с установкой Microsoft BitLocker для администрирования и мониторинга (MBAM) 2,5 в автономной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="608f5-104">This article introduces how to troubleshoot Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 installation issues in a standalone configuration.</span></span>

## <span data-ttu-id="608f5-105">Обращение к файлам журнала MBAM для устранения неполадок</span><span class="sxs-lookup"><span data-stu-id="608f5-105">Referring MBAM log files for troubleshooting</span></span>

<span data-ttu-id="608f5-106">MBAM включает ведение журнала для установки сервера, установки клиентов и событий.</span><span class="sxs-lookup"><span data-stu-id="608f5-106">MBAM includes logging for server installation, client installation, and events.</span></span> <span data-ttu-id="608f5-107">Это ведение журнала должно быть рекомендовано для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="608f5-107">This logging should be referred to for troubleshooting.</span></span> 
 
### <span data-ttu-id="608f5-108">Файлы журнала установки сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="608f5-108">MBAM server installation log files</span></span>

<span data-ttu-id="608f5-109">MBAMServerSetup.exe создает следующие файлы журнала в папке% temp% пользователя при установке MBAM:</span><span class="sxs-lookup"><span data-stu-id="608f5-109">MBAMServerSetup.exe generates the following log files in the user’s %temp% folder during MBAM installation:</span></span><br /> **<span data-ttu-id="608f5-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 номеров>. log</span><span class="sxs-lookup"><span data-stu-id="608f5-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 numbers>.log</span></span>**

<span data-ttu-id="608f5-111">В MBAMServerSetup.exe регистрируются действия, которые были предприняты при установке компонентов MBAM и MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="608f5-111">MBAMServerSetup.exe logs the actions that were taken during MBAM setup and MBAM server feature installation:</span></span><br /> **<span data-ttu-id="608f5-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. log</span><span class="sxs-lookup"><span data-stu-id="608f5-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log</span></span>**

<span data-ttu-id="608f5-113">MBAMServerSetup.exe заносит в журнал дополнительные действия, предпринятые во время установки.</span><span class="sxs-lookup"><span data-stu-id="608f5-113">MBAMServerSetup.exe logs additional actions that were taken during installation.</span></span>

### <span data-ttu-id="608f5-114">Файл журнала установки клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="608f5-114">MBAM client installation log file</span></span>

<span data-ttu-id="608f5-115">Установка клиента записывается в следующем файле журнала в папке% Temp% (или в другом расположении в зависимости от того, как был установлен клиент).</span><span class="sxs-lookup"><span data-stu-id="608f5-115">The client installation is recorded in the following log file in the %temp% folder (or a custom location, depending on how the client was installed):</span></span> <br />**<span data-ttu-id="608f5-116">MSI \<five random characters\> . log</span><span class="sxs-lookup"><span data-stu-id="608f5-116">MSI\<five random characters\>.log</span></span>**

<span data-ttu-id="608f5-117">Этот журнал включает действия, которые выполняются во время установки клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="608f5-117">This log contains the actions that are taken during MBAM client installation.</span></span>
 
### <span data-ttu-id="608f5-118">Событие клиента MBAM — канал ведения журнала</span><span class="sxs-lookup"><span data-stu-id="608f5-118">MBAM client event-logging channel</span></span>

<span data-ttu-id="608f5-119">В MBAM есть отдельные каналы ведения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="608f5-119">MBAM has separate event-logging channels.</span></span> <span data-ttu-id="608f5-120">Файлы журнала администрирования, аналитики и операционной системы находятся в окне "Просмотр событий" в разделе **журналы приложений и служб**в  >  **Microsoft**  >  **Windows**  >  **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="608f5-120">The Admin, Analytical, and Operational log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span>

<span data-ttu-id="608f5-121">В таблице ниже приведено краткое описание каждого журнала событий.</span><span class="sxs-lookup"><span data-stu-id="608f5-121">The following table provides a brief description of each event log.</span></span>
 
|<span data-ttu-id="608f5-122">Журнал событий</span><span class="sxs-lookup"><span data-stu-id="608f5-122">Event log</span></span>| <span data-ttu-id="608f5-123">Описание</span><span class="sxs-lookup"><span data-stu-id="608f5-123">Description</span></span>|
|----------|-------|
|<span data-ttu-id="608f5-124">Microsoft-Windows-MBAM/администратор</span><span class="sxs-lookup"><span data-stu-id="608f5-124">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="608f5-125">Содержат сообщения об ошибках</span><span class="sxs-lookup"><span data-stu-id="608f5-125">Contains error messages</span></span>|
|<span data-ttu-id="608f5-126">Microsoft-Windows-MBAM/аналитический</span><span class="sxs-lookup"><span data-stu-id="608f5-126">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="608f5-127">Дополнительные сведения для ведения журнала</span><span class="sxs-lookup"><span data-stu-id="608f5-127">Contains advanced logging information</span></span>|
|<span data-ttu-id="608f5-128">Microsoft-Windows-MBAM/Operational</span><span class="sxs-lookup"><span data-stu-id="608f5-128">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="608f5-129">Содержат сообщения об успешном завершении</span><span class="sxs-lookup"><span data-stu-id="608f5-129">Contains success messages</span></span>|

### <span data-ttu-id="608f5-130">Событие сервера MBAM — канал ведения журнала</span><span class="sxs-lookup"><span data-stu-id="608f5-130">MBAM server event-logging channel</span></span>

<span data-ttu-id="608f5-131">Файлы журнала находятся в окне просмотра событий, в разделе **журналы приложений и служб**в  >  **Microsoft**  >  **Windows**  >  **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="608f5-131">The log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span> <span data-ttu-id="608f5-132">В таблице ниже указаны журналы событий сервера, которые появились в MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="608f5-132">The following table includes server event logs that were introduced in MBAM 2.5:</span></span>

|<span data-ttu-id="608f5-133">Журнал событий</span><span class="sxs-lookup"><span data-stu-id="608f5-133">Event log</span></span>| <span data-ttu-id="608f5-134">Описание</span><span class="sxs-lookup"><span data-stu-id="608f5-134">Description</span></span>|
|--------|-------------|
|<span data-ttu-id="608f5-135">Microsoft-Windows-MBAM/администратор</span><span class="sxs-lookup"><span data-stu-id="608f5-135">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="608f5-136">Содержат сообщения об ошибках</span><span class="sxs-lookup"><span data-stu-id="608f5-136">Contains error messages</span></span>|
|<span data-ttu-id="608f5-137">Microsoft-Windows-MBAM/аналитический</span><span class="sxs-lookup"><span data-stu-id="608f5-137">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="608f5-138">Дополнительные сведения для ведения журнала</span><span class="sxs-lookup"><span data-stu-id="608f5-138">Contains advanced logging information</span></span>|
|<span data-ttu-id="608f5-139">Microsoft-Windows-MBAM/Operational</span><span class="sxs-lookup"><span data-stu-id="608f5-139">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="608f5-140">Содержат сообщения об успешном завершении</span><span class="sxs-lookup"><span data-stu-id="608f5-140">Contains success messages</span></span>|

### <span data-ttu-id="608f5-141">Журналы веб-службы MBAM</span><span class="sxs-lookup"><span data-stu-id="608f5-141">MBAM web service logs</span></span>

<span data-ttu-id="608f5-142">Каждый журнал веб-службы MBAM записывает данные журнала в файл SVCLOG.</span><span class="sxs-lookup"><span data-stu-id="608f5-142">Each MBAM web service log writes logging information to an SVCLOG file.</span></span> <span data-ttu-id="608f5-143">По умолчанию каждая веб-служба записывает файл трассировки в папку, которая использует ее имя в папке Solution\Logs управления C:\inetpub\Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="608f5-143">By default, each web service writes the trace file under a folder that uses its name in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span>

<span data-ttu-id="608f5-144">Вы можете использовать средство просмотра служебной трассировки (часть Microsoft Visual Studio) для просмотра трассировок SVCLOG.</span><span class="sxs-lookup"><span data-stu-id="608f5-144">You can use the service trace viewer tool (part of Microsoft Visual Studio) to review the svclog traces.</span></span>

## <span data-ttu-id="608f5-145">Устранение неполадок, связанных с шифрованием и отчетами</span><span class="sxs-lookup"><span data-stu-id="608f5-145">Troubleshooting encryption and reporting issues</span></span>

<span data-ttu-id="608f5-146">В этом разделе содержатся сведения об устранении неполадок, возникающих в компонентах сервера, клиентах, параметрах конфигурации и известных проблемах.</span><span class="sxs-lookup"><span data-stu-id="608f5-146">This section contains troubleshooting information for server functionality, client functionality, configuration settings, and known issues:</span></span>
 
### <span data-ttu-id="608f5-147">Установка клиента MBAM, параметры групповой политики</span><span class="sxs-lookup"><span data-stu-id="608f5-147">MBAM client installation, Group Policy settings</span></span>

<span data-ttu-id="608f5-148">Определение того, установлен ли агент MBAM на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="608f5-148">Determine whether the MBAM agent is installed on the client computer.</span></span> <span data-ttu-id="608f5-149">При установке MBAM создается служба, которая называется службой клиента управления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="608f5-149">When MBAM is installed, it creates a service that is named BitLocker Management Client Service.</span></span> <span data-ttu-id="608f5-150">Эта служба настроена на автоматический запуск.</span><span class="sxs-lookup"><span data-stu-id="608f5-150">This service is configured to start automatically.</span></span> <span data-ttu-id="608f5-151">Определите, работает ли служба.</span><span class="sxs-lookup"><span data-stu-id="608f5-151">Determine whether the service is running.</span></span>

<span data-ttu-id="608f5-152">Убедитесь, что параметры групповой политики MBAM применяются на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="608f5-152">Make sure that MBAM Group Policy settings are applied on the client computer.</span></span> <span data-ttu-id="608f5-153">Если на клиентском компьютере были применены параметры групповой политики, создается следующий подраздел реестра: **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**</span><span class="sxs-lookup"><span data-stu-id="608f5-153">The following registry subkey is created if the Group Policy settings were applied on the client computer: **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**</span></span>

<span data-ttu-id="608f5-154">Убедитесь в том, что этот раздел существует и заполнен с помощью значений в параметрах групповой политики.</span><span class="sxs-lookup"><span data-stu-id="608f5-154">Verify that this key exists and is populated by using values per Group Policy settings.</span></span>

### <span data-ttu-id="608f5-155">Агент MBAM в начальном периоде задержки</span><span class="sxs-lookup"><span data-stu-id="608f5-155">MBAM Agent in the initial delay period</span></span>

<span data-ttu-id="608f5-156">Клиент MBAM не запускает операцию сразу после установки.</span><span class="sxs-lookup"><span data-stu-id="608f5-156">The MBAM client doesn't start the operation immediately after installation.</span></span> <span data-ttu-id="608f5-157">Начальная случайная задержка составляет 1 – 18 минут, прежде чем агент MBAM начинает операцию.</span><span class="sxs-lookup"><span data-stu-id="608f5-157">There is an initial random delay of 1–18 minutes before the MBAM Agent starts its operation.</span></span> <span data-ttu-id="608f5-158">В дополнение к начальной задержке, задержка не должна быть менее 90 минут.</span><span class="sxs-lookup"><span data-stu-id="608f5-158">In addition to the initial delay, there is a delay of at least 90 minutes.</span></span> <span data-ttu-id="608f5-159">(Задержка зависит от параметров групповой политики, которые настроены на частоту проверки состояния клиента.) Таким образом, Общая задержка перед началом работы клиента — задержка *случайной задержки при запуске*  +  *client checking frequency delay*.</span><span class="sxs-lookup"><span data-stu-id="608f5-159">(The delay depends on the Group Policy settings that are configured for the frequency of checking the client status.) Therefore, the total delay before a client starts operation is *random startup delay* + *client checking frequency delay*.</span></span>

<span data-ttu-id="608f5-160">Если журналы событий для операционной и для администраторов пусты, клиент еще не начал операцию и находится в период задержки, упомянутый ранее.</span><span class="sxs-lookup"><span data-stu-id="608f5-160">If the Operational and Admin event logs are blank, the client has not started the operation yet and is in the delay period that was mentioned earlier.</span></span> <span data-ttu-id="608f5-161">Если вы хотите обойти эту задержку, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="608f5-161">If you want to bypass the delay, follow these steps:</span></span>
 
1. <span data-ttu-id="608f5-162">Остановите службу клиента управления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="608f5-162">Stop the BitLocker Management Client Service service.</span></span>

2. <span data-ttu-id="608f5-163">В разделе реестра **HKEY_LOCAL_MACHINE \software\microsoft\mbam** Создайте значение реестра **NoStartupDelay** , задайте для него тип **REG_DWORD**и установите для него значение **1**.</span><span class="sxs-lookup"><span data-stu-id="608f5-163">Under the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM** registry subkey, create the **NoStartupDelay** registry value, set its type to **REG_DWORD**, and then set its value to **1**.</span></span>

3. <span data-ttu-id="608f5-164">В разделе **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**задайте для параметров **ClientWakeupFrequency** и **StatusReportingFrequency** значение **1**.</span><span class="sxs-lookup"><span data-stu-id="608f5-164">Under **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**, set the **ClientWakeupFrequency** and **StatusReportingFrequency** values to **1**.</span></span> <span data-ttu-id="608f5-165">Эти значения будут возвращены к исходным параметрам после обновления групповой политики на компьютере.</span><span class="sxs-lookup"><span data-stu-id="608f5-165">These values will revert to their original settings after Group Policy updates are on the computer.</span></span>

4. <span data-ttu-id="608f5-166">Запустите службу клиента управления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="608f5-166">Start the BitLocker Management Client Service service.</span></span>

<span data-ttu-id="608f5-167">После запуска службы при локальном входе на компьютер и отсутствии ошибок вы должны получить запрос на шифрование компьютера в течение одной минуты.</span><span class="sxs-lookup"><span data-stu-id="608f5-167">After the service starts, if you log in locally on the computer and there are no errors, you should receive a request to encrypt the computer within one minute.</span></span> <span data-ttu-id="608f5-168">Если вы не получили запрос, проверьте, нет ли в журналах администратора MBAM записи об ошибках.</span><span class="sxs-lookup"><span data-stu-id="608f5-168">If you do not receive a request, you should review the MBAM Admin logs for any error entries.</span></span>

### <span data-ttu-id="608f5-169">На компьютере отсутствует доверенный платформенный модуль или устройство TPM не включено в BIOS</span><span class="sxs-lookup"><span data-stu-id="608f5-169">Computer does not have a TPM device, or the TPM device is not enabled in the BIOS</span></span>

<span data-ttu-id="608f5-170">Просматривайте журнал событий администратора MBAM.</span><span class="sxs-lookup"><span data-stu-id="608f5-170">Review the MBAM Admin event log.</span></span> <span data-ttu-id="608f5-171">В журнале событий администрирования MBAM появляется запись о событии, аналогичную приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="608f5-171">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

<span data-ttu-id="608f5-172">Откройте консоль управления TPM (TPM. msc) и убедитесь, что на компьютере есть устройство TPM.</span><span class="sxs-lookup"><span data-stu-id="608f5-172">Open TPM Management (tpm.msc), and check whether the computer has a TPM device.</span></span> <span data-ttu-id="608f5-173">Если в TPM. msc не отображается устройство, откройте Диспетчер устройств (devmgmt. msc) и проверьте наличие доверенного платформенного модуля в разделе "устройства безопасности".</span><span class="sxs-lookup"><span data-stu-id="608f5-173">If tpm.msc does not show a device, open Device Manager (devmgmt.msc), and check for a Trusted Platform Module under Security Devices.</span></span> <span data-ttu-id="608f5-174">Если вы не видите устройство доверенного платформенного модуля, это может быть вызвано одной из указанных ниже причин.</span><span class="sxs-lookup"><span data-stu-id="608f5-174">If you do not see a Trusted Platform Module device, this might be true for one of the following reasons:</span></span>

* <span data-ttu-id="608f5-175">У вашей системы нет устройства доверенного платформенного модуля (TPM/Security).</span><span class="sxs-lookup"><span data-stu-id="608f5-175">Your system doesn't have a Trusted Platform Module (TPM/Security) device.</span></span>

* <span data-ttu-id="608f5-176">Устройство доверенного платформенного модуля отключено в BIOS.</span><span class="sxs-lookup"><span data-stu-id="608f5-176">The TPM device is disabled in the BIOS.</span></span>

* <span data-ttu-id="608f5-177">В BIOS включено устройство TPM, но управление устройством TPM из параметра операционной системы отключено в BIOS.</span><span class="sxs-lookup"><span data-stu-id="608f5-177">TPM Device is enabled in the BIOS, but management of the TPM device from the operating system setting is disabled in the BIOS.</span></span>

* <span data-ttu-id="608f5-178">Вы не используете драйвер Microsoft для устройства доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="608f5-178">You aren't using a Microsoft driver for the TPM device.</span></span> <span data-ttu-id="608f5-179">Ознакомьтесь с устройствами, указанными в диспетчере устройств, чтобы определить драйвер устройства доверенного платформенного модуля (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="608f5-179">Review the devices that are listed in device manager to identify the Microsoft TPM device driver.</span></span>

<span data-ttu-id="608f5-180">Если устройство доверенного платформенного модуля не использует драйвер C:\Windows\System32\tpm.sys, необходимо обновить драйвер, выбрав файл C:\Windows\Inf\tpm.inf.</span><span class="sxs-lookup"><span data-stu-id="608f5-180">If the TPM device is not using the C:\Windows\System32\tpm.sys driver, you should update the driver by selecting the C:\Windows\Inf\tpm.inf file.</span></span>

### <span data-ttu-id="608f5-181">На компьютере отсутствует допустимый системный раздел</span><span class="sxs-lookup"><span data-stu-id="608f5-181">Computer does not have a valid SYSTEM partition</span></span>

<span data-ttu-id="608f5-182">Просматривайте журнал событий администратора MBAM.</span><span class="sxs-lookup"><span data-stu-id="608f5-182">Review the MBAM Admin event log.</span></span> <span data-ttu-id="608f5-183">В журнале событий администрирования MBAM появляется запись о событии, аналогичную приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="608f5-183">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

<span data-ttu-id="608f5-184">Для включения шифрования BitLocker требуется системный раздел ([Шифрование диска BitLocker в Windows 7: часто задаваемые вопросы](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span><span class="sxs-lookup"><span data-stu-id="608f5-184">BitLocker requires a SYSTEM partition to enable encryption ([BitLocker Drive Encryption in Windows 7: Frequently Asked Questions](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span></span>

<span data-ttu-id="608f5-185">MBAM не создает системный раздел автоматически.</span><span class="sxs-lookup"><span data-stu-id="608f5-185">MBAM doesn't create the system partition automatically.</span></span> <span data-ttu-id="608f5-186">Вы можете использовать служебную программу подготовки диска для BitLocker (bdehdcfg.exe) для создания системного раздела и перемещения необходимых файлов загрузки.</span><span class="sxs-lookup"><span data-stu-id="608f5-186">You can use the BitLocker drive preparation utility (bdehdcfg.exe) to create the system partition and move the required startup files.</span></span>

<span data-ttu-id="608f5-187">Например, вы можете использовать команду **% WINDIR% \system32\bdeHdCfg.exe-Target (размер по умолчанию) 300 – quiet** , чтобы подготовить диск без уведомления, прежде чем развертывать MBAM, чтобы зашифровать диски.</span><span class="sxs-lookup"><span data-stu-id="608f5-187">For example, you can use the command **%windir%\system32\bdeHdCfg.exe -target default -size 300 –quiet** to prepare the drive silently before you deploy MBAM to encrypt the drives.</span></span> <span data-ttu-id="608f5-188">Для этого требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="608f5-188">This requires a restart.</span></span> <span data-ttu-id="608f5-189">Вы также можете создать сценарий действия, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="608f5-189">You can also script the action if this is required.</span></span> <span data-ttu-id="608f5-190">В следующем документе описан инструмент подготовки диска для BitLocker:</span><span class="sxs-lookup"><span data-stu-id="608f5-190">The following document describes the BitLocker Drive Preparation Tool:</span></span>

[<span data-ttu-id="608f5-191">Описание средства подготовки диска для BitLocker</span><span class="sxs-lookup"><span data-stu-id="608f5-191">Description of the BitLocker Drive Preparation Tool</span></span>](https://support.microsoft.com/help/933246)

### <span data-ttu-id="608f5-192">Диски не отформатированы для использования совместимой файловой системы</span><span class="sxs-lookup"><span data-stu-id="608f5-192">Drives are not formatted to have a compatible file system</span></span>

<span data-ttu-id="608f5-193">Ознакомьтесь со [статьей TechNet о требованиях файловой системы для BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).</span><span class="sxs-lookup"><span data-stu-id="608f5-193">See the [TechNet article for file system requirements for BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).</span></span>

### <span data-ttu-id="608f5-194">Конфликт групповых политик</span><span class="sxs-lookup"><span data-stu-id="608f5-194">Group Policy conflict</span></span>

<span data-ttu-id="608f5-195">В журнале событий администрирования MBAM появляется запись о событии, аналогичную приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="608f5-195">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

<span data-ttu-id="608f5-196">Проверьте параметры групповой политики, чтобы убедиться в отсутствии конфликта между параметрами групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="608f5-196">Verify your Group Policy settings to make sure that you do not have a conflicting setting among the MBAM Group Policy settings.</span></span>

<span data-ttu-id="608f5-197">Групповую политику следует настроить с помощью шаблона MBAM MDOP, а не шаблона шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="608f5-197">You should configure Group Policy by using the MDOP MBAM template and not the BitLocker Drive Encryption template.</span></span>

<span data-ttu-id="608f5-198">Пример</span><span class="sxs-lookup"><span data-stu-id="608f5-198">For example:</span></span>

<span data-ttu-id="608f5-199">В разделе Параметры шифрования диска операционной системы вы выбрали доверенный платформенный модуль в качестве предохранителя, и вы также выбрали параметр **разрешить дополнительные контакты для запуска**.</span><span class="sxs-lookup"><span data-stu-id="608f5-199">Under Operating system drive encryption settings, you selected TPM as the protector, and you also selected **Allow enhanced PINs for startup**.</span></span> <span data-ttu-id="608f5-200">Это конфликтующие параметры, так как для защиты только доверенного платформенного модуля не требуется ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="608f5-200">These are conflicting settings because TPM-only protection doesn't require a PIN.</span></span> <span data-ttu-id="608f5-201">Поэтому вы должны отключить параметр расширенные контакты.</span><span class="sxs-lookup"><span data-stu-id="608f5-201">Therefore, you should disable the enhanced PINs setting.</span></span>

### <span data-ttu-id="608f5-202">Пользователь мог запрашивать исключение</span><span class="sxs-lookup"><span data-stu-id="608f5-202">User may have requested an exemption</span></span>

<span data-ttu-id="608f5-203">Если вы включили параметр параметры групповой политики Components\MDOP MBAM (Управление шифрованием для компьютера \ административные шаблоны \ компоненты Windows \client Management\Configure), пользователям будет предложено запросить исключение.</span><span class="sxs-lookup"><span data-stu-id="608f5-203">If you enabled the Computer Configuration\Administrative Templates\Windows Components\MDOP MBAM (BitLocker Management)\Client Management\Configure user exemption policy Group Policy setting, users will be offered the option to request an exemption.</span></span>

<span data-ttu-id="608f5-204">По умолчанию, если пользователь запрашивает исключение, исключение будет действовать в течение 7 дней, и пользователь не сможет получать запросы на шифрование в течение этого периода.</span><span class="sxs-lookup"><span data-stu-id="608f5-204">By default, if the user requests an exemption, the exemption will be valid for 7 days, and the user will not receive prompts to encrypt during this period.</span></span> <span data-ttu-id="608f5-205">(Значение по умолчанию можно увеличить или уменьшить в ходе настройки политики.) После того, как период освобождения будет завершен, пользователю будет предложено выполнить шифрование.</span><span class="sxs-lookup"><span data-stu-id="608f5-205">(The default value can be increased or decreased during policy configuration.) After the exemption period is over, the user is prompted to encrypt.</span></span>

<span data-ttu-id="608f5-206">В журнале событий администратора MBAM появляется следующая запись, когда компьютер находится в разделе освобождение пользователей.</span><span class="sxs-lookup"><span data-stu-id="608f5-206">You will see the following entry in the MBAM Admin event log when a computer is under user exemption:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

<span data-ttu-id="608f5-207">Если вы хотите вручную переопределять освобождение от пользователя для компьютера, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="608f5-207">If you want to manually override user exemption for a computer, follow these steps:</span></span>
 
1. <span data-ttu-id="608f5-208">Установите для параметра AllowUserExemption значение **0** в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="608f5-208">Set the AllowUserExemption value to **0** under the following registry subkey:</span></span> <br />
**<span data-ttu-id="608f5-209">HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span><span class="sxs-lookup"><span data-stu-id="608f5-209">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

2. <span data-ttu-id="608f5-210">Удалите все значения реестра из следующего подраздела реестра, кроме **AgentVersion**, **EncodedComputerName**и **установленного**.</span><span class="sxs-lookup"><span data-stu-id="608f5-210">Delete all the registry values under the following registry subkey except for **AgentVersion**, **EncodedComputerName**, and **Installed**:</span></span><br />
**<span data-ttu-id="608f5-211">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM</span><span class="sxs-lookup"><span data-stu-id="608f5-211">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM</span></span>**

    <span data-ttu-id="608f5-212">**Примечание** Чтобы изменения вступили в силу, необходимо перезапустить агент MBAM.</span><span class="sxs-lookup"><span data-stu-id="608f5-212">**Note** You must restart the MBAM agent for the changes to take effect.</span></span>

<span data-ttu-id="608f5-213">Имейте в виду, что после применения групповой политики на компьютере эти значения могут вернуться к исходным параметрам.</span><span class="sxs-lookup"><span data-stu-id="608f5-213">Be aware that after you apply Group Policy to the computer, these values may revert to their original settings.</span></span>

### <span data-ttu-id="608f5-214">Неполадка WMI</span><span class="sxs-lookup"><span data-stu-id="608f5-214">WMI issue</span></span>

<span data-ttu-id="608f5-215">MBAM использует методы класса win32_encryptablevolume для управления шифрованием BitLocker.</span><span class="sxs-lookup"><span data-stu-id="608f5-215">MBAM uses methods of the win32_encryptablevolume class to manage BitLocker.</span></span> <span data-ttu-id="608f5-216">Если этот модуль не зарегистрирован или поврежден, клиент MBAM будет работать неправильно, и в журнале событий администратора MBAM появится следующая запись о событии:</span><span class="sxs-lookup"><span data-stu-id="608f5-216">If this module is unregistered or corrupted, the MBAM client will not operate correctly, and you will see the following event entry in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

<span data-ttu-id="608f5-217">Кроме того, вы можете заметить, что политики восстановления и оборудования не применяются с кодом ошибки 0x8007007e.</span><span class="sxs-lookup"><span data-stu-id="608f5-217">Additionally, you may notice that the Recovery and Hardware policies do not apply with Error Code 0x8007007e.</span></span> <span data-ttu-id="608f5-218">Это означает, что указанный модуль не найден.</span><span class="sxs-lookup"><span data-stu-id="608f5-218">This translates to "The specified module could not be found."</span></span>

<span data-ttu-id="608f5-219">Чтобы устранить эту проблему, перерегистрируйте класс **Win32_EncryptableVolume** с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="608f5-219">To resolve this issue, you should reregister the **win32_encryptablevolume** class by using the following command:</span></span>

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <span data-ttu-id="608f5-220">Устранение проблем с связью с агентом MBAM</span><span class="sxs-lookup"><span data-stu-id="608f5-220">Troubleshooting MBAM Agent communication issues</span></span>

<span data-ttu-id="608f5-221">В этом разделе содержатся сведения об устранении перечисленных ниже проблем, связанных с связью с агентом MBAM.</span><span class="sxs-lookup"><span data-stu-id="608f5-221">This section contains troubleshooting information for the following issues that are related to MBAM agent communication:</span></span>

### <span data-ttu-id="608f5-222">Неверный URL-адрес службы MBAM</span><span class="sxs-lookup"><span data-stu-id="608f5-222">Incorrect MBAM service URL</span></span>

<span data-ttu-id="608f5-223">Если значение службы состояния соответствия MBAM или служба восстановления и оборудования не задано правильно, в журнале событий администратора MBAM на клиентском компьютере появится запись о событии, похожую на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="608f5-223">If the value of MBAM Compliance Status Service or Recovery and Hardware Service is incorrect, you'll see an event entry that resembles the following in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

<span data-ttu-id="608f5-224">Проверьте значения параметров **KeyRecoveryServiceEndPoint** и **StatusReportingServiceEndpoint** в следующем разделе реестра на клиентском компьютере:</span><span class="sxs-lookup"><span data-stu-id="608f5-224">Verify the values of **KeyRecoveryServiceEndPoint** and **StatusReportingServiceEndpoint** under the following registry subkey on the client computer:</span></span> <br />
**<span data-ttu-id="608f5-225">HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span><span class="sxs-lookup"><span data-stu-id="608f5-225">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

<span data-ttu-id="608f5-226">По умолчанию URL-адрес KeyRecoveryServiceEndPoint (конечная точка для восстановления MBAM и службы оборудования) имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="608f5-226">By default, the URL for KeyRecoveryServiceEndPoint (MBAM Recovery and Hardware service endpoint) is in the following format:</span></span> <br />
**<span data-ttu-id="608f5-227">http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="608f5-227">http://\<servername\>:\<port\>/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>**

<span data-ttu-id="608f5-228">По умолчанию URL-адрес для StatusReportingServiceEndpoint (конечная точка службы отчетов о состоянии MBAM) имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="608f5-228">By default, the URL for StatusReportingServiceEndpoint (MBAM Status reporting service endpoint) is in the following format:</span></span><br />
**<span data-ttu-id="608f5-229">http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="608f5-229">http://\<servername\>:\<port\>/MBAMComplianceStatusService/StatusReportingService.svc</span></span>**

> [!Note]
> <span data-ttu-id="608f5-230">В URL-адресе не должно быть пробелов.</span><span class="sxs-lookup"><span data-stu-id="608f5-230">There should be no spaces in the URL.</span></span>

<span data-ttu-id="608f5-231">Если URL-адрес службы неверен, необходимо исправить URL-адрес службы в следующем параметре групповой политики:</span><span class="sxs-lookup"><span data-stu-id="608f5-231">If the service URL is incorrect, you should correct the service URL in the following Group Policy setting:</span></span>

<span data-ttu-id="608f5-232">**Конфигурация компьютера**  >  **Политики**  >  **Административные шаблоны**  >  **Компоненты Windows**  >  **MBAM MDOP (Управление BitLocker)**  >  **Управление клиентами**  >  **Настройка служб MBAM**</span><span class="sxs-lookup"><span data-stu-id="608f5-232">**Computer configuration** > **Policies** > **Administrative Templates** > **Windows Components** > **MDOP MBAM (BitLocker Management)** > **Client Management** > **Configure MBAM Services**</span></span>

### <span data-ttu-id="608f5-233">Проблема с подключением, влияющая на сервер администрирования MBAM</span><span class="sxs-lookup"><span data-stu-id="608f5-233">Connectivity issue that affects the MBAM administration server</span></span>

<span data-ttu-id="608f5-234">Если между агентом клиента и сервером администрирования MBAM есть проблемы с подключением, агент MBAM не сможет публиковать обновления базы данных.</span><span class="sxs-lookup"><span data-stu-id="608f5-234">The MBAM agent will be unable to post any updates to the database if connectivity issues exist between the client agent and the MBAM administration server.</span></span> <span data-ttu-id="608f5-235">В этом случае в журнале событий администратора MBAM на клиентском компьютере будут замечены ошибки подключения.</span><span class="sxs-lookup"><span data-stu-id="608f5-235">In this case, you will notice connectivity failure entries in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

<span data-ttu-id="608f5-236">Основные проверки:</span><span class="sxs-lookup"><span data-stu-id="608f5-236">Basic checks:</span></span>

* <span data-ttu-id="608f5-237">Убедитесь в том, что для проверки основных подключений используется команда ping для сервера администрирования MBAM по имени и IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="608f5-237">Verify basic connectivity by pinging the MBAM administration server by name and IP.</span></span> <span data-ttu-id="608f5-238">Убедитесь, что вы можете подключиться к веб-сайту администрирования MBAM или порту службы, используя Telnet или Portqry.</span><span class="sxs-lookup"><span data-stu-id="608f5-238">Check whether you can connect to the MBAM administration website or service port by using telnet or portqry.</span></span>

* <span data-ttu-id="608f5-239">Убедитесь, что служба IIS запущена на сервере администрирования и мониторинга MBAM и что веб-служба MBAM прослушивает тот же порт, который настроен на клиентском компьютере MBAM ( `netstat –ano | find "portnumber"` ).</span><span class="sxs-lookup"><span data-stu-id="608f5-239">Verify that the IIS service is running on the MBAM administration and monitoring server and that the MBAM web service is listening on the same port that is configured on the MBAM client computer (`netstat –ano | find "portnumber"`).</span></span>

* <span data-ttu-id="608f5-240">Убедитесь, что номер порта, настроенный для веб-сайта MBAM, использует диспетчер IIS (inetmgr).</span><span class="sxs-lookup"><span data-stu-id="608f5-240">Verify that the port number that is configured for the MBAM website is using IIS Manager (inetmgr).</span></span> <span data-ttu-id="608f5-241">Убедитесь, что номер порта совпадает с номером порта, который прослушивает клиент.</span><span class="sxs-lookup"><span data-stu-id="608f5-241">Make sure that the port number is the same as the port number on which the client is listening.</span></span> <span data-ttu-id="608f5-242">Убедитесь, что номер порта не является общим для другого приложения.</span><span class="sxs-lookup"><span data-stu-id="608f5-242">Make sure that the port number is not shared by another application.</span></span> <span data-ttu-id="608f5-243">Например, другое приложение на сервере не должно использовать один и тот же порт.</span><span class="sxs-lookup"><span data-stu-id="608f5-243">For example, another application on the server should not be using the same port.</span></span>

* <span data-ttu-id="608f5-244">Если у вас есть брандмауэр, убедитесь, что порт открыт в брандмауэре или прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="608f5-244">If there is a firewall, make sure that the port is open in the firewall or proxy server.</span></span>

* <span data-ttu-id="608f5-245">Если связь между клиентом и сервером является безопасной, убедитесь в том, что вы используете допустимый SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="608f5-245">If the communication between client and server is secure, make sure that you are using a valid SSL certificate.</span></span>

* <span data-ttu-id="608f5-246">Проверьте сетевое соединение между веб-сервером и сервером базы данных, на который будут отправляться данные для вставки.</span><span class="sxs-lookup"><span data-stu-id="608f5-246">Verify network connectivity between the web server and the database server to which the data is sent for insertion.</span></span> <span data-ttu-id="608f5-247">Вы можете проверить подключение к базе данных с веб-сервера на сервер базы данных с помощью администратора источников данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="608f5-247">You can check database connectivity from the web server to the database server by using ODBC Data Source Administrator.</span></span> <span data-ttu-id="608f5-248">Подробные сведения об устранении неполадок подключения к SQL Server можно найти в статье [Устранение неполадок при подключении к ядру СУБД SQL Server](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span><span class="sxs-lookup"><span data-stu-id="608f5-248">Detailed SQL Server connection troubleshooting information is available in [How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span></span>

#### <span data-ttu-id="608f5-249">Устранение проблем с подключением</span><span class="sxs-lookup"><span data-stu-id="608f5-249">Troubleshooting the connectivity issue</span></span>

<span data-ttu-id="608f5-250">Убедитесь, что URL-адрес службы, настроенный на клиенте, задан правильно.</span><span class="sxs-lookup"><span data-stu-id="608f5-250">Make sure that the service URL that is configured on the client is correct.</span></span> <span data-ttu-id="608f5-251">Скопируйте значение URL-адреса для KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) из реестра и откройте его в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="608f5-251">Copy the value of the URL for KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) from the registry, and open it in Internet Explorer.</span></span>

<span data-ttu-id="608f5-252">Аналогичным образом скопируйте значение URL-адреса для StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) и откройте его в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="608f5-252">Similarly, copy the value of the URL for StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**), and open it in Internet Explorer.</span></span>

> [!Note]
> <span data-ttu-id="608f5-253">Если вам не удается найти URL-адрес на клиентском компьютере, необходимо протестировать базовое подключение клиента к серверу, на котором запущены службы IIS.</span><span class="sxs-lookup"><span data-stu-id="608f5-253">If you cannot browse to the URL from the client computer, you should test basic network connectivity from the client to the server that is running IIS.</span></span> <span data-ttu-id="608f5-254">Просмотрите пункты 1, 2, 3 и 4 в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="608f5-254">See points 1, 2, 3, and 4 in the previous section.</span></span>

<span data-ttu-id="608f5-255">Кроме того, проверьте журналы приложений на сервере администрирования и мониторинга на наличие ошибок.</span><span class="sxs-lookup"><span data-stu-id="608f5-255">Additionally, review the Application logs on the administration and monitoring server for any errors.</span></span>

<span data-ttu-id="608f5-256">Вы можете создать одновременную трассировку сети между клиентом и сервером и проанализировать трассировку, чтобы определить причину сбоя соединения между агентом клиента и сервером администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="608f5-256">You can make a concurrent network trace between the client and the server, and review the trace to determine the cause of connection failure between the client agent and the MBAM administration server.</span></span>

> [!Note]
> <span data-ttu-id="608f5-257">Если вы можете найти URL-адреса службы на клиентском компьютере и в журналах событий администрирования MBAM есть ошибки подключения, это может быть вызвано сбоем подключения между сервером администрирования и сервером базы данных.</span><span class="sxs-lookup"><span data-stu-id="608f5-257">If you can browse to the service URLs from the client computer and there are connectivity error entries in the MBAM admin event logs, this might be because of a connectivity failure between the administration server and the database server.</span></span>

<span data-ttu-id="608f5-258">Если вы можете успешно перейти к обоим URL-адресам службы и есть связь между клиентом и сервером, служба IIS работает.</span><span class="sxs-lookup"><span data-stu-id="608f5-258">If you can successfully browse to both service URLs, and there is connectivity between the client and the server that is running, IIS is working.</span></span> <span data-ttu-id="608f5-259">Однако может возникнуть проблема с обменом данными между сервером, на котором запущены службы IIS и сервером базы данных.</span><span class="sxs-lookup"><span data-stu-id="608f5-259">However, there may be a problem in communication between the server that is running IIS and the database server.</span></span>

<span data-ttu-id="608f5-260">Возможно, службы MBAM не смогут подключиться к серверу базы данных из-за сетевой ошибки или неверной настройки строки подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="608f5-260">The MBAM services may be unable to connect to the database server because of a network issue or an incorrect database connection string setting.</span></span> <span data-ttu-id="608f5-261">Просматривайте журналы приложений на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="608f5-261">Review the Application logs on the administration and monitoring server.</span></span> <span data-ttu-id="608f5-262">Вы можете столкнуться с ошибками в записях или предупреждениях исходного ASP.NET 2.0.50727.0, которые похожи на следующую запись в журнале:</span><span class="sxs-lookup"><span data-stu-id="608f5-262">You might see errors entries or warnings from source ASP.NET 2.0.50727.0 that resemble the following log entry:</span></span>

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### <span data-ttu-id="608f5-263">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="608f5-263">Possible causes</span></span>

##### <span data-ttu-id="608f5-264">Причина 1</span><span class="sxs-lookup"><span data-stu-id="608f5-264">Cause 1</span></span>

<span data-ttu-id="608f5-265">Возможно, администратор указал недействительное имя или имя базы данных в процессе установки сервера администрирования и мониторинга серверных компонентов.</span><span class="sxs-lookup"><span data-stu-id="608f5-265">The administrator may have specified an invalid database instance name/database name during installation of administration and monitoring server components.</span></span>

<span data-ttu-id="608f5-266">Вы можете проверить и исправить строки подключения к базе данных с помощью консоли управления IIS.</span><span class="sxs-lookup"><span data-stu-id="608f5-266">You can verify and correct the database connection strings by using the IIS Management console.</span></span> <span data-ttu-id="608f5-267">Для этого откройте Диспетчер IIS и перейдите к Администрирование и мониторинг Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="608f5-267">To do this, open IIS Manager, and browse to Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="608f5-268">Для каждой службы, указанной в левой части экрана, выполните указанные ниже действия, чтобы изменить строки подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="608f5-268">For each service that is listed on the left side, follow these steps to change the database connection strings:</span></span>

1. <span data-ttu-id="608f5-269">В **представлении функции**дважды щелкните **строку подключения**.</span><span class="sxs-lookup"><span data-stu-id="608f5-269">In **Features View**, double-select **Connection Strings**.</span></span>

2. <span data-ttu-id="608f5-270">На странице **строки соединения** выберите строку подключения, которую вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="608f5-270">On the **Connection Strings** page, select the connection string that you want to change.</span></span>

3. <span data-ttu-id="608f5-271">На панели **действия** нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="608f5-271">In the **Actions** pane, select **Edit**.</span></span>

4. <span data-ttu-id="608f5-272">В диалоговом окне **изменение строки подключения** измените свойства, которые нужно изменить, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="608f5-272">In the **Edit Connection String** dialog box, change the properties that you want to change, and then select **OK**.</span></span>

##### <span data-ttu-id="608f5-273">Причина 2</span><span class="sxs-lookup"><span data-stu-id="608f5-273">Cause 2</span></span>

<span data-ttu-id="608f5-274">Порт SQL Server заблокирован в брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="608f5-274">SQL Server port blocked in firewall.</span></span> <span data-ttu-id="608f5-275">Проверьте номер порта, на котором установлен SQL Server для прослушивания, и убедитесь, что порт открыт в брандмауэре между сервером администрирования и сервером баз данных.</span><span class="sxs-lookup"><span data-stu-id="608f5-275">Verify the port number to which SQL Server is configured to listen, and make sure that the port is open in the firewall between the administration server and database server.</span></span>

##### <span data-ttu-id="608f5-276">Причина 3</span><span class="sxs-lookup"><span data-stu-id="608f5-276">Cause 3</span></span>

<span data-ttu-id="608f5-277">Неверные привязки TCP/IP для сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="608f5-277">Incorrect SQL server TCP/IP bindings.</span></span> <span data-ttu-id="608f5-278">Проверьте привязки SQL TCP/IP в диспетчере конфигурации SQL Server на сервере базы данных.</span><span class="sxs-lookup"><span data-stu-id="608f5-278">Verify SQL TCP/IP bindings in SQL Server Configuration Manager on the database server.</span></span> <span data-ttu-id="608f5-279">Для подключения к базе данных MBAM требуется, чтобы были включены протоколы TCP/IP и именованные каналы.</span><span class="sxs-lookup"><span data-stu-id="608f5-279">MBAM requires that the TCP/IP and Named Pipes protocols are enabled to connect to the database.</span></span>

##### <span data-ttu-id="608f5-280">Причина 4</span><span class="sxs-lookup"><span data-stu-id="608f5-280">Cause 4</span></span>

<span data-ttu-id="608f5-281">Учетная запись NT Authority\Network Service или сервер администрирования MBAM не имеет необходимых разрешений для подключения к базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="608f5-281">The NT Authority\Network Service account or the MBAM Administration Server’s computer account doesn't have the required permissions to connect to the SQL database.</span></span>

<span data-ttu-id="608f5-282">При установке компонентов базы данных на сервере базы данных установщик создает две локальные группы: Проверка соответствия MBAM доступа к БД и восстановление MBAM и доступ к данным оборудования.</span><span class="sxs-lookup"><span data-stu-id="608f5-282">During the installation of database components on the database server, the installer creates two local groups: MBAM Compliance Auditing DB Access and MBAM Recovery and Hardware DB Access.</span></span>

<span data-ttu-id="608f5-283">Учетная запись NT Authority\Network Service, учетная запись сервера администрирования MBAM и пользователь, который устанавливает компоненты базы данных, автоматически добавляются в эти группы.</span><span class="sxs-lookup"><span data-stu-id="608f5-283">The NT Authority\Network Service account, the MBAM administration server’s computer account, and the user who installs the database components are automatically added to these groups.</span></span>

<span data-ttu-id="608f5-284">Эти группы получают необходимые разрешения на доступ к базе данных во время установки.</span><span class="sxs-lookup"><span data-stu-id="608f5-284">These groups are granted the required permissions on the database during the installation.</span></span> <span data-ttu-id="608f5-285">Все пользователи, входящие в эту группу, автоматически получают необходимые разрешения на доступ к базе данных.</span><span class="sxs-lookup"><span data-stu-id="608f5-285">All users who are part of this group automatically receive the required permissions on the database.</span></span>

<span data-ttu-id="608f5-286">Возможно, веб-служба не подключается к серверу базы данных вследствие проблем с разрешениями, если выполняется одно или несколько из указанных ниже условий.</span><span class="sxs-lookup"><span data-stu-id="608f5-286">The web service may not connect to the database server because of a permissions issue if one or more of the following conditions are true:</span></span>

* <span data-ttu-id="608f5-287">Упомянутые ранее группы удаляются из локальных групп на сервере базы данных.</span><span class="sxs-lookup"><span data-stu-id="608f5-287">The groups that were mentioned earlier are removed from the local groups on the database server.</span></span>

* <span data-ttu-id="608f5-288">Учетная запись NT Authority\Network Service и учетная запись сервера администрирования MBAM не являются членами этих групп.</span><span class="sxs-lookup"><span data-stu-id="608f5-288">The NT Authority\Network Service account and the MBAM administration server’s computer account are not members of these groups.</span></span>

* <span data-ttu-id="608f5-289">Эти группы не обладают необходимыми разрешениями для базы данных.</span><span class="sxs-lookup"><span data-stu-id="608f5-289">These groups do not have the required permissions on the database.</span></span>

<span data-ttu-id="608f5-290">Ошибки, связанные с разрешениями, будут регистрироваться в журналах приложений на сервере администрирования и мониторинга MBAM, если хотя бы одно из предыдущих условий истинно.</span><span class="sxs-lookup"><span data-stu-id="608f5-290">You will notice permissions-related errors in the Application logs on the MBAM administration and monitoring server if any of the previous conditions are true.</span></span> <span data-ttu-id="608f5-291">В этом случае необходимо вручную добавить учетную запись NT Authority\Network Service и сервер администрирования MBAM и предоставить им общую роль сервера базы данных SQL, использующую SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .</span><span class="sxs-lookup"><span data-stu-id="608f5-291">In that case, you should manually add the NT Authority\Network Service account and MBAM administration server’s computer account and grant them a server-wide public role on the SQL database server that is using SQL Server Management Studio (https://msdn.microsoft.com/library/aa337562.aspx).</span></span>

#### <span data-ttu-id="608f5-292">Просмотр журналов веб-службы</span><span class="sxs-lookup"><span data-stu-id="608f5-292">Review the web service logs</span></span>

<span data-ttu-id="608f5-293">Если ни одно из событий не зарегистрировано в журналах приложений на сервере администрирования MBAM, можно просмотреть журналы веб-службы (SVCLOG) веб-службы MBAM, размещенные на сервере администрирования MBAM и сервера мониторинга.</span><span class="sxs-lookup"><span data-stu-id="608f5-293">If no events are logged in the Application logs on the MBAM administration server, it’s time to review the web service logs (.svclog) of the MBAM web service that is hosted on the MBAM administration and monitoring server.</span></span> <span data-ttu-id="608f5-294">Для просмотра файла журнала необходимо использовать средство просмотра трассировки службы (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx .</span><span class="sxs-lookup"><span data-stu-id="608f5-294">You will have to use the Service Trace Viewer Tool (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx to view the log file.</span></span>

<span data-ttu-id="608f5-295">В первую очередь следует исследовать журналы трассировки служб RecoveryandHardwareService и ComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="608f5-295">You should primarily investigate the service trace logs of RecoveryandHardwareService and ComplianceStatusService.</span></span> <span data-ttu-id="608f5-296">По умолчанию журналы веб-службы находятся в папке Solution\Logs управления C:\inetpub\Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="608f5-296">By default, web service logs are located in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span> <span data-ttu-id="608f5-297">Каждая служба записывает файл. svclog в свою папку.</span><span class="sxs-lookup"><span data-stu-id="608f5-297">There, each service writes its .svclog file under its own folder.</span></span>

<span data-ttu-id="608f5-298">Проверьте активность в журнале трассировки служб на предмет ошибок или предупреждений.</span><span class="sxs-lookup"><span data-stu-id="608f5-298">Review the activity in the service trace log for any error or warning entries.</span></span> <span data-ttu-id="608f5-299">По умолчанию записи ошибок выделены красным цветом.</span><span class="sxs-lookup"><span data-stu-id="608f5-299">By default, error entries are highlighted in red.</span></span> <span data-ttu-id="608f5-300">Чтобы просмотреть подробные сведения об ошибке, щелкните описание ошибки на правой панели средства просмотра трассировки.</span><span class="sxs-lookup"><span data-stu-id="608f5-300">Select the error description on the right pane of the trace viewer to view detailed information about the error entry.</span></span> <span data-ttu-id="608f5-301">Ниже приведен пример записи об ошибке из журнала трассировки.</span><span class="sxs-lookup"><span data-stu-id="608f5-301">The following is a sample error entry from the trace log:</span></span>

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## <span data-ttu-id="608f5-302">Переустановка или повторная настройка инфраструктуры MBAM</span><span class="sxs-lookup"><span data-stu-id="608f5-302">Re-installation or reconfiguration of MBAM infrastructure</span></span>

<span data-ttu-id="608f5-303">Для переустановки или повторной настройки инфраструктуры MBAM необходимо знать следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="608f5-303">To re-install or reconfigure MBAM infrastructure, you must know the following things:</span></span>

* <span data-ttu-id="608f5-304">Учетная запись пула приложений</span><span class="sxs-lookup"><span data-stu-id="608f5-304">Application Pool account</span></span>

* <span data-ttu-id="608f5-305">Группы MBAM (служба поддержки, Группа "Пользователи отчета")</span><span class="sxs-lookup"><span data-stu-id="608f5-305">MBAM Groups (Helpdesk, Advanced, Report Users Group)</span></span>

* <span data-ttu-id="608f5-306">URL-адрес отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="608f5-306">MBAM Reports URL</span></span>

* <span data-ttu-id="608f5-307">Имя сервера SQL Server и имена баз данных</span><span class="sxs-lookup"><span data-stu-id="608f5-307">SQL Server name and database names</span></span>

* <span data-ttu-id="608f5-308">Учетные записи MBAM ReadWrite и ReadOnly</span><span class="sxs-lookup"><span data-stu-id="608f5-308">MBAM ReadWrite and ReadOnly Accounts</span></span>

### <span data-ttu-id="608f5-309">Учетная запись пула приложений</span><span class="sxs-lookup"><span data-stu-id="608f5-309">Application Pool account</span></span>

<span data-ttu-id="608f5-310">Чтобы найти учетную запись пула приложений, войдите на веб-сервер MBAM, откройте **Диспетчер служб IIS**и выберите **Пулы приложений**.</span><span class="sxs-lookup"><span data-stu-id="608f5-310">To find the Application Pool account, log on to the MBAM Web Server, open **Internet Information Services (IIS) Manager**, and then select **Application Pools**:</span></span>

![пулы приложений](images/troubleshooting-MBAM-installation-1.png)

<span data-ttu-id="608f5-312">Имя субъекта-службы (SPN) должно быть установлено в этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="608f5-312">The Service Principal Name (SPN) must be set in this account.</span></span> <span data-ttu-id="608f5-313">Этот параметр очень важен для функциональных возможностей MBAM.</span><span class="sxs-lookup"><span data-stu-id="608f5-313">This setting is very important to the functionality of MBAM.</span></span>

### <span data-ttu-id="608f5-314">Группы MBAM (служба поддержки, Группа "Пользователи отчетов" и URL-адрес отчетов)</span><span class="sxs-lookup"><span data-stu-id="608f5-314">MBAM Groups (Helpdesk, Advanced, Report Users Group and Reports URL)</span></span>

![Группы MBAM](images/troubleshooting-MBAM-installation-2.png)

<span data-ttu-id="608f5-316">Это предоставляет такие сведения, как группа "служба поддержки", Группа "дополнительные службы поддержки", Группа "Пользователи отчетов" и URL-адреса отчетов MBAM.</span><span class="sxs-lookup"><span data-stu-id="608f5-316">This provides information such as Helpdesk Group, Advanced Helpdesk Group, Report Users group, and MBAM Reports URL.</span></span> <span data-ttu-id="608f5-317">URL-адрес отчетов MBAM должен быть указан в настройке MBAM, и его следует прочитать следующим образом: HTTP (s)://servername/ReportServer.</span><span class="sxs-lookup"><span data-stu-id="608f5-317">The MBAM Reports URL must be provided in the MBAM setup and should read as: http(s)://servername/ReportServer.</span></span>

### <span data-ttu-id="608f5-318">Имена сервера SQL Server и имя базы данных (DB)</span><span class="sxs-lookup"><span data-stu-id="608f5-318">SQL Server name and database (DB) names</span></span>

<span data-ttu-id="608f5-319">Чтобы найти имена и экземпляры SQL Server, на которых размещена служба MBAM DBs, войдите в MBAM веб-сервер (IIS) и перейдите к разделу реестра folowing:</span><span class="sxs-lookup"><span data-stu-id="608f5-319">To find the SQL Server names and instances hosting the MBAM DBs, log on to the MBAM Web (IIS) server and browse to the folowing registry subkey:</span></span>

**<span data-ttu-id="608f5-320">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\Web</span><span class="sxs-lookup"><span data-stu-id="608f5-320">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web</span></span>**

![Программа](images/troubleshooting-MBAM-installation-3.png)

<span data-ttu-id="608f5-322">Выделенные части — это строки соединения.</span><span class="sxs-lookup"><span data-stu-id="608f5-322">The highlighted portions are connection strings.</span></span> <span data-ttu-id="608f5-323">Для них должны быть указаны имя сервера SQL Server, имена баз данных и экземпляры (если оно именовано).</span><span class="sxs-lookup"><span data-stu-id="608f5-323">These should have the SQL Server name, database names, and instances (if named).</span></span>

### <span data-ttu-id="608f5-324">Учетные записи MBAM ReadWrite и ReadOnly</span><span class="sxs-lookup"><span data-stu-id="608f5-324">MBAM ReadWrite and ReadOnly accounts</span></span>

<span data-ttu-id="608f5-325">Эти данные будут храниться в базе данных SQL Server, для которой имя уже найдено на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="608f5-325">This information will be in the SQL Server database, for which we already found the name from the web server.</span></span>

#### <span data-ttu-id="608f5-326">Учетная запись ReadWrite</span><span class="sxs-lookup"><span data-stu-id="608f5-326">ReadWrite account</span></span>

1. <span data-ttu-id="608f5-327">Войдите в центр управления SQL.</span><span class="sxs-lookup"><span data-stu-id="608f5-327">Log in to the SQL Management Studio.</span></span>

2. <span data-ttu-id="608f5-328">Щелкните правой кнопкой мыши **MBAM восстановления и оборудования**, выберите пункт **Свойства**и нажмите кнопку **разрешения**.</span><span class="sxs-lookup"><span data-stu-id="608f5-328">Right-click **MBAM Recovery and Hardware**, select **Properties**, and then select **Permissions**.</span></span>

<span data-ttu-id="608f5-329">Например, имя учетной записи лаборатории — **MBAMWrite**.</span><span class="sxs-lookup"><span data-stu-id="608f5-329">For example, The the lab account name is **MBAMWrite**.</span></span> <span data-ttu-id="608f5-330">Учетные записи в пуле приложений и на ReadWrite должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="608f5-330">The Application Pool and ReadWrite accounts are set to be the same.</span></span>

![БАЗА ДАННЫХ SQL](images/troubleshooting-MBAM-installation-4.png)

![Свойства базы данных](images/troubleshooting-MBAM-installation-5.png)

<span data-ttu-id="608f5-333">Перейдите к пункту **Безопасность** и войдите в **систему** в SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="608f5-333">Browse to **Security** and then **Logins** in SQL Management Studio.</span></span> <span data-ttu-id="608f5-334">Перейдите к учетной записи, показанной на предыдущем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="608f5-334">Browse to the account shown in the previous screenshot.</span></span>

![Безопасность SQL](images/troubleshooting-MBAM-installation-6.png)

<span data-ttu-id="608f5-336">Щелкните Учетные записи правой кнопкой мыши, выберите **Свойства сопоставление пользователей**и найдите базу данных восстановления MBAM и оборудования.</span><span class="sxs-lookup"><span data-stu-id="608f5-336">Right-click the accounts, go to **Properties User Mapping**, and locate the MBAM Recovery and Hardware database:</span></span>

![Сопоставление пользователей](images/troubleshooting-MBAM-installation-7.png)

#### <span data-ttu-id="608f5-338">Учетная запись только для чтения</span><span class="sxs-lookup"><span data-stu-id="608f5-338">ReadOnly account</span></span>

<span data-ttu-id="608f5-339">Откройте Диспетчер конфигураций служб SQL Server Reporting Services на сервере SSRS.</span><span class="sxs-lookup"><span data-stu-id="608f5-339">Open SQL Server Reporting Services Configuration Manager on the SSRS Server.</span></span> <span data-ttu-id="608f5-340">Выберите **URL-адрес диспетчера отчетов**, а затем найдите **URL-адреса**:</span><span class="sxs-lookup"><span data-stu-id="608f5-340">Select **Report Manager URL**, and then browse the **URLs**:</span></span>

![Диспетчер отчетов](images/troubleshooting-MBAM-installation-8.png)

<span data-ttu-id="608f5-342">Выберите **Администрирование и мониторинг Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="608f5-342">Select **Microsoft Bitlocker Administration and Monitoring**:</span></span>

![Администрирование и мониторинг BitLocker](images/troubleshooting-MBAM-installation-9.png)

<span data-ttu-id="608f5-344">Выберите **MaltaDatasource**:</span><span class="sxs-lookup"><span data-stu-id="608f5-344">Select **MaltaDatasource**:</span></span>

![DBs](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

<span data-ttu-id="608f5-347">Для MaltaDataSource должно быть задано имя учетной записи "только для чтения", и его следует использовать в настройке MBAM.</span><span class="sxs-lookup"><span data-stu-id="608f5-347">MaltaDataSource should have the ReadOnly Account name and should be used in MBAM setup.</span></span>

## <span data-ttu-id="608f5-348">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="608f5-348">Reference</span></span>

<span data-ttu-id="608f5-349">Дополнительные сведения доступны в следующих статьях.</span><span class="sxs-lookup"><span data-stu-id="608f5-349">For more information, see the following articles:</span></span>

[<span data-ttu-id="608f5-350">Развертывание MBAM 2,5 в автономной конфигурации</span><span class="sxs-lookup"><span data-stu-id="608f5-350">Deploying MBAM 2.5 in a standalone configuration</span></span>](https://support.microsoft.com/help/3046555)

[<span data-ttu-id="608f5-351">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="608f5-351">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
