---
title: Предоставление доступа на уровне домена к архиву
description: Предоставление доступа на уровне домена к архиву
author: dansimp
ms.assetid: 11ca1d40-4b5c-496e-8922-d01412717858
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b33c0ec8821248ab4eddc051e67e7f0e6c073a9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818722"
---
# <span data-ttu-id="ebe7f-103">Предоставление доступа на уровне домена к архиву</span><span class="sxs-lookup"><span data-stu-id="ebe7f-103">Delegate Domain-Level Access to the Archive</span></span>


<span data-ttu-id="ebe7f-104">Настройте делегирование для своей среды, чтобы администраторы групповой политики могли получать доступ к объектам групповой политики (GPO) в архиве и управлять им.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-104">Set up delegation for your environment so that Group Policy administrators have the appropriate access to and control over Group Policy Objects (GPOs) in the archive.</span></span> <span data-ttu-id="ebe7f-105">Существуют базовые разрешения, которые можно применять для повышения эффективности операций.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-105">There are baseline permissions you can apply to make operation more efficient.</span></span> <span data-ttu-id="ebe7f-106">Вы можете предоставить разрешения в соответствии с потребностями Организации.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="ebe7f-107">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора РАСШИРЕНного управления правами (полного доступа) или необходимых разрешений в расширенном управлении групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="ebe7f-108">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="ebe7f-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="ebe7f-109">Делегирование доступа для пользователей и групп с соответствующими разрешениями для всех GPO в рамках домена</span><span class="sxs-lookup"><span data-stu-id="ebe7f-109">To delegate access so that users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="ebe7f-110">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ebe7f-111">Откройте вкладку **Делегирование домена** и настройте доступ ко всем объектам групповой политики в домене.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-111">Click the **Domain Delegation** tab, and configure access to all GPOs in the domain:</span></span>

    1.  <span data-ttu-id="ebe7f-112">Чтобы добавить доступ для пользователя или группы, нажмите кнопку **Добавить** , выберите пользователя или группу и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="ebe7f-113">В диалоговом окне **Добавление группы или пользователя** выберите роль и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="ebe7f-114">Чтобы удалить доступ для пользователя или группы, выберите пользователя или группу и нажмите кнопку **Удалить** .</span><span class="sxs-lookup"><span data-stu-id="ebe7f-114">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

    3.  <span data-ttu-id="ebe7f-115">Чтобы изменить роли и разрешения, делегированные пользователю или группе, нажмите кнопку " **Дополнительно** ".</span><span class="sxs-lookup"><span data-stu-id="ebe7f-115">To modify the roles and permissions delegated to a user or group, select click the **Advanced** button.</span></span> <span data-ttu-id="ebe7f-116">В диалоговом окне **разрешения** выберите пользователя или группу, установите флажки для всех ролей, которые необходимо назначить этому пользователю или группе, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="ebe7f-117">**Примечание**  В редактор и утверждающие есть разрешения на просмотр.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="ebe7f-118">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="ebe7f-118">Additional considerations</span></span>

-   <span data-ttu-id="ebe7f-119">По умолчанию для выполнения этой процедуры необходимо быть администратором РАСШИРЕНной версии (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="ebe7f-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="ebe7f-120">В частности, необходимо иметь разрешение на **изменение безопасности** для домена.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="ebe7f-121">Для делегирования доступа на чтение для администраторов групповой политики, использующих многогрупповую политику, необходимо предоставить им **содержимое списка** и разрешения на **Чтение параметров** .</span><span class="sxs-lookup"><span data-stu-id="ebe7f-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="ebe7f-122">Это позволит им просматривать объекты групповой политики на вкладке " **содержимое** " в режиме расширенного использования.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="ebe7f-123">Другие разрешения должны быть явным образом делегированы.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="ebe7f-124">Редакторам необходимо предоставить разрешение на **Чтение** для развернутой копии объекта групповой политики, чтобы полностью использовать установку программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-124">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="ebe7f-125">Членство в группе "владельцы создателей групповой политики" должно быть ограничено, soit не используется для обхода управления доступом к GPO.</span><span class="sxs-lookup"><span data-stu-id="ebe7f-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="ebe7f-126">(В **консоли управления групповыми политиками**щелкните **объекты групповой политики** в лесу и домене, в которых вы хотите управлять объектами GPO, выберите пункт **Делегирование**и настройте параметры в соответствии с потребностями Организации.)</span><span class="sxs-lookup"><span data-stu-id="ebe7f-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="ebe7f-127">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="ebe7f-127">Additional references</span></span>

-   [<span data-ttu-id="ebe7f-128">Управление архивами</span><span class="sxs-lookup"><span data-stu-id="ebe7f-128">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





