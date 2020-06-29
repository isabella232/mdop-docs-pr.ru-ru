---
title: Изменение разрешений закрытых ключей для обеспечения поддержки сервера управления или сервера потоковой передачи
description: Изменение разрешений закрытых ключей для обеспечения поддержки сервера управления или сервера потоковой передачи
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817029"
---
# <span data-ttu-id="b8d7e-103">Изменение разрешений закрытых ключей для обеспечения поддержки сервера управления или сервера потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="b8d7e-103">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>


<span data-ttu-id="b8d7e-104">Для поддержки более надежной установки App-V вы можете изменить закрытые ключи в Windows server2003 или Windows Server2008 с помощью описанных ниже процедур.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-104">To support a more secure App-V installation, you can use the following procedures to modify private keys in either Windows Server2003 or Windows Server2008.</span></span> <span data-ttu-id="b8d7e-105">Чтобы изменить разрешения закрытого ключа, можно использовать средство Windows server2003 Resource Kit `WinHttpCertCfg.exe` .</span><span class="sxs-lookup"><span data-stu-id="b8d7e-105">To modify the permissions of the private key, you can use the Windows Server2003 Resource Kit tool `WinHttpCertCfg.exe`.</span></span>

<span data-ttu-id="b8d7e-106">Для Windows server2003 процедура требует, чтобы сертификат, соответствующий предварительным требованиям, перечисленным в этом документе, был установлен на компьютере или компьютерах, на которых будет устанавливаться управление App-V или потоковый сервер.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-106">For Windows Server2003, the procedure requires that a certificate that meets the prerequisites listed in this document is installed on the computer or computers on which you will install the App-V Management or Streaming Server.</span></span> <span data-ttu-id="b8d7e-107">Дополнительные сведения об использовании этого `WinHttpCertCfg.exe` средства можно найти на странице <https://go.microsoft.com/fwlink/?LinkId=151981> .</span><span class="sxs-lookup"><span data-stu-id="b8d7e-107">Additional information about using the `WinHttpCertCfg.exe` tool is available at <https://go.microsoft.com/fwlink/?LinkId=151981>.</span></span>

<span data-ttu-id="b8d7e-108">В Windows Server2008 процесс изменения ACL для закрытого ключа значительно упрощен.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-108">In Windows Server2008, the process of changing the ACLs on the private key is much simpler.</span></span> <span data-ttu-id="b8d7e-109">Пользовательский интерфейс сертификата можно использовать для управления разрешениями закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-109">The certificate’s user interface can be used to manage private key permissions.</span></span>

<span data-ttu-id="b8d7e-110">**Примечание**  Контекст безопасности по умолчанию — сетевая служба; Однако вместо этого можно использовать учетную запись домена.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-110">**Note** The default security context is Network Service; however, a domain account can be used instead.</span></span>

 

**<span data-ttu-id="b8d7e-111">Управление закрытыми ключами в Windows server2003</span><span class="sxs-lookup"><span data-stu-id="b8d7e-111">To manage private keys in Windows Server2003</span></span>**

1.  <span data-ttu-id="b8d7e-112">На компьютере, который станет сервером управления App-V или потоком потоков, введите в командной строке следующую команду, чтобы получить список текущих разрешений, назначенных определенному сертификату.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-112">On the computer that will become the App-V Management or Streaming Server, type the following command in a command prompt to list the current permissions assigned to a specific certificate:</span></span>

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  <span data-ttu-id="b8d7e-113">При необходимости измените разрешения сертификата, чтобы предоставить доступ на чтение к контексту безопасности, который будет использоваться для управления или службы потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-113">If necessary, modify the permissions of the certificate to provide read access to the security context that will be used for Management or Streaming Service:</span></span>

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  <span data-ttu-id="b8d7e-114">Убедитесь в том, что контекст безопасности был добавлен надлежащим образом, указывая разрешения на сертификат.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-114">Verify that the security context was properly added by listing the permissions on the certificate:</span></span>

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**<span data-ttu-id="b8d7e-115">Управление закрытыми ключами в Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="b8d7e-115">To manage private keys in Windows Server2008</span></span>**

1.  <span data-ttu-id="b8d7e-116">Создание консоли управления (MMC) с помощью оснастки " *Сертификаты* ", которая указывает на хранилище сертификатов *локального компьютера* .</span><span class="sxs-lookup"><span data-stu-id="b8d7e-116">Create a Microsoft Management Console (MMC) with the *Certificates* snap-in that targets the *Local Machine* certificate store.</span></span>

2.  <span data-ttu-id="b8d7e-117">Разверните MMC и выберите **Управление закрытыми ключами**.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-117">Expand the MMC and select **Manage Private Keys**.</span></span>

3.  <span data-ttu-id="b8d7e-118">На вкладке **Безопасность** добавьте учетную запись **сетевой службы** с правом на **Чтение** .</span><span class="sxs-lookup"><span data-stu-id="b8d7e-118">On the **Security** tab, add the **Network Service** account with **Read** access.</span></span>

## <span data-ttu-id="b8d7e-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b8d7e-119">Related topics</span></span>


[<span data-ttu-id="b8d7e-120">Настройка сертификатов для обеспечения поддержки сервера управления App-V или сервера потоковой передачи Streaming Server</span><span class="sxs-lookup"><span data-stu-id="b8d7e-120">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[<span data-ttu-id="b8d7e-121">Настройка сертификатов для обеспечения поддержки безопасной потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="b8d7e-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

 

 





