---
title: Использование тестовой среды
description: Использование тестовой среды
author: dansimp
ms.assetid: b8d7b3ee-030a-4b5b-8223-4a3276fd47a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2299fb6eaf7c75f6841056f67a05fe025ea19bb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818232"
---
# <span data-ttu-id="a6efe-103">Использование тестовой среды</span><span class="sxs-lookup"><span data-stu-id="a6efe-103">Use a Test Environment</span></span>


<span data-ttu-id="a6efe-104">Если вы используете проверочное подразделение (OU) для тестирования объектов групповой политики (GPO) перед развертыванием в рабочей среде, для доступа к тестовому подразделению необходимы соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="a6efe-104">If you use a testing organizational unit (OU) to test Group Policy objects (GPOs) before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="a6efe-105">Использование тестового подразделений является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a6efe-105">The use of a test OU is optional.</span></span>

**<span data-ttu-id="a6efe-106">Использование тестового подразделения</span><span class="sxs-lookup"><span data-stu-id="a6efe-106">To use a test OU</span></span>**

1.  <span data-ttu-id="a6efe-107">Несмотря на то, что объект групповой политики извлечен для редактирования, в **консоли управления групповыми политиками**нажмите кнопку **объекты групповой политики** в лесу и домене, в которых вы управляете объектами GPO.</span><span class="sxs-lookup"><span data-stu-id="a6efe-107">While you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="a6efe-108">Щелкните извлеченную копию объекта групповой политики, который нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="a6efe-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="a6efe-109">Имя будет начинаться с **\ [расширенного именования \]**.</span><span class="sxs-lookup"><span data-stu-id="a6efe-109">The name will be preceded with **\[AGPM\]**.</span></span> <span data-ttu-id="a6efe-110">(Если он не указан в списке, нажмите кнопку **действие**, а затем — **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="a6efe-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="a6efe-111">Отсортируйте имена в алфавитном порядке, а **\ [групповой политики \ \ список (расширенная версия)** , как правило, будет отображаться в верхней части списка.)</span><span class="sxs-lookup"><span data-stu-id="a6efe-111">Sort the names alphabetically, and **\[AGPM\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="a6efe-112">Перетащите GPO в проверочное подразделение.</span><span class="sxs-lookup"><span data-stu-id="a6efe-112">Drag and drop the GPO to the test OU.</span></span>

4.  <span data-ttu-id="a6efe-113">Нажмите кнопку **ОК** в диалоговом окне с вопросом, нужно ли создать ссылку на объект групповой политики в тестовом подразделении.</span><span class="sxs-lookup"><span data-stu-id="a6efe-113">Click **OK** in the dialog box asking whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="a6efe-114">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="a6efe-114">Additional considerations</span></span>

-   <span data-ttu-id="a6efe-115">После того как тестирование будет завершено, при возврате объекта групповой политики автоматически удаляется ссылка на извлеченную копию объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="a6efe-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="a6efe-116">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="a6efe-116">Additional references</span></span>

-   [<span data-ttu-id="a6efe-117">Изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="a6efe-117">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





