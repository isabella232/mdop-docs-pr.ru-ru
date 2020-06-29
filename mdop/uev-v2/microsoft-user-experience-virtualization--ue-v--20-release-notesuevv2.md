---
title: Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.0
description: Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.0
author: dansimp
ms.assetid: 5ef66cd1-ba2b-4383-9f45-e7cde41f1ba1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad3deffa5cd567a70711e5447197e630f04ea254
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825282"
---
# <span data-ttu-id="be690-103">Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.0</span><span class="sxs-lookup"><span data-stu-id="be690-103">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>


<span data-ttu-id="be690-104">Чтобы выполнить поиск в заметках о выпуске Microsoft User Experience Virtualization (UE-V) 2,0, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="be690-104">To search Microsoft User Experience Virtualization (UE-V) 2.0 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="be690-105">Перед установкой UE-V вы должны внимательно прочитать эти заметки о выпуске.</span><span class="sxs-lookup"><span data-stu-id="be690-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="be690-106">Заметки о выпуске содержат сведения, необходимые для успешной установки виртуализации взаимодействия с пользователем, и содержат дополнительные сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="be690-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="be690-107">Если между этими заметками о выпуске и другой документацией UE-V есть различия, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="be690-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="be690-108">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="be690-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="be690-109">Предоставление отзыва</span><span class="sxs-lookup"><span data-stu-id="be690-109">Providing feedback</span></span>


<span data-ttu-id="be690-110">Расскажите нам, что вы думаете о нашей документации для MDOP, предоставив нам свой отзыв и комментарии.</span><span class="sxs-lookup"><span data-stu-id="be690-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="be690-111">Отправьте отзыв о документации в [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="be690-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="be690-112">Известные проблемы UE-V</span><span class="sxs-lookup"><span data-stu-id="be690-112">UE-V known issues</span></span>


<span data-ttu-id="be690-113">В этом разделе содержатся заметки о выпуске для виртуализации взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="be690-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="be690-114">Параметры реестра не синхронизируются между приложением App-V и приложениями машинного кода на одном компьютере</span><span class="sxs-lookup"><span data-stu-id="be690-114">Registry settings do not synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="be690-115">Если на компьютере установлено приложение, установленное как с помощью Application Virtualization (App-V), так и локально с помощью установщика Windows (MSI-файла), параметры, основанные на реестре, не синхронизируются между этими технологиями.</span><span class="sxs-lookup"><span data-stu-id="be690-115">When a computer has an application that is installed through both Application Virtualization (App-V) and a locally with a Windows Installer (.msi) file, the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="be690-116">**Временное решение:** Чтобы устранить эту проблему, запустите приложение, выбрав одну из двух технологий, но не то, и другое.</span><span class="sxs-lookup"><span data-stu-id="be690-116">**WORKAROUND:** To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="settings-do-not-synchronization-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="be690-117">Параметры не синхронизируются, если сетевая доля выходит за пределы домена пользователя</span><span class="sxs-lookup"><span data-stu-id="be690-117">Settings do not synchronization when network share is outside user’s domain</span></span>

<span data-ttu-id="be690-118">Если Windows® 8 попытается синхронизировать параметры операционной системы, синхронизация завершается сбоем со следующим сообщением об ошибке: **"Boost:: FileSystem:: EXISTS": неверное имя пользователя или пароль**.</span><span class="sxs-lookup"><span data-stu-id="be690-118">When Windows® 8 attempts operating system settings synchronization, the synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="be690-119">Эта ошибка может указывать на то, что сетевой общий доступ находится за пределами домена пользователя или домена с отношением доверия с этим доменом.</span><span class="sxs-lookup"><span data-stu-id="be690-119">This error can indicate that the network share is outside the user’s domain or a domain with a trust relationship to that domain.</span></span> <span data-ttu-id="be690-120">Чтобы проверить работоспособность журнала событий, откройте **средство просмотра событий** и перейдите в раздел " **приложения и службы**", которые регистрируются в журнале  /  **Microsoft**  /  **виртуализации Microsoft User Experience**  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="be690-120">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="be690-121">Общие сетевые ресурсы, используемые для расположений хранилищ параметров UE-V, должны располагаться в том же домене Active Directory, что и пользователь, либо доверенный домен домена пользователя.</span><span class="sxs-lookup"><span data-stu-id="be690-121">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user or a trusted domain of the user’s domain.</span></span>

