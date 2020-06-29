---
title: Развертывание образа для восстановления DaRT в качестве удаленного раздела
description: Развертывание образа для восстановления DaRT в качестве удаленного раздела
author: dansimp
ms.assetid: 757c9340-8eac-42e8-85de-4302e436713a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a3acdbf72a2c6dac0238f868c7280f1c389b1311
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823569"
---
# <span data-ttu-id="2bc3a-103">Развертывание образа для восстановления DaRT в качестве удаленного раздела</span><span class="sxs-lookup"><span data-stu-id="2bc3a-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="2bc3a-104">После того как вы закончите работу мастера переноса изображений для восстановления с помощью DaRT и создали образ восстановления, вы можете извлечь файл Boot. wim из файла образа ISO и развернуть его как удаленную секцию в сети.</span><span class="sxs-lookup"><span data-stu-id="2bc3a-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="2bc3a-105">Развертывание DaRT как удаленной секции</span><span class="sxs-lookup"><span data-stu-id="2bc3a-105">To deploy DaRT as a remote partition</span></span>**

1.  <span data-ttu-id="2bc3a-106">Извлеките файл Boot. wim из файла образа DaRT ISO.</span><span class="sxs-lookup"><span data-stu-id="2bc3a-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="2bc3a-107">Подключите файл образа ISO, созданный в диалоговом окне **Создание образа запуска** , с помощью предпочтительного способа подключения образа.</span><span class="sxs-lookup"><span data-stu-id="2bc3a-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="2bc3a-108">Откройте файл образа ISO и скопируйте файл Boot. wim из папки \\sources на подключенном образе в расположение на вашем компьютере или на внешнем диске.</span><span class="sxs-lookup"><span data-stu-id="2bc3a-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="2bc3a-109">**Примечание**  Если вы загрузили CD или DVD-диск в образ восстановления, вы можете открыть файлы на компакт-диске или DVD-диске и скопировать файл Boot. wim из папки \\sources.</span><span class="sxs-lookup"><span data-stu-id="2bc3a-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="2bc3a-110">Это позволяет пропустить необходимость монтировать образ.</span><span class="sxs-lookup"><span data-stu-id="2bc3a-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="2bc3a-111">Развертывание файла Boot. wim на сервере WDS, доступ к которому можно получить с компьютеров конечных пользователей на предприятии.</span><span class="sxs-lookup"><span data-stu-id="2bc3a-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="2bc3a-112">Настройте WDS-сервер для использования файла Boot. wim для DaRT, следуя стандартным процедурам развертывания WDS.</span><span class="sxs-lookup"><span data-stu-id="2bc3a-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="2bc3a-113">Дополнительные сведения о том, как развернуть DaRT как удаленную секцию, можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="2bc3a-113">For more information about how to deploy DaRT as a remote partition, see the following:</span></span>

-   [<span data-ttu-id="2bc3a-114">Пошаговое руководство: развертывание образа с помощью протокола PXE</span><span class="sxs-lookup"><span data-stu-id="2bc3a-114">Walkthrough: Deploy an Image by Using PXE</span></span>](https://go.microsoft.com/fwlink/?LinkId=212108)

-   [<span data-ttu-id="2bc3a-115">Руководство по началу работы со службами развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="2bc3a-115">Windows Deployment Services Getting Started Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=212106)

## <span data-ttu-id="2bc3a-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2bc3a-116">Related topics</span></span>


[<span data-ttu-id="2bc3a-117">Развертывание образа для восстановления DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="2bc3a-117">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





