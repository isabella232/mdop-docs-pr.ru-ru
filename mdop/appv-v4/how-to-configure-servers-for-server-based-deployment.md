---
title: Настройка серверов для развертывания на основе сервера
description: Настройка серверов для развертывания на основе сервера
author: dansimp
ms.assetid: 6371c37a-46eb-44e8-ad6b-4430c866c8b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c60ae89bc42fddad8aeb6a4f6df0f2c0b4ee4f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817919"
---
# <span data-ttu-id="527cd-103">Настройка серверов для развертывания на основе сервера</span><span class="sxs-lookup"><span data-stu-id="527cd-103">How to Configure Servers for Server-Based Deployment</span></span>


<span data-ttu-id="527cd-104">В этом разделе описаны процедуры, которые можно использовать для настройки серверов управления Microsoft System Center Application Virtualization (App-V) и серверных потоков Microsoft System Center Application Virtualization, а также служб IIS и файловых серверов в соответствии с стратегии развертывания на основе сервера виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="527cd-104">This section provides procedures you can use to configure the Microsoft System Center Application Virtualization (App-V) Management Servers and Microsoft System Center Application Virtualization Streaming Servers, and the Internet Information Services (IIS) and file servers, as appropriate for your Application Virtualization Server-based deployment strategy.</span></span>

## <span data-ttu-id="527cd-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="527cd-105">In This Section</span></span>


<a href="" id="how-to-configure-the-application-virtualization-management-servers"></a>[<span data-ttu-id="527cd-106">Настройка серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="527cd-106">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)  
<span data-ttu-id="527cd-107">В этой статье приведены пошаговые инструкции по настройке серверов управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="527cd-107">Provides a step-by-step procedure for configuring the Application Virtualization Management Servers.</span></span>

<a href="" id="how-to-configure-the-application-virtualization-streaming-servers"></a>[<span data-ttu-id="527cd-108">Настройка серверов Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="527cd-108">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)  
<span data-ttu-id="527cd-109">В этой статье приведены пошаговые инструкции по настройке серверов потоковой передачи данных Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="527cd-109">Provides a step-by-step procedure for configuring the Application Virtualization Streaming Servers.</span></span>

<a href="" id="how-to-configure-the-server-for-iis"></a>[<span data-ttu-id="527cd-110">Настройка сервера для служб IIS</span><span class="sxs-lookup"><span data-stu-id="527cd-110">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)  
<span data-ttu-id="527cd-111">В этой статье приведены пошаговые инструкции по настройке сервера IIS для развертывания на сервере.</span><span class="sxs-lookup"><span data-stu-id="527cd-111">Provides a step-by-step procedure for configuring the IIS server for your server-based deployment.</span></span>

<a href="" id="how-to-configure-the-server-to-be-trusted-for-delegation"></a>[<span data-ttu-id="527cd-112">Настройка сервера для разрешения делегирования</span><span class="sxs-lookup"><span data-stu-id="527cd-112">How to Configure the Server to be Trusted for Delegation</span></span>](how-to-configure-the-server-to-be-trusted-for-delegation.md)  
<span data-ttu-id="527cd-113">Подробные инструкции о том, как настроить сервер для использования в качестве доверенного для делегирования.</span><span class="sxs-lookup"><span data-stu-id="527cd-113">Provides detailed instructions about how to configure the server to be trusted for delegation.</span></span>

<a href="" id="configuring-the-firewall-for-the-app-v-servers"></a>[<span data-ttu-id="527cd-114">Настройка брандмауэра для серверов App-V Server</span><span class="sxs-lookup"><span data-stu-id="527cd-114">Configuring the Firewall for the App-V Servers</span></span>](configuring-the-firewall-for-the-app-v-servers.md)  
<span data-ttu-id="527cd-115">Описание параметров брандмауэра, необходимых для серверов App-V.</span><span class="sxs-lookup"><span data-stu-id="527cd-115">Describes the firewall settings required for the App-V servers.</span></span>

<a href="" id="how-to-install-and-configure-the-default-application"></a>[<span data-ttu-id="527cd-116">Установка и настройка приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="527cd-116">How to Install and Configure the Default Application</span></span>](how-to-install-and-configure-the-default-application.md)  
<span data-ttu-id="527cd-117">В этой статье описано, как установить и настроить приложение по умолчанию для тестирования системы App-V.</span><span class="sxs-lookup"><span data-stu-id="527cd-117">Describes how to install and configure the default application for testing the App-V system.</span></span>

## <span data-ttu-id="527cd-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="527cd-118">Related topics</span></span>


[<span data-ttu-id="527cd-119">Обзор сценария на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="527cd-119">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)

[<span data-ttu-id="527cd-120">Сценарий на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="527cd-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="527cd-121">Установка серверов и компонентов системы</span><span class="sxs-lookup"><span data-stu-id="527cd-121">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





