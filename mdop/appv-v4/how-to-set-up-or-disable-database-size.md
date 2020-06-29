---
title: Установка или отключение определения размера базы данных
description: Установка или отключение определения размера базы данных
author: dansimp
ms.assetid: 4abaf349-132d-4186-8873-a0e515593b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cbb041920e2680d51b01926f144eba595fe28d05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816562"
---
# <span data-ttu-id="47a35-103">Установка или отключение определения размера базы данных</span><span class="sxs-lookup"><span data-stu-id="47a35-103">How to Set Up or Disable Database Size</span></span>


<span data-ttu-id="47a35-104">Ниже приведены процедуры, которые можно использовать в консоли управления сервером Application Virtualization для указания размера (в МБ) использования системы Application Virtualization, которую нужно сохранить в базе данных.</span><span class="sxs-lookup"><span data-stu-id="47a35-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the size (in MB) of Application Virtualization System usage that you want to store in the database.</span></span>

<span data-ttu-id="47a35-105">Когда размер сохраненных данных достигает 95% (верхняя подложка) указанного предела, система удалит 10% данных об использовании, оставляя 85% данных.</span><span class="sxs-lookup"><span data-stu-id="47a35-105">When the size of the stored data reaches 95% (the high watermark) of the specified limit, the system will delete 10% of the usage data, leaving 85% of the data.</span></span> <span data-ttu-id="47a35-106">Данные об использовании пакетов и приложений будут удалены.</span><span class="sxs-lookup"><span data-stu-id="47a35-106">Package and application usage data will be deleted.</span></span> <span data-ttu-id="47a35-107">Если размер базы данных достаточен и приближается большая подложка, в журнал SQL Server отправляется предупреждение о том, что это ограничение достигнуто.</span><span class="sxs-lookup"><span data-stu-id="47a35-107">When the database grows large enough and approaches the high watermark, a warning message is sent to the SQL Server log to inform you that this limit has been reached.</span></span> <span data-ttu-id="47a35-108">Это предупреждение необходимо, так как действие очистки может повлиять на выходные данные отчетов.</span><span class="sxs-lookup"><span data-stu-id="47a35-108">This warning is necessary because the cleanup action can affect the output of the reports.</span></span> <span data-ttu-id="47a35-109">Кроме того, она поможет вам решить, нужно ли увеличивать максимальный размер базы данных, сократить количество месяцев на хранение данных об использовании или отключить уровень ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="47a35-109">It will also help you decide whether you need to increase the maximum database size, reduce the number of months of usage data to be kept, or turn down the logging level.</span></span>

<span data-ttu-id="47a35-110">**Примечание**  **Ограничения на размер не** доставляются, и вы можете отключить отчеты об **использовании и удаление** базы данных.</span><span class="sxs-lookup"><span data-stu-id="47a35-110">**Note** The **No Size Limit** and **Keep All Usage** options are provided so that you can disable usage reporting and database cleanup.</span></span> <span data-ttu-id="47a35-111">Если выбрать эти элементы, журнал транзакций базы данных также будет очищен.</span><span class="sxs-lookup"><span data-stu-id="47a35-111">Selecting these items will clean up the database transaction log as well.</span></span> <span data-ttu-id="47a35-112">(Все фиксированные транзакции Microsoft SQL Server будут удалены из журнала базы данных.)</span><span class="sxs-lookup"><span data-stu-id="47a35-112">(All committed Microsoft SQL Server transactions will be removed from the database log.)</span></span>

 

**<span data-ttu-id="47a35-113">Настройка размера базы данных</span><span class="sxs-lookup"><span data-stu-id="47a35-113">To set up database size</span></span>**

1.  <span data-ttu-id="47a35-114">Щелкните правой кнопкой мыши узел системы Application Virtualization на левой панели и выберите пункт **Параметры системы**.</span><span class="sxs-lookup"><span data-stu-id="47a35-114">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="47a35-115">Откройте вкладку **база данных** .</span><span class="sxs-lookup"><span data-stu-id="47a35-115">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="47a35-116">Выберите переключатель **максимальный размер базы данных (МБ)** или **нет ограничения размера** .</span><span class="sxs-lookup"><span data-stu-id="47a35-116">Select the **Maximum Database Size (MB)** or **No Size Limit** radio button.</span></span>

4.  <span data-ttu-id="47a35-117">Если вы укажете размер базы данных, рекомендуем ввести число в диапазоне от 512 до 4096 МБ.</span><span class="sxs-lookup"><span data-stu-id="47a35-117">If you choose to specify a database size, best practices recommend that you enter a number between 512 and 4096 MB.</span></span> <span data-ttu-id="47a35-118">Размер по умолчанию составляет 1024 МБ и, если требуется увеличивать размер базы данных, максимальное значение, которое можно ввести, — 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="47a35-118">The default size is 1024 MB and if you need to increase the database size, the maximum value you can enter is 2,147,483,647.</span></span> <span data-ttu-id="47a35-119">Если вы выберете параметр **без ограничения размера**, размер базы данных будет увеличиваться до тех пор, пока не достигнет предельного размера диска.</span><span class="sxs-lookup"><span data-stu-id="47a35-119">If you select **No Size Limit**, the database will grow until it reaches the disk size limit.</span></span>

5.  <span data-ttu-id="47a35-120">Нажмите кнопку **Применить** или **ОК**.</span><span class="sxs-lookup"><span data-stu-id="47a35-120">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="47a35-121">Чтобы отключить ограничения на размер базы данных</span><span class="sxs-lookup"><span data-stu-id="47a35-121">To disable database size limits</span></span>**

1.  <span data-ttu-id="47a35-122">Щелкните правой кнопкой мыши узел системы Application Virtualization в области **область** и выберите пункт **Параметры системы**.</span><span class="sxs-lookup"><span data-stu-id="47a35-122">Right-click the Application Virtualization System node in the **Scope** pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="47a35-123">Откройте вкладку **база данных** .</span><span class="sxs-lookup"><span data-stu-id="47a35-123">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="47a35-124">Установите флажок **не предельный размер и не** **забудьте все** переключатели использования.</span><span class="sxs-lookup"><span data-stu-id="47a35-124">Select the **No Size Limit** and **Keep All Usage** radio buttons.</span></span>

4.  <span data-ttu-id="47a35-125">Нажмите кнопку **Применить** или **ОК**.</span><span class="sxs-lookup"><span data-stu-id="47a35-125">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="47a35-126">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="47a35-126">Related topics</span></span>


[<span data-ttu-id="47a35-127">Настройка системы Application Virtualization на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="47a35-127">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="47a35-128">Установка или отключение подготовки отчетов об использовании</span><span class="sxs-lookup"><span data-stu-id="47a35-128">How to Set Up or Disable Usage Reporting</span></span>](how-to-set-up-or-disable-usage-reporting.md)

 

 





