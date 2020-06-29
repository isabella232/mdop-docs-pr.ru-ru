---
title: Вкладка "Общие" свойств Application Virtualization
description: Вкладка "Общие" свойств Application Virtualization
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819689"
---
# <span data-ttu-id="e3837-103">Свойства Application Virtualization: вкладка "Общие"</span><span class="sxs-lookup"><span data-stu-id="e3837-103">Application Virtualization Properties: General Tab</span></span>


<span data-ttu-id="e3837-104">Вкладка " **Общие** " в диалоговом окне " **свойства Application Virtualization** " используется для изменения параметров журнала и местоположений данных.</span><span class="sxs-lookup"><span data-stu-id="e3837-104">Use the **General** tab of the **Application Virtualization Properties** dialog box to modify log settings and data locations.</span></span>

<span data-ttu-id="e3837-105">На этой вкладке есть указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="e3837-105">This tab contains the following elements.</span></span>

<a href="" id="log-level"></a>**<span data-ttu-id="e3837-106">Уровень ведения журнала</span><span class="sxs-lookup"><span data-stu-id="e3837-106">Log Level</span></span>**  
<span data-ttu-id="e3837-107">Выберите уровень из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="e3837-107">Select the level from the drop-down list.</span></span> <span data-ttu-id="e3837-108">Уровень по умолчанию — **сведения**.</span><span class="sxs-lookup"><span data-stu-id="e3837-108">The default level is **Information**.</span></span>

<a href="" id="reset-log"></a>**<span data-ttu-id="e3837-109">Сброс журнала</span><span class="sxs-lookup"><span data-stu-id="e3837-109">Reset Log</span></span>**  
<span data-ttu-id="e3837-110">Нажмите эту кнопку, чтобы создать резервную копию текущего файла журнала и сразу же запустить новый файл.</span><span class="sxs-lookup"><span data-stu-id="e3837-110">Click this button to back up the current log file and immediately start a new log file.</span></span>

<a href="" id="location"></a>**<span data-ttu-id="e3837-111">Location</span><span class="sxs-lookup"><span data-stu-id="e3837-111">Location</span></span>**  
<span data-ttu-id="e3837-112">Введите или перейдите в папку, в которой вы хотите сохранить файл журнала sftlog.txt.</span><span class="sxs-lookup"><span data-stu-id="e3837-112">Enter or browse to the location where you want to save the log file sftlog.txt.</span></span> <span data-ttu-id="e3837-113">Ниже указаны расположения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e3837-113">The default locations are as follows:</span></span>

-   <span data-ttu-id="e3837-114">Для WindowsXP, Windows server2003 —*C:\\Documents и Settings\\All Users\\Application Data\\Microsoft\\Application виртуализация*</span><span class="sxs-lookup"><span data-stu-id="e3837-114">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="e3837-115">Для Windows Vista, Windows 7, Windows Server2008 —*клиент виртуализации C:\\ProgramData\\Microsoft\\Application*</span><span class="sxs-lookup"><span data-stu-id="e3837-115">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="system-log-level"></a>**<span data-ttu-id="e3837-116">Уровень ведения журнала системы</span><span class="sxs-lookup"><span data-stu-id="e3837-116">System Log Level</span></span>**  
<span data-ttu-id="e3837-117">Выберите уровень из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="e3837-117">Select the level from the drop-down list.</span></span> <span data-ttu-id="e3837-118">Уровень по умолчанию — **предупреждение**.</span><span class="sxs-lookup"><span data-stu-id="e3837-118">The default level is **Warning**.</span></span>

<span data-ttu-id="e3837-119">**Примечание**  Параметр **уровня системного журнала** определяет уровень сообщений, отправляемых в журнал событий системы.</span><span class="sxs-lookup"><span data-stu-id="e3837-119">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="e3837-120">Журнальные сообщения идентичны сообщениям, которые регистрируются в журнале событий клиента, но сохраняются в другом расположении, не имеющем ограничений на место в журнале событий клиента.</span><span class="sxs-lookup"><span data-stu-id="e3837-120">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location that does not have the space limitations of the client event log.</span></span> <span data-ttu-id="e3837-121">Поскольку системный журнал событий не имеет ограничений на место, лучше подходит для случаев, когда требуется подробный журнал.</span><span class="sxs-lookup"><span data-stu-id="e3837-121">Because the system event log does not have space limitations, it is ideally suited for situations where verbose logging is necessary.</span></span>

 

<a href="" id="global-data-directory"></a>**<span data-ttu-id="e3837-122">Глобальный каталог данных</span><span class="sxs-lookup"><span data-stu-id="e3837-122">Global Data Directory</span></span>**  
<span data-ttu-id="e3837-123">Введите или перейдите в папку, в которой находится файл журнала.</span><span class="sxs-lookup"><span data-stu-id="e3837-123">Enter or browse to the location of the directory of the log file.</span></span> <span data-ttu-id="e3837-124">Ниже указаны расположения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e3837-124">The default locations are as follows:</span></span>

-   <span data-ttu-id="e3837-125">Для WindowsXP, Windows server2003 —*C:\\Documents и Settings\\All Users\\Application Data\\Microsoft\\Application виртуализация*</span><span class="sxs-lookup"><span data-stu-id="e3837-125">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="e3837-126">Для Windows Vista, Windows 7, Windows Server2008 —*клиент виртуализации C:\\ProgramData\\Microsoft\\Application*</span><span class="sxs-lookup"><span data-stu-id="e3837-126">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="user-data-directory"></a>**<span data-ttu-id="e3837-127">Каталог данных пользователя</span><span class="sxs-lookup"><span data-stu-id="e3837-127">User Data Directory</span></span>**  
<span data-ttu-id="e3837-128">Введите путь к каталогу, в котором хранятся пользовательские данные, или перейдите к нему.</span><span class="sxs-lookup"><span data-stu-id="e3837-128">Enter or browse to the location of the directory where user-specific data is stored.</span></span> <span data-ttu-id="e3837-129">Значением по умолчанию является% APPDATA%.</span><span class="sxs-lookup"><span data-stu-id="e3837-129">The default is %APPDATA%.</span></span> <span data-ttu-id="e3837-130">Этот путь должен быть действительной переменной среды на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="e3837-130">This path must be a valid environment variable on the client computer.</span></span>

## <span data-ttu-id="e3837-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e3837-131">Related topics</span></span>


[<span data-ttu-id="e3837-132">Консоль управления клиентами: свойства Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="e3837-132">Client Management Console: Application Virtualization Properties</span></span>](client-management-console-application-virtualization-properties.md)

 

 





