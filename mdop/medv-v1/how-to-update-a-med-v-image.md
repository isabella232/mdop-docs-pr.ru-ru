---
title: Обновление образа MED-V
description: Обновление образа MED-V
author: dansimp
ms.assetid: 61eacf50-3a00-4bb8-b2f3-7350a6467fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f62cbd54d8593646460700a86ea48b5df4ce437
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812496"
---
# <span data-ttu-id="adb0b-103">Обновление образа MED-V</span><span class="sxs-lookup"><span data-stu-id="adb0b-103">How to Update a MED-V Image</span></span>


## <span data-ttu-id="adb0b-104">Обновление образа MED-V</span><span class="sxs-lookup"><span data-stu-id="adb0b-104">How to Update a MED-V Image</span></span>


<span data-ttu-id="adb0b-105">Существующий образ MED-V можно обновить, тем самым создав новую версию изображения.</span><span class="sxs-lookup"><span data-stu-id="adb0b-105">An existing MED-V image can be updated, thereby creating a new version of the image.</span></span> <span data-ttu-id="adb0b-106">После этого новая версия может быть развернута на клиентских компьютерах и заменена существующим образом.</span><span class="sxs-lookup"><span data-stu-id="adb0b-106">The new version can then be deployed on client computers, replacing the existing image.</span></span>

<span data-ttu-id="adb0b-107">**Примечание**  Если на клиенте развернута новая версия, она перезапишет существующий образ.</span><span class="sxs-lookup"><span data-stu-id="adb0b-107">**Note** When a new version is deployed on the client, it overwrites the existing image.</span></span> <span data-ttu-id="adb0b-108">При обновлении изображения убедитесь, что данные не нужно сохранять на клиенте.</span><span class="sxs-lookup"><span data-stu-id="adb0b-108">When updating an image, ensure that no data on the client needs to be saved.</span></span>

 

**<span data-ttu-id="adb0b-109">Обновление изображения MED-V</span><span class="sxs-lookup"><span data-stu-id="adb0b-109">To update a MED-V image</span></span>**

1.  <span data-ttu-id="adb0b-110">Откройте существующее изображение в Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="adb0b-110">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="adb0b-111">Внесите необходимые изменения в изображение, обновив изображение (например, установка нового программного обеспечения).</span><span class="sxs-lookup"><span data-stu-id="adb0b-111">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="adb0b-112">Закройте Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="adb0b-112">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="adb0b-113">Протестируйте изображение.</span><span class="sxs-lookup"><span data-stu-id="adb0b-113">Test the image.</span></span>

5.  <span data-ttu-id="adb0b-114">После того как вы проверите изображение, заупаковке его в локальный репозиторий, используя то же имя, что и у существующего образа.</span><span class="sxs-lookup"><span data-stu-id="adb0b-114">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="adb0b-115">**Примечание**  Если имя изображения отличается от имени существующей версии, будет создано новое изображение, а не новая версия существующего изображения.</span><span class="sxs-lookup"><span data-stu-id="adb0b-115">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="adb0b-116">Добавьте новую версию на сервер или распространите ее с помощью пакета развертывания.</span><span class="sxs-lookup"><span data-stu-id="adb0b-116">Upload the new version to the server or distribute it via a deployment package.</span></span>

## <span data-ttu-id="adb0b-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="adb0b-117">Related topics</span></span>


[<span data-ttu-id="adb0b-118">Создание образа Virtual PC для MED-V</span><span class="sxs-lookup"><span data-stu-id="adb0b-118">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="adb0b-119">Создание и тестирование образа MED-V</span><span class="sxs-lookup"><span data-stu-id="adb0b-119">How to Create and Test a MED-V Image</span></span>](how-to-create-and-test-a-med-v-image.md)

[<span data-ttu-id="adb0b-120">Упаковка образа MED-V</span><span class="sxs-lookup"><span data-stu-id="adb0b-120">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)

[<span data-ttu-id="adb0b-121">Отправка образа MED-V на сервер</span><span class="sxs-lookup"><span data-stu-id="adb0b-121">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="adb0b-122">Обновление образа рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="adb0b-122">Updating a MED-V Workspace Image</span></span>](updating-a-med-v-workspace-image.md)

 

 





