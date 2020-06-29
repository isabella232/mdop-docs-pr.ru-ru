---
title: Планирование развертывания клиента Application Virtualization Client
description: Планирование развертывания клиента Application Virtualization Client
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815952"
---
# <span data-ttu-id="fd99d-103">Планирование развертывания клиента Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="fd99d-103">Planning for Application Virtualization Client Deployment</span></span>


<span data-ttu-id="fd99d-104">После того как вы решите, как вы будете публиковать и развертывать пакеты виртуальных приложений на компьютерах конечных пользователей, вы должны спланировать развертывание программного обеспечения клиента Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="fd99d-104">After you have decided how you will publish and deploy virtual application packages to your end user computers, you should plan the deployment of the Application Virtualization Client software.</span></span>

<span data-ttu-id="fd99d-105">Клиент Application Virtualization — это компонент, который фактически запускает виртуальные приложения.</span><span class="sxs-lookup"><span data-stu-id="fd99d-105">The Application Virtualization Client is the component that actually runs the virtual applications.</span></span> <span data-ttu-id="fd99d-106">Клиент Application Virtualization позволяет пользователям взаимодействовать со значками и дважды щелкать типы файлов, чтобы запустить виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="fd99d-106">The Application Virtualization Client enables users to interact with icons and to double-click file types to start a virtual application.</span></span> <span data-ttu-id="fd99d-107">Кроме того, он обрабатывает потоковую передачу содержимого приложения с потокового сервера и кэширует его перед запуском приложения.</span><span class="sxs-lookup"><span data-stu-id="fd99d-107">It also handles streaming of the application content from a streaming server and caches it before starting the application.</span></span> <span data-ttu-id="fd99d-108">Содержимое приложения структурировано таким образом, что весь контент, необходимый для запуска приложения и обработки первоначального взаимодействия с пользователем, сначала передается на компьютер конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="fd99d-108">The application content is structured such that all the content needed to start the application and handle initial user interaction is streamed to the end user computer first.</span></span> <span data-ttu-id="fd99d-109">Существует два типа клиентского программного обеспечения виртуализации приложений: клиент Application Virtualization для служб удаленных рабочих столов (ранее — службы терминалов), который используется на серверных системах сеансов удаленных рабочих столов (RDSession Host) и клиенте Application Virtualization для настольных систем, который используется для всех остальных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="fd99d-109">There are two different types of Application Virtualization Client software: the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services), which is used on Remote Desktop Session Host (RDSession Host) server systems, and the Application Virtualization Desktop Client, which is used for all other computers.</span></span>

<span data-ttu-id="fd99d-110">Клиент Application Virtualization следует настроить во время установки либо в консоли управления Application Virtualization, либо с помощью командной строки установщика, используя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="fd99d-110">The Application Virtualization Client should be configured at installation time, either in the Application Virtualization Management Console or via the installer command line, with a number of important settings, including the following:</span></span>

-   <span data-ttu-id="fd99d-111">Расположение значков для всех приложений.</span><span class="sxs-lookup"><span data-stu-id="fd99d-111">Locations of the icons for all the applications.</span></span>

-   <span data-ttu-id="fd99d-112">Расположение OSD файла, содержащего сведения об определении пакета.</span><span class="sxs-lookup"><span data-stu-id="fd99d-112">The location of the OSD file that contains the package definition information.</span></span>

-   <span data-ttu-id="fd99d-113">Источник контента приложения.</span><span class="sxs-lookup"><span data-stu-id="fd99d-113">The application content source.</span></span>

-   <span data-ttu-id="fd99d-114">Протокол связи, который будет использоваться при извлечении вышеперечисленных элементов.</span><span class="sxs-lookup"><span data-stu-id="fd99d-114">The communications protocol to be used when retrieving the preceding items.</span></span>

-   <span data-ttu-id="fd99d-115">Используемый метод управления размером кэша и кэша.</span><span class="sxs-lookup"><span data-stu-id="fd99d-115">The cache size and cache size management method to be used.</span></span>

<span data-ttu-id="fd99d-116">Для ускорения развертывания клиентского программного обеспечения Application Virtualization при использовании решения для электронной рассылки программного обеспечения (ESD) предыдущие параметры необходимо предварительно определить заранее.</span><span class="sxs-lookup"><span data-stu-id="fd99d-116">To expedite the deployment of the Application Virtualization Client software when using an electronic software distribution (ESD) solution, the preceding settings must be defined carefully in advance.</span></span> <span data-ttu-id="fd99d-117">Это особенно важно, если у вас есть компьютеры в разных офисах, где их клиенты должны быть настроены на использование разных исходных расположений.</span><span class="sxs-lookup"><span data-stu-id="fd99d-117">This is especially important when you have computers in different offices, where their clients would need to be configured to use different source locations.</span></span>

