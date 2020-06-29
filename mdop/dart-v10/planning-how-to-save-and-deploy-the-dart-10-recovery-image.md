---
title: Планирование способов сохранения и развертывания образа для восстановления DaRT 10
description: Планирование способов сохранения и развертывания образа для восстановления DaRT 10
author: dansimp
ms.assetid: 9a3e5413-2621-49ce-8bd2-992616691703
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbaa8c4160970de90561f5ff8cedcefd08ca1dd7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822989"
---
# <span data-ttu-id="c0dc9-103">Планирование способов сохранения и развертывания образа для восстановления DaRT 10</span><span class="sxs-lookup"><span data-stu-id="c0dc9-103">Planning How to Save and Deploy the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="c0dc9-104">Вы можете сохранить и развернуть образ восстановления с помощью набора средств диагностики и восстановления (Майкрософт) (DaRT), выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-104">You can save and deploy the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image by using the following methods.</span></span> <span data-ttu-id="c0dc9-105">Определив метод, который будет использоваться, продумайте преимущества и недостатки каждого из них.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-105">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="c0dc9-106">Кроме того, следует предусмотреть инфраструктуру и сотрудников службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-106">You should also consider your infrastructure and support staff.</span></span> <span data-ttu-id="c0dc9-107">Если у вас небольшая инфраструктура, вам может потребоваться развернуть DaRT 10 с помощью съемных носителей, так как образ восстановления всегда будет доступен, если он установлен на локальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-107">If you have a small infrastructure, you might want to deploy DaRT 10 by using removable media, since the recovery image will always be available if you install it to the local hard drive.</span></span>

<span data-ttu-id="c0dc9-108">Если в вашей организации используются доменные службы Active Directory (AD DS), вам может потребоваться развернуть образы восстановления как сетевую службу с помощью Windows DS.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-108">If your organization uses Active Directory Domain Services (AD DS), you may want to deploy recovery images as a network service by using Windows DS.</span></span> <span data-ttu-id="c0dc9-109">Образы восстановления всегда доступны любому подключенному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-109">Recovery images are always available to any connected computer.</span></span> <span data-ttu-id="c0dc9-110">Вы можете развернуть несколько изображений из Windows DS и поддерживать их все в одном приложении.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-110">You can deploy multiple images from Windows DS and maintain them all in one place.</span></span>

