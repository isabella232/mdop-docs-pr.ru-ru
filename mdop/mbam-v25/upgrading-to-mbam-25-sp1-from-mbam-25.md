---
title: Обновление до MBAM 2.5 с пакетом обновления 1 (SP1) с MBAM 2.5
description: Обновление до MBAM 2.5 с пакетом обновления 1 (SP1) с MBAM 2.5
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 19da3df0976b51700e0d10c302a31421a88d17e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812744"
---
# <span data-ttu-id="97412-103">Обновление до MBAM 2.5 с пакетом обновления 1 (SP1) с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="97412-103">Upgrading to MBAM 2.5 SP1 from MBAM 2.5</span></span>
<span data-ttu-id="97412-104">В этом разделе описывается процесс обновления 2,5 сервера администрирования и мониторинга Microsoft BitLocker (MBAM) и клиента MBAM из 2,5 в MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="97412-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 and the MBAM Client from 2.5 to MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="97412-105">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="97412-105">Before you begin</span></span>
#### <span data-ttu-id="97412-106">Загрузка выпуска для сопровождения 2019 мая</span><span class="sxs-lookup"><span data-stu-id="97412-106">Download the May 2019 servicing release</span></span>
[<span data-ttu-id="97412-107">Пакет оптимизации для классической версии</span><span class="sxs-lookup"><span data-stu-id="97412-107">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=58345)

#### <span data-ttu-id="97412-108">Проверка documentaion установки</span><span class="sxs-lookup"><span data-stu-id="97412-108">Verify the installation documentaion</span></span>
<span data-ttu-id="97412-109">Убедитесь в том, что у вас есть текущая документация по среде MBAM, в том числе все имена серверов, имена баз данных, учетные записи служб и их пароли.</span><span class="sxs-lookup"><span data-stu-id="97412-109">Verify you have a current documentation of your MBAM environment, including all server names, database names, service accounts and their passwords.</span></span>

### <span data-ttu-id="97412-110">Действия по обновлению</span><span class="sxs-lookup"><span data-stu-id="97412-110">Upgrade steps</span></span>
#### <span data-ttu-id="97412-111">Инструкции по обновлению базы данных MBAM (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="97412-111">Steps to upgrade the MBAM Database (SQL Server)</span></span>
1. <span data-ttu-id="97412-112">Использование конфигуратора MBAM; Удалите роль отчеты из SQL Server или в том месте, где размещена база данных SSRS.</span><span class="sxs-lookup"><span data-stu-id="97412-112">Using the MBAM Configurator; remove the Reports role from the SQL server, or wherever the SSRS database is hosted.</span></span> <span data-ttu-id="97412-113">В зависимости от используемой среды это может быть один и тот же сервер или отдельное приложение.</span><span class="sxs-lookup"><span data-stu-id="97412-113">Depending on your environment, this can be the same server or a separate one.</span></span>
  > [!NOTE]
  > <span data-ttu-id="97412-114">Вы не увидите параметр для удаления баз данных. это ожидается.</span><span class="sxs-lookup"><span data-stu-id="97412-114">You will not see an option to remove the Databases; this is expected.</span></span>  
2. <span data-ttu-id="97412-115">Установите пакет обновления 2,5 (SP1) (с веб-сайтом MDOP — пакет 2015 для настольных систем Майкрософт на сайте центра обслуживания корпоративных лицензий).</span><span class="sxs-lookup"><span data-stu-id="97412-115">Install 2.5 SP1(Located with MDOP - Microsoft Desktop Optimization Pack 2015 from the Volume Licensing Service Center site:</span></span>  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. <span data-ttu-id="97412-116">Не настраивать его в настоящее время</span><span class="sxs-lookup"><span data-stu-id="97412-116">Do not configure it at this time</span></span> 
4. <span data-ttu-id="97412-117">Использование конфигуратора MBAM; Повторное добавление роли "отчеты"</span><span class="sxs-lookup"><span data-stu-id="97412-117">Using the MBAM Configurator; re-add the Reports role</span></span>
5. <span data-ttu-id="97412-118">Использование конфигуратора MBAM; Повторное добавление роли базы данных SQL на сервере SQL Server</span><span class="sxs-lookup"><span data-stu-id="97412-118">Using the MBAM Configurator; re-add the SQL Database role on the SQL Server</span></span>
6. <span data-ttu-id="97412-119">В итоге вы будете предупреждать о том, что DBs уже существует и не создавались, но ожидается</span><span class="sxs-lookup"><span data-stu-id="97412-119">At the end, you will be warned that the DBs already exist and  weren’t created, but this is expected</span></span>
7. <span data-ttu-id="97412-120">Этот процесс обновляет существующие базы данных до установленной текущей версии.</span><span class="sxs-lookup"><span data-stu-id="97412-120">This process updates the existing databases to the current version being installed.</span></span>              

#### <span data-ttu-id="97412-121">Инструкции по обновлению сервера MBAM (на котором запущены MBAM и службы IIS)</span><span class="sxs-lookup"><span data-stu-id="97412-121">Steps to upgrade the MBAM Server (Running MBAM and IIS)</span></span>
1. <span data-ttu-id="97412-122">Использование конфигуратора MBAM; Удаление порталов для администраторов и самообслуживания на сервере IIS</span><span class="sxs-lookup"><span data-stu-id="97412-122">Using the MBAM Configurator; remove the Admin and Self Service Portals from  the IIS server</span></span>
2. <span data-ttu-id="97412-123">Установка MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="97412-123">Install MBAM 2.5 SP1</span></span>
3. <span data-ttu-id="97412-124">Не настраивать его в настоящее время</span><span class="sxs-lookup"><span data-stu-id="97412-124">Do not configure it at this time</span></span>  
4. <span data-ttu-id="97412-125">Использование конфигуратора MBAM; Повторное добавление порталов для администраторов и самообслуживания на сервер IIS</span><span class="sxs-lookup"><span data-stu-id="97412-125">Using the MBAM Configurator; re-add the Admin and Self Service Portals to the IIS server</span></span> 
5. <span data-ttu-id="97412-126">Откройте командную в командной строке с повышенными привилегиями, введите **iisreset**и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="97412-126">Open an elevated command prompt, type **IISRESET**, and hit Enter.</span></span>
 
#### <span data-ttu-id="97412-127">Инструкции по обновлению клиентов и конечных точек MBAM</span><span class="sxs-lookup"><span data-stu-id="97412-127">Steps to upgrade the MBAM Clients/Endpoints</span></span>
1. <span data-ttu-id="97412-128">Удаление агента 2,5 из конечных точек клиента</span><span class="sxs-lookup"><span data-stu-id="97412-128">Uninstall the 2.5 Agent from client endpoints</span></span>
2. <span data-ttu-id="97412-129">Установка агента 2,5 SP1 на конечных точках клиента</span><span class="sxs-lookup"><span data-stu-id="97412-129">Install the 2.5 SP1 Agent on the client endpoints</span></span>
3. <span data-ttu-id="97412-130">Обновление пакета обновления 2019 для клиентов, на котором запущен агент 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="97412-130">Push out the May 2019 Rollup Client update to clients running the 2.5 SP1 Agent</span></span> 
4. <span data-ttu-id="97412-131">Перед установкой накопительного пакета обновления 2019 может потребоваться удаление существующего клиента.</span><span class="sxs-lookup"><span data-stu-id="97412-131">There is no need to uninstall the existing client prior to installing the May 2019 Rollup.</span></span>  
