---
title: Диалоговое окно "Запуск Защитника" (App-V 4.6 с пакетом обновления 1 (SP1))
description: Диалоговое окно "Запуск Защитника" (App-V 4.6 с пакетом обновления 1 (SP1))
author: dansimp
ms.assetid: 716ec7f9-ddad-45dd-a3c7-4a9d81cfcfd0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e33d48c089d7bf903c65da804e6cf5aa1bd2065
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821772"
---
# <span data-ttu-id="5a1a6-103">Диалоговое окно "Запуск Защитника" (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="5a1a6-103">Defender Running Dialog Box (App-V 4.6 SP1)</span></span>


<span data-ttu-id="5a1a6-104">Запущен защитник Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5a1a6-104">Microsoft Windows Defender is running.</span></span> <span data-ttu-id="5a1a6-105">Прежде чем продолжить установку, необходимо остановить работу защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="5a1a6-105">You should stop Windows Defender before continuing with the installation.</span></span> <span data-ttu-id="5a1a6-106">Защитник Windows может взаимодействовать с созданием пакета путем доступа к файлам, которые должны быть добавлены в виртуальный пакет приложения, или путем добавления лишних данных в виртуальный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="5a1a6-106">Windows Defender can interfere with creation of a package by accessing files that must be added to the virtual application package or by adding extraneous data to the virtual application package.</span></span>

<span data-ttu-id="5a1a6-107">Чтобы остановить выполнение защитника Microsoft Windows во время виртуализации, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5a1a6-107">Use the following procedure to stop Microsoft Windows Defender from running during sequencing.</span></span>

1.  <span data-ttu-id="5a1a6-108">На компьютере, на котором запущен секвенсор App-V, нажмите кнопку **Пуск**, щелкните правой кнопкой мыши пункт **компьютер**, а затем выберите пункт **Управление**.</span><span class="sxs-lookup"><span data-stu-id="5a1a6-108">On the computer running the App-V Sequencer, click **Start**, right-click **Computer**, and then click **Manage**.</span></span>

2.  <span data-ttu-id="5a1a6-109">В консоли **Управление компьютером** дважды щелкните элемент **службы и приложения**, а затем дважды щелкните элемент **службы** , чтобы развернуть **оснастку "службы"**.</span><span class="sxs-lookup"><span data-stu-id="5a1a6-109">In the **Computer Management** console, double click **Services and Applications**, and then double-click **Services** to expand **Services**.</span></span>

3.  <span data-ttu-id="5a1a6-110">Найдите его в списке.</span><span class="sxs-lookup"><span data-stu-id="5a1a6-110">Locate it in the list.</span></span> <span data-ttu-id="5a1a6-111">Щелкните правой кнопкой мыши защитник Windows, выберите команду **остановить** , чтобы остановить защитник Microsoft Windows, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5a1a6-111">Right-click Windows Defender, click **Stop** to stop Microsoft Windows Defender, and then click **Ok**.</span></span>

## <span data-ttu-id="5a1a6-112">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5a1a6-112">Related topics</span></span>


[<span data-ttu-id="5a1a6-113">Диалоговые окна (AppV 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="5a1a6-113">Dialog Boxes (AppV 4.6 SP1)</span></span>](dialog-boxes--appv-46-sp1-.md)

 

 





