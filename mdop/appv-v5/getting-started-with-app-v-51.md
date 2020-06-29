---
title: Начало работы с App-V 5.1
description: Начало работы с App-V 5.1
author: dansimp
ms.assetid: 49a20e1f-0566-4e53-a417-1521393fc974
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff10f12bc672a24f2837f50bfb1f0033ede3e46f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814549"
---
# <span data-ttu-id="07ca4-103">Начало работы с App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="07ca4-103">Getting Started with App-V 5.1</span></span>


<span data-ttu-id="07ca4-104">Microsoft Application Virtualization (App-V) 5,1 позволяет администраторам развертывать, обновлять и поддерживать приложения как службы в режиме реального времени, по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="07ca4-104">Microsoft Application Virtualization (App-V) 5.1 enables administrators to deploy, update, and support applications as services in real time, on an as-needed basis.</span></span> <span data-ttu-id="07ca4-105">Отдельные приложения преобразуются из локально установленных продуктов в централизованно управляемые службы и доступны там, где это необходимо, без необходимости предварительной настройки компьютеров и изменения параметров операционной системы.</span><span class="sxs-lookup"><span data-stu-id="07ca4-105">Individual applications are transformed from locally installed products into centrally managed services and are available wherever you need, without the need to preconfigure computers or to change operating system settings.</span></span>

