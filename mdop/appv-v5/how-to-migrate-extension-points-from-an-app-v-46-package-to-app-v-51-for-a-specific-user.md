---
title: Перенос точек расширения из пакета App-V 4.6 в App-V 5.1 для конкретного пользователя
description: Перенос точек расширения из пакета App-V 4.6 в App-V 5.1 для конкретного пользователя
author: dansimp
ms.assetid: 19da3776-5ebe-41e1-9890-12b84ef3c1c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: e2166b0f280153ad62709b21bb3477d0c4277fcd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813869"
---
# <span data-ttu-id="a5d81-103">Перенос точек расширения из пакета App-V 4.6 в App-V 5.1 для конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="a5d81-103">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>


<span data-ttu-id="a5d81-104">Чтобы перенести пакеты, созданные с помощью App-V, с использованием файла конфигурации пользователя, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a5d81-104">Use the following procedure to migrate packages created with App-V using the user configuration file.</span></span>

<span data-ttu-id="a5d81-105">**Примечание**  В этой процедуре предполагается, что вы используете последнюю версию App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="a5d81-105">**Note** This procedure assumes that you are running the latest version of App-V 4.6.</span></span>

**<span data-ttu-id="a5d81-106">Преобразование пакета</span><span class="sxs-lookup"><span data-stu-id="a5d81-106">To convert a package</span></span>**

1. <span data-ttu-id="a5d81-107">Найдите файл конфигурации пользователя для пакета, который вы хотите преобразовать.</span><span class="sxs-lookup"><span data-stu-id="a5d81-107">Locate the user configuration file for the package you want to convert.</span></span> <span data-ttu-id="a5d81-108">Чтобы настроить политику, выполните следующие обновления в разделе **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID &gt; пакета**.</span><span class="sxs-lookup"><span data-stu-id="a5d81-108">To set the policy, perform the following updates in the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;**.</span></span>

   <span data-ttu-id="a5d81-109">Ниже приведен пример файла конфигурации пользователя.</span><span class="sxs-lookup"><span data-stu-id="a5d81-109">The following is an example of a user configuration file:</span></span>

   <span data-ttu-id="a5d81-110">&lt;? XML Version = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="a5d81-110">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="a5d81-111">&lt;UserConfiguration PackageId = &lt; ИД пакета &gt; DisplayName = &lt; имя пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="a5d81-111">&lt;UserConfiguration PackageId=&lt;Package ID&gt; DisplayName=&lt;Name of the Package&gt;</span></span>

   <span data-ttu-id="a5d81-112">xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "истина"</span><span class="sxs-lookup"><span data-stu-id="a5d81-112">xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>; &lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="a5d81-113">PackageName = &lt; ИД пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="a5d81-113">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="a5d81-114">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="a5d81-114">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="a5d81-115">Чтобы добавить пакет App-V 5,1, введите следующую команду в окне командной строки PowerShell с повышенными привилегиями:</span><span class="sxs-lookup"><span data-stu-id="a5d81-115">To add the App-V 5.1 package, type the following in an elevated PowerShell command prompt window:</span></span>

   <span data-ttu-id="a5d81-116">PS &gt; **$pkg = Add-AppvClientPackage —** путь к &lt; расположению пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="a5d81-116">PS&gt;**$pkg= Add-AppvClientPackage –Path** &lt;Path to package location&gt;</span></span>

   <span data-ttu-id="a5d81-117">&gt;**DynamicUserConfiguration Publish-AppVClientPackage $pkg —** &lt; путь к файлу конфигурации пользователя&gt;</span><span class="sxs-lookup"><span data-stu-id="a5d81-117">PS&gt;**Publish-AppVClientPackage $pkg -DynamicUserConfiguration** &lt;Path to the user configuration file&gt;</span></span>

3. <span data-ttu-id="a5d81-118">Откройте приложение с помощью FTAs или ярлыков прямо сейчас.</span><span class="sxs-lookup"><span data-stu-id="a5d81-118">Open the application using FTAs or shortcuts now.</span></span> <span data-ttu-id="a5d81-119">Приложение должно открыться с помощью App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a5d81-119">The application should open using App-V 5.1.</span></span>

   <span data-ttu-id="a5d81-120">Пакет App-V 4,6 и преобразованный пакет приложения App-V 5,1 публикуются для пользователя, но FTAs и сочетания клавиш для приложений предполагались в пакете App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a5d81-120">The App-V 4.6 package and the converted App-V 5.1 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.1 package.</span></span>

   <span data-ttu-id="a5d81-121">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="a5d81-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a5d81-122">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="a5d81-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a5d81-123">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="a5d81-123">Got an App-V issue?</span></span>** <span data-ttu-id="a5d81-124">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a5d81-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a5d81-125">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a5d81-125">Related topics</span></span>


[<span data-ttu-id="a5d81-126">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a5d81-126">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="a5d81-127">Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="a5d81-127">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)

 

 





