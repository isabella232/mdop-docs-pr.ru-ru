---
title: Миграция пакетов параметров UE-V 2. x
description: Миграция пакетов параметров UE-V 2. x
author: dansimp
ms.assetid: f79381f4-e142-405c-b728-5c048502aa70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0aa1f1c36594d69de40306dfa70a4a0cf5c86dbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825519"
---
# <span data-ttu-id="bf899-103">Миграция пакетов параметров UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="bf899-103">Migrating UE-V 2.x Settings Packages</span></span>


<span data-ttu-id="bf899-104">В жизненном цикле приложения Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 или 2,1 SP1, возможно, потребуется переместить пакеты параметров пользователя при переходе на новый сервер или при выполнении резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bf899-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 deployment, you might have to relocate the user settings packages either when you migrate to a new server or when you perform backups.</span></span> <span data-ttu-id="bf899-105">Возможно, требуется миграция пакетов параметров в следующих сценариях.</span><span class="sxs-lookup"><span data-stu-id="bf899-105">Settings packages might have to be migrated in the following scenarios:</span></span>

-   <span data-ttu-id="bf899-106">Обновление существующего серверного оборудования на более современный сервер.</span><span class="sxs-lookup"><span data-stu-id="bf899-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="bf899-107">Миграция местоположения хранилища параметров с тестового сервера на рабочий сервер.</span><span class="sxs-lookup"><span data-stu-id="bf899-107">Migration of a settings storage location share from a test server to a production server.</span></span>

<span data-ttu-id="bf899-108">При копировании файлов и папок не сохраняются параметры безопасности и разрешения.</span><span class="sxs-lookup"><span data-stu-id="bf899-108">Simply copying the files and folders does not preserve the security settings and permissions.</span></span> <span data-ttu-id="bf899-109">Ниже описаны действия, которые необходимо выполнить, чтобы правильно скопировать пакет параметров вместе с разрешениями файловой системы NTFS на новый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="bf899-109">The following steps describe how to correctly copy the settings package along with their NTFS file system permissions to a new share.</span></span>

**<span data-ttu-id="bf899-110">Сохранение пакетов параметров UE-V 2 при переходе на новый сервер</span><span class="sxs-lookup"><span data-stu-id="bf899-110">To preserve UE-V 2 settings packages when you migrate to a new server</span></span>**

1.  <span data-ttu-id="bf899-111">В новом расположении на другом сервере создайте новую папку, например MySettings.</span><span class="sxs-lookup"><span data-stu-id="bf899-111">In a new location on a different server, create a new folder, for example, MySettings.</span></span>

2.  <span data-ttu-id="bf899-112">Отключите общий доступ для старой папки на старом сервере.</span><span class="sxs-lookup"><span data-stu-id="bf899-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="bf899-113">Копирование существующих пакетов параметров на новый сервер с помощью средства Robocopy</span><span class="sxs-lookup"><span data-stu-id="bf899-113">To copy the existing settings packages to the new server with Robocopy</span></span>

    ``` syntax
    C:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="bf899-114">**Примечание**  Для наблюдения за ходом копирования откройте MySettings.txt с помощью средства просмотра журнала, например Trace32.</span><span class="sxs-lookup"><span data-stu-id="bf899-114">**Note** To monitor the copy progress, open MySettings.txt with a log viewer such as Trace32.</span></span>

     

4.  <span data-ttu-id="bf899-115">Предоставьте разрешения на доступ к новому общему доступу.</span><span class="sxs-lookup"><span data-stu-id="bf899-115">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="bf899-116">Оставьте разрешения на доступ к файловой системе NTFS, так как они были установлены программой Robocopy.</span><span class="sxs-lookup"><span data-stu-id="bf899-116">Leave the NTFS file system permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="bf899-117">На компьютерах, на которых запущен агент UE-V, обновите параметр конфигурации **SettingsStoragePath** , указав путь к новому общему ресурсу в формате UNC (Universal Naming Convention).</span><span class="sxs-lookup"><span data-stu-id="bf899-117">On computers that run the UE-V Agent, update the **SettingsStoragePath** configuration setting to the Universal Naming Convention (UNC) path of the new share.</span></span>

    <span data-ttu-id="bf899-118">**У вас есть предложение UE-V**?</span><span class="sxs-lookup"><span data-stu-id="bf899-118">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="bf899-119">Здесь вы можете добавить предложения и проголосовать [здесь](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="bf899-119">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="bf899-120">**У вас возникла ошибка UE-V**?</span><span class="sxs-lookup"><span data-stu-id="bf899-120">**Got a UE-V issue**?</span></span> <span data-ttu-id="bf899-121">Воспользуйтесь [форумом на сайте UE-V TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="bf899-121">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="bf899-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="bf899-122">Related topics</span></span>


[<span data-ttu-id="bf899-123">Администрирование UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="bf899-123">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