<span data-ttu-id="07ca4-106">App-V состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="07ca4-106">App-V consists of the following elements:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="07ca4-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="07ca4-107">Element</span></span></th>
<th align="left"><span data-ttu-id="07ca4-108">Описание</span><span class="sxs-lookup"><span data-stu-id="07ca4-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07ca4-109">Сервер управления App-V</span><span class="sxs-lookup"><span data-stu-id="07ca4-109">App-V Management Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="07ca4-110">Предоставляет центральное расположение для управления инфраструктурой App-V, которое предоставляет виртуальные приложения для клиентского компьютера App-V и служб удаленных рабочих столов (ранее — служб терминалов).</span><span class="sxs-lookup"><span data-stu-id="07ca4-110">Provides a central location for managing the App-V infrastructure, which delivers virtual applications to both the App-V Desktop Client and the Remote Desktop Services (formerly Terminal Services) Client.</span></span></p></li>
<li><p><span data-ttu-id="07ca4-111">Использует Microsoft SQL Server® для хранилища данных, где один или несколько серверов управления App-V могут совместно использовать одно хранилище данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="07ca4-111">Uses Microsoft SQL Server® for its data store, where one or more App-V Management servers can share a single SQL Server data store.</span></span></p></li>
<li><p><span data-ttu-id="07ca4-112">Выполняет проверку подлинности запросов и обеспечивает безопасность, измерения, мониторинг и сбор данных.</span><span class="sxs-lookup"><span data-stu-id="07ca4-112">Authenticates requests and provides security, metering, monitoring, and data gathering.</span></span> <span data-ttu-id="07ca4-113">Для управления пользователями и приложениями на сервере используются службы Active Directory и поддерживаемые инструменты.</span><span class="sxs-lookup"><span data-stu-id="07ca4-113">The server uses Active Directory and supporting tools to manage users and applications.</span></span></p></li>
<li><p><span data-ttu-id="07ca4-114">Есть сайт управления, позволяющий настраивать инфраструктуру App-V с любого компьютера.</span><span class="sxs-lookup"><span data-stu-id="07ca4-114">Has a management site that lets you configure the App-V infrastructure from any computer.</span></span> <span data-ttu-id="07ca4-115">Вы можете добавлять и удалять приложения, управлять сочетаниями клавиш, назначать разрешения на доступ пользователям и группам, а также создавать группы подключений.</span><span class="sxs-lookup"><span data-stu-id="07ca4-115">You can add and remove applications, manipulate shortcuts, assign access permissions to users and groups, and create connection groups.</span></span></p></li>
<li><p><span data-ttu-id="07ca4-116">Обеспечивает связь между консолью управления веб-приложением App-V и хранилищем данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="07ca4-116">Enables communication between the App-V Web Management Console and the SQL Server data store.</span></span> <span data-ttu-id="07ca4-117">Эти компоненты могут быть установлены на одном сервере или на одном или нескольких отдельных компьютерах в зависимости от требуемой системной архитектуры.</span><span class="sxs-lookup"><span data-stu-id="07ca4-117">These components can all be installed on a single server computer, or on one or more separate computers, depending on the required system architecture.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07ca4-118">Сервер публикаций App-V</span><span class="sxs-lookup"><span data-stu-id="07ca4-118">App-V Publishing Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="07ca4-119">Предоставляет клиентам App-V приложения с лицензионными данными для определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="07ca4-119">Provides App-V Clients with entitled applications for the specific user</span></span></p></li>
<li><p><span data-ttu-id="07ca4-120">Размещает виртуальный пакет приложения для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="07ca4-120">Hosts the virtual application package for streaming.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07ca4-121">Классическое приложение App-V</span><span class="sxs-lookup"><span data-stu-id="07ca4-121">App-V Desktop Client</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="07ca4-122">Получение виртуальных приложений</span><span class="sxs-lookup"><span data-stu-id="07ca4-122">Retrieves virtual applications</span></span></p></li>
<li><p><span data-ttu-id="07ca4-123">Публикация приложений на клиентах</span><span class="sxs-lookup"><span data-stu-id="07ca4-123">Publishes the applications on the clients</span></span></p></li>
<li><p><span data-ttu-id="07ca4-124">Автоматическая настройка виртуальных сред во время выполнения для конечных точек Windows и управление ими.</span><span class="sxs-lookup"><span data-stu-id="07ca4-124">Automatically sets up and manages virtual environments at runtime on Windows endpoints.</span></span></p></li>
<li><p><span data-ttu-id="07ca4-125">Сохраняются пользовательские параметры виртуальных приложений, такие как реестр и изменения файлов, в каждом пользовательском профиле&#39;s.</span><span class="sxs-lookup"><span data-stu-id="07ca4-125">Stores user-specific virtual application settings, such as registry and file changes, in each user&#39;s profile.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07ca4-126">Клиент служб удаленных рабочих столов (RDS) для App-V</span><span class="sxs-lookup"><span data-stu-id="07ca4-126">App-V Remote Desktop Services (RDS) Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="07ca4-127">Позволяет серверам узлов сеансов удаленных рабочих столов использовать возможности настольного клиента App-V для общих сеансов рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="07ca4-127">Enables Remote Desktop Session Host servers to use the capabilities of the App-V Desktop Client for shared desktop sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07ca4-128">Секвенсор App-V</span><span class="sxs-lookup"><span data-stu-id="07ca4-128">App-V Sequencer</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="07ca4-129">— Это средство на основе мастера, которое используется для преобразования традиционных приложений в виртуальные приложения.</span><span class="sxs-lookup"><span data-stu-id="07ca4-129">Is a wizard-based tool that you use to transform traditional applications into virtual applications.</span></span></p></li>
<li><p><span data-ttu-id="07ca4-130">Создает пакет приложения, который состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="07ca4-130">Produces the application “package,” which consists of:</span></span></p>
<ol>
<li><p><span data-ttu-id="07ca4-131">файл последовательного приложения (APPV)</span><span class="sxs-lookup"><span data-stu-id="07ca4-131">a sequenced application (APPV) file</span></span></p></li>
<li><p><span data-ttu-id="07ca4-132">файл установщика Windows (MSI), который может быть развернут на клиентах, настроенных для изолированной операции</span><span class="sxs-lookup"><span data-stu-id="07ca4-132">a Windows Installer file (MSI) that can be deployed to clients configured for stand-alone operation</span></span></p></li>
<li><p><span data-ttu-id="07ca4-133">Несколько XML-файлов, в том числе Report.XML, PackageName_DeploymentConfig.XML и PackageName_UserConfig.XML.</span><span class="sxs-lookup"><span data-stu-id="07ca4-133">Several XML files including Report.XML, PackageName_DeploymentConfig.XML, and PackageName_UserConfig.XML.</span></span> <span data-ttu-id="07ca4-134">XML-файлы UserConfig и DeploymentConfig используются для настройки изменения поведения пакета по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07ca4-134">The UserConfig and DeploymentConfig XML files are used to configure custom changes to the default behavior of the package.</span></span></p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="07ca4-135">Дополнительные сведения об этих элементах можно найти в разделе [архитектура высшего уровня для App-V 5,1](high-level-architecture-for-app-v-51.md).</span><span class="sxs-lookup"><span data-stu-id="07ca4-135">For more information about these elements, see [High Level Architecture for App-V 5.1](high-level-architecture-for-app-v-51.md).</span></span>

