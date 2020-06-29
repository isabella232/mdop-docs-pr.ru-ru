---
title: Рекомендации по обеспечению безопасности для DaRT 10
description: Рекомендации по обеспечению безопасности для DaRT 10
author: dansimp
ms.assetid: c653daf1-f12a-4667-98cc-f0c89fa38e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f10ecf81021d41fbc08b288573c05a8d64c47d7c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823052"
---
# <span data-ttu-id="feb04-103">Рекомендации по обеспечению безопасности для DaRT 10</span><span class="sxs-lookup"><span data-stu-id="feb04-103">Security Considerations for DaRT 10</span></span>


<span data-ttu-id="feb04-104">В этой статье содержится краткий обзор учетных записей и групп, файлов журналов и других вопросов, связанных с безопасностью, для средств диагностики и восстановления Microsoft (DaRT) 10.</span><span class="sxs-lookup"><span data-stu-id="feb04-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span></span> <span data-ttu-id="feb04-105">Чтобы получить дополнительные сведения, воспользуйтесь ссылками, приведенными в этой статье.</span><span class="sxs-lookup"><span data-stu-id="feb04-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="feb04-106">Общие рекомендации по безопасности</span><span class="sxs-lookup"><span data-stu-id="feb04-106">General security considerations</span></span>


<span data-ttu-id="feb04-107">**Общие сведения о рисках для системы безопасности**.</span><span class="sxs-lookup"><span data-stu-id="feb04-107">**Understand the security risks**.</span></span> <span data-ttu-id="feb04-108">DaRT 10 включает функциональные возможности, позволяющие администратору или сотрудникам службы поддержки использовать инструменты DaRT удаленно для устранения неполадок на компьютере конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="feb04-108">DaRT 10 includes functionality that lets an administrator or a help desk worker run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="feb04-109">Кроме того, вы можете сохранить образ международной организации по стандартизации (ISO) на USB-накопителе или разместить его содержимое как раздел восстановления на жестком диске компьютера, чтобы добавить на него образ ISO в сети.</span><span class="sxs-lookup"><span data-stu-id="feb04-109">In addition, you can save the International Organization for Standardization (ISO) image to a USB flash drive or put the ISO image on a network to include its contents as a recovery partition on a computer’s hard disk.</span></span> <span data-ttu-id="feb04-110">Эти возможности обеспечивают гибкость, но также создают потенциальные риски безопасности, которые следует принимать во время настройки DaRT.</span><span class="sxs-lookup"><span data-stu-id="feb04-110">These capabilities provide flexibility, but also create potential security risks that you should consider when configuring DaRT.</span></span>

<span data-ttu-id="feb04-111">**Физическая защита компьютеров**.</span><span class="sxs-lookup"><span data-stu-id="feb04-111">**Physically secure your computers**.</span></span> <span data-ttu-id="feb04-112">Если администраторы и сотрудники службы поддержки не находятся на своем компьютере, они должны блокировать свои компьютеры и использовать защищенную экранную заставку.</span><span class="sxs-lookup"><span data-stu-id="feb04-112">When administrators and help desk workers are not physically at their computers, they should lock their computers and use a secured screen saver.</span></span>

<span data-ttu-id="feb04-113">**Установка последних обновлений для системы безопасности на всех компьютерах**.</span><span class="sxs-lookup"><span data-stu-id="feb04-113">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="feb04-114">Будьте в курсе новых обновлений для операционных систем, подписавшись на службу уведомлений системы безопасности ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="feb04-114">Stay informed about new updates for operating systems by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

## <span data-ttu-id="feb04-115">Ограничение доступа к средствам DaRT для конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="feb04-115">Limit end-user access to DaRT tools</span></span>


