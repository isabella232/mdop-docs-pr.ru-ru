---
title: Публикация виртуального приложения на клиенте
description: Публикация виртуального приложения на клиенте
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816872"
---
# <span data-ttu-id="67479-103">Публикация виртуального приложения на клиенте</span><span class="sxs-lookup"><span data-stu-id="67479-103">How to Publish a Virtual Application on the Client</span></span>


<span data-ttu-id="67479-104">При развертывании виртуализации приложений с помощью электронной системы распространения программного обеспечения можно использовать одну из описанных ниже процедур для публикации пакета приложения для пользователей.</span><span class="sxs-lookup"><span data-stu-id="67479-104">When you deploy Application Virtualization by using an electronic software distribution system, you can use one of the following procedures to publish an application package to your users.</span></span>

**<span data-ttu-id="67479-105">Публикация пакета в отдельном файле установщика Windows</span><span class="sxs-lookup"><span data-stu-id="67479-105">To publish a package using a stand-alone Windows Installer file</span></span>**

1.  <span data-ttu-id="67479-106">Клиент должен быть установлен с параметром *REQUIREAUTHORIZATIONIFCACHED* , равным 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="67479-106">The client should be installed with the *REQUIREAUTHORIZATIONIFCACHED* parameter set to 0 (zero).</span></span> <span data-ttu-id="67479-107">Дополнительные сведения об установке этого параметра можно найти в разделе [Параметры командной строки установщика клиента Application Virtualization](application-virtualization-client-installer-command-line-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="67479-107">For more information about setting this parameter, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md)</span></span>

2.  <span data-ttu-id="67479-108">Скопируйте файл установщика Windows и SFT – файл в ту же папку на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="67479-108">Copy the Windows Installer file and the SFT file to same folder on the target computer.</span></span>

3.  <span data-ttu-id="67479-109">На компьютере выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="67479-109">Run the following command on the computer:</span></span>

    `Msiexec.exe /I "packagename.msi" /q`

**<span data-ttu-id="67479-110">Публикация пакета с помощью установщика Windows и манифеста пакета</span><span class="sxs-lookup"><span data-stu-id="67479-110">To publish a package using Windows Installer and the package manifest</span></span>**

1.  <span data-ttu-id="67479-111">Скопируйте файл установщика Windows на целевой компьютер и SFT — в общую папку содержимого на потоковый сервер.</span><span class="sxs-lookup"><span data-stu-id="67479-111">Copy the Windows Installer file to the target computer and the SFT file to the CONTENT share on the streaming server.</span></span>

2.  <span data-ttu-id="67479-112">На каждом компьютере пользователя выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="67479-112">Run the following command on each user’s computer:</span></span>

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    <span data-ttu-id="67479-113">**Важно!**  Для OVERRIDEURL все символы обратной косой черты должны быть escape-символами с помощью предшествующей обратной косой черты или путь OVERRIDEURL не будет анализироваться должным образом.</span><span class="sxs-lookup"><span data-stu-id="67479-113">**Important** For OVERRIDEURL all backslash characters must be escaped using a preceding backslash, or the OVERRIDEURL path will not be parsed correctly.</span></span> <span data-ttu-id="67479-114">Кроме того, свойства и значения должны быть введены прописными буквами, за исключением случаев, когда значение является путем к файлу.</span><span class="sxs-lookup"><span data-stu-id="67479-114">Also, properties and values must be entered as uppercase except where the value is a path to a file.</span></span>

     

**<span data-ttu-id="67479-115">Публикация пакета с помощью SFTMIME</span><span class="sxs-lookup"><span data-stu-id="67479-115">To publish a package using SFTMIME</span></span>**

-   <span data-ttu-id="67479-116">Например, чтобы опубликовать приложение для всех пользователей на компьютере, выполните на компьютере пользователя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="67479-116">For an example of how to publish an application for all users on a computer, run the following command on the user’s computer:</span></span>

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    <span data-ttu-id="67479-117">Дополнительные сведения об этих и других командах SFTMIME можно найти в разделе [Справочник по командам SFTMIME](sftmime--command-reference.md).</span><span class="sxs-lookup"><span data-stu-id="67479-117">For additional details about these and other SFTMIME commands, see [SFTMIME Command Reference](sftmime--command-reference.md).</span></span>

## <span data-ttu-id="67479-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="67479-118">Related topics</span></span>


[<span data-ttu-id="67479-119">Определение способа публикации</span><span class="sxs-lookup"><span data-stu-id="67479-119">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="67479-120">Сценарий на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="67479-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="67479-121">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="67479-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

[<span data-ttu-id="67479-122">Сценарий изолированной доставки для клиентов Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="67479-122">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





