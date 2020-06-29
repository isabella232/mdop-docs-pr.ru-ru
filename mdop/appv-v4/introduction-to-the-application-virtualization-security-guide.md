---
title: Введение в руководство по безопасности Application Virtualization
description: Введение в руководство по безопасности Application Virtualization
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816269"
---
# <span data-ttu-id="9dc81-103">Введение в руководство по безопасности Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9dc81-103">Introduction to the Application Virtualization Security Guide</span></span>


<span data-ttu-id="9dc81-104">Это руководство по безопасности Microsoft Application Virtualization (App-V) содержит инструкции для администраторов, которые отвечают за настройку функций безопасности, выбранных для развертывания App-V.</span><span class="sxs-lookup"><span data-stu-id="9dc81-104">This Microsoft Application Virtualization (App-V) security guide provides instructions for administrators who are responsible for configuring the security features that were selected for the App-V deployment.</span></span>

<span data-ttu-id="9dc81-105">**Примечание**  В этой документации не предоставлены рекомендации по выбору конкретных параметров безопасности.</span><span class="sxs-lookup"><span data-stu-id="9dc81-105">**Note** This documentation does not provide guidance for choosing the specific security options.</span></span> <span data-ttu-id="9dc81-106">Эта информация предоставляется в техническом документе рекомендации по обеспечению безопасности для App-V, доступного по адресу <https://go.microsoft.com/fwlink/?LinkId=127120> .</span><span class="sxs-lookup"><span data-stu-id="9dc81-106">That information is provided in the App-V Security Best Practices white paper available at <https://go.microsoft.com/fwlink/?LinkId=127120>.</span></span>

 

<span data-ttu-id="9dc81-107">Администратор App-V, использующий это руководство, должен ознакомиться со следующими технологиями, связанными с безопасностью:</span><span class="sxs-lookup"><span data-stu-id="9dc81-107">As an App-V administrator using this guide, you should be familiar with the following security-related technologies:</span></span>

-   <span data-ttu-id="9dc81-108">Доменные службы Active Directory</span><span class="sxs-lookup"><span data-stu-id="9dc81-108">Active Directory Domain Services</span></span>

-   <span data-ttu-id="9dc81-109">Инфраструктура открытых ключей (PKI)</span><span class="sxs-lookup"><span data-stu-id="9dc81-109">Public key infrastructure (PKI)</span></span>

-   <span data-ttu-id="9dc81-110">IP-безопасность (IPsec)</span><span class="sxs-lookup"><span data-stu-id="9dc81-110">Internet Protocol Security (IPsec)</span></span>

-   <span data-ttu-id="9dc81-111">Групповые политики</span><span class="sxs-lookup"><span data-stu-id="9dc81-111">Group Policies</span></span>

-   <span data-ttu-id="9dc81-112">Информационные службы Интернета (IIS)</span><span class="sxs-lookup"><span data-stu-id="9dc81-112">Internet Information Services (IIS)</span></span>

## <span data-ttu-id="9dc81-113">Компоненты инфраструктуры APP-V</span><span class="sxs-lookup"><span data-stu-id="9dc81-113">APP-V Infrastructure Components</span></span>


<span data-ttu-id="9dc81-114">При планировании среды App-V с улучшенной безопасностью вы можете использовать несколько различных моделей инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9dc81-114">When planning an enhanced security App-V environment, you can consider several different infrastructure models.</span></span>

<span data-ttu-id="9dc81-115">**Примечание**  Дополнительные сведения о моделях инфраструктуры App-V можно найти в следующей документации:</span><span class="sxs-lookup"><span data-stu-id="9dc81-115">**Note** For more information about App-V infrastructure models, see the following documentation:</span></span>

