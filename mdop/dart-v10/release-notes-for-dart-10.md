---
title: Заметки о выпуске для DaRT 10
description: Заметки о выпуске для DaRT 10
author: dansimp
ms.assetid: eb996980-f9c4-42cb-bde9-6b3d4b82b58c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 12ae5865538155f3c9ecf8b5f23b0d9e23232833
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822952"
---
# <span data-ttu-id="634ed-103">Заметки о выпуске для DaRT 10</span><span class="sxs-lookup"><span data-stu-id="634ed-103">Release Notes for DaRT 10</span></span>


**<span data-ttu-id="634ed-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="634ed-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="634ed-105">Внимательно прочитайте эти заметки о выпуске, прежде чем устанавливать набор средств диагностики и восстановления Microsoft (DaRT) 10.</span><span class="sxs-lookup"><span data-stu-id="634ed-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span></span>

<span data-ttu-id="634ed-106">Эти заметки о выпуске содержат сведения, необходимые для успешной установки набора средств диагностики и восстановления 10.</span><span class="sxs-lookup"><span data-stu-id="634ed-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 10.</span></span> <span data-ttu-id="634ed-107">Заметки о выпуске также содержат сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="634ed-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="634ed-108">Если между этими заметками о выпуске и документацией для DaRT имеется разница, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="634ed-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="634ed-109">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="634ed-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="634ed-110">Известные проблемы с DaRT 10</span><span class="sxs-lookup"><span data-stu-id="634ed-110">Known issues with DaRT 10</span></span>


### <span data-ttu-id="634ed-111">Disk Commander не может восстановить поврежденную основную загрузочную запись в физическом разделе в Windows 10</span><span class="sxs-lookup"><span data-stu-id="634ed-111">Disk Commander is unable to repair a corrupt master boot record in a physical partition in Windows 10</span></span>

<span data-ttu-id="634ed-112">В Windows 10 в разделе "восстановление основной загрузочной записи (MBR) или заголовков таблицы разделов GUID (GPT)" на диске с диском Commander не удается восстановить поврежденную основную загрузочную запись на физическом компьютере, поэтому не удается загрузить клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="634ed-112">In Windows 10, the “Restore the Master Boot Record (MBR) or the header of the GUID Partition Table (GPT)” option in Disk Commander is unable to repair a corrupt master boot record in a physical partition, and therefore is unable to boot the client computer.</span></span>

<span data-ttu-id="634ed-113">**Временное решение:** Запустите **Восстановление при запуске**, нажмите кнопку **Диагностика**и выберите пункт **Дополнительные параметры**, а затем нажмите кнопку **начать восстановление**.</span><span class="sxs-lookup"><span data-stu-id="634ed-113">**Workaround:** Start **Startup Repair**, click **Troubleshoot**, click **Advanced options**, and then click **Start repair**.</span></span>

### <span data-ttu-id="634ed-114">Несколько экземпляров очистки диска, ориентированных на один и тот же диск, приводят к возникновению сбоя в отношении всех экземпляров, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="634ed-114">Multiple instances of Disk Wipe that target the same drive cause all instances except the last one to report a failure</span></span>

<span data-ttu-id="634ed-115">Если вы запустите несколько экземпляров очистки диска, а затем попытайтесь очистить один и тот же диск с помощью двух отдельных экземпляров для очистки диска, все экземпляры, кроме последнего, сообщают о невозможности очистки диска.</span><span class="sxs-lookup"><span data-stu-id="634ed-115">If you start multiple instances of Disk Wipe, and then try to wipe the same drive by using two separate Disk Wipe instances, all instances except the last one report a failure to wipe the drive.</span></span>

<span data-ttu-id="634ed-116">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="634ed-116">**Workaround:** None.</span></span>

