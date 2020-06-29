---
title: Преобразование пакета, созданного в предыдущей версии App-V
description: Преобразование пакета, созданного в предыдущей версии App-V
author: dansimp
ms.assetid: b092a5f8-cc5f-4df8-a5a2-0a68fd7bd5b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bd0d5db7cb406a5a7fe67c69ff77461cce2b0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814360"
---
# <span data-ttu-id="dbe2f-103">Преобразование пакета, созданного в предыдущей версии App-V</span><span class="sxs-lookup"><span data-stu-id="dbe2f-103">How to Convert a Package Created in a Previous Version of App-V</span></span>


<span data-ttu-id="dbe2f-104">С помощью служебной программы преобразователя пакетов можно обновлять пакеты виртуальных приложений, созданные в предыдущих версиях приложения App-V.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-104">You can use the package converter utility to upgrade virtual application packages that have been created with previous versions of App-V.</span></span>

**<span data-ttu-id="dbe2f-105">Примечание.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-105">Note</span></span>**  
<span data-ttu-id="dbe2f-106">Если на компьютере установлена архитектура 64-bit, необходимо использовать версию x86 оболочки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-106">If you are running a computer with a 64-bit architecture, you must use the x86 version of PowerShell.</span></span>



<span data-ttu-id="dbe2f-107">Конвертер пакетов может напрямую преобразовывать пакеты, созданные с помощью секвенсора App-V 4,5 или последующих версий.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-107">The package converter can only directly convert packages that were created by using the App-V 4.5 sequencer or a subsequent version.</span></span> <span data-ttu-id="dbe2f-108">Пакеты, созданные с помощью более ранней версии App-V 4,5, должны быть обновлены до формата App-V 4,5 или App-V 4,6 перед преобразованием.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-108">Packages that were created using a version prior to App-V 4.5 must be upgraded to the App-V 4.5 or App-V 4.6 format before conversion.</span></span>

<span data-ttu-id="dbe2f-109">Ниже приведены сведения о том, как преобразовать существующие пакеты виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-109">The following information provides direction for converting existing virtual application packages.</span></span>

**<span data-ttu-id="dbe2f-110">Важно.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-110">Important</span></span>**  
<span data-ttu-id="dbe2f-111">Необходимо настроить преобразователь пакетов, чтобы всегда сохранять файл ингредиентов пакета в безопасном месте и каталоге.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-111">You must configure the package converter to always save the package ingredients file to a secure location and directory.</span></span> <span data-ttu-id="dbe2f-112">Безопасное расположение доступно только администратору.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-112">A secure location is accessible only by an administrator.</span></span> <span data-ttu-id="dbe2f-113">Кроме того, при развертывании пакета необходимо сохранить пакет в безопасном расположении или убедиться в том, что во время преобразования никто из пользователей не может войти в систему.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-113">Additionally, when you deploy the package, you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion process.</span></span>



**<span data-ttu-id="dbe2f-114">Начало работы</span><span class="sxs-lookup"><span data-stu-id="dbe2f-114">Getting started</span></span>**

1.  <span data-ttu-id="dbe2f-115">Установите секвенсор App-V на компьютер в среде.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-115">Install the App-V Sequencer on a computer in your environment.</span></span> <span data-ttu-id="dbe2f-116">Сведения о том, как установить секвенсор, приведены в разделе [Установка секвенсора](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="dbe2f-116">For information about how to install the Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2. <span data-ttu-id="dbe2f-117">Импорт требуемого модуля PowerShell</span><span class="sxs-lookup"><span data-stu-id="dbe2f-117">Import the required Powershell Module</span></span>

```powershell
Import-Module AppVPkgConverter
```

3. <span data-ttu-id="dbe2f-118">Доступны следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="dbe2f-118">The following cmdlets are available:</span></span>

   -   <span data-ttu-id="dbe2f-119">Test-AppvLegacyPackage — этот командлет предназначен для проверки пакетов.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-119">Test-AppvLegacyPackage – This cmdlet is designed to check packages.</span></span> <span data-ttu-id="dbe2f-120">Она будет возвращать сведения о сбоях в пакете, таких как отсутствующие **SFT** — файлы, недопустимые ошибки источника, **OSD** или неправильная версия пакета.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-120">It will return information about any failures with the package such as missing **.sft** files, an invalid source, **.osd** file errors, or invalid package version.</span></span> <span data-ttu-id="dbe2f-121">Этот командлет не будет анализировать **SFT** – файл или выполнять какие – либо проверки глубины.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-121">This cmdlet will not parse the **.sft** file or do any in depth validation.</span></span> <span data-ttu-id="dbe2f-122">Чтобы получить сведения о параметрах и основных функциональных возможностях для этого командлета, используйте PowerShell cmdline: Type `Test-AppvLegacyPackage -?` .</span><span class="sxs-lookup"><span data-stu-id="dbe2f-122">For information about options and basic functionality for this cmdlet, using the PowerShell cmdline, type `Test-AppvLegacyPackage -?`.</span></span>

   -   <span data-ttu-id="dbe2f-123">ConvertFrom-AppvLegacyPackage – чтобы преобразовать существующий пакет, введите `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` .</span><span class="sxs-lookup"><span data-stu-id="dbe2f-123">ConvertFrom-AppvLegacyPackage – To convert an existing package, type `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages`.</span></span> <span data-ttu-id="dbe2f-124">В этой команде — это `c:\contentStore` расположение существующего пакета и `c:\convertedPackages` Каталог вывода, в который будет сохранен конечный файл виртуального приложения App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-124">In this command, `c:\contentStore` represents the location of the existing package and `c:\convertedPackages` is the output directory to which the resulting App-V 5.0 virtual application package file will be saved.</span></span> <span data-ttu-id="dbe2f-125">По умолчанию, если не указать новое имя, для имени файла App-V 5,0 будет использоваться старое имя пакета.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-125">By default, if you do not specify a new name, the old package name will be used for the App-V 5.0 filename.</span></span>

       <span data-ttu-id="dbe2f-126">Кроме того, преобразователь пакетов оптимизирует производительность пакетов в App-V 5,0, настроив пакет на потоковую ошибку пакета App-V.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-126">Additionally, the package converter optimizes performance of packages in App-V 5.0 by setting the package to stream fault the App-V package.</span></span>  <span data-ttu-id="dbe2f-127">Это более производительно, чем основной блок функций и полностью загружаемый пакет.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-127">This is more performant than the primary feature block and fully downloading the package.</span></span> <span data-ttu-id="dbe2f-128">Флаг **DownloadFullPackageOnFirstLaunch** позволяет преобразовать пакет и установить его полностью по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-128">The flag **DownloadFullPackageOnFirstLaunch** allows you to convert the package and set the package to be fully downloaded by default.</span></span>

       **<span data-ttu-id="dbe2f-129">Примечание.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-129">Note</span></span>**  
       <span data-ttu-id="dbe2f-130">Перед указанием выходного каталога необходимо создать выходной каталог.</span><span class="sxs-lookup"><span data-stu-id="dbe2f-130">Before you specify the output directory, you must create the output directory.</span></span>



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.0 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="dbe2f-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="dbe2f-131">Related topics</span></span>


[<span data-ttu-id="dbe2f-132">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="dbe2f-132">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









