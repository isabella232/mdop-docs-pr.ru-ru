---
title: Развертывание сервера App-V 5.0
description: Развертывание сервера App-V 5.0
author: dansimp
ms.assetid: a47f0dc8-2971-4e4d-8d57-6b69bbed4b63
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8fb65015a172a88d5e27d377037348dbc044654
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814573"
---
# <span data-ttu-id="0a178-103">Развертывание сервера App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="0a178-103">Deploying the App-V 5.0 Server</span></span>


<span data-ttu-id="0a178-104">Вы можете установить компоненты сервера App-V 5,0 с помощью различных конфигураций развертывания, описанных в этой статье.</span><span class="sxs-lookup"><span data-stu-id="0a178-104">You can install the App-V 5.0 server features by using different deployment configurations, which described in this topic.</span></span> <span data-ttu-id="0a178-105">Перед установкой функций сервера ознакомьтесь с разделом сервер в разделе о [безопасности App-V 5,0](app-v-50-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="0a178-105">Before you install the server features, review the server section of [App-V 5.0 Security Considerations](app-v-50-security-considerations.md).</span></span>

<span data-ttu-id="0a178-106">Сведения о развертывании сервера App-V 5,0 с пакетом обновления 3 (SP3) можно найти в разделе [о приложении App-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span><span class="sxs-lookup"><span data-stu-id="0a178-106">For information about deploying the App-V 5.0 SP3 Server, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span></span>

<span data-ttu-id="0a178-107">**Важно!**  Перед установкой и настройкой серверов App-V 5,0 необходимо указать порт, в котором будет размещен каждый из компонентов.</span><span class="sxs-lookup"><span data-stu-id="0a178-107">**Important** Before you install and configure the App-V 5.0 servers, you must specify a port where each component will be hosted.</span></span> <span data-ttu-id="0a178-108">Кроме того, необходимо добавить соответствующие правила брандмауэра, разрешающие входящим запросам доступ к указанным портам.</span><span class="sxs-lookup"><span data-stu-id="0a178-108">You must also add the associated firewall rules to allow incoming requests to access the specified ports.</span></span> <span data-ttu-id="0a178-109">Установщик не изменяет параметры брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="0a178-109">The installer does not modify firewall settings.</span></span>

 

## <a href="" id="---------app-v-5-0-server-overview"></a> <span data-ttu-id="0a178-110">Общие сведения о сервере App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0a178-110">App-V 5.0 Server overview</span></span>


<span data-ttu-id="0a178-111">Сервер App-V 5,0 состоит из пяти компонентов.</span><span class="sxs-lookup"><span data-stu-id="0a178-111">The App-V 5.0 Server is made up of five components.</span></span> <span data-ttu-id="0a178-112">Каждый компонент играет другую цель в среде App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0a178-112">Each component serves a different purpose within the App-V 5.0 environment.</span></span> <span data-ttu-id="0a178-113">Ниже кратко описан каждый из пяти компонентов.</span><span class="sxs-lookup"><span data-stu-id="0a178-113">Each of the five components is briefly described here:</span></span>

-   <span data-ttu-id="0a178-114">Сервер управления — предоставляет общую функциональность управления для инфраструктуры App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0a178-114">Management Server – provides overall management functionality for the App-V 5.0 infrastructure.</span></span>

-   <span data-ttu-id="0a178-115">База данных управления — упрощает предварительное развертывание баз данных для управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0a178-115">Management Database – facilitates database predeployments for App-V 5.0 management.</span></span>

-   <span data-ttu-id="0a178-116">Сервер публикации — предоставляет функции размещения и потоковой передачи для виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="0a178-116">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="0a178-117">Сервер отчетов — предоставляет службы отчетов App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0a178-117">Reporting Server – provides App-V 5.0 reporting services.</span></span>

-   <span data-ttu-id="0a178-118">База данных отчетов — упрощает предварительное развертывание баз данных для отчетов App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0a178-118">Reporting Database – facilitates database predeployments for App-V 5.0 reporting.</span></span>

## <a href="" id="---------app-v-5-0-stand-alone-deployment"></a> <span data-ttu-id="0a178-119">Изолированное развертывание App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0a178-119">App-V 5.0 stand-alone deployment</span></span>


<span data-ttu-id="0a178-120">Автономное развертывание App-V 5,0 обеспечивает хорошую топологию для небольшого развертывания или тестовой среды.</span><span class="sxs-lookup"><span data-stu-id="0a178-120">The App-V 5.0 standalone deployment provides a good topology for a small deployment or a test environment.</span></span> <span data-ttu-id="0a178-121">При использовании этого типа реализации все серверные компоненты развертываются на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="0a178-121">When you use this type of implementation, all server components are deployed to a single computer.</span></span> <span data-ttu-id="0a178-122">Службы и связанные базы данных будут конкурировать за ресурсы на компьютере, на котором запущены компоненты App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0a178-122">The services and associated databases will compete for the resources on the computer that runs the App-V 5.0 components.</span></span> <span data-ttu-id="0a178-123">Поэтому не следует использовать эту топологию для крупных развертываний.</span><span class="sxs-lookup"><span data-stu-id="0a178-123">Therefore, you should not use this topology for larger deployments.</span></span>

[<span data-ttu-id="0a178-124">Порядок развертывания сервера App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="0a178-124">How to Deploy the App-V 5.0 Server</span></span>](how-to-deploy-the-app-v-50-server-50sp3.md)

[<span data-ttu-id="0a178-125">Развертывание сервера App-V 5.0 с помощью сценария</span><span class="sxs-lookup"><span data-stu-id="0a178-125">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

## <a href="" id="---------app-v-5-0-server-distributed-deployment"></a> <span data-ttu-id="0a178-126">Распределенное развертывание для App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="0a178-126">App-V 5.0 Server distributed deployment</span></span>


<span data-ttu-id="0a178-127">Распределенная топология развертывания может поддерживать более обширную клиентскую базу App-V 5,0, которая позволяет проще управлять средой и масштабировать ее.</span><span class="sxs-lookup"><span data-stu-id="0a178-127">The distributed deployment topology can support a large App-V 5.0 client base and it allows you to more easily manage and scale your environment.</span></span> <span data-ttu-id="0a178-128">При использовании этого типа развертывания серверные компоненты App-V 5,0 развертываются на нескольких компьютерах, основываясь на структуре и требованиях Организации.</span><span class="sxs-lookup"><span data-stu-id="0a178-128">When you use this type of deployment, the App-V 5.0 Server components are deployed across multiple computers, based on the structure and requirements of the organization.</span></span>

[<span data-ttu-id="0a178-129">Установка баз данных управления и отчетности отдельно от служб управления и отчетности</span><span class="sxs-lookup"><span data-stu-id="0a178-129">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[<span data-ttu-id="0a178-130">Установка сервера отчетности на отдельном компьютере и подключение его к базе данных</span><span class="sxs-lookup"><span data-stu-id="0a178-130">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

[<span data-ttu-id="0a178-131">Развертывание сервера App-V 5.0 с помощью сценария</span><span class="sxs-lookup"><span data-stu-id="0a178-131">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

[<span data-ttu-id="0a178-132">Установка сервера публикации на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="0a178-132">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer.md)

[<span data-ttu-id="0a178-133">Установка сервера управления на отдельном компьютере и подключение его к базе данных</span><span class="sxs-lookup"><span data-stu-id="0a178-133">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

## <span data-ttu-id="0a178-134">Использование решения для корпоративного распространения программного обеспечения (ESD) и App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0a178-134">Using an Enterprise Software Distribution (ESD) solution and App-V 5.0</span></span>


<span data-ttu-id="0a178-135">Вы также можете развернуть клиенты App-V 5,0 и пакеты с помощью ESD, не развертывая App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0a178-135">You can also deploy the App-V 5.0 clients and packages by using an ESD without having to deploy App-V 5.0.</span></span> <span data-ttu-id="0a178-136">Все возможности интеграции варьируются в зависимости от используемой ESD.</span><span class="sxs-lookup"><span data-stu-id="0a178-136">The full capabilities for integration will vary depending on the ESD that you use.</span></span>

<span data-ttu-id="0a178-137">**Примечание**  Сервер отчетов App-V 5,0 и база данных отчетов по-прежнему можно разворачивать вместе с ESD для сбора данных отчетов из клиентов App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0a178-137">**Note** The App-V 5.0 reporting server and reporting database can still be deployed alongside the ESD to collect the reporting data from the App-V 5.0 clients.</span></span> <span data-ttu-id="0a178-138">Тем не менее, другие три серверные компоненты не должны развертываться, так как они будут конфликтовать с функциями ESD.</span><span class="sxs-lookup"><span data-stu-id="0a178-138">However, the other three server components should not be deployed, because they will conflict with the ESD functionality.</span></span>

 

[<span data-ttu-id="0a178-139">Развертывание пакетов App-V 5.0 с помощью системы электронного распространения программного обеспечения (ESD)</span><span class="sxs-lookup"><span data-stu-id="0a178-139">Deploying App-V 5.0 Packages by Using Electronic Software Distribution (ESD)</span></span>](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-0-server-logs"></a> <span data-ttu-id="0a178-140">Журналы сервера App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0a178-140">App-V 5.0 Server logs</span></span>


<span data-ttu-id="0a178-141">Данные журнала сервера App-V 5,0 можно использовать для устранения неполадок, связанных с установкой и функционированием сервера, при использовании App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0a178-141">You can use App-V 5.0 server log information to help troubleshoot the server installation and operational events while using App-V 5.0.</span></span> <span data-ttu-id="0a178-142">Данные журнала, связанные с сервером, можно просмотреть в **средстве просмотра событий**.</span><span class="sxs-lookup"><span data-stu-id="0a178-142">The server-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="0a178-143">В следующей строке показан определенный путь для событий, связанных с сервером.</span><span class="sxs-lookup"><span data-stu-id="0a178-143">The following line displays the specific path for Server-related events:</span></span>

**<span data-ttu-id="0a178-144">Окно просмотра событий \ \ журналы приложений и служб \ \ Microsoft \ \ приложение V</span><span class="sxs-lookup"><span data-stu-id="0a178-144">Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V</span></span>**

<span data-ttu-id="0a178-145">Связанные журналы настройки сохраняются в следующей папке:</span><span class="sxs-lookup"><span data-stu-id="0a178-145">Associated setup logs are saved in the following directory:</span></span>

**<span data-ttu-id="0a178-146">во</span><span class="sxs-lookup"><span data-stu-id="0a178-146">%temp%</span></span>**

<span data-ttu-id="0a178-147">В приложении App-V 5,0 с пакетом обновления 3 (SP3) некоторые журналы были объединены и перемещены.</span><span class="sxs-lookup"><span data-stu-id="0a178-147">In App-V 5.0 SP3, some logs have been consolidated and moved.</span></span> <span data-ttu-id="0a178-148">Дополнительные [сведения о приложении App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="0a178-148">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <a href="" id="---------app-v-5-0-reporting"></a> <span data-ttu-id="0a178-149">Отчеты App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0a178-149">App-V 5.0 reporting</span></span>


<span data-ttu-id="0a178-150">Отчеты App-V 5,0 позволяют клиентам App-V 5,0 собирать данные, а затем отправлять их на хранение в центральном репозитории.</span><span class="sxs-lookup"><span data-stu-id="0a178-150">App-V 5.0 reporting allows App-V 5.0 clients to collect data and then send it back to be stored in a central repository.</span></span> <span data-ttu-id="0a178-151">Эти сведения можно использовать для более удобного просмотра использования виртуальных приложений в Организации.</span><span class="sxs-lookup"><span data-stu-id="0a178-151">You can use this information to get a better view of the virtual application usage within your organization.</span></span> <span data-ttu-id="0a178-152">В списке ниже перечислены некоторые типы данных, собираемые клиентом App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0a178-152">The following list displays some of the types of information the App-V 5.0 client collects:</span></span>

-   <span data-ttu-id="0a178-153">Сведения о компьютере, на котором запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0a178-153">Information about the computer that runs the App-V 5.0 client.</span></span>

-   <span data-ttu-id="0a178-154">Сведения о виртуализированных пакетах на определенном компьютере, на котором запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0a178-154">Information about virtualized packages on a specific computer that runs the App-V 5.0 client.</span></span>

-   <span data-ttu-id="0a178-155">Сведения о том, что пакет открыт и завершает работу для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a178-155">Information about package open and shutdown for a specific user.</span></span>

<span data-ttu-id="0a178-156">Сведения об отчетах будут поддерживаться до тех пор, пока они не будут успешно переданы в базу данных сервера отчетов.</span><span class="sxs-lookup"><span data-stu-id="0a178-156">The reporting information will be maintained until it is successfully sent to the reporting server database.</span></span> <span data-ttu-id="0a178-157">После внесения данных в базу данных вы можете использовать службы отчетов Microsoft SQL Server для создания необходимых отчетов.</span><span class="sxs-lookup"><span data-stu-id="0a178-157">After the data is in the database, you can use Microsoft SQL Server Reporting Services to generate any necessary reports.</span></span>

<span data-ttu-id="0a178-158">Если вы хотите получить данные отчета, необходимо использовать Microsoft SQL Server Reporting Services (SSRS), доступную в Microsoft SQL.</span><span class="sxs-lookup"><span data-stu-id="0a178-158">If you want to retrieve report information, you must use Microsoft SQL Server Reporting Services (SSRS) which is available with Microsoft SQL.</span></span> <span data-ttu-id="0a178-159">Служба SSRS не устанавливается при установке сервера отчетов App-V 5,0 и должна быть развернута отдельно для создания связанных отчетов.</span><span class="sxs-lookup"><span data-stu-id="0a178-159">SSRS is not installed when you install the App-V 5.0 reporting server and it must be deployed separately to generate the associated reports.</span></span>

<span data-ttu-id="0a178-160">Ниже приведены ссылки на дополнительные сведения [об отчетах App-V 5,0](about-app-v-50-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="0a178-160">Use the following link for more information [About App-V 5.0 Reporting](about-app-v-50-reporting.md).</span></span>

[<span data-ttu-id="0a178-161">Порядок включения отчетов в клиенте App-V 5.0 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a178-161">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

## <span data-ttu-id="0a178-162">Другие ресурсы для сервера App-V</span><span class="sxs-lookup"><span data-stu-id="0a178-162">Other resources for the App-V server</span></span>


[<span data-ttu-id="0a178-163">Развертывание App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="0a178-163">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)






 

 




