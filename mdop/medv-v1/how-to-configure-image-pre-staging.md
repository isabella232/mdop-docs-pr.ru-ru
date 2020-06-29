---
title: Настройка промежуточного размещения образа
description: Настройка промежуточного размещения образа
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826409"
---
# <span data-ttu-id="9415c-103">Настройка промежуточного размещения образа</span><span class="sxs-lookup"><span data-stu-id="9415c-103">How to Configure Image Pre-staging</span></span>


<span data-ttu-id="9415c-104">**Примечание**  Предварительный тест для образа полезен только для начальной загрузки изображения.</span><span class="sxs-lookup"><span data-stu-id="9415c-104">**Note** Image pre-staging is useful only for the initial image download.</span></span> <span data-ttu-id="9415c-105">Оно не поддерживается для обновления изображений.</span><span class="sxs-lookup"><span data-stu-id="9415c-105">It is not supported for image update.</span></span>

 

## <span data-ttu-id="9415c-106">Настройка промежуточного размещения образа</span><span class="sxs-lookup"><span data-stu-id="9415c-106">How to Configure Image Pre-staging</span></span>


**<span data-ttu-id="9415c-107">Настройка предварительного размещения изображений</span><span class="sxs-lookup"><span data-stu-id="9415c-107">To configure image pre-staging</span></span>**

1.  <span data-ttu-id="9415c-108">На клиентском компьютере в папке хранилища изображений создайте папку для предварительного промежуточного изображения и назовите его *Images MED-V*.</span><span class="sxs-lookup"><span data-stu-id="9415c-108">On the client computer, under the image store directory, create a folder for the pre-staging image, and name it *MED-V Images*.</span></span>

    <span data-ttu-id="9415c-109">**Примечание**  Эта папка должна называться *изображениями MED-V*.</span><span class="sxs-lookup"><span data-stu-id="9415c-109">**Note** This folder must be called *MED-V Images*.</span></span>

     

2.  <span data-ttu-id="9415c-110">В папке Images MED-V создайте вложенную папку и назовите ее *PrestagedImages*.</span><span class="sxs-lookup"><span data-stu-id="9415c-110">Inside the MED-V Images folder, create a subfolder and name it *PrestagedImages*.</span></span>

    <span data-ttu-id="9415c-111">**Примечание**  Эта папка должна называться *PrestagedImages*.</span><span class="sxs-lookup"><span data-stu-id="9415c-111">**Note** This folder must be called *PrestagedImages*.</span></span>

     

3.  <span data-ttu-id="9415c-112">Чтобы применить безопасность списков управления доступом (ACL) к папке *изображений MED-V* , установите следующий список ACL:</span><span class="sxs-lookup"><span data-stu-id="9415c-112">To apply Access Control Lists (ACL) security to the *MED-V Images* folder, set the following ACL:</span></span>

    **<span data-ttu-id="9415c-113">Пользователи NT AUTHORITY\\Authenticated: (OI) (CI) (Специальный доступ:)</span><span class="sxs-lookup"><span data-stu-id="9415c-113">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 <span data-ttu-id="9415c-114">ФАЙЛ \ _APPEND \ _DATA</span><span class="sxs-lookup"><span data-stu-id="9415c-114">FILE\_APPEND\_DATA</span></span>**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **<span data-ttu-id="9415c-115">NT AUTHORITY\\SYSTEM: (OI) F</span><span class="sxs-lookup"><span data-stu-id="9415c-115">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="9415c-116">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="9415c-116">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="9415c-117">**Примечание**  Рекомендуется применять безопасность ACL к папке *изображений MED-V* .</span><span class="sxs-lookup"><span data-stu-id="9415c-117">**Note** It is recommended to apply ACL security to the *MED-V Images* folder.</span></span>

     

