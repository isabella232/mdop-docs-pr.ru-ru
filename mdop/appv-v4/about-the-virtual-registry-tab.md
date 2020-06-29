---
title: Вкладка "Сведения о виртуальном реестре"
description: Вкладка "Сведения о виртуальном реестре"
author: dansimp
ms.assetid: ca8d837f-8218-4f86-95fd-13a44dccd022
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 77decee4a8e07333b466db0a1bd0513efe859c9a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819892"
---
# <span data-ttu-id="dd6e3-103">Вкладка "Сведения о виртуальном реестре"</span><span class="sxs-lookup"><span data-stu-id="dd6e3-103">About the Virtual Registry Tab</span></span>


<span data-ttu-id="dd6e3-104">Виртуальный реестр создается во время последовательности.</span><span class="sxs-lookup"><span data-stu-id="dd6e3-104">A virtual registry is created during sequencing.</span></span> <span data-ttu-id="dd6e3-105">На вкладке **виртуальный реестр** отображаются все разделы реестра и значения, необходимые для выполнения последовательного пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="dd6e3-105">The **Virtual Registry** tab displays all the registry keys and values that are required for a sequenced application package to run.</span></span> <span data-ttu-id="dd6e3-106">Эта вкладка используется для добавления, изменения и удаления разделов реестра и значений реестра.</span><span class="sxs-lookup"><span data-stu-id="dd6e3-106">Use this tab to add, edit, and delete registry keys and registry values.</span></span>

<span data-ttu-id="dd6e3-107">Вы также можете игнорировать ключи системы размещения, выбрав параметр **переопределить локальный ключ**или создав объединенное представление ключа в виртуальной среде, выбрав команду **объединить с локальным ключом**.</span><span class="sxs-lookup"><span data-stu-id="dd6e3-107">You can also choose to ignore the hosting system’s keys by selecting **Override Local Key**, or you can create a merged view of the key from within the virtual environment by selecting **Merge with Local Key**.</span></span>

<span data-ttu-id="dd6e3-108">Изменения, внесенные в вкладку **Параметры** виртуального реестра, влияют на приложения, которые являются частью определенного пакета приложения, но они не влияют на работу других приложений, которые переносятся в поток или локально установлены на клиентском компьютере Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="dd6e3-108">The changes to the virtual registry **Settings** tab affect applications that are part of the specific sequenced application package, but they do not affect the operation of other applications that are streamed to or locally installed on the Application Virtualization Desktop Client.</span></span>

<span data-ttu-id="dd6e3-109">**Примечание**  Будьте осторожны, изменяя разделы и значения виртуальных разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="dd6e3-109">**Note** Exercise caution when changing virtual registry keys and values.</span></span> <span data-ttu-id="dd6e3-110">Изменение этих ключей и значений может привести к неработоспособности упорядоченного пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="dd6e3-110">Changing these keys and values might render your sequenced application package inoperable.</span></span>

 

<span data-ttu-id="dd6e3-111">В левой области на вкладке **Virtual Registry (виртуальный реестр** ) показан полный список виртуальных реестров, созданных в процессе виртуализации приложения.</span><span class="sxs-lookup"><span data-stu-id="dd6e3-111">The left pane of the **Virtual Registry** tab displays the full list of virtual registries created during the sequencing of an application.</span></span>

## <span data-ttu-id="dd6e3-112">Столбцы</span><span class="sxs-lookup"><span data-stu-id="dd6e3-112">Columns</span></span>


<a href="" id="name"></a>**<span data-ttu-id="dd6e3-113">Имя</span><span class="sxs-lookup"><span data-stu-id="dd6e3-113">Name</span></span>**  
<span data-ttu-id="dd6e3-114">Имя записи в виртуальном реестре.</span><span class="sxs-lookup"><span data-stu-id="dd6e3-114">The name for the entry in the virtual registry.</span></span>

<a href="" id="type"></a>**<span data-ttu-id="dd6e3-115">Тип</span><span class="sxs-lookup"><span data-stu-id="dd6e3-115">Type</span></span>**  
<span data-ttu-id="dd6e3-116">Способ хранения данных в записи.</span><span class="sxs-lookup"><span data-stu-id="dd6e3-116">How the entry stores its data.</span></span>

<a href="" id="data"></a>**<span data-ttu-id="dd6e3-117">Данные</span><span class="sxs-lookup"><span data-stu-id="dd6e3-117">Data</span></span>**  
<span data-ttu-id="dd6e3-118">Значение, сохраненное в элементе.</span><span class="sxs-lookup"><span data-stu-id="dd6e3-118">The value stored by the entry.</span></span>

<a href="" id="attributes"></a>**<span data-ttu-id="dd6e3-119">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="dd6e3-119">Attributes</span></span>**  
<span data-ttu-id="dd6e3-120">Отображение атрибутов файла.</span><span class="sxs-lookup"><span data-stu-id="dd6e3-120">Displays the file attributes.</span></span>

## <span data-ttu-id="dd6e3-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="dd6e3-121">Related topics</span></span>


[<span data-ttu-id="dd6e3-122">Изменение информации раздела виртуального реестра</span><span class="sxs-lookup"><span data-stu-id="dd6e3-122">How to Modify Virtual Registry Key Information</span></span>](how-to-modify-virtual-registry-key-information.md)

[<span data-ttu-id="dd6e3-123">Консоль Sequencer</span><span class="sxs-lookup"><span data-stu-id="dd6e3-123">Sequencer Console</span></span>](sequencer-console.md)

 

 





