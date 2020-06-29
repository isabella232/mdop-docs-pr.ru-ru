---
title: Перенос пакетов параметров UE-V
description: Перенос пакетов параметров UE-V
author: dansimp
ms.assetid: 93d99254-3e17-4e96-92ad-87059d8554a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0087f334e916c06e7611d2671d0b50e7d1dd916
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823209"
---
# <span data-ttu-id="0cc9b-103">Перенос пакетов параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="0cc9b-103">Migrating UE-V Settings Packages</span></span>


<span data-ttu-id="0cc9b-104">В жизненном цикле развертывания Microsoft User Experience Virtualization (UE-V) может потребоваться переместить пакеты параметров пользователя при переходе на новый сервер или в целях резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) deployment, you might need to relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span> <span data-ttu-id="0cc9b-105">Миграция пакетов параметров может потребоваться в указанных ниже случаях.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-105">Migration of settings packages might be needed in the following scenarios:</span></span>

-   <span data-ttu-id="0cc9b-106">Обновление существующего серверного оборудования на более современный сервер.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="0cc9b-107">Миграция местоположения хранилища параметров из лаборатории на рабочий сервер.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-107">Migration of a settings storage location share from a lab to a production server.</span></span>

<span data-ttu-id="0cc9b-108">Копирование файлов и папок не сохранит параметры безопасности и разрешения.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-108">Simply copying the files and folders will not preserve the security settings and permissions.</span></span> <span data-ttu-id="0cc9b-109">Описанные ниже действия будут правильно копировать файлы пакета параметров с разрешениями NTFS на новый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-109">The following described steps will properly copy the settings package files with their NTFS permissions to a new share.</span></span>

**<span data-ttu-id="0cc9b-110">Сохранение пакетов параметров UE-V при переходе на новый сервер</span><span class="sxs-lookup"><span data-stu-id="0cc9b-110">How to preserve UE-V settings packages when migrating to a new server</span></span>**

1.  <span data-ttu-id="0cc9b-111">В новом расположении на другом сервере создайте новую папку. Например, MySettings.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-111">In a new location on a different server, create a new folder; for example, MySettings.</span></span>

2.  <span data-ttu-id="0cc9b-112">Отключите общий доступ для старой папки на старом сервере.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="0cc9b-113">Переместите существующие пакеты параметров на новый сервер с помощью средства Robocopy из командной строки.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-113">Move the existing settings packages to the new server with Robocopy from the command line.</span></span> <span data-ttu-id="0cc9b-114">Пример</span><span class="sxs-lookup"><span data-stu-id="0cc9b-114">For example:</span></span>

    ``` syntax
    c:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="0cc9b-115">**Примечание**  Для наблюдения за ходом копирования откройте MySettings.txt с помощью средства чтения файлов журнала, например Trace32.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-115">**Note** To monitor the copy progress, open MySettings.txt with a log file reader such as Trace32.</span></span>

     

4.  <span data-ttu-id="0cc9b-116">Предоставьте разрешения на доступ к новому общему доступу.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-116">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="0cc9b-117">Оставьте разрешения NTFS недоступными, так как они были установлены службой Robocopy.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-117">Leave the NTFS permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="0cc9b-118">На компьютерах, на которых запущен агент UE-V, обновите параметр конфигурации SettingsStoragePath, указав путь к новому общему ресурсу в формате UNC.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-118">On computers that run the UE-V agent, update the SettingsStoragePath configuration setting to the UNC path of the new share.</span></span>

## <span data-ttu-id="0cc9b-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0cc9b-119">Related topics</span></span>


[<span data-ttu-id="0cc9b-120">Администрирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="0cc9b-120">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="0cc9b-121">Операции в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="0cc9b-121">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





