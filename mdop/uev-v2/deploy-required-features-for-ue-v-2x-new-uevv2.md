---
title: Развертывание необходимых компонентов для UE-v 2.x
description: Развертывание необходимых компонентов для UE-v 2.x
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824669"
---
# <span data-ttu-id="54ba4-103">Развертывание необходимых компонентов для UE-v 2.x</span><span class="sxs-lookup"><span data-stu-id="54ba4-103">Deploy Required Features for UE-V 2.x</span></span>


<span data-ttu-id="54ba4-104">Для всех развертываний Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 и 2,1 SP1 нужны следующие функции:</span><span class="sxs-lookup"><span data-stu-id="54ba4-104">All Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 deployments require these features</span></span>

-   <span data-ttu-id="54ba4-105">[Развертывание места хранения параметров](#ssl) , доступного для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="54ba4-105">[Deploy a Settings Storage Location](#ssl) that is accessible to end users.</span></span>

    <span data-ttu-id="54ba4-106">Это стандартная сетевая общей папке, в которой хранятся и извлекаются параметры пользователя.</span><span class="sxs-lookup"><span data-stu-id="54ba4-106">This is a standard network share that stores and retrieves user settings.</span></span>

-   [<span data-ttu-id="54ba4-107">Выбор метода конфигурации для UE-V</span><span class="sxs-lookup"><span data-stu-id="54ba4-107">Choose the Configuration Method for UE-V</span></span>](#config)

    <span data-ttu-id="54ba4-108">UE-V можно разворачивать и настраивать с помощью стандартных средств управления, включая групповую политику, Диспетчер конфигураций, а также инфраструктуру управления Windows и PowerShell.</span><span class="sxs-lookup"><span data-stu-id="54ba4-108">UE-V can be deployed and configured using common management tools including group policy, Configuration Manager, or Windows Management Infrastructure and Powershell.</span></span>

-   <span data-ttu-id="54ba4-109">[Развертывание агента UE-V](#agent) для установки на каждом компьютере, который синхронизирует параметры.</span><span class="sxs-lookup"><span data-stu-id="54ba4-109">[Deploy a UE-V Agent](#agent) to be installed on every computer that synchronizes settings.</span></span>

    <span data-ttu-id="54ba4-110">Это отслеживает зарегистрированные приложения и операционную систему на предмет изменений параметров и синхронизирует эти параметры между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="54ba4-110">This monitors registered applications and the operating system for any settings changes and synchronizes those settings between computers.</span></span>

<span data-ttu-id="54ba4-111">В этой статье описано, как развертывать эти функции.</span><span class="sxs-lookup"><span data-stu-id="54ba4-111">The topics in this section describe how to deploy these features.</span></span>

## <a href="" id="ssl"></a><span data-ttu-id="54ba4-112">Развертывание расположения хранилища параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="54ba4-112">Deploy a UE-V Settings Storage Location</span></span>


<span data-ttu-id="54ba4-113">Для UE-V требуется расположение, в котором нужно хранить параметры пользователя в файлах пакета параметров.</span><span class="sxs-lookup"><span data-stu-id="54ba4-113">UE-V requires a location in which to store user settings in settings package files.</span></span> <span data-ttu-id="54ba4-114">Вы можете настроить место хранения параметров одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="54ba4-114">You can configure this settings storage location in one of these ways:</span></span>

-   <span data-ttu-id="54ba4-115">Создание собственного места для хранения параметров</span><span class="sxs-lookup"><span data-stu-id="54ba4-115">Create your own settings storage location</span></span>

-   <span data-ttu-id="54ba4-116">Использование существующей службы каталогов Active Directory для хранения параметров</span><span class="sxs-lookup"><span data-stu-id="54ba4-116">Use existing Active Directory for your settings storage location</span></span>

<span data-ttu-id="54ba4-117">Если вы не создаете место хранения параметров, агент UE-V Agent будет по умолчанию использовать Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="54ba4-117">If you don’t create a settings storage location, the UE-V Agent will use Active Directory (AD) by default.</span></span>

**<span data-ttu-id="54ba4-118">Примечание.</span><span class="sxs-lookup"><span data-stu-id="54ba4-118">Note</span></span>**  
<span data-ttu-id="54ba4-119">В [плане производительности и емкости](https://technet.microsoft.com/library/dn458932.aspx#capacity) , а также для снижения проблем с задержкой сети, создайте места хранения параметров в тех же локальных сетях, где находятся компьютеры пользователей.</span><span class="sxs-lookup"><span data-stu-id="54ba4-119">As a matter of [performance and capacity planning](https://technet.microsoft.com/library/dn458932.aspx#capacity) and to reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="54ba4-120">Рекомендуем использовать для хранения параметров 20 МБ свободного места на диске для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="54ba4-120">We recommend 20 MB of disk space per user for the settings storage location.</span></span>



### <span data-ttu-id="54ba4-121">Создание места хранения параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="54ba4-121">Create a UE-V Settings Storage Location</span></span>

<span data-ttu-id="54ba4-122">Перед определением места хранения параметров необходимо создать корневой каталог с разрешениями на чтение и запись для пользователей, которые хранят параметры в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="54ba4-122">Before you define the settings storage location, you must create a root directory with read/write permissions for users who store settings on the share.</span></span> <span data-ttu-id="54ba4-123">Агент UE-V создает пользовательские папки под этим корневым каталогом.</span><span class="sxs-lookup"><span data-stu-id="54ba4-123">The UE-V Agent creates user-specific folders under this root directory.</span></span>

<span data-ttu-id="54ba4-124">Место хранения параметров определяется путем настройки параметра конфигурации SettingsStoragePath, который можно настроить с помощью одного из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="54ba4-124">The settings storage location is defined by setting the SettingsStoragePath configuration option, which you can configure by using one of these methods:</span></span>

-   <span data-ttu-id="54ba4-125">При [развертывании агента UE-V](#agent) с помощью параметра командной строки или пакетного сценария</span><span class="sxs-lookup"><span data-stu-id="54ba4-125">When you [Deploy the UE-V Agent](#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="54ba4-126">С помощью параметров [групповой политики](https://technet.microsoft.com/library/dn458893.aspx)</span><span class="sxs-lookup"><span data-stu-id="54ba4-126">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="54ba4-127">С помощью [пакета конфигурации System Center](https://technet.microsoft.com/library/dn458917.aspx) для UE-V</span><span class="sxs-lookup"><span data-stu-id="54ba4-127">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="54ba4-128">После установки агента UE-V с помощью [Windows PowerShell или инструментария управления Windows (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span><span class="sxs-lookup"><span data-stu-id="54ba4-128">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>

<span data-ttu-id="54ba4-129">Путь должен быть указан в формате UNC сервера и общего доступа.</span><span class="sxs-lookup"><span data-stu-id="54ba4-129">The path must be in a universal naming convention (UNC) path of the server and share.</span></span> <span data-ttu-id="54ba4-130">Например, **\\\\Server\\Settingsshare\\**.</span><span class="sxs-lookup"><span data-stu-id="54ba4-130">For example, **\\\\Server\\Settingsshare\\**.</span></span> <span data-ttu-id="54ba4-131">Этот параметр конфигурации поддерживает использование переменных для включения конкретных сценариев синхронизации.</span><span class="sxs-lookup"><span data-stu-id="54ba4-131">This configuration option supports the use of variables to enable specific synchronization scenarios.</span></span> <span data-ttu-id="54ba4-132">Например, вы можете использовать `%username%\%computername%` переменные для сохранения параметров конечного пользователя в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="54ba4-132">For example, you can use the `%username%\%computername%` variables to preserve the end user settings experience in these scenarios:</span></span>

-   <span data-ttu-id="54ba4-133">Завершение работы пользователей, использующих несколько физических компьютеров предприятия</span><span class="sxs-lookup"><span data-stu-id="54ba4-133">End users that use multiple physical computers in your enterprise</span></span>

-   <span data-ttu-id="54ba4-134">Корпоративные компьютеры, используемые несколькими конечными пользователями</span><span class="sxs-lookup"><span data-stu-id="54ba4-134">Enterprise computers that are used by multiple end users</span></span>

<span data-ttu-id="54ba4-135">Агент UE-V динамически создает путь к хранилищу параметров для определенного пользователя, с именем скрытой системной папки в `SettingsPackages` соответствии с параметром конфигурации **SettingsStoragePath**.</span><span class="sxs-lookup"><span data-stu-id="54ba4-135">The UE-V Agent dynamically creates a user-specific settings storage path, with a hidden system folder named `SettingsPackages`, based on the configuration setting of **SettingsStoragePath**.</span></span> <span data-ttu-id="54ba4-136">Агент считывает и записывает в это расположение параметры, заданные зарегистрированными шаблонами расположений параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="54ba4-136">The agent reads and writes settings to this location as defined by the registered UE-V settings location templates.</span></span>

<span data-ttu-id="54ba4-137">**Параметры UE-V определяются правилом "Последнее запись WINS".** Если место хранения параметров одинаково для пользователей с несколькими управляемыми компьютерами, один агент UE-V производит чтение и запись в расположение параметров независимо от агентов, запущенных на других компьютерах.</span><span class="sxs-lookup"><span data-stu-id="54ba4-137">**UE-V settings are determined by a "Last write wins" rule:** If the settings storage location is the same for user with multiple managed computers, one UE-V Agent reads and writes to the settings location independently of agents running on other computers.</span></span> <span data-ttu-id="54ba4-138">Последние записанные параметры и значения — это те, которые применяются при чтении следующего агента из места хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="54ba4-138">The last written settings and values are the ones applied when the next agent reads from the settings storage location.</span></span>

<span data-ttu-id="54ba4-139">**Развертывание места хранения параметров.** Выполните указанные ниже действия, чтобы определить место хранения параметров, а не использование существующей службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54ba4-139">**Deploy the settings storage location:** Follow these steps to define the settings storage location rather than using your existing Active Directory service.</span></span> <span data-ttu-id="54ba4-140">Ограничьте доступ к общему хранилищу параметров для тех пользователей, которым он необходим, как показано в приведенных ниже таблицах.</span><span class="sxs-lookup"><span data-stu-id="54ba4-140">You should limit access to the settings storage share to those users that require it, as shown in the tables below.</span></span>

**<span data-ttu-id="54ba4-141">Развертывание сетевого общего доступа UE-V</span><span class="sxs-lookup"><span data-stu-id="54ba4-141">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="54ba4-142">Создайте новую группу безопасности для пользователей UE-V.</span><span class="sxs-lookup"><span data-stu-id="54ba4-142">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="54ba4-143">Создайте новую папку на центральном компьютере, где хранятся пакеты параметров UE-V, а затем предоставьте пользователям UE-V доступ к папке с разрешениями группы.</span><span class="sxs-lookup"><span data-stu-id="54ba4-143">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="54ba4-144">Администратору, который поддерживает UE-V, должны быть предоставлены разрешения на доступ к этой общей папке.</span><span class="sxs-lookup"><span data-stu-id="54ba4-144">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="54ba4-145">Установите следующие разрешения на доступ к блоку сообщений сервера уровня ресурсов (SMB) для папки "Параметры хранилища".</span><span class="sxs-lookup"><span data-stu-id="54ba4-145">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="54ba4-146">Учетная запись пользователя</span><span class="sxs-lookup"><span data-stu-id="54ba4-146">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="54ba4-147">Рекомендуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="54ba4-147">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="54ba4-148">Все пользователи</span><span class="sxs-lookup"><span data-stu-id="54ba4-148">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="54ba4-149">Нет разрешений</span><span class="sxs-lookup"><span data-stu-id="54ba4-149">No permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="54ba4-150">Группа безопасности пользователей UE-V</span><span class="sxs-lookup"><span data-stu-id="54ba4-150">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="54ba4-151">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="54ba4-151">Full control</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="54ba4-152">Установите следующие разрешения файловой системы NTFS для папки "место хранения параметров".</span><span class="sxs-lookup"><span data-stu-id="54ba4-152">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="54ba4-153">Учетная запись пользователя</span><span class="sxs-lookup"><span data-stu-id="54ba4-153">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="54ba4-154">Рекомендуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="54ba4-154">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="54ba4-155">Папка</span><span class="sxs-lookup"><span data-stu-id="54ba4-155">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="54ba4-156">Создатель/владелец</span><span class="sxs-lookup"><span data-stu-id="54ba4-156">Creator/owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="54ba4-157">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="54ba4-157">Full control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="54ba4-158">Только для вложенных папок и файлов</span><span class="sxs-lookup"><span data-stu-id="54ba4-158">Subfolders and files only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="54ba4-159">Группа безопасности пользователей UE-V</span><span class="sxs-lookup"><span data-stu-id="54ba4-159">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="54ba4-160">Просмотр папки/Чтение данных, создание папок и добавление данных</span><span class="sxs-lookup"><span data-stu-id="54ba4-160">List folder/read data, create folders/append data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="54ba4-161">Только для этой папки</span><span class="sxs-lookup"><span data-stu-id="54ba4-161">This folder only</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="54ba4-162">В этой конфигурации агент UE-V Agent создает и защищает папку Settingspackage, когда она выполняется в контексте пользователя, и предоставляет каждому пользователю разрешение на создание папок для хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="54ba4-162">With this configuration, the UE-V Agent creates and secures a Settingspackage folder while it runs in the context of the user, and grants each user permission to create folders for settings storage.</span></span> <span data-ttu-id="54ba4-163">Пользователи получают полный доступ к своей папке Settingspackage, пока другие пользователи не имеют к ней доступа.</span><span class="sxs-lookup"><span data-stu-id="54ba4-163">Users receive full control to their Settingspackage folder while other users cannot access it.</span></span>

**<span data-ttu-id="54ba4-164">Примечание.</span><span class="sxs-lookup"><span data-stu-id="54ba4-164">Note</span></span>**  
<span data-ttu-id="54ba4-165">Если вы создаете общий доступ к хранилищу параметров на компьютере под управлением операционной системы Windows Server, настройте UE-V, чтобы убедиться в том, что локальная группа администраторов или текущий пользователь является владельцем папки, в которой хранятся пакеты параметров.</span><span class="sxs-lookup"><span data-stu-id="54ba4-165">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="54ba4-166">Чтобы включить эту дополнительную защиту, укажите этот параметр в редакторе реестра Windows Server.</span><span class="sxs-lookup"><span data-stu-id="54ba4-166">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="54ba4-167">Добавьте раздел реестра **reg \ _DWORD** с именем **"RepositoryOwnerCheckEnabled"** в раздел **hKey \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.</span><span class="sxs-lookup"><span data-stu-id="54ba4-167">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="54ba4-168">Установите для раздела реестра значение *1*.</span><span class="sxs-lookup"><span data-stu-id="54ba4-168">Set the registry key value to *1*.</span></span>



### <span data-ttu-id="54ba4-169">Использование службы каталогов Active Directory с UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="54ba4-169">Use Active Directory with UE-V 2.x</span></span>

<span data-ttu-id="54ba4-170">Агент UE-V использует Active Directory (AD) по умолчанию, если место хранения параметров не определено в противном случае.</span><span class="sxs-lookup"><span data-stu-id="54ba4-170">The UE-V Agent uses Active Directory (AD) by default if a settings storage location is not otherwise defined.</span></span> <span data-ttu-id="54ba4-171">В этих случаях агент UE-V динамически создает папку хранения параметров в корне основного каталога рекламных объявлений каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="54ba4-171">In these cases, the UE-V Agent dynamically creates the settings storage folder under the root of the AD home directory of each user.</span></span> <span data-ttu-id="54ba4-172">Но если настраиваемый параметр каталога настроен в AD, вместо него используется этот каталог.</span><span class="sxs-lookup"><span data-stu-id="54ba4-172">But, if a custom directory setting is configured in AD, then that directory is used instead.</span></span>

## <a href="" id="config"></a><span data-ttu-id="54ba4-173">Выберите метод конфигурации для UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="54ba4-173">Choose the Configuration Method for UE-V 2.x</span></span>


<span data-ttu-id="54ba4-174">Вы хотите узнать, какой метод конфигурации вы используете для управления UE-V после развертывания, так как это будет метод конфигурации, который вы используете для развертывания UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="54ba4-174">You want to figure out which configuration method you'll use to manage UE-V after deployment since this will be the configuration method you use to deploy the UE-V Agent.</span></span> <span data-ttu-id="54ba4-175">Обычно это метод конфигурации, который уже используется в среде, например Windows PowerShell или Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="54ba4-175">Typically, this is the configuration method that you already use in your environment, such as Windows PowerShell or Configuration Manager.</span></span>

<span data-ttu-id="54ba4-176">Агенты UE-V до, во время и после установки агента UE-V можно настроить в зависимости от используемого метода конфигурации.</span><span class="sxs-lookup"><span data-stu-id="54ba4-176">You can configure UE-V before, during, or after UE-V Agent installation, depending on the configuration method that you use.</span></span>

-   <span data-ttu-id="54ba4-177">[Групповая политика](https://technet.microsoft.com/library/dn458893.aspx)**:** вы можете использовать существующую инфраструктуру групповой политики для настройки UE-v до или после развертывания агента UE-v.</span><span class="sxs-lookup"><span data-stu-id="54ba4-177">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You can use your existing Group Policy infrastructure to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="54ba4-178">Шаблон файлов ADMX групповой политики UE-V обеспечивает централизованное управление общими параметрами конфигурации агента UE-V и включает параметры для настройки синхронизации UE-V.</span><span class="sxs-lookup"><span data-stu-id="54ba4-178">The UE-V Group Policy ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span>

    <span data-ttu-id="54ba4-179">**Установка шаблонов ADMX для групповой политики UE-V:** Шаблоны ADMX из групповой политики для UE-v настройте параметры синхронизации для агента UE-2.2 и разрешите централизованное управление общими параметрами конфигурации агента UE-V с помощью существующей инфраструктуры групповой политики.</span><span class="sxs-lookup"><span data-stu-id="54ba4-179">**Installing the UE-V Group Policy ADMX Templates:** Group Policy ADMX templates for UE-V configure the synchronization settings for the UE-V Agent and enable the central management of common UE-V Agent configuration settings by using an existing Group Policy infrastructure.</span></span>

    <span data-ttu-id="54ba4-180">Ниже перечислены поддерживаемые операционные системы для контроллера домена, на котором развертываются объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="54ba4-180">Supported operating systems for the domain controller that deploys the Group Policy Objects include the following:</span></span>

    <span data-ttu-id="54ba4-181">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="54ba4-181">Windows Server 2008 R2</span></span>

    <span data-ttu-id="54ba4-182">Windows Server 2012 и Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="54ba4-182">Windows Server 2012 and Windows Server 2012 R2</span></span>

-   <span data-ttu-id="54ba4-183">[Диспетчер конфигураций](https://technet.microsoft.com/library/dn458917.aspx)**:** пакет конфигурации UE-V позволяет использовать параметры соответствия требованиям компонента System Center Configuration Manager 2012 или более поздней версии для применения согласованных конфигураций на сайтах, где установлены UE-V и Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="54ba4-183">[Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** The UE-V Configuration Pack lets you use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

-   <span data-ttu-id="54ba4-184">[Windows PowerShell и WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** для изменения конфигураций после установки агента UE-V можно использовать команды сценария для Windows PowerShell и инструментария управления Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="54ba4-184">[Windows PowerShell and WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** You can use scripted commands for Windows PowerShell and Windows Management Instrumentation (WMI) to modify configurations after you install the UE-V Agent.</span></span>

    **<span data-ttu-id="54ba4-185">Примечание.</span><span class="sxs-lookup"><span data-stu-id="54ba4-185">Note</span></span>**  
    <span data-ttu-id="54ba4-186">Изменение реестра может привести к потере данных или перестает отвечать на запросы компьютера.</span><span class="sxs-lookup"><span data-stu-id="54ba4-186">Registry modification can result in data loss, or the computer becomes unresponsive.</span></span> <span data-ttu-id="54ba4-187">Мы рекомендуем использовать другие методы настройки.</span><span class="sxs-lookup"><span data-stu-id="54ba4-187">We recommend that you use other configuration methods.</span></span>



-   <span data-ttu-id="54ba4-188">**Установка из командной строки или пакетного сценария:** Параметры, которые используются при [развертывании агента UE-v](#agent) , настройте множество параметров ue-v.</span><span class="sxs-lookup"><span data-stu-id="54ba4-188">**Command-line or Batch Script Installation:** Parameters that are used when you [Deploy the UE-V Agent](#agent) configure many UE-V settings.</span></span> <span data-ttu-id="54ba4-189">Электронные системы распространения программного обеспечения, такие как System Center 2012 Configuration Manager, используют эти параметры для настройки клиентов при развертывании и установке программного обеспечения агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="54ba4-189">Electronic software distribution systems, such as System Center 2012 Configuration Manager, use these parameters to configure their clients when they deploy and install the UE-V Agent software.</span></span>

## <a href="" id="agent"></a><span data-ttu-id="54ba4-190">Развертывание агента UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="54ba4-190">Deploy the UE-V 2.x Agent</span></span>


<span data-ttu-id="54ba4-191">Агент UE-V является ядром развертывания UE-v и должен выполняться на каждом компьютере, использующем UE-V для синхронизации приложений и параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="54ba4-191">The UE-V Agent is the core of a UE-V deployment and must run on each computer that uses UE-V to synchronize application and Windows settings.</span></span>

<span data-ttu-id="54ba4-192">**Установочные файлы агента UE-V:** Один установочный файл, AgentSetup.exe, устанавливает агент UE-V Agent как в 32-, так и в 64-разрядной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="54ba4-192">**UE-V Agent Installation Files:** A single installation file, AgentSetup.exe, installs the UE-V Agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="54ba4-193">Кроме того, предоставляются AgentSetupx86.msiные и AgentSetupx64.msi специфические файлы установщика Windows, а так как они меньше, они могут ускорить развертывание агента.</span><span class="sxs-lookup"><span data-stu-id="54ba4-193">In addition, AgentSetupx86.msi or AgentSetupx64.msi architecture-specific Windows Installer files are provided, and since they are smaller, they might streamline the agent deployments.</span></span> <span data-ttu-id="54ba4-194">[Параметры командной строки для установщика AgentSetup.exe](#params) поддерживаются и для установки установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="54ba4-194">The [command-line parameters for the AgentSetup.exe installer](#params) are supported for the Windows Installer installation as well.</span></span>

**<span data-ttu-id="54ba4-195">Важно.</span><span class="sxs-lookup"><span data-stu-id="54ba4-195">Important</span></span>**  
<span data-ttu-id="54ba4-196">Во время установки или удаления агента UE-V вы можете использовать либо файл AgentSetup.exe, либо &lt; файл Arch AgentSetup &gt; . msi, но не оба варианта.</span><span class="sxs-lookup"><span data-stu-id="54ba4-196">During UE-V Agent installation or uninstallation, you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="54ba4-197">Для удаления агента UE-V, который использовался для установки UE-V Agent, необходимо использовать один и тот же файл.</span><span class="sxs-lookup"><span data-stu-id="54ba4-197">The same file must be used to uninstall the UE-V Agent that was used to install the UE-V Agent.</span></span>



### <span data-ttu-id="54ba4-198">Развертывание агента UE-V</span><span class="sxs-lookup"><span data-stu-id="54ba4-198">To Deploy the UE-V Agent</span></span>

<span data-ttu-id="54ba4-199">Для развертывания агента UE-V можно использовать следующие методы:</span><span class="sxs-lookup"><span data-stu-id="54ba4-199">You can use the following methods to deploy the UE-V Agent:</span></span>

-   <span data-ttu-id="54ba4-200">Система решений для электронного распространения программного обеспечения (ESD), например Configuration Manager, которая может установить файл установщика Windows (MSI).</span><span class="sxs-lookup"><span data-stu-id="54ba4-200">An electronic software distribution (ESD) solution system, such as Configuration Manager, that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="54ba4-201">Сценарий установки, который ссылается на файл установщика Windows (MSI), хранящийся централизованно в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="54ba4-201">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="54ba4-202">Программа установки, запускаемая вручную на компьютере.</span><span class="sxs-lookup"><span data-stu-id="54ba4-202">An installation program that you run manually on the computer.</span></span>

<span data-ttu-id="54ba4-203">Выполните описанные ниже действия, чтобы развернуть агент UE-V из сетевого общего доступа.</span><span class="sxs-lookup"><span data-stu-id="54ba4-203">Use the following procedure to deploy the UE-V Agent from a network share.</span></span>

**<span data-ttu-id="54ba4-204">Установка и настройка агента UE-V для сетевого общего доступа</span><span class="sxs-lookup"><span data-stu-id="54ba4-204">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="54ba4-205">Поэтапный файл установки агента UE-V AgentSetup.exe в сетевой папке, в которую пользователи имеют разрешение на чтение.</span><span class="sxs-lookup"><span data-stu-id="54ba4-205">Stage the UE-V Agent installation file AgentSetup.exe on a network share to which users have Read permission.</span></span>

2.  <span data-ttu-id="54ba4-206">Разверните сценарий на компьютерах пользователей, которые установили агент UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="54ba4-206">Deploy a script to user computers that installs the UE-V Agent.</span></span> <span data-ttu-id="54ba4-207">В сценарии должно быть указано место хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="54ba4-207">The script should specify the settings storage location.</span></span>

<span data-ttu-id="54ba4-208">**Варианты развертывания:** Убедитесь, что при установке агента UE-V используется правильный формат переменной.</span><span class="sxs-lookup"><span data-stu-id="54ba4-208">**Deployment options:** Be sure to use the correct variable format when you install the UE-V Agent.</span></span> <span data-ttu-id="54ba4-209">В таблице ниже приведены примеры параметров развертывания для использования AgentSetup.exe или файлов установщика Windows (MSI).</span><span class="sxs-lookup"><span data-stu-id="54ba4-209">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="54ba4-210">Тип развертывания</span><span class="sxs-lookup"><span data-stu-id="54ba4-210">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="54ba4-211">Описание развертывания</span><span class="sxs-lookup"><span data-stu-id="54ba4-211">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="54ba4-212">Пример.</span><span class="sxs-lookup"><span data-stu-id="54ba4-212">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54ba4-213">Командная строка</span><span class="sxs-lookup"><span data-stu-id="54ba4-213">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-214">При установке агента UE-V в командной строке используйте <em> Формат переменной% ^ username% </em> .</span><span class="sxs-lookup"><span data-stu-id="54ba4-214">When you install the UE-V Agent at a command prompt, use the <em>%^username%</em> variable format.</span></span> <span data-ttu-id="54ba4-215">Если кавычки необходимы из-за пробелов в пути к хранилищу параметров, используйте файл пакетного сценария для развертывания.</span><span class="sxs-lookup"><span data-stu-id="54ba4-215">If quotation marks are required because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54ba4-216">Пакетный сценарий</span><span class="sxs-lookup"><span data-stu-id="54ba4-216">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-217">При установке агента UE-V из пакетного файла сценария используйте <em> Формат переменной%% username%% </em> .</span><span class="sxs-lookup"><span data-stu-id="54ba4-217">When you install the UE-V Agent from a batch script file, use the <em>%%username%%</em> variable format.</span></span> <span data-ttu-id="54ba4-218">Если вы используете этот метод установки, необходимо обменять переменную символом%%.</span><span class="sxs-lookup"><span data-stu-id="54ba4-218">If you use this installation method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="54ba4-219">Без этого символа сценарий разворачивает <em> </em> переменную username во время установки, а не во время выполнения, что приводит к тому, что UE-V использует единое место хранения параметров для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="54ba4-219">Without this character, the script expands the <em>username</em> variable at installation time, rather than at run time, which causes UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54ba4-220">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="54ba4-220">Windows PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-221">При установке агента UE-V из приглашения Windows PowerShell или сценария Windows PowerShell используйте <em> Формат переменной% username% </em> .</span><span class="sxs-lookup"><span data-stu-id="54ba4-221">When you install the UE-V Agent from a Windows PowerShell prompt or a Windows PowerShell script, use the <em>%username%</em> variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54ba4-222">Электронное распространение программного обеспечения, например развертывание программного обеспечения Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="54ba4-222">Electronic software distribution, such as deployment of Configuration Manager Software Deployment</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-223">При установке агента UE-V с помощью Configuration Manager используйте <em> Формат переменной ^% username ^% </em> .</span><span class="sxs-lookup"><span data-stu-id="54ba4-223">When you install the UE-V Agent by using Configuration Manager, use the <em>^%username^%</em> variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="54ba4-224">Примечание.</span><span class="sxs-lookup"><span data-stu-id="54ba4-224">Note</span></span>**  
<span data-ttu-id="54ba4-225">Установка агента UE-V требует наличия прав администратора, и перед запуском агента UE-V требуется перезагрузка компьютера.</span><span class="sxs-lookup"><span data-stu-id="54ba4-225">The installation of the UE-V Agent requires administrator rights, and the computer requires a restart before the UE-V Agent can run.</span></span>



### <a href="" id="params"></a><span data-ttu-id="54ba4-226">Параметры командной строки для развертывания агента UE-V</span><span class="sxs-lookup"><span data-stu-id="54ba4-226">Command-line parameters for UE-V Agent deployment</span></span>

<span data-ttu-id="54ba4-227">Ниже указаны параметры командной строки агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="54ba4-227">The command-line parameters of the UE-V Agent are as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="54ba4-228">Параметр командной строки</span><span class="sxs-lookup"><span data-stu-id="54ba4-228">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="54ba4-229">Определение</span><span class="sxs-lookup"><span data-stu-id="54ba4-229">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="54ba4-230">Заметки</span><span class="sxs-lookup"><span data-stu-id="54ba4-230">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54ba4-231">/Help или/h или/?</span><span class="sxs-lookup"><span data-stu-id="54ba4-231">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-232">Отображает диалоговое окно "использование AgentSetup.exe".</span><span class="sxs-lookup"><span data-stu-id="54ba4-232">Displays the AgentSetup.exe usage dialog box.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54ba4-233">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="54ba4-233">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-234">Указывает путь UNC (Universal Naming Convention), который определяет, где хранятся параметры.</span><span class="sxs-lookup"><span data-stu-id="54ba4-234">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="54ba4-235">Важно.</span><span class="sxs-lookup"><span data-stu-id="54ba4-235">Important</span></span></strong><br/><p><span data-ttu-id="54ba4-236">Необходимо указать SettingsStoragePath в UE-V 2,1 и UE-V 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="54ba4-236">You must specify a SettingsStoragePath in UE-V 2.1 and UE-V 2.1 SP1.</span></span> <span data-ttu-id="54ba4-237">Вы можете задать строку AdHomePath, указывающую на то, что пользователь&#39;s — домашний путь Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54ba4-237">You can set the AdHomePath string to specify that the user&#39;s Active Directory home path is used.</span></span> <span data-ttu-id="54ba4-238">Например, <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span><span class="sxs-lookup"><span data-stu-id="54ba4-238">For example, <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span></span></p>
<p><span data-ttu-id="54ba4-239">В UE-V 2,0 вы можете оставить SettingsStoragePath пустым, чтобы вместо этого использовать домашний путь Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54ba4-239">In UE-V 2.0, you can leave SettingsStoragePath blank to use the Active Directory home path instead.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="54ba4-240">% Username% или% ComputerName% принимают переменные среды.</span><span class="sxs-lookup"><span data-stu-id="54ba4-240">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="54ba4-241">Для сценариев могут потребоваться переменные с экранированием.</span><span class="sxs-lookup"><span data-stu-id="54ba4-241">Scripting can require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="54ba4-242">По умолчанию </strong> : &lt; нет&gt;</span><span class="sxs-lookup"><span data-stu-id="54ba4-242">Default</strong>: &lt;none&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54ba4-243">SettingsStoragePathReg</span><span class="sxs-lookup"><span data-stu-id="54ba4-243">SettingsStoragePathReg</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-244">Получает значение SettingsStoragePath из реестра во время установки.</span><span class="sxs-lookup"><span data-stu-id="54ba4-244">Gets the SettingsStoragePath value from the registry during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-245">В командной строке введите следующий пример, чтобы принудительно использовать в UE-V путь к корневому каталогу Active Directory вместо определенного UNC.</span><span class="sxs-lookup"><span data-stu-id="54ba4-245">At the command prompt, type the following example to force UE-V to use the Active Directory home path instead of a specific UNC.</span></span></p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54ba4-246">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="54ba4-246">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-247">Указывает путь UNC, определяющий расположение, которое было проверено для новых шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="54ba4-247">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-248">Требуется только для шаблонов местоположения настраиваемых параметров</span><span class="sxs-lookup"><span data-stu-id="54ba4-248">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54ba4-249">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="54ba4-249">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-250">Указывает, следует ли регистрировать шаблоны Microsoft по умолчанию во время установки.</span><span class="sxs-lookup"><span data-stu-id="54ba4-250">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-251">Истина | False</span><span class="sxs-lookup"><span data-stu-id="54ba4-251">True | False</span></span></p>
<p><strong><span data-ttu-id="54ba4-252">По умолчанию </strong> : истина</span><span class="sxs-lookup"><span data-stu-id="54ba4-252">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54ba4-253">PowerSchool</span><span class="sxs-lookup"><span data-stu-id="54ba4-253">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-254">Указывает, какой метод синхронизации следует использовать.</span><span class="sxs-lookup"><span data-stu-id="54ba4-254">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-255">SyncProvider | Ничего</span><span class="sxs-lookup"><span data-stu-id="54ba4-255">SyncProvider | None</span></span></p>
<p><strong><span data-ttu-id="54ba4-256">По умолчанию </strong> : SyncProvider</span><span class="sxs-lookup"><span data-stu-id="54ba4-256">Default</strong>: SyncProvider</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54ba4-257">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="54ba4-257">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-258">Указывает время ожидания компьютера (в миллисекундах), по истечении которого из места хранения параметров извлекаются параметры пользователя.</span><span class="sxs-lookup"><span data-stu-id="54ba4-258">Specifies the number of milliseconds that the computer waits before time-out when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="54ba4-259">По умолчанию </strong> : 2000 миллисекунд</span><span class="sxs-lookup"><span data-stu-id="54ba4-259">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="54ba4-260">(подождите до двух секунд)</span><span class="sxs-lookup"><span data-stu-id="54ba4-260">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54ba4-261">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="54ba4-261">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-262">Указывает, включена или отключена синхронизация UE-V.</span><span class="sxs-lookup"><span data-stu-id="54ba4-262">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-263">Истина | False</span><span class="sxs-lookup"><span data-stu-id="54ba4-263">True | False</span></span></p>
<p><strong><span data-ttu-id="54ba4-264">По умолчанию </strong> : истина</span><span class="sxs-lookup"><span data-stu-id="54ba4-264">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54ba4-265">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="54ba4-265">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-266">Задает размер файла пакета параметров в байтах, когда агент UE-V сообщает, что файлы превышают пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="54ba4-266">Specifies a settings package file size in bytes when the UE-V Agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-267">&lt;Емкость&gt;</span><span class="sxs-lookup"><span data-stu-id="54ba4-267">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="54ba4-268">По умолчанию </strong> : нет (порог предупреждения отсутствует)</span><span class="sxs-lookup"><span data-stu-id="54ba4-268">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54ba4-269">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="54ba4-269">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-270">Указывает параметр для участия в программе улучшения качества программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="54ba4-270">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="54ba4-271">Если установлено значение <strong> true </strong> , сведения установщика загружаются на сайт программы улучшения качества программного обеспечения Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="54ba4-271">If set to <strong>True</strong>, installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="54ba4-272">Если задано значение <strong> false </strong> , сведения не передаются.</span><span class="sxs-lookup"><span data-stu-id="54ba4-272">If set to <strong>False</strong>, no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-273">Истина | False</span><span class="sxs-lookup"><span data-stu-id="54ba4-273">True | False</span></span></p>
<p><strong><span data-ttu-id="54ba4-274">По умолчанию </strong> : ложь</span><span class="sxs-lookup"><span data-stu-id="54ba4-274">Default</strong>: False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54ba4-275">Перезапустить</span><span class="sxs-lookup"><span data-stu-id="54ba4-275">NoRestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-276">Поддержка задержки после перезапуска компьютера после установки UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="54ba4-276">Supports deferral of the restart of the computer after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54ba4-277">INSTALLFOLDER</span><span class="sxs-lookup"><span data-stu-id="54ba4-277">INSTALLFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-278">Позволяет настроить другую папку установки для агента UE-V или UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="54ba4-278">Enables a different installation folder to be set for the UE-V Agent or UE-V Generator.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54ba4-279">MUENABLED</span><span class="sxs-lookup"><span data-stu-id="54ba4-279">MUENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-280">Позволяет программе установки принимать параметр, который должен быть включен в программу центра обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="54ba4-280">Enables Setup to accept the option to be included in the Microsoft Update program.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54ba4-281">ACCEPTLICENSETERMS</span><span class="sxs-lookup"><span data-stu-id="54ba4-281">ACCEPTLICENSETERMS</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-282">Позволяет автоматически устанавливать UE-V.</span><span class="sxs-lookup"><span data-stu-id="54ba4-282">Lets UE-V be installed silently.</span></span> <span data-ttu-id="54ba4-283">Это значение должно быть установлено в <strong> true </strong> для автоматической установки UE-v и обойти требование, которое пользователь принимает условия лицензии UE-v.</span><span class="sxs-lookup"><span data-stu-id="54ba4-283">This must be set to <strong>True</strong> to install UE-V silently and bypass the requirement that the user accepts the UE-V license terms.</span></span> <span data-ttu-id="54ba4-284">Если задано значение <strong> false </strong> или оставлено пустым, пользователь получает сообщение об ошибке, а UE-V не установлен.</span><span class="sxs-lookup"><span data-stu-id="54ba4-284">If set to <strong>False</strong> or left empty, the user receives an error message and UE-V is not installed.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="54ba4-285">Важно.</span><span class="sxs-lookup"><span data-stu-id="54ba4-285">Important</span></span></strong><br/><p><span data-ttu-id="54ba4-286">Этот параметр требуется для автоматической установки UE-V.</span><span class="sxs-lookup"><span data-stu-id="54ba4-286">This parameter is required to install UE-V silently.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54ba4-287">Перезапустить</span><span class="sxs-lookup"><span data-stu-id="54ba4-287">NORESTART</span></span></p></td>
<td align="left"><p><span data-ttu-id="54ba4-288">Предотвращает обязательную перезагрузку после установки UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="54ba4-288">Prevents a mandatory restart after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="54ba4-289">Обновление агента UE-V</span><span class="sxs-lookup"><span data-stu-id="54ba4-289">Update the UE-V Agent</span></span>

<span data-ttu-id="54ba4-290">Обновления программного обеспечения агента UE-V предоставляются с помощью центра обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="54ba4-290">Updates for the UE-V Agent software are provided through Microsoft Update.</span></span> <span data-ttu-id="54ba4-291">Обновления агента UE-V можно развертывать с помощью систем инфраструктуры для корпоративного распространения программного обеспечения (ESD).</span><span class="sxs-lookup"><span data-stu-id="54ba4-291">You can deploy UE-V Agent updates by using Enterprise Software Distribution (ESD) infrastructure systems.</span></span>

<span data-ttu-id="54ba4-292">Во время обновления агента UE-V можно обновить стандартную группу шаблонов расположений параметров для приложений Майкрософт и параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="54ba4-292">During a UE-V Agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings can be updated.</span></span>

### <span data-ttu-id="54ba4-293">Обновление агента UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="54ba4-293">Upgrade the UE-V 2.x Agent</span></span>

<span data-ttu-id="54ba4-294">Агент UE-V 2. x предлагает множество новых функций и изменяет способ и время отправки содержимого в общий доступ к хранилищу параметров.</span><span class="sxs-lookup"><span data-stu-id="54ba4-294">The UE-V 2.x Agent introduces many new features and modifies how and when the agent uploads content to the settings storage share.</span></span> <span data-ttu-id="54ba4-295">Эти изменения автоматизируются в процессе обновления.</span><span class="sxs-lookup"><span data-stu-id="54ba4-295">The upgrade process automates these changes.</span></span> <span data-ttu-id="54ba4-296">Чтобы обновить агент UE-V Agent, запустите пакет установки агента UE-V (AgentSetup.exe, AgentSetupx86.msi или AgentSetupx64.msi) на компьютерах пользователей.</span><span class="sxs-lookup"><span data-stu-id="54ba4-296">To upgrade the UE-V Agent, run the UE-V Agent install package (AgentSetup.exe, AgentSetupx86.msi, or AgentSetupx64.msi) on users’ computers.</span></span>

**<span data-ttu-id="54ba4-297">Примечание.</span><span class="sxs-lookup"><span data-stu-id="54ba4-297">Note</span></span>**  
<span data-ttu-id="54ba4-298">При обновлении агента UE-V вы должны использовать один и тот же тип установщика (exe или MSI-пакет), который установил предыдущий агент UE-V.</span><span class="sxs-lookup"><span data-stu-id="54ba4-298">When you upgrade the UE-V Agent, you must use the same installer type (.exe file or .msi packet) that installed the previous UE-V Agent.</span></span> <span data-ttu-id="54ba4-299">Например, чтобы обновить агенты UE-V 1,0, установленные с помощью AgentSetup.exe, используйте UE-V 2 AgentSetup.exe.</span><span class="sxs-lookup"><span data-stu-id="54ba4-299">For example, use the UE-V 2 AgentSetup.exe to upgrade UE-V 1.0 Agents that were installed by using AgentSetup.exe.</span></span>



<span data-ttu-id="54ba4-300">При запуске программы установки агента сохраняются следующие конфигурации:</span><span class="sxs-lookup"><span data-stu-id="54ba4-300">The following configurations are preserved when the Agent Setup program runs:</span></span>

-   <span data-ttu-id="54ba4-301">Путь к хранилищу параметров</span><span class="sxs-lookup"><span data-stu-id="54ba4-301">Settings storage path</span></span>

-   <span data-ttu-id="54ba4-302">Параметры реестра</span><span class="sxs-lookup"><span data-stu-id="54ba4-302">Registry settings</span></span>

-   <span data-ttu-id="54ba4-303">Запланированные задачи (параметры интервалов восстанавливаются по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54ba4-303">Scheduled tasks (Interval settings are reset to their defaults)</span></span>

**<span data-ttu-id="54ba4-304">Примечание.</span><span class="sxs-lookup"><span data-stu-id="54ba4-304">Note</span></span>**  
<span data-ttu-id="54ba4-305">Компьютер с шаблонами расположений параметров UE-V 2. x, которые зарегистрированы в журнале событий Windows агента UE-V 1,0 Register Error.</span><span class="sxs-lookup"><span data-stu-id="54ba4-305">A computer with UE-V 2.x settings location templates that are registered in the UE-V 1.0 Agent register errors in the Windows Event Log.</span></span>



<span data-ttu-id="54ba4-306">Вы можете автоматизировать и распространить обновление агента UE-V с помощью Microsoft System Center 2012 Configuration Manager или другого средства распространения корпоративного программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="54ba4-306">You can use Microsoft System Center 2012 Configuration Manager or another enterprise software distribution tool to automate and distribute the UE-V Agent upgrade.</span></span>

<span data-ttu-id="54ba4-307">**Рекомендации:** Мы рекомендуем вам обновить все агенты UE-V 1,0 в вычислительной среде, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="54ba4-307">**Recommendations:** We recommend that you upgrade all of the UE-V 1.0 Agents in a computing environment, but it is not required.</span></span> <span data-ttu-id="54ba4-308">Шаблоны расположений параметров UE-V 2. x могут взаимодействовать с агентом UE-V 1,0, так как они имеют доступ только к параметрам в пути к хранилищу параметров.</span><span class="sxs-lookup"><span data-stu-id="54ba4-308">UE-V 2.x settings location templates can interact with a UE-V 1.0 Agent because they only share the settings from the settings storage path.</span></span> <span data-ttu-id="54ba4-309">Однако мы рекомендуем переносить развертывания на одну версию агента для упрощения управления и поддержки UE-V.</span><span class="sxs-lookup"><span data-stu-id="54ba4-309">We recommend, however, that you move the deployments to a single agent version to simplify management and to support UE-V.</span></span>

### <span data-ttu-id="54ba4-310">Восстановление агента UE-V после неудачного обновления</span><span class="sxs-lookup"><span data-stu-id="54ba4-310">Repair the UE-V Agent after an unsuccessful upgrade</span></span>

<span data-ttu-id="54ba4-311">При попытке выполнения одной из указанных ниже операций могут возникать ошибки.</span><span class="sxs-lookup"><span data-stu-id="54ba4-311">You might experience errors after you attempt one of the following operations:</span></span>

-   <span data-ttu-id="54ba4-312">Переход с UE-V 1,0 на UE-V 2</span><span class="sxs-lookup"><span data-stu-id="54ba4-312">Upgrade from UE-V 1.0 to UE-V 2</span></span>

-   <span data-ttu-id="54ba4-313">Переход на более новую версию Windows (например, с Windows 7 на Windows 8 или Windows 8 на Windows 8,1).</span><span class="sxs-lookup"><span data-stu-id="54ba4-313">Upgrade to a newer version of Windows, for example, from Windows 7 to Windows 8 or from Windows 8 to Windows 8.1.</span></span>

-   <span data-ttu-id="54ba4-314">Удаление агента после обновления агента UE-V Agent</span><span class="sxs-lookup"><span data-stu-id="54ba4-314">Uninstall the agent after upgrading the UE-V Agent</span></span>

<span data-ttu-id="54ba4-315">Для устранения проблем попробуйте восстановить агент UE-V, введя эту команду в командной строке на компьютере, на котором установлен агент.</span><span class="sxs-lookup"><span data-stu-id="54ba4-315">To resolve any issues, attempt to repair the UE-V Agent by entering this command at a command prompt on the computer where the agent is installed.</span></span>

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

<span data-ttu-id="54ba4-316">Затем вы можете повторить процесс удаления или обновить, установив более новую версию агента UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="54ba4-316">You can then retry the uninstall process or upgrade by installing the newer version of the UE-V Agent.</span></span>






## <span data-ttu-id="54ba4-317">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="54ba4-317">Related topics</span></span>


[<span data-ttu-id="54ba4-318">Подготовка к развертыванию UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="54ba4-318">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="54ba4-319">Развертывание UE-V 2. x для настраиваемых приложений</span><span class="sxs-lookup"><span data-stu-id="54ba4-319">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)









