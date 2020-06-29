---
title: Планирование требований групповой политики MBAM 1.0
description: Планирование требований групповой политики MBAM 1.0
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812437"
---
# <span data-ttu-id="30ea9-103">Планирование требований групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="30ea9-103">Planning for MBAM 1.0 Group Policy Requirements</span></span>


<span data-ttu-id="30ea9-104">Для управления клиентами администрирования и наблюдения (MBAM) Microsoft BitLocker требуются пользовательские параметры групповой политики, которые необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="30ea9-104">Microsoft BitLocker Administration and Monitoring (MBAM) Client management requires custom Group Policy settings to be applied.</span></span> <span data-ttu-id="30ea9-105">В этом разделе описаны доступные параметры политики для объекта групповой политики (GPO), которые можно использовать для управления шифрованием диска BitLocker в предприятии с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="30ea9-105">This topic describes the available policy options for Group Policy Object (GPO) when you use MBAM to manage BitLocker Drive Encryption in the enterprise.</span></span>

**<span data-ttu-id="30ea9-106">Важно.</span><span class="sxs-lookup"><span data-stu-id="30ea9-106">Important</span></span>**  
<span data-ttu-id="30ea9-107">MBAM не использует параметры GPO по умолчанию для шифрования диска Windows BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-107">MBAM does not use the default GPO settings for Windows BitLocker drive encryption.</span></span> <span data-ttu-id="30ea9-108">Если включены параметры по умолчанию, это может привести к конфликтам поведения.</span><span class="sxs-lookup"><span data-stu-id="30ea9-108">If the default settings are enabled, they can cause conflicting behavior.</span></span> <span data-ttu-id="30ea9-109">Чтобы включить MBAM для управления BitLocker, необходимо задать параметры политики GPO после установки шаблона групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="30ea9-109">To enable MBAM to manage BitLocker, you must define the GPO policy settings after you install the MBAM Group Policy Template.</span></span>



<span data-ttu-id="30ea9-110">После установки шаблона групповой политики MBAM вы можете просматривать и изменять доступные пользовательские параметры политики MBAM, которые позволят MBAM управлять шифрованием Enterprise BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-110">After you install the MBAM Group Policy template, you can view and modify the available custom MBAM GPO policy settings that enable MBAM to manage the enterprise BitLocker encryption.</span></span> <span data-ttu-id="30ea9-111">Шаблон групповой политики MBAM должен быть установлен на компьютере, на котором может выполняться консоль управления групповыми политиками (GPMC) или Расширенная технология MDOP для управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="30ea9-111">The MBAM Group Policy template must be installed on a computer that is capable of running the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) MDOP technology.</span></span> <span data-ttu-id="30ea9-112">Затем, чтобы изменить применимый объект групповой политики, откройте консоль управления групповыми политиками (GPMC) и перейдите к следующему узлу GPO: **конфигурации компьютера**, \\ **шаблоны**, \\ **компоненты Windows** \\ **MDOP MBAM (Управление BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="30ea9-112">Next, to edit the applicable GPO, open the GPMC or AGPM, and then navigate to the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<span data-ttu-id="30ea9-113">Узел GPO MDOP MBAM (BitLocker Management) включает четыре параметра глобальных политик и четыре дочерних узла параметров GPO соответственно.</span><span class="sxs-lookup"><span data-stu-id="30ea9-113">The MDOP MBAM (BitLocker Management) GPO node contains four global policy settings and four child GPO setting nodes, respectively.</span></span> <span data-ttu-id="30ea9-114">В параметрах глобальных политик GPO используются следующие параметры: Управление клиентами, несъемные диски, диски операционной системы и съемные диски.</span><span class="sxs-lookup"><span data-stu-id="30ea9-114">The four GPO global policy settings are: Client Management, Fixed Drive, Operating System Drive, and Removable Drive.</span></span> <span data-ttu-id="30ea9-115">В следующих разделах приведены определения политик и рекомендуемые параметры политики, которые помогут вам спланировать требования к параметрам политики MBAM GPO.</span><span class="sxs-lookup"><span data-stu-id="30ea9-115">The following sections provide policy definitions and suggested policy settings to help you plan for the MBAM GPO policy setting requirements.</span></span>

**<span data-ttu-id="30ea9-116">Примечание.</span><span class="sxs-lookup"><span data-stu-id="30ea9-116">Note</span></span>**  
<span data-ttu-id="30ea9-117">Дополнительные сведения о настройке минимально предложенных параметров GPO для включения MBAM управления шифрованием BitLocker вы узнаете, [как изменить параметры GPO MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md).</span><span class="sxs-lookup"><span data-stu-id="30ea9-117">For more information about configuring the minimum suggested GPO settings to enable MBAM to manage BitLocker encryption, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span>



## <span data-ttu-id="30ea9-118">Определения глобальных политик</span><span class="sxs-lookup"><span data-stu-id="30ea9-118">Global policy definitions</span></span>


