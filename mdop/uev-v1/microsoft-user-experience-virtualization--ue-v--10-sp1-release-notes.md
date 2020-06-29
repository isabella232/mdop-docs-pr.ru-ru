---
title: Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 1.0 с пакетом обновления 1 (SP1)
description: Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 1.0 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: 447fae0c-fe87-4d1c-b616-6f92fbdaf6d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8584999d9fdbdfccc3e9b2b1486cb97635475747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812485"
---
# <span data-ttu-id="507b4-103">Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 1.0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="507b4-103">Microsoft User Experience Virtualization (UE-V) 1.0 SP1 Release Notes</span></span>


<span data-ttu-id="507b4-104">Чтобы выполнить поиск заметок о выпуске пакета обновления 1 (SP1) для Microsoft User Experience Virtualization (UE-V) 1,0, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="507b4-104">To search Microsoft User Experience Virtualization (UE-V) 1.0 Service Pack 1 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="507b4-105">Перед установкой UE-V вы должны внимательно прочитать эти заметки о выпуске.</span><span class="sxs-lookup"><span data-stu-id="507b4-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="507b4-106">Заметки о выпуске содержат сведения, необходимые для успешной установки виртуализации взаимодействия с пользователем, и содержат дополнительные сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="507b4-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="507b4-107">Если между этими заметками о выпуске и другой документацией UE-V есть различия, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="507b4-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="507b4-108">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="507b4-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="507b4-109">Известные проблемы UE-V</span><span class="sxs-lookup"><span data-stu-id="507b4-109">UE-V known issues</span></span>


<span data-ttu-id="507b4-110">В этом разделе содержатся заметки о выпуске для функции User Experience Virtualization 1,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="507b4-110">This section contains release notes for User Experience Virtualization 1.0 SP1.</span></span>

### <span data-ttu-id="507b4-111">Не удается синхронизировать параметры реестра между приложением App-V и собственными приложениями на одном компьютере</span><span class="sxs-lookup"><span data-stu-id="507b4-111">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="507b4-112">Если на компьютере установлено приложение, доступное как в приложении Application Virtualization (App-V), так и в исходном приложении, установленном с помощью установщика Windows (MSI-файла), параметры, основанные на реестре, не синхронизируются между этими технологиями.</span><span class="sxs-lookup"><span data-stu-id="507b4-112">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application installed with a Windows Installer (.msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="507b4-113">ВРЕМЕННОе решение: чтобы устранить эту проблему, запустите приложение, выбрав одну из двух технологий, но не то, и другое.</span><span class="sxs-lookup"><span data-stu-id="507b4-113">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="windows-8-setting-synchronization-fails-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="507b4-114">Синхронизация параметров Windows 8 завершается сбоем, если сетевая доля выходит за пределы домена пользователя</span><span class="sxs-lookup"><span data-stu-id="507b4-114">Windows 8 setting synchronization fails when network share is outside user’s domain</span></span>

<span data-ttu-id="507b4-115">Если Windows® 8 пытается синхронизировать параметры операционной системы, synchrnization завершает работу со следующим сообщением об ошибке: **"Boost:: FileSystem:: EXISTS": неверное имя пользователя или пароль**.</span><span class="sxs-lookup"><span data-stu-id="507b4-115">When Windows® 8 attempts operating system settings synchronization, the synchrnization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="507b4-116">Эта ошибка может указывать на то, что сетевой общий доступ выходит за пределы домена пользователя.</span><span class="sxs-lookup"><span data-stu-id="507b4-116">This error can indicate that the network share is outside the user’s domain.</span></span> <span data-ttu-id="507b4-117">Чтобы проверить работоспособность журнала событий, откройте **средство просмотра событий** и перейдите в раздел " **приложения и службы**", которые регистрируются в журнале  /  **Microsoft**  /  **виртуализации Microsoft User Experience**  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="507b4-117">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="507b4-118">Общие сетевые ресурсы, используемые для расположений хранилищ параметров UE-V, должны располагаться в том же домене Active Directory, что и пользователь.</span><span class="sxs-lookup"><span data-stu-id="507b4-118">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span>

<span data-ttu-id="507b4-119">ВРЕМЕННОе решение: используйте общие сетевые ресурсы из того же домена Active Directory, что и пользователь.</span><span class="sxs-lookup"><span data-stu-id="507b4-119">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="507b4-120">.</span><span class="sxs-lookup"><span data-stu-id="507b4-120">.</span></span>

### <span data-ttu-id="507b4-121">Перемещение подписей электронной почты в Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="507b4-121">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="507b4-122">UE-V перемещает файлы подписей Outlook 2010 между устройствами.</span><span class="sxs-lookup"><span data-stu-id="507b4-122">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="507b4-123">Однако параметры подписи по умолчанию для новых сообщений, ответов и пересылаемых писем не перемещаются.</span><span class="sxs-lookup"><span data-stu-id="507b4-123">However, the default signature options for new messages and replies/forwards are not roamed.</span></span> <span data-ttu-id="507b4-124">Эти два параметра хранятся в профиле Outlook, который UE-V не перемещается.</span><span class="sxs-lookup"><span data-stu-id="507b4-124">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="507b4-125">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="507b4-125">WORKAROUND: None.</span></span>

