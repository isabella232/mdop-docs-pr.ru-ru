---
title: Управление шаблонами расположения параметров UE-V 1.0 с помощью PowerShell и инструментария WMI
description: Управление шаблонами расположения параметров UE-V 1.0 с помощью PowerShell и инструментария WMI
author: dansimp
ms.assetid: 4b911c78-a5e9-4199-bfeb-72ab764d47c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8dab0997cdfaf7c96862fcce4bc012c3edfe0c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812493"
---
# <span data-ttu-id="4dc76-103">Управление шаблонами расположения параметров UE-V 1.0 с помощью PowerShell и инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="4dc76-103">Managing UE-V 1.0 Settings Location Templates Using PowerShell and WMI</span></span>


<span data-ttu-id="4dc76-104">Microsoft User Experience Virtualization (UE-V) использует шаблоны расположений параметров (XML-файлы), которые определяют параметры, зафиксированные и примененные с помощью виртуализации взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="4dc76-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="4dc76-105">UE-V включает набор стандартных шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="4dc76-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="4dc76-106">Кроме того, оно включает в себя средство для создания настраиваемых шаблонов расположения параметров с помощью UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="4dc76-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="4dc76-107">После создания и развертывания шаблонов расположений параметров вы можете управлять этими шаблонами с помощью PowerShell или WMI.</span><span class="sxs-lookup"><span data-stu-id="4dc76-107">After you create and deploy settings location templates you can manage those templates using PowerShell or WMI.</span></span>

## <span data-ttu-id="4dc76-108">Управление шаблонами расположений параметров с помощью WMI и PowerShell</span><span class="sxs-lookup"><span data-stu-id="4dc76-108">Manage settings location templates with WMI and PowerShell</span></span>


<span data-ttu-id="4dc76-109">Функции WMI и PowerShell в UE-V включают возможность включать, отключать, регистрировать, обновлять и отменять регистрацию шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="4dc76-109">The WMI and PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="4dc76-110">С помощью этих функций вы можете автоматизировать процесс регистрации, обновления и отмены регистрации шаблонов с помощью агента UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="4dc76-110">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V agent.</span></span> <span data-ttu-id="4dc76-111">Вы также можете вручную регистрировать шаблоны с помощью WMI и команд PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4dc76-111">You can also manually register templates using WMI and PowerShell commands.</span></span> <span data-ttu-id="4dc76-112">С помощью этих функций в сочетании с электронным решением для распространения программного обеспечения, групповой политикой или другим методом автоматического развертывания, таким как сценарий, вы можете автоматизировать этот процесс.</span><span class="sxs-lookup"><span data-stu-id="4dc76-112">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="4dc76-113">Для обновления, регистрации и отмены регистрации шаблона расположений параметров необходимы разрешения администратора.</span><span class="sxs-lookup"><span data-stu-id="4dc76-113">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="4dc76-114">Для включения и отключения шаблонов не требуются разрешения администратора.</span><span class="sxs-lookup"><span data-stu-id="4dc76-114">Administrator permissions are not required to enable or disable templates.</span></span>

