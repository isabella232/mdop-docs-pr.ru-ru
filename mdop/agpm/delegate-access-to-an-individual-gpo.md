---
title: Передача прав доступа к отдельному объекту групповой политики
description: Передача прав доступа к отдельному объекту групповой политики
author: dansimp
ms.assetid: b2a7d550-14bf-4b41-b6e4-2cc091eedd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5d2ae8c6ef52eae39feb67b9df42e84f523300
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818732"
---
# <span data-ttu-id="cd3d6-103">Передача прав доступа к отдельному объекту групповой политики</span><span class="sxs-lookup"><span data-stu-id="cd3d6-103">Delegate Access to an Individual GPO</span></span>


<span data-ttu-id="cd3d6-104">Как Администратор расширенного управления групповыми политиками (полный доступ) вы можете делегировать управление управляемым объектом групповой политики (GPO), чтобы выбранные группы и редакторы могли редактировать их, рецензенты смогут ее просмотреть, и утверждающие могут утвердить ее.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy object (GPO), so selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="cd3d6-105">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора расширенного управления групповыми политиками (полного доступа), учетная запись пользователя утверждающего, создавшего GPO, или учетная запись пользователя с необходимыми разрешениями для расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="cd3d6-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="cd3d6-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="cd3d6-107">Делегирование управления управляемым объектом групповой политики</span><span class="sxs-lookup"><span data-stu-id="cd3d6-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="cd3d6-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="cd3d6-109">На вкладке **содержимое** в области сведений откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики, а затем выберите GPO для делегирования.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="cd3d6-110">Нажмите кнопку **Добавить** , выберите пользователей или группы, которым будет разрешен доступ, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-110">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="cd3d6-111">Чтобы настроить разрешения для каждого пользователя или группы, нажмите кнопку **Дополнительно** на вкладке **содержание** и установите флажок разрешения ролей для разрешенных и запрещенных.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-111">To customize the permissions for each user or group, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="cd3d6-112">(Для более детального управления в диалоговом окне **разрешения** нажмите кнопку **Дополнительно** .)</span><span class="sxs-lookup"><span data-stu-id="cd3d6-112">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="cd3d6-113">Нажмите кнопку **Применить**, а затем в диалоговом окне **разрешения** нажмите кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="cd3d6-113">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="cd3d6-114">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="cd3d6-114">Additional considerations</span></span>

-   <span data-ttu-id="cd3d6-115">По умолчанию для выполнения этой процедуры необходимо быть утверждающее, которое создало или управляло объектом групповой политики или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="cd3d6-115">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="cd3d6-116">В частности, необходимо иметь разрешение на доступ к **содержимому** для домена и **изменить разрешение безопасности** для этого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-116">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="cd3d6-117">Для делегирования доступа на чтение для администраторов групповой политики, использующих многогрупповую политику, необходимо предоставить им **содержимое списка** и разрешения на **Чтение параметров** .</span><span class="sxs-lookup"><span data-stu-id="cd3d6-117">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="cd3d6-118">Это позволит им просматривать объекты групповой политики на вкладке " **содержимое** " в режиме расширенного использования.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-118">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="cd3d6-119">Установка разрешения на применение к **объекту и вложенным объектам**.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-119">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="cd3d6-120">Другие разрешения должны быть явным образом делегированы.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-120">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="cd3d6-121">Редакторы должны иметь разрешение на **Чтение** для развернутой копии GPO, чтобы полностью использовать установку программного обеспечения групповой политики.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-121">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="cd3d6-122">Членство в группе Владельцы создателей групповой политики должно быть ограничено, чтобы не использовать управление правами на доступ к объектам GPO.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-122">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="cd3d6-123">(В **консоли управления групповыми политиками**щелкните **объекты групповой политики** в лесу и домене, в которых вы хотите управлять объектами GPO, выберите пункт **Делегирование**и настройте параметры в соответствии с потребностями Организации.)</span><span class="sxs-lookup"><span data-stu-id="cd3d6-123">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="cd3d6-124">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="cd3d6-124">Additional references</span></span>

-   [<span data-ttu-id="cd3d6-125">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="cd3d6-125">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





