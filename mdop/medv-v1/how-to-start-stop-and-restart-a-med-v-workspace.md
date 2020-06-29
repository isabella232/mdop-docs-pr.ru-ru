---
title: Запуск, остановка и перезапуск рабочей области MED-V
description: Запуск, остановка и перезапуск рабочей области MED-V
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825722"
---
# <span data-ttu-id="c5352-103">Запуск, остановка и перезапуск рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="c5352-103">How to Start, Stop, and Restart a MED-V Workspace</span></span>


**<span data-ttu-id="c5352-104">Начало работы с рабочей областью MED-V</span><span class="sxs-lookup"><span data-stu-id="c5352-104">To start a MED-V workspace</span></span>**

1.  <span data-ttu-id="c5352-105">В области уведомлений щелкните правой кнопкой мыши значок MED-V.</span><span class="sxs-lookup"><span data-stu-id="c5352-105">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="c5352-106">В подменю выберите команду **запустить рабочую область**.</span><span class="sxs-lookup"><span data-stu-id="c5352-106">On the submenu, click **Start Workspace**.</span></span>

    -   <span data-ttu-id="c5352-107">Если на компьютере запущено несколько рабочих областей MED-V, откроется окно **Выбор рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="c5352-107">If there are multiple MED-V workspaces running on the computer, the **Workspace Selection** window appears.</span></span>

        1.  <span data-ttu-id="c5352-108">Выберите рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="c5352-108">Select a MED-V workspace.</span></span>

        2.  <span data-ttu-id="c5352-109">Установите флажок **запускать выбранную рабочую область без запроса** , чтобы пропустить это окно при следующем запуске клиента и автоматически открыть выбранную рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="c5352-109">Select the **Start the selected Workspace without asking me** check box to skip this window the next time the client is started and to automatically open the selected MED-V workspace.</span></span>

        3.  <span data-ttu-id="c5352-110">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c5352-110">Click **OK**.</span></span>

    <span data-ttu-id="c5352-111">Откроется окно **Запуск проверки подлинности рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="c5352-111">The **Start Workspace Authentication** window appears.</span></span>

    -   <span data-ttu-id="c5352-112">Если на компьютере установлено несколько рабочих областей MED-V и вы выбрали использование указанной рабочей области MED-V, появится окно, показанное на приведенном ниже рисунке.</span><span class="sxs-lookup"><span data-stu-id="c5352-112">If there are several MED-V workspaces on the computer and you have opted to use a specified MED-V workspace, the window shown in the following figure appears.</span></span>

        ![](images/medv-logon.gif)

    -   <span data-ttu-id="c5352-113">Если на компьютере установлено только одно рабочее пространство MED-V, параметр "начать последнюю использованную рабочую область" недоступен.</span><span class="sxs-lookup"><span data-stu-id="c5352-113">If there is only one MED-V workspace on the computer, the “Start last used Workspace” option is unavailable.</span></span>

3.  <span data-ttu-id="c5352-114">Введите свои учетные данные пользователя домена.</span><span class="sxs-lookup"><span data-stu-id="c5352-114">Type in your domain user credentials.</span></span>

    <span data-ttu-id="c5352-115">**Примечание**  При первом запуске рабочей области для MED-V имя пользователя должно быть представлено в следующем формате: &lt; доменное имя &gt; \\ &lt; пользователя &gt; .</span><span class="sxs-lookup"><span data-stu-id="c5352-115">**Note** The first time a MED-V workspace is started, the user name should be in the following format: &lt;domain name&gt;\\&lt;user name&gt;.</span></span>

     

4.  <span data-ttu-id="c5352-116">Выберите **Сохранить пароль** , чтобы сохранить пароль между сеансами.</span><span class="sxs-lookup"><span data-stu-id="c5352-116">Select **Save my password** to save your password between sessions.</span></span>

    <span data-ttu-id="c5352-117">**Примечание**  Чтобы включить функцию сохранения пароля, атрибуту EnableSavePassword в файле ClientSettings.xml должно быть присвоено значение true.</span><span class="sxs-lookup"><span data-stu-id="c5352-117">**Note** To enable the save password feature, the EnableSavePassword attribute must be set to True in the ClientSettings.xml file.</span></span> <span data-ttu-id="c5352-118">Файл можно найти в папке *Servers\\Configuration Server\\* .</span><span class="sxs-lookup"><span data-stu-id="c5352-118">The file can be found in the *Servers\\Configuration Server\\* folder.</span></span>

     

5.  <span data-ttu-id="c5352-119">Снимите флажок **начать последнюю использованную рабочую область** , чтобы выбрать другую рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="c5352-119">Clear the **Start last used workspace** check box to choose a different MED-V workspace.</span></span>

6.  <span data-ttu-id="c5352-120">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c5352-120">Click **OK**.</span></span>

    <span data-ttu-id="c5352-121">Некоторые экраны состояния отображаются в зависимости от конфигурации рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="c5352-121">Several status screens appear depending on the MED-V workspace configuration.</span></span>

    <span data-ttu-id="c5352-122">Откроется окно **начальной рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="c5352-122">The **Starting Workspace** screen appears.</span></span>

**<span data-ttu-id="c5352-123">Перезапуск рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="c5352-123">To restart a MED-V workspace</span></span>**

1.  <span data-ttu-id="c5352-124">Когда клиент запущен, в области уведомлений щелкните правой кнопкой мыши значок MED-V.</span><span class="sxs-lookup"><span data-stu-id="c5352-124">When the client is running, in the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="c5352-125">В подменю выберите команду **перезапустить рабочую область**.</span><span class="sxs-lookup"><span data-stu-id="c5352-125">On the submenu, click **Restart Workspace**.</span></span>

    <span data-ttu-id="c5352-126">Рабочая область MED-V перезапускается.</span><span class="sxs-lookup"><span data-stu-id="c5352-126">The MED-V workspace is restarted.</span></span>

    -   <span data-ttu-id="c5352-127">В постоянной рабочей области MED-V виртуальная машина закрывается, а затем перезапускается.</span><span class="sxs-lookup"><span data-stu-id="c5352-127">In a persistent MED-V workspace, the virtual machine is shut down and then restarted.</span></span>

    -   <span data-ttu-id="c5352-128">В рабочей области revertible MED-V виртуальная машина фактически не выключается; Вместо этого он возвращается к исходному состоянию.</span><span class="sxs-lookup"><span data-stu-id="c5352-128">In a revertible MED-V workspace, the virtual machine does not actually shut down; instead, it returns to its original state.</span></span>

**<span data-ttu-id="c5352-129">Остановка рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="c5352-129">To stop a MED-V workspace</span></span>**

1.  <span data-ttu-id="c5352-130">В области уведомлений щелкните правой кнопкой мыши значок MED-V.</span><span class="sxs-lookup"><span data-stu-id="c5352-130">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="c5352-131">В подменю выберите команду **остановить рабочую область**.</span><span class="sxs-lookup"><span data-stu-id="c5352-131">On the submenu, click **Stop Workspace**.</span></span>

    <span data-ttu-id="c5352-132">Рабочее пространство MED-V остановлено.</span><span class="sxs-lookup"><span data-stu-id="c5352-132">The MED-V workspace is stopped.</span></span>

## <span data-ttu-id="c5352-133">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c5352-133">Related topics</span></span>


[<span data-ttu-id="c5352-134">Запуск клиента MED-V и выход из него</span><span class="sxs-lookup"><span data-stu-id="c5352-134">How to Start and Exit the MED-V Client</span></span>](how-to-start-and-exit-the-med-v-client.md)

 

 





