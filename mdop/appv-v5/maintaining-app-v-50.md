---
title: Обслуживание App-V 5.0
description: Обслуживание App-V 5.0
author: dansimp
ms.assetid: 66851ec3-c674-493b-ad6d-db8fcbf1956c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3445bfe00ba7703a66fa3da2f9d7089990dd3854
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813616"
---
# <span data-ttu-id="e074e-103">Обслуживание App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="e074e-103">Maintaining App-V 5.0</span></span>


<span data-ttu-id="e074e-104">После того как вы закончите все необходимое планирование, а затем развернуть App-V 5,0, вы можете использовать следующие сведения для поддержки инфраструктуры App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e074e-104">After you have completed all the necessary planning, and then deployment of App-V 5.0, you can use the following information to maintain the App-V 5.0 infrastructure.</span></span>

## <a href="" id="move-the-app-v-5-0-server-"></a><span data-ttu-id="e074e-105">Перемещение сервера App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e074e-105">Move the App-V 5.0 Server</span></span>


<span data-ttu-id="e074e-106">Сервер App-V 5,0 подключается к базе данных App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e074e-106">The App-V 5.0 server connects to the App-V 5.0 database.</span></span> <span data-ttu-id="e074e-107">Следовательно, вы можете установить компонент управления на любой компьютер в сети, а затем подключить его к базе данных App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e074e-107">Therefore you can install the management component to any computer on the network and then connect it to the App-V 5.0 database.</span></span>

[<span data-ttu-id="e074e-108">Перенос сервера App-V на другой компьютер</span><span class="sxs-lookup"><span data-stu-id="e074e-108">How to Move the App-V Server to Another Computer</span></span>](how-to-move-the-app-v-server-to-another-computer.md)

## <a href="" id="determine-if-an-app-v-5-0-application-is-running-virtualized-"></a><span data-ttu-id="e074e-109">Определение того, запущено ли приложение App-V 5,0 виртуализировано</span><span class="sxs-lookup"><span data-stu-id="e074e-109">Determine if an App-V 5.0 Application is Running Virtualized</span></span>


<span data-ttu-id="e074e-110">Независимые поставщики программного обеспечения, которые хотят определить, выполняется ли виртуализация приложения с помощью App-V 5,0 или более поздней версии, должен открыть именованный объект с именем \*\*AppVVirtual- &lt; PID &gt; \*\* в пространстве имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e074e-110">Independent software vendors (ISV) who want to determine if an application is running virtualized with App-V 5.0 or above, should open a named object called **AppVVirtual-&lt;PID&gt;** in the default namespace.</span></span> <span data-ttu-id="e074e-111">Например, можно использовать интерфейс Windows API **GetCurrentProcessId ()** для получения идентификатора текущего процесса, например 4052, а затем, если именованный объект события с именем **AppVVirtual-4052** может быть успешно открыт с помощью **OpenEvent ()** в пространстве имен по умолчанию для доступа к чтению, то приложение является виртуальным.</span><span class="sxs-lookup"><span data-stu-id="e074e-111">For example, Windows API **GetCurrentProcessId()** can be used to obtain the current process's ID, for example 4052, and then if a named Event object called **AppVVirtual-4052** can be successfully opened using **OpenEvent()** in the default namespace for read access, then the application is virtual.</span></span> <span data-ttu-id="e074e-112">Если происходит сбой вызова **OpenEvent ()** , приложение не является виртуальным.</span><span class="sxs-lookup"><span data-stu-id="e074e-112">If the **OpenEvent()** call fails, the application is not virtual.</span></span>

<span data-ttu-id="e074e-113">Кроме того, для тех, кто хочет явно виртуализировать или не виртуализировать вызовы для определенного API с помощью App-V 5,0 и более поздних версий, может использовать функции **VirtualizeCurrentThread ()** и **CurrentThreadIsVirtualized ()** , реализованные в модуле AppEntSubsystems32.dll.</span><span class="sxs-lookup"><span data-stu-id="e074e-113">Additionally, ISV’s who want to explicitly virtualize or not virtualize calls on specific API’s with App-V 5.0 and above, can use the **VirtualizeCurrentThread()** and **CurrentThreadIsVirtualized()** functions implemented in the AppEntSubsystems32.dll module.</span></span> <span data-ttu-id="e074e-114">Это позволяет подсказкам в нижестоящих компонентах, которые не должны быть виртуализированы при вызове.</span><span class="sxs-lookup"><span data-stu-id="e074e-114">These provide a way of hinting at a downstream component that the call should or should not be virtualized.</span></span>






## <span data-ttu-id="e074e-115">Другие ресурсы для обслуживания App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e074e-115">Other resources for maintaining App-V 5.0</span></span>


[<span data-ttu-id="e074e-116">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="e074e-116">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





