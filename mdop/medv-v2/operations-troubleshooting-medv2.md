---
title: Устранение неполадок в операциях
description: Устранение неполадок в операциях
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812741"
---
# <span data-ttu-id="16739-103">Устранение неполадок в операциях</span><span class="sxs-lookup"><span data-stu-id="16739-103">Operations Troubleshooting</span></span>


<span data-ttu-id="16739-104">Этот раздел содержит сведения, которые можно использовать для устранения общих проблем, связанных с рабочим столом в Microsoft Enterprise Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="16739-104">This topic includes information that you can use to help troubleshoot general operational issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="16739-105">Устранение неполадок, связанных с работой в MED-V</span><span class="sxs-lookup"><span data-stu-id="16739-105">Troubleshooting Issues in MED-V Operations</span></span>


<span data-ttu-id="16739-106">Ниже перечислены некоторые проблемы, с которыми пользователи могут столкнуться при использовании MED-V и решений для устранения этих проблем.</span><span class="sxs-lookup"><span data-stu-id="16739-106">The following are some issues end users might encounter when they run MED-V and solutions to help troubleshoot these issues:</span></span>

<span data-ttu-id="16739-107">**Не удается перенаправление документации**.</span><span class="sxs-lookup"><span data-stu-id="16739-107">**Documentation Redirection Fails**.</span></span> <span data-ttu-id="16739-108">Как правило, эта проблема возникает, если папка Мои документы конечного пользователя указывает на расположение в сети.</span><span class="sxs-lookup"><span data-stu-id="16739-108">This issue typically occurs when an end user’s My Documents folder points to a network location.</span></span> <span data-ttu-id="16739-109">Windows не поддерживает создание общего доступа из другой общей папки.</span><span class="sxs-lookup"><span data-stu-id="16739-109">Windows does not support creating a share from another shared folder.</span></span> <span data-ttu-id="16739-110">Когда диск или папка перенаправляется на гость, RDP\\Windows Virtual PC создает для нее общий доступ.</span><span class="sxs-lookup"><span data-stu-id="16739-110">When a drive or folder is redirected to the guest, RDP\\Windows Virtual PC creates a share for that folder.</span></span> <span data-ttu-id="16739-111">Таким образом, если папка Мои документы на узле уже указывает на общий доступ, RDP\\Windows Virtual PC не может создать общий доступ к общему доступу.</span><span class="sxs-lookup"><span data-stu-id="16739-111">Therefore, if the My Documents folder on the host is already pointing to a share, RDP\\Windows Virtual PC cannot create a share of a share.</span></span>

<span data-ttu-id="16739-112">Другая возможная причина этой проблемы заключается в том, что учетные данные, необходимые для подключения к сетевому ресурсу, могут отличаться от учетных данных пользователя домена.</span><span class="sxs-lookup"><span data-stu-id="16739-112">Another possible cause of this issue is that the credentials that are required to connect to the network resource might differ from the user’s domain credentials.</span></span> <span data-ttu-id="16739-113">MED-V может обнаружить, что документы перенаправлены на узел, отправить эту информацию на гость и попытаться восстановить подключение к сетевому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="16739-113">MED-V might be detecting that documents are redirected on the host, send that information to the guest, and then try to reconnect the network resource.</span></span> <span data-ttu-id="16739-114">Если учетная запись пользователя не проходит проверку подлинности, при попытке выполнить проверку подлинности в MED-V может возникнуть ошибка.</span><span class="sxs-lookup"><span data-stu-id="16739-114">If the user’s credentials do not authenticate, MED-V might stop trying to authenticate.</span></span>

**<span data-ttu-id="16739-115">Решение</span><span class="sxs-lookup"><span data-stu-id="16739-115">Solution</span></span>**

<span data-ttu-id="16739-116">Чтобы устранить эту проблему, попробуйте выполнить одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="16739-116">Try one of the following to resolve this issue:</span></span>

