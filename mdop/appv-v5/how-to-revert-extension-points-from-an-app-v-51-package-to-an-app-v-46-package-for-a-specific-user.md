---
title: Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для конкретного пользователя
description: Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для конкретного пользователя
author: dansimp
ms.assetid: bd53c5d6-7fd2-4816-b03b-d59da0a35819
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a69d6fb5b180161f39aa89e03b52227f32ce4879
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813733"
---
# <span data-ttu-id="df59e-103">Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="df59e-103">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>


<span data-ttu-id="df59e-104">Чтобы вернуть пакет App-V 5,1 в формат файла App-V с помощью файла конфигурации пользователя, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="df59e-104">Use the following procedure to revert an App-V 5.1 package to the App-V file format using the user configuration file.</span></span>

**<span data-ttu-id="df59e-105">Отмена пакета</span><span class="sxs-lookup"><span data-stu-id="df59e-105">To revert a package</span></span>**

1.  <span data-ttu-id="df59e-106">Убедитесь в том, что пакет App-V 4,6 опубликован для пользователей, но FTAs и сочетания клавиш предполагались пакетом App-V 5,1 с помощью следующего метода миграции, [как переносить точки расширения из пакета App-v 4,6 в приложение App-v 5,1 для определенного пользователя](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="df59e-106">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.1 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span></span>

    <span data-ttu-id="df59e-107">В разделе **userConfiguration** файла конфигурации развертывания для преобразованного пакета, чтобы настроить политику, сделайте следующее обновление в разделе **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "ложь" PackageName = &lt; ИД &gt; пакета**</span><span class="sxs-lookup"><span data-stu-id="df59e-107">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="df59e-108">В командной строке с повышенными привилегиями введите:</span><span class="sxs-lookup"><span data-stu-id="df59e-108">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="df59e-109">PS &gt; **Publish-AppVClientPackage $pkg — DynamicUserConfigurationPath** &lt; путь к файлу конфигурации пользователя&gt;</span><span class="sxs-lookup"><span data-stu-id="df59e-109">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath** &lt;path to user configuration file&gt;</span></span>

3.  <span data-ttu-id="df59e-110">Выполните обновление публикации или дождитесь следующего запланированного обновления публикации для App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="df59e-110">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6.</span></span> <span data-ttu-id="df59e-111">Откройте приложение с помощью FTAs или сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="df59e-111">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="df59e-112">Теперь приложение должно открываться с помощью App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="df59e-112">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="df59e-113">Примечание.</span><span class="sxs-lookup"><span data-stu-id="df59e-113">Note</span></span>**  
    <span data-ttu-id="df59e-114">Если вы больше не хотите использовать пакет App-V 5,1, вы можете отменить публикацию пакета App-V 5,1, а точки расширения будут автоматически возвращены в приложение App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="df59e-114">If you do not need the App-V 5.1 package anymore, you can unpublish the App-V 5.1 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="df59e-115">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="df59e-115">Related topics</span></span>


[<span data-ttu-id="df59e-116">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="df59e-116">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









