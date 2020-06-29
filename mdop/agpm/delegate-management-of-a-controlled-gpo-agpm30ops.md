---
title: Передача прав управления управляемым объектом групповой политики
description: Передача прав управления управляемым объектом групповой политики
author: dansimp
ms.assetid: 509b02e7-ce0b-4919-b58a-c3a33051152e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d34231f25c172951cd0176b3e490dab84b98f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818719"
---
# <span data-ttu-id="ee22f-103">Передача прав управления управляемым объектом групповой политики</span><span class="sxs-lookup"><span data-stu-id="ee22f-103">Delegate Management of a Controlled GPO</span></span>


<span data-ttu-id="ee22f-104">Утверждающий может делегировать управление управляемым объектом групповой политики (GPO), который был создан этим утверждающим.</span><span class="sxs-lookup"><span data-stu-id="ee22f-104">An Approver can delegate the management of a controlled Group Policy Object (GPO) that was created by that Approver.</span></span> <span data-ttu-id="ee22f-105">Как и Администратор расширенного управления групповыми политиками (полный доступ), утверждающий может делегировать доступ к такому объекту групповой политики, чтобы выбранные редакторы могли редактировать его, рецензенты могут проверить его, а другие утверждающие могут утвердить его.</span><span class="sxs-lookup"><span data-stu-id="ee22f-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO so that selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="ee22f-106">По умолчанию утверждающий не может делегировать доступ к GPO, созданному другим администратором групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ee22f-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="ee22f-107">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора РАСШИРЕНного управления правами (полного доступа), учетная запись пользователя утверждающего, создавшего GPO, или учетная запись пользователя с необходимыми разрешениями для расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="ee22f-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="ee22f-108">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="ee22f-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="ee22f-109">Делегирование управления управляемым объектом групповой политики</span><span class="sxs-lookup"><span data-stu-id="ee22f-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="ee22f-110">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ee22f-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ee22f-111">На вкладке **содержимое** в области сведений откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики, а затем выберите GPO для делегирования.</span><span class="sxs-lookup"><span data-stu-id="ee22f-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="ee22f-112">Чтобы добавить доступ для пользователя или группы, нажмите кнопку **Добавить** , выберите пользователя или группу и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ee22f-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="ee22f-113">В диалоговом окне **Добавление группы или пользователя** выберите роль и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ee22f-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="ee22f-114">Чтобы удалить доступ для пользователя или группы, выберите пользователя или группу, а затем нажмите кнопку **Удалить** .</span><span class="sxs-lookup"><span data-stu-id="ee22f-114">To remove access for a user or group, select the user or group, and then click the **Remove** button.</span></span>

        <span data-ttu-id="ee22f-115">**Примечание**  Если пользователь или группа наследуют доступ к домену, кнопка " **Удалить** " недоступна.</span><span class="sxs-lookup"><span data-stu-id="ee22f-115">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="ee22f-116">Вы можете изменить доступ на уровне домена на вкладке " **Делегирование домена** ".</span><span class="sxs-lookup"><span data-stu-id="ee22f-116">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="ee22f-117">Чтобы изменить роли и разрешения, делегированные пользователю или группе, нажмите кнопку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="ee22f-117">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="ee22f-118">В диалоговом окне **разрешения** выберите пользователя или группу, установите флажки для всех ролей, которые необходимо назначить этому пользователю или группе, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ee22f-118">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="ee22f-119">**Примечание**  В редактор и утверждающие есть разрешения на просмотр.</span><span class="sxs-lookup"><span data-stu-id="ee22f-119">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="ee22f-120">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="ee22f-120">Additional considerations</span></span>

-   <span data-ttu-id="ee22f-121">По умолчанию для выполнения этой процедуры необходимо быть утверждающее, которое создало или управляло объектом групповой политики или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="ee22f-121">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="ee22f-122">В частности, необходимо иметь разрешение на доступ к **содержимому** для домена и **изменить разрешение безопасности** для этого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ee22f-122">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="ee22f-123">Для делегирования доступа на чтение для администраторов групповой политики, использующих многогрупповую политику, необходимо предоставить им **содержимое списка** и разрешения на **Чтение параметров** .</span><span class="sxs-lookup"><span data-stu-id="ee22f-123">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="ee22f-124">Это позволит им просматривать объекты групповой политики на вкладке " **содержимое** " в режиме расширенного использования.</span><span class="sxs-lookup"><span data-stu-id="ee22f-124">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="ee22f-125">Другие разрешения должны быть явным образом делегированы.</span><span class="sxs-lookup"><span data-stu-id="ee22f-125">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="ee22f-126">Редакторы должны иметь разрешение на **Чтение** для развернутой копии GPO, чтобы полностью использовать установку программного обеспечения групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ee22f-126">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

### <span data-ttu-id="ee22f-127">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="ee22f-127">Additional references</span></span>

-   [<span data-ttu-id="ee22f-128">Создание, администрирование и импорт объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="ee22f-128">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 





