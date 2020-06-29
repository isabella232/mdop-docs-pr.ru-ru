---
title: Запрос на развертывание объекта групповой политики
description: Запрос на развертывание объекта групповой политики
author: dansimp
ms.assetid: 9aa9af29-4754-4f72-b624-bb3e1087cbe1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a9e5fdbbd352adb6d542932c7180c513cfac8b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820379"
---
# <span data-ttu-id="2b61d-103">Запрос на развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="2b61d-103">Request Deployment of a GPO</span></span>


<span data-ttu-id="2b61d-104">После изменения и возврата объекта групповой политики (GPO) разверните этот объект, чтобы он вступил в силу в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="2b61d-104">After you have modified and checked in a Group Policy object (GPO), deploy the GPO, so it will take effect in the production environment.</span></span>

<span data-ttu-id="2b61d-105">Для выполнения этой процедуры требуется учетная запись пользователя с ролью "редактор" или необходимыми разрешениями для расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="2b61d-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="2b61d-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="2b61d-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="2b61d-107">Запрос развертывания объекта групповой политики в рабочей среде</span><span class="sxs-lookup"><span data-stu-id="2b61d-107">To request the deployment of a GPO to the production environment</span></span>**

1.  <span data-ttu-id="2b61d-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="2b61d-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2b61d-109">На вкладке **содержание** в области сведений откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="2b61d-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="2b61d-110">Щелкните правой кнопкой мыши объект групповой политики, который нужно развернуть, и выберите команду **развернуть**.</span><span class="sxs-lookup"><span data-stu-id="2b61d-110">Right-click the GPO to be deployed, and then click **Deploy**.</span></span>

4.  <span data-ttu-id="2b61d-111">Если вы не являетесь администратором или у вас нет специального разрешения на развертывание объектов групповой политики, необходимо отправить запрос на развертывание.</span><span class="sxs-lookup"><span data-stu-id="2b61d-111">Unless you are an Approver or AGPM Administrator or have special permission to deploy GPOs, you must submit a request for deployment.</span></span> <span data-ttu-id="2b61d-112">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="2b61d-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="2b61d-113">Введите Примечание, которое будет отображаться в **журнале** для объекта групповой политики, а затем нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="2b61d-113">Type a comment to be displayed in the **History** for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="2b61d-114">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="2b61d-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="2b61d-115">Объект групповой политики отображается в списке объектов групповой политики на вкладке **ожидающие** . Когда утверждающий утвердил ваш запрос, объект групповой политики будет перемещен с вкладки **ожидающие** на вкладку **управляемый** и будет развернут.</span><span class="sxs-lookup"><span data-stu-id="2b61d-115">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Controlled** tab and be deployed.</span></span>

### <span data-ttu-id="2b61d-116">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="2b61d-116">Additional considerations</span></span>

-   <span data-ttu-id="2b61d-117">Для выполнения этой процедуры необходимо быть редактором по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2b61d-117">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="2b61d-118">В частности, необходимо иметь **содержимое списка** и разрешения на **изменение параметров** для GPO.</span><span class="sxs-lookup"><span data-stu-id="2b61d-118">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="2b61d-119">Чтобы отменить запрос перед его утверждением, откройте вкладку **Ожидание** . Щелкните объект групповой политики правой кнопкой мыши и выберите команду **снять**.</span><span class="sxs-lookup"><span data-stu-id="2b61d-119">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="2b61d-120">Объект групповой политики будет возвращен на вкладку " **управляемые** ".</span><span class="sxs-lookup"><span data-stu-id="2b61d-120">The GPO will be returned to the **Controlled** tab.</span></span>

### <span data-ttu-id="2b61d-121">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="2b61d-121">Additional references</span></span>

-   [<span data-ttu-id="2b61d-122">Изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="2b61d-122">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





