---
title: Создание корневого каталога пакета
description: Создание корневого каталога пакета
author: dansimp
ms.assetid: bcfe3bd4-6c60-409a-8ffa-cc22f27194b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c9e1e7be71627d4e55eff7a4e2582a21b834876d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817629"
---
# <span data-ttu-id="acd1a-103">Создание корневого каталога пакета</span><span class="sxs-lookup"><span data-stu-id="acd1a-103">How to Create the Package Root Directory</span></span>


<span data-ttu-id="acd1a-104">Корневой каталог пакета — это каталог на компьютере, на котором запущен секвенсор App-V, в котором установлены файлы для упорядоченного приложения.</span><span class="sxs-lookup"><span data-stu-id="acd1a-104">The package root directory is the directory on the computer running the App-V Sequencer where files for the sequenced application are installed.</span></span> <span data-ttu-id="acd1a-105">Этот каталог также существует практически на компьютере, на котором поток будет передаваться последовательным приложением.</span><span class="sxs-lookup"><span data-stu-id="acd1a-105">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span> <span data-ttu-id="acd1a-106">Вы должны создать корневой каталог пакета, прежде чем выполнять наблюдение за установкой нового приложения.</span><span class="sxs-lookup"><span data-stu-id="acd1a-106">You should create the package root directory before you monitor the installation of a new application.</span></span>

<span data-ttu-id="acd1a-107">После создания корневого каталога пакета вы можете приступить к виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="acd1a-107">After you have created the package root directory, you can begin sequencing applications.</span></span> <span data-ttu-id="acd1a-108">Дополнительные сведения о том, [как установить секвенсор, можно найти в разделе Установка программы Sequencer](how-to-install-the-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="acd1a-108">For more information about sequencing a new application, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

**<span data-ttu-id="acd1a-109">Создание корневого каталога пакета</span><span class="sxs-lookup"><span data-stu-id="acd1a-109">To create the package root directory</span></span>**

1.  <span data-ttu-id="acd1a-110">Чтобы создать корневой каталог пакета, на компьютере с запущенным секвенсором App-V сопоставьте диск Q:\\ с указанным сетевым расположением.</span><span class="sxs-lookup"><span data-stu-id="acd1a-110">To create the package root directory, on the computer running the App-V Sequencer, map the Q:\\ drive to the specified network location.</span></span> <span data-ttu-id="acd1a-111">В указанном месте должно быть достаточно места для сохранения приложения, которое вы собираетесь поочередно.</span><span class="sxs-lookup"><span data-stu-id="acd1a-111">The location you specify should have sufficient space to save the application you are sequencing.</span></span>

2.  <span data-ttu-id="acd1a-112">Чтобы создать каталог, который можно использовать для нового виртуального приложения, создайте папку на диске Q:\\ и назначьте ей имя.</span><span class="sxs-lookup"><span data-stu-id="acd1a-112">To create a directory that you can use for a new virtual application, create a folder on the Q:\\ drive and assign it a name.</span></span>

    <span data-ttu-id="acd1a-113">**Важно!**  Имя, назначаемое виртуальным файлам приложения, которое будет сохранено в корневом каталоге пакета, должно использовать формат именования 8,3.</span><span class="sxs-lookup"><span data-stu-id="acd1a-113">**Important** The name you assign to virtual application files that will be saved in the package root directory should use the 8.3 naming format.</span></span> <span data-ttu-id="acd1a-114">Имена файлов должны состоять не более чем из 8 символов с тремя-значным расширением имени файла.</span><span class="sxs-lookup"><span data-stu-id="acd1a-114">The file names should be no longer than 8 characters with a three-character file name extension.</span></span>

     

## <span data-ttu-id="acd1a-115">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="acd1a-115">Related topics</span></span>


[<span data-ttu-id="acd1a-116">Задачи Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="acd1a-116">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





