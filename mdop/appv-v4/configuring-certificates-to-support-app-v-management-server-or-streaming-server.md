---
title: Настройка сертификатов для обеспечения поддержки сервера управления App-V или сервера потоковой передачи Streaming Server
description: Настройка сертификатов для обеспечения поддержки сервера управления App-V или сервера потоковой передачи Streaming Server
author: dansimp
ms.assetid: 2f24e550-585e-4b7e-b486-22a3f181f543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e537244b24d7303af550b3ced8286ba2680009e7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821899"
---
# <span data-ttu-id="2d51b-103">Настройка сертификатов для обеспечения поддержки сервера управления App-V или сервера потоковой передачи Streaming Server</span><span class="sxs-lookup"><span data-stu-id="2d51b-103">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>


<span data-ttu-id="2d51b-104">После того как вы завершите процесс подготовки сертификата и измените разрешения закрытого ключа для поддержки установки App-V, вы можете запустить настройку сервера управления или потокового сервера.</span><span class="sxs-lookup"><span data-stu-id="2d51b-104">After you complete the certificate provisioning process and change the private key permissions to support the App-V installation, you can launch the setup of the Management Server or the Streaming Server.</span></span> <span data-ttu-id="2d51b-105">Если при запуске программы установки вы предоставили сертификат, мастер отобразит его на экране **режима безопасности подключения** и установлен флажок **использовать повышенную безопасность** (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="2d51b-105">During setup, if a certificate is provisioned before running the setup program, the wizard displays the certificate in the **Connection Security Mode** screen and, by default, the **Use enhanced security** check box is selected.</span></span>

<span data-ttu-id="2d51b-106">**Примечание**  Выберите сертификат, который был настроен для App-V, если для этого сервера предоставлено больше одного сертификата.</span><span class="sxs-lookup"><span data-stu-id="2d51b-106">**Note** Select the certificate that was configured for App-V if there is more than one certificate provisioned for this server.</span></span>

 

<span data-ttu-id="2d51b-107">**Важно!**  При переходе с версии 4,2 на версию 4,5 программа установки имеет возможность **использовать повышенную безопасность**; Однако если выбрать этот параметр, потоковая передача по протоколу RTSP не отключается.</span><span class="sxs-lookup"><span data-stu-id="2d51b-107">**Important** When upgrading from version 4.2 to version 4.5, the setup has an option for **Use enhanced security**; however, selecting this option will not disable streaming over RTSP.</span></span> <span data-ttu-id="2d51b-108">Чтобы отключить протокол RTSP после установки, необходимо использовать консоль управления.</span><span class="sxs-lookup"><span data-stu-id="2d51b-108">You must use the Management Console to disable RTSP after installation.</span></span>

 

<span data-ttu-id="2d51b-109">Выберите порт TCP, который служба будет использовать для связи с клиентами.</span><span class="sxs-lookup"><span data-stu-id="2d51b-109">Select the TCP port that the service will use for client communications.</span></span> <span data-ttu-id="2d51b-110">Портом по умолчанию является TCP 322; Однако вы можете изменить порт на настраиваемый для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="2d51b-110">The default port is TCP 322; however, you can change the port to a custom port for your environment.</span></span>

<span data-ttu-id="2d51b-111">Оставшиеся действия мастера выполняются так же, как и при развертывании сервера управления App-V или потоковой передачи данных без использования **улучшенной функции безопасности** .</span><span class="sxs-lookup"><span data-stu-id="2d51b-111">The remaining steps of the wizard are the same as if you were deploying an App-V Management or Streaming Server without using the **Enhanced security** feature.</span></span>

## <span data-ttu-id="2d51b-112">Настройка сертификатов для сред балансировки сетевой нагрузки</span><span class="sxs-lookup"><span data-stu-id="2d51b-112">Configuring Certificates for NLB Environments</span></span>


<span data-ttu-id="2d51b-113">Для поддержки больших предприятий, как правило, сервер управления помещается в кластер балансировки сетевой нагрузки (NLB) для поддержки большого количества подключений.</span><span class="sxs-lookup"><span data-stu-id="2d51b-113">To support large enterprises, often the Management Server is placed into a Network Load Balancing (NLB) cluster to support the large number of connections.</span></span> <span data-ttu-id="2d51b-114">Для этого необходимы как минимум два сервера управления, которые представляют собой один сервер управления.</span><span class="sxs-lookup"><span data-stu-id="2d51b-114">This requires at least two Management Servers that appear to be a single Management Server.</span></span> <span data-ttu-id="2d51b-115">Если в вашей среде используется кластер NLB с несколькими серверами управления, требуется дополнительная конфигурация сертификата, используемого для кластера NLB.</span><span class="sxs-lookup"><span data-stu-id="2d51b-115">When your environment uses an NLB cluster with several Management Servers, you need an advanced configuration of the certificate used for the NLB cluster.</span></span>

<span data-ttu-id="2d51b-116">Сертификат App-V отправляется в центр сертификации (ЦС), настроенный на компьютере под управлением Windows server2003.</span><span class="sxs-lookup"><span data-stu-id="2d51b-116">The App-V certificate is submitted to a certification authority (CA) that is configured on a computer running Windows Server2003.</span></span> <span data-ttu-id="2d51b-117">Сеть хранения данных позволяет подключаться к определенному серверу управления NLB-кластерным именем, используя имя DNS, которое может отличаться от реальных имен компьютеров, так как в этом случае может быть до 32 серверов, которые включают NLB-кластер.</span><span class="sxs-lookup"><span data-stu-id="2d51b-117">The SAN lets you connect to a specific Management Server NLB cluster host name by using a Domain Name System (DNS) name that might differ from the actual computer names, because there can be up to 32 servers that comprise the NLB cluster.</span></span>

<span data-ttu-id="2d51b-118">Эти настройки необходимы только при использовании кластера NLB.</span><span class="sxs-lookup"><span data-stu-id="2d51b-118">This configuration is necessary only when using an NLB cluster.</span></span> <span data-ttu-id="2d51b-119">Когда клиент подключается к серверу, он будет подключаться с помощью полного доменного имени (FQDN) NLB-кластера, а не FQDN отдельного сервера.</span><span class="sxs-lookup"><span data-stu-id="2d51b-119">When the client connects to the server, it will connect using the fully qualified domain name (FQDN) of the NLB cluster and not the FQDN of an individual server.</span></span> <span data-ttu-id="2d51b-120">Если вы не добавите свойство SAN с полным доменным именем на узлы сервера в кластере, все клиентские соединения отклоняются, так как общее имя сертификата не совпадает с именем сервера.</span><span class="sxs-lookup"><span data-stu-id="2d51b-120">If you do not add the SAN property with the FQDN of the server nodes in the cluster, all client connections are refused because the common name of the certificate won’t match the server name.</span></span>

<span data-ttu-id="2d51b-121">Более подробные сведения о настройке сертификатов с помощью атрибута SAN можно найти в разделе <https://go.microsoft.com/fwlink/?LinkId=133228> .</span><span class="sxs-lookup"><span data-stu-id="2d51b-121">For more detailed information about configuring certificates with the SAN attribute, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

## <span data-ttu-id="2d51b-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2d51b-122">Related topics</span></span>


[<span data-ttu-id="2d51b-123">Настройка сертификатов для обеспечения поддержки безопасной потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="2d51b-123">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

[<span data-ttu-id="2d51b-124">Изменение разрешений закрытых ключей для обеспечения поддержки сервера управления или сервера потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="2d51b-124">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





