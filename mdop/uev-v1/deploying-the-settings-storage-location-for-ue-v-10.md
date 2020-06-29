---
title: Развертывание места хранения параметров для UE-V 1.0
description: Развертывание места хранения параметров для UE-V 1.0
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826639"
---
# <span data-ttu-id="7a4ce-103">Развертывание места хранения параметров для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7a4ce-103">Deploying the Settings Storage Location for UE-V 1.0</span></span>


<span data-ttu-id="7a4ce-104">Для развертывания Microsoft User Experience Virtualization (UE-V) требуется место хранения параметров, в котором пользовательские параметры хранятся в файле пакета параметров.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-104">Microsoft User Experience Virtualization (UE-V) deployment requires a settings storage location where the user settings are stored in a settings package file.</span></span> <span data-ttu-id="7a4ce-105">Место хранения параметров можно настроить одним из следующих двух способов:</span><span class="sxs-lookup"><span data-stu-id="7a4ce-105">The settings storage location can be configured in one of the following two ways:</span></span>

-   <span data-ttu-id="7a4ce-106">**Корневой каталог Active Directory** — если для пользователя в Active Directory определен основной каталог, агент UE-V будет использовать это расположение для хранения параметров пакетов расположений.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-106">**Active Directory home directory** – if a home directory is defined for the user in Active Directory, the UE-V agent will use this location to store settings location packages.</span></span> <span data-ttu-id="7a4ce-107">Агент UE-V динамически создает папку хранилища для определенного пользователя под корнем основного каталога.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-107">The UE-V agent dynamically creates the user-specific storage folder below the root of the home directory.</span></span> <span data-ttu-id="7a4ce-108">Агент использует только основной каталог в службе каталогов Active Directory, если расположение хранилища параметров не определено.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-108">The agent only uses the home directory of the Active Directory if a settings storage location is not defined.</span></span>

-   <span data-ttu-id="7a4ce-109">**Создание общего доступа к хранилищу параметров** — общий доступ к хранилищу параметров — это стандартная Сетевая учетная запись, доступная для пользователей UE-V.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-109">**Create a settings storage share** – the settings storage share is a standard network share that is accessible by UE-V users.</span></span>

## <span data-ttu-id="7a4ce-110">Развертывание параметра "общий доступ к хранилищу параметров UE-V"</span><span class="sxs-lookup"><span data-stu-id="7a4ce-110">Deploy a UE-V settings storage share</span></span>


<span data-ttu-id="7a4ce-111">При создании общего доступа к хранилищу параметров Ограничьте доступ только тем пользователям, которым нужен доступ.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-111">When you create the settings storage share, you should limit access only to users that need access.</span></span> <span data-ttu-id="7a4ce-112">Необходимые разрешения указаны в таблицах ниже.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-112">The necessary permissions are shown in the tables below.</span></span>

**<span data-ttu-id="7a4ce-113">Развертывание сетевого общего доступа UE-V</span><span class="sxs-lookup"><span data-stu-id="7a4ce-113">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="7a4ce-114">Создайте новую группу безопасности для пользователей UE-V.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-114">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="7a4ce-115">Создайте новую папку на центральном компьютере, где будут храниться пакеты параметров UE-V, а затем предоставьте пользователям UE-V разрешения на доступ к этой папке.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-115">Create a new folder on the centrally located computer that will store the UE-V settings packages, and then grant the UE-V users with group permissions to the folder.</span></span> <span data-ttu-id="7a4ce-116">Администратору, поддерживающему UE-V, потребуется разрешение на доступ к этой общей папке.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-116">The administrator supporting UE-V will need permissions to this shared folder.</span></span>

