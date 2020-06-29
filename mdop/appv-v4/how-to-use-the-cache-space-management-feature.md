---
title: Использование функции управления размером кэша
description: Использование функции управления размером кэша
author: dansimp
ms.assetid: 60965660-c015-46a8-88ac-54cbc050fe33
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fcb9cc4bc076e1acf52fb1c03797384c45b82f7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816409"
---
# <span data-ttu-id="6fd2c-103">Использование функции управления размером кэша</span><span class="sxs-lookup"><span data-stu-id="6fd2c-103">How to Use the Cache Space Management Feature</span></span>


<span data-ttu-id="6fd2c-104">Функция управления пространством кэша файловой системы использует по крайней мере Последнее использование алгоритма (LRU) и включается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-104">The FileSystem cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="6fd2c-105">Если пространство, требуемое для нового пакета, превысит доступное свободное пространство в кэше, клиент Application Virtualization (App-V) использует эту функцию, чтобы определить, какие из существующих пакетов могут удалять из кэша, чтобы освободить место для нового пакета.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-105">If the space that is required for a new package would exceed the available free space in the cache, the Application Virtualization (App-V) Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="6fd2c-106">Клиент удаляет пакет с самой ранней датой последнего доступа, если он старше значения, указанного в параметре реестра MinPkgAge.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-106">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="6fd2c-107">Использование функции управления пространством кэша FileSystem также поможет избежать проблем с кэшем кэша.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-107">Use of the FileSystem cache space management feature can also help to avoid low cache space problems.</span></span>

<span data-ttu-id="6fd2c-108">При необходимости в них удаляется несколько пакетов.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-108">More than one package is deleted if necessary.</span></span> <span data-ttu-id="6fd2c-109">Заблокированные пакеты не удаляются.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-109">Packages that are locked are not deleted.</span></span>

<span data-ttu-id="6fd2c-110">**Примечание**  Чтобы убедиться в том, что в кэше достаточно места для всех пакетов, которые могут быть развернуты, используйте параметр " **использовать порог свободного места на диске** " при настройке клиента, чтобы при необходимости кэш мог расти.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-110">**Note** To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="6fd2c-111">Кроме того, вы можете заранее определить, сколько места на диске требуется для кэша App-V, и в процессе установки задать размер кэша соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-111">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span>

 

<span data-ttu-id="6fd2c-112">Функция управления пространством кэша управляется значением реестра UnloadLeastRecentlyUsed.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-112">The cache space management feature is controlled by the UnloadLeastRecentlyUsed registry value.</span></span> <span data-ttu-id="6fd2c-113">Значение 1 включает функцию, а значение 0 (ноль) — отключает ее.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-113">A value of 1 enables the feature, and a value of 0 (zero) disables it.</span></span>

**<span data-ttu-id="6fd2c-114">Включение и отключение функции управления пространством кэша</span><span class="sxs-lookup"><span data-stu-id="6fd2c-114">To enable or disable the cache space management feature</span></span>**

-   <span data-ttu-id="6fd2c-115">Задайте для следующего значения реестра значение 1, чтобы включить алгоритм LRU.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-115">Set the following registry value to 1 to enable the LRU algorithm.</span></span> <span data-ttu-id="6fd2c-116">Установите для него значение 0 (нуль), чтобы отключить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-116">Set it to 0 (zero) to disable the feature.</span></span>

    <span data-ttu-id="6fd2c-117">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed</span><span class="sxs-lookup"><span data-stu-id="6fd2c-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed</span></span>

**<span data-ttu-id="6fd2c-118">Управление пакетами, которые могут быть удалены</span><span class="sxs-lookup"><span data-stu-id="6fd2c-118">To control which packages can be discarded</span></span>**

-   <span data-ttu-id="6fd2c-119">Чтобы определить, когда можно выбрать пакет для удаления, задайте для следующего значения реестра значение, равное минимальному количеству дней, которое вы хотите пропройти с момента последнего доступа к пакету.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-119">To determine when the package can be selected for discard, set the following registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="6fd2c-120">Пакеты, которые использовались в последнее время, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-120">Packages that have been used more recently are not discarded.</span></span>

    <span data-ttu-id="6fd2c-121">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge</span><span class="sxs-lookup"><span data-stu-id="6fd2c-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge</span></span>

    <span data-ttu-id="6fd2c-122">**Внимание!**  Максимальное значение для этого раздела реестра — 0x00011111.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-122">**Caution** The maximum value for this registry key is 0x00011111.</span></span> <span data-ttu-id="6fd2c-123">Большие значения будут препятствовать правильной работе функции управления пространством кэша.</span><span class="sxs-lookup"><span data-stu-id="6fd2c-123">Larger values will prevent the correct operation of the cache space management feature.</span></span>

     

## <span data-ttu-id="6fd2c-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="6fd2c-124">Related topics</span></span>


[<span data-ttu-id="6fd2c-125">Настройка параметров реестра клиента App-V с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="6fd2c-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





