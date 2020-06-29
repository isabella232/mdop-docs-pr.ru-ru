---
title: Создание корневого каталога пакета программы Sequencer
description: Создание корневого каталога пакета программы Sequencer
author: dansimp
ms.assetid: 23fe28f1-c284-43ee-b8b7-1dfbed94eea5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5150e87915202794624b6c51510e56454d2c7d36
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817619"
---
# <span data-ttu-id="ac316-103">Создание корневого каталога пакета программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="ac316-103">How to Create the Sequencer Package Root Directory</span></span>


<span data-ttu-id="ac316-104">Корневой каталог пакета — это каталог на компьютере, на котором запущен секвенсор App-V, в котором установлены файлы для упорядоченного приложения.</span><span class="sxs-lookup"><span data-stu-id="ac316-104">The package root directory is the directory on the computer running the App-V Sequencer where files for the sequenced application are installed.</span></span> <span data-ttu-id="ac316-105">Этот каталог также существует практически на компьютере, на котором поток будет передаваться последовательным приложением.</span><span class="sxs-lookup"><span data-stu-id="ac316-105">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span> <span data-ttu-id="ac316-106">Вы должны создать корневой каталог пакета, прежде чем выполнять наблюдение за установкой нового приложения.</span><span class="sxs-lookup"><span data-stu-id="ac316-106">You should create the package root directory before you monitor the installation of a new application.</span></span>

<span data-ttu-id="ac316-107">После создания корневого каталога пакета вы можете приступить к виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="ac316-107">After you have created the package root directory, you can begin sequencing applications.</span></span> <span data-ttu-id="ac316-108">Дополнительные сведения о том, [как последовательное](how-to-sequence-an-application.md)новое приложение, приведены в разделе Упорядочение приложения.</span><span class="sxs-lookup"><span data-stu-id="ac316-108">For more information about sequencing a new application, see [How to Sequence an Application](how-to-sequence-an-application.md).</span></span>

**<span data-ttu-id="ac316-109">Создание корневого каталога пакета</span><span class="sxs-lookup"><span data-stu-id="ac316-109">To create the package root directory</span></span>**

1.  <span data-ttu-id="ac316-110">Чтобы создать корневой каталог пакета, на компьютере с запущенным секвенсором App-V сопоставьте диск Q:\\ с указанным сетевым расположением.</span><span class="sxs-lookup"><span data-stu-id="ac316-110">To create the package root directory, on the computer running the App-V Sequencer, map the Q:\\ drive to the specified network location.</span></span> <span data-ttu-id="ac316-111">В указанном месте должно быть достаточно места для сохранения приложения, которое вы собираетесь поочередно.</span><span class="sxs-lookup"><span data-stu-id="ac316-111">The location you specify should have sufficient space to save the application you are sequencing.</span></span>

2.  <span data-ttu-id="ac316-112">Чтобы создать каталог, который можно использовать для нового виртуального приложения, создайте папку на диске Q:\\ и назначьте ей имя.</span><span class="sxs-lookup"><span data-stu-id="ac316-112">To create a directory that you can use for a new virtual application, create a folder on the Q:\\ drive and assign it a name.</span></span>

    <span data-ttu-id="ac316-113">**Важно!**  Имя, назначаемое виртуальным файлам приложения, которое будет сохранено в корневом каталоге пакета, должно использовать формат именования 8,3.</span><span class="sxs-lookup"><span data-stu-id="ac316-113">**Important** The name you assign to virtual application files that will be saved in the package root directory should use the 8.3 naming format.</span></span> <span data-ttu-id="ac316-114">Имена файлов должны состоять не более чем из 8 символов с тремя-значным расширением имени файла.</span><span class="sxs-lookup"><span data-stu-id="ac316-114">The file names should be no longer than 8 characters with a three-character file name extension.</span></span>

     

## <span data-ttu-id="ac316-115">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ac316-115">Related topics</span></span>


[<span data-ttu-id="ac316-116">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="ac316-116">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

[<span data-ttu-id="ac316-117">Изменение расположения каталога журнала</span><span class="sxs-lookup"><span data-stu-id="ac316-117">How to Modify the Log Directory Location</span></span>](how-to-modify-the-log-directory-location.md)

[<span data-ttu-id="ac316-118">Изменение расположения каталога временных файлов</span><span class="sxs-lookup"><span data-stu-id="ac316-118">How to Modify the Scratch Directory Location</span></span>](how-to-modify-the-scratch-directory-location.md)

 

 





