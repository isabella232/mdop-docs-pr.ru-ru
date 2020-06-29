---
title: Развертывание образа для восстановления DaRT 7.0
description: Развертывание образа для восстановления DaRT 7.0
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812656"
---
# <span data-ttu-id="ef049-103">Развертывание образа для восстановления DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="ef049-103">Deploying the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="ef049-104">После создания файла международной организации по стандартизации (ISO), содержащего образ восстановления для Microsoft Diagnostics и восстановления (DaRT) 7, вы можете развернуть на нем образ восстановления DaRT в рамках всей Организации, чтобы он был доступен для конечных пользователей и агентов поддержки.</span><span class="sxs-lookup"><span data-stu-id="ef049-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image, you can deploy the DaRT recovery image throughout your enterprise so that it is available to end users and helpdesk agents.</span></span> <span data-ttu-id="ef049-105">Существует четыре поддерживаемых способа развертывания изображения для восстановления с помощью DaRT.</span><span class="sxs-lookup"><span data-stu-id="ef049-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="ef049-106">Запись файла образа ISO на компакт-диск или DVD-диск</span><span class="sxs-lookup"><span data-stu-id="ef049-106">Burn the ISO image file to a CD or DVD</span></span>

-   <span data-ttu-id="ef049-107">Сохранение содержимого файла образа ISO на USB-накопителе (UFD)</span><span class="sxs-lookup"><span data-stu-id="ef049-107">Save the contents of the ISO image file to a USB Flash Drive (UFD)</span></span>

-   <span data-ttu-id="ef049-108">Извлеките файл Boot. wim из образа ISO и разверните его как удаленную секцию, доступную для компьютеров конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="ef049-108">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

-   <span data-ttu-id="ef049-109">Извлечение файла Boot. wim из образа ISO и развертывание в разделе восстановления новой копии Windows 7</span><span class="sxs-lookup"><span data-stu-id="ef049-109">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 7 installation</span></span>

<span data-ttu-id="ef049-110">**Важно!**  **Мастер переноса изображений** с помощью DaRT предлагает только возможность записи компакт-дисков и DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="ef049-110">**Important** The **DaRT Recovery Image Wizard** only provides the option to burn a CD or DVD.</span></span> <span data-ttu-id="ef049-111">Для всех других способов сохранения и развертывания образа восстановления требуется выполнить дополнительные действия, связанные с инструментами, которые не включены в DaRT.</span><span class="sxs-lookup"><span data-stu-id="ef049-111">All other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="ef049-112">В этом разделе приведены рекомендации и ссылки для других способов.</span><span class="sxs-lookup"><span data-stu-id="ef049-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="ef049-113">Развертывание изображения для восстановления DaRT с помощью USB-накопителя</span><span class="sxs-lookup"><span data-stu-id="ef049-113">Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="ef049-114">После того как вы закончите работу мастера переноса изображений с помощью DaRT, вы можете <https://go.microsoft.com/fwlink/?LinkId=218888> скопировать файл образа ISO на USB-накопитель (UFD).</span><span class="sxs-lookup"><span data-stu-id="ef049-114">After you have finished running the DaRT Recovery Image Wizard, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

[<span data-ttu-id="ef049-115">Развертывание образа для восстановления DaRT с помощью USB-устройства флэш-памяти</span><span class="sxs-lookup"><span data-stu-id="ef049-115">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## <span data-ttu-id="ef049-116">Развертывание образа восстановления DaRT как части раздела восстановления</span><span class="sxs-lookup"><span data-stu-id="ef049-116">Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="ef049-117">После завершения работы мастера изображений для восстановления DaRT и создания образа восстановления вы можете извлечь файл Boot. wim из файла образа ISO и развернуть его как раздел восстановления в образе Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ef049-117">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

[<span data-ttu-id="ef049-118">Развертывание образа для восстановления DaRT в качестве части раздела восстановления</span><span class="sxs-lookup"><span data-stu-id="ef049-118">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## <span data-ttu-id="ef049-119">Развертывание образа восстановления DaRT в виде удаленной секции</span><span class="sxs-lookup"><span data-stu-id="ef049-119">Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="ef049-120">После того как вы закончите работу мастера переноса изображений для восстановления с помощью DaRT и создали образ восстановления, вы можете извлечь файл Boot. wim из файла образа ISO и развернуть его как удаленную секцию в сети.</span><span class="sxs-lookup"><span data-stu-id="ef049-120">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

[<span data-ttu-id="ef049-121">Развертывание образа для восстановления DaRT в качестве удаленного раздела</span><span class="sxs-lookup"><span data-stu-id="ef049-121">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## <span data-ttu-id="ef049-122">Другие ресурсы для поддержки развертывания изображения для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="ef049-122">Other resources for maintaining Deploying the DaRT Recovery Image</span></span>


-   [<span data-ttu-id="ef049-123">Развертывание DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="ef049-123">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