<span data-ttu-id="be690-122">**Временное решение:** Используйте общие сетевые ресурсы из того же домена Active Directory, что и пользователь.</span><span class="sxs-lookup"><span data-stu-id="be690-122">**WORKAROUND:** Use network shares from the same Active Directory domain as the user.</span></span>

### <span data-ttu-id="be690-123">Непредсказуемые результаты с установленными приложениями Office 2010 и Office 2013</span><span class="sxs-lookup"><span data-stu-id="be690-123">Unpredictable results with both Office 2010 and Office 2013 installed</span></span>

<span data-ttu-id="be690-124">Если у пользователя установлен и Office 2010, и Office 2013, все общие параметры, которые поддерживаются двумя версиями Office, перемещаются UE-V.</span><span class="sxs-lookup"><span data-stu-id="be690-124">When a user has both Office 2010 and Office 2013 installed, any common settings between the two versions of Office are roamed by UE-V.</span></span> <span data-ttu-id="be690-125">Это может привести к тому, что размер пакета Office 2010 станет довольно большим или привести к непредсказуемым конфликтам с 2013, особенно если используется Office 365.</span><span class="sxs-lookup"><span data-stu-id="be690-125">This could cause the Office 2010 package size to be quite large or result in unpredictable conflicts with 2013, particularly if Office 365 is used.</span></span>

<span data-ttu-id="be690-126">**Временное решение:** Установка только одной версии Office или ограничение параметров синхронизации UE-V.</span><span class="sxs-lookup"><span data-stu-id="be690-126">**WORKAROUND:** Install only one version of Office or limit which settings are synchronized by UE-V.</span></span>

### <span data-ttu-id="be690-127">Удаление и повторная установка приложения для Windows 8 восстанавливает исходное состояние параметров</span><span class="sxs-lookup"><span data-stu-id="be690-127">Uninstall and re-install of Windows 8 app reverts settings to initial state</span></span>

<span data-ttu-id="be690-128">При использовании синхронизации параметров UE-V для приложения Windows 8, если пользователь удаляет приложение, а затем переустанавливает приложение, параметры приложения возвращаются к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="be690-128">While using UE-V settings synchronization for a Windows 8 app, if the user uninstalls the app and then reinstalls the app, the app’s settings revert to their default values.</span></span><span data-ttu-id="be690-129">Это происходит из-за того, что при удалении удаляется локальная (кэшированная) копия параметров приложения, но не удаляется локальный пакет параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="be690-129"> This happens because the uninstall removes the local (cached) copy of the app’s settings but does not remove the local UE-V settings package.</span></span><span data-ttu-id="be690-130">После повторной установки и запуска приложения UE-V собирает параметры приложения, которые были восстановлены в приложении по умолчанию, а затем загружают параметры по умолчанию в центральное место хранения.</span><span class="sxs-lookup"><span data-stu-id="be690-130"> When the app is reinstalled and launched, UE-V gather the app settings that were reset to the app defaults and then uploads the default settings to the central storage location.</span></span><span data-ttu-id="be690-131">Другие компьютеры, на которых запущено приложение, затем скачайте параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="be690-131"> Other computers running the app then download the default settings.</span></span><span data-ttu-id="be690-132">Такое поведение аналогично поведению классических приложений.</span><span class="sxs-lookup"><span data-stu-id="be690-132"> This behavior is identical to the behavior of desktop applications.</span></span>

