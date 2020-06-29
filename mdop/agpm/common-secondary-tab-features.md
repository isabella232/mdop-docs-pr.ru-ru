---
title: Общие функции вкладки "Второстепенные"
description: Общие функции вкладки "Второстепенные"
author: dansimp
ms.assetid: 44a15c28-944c-49c1-8534-115ce1c362ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546fd4c91e060a5595b6c848015290882de933b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819089"
---
# <span data-ttu-id="aad89-103">Общие функции вкладки "Второстепенные"</span><span class="sxs-lookup"><span data-stu-id="aad89-103">Common Secondary Tab Features</span></span>


<span data-ttu-id="aad89-104">Каждая вспомогательная вкладка состоит из двух разделов:**объектов групповой политики** и **групп и пользователей**.</span><span class="sxs-lookup"><span data-stu-id="aad89-104">Each secondary tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="aad89-105">Раздел "объекты групповой политики"</span><span class="sxs-lookup"><span data-stu-id="aad89-105">Group Policy objects section</span></span>


<span data-ttu-id="aad89-106">Раздел " **объекты групповой политики** " отображает отфильтрованный список объектов групповой политики (GPO) и определяет указанные ниже характеристики для каждого GPO.</span><span class="sxs-lookup"><span data-stu-id="aad89-106">The **Group Policy objects** section displays a filtered list of Group Policy objects (GPOs) and identifies the following characteristics for each GPO:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aad89-107">Характеристика объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="aad89-107">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="aad89-108">Описание</span><span class="sxs-lookup"><span data-stu-id="aad89-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aad89-109">Name</span><span class="sxs-lookup"><span data-stu-id="aad89-109">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aad89-110">Имя объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="aad89-110">Name of the Group Policy object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aad89-111">Компьютер (Comp).</span><span class="sxs-lookup"><span data-stu-id="aad89-111">Computer (Comp.)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aad89-112">Автоматически созданная версия части объекта групповой политики на компьютере.</span><span class="sxs-lookup"><span data-stu-id="aad89-112">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aad89-113">Пользователь</span><span class="sxs-lookup"><span data-stu-id="aad89-113">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aad89-114">Автоматически созданная версия части объекта групповой политики пользователя.</span><span class="sxs-lookup"><span data-stu-id="aad89-114">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aad89-115">Состояние</span><span class="sxs-lookup"><span data-stu-id="aad89-115">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aad89-116">Состояние выбранного объекта групповой политики:</span><span class="sxs-lookup"><span data-stu-id="aad89-116">The state of the selected GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="aad89-117">Неуправляемый: Управление </strong> с помощью расширенного управления групповыми политиками не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="aad89-117">Uncontrolled:</strong> Not managed by AGPM.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="aad89-118">Возвращено: </strong> доступно для авторизованных редакторов для извлечения для редактирования или для развертывания администратором групповой политики.</span><span class="sxs-lookup"><span data-stu-id="aad89-118">Checked In:</strong> Available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="aad89-119">Извлечено: </strong> сейчас редактируется.</span><span class="sxs-lookup"><span data-stu-id="aad89-119">Checked Out:</strong> Currently being edited.</span></span> <span data-ttu-id="aad89-120">Недоступен для других редакторов, чтобы извлечь его до тех пор, пока редактор, который их проверил, или не произведет проверку.</span><span class="sxs-lookup"><span data-stu-id="aad89-120">Unavailable for other Editors to check out until the Editor who checked it out or an AGPM Administrator checks it in.</span></span></p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong><span data-ttu-id="aad89-121">Ожидание: </strong> ожидание утверждения администратором групповой политики перед созданием, управлением, развертыванием и удалением.</span><span class="sxs-lookup"><span data-stu-id="aad89-121">Pending:</strong> Awaiting approval from a Group Policy administrator before being created, controlled, deployed, or deleted.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="aad89-122">Удалено: </strong> удалено из архива, но по-прежнему может быть восстановлено.</span><span class="sxs-lookup"><span data-stu-id="aad89-122">Deleted:</strong> Deleted from the archive, but still able to be restored.</span></span></p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong><span data-ttu-id="aad89-123">Шаблон: </strong> статическая версия GPO для использования в качестве отправной точки при создании новых объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="aad89-123">Template:</strong> A static version of a GPO for use as a starting point when creating new GPOs.</span></span></p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong><span data-ttu-id="aad89-124">Шаблон (по умолчанию): </strong> по умолчанию этот шаблон является начальной точкой, используемой при создании нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="aad89-124">Template (default):</strong> By default, this template is the starting point used when creating a new GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aad89-125">Состояние объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="aad89-125">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aad89-126">Конфигурацию компьютера и конфигурацию пользователя можно управлять отдельно.</span><span class="sxs-lookup"><span data-stu-id="aad89-126">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="aad89-127">Состояние GPO показывает, какие части объекта групповой политики включены.</span><span class="sxs-lookup"><span data-stu-id="aad89-127">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aad89-128">Фильтр WMI</span><span class="sxs-lookup"><span data-stu-id="aad89-128">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aad89-129">Отобразить все фильтры WMI, примененные к этому объекту групповой политики.</span><span class="sxs-lookup"><span data-stu-id="aad89-129">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="aad89-130">Управление фильтрами WMI осуществляется с помощью <strong> узла "фильтры WMI" </strong> для домена в дереве консоли консоли управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="aad89-130">WMI filters are managed under the <strong>WMI Filters</strong> node for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aad89-131">Изменено</span><span class="sxs-lookup"><span data-stu-id="aad89-131">Modified</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aad89-132">Для управляемого объекта групповой политики: самая поздняя дата, когда она была возвращена после изменения или извлечения для изменения.</span><span class="sxs-lookup"><span data-stu-id="aad89-132">For a controlled GPO, the most recent date when it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="aad89-133">Для неконтрольного объекта групповой политики — Дата последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="aad89-133">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aad89-134">Владелец</span><span class="sxs-lookup"><span data-stu-id="aad89-134">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aad89-135">Редактор, который вернул или утверждающий, который развернул выбранный объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="aad89-135">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="aad89-136">Раздел групп и пользователей</span><span class="sxs-lookup"><span data-stu-id="aad89-136">Groups and Users section</span></span>


