---
title: Пошаговое руководство по средству расширенного управления групповыми политиками Майкрософт2.5
description: Пошаговое руководство по средству расширенного управления групповыми политиками Майкрософт2.5
author: dansimp
ms.assetid: 454298c9-0fab-497a-9808-c0246a4c8db5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 67925e417e4fb1f5398dfd030f366936f1d36909
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820192"
---
# <span data-ttu-id="78a3d-103">Пошаговое руководство по средству расширенного управления групповыми политиками Майкрософт2.5</span><span class="sxs-lookup"><span data-stu-id="78a3d-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 2.5</span></span>


<span data-ttu-id="78a3d-104">В этом пошаговом руководстве показаны сложные методики управления групповыми политиками с помощью консоли управления групповыми политиками (GPMC) и расширенного управления групповыми политиками Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="78a3d-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="78a3d-105">Функция расширенного управления групповыми политиками расширяет возможности GPMC, обеспечивая:</span><span class="sxs-lookup"><span data-stu-id="78a3d-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="78a3d-106">Стандартные роли для делегирования разрешений на управление объектами групповой политики (GPO) нескольким администраторам групповых политик.</span><span class="sxs-lookup"><span data-stu-id="78a3d-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators.</span></span>

-   <span data-ttu-id="78a3d-107">Архивация, позволяющая администраторам групповых политик создавать и изменять GPO в автономном режиме, прежде чем развертывать их в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="78a3d-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="78a3d-108">Возможность вернуться к предыдущей версии GPO.</span><span class="sxs-lookup"><span data-stu-id="78a3d-108">The ability to roll back to any previous version of a GPO.</span></span>

-   <span data-ttu-id="78a3d-109">Возможность возврата и извлечения для GPO, чтобы убедиться, что администраторы групповых политик не случайно перезаписывают работу друг друга.</span><span class="sxs-lookup"><span data-stu-id="78a3d-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="78a3d-110">Общие сведения о сценарии РАСШИРЕНного использования функций</span><span class="sxs-lookup"><span data-stu-id="78a3d-110">AGPM scenario overview</span></span>


