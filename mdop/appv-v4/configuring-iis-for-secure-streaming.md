---
title: Настройка IIS для защиты потоковой передачи
description: Настройка IIS для защиты потоковой передачи
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821882"
---
# <span data-ttu-id="9d96f-103">Настройка IIS для защиты потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="9d96f-103">Configuring IIS for Secure Streaming</span></span>


<span data-ttu-id="9d96f-104">С выпуском Microsoft Application Virtualization (App-V) версии 4,5 можно использовать протоколы HTTP и HTTPS для потоковой передачи пакетов приложений клиентам App-V.</span><span class="sxs-lookup"><span data-stu-id="9d96f-104">With the release of Microsoft Application Virtualization (App-V) version 4.5, you can use HTTP and HTTPS as protocols for streaming application packages to the App-V clients.</span></span> <span data-ttu-id="9d96f-105">Этот параметр позволяет организациям использовать дополнительную масштабируемость, предоставляемую IIS, обычно.</span><span class="sxs-lookup"><span data-stu-id="9d96f-105">This option enables organizations to leverage the additional scalability that IIS typically offers.</span></span> <span data-ttu-id="9d96f-106">Если вы используете IIS как потоковый сервер, вы можете защитить связь между клиентом и сервером с помощью HTTPS вместо HTTP.</span><span class="sxs-lookup"><span data-stu-id="9d96f-106">When you use IIS as a streaming server, you can help secure the communications between the client and server by using HTTPS instead of HTTP.</span></span>

<span data-ttu-id="9d96f-107">**Примечание**  Если вы хотите передавать приложения с файлового сервера, необходимо повысить безопасность обмена данными с пакетами приложений.</span><span class="sxs-lookup"><span data-stu-id="9d96f-107">**Note** If you want to stream applications from a file server, you should enhance the security of the communications to the application packages.</span></span> <span data-ttu-id="9d96f-108">Это может быть достигнуто с помощью IPsec.</span><span class="sxs-lookup"><span data-stu-id="9d96f-108">This can be achieved using IPsec.</span></span> <span data-ttu-id="9d96f-109">Дополнительные сведения содержатся в указанных ниже разделах библиотеки TechNet.</span><span class="sxs-lookup"><span data-stu-id="9d96f-109">For more information see the following topics in the TechNet Library:</span></span>

-   <span data-ttu-id="9d96f-110">Для Windows server2003</span><span class="sxs-lookup"><span data-stu-id="9d96f-110">For Windows Server2003,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133226>

-   <span data-ttu-id="9d96f-111">Для Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d96f-111">For Windows Server 2008,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## <span data-ttu-id="9d96f-112">Типы MIME</span><span class="sxs-lookup"><span data-stu-id="9d96f-112">MIME Types</span></span>


<span data-ttu-id="9d96f-113">При использовании IIS для потоковой передачи виртуальных приложений с использованием HTTP или HTTPS для поддержки App-V на сервере IIS должны быть добавлены следующие типы MIME:</span><span class="sxs-lookup"><span data-stu-id="9d96f-113">When you use IIS to stream virtual applications with HTTP or HTTPS, to support App-V, the following MIME types must be added to the IIS server:</span></span>

-   <span data-ttu-id="9d96f-114">. OSD = TXT</span><span class="sxs-lookup"><span data-stu-id="9d96f-114">.OSD=TXT</span></span>

-   <span data-ttu-id="9d96f-115">. SFT = binary</span><span class="sxs-lookup"><span data-stu-id="9d96f-115">.SFT=Binary</span></span>

<span data-ttu-id="9d96f-116">Ниже указаны статьи базы знаний, в которых приведены рекомендации по добавлению типов MIME.</span><span class="sxs-lookup"><span data-stu-id="9d96f-116">Use the following KB articles as guidance for adding MIME types:</span></span>

<span data-ttu-id="9d96f-117">IIS 6,0:</span><span class="sxs-lookup"><span data-stu-id="9d96f-117">IIS 6.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151973>

<span data-ttu-id="9d96f-118">IIS 7,0:</span><span class="sxs-lookup"><span data-stu-id="9d96f-118">IIS 7.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151977>

## <span data-ttu-id="9d96f-119">Проверка подлинности Kerberos</span><span class="sxs-lookup"><span data-stu-id="9d96f-119">Kerberos Authentication</span></span>


<span data-ttu-id="9d96f-120">При использовании проверки подлинности HTTP или HTTPS и Kerberos для потоковой передачи файлов ICO, OSD и SFT вы повышаете безопасность среды.</span><span class="sxs-lookup"><span data-stu-id="9d96f-120">When you use HTTP or HTTPS and Kerberos authentication to stream ICO, OSD, or SFT files, you are enhancing the security of your environment.</span></span> <span data-ttu-id="9d96f-121">Тем не менее, чтобы службы IIS поддерживали проверку подлинности Kerberos, необходимо настроить соответствующее имя субъекта-службы (SPN).</span><span class="sxs-lookup"><span data-stu-id="9d96f-121">However, for IIS to support Kerberos authentication, you must configure a proper Service Principal Name (SPN).</span></span> <span data-ttu-id="9d96f-122">Это `setspn.exe` средство доступно для Windows server2003 из средств поддержки на установочном компакт-диске и встроено в Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="9d96f-122">The `setspn.exe` tool is available for Windows Server2003 from the Support Tools on the installation CD and is built-in to Windows Server2008.</span></span>

<span data-ttu-id="9d96f-123">Чтобы создать SPN, запустите `setspn.exe` из командной строки, войдя в учетную запись администратора домена (например, `setspn.exe –A HTTP/FQDN of Server ServerName` .</span><span class="sxs-lookup"><span data-stu-id="9d96f-123">To create an SPN, run `setspn.exe` from a command prompt while logged in as a member of Domain Administrators—for example, `setspn.exe –A HTTP/FQDN of Server ServerName`.</span></span>

## <span data-ttu-id="9d96f-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9d96f-124">Related topics</span></span>


[<span data-ttu-id="9d96f-125">Настройка сервера управления или сервера потоковой передачи для обеспечения защиты подключений после установки</span><span class="sxs-lookup"><span data-stu-id="9d96f-125">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





