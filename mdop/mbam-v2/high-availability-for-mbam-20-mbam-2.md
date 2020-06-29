---
title: Высокая доступность для MBAM 2.0
description: Высокая доступность для MBAM 2.0
author: dansimp
ms.assetid: 244ee013-9e2a-48d2-b842-4e10594fd74f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6482a099d96aee731f81368b8b787325e592c453
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824729"
---
# <span data-ttu-id="a1966-103">Высокая доступность для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a1966-103">High Availability for MBAM 2.0</span></span>


<span data-ttu-id="a1966-104">В этом разделе приведены основные сведения о высокодоступной установке системы администрирования и мониторинга Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="a1966-104">This topic provides basic information about a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="a1966-105">Сценарии высокой доступности не полностью поддерживаются в этой версии MBAM, поэтому они не описаны здесь.</span><span class="sxs-lookup"><span data-stu-id="a1966-105">High-availability scenarios are not fully supported in this version of MBAM, so they are not described here.</span></span> <span data-ttu-id="a1966-106">Рекомендуется выполнять поиск в связанных блогах и форумах, где пользователи могут успешно настроить высокий уровень доступности для MBAM в своей среде.</span><span class="sxs-lookup"><span data-stu-id="a1966-106">It is recommended that you search related blogs and forums, where users describe how they have successfully configured high availability for MBAM in their environments.</span></span>

## <span data-ttu-id="a1966-107">Сценарии высокой доступности для MBAM</span><span class="sxs-lookup"><span data-stu-id="a1966-107">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="a1966-108">Администрирование и мониторинг Microsoft BitLocker разработаны для обеспечения отказоустойчивости.</span><span class="sxs-lookup"><span data-stu-id="a1966-108">Microsoft BitLocker Administration and Monitoring is designed to be fault-tolerant.</span></span> <span data-ttu-id="a1966-109">Если сервер становится недоступен, пользователи не должны иметь негативных изменений.</span><span class="sxs-lookup"><span data-stu-id="a1966-109">If a server becomes unavailable, users should not be negatively affected.</span></span> <span data-ttu-id="a1966-110">Например, если агент MBAM не может подключиться к веб-серверу MBAM, пользователи не должны получать запрос на ввод действия.</span><span class="sxs-lookup"><span data-stu-id="a1966-110">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="a1966-111">При планировании установки MBAM рассматривайте следующие элементы, которые могут повлиять на доступность службы MBAM:</span><span class="sxs-lookup"><span data-stu-id="a1966-111">When you plan your MBAM installation, consider the following items, which can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="a1966-112">Шифрование диска и пароль восстановления — если пароль восстановления не может быть условным, шифрование не запускается на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="a1966-112">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption does not start on the client computer.</span></span>

-   <span data-ttu-id="a1966-113">Состояние соответствия требованиям: Если сервер, на котором размещается служба отчетов о состоянии соответствия требованиям, недоступен, данные о соответствии соответствия не будут актуальными.</span><span class="sxs-lookup"><span data-stu-id="a1966-113">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data does not remain current.</span></span>

-   <span data-ttu-id="a1966-114">Справочная информация о ключе восстановления службы поддержки: Если службе поддержки не удается получить доступ к сведениям о базе данных MBAM, в справочной службе нельзя предоставить ключи восстановления пользователям.</span><span class="sxs-lookup"><span data-stu-id="a1966-114">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, the Help Desk cannot provide recovery keys to users.</span></span>

-   <span data-ttu-id="a1966-115">Доступность отчетов — если сервер, на котором размещаются отчеты о соответствии и аудите, недоступен, отчеты будут недоступны.</span><span class="sxs-lookup"><span data-stu-id="a1966-115">Availability of reports –If the server that hosts the Compliance and Audit Reports is not available, reports will not be available.</span></span>

## <a href="" id="how-the-mbam-backup-uses-the-volume-shadow-copy-service--vss--"></a><span data-ttu-id="a1966-116">Использование службы теневого копирования томов (VSS) в резервной копии MBAM</span><span class="sxs-lookup"><span data-stu-id="a1966-116">How the MBAM Backup Uses the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="a1966-117">MBAM 2.0 предоставляет средство записи теневого копирования тома (VSS), именуемое администратором Microsoft BitLocker и разработчиком управления, которое способствует созданию резервной копии базы данных соответствия требованиям и аудита и базы данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="a1966-117">MBAM2.0 provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer, which facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="a1966-118">Установщик Windows Server MBAM регистрирует модуль записи VSS MBAM.</span><span class="sxs-lookup"><span data-stu-id="a1966-118">The MBAM Server Windows Installer registers the MBAM VSS Writer.</span></span> <span data-ttu-id="a1966-119">Если при регистрации модуля записи VSS произошел сбой, то при установке сервера MBAM будет произведен откат.</span><span class="sxs-lookup"><span data-stu-id="a1966-119">Any failure during the VSS writer registration causes the MBAM Server installation to roll back.</span></span> <span data-ttu-id="a1966-120">В топологии, в которой база данных соответствия требованиям и базы и база данных для восстановления установлены на разных серверах, на каждом сервере регистрируется отдельный экземпляр MBAM Writer.</span><span class="sxs-lookup"><span data-stu-id="a1966-120">In a topology where the Compliance and Audit Database and the Recovery Database are installed on different servers, a separate instance of MBAM VSS Writer is registered on each server.</span></span> <span data-ttu-id="a1966-121">Модуль записи VSS MBAM зависит от модуля записи VSS SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a1966-121">The MBAM VSS Writer is dependent on the SQL Server VSS Writer.</span></span> <span data-ttu-id="a1966-122">Средство записи VSS SQL Server зарегистрировано как часть установки Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a1966-122">The SQL Server VSS Writer is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="a1966-123">Любая технология резервного копирования, использующая средства записи VSS для выполнения резервного копирования, может найти модуль записи VSS MBAM.</span><span class="sxs-lookup"><span data-stu-id="a1966-123">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS Writer.</span></span>

## <span data-ttu-id="a1966-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a1966-124">Related topics</span></span>


[<span data-ttu-id="a1966-125">Обслуживание MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a1966-125">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)

 

 





