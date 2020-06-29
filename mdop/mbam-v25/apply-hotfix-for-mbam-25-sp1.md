---
title: Применение исправлений для MBAM 2.5 с пакетом обновления 1 (SP1)
description: Применение исправлений для MBAM 2.5 с пакетом обновления 1 (SP1)
ms.author: ppriya-msft
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: 71f840ce4d57a0698289128f92b9d760ca14ddfc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824189"
---
# <span data-ttu-id="aa9da-103">Применение исправлений для MBAM 2.5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="aa9da-103">Applying hotfixes on MBAM 2.5 SP1</span></span>
<span data-ttu-id="aa9da-104">В этом разделе описывается процесс применения исправлений для администрирования и мониторинга Microsoft BitLocker (MBAM) Server 2,5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="aa9da-104">This topic describes the process for applying the hotfixes for Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>

### <span data-ttu-id="aa9da-105">Прежде чем начать, скачайте Последнее исправление для сервера администрирования и мониторинга Microsoft BitLocker (MBAM) Server 2,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="aa9da-105">Before you begin, download the latest hotfix of Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>
[<span data-ttu-id="aa9da-106">Пакет оптимизации для классической версии</span><span class="sxs-lookup"><span data-stu-id="aa9da-106">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> <span data-ttu-id="aa9da-107">Дополнительные сведения об этих выпусках исправлений можно найти в разделе [диаграмма версии MBAM](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span><span class="sxs-lookup"><span data-stu-id="aa9da-107">For more information about the hotfix releases, see the [MBAM version chart](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span></span>

#### <span data-ttu-id="aa9da-108">Действия по обновлению сервера MBAM для существующей среды MBAM</span><span class="sxs-lookup"><span data-stu-id="aa9da-108">Steps to update the MBAM Server for existing MBAM environment</span></span> 
1. <span data-ttu-id="aa9da-109">Удалите компонент сервера MBAM (сделайте это, открыв средство настройки сервера MBAM и выбрав команду Удалить компоненты).</span><span class="sxs-lookup"><span data-stu-id="aa9da-109">Remove MBAM server feature (do this by opening the MBAM Server Configuration Tool, then selecting Remove Features).</span></span>
2. <span data-ttu-id="aa9da-110">Удаление MBAM MDOP из панели управления | Программы и компоненты.</span><span class="sxs-lookup"><span data-stu-id="aa9da-110">Remove MDOP MBAM from Control Panel | Programs and Features.</span></span>
3. <span data-ttu-id="aa9da-111">Установите серверные компоненты MBAM 2,5 SP1 RTM.</span><span class="sxs-lookup"><span data-stu-id="aa9da-111">Install MBAM 2.5 SP1 RTM server components.</span></span>
4. <span data-ttu-id="aa9da-112">Установка последнего исправления для MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="aa9da-112">Install lastest MBAM 2.5 SP1 hotfix rollup.</span></span>
5. <span data-ttu-id="aa9da-113">Настройка функций MBAM с помощью конфигуратора MBAM сервера.</span><span class="sxs-lookup"><span data-stu-id="aa9da-113">Configure MBAM features using MBAM Server Configurator.</span></span>

#### <span data-ttu-id="aa9da-114">Инструкции по установке нового исправления сервера MBAM 2,5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="aa9da-114">Steps to install the new MBAM 2.5 SP1 server hotfix</span></span>
<span data-ttu-id="aa9da-115">Ознакомьтесь с документом для [установки новой версии сервера](deploying-the-mbam-25-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="aa9da-115">Refer to the document for [new server installation](deploying-the-mbam-25-server-infrastructure.md).</span></span>
