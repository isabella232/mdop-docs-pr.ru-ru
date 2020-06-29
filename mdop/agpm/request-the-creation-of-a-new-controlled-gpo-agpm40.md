---
title: Запрос на создание нового управляемого объекта групповой политики
description: Запрос на создание нового управляемого объекта групповой политики
author: dansimp
ms.assetid: cb265238-386f-4780-a59a-0c9a4a87d736
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 85a435f84e055013c5100a720377f4bffaef4319
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820319"
---
# <span data-ttu-id="468db-103">Запрос на создание нового управляемого объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="468db-103">Request the Creation of a New Controlled GPO</span></span>


<span data-ttu-id="468db-104">Если вы не являетесь утверждающим или администратором РАСШИРЕНного управления правами (полный доступ), необходимо запросить создание нового объекта групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="468db-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the creation of a new Group Policy Object (GPO).</span></span>

<span data-ttu-id="468db-105">Для выполнения этой процедуры требуется учетная запись пользователя с редактором или ролью "рецензент" или "проверяющий" или необходимыми разрешениями в расширенном управлении групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="468db-105">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="468db-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="468db-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="468db-107">Создание объекта групповой политики с управлением изменениями с помощью РАСШИРЕНного управления</span><span class="sxs-lookup"><span data-stu-id="468db-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="468db-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="468db-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="468db-109">Щелкните правой кнопкой мыши **изменить элемент управления**, а затем выберите команду **создать управляемый объект групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="468db-109">Right-click **Change Control**, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="468db-110">Если у вас нет специального разрешения на создание GPO, необходимо отправить запрос на создание.</span><span class="sxs-lookup"><span data-stu-id="468db-110">Unless you have special permission to create GPOs, you must submit a request for creation.</span></span> <span data-ttu-id="468db-111">В диалоговом окне **новый управляемый объект групповой политики** :</span><span class="sxs-lookup"><span data-stu-id="468db-111">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="468db-112">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="468db-112">To receive a copy of the request, enter your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="468db-113">Введите имя для нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="468db-113">Type a name for the new GPO.</span></span>

    3.  <span data-ttu-id="468db-114">Необязательно: введите Примечание для нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="468db-114">Optional: Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="468db-115">Чтобы развернуть новый объект групповой политики в рабочей среде домена сразу после утверждения, нажмите кнопку **создать Live**.</span><span class="sxs-lookup"><span data-stu-id="468db-115">To deploy the new GPO to the production environment of the domain immediately upon approval, click **Create live**.</span></span> <span data-ttu-id="468db-116">Чтобы создать новый объект групповой политики в автономном режиме без немедленного развертывания после утверждения, нажмите кнопку **создать в автономном режиме**.</span><span class="sxs-lookup"><span data-stu-id="468db-116">To create the new GPO offline without immediately deploying it upon approval, click **Create offline**.</span></span>

    5.  <span data-ttu-id="468db-117">Выберите шаблон GPO, который будет использоваться в качестве отправной точки для нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="468db-117">Select the GPO template to use as a starting point for the new GPO.</span></span>

    6.  <span data-ttu-id="468db-118">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="468db-118">Click **Submit**.</span></span>

4.  <span data-ttu-id="468db-119">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="468db-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="468db-120">Новый объект групповой политики отображается в списке объектов групповой политики на вкладке **ожидающие** . Когда утверждающий утвердил ваш запрос, объект групповой политики будет перемещен на вкладку **Управление** .</span><span class="sxs-lookup"><span data-stu-id="468db-120">The new GPO is displayed in the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="468db-121">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="468db-121">Additional considerations</span></span>

-   <span data-ttu-id="468db-122">По умолчанию для выполнения этой процедуры необходимо быть редактором или рецензентом.</span><span class="sxs-lookup"><span data-stu-id="468db-122">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="468db-123">В частности, для домена требуется разрешение на доступ к **содержимому списка** .</span><span class="sxs-lookup"><span data-stu-id="468db-123">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="468db-124">Чтобы отказаться от запроса до его утверждения, откройте вкладку **ожидающие** . Щелкните объект групповой политики правой кнопкой мыши и выберите команду **снять**.</span><span class="sxs-lookup"><span data-stu-id="468db-124">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, then click **Withdraw**.</span></span> <span data-ttu-id="468db-125">Объект групповой политики будет удален.</span><span class="sxs-lookup"><span data-stu-id="468db-125">The GPO will be destroyed.</span></span>

### <span data-ttu-id="468db-126">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="468db-126">Additional references</span></span>

-   [<span data-ttu-id="468db-127">Создание и администрирование объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="468db-127">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

 

 





