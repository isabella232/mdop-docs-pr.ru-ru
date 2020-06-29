---
title: Предоставление доступа на уровне домена
description: Предоставление доступа на уровне домена
author: dansimp
ms.assetid: 64c8e773-38cc-4991-9ed2-5a801094d06e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb4c33e60b0d995e45fca6c9e91a26c30dd4a7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820999"
---
# <span data-ttu-id="05522-103">Предоставление доступа на уровне домена</span><span class="sxs-lookup"><span data-stu-id="05522-103">Delegate Domain-Level Access</span></span>


<span data-ttu-id="05522-104">Настройте делегирование для своей среды, чтобы администраторы групповой политики могли получать доступ к объектам групповой политики (GPO) и управлять им.</span><span class="sxs-lookup"><span data-stu-id="05522-104">Set up delegation for your environment so Group Policy administrators have the appropriate access to and control over Group Policy objects (GPOs).</span></span> <span data-ttu-id="05522-105">Существуют базовые разрешения, которые можно применять для повышения эффективности работы расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="05522-105">There are baseline permissions you can apply to make the operation of Advanced Group Policy Management (AGPM) more efficient.</span></span> <span data-ttu-id="05522-106">Вы можете предоставить разрешения в соответствии с потребностями Организации.</span><span class="sxs-lookup"><span data-stu-id="05522-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="05522-107">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора РАСШИРЕНного управления правами (полного доступа) или необходимых разрешений в расширенном управлении групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="05522-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="05522-108">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="05522-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="05522-109">Для делегирования доступа пользователи и группы имеют соответствующие разрешения на доступ ко всем объектам групповой политики в пределах домена.</span><span class="sxs-lookup"><span data-stu-id="05522-109">To delegate access so users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="05522-110">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="05522-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="05522-111">Откройте вкладку **Делегирование домена** и нажмите кнопку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="05522-111">Click the **Domain Delegation** tab, then click the **Advanced** button.</span></span>

3.  <span data-ttu-id="05522-112">В диалоговом окне **разрешения** установите флажки для всех ролей, которые необходимо назначить отдельным сотруднику, а затем нажмите кнопку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="05522-112">In the **Permissions** dialog box, click the check box for each role to be assigned to an individual, and then click the **Advanced** button.</span></span>

    <span data-ttu-id="05522-113">**Примечание**  В редактор и утверждающие есть разрешения на просмотр.</span><span class="sxs-lookup"><span data-stu-id="05522-113">**Note** Editor and Approver include Reviewer permissions.</span></span>

     

4.  <span data-ttu-id="05522-114">В диалоговом окне **Дополнительные параметры безопасности** выберите администратора групповой политики, а затем нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="05522-114">In the **Advanced Security Settings** dialog box, select a Group Policy administrator, and then click **Edit**.</span></span>

5.  <span data-ttu-id="05522-115">В поле **Применить**выберите **этот объект и вложенные объекты**, настройте особые разрешения за пределами стандартных ролей расширенного доступа, а затем нажмите кнопку **ОК** в диалоговом окне **запись** **разрешения** .</span><span class="sxs-lookup"><span data-stu-id="05522-115">For **Apply onto**, select **This object and nested objects**, configure any special permissions beyond the standard AGPM roles, then click **OK** in the **Permission** **Entry** dialog box.</span></span>

6.  <span data-ttu-id="05522-116">В диалоговом окне **Дополнительные параметры безопасности** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="05522-116">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

7.  <span data-ttu-id="05522-117">В диалоговом окне **разрешения** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="05522-117">In the **Permissions** dialog box, click **OK**.</span></span>

### <span data-ttu-id="05522-118">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="05522-118">Additional considerations</span></span>

-   <span data-ttu-id="05522-119">По умолчанию для выполнения этой процедуры необходимо быть администратором РАСШИРЕНной версии (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="05522-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="05522-120">В частности, необходимо иметь разрешение на **изменение безопасности** для домена.</span><span class="sxs-lookup"><span data-stu-id="05522-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="05522-121">Для делегирования доступа на чтение для администраторов групповой политики, использующих многогрупповую политику, необходимо предоставить им **содержимое списка** и разрешения на **Чтение параметров** .</span><span class="sxs-lookup"><span data-stu-id="05522-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="05522-122">Это позволит им просматривать объекты групповой политики на вкладке " **содержимое** " в режиме расширенного использования.</span><span class="sxs-lookup"><span data-stu-id="05522-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="05522-123">Установка разрешения на применение к **объекту и вложенным объектам**.</span><span class="sxs-lookup"><span data-stu-id="05522-123">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="05522-124">Другие разрешения должны быть явным образом делегированы.</span><span class="sxs-lookup"><span data-stu-id="05522-124">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="05522-125">Редакторам необходимо предоставить разрешение на **Чтение** для развернутой копии объекта групповой политики, чтобы полностью использовать установку программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="05522-125">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="05522-126">Членство в группе Владельцы создателей групповой политики должно быть ограничено, чтобы не использовать управление правами на доступ к объектам GPO.</span><span class="sxs-lookup"><span data-stu-id="05522-126">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="05522-127">(В **консоли управления групповыми политиками**щелкните **объекты групповой политики** в лесу и домене, в которых вы хотите управлять объектами GPO, выберите пункт **Делегирование**и настройте параметры в соответствии с потребностями Организации.)</span><span class="sxs-lookup"><span data-stu-id="05522-127">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="05522-128">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="05522-128">Additional references</span></span>

-   [<span data-ttu-id="05522-129">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="05522-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





