---
title: Развертывание рабочей области MED-V с помощью корпоративной системы распространения программного обеспечения
description: Развертывание рабочей области MED-V с помощью корпоративной системы распространения программного обеспечения
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823629"
---
# <span data-ttu-id="293cd-103">Развертывание рабочей области MED-V с помощью корпоративной системы распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="293cd-103">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>


<span data-ttu-id="293cd-104">Клиент MED-V может распространяться с помощью корпоративной системы распространения программного обеспечения, например Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="293cd-104">MED-V client can be distributed using an enterprise software distribution system, such as Microsoft System Center Configuration Manager.</span></span>

<span data-ttu-id="293cd-105">**Примечание**  Если для установки MED-V используется Microsoft System Center Configuration Manager, при создании пакета для MED-V установите для режима выполнения права администратора.</span><span class="sxs-lookup"><span data-stu-id="293cd-105">**Note** If MED-V is installed by using Microsoft System Center Configuration Manager, when creating a package for MED-V, set the run mode to administrative rights.</span></span>

 

<span data-ttu-id="293cd-106">Перед развертыванием MED-V с помощью корпоративной системы распространения программного обеспечения убедитесь, что вы создали образ MED-V, готовый для развертывания.</span><span class="sxs-lookup"><span data-stu-id="293cd-106">Before deploying MED-V using an enterprise software distribution system, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="293cd-107">Дополнительные сведения о создании изображений в MED-V можно найти в разделе [Создание изображения med-v](creating-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="293cd-107">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="293cd-108">После подготовки изображения MED-V рассматривайте лучший способ распространения изображения в своей среде.</span><span class="sxs-lookup"><span data-stu-id="293cd-108">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="293cd-109">Изображение может распространяться одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="293cd-109">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="293cd-110">Загружается в Интернет и распространяется с помощью веб-загрузки, при желании используя технологию передачи усечения.</span><span class="sxs-lookup"><span data-stu-id="293cd-110">Uploaded to the Web and distributed via Web download, optionally utilizing Trim Transfer technology.</span></span>

-   <span data-ttu-id="293cd-111">Распределен с использованием предварительной версии образа.</span><span class="sxs-lookup"><span data-stu-id="293cd-111">Distributed using image pre-staging.</span></span>

## <span data-ttu-id="293cd-112">Развертывание изображения через Интернет</span><span class="sxs-lookup"><span data-stu-id="293cd-112">Deploying the Image via the Web</span></span>


<span data-ttu-id="293cd-113">Если вы развертываете изображение через Интернет, загрузите изображение MED-V на веб-сервер распространения изображений.</span><span class="sxs-lookup"><span data-stu-id="293cd-113">If you are deploying the image via the Web, upload the MED-V image to an image Web distribution server.</span></span> <span data-ttu-id="293cd-114">Сведения о настройке веб-сервера изображений можно найти в разделе [Настройка образа веб-сервера распространения](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="293cd-114">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="293cd-115">Сведения о том, как загрузить изображение на сервер, приведены в разделе [Добавление изображения MED-V на сервер](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="293cd-115">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

## <span data-ttu-id="293cd-116">Развертывание образа с помощью предварительной подготовки</span><span class="sxs-lookup"><span data-stu-id="293cd-116">Deploying the Image via Pre-staging</span></span>


<span data-ttu-id="293cd-117">Если вы развертываете изображение с помощью предварительной версии образа, Настройте папку для предварительного этапа и помещаете в нее изображение MED-V.</span><span class="sxs-lookup"><span data-stu-id="293cd-117">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="293cd-118">Дополнительные сведения о настройке предварительной версии образа можно найти в разделе [Настройка предварительной](how-to-configure-image-pre-staging.md)подготовки образа.</span><span class="sxs-lookup"><span data-stu-id="293cd-118">For more information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="293cd-119">**Примечание**  Если вы используете предварительную настройку образа, важно настроить папку предварительной подготовки для изображений, прежде чем перенаправить пакет Client. msi.</span><span class="sxs-lookup"><span data-stu-id="293cd-119">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to pushing the client .msi package.</span></span> <span data-ttu-id="293cd-120">Путь к папке должен быть включен в пакет Client. msi.</span><span class="sxs-lookup"><span data-stu-id="293cd-120">The folder path needs to be included in the client .msi package.</span></span>

 

<span data-ttu-id="293cd-121">И, наконец, отправьте пакет Client. msi с помощью корпоративного центра распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="293cd-121">Finally, push the client .msi package using your enterprise software distribution center.</span></span> <span data-ttu-id="293cd-122">После этого можно установить MED-V и развернутое изображение.</span><span class="sxs-lookup"><span data-stu-id="293cd-122">MED-V can then be installed and the image deployed.</span></span> <span data-ttu-id="293cd-123">Дополнительные сведения об установке клиента MED-V можно найти [в разделе Установка клиента med-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="293cd-123">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span> <span data-ttu-id="293cd-124">Дополнительные сведения о развертывании образа можно найти в разделе [развертывание образа рабочей области](how-to-deploy-a-workspace-imageesds.md).</span><span class="sxs-lookup"><span data-stu-id="293cd-124">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imageesds.md).</span></span>

 

 





