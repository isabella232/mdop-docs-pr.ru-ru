---
title: Разрешения на доступ пользователей в клиенте Application Virtualization
description: Разрешения на доступ пользователей в клиенте Application Virtualization
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815119"
---
# <span data-ttu-id="b62a0-103">Разрешения на доступ пользователей в клиенте Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="b62a0-103">User Access Permissions in Application Virtualization Client</span></span>


<span data-ttu-id="b62a0-104">На вкладке " **разрешения** " в диалоговом окне " **свойства** " щелкните правой кнопкой мыши узел **Application Virtualization** на консоли управления клиентом Application Virtualization, администраторы могут предоставить пользователям разрешения на использование различных клиентских функций.</span><span class="sxs-lookup"><span data-stu-id="b62a0-104">On the **Permissions** tab on the **Properties** dialog box, accessible by right-clicking the **Application Virtualization** node in the Application Virtualization Client Management Console, administrators can grant users permissions to use the various client functions.</span></span>

<span data-ttu-id="b62a0-105">**Примечание**  Перед изменением разрешений для пользователей убедитесь, что все изменения разрешений соответствуют рекомендациям Организации для предоставления разрешений пользователей.</span><span class="sxs-lookup"><span data-stu-id="b62a0-105">**Note** Before changing users permissions, ensure that any permissions changes are consistent with the organization's guidelines for granting user permissions.</span></span>

 

