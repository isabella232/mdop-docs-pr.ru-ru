---
title: Создание и изменение файла SMS \ _def. mof
description: Создание и изменение файла SMS \ _def. mof
author: dansimp
ms.assetid: 0bc5e7d8-9747-4da6-a1b3-38d8f27ba121
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 272f597974e96efa0c742fecfe9488a4899fc695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823199"
---
# <span data-ttu-id="1590c-103">Создание и изменение файла SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="1590c-103">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="1590c-104">Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker с помощью отчетов Configuration Manager MBAM, необходимо создать или изменить файл SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="1590c-104">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span>

<span data-ttu-id="1590c-105">Если вы используете SystemCenter2012 ConfigurationManager, необходимо создать файл.</span><span class="sxs-lookup"><span data-stu-id="1590c-105">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="1590c-106">Создайте файл на сайте верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="1590c-106">Create the file on the top-tier site.</span></span> <span data-ttu-id="1590c-107">Изменения будут реплицированы на другие сайты в вашей инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="1590c-107">The changes will be replicated to the other sites in your infrastructure.</span></span>

<span data-ttu-id="1590c-108">В Configuration Manager 2007 файл уже существует, поэтому его нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="1590c-108">In Configuration Manager 2007, the file already exists, so you only have to edit it.</span></span> **<span data-ttu-id="1590c-109">Не перезаписать существующий файл.</span><span class="sxs-lookup"><span data-stu-id="1590c-109">Do not overwrite the existing file.</span></span>**

<span data-ttu-id="1590c-110">В следующих разделах выполните инструкции, соответствующие версии Configuration Manager, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="1590c-110">In the following sections, complete the instructions that correspond to the version of Configuration Manager that you are using.</span></span>

**<span data-ttu-id="1590c-111">Создание файла SMS \ _def. mof для SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="1590c-111">To create the Sms\_def.mof file for SystemCenter2012 ConfigurationManager</span></span>**

1.  <span data-ttu-id="1590c-112">На сервере Configuration Manager перейдите в папку, в которой нужно создать файл SMS \ _def. mof, например, Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="1590c-112">On the Configuration Manager Server, browse to the location where you have to create the Sms\_def.mof file, for example, the Desktop.</span></span>

2.  <span data-ttu-id="1590c-113">Создайте текстовый файл с именем **SMS \ _def. mof** и скопируйте приведенный ниже код, чтобы заполнить файл, используя следующие классы Sms \ _def. mof MBAM:</span><span class="sxs-lookup"><span data-stu-id="1590c-113">Create a text file called **Sms\_def.mof** and copy the following code to populate the file with the following Sms\_def.mof MBAM classes:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  <span data-ttu-id="1590c-114">Импортируйте файл **SMS \ _def. mof** , выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1590c-114">Import the **Sms\_def.mof** file by doing the following:</span></span>

    1.  <span data-ttu-id="1590c-115">Откройте **консоль SystemCenter2012 ConfigurationManager** и перейдите на вкладку **Администрирование** .</span><span class="sxs-lookup"><span data-stu-id="1590c-115">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="1590c-116">На вкладке **Администрирование** выберите пункт **Параметры клиента**.</span><span class="sxs-lookup"><span data-stu-id="1590c-116">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="1590c-117">Щелкните правой кнопкой мыши **Параметры клиента по умолчанию**, а затем выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="1590c-117">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="1590c-118">В окне **параметры по умолчанию** выберите пункт **Инвентаризация оборудования**.</span><span class="sxs-lookup"><span data-stu-id="1590c-118">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="1590c-119">Нажмите кнопку **Set Classes (выбрать классы**), а затем — **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="1590c-119">Click **Set Classes**, and then click **Import**.</span></span>

    6.  <span data-ttu-id="1590c-120">В открывшемся браузере выберите свой **MOF** -файл и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="1590c-120">In the browser that opens, select your **.mof** file, and then click **Open**.</span></span> <span data-ttu-id="1590c-121">Откроется окно **Импорт сводки** .</span><span class="sxs-lookup"><span data-stu-id="1590c-121">The **Import Summary** window opens.</span></span>

    7.  <span data-ttu-id="1590c-122">В окне " **Сводка импорта** " убедитесь, что выбран параметр "импортировать классы инвентаризации оборудования и параметры класса", а затем нажмите кнопку " **Импорт**".</span><span class="sxs-lookup"><span data-stu-id="1590c-122">In the **Import Summary** window, ensure that the option to import both hardware inventory classes and class settings is selected, and then click **Import**.</span></span>

    8.  <span data-ttu-id="1590c-123">В окне **классы инвентаризации оборудования** и в окне **параметры по умолчанию** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1590c-123">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

