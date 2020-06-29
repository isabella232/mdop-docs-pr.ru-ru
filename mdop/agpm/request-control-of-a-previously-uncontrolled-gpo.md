---
title: Запросить на управление ранее неуправляемым объектом групповой политики
description: Запросить на управление ранее неуправляемым объектом групповой политики
author: dansimp
ms.assetid: 00e8725d-5d7f-4eed-a5e6-c3631632cfbd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a92db48d87398568900fc0031e688c862a69b417
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818462"
---
# <span data-ttu-id="56430-103">Запросить на управление ранее неуправляемым объектом групповой политики</span><span class="sxs-lookup"><span data-stu-id="56430-103">Request Control of a Previously Uncontrolled GPO</span></span>


<span data-ttu-id="56430-104">Для использования расширенного управления групповыми политиками для предоставления управления изменениями для существующего объекта групповой политики (GPO) этот объект должен управляться с помощью РАСШИРЕНного контроля учетных элементов.</span><span class="sxs-lookup"><span data-stu-id="56430-104">To use Advanced Group Policy Management (AGPM) to provide change control for an existing Group Policy object (GPO), the GPO must be controlled with AGPM.</span></span> <span data-ttu-id="56430-105">Если вы не являетесь утверждающим или администратором РАСШИРЕНного управления правами (полный доступ), необходимо запросить управление объектом групповой политики.</span><span class="sxs-lookup"><span data-stu-id="56430-105">Unless you are an Approver or an AGPM Administrator (Full Control), you must request that the GPO be controlled.</span></span>

<span data-ttu-id="56430-106">Для выполнения этой процедуры требуется учетная запись пользователя с редактором или ролью "рецензент" или "проверяющий" или необходимыми разрешениями в расширенном управлении групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="56430-106">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="56430-107">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="56430-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="56430-108">Управление ранее неуправлениым объектом групповой политики</span><span class="sxs-lookup"><span data-stu-id="56430-108">To control a previously uncontrolled GPO</span></span>**

1.  <span data-ttu-id="56430-109">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="56430-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="56430-110">На вкладке **содержание** в области сведений щелкните вкладку **неконтрольные** значения, чтобы отобразить неконтрольные объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="56430-110">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="56430-111">Щелкните правой кнопкой мыши объект групповой политики, для которого нужно настроить управление групповыми политиками, и выберите пункт **элемент управления**.</span><span class="sxs-lookup"><span data-stu-id="56430-111">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="56430-112">Если у вас нет специального разрешения на управление объектами групповой политики, необходимо отправить запрос на управление.</span><span class="sxs-lookup"><span data-stu-id="56430-112">Unless you have special permission to control GPOs, you must submit a request for control.</span></span> <span data-ttu-id="56430-113">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="56430-113">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="56430-114">Введите Примечание, которое будет отображаться в **журнале** объекта групповой политики, а затем нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="56430-114">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="56430-115">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="56430-115">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="56430-116">Объект групповой политики удаляется из списка на вкладке " **неконтрольные элементы** " и добавляется на вкладку " **отложенные** ". Когда утверждающий утвердил ваш запрос, объект групповой политики будет перемещен на вкладку **Управление** .</span><span class="sxs-lookup"><span data-stu-id="56430-116">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="56430-117">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="56430-117">Additional considerations</span></span>

-   <span data-ttu-id="56430-118">По умолчанию для выполнения этой процедуры необходимо быть редактором или рецензентом.</span><span class="sxs-lookup"><span data-stu-id="56430-118">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="56430-119">В частности, необходимо иметь **содержимое списка** и **прочитать параметры** разрешений для домена.</span><span class="sxs-lookup"><span data-stu-id="56430-119">Specifically, you must have **List Contents** and **Read Settings** permissions for the domain.</span></span>

-   <span data-ttu-id="56430-120">Чтобы отменить запрос перед его утверждением, откройте вкладку **Ожидание** . Щелкните объект групповой политики правой кнопкой мыши и выберите команду **снять**.</span><span class="sxs-lookup"><span data-stu-id="56430-120">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="56430-121">Объект GPO будет возвращен на вкладку **uncontrols** .</span><span class="sxs-lookup"><span data-stu-id="56430-121">The GPO will be returned to the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="56430-122">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="56430-122">Additional references</span></span>

-   [<span data-ttu-id="56430-123">Создание, администрирование и импорт объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="56430-123">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor.md)

 

 





