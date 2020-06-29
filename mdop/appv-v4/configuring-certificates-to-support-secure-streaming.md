---
title: Настройка сертификатов для обеспечения поддержки безопасной потоковой передачи
description: Настройка сертификатов для обеспечения поддержки безопасной потоковой передачи
author: dansimp
ms.assetid: 88dc76d8-7745-4729-92a1-af089c921244
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9376634a1b9843f46dba4cd452e672cc9e535226
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821892"
---
# <span data-ttu-id="81736-103">Настройка сертификатов для обеспечения поддержки безопасной потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="81736-103">Configuring Certificates to Support Secure Streaming</span></span>


<span data-ttu-id="81736-104">По умолчанию служба App-V запускается под учетной записью Network Service.</span><span class="sxs-lookup"><span data-stu-id="81736-104">By default, the App-V service runs under the Network Service account.</span></span> <span data-ttu-id="81736-105">Тем не менее, вы можете создать учетную запись службы в доменных службах Active Directory и заменить ее учетную запись сетевой службы учетной записью домена Active Directory.</span><span class="sxs-lookup"><span data-stu-id="81736-105">However, you can create a service account in Active Directory Domain Services and replace the Network Service account with the Active Directory Domain account.</span></span>

<span data-ttu-id="81736-106">Контекст безопасности, под которым запускается служба, важен для настройки расширенной безопасной связи.</span><span class="sxs-lookup"><span data-stu-id="81736-106">The security context under which the service runs is important for configuring enhanced secure communications.</span></span> <span data-ttu-id="81736-107">Этот контекст безопасности должен иметь разрешения на чтение закрытого ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="81736-107">This security context must have read permissions for the certificate private key.</span></span> <span data-ttu-id="81736-108">Когда для сервера App-V генерируется *запрос на подписывание сертификата* PKCS \ #10 (CSR), вызывается *поставщик служб шифрования* Windows и создается закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="81736-108">When a PKCS\#10 *Certificate Signing Request* (CSR) is generated for the App-V server, the Windows *Cryptographic Service Provider* is called and a private key is generated.</span></span> <span data-ttu-id="81736-109">Закрытый ключ защищен с помощью разрешений, предоставленных только учетным записям System и Administrator.</span><span class="sxs-lookup"><span data-stu-id="81736-109">The private key is secured with permissions given to the System and Administrator accounts only.</span></span>

<span data-ttu-id="81736-110">Необходимо изменить списки управления доступом (ACL) для закрытого ключа, чтобы предоставить серверу управления App-V или потоковой передачи доступ к закрытому ключу, требуемому для успешной безопасной передачи данных TLS.</span><span class="sxs-lookup"><span data-stu-id="81736-110">You must modify the access control lists (ACLs) on the private key to let the App-V Management or Streaming Server access the private key required for successful TLS secured communication.</span></span>

## <span data-ttu-id="81736-111">Получение и установка сертификата</span><span class="sxs-lookup"><span data-stu-id="81736-111">Obtaining and Installing a Certificate</span></span>


<span data-ttu-id="81736-112">Ниже приведены сценарии для получения и установки сертификата для App-V.</span><span class="sxs-lookup"><span data-stu-id="81736-112">The scenarios for obtaining and installing a certificate for App-V are as follows:</span></span>

-   <span data-ttu-id="81736-113">Внутренняя инфраструктура открытых ключей (PKI).</span><span class="sxs-lookup"><span data-stu-id="81736-113">Internal public key infrastructure (PKI).</span></span>

-   <span data-ttu-id="81736-114">Центр сертификации (ЦС), выдавший сертификат стороннего поставщика.</span><span class="sxs-lookup"><span data-stu-id="81736-114">Third-party certificate issuing certification authority (CA).</span></span>

    <span data-ttu-id="81736-115">**Примечание**  Если вам нужно получить сертификат из стороннего центра сертификации, воспользуйтесь документацией, доступной на веб-сайте этого ЦС.</span><span class="sxs-lookup"><span data-stu-id="81736-115">**Note** If you need to obtain a certificate from a third-party CA, follow the documentation available on that CA’s Web site.</span></span>

     

<span data-ttu-id="81736-116">Если инфраструктура PKI была развернута, обратитесь к администратору инфраструктуры PKI для получения сертификата, который соответствует требованиям, описанным в этой статье.</span><span class="sxs-lookup"><span data-stu-id="81736-116">If a PKI infrastructure has been deployed, consult with the PKI administrators to acquire a certificate that complies with the requirements described in this topic.</span></span> <span data-ttu-id="81736-117">Если инфраструктура PKI недоступна, вы можете получить действительный сертификат с помощью стороннего ЦС.</span><span class="sxs-lookup"><span data-stu-id="81736-117">If a PKI infrastructure is not available, use a third-party CA to obtain a valid certificate.</span></span>

<span data-ttu-id="81736-118">Пошаговые инструкции по получению и установке сертификата вы найдете в статье <https://go.microsoft.com/fwlink/?LinkId=151969> .</span><span class="sxs-lookup"><span data-stu-id="81736-118">For step-by-step guidance for obtaining and installing a certificate, see <https://go.microsoft.com/fwlink/?LinkId=151969>.</span></span>

## <span data-ttu-id="81736-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="81736-119">Related topics</span></span>


<span data-ttu-id="81736-120">Настройка сертификатов для обеспечения поддержки защищенной потоковой передачи [разрешения на изменение закрытого ключа для поддержки сервера управления или потокового сервера](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)</span><span class="sxs-lookup"><span data-stu-id="81736-120">Configuring Certificates to Support Secure Streaming [How to Modify Private Key Permissions to Support Management Server or Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)</span></span>

 

 





