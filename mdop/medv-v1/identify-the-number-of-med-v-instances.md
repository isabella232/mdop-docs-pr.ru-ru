---
title: Определение количества экземпляров MED-V
description: Определение количества экземпляров MED-V
author: dansimp
ms.assetid: edea9bdf-a28c-4d24-9298-7bd6536c3a94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22f7d54318d2dc489461474e5531c5162d8c087d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824259"
---
# <span data-ttu-id="edfa3-103">Определение количества экземпляров MED-V</span><span class="sxs-lookup"><span data-stu-id="edfa3-103">Identify the Number of MED-V Instances</span></span>


<span data-ttu-id="edfa3-104">Необходимо определить количество экземпляров MED-V, а также определить область для каждого экземпляра, чтобы можно было спроектировать инфраструктуру сервера.</span><span class="sxs-lookup"><span data-stu-id="edfa3-104">You need to determine the number of MED-V instances, as well as define the scope for each instance so that you can design the server infrastructure.</span></span> <span data-ttu-id="edfa3-105">Экземпляр MED-V включает следующее:</span><span class="sxs-lookup"><span data-stu-id="edfa3-105">A MED-V instance includes the following:</span></span>

-   <span data-ttu-id="edfa3-106">Сервер MED-V и рабочие области MED-V, хранящиеся на сервере, в том числе разрешения Active Directory.</span><span class="sxs-lookup"><span data-stu-id="edfa3-106">The MED-V server and the MED-V workspaces stored on the server, including Active Directory permissions.</span></span>

-   <span data-ttu-id="edfa3-107">База данных SQL Server, в которой хранятся клиентские события.</span><span class="sxs-lookup"><span data-stu-id="edfa3-107">A SQL Server database that stores client events.</span></span> <span data-ttu-id="edfa3-108">База данных может совместно использоваться несколькими экземплярами MED-V.</span><span class="sxs-lookup"><span data-stu-id="edfa3-108">The database may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="edfa3-109">Репозиторий изображений для упакованных изображений MED-V.</span><span class="sxs-lookup"><span data-stu-id="edfa3-109">The image repository for the packed MED-V images.</span></span> <span data-ttu-id="edfa3-110">Хранилище может совместно использоваться несколькими экземплярами MED-V.</span><span class="sxs-lookup"><span data-stu-id="edfa3-110">The repository may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="edfa3-111">Консоль управления, используемая для создания и упаковки изображений, а также для создания рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="edfa3-111">The management console used to create and pack images and to create MED-V workspaces.</span></span> <span data-ttu-id="edfa3-112">Консоль нельзя использовать одновременно несколькими экземплярами MED-V, но ее можно отключить от одного сервера MED-V и затем подключиться к другому серверу MED-V.</span><span class="sxs-lookup"><span data-stu-id="edfa3-112">The console cannot be used simultaneously by multiple MED-V instances, but it can be disconnected from one MED-V server and then connected to a different MED-V server.</span></span>

-   <span data-ttu-id="edfa3-113">Клиенты MED-V, получающие рабочие области MED-V, и авторизацию для их использования на сервере.</span><span class="sxs-lookup"><span data-stu-id="edfa3-113">MED-V clients that receive MED-V workspaces, and authorization to use them, from the server.</span></span>

<span data-ttu-id="edfa3-114">Отдельные экземпляры MED-V нельзя интегрировать или совместно использовать в рабочих областях MED-V.</span><span class="sxs-lookup"><span data-stu-id="edfa3-114">Separate MED-V instances cannot be integrated or share MED-V workspaces.</span></span> <span data-ttu-id="edfa3-115">Таким образом, каждый дополнительный экземпляр децентрализует управление виртуализацией.</span><span class="sxs-lookup"><span data-stu-id="edfa3-115">Therefore, each additional instance decentralizes the virtualization management.</span></span>

## <span data-ttu-id="edfa3-116">Определение количества требуемых экземпляров MED-V</span><span class="sxs-lookup"><span data-stu-id="edfa3-116">Determine the Number of MED-V Instances Required</span></span>


<span data-ttu-id="edfa3-117">Начните с того, что вы используете один экземпляр MED-V.</span><span class="sxs-lookup"><span data-stu-id="edfa3-117">Start by assuming you are using one MED-V instance.</span></span> <span data-ttu-id="edfa3-118">Затем Рассматривайте указанные ниже условия и добавляйте дополнительные экземпляры для каждого условия, которое применяется к вашей инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="edfa3-118">Then, consider the following conditions, and add additional instances for each condition that applies to your infrastructure.</span></span>

-   <span data-ttu-id="edfa3-119">Количество поддерживаемых пользователей (каждый из экземпляров MED-V может поддерживать до 5 000 одновременно активных клиентов).</span><span class="sxs-lookup"><span data-stu-id="edfa3-119">Number of supported users—Each MED-V instance can support up to 5,000 concurrently active clients.</span></span> <span data-ttu-id="edfa3-120">Параллельно активный означает, что клиент подключен к серверу MED-V и отправляет опросы на сервер для обновления политики и изображений, а также для событий.</span><span class="sxs-lookup"><span data-stu-id="edfa3-120">Concurrently active means the client is online with the MED-V server and sending polls to the server for policy and image updates, as well as events.</span></span> <span data-ttu-id="edfa3-121">Если ваша инфраструктура будет включать более 5 000 активных пользователей, добавьте один экземпляр для каждого пользователя 5 000.</span><span class="sxs-lookup"><span data-stu-id="edfa3-121">If your infrastructure will include more than 5,000 active users, add one instance for every 5,000 users.</span></span>