<span data-ttu-id="b62a0-106">В таблице ниже перечислены и описаны разрешения, которые могут быть предоставлены пользователям.</span><span class="sxs-lookup"><span data-stu-id="b62a0-106">The following table lists and describes the permissions that can be granted to users.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b62a0-107">Имя разрешения</span><span class="sxs-lookup"><span data-stu-id="b62a0-107">Permission Name</span></span></th>
<th align="left"><span data-ttu-id="b62a0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b62a0-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b62a0-109">Добавление приложений</span><span class="sxs-lookup"><span data-stu-id="b62a0-109">Add applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-110">Зарегистрируйте новые приложения, передавая клиенту новый OSD-файл с помощью sfttray.exe, sftmime.exe или MMC.</span><span class="sxs-lookup"><span data-stu-id="b62a0-110">Register new applications by passing a new OSD file to the client by using sfttray.exe, sftmime.exe or the MMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b62a0-111">Изменение размера кэша файловой системы</span><span class="sxs-lookup"><span data-stu-id="b62a0-111">Change file system cache size</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-112">Увеличивайте размер кэша файловой системы.</span><span class="sxs-lookup"><span data-stu-id="b62a0-112">Increase the size of the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b62a0-113">Изменение диска файловой системы</span><span class="sxs-lookup"><span data-stu-id="b62a0-113">Change file system drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-114">Выберите другую предпочтительную букву диска для файловой системы.</span><span class="sxs-lookup"><span data-stu-id="b62a0-114">Select a different preferred drive letter for the file system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b62a0-115">Изменение параметров журнала</span><span class="sxs-lookup"><span data-stu-id="b62a0-115">Change log settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-116">Измените уровень журнала или путь к журналу для файла журнала клиента.</span><span class="sxs-lookup"><span data-stu-id="b62a0-116">Change the log level or the log path for the client log file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b62a0-117">Изменение OSD файлов</span><span class="sxs-lookup"><span data-stu-id="b62a0-117">Change OSD files</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-118">Изменение OSD файлов для зарегистрированных приложений и их передача клиенту.</span><span class="sxs-lookup"><span data-stu-id="b62a0-118">Modify OSD files for registered applications and pass them into the client.</span></span> <span data-ttu-id="b62a0-119">Это не повлияет на обновление публикации.</span><span class="sxs-lookup"><span data-stu-id="b62a0-119">This does not affect publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b62a0-120">Очистка параметров приложения</span><span class="sxs-lookup"><span data-stu-id="b62a0-120">Clear application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-121">Удаление типов файлов, ярлыков и любых конфигураций для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="b62a0-121">Delete file types, shortcuts and any configurations for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b62a0-122">Удаление приложений</span><span class="sxs-lookup"><span data-stu-id="b62a0-122">Delete applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-123">Удалите все ссылки на приложение из файловой системы и кэша OSD для всех пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b62a0-123">Remove all references to an application from the file system and OSD cache for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b62a0-124">Импорт приложений в кэш</span><span class="sxs-lookup"><span data-stu-id="b62a0-124">Import applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-125">Загружайте данные приложения непосредственно из указанного SFT-файла в кэш файловой системы.</span><span class="sxs-lookup"><span data-stu-id="b62a0-125">Load application data directly from a specified SFT file into the file system cache.</span></span> <span data-ttu-id="b62a0-126">Это повлияет на всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="b62a0-126">This affects all users.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b62a0-127">Загрузка приложений в кэш</span><span class="sxs-lookup"><span data-stu-id="b62a0-127">Load applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-128">Начало загрузки SFT-файла приложения из настроенного источника, например, потокового сервера App-V.</span><span class="sxs-lookup"><span data-stu-id="b62a0-128">Start a load of the SFT file for an application from the configured source, such as an App-V Streaming Server.</span></span> <span data-ttu-id="b62a0-129">Приложение будет загружено для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="b62a0-129">This loads the application for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b62a0-130">Блокировка и разблокировка приложений в кэше</span><span class="sxs-lookup"><span data-stu-id="b62a0-130">Lock and unlock applications in the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-131">Запрет или разрешение на выгрузку приложений из кэша файловой системы.</span><span class="sxs-lookup"><span data-stu-id="b62a0-131">Prevent or allow applications from being unloaded from the file system cache.</span></span> <span data-ttu-id="b62a0-132">Это повлияет на всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="b62a0-132">This affects all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b62a0-133">Управление сопоставлениями типов файлов</span><span class="sxs-lookup"><span data-stu-id="b62a0-133">Manage file type associations</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-134">Добавление, изменение и удаление сопоставлений типов файлов только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="b62a0-134">Add, modify, or delete file type associations for the current user only.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b62a0-135">Управление параметрами обновления публикации</span><span class="sxs-lookup"><span data-stu-id="b62a0-135">Manage publishing refresh settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-136">Изменение параметров, управляющих временем обновлений публикации для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="b62a0-136">Change settings that control the timing of publishing refreshes for all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b62a0-137">Управление серверами публикаций</span><span class="sxs-lookup"><span data-stu-id="b62a0-137">Manage publishing servers</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-138">Добавляйте, изменяйте и удаляйте серверы публикаций для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="b62a0-138">Add, modify, or delete publishing servers for all users on the computer.</span></span> <span data-ttu-id="b62a0-139">Это разрешение неявно включает в себя разрешение на управление параметрами обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="b62a0-139">This permission implicitly includes permission to manage publishing refresh settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b62a0-140">Публикация сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="b62a0-140">Publish shortcuts</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-141">Создание новых сочетаний клавиш для зарегистрированных приложений.</span><span class="sxs-lookup"><span data-stu-id="b62a0-141">Create new shortcuts to registered applications.</span></span> <span data-ttu-id="b62a0-142">Пользователь также должен иметь разрешение на создание файлов в локальной файловой системе.</span><span class="sxs-lookup"><span data-stu-id="b62a0-142">The user must also have permission to create files in the local file system.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b62a0-143">Восстановление приложений</span><span class="sxs-lookup"><span data-stu-id="b62a0-143">Repair applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-144">Удаляйте особые конфигурации приложения для текущего пользователя, не удаляя ярлыки и сопоставления типов файлов.</span><span class="sxs-lookup"><span data-stu-id="b62a0-144">Remove application specific configurations for the current user without removing shortcuts or file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b62a0-145">Начало обновления публикации</span><span class="sxs-lookup"><span data-stu-id="b62a0-145">Start a publishing refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-146">Запуск незапланированного обновления публикации для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="b62a0-146">Start an unscheduled publishing refresh for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b62a0-147">Переключение в автономный режим</span><span class="sxs-lookup"><span data-stu-id="b62a0-147">Toggle offline mode</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-148">Измените значение всего клиента с Online на автономный для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="b62a0-148">Change the entire client from online to offline mode for all users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b62a0-149">Выгрузка приложений из кэша</span><span class="sxs-lookup"><span data-stu-id="b62a0-149">Unload applications from the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-150">Удаляйте данные приложения из кэша файловой системы для всех пользователей, не удаляя параметры, ярлыки и сопоставления типов файлов для пользователей.</span><span class="sxs-lookup"><span data-stu-id="b62a0-150">Clear application data from the file system cache for all users without removing user-specific settings, shortcuts, or file type associations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b62a0-151">Просмотр всех приложений</span><span class="sxs-lookup"><span data-stu-id="b62a0-151">View all applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="b62a0-152">Предоставление пользователю возможности просматривать виртуальные приложения для всех пользователей, зарегистрированных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b62a0-152">Allow the user to see the virtual applications for all users registered on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b62a0-153">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b62a0-153">Related topics</span></span>


[<span data-ttu-id="b62a0-154">Изменение прав доступа пользователей</span><span class="sxs-lookup"><span data-stu-id="b62a0-154">How to Change User Access Permissions</span></span>](how-to-change-user-access-permissions.md)

 

 





