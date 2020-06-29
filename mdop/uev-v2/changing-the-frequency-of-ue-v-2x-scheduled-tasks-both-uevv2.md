---
title: Изменение частоты выполнения запланированных задач UE-V 2. x
description: Изменение частоты выполнения запланированных задач UE-V 2. x
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824429"
---
# <span data-ttu-id="b0306-103">Изменение частоты выполнения запланированных задач UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="b0306-103">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>


<span data-ttu-id="b0306-104">Установщик агента Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 или 2,1 SP1 AgentSetup.exe создает следующие запланированные задачи при установке агента UE-V:</span><span class="sxs-lookup"><span data-stu-id="b0306-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 Agent installer, AgentSetup.exe, creates the following scheduled tasks during the UE-V Agent installation:</span></span>

-   **<span data-ttu-id="b0306-105">Мониторинг параметров приложения</span><span class="sxs-lookup"><span data-stu-id="b0306-105">Monitor Application Settings</span></span>**

-   **<span data-ttu-id="b0306-106">Приложение контроллера синхронизации</span><span class="sxs-lookup"><span data-stu-id="b0306-106">Sync Controller Application</span></span>**

-   **<span data-ttu-id="b0306-107">Синхронизация параметров при выходе из системы</span><span class="sxs-lookup"><span data-stu-id="b0306-107">Synchronize Settings at Logoff</span></span>**

-   **<span data-ttu-id="b0306-108">Автоматическое обновление шаблона</span><span class="sxs-lookup"><span data-stu-id="b0306-108">Template Auto Update</span></span>**

-   **<span data-ttu-id="b0306-109">Сбор данных по улучшению качества программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="b0306-109">Collect CEIP data</span></span>**

-   **<span data-ttu-id="b0306-110">Отправка данных программы улучшения качества программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="b0306-110">Upload CEIP Data</span></span>**

<span data-ttu-id="b0306-111">**Примечание**  За исключением сбора данных CEIP, эти задачи должны оставаться включенными, так как UE-V не сможет работать без них.</span><span class="sxs-lookup"><span data-stu-id="b0306-111">**Note** With the exception of Collect CEIP Data, these tasks must remain enabled as UE-V cannot function without them.</span></span>

 

