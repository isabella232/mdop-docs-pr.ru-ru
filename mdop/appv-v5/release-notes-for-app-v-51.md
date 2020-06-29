---
title: Заметки о выпуске App-V 5.1
description: Заметки о выпуске App-V 5.1
author: dansimp
ms.assetid: 62c5be3b-0a46-4512-93ed-97c23184f343
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2016
ms.openlocfilehash: 7437a16bc10b21bb15b0f8307c2711177e78cb72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813309"
---
# <span data-ttu-id="39a3e-103">Заметки о выпуске App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="39a3e-103">Release Notes for App-V 5.1</span></span>


<span data-ttu-id="39a3e-104">Ниже описаны известные проблемы, возникающие в Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="39a3e-104">The following are known issues in Microsoft Application Virtualization (App-V) 5.1.</span></span>

## <span data-ttu-id="39a3e-105">Произошла ошибка во время обновления публикации между сервером управления App-V 5,0 SP3 и клиентом App-V 5,1 в Windows 10</span><span class="sxs-lookup"><span data-stu-id="39a3e-105">Error occurs during publishing refresh between App-V 5.0 SP3 Management Server and App-V 5.1 Client on Windows 10</span></span>


<span data-ttu-id="39a3e-106">При обновлении публикации при синхронизации пакетов с сервера управления App-V 5,0 SP3 до клиента App-V 5,1 в Windows 10 возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="39a3e-106">An error is generated during publishing refresh when synchronizing packages from the App-V 5.0 SP3 management server to an App-V 5.1 client on Windows 10 .</span></span> <span data-ttu-id="39a3e-107">Эта ошибка возникает, потому что сервер App-V 5,0 SP3 не понимает операционную систему Windows 10, указанную в URL-адресе публикации.</span><span class="sxs-lookup"><span data-stu-id="39a3e-107">This error occurs because the App-V 5.0 SP3 server does not understand the Windows 10 operating system that is specified in the publishing URL.</span></span> <span data-ttu-id="39a3e-108">Эта проблема устранена для сервера публикаций App-V 5,1, но не относится к версиям App-V 5,0 SP3 или более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="39a3e-108">The issue is fixed for App-V 5.1 publishing server, but is not backported to versions of App-V 5.0 SP3 or earlier.</span></span>

<span data-ttu-id="39a3e-109">**Временное решение**: обновите сервер App-v 5,0 до сервера управления App-v 5,1 для клиентов Windows 10.</span><span class="sxs-lookup"><span data-stu-id="39a3e-109">**Workaround**: Upgrade the App-V 5.0 Management server to the App-V 5.1 Management server for Windows 10 Clients.</span></span>

## <span data-ttu-id="39a3e-110">Пользовательские конфигурации не применяются к пакетам, которые будут опубликованы глобально, если они задаются с помощью сервера App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="39a3e-110">Custom configurations do not get applied for packages that will be published globally if they are set using the App-V 5.1 Server</span></span>


<span data-ttu-id="39a3e-111">Если вы назначаете пакет в РЕКЛАМную группу, которая будет содержать учетные записи компьютеров и примените пользовательскую конфигурацию к этой группе с помощью сервера App-V, настраиваемая конфигурация не будет применена к этим машинам.</span><span class="sxs-lookup"><span data-stu-id="39a3e-111">If you assign a package to an AD group that contains machine accounts and apply a custom configuration to that group using the App-V Server, the custom configuration will not be applied to those machines.</span></span> <span data-ttu-id="39a3e-112">Клиент App-V 5,1 будет публиковать пакеты, назначенные учетной записи компьютера глобально.</span><span class="sxs-lookup"><span data-stu-id="39a3e-112">The App-V 5.1 Client will publish packages assigned to a machine account globally.</span></span> <span data-ttu-id="39a3e-113">Однако он хранит пользовательские файлы конфигурации для каждого пользователя в профиле каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="39a3e-113">However, it stores custom configuration files per user in each user’s profile.</span></span> <span data-ttu-id="39a3e-114">Для глобальных опубликованных пакетов не будет доступа к этой настраиваемой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="39a3e-114">Globally published packages will not have access to this custom configuration.</span></span>

