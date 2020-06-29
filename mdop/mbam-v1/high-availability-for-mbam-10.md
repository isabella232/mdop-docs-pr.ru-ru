---
title: Высокая доступность для MBAM 1.0
description: Высокая доступность для MBAM 1.0
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825362"
---
# <span data-ttu-id="a07ee-103">Высокая доступность для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a07ee-103">High Availability for MBAM 1.0</span></span>


<span data-ttu-id="a07ee-104">В этой статье описано, как настроить высокодоступную установку администрирования и мониторинга Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="a07ee-104">This topic describes how to configure a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

## <span data-ttu-id="a07ee-105">Сценарии высокой доступности для MBAM</span><span class="sxs-lookup"><span data-stu-id="a07ee-105">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="a07ee-106">Средства администрирования и наблюдения Microsoft BitLocker (MBAM) предназначены для обеспечения отказоустойчивости.</span><span class="sxs-lookup"><span data-stu-id="a07ee-106">Microsoft BitLocker Administration and Monitoring (MBAM) is designed to be fault-tolerant.</span></span> <span data-ttu-id="a07ee-107">Если сервер становится недоступен, пользователи не должны иметь негативных изменений.</span><span class="sxs-lookup"><span data-stu-id="a07ee-107">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="a07ee-108">Например, если агент MBAM не может подключиться к веб-серверу MBAM, пользователи не должны получать запрос на ввод действия.</span><span class="sxs-lookup"><span data-stu-id="a07ee-108">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="a07ee-109">При планировании установки MBAM учитывайте следующие проблемы, которые могут повлиять на доступность службы MBAM:</span><span class="sxs-lookup"><span data-stu-id="a07ee-109">When you plan your MBAM installation, consider the following concerns that can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="a07ee-110">Шифрование диска и пароль восстановления — если пароль восстановления не может быть установлен, шифрование не запускается на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="a07ee-110">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption will not start on the client computer.</span></span>

-   <span data-ttu-id="a07ee-111">Состояние соответствия требованиям: Если сервер, на котором размещается служба отчетов о состоянии соответствия требованиям, недоступен, данные соответствия не будут актуальными.</span><span class="sxs-lookup"><span data-stu-id="a07ee-111">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data will not remain current.</span></span>

-   <span data-ttu-id="a07ee-112">Справка по ключу восстановления службы поддержки. Если службе поддержки не удается получить доступ к сведениям о базе данных MBAM, они не смогут предоставлять пользователям ключи восстановления.</span><span class="sxs-lookup"><span data-stu-id="a07ee-112">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, they will be unable to provide recovery keys to users.</span></span>

-   <span data-ttu-id="a07ee-113">Доступность отчетов — отчеты будут недоступны, если сервер, на котором размещаются отчеты о соответствии и аудите, недоступен.</span><span class="sxs-lookup"><span data-stu-id="a07ee-113">Availability of reports – Reports will not be available if the server that hosts the Compliance and Audit Reports is not available.</span></span>

<span data-ttu-id="a07ee-114">Основной проблемой для MBAM высокой доступности является доступность восстановления ключей BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a07ee-114">The main concern for MBAM high availability is BitLocker key recovery availability.</span></span> <span data-ttu-id="a07ee-115">Если службе поддержки не удается предоставить доступ к ключам восстановления, пользователи, которым не удается разблокировать компьютеры.</span><span class="sxs-lookup"><span data-stu-id="a07ee-115">If the help desk cannot provide recovery keys, users who are locked out cannot unlock their computers.</span></span> <span data-ttu-id="a07ee-116">Чтобы избежать этой проблемы, рекомендуется реализовать избыточные веб-серверы и базы данных для обеспечения высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="a07ee-116">To avoid this problem, consider implementing redundant web servers and databases to ensure high availability.</span></span>

<span data-ttu-id="a07ee-117">Более подробную информацию о масштабируемости MBAM и высокой доступности можно найти в [статье технический документ MBAM масштабируемость](https://go.microsoft.com/fwlink/p/?LinkId=229025) ( https://go.microsoft.com/fwlink/p/?LinkId=229025) .</span><span class="sxs-lookup"><span data-stu-id="a07ee-117">For more information about MBAM scalability and high availability, see the [MBAM Scalability White Paper](https://go.microsoft.com/fwlink/p/?LinkId=229025) (https://go.microsoft.com/fwlink/p/?LinkId=229025).</span></span>

<span data-ttu-id="a07ee-118">Общие рекомендации по обеспечению высокой доступности Microsoft SQL Server см. в разделе [Высокая доступность](https://go.microsoft.com/fwlink/p/?LinkId=221504) ( https://go.microsoft.com/fwlink/p/?LinkId=221504) .</span><span class="sxs-lookup"><span data-stu-id="a07ee-118">For general guidance on high availability for Microsoft SQL Server, see [High Availability](https://go.microsoft.com/fwlink/p/?LinkId=221504) (https://go.microsoft.com/fwlink/p/?LinkId=221504).</span></span>

<span data-ttu-id="a07ee-119">Общие рекомендации по обеспечению доступности и масштабируемости для веб-серверов приведены в статье [доступность и масштабируемость](https://go.microsoft.com/fwlink/p/?LinkId=221503) ( https://go.microsoft.com/fwlink/p/?LinkId=221503) .</span><span class="sxs-lookup"><span data-stu-id="a07ee-119">For general guidance on availability and scalability for web servers, see [Availability and Scalability](https://go.microsoft.com/fwlink/p/?LinkId=221503) (https://go.microsoft.com/fwlink/p/?LinkId=221503).</span></span>

## <span data-ttu-id="a07ee-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a07ee-120">Related topics</span></span>


[<span data-ttu-id="a07ee-121">Обслуживание MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a07ee-121">Maintaining MBAM 1.0</span></span>](maintaining-mbam-10.md)

 

 





