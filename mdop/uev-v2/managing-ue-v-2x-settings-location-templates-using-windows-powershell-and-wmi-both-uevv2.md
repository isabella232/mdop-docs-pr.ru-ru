---
title: Управление шаблонами расположений параметров UE-V 2. x с помощью Windows PowerShell и WMI
description: Управление шаблонами расположений параметров UE-V 2. x с помощью Windows PowerShell и WMI
author: dansimp
ms.assetid: b5253050-acc3-4274-90d0-1fa4c480331d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9788ff1a11f1c70e52b75dd2187a198f5472f77f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812880"
---
# <span data-ttu-id="171ad-103">Управление шаблонами расположений параметров UE-V 2. x с помощью Windows PowerShell и WMI</span><span class="sxs-lookup"><span data-stu-id="171ad-103">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</span></span>


<span data-ttu-id="171ad-104">Виртуализация взаимодействия с пользователем Microsoft (UE-V) 2,0, 2,1 и 2,1 SP1 используют шаблоны расположения XML-параметров для определения параметров, которые захватывает и применяется виртуализация пользователя.</span><span class="sxs-lookup"><span data-stu-id="171ad-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the settings that User Experience Virtualization captures and applies.</span></span> <span data-ttu-id="171ad-105">UE-V включает набор стандартных шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="171ad-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="171ad-106">Кроме того, оно включает в себя средство для создания настраиваемых шаблонов расположения параметров с помощью UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="171ad-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="171ad-107">После создания и развертывания шаблонов расположений параметров можно управлять этими шаблонами с помощью Windows PowerShell и инструментария управления Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="171ad-107">After you create and deploy settings location templates, you can manage those templates by using Windows PowerShell and the Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="171ad-108">Полный список командлетов PowerShell для UE-V можно найти в [справочнике по командлетам UE-v 2](https://go.microsoft.com/fwlink/p/?LinkId=393495) ( https://go.microsoft.com/fwlink/p/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="171ad-108">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/p/?LinkId=393495) (https://go.microsoft.com/fwlink/p/?LinkId=393495).</span></span>

## <span data-ttu-id="171ad-109">Управление шаблонами расположений параметров UE-V 2 с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="171ad-109">Manage UE-V 2 settings location templates by using Windows PowerShell</span></span>


<span data-ttu-id="171ad-110">Возможности WMI и Windows PowerShell для UE-V включают возможность включать, отключать, регистрировать, обновлять и отменять регистрацию шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="171ad-110">The WMI and Windows PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="171ad-111">С помощью этих функций вы можете автоматизировать процесс регистрации, обновления и отмены регистрации шаблонов с помощью агента UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="171ad-111">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V Agent.</span></span> <span data-ttu-id="171ad-112">Вы также можете вручную зарегистрировать шаблоны с помощью WMI и команд Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="171ad-112">You can also manually register templates by using WMI and Windows PowerShell commands.</span></span> <span data-ttu-id="171ad-113">С помощью этих функций в сочетании с электронным решением для распространения программного обеспечения, групповой политикой или другим методом автоматического развертывания, таким как сценарий, вы можете автоматизировать этот процесс.</span><span class="sxs-lookup"><span data-stu-id="171ad-113">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="171ad-114">Для обновления, регистрации и отмены регистрации шаблона расположений параметров необходимы разрешения администратора.</span><span class="sxs-lookup"><span data-stu-id="171ad-114">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="171ad-115">Для включения, отключения и использования шаблонов списков не требуются разрешения администратора.</span><span class="sxs-lookup"><span data-stu-id="171ad-115">Administrator permissions are not required to enable, disable, or list templates.</span></span>

***<em><span data-ttu-id="171ad-116">Управление шаблонами расположений параметров с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="171ad-116">To manage settings location templates by using Windows PowerShell</span></span>ell</em>***

1.  <span data-ttu-id="171ad-117">Используйте учетную запись с правами администратора, чтобы открыть командную команду Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="171ad-117">Use an account with administrator rights to open a Windows PowerShell command prompt.</span></span>

