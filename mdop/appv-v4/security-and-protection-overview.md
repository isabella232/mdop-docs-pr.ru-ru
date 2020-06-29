---
title: Обзор защиты и безопасности
description: Обзор защиты и безопасности
author: dansimp
ms.assetid: a43e1c53-7936-4d48-a110-0be26c8e9d97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b08b7dcb3defa8a01a4fd8a3e7234b5ac2956c4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815659"
---
# <span data-ttu-id="c04c4-103">Обзор защиты и безопасности</span><span class="sxs-lookup"><span data-stu-id="c04c4-103">Security and Protection Overview</span></span>


<span data-ttu-id="c04c4-104">Microsoft Application Virtualization 4.5 предоставляет следующие улучшенные функции безопасности, помогающие планировать и реализовывать более надежную стратегию развертывания.</span><span class="sxs-lookup"><span data-stu-id="c04c4-104">Microsoft Application Virtualization4.5 provides the following enhanced security features to help you plan and implement a more secure deployment strategy:</span></span>

-   <span data-ttu-id="c04c4-105">Виртуализация приложений теперь поддерживает TLS-безопасность с помощью сертификатов X. 509 v3.</span><span class="sxs-lookup"><span data-stu-id="c04c4-105">Application Virtualization now supports Transport Layer Security (TLS) using X.509 V3 certificates.</span></span> <span data-ttu-id="c04c4-106">При условии, что сертификат сервера был подготовлен к запланированному управлению виртуализацией приложения или потоковому серверу, при установке по умолчанию будет использоваться Secure с протоколом RTSP по порту 322.</span><span class="sxs-lookup"><span data-stu-id="c04c4-106">Provided that a server certificate has been provisioned to the planned Application Virtualization Management or Streaming Server, the installation will default to secure, using the RTSPS protocol over port 322.</span></span> <span data-ttu-id="c04c4-107">Использование протоколов RTSP обеспечивает подписывание и шифрование связи между серверами Application Virtualization и клиентами Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="c04c4-107">Using RTSPS ensures that communication between the Application Virtualization Servers and the Application Virtualization Clients is signed and encrypted.</span></span> <span data-ttu-id="c04c4-108">Если при установке сервера Application Virtualization сертификат не назначен на сервер, для связи будет задано значение RTSP через порт 554.</span><span class="sxs-lookup"><span data-stu-id="c04c4-108">If no certificate is assigned to the server during the Application Virtualization Server installation, the communication will be set to RTSP over port 554.</span></span>

    **<span data-ttu-id="c04c4-109">Примечание о безопасности.</span><span class="sxs-lookup"><span data-stu-id="c04c4-109">Security Note:</span></span>**

    <span data-ttu-id="c04c4-110">Для обеспечения безопасной настройки сервера необходимо убедиться, что порты RTSP отключены, даже если у вас есть все пакеты, настроенные на использование протоколов RTSP.</span><span class="sxs-lookup"><span data-stu-id="c04c4-110">To help provide a secure setup of the server, you must make sure that RTSP ports are disabled even if you have all packages configured to use RTSPS.</span></span>

    <span data-ttu-id="c04c4-111">Если вы добавите на сервер сертификаты безопасности после установки сервера, возможно, сервер не обнаружит сертификаты.</span><span class="sxs-lookup"><span data-stu-id="c04c4-111">If you add security certificates to the server after installing the server, the server might not detect the certificates.</span></span> <span data-ttu-id="c04c4-112">Чтобы обеспечить обнаружение сертификата безопасности, перезапустите сервер после добавления сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c04c4-112">To help ensure security certificate detection, restart the server after adding the certificates.</span></span>

-   <span data-ttu-id="c04c4-113">Клиент должен быть настроен на использование одного и того же протокола и порта, чем сервер, или он не сможет взаимодействовать с сервером.</span><span class="sxs-lookup"><span data-stu-id="c04c4-113">The client must be configured to use the same protocol and port as the server, or it will not be able to communicate with the server.</span></span> <span data-ttu-id="c04c4-114">Клиент также должен доверять поставщику сертификата и поставляется с несколькими основными поставщиками в доверенном корневом хранилище.</span><span class="sxs-lookup"><span data-stu-id="c04c4-114">The client must also trust the issuer of the certificate and ships with several of the primary providers in its Trusted Root Store.</span></span> <span data-ttu-id="c04c4-115">Вы можете использовать самозаверяющие сертификаты, но вам нужно будет обновить их.</span><span class="sxs-lookup"><span data-stu-id="c04c4-115">You can use self-signed certificates, but you will need to update the clients.</span></span>

