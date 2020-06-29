---
title: Рекомендации по обеспечению безопасности для DaRT 7.0
description: Рекомендации по обеспечению безопасности для DaRT 7.0
author: dansimp
ms.assetid: 52ad7e6c-c169-4ba4-aa76-56335a585eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739c0319195aeb26e38d55ffe01d14b623de7f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822732"
---
# <span data-ttu-id="91716-103">Рекомендации по обеспечению безопасности для DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="91716-103">Security Considerations for DaRT 7.0</span></span>


<span data-ttu-id="91716-104">Набор средств диагностики и восстановления Microsoft (DaRT) 7 включает в себя функциональные возможности, позволяющие администратору удаленно запускать инструменты DaRT для устранения неполадок на компьютере конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="91716-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes functionality that lets an administrator run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="91716-105">В более ранних выпусках DaRT специалист по технической поддержки или администратор должен физически находиться на компьютере конечного пользователя и загрузить DaRT с помощью компакт-диска или DVD-дисков, которые включают в себя образ для DaRT.</span><span class="sxs-lookup"><span data-stu-id="91716-105">In earlier releases of DaRT, a help desk technician or administrator had to physically be at an end-user computer and boot into DaRT by using the CD or DVD that included the DaRT recovery image.</span></span> <span data-ttu-id="91716-106">После этого специалист или администратор службы поддержки может выполнять одни и те же процедуры удаленно.</span><span class="sxs-lookup"><span data-stu-id="91716-106">Now, the help desk technician or administrator can perform the same procedures remotely.</span></span>

<span data-ttu-id="91716-107">Кроме того, в DaRT7 в дополнение к записи компакт-дисков или DVD-дисков вы можете сохранить образ международной организации по стандартизации (ISO) на USB-устройстве.</span><span class="sxs-lookup"><span data-stu-id="91716-107">Also in DaRT7, in addition to burning a CD or DVD, you are now able to save the International Organization for Standardization (ISO) image to a USB flash drive.</span></span> <span data-ttu-id="91716-108">Вы также можете разместить ISO-образ в сети или добавить его содержимое как раздел восстановления на жесткий диск компьютера.</span><span class="sxs-lookup"><span data-stu-id="91716-108">You can also put the ISO image on a network or include its contents as a recovery partition on a computer hard disk.</span></span>

<span data-ttu-id="91716-109">Функция **удаленного подключения** в DaRT7 позволяет конечным пользователям получить доступ к DART с помощью одного из этих новых методов развертывания.</span><span class="sxs-lookup"><span data-stu-id="91716-109">The **Remote Connection** feature in DaRT7 lets end users access DaRT by using one of these new deployment methods.</span></span> <span data-ttu-id="91716-110">Таким образом, они могут быстрее начать DaRT и получить доступ к средствам DaRT.</span><span class="sxs-lookup"><span data-stu-id="91716-110">Therefore, they can more easily start DaRT and access the DaRT tools.</span></span>

<span data-ttu-id="91716-111">Новые функции DaRT7 обеспечивают более гибкие возможности использования DaRT в Организации.</span><span class="sxs-lookup"><span data-stu-id="91716-111">The new functionalities in DaRT7 provide much more flexibility in how you use DaRT in your enterprise.</span></span> <span data-ttu-id="91716-112">Однако они также создают собственный набор проблем безопасности, которые необходимо решить.</span><span class="sxs-lookup"><span data-stu-id="91716-112">However, they also create their own set of security issues that must be addressed.</span></span> <span data-ttu-id="91716-113">При настройке DaRT рекомендуется ознакомиться с приведенными ниже советами по безопасности.</span><span class="sxs-lookup"><span data-stu-id="91716-113">We recommend that you consider the following security tips when you configure DaRT.</span></span>

## <span data-ttu-id="91716-114">Обеспечение безопасности при создании изображения для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="91716-114">To help maintain security when you create the DaRT recovery image</span></span>


