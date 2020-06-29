---
title: Развертывание образа для восстановления DaRT в качестве удаленного раздела
description: Развертывание образа для восстановления DaRT в качестве удаленного раздела
author: dansimp
ms.assetid: 06a5e250-b992-4f6a-ad74-e7715f9e96e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3cdb1313a64bacd652a5253c09f36fa792d0fa3c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813064"
---
# <span data-ttu-id="42576-103">Развертывание образа для восстановления DaRT в качестве удаленного раздела</span><span class="sxs-lookup"><span data-stu-id="42576-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="42576-104">После того как вы закончите работу мастера создания образа восстановления для Microsoft Diagnostics и восстановления (DaRT) 10 и создали образ восстановления, вы можете извлечь файл Boot. wim из файла образа ISO и развернуть его как удаленную секцию в сети.</span><span class="sxs-lookup"><span data-stu-id="42576-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="42576-105">Развертывание DaRT 10 как удаленной секции</span><span class="sxs-lookup"><span data-stu-id="42576-105">To deploy DaRT 10 as a remote partition</span></span>**

1.  <span data-ttu-id="42576-106">Извлеките файл Boot. wim из файла образа DaRT ISO.</span><span class="sxs-lookup"><span data-stu-id="42576-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="42576-107">Подключите файл образа ISO, созданный в диалоговом окне **Создание образа запуска** , с помощью предпочтительного способа подключения образа.</span><span class="sxs-lookup"><span data-stu-id="42576-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="42576-108">Откройте файл образа ISO и скопируйте файл Boot. wim из папки \\sources на подключенном образе в расположение на вашем компьютере или на внешнем диске.</span><span class="sxs-lookup"><span data-stu-id="42576-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="42576-109">**Примечание**  Если вы загрузили CD или DVD-диск в образ восстановления, вы можете открыть файлы на компакт-диске или DVD-диске и скопировать файл Boot. wim из папки \\sources.</span><span class="sxs-lookup"><span data-stu-id="42576-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="42576-110">Это позволяет пропустить необходимость монтировать образ.</span><span class="sxs-lookup"><span data-stu-id="42576-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="42576-111">Развертывание файла Boot. wim на сервере WDS, доступ к которому можно получить с компьютеров конечных пользователей на предприятии.</span><span class="sxs-lookup"><span data-stu-id="42576-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="42576-112">Настройте WDS-сервер для использования файла Boot. wim для DaRT, следуя стандартным процедурам развертывания WDS.</span><span class="sxs-lookup"><span data-stu-id="42576-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="42576-113">Дополнительные сведения о том, как развернуть DaRT как удаленную секцию, можно найти в разделе [Пошаговое руководство: развертывание образа с помощью PXE](https://go.microsoft.com/fwlink/?LinkId=212108) и [руководства по началу работы служб развертывания Windows](https://go.microsoft.com/fwlink/?LinkId=212106).</span><span class="sxs-lookup"><span data-stu-id="42576-113">For more information about how to deploy DaRT as a remote partition, see [Walkthrough: Deploy an Image by Using PXE](https://go.microsoft.com/fwlink/?LinkId=212108) and [Windows Deployment Services Getting Started Guide](https://go.microsoft.com/fwlink/?LinkId=212106).</span></span>

## <span data-ttu-id="42576-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="42576-114">Related topics</span></span>


[<span data-ttu-id="42576-115">Создание образа для восстановления DaRT 10</span><span class="sxs-lookup"><span data-stu-id="42576-115">Creating the DaRT 10 Recovery Image</span></span>](creating-the-dart-10-recovery-image.md)

[<span data-ttu-id="42576-116">Развертывание образа для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="42576-116">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-10.md)

[<span data-ttu-id="42576-117">Планирование для DaRT 10</span><span class="sxs-lookup"><span data-stu-id="42576-117">Planning for DaRT 10</span></span>](planning-for-dart-10.md)

 

 





