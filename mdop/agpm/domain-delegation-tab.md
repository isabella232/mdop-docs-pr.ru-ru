---
title: Вкладка "Делегирование домена"
description: Вкладка "Делегирование домена"
author: dansimp
ms.assetid: 15a9bfff-e25b-4b62-9ebc-521a5f4eae96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d49083bcefe6c7edcb3a95dc63d2249826d50327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818629"
---
# <span data-ttu-id="e86a7-103">Вкладка "Делегирование домена"</span><span class="sxs-lookup"><span data-stu-id="e86a7-103">Domain Delegation Tab</span></span>


<span data-ttu-id="e86a7-104">Вкладка " **Делегирование домена** " в области **управления изменениями** содержит список администраторов групповой политики, которые имеют доступ к архиву на уровне домена, и указывает роли каждого из них.</span><span class="sxs-lookup"><span data-stu-id="e86a7-104">The **Domain Delegation** tab on the **Change Control** pane provides a list of Group Policy administrators who have domain-level access to the archive and indicates the roles of each.</span></span> <span data-ttu-id="e86a7-105">Кроме того, эта вкладка позволяет администраторам расширенного управления групповыми политиками (полный доступ) настраивать разрешения на уровне домена для редакторов, утверждающих, рецензентов и других администраторов управления РАСШИРЕНным доступом.</span><span class="sxs-lookup"><span data-stu-id="e86a7-105">Additionally, this tab enables AGPM Administrators (Full Control) to configure domain-level permissions for Editors, Approvers, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="e86a7-106">На вкладке **Делегирование домена** находятся два раздела: Настройка уведомлений электронной почты и делегирование на основе ролей для расширенного управления групповыми политиками на уровне домена.</span><span class="sxs-lookup"><span data-stu-id="e86a7-106">There are two sections on the **Domain Delegation** tab—configuration of e-mail notification and role-based delegation for Advanced Group Policy Management (AGPM) at the domain level.</span></span>

## <span data-ttu-id="e86a7-107">Настройка уведомления по электронной почте</span><span class="sxs-lookup"><span data-stu-id="e86a7-107">Configuration of e-mail notification</span></span>


<span data-ttu-id="e86a7-108">В разделе уведомлений по электронной почте на этой вкладке указаны утверждающие, которые будут получать уведомления о том, что ожидающие операции находятся в РАСШИРЕНном режиме.</span><span class="sxs-lookup"><span data-stu-id="e86a7-108">The e-mail notification section of this tab identifies the Approvers that will receive notification when operations are pending in AGPM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e86a7-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="e86a7-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="e86a7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e86a7-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e86a7-111">Исходная версия</span><span class="sxs-lookup"><span data-stu-id="e86a7-111">From</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e86a7-112">Псевдоним в РАСШИРЕНном списке, из которого уведомление отправляется утверждающим.</span><span class="sxs-lookup"><span data-stu-id="e86a7-112">The AGPM alias from which notification is sent to Approvers.</span></span> <span data-ttu-id="e86a7-113">В среде с несколькими доменами это может быть один и тот же псевдоним во всей среде или другой псевдоним для каждого домена.</span><span class="sxs-lookup"><span data-stu-id="e86a7-113">In an environment with multiple domains, this can be the same alias throughout the environment or a different alias for each domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e86a7-114">Результат</span><span class="sxs-lookup"><span data-stu-id="e86a7-114">To</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e86a7-115">Разделенный запятыми список адресов электронной почты утверждающих, которым нужно отправить уведомление</span><span class="sxs-lookup"><span data-stu-id="e86a7-115">A comma-delimited list of e-mail addresses of Approvers to whom notification is to be sent</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e86a7-116">SMTP-сервер</span><span class="sxs-lookup"><span data-stu-id="e86a7-116">SMTP server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e86a7-117">Имя почтового сервера, например mail.contoso.com</span><span class="sxs-lookup"><span data-stu-id="e86a7-117">The name of the e-mail server, such as mail.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e86a7-118">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="e86a7-118">User name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e86a7-119">Пользователь с доступом к SMTP-серверу</span><span class="sxs-lookup"><span data-stu-id="e86a7-119">A user with access to the SMTP server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e86a7-120">Пароль</span><span class="sxs-lookup"><span data-stu-id="e86a7-120">Password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e86a7-121">Пароль пользователя для проверки подлинности на SMTP-сервере</span><span class="sxs-lookup"><span data-stu-id="e86a7-121">User's password for authentication to the SMTP server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e86a7-122">Подтвердить пароль</span><span class="sxs-lookup"><span data-stu-id="e86a7-122">Confirm password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e86a7-123">Подтверждение пароля пользователя</span><span class="sxs-lookup"><span data-stu-id="e86a7-123">Confirm user's password</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e86a7-124">Делегирование на основе ролей на уровне домена</span><span class="sxs-lookup"><span data-stu-id="e86a7-124">Domain-level role-based delegation</span></span>


