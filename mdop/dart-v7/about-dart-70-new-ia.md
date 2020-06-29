---
title: Сведения о DaRT 7.0
description: Сведения о DaRT 7.0
author: dansimp
ms.assetid: 217ffafc-6d73-4b80-88d9-71870460d4ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cd647b2f596ce88ce38580f08422ff8f92b35c06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823272"
---
# <span data-ttu-id="337af-103">Сведения о DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="337af-103">About DaRT 7.0</span></span>


<span data-ttu-id="337af-104">Набор средств диагностики и восстановления Microsoft (DaRT) 7 помогает устранять неполадки и восстанавливать настольные компьютеры под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="337af-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 helps you troubleshoot and repair Windows-based desktops.</span></span> <span data-ttu-id="337af-105">Сюда входят такие настольные компьютеры, которые не могут быть запущены.</span><span class="sxs-lookup"><span data-stu-id="337af-105">This includes those desktops that cannot be started.</span></span> <span data-ttu-id="337af-106">DaRT — это мощный набор инструментов, расширяющий среду восстановления Windows (WinRE).</span><span class="sxs-lookup"><span data-stu-id="337af-106">DaRT is a powerful set of tools that extend the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="337af-107">С помощью DaRT вы можете проанализировать проблемы, чтобы определить ее причину, например, проверив журнал событий компьютера или системный реестр.</span><span class="sxs-lookup"><span data-stu-id="337af-107">By using DaRT, you can analyze an issue to determine its cause, for example, by inspecting the computer’s event log or system registry.</span></span>

<span data-ttu-id="337af-108">DaRT также содержит инструменты, которые помогут вам устранить проблему, как только вы определите ее причину.</span><span class="sxs-lookup"><span data-stu-id="337af-108">DaRT also provides tools to help you fix a problem as soon as you determine the cause.</span></span> <span data-ttu-id="337af-109">Например, с помощью средств DaRT вы можете отключить неисправный драйвер устройства, удалить исправления, восстановить удаленные файлы и проверить компьютер на наличие вредоносных программ, даже если вы не можете запускать установленную операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="337af-109">For example, you can use the tools in DaRT to disable a faulty device driver, remove hotfixes, restore deleted files, and scan the computer for malware even when you cannot or should not start the installed Windows operating system.</span></span>

<span data-ttu-id="337af-110">DaRT помогает быстро восстанавливать компьютеры под управлением Windows 7 64 или более чем с 32-разрядных версий, обычно за меньшее время, чем при переобразе компьютера.</span><span class="sxs-lookup"><span data-stu-id="337af-110">DaRT can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 7, typically in less time than it would take to reimage the computer.</span></span>

## <span data-ttu-id="337af-111">Об образе для восстановления DaRT 7</span><span class="sxs-lookup"><span data-stu-id="337af-111">About the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="337af-112">Функция DaRT позволяет создавать образы восстановления, основанные на WinRE, в сочетании с набором средств, предоставляемых DaRT.</span><span class="sxs-lookup"><span data-stu-id="337af-112">Functionality in DaRT lets you create a recovery image that is based on WinRE combined with a set of tools that DaRT provides.</span></span> <span data-ttu-id="337af-113">Изображение для восстановления DaRT использует преимущества WinRE, из которого можно получить доступ к окну **инструментов Диагностика и восстановление** .</span><span class="sxs-lookup"><span data-stu-id="337af-113">The DaRT recovery image takes advantage of WinRE, from which you can access the **Diagnostics and Recovery Toolset** window.</span></span>

<span data-ttu-id="337af-114">С помощью **мастера изображений для восстановления** DART вы можете создать изображение для восстановления стрелок.</span><span class="sxs-lookup"><span data-stu-id="337af-114">Use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span> <span data-ttu-id="337af-115">По умолчанию мастер создает файл изображения Международной организации по стандартизации (ISO) на рабочем столе с именем DaRT70. ISO, но вы можете указать другое расположение и имя файла.</span><span class="sxs-lookup"><span data-stu-id="337af-115">By default, the wizard creates an International Organization for Standardization (ISO) image file on your desktop that is named DaRT70.iso, although you can specify a different location and file name.</span></span> <span data-ttu-id="337af-116">Мастер также позволяет записать изображение на компакт-диск или DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="337af-116">The wizard also lets you burn the image to a CD or DVD.</span></span> <span data-ttu-id="337af-117">Завершив работу мастера, вы можете сохранить образ восстановления на USB-накопитель или сохранить его в формате, который можно использовать для создания удаленной секции или раздела восстановления.</span><span class="sxs-lookup"><span data-stu-id="337af-117">After you have finished the wizard, you can save the recovery image to a USB flash drive or save it in a format that you can use to create a remote partition or a recovery partition.</span></span>

