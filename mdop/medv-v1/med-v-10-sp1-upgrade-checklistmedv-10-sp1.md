---
title: Контрольный список обновления MED-V 1.0 с пакетом обновления 1 (SP1)
description: Контрольный список обновления MED-V 1.0 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827269"
---
# <span data-ttu-id="c9b2b-103">Контрольный список обновления MED-V 1.0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="c9b2b-103">MED-V 1.0 SP1 Upgrade Checklist</span></span>


<span data-ttu-id="c9b2b-104">Чтобы обновить версию Microsoft Enterprise Virtualization (MED-V) 1.0 до MED-V 1.0 Service Pack1 (SP1), необходимо обновить клиент.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-104">To upgrade Microsoft Enterprise Desktop Virtualization (MED-V)1.0 to MED-V1.0 Service Pack1 (SP1), the client must be upgraded.</span></span> <span data-ttu-id="c9b2b-105">При необходимости можно обновить сервер.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-105">The server can optionally be upgraded.</span></span>

## <span data-ttu-id="c9b2b-106">Обновление сервера</span><span class="sxs-lookup"><span data-stu-id="c9b2b-106">Server Upgrade</span></span>


**<span data-ttu-id="c9b2b-107">Обновление сервера MED-V 1.0 до версии MED-V 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="c9b2b-107">To upgrade the MED-V1.0 server to MED-V1.0 SP1</span></span>**

1.  <span data-ttu-id="c9b2b-108">Создавайте резервные копии следующих файлов, расположенных в каталоге \* &lt; installDir &gt; /Servers/ConfigurationServer\* :</span><span class="sxs-lookup"><span data-stu-id="c9b2b-108">Back up the following files that are located in the *&lt;InstallDir&gt; / Servers / ConfigurationServer* directory:</span></span>

    -   <span data-ttu-id="c9b2b-109">OrganizationalPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="c9b2b-109">OrganizationalPolicy.XML</span></span>

    -   <span data-ttu-id="c9b2b-110">ClientPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="c9b2b-110">ClientPolicy.XML</span></span>

    -   <span data-ttu-id="c9b2b-111">WorkspaceKeys.XML</span><span class="sxs-lookup"><span data-stu-id="c9b2b-111">WorkspaceKeys.XML</span></span>

2.  <span data-ttu-id="c9b2b-112">Создавайте резервные копии файлов \* &lt; installDir &gt; /servers/ServerSettings.xml\* .</span><span class="sxs-lookup"><span data-stu-id="c9b2b-112">Back up the *&lt;InstallDir&gt; / Servers / ServerSettings.xml* file.</span></span>

3.  <span data-ttu-id="c9b2b-113">Удалите сервер MED-V 1.0.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-113">Uninstall the MED-V1.0 server.</span></span>

4.  <span data-ttu-id="c9b2b-114">Установите сервер MED-V 1.0 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c9b2b-114">Install the MED-V1.0 SP1 server.</span></span>

5.  <span data-ttu-id="c9b2b-115">Восстановите резервные копии файлов в соответствующих каталогах.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-115">Restore the backup files to the appropriate directories.</span></span>

6.  <span data-ttu-id="c9b2b-116">Перезапустите службу сервера MED-V.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-116">Restart the MED-V server service.</span></span>

<span data-ttu-id="c9b2b-117">**Примечание**  Если конфигурация сервера была изменена по умолчанию, файлы могут храниться в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-117">**Note** If the server configuration has been changed from the default, the files might be stored in a different location.</span></span>

 

## <span data-ttu-id="c9b2b-118">Обновление клиента</span><span class="sxs-lookup"><span data-stu-id="c9b2b-118">Client Upgrade</span></span>


<span data-ttu-id="c9b2b-119">Чтобы обновить клиент MED-V 1.0 до версии MED-v 1.0 с пакетом обновления 1 (SP1), установите файл MSP в клиенте MED-V 1.0.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-119">To upgrade the MED-V1.0 client to MED-V1.0 SP1, install the .msp file on a MED-V1.0 client.</span></span> <span data-ttu-id="c9b2b-120">Клиент и MED-V обновляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-120">The client and MED-V are automatically upgraded.</span></span>

 

 