### <span data-ttu-id="634ed-117">Очистка диска может привести к невозможности очистки всех данных на устройствах с твердотельным состоянием с флэш-памятью.</span><span class="sxs-lookup"><span data-stu-id="634ed-117">Disk Wipe may not clear all data on solid-state drives that have flash memory</span></span>

<span data-ttu-id="634ed-118">Если вы используете очистку диска для удаления данных на устройстве с твердотельной заливкой (SSD) с флэш-памятью, все данные могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="634ed-118">If you use Disk Wipe to clear data on a solid-state drive (SSD) that has flash memory, all of the data may not be erased.</span></span> <span data-ttu-id="634ed-119">Эта проблема возникает из-за того, что встроенное по SSD управляет физическим расположением записи при запуске очистки диска.</span><span class="sxs-lookup"><span data-stu-id="634ed-119">This issue occurs because the SSD firmware controls the physical location of writes while Disk Wipe is running.</span></span>

<span data-ttu-id="634ed-120">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="634ed-120">**Workaround:** None.</span></span>

### <span data-ttu-id="634ed-121">Не удается выполнить восстановление системы при запуске мастера Locksmith или редактора реестра</span><span class="sxs-lookup"><span data-stu-id="634ed-121">System restore fails when you run Locksmith Wizard or Registry Editor</span></span>

<span data-ttu-id="634ed-122">Если вы запустите мастер Locksmith, редактор реестра и другие инструменты, восстановление системы завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="634ed-122">If you run Locksmith Wizard, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="634ed-123">**Временное решение:** Закройте и перезапустите DaRT, а затем запустите восстановление системы.</span><span class="sxs-lookup"><span data-stu-id="634ed-123">**Workaround:** Close and restart DaRT, and then start System Restore.</span></span>

### <span data-ttu-id="634ed-124">Проверка системных файлов (SFC) не запускается после запуска и закрытия мастера Locksmith или консоли управления компьютером.</span><span class="sxs-lookup"><span data-stu-id="634ed-124">System File Checker (SFC) Scan fails to run after you start and close Locksmith Wizard or Computer Management</span></span>

<span data-ttu-id="634ed-125">При запуске и последующем закрытии мастера Locksmith или средств в окне "Управление компьютером" не удается запустить средство проверки системных файлов.</span><span class="sxs-lookup"><span data-stu-id="634ed-125">If you start and then close Locksmith Wizard or tools in Computer Management, System File Checker fails to run.</span></span>

<span data-ttu-id="634ed-126">**Временное решение:** Закройте и перезапустите DaRT, а затем запустите средство проверки системных файлов.</span><span class="sxs-lookup"><span data-stu-id="634ed-126">**Workaround:** Close and restart DaRT, and then start System File Checker.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-the-windows-assessment-and-deployment-kit-is-not-installed"></a> <span data-ttu-id="634ed-127">Установщик DaRT не завершается сбоем, если комплект средств для развертывания и оценки Windows не установлен</span><span class="sxs-lookup"><span data-stu-id="634ed-127">DaRT installer does not fail when the Windows Assessment and Deployment Kit is not installed</span></span>

<span data-ttu-id="634ed-128">Если вы установили DaRT 10, используя командную строку для запуска установщика Windows (MSI), и комплект средств для развертывания и оценки Windows (WindowsADK) не установлен, установка DaRT завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="634ed-128">If you install DaRT 10 by using the command line to run the Windows Installer (.msi), and the Windows Assessment and Deployment Kit (WindowsADK) has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="634ed-129">В настоящее время установщик DaRT 10 устанавливает все компоненты, кроме изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="634ed-129">Currently, the DaRT 10 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="634ed-130">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="634ed-130">**Workaround:** None.</span></span>

## <span data-ttu-id="634ed-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="634ed-131">Related topics</span></span>


[<span data-ttu-id="634ed-132">Сведения о DaRT 10</span><span class="sxs-lookup"><span data-stu-id="634ed-132">About DaRT 10</span></span>](about-dart-10.md)

 

 





