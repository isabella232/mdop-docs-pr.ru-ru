---
ms.reviewer: ''
title: Использование приложения App-V 4,6 из приложения App-V 5,0
description: Использование приложения App-V 4,6 из приложения App-V 5,0
ms.assetid: 4e78cb32-9c8b-478e-ae8b-c474a7e42487
author: msfttracyp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 8b29e861b97d18e427f6a8247a1f731be2dc0889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813645"
---
# <span data-ttu-id="4b4a6-103">Использование приложения App-V 4,6 из приложения App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="4b4a6-103">How to Use an App-V 4.6 Application From an App-V 5.0 Application</span></span>

<span data-ttu-id="4b4a6-104">*Примечание:*\* App-V 4,6 вышел из основной поддержки.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="4b4a6-105">Указанные ниже инструкции относятся к пакету приложения App-V 4,6 с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="4b4a6-105">The following applies to an App-V 4.6 SP3 package.</span></span>

<span data-ttu-id="4b4a6-106">Чтобы запустить приложение App-V 4.6 с приложениями App-V 5,0 на отдельном клиенте, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-106">Use the following procedure to run an App-V4.6 application with App-V 5.0 applications on a standalone client.</span></span>

**<span data-ttu-id="4b4a6-107">Запуск приложений на автономном клиенте</span><span class="sxs-lookup"><span data-stu-id="4b4a6-107">To run applications on a standalone client</span></span>**

1.  <span data-ttu-id="4b4a6-108">Выберите в среде два приложения, которые можно открывать друг от друга.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-108">Select two applications in your environment that can be opened from one another.</span></span> <span data-ttu-id="4b4a6-109">Например, Microsoft Outlook и Adobe Acrobat Reader.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-109">For example, Microsoft Outlook and Adobe Acrobat Reader.</span></span> <span data-ttu-id="4b4a6-110">Вы можете получить доступ к вложению электронной почты, созданному с помощью Adobe Acrobat.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-110">You can access an email attachment created using Adobe Acrobat.</span></span>

2.  <span data-ttu-id="4b4a6-111">Преобразуйте пакеты или создайте новый пакет для любого из приложений, использующих формат App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-111">Convert the packages, or create a new package for either of the applications using the App-V 5.0 format.</span></span> <span data-ttu-id="4b4a6-112">Дополнительные сведения о преобразовании пакетов можно найти в разделе [как переносить точки расширения из пакета App-v 4,6 в преобразованный пакет App-v 5,0 для всех пользователей на определенном компьютере](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) или [переносить точки расширения из пакета app-v 4,6 в приложение app-v 5,0 для определенного пользователя](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="4b4a6-112">For more information about converting packages see, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) or [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span></span>

3.  <span data-ttu-id="4b4a6-113">Добавьте и подготовьте пакет с помощью консоли управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-113">Add and provision the package using the App-V 5.0 management console.</span></span> <span data-ttu-id="4b4a6-114">Дополнительные сведения о добавлении и подготовке пакетов можно найти в разделе [Добавление и обновление пакетов с помощью консоли управления](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) и [Настройка доступа к пакетам с помощью консоли управления](how-to-configure-access-to-packages-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="4b4a6-114">For more information adding and provisioning packages see, [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) and [How to Configure Access to Packages by Using the Management Console](how-to-configure-access-to-packages-by-using-the-management-console-50.md).</span></span>

4.  <span data-ttu-id="4b4a6-115">Преобразованное приложение теперь запускается с помощью App-V 5,0, и вы можете открыть одно приложение из другого.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-115">The converted application now runs using App-V 5.0 and you can open one application from the other.</span></span> <span data-ttu-id="4b4a6-116">Например, если вы преобразовали пакет Microsoft Office в пакет App-V 5,0, а приложение Adobe Acrobat по-прежнему работает как пакет App-V 4.6, вы можете открыть вложение Adobe Acrobat Reader с помощью Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-116">For example, if you converted a Microsoft Office package to an App-V 5.0 package and Adobe Acrobat is still running as an App-V4.6 package, you can open an Adobe Acrobat Reader attachment using Microsoft Outlook.</span></span>

    <span data-ttu-id="4b4a6-117">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="4b4a6-117">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="4b4a6-118">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="4b4a6-118">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="4b4a6-119">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="4b4a6-119">Got an App-V issue?</span></span>** <span data-ttu-id="4b4a6-120">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="4b4a6-120">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="4b4a6-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4b4a6-121">Related topics</span></span>


[<span data-ttu-id="4b4a6-122">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="4b4a6-122">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 