2.  <span data-ttu-id="171ad-118">Используйте указанные ниже командлеты Windows PowerShell для регистрации и управления шаблонами расположений параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="171ad-118">Use the following Windows PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="171ad-119">Команда Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="171ad-119">Windows PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="171ad-120">Описание</span><span class="sxs-lookup"><span data-stu-id="171ad-120">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-121">Список всех шаблонов расположений параметров, зарегистрированных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="171ad-121">Lists all the settings location templates that are registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-122">Перечисляются все шаблоны расположений параметров, которые зарегистрированы на компьютере, где имя приложения или шаблона содержит &lt; строку &gt; .</span><span class="sxs-lookup"><span data-stu-id="171ad-122">Lists all the settings location templates that are registered on the computer where the application name or template name contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-123">Перечисляются все шаблоны расположений параметров, которые зарегистрированы на компьютере, где идентификатор шаблона содержит &lt; строку &gt; .</span><span class="sxs-lookup"><span data-stu-id="171ad-123">Lists all the settings location templates that are registered on the computer where the template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-124">Перечисляются все шаблоны расположений параметров, которые зарегистрированы на компьютере, где имя приложения или шаблона или идентификатор шаблона содержат &lt; строку &gt; .</span><span class="sxs-lookup"><span data-stu-id="171ad-124">Lists all the settings location templates that are registered on the computer where the application or template name, or template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-125">Получает имя программы и сведения о версии, которые зависят от идентификатора шаблона.</span><span class="sxs-lookup"><span data-stu-id="171ad-125">Gets the name of the program and version information, which depend on the template ID.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-126">Получает эффективный список приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-126">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-127">Получает список приложений Windows, настроенных для компьютера.</span><span class="sxs-lookup"><span data-stu-id="171ad-127">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-128">Получает список приложений для Windows, которые настроены для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="171ad-128">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-129">Регистрирует один или несколько шаблонов расположений параметров с UE-V с помощью относительных путей и (или) подстановочных знаков в путях к файлам.</span><span class="sxs-lookup"><span data-stu-id="171ad-129">Registers one or more settings location template with UE-V by using relative paths and/or wildcard characters in file paths.</span></span> <span data-ttu-id="171ad-130">После регистрации шаблона UE-V синхронизирует параметры, определенные в шаблоне, между компьютерами с зарегистрированным шаблоном.</span><span class="sxs-lookup"><span data-stu-id="171ad-130">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-131">Регистрирует один или несколько шаблонов расположений параметров с UE-V с помощью литеральных путей, где ни один из символов не может интерпретироваться как подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="171ad-131">Registers one or more settings location template with UE-V by using literal paths, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="171ad-132">После регистрации шаблона UE-V синхронизирует параметры, определенные в шаблоне, между компьютерами с зарегистрированным шаблоном.</span><span class="sxs-lookup"><span data-stu-id="171ad-132">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-133">Отмена регистрации шаблона расположения параметров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="171ad-133">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="171ad-134">При отмене регистрации шаблона UE-V больше не синхронизирует параметры, определенные в шаблоне, между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="171ad-134">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-135">Отмена регистрации всех шаблонов расположений параметров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="171ad-135">Unregisters all settings location templates with UE-V.</span></span> <span data-ttu-id="171ad-136">При отмене регистрации шаблона UE-V больше не синхронизирует параметры, определенные в шаблоне, между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="171ad-136">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-137">Обновляет один или несколько шаблонов расположений параметров с более поздней версией шаблона.</span><span class="sxs-lookup"><span data-stu-id="171ad-137">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="171ad-138">Используйте относительные пути и (или) подстановочные знаки в путях к файлам.</span><span class="sxs-lookup"><span data-stu-id="171ad-138">Use relative paths and/or wildcard characters in the file paths.</span></span> <span data-ttu-id="171ad-139">Новый шаблон должен иметь более новую версию, чем существующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="171ad-139">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-140">Обновляет один или несколько шаблонов расположений параметров с более поздней версией шаблона.</span><span class="sxs-lookup"><span data-stu-id="171ad-140">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="171ad-141">Используйте полные пути к файлам шаблонов, в которых нельзя интерпретировать символы как подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="171ad-141">Use full paths to template files, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="171ad-142">Новый шаблон должен иметь более новую версию, чем существующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="171ad-142">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-143">Удаление одного или нескольких приложений для Windows из списка компьютеров приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-143">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-144">Удаляет приложение для Windows из списка текущих приложений пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-144">Removes Windows app from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-145">Удаляет все приложения для Windows из списка компьютеров приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-145">Removes all Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-146">Удаляет одно или несколько приложений для Windows из текущего пользователя в списке приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-146">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-147">Удаляет все приложения для Windows из списка текущих приложений пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-147">Removes all Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-148">Отключает шаблон расположения параметров для текущего пользователя компьютера.</span><span class="sxs-lookup"><span data-stu-id="171ad-148">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-149">Отключение одного или нескольких приложений для Windows в списке приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-149">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-150">Отключение одного или нескольких приложений для Windows в текущем списке приложений пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-150">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-151">Включает шаблон расположения параметров для текущего пользователя компьютера.</span><span class="sxs-lookup"><span data-stu-id="171ad-151">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-152">Включает одно или несколько приложений для Windows в списке приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-152">Enables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-153">Включает одно или несколько приложений для Windows в списке приложений для Windows текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="171ad-153">Enables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-154">Определяет соответствие одного или нескольких шаблонов расположению параметров с XML-схемой.</span><span class="sxs-lookup"><span data-stu-id="171ad-154">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="171ad-155">Может использовать относительные пути и подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="171ad-155">Can use relative paths and wildcard characters.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-156">Определяет соответствие одного или нескольких шаблонов расположению параметров с XML-схемой.</span><span class="sxs-lookup"><span data-stu-id="171ad-156">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="171ad-157">Путь должен представлять собой полный путь к файлу шаблона, но не содержит подстановочных знаков.</span><span class="sxs-lookup"><span data-stu-id="171ad-157">The path must be a full path to the template file, but does not include wildcard characters.</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="171ad-158">Функции UE-V Windows PowerShell позволяют управлять группой шаблонов параметров, которые развернуты в Организации.</span><span class="sxs-lookup"><span data-stu-id="171ad-158">The UE-V Windows PowerShell features enable you to manage a group of settings templates that are deployed in your enterprise.</span></span> <span data-ttu-id="171ad-159">Чтобы управлять группой шаблонов с помощью Windows PowerShell, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="171ad-159">Use the following procedure to manage a group of templates by using Windows PowerShell.</span></span>

