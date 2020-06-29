---
title: Настройка UE-V с помощью объектов групповой политики
description: Настройка UE-V с помощью объектов групповой политики
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826699"
---
# <span data-ttu-id="04d24-103">Настройка UE-V с помощью объектов групповой политики</span><span class="sxs-lookup"><span data-stu-id="04d24-103">Configuring UE-V with Group Policy Objects</span></span>


<span data-ttu-id="04d24-104">Некоторые параметры групповой политики Microsoft User Experience Virtualization (UE-V) можно определять для компьютеров и других пользователей.</span><span class="sxs-lookup"><span data-stu-id="04d24-104">Some Microsoft User Experience Virtualization (UE-V) Group Policy settings can be defined for computers and others can be defined for users.</span></span> <span data-ttu-id="04d24-105">Параметры политики конфигурации агента UE-V можно определять для компьютеров и пользователей.</span><span class="sxs-lookup"><span data-stu-id="04d24-105">UE-V agent configuration policy settings can be defined for computers or users.</span></span> <span data-ttu-id="04d24-106">Дополнительные сведения о том, как установить ADMX-файлы групповой политики, можно найти [в разделе Установка шаблонов ADMX групповой политики UE-v](installing-the-ue-v-group-policy-admx-templates.md).</span><span class="sxs-lookup"><span data-stu-id="04d24-106">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V Group Policy ADMX Templates](installing-the-ue-v-group-policy-admx-templates.md).</span></span>