<span data-ttu-id="78a3d-111">В этом сценарии для каждой роли в разделе управления ГРУППОВыми политиками используется отдельная учетная запись, в которой показано, как можно управлять групповой политикой в среде с несколькими администраторами групповой политики с разными уровнями разрешений.</span><span class="sxs-lookup"><span data-stu-id="78a3d-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="78a3d-112">В частности, вы будете выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="78a3d-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="78a3d-113">Используя учетную запись, которая входит в группу "Администраторы домена", установите сервер доменных групп и назначьте роль администратора РАСШИРЕНной учетной записи или группе.</span><span class="sxs-lookup"><span data-stu-id="78a3d-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="78a3d-114">Используя учетные записи, которым будут назначаться роли для РАСШИРЕНного использования функций, установите Клиентская политика</span><span class="sxs-lookup"><span data-stu-id="78a3d-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="78a3d-115">Используя учетную запись с ролью администратора РАСШИРЕНного доступа к данным, настройте для них доступ к объектам групповой политики, назначив им роли другие учетные записи.</span><span class="sxs-lookup"><span data-stu-id="78a3d-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="78a3d-116">Используя учетную запись с ролью редактора, запросите создание объекта групповой политики, которое затем утверждается с помощью учетной записи с ролью утверждающего.</span><span class="sxs-lookup"><span data-stu-id="78a3d-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="78a3d-117">С помощью учетной записи редактора извлеките объект групповой политики из архива, измените объект групповой политики, установите для него флажок в архив и запросите развертывание.</span><span class="sxs-lookup"><span data-stu-id="78a3d-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="78a3d-118">С помощью учетной записи, в которой находится роль утверждающего, изучите объект групповой политики и разверните его в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="78a3d-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="78a3d-119">С помощью учетной записи, в которой находится роль редактора, создайте шаблон GPO и используйте его в качестве отправной точки для создания нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="78a3d-120">С помощью учетной записи, в которой находится роль утверждающего, удалите и восстановите объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![процесс разработки объектов групповой политики](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="78a3d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="78a3d-122">Requirements</span></span>


<span data-ttu-id="78a3d-123">Компьютеры, на которых вы хотите установить многопользовательскую версию, должны удовлетворять следующим требованиям, и вы должны создать учетные записи для использования в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="78a3d-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

### <span data-ttu-id="78a3d-124">Требования к серверу для РАСШИРЕНного сервера</span><span class="sxs-lookup"><span data-stu-id="78a3d-124">AGPM Server requirements</span></span>

<span data-ttu-id="78a3d-125">Для сервера управления групповыми политиками (WindowsVista) требуется® (32-разрядная версия) без установленного пакета обновления или Windows Server® 2003 (32-bit версия), а также GPMC.</span><span class="sxs-lookup"><span data-stu-id="78a3d-125">AGPM Server2.5 requires WindowsVista® (32-bit version) with no service packs installed or Windows Server®2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="78a3d-126">Кроме того, вы должны входить в группу администраторов домена, чтобы установить сервер доменных групп с РАСШИРЕНным набором элементов.</span><span class="sxs-lookup"><span data-stu-id="78a3d-126">Additionally, you must be a member of the Domain Admins group to install AGPM Server.</span></span>

<span data-ttu-id="78a3d-127">На рядовом сервере или контроллере домена необходимо установить сервер расширенного управления групповыми политиками с последней версией GPMC и поддерживаться с помощью функции РАСШИРЕНного доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="78a3d-127">You should install AGPM Server on a member server or domain controller with the most recent version of the GPMC that is available to you and supported by AGPM.</span></span> <span data-ttu-id="78a3d-128">Функция РАСШИРЕНного управления групповыми политиками использует GPMC для резервного копирования и восстановления объектов групповой политики, а новые версии GPMC предоставляют дополнительные параметры политики, недоступные в предыдущих версиях.</span><span class="sxs-lookup"><span data-stu-id="78a3d-128">AGPM uses the GPMC to back up and restore GPOs, and newer versions of the GPMC provide additional policy settings not available in preceding versions.</span></span> <span data-ttu-id="78a3d-129">Если версия GPMC на сервере управления ГРУППОВыми политиками старше, чем версия на компьютерах, используемых администраторами для управления групповой политикой, сервер управления ГРУППОВыми политиками не сможет сохранить эти параметры политики, недоступные в более ранней версии GPMC.</span><span class="sxs-lookup"><span data-stu-id="78a3d-129">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store those policy settings not available in the older version of the GPMC.</span></span>

<span data-ttu-id="78a3d-130">В частности, если на сервере управления групповыми политиками установлена операционная система Windows server2003 и версия GPMC, сопровождающая его, а на компьютерах администраторов групповых политик запущены WindowsVista и версия GPMC, которая сопровождает ее, вы все равно можете управлять большинством параметров политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-130">Specifically, if your AGPM Server is running Windows Server2003 and the version of the GPMC that accompanied it, and your Group Policy administrators’ computers are running WindowsVista and the version of the GPMC that accompanied it, you can still manage most policy settings.</span></span> <span data-ttu-id="78a3d-131">Тем не менее, параметры политики из консоли управления групповыми политиками в Windows Vista, недоступные в консоли управления групповыми политиками в Windows Server 2003 (например, связанные с перенаправлением папок, беспроводные сети (IEEE 802,11) и развернутыми принтерами, не могут храниться на компьютере, даже если администраторы могут настроить их с помощью РАСШИРЕНного использования функций на компьютерах.</span><span class="sxs-lookup"><span data-stu-id="78a3d-131">However, policy settings from the GPMC in Windows Vista that are not available in the GPMC in Windows Server 2003—such as those related to folder redirection, wireless networking (IEEE 802.11), and deployed printers—cannot be stored by the AGPM Server, even though administrators can configure them using AGPM on their computers.</span></span>

<span data-ttu-id="78a3d-132">Если вы хотите установить на компьютере с более ранней версией GPMC, чем администраторы групповой политики, ознакомьтесь с подробными сведениями о том, какие параметры политики доступны для всех операционных систем, в справке по параметрам групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-132">If you must install AGPM Server on a computer with an older version of GPMC than your Group Policy administrators are running, see the Group Policy Settings Reference for details about which policy settings are available with which operating systems.</span></span> <span data-ttu-id="78a3d-133">Сведения о том, как загрузить ссылку на параметры групповой политики, можно найти в разделе <https://go.microsoft.com/fwlink/?LinkID=106147> .</span><span class="sxs-lookup"><span data-stu-id="78a3d-133">To download the Group Policy Settings Reference, see <https://go.microsoft.com/fwlink/?LinkID=106147>.</span></span>

<span data-ttu-id="78a3d-134">**Примечание**  Архивы не могут быть перенесены с сервера РАСШИРЕНного использования или сервера GPOVault под управлением Windows server2003 на сервер, на котором запущены WindowsVista.</span><span class="sxs-lookup"><span data-stu-id="78a3d-134">**Note** Archives cannot be migrated from an AGPM Server or a GPOVault Server running Windows Server2003 to an AGPM Server running WindowsVista.</span></span>

<span data-ttu-id="78a3d-135">Для Windows server2003, если на компьютере, на котором вы хотите установить сервер многоязыкового РАСШИРЕНного обновления, установлен сервер GPOVault, рекомендуется не удалять GPOVault сервер перед началом установки.</span><span class="sxs-lookup"><span data-stu-id="78a3d-135">For Windows Server2003, if GPOVault Server is installed on the computer on which you want to install AGPM Server, it is recommended that you do not uninstall GPOVault Server before beginning the installation.</span></span> <span data-ttu-id="78a3d-136">При установке сервера с РАСШИРЕНным учетным GPOVault сервер удаляется и автоматически переносятся из существующих GPOVault архивных данных в архив с РАСШИРЕНными учетными данными.</span><span class="sxs-lookup"><span data-stu-id="78a3d-136">The installation of AGPM Server will uninstall GPOVault Server and automatically transfer your existing GPOVault archive data to an AGPM archive.</span></span>

 

### <span data-ttu-id="78a3d-137">Требования клиента к РАСШИРЕНным требованиям</span><span class="sxs-lookup"><span data-stu-id="78a3d-137">AGPM Client requirements</span></span>

<span data-ttu-id="78a3d-138">Клиентская система управления групповыми политиками требует WindowsVista (32-разрядная версия) без установленного пакета обновления или Windows server2003 (32-разрядная версия), а также консоли управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="78a3d-138">AGPM Client2.5 requires WindowsVista (32-bit version) with no service packs installed or Windows Server2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="78a3d-139">Клиент с расширенным управлением групповыми политиками можно установить на компьютер, на котором установлен сервер разсети</span><span class="sxs-lookup"><span data-stu-id="78a3d-139">AGPM Client can be installed on a computer running AGPM Server.</span></span>

### <span data-ttu-id="78a3d-140">Требования к сценарию</span><span class="sxs-lookup"><span data-stu-id="78a3d-140">Scenario requirements</span></span>

<span data-ttu-id="78a3d-141">Перед тем как приступить к созданию этого сценария, создайте четыре учетных записи пользователей.</span><span class="sxs-lookup"><span data-stu-id="78a3d-141">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="78a3d-142">Во время сценария вы будете назначать одну из следующих ролей РАСШИРЕНного управления правами на доступ каждому из этих учетных записей: администратор РАСШИРЕНного доступа (полный доступ), утверждающий, редактор и рецензент.</span><span class="sxs-lookup"><span data-stu-id="78a3d-142">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="78a3d-143">Эти учетные записи должны быть доступны для отправки и получения сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="78a3d-143">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="78a3d-144">Назначьте разрешения на доступ к **объектам GPO** для учетных записей с помощью администратора расширенного доступа к данным, утверждающего и (необязательно), ролей редактора.</span><span class="sxs-lookup"><span data-stu-id="78a3d-144">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="78a3d-145">**Примечание** 
 Разрешение " **связывание объектов GPO** " назначается членам группы администраторов домена и администраторов предприятия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="78a3d-145">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="78a3d-146">Чтобы назначить разрешение на доступ к **GPO** для дополнительных пользователей или групп (например, учетные записи с ролями администратора или утверждающего), щелкните узел **домена, а**затем откройте вкладку **Делегирование** , нажмите кнопку **Добавить**, а затем выберите пункт Пользователи или группы, которым нужно назначить разрешение.</span><span class="sxs-lookup"><span data-stu-id="78a3d-146">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

<span data-ttu-id="78a3d-147">В этом сценарии действия выполняются с разными учетными записями.</span><span class="sxs-lookup"><span data-stu-id="78a3d-147">For this scenario, you perform actions with different accounts.</span></span> <span data-ttu-id="78a3d-148">Вы можете войти в систему с каждой учетной записью, а также с помощью команды " **выполнить как** ", чтобы запустить GPMC с указанной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="78a3d-148">You can either log on with each account as indicated, or you can use the **Run as** command to start the GPMC with the indicated account.</span></span>

<span data-ttu-id="78a3d-149">**Примечание**  Чтобы использовать команду " **выполнить как** " с помощью GPMC в Windows server2003, нажмите кнопку **Пуск**, выберите пункты **Администрирование** **, щелкните правой**кнопкой мыши и выберите команду **Запуск от имени**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-149">**Note** To use the **Run as** command with GPMC on Windows Server2003, click **Start**, point to **Administrative Tools**, right-click **Group Policy Management**, and click **Run as**.</span></span> <span data-ttu-id="78a3d-150">Щелкните **следующего пользователя** и введите учетные данные для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="78a3d-150">Click **The following user** and enter credentials for an account.</span></span>

<span data-ttu-id="78a3d-151">Чтобы использовать команду **Запуск от имени** в консоли управления групповыми политиками в Windows Vista, нажмите кнопку **Пуск** , наведите указатель на пункт **выполнить**и введите **runas/user:** <em> DomainName\\UserName </em> **"MMC%WINDIR%\\system32\\gpmc.msc"**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-151">To use the **Run as** command with GPMC on Windows Vista, click the **Start** button, point to **Run**, and type **runas /user:**<em>DomainName\\UserName</em>**"mmc %windir%\\system32\\gpmc.msc"**, and click **OK**.</span></span> <span data-ttu-id="78a3d-152">При появлении соответствующего запроса введите пароль для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="78a3d-152">Type the password for the account when prompted.</span></span>

 

## <span data-ttu-id="78a3d-153">Инструкции по установке и настройке РАСШИРЕНного изменения параметров</span><span class="sxs-lookup"><span data-stu-id="78a3d-153">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="78a3d-154">Чтобы установить и настроить параметры РАСШИРЕНного конфигурирования, необходимо выполнить описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="78a3d-154">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="78a3d-155">Шаг 1: Установка сервера РАСШИРЕНного набора элементов</span><span class="sxs-lookup"><span data-stu-id="78a3d-155">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="78a3d-156">Шаг 2. Установка клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="78a3d-156">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="78a3d-157">Шаг 3: Настройка подключения к серверу с РАСШИРЕНным интерфейсом</span><span class="sxs-lookup"><span data-stu-id="78a3d-157">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="78a3d-158">Шаг 4: Настройка уведомления по электронной почте</span><span class="sxs-lookup"><span data-stu-id="78a3d-158">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="78a3d-159">Шаг 5: передача прав доступа</span><span class="sxs-lookup"><span data-stu-id="78a3d-159">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="78a3d-160">Шаг 1: Установка сервера РАСШИРЕНного набора элементов</span><span class="sxs-lookup"><span data-stu-id="78a3d-160">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="78a3d-161">На этом этапе необходимо установить сервер РАСШИРЕНного управления правами на рядовом сервере или контроллере домена, который будет запускать службу расширенного управления групповыми политиками, и настроить этот архив.</span><span class="sxs-lookup"><span data-stu-id="78a3d-161">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="78a3d-162">Все операции РАСШИРЕНного управления правами обрабатываются в этой службе Windows и выполняются с учетными данными службы.</span><span class="sxs-lookup"><span data-stu-id="78a3d-162">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="78a3d-163">Архивация, управляемая сервером расширенного управления групповыми политиками, может быть размещена на этом сервере или на другом сервере в том же лесе.</span><span class="sxs-lookup"><span data-stu-id="78a3d-163">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="78a3d-164">Установка сервера расширенного управления групповыми политиками на компьютере, на котором будет размещена служба РАСШИРЕНного управления</span><span class="sxs-lookup"><span data-stu-id="78a3d-164">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="78a3d-165">Войдите в систему под учетной записью, которая входит в группу "Администраторы домена".</span><span class="sxs-lookup"><span data-stu-id="78a3d-165">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="78a3d-166">Запустите компакт-диск с пакетом оптимизации рабочей среды Microsoft и следуйте инструкциям на экране, чтобы выбрать **Расширенное управление групповыми политиками — сервер**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-166">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="78a3d-167">В диалоговом окне **Добро пожаловать** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-167">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="78a3d-168">В диалоговом окне **условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт** подтвердите условия и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-168">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="78a3d-169">В диалоговом окне **путь к приложению** выберите расположение, в которое нужно установить сервер расширенного набора.</span><span class="sxs-lookup"><span data-stu-id="78a3d-169">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="78a3d-170">На компьютере, на котором установлен сервер расширенного управления групповыми политиками, будет размещена служба и Управление архивом.</span><span class="sxs-lookup"><span data-stu-id="78a3d-170">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="78a3d-171">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-171">Click **Next**.</span></span>

6.  <span data-ttu-id="78a3d-172">В диалоговом окне **Архивировать путь** выберите расположение для архива относительно сервера расширенного поиска.</span><span class="sxs-lookup"><span data-stu-id="78a3d-172">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="78a3d-173">Путь к архиву может указывать на папку на сервере расширенного управления групповыми политиками или в другом месте, но необходимо выбрать расположение, в котором достаточно свободного места для хранения всех объектов групповой политики и данных журнала, управляемых этим сервером управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="78a3d-173">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="78a3d-174">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-174">Click **Next**.</span></span>

7.  <span data-ttu-id="78a3d-175">В диалоговом окне **учетная запись службы расширенного** выбора параметров выберите учетную запись службы, под которой будет выполняться служба расширенного выбора и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-175">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="78a3d-176">В диалоговом окне **Владелец архива** выберите учетную запись или группу, которой необходимо назначить роль администратора расширенного доступа (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="78a3d-176">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="78a3d-177">Этот администратор может назначать роли и разрешения РАСШИРЕНного доступа другим администраторам групповой политики (в том числе к роли администратора РАСШИРЕНного доступа к данным).</span><span class="sxs-lookup"><span data-stu-id="78a3d-177">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="78a3d-178">Для этого сценария выберите учетную запись, которая будет использоваться в роли администратора РАСШИРЕНного администрирования.</span><span class="sxs-lookup"><span data-stu-id="78a3d-178">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="78a3d-179">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-179">Click **Next**.</span></span>

9.  <span data-ttu-id="78a3d-180">Нажмите кнопку **установить**, а затем — **Готово** , чтобы завершить работу мастера установки.</span><span class="sxs-lookup"><span data-stu-id="78a3d-180">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="78a3d-181">**Внимание!**  Не изменяйте параметры службы РАСШИРЕНного **управления правами с помощью средств администрирования** и **служб** в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="78a3d-181">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="78a3d-182">Это может привести к невозможности запуска службы РАСШИРЕНного настольных служб.</span><span class="sxs-lookup"><span data-stu-id="78a3d-182">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="78a3d-183">Сведения о том, как изменить параметры службы, приведены в разделе Справка по расширенному управлению групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="78a3d-183">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="78a3d-184">Шаг 2. Установка клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="78a3d-184">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="78a3d-185">Каждый администратор групповой политики — любой пользователь, который создает, редактирует, развертывает или удаляет GPO, должен установить на компьютеры, которые они используют, для управления объектами групповой политики, клиент с РАСШИРЕНными правами.</span><span class="sxs-lookup"><span data-stu-id="78a3d-185">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="78a3d-186">Для этого сценария необходимо установить клиентская версия с РАСШИРЕНным Управлением по крайней мере на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="78a3d-186">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="78a3d-187">На компьютерах конечных пользователей, которые не выполняют администрирование групповой политики, вам не нужно устанавливать клиент с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="78a3d-187">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="78a3d-188">Установка клиента с расширенным управлением групповыми политиками на компьютере администратора групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-188">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="78a3d-189">Запустите компакт-диск с пакетом оптимизации рабочей среды Microsoft и следуйте инструкциям на экране, чтобы выбрать **Расширенное управление групповыми политиками — клиент**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-189">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="78a3d-190">В диалоговом окне **Добро пожаловать** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-190">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="78a3d-191">В диалоговом окне **условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт** подтвердите условия и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-191">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="78a3d-192">В диалоговом окне **путь к приложению** выберите расположение для установки клиента с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="78a3d-192">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="78a3d-193">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-193">Click **Next**.</span></span>

5.  <span data-ttu-id="78a3d-194">В диалоговом окне **сервер с расширенным** управлением разкрывающимся списком введите полное имя компьютера и порт для сервера расширенного выбора ключа, к которому нужно подключиться.</span><span class="sxs-lookup"><span data-stu-id="78a3d-194">In the **AGPM Server** dialog box, type the fully-qualified computer name and the port for the AGPM Server to which to connect.</span></span> <span data-ttu-id="78a3d-195">Портом по умолчанию для службы РАСШИРЕНного обслуживания не является 4600.</span><span class="sxs-lookup"><span data-stu-id="78a3d-195">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="78a3d-196">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-196">Click **Next**.</span></span>

6.  <span data-ttu-id="78a3d-197">Нажмите кнопку **установить**, а затем — **Готово** , чтобы завершить работу мастера установки.</span><span class="sxs-lookup"><span data-stu-id="78a3d-197">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="78a3d-198">Шаг 3: Настройка подключения к серверу с РАСШИРЕНным интерфейсом</span><span class="sxs-lookup"><span data-stu-id="78a3d-198">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="78a3d-199">В разделе управления ГРУППОВыми политиками сохраняются все версии всех управляемых объектов групповой политики (GPO), для которых Управление изменениями обеспечивается в центральном архиве, поэтому администраторы групповой политики могут просматривать и изменять GPO в автономном режиме без немедленного воздействия на развернутую версию каждого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-199">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="78a3d-200">На этом этапе необходимо настроить соединение с сервером РАСШИРЕНного администрирования и убедиться, что все администраторы групповой политики подключаются к одному и тому же серверу.</span><span class="sxs-lookup"><span data-stu-id="78a3d-200">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="78a3d-201">(Дополнительные сведения о настройке нескольких серверов РАСШИРЕНной конфигурации см. в разделе Справка по расширенному управлению групповыми политиками.)</span><span class="sxs-lookup"><span data-stu-id="78a3d-201">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="78a3d-202">Настройка подключения к серверу РАСШИРЕНного конфигурирования для всех администраторов групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-202">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="78a3d-203">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которую выбрали в качестве владельца архива.</span><span class="sxs-lookup"><span data-stu-id="78a3d-203">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="78a3d-204">У этого пользователя есть роль администратора управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="78a3d-204">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="78a3d-205">Нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем — **Управление групповой политикой** , чтобы открыть консоль управления групповыми **политиками (GPMC)**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-205">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the **Group Policy Management Console (GPMC)**.</span></span>

3.  <span data-ttu-id="78a3d-206">В дереве **консоли управления групповыми политиками** измените объект групповой политики, который применяется ко всем администраторам групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-206">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="78a3d-207">В окне " **Редактор объектов групповой политики** " выберите " **Конфигурация пользователя**", " **Административные шаблоны**" и " **компоненты Windows**".</span><span class="sxs-lookup"><span data-stu-id="78a3d-207">In the **Group Policy Object Editor** window, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

5.  <span data-ttu-id="78a3d-208">Если в разделе **компоненты Windows**отсутствует **Расширенное** руководство, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="78a3d-208">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="78a3d-209">Щелкните правой кнопкой мыши **Административные шаблоны** и выберите команду **Добавить или удалить шаблоны**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-209">Right-click **Administrative Templates** and select **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="78a3d-210">Нажмите кнопку **Добавить**, выберите элемент **расширенного формата ADMX** или для **расширенного**расширения (ADM), нажмите кнопку **Открыть**, а затем — **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-210">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

6.  <span data-ttu-id="78a3d-211">В разделе **компоненты Windows**дважды щелкните элемент **расширенной**учетной записью.</span><span class="sxs-lookup"><span data-stu-id="78a3d-211">Under **Windows Components**, double-click **AGPM**.</span></span>

7.  <span data-ttu-id="78a3d-212">В области сведений дважды щелкните **сервер расширенного доменных данных (все домены)**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-212">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

8.  <span data-ttu-id="78a3d-213">В окне **свойств сервера (все домены)** для настольных компьютеров выберите параметр **включено** и введите полное имя и порт (например, Server.contoso.com:4600) для сервера, на котором размещается Архив.</span><span class="sxs-lookup"><span data-stu-id="78a3d-213">In the **AGPM Server (all domains) Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, server.contoso.com:4600) for the server hosting the archive.</span></span> <span data-ttu-id="78a3d-214">Портом, используемым службой РАСШИРЕНного поиска, является порт 4600.</span><span class="sxs-lookup"><span data-stu-id="78a3d-214">The port used by the AGPM Service is port 4600.</span></span>

