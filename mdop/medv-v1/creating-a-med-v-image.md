---
title: Создание образа MED-V
description: Создание образа MED-V
author: dansimp
ms.assetid: 7cbbcd22-83f5-4b60-825f-781b4c6a2d36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de1c2cd87d85bbe2fc40b9007eba8f86d2ed6f60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812501"
---
# <span data-ttu-id="f5210-103">Создание образа MED-V</span><span class="sxs-lookup"><span data-stu-id="f5210-103">Creating a MED-V Image</span></span>


## <span data-ttu-id="f5210-104">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="f5210-104">In This Section</span></span>


<span data-ttu-id="f5210-105">В этом разделе рассказывается о том, как настроить образ MED-V на компьютере, на котором установлены клиент MED-V и приложение для управления MED-V, и описаны указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f5210-105">This section describes how to configure a MED-V image on a computer on which the MED-V client and MED-V management application are installed, and explains the following:</span></span>

<a href="" id="how-to-create-and-test-a-med-v-image"></a>[<span data-ttu-id="f5210-106">Создание и тестирование образа MED-V</span><span class="sxs-lookup"><span data-stu-id="f5210-106">How to Create and Test a MED-V Image</span></span>](how-to-create-and-test-a-med-v-image.md)  
<span data-ttu-id="f5210-107">В этой статье описано, как создать изображение в MED-V и протестировать его локально.</span><span class="sxs-lookup"><span data-stu-id="f5210-107">Describes how to create a MED-V image, and then test the image locally.</span></span>

<a href="" id="how-to-pack-a-med-v-image"></a>[<span data-ttu-id="f5210-108">Упаковка образа MED-V</span><span class="sxs-lookup"><span data-stu-id="f5210-108">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)  
<span data-ttu-id="f5210-109">В этой статье описано, как упаковать образ MED-V, чтобы его можно было добавить в пакет развертывания или отправить на сервер.</span><span class="sxs-lookup"><span data-stu-id="f5210-109">Describes how to pack a MED-V image so that it can be added to a deployment package or uploaded to the server.</span></span>

<a href="" id="how-to-upload-a-med-v-image-to-the-server"></a>[<span data-ttu-id="f5210-110">Отправка образа MED-V на сервер</span><span class="sxs-lookup"><span data-stu-id="f5210-110">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)  
<span data-ttu-id="f5210-111">В этой статье описано, как добавить на сервер образ MED-V.</span><span class="sxs-lookup"><span data-stu-id="f5210-111">Describes how to upload a MED-V image to the server.</span></span>

<a href="" id="how-to-localize-a-med-v-image"></a>[<span data-ttu-id="f5210-112">Локализация образа MED-V</span><span class="sxs-lookup"><span data-stu-id="f5210-112">How to Localize a MED-V Image</span></span>](how-to-localize-a-med-v-image.md)  
<span data-ttu-id="f5210-113">В этой статье описано, как локализовать изображение MED-V, выполнив извлечение или скачивание изображения.</span><span class="sxs-lookup"><span data-stu-id="f5210-113">Describes how to localize a MED-V image either through extracting or downloading the image.</span></span>

<a href="" id="how-to-update-a-med-v-image"></a>[<span data-ttu-id="f5210-114">Обновление образа MED-V</span><span class="sxs-lookup"><span data-stu-id="f5210-114">How to Update a MED-V Image</span></span>](how-to-update-a-med-v-image.md)  
<span data-ttu-id="f5210-115">В этой статье описано, как обновить изображение в MED-V, чтобы создать новую версию изображения.</span><span class="sxs-lookup"><span data-stu-id="f5210-115">Describes how to update a MED-V image to create a new version of the image.</span></span>

<a href="" id="how-to-delete-a-med-v-image"></a>[<span data-ttu-id="f5210-116">Удаление образа MED-V</span><span class="sxs-lookup"><span data-stu-id="f5210-116">How to Delete a MED-V Image</span></span>](how-to-delete-a-med-v-image.md)  
<span data-ttu-id="f5210-117">В этой статье описано, как удалить образ MED-V.</span><span class="sxs-lookup"><span data-stu-id="f5210-117">Describes how to delete a MED-V image.</span></span>

<span data-ttu-id="f5210-118">**Примечание**  После настройки изображения MED-V компьютер не должен входить в домен, так как в ходе настройки MED-V Workspace необходимо выполнить процедуру присоединения к домену на клиенте после развертывания.</span><span class="sxs-lookup"><span data-stu-id="f5210-118">**Note** After the MED-V image is configured, the computer should not be part of a domain because the join domain procedure should be performed on the client after the deployment, as part of the MED-V workspace setup.</span></span>

 

 

 





