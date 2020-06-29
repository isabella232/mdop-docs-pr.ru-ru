---
title: Создание и тестирование образа MED-V
description: Создание и тестирование образа MED-V
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827042"
---
# <span data-ttu-id="57756-103">Создание и тестирование образа MED-V</span><span class="sxs-lookup"><span data-stu-id="57756-103">How to Create and Test a MED-V Image</span></span>


<span data-ttu-id="57756-104">Администратор MED-V создает образ MED-V таким образом, чтобы его можно было загрузить, связать с рабочей областью MED-V, а затем распространить на него через Интернет, добавить в пакет MED-V или загрузить на клиент с помощью сторонней системы.</span><span class="sxs-lookup"><span data-stu-id="57756-104">The MED-V administrator creates a MED-V image so that it can be uploaded, associated with a MED-V workspace, and then distributed to the client over the Web, added to a MED-V package, or downloaded to the client by using a third-party system.</span></span> <span data-ttu-id="57756-105">Рекомендуется сначала создать тестовый образ и протестировать его в клиенте MED-V перед развертыванием.</span><span class="sxs-lookup"><span data-stu-id="57756-105">It is recommended to first create a test image and test it on MED-V client before deploying it.</span></span>

<span data-ttu-id="57756-106">При создании изображения MED-V она переходит к следующим этапам.</span><span class="sxs-lookup"><span data-stu-id="57756-106">When creating a MED-V image, it goes through the following stages:</span></span>

1.  <span data-ttu-id="57756-107">**Локальное тестовое изображение**— это базовый образ, который можно протестировать локально.</span><span class="sxs-lookup"><span data-stu-id="57756-107">**Local test image**—A basic image that can be tested locally.</span></span>

2.  <span data-ttu-id="57756-108">**Локально упакованное изображение**— после того как изображение будет протестировано, оно будет упаковано так, как оно существовало перед тестированием.</span><span class="sxs-lookup"><span data-stu-id="57756-108">**Local packed image**—After the image is tested, the image is packed as it existed prior to testing.</span></span> <span data-ttu-id="57756-109">Изменения, внесенные во время тестирования, не включаются в упакованное изображение.</span><span class="sxs-lookup"><span data-stu-id="57756-109">No changes made during testing are included in the packed image.</span></span>

3.  <span data-ttu-id="57756-110">**Упакованное изображение на сервере**— упакованное изображение будет отправлено на сервер.</span><span class="sxs-lookup"><span data-stu-id="57756-110">**Packed image on server**—The packed image is uploaded to the server.</span></span>

## <span data-ttu-id="57756-111">Создание тестового изображения для MED-V</span><span class="sxs-lookup"><span data-stu-id="57756-111">How to Create a MED-V Test Image</span></span>


**<span data-ttu-id="57756-112">Создание нового тестового образа для MED-V</span><span class="sxs-lookup"><span data-stu-id="57756-112">To create a new MED-V test image</span></span>**

1.  <span data-ttu-id="57756-113">Нажмите кнопку Управление **изображениями** .</span><span class="sxs-lookup"><span data-stu-id="57756-113">Click the **Images** management button.</span></span>

    <span data-ttu-id="57756-114">Откроется модуль **изображения** .</span><span class="sxs-lookup"><span data-stu-id="57756-114">The **Images** module appears.</span></span>

    -   <span data-ttu-id="57756-115">Модуль **изображений** состоит из следующих областей:</span><span class="sxs-lookup"><span data-stu-id="57756-115">The **Images** module consists of the following panes:</span></span>

        -   <span data-ttu-id="57756-116">**Образы локальных тестов**— локальные распакованные изображения.</span><span class="sxs-lookup"><span data-stu-id="57756-116">**Local Test Images**—Local unpacked images.</span></span>

        -   <span data-ttu-id="57756-117">**Локальные Упакованные изображения**— все Упакованные изображения на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="57756-117">**Local Packed Images**—All packed images on the local computer.</span></span>

        -   <span data-ttu-id="57756-118">**Упакованные изображения на сервере**— все изображения, Упакованные и загруженные на сервер.</span><span class="sxs-lookup"><span data-stu-id="57756-118">**Packed Images on Server**—All images that have been packed and uploaded to the server.</span></span>

    -   <span data-ttu-id="57756-119">В **локальных упакованных изображениях** и **упакованных изображениях на** панелях сервера самая последняя версия каждого изображения отображается как родительский узел.</span><span class="sxs-lookup"><span data-stu-id="57756-119">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="57756-120">Щелкните родительский узел, чтобы просмотреть все существующие версии изображения.</span><span class="sxs-lookup"><span data-stu-id="57756-120">Click the parent node to view all other existing versions of the image.</span></span>

