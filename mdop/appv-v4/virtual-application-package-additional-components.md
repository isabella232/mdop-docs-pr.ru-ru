---
title: Дополнительные компоненты пакета виртуального приложения
description: Дополнительные компоненты пакета виртуального приложения
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815079"
---
# <span data-ttu-id="63398-103">Дополнительные компоненты пакета виртуального приложения</span><span class="sxs-lookup"><span data-stu-id="63398-103">Virtual Application Package Additional Components</span></span>


<span data-ttu-id="63398-104">Программа Sequencer App-V обнаружила каталог, который содержит 64-разрядные и 32-разрядные исполняемые файлы и (или DLL), которые зависят от того, на какой стороне параллельной сборки.</span><span class="sxs-lookup"><span data-stu-id="63398-104">The App-V Sequencer has detected a directory that contains 64-bit and 32-bit executables and/or dynamic-link library (.dll) files that depend on the same side-by-side assembly.</span></span> <span data-ttu-id="63398-105">Обычно секвенсор создает частные параллельные сборки для всех общедоступных сборок, которые используются в пакете. Однако невозможно создать 32-разрядные и 64-разрядные версии закрытых сборок в одном и том же каталоге.</span><span class="sxs-lookup"><span data-stu-id="63398-105">Typically, the Sequencer creates private side-by-side assemblies for all public assemblies that are used by the package; however, it is not possible to create 32-bit and 64-bit versions of the private assemblies in the same directory.</span></span>

<span data-ttu-id="63398-106">Если секвенсор обнаруживает один конфликт, выполняются следующие действия:</span><span class="sxs-lookup"><span data-stu-id="63398-106">If the Sequencer detects a single conflict, it will perform the following actions:</span></span>

-   <span data-ttu-id="63398-107">Удалите все существующие закрытые сборки 64-bit из всего пакета, независимо от того, есть ли у него конфликт между каталогами.</span><span class="sxs-lookup"><span data-stu-id="63398-107">Remove all of the existing 64-bit private assemblies in the entire package, whether or not the directory has a conflict.</span></span>

-   <span data-ttu-id="63398-108">Создавайте только 32-разрядные версии частных параллельных сборок.</span><span class="sxs-lookup"><span data-stu-id="63398-108">Create only 32-bit versions of the private side-by-side assemblies.</span></span>

<span data-ttu-id="63398-109">Вы должны самостоятельно устанавливать общедоступные версии всех необходимых сборок 64-bit на компьютере, на котором запущены программы Sequencer и на всех клиентских компьютерах App-V.</span><span class="sxs-lookup"><span data-stu-id="63398-109">You should natively install public versions of all the required 64-bit assemblies on the computer running the Sequencer and on all App-V client computers.</span></span>

<span data-ttu-id="63398-110">Чтобы найти необходимые существующие общедоступные сборки, откройте каталог, в котором хранится пакет, и просмотрите папку **VFS** .</span><span class="sxs-lookup"><span data-stu-id="63398-110">To locate the required existing public assemblies, open the directory where the package is saved and look in the **VFS** folder.</span></span> <span data-ttu-id="63398-111">Например, если корневой каталог пакета **Q:\\MyApp**, то при последовательном выполнении приложения просмотрите **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** и найдите все существующие общедоступные сборки.</span><span class="sxs-lookup"><span data-stu-id="63398-111">For example, if the package root is **Q:\\MyApp**, when you sequence the application, look in **Q:\\MyApp\\VFS\\CSIDL\_Windows\\WinSxS\\Manifests** and locate all of the existing public assemblies.</span></span> <span data-ttu-id="63398-112">64-разрядные версии этих файлов всегда начинаются со следующего текста в начале имени манифеста: **AMD64...**.</span><span class="sxs-lookup"><span data-stu-id="63398-112">The 64-bit versions of these files will always start with the following text at the beginning of the manifest name: **amd64…**.</span></span> <span data-ttu-id="63398-113">Точное имя и версия сборки можно найти в соответствующем файле манифеста.</span><span class="sxs-lookup"><span data-stu-id="63398-113">The exact name and version of the assembly can be found in the associated manifest file.</span></span>

<span data-ttu-id="63398-114">Чтобы скачать и установить правильную версию необходимых компонентов, воспользуйтесь одной из приведенных ниже ссылок.</span><span class="sxs-lookup"><span data-stu-id="63398-114">Use any of the following links to download and install the correct version of the required prerequisites:</span></span>

-   [<span data-ttu-id="63398-115">Распространяемый пакет Microsoft Visual C++ 2005 (x64)</span><span class="sxs-lookup"><span data-stu-id="63398-115">Microsoft Visual C++ 2005 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [<span data-ttu-id="63398-116">Распространяемый пакет Microsoft Visual C++ 2005 с пакетом обновления 1 (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="63398-116">Microsoft Visual C++ 2005 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [<span data-ttu-id="63398-117">Распространяемый пакет Microsoft Visual C++ 2008 (x64)</span><span class="sxs-lookup"><span data-stu-id="63398-117">Microsoft Visual C++ 2008 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [<span data-ttu-id="63398-118">Распространяемый пакет Microsoft Visual C++ 2008 с пакетом обновления 1 (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="63398-118">Microsoft Visual C++ 2008 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