**<span data-ttu-id="4dc76-115">Управление шаблонами расположений параметров с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="4dc76-115">To manage settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="4dc76-116">Используйте учетную запись с правами администратора, чтобы открыть окно Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4dc76-116">Use an account with administrator rights to open a Windows PowerShell window.</span></span> <span data-ttu-id="4dc76-117">Чтобы импортировать модуль **PowerShell Microsoft UE-V** , введите в командной строке PowerShell указанную ниже команду.</span><span class="sxs-lookup"><span data-stu-id="4dc76-117">To import the **Microsoft UE-V PowerShell** module, type the following command at the PowerShell command prompt.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="4dc76-118">Используйте следующие командлеты PowerShell для регистрации и управления шаблонами расположений параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="4dc76-118">Use the following PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="4dc76-119">Команда PowerShell</span><span class="sxs-lookup"><span data-stu-id="4dc76-119">PowerShell command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="4dc76-120">Описание</span><span class="sxs-lookup"><span data-stu-id="4dc76-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4dc76-121">Get-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="4dc76-121">Get-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-122">Список всех шаблонов расположений параметров, зарегистрированных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4dc76-122">Lists all the settings location templates registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4dc76-123">Регистрация — UevTemplate</span><span class="sxs-lookup"><span data-stu-id="4dc76-123">Register-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-124">Регистрирует шаблон расположения параметров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="4dc76-124">Registers a settings location template with UE-V.</span></span> <span data-ttu-id="4dc76-125">После регистрации шаблона UE-V синхронизирует параметры, определенные в шаблоне, между компьютерами с зарегистрированным шаблоном.</span><span class="sxs-lookup"><span data-stu-id="4dc76-125">Once a template is registered, UE-V will synchronize the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4dc76-126">Отмена регистрации — UevTemplate</span><span class="sxs-lookup"><span data-stu-id="4dc76-126">Unregister-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-127">Отмена регистрации шаблона расположения параметров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="4dc76-127">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="4dc76-128">После отмены регистрации шаблона UE-V больше не будет синхронизировать параметры, определенные в шаблоне, между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="4dc76-128">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4dc76-129">Update-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="4dc76-129">Update-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-130">Обновляет шаблон расположений параметров с более новой версией шаблона.</span><span class="sxs-lookup"><span data-stu-id="4dc76-130">Updates a settings location template with a more recent version of the template.</span></span> <span data-ttu-id="4dc76-131">Новый шаблон должен иметь версию, которая позже существующей.</span><span class="sxs-lookup"><span data-stu-id="4dc76-131">The new template should have a version that is later than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4dc76-132">Disable-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="4dc76-132">Disable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-133">Отключает шаблон расположения параметров для текущего пользователя компьютера.</span><span class="sxs-lookup"><span data-stu-id="4dc76-133">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4dc76-134">Enable-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="4dc76-134">Enable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-135">Включает шаблон расположения параметров для текущего пользователя компьютера.</span><span class="sxs-lookup"><span data-stu-id="4dc76-135">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4dc76-136">Test-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="4dc76-136">Test-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-137">Определяет, соответствует ли указанный шаблон расположению параметров своей XML-схеме.</span><span class="sxs-lookup"><span data-stu-id="4dc76-137">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="4dc76-138">Возможности UE-V PowerShell позволяют управлять группой шаблонов параметров, развернутых в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="4dc76-138">The UE-V PowerShell features allow you to manage a group of settings templates deployed in your enterprise.</span></span> <span data-ttu-id="4dc76-139">Чтобы управлять группой шаблонов с помощью PowerShell, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4dc76-139">To manage a group of templates using PowerShell, do the following.</span></span>

**<span data-ttu-id="4dc76-140">Управление группой шаблонов расположения параметров с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="4dc76-140">To manage a group of settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="4dc76-141">Измените или обновите шаблоны расположения нужных параметров.</span><span class="sxs-lookup"><span data-stu-id="4dc76-141">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="4dc76-142">Развертывание шаблонов расположений необходимых параметров в папке, доступной на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4dc76-142">Deploy the desired settings location templates to a folder accessible to the local computer.</span></span>

3.  <span data-ttu-id="4dc76-143">На локальном компьютере откройте окно Windows PowerShell с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="4dc76-143">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="4dc76-144">Импортируйте модуль PowerShell Microsoft UE-V, введя указанную ниже команду.</span><span class="sxs-lookup"><span data-stu-id="4dc76-144">Import the Microsoft UE-V PowerShell module, by typing the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

5.  <span data-ttu-id="4dc76-145">Отмените регистрацию всех ранее зарегистрированных версий шаблонов, введя указанную ниже команду.</span><span class="sxs-lookup"><span data-stu-id="4dc76-145">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    <span data-ttu-id="4dc76-146">Все активные шаблоны будут отменены на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4dc76-146">This will unregister all active templates on the computer.</span></span>

6.  <span data-ttu-id="4dc76-147">Зарегистрируйте обновленные шаблоны, введя указанную ниже команду.</span><span class="sxs-lookup"><span data-stu-id="4dc76-147">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="4dc76-148">Будут зарегистрированы все шаблоны расположений параметров, расположенные в указанной папке шаблона.</span><span class="sxs-lookup"><span data-stu-id="4dc76-148">This will register all of the settings location templates located in the specified template folder.</span></span>

<span data-ttu-id="4dc76-149">Виртуализация взаимодействия с пользователем предоставляет следующий набор команд WMI.</span><span class="sxs-lookup"><span data-stu-id="4dc76-149">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="4dc76-150">Администраторы могут использовать эти интерфейсы для управления шаблонами расположений параметров из Windows PowerShell и автоматизации задач администрирования шаблонов.</span><span class="sxs-lookup"><span data-stu-id="4dc76-150">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="4dc76-151">Управление шаблонами расположений параметров с помощью WMI</span><span class="sxs-lookup"><span data-stu-id="4dc76-151">To manage settings location templates with WMI</span></span>**