-   [<span data-ttu-id="9dc81-116">Руководство по планированию и развертыванию App-V</span><span class="sxs-lookup"><span data-stu-id="9dc81-116">App-V Planning and Deployment Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [<span data-ttu-id="9dc81-117">Серия руководств по планированию инфраструктуры и проектированию</span><span class="sxs-lookup"><span data-stu-id="9dc81-117">Infrastructure Planning and Design Guide Series</span></span>](https://go.microsoft.com/fwlink/?LinkId=151986)

 

<span data-ttu-id="9dc81-118">В этих моделях используются некоторые, но, возможно, не все компоненты App-V, показанные на приведенном ниже рисунке.</span><span class="sxs-lookup"><span data-stu-id="9dc81-118">These models utilize some but possibly not all of the App-V components depicted in the following illustration.</span></span>

![Схема Office для подразделения App-v](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a><span data-ttu-id="9dc81-120">Сервер управления виртуализацией приложений (App-V)</span><span class="sxs-lookup"><span data-stu-id="9dc81-120">Application Virtualization (App-V) Management Server</span></span>  
<span data-ttu-id="9dc81-121">Сервер управления App-V Streaming отправляет содержимое пакета и публикует в клиенте App-V сочетания клавиш и сопоставления типов файлов.</span><span class="sxs-lookup"><span data-stu-id="9dc81-121">The App-V Management Server streams the package content and publishes the shortcuts and file-type associations to the App-V Client.</span></span> <span data-ttu-id="9dc81-122">Сервер управления App-V также поддерживает активное обновление, Управление лицензиями и базу данных, которые можно использовать для создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="9dc81-122">The App-V Management Server also supports active upgrade, license management, and a database that can be used for reporting.</span></span>

<a href="" id="application-virtualization--app-v--streaming-server"></a><span data-ttu-id="9dc81-123">Потоковый сервер Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="9dc81-123">Application Virtualization (App-V) Streaming Server</span></span>  
<span data-ttu-id="9dc81-124">Потоковый сервер App-V размещает пакеты для потоковой передачи клиентам App-V в средах, например в филиалах, где пропускная способность соединения с сервером управления App-V недостаточна для потоковой передачи содержимого клиентам.</span><span class="sxs-lookup"><span data-stu-id="9dc81-124">The App-V Streaming Server hosts the packages for streaming to App-V Clients in environments such as branch offices, where the bandwidth of the connection to the App-V Management Server is insufficient for streaming package content to clients.</span></span> <span data-ttu-id="9dc81-125">Потоковый сервер содержит только потоковую функцию и не предоставляет консоль управления App-V или веб-службе управления App-V.</span><span class="sxs-lookup"><span data-stu-id="9dc81-125">The Streaming Server contains only streaming functionality and does not provide you with the App-V Management Console or the App-V Management Web Service.</span></span>

<a href="" id="application-virtualization--app-v--data-store"></a><span data-ttu-id="9dc81-126">Хранилище данных Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="9dc81-126">Application Virtualization (App-V) Data Store</span></span>  
<span data-ttu-id="9dc81-127">Хранилище данных App-V в базе данных SQL сохраняет информацию, связанную с инфраструктурой App-V.</span><span class="sxs-lookup"><span data-stu-id="9dc81-127">The App-V data store, in the SQL database, retains information related to the App-V infrastructure.</span></span> <span data-ttu-id="9dc81-128">Данные в хранилище данных App-V включают все записи приложений, назначения приложений и группы, управляющие средой Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="9dc81-128">The information in the App-V data store includes all application records, application assignments, and which groups manage the Application Virtualization environment.</span></span>

<a href="" id="application-virtualization--app-v--management-service"></a><span data-ttu-id="9dc81-129">Служба управления виртуализацией приложений (App-V)</span><span class="sxs-lookup"><span data-stu-id="9dc81-129">Application Virtualization (App-V) Management Service</span></span>  
<span data-ttu-id="9dc81-130">Служба управления App-V передает запросы на чтение и запись в хранилище данных Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="9dc81-130">The App-V Management Service communicates read/write requests to the Application Virtualization data store.</span></span> <span data-ttu-id="9dc81-131">Этот компонент может быть установлен на том же компьютере, что и сервер App-V Management, либо на отдельном компьютере, на котором установлены службы IIS.</span><span class="sxs-lookup"><span data-stu-id="9dc81-131">This component can be installed on the same computer as the App-V Management Server or on a separate computer with IIS installed.</span></span>

<a href="" id="application-virtualization--app-v--management-console"></a><span data-ttu-id="9dc81-132">Консоль управления Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="9dc81-132">Application Virtualization (App-V) Management Console</span></span>  
<span data-ttu-id="9dc81-133">Консоль управления App-V — это средство управления с помощью оснастки для администрирования сервера App-V.</span><span class="sxs-lookup"><span data-stu-id="9dc81-133">The App-V Management Console is a snap-in management utility for App-V Server administration.</span></span> <span data-ttu-id="9dc81-134">Этот компонент может быть установлен на том же компьютере, что и сервер App-V, либо на отдельной рабочей станции с MMC 3.0 и. Установлено приложение NET 2.0.</span><span class="sxs-lookup"><span data-stu-id="9dc81-134">This component can be installed on the same computer as the App-V Server or on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span>

<a href="" id="application-virtualization--app-v--sequencer"></a><span data-ttu-id="9dc81-135">Секвенсор Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="9dc81-135">Application Virtualization (App-V) Sequencer</span></span>  
<span data-ttu-id="9dc81-136">Секвенсор App-V отслеживает и захватывает установку приложений и создает пакеты виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="9dc81-136">The App-V Sequencer monitors and captures the installation of applications and creates virtual application packages.</span></span> <span data-ttu-id="9dc81-137">Результат работы секвенсора состоит из значка приложения, файла OSD, содержащего сведения о определении приложения, файла манифеста пакета и SFT-файла, содержащего файлы содержимого приложения.</span><span class="sxs-lookup"><span data-stu-id="9dc81-137">The output of the Sequencer consists of the application icon, the OSD file containing application definition information, a package manifest file, and an SFT file containing the application’s content files.</span></span> <span data-ttu-id="9dc81-138">Кроме того, можно создать файл установщика Windows для установки пакета без использования инфраструктуры App-V.</span><span class="sxs-lookup"><span data-stu-id="9dc81-138">Optionally, a Windows Installer file can be created for installing the package without using the App-V infrastructure.</span></span>

<a href="" id="application-virtualization--app-v--client"></a><span data-ttu-id="9dc81-139">Клиент Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="9dc81-139">Application Virtualization (App-V) Client</span></span>  
<span data-ttu-id="9dc81-140">Клиент App-V установлен на клиентском компьютере App-V или на клиентском компьютере служб терминалов App-V.</span><span class="sxs-lookup"><span data-stu-id="9dc81-140">The App-V Client is installed on the App-V Desktop Client computer or on the App-V Terminal Services Client computer.</span></span> <span data-ttu-id="9dc81-141">Она предоставляет виртуальную среду для виртуальных пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="9dc81-141">It provides the virtual environment for the virtual application packages.</span></span> <span data-ttu-id="9dc81-142">Клиент App-V управляет потоковой передачей пакета в кэш, обновление публикации виртуальных приложений и взаимодействие с серверами Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="9dc81-142">The App-V Client manages the package streaming to the cache, virtual application publishing refresh, and interaction with the Application Virtualization Servers.</span></span>

 

 





