---
title: Заметки о выпуске для DaRT 8.1
description: Заметки о выпуске для DaRT 8.1
author: dansimp
ms.assetid: 44303107-60f4-485c-848a-7e0529f142d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d0ba817ddd5bbdefcf7fed833f4c47e7b9d9ce0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824762"
---
# <span data-ttu-id="ed530-103">Заметки о выпуске для DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="ed530-103">Release Notes for DaRT 8.1</span></span>


**<span data-ttu-id="ed530-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="ed530-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="ed530-105">Внимательно прочтите эти заметки о выпуске, прежде чем устанавливать набор средств диагностики и восстановления Microsoft 8,1 (DaRT).</span><span class="sxs-lookup"><span data-stu-id="ed530-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.1.</span></span>

<span data-ttu-id="ed530-106">Эти заметки о выпуске содержат сведения, необходимые для успешной установки средств диагностики и восстановления 8,1.</span><span class="sxs-lookup"><span data-stu-id="ed530-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 8.1.</span></span> <span data-ttu-id="ed530-107">Заметки о выпуске также содержат сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="ed530-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="ed530-108">Если между этими заметками о выпуске и документацией для DaRT имеется разница, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="ed530-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="ed530-109">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="ed530-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="ed530-110">Известные проблемы с DaRT 8,1</span><span class="sxs-lookup"><span data-stu-id="ed530-110">Known issues with DaRT 8.1</span></span>


### <span data-ttu-id="ed530-111">Disk Commander не может восстановить поврежденную основную загрузочную запись в физическом разделе в Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="ed530-111">Disk Commander is unable to repair a corrupt master boot record in a physical partition in Windows 8.1</span></span>

<span data-ttu-id="ed530-112">В Windows 8,1 в разделе "восстановление основной загрузочной записи (MBR) или заголовков таблицы разделов GUID (GPT)" на диске с диском Commander не удается восстановить поврежденную основную загрузочную запись на физическом компьютере, поэтому не удается загрузить клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="ed530-112">In Windows 8.1, the “Restore the Master Boot Record (MBR) or the header of the GUID Partition Table (GPT)” option in Disk Commander is unable to repair a corrupt master boot record in a physical partition, and therefore is unable to boot the client computer.</span></span>

<span data-ttu-id="ed530-113">**Временное решение:** Запустите **Восстановление при запуске**, нажмите кнопку **Диагностика**и выберите пункт **Дополнительные параметры**, а затем нажмите кнопку **начать восстановление**.</span><span class="sxs-lookup"><span data-stu-id="ed530-113">**Workaround:** Start **Startup Repair**, click **Troubleshoot**, click **Advanced options**, and then click **Start repair**.</span></span>

### <span data-ttu-id="ed530-114">Несколько экземпляров очистки диска, ориентированных на один и тот же диск, приводят к возникновению сбоя в отношении всех экземпляров, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="ed530-114">Multiple instances of Disk Wipe that target the same drive cause all instances except the last one to report a failure</span></span>

<span data-ttu-id="ed530-115">Если вы запустите несколько экземпляров очистки диска, а затем попытайтесь очистить один и тот же диск с помощью двух отдельных экземпляров для очистки диска, все экземпляры, кроме последнего, сообщают о невозможности очистки диска.</span><span class="sxs-lookup"><span data-stu-id="ed530-115">If you start multiple instances of Disk Wipe, and then try to wipe the same drive by using two separate Disk Wipe instances, all instances except the last one report a failure to wipe the drive.</span></span>

<span data-ttu-id="ed530-116">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="ed530-116">**Workaround:** None.</span></span>

### <span data-ttu-id="ed530-117">Очистка диска может привести к невозможности очистки всех данных на устройствах с твердотельным состоянием с флэш-памятью.</span><span class="sxs-lookup"><span data-stu-id="ed530-117">Disk Wipe may not clear all data on solid-state drives that have flash memory</span></span>

<span data-ttu-id="ed530-118">Если вы используете очистку диска для удаления данных на устройстве с твердотельной заливкой (SSD) с флэш-памятью, все данные могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="ed530-118">If you use Disk Wipe to clear data on a solid-state drive (SSD) that has flash memory, all of the data may not be erased.</span></span> <span data-ttu-id="ed530-119">Эта проблема возникает из-за того, что встроенное по SSD управляет физическим расположением записи при запуске очистки диска.</span><span class="sxs-lookup"><span data-stu-id="ed530-119">This issue occurs because the SSD firmware controls the physical location of writes while Disk Wipe is running.</span></span>

<span data-ttu-id="ed530-120">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="ed530-120">**Workaround:** None.</span></span>

