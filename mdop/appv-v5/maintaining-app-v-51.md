---
title: Обслуживание App-V 5.1
description: Обслуживание App-V 5.1
author: dansimp
ms.assetid: 5abd17d3-e8af-4261-b914-741ae116b0e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 431ad65507a5699358159c73eaf9f3cf0dee33b7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813613"
---
# <span data-ttu-id="20053-103">Обслуживание App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="20053-103">Maintaining App-V 5.1</span></span>


<span data-ttu-id="20053-104">После того как вы закончите все необходимое планирование, а затем развернуть App-V 5,1, вы можете использовать следующие сведения для поддержки инфраструктуры App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="20053-104">After you have completed all the necessary planning, and then deployment of App-V 5.1, you can use the following information to maintain the App-V 5.1 infrastructure.</span></span>

## <a href="" id="move-the-app-v-5-1-server-"></a><span data-ttu-id="20053-105">Перемещение сервера App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="20053-105">Move the App-V 5.1 Server</span></span>


<span data-ttu-id="20053-106">Сервер App-V 5,1 подключается к базе данных App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="20053-106">The App-V 5.1 server connects to the App-V 5.1 database.</span></span> <span data-ttu-id="20053-107">Следовательно, вы можете установить компонент управления на любой компьютер в сети, а затем подключить его к базе данных App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="20053-107">Therefore you can install the management component to any computer on the network and then connect it to the App-V 5.1 database.</span></span>

[<span data-ttu-id="20053-108">Перенос сервера App-V на другой компьютер</span><span class="sxs-lookup"><span data-stu-id="20053-108">How to Move the App-V Server to Another Computer</span></span>](how-to-move-the-app-v-server-to-another-computer51.md)

## <a href="" id="determine-if-an-app-v-5-1-application-is-running-virtualized-"></a><span data-ttu-id="20053-109">Определение того, запущено ли приложение App-V 5,1 виртуализировано</span><span class="sxs-lookup"><span data-stu-id="20053-109">Determine if an App-V 5.1 Application is Running Virtualized</span></span>


<span data-ttu-id="20053-110">Независимые поставщики программного обеспечения, которые хотят определить, выполняется ли виртуализация приложения с помощью App-V 5,1 или более поздней версии, должен открыть именованный объект с именем \*\*AppVVirtual- &lt; PID &gt; \*\* в пространстве имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20053-110">Independent software vendors (ISV) who want to determine if an application is running virtualized with App-V 5.1 or above, should open a named object called **AppVVirtual-&lt;PID&gt;** in the default namespace.</span></span> <span data-ttu-id="20053-111">Например, можно использовать интерфейс Windows API **GetCurrentProcessId ()** для получения идентификатора текущего процесса, например 4052, а затем, если именованный объект события с именем **AppVVirtual-4052** может быть успешно открыт с помощью **OpenEvent ()** в пространстве имен по умолчанию для доступа к чтению, то приложение является виртуальным.</span><span class="sxs-lookup"><span data-stu-id="20053-111">For example, Windows API **GetCurrentProcessId()** can be used to obtain the current process's ID, for example 4052, and then if a named Event object called **AppVVirtual-4052** can be successfully opened using **OpenEvent()** in the default namespace for read access, then the application is virtual.</span></span> <span data-ttu-id="20053-112">Если происходит сбой вызова **OpenEvent ()** , приложение не является виртуальным.</span><span class="sxs-lookup"><span data-stu-id="20053-112">If the **OpenEvent()** call fails, the application is not virtual.</span></span>

<span data-ttu-id="20053-113">Кроме того, для тех, кто хочет явно виртуализировать или не виртуализировать вызовы для определенного API с помощью App-V 5,1 и более поздних версий, может использовать функции **VirtualizeCurrentThread ()** и **CurrentThreadIsVirtualized ()** , реализованные в модуле AppEntSubsystems32.dll.</span><span class="sxs-lookup"><span data-stu-id="20053-113">Additionally, ISV’s who want to explicitly virtualize or not virtualize calls on specific API’s with App-V 5.1 and above, can use the **VirtualizeCurrentThread()** and **CurrentThreadIsVirtualized()** functions implemented in the AppEntSubsystems32.dll module.</span></span> <span data-ttu-id="20053-114">Это позволяет подсказкам в нижестоящих компонентах, которые не должны быть виртуализированы при вызове.</span><span class="sxs-lookup"><span data-stu-id="20053-114">These provide a way of hinting at a downstream component that the call should or should not be virtualized.</span></span>






## <span data-ttu-id="20053-115">Другие ресурсы для обслуживания App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="20053-115">Other resources for maintaining App-V 5.1</span></span>


[<span data-ttu-id="20053-116">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="20053-116">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