### <span data-ttu-id="507b4-126">Параметры синхронизации не синхронизируются с ожидаемым интервалом при работе в режиме медленного канала</span><span class="sxs-lookup"><span data-stu-id="507b4-126">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="507b4-127">В нормальных условиях места хранения параметров должны быть доступны через сетевое подключение Fast Link.</span><span class="sxs-lookup"><span data-stu-id="507b4-127">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="507b4-128">В режиме медленной связи синхронизация будет выполняться периодически на периодической основе.</span><span class="sxs-lookup"><span data-stu-id="507b4-128">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="507b4-129">По умолчанию расписание синхронизации режима медленного соединения задается каждые 360 минут.</span><span class="sxs-lookup"><span data-stu-id="507b4-129">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="507b4-130">ВРЕМЕННОе решение: чтобы изменить частоту фоновой синхронизации на компьютерах в режиме медленной связи, вы можете настроить групповую политику для политики фоновой синхронизации для **автономных файлов**.</span><span class="sxs-lookup"><span data-stu-id="507b4-130">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="507b4-131">Специальные символы не синхронизируются</span><span class="sxs-lookup"><span data-stu-id="507b4-131">Special characters do not synchronize</span></span>

<span data-ttu-id="507b4-132">Некоторые символы, такие как символы денежных единиц, не синхронизируются между компьютерами с Windows 7 и Windows 8, на которых запущен агент UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="507b4-132">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="507b4-133">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="507b4-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="507b4-134">UE-V не поддерживает перемещаемые параметры между 32-битным и 64-разрядными версиями Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="507b4-134">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="507b4-135">Мы рекомендуем установить 32-разрядную версию Microsoft Office для 32-и 64-разрядных операционных систем.</span><span class="sxs-lookup"><span data-stu-id="507b4-135">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="507b4-136">Для выбора нужной версии Microsoft Office щелкните здесь ( [http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623) ).</span><span class="sxs-lookup"><span data-stu-id="507b4-136">To choose the Microsoft Office version that you need, click here ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="507b4-137">UE-V поддерживает перемещаемые параметры между идентичными версиями Office.</span><span class="sxs-lookup"><span data-stu-id="507b4-137">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="507b4-138">Например, 32-разрядные параметры Office будут перемещаться между всеми 32-разрядными экземплярами Office.</span><span class="sxs-lookup"><span data-stu-id="507b4-138">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="507b4-139">UE-V не поддерживает перемещаемые параметры между 32-битным и 64-разрядными версиями Office.</span><span class="sxs-lookup"><span data-stu-id="507b4-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="507b4-140">ВРЕМЕННОе решение: нет</span><span class="sxs-lookup"><span data-stu-id="507b4-140">WORKAROUND: None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="507b4-141">MSI не локализованы</span><span class="sxs-lookup"><span data-stu-id="507b4-141">MSI’s are not localized</span></span>

<span data-ttu-id="507b4-142">UE-V 1,0 SP1 включает локализованную программу установки для агента UE-V и генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="507b4-142">UE-V 1.0 SP1 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="507b4-143">Эти файлы MSI по-прежнему доступны, но пользовательский интерфейс минимизирован и отображается только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="507b4-143">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="507b4-144">Несмотря на то, что файл находится на английском языке, во время установки программа установки устанавливает все поддерживаемые языки.</span><span class="sxs-lookup"><span data-stu-id="507b4-144">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="507b4-145">ВРЕМЕННОе решение: нет</span><span class="sxs-lookup"><span data-stu-id="507b4-145">WORKAROUND: None</span></span>

### <span data-ttu-id="507b4-146">Другие папки в общем доступе с расположением хранилища параметров недоступны в режиме медленного подключения</span><span class="sxs-lookup"><span data-stu-id="507b4-146">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="507b4-147">Общие ресурсы хранилища параметров не должны располагаться в сетевой папке, которая используется для других папок, которые должны быть всегда доступны.</span><span class="sxs-lookup"><span data-stu-id="507b4-147">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="507b4-148">Когда сетевая папка, в которой размещено место хранения параметров, переходит в режим медленного подключения, единственным доступным является папка "Параметры хранилища".</span><span class="sxs-lookup"><span data-stu-id="507b4-148">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="507b4-149">Другие папки в общем доступе недоступны в режиме медленного подключения.</span><span class="sxs-lookup"><span data-stu-id="507b4-149">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="507b4-150">Временное решение: нет</span><span class="sxs-lookup"><span data-stu-id="507b4-150">Workaround: None</span></span>

