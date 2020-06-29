---
title: Планирование способов сохранения и развертывания образа для восстановления DaRT 7.0
description: Планирование способов сохранения и развертывания образа для восстановления DaRT 7.0
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822799"
---
# <span data-ttu-id="a3690-103">Планирование способов сохранения и развертывания образа для восстановления DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="a3690-103">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="a3690-104">Используйте сведения из этого раздела, если вы планируете сохранить и развернуть образ восстановления для Microsoft Diagnostics и средств восстановления (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="a3690-104">Use the information in this section when you plan for saving and deploying the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="a3690-105">Планирование сохранения и развертывания изображения для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="a3690-105">Planning How to Save and Deploy the DaRT Recovery Image</span></span>


<span data-ttu-id="a3690-106">Вы можете сохранить и развернуть образ для DaRT с помощью описанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="a3690-106">You can save and deploy the DaRT recovery image by using the following methods.</span></span> <span data-ttu-id="a3690-107">Определив метод, который будет использоваться, продумайте преимущества и недостатки каждого из них.</span><span class="sxs-lookup"><span data-stu-id="a3690-107">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="a3690-108">Кроме того, вы можете использовать DaRT в Организации.</span><span class="sxs-lookup"><span data-stu-id="a3690-108">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="a3690-109">**Примечание**  Возможно, вы захотите использовать в Организации более одного способа.</span><span class="sxs-lookup"><span data-stu-id="a3690-109">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="a3690-110">Например, вы можете загрузить DaRT из удаленной секции для большинства ситуаций и получить доступ к флэш-накопителю USB на случай, если компьютер пользователя не может подключиться к сети.</span><span class="sxs-lookup"><span data-stu-id="a3690-110">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="a3690-111">В таблице ниже приведены некоторые преимущества и недостатки использования DaRT в Организации.</span><span class="sxs-lookup"><span data-stu-id="a3690-111">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a3690-112">Метод загрузки для DaRT</span><span class="sxs-lookup"><span data-stu-id="a3690-112">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="a3690-113">Преимущества</span><span class="sxs-lookup"><span data-stu-id="a3690-113">Advantages</span></span></th>
<th align="left"><span data-ttu-id="a3690-114">Недостатки</span><span class="sxs-lookup"><span data-stu-id="a3690-114">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3690-115">С компакт-диска или DVD</span><span class="sxs-lookup"><span data-stu-id="a3690-115">From a CD or DVD</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3690-116">Поддерживаются сценарии, в которых повреждена основная загрузочная запись (MBR), и вы не можете получить доступ к жесткому диску.</span><span class="sxs-lookup"><span data-stu-id="a3690-116">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk.</span></span> <span data-ttu-id="a3690-117">Также поддерживаются ситуации, в которых отсутствует сетевое соединение.</span><span class="sxs-lookup"><span data-stu-id="a3690-117">Also supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="a3690-118">Это наиболее общее представление о пользователях более ранних версий DaRT, а также на компакт-дисках и DVD-дисках, с помощью <strong> мастера создания изображений для восстановления DaRT </strong> .</span><span class="sxs-lookup"><span data-stu-id="a3690-118">This is most familiar to users of earlier versions of DaRT, and a CD or DVD can be burned directly from the <strong>DaRT Recovery Image Wizard</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3690-119">Предполагается, что кто-то, у кого есть доступ к компакт-диску или DVD-диску, физически находится на компьютере конечного пользователя, чтобы загрузить DaRT.</span><span class="sxs-lookup"><span data-stu-id="a3690-119">Requires that someone with access to the CD or DVD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3690-120">С USB-накопителя (UFD)</span><span class="sxs-lookup"><span data-stu-id="a3690-120">From a USB flash drive (UFD)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3690-121">Имеет те же преимущества, что и загрузка с компакт-диска или DVD-диска, а также поддержка компьютеров, у которых нет дисководов для компакт-дисков или DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="a3690-121">Provides same advantages as booting from a CD or DVD and also provides support to computers that have no CD or DVD drive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3690-122">Перед тем как использовать средство DaRT для загрузки, необходимо отформатировать USB-устройство флэш-памяти.</span><span class="sxs-lookup"><span data-stu-id="a3690-122">Requires you to format the UFD before you can use it to boot into DaRT.</span></span> <span data-ttu-id="a3690-123">Также требуется, чтобы кто-то, у кого есть доступ к UFD, физически находится на компьютере конечного пользователя, чтобы загрузить DaRT.</span><span class="sxs-lookup"><span data-stu-id="a3690-123">Also requires that someone with access to the UFD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3690-124">С удаленным (сетевым) разделом</span><span class="sxs-lookup"><span data-stu-id="a3690-124">From a remote (network) partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3690-125">Вы можете загрузиться с помощью DaRT без компакт-диска, DVD-диска или USB UFD.</span><span class="sxs-lookup"><span data-stu-id="a3690-125">Lets you boot into DaRT without needing a CD, DVD, or UFD.</span></span> <span data-ttu-id="a3690-126">Кроме того, вы можете легко обновлять DaRT, так как для обновления доступно только одно расположение файлов.</span><span class="sxs-lookup"><span data-stu-id="a3690-126">Also allows for easy upgrades of DaRT because there is only one file location to update.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3690-127">Не работает, если конечный компьютер пользователя не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="a3690-127">Does not work if the end-user computer is not connected to the network.</span></span></p>
<p><span data-ttu-id="a3690-128">Доступно для конечных пользователей, и при создании образа восстановления могут потребоваться дополнительные рекомендации по обеспечению безопасности.</span><span class="sxs-lookup"><span data-stu-id="a3690-128">Widely available to end users and might require additional security considerations when you are creating the recovery image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3690-129">Из раздела восстановления</span><span class="sxs-lookup"><span data-stu-id="a3690-129">From a recovery partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3690-130">Позволяет загружаться с помощью DaRT без использования компакт-диска, DVD-диска или UFD, включающего экземпляры, в которых отсутствует сетевое подключение.</span><span class="sxs-lookup"><span data-stu-id="a3690-130">Lets you boot into DaRT without needing a CD, DVD, or UFD that includes instances in which there is no network connectivity.</span></span></p>
<p><span data-ttu-id="a3690-131">Кроме того, можно реализовать и управлять в рамках стандартного процесса образа Windows с помощью автоматизированных средств распространения, например диспетчера конфигураций конечных точек Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a3690-131">Also, can be implemented and managed as part of your standard Windows image process by using automated distribution tools, such as Microsoft Endpoint Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3690-132">При обновлении DaRT требуется обновить все компьютеры в Организации, а не только один раздел (в сети) или устройство (CD, DVD или UFD).</span><span class="sxs-lookup"><span data-stu-id="a3690-132">When updating DaRT, requires you to update all computers in your enterprise instead of just one partition (on the network) or device (CD, DVD, or UFD).</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a3690-133">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a3690-133">Related topics</span></span>


[<span data-ttu-id="a3690-134">Планирование развертывания DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="a3690-134">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