-   <span data-ttu-id="c04c4-116">При настройке серверов IIS на использование протокола HTTPS для потоковой передачи данных необходимо настроить SSL на сервере IIS и подготовить сертификат для сервера.</span><span class="sxs-lookup"><span data-stu-id="c04c4-116">When configuring IIS servers to use the HTTPS protocol for streaming, you will need to set up Secure Sockets Layer (SSL) on the IIS server and provision the certificate for the server.</span></span> <span data-ttu-id="c04c4-117">Кроме того, клиентам необходимо настроить доверительные отношения с корневым центром сертификации, который выдал сертификат сервера.</span><span class="sxs-lookup"><span data-stu-id="c04c4-117">The clients will also need to be configured to trust the root certification authority that issued the server certificate.</span></span>

-   <span data-ttu-id="c04c4-118">Проверка подлинности Kerberos добавлена в Microsoft Application Virtualization как механизм проверки подлинности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c04c4-118">Kerberos authentication has been added to Microsoft Application Virtualization as the default authentication mechanism.</span></span> <span data-ttu-id="c04c4-119">Более ранние версии использовали для проверки подлинности NTLM v2.</span><span class="sxs-lookup"><span data-stu-id="c04c4-119">Earlier versions relied upon NTLM V2 for authentication.</span></span> <span data-ttu-id="c04c4-120">Использование проверки подлинности Kerberos повысит безопасность связи между клиентом и сервером Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="c04c4-120">Using Kerberos Authentication strengthens the security of the communication between the client and the Application Virtualization server.</span></span> <span data-ttu-id="c04c4-121">Когда подключение инициируется клиентом, сервер Application Virtualization проверяет билет сеанса с помощью центра распространения ключей (KDC).</span><span class="sxs-lookup"><span data-stu-id="c04c4-121">When a connection has been initiated from the client, the Application Virtualization Server verifies the session ticket with the Key Distribution Center (KDC).</span></span>

-   <span data-ttu-id="c04c4-122">Из-за поддержки использования сертификатов сервера и использования протоколов RTSP или HTTPS теперь можно поддерживать клиентов за пределами корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="c04c4-122">Because of the support for using server certificates and using the RTSPS or HTTPS protocols, you can now support clients outside of the corporate network.</span></span> <span data-ttu-id="c04c4-123">Это поможет устранить необходимость настройки безопасного подключения к корпоративной сети (VPN, RAS и т. д.) перед запуском подготовленных приложений виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="c04c4-123">This can help eliminate the need for mobile users to set up a secure connection to the corporate network (VPN, RAS, and so on) prior to launching Application Virtualization provisioned applications.</span></span>

<span data-ttu-id="c04c4-124">Ниже перечислены некоторые важные соображения, которые необходимо учитывать при безопасности.</span><span class="sxs-lookup"><span data-stu-id="c04c4-124">Other important security considerations to consider include the following:</span></span>

-   <span data-ttu-id="c04c4-125">Всегда обновляйте серверы, чтобы они были полностью обновлены и защищены.</span><span class="sxs-lookup"><span data-stu-id="c04c4-125">Always keep servers fully updated and protected.</span></span>

-   <span data-ttu-id="c04c4-126">Чтобы добавить сертификат для обеспечения более безопасной связи с сервером управления виртуализацией приложений, должны быть выполнены указанные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="c04c4-126">To add a certificate to enable more secure communications to the Application Virtualization Management Server, the following criteria must be met:</span></span>

    -   <span data-ttu-id="c04c4-127">Пользователь, который будет добавлять сертификат, должен быть администратором на сервере, на котором расположено хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c04c4-127">The user who will be adding the certificate must be an administrator on the server where the certificate store is located.</span></span>

    -   <span data-ttu-id="c04c4-128">Служба сервера должна быть запущена.</span><span class="sxs-lookup"><span data-stu-id="c04c4-128">The server service must be started.</span></span>

    -   <span data-ttu-id="c04c4-129">Порт 139 на сервере управления должен быть открыт для веб-службы server'sIP.</span><span class="sxs-lookup"><span data-stu-id="c04c4-129">Port 139 on the Management Server must be open to the Web Service server’sIP.</span></span>

