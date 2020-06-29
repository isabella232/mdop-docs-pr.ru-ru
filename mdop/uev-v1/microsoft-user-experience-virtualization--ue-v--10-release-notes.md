---
title: Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 1.0
description: Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 1.0
author: dansimp
ms.assetid: 920f3fae-e9b5-4b94-beda-32c19d31e94b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9f9942eef7ea84cf7010a0c0173427827a512216
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812488"
---
# <span data-ttu-id="15c3b-103">Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="15c3b-103">Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes</span></span>


<span data-ttu-id="15c3b-104">Чтобы найти заметки о выпуске Microsoft User Experience Virtualization (UE-V), нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="15c3b-104">To search Microsoft User Experience Virtualization (UE-V) release notes, press Ctrl+F.</span></span>

<span data-ttu-id="15c3b-105">Перед установкой UE-V вы должны внимательно прочитать эти заметки о выпуске.</span><span class="sxs-lookup"><span data-stu-id="15c3b-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="15c3b-106">Заметки о выпуске содержат сведения, необходимые для успешной установки виртуализации взаимодействия с пользователем, и содержат дополнительные сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="15c3b-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="15c3b-107">Если между этими заметками о выпуске и другой документацией UE-V есть различия, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="15c3b-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="15c3b-108">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="15c3b-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="15c3b-109">Предоставление отзыва</span><span class="sxs-lookup"><span data-stu-id="15c3b-109">Providing feedback</span></span>


<span data-ttu-id="15c3b-110">Расскажите нам, что вы думаете о нашей документации для MDOP, предоставив нам свой отзыв и комментарии.</span><span class="sxs-lookup"><span data-stu-id="15c3b-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="15c3b-111">Отправьте отзыв о документации в [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="15c3b-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="15c3b-112">Известные проблемы UE-V</span><span class="sxs-lookup"><span data-stu-id="15c3b-112">UE-V known issues</span></span>


<span data-ttu-id="15c3b-113">В этом разделе содержатся заметки о выпуске для виртуализации взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="15c3b-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="15c3b-114">Не удается синхронизировать параметры реестра между приложением App-V и собственными приложениями на одном компьютере</span><span class="sxs-lookup"><span data-stu-id="15c3b-114">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="15c3b-115">Если на компьютере установлено приложение, доступное как из приложения Application Virtualization (App-V), так и с помощью собственного приложения установки (установленного с помощью MSI-файла), параметры, основанные на реестре, не синхронизируются между этими технологиями.</span><span class="sxs-lookup"><span data-stu-id="15c3b-115">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application (installed with an .msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="15c3b-116">ВРЕМЕННОе решение: чтобы устранить эту проблему, запустите приложение, выбрав одну из двух технологий, но не то, и другое.</span><span class="sxs-lookup"><span data-stu-id="15c3b-116">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <span data-ttu-id="15c3b-117">Синхронизация параметров Windows 8 завершается с ошибкой: "Boost:: FileSystem:: EXISTS:" неверное имя пользователя или пароль "</span><span class="sxs-lookup"><span data-stu-id="15c3b-117">Windows 8 setting synchronization fails with error: "boost::filesystem::exists::Incorrect user name or password"</span></span>

<span data-ttu-id="15c3b-118">При синхронизации параметров операционной системы Windows® 8 появляется следующее сообщение об ошибке: **Boost:: FileSystem:: EXISTS:: неверное имя пользователя или пароль**.</span><span class="sxs-lookup"><span data-stu-id="15c3b-118">The Windows® 8 operating system settings synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="15c3b-119">Чтобы проверить работоспособность журнала событий, откройте **средство просмотра событий** и перейдите в раздел " **приложения и службы**", которые регистрируются в журнале  /  **Microsoft**  /  **виртуализации Microsoft User Experience**  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="15c3b-119">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="15c3b-120">Общие сетевые ресурсы, используемые для расположений хранилищ параметров UE-V, должны располагаться в том же домене Active Directory, что и пользователь.</span><span class="sxs-lookup"><span data-stu-id="15c3b-120">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span> <span data-ttu-id="15c3b-121">В противном случае может появиться следующее сообщение об ошибке: "неверное имя пользователя или пароль".</span><span class="sxs-lookup"><span data-stu-id="15c3b-121">Otherwise, the following error might occur: "Incorrect user name or password".</span></span>