<span data-ttu-id="07ca4-136">Если вы не знакомы с этим продуктом, рекомендуем вам внимательно ознакомиться с документацией.</span><span class="sxs-lookup"><span data-stu-id="07ca4-136">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="07ca4-137">Перед развертыванием в рабочей среде мы также рекомендуем проверить план развертывания в среде тестовой сети.</span><span class="sxs-lookup"><span data-stu-id="07ca4-137">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="07ca4-138">Вы также можете воспользоваться классом, чтобы узнать о необходимых технологиях.</span><span class="sxs-lookup"><span data-stu-id="07ca4-138">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="07ca4-139">Дополнительные сведения о возможностях обучения Microsoft можно найти в разделе Общие сведения о Microsoft Training <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="07ca4-139">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="07ca4-140">**Примечание**  Недоступна загружаемая версия руководства администратора.</span><span class="sxs-lookup"><span data-stu-id="07ca4-140">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="07ca4-141">Тем не менее, вы можете узнать о специальных режимах библиотеки TechNet, где можно выбрать статьи, сгруппировать их в коллекцию, распечатать или экспортировать в файл по адресу <https://go.microsoft.com/fwlink/?LinkId=272491> ( https://go.microsoft.com/fwlink/?LinkId=272491) .</span><span class="sxs-lookup"><span data-stu-id="07ca4-141">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272491> (https://go.microsoft.com/fwlink/?LinkId=272491).</span></span>

 

<span data-ttu-id="07ca4-142">Этот раздел руководства администратора App-V 5,1 содержит подробные сведения о приложении App-V 5,1, которые помогут вам понять, как ознакомиться с продуктом, прежде чем приступить к планированию развертывания.</span><span class="sxs-lookup"><span data-stu-id="07ca4-142">This section of the App-V 5.1 Administrator’s Guide includes high-level information about App-V 5.1 to provide you with a basic understanding of the product before you begin the deployment planning.</span></span>

## <span data-ttu-id="07ca4-143">Начало работы с приложением-V 5,1</span><span class="sxs-lookup"><span data-stu-id="07ca4-143">Getting started with App-V 5.1</span></span>


-   [<span data-ttu-id="07ca4-144">Сведения об App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="07ca4-144">About App-V 5.1</span></span>](about-app-v-51.md)

    <span data-ttu-id="07ca4-145">В этой статье приведены общие сведения о приложении App-V 5,1 и его использовании в Организации.</span><span class="sxs-lookup"><span data-stu-id="07ca4-145">Provides a high-level overview of App-V 5.1 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="07ca4-146">Оценка App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="07ca4-146">Evaluating App-V 5.1</span></span>](evaluating-app-v-51.md)

    <span data-ttu-id="07ca4-147">Сведения о том, как наилучшим образом оценить приложение App-V 5,1 для использования в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="07ca4-147">Provides information about how you can best evaluate App-V 5.1 for use in your organization.</span></span>

-   [<span data-ttu-id="07ca4-148">Высокоуровневая архитектура App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="07ca4-148">High Level Architecture for App-V 5.1</span></span>](high-level-architecture-for-app-v-51.md)

    <span data-ttu-id="07ca4-149">Содержит описание функций App-V 5,1 и их взаимодействия друг с другом.</span><span class="sxs-lookup"><span data-stu-id="07ca4-149">Provides a description of the App-V 5.1 features and how they work together.</span></span>

-   [<span data-ttu-id="07ca4-150">Специальные возможности для App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="07ca4-150">Accessibility for App-V 5.1</span></span>](accessibility-for-app-v-51.md)

    <span data-ttu-id="07ca4-151">Сведения о функциях и службах, которые делают этот продукт и соответствующую документацию более удобной для людей с ограниченными возможностями.</span><span class="sxs-lookup"><span data-stu-id="07ca4-151">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="07ca4-152">Другие ресурсы для этого продукта</span><span class="sxs-lookup"><span data-stu-id="07ca4-152">Other resources for this product</span></span>


-   [<span data-ttu-id="07ca4-153">Руководство администратора Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="07ca4-153">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)

-   [<span data-ttu-id="07ca4-154">Планирование использования App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="07ca4-154">Planning for App-V 5.1</span></span>](planning-for-app-v-51.md)

-   [<span data-ttu-id="07ca4-155">Развертывание App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="07ca4-155">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

-   [<span data-ttu-id="07ca4-156">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="07ca4-156">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

-   [<span data-ttu-id="07ca4-157">Устранение неполадок в App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="07ca4-157">Troubleshooting App-V 5.1</span></span>](troubleshooting-app-v-51.md)

-   [<span data-ttu-id="07ca4-158">Технический справочник для App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="07ca4-158">Technical Reference for App-V 5.1</span></span>](technical-reference-for-app-v-51.md)






 

 





