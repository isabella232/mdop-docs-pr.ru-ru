---
title: Обзор виртуализации приложений
description: Обзор виртуализации приложений
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816062"
---
# <span data-ttu-id="0752d-103">Обзор виртуализации приложений</span><span class="sxs-lookup"><span data-stu-id="0752d-103">Overview of Application Virtualization</span></span>


<span data-ttu-id="0752d-104">Microsoft Application Virtualization (App-V) может сделать приложения доступными для конечных пользователей, не устанавливая их непосредственно на эти компьютеры.</span><span class="sxs-lookup"><span data-stu-id="0752d-104">Microsoft Application Virtualization (App-V) can make applications available to end user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="0752d-105">Это можно сделать с помощью процесса, который называется *виртуализацией приложения*, что позволяет каждому приложению выполняться в собственной автономной виртуальной среде на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="0752d-105">This is made possible through a process known as *sequencing the application*, which enables each application to run in its own self-contained virtual environment on the client computer.</span></span> <span data-ttu-id="0752d-106">Упорядоченные приложения изолированы друг от друга.</span><span class="sxs-lookup"><span data-stu-id="0752d-106">The sequenced applications are isolated from each other.</span></span> <span data-ttu-id="0752d-107">Это устраняет конфликты приложения, но приложения по-прежнему могут взаимодействовать с клиентским компьютером.</span><span class="sxs-lookup"><span data-stu-id="0752d-107">This eliminates application conflicts, but the applications can still interact with the client computer.</span></span>

<span data-ttu-id="0752d-108">Клиент App-V — это функция, с помощью которой пользователь может взаимодействовать с приложениями после того, как они были опубликованы на компьютере.</span><span class="sxs-lookup"><span data-stu-id="0752d-108">The App-V client is the feature that lets the end user interact with the applications after they have been published to the computer.</span></span> <span data-ttu-id="0752d-109">Клиент управляет виртуальной средой, в которой виртуализированные приложения выполняются на каждом компьютере.</span><span class="sxs-lookup"><span data-stu-id="0752d-109">The client manages the virtual environment in which the virtualized applications run on each computer.</span></span> <span data-ttu-id="0752d-110">После установки клиента на компьютере приложения должны быть доступны для компьютера с помощью процесса, называемого *публикацией*, который позволяет конечному пользователю запускать виртуальные приложения.</span><span class="sxs-lookup"><span data-stu-id="0752d-110">After the client has been installed on a computer, the applications must be made available to the computer through a process known as *publishing*, which enables the end user to run the virtual applications.</span></span> <span data-ttu-id="0752d-111">Процесс публикации копирует значки виртуальных приложений и ярлыки на компьютер — обычно на рабочем столе Windows или в меню " **Пуск** ", а также копирует на компьютер определение пакета и сведения о сопоставлении типов файлов.</span><span class="sxs-lookup"><span data-stu-id="0752d-111">The publishing process copies the virtual application icons and shortcuts to the computer—typically on the Windows desktop or on the **Start** menu—and also copies the package definition and file type association information to the computer.</span></span> <span data-ttu-id="0752d-112">Публикация также делает содержимое пакета приложения доступным для компьютера конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="0752d-112">Publishing also makes the application package content available to the end user’s computer.</span></span>

<span data-ttu-id="0752d-113">Содержимое виртуального пакета приложения можно скопировать на один или несколько серверов виртуализации приложений, чтобы его можно было передавать клиентам по запросу и кэшировано локально.</span><span class="sxs-lookup"><span data-stu-id="0752d-113">The virtual application package content can be copied onto one or more Application Virtualization servers so that it can be streamed down to the clients on demand and cached locally.</span></span> <span data-ttu-id="0752d-114">Файловые серверы и веб-серверы также можно использовать в качестве потокового сервера, а содержимое можно скопировать непосредственно на компьютер конечного пользователя (например, при использовании электронной системы распространения программного обеспечения, например диспетчера конфигураций конечных точек Microsoft).</span><span class="sxs-lookup"><span data-stu-id="0752d-114">File servers and Web servers can also be used as streaming servers, or the content can be copied directly to the end user’s computer—for example, if you are using an electronic software distribution system, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="0752d-115">При использовании многосерверной реализации, поддержание содержимого пакета и поддержание актуальности на всех потоковых серверах, требуется всестороннее решение для управления пакетами.</span><span class="sxs-lookup"><span data-stu-id="0752d-115">In a multi-server implementation, maintaining the package content and keeping it up to date on all the streaming servers requires a comprehensive package management solution.</span></span> <span data-ttu-id="0752d-116">В зависимости от размера организации может потребоваться наличие большого количества виртуальных приложений, доступных для конечных пользователей, которые находятся в разных странах мира.</span><span class="sxs-lookup"><span data-stu-id="0752d-116">Depending on the size of your organization, you might need to have many virtual applications available to end users located all over the world.</span></span> <span data-ttu-id="0752d-117">Управление пакетами для обеспечения доступности соответствующих приложений для всех пользователей, где и когда им необходим доступ к ним, следовательно, это является важным требованием.</span><span class="sxs-lookup"><span data-stu-id="0752d-117">Managing the packages to ensure that the appropriate applications are available to all users where and when they need access to them is therefore an important requirement.</span></span>

