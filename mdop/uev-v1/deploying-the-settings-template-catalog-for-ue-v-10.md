---
title: Развертывание каталога шаблонов параметров для UE-V 1.0
description: Развертывание каталога шаблонов параметров для UE-V 1.0
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826632"
---
# <span data-ttu-id="8b605-103">Развертывание каталога шаблонов параметров для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="8b605-103">Deploying the Settings Template Catalog for UE-V 1.0</span></span>


<span data-ttu-id="8b605-104">Шаблоны расположений пользовательских параметров можно хранить на пути к папке на компьютерах с Microsoft User Experience Virtualization (UE-V) или в сетевом ресурсе SMB (Server Message Block).</span><span class="sxs-lookup"><span data-stu-id="8b605-104">Custom settings location templates can be stored on a folder path on Microsoft User Experience Virtualization (UE-V) computers or on a Server Message Block (SMB) network share.</span></span> <span data-ttu-id="8b605-105">Запланированная задача на компьютере проверяет наличие новых или обновленных шаблонов в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="8b605-105">A scheduled task on the computer checks for new or updated templates from this location.</span></span> <span data-ttu-id="8b605-106">Задача проверяет это расположение раз в день и обновляет режим синхронизации на основе шаблонов в этой папке.</span><span class="sxs-lookup"><span data-stu-id="8b605-106">The task checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="8b605-107">Шаблоны, добавленные или обновленные в этой папке, так как последняя проверка регистрируется агентом UE-V.</span><span class="sxs-lookup"><span data-stu-id="8b605-107">Templates that are added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="8b605-108">Агент UE-V отменяет регистрацию шаблонов, которые были удалены из этой папки.</span><span class="sxs-lookup"><span data-stu-id="8b605-108">The UE-V agent deregisters templates that were removed from this folder.</span></span> <span data-ttu-id="8b605-109">Запланированная задача выполняется как система.</span><span class="sxs-lookup"><span data-stu-id="8b605-109">The scheduled task runs as SYSTEM.</span></span> <span data-ttu-id="8b605-110">Как минимум, в сетевом общем доступе должны быть предоставлены разрешения для группы Domain Computers.</span><span class="sxs-lookup"><span data-stu-id="8b605-110">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="8b605-111">Кроме того, предоставьте разрешения на доступ к папке "сетевая папка" для администраторов, которые будут управлять сохраненными шаблонами.</span><span class="sxs-lookup"><span data-stu-id="8b605-111">In addition, grant access permissions for the network share folder to administrators who will manage the stored templates.</span></span> <span data-ttu-id="8b605-112">Дополнительные сведения о шаблонах расположений настраиваемых параметров можно найти в разделе [Планирование развертывания настраиваемого шаблона для UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="8b605-112">For more information about custom setting location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

**<span data-ttu-id="8b605-113">Настройка каталога шаблонов параметров для UE-V</span><span class="sxs-lookup"><span data-stu-id="8b605-113">To configure the settings template catalog for UE-V</span></span>**

1.  <span data-ttu-id="8b605-114">Создайте на компьютере новую папку, в которой будет храниться каталог шаблонов параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="8b605-114">Create a new folder on the computer that will store the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="8b605-115">Установите следующие разрешения на уровне общего доступа (SMB) для папки каталога шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="8b605-115">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="8b605-116">Учетная запись пользователя</span><span class="sxs-lookup"><span data-stu-id="8b605-116">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="8b605-117">Рекомендации по разрешениям</span><span class="sxs-lookup"><span data-stu-id="8b605-117">Recommend permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8b605-118">Все пользователи</span><span class="sxs-lookup"><span data-stu-id="8b605-118">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8b605-119">Нет разрешений</span><span class="sxs-lookup"><span data-stu-id="8b605-119">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8b605-120">Компьютеры домена</span><span class="sxs-lookup"><span data-stu-id="8b605-120">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8b605-121">Уровни разрешений "чтение"</span><span class="sxs-lookup"><span data-stu-id="8b605-121">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8b605-122">Администраторы</span><span class="sxs-lookup"><span data-stu-id="8b605-122">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8b605-123">Уровни разрешений на чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8b605-123">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="8b605-124">Установите следующие разрешения NTFS для папки каталога шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="8b605-124">Set the following NTFS permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="8b605-125">Учетная запись пользователя</span><span class="sxs-lookup"><span data-stu-id="8b605-125">User Account</span></span></th>
    <th align="left"><span data-ttu-id="8b605-126">Рекомендуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="8b605-126">Recommended Permissions</span></span></th>
    <th align="left"><span data-ttu-id="8b605-127">Применить к</span><span class="sxs-lookup"><span data-stu-id="8b605-127">Apply To</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8b605-128">Создатель/владелец</span><span class="sxs-lookup"><span data-stu-id="8b605-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8b605-129">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="8b605-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8b605-130">Эта папка, вложенные папки и файлы</span><span class="sxs-lookup"><span data-stu-id="8b605-130">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8b605-131">Компьютеры домена</span><span class="sxs-lookup"><span data-stu-id="8b605-131">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8b605-132">Просмотр содержимого папки и чтение</span><span class="sxs-lookup"><span data-stu-id="8b605-132">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8b605-133">Эта папка, вложенные папки и файлы</span><span class="sxs-lookup"><span data-stu-id="8b605-133">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8b605-134">Все пользователи</span><span class="sxs-lookup"><span data-stu-id="8b605-134">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8b605-135">Нет разрешений</span><span class="sxs-lookup"><span data-stu-id="8b605-135">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8b605-136">Нет разрешений</span><span class="sxs-lookup"><span data-stu-id="8b605-136">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8b605-137">Администраторы</span><span class="sxs-lookup"><span data-stu-id="8b605-137">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8b605-138">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="8b605-138">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8b605-139">Эта папка, вложенные папки и файлы</span><span class="sxs-lookup"><span data-stu-id="8b605-139">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="8b605-140">Нажмите кнопку **ОК** , чтобы закрыть диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="8b605-140">Click **OK** to close the dialog boxes.</span></span>

## <span data-ttu-id="8b605-141">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8b605-141">Related topics</span></span>


[<span data-ttu-id="8b605-142">Развертывание UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="8b605-142">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="8b605-143">Планирование развертывания пользовательского шаблона для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="8b605-143">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





