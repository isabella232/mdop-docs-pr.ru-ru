---
title: Развертывание рабочей области MED-V с помощью пакета развертывания
description: Развертывание рабочей области MED-V с помощью пакета развертывания
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823632"
---
# <span data-ttu-id="f0f8e-103">Развертывание рабочей области MED-V с помощью пакета развертывания</span><span class="sxs-lookup"><span data-stu-id="f0f8e-103">Deploying a MED-V Workspace Using a Deployment Package</span></span>


<span data-ttu-id="f0f8e-104">Установка пакета развертывания предоставляет способ установки клиента MED-V вместе со всеми необходимыми предварительными требованиями, а также с параметрами, заданными администратором.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-104">The deployment package installation provides a method of installing MED-V client together with all its required prerequisites as well as any settings predefined by the administrator.</span></span>

<span data-ttu-id="f0f8e-105">При использовании пакета развертывания пакет распространяется через общую сеть или съемный носитель.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-105">When using a deployment package, the package is distributed via a shared network or removable media.</span></span> <span data-ttu-id="f0f8e-106">Изображение может быть включено в пакет или может распространяться отдельно.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-106">The image can be included in the package or can be distributed separately.</span></span>

<span data-ttu-id="f0f8e-107">Перед созданием пакета развертывания убедитесь, что вы создали образ MED-V, готовый к развертыванию.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-107">Before creating a deployment package, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="f0f8e-108">Дополнительные сведения о создании изображений в MED-V можно найти в разделе [Создание изображения med-v](creating-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="f0f8e-108">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="f0f8e-109">После подготовки изображения MED-V рассматривайте лучший способ распространения изображения в своей среде.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-109">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="f0f8e-110">Изображение может распространяться одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-110">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="f0f8e-111">Загружается в Интернет и распространяется с помощью веб-загрузки, при необходимости с использованием технологии передачи обрезки.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-111">Uploaded to the Web and distributed via Web download, optionally using Trim Transfer technology.</span></span>

-   <span data-ttu-id="f0f8e-112">Распределен с использованием предварительной версии образа.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-112">Distributed using image pre-staging.</span></span>

-   <span data-ttu-id="f0f8e-113">Входит в состав пакета развертывания и распространяется вместе со всеми другими компонентами MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-113">Included in the deployment package and distributed together with all the other MED-V components.</span></span>

<span data-ttu-id="f0f8e-114">Если изображение будет включено в пакет, для него не требуется никаких других конфигураций.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-114">If the image will be included in the package, no other configurations are necessary for the image.</span></span> <span data-ttu-id="f0f8e-115">Если изображение не будет включено в пакет развертывания, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-115">If the image will not be included in the deployment package, do one of the following:</span></span>

-   <span data-ttu-id="f0f8e-116">Если вы развертываете изображение через Интернет, загрузите изображение MED-V на веб-сервер распространения изображений.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-116">If you are deploying the image via the Web, upload the MED-V image to the image Web distribution server.</span></span> <span data-ttu-id="f0f8e-117">Сведения о настройке веб-сервера изображений можно найти в разделе [Настройка образа веб-сервера распространения](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="f0f8e-117">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="f0f8e-118">Сведения о том, как загрузить изображение на сервер, приведены в разделе [Добавление изображения MED-V на сервер](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="f0f8e-118">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

-   <span data-ttu-id="f0f8e-119">Если вы развертываете изображение с помощью предварительной версии образа, Настройте папку для предварительного этапа и помещаете в нее изображение MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-119">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="f0f8e-120">Дополнительные сведения о настройке предварительной версии образа можно найти [в разделе Настройка предварительной подготовки образа](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="f0f8e-120">For more information on configuring the image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="f0f8e-121">**Примечание**  Если вы используете предварительную настройку образа, важно настроить папку перед созданием пакета развертывания.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-121">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to creating the deployment package.</span></span> <span data-ttu-id="f0f8e-122">Путь к папке должен быть включен в пакет развертывания.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-122">The folder path needs to be included in the deployment package.</span></span>

 

<span data-ttu-id="f0f8e-123">Наконец, создайте пакет развертывания.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-123">Finally, create the deployment package.</span></span> <span data-ttu-id="f0f8e-124">Дополнительные сведения о создании пакета развертывания можно найти в разделе [Настройка пакета развертывания](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="f0f8e-124">For more information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span> <span data-ttu-id="f0f8e-125">После завершения пакета распространите его на развертывание.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-125">After the package is complete, distribute it for deployment.</span></span>

<span data-ttu-id="f0f8e-126">После распространения пакета развертывания клиент MED-V может быть установлен, а его изображение развернуто.</span><span class="sxs-lookup"><span data-stu-id="f0f8e-126">After the deployment package is distributed, MED-V client can be installed and the image deployed.</span></span> <span data-ttu-id="f0f8e-127">Дополнительные сведения об установке клиента MED-V можно найти [в разделе Установка клиента med-v](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="f0f8e-127">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span> <span data-ttu-id="f0f8e-128">Дополнительные сведения о развертывании образа можно найти в разделе [развертывание образа рабочей области](how-to-deploy-a-workspace-imagedeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="f0f8e-128">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imagedeployment-package.md).</span></span>

 

 





