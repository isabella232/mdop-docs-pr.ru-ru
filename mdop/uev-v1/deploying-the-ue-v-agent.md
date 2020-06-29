---
title: Развертывание агента UE-V
description: Развертывание агента UE-V
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827182"
---
# <span data-ttu-id="7271e-103">Развертывание агента UE-V</span><span class="sxs-lookup"><span data-stu-id="7271e-103">Deploying the UE-V Agent</span></span>


<span data-ttu-id="7271e-104">Агент Microsoft User Experience Virtualization (UE-V) Agent должен выполняться на каждом компьютере, использующем UE-V для перемещения приложений и параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="7271e-104">The Microsoft User Experience Virtualization (UE-V) agent must run on each computer that uses UE-V to roam application and Windows settings.</span></span> <span data-ttu-id="7271e-105">Один файл установщика, AgentSetup.exe, устанавливает агент UE-V Agent как в 32-разрядной, так и в 64-разрядной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="7271e-105">A single installer file, AgentSetup.exe, installs the UE-V agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="7271e-106">Для агента UE-V используются следующие параметры командной строки:</span><span class="sxs-lookup"><span data-stu-id="7271e-106">The command-line parameters of the UE-V Agent are the following:</span></span>

**<span data-ttu-id="7271e-107">Параметры командной строки AgentSetup.exe</span><span class="sxs-lookup"><span data-stu-id="7271e-107">AgentSetup.exe command-line parameters</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="7271e-108">Параметр командной строки</span><span class="sxs-lookup"><span data-stu-id="7271e-108">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7271e-109">Определение</span><span class="sxs-lookup"><span data-stu-id="7271e-109">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7271e-110">Заметки</span><span class="sxs-lookup"><span data-stu-id="7271e-110">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7271e-111">/Help или/h или/?</span><span class="sxs-lookup"><span data-stu-id="7271e-111">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-112">Отображает диалоговое окно "использование AgentSetup.exe".</span><span class="sxs-lookup"><span data-stu-id="7271e-112">Displays the AgentSetup.exe usage dialog.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7271e-113">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="7271e-113">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-114">Указывает путь UNC (Universal Naming Convention), который определяет, где хранятся параметры.</span><span class="sxs-lookup"><span data-stu-id="7271e-114">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-115">% Username% или% ComputerName% принимают переменные среды.</span><span class="sxs-lookup"><span data-stu-id="7271e-115">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="7271e-116">Для выполнения сценариев могут потребоваться переменные с экранированием.</span><span class="sxs-lookup"><span data-stu-id="7271e-116">Scripting may require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="7271e-117">По умолчанию </strong> : &lt; нет &gt; (Домашняя страница пользователя Active Directory)</span><span class="sxs-lookup"><span data-stu-id="7271e-117">Default</strong>: &lt;none&gt; (Active Directory user home)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7271e-118">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="7271e-118">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-119">Указывает путь UNC, определяющий расположение, которое было проверено для новых шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="7271e-119">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-120">Требуется только для шаблонов местоположения настраиваемых параметров</span><span class="sxs-lookup"><span data-stu-id="7271e-120">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7271e-121">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="7271e-121">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-122">Указывает, следует ли регистрировать шаблоны Microsoft по умолчанию во время установки.</span><span class="sxs-lookup"><span data-stu-id="7271e-122">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-123">Истина | False</span><span class="sxs-lookup"><span data-stu-id="7271e-123">True | False</span></span></p>
<p><strong><span data-ttu-id="7271e-124">По умолчанию </strong> : истина</span><span class="sxs-lookup"><span data-stu-id="7271e-124">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7271e-125">PowerSchool</span><span class="sxs-lookup"><span data-stu-id="7271e-125">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-126">Указывает, какой метод синхронизации следует использовать.</span><span class="sxs-lookup"><span data-stu-id="7271e-126">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-127">OfflineFiles | Ничего</span><span class="sxs-lookup"><span data-stu-id="7271e-127">OfflineFiles | None</span></span></p>
<p><strong><span data-ttu-id="7271e-128">По умолчанию </strong> : OfflineFiles</span><span class="sxs-lookup"><span data-stu-id="7271e-128">Default</strong>: OfflineFiles</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7271e-129">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="7271e-129">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-130">Задает время ожидания (в миллисекундах), по истечении которого компьютер извлекает параметры пользователя из места хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="7271e-130">Specifies the number of milliseconds that the computer waits before timeout when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="7271e-131">По умолчанию </strong> : 2000 миллисекунд</span><span class="sxs-lookup"><span data-stu-id="7271e-131">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="7271e-132">(подождите до двух секунд)</span><span class="sxs-lookup"><span data-stu-id="7271e-132">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7271e-133">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="7271e-133">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-134">Указывает, включена или отключена синхронизация UE-V.</span><span class="sxs-lookup"><span data-stu-id="7271e-134">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-135">Истина | False</span><span class="sxs-lookup"><span data-stu-id="7271e-135">True | False</span></span></p>
<p><strong><span data-ttu-id="7271e-136">По умолчанию </strong> : истина</span><span class="sxs-lookup"><span data-stu-id="7271e-136">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7271e-137">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="7271e-137">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-138">Задает размер файла пакета параметров в байтах, когда агент UE-V сообщает, что файлы превышают пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="7271e-138">Specifies a settings package file size in bytes when the UE-V agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-139">&lt;Емкость&gt;</span><span class="sxs-lookup"><span data-stu-id="7271e-139">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="7271e-140">По умолчанию </strong> : нет (порог предупреждения отсутствует)</span><span class="sxs-lookup"><span data-stu-id="7271e-140">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7271e-141">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="7271e-141">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-142">Указывает параметр для участия в программе улучшения качества программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="7271e-142">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="7271e-143">Если установлено значение true, сведения об установщике загружаются на сайт программы улучшения качества программного обеспечения Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7271e-143">If set to true, then installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="7271e-144">Если задано значение false, сведения не передаются.</span><span class="sxs-lookup"><span data-stu-id="7271e-144">If set to false, then no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-145">Истина | False</span><span class="sxs-lookup"><span data-stu-id="7271e-145">True | False</span></span></p>
<p><strong><span data-ttu-id="7271e-146">По умолчанию </strong> : ложь</span><span class="sxs-lookup"><span data-stu-id="7271e-146">Default</strong>: False</span></span></p>
<p><strong><span data-ttu-id="7271e-147">В Windows 7 </strong> : истина</span><span class="sxs-lookup"><span data-stu-id="7271e-147">On Windows 7</strong>: True</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7271e-148">Во время установки параметр командной строки SettingsStoragePath указывает место хранения параметров для значений параметров.</span><span class="sxs-lookup"><span data-stu-id="7271e-148">During installation, the SettingsStoragePath command-line parameter specifies the settings storage location for the settings values.</span></span> <span data-ttu-id="7271e-149">Место хранения параметров может быть определено перед развертыванием агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="7271e-149">A settings storage location can be defined before deploying the UE-V Agent.</span></span> <span data-ttu-id="7271e-150">Если расположение хранилища параметров не определено, UE-V использует домашний каталог пользователя Active Directory в качестве места хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="7271e-150">If no settings storage location is defined, then UE-V uses the Active Directory user Home Directory as the settings storage location.</span></span> <span data-ttu-id="7271e-151">Когда вы указываете конфигурацию SettingsStoragePath во время настройки и используете% username% как часть значения, этот параметр будет перемещаться на всех компьютерах или сеансах, в которых пользователь входит в систему.</span><span class="sxs-lookup"><span data-stu-id="7271e-151">When you specify the SettingsStoragePath configuration during setup and use the %username% as part of the value, this will roam the same user settings experience on all computers or sessions that a user logs into.</span></span> <span data-ttu-id="7271e-152">Если указать переменные%username%\\%ComputerName% в качестве части значения SettingsStoragePath, это сохранит параметры для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="7271e-152">If you specify the %username%\\%computername% variables as part of the SettingsStoragePath value, this will preserve the settings experience for each computer.</span></span>