<span data-ttu-id="91716-115">При создании изображения для восстановления DaRT вы можете выбрать инструменты, которые вы хотите включить.</span><span class="sxs-lookup"><span data-stu-id="91716-115">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="91716-116">По соображениям безопасности вы можете ограничить доступ конечных пользователей к более мощным средствам DaRT, таким как очистка диска и Locksmith.</span><span class="sxs-lookup"><span data-stu-id="91716-116">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="91716-117">В DaRT7 вы можете отключить определенные инструменты во время настройки и по-прежнему делать их доступными для агентов службы поддержки, когда пользователь запускает функцию удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="91716-117">In DaRT7, you can disable certain tools during configuration and still make them available to helpdesk agents when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="91716-118">Вы даже можете настроить изображение DaRT таким образом, чтобы параметр начала сеанса удаленного подключения был единственным средством, доступным для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="91716-118">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="91716-119">**Важно!**  После того как удаленное подключение установлено, все инструменты, которые вы включили в образ восстановления, в том числе те, которые недоступны для конечного пользователя, станут доступны агенту службы поддержки на компьютере конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="91716-119">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to the helpdesk agent working on the end–user computer.</span></span>

 

<span data-ttu-id="91716-120">Дополнительные сведения о том, как включить инструменты в образ восстановления DaRT, приведены в разделе [Использование мастера переноса изображений для DART для создания образа восстановления](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="91716-120">For more information about including tools in the DaRT recovery image, see [How to Use the DaRT Recovery Image Wizard to Create the Recovery Image](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="91716-121">Для обеспечения безопасности путем шифрования изображения для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="91716-121">To help maintain security by encrypting the DaRT recovery image</span></span>


<span data-ttu-id="91716-122">Если вы используете один из вариантов развертывания, описанных в DaRT7, например, сохранение на USB-накопитель или создание удаленной секции или раздела восстановления, вы можете включить предпочтительный способ шифрования диска в ISO.</span><span class="sxs-lookup"><span data-stu-id="91716-122">If you use one of the deployment options new in DaRT7, for example, saving to a USB flash drive or creating a remote partition or a recovery partition, you can include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="91716-123">Это поможет вам убедиться в том, что конечный пользователь не может использовать функцию DaRT, чтобы получить доступ к образу восстановления.</span><span class="sxs-lookup"><span data-stu-id="91716-123">This will help make sure that an end user cannot use the functionality of DaRT should they gain access to the recovery image.</span></span> <span data-ttu-id="91716-124">Кроме того, он также может гарантировать, что неавторизованные пользователи не смогут загрузить DaRT на компьютерах, входящих в состав другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="91716-124">And it will also make sure that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span>

<span data-ttu-id="91716-125">Метод шифрования должен быть развернут и включен на всех компьютерах.</span><span class="sxs-lookup"><span data-stu-id="91716-125">Your encryption method should be deployed and enabled in all computers.</span></span>

<span data-ttu-id="91716-126">**Примечание**  DaRT7 поддерживает BitLocker в собственном виде.</span><span class="sxs-lookup"><span data-stu-id="91716-126">**Note** DaRT7 supports BitLocker natively.</span></span>

 

## <span data-ttu-id="91716-127">Обеспечение безопасности между двумя компьютерами во время удаленного подключения</span><span class="sxs-lookup"><span data-stu-id="91716-127">To help maintain security between two computers during Remote Connection</span></span>


<span data-ttu-id="91716-128">По умолчанию связь между двумя компьютерами, на которых установлен **Удаленный сеанс подключения** , может быть не зашифрована.</span><span class="sxs-lookup"><span data-stu-id="91716-128">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="91716-129">Таким образом, чтобы обеспечить безопасность двух компьютеров, рекомендуется, чтобы оба компьютера были частью одной сети.</span><span class="sxs-lookup"><span data-stu-id="91716-129">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="91716-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="91716-130">Related topics</span></span>


[<span data-ttu-id="91716-131">Операции DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="91716-131">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





