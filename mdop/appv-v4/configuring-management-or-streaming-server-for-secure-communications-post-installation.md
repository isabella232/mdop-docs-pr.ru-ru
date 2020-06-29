---
title: Настройка сервера управления или сервера потоковой передачи для обеспечения защиты подключений после установки
description: Настройка сервера управления или сервера потоковой передачи для обеспечения защиты подключений после установки
author: dansimp
ms.assetid: 1062a213-470b-4ae2-b12f-b3e28a6ab745
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a2713f130809c431b7444f3e928a523838597a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821879"
---
# <span data-ttu-id="d6178-103">Настройка сервера управления или сервера потоковой передачи для обеспечения защиты подключений после установки</span><span class="sxs-lookup"><span data-stu-id="d6178-103">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>


<span data-ttu-id="d6178-104">Если не удалось подготовить правильный сертификат перед установкой сервера управления App-V или потокового сервера App-V, для App-V можно настроить повышенную безопасность после первоначальной установки.</span><span class="sxs-lookup"><span data-stu-id="d6178-104">If the proper certificate was not provisioned before the installation of the App-V Management Server or the App-V Streaming Server, App-V can be configured for enhanced security after the initial installation.</span></span> <span data-ttu-id="d6178-105">Сервер управления App-V можно настроить с помощью консоли управления App-V.</span><span class="sxs-lookup"><span data-stu-id="d6178-105">You can configure the App-V Management Server through the App-V Management Console.</span></span> <span data-ttu-id="d6178-106">Однако потоковый сервер App-V управляется в реестре.</span><span class="sxs-lookup"><span data-stu-id="d6178-106">However, the App-V Streaming Server is managed through the registry.</span></span> <span data-ttu-id="d6178-107">В любом случае сертификат должен содержать правильное *Использование расширенного ключа* (EKU) для проверки подлинности сервера, и сетевая служба должна иметь доступ на чтение закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="d6178-107">In either case, the certificate must include the proper *extended key usage* (EKU) for Server authentication and the Network Service must have read access to the private key.</span></span>

## <span data-ttu-id="d6178-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="d6178-108">In This Section</span></span>


<a href="" id="how-to-configure-management-server-security-post-installation"></a>[<span data-ttu-id="d6178-109">Настройка системы безопасности сервера управления после установки</span><span class="sxs-lookup"><span data-stu-id="d6178-109">How to Configure Management Server Security Post-Installation</span></span>](how-to-configure-management-server-security-post-installation.md)  
<span data-ttu-id="d6178-110">Процедура, которую можно выполнить после установки с помощью консоли управления App-V, чтобы добавить сертификат и настроить сервер управления App-V для усиления безопасности.</span><span class="sxs-lookup"><span data-stu-id="d6178-110">Provides a procedure that can be performed post-installation, using the App-V Management Console, to add the certificate and configure the App-V Management Server for enhanced security.</span></span>

<a href="" id="how-to-configure-streaming-server-security-post-installation"></a>[<span data-ttu-id="d6178-111">Настройка системы безопасности сервера потоковой передачи после установки</span><span class="sxs-lookup"><span data-stu-id="d6178-111">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)  
<span data-ttu-id="d6178-112">Предоставляет процедуру, которая может быть выполнена после установки, для добавления сертификата и настройки потокового сервера App-V для усиления безопасности.</span><span class="sxs-lookup"><span data-stu-id="d6178-112">Provides a procedure that can be performed post-installation, to add the certificate and configure the App-V Streaming Server for enhanced security.</span></span>

<a href="" id="troubleshooting-certificate-permission-issues"></a>[<span data-ttu-id="d6178-113">Устранение проблем с разрешениями сертификатов</span><span class="sxs-lookup"><span data-stu-id="d6178-113">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)  
<span data-ttu-id="d6178-114">Инструкции по устранению неполадок при отсутствии настройки закрытого ключа с использованием правильного списка ACL для сетевой службы.</span><span class="sxs-lookup"><span data-stu-id="d6178-114">Provides troubleshooting guidance for when the private key has not been configured with the proper ACL for the Network Service.</span></span>

 

 





