---
title: Сброс параметров кэша файловой системы
description: Сброс параметров кэша файловой системы
author: dansimp
ms.assetid: 7777259d-8c21-4c06-9384-9599b69f9828
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 680634d98f8aac048af605c62029a0ee6b20af03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816712"
---
# <span data-ttu-id="fc09f-103">Сброс параметров кэша файловой системы</span><span class="sxs-lookup"><span data-stu-id="fc09f-103">How to Reset the FileSystem Cache</span></span>


<span data-ttu-id="fc09f-104">Сброс кэша файловой системы не так, как обычно требуется.</span><span class="sxs-lookup"><span data-stu-id="fc09f-104">Resetting the FileSystem cache is not something that should usually be necessary.</span></span> <span data-ttu-id="fc09f-105">Тем не менее, если вам нужно полностью сбросить кэш файловой системы, например для устранения неполадок, вы можете использовать описанную ниже процедуру.</span><span class="sxs-lookup"><span data-stu-id="fc09f-105">However if you need to completely reset the FileSystem cache, perhaps for troubleshooting purposes, you can use the following procedure.</span></span> <span data-ttu-id="fc09f-106">Для выполнения этого действия требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="fc09f-106">Administrative rights are required to perform this action.</span></span>

**<span data-ttu-id="fc09f-107">Сброс кэша файловой системы</span><span class="sxs-lookup"><span data-stu-id="fc09f-107">To reset the FileSystem cache</span></span>**

1.  <span data-ttu-id="fc09f-108">Задайте для следующего значения реестра значение 0 (ноль):</span><span class="sxs-lookup"><span data-stu-id="fc09f-108">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="fc09f-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span><span class="sxs-lookup"><span data-stu-id="fc09f-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="fc09f-110">Перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="fc09f-110">Restart the computer.</span></span>

## <span data-ttu-id="fc09f-111">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="fc09f-111">Related topics</span></span>


[<span data-ttu-id="fc09f-112">Настройка параметров реестра клиента App-V с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="fc09f-112">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





