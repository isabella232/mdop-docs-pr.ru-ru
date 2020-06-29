---
title: Определение способа публикации
description: Определение способа публикации
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821679"
---
# <span data-ttu-id="f76a1-103">Определение способа публикации</span><span class="sxs-lookup"><span data-stu-id="f76a1-103">Determine Your Publishing Method</span></span>


<span data-ttu-id="f76a1-104">После упорядочения приложения с помощью Application Virtualization Sequencer необходимо *опубликовать* это приложение для пользователей.</span><span class="sxs-lookup"><span data-stu-id="f76a1-104">After you sequence an application by using the Application Virtualization Sequencer, you need to *publish* that application to your users.</span></span> <span data-ttu-id="f76a1-105">Публикация приложения включает в себя значки, сведения определения пакета и расположение источника содержимого для каждого компьютера, на котором установлен клиент Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f76a1-105">Publishing the application consists of delivering the icons, package definition information, and content source location to each computer where the Application Virtualization Client has been installed.</span></span> <span data-ttu-id="f76a1-106">В следующей таблице описаны методы публикации, которые поддерживаются при развертывании виртуализации приложений с помощью электронной системы программного обеспечения (ESD).</span><span class="sxs-lookup"><span data-stu-id="f76a1-106">The following table describes publishing methods that are supported when you deploy Application Virtualization by using an electronic software distribution (ESD) system.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f76a1-107">Метод</span><span class="sxs-lookup"><span data-stu-id="f76a1-107">Method</span></span></th>
<th align="left"><span data-ttu-id="f76a1-108">Преимущества</span><span class="sxs-lookup"><span data-stu-id="f76a1-108">Advantages</span></span></th>
<th align="left"><span data-ttu-id="f76a1-109">Недостатки</span><span class="sxs-lookup"><span data-stu-id="f76a1-109">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f76a1-110">Создавайте файл установщика Windows во время виртуализации, как отдельное решение.</span><span class="sxs-lookup"><span data-stu-id="f76a1-110">Generate a Windows Installer file during sequencing, as a stand-alone solution.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f76a1-111">Очень простое использование.</span><span class="sxs-lookup"><span data-stu-id="f76a1-111">Very simple to use.</span></span></p></li>
<li><p><span data-ttu-id="f76a1-112">Пакет загружен в кэш локально на каждом компьютере.</span><span class="sxs-lookup"><span data-stu-id="f76a1-112">Package loaded into cache locally on each computer.</span></span></p></li>
<li><p><span data-ttu-id="f76a1-113">Значки, выводимые пользователю.</span><span class="sxs-lookup"><span data-stu-id="f76a1-113">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="f76a1-114">Похоже на традиционное развертывание программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="f76a1-114">Similar to traditional software deployment.</span></span></p></li>
<li><p><span data-ttu-id="f76a1-115">Потоковые серверы не требуются.</span><span class="sxs-lookup"><span data-stu-id="f76a1-115">No need for streaming servers.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f76a1-116">Нет гибкости в расположении содержимого пакета на компьютерах — одно и то же расположение на всех компьютерах.</span><span class="sxs-lookup"><span data-stu-id="f76a1-116">No flexibility in location of package contents on computers—same location on all computers.</span></span></p></li>
<li><p><span data-ttu-id="f76a1-117">Для удаления приложений необходимо использовать только надстройку "Установка и удаление программ" или msiexec.</span><span class="sxs-lookup"><span data-stu-id="f76a1-117">Must use only Add/Remove Programs or msiexec to remove applications.</span></span></p></li>
<li><p><span data-ttu-id="f76a1-118">Удаление и замена с новой версией, необходимой для обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="f76a1-118">Removal and replacement with new version required for package updating.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f76a1-119">Создание файла установщика Windows во время выполнения виртуализации с использованием свойств MODE, LOAD и OVERRIDEURL в командной строке и манифеста пакета.</span><span class="sxs-lookup"><span data-stu-id="f76a1-119">Generate a Windows Installer file during sequencing, used with MODE, LOAD, and OVERRIDEURL command-line properties and the package manifest.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f76a1-120">Простота в использовании, но с повышенной гибкостью.</span><span class="sxs-lookup"><span data-stu-id="f76a1-120">Simple to use but with added flexibility.</span></span></p></li>
<li><p><span data-ttu-id="f76a1-121">Значки, выводимые пользователю.</span><span class="sxs-lookup"><span data-stu-id="f76a1-121">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="f76a1-122">SFT-файл, содержащий приложения, может быть размещен в исходном расположении, с клиентами, настроенными на использование этого расположения.</span><span class="sxs-lookup"><span data-stu-id="f76a1-122">SFT file containing the applications can be placed on a streaming source location, with clients configured to use that location.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f76a1-123">Ограниченная гибкость — управлять можно только расположением содержимого пакета во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f76a1-123">Limited flexibility—only the location of the package content can be controlled at run time.</span></span></p></li>
<li><p><span data-ttu-id="f76a1-124">Для удаления приложения необходимо использовать только надстройку "Установка и удаление программ" или msiexec.</span><span class="sxs-lookup"><span data-stu-id="f76a1-124">Must use only Add/Remove Programs or msiexec to remove the application.</span></span></p></li>
<li><p><span data-ttu-id="f76a1-125">Удаление и замена с новой версией, необходимой для обновления пакета, если только не используется потоковый сервер.</span><span class="sxs-lookup"><span data-stu-id="f76a1-125">Removal and replacement with new version required for package updating, unless using streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f76a1-126">Выполнение команд SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="f76a1-126">Run SFTMIME commands.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f76a1-127">Полная гибкость — полный контроль над всеми функциями управления пакетами.</span><span class="sxs-lookup"><span data-stu-id="f76a1-127">Complete flexibility—full control of all package management functions.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f76a1-128">Команды должны быть написаны в сценариях для использования с системой ESD.</span><span class="sxs-lookup"><span data-stu-id="f76a1-128">Commands must be scripted for use with the ESD system.</span></span></p></li>
<li><p><span data-ttu-id="f76a1-129">Команды должны выполняться на каждом компьютере в правильной последовательности.</span><span class="sxs-lookup"><span data-stu-id="f76a1-129">Commands must be run on each computer in correct sequence.</span></span></p></li>
<li><p><span data-ttu-id="f76a1-130">Подробное изучение командного языка и тщательное планирование.</span><span class="sxs-lookup"><span data-stu-id="f76a1-130">Detailed understanding of command language and careful planning required.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f76a1-131">Дополнительные сведения об использовании этих методов публикации вы узнаете, [как опубликовать виртуальное приложение на клиентском компьютере](how-to-publish-a-virtual-application-on-the-client.md).</span><span class="sxs-lookup"><span data-stu-id="f76a1-131">For more information about using these publishing methods, see [How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md).</span></span>

## <span data-ttu-id="f76a1-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f76a1-132">Related topics</span></span>


[<span data-ttu-id="f76a1-133">Определение способа потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="f76a1-133">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="f76a1-134">Сценарий на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="f76a1-134">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="f76a1-135">Обзор сценария на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="f76a1-135">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="f76a1-136">Публикация виртуального приложения на клиенте</span><span class="sxs-lookup"><span data-stu-id="f76a1-136">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="f76a1-137">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="f76a1-137">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





