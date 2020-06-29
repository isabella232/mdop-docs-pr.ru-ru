---
title: Вкладка "Общие"
description: Вкладка "Общие"
author: dansimp
ms.assetid: aeefae39-60cd-4ad4-9575-c07d7e2b1e59
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 327635422030b713aeadbc5de0007685b69e1c2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821472"
---
# <span data-ttu-id="137e5-103">Вкладка "Общие"</span><span class="sxs-lookup"><span data-stu-id="137e5-103">General Tab</span></span>


<span data-ttu-id="137e5-104">Вкладка " **Общие** " используется для настройки параметров секвенсора Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="137e5-104">Use the **General** tab to configure options for Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<a href="" id="scratch-directory"></a>**<span data-ttu-id="137e5-105">Вспомогательный каталог</span><span class="sxs-lookup"><span data-stu-id="137e5-105">Scratch Directory</span></span>**  
<span data-ttu-id="137e5-106">Указывает путь к расположению, в котором секвенсор временно сохраняет файлы, созданные в процессе упорядочивания.</span><span class="sxs-lookup"><span data-stu-id="137e5-106">Specifies the path to the location where the Sequencer will temporarily save files generated during sequencing.</span></span> <span data-ttu-id="137e5-107">Путь по умолчанию — C:\\ProgramFiles\\Microsoft Виртуализация приложений Sequencer\\Scratch.</span><span class="sxs-lookup"><span data-stu-id="137e5-107">The default path is C:\\ProgramFiles\\Microsoft Application Virtualization Sequencer\\Scratch.</span></span> <span data-ttu-id="137e5-108">Чтобы указать новый путь, нажмите кнопку **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="137e5-108">To specify a new path, click **Browse**.</span></span>

<a href="" id="log-directory"></a>**<span data-ttu-id="137e5-109">Каталог журнала</span><span class="sxs-lookup"><span data-stu-id="137e5-109">Log Directory</span></span>**  
<span data-ttu-id="137e5-110">Указывает путь к каталогу, в котором программа Sequencer будет хранить файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="137e5-110">Specifies the path to the directory where the Sequencer will save log files.</span></span> <span data-ttu-id="137e5-111">Путь по умолчанию — C:\\ProgramFiles\\Microsoft Виртуализация приложений Sequencer\\Logs.</span><span class="sxs-lookup"><span data-stu-id="137e5-111">The default path is C:\\ProgramFiles\\Microsoft Application Virtualization Sequencer\\Logs.</span></span> <span data-ttu-id="137e5-112">Чтобы указать новый путь, нажмите кнопку **Обзор** .</span><span class="sxs-lookup"><span data-stu-id="137e5-112">To specify a new path, click **Browse**</span></span>

<a href="" id="allow-use-of-msi-installer"></a>**<span data-ttu-id="137e5-113">Разрешить использование установщика MSI</span><span class="sxs-lookup"><span data-stu-id="137e5-113">Allow Use of MSI Installer</span></span>**  
<span data-ttu-id="137e5-114">Выберите этот параметр, чтобы разрешить взаимодействие между секвенсором и установщиком приложения.</span><span class="sxs-lookup"><span data-stu-id="137e5-114">Select this option to allow interaction between the Sequencer and the application installer.</span></span> <span data-ttu-id="137e5-115">Этот параметр выбран по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="137e5-115">This option is selected by default.</span></span>

<a href="" id="allow-virtualization-of-events"></a>**<span data-ttu-id="137e5-116">Разрешить виртуализацию событий</span><span class="sxs-lookup"><span data-stu-id="137e5-116">Allow Virtualization of Events</span></span>**  
<span data-ttu-id="137e5-117">Выберите этот параметр, чтобы разрешить виртуализацию низкоуровневых операций операционной системы приложения, если последовательный пакет приложения выполняется на настольных клиентах App-V.</span><span class="sxs-lookup"><span data-stu-id="137e5-117">Select this option to allow low-level operating system activities of the application to be virtualized when a sequenced application package is run on App-V Desktop Clients.</span></span> <span data-ttu-id="137e5-118">Этот параметр выбран по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="137e5-118">This option is selected by default.</span></span>

<a href="" id="allow-virtualization-of-services"></a>**<span data-ttu-id="137e5-119">Разрешить виртуализацию служб</span><span class="sxs-lookup"><span data-stu-id="137e5-119">Allow Virtualization of Services</span></span>**  
<span data-ttu-id="137e5-120">Выберите этот параметр, чтобы разрешить виртуализацию служб, необходимых приложению, при запуске приложения на настольных компьютерах App-V.</span><span class="sxs-lookup"><span data-stu-id="137e5-120">Select this option to allow services required by the application to be virtualized when the application is run on App-V Desktop Clients.</span></span> <span data-ttu-id="137e5-121">Этот параметр выбран по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="137e5-121">This option is selected by default.</span></span>

<a href="" id="append-package-version-to-filename"></a>**<span data-ttu-id="137e5-122">Добавление версии пакета в имя файла</span><span class="sxs-lookup"><span data-stu-id="137e5-122">Append Package Version to Filename</span></span>**  
<span data-ttu-id="137e5-123">Выберите этот параметр, чтобы автоматически добавить в имя файла последовательный номер версии пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="137e5-123">Select this option to automatically append the sequenced application package version number to the file name.</span></span> <span data-ttu-id="137e5-124">Этот параметр выбран по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="137e5-124">This option is selected by default.</span></span>

<a href="" id="ok"></a>**<span data-ttu-id="137e5-125">ОК</span><span class="sxs-lookup"><span data-stu-id="137e5-125">OK</span></span>**  
<span data-ttu-id="137e5-126">Сохранение изменений и закрытие диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="137e5-126">Saves changes and closes the dialog box.</span></span>

<a href="" id="cancel"></a>**<span data-ttu-id="137e5-127">Отмена</span><span class="sxs-lookup"><span data-stu-id="137e5-127">Cancel</span></span>**  
<span data-ttu-id="137e5-128">Выход из диалогового окна без сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="137e5-128">Exits the dialog box without saving any changes.</span></span>

<a href="" id="apply"></a>**<span data-ttu-id="137e5-129">Подать заявку</span><span class="sxs-lookup"><span data-stu-id="137e5-129">Apply</span></span>**  
<span data-ttu-id="137e5-130">Сохраняет изменения и остается в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="137e5-130">Saves the changes and remains in the dialog box.</span></span>

## <span data-ttu-id="137e5-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="137e5-131">Related topics</span></span>


[<span data-ttu-id="137e5-132">Диалоговое окно параметров программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="137e5-132">Application Virtualization Sequencer Options Dialog Box</span></span>](application-virtualization-sequencer-options-dialog-box.md)

 

 