2.  <span data-ttu-id="57756-121">В области **образы локальных тестов** нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="57756-121">In the **Local Test Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="57756-122">В диалоговом окне **Создание тестового изображения** выберите образ виртуальной машины, который вы хотите настроить как тестовый образ MED-V, выполнив одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="57756-122">On the **Test Image Creation** dialog box, select the virtual machine image that you want to configure as a MED-V test image by doing one of the following:</span></span>

    -   <span data-ttu-id="57756-123">В поле **базовый файл изображения** введите полный путь к каталогу, в котором находится образ Microsoft Virtual PC, подготовленный для MED-V.</span><span class="sxs-lookup"><span data-stu-id="57756-123">In the **Base image** file field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="57756-124">Нажмите кнопку **Обзор** , чтобы перейти к каталогу, в котором находится изображение Microsoft Virtual PC, подготовленное для MED-V.</span><span class="sxs-lookup"><span data-stu-id="57756-124">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="57756-125">В поле **имя изображения** введите или выберите нужное имя.</span><span class="sxs-lookup"><span data-stu-id="57756-125">In the **Image name** field, type or select the desired name.</span></span>

    <span data-ttu-id="57756-126">**Примечание**  Следующие символы не могут быть включены в имя изображения: Space " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="57756-126">**Note** The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>

     

