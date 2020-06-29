---
title: Настройка дополнительных параметров с помощью Windows PowerShell
description: Настройка дополнительных параметров с помощью Windows PowerShell
author: dansimp
ms.assetid: 437a31cc-2a11-456f-b448-b0b869fb53f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a3ece3f76f6e982913aad2b25cfe0084542f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827392"
---
# <span data-ttu-id="dcda3-103">Настройка дополнительных параметров с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dcda3-103">Configuring Advanced Settings by Using Windows PowerShell</span></span>


<span data-ttu-id="dcda3-104">Созданный пакет рабочей области для MED-V включает в себя файл сценария Windows PowerShell (PS1), который можно изменить перед тестированием и развертыванием пакета для рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="dcda3-104">The MED-V workspace package that you create includes a Windows PowerShell script (.ps1) file that you can edit before you test and deploy your MED-V workspace package.</span></span> <span data-ttu-id="dcda3-105">В этом разделе приведены сведения и рекомендации по управлению параметрами конфигурации для MED-V с помощью Windows PowerShell перед развертыванием рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="dcda3-105">This section provides information and guidance to help you manage MED-V configuration settings by using Windows PowerShell before you deploy the MED-V workspaces.</span></span>

## <span data-ttu-id="dcda3-106">Использование командлетов Windows PowerShell в MED-V</span><span class="sxs-lookup"><span data-stu-id="dcda3-106">Using Windows PowerShell Cmdlets in MED-V</span></span>


<span data-ttu-id="dcda3-107">Следующие командлеты Windows PowerShell доступны в Microsoft Enterprise Virtualization (MED-V) 2,0:</span><span class="sxs-lookup"><span data-stu-id="dcda3-107">The following Windows PowerShell cmdlets are available in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

**<span data-ttu-id="dcda3-108">New-MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcda3-108">New-MedvConfiguration</span></span>**

**<span data-ttu-id="dcda3-109">Export-MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcda3-109">Export-MedvConfiguration</span></span>**

**<span data-ttu-id="dcda3-110">New-MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="dcda3-110">New-MedvWorkspace</span></span>**

**<span data-ttu-id="dcda3-111">Export-MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="dcda3-111">Export-MedvWorkspace</span></span>**

<span data-ttu-id="dcda3-112">Чтобы получить доступ к командлетам Windows PowerShell для MED-V, откройте Windows PowerShell и введите следующую команду для импорта модулей MED-V.</span><span class="sxs-lookup"><span data-stu-id="dcda3-112">To access Windows PowerShell cmdlets for MED-V, open Windows PowerShell and type the following command to import the MED-V modules.</span></span>

``` syntax
Import-Module microsoft.medv
```

<span data-ttu-id="dcda3-113">После импорта модулей вы можете получить доступ к встроенной справке по командлетам с помощью стандартных команд справки Windows PowerShell, **Man** или **Get-Help**.</span><span class="sxs-lookup"><span data-stu-id="dcda3-113">After the modules are imported, you can access inline help for the cmdlets by using the standard Windows PowerShell Help commands, **man** or **get-help**.</span></span> <span data-ttu-id="dcda3-114">Например, для доступа к описанию командлета **New-MedvConfiguration** , в том числе полного списка доступных параметров, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="dcda3-114">For example, to access a description of the **New-MedvConfiguration** cmdlet including a complete list of available parameters, type the following command.</span></span>

``` syntax
get-help New-MedvConfiguration
```

<span data-ttu-id="dcda3-115">Вы также можете просмотреть справку по определенным параметрам.</span><span class="sxs-lookup"><span data-stu-id="dcda3-115">You can also view help for specific parameters.</span></span> <span data-ttu-id="dcda3-116">Например, чтобы просмотреть справку по параметру VmMemory, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="dcda3-116">For example, to view help for the parameter VmMemory, type the following:</span></span>

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

<span data-ttu-id="dcda3-117">Чтобы просмотреть список всех параметров конфигурации для MED-V и их значений по умолчанию, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="dcda3-117">To view a list of all MED-V configuration settings and their defaults, type the following command.</span></span>

``` syntax
New-MedvConfiguration -ForceDefaults
```

<span data-ttu-id="dcda3-118">Чтобы просмотреть список всех параметров конфигурации для MED-V и их текущих значений, введите указанную ниже команду.</span><span class="sxs-lookup"><span data-stu-id="dcda3-118">To view a list of all MED-V configuration settings and their current values, type the following command.</span></span>

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## <span data-ttu-id="dcda3-119">Создание рабочей области для MED-V с пользовательскими параметрами</span><span class="sxs-lookup"><span data-stu-id="dcda3-119">Creating a MED-V Workspace with Custom Settings</span></span>