4.  <span data-ttu-id="9415c-118">Чтобы применить безопасность ACL к папке *PrestagedImages* , установите следующий список ACL:</span><span class="sxs-lookup"><span data-stu-id="9415c-118">To apply ACL security to the *PrestagedImages* folder, set the following ACL:</span></span>

    **<span data-ttu-id="9415c-119">Пользователи NT AUTHORITY\\Authenticated: (OI) (CI) (Специальный доступ:)</span><span class="sxs-lookup"><span data-stu-id="9415c-119">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

    **<span data-ttu-id="9415c-120">ЧТЕНИЕ \ _CONTROL</span><span class="sxs-lookup"><span data-stu-id="9415c-120">READ\_CONTROL</span></span>**

    **<span data-ttu-id="9415c-121">СИНХРОНИЗАТОРОМ</span><span class="sxs-lookup"><span data-stu-id="9415c-121">SYNCHRONIZE</span></span>**

    **<span data-ttu-id="9415c-122">ФАЙЛ \ _GENERIC \ _READ</span><span class="sxs-lookup"><span data-stu-id="9415c-122">FILE\_GENERIC\_READ</span></span>**

    **<span data-ttu-id="9415c-123">ФАЙЛ \ _READ \ _DATA</span><span class="sxs-lookup"><span data-stu-id="9415c-123">FILE\_READ\_DATA</span></span>**

    **<span data-ttu-id="9415c-124">ФАЙЛ \ _READ \ _EA</span><span class="sxs-lookup"><span data-stu-id="9415c-124">FILE\_READ\_EA</span></span>**

    **<span data-ttu-id="9415c-125">ФАЙЛ \ _READ \ _ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="9415c-125">FILE\_READ\_ATTRIBUTES</span></span>**

    **<span data-ttu-id="9415c-126">NT AUTHORITY\\SYSTEM: (OI) F</span><span class="sxs-lookup"><span data-stu-id="9415c-126">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="9415c-127">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="9415c-127">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="9415c-128">**Примечание**  Рекомендуется применять безопасность ACL к папке *PrestagedImages* .</span><span class="sxs-lookup"><span data-stu-id="9415c-128">**Note** It is recommended to apply ACL security to the *PrestagedImages* folder.</span></span>

     

5.  <span data-ttu-id="9415c-129">Помещает файлы изображений (CKM и ИНДЕКСные файлы) в папку *PrestagedImages* .</span><span class="sxs-lookup"><span data-stu-id="9415c-129">Push the image files (CKM and INDEX files) to the *PrestagedImages* folder.</span></span>

    <span data-ttu-id="9415c-130">**Примечание**  После того как файлы изображений будут помещены в папку, предшествующую этапам, рекомендуется выполнить проверку целостности данных и помечать их как файлы только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9415c-130">**Note** After the image files have been pushed to the pre-stage folder, it is recommended to run a data integrity check and to mark the files as read-only.</span></span>

     

6.  <span data-ttu-id="9415c-131">Включите следующий параметр в установку клиента MED-V: *Client.MSI VMSFOLDER = "C:\\MED-V Images"*.</span><span class="sxs-lookup"><span data-stu-id="9415c-131">Include the following parameter in the MED-V client installation: *Client.MSI VMSFOLDER=”C:\\MED-V Images”*.</span></span>

## <span data-ttu-id="9415c-132">Как обновить расположение до этапа</span><span class="sxs-lookup"><span data-stu-id="9415c-132">How to Update the Pre-stage Location</span></span>


**<span data-ttu-id="9415c-133">Обновление расположения для предварительного этапа</span><span class="sxs-lookup"><span data-stu-id="9415c-133">To update the pre-stage location</span></span>**

1.  <span data-ttu-id="9415c-134">Раздел реестра *PrestagedImagesPath*указывает на расположение изображений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9415c-134">The registry key, *PrestagedImagesPath*, points to the default image location.</span></span> <span data-ttu-id="9415c-135">Она находится в следующей папке:</span><span class="sxs-lookup"><span data-stu-id="9415c-135">It is located in the following directory:</span></span>

    -   <span data-ttu-id="9415c-136">На платформе x86</span><span class="sxs-lookup"><span data-stu-id="9415c-136">On an x86 -</span></span> `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   <span data-ttu-id="9415c-137">На 64-разрядной версии</span><span class="sxs-lookup"><span data-stu-id="9415c-137">On an x64 -</span></span> `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  <span data-ttu-id="9415c-138">Если изображение находится в другом месте, измените путь.</span><span class="sxs-lookup"><span data-stu-id="9415c-138">If the image is in a different location, change the path.</span></span>

 

 