3.  <span data-ttu-id="7a4ce-117">Установите следующие разрешения на уровне общего доступа (SMB) для папки "Настройка места хранения":</span><span class="sxs-lookup"><span data-stu-id="7a4ce-117">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="7a4ce-118">Учетная запись пользователя</span><span class="sxs-lookup"><span data-stu-id="7a4ce-118">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="7a4ce-119">Рекомендуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="7a4ce-119">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7a4ce-120">Все пользователи</span><span class="sxs-lookup"><span data-stu-id="7a4ce-120">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7a4ce-121">Нет разрешений</span><span class="sxs-lookup"><span data-stu-id="7a4ce-121">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7a4ce-122">Группа безопасности пользователей UE-V</span><span class="sxs-lookup"><span data-stu-id="7a4ce-122">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7a4ce-123">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="7a4ce-123">Full Control</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="7a4ce-124">Задайте следующие разрешения NTFS для папки "расположение хранилища параметров".</span><span class="sxs-lookup"><span data-stu-id="7a4ce-124">Set the following NTFS permissions for the settings storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="7a4ce-125">Учетная запись пользователя</span><span class="sxs-lookup"><span data-stu-id="7a4ce-125">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="7a4ce-126">Рекомендуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="7a4ce-126">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="7a4ce-127">Папка</span><span class="sxs-lookup"><span data-stu-id="7a4ce-127">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7a4ce-128">Создатель/владелец</span><span class="sxs-lookup"><span data-stu-id="7a4ce-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7a4ce-129">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="7a4ce-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7a4ce-130">Только для вложенных папок и файлов</span><span class="sxs-lookup"><span data-stu-id="7a4ce-130">Subfolders and Files Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7a4ce-131">Группа безопасности пользователей UE-V</span><span class="sxs-lookup"><span data-stu-id="7a4ce-131">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7a4ce-132">Просмотр папки/Чтение данных, создание папок и добавление данных</span><span class="sxs-lookup"><span data-stu-id="7a4ce-132">List Folder/Read Data, Create Folders/Append Data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7a4ce-133">Только для этой папки</span><span class="sxs-lookup"><span data-stu-id="7a4ce-133">This Folder Only</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

5.  <span data-ttu-id="7a4ce-134">Нажмите кнопку **ОК** , чтобы закрыть диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-134">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="7a4ce-135">С помощью этой конфигурации разрешений пользователи могут создавать папки для хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-135">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="7a4ce-136">Агент UE-V создает и защищает `settingspackage` папку во время работы в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-136">The UE-V agent creates and secures a `settingspackage` folder while running in the context of the user.</span></span> <span data-ttu-id="7a4ce-137">Пользователь получает полный доступ к своей `settingspackage` папке.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-137">The user receives full control to their `settingspackage` folder.</span></span> <span data-ttu-id="7a4ce-138">Другие пользователи не наследуют доступ к этой папке.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-138">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="7a4ce-139">Вам не нужно создавать и защищать отдельные каталоги пользователей, так как это будет сделано автоматически агентом, который запускается в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-139">You do not need to create and secure individual user directories, because this will be done automatically by the agent that runs in the context of the user.</span></span>

<span data-ttu-id="7a4ce-140">**Примечание**  Дополнительную защиту можно настроить, когда используется сервер Windows для общего доступа к хранилищу параметров.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-140">**Note** Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="7a4ce-141">UE-V можно настроить так, чтобы убедиться в том, что группа локального администратора или текущий пользователь является владельцем папки, в которой хранятся пакеты параметров.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-141">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="7a4ce-142">Чтобы включить дополнительную защиту, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-142">To enable additional security complete the following:</span></span>

1.  <span data-ttu-id="7a4ce-143">Добавьте раздел реестра **reg \ _DWORD** с именем "RepositoryOwnerCheckEnabled" в раздел **hKey \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration.**</span><span class="sxs-lookup"><span data-stu-id="7a4ce-143">Add a **REG\_DWORD** registry key named "RepositoryOwnerCheckEnabled" to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration.**</span></span>

2.  <span data-ttu-id="7a4ce-144">Задайте для раздела реестра значение 1.</span><span class="sxs-lookup"><span data-stu-id="7a4ce-144">Set registry key value to 1.</span></span>

 

## <span data-ttu-id="7a4ce-145">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7a4ce-145">Related topics</span></span>


[<span data-ttu-id="7a4ce-146">Развертывание UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7a4ce-146">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="7a4ce-147">Поддерживаемые конфигурации UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7a4ce-147">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

<span data-ttu-id="7a4ce-148">Развертывание центрального хранилища для шаблонов и параметров настройки виртуализации пользователя [Установка UE-V Generator](installing-the-ue-v-generator.md)</span><span class="sxs-lookup"><span data-stu-id="7a4ce-148">Deploy the Central Storage for User Experience Virtualization Settings Templates and Settings Packages [Installing the UE-V Generator](installing-the-ue-v-generator.md)</span></span>

[<span data-ttu-id="7a4ce-149">Развертывание агента UE-V</span><span class="sxs-lookup"><span data-stu-id="7a4ce-149">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

 

 





