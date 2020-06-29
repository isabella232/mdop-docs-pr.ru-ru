---
title: Настройка администрирования App-V для распределенной среды
description: Настройка администрирования App-V для распределенной среды
author: dansimp
ms.assetid: 53971fa9-8319-435c-be74-c37feb9af1da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c1a638d6afde9270859c8aa98fc9f421c39cfc72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821912"
---
# <span data-ttu-id="bf68b-103">Настройка администрирования App-V для распределенной среды</span><span class="sxs-lookup"><span data-stu-id="bf68b-103">Configuring App-V Administration for a Distributed Environment</span></span>


<span data-ttu-id="bf68b-104">При проектировании инфраструктуры для конкретной организации вы можете установить веб-службу управления App-V на компьютере, отличном от компьютера, на котором установлен сервер управления App-V.</span><span class="sxs-lookup"><span data-stu-id="bf68b-104">When designing the infrastructure for your specific organization, you can install the App-V Management Web Service on a computer other than the computer where you install the App-V Management Server.</span></span> <span data-ttu-id="bf68b-105">Ниже приведены распространенные причины разделения этих компонентов App-V.</span><span class="sxs-lookup"><span data-stu-id="bf68b-105">Common reasons for separating these App-V components include the following:</span></span>

-   <span data-ttu-id="bf68b-106">Производительность</span><span class="sxs-lookup"><span data-stu-id="bf68b-106">Performance</span></span>

-   <span data-ttu-id="bf68b-107">Надежность</span><span class="sxs-lookup"><span data-stu-id="bf68b-107">Reliability</span></span>

-   <span data-ttu-id="bf68b-108">Доступность</span><span class="sxs-lookup"><span data-stu-id="bf68b-108">Availability</span></span>

-   <span data-ttu-id="bf68b-109">Масштабируемость</span><span class="sxs-lookup"><span data-stu-id="bf68b-109">Scalability</span></span>

<span data-ttu-id="bf68b-110">Для разделения сервера управления и веб-службы управления необходимо дополнительно настроить конфигурацию для правильной работы инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="bf68b-110">Separating the Management Server and Management Web Service requires additional configuration for the infrastructure to operate correctly.</span></span> <span data-ttu-id="bf68b-111">Если вы разделяете эти две функции, но не выполняете процедуры, описанные в этой статье, консоль управления будет подключаться к веб-службе управления, но не сможет правильно пройти проверку подлинности с помощью хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="bf68b-111">When you separate these two features but do not complete the procedures described in this topic, the Management Console will connect to the Management Web Service but will not be able to properly authenticate with the data store.</span></span> <span data-ttu-id="bf68b-112">Консоль управления не будет загружаться должным образом, и администратор не сможет выполнить какие – либо задачи администрирования.</span><span class="sxs-lookup"><span data-stu-id="bf68b-112">The Management Console will not load properly, and the administrator will not be able to complete any administrative tasks.</span></span>

<span data-ttu-id="bf68b-113">Это происходит потому, что веб-служба управления не может использовать для доступа к хранилищу данных учетные данные, переданные из консоли управления.</span><span class="sxs-lookup"><span data-stu-id="bf68b-113">This behavior occurs because the Management Web Service cannot use the credentials, passed to it from the Management Console, to access the data store.</span></span> <span data-ttu-id="bf68b-114">Решение состоит в том, чтобы настроить сервер веб-службы управления как доверенный для делегирования.</span><span class="sxs-lookup"><span data-stu-id="bf68b-114">The solution is to configure the Management Web Service server to be “Trusted for delegation.”</span></span>

## <span data-ttu-id="bf68b-115">Настройка доменных служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="bf68b-115">Configuring Active Directory Domain Services</span></span>


<span data-ttu-id="bf68b-116">Кроме того, необходимо правильно настроить доменные службы Active Directory для работы в распределенной среде.</span><span class="sxs-lookup"><span data-stu-id="bf68b-116">It is also necessary to configure Active Directory Domain Services properly to work in a distributed environment.</span></span> <span data-ttu-id="bf68b-117">Этот раздел содержит сведения, необходимые для настройки доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bf68b-117">This section includes the information you need configure Active Directory Domain Services.</span></span>

### <span data-ttu-id="bf68b-118">Если служба SQL использует локальную системную учетную запись</span><span class="sxs-lookup"><span data-stu-id="bf68b-118">When SQL Service Uses Local System account</span></span>

<span data-ttu-id="bf68b-119">Чтобы настроить среду, в которой служба SQL использует локальную системную учетную запись, измените свойства учетной записи компьютера для веб-службы управления, чтобы она была доверенной для делегирования.</span><span class="sxs-lookup"><span data-stu-id="bf68b-119">To set up the environment where the SQL Service uses the local system account, change the properties of the machine account of the Management Web Service to be trusted for delegation.</span></span> <span data-ttu-id="bf68b-120">Подробные сведения о том, как это сделать, описаны [в разделе Настройка доверенности сервера для делегирования](how-to-configure-the-server-to-be-trusted-for-delegation.md)</span><span class="sxs-lookup"><span data-stu-id="bf68b-120">For detailed procedures about how to do this, see [How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)</span></span>

### <span data-ttu-id="bf68b-121">При использовании службой SQL учетной записи на основе домена</span><span class="sxs-lookup"><span data-stu-id="bf68b-121">When SQL Service Uses Domain-Based Account</span></span>

<span data-ttu-id="bf68b-122">Чтобы настроить среду, в которой SQL Server использует учетные записи доменных служб, необходимо решить, применяются ли к ним различные условия, в том числе указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="bf68b-122">To set up the environment where SQL Servers use domain-based service accounts, you need to consider whether or not a variety of factors apply, including the following:</span></span>

-   <span data-ttu-id="bf68b-123">Кластеризация SQL Server</span><span class="sxs-lookup"><span data-stu-id="bf68b-123">Clustering of SQL Server</span></span>

-   <span data-ttu-id="bf68b-124">Репликация</span><span class="sxs-lookup"><span data-stu-id="bf68b-124">Replication</span></span>

-   <span data-ttu-id="bf68b-125">Автоматические задачи</span><span class="sxs-lookup"><span data-stu-id="bf68b-125">Automated tasks</span></span>

-   <span data-ttu-id="bf68b-126">Связанные серверы</span><span class="sxs-lookup"><span data-stu-id="bf68b-126">Linked servers</span></span>

<span data-ttu-id="bf68b-127">Сведения о настройке доменных служб Active Directory при использовании службы SQL для учетной записи на основе домена приведены в разделе <https://go.microsoft.com/fwlink/?LinkId=151968> .</span><span class="sxs-lookup"><span data-stu-id="bf68b-127">For information about configuring Active Directory Domain Services when the SQL service uses a domain-based account, see <https://go.microsoft.com/fwlink/?LinkId=151968>.</span></span>

 

 





