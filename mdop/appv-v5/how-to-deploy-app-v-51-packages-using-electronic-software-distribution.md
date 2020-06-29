---
title: Развертывание пакетов App-V 5.1 с помощью системы электронного распространения программного обеспечения
description: Развертывание пакетов App-V 5.1 с помощью системы электронного распространения программного обеспечения
author: dansimp
ms.assetid: e1957a5a-1f18-42da-b2c1-a5ae5a4cca7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a9ed5fbb264f8fb9676d7fa18fe4de8019ea8e79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814184"
---
# <span data-ttu-id="9f053-103">Развертывание пакетов App-V 5.1 с помощью системы электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="9f053-103">How to deploy App-V 5.1 Packages Using Electronic Software Distribution</span></span>


<span data-ttu-id="9f053-104">Вы можете использовать систему электронной рассылки программного обеспечения (ESD) для развертывания виртуальных приложений App-V 5,1 для клиентов App-V.</span><span class="sxs-lookup"><span data-stu-id="9f053-104">You can use an electronic software distribution (ESD) system to deploy App-V 5.1 virtual applications to App-V clients.</span></span> <span data-ttu-id="9f053-105">Дополнительные сведения можно найти в документации, которая поддерживается с помощью ESD.</span><span class="sxs-lookup"><span data-stu-id="9f053-105">For details, see the documentation available with the ESD you are using.</span></span>

<span data-ttu-id="9f053-106">Требования к компонентам и параметры для развертывания пакетов App-V можно найти [в разделе Планирование развертывания App-v 5,1 с помощью электронной системы распространения программного обеспечения](planning-to-deploy-app-v-51-with-an-electronic-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="9f053-106">For component requirements and options for using an ESD to deploy App-V packages, see [Planning to Deploy App-V 5.1 with an Electronic Software Distribution System](planning-to-deploy-app-v-51-with-an-electronic-software-distribution-system.md).</span></span>

<span data-ttu-id="9f053-107">Чтобы опубликовать пакеты на клиентских компьютерах App-V с помощью ESD, воспользуйтесь одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="9f053-107">Use one of the following methods to publish packages to App-V client computers with an ESD:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9f053-108">Метод</span><span class="sxs-lookup"><span data-stu-id="9f053-108">Method</span></span></th>
<th align="left"><span data-ttu-id="9f053-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9f053-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f053-110">Функциональные возможности, предоставляемые сторонним электростатическим</span><span class="sxs-lookup"><span data-stu-id="9f053-110">Functionality provided by a third-party ESD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f053-111">Использование функций в независимых от друга функциях ESD.</span><span class="sxs-lookup"><span data-stu-id="9f053-111">Use the functionality in a third-party ESD.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9f053-112">Самостоятельный установщик Windows</span><span class="sxs-lookup"><span data-stu-id="9f053-112">Stand-alone Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f053-113">Установите приложение на целевом клиентском компьютере, используя соответствующий файл установщика Windows (MSI), созданный при первоначальной последовательности приложения.</span><span class="sxs-lookup"><span data-stu-id="9f053-113">Install the application on the target client computer by using the associated Windows Installer (.msi) file that is created when you initially sequence an application.</span></span> <span data-ttu-id="9f053-114">Файл установщика Windows включает соответствующие сведения о файле App-V 5,1, используемые для настройки пакета, и копирует необходимые файлы пакета на клиент.</span><span class="sxs-lookup"><span data-stu-id="9f053-114">The Windows Installer file contains the associated App-V 5.1 package file information used to configure a package and copies the required package files to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f053-115">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9f053-115">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f053-116">Используйте командлеты PowerShell для развертывания виртуализированных приложений.</span><span class="sxs-lookup"><span data-stu-id="9f053-116">Use PowerShell cmdlets to deploy virtualized applications.</span></span> <span data-ttu-id="9f053-117">Дополнительные сведения об использовании PowerShell и App-V 5,1 можно найти в разделе <a href="administering-app-v-51-by-using-powershell.md" data-raw-source="[Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md)"> Администрирование App-v 5,1 с помощью PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="9f053-117">For more information about using PowerShell and App-V 5.1, see <a href="administering-app-v-51-by-using-powershell.md" data-raw-source="[Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md)">Administering App-V 5.1 by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="9f053-118">Развертывание пакетов App-V 5,1 с помощью ESD</span><span class="sxs-lookup"><span data-stu-id="9f053-118">To deploy App-V 5.1 packages by using an ESD</span></span>**

1.  <span data-ttu-id="9f053-119">Установите секвенсор App-V 5,1 на компьютере в среде.</span><span class="sxs-lookup"><span data-stu-id="9f053-119">Install the App-V 5.1 Sequencer on a computer in your environment.</span></span> <span data-ttu-id="9f053-120">Дополнительные сведения об установке секвенсора вы узнаете, [как установить секвенсор](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="9f053-120">For more information about installing the sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  <span data-ttu-id="9f053-121">Используйте секвенсор App-V 5,1, чтобы создать виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="9f053-121">Use the App-V 5.1 Sequencer to create virtual application.</span></span> <span data-ttu-id="9f053-122">Сведения о создании виртуального приложения можно найти в разделе [Создание виртуальных приложений для App-V 5,1 и управление ими](creating-and-managing-app-v-51-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="9f053-122">For information about creating a virtual application, see [Creating and Managing App-V 5.1 Virtualized Applications](creating-and-managing-app-v-51-virtualized-applications.md).</span></span>

3.  <span data-ttu-id="9f053-123">После создания виртуального приложения разверните пакет с помощью решения ESD.</span><span class="sxs-lookup"><span data-stu-id="9f053-123">After you create the virtual application, deploy the package by using your ESD solution.</span></span>

    <span data-ttu-id="9f053-124">Если вы используете System Center Configuration Manager, начните с обзора " [Введение в Управление приложениями" в Configuration Manager, чтобы](https://go.microsoft.com/fwlink/?LinkId=281816) получить сведения об использовании App-V 5,1 и System Center2012 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9f053-124">If you are using System Center Configuration Manager, start by reviewing [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) for information about using App-V 5.1 and System Center2012 Configuration Manager.</span></span>

    <span data-ttu-id="9f053-125">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="9f053-125">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9f053-126">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="9f053-126">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="9f053-127">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="9f053-127">Got an App-V issue?</span></span>** <span data-ttu-id="9f053-128">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9f053-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="9f053-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9f053-129">Related topics</span></span>


[<span data-ttu-id="9f053-130">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="9f053-130">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