1.  <span data-ttu-id="4dc76-152">Используйте учетную запись с правами администратора, чтобы открыть окно Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4dc76-152">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="4dc76-153">Используйте следующие команды WMI для регистрации и управления шаблонами расположений параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="4dc76-153">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="4dc76-154">Команда PowerShell</span><span class="sxs-lookup"><span data-stu-id="4dc76-154">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="4dc76-155">Описание</span><span class="sxs-lookup"><span data-stu-id="4dc76-155">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4dc76-156">Get-WmiObject-Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId, TemplateName, TemplateVersion, Enabled | Форматирование таблицы с автоподбором</span><span class="sxs-lookup"><span data-stu-id="4dc76-156">Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-157">Список всех шаблонов расположений параметров, зарегистрированных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4dc76-157">Lists all the settings location templates registered for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4dc76-158">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-ArgumentList &lt; путь к шаблону&gt;</span><span class="sxs-lookup"><span data-stu-id="4dc76-158">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-159">Регистрирует шаблон расположения параметров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="4dc76-159">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4dc76-160">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name UnregisterByTemplateId-ArgumentList &lt; ID шаблона&gt;</span><span class="sxs-lookup"><span data-stu-id="4dc76-160">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-161">Отмена регистрации шаблона расположения параметров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="4dc76-161">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="4dc76-162">После отмены регистрации шаблона UE-V больше не будет синхронизировать параметры, определенные в шаблоне, между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="4dc76-162">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4dc76-163">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name EnableByTemplateId-ArgumentList &lt; ID шаблона&gt;</span><span class="sxs-lookup"><span data-stu-id="4dc76-163">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-164">Включает шаблон расположений параметров с UE-V</span><span class="sxs-lookup"><span data-stu-id="4dc76-164">Enables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4dc76-165">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name DisableByTemplateId-ArgumentList &lt; ID шаблона&gt;</span><span class="sxs-lookup"><span data-stu-id="4dc76-165">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-166">Отключает шаблон расположения параметров с UE-V</span><span class="sxs-lookup"><span data-stu-id="4dc76-166">Disables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4dc76-167">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name ArgumentList — &lt; путь к шаблону&gt;</span><span class="sxs-lookup"><span data-stu-id="4dc76-167">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-168">Обновляет шаблон расположений параметров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="4dc76-168">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="4dc76-169">Новый шаблон должен иметь более позднюю версию, чем существующий.</span><span class="sxs-lookup"><span data-stu-id="4dc76-169">The new template should have a version that is higher than the existing one.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4dc76-170">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Validate-ArgumentList &lt; путь к шаблону&gt;</span><span class="sxs-lookup"><span data-stu-id="4dc76-170">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4dc76-171">Определяет, соответствует ли указанный шаблон расположению параметров своей XML-схеме.</span><span class="sxs-lookup"><span data-stu-id="4dc76-171">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="4dc76-172">Развертывание агента UE-V с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="4dc76-172">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="4dc76-173">Поэтапный файл установщика UE-V в общедоступном сетевом общем доступе.</span><span class="sxs-lookup"><span data-stu-id="4dc76-173">Stage the UE-V installer file in an accessible network share.</span></span>

    <span data-ttu-id="4dc76-174">**Примечание**  Используйте AgentSetup.exe для развертывания 32-и 64-разрядных версий агента UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="4dc76-174">**Note** Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="4dc76-175">Для каждой архитектуры доступны файлы установщика Windows версии, AgentSetupx86.msi и AgentSetupx64.msi.</span><span class="sxs-lookup"><span data-stu-id="4dc76-175">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="4dc76-176">Чтобы позднее удалить агент UE-V с помощью файла установки, необходимо использовать тот же тип файлов.</span><span class="sxs-lookup"><span data-stu-id="4dc76-176">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>

     

2.  <span data-ttu-id="4dc76-177">Для установки агента используйте одну из следующих команд PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4dc76-177">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## <span data-ttu-id="4dc76-178">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4dc76-178">Related topics</span></span>


[<span data-ttu-id="4dc76-179">Управление агентом и пакетами UE-V 1.0 с помощью PowerShell и инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="4dc76-179">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[<span data-ttu-id="4dc76-180">Администрирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="4dc76-180">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="4dc76-181">Операции в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="4dc76-181">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