<span data-ttu-id="7271e-153">Файлы установщика Windows (MSI), зависящие от архитектуры, предоставляются для установки агента UE-V в дополнение к Объединенному установщику 32-и 64-разрядной версии.</span><span class="sxs-lookup"><span data-stu-id="7271e-153">Architecture-specific Windows Installer (.msi) files are provided for the UE-V agent installation in addition to the combined 32-bit and 64-bit installer.</span></span> <span data-ttu-id="7271e-154">Файлы установки AgentSetupx86.msi или AgentSetupx64.msi меньше файла AgentSetup.exe и могут ускорить развертывание агента.</span><span class="sxs-lookup"><span data-stu-id="7271e-154">The AgentSetupx86.msi or AgentSetupx64.msi install files are smaller than the AgentSetup.exe file and might streamline the agent deployments.</span></span> <span data-ttu-id="7271e-155">Параметры командной строки для установщика AgentSetup.exe поддерживаются для установки установщика Windows (MSI).</span><span class="sxs-lookup"><span data-stu-id="7271e-155">The command-line parameters for the AgentSetup.exe installer are supported for the Windows Installer (.msi) installation.</span></span>

<span data-ttu-id="7271e-156">**Примечание**  При установке или удалении агента UE-V вы можете либо использовать файл AgentSetup.exe, либо &lt; файл AgentSetup Arch &gt; . msi, но не оба варианта.</span><span class="sxs-lookup"><span data-stu-id="7271e-156">**Note** During UE-V agent installation or uninstallation you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="7271e-157">Один и тот же файл необходимо использовать для удаления агента UE-V, так как он использовался для установки UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="7271e-157">The same file must be used to uninstall the UE-V Agent as it was used to install the UE-V Agent.</span></span>

 

