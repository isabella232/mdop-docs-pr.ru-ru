---
title: Настройка серверов публикации
description: Настройка серверов публикации
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816529"
---
# <span data-ttu-id="deb0d-103">Настройка серверов публикации</span><span class="sxs-lookup"><span data-stu-id="deb0d-103">How to Set Up Publishing Servers</span></span>


<span data-ttu-id="deb0d-104">Вы можете использовать следующие процедуры для добавления и настройки серверов виртуализации приложений прямо из консоли управления клиентом.</span><span class="sxs-lookup"><span data-stu-id="deb0d-104">You can use the following procedures to add and configure Application Virtualization Servers directly from the Client Management Console.</span></span>

**<span data-ttu-id="deb0d-105">Добавление сервера публикаций приложения</span><span class="sxs-lookup"><span data-stu-id="deb0d-105">To add an application publishing server</span></span>**

1.  <span data-ttu-id="deb0d-106">В области **результатов** щелкните правой кнопкой мыши и выберите в контекстном меню пункт **создать сервер** , чтобы запустить мастер создания сервера Application Virtualization, или же щелкните правой кнопкой мыши узел **сервера публикаций** и выберите в контекстном меню пункт **создать сервер** .</span><span class="sxs-lookup"><span data-stu-id="deb0d-106">In the **Results** pane, right-click and select **New Server** from the pop-up-menu to start the New Application Virtualization Server Wizard, or alternatively, right-click the **Publishing Server** node and select **New Server** from the pop-up-menu.</span></span>

2.  <span data-ttu-id="deb0d-107">На странице 1 мастера введите имя сервера в поле **Отображаемое имя** и выберите тип сервера в раскрывающемся списке **Type (тип** ).</span><span class="sxs-lookup"><span data-stu-id="deb0d-107">On page one of the wizard, enter the name of the server in the **Display Name** field and select the server type from the **Type** drop-down list.</span></span> <span data-ttu-id="deb0d-108">Вы можете выбрать **сервер виртуализации приложений**, **сервер виртуализации приложений**, **стандартный HTTP-сервер**или **сервер расширенной защиты HTTP** из раскрывающегося списка типов сервера.</span><span class="sxs-lookup"><span data-stu-id="deb0d-108">You can choose **Application Virtualization Server**, **Enhanced Security Application Virtualization Server**, **Standard HTTP Server**, or **Enhanced Security HTTP Server** from the drop-down list of server types.</span></span>

3.  <span data-ttu-id="deb0d-109">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="deb0d-109">Click **Next**.</span></span>

4.  <span data-ttu-id="deb0d-110">На второй странице мастера введите нужные сведения в поля " **имя узла** " и " **порт** ".</span><span class="sxs-lookup"><span data-stu-id="deb0d-110">On page two of the wizard, type the appropriate information into the **Host Name** and **Port** fields.</span></span> <span data-ttu-id="deb0d-111">Поле " **путь** " не может быть доступно для серверов виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="deb0d-111">The **Path** field is not editable for Application Virtualization Servers.</span></span> <span data-ttu-id="deb0d-112">Необходимо ввести путь к стандартному серверу HTTP или расширенному серверу безопасности HTTP.</span><span class="sxs-lookup"><span data-stu-id="deb0d-112">You must enter a path for Standard HTTP Server or Enhanced Security HTTP Server.</span></span>

5.  <span data-ttu-id="deb0d-113">Нажмите кнопку **Готово** , чтобы добавить сервер.</span><span class="sxs-lookup"><span data-stu-id="deb0d-113">Click **Finish** to add the server.</span></span>

**<span data-ttu-id="deb0d-114">Настройка сервера публикаций приложения</span><span class="sxs-lookup"><span data-stu-id="deb0d-114">To set up an application publishing server</span></span>**

1.  <span data-ttu-id="deb0d-115">В области **результатов** щелкните правой кнопкой мыши нужный сервер и в контекстном меню выберите пункт **свойства** .</span><span class="sxs-lookup"><span data-stu-id="deb0d-115">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="deb0d-116">Откройте вкладку **Общие** , в которой вы можете изменить имя сервера, выберите тип из раскрывающегося списка типы серверов, а затем укажите имя узла и порт.</span><span class="sxs-lookup"><span data-stu-id="deb0d-116">Click the **General** tab, where you can change the server name, select a type from the drop-down list of server types, and specify the host name and port.</span></span> <span data-ttu-id="deb0d-117">Если тип сервера — стандартный HTTP-сервер или HTTP-сервер расширенной безопасности, поле " **путь** " также можно редактировать.</span><span class="sxs-lookup"><span data-stu-id="deb0d-117">When the server type is Standard HTTP Server or Enhanced Security HTTP Server, the **Path** field is also editable.</span></span>

3.  <span data-ttu-id="deb0d-118">Откройте вкладку **Обновление** , в которой установлен флажок **Обновить публикацию при входе пользователя** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="deb0d-118">Click the **Refresh** tab, where the **Refresh publishing on user login** check box is selected by default.</span></span> <span data-ttu-id="deb0d-119">Чтобы изменить частоту обновления, установите флажок **обновлять публикацию каждый раз** и введите число, представляющее частоту в поле.</span><span class="sxs-lookup"><span data-stu-id="deb0d-119">To change the refresh rate, select the **Refresh publishing every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="deb0d-120">Затем в раскрывающемся меню выберите **минуты**, **часы**и **дни** .</span><span class="sxs-lookup"><span data-stu-id="deb0d-120">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span> <span data-ttu-id="deb0d-121">(Минимальное количество времени, которое вы можете ввести, составляет 30 минут.)</span><span class="sxs-lookup"><span data-stu-id="deb0d-121">(The minimum amount of time you can enter is 30 minutes.)</span></span>

4.  <span data-ttu-id="deb0d-122">Нажмите кнопку **Применить** , чтобы изменить конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="deb0d-122">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="deb0d-123">Завершив публикацию, нажмите кнопку **ОК** , чтобы закрыть диалоговое окно и вернуться на консоль управления клиентом.</span><span class="sxs-lookup"><span data-stu-id="deb0d-123">When you are finished publishing, click **OK** to exit the dialog box and return to the Client Management Console.</span></span>

## <span data-ttu-id="deb0d-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="deb0d-124">Related topics</span></span>


[<span data-ttu-id="deb0d-125">Отключение или изменение параметров режима изолированной работы</span><span class="sxs-lookup"><span data-stu-id="deb0d-125">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





