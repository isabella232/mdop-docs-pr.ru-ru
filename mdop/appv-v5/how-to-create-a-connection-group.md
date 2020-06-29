---
title: Создание связывающей группы
description: Создание связывающей группы
author: dansimp
ms.assetid: 9d272052-2d28-4e41-989c-89610482a0ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 816fc3b37be056ed54a88c394ef64fa1edaf47ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814341"
---
# <span data-ttu-id="ee3e7-103">Создание связывающей группы</span><span class="sxs-lookup"><span data-stu-id="ee3e7-103">How to Create a Connection Group</span></span>


<span data-ttu-id="ee3e7-104">Выполните эти действия, чтобы создать группу подключений с помощью консоли управления App-V.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-104">Use these steps to create a connection group by using the App-V Management Console.</span></span> <span data-ttu-id="ee3e7-105">Чтобы использовать PowerShell для создания групп подключений, ознакомьтесь со [сведениями о том, как управлять группами подключений на отдельном компьютере с помощью PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="ee3e7-105">To use PowerShell to create connection groups, see [How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).</span></span>

<span data-ttu-id="ee3e7-106">Когда вы размещаете пакеты в группе подключений, их пути к корневому каталогу пакета объединяются.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-106">When you place packages in a connection group, their package root paths are merged.</span></span> <span data-ttu-id="ee3e7-107">Если вы удалите пакеты, Объединенные корневые пакеты обслуживаются только в остальных пакетах.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-107">If you remove packages, only the remaining packages maintain the merged root.</span></span>

**<span data-ttu-id="ee3e7-108">Создание группы подключения</span><span class="sxs-lookup"><span data-stu-id="ee3e7-108">To create a connection group</span></span>**

1.  <span data-ttu-id="ee3e7-109">В консоли управления App-V 5,0 выберите **Packages (пакеты**).</span><span class="sxs-lookup"><span data-stu-id="ee3e7-109">In the App-V 5.0 Management Console, select **Packages**.</span></span>

2.  <span data-ttu-id="ee3e7-110">Выберите **группы подключений** , чтобы отобразить библиотеку групп подключения.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-110">Select **CONNECTION GROUPS** to display the Connection Groups library.</span></span>

3.  <span data-ttu-id="ee3e7-111">Нажмите кнопку **Добавить группу подключения** , чтобы создать новую группу подключения.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-111">Select **ADD CONNECTION GROUP** to create a new connection group.</span></span>

4.  <span data-ttu-id="ee3e7-112">В области **Новая группа подключения** введите описание группы.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-112">In the **New Connection Group** pane, type a description for the group.</span></span>

5.  <span data-ttu-id="ee3e7-113">Нажмите кнопку **изменить** в области **подключенные пакеты** , чтобы добавить в группу Подключение новое приложение.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-113">Click **EDIT** in the **CONNECTED PACKAGES** pane to add a new application to the connection group.</span></span>

6.  <span data-ttu-id="ee3e7-114">В области " **пакеты всей библиотеки** " выберите приложение, которое необходимо добавить, и щелкните стрелку, чтобы добавить приложение.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-114">In the **PACKAGES Entire Library** pane, select the application to be added, and click the arrow to add the application.</span></span>

    <span data-ttu-id="ee3e7-115">Чтобы удалить приложение, выберите приложение, которое нужно удалить, в области **пакеты** и щелкните стрелку.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-115">To remove an application, select the application to be removed in the **PACKAGES IN** pane and click the arrow.</span></span>

    <span data-ttu-id="ee3e7-116">Чтобы переустановить приоритеты приложений в группе "соединение", используйте стрелки в области " **пакеты** ".</span><span class="sxs-lookup"><span data-stu-id="ee3e7-116">To reprioritize the applications in your connection group, use the arrows in the **PACKAGES IN** pane.</span></span>

    <span data-ttu-id="ee3e7-117">**Важно!**  По умолчанию конфигурации доступа доменных служб Active Directory, связанные с определенным приложением, не добавляются в группу подключения.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-117">**Important** By default, the Active Directory Domain Services access configurations that are associated with a specific application are not added to the connection group.</span></span> <span data-ttu-id="ee3e7-118">Чтобы перенести конфигурацию доступа в Active Directory, выберите **Добавить пакет доступ к группе**, которая находится в области **пакеты** .</span><span class="sxs-lookup"><span data-stu-id="ee3e7-118">To transfer the Active Directory access configuration, select **ADD PACKAGE ACCESS TO GROUP ACCESS**, which is located in the **PACKAGES IN** pane.</span></span>

     

7.  <span data-ttu-id="ee3e7-119">После добавления всех приложений и настройки доступа к Active Directory нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-119">After adding all the applications and configuring Active Directory access, click **Apply**.</span></span>

    <span data-ttu-id="ee3e7-120">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="ee3e7-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="ee3e7-121">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="ee3e7-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="ee3e7-122">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="ee3e7-122">Got an App-V issue?</span></span>** <span data-ttu-id="ee3e7-123">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ee3e7-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ee3e7-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ee3e7-124">Related topics</span></span>


[<span data-ttu-id="ee3e7-125">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ee3e7-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="ee3e7-126">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="ee3e7-126">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