<span data-ttu-id="be690-133">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="be690-133">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="be690-134">Перемещение подписей электронной почты в Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="be690-134">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="be690-135">UE-V перемещает файлы подписей Outlook 2010 между устройствами.</span><span class="sxs-lookup"><span data-stu-id="be690-135">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="be690-136">Однако параметры подписи по умолчанию для новых сообщений, ответов и пересылаемых писем не синхронизируются.</span><span class="sxs-lookup"><span data-stu-id="be690-136">However, the default signature options for new messages and replies or forwards are not synchronized.</span></span> <span data-ttu-id="be690-137">Эти два параметра хранятся в профиле Outlook, который UE-V не перемещается.</span><span class="sxs-lookup"><span data-stu-id="be690-137">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="be690-138">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="be690-138">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="be690-139">UE-V не поддерживает перемещаемые параметры между 32-битным и 64-разрядными версиями Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="be690-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="be690-140">Рекомендуем установить 64-разрядную версию Microsoft Office для современных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="be690-140">We recommend that you install the 64-bit version of Microsoft Office for modern computers.</span></span> <span data-ttu-id="be690-141">Чтобы узнать, какая версия вам нужна, [щелкните здесь](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span><span class="sxs-lookup"><span data-stu-id="be690-141">To determine which version you need, [click here](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span></span> <span data-ttu-id="be690-142">UE-V поддерживает перемещаемые параметры между идентичными версиями Office.</span><span class="sxs-lookup"><span data-stu-id="be690-142">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="be690-143">Например, 32-разрядные параметры Office будут перемещаться между всеми 32-разрядными экземплярами Office.</span><span class="sxs-lookup"><span data-stu-id="be690-143">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="be690-144">UE-V не поддерживает перемещаемые параметры между 32-битным и 64-разрядными версиями Office.</span><span class="sxs-lookup"><span data-stu-id="be690-144">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="be690-145">**Временное решение:** Ничего</span><span class="sxs-lookup"><span data-stu-id="be690-145">**WORKAROUND:** None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="be690-146">MSI не локализованы</span><span class="sxs-lookup"><span data-stu-id="be690-146">MSI’s are not localized</span></span>

<span data-ttu-id="be690-147">UE-V 2,0 включает локализованную программу установки для агента UE-V и генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="be690-147">UE-V 2.0 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="be690-148">Эти файлы MSI по-прежнему доступны, но пользовательский интерфейс минимизирован и отображается только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="be690-148">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="be690-149">Несмотря на то, что файл находится на английском языке, во время установки программа установки устанавливает все поддерживаемые языки.</span><span class="sxs-lookup"><span data-stu-id="be690-149">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="be690-150">**Временное решение:** Ничего</span><span class="sxs-lookup"><span data-stu-id="be690-150">**WORKAROUND:** None</span></span>