5.  <span data-ttu-id="57756-127">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="57756-127">Click **OK**.</span></span>

    <span data-ttu-id="57756-128">На главном компьютере будет создано новое тестовое изображение для MED-V со свойствами, определенными в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="57756-128">A new MED-V test image is created on your host computer with the properties defined in the following table.</span></span>

    <span data-ttu-id="57756-129">Дополнительные сведения о настройке образа рабочей области MED-V можно найти в разделе [Настройка политик рабочей области](configuring-med-v-workspace-policies.md)для MED-v.</span><span class="sxs-lookup"><span data-stu-id="57756-129">For more information about configuring the MED-V workspace image, refer to [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

**<span data-ttu-id="57756-130">Свойства локальных тестовых изображений</span><span class="sxs-lookup"><span data-stu-id="57756-130">Local Test Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="57756-131">Свойство</span><span class="sxs-lookup"><span data-stu-id="57756-131">Property</span></span></th>
<th align="left"><span data-ttu-id="57756-132">Описание</span><span class="sxs-lookup"><span data-stu-id="57756-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57756-133">Имя изображения</span><span class="sxs-lookup"><span data-stu-id="57756-133">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="57756-134">Имя тестового изображения, которое было определено при создании изображения администратором.</span><span class="sxs-lookup"><span data-stu-id="57756-134">The name of the test image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57756-135">Путь к изображению</span><span class="sxs-lookup"><span data-stu-id="57756-135">Image Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="57756-136">Локальный путь к тестовому изображению.</span><span class="sxs-lookup"><span data-stu-id="57756-136">The local path of the test image.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57756-137">Созданные</span><span class="sxs-lookup"><span data-stu-id="57756-137">Created</span></span></p></td>
<td align="left"><p><span data-ttu-id="57756-138">Дата создания тестового образа.</span><span class="sxs-lookup"><span data-stu-id="57756-138">The date the test image was created.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="57756-139">Проверка образа MED-V из клиента MED-V</span><span class="sxs-lookup"><span data-stu-id="57756-139">How to Test a MED-V Image from the MED-V Client</span></span>


<span data-ttu-id="57756-140">После создания тестового образа для MED-V выполните описанные ниже действия, чтобы протестировать изображение локально.</span><span class="sxs-lookup"><span data-stu-id="57756-140">After a MED-V test image is created, use the following procedure to test the image locally.</span></span>

**<span data-ttu-id="57756-141">Тестирование образа MED-V</span><span class="sxs-lookup"><span data-stu-id="57756-141">To test a MED-V image</span></span>**

1.  <span data-ttu-id="57756-142">Нажмите кнопку Управление **политиками** .</span><span class="sxs-lookup"><span data-stu-id="57756-142">Click the **Policy** management button.</span></span>

2.  <span data-ttu-id="57756-143">В модуле **политики** назначьте тестовое изображение для MED-v в рабочую область MED-v, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="57756-143">In the **Policy** module, assign the MED-V test image to a MED-V workspace by doing the following:</span></span>

    1.  <span data-ttu-id="57756-144">Откройте вкладку **Виртуальная машина** .</span><span class="sxs-lookup"><span data-stu-id="57756-144">Click the **Virtual Machine** tab.</span></span>

    2.  <span data-ttu-id="57756-145">В поле **назначенное изображение** выберите созданное тестовое изображение для MED-V.</span><span class="sxs-lookup"><span data-stu-id="57756-145">In the **Assigned Image** field, select the MED-V test image you created.</span></span> <span data-ttu-id="57756-146">Если тестового изображения нет в списке, нажмите кнопку **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="57756-146">If your test image is not in the list, click **Refresh**.</span></span>

    3.  <span data-ttu-id="57756-147">На панели инструментов нажмите кнопку **сохранить изменения**.</span><span class="sxs-lookup"><span data-stu-id="57756-147">On the toolbar, click **Save changes**.</span></span>

3.  <span data-ttu-id="57756-148">Настройте любые другие параметры рабочей области для MED-V, которые нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="57756-148">Configure any other MED-V workspace settings to be tested.</span></span> <span data-ttu-id="57756-149">Дополнительные сведения можно найти в разделе [Настройка политик рабочих областей для MED-V](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="57756-149">For more information, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

4.  <span data-ttu-id="57756-150">Запустите клиент MED-V.</span><span class="sxs-lookup"><span data-stu-id="57756-150">Start MED-V client.</span></span>

5.  <span data-ttu-id="57756-151">В диалоговом окне **подтверждение выполнения проверки** щелкните **использовать тестовое изображение**.</span><span class="sxs-lookup"><span data-stu-id="57756-151">In the **Confirm Running Test** confirmation box, click **Use Test Image**.</span></span>

6.  <span data-ttu-id="57756-152">Протестируйте тестовое изображение рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="57756-152">Test the MED-V workspace test image.</span></span>

    <span data-ttu-id="57756-153">Сведения о запуске и запуске клиента MED-V можно найти в разделе [операции клиента med-v](med-v-client-operations.md).</span><span class="sxs-lookup"><span data-stu-id="57756-153">For information about starting and running MED-V client, see [MED-V Client Operations](med-v-client-operations.md).</span></span>

<span data-ttu-id="57756-154">**Примечание**  При тестировании изображения не открывайте VPC и не вносите изменения в образ.</span><span class="sxs-lookup"><span data-stu-id="57756-154">**Note** While testing an image, do not open VPC and make changes to the image.</span></span>

 

<span data-ttu-id="57756-155">**Примечание**  При тестировании изображения никакие изменения не сохраняются в образе между сеансами. Вместо этого они сохраняются в отдельном временном файле.</span><span class="sxs-lookup"><span data-stu-id="57756-155">**Note** When testing an image, no changes are saved to the image between sessions; instead, they are saved in a separate, temporary file.</span></span> <span data-ttu-id="57756-156">Это необходимо для того, чтобы убедиться в том, что при упаковке и запуске изображения в производственной среде оно является исходным, чистым изображением.</span><span class="sxs-lookup"><span data-stu-id="57756-156">This is to ensure that when the image is packed and run on the production environment, it is the original, clean image.</span></span>

 

## <span data-ttu-id="57756-157">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="57756-157">Related topics</span></span>


[<span data-ttu-id="57756-158">Создание образа Virtual PC для MED-V</span><span class="sxs-lookup"><span data-stu-id="57756-158">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="57756-159">Создание рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="57756-159">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="57756-160">Настройка политик рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="57756-160">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="57756-161">Операции клиента MED-V</span><span class="sxs-lookup"><span data-stu-id="57756-161">MED-V Client Operations</span></span>](med-v-client-operations.md)

 

 





