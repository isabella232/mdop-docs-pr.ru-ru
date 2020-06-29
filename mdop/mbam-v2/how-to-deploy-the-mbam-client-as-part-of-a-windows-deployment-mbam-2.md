---
title: Развертывание клиента MBAM в рамках развертывания Windows
description: Развертывание клиента MBAM в рамках развертывания Windows
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824622"
---
# <span data-ttu-id="d940f-103">Развертывание клиента MBAM в рамках развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="d940f-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="d940f-104">Клиент администрирования и мониторинга Microsoft BitLocker (MBAM) позволяет администраторам принудительно применять и отслеживать шифрование диска BitLocker на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="d940f-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="d940f-105">Если компьютеры с микросхемой доверенного платформенного модуля (TPM), клиент BitLocker можно интегрировать в организацию, включив Управление BitLocker и шифрование на клиентских компьютерах в рамках процесса создания образа и развертывания Windows.</span><span class="sxs-lookup"><span data-stu-id="d940f-105">If computers that have a Trusted Platform Module (TPM) chip, the BitLocker client can be integrated into an organization by enabling BitLocker management and encryption on client computers as part of the imaging and Windows deployment process.</span></span>

**<span data-ttu-id="d940f-106">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d940f-106">Note</span></span>**  
<span data-ttu-id="d940f-107">Сведения о требованиях к клиентским системам администрирования и мониторинга Microsoft BitLocker можно найти в разделе [Поддерживаемые конфигурации MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d940f-107">To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



<span data-ttu-id="d940f-108">Шифрование клиентских компьютеров с помощью BitLocker во время начальной стадии обработки образа в развертывании Windows может снизить затраты на администрирование, необходимые для реализации MBAM в Организации.</span><span class="sxs-lookup"><span data-stu-id="d940f-108">Encrypting client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead necessary for implementing MBAM in an organization.</span></span> <span data-ttu-id="d940f-109">Кроме того, это гарантирует, что все развернутые компьютеры уже работают с BitLocker и настроены правильно.</span><span class="sxs-lookup"><span data-stu-id="d940f-109">It also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="d940f-110">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d940f-110">Note</span></span>**  
<span data-ttu-id="d940f-111">В этом разделе описана процедура изменения реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="d940f-111">The procedure in this topic describes modifying the Windows registry.</span></span> <span data-ttu-id="d940f-112">Неправильное использование редактора реестра может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows.</span><span class="sxs-lookup"><span data-stu-id="d940f-112">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="d940f-113">Корпорация Майкрософт не гарантирует, что проблемы, возникающие в результате неправильного использования редактора реестра, могут быть устранены.</span><span class="sxs-lookup"><span data-stu-id="d940f-113">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="d940f-114">Ответственность за использование редактора реестра.</span><span class="sxs-lookup"><span data-stu-id="d940f-114">Use Registry Editor at your own risk.</span></span>



**<span data-ttu-id="d940f-115">Шифрование компьютера в рамках развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="d940f-115">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="d940f-116">Если в вашей организации планируется использовать предохранитель доверенного платформенного модуля (TPM) или параметры предохранителя TPM + PIN-кода в BitLocker, необходимо активировать микросхему TPM перед начальным развертыванием MBAM.</span><span class="sxs-lookup"><span data-stu-id="d940f-116">If your organization is planning to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="d940f-117">После активации микросхемы TPM вы не сможете перезагружаться позже в процессе, и вы убедитесь, что микросхемы TPM правильно настроены в соответствии с требованиями вашей организации.</span><span class="sxs-lookup"><span data-stu-id="d940f-117">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="d940f-118">Вы должны активировать микросхему доверенного платформенного модуля вручную в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="d940f-118">You must activate the TPM chip manually in the BIOS of the computer.</span></span>

    **<span data-ttu-id="d940f-119">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d940f-119">Note</span></span>**  
    <span data-ttu-id="d940f-120">Некоторые поставщики предоставляют средства для включения и активации микросхемы TPM в BIOS в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="d940f-120">Some vendors provide tools to turn on and activate the TPM chip in the BIOS from within the operating system.</span></span> <span data-ttu-id="d940f-121">Дополнительные сведения о настройке микросхемы TPM можно найти в документации изготовителя.</span><span class="sxs-lookup"><span data-stu-id="d940f-121">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>



2.  <span data-ttu-id="d940f-122">Установите агент клиента администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d940f-122">Install the Microsoft BitLocker Administration and Monitoring client agent.</span></span>

3.  <span data-ttu-id="d940f-123">Присоединение компьютера к домену (рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="d940f-123">Join the computer to a domain (recommended).</span></span>

    -   <span data-ttu-id="d940f-124">Если компьютер не подключен к домену, пароль восстановления не хранится в службе восстановления ключа MBAM.</span><span class="sxs-lookup"><span data-stu-id="d940f-124">If the computer is not joined to the domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="d940f-125">По умолчанию MBAM не поддерживает шифрование, если не удается сохранить ключ восстановления.</span><span class="sxs-lookup"><span data-stu-id="d940f-125">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="d940f-126">Если компьютер запускается в режиме восстановления, прежде чем ключ восстановления будет сохранен на сервере MBAM, необходимо переобразировать компьютер.</span><span class="sxs-lookup"><span data-stu-id="d940f-126">If a computer starts in recovery mode before the recovery key is stored on the MBAM Server, the computer has to be reimaged.</span></span> <span data-ttu-id="d940f-127">Метод восстановления недоступен.</span><span class="sxs-lookup"><span data-stu-id="d940f-127">No recovery method is available.</span></span>

4.  <span data-ttu-id="d940f-128">Запустите командную строку от имени администратора, остановите службу MBAM и настройте ее **вручную** или **по запросу**, а затем начните с ввода следующих команд:</span><span class="sxs-lookup"><span data-stu-id="d940f-128">Run the command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**, and then start by typing the following commands:</span></span>

    **<span data-ttu-id="d940f-129">NET STOP mbamagent</span><span class="sxs-lookup"><span data-stu-id="d940f-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="d940f-130">SC config mbamagent Start = Demand</span><span class="sxs-lookup"><span data-stu-id="d940f-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="d940f-131">Настройте параметры реестра для агента MBAM, чтобы игнорировать групповую политику и выполнить **шифрование только для операционной системы** , запустив **regedit**, а затем импортируйте шаблон раздела реестра из c:\\program Files Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span><span class="sxs-lookup"><span data-stu-id="d940f-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** by running **Regedit**, and then importing the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="d940f-132">В regedit перейдите на HKLM\\SOFTWARE\\Microsoft\\MBAM и настройте параметры, указанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d940f-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM, and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="d940f-133">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="d940f-133">Registry entry</span></span>

    <span data-ttu-id="d940f-134">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="d940f-134">Configuration settings</span></span>

    <span data-ttu-id="d940f-135">DeploymentTime</span><span class="sxs-lookup"><span data-stu-id="d940f-135">DeploymentTime</span></span>

    <span data-ttu-id="d940f-136">0 = ВЫКЛ.</span><span class="sxs-lookup"><span data-stu-id="d940f-136">0 = OFF</span></span>

    <span data-ttu-id="d940f-137">1 = Использование параметров политики времени развертывания (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d940f-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="d940f-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="d940f-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="d940f-139">0 = не использовать криптоключ ключа (в этом случае следующие два элемента реестра не требуются).</span><span class="sxs-lookup"><span data-stu-id="d940f-139">0 = Do not use key escrow ( the next two registry entries are not required in this case)</span></span>

    <span data-ttu-id="d940f-140">1 = использование депонирования ключа в системе восстановления ключей (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d940f-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="d940f-141">Рекомендуется: компьютер должен поддерживать связь с службой восстановления ключей.</span><span class="sxs-lookup"><span data-stu-id="d940f-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="d940f-142">Убедитесь, что компьютер может взаимодействовать со службой, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="d940f-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="d940f-143">KeyRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="d940f-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="d940f-144">0 = Отправка только ключа восстановления</span><span class="sxs-lookup"><span data-stu-id="d940f-144">0 = Uploads Recovery Key Only</span></span>

    <span data-ttu-id="d940f-145">1 = Отправка ключа восстановления и пакета восстановления ключа (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d940f-145">1 = Uploads Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="d940f-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="d940f-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="d940f-147">Задайте для этого параметра URL-адрес веб – сервера восстановления ключа (например, http:// &lt; имя компьютера &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.).</span><span class="sxs-lookup"><span data-stu-id="d940f-147">Set this value to the URL for the Key Recovery web server, for example, http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. <span data-ttu-id="d940f-148">Агент MBAM перезапускает систему во время развертывания клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="d940f-148">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="d940f-149">Когда вы будете готовы к перезагрузке, выполните в командной строке в качестве администратора следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d940f-149">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="d940f-150">NET start mbamagent</span><span class="sxs-lookup"><span data-stu-id="d940f-150">net start mbamagent</span></span>**

8. <span data-ttu-id="d940f-151">После перезапуска компьютера и BIOS, предложит вам изменить доверенный платформенный модуль, подтвердите изменение.</span><span class="sxs-lookup"><span data-stu-id="d940f-151">When the computers restarts, and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="d940f-152">В процессе обработки образа операционной системы клиента Windows, когда вы будете готовы начать шифрование, перезапустите службу агента MBAM и установите для параметра автоматический запуск команду **автоматически** , выполнив командную строку от имени администратора и введя следующие команды:</span><span class="sxs-lookup"><span data-stu-id="d940f-152">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service, and set start to **automatic** by running a command prompt as an administrator and typing the following commands:</span></span>

   **<span data-ttu-id="d940f-153">SC config mbamagent Start = Auto</span><span class="sxs-lookup"><span data-stu-id="d940f-153">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="d940f-154">NET start mbamagent</span><span class="sxs-lookup"><span data-stu-id="d940f-154">net start mbamagent</span></span>**

10. <span data-ttu-id="d940f-155">Удалите значения из раздела "пропустить", запустив regedit и перейдя к разделу реестра HKLM\\SOFTWARE\\Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d940f-155">Remove the bypass registry values by running Regedit and going to the HKLM\\SOFTWARE\\Microsoft registry entry.</span></span> <span data-ttu-id="d940f-156">Чтобы удалить узел **MBAM** , щелкните узел правой кнопкой мыши и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="d940f-156">To delete the **MBAM** node, right-click the node and click **Delete**.</span></span>

## <span data-ttu-id="d940f-157">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d940f-157">Related topics</span></span>


[<span data-ttu-id="d940f-158">Развертывание клиента MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d940f-158">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)