-   <span data-ttu-id="c04c4-130">Используйте списки управления доступом (ACL), чтобы убедиться в том, что пакеты приложения и все файлы пакета защищены и не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="c04c4-130">Use access control lists (ACLs) to ensure that the application packages and all package files are protected and cannot be tampered.</span></span> <span data-ttu-id="c04c4-131">Списки ACL ограничивают доступ к расположению или папке, в которых хранятся пакеты, разрешая доступ только к определенным учетным записям.</span><span class="sxs-lookup"><span data-stu-id="c04c4-131">ACLs restrict access to the location or folder where you store the packages, allowing access only to certain accounts.</span></span>

-   <span data-ttu-id="c04c4-132">Убедитесь, что канал между сервером управления виртуализацией приложений и базой данных защищен (например, с помощью IPsec).</span><span class="sxs-lookup"><span data-stu-id="c04c4-132">Make sure that the channel between the Application Virtualization Management Server and the database is secured—for example, by using IPsec.</span></span>

-   <span data-ttu-id="c04c4-133">Если пакеты хранятся в сети хранения данных или NAS, убедитесь в том, что соединение между центральным устройством хранения и серверами Application Virtualization защищается.</span><span class="sxs-lookup"><span data-stu-id="c04c4-133">If packages are stored on a SAN or NAS, ensure the connection between the central storage device and the Application Virtualization Servers is protected.</span></span>

-   <span data-ttu-id="c04c4-134">Все коммуникационные каналы для клиента должны быть защищены (включая соединения с сервером публикаций, сервером Application Virtualization Server и путем к файлам OSD и ICO), используя протокол, например HTTPS или IPsec.</span><span class="sxs-lookup"><span data-stu-id="c04c4-134">All communication channels to the client should be protected—including connections to the publishing server, the Application Virtualization Server, and the path to the OSD and ICO files—by using a protocol such as HTTPS or IPsec.</span></span> 

-   <span data-ttu-id="c04c4-135">Разрешения клиентов следует настроить так, чтобы обеспечить возможность несанкционированного подделки пакетов.</span><span class="sxs-lookup"><span data-stu-id="c04c4-135">Client permissions should be configured to help ensure that packages cannot be tampered with by users.</span></span> <span data-ttu-id="c04c4-136">Особенно важно, чтобы вы не предоставили пользователям разрешение на добавление или обновление пакетов в системах, например серверах узла сеансов удаленных рабочих столов (узлов RDSession), которые являются общими для нескольких пользователей.</span><span class="sxs-lookup"><span data-stu-id="c04c4-136">It is especially important that you do not grant users permission to add or update packages on systems, such as Remote Desktop Session Host (RDSession Host) servers, that are shared with multiple users.</span></span>

-   <span data-ttu-id="c04c4-137">Проверка подлинности Kerberos должна быть разрешена в среде домена или леса, чтобы консоль управления сервером работала правильно.</span><span class="sxs-lookup"><span data-stu-id="c04c4-137">Kerberos authentication must be permitted across domain or forest environments for the Server Management Console to work correctly.</span></span>

-   <span data-ttu-id="c04c4-138">Этот выпуск программного обеспечения не поддерживает размещение сервера RTSP на основе Kerberos и сервера IIS с учетной записью Майкрософт только для NTLM на одном и том же компьютере.</span><span class="sxs-lookup"><span data-stu-id="c04c4-138">This release of the software does not support hosting a Kerberos-based RTSP server and a Microsoft NTLM-only-based IIS server on the same computer.</span></span> <span data-ttu-id="c04c4-139">Для размещения сервера RTSP и сервера IIS на том же компьютере удалите имя участника-службы с сервера IIS и используйте проверку подлинности NTLM.</span><span class="sxs-lookup"><span data-stu-id="c04c4-139">To host an RTSP server and an IIS server on the same computer, remove the SPN from the IIS server and use NTLM authentication.</span></span>

## <span data-ttu-id="c04c4-140">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c04c4-140">Related topics</span></span>


[<span data-ttu-id="c04c4-141">Планирование развертывания системы виртуализации приложений</span><span class="sxs-lookup"><span data-stu-id="c04c4-141">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





