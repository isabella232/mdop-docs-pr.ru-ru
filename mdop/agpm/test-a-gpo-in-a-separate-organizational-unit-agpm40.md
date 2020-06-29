---
title: Проверка объекта групповой политики в отдельном подразделении
description: Проверка объекта групповой политики в отдельном подразделении
author: dansimp
ms.assetid: 9a9e6d22-74e6-41d8-ac2f-12a1b76ad5a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 509721fdd775c8669399549f6dcc29cb9ebaea2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818259"
---
# <span data-ttu-id="d44de-103">Проверка объекта групповой политики в отдельном подразделении</span><span class="sxs-lookup"><span data-stu-id="d44de-103">Test a GPO in a Separate Organizational Unit</span></span>


<span data-ttu-id="d44de-104">Если вы используете тестовое подразделение (OU) для проверки объектов групповой политики (GPO) в пределах того же домена перед развертыванием в рабочей среде, необходимо иметь необходимые разрешения для доступа к проверочному подразделению.</span><span class="sxs-lookup"><span data-stu-id="d44de-104">If you use a testing organizational unit (OU) to test Group Policy Objects (GPOs) within the same domain before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="d44de-105">Использование тестового подразделения является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d44de-105">Using a test OU is optional.</span></span>

**<span data-ttu-id="d44de-106">Использование тестового подразделения</span><span class="sxs-lookup"><span data-stu-id="d44de-106">To use a test OU</span></span>**

1.  <span data-ttu-id="d44de-107">Несмотря на то, что объект групповой политики извлечен для редактирования, в **консоли управления групповыми политиками**нажмите кнопку **объекты групповой политики** в лесу и домене, в котором вы управляете объектами GPO.</span><span class="sxs-lookup"><span data-stu-id="d44de-107">Although you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="d44de-108">Щелкните извлеченную копию объекта групповой политики, который нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="d44de-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="d44de-109">Перед именем будет стоять " \**\ [расширенная политика \**".</span><span class="sxs-lookup"><span data-stu-id="d44de-109">The name will be preceded by **\[AGPM\]**.</span></span> <span data-ttu-id="d44de-110">(Если он не указан в списке, нажмите кнопку **действие**, а затем — **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="d44de-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="d44de-111">Отсортируйте имена в алфавитном порядке, а **\ [групповой политики \ \ список (расширенная версия)** , как правило, будет отображаться в верхней части списка.)</span><span class="sxs-lookup"><span data-stu-id="d44de-111">Sort the names alphabetically, and **\[AGPM\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="d44de-112">Перетащите GPO в проверочное подразделение.</span><span class="sxs-lookup"><span data-stu-id="d44de-112">Drag the GPO to the test OU.</span></span>

4.  <span data-ttu-id="d44de-113">Нажмите кнопку **ОК** в диалоговом окне с запросом на создание ссылки на объект групповой политики в тестовом подразделении.</span><span class="sxs-lookup"><span data-stu-id="d44de-113">Click **OK** in the dialog box that asks whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="d44de-114">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="d44de-114">Additional considerations</span></span>

-   <span data-ttu-id="d44de-115">После того как тестирование будет завершено, при возврате объекта групповой политики автоматически удаляется ссылка на извлеченную копию объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="d44de-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="d44de-116">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="d44de-116">Additional references</span></span>

-   [<span data-ttu-id="d44de-117">Использование тестовой среды</span><span class="sxs-lookup"><span data-stu-id="d44de-117">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