9.  <span data-ttu-id="78a3d-215">Нажмите кнопку **ОК**, а затем закройте окно **редактора объектов групповой политики** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-215">Click **OK**, and then close the **Group Policy Object Editor** window.</span></span> <span data-ttu-id="78a3d-216">После обновления групповой политики соединение с сервером РАСШИРЕНного политики для каждого администратора будет настроено.</span><span class="sxs-lookup"><span data-stu-id="78a3d-216">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="78a3d-217">Шаг 4: Настройка уведомления по электронной почте</span><span class="sxs-lookup"><span data-stu-id="78a3d-217">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="78a3d-218">Как Администратор расширенного управления групповыми политиками (полный доступ) вы указываете адреса электронной почты утверждающих и администраторов РАСШИРЕНного доступа, которым будет отправлено сообщение электронной почты с запросом, когда редактор попытается создать, развернуть или удалить объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-218">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="78a3d-219">Кроме того, вы можете определить псевдоним, из которого отправляются эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="78a3d-219">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="78a3d-220">Настройка уведомления по электронной почте для РАСШИРЕНного</span><span class="sxs-lookup"><span data-stu-id="78a3d-220">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="78a3d-221">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-221">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="78a3d-222">В области сведений откройте вкладку **Делегирование домена** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-222">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="78a3d-223">В поле **от** введите псевдоним электронной почты для расширенного ключа, из которого нужно отправить уведомления.</span><span class="sxs-lookup"><span data-stu-id="78a3d-223">In the **From** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="78a3d-224">В поле **Кому** введите адрес электронной почты учетной записи пользователя, которому вы хотите назначить роль утверждающего.</span><span class="sxs-lookup"><span data-stu-id="78a3d-224">In the **To** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="78a3d-225">В поле **SMTP-сервер** введите допустимый почтовый SMTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="78a3d-225">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="78a3d-226">В полях **имя пользователя** и **пароль** введите учетные данные пользователя, у которого есть доступ к службе SMTP.</span><span class="sxs-lookup"><span data-stu-id="78a3d-226">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="78a3d-227">Нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-227">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="78a3d-228">Шаг 5: передача прав доступа</span><span class="sxs-lookup"><span data-stu-id="78a3d-228">Step 5: Delegate access</span></span>

