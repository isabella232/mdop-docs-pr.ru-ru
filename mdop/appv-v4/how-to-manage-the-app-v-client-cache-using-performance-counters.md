---
title: Управление кэшем клиента App-V с помощью счетчиков производительности
description: Управление кэшем клиента App-V с помощью счетчиков производительности
author: dansimp
ms.assetid: 49d6c3f2-68b8-4c69-befa-7598a8737d05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 396cceaf9a3bde661200be2771a85596a512732f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817132"
---
# <span data-ttu-id="7e6dd-103">Управление кэшем клиента App-V с помощью счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="7e6dd-103">How to Manage the App-V Client Cache Using Performance Counters</span></span>


<span data-ttu-id="7e6dd-104">Вы можете использовать описанную ниже процедуру, чтобы определить, сколько свободного места доступно в кэше клиента Application Virtualization (App-V), с помощью системного монитора для графического отображения данных.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-104">You can use the following procedure to determine how much free space is available in the Application Virtualization (App-V) client cache by using Performance Monitor to display the information graphically.</span></span> <span data-ttu-id="7e6dd-105">Эти данные записываются на клиентском компьютере счетчиком производительности с именем "кэш клиента приложения virt" и включают следующие счетчики: "размер кэша (МБ)", "кэш свободного места (МБ)," и "% свободного места".</span><span class="sxs-lookup"><span data-stu-id="7e6dd-105">This information is captured on the client computer by a performance counter called “App Virt Client Cache,” and it includes the following counters: “Cache size (MB),” “Cache free space (MB),” and “% free space.”</span></span>

**<span data-ttu-id="7e6dd-106">Определение использования пространства кэша в клиенте</span><span class="sxs-lookup"><span data-stu-id="7e6dd-106">To determine client cache space usage</span></span>**

1.  <span data-ttu-id="7e6dd-107">Откройте командную команду как администратор или выберите **Пуск**, **выполнить**, введите **perfmon.exe**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-107">Open a command prompt as administrator, or click **Start**, **Run**, type **perfmon.exe**, and click **OK**.</span></span>

2.  <span data-ttu-id="7e6dd-108">В зависимости от используемой операционной системы Windows щелкните значок системный монитор или средство системного монитора после того, как откроется окно MMC.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-108">Depending on the Windows operating system being used, click the Performance Monitor or System Monitor tool after the MMC window opens.</span></span>

3.  <span data-ttu-id="7e6dd-109">Чтобы добавить счетчики, щелкните правой кнопкой мыши область диаграммы и выберите команду **Добавить счетчики**.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-109">To add counters, right-click the graph area and select **Add Counters**.</span></span>

4.  <span data-ttu-id="7e6dd-110">Щелкните раскрывающийся список, чтобы просмотреть перечень доступных счетчиков, прокрутите страницу и выберите в нем три счетчика, чтобы найти **virt клиентский кэш приложения**.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-110">Click the drop-down to display the list of available counters, scroll to find **App Virt Client Cache**, and then add the three counters.</span></span>

    <span data-ttu-id="7e6dd-111">**Важно!**  Счетчики производительности App-V реализованы в 32-разрядной библиотеке DLL, поэтому для ее просмотра необходимо использовать следующую команду для запуска 32-разрядной версии системного монитора: **MMC/32 Perfmon. msc**.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-111">**Important** The App-V performance counters are implemented in a 32-bit DLL, so to see them, you must use the following command to start the 32-bit version of Performance Monitor: **mmc /32 perfmon.msc**.</span></span> <span data-ttu-id="7e6dd-112">Эту команду необходимо запускать непосредственно на компьютере, который отслеживается, и не может использоваться для наблюдения за удаленным компьютером под управлением 64-разрядной операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-112">This command must be run directly on the computer being monitored and cannot be used to monitor a remote computer running a 64-bit operating system.</span></span>

     

## <span data-ttu-id="7e6dd-113">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7e6dd-113">Related topics</span></span>


[<span data-ttu-id="7e6dd-114">Управление виртуальными приложениями с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="7e6dd-114">How to Manage Virtual Applications by Using the Command Line</span></span>](how-to-manage-virtual-applications-by-using-the-command-line.md)

 

 





