---
title: Развертывание образа для восстановления DaRT в качестве части раздела восстановления
description: Развертывание образа для восстановления DaRT в качестве части раздела восстановления
author: dansimp
ms.assetid: 07c5d539-51d9-4759-adc7-72b40d5d7bb3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e3647d684f64a0635e2875314498bde841204369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824382"
---
# <span data-ttu-id="74adc-103">Развертывание образа для восстановления DaRT в качестве части раздела восстановления</span><span class="sxs-lookup"><span data-stu-id="74adc-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="74adc-104">После того как вы закончите работу мастера создания образа восстановления для Microsoft Diagnostics и восстановления (DaRT) 8,0 и создали образ восстановления, вы можете извлечь файл Boot. wim из файла образа ISO и развернуть его как раздел восстановления в образе Windows 8.</span><span class="sxs-lookup"><span data-stu-id="74adc-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 8 image.</span></span> <span data-ttu-id="74adc-105">Рекомендуется использовать раздел, поскольку любые проблемы с повреждением, препятствующие запуску операционной системы Windows, также препятствуют запуску образа восстановления.</span><span class="sxs-lookup"><span data-stu-id="74adc-105">A partition is recommended, because any corruption issues that prevent the Windows operating system from starting would also prevent the recovery image from starting.</span></span> <span data-ttu-id="74adc-106">Кроме того, отдельный раздел исключает необходимость предоставления ключа восстановления BitLocker дважды.</span><span class="sxs-lookup"><span data-stu-id="74adc-106">A separate partition also eliminates the need to provide the BitLocker recovery key twice.</span></span> <span data-ttu-id="74adc-107">Чтобы запретить пользователям хранить на нем файлы, возможно, нужно скрыть раздел.</span><span class="sxs-lookup"><span data-stu-id="74adc-107">Consider hiding the partition to prevent users from storing files on it.</span></span>

**<span data-ttu-id="74adc-108">Развертывание DaRT в разделе восстановления на изображении для Windows 8</span><span class="sxs-lookup"><span data-stu-id="74adc-108">To deploy DaRT in the recovery partition of a Windows 8 image</span></span>**

1.  <span data-ttu-id="74adc-109">Создайте конечную секцию в том формате Windows 8, которая больше или равна размеру файла образа ISO, созданного с помощью **мастера создания образа восстановления для DaRT 8,0**.</span><span class="sxs-lookup"><span data-stu-id="74adc-109">Create a target partition in your Windows 8 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT 8.0 Recovery Image wizard**.</span></span>

    <span data-ttu-id="74adc-110">Минимальный размер, необходимый для раздела DaRT, 500MB в соответствии с функциями удаленного подключения для DaRT.</span><span class="sxs-lookup"><span data-stu-id="74adc-110">The minimum size required for a DaRT partition is 500MB to accommodate the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="74adc-111">Извлеките файл Boot. wim из файла образа DaRT ISO.</span><span class="sxs-lookup"><span data-stu-id="74adc-111">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="74adc-112">Используя предпочтительный метод вашей компании, подключите файл образа ISO, созданный на странице **Создание загрузочного образа** .</span><span class="sxs-lookup"><span data-stu-id="74adc-112">Using your company’s preferred method, mount the ISO image file that you created on the **Create Startup Image** page.</span></span>

    2.  <span data-ttu-id="74adc-113">Откройте файл образа ISO и скопируйте файл Boot. wim из папки \\sources на подключенном образе в расположение на вашем компьютере или на внешнем диске.</span><span class="sxs-lookup"><span data-stu-id="74adc-113">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="74adc-114">**Примечание**  Если вы загрузили компакт-диск, DVD-диск или USB-образ восстановления, вы можете открыть файлы на съемном носителе и скопировать файл Boot. wim из папки \\sources.</span><span class="sxs-lookup"><span data-stu-id="74adc-114">**Note** If you burned a CD, DVD, or USB of the recovery image, you can open the files on the removable media and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="74adc-115">При копировании файла Boot. wim вам не нужно подключать образ.</span><span class="sxs-lookup"><span data-stu-id="74adc-115">If you copy boot.wim file, you don’t need to mount the image.</span></span>

         

3.  <span data-ttu-id="74adc-116">С помощью файла Boot. wim Создайте загрузочный раздел для восстановления с помощью стандартного метода для создания собственного образа Windows RE.</span><span class="sxs-lookup"><span data-stu-id="74adc-116">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="74adc-117">Дополнительные сведения о том, как создать или настроить раздел восстановления, можно найти [в разделе Настройка среды Windows RE](https://go.microsoft.com/fwlink/?LinkId=214222).</span><span class="sxs-lookup"><span data-stu-id="74adc-117">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="74adc-118">Замените целевую секцию в образе Windows 8 на раздел восстановления.</span><span class="sxs-lookup"><span data-stu-id="74adc-118">Replace the target partition in your Windows 8 image with the recovery partition.</span></span>

    <span data-ttu-id="74adc-119">Дополнительные сведения о том, как развернуть решение для восстановления для повторной установки заводского образа в случае сбоя системы, можно найти в разделе [развертывание образа восстановления системы](https://go.microsoft.com/fwlink/?LinkId=214221).</span><span class="sxs-lookup"><span data-stu-id="74adc-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="74adc-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="74adc-120">Related topics</span></span>


[<span data-ttu-id="74adc-121">Создание образа для восстановления DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="74adc-121">Creating the DaRT 8.0 Recovery Image</span></span>](creating-the-dart-80-recovery-image-dart-8.md)

[<span data-ttu-id="74adc-122">Развертывание образа для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="74adc-122">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-8.md)

[<span data-ttu-id="74adc-123">Планирование для DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="74adc-123">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

 

 





