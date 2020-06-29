---
title: Настройка сертификатов для обеспечения поддержки службы веб-управления App-V
description: Настройка сертификатов для обеспечения поддержки службы веб-управления App-V
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821889"
---
# <span data-ttu-id="89341-103">Настройка сертификатов для обеспечения поддержки службы веб-управления App-V</span><span class="sxs-lookup"><span data-stu-id="89341-103">Configuring Certificates to Support the App-V Web Management Service</span></span>


<span data-ttu-id="89341-104">Служба управления веб-интерфейсом App-V должна быть настроена для поддержки подключений на основе SSL для обеспечения безопасности связи.</span><span class="sxs-lookup"><span data-stu-id="89341-104">The App-V Web Management Service must be configured to support SSL-based connections to help secure the communication.</span></span> <span data-ttu-id="89341-105">Для этого процесса необходимо, чтобы на веб-сервере или компьютере, на котором установлена служба управления, был сертификат, выпущенный для службы или компьютера.</span><span class="sxs-lookup"><span data-stu-id="89341-105">This process requires that the Web server or computer on which the Management Service is installed has a certificate issued to the service or computer.</span></span>

<span data-ttu-id="89341-106">В следующих сценариях показано, как получить сертификат для этой цели:</span><span class="sxs-lookup"><span data-stu-id="89341-106">The following scenarios illustrate how to obtain a certificate for this purpose:</span></span>

1.  <span data-ttu-id="89341-107">В инфраструктуре компании уже есть инфраструктура открытых ключей (PKI), которая автоматически выдаст сертификаты компьютерам.</span><span class="sxs-lookup"><span data-stu-id="89341-107">The company infrastructure already has a public key infrastructure (PKI) in place that automatically issues certificates to computers.</span></span>

2.  <span data-ttu-id="89341-108">В инфраструктуре компании уже есть инфраструктура PKI, но она не будет автоматически выдавала сертификаты компьютерам.</span><span class="sxs-lookup"><span data-stu-id="89341-108">The company infrastructure already has a PKI in place, although it does not automatically issue certificates to computers.</span></span>

3.  <span data-ttu-id="89341-109">Инфраструктура компании не имеет PKI на своем расположении.</span><span class="sxs-lookup"><span data-stu-id="89341-109">The company infrastructure has no PKI in place.</span></span>

<span data-ttu-id="89341-110">В каждом из описанных выше сценариев метод получения сертификата отличается, но конечный результат одинаков.</span><span class="sxs-lookup"><span data-stu-id="89341-110">In each of the preceding scenarios, the method for obtaining a certificate is different, but the end result is the same.</span></span> <span data-ttu-id="89341-111">Администратор должен назначить сертификат для веб-сайта по умолчанию IIS и настроить службу управления веб-сайтом App-V для использования безопасной связи.</span><span class="sxs-lookup"><span data-stu-id="89341-111">The administrator must assign a certificate to the IIS Default Web Site and configure the App-V Web Management Service to require secure communications.</span></span>

<span data-ttu-id="89341-112">**Важно!**  Имя сертификата должно совпадать с именем сервера.</span><span class="sxs-lookup"><span data-stu-id="89341-112">**Important** The name of the certificate must match the name of the server.</span></span> <span data-ttu-id="89341-113">Рекомендуется использовать полные доменные имена (FQDN) для общего имени сертификата.</span><span class="sxs-lookup"><span data-stu-id="89341-113">It is a best practice to use fully qualified domain names (FQDNs) for the common name of the certificate.</span></span>

 

<span data-ttu-id="89341-114">Приложение App-V может использовать серверы IIS для поддержки различных конфигураций инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="89341-114">App-V can use IIS servers to support different infrastructure configurations.</span></span> <span data-ttu-id="89341-115">Дополнительные сведения о настройке серверов IIS для поддержки HTTPS см. в разделе <https://go.microsoft.com/fwlink/?LinkId=151972> .</span><span class="sxs-lookup"><span data-stu-id="89341-115">For more information about configuring IIS servers to support HTTPS, see <https://go.microsoft.com/fwlink/?LinkId=151972>.</span></span>

## <span data-ttu-id="89341-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="89341-116">Related topics</span></span>


[<span data-ttu-id="89341-117">Установка и настройка консоли управления App-V для организации более безопасной среды</span><span class="sxs-lookup"><span data-stu-id="89341-117">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 





