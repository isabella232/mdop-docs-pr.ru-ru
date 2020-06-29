---
title: Использование пользовательского интерфейса консоли управления MED-V
description: Использование пользовательского интерфейса консоли управления MED-V
author: dansimp
ms.assetid: f42714d7-6f0c-4995-ab31-d4ef0845a22c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22fc98c3edbea48847e1a00369bea21a470e66b7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825849"
---
# <span data-ttu-id="d7426-103">Использование пользовательского интерфейса консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="d7426-103">Using the MED-V Management Console User Interface</span></span>


<span data-ttu-id="d7426-104">Пользовательский интерфейс консоли делится на следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="d7426-104">The console user interface is divided into the following sections:</span></span>

-   <span data-ttu-id="d7426-105">Следующие **кнопки управления MED-V**, соответствующие трем модулям:</span><span class="sxs-lookup"><span data-stu-id="d7426-105">The following **MED-V management buttons**, which correspond to the three modules:</span></span>

    -   <span data-ttu-id="d7426-106">**Политика**— модуль **политики** используется для определения рабочих областей MED-V и связанных с ними параметров и разрешений.</span><span class="sxs-lookup"><span data-stu-id="d7426-106">**Policy**—The **Policy** module is used to define the MED-V workspaces and their related settings and permissions.</span></span>

    -   <span data-ttu-id="d7426-107">**Изображения**— модуль **Images** используется для управления изображениями рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="d7426-107">**Images**—The **Images** module is used to manage MED-V workspace images.</span></span>

    -   <span data-ttu-id="d7426-108">**Отчеты**— модуль " **отчеты** " используется для создания и просмотра отчетов о рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="d7426-108">**Reports**—The **Reports** module is used for generating and viewing MED-V workspace reports.</span></span>

-   <span data-ttu-id="d7426-109">На **панели инструментов** отображаются сочетания клавиш, связанные с выбранной кнопкой.</span><span class="sxs-lookup"><span data-stu-id="d7426-109">The **toolbar** displays shortcuts relevant to the button selected.</span></span>

-   <span data-ttu-id="d7426-110">В **области отображения** отображается модуль, соответствующий выбранной кнопке.</span><span class="sxs-lookup"><span data-stu-id="d7426-110">The **display pane** displays a module corresponding to the button that is selected.</span></span>

![](images/medv-ui-console-general.gif)

## <span data-ttu-id="d7426-111">Вход в консоль управления MED-V</span><span class="sxs-lookup"><span data-stu-id="d7426-111">How to Log In to the MED-V Management Console</span></span>


**<span data-ttu-id="d7426-112">Открытие консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="d7426-112">To open the MED-V management console</span></span>**

-   <span data-ttu-id="d7426-113">В меню **Пуск** Windows выберите **все программы, &gt; &gt; Управление**med-v, или на рабочем столе дважды щелкните значок Управление med-v.</span><span class="sxs-lookup"><span data-stu-id="d7426-113">On the Windows **Start** menu, select **All Programs &gt; MED-V &gt; MED-V Management**, or on the desktop, double-click the MED-V Management icon.</span></span>

    <span data-ttu-id="d7426-114">Откроется окно **входа в систему управления MED-V** .</span><span class="sxs-lookup"><span data-stu-id="d7426-114">The **MED-V Management Login** window appears.</span></span>

<span data-ttu-id="d7426-115">**Примечание**  В целях обеспечения безопасности первый пользователь, который должен войти в консоль управления MED-V, станет единственным пользователем на этом компьютере, которому разрешен доступ к консоли управления.</span><span class="sxs-lookup"><span data-stu-id="d7426-115">**Note** For security reasons, the first user to log in to the MED-V management console will become the only user on that computer allowed to access the management console.</span></span>

 

**<span data-ttu-id="d7426-116">Для входа в систему</span><span class="sxs-lookup"><span data-stu-id="d7426-116">To log in</span></span>**

1.  <span data-ttu-id="d7426-117">Введите свои учетные данные пользователя домена в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="d7426-117">Type in your domain user credentials in the following format:</span></span>

    <span data-ttu-id="d7426-118">"Domain \ _name \\user\ _name", "пароль"</span><span class="sxs-lookup"><span data-stu-id="d7426-118">"domain\_name\\user\_name", "password"</span></span>

    <span data-ttu-id="d7426-119">**Примечание**  При настройке сервера пользователи с полным доступом и пользователи с доступом только для чтения определяются.</span><span class="sxs-lookup"><span data-stu-id="d7426-119">**Note** When configuring the server, users with full access as well as users with read-only access are defined.</span></span> <span data-ttu-id="d7426-120">Все пользователи должны быть пользователями домена.</span><span class="sxs-lookup"><span data-stu-id="d7426-120">All users must be domain users.</span></span> <span data-ttu-id="d7426-121">Имя пользователя и пароль домена используются для входа в систему управления MED-V.</span><span class="sxs-lookup"><span data-stu-id="d7426-121">The domain user name and password is used for MED-V management login.</span></span>

     

2.  <span data-ttu-id="d7426-122">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d7426-122">Click **OK**.</span></span>

    <span data-ttu-id="d7426-123">Появится консоль **управления MED-V** .</span><span class="sxs-lookup"><span data-stu-id="d7426-123">The **MED-V Management** console appears.</span></span>

## <span data-ttu-id="d7426-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d7426-124">Related topics</span></span>


[<span data-ttu-id="d7426-125">Установка клиента MED-V и консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="d7426-125">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

 

 