<span data-ttu-id="b0306-112">Эти запланированные задачи не настраиваются с помощью средств UE-V.</span><span class="sxs-lookup"><span data-stu-id="b0306-112">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="b0306-113">Администраторы, которые хотят изменить запланированную задачу для этих элементов, могут создать сценарий, который использует параметры командной строки Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="b0306-113">Administrators who want to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="b0306-114">Дополнительные сведения об Schtasks.exeх приведены в разделе [Использование программы Schtasks, exe для планирования задач в Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span><span class="sxs-lookup"><span data-stu-id="b0306-114">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

<span data-ttu-id="b0306-115">Дополнительные сведения о</span><span class="sxs-lookup"><span data-stu-id="b0306-115">For more information about</span></span>

## <span data-ttu-id="b0306-116">Запланированные задачи UE-V</span><span class="sxs-lookup"><span data-stu-id="b0306-116">UE-V Scheduled Tasks</span></span>


<span data-ttu-id="b0306-117">Следующие запланированные задачи включены в UE-V 2 с помощью команд конфигурации планировщика заданий.</span><span class="sxs-lookup"><span data-stu-id="b0306-117">The following scheduled tasks are included in UE-V 2 with sample scheduled task configuration commands.</span></span>

### <span data-ttu-id="b0306-118">Сбор данных по улучшению качества программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="b0306-118">Collect CEIP Data</span></span>

<span data-ttu-id="b0306-119">Если после установки пользователь или администратор выбрал участие в программе улучшения качества программного обеспечения (CEIP), UE-V собирает данные, чтобы улучшить продукт в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="b0306-119">If upon installation the user or administrator choses to participate in the Customer Experience Improvement Program (CEIP), UE-V collects data to help improve the product in future releases.</span></span> <span data-ttu-id="b0306-120">Это запланированное задание запускается только при входе в систему.</span><span class="sxs-lookup"><span data-stu-id="b0306-120">This scheduled task only runs at logon.</span></span> <span data-ttu-id="b0306-121">Задача **сбора данных CEIP** запускает UevSqmSession.exe, которая находится в каталоге установки агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="b0306-121">The **Collect CEIP Data** task runs the UevSqmSession.exe, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b0306-122">Название задачи</span><span class="sxs-lookup"><span data-stu-id="b0306-122">Task name</span></span></th>
<th align="left"><span data-ttu-id="b0306-123">Событие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b0306-123">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0306-124">Данные \Microsoft\UE-V\Collect CEIP</span><span class="sxs-lookup"><span data-stu-id="b0306-124">\Microsoft\UE-V\Collect CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-125">Вторич</span><span class="sxs-lookup"><span data-stu-id="b0306-125">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b0306-126">Мониторинг параметров приложения</span><span class="sxs-lookup"><span data-stu-id="b0306-126">Monitor Application Settings</span></span>

<span data-ttu-id="b0306-127">Задача " **Параметры приложения** " используется для синхронизации параметров приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="b0306-127">The **Monitor Application Settings** task is used to synchronize settings for Windows apps.</span></span> <span data-ttu-id="b0306-128">Оно запускается при входе в систему, но задерживается на 30 секунд, чтобы не повлиять на время входа в систему.</span><span class="sxs-lookup"><span data-stu-id="b0306-128">It is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span> <span data-ttu-id="b0306-129">Задача "мониторинг состояния приложения" запускает UevAppMonitor.exe файл, который находится в каталоге установки агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="b0306-129">The Monitor Application Status task runs the UevAppMonitor.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b0306-130">Название задачи</span><span class="sxs-lookup"><span data-stu-id="b0306-130">Task name</span></span></th>
<th align="left"><span data-ttu-id="b0306-131">Событие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b0306-131">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0306-132">Состояние \Microsoft\UE-V\Monitorного приложения</span><span class="sxs-lookup"><span data-stu-id="b0306-132">\Microsoft\UE-V\Monitor Application Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-133">Вторич</span><span class="sxs-lookup"><span data-stu-id="b0306-133">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b0306-134">Приложение контроллера синхронизации</span><span class="sxs-lookup"><span data-stu-id="b0306-134">Sync Controller Application</span></span>

<span data-ttu-id="b0306-135">Задача " **Синхронизация приложения контроллера** " используется для запуска контроллера синхронизации для синхронизации параметров с компьютера и места хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="b0306-135">The **Sync Controller Application** task is used to start the Sync Controller to synchronize settings from the computer to the settings storage location.</span></span> <span data-ttu-id="b0306-136">По умолчанию задача выполняется каждые 30 минут.</span><span class="sxs-lookup"><span data-stu-id="b0306-136">By default, the task runs every 30 minutes.</span></span> <span data-ttu-id="b0306-137">В это время локальные параметры синхронизируются с местом хранения параметров, и обновленные параметры в местоположении хранения параметров синхронизируются с компьютером.</span><span class="sxs-lookup"><span data-stu-id="b0306-137">At that time, local settings are synchronized to the settings storage location, and updated settings on the settings storage location are synchronized to the computer.</span></span> <span data-ttu-id="b0306-138">Приложение контроллера синхронизации запускает Microsoft.Uev.SyncController.exe, которое находится в каталоге установки UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="b0306-138">The Sync Controller application runs the Microsoft.Uev.SyncController.exe, which is located in the UE-V Agent installation directory.</span></span>
<span data-ttu-id="b0306-139">**Примечание.** Как и в случае с **параметрами приложения монитора** , эта задача запускается при входе в систему, но задерживается на 30 секунд, чтобы не повлиять на время входа в систему.</span><span class="sxs-lookup"><span data-stu-id="b0306-139">**Note:** As per the **Monitor Application Settings** task, this task is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b0306-140">Название задачи</span><span class="sxs-lookup"><span data-stu-id="b0306-140">Task name</span></span></th>
<th align="left"><span data-ttu-id="b0306-141">Событие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b0306-141">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0306-142">Приложение контроллера \Microsoft\UE-V\Sync</span><span class="sxs-lookup"><span data-stu-id="b0306-142">\Microsoft\UE-V\Sync Controller Application</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-143">Вход в систему и каждые 30 минут позже</span><span class="sxs-lookup"><span data-stu-id="b0306-143">Logon, and every 30 minutes thereafter</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b0306-144">Например, следующая команда настраивает агент для синхронизации параметров каждые 15 минут вместо 30 минут по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b0306-144">For example, the following command configures the agent to synchronize settings every 15 minutes instead of the default 30 minutes.</span></span>

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### <span data-ttu-id="b0306-145">Синхронизация параметров при выходе из системы</span><span class="sxs-lookup"><span data-stu-id="b0306-145">Synchronize Settings at Logoff</span></span>

<span data-ttu-id="b0306-146">Для запуска приложения при входе в систему, которое управляет синхронизацией приложений при выходе для UE-V, используется задача " **синхронизировать параметры при выходе из системы** ".</span><span class="sxs-lookup"><span data-stu-id="b0306-146">The **Synchronize Settings at Logoff** task is used to start an application at logon that controls the synchronization of applications at logoff for UE-V.</span></span> <span data-ttu-id="b0306-147">При выполнении задачи "Синхронизация параметров при выходе" запускается файл Microsoft.Uev.SyncController.exe, который находится в каталоге установки UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="b0306-147">The Synchronize Settings at Logoff task runs the Microsoft.Uev.SyncController.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b0306-148">Название задачи</span><span class="sxs-lookup"><span data-stu-id="b0306-148">Task name</span></span></th>
<th align="left"><span data-ttu-id="b0306-149">Событие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b0306-149">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0306-150">Параметры \Microsoft\UE-V\Synchronize при выходе из системы</span><span class="sxs-lookup"><span data-stu-id="b0306-150">\Microsoft\UE-V\Synchronize Settings at Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-151">Вторич</span><span class="sxs-lookup"><span data-stu-id="b0306-151">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b0306-152">Автоматическое обновление шаблона</span><span class="sxs-lookup"><span data-stu-id="b0306-152">Template Auto Update</span></span>

<span data-ttu-id="b0306-153">Задача " **Автоматическое обновление шаблона** " проверяет каталог шаблонов параметров на предмет новых, обновленных или удаленных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="b0306-153">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="b0306-154">Эта задача выполняется только в том случае, если настроена SettingsTemplateCatalog.</span><span class="sxs-lookup"><span data-stu-id="b0306-154">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="b0306-155">Задача " **Автоматическое обновление шаблона** " запускает ApplySettingsCatalog.exe файл, который находится в каталоге установки агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="b0306-155">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b0306-156">Название задачи</span><span class="sxs-lookup"><span data-stu-id="b0306-156">Task name</span></span></th>
<th align="left"><span data-ttu-id="b0306-157">Событие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b0306-157">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0306-158">Автоматическое обновление \Microsoft\UE-V\Template</span><span class="sxs-lookup"><span data-stu-id="b0306-158">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-159">Загрузка системы и в 3:30 – каждый день в любое время в течение 1 часового периода.</span><span class="sxs-lookup"><span data-stu-id="b0306-159">System startup and at 3:30 AM every day, at a random time within a 1-hour window</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b0306-160">**Пример:** Следующая команда настраивает агент UE-V Agent для проверки хранилища каталога шаблонов параметров каждый час.</span><span class="sxs-lookup"><span data-stu-id="b0306-160">**Example:** The following command configures the UE-V Agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### <span data-ttu-id="b0306-161">Отправка данных программы улучшения качества программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="b0306-161">Upload CEIP Data</span></span>

<span data-ttu-id="b0306-162">Задача « **Отправка данных CEIP** » запускается во время установки, если пользователь или администратор выбрал участие в программе улучшения качества программного обеспечения (CEIP).</span><span class="sxs-lookup"><span data-stu-id="b0306-162">The **Upload CEIP Data** task runs during the installation if the user or the administrator chose to participate in the Customer Experience Improvement Program (CEIP).</span></span> <span data-ttu-id="b0306-163">Эта задача передает данные на серверы программы улучшения качества программного обеспечения, в которых используются данные, чтобы улучшить продукт для будущих выпусков UE-V.</span><span class="sxs-lookup"><span data-stu-id="b0306-163">This task uploads the data to the CEIP servers where the data is used to help improve the product for future releases of UE-V.</span></span> <span data-ttu-id="b0306-164">Это запланированное задание запускается при входе в систему и каждые 4 часа позже.</span><span class="sxs-lookup"><span data-stu-id="b0306-164">This scheduled task runs at logon and every 4 hours afterwards.</span></span> <span data-ttu-id="b0306-165">Задача « **Отправка данных CEIP** » запускает файл UevSqmUploader.exe, который находится в каталоге установки агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="b0306-165">The **Upload CEIP data** task runs the UevSqmUploader.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b0306-166">Название задачи</span><span class="sxs-lookup"><span data-stu-id="b0306-166">Task name</span></span></th>
<th align="left"><span data-ttu-id="b0306-167">Событие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b0306-167">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0306-168">Данные \Microsoft\UE-V\Upload CEIP</span><span class="sxs-lookup"><span data-stu-id="b0306-168">\Microsoft\UE-V\Upload CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-169">При входе в систему и каждые 4 часа</span><span class="sxs-lookup"><span data-stu-id="b0306-169">At logon and every 4 hours</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b0306-170">Сведения о запланированной задаче UE-V 2</span><span class="sxs-lookup"><span data-stu-id="b0306-170">UE-V 2 Scheduled Task Details</span></span>


<span data-ttu-id="b0306-171">На следующей диаграмме приведены дополнительные сведения о запланированных задачах для UE-V 2.</span><span class="sxs-lookup"><span data-stu-id="b0306-171">The following chart provides additional information about scheduled tasks for UE-V 2:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b0306-172">Название задачи </strong> (имя файла)</span><span class="sxs-lookup"><span data-stu-id="b0306-172">Task Name</strong> (file name)</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="b0306-173">Частота по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b0306-173">Default Frequency</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b0306-174">Power Toggle</span><span class="sxs-lookup"><span data-stu-id="b0306-174">Power Toggle</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b0306-175">Только простое</span><span class="sxs-lookup"><span data-stu-id="b0306-175">Idle Only</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b0306-176">Сетевое подключение</span><span class="sxs-lookup"><span data-stu-id="b0306-176">Network Connection</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b0306-177">Описание</span><span class="sxs-lookup"><span data-stu-id="b0306-177">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b0306-178">Мониторинг параметров приложения </strong> (UevAppMonitor.exe)</span><span class="sxs-lookup"><span data-stu-id="b0306-178">Monitor Application Settings</strong> (UevAppMonitor.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-179">Запустится 30 секунд после входа в систему и будет продолжаться до выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="b0306-179">Starts 30 seconds after logon and continues until logoff.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-180">Нет</span><span class="sxs-lookup"><span data-stu-id="b0306-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-181">Да</span><span class="sxs-lookup"><span data-stu-id="b0306-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-182">Н/Д</span><span class="sxs-lookup"><span data-stu-id="b0306-182">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-183">Синхронизирует параметры для приложений для Windows (AppX).</span><span class="sxs-lookup"><span data-stu-id="b0306-183">Synchronizes settings for Windows (AppX) apps.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b0306-184">Приложение контроллера синхронизации </strong> (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="b0306-184">Sync Controller Application</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-185">При входе в систему и каждые 30 минут после.</span><span class="sxs-lookup"><span data-stu-id="b0306-185">At logon and every 30 min thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-186">Да</span><span class="sxs-lookup"><span data-stu-id="b0306-186">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-187">Да</span><span class="sxs-lookup"><span data-stu-id="b0306-187">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-188">Только при подключении к сети</span><span class="sxs-lookup"><span data-stu-id="b0306-188">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-189">Запускает контроллер синхронизации, который синхронизирует локальные параметры с расположением хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="b0306-189">Starts the Sync Controller which synchronizes local settings with the settings storage location.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b0306-190">Синхронизация параметров при выходе из системы </strong> (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="b0306-190">Synchronize Settings at Logoff</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-191">Запускается при входе в систему, а затем ждет выхода из системы для синхронизации параметров.</span><span class="sxs-lookup"><span data-stu-id="b0306-191">Runs at logon and then waits for Logoff to Synchronize settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-192">Нет</span><span class="sxs-lookup"><span data-stu-id="b0306-192">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-193">Да</span><span class="sxs-lookup"><span data-stu-id="b0306-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-194">Н/Д</span><span class="sxs-lookup"><span data-stu-id="b0306-194">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-195">Запускает приложение при входе в систему, которое управляет синхронизацией приложений при выходе из системы.</span><span class="sxs-lookup"><span data-stu-id="b0306-195">Start an application at logon that controls the synchronization of applications at logoff.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b0306-196">Автоматическое обновление шаблона </strong> (ApplySettingsCatalog.exe)</span><span class="sxs-lookup"><span data-stu-id="b0306-196">Template Auto Update</strong> (ApplySettingsCatalog.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-197">Запускается при первом входе в 3:30, а затем — каждый день.</span><span class="sxs-lookup"><span data-stu-id="b0306-197">Runs at initial logon and at 3:30 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-198">Да</span><span class="sxs-lookup"><span data-stu-id="b0306-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-199">Нет</span><span class="sxs-lookup"><span data-stu-id="b0306-199">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-200">Н/Д</span><span class="sxs-lookup"><span data-stu-id="b0306-200">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-201">Проверяет каталог шаблонов параметров на предмет новых, обновленных или удаленных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="b0306-201">Checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="b0306-202">Эта задача выполняется, только если настроена SettingsTemplateCatalog.</span><span class="sxs-lookup"><span data-stu-id="b0306-202">This task only runs if SettingsTemplateCatalog is configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b0306-203">Сбор данных для программы улучшения качества программного обеспечения </strong> (UevSqmSession.exe)</span><span class="sxs-lookup"><span data-stu-id="b0306-203">Collect CEIP data</strong> (UevSqmSession.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-204">При входе в службу запускается</span><span class="sxs-lookup"><span data-stu-id="b0306-204">At logon launches service</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-205">Нет</span><span class="sxs-lookup"><span data-stu-id="b0306-205">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-206">Да</span><span class="sxs-lookup"><span data-stu-id="b0306-206">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-207">Н/Д</span><span class="sxs-lookup"><span data-stu-id="b0306-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-208">Если пользователь или администратор в программе улучшения качества программного обеспечения (CEIP), эта задача собирает данные, которые помогают улучшить UE-V будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="b0306-208">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task collects data that helps improve UE-V future releases.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b0306-209">Отправка данных CEIP </strong> (UevSqmUploader.exe)</span><span class="sxs-lookup"><span data-stu-id="b0306-209">Upload CEIP Data</strong> (UevSqmUploader.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-210">Работает при входе в систему и в 4:00 – раз в день.</span><span class="sxs-lookup"><span data-stu-id="b0306-210">Runs at logon and at 4:00 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-211">Нет</span><span class="sxs-lookup"><span data-stu-id="b0306-211">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-212">Да</span><span class="sxs-lookup"><span data-stu-id="b0306-212">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-213">Только при подключении к сети</span><span class="sxs-lookup"><span data-stu-id="b0306-213">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0306-214">Если пользователь или администратор попытается войти в программу улучшения качества программного обеспечения (CEIP), эта задача передает данные на серверы программы улучшения качества программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="b0306-214">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task uploads the data to the CEIP servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="b0306-215">Списка</span><span class="sxs-lookup"><span data-stu-id="b0306-215">Legend</span></span>**

-   <span data-ttu-id="b0306-216">**Power Toggle** — планировщик заданий оптимизирует энергопотребление, если не подключен к сети переменного тока.</span><span class="sxs-lookup"><span data-stu-id="b0306-216">**Power Toggle** – Task Scheduler will optimize power consumption when not connected to AC power.</span></span> <span data-ttu-id="b0306-217">Задача может перестать работать, если компьютер переключается на питание от батареи.</span><span class="sxs-lookup"><span data-stu-id="b0306-217">The task might stop running if the computer switches to battery power.</span></span>

-   <span data-ttu-id="b0306-218">**Только в режиме бездействия** – задача будет остановлена, если компьютер прекратит работу.</span><span class="sxs-lookup"><span data-stu-id="b0306-218">**Idle Only** – The task will stop running if the computer ceases to be idle.</span></span> <span data-ttu-id="b0306-219">По умолчанию задача не будет перезапущена после простоя компьютера.</span><span class="sxs-lookup"><span data-stu-id="b0306-219">By default the task will not restart when the computer is idle again.</span></span> <span data-ttu-id="b0306-220">Вместо этого задача начнется снова при следующем триггере задачи.</span><span class="sxs-lookup"><span data-stu-id="b0306-220">Instead the task will begin again on the next task trigger.</span></span>

-   <span data-ttu-id="b0306-221">**Сетевое подключение** : задачи, помеченные как "Да", выполняются только в том случае, если на компьютере установлено сетевое подключение.</span><span class="sxs-lookup"><span data-stu-id="b0306-221">**Network Connection** – Tasks marked “Yes” only run if the computer has a network connection available.</span></span> <span data-ttu-id="b0306-222">Задачи, помеченные как "н/д", работают независимо от сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="b0306-222">Tasks marked “N/A” run regardless of network connectivity.</span></span>

### <span data-ttu-id="b0306-223">Управление запланированными задачами</span><span class="sxs-lookup"><span data-stu-id="b0306-223">How to Manage Scheduled Tasks</span></span>

<span data-ttu-id="b0306-224">Чтобы найти запланированные задачи, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0306-224">To find Scheduled Tasks, perform the following:</span></span>

1.  <span data-ttu-id="b0306-225">Откройте "Расписание задач" на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="b0306-225">Open “Schedule Tasks” on the user computer.</span></span>

2.  <span data-ttu-id="b0306-226">Перейти к: планировщик заданий — &gt; Библиотека планировщика заданий — &gt; Microsoft- &gt; UE-V</span><span class="sxs-lookup"><span data-stu-id="b0306-226">Navigate to: Task Scheduler -&gt; Task Scheduler Library -&gt; Microsoft -&gt; UE-V</span></span>

3.  <span data-ttu-id="b0306-227">Выберите запланированную задачу, которую вы хотите настроить, и настройте ее в области сведений.</span><span class="sxs-lookup"><span data-stu-id="b0306-227">Select the scheduled task you wish to manage and configure in the details pane.</span></span>

### <span data-ttu-id="b0306-228">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="b0306-228">Additional information</span></span>

<span data-ttu-id="b0306-229">Следующие дополнительные сведения применимы к запланированным задачам UE-V.</span><span class="sxs-lookup"><span data-stu-id="b0306-229">The following additional information applies to UE-V scheduled tasks:</span></span>

-   <span data-ttu-id="b0306-230">Все программы для последовательности задач находятся в папке установки агента UE-V (по `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` умолчанию).</span><span class="sxs-lookup"><span data-stu-id="b0306-230">ll task sequence programs are located in the UE-V Agent installation folder, `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\`, by default.</span></span>

-   <span data-ttu-id="b0306-231">Запланированная задача приложения контроллера синхронизации является важнейшим компонентом, если UE-V PowerSchool имеет значение "SyncProvider" (конфигурация по умолчанию UE-V 2).</span><span class="sxs-lookup"><span data-stu-id="b0306-231">The Sync Controller Application Scheduled task is the crucial component when the UE-V SyncMethod is set to “SyncProvider” (UE-V 2 default configuration).</span></span> <span data-ttu-id="b0306-232">Это запланированное задание синхронизирует SettingsSToragePath с локально кэшированными версиями файлов пакетов параметров.</span><span class="sxs-lookup"><span data-stu-id="b0306-232">This scheduled task keeps the SettingsSToragePath synchronized with the locally cached versions of the settings package files.</span></span> <span data-ttu-id="b0306-233">Если пользователи приводят к нечастой синхронизации параметров, вы можете уменьшить количество запланированных задач так, чтобы оно было меньше 1 минуты.</span><span class="sxs-lookup"><span data-stu-id="b0306-233">If users complain that settings do not synchronize often enough, then you can reduce the scheduled task setting to as little as 1 minute.</span></span><span data-ttu-id="b0306-234">При необходимости вы также можете увеличить значение по умолчанию: 30 мин на более высокое значение.</span><span class="sxs-lookup"><span data-stu-id="b0306-234"> You can also increase the 30 min default to a higher amount if necessary.</span></span> <span data-ttu-id="b0306-235">Если пользователи выдерживают, что параметры не синхронизируются достаточно быстро при входе в систему, вы можете удалить параметр задержки для запланированной задачи.</span><span class="sxs-lookup"><span data-stu-id="b0306-235">If users complain that settings do not synchronize fast enough on logon, then you can remove the delay setting for the scheduled task.</span></span> <span data-ttu-id="b0306-236">(Параметры задержки можно найти в диалоговом окне " **изменение триггера** ")</span><span class="sxs-lookup"><span data-stu-id="b0306-236">(You can find the delay setting in the **Edit Trigger** dialogue box)</span></span>

-   <span data-ttu-id="b0306-237">Вы не хотите отключать запланированную задачу "автоматическое обновление шаблона", если вы используете другой метод для синхронизации шаблонов клиентов (например, групповой политики или базовых планов Configuration Manager).</span><span class="sxs-lookup"><span data-stu-id="b0306-237">You do not need to disable the Template Auto Update scheduled task if you use another method to keep the clients’ templates in sync (i.e. Group Policy or Configuration Manager Baselines).</span></span> <span data-ttu-id="b0306-238">Если значение свойства SettingsTemplateCatalog оставлено пустым, UE-V не проверяет каталог параметров для настраиваемых шаблонов.</span><span class="sxs-lookup"><span data-stu-id="b0306-238">Leaving the SettingsTemplateCatalog property value blank prevents UE-V from checking the settings catalog for custom templates.</span></span> <span data-ttu-id="b0306-239">Это запланированное задание запускается ApplySettingsCatalog.exe и, в сущности, будет возвращаться немедленно.</span><span class="sxs-lookup"><span data-stu-id="b0306-239">This scheduled task runs ApplySettingsCatalog.exe and will essentially return immediately.</span></span>

-   <span data-ttu-id="b0306-240">Запланированная задача "Параметры приложения" обновляет параметры приложения для Windows (AppX) в режиме реального времени, основываясь на параметрах программы приложения Windows, встроенных в каждое приложение.</span><span class="sxs-lookup"><span data-stu-id="b0306-240">The Monitor Application Settings scheduled task will update Windows app (AppX) settings in real time, based on Windows app program setting triggers built into each app.</span></span>






## <span data-ttu-id="b0306-241">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b0306-241">Related topics</span></span>


[<span data-ttu-id="b0306-242">Администрирование UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="b0306-242">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="b0306-243">Развертывание UE-V 2. x для настраиваемых приложений</span><span class="sxs-lookup"><span data-stu-id="b0306-243">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 