<span data-ttu-id="337af-118">Если вы хотите использовать DaRT для запуска компьютера конечного пользователя, который не запускается, вы можете выполнить инструкции по [восстановлению локальных компьютеров с помощью DaRT Recovery](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="337af-118">When you have to use DaRT to startup an end-user computer that will not start, you can follow the instructions at [How to Recover Local Computers Using the DaRT Recovery Image](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="337af-119">Подробные сведения о средствах DaRT можно найти в статье [Обзор средств на dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="337af-119">For detailed information about the tools in DaRT, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

## <a href="" id="what-s-new-in-dart-7"></a><span data-ttu-id="337af-120">Новые возможности DaRT 7</span><span class="sxs-lookup"><span data-stu-id="337af-120">What’s New in DaRT 7</span></span>


<span data-ttu-id="337af-121">DaRT7 продолжает поддерживать все сценарии, включенные в предыдущие версии, и добавляет новую функцию удаленного подключения в дополнение к трем новым параметрам развертывания.</span><span class="sxs-lookup"><span data-stu-id="337af-121">DaRT7 continues to support all the scenarios included in previous versions and it adds a new Remote Connection feature in addition to three new deployment options.</span></span>

### <span data-ttu-id="337af-122">Создание изображений DaRT 7</span><span class="sxs-lookup"><span data-stu-id="337af-122">DaRT 7 Image Creation</span></span>

<span data-ttu-id="337af-123">Мастер, который используется для создания изображений DaRT ISO, теперь называется **изображением** для переноса DART, и теперь поддерживает возможность включения и отключения новой функции удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="337af-123">The wizard that you use to create DaRT ISO images is now called **DaRT Recovery Image** and it now supports an option to enable or disable the new Remote Connection feature.</span></span> <span data-ttu-id="337af-124">Удаленное подключение позволяет агенту службы поддержки запускать инструменты DaRT из удаленного местоположения.</span><span class="sxs-lookup"><span data-stu-id="337af-124">Remote Connection lets a helpdesk agent run the DaRT tools from a remote location.</span></span> <span data-ttu-id="337af-125">В предыдущих выпусках агент службы поддержки был физически представлен на компьютере конечного пользователя для запуска инструментов DaRT.</span><span class="sxs-lookup"><span data-stu-id="337af-125">In previous releases, the helpdesk agent had to be physically present at the end-user computer to run the DaRT tools.</span></span>

<span data-ttu-id="337af-126">Кроме того, мастер позволяет настроить приветственное сообщение для функции удаленного подключения (сообщение отображается, когда пользователь запускает средство удаленного подключения).</span><span class="sxs-lookup"><span data-stu-id="337af-126">The wizard also lets you customize the Welcome message for the Remote Connection feature (the message is shown when end users run the Remote Connection tool).</span></span> <span data-ttu-id="337af-127">ИТ — администраторы также могут настроить номер порта, который должен использоваться удаленным подключением.</span><span class="sxs-lookup"><span data-stu-id="337af-127">IT Admins can also configure which Port Number should be used by Remote Connection.</span></span>

<span data-ttu-id="337af-128">Дополнительные сведения о **мастере изображений для восстановления** DART и удаленном подключении можно найти [в разделе Создание образа для восстановления DaRT 7,0](creating-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="337af-128">For more information about the **DaRT Recovery Image Wizard** or Remote Connection, see [Creating the DaRT 7.0 Recovery Image](creating-the-dart-70-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="337af-129">DaRT 7 развертывание ISO</span><span class="sxs-lookup"><span data-stu-id="337af-129">DaRT 7 ISO Deployment</span></span>

<span data-ttu-id="337af-130">Помимо записи на компакт-диск или DVD-диск, DaRT7 добавляет три новых параметра при развертывании ISO-файла, содержащего изображение для переноса DaRT.</span><span class="sxs-lookup"><span data-stu-id="337af-130">In addition to burning to a CD or DVD, DaRT7 adds three new options when you deploy the ISO that contains the DaRT recovery image:</span></span>

-   <span data-ttu-id="337af-131">Развертывание USB-накопителя</span><span class="sxs-lookup"><span data-stu-id="337af-131">USB flash drive deployment</span></span>

-   <span data-ttu-id="337af-132">Удаленное развертывание секций</span><span class="sxs-lookup"><span data-stu-id="337af-132">Remote partition deployment</span></span>

-   <span data-ttu-id="337af-133">Развертывание раздела восстановления</span><span class="sxs-lookup"><span data-stu-id="337af-133">Recovery partition deployment</span></span>

<span data-ttu-id="337af-134">Параметр развертывания флэш-накопителя USB позволяет компании использовать DaRT на компьютерах, на которых не установлены компакт-диски и DVD-дисководы.</span><span class="sxs-lookup"><span data-stu-id="337af-134">The USB flash drive deployment option lets a company use DaRT on computers that do not have CD or DVD drives available.</span></span> <span data-ttu-id="337af-135">Параметры восстановления и удаленных секций позволяют пользователям легко получать доступ к изображению DaRT и включать функцию удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="337af-135">The recovery and remote partition options let end users have easy access to the DaRT image and to enable the Remote Connection functionality.</span></span>

<span data-ttu-id="337af-136">Дополнительные сведения о развертывании изображений для восстановления DaRT можно найти [в разделе Развертывание образа для восстановления dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="337af-136">For more information about how to deploy DaRT recovery images, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="337af-137">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="337af-137">Related topics</span></span>


[<span data-ttu-id="337af-138">Начало работы с DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="337af-138">Getting Started with DaRT 7.0</span></span>](getting-started-with-dart-70-new-ia.md)

[<span data-ttu-id="337af-139">Заметки о выпуске для DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="337af-139">Release Notes for DaRT 7.0</span></span>](release-notes-for-dart-70-new-ia.md)

 

 





