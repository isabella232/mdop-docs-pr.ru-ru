---
title: Параметры командной строки для файлов установки MED-V
description: Параметры командной строки для файлов установки MED-V
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826469"
---
# <span data-ttu-id="f5512-103">Параметры командной строки для файлов установки MED-V</span><span class="sxs-lookup"><span data-stu-id="f5512-103">Command-Line Options for MED-V Installation Files</span></span>


<span data-ttu-id="f5512-104">При установке или удалении Microsoft Enterprise Virtualization (MED-V) 2,0 вы сможете запускать установочные файлы в командной строке.</span><span class="sxs-lookup"><span data-stu-id="f5512-104">When you install or uninstall Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="f5512-105">В этом разделе описаны различные параметры, которые можно задать при установке или удалении MED-V из командной строки.</span><span class="sxs-lookup"><span data-stu-id="f5512-105">This section describes different options that you can specify when you install or uninstall MED-V at the command prompt.</span></span>

### <span data-ttu-id="f5512-106">Аргументы командной строки</span><span class="sxs-lookup"><span data-stu-id="f5512-106">Command-Line Arguments</span></span>

<span data-ttu-id="f5512-107">Вы можете использовать указанные ниже аргументы командной строки вместе с соответствующими файлами установки для MED-V.</span><span class="sxs-lookup"><span data-stu-id="f5512-107">You can use the following command-line arguments together with their respective MED-V installation files.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f5512-108">Файл установки</span><span class="sxs-lookup"><span data-stu-id="f5512-108">Installation File</span></span></th>
<th align="left"><span data-ttu-id="f5512-109">Аргумент</span><span class="sxs-lookup"><span data-stu-id="f5512-109">Argument</span></span></th>
<th align="left"><span data-ttu-id="f5512-110">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="f5512-110">Accepted Values</span></span></th>
<th align="left"><span data-ttu-id="f5512-111">Тип</span><span class="sxs-lookup"><span data-stu-id="f5512-111">Type</span></span></th>
<th align="left"><span data-ttu-id="f5512-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f5512-112">Description</span></span></th>
<th align="left"><span data-ttu-id="f5512-113">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="f5512-113">Default</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5512-114">Агент узла</span><span class="sxs-lookup"><span data-stu-id="f5512-114">Host Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-115">MEDVDIR</span><span class="sxs-lookup"><span data-stu-id="f5512-115">MEDVDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-116">&lt;путь установки&gt;</span><span class="sxs-lookup"><span data-stu-id="f5512-116">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-117">Установка</span><span class="sxs-lookup"><span data-stu-id="f5512-117">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-118">Изменение установленного каталога</span><span class="sxs-lookup"><span data-stu-id="f5512-118">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-119">При установке программы Files\Microsoft Корпоративная виртуализация рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f5512-119">Installation goes to Program Files\Microsoft Enterprise Desktop Virtualization.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5512-120">Диспетчер рабочих областей для MED-V</span><span class="sxs-lookup"><span data-stu-id="f5512-120">MED-V Workspace Packager</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-121">MEDVDIR</span><span class="sxs-lookup"><span data-stu-id="f5512-121">MEDVDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-122">&lt;путь установки&gt;</span><span class="sxs-lookup"><span data-stu-id="f5512-122">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-123">Установка</span><span class="sxs-lookup"><span data-stu-id="f5512-123">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-124">Изменение установленного каталога</span><span class="sxs-lookup"><span data-stu-id="f5512-124">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-125">При установке программы Files\Microsoft Корпоративная виртуализация рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f5512-125">Installation goes to Program Files\Microsoft Enterprise Desktop Virtualization.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5512-126">Рабочая область MED-V</span><span class="sxs-lookup"><span data-stu-id="f5512-126">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-127">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="f5512-127">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-128">&lt;путь установки&gt;</span><span class="sxs-lookup"><span data-stu-id="f5512-128">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-129">Установка</span><span class="sxs-lookup"><span data-stu-id="f5512-129">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-130">Изменение установленного каталога</span><span class="sxs-lookup"><span data-stu-id="f5512-130">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-131">Установка переходит на ProgramData\Microsoft\Medv\Workspace.</span><span class="sxs-lookup"><span data-stu-id="f5512-131">Installation goes to ProgramData\Microsoft\Medv\Workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5512-132">Рабочая область MED-V</span><span class="sxs-lookup"><span data-stu-id="f5512-132">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-133">ПЕРЕЗАПИСАТЬ VHD</span><span class="sxs-lookup"><span data-stu-id="f5512-133">OVERWRITE VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-134">0или1</span><span class="sxs-lookup"><span data-stu-id="f5512-134">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-135">Установка</span><span class="sxs-lookup"><span data-stu-id="f5512-135">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-136">Установка завершается сбоем, если существует VHD (0) или перезаписать существующий виртуальный жесткий диск (1).</span><span class="sxs-lookup"><span data-stu-id="f5512-136">Fail installation if VHD exists(0) or overwrite existing VHD(1).</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-137">Перезапись не происходит, и установка завершается сбоем, если виртуальный жесткий диск (VHD) уже существует.</span><span class="sxs-lookup"><span data-stu-id="f5512-137">Overwrite does not occur and installation fails if a virtual hard disk (VHD) already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5512-138">Рабочая область MED-V</span><span class="sxs-lookup"><span data-stu-id="f5512-138">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-139">SUPPRESSMEDVLAUNCH</span><span class="sxs-lookup"><span data-stu-id="f5512-139">SUPPRESSMEDVLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-140">0или1</span><span class="sxs-lookup"><span data-stu-id="f5512-140">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-141">Установка</span><span class="sxs-lookup"><span data-stu-id="f5512-141">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-142">Начало (0) или не запускается (1) MED-V после установки рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="f5512-142">Start(0) or do not start(1) MED-V after MED-V workspace is installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-143">Если Рабочая область MED-V была установлена с пользовательским интерфейсом, флажок на <strong> странице "Готово" определяет, </strong> следует ли запускать med-v.</span><span class="sxs-lookup"><span data-stu-id="f5512-143">If the MED-V workspace was installed with the user interface (UI), a check box on the <strong>Finish</strong> page controls whether to start MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5512-144">Рабочая область MED-V</span><span class="sxs-lookup"><span data-stu-id="f5512-144">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-145">DELETEDIFFDISKS</span><span class="sxs-lookup"><span data-stu-id="f5512-145">DELETEDIFFDISKS</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-146">0или1</span><span class="sxs-lookup"><span data-stu-id="f5512-146">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-147">Удаление</span><span class="sxs-lookup"><span data-stu-id="f5512-147">Uninstallation</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-148">Сохранить (0) или удалить (1) виртуальные жесткие диски, созданные MED-V</span><span class="sxs-lookup"><span data-stu-id="f5512-148">Keep(0) or delete(1) VHDs created by MED-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5512-149">Виртуальные жесткие диски не удаляются.</span><span class="sxs-lookup"><span data-stu-id="f5512-149">No VHDs are deleted.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f5512-150">Примеры аргументов командной строки</span><span class="sxs-lookup"><span data-stu-id="f5512-150">Examples of Command-Line Arguments</span></span>