### <span data-ttu-id="be690-151">Favicons, связанные с браузером Internet Explorer 9, не перемещаются</span><span class="sxs-lookup"><span data-stu-id="be690-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="be690-152">Favicons, связанные с браузером Internet Explorer 9, не перемещаются с помощью виртуализации взаимодействия с пользователем и не отображаются при первом появлении этого списка на новом компьютере.</span><span class="sxs-lookup"><span data-stu-id="be690-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="be690-153">**Временное решение:** После использования закладки и кэширования в браузере Internet Explorer 9 будет выводиться Favicons с соответствующими избранными.</span><span class="sxs-lookup"><span data-stu-id="be690-153">**WORKAROUND:** Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="be690-154">Пути к параметрам файла хранятся в реестре</span><span class="sxs-lookup"><span data-stu-id="be690-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="be690-155">Некоторые параметры приложения хранят пути файлов конфигурации и параметров в виде значений в реестре.</span><span class="sxs-lookup"><span data-stu-id="be690-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="be690-156">Файлы, на которые указывают ссылки в реестре, должны быть синхронизированы при перемещении параметров между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="be690-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="be690-157">**Временное решение:** С помощью перенаправления папок или других технологий убедитесь, что файлы, на которые указывают ссылки, указаны в одном и том же месте на всех компьютерах, где параметры перемещаются.</span><span class="sxs-lookup"><span data-stu-id="be690-157">**WORKAROUND:** Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="be690-158">Путь к хранилищу с длинными параметрами может вызвать ошибку</span><span class="sxs-lookup"><span data-stu-id="be690-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="be690-159">Храните пути к хранилищу параметров как можно короче.</span><span class="sxs-lookup"><span data-stu-id="be690-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="be690-160">Длинные пути могут не допускать разрешения и синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="be690-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="be690-161">UE-V использует путь к хранилищу параметров как часть расчетного пути для хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="be690-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="be690-162">Этот путь вычисляется следующим образом: параметры путь к хранилищу и "settingspackages" + Dir (ИД шаблона) + имя пакета (идентификатор шаблона) +. pkgx.</span><span class="sxs-lookup"><span data-stu-id="be690-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID) + .pkgx.</span></span> <span data-ttu-id="be690-163">Если размер вычисляемого пути превышает 260 символов, в журнале событий UE-V память пакета завершается сбоем и генерируется следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="be690-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="be690-164">Для проверки событий журнала в журнале откройте средство просмотра событий и перейдите в раздел Журналы приложений и служб/Microsoft/пользовательский интерфейс, виртуализация и ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="be690-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="be690-165">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="be690-165">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="be690-166">Некоторые параметры операционной системы перемещаются только в том случае, если они есть в версиях операционной системы</span><span class="sxs-lookup"><span data-stu-id="be690-166">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="be690-167">Параметры операционной системы для символов экранного диктора и денежных единиц, относящихся к национальной настройке (например, язык и региональные стандарты), будут перемещаться только в версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="be690-167">Operating system settings for Narrator and currency characters specific to the locale (i.e. language and regional settings) will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="be690-168">Например, символы денежных единиц не будут перемещаться между Windows 7 и Windows 8.</span><span class="sxs-lookup"><span data-stu-id="be690-168">For example, currency characters will not roam between Windows 7 and Windows 8.</span></span>

<span data-ttu-id="be690-169">**Временное решение:** Ничего</span><span class="sxs-lookup"><span data-stu-id="be690-169">**WORKAROUND:** None</span></span>

### <span data-ttu-id="be690-170">Приложения для Windows 8 не синхронизируют параметры после того, как приложение перезапускается после неожиданного закрытия</span><span class="sxs-lookup"><span data-stu-id="be690-170">Windows 8 apps do not sync settings when the app restarts after closing unexpectedly</span></span>

<span data-ttu-id="be690-171">Если приложение Windows 8 неожиданно закрывается после запуска, параметры приложения могут быть не синхронизированы при перезапуске приложения.</span><span class="sxs-lookup"><span data-stu-id="be690-171">If a Windows 8 app closes unexpectedly soon after startup, settings for the application may not be synchronized when the application is restarted.</span></span>

<span data-ttu-id="be690-172">**Временное решение:** Закройте приложение для Windows 8, закройте и перезапустите приложение UevAppMonitor.exe (может использовать TaskManager), а затем перезапустите приложение Windows 8.</span><span class="sxs-lookup"><span data-stu-id="be690-172">**WORKAROUND:** Close the Windows 8 app, close and restart the UevAppMonitor.exe application (can use TaskManager), and then restart the Windows 8 app.</span></span>

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a><span data-ttu-id="be690-173">Агент UE-V 1 вызывает ошибки при запуске шаблонов UE-V 2</span><span class="sxs-lookup"><span data-stu-id="be690-173">UE-V 1 agent generates errors when running UE-V 2 templates</span></span>

<span data-ttu-id="be690-174">Если шаблон расположений параметров UE-V 2 распространяется на компьютер, установленный с агентом UE-V 1, некоторые параметры не синхронизируются между компьютерами, и агент сообщает об ошибках в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="be690-174">If a UE-V 2 settings location template is distributed to a computer installed with a UE-V 1 agent, some settings fail to synchronize between computers and the agent reports errors in the event log.</span></span>