### <span data-ttu-id="507b4-151">Favicons, связанные с браузером Internet Explorer 9, не перемещаются</span><span class="sxs-lookup"><span data-stu-id="507b4-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="507b4-152">Favicons, связанные с браузером Internet Explorer 9, не перемещаются с помощью виртуализации взаимодействия с пользователем и не отображаются при первом появлении этого списка на новом компьютере.</span><span class="sxs-lookup"><span data-stu-id="507b4-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="507b4-153">ВРЕМЕННОе решение: при использовании закладки и кэшировании в браузере Internet Explorer 9 появится Favicons с соответствующими избранными.</span><span class="sxs-lookup"><span data-stu-id="507b4-153">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="507b4-154">Пути к параметрам файла хранятся в реестре</span><span class="sxs-lookup"><span data-stu-id="507b4-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="507b4-155">Некоторые параметры приложения хранят пути файлов конфигурации и параметров в виде значений в реестре.</span><span class="sxs-lookup"><span data-stu-id="507b4-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="507b4-156">Файлы, на которые указывают ссылки в реестре, должны быть синхронизированы при перемещении параметров между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="507b4-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="507b4-157">ВРЕМЕННОе решение: используйте перенаправление папок или другие технологии, чтобы убедиться в том, что файлы, на которые указывают ссылки, находятся в том же расположении на всех компьютерах, где параметры перемещаются.</span><span class="sxs-lookup"><span data-stu-id="507b4-157">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="507b4-158">Путь к хранилищу с длинными параметрами может вызвать ошибку</span><span class="sxs-lookup"><span data-stu-id="507b4-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="507b4-159">Храните пути к хранилищу параметров как можно короче.</span><span class="sxs-lookup"><span data-stu-id="507b4-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="507b4-160">Длинные пути могут не допускать разрешения и синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="507b4-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="507b4-161">UE-V использует путь к хранилищу параметров как часть расчетного пути для хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="507b4-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="507b4-162">Этот путь вычисляется следующим образом: параметры путь к хранилищу и "settingspackages" + Dir (ИД шаблона) + имя пакета (ИД шаблона).</span><span class="sxs-lookup"><span data-stu-id="507b4-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID).</span></span> <span data-ttu-id="507b4-163">Если размер вычисляемого пути превышает 260 символов, в журнале событий UE-V память пакета завершается сбоем и генерируется следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="507b4-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="507b4-164">Для проверки событий журнала в журнале откройте средство просмотра событий и перейдите в раздел Журналы приложений и служб/Microsoft/пользовательский интерфейс, виртуализация и ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="507b4-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="507b4-165">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="507b4-165">WORKAROUND: None.</span></span>

### <span data-ttu-id="507b4-166">Задержка агента UE-V при выходе или входе</span><span class="sxs-lookup"><span data-stu-id="507b4-166">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="507b4-167">Если при входе в систему или выходе из нее происходит подключение к сети, то, возможно, вы задерживаете, выход из системы или вход в сеть.</span><span class="sxs-lookup"><span data-stu-id="507b4-167">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="507b4-168">Функция автономных файлов может занять до трех минут, чтобы определить текущее состояние сети.</span><span class="sxs-lookup"><span data-stu-id="507b4-168">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="507b4-169">Если вход или завершение работы не выполняется до тех пор, пока автономные файлы не определили, что компьютер подключен к медленной ссылке, пакет параметров UE-V будет отправлен на сервер, а не в локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="507b4-169">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="507b4-170">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="507b4-170">WORKAROUND: None.</span></span>

### <span data-ttu-id="507b4-171">Конфликт параметров при попытке перемещения параметров операционной системы в Windows 8</span><span class="sxs-lookup"><span data-stu-id="507b4-171">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="507b4-172">Если в Windows 8 включена синхронизация учетных записей Майкрософт вместе с UE-V для параметров операционной системы, примененные параметры могут быть несогласованными.</span><span class="sxs-lookup"><span data-stu-id="507b4-172">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="507b4-173">ВРЕМЕННОе решение выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="507b4-173">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="507b4-174">Отключение синхронизации учетной записи Майкрософт, если вы используете UE-V для перемещения параметров операционной системы</span><span class="sxs-lookup"><span data-stu-id="507b4-174">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="507b4-175">Отключение UE-V для параметров операционной системы</span><span class="sxs-lookup"><span data-stu-id="507b4-175">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="507b4-176">Некоторые параметры операционной системы перемещаются только в том случае, если они есть в версиях операционной системы</span><span class="sxs-lookup"><span data-stu-id="507b4-176">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="507b4-177">Параметры операционной системы для экранного диктора и символов денежных единиц, относящихся к национальной настройке, будут перемещаться только в версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="507b4-177">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="507b4-178">Например, для обозначения денежных единиц вы можете перемещаться только с Windows 7 на Windows 7.</span><span class="sxs-lookup"><span data-stu-id="507b4-178">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="507b4-179">ВРЕМЕННОе решение: нет</span><span class="sxs-lookup"><span data-stu-id="507b4-179">WORKAROUND: None</span></span>

 

 