<span data-ttu-id="f5512-151">В следующем примере выполняется установка рабочей области MED-V, созданной с помощью диспетчера рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="f5512-151">The following example installs the MED-V workspace created by the MED-V workspace Packager.</span></span> <span data-ttu-id="f5512-152">Файл установки создает файл журнала в каталоге TEMP и запускает установочный файл в тихом режиме, но не запускает агент узла MED-V по завершении.</span><span class="sxs-lookup"><span data-stu-id="f5512-152">The installation file creates a log file in the Temp directory and runs the installation file in quiet mode, but does not start the MED-V Host Agent on completion.</span></span> <span data-ttu-id="f5512-153">Установочный файл перезаписывает все VHD-файлы, оставшиеся после предыдущей установки с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="f5512-153">The installation file overwrites any VHD left behind by a previous installation that has the same name.</span></span>

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

<span data-ttu-id="f5512-154">В следующем примере удаляется Рабочая область MED-V, которая ранее была установлена.</span><span class="sxs-lookup"><span data-stu-id="f5512-154">The following example uninstalls the MED-V workspace that was previously installed.</span></span> <span data-ttu-id="f5512-155">Файл установки создает файл журнала в каталоге TEMP и запускает установочный файл в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="f5512-155">The installation file creates a log file in the Temp directory and runs the installation file in quiet mode.</span></span> <span data-ttu-id="f5512-156">Установочный файл удаляет все оставшиеся файлы виртуального жесткого диска из файловой системы.</span><span class="sxs-lookup"><span data-stu-id="f5512-156">The installation file deletes any remaining virtual hard disk files from the file system.</span></span>

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## <span data-ttu-id="f5512-157">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f5512-157">Related topics</span></span>


[<span data-ttu-id="f5512-158">Развертывание компонентов MED-V</span><span class="sxs-lookup"><span data-stu-id="f5512-158">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

[<span data-ttu-id="f5512-159">Технический справочник по MED-V</span><span class="sxs-lookup"><span data-stu-id="f5512-159">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