4.  <span data-ttu-id="1590c-124">Включите класс **Win32 \ _Tpm** , как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="1590c-124">Enable the **Win32\_Tpm** class as follows:</span></span>

    1.  <span data-ttu-id="1590c-125">Откройте **консоль SystemCenter2012 ConfigurationManager** и перейдите на вкладку **Администрирование** .</span><span class="sxs-lookup"><span data-stu-id="1590c-125">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="1590c-126">На вкладке **Администрирование** выберите пункт **Параметры клиента**.</span><span class="sxs-lookup"><span data-stu-id="1590c-126">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="1590c-127">Щелкните правой кнопкой мыши **Параметры клиента по умолчанию**, а затем выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="1590c-127">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="1590c-128">В окне **параметры по умолчанию** выберите пункт **Инвентаризация оборудования**.</span><span class="sxs-lookup"><span data-stu-id="1590c-128">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="1590c-129">Нажмите кнопку **Set Classes (классы**).</span><span class="sxs-lookup"><span data-stu-id="1590c-129">Click **Set Classes**.</span></span>

    6.  <span data-ttu-id="1590c-130">В главном окне прокрутите вниз и выберите класс **TPM (Win32 \ _Tpm)** .</span><span class="sxs-lookup"><span data-stu-id="1590c-130">In the main window, scroll down, and then select the **TPM (Win32\_Tpm)** class.</span></span>

    7.  <span data-ttu-id="1590c-131">В разделе **TPM**убедитесь, что выбрано свойство **SpecVersion** .</span><span class="sxs-lookup"><span data-stu-id="1590c-131">Under **TPM**, ensure that the **SpecVersion** property is selected.</span></span>

    8.  <span data-ttu-id="1590c-132">В окне **классы инвентаризации оборудования** и в окне **параметры по умолчанию** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1590c-132">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

**<span data-ttu-id="1590c-133">Изменение файла SMS \ _def. mof для Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="1590c-133">To edit the sms\_def.mof file for Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="1590c-134">На сервере Configuration Manager выберите расположение файла **SMS \ _def. mof** :</span><span class="sxs-lookup"><span data-stu-id="1590c-134">On the Configuration Manager Server, browse to the location of the **sms\_def.mof** file:</span></span>

    <span data-ttu-id="1590c-135">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="1590c-135">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="1590c-136">В процессе установки по умолчанию используется папка% systemdrive% \\Program Files (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="1590c-136">On a default installation, the installation location is %systemdrive% \\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="1590c-137">Скопируйте приведенный ниже код и добавьте его в файл **SMS \ _def. mof** , чтобы добавить в файл следующие необходимые классы MBAM:</span><span class="sxs-lookup"><span data-stu-id="1590c-137">Copy the following code, and then append it to **Sms\_def.mof** file to add the following required MBAM classes to the file:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=32|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=64|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy_64: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  <span data-ttu-id="1590c-138">Измените класс **Win32 \ _Tpm** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1590c-138">Modify the **Win32\_Tpm** class as follows:</span></span>

    -   <span data-ttu-id="1590c-139">В атрибутах класса настройте **SMS \ _REPORT** в **значение true** .</span><span class="sxs-lookup"><span data-stu-id="1590c-139">Set **SMS\_REPORT** to **TRUE** in the class attributes.</span></span>

    -   <span data-ttu-id="1590c-140">Задайте для свойства **SMS \ _REPORT** **значение true** в атрибуте свойств **SpecVersion** .</span><span class="sxs-lookup"><span data-stu-id="1590c-140">Set **SMS\_REPORT** to **TRUE** in the **SpecVersion** property attribute.</span></span>

    <span data-ttu-id="1590c-141">**У вас есть предложение MBAM**?</span><span class="sxs-lookup"><span data-stu-id="1590c-141">**Got a suggestion for MBAM**?</span></span> <span data-ttu-id="1590c-142">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="1590c-142">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> <span data-ttu-id="1590c-143">**У тебя возникли неполадки с MBAM**?</span><span class="sxs-lookup"><span data-stu-id="1590c-143">**Got a MBAM issue**?</span></span> <span data-ttu-id="1590c-144">Используйте [Форум TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1590c-144">Use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="1590c-145">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1590c-145">Related topics</span></span>


[<span data-ttu-id="1590c-146">Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="1590c-146">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)

[<span data-ttu-id="1590c-147">Изменение файла Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="1590c-147">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

[<span data-ttu-id="1590c-148">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="1590c-148">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

 

 
## <span data-ttu-id="1590c-149">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="1590c-149">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="1590c-150">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="1590c-150">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="1590c-151">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1590c-151">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