<span data-ttu-id="78a3d-229">Как Администратор расширенного управления групповыми политиками (режим полного доступа) вы делегируйте доступ к объектам GPO на уровне домена, назначая роли учетной записи каждого администратора групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-229">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="78a3d-230">**Примечание**  Вы также можете делегировать доступ на уровне объекта групповой политики, а не на уровне домена.</span><span class="sxs-lookup"><span data-stu-id="78a3d-230">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="78a3d-231">Подробные сведения можно найти в разделе Справка по расширенному управлению групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="78a3d-231">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="78a3d-232">**Важно!**  Вы должны ограничивать членство в группе "владельцы" владельца групповой политики, поэтому ее нельзя использовать для обхода управления доступом к GPO.</span><span class="sxs-lookup"><span data-stu-id="78a3d-232">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="78a3d-233">(В **консоли управления групповыми политиками**щелкните **объекты групповой политики** в лесу и домене, в которых вы хотите управлять объектами GPO, выберите пункт **Делегирование**и настройте параметры в соответствии с потребностями Организации.)</span><span class="sxs-lookup"><span data-stu-id="78a3d-233">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="78a3d-234">Передача доступа ко всем объектам групповой политики внутри домена</span><span class="sxs-lookup"><span data-stu-id="78a3d-234">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="78a3d-235">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-235">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="78a3d-236">На вкладке **доменное делегирование** нажмите кнопку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-236">On the **Domain Delegation** tab, click the **Advanced** button.</span></span>