<span data-ttu-id="7271e-158">Убедитесь, что при установке агента UE-V используется правильный формат переменной.</span><span class="sxs-lookup"><span data-stu-id="7271e-158">Be sure to use the correct variable format when you install the UE-V agent.</span></span> <span data-ttu-id="7271e-159">В таблице ниже приведены примеры параметров развертывания для использования AgentSetup.exe или установочных файлов установщика Windows (MSI).</span><span class="sxs-lookup"><span data-stu-id="7271e-159">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) installation files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="7271e-160">Тип развертывания</span><span class="sxs-lookup"><span data-stu-id="7271e-160">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7271e-161">Описание развертывания</span><span class="sxs-lookup"><span data-stu-id="7271e-161">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7271e-162">Пример.</span><span class="sxs-lookup"><span data-stu-id="7271e-162">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7271e-163">Командная строка</span><span class="sxs-lookup"><span data-stu-id="7271e-163">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-164">При установке агента UE-V из командной строки используйте формат переменной% ^ username%.</span><span class="sxs-lookup"><span data-stu-id="7271e-164">When you install the UE-V agent from a command prompt, use the %^username% variable format.</span></span> <span data-ttu-id="7271e-165">Если кавычки необходимы из-за пробелов в пути к хранилищу параметров, используйте файл пакетного сценария для развертывания.</span><span class="sxs-lookup"><span data-stu-id="7271e-165">If quotation marks are needed because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7271e-166">Пакетный сценарий</span><span class="sxs-lookup"><span data-stu-id="7271e-166">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-167">При установке агента UE-V из пакетного файла сценария используйте формат переменной%% username%%.</span><span class="sxs-lookup"><span data-stu-id="7271e-167">When you install the UE-V Agent from a batch script file, use the %%username%% variable format.</span></span> <span data-ttu-id="7271e-168">Если вы используете этот метод установки, необходимо обменять переменную символом%%.</span><span class="sxs-lookup"><span data-stu-id="7271e-168">If you use this install method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="7271e-169">Без этого символа сценарий разворачивает переменную username во время установки, а не во время выполнения, что приводит к тому, что UE-V использует единое хранилище параметров для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="7271e-169">Without this character, the script expands the username variable at install time, rather than at run time, causing UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7271e-170">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7271e-170">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-171">При установке агента UE-V из запроса PowerShell или сценария PowerShell используйте формат переменной% username%.</span><span class="sxs-lookup"><span data-stu-id="7271e-171">When you install the UE-V agent from a PowerShell prompt or PowerShell script, use the %username% variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7271e-172">Электронное распространение программного обеспечения, например развертывание программного обеспечения Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7271e-172">Electronic software distribution, such as deployment of Configuration Manager Software Deployment)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7271e-173">При установке агента UE-V с помощью Configuration Manager используйте формат переменной ^% username ^%.</span><span class="sxs-lookup"><span data-stu-id="7271e-173">When you install the UE-V Agent with Configuration Manager, use the ^%username^% variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7271e-174">**Примечание**  Установка агента U-EV требует наличия прав администратора, и перед запуском агента UE-V может потребоваться перезагрузка компьютера.</span><span class="sxs-lookup"><span data-stu-id="7271e-174">**Note** The installation of the U-EV Agent requires Administrator rights and the computer will require a restart before the UE-V agent can run.</span></span>

 

