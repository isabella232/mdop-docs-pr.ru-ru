---
title: Проектирование репозиториев образа MED-V
description: Проектирование репозиториев образа MED-V
author: dansimp
ms.assetid: e153154d-2751-4990-b94d-a2d76242c15f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0c59a0dd2d1b3a78bd211c6a6353a86c77d8fc2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823612"
---
# <span data-ttu-id="0e503-103">Проектирование репозиториев образа MED-V</span><span class="sxs-lookup"><span data-stu-id="0e503-103">Design the MED-V Image Repositories</span></span>


<span data-ttu-id="0e503-104">После создания и упаковки изображений для MED-V они могут храниться на файловом сервере в любом месте.</span><span class="sxs-lookup"><span data-stu-id="0e503-104">After MED-V images are created and packed, they can be stored on a file server in any location.</span></span> <span data-ttu-id="0e503-105">Файлы могут быть отправлены по протоколу HTTP или HTTPS одним или несколькими серверами IIS.</span><span class="sxs-lookup"><span data-stu-id="0e503-105">The files may be sent over HTTP or HTTPS by one or more IIS servers.</span></span> <span data-ttu-id="0e503-106">Репозиторий изображений может совместно использоваться несколькими экземплярами MED-V.</span><span class="sxs-lookup"><span data-stu-id="0e503-106">The image repository can be shared by multiple MED-V instances.</span></span>

<span data-ttu-id="0e503-107">Чтобы разработать репозитории изображений, сначала необходимо решить, как будут развертываться изображения для каждого клиента, а затем, требуется ли для этого клиента локальное хранилище изображений.</span><span class="sxs-lookup"><span data-stu-id="0e503-107">To design the image repositories, you must first decide how the images will be deployed to each client and then whether that client requires a local image repository.</span></span> <span data-ttu-id="0e503-108">Затем каждый репозиторий разрабатывается и размещается вместе с сопутствующим сервером IIS.</span><span class="sxs-lookup"><span data-stu-id="0e503-108">Each repository is then designed and placed, along with its accompanying IIS server.</span></span>

## <span data-ttu-id="0e503-109">Определение того, как развертываются изображения</span><span class="sxs-lookup"><span data-stu-id="0e503-109">Determine How Images Will Be Deployed</span></span>


<span data-ttu-id="0e503-110">Для каждой рабочей области для MED-V решите, как вы планируете развертывать образы MED-V на клиенте.</span><span class="sxs-lookup"><span data-stu-id="0e503-110">For each MED-V workspace, decide how you plan to deploy MED-V images to the client.</span></span> <span data-ttu-id="0e503-111">Это важно для определения количества хранилищ, необходимых для хранения упакованных изображений, которые будут помещены в них, а затем для разработки этих репозиториев.</span><span class="sxs-lookup"><span data-stu-id="0e503-111">This is important in determining how many repositories are necessary to store the packed images, where those repositories will be placed, and then to design those repositories.</span></span>

<span data-ttu-id="0e503-112">Упакованные изображения можно развертывать следующими способами:</span><span class="sxs-lookup"><span data-stu-id="0e503-112">Packed images can be deployed in the following ways:</span></span>

-   <span data-ttu-id="0e503-113">Загружен по сети с сервера распространения изображений, включающего файловый сервер и сервер IIS.</span><span class="sxs-lookup"><span data-stu-id="0e503-113">Downloaded over the network from an image distribution server, which comprises a file server and IIS server.</span></span>

-   <span data-ttu-id="0e503-114">На съемном носителе (например, USB-накопителе или DVD-диске).</span><span class="sxs-lookup"><span data-stu-id="0e503-114">On removable media, such as a USB drive or DVD.</span></span>

-   <span data-ttu-id="0e503-115">Предварительно заготовить к каталогу хранилища изображений на клиентском компьютере с помощью корпоративного центра распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="0e503-115">Pre-staged to an image store directory on the client computer using an enterprise software distribution center.</span></span>

<span data-ttu-id="0e503-116">Определите, какой метод или методы будут использоваться при развертывании изображений MED-V на каждом из клиентов и в том случае, если для расположения требуется репозиторий изображений.</span><span class="sxs-lookup"><span data-stu-id="0e503-116">Decide which method, or methods, will be used to deploy MED-V images to each of the clients and whether the location will require an image repository.</span></span>