<span data-ttu-id="c0dc9-111">**Примечание**  Возможно, вы захотите использовать в Организации более одного способа.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-111">**Note** You may want to use more than one method in your organization.</span></span> <span data-ttu-id="c0dc9-112">Например, вы можете загрузить DaRT из удаленной секции для большинства ситуаций и получить доступ к флэш-накопителю USB на случай, если компьютер пользователя не может подключиться к сети.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-112">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="c0dc9-113">В таблице ниже приведены некоторые преимущества и недостатки использования DaRT в Организации.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-113">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0dc9-114">Метод загрузки для DaRT</span><span class="sxs-lookup"><span data-stu-id="c0dc9-114">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="c0dc9-115">Преимущества</span><span class="sxs-lookup"><span data-stu-id="c0dc9-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="c0dc9-116">Недостатки</span><span class="sxs-lookup"><span data-stu-id="c0dc9-116">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c0dc9-117">Съемные носители</span><span class="sxs-lookup"><span data-stu-id="c0dc9-117">Removable Media</span></span></strong></p>
<p><span data-ttu-id="c0dc9-118">Образ восстановления записывается на CD, DVD или USB-накопитель, чтобы предоставить сотрудникам службы поддержки средства восстановления для компьютера нестабильной работы.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-118">The recovery image is written to a CD, DVD, or USB drive to enable support staff to take the recovery tools with them to the unstable computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0dc9-119">Поддерживает сценарии, в которых повреждена основная загрузочная запись (MBR) и вы не можете получить доступ к жесткому диску и поддерживает ситуации, в которых отсутствует сетевое соединение.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-119">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk and supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="c0dc9-120">Позволяет создавать несколько образов восстановления с различными инструментами для обеспечения разных уровней поддержки.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-120">Enables you to create multiple recovery images with different tools to provide different levels of support.</span></span></p>
<p><span data-ttu-id="c0dc9-121">Предоставляет встроенные средства для записи изображений для восстановления на съемные носители.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-121">Provides a built-in tool for burning recovery images to removable media.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0dc9-122">Требуется, чтобы сотрудники службы поддержки были физически на компьютере конечного пользователя, чтобы загрузить DaRT.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-122">Requires that support staff are physically at the end-user computer to boot into DaRT.</span></span></p>
<p><span data-ttu-id="c0dc9-123">Требуется время и обслуживание для создания нескольких носителей с разными конфигурациями для 32-разрядных и 64-разрядных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-123">Requires time and maintenance to create multiple media with different configurations for 32-bit and 64-bit computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c0dc9-124">С удаленным (сетевым) разделом</span><span class="sxs-lookup"><span data-stu-id="c0dc9-124">From a remote (network) partition</span></span></strong></p>
<p><span data-ttu-id="c0dc9-125">Образ восстановления размещается на сервере сетевой загрузки, например в службах развертывания Windows (Windows DS), что позволяет пользователям или сотрудникам отдела обслуживания передавать их на компьютеры по запросу.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-125">The recovery image is hosted on a network boot server like Windows Deployment Services (Windows DS), which allows users or support staff to stream it to computers on demand.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0dc9-126">Доступно для всех компьютеров, у которых есть доступ к серверу сетевой загрузки.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-126">Available to all computers that have access to the network boot server.</span></span></p>
<p><span data-ttu-id="c0dc9-127">Образы восстановления размещаются на центральном сервере, который включает централизованные обновления.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-127">Recovery images are hosted on a central server, which enables centralized updates.</span></span></p>
<p><span data-ttu-id="c0dc9-128">Сотрудники службы централизованной поддержки могут выполнять ремонт, используя удаленное подключение.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-128">Centralized help desk staff can provide repairs by using remote connectivity.</span></span></p>
<p><span data-ttu-id="c0dc9-129">На клиентах нет требований к локальному хранилищу.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-129">No local storage requirement on the clients.</span></span></p>
<p><span data-ttu-id="c0dc9-130">Возможность создания нескольких изображений восстановления с различными инструментами для конкретных уровней поддержки.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-130">Ability to create multiple recovery images with different tools for specific support levels.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0dc9-131">Нужна защита инфраструктуры служб Windows DS для того, чтобы обычные пользователи могли запускать только образ восстановления DaRT, а не полный процесс обработки образа операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-131">The need to secure Windows DS infrastructure to ensure that regular users can start only the DaRT recovery image and not the full operating system imaging process.</span></span></p>
<p></p>
<p></p>
<p><span data-ttu-id="c0dc9-132">Требуется, чтобы компьютер пользователя был подключен к сети во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-132">Requires that the end-user computer is connected to the network at runtime.</span></span></p>
<p><span data-ttu-id="c0dc9-133">Требуется, чтобы образ восстановления был подключен по сети.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-133">Requires that the recovery image is brought across the network.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c0dc9-134">Из раздела восстановления на локальном жестком диске</span><span class="sxs-lookup"><span data-stu-id="c0dc9-134">From a recovery partition on the local hard drive</span></span></strong></p>
<p><span data-ttu-id="c0dc9-135">Образ для восстановления установлен на локальном жестком диске либо вручную, либо с помощью электронных систем распространения программного обеспечения, таких как System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-135">The recovery image is installed on a local hard drive either manually or by using electronic software distribution systems like System Center Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0dc9-136">Изображение для восстановления всегда доступно, так как оно предварительно размещено на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-136">The recovery image is always available because it is pre-staged on the computer.</span></span></p>
<p><span data-ttu-id="c0dc9-137">Ролевая служба централизованной поддержки может предоставлять поддержку с помощью удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-137">Centralized help desk staff can provide support by using Remote Connection.</span></span></p>
<p><span data-ttu-id="c0dc9-138">Образ восстановления централизованно управляется и развертывается.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-138">The recovery image is centrally managed and deployed.</span></span></p>
<p><span data-ttu-id="c0dc9-139">Удаляются дополнительные запросы ключей восстановления на компьютерах, защищенных с помощью шифрования диска Windows BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-139">Additional recovery key requests on computers that are protected by Windows BitLocker drive encryption are eliminated.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0dc9-140">Требуется локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-140">Local storage is required.</span></span></p>
<p><span data-ttu-id="c0dc9-141">Для снижения риска неудачного загрузочного раздела рекомендуется выделить специальную незашифрованную секцию для размещения образа восстановления.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-141">A dedicated, unencrypted partition for recovery image placement is recommended to reduce the risk of a failed boot partition.</span></span></p>
<p><span data-ttu-id="c0dc9-142">При обновлении DaRT необходимо обновить все компьютеры в Организации, а не только один раздел (в сети) или съемные устройства.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-142">When updating DaRT, you must update all computers in your enterprise instead of just one partition (on the network) or removable device.</span></span></p>
<p><span data-ttu-id="c0dc9-143">При развертывании образа восстановления после включения BitLocker необходимо учитывать дополнительные вопросы.</span><span class="sxs-lookup"><span data-stu-id="c0dc9-143">Additional consideration is required if you deploy the recovery image after BitLocker has been enabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c0dc9-144">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c0dc9-144">Related topics</span></span>


[<span data-ttu-id="c0dc9-145">Планирование развертывания DaRT 10</span><span class="sxs-lookup"><span data-stu-id="c0dc9-145">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 





