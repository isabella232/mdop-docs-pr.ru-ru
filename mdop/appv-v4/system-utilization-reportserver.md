---
title: Отчет об использовании системы
description: Отчет об использовании системы
author: dansimp
ms.assetid: 4d490d15-2d1f-4f2c-99bb-0685447c0672
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe7ff547d969c63ace234104c3e6b7146da2c113
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815252"
---
# <span data-ttu-id="e1fb8-103">Отчет об использовании системы</span><span class="sxs-lookup"><span data-stu-id="e1fb8-103">System Utilization Report</span></span>


<span data-ttu-id="e1fb8-104">С помощью отчета об использовании системы можно выграфике общее ежедневное использование системы.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-104">Use the System Utilization Report to graph the total daily system usage.</span></span> <span data-ttu-id="e1fb8-105">Вы можете использовать этот отчет для определения нагрузки системы виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-105">You can use this report to determine the load on your Application Virtualization System.</span></span>

<span data-ttu-id="e1fb8-106">Этот отчет отслеживает использование с течением времени в течение отчетного периода для указанного сервера или группы сервера.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-106">This report tracks the usage over time during the reporting period for the specified server or for the server group.</span></span>

<span data-ttu-id="e1fb8-107">В отчете об использовании системы также отображаются следующие сведения об использовании системы:</span><span class="sxs-lookup"><span data-stu-id="e1fb8-107">The System Utilization Report also graphs the following system usage:</span></span>

-   <span data-ttu-id="e1fb8-108">Использование по дням недели</span><span class="sxs-lookup"><span data-stu-id="e1fb8-108">Usage by day of the week</span></span>

-   <span data-ttu-id="e1fb8-109">Использование по часам дня</span><span class="sxs-lookup"><span data-stu-id="e1fb8-109">Usage by hour of the day</span></span>

<span data-ttu-id="e1fb8-110">В отчете об использовании системы также выводятся сведения об общем использовании системы для конкретных пользователей и общего количества сеансов.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-110">The System Utilization Report also includes a summary of the total system usage for specific users and total session counts.</span></span>

<span data-ttu-id="e1fb8-111">При создании отчета указываются параметры, которые используются для сбора данных при выполнении отчета.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-111">When you create a report, you specify the parameters that are used for collecting the data when the report is run.</span></span>

<span data-ttu-id="e1fb8-112">Отчеты не выполняются автоматически. для создания выходных данных необходимо явным образом выполнить их.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-112">Reports are not run automatically; you must run them explicitly to generate output data.</span></span> <span data-ttu-id="e1fb8-113">Время, необходимое для выполнения этого отчета, определяется объемом данных, собранных в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-113">The length of time it takes to run this report is determined by the amount of data collected in the data store.</span></span>

<span data-ttu-id="e1fb8-114">После того как вы запустите отчет, и выходные данные отобразятся в консоли управления сервером Application Virtualization, вы можете экспортировать отчет в следующих форматах:</span><span class="sxs-lookup"><span data-stu-id="e1fb8-114">After you run a report and the output is displayed in the Application Virtualization Server Management Console, you can export the report into the following formats:</span></span>

-   <span data-ttu-id="e1fb8-115">Adobe Acrobat (PDF)</span><span class="sxs-lookup"><span data-stu-id="e1fb8-115">Adobe Acrobat (PDF)</span></span>

-   <span data-ttu-id="e1fb8-116">Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="e1fb8-116">Microsoft Office Excel</span></span>

<span data-ttu-id="e1fb8-117">**Примечание**  Имя сервера App-V, отправленное из клиентов, должно входить в группу сервера по умолчанию, чтобы отчет об использовании системы отображал данные.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-117">**Note** The App-V server name reported from the clients must be part of the Default Server Group in order for the System Utilization report to show data.</span></span> <span data-ttu-id="e1fb8-118">Например, если вы используете несколько серверов с балансировкой сетевой нагрузки (NLB), необходимо добавить имя кластера NLB в группу серверов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-118">For example, if you are using multiple servers with a Network Load Balancer (NLB), you must add the NLB cluster name to the Default Server Group.</span></span>

 

## <span data-ttu-id="e1fb8-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e1fb8-119">Related topics</span></span>


[<span data-ttu-id="e1fb8-120">Создание отчета</span><span class="sxs-lookup"><span data-stu-id="e1fb8-120">How to Create a Report</span></span>](how-to-create-a-reportserver.md)

[<span data-ttu-id="e1fb8-121">Удаление отчета</span><span class="sxs-lookup"><span data-stu-id="e1fb8-121">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)

[<span data-ttu-id="e1fb8-122">Экспорт отчета</span><span class="sxs-lookup"><span data-stu-id="e1fb8-122">How to Export a Report</span></span>](how-to-export-a-reportserver.md)

[<span data-ttu-id="e1fb8-123">Печать отчета</span><span class="sxs-lookup"><span data-stu-id="e1fb8-123">How to Print a Report</span></span>](how-to-print-a-reportserver.md)

[<span data-ttu-id="e1fb8-124">Запуск отчета</span><span class="sxs-lookup"><span data-stu-id="e1fb8-124">How to Run a Report</span></span>](how-to-run-a-reportserver.md)

 

 





