---
title: Восстановление параметров приложений и системы Windows, синхронизированных с UE-V 1.0
description: Восстановление параметров приложений и системы Windows, синхронизированных с UE-V 1.0
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812376"
---
# <span data-ttu-id="0417a-103">Восстановление параметров приложений и системы Windows, синхронизированных с UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="0417a-103">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>


<span data-ttu-id="0417a-104">Функции WMI и PowerShell в Microsoft User Experience Virtualization (UE-V) предоставляют возможность восстанавливать пакеты параметров.</span><span class="sxs-lookup"><span data-stu-id="0417a-104">WMI and PowerShell features of Microsoft User Experience Virtualization (UE-V) provide the ability to restore settings packages.</span></span> <span data-ttu-id="0417a-105">Команды WMI и PowerShell позволяют восстанавливать параметры приложения и Windows в значениях параметров, которые были установлены на компьютере при первом запуске приложения после установки UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="0417a-105">WMI and PowerShell commands allow you to restore application and Windows settings to the settings values that were on the computer the first time the application launched after the UE-V Agent was installed.</span></span> <span data-ttu-id="0417a-106">Это действие по восстановлению выполняется отдельно для каждого приложения или параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="0417a-106">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="0417a-107">Эти параметры восстанавливаются при следующем запуске приложения или при входе пользователя в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="0417a-107">The settings are restored the next time that the application is run or when the user logs on to the operating system.</span></span>

**<span data-ttu-id="0417a-108">Восстановление параметров приложения и параметров Windows с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="0417a-108">To restore application settings and Windows settings with PowerShell</span></span>**

1.  <span data-ttu-id="0417a-109">Откройте окно Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0417a-109">Open the Windows PowerShell window.</span></span> <span data-ttu-id="0417a-110">Чтобы импортировать модуль PowerShell Microsoft UE-V, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0417a-110">To import the Microsoft UE-V PowerShell module, enter the following command:</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="0417a-111">Чтобы восстановить параметры приложения и параметры Windows, введите следующий командлет PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0417a-111">Enter the following PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="0417a-112">Командлет PowerShell</span><span class="sxs-lookup"><span data-stu-id="0417a-112">PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="0417a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="0417a-113">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0417a-114">Restore-UevUserSetting</span><span class="sxs-lookup"><span data-stu-id="0417a-114">Restore-UevUserSetting</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0417a-115">Восстанавливает параметры пользователя для приложения или восстанавливает группу параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="0417a-115">Restores the user settings for an application or restores a group of Windows settings</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="0417a-116">Восстановление параметров приложения и параметров Windows с помощью WMI</span><span class="sxs-lookup"><span data-stu-id="0417a-116">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="0417a-117">Откройте окно PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0417a-117">Open a PowerShell window.</span></span>

2.  <span data-ttu-id="0417a-118">Чтобы восстановить параметры приложения и параметры Windows, введите следующую команду WMI.</span><span class="sxs-lookup"><span data-stu-id="0417a-118">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="0417a-119">Команда WMI</span><span class="sxs-lookup"><span data-stu-id="0417a-119">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="0417a-120">Описание</span><span class="sxs-lookup"><span data-stu-id="0417a-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0417a-121">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class UserSettings-Name RestoreByTemplateId-ArgumentList &lt; template_ID&gt;</span><span class="sxs-lookup"><span data-stu-id="0417a-121">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0417a-122">Восстанавливает параметры пользователя для приложения или восстанавливает группу параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="0417a-122">Restores the user settings for an application or restores a group of Windows settings</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="0417a-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0417a-123">Related topics</span></span>


[<span data-ttu-id="0417a-124">Администрирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="0417a-124">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="0417a-125">Операции в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="0417a-125">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





