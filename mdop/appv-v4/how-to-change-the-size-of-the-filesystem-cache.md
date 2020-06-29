---
title: Изменение размера кэша файловой системы
description: Изменение размера кэша файловой системы
author: dansimp
ms.assetid: 6ed17ba3-293b-4482-b3fa-31e5f606dad6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63c98d53ccb31e8eb64bc70d3d79b2198c506e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818002"
---
# <span data-ttu-id="a109d-103">Изменение размера кэша файловой системы</span><span class="sxs-lookup"><span data-stu-id="a109d-103">How to Change the Size of the FileSystem Cache</span></span>


<span data-ttu-id="a109d-104">Вы можете изменить размер кэша файловой системы, используя командную строку.</span><span class="sxs-lookup"><span data-stu-id="a109d-104">You can change the size of the FileSystem cache by using the command line.</span></span> <span data-ttu-id="a109d-105">Это действие требует полного сброса кэша и требует наличия прав администратора.</span><span class="sxs-lookup"><span data-stu-id="a109d-105">This action requires a complete reset of the cache, and it requires administrative rights.</span></span>

**<span data-ttu-id="a109d-106">Изменение размера кэша файловой системы</span><span class="sxs-lookup"><span data-stu-id="a109d-106">To change the size of the FileSystem cache</span></span>**

1.  <span data-ttu-id="a109d-107">Задайте для следующего значения реестра значение 0 (ноль):</span><span class="sxs-lookup"><span data-stu-id="a109d-107">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="a109d-108">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span><span class="sxs-lookup"><span data-stu-id="a109d-108">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="a109d-109">Задайте для следующего значения реестра максимальный размер кэша (в МЕГАБАЙТах), необходимый для удержания пакетов (например, 8192 МБ).</span><span class="sxs-lookup"><span data-stu-id="a109d-109">Set the following registry value to the maximum cache size, in MB, that is necessary to hold the packages—for example, 8192 MB:</span></span>

    <span data-ttu-id="a109d-110">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span><span class="sxs-lookup"><span data-stu-id="a109d-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span></span>

3.  <span data-ttu-id="a109d-111">Перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="a109d-111">Restart the computer.</span></span>

## <span data-ttu-id="a109d-112">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a109d-112">Related topics</span></span>


[<span data-ttu-id="a109d-113">Настройка параметров реестра клиента App-V с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="a109d-113">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