<span data-ttu-id="30ea9-119">В этом разделе описаны определения глобальных политик MBAM, которые можно найти на следующем узле GPO: **Параметры конфигурации компьютера**, \\ **шаблоны**, \\ **компоненты Windows** \\ **MDOP MBAM (Управление BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="30ea9-119">This section describes the MBAM Global policy definitions, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30ea9-120">Имя политики</span><span class="sxs-lookup"><span data-stu-id="30ea9-120">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="30ea9-121">Общие сведения и рекомендуемый параметр политики</span><span class="sxs-lookup"><span data-stu-id="30ea9-121">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30ea9-122">Выбор метода шифрования диска и стойкости шифра</span><span class="sxs-lookup"><span data-stu-id="30ea9-122">Choose drive encryption method and cipher strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-123">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-123">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-124">Настройте эту политику, чтобы использовать определенный метод шифрования и стойкость шифра.</span><span class="sxs-lookup"><span data-stu-id="30ea9-124">Configure this policy to use a specific encryption method and cipher strength.</span></span></p>
<p><span data-ttu-id="30ea9-125">Если эта политика не настроена, BitLocker использует метод шифрования по умолчанию AES 128-bit с диффузором или методом шифрования, указанным в сценарии настройки.</span><span class="sxs-lookup"><span data-stu-id="30ea9-125">When this policy is not configured, BitLocker uses the default encryption method of AES 128-bit with Diffuser or the encryption method specified by the setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30ea9-126">Предотвращение перезаписи памяти при перезагрузке</span><span class="sxs-lookup"><span data-stu-id="30ea9-126">Prevent memory overwrite on restart</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-127">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-127">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-128">Настройте эту политику, чтобы повысить производительность при перезапуске, не перезаписывая Секреты BitLocker в памяти при перезапуске.</span><span class="sxs-lookup"><span data-stu-id="30ea9-128">Configure this policy to improve restart performance without overwriting BitLocker secrets in memory on restart.</span></span></p>
<p><span data-ttu-id="30ea9-129">Если эта политика не настроена, Секреты BitLocker удаляются из памяти при перезапуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="30ea9-129">When this policy is not configured, BitLocker secrets are removed from memory when the computer restarts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30ea9-130">Проверка правила использования сертификата смарт-карты</span><span class="sxs-lookup"><span data-stu-id="30ea9-130">Validate smart card certificate usage rule</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-131">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-131">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-132">Настройте эту политику на использование защиты BitLocker на основе сертификатов смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="30ea9-132">Configure this policy to use smartcard certificate-based BitLocker protection.</span></span></p>
<p><span data-ttu-id="30ea9-133">Если эта политика не настроена, для указания сертификата используется идентификатор объекта по умолчанию 1.3.6.1.4.1.311.67.1.1.</span><span class="sxs-lookup"><span data-stu-id="30ea9-133">When this policy is not configured, a default object identifier 1.3.6.1.4.1.311.67.1.1 is used to specify a certificate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30ea9-134">Предоставление уникальных идентификаторов для Организации</span><span class="sxs-lookup"><span data-stu-id="30ea9-134">Provide the unique identifiers for your organization</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-135">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-135">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-136">Настройте эту политику на использование агента восстановления данных на основе сертификатов или устройства чтения BitLocker to go.</span><span class="sxs-lookup"><span data-stu-id="30ea9-136">Configure this policy to use a certificate-based data recovery agent or the BitLocker To Go reader.</span></span></p>
<p><span data-ttu-id="30ea9-137">Если эта политика не настроена, <strong> поле "Идентификация" </strong> не используется.</span><span class="sxs-lookup"><span data-stu-id="30ea9-137">When this policy is not configured, the <strong>Identification</strong> field is not used.</span></span></p>
<p><span data-ttu-id="30ea9-138">Если в вашей компании требуется более высокий уровень безопасности, может потребоваться настроить <strong> поле идентификация, </strong> чтобы убедиться, что все USB-устройства имеют этот параметр и что они выровнены с помощью этого параметра групповой политики.</span><span class="sxs-lookup"><span data-stu-id="30ea9-138">If your company requires higher security measurements, you may want to configure the <strong>Identification</strong> field to make sure that all USB devices have this field set and that they are aligned with this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="30ea9-139">Определения политики управления клиентом</span><span class="sxs-lookup"><span data-stu-id="30ea9-139">Client Management policy definitions</span></span>


<span data-ttu-id="30ea9-140">В этом разделе описаны определения политик управления клиентами для MBAM, которые можно найти на следующем узле GPO: **Конфигурация компьютера**, \\ **шаблоны**, \\ **элементы управления Windows**, службы \\ **MDOP MBAM (Управление BitLocker)**  \\  **Client Management**.</span><span class="sxs-lookup"><span data-stu-id="30ea9-140">This section describes the Client Management policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Client Management**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30ea9-141">Имя политики</span><span class="sxs-lookup"><span data-stu-id="30ea9-141">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="30ea9-142">Общие сведения и рекомендуемые параметры политики</span><span class="sxs-lookup"><span data-stu-id="30ea9-142">Overview and Suggested Policy Settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30ea9-143">Настройка служб MBAM</span><span class="sxs-lookup"><span data-stu-id="30ea9-143">Configure MBAM Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-144">Рекомендуемая конфигурация: <strong> включена</span><span class="sxs-lookup"><span data-stu-id="30ea9-144">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="30ea9-145">Конечная точка восстановления MBAM и обслуживания оборудования </strong> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-145">MBAM Recovery and Hardware service endpoint</strong>.</span></span> <span data-ttu-id="30ea9-146">Это первый параметр политики, который необходимо настроить для включения управления шифрованием клиента BitLocker MBAM.</span><span class="sxs-lookup"><span data-stu-id="30ea9-146">This is the first policy setting that you must configure to enable the MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="30ea9-147">Для этого параметра введите расположение конечной точки, как показано в следующем примере: <strong> http:// </strong><em> &lt; MBAM администрирование и сервер мониторинга &gt; </em><strong> : </strong><em> &lt; порт, с которым связана веб-служба, с &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-147">For this setting, enter the endpoint location similar to the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMRecoveryAndHardwareService/CoreService.svc</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="30ea9-148">Выберите сведения о восстановлении BitLocker, которые нужно сохранить </strong> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-148">Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="30ea9-149">Этот параметр политики позволяет настроить службу восстановления ключа для резервного копирования данных восстановления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-149">This policy setting lets you configure the key recovery service to back up the BitLocker recovery information.</span></span> <span data-ttu-id="30ea9-150">Кроме того, она позволяет настроить службу отчетов о состоянии для сбора отчетов о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="30ea9-150">It also lets you configure the status reporting service for collecting compliance and audit reports.</span></span> <span data-ttu-id="30ea9-151">Политика предоставляет административный способ восстановления данных, зашифрованных с помощью BitLocker, для предотвращения потери данных из-за отсутствия ключевых данных.</span><span class="sxs-lookup"><span data-stu-id="30ea9-151">The policy provides an administrative method of recovering data encrypted by BitLocker to help prevent data loss due to the lack of key information.</span></span> <span data-ttu-id="30ea9-152">Отчет о состоянии и действие по восстановлению ключа автоматически и без уведомления будут отправляться в настроенное расположение сервера отчетов.</span><span class="sxs-lookup"><span data-stu-id="30ea9-152">Status report and key recovery activity will automatically and silently be sent to the configured report server location.</span></span></p>
<p><span data-ttu-id="30ea9-153">Если вы не настраиваете этот параметр политики или отключите его, данные восстановления ключа не будут сохранены, а отчет о состоянии и действие по восстановлению ключа не будут переданы на сервер.</span><span class="sxs-lookup"><span data-stu-id="30ea9-153">If you do not configure or if you disable this policy setting, the key recovery information will not be saved, and status report and key recovery activity will not be reported to server.</span></span> <span data-ttu-id="30ea9-154">Если для этого параметра задан <strong> пароль восстановления и пакет ключей </strong> , пароль восстановления и пакет ключа будут автоматически и без предупреждения архивироваться на настроенное расположение сервера восстановления ключа.</span><span class="sxs-lookup"><span data-stu-id="30ea9-154">When this setting is set to <strong>Recovery Password and key package</strong>, the recovery password and key package will be automatically and silently backed up to the configured key recovery server location.</span></span></p></li>
<li><p><strong><span data-ttu-id="30ea9-155">Введите частоту проверки состояния клиента (в минутах) </strong> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-155">Enter the client checking status frequency in minutes</strong>.</span></span> <span data-ttu-id="30ea9-156">Этот параметр политики управляет частотой, с которой клиент проверяет политики защиты BitLocker и состояние на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="30ea9-156">This policy setting manages how frequently the client checks the BitLocker protection policies and the status on the client computer.</span></span> <span data-ttu-id="30ea9-157">Этот параметр также управляет частотой сохранения состояния соответствия клиентов на сервере.</span><span class="sxs-lookup"><span data-stu-id="30ea9-157">This policy also manages how frequently the client compliance status is saved to the server.</span></span> <span data-ttu-id="30ea9-158">Клиент проверяет политики защиты BitLocker и состояние на клиентском компьютере, а также выполняет резервное копирование ключа восстановления клиента с настроенной частотой.</span><span class="sxs-lookup"><span data-stu-id="30ea9-158">The client checks the BitLocker protection policies and status on the client computer, and it also backs up the client recovery key at the configured frequency.</span></span></p>
<p><span data-ttu-id="30ea9-159">Установите эту частоту на основе требования, установленного вашей компанией, для проверки состояния соответствия компьютера и частоту резервного копирования ключа восстановления клиента.</span><span class="sxs-lookup"><span data-stu-id="30ea9-159">Set this frequency based on the requirement established by your company on how frequently to check the compliance status of the computer, and how frequently to back up the client recovery key.</span></span></p></li>
<li><p><strong><span data-ttu-id="30ea9-160">Конечная точка службы отчетов о состоянии MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-160">MBAM Status reporting service endpoint</strong>.</span></span> <span data-ttu-id="30ea9-161">Это второй параметр политики, который необходимо настроить, чтобы включить управление шифрованием в клиенте MBAM клиента BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-161">This is the second policy setting that you must configure to enable MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="30ea9-162">Для этого параметра введите расположение конечной точки, используя следующий пример: <strong> http:// </strong><em> &lt; MBAM администрирование и сервер мониторинга &gt; </em><strong> : </strong><em> &lt; порт, с которым связана веб-служба. &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.</span><span class="sxs-lookup"><span data-stu-id="30ea9-162">For this setting, enter the endpoint location by using the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMComplianceStatusService/StatusReportingService.</span></span> <span data-ttu-id="30ea9-163">SVC </strong> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-163">svc</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30ea9-164">Разрешение проверки совместимости оборудования</span><span class="sxs-lookup"><span data-stu-id="30ea9-164">Allow hardware compatibility checking</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-165">Рекомендуемая конфигурация: <strong> включена</span><span class="sxs-lookup"><span data-stu-id="30ea9-165">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="30ea9-166">Этот параметр политики позволяет управлять проверкой совместимости оборудования перед включением защиты BitLocker на дисках клиентских компьютеров MBAM.</span><span class="sxs-lookup"><span data-stu-id="30ea9-166">This policy setting lets you manage the verification of hardware compatibility before you enable BitLocker protection on drives of MBAM client computers.</span></span></p>
<p><span data-ttu-id="30ea9-167">Этот параметр политики следует включить, если в вашей организации установлены старые аппаратные средства компьютера или компьютеры, не поддерживающие доверенный платформенный модуль (TPM).</span><span class="sxs-lookup"><span data-stu-id="30ea9-167">You should enable this policy option if your enterprise has older computer hardware or computers that do not support Trusted Platform Module (TPM).</span></span> <span data-ttu-id="30ea9-168">Если одно из этих условий истинно, включите проверку совместимости оборудования, чтобы убедиться, что MBAM применяется только к моделям компьютеров, поддерживающим BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-168">If either of these criteria is true, enable the hardware compatibility verification to make sure that MBAM is applied only to computer models that support BitLocker.</span></span> <span data-ttu-id="30ea9-169">Если все компьютеры в вашей организации поддерживают BitLocker, вам не нужно развертывать совместимость оборудования, и вы можете отключить параметр " <strong> не настраивать эту политику" </strong> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-169">If all computers in your organization support BitLocker, you do not have to deploy the Hardware Compatibility, and you can set this policy to <strong>Not Configured</strong>.</span></span></p>
<p><span data-ttu-id="30ea9-170">Если вы включите этот параметр политики, модель компьютера будет проверяться на совместимость со списком оборудования каждые 24 часа, прежде чем политика включит защиту BitLocker на диске компьютера.</span><span class="sxs-lookup"><span data-stu-id="30ea9-170">If you enable this policy setting, the model of the computer is validated against the hardware compatibility list once every 24 hours, before the policy enables BitLocker protection on a computer drive.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="30ea9-171">Примечание.</span><span class="sxs-lookup"><span data-stu-id="30ea9-171">Note</span></span></strong><br/><p><span data-ttu-id="30ea9-172">Перед включением этого параметра политики убедитесь в том, что вы настроили <strong> Параметры MBAM восстановления и конечной точки обслуживания оборудования в параметрах </strong> <strong> политики "настроить службы MBAM" </strong> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-172">Before enabling this policy setting, make sure that you have configured the <strong>MBAM Recovery and Hardware service endpoint</strong> setting in the <strong>Configure MBAM Services</strong> policy options.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="30ea9-173">Если вы отключаете или не настраиваете этот параметр политики, модель компьютера не проверяется относительно списка совместимого оборудования.</span><span class="sxs-lookup"><span data-stu-id="30ea9-173">If you either disable or do not configure this policy setting, the computer model is not validated against the hardware compatibility list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30ea9-174">Настройка политики исключения пользователей</span><span class="sxs-lookup"><span data-stu-id="30ea9-174">Configure user exemption policy</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-175">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-175">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-176">Этот параметр политики позволяет настроить адрес веб-сайта, адрес электронной почты или номер телефона, который позволит пользователю запросить исключение из шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-176">This policy setting lets you configure a web site address, email address, or phone number that will instruct a user to request an exemption from BitLocker encryption.</span></span></p>
<p><span data-ttu-id="30ea9-177">Если вы включаете этот параметр политики и предоставляете адрес веб-сайта, адрес электронной почты или номер телефона, пользователи увидят диалоговое окно с инструкциями по применению к исключению из защиты BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-177">If you enable this policy setting and provide a web site address, email address, or phone number, users will see a dialog with instructions on how to apply for an exemption from BitLocker protection.</span></span> <span data-ttu-id="30ea9-178">Дополнительные сведения о включении исключений шифрования BitLocker для пользователей можно найти <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> в разделе Управление исключениями шифрования BitLocker для пользователя </a> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-178">For more information about how to enable BitLocker encryption exemptions for users, see <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)">How to Manage User BitLocker Encryption Exemptions</a>.</span></span></p>
<p><span data-ttu-id="30ea9-179">Если вы отключаете или не настраиваете этот параметр политики, инструкции по применению к запросу на исключением не будут предоставляться пользователям.</span><span class="sxs-lookup"><span data-stu-id="30ea9-179">If you either disable or do not configure this policy setting, the instructions about how to apply for an exemption request will not be presented to users.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="30ea9-180">Примечание.</span><span class="sxs-lookup"><span data-stu-id="30ea9-180">Note</span></span></strong><br/><p><span data-ttu-id="30ea9-181">За исключением пользователей управляют пользователи, а не на компьютер.</span><span class="sxs-lookup"><span data-stu-id="30ea9-181">User exemption is managed per user, not per computer.</span></span> <span data-ttu-id="30ea9-182">Если несколько пользователей входят на один и тот же компьютер, а не исключаются, компьютер будет зашифрован.</span><span class="sxs-lookup"><span data-stu-id="30ea9-182">If multiple users log on to the same computer and one user is not exempt, the computer will be encrypted.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="30ea9-183">Определения политики для фиксированных дисков</span><span class="sxs-lookup"><span data-stu-id="30ea9-183">Fixed Drive policy definitions</span></span>