3.  <span data-ttu-id="78a3d-237">В диалоговом окне " **разрешения** " сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="78a3d-237">In the **Permissions** dialog box:</span></span>

    1.  <span data-ttu-id="78a3d-238">Выберите учетную запись администратора групповой политики, а затем установите флажок **утверждающий** , чтобы назначить эту роль учетной записи.</span><span class="sxs-lookup"><span data-stu-id="78a3d-238">Click the user account of a Group Policy administrator, and then select the **Approver** check box to assign that role to the account.</span></span> <span data-ttu-id="78a3d-239">Снимите флажок " **Редактор** ".</span><span class="sxs-lookup"><span data-stu-id="78a3d-239">Clear the **Editor** check box.</span></span> <span data-ttu-id="78a3d-240">(Эта роль включает в себя роль проверяющего.)</span><span class="sxs-lookup"><span data-stu-id="78a3d-240">(This role includes the Reviewer role.)</span></span>

    2.  <span data-ttu-id="78a3d-241">Выберите учетную запись другого администратора групповой политики, а затем установите флажок **Редактор** , чтобы назначить эту роль учетной записи.</span><span class="sxs-lookup"><span data-stu-id="78a3d-241">Click the user account of another Group Policy administrator, and then select the **Editor** check box to assign that role to the account.</span></span> <span data-ttu-id="78a3d-242">(Эта роль включает в себя роль проверяющего.)</span><span class="sxs-lookup"><span data-stu-id="78a3d-242">(This role includes the Reviewer role.)</span></span>

    3.  <span data-ttu-id="78a3d-243">Выберите третью учетную запись, а затем установите флажок **рецензент** , чтобы назначить только роль рецензента учетной записи администратора групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-243">Click a third account and then select the **Reviewer** check box to assign only the Reviewer role to the account of that Group Policy administrator.</span></span> <span data-ttu-id="78a3d-244">Снимите флажок " **Редактор** ".</span><span class="sxs-lookup"><span data-stu-id="78a3d-244">Clear the **Editor** check box.</span></span>

    4.  <span data-ttu-id="78a3d-245">Нажмите кнопку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-245">Click the **Advanced** button.</span></span>

4.  <span data-ttu-id="78a3d-246">В диалоговом окне **Дополнительные параметры безопасности** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="78a3d-246">In the **Advanced Security Settings** dialog box:</span></span>

    1.  <span data-ttu-id="78a3d-247">Выберите администратора групповой политики и нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-247">Select a Group Policy administrator, and then click **Edit**.</span></span>

    2.  <span data-ttu-id="78a3d-248">В поле **Применить**выберите **этот объект и вложенные объекты**, а затем нажмите кнопку **ОК** в диалоговом окне **запись** **разрешения** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-248">For **Apply onto**, select **This object and nested objects**, and then click **OK** in the **Permission** **Entry** dialog box.</span></span>

    3.  <span data-ttu-id="78a3d-249">Повторите эти действия для каждого администратора групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-249">Repeat for each Group Policy administrator.</span></span>

5.  <span data-ttu-id="78a3d-250">В диалоговом окне **Дополнительные параметры безопасности** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-250">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

6.  <span data-ttu-id="78a3d-251">В диалоговом окне **разрешения** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-251">In the **Permissions** dialog box, click **OK**.</span></span>

## <span data-ttu-id="78a3d-252">Инструкции по управлению объектами групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-252">Steps for managing GPOs</span></span>


<span data-ttu-id="78a3d-253">Для создания, изменения, проверки и развертывания объектов групповой политики с помощью РАСШИРЕНного использования функций необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="78a3d-253">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="78a3d-254">Кроме того, вы создадите шаблон, удалите объект групповой политики и восстановите удаленный объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-254">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="78a3d-255">Действие 1: создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-255">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="78a3d-256">Действие 2: изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-256">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="78a3d-257">Шаг 3: Проверка и развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-257">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="78a3d-258">Шаг 4: использование шаблона для создания объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-258">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="78a3d-259">Шаг 5: удаление и восстановление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-259">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="78a3d-260">Действие 1: создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-260">Step 1: Create a GPO</span></span>

<span data-ttu-id="78a3d-261">В среде с несколькими администраторами групповой политики у пользователей с ролью "редактор" есть возможность запросить создание новых объектов GPO, но такой запрос должен быть утвержден участником роли утверждающего, поскольку создание нового объекта групповой политики влияет на производственную среду.</span><span class="sxs-lookup"><span data-stu-id="78a3d-261">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="78a3d-262">На этом этапе вы используете учетную запись с ролью "редактор" для запроса создания нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-262">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="78a3d-263">С помощью учетной записи, в которой находится роль утверждающего, вы утверждаете этот запрос и завершаете создание объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-263">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="78a3d-264">Запрос на создание нового объекта групповой политики, управляемого с помощью расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="78a3d-264">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="78a3d-265">На компьютере, на котором установлен клиент с РАСШИРЕНным управлением правами, войдите в систему с помощью учетной записи пользователя, которой назначена роль "редактор" в расширенном управлении учетными записями.</span><span class="sxs-lookup"><span data-stu-id="78a3d-265">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="78a3d-266">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-266">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="78a3d-267">Щелкните правой кнопкой мыши узел **контроль изменений** и выберите команду **создать управляемый объект групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-267">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="78a3d-268">В диалоговом окне **новый управляемый объект групповой политики** :</span><span class="sxs-lookup"><span data-stu-id="78a3d-268">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="78a3d-269">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-269">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="78a3d-270">Введите **MyGPO** в качестве имени нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-270">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="78a3d-271">Введите Примечание для нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-271">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="78a3d-272">Нажмите кнопку **создать Live** , чтобы новый объект групповой политики был развернут в рабочей среде сразу после утверждения.</span><span class="sxs-lookup"><span data-stu-id="78a3d-272">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="78a3d-273">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-273">Click **Submit**.</span></span>

5.  <span data-ttu-id="78a3d-274">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-274">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="78a3d-275">Новый объект групповой политики появится на вкладке **ожидающие** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-275">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="78a3d-276">Утверждение ожидающего запроса на создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-276">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="78a3d-277">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которой назначена роль утверждающего в РАСШИРЕНном.</span><span class="sxs-lookup"><span data-stu-id="78a3d-277">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="78a3d-278">Откройте папку "Входящие" электронной почты для учетной записи и обратите внимание на то, что вы получили сообщение электронной почты от псевдонима с помощью запроса редактора, чтобы создать объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-278">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="78a3d-279">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-279">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="78a3d-280">На вкладке **содержание** откройте вкладку **ожидается** , чтобы отобразить ожидающие GPO.</span><span class="sxs-lookup"><span data-stu-id="78a3d-280">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="78a3d-281">Щелкните правой кнопкой мыши **MyGPO**и выберите команду **утвердить**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-281">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="78a3d-282">Нажмите кнопку **Да** , чтобы подтвердить утверждение создания объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-282">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="78a3d-283">Объект групповой политики перемещается на вкладку **Управление** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-283">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="78a3d-284">Действие 2: изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-284">Step 2: Edit a GPO</span></span>

