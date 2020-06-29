---
title: Администрирование виртуальных приложений App-V 5.0 с помощью консоли управления
description: Администрирование виртуальных приложений App-V 5.0 с помощью консоли управления
author: dansimp
ms.assetid: e9280dbd-782b-493a-b495-daab25247795
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: 7a71f7c0fd82f8ef9d1efd5b978591b6838a648a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814869"
---
# <span data-ttu-id="ea7e1-103">Администрирование виртуальных приложений App-V 5.0 с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-103">Administering App-V 5.0 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="ea7e1-104">Используйте сервер управления Microsoft Application Virtualization (App-V) 5,0 для управления пакетами, группами подключений и доступом к пакетам в среде.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-104">Use the Microsoft Application Virtualization (App-V) 5.0 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="ea7e1-105">Сервер публикует значки, ярлыки и сопоставления типов файлов на авторизованных компьютерах, на которых запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.0 client.</span></span> <span data-ttu-id="ea7e1-106">Как правило, один или несколько серверов управления совместно имеют общее хранилище данных для конфигурации и сведений о пакете.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="ea7e1-107">Сервер управления использует группы доменных служб Active Directory (AD DS) для управления авторизацией пользователей и установленный SQL Server для управления базой данных и хранилищем данных.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="ea7e1-108">Так как серверы управления потоками приложений для конечных пользователей по запросу, эти серверы лучше всего подходят для конфигураций системы, которые обладают надежной и высокоскоростной ЛВС.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="ea7e1-109">Сервер управления состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="ea7e1-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="ea7e1-110">Сервер управления — используйте сервер управления для управления пакетами и группами подключений.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="ea7e1-111">Сервер публикации — используйте сервер публикации для развертывания пакетов на компьютерах, на которых запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.0 client.</span></span>

-   <span data-ttu-id="ea7e1-112">База данных управления — используйте базу данных управления для управления доступом к пакету и публикации синхронизации сервера с сервером управления.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="ea7e1-113">Задачи консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-113">Management Console tasks</span></span>


<span data-ttu-id="ea7e1-114">Ниже перечислены наиболее распространенные задачи, которые можно выполнять с помощью консоли управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-114">The most common tasks that you can perform with the App-V 5.0 Management console are:</span></span>

-   [<span data-ttu-id="ea7e1-115">Подключение к консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-beta.md)

-   [<span data-ttu-id="ea7e1-116">Добавление или обновление пакетов с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)

-   [<span data-ttu-id="ea7e1-117">Настройка доступа к пакетам с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

-   [<span data-ttu-id="ea7e1-118">Публикация пакета с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-50.md)

-   [<span data-ttu-id="ea7e1-119">Удаление пакета в консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-beta.md)

-   [<span data-ttu-id="ea7e1-120">Добавление или удаление администратора с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)

-   [<span data-ttu-id="ea7e1-121">Регистрация и отмена регистрации сервера публикации с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console.md)

-   [<span data-ttu-id="ea7e1-122">Создание пользовательского файла конфигурации с помощью консоли управления App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ea7e1-122">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)

-   [<span data-ttu-id="ea7e1-123">Передача прав доступа и конфигураций в другую версию пакета с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console.md)

-   [<span data-ttu-id="ea7e1-124">Настройка расширений виртуальных приложений для определенной группы AD с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console.md)

-   [<span data-ttu-id="ea7e1-125">Настройка приложений и расширений виртуальных приложений по умолчанию в консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-125">Configure Applications and Default Virtual Application Extensions in Management Console</span></span>](configure-applications-and-default-virtual-application-extensions-in-management-console.md)

<span data-ttu-id="ea7e1-126">Основные элементы консоли управления App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="ea7e1-126">The main elements of the App-V 5.0 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ea7e1-127">Вкладка консоли управления</span><span class="sxs-lookup"><span data-stu-id="ea7e1-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="ea7e1-128">Описание</span><span class="sxs-lookup"><span data-stu-id="ea7e1-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea7e1-129">Обзор</span><span class="sxs-lookup"><span data-stu-id="ea7e1-129">Overview</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><strong><span data-ttu-id="ea7e1-130">Секвенсор App-V </strong> - Выберите этот параметр, чтобы просмотреть общие сведения об использовании секвенсора App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-130">App-V Sequencer</strong> - Select this option to review general information about using the App-V 5.0 sequencer.</span></span></p></li>
<li><p><strong><span data-ttu-id="ea7e1-131">Библиотека пакетов приложения </strong> : Выберите этот параметр, чтобы открыть <strong> страницу "пакеты" на </strong> консоли управления.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-131">Application Packages Library</strong> – Select this option to open the <strong>PACKAGES</strong> page of the Management Console.</span></span> <span data-ttu-id="ea7e1-132">Эта страница служит для просмотра пакетов, которые были добавлены на сервер.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-132">Use this page to review packages that have been added to the server.</span></span> <span data-ttu-id="ea7e1-133">Вы также можете управлять группами подключений, а также добавлять и обновлять пакеты.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-133">You can also manage the connection groups, as well as add or upgrade packages.</span></span></p></li>
<li><p><strong><span data-ttu-id="ea7e1-134">СЕРВЕРЫ </strong> : Выберите этот параметр, чтобы открыть <strong> страницу "серверы" </strong> консоли управления.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-134">SERVERS</strong> – Select this option to open the <strong>SERVERS</strong> page of the Management Console.</span></span> <span data-ttu-id="ea7e1-135">На этой странице можно просмотреть список серверов, зарегистрированных в вашей инфраструктуре App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-135">Use this page to review the list of servers that have been registered with your App-V 5.0 infrastructure.</span></span></p></li>
<li><p><strong><span data-ttu-id="ea7e1-136">КЛИЕНТЫ </strong> : Выберите этот параметр, чтобы просмотреть общие сведения о клиентах App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-136">CLIENTS</strong> – Select this option to review general information about App-V 5.0 clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea7e1-137">Вкладка "пакеты"</span><span class="sxs-lookup"><span data-stu-id="ea7e1-137">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea7e1-138">С помощью <strong> </strong> вкладки "пакеты" можно добавлять и обновлять пакеты.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-138">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span> <span data-ttu-id="ea7e1-139">Вы также можете управлять группами подключений, щелкая <strong> группы подключения </strong> .</span><span class="sxs-lookup"><span data-stu-id="ea7e1-139">You can also manage connection groups by clicking <strong>CONNECTION GROUPS</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea7e1-140">Вкладка "серверы"</span><span class="sxs-lookup"><span data-stu-id="ea7e1-140">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea7e1-141">С помощью <strong> </strong> вкладки серверы зарегистрируйте новый сервер.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-141">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea7e1-142">Вкладка "Администраторы"</span><span class="sxs-lookup"><span data-stu-id="ea7e1-142">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea7e1-143">С помощью <strong> </strong> вкладки администраторы можно зарегистрировать, добавить или удалить администраторов в среде App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ea7e1-143">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.0 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <a href="" id="other-resources-for-this-app-v-5-0-deployment-"></a><span data-ttu-id="ea7e1-144">Другие ресурсы для развертывания приложения-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ea7e1-144">Other resources for this App-V 5.0 deployment</span></span>


-   [<span data-ttu-id="ea7e1-145">Руководство администратора Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="ea7e1-145">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="ea7e1-146">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ea7e1-146">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





