---
title: Изменение ОС, связанных с существующим файлом установщика Windows
description: Изменение ОС, связанных с существующим файлом установщика Windows
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816952"
---
# <span data-ttu-id="bc400-103">Изменение ОС, связанных с существующим файлом установщика Windows</span><span class="sxs-lookup"><span data-stu-id="bc400-103">How to Modify the Operating Systems Associated With an Existing Windows Installer File</span></span>


<span data-ttu-id="bc400-104">Выполните описанные ниже действия, чтобы изменить версии операционной системы, связанные с существующим файлом установщика Windows (**MSI**), созданным с помощью секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="bc400-104">Use the following procedure to modify the operating system versions associated with an existing Windows Installer (**MSI**) file that was created by using the App-V Sequencer.</span></span>

**<span data-ttu-id="bc400-105">Изменение операционной системы существующего файла установщика Windows</span><span class="sxs-lookup"><span data-stu-id="bc400-105">To modify the operating systems of an existing Windows Installer file</span></span>**

1.  <span data-ttu-id="bc400-106">Установите секвенсор App-V на компьютер в среде с установленной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="bc400-106">Install the App-V Sequencer on a computer in your environment that has only the operating system installed.</span></span> <span data-ttu-id="bc400-107">Кроме того, программа Sequencer может быть установлена на компьютере под управлением виртуальной среды (например, Microsoft Virtual PC).</span><span class="sxs-lookup"><span data-stu-id="bc400-107">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="bc400-108">Этот метод полезен, так как проще поддерживать чистую последовательность, которую можно повторно использовать с минимальной дополнительной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="bc400-108">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span> <span data-ttu-id="bc400-109">Дополнительные сведения об установке секвенсора App-V можно найти в разделе [Установка секвенсора](how-to-install-the-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="bc400-109">For more information about installing the App-V Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

2.  <span data-ttu-id="bc400-110">Скопируйте весь пакет виртуального приложения, содержащий файл установщика Windows, который вы хотите изменить, на компьютер, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="bc400-110">Copy the entire virtual application package that contains the Windows Installer file you want to modify to the computer running the Sequencer.</span></span>

3.  <span data-ttu-id="bc400-111">Чтобы изменить файл установщика Windows, откройте консоль секвенсор, выберите команду **Package**  /  **Открыть**пакет и перейдите в папку, в которой сохранен виртуальный пакет приложения, связанный с файлом установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="bc400-111">To modify the Windows Installer file, open the Sequencer console, select **Package** / **Open**, and then browse to the location where the virtual application package associated with the Windows Installer file is saved.</span></span>

4.  <span data-ttu-id="bc400-112">Чтобы добавить или удалить операционную систему, выберите вкладку " **развертывание** " на консоли секвенсора.</span><span class="sxs-lookup"><span data-stu-id="bc400-112">To add or remove operating systems, select the **Deployment** tab in the Sequencer console.</span></span> <span data-ttu-id="bc400-113">Чтобы указать дополнительные операционные системы, которые будут связаны с файлом установщика Windows, выберите нужную операционную систему, а затем щелкните стрелку, указывающую на **выбранный** элемент управления списком операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bc400-113">To specify additional operating systems that will be associated with the Windows Installer file, select the desired operating system, and then click the arrow that points to the **Selected** operating system list control.</span></span>

    <span data-ttu-id="bc400-114">Чтобы удалить связь с операционной системой, выберите операционную систему, которую вы хотите удалить, и щелкните стрелку, указывающую на **доступный** элемент управления "список операционной системы".</span><span class="sxs-lookup"><span data-stu-id="bc400-114">To remove an operating system association, select the operating system you want to remove, and then click the arrow that points to the **Available** operating system list control.</span></span>

5.  <span data-ttu-id="bc400-115">Чтобы создать новый установщик Windows, связанный с пакетом виртуального приложения, выберите команду **создать пакет установщика Microsoft Windows (MSI)**.</span><span class="sxs-lookup"><span data-stu-id="bc400-115">To create a new Windows Installer that will be associated with the virtual application package, select **Generate Microsoft Windows Installer (MSI) Package**.</span></span> <span data-ttu-id="bc400-116">Кроме того, можно выбрать **инструменты**  /  **Создать MSI**.</span><span class="sxs-lookup"><span data-stu-id="bc400-116">Alternatively, you can select **Tools** / **Create MSI**.</span></span>

    <span data-ttu-id="bc400-117">**Примечание**  Если выбрать пункт **инструменты** / **Создать MSI** для создания нового файла установщика Windows, вы можете пропустить **Шаг 6** этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="bc400-117">**Note** If you select **Tools** / **Create MSI** to create a new Windows Installer file, you can skip **Step 6** of this procedure.</span></span>

     

6.  <span data-ttu-id="bc400-118">Чтобы сохранить виртуальный пакет приложения, выберите команду **Package**  /  **сохранить**пакет.</span><span class="sxs-lookup"><span data-stu-id="bc400-118">To save the virtual application package, select **Package** / **Save**.</span></span>

## <span data-ttu-id="bc400-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="bc400-119">Related topics</span></span>


[<span data-ttu-id="bc400-120">Задачи Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="bc400-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





