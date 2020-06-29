---
title: Планирование того, какие приложения необходимо синхронизировать с UE-V 1.0
description: Планирование того, какие приложения необходимо синхронизировать с UE-V 1.0
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812416"
---
# <span data-ttu-id="30696-103">Планирование того, какие приложения необходимо синхронизировать с UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="30696-103">Planning Which Applications to Synchronize with UE-V 1.0</span></span>


<span data-ttu-id="30696-104">Виртуализация взаимодействия с пользователем Microsoft (UE-V) использует шаблоны расположений параметров (XML-файлы), которые определяют параметры, которые записываются и применяются UE-V.</span><span class="sxs-lookup"><span data-stu-id="30696-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="30696-105">UE-V включает набор предопределенных шаблонов расположений параметров, а также позволяет администраторам создавать пользовательские шаблоны расположений для сторонних или бизнес-приложений, используемых в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="30696-105">UE-V includes a set of predefined settings location templates and also allows administrators to create custom settings location templates for third-party or line-of-business applications that are used in the enterprise.</span></span>

<span data-ttu-id="30696-106">Администратор может определить, какие параметры следует включить в решение UE-V, с помощью каких из них можно настроить пользователи, а также указать, как и где хранятся параметры приложения.</span><span class="sxs-lookup"><span data-stu-id="30696-106">As an administrator, when you consider which applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="30696-107">Не у всех приложений есть параметры, которые можно настраивать или которые часто используются пользователями.</span><span class="sxs-lookup"><span data-stu-id="30696-107">Not all applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="30696-108">Кроме того, не все параметры приложений могут безопасно перемещаться на нескольких компьютерах или в разных средах.</span><span class="sxs-lookup"><span data-stu-id="30696-108">In addition, not all applications settings can safely roam across multiple computers or environments.</span></span> <span data-ttu-id="30696-109">Синхронизация параметров, отвечающих указанным ниже условиям.</span><span class="sxs-lookup"><span data-stu-id="30696-109">Synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="30696-110">Параметры, которые хранятся в расположениях, доступных пользователям.</span><span class="sxs-lookup"><span data-stu-id="30696-110">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="30696-111">Например, не следует синхронизировать параметры, которые хранятся в папке System32 или вне раздела HKCU в реестре.</span><span class="sxs-lookup"><span data-stu-id="30696-111">For example, do not synchronize settings that are stored in system32 or outside HKCU section of the registry.</span></span>

-   <span data-ttu-id="30696-112">Параметры, не связанные с конкретным компьютером.</span><span class="sxs-lookup"><span data-stu-id="30696-112">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="30696-113">Например, можно исключить конфигурацию сети или оборудования.</span><span class="sxs-lookup"><span data-stu-id="30696-113">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="30696-114">Параметры, которые можно синхронизировать между компьютерами без риска повреждения данных.</span><span class="sxs-lookup"><span data-stu-id="30696-114">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="30696-115">Например, не используйте параметры, которые хранятся в файле базы данных.</span><span class="sxs-lookup"><span data-stu-id="30696-115">For example, do not use settings that are stored in a database file.</span></span>

## <span data-ttu-id="30696-116">Шаблоны расположений параметров, которые включены в UE-V</span><span class="sxs-lookup"><span data-stu-id="30696-116">Settings location templates that are included in UE-V</span></span>


**<span data-ttu-id="30696-117">Шаблоны расположений параметров приложений UE-V</span><span class="sxs-lookup"><span data-stu-id="30696-117">UE-V application settings location templates</span></span>**

