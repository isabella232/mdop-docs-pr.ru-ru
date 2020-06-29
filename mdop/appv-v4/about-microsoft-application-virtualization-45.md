---
title: Сведения о системе Microsoft Application Virtualization 4.5
description: Сведения о системе Microsoft Application Virtualization 4.5
author: dansimp
ms.assetid: 39f45a6f-ac55-4fd7-8a83-865e1a7034f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 30f285680ab24e9c638ff8a200946925074bddf1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820029"
---
# <span data-ttu-id="b3141-103">Сведения о системе Microsoft Application Virtualization 4.5</span><span class="sxs-lookup"><span data-stu-id="b3141-103">About Microsoft Application Virtualization 4.5</span></span>


<span data-ttu-id="b3141-104">Ранее известным как виртуализация приложений SoftGrid, Microsoft Application Virtualization (App-V) 4,5 — это первый выпуск продукта, фирменный символикой Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b3141-104">Formerly known as SoftGrid Application Virtualization, Microsoft Application Virtualization (App-V) 4.5 is the first Microsoft-branded release of the product.</span></span> <span data-ttu-id="b3141-105">Она включает в себя новые возможности, облегчающие корпоративным ИТ-организациям поддержку крупномасштабных глобальных реализаций виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="b3141-105">It includes new capabilities that make it easy for enterprise IT organizations to support large-scale, global application virtualization implementations.</span></span>

-   <span data-ttu-id="b3141-106">Динамическая виртуализация: App-V 4,5 обеспечивает гибкие возможности управления взаимодействием виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="b3141-106">Dynamic Virtualization: App-V 4.5 provides the flexibility to control virtual application interaction.</span></span> <span data-ttu-id="b3141-107">Администраторы, которые хотят консолидировать виртуальные среды и быстрее, чем упрощает администрирование, могут использовать композицию динамического набора продукта, которая последовательное и управляет пакетами для приложений промежуточного слоя отдельно от основного приложения.</span><span class="sxs-lookup"><span data-stu-id="b3141-107">Administrators who want to consolidate virtual environments and enable faster, easier administration, can use the product’s Dynamic Suite Composition, which sequences and manages packages for middleware applications separately from the main application.</span></span> <span data-ttu-id="b3141-108">Она сокращает размер пакета, устраняя избыточную упаковку по промежуточному плану.</span><span class="sxs-lookup"><span data-stu-id="b3141-108">It shrinks potential package size by eliminating redundant packaging of middleware.</span></span> <span data-ttu-id="b3141-109">Это позволяет нескольким веб-приложениям взаимодействовать с одним и тем же экземпляр виртуализированного приложения, например с Microsoft .NET Framework или средой выполнения Java на платформе Sun (JRE).</span><span class="sxs-lookup"><span data-stu-id="b3141-109">This lets multiple Web applications communicate with the same single instance of a virtualized application of, for example, Microsoft .NET Framework or Sun Java Runtime Environment (JRE).</span></span> <span data-ttu-id="b3141-110">Обновления для общих виртуальных промежуточных программного обеспечения упрощены и обновлены одно виртуальное приложение, а не несколько.</span><span class="sxs-lookup"><span data-stu-id="b3141-110">Updates for the common virtual middleware are simplified and one virtual application is updated instead of several.</span></span> <span data-ttu-id="b3141-111">Эта возможность "многие к одному" значительно сокращает стоимость обновлений.</span><span class="sxs-lookup"><span data-stu-id="b3141-111">This “many-to-one” capability greatly reduces the cost of updates.</span></span> <span data-ttu-id="b3141-112">Кроме того, это упрощает развертывание и Управление приложениями, которые используют несколько подключаемых модулей и надстроек, и улучшает управление распространением подключаемых модулей для разных групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="b3141-112">It also makes it easier to deploy and manage applications that use multiple plug-ins and add-ins, and improves management of plug-in distribution to different user groups.</span></span>

