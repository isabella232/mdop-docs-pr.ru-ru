---
title: Вкладка "Элементы исключения"
description: Вкладка "Элементы исключения"
author: dansimp
ms.assetid: 864e46dd-3d6e-4a1b-acf4-9dc00548117e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f472fb61c121a1977c3c4ff927bd1ba6f680d86
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821579"
---
# <span data-ttu-id="fd1b4-103">Вкладка "Элементы исключения"</span><span class="sxs-lookup"><span data-stu-id="fd1b4-103">Exclusion Items Tab</span></span>


<span data-ttu-id="fd1b4-104">На вкладке **элементы исключений** отображаются выражения, исключаемые секвенсором Application Virtualization из виртуальной файловой системы или виртуального реестра.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-104">The **Exclusion Items** tab displays the expressions that the Application Virtualization Sequencer excludes from the virtual file system or virtual registry.</span></span> <span data-ttu-id="fd1b4-105">Эти выражения исключены для обеспечения возможности запуска упорядоченного пакета приложения на клиентских компьютерах Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-105">These expressions are excluded to ensure that the sequenced application package can run on Application Virtualization Desktop Clients.</span></span> <span data-ttu-id="fd1b4-106">Вы также можете исключить нестандартные каталоги установки, которые могут быть нежелательными в последовательности.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-106">You can also exclude non-standard installation directories that might be unwanted in the sequencing.</span></span>

<span data-ttu-id="fd1b4-107">На этой вкладке есть указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-107">This tab contains the following elements.</span></span>

<a href="" id="exclude-path"></a>**<span data-ttu-id="fd1b4-108">Исключить путь</span><span class="sxs-lookup"><span data-stu-id="fd1b4-108">Exclude Path</span></span>**  
<span data-ttu-id="fd1b4-109">Отображает имена переменных, которые программа Sequencer исключает при анализе элементов виртуальной файловой системы или виртуальных элементов реестра.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-109">Displays variable names that the Sequencer excludes if encountered while parsing virtual file system items or virtual registry items.</span></span>

<a href="" id="resolves-to"></a>**<span data-ttu-id="fd1b4-110">Разрешается в</span><span class="sxs-lookup"><span data-stu-id="fd1b4-110">Resolves To</span></span>**  
<span data-ttu-id="fd1b4-111">Показывает фактические пути, соответствующие переменным секвенсора.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-111">Displays the actual paths that correspond to the Sequencer variables.</span></span>

<a href="" id="map-type"></a>**<span data-ttu-id="fd1b4-112">Тип карты</span><span class="sxs-lookup"><span data-stu-id="fd1b4-112">Map Type</span></span>**  
<span data-ttu-id="fd1b4-113">Выводит правила сопоставления, применяемые секвенсором для синтаксического анализа элементов в виртуальной файловой системе или виртуальном реестре.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-113">Displays mapping rules that the Sequencer applies to parse items in the virtual file system or virtual registry.</span></span> <span data-ttu-id="fd1b4-114">Может произойти одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="fd1b4-114">One of the following values can occur:</span></span>

<a href="" id="new"></a>**<span data-ttu-id="fd1b4-115">Новый</span><span class="sxs-lookup"><span data-stu-id="fd1b4-115">New</span></span>**  
<span data-ttu-id="fd1b4-116">Щелкните, чтобы ввести новый элемент исключения.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-116">Click to enter a new exclusion item.</span></span>

<a href="" id="edit"></a>**<span data-ttu-id="fd1b4-117">Edit</span><span class="sxs-lookup"><span data-stu-id="fd1b4-117">Edit</span></span>**  
<span data-ttu-id="fd1b4-118">Щелкните, чтобы изменить выбранное исключение.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-118">Click to edit a selected exclusion.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="fd1b4-119">Delete</span><span class="sxs-lookup"><span data-stu-id="fd1b4-119">Delete</span></span>**  
<span data-ttu-id="fd1b4-120">Щелкните, чтобы удалить выбранное исключение.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-120">Click to remove a selected exclusion.</span></span>

<a href="" id="save-as-default"></a>**<span data-ttu-id="fd1b4-121">Сохранить по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fd1b4-121">Save As Default</span></span>**  
<span data-ttu-id="fd1b4-122">Нажмите эту кнопку, чтобы сохранить текущие исключаемые элементы как используемые по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-122">Click to save the current exclusion items as your default.</span></span>

<a href="" id="restore-defaults"></a>**<span data-ttu-id="fd1b4-123">Восстановление значений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fd1b4-123">Restore Defaults</span></span>**  
<span data-ttu-id="fd1b4-124">Щелкните, чтобы восстановить элементы, назначенные по умолчанию, и удалите все добавленные элементы.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-124">Click to restore default-assigned exclusion items and remove any items you added.</span></span>

<a href="" id="ok"></a>**<span data-ttu-id="fd1b4-125">ОК</span><span class="sxs-lookup"><span data-stu-id="fd1b4-125">OK</span></span>**  
<span data-ttu-id="fd1b4-126">Щелкните, чтобы сохранить отображаемые исключения.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-126">Click to accept the displayed exceptions.</span></span>

<a href="" id="cancel"></a>**<span data-ttu-id="fd1b4-127">Отмена</span><span class="sxs-lookup"><span data-stu-id="fd1b4-127">Cancel</span></span>**  
<span data-ttu-id="fd1b4-128">Нажмите эту кнопку, чтобы отменить внесенные изменения.</span><span class="sxs-lookup"><span data-stu-id="fd1b4-128">Click to cancel any changes you have made.</span></span>

## <span data-ttu-id="fd1b4-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="fd1b4-129">Related topics</span></span>


[<span data-ttu-id="fd1b4-130">Диалоговое окно параметров программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="fd1b4-130">Application Virtualization Sequencer Options Dialog Box</span></span>](application-virtualization-sequencer-options-dialog-box.md)

[<span data-ttu-id="fd1b4-131">Диалоговое окно "Элементы исключения"</span><span class="sxs-lookup"><span data-stu-id="fd1b4-131">Exclusion Item Dialog Box</span></span>](exclusion-item-dialog-box.md)

 

 