<span data-ttu-id="30696-118">Программа установки агента UE-V устанавливает агент и регистрирует стандартную группу шаблонов расположения параметров для распространенных приложений Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="30696-118">The UE-V agent installation software installs the agent and registers a default group of settings location templates for common Microsoft applications.</span></span> <span data-ttu-id="30696-119">Шаблоны расположений параметров захватывают значения параметров для следующих приложений:</span><span class="sxs-lookup"><span data-stu-id="30696-119">These settings location templates capture settings values for the following applications:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="30696-120">Категория приложения</span><span class="sxs-lookup"><span data-stu-id="30696-120">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="30696-121">Описание</span><span class="sxs-lookup"><span data-stu-id="30696-121">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30696-122">Приложения Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="30696-122">Microsoft Office 2010 applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="30696-123">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="30696-123">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="30696-124">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="30696-124">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="30696-125">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="30696-125">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="30696-126">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="30696-126">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="30696-127">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="30696-127">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="30696-128">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="30696-128">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="30696-129">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="30696-129">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="30696-130">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="30696-130">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="30696-131">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="30696-131">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="30696-132">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="30696-132">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="30696-133">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="30696-133">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="30696-134">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="30696-134">Microsoft OneNote 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30696-135">Параметры браузера (Internet Explorer 8, Internet Explorer 9 и Internet Explorer 10)</span><span class="sxs-lookup"><span data-stu-id="30696-135">Browser options (Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10)</span></span></p></td>
<td align="left"><p><span data-ttu-id="30696-136">Избранное, Домашняя страница, вкладки и панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="30696-136">Favorites, home page, tabs, and toolbars.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30696-137">Аксессуары для Windows</span><span class="sxs-lookup"><span data-stu-id="30696-137">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="30696-138">Калькулятор, Блокнот, WordPad.</span><span class="sxs-lookup"><span data-stu-id="30696-138">Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="30696-139">Параметры приложения применяются к приложению при запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="30696-139">Application settings are applied to the application when the application is started.</span></span> <span data-ttu-id="30696-140">Они сохраняются при закрытии приложения.</span><span class="sxs-lookup"><span data-stu-id="30696-140">They are saved when the application closes.</span></span>

**<span data-ttu-id="30696-141">Шаблоны расположений параметров Windows UE-V</span><span class="sxs-lookup"><span data-stu-id="30696-141">UE-V Windows settings location templates</span></span>**

<span data-ttu-id="30696-142">Виртуализация взаимодействия с пользователем включает шаблоны расположений параметров, которые захватывают значения параметров для указанных ниже параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="30696-142">User Experience Virtualization includes settings location templates that capture settings values for the following Windows settings:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30696-143">Параметры Windows</span><span class="sxs-lookup"><span data-stu-id="30696-143">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="30696-144">Описание</span><span class="sxs-lookup"><span data-stu-id="30696-144">Description</span></span></th>
<th align="left"><span data-ttu-id="30696-145">Применять</span><span class="sxs-lookup"><span data-stu-id="30696-145">Apply on</span></span></th>
<th align="left"><span data-ttu-id="30696-146">Состояние по умолчанию</span><span class="sxs-lookup"><span data-stu-id="30696-146">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30696-147">Фон рабочего стола</span><span class="sxs-lookup"><span data-stu-id="30696-147">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="30696-148">Текущий активный фон рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="30696-148">Currently active desktop background.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30696-149">Вход, разблокировка, удаленное подключение.</span><span class="sxs-lookup"><span data-stu-id="30696-149">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30696-150">Включено</span><span class="sxs-lookup"><span data-stu-id="30696-150">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30696-151">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="30696-151">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="30696-152">Специальные возможности и параметры ввода, экранная лупа, Экранный диктор и экранная клавиатура.</span><span class="sxs-lookup"><span data-stu-id="30696-152">Accessibility and input settings, magnifier, Narrator, and on-Screen keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30696-153">Вход, разблокировка, удаленное подключение.</span><span class="sxs-lookup"><span data-stu-id="30696-153">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30696-154">Отключено</span><span class="sxs-lookup"><span data-stu-id="30696-154">Disabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30696-155">Параметры рабочего стола</span><span class="sxs-lookup"><span data-stu-id="30696-155">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="30696-156">Параметры меню "Пуск" и панели задач, параметры папки, значки рабочего стола по умолчанию, дополнительные часы, параметры региона и языка.</span><span class="sxs-lookup"><span data-stu-id="30696-156">Start menu and Taskbar settings, Folder options, default desktop icons, additional clocks, and region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30696-157">Только вход.</span><span class="sxs-lookup"><span data-stu-id="30696-157">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30696-158">Отключено</span><span class="sxs-lookup"><span data-stu-id="30696-158">Disabled</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="30696-159">Параметры фона рабочего стола Windows и специальные возможности применяются при входе пользователя в систему, при снятии блокировки компьютера или при удаленном соединении с другим компьютером.</span><span class="sxs-lookup"><span data-stu-id="30696-159">The Windows desktop background and Ease of Access settings are applied when the user logs on, when the computer is unlocked, or upon remote connection to another computer.</span></span> <span data-ttu-id="30696-160">Агент сохраняет эти параметры, когда пользователь выходит из системы, когда компьютер заблокирован, или когда удаленное подключение разорвано.</span><span class="sxs-lookup"><span data-stu-id="30696-160">The agent saves these settings when the user logs off, when the computer is locked, or when a remote connection is disconnected.</span></span> <span data-ttu-id="30696-161">По умолчанию параметры фона рабочего стола Windows перемещаются между компьютерами одной и той же версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="30696-161">By default, Windows desktop background settings are roamed between computers of the same operating system version.</span></span>

