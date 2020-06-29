---
title: Установка или отключение подготовки отчетов об использовании
description: Установка или отключение подготовки отчетов об использовании
author: dansimp
ms.assetid: 8587003a-128d-4b5d-ac70-5b9eddddd3dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f8f6c44d4060581f1ebe435875bc2f105cb93d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816549"
---
# <span data-ttu-id="00d39-103">Установка или отключение подготовки отчетов об использовании</span><span class="sxs-lookup"><span data-stu-id="00d39-103">How to Set Up or Disable Usage Reporting</span></span>


<span data-ttu-id="00d39-104">Ниже приведены процедуры, которые можно использовать в консоли управления сервером Application Virtualization для указания длительности (в месяцах) сведений об использовании системы Application Virtualization, которые нужно хранить в базе данных.</span><span class="sxs-lookup"><span data-stu-id="00d39-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the duration (in months) of Application Virtualization System usage information you want to store in the database.</span></span>

<span data-ttu-id="00d39-105">**Примечание**  Чтобы сохранить сведения об использовании, необходимо установить флажок **записывать данные об использовании** на вкладке **конвейер поставщика** . Чтобы отобразить эту вкладку, щелкните правой кнопкой мыши политику поставщика в области **результатов политик поставщика** и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="00d39-105">**Note** To store usage information, you must select the **Log Usage Information** check box on the **Provider Pipeline** tab. To display this tab, right-click the provider policy in the **Provider Policies Results** pane and select **Properties**.</span></span>

 

**<span data-ttu-id="00d39-106">Настройка отчетов об использовании</span><span class="sxs-lookup"><span data-stu-id="00d39-106">To set up usage reporting</span></span>**

1.  <span data-ttu-id="00d39-107">Щелкните правой кнопкой мыши узел системы Application Virtualization на левой панели и выберите пункт **Параметры системы**.</span><span class="sxs-lookup"><span data-stu-id="00d39-107">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="00d39-108">Откройте вкладку **база данных** .</span><span class="sxs-lookup"><span data-stu-id="00d39-108">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="00d39-109">Установите переключатель **сохранить использование (мес)** или **сохранить все использование** .</span><span class="sxs-lookup"><span data-stu-id="00d39-109">Select the **Keep Usage For (Months)** or **Keep All Usage** radio button.</span></span>

4.  <span data-ttu-id="00d39-110">Если вы укажете длительность использования в месяцах, введите число от 1 до 120 (значение по умолчанию — 6 месяцев).</span><span class="sxs-lookup"><span data-stu-id="00d39-110">If you choose to specify usage duration in months, enter a number from 1 to 120 (default value is 6 months).</span></span> <span data-ttu-id="00d39-111">Если выбрать **сохранить все использование**, база данных будет увеличиваться, пока не достигнет заданного предельного размера.</span><span class="sxs-lookup"><span data-stu-id="00d39-111">If you select **Keep All Usage**, the database will grow until it reaches the specified size limit.</span></span>

5.  <span data-ttu-id="00d39-112">Нажмите кнопку **Применить** или **ОК**.</span><span class="sxs-lookup"><span data-stu-id="00d39-112">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="00d39-113">Отключение отчетов об использовании</span><span class="sxs-lookup"><span data-stu-id="00d39-113">To disable usage reporting</span></span>**

1.  <span data-ttu-id="00d39-114">Щелкните узел **политики поставщика** .</span><span class="sxs-lookup"><span data-stu-id="00d39-114">Click the **Provider Policies** node.</span></span>

2.  <span data-ttu-id="00d39-115">Щелкните правой кнопкой мыши **политику поставщика** и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="00d39-115">Right-click **Provider Policy** and select **Properties**.</span></span>

3.  <span data-ttu-id="00d39-116">Перейдите на вкладку **поставщик конвейера** .</span><span class="sxs-lookup"><span data-stu-id="00d39-116">Select the **Provider Pipeline** tab.</span></span>

4.  <span data-ttu-id="00d39-117">Снимите флажок **Регистрация сведений об использовании** .</span><span class="sxs-lookup"><span data-stu-id="00d39-117">Clear the **Log Usage Information** check box.</span></span>

5.  <span data-ttu-id="00d39-118">Нажмите кнопку **Применить** или **ОК**.</span><span class="sxs-lookup"><span data-stu-id="00d39-118">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="00d39-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="00d39-119">Related topics</span></span>


[<span data-ttu-id="00d39-120">Настройка системы Application Virtualization на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="00d39-120">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="00d39-121">Установка или отключение определения размера базы данных</span><span class="sxs-lookup"><span data-stu-id="00d39-121">How to Set Up or Disable Database Size</span></span>](how-to-set-up-or-disable-database-size.md)

 

 