<span data-ttu-id="78a3d-285">С помощью объектов групповой политики можно настраивать параметры компьютера или пользователя и развертывать их на нескольких компьютерах или в других пользователей.</span><span class="sxs-lookup"><span data-stu-id="78a3d-285">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="78a3d-286">На этом этапе вы используете учетную запись с ролью "редактор" для извлечения GPO из архива, изменения GPO в автономном режиме, проверки GPO в архиве и запроса развертывания объекта групповой политики в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="78a3d-286">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="78a3d-287">В этом сценарии вы можете настроить параметр в объекте групповой политики таким образом, чтобы пароль имел длину не менее восьми символов.</span><span class="sxs-lookup"><span data-stu-id="78a3d-287">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="78a3d-288">Извлечение GPO из архива для редактирования</span><span class="sxs-lookup"><span data-stu-id="78a3d-288">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="78a3d-289">На компьютере, на котором установлен клиент с РАСШИРЕНным управлением правами, войдите в систему с помощью учетной записи пользователя, которой назначена роль редактора в РАСШИРЕНном наборе данных.</span><span class="sxs-lookup"><span data-stu-id="78a3d-289">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="78a3d-290">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-290">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="78a3d-291">На вкладке **содержание** в области сведений откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-291">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="78a3d-292">Щелкните правой кнопкой мыши **MyGPO**и выберите пункт **извлечь.**</span><span class="sxs-lookup"><span data-stu-id="78a3d-292">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="78a3d-293">Введите Примечание, которое будет отображаться в **истории** объекта групповой политики, когда он извлечен, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-293">Type a comment to be displayed in the **History** of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="78a3d-294">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-294">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="78a3d-295">На вкладке **Управление** состоянием GPO считается **извлеченным**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-295">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="78a3d-296">Изменение GPO в автономном режиме и Настройка минимальной длины пароля</span><span class="sxs-lookup"><span data-stu-id="78a3d-296">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="78a3d-297">На вкладке **Управление** , щелкните правой кнопкой мыши **MyGPO**и выберите команду **изменить** , чтобы открыть окно **редактора объектов групповой политики** и внести изменения в автономную копию GPO.</span><span class="sxs-lookup"><span data-stu-id="78a3d-297">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="78a3d-298">Для этого сценария настройте минимальную длину пароля:</span><span class="sxs-lookup"><span data-stu-id="78a3d-298">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="78a3d-299">В разделе **Конфигурация компьютера**дважды щелкните элемент **Параметры Windows**, дважды щелкните значок **Параметры безопасности**, дважды щелкните элемент **политики учетных записей**и дважды щелкните пункт **Политика паролей**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-299">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Password Policy**.</span></span>

    2.  <span data-ttu-id="78a3d-300">В области сведений дважды щелкните элемент **Минимальная длина пароля**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-300">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="78a3d-301">В окне "Свойства" установите флажок **определить этот параметр политики** , укажите число символов **8**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-301">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="78a3d-302">Закройте окно **редактора объектов групповой политики** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-302">Close the **Group Policy Object Editor** window.</span></span>

**<span data-ttu-id="78a3d-303">Проверка GPO в архиве</span><span class="sxs-lookup"><span data-stu-id="78a3d-303">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="78a3d-304">На вкладке **Управление** , щелкните правой кнопкой мыши **MyGPO** и выберите команду **вернуть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-304">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="78a3d-305">Введите примечание и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-305">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="78a3d-306">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-306">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="78a3d-307">На вкладке **Управление** состоянием объекта групповой политики считается **возвращенное**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-307">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="78a3d-308">Запрос развертывания объекта групповой политики в рабочей среде</span><span class="sxs-lookup"><span data-stu-id="78a3d-308">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="78a3d-309">На вкладке **Управление** , щелкните правой кнопкой мыши **MyGPO** и выберите команду **развернуть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-309">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="78a3d-310">Поскольку эта учетная запись не является администратором утверждения или РАСШИРЕНного администрирования, необходимо отправить запрос на развертывание.</span><span class="sxs-lookup"><span data-stu-id="78a3d-310">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="78a3d-311">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-311">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="78a3d-312">Введите Примечание, которое будет отображаться в **журнале** объекта групповой политики, а затем нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-312">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="78a3d-313">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-313">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="78a3d-314">**MyGPO** отображается в списке объектов групповой политики на вкладке **ожидающие** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-314">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="78a3d-315">Шаг 3: Проверка и развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-315">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="78a3d-316">На этом этапе вы действуете как утверждающий, создавая отчеты и анализируя параметры и изменяя параметры в объекте групповой политики, чтобы определить, нужно ли их утверждать.</span><span class="sxs-lookup"><span data-stu-id="78a3d-316">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="78a3d-317">После того как вы выберете объект групповой политики, вы развернете его в производственную среду и свяжите его с доменом или подразделением (OU), чтобы оно запустилось при обновлении групповой политики для компьютеров в этом домене или OU.</span><span class="sxs-lookup"><span data-stu-id="78a3d-317">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="78a3d-318">Просмотр параметров в объекте групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-318">To review settings in the GPO</span></span>**

1.  <span data-ttu-id="78a3d-319">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которой назначена роль утверждающего в РАСШИРЕНном.</span><span class="sxs-lookup"><span data-stu-id="78a3d-319">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="78a3d-320">(Любой администратор групповой политики с ролью рецензента, включенный во все другие роли, может просматривать параметры в объекте групповой политики.)</span><span class="sxs-lookup"><span data-stu-id="78a3d-320">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2.  <span data-ttu-id="78a3d-321">Откройте папку "Входящие" электронной почты для учетной записи и обратите внимание на то, что вы получили сообщение электронной почты от псевдонима РАСШИРЕНного использования запроса редактора для развертывания объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-321">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3.  <span data-ttu-id="78a3d-322">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="78a3d-323">На вкладке **содержание** в области сведений откройте вкладку **ожидается** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-323">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5.  <span data-ttu-id="78a3d-324">Дважды щелкните **MyGPO** , чтобы отобразить историю.</span><span class="sxs-lookup"><span data-stu-id="78a3d-324">Double-click **MyGPO** to display its history.</span></span>

6.  <span data-ttu-id="78a3d-325">Проверьте параметры в последней версии MyGPO:</span><span class="sxs-lookup"><span data-stu-id="78a3d-325">Review the settings in the most recent version of MyGPO:</span></span>

    1.  <span data-ttu-id="78a3d-326">В окне " **Журнал** " щелкните правой кнопкой мыши версию объекта групповой политики с последней меткой времени, выберите пункт **Параметры**, а затем — **отчет HTML** , чтобы отобразить сводку по параметрам объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-326">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

    2.  <span data-ttu-id="78a3d-327">В веб-браузере нажмите кнопку **Показать все** , чтобы отобразить все параметры в объекте групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-327">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span>

    3.  <span data-ttu-id="78a3d-328">Закройте браузер.</span><span class="sxs-lookup"><span data-stu-id="78a3d-328">Close the browser.</span></span>