## <span data-ttu-id="0e503-117">Определение количества репозиториев изображений</span><span class="sxs-lookup"><span data-stu-id="0e503-117">Determine the Number of Image Repositories</span></span>


<span data-ttu-id="0e503-118">Теперь, когда вы определили минимальную подходящую подписку, добавьте дополнительные, если применимо любое из указанных ниже условий.</span><span class="sxs-lookup"><span data-stu-id="0e503-118">Now that you have determined the minimum number of repositories you need, add more if any of the following criteria apply:</span></span>

-   <span data-ttu-id="0e503-119">Организационные или нормативные причины для разделения изображений MED-v (некоторые образы MED-V могут не сосуществовать в одном и том же репозитории).</span><span class="sxs-lookup"><span data-stu-id="0e503-119">Organizational or regulatory reasons to separate the MED-V images—some MED-V images may not be able to coexist in the same repository.</span></span> <span data-ttu-id="0e503-120">Например, для конфиденциальных персональных данных может потребоваться хранилище на сервере, доступное только ограниченному набору сотрудников, которым нужен доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="0e503-120">For example, sensitive personal data may require storage on a server that is only available to a limited set of employees who need access to the data.</span></span>

-   <span data-ttu-id="0e503-121">Клиенты в изолированных сетях — если изображения будут развертываться по сети, определите, являются ли какие-либо сети изолированными и требуют отдельного репозитория.</span><span class="sxs-lookup"><span data-stu-id="0e503-121">Clients in isolated networks—if images will be deployed over the network, determine whether any networks are isolated and require a separate repository.</span></span> <span data-ttu-id="0e503-122">Например, организации часто изолируют лабораторные сети из производственных сетей.</span><span class="sxs-lookup"><span data-stu-id="0e503-122">For example, organizations often isolate lab networks from production networks.</span></span>

-   <span data-ttu-id="0e503-123">Клиенты в удаленных сетях — если изображения будут развертываться по сети, некоторые клиентские компьютеры могут быть отделены от репозитория сетевыми связями, которые имеют недостаточную пропускную способность для обеспечения адекватной работы, когда клиент загружает рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="0e503-123">Clients in remote networks—if images will be deployed over the network, some client machines may be separated from the repository by network links that have insufficient bandwidth to provide an adequate experience when a client loads a MED-V workspace.</span></span> <span data-ttu-id="0e503-124">При необходимости создайте дополнительные экземпляры MED-V, чтобы решить эту необходимость.</span><span class="sxs-lookup"><span data-stu-id="0e503-124">If necessary, design additional MED-V instances to address this need.</span></span>

<span data-ttu-id="0e503-125">Добавьте эти репозитории в проект.</span><span class="sxs-lookup"><span data-stu-id="0e503-125">Add these repositories to the design.</span></span> <span data-ttu-id="0e503-126">Определите имя для каждого репозитория и причину его создания.</span><span class="sxs-lookup"><span data-stu-id="0e503-126">Decide on a name for each repository and the reason for designing it.</span></span> <span data-ttu-id="0e503-127">Решите, какие образы для MED-V будут храниться в репозиториях и какие клиенты MED-V будут загружать рабочие области MED-V с изображениями из репозитория.</span><span class="sxs-lookup"><span data-stu-id="0e503-127">Decide which MED-V images the repositories will hold and which MED-V clients will load MED-V workspaces with images from the repository.</span></span>

## <span data-ttu-id="0e503-128">Разработка и помещение Репозитарией изображений</span><span class="sxs-lookup"><span data-stu-id="0e503-128">Design and Place the Image Repositories</span></span>


<span data-ttu-id="0e503-129">Когда для клиентов будет доступно новое изображение, клиенты начинают скачивать изображение, возможно, одновременно.</span><span class="sxs-lookup"><span data-stu-id="0e503-129">When a new image is available to clients, clients begin downloading the image, possibly simultaneously.</span></span> <span data-ttu-id="0e503-130">Это приведет к созданию большого спроса на репозиторий и необходимости учитывать его при проектировании репозитория изображений.</span><span class="sxs-lookup"><span data-stu-id="0e503-130">This creates a high demand on the repository and must be taken into account when designing the image repository.</span></span>

