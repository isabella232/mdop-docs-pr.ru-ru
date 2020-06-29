---
title: Создание образа для восстановления DaRT 7.0
description: Создание образа для восстановления DaRT 7.0
author: dansimp
ms.assetid: ebb2ec58-0349-469d-a23f-3f944fe4c1fa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19ff144cac61ca7ea5a8498f67caf8a99229d77
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823282"
---
# <span data-ttu-id="75109-103">Создание образа для восстановления DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="75109-103">Creating the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="75109-104">Набор средств диагностики и восстановления Microsoft (DaRT) 7 включает **мастер изображений для восстановления DaRT** , который используется в Windows для создания загрузочного образа международной организации по стандартизации (ISO).</span><span class="sxs-lookup"><span data-stu-id="75109-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="75109-105">ISO-образ — это файл, который представляет собой необработанное содержимое компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="75109-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

## <span data-ttu-id="75109-106">Создание образа восстановления с помощью мастера создания образа восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="75109-106">Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="75109-107">ISO-файл, созданный с помощью мастера создания образа для восстановления DaRT, включает в себя изображение для восстановления DaRT, позволяющее загрузить компьютер с ошибкой, даже если он не запускается в противном случае.</span><span class="sxs-lookup"><span data-stu-id="75109-107">The ISO created by the DaRT Recovery Image Wizard contains the DaRT recovery image that lets you boot into a problem computer, even if it might otherwise not start.</span></span> <span data-ttu-id="75109-108">После загрузки компьютера на DaRT вы можете использовать различные инструменты DaRT для диагностики и восстановления компьютера.</span><span class="sxs-lookup"><span data-stu-id="75109-108">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span>

<span data-ttu-id="75109-109">Вы можете записать ISO на записываемый компакт-диск или DVD-диски, сохранить его на USB-накопитель или сохранить в формате, который можно использовать для загрузки DaRT из удаленной секции или из раздела восстановления.</span><span class="sxs-lookup"><span data-stu-id="75109-109">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span> <span data-ttu-id="75109-110">Дополнительные сведения можно найти [в разделе Развертывание образа для восстановления DaRT 7,0](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="75109-110">For more information, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="75109-111">**Примечание**  Если на вашем компьютере есть дисковод CD-RW, мастер предлагает записать образ ISO на чистый компакт-диск или DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="75109-111">**Note** If your computer includes a CD-RW drive, the wizard offers to burn the ISO image to a blank CD or DVD.</span></span> <span data-ttu-id="75109-112">Если на компьютере не установлен диск, который поддерживается мастером, вы можете записать образ ISO на компакт-диск или DVD-диск, используя большинство программ, которые могут записывать компакт-диски и DVD-диски.</span><span class="sxs-lookup"><span data-stu-id="75109-112">If your computer does not include a drive that is supported by the wizard, you can burn the ISO image onto a CD or DVD by using most programs that can burn a CD or DVD.</span></span>

 

<span data-ttu-id="75109-113">Чтобы создать загрузочный компакт-диск или DVD-диск из образа ISO, необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="75109-113">To create a bootable CD or DVD from the ISO image, you must have:</span></span>

-   <span data-ttu-id="75109-114">Дисковод CD-RW.</span><span class="sxs-lookup"><span data-stu-id="75109-114">A CD-RW drive.</span></span>

-   <span data-ttu-id="75109-115">Записываемый компакт-диск или DVD-диск (в формате, поддерживаемом записываемым диском).</span><span class="sxs-lookup"><span data-stu-id="75109-115">A recordable CD or DVD (in a format supported by the recordable drive).</span></span>

-   <span data-ttu-id="75109-116">Программное обеспечение, поддерживающее записывающее устройство и поддерживающее запись образа ISO непосредственно на компакт-диск или DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="75109-116">Software that supports the recordable drive and supports burning an ISO image directly to CD or DVD.</span></span>

    <span data-ttu-id="75109-117">**Важно!**  Протестируйте компакт-диск или DVD-диск, созданный на всех компьютерах, на которых вы собираетесь поддерживать, так как некоторые компьютеры не могут начать работу со съемных носителей с поддержкой записи.</span><span class="sxs-lookup"><span data-stu-id="75109-117">**Important** Test the CD or DVD that you create on all the different kinds of computers that you intend to support because some computers cannot start from all kinds of recordable media.</span></span>

     

<span data-ttu-id="75109-118">Чтобы сохранить образ ISO на USB-накопителе (UFD), необходимо:</span><span class="sxs-lookup"><span data-stu-id="75109-118">To save the ISO image to a USB flash drive (UFD), you must have:</span></span>

-   <span data-ttu-id="75109-119">Правильно отформатированное устройство флэш-памяти.</span><span class="sxs-lookup"><span data-stu-id="75109-119">A correctly formatted UFD.</span></span>

-   <span data-ttu-id="75109-120">Программа, которую можно использовать для подключения образа ISO.</span><span class="sxs-lookup"><span data-stu-id="75109-120">A program that you can use to mount the ISO image.</span></span>

[<span data-ttu-id="75109-121">Использование мастера образа для восстановления DaRT для создания образа для восстановления</span><span class="sxs-lookup"><span data-stu-id="75109-121">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)

## <span data-ttu-id="75109-122">Создание образа с ограниченным временем восстановления</span><span class="sxs-lookup"><span data-stu-id="75109-122">Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="75109-123">Вы можете создать изображение для восстановления DaRT, которое может быть использовано только в течение определенного количества дней после его создания.</span><span class="sxs-lookup"><span data-stu-id="75109-123">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="75109-124">Для этого необходимо запустить **Мастер создания образа для восстановления DaRT** в командной строке и указать количество дней.</span><span class="sxs-lookup"><span data-stu-id="75109-124">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

[<span data-ttu-id="75109-125">Создание образа для восстановления с ограничением по времени</span><span class="sxs-lookup"><span data-stu-id="75109-125">How to Create a Time Limited Recovery Image</span></span>](how-to-create-a-time-limited-recovery-image-dart-7.md)

## <span data-ttu-id="75109-126">Другие ресурсы для создания образа восстановления DaRT7</span><span class="sxs-lookup"><span data-stu-id="75109-126">Other resources for creating the DaRT7 recovery image</span></span>


-   [<span data-ttu-id="75109-127">Развертывание DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="75109-127">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