7.  <span data-ttu-id="78a3d-329">Сравните последнюю версию MyGPO с первой версией, возвращенной в Архив:</span><span class="sxs-lookup"><span data-stu-id="78a3d-329">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

    1.  <span data-ttu-id="78a3d-330">В окне " **Журнал** " выберите версию объекта групповой политики с самой последней отметкой времени.</span><span class="sxs-lookup"><span data-stu-id="78a3d-330">In the **History** window, click the GPO version with the most recent timestamp.</span></span> <span data-ttu-id="78a3d-331">Нажмите клавишу **CTRL** и щелкните самую старую версию объекта групповой политики, которая находится в состоянии " **возвращено**".</span><span class="sxs-lookup"><span data-stu-id="78a3d-331">Press **CTRL** and click the oldest GPO version that has a state of **Checked In**.</span></span>

    2.  <span data-ttu-id="78a3d-332">Нажмите кнопку **различия** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-332">Click the **Differences** button.</span></span> <span data-ttu-id="78a3d-333">Раздел **политики учетных записей и политика паролей** выделены зеленым цветом и предшествует **\ [+ \]**, что указывает на то, что этот параметр настроен только в последней версии GPO.</span><span class="sxs-lookup"><span data-stu-id="78a3d-333">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

    3.  <span data-ttu-id="78a3d-334">Выберите политики **учетных записей и политика паролей**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-334">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="78a3d-335">Параметр **минимальной длины пароля** также выделяется зеленым цветом и предшествует **\ [+ \]**, что указывает на то, что оно настроено только в последней версии GPO.</span><span class="sxs-lookup"><span data-stu-id="78a3d-335">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

    4.  <span data-ttu-id="78a3d-336">Закройте веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="78a3d-336">Close the Web browser.</span></span>

**<span data-ttu-id="78a3d-337">Развертывание объекта групповой политики в рабочей среде</span><span class="sxs-lookup"><span data-stu-id="78a3d-337">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="78a3d-338">На вкладке **Ожидание** щелкните правой кнопкой мыши **MyGPO** и выберите команду **утвердить**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-338">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="78a3d-339">Введите Примечание для включения в историю объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-339">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="78a3d-340">Щелкните **Да**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-340">Click **Yes**.</span></span> <span data-ttu-id="78a3d-341">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-341">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="78a3d-342">Объект групповой политики развернут в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="78a3d-342">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="78a3d-343">Связывание объекта групповой политики с доменом или подразделением</span><span class="sxs-lookup"><span data-stu-id="78a3d-343">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="78a3d-344">В консоли управления групповыми политиками щелкните правой кнопкой мыши домен или подразделение, к которому вы хотите применить настраиваемый объект групповой политики, а затем выберите команду **связать существующий объект групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-344">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="78a3d-345">В диалоговом окне **Выбор объекта групповой политики** щелкните **MyGPO**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-345">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="78a3d-346">Шаг 4: использование шаблона для создания объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-346">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="78a3d-347">На этом этапе вы используете учетную запись с ролью "редактор", чтобы создать шаблон — нередактируемую статическую версию GPO для использования в качестве отправной точки для создания новых объектов групповой политики, а затем Создай новый объект групповой политики на основе этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="78a3d-347">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="78a3d-348">Шаблоны полезны для быстрого создания нескольких GPO, включающих множество одинаковых параметров.</span><span class="sxs-lookup"><span data-stu-id="78a3d-348">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="78a3d-349">Создание шаблона на основе существующего объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-349">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="78a3d-350">На компьютере, на котором установлен клиент с РАСШИРЕНным управлением правами, войдите в систему с помощью учетной записи пользователя, которой назначена роль редактора в РАСШИРЕНном наборе данных.</span><span class="sxs-lookup"><span data-stu-id="78a3d-350">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="78a3d-351">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-351">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="78a3d-352">На вкладке **содержание** в области сведений откройте вкладку **Управление** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-352">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="78a3d-353">Щелкните правой кнопкой мыши **MyGPO**и выберите команду **Сохранить как шаблон** , чтобы создать шаблон, включающий все параметры, в настоящее время находящиеся в MyGPO.</span><span class="sxs-lookup"><span data-stu-id="78a3d-353">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="78a3d-354">Введите **MyTemplate** в качестве имени шаблона и примечания, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-354">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="78a3d-355">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-355">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="78a3d-356">Новый шаблон появится на вкладке **шаблоны** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-356">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="78a3d-357">Запрос на создание нового объекта групповой политики, управляемого с помощью расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="78a3d-357">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="78a3d-358">Откройте вкладку **Управление** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-358">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="78a3d-359">Щелкните правой кнопкой мыши узел **контроль изменений** и выберите команду **создать управляемый объект групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-359">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="78a3d-360">В диалоговом окне **новый управляемый объект групповой политики** :</span><span class="sxs-lookup"><span data-stu-id="78a3d-360">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="78a3d-361">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-361">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="78a3d-362">Введите **MyOtherGPO** в качестве имени нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-362">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="78a3d-363">Введите Примечание для нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-363">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="78a3d-364">Нажмите кнопку **создать в реальном времени**, чтобы новый объект групповой политики был развернут в рабочей среде сразу после утверждения.</span><span class="sxs-lookup"><span data-stu-id="78a3d-364">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="78a3d-365">**В шаблоне из GPO**выберите **MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-365">For **From GPO template**, select **MyTemplate**.</span></span>

    6.  <span data-ttu-id="78a3d-366">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-366">Click **Submit**.</span></span>

