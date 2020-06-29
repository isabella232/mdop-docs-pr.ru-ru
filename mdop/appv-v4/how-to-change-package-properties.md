---
title: Изменение свойств пакета
description: Изменение свойств пакета
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818042"
---
# <span data-ttu-id="7aa2a-103">Изменение свойств пакета</span><span class="sxs-lookup"><span data-stu-id="7aa2a-103">How to Change Package Properties</span></span>


<span data-ttu-id="7aa2a-104">Вы можете использовать следующие процедуры для изменения имени пакета Application Virtualization и связанных с ним комментариев.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-104">You can use the following procedures to modify an Application Virtualization package name and its associated comments.</span></span>

<span data-ttu-id="7aa2a-105">Если пакет создается в первый раз, вы также можете изменить размер блока параметров упорядочивания, который определяет, как потоковый пакет приложения будет передается с сервера Application Virtualization на Настольный клиент виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-105">If this is the first time the package has been created, you can also change the sequencing parameter block size, which determines how a sequenced application package is streamed from an Application Virtualization Server to an Application Virtualization Desktop Client.</span></span>

<span data-ttu-id="7aa2a-106">**Примечание**  При выборе размера блока учитывайте размер SFT-файла и пропускной способности сети.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-106">**Note** When selecting a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="7aa2a-107">Файл с меньшим размером блока занимает больше времени, чем потоковая передача по сети, но это снижает нагрузку на пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-107">A file with a smaller block size takes longer to stream over the network, but it is less bandwidth intensive.</span></span> <span data-ttu-id="7aa2a-108">Файлы с более крупными размерами блоков могут работать быстрее, но они используют дополнительную пропускную способность сети.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-108">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="7aa2a-109">С помощью экспериментов вы можете найти оптимальный размер блока для потоковой передачи приложений в сети.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-109">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span>

 

<span data-ttu-id="7aa2a-110">Оставшаяся часть свойств пакета на вкладке **Свойства** автоматически создается и не может быть изменена на этой вкладке.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-110">The remainder of the package properties on the **Properties** tab is automatically generated and cannot be modified on this tab.</span></span>

**<span data-ttu-id="7aa2a-111">Изменение имени или примечаний пакета</span><span class="sxs-lookup"><span data-stu-id="7aa2a-111">To change the package name or comments</span></span>**

1.  <span data-ttu-id="7aa2a-112">Откройте вкладку **Свойства** .</span><span class="sxs-lookup"><span data-stu-id="7aa2a-112">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="7aa2a-113">В текстовом поле **имя пакета** введите или измените одно имя, используемое для пакета, который может содержать несколько приложений.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-113">In the **Package Name** text box, enter or edit the single name used for the package, which can contain multiple applications.</span></span>

3.  <span data-ttu-id="7aa2a-114">В текстовом поле **Примечания** при необходимости введите или измените любые примечания.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-114">In the **Comments** text box, optionally enter or edit any comments.</span></span> <span data-ttu-id="7aa2a-115">Рекомендуемая рекомендация — предоставить подробные сведения о пакете и последовательности.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-115">The suggested best practice is to provide detail information about the package and sequencing.</span></span>

4.  <span data-ttu-id="7aa2a-116">В меню **файл** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-116">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="7aa2a-117">Изменение размера блока</span><span class="sxs-lookup"><span data-stu-id="7aa2a-117">To change the block size</span></span>**

1.  <span data-ttu-id="7aa2a-118">Откройте вкладку **Свойства** .</span><span class="sxs-lookup"><span data-stu-id="7aa2a-118">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="7aa2a-119">В раскрывающемся списке **Размер блока** выберите **4 КБ**, **16 кб**, **32 КБ**или **64 КБ**.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-119">On the **Block Size** drop-down list, select **4 KB**, **16 KB**, **32 KB**, or **64 KB**.</span></span>

3.  <span data-ttu-id="7aa2a-120">В меню **файл** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-120">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="7aa2a-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7aa2a-121">Related topics</span></span>


[<span data-ttu-id="7aa2a-122">Вкладка "Сведения о свойствах"</span><span class="sxs-lookup"><span data-stu-id="7aa2a-122">About the Properties Tab</span></span>](about-the-properties-tab.md)

[<span data-ttu-id="7aa2a-123">Консоль Sequencer</span><span class="sxs-lookup"><span data-stu-id="7aa2a-123">Sequencer Console</span></span>](sequencer-console.md)

 

 