<span data-ttu-id="39a3e-115">**Временное решение**выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="39a3e-115">**Workaround**: Do one of the following:</span></span>

-   <span data-ttu-id="39a3e-116">Назначьте пакет группам, содержащим только учетные записи пользователей.</span><span class="sxs-lookup"><span data-stu-id="39a3e-116">Assign the package to groups containing only user accounts.</span></span> <span data-ttu-id="39a3e-117">Это гарантирует, что настраиваемая конфигурация пакета будет храниться в каждом пользовательском профиле и будет применена правильно.</span><span class="sxs-lookup"><span data-stu-id="39a3e-117">This will ensure that the package’s custom configuration will be stored in each user’s profile and will be applied correctly.</span></span>

-   <span data-ttu-id="39a3e-118">Создайте пользовательский файл конфигурации развертывания и примените его к пакету на клиенте с помощью командлета Add-AppvClientPackage с параметром – DynamicDeploymentConfiguration.</span><span class="sxs-lookup"><span data-stu-id="39a3e-118">Create a custom deployment configuration file and apply it to the package on the client using the Add-AppvClientPackage cmdlet with the –DynamicDeploymentConfiguration parameter.</span></span> <span data-ttu-id="39a3e-119">Дополнительные сведения можно найти в разделе [о динамической конфигурации App-V 5,1](about-app-v-51-dynamic-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="39a3e-119">See [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md) for more information.</span></span>

-   <span data-ttu-id="39a3e-120">Создайте новый пакет с настраиваемой конфигурацией с помощью секвенсора App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="39a3e-120">Create a new package with the custom configuration using the App-V 5.1 Sequencer.</span></span>

## <span data-ttu-id="39a3e-121">После установки новой версии App-V 5,1 серверные файлы не удаляются</span><span class="sxs-lookup"><span data-stu-id="39a3e-121">Server files not deleted after new App-V 5.1 Server installation</span></span>


<span data-ttu-id="39a3e-122">При удалении сервера App-V 5,0 SP1 и последующем установке сервера App-V 5,1 установка завершается сбоем, устанавливается неправильная версия сервера управления и возвращается сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="39a3e-122">If you uninstall the App-V 5.0 SP1 Server and then install the App-V 5.1 Server, the installation fails, the wrong version of the Management server is installed, and an error message is returned.</span></span> <span data-ttu-id="39a3e-123">Проблема возникает из-за того, что файлы сервера не удаляются при удалении App-V 5,0 с пакетом обновления 1 (SP1), поэтому процесс установки производит обновление вместо новой установки.</span><span class="sxs-lookup"><span data-stu-id="39a3e-123">The issue occurs because the Server files are not being deleted when you uninstall App-V 5.0 SP1, so the installation process does an upgrade instead of a new installation.</span></span>

<span data-ttu-id="39a3e-124">**Временное решение**: удалите этот раздел реестра, прежде чем приступить к установке App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="39a3e-124">**Workaround**: Delete this registry key before you start installing App-V 5.1:</span></span>

<span data-ttu-id="39a3e-125">В разделе HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall найдите и удалите раздел GUID установки, который включает параметр DWORD "DisplayName" с данными значения "Microsoft Application Virtualization (App-V) Server".</span><span class="sxs-lookup"><span data-stu-id="39a3e-125">Under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall, locate and delete the installation GUID key that contains the DWORD value "DisplayName" with value data "Microsoft Application Virtualization (App-V) Server".</span></span> <span data-ttu-id="39a3e-126">Это единственный ключ, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="39a3e-126">This is the only key that should be deleted.</span></span>

## <span data-ttu-id="39a3e-127">Сопоставления типов файлов, добавленные вручную, не сохраняются надлежащим образом</span><span class="sxs-lookup"><span data-stu-id="39a3e-127">File type associations added manually are not saved correctly</span></span>


<span data-ttu-id="39a3e-128">Сопоставления типов файлов, добавленные в пакет приложения вручную с помощью клавиш и вкладки FTAs в конце мастера обновления приложений, не сохраняются надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="39a3e-128">File type associations added to an application package manually using the Shortcuts and FTAs tab at the end of the application upgrade wizard are not saved correctly.</span></span> <span data-ttu-id="39a3e-129">Они не будут доступны для клиента App-V или секвенсор при повторном обновлении сохраненного пакета.</span><span class="sxs-lookup"><span data-stu-id="39a3e-129">They will not be available to the App-V Client or to the Sequencer when updating the saved package again.</span></span>

<span data-ttu-id="39a3e-130">**Временное решение**: чтобы добавить ассоциацию типа файла, откройте пакет для изменения и запустите мастер обновления.</span><span class="sxs-lookup"><span data-stu-id="39a3e-130">**Workaround**: To add a file type association, open the package for modification and run the update wizard.</span></span> <span data-ttu-id="39a3e-131">На этапе установки добавьте новую связь типа файла в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="39a3e-131">During the Installation step, add the new file type association through the operating system.</span></span> <span data-ttu-id="39a3e-132">Секвенсор обнаружит новую связь в системном реестре и добавит ее в виртуальный реестр пакета, где он будет доступен для клиента.</span><span class="sxs-lookup"><span data-stu-id="39a3e-132">The sequencer will detect the new association in the system registry and add it to the package’s virtual registry, where it will be available to the client.</span></span>

## <span data-ttu-id="39a3e-133">Дополнительные данные записываются на локальный диск, когда потоковые пакеты в режиме общего хранилища содержимого (SCS) выводятся в клиенте, который также управляется AppLocker.</span><span class="sxs-lookup"><span data-stu-id="39a3e-133">When streaming packages in Shared Content Store (SCS) mode to a client that is also managed with AppLocker, additional data is written to the local disk.</span></span>


<span data-ttu-id="39a3e-134">Чтобы уменьшить объем данных, записываемых на локальный диск клиента, вы можете включить режим SCS в клиенте App-V 5,1 для потоковой передачи содержимого пакета по запросу.</span><span class="sxs-lookup"><span data-stu-id="39a3e-134">To decrease the amount of data written to a client’s local disk, you can enable SCS mode on the App-V 5.1 Client to stream the contents of a package on demand.</span></span> <span data-ttu-id="39a3e-135">Тем не менее, если AppLocker управляет приложением в пакете, некоторые данные могут быть написаны на локальном диске клиента, который в противном случае не записывается.</span><span class="sxs-lookup"><span data-stu-id="39a3e-135">However, if AppLocker manages an application within the package, some data might be written to the client’s local disk that would not otherwise be written.</span></span>

<span data-ttu-id="39a3e-136">**Временное решение**: нет</span><span class="sxs-lookup"><span data-stu-id="39a3e-136">**Workaround**: None</span></span>

## <span data-ttu-id="39a3e-137">Кнопка "Обзор" в диалоговом окне "добавить пакет" на консоли управления недоступна при использовании Chrome или Firefox</span><span class="sxs-lookup"><span data-stu-id="39a3e-137">In the Management Console Add Package dialog box, the Browse button is not available when using Chrome or Firefox</span></span>


<span data-ttu-id="39a3e-138">На странице Packages (пакеты) на консоли управления, если в правом нижнем углу нажать кнопку **Добавить или обновить** , появится диалоговое окно **Добавление пакета** .</span><span class="sxs-lookup"><span data-stu-id="39a3e-138">On the Packages page of the Management Console, if you click **Add or Upgrade** in the lower-right corner, the **Add Package** dialog box appears.</span></span> <span data-ttu-id="39a3e-139">Если вы обращаетесь к консоли управления с помощью Chrome или Firefox в качестве браузера, вы не сможете перейти к расположению пакета.</span><span class="sxs-lookup"><span data-stu-id="39a3e-139">If you are accessing the Management Console using Chrome or Firefox as your browser, you will not be able to browse to the location of the package.</span></span>

<span data-ttu-id="39a3e-140">**Временное решение**: введите (или скопируйте и вставьте) путь к пакету в поле **Add Package input (добавить пакет** ).</span><span class="sxs-lookup"><span data-stu-id="39a3e-140">**Workaround**: Type or copy and paste the path to the package into the **Add Package** input field.</span></span> <span data-ttu-id="39a3e-141">Если консоль управления имеет доступ к этому пути, вы сможете добавить пакет.</span><span class="sxs-lookup"><span data-stu-id="39a3e-141">If the Management Console has access to this path, you will be able to add the package.</span></span> <span data-ttu-id="39a3e-142">Если пакет находится в общей сетевой папке, вы можете перейти к расположению с помощью проводника, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="39a3e-142">If the package is on a network share, you can browse to the location using File Explorer by doing these steps:</span></span>

1.  <span data-ttu-id="39a3e-143">Удерживая нажатой **клавишу Shift**, щелкните файл пакета правой кнопкой мыши</span><span class="sxs-lookup"><span data-stu-id="39a3e-143">While pressing **Shift**, right-click on the package file</span></span>

2.  <span data-ttu-id="39a3e-144">Выберите команду " **Копировать как путь** "</span><span class="sxs-lookup"><span data-stu-id="39a3e-144">Select **Copy as path**</span></span>

3.  <span data-ttu-id="39a3e-145">Вставьте путь в поле ввода диалогового окна " **Добавление пакета** ".</span><span class="sxs-lookup"><span data-stu-id="39a3e-145">Paste the path into the **Add Package** dialog box input field</span></span>

## <a href="" id="upgrading-app-v-management-server-to-5-1-sometimes-fails-with-the-message--a-database-error-occurred-"></a><span data-ttu-id="39a3e-146">При обновлении сервера управления App-V до 5,1 иногда происходит сбой с сообщением "произошла ошибка базы данных".</span><span class="sxs-lookup"><span data-stu-id="39a3e-146">Upgrading App-V Management Server to 5.1 sometimes fails with the message “A database error occurred”</span></span>


<span data-ttu-id="39a3e-147">Если вы установили сервер управления пакетом обновления 1 (SP1) для App-V 5,0, а затем пытаетесь перейти на сервер App-V 5,1, если настроены и включены несколько групп подключений, появляется следующее сообщение об ошибке: "произошла ошибка базы данных".</span><span class="sxs-lookup"><span data-stu-id="39a3e-147">If you install the App-V 5.0 SP1 Management Server, and then try to upgrade to App-V 5.1 Server when multiple connection groups are configured and enabled, the following error is displayed: “A database error occurred.</span></span> <span data-ttu-id="39a3e-148">Причина: "Недопустимый столбец с именем" PackageOptional ".</span><span class="sxs-lookup"><span data-stu-id="39a3e-148">Reason: 'Invalid column name 'PackageOptional'.</span></span> <span data-ttu-id="39a3e-149">Неправильное имя столбца "VersionOptional".</span><span class="sxs-lookup"><span data-stu-id="39a3e-149">Invalid column name 'VersionOptional'.”</span></span>

<span data-ttu-id="39a3e-150">**Временное решение**: выполните эту команду в базе данных SQL:</span><span class="sxs-lookup"><span data-stu-id="39a3e-150">**Workaround**: Run this command on your SQL database:</span></span>

`ALTER TABLE AppVManagement.dbo.PackageGroupMembers ADD PackageOptional bit NOT NULL DEFAULT 0, VersionOptional bit NOT NULL DEFAULT 0`

<span data-ttu-id="39a3e-151">где "AppVManagement" — это имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="39a3e-151">where “AppVManagement” is the name of the database.</span></span>

## <span data-ttu-id="39a3e-152">Пользователи не могут открыть пакет в опубликованной пользователем группе подключения, если вы добавляете или удаляете дополнительный пакет.</span><span class="sxs-lookup"><span data-stu-id="39a3e-152">Users cannot open a package in a user-published connection group if you add or remove an optional package</span></span>


<span data-ttu-id="39a3e-153">В средах, в которых запущен клиент RDS или у которых есть несколько параллельных пользователей на компьютере, пользователи, вошедших в группу, не могут открывать приложения в пакетах, которые находятся в опубликованной пользователем группе подключения, если дополнительный пакет добавляется в группу или удаляется из нее.</span><span class="sxs-lookup"><span data-stu-id="39a3e-153">In environments that are running the RDS Client or that have multiple concurrent users per computer, logged-in users cannot open applications in packages that are in a user-published connection group if an optional package is added to or removed from the connection group.</span></span>

<span data-ttu-id="39a3e-154">**Временное решение**: Выйдите из учетной записи пользователя, а затем снова войдите в нее.</span><span class="sxs-lookup"><span data-stu-id="39a3e-154">**Workaround**: Have users log out and then log back in.</span></span>

## <span data-ttu-id="39a3e-155">Сообщение об ошибке ошибочно отображается, если группа подключений опубликована только для пользователя</span><span class="sxs-lookup"><span data-stu-id="39a3e-155">Error message is erroneously displayed when the connection group is published only to the user</span></span>


<span data-ttu-id="39a3e-156">При запуске Repair-AppvClientConnectionGroup появляется следующее сообщение об ошибке, даже если группа подключений опубликована только для пользователя: "Внутренняя ошибка интеграции App-V: пакет не интегрирован для пользователя.</span><span class="sxs-lookup"><span data-stu-id="39a3e-156">When you run Repair-AppvClientConnectionGroup, the following error is displayed, even when the connection group is published only to the user: “Internal App-V Integration error: Package not integrated for the user.</span></span> <span data-ttu-id="39a3e-157">Убедитесь, что пакет добавлен на компьютер и опубликован пользователю. "</span><span class="sxs-lookup"><span data-stu-id="39a3e-157">Please ensure that the package is added to the machine and published to the user.”</span></span>

<span data-ttu-id="39a3e-158">**Временное решение**выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="39a3e-158">**Workaround**: Do one of the following:</span></span>

-   <span data-ttu-id="39a3e-159">Опубликуйте все пакеты в группе подключения.</span><span class="sxs-lookup"><span data-stu-id="39a3e-159">Publish all packages in a connection group.</span></span>

    <span data-ttu-id="39a3e-160">Проблема возникает в том случае, если у удаляемой группы подключения есть пакеты, которые отсутствуют или недоступны пользователю (то есть не Опубликовано глобально или с пользователем).</span><span class="sxs-lookup"><span data-stu-id="39a3e-160">The problem arises when the connection group being repaired has packages that are missing or not available to the user (that is, not published globally or to the user).</span></span> <span data-ttu-id="39a3e-161">Однако восстановление будет работать, если все пакеты группы подключений доступны, поэтому убедитесь, что все пакеты опубликованы.</span><span class="sxs-lookup"><span data-stu-id="39a3e-161">However, the repair will work if all of the connection group’s packages are available, so ensure that all packages are published.</span></span>

-   <span data-ttu-id="39a3e-162">Исправлять пакеты по отдельности с помощью команды Repair-AppvClientPackage, а не команды Repair-AppvClientConnectionGroup.</span><span class="sxs-lookup"><span data-stu-id="39a3e-162">Repair packages individually using the Repair-AppvClientPackage command rather than the Repair-AppvClientConnectionGroup command.</span></span>

    <span data-ttu-id="39a3e-163">Определите, какие пакеты доступны пользователям, и запустите команду repair-AppvClientPackage один раз для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="39a3e-163">Determine which packages are available to users and then run the Repair-AppvClientPackage command once for each package.</span></span> <span data-ttu-id="39a3e-164">С помощью командлетов PowerShell выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="39a3e-164">Use PowerShell cmdlets to do the following:</span></span>

    1.  <span data-ttu-id="39a3e-165">Получение всех пакетов в группе подключения.</span><span class="sxs-lookup"><span data-stu-id="39a3e-165">Get all the packages in a connection group.</span></span>

    2.  <span data-ttu-id="39a3e-166">Проверьте, опубликован ли каждый пакет в данный момент.</span><span class="sxs-lookup"><span data-stu-id="39a3e-166">Check to see if each package is currently published.</span></span>

    3.  <span data-ttu-id="39a3e-167">Если пакет уже опубликован, запустите команду repair-AppvClientPackage для этого пакета.</span><span class="sxs-lookup"><span data-stu-id="39a3e-167">If the package is currently published, run Repair-AppvClientPackage on that package.</span></span>

## <span data-ttu-id="39a3e-168">Значки неправильно отображаются в секвенсоре</span><span class="sxs-lookup"><span data-stu-id="39a3e-168">Icons not displayed properly in Sequencer</span></span>


<span data-ttu-id="39a3e-169">Значки на вкладке "сочетания клавиш" и "сопоставление типов файлов" отображаются неправильно при изменении пакета в секвенсоре App-V.</span><span class="sxs-lookup"><span data-stu-id="39a3e-169">Icons in the Shortcuts and File Type Associations tab are not displayed correctly when modifying a package in the App-V Sequencer.</span></span> <span data-ttu-id="39a3e-170">Эта проблема возникает в том случае, если размер значков не равен 16x16 или 32x32.</span><span class="sxs-lookup"><span data-stu-id="39a3e-170">This problem occurs when the size of the icons are not 16x16 or 32x32.</span></span>

<span data-ttu-id="39a3e-171">**Временное решение**: Используйте только значки размером 16x16 или 32x32.</span><span class="sxs-lookup"><span data-stu-id="39a3e-171">**Workaround**: Only use icons that are 16x16 or 32x32.</span></span>

## <span data-ttu-id="39a3e-172">Сценарий InsertVersionInfo. SQL больше не требуется для базы данных управления</span><span class="sxs-lookup"><span data-stu-id="39a3e-172">InsertVersionInfo.sql script no longer required for the Management Database</span></span>


<span data-ttu-id="39a3e-173">Сценарий InsertVersionInfo. SQL не требуется для версий базы данных управления App-V более поздней версии, чем App-V 5,0 с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="39a3e-173">The InsertVersionInfo.sql script is not required for versions of the App-V management database later than App-V 5.0 SP3.</span></span>

<span data-ttu-id="39a3e-174">Сценарий Permissions. SQL должен обновляться в соответствии с **шагом 2** в [статье 3031340 базы знаний](https://support.microsoft.com/kb/3031340).</span><span class="sxs-lookup"><span data-stu-id="39a3e-174">The Permissions.sql script should be updated according to **Step 2** in [KB article 3031340](https://support.microsoft.com/kb/3031340).</span></span>

<span data-ttu-id="39a3e-175">**Важно!** 
 **Шаг 1** не требуется для версий App-v, более поздних, чем App-v 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="39a3e-175">**Important**
**Step 1** is not required for versions of App-V later than App-V 5.0 SP3.</span></span>

 

## <span data-ttu-id="39a3e-176">Microsoft Visual Studio 2012 не поддерживается</span><span class="sxs-lookup"><span data-stu-id="39a3e-176">Microsoft Visual Studio 2012 not supported</span></span>


<span data-ttu-id="39a3e-177">Приложение App-V 5,1 не поддерживает Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="39a3e-177">App-V 5.1 does not support Visual Studio 2012.</span></span>

<span data-ttu-id="39a3e-178">**Временное решение**: нет</span><span class="sxs-lookup"><span data-stu-id="39a3e-178">**Workaround**: None</span></span>

## <span data-ttu-id="39a3e-179">Ограничения имени файла приложения для приложения Sequencer-V 5. x</span><span class="sxs-lookup"><span data-stu-id="39a3e-179">Application filename restrictions for App-V 5.x Sequencer</span></span>


<span data-ttu-id="39a3e-180">Секвенсор App-V 5. x не может последовательностей в приложениях с именами, соответствующими "CO_ &lt; x &gt; ", где x — любая цифра.</span><span class="sxs-lookup"><span data-stu-id="39a3e-180">The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="39a3e-181">Будет сгенерировано сообщение об ошибке 0x8007139F.</span><span class="sxs-lookup"><span data-stu-id="39a3e-181">Error 0x8007139F will be generated.</span></span>

<span data-ttu-id="39a3e-182">**Временное решение**: используйте другое имя файла</span><span class="sxs-lookup"><span data-stu-id="39a3e-182">**Workaround**: Use a different filename</span></span>

## <span data-ttu-id="39a3e-183">Ошибка "файл не найден" при подключении пакета</span><span class="sxs-lookup"><span data-stu-id="39a3e-183">Intermittent "File Not Found" error when Mounting a Package</span></span>


<span data-ttu-id="39a3e-184">Иногда при подключении пакета генерируется ошибка "файл не найден" (0x80070002).</span><span class="sxs-lookup"><span data-stu-id="39a3e-184">Occasionally when mounting a package, a "File Not Found" (0x80070002) error is generated.</span></span> <span data-ttu-id="39a3e-185">Обычно это происходит, если папка в пакете App-V состоит из большого количества файлов (например, 20K или более).</span><span class="sxs-lookup"><span data-stu-id="39a3e-185">Typically, this occurs when a folder in an App-V package contains many files ( i.e. 20K or more).</span></span> <span data-ttu-id="39a3e-186">Это может привести к тому, что потоковые потоки будут занимать больше времени, чем ожидалось, и не выйдет время ожидания, которое создает ошибку "файл не найден"</span><span class="sxs-lookup"><span data-stu-id="39a3e-186">This can cause streaming to take longer than expected and to time out which generates the "File Not Found" error.</span></span>

<span data-ttu-id="39a3e-187">**Временное решение**: начиная с HF06, появился новый раздел реестра, позволяющий расширить этот период ожидания.</span><span class="sxs-lookup"><span data-stu-id="39a3e-187">**Workaround**: Starting with HF06, a new registry key has been introduced to enable extending this time-out period.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<tbody>
<tr>
<td align="left"><span data-ttu-id="39a3e-188">Путь</span><span class="sxs-lookup"><span data-stu-id="39a3e-188">Path</span></span></td>
<td align="left"><span data-ttu-id="39a3e-189">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\Streaming</span><span class="sxs-lookup"><span data-stu-id="39a3e-189">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Streaming</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="39a3e-190">Параметр</span><span class="sxs-lookup"><span data-stu-id="39a3e-190">Setting</span></span></td>
<td align="left"><span data-ttu-id="39a3e-191">StreamResponseWaitTimeout</span><span class="sxs-lookup"><span data-stu-id="39a3e-191">StreamResponseWaitTimeout</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="39a3e-192">Типа</span><span class="sxs-lookup"><span data-stu-id="39a3e-192">DataType</span></span></td>
<td align="left"><span data-ttu-id="39a3e-193">DWORD</span><span class="sxs-lookup"><span data-stu-id="39a3e-193">DWORD</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="39a3e-194">Измерения</span><span class="sxs-lookup"><span data-stu-id="39a3e-194">Units</span></span></td>
<td align="left"><span data-ttu-id="39a3e-195">Течение</span><span class="sxs-lookup"><span data-stu-id="39a3e-195">Seconds</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="39a3e-196">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="39a3e-196">Default</span></span></td>
<td align="left"><span data-ttu-id="39a3e-197">5</span><span class="sxs-lookup"><span data-stu-id="39a3e-197">5</span></span><br />
<strong><span data-ttu-id="39a3e-198">Примечание </strong> : это значение по умолчанию, если раздел реестра не определен, или &lt; задано значение 5.</span><span class="sxs-lookup"><span data-stu-id="39a3e-198">Note</strong>: this value is the default if the registry key is not defined or a value &lt;=5 is specified.</span></span>
</td>
</tr>
</tbody>
</table>






## <span data-ttu-id="39a3e-199">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="39a3e-199">Related topics</span></span>


[<span data-ttu-id="39a3e-200">Сведения об App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="39a3e-200">About App-V 5.1</span></span>](about-app-v-51.md)

 

 