<span data-ttu-id="aad89-137">При выборе объекта групповой политики в разделе **группы и пользователи** отображается список групп и пользователей, имеющих доступ к этому объекту групповой политики.</span><span class="sxs-lookup"><span data-stu-id="aad89-137">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="aad89-138">Разрешенные разрешения и наследование отображаются для каждой группы или пользователя.</span><span class="sxs-lookup"><span data-stu-id="aad89-138">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="aad89-139">Администратор РАСШИРЕНного доступа может настраивать разрешения с помощью стандартных ролей (редакторов, утверждающих и рецензентов), а также настроенных сочетаний разрешений.</span><span class="sxs-lookup"><span data-stu-id="aad89-139">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, and Reviewer) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aad89-140">Кнопка</span><span class="sxs-lookup"><span data-stu-id="aad89-140">Button</span></span></th>
<th align="left"><span data-ttu-id="aad89-141">Эффект</span><span class="sxs-lookup"><span data-stu-id="aad89-141">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aad89-142">Add</span><span class="sxs-lookup"><span data-stu-id="aad89-142">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aad89-143">Добавьте новую запись в дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="aad89-143">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="aad89-144">Вы можете добавить пользователя или группу в службе каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="aad89-144">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aad89-145">Удалить</span><span class="sxs-lookup"><span data-stu-id="aad89-145">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aad89-146">Удаление выделенного элемента из списка управления доступом.</span><span class="sxs-lookup"><span data-stu-id="aad89-146">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aad89-147">Свойства</span><span class="sxs-lookup"><span data-stu-id="aad89-147">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aad89-148">Отображение свойств выбранного объекта.</span><span class="sxs-lookup"><span data-stu-id="aad89-148">Display the properties for the selected object.</span></span> <span data-ttu-id="aad89-149">На странице "Свойства" отображается один и тот же объект в окне " <strong> Пользователи и компьютеры Active Directory" </strong> .</span><span class="sxs-lookup"><span data-stu-id="aad89-149">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aad89-150">Дополнительно</span><span class="sxs-lookup"><span data-stu-id="aad89-150">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aad89-151">Откройте <strong> Редактор списка управления доступом </strong> .</span><span class="sxs-lookup"><span data-stu-id="aad89-151">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="aad89-152">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="aad89-152">Additional considerations</span></span>

-   <span data-ttu-id="aad89-153">Сведения о ролях и разрешениях, связанных с определенными задачами, можно найти в разделе [выполнение задач администратора расширенного администрирования](performing-agpm-administrator-tasks.md), [выполнение задач редактора](performing-editor-tasks.md), [выполнение задач утверждающего](performing-approver-tasks.md)и [выполнение задач рецензента](performing-reviewer-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="aad89-153">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks.md), [Performing Editor Tasks](performing-editor-tasks.md), [Performing Approver Tasks](performing-approver-tasks.md), and [Performing Reviewer Tasks](performing-reviewer-tasks.md).</span></span>

### <span data-ttu-id="aad89-154">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="aad89-154">Additional references</span></span>

-   [<span data-ttu-id="aad89-155">Вкладка "Содержимое"</span><span class="sxs-lookup"><span data-stu-id="aad89-155">Contents Tab</span></span>](contents-tab.md)

 

 





