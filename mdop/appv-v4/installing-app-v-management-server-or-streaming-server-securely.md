---
title: Безопасная установка сервера управления App-V и сервера потоковой передачи Streaming Server
description: Безопасная установка сервера управления App-V и сервера потоковой передачи Streaming Server
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816329"
---
# <span data-ttu-id="91a96-103">Безопасная установка сервера управления App-V и сервера потоковой передачи Streaming Server</span><span class="sxs-lookup"><span data-stu-id="91a96-103">Installing App-V Management Server or Streaming Server Securely</span></span>


<span data-ttu-id="91a96-104">В подразделах этого раздела содержатся сведения о том, как установить расширенную версию системы безопасности сервера App-V Management Server или на потоковый сервер App-V.</span><span class="sxs-lookup"><span data-stu-id="91a96-104">The topics in this section provide information for installing an enhanced security version of the App-V Management Server or the App-V Streaming Server.</span></span>

<span data-ttu-id="91a96-105">**Примечание**  Установка и Настройка серверного сервера управления App-V или потокового потока для использования усиленной безопасности (например, для защиты транспортного уровня или TLS) требует предоставления сертификата X. 509 v3 на сервере App-V.</span><span class="sxs-lookup"><span data-stu-id="91a96-105">**Note** Installing or configuring an App-V Management or Streaming Server to use enhanced security (for example, Transport Layer Security, or TLS) requires that an X.509 V3 certificate has been provisioned to the App-V server.</span></span>

 

<span data-ttu-id="91a96-106">Когда вы готовитесь к установке или настройке сервера потоков управления (Secure Management), учитывайте следующие технические требования:</span><span class="sxs-lookup"><span data-stu-id="91a96-106">When you prepare to install or configure a secure Management or Streaming Server, consider the following technical requirements:</span></span>

-   <span data-ttu-id="91a96-107">Сертификат должен быть действительным.</span><span class="sxs-lookup"><span data-stu-id="91a96-107">The certificate must be valid.</span></span> <span data-ttu-id="91a96-108">Если сертификат недействителен, клиент завершает соединение.</span><span class="sxs-lookup"><span data-stu-id="91a96-108">If the certificate is not valid, the client ends the connection.</span></span>

-   <span data-ttu-id="91a96-109">Сертификат должен содержать правильное *Расширенное использование ключа* (EKU) — проверка подлинности сервера (OID 1.3.6.1.5.5.7.3.1).</span><span class="sxs-lookup"><span data-stu-id="91a96-109">The certificate must contain the correct *Enhanced Key Usage* (EKU)—Server Authentication (OID 1.3.6.1.5.5.7.3.1).</span></span> <span data-ttu-id="91a96-110">Если сертификат не содержит этого EKU, клиент завершает соединение.</span><span class="sxs-lookup"><span data-stu-id="91a96-110">If the certificate does not contain this EKU, the client ends the connection.</span></span>

-   <span data-ttu-id="91a96-111">Полное доменное имя (FQDN) сертификата должно соответствовать серверу, на котором он установлен.</span><span class="sxs-lookup"><span data-stu-id="91a96-111">The certificate fully qualified domain name (FQDN) must match the server on which it is installed.</span></span> <span data-ttu-id="91a96-112">Например, если у клиента есть Звонок `RTSPS://Myserver.mycompany.com/content/MyApp.sft` и для него задано значение **Issued To** `Server1.mycompany.com` , клиент не будет подключаться к серверу, а сеанс завершится.</span><span class="sxs-lookup"><span data-stu-id="91a96-112">For example, if the client is calling `RTSPS://Myserver.mycompany.com/content/MyApp.sft` and the certificate **Issued To** field is set to `Server1.mycompany.com`, the client will not connect to the server and the session ends.</span></span> <span data-ttu-id="91a96-113">Пользователю сообщается об ошибке.</span><span class="sxs-lookup"><span data-stu-id="91a96-113">The failure is reported to the user.</span></span>

    <span data-ttu-id="91a96-114">**Примечание**  Если вы используете App-V в кластере балансировки нагрузки сети, необходимо настроить сертификат с дополнительными именами субъектов (SAN) для поддержки протоколов RTSP.</span><span class="sxs-lookup"><span data-stu-id="91a96-114">**Note** If you are using App-V in a Network Load Balancing cluster, you must configure the certificate with Subject Alternate Names (SANs) to support RTSPS.</span></span> <span data-ttu-id="91a96-115">Сведения о настройке центра сертификации (ЦС) и создании сертификатов с помощью сети SAN можно найти в разделе <https://go.microsoft.com/fwlink/?LinkId=133228> .</span><span class="sxs-lookup"><span data-stu-id="91a96-115">For information about configuring the certification authority (CA) and creating certificates with SANs, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

     

-   <span data-ttu-id="91a96-116">Клиент и сервер должны доверять корневому центру сертификации — центр сертификации, выдавший сертификат серверу App-V, должен быть доверенным для клиента, подключающегося к серверу.</span><span class="sxs-lookup"><span data-stu-id="91a96-116">The client and the server need to trust the root CA—The CA issuing the certificate to the App-V server must by trusted by the client connecting to the server.</span></span> <span data-ttu-id="91a96-117">В противном случае клиент завершает соединение.</span><span class="sxs-lookup"><span data-stu-id="91a96-117">If not, the client ends the connection.</span></span>

-   <span data-ttu-id="91a96-118">Чтобы разрешить учетной записи службы App-V доступ к сертификату, необходимо изменить разрешения для закрытого ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="91a96-118">The certificate’s private key must have permissions changed to allow the App-V Service account to access the certificate.</span></span> <span data-ttu-id="91a96-119">По умолчанию App-V использует учетную запись сетевой службы и по умолчанию учетной записи Network Service не предоставлены разрешения на доступ к закрытому ключу, что предотвращает безопасные подключения.</span><span class="sxs-lookup"><span data-stu-id="91a96-119">By default, App-V uses the Network Service account, and by default, the Network Service account does not have permission to access the private key, which will prevent secure connections.</span></span>

## <span data-ttu-id="91a96-120">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="91a96-120">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[<span data-ttu-id="91a96-121">Настройка сертификатов для обеспечения поддержки безопасной потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="91a96-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)  
<span data-ttu-id="91a96-122">Сведения о том, как получать, настраивать и устанавливать сертификаты для обеспечения защищенной потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="91a96-122">Provides information about obtaining, configuring, and installing certificates to support secure streaming.</span></span>

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[<span data-ttu-id="91a96-123">Изменение разрешений закрытых ключей для обеспечения поддержки сервера управления или сервера потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="91a96-123">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
<span data-ttu-id="91a96-124">В этой процедуре описаны процедуры, с помощью которых можно изменять ключи в Windows server2003 и Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="91a96-124">Provides procedures you can use to modify keys in Windows Server2003 and Windows Server2008.</span></span>

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[<span data-ttu-id="91a96-125">Настройка сертификатов для обеспечения поддержки сервера управления App-V или сервера потоковой передачи Streaming Server</span><span class="sxs-lookup"><span data-stu-id="91a96-125">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
<span data-ttu-id="91a96-126">Сведения о настройке сертификатов для серверов управления App-V или потоковой передачи данных, в том числе о настройке сертификатов для сред балансировки сетевой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="91a96-126">Provides information about configuring certificates for the App-V Management or Streaming Servers, including information about configuring certificates for Network Load Balancing environments.</span></span>

 

 





