---
title: Настройка UE-V 2. x с объектами групповой политики
description: Настройка UE-V 2. x с объектами групповой политики
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824422"
---
# <span data-ttu-id="5c619-103">Настройка UE-V 2. x с объектами групповой политики</span><span class="sxs-lookup"><span data-stu-id="5c619-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="5c619-104">Некоторые параметры групповой политики для Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 и 2,1 SP1 можно определять для компьютеров, а другие параметры групповой политики можно определять для пользователей.</span><span class="sxs-lookup"><span data-stu-id="5c619-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="5c619-105">Дополнительные сведения о том, как установить ADMX-файлы групповой политики, можно найти [в разделе Установка шаблонов ADMX-v 2 групповой политики](https://technet.microsoft.com/library/dn458891.aspx#admx).</span><span class="sxs-lookup"><span data-stu-id="5c619-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="5c619-106">Для UE-V можно настроить следующие параметры политики.</span><span class="sxs-lookup"><span data-stu-id="5c619-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="5c619-107">Параметры групповой политики</span><span class="sxs-lookup"><span data-stu-id="5c619-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5c619-108">Имя параметра групповой политики</span><span class="sxs-lookup"><span data-stu-id="5c619-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="5c619-109">Target</span><span class="sxs-lookup"><span data-stu-id="5c619-109">Target</span></span></th>
<th align="left"><span data-ttu-id="5c619-110">Описание параметров групповой политики</span><span class="sxs-lookup"><span data-stu-id="5c619-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="5c619-111">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="5c619-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5c619-112">Текст ссылки для контакта</span><span class="sxs-lookup"><span data-stu-id="5c619-112">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-113">Только компьютеры</span><span class="sxs-lookup"><span data-stu-id="5c619-113">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-114">Этот параметр групповой политики указывает текст гиперссылки на URL-адрес контакта в центре параметров компании.</span><span class="sxs-lookup"><span data-stu-id="5c619-114">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-115">Если вы включите этот параметр групповой политики, в центре параметров компании отображается указанный текст в ссылке на URL-адрес контакта.</span><span class="sxs-lookup"><span data-stu-id="5c619-115">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5c619-116">Свяжитесь с URL-адресом</span><span class="sxs-lookup"><span data-stu-id="5c619-116">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-117">Только компьютеры</span><span class="sxs-lookup"><span data-stu-id="5c619-117">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-118">Этот параметр групповой политики указывает URL-адрес ссылки на контакт в центре параметров компании.</span><span class="sxs-lookup"><span data-stu-id="5c619-118">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-119">Если этот параметр включен, текст контакта в центре параметров компании ссылается на указанный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5c619-119">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="5c619-120">Ссылка может относиться к любому стандартному протоколу, например HTTP или mailto.</span><span class="sxs-lookup"><span data-stu-id="5c619-120">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5c619-121">Не используйте поставщика синхронизации</span><span class="sxs-lookup"><span data-stu-id="5c619-121">Do not use the sync provider</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-122">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="5c619-122">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-123">Используя этот параметр групповой политики, вы можете указать, использует ли UE-V функцию поставщика синхронизации.</span><span class="sxs-lookup"><span data-stu-id="5c619-123">By using this Group Policy setting, you can configure whether UE-V uses the sync provider feature.</span></span> <span data-ttu-id="5c619-124">Этот параметр политики также позволяет отображать уведомления о задержке при импорте параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="5c619-124">This policy setting also lets you enable notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-125">Включите этот параметр, чтобы настроить агент UE-V не использовать поставщик синхронизации.</span><span class="sxs-lookup"><span data-stu-id="5c619-125">Enable this setting to configure the UE-V Agent not to use the sync provider.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5c619-126">Уведомление о первом использовании</span><span class="sxs-lookup"><span data-stu-id="5c619-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-127">Только компьютеры</span><span class="sxs-lookup"><span data-stu-id="5c619-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-128">Этот параметр групповой политики включает уведомление в области уведомлений, которое появляется при использовании UE-V</span><span class="sxs-lookup"><span data-stu-id="5c619-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="5c619-129">агент запускается в первый раз.</span><span class="sxs-lookup"><span data-stu-id="5c619-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-130">По умолчанию включено.</span><span class="sxs-lookup"><span data-stu-id="5c619-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5c619-131">Перемещаемые параметры Windows</span><span class="sxs-lookup"><span data-stu-id="5c619-131">Roam Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-132">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="5c619-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-133">Этот параметр групповой политики позволяет настроить синхронизацию параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="5c619-133">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-134">Выберите параметры Windows, которые синхронизируются между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="5c619-134">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="5c619-135">По умолчанию темы Windows, параметры рабочего стола и параметры специальных возможностей синхронизируют параметры между компьютерами одной и той же версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5c619-135">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5c619-136">Порог предупреждений о размере пакета параметров</span><span class="sxs-lookup"><span data-stu-id="5c619-136">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-137">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="5c619-137">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-138">Этот параметр групповой политики позволяет настроить агент UE-V для отчета о том, что размер файла пакета параметров достигнет определенного порогового значения.</span><span class="sxs-lookup"><span data-stu-id="5c619-138">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-139">Укажите предпочтительный порог для размера пакета параметров в килобайтах (КБ).</span><span class="sxs-lookup"><span data-stu-id="5c619-139">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="5c619-140">По умолчанию агент UE-V не имеет порогового значения размера файла пакета.</span><span class="sxs-lookup"><span data-stu-id="5c619-140">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5c619-141">Путь к хранилищу параметров</span><span class="sxs-lookup"><span data-stu-id="5c619-141">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-142">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="5c619-142">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-143">Этот параметр групповой политики определяет, где будут храниться параметры пользователя.</span><span class="sxs-lookup"><span data-stu-id="5c619-143">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-144">Введите UNC-путь и переменные (например, \Server\SettingsShare%username%.).</span><span class="sxs-lookup"><span data-stu-id="5c619-144">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5c619-145">Путь к каталогу шаблонов параметров</span><span class="sxs-lookup"><span data-stu-id="5c619-145">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-146">Только компьютеры</span><span class="sxs-lookup"><span data-stu-id="5c619-146">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-147">Этот параметр групповой политики определяет, где хранятся шаблоны расположений настраиваемых параметров.</span><span class="sxs-lookup"><span data-stu-id="5c619-147">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="5c619-148">Этот параметр политики также указывает, следует ли использовать каталог для замены стандартных шаблонов Microsoft, установленных с помощью UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="5c619-148">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-149">Введите путь UNC (Universal Naming Convention), например \Server\TemplateShare или папку на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5c619-149">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="5c619-150">Установите флажок, чтобы заменить используемые по умолчанию шаблоны Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5c619-150">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5c619-151">Синхронизация параметров для лимитных подключений</span><span class="sxs-lookup"><span data-stu-id="5c619-151">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-152">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="5c619-152">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-153">Этот параметр групповой политики определяет, будет ли UE-V синхронизировать параметры через Лимитные подключения.</span><span class="sxs-lookup"><span data-stu-id="5c619-153">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-154">По умолчанию агент UE-V не синхронизирует параметры для лимитного подключения.</span><span class="sxs-lookup"><span data-stu-id="5c619-154">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5c619-155">Синхронизация параметров для лимитных подключений даже при роуминге</span><span class="sxs-lookup"><span data-stu-id="5c619-155">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-156">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="5c619-156">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-157">Этот параметр групповой политики определяет, синхронизируют ли UE-V параметры с лимитным подключением за пределами домашней сети поставщика услуг, например при подключении к данным в режиме роуминга.</span><span class="sxs-lookup"><span data-stu-id="5c619-157">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-158">По умолчанию UE-V не синхронизирует параметры при подключении с лимитным тарифным планом, если он находится в режиме роуминга.</span><span class="sxs-lookup"><span data-stu-id="5c619-158">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5c619-159">Время ожидания синхронизации</span><span class="sxs-lookup"><span data-stu-id="5c619-159">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-160">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="5c619-160">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-161">Этот параметр групповой политики позволяет настроить время ожидания компьютера до истечения времени ожидания при извлечении параметров пользователей из расположения Remote Settings (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="5c619-161">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="5c619-162">Если место в внешнем хранилище недоступно, а пользователь не использует поставщика синхронизации, запуск приложения задерживается на это количество миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="5c619-162">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-163">Укажите предпочтительное время ожидания синхронизации в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="5c619-163">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="5c619-164">Значение по умолчанию — 2000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="5c619-164">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5c619-165">Значок на панели задач</span><span class="sxs-lookup"><span data-stu-id="5c619-165">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-166">Только компьютеры</span><span class="sxs-lookup"><span data-stu-id="5c619-166">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-167">Этот параметр групповой политики включает значок панели виртуализации взаимодействия с пользователем (UE-V).</span><span class="sxs-lookup"><span data-stu-id="5c619-167">This Group Policy setting enables the User Experience Virtualization (UE-V) tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-168">По умолчанию включено.</span><span class="sxs-lookup"><span data-stu-id="5c619-168">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5c619-169">Использование виртуализации взаимодействия с пользователем (UE-V)</span><span class="sxs-lookup"><span data-stu-id="5c619-169">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-170">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="5c619-170">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-171">Этот параметр групповой политики позволяет включить или отключить виртуализацию взаимодействия с пользователем (UE-V).</span><span class="sxs-lookup"><span data-stu-id="5c619-171">This Group Policy setting lets you enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-172">Включите или отключите этот параметр групповой политики.</span><span class="sxs-lookup"><span data-stu-id="5c619-172">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5c619-173">**Примечание**  Кроме того, параметры групповой политики доступны для многих классических приложений и приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="5c619-173">**Note** In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="5c619-174">Вы можете использовать эти параметры, чтобы включить или отключить синхронизацию параметров для конкретных приложений.</span><span class="sxs-lookup"><span data-stu-id="5c619-174">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="5c619-175">Параметры групповой политики приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="5c619-175">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5c619-176">Имя параметра групповой политики</span><span class="sxs-lookup"><span data-stu-id="5c619-176">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="5c619-177">Target</span><span class="sxs-lookup"><span data-stu-id="5c619-177">Target</span></span></th>
<th align="left"><span data-ttu-id="5c619-178">Описание параметров групповой политики</span><span class="sxs-lookup"><span data-stu-id="5c619-178">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="5c619-179">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="5c619-179">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5c619-180">Не синхронизировать приложения для Windows</span><span class="sxs-lookup"><span data-stu-id="5c619-180">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-181">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="5c619-181">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-182">Этот параметр групповой политики определяет, будет ли агент UE-V синхронизировать параметры для приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="5c619-182">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-183">По умолчанию выполняется синхронизация приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="5c619-183">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5c619-184">Список приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="5c619-184">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-185">Компьютер и пользователь</span><span class="sxs-lookup"><span data-stu-id="5c619-185">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-186">Этот параметр перечисляет имена семейных пакетов приложений для Windows и определяет, будут ли UE-V синхронизировать параметры приложения.</span><span class="sxs-lookup"><span data-stu-id="5c619-186">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-187">Вы можете использовать этот параметр, чтобы указать, что параметры приложения никогда не синхронизируются с помощью UE-V, даже если параметры всех других приложений для Windows синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="5c619-187">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5c619-188">Синхронизация приложений для Windows, не имеющих списка</span><span class="sxs-lookup"><span data-stu-id="5c619-188">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-189">Компьютер и пользователь</span><span class="sxs-lookup"><span data-stu-id="5c619-189">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-190">Этот параметр групповой политики определяет поведение синхронизации параметров по умолчанию для агента UE-V для приложений для Windows, которые явно не указаны в списке приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="5c619-190">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5c619-191">По умолчанию агент UE-V синхронизирует только параметры тех приложений Windows, которые включены в список приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="5c619-191">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5c619-192">Дополнительные сведения о синхронизации приложений для Windows можно найти в разделе [список приложений для Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="5c619-192">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="5c619-193">Настройка параметров групповой политики, назначенных для компьютера</span><span class="sxs-lookup"><span data-stu-id="5c619-193">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="5c619-194">С помощью консоли управления групповыми политиками (GPMC) или расширенного управления групповыми политиками (групповой политики) на компьютере, который выступает в качестве контроллера домена, для управления параметрами групповой политики для компьютеров UE-V.</span><span class="sxs-lookup"><span data-stu-id="5c619-194">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="5c619-195">Перейдите к разделу **Конфигурация компьютера**, выберите **политики**, выберите **Административные шаблоны**, щелкните **компоненты Windows**, а затем выберите **Microsoft User Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="5c619-195">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="5c619-196">Выберите параметр групповой политики, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="5c619-196">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="5c619-197">Настройка параметров групповой политики, предназначенных для пользователей</span><span class="sxs-lookup"><span data-stu-id="5c619-197">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="5c619-198">С помощью консоли управления групповыми политиками (GPMC) или расширенного управления групповыми политиками в пакете Microsoft Desktop Optimization Pack (MDOP) на компьютере контроллера домена можно управлять параметрами групповой политики для UE-V.</span><span class="sxs-lookup"><span data-stu-id="5c619-198">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="5c619-199">Перейдите к разделу **Конфигурация пользователя**, выберите **политики**, выберите **Административные шаблоны**, щелкните **компоненты Windows**, а затем выберите **Microsoft User Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="5c619-199">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="5c619-200">Выберите измененный параметр групповой политики.</span><span class="sxs-lookup"><span data-stu-id="5c619-200">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="5c619-201">Для определения синхронизации агент UE-V использует следующий порядок приоритетов.</span><span class="sxs-lookup"><span data-stu-id="5c619-201">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="5c619-202">Порядок приоритетов для параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="5c619-202">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="5c619-203">Пользовательские параметры, управляемые параметрами групповой политики: эти параметры конфигурации хранятся в разделе реестра с помощью групповой политики `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="5c619-203">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="5c619-204">Параметры, целевые для компьютера и управляемые параметрами групповой политики: эти параметры конфигурации хранятся в разделе реестра с помощью групповой политики `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="5c619-204">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="5c619-205">Параметры конфигурации, определяемые текущим пользователем с помощью Windows PowerShell или инструментария управления Windows (WMI) — эти параметры конфигурации хранятся агентом UE-V в этой папке `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` реестра:</span><span class="sxs-lookup"><span data-stu-id="5c619-205">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="5c619-206">Параметры конфигурации, определенные для компьютера с помощью Windows PowerShell или WMI.</span><span class="sxs-lookup"><span data-stu-id="5c619-206">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="5c619-207">Эти параметры конфигурации хранятся агентом UE-V в этой папке `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` реестра:</span><span class="sxs-lookup"><span data-stu-id="5c619-207">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="5c619-208">**У вас есть предложение UE-V**?</span><span class="sxs-lookup"><span data-stu-id="5c619-208">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="5c619-209">Здесь вы можете добавить предложения и проголосовать [здесь](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="5c619-209">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="5c619-210">**У вас возникла ошибка UE-V**?</span><span class="sxs-lookup"><span data-stu-id="5c619-210">**Got a UE-V issue**?</span></span> <span data-ttu-id="5c619-211">Воспользуйтесь [форумом на сайте UE-V TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="5c619-211">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="5c619-212">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5c619-212">Related topics</span></span>


[<span data-ttu-id="5c619-213">Администрирование UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="5c619-213">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="5c619-214">Управление конфигурациями UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="5c619-214">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





