---
title: Создание и изменение файла SMS \ _def. mof
description: Создание и изменение файла SMS \ _def. mof
author: dansimp
ms.assetid: d1747e43-484e-4031-a63b-6342fe588aa2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/04/2017
ms.openlocfilehash: 15f1d1a1c19cb9b19b7d83534e035d5410720ce9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823512"
---
# <span data-ttu-id="31483-103">Создание и изменение файла SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="31483-103">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="31483-104">Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker с помощью отчетов Configuration Manager MBAM, необходимо создать или изменить файл SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="31483-104">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span>

<span data-ttu-id="31483-105">Если вы используете SystemCenter2012 ConfigurationManager, необходимо создать файл.</span><span class="sxs-lookup"><span data-stu-id="31483-105">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span>

<span data-ttu-id="31483-106">В Configuration Manager 2007 файл уже существует, поэтому его нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="31483-106">In Configuration Manager 2007, the file already exists, so you only have to edit it.</span></span> <span data-ttu-id="31483-107">**Не перезаписать существующий файл**.</span><span class="sxs-lookup"><span data-stu-id="31483-107">**Do not overwrite the existing file**.</span></span>

<span data-ttu-id="31483-108">В следующих разделах выполните инструкции, соответствующие версии Configuration Manager, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="31483-108">In the following sections, complete the instructions that correspond to the version of Configuration Manager that you are using.</span></span>

**<span data-ttu-id="31483-109">Создание файла SMS \ _def. mof для SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="31483-109">To create the Sms\_def.mof file for SystemCenter2012 ConfigurationManager</span></span>**

1.  <span data-ttu-id="31483-110">На сервере Configuration Manager перейдите в папку, в которой нужно создать файл SMS \ _def. mof, например, Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="31483-110">On the Configuration Manager Server, browse to the location where you have to create the Sms\_def.mof file, for example, the Desktop.</span></span>

2.  <span data-ttu-id="31483-111">Создайте текстовый файл с именем **SMS \ _def. mof** и скопируйте приведенный ниже код, чтобы заполнить файл, используя следующие классы Sms \ _def. mof MBAM:</span><span class="sxs-lookup"><span data-stu-id="31483-111">Create a text file called **Sms\_def.mof** and copy the following code to populate the file with the following Sms\_def.mof MBAM classes:</span></span>

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

        //MBAM agent fields
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

3.  <span data-ttu-id="31483-112">Импортируйте файл **SMS \ _def. mof** , выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="31483-112">Import the **Sms\_def.mof** file by doing the following:</span></span>

    1.  <span data-ttu-id="31483-113">Откройте **консоль SystemCenter2012 ConfigurationManager** и перейдите на вкладку **Администрирование** .</span><span class="sxs-lookup"><span data-stu-id="31483-113">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="31483-114">На вкладке **Администрирование** выберите пункт **Параметры клиента**.</span><span class="sxs-lookup"><span data-stu-id="31483-114">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="31483-115">Щелкните правой кнопкой мыши **Параметры клиента по умолчанию**, а затем выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="31483-115">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="31483-116">В окне **параметры по умолчанию** выберите пункт **Инвентаризация оборудования**.</span><span class="sxs-lookup"><span data-stu-id="31483-116">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="31483-117">Нажмите кнопку **Set Classes (выбрать классы**), а затем — **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="31483-117">Click **Set Classes**, and then click **Import**.</span></span>

    6.  <span data-ttu-id="31483-118">В открывшемся браузере выберите свой **MOF** -файл и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="31483-118">In the browser that opens, select your **.mof** file, and then click **Open**.</span></span> <span data-ttu-id="31483-119">Откроется окно **Импорт сводки** .</span><span class="sxs-lookup"><span data-stu-id="31483-119">The **Import Summary** window opens.</span></span>

    7.  <span data-ttu-id="31483-120">В окне " **Сводка импорта** " убедитесь, что выбран параметр "импортировать классы инвентаризации оборудования и параметры класса", а затем нажмите кнопку " **Импорт**".</span><span class="sxs-lookup"><span data-stu-id="31483-120">In the **Import Summary** window, ensure that the option to import both hardware inventory classes and class settings is selected, and then click **Import**.</span></span>

    8.  <span data-ttu-id="31483-121">В окне **классы инвентаризации оборудования** и в окне **параметры по умолчанию** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="31483-121">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

