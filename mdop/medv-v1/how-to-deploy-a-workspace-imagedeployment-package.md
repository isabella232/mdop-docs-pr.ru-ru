---
title: Развертывание образа рабочей области
description: Развертывание образа рабочей области
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827012"
---
# <span data-ttu-id="d0928-103">Развертывание образа рабочей области</span><span class="sxs-lookup"><span data-stu-id="d0928-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="d0928-104">При использовании пакета развертывания новое изображение может быть развернуто на клиентских компьютерах одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="d0928-104">When using a deployment package, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="d0928-105">Загрузка из Интернета</span><span class="sxs-lookup"><span data-stu-id="d0928-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="d0928-106">Предварительное хранение образа</span><span class="sxs-lookup"><span data-stu-id="d0928-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [<span data-ttu-id="d0928-107">Развертывание образа в пакете развертывания</span><span class="sxs-lookup"><span data-stu-id="d0928-107">Deploying the image inside the deployment package</span></span>](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="d0928-108">Развертывание образа рабочей области через Интернет</span><span class="sxs-lookup"><span data-stu-id="d0928-108">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="d0928-109">Развертывание образа рабочей области через Интернет</span><span class="sxs-lookup"><span data-stu-id="d0928-109">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="d0928-110">Добавьте на сервер образ MED-V.</span><span class="sxs-lookup"><span data-stu-id="d0928-110">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="d0928-111">Сведения о загрузке изображения можно найти в разделе [Добавление изображения MED-V на сервер](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="d0928-111">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="d0928-112">Создайте пакет развертывания и включите путь сервера к расположению образа.</span><span class="sxs-lookup"><span data-stu-id="d0928-112">Create a deployment package, and include the server path to the location of the image.</span></span>

    <span data-ttu-id="d0928-113">Сведения о том, как создать пакет развертывания, приведены в разделе [Настройка пакета развертывания](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="d0928-113">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="d0928-114">Развертывание пакета для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d0928-114">Deploy the package to end users.</span></span>

    <span data-ttu-id="d0928-115">Сведения о развертывании пакета можно найти в разделе [Установка клиента MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="d0928-115">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="d0928-116">Клиент MED-V установлен и запускается в первый раз.</span><span class="sxs-lookup"><span data-stu-id="d0928-116">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="d0928-117">При первом запуске клиент загружает изображение с адреса сервера, указанного в клиентской установке.</span><span class="sxs-lookup"><span data-stu-id="d0928-117">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="d0928-118">Развертывание образа рабочей области с помощью предварительной версии образа</span><span class="sxs-lookup"><span data-stu-id="d0928-118">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="d0928-119">Развертывание образа рабочей области с помощью предварительной версии образа</span><span class="sxs-lookup"><span data-stu-id="d0928-119">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="d0928-120">Создайте папку, предваряя изображение, и отправьте ее в папку.</span><span class="sxs-lookup"><span data-stu-id="d0928-120">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="d0928-121">Дополнительные сведения о настройке предварительной версии образа можно найти [в разделе Настройка предварительного размещения изображений](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="d0928-121">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="d0928-122">Создайте пакет развертывания и добавьте путь к папке, которая должна быть предваряется для изображений.</span><span class="sxs-lookup"><span data-stu-id="d0928-122">Create a deployment package, and include the path to the image pre-stage folder.</span></span>

    <span data-ttu-id="d0928-123">Сведения о том, как создать пакет развертывания, приведены в разделе [Настройка пакета развертывания](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="d0928-123">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="d0928-124">Развертывание пакета для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d0928-124">Deploy the package to end users.</span></span>

    <span data-ttu-id="d0928-125">Сведения о развертывании пакета можно найти в разделе [Установка клиента MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="d0928-125">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="d0928-126">Клиент MED-V установлен и запускается в первый раз.</span><span class="sxs-lookup"><span data-stu-id="d0928-126">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="d0928-127">При первом запуске клиент извлекает изображение из папки, предшествующей этапу, указанной в клиентской установке.</span><span class="sxs-lookup"><span data-stu-id="d0928-127">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a><span data-ttu-id="d0928-128">Развертывание образа рабочей области с помощью пакета развертывания</span><span class="sxs-lookup"><span data-stu-id="d0928-128">How to Deploy a Workspace Image Using a Deployment Package</span></span>


**<span data-ttu-id="d0928-129">Развертывание образа рабочей области с помощью пакета развертывания</span><span class="sxs-lookup"><span data-stu-id="d0928-129">To deploy a workspace image using a deployment package</span></span>**

1.  <span data-ttu-id="d0928-130">Создайте пакет развертывания и включите изображение в пакет.</span><span class="sxs-lookup"><span data-stu-id="d0928-130">Create a deployment package, and include the image in the package.</span></span>

    <span data-ttu-id="d0928-131">Сведения о том, как создать пакет развертывания, приведены в разделе [Настройка пакета развертывания](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="d0928-131">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

2.  <span data-ttu-id="d0928-132">Развертывание пакета для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d0928-132">Deploy the package to end users.</span></span>

    <span data-ttu-id="d0928-133">Сведения о развертывании пакета можно найти в разделе [Установка клиента MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="d0928-133">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="d0928-134">Изображение будет импортировано на узел в процессе установки пакета.</span><span class="sxs-lookup"><span data-stu-id="d0928-134">The image is imported to the host as part of the package installation.</span></span>

## <span data-ttu-id="d0928-135">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d0928-135">Related topics</span></span>


[<span data-ttu-id="d0928-136">Настройка сервера веб-распространения образов</span><span class="sxs-lookup"><span data-stu-id="d0928-136">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

[<span data-ttu-id="d0928-137">Настройка пакета развертывания</span><span class="sxs-lookup"><span data-stu-id="d0928-137">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

 

 