**<span data-ttu-id="fd99d-118">Примечание.</span><span class="sxs-lookup"><span data-stu-id="fd99d-118">Note</span></span>**  
-   <span data-ttu-id="fd99d-119">Значения расположения значков и файлов OSD — это важный фактор, который следует учитывать при выборе способа публикации, будь то использование установщика Windows или SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="fd99d-119">The icon location and OSD file values are an important factor to consider when choosing your publishing method, whether using Windows Installer or SFTMIME.</span></span> <span data-ttu-id="fd99d-120">Параметр для источника контента приложения определяется выбранным методом потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="fd99d-120">The setting for the application content source is defined by your choice of streaming method.</span></span>

-   <span data-ttu-id="fd99d-121">Чтобы убедиться в том, что в кэше достаточно места для всех пакетов, которые могут быть развернуты, используйте параметр " **использовать порог свободного места на диске** " при настройке клиента, чтобы при необходимости кэш мог расти.</span><span class="sxs-lookup"><span data-stu-id="fd99d-121">To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="fd99d-122">Кроме того, вы можете заранее определить, сколько места на диске требуется для кэша App-V, и в процессе установки задать размер кэша соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="fd99d-122">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span> <span data-ttu-id="fd99d-123">Дополнительные сведения о функции управления пространством кэша можно найти в разделе **Использование функции управления пространством кэша** в руководстве по работе с Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="fd99d-123">For more information about the cache space management feature, see **How to Use the Cache Space Management Feature** in the Microsoft Application Virtualization (App-V) Operations Guide.</span></span>

-   <span data-ttu-id="fd99d-124">При выполнении операций публикации и передачи данных по HTTP (S) клиенты App-V 4,5 с пакетом обновления 1 (SP1) используют параметры прокси-сервера, настроенные в Internet Explorer на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="fd99d-124">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>

<span data-ttu-id="fd99d-125">Дополнительные сведения о настройке параметров клиентской установки можно найти в разделе [Параметры командной строки установщика клиента Application Virtualization](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fd99d-125">For more information about configuring the client installation parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

 

<span data-ttu-id="fd99d-126">Наконец, вам нужно определить, как развернуть клиентское программное обеспечение Application Virtualization для настольных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="fd99d-126">Finally, you need to determine how to deploy the Application Virtualization Desktop Client software for the desktop clients.</span></span> <span data-ttu-id="fd99d-127">Несмотря на то, что клиент виртуализации приложений для настольных компьютеров можно развернуть вручную на каждом компьютере, большинству организаций это нужно сделать с помощью автоматизированного процесса.</span><span class="sxs-lookup"><span data-stu-id="fd99d-127">Although it is possible to deploy the Application Virtualization Desktop Client manually on each computer, most organizations would need to do this through some automated process.</span></span> <span data-ttu-id="fd99d-128">В средней или крупной организации может быть система с ESD и это идеальный способ развертывания клиента.</span><span class="sxs-lookup"><span data-stu-id="fd99d-128">A medium or large organization might have an ESD system in operation, and that would be an ideal way to deploy the client.</span></span> <span data-ttu-id="fd99d-129">Если система ESD не существует, вы можете использовать стандартный способ установки программного обеспечения в своей организации.</span><span class="sxs-lookup"><span data-stu-id="fd99d-129">If no ESD system exists, you can use your standard method of installing software in your organization.</span></span> <span data-ttu-id="fd99d-130">Варианты выбора включают в себя групповую политику или различные методики создания сценариев.</span><span class="sxs-lookup"><span data-stu-id="fd99d-130">Choices include Group Policy or various scripting techniques.</span></span> <span data-ttu-id="fd99d-131">В зависимости от количества и размера Ваших офисов, этот процесс развертывания может быть сложным, и важно иметь структурированный подход к обеспечению того, чтобы все компьютеры могли получить клиент, установленный с правильной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="fd99d-131">Depending on the number and size of the offices you have, this deployment process can be complex, and it is essential that you take a structured approach to ensure all computers get a client installed with the correct configuration.</span></span>

## <span data-ttu-id="fd99d-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="fd99d-132">Related topics</span></span>


[<span data-ttu-id="fd99d-133">Планирование развертывания системы виртуализации приложений</span><span class="sxs-lookup"><span data-stu-id="fd99d-133">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

[<span data-ttu-id="fd99d-134">Установка клиента с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="fd99d-134">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="fd99d-135">Публикация виртуального приложения на клиенте</span><span class="sxs-lookup"><span data-stu-id="fd99d-135">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="fd99d-136">Обновление клиента Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="fd99d-136">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="fd99d-137">Удаление клиента App-V</span><span class="sxs-lookup"><span data-stu-id="fd99d-137">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





