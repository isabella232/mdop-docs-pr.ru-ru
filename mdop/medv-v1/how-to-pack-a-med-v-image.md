---
title: Упаковка образа MED-V
description: Упаковка образа MED-V
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824679"
---
# <span data-ttu-id="4c905-103">Упаковка образа MED-V</span><span class="sxs-lookup"><span data-stu-id="4c905-103">How to Pack a MED-V Image</span></span>


<span data-ttu-id="4c905-104">Образ MED-V необходимо упаковать, прежде чем его можно будет добавить в пакет развертывания или отправить на сервер.</span><span class="sxs-lookup"><span data-stu-id="4c905-104">A MED-V image must be packed before it can be added to a deployment package or uploaded to the server.</span></span>

**<span data-ttu-id="4c905-105">Создание упакованного изображения MED-V</span><span class="sxs-lookup"><span data-stu-id="4c905-105">To create a packed MED-V image</span></span>**

1.  <span data-ttu-id="4c905-106">Нажмите кнопку Управление **изображениями** .</span><span class="sxs-lookup"><span data-stu-id="4c905-106">Click the **Images** management button.</span></span>

2.  <span data-ttu-id="4c905-107">В области **Images (изображения** в **локальных упакованных изображениях** ) нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="4c905-107">In the **Images** module, in the **Local Packed Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="4c905-108">В диалоговом окне **Создание упакованных изображений** выберите образ виртуальной машины, выполнив одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="4c905-108">In the **Packed Image Creation** dialog box, select the virtual machine image by doing one of the following:</span></span>

    -   <span data-ttu-id="4c905-109">В поле **базовый файл изображения** введите полный путь к каталогу, в котором находится образ Microsoft Virtual PC, подготовленный для MED-V.</span><span class="sxs-lookup"><span data-stu-id="4c905-109">In the **Base image file** field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="4c905-110">Нажмите кнопку **Обзор** , чтобы перейти к каталогу, в котором находится изображение Microsoft Virtual PC, подготовленное для MED-V.</span><span class="sxs-lookup"><span data-stu-id="4c905-110">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="4c905-111">Укажите имя нового изображения, выполнив одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="4c905-111">Specify the name of the new image by doing one of the following:</span></span>

    -   <span data-ttu-id="4c905-112">В поле **имя изображения** введите нужное имя.</span><span class="sxs-lookup"><span data-stu-id="4c905-112">In the **Image name** field, type the desired name.</span></span>

        **<span data-ttu-id="4c905-113">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4c905-113">Note</span></span>**  
        <span data-ttu-id="4c905-114">Следующие символы не могут быть включены в имя изображения: Space " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="4c905-114">The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. <span data-ttu-id="4c905-115">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4c905-115">Click **OK**.</span></span>

   <span data-ttu-id="4c905-116">На главном компьютере будет создано новое упакованное изображение MED-V со свойствами, определенными в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="4c905-116">A new MED-V packed image is created on your host computer with the properties defined in the following table.</span></span>

**<span data-ttu-id="4c905-117">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4c905-117">Note</span></span>**  
<span data-ttu-id="4c905-118">В **локальных упакованных изображениях** и **упакованных изображениях на** панелях сервера самая последняя версия каждого изображения отображается как родительский узел.</span><span class="sxs-lookup"><span data-stu-id="4c905-118">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="4c905-119">Щелкните родительский узел, чтобы просмотреть все существующие версии изображения.</span><span class="sxs-lookup"><span data-stu-id="4c905-119">Click the parent node to view all other existing versions of the image.</span></span>



**<span data-ttu-id="4c905-120">Свойства локальных упакованных изображений</span><span class="sxs-lookup"><span data-stu-id="4c905-120">Local Packed Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c905-121">Свойство</span><span class="sxs-lookup"><span data-stu-id="4c905-121">Property</span></span></th>
<th align="left"><span data-ttu-id="4c905-122">Описание</span><span class="sxs-lookup"><span data-stu-id="4c905-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4c905-123">Имя изображения</span><span class="sxs-lookup"><span data-stu-id="4c905-123">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c905-124">Имя упакованного изображения в том виде, в каком оно было определено при создании изображения администратором.</span><span class="sxs-lookup"><span data-stu-id="4c905-124">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4c905-125">Версия</span><span class="sxs-lookup"><span data-stu-id="4c905-125">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c905-126">Версия отображаемого изображения.</span><span class="sxs-lookup"><span data-stu-id="4c905-126">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4c905-127">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4c905-127">Note</span></span></strong><br/><p><span data-ttu-id="4c905-128">Все предыдущие версии сохраняются, если не удаляется.</span><span class="sxs-lookup"><span data-stu-id="4c905-128">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4c905-129">Размер файла (сжатый)</span><span class="sxs-lookup"><span data-stu-id="4c905-129">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c905-130">Физический размер изображения в сжатом виде.</span><span class="sxs-lookup"><span data-stu-id="4c905-130">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4c905-131">Размер изображения (без сжатия)</span><span class="sxs-lookup"><span data-stu-id="4c905-131">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c905-132">Физический размер изображения в несжатом виде.</span><span class="sxs-lookup"><span data-stu-id="4c905-132">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4c905-133">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4c905-133">Related topics</span></span>


[<span data-ttu-id="4c905-134">Установка клиента MED-V и консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="4c905-134">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="4c905-135">Использование пользовательского интерфейса консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="4c905-135">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="4c905-136">Создание образа Virtual PC для MED-V</span><span class="sxs-lookup"><span data-stu-id="4c905-136">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)









