---
title: Присоединенные к домену и не присоединенные к домену клиенты
description: Присоединенные к домену и не присоединенные к домену клиенты
author: dansimp
ms.assetid: a935dc98-de60-45f3-ab74-2444ce082e88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4385ab3f26bb867dd649fe768e1500c9d015ffa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821632"
---
# <span data-ttu-id="a9086-103">Присоединенные к домену и не присоединенные к домену клиенты</span><span class="sxs-lookup"><span data-stu-id="a9086-103">Domain-Joined and Non-Domain-Joined Clients</span></span>


<span data-ttu-id="a9086-104">Настольные компьютеры App-V можно настроить так, чтобы разрешить подключение к сети независимо от того, является ли клиент присоединенным к домену или не присоединен к домену.</span><span class="sxs-lookup"><span data-stu-id="a9086-104">The App-V Desktop Client can be configured to allow connection to a network regardless of whether the client is domain joined or non-domain joined.</span></span>

## <span data-ttu-id="a9086-105">Клиенты, подключенные к домену</span><span class="sxs-lookup"><span data-stu-id="a9086-105">Domain-Joined Clients</span></span>


<span data-ttu-id="a9086-106">Клиенты, которые подключены к домену, но вне внутренней сети, могут взаимодействовать с инфраструктурой App-V с помощью VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="a9086-106">Clients that are domain joined, but outside the internal network, can communicate with the App-V infrastructure by using a VPN connection.</span></span> <span data-ttu-id="a9086-107">Если вы хотите предоставить пользователям возможность выйти из внутренней сети, но по-прежнему общаться в инфраструктуре App-V, для вашей среды требуется очень малая Настройка.</span><span class="sxs-lookup"><span data-stu-id="a9086-107">When you want to provide users the ability to leave the internal network but still communicate in an App-V infrastructure, your environment requires very little setup.</span></span> <span data-ttu-id="a9086-108">Поскольку пользователи уже являются частью домена, необходимо убедиться, что на клиенте поддерживаются кэшированные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="a9086-108">Because the users are already part of the domain, you simply need to ensure that Cached Credentials are supported on the client.</span></span> <span data-ttu-id="a9086-109">Это конфигурация по умолчанию, и любые изменения, внесенные в этот параметр, можно выполнить из групповых политик.</span><span class="sxs-lookup"><span data-stu-id="a9086-109">This is the default configuration, and any changes to this setting can be accomplished from Group Policies.</span></span>

<span data-ttu-id="a9086-110">Как уже упоминалось в руководстве по рекомендации по обеспечению безопасности App-V, пользователь попытается отправить ему пользовательский билет на проверку подлинности в инфраструктуре App-V.</span><span class="sxs-lookup"><span data-stu-id="a9086-110">As mentioned in the App-V Security Best Practices Guide, the user will attempt to send their user ticket to the App-V infrastructure for authentication.</span></span> <span data-ttu-id="a9086-111">Если срок действия билета истек, он вернется к использованию NTLM и кэшированных учетных данных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="a9086-111">If the ticket is expired, it will revert to using NTLM and the cached credentials on the computer.</span></span> <span data-ttu-id="a9086-112">Чтобы разрешить перемещение, администраторы должны удостовериться, что доступ к серверу публикации осуществляется внутренне с помощью внешнего доступа по имени, чтобы имена правильно разрешились.</span><span class="sxs-lookup"><span data-stu-id="a9086-112">To allow roaming, administrators must ensure that the publishing server being accessed internally is available at the same name externally for the names to resolve properly.</span></span>

## <span data-ttu-id="a9086-113">Клиенты, не присоединенные к домену</span><span class="sxs-lookup"><span data-stu-id="a9086-113">Non-Domain-Joined Clients</span></span>


<span data-ttu-id="a9086-114">Клиенты, не присоединенные к домену, но требующие взаимодействия в инфраструктуре App-v, должны быть настроены таким же, чтобы обеспечить успешную проверку подлинности в инфраструктуре App-V.</span><span class="sxs-lookup"><span data-stu-id="a9086-114">Clients that are non-domain joined but need to communicate in the App-V infrastructure must be configured to ensure that authentication to the App-V infrastructure is successful.</span></span> <span data-ttu-id="a9086-115">Клиент App-V для настольных компьютеров не допускает запросов на обновление публикации, поэтому клиент должен быть настроен таким образом, чтобы он содержал нужные учетные данные для сервера управления App-V.</span><span class="sxs-lookup"><span data-stu-id="a9086-115">The App-V Desktop Client does not permit prompting for the publishing refresh process, so the client must be configured to present the proper credentials to the App-V Management Server.</span></span>

<span data-ttu-id="a9086-116">Сервер публикаций, настроенный для обновления публикации из клиента, не подключенного к домену, требует, чтобы внешнее имя, доступное клиентам, было настроено в качестве общего имени или альтернативного имени субъекта (SAN) на сертификате сервера публикации.</span><span class="sxs-lookup"><span data-stu-id="a9086-116">The publishing server, which is configured for publishing refresh from the non-domain joined client, requires that the external name that clients access is configured as the common name or a subject alternate name (SAN) on the publishing server’s certificate.</span></span>

## <span data-ttu-id="a9086-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a9086-117">Related topics</span></span>


[<span data-ttu-id="a9086-118">Назначение правильных учетных данных для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9086-118">How to Assign the Proper Credentials for Windows Vista</span></span>](how-to-assign--the-proper-credentials-for-windows-vista.md)

[<span data-ttu-id="a9086-119">Назначение правильных учетных данных для Windows XP</span><span class="sxs-lookup"><span data-stu-id="a9086-119">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