<span data-ttu-id="dcda3-120">После успешного создания пакета рабочей области MED-V с помощью диспетчера рабочих областей MED-V в папке, указанной для сохранения файлов упаковщика, создается сценарий Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dcda3-120">After you successfully create a MED-V workspace package by using the MED-V Workspace Packager, a Windows PowerShell script is generated in the folder you specified for saving your packager files.</span></span> <span data-ttu-id="dcda3-121">Содержимое этого сценария показывает некоторые доступные параметры конфигурации для MED-V, которые можно изменять.</span><span class="sxs-lookup"><span data-stu-id="dcda3-121">The contents of this script show some of the available MED-V configuration settings that you can edit.</span></span>

<span data-ttu-id="dcda3-122">Следуя этим инструкциям, вы можете настроить сценарий, а затем запустить его в Windows PowerShell, чтобы создать рабочую область MED-V с новыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="dcda3-122">Following these steps, you can customize the script and then run it in Windows PowerShell to create a MED-V workspace with the new settings.</span></span>

<span data-ttu-id="dcda3-123">**Важно!**  Запустите Windows PowerShell с учетными данными администратора и убедитесь, что политика выполнения Windows PowerShell разрешает выполнение сценариев.</span><span class="sxs-lookup"><span data-stu-id="dcda3-123">**Important** Run Windows PowerShell with administrative credentials, and ensure that the Windows PowerShell execution policy allows the running of scripts.</span></span>

1.  <span data-ttu-id="dcda3-124">Измените сценарий Windows PowerShell, созданный диспетчером рабочих областей MED-V, или создайте новый сценарий с нужными параметрами конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dcda3-124">Edit the Windows PowerShell script that was generated by the MED-V Workspace Packager, or author a new script with the configuration settings that you want.</span></span>

2.  <span data-ttu-id="dcda3-125">Запустите Windows PowerShell с учетными данными администратора и в командной строке введите указанную ниже команду.</span><span class="sxs-lookup"><span data-stu-id="dcda3-125">Run Windows PowerShell with administrative credentials and at the command prompt, type the following command.</span></span>

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    <span data-ttu-id="dcda3-126">Эта команда запускает сценарий Windows PowerShell и запускает командлет **New-MedvWorkspace** для создания нового пакета рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="dcda3-126">This command runs the Windows PowerShell script and runs the **New-MedvWorkspace** cmdlet to generate a new MED-V workspace package.</span></span> <span data-ttu-id="dcda3-127">Новые файлы упаковщика сохраняются в папке, которая была первоначально указана для хранения файлов диспетчера рабочих областей для MED-V.</span><span class="sxs-lookup"><span data-stu-id="dcda3-127">The new packager files are saved in the folder that you originally specified for storing your MED-V Workspace Packager files.</span></span> <span data-ttu-id="dcda3-128">Дополнительные сведения об этом командлете можно найти в справке Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dcda3-128">For additional help about this cmdlet, see the Windows PowerShell Help.</span></span>

 

## <span data-ttu-id="dcda3-129">Экспорт конфигурации MED-V в файл реестра</span><span class="sxs-lookup"><span data-stu-id="dcda3-129">Exporting a MED-V Configuration to a Registry File</span></span>


<span data-ttu-id="dcda3-130">После установки рабочей области для MED-V вы можете обновить параметры конфигурации MED-V.</span><span class="sxs-lookup"><span data-stu-id="dcda3-130">You can update MED-V configuration settings after the MED-V workspace is installed.</span></span> <span data-ttu-id="dcda3-131">С помощью командлета **New-MedvConfiguration** можно указать параметры, которые нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="dcda3-131">Use the **New-MedvConfiguration** cmdlet to specify the parameters that you want to change.</span></span> <span data-ttu-id="dcda3-132">Например, чтобы создать файл реестра, который изменяет параметр памяти виртуальной машины, введите указанные ниже команды.</span><span class="sxs-lookup"><span data-stu-id="dcda3-132">For example, to create a registry file that changes the virtual machine memory setting, type the following commands.</span></span>

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

<span data-ttu-id="dcda3-133">Чтобы применить новые параметры конфигурации, вы можете импортировать полученный файл реестра из главного компьютера в рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="dcda3-133">You can import the resultant registry file from the host computer to a MED-V workspace to apply the new configuration settings.</span></span>

## <span data-ttu-id="dcda3-134">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="dcda3-134">Related topics</span></span>


[<span data-ttu-id="dcda3-135">Управление параметрами конфигурации рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="dcda3-135">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="dcda3-136">Тестирование и развертывание пакета рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="dcda3-136">Test And Deploy the MED-V Workspace Package</span></span>](test-and-deploy-the-med-v-workspace-package.md)

 

 





