---
title: Развертывание клиента MBAM в рамках развертывания Windows
description: Развертывание клиента MBAM в рамках развертывания Windows
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824912"
---
# <span data-ttu-id="4078e-103">Развертывание клиента MBAM в рамках развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="4078e-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="4078e-104">Клиент администрирования и мониторинга Microsoft BitLocker (MBAM) позволяет администраторам принудительно применять и отслеживать шифрование диска BitLocker на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="4078e-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="4078e-105">Клиент BitLocker можно интегрировать в организацию, включив Управление BitLocker и шифрование на клиентских компьютерах во время создания образа компьютера и процесса развертывания Windows.</span><span class="sxs-lookup"><span data-stu-id="4078e-105">The BitLocker Client can be integrated into an organization by enabling BitLocker management and encryption on client computers during the computer imaging and Windows deployment process.</span></span>

**<span data-ttu-id="4078e-106">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4078e-106">Note</span></span>**  
<span data-ttu-id="4078e-107">Сведения о требованиях к системе клиента MBAM можно найти в разделе [Поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="4078e-107">To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>



<span data-ttu-id="4078e-108">Шифрование клиентских компьютеров с помощью BitLocker во время начальной стадии обработки образа в развертывании Windows может снизить затраты на администрирование MBAM реализации.</span><span class="sxs-lookup"><span data-stu-id="4078e-108">Encryption of client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead for MBAM implementation.</span></span> <span data-ttu-id="4078e-109">Этот подход также гарантирует, что все развернутые компьютеры уже работают с BitLocker и настроены правильно.</span><span class="sxs-lookup"><span data-stu-id="4078e-109">This approach also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="4078e-110">Warning</span><span class="sxs-lookup"><span data-stu-id="4078e-110">Warning</span></span>**  
<span data-ttu-id="4078e-111">В этой статье описано, как изменить реестр Windows с помощью редактора реестра.</span><span class="sxs-lookup"><span data-stu-id="4078e-111">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="4078e-112">Если изменить реестр Windows некорректно, это может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows.</span><span class="sxs-lookup"><span data-stu-id="4078e-112">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="4078e-113">Перед изменением реестра необходимо создать резервную копию файлов реестра (System. dat и User. dat).</span><span class="sxs-lookup"><span data-stu-id="4078e-113">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="4078e-114">Корпорация Майкрософт не несет ответственности за то, что проблемы, которые могут возникнуть при изменении реестра, могут быть устранены.</span><span class="sxs-lookup"><span data-stu-id="4078e-114">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="4078e-115">Изменение реестра на свой страх и риск.</span><span class="sxs-lookup"><span data-stu-id="4078e-115">Change the registry at your own risk.</span></span>



**<span data-ttu-id="4078e-116">Шифрование компьютера в рамках развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="4078e-116">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="4078e-117">Если в вашей организации планируется использовать предохранитель доверенного платформенного модуля (TPM) или параметры предохранителя TPM + PIN-кода в BitLocker, необходимо активировать микросхему TPM перед начальным развертыванием MBAM.</span><span class="sxs-lookup"><span data-stu-id="4078e-117">If your organization plans to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="4078e-118">После активации микросхемы TPM вы не сможете перезагружаться позже в процессе, и вы убедитесь, что микросхемы TPM правильно настроены в соответствии с требованиями вашей организации.</span><span class="sxs-lookup"><span data-stu-id="4078e-118">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="4078e-119">Микросхемы TPM необходимо активировать вручную в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="4078e-119">You must activate the TPM chip manually in the computer's BIOS.</span></span> <span data-ttu-id="4078e-120">Дополнительные сведения о настройке микросхемы TPM можно найти в документации изготовителя.</span><span class="sxs-lookup"><span data-stu-id="4078e-120">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>

2.  <span data-ttu-id="4078e-121">Установите агент клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="4078e-121">Install the MBAM client agent.</span></span>

3.  <span data-ttu-id="4078e-122">Мы рекомендуем присоединить компьютер к домену...</span><span class="sxs-lookup"><span data-stu-id="4078e-122">We recommend that you join the computer to a domain...</span></span>

    -   <span data-ttu-id="4078e-123">Если компьютер не подключен к домену, пароль восстановления не хранится в службе восстановления ключа MBAM.</span><span class="sxs-lookup"><span data-stu-id="4078e-123">If the computer is not joined to a domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="4078e-124">По умолчанию MBAM не поддерживает шифрование, если не удается сохранить ключ восстановления.</span><span class="sxs-lookup"><span data-stu-id="4078e-124">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="4078e-125">Если компьютер запускается в режиме восстановления, прежде чем ключ восстановления будет сохранен на сервере MBAM, необходимо переобразировать компьютер.</span><span class="sxs-lookup"><span data-stu-id="4078e-125">If a computer starts in recovery mode before the recovery key is stored on the MBAM server, the computer has to be reimaged.</span></span> <span data-ttu-id="4078e-126">Метод восстановления недоступен.</span><span class="sxs-lookup"><span data-stu-id="4078e-126">No recovery method is available.</span></span>

4.  <span data-ttu-id="4078e-127">Откройте командную команду от имени администратора, остановите службу MBAM и настройте ее на **ручной** или **по запросу**.</span><span class="sxs-lookup"><span data-stu-id="4078e-127">Open a command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**.</span></span> <span data-ttu-id="4078e-128">Затем выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="4078e-128">Then, run the following commands:</span></span>

    **<span data-ttu-id="4078e-129">NET STOP mbamagent</span><span class="sxs-lookup"><span data-stu-id="4078e-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="4078e-130">SC config mbamagent Start = Demand</span><span class="sxs-lookup"><span data-stu-id="4078e-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="4078e-131">Настройка параметров реестра для агента MBAM, чтобы игнорировать групповую политику и запустить доверенный платформенный модуль для **шифрования только** для этого, запустите **regedit**, а затем импортируйте шаблон раздела реестра из c:\\program Files Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span><span class="sxs-lookup"><span data-stu-id="4078e-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** To do this, run **regedit**, and then import the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="4078e-132">В regedit перейдите на HKLM\\SOFTWARE\\Microsoft\\MBAM и настройте параметры, указанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="4078e-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="4078e-133">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="4078e-133">Registry entry</span></span>

    <span data-ttu-id="4078e-134">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="4078e-134">Configuration settings</span></span>

    <span data-ttu-id="4078e-135">DeploymentTime</span><span class="sxs-lookup"><span data-stu-id="4078e-135">DeploymentTime</span></span>

    <span data-ttu-id="4078e-136">0 = ВЫКЛ.</span><span class="sxs-lookup"><span data-stu-id="4078e-136">0 = OFF</span></span>

    <span data-ttu-id="4078e-137">1 = Использование параметров политики времени развертывания (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4078e-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="4078e-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="4078e-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="4078e-139">0 = не использовать криптоключ ключа (в этом случае следующие два элемента реестра не требуются).</span><span class="sxs-lookup"><span data-stu-id="4078e-139">0 = Do not use key escrow (The next two registry entries are not required in this case.)</span></span>

    <span data-ttu-id="4078e-140">1 = использование депонирования ключа в системе восстановления ключей (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4078e-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="4078e-141">Рекомендуется: компьютер должен поддерживать связь с службой восстановления ключей.</span><span class="sxs-lookup"><span data-stu-id="4078e-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="4078e-142">Убедитесь, что компьютер может взаимодействовать со службой, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="4078e-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="4078e-143">KeyRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="4078e-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="4078e-144">0 = загрузить только ключ восстановления</span><span class="sxs-lookup"><span data-stu-id="4078e-144">0 = Upload Recovery Key Only</span></span>

    <span data-ttu-id="4078e-145">1 = Отправка ключа восстановления и пакета восстановления ключа (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4078e-145">1 = Upload Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="4078e-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="4078e-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="4078e-147">Задайте для этого параметра URL-адрес веб – сервера восстановления ключей.</span><span class="sxs-lookup"><span data-stu-id="4078e-147">Set this value to the URL for the Key Recovery web server.</span></span>

    <span data-ttu-id="4078e-148">Пример: http:// &lt; имя компьютера &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.</span><span class="sxs-lookup"><span data-stu-id="4078e-148">Example: http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. <span data-ttu-id="4078e-149">Агент MBAM перезапускает систему во время развертывания клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="4078e-149">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="4078e-150">Когда вы будете готовы к перезагрузке, выполните в командной строке в качестве администратора следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4078e-150">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="4078e-151">NET start mbamagent</span><span class="sxs-lookup"><span data-stu-id="4078e-151">net start mbamagent</span></span>**

8. <span data-ttu-id="4078e-152">После перезапуска компьютера и BIOS, предложит вам изменить доверенный платформенный модуль, подтвердите изменение.</span><span class="sxs-lookup"><span data-stu-id="4078e-152">When the computers restarts and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="4078e-153">Когда вы будете готовы начать шифрование, перезапустите службу агента MBAM на этапе обработки образа операционной системы клиента Windows.</span><span class="sxs-lookup"><span data-stu-id="4078e-153">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service.</span></span> <span data-ttu-id="4078e-154">Затем, чтобы установить **Автоматический**запуск, откройте командную команду от имени администратора и выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="4078e-154">Then, to set start to **automatic**, open a command prompt as an administrator and run the following commands:</span></span>

   **<span data-ttu-id="4078e-155">SC config mbamagent Start = Auto</span><span class="sxs-lookup"><span data-stu-id="4078e-155">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="4078e-156">NET start mbamagent</span><span class="sxs-lookup"><span data-stu-id="4078e-156">net start mbamagent</span></span>**

10. <span data-ttu-id="4078e-157">Удалите значения из раздела "пропустить".</span><span class="sxs-lookup"><span data-stu-id="4078e-157">Remove the bypass registry values.</span></span> <span data-ttu-id="4078e-158">Для этого запустите regedit, перейдите в раздел реестра HKLM\\SOFTWARE\\Microsoft, щелкните правой кнопкой мыши узел **MBAM** и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="4078e-158">To do this, run regedit, browse to the HKLM\\SOFTWARE\\Microsoft registry entry, right-click the **MBAM** node, and then click **Delete**.</span></span>

## <span data-ttu-id="4078e-159">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4078e-159">Related topics</span></span>


[<span data-ttu-id="4078e-160">Развертывание клиента MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="4078e-160">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)









