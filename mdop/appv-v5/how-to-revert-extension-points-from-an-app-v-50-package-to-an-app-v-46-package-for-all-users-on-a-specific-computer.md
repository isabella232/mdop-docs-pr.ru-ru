---
title: Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для всех пользователей на указанном компьютере
description: Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для всех пользователей на указанном компьютере
ms.assetid: 2a43ca1b-6847-4dd1-ade2-336ac4ac6af0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 62542e5cd0b9dcb55f6e8f3db4d4f43c011a2839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813728"
---
# <span data-ttu-id="b0414-103">Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для всех пользователей на указанном компьютере</span><span class="sxs-lookup"><span data-stu-id="b0414-103">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>

<span data-ttu-id="b0414-104">*Примечание:*\* App-V 4,6 вышел из основной поддержки.</span><span class="sxs-lookup"><span data-stu-id="b0414-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="b0414-105">В следующем примере предполагается, что клиент App-V 4,6 с пакетом обновления 3 (SP3) уже установлен.</span><span class="sxs-lookup"><span data-stu-id="b0414-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="b0414-106">Используйте описанную ниже процедуру, чтобы вернуть точки расширения из пакета App-V 5,0 в формат файлов App-V 4,6 с помощью файла конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="b0414-106">Use the following procedure to revert extension points from an App-V 5.0 package to the App-V 4.6 file format using the deployment configuration file.</span></span>

**<span data-ttu-id="b0414-107">Отмена пакета</span><span class="sxs-lookup"><span data-stu-id="b0414-107">To revert a package</span></span>**

1.  <span data-ttu-id="b0414-108">Убедитесь в том, что пакет App-V 4,6 опубликован для пользователей, но FTAs и сочетания клавиш предполагаются пакетом App-V 5,0 с помощью следующего метода миграции, [чтобы переносить точки расширения из пакета App-v 4,6 в преобразованный пакет App-v 5,0 для всех пользователей на определенном компьютере](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).</span><span class="sxs-lookup"><span data-stu-id="b0414-108">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.0 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).</span></span>

    <span data-ttu-id="b0414-109">В разделе **userConfiguration** файла конфигурации развертывания для преобразованного пакета, чтобы настроить политику, сделайте следующее обновление в разделе **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "ложь" PackageName = &lt; ИД &gt; пакета**</span><span class="sxs-lookup"><span data-stu-id="b0414-109">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="b0414-110">В командной строке с повышенными привилегиями введите:</span><span class="sxs-lookup"><span data-stu-id="b0414-110">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="b0414-111">PS &gt; **Set-AppvClientPackage $pkg – DynamicDeploymentConfiguration** &lt; путь к файлу конфигурации развертывания&gt;</span><span class="sxs-lookup"><span data-stu-id="b0414-111">PS&gt;**Set-AppvClientPackage $pkg –DynamicDeploymentConfiguration** &lt;path to deployment configuration file&gt;</span></span>

    <span data-ttu-id="b0414-112">PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfigurationType useDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="b0414-112">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationType useDeploymentConfiguration**</span></span>

3.  <span data-ttu-id="b0414-113">Выполните обновление публикации или дождитесь следующего запланированного обновления публикации для пакета App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="b0414-113">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6 SP2 package.</span></span>

    <span data-ttu-id="b0414-114">Откройте приложение с помощью FTAs или сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="b0414-114">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="b0414-115">Теперь приложение должно открываться с помощью App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="b0414-115">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="b0414-116">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b0414-116">Note</span></span>**  
    <span data-ttu-id="b0414-117">Если вы больше не хотите использовать пакет App-V 5,0, вы можете отменить публикацию пакета App-V 5,0, а точки расширения будут автоматически возвращены в приложение App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="b0414-117">If you do not need the App-V 5.0 package anymore, you can unpublish the App-V 5.0 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="b0414-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b0414-118">Related topics</span></span>


[<span data-ttu-id="b0414-119">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b0414-119">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