4.  <span data-ttu-id="78a3d-367">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-367">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="78a3d-368">Новый объект групповой политики появится на вкладке **ожидающие** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-368">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="78a3d-369">Используйте учетную запись, которой назначена роль утверждающего, чтобы утвердить ожидающий запрос на создание объекта групповой политики, как на [этапе 1: Создайте объект групповой политики](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="78a3d-369">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="78a3d-370">MyTemplate все параметры, настроенные в MyGPO.</span><span class="sxs-lookup"><span data-stu-id="78a3d-370">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="78a3d-371">Поскольку MyOtherGPO был создан с помощью MyTemplate, он первоначально содержит все параметры, MyGPO содержащиеся на момент создания MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="78a3d-371">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="78a3d-372">Чтобы подтвердить это, вы можете создать отчет о разнице, чтобы сравнить MyOtherGPO с MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="78a3d-372">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="78a3d-373">Извлечение GPO из архива для редактирования</span><span class="sxs-lookup"><span data-stu-id="78a3d-373">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="78a3d-374">На компьютере, на котором установлен клиент с РАСШИРЕНным управлением правами, войдите в систему с помощью учетной записи пользователя, которой назначена роль редактора в РАСШИРЕНном наборе данных.</span><span class="sxs-lookup"><span data-stu-id="78a3d-374">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="78a3d-375">Щелкните правой кнопкой мыши **MyOtherGPO**и выберите пункт **извлечь.**</span><span class="sxs-lookup"><span data-stu-id="78a3d-375">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="78a3d-376">Введите Примечание, которое будет отображаться в истории объекта групповой политики, когда он извлечен, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-376">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="78a3d-377">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-377">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="78a3d-378">На вкладке **Управление** состоянием GPO считается **извлеченным**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-378">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="78a3d-379">Изменение GPO в автономном режиме и Настройка длительности блокировки учетной записи</span><span class="sxs-lookup"><span data-stu-id="78a3d-379">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="78a3d-380">На вкладке **Управление** , щелкните правой кнопкой мыши **MyOtherGPO**и выберите команду **изменить** , чтобы открыть окно **редактора объектов групповой политики** и внести изменения в автономную копию GPO.</span><span class="sxs-lookup"><span data-stu-id="78a3d-380">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="78a3d-381">Для этого сценария настройте минимальную длину пароля:</span><span class="sxs-lookup"><span data-stu-id="78a3d-381">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="78a3d-382">В разделе **Конфигурация компьютера**дважды щелкните элемент **Параметры Windows**, дважды щелкните элемент **Параметры безопасности**, дважды щелкните политики **учетных записей**и дважды щелкните **политику блокировки учетных записей**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-382">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="78a3d-383">В области сведений дважды щелкните **Продолжительность блокировки учетной записи**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-383">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="78a3d-384">В окне "Свойства" установите флажок **задать этот параметр политики**, задайте для параметра продолжительность **30** минут и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-384">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="78a3d-385">Закройте окно **редактора объектов групповой политики** .</span><span class="sxs-lookup"><span data-stu-id="78a3d-385">Close the **Group Policy Object Editor** window.</span></span>

<span data-ttu-id="78a3d-386">Проверьте MyOtherGPO в архиве и запросите развертывание в том виде, в котором вы делали в MyGPO на [этапе 2. Измените объект групповой политики](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="78a3d-386">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="78a3d-387">Вы можете сравнить MyOtherGPO с MyGPO или с MyTemplate с помощью отчетов о различиях.</span><span class="sxs-lookup"><span data-stu-id="78a3d-387">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="78a3d-388">Любая учетная запись, включающая в себя роль рецензента (Управление групповыми политиками \ [полный доступ \], утверждающая, редактор или рецензент), может создавать отчеты.</span><span class="sxs-lookup"><span data-stu-id="78a3d-388">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="78a3d-389">Сравнение GPO с другим GPO и с шаблоном</span><span class="sxs-lookup"><span data-stu-id="78a3d-389">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="78a3d-390">Чтобы сравнить MyGPO и MyOtherGPO, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="78a3d-390">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="78a3d-391">На вкладке **Управление** нажмите кнопку **MyGPO**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-391">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="78a3d-392">Нажмите клавишу **CTRL** , а затем — **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-392">Press **CTRL** and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="78a3d-393">Щелкните правой кнопкой мыши **MyOtherGPO**, наведите указатель на пункт **отличия**и выберите пункт **отчет в формате HTML**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-393">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="78a3d-394">Чтобы сравнить MyOtherGPO и MyTemplate, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="78a3d-394">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="78a3d-395">На вкладке **Управление** нажмите кнопку **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-395">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="78a3d-396">Щелкните правой кнопкой мыши **MyOtherGPO**, наведите указатель на пункт **отличия**и выберите пункт **шаблон**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-396">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="78a3d-397">Выберите **MyTemplate** и **HTML-отчет**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-397">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="78a3d-398">Шаг 5: удаление и восстановление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-398">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="78a3d-399">На этом этапе вы действуете как утверждающий для удаления GPO.</span><span class="sxs-lookup"><span data-stu-id="78a3d-399">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="78a3d-400">Удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-400">To delete a GPO</span></span>**

1.  <span data-ttu-id="78a3d-401">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которой назначена роль утверждающего.</span><span class="sxs-lookup"><span data-stu-id="78a3d-401">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="78a3d-402">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-402">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="78a3d-403">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-403">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="78a3d-404">Щелкните правой кнопкой мыши **MyGPO**и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-404">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="78a3d-405">Выберите команду **удалить объект групповой политики из архива и производства** , чтобы удалить версию в архиве, а также версию объекта групповой политики, развернутую в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="78a3d-405">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="78a3d-406">Введите Примечание, которое будет отображаться в контрольной записи для объекта групповой политики, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-406">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="78a3d-407">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-407">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="78a3d-408">Объект групповой политики удаляется с вкладки " **управляемые** " и отображается на вкладке " **Корзина** ", в которой ее можно восстановить или уничтожить.</span><span class="sxs-lookup"><span data-stu-id="78a3d-408">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="78a3d-409">Иногда вы обнаружите, что после удаления объекта групповой политики он по-прежнему нужен.</span><span class="sxs-lookup"><span data-stu-id="78a3d-409">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="78a3d-410">На этом этапе вы выступаете в качестве утверждающего для восстановления удаляемого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-410">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="78a3d-411">Восстановление удаленного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="78a3d-411">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="78a3d-412">На вкладке " **содержимое** " щелкните вкладку " **Корзина** ", чтобы отобразить удаленные GPO.</span><span class="sxs-lookup"><span data-stu-id="78a3d-412">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="78a3d-413">Щелкните правой кнопкой мыши **MyGPO**и выберите команду **восстановить**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-413">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="78a3d-414">Введите Примечание, которое будет отображаться в журнале объекта групповой политики, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-414">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="78a3d-415">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-415">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="78a3d-416">Объект групповой политики удаляется из вкладки " **Корзина** " и отображается на вкладке " **управляемые** ".</span><span class="sxs-lookup"><span data-stu-id="78a3d-416">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="78a3d-417">**Примечание**  Восстановление GPO в архиве не приводит к его повторному развертыванию в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="78a3d-417">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="78a3d-418">Чтобы вернуть GPO в производственную среду, разверните объект групповой политики, как на [шаге 3: Проверка и развертывание объекта групповой политики](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="78a3d-418">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="78a3d-419">После изменения и развертывания объекта групповой политики, возможно, вы обнаружите, что последние изменения в объекте групповой политики приводят к возникновению проблемы.</span><span class="sxs-lookup"><span data-stu-id="78a3d-419">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="78a3d-420">На этом этапе вы выполняете роль утверждающего, чтобы вернуться к предыдущей версии GPO.</span><span class="sxs-lookup"><span data-stu-id="78a3d-420">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="78a3d-421">Вы можете вернуться к любой версии в истории объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-421">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="78a3d-422">С помощью примечаний и подписей вы можете определить известные хорошие версии и внести определенные изменения.</span><span class="sxs-lookup"><span data-stu-id="78a3d-422">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="78a3d-423">Чтобы вернуться к предыдущей версии GPO,</span><span class="sxs-lookup"><span data-stu-id="78a3d-423">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="78a3d-424">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="78a3d-424">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="78a3d-425">Дважды щелкните **MyGPO** , чтобы отобразить историю.</span><span class="sxs-lookup"><span data-stu-id="78a3d-425">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="78a3d-426">Щелкните правой кнопкой мыши версию, которую нужно развернуть, и выберите команду **развернуть**, а затем — **Да**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-426">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="78a3d-427">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-427">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="78a3d-428">В окне **журнала** нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-428">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="78a3d-429">**Примечание**  Чтобы убедиться в том, что версия, которая была повторно обновлена, предназначена для версии, проверьте отчет о различиях для двух версий.</span><span class="sxs-lookup"><span data-stu-id="78a3d-429">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="78a3d-430">В окне **журнала** для объекта групповой политики выберите две версии, щелкните их правой кнопкой мыши, наведите указатель на пункт **разница**и выберите **отчет HTML** или **отчет XML**.</span><span class="sxs-lookup"><span data-stu-id="78a3d-430">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





