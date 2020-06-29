---
title: Удаление группы приложений
description: Удаление группы приложений
author: dansimp
ms.assetid: 3016b373-f5a0-4c82-96e8-e5e7960f0cc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b392fe84f4318cf7f355de0c07e4d6f1f5108ed7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816782"
---
# <span data-ttu-id="5564d-103">Удаление группы приложений</span><span class="sxs-lookup"><span data-stu-id="5564d-103">How to Remove an Application Group</span></span>


<span data-ttu-id="5564d-104">Вы можете использовать следующие процедуры для удаления группы приложения в консоли управления сервером виртуализации приложений одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="5564d-104">You can use the following procedures to remove an application group in the Application Virtualization Server Management Console in one of two ways:</span></span>

<span data-ttu-id="5564d-105">**Внимание!**  При удалении группы вместе с ее приложениями удаляются эти приложения с сервера управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="5564d-105">**Caution** Deleting a group with its applications deletes those applications from the Application Virtualization Management Server.</span></span> <span data-ttu-id="5564d-106">При попытке сделать это вы должны подтвердить удаление во всплывающем окне.</span><span class="sxs-lookup"><span data-stu-id="5564d-106">When you try to do this, you must confirm the deletion in a pop-up window.</span></span>

 

**<span data-ttu-id="5564d-107">Чтобы очистить и удалить группу приложения, выполните следующее.</span><span class="sxs-lookup"><span data-stu-id="5564d-107">To empty and then delete an application group</span></span>**

1.  <span data-ttu-id="5564d-108">В консоли Управление сервером виртуализации приложений разверните раздел **приложения** на левой панели и выберите группу **приложений** , которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="5564d-108">In the Application Virtualization Server Management Console, expand **Applications** in the left pane and select the **Application** group you want to remove.</span></span>

2.  <span data-ttu-id="5564d-109">В области справа выберите приложения и группы приложений, которые вы хотите сохранить.</span><span class="sxs-lookup"><span data-stu-id="5564d-109">In the right pane, select the applications and application groups you want to keep.</span></span> <span data-ttu-id="5564d-110">Вы можете выбрать несколько приложений и групп приложений с помощью клавиш **CTRL** и **SHIFT** .</span><span class="sxs-lookup"><span data-stu-id="5564d-110">You can use the **CTRL** and **Shift** keys to select multiple applications and application groups.</span></span>

3.  <span data-ttu-id="5564d-111">Щелкните выбранные приложения правой кнопкой мыши и выберите пункт **переместить**.</span><span class="sxs-lookup"><span data-stu-id="5564d-111">Right-click the selected applications, and choose **Move**.</span></span>

4.  <span data-ttu-id="5564d-112">В окне **Выбор целевого объекта** перейдите к новому расположению и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5564d-112">In the **Select Target** window, navigate to the new location and click **OK**.</span></span> <span data-ttu-id="5564d-113">Повторите это действие, если вы хотите переместить различные приложения в несколько групп.</span><span class="sxs-lookup"><span data-stu-id="5564d-113">Repeat this step if you want to move different applications to more than one group.</span></span>

5.  <span data-ttu-id="5564d-114">Когда вы закончите перенос приложений, которые нужно сохранить, щелкните правой кнопкой мыши группу приложения и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="5564d-114">When you finish moving the applications you want to keep, right-click the application group and choose **Delete**.</span></span>

6.  <span data-ttu-id="5564d-115">Нажмите кнопку **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5564d-115">Click **Yes** to confirm.</span></span>

**<span data-ttu-id="5564d-116">Удаление группы со всеми ее дочерними группами и ее приложениями</span><span class="sxs-lookup"><span data-stu-id="5564d-116">To delete the group, with all its child groups and its applications</span></span>**

1.  <span data-ttu-id="5564d-117">В консоли Управление сервером виртуализации приложений разверните раздел **приложения** на левой панели.</span><span class="sxs-lookup"><span data-stu-id="5564d-117">In the Application Virtualization Server Management Console, expand **Applications** in the left pane.</span></span>

2.  <span data-ttu-id="5564d-118">Щелкните правой кнопкой мыши группу приложений, которую вы хотите удалить, и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="5564d-118">Right-click the application group you want to remove, and choose **Delete**.</span></span>

3.  <span data-ttu-id="5564d-119">Нажмите кнопку **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5564d-119">Click **Yes** to confirm.</span></span>

    <span data-ttu-id="5564d-120">**Примечание**  Вы можете выбрать и удалить несколько групп приложения одновременно.</span><span class="sxs-lookup"><span data-stu-id="5564d-120">**Note** You can select and remove multiple application groups simultaneously.</span></span> <span data-ttu-id="5564d-121">В области справа щелкните сочетание клавиш, удерживая нажатой **клавишу CTRL**или **SHIFT**, чтобы выбрать несколько групп.</span><span class="sxs-lookup"><span data-stu-id="5564d-121">In the right pane, use the **CTRL**-click or **Shift**-click key combinations to select more than one group.</span></span>

     

## <span data-ttu-id="5564d-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5564d-122">Related topics</span></span>


[<span data-ttu-id="5564d-123">Управление группами приложений на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="5564d-123">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="5564d-124">Управление приложениями на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="5564d-124">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





