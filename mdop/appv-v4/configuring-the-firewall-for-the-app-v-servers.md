---
title: Настройка брандмауэра для серверов App-V Server
description: Настройка брандмауэра для серверов App-V Server
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821819"
---
# <span data-ttu-id="4fba2-103">Настройка брандмауэра для серверов App-V Server</span><span class="sxs-lookup"><span data-stu-id="4fba2-103">Configuring the Firewall for the App-V Servers</span></span>


<span data-ttu-id="4fba2-104">После установки сервера управления Microsoft Application Virtualization (App-V) или попотокового сервера в конфигурации для использования протокола RTSP или RTSP вы должны создать исключения брандмауэра для программ App-V.</span><span class="sxs-lookup"><span data-stu-id="4fba2-104">After you install the Microsoft Application Virtualization (App-V) Management Server or Streaming Server and configure it to use the RTSP or RTSPS protocol, you must create firewall exceptions for the App-V programs.</span></span>

## <span data-ttu-id="4fba2-105">Настройка исключений брандмауэра для сервера управления виртуализацией приложений</span><span class="sxs-lookup"><span data-stu-id="4fba2-105">Configuring Firewall Exceptions for Application Virtualization Management Server</span></span>


<span data-ttu-id="4fba2-106">Создайте исключение брандмауэра для **sghwdsptr.exe** и **sghwsvr.exe**.</span><span class="sxs-lookup"><span data-stu-id="4fba2-106">Create a firewall exception for **sghwdsptr.exe** and **sghwsvr.exe**.</span></span> <span data-ttu-id="4fba2-107">Эти программы находятся в папке C:\\program Files Files\\Microsoft System Center приложения virt Server\\App virt управление Server\\bin в 32-разрядной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="4fba2-107">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="4fba2-108">Если вы используете 64-разрядную версию операционной системы, она расположена в разделе C:\\program Files Files (x86) \\Microsoft System Center App Virt Management Server\\App virt Management Server\\bin.</span><span class="sxs-lookup"><span data-stu-id="4fba2-108">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin.</span></span>

## <span data-ttu-id="4fba2-109">Настройка исключений брандмауэра для потокового сервера Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="4fba2-109">Configuring Firewall Exceptions for Application Virtualization Streaming Server</span></span>


<span data-ttu-id="4fba2-110">Создайте исключение брандмауэра для **sglwdsptr.exe** и **sglwsvr.exe**.</span><span class="sxs-lookup"><span data-stu-id="4fba2-110">Create a firewall exception for **sglwdsptr.exe** and **sglwsvr.exe**.</span></span> <span data-ttu-id="4fba2-111">Эти программы находятся в папке C:\\program Files Files\\Microsoft System Center приложения virt Streaming Server\\App virt Streaming Server\\bin в 32-разрядной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="4fba2-111">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="4fba2-112">Если вы используете 64-разрядную версию операционной системы, она расположена в разделе C:\\program Files Files (x86) \\Microsoft System Center App Virt Streaming Server\\App virt Streaming Server\\bin.</span><span class="sxs-lookup"><span data-stu-id="4fba2-112">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin.</span></span>

## <span data-ttu-id="4fba2-113">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4fba2-113">Related topics</span></span>


[<span data-ttu-id="4fba2-114">Настройка серверов для развертывания на основе сервера</span><span class="sxs-lookup"><span data-stu-id="4fba2-114">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="4fba2-115">Установка и настройка приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4fba2-115">How to Install and Configure the Default Application</span></span>](how-to-install-and-configure-the-default-application.md)

 

 





