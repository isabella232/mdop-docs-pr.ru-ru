---
title: Запуск отчета
description: Запуск отчета
author: dansimp
ms.assetid: 72a5419b-aa65-4e60-b23e-3751186b7aed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739d8e2c86a2264dc8194b507eebf19b7ee88328
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816719"
---
# <span data-ttu-id="e0e71-103">Запуск отчета</span><span class="sxs-lookup"><span data-stu-id="e0e71-103">How to Run a Report</span></span>


<span data-ttu-id="e0e71-104">Процесс запуска отчета не зависит от типа отчета.</span><span class="sxs-lookup"><span data-stu-id="e0e71-104">The process for running a report is the same regardless of the report type.</span></span> <span data-ttu-id="e0e71-105">При выборе типа отчета в консоли управления сервером Application Virtualization в окне отображается краткое описание выбранного отчета.</span><span class="sxs-lookup"><span data-stu-id="e0e71-105">When you select a report type in the Application Virtualization Server Management Console, the window displays a brief description of the selected report.</span></span>

<span data-ttu-id="e0e71-106">**Примечание**  Отчеты не выполняются автоматически. для создания выходных данных необходимо явным образом выполнить их.</span><span class="sxs-lookup"><span data-stu-id="e0e71-106">**Note** Reports are not run automatically; you must run them explicitly to generate output data.</span></span> <span data-ttu-id="e0e71-107">Время, необходимое для выполнения отчета, определяется объемом данных, собранных в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="e0e71-107">The length of time it takes to run a report is determined by the amount of data collected in the data store.</span></span>

 

**<span data-ttu-id="e0e71-108">Запуск отчета</span><span class="sxs-lookup"><span data-stu-id="e0e71-108">To run a report</span></span>**

1.  <span data-ttu-id="e0e71-109">В области навигации щелкните узел **отчеты** .</span><span class="sxs-lookup"><span data-stu-id="e0e71-109">Click the **Reports** node in the navigation pane.</span></span>

2.  <span data-ttu-id="e0e71-110">Щелкните нужный отчет правой кнопкой мыши и выберите в контекстном меню команду **выполнить отчет** .</span><span class="sxs-lookup"><span data-stu-id="e0e71-110">Right-click the desired report, and select **Run Report** from the pop-up menu.</span></span>

3.  <span data-ttu-id="e0e71-111">Страницы, которые необходимо выполнить для отчета, зависят от типа отчета.</span><span class="sxs-lookup"><span data-stu-id="e0e71-111">The pages you must complete to run a report vary depending on the type of report.</span></span> <span data-ttu-id="e0e71-112">Чтобы запустить отчет, заполните соответствующие страницы из следующего списка:</span><span class="sxs-lookup"><span data-stu-id="e0e71-112">To run a report, complete the appropriate pages from the following list:</span></span>

    1.  <span data-ttu-id="e0e71-113">Выберите переключатель **отчетный период** , чтобы указать частоту выполнения отчета.</span><span class="sxs-lookup"><span data-stu-id="e0e71-113">Select a **Report Period** radio button to specify the frequency for running the report.</span></span>

    2.  <span data-ttu-id="e0e71-114">Укажите дату начала и дату окончания в соответствующих полях, чтобы определить диапазон дат, включенных в отчет.</span><span class="sxs-lookup"><span data-stu-id="e0e71-114">Specify the start date and end date in the respective fields to determine the range of dates included in the report.</span></span> <span data-ttu-id="e0e71-115">Вы можете ввести эти даты вручную или воспользоваться функцией календаря и выбрать нужные даты.</span><span class="sxs-lookup"><span data-stu-id="e0e71-115">You can enter these dates manually or use the calendar function and select the dates.</span></span>

    3.  <span data-ttu-id="e0e71-116">Выберите пункт **сервер**, **Группа серверов**или **Корпоративный** переключатель, а затем выберите серверную группу и сервер из соответствующего раскрывающегося списка и поле включена.</span><span class="sxs-lookup"><span data-stu-id="e0e71-116">Select the **Server**, **Server Group**, or **Enterprise** radio button, and then select the server group and server from the corresponding drop-down list and field as enabled.</span></span>

    4.  <span data-ttu-id="e0e71-117">Выберите нужное приложение из раскрывающегося списка приложений.</span><span class="sxs-lookup"><span data-stu-id="e0e71-117">Select the desired application from the drop-down list of applications.</span></span>

4.  <span data-ttu-id="e0e71-118">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="e0e71-118">Click **Finish**.</span></span>

## <span data-ttu-id="e0e71-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e0e71-119">Related topics</span></span>


[<span data-ttu-id="e0e71-120">Типы отчетов Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="e0e71-120">Application Virtualization Report Types</span></span>](application-virtualization-report-types.md)

[<span data-ttu-id="e0e71-121">Создание отчета</span><span class="sxs-lookup"><span data-stu-id="e0e71-121">How to Create a Report</span></span>](how-to-create-a-reportserver.md)

[<span data-ttu-id="e0e71-122">Удаление отчета</span><span class="sxs-lookup"><span data-stu-id="e0e71-122">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)

[<span data-ttu-id="e0e71-123">Экспорт отчета</span><span class="sxs-lookup"><span data-stu-id="e0e71-123">How to Export a Report</span></span>](how-to-export-a-reportserver.md)

[<span data-ttu-id="e0e71-124">Печать отчета</span><span class="sxs-lookup"><span data-stu-id="e0e71-124">How to Print a Report</span></span>](how-to-print-a-reportserver.md)

 

 





