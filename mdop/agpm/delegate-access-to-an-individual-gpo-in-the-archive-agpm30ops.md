---
title: Передача прав доступа для отдельного объекта групповой политики в архиве
description: Передача прав доступа для отдельного объекта групповой политики в архиве
author: dansimp
ms.assetid: 7b37b188-2b6b-4e52-be97-8ef899e9893b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 592937a28b0e2556991b0c338b88b2cfa88ba83d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818769"
---
# <span data-ttu-id="ed53e-103">Передача прав доступа для отдельного объекта групповой политики в архиве</span><span class="sxs-lookup"><span data-stu-id="ed53e-103">Delegate Access to an Individual GPO in the Archive</span></span>


<span data-ttu-id="ed53e-104">Как Администратор расширенного управления групповыми политиками (полный доступ) вы можете делегировать управление управляемым объектом групповой политики (GPO) в архиве, чтобы выбранные группы и редакторы могли редактировать их, рецензенты смогут проверить ее, а утверждающие могут утвердить ее.</span><span class="sxs-lookup"><span data-stu-id="ed53e-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy Object (GPO) in the archive so that selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="ed53e-105">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора РАСШИРЕНного управления правами (полного доступа), учетная запись пользователя утверждающего, создавшего GPO, или учетная запись пользователя с необходимыми разрешениями для расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="ed53e-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="ed53e-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="ed53e-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="ed53e-107">Делегирование управления управляемым объектом групповой политики</span><span class="sxs-lookup"><span data-stu-id="ed53e-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="ed53e-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ed53e-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ed53e-109">На вкладке **содержимое** в области сведений откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики, а затем выберите GPO для делегирования.</span><span class="sxs-lookup"><span data-stu-id="ed53e-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="ed53e-110">Чтобы добавить доступ для пользователя или группы, нажмите кнопку **Добавить** , выберите пользователя или группу и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ed53e-110">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="ed53e-111">В диалоговом окне **Добавление группы или пользователя** выберите роль и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ed53e-111">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="ed53e-112">Чтобы удалить доступ для пользователя или группы, выберите пользователя или группу и нажмите кнопку **Удалить** .</span><span class="sxs-lookup"><span data-stu-id="ed53e-112">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

        <span data-ttu-id="ed53e-113">**Примечание**  Если пользователь или группа наследуют доступ к домену, кнопка " **Удалить** " недоступна.</span><span class="sxs-lookup"><span data-stu-id="ed53e-113">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="ed53e-114">Вы можете изменить доступ на уровне домена на вкладке " **Делегирование домена** ".</span><span class="sxs-lookup"><span data-stu-id="ed53e-114">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="ed53e-115">Чтобы изменить роли и разрешения, делегированные пользователю или группе, нажмите кнопку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="ed53e-115">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="ed53e-116">В диалоговом окне **разрешения** выберите пользователя или группу, установите флажок для каждой роли, которую нужно назначить этому пользователю или группе, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ed53e-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and click **OK**.</span></span>

        <span data-ttu-id="ed53e-117">**Примечание**  В редактор и утверждающие есть разрешения на просмотр.</span><span class="sxs-lookup"><span data-stu-id="ed53e-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="ed53e-118">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="ed53e-118">Additional considerations</span></span>

-   <span data-ttu-id="ed53e-119">По умолчанию для выполнения этой процедуры необходимо быть утверждающее, которое создало или управляло объектом групповой политики или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="ed53e-119">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="ed53e-120">В частности, необходимо иметь разрешение на доступ к **содержимому** для домена и **изменить разрешение безопасности** для этого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ed53e-120">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="ed53e-121">Для делегирования доступа на чтение для администраторов групповой политики, использующих многогрупповую политику, необходимо предоставить им **содержимое списка** и разрешения на **Чтение параметров** .</span><span class="sxs-lookup"><span data-stu-id="ed53e-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="ed53e-122">Это позволит им просматривать объекты групповой политики на вкладке " **содержимое** " в режиме расширенного использования.</span><span class="sxs-lookup"><span data-stu-id="ed53e-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="ed53e-123">Другие разрешения должны быть явным образом делегированы.</span><span class="sxs-lookup"><span data-stu-id="ed53e-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="ed53e-124">Редакторы должны иметь разрешение на **Чтение** для развернутой копии GPO, чтобы полностью использовать установку программного обеспечения групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ed53e-124">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="ed53e-125">Членство в группе "владельцы создателей групповой политики" должно быть ограничено, soit не используется для обхода управления доступом к GPO.</span><span class="sxs-lookup"><span data-stu-id="ed53e-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="ed53e-126">(В **консоли управления групповыми политиками**щелкните **объекты групповой политики** в лесу и домене, в которых вы хотите управлять объектами GPO, выберите пункт **Делегирование**и настройте параметры в соответствии с потребностями Организации.)</span><span class="sxs-lookup"><span data-stu-id="ed53e-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="ed53e-127">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="ed53e-127">Additional references</span></span>

-   [<span data-ttu-id="ed53e-128">Управление архивами</span><span class="sxs-lookup"><span data-stu-id="ed53e-128">Managing the Archive</span></span>](managing-the-archive.md)

 

 





