---
title: Сведения о лицензировании приложений
description: Сведения о лицензировании приложений
author: dansimp
ms.assetid: 6b487641-1627-4e91-b829-04f001008176
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546bc630b95fe52f960c7bdfb771d3e2561f9318
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820099"
---
# <span data-ttu-id="5d10b-103">Сведения о лицензировании приложений</span><span class="sxs-lookup"><span data-stu-id="5d10b-103">About Application Licensing</span></span>


<span data-ttu-id="5d10b-104">Вы можете управлять лицензиями приложений прямо из консоли управления сервером Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="5d10b-104">You can manage application licenses directly from the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="5d10b-105">Типы лицензий</span><span class="sxs-lookup"><span data-stu-id="5d10b-105">License Types</span></span>


<span data-ttu-id="5d10b-106">Система виртуализации приложений System Center в настоящее время поддерживает следующие типы лицензий:</span><span class="sxs-lookup"><span data-stu-id="5d10b-106">The System Center Application Virtualization System currently supports the following license types:</span></span>

-   <span data-ttu-id="5d10b-107">**Неограниченная лицензия**— предоставляет доступ к приложению на любое количество одновременных пользователей.</span><span class="sxs-lookup"><span data-stu-id="5d10b-107">**Unlimited License**—Allows access to the application by any number of simultaneous users.</span></span> <span data-ttu-id="5d10b-108">Этот метод лицензирования подходит, если вы хотите связать лицензию на уровне Организации с приложением.</span><span class="sxs-lookup"><span data-stu-id="5d10b-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="5d10b-109">**Одновременная лицензия**— позволяет определить максимальное количество пользователей, которые могут использовать приложение.</span><span class="sxs-lookup"><span data-stu-id="5d10b-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="5d10b-110">" **Лицензия с именем**" — позволяет назначать лицензию отдельному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5d10b-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="5d10b-111">Именованную лицензию можно использовать, чтобы гарантировать, что определенный пользователь всегда сможет запускать приложение.</span><span class="sxs-lookup"><span data-stu-id="5d10b-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="5d10b-112">Вы можете сочетать одновременные и именованные лицензии для одного и того же приложения.</span><span class="sxs-lookup"><span data-stu-id="5d10b-112">You can combine concurrent and named licenses for the same application.</span></span>

<span data-ttu-id="5d10b-113">Лицензирование отключено по умолчанию, но вы можете включить его на вкладке " **конвейер поставщика** " в диалоговом окне **свойств поставщика** .</span><span class="sxs-lookup"><span data-stu-id="5d10b-113">Licensing is disabled by default, but you can enable it from the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span> <span data-ttu-id="5d10b-114">Дополнительные сведения о включении и отключении лицензирования можно найти [в разделе Настройка и отключение лицензирования приложений](how-to-set-up-or-disable-application-licensing.md).</span><span class="sxs-lookup"><span data-stu-id="5d10b-114">For details about enabling and disabling licensing, see [How to Set Up or Disable Application Licensing](how-to-set-up-or-disable-application-licensing.md).</span></span>

## <span data-ttu-id="5d10b-115">Политики поставщика</span><span class="sxs-lookup"><span data-stu-id="5d10b-115">Provider Policies</span></span>


<span data-ttu-id="5d10b-116">Политики поставщика были разработаны для модели поставщика услуг приложения (ASP).</span><span class="sxs-lookup"><span data-stu-id="5d10b-116">Provider policies were developed for the Application Service Provider (ASP) model.</span></span> <span data-ttu-id="5d10b-117">В этой модели один ASP может размещать единую систему Application Virtualization для нескольких клиентов, где каждый клиент должен оставаться изолированным.</span><span class="sxs-lookup"><span data-stu-id="5d10b-117">In this model, a single ASP can host a single Application Virtualization System for multiple clients, where each client needs to remain isolated.</span></span> <span data-ttu-id="5d10b-118">Клиенты могут радикально различаться, например, если один клиент может требовать проверку подлинности, а другой — нет.</span><span class="sxs-lookup"><span data-stu-id="5d10b-118">Clients might have dramatically different requirements—for example, one client might require authentication while another does not.</span></span> <span data-ttu-id="5d10b-119">Вы можете использовать политики поставщика для сопоставления разрешений с клиентами, чтобы только утвержденные пользователи могли получать доступ к каждому виртуальному приложению или пакету виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="5d10b-119">You can use provider policies to associate permissions with clients so that only the approved users can access each virtual application or virtual application package.</span></span>

<span data-ttu-id="5d10b-120">Для корпоративных клиентов вы можете использовать эту функцию, если у вас есть строгое требование к лицензированию для одного или нескольких приложений.</span><span class="sxs-lookup"><span data-stu-id="5d10b-120">For the enterprise customer, you can use this feature when you have strict licensing requirements for one or more applications.</span></span> <span data-ttu-id="5d10b-121">В этой ситуации компонент лицензирования отключен на вкладке **конвейер поставщика** в диалоговом окне **Свойства поставщика** .</span><span class="sxs-lookup"><span data-stu-id="5d10b-121">Under this situation, the licensing component is disabled on the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span>

<span data-ttu-id="5d10b-122">На вкладке **поставщик конвейера** также есть флажки для включения проверки подлинности, авторизации (**принудительного применения параметров разрешений доступа**) и отслеживания**использования журнала (сведения об использовании**).</span><span class="sxs-lookup"><span data-stu-id="5d10b-122">The **Provider Pipeline** tab also has check boxes to enable authentication, authorization (**Enforce Access Permission Settings**), and metering (**Log Usage Information**).</span></span> <span data-ttu-id="5d10b-123">Если у вашей конфигурации есть особые требования, вы можете создать собственные компоненты конвейера и добавить их в систему, нажав кнопку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="5d10b-123">If your configuration has special requirements, you can write your own pipeline components and add them to the system by clicking the **Advanced** button.</span></span>