## <span data-ttu-id="7271e-175">Методы развертывания агента UE-V из общей сетевой папке</span><span class="sxs-lookup"><span data-stu-id="7271e-175">UE-V Agent deployment methods from a network share</span></span>


<span data-ttu-id="7271e-176">Для развертывания агента UE-V можно использовать следующие методы:</span><span class="sxs-lookup"><span data-stu-id="7271e-176">You can use the following methods to deploy the UE-V agent:</span></span>

-   <span data-ttu-id="7271e-177">Решение для электронного распространения программного обеспечения, позволяющее установить файл установщика Windows (MSI).</span><span class="sxs-lookup"><span data-stu-id="7271e-177">An electronic software distribution (ESD) solution that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="7271e-178">Сценарий установки, который ссылается на файл установщика Windows (MSI), хранящийся централизованно в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="7271e-178">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="7271e-179">Запуск программы установки на компьютере вручную.</span><span class="sxs-lookup"><span data-stu-id="7271e-179">Manually running the installation program on the computer.</span></span>

<span data-ttu-id="7271e-180">Чтобы развернуть агент UE-V из сетевого общего доступа, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7271e-180">To deploy the UE-V agent from a network share, use the following steps:</span></span>

**<span data-ttu-id="7271e-181">Установка и настройка агента UE-V для сетевого общего доступа</span><span class="sxs-lookup"><span data-stu-id="7271e-181">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="7271e-182">Поэтапный файл установки агента UE-V (AgentSetup.exe) в сетевой папке, для которой пользователи имеют разрешение на чтение.</span><span class="sxs-lookup"><span data-stu-id="7271e-182">Stage the UE-V agent installation file (AgentSetup.exe) on a network share to which users have “read” permission.</span></span>

2.  <span data-ttu-id="7271e-183">Разверните сценарий на компьютерах пользователей, которые установили агент UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="7271e-183">Deploy a script to user computers that installs the UE-V agent.</span></span> <span data-ttu-id="7271e-184">В сценарии должно быть указано место хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="7271e-184">The script should specify the settings storage location.</span></span>

**<span data-ttu-id="7271e-185">Обновление агента UE-V</span><span class="sxs-lookup"><span data-stu-id="7271e-185">Update the UE-V Agent</span></span>**

<span data-ttu-id="7271e-186">Обновления программного обеспечения агента UE-V будут предоставляться с помощью центра обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7271e-186">Updates for the UE-V agent software will be provided through Microsoft Update.</span></span> <span data-ttu-id="7271e-187">Во время обновления агента UE-V можно обновить стандартную группу шаблонов расположений параметров для приложений Майкрософт и параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="7271e-187">During a UE-V agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings may be updated.</span></span> <span data-ttu-id="7271e-188">Обновления агента UE-V можно развертывать с помощью инфраструктуры для распространения программного обеспечения (ESD) предприятия.</span><span class="sxs-lookup"><span data-stu-id="7271e-188">UE-V agent updates can be deployed by using Enterprise Software Distribution (ESD) infrastructure.</span></span>

## <span data-ttu-id="7271e-189">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7271e-189">Related topics</span></span>


[<span data-ttu-id="7271e-190">Развертывание UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7271e-190">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="7271e-191">Поддерживаемые конфигурации UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7271e-191">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

[<span data-ttu-id="7271e-192">Развертывание места хранения параметров для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7271e-192">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

[<span data-ttu-id="7271e-193">Установка генератора UE-V</span><span class="sxs-lookup"><span data-stu-id="7271e-193">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="7271e-194">Развертывание агента виртуализации взаимодействия с пользователем</span><span class="sxs-lookup"><span data-stu-id="7271e-194">Deploy the User Experience Virtualization Agent</span></span>
 

 