-   <span data-ttu-id="edfa3-122">Пользователи в доменах без доверия — сервер MED-V связывает разрешения рабочей области для MED-V с пользователями и (или) группами Active Directory.</span><span class="sxs-lookup"><span data-stu-id="edfa3-122">Users in untrusted domains—The MED-V server associates MED-V workspace permissions with Active Directory users and/or groups.</span></span> <span data-ttu-id="edfa3-123">Для этого требуется, чтобы пользователи MED-V существовали в пределах границы доверия сервера MED-V.</span><span class="sxs-lookup"><span data-stu-id="edfa3-123">This requires MED-V users to exist within the trust boundary of the MED-V server.</span></span> <span data-ttu-id="edfa3-124">Добавьте один экземпляр MED-V для каждой группы пользователей MED-V из отдельного домена, не имеющего доверия.</span><span class="sxs-lookup"><span data-stu-id="edfa3-124">Add one MED-V instance for each group of MED-V users that is in a separate, untrusted domain.</span></span>

-   <span data-ttu-id="edfa3-125">Клиенты в изолированных сетях — определяют, находятся ли клиенты в изолированных сетях, и поэтому требуют отдельного экземпляра MED-V.</span><span class="sxs-lookup"><span data-stu-id="edfa3-125">Clients in isolated networks—Determine whether any clients reside in networks that are isolated and therefore require a separate MED-V instance.</span></span> <span data-ttu-id="edfa3-126">Например, организации часто изолируют лабораторные сети из производственных сетей.</span><span class="sxs-lookup"><span data-stu-id="edfa3-126">For example, organizations often isolate lab networks from production networks.</span></span> <span data-ttu-id="edfa3-127">Добавьте экземпляр MED-V для каждой изолированной сети, которая будет содержать клиенты MED-V.</span><span class="sxs-lookup"><span data-stu-id="edfa3-127">Add a MED-V instance for each isolated network that will contain MED-V clients.</span></span>

-   <span data-ttu-id="edfa3-128">Организационные требования. организациям может потребоваться, чтобы группа клиентов управлялась отдельным экземпляром MED-V по соображениям безопасности, например при доставке конфиденциальных приложений только ограниченному набору пользователей в домене.</span><span class="sxs-lookup"><span data-stu-id="edfa3-128">Organizational requirements—The organization may require that a group of clients be managed by a separate MED-V instance for security reasons, such as when sensitive applications are delivered only to a restricted set of users within a domain.</span></span> <span data-ttu-id="edfa3-129">Например, сотрудник отдела заработной платы может отказаться от доступа пользователей других отделов к экземпляру MED-V, в котором хранится политика для обработки зарплаты.</span><span class="sxs-lookup"><span data-stu-id="edfa3-129">For example, the payroll department may deny users from other departments access to the MED-V instance that stores policy for payroll processing.</span></span> <span data-ttu-id="edfa3-130">Кроме того, если в организации используется модель распределенного управления, для каждой бизнес-группы с клиентами MED-V может потребоваться отдельный экземпляр MED-V, чтобы разрешить группе управлять своей виртуальной средой.</span><span class="sxs-lookup"><span data-stu-id="edfa3-130">Additionally, if the organization uses a distributed management model, a separate MED-V instance may be required for each business group having MED-V clients in order to enable the group to manage its own virtualized environment.</span></span> <span data-ttu-id="edfa3-131">Добавьте один экземпляр MED-V для каждого отдельного требования Организации.</span><span class="sxs-lookup"><span data-stu-id="edfa3-131">Add one MED-V instance for each separate organizational requirement.</span></span>

-   <span data-ttu-id="edfa3-132">Юридическая информация — вопросы, связанные с безопасностью, конфиденциальностью и Fiduciary законами, может потребоваться разделение некоторых данных или появление других данных, которые не пересекают национальные границы.</span><span class="sxs-lookup"><span data-stu-id="edfa3-132">Legal considerations—National security or privacy issues and fiduciary laws could require the separation of certain data or prevent other data from crossing national borders.</span></span> <span data-ttu-id="edfa3-133">При необходимости добавьте дополнительные экземпляры MED-V, чтобы решить эту необходимость.</span><span class="sxs-lookup"><span data-stu-id="edfa3-133">If necessary, add additional MED-V instances to address this need.</span></span>

<span data-ttu-id="edfa3-134">После определения количества экземпляров MED-V, необходимых для вашей инфраструктуры, а также причины для каждой из них укажите имя для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="edfa3-134">After you determine the number of MED-V instances required for your infrastructure, as well as the reasoning for each one, provide a name for each instance.</span></span>

 

 