<span data-ttu-id="04d24-107">Для UE-V можно настроить следующие параметры политики:</span><span class="sxs-lookup"><span data-stu-id="04d24-107">The following policy settings can be configured for UE-V:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="04d24-108">Имя параметра политики</span><span class="sxs-lookup"><span data-stu-id="04d24-108">Policy setting name</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="04d24-109">Target</span><span class="sxs-lookup"><span data-stu-id="04d24-109">Target</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="04d24-110">Описание параметра политики</span><span class="sxs-lookup"><span data-stu-id="04d24-110">Policy setting description</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="04d24-111">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="04d24-111">Configuration options</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04d24-112">Использование виртуализации взаимодействия с пользователем (UE-V)</span><span class="sxs-lookup"><span data-stu-id="04d24-112">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-113">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="04d24-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-114">Этот параметр политики позволяет включить или отключить виртуализацию взаимодействия с пользователем (UE-V).</span><span class="sxs-lookup"><span data-stu-id="04d24-114">This policy setting allows you to enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-115">Включите или отключите этот параметр политики.</span><span class="sxs-lookup"><span data-stu-id="04d24-115">Enable or disable this policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04d24-116">Путь к хранилищу параметров</span><span class="sxs-lookup"><span data-stu-id="04d24-116">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-117">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="04d24-117">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-118">Этот параметр политики определяет, где будут храниться параметры пользователя.</span><span class="sxs-lookup"><span data-stu-id="04d24-118">This policy setting configures where the user settings will be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-119">Укажите путь UNC и переменные (например, \Server\SettingsShare%username%.).</span><span class="sxs-lookup"><span data-stu-id="04d24-119">Provide a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04d24-120">Путь к каталогу шаблонов параметров</span><span class="sxs-lookup"><span data-stu-id="04d24-120">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-121">Только компьютеры</span><span class="sxs-lookup"><span data-stu-id="04d24-121">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-122">Этот параметр политики определяет, где хранятся пользовательские шаблоны расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="04d24-122">This policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="04d24-123">Этот параметр политики также указывает, будет ли каталог использоваться для замены используемых по умолчанию шаблонов Microsoft, установленных с помощью UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="04d24-123">This policy setting also configures whether the catalog will be used to replace the default Microsoft templates that are installed with the UE-V agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-124">Укажите путь UNC (Universal Naming Convention), например \Server\TemplateShare или расположение папки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="04d24-124">Provide a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p></p>
<p><span data-ttu-id="04d24-125">Установите флажок, чтобы заменить используемые по умолчанию шаблоны Microsoft.</span><span class="sxs-lookup"><span data-stu-id="04d24-125">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04d24-126">Не используйте автономные файлы</span><span class="sxs-lookup"><span data-stu-id="04d24-126">Do not use Offline Files</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-127">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="04d24-127">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-128">Этот параметр политики позволяет указать, будет ли UE-V использовать функцию автономных файлов Windows.</span><span class="sxs-lookup"><span data-stu-id="04d24-128">This policy setting allows you to configure whether UE-V will use the Windows Offline Files feature.</span></span> <span data-ttu-id="04d24-129">Этот параметр политики также позволяет включить уведомления о задержке импорта параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="04d24-129">This policy setting also allows you to enable notification to occur when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-130">Чтобы настроить агент UE-V без использования автономных файлов, включите этот параметр.</span><span class="sxs-lookup"><span data-stu-id="04d24-130">To configure the UE-V Agent to not use offline files, enable this setting.</span></span></p>
<p></p>
<p><span data-ttu-id="04d24-131">Укажите, следует ли предоставлять уведомления о задержке импорта параметров.</span><span class="sxs-lookup"><span data-stu-id="04d24-131">Specify if notifications should be given when settings import is delayed.</span></span></p>
<p></p>
<p><span data-ttu-id="04d24-132">Укажите интервал времени (в секундах), по истечении которого будет выводиться уведомление.</span><span class="sxs-lookup"><span data-stu-id="04d24-132">Specify the length of time in seconds to wait before the notification appears.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04d24-133">Время ожидания синхронизации</span><span class="sxs-lookup"><span data-stu-id="04d24-133">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-134">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="04d24-134">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-135">Этот параметр политики задает количество миллисекунд, в течение которых компьютер будет ждаться, прежде чем превышено время ожидания при получении параметров пользователя из расположения удаленных параметров.</span><span class="sxs-lookup"><span data-stu-id="04d24-135">This policy setting configures the number of milliseconds that the computer waits before a timeout when retrieving user settings from the remote settings location.</span></span> <span data-ttu-id="04d24-136">Если место в внешнем хранилище недоступно, запуск приложения задерживается этим количеством миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="04d24-136">If the remote storage location is unavailable, the application launch is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-137">Укажите предпочтительное время ожидания синхронизации в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="04d24-137">Specify the preferred synchronization timeout in milliseconds.</span></span> <span data-ttu-id="04d24-138">Значение по умолчанию 2000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="04d24-138">The default value of 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04d24-139">Порог предупреждений о размере пакета</span><span class="sxs-lookup"><span data-stu-id="04d24-139">Package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-140">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="04d24-140">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-141">Этот параметр политики позволяет настроить агент UE-V для отчета о том, что размер файла пакета параметров достигнет определенного порогового значения.</span><span class="sxs-lookup"><span data-stu-id="04d24-141">This policy setting allows you to configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-142">Указывает предпочтительный порог для размера пакета параметров в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="04d24-142">Specified the preferred threshold for settings package sizes in kilobytes.</span></span></p>
<p><span data-ttu-id="04d24-143">По умолчанию агент UE-V не имеет порогового значения размера файла пакета.</span><span class="sxs-lookup"><span data-stu-id="04d24-143">By default, the UE-V agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04d24-144">Параметры перемещаемых приложений</span><span class="sxs-lookup"><span data-stu-id="04d24-144">Roaming Application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-145">Только для пользователей</span><span class="sxs-lookup"><span data-stu-id="04d24-145">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-146">Этот параметр политики позволяет настроить перемещение параметров пользователя для приложений.</span><span class="sxs-lookup"><span data-stu-id="04d24-146">This policy setting configures the roaming of user settings of applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-147">Выберите параметры Windows, которые будут перемещаться между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="04d24-147">Select which Windows settings will roam between computers.</span></span></p>
<p><span data-ttu-id="04d24-148">По умолчанию параметры пользователя для приложений с шаблоном параметров, предоставленными UE-V, перемещаются между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="04d24-148">By default, the user settings of applications with settings template provided by UE-V are roamed between computers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04d24-149">Перемещаемые параметры Windows</span><span class="sxs-lookup"><span data-stu-id="04d24-149">Roaming Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-150">Только для пользователей</span><span class="sxs-lookup"><span data-stu-id="04d24-150">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-151">Этот параметр политики настраивает перемещаемые параметры Windows.</span><span class="sxs-lookup"><span data-stu-id="04d24-151">This policy setting configures the roaming of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04d24-152">Выберите, какие приложения будут перемещаться между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="04d24-152">Select which applications will roam between computers.</span></span></p>
<p><span data-ttu-id="04d24-153">По умолчанию темы Windows перемещаются между компьютерами одной и той же версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="04d24-153">By default, Windows themes are roamed between computers of the same operating system version.</span></span> <span data-ttu-id="04d24-154">Параметры рабочего стола Windows и параметры специальных возможностей не перемещаются.</span><span class="sxs-lookup"><span data-stu-id="04d24-154">Windows desktop settings and Ease of Access settings are not roamed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="04d24-155">Настройка политик, предназначенных для компьютера</span><span class="sxs-lookup"><span data-stu-id="04d24-155">To configure computer-targeted policies</span></span>**