<span data-ttu-id="30696-162">Настольные компьютеры с Windows и параметры специальных возможностей применяются при входе в систему, прежде чем будет представлен рабочий стол пользователю.</span><span class="sxs-lookup"><span data-stu-id="30696-162">Windows desktop and Ease of Access settings are applied at logon before the desktop is presented to the user.</span></span> <span data-ttu-id="30696-163">Для оптимизации процесса входа эти параметры не перемещаются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30696-163">To optimize the logon experience, these settings are not roamed by default.</span></span> <span data-ttu-id="30696-164">Настольные и удобные параметры доступа можно включить с помощью групповой политики, PowerShell и WMI.</span><span class="sxs-lookup"><span data-stu-id="30696-164">Desktop and Ease of Access settings can be enabled by using Group Policy, PowerShell, and WMI.</span></span>

<span data-ttu-id="30696-165">UE-V не поддерживает перемещение параметров между операционными системами разных языков.</span><span class="sxs-lookup"><span data-stu-id="30696-165">UE-V does not support the roaming of settings between operating systems with different languages.</span></span> <span data-ttu-id="30696-166">Например, синхронизация между английским и немецкий не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="30696-166">For example, synchronization between English and German is not supported.</span></span> <span data-ttu-id="30696-167">Язык всех компьютеров, на которых агент UE-V перемещает параметры пользователя должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="30696-167">The language of all computers to which UE-V roams the user settings must match.</span></span>

<span data-ttu-id="30696-168">**Примечание**  Если вы изменили шаблоны расположения параметров, предоставленные корпорацией Майкрософт, виртуализация взаимодействия с пользователем может работать неправильно для определенного приложения или группы параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="30696-168">**Note** If you change the settings location templates that are provided by Microsoft, User Experience Virtualization might not work properly for the designated application or Windows settings group.</span></span>

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a><span data-ttu-id="30696-169">Предотвращение непреднамеренной конфигурации пользовательских параметров</span><span class="sxs-lookup"><span data-stu-id="30696-169">Prevent unintentional user Settings configuration</span></span>


<span data-ttu-id="30696-170">Виртуализация взаимодействия с пользователем проверяет сведения о новых параметрах пользователей и загружает эти данные в соответствии с местом хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="30696-170">User Experience Virtualization checks for new user settings information, and downloads that information accordingly from a settings storage location.</span></span> <span data-ttu-id="30696-171">Затем эти параметры применяются к локальному компьютеру в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="30696-171">Then, it applies the settings to the local computer in the following cases:</span></span>

-   <span data-ttu-id="30696-172">Каждый раз, когда приложение запускается с зарегистрированным шаблоном UE-V.</span><span class="sxs-lookup"><span data-stu-id="30696-172">Every time an application is launched that has a registered UE-V template.</span></span>

-   <span data-ttu-id="30696-173">Когда пользователь входит в систему на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="30696-173">When a user logs on to their computer.</span></span>

-   <span data-ttu-id="30696-174">Когда пользователь снимает блокировку с компьютера.</span><span class="sxs-lookup"><span data-stu-id="30696-174">When a user unlocks their computer.</span></span>

