---
title: Обновление образа рабочей области MED-V
description: Обновление образа рабочей области MED-V
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825852"
---
# <span data-ttu-id="5f6db-103">Обновление образа рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="5f6db-103">Updating a MED-V Workspace Image</span></span>


<span data-ttu-id="5f6db-104">Изображение можно обновить одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="5f6db-104">An image can be updated in one of the following ways:</span></span>

-   <span data-ttu-id="5f6db-105">Это обновление может быть отправлено в операционную систему на виртуальной машине с помощью корпоративной системы распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="5f6db-105">The update can be pushed to the guest operating system using your enterprise software distribution system.</span></span>

-   <span data-ttu-id="5f6db-106">Обновление можно загрузить на сервер распространения веб-сайта, а затем скачать его с помощью клиента и применить к образу MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f6db-106">The update can be uploaded to the image Web distribution server, and then downloaded by the client and applied to the MED-V image.</span></span>

-   <span data-ttu-id="5f6db-107">Базовый образ MED-V можно обновить и повторно развернуть.</span><span class="sxs-lookup"><span data-stu-id="5f6db-107">The MED-V base image can be updated and redeployed.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a><span data-ttu-id="5f6db-108">Как обновить образ MED-V с помощью корпоративной системы распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="5f6db-108">How to Update a MED-V Image Using an Enterprise Software Distribution System</span></span>


**<span data-ttu-id="5f6db-109">Обновление изображения MED-V с помощью корпоративной системы распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="5f6db-109">To update a MED-V image using an enterprise software distribution system</span></span>**

-   <span data-ttu-id="5f6db-110">Ознакомьтесь с документацией по используемой системе.</span><span class="sxs-lookup"><span data-stu-id="5f6db-110">Refer to the documentation of the system you are using.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a><span data-ttu-id="5f6db-111">Как обновить образ MED-V с помощью веб-сайта</span><span class="sxs-lookup"><span data-stu-id="5f6db-111">How to Update a MED-V Image Using Web Download</span></span>


**<span data-ttu-id="5f6db-112">Обновление изображения MED-V с помощью веб-загрузки</span><span class="sxs-lookup"><span data-stu-id="5f6db-112">To update a MED-V image using Web download</span></span>**

1.  <span data-ttu-id="5f6db-113">В управлении MED-V на вкладке **Виртуальная машина** убедитесь, что следующие параметры применяются к политикам рабочих областей med-v, связанным с обновляемым образом для MED-v.</span><span class="sxs-lookup"><span data-stu-id="5f6db-113">In MED-V management, on the **Virtual Machine** tab, ensure that the following settings are applied to the MED-V workspace policies that are associated with the MED-V image being updated:</span></span>

    -   <span data-ttu-id="5f6db-114">Установлен флажок **предлагать обновление при наличии новой версии** .</span><span class="sxs-lookup"><span data-stu-id="5f6db-114">The **Suggest update when a new version is available** check box is selected.</span></span>

    -   <span data-ttu-id="5f6db-115">Кроме того, если установлен флажок **загружать изображения для этой рабочей области, клиенты должны использовать функцию "обрезать перенос** ".</span><span class="sxs-lookup"><span data-stu-id="5f6db-115">Optionally, the **Clients should use Trim Transfer when downloading images for this Workspace** check box is selected.</span></span>

    <span data-ttu-id="5f6db-116">Дополнительные сведения можно найти [в разделе Применение параметров виртуальной машины к рабочей области MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="5f6db-116">For more information, see [How to Apply Virtual Machine Settings to a MED-V Workspace](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span></span>

2.  <span data-ttu-id="5f6db-117">Загрузите обновление образа на сервер распространения веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="5f6db-117">Upload the image update to the image Web distribution server.</span></span>

    <span data-ttu-id="5f6db-118">Все клиенты с изображениями, которые должны быть обновлены автоматически, загружают обновление и применяет его к образу.</span><span class="sxs-lookup"><span data-stu-id="5f6db-118">All clients with images that need to be updated automatically download the update and apply it to the image.</span></span>

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a><span data-ttu-id="5f6db-119">Обновление базового образа для MED-V</span><span class="sxs-lookup"><span data-stu-id="5f6db-119">How to Update a MED-V Base Image</span></span>


**<span data-ttu-id="5f6db-120">Обновление базового образа MED-V</span><span class="sxs-lookup"><span data-stu-id="5f6db-120">To update a MED-V base image</span></span>**

1.  <span data-ttu-id="5f6db-121">Откройте существующее изображение в Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="5f6db-121">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="5f6db-122">Внесите необходимые изменения в изображение, обновив изображение (например, установка нового программного обеспечения).</span><span class="sxs-lookup"><span data-stu-id="5f6db-122">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="5f6db-123">Закройте Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="5f6db-123">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="5f6db-124">Протестируйте изображение.</span><span class="sxs-lookup"><span data-stu-id="5f6db-124">Test the image.</span></span>

5.  <span data-ttu-id="5f6db-125">После того как вы проверите изображение, заупаковке его в локальный репозиторий, используя то же имя, что и у существующего образа.</span><span class="sxs-lookup"><span data-stu-id="5f6db-125">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="5f6db-126">**Примечание**  Если имя изображения отличается от имени существующей версии, будет создано новое изображение, а не новая версия существующего изображения.</span><span class="sxs-lookup"><span data-stu-id="5f6db-126">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="5f6db-127">Добавьте новую версию на сервер, перемещайте ее в папку с предварительным размещением изображений или распространите с помощью пакета развертывания.</span><span class="sxs-lookup"><span data-stu-id="5f6db-127">Upload the new version to the server, push it to the image pre-stage folder, or distribute it via a deployment package.</span></span>

## <span data-ttu-id="5f6db-128">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5f6db-128">Related topics</span></span>


[<span data-ttu-id="5f6db-129">Создание образа MED-V</span><span class="sxs-lookup"><span data-stu-id="5f6db-129">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="5f6db-130">Обновление образа MED-V</span><span class="sxs-lookup"><span data-stu-id="5f6db-130">How to Update a MED-V Image</span></span>](how-to-update-a-med-v-image.md)

[<span data-ttu-id="5f6db-131">Настройка политик рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="5f6db-131">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="5f6db-132">Настройка сервера веб-распространения образов</span><span class="sxs-lookup"><span data-stu-id="5f6db-132">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





