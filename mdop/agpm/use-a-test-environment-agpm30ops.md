---
title: Использование тестовой среды
description: Использование тестовой среды
author: dansimp
ms.assetid: 86295084-b39e-4040-bb3f-15c3c1e99b1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1264d9fe6f922a7e61bcd069581c7bd5e39b7787
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818239"
---
# <span data-ttu-id="e5cac-103">Использование тестовой среды</span><span class="sxs-lookup"><span data-stu-id="e5cac-103">Use a Test Environment</span></span>


<span data-ttu-id="e5cac-104">Если вы используете проверочное подразделение (OU) для тестирования объектов групповой политики (GPO) перед развертыванием в рабочей среде, для доступа к тестовому подразделению необходимы соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="e5cac-104">If you use a testing organizational unit (OU) to test Group Policy Objects (GPOs) before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="e5cac-105">Использование тестового подразделений является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e5cac-105">The use of a test OU is optional.</span></span>

**<span data-ttu-id="e5cac-106">Использование тестового подразделения</span><span class="sxs-lookup"><span data-stu-id="e5cac-106">To use a test OU</span></span>**

1.  <span data-ttu-id="e5cac-107">Несмотря на то, что объект групповой политики извлечен для редактирования, в **консоли управления групповыми политиками**нажмите кнопку **объекты групповой политики** в лесу и домене, в которых вы управляете объектами GPO.</span><span class="sxs-lookup"><span data-stu-id="e5cac-107">While you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="e5cac-108">Щелкните извлеченную копию объекта групповой политики, который нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="e5cac-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="e5cac-109">Имя будет начинаться с **\ [извлечено \]**.</span><span class="sxs-lookup"><span data-stu-id="e5cac-109">The name will be preceded with **\[Checked Out\]**.</span></span> <span data-ttu-id="e5cac-110">(Если он не указан в списке, нажмите кнопку **действие**, а затем — **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="e5cac-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="e5cac-111">Сортировка имен в алфавитном порядке и **\ [извлечено \]** GPO обычно отображаются в верхней части списка.)</span><span class="sxs-lookup"><span data-stu-id="e5cac-111">Sort the names alphabetically, and **\[Checked Out\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="e5cac-112">Перетащите GPO в проверочное подразделение.</span><span class="sxs-lookup"><span data-stu-id="e5cac-112">Drag and drop the GPO to the test OU.</span></span>

4.  <span data-ttu-id="e5cac-113">Нажмите кнопку **ОК** в диалоговом окне с вопросом, нужно ли создать ссылку на объект групповой политики в тестовом подразделении.</span><span class="sxs-lookup"><span data-stu-id="e5cac-113">Click **OK** in the dialog box asking whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="e5cac-114">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="e5cac-114">Additional considerations</span></span>

-   <span data-ttu-id="e5cac-115">После того как тестирование будет завершено, при возврате объекта групповой политики автоматически удаляется ссылка на извлеченную копию объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="e5cac-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="e5cac-116">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="e5cac-116">Additional references</span></span>

-   [<span data-ttu-id="e5cac-117">Изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="e5cac-117">Editing a GPO</span></span>](editing-a-gpo-agpm30ops.md)

 

 