4.  <span data-ttu-id="31483-122">Включите класс **Win32 \ _Tpm** , как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="31483-122">Enable the **Win32\_Tpm** class as follows:</span></span>

    1.  <span data-ttu-id="31483-123">Откройте **консоль SystemCenter2012 ConfigurationManager** и перейдите на вкладку **Администрирование** .</span><span class="sxs-lookup"><span data-stu-id="31483-123">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="31483-124">На вкладке **Администрирование** выберите пункт **Параметры клиента**.</span><span class="sxs-lookup"><span data-stu-id="31483-124">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="31483-125">Щелкните правой кнопкой мыши **Параметры клиента по умолчанию**, а затем выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="31483-125">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="31483-126">В окне **параметры по умолчанию** выберите пункт **Инвентаризация оборудования**.</span><span class="sxs-lookup"><span data-stu-id="31483-126">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="31483-127">Нажмите кнопку **Set Classes (классы**).</span><span class="sxs-lookup"><span data-stu-id="31483-127">Click **Set Classes**.</span></span>

    6.  <span data-ttu-id="31483-128">В главном окне прокрутите вниз и выберите класс **TPM (Win32 \ _Tpm)** .</span><span class="sxs-lookup"><span data-stu-id="31483-128">In the main window, scroll down, and then select the **TPM (Win32\_Tpm)** class.</span></span>

    7.  <span data-ttu-id="31483-129">В разделе **TPM**убедитесь, что выбрано свойство **SpecVersion** .</span><span class="sxs-lookup"><span data-stu-id="31483-129">Under **TPM**, ensure that the **SpecVersion** property is selected.</span></span>

    8.  <span data-ttu-id="31483-130">В окне **классы инвентаризации оборудования** и в окне **параметры по умолчанию** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="31483-130">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

**<span data-ttu-id="31483-131">Изменение файла SMS \ _def. mof для Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="31483-131">To edit the sms\_def.mof file for Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="31483-132">На сервере Configuration Manager выберите расположение файла **SMS \ _def. mof** :</span><span class="sxs-lookup"><span data-stu-id="31483-132">On the Configuration Manager Server, browse to the location of the **sms\_def.mof** file:</span></span>

    <span data-ttu-id="31483-133">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="31483-133">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="31483-134">В процессе установки по умолчанию используется папка% systemdrive% \\Program Files (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="31483-134">On a default installation, the installation location is %systemdrive% \\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="31483-135">Скопируйте приведенный ниже код и добавьте его в файл **SMS \ _def. mof** , чтобы добавить в файл следующие необходимые классы MBAM:</span><span class="sxs-lookup"><span data-stu-id="31483-135">Copy the following code, and then append it to **Sms\_def.mof** file to add the following required MBAM classes to the file:</span></span>

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

3.  <span data-ttu-id="31483-136">Измените класс **Win32 \ _Tpm** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="31483-136">Modify the **Win32\_Tpm** class as follows:</span></span>

    -   <span data-ttu-id="31483-137">В атрибутах класса настройте **SMS \ _REPORT** в **значение true** .</span><span class="sxs-lookup"><span data-stu-id="31483-137">Set **SMS\_REPORT** to **TRUE** in the class attributes.</span></span>

    -   <span data-ttu-id="31483-138">Задайте для свойства **SMS \ _REPORT** **значение true** в атрибуте свойств **SpecVersion** .</span><span class="sxs-lookup"><span data-stu-id="31483-138">Set **SMS\_REPORT** to **TRUE** in the **SpecVersion** property attribute.</span></span>

## <span data-ttu-id="31483-139">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="31483-139">Related topics</span></span>


[<span data-ttu-id="31483-140">Порядок создания или изменения MOF-файлов</span><span class="sxs-lookup"><span data-stu-id="31483-140">How to Create or Edit the mof Files</span></span>](how-to-create-or-edit-the-mof-files.md)

[<span data-ttu-id="31483-141">Развертывание MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="31483-141">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





