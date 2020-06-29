---
title: Обзор компонентов системы Application Virtualization
description: Обзор компонентов системы Application Virtualization
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816052"
---
# <span data-ttu-id="5d9dd-103">Обзор компонентов системы Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="5d9dd-103">Overview of the Application Virtualization System Components</span></span>


<span data-ttu-id="5d9dd-104">В приведенной ниже таблице описаны основные компоненты системы управления виртуализацией приложений Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-104">The following table describes the primary components of the Microsoft Application Virtualization Management System.</span></span> <span data-ttu-id="5d9dd-105">Дополнительные сведения о том, как развертывать эти компоненты системы, можно найти в разделе [сценарий на сервере Application Virtualization](application-virtualization-server-based-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="5d9dd-105">For more information about deploying these system components, see [Application Virtualization Server-Based Scenario](application-virtualization-server-based-scenario.md).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5d9dd-106">Компонент</span><span class="sxs-lookup"><span data-stu-id="5d9dd-106">Component</span></span></th>
<th align="left"><span data-ttu-id="5d9dd-107">Функция</span><span class="sxs-lookup"><span data-stu-id="5d9dd-107">Function</span></span></th>
<th align="left"><span data-ttu-id="5d9dd-108">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="5d9dd-108">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5d9dd-109">Сервер управления виртуализацией приложений Майкрософт</span><span class="sxs-lookup"><span data-stu-id="5d9dd-109">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-110">Компонент, ответственный за потоковую передачу содержимого пакета и публикацию ярлыков и сопоставлений типов файлов в клиенте Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-110">The component responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-111">Сервер управления виртуализацией приложений поддерживает активное обновление, Управление лицензиями и базу данных, которые можно использовать для создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-111">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5d9dd-112"></strong>Папка содержимого</span><span class="sxs-lookup"><span data-stu-id="5d9dd-112">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-113">Расположение пакетов Application Virtualization для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-113">The location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-114">Эту папку можно найти в общем доступе на сервере управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-114">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span> <span data-ttu-id="5d9dd-115">Эта папка также может находиться в сети хранения данных (SAN).</span><span class="sxs-lookup"><span data-stu-id="5d9dd-115">The folder can also be located on a Storage Area Network (SAN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5d9dd-116">Консоль управления Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="5d9dd-116">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-117">Средство управления оснасткой MMC 3,0 для администрирования сервера виртуализации Microsoft Applications.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-117">An MMC 3.0 snap-in management utility for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-118">Этот компонент можно установить на сервере Microsoft Application Virtualization или на отдельной рабочей станции с MMC 3.0 и. Установлено приложение NET 2.0.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-118">This component can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5d9dd-119">Веб-служба управления виртуализацией приложений Майкрософт</span><span class="sxs-lookup"><span data-stu-id="5d9dd-119">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-120">Компонент, который отвечает за взаимодействие запросов на чтение и запись в хранилище данных Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-120">The component responsible for communicating any read/write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-121">Этот компонент может быть установлен на сервере Microsoft Application Virtualization или на отдельном компьютере, на котором установлены службы IIS.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-121">This component can installed on the Microsoft Application Virtualization Server or on a separate computer with IIS installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5d9dd-122">Хранилище данных Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="5d9dd-122">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-123">Компонент, хранящийся в базе данных SQL и ответственный за хранение всей информации, связанной с инфраструктурой виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-123">The component stored in the SQL database and responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-124">Эти сведения включают все записи приложений, назначения приложений и группы, ответственные за управление средой виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-124">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5d9dd-125">Сервер потоковой передачи Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="5d9dd-125">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-126">Компонент, ответственный за размещение пакетов Application Virtualization для потоковой передачи клиентам в филиале, где ссылка на сервер управления виртуализацией приложений считается глобальной сетью.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-126">The component responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a WAN.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-127">Этот сервер содержит только потоковую функциональность и не предоставляет ни консоль управления Application Virtualization, ни веб-службу управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-127">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5d9dd-128">Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="5d9dd-128">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-129">Компонент, который используется для мониторинга и сохранения установки приложений для создания виртуальных пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-129">The component used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-130">Вывод состоит из значков приложения, OSD-файла, содержащего сведения о определении пакета, файла манифеста пакета и SFT-файла, содержащего файлы содержимого программы приложения.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-130">Output consists of the application’s icons, an OSD file containing package definition information, a package manifest file, and the SFT file containing the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5d9dd-131">Клиент Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="5d9dd-131">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-132">Компонент, установленный в классическом клиенте Application Virtualization или в клиенте Application Virtualization для служб удаленных рабочих столов (ранее — службы терминалов) и предоставляющий виртуальную среду для виртуализированных приложений.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-132">The component installed on the Application Virtualization Desktop Client or on the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services) and that provides the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d9dd-133">Клиент Microsoft Application Virtualization управляет потоковой передачей пакета в кэш, обновлять публикацию, транспортировку и все взаимодействие с серверами Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-133">The Microsoft Application Virtualization Client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization Servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5d9dd-134">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5d9dd-134">Related topics</span></span>


[<span data-ttu-id="5d9dd-135">Сценарий на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="5d9dd-135">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="5d9dd-136">Планирование решения для потоковой передачи при внедрении на основе сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="5d9dd-136">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[<span data-ttu-id="5d9dd-137">Публикация виртуальных приложений с помощью серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="5d9dd-137">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





