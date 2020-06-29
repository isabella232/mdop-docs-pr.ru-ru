---
title: Сценарий на основе электронного распространения программного обеспечения
description: Сценарий на основе электронного распространения программного обеспечения
author: dansimp
ms.assetid: 18be0f8d-60ee-449b-aa83-93c86d1a908e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 52b9a30f2b1d403ec41090252f331a984225fd19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821592"
---
# <span data-ttu-id="2ae74-103">Сценарий на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="2ae74-103">Electronic Software Distribution-Based Scenario</span></span>


<span data-ttu-id="2ae74-104">Если вы планируете использовать сценарий развертывания с помощью электронного программного обеспечения (ESD) для вашей среды виртуализации приложений (Майкрософт), важно понимать факторы, в которых они распространяются, и которые затрагиваются этим решением.</span><span class="sxs-lookup"><span data-stu-id="2ae74-104">If you plan to use an electronic software distribution (ESD) deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="2ae74-105">В этом разделе описывается сценарий ESD и предоставляются сведения о методах доставки пакетов, протоколах передачи и внешних компонентах, которые необходимо предусмотреть в стратегии развертывания.</span><span class="sxs-lookup"><span data-stu-id="2ae74-105">The topics in this section describe the ESD scenario and provide information about package delivery methods, transmission protocols, and external components that you will need to consider in your deployment strategy.</span></span> <span data-ttu-id="2ae74-106">Вы также можете использовать процедуры из этого раздела, чтобы завершить развертывание, на этапе настройки сервера на этапе проверки развертывания.</span><span class="sxs-lookup"><span data-stu-id="2ae74-106">You can also use the procedures in this section to complete your deployment, from the server configuration phase through the deployment verification phase.</span></span>

## <span data-ttu-id="2ae74-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="2ae74-107">In This Section</span></span>


<a href="" id="electronic-software-distribution-based-scenario-overview"></a>[<span data-ttu-id="2ae74-108">Обзор сценария на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="2ae74-108">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)  
<span data-ttu-id="2ae74-109">Содержит важную информацию о методах публикации и потоковой передачи, которые можно использовать для развертывания с помощью ESD.</span><span class="sxs-lookup"><span data-stu-id="2ae74-109">Provides important information about the publishing and streaming methods you can use for an ESD-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-esd-based-deployment"></a>[<span data-ttu-id="2ae74-110">Настройка серверов для развертывания на основе ESD</span><span class="sxs-lookup"><span data-stu-id="2ae74-110">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)  
<span data-ttu-id="2ae74-111">В этом разделе описаны процедуры, которые можно использовать для настройки почтовых серверов виртуализации приложений, сервера IIS и файлового сервера для стратегии развертывания на основе электронного распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="2ae74-111">This section provides procedures you can use to configure the Application Virtualization Streaming Servers, the IIS server, and the file server for your electronic software distribution–based deployment strategy.</span></span>

<a href="" id="how-to-install-the-client-by-using-the-command-line"></a>[<span data-ttu-id="2ae74-112">Установка клиента с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="2ae74-112">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)  
<span data-ttu-id="2ae74-113">Предоставляет инструкции командной строки для установки клиента Application Virtualization с помощью setup.exe или setup.msi файла.</span><span class="sxs-lookup"><span data-stu-id="2ae74-113">Provides command-line procedures for installing the Application Virtualization Client, using either the setup.exe or the setup.msi file.</span></span>

<a href="" id="how-to-uninstall-the-app-v-client"></a>[<span data-ttu-id="2ae74-114">Удаление клиента App-V</span><span class="sxs-lookup"><span data-stu-id="2ae74-114">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)  
<span data-ttu-id="2ae74-115">В этой статье приведены пошаговые инструкции, которые можно использовать для подтверждения того, что клиент Application Virtualization установлен и работает правильно.</span><span class="sxs-lookup"><span data-stu-id="2ae74-115">Provides a step-by-step procedure you can use to confirm that the Application Virtualization Client has been installed and is functioning correctly.</span></span>

<a href="" id="how-to-publish-a-virtual-application-on-the-client"></a>[<span data-ttu-id="2ae74-116">Публикация виртуального приложения на клиенте</span><span class="sxs-lookup"><span data-stu-id="2ae74-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)  
<span data-ttu-id="2ae74-117">Инструкции командной строки, которые можно использовать для публикации пакета приложения с помощью установщика Windows или SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="2ae74-117">Provides command-line procedures for publishing an application package, using either Windows Installer or SFTMIME.</span></span>

## <span data-ttu-id="2ae74-118">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="2ae74-118">Reference</span></span>


[<span data-ttu-id="2ae74-119">Параметры командной строки установщика клиента Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="2ae74-119">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="2ae74-120">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="2ae74-120">Related Sections</span></span>


[<span data-ttu-id="2ae74-121">Сценарий на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="2ae74-121">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

## <span data-ttu-id="2ae74-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2ae74-122">Related topics</span></span>


[<span data-ttu-id="2ae74-123">Рекомендации перед развертыванием и обновлением Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="2ae74-123">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="2ae74-124">Сценарий изолированной доставки для клиентов Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="2ae74-124">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





