---
title: Откат к предыдущей версии объекта групповой политики
description: Откат к предыдущей версии объекта групповой политики
author: dansimp
ms.assetid: 2a98ad8f-32cb-41eb-ab99-0318f2a55d81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 715f70ad6e87a0b2fa463426d4f6a8955250e446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820289"
---
# <span data-ttu-id="38747-103">Откат к предыдущей версии объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="38747-103">Roll Back to a Previous Version of a GPO</span></span>


<span data-ttu-id="38747-104">Утверждающий может откатить изменения объекта групповой политики (GPO), повторно развертывая более раннюю версию GPO из ее истории.</span><span class="sxs-lookup"><span data-stu-id="38747-104">An Approver can roll back changes to a Group Policy Object (GPO) by redeploying an earlier version of the GPO from its history.</span></span> <span data-ttu-id="38747-105">Развертывание более ранней версии объекта групповой политики перезапишет версию объекта групповой политики, которая в данный момент находится в производстве.</span><span class="sxs-lookup"><span data-stu-id="38747-105">Deploying an earlier version of a GPO overwrites the version of the GPO currently in production.</span></span>

<span data-ttu-id="38747-106">Для выполнения этой процедуры необходимо использовать учетную запись пользователя с ролью "полный доступ" и "Администратор расширенного управления групповыми политиками (для опытных пользователей)" или необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="38747-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="38747-107">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="38747-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="38747-108">Развертывание предыдущей версии GPO в рабочей среде</span><span class="sxs-lookup"><span data-stu-id="38747-108">To deploy a previous version of a GPO to the production environment</span></span>**

1.  <span data-ttu-id="38747-109">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="38747-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="38747-110">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="38747-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="38747-111">Дважды щелкните объект групповой политики, который нужно развернуть, чтобы отобразить его **историю**.</span><span class="sxs-lookup"><span data-stu-id="38747-111">Double-click the GPO to be deployed to display its **History**.</span></span>

4.  <span data-ttu-id="38747-112">Щелкните правой кнопкой мыши версию, которую нужно развернуть, и выберите команду **развернуть**, а затем — **Да**.</span><span class="sxs-lookup"><span data-stu-id="38747-112">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

5.  <span data-ttu-id="38747-113">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="38747-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="38747-114">В окне **журнала** нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="38747-114">In the **History** window, click **Close**.</span></span>

<span data-ttu-id="38747-115">**Примечание**  Чтобы убедиться в том, что версия, которая была повторно реализована, соответствует версии, просмотрите отчет о различиях для двух версий.</span><span class="sxs-lookup"><span data-stu-id="38747-115">**Note** To verify that the version that has been redeployed matches the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="38747-116">В окне **журнала** для объекта групповой политики выделите две версии, а затем щелкните правой кнопкой мыши и выберите " **разница** " и "отчет **HTML** " или "отчет в формате **XML**".</span><span class="sxs-lookup"><span data-stu-id="38747-116">In the **History** window for the GPO, highlight the two versions, and then right-click and select **Difference** and either **HTML Report** or **XML Report**.</span></span>

 

### <span data-ttu-id="38747-117">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="38747-117">Additional considerations</span></span>

-   <span data-ttu-id="38747-118">По умолчанию для выполнения этой процедуры необходимо быть утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="38747-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="38747-119">В частности, необходимо иметь **содержимое списка** и **развернуть разрешения GPO** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="38747-119">Specifically, you must have **List Contents** and **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="38747-120">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="38747-120">Additional references</span></span>

-   [<span data-ttu-id="38747-121">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="38747-121">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

 

 





