---
title: Отправка образа MED-V на сервер
description: Отправка образа MED-V на сервер
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825702"
---
# <span data-ttu-id="1dfaf-103">Отправка образа MED-V на сервер</span><span class="sxs-lookup"><span data-stu-id="1dfaf-103">How to Upload a MED-V Image to the Server</span></span>


<span data-ttu-id="1dfaf-104">После тестирования образа MED-V его можно упаковывать, а затем отправлять на сервер.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-104">After a MED-V image has been tested, it can be packed and then uploaded to the server.</span></span> <span data-ttu-id="1dfaf-105">Сведения о настройке веб-сервера изображений можно найти в разделе [Настройка образа веб-сервера распространения](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="1dfaf-105">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span>

<span data-ttu-id="1dfaf-106">После того как изображение MED-V будет упаковано и загружено на сервер, оно может быть распределено между пользователями с помощью корпоративного центра распространения программного обеспечения или может быть загружено пользователями с помощью пакета развертывания.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-106">Once a MED-V image is packed and uploaded to the server, it can be distributed to users by using an enterprise software distribution center, or it can be downloaded by users using a deployment package.</span></span> <span data-ttu-id="1dfaf-107">Сведения о развертывании с помощью корпоративного центра распространения программного обеспечения можно найти в разделе [Развертывание рабочей области MED-V с помощью корпоративной системы распространения программного обеспечения](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="1dfaf-107">For information on deployment using an enterprise software distribution center, see [Deploying a MED-V Workspace Using an Enterprise Software Distribution System](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span></span> <span data-ttu-id="1dfaf-108">Сведения о развертывании с помощью пакета можно найти в разделе [Развертывание рабочей области MED-V с помощью пакета развертывания](deploying-a-med-v-workspace-using-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="1dfaf-108">For information on deployment using a package, see [Deploying a MED-V Workspace Using a Deployment Package](deploying-a-med-v-workspace-using-a-deployment-package.md).</span></span>

**<span data-ttu-id="1dfaf-109">Примечание.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-109">Note</span></span>**  
<span data-ttu-id="1dfaf-110">Перед отправкой изображения убедитесь в том, что веб-прокси не определен в параметрах браузера, и что служба Windows Update не работает в данный момент.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-110">Before uploading an image, verify that a Web proxy is not defined in your browser settings and that Windows Update is not currently running.</span></span>



**<span data-ttu-id="1dfaf-111">Отправка изображения MED-V на сервер</span><span class="sxs-lookup"><span data-stu-id="1dfaf-111">To upload a MED-V image to the server</span></span>**

1.  <span data-ttu-id="1dfaf-112">В области **локальные Упакованные изображения** выберите созданное изображение.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-112">In the **Local Packed Images** pane, select the image you created.</span></span>

2.  <span data-ttu-id="1dfaf-113">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-113">Click **Upload**.</span></span>

    <span data-ttu-id="1dfaf-114">Изображение будет отправлено на сервер.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-114">The image is uploaded to the server.</span></span> <span data-ttu-id="1dfaf-115">Это может занять значительно немного времени.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-115">This might take a considerable amount of time.</span></span>

    <span data-ttu-id="1dfaf-116">Изображения на сервере определяются с помощью свойств, перечисленных в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-116">Images on the server are defined with the properties listed in the following table.</span></span>

**<span data-ttu-id="1dfaf-117">Упакованные изображения в свойствах сервера</span><span class="sxs-lookup"><span data-stu-id="1dfaf-117">Packed Images on Server Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1dfaf-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="1dfaf-118">Property</span></span></th>
<th align="left"><span data-ttu-id="1dfaf-119">Описание</span><span class="sxs-lookup"><span data-stu-id="1dfaf-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dfaf-120">Имя изображения</span><span class="sxs-lookup"><span data-stu-id="1dfaf-120">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfaf-121">Имя упакованного изображения в том виде, в каком оно было определено при создании изображения администратором.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-121">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dfaf-122">Версия</span><span class="sxs-lookup"><span data-stu-id="1dfaf-122">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfaf-123">Версия отображаемого изображения.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-123">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1dfaf-124">Примечание.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-124">Note</span></span></strong><br/><p><span data-ttu-id="1dfaf-125">Все предыдущие версии сохраняются, если не удаляется.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-125">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dfaf-126">Размер файла (сжатый)</span><span class="sxs-lookup"><span data-stu-id="1dfaf-126">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfaf-127">Физический размер изображения в сжатом виде.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-127">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dfaf-128">Размер изображения (без сжатия)</span><span class="sxs-lookup"><span data-stu-id="1dfaf-128">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfaf-129">Физический размер изображения в несжатом виде.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-129">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="1dfaf-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1dfaf-130">Related topics</span></span>


[<span data-ttu-id="1dfaf-131">Установка клиента MED-V и консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="1dfaf-131">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="1dfaf-132">Использование пользовательского интерфейса консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="1dfaf-132">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="1dfaf-133">Создание образа Virtual PC для MED-V</span><span class="sxs-lookup"><span data-stu-id="1dfaf-133">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="1dfaf-134">Упаковка образа MED-V</span><span class="sxs-lookup"><span data-stu-id="1dfaf-134">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)