<span data-ttu-id="be690-175">**Временное решение:** При переходе с UE-V 1 на UE-V 2 и, возможно, у вас есть компьютеры, на которых работает Предыдущая версия агента, создайте отдельный каталог UE-V 2,0 для поддержки агента и шаблонов UE-v 2,0.</span><span class="sxs-lookup"><span data-stu-id="be690-175">**WORKAROUND:** When migrating from UE-V 1 to UE-V 2 and it is likely you’ll have computers running the previous version of the agent, create a separate UE-V 2.0 catalog to support the UE-V 2.0 Agent and templates.</span></span>

## <span data-ttu-id="be690-176">Исправления и статьи базы знаний для UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="be690-176">Hotfixes and Knowledge Base articles for UE-V 2.0</span></span>


<span data-ttu-id="be690-177">В этом разделе содержатся исправления и статьи базы знаний для UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="be690-177">This section contains hotfixes and KB articles for UE-V 2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="be690-178">Статья базы знаний</span><span class="sxs-lookup"><span data-stu-id="be690-178">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="be690-179">Title</span><span class="sxs-lookup"><span data-stu-id="be690-179">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="be690-180">Ссылка</span><span class="sxs-lookup"><span data-stu-id="be690-180">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be690-181">2927019</span><span class="sxs-lookup"><span data-stu-id="be690-181">2927019</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-182">Пакет исправлений 1 для Microsoft User Experience Virtualization 2,0</span><span class="sxs-lookup"><span data-stu-id="be690-182">Hotfix Package 1 for Microsoft User Experience Virtualization 2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2927019" data-raw-source="[support.microsoft.com/kb/2927019](https://support.microsoft.com/kb/2927019)"><span data-ttu-id="be690-183">support.microsoft.com/kb/2927019</span><span class="sxs-lookup"><span data-stu-id="be690-183">support.microsoft.com/kb/2927019</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be690-184">2903501</span><span class="sxs-lookup"><span data-stu-id="be690-184">2903501</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-185">UE-V: совместимость с интерфейсом пользователя (UE-V) Compatibility с профилями пользователей</span><span class="sxs-lookup"><span data-stu-id="be690-185">UE-V: User Experience Virtualization (UE-V) compatibility with user profiles</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)"><span data-ttu-id="be690-186">support.microsoft.com/kb/2903501/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-186">support.microsoft.com/kb/2903501/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be690-187">2770042</span><span class="sxs-lookup"><span data-stu-id="be690-187">2770042</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-188">Параметры реестра UE-V</span><span class="sxs-lookup"><span data-stu-id="be690-188">UE-V Registry Settings</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)"><span data-ttu-id="be690-189">support.microsoft.com/kb/2770042/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-189">support.microsoft.com/kb/2770042/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be690-190">2847017</span><span class="sxs-lookup"><span data-stu-id="be690-190">2847017</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-191">Параметры UE-V реплицированы с помощью Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="be690-191">UE-V settings replicated by Internet Explorer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)"><span data-ttu-id="be690-192">support.microsoft.com/kb/2847017/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-192">support.microsoft.com/kb/2847017/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be690-193">2930271</span><span class="sxs-lookup"><span data-stu-id="be690-193">2930271</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-194">Общие сведения об ограничениях для перемещаемых подписей Outlook в Microsoft UE-V</span><span class="sxs-lookup"><span data-stu-id="be690-194">Understanding the limitations of roaming Outlook signatures in Microsoft UE-V</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2930271/EN-US" data-raw-source="[support.microsoft.com/kb/2930271/EN-US](https://support.microsoft.com/kb/2930271/EN-US)"><span data-ttu-id="be690-195">support.microsoft.com/kb/2930271/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-195">support.microsoft.com/kb/2930271/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be690-196">2769631</span><span class="sxs-lookup"><span data-stu-id="be690-196">2769631</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-197">Восстановление поврежденной установки UE-V</span><span class="sxs-lookup"><span data-stu-id="be690-197">How to repair a corrupted UE-V install</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)"><span data-ttu-id="be690-198">support.microsoft.com/kb/2769631/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-198">support.microsoft.com/kb/2769631/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be690-199">2850989</span><span class="sxs-lookup"><span data-stu-id="be690-199">2850989</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-200">Миграция профилей MAPI с помощью Microsoft UE-V не поддерживается</span><span class="sxs-lookup"><span data-stu-id="be690-200">Migrating MAPI profiles with Microsoft UE-V is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)"><span data-ttu-id="be690-201">support.microsoft.com/kb/2850989/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-201">support.microsoft.com/kb/2850989/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be690-202">2769586</span><span class="sxs-lookup"><span data-stu-id="be690-202">2769586</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-203">UE-V перемещение пустых папок и разделов реестра</span><span class="sxs-lookup"><span data-stu-id="be690-203">UE-V roams empty folders and registry keys</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)"><span data-ttu-id="be690-204">support.microsoft.com/kb/2769586/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-204">support.microsoft.com/kb/2769586/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be690-205">2782997</span><span class="sxs-lookup"><span data-stu-id="be690-205">2782997</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-206">Как включить ведение журнала отладки в Microsoft User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="be690-206">How To Enable Debug Logging in Microsoft User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)"><span data-ttu-id="be690-207">support.microsoft.com/kb/2782997/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-207">support.microsoft.com/kb/2782997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be690-208">2769570</span><span class="sxs-lookup"><span data-stu-id="be690-208">2769570</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-209">UE-V не обновляет тему в сеансах RDS и VDI</span><span class="sxs-lookup"><span data-stu-id="be690-209">UE-V does not update the theme on RDS or VDI sessions</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)"><span data-ttu-id="be690-210">support.microsoft.com/kb/2769570/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-210">support.microsoft.com/kb/2769570/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be690-211">2901856</span><span class="sxs-lookup"><span data-stu-id="be690-211">2901856</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-212">Параметры приложения не синхронизируются после принудительной перезагрузки на компьютере с поддержкой UE-V</span><span class="sxs-lookup"><span data-stu-id="be690-212">Application settings do not sync after you force a restart on a UE-V-enabled computer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2901856/EN-US" data-raw-source="[support.microsoft.com/kb/2901856/EN-US](https://support.microsoft.com/kb/2901856/EN-US)"><span data-ttu-id="be690-213">support.microsoft.com/kb/2901856/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-213">support.microsoft.com/kb/2901856/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be690-214">2850582</span><span class="sxs-lookup"><span data-stu-id="be690-214">2850582</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-215">Использование виртуализации взаимодействия с пользователем Microsoft в приложениях App-V</span><span class="sxs-lookup"><span data-stu-id="be690-215">How To Use Microsoft User Experience Virtualization With App-V Applications</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)"><span data-ttu-id="be690-216">support.microsoft.com/kb/2850582/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-216">support.microsoft.com/kb/2850582/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be690-217">3041879</span><span class="sxs-lookup"><span data-stu-id="be690-217">3041879</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-218">Текущие версии файлов для Microsoft User Experience Virtualization</span><span class="sxs-lookup"><span data-stu-id="be690-218">Current file versions for Microsoft User Experience Virtualization</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)"><span data-ttu-id="be690-219">support.microsoft.com/kb/3041879/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-219">support.microsoft.com/kb/3041879/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be690-220">2843592</span><span class="sxs-lookup"><span data-stu-id="be690-220">2843592</span></span></p></td>
<td align="left"><p><span data-ttu-id="be690-221">Сведения о виртуализации взаимодействия с пользователем и о высокой доступности</span><span class="sxs-lookup"><span data-stu-id="be690-221">Information on User Experience Virtualization and High Availability</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)"><span data-ttu-id="be690-222">support.microsoft.com/kb/2843592/EN-US</span><span class="sxs-lookup"><span data-stu-id="be690-222">support.microsoft.com/kb/2843592/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





