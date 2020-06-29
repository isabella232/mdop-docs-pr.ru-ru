---
title: Устранение проблем с разрешениями сертификатов
description: Устранение проблем с разрешениями сертификатов
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815209"
---
# <span data-ttu-id="2da96-103">Устранение проблем с разрешениями сертификатов</span><span class="sxs-lookup"><span data-stu-id="2da96-103">Troubleshooting Certificate Permission Issues</span></span>


<span data-ttu-id="2da96-104">После установки приложения App-V 4.5 в том случае, если в качестве закрытого ключа не указана соответствующая таблица ACL для сетевой службы, событие заносится в журнал событий NT и в файл помещается запись `Sft-server.log` .</span><span class="sxs-lookup"><span data-stu-id="2da96-104">After the installation of App-V4.5, if the private key has not been configured with the proper ACL for the Network Service, an event is logged in the NT Event Log and an entry is placed in the `Sft-server.log` file.</span></span>

## <span data-ttu-id="2da96-105">Сообщения об ошибках</span><span class="sxs-lookup"><span data-stu-id="2da96-105">Error Messages</span></span>


### <span data-ttu-id="2da96-106">Windows server2003</span><span class="sxs-lookup"><span data-stu-id="2da96-106">Windows Server2003</span></span>

<span data-ttu-id="2da96-107">Event ID 36870 — произошла неустранимая ошибка при попытке доступа к закрытому ключу учетных данных SSL-сервера.</span><span class="sxs-lookup"><span data-stu-id="2da96-107">Event ID 36870—A fatal error occurred when attempting to access the SSL server credential private key.</span></span> <span data-ttu-id="2da96-108">Код ошибки, возвращенный из криптографического модуля, — 0x80090016.</span><span class="sxs-lookup"><span data-stu-id="2da96-108">The error code returned from the cryptographic module is 0x80090016.</span></span>

### <span data-ttu-id="2da96-109">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="2da96-109">Windows Server2008</span></span>

<span data-ttu-id="2da96-110">Event ID 36870 — произошла неустранимая ошибка при попытке доступа к закрытому ключу учетных данных SSL-сервера.</span><span class="sxs-lookup"><span data-stu-id="2da96-110">Event ID 36870—A fatal error occurred when attempting to access the SSL server credential private key.</span></span> <span data-ttu-id="2da96-111">Код ошибки, возвращенный из криптографического модуля, — 0x8009030d.</span><span class="sxs-lookup"><span data-stu-id="2da96-111">The error code returned from the cryptographic module is 0x8009030d.</span></span>

## <span data-ttu-id="2da96-112">SFT-Server. log</span><span class="sxs-lookup"><span data-stu-id="2da96-112">Sft-server.log</span></span>


<span data-ttu-id="2da96-113">В `sft-server.log` файле, расположенном в каталоге, помещается следующее сообщение об ошибке `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` :</span><span class="sxs-lookup"><span data-stu-id="2da96-113">The following error is placed in the `sft-server.log` file located in the `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` directory:</span></span>

<span data-ttu-id="2da96-114">Не удалось загрузить сертификат.</span><span class="sxs-lookup"><span data-stu-id="2da96-114">Certificate could not be loaded.</span></span> <span data-ttu-id="2da96-115">Код ошибки \ [-2146893043 \].</span><span class="sxs-lookup"><span data-stu-id="2da96-115">Error code \[-2146893043\].</span></span> <span data-ttu-id="2da96-116">Убедитесь в том, что учетная запись Network Service имеет надлежащий доступ к сертификату и соответствующему файлу закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="2da96-116">Make sure that the Network Service account has proper access to the certificate and its corresponding private key file.</span></span>

 

 