1.  <span data-ttu-id="04d24-156">С помощью консоли управления групповыми политиками (GPMC) или расширенного управления групповыми политиками (групповой политики) на компьютере контроллера домена, управляющего групповой политикой для компьютеров с UE-V.</span><span class="sxs-lookup"><span data-stu-id="04d24-156">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the domain controller computer that manages Group Policy for UE-V computers.</span></span> <span data-ttu-id="04d24-157">Перейдите к разделу **Конфигурация компьютера**, выберите **политики**, выберите **Административные шаблоны**, щелкните **компоненты Windows**, а затем выберите **Microsoft User Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="04d24-157">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="04d24-158">Выберите параметр политики, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="04d24-158">Select the policy setting to be edited.</span></span>

**<span data-ttu-id="04d24-159">Настройка политик, предназначенных для пользователей</span><span class="sxs-lookup"><span data-stu-id="04d24-159">To configure user-targeted policies</span></span>**

1.  <span data-ttu-id="04d24-160">Используйте консоль управления групповыми политиками (GPMC) или Расширенное средство управления групповыми политиками в пакете оптимизации рабочего стола (MDOP) на компьютере контроллера домена, управляющем групповой политикой для UE-V.</span><span class="sxs-lookup"><span data-stu-id="04d24-160">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer that manages Group Policy for UE-V.</span></span> <span data-ttu-id="04d24-161">Перейдите к разделу **Конфигурация пользователя**, выберите **политики**, выберите **Административные шаблоны**, щелкните **компоненты Windows**, а затем выберите **Microsoft User Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="04d24-161">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="04d24-162">Выберите параметр политики, измененный.</span><span class="sxs-lookup"><span data-stu-id="04d24-162">Select the policy setting edited.</span></span>

<span data-ttu-id="04d24-163">Для определения синхронизации агент UE-V использует следующий порядок приоритетов.</span><span class="sxs-lookup"><span data-stu-id="04d24-163">The UE-V agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="04d24-164">Порядок приоритетов для параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="04d24-164">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="04d24-165">Целевые параметры пользователей, управляемые групповой политикой: эти параметры конфигурации хранятся в разделе реестра групповой политикой `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="04d24-165">User-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="04d24-166">Целевые параметры компьютера, управляемые групповой политикой — эти параметры конфигурации хранятся в разделе реестра с помощью групповой политики `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="04d24-166">Computer-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="04d24-167">Параметры конфигурации, определяемые текущим пользователем с помощью PowerShell или WMI — эти параметры конфигурации хранятся агентом UE-V в этом разделе `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` реестра:</span><span class="sxs-lookup"><span data-stu-id="04d24-167">Configuration settings defined by the current user using PowerShell or WMI - These configuration settings are stored by the UE-V agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="04d24-168">Параметры конфигурации, определенные для компьютера с помощью PowerShell или WMI.</span><span class="sxs-lookup"><span data-stu-id="04d24-168">Configuration settings defined for the computer using PowerShell or WMI.</span></span> <span data-ttu-id="04d24-169">Эти параметры конфигурации хранятся агентом UE-V в разделе `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="04d24-169">These configuration settings are stored by the UE-V agent under the `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration`.</span></span>

## <span data-ttu-id="04d24-170">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="04d24-170">Related topics</span></span>


[<span data-ttu-id="04d24-171">Администрирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="04d24-171">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="04d24-172">Операции в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="04d24-172">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