-   <span data-ttu-id="16739-117">Настройте корневой каталог пользователя в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="16739-117">Set the user’s root directory inside Active Directory.</span></span> <span data-ttu-id="16739-118">После этого гость и узел должны подключаться к тому же сетевому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="16739-118">The guest and host should then connect to the same network resource.</span></span>

-   <span data-ttu-id="16739-119">Вместо того чтобы перенаправлять папку "Мои документы" в путь UNC, сопоставьте ей букву диска (на узле сопоставьте диск, который указывает на ресурс сети).</span><span class="sxs-lookup"><span data-stu-id="16739-119">Instead of redirecting the My Documents folder to a UNC path, map it to a drive letter (on the host, map a drive that points to the network resource).</span></span> <span data-ttu-id="16739-120">После этого в папке Мои документы можно настроить использование буквы диска вместо пути в формате UNC.</span><span class="sxs-lookup"><span data-stu-id="16739-120">The My Documents folder can then be set to use the drive letter instead of the UNC path.</span></span> <span data-ttu-id="16739-121">Гость перейдет к тому же подключенному диску, как и предполагалось.</span><span class="sxs-lookup"><span data-stu-id="16739-121">The guest will then redirect to that same mapped drive as expected.</span></span>

-   <span data-ttu-id="16739-122">Создайте в гостевой системе сценарий, который перенаправляет папку "Мои документы" сетевому ресурсу, и при необходимости предоставляет дополнительные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="16739-122">Create a startup script in the guest that redirects the My Documents folder to the network resource and provides additional credentials as needed.</span></span>

<span data-ttu-id="16739-123">**Перенаправление URL-адреса не выполняется**.</span><span class="sxs-lookup"><span data-stu-id="16739-123">**URL Redirection Fails**.</span></span> <span data-ttu-id="16739-124">URL-адрес, указанный для переадресации с узла на гость, не перенаправляется надлежащим образом или возвращает сообщение об ошибке, указывающее на то, что веб-сайт не существует.</span><span class="sxs-lookup"><span data-stu-id="16739-124">A URL that you have specified for redirection from the host to the guest is not redirecting as intended or is returning an error message that indicates that the website does not exist.</span></span>

**<span data-ttu-id="16739-125">Решение</span><span class="sxs-lookup"><span data-stu-id="16739-125">Solution</span></span>**

<span data-ttu-id="16739-126">Эта ошибка может возникать, если в сведениях о переадресации URL-адреса есть ошибки или неправильное использование знаков, например звездочки (\ \*).</span><span class="sxs-lookup"><span data-stu-id="16739-126">This error can occur when there is a misspelling or incorrect use of characters, such as asterisk (\*), in the URL redirection information.</span></span> <span data-ttu-id="16739-127">Проверьте значение реестра для перенаправления URL-адреса и исправьте ошибки.</span><span class="sxs-lookup"><span data-stu-id="16739-127">Check the registry value for URL redirection and correct any mistakes.</span></span>

<span data-ttu-id="16739-128">Раздел реестра называется `RedirectUrls` и обычно находится по адресу:</span><span class="sxs-lookup"><span data-stu-id="16739-128">The registry key is called `RedirectUrls` and is typically located at:</span></span>

<span data-ttu-id="16739-129">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="16739-129">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="16739-130">**Значок на панели задач**.</span><span class="sxs-lookup"><span data-stu-id="16739-130">**Icon in Taskbar Misleading**.</span></span> <span data-ttu-id="16739-131">По умолчанию, значок, который отображается на панели задач конечного пользователя для опубликованных приложений и перенаправленные URL-адреса, — это значок для Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="16739-131">By default, the icon that appears in an end user’s taskbar for published applications and redirected URLs is the icon for Windows Virtual PC.</span></span> <span data-ttu-id="16739-132">Если конечный пользователь не знает это поведение по умолчанию, он может стать запутанным при просмотре панели задач, чтобы найти их приложение.</span><span class="sxs-lookup"><span data-stu-id="16739-132">If an end user is not aware of this default behavior, they can become confused when looking at the taskbar to locate their application.</span></span>

**<span data-ttu-id="16739-133">Решение</span><span class="sxs-lookup"><span data-stu-id="16739-133">Solution</span></span>**

