---
title: Сценарий на основе использования сервера Application Virtualization Server
description: Сценарий на основе использования сервера Application Virtualization Server
author: dansimp
ms.assetid: 10ed0b18-087d-470f-951b-5083f4cb076f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6699bdc734258f67e4938e33266a2f061531939
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819529"
---
# <span data-ttu-id="e08ce-103">Сценарий на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="e08ce-103">Application Virtualization Server-Based Scenario</span></span>


<span data-ttu-id="e08ce-104">Если вы планируете использовать серверный сценарий развертывания для среды Microsoft Application Virtualization (App-V), необходимо понимать различия между сервером управления виртуализацией приложений и потоком данных сервера в приложении Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="e08ce-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization (App-V) environment, you should understand the differences between the Application Virtualization Management Server and the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="e08ce-105">В этом разделе описаны эти различия, а также сведения о методах доставки пакетов, протоколах передачи и внешних компонентах, которые необходимо учитывать при продолжении развертывания.</span><span class="sxs-lookup"><span data-stu-id="e08ce-105">The topics in this section describe those differences and also provide information about package delivery methods, transmission protocols, and external components that you have to consider as you continue with your deployment.</span></span> <span data-ttu-id="e08ce-106">Этот раздел также содержит пошаговые инструкции по установке и настройке сервера управления App-V и потоковых серверов Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="e08ce-106">This section also provides step-by-step procedures for installing and configuring the App-V Management Server and the Application Virtualization Streaming Servers.</span></span>

## <span data-ttu-id="e08ce-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="e08ce-107">In This Section</span></span>


<a href="" id="application-virtualization-server-based-scenario-overview"></a>[<span data-ttu-id="e08ce-108">Обзор сценария на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="e08ce-108">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)  
<span data-ttu-id="e08ce-109">Предоставляет важные сведения о развертывании сервера управления виртуализацией приложений, сервера потоковой передачи данных Application Virtualization и методах доставки, протоколов и внешних компонентов, относящихся к плану развертывания на основе сервера.</span><span class="sxs-lookup"><span data-stu-id="e08ce-109">Provides important deployment information about the Application Virtualization Management Server, the Application Virtualization Streaming Server, and the package delivery methods, protocols, and external components relevant to your server-based deployment plan.</span></span>

<a href="" id="how-to-install-the-servers-and-system-components"></a>[<span data-ttu-id="e08ce-110">Установка серверов и компонентов системы</span><span class="sxs-lookup"><span data-stu-id="e08ce-110">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)  
<span data-ttu-id="e08ce-111">В этой статье описано, как установить компоненты платформы Microsoft Application Virtualization, необходимые для серверного развертывания.</span><span class="sxs-lookup"><span data-stu-id="e08ce-111">Describes how to install the Microsoft Application Virtualization platform components required for your server-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-server-based-deployment"></a>[<span data-ttu-id="e08ce-112">Настройка серверов для развертывания на основе сервера</span><span class="sxs-lookup"><span data-stu-id="e08ce-112">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)  
<span data-ttu-id="e08ce-113">В этой статье описано, как настроить сервер управления виртуализацией приложений, сервер потоковой передачи данных Application Integration (IIS) и файловый сервер.</span><span class="sxs-lookup"><span data-stu-id="e08ce-113">Describes how to configure the Application Virtualization Management Server, the Application Virtualization Streaming Server, the Internet Information Integration (IIS) server, and the file server.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-"></a>[<span data-ttu-id="e08ce-114">Настройка "нередактируемого" кэша в клиенте App-V (VDI)</span><span class="sxs-lookup"><span data-stu-id="e08ce-114">How to Configure a Read-only Cache on the App-V Client (VDI)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-.md)  
<span data-ttu-id="e08ce-115">В этой статье описано, как настроить клиент App-V на использование кэша только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e08ce-115">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--rds-"></a>[<span data-ttu-id="e08ce-116">Настройка "нередактируемого" кэша в клиенте App-V (RDS)</span><span class="sxs-lookup"><span data-stu-id="e08ce-116">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--rds--sp1.md)  
<span data-ttu-id="e08ce-117">В этой статье описано, как настроить клиент App-V на использование кэша только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e08ce-117">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v"></a>[<span data-ttu-id="e08ce-118">Настройка поддержки зеркального отображения Microsoft SQL Server для App-V</span><span class="sxs-lookup"><span data-stu-id="e08ce-118">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)  
<span data-ttu-id="e08ce-119">В этой статье описано, как настроить зеркальное отображение базы данных с помощью Microsoft SQL Server для системы App-V.</span><span class="sxs-lookup"><span data-stu-id="e08ce-119">Describes how to configure database mirroring by using Microsoft SQL Server for your App-V system.</span></span>

## <span data-ttu-id="e08ce-120">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="e08ce-120">Reference</span></span>


[<span data-ttu-id="e08ce-121">Параметры командной строки установщика клиента Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="e08ce-121">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="e08ce-122">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="e08ce-122">Related Sections</span></span>


[<span data-ttu-id="e08ce-123">Сценарий на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="e08ce-123">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

## <span data-ttu-id="e08ce-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e08ce-124">Related topics</span></span>


[<span data-ttu-id="e08ce-125">Рекомендации перед развертыванием и обновлением Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="e08ce-125">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="e08ce-126">Сценарий изолированной доставки для клиентов Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="e08ce-126">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





