---
title: Изменение частоты запланированных задач UE-V
description: Изменение частоты запланированных задач UE-V
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822689"
---
# <span data-ttu-id="92b30-103">Изменение частоты запланированных задач UE-V</span><span class="sxs-lookup"><span data-stu-id="92b30-103">Changing the Frequency of UE-V Scheduled Tasks</span></span>


<span data-ttu-id="92b30-104">Установщик агента Microsoft User Experience Virtualization (UE-V), AgentSetup.exe, создает две запланированные задачи при установке агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="92b30-104">The Microsoft User Experience Virtualization (UE-V) Agent installer, AgentSetup.exe, creates two scheduled tasks during the UE-V Agent installation.</span></span> <span data-ttu-id="92b30-105">Две задачи — задача " **Автоматическое обновление шаблона** " и задача " **состояние места хранения** ".</span><span class="sxs-lookup"><span data-stu-id="92b30-105">The two tasks are the **Template Auto Update** task and the **Setting Storage Location Status** task.</span></span> <span data-ttu-id="92b30-106">Эти запланированные задачи не настраиваются с помощью средств UE-V.</span><span class="sxs-lookup"><span data-stu-id="92b30-106">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="92b30-107">Администраторы, которые хотят изменить запланированную задачу для этих элементов, могут создать сценарий, который использует параметры командной строки Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="92b30-107">Administrators who wish to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="92b30-108">Дополнительные сведения об Schtasks.exeх приведены в разделе [Использование программы Schtasks, exe для планирования задач в Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span><span class="sxs-lookup"><span data-stu-id="92b30-108">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

## <span data-ttu-id="92b30-109">Автоматическое обновление шаблона</span><span class="sxs-lookup"><span data-stu-id="92b30-109">Template Auto-Update</span></span>


<span data-ttu-id="92b30-110">Задача " **Автоматическое обновление шаблона** " проверяет каталог шаблонов параметров на предмет новых, обновленных или удаленных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="92b30-110">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="92b30-111">Эта задача выполняется только в том случае, если настроена SettingsTemplateCatalog.</span><span class="sxs-lookup"><span data-stu-id="92b30-111">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="92b30-112">Задача " **Автоматическое обновление шаблона** " запускает ApplySettingsCatalog.exe файл, который находится в каталоге установки UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="92b30-112">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent install directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="92b30-113">Название задачи</span><span class="sxs-lookup"><span data-stu-id="92b30-113">Task name</span></span></th>
<th align="left"><span data-ttu-id="92b30-114">Триггер по умолчанию</span><span class="sxs-lookup"><span data-stu-id="92b30-114">Default trigger</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92b30-115">Автоматическое обновление \Microsoft\UE-V\Template</span><span class="sxs-lookup"><span data-stu-id="92b30-115">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="92b30-116">3:30 – ежедневно</span><span class="sxs-lookup"><span data-stu-id="92b30-116">3:30 AM every day</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="92b30-117">**Пример:** Следующая команда настраивает агент для проверки хранилища каталога шаблонов параметров на каждый час.</span><span class="sxs-lookup"><span data-stu-id="92b30-117">**Example:** The following command configures the agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## <span data-ttu-id="92b30-118">Состояние места хранения параметров</span><span class="sxs-lookup"><span data-stu-id="92b30-118">Settings Storage Location Status</span></span>


<span data-ttu-id="92b30-119">В **параметрах задачи "состояние расположения хранилища** " выполняются следующие действия:</span><span class="sxs-lookup"><span data-stu-id="92b30-119">The **Setting Storage Location Status** task performs the following actions:</span></span>

1.  <span data-ttu-id="92b30-120">Проверка того, что папки UE-V по-прежнему закреплены или зарегистрированы с помощью функции "автономные файлы".</span><span class="sxs-lookup"><span data-stu-id="92b30-120">Checks to make sure the UE-V folders are still pinned or registered with the offline files feature.</span></span>

2.  <span data-ttu-id="92b30-121">Проверяет, находится ли расположение хранения параметров в автономном режиме или в сети.</span><span class="sxs-lookup"><span data-stu-id="92b30-121">Checks whether the settings storage location is offline or online.</span></span>

3.  <span data-ttu-id="92b30-122">Принудительная синхронизация с указанным интервалом, а не интервалом, используемым по умолчанию для автономных файлов.</span><span class="sxs-lookup"><span data-stu-id="92b30-122">Forces a synchronization on the specified interval instead of the default interval for offline files.</span></span>

4.  <span data-ttu-id="92b30-123">Синхронизирует все пакеты параметров, настроенные для предварительной выборки.</span><span class="sxs-lookup"><span data-stu-id="92b30-123">Synchronizes any settings packages that are configured to be pre-fetched.</span></span>

5.  <span data-ttu-id="92b30-124">Проверяет, изменился ли путь к корневому каталогу Active Directory.</span><span class="sxs-lookup"><span data-stu-id="92b30-124">Checks if the Active Directory home directory path has changed.</span></span>

6.  <span data-ttu-id="92b30-125">Записывает текущую конфигурацию хранилища параметров в следующем расположении:</span><span class="sxs-lookup"><span data-stu-id="92b30-125">Writes the current settings storage configuration under the following location</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="92b30-126">Название задачи</span><span class="sxs-lookup"><span data-stu-id="92b30-126">Task name</span></span></th>
    <th align="left"><span data-ttu-id="92b30-127">Триггер по умолчанию</span><span class="sxs-lookup"><span data-stu-id="92b30-127">Default trigger</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="92b30-128">Состояние места хранения \Microsoft\UE-V\Settings</span><span class="sxs-lookup"><span data-stu-id="92b30-128">\Microsoft\UE-V\Settings Storage Location Status</span></span></p></td>
    <td align="left"><p><span data-ttu-id="92b30-129">При входе в систему любого пользователя – после срабатывания триггера повторяется каждые 30 минут бесконечно.</span><span class="sxs-lookup"><span data-stu-id="92b30-129">At logon of any user – After triggered, repeat every 30 minutes indefinitely.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="92b30-130">**Пример:** Следующая команда настраивает агент на выполнение действия, находящиеся в каждый час.</span><span class="sxs-lookup"><span data-stu-id="92b30-130">**Example:** The following command configures the agent to run the action above every hour.</span></span>

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## <span data-ttu-id="92b30-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="92b30-131">Related topics</span></span>


[<span data-ttu-id="92b30-132">Администрирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="92b30-132">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="92b30-133">Операции в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="92b30-133">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





