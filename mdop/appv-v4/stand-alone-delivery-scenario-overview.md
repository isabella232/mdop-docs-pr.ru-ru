---
title: Обзор сценария изолированной доставки
description: Обзор сценария изолированной доставки
author: dansimp
ms.assetid: b109f309-f3c1-43af-996f-2a9b138dd171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f29b1c8d1c9ae97f7a21498369647f31f552839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815309"
---
# <span data-ttu-id="eaf78-103">Обзор сценария изолированной доставки</span><span class="sxs-lookup"><span data-stu-id="eaf78-103">Stand-Alone Delivery Scenario Overview</span></span>


<span data-ttu-id="eaf78-104">Автономный сценарий доставки — это идеальное решение для виртуализации приложений для сред, в которых подключение по медленной пропускной способности или отсутствие подключения ограничивает возможности потока приложения для настольной системы Application Virtualization для потоковой передачи приложений с централизованных серверов.</span><span class="sxs-lookup"><span data-stu-id="eaf78-104">The stand-alone delivery scenario is an ideal application virtualization solution for environments where either low bandwidth connectivity or no connectivity limits the ability of the Application Virtualization Desktop Client to stream applications from centralized servers.</span></span> <span data-ttu-id="eaf78-105">В этих средах пользователи часто работают удаленно и владельцы устройств устанавливают приложения с помощью файлов установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="eaf78-105">In these environments, users often work remotely and device owners install applications by using Windows Installer files.</span></span>

<span data-ttu-id="eaf78-106">Вы можете использовать Application Virtualization Sequencer для создания последовательных приложений, включающих файлы установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="eaf78-106">You can use the Application Virtualization Sequencer to create sequenced applications that include Windows Installer files.</span></span> <span data-ttu-id="eaf78-107">Эти пакеты включают виртуализированные приложения, сведения о публикации и необходимые процедуры установщика для установки пакетов на клиентские системы.</span><span class="sxs-lookup"><span data-stu-id="eaf78-107">These packages include the virtualized applications, publication information, and the necessary installer routines for installing the packages on the client systems.</span></span> <span data-ttu-id="eaf78-108">Установщик добавит пакет виртуального приложения в классическое приложение Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="eaf78-108">The installer adds the virtual application package to the Microsoft Application Virtualization Desktop Client.</span></span> <span data-ttu-id="eaf78-109">Сведения о публикации настроены на загрузку приложений из локального расположения, а не на их потоковую сеть в глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="eaf78-109">The publication information is configured to load applications from a local location rather than stream them across a WAN.</span></span> <span data-ttu-id="eaf78-110">Пользователи могут временно подключаться к сети, чтобы получать файлы установщика Windows или запускать их с DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="eaf78-110">Users can temporarily connect to a network to retrieve the Windows Installer files or can run them from a DVD.</span></span>

<span data-ttu-id="eaf78-111">Автономный сценарий доставки предоставляет пользователям следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="eaf78-111">The stand-alone delivery scenario provides users the following benefits:</span></span>

-   <span data-ttu-id="eaf78-112">Простая операция развертывания.</span><span class="sxs-lookup"><span data-stu-id="eaf78-112">Simple deployment operation.</span></span>

-   <span data-ttu-id="eaf78-113">Сеть и серверы не требуются во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="eaf78-113">Network and servers not needed at runtime.</span></span>

-   <span data-ttu-id="eaf78-114">Приложения, которые были предварительно кэшированы и доступны всем пользователям.</span><span class="sxs-lookup"><span data-stu-id="eaf78-114">Applications pre-cached and available to all users.</span></span>

<span data-ttu-id="eaf78-115">У отдельного сценария доставки есть следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="eaf78-115">The stand-alone delivery scenario has the following limitations:</span></span>

-   <span data-ttu-id="eaf78-116">Встроенные, автоматизированные отчеты недоступны; отчеты должны создаваться с помощью внешних средств создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="eaf78-116">Built-in, automated reporting is unavailable; reports must be generated with external reporting tools.</span></span>

-   <span data-ttu-id="eaf78-117">Приложения должны быть доставлены клиенту вручную, как исходные файлы установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="eaf78-117">Applications must be delivered to the client manually like the original Windows Installer files.</span></span>

## <span data-ttu-id="eaf78-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="eaf78-118">Related topics</span></span>


[<span data-ttu-id="eaf78-119">Установка клиента Application Virtualization Client вручную</span><span class="sxs-lookup"><span data-stu-id="eaf78-119">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="eaf78-120">Публикация виртуального приложения на клиенте</span><span class="sxs-lookup"><span data-stu-id="eaf78-120">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 





