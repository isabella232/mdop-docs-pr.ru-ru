---
title: Открытие виртуализированного приложения с помощью командной строки
description: Открытие виртуализированного приложения с помощью командной строки
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816919"
---
# <span data-ttu-id="bc24e-103">Открытие виртуализированного приложения с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="bc24e-103">How to Open a Sequenced Application Using the Command Line</span></span>


<span data-ttu-id="bc24e-104">Вы можете открыть пакеты виртуальных приложений с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="bc24e-104">You can open virtual application packages using the command line.</span></span> <span data-ttu-id="bc24e-105">Вы должны запустить командную запись **cmd** в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="bc24e-105">You must run the **cmd** prompt as an administrator.</span></span>

<span data-ttu-id="bc24e-106">Чтобы открыть последовательные пакеты приложений с помощью командной строки, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="bc24e-106">Use the following procedure to open sequenced application packages using the command line</span></span>

**<span data-ttu-id="bc24e-107">Открытие последовательного приложения с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="bc24e-107">To open a sequenced application using the command line</span></span>**

1.  <span data-ttu-id="bc24e-108">Чтобы открыть командную команду, нажмите кнопку **Пуск**и выберите команду **выполнить**, введите **cmd**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bc24e-108">To open the command prompt, click **Start**, and select **Run**, type **cmd**, and click **OK**.</span></span>

2.  <span data-ttu-id="bc24e-109">В командной строке введите **cd\\** и укажите путь к каталогу, в котором установлен секвенсор, и нажмите клавишу **ВВОД.**</span><span class="sxs-lookup"><span data-stu-id="bc24e-109">At a command prompt, type **cd\\** and specify the path to the directory where the Sequencer is installed and then press **Enter.**</span></span>

3.  <span data-ttu-id="bc24e-110">В командной строке введите следующую команду, заменив текст курсивом на значения:</span><span class="sxs-lookup"><span data-stu-id="bc24e-110">At the command prompt, type the following command, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="bc24e-111">SFTSequencer/OPEN:*"указывает файл SPRJ, который нужно открыть"*</span><span class="sxs-lookup"><span data-stu-id="bc24e-111">SFTSequencer /OPEN:*”specifies the .sprj file to open"*</span></span>

    <span data-ttu-id="bc24e-112">Нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="bc24e-112">Press **Enter**.</span></span>

4.  <span data-ttu-id="bc24e-113">Вы также можете указать следующие необязательные параметры.</span><span class="sxs-lookup"><span data-stu-id="bc24e-113">You can also specify the following optional parameters.</span></span> <span data-ttu-id="bc24e-114">В командной строке введите следующие команды, заменив курсивный текст на нужные значения:</span><span class="sxs-lookup"><span data-stu-id="bc24e-114">At the command prompt, type the following commands, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="bc24e-115">/PACKAGENAME: "*указывает имя пакета"*</span><span class="sxs-lookup"><span data-stu-id="bc24e-115">/PACKAGENAME:"*specifies the package name"*</span></span>

    <span data-ttu-id="bc24e-116">/MSI-указывает на создание связанного установщика Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bc24e-116">/MSI - specifies generating an associated Microsoft Windows Installer.</span></span>

    <span data-ttu-id="bc24e-117">/COMPRESS — указывает, будет ли пакет сжиматься.</span><span class="sxs-lookup"><span data-stu-id="bc24e-117">/COMPRESS – specifies if the package will be compressed.</span></span> <span data-ttu-id="bc24e-118">По умолчанию пакеты не сжимаются.</span><span class="sxs-lookup"><span data-stu-id="bc24e-118">By default, packages are not compressed.</span></span>

    <span data-ttu-id="bc24e-119">Нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="bc24e-119">Press **Enter**.</span></span>

    <span data-ttu-id="bc24e-120">**Примечание**  Если установщик или пакет установщика Windows имеет графический интерфейс пользователя, он будет отображаться после того, как вы задаете параметры командной строки.</span><span class="sxs-lookup"><span data-stu-id="bc24e-120">**Note** If the installer or Windows Installer package has a graphical user interface, it will be displayed after you specify the command-line parameters.</span></span>

     

## <span data-ttu-id="bc24e-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="bc24e-121">Related topics</span></span>


[<span data-ttu-id="bc24e-122">Управление виртуальными приложениями с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="bc24e-122">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