<span data-ttu-id="15c3b-122">ВРЕМЕННОе решение: используйте общие сетевые ресурсы из того же домена Active Directory, что и пользователь.</span><span class="sxs-lookup"><span data-stu-id="15c3b-122">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="15c3b-123">.</span><span class="sxs-lookup"><span data-stu-id="15c3b-123">.</span></span>

### <span data-ttu-id="15c3b-124">Перемещение подписей электронной почты в Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="15c3b-124">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="15c3b-125">UE-V перемещает файлы подписей Outlook 2010 между устройствами.</span><span class="sxs-lookup"><span data-stu-id="15c3b-125">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="15c3b-126">Однако параметры подписей по умолчанию для новых сообщений, ответов и пересылаемых задаются не будут.</span><span class="sxs-lookup"><span data-stu-id="15c3b-126">However, the default signature options for new messages and replies/forwards are not.</span></span><span data-ttu-id="15c3b-127">Эти два параметра хранятся в профиле Outlook, который UE-Vdoes не роуминг.</span><span class="sxs-lookup"><span data-stu-id="15c3b-127"> These two settings are stored in the Outlook profile, which UE-Vdoes not roam.</span></span>

<span data-ttu-id="15c3b-128">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="15c3b-128">WORKAROUND: None.</span></span>

### <span data-ttu-id="15c3b-129">Параметры синхронизации не синхронизируются с ожидаемым интервалом при работе в режиме медленного канала</span><span class="sxs-lookup"><span data-stu-id="15c3b-129">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="15c3b-130">В нормальных условиях места хранения параметров должны быть доступны через сетевое подключение Fast Link.</span><span class="sxs-lookup"><span data-stu-id="15c3b-130">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="15c3b-131">В режиме медленной связи синхронизация будет выполняться периодически на периодической основе.</span><span class="sxs-lookup"><span data-stu-id="15c3b-131">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="15c3b-132">По умолчанию расписание синхронизации режима медленного соединения задается каждые 360 минут.</span><span class="sxs-lookup"><span data-stu-id="15c3b-132">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="15c3b-133">ВРЕМЕННОе решение: чтобы изменить частоту фоновой синхронизации на компьютерах в режиме медленной связи, вы можете настроить групповую политику для политики фоновой синхронизации для **автономных файлов**.</span><span class="sxs-lookup"><span data-stu-id="15c3b-133">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="15c3b-134">Специальные символы не синхронизируются</span><span class="sxs-lookup"><span data-stu-id="15c3b-134">Special characters do not synchronize</span></span>

<span data-ttu-id="15c3b-135">Некоторые символы, такие как символы денежных единиц, не синхронизируются между компьютерами с Windows 7 и Windows 8, на которых запущен агент UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="15c3b-135">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="15c3b-136">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="15c3b-136">WORKAROUND: None.</span></span>

### <span data-ttu-id="15c3b-137">UE-V не поддерживает перемещаемые параметры между 32-битным и 64-разрядными версиями Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="15c3b-137">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="15c3b-138">Мы рекомендуем установить 32-разрядную версию Microsoft Office для 32-и 64-разрядных операционных систем.</span><span class="sxs-lookup"><span data-stu-id="15c3b-138">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="15c3b-139">Чтобы выбрать нужную вам версию Microsoft Office, щелкните здесь.</span><span class="sxs-lookup"><span data-stu-id="15c3b-139">To choose the Microsoft Office version that you need, click here.</span></span> <span data-ttu-id="15c3b-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span><span class="sxs-lookup"><span data-stu-id="15c3b-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="15c3b-141">UE-V поддерживает перемещаемые параметры между идентичными версиями Office.</span><span class="sxs-lookup"><span data-stu-id="15c3b-141">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="15c3b-142">Например, 32-разрядные параметры Office будут перемещаться между всеми 32-разрядными экземплярами Office.</span><span class="sxs-lookup"><span data-stu-id="15c3b-142">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="15c3b-143">UE-V не поддерживает перемещаемые параметры между 32-битным и 64-разрядными версиями Office.</span><span class="sxs-lookup"><span data-stu-id="15c3b-143">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="15c3b-144">ВРЕМЕННОе решение: нет</span><span class="sxs-lookup"><span data-stu-id="15c3b-144">WORKAROUND: None</span></span>