<span data-ttu-id="30ea9-184">В этом разделе описаны определения политик для фиксированных дисков для MBAM, которые можно найти на следующем узле GPO: **Параметры конфигурации компьютера**, \\ **шаблоны**, \\ **компоненты Windows** \\ **MDOP MBAM (Управление BitLocker)**  \\  **фиксированный диск**.</span><span class="sxs-lookup"><span data-stu-id="30ea9-184">This section describes the Fixed Drive policy definitions for MBAM, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Fixed Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30ea9-185">Имя политики</span><span class="sxs-lookup"><span data-stu-id="30ea9-185">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="30ea9-186">Общие сведения и рекомендуемый параметр политики</span><span class="sxs-lookup"><span data-stu-id="30ea9-186">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30ea9-187">Неисправленные параметры шифрования диска с данными</span><span class="sxs-lookup"><span data-stu-id="30ea9-187">Fixed data drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-188">Рекомендуемая конфигурация: <strong> включена </strong> и установите <strong> флажок Включить автоматическое снятие блокировки с фиксированным </strong> объемом данных, если требуется шифрование тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="30ea9-188">Suggested Configuration: <strong>Enabled</strong>, and select the <strong>Enable auto-unlock fixed data drive</strong> check box if the operating system volume is required to be encrypted.</span></span></p>
<p><span data-ttu-id="30ea9-189">Этот параметр политики позволяет управлять зашифрованием фиксированных дисков.</span><span class="sxs-lookup"><span data-stu-id="30ea9-189">This policy setting lets you manage whether or not to encrypt the fixed drives.</span></span></p>
<p><span data-ttu-id="30ea9-190">Когда вы включаете этот параметр политики, не отключайте <strong> параметр "настроить использование пароля для несъемных дисков с данными" </strong> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-190">When you enable this policy, do not disable the <strong>Configure use of password for fixed data drives</strong> policy.</span></span></p>
<p><span data-ttu-id="30ea9-191">Если установлен <strong> флажок Включить автоматическое снятие блокировки диска с данными </strong> , необходимо, чтобы том операционной системы был зашифрован.</span><span class="sxs-lookup"><span data-stu-id="30ea9-191">If the <strong>Enable auto-unlock fixed data drive</strong> check box is selected, the operating system volume must be encrypted.</span></span></p>
<p><span data-ttu-id="30ea9-192">Если вы включите этот параметр политики, пользователи должны будут разместить все съемные диски в разделе "Защита BitLocker", который будет шифровать диски.</span><span class="sxs-lookup"><span data-stu-id="30ea9-192">If you enable this policy setting, users are required to put all fixed drives under BitLocker protection, which will encrypt the drives.</span></span></p>
<p><span data-ttu-id="30ea9-193">Если вы не настраиваете этот параметр политики или отключаете этот параметр, пользователи не обязаны размещать фиксированные диски в разделе Защита BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-193">If you do not configure this policy or if you disable this policy, users are not required to put fixed drives under BitLocker protection.</span></span></p>
<p><span data-ttu-id="30ea9-194">Если этот параметр отключен, агент MBAM расшифровывает все зашифрованные несъемные диски.</span><span class="sxs-lookup"><span data-stu-id="30ea9-194">If you disable this policy, the MBAM agent decrypts any encrypted fixed drives.</span></span></p>
<p><span data-ttu-id="30ea9-195">Если шифрование тома операционной системы не является обязательным, снимите <strong> флажок Включить автоматическое снятие блокировки данных для фиксированного диска с данными </strong> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-195">If encrypting the operating system volume is not required, clear the <strong>Enable auto-unlock fixed data drive</strong> check box.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30ea9-196">Отказ от разрешения "запись" на съемные диски, не защищенные BitLocker</span><span class="sxs-lookup"><span data-stu-id="30ea9-196">Deny “write” permission to fixed drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-197">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-197">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-198">Этот параметр политики определяет, требуется ли защита BitLocker для фиксированных дисков на компьютере, чтобы они были доступны для записи.</span><span class="sxs-lookup"><span data-stu-id="30ea9-198">This policy setting determines if BitLocker protection is required for fixed drives on a computer so that they are writable.</span></span> <span data-ttu-id="30ea9-199">Этот параметр политики применяется, когда вы включаете BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-199">This policy setting is applied when you turn on BitLocker.</span></span></p>
<p><span data-ttu-id="30ea9-200">Если политика не настроена, все съемные диски на компьютере монтируются с разрешениями на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="30ea9-200">When the policy is not configured, all fixed drives on the computer are mounted with read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30ea9-201">Разрешение доступа к съемным дискам, защищенным с помощью BitLocker, из более ранних версий Windows</span><span class="sxs-lookup"><span data-stu-id="30ea9-201">Allow access to BitLocker-protected fixed drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-202">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-202">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-203">Включите эту политику, чтобы разблокировать и просмотреть съемные диски, отформатированные с помощью файловой системы FAT, на компьютерах под управлением Windows Server 2008, Windows Vista, Windows XP с пакетом обновления 3 (SP3) или Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="30ea9-203">Enable this policy to unlock and view the fixed drives that are formatted with the file allocation table (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="30ea9-204">Эти операционные системы имеют разрешения на доступ только для чтения к дискам, защищенным с помощью BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-204">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="30ea9-205">Если политика отключена, незаблокированные диски, отформатированные с помощью файловой системы FAT, нельзя будет просматривать на компьютерах под управлением Windows Server 2008, Windows Vista, Windows XP с пакетом обновления 3 (SP3) или Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="30ea9-205">When the policy is disabled, fixed drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30ea9-206">Настройка использования пароля для фиксированных дисков</span><span class="sxs-lookup"><span data-stu-id="30ea9-206">Configure use of password for fixed drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-207">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-207">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-208">Включите эту политику, чтобы настроить защиту паролем на съемных дисках.</span><span class="sxs-lookup"><span data-stu-id="30ea9-208">Enable this policy to configure password protection on fixed drives.</span></span></p>
<p><span data-ttu-id="30ea9-209">Если политика не настроена, пароли будут поддерживаться с параметрами по умолчанию, которые не включают требования к сложности пароля и требуют только восьми символов.</span><span class="sxs-lookup"><span data-stu-id="30ea9-209">When the policy is not configured, passwords will be supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="30ea9-210">Для более высокой безопасности включите эту политику и установите флажок <strong> требовать пароль для несъемного диска </strong> с данными, установите флажок требовать повышенную <strong> сложность пароля </strong> и укажите нужную <strong> минимальную длину пароля </strong> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-210">For higher security, enable this policy and select <strong>Require password for fixed data drive</strong>, select <strong>Require password complexity</strong>, and set the desired <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30ea9-211">Выбор способа восстановления несъемных дисков, защищенных с помощью BitLocker</span><span class="sxs-lookup"><span data-stu-id="30ea9-211">Choose how BitLocker-protected fixed drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-212">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-212">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-213">Настройте эту политику, чтобы включить агент восстановления данных BitLocker или сохранить сведения о восстановлении BitLocker в доменных службах Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="30ea9-213">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="30ea9-214">Если эта политика не настроена, агент восстановления данных BitLocker разрешен, и данные восстановления не заархивированы в доменные службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30ea9-214">When this policy is not configured, the BitLocker data recovery agent is allowed, and recovery information is not backed up to AD DS.</span></span> <span data-ttu-id="30ea9-215">Для MBAM не требуется создавать резервные копии данных для восстановления в доменных СЛУЖБах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30ea9-215">MBAM does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="30ea9-216">Определения политик для дисков операционной системы</span><span class="sxs-lookup"><span data-stu-id="30ea9-216">Operating System Drive policy definitions</span></span>


<span data-ttu-id="30ea9-217">В этом разделе описаны определения политик дисков операционной системы для MBAM, расположенные на следующем узле GPO: **Параметры конфигурации компьютера**, \\ **шаблоны**, \\ **компоненты Windows** \\ **MDOP MBAM (Управление BitLocker)**  \\  ,**диск операционной системы**.</span><span class="sxs-lookup"><span data-stu-id="30ea9-217">This section describes the Operating System Drive policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Operating System Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30ea9-218">Имя политики</span><span class="sxs-lookup"><span data-stu-id="30ea9-218">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="30ea9-219">Общие сведения и рекомендуемый параметр политики</span><span class="sxs-lookup"><span data-stu-id="30ea9-219">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30ea9-220">Параметры шифрования диска операционной системы</span><span class="sxs-lookup"><span data-stu-id="30ea9-220">Operating system drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-221">Рекомендуемая конфигурация: <strong> включена</span><span class="sxs-lookup"><span data-stu-id="30ea9-221">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="30ea9-222">Этот параметр политики определяет, будет ли диск операционной системы зашифрован.</span><span class="sxs-lookup"><span data-stu-id="30ea9-222">This policy setting determines if the operating system drive will be encrypted.</span></span></p>
<p><span data-ttu-id="30ea9-223">Настройте эту политику, чтобы сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="30ea9-223">Configure this policy to do the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="30ea9-224">Принудительная защита BitLocker для диска с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="30ea9-224">Enforce BitLocker protection for the operating system drive.</span></span></p></li>
<li><p><span data-ttu-id="30ea9-225">Настройте использование закрепления с помощью ПИН-кода доверенного платформенного модуля (TPM) для защиты операционной системы.</span><span class="sxs-lookup"><span data-stu-id="30ea9-225">Configure PIN usage to use a Trusted Platform Module (TPM) PIN for operating system protection.</span></span></p></li>
<li><p><span data-ttu-id="30ea9-226">Настройка расширенных загрузочных закрепления для разрешения знаков, таких как прописные и строчные буквы и цифры.</span><span class="sxs-lookup"><span data-stu-id="30ea9-226">Configure enhanced startup PINs to permit characters such as uppercase and lowercase letters, and numbers.</span></span> <span data-ttu-id="30ea9-227">MBAM не поддерживает использование символов и пробелов для расширенных контактов, несмотря на то что BitLocker поддерживает символы и пробелы.</span><span class="sxs-lookup"><span data-stu-id="30ea9-227">MBAM does not support the use of symbols and spaces for enhanced PINs, even though BitLocker supports symbols and spaces.</span></span></p></li>
</ul>
<p><span data-ttu-id="30ea9-228">Если вы включите этот параметр политики, пользователи обязаны защищать диск операционной системы с помощью BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-228">If you enable this policy setting, users are required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="30ea9-229">Если вы не настраиваете и не можете отключить этот параметр, пользователи не обязаны защищать диск операционной системы с помощью BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-229">If you do not configure or if you disable the setting, users are not required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="30ea9-230">Если этот параметр отключен, агент MBAM расшифровывает том операционной системы, если он зашифрован.</span><span class="sxs-lookup"><span data-stu-id="30ea9-230">If you disable this policy, the MBAM agent decrypts the operating system volume if it is encrypted.</span></span></p>
<p><span data-ttu-id="30ea9-231">Если этот параметр политики включен, пользователям необходимо обеспечить защиту операционной системы с помощью BitLocker, а диск зашифрован.</span><span class="sxs-lookup"><span data-stu-id="30ea9-231">When it is enabled, this policy setting requires users to secure the operating system by using BitLocker protection, and the drive is encrypted.</span></span> <span data-ttu-id="30ea9-232">В соответствии с вашими требованиями к шифрованию вы можете выбрать способ защиты для диска с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="30ea9-232">Based on your encryption requirements, you may select the method of protection for the operating system drive.</span></span></p>
<p><span data-ttu-id="30ea9-233">Для более высоких требований к безопасности используйте доверенный платформенный модуль + PIN-код, разрешите Расширенные ПИН-коды и установите для них минимальную длину в восьми символов.</span><span class="sxs-lookup"><span data-stu-id="30ea9-233">For higher security requirements, use TPM + PIN, allow enhanced PINs, and set the minimum PIN length to eight characters.</span></span></p>
<p><span data-ttu-id="30ea9-234">Если эта политика включена с предохранителем доверенного платформенного модуля +, вы можете отключить следующие политики в <strong> разделе </strong>  /  <strong> </strong>  /  <strong> Параметры режима сна системного управления питанием </strong> :</span><span class="sxs-lookup"><span data-stu-id="30ea9-234">When this policy is enabled with the TPM + PIN protector, you can consider disabling the following policies under <strong>System</strong> / <strong>Power Management</strong> / <strong>Sleep Settings</strong>:</span></span></p>
<ul>
<li><p><span data-ttu-id="30ea9-235">Разрешить режимы ожидания (S1-S3) при простое компьютера (питание от сети)</span><span class="sxs-lookup"><span data-stu-id="30ea9-235">Allow Standby States (S1-S3) When Sleeping (Plugged In)</span></span></p></li>
<li><p><span data-ttu-id="30ea9-236">Разрешить режимы ожидания (S1-S3) при простое компьютера (питание от батареи)</span><span class="sxs-lookup"><span data-stu-id="30ea9-236">Allow Standby States (S1-S3) When Sleeping (On Battery)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30ea9-237">Настройка профиля проверки платформы TPM</span><span class="sxs-lookup"><span data-stu-id="30ea9-237">Configure TPM platform validation profile</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-238">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-238">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-239">Этот параметр политики позволяет настроить, как оборудование безопасности доверенного платформенного модуля для компьютера обеспечивает безопасность ключа шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-239">This policy setting lets you configure how the TPM security hardware on a computer secures the BitLocker encryption key.</span></span> <span data-ttu-id="30ea9-240">Этот параметр политики не применяется, если на компьютере не установлен совместимый доверенный платформенный модуль или для BitLocker уже включена защита TPM.</span><span class="sxs-lookup"><span data-stu-id="30ea9-240">This policy setting does not apply if the computer does not have a compatible TPM or if BitLocker already has TPM protection enabled.</span></span></p>
<p><span data-ttu-id="30ea9-241">Если эта политика не настроена, доверенный платформенный модуль использует профиль проверки платформы по умолчанию или профиль проверки платформы, указанный в сценарии настройки.</span><span class="sxs-lookup"><span data-stu-id="30ea9-241">When this policy is not configured, the TPM uses the default platform validation profile or the platform validation profile specified by the setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30ea9-242">Выбор способа восстановления дисков операционной системы, защищенных с помощью BitLocker</span><span class="sxs-lookup"><span data-stu-id="30ea9-242">Choose how to recover BitLocker-protected operating system drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-243">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-243">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-244">Настройте эту политику, чтобы включить агент восстановления данных BitLocker или сохранить сведения о восстановлении BitLocker в доменных службах Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="30ea9-244">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="30ea9-245">Если эта политика не настроена, агент восстановления данных разрешен, и сведения о восстановлении не заархивированы в доменные службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30ea9-245">When this policy is not configured, the data recovery agent is allowed, and the recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="30ea9-246">Для работы MBAM не требуется резервное копирование данных для восстановления в доменные службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30ea9-246">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="30ea9-247">Определения политик съемных дисков</span><span class="sxs-lookup"><span data-stu-id="30ea9-247">Removable Drive policy definitions</span></span>


<span data-ttu-id="30ea9-248">В этом разделе описаны определения политик съемных дисков для MBAM, которые можно найти на следующем узле GPO: **Конфигурация компьютера**, шаблоны, параметры Windows, архивные \\ **Administrative Templates** \\ **компоненты** \\ **MDOP MBAM (Управление BitLocker)**  \\  **съемный диск**.</span><span class="sxs-lookup"><span data-stu-id="30ea9-248">This section describes the Removable Drive Policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Removable Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30ea9-249">Имя политики</span><span class="sxs-lookup"><span data-stu-id="30ea9-249">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="30ea9-250">Общие сведения и рекомендуемый параметр политики</span><span class="sxs-lookup"><span data-stu-id="30ea9-250">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30ea9-251">Управление использованием BitLocker на съемных дисках</span><span class="sxs-lookup"><span data-stu-id="30ea9-251">Control the use of BitLocker on removable drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-252">Рекомендуемая конфигурация: <strong> включена</span><span class="sxs-lookup"><span data-stu-id="30ea9-252">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="30ea9-253">Этот параметр политики управляет использованием BitLocker на съемных дисках с данными.</span><span class="sxs-lookup"><span data-stu-id="30ea9-253">This policy controls the use of BitLocker on removable data drives.</span></span></p>
<p><span data-ttu-id="30ea9-254">Включите <strong> параметр Разрешить пользователям применять защиту BitLocker для съемных носителей с данными </strong> , чтобы разрешить пользователям запускать мастер настройки BitLocker на съемном носителе данных.</span><span class="sxs-lookup"><span data-stu-id="30ea9-254">Enable the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option, to allow users to run the BitLocker setup wizard on a removable data drive.</span></span></p>
<p><span data-ttu-id="30ea9-255">Включите <strong> параметр Разрешить пользователям приостанавливать и расшифровывать BitLocker на съемных носителях </strong> с данными, чтобы разрешить пользователям удалять шифрование диска BitLocker с диска, а также приостанавливать шифрование при проведении обслуживания.</span><span class="sxs-lookup"><span data-stu-id="30ea9-255">Enable the <strong>Allow users to suspend and decrypt BitLocker on removable data drives</strong> option to allow users to remove BitLocker drive encryption from the drive or to suspend the encryption while maintenance is performed.</span></span></p>
<p><span data-ttu-id="30ea9-256">Если этот параметр включен, а флажок <strong> Разрешить пользователям применять защиту BitLocker для съемных дисков с данными </strong> установлен, клиент MBAM сохранит данные для восстановления на съемных носителях на сервере восстановления ключей MBAM, и это позволит пользователям восстановить диск после потери пароля.</span><span class="sxs-lookup"><span data-stu-id="30ea9-256">When this policy is enabled and the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option is selected, the MBAM Client saves the recovery information about removable drives to the MBAM key recovery server, and it allows users to recover the drive if the password is lost.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30ea9-257">Отказ от разрешения на доступ для записи на съемные диски, не защищенные BitLocker</span><span class="sxs-lookup"><span data-stu-id="30ea9-257">Deny the “write” permissions to removable drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-258">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-258">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-259">Включите эту политику, чтобы разрешить доступ только для записи для дисков, защищенных с помощью BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-259">Enable this policy to allow write-only permissions to BitLocker protected drives.</span></span></p>
<p><span data-ttu-id="30ea9-260">Если эта политика включена, все съемные диски с данными на компьютере должны быть зашифрованы, пока разрешены разрешения на запись.</span><span class="sxs-lookup"><span data-stu-id="30ea9-260">When this policy is enabled, all removable data drives on the computer require encryption before write permissions are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30ea9-261">Предоставление доступа к съемным дискам, защищенным с помощью BitLocker, из более ранних версий Windows</span><span class="sxs-lookup"><span data-stu-id="30ea9-261">Allow access to BitLocker-protected removable drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-262">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-262">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-263">Включите эту политику, чтобы разблокировать и просмотреть съемные диски, отформатированные с помощью файловой системы FAT, на компьютерах под управлением Windows Server 2008, Windows Vista, Windows XP с пакетом обновления 3 (SP3) или Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="30ea9-263">Enable this policy to unlock and view the fixed drives that are formatted with the (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="30ea9-264">Эти операционные системы имеют разрешения на доступ только для чтения к дискам, защищенным с помощью BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30ea9-264">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="30ea9-265">При отключении политики съемные диски, отформатированные с помощью файловой системы FAT, не разблокируются, и их содержимое невозможно будет просматривать на компьютерах под управлением Windows Server 2008, Windows Vista, Windows XP с пакетом обновления 3 (SP3) или Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="30ea9-265">When the policy is disabled, removable drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30ea9-266">Настройка использования пароля для съемных носителей с данными</span><span class="sxs-lookup"><span data-stu-id="30ea9-266">Configure the use of password for removable data drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-267">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-267">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-268">Включите эту политику, чтобы настроить защиту паролем для съемных носителей с данными.</span><span class="sxs-lookup"><span data-stu-id="30ea9-268">Enable this policy to configure password protection on removable data drives.</span></span></p>
<p><span data-ttu-id="30ea9-269">Если эта политика не настроена, пароли будут поддерживаться с параметрами по умолчанию, которые не включают требования к сложности паролей и требуют только восьми символов.</span><span class="sxs-lookup"><span data-stu-id="30ea9-269">When this policy is not configured, passwords are supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="30ea9-270">Чтобы повысить уровень безопасности, включите эту политику и установите флажок <strong> требовать пароль для съемных носителей с данными </strong> , установите флажок <strong> требовать сложность пароля </strong> и задайте предпочтительную <strong> минимальную длину пароля </strong> .</span><span class="sxs-lookup"><span data-stu-id="30ea9-270">For increased security, you can enable this policy and select <strong>Require password for removable data drive</strong>, select <strong>Require password complexity</strong>, and then set the preferred <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30ea9-271">Выбор способа восстановления съемных дисков, защищенных с помощью BitLocker</span><span class="sxs-lookup"><span data-stu-id="30ea9-271">Choose how BitLocker-protected removable drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="30ea9-272">Предлагаемая конфигурация: <strong> не настроена</span><span class="sxs-lookup"><span data-stu-id="30ea9-272">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="30ea9-273">Вы можете настроить эту политику, чтобы включить агент восстановления данных BitLocker или сохранить сведения о восстановлении BitLocker в доменных службах Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="30ea9-273">You can configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="30ea9-274">Если для политики задано значение <strong> не задано </strong> , агент восстановления данных разрешен, а сведения о восстановлении не заархивированы в доменные службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30ea9-274">When the policy is set to <strong>Not Configured</strong>, the data recovery agent is allowed and recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="30ea9-275">Для работы MBAM не требуется резервное копирование данных для восстановления в доменные службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30ea9-275">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="30ea9-276">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="30ea9-276">Related topics</span></span>


[<span data-ttu-id="30ea9-277">Подготовка среды для развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="30ea9-277">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)









