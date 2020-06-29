---
title: Управление параметрами конфигурации рабочей области MED-V
description: Управление параметрами конфигурации рабочей области MED-V
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826159"
---
# <span data-ttu-id="addb0-103">Управление параметрами конфигурации рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="addb0-103">Managing MED-V Workspace Configuration Settings</span></span>


<span data-ttu-id="addb0-104">Microsoft Enterprise Virtualization (MED-V) 2,0 хранит параметры конфигурации в реестре.</span><span class="sxs-lookup"><span data-stu-id="addb0-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 stores its configuration settings in the registry.</span></span> <span data-ttu-id="addb0-105">Данные, которые мы включаем сюда для работы с реестром, могут помочь вам лучше управлять службами MED-V.</span><span class="sxs-lookup"><span data-stu-id="addb0-105">The information we include here about the registry may help you better manage your MED-V services.</span></span>

<span data-ttu-id="addb0-106">При поиске значений результирующих параметров для MED-V используется следующий путь поиска:</span><span class="sxs-lookup"><span data-stu-id="addb0-106">MED-V uses the following search path when looking for the resultant settings values:</span></span>

<span data-ttu-id="addb0-107">MED-V сначала выполняет поиск в политике компьютера.</span><span class="sxs-lookup"><span data-stu-id="addb0-107">MED-V first looks in the machine policy.</span></span>

<span data-ttu-id="addb0-108">Если значение не найдено, MED-V выполняет поиск в политике пользователя.</span><span class="sxs-lookup"><span data-stu-id="addb0-108">If the value is not found, MED-V looks in the user policy.</span></span>

<span data-ttu-id="addb0-109">Если значение не найдено, MED-V будет выглядеть в кусте HKEY \ _LOCAL \ _MACHINE \\System.</span><span class="sxs-lookup"><span data-stu-id="addb0-109">If the value is not found, MED-V looks in the HKEY\_LOCAL\_MACHINE\\System hive.</span></span>

<span data-ttu-id="addb0-110">Если значение не найдено, MED-V будет выглядеть в кусте реестра HKEY \ _CURRENT USER.</span><span class="sxs-lookup"><span data-stu-id="addb0-110">If the value is not found, MED-V looks in the HKEY\_CURRENT USER registry hive.</span></span>

<span data-ttu-id="addb0-111">Если значение по-прежнему не найдено, для MED-V используется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="addb0-111">If the value is still not found, MED-V uses the default.</span></span>

<span data-ttu-id="addb0-112">Общие рекомендации — это установка значения в кусте HKEY \ _LOCAL \ _MACHINE \\System или в политике компьютера.</span><span class="sxs-lookup"><span data-stu-id="addb0-112">A general best practice is to set the value in the HKEY\_LOCAL\_MACHINE\\System hive or in the machine policy.</span></span> <span data-ttu-id="addb0-113">Но если вы хотите, чтобы конечный пользователь мог настроить определенный параметр, его следует оставить.</span><span class="sxs-lookup"><span data-stu-id="addb0-113">But if you want the end user to be able to configure a particular setting, then you should leave it out.</span></span>