## <span data-ttu-id="5d10b-124">Учетные записи</span><span class="sxs-lookup"><span data-stu-id="5d10b-124">Account Authorities</span></span>


<span data-ttu-id="5d10b-125">Центр учетных записей — это домен, в котором установлен сервер Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="5d10b-125">The account authority is the domain in which the Application Virtualization Server is installed.</span></span> <span data-ttu-id="5d10b-126">После установки сервера вам будет предложено указать имя домена; домен, в котором установлен компьютер, по умолчанию будет обнаружен и использован.</span><span class="sxs-lookup"><span data-stu-id="5d10b-126">As you proceed through the server installation, you are prompted to supply a domain name; the domain in which the computer is installed is detected and used by default.</span></span> <span data-ttu-id="5d10b-127">При попытке входа в систему пользователи получат запрос на ввод учетных данных, прежде чем они смогут получить доступ к этому домену.</span><span class="sxs-lookup"><span data-stu-id="5d10b-127">When users attempt to log in to the system, they are prompted for their credentials before they can access that domain.</span></span>

<span data-ttu-id="5d10b-128">Система виртуализации приложений поддерживает несколько доменов.</span><span class="sxs-lookup"><span data-stu-id="5d10b-128">The Application Virtualization System supports multiple domains.</span></span> <span data-ttu-id="5d10b-129">Вы можете предоставить доступ к приложениям группам пользователей в других доменах, если установлено отношение доверия между доменами.</span><span class="sxs-lookup"><span data-stu-id="5d10b-129">You can grant application access to user groups in other domains if a trust relationship is established between domains.</span></span> <span data-ttu-id="5d10b-130">Пользователи должны вводить учетные данные, которые распознаются каждым доменом.</span><span class="sxs-lookup"><span data-stu-id="5d10b-130">Users must supply credentials that are recognized by each domain.</span></span>

<span data-ttu-id="5d10b-131">В консоли управления сервером виртуализации приложений вы можете изменить основной домен (центр учетных записей) и учетные данные, которые используются для доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="5d10b-131">In the Application Virtualization Server Management Console, you can change the primary domain (account authority) and the credentials that are used to access it.</span></span>

## <span data-ttu-id="5d10b-132">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="5d10b-132">Authentication</span></span>


<span data-ttu-id="5d10b-133">Проверка подлинности — это механизм, который используется для подтверждения личности пользователя.</span><span class="sxs-lookup"><span data-stu-id="5d10b-133">Authentication is the mechanism used to confirm a user's identity.</span></span> <span data-ttu-id="5d10b-134">Любой пользователь с известным именем пользователя и паролем имеет доступ.</span><span class="sxs-lookup"><span data-stu-id="5d10b-134">Any user with a recognized user name and password has access.</span></span>

<span data-ttu-id="5d10b-135">В системе виртуализации приложений вы можете включить или отключить проверку подлинности с помощью флажка на вкладке **конвейер поставщика** . По умолчанию проверка подлинности Windows включена.</span><span class="sxs-lookup"><span data-stu-id="5d10b-135">In the Application Virtualization System, you can enable or disable authentication through a check box on the **Provider Pipeline** tab. By default, Windows Authentication is enabled.</span></span>

## <span data-ttu-id="5d10b-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="5d10b-136">Authorization</span></span>


<span data-ttu-id="5d10b-137">Авторизация — это процесс, который используется для подтверждения личности пользователя.</span><span class="sxs-lookup"><span data-stu-id="5d10b-137">Authorization is the process used to confirm a user’s identity.</span></span> <span data-ttu-id="5d10b-138">После подтверждения личности пользователя система определяет, предоставил ли пользователь доступ к системе и каким приложениям он предоставил доступ.</span><span class="sxs-lookup"><span data-stu-id="5d10b-138">After confirming the user's identity, the system determines whether the user was granted access to the system and to which applications the user was granted access.</span></span> <span data-ttu-id="5d10b-139">Для включения или отключения авторизации в консоли управления сервером виртуализации приложений установлен флажок **принудительно установить разрешения на доступ** на вкладке **конвейера поставщика** .</span><span class="sxs-lookup"><span data-stu-id="5d10b-139">The Application Virtualization Server Management Console has an **Enforce Access Permission Settings** check box on the **Provider Pipeline** tab to enable or disable authorization.</span></span>

<span data-ttu-id="5d10b-140">В системе Виртуализация приложений доступ предоставляется только для группы пользователей, а не для отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="5d10b-140">In the Application Virtualization System, access is granted to a user group only, not to individual users.</span></span>

## <span data-ttu-id="5d10b-141">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5d10b-141">Related topics</span></span>


[<span data-ttu-id="5d10b-142">Управление лицензиями приложений на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="5d10b-142">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="5d10b-143">Установка или отключение лицензирования приложений</span><span class="sxs-lookup"><span data-stu-id="5d10b-143">How to Set Up or Disable Application Licensing</span></span>](how-to-set-up-or-disable-application-licensing.md)

[<span data-ttu-id="5d10b-144">Консоль управления серверами: узел политик поставщика</span><span class="sxs-lookup"><span data-stu-id="5d10b-144">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