<span data-ttu-id="e86a7-125">В разделе Делегирование на основе ролей вы можете отобразить и включить администраторам РАСШИРЕНного доступа к данным о разрешенных, запрещенных и унаследованных разрешениях для каждой группы и пользователя в домене с доступом к архиву.</span><span class="sxs-lookup"><span data-stu-id="e86a7-125">The role-based delegation section of this tab displays and enables an AGPM Administrator to delegate allowed, denied, and inherited permissions for each group and user on the domain with access to the archive.</span></span> <span data-ttu-id="e86a7-126">Администраторы РАСШИРЕНного доступа могут настраивать разрешения домена с помощью стандартных ролей (редактор, утверждающий, рецензент и администратор РАСШИРЕНного доступа) или настроенного сочетания разрешений для каждого администратора групповой политики.</span><span class="sxs-lookup"><span data-stu-id="e86a7-126">An AGPM Administrator can configure domain-wide permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions for each Group Policy administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e86a7-127">Кнопка</span><span class="sxs-lookup"><span data-stu-id="e86a7-127">Button</span></span></th>
<th align="left"><span data-ttu-id="e86a7-128">Эффект</span><span class="sxs-lookup"><span data-stu-id="e86a7-128">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e86a7-129">Add</span><span class="sxs-lookup"><span data-stu-id="e86a7-129">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e86a7-130">Добавьте новую запись в дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="e86a7-130">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="e86a7-131">Пользователи и группы в службе каталогов Active Directory могут быть добавлены в качестве администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="e86a7-131">Any users or groups in Active Directory can be added as Group Policy administrators.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e86a7-132">Удалить</span><span class="sxs-lookup"><span data-stu-id="e86a7-132">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e86a7-133">Удаление выбранных администраторов групповой политики из списка управления доступом.</span><span class="sxs-lookup"><span data-stu-id="e86a7-133">Remove the selected Group Policy administrators from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e86a7-134">Свойства</span><span class="sxs-lookup"><span data-stu-id="e86a7-134">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e86a7-135">Отображение свойств выбранных администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="e86a7-135">Display the properties for the selected Group Policy administrators.</span></span> <span data-ttu-id="e86a7-136">На странице Свойства показан один и тот же объект в <strong> Active Directory "Пользователи" и "компьютеры" </strong> .</span><span class="sxs-lookup"><span data-stu-id="e86a7-136">The properties page is the same one displayed for an object in <strong>Active Directory User and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e86a7-137">Дополнительно</span><span class="sxs-lookup"><span data-stu-id="e86a7-137">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e86a7-138">Откройте <strong> Редактор списка управления доступом </strong> .</span><span class="sxs-lookup"><span data-stu-id="e86a7-138">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="e86a7-139">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="e86a7-139">Additional considerations</span></span>

-   <span data-ttu-id="e86a7-140">Сведения о ролях и разрешениях, связанных с определенными задачами, можно найти в разделе [выполнение задач администратора расширенного администрирования](performing-agpm-administrator-tasks.md), [выполнение задач редактора](performing-editor-tasks.md), [выполнение задач утверждающего](performing-approver-tasks.md)и [выполнение задач рецензента](performing-reviewer-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="e86a7-140">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks.md), [Performing Editor Tasks](performing-editor-tasks.md), [Performing Approver Tasks](performing-approver-tasks.md), and [Performing Reviewer Tasks](performing-reviewer-tasks.md).</span></span>

### <span data-ttu-id="e86a7-141">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="e86a7-141">Additional references</span></span>

-   [<span data-ttu-id="e86a7-142">Пользовательский интерфейс: расширенное управление групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="e86a7-142">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

-   [<span data-ttu-id="e86a7-143">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="e86a7-143">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





