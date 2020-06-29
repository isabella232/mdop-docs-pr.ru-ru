---
title: Изменение расположения каталога временных файлов
description: Изменение расположения каталога временных файлов
author: dansimp
ms.assetid: 61ecb379-85be-4316-8023-a2c1811504e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2de0c600ad1cd931e4d3762a2d73fce90b4a638
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816942"
---
# <span data-ttu-id="e792b-103">Изменение расположения каталога временных файлов</span><span class="sxs-lookup"><span data-stu-id="e792b-103">How to Modify the Scratch Directory Location</span></span>


<span data-ttu-id="e792b-104">Вспомогательный каталог используется секвенсором App-V для сохранения временных файлов в процессе виртуализации приложения.</span><span class="sxs-lookup"><span data-stu-id="e792b-104">The scratch directory is used by the App-V Sequencer to save temporary files during the sequencing of an application.</span></span>

<span data-ttu-id="e792b-105">**Важно!**  Указанное расположение вспомогательной папки должно находиться на компьютере с секвенсором App-V.</span><span class="sxs-lookup"><span data-stu-id="e792b-105">**Important** The specified scratch directory location should be located on the computer running the App-V Sequencer.</span></span>

 

<span data-ttu-id="e792b-106">Чтобы изменить расположение вспомогательной папки, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e792b-106">Use the following procedure to modify the scratch directory location.</span></span>

**<span data-ttu-id="e792b-107">Изменение расположения вспомогательной папки</span><span class="sxs-lookup"><span data-stu-id="e792b-107">To modify the scratch directory location</span></span>**

1.  <span data-ttu-id="e792b-108">Чтобы открыть консоль Sequencer App-v, на компьютере с запущенным секвенсором App-v выберите **Пуск**  /  **программы**  /  **Microsoft**Application Virtualization  /  **Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="e792b-108">To open the App-V Sequencer Console, on the computer running the App-V Sequencer, select **Start** / **Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="e792b-109">Чтобы открыть диалоговое окно **Параметры** секвенсора App-V, выберите **Сервис**  /  **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="e792b-109">To access the App-V Sequencer **Options** dialog box, select **Tools** / **Options**.</span></span> <span data-ttu-id="e792b-110">На вкладке **Общие** укажите новую папку, в которой нужно сохранить временные файлы секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="e792b-110">On the **General** tab, specify the new scratch directory location where you want the App-V Sequencer temporary files to be saved.</span></span> <span data-ttu-id="e792b-111">Кроме того, вы можете нажать кнопку **Обзор** и использовать диалоговое окно **Обзор папок** , чтобы указать новое расположение.</span><span class="sxs-lookup"><span data-stu-id="e792b-111">Alternatively, you can click **Browse** and use the **Browse For Folder** dialog box to specify a new location.</span></span>

3.  <span data-ttu-id="e792b-112">Чтобы сохранить новое расположение и закрыть диалоговое окно " **Параметры** ", нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e792b-112">To save the new location and close the **Options** dialog box, click **OK**.</span></span>

## <span data-ttu-id="e792b-113">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e792b-113">Related topics</span></span>


[<span data-ttu-id="e792b-114">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="e792b-114">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

[<span data-ttu-id="e792b-115">Создание корневого каталога пакета программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="e792b-115">How to Create the Sequencer Package Root Directory</span></span>](how-to-create-the-sequencer-package-root-directory.md)

[<span data-ttu-id="e792b-116">Изменение расположения каталога журнала</span><span class="sxs-lookup"><span data-stu-id="e792b-116">How to Modify the Log Directory Location</span></span>](how-to-modify-the-log-directory-location.md)

 

 





