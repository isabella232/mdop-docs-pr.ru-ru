---
title: Развертывание образа для восстановления DaRT в качестве части раздела восстановления
description: Развертывание образа для восстановления DaRT в качестве части раздела восстановления
author: dansimp
ms.assetid: 462f2d08-f03b-4a07-b2d3-c69205dc6f70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e75c3f9e58d784c13003feb84001f89c4607115d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823559"
---
# <span data-ttu-id="48a09-103">Развертывание образа для восстановления DaRT в качестве части раздела восстановления</span><span class="sxs-lookup"><span data-stu-id="48a09-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="48a09-104">После завершения работы мастера изображений для восстановления DaRT и создания образа восстановления вы можете извлечь файл Boot. wim из файла образа ISO и развернуть его как раздел восстановления в образе Windows 7.</span><span class="sxs-lookup"><span data-stu-id="48a09-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

**<span data-ttu-id="48a09-105">Развертывание DaRT в разделе восстановления образа Windows 7</span><span class="sxs-lookup"><span data-stu-id="48a09-105">To deploy DaRT in the recovery partition of a Windows 7 image</span></span>**

1.  <span data-ttu-id="48a09-106">Создайте конечную секцию в том формате Windows 7, которая больше или равна размеру файла образа ISO, созданного с помощью **мастера подготовки изображений для восстановления**.</span><span class="sxs-lookup"><span data-stu-id="48a09-106">Create a target partition in your Windows 7 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT Recovery Image Wizard**.</span></span>

    <span data-ttu-id="48a09-107">Минимальный размер, необходимый для раздела DaRT, составляет примерно 300MB.</span><span class="sxs-lookup"><span data-stu-id="48a09-107">The minimum size required for a DaRT partition is approximately 300MB.</span></span> <span data-ttu-id="48a09-108">Тем не менее, мы рекомендуем 450MB, чтобы они соответствовали возможностям удаленного подключения для DaRT.</span><span class="sxs-lookup"><span data-stu-id="48a09-108">However, we recommend 450MB to accommodate for the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="48a09-109">Извлеките файл Boot. wim из файла образа DaRT ISO.</span><span class="sxs-lookup"><span data-stu-id="48a09-109">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="48a09-110">Подключите файл образа ISO, созданный в диалоговом окне **Создание образа запуска** , с помощью предпочтительного способа подключения образа.</span><span class="sxs-lookup"><span data-stu-id="48a09-110">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="48a09-111">Откройте файл образа ISO и скопируйте файл Boot. wim из папки \\sources на подключенном образе в расположение на вашем компьютере или на внешнем диске.</span><span class="sxs-lookup"><span data-stu-id="48a09-111">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="48a09-112">**Примечание**  Если вы загрузили CD или DVD-диск в образ восстановления, вы можете открыть файлы на компакт-диске или DVD-диске и скопировать файл Boot. wim из папки \\sources.</span><span class="sxs-lookup"><span data-stu-id="48a09-112">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="48a09-113">Это позволяет пропустить необходимость монтировать образ.</span><span class="sxs-lookup"><span data-stu-id="48a09-113">This lets you skip the need to mount the image.</span></span>

         

3.  <span data-ttu-id="48a09-114">С помощью файла Boot. wim Создайте загрузочный раздел для восстановления с помощью стандартного метода для создания собственного образа Windows RE.</span><span class="sxs-lookup"><span data-stu-id="48a09-114">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="48a09-115">Дополнительные сведения о том, как создать или настроить раздел восстановления, можно найти [в разделе Настройка среды Windows RE](https://go.microsoft.com/fwlink/?LinkId=214222).</span><span class="sxs-lookup"><span data-stu-id="48a09-115">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="48a09-116">Замените конечную секцию в образе Windows 7 на раздел восстановления.</span><span class="sxs-lookup"><span data-stu-id="48a09-116">Replace the target partition in your Windows 7 image with the recovery partition.</span></span>

<span data-ttu-id="48a09-117">После того как вы будете готовы к сообразу Windows 7, распространите изображение на компьютеры организации с помощью стандартного процесса развертывания образа вашей компании.</span><span class="sxs-lookup"><span data-stu-id="48a09-117">After your Windows 7 image is ready, distribute the image to computers in your enterprise by using your company’s standard image deployment process.</span></span> <span data-ttu-id="48a09-118">Дополнительные сведения о том, как создать образ Windows 7, приведены в [статье Создание стандартного образа Windows 7: пошаговое руководство](https://go.microsoft.com/fwlink/?LinkId=212103).</span><span class="sxs-lookup"><span data-stu-id="48a09-118">For more information about how to create a Windows 7 image, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=212103).</span></span>

<span data-ttu-id="48a09-119">Дополнительные сведения о том, как развернуть решение для восстановления для повторной установки заводского образа в случае сбоя системы, можно найти в разделе [развертывание образа восстановления системы](https://go.microsoft.com/fwlink/?LinkId=214221).</span><span class="sxs-lookup"><span data-stu-id="48a09-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="48a09-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="48a09-120">Related topics</span></span>


[<span data-ttu-id="48a09-121">Развертывание образа для восстановления DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="48a09-121">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





