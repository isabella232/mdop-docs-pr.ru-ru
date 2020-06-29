---
title: Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для всех пользователей на указанном компьютере
description: Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для всех пользователей на указанном компьютере
author: dansimp
ms.assetid: 64640b8e-de6b-4006-a33e-353d285af15e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: ce8d5cc0e79be46fd9680a3bea0236bbeb93ea83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813725"
---
# <span data-ttu-id="caf0b-103">Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для всех пользователей на указанном компьютере</span><span class="sxs-lookup"><span data-stu-id="caf0b-103">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>


<span data-ttu-id="caf0b-104">Используйте описанную ниже процедуру, чтобы вернуть точки расширения из пакета App-V 5,1 в формат файлов App-V 4,6 с помощью файла конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="caf0b-104">Use the following procedure to revert extension points from an App-V 5.1 package to the App-V 4.6 file format using the deployment configuration file.</span></span>

**<span data-ttu-id="caf0b-105">Отмена пакета</span><span class="sxs-lookup"><span data-stu-id="caf0b-105">To revert a package</span></span>**

1.  <span data-ttu-id="caf0b-106">Убедитесь в том, что пакет App-V 4,6 опубликован для пользователей, но FTAs и сочетания клавиш предполагаются пакетом App-V 5,1 с помощью следующего метода миграции, [чтобы переносить точки расширения из пакета App-v 4,6 в преобразованный пакет App-v 5,1 для всех пользователей на определенном компьютере](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).</span><span class="sxs-lookup"><span data-stu-id="caf0b-106">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.1 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).</span></span>

    <span data-ttu-id="caf0b-107">В разделе **userConfiguration** файла конфигурации развертывания для преобразованного пакета, чтобы настроить политику, сделайте следующее обновление в разделе **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "ложь" PackageName = &lt; ИД &gt; пакета**</span><span class="sxs-lookup"><span data-stu-id="caf0b-107">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="caf0b-108">В командной строке с повышенными привилегиями введите:</span><span class="sxs-lookup"><span data-stu-id="caf0b-108">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="caf0b-109">PS &gt; **Set-AppvClientPackage $pkg – DynamicDeploymentConfiguration** &lt; путь к файлу конфигурации развертывания&gt;</span><span class="sxs-lookup"><span data-stu-id="caf0b-109">PS&gt;**Set-AppvClientPackage $pkg –DynamicDeploymentConfiguration** &lt;path to deployment configuration file&gt;</span></span>

    <span data-ttu-id="caf0b-110">PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfigurationType useDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="caf0b-110">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationType useDeploymentConfiguration**</span></span>

3.  <span data-ttu-id="caf0b-111">Выполните обновление публикации или дождитесь следующего запланированного обновления публикации для пакета App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="caf0b-111">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6 package.</span></span>

    <span data-ttu-id="caf0b-112">Откройте приложение с помощью FTAs или сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="caf0b-112">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="caf0b-113">Теперь приложение должно открываться с помощью App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="caf0b-113">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="caf0b-114">Примечание.</span><span class="sxs-lookup"><span data-stu-id="caf0b-114">Note</span></span>**  
    <span data-ttu-id="caf0b-115">Если вы больше не хотите использовать пакет App-V 5,1, вы можете отменить публикацию пакета App-V 5,1, а точки расширения будут автоматически возвращены в приложение App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="caf0b-115">If you do not need the App-V 5.1 package anymore, you can unpublish the App-V 5.1 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="caf0b-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="caf0b-116">Related topics</span></span>


[<span data-ttu-id="caf0b-117">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="caf0b-117">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