<span data-ttu-id="16739-134">Единственный способ избежать этого поведения по умолчанию — изменить параметры пользователя для свойств панели задач, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="16739-134">The only way to avoid this default behavior is to change the user settings for the taskbar properties as follows:</span></span>

1.  <span data-ttu-id="16739-135">Щелкните панель задач правой кнопкой мыши и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="16739-135">Right-click the taskbar and then click **Properties**.</span></span>

2.  <span data-ttu-id="16739-136">На **панели задач и** в диалоговом окне Свойства: меню "Пуск" щелкните вкладку на **панели задач** .</span><span class="sxs-lookup"><span data-stu-id="16739-136">In the **Taskbar and Start Menu Properties** dialog box, click the **Taskbar** tab.</span></span>

3.  <span data-ttu-id="16739-137">В раскрывающемся списке **кнопок на панели задач** выберите параметр **не объединять**.</span><span class="sxs-lookup"><span data-stu-id="16739-137">In the drop-down bar for the **Taskbar buttons** box, select **Never combine**.</span></span>

4.  <span data-ttu-id="16739-138">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="16739-138">Click **OK**.</span></span>

<span data-ttu-id="16739-139">Отображаются ожидаемые значки опубликованных приложений и перенаправленные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="16739-139">The expected icons for published applications and redirected URLs are displayed.</span></span>

<span data-ttu-id="16739-140">**Предупреждение, выданное при попытке входа в систему с помощью второй учетной записи пользователя или виртуальной машины**.</span><span class="sxs-lookup"><span data-stu-id="16739-140">**Warning Issued if Second User Attempts Log on or if Virtual Machine is in Use**.</span></span> <span data-ttu-id="16739-141">Предупреждающее сообщение выдается, когда второй пользователь входит в рабочую область MED-V, когда первый пользователь по-прежнему работает под управлением MED-V.</span><span class="sxs-lookup"><span data-stu-id="16739-141">A warning message is issued when a second user logs on to a MED-V workspace while a first user is still running MED-V.</span></span> <span data-ttu-id="16739-142">Предупреждение также выводится, если при использовании виртуальной машины была запущена система MED-V, например, если виртуальная машина была запущена с помощью Windows Virtual PC в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="16739-142">The warning is also issued if MED-V is started while the virtual machine is being used, for example, if the virtual machine was started through Windows Virtual PC on the **Start** menu.</span></span> <span data-ttu-id="16739-143">Когда пользователь принимает предупреждающее сообщение, MED-V завершает работу.</span><span class="sxs-lookup"><span data-stu-id="16739-143">When the end user accepts the warning message, MED-V shuts down.</span></span>

**<span data-ttu-id="16739-144">Решение</span><span class="sxs-lookup"><span data-stu-id="16739-144">Solution</span></span>**

<span data-ttu-id="16739-145">Конечный пользователь должен проверить, что все остальные пользователи вошли в систему, прежде чем пытаться войти в систему.</span><span class="sxs-lookup"><span data-stu-id="16739-145">An end user must verify that all other users are logged off MED-V before they try to log on.</span></span> <span data-ttu-id="16739-146">Это гарантирует, что другие экземпляры MED-V не запущены, и что Virtual PC не отвечает за контроль виртуальных машин в Windows.</span><span class="sxs-lookup"><span data-stu-id="16739-146">This ensures that no other instance of MED-V is running and that Windows Virtual PC is not in control of the virtual machine.</span></span>

<span data-ttu-id="16739-147">**Звуковой сигнал, который слышен при первом запуске программы установки**.</span><span class="sxs-lookup"><span data-stu-id="16739-147">**Beeps Heard During First Time Setup**.</span></span> <span data-ttu-id="16739-148">Иногда звуковые сигналы слышны, а MED-V запускается при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="16739-148">Occasionally, beeps are heard while MED-V is running first time setup.</span></span> <span data-ttu-id="16739-149">Это может привести к путанице с конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="16739-149">This can be confusing to an end user.</span></span> <span data-ttu-id="16739-150">Звуковые сигналы исходят с виртуальной машины при выполнении определенных действий, например при завершении работы.</span><span class="sxs-lookup"><span data-stu-id="16739-150">The beeps are originating from the virtual machine when it performs certain actions, such as shutting down.</span></span>

