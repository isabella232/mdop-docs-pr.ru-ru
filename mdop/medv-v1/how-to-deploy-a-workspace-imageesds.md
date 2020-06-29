---
title: Развертывание образа рабочей области
description: Развертывание образа рабочей области
author: dansimp
ms.assetid: ccc8e89b-1625-4b58-837e-4c6d93d46070
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4cb16b0a4c278d135fdc9b737aa7a6e9b46115e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827002"
---
# <span data-ttu-id="242c3-103">Развертывание образа рабочей области</span><span class="sxs-lookup"><span data-stu-id="242c3-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="242c3-104">Если вы используете корпоративную систему распространения программного обеспечения, вы можете развернуть на клиентских компьютерах новое изображение одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="242c3-104">When using an enterprise software distribution system, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="242c3-105">Загрузка из Интернета</span><span class="sxs-lookup"><span data-stu-id="242c3-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="242c3-106">Предварительное хранение образа</span><span class="sxs-lookup"><span data-stu-id="242c3-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="242c3-107">Развертывание образа рабочей области через Интернет</span><span class="sxs-lookup"><span data-stu-id="242c3-107">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="242c3-108">Развертывание образа рабочей области через Интернет</span><span class="sxs-lookup"><span data-stu-id="242c3-108">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="242c3-109">Добавьте на сервер образ MED-V.</span><span class="sxs-lookup"><span data-stu-id="242c3-109">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="242c3-110">Сведения о загрузке изображения можно найти в разделе [Добавление изображения MED-V на сервер](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="242c3-110">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="242c3-111">С помощью корпоративной системы распространения программного обеспечения установите на компьютеры пользователей пакет Client. msi для MED-V.</span><span class="sxs-lookup"><span data-stu-id="242c3-111">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="242c3-112">Сведения об установке пакета Client. msi для MED-V можно найти в разделе [Установка клиента med-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="242c3-112">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="242c3-113">Клиент MED-V установлен и запускается в первый раз.</span><span class="sxs-lookup"><span data-stu-id="242c3-113">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="242c3-114">При первом запуске клиент загружает изображение с адреса сервера, указанного в клиентской установке.</span><span class="sxs-lookup"><span data-stu-id="242c3-114">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="242c3-115">Развертывание образа рабочей области с помощью предварительной версии образа</span><span class="sxs-lookup"><span data-stu-id="242c3-115">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="242c3-116">Развертывание образа рабочей области с помощью предварительной версии образа</span><span class="sxs-lookup"><span data-stu-id="242c3-116">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="242c3-117">Создайте папку, предваряя изображение, и отправьте ее в папку.</span><span class="sxs-lookup"><span data-stu-id="242c3-117">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="242c3-118">Дополнительные сведения о настройке предварительной версии образа можно найти [в разделе Настройка предварительного размещения изображений](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="242c3-118">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="242c3-119">С помощью корпоративной системы распространения программного обеспечения установите на компьютеры пользователей пакет Client. msi для MED-V.</span><span class="sxs-lookup"><span data-stu-id="242c3-119">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="242c3-120">Сведения об установке пакета Client. msi для MED-V можно найти в разделе [Установка клиента med-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="242c3-120">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="242c3-121">Клиент MED-V установлен и запускается в первый раз.</span><span class="sxs-lookup"><span data-stu-id="242c3-121">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="242c3-122">При первом запуске клиент извлекает изображение из папки, предшествующей этапу, указанной в клиентской установке.</span><span class="sxs-lookup"><span data-stu-id="242c3-122">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <span data-ttu-id="242c3-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="242c3-123">Related topics</span></span>


[<span data-ttu-id="242c3-124">Настройка сервера веб-распространения образов</span><span class="sxs-lookup"><span data-stu-id="242c3-124">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