-   <span data-ttu-id="30696-175">Подключение к удаленному рабочему столу, на котором установлен UE-V.</span><span class="sxs-lookup"><span data-stu-id="30696-175">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

<span data-ttu-id="30696-176">Если UE-V установлен на компьютере A и на компьютере B, а необходимые параметры приложения находятся на компьютере A, сначала необходимо открыть и закрыть приложение.</span><span class="sxs-lookup"><span data-stu-id="30696-176">If UE-V is installed on computer A and computer B, and the desired settings for the application are on computer A, then computer A must open and close the application first.</span></span> <span data-ttu-id="30696-177">Если приложение сначала открывается и закрывается на компьютере B, параметры приложения на компьютере A будут совпадать с параметрами приложения на компьютере B.</span><span class="sxs-lookup"><span data-stu-id="30696-177">If an application is opened and closed on computer B first, then the application settings on computer A will be configured to be the same as the application settings on computer B.</span></span>

<span data-ttu-id="30696-178">Этот сценарий также применим к параметрам Windows.</span><span class="sxs-lookup"><span data-stu-id="30696-178">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="30696-179">Если параметры Windows на компьютере B должны совпадать с параметрами Windows на компьютере A, пользователю следует сначала войти в систему и выйти из нее.</span><span class="sxs-lookup"><span data-stu-id="30696-179">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should logon and logoff computer A first.</span></span>

<span data-ttu-id="30696-180">Если нужные параметры пользователей применяются в неправильном порядке, их можно восстановить, выполнив операцию восстановления для определенного приложения или конфигурации Windows на компьютере, на котором были переписаны параметры.</span><span class="sxs-lookup"><span data-stu-id="30696-180">If the desired user settings are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="30696-181">Дополнительные сведения можно найти [в разделе Восстановление параметров приложений и Windows, синхронизированных с UE-V 1,0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="30696-181">For more information, see [Restoring Application and Windows Settings Synchronized with UE-V 1.0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).</span></span>

## <span data-ttu-id="30696-182">Пользовательские шаблоны расположения параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="30696-182">Custom UE-V settings location templates</span></span>


<span data-ttu-id="30696-183">Вы можете создавать шаблоны расположений с пользовательскими параметрами с помощью генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="30696-183">You can create custom settings location templates by using the UE-V Generator.</span></span> <span data-ttu-id="30696-184">После создания и проверки настраиваемого шаблона расположения параметров в тестовой среде вы можете развернуть шаблоны расположений параметров на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="30696-184">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span> <span data-ttu-id="30696-185">Пользовательские шаблоны расположений параметров должны развертываться с помощью существующей инфраструктуры развертывания, например с помощью метода распространения программного обеспечения (ESD), с параметрами или настроив каталог шаблонов UE-V Settings.</span><span class="sxs-lookup"><span data-stu-id="30696-185">Custom settings location templates must be deployed with an existing deployment infrastructure, such as enterprise software distribution (ESD) method, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="30696-186">Шаблоны, развернутые с помощью ESD или групповой политики, должны быть зарегистрированы с помощью UE-V WMI или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30696-186">Templates that are deployed with ESD or Group Policy must be registered by using UE-V WMI or PowerShell.</span></span> <span data-ttu-id="30696-187">Дополнительные сведения о шаблонах расположений для настраиваемых параметров можно найти в разделе [Планирование развертывания настраиваемого шаблона для UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="30696-187">For more information about custom settings location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

<span data-ttu-id="30696-188">Сведения о том, следует ли синхронизировать бизнес-приложение, можно найти в статье [Контрольный список для оценки бизнес-приложений для UE-V 1,0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="30696-188">For guidance on whether a line-of-business application should be synchronized, see [Checklist for Evaluating Line-of-Business Applications for UE-V 1.0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span></span>

## <span data-ttu-id="30696-189">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="30696-189">Related topics</span></span>


[<span data-ttu-id="30696-190">Планирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="30696-190">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="30696-191">Планирование развертывания пользовательского шаблона для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="30696-191">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

[<span data-ttu-id="30696-192">Развертывание UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="30696-192">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

 

 