**<span data-ttu-id="171ad-160">Управление группой шаблонов расположений параметров с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="171ad-160">To manage a group of settings location templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="171ad-161">Измените или обновите шаблоны расположения нужных параметров.</span><span class="sxs-lookup"><span data-stu-id="171ad-161">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="171ad-162">Если вы хотите изменить или обновить шаблоны расположений параметров, разверните эти шаблоны расположений в папку, доступную на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="171ad-162">If you want to modify or update the settings location templates, deploy those settings location templates to a folder that is accessible to the local computer.</span></span>

3.  <span data-ttu-id="171ad-163">На локальном компьютере откройте окно Windows PowerShell с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="171ad-163">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="171ad-164">Отмените регистрацию всех ранее зарегистрированных версий шаблонов, введя указанную ниже команду.</span><span class="sxs-lookup"><span data-stu-id="171ad-164">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Unregister-UevTemplate -All
    ```

    <span data-ttu-id="171ad-165">Эта команда отменяет регистрацию всех активных шаблонов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="171ad-165">This command unregisters all active templates on the computer.</span></span>

5.  <span data-ttu-id="171ad-166">Зарегистрируйте обновленные шаблоны, введя указанную ниже команду.</span><span class="sxs-lookup"><span data-stu-id="171ad-166">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="171ad-167">Эта команда регистрирует все шаблоны расположений параметров, которые находятся в указанной папке шаблона.</span><span class="sxs-lookup"><span data-stu-id="171ad-167">This command registers all of the settings location templates that are located in the specified template folder.</span></span>

### <a href="" id="win8applist"></a><span data-ttu-id="171ad-168">Список приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="171ad-168">Windows app list</span></span>

<span data-ttu-id="171ad-169">Заполнив список приложений для Windows в списке приложений для Windows, вы указываете, будет ли это приложение включено или отключено для синхронизации параметров.</span><span class="sxs-lookup"><span data-stu-id="171ad-169">By listing a Windows app in the Windows app list, you specify whether that app is enabled or disabled for settings synchronization.</span></span> <span data-ttu-id="171ad-170">Приложения определяются в списке по их названию семейства пакетов и следует ли включать или отключать синхронизацию параметров для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="171ad-170">Apps are identified in the list by their Package Family name and whether settings synchronization should be enabled or disabled for that app.</span></span> <span data-ttu-id="171ad-171">При использовании этих параметров вместе с параметром "непоставленный режим синхронизации по умолчанию" можно управлять синхронизацией приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-171">When you use these settings along with the Unlisted Default Sync Behavior setting, you can control whether Windows apps are synchronized.</span></span>

<span data-ttu-id="171ad-172">Чтобы отобразить имя семейства пакетов установленных приложений для Windows, в командной строке Windows PowerShell введите:</span><span class="sxs-lookup"><span data-stu-id="171ad-172">To display the Package Family Name of installed Windows apps, at a Windows PowerShell command prompt, enter:</span></span>

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

<span data-ttu-id="171ad-173">Чтобы отобразить список приложений для Windows, которые могут синхронизировать параметры на компьютере с именем семейства пакетов, включенным состоянием и включенным источником, в командной строке Windows PowerShell введите:</span><span class="sxs-lookup"><span data-stu-id="171ad-173">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="171ad-174">Определения свойств Get-UevAppxPackage</span><span class="sxs-lookup"><span data-stu-id="171ad-174">Definitions of Get-UevAppxPackage properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="171ad-175">DisplayName</span><span class="sxs-lookup"><span data-stu-id="171ad-175">DisplayName</span></span>**  
<span data-ttu-id="171ad-176">Имя, которое отображается для пользователя в приложении центра параметров компании.</span><span class="sxs-lookup"><span data-stu-id="171ad-176">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="171ad-177">`DisplayName`Свойство является производным от `PackageFamilyName` Свойства.</span><span class="sxs-lookup"><span data-stu-id="171ad-177">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="171ad-178">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="171ad-178">PackageFamilyName</span></span>**  
<span data-ttu-id="171ad-179">Имя пакета, установленного для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="171ad-179">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="171ad-180">Включено</span><span class="sxs-lookup"><span data-stu-id="171ad-180">Enabled</span></span>**  
<span data-ttu-id="171ad-181">Определяет, настроены ли параметры для приложения для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="171ad-181">Defines whether the settings for the app are configured to synchronize.</span></span>

<a href="" id="enabledsource"></a>**<span data-ttu-id="171ad-182">EnabledSource</span><span class="sxs-lookup"><span data-stu-id="171ad-182">EnabledSource</span></span>**  
<span data-ttu-id="171ad-183">Расположение, в котором задана конфигурация, включающая или отключающее приложение.</span><span class="sxs-lookup"><span data-stu-id="171ad-183">The location where the configuration that enables or disables the app is set.</span></span> <span data-ttu-id="171ad-184">Возможные значения: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*и *PolicyUser*.</span><span class="sxs-lookup"><span data-stu-id="171ad-184">Possible values are: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*, and *PolicyUser*.</span></span>

<a href="" id="notset"></a>**<span data-ttu-id="171ad-185">NotSet (Не задано)</span><span class="sxs-lookup"><span data-stu-id="171ad-185">NotSet</span></span>**  
<span data-ttu-id="171ad-186">Политика не настроена для синхронизации этого приложения.</span><span class="sxs-lookup"><span data-stu-id="171ad-186">The policy is not configured to synchronize this app.</span></span>

<a href="" id="localmachine"></a>**<span data-ttu-id="171ad-187">Хранилище</span><span class="sxs-lookup"><span data-stu-id="171ad-187">LocalMachine</span></span>**  
<span data-ttu-id="171ad-188">Включенное состояние задается в разделе реестра на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="171ad-188">The enabled state is set in the local computer section of the registry.</span></span>

<a href="" id="localuser"></a>**<span data-ttu-id="171ad-189">LocalUser</span><span class="sxs-lookup"><span data-stu-id="171ad-189">LocalUser</span></span>**  
<span data-ttu-id="171ad-190">Включенное состояние задается в разделе реестра текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="171ad-190">The enabled state is set in the current user section of the registry.</span></span>

<a href="" id="policymachine"></a>**<span data-ttu-id="171ad-191">PolicyMachine</span><span class="sxs-lookup"><span data-stu-id="171ad-191">PolicyMachine</span></span>**  
<span data-ttu-id="171ad-192">Включенное состояние задается в разделе Политика раздела локальный компьютер в реестре.</span><span class="sxs-lookup"><span data-stu-id="171ad-192">The enabled state is set in the policy section of the local computer section of the registry.</span></span>

<span data-ttu-id="171ad-193">Чтобы получить список приложений для Windows, настраиваемый пользователем, в командной строке Windows PowerShell введите:</span><span class="sxs-lookup"><span data-stu-id="171ad-193">To get the user-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –CurrentComputerUser`

