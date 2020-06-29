---
title: Применение файла конфигурации пользователя с помощью PowerShell
description: Применение файла конфигурации пользователя с помощью PowerShell
author: dansimp
ms.assetid: 986e638c-4a0c-4a7e-be73-f4615e8b8000
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97b3db253993d6d855384ee5d9771a7f9ff5b64d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814429"
---
# <span data-ttu-id="7b9fb-103">Применение файла конфигурации пользователя с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="7b9fb-103">How to Apply the User Configuration File by Using PowerShell</span></span>


<span data-ttu-id="7b9fb-104">Файл динамической конфигурации применяется, когда пакет публикуется для определенного пользователя, и определяет, как будет выполняться пакет.</span><span class="sxs-lookup"><span data-stu-id="7b9fb-104">The dynamic user configuration file is applied when a package is published to a specific user and determines how the package will run.</span></span>

<span data-ttu-id="7b9fb-105">Чтобы задать файл конфигурации для определенного пользователя, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7b9fb-105">Use the following procedure to specify a user-specific configuration file.</span></span> <span data-ttu-id="7b9fb-106">Ниже описана процедура, основанная на примере.</span><span class="sxs-lookup"><span data-stu-id="7b9fb-106">The following procedure is based on the example:</span></span>

**<span data-ttu-id="7b9fb-107">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="7b9fb-107">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="7b9fb-108">Применение файла конфигурации пользователя</span><span class="sxs-lookup"><span data-stu-id="7b9fb-108">To apply a user Configuration file</span></span>**

1.  <span data-ttu-id="7b9fb-109">Чтобы добавить пакет на компьютер с помощью консоли PowerShell, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7b9fb-109">To add the package to the computer using the PowerShell console type the following command:</span></span>

    <span data-ttu-id="7b9fb-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.AppV**.</span><span class="sxs-lookup"><span data-stu-id="7b9fb-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.appv**.</span></span>

2.  <span data-ttu-id="7b9fb-111">Используйте следующую команду, чтобы опубликовать пакет для пользователя, и укажите обновленный файл динамической конфигурации.</span><span class="sxs-lookup"><span data-stu-id="7b9fb-111">Use the following command to publish the package to the user and specify the updated the dynamic user configuration file:</span></span>

    **<span data-ttu-id="7b9fb-112">Publish (AppVClientPackage $pkg — DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span><span class="sxs-lookup"><span data-stu-id="7b9fb-112">Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span></span>**

    <span data-ttu-id="7b9fb-113">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="7b9fb-113">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="7b9fb-114">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="7b9fb-114">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="7b9fb-115">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="7b9fb-115">Got an App-V issue?</span></span>** <span data-ttu-id="7b9fb-116">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="7b9fb-116">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="7b9fb-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7b9fb-117">Related topics</span></span>


[<span data-ttu-id="7b9fb-118">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="7b9fb-118">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





