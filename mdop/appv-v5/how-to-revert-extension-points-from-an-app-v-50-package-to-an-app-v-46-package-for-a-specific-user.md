---
ms.reviewer: ''
title: Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для конкретного пользователя
description: Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для конкретного пользователя
ms.assetid: f1d2ab1f-0831-4976-b49f-169511d3382a
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2a0660024734806c508043cc2db030c96cfd16a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813741"
---
# <span data-ttu-id="b1c53-103">Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="b1c53-103">How to Revert Extension Points From an App-V 5.0 Package to an App-V 4.6 Package for a Specific User</span></span>

<span data-ttu-id="b1c53-104">*Примечание:*\* App-V 4,6 вышел из основной поддержки.</span><span class="sxs-lookup"><span data-stu-id="b1c53-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="b1c53-105">Чтобы вернуть пакет App-V 5,0 в формат файла App-V с помощью файла конфигурации пользователя, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b1c53-105">Use the following procedure to revert an App-V 5.0 package to the App-V file format using the user configuration file.</span></span>

**<span data-ttu-id="b1c53-106">Отмена пакета</span><span class="sxs-lookup"><span data-stu-id="b1c53-106">To revert a package</span></span>**

1.  <span data-ttu-id="b1c53-107">Убедитесь в том, что пакет App-V 4,6 опубликован для пользователей, но FTAs и сочетания клавиш предполагались пакетом App-V 5,0 с помощью следующего метода миграции, [как переносить точки расширения из пакета App-v 4,6 в приложение App-v 5,0 для определенного пользователя](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="b1c53-107">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.0 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span></span>

    <span data-ttu-id="b1c53-108">В разделе **userConfiguration** файла конфигурации развертывания для преобразованного пакета, чтобы настроить политику, сделайте следующее обновление в разделе **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "ложь" PackageName = &lt; ИД &gt; пакета**</span><span class="sxs-lookup"><span data-stu-id="b1c53-108">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="b1c53-109">В командной строке с повышенными привилегиями введите:</span><span class="sxs-lookup"><span data-stu-id="b1c53-109">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="b1c53-110">PS &gt; **Publish-AppVClientPackage $pkg — DynamicUserConfigurationPath** &lt; путь к файлу конфигурации пользователя&gt;</span><span class="sxs-lookup"><span data-stu-id="b1c53-110">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath** &lt;path to user configuration file&gt;</span></span>

3.  <span data-ttu-id="b1c53-111">Выполните обновление публикации или дождитесь следующего запланированного обновления публикации для App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="b1c53-111">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6.</span></span> <span data-ttu-id="b1c53-112">Откройте приложение с помощью FTAs или сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="b1c53-112">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="b1c53-113">Теперь приложение должно открываться с помощью App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="b1c53-113">The Application should now open using App-V 4.6 SP2.</span></span>

    **<span data-ttu-id="b1c53-114">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b1c53-114">Note</span></span>**  
    <span data-ttu-id="b1c53-115">Если вы больше не хотите использовать пакет App-V 5,0, вы можете отменить публикацию пакета App-V 5,0, а точки расширения будут автоматически возвращены в приложение App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="b1c53-115">If you do not need the App-V 5.0 package anymore, you can unpublish the App-V 5.0 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="b1c53-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b1c53-116">Related topics</span></span>


[<span data-ttu-id="b1c53-117">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b1c53-117">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)