**<span data-ttu-id="addb0-114">Примечание.</span><span class="sxs-lookup"><span data-stu-id="addb0-114">Note</span></span>**  
<span data-ttu-id="addb0-115">Перед развертыванием рабочих областей MED-V вы можете использовать редактор сценариев для изменения сценария Windows PowerShell (PS1-файла), созданного с помощью упаковщика рабочих областей для задолженности.</span><span class="sxs-lookup"><span data-stu-id="addb0-115">Before you deploy your MED-V workspaces, you can use a script editor to change the Windows PowerShell script (.ps1 file) that the MED-V workspace packager created.</span></span> <span data-ttu-id="addb0-116">Дополнительные сведения можно найти в разделе [Настройка дополнительных параметров с помощью Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="addb0-116">For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span></span>

<span data-ttu-id="addb0-117">После развертывания рабочих областей MED-V вы можете изменить определенные параметры конфигурации MED-V, изменив записи в реестре.</span><span class="sxs-lookup"><span data-stu-id="addb0-117">After you have deployed your MED-V workspaces, you can change certain MED-V configuration settings by editing the registry entries.</span></span>



<span data-ttu-id="addb0-118">В этом разделе перечислены все настраиваемые разделы реестра для MED-V и описаны их использование.</span><span class="sxs-lookup"><span data-stu-id="addb0-118">This section lists all the configurable MED-V registry keys and explains their uses.</span></span>

## <span data-ttu-id="addb0-119">Ключ диагностики</span><span class="sxs-lookup"><span data-stu-id="addb0-119">Diagnostics Key</span></span>


<span data-ttu-id="addb0-120">В таблице ниже приведены сведения о значениях реестра, связанных с клавишей HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="addb0-120">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="addb0-121">Имя</span><span class="sxs-lookup"><span data-stu-id="addb0-121">Name</span></span> </th>
<th align="left"><span data-ttu-id="addb0-122">Тип</span><span class="sxs-lookup"><span data-stu-id="addb0-122">Type</span></span> </th>
<th align="left"><span data-ttu-id="addb0-123">Данные и по умолчанию</span><span class="sxs-lookup"><span data-stu-id="addb0-123">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="addb0-124">Описание</span><span class="sxs-lookup"><span data-stu-id="addb0-124">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-125">EventLogLevel</span><span class="sxs-lookup"><span data-stu-id="addb0-125">EventLogLevel</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-126">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-127">По умолчанию = 3</span><span class="sxs-lookup"><span data-stu-id="addb0-127">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-128">Тип данных, которые регистрируются в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="addb0-128">The type of information that is logged in the event log.</span></span> <span data-ttu-id="addb0-129">Ниже указаны уровни: 0 (нет), 1 (ошибка), 2 (предупреждение), 3 (сведения), 4 (Отладка).</span><span class="sxs-lookup"><span data-stu-id="addb0-129">Levels include the following: 0 (None), 1 (Error), 2 (Warning), 3 (Information), 4 (Debug).</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="addb0-130">Клавиша FTS</span><span class="sxs-lookup"><span data-stu-id="addb0-130">Fts Key</span></span>


<span data-ttu-id="addb0-131">В таблице ниже приведены сведения о значениях реестра, связанных с клавишей HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Fts.</span><span class="sxs-lookup"><span data-stu-id="addb0-131">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Fts key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="addb0-132">Имя</span><span class="sxs-lookup"><span data-stu-id="addb0-132">Name</span></span></th>
<th align="left"><span data-ttu-id="addb0-133">Тип</span><span class="sxs-lookup"><span data-stu-id="addb0-133">Type</span></span></th>
<th align="left"><span data-ttu-id="addb0-134">Данные и по умолчанию</span><span class="sxs-lookup"><span data-stu-id="addb0-134">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="addb0-135">Описание</span><span class="sxs-lookup"><span data-stu-id="addb0-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-136">AddUserToAdminGroupEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-136">AddUserToAdminGroupEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-137">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-137">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-138">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="addb0-138">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-139">Настройка автоматического добавления конечных пользователей в группу Администратор&#39;s.</span><span class="sxs-lookup"><span data-stu-id="addb0-139">Configures whether first time setup automatically adds the end user to the administrator&#39;s group.</span></span> <span data-ttu-id="addb0-140">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-140">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-141">0 = false: при первом запуске программы установки автоматически не добавляется конечный пользователь в группу Администратор&#39;s.</span><span class="sxs-lookup"><span data-stu-id="addb0-141">0 = false: First time setup does not automatically add the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-142">1 = true: при первом запуске программа установки автоматически добавляет пользователя в группу Администратор&#39;s.</span><span class="sxs-lookup"><span data-stu-id="addb0-142">1 = true: First time setup automatically adds the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-143">ComputerNameMask</span><span class="sxs-lookup"><span data-stu-id="addb0-143">ComputerNameMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-144">SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-144">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-145">MEDV\*</span><span class="sxs-lookup"><span data-stu-id="addb0-145">MEDV\*</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-146">Маска имени компьютера, которая используется для создания гостевой виртуальной машины&#39;s имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="addb0-146">The computer name mask that is used to create the guest virtual machine&#39;s computer name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-147">Маска может содержать тег% username%, чтобы вставить имя пользователя как часть имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="addb0-147">The mask can contain a %username% tag to insert the username as part of the computer name.</span></span> <span data-ttu-id="addb0-148">Аналогичным образом, тег% hostname% вставляет имя главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="addb0-148">Likewise, the %hostname% tag inserts the name of the host computer.</span></span></p>
<p><span data-ttu-id="addb0-149">Каждый &quot; # &quot; символ маски заменяется случайной цифрой.</span><span class="sxs-lookup"><span data-stu-id="addb0-149">Every &quot;#&quot; character in the mask is replaced by a random digit.</span></span> <span data-ttu-id="addb0-150">Знак звездочки (\*) в конце маски заменяется случайными буквенно-цифровыми символами.</span><span class="sxs-lookup"><span data-stu-id="addb0-150">An asterisk (\*) character at the end of the mask is replaced by random alphanumeric characters.</span></span></p>
<p><span data-ttu-id="addb0-151">Определенное количество символов из% hostname% и% username% можно записать с помощью квадратных скобок.</span><span class="sxs-lookup"><span data-stu-id="addb0-151">A specific number of characters from %hostname% and %username% can be captured by using square brackets.</span></span> <span data-ttu-id="addb0-152">Например, &quot; % username% [3] &quot; будет использовать первые три символа имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="addb0-152">For example, &quot;%username%[3]&quot; would use the first three characters of the username.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-153">DeleteVMStateTimeout</span><span class="sxs-lookup"><span data-stu-id="addb0-153">DeleteVMStateTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-154">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-154">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-155">По умолчанию = 90</span><span class="sxs-lookup"><span data-stu-id="addb0-155">Default=90</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-156">Время ожидания (в секундах), по истечении которого при первой попытке установки будет удалена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="addb0-156">The time-out value, in seconds, when first time setup tries to delete the virtual machine.</span></span> <span data-ttu-id="addb0-157">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-157">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-158">DetachVfdTimeout</span><span class="sxs-lookup"><span data-stu-id="addb0-158">DetachVfdTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-160">По умолчанию = 120</span><span class="sxs-lookup"><span data-stu-id="addb0-160">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-161">Время ожидания (в секундах), по истечении которого программа установки пытается отключить виртуальный гибкий диск от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="addb0-161">The time-out value, in seconds, when first time setup tries to detach the virtual floppy disk from the virtual machine.</span></span> <span data-ttu-id="addb0-162">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-162">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-163">DialogUrl</span><span class="sxs-lookup"><span data-stu-id="addb0-163">DialogUrl</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-164">SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-164">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-165">Настраиваемый URL-адрес, который связан с внутренней веб-страницей и отображается при первом запуске диалогового окна настройки.</span><span class="sxs-lookup"><span data-stu-id="addb0-165">Customizable URL that links to internal webpage and is displayed by first time setup dialog messages.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-166">ExplorerTimeout</span><span class="sxs-lookup"><span data-stu-id="addb0-166">ExplorerTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-167">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-167">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-168">По умолчанию = 900</span><span class="sxs-lookup"><span data-stu-id="addb0-168">Default=900</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-169">Время ожидания в секундах, в течение которого программа установки ждет первого раза в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="addb0-169">The time-out value, in seconds, that first time setup waits for Windows Explorer.</span></span> <span data-ttu-id="addb0-170">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-170">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-171">FailureDialogMsg</span><span class="sxs-lookup"><span data-stu-id="addb0-171">FailureDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-172">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-172">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-173">Сообщение обнаружено в файле ресурсов</span><span class="sxs-lookup"><span data-stu-id="addb0-173">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-174">Настраиваемое сообщение, которое отображается для конечного пользователя при первой попытке завершения установки.</span><span class="sxs-lookup"><span data-stu-id="addb0-174">Customizable message that is displayed to the end user when first time setup cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-175">GiveUserGroupRightsMaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="addb0-175">GiveUserGroupRightsMaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-176">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-176">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-177">По умолчанию = 3</span><span class="sxs-lookup"><span data-stu-id="addb0-177">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-178">Максимальное количество попыток предоставления прав группе конечных пользователей с помощью MED-V.</span><span class="sxs-lookup"><span data-stu-id="addb0-178">The maximum number of times that MED-V tries to give an end user group rights.</span></span> <span data-ttu-id="addb0-179">Превышение указанного значения повтора без возможности успешного предоставления прав доступа к группе конечных пользователей, скорее всего, приводит к сбою подготовки виртуальной машины, для которого он подключается к значению MaxRetryCount.</span><span class="sxs-lookup"><span data-stu-id="addb0-179">Exceeding the specified retry value without being able to successfully give an end user group rights most likely causes a virtual machine preparation failure that is then subject to the MaxRetryCount value.</span></span> <span data-ttu-id="addb0-180">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-180">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-181">GiveUserGroupRightsTimeout</span><span class="sxs-lookup"><span data-stu-id="addb0-181">GiveUserGroupRightsTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-182">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-182">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-183">По умолчанию = 300</span><span class="sxs-lookup"><span data-stu-id="addb0-183">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-184">Время ожидания в секундах, когда вы предоставляете права группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="addb0-184">The time-out value, in seconds, when giving a user group rights.</span></span> <span data-ttu-id="addb0-185">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-185">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-186">LogFilePaths</span><span class="sxs-lookup"><span data-stu-id="addb0-186">LogFilePaths</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-187">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-187">MULTI_SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-188">Список путей к файлам журнала, собираемых MED-V при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="addb0-188">A list of the log file paths that MED-V collects during first time setup.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-189">MaxPostponeTime</span><span class="sxs-lookup"><span data-stu-id="addb0-189">MaxPostponeTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-190">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-190">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-191">По умолчанию = 120</span><span class="sxs-lookup"><span data-stu-id="addb0-191">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-192">Максимальное количество часов, которое может быть отложено конечным пользователем при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="addb0-192">The maximum number of hours that first time setup can be postponed by the end user.</span></span> <span data-ttu-id="addb0-193">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-193">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-194">MaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="addb0-194">MaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-195">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-195">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-196">По умолчанию = 3</span><span class="sxs-lookup"><span data-stu-id="addb0-196">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-197">Максимальное количество попыток подготовки виртуальной машины с помощью MED-V, если каждая попытка завершается сбоем, кроме программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="addb0-197">The maximum number of times that MED-V tries to prepare a virtual machine if each attempt ends in a failure other than a software error.</span></span> <span data-ttu-id="addb0-198">Когда подготовка виртуальной машины завершается сбоем и количество попыток настройки при первой попытке будет превышено, приложение MED-V информирует пользователя об ошибке и не дает возможность повторить попытку.</span><span class="sxs-lookup"><span data-stu-id="addb0-198">When virtual machine preparation fails and the number of first time setup retries is exceeded, then MED-V informs the end user about the failure and does not give the option to retry.</span></span> <span data-ttu-id="addb0-199">Счетчик будет повторно установлен при каждом запуске MED-V.</span><span class="sxs-lookup"><span data-stu-id="addb0-199">The count is re-set every time that MED-V is started.</span></span> <span data-ttu-id="addb0-200">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-200">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-201">Режим</span><span class="sxs-lookup"><span data-stu-id="addb0-201">Mode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-202">SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-202">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-203">По умолчанию = автоматическая установка</span><span class="sxs-lookup"><span data-stu-id="addb0-203">Default=Unattended</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-204">Настройка взаимодействия с пользователем при первом запуске программы.</span><span class="sxs-lookup"><span data-stu-id="addb0-204">Configures how first time setup interacts with the user.</span></span> <span data-ttu-id="addb0-205">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="addb0-205">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="addb0-206">Согласованием.</span><span class="sxs-lookup"><span data-stu-id="addb0-206">Attended.</span></span></strong> <span data-ttu-id="addb0-207">Конечный пользователь должен ввести данные при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="addb0-207">The end user must enter information during first time setup.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="addb0-208">Примечание.</span><span class="sxs-lookup"><span data-stu-id="addb0-208">Note</span></span></strong><br/><p><span data-ttu-id="addb0-209">Если вы создали файл Sysprep. INF, чтобы мини-процесс мог завершить ввод данных пользователем, необходимо выбрать <strong> </strong> режим автоматической установки или проблемы при первом запуске.</span><span class="sxs-lookup"><span data-stu-id="addb0-209">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, then you must select <strong>Attended</strong> mode or problems might occur during first time setup.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="addb0-210">Автоматический режим </strong> .</span><span class="sxs-lookup"><span data-stu-id="addb0-210">Unattended</strong>.</span></span> <span data-ttu-id="addb0-211">Виртуальная машина не отображается для конечных пользователей при первом запуске программы установки, но перед началом первой настройки будет выводиться запрос конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="addb0-211">The virtual machine is not shown to the end user during first time setup, but the end user is prompted before first time setup starts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="addb0-212">Автоматическая установка </strong> .</span><span class="sxs-lookup"><span data-stu-id="addb0-212">Silent</strong>.</span></span> <span data-ttu-id="addb0-213">Виртуальная машина не отображается для конечного пользователя при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="addb0-213">The virtual machine is not shown to the end user at all during first time setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-214">NonInteractiveRetryTimeoutInc</span><span class="sxs-lookup"><span data-stu-id="addb0-214">NonInteractiveRetryTimeoutInc</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-215">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-215">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-216">По умолчанию = 15</span><span class="sxs-lookup"><span data-stu-id="addb0-216">Default=15</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-217">Время ожидания (в минутах), в течение которого при первой попытке настройки необходимо завершить настройку при первом запуске интерактивного режима.</span><span class="sxs-lookup"><span data-stu-id="addb0-217">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode when re-attempting setup.</span></span> <span data-ttu-id="addb0-218">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-218">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-219">NonInteractiveTimeout</span><span class="sxs-lookup"><span data-stu-id="addb0-219">NonInteractiveTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-220">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-220">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-221">По умолчанию = 45</span><span class="sxs-lookup"><span data-stu-id="addb0-221">Default=45</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-222">Время ожидания (в минутах), в которое в первый раз при настройке интерактивного режима необходимо завершить настройку.</span><span class="sxs-lookup"><span data-stu-id="addb0-222">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode.</span></span> <span data-ttu-id="addb0-223">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-223">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-224">PostponeUtcDateTimeLimit</span><span class="sxs-lookup"><span data-stu-id="addb0-224">PostponeUtcDateTimeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-225">SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-225">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-226">Дата и время в формате UTC DateTime, которое может быть отложено при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="addb0-226">The date and time, in UTC DateTime format, that first time setup can be postponed.</span></span> <span data-ttu-id="addb0-227">Введите формат &quot; гггг-мм-дд чч: мм &quot; с часами, указанными в 24-часовом стандарте часов.</span><span class="sxs-lookup"><span data-stu-id="addb0-227">Enter in the format &quot;yyyy-MM-dd hh:mm&quot; with hours specified by using the 24-hour clock standard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-228">RetryDialogMsg</span><span class="sxs-lookup"><span data-stu-id="addb0-228">RetryDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-229">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-229">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-230">Сообщение обнаружено в файле ресурсов</span><span class="sxs-lookup"><span data-stu-id="addb0-230">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-231">Настраиваемое сообщение, которое отображается для конечного пользователя при первой попытке настройки.</span><span class="sxs-lookup"><span data-stu-id="addb0-231">Customizable message that is displayed to the end user when first time setup must re-attempt setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-232">SetComputerNameEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-232">SetComputerNameEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-233">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-233">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-234">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="addb0-234">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-235">Указывает, следует ли обновлять запись ComputerName в разделе [UserData] файла Sysprep. INF в гостевой системе в соответствии с заданными ComputerNameMask.</span><span class="sxs-lookup"><span data-stu-id="addb0-235">Configures whether the ComputerName entry under the [UserData] section of the Sysprep.inf file in the guest should be updated according to the specified ComputerNameMask.</span></span>   <span data-ttu-id="addb0-236">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-236">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-237">0 = false: запись ComputerName в файле Sysprep. inf не обновляется в соответствии с ComputerNameMask.</span><span class="sxs-lookup"><span data-stu-id="addb0-237">0 = false: The ComputerName entry in the Sysprep.inf file is not updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-238">1 = истина: запись ComputerName в файле Sysprep. INF обновлена в соответствии с ComputerNameMask.</span><span class="sxs-lookup"><span data-stu-id="addb0-238">1 = true: The ComputerName entry in the Sysprep.inf file is updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-239">SetJoinDomainEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-239">SetJoinDomainEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-240">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-240">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-241">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="addb0-241">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-242">Указывает, следует ли обновлять параметр JoinDomain в разделе [идентификация] файла Sysprep. INF в гостевой системе в соответствии с параметрами на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-242">Configures whether the JoinDomain setting under the [Identification] section of the Sysprep.inf file in the guest should be updated to match the settings on the host.</span></span>  <span data-ttu-id="addb0-243">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-243">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-244">0 = false: параметр JoinDomain в файле Sysprep. inf не обновляется в соответствии с параметрами на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-244">0 = false: The JoinDomain setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-245">1 = true: параметр JoinDomain в файле Sysprep. INF обновляется в соответствии с параметрами на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-245">1 = true: The JoinDomain setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-246">SetMachineObjectOUEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-246">SetMachineObjectOUEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-247">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-247">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-248">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="addb0-248">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-249">Определяет, будет ли параметр MachineObjectOU в разделе [идентификация] файла Sysprep. INF в гостевой системе обновлен в соответствии с узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-249">Configures whether the MachineObjectOU setting under the [Identification] section of the Sysprep.inf file in the guest is updated to match the host.</span></span>  <span data-ttu-id="addb0-250">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-250">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-251">0 = false: параметр MachineObjectOU в файле Sysprep. inf не обновляется в соответствии с параметрами на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-251">0 = false: The MachineObjectOU setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-252">1 = true: параметр MachineObjectOU в файле Sysprep. INF обновляется в соответствии с параметрами на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-252">1 = true: The MachineObjectOU setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-253">SetRegionalSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-253">SetRegionalSettingsEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-254">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-254">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-255">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="addb0-255">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-256">Настройка обновления параметров в разделе [RegionalSettings] файла Sysprep. INF в гостевой системе для соответствия узлу.</span><span class="sxs-lookup"><span data-stu-id="addb0-256">Configures whether the settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span>  <span data-ttu-id="addb0-257">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-257">0 = false; 1 = true.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="addb0-258">Примечание.</span><span class="sxs-lookup"><span data-stu-id="addb0-258">Note</span></span></strong><br/><p><span data-ttu-id="addb0-259">По умолчанию параметр TimeZone для гостя всегда синхронизируется с параметром TimeZone в узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-259">By default, the setting for TimeZone in the guest is always synchronized with the TimeZone setting in the host.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-260">0 = false: параметры в разделе [RegionalSettings] файла Sysprep. INF в гостевой системе не обновляются в соответствии с узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-260">0 = false: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are not updated to match the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-261">1 = true: параметры в разделе [RegionalSettings] файла Sysprep. INF в гостевой системе обновлены в соответствии с узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-261">1 = true: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-262">SetUserDataEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-262">SetUserDataEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-263">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-263">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-264">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="addb0-264">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-265">Настройка обновления параметров FullName и OrgName в разделе [UserData] файла Sysprep. INF в гостевой системе в соответствии с параметрами на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-265">Configures whether the FullName and the OrgName settings under the [UserData] section of the Sysprep.inf file in the guest are updated to match the settings on the host.</span></span>  <span data-ttu-id="addb0-266">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-266">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-267">0 = false: параметры FullName и OrgName в файле Sysprep. inf не обновляются в соответствии с параметрами на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-267">0 = false: The FullName and OrgName settings in the Sysprep.inf file are not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-268">1 = true: параметры FullName и OrgName в файле Sysprep. INF обновляются в соответствии с параметрами на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-268">1 = true: The FullName and OrgName settings in the Sysprep.inf file are updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-269">StartDialogMsg</span><span class="sxs-lookup"><span data-stu-id="addb0-269">StartDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-270">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-270">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-271">Сообщение обнаружено в файле ресурсов</span><span class="sxs-lookup"><span data-stu-id="addb0-271">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-272">Настраиваемое сообщение, которое отображается для конечного пользователя при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="addb0-272">Customizable message that is displayed to the end user when first time setup is ready to start.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-273">TaskCancelTimeout</span><span class="sxs-lookup"><span data-stu-id="addb0-273">TaskCancelTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-274">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-275">По умолчанию = 30</span><span class="sxs-lookup"><span data-stu-id="addb0-275">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-276">Время ожидания в секундах, в течение которого первый раз программа установки ждет ответа от виртуальной машины на операцию отмены.</span><span class="sxs-lookup"><span data-stu-id="addb0-276">The time-out value, in seconds, that first time setup waits for a response from the virtual machine for a Cancel operation.</span></span> <span data-ttu-id="addb0-277">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-277">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-278">TaskVMTurnOffTimeout</span><span class="sxs-lookup"><span data-stu-id="addb0-278">TaskVMTurnOffTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-279">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-279">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-280">По умолчанию = 60</span><span class="sxs-lookup"><span data-stu-id="addb0-280">Default=60</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-281">Время ожидания в секундах, в течение которого первый раз программа установки ждет завершения работы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="addb0-281">The time-out value, in seconds, that first time setup waits for the virtual machine to shut down.</span></span> <span data-ttu-id="addb0-282">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-282">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-283">UpgradeTimeout</span><span class="sxs-lookup"><span data-stu-id="addb0-283">UpgradeTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-284">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-284">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-285">По умолчанию = 600</span><span class="sxs-lookup"><span data-stu-id="addb0-285">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-286">Время, в течение которого вы попытались попытаться обновить программное обеспечение гостевого агента MED-V по истечении времени ожидания. Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-286">The time, in seconds, before an attempted upgrade of the MED-V Guest Agent software times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="addb0-287">Клавиша UserExperience</span><span class="sxs-lookup"><span data-stu-id="addb0-287">UserExperience Key</span></span>


<span data-ttu-id="addb0-288">В таблице ниже приведены сведения о значениях реестра, связанных с клавишами HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience и клавиша HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\UserExperience.</span><span class="sxs-lookup"><span data-stu-id="addb0-288">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\UserExperience key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="addb0-289">Имя</span><span class="sxs-lookup"><span data-stu-id="addb0-289">Name</span></span></th>
<th align="left"><span data-ttu-id="addb0-290">Тип</span><span class="sxs-lookup"><span data-stu-id="addb0-290">Type</span></span></th>
<th align="left"><span data-ttu-id="addb0-291">Данные и по умолчанию</span><span class="sxs-lookup"><span data-stu-id="addb0-291">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="addb0-292">Описание</span><span class="sxs-lookup"><span data-stu-id="addb0-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-293">AppPublishingEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-293">AppPublishingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-294">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-294">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-295">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="addb0-295">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-296">Указывает, включена ли публикация приложения на гостевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="addb0-296">Configures whether application publication from the guest to the host is enabled.</span></span>  <span data-ttu-id="addb0-297">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-297">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-298">0 = false: Отключение публикации приложения от гостя на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-298">0 = false: Disables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-299">1 = true: включает публикацию приложения от гостя на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-299">1 = true: Enables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-300">AudioSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-300">AudioSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-301">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-301">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-302">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="addb0-302">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-303">Настраивает способ совместного использования звукового устройства ввода-вывода между гостевой системой и узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-303">Configures whether the sharing of the audio I/O device between the guest and the host is enabled.</span></span>  <span data-ttu-id="addb0-304">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-304">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-305">0 = false: отключает общий доступ к звуковому устройству ввода-вывода между гостевой системой и узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-305">0 = false: Disables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-306">1 = true: позволяет предоставлять общий доступ к звуковому устройству ввода-вывода между гостевым и ведущим узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-306">1 = true: Enables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-307">ClipboardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-307">ClipboardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-308">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-308">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-309">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="addb0-309">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-310">Определяет, будет ли общий доступ к буферу обмена между гостевой и ведущим приложением включен.</span><span class="sxs-lookup"><span data-stu-id="addb0-310">Configures whether the sharing of the Clipboard between the guest and the host is enabled.</span></span>  <span data-ttu-id="addb0-311">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-311">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-312">0 = false: отключает общий доступ к буферу обмена между гостевым и ведущим узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-312">0 = false: Disables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-313">1 = true: позволяет предоставлять общий доступ к буферу обмена между гостевой и ведущим узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-313">1 = true: Enables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-314">DialogTimeout</span><span class="sxs-lookup"><span data-stu-id="addb0-314">DialogTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-315">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-315">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-316">По умолчанию = 300</span><span class="sxs-lookup"><span data-stu-id="addb0-316">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-317">Время, в секундах, до истечения времени первого запуска диалогового окна настройки. Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-317">The time, in seconds, before the first time setup Start Dialog times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-318">HideVmTimeout</span><span class="sxs-lookup"><span data-stu-id="addb0-318">HideVmTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-319">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-319">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-320">По умолчанию = 30</span><span class="sxs-lookup"><span data-stu-id="addb0-320">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-321">Время ожидания (в минутах), в течение которого полноэкранное окно виртуальной машины будет скрыто от конечного пользователя во время длительной попытки входа.</span><span class="sxs-lookup"><span data-stu-id="addb0-321">The time-out value, in minutes, that the full-screen virtual machine window is hidden from the end user during a long logon attempt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-322">LogonStartEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-322">LogonStartEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-323">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-323">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-324">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="addb0-324">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-325">Указывает, следует ли запускать гость, когда пользователь входит в систему на рабочем столе или при запуске первого гостевого приложения.</span><span class="sxs-lookup"><span data-stu-id="addb0-325">Configures whether the guest should be started when the end user logs on to the desktop or when the first guest application is started.</span></span>  <span data-ttu-id="addb0-326">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-326">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-327">0 = false: гость запускается при запуске первой гостевой программы.</span><span class="sxs-lookup"><span data-stu-id="addb0-327">0 = false: The guest is started when the first guest application is started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-328">1 = true: гость запускается, когда пользователь входит в систему на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="addb0-328">1 = true: The guest is started when the end user logs on to the desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-329">PrinterSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-329">PrinterSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-330">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-330">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-331">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="addb0-331">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-332">Определяет, включен ли общий доступ к принтерам между гостевой и ведущим узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-332">Configures whether the sharing of printers between the guest and the host is enabled.</span></span>  <span data-ttu-id="addb0-333">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-333">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-334">0 = false: отключает общий доступ к принтерам между гостевой и ведущим узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-334">0 = false: Disables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-335">1 = true: позволяет предоставлять общий доступ к принтерам между гостевой и ведущим узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-335">1 = true: Enables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-336">RebootAbsoluteDelayTimeout</span><span class="sxs-lookup"><span data-stu-id="addb0-336">RebootAbsoluteDelayTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-337">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-337">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-338">По умолчанию = 1440</span><span class="sxs-lookup"><span data-stu-id="addb0-338">Default=1440</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-339">Время ожидания (в минутах), в течение которого при первом запуске программы установки Ожидается перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="addb0-339">The time-out value, in minutes, that first time setup waits for a restart.</span></span> <span data-ttu-id="addb0-340">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-340">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-341">RedirectUrls</span><span class="sxs-lookup"><span data-stu-id="addb0-341">RedirectUrls</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-342">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-342">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-343">Указанный список URL-адресов</span><span class="sxs-lookup"><span data-stu-id="addb0-343">Specified URL list</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-344">Указывает список URL-адресов, которые нужно перенаправить с узла на гостя.</span><span class="sxs-lookup"><span data-stu-id="addb0-344">Specifies a list of URLs to be redirected from the host to the guest.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-345">SmartCardLogonEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-345">SmartCardLogonEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-346">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-346">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-347">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="addb0-347">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-348">Определяет, можно ли использовать смарт-карты для проверки подлинности пользователей в MED – V.</span><span class="sxs-lookup"><span data-stu-id="addb0-348">Configures whether smart cards can be used to authenticate users to MED-V.</span></span> <span data-ttu-id="addb0-349">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-349">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-350">0 = false: не разрешать проверка подлинности конечных пользователей в MED-V на интеллектуальных картах.</span><span class="sxs-lookup"><span data-stu-id="addb0-350">0 = false: Does not let Smart Cards authenticate end users to MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-351">1 = true: позволяет смарт-картам проверять подлинность конечных пользователей для использования в качестве серверной MED.</span><span class="sxs-lookup"><span data-stu-id="addb0-351">1 = true: Lets Smart Cards authenticate end users to MED-V.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="addb0-352">Важно.</span><span class="sxs-lookup"><span data-stu-id="addb0-352">Important</span></span></strong><br/><p><span data-ttu-id="addb0-353">Если включены параметры SmartCardLogonEnabled и CredentialCacheEnabled, SmartCardLogonEnabled переопределяет CredentialCacheEnabled.</span><span class="sxs-lookup"><span data-stu-id="addb0-353">If SmartCardLogonEnabled and CredentialCacheEnabled are both enabled, SmartCardLogonEnabled overrides CredentialCacheEnabled.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-354">SmartCardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-354">SmartCardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-356">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="addb0-356">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-357">Определяет, включен ли общий доступ к смарт-картам между гостевой и ведущим узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-357">Configures whether the sharing of Smart Cards between the guest and the host is enabled.</span></span>  <span data-ttu-id="addb0-358">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-358">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-359">0 = false: отключает общий доступ к смарт-картам между гостевым и ведущим узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-359">0 = false: Disables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-360">1 = true: позволяет предоставлять общий доступ к смарт-картам между гостевой и ведущим узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-360">1 = true: Enables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-361">USBDeviceSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-361">USBDeviceSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-363">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="addb0-363">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-364">Определяет, будет ли общий доступ к USB-устройствам между гостевой и ведущим узлом включен.</span><span class="sxs-lookup"><span data-stu-id="addb0-364">Configures whether the sharing of USB devices between the guest and the host is enabled.</span></span>  <span data-ttu-id="addb0-365">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-365">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-366">0 = false: отключает общий доступ устройств USB между гостевым и ведущим узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-366">0 = false: Disables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-367">1 = true: позволяет предоставлять общий доступ к USB-устройствам между гостевой системой и узлом.</span><span class="sxs-lookup"><span data-stu-id="addb0-367">1 = true: Enables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="addb0-368">Ключ виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="addb0-368">VM Key</span></span>


<span data-ttu-id="addb0-369">В таблице ниже приведены сведения о значениях реестра, связанных с клавишами HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\VM и клавиша HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\VM.</span><span class="sxs-lookup"><span data-stu-id="addb0-369">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\VM key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\VM key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="addb0-370">Имя</span><span class="sxs-lookup"><span data-stu-id="addb0-370">Name</span></span></th>
<th align="left"><span data-ttu-id="addb0-371">Тип</span><span class="sxs-lookup"><span data-stu-id="addb0-371">Type</span></span></th>
<th align="left"><span data-ttu-id="addb0-372">Данные и по умолчанию</span><span class="sxs-lookup"><span data-stu-id="addb0-372">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="addb0-373">Описание</span><span class="sxs-lookup"><span data-stu-id="addb0-373">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-374">CloseAction</span><span class="sxs-lookup"><span data-stu-id="addb0-374">CloseAction</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-375">SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-375">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-376">По умолчанию = СПЯЩий режим</span><span class="sxs-lookup"><span data-stu-id="addb0-376">Default=HIBERNATE</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-377">Действие, выполняемое виртуальной машиной после закрытия последнего работающего приложения.</span><span class="sxs-lookup"><span data-stu-id="addb0-377">The action that the virtual machine performs after the last application that is running is closed.</span></span> <span data-ttu-id="addb0-378">Этот параметр игнорируется, если включен параметр LogonStartEnabled.</span><span class="sxs-lookup"><span data-stu-id="addb0-378">This setting is ignored if the LogonStartEnabled value is enabled.</span></span> <span data-ttu-id="addb0-379">Возможны следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="addb0-379">Possible options are as follows:</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="addb0-380">РЕЖИМ ГИБЕРНАЦИи </strong> .</span><span class="sxs-lookup"><span data-stu-id="addb0-380">HIBERNATE</strong> .</span></span> <span data-ttu-id="addb0-381">Этот параметр освобождает все физические ресурсы, которые использует виртуальная машина, например память и ЦП, и сохраняет состояние всех запущенных приложений и операций.</span><span class="sxs-lookup"><span data-stu-id="addb0-381">This option releases all physical resources that the virtual machine is using, such as memory and CPU, and saves the state of all running applications and operations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="addb0-382">Завершение работы </strong> .</span><span class="sxs-lookup"><span data-stu-id="addb0-382">SHUTDOWN</strong> .</span></span> <span data-ttu-id="addb0-383">Этот параметр безопасно завершает работу гостевой операционной системы, а затем освобождает все физические ресурсы, которые использует виртуальная машина, например память и ЦП.</span><span class="sxs-lookup"><span data-stu-id="addb0-383">This option shuts down the guest operating system safely and then releases all physical resources that the virtual machine is using, such as memory and CPU.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="addb0-384">отключение </strong> .</span><span class="sxs-lookup"><span data-stu-id="addb0-384">TURN-OFF</strong>.</span></span> <span data-ttu-id="addb0-385">Этот параметр может привести к потере данных, так как он аналогичен выключению кнопки питания или выдаче шнура питания на физическом компьютере.</span><span class="sxs-lookup"><span data-stu-id="addb0-385">This option can cause data loss because it is the same as turning off the power button or pulling out the power cord on a physical computer.</span></span> <span data-ttu-id="addb0-386">Используйте этот параметр только в том случае, если вы не можете использовать один из двух других параметров.</span><span class="sxs-lookup"><span data-stu-id="addb0-386">Use this option only if you cannot use one of the other two options.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-387">GuestMemFromHostMem</span><span class="sxs-lookup"><span data-stu-id="addb0-387">GuestMemFromHostMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-388">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-388">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-389">378, 512, 1024, 1536, 2048</span><span class="sxs-lookup"><span data-stu-id="addb0-389">378, 512, 1024, 1536, 2048</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-390">Список значений памяти (МБ) для гостя.</span><span class="sxs-lookup"><span data-stu-id="addb0-390">A list of memory (MB) values for the guest.</span></span> <span data-ttu-id="addb0-391">Это значение используется для определения объема памяти, доступного для гостя.</span><span class="sxs-lookup"><span data-stu-id="addb0-391">This value is used to determine how much RAM is available to the guest.</span></span> <span data-ttu-id="addb0-392">В сочетании с HostMemToGuestMem создается таблица подстановки, с помощью которой можно определить, сколько памяти нужно выделить на гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="addb0-392">Combined with HostMemToGuestMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="addb0-393">Возможные значения могут быть от 128 до 3712.</span><span class="sxs-lookup"><span data-stu-id="addb0-393">Possible values can be from 128 to 3712.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-394">GuestUpdateDuration</span><span class="sxs-lookup"><span data-stu-id="addb0-394">GuestUpdateDuration</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-396">По умолчанию = 240</span><span class="sxs-lookup"><span data-stu-id="addb0-396">Default=240</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-397">Количество минут, в течение которых MED-V должен поддерживать функцию "Неспящий режим" на гостевом компьютере для автоматического обновления, начиная с момента, указанного в значении GuestUpdateTime.</span><span class="sxs-lookup"><span data-stu-id="addb0-397">The number of minutes that MED-V should keep the guest awake for automatic updating, starting at the time specified in the GuestUpdateTime value.</span></span> <span data-ttu-id="addb0-398">Диапазон от 0 до 1440.</span><span class="sxs-lookup"><span data-stu-id="addb0-398">Range = 0 to 1440.</span></span> <span data-ttu-id="addb0-399">Установка этого значения равным нулю (0) отключает функцию исправлений гостя.</span><span class="sxs-lookup"><span data-stu-id="addb0-399">Setting this value to zero (0) disables the guest patching functionality.</span></span></p>
<p><span data-ttu-id="addb0-400">Дополнительные сведения об автоматическом обновлении можно найти в разделе <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Управление автоматическим обновлением для рабочих областей MED-V </a> .</span><span class="sxs-lookup"><span data-stu-id="addb0-400">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-401">GuestUpdateTime</span><span class="sxs-lookup"><span data-stu-id="addb0-401">GuestUpdateTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-402">SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-402">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-403">По умолчанию = 00:00</span><span class="sxs-lookup"><span data-stu-id="addb0-403">Default=00:00</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-404">Час и минута для каждого дня, когда MED-V должен пробудить гостевую систему для автоматического обновления, используя 24-часовой стандарт часов.</span><span class="sxs-lookup"><span data-stu-id="addb0-404">The hour and minute each day when MED-V should wake up the guest for automatic updating, by using the 24-hour clock standard.</span></span> <span data-ttu-id="addb0-405">Укажите время в формате чч: мм</span><span class="sxs-lookup"><span data-stu-id="addb0-405">Specify the time in the format HH:MM</span></span>  </p>
<p><span data-ttu-id="addb0-406">Дополнительные сведения об автоматическом обновлении можно найти в разделе <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Управление автоматическим обновлением для рабочих областей MED-V </a> .</span><span class="sxs-lookup"><span data-stu-id="addb0-406">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-407">HostMemToGuestMem</span><span class="sxs-lookup"><span data-stu-id="addb0-407">HostMemToGuestMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-408">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-408">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-409">1024, 2048, 4096, 8192, 16384</span><span class="sxs-lookup"><span data-stu-id="addb0-409">1024, 2048, 4096, 8192, 16384</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-410">Список значений памяти (МБ) для гостя, определяемый объемом ОЗУ, доступном на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-410">A list of memory (MB) values for the guest, determined by the RAM available on the host.</span></span> <span data-ttu-id="addb0-411">В сочетании с GuestMemFromHostMem создается таблица подстановки, с помощью которой можно определить, сколько памяти нужно выделить на гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="addb0-411">Combined with GuestMemFromHostMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="addb0-412">Возможные значения могут быть от 1024 до 16384.</span><span class="sxs-lookup"><span data-stu-id="addb0-412">Possible values can be from 1024 to 16384.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-413">HostMemToGuestMemCalcEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-413">HostMemToGuestMemCalcEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-414">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-414">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-415">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="addb0-415">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-416">Определяет, будет ли память, выделенная для гостя, рассчитывается на основе памяти, представленной на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-416">Configures whether the memory allocated for the guest is calculated from the memory present on the host.</span></span>  <span data-ttu-id="addb0-417">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-417">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-418">0 = false: память, выделенная для гостя, не рассчитывается на основе памяти, представленной на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-418">0 = false: The memory allocated for the guest is not calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-419">1 = true: память, выделенная для гостя, рассчитывается на основе памяти, представленной на узле.</span><span class="sxs-lookup"><span data-stu-id="addb0-419">1 = true: The memory allocated for the guest is calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-420">Память</span><span class="sxs-lookup"><span data-stu-id="addb0-420">Memory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-421">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-421">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-422">По умолчанию — 512</span><span class="sxs-lookup"><span data-stu-id="addb0-422">Default=512</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-423">ОЗУ (МБ), которое должно быть выделено для гостевой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="addb0-423">The RAM (MB) that should be allocated for the guest virtual machine.</span></span> <span data-ttu-id="addb0-424">Этот параметр игнорируется, если включен параметр HostMemToGuestMemEnabled.</span><span class="sxs-lookup"><span data-stu-id="addb0-424">This setting is ignored if the HostMemToGuestMemEnabled setting is enabled.</span></span> <span data-ttu-id="addb0-425">Диапазон от 128 до 2048.</span><span class="sxs-lookup"><span data-stu-id="addb0-425">Range=128 to 2048.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-426">MultiUserEnabled</span><span class="sxs-lookup"><span data-stu-id="addb0-426">MultiUserEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-427">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-427">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-428">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="addb0-428">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-429">Настройка общего доступа нескольких пользователей к одной и той же рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="addb0-429">Configures whether multiple users share the same MED-V workspace.</span></span>  <span data-ttu-id="addb0-430">0 = ложь; 1 = истина.</span><span class="sxs-lookup"><span data-stu-id="addb0-430">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-431">0 = false: несколько пользователей не могут совместно использовать одну и ту же рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="addb0-431">0 = false: Multiple users do not share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-432">1 = true: несколько пользователей совместно имеют одну и ту же рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="addb0-432">1 = true: Multiple users share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="addb0-433">NetworkingMode</span><span class="sxs-lookup"><span data-stu-id="addb0-433">NetworkingMode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-434">SZ</span><span class="sxs-lookup"><span data-stu-id="addb0-434">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-435">По умолчанию = NAT</span><span class="sxs-lookup"><span data-stu-id="addb0-435">Default=NAT</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-436">Сетевое подключение, используемое в качестве гостя.</span><span class="sxs-lookup"><span data-stu-id="addb0-436">The kind of network connection used on the guest.</span></span> <span data-ttu-id="addb0-437">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="addb0-437">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="addb0-438">Моста </strong> .</span><span class="sxs-lookup"><span data-stu-id="addb0-438">Bridged</strong>.</span></span> <span data-ttu-id="addb0-439">Для MED-V имеется собственный сетевой адрес, обычно получаемый с помощью DHCP.</span><span class="sxs-lookup"><span data-stu-id="addb0-439">MED-V has its own network address, typically obtained through DHCP.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="addb0-440">NAT </strong> .</span><span class="sxs-lookup"><span data-stu-id="addb0-440">NAT</strong>.</span></span> <span data-ttu-id="addb0-441">В MED-V используется преобразование сетевых адресов (NAT) для предоставления общего доступа к узлу&#39;s IP для исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="addb0-441">MED-V uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-442">TaskTimeout</span><span class="sxs-lookup"><span data-stu-id="addb0-442">TaskTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-443">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-443">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-444">По умолчанию = 600</span><span class="sxs-lookup"><span data-stu-id="addb0-444">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-445">Общее время ожидания в секундах, в течение которого MED-V ждет завершения задачи, например для перезапуска и завершения работы.</span><span class="sxs-lookup"><span data-stu-id="addb0-445">A general time-out value, in seconds, that MED-V waits for a task to be completed, such as restarting and shutting down.</span></span> <span data-ttu-id="addb0-446">Диапазон от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="addb0-446">Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="addb0-447">Параметры реестра гостя</span><span class="sxs-lookup"><span data-stu-id="addb0-447">Guest Registry Settings</span></span>


<span data-ttu-id="addb0-448">В этом разделе перечислены настраиваемые гостевые разделы реестра MED-V и описаны их использование.</span><span class="sxs-lookup"><span data-stu-id="addb0-448">This section lists the configurable MED-V guest registry keys and explains their uses.</span></span>

### <span data-ttu-id="addb0-449">версии</span><span class="sxs-lookup"><span data-stu-id="addb0-449">v2</span></span>

<span data-ttu-id="addb0-450">В таблице ниже приведены сведения о значении реестра гостя, связанном с клавишей HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\.</span><span class="sxs-lookup"><span data-stu-id="addb0-450">The following table provides information about the guest registry value associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\ key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="addb0-451">Имя</span><span class="sxs-lookup"><span data-stu-id="addb0-451">Name</span></span> </th>
<th align="left"><span data-ttu-id="addb0-452">Тип</span><span class="sxs-lookup"><span data-stu-id="addb0-452">Type</span></span> </th>
<th align="left"><span data-ttu-id="addb0-453">Данные и по умолчанию</span><span class="sxs-lookup"><span data-stu-id="addb0-453">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="addb0-454">Описание</span><span class="sxs-lookup"><span data-stu-id="addb0-454">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="addb0-455">EnableGPWorkarounds</span><span class="sxs-lookup"><span data-stu-id="addb0-455">EnableGPWorkarounds</span></span></p></td>
<td align="left"><p><span data-ttu-id="addb0-456">DWORD</span><span class="sxs-lookup"><span data-stu-id="addb0-456">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-457">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="addb0-457">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="addb0-458">Настраивает способ обработки ключей BufferPolicyReads и GroupPolicyMinTransferRate с помощью MED-V.</span><span class="sxs-lookup"><span data-stu-id="addb0-458">Configures how MED-V handles the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="addb0-459">По умолчанию MED-V задает указанные ниже сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="addb0-459">By default, MED-V sets these keys as follows:</span></span></p>
<p><span data-ttu-id="addb0-460">BufferPolicyReads = 1 и GroupPolicyMinTransferRate = 0.</span><span class="sxs-lookup"><span data-stu-id="addb0-460">BufferPolicyReads=1 and GroupPolicyMinTransferRate=0.</span></span></p>
<p><span data-ttu-id="addb0-461">Создавайте ключ EnableGPWorkarounds, если это необходимо, и установите для ключа нулевое значение, если не хотите, чтобы MED-V изменил параметры по умолчанию для BufferPolicyReads и GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="addb0-461">Create the EnableGPWorkarounds  key, if it is necessary, and set the key to zero if you do not want MED-V to change the default settings of BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="addb0-462">Примечание.</span><span class="sxs-lookup"><span data-stu-id="addb0-462">Note</span></span></strong><br/><p><span data-ttu-id="addb0-463">Если Рабочая область MED-V работает в режиме NAT, EnableGPWorkarounds влияет на разделы реестра BufferPolicyReads и GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="addb0-463">If your MED-V workspace is running in NAT mode, EnableGPWorkarounds affects the registry keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span> <span data-ttu-id="addb0-464">Если Рабочая область MED-V работает в режиме моста, EnableGPWorkarounds влияет только на раздел реестра BufferPolicyReads.</span><span class="sxs-lookup"><span data-stu-id="addb0-464">If your MED-V workspace is running in BRIDGED mode, EnableGPWorkarounds only affects the registry key BufferPolicyReads.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="addb0-465">1 = true: MED-V задает клавиши BufferPolicyReads = 1 и GroupPolicyMinTransferRate = 0 (при работе в режиме NAT) или просто BufferPolicyReads = 1 (если работает в режиме моста).</span><span class="sxs-lookup"><span data-stu-id="addb0-465">1=true: MED-V sets the keys BufferPolicyReads=1 and GroupPolicyMinTransferRate=0 (if running in NAT mode) or just BufferPolicyReads=1 (if running in BRIDGED mode).</span></span></p>
<p><span data-ttu-id="addb0-466">0 = false: MED-V не вносит изменения в ключи BufferPolicyReads и GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="addb0-466">0=false: MED-V does not make any changes to the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="addb0-467">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="addb0-467">Related topics</span></span>


[<span data-ttu-id="addb0-468">Управление приложениями рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="addb0-468">Manage MED-V Workspace Applications</span></span>](manage-med-v-workspace-applications.md)

[<span data-ttu-id="addb0-469">Управление перенаправлением URL-адресов MED-V</span><span class="sxs-lookup"><span data-stu-id="addb0-469">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)

[<span data-ttu-id="addb0-470">Управление параметрами рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="addb0-470">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)









