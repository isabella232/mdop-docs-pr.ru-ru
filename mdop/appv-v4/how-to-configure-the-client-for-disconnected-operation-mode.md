---
title: Настройка клиента для включения режима изолированной работы
description: Настройка клиента для включения режима изолированной работы
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817819"
---
# <span data-ttu-id="5e1a1-103">Настройка клиента для включения режима изолированной работы</span><span class="sxs-lookup"><span data-stu-id="5e1a1-103">How to Configure the Client for Disconnected Operation Mode</span></span>


<span data-ttu-id="5e1a1-104">Режим разъединенных операций включает клиентское приложение Application Virtualization (App-V) или клиент Application Virtualization (App-V) для служб удаленных рабочих столов (ранее — служб терминалов) для запуска приложений, которые хранятся в кэше файловой системы клиента, когда клиент не может подключиться к серверу управления App-V.</span><span class="sxs-lookup"><span data-stu-id="5e1a1-104">The disconnected operation mode enables the Application Virtualization (App-V) Desktop Client or the Application Virtualization (App-V) Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client cannot connect to the App-V Management Server.</span></span>

<span data-ttu-id="5e1a1-105">**Важно!**  В крупной организации, где несколько серверов сеансов удаленных рабочих столов (на которых раньше настольных серверов) подключены к ферме для поддержки множества пользователей, использование единого сервера управления App-V для поддержки фермы представляет единственную точку сбоя.</span><span class="sxs-lookup"><span data-stu-id="5e1a1-105">**Important** In a large organization where multiple Remote Desktop Session Host (RD°Session Host) servers (formerly Terminal Servers) are linked in a farm to support many users, using a single App-V Management Server to support the farm represents a single point of failure.</span></span> <span data-ttu-id="5e1a1-106">Для обеспечения высокого уровня доступности для поддержки фермы узла RDSession рассматривайте возможность связывания двух или более серверов управления App-V для использования одной базы данных.</span><span class="sxs-lookup"><span data-stu-id="5e1a1-106">To provide high availability to support the RDSession Host farm, consider linking two or more App-V Management Servers to use the same database.</span></span>

 

**<span data-ttu-id="5e1a1-107">Включение режима разъединенных операций</span><span class="sxs-lookup"><span data-stu-id="5e1a1-107">To enable disconnected operation mode</span></span>**

-   <span data-ttu-id="5e1a1-108">Установите для следующего раздела реестра значение 1, чтобы включить режим разъединенных операций:</span><span class="sxs-lookup"><span data-stu-id="5e1a1-108">Set the following registry key value equal to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="5e1a1-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="5e1a1-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

**<span data-ttu-id="5e1a1-110">Чтобы установить ограничение по времени в режиме отключенной операции, используйте</span><span class="sxs-lookup"><span data-stu-id="5e1a1-110">To set a time limit on disconnected operation mode use</span></span>**

1.  <span data-ttu-id="5e1a1-111">Задайте для следующего раздела реестра значение 1:</span><span class="sxs-lookup"><span data-stu-id="5e1a1-111">Set the following registry key value to 1:</span></span>

    <span data-ttu-id="5e1a1-112">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="5e1a1-112">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

2.  <span data-ttu-id="5e1a1-113">Задайте для значения в следующем разделе реестра количество минут, в течение которых вы хотите ограничить режим автономной работы.</span><span class="sxs-lookup"><span data-stu-id="5e1a1-113">Set the following registry key value to the number of minutes you want to limit disconnected operation mode.</span></span> <span data-ttu-id="5e1a1-114">Допустимый диапазон значений: 1 – 999999.</span><span class="sxs-lookup"><span data-stu-id="5e1a1-114">The valid range of values is 1–999999.</span></span> <span data-ttu-id="5e1a1-115">Значение по умолчанию — 90 дней или 129 600 минут.</span><span class="sxs-lookup"><span data-stu-id="5e1a1-115">The default value is 90 days or 129,600 minutes.</span></span>

    <span data-ttu-id="5e1a1-116">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="5e1a1-116">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span></span>

**<span data-ttu-id="5e1a1-117">Настройка клиента для служб удаленных рабочих столов для отключения режима работы</span><span class="sxs-lookup"><span data-stu-id="5e1a1-117">To configure the Client for Remote Desktop Services for disconnected operation mode</span></span>**

1.  <span data-ttu-id="5e1a1-118">Установите для следующего раздела реестра значение 1, чтобы включить режим отключенной работы.</span><span class="sxs-lookup"><span data-stu-id="5e1a1-118">Set the following registry key value to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="5e1a1-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="5e1a1-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

2.  <span data-ttu-id="5e1a1-120">Установите для следующего параметра реестра значение 0 (ноль), чтобы разрешить неограниченный режим работы отключенной операции:</span><span class="sxs-lookup"><span data-stu-id="5e1a1-120">Set the following registry key value to 0 (zero) to allow unlimited use of disconnected operation mode:</span></span>

    <span data-ttu-id="5e1a1-121">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="5e1a1-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

3.  <span data-ttu-id="5e1a1-122">Убедитесь, что все пакеты предварительно загружены в кэш для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="5e1a1-122">Ensure that all packages are preloaded into the cache to improve performance.</span></span>

## <span data-ttu-id="5e1a1-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5e1a1-123">Related topics</span></span>


[<span data-ttu-id="5e1a1-124">Режим изолированной работы</span><span class="sxs-lookup"><span data-stu-id="5e1a1-124">Disconnected Operation Mode</span></span>](disconnected-operation-mode.md)

[<span data-ttu-id="5e1a1-125">Настройка параметров реестра клиента App-V с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="5e1a1-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