<span data-ttu-id="0e503-131">Для каждого репозитория Определите объем данных, которые он будет хранить.</span><span class="sxs-lookup"><span data-stu-id="0e503-131">For each repository, determine the amount of data it will store.</span></span> <span data-ttu-id="0e503-132">Суммировать размеры изображений, которые будут храниться в репозитории.</span><span class="sxs-lookup"><span data-stu-id="0e503-132">Sum the sizes of images that will be stored in the repository.</span></span> <span data-ttu-id="0e503-133">Это значение дискового пространства, необходимого на файловом сервере.</span><span class="sxs-lookup"><span data-stu-id="0e503-133">This is the value of the disk space required on the file server.</span></span>

<span data-ttu-id="0e503-134">Затем добавьте в репозиторий число клиентов, которые могут загружать образы MED-V.</span><span class="sxs-lookup"><span data-stu-id="0e503-134">Next, add up the number of clients that may download MED-V images from the repository.</span></span> <span data-ttu-id="0e503-135">Это максимальное число одновременных Скачиваний, которые могут возникнуть при загрузке нового изображения MED-V в репозиторий.</span><span class="sxs-lookup"><span data-stu-id="0e503-135">This is the maximum number of concurrent downloads that can occur when a new MED-V image is loaded into the repository.</span></span> <span data-ttu-id="0e503-136">Файловый сервер должен быть разработан с помощью дисковой подсистемы, которая может отвечать требованиям к вводу-выводу, который будет создан.</span><span class="sxs-lookup"><span data-stu-id="0e503-136">The file server must be designed with a disk subsystem that can meet the IO demands this will create.</span></span>

<span data-ttu-id="0e503-137">Репозиторий изображений может находиться в той же системе, что и сервер MED-V, и на сервере с запущенным SQL Server или на удаленном файловом общем доступе.</span><span class="sxs-lookup"><span data-stu-id="0e503-137">The image repository can reside on the same system as the MED-V server and the server running SQL Server, or on a remote file share.</span></span> <span data-ttu-id="0e503-138">Вы также можете запустить его в виртуальной машине Windows Server2008 Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="0e503-138">You can also run it in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="0e503-139">Проверьте расположение в сети клиентов, которые будут обслуживаться в репозитории изображений, и поместите его в сетевую папку, в которой будет достаточно пропускной способности для соответствия требованиям уровня обслуживания для этих клиентов.</span><span class="sxs-lookup"><span data-stu-id="0e503-139">Check the network location of the clients that the image repository will service, and place the repository in a network location where it will have sufficient bandwidth to meet the service level expectations of those clients.</span></span>

### <span data-ttu-id="0e503-140">Отказоустойчивость</span><span class="sxs-lookup"><span data-stu-id="0e503-140">Fault Tolerance</span></span>

<span data-ttu-id="0e503-141">Если репозиторий изображений недоступен, клиенты не смогут загрузить новые или обновленные образы MED-V.</span><span class="sxs-lookup"><span data-stu-id="0e503-141">If the image repository is unavailable, clients will not be able to download new or updated MED-V images.</span></span> <span data-ttu-id="0e503-142">Чтобы разработать параметры отказоустойчивости для файлового сервера и отказоустойчивых дисков, ознакомьтесь с руководством по [планированию инфраструктуры и проектированию Microsoft SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) .</span><span class="sxs-lookup"><span data-stu-id="0e503-142">To design fault-tolerance options for the file server and fault-tolerant disks, see the [Infrastructure Planning and Design Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) guide.</span></span>

## <span data-ttu-id="0e503-143">Проектирование и размещение серверов IIS</span><span class="sxs-lookup"><span data-stu-id="0e503-143">Design and Place the IIS Servers</span></span>


<span data-ttu-id="0e503-144">Этот раздел подходит только в том случае, если клиенты загружают файлы изображений по сети по протоколу HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0e503-144">This section is only relevant if clients will download image files over the network using HTTP or HTTPS.</span></span>

