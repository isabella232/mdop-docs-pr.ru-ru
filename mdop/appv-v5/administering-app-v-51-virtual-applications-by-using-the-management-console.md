---
title: Администрирование виртуальных приложений App-V 5.1 с помощью консоли управления
description: Администрирование виртуальных приложений App-V 5.1 с помощью консоли управления
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814864"
---
# <span data-ttu-id="26c34-103">Администрирование виртуальных приложений App-V 5.1 с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-103">Administering App-V 5.1 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="26c34-104">Используйте сервер управления Microsoft Application Virtualization (App-V) 5,1 для управления пакетами, группами подключений и доступом к пакетам в среде.</span><span class="sxs-lookup"><span data-stu-id="26c34-104">Use the Microsoft Application Virtualization (App-V) 5.1 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="26c34-105">Сервер публикует значки, ярлыки и сопоставления типов файлов на авторизованных компьютерах, на которых запущен клиент App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="26c34-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.1 client.</span></span> <span data-ttu-id="26c34-106">Как правило, один или несколько серверов управления совместно имеют общее хранилище данных для конфигурации и сведений о пакете.</span><span class="sxs-lookup"><span data-stu-id="26c34-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="26c34-107">Сервер управления использует группы доменных служб Active Directory (AD DS) для управления авторизацией пользователей и установленный SQL Server для управления базой данных и хранилищем данных.</span><span class="sxs-lookup"><span data-stu-id="26c34-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="26c34-108">Так как серверы управления потоками приложений для конечных пользователей по запросу, эти серверы лучше всего подходят для конфигураций системы, которые обладают надежной и высокоскоростной ЛВС.</span><span class="sxs-lookup"><span data-stu-id="26c34-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="26c34-109">Сервер управления состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="26c34-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="26c34-110">Сервер управления — используйте сервер управления для управления пакетами и группами подключений.</span><span class="sxs-lookup"><span data-stu-id="26c34-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="26c34-111">Сервер публикации — используйте сервер публикации для развертывания пакетов на компьютерах, на которых запущен клиент App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="26c34-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.1 client.</span></span>

-   <span data-ttu-id="26c34-112">База данных управления — используйте базу данных управления для управления доступом к пакету и публикации синхронизации сервера с сервером управления.</span><span class="sxs-lookup"><span data-stu-id="26c34-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="26c34-113">Задачи консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-113">Management Console tasks</span></span>


<span data-ttu-id="26c34-114">Ниже перечислены наиболее распространенные задачи, которые можно выполнять с помощью консоли управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="26c34-114">The most common tasks that you can perform with the App-V 5.1 Management console are:</span></span>

-   [<span data-ttu-id="26c34-115">Подключение к консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-51.md)

-   [<span data-ttu-id="26c34-116">Добавление или обновление пакетов с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [<span data-ttu-id="26c34-117">Настройка доступа к пакетам с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [<span data-ttu-id="26c34-118">Публикация пакета с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [<span data-ttu-id="26c34-119">Удаление пакета в консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-51.md)

-   [<span data-ttu-id="26c34-120">Добавление или удаление администратора с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [<span data-ttu-id="26c34-121">Регистрация и отмена регистрации сервера публикации с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [<span data-ttu-id="26c34-122">Создание пользовательского файла конфигурации с помощью консоли управления App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="26c34-122">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [<span data-ttu-id="26c34-123">Передача прав доступа и конфигураций в другую версию пакета с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [<span data-ttu-id="26c34-124">Настройка расширений виртуальных приложений для определенной группы AD с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [<span data-ttu-id="26c34-125">Просмотр и настройка приложений и расширений виртуальных приложений по умолчанию с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-125">How to View and Configure Applications and Default Virtual Application Extensions by Using the Management Console</span></span>](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

<span data-ttu-id="26c34-126">Основные элементы консоли управления App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="26c34-126">The main elements of the App-V 5.1 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="26c34-127">Вкладка консоли управления</span><span class="sxs-lookup"><span data-stu-id="26c34-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="26c34-128">Описание</span><span class="sxs-lookup"><span data-stu-id="26c34-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26c34-129">Вкладка "пакеты"</span><span class="sxs-lookup"><span data-stu-id="26c34-129">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="26c34-130">С помощью <strong> </strong> вкладки "пакеты" можно добавлять и обновлять пакеты.</span><span class="sxs-lookup"><span data-stu-id="26c34-130">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26c34-131">Вкладка "группы подключения"</span><span class="sxs-lookup"><span data-stu-id="26c34-131">Connection Groups tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="26c34-132"><strong>Вкладка "группы подключения </strong> " используется для управления группами подключений.</span><span class="sxs-lookup"><span data-stu-id="26c34-132">Use the <strong>CONNECTION GROUPS</strong> tab to manage connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26c34-133">Вкладка "серверы"</span><span class="sxs-lookup"><span data-stu-id="26c34-133">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="26c34-134">С помощью <strong> </strong> вкладки серверы зарегистрируйте новый сервер.</span><span class="sxs-lookup"><span data-stu-id="26c34-134">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26c34-135">Вкладка "Администраторы"</span><span class="sxs-lookup"><span data-stu-id="26c34-135">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="26c34-136">С помощью <strong> </strong> вкладки администраторы можно зарегистрировать, добавить или удалить администраторов в среде App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="26c34-136">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.1 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="26c34-137">**Важно!**  На веб-сайте, на котором открывается консоль управления Веба, должен быть включен JavaScript.</span><span class="sxs-lookup"><span data-stu-id="26c34-137">**Important** JavaScript must be enabled on the browser that opens the Web Management Console.</span></span>

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a><span data-ttu-id="26c34-138">Другие ресурсы для развертывания приложения-V 5,1</span><span class="sxs-lookup"><span data-stu-id="26c34-138">Other resources for this App-V 5.1 deployment</span></span>


-   [<span data-ttu-id="26c34-139">Руководство администратора Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="26c34-139">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)

-   [<span data-ttu-id="26c34-140">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="26c34-140">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