-   <span data-ttu-id="b3141-113">Расширенная масштабируемость: выберите один из трех гибких режимов развертывания.</span><span class="sxs-lookup"><span data-stu-id="b3141-113">Extended Scalability: Choose among three flexible deployment modes:</span></span>

    1.  <span data-ttu-id="b3141-114">Сервер управления виртуализацией приложений, который входит в состав пакета оптимизации рабочей среды Майкрософт и Microsoft Application Virtualization для пакетов служб удаленных рабочих столов, включает динамическую потоковую передачу, включая пакетные и активные обновления, а также требует наличия доменных служб Microsoft Active Directory и Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b3141-114">Application Virtualization Management Server, which ships as part of the Microsoft Desktop Optimization Pack and Microsoft Application Virtualization for Remote Desktop Services packages, enables dynamic streaming including package and active upgrades, and requires Microsoft Active Directory Domain Services and Microsoft SQL Server.</span></span>

    2.  <span data-ttu-id="b3141-115">Потоковый сервер Application Virtualization — упрощенная версия, которая входит в состав пакета оптимизации рабочего стола (Майкрософт) и Microsoft Application Virtualization для пакетов служб удаленных рабочих столов, обеспечивает потоковую передачу приложений, включая пакетные и активные обновления, без использования доменных служб Active Directory и переголовков баз данных, а также позволяет администраторам развертывать на существующие серверы или добавлять потоковую передачу в электронные системы.</span><span class="sxs-lookup"><span data-stu-id="b3141-115">Application Virtualization Streaming Server, a lightweight version which also ships as part of the Microsoft Desktop Optimization Pack and Microsoft Application Virtualization for Remote Desktop Services packages, offers application streaming including package and active upgrades without the Active Directory Domain Services and database overheads, and enables administrators to deploy to existing servers or add streaming to Electronic Software Delivery (ESD) systems.</span></span>

    3.  <span data-ttu-id="b3141-116">В автономном режиме виртуальные приложения можно запускать без потоковой передачи данных и взаимодействовать с диспетчером конфигурации конечных точек Майкрософт и сторонними системами ESD.</span><span class="sxs-lookup"><span data-stu-id="b3141-116">Standalone mode enables virtual applications to run without streaming and is interoperable with Microsoft Endpoint Configuration Manager and third-party ESD systems.</span></span>

-   <span data-ttu-id="b3141-117">Глобализация: продукт локализуется на 11 языках, включает поддержку приложений на иностранных языках, использующих специальные символы, и поддерживает обнаружение Active Directory и серверов и языков среды выполнения на иностранных языках.</span><span class="sxs-lookup"><span data-stu-id="b3141-117">Globalization: The product is localized across 11 languages, includes support for foreign language applications that use special characters, and supports foreign language Active Directory and servers and runtime locale detection.</span></span>

-   <span data-ttu-id="b3141-118">Стандарты безопасности Майкрософт: Microsoft Application Virtualization (App-V) 4,5 соответствует стандартам безопасности Microsoft, включая надежные вычисления, безопасность инициативы и жизненный цикл разработки Windows.</span><span class="sxs-lookup"><span data-stu-id="b3141-118">Microsoft Security Standards: Microsoft Application Virtualization (App-V) 4.5 complies with Microsoft security standards including Trustworthy Computing, Secure Windows Initiative and Security Development Lifecycle.</span></span> <span data-ttu-id="b3141-119">Она включает поддержку сценариев в Интернете и обеспечивает безопасную настройку по умолчанию для каждого из полей.</span><span class="sxs-lookup"><span data-stu-id="b3141-119">It includes support for Internet-facing scenarios and provides Secure by Default configuration out of the box.</span></span>

## <span data-ttu-id="b3141-120">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="b3141-120">In This Section</span></span>


<a href="" id="microsoft-application-virtualization-management-system-release-notes"></a>[<span data-ttu-id="b3141-121">Заметки о выпуске системы управления виртуализацией приложений Microsoft</span><span class="sxs-lookup"><span data-stu-id="b3141-121">Microsoft Application Virtualization Management System Release Notes</span></span>](microsoft-application-virtualization-management-system-release-notes.md)  
<span data-ttu-id="b3141-122">Предоставляет актуальные сведения об известных проблемах, возникающих при использовании Microsoft Application Virtualization (App-V) 4,5.</span><span class="sxs-lookup"><span data-stu-id="b3141-122">Provides the most up-to-date information about known issues with Microsoft Application Virtualization (App-V) 4.5.</span></span>

 

 