## <span data-ttu-id="0752d-118">Возможности системы Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0752d-118">Microsoft Application Virtualization System Features</span></span>


<span data-ttu-id="0752d-119">В таблице ниже описаны основные возможности системы управления виртуализацией приложений Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0752d-119">The following table describes the primary features of the Microsoft Application Virtualization Management System.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0752d-120">Функция</span><span class="sxs-lookup"><span data-stu-id="0752d-120">Feature</span></span></th>
<th align="left"><span data-ttu-id="0752d-121">Функция</span><span class="sxs-lookup"><span data-stu-id="0752d-121">Function</span></span></th>
<th align="left"><span data-ttu-id="0752d-122">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="0752d-122">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0752d-123">Сервер управления виртуализацией приложений Майкрософт</span><span class="sxs-lookup"><span data-stu-id="0752d-123">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-124">Отвечает за потоковую передачу содержимого пакета и публикацию ярлыков и сопоставлений типов файлов в клиенте Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="0752d-124">Responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-125">Сервер управления виртуализацией приложений поддерживает активное обновление, Управление лицензиями и базу данных, которые можно использовать для создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="0752d-125">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0752d-126"></strong>Папка содержимого</span><span class="sxs-lookup"><span data-stu-id="0752d-126">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-127">Указывает расположение пакетов Application Virtualization для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="0752d-127">Indicates the location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-128">Эту папку можно найти в общем доступе на сервере управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="0752d-128">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0752d-129">Консоль управления Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0752d-129">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-130">Эта консоль — средство управления оснасткой MMC 3,0, используемое для администрирования сервера виртуализации приложений Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0752d-130">This console is an MMC 3.0 snap-in management tool used for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-131">Это средство можно установить на сервере Microsoft Application Virtualization или на отдельной рабочей станции с консолью управления Майкрософт (MMC) 3.0 и Microsoft. NETFramework 2,0 установлен.</span><span class="sxs-lookup"><span data-stu-id="0752d-131">This tool can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has Microsoft Management Console (MMC)3.0 and Microsoft .NETFramework 2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0752d-132">Веб-служба управления виртуализацией приложений Майкрософт</span><span class="sxs-lookup"><span data-stu-id="0752d-132">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-133">Отвечает за связь запросов на чтение и запись в хранилище данных Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="0752d-133">Responsible for communicating any read and write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-134">Веб-службу управления можно установить на сервере управления виртуализацией приложений (Майкрософт) или на отдельном компьютере, на котором установлены службы Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="0752d-134">The Management Web Service can be installed on the Microsoft Application Virtualization Management server or on a separate computer that has Microsoft Internet Information Services (IIS) installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0752d-135">Хранилище данных Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0752d-135">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-136">База данных SQL Server App-V отвечает за хранение всей информации, связанной с инфраструктурой виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="0752d-136">The App-V SQL Server database responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-137">Эти сведения включают все записи приложений, назначения приложений и группы, ответственные за управление средой виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="0752d-137">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0752d-138">Сервер потоковой передачи Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0752d-138">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-139">Ответственность за размещение пакетов Application Virtualization для потоковой передачи клиентам в филиале, где ссылка на сервер управления виртуализацией приложений считается глобальным подключением к глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="0752d-139">Responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a wide area networks (WAN) connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-140">Этот сервер содержит только потоковую функциональность и не предоставляет ни консоль управления Application Virtualization, ни веб-службу управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="0752d-140">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0752d-141">Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="0752d-141">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-142">Секвенсор используется для отслеживания и сохранения установки приложений для создания пакетов виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="0752d-142">The sequencer is used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-143">Результат состоит из значков приложения, OSD-файла, который содержит сведения о определении пакета, файла манифеста пакета и SFT-файла, содержащего файлы содержимого программы приложения.</span><span class="sxs-lookup"><span data-stu-id="0752d-143">The output consists of the application’s icons, an .osd file that contains package definition information, a package manifest file, and the .sft file that contains the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0752d-144">Клиент Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0752d-144">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-145">Классическое приложение Application Virtualization и клиент Application Virtualization для служб удаленных рабочих столов предоставляют виртуальную среду для виртуализированных приложений и управляют ею.</span><span class="sxs-lookup"><span data-stu-id="0752d-145">The Application Virtualization Desktop Client and the Application Virtualization Client for Remote Desktop Services provide and manage the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0752d-146">Клиент Microsoft Application Virtualization управляет потоковой передачей пакета в кэш, обновлять публикацию, транспортировку и все взаимодействие с серверами Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="0752d-146">The Microsoft Application Virtualization client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