**<span data-ttu-id="16739-151">Решение</span><span class="sxs-lookup"><span data-stu-id="16739-151">Solution</span></span>**

<span data-ttu-id="16739-152">Вы можете остановить службу звукового сигнала, указав команду "net stop Beep" в начале каждой последовательности запуска виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="16739-152">You can stop the beep service by specifying the "net stop beep" command at the beginning of each virtual machine start sequence.</span></span> <span data-ttu-id="16739-153">Кроме того, вы можете отключить звуковую службу, указав команду "SC config Beep Start = Disabled".</span><span class="sxs-lookup"><span data-stu-id="16739-153">Or you can disable the beep service by specifying the “sc config beep start= disabled" command.</span></span> <span data-ttu-id="16739-154">Эти команды можно задать перед запечатыванием изображения или в составе программы Sysprep.</span><span class="sxs-lookup"><span data-stu-id="16739-154">You can specify these commands either before you seal the image or as part of Sysprep.</span></span>

<span data-ttu-id="16739-155">**Несколько сетевых подключений, созданных для рабочих областей MED-V в режиме моста**.</span><span class="sxs-lookup"><span data-stu-id="16739-155">**Multiple Network Connections Created for MED-V Workspaces in BRIDGED Mode**.</span></span> <span data-ttu-id="16739-156">Если при первом запуске программы установки создается рабочая область MED-V, настроенная для режима NAT, она создает только одно сетевое подключение в Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="16739-156">If first time setup is creating a MED-V workspace that is configured for NAT mode, it only creates a single network connection in Windows Virtual PC.</span></span> <span data-ttu-id="16739-157">Тем не менее, если при первой настройке будет создана Рабочая область MED-V, настроенная для режима моста, создается отдельное сетевое подключение для каждого сетевого адаптера, установленного на компьютере, так как MED-V не может определить, какой именно сетевой адаптер является активным.</span><span class="sxs-lookup"><span data-stu-id="16739-157">However, if first time setup is creating a MED-V workspace that is configured for BRIDGED mode, it creates a separate network connection for each network adapter that is installed in the computer, because MED-V cannot determine which network adapter is active.</span></span> <span data-ttu-id="16739-158">Кроме того, это гарантирует, что для проводных и беспроводных подключений для перемещаемых пользователей всегда будет использоваться сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="16739-158">This also ensures that roaming users always have a network adapter available for wired and wireless connections.</span></span>

**<span data-ttu-id="16739-159">Решение</span><span class="sxs-lookup"><span data-stu-id="16739-159">Solution</span></span>**

<span data-ttu-id="16739-160">Нет.</span><span class="sxs-lookup"><span data-stu-id="16739-160">None.</span></span>

<span data-ttu-id="16739-161">**Приложение MED-V не отвечает на запросы слишком долго при закрытии**.</span><span class="sxs-lookup"><span data-stu-id="16739-161">**MED-V Application is Unresponsive for Too Long when Closing**.</span></span> <span data-ttu-id="16739-162">В некоторых случаях приложение MED-V перестает отвечать на запросы при попытке закрыть его.</span><span class="sxs-lookup"><span data-stu-id="16739-162">In some instances, a MED-V application stops responding when it is trying to close.</span></span>

**<span data-ttu-id="16739-163">Решение</span><span class="sxs-lookup"><span data-stu-id="16739-163">Solution</span></span>**

