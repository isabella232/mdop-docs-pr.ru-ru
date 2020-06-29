---
title: Изменение расположения каталога журнала
description: Изменение расположения каталога журнала
author: dansimp
ms.assetid: 203c674f-8d46-4d42-9af0-245a2681fc0f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 267b37a7f629551b5556aab95b131b88aec9ad17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816959"
---
# <span data-ttu-id="8c407-103">Изменение расположения каталога журнала</span><span class="sxs-lookup"><span data-stu-id="8c407-103">How to Modify the Log Directory Location</span></span>


<span data-ttu-id="8c407-104">Расположение каталога журнала — это место, в котором секвенсор Application Virtualization (App-V) записывает сведения о последовательности приложения.</span><span class="sxs-lookup"><span data-stu-id="8c407-104">The log directory location is where the Application Virtualization (App-V) Sequencer writes information about the sequencing of an application.</span></span>

<span data-ttu-id="8c407-105">**Важно!**  Каталог расположения журнала должен находиться на компьютере, на котором запущен секвенсор App-V.</span><span class="sxs-lookup"><span data-stu-id="8c407-105">**Important** The log location directory must be located on the computer running the App-V Sequencer.</span></span>

 

<span data-ttu-id="8c407-106">Используйте описанную ниже процедуру, чтобы изменить расположение каталога, в котором секвенсор App-V сохраняет связанные журналы.</span><span class="sxs-lookup"><span data-stu-id="8c407-106">Use the following procedure to change the location of the directory where the App-V Sequencer will save associated logs.</span></span>

**<span data-ttu-id="8c407-107">Изменение расположения каталога журнала</span><span class="sxs-lookup"><span data-stu-id="8c407-107">To modify the log directory location</span></span>**

1.  <span data-ttu-id="8c407-108">Чтобы открыть консоль Sequencer App-v, на компьютере с запущенным секвенсором App-v выберите **Пуск**  /  **программы**  /  **Microsoft**Application Virtualization  /  **Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="8c407-108">To open the App-V Sequencer Console, on the computer running the App-V Sequencer, select **Start** / **Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="8c407-109">Чтобы открыть диалоговое окно **Параметры** секвенсора App-V, выберите **Сервис**  /  **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="8c407-109">To access the App-V Sequencer **Options** dialog box, select **Tools** / **Options**.</span></span> <span data-ttu-id="8c407-110">На вкладке **Общие** укажите новое расположение, в котором нужно сохранить данные файла журнала секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="8c407-110">On the **General** tab, specify the new directory location where you want the App-V Sequencer log file information to be saved.</span></span> <span data-ttu-id="8c407-111">Кроме того, вы можете нажать кнопку **Обзор** и использовать диалоговое окно **Обзор папок** , чтобы указать новое расположение.</span><span class="sxs-lookup"><span data-stu-id="8c407-111">Alternatively, you can click **Browse** and use the **Browse For Folder** dialog box to specify a new location.</span></span>

3.  <span data-ttu-id="8c407-112">Чтобы сохранить новое расположение и закрыть диалоговое окно " **Параметры** ", нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8c407-112">To save the new location and close the **Options** dialog box, click **OK**.</span></span>

## <span data-ttu-id="8c407-113">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8c407-113">Related topics</span></span>


[<span data-ttu-id="8c407-114">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="8c407-114">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

[<span data-ttu-id="8c407-115">Настройка программы App-V Sequencer</span><span class="sxs-lookup"><span data-stu-id="8c407-115">How to Configure the App-V Sequencer</span></span>](how-to-configure-the-app-v-sequencer.md)

 

 