### <span data-ttu-id="15c3b-145">Другие папки в общем доступе с расположением хранилища параметров недоступны в режиме медленного подключения</span><span class="sxs-lookup"><span data-stu-id="15c3b-145">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="15c3b-146">Общие ресурсы хранилища параметров не должны располагаться в сетевой папке, которая используется для других папок, которые должны быть всегда доступны.</span><span class="sxs-lookup"><span data-stu-id="15c3b-146">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="15c3b-147">Когда сетевая папка, в которой размещено место хранения параметров, переходит в режим медленного подключения, единственным доступным является папка "Параметры хранилища".</span><span class="sxs-lookup"><span data-stu-id="15c3b-147">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="15c3b-148">Другие папки в общем доступе недоступны в режиме медленного подключения.</span><span class="sxs-lookup"><span data-stu-id="15c3b-148">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="15c3b-149">Временное решение: нет</span><span class="sxs-lookup"><span data-stu-id="15c3b-149">Workaround: None</span></span>

### <span data-ttu-id="15c3b-150">Favicons, связанные с браузером Internet Explorer 9, не перемещаются</span><span class="sxs-lookup"><span data-stu-id="15c3b-150">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="15c3b-151">Favicons, связанные с браузером Internet Explorer 9, не перемещаются с помощью виртуализации взаимодействия с пользователем и не отображаются при первом появлении этого списка на новом компьютере.</span><span class="sxs-lookup"><span data-stu-id="15c3b-151">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="15c3b-152">ВРЕМЕННОе решение: при использовании закладки и кэшировании в браузере Internet Explorer 9 появится Favicons с соответствующими избранными.</span><span class="sxs-lookup"><span data-stu-id="15c3b-152">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="15c3b-153">Пути к параметрам файла хранятся в реестре</span><span class="sxs-lookup"><span data-stu-id="15c3b-153">File settings paths are stored in registry</span></span>

<span data-ttu-id="15c3b-154">Некоторые параметры приложения хранят пути файлов конфигурации и параметров в виде значений в реестре.</span><span class="sxs-lookup"><span data-stu-id="15c3b-154">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="15c3b-155">Файлы, на которые указывают ссылки в реестре, должны быть синхронизированы при перемещении параметров между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="15c3b-155">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="15c3b-156">ВРЕМЕННОе решение: используйте перенаправление папок или другие технологии, чтобы убедиться в том, что файлы, на которые указывают ссылки, находятся в том же расположении на всех компьютерах, где параметры перемещаются.</span><span class="sxs-lookup"><span data-stu-id="15c3b-156">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="15c3b-157">Пути, длина которых превышает 260 символов, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="15c3b-157">Paths longer than 260 characters are not supported</span></span>

<span data-ttu-id="15c3b-158">Пути хранилища параметров, длина которых превышает 260 символов, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="15c3b-158">Settings storage paths that are longer than 260 characters are not supported.</span></span> <span data-ttu-id="15c3b-159">При копировании пакетов параметров UE-V в пути к хранилищу параметров, длина которых превышает 260 символов, произойдет сбой и будет создано следующее сообщение об исключении в журнале событий UE-V: **\ [Boost:: FileSystem:: Copy \ _File: системе не удается найти указанный путь \ \]**.</span><span class="sxs-lookup"><span data-stu-id="15c3b-159">Copying the UE-V settings packages to settings storage paths that are longer than 260 characters will fail and generate the following exception message in the UE-V operational event log: **\[boost::filesystem::copy\_file: The system cannot find the path specified\]**.</span></span> <span data-ttu-id="15c3b-160">Чтобы проверить работоспособность журнала событий, откройте **средство просмотра событий** и перейдите в раздел " **приложения и службы**", которые регистрируются в журнале  /  **Microsoft**  /  **виртуализации Microsoft User Experience**  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="15c3b-160">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span>

