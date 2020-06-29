---
title: Создание рабочей области MED-V
description: Создание рабочей области MED-V
author: dansimp
ms.assetid: 9578bb99-8a09-44c1-b88f-538901f16ad3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 189da6b28515f0d234c8a258138a27be7a7375d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824862"
---
# <span data-ttu-id="b51c1-103">Создание рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="b51c1-103">Creating a MED-V Workspace</span></span>


<span data-ttu-id="b51c1-104">Рабочая область MED-V — это классическое окружение, в котором конечные пользователи взаимодействуют с виртуальной машиной, предоставляемой MED-V.</span><span class="sxs-lookup"><span data-stu-id="b51c1-104">A MED-V workspace is the desktop environment in which end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="b51c1-105">Рабочая область MED-V создается и настраивается администратором.</span><span class="sxs-lookup"><span data-stu-id="b51c1-105">The MED-V workspace is created and customized by the administrator.</span></span> <span data-ttu-id="b51c1-106">Она состоит из изображения и политики, которые определяют правила и функциональные возможности рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="b51c1-106">It consists of an image and the policy, which defines the rules and functionality of the MED-V workspace.</span></span> <span data-ttu-id="b51c1-107">Можно создавать несколько рабочих областей MED-V, каждый из которых настроен с помощью собственной конфигурации, параметров и правил.</span><span class="sxs-lookup"><span data-stu-id="b51c1-107">Multiple MED-V workspaces can be created, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="b51c1-108">Пользователь, группа или несколько пользователей или групп могут быть связаны с каждой рабочей областью MED-V, тем самым обеспечивая доступ к рабочей области MED-V только для компьютеров пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="b51c1-108">A user, group, or multiple users or groups can be associated with each MED-V workspace, thereby making the MED-V workspace available only for the associated user's or group's computers.</span></span>

## <span data-ttu-id="b51c1-109">Добавление рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="b51c1-109">How to Add a MED-V Workspace</span></span>


**<span data-ttu-id="b51c1-110">Добавление рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="b51c1-110">To add a MED-V workspace</span></span>**

1.  <span data-ttu-id="b51c1-111">Нажмите кнопку Управление **политиками** , чтобы открыть модуль **политики** .</span><span class="sxs-lookup"><span data-stu-id="b51c1-111">Click the **Policy** management button to open the **Policy** module.</span></span>

    <span data-ttu-id="b51c1-112">Модуль **политики** состоит из меню " **рабочие области** " на вкладке " **Общие**", " **виртуальные машины**", " **развертывание**" **Web** **, "** сетевые параметры", " **Настройка**", " **сеть**" и " **производительность** ".</span><span class="sxs-lookup"><span data-stu-id="b51c1-112">The **Policy** module consists of the **Workspaces** menu on the left and the **General**, **Virtual Machine**, **Deployment**, **Applications**, **Web**, **VM Setup**, **Network**, and **Performance** tabs.</span></span>

2.  <span data-ttu-id="b51c1-113">В меню **Политика** выберите пункт **создать рабочую область**или нажмите кнопку **добавить** , чтобы создать новую рабочую область для MED-V.</span><span class="sxs-lookup"><span data-stu-id="b51c1-113">On the **Policy** menu, select **New Workspace**, or click **Add** to create a new MED-V workspace.</span></span>

3.  <span data-ttu-id="b51c1-114">На вкладке **Общие** в поле **имя** введите имя рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="b51c1-114">On the **General** tab, in the **Name** field, enter the name of the MED-V workspace.</span></span>

4.  <span data-ttu-id="b51c1-115">В поле **Описание** введите описание рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="b51c1-115">In the **Description** field, enter a description for the MED-V workspace.</span></span>

5.  <span data-ttu-id="b51c1-116">В поле **контактные данные службы поддержки** введите контактные данные для службы технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="b51c1-116">In the **Support contact info** field, enter the contact information for technical support.</span></span>

    <span data-ttu-id="b51c1-117">Дополнительные сведения о настройке рабочей области MED-V можно найти в разделе [Настройка политик рабочих областей для MED-v](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b51c1-117">For more information about configuring a MED-V workspace, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

## <span data-ttu-id="b51c1-118">Клонирование рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="b51c1-118">How to Clone a MED-V Workspace</span></span>


<span data-ttu-id="b51c1-119">Рабочую область MED-V можно клонировать таким образом, чтобы можно было создать рабочую область MED-V, идентичную существующей рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="b51c1-119">A MED-V workspace can be cloned so that you can create a MED-V workspace identical to an existing MED-V workspace.</span></span>

**<span data-ttu-id="b51c1-120">Клонирование рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="b51c1-120">To clone a MED-V workspace</span></span>**

1.  <span data-ttu-id="b51c1-121">Щелкните рабочую область MED-V, чтобы клонировать ее.</span><span class="sxs-lookup"><span data-stu-id="b51c1-121">Click the MED-V workspace to clone.</span></span>

2.  <span data-ttu-id="b51c1-122">В меню **Политика** выберите команду **клонировать рабочую область**.</span><span class="sxs-lookup"><span data-stu-id="b51c1-122">On the **Policy** menu, select **Clone Workspace**.</span></span>

    <span data-ttu-id="b51c1-123">Будет создана новая Рабочая область MED-V с именем &lt; исходного рабочего пространства MED-v &gt; -2.</span><span class="sxs-lookup"><span data-stu-id="b51c1-123">A new MED-V workspace is created with the name &lt;Original MED-V workspace name&gt; - 2.</span></span>

## <span data-ttu-id="b51c1-124">Удаление рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="b51c1-124">How to Delete a MED-V Workspace</span></span>


**<span data-ttu-id="b51c1-125">Удаление рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="b51c1-125">To delete a MED-V workspace</span></span>**

-   <span data-ttu-id="b51c1-126">В разделе Рабочая область в модуле **политики** нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="b51c1-126">In the **Policy** module, while the workspace pane is in focus, click **Remove**.</span></span>

## <span data-ttu-id="b51c1-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b51c1-127">Related topics</span></span>


[<span data-ttu-id="b51c1-128">Использование пользовательского интерфейса консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="b51c1-128">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





