---
title: Перенос точек расширения из пакета App-V 4.6 в App-V 5.0 для конкретного пользователя
description: Перенос точек расширения из пакета App-V 4.6 в App-V 5.0 для конкретного пользователя
ms.assetid: dad25992-3c75-4b7d-b4c6-c2edf43baaea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a17d9dad11092a4c8356983b70bea3c18da1be04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813877"
---
# <span data-ttu-id="c9ec6-103">Перенос точек расширения из пакета App-V 4.6 в App-V 5.0 для конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="c9ec6-103">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>

<span data-ttu-id="c9ec6-104">*Примечание:*\* App-V 4,6 вышел из основной поддержки.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="c9ec6-105">Чтобы перенести пакеты, созданные с помощью App-V, с использованием файла конфигурации пользователя, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-105">Use the following procedure to migrate packages created with App-V using the user configuration file.</span></span>

**<span data-ttu-id="c9ec6-106">Преобразование пакета</span><span class="sxs-lookup"><span data-stu-id="c9ec6-106">To convert a package</span></span>**

1. <span data-ttu-id="c9ec6-107">Найдите файл конфигурации пользователя для пакета, который вы хотите преобразовать.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-107">Locate the user configuration file for the package you want to convert.</span></span> <span data-ttu-id="c9ec6-108">Чтобы настроить политику, выполните следующие обновления в разделе **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID &gt; пакета**.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-108">To set the policy, perform the following updates in the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;**.</span></span>

   <span data-ttu-id="c9ec6-109">Ниже приведен пример файла конфигурации пользователя.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-109">The following is an example of a user configuration file:</span></span>

   <span data-ttu-id="c9ec6-110">&lt;? XML Version = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="c9ec6-110">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="c9ec6-111">&lt;UserConfiguration PackageId = &lt; ИД пакета &gt; DisplayName = &lt; имя пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="c9ec6-111">&lt;UserConfiguration PackageId=&lt;Package ID&gt; DisplayName=&lt;Name of the Package&gt;</span></span>

   <span data-ttu-id="c9ec6-112">xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "истина"</span><span class="sxs-lookup"><span data-stu-id="c9ec6-112">xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>; &lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="c9ec6-113">PackageName = &lt; ИД пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="c9ec6-113">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="c9ec6-114">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c9ec6-114">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="c9ec6-115">Чтобы добавить пакет App-V 5,0, введите в командной строке с повышенными привилегиями PowerShell следующее:</span><span class="sxs-lookup"><span data-stu-id="c9ec6-115">To add the App-V 5.0 package type the following in an elevated PowerShell command prompt:</span></span>

   <span data-ttu-id="c9ec6-116">PS &gt; **$pkg = Add-AppvClientPackage —** путь к &lt; расположению пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="c9ec6-116">PS&gt;**$pkg= Add-AppvClientPackage –Path** &lt;Path to package location&gt;</span></span>

   <span data-ttu-id="c9ec6-117">&gt;**DynamicUserConfiguration Publish-AppVClientPackage $pkg —** &lt; путь к файлу конфигурации пользователя&gt;</span><span class="sxs-lookup"><span data-stu-id="c9ec6-117">PS&gt;**Publish-AppVClientPackage $pkg -DynamicUserConfiguration** &lt;Path to the user configuration file&gt;</span></span>

3. <span data-ttu-id="c9ec6-118">Откройте приложение с помощью FTAs или ярлыков прямо сейчас.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-118">Open the application using FTAs or shortcuts now.</span></span> <span data-ttu-id="c9ec6-119">Приложение должно открыться с помощью App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-119">The application should open using App-V 5.0.</span></span>

   <span data-ttu-id="c9ec6-120">Пакет обновления 2 (SP2) для App-V и преобразованный пакет App-V 5,0 публикуются для пользователя, но FTAs и сочетания клавиш для приложений предполагались пакетом App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-120">The App-V SP2 package and the converted App-V 5.0 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.0 package.</span></span>

   <span data-ttu-id="c9ec6-121">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="c9ec6-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="c9ec6-122">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="c9ec6-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="c9ec6-123">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="c9ec6-123">Got an App-V issue?</span></span>** <span data-ttu-id="c9ec6-124">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="c9ec6-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="c9ec6-125">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c9ec6-125">Related topics</span></span>


[<span data-ttu-id="c9ec6-126">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c9ec6-126">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





