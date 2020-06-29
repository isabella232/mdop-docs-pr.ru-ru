---
title: Регистрация и отмена регистрации сервера публикации с помощью консоли управления
description: Регистрация и отмена регистрации сервера публикации с помощью консоли управления
author: dansimp
ms.assetid: 69cef0a8-8102-4697-b1ba-f16e0f25216b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b63922ff03ea19326e395e57236fcd079711bd43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813757"
---
# <span data-ttu-id="39a71-103">Регистрация и отмена регистрации сервера публикации с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="39a71-103">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>


<span data-ttu-id="39a71-104">Вы можете регистрировать и отменять регистрацию серверов публикаций, которые будут синхронизироваться с сервером управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="39a71-104">You can register and unregister publishing servers that will synchronize with the App-V 5.1 management server.</span></span> <span data-ttu-id="39a71-105">Кроме того, вы можете увидеть последнюю попытку, которую сервер публикаций сделал для синхронизации данных с сервером управления.</span><span class="sxs-lookup"><span data-stu-id="39a71-105">You can also see the last attempt that the publishing server made to synchronize the information with the management server.</span></span>

<span data-ttu-id="39a71-106">Для регистрации или отмены регистрации сервера публикаций выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="39a71-106">Use the following procedure to register or unregister a publishing server.</span></span>

**<span data-ttu-id="39a71-107">Регистрация сервера публикаций с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="39a71-107">To register a publishing server using the Management Console</span></span>**

1.  <span data-ttu-id="39a71-108">Подключитесь к консоли управления и выберите пункт **серверы**.</span><span class="sxs-lookup"><span data-stu-id="39a71-108">Connect to the Management Console and select **Servers**.</span></span> <span data-ttu-id="39a71-109">Дополнительные сведения о том, как подключиться к консоли управления, можно найти в разделе [Подключение к консоли управления](how-to-connect-to-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="39a71-109">For more information about how to connect to the Management Console, see [How to Connect to the Management Console](how-to-connect-to-the-management-console-51.md).</span></span>

2.  <span data-ttu-id="39a71-110">Откроется список серверов публикаций, которые уже синхронизируются с сервером управления.</span><span class="sxs-lookup"><span data-stu-id="39a71-110">A list of publishing servers that already synchronize with the management server is displayed.</span></span> <span data-ttu-id="39a71-111">Нажмите кнопку Зарегистрировать новый сервер, чтобы зарегистрировать новый сервер.</span><span class="sxs-lookup"><span data-stu-id="39a71-111">Click Register New Server to register a new server.</span></span>

3.  <span data-ttu-id="39a71-112">Введите имя компьютера домена, подключенного к домену, в строке **имя сервера** , чтобы указать имя сервера.</span><span class="sxs-lookup"><span data-stu-id="39a71-112">Type a computer name of a domain joined computer on the **Server Name** line, to specify a name for the server.</span></span> <span data-ttu-id="39a71-113">Кроме того, необходимо указать доменное имя, например **MyDomain\\TestServer**.</span><span class="sxs-lookup"><span data-stu-id="39a71-113">You should also include a domain name, for example, **MyDomain\\TestServer**.</span></span> <span data-ttu-id="39a71-114">Нажмите кнопку **проверить**.</span><span class="sxs-lookup"><span data-stu-id="39a71-114">Click **Check**.</span></span>

4.  <span data-ttu-id="39a71-115">Выберите компьютер и нажмите кнопку **Добавить** , чтобы добавить компьютер в список серверов.</span><span class="sxs-lookup"><span data-stu-id="39a71-115">Select the computer and click **Add** to add the computer to the list of servers.</span></span> <span data-ttu-id="39a71-116">Новый сервер появится в списке.</span><span class="sxs-lookup"><span data-stu-id="39a71-116">The new server will be displayed in the list.</span></span>

**<span data-ttu-id="39a71-117">Отмена регистрации сервера публикаций с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="39a71-117">To unregister a publishing server using the Management Console</span></span>**

1.  <span data-ttu-id="39a71-118">Подключитесь к консоли управления и выберите пункт **серверы**.</span><span class="sxs-lookup"><span data-stu-id="39a71-118">Connect to the Management Console and select **Servers**.</span></span> <span data-ttu-id="39a71-119">Дополнительные сведения о том, как подключиться к консоли управления, можно найти в разделе [Подключение к консоли управления](how-to-connect-to-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="39a71-119">For more information about how to connect to the Management Console, see [How to Connect to the Management Console](how-to-connect-to-the-management-console-51.md).</span></span>

2.  <span data-ttu-id="39a71-120">Откроется список серверов публикаций, которые синхронизируются с сервером управления.</span><span class="sxs-lookup"><span data-stu-id="39a71-120">A list of publishing servers that synchronize with the management server is displayed.</span></span>

3.  <span data-ttu-id="39a71-121">Чтобы отменить регистрацию сервера, щелкните правой кнопкой мыши имя компьютера и выберите имя компьютера и нажмите отменить **регистрацию сервера**.</span><span class="sxs-lookup"><span data-stu-id="39a71-121">To unregister the server, right-click the computer name and select the computer name and select **unregister server**.</span></span>

    <span data-ttu-id="39a71-122">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="39a71-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="39a71-123">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="39a71-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="39a71-124">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="39a71-124">Got an App-V issue?</span></span>** <span data-ttu-id="39a71-125">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="39a71-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="39a71-126">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="39a71-126">Related topics</span></span>


[<span data-ttu-id="39a71-127">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="39a71-127">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