<span data-ttu-id="0e503-145">Сервер IIS может сосуществовать в той же системе, что и сервер MED-V, и на сервере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0e503-145">The IIS server can coexist on the same system as the MED-V server and the server running SQL Server.</span></span> <span data-ttu-id="0e503-146">Оно также может выполняться в виртуальной машине Windows Server2008 Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="0e503-146">It can also run in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="0e503-147">Инфраструктура сервера IIS должна иметь достаточную пропускную способность для доставки изображений клиентам в рамках ожидаемого уровня обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0e503-147">The IIS server infrastructure must have sufficient throughput to deliver images to clients within the service level expectations of the organization.</span></span> <span data-ttu-id="0e503-148">Она должна быть разработана с помощью дисковой подсистемы, которая может соответствовать требованиям к вводу-выводу.</span><span class="sxs-lookup"><span data-stu-id="0e503-148">It must be designed with a disk subsystem that can meet the IO demands this creates.</span></span>

<span data-ttu-id="0e503-149">Для каждого репозитория изображений следует суммировать количество клиентов, которые могут загружать образы MED-V с помощью IIS.</span><span class="sxs-lookup"><span data-stu-id="0e503-149">For each image repository, sum the number of clients that may download MED-V images using IIS.</span></span> <span data-ttu-id="0e503-150">Это максимальное число одновременных Скачиваний, которые могут возникнуть при загрузке изображения в репозиторий.</span><span class="sxs-lookup"><span data-stu-id="0e503-150">This is the maximum number of concurrent downloads that can occur when an image is loaded into the repository.</span></span> <span data-ttu-id="0e503-151">Используйте сумму пропускной способности и ожидаемые значения уровня обслуживания, определенные в разделе [Определение области охвата проекта](define-the-project-scope.md) для планирования инфраструктуры сервера IIS и определения подходящего объема пропускной способности, выделяемой для репозитория.</span><span class="sxs-lookup"><span data-stu-id="0e503-151">Use the throughput sum and the service level expectations determined in [Define the Project Scope](define-the-project-scope.md) to plan the design of the IIS server infrastructure and to determine the appropriate amount of bandwidth to allocate for the repository.</span></span>

<span data-ttu-id="0e503-152">Для создания инфраструктуры служб IIS ознакомьтесь с [разработкой "Планирование инфраструктуры и проектирование Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) ".</span><span class="sxs-lookup"><span data-stu-id="0e503-152">To design the IIS infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

### <span data-ttu-id="0e503-153">Отказоустойчивость</span><span class="sxs-lookup"><span data-stu-id="0e503-153">Fault Tolerance</span></span>

<span data-ttu-id="0e503-154">Если инфраструктура сервера IIS недоступна, клиенты не смогут скачивать новые или обновленные образы.</span><span class="sxs-lookup"><span data-stu-id="0e503-154">If the IIS server infrastructure is unavailable, clients will not be able to download new or updated images.</span></span> <span data-ttu-id="0e503-155">Чтобы настроить отказоустойчивость, сервер IIS под управлением Windows Server2008 можно поместить в отказоустойчивый кластер.</span><span class="sxs-lookup"><span data-stu-id="0e503-155">To configure fault tolerance, the Windows Server2008-based IIS server can be placed in a failover cluster.</span></span> <span data-ttu-id="0e503-156">Для разработки отказоустойчивости инфраструктуры сервера IIS ознакомьтесь с [разработкой "Планирование инфраструктуры и проектирование Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) ".</span><span class="sxs-lookup"><span data-stu-id="0e503-156">To design the fault tolerance for the IIS server infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

## <span data-ttu-id="0e503-157">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0e503-157">Related topics</span></span>


[<span data-ttu-id="0e503-158">Развертывание рабочей области MED-V с помощью корпоративной системы распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="0e503-158">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)

[<span data-ttu-id="0e503-159">Развертывание рабочей области MED-V с помощью пакета развертывания</span><span class="sxs-lookup"><span data-stu-id="0e503-159">Deploying a MED-V Workspace Using a Deployment Package</span></span>](deploying-a-med-v-workspace-using-a-deployment-package.md)

 

 





