---
title: Добавление или удаление администратора с помощью консоли управления
description: Добавление или удаление администратора с помощью консоли управления
author: dansimp
ms.assetid: 7ff8c436-9d2e-446a-9ea2-bbab7e25bf21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8fbc1a532a39c8688b99c28a2e23b713b348967c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814493"
---
# <span data-ttu-id="4c2c7-103">Добавление или удаление администратора с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="4c2c7-103">How to Add or Remove an Administrator by Using the Management Console</span></span>


<span data-ttu-id="4c2c7-104">Чтобы добавить или удалить администратора на сервере Microsoft Application Virtualization (App-V) 5,1, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4c2c7-104">Use the following procedures to add or remove an administrator on the Microsoft Application Virtualization (App-V) 5.1 server.</span></span>

**<span data-ttu-id="4c2c7-105">Добавление администратора с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="4c2c7-105">To add an administrator using the Management Console</span></span>**

1.  <span data-ttu-id="4c2c7-106">Откройте консоль управления Microsoft Application Virtualization (App-V) 5,1 и выберите в области навигации пункт **Администраторы** .</span><span class="sxs-lookup"><span data-stu-id="4c2c7-106">Open the Microsoft Application Virtualization (App-V) 5.1 Management Console and click **Administrators** in the navigation pane.</span></span> <span data-ttu-id="4c2c7-107">В области навигации отображается список пользователей и групп Active Directory, у которых в настоящее время есть административный доступ к Microsoft Application Virtualization (App-V) 5,1 Server.</span><span class="sxs-lookup"><span data-stu-id="4c2c7-107">The navigation pane displays a list of Access Directory (AD) users and groups that currently have administrative access to the Microsoft Application Virtualization (App-V) 5.1 server.</span></span>

2.  <span data-ttu-id="4c2c7-108">Чтобы добавить нового администратора, нажмите кнопку **Добавить администратора** , введите имя администратора, которого вы хотите добавить в поле **имя Active Directory** .</span><span class="sxs-lookup"><span data-stu-id="4c2c7-108">To add a new administrator, click **Add Administrator** Type the name of the administrator that you want to add in the **Active Directory Name** field.</span></span> <span data-ttu-id="4c2c7-109">Убедитесь, что вы предоставляли соответствующее имя домена учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c2c7-109">Ensure you provide the associated user account domain name.</span></span> <span data-ttu-id="4c2c7-110">Например, **Domain**  \\  **имя пользователя**домена.</span><span class="sxs-lookup"><span data-stu-id="4c2c7-110">For example, **Domain** \\ **UserName**.</span></span>

3.  <span data-ttu-id="4c2c7-111">Выберите учетную запись, которую вы хотите добавить, и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="4c2c7-111">Select the account that you want to add and click **Add**.</span></span> <span data-ttu-id="4c2c7-112">Новая учетная запись появится в списке администраторов сервера.</span><span class="sxs-lookup"><span data-stu-id="4c2c7-112">The new account is displayed in the list of server administrators.</span></span>

**<span data-ttu-id="4c2c7-113">Удаление администратора с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="4c2c7-113">To remove an administrator using the Management Console</span></span>**

1.  <span data-ttu-id="4c2c7-114">Откройте консоль управления Microsoft Application Virtualization (App-V) 5,1 и выберите в области навигации пункт **Администраторы** .</span><span class="sxs-lookup"><span data-stu-id="4c2c7-114">Open the Microsoft Application Virtualization (App-V) 5.1 Management Console and click **Administrators** in the navigation pane.</span></span> <span data-ttu-id="4c2c7-115">В области навигации отображается список пользователей и групп, в которых в настоящее время есть административный доступ к Microsoft Application Virtualization (App-V) 5,1 Server.</span><span class="sxs-lookup"><span data-stu-id="4c2c7-115">The navigation pane displays a list of AD users and groups that currently have administrative access to the Microsoft Application Virtualization (App-V) 5.1 server.</span></span>

2.  <span data-ttu-id="4c2c7-116">Щелкните правой кнопкой мыши учетную запись, которую вы хотите удалить из списка администраторов, и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="4c2c7-116">Right-click the account to be removed from the list of administrators and select **Remove**.</span></span>

    <span data-ttu-id="4c2c7-117">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="4c2c7-117">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="4c2c7-118">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="4c2c7-118">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="4c2c7-119">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="4c2c7-119">Got an App-V issue?</span></span>** <span data-ttu-id="4c2c7-120">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="4c2c7-120">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="4c2c7-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4c2c7-121">Related topics</span></span>


[<span data-ttu-id="4c2c7-122">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4c2c7-122">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





