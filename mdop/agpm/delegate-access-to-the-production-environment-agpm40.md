---
title: Передача прав доступа к рабочей среде
description: Передача прав доступа к рабочей среде
author: dansimp
ms.assetid: 4c670581-8c47-41ea-80eb-02846ff1ec1f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a3920a8ba5835cbbcb8a74f0af4e3ca1e1c5f43f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818729"
---
# <span data-ttu-id="65efd-103">Передача прав доступа к рабочей среде</span><span class="sxs-lookup"><span data-stu-id="65efd-103">Delegate Access to the Production Environment</span></span>


<span data-ttu-id="65efd-104">С помощью расширенного управления групповыми политиками можно изменить доступ к объектам групповой политики (GPO) в рабочей среде домена, заменив существующие разрешения для этих GPO.</span><span class="sxs-lookup"><span data-stu-id="65efd-104">In Advanced Group Policy Management (AGPM), you can change access to Group Policy Objects (GPOs) in the production environment of the domain, replacing any existing permissions on those GPOs.</span></span> <span data-ttu-id="65efd-105">Вы можете настроить разрешения на уровне домена, чтобы разрешить или запретить пользователям изменять, удалять и изменять безопасность объектов групповой политики в производственной среде, если они не используют папку **управления изменениями** в консоли управления групповыми политиками (GPMC).</span><span class="sxs-lookup"><span data-stu-id="65efd-105">You can configure permissions at the domain level to either allow or prevent users from editing, deleting, or modifying the security of GPOs in the production environment when they are not using the **Change Control** folder in the Group Policy Management Console (GPMC).</span></span>

**<span data-ttu-id="65efd-106">Примечание.</span><span class="sxs-lookup"><span data-stu-id="65efd-106">Note</span></span>**  
-   <span data-ttu-id="65efd-107">Изменение способа делегирования доступа к производственной среде не влияет на возможность пользователей связывать объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="65efd-107">Changing how access to the production environment is delegated does not affect users' ability to link GPOs.</span></span>

-   <span data-ttu-id="65efd-108">При управлении и развертывании объектов групповой политики доступ к другим учетным записям за исключением тех, которые имеют разрешения **чтения** и **применения** , удаляется.</span><span class="sxs-lookup"><span data-stu-id="65efd-108">When GPOs are controlled or deployed, access for any other accounts except those with **Read** and **Apply** permissions is removed.</span></span>

 

<span data-ttu-id="65efd-109">Для выполнения этой процедуры требуется учетная запись пользователя, у которого есть роль администратора РАСШИРЕНного управления правами (полный доступ) или необходимые разрешения в расширенном управлении групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="65efd-109">A user account that has either the role of AGPM Administrator (Full Control) or the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="65efd-110">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="65efd-110">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="65efd-111">Изменение доступа к объектам групповой политики в рабочей среде домена</span><span class="sxs-lookup"><span data-stu-id="65efd-111">To change access to GPOs in the production environment of the domain</span></span>**

1.  <span data-ttu-id="65efd-112">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="65efd-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="65efd-113">Откройте вкладку **Делегирование производства** .</span><span class="sxs-lookup"><span data-stu-id="65efd-113">Click the **Production Delegation** tab.</span></span>

3.  <span data-ttu-id="65efd-114">Чтобы добавить разрешения для пользователя или группы, у которых нет доступа к производственной среде, или заменить разрешения для пользователя или группы, у которых есть доступ, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="65efd-114">To add permissions for a user or group that does not have access to the production environment, or to replace the permissions for a user or group that does have access:</span></span>

    1.  <span data-ttu-id="65efd-115">Нажмите кнопку **Добавить**, выберите пользователя или группу, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="65efd-115">Click **Add**, select a user or group, and then click **OK**.</span></span>

    2.  <span data-ttu-id="65efd-116">Выберите разрешения, которые нужно делегировать этому пользователю или группе для рабочей среды, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="65efd-116">Select permissions to delegate to that user or group for the production environment, and then click **OK**.</span></span>

4.  <span data-ttu-id="65efd-117">Чтобы удалить все разрешения в производственную среду для пользователя или группы, выберите пользователя или группу, нажмите кнопку **Удалить**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="65efd-117">To remove all permissions to the production environment for a user or group, select the user or group, click **Remove**, and then click **OK**.</span></span>

### <span data-ttu-id="65efd-118">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="65efd-118">Additional considerations</span></span>

-   <span data-ttu-id="65efd-119">По умолчанию для выполнения этой процедуры необходимо быть администратором РАСШИРЕНной версии (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="65efd-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="65efd-120">В частности, необходимо иметь разрешение на **изменение безопасности** для домена.</span><span class="sxs-lookup"><span data-stu-id="65efd-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="65efd-121">Разрешения для учетной записи службы РАСШИРЕНного доступа к аналитике нельзя изменить на вкладке " **Делегирование производства** ".</span><span class="sxs-lookup"><span data-stu-id="65efd-121">Permissions for the AGPM Service Account cannot be changed on the **Production Delegation** tab.</span></span>

-   <span data-ttu-id="65efd-122">По умолчанию следующие учетные записи имеют разрешения для GPO в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="65efd-122">By default, the following accounts have permissions for GPOs in the production environment:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="65efd-123">Account</span><span class="sxs-lookup"><span data-stu-id="65efd-123">Account</span></span></th>
    <th align="left"><span data-ttu-id="65efd-124">Разрешения по умолчанию для GPO</span><span class="sxs-lookup"><span data-stu-id="65efd-124">Default Permissions for GPOs</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="65efd-125">&lt;Учетная запись службы РАСШИРЕНного учета&gt;</span><span class="sxs-lookup"><span data-stu-id="65efd-125">&lt;AGPM Service Account&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65efd-126">Изменение настроек, удаление и изменение параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="65efd-126">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="65efd-127">Пользователи, прошедшие проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="65efd-127">Authenticated Users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65efd-128">Чтение, применение</span><span class="sxs-lookup"><span data-stu-id="65efd-128">Read, Apply</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="65efd-129">Администраторы домена</span><span class="sxs-lookup"><span data-stu-id="65efd-129">Domain Admins</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65efd-130">Изменение настроек, удаление и изменение параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="65efd-130">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="65efd-131">Администраторы предприятий</span><span class="sxs-lookup"><span data-stu-id="65efd-131">Enterprise Admins</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65efd-132">Изменение настроек, удаление и изменение параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="65efd-132">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="65efd-133">Контроллеры домена предприятия</span><span class="sxs-lookup"><span data-stu-id="65efd-133">Enterprise Domain Controllers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65efd-134">Read</span><span class="sxs-lookup"><span data-stu-id="65efd-134">Read</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="65efd-135">Система</span><span class="sxs-lookup"><span data-stu-id="65efd-135">System</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65efd-136">Изменение настроек, удаление и изменение параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="65efd-136">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="65efd-137">Членство в группе "владельцы создателей групповой политики" должно быть ограничено, soit не используется для обхода управления доступом к GPO.</span><span class="sxs-lookup"><span data-stu-id="65efd-137">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="65efd-138">(В **консоли управления групповыми политиками**щелкните **объекты групповой политики** в лесу и домене, в которых вы хотите управлять объектами GPO, выберите пункт **Делегирование**и настройте параметры в соответствии с потребностями Организации.)</span><span class="sxs-lookup"><span data-stu-id="65efd-138">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="65efd-139">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="65efd-139">Additional references</span></span>

-   [<span data-ttu-id="65efd-140">Настройка средства расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="65efd-140">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