<span data-ttu-id="171ad-194">Чтобы получить список приложений для Windows, настроенный на компьютере, в командной строке Windows PowerShell введите:</span><span class="sxs-lookup"><span data-stu-id="171ad-194">To get the computer-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –Computer`

<span data-ttu-id="171ad-195">Для параметра CurrentComputerUser или Computer командлет возвращает список приложений для Windows, которые настроены на уровне пользователя или компьютера.</span><span class="sxs-lookup"><span data-stu-id="171ad-195">For either parameter, CurrentComputerUser or Computer, the cmdlet returns a list of the Windows apps that are configured at the user or at the computer level.</span></span>

**<span data-ttu-id="171ad-196">Определения свойств</span><span class="sxs-lookup"><span data-stu-id="171ad-196">Definitions of properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="171ad-197">DisplayName</span><span class="sxs-lookup"><span data-stu-id="171ad-197">DisplayName</span></span>**  
<span data-ttu-id="171ad-198">Имя, которое отображается для пользователя в приложении центра параметров компании.</span><span class="sxs-lookup"><span data-stu-id="171ad-198">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="171ad-199">`DisplayName`Свойство является производным от `PackageFamilyName` Свойства.</span><span class="sxs-lookup"><span data-stu-id="171ad-199">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="171ad-200">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="171ad-200">PackageFamilyName</span></span>**  
<span data-ttu-id="171ad-201">Имя пакета, установленного для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="171ad-201">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="171ad-202">Включено</span><span class="sxs-lookup"><span data-stu-id="171ad-202">Enabled</span></span>**  
<span data-ttu-id="171ad-203">Определяет, настроены ли параметры для приложения для синхронизации определенного коммутатора, то есть **пользователя** или **компьютера**.</span><span class="sxs-lookup"><span data-stu-id="171ad-203">Defines whether the settings for the app are configured to synchronize for the specified switch, that is, **user** or **computer**.</span></span>

<a href="" id="installed"></a>**<span data-ttu-id="171ad-204">Установлено</span><span class="sxs-lookup"><span data-stu-id="171ad-204">Installed</span></span>**  
<span data-ttu-id="171ad-205">Значение true, если приложение (например, PackageFamilyName установлен для текущего пользователя).</span><span class="sxs-lookup"><span data-stu-id="171ad-205">True if the app, that is, the PackageFamilyName is installed for the current user.</span></span>

### <span data-ttu-id="171ad-206">Управление шаблонами расположений параметров UE-V 2 с помощью WMI</span><span class="sxs-lookup"><span data-stu-id="171ad-206">Manage UE-V 2 settings location templates by using WMI</span></span>

<span data-ttu-id="171ad-207">Виртуализация взаимодействия с пользователем предоставляет следующий набор команд WMI.</span><span class="sxs-lookup"><span data-stu-id="171ad-207">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="171ad-208">Администраторы могут использовать эти интерфейсы для управления шаблонами расположений параметров из Windows PowerShell и автоматизации задач администрирования шаблонов.</span><span class="sxs-lookup"><span data-stu-id="171ad-208">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="171ad-209">Управление шаблонами расположений параметров с помощью WMI</span><span class="sxs-lookup"><span data-stu-id="171ad-209">To manage settings location templates by using WMI</span></span>**

1.  <span data-ttu-id="171ad-210">Используйте учетную запись с правами администратора, чтобы открыть окно Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="171ad-210">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="171ad-211">Используйте следующие команды WMI для регистрации и управления шаблонами расположений параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="171ad-211">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="171ad-212">Описание</span><span class="sxs-lookup"><span data-stu-id="171ad-212">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-213">Список всех шаблонов расположений параметров, зарегистрированных для компьютера.</span><span class="sxs-lookup"><span data-stu-id="171ad-213">Lists all the settings location templates that are registered for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-214">Получает имя программы и сведения о версии, которые зависят от имени шаблона.</span><span class="sxs-lookup"><span data-stu-id="171ad-214">Gets the name of the program and version information, which depends on the template name.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-215">Получает эффективный список приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-215">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="171ad-216">Get-WmiObject-Namespace root\Microsoft\UEV MachineConfiguredWindows8App</span><span class="sxs-lookup"><span data-stu-id="171ad-216">Get-WmiObject -Namespace root\Microsoft\UEV MachineConfiguredWindows8App</span></span></p></td>
    <td align="left"><p><span data-ttu-id="171ad-217">Получает список приложений Windows, настроенных для компьютера.</span><span class="sxs-lookup"><span data-stu-id="171ad-217">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-218">Получает список приложений для Windows, которые настроены для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="171ad-218">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-219">Регистрирует шаблон расположения параметров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="171ad-219">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-220">Отмена регистрации шаблона расположения параметров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="171ad-220">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="171ad-221">После отмены регистрации шаблона UE-V больше не синхронизирует параметры, определенные в шаблоне, между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="171ad-221">As soon as a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-222">Обновляет шаблон расположений параметров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="171ad-222">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="171ad-223">Новый шаблон должен иметь более новую версию, чем существующий.</span><span class="sxs-lookup"><span data-stu-id="171ad-223">The new template should be a newer version than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-224">Удаление одного или нескольких приложений для Windows из списка компьютеров приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-224">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-225">Удаляет одно или несколько приложений для Windows из текущего пользователя в списке приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-225">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-226">Отключает один или несколько шаблонов расположений параметров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="171ad-226">Disables one or more settings location templates with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-227">Отключение одного или нескольких приложений для Windows в списке приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-227">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-228">Отключение одного или нескольких приложений для Windows в текущем списке приложений пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-228">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-229">Включает шаблон расположений параметров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="171ad-229">Enables a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-230">Включает приложения для Windows в списке приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="171ad-230">Enables Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-231">Позволяет приложениям для Windows в списке приложений для Windows текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="171ad-231">Enables Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="171ad-232">Определяет, соответствует ли указанный шаблон расположению параметров своей XML-схеме.</span><span class="sxs-lookup"><span data-stu-id="171ad-232">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### <span data-ttu-id="171ad-233">Развертывание агента UE-V с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="171ad-233">Deploying the UE-V Agent using Windows PowerShell</span></span>

**<span data-ttu-id="171ad-234">Развертывание агента UE-V с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="171ad-234">How to deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="171ad-235">Поэтапный пакет установки агента UE-V в общедоступном сетевом общем доступе.</span><span class="sxs-lookup"><span data-stu-id="171ad-235">Stage the UE-V Agent installation package in an accessible network share.</span></span>

    **<span data-ttu-id="171ad-236">Примечание.</span><span class="sxs-lookup"><span data-stu-id="171ad-236">Note</span></span>**  
    <span data-ttu-id="171ad-237">Используйте AgentSetup.exe для развертывания 32-и 64-разрядных версий агента UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="171ad-237">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="171ad-238">Для каждой архитектуры доступны пакеты установщика Windows, AgentSetupx86.msi и AgentSetupx64.msi.</span><span class="sxs-lookup"><span data-stu-id="171ad-238">The Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="171ad-239">Чтобы позднее удалить агент UE-V с помощью файла установки, необходимо использовать тот же тип файлов.</span><span class="sxs-lookup"><span data-stu-id="171ad-239">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="171ad-240">Используйте одну из следующих команд Windows PowerShell, чтобы установить агент UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="171ad-240">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

<span data-ttu-id="171ad-241">**У вас есть предложение UE-V**?</span><span class="sxs-lookup"><span data-stu-id="171ad-241">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="171ad-242">Здесь вы можете добавить предложения и проголосовать [здесь](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="171ad-242">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="171ad-243">**У вас возникла ошибка UE-V**?</span><span class="sxs-lookup"><span data-stu-id="171ad-243">**Got a UE-V issue**?</span></span> <span data-ttu-id="171ad-244">Воспользуйтесь [форумом на сайте UE-V TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="171ad-244">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="171ad-245">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="171ad-245">Related topics</span></span>


[<span data-ttu-id="171ad-246">Администрирование UE-V 2. x с помощью Windows PowerShell и WMI</span><span class="sxs-lookup"><span data-stu-id="171ad-246">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="171ad-247">Администрирование UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="171ad-247">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









