---
title: Развертывание образа для восстановления DaRT
description: Развертывание образа для восстановления DaRT
author: dansimp
ms.assetid: df5cb54a-be8c-4ed2-89ea-d3c67c2ef4d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e445873324f005455ba3c96319847dea8ba761ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824112"
---
# <span data-ttu-id="53d71-103">Развертывание образа для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="53d71-103">Deploying the DaRT Recovery Image</span></span>


<span data-ttu-id="53d71-104">После создания файла международной организации по стандартизации (ISO), содержащего образ восстановления для Microsoft Diagnostics и Recovery (DaRT) 8,0, вы можете развернуть на нем образ восстановления DaRT 8,0 в рамках своей организации, чтобы он был доступен для конечных пользователей и сотрудников службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="53d71-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image, you can deploy the DaRT 8.0 recovery image throughout your enterprise so that it is available to end users and help desk workers.</span></span> <span data-ttu-id="53d71-105">Существует четыре поддерживаемых способа развертывания изображения для восстановления с помощью DaRT.</span><span class="sxs-lookup"><span data-stu-id="53d71-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span> <span data-ttu-id="53d71-106">Чтобы узнать о преимуществах и недостатках каждого способа, ознакомьтесь со сведениями [о том, как сохранить и развернуть изображение для восстановления DaRT 8,0](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="53d71-106">To review the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 8.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="53d71-107">Запись файла образа ISO на компакт-диск или DVD-диск с помощью мастера создания изображений для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="53d71-107">Burn the ISO image file to a CD or DVD by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="53d71-108">Сохранение содержимого файла образа ISO на USB-накопителе (UFD) с помощью мастера создания образа для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="53d71-108">Save the contents of the ISO image file to a USB Flash Drive (UFD) by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="53d71-109">Извлеките файл Boot. wim из образа ISO и разверните его как удаленную секцию, доступную для компьютеров конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="53d71-109">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

<span data-ttu-id="53d71-110">Извлеките файл Boot. wim из образа ISO и разверните раздел восстановления для новой копии Windows 8.</span><span class="sxs-lookup"><span data-stu-id="53d71-110">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 8 installation</span></span>

<span data-ttu-id="53d71-111">**Важно!**  С помощью **мастера изображений для восстановления DaRT** можно записать изображение на компакт-диск, DVD-диск или UFD, но для других способов сохранения и развертывания образа восстановления требуется выполнить дополнительные действия, которые включают в себя средства, не включенные в DART.</span><span class="sxs-lookup"><span data-stu-id="53d71-111">**Important** The **DaRT Recovery Image Wizard** provides the option to burn the image to a CD, DVD or UFD, but the other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="53d71-112">В этом разделе приведены рекомендации и ссылки для других способов.</span><span class="sxs-lookup"><span data-stu-id="53d71-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="53d71-113">Развертывание образа восстановления DaRT как части раздела восстановления</span><span class="sxs-lookup"><span data-stu-id="53d71-113">Deploy the DaRT recovery image as part of a recovery partition</span></span>


<span data-ttu-id="53d71-114">После завершения работы мастера изображений для восстановления DaRT и создания образа восстановления вы можете извлечь файл Boot. wim из файла образа ISO и развернуть его как раздел восстановления в образе Windows 8.</span><span class="sxs-lookup"><span data-stu-id="53d71-114">After you have finished running the DaRT Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 8 image.</span></span>

[<span data-ttu-id="53d71-115">Развертывание образа для восстановления DaRT в качестве части раздела восстановления</span><span class="sxs-lookup"><span data-stu-id="53d71-115">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-8.md)

## <span data-ttu-id="53d71-116">Развертывание образа восстановления DaRT в виде удаленной секции</span><span class="sxs-lookup"><span data-stu-id="53d71-116">Deploy the DaRT recovery image as a remote partition</span></span>


<span data-ttu-id="53d71-117">Вы можете разместить образ восстановления на центральном сетевом сервере, например в службах развертывания Windows, и позволить пользователям или сотрудникам отдела обслуживания передавать изображение на компьютеры по требованию.</span><span class="sxs-lookup"><span data-stu-id="53d71-117">You can host the recovery image on a central network boot server, such as Windows Deployment Services, and allow users or support staff to stream the image to computers on demand.</span></span>

[<span data-ttu-id="53d71-118">Развертывание образа для восстановления DaRT в качестве удаленного раздела</span><span class="sxs-lookup"><span data-stu-id="53d71-118">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-8.md)

## <span data-ttu-id="53d71-119">Другие ресурсы по развертыванию изображения для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="53d71-119">Other resources for deploying the DaRT recovery image</span></span>


[<span data-ttu-id="53d71-120">Развертывание DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="53d71-120">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 