<span data-ttu-id="feb04-116">При создании изображения для восстановления DaRT вы можете выбрать инструменты, которые вы хотите включить.</span><span class="sxs-lookup"><span data-stu-id="feb04-116">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="feb04-117">По соображениям безопасности вы можете ограничить доступ конечных пользователей к более мощным средствам DaRT, таким как очистка диска и Locksmith.</span><span class="sxs-lookup"><span data-stu-id="feb04-117">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="feb04-118">В DaRT 10 вы можете отключить определенные инструменты во время настройки и по-прежнему сделать их доступными для сотрудников службы поддержки, когда конечный пользователь запускает функцию удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="feb04-118">In DaRT 10, you can disable certain tools during configuration and still make them available to help desk workers when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="feb04-119">Вы даже можете настроить изображение DaRT таким образом, чтобы параметр начала сеанса удаленного подключения был единственным средством, доступным для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="feb04-119">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="feb04-120">**Важно!**  После установки удаленного подключения все инструменты, которые вы включили в образ восстановления, в том числе те, которые недоступны для конечного пользователя, станут доступны любому сотруднику службы поддержки, работающему на компьютере конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="feb04-120">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to any help desk worker who is working on the end–user computer.</span></span>

 

<span data-ttu-id="feb04-121">Дополнительные сведения о том, как включить инструменты в образ восстановления DaRT, можно найти в статье [Обзор средств на DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="feb04-121">For more information about including tools in the DaRT recovery image, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

## <span data-ttu-id="feb04-122">Защита изображения для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="feb04-122">Secure the DaRT recovery image</span></span>


<span data-ttu-id="feb04-123">Если вы развертываете изображение для восстановления DaRT, сохранив его на USB-накопителе или создави удаленную секцию или раздел восстановления, вы можете добавить предпочтительный способ шифрования диска в ISO.</span><span class="sxs-lookup"><span data-stu-id="feb04-123">If you deploy the DaRT recovery image by saving it to a USB flash drive or by creating a remote partition or a recovery partition, you might want to include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="feb04-124">Шифрование ISO помогает гарантировать, что конечные пользователи не смогут использовать функцию DaRT, если они должны получить доступ к образу восстановления, и это гарантирует, что неавторизованные пользователи не смогут загрузить DaRT на компьютерах, входящих в состав другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="feb04-124">Encrypting the ISO helps to ensure that end users cannot use DaRT functionality if they were to gain access to the recovery image, and it ensures that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span> <span data-ttu-id="feb04-125">Если вы используете метод шифрования, не забудьте развернуть и включить его на всех компьютерах.</span><span class="sxs-lookup"><span data-stu-id="feb04-125">If you use an encryption method, be sure to deploy and enable it in all computers.</span></span>

<span data-ttu-id="feb04-126">**Примечание**  DaRT 10 поддерживает BitLocker на родном языке.</span><span class="sxs-lookup"><span data-stu-id="feb04-126">**Note** DaRT 10 supports BitLocker natively.</span></span>

 

<span data-ttu-id="feb04-127">Чтобы включить шифрование диска, добавьте файлы решения для шифрования при создании образа восстановления.</span><span class="sxs-lookup"><span data-stu-id="feb04-127">To include drive encryption, add the encryption solution files when you create the recovery image.</span></span> <span data-ttu-id="feb04-128">Ваше решение для шифрования должно быть способно работать в среде WinPE.</span><span class="sxs-lookup"><span data-stu-id="feb04-128">Your encryption solution must be able to run on WinPE.</span></span> <span data-ttu-id="feb04-129">Конечные пользователи, которые загружают из ISO, смогут получить доступ к этому решению шифрования и разблокировать диск.</span><span class="sxs-lookup"><span data-stu-id="feb04-129">End users who boot from the ISO are then able to access that encryption solution and unblock the drive.</span></span>

## <span data-ttu-id="feb04-130">Обеспечение безопасности двух компьютеров при использовании удаленного подключения</span><span class="sxs-lookup"><span data-stu-id="feb04-130">Maintain security between two computers when you use Remote Connection</span></span>


<span data-ttu-id="feb04-131">По умолчанию связь между двумя компьютерами, на которых установлен **Удаленный сеанс подключения** , может быть не зашифрована.</span><span class="sxs-lookup"><span data-stu-id="feb04-131">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="feb04-132">Таким образом, чтобы обеспечить безопасность двух компьютеров, рекомендуется, чтобы оба компьютера были частью одной сети.</span><span class="sxs-lookup"><span data-stu-id="feb04-132">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="feb04-133">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="feb04-133">Related topics</span></span>


[<span data-ttu-id="feb04-134">Безопасность и конфиденциальность в DaRT 10</span><span class="sxs-lookup"><span data-stu-id="feb04-134">Security and Privacy for DaRT 10</span></span>](security-and-privacy-for-dart-10.md)

 

 





