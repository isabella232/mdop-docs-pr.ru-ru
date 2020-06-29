---
title: Узел системы виртуализации приложений консоли управления сервером
description: Узел системы виртуализации приложений консоли управления сервером
author: dansimp
ms.assetid: 9450832e-335c-41e7-af24-fddb8ffc327c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51256ee7e96a97016e73dc79c87e4d422198cfb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815442"
---
# <span data-ttu-id="a9d37-103">Консоль управления серверами: узел системы Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="a9d37-103">Server Management Console: Application Virtualization System Node</span></span>


<span data-ttu-id="a9d37-104">Узел системы Application Virtualization является узлом верхнего уровня в области " **область** ".</span><span class="sxs-lookup"><span data-stu-id="a9d37-104">The Application Virtualization System node is the top-level node in the **Scope** pane.</span></span> <span data-ttu-id="a9d37-105">Этот узел отображает имя сервера, на котором находится текущая консоль, или отображает имя локального компьютера (если вы соединены с этим именем) или "локальный", когда консоль подключена к локальному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="a9d37-105">This node displays the name of the server the console is currently controlling, or it displays the name of the local computer (if you are connected by the name) or "local" when the console is connected to the local computer.</span></span> <span data-ttu-id="a9d37-106">Из узла системы Application Virtualization вы можете подключаться к другому компьютеру или подключаться к текущему компьютеру с другим набором учетных данных.</span><span class="sxs-lookup"><span data-stu-id="a9d37-106">From the Application Virtualization System node, you can connect to another computer or you can connect to the current computer with a different set of credentials.</span></span>

<span data-ttu-id="a9d37-107">Вы можете щелкнуть правой кнопкой мыши узел системы Application Virtualization, чтобы отобразить указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="a9d37-107">You can right-click the Application Virtualization System node to display the following elements.</span></span>

<a href="" id="configure-connection"></a>**<span data-ttu-id="a9d37-108">Настройка подключения</span><span class="sxs-lookup"><span data-stu-id="a9d37-108">Configure Connection</span></span>**  
<span data-ttu-id="a9d37-109">В этом диалоговом окне можно изменить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="a9d37-109">In this dialog box, you can modify the following settings:</span></span>

- <span data-ttu-id="a9d37-110">**Имя узла веб-службы**— позволяет указать имя системы виртуализации приложений, к которой вы хотите подключиться, или указать **localhost** для подключения к локальному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="a9d37-110">**Web Service Host Name**—Enables you to enter the name of the Application Virtualization System to which you want to connect, or you can enter **localhost** to connect to the local computer.</span></span>

- <span data-ttu-id="a9d37-111">**Используйте безопасное соединение**— установите этот флажок, если вы хотите подключиться к серверу с помощью безопасного соединения.</span><span class="sxs-lookup"><span data-stu-id="a9d37-111">**Use Secure Connection**—Select if you want to connect to the server with a secure connection.</span></span>

- <span data-ttu-id="a9d37-112">**Port (порт**) — позволяет ввести номер порта, который вы хотите использовать для подключения.</span><span class="sxs-lookup"><span data-stu-id="a9d37-112">**Port**—Enables you to enter the port number you want to use for the connection.</span></span> <span data-ttu-id="a9d37-113">80 является стандартным номером порта по умолчанию, а 443 — номером защищенного порта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a9d37-113">80 is the default regular port number, and 443 is default secure port number.</span></span>

- <span data-ttu-id="a9d37-114">**Использовать текущую учетную запись Windows**— выберите этот параметр, чтобы использовать текущие учетные данные учетной записи Windows.</span><span class="sxs-lookup"><span data-stu-id="a9d37-114">**Use Current Windows Account**—Select to use the current Windows account credentials.</span></span>

- <span data-ttu-id="a9d37-115">**Укажите учетную запись Windows**— выберите, когда нужно подключиться к серверу в качестве другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="a9d37-115">**Specify Windows Account**—Select when you want to connect to the server as a different user.</span></span>

- <span data-ttu-id="a9d37-116">**Name (имя**) — позволяет вводить имя нового пользователя, используя либо *DOMAIN\\username* , либо <em> </em> Формат username@domain.</span><span class="sxs-lookup"><span data-stu-id="a9d37-116">**Name**—Enables you to enter the name of the new user by using either the *DOMAIN\\username* or the <em>username@domain</em> format.</span></span>

- <span data-ttu-id="a9d37-117">**Password (пароль**) — позволяет вводить пароль, соответствующий новому пользователю.</span><span class="sxs-lookup"><span data-stu-id="a9d37-117">**Password**—Enables you to enter the password that corresponds to the new user.</span></span>

<a href="" id="system-options"></a>**<span data-ttu-id="a9d37-118">Параметры системы</span><span class="sxs-lookup"><span data-stu-id="a9d37-118">System Options</span></span>**  
<span data-ttu-id="a9d37-119">На следующих вкладках в этом диалоговом окне можно изменить соответствующие параметры.</span><span class="sxs-lookup"><span data-stu-id="a9d37-119">On the following tabs on this dialog box, you can modify the associated settings:</span></span>

-   <span data-ttu-id="a9d37-120">**Вкладка "Общие"**— позволяет указать **путь к содержимому по умолчанию** для хранения файлов OSD и значков.</span><span class="sxs-lookup"><span data-stu-id="a9d37-120">**General Tab**—Enables you to specify the **Default Content Path** where the OSD and icon files are stored.</span></span>

-   <span data-ttu-id="a9d37-121">**Вкладка Database (база данных**) — позволяет указать максимальный **Размер базы данных** и **Журнал использования**.</span><span class="sxs-lookup"><span data-stu-id="a9d37-121">**Database Tab**—Enables you to specify the maximum **Database Size** and the **Usage History**.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="a9d37-122">Просмотр</span><span class="sxs-lookup"><span data-stu-id="a9d37-122">View</span></span>**  
<span data-ttu-id="a9d37-123">Изменяет внешний вид консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="a9d37-123">Changes the appearance of the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="a9d37-124">Дополнительные сведения о том, как изменить внешний вид консоли, можно найти в статье файлы справки для консоли управления Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a9d37-124">For more information about changing the appearance of the console, refer to the help files for the Microsoft Management Console.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="a9d37-125">Новое окно</span><span class="sxs-lookup"><span data-stu-id="a9d37-125">New Window from Here</span></span>**  
<span data-ttu-id="a9d37-126">Открытие нового окна консоли управления.</span><span class="sxs-lookup"><span data-stu-id="a9d37-126">Opens a new management console window.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="a9d37-127">Экспорт списка</span><span class="sxs-lookup"><span data-stu-id="a9d37-127">Export List</span></span>**  
<span data-ttu-id="a9d37-128">Создает текстовый файл с разделителями-знаками табуляции, который включает содержимое области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="a9d37-128">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="a9d37-129">Этот элемент отображает диалоговое окно " **Сохранение файла** ", в котором указывается расположение для текстового файла, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="a9d37-129">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="a9d37-130">Help</span><span class="sxs-lookup"><span data-stu-id="a9d37-130">Help</span></span>**  
<span data-ttu-id="a9d37-131">Запуск файла справки консоли управления.</span><span class="sxs-lookup"><span data-stu-id="a9d37-131">Starts the management console help file.</span></span>

## <span data-ttu-id="a9d37-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a9d37-132">Related topics</span></span>


[<span data-ttu-id="a9d37-133">Справка по консоли управления серверами Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="a9d37-133">Application Virtualization Server Management Console Reference</span></span>](application-virtualization-server-management-console-reference.md)

 

 