<span data-ttu-id="16739-164">Вы можете указать продолжительность времени, в течение которого MED-V ждет закрытия приложений, не отвечающих на запросы, установив раздел реестра WaitToKillAppTimeout на гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="16739-164">You can specify the length of time that MED-V waits to close unresponsive applications by setting the WaitToKillAppTimeout registry key in the guest virtual machine.</span></span> <span data-ttu-id="16739-165">Дополнительные сведения о том, [как увеличить время завершения работы программы, чтобы правильно завершить процесс в Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) ( https://go.microsoft.com/fwlink/?LinkId=206819) .</span><span class="sxs-lookup"><span data-stu-id="16739-165">For more information, see [How To Increase Shutdown Time So That Processes Can Quit Properly in Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) (https://go.microsoft.com/fwlink/?LinkId=206819).</span></span>

<span data-ttu-id="16739-166">**Переименование опубликованного ярлыка приложения на гостевой виртуальной машине не изменяет опубликованное имя на узле**.</span><span class="sxs-lookup"><span data-stu-id="16739-166">**Renaming a Published Application Shortcut in the Guest Virtual Machine does not Change the Published Name in the Host**.</span></span> <span data-ttu-id="16739-167">При публикации приложения с помощью создания ярлыка и переименования ярлыка на гостевой виртуальной машине имя исходного приложения сохраняется в меню " **Пуск** " узла.</span><span class="sxs-lookup"><span data-stu-id="16739-167">When you publish an application by creating a shortcut and then rename the shortcut in the guest virtual machine, the original application name remains in the host **Start** menu.</span></span> <span data-ttu-id="16739-168">Программа продолжает работать должным образом, но программа всегда сохранит исходное имя.</span><span class="sxs-lookup"><span data-stu-id="16739-168">The program continues to run as expected, however the program will always retain the original name.</span></span>

**<span data-ttu-id="16739-169">Решение</span><span class="sxs-lookup"><span data-stu-id="16739-169">Solution</span></span>**

<span data-ttu-id="16739-170">Нет.</span><span class="sxs-lookup"><span data-stu-id="16739-170">None.</span></span> <span data-ttu-id="16739-171">Это известное поведение Virtual PC для Windows.</span><span class="sxs-lookup"><span data-stu-id="16739-171">This is a known behavior of Windows Virtual PC.</span></span>

<span data-ttu-id="16739-172">**При перемещении ярлыка на гостевой виртуальной машине это расположение не обновляется в меню "Пуск" главного компьютера**.</span><span class="sxs-lookup"><span data-stu-id="16739-172">**Moving a Shortcut in the Guest Virtual Machine does not Update the Location on the Host Computer Start Menu**.</span></span> <span data-ttu-id="16739-173">Сочетания клавиш для работы с приложением MED-V, опубликованные в **главном меню компьютера** , находятся в реестре.</span><span class="sxs-lookup"><span data-stu-id="16739-173">MED-V application shortcuts that are published to the host computer **Start** menu are cataloged in the registry.</span></span> <span data-ttu-id="16739-174">Если переместить ярлык приложения во вложенную папку, реестр не будет обновляться, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="16739-174">If you move an application shortcut into a subfolder, the registry is not updated to reflect the change.</span></span>

**<span data-ttu-id="16739-175">Решение</span><span class="sxs-lookup"><span data-stu-id="16739-175">Solution</span></span>**

<span data-ttu-id="16739-176">Чтобы изменить расположение сочетания клавиш для приложения MED-V, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="16739-176">Follow these steps to change the location of a MED-V application shortcut:</span></span>

1.  <span data-ttu-id="16739-177">После запуска MED-V откройте проводник Windows на гостевой виртуальной машине MED-V.</span><span class="sxs-lookup"><span data-stu-id="16739-177">When MED-V is running, open up Windows Explorer on the MED-V guest virtual machine.</span></span>

2.  <span data-ttu-id="16739-178">Перейдите к каталогу "%ALLUSERSPROFILE%\\Start Menu\\Programs".</span><span class="sxs-lookup"><span data-stu-id="16739-178">Browse to the "%ALLUSERSPROFILE%\\Start Menu\\Programs" directory.</span></span>

3.  <span data-ttu-id="16739-179">Перемещение ярлыков приложения из папок StartMenu или программы.</span><span class="sxs-lookup"><span data-stu-id="16739-179">Move the application shortcuts out of the startmenu or programs folders.</span></span>

4.  <span data-ttu-id="16739-180">После около 30 секунд убедитесь, что ярлыки удаляются из меню **Пуск** главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="16739-180">After about 30 seconds, validate that the shortcuts are removed from the host computer **Start** menu.</span></span>

5.  <span data-ttu-id="16739-181">Переместите ярлыки приложений обратно в новые папки программы в каталоге Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="16739-181">Move the application shortcuts back in to the new program folders under the Start Menu\\Programs directory.</span></span>

6.  <span data-ttu-id="16739-182">После примерно 30 секунд убедитесь в том, что ярлыки обновлены в главном **меню главного** компьютера.</span><span class="sxs-lookup"><span data-stu-id="16739-182">After about 30 seconds, validate that the shortcuts are updated in the host computer **Start** Menu.</span></span>

<span data-ttu-id="16739-183">**Опубликованные приложения могут**исключаться из периода простоя.</span><span class="sxs-lookup"><span data-stu-id="16739-183">**Published Applications can Time Out after Sitting Idle**.</span></span> <span data-ttu-id="16739-184">В некоторых случаях опубликованные приложения будут иметь время ожидания, если они не простаивают в течение некоторого времени.</span><span class="sxs-lookup"><span data-stu-id="16739-184">In some cases, published applications will time out if they have sat idle for some time.</span></span> <span data-ttu-id="16739-185">Это происходит только в том случае, если включена безопасность IPsec и в режиме NAT настроена Рабочая область MED-V.</span><span class="sxs-lookup"><span data-stu-id="16739-185">This situation only occurs if IPsec is enabled and the MED-V workspace is configured for NAT mode.</span></span> <span data-ttu-id="16739-186">Такая ситуация не возникает при работе в режиме моста.</span><span class="sxs-lookup"><span data-stu-id="16739-186">This situation does not occur if running in BRIDGED mode.</span></span>

**<span data-ttu-id="16739-187">Решение</span><span class="sxs-lookup"><span data-stu-id="16739-187">Solution</span></span>**

<span data-ttu-id="16739-188">Отключите IPsec при запуске рабочей области MED-V в режиме NAT.</span><span class="sxs-lookup"><span data-stu-id="16739-188">Disable IPsec when you are running the MED-V workspace in NAT mode.</span></span>

<span data-ttu-id="16739-189">**Закрепление опубликованного приложения на панели задач обходит MED-V**.</span><span class="sxs-lookup"><span data-stu-id="16739-189">**Pinning a Published Application to the Taskbar Bypasses MED-V**.</span></span> <span data-ttu-id="16739-190">Если пользователь зафиксирует опубликованное приложение на панели задач, а затем закроет приложение, то MED-V обходится при следующем открытии приложения из значка на панели задач.</span><span class="sxs-lookup"><span data-stu-id="16739-190">If an end user pins a published application to the taskbar and then closes the application, MED-V is bypassed the next time that the application is opened from the taskbar icon.</span></span> <span data-ttu-id="16739-191">Вместо этого приложение откроется прямо в окне VMSAL.</span><span class="sxs-lookup"><span data-stu-id="16739-191">Instead, the application opens directly in a VMSAL window.</span></span>

**<span data-ttu-id="16739-192">Решение</span><span class="sxs-lookup"><span data-stu-id="16739-192">Solution</span></span>**

<span data-ttu-id="16739-193">Не закрепите приложения, опубликованные в MED-V, на панели задач.</span><span class="sxs-lookup"><span data-stu-id="16739-193">Do not pin the applications published in MED-V to the taskbar.</span></span>

## <span data-ttu-id="16739-194">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="16739-194">Related topics</span></span>


[<span data-ttu-id="16739-195">Рекомендации по обеспечению безопасности операций MED-V</span><span class="sxs-lookup"><span data-stu-id="16739-195">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)

[<span data-ttu-id="16739-196">Устранение неполадок при развертывании</span><span class="sxs-lookup"><span data-stu-id="16739-196">Deployment Troubleshooting</span></span>](deployment-troubleshooting.md)

 

 