### <span data-ttu-id="ed530-121">Не удается выполнить восстановление системы при запуске мастера Locksmith или редактора реестра</span><span class="sxs-lookup"><span data-stu-id="ed530-121">System restore fails when you run Locksmith Wizard or Registry Editor</span></span>

<span data-ttu-id="ed530-122">Если вы запустите мастер Locksmith, редактор реестра и другие инструменты, восстановление системы завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="ed530-122">If you run Locksmith Wizard, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="ed530-123">**Временное решение:** Закройте и перезапустите DaRT, а затем запустите восстановление системы.</span><span class="sxs-lookup"><span data-stu-id="ed530-123">**Workaround:** Close and restart DaRT, and then start System Restore.</span></span>

### <span data-ttu-id="ed530-124">Проверка системных файлов (SFC) не запускается после запуска и закрытия мастера Locksmith или консоли управления компьютером.</span><span class="sxs-lookup"><span data-stu-id="ed530-124">System File Checker (SFC) Scan fails to run after you start and close Locksmith Wizard or Computer Management</span></span>

<span data-ttu-id="ed530-125">При запуске и последующем закрытии мастера Locksmith или средств в окне "Управление компьютером" не удается запустить средство проверки системных файлов.</span><span class="sxs-lookup"><span data-stu-id="ed530-125">If you start and then close Locksmith Wizard or tools in Computer Management, System File Checker fails to run.</span></span>

<span data-ttu-id="ed530-126">**Временное решение:** Закройте и перезапустите DaRT, а затем запустите средство проверки системных файлов.</span><span class="sxs-lookup"><span data-stu-id="ed530-126">**Workaround:** Close and restart DaRT, and then start System File Checker.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-the-windows-assessment-and-deployment-kit-is-not-installed"></a> <span data-ttu-id="ed530-127">Установщик DaRT не завершается сбоем, если комплект средств для развертывания и оценки Windows не установлен</span><span class="sxs-lookup"><span data-stu-id="ed530-127">DaRT installer does not fail when the Windows Assessment and Deployment Kit is not installed</span></span>

<span data-ttu-id="ed530-128">Если вы установили DaRT 8,1, используя командную строку для запуска установщика Windows (MSI), а также комплекта средств для развертывания и оценки Windows (WindowsADK), установка DaRT завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="ed530-128">If you install DaRT 8.1 by using the command line to run the Windows Installer (.msi), and the Windows Assessment and Deployment Kit (WindowsADK) has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="ed530-129">В настоящее время установщик DaRT 8,1 устанавливает все компоненты, кроме изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="ed530-129">Currently, the DaRT 8.1 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="ed530-130">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="ed530-130">**Workaround:** None.</span></span>

### <span data-ttu-id="ed530-131">Защитник Windows не запускается после запуска мастера Locksmith, редактора реестра, анализатора сбоев и управления компьютером</span><span class="sxs-lookup"><span data-stu-id="ed530-131">Windows Defender cannot start after Locksmith Wizard, Registry Editor, Crash Analyzer, and Computer Management are started</span></span>

<span data-ttu-id="ed530-132">Защитник Windows не запускается, если вы уже начали работу с мастером Locksmith, редактором реестра, анализатором сбоев и управлением компьютером.</span><span class="sxs-lookup"><span data-stu-id="ed530-132">Windows Defender does not start if you have already started Locksmith Wizard, Registry Editor, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="ed530-133">**Временное решение:** Закройте и перезапустите DaRT, а затем запустите Защитник Windows.</span><span class="sxs-lookup"><span data-stu-id="ed530-133">**Workaround:** Close and restart DaRT, and then start Windows Defender.</span></span>

### <span data-ttu-id="ed530-134">Защитник Windows может замедленно запускаться</span><span class="sxs-lookup"><span data-stu-id="ed530-134">Windows Defender may be slow to start</span></span>

<span data-ttu-id="ed530-135">Для запуска защитника Windows иногда требуется несколько минут.</span><span class="sxs-lookup"><span data-stu-id="ed530-135">Windows Defender sometimes takes a few minutes to start.</span></span> <span data-ttu-id="ed530-136">Индикатор выполнения показывает текущее состояние загрузки.</span><span class="sxs-lookup"><span data-stu-id="ed530-136">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="ed530-137">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="ed530-137">**Workaround:** None.</span></span>

## <span data-ttu-id="ed530-138">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ed530-138">Related topics</span></span>


[<span data-ttu-id="ed530-139">Сведения о DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="ed530-139">About DaRT 8.1</span></span>](about-dart-81.md)

 

 





