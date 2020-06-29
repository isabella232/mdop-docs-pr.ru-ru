---
title: Сведения об использовании командной строки программы Sequencer
description: Сведения об использовании командной строки программы Sequencer
author: dansimp
ms.assetid: 0fd5f81b-17f9-4065-bce2-8785e8aac7c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: afb3fb8608c78a3b9237a80529a6c22d792661ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819902"
---
# <span data-ttu-id="847b9-103">Сведения об использовании командной строки программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="847b9-103">About Using the Sequencer Command Line</span></span>


<span data-ttu-id="847b9-104">Для создания пакетов последовательных приложений можно использовать командную строку.</span><span class="sxs-lookup"><span data-stu-id="847b9-104">You can use the command line to create sequenced application packages.</span></span> <span data-ttu-id="847b9-105">Использование командной строки для создания виртуальных приложений полезно в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="847b9-105">Using the command line to create virtual applications is useful in the following scenarios:</span></span>

-   <span data-ttu-id="847b9-106">Вам необходимо создать большое количество последовательных пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="847b9-106">You need to create a large number of sequenced application packages.</span></span>

-   <span data-ttu-id="847b9-107">Вам нужно создать последовательный пакет приложения на регулярной основе.</span><span class="sxs-lookup"><span data-stu-id="847b9-107">You need to create a sequenced application package on a recurring basis.</span></span>

<span data-ttu-id="847b9-108">**Важно!**  Упорядочение в командной строке можно выполнять только для последовательности, используемой по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="847b9-108">**Important** Sequencing at the command prompt allows for default sequencing only.</span></span> <span data-ttu-id="847b9-109">Если необходимо изменить параметры последовательности по умолчанию, необходимо вручную изменить последовательный пакет приложения или перестроить приложение.</span><span class="sxs-lookup"><span data-stu-id="847b9-109">If you need to change default sequencing parameters, you must either manually modify a sequenced application package or re-sequence the application.</span></span>

 

<span data-ttu-id="847b9-110">Все последующие изменения в существующих последовательных пакетах приложения должны быть выполнены с помощью мастера упорядочения.</span><span class="sxs-lookup"><span data-stu-id="847b9-110">All subsequent modifications to existing sequenced application packages must be made using the sequencing wizard.</span></span>

## <span data-ttu-id="847b9-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="847b9-111">Prerequisites</span></span>


<span data-ttu-id="847b9-112">Для последовательной работы приложения с помощью командной строки должны выполняться следующие условия:</span><span class="sxs-lookup"><span data-stu-id="847b9-112">To sequence an application by using the command prompt, the following conditions must be met:</span></span>

-   <span data-ttu-id="847b9-113">Приложение, которое будет выполняться последовательно, не должно требовать изменения или временные решения для него за пределами установщика или пакета установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="847b9-113">The application that is about to be sequenced must not require changes or workarounds made to it outside the installer or Windows Installer package.</span></span>

-   <span data-ttu-id="847b9-114">Перед виртуализацией необходимо подготовить список пакетных файлов для создания последовательных пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="847b9-114">Before sequencing, you must prepare a list of batch files for creating the sequenced application packages.</span></span>

-   <span data-ttu-id="847b9-115">Дополнительные сведения о параметрах командной строки можно найти в разделе [Параметры командной строки](command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="847b9-115">Review For more information about the command line parameters, see [Command-Line Parameters](command-line-parameters.md).</span></span>

-   <span data-ttu-id="847b9-116">Проверьте ошибки, которые могут выводиться при создании пакета упорядоченного приложения с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="847b9-116">Review the errors that might be displayed when creating a sequenced application package by using the command line.</span></span> <span data-ttu-id="847b9-117">Дополнительные сведения об этих ошибках можно найти в разделе [ошибки командной строки](command-line-errors.md).</span><span class="sxs-lookup"><span data-stu-id="847b9-117">For more information, see these errors, see [Command-Line Errors](command-line-errors.md).</span></span>

## <span data-ttu-id="847b9-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="847b9-118">Related topics</span></span>


[<span data-ttu-id="847b9-119">Управление виртуальными приложениями с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="847b9-119">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