<span data-ttu-id="15c3b-161">Пути к параметрам файла, длина которых превышает 260 символов, в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="15c3b-161">File settings paths that are longer than 260 characters are not currently supported.</span></span> <span data-ttu-id="15c3b-162">Параметры файлов, на которые указывают ссылки в шаблонах расположений параметров UE-V, не могут находиться в пути к каталогу, длина которого превышает 260 знаков.</span><span class="sxs-lookup"><span data-stu-id="15c3b-162">File settings that are referenced in UE-V settings location templates cannot be located in a directory path that is longer than 260 characters.</span></span>

<span data-ttu-id="15c3b-163">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="15c3b-163">WORKAROUND: None.</span></span>

### <span data-ttu-id="15c3b-164">Задержка агента UE-V при выходе или входе</span><span class="sxs-lookup"><span data-stu-id="15c3b-164">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="15c3b-165">Если при входе в систему или выходе из нее происходит подключение к сети, то, возможно, вы задерживаете, выход из системы или вход в сеть.</span><span class="sxs-lookup"><span data-stu-id="15c3b-165">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="15c3b-166">Функция автономных файлов может занять до трех минут, чтобы определить текущее состояние сети.</span><span class="sxs-lookup"><span data-stu-id="15c3b-166">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="15c3b-167">Если вход или завершение работы не выполняется до тех пор, пока автономные файлы не определили, что компьютер подключен к медленной ссылке, пакет параметров UE-V будет отправлен на сервер, а не в локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="15c3b-167">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="15c3b-168">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="15c3b-168">WORKAROUND: None.</span></span>

### <span data-ttu-id="15c3b-169">Конфликт параметров при попытке перемещения параметров операционной системы в Windows 8</span><span class="sxs-lookup"><span data-stu-id="15c3b-169">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="15c3b-170">Если в Windows 8 включена синхронизация учетных записей Майкрософт вместе с UE-V для параметров операционной системы, примененные параметры могут быть несогласованными.</span><span class="sxs-lookup"><span data-stu-id="15c3b-170">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="15c3b-171">ВРЕМЕННОе решение выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="15c3b-171">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="15c3b-172">Отключение синхронизации учетной записи Майкрософт, если вы используете UE-V для перемещения параметров операционной системы</span><span class="sxs-lookup"><span data-stu-id="15c3b-172">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="15c3b-173">Отключение UE-V для параметров операционной системы</span><span class="sxs-lookup"><span data-stu-id="15c3b-173">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="15c3b-174">Некоторые параметры операционной системы перемещаются только в том случае, если они есть в версиях операционной системы</span><span class="sxs-lookup"><span data-stu-id="15c3b-174">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="15c3b-175">Параметры операционной системы для экранного диктора и символов денежных единиц, относящихся к национальной настройке, будут перемещаться только в версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="15c3b-175">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="15c3b-176">Например, для обозначения денежных единиц вы можете перемещаться только с Windows 7 на Windows 7.</span><span class="sxs-lookup"><span data-stu-id="15c3b-176">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="15c3b-177">ВРЕМЕННОе решение: нет</span><span class="sxs-lookup"><span data-stu-id="15c3b-177">WORKAROUND: None</span></span>

### <span data-ttu-id="15c3b-178">Закладки Internet Explorer не отображаются в обозревателе Internet Explorer SmartBar</span><span class="sxs-lookup"><span data-stu-id="15c3b-178">Internet Explorer bookmarks do not appear in the Internet Explorer smartbar</span></span>

<span data-ttu-id="15c3b-179">Если закладки Internet Explorer перемещаются с одного компьютера на другой, то индекс на втором компьютере не может быть обновлен, поэтому при вводе текста в адресную строку избранное не будет отображаться как возможный результат поиска на компьютере 2.</span><span class="sxs-lookup"><span data-stu-id="15c3b-179">When Internet Explorer bookmarks roam from one computer to another computer, the index on the second computer cannot update, so when typing in the address bar, the favorite will not appear as a possible search result on computer 2.</span></span>

<span data-ttu-id="15c3b-180">ВРЕМЕННОе решение: нет</span><span class="sxs-lookup"><span data-stu-id="15c3b-180">WORKAROUND: None</span></span>

 

 





