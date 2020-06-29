---
title: Создание связывающей группы
description: Создание связывающей группы
author: dansimp
ms.assetid: 221e2eed-7ebb-42e3-b3d6-11c37c0578e6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f20b3e71c7c0b72d66700bbad945860112ffd03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814333"
---
# <span data-ttu-id="834fd-103">Создание связывающей группы</span><span class="sxs-lookup"><span data-stu-id="834fd-103">How to Create a Connection Group</span></span>


<span data-ttu-id="834fd-104">Выполните эти действия, чтобы создать группу подключений с помощью консоли управления App-V.</span><span class="sxs-lookup"><span data-stu-id="834fd-104">Use these steps to create a connection group by using the App-V Management Console.</span></span> <span data-ttu-id="834fd-105">Чтобы использовать PowerShell для создания групп подключений, ознакомьтесь со [сведениями о том, как управлять группами подключений на отдельном компьютере с помощью PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md).</span><span class="sxs-lookup"><span data-stu-id="834fd-105">To use PowerShell to create connection groups, see [How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md).</span></span>

<span data-ttu-id="834fd-106">Когда вы размещаете пакеты в группе подключений, их пути к корневому каталогу пакета объединяются.</span><span class="sxs-lookup"><span data-stu-id="834fd-106">When you place packages in a connection group, their package root paths are merged.</span></span> <span data-ttu-id="834fd-107">Если вы удалите пакеты, Объединенные корневые пакеты обслуживаются только в остальных пакетах.</span><span class="sxs-lookup"><span data-stu-id="834fd-107">If you remove packages, only the remaining packages maintain the merged root.</span></span>

**<span data-ttu-id="834fd-108">Создание группы подключения</span><span class="sxs-lookup"><span data-stu-id="834fd-108">To create a connection group</span></span>**

1.  <span data-ttu-id="834fd-109">В консоли управления App-V 5,1 выберите **группы подключения** , чтобы отобразить библиотеку групп подключения.</span><span class="sxs-lookup"><span data-stu-id="834fd-109">In the App-V 5.1 Management Console, select **CONNECTION GROUPS** to display the Connection Groups library.</span></span>

2.  <span data-ttu-id="834fd-110">Нажмите кнопку **Добавить группу подключения** , чтобы создать новую группу подключения.</span><span class="sxs-lookup"><span data-stu-id="834fd-110">Select **ADD CONNECTION GROUP** to create a new connection group.</span></span>

3.  <span data-ttu-id="834fd-111">В области **Новая группа подключения** введите описание группы.</span><span class="sxs-lookup"><span data-stu-id="834fd-111">In the **New Connection Group** pane, type a description for the group.</span></span>

4.  <span data-ttu-id="834fd-112">Нажмите кнопку **изменить** в области **подключенные пакеты** , чтобы добавить в группу Подключение новое приложение.</span><span class="sxs-lookup"><span data-stu-id="834fd-112">Click **EDIT** in the **CONNECTED PACKAGES** pane to add a new application to the connection group.</span></span>

5.  <span data-ttu-id="834fd-113">В области " **пакеты всей библиотеки** " выберите приложение, которое необходимо добавить, и щелкните стрелку, чтобы добавить приложение.</span><span class="sxs-lookup"><span data-stu-id="834fd-113">In the **PACKAGES Entire Library** pane, select the application to be added, and click the arrow to add the application.</span></span>

    <span data-ttu-id="834fd-114">Чтобы удалить приложение, выберите приложение, которое нужно удалить, в области **пакеты** и щелкните стрелку.</span><span class="sxs-lookup"><span data-stu-id="834fd-114">To remove an application, select the application to be removed in the **PACKAGES IN** pane and click the arrow.</span></span>

    <span data-ttu-id="834fd-115">Чтобы переустановить приоритеты приложений в группе "соединение", используйте стрелки в области " **пакеты** ".</span><span class="sxs-lookup"><span data-stu-id="834fd-115">To reprioritize the applications in your connection group, use the arrows in the **PACKAGES IN** pane.</span></span>

    <span data-ttu-id="834fd-116">**Важно!**  По умолчанию конфигурации доступа доменных служб Active Directory, связанные с определенным приложением, не добавляются в группу подключения.</span><span class="sxs-lookup"><span data-stu-id="834fd-116">**Important** By default, the Active Directory Domain Services access configurations that are associated with a specific application are not added to the connection group.</span></span> <span data-ttu-id="834fd-117">Чтобы перенести конфигурацию доступа в Active Directory, выберите **Добавить пакет доступ к группе**, которая находится в области **пакеты** .</span><span class="sxs-lookup"><span data-stu-id="834fd-117">To transfer the Active Directory access configuration, select **ADD PACKAGE ACCESS TO GROUP ACCESS**, which is located in the **PACKAGES IN** pane.</span></span>

     

6.  <span data-ttu-id="834fd-118">После добавления всех приложений и настройки доступа к Active Directory нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="834fd-118">After adding all the applications and configuring Active Directory access, click **Apply**.</span></span>

    <span data-ttu-id="834fd-119">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="834fd-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="834fd-120">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="834fd-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="834fd-121">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="834fd-121">Got an App-V issue?</span></span>** <span data-ttu-id="834fd-122">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="834fd-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="834fd-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="834fd-123">Related topics</span></span>


[<span data-ttu-id="834fd-124">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="834fd-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="834fd-125">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="834fd-125">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





