---
title: Пошаговое руководство по средству расширенного управления групповыми политиками Майкрософт3.0
description: Пошаговое руководство по средству расширенного управления групповыми политиками Майкрософт3.0
author: dansimp
ms.assetid: d067f465-d7c8-4f6d-b311-66b9b06874f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b4efa5075027e99a3e50a344aafcdf6f6f69a147
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818329"
---
# <span data-ttu-id="9b302-103">Пошаговое руководство по средству расширенного управления групповыми политиками Майкрософт3.0</span><span class="sxs-lookup"><span data-stu-id="9b302-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="9b302-104">В этом пошаговом руководстве показаны сложные методики управления групповыми политиками с помощью консоли управления групповыми политиками (GPMC) и расширенного управления групповыми политиками Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="9b302-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="9b302-105">Функция расширенного управления групповыми политиками расширяет возможности GPMC, обеспечивая:</span><span class="sxs-lookup"><span data-stu-id="9b302-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="9b302-106">Стандартные роли для делегирования разрешений на управление объектами групповой политики (GPO) нескольким администраторам групповой политики, а также возможность делегирования доступа к GPO в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="9b302-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators, as well as the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="9b302-107">Архивация, позволяющая администраторам групповых политик создавать и изменять GPO в автономном режиме, прежде чем развертывать их в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="9b302-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="9b302-108">Возможность вернуться к предыдущей версии GPO в архиве и ограничить количество версий, сохраненных в архиве.</span><span class="sxs-lookup"><span data-stu-id="9b302-108">The ability to roll back to any previous version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="9b302-109">Возможность возврата и извлечения для GPO, чтобы убедиться, что администраторы групповых политик не случайно перезаписывают работу друг друга.</span><span class="sxs-lookup"><span data-stu-id="9b302-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="9b302-110">Общие сведения о сценарии РАСШИРЕНного использования функций</span><span class="sxs-lookup"><span data-stu-id="9b302-110">AGPM scenario overview</span></span>


<span data-ttu-id="9b302-111">В этом сценарии для каждой роли в разделе управления ГРУППОВыми политиками используется отдельная учетная запись, в которой показано, как можно управлять групповой политикой в среде с несколькими администраторами групповой политики с разными уровнями разрешений.</span><span class="sxs-lookup"><span data-stu-id="9b302-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="9b302-112">В частности, вы будете выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="9b302-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="9b302-113">Используя учетную запись, которая входит в группу "Администраторы домена", установите сервер доменных групп и назначьте роль администратора РАСШИРЕНной учетной записи или группе.</span><span class="sxs-lookup"><span data-stu-id="9b302-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="9b302-114">Используя учетные записи, которым будут назначаться роли для РАСШИРЕНного использования функций, установите Клиентская политика</span><span class="sxs-lookup"><span data-stu-id="9b302-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="9b302-115">Используя учетную запись с ролью администратора РАСШИРЕНного доступа к данным, настройте для них доступ к объектам групповой политики, назначив им роли другие учетные записи.</span><span class="sxs-lookup"><span data-stu-id="9b302-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="9b302-116">Используя учетную запись с ролью редактора, запросите создание объекта групповой политики, которое затем утверждается с помощью учетной записи с ролью утверждающего.</span><span class="sxs-lookup"><span data-stu-id="9b302-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="9b302-117">С помощью учетной записи редактора извлеките объект групповой политики из архива, измените объект групповой политики, установите для него флажок в архив и запросите развертывание.</span><span class="sxs-lookup"><span data-stu-id="9b302-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="9b302-118">С помощью учетной записи, в которой находится роль утверждающего, изучите объект групповой политики и разверните его в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="9b302-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="9b302-119">С помощью учетной записи, в которой находится роль редактора, создайте шаблон GPO и используйте его в качестве отправной точки для создания нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="9b302-120">С помощью учетной записи, в которой находится роль утверждающего, удалите и восстановите объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![процесс разработки объектов групповой политики](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="9b302-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9b302-122">Requirements</span></span>


<span data-ttu-id="9b302-123">Компьютеры, на которых вы хотите установить многопользовательскую версию, должны удовлетворять следующим требованиям, и вы должны создать учетные записи для использования в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="9b302-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="9b302-124">**Примечание**  Если вы установили компонент РАСШИРЕНной версии 2,5 и пытаетесь перейти с Windows Server® 2003 на Windows Server2008 или WindowsVista® без установленного пакета обновления для WindowsVista с Pack1 службы, необходимо обновить операционную систему, прежде чем вы сможете выполнить обновление до версии РАСШИРЕНного сервера.</span><span class="sxs-lookup"><span data-stu-id="9b302-124">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008 or WindowsVista® with no service packs installed to WindowsVista with Service Pack1, you must upgrade the operating system before you can upgrade to AGPM3.0.</span></span>

 

### <span data-ttu-id="9b302-125">Требования к серверу для РАСШИРЕНного сервера</span><span class="sxs-lookup"><span data-stu-id="9b302-125">AGPM Server requirements</span></span>

<span data-ttu-id="9b302-126">Для сервера управления групповыми политиками (RAS) версии 3.0 требуется Windows Server2008 или WindowsVista с Pack1 службы и консоль GPMC из средств удаленного администрирования сервера (RSAT).</span><span class="sxs-lookup"><span data-stu-id="9b302-126">AGPM Server3.0 requires Windows Server2008 or WindowsVista with Service Pack1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="9b302-127">Поддерживаются как 32, так и 64-разрядные версии.</span><span class="sxs-lookup"><span data-stu-id="9b302-127">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="9b302-128">Перед установкой сервера РАСШИРЕНного доменных прав необходимо быть членом группы администраторов домена и следующими функциями Windows, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="9b302-128">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="9b302-129">ПОЛИТИКОЙ</span><span class="sxs-lookup"><span data-stu-id="9b302-129">GPMC</span></span>

    -   <span data-ttu-id="9b302-130">Windows Server 2008: консоль GPMC автоматически устанавливается с помощью расширенного управления групповыми политиками, если оно отсутствует.</span><span class="sxs-lookup"><span data-stu-id="9b302-130">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="9b302-131">Windows Vista: перед установкой многоэлементного управления групповыми политиками необходимо установить GPMC из RSAT.</span><span class="sxs-lookup"><span data-stu-id="9b302-131">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="9b302-132">Дополнительные сведения можно найти в разделе <https://go.microsoft.com/fwlink/?LinkID=116179> .</span><span class="sxs-lookup"><span data-stu-id="9b302-132">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="9b302-133">.NET Framework 3.5</span><span class="sxs-lookup"><span data-stu-id="9b302-133">.NET Framework 3.5</span></span>

<span data-ttu-id="9b302-134">Следующие компоненты Windows необходимы для сервера РАСШИРЕНного отслеживания и будут автоматически установлены, если их нет:</span><span class="sxs-lookup"><span data-stu-id="9b302-134">The following Windows features are required by AGPM Server and will be automatically installed if not present:</span></span>

-   <span data-ttu-id="9b302-135">Активация WCF; Активация не по протоколу HTTP</span><span class="sxs-lookup"><span data-stu-id="9b302-135">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="9b302-136">Служба активации процессов Windows</span><span class="sxs-lookup"><span data-stu-id="9b302-136">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="9b302-137">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="9b302-137">Process Model</span></span>

    -   <span data-ttu-id="9b302-138">Среда .NET</span><span class="sxs-lookup"><span data-stu-id="9b302-138">.NET Environment</span></span>

    -   <span data-ttu-id="9b302-139">API конфигурации</span><span class="sxs-lookup"><span data-stu-id="9b302-139">Configuration APIs</span></span>

### <span data-ttu-id="9b302-140">Требования клиента к РАСШИРЕНным требованиям</span><span class="sxs-lookup"><span data-stu-id="9b302-140">AGPM Client requirements</span></span>

<span data-ttu-id="9b302-141">Для клиента с расширенными учетными таблицами управления групповыми политиками требуется Windows Server2008 или WindowsVista с пакетом обновления 1 и консоль GPMC из средств удаленного администрирования сервера (RSAT).</span><span class="sxs-lookup"><span data-stu-id="9b302-141">AGPM Client3.0 requires Windows Server2008 or WindowsVista with Service Pack 1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="9b302-142">Поддерживаются как 32, так и 64-разрядные версии.</span><span class="sxs-lookup"><span data-stu-id="9b302-142">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="9b302-143">Клиент с расширенным управлением групповыми политиками можно установить на компьютер, на котором установлен сервер разсети</span><span class="sxs-lookup"><span data-stu-id="9b302-143">AGPM Client can be installed on a computer running AGPM Server.</span></span>

<span data-ttu-id="9b302-144">Следующие возможности Windows необходимы клиенту с помощью РАСШИРЕНного отслеживания и будут автоматически установлены, если не указано иное:</span><span class="sxs-lookup"><span data-stu-id="9b302-144">The following Windows features are required by AGPM Client and will be automatically installed if not present unless otherwise noted:</span></span>

-   <span data-ttu-id="9b302-145">ПОЛИТИКОЙ</span><span class="sxs-lookup"><span data-stu-id="9b302-145">GPMC</span></span>

    -   <span data-ttu-id="9b302-146">Windows Server 2008: консоль GPMC автоматически устанавливается с помощью расширенного управления групповыми политиками, если оно отсутствует.</span><span class="sxs-lookup"><span data-stu-id="9b302-146">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="9b302-147">Windows Vista: перед установкой многоэлементного управления групповыми политиками необходимо установить GPMC из RSAT.</span><span class="sxs-lookup"><span data-stu-id="9b302-147">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="9b302-148">Дополнительные сведения можно найти в разделе <https://go.microsoft.com/fwlink/?LinkID=116179> .</span><span class="sxs-lookup"><span data-stu-id="9b302-148">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="9b302-149">.NET Framework 3,0</span><span class="sxs-lookup"><span data-stu-id="9b302-149">.NET Framework 3.0</span></span>

### <span data-ttu-id="9b302-150">Требования к сценарию</span><span class="sxs-lookup"><span data-stu-id="9b302-150">Scenario requirements</span></span>

<span data-ttu-id="9b302-151">Перед тем как приступить к созданию этого сценария, создайте четыре учетных записи пользователей.</span><span class="sxs-lookup"><span data-stu-id="9b302-151">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="9b302-152">Во время сценария вы будете назначать одну из следующих ролей РАСШИРЕНного управления правами на доступ каждому из этих учетных записей: администратор РАСШИРЕНного доступа (полный доступ), утверждающий, редактор и рецензент.</span><span class="sxs-lookup"><span data-stu-id="9b302-152">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="9b302-153">Эти учетные записи должны быть доступны для отправки и получения сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9b302-153">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="9b302-154">Назначьте разрешения на доступ к **объектам GPO** для учетных записей с помощью администратора расширенного доступа к данным, утверждающего и (необязательно), ролей редактора.</span><span class="sxs-lookup"><span data-stu-id="9b302-154">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="9b302-155">**Примечание** 
 Разрешение " **связывание объектов GPO** " назначается членам группы администраторов домена и администраторов предприятия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9b302-155">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="9b302-156">Чтобы назначить разрешение на доступ к **GPO** для дополнительных пользователей или групп (например, учетные записи с ролями администратора или утверждающего), щелкните узел **домена, а**затем откройте вкладку **Делегирование** , нажмите кнопку **Добавить**, а затем выберите пункт Пользователи или группы, которым нужно назначить разрешение.</span><span class="sxs-lookup"><span data-stu-id="9b302-156">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

## <span data-ttu-id="9b302-157">Инструкции по установке и настройке РАСШИРЕНного изменения параметров</span><span class="sxs-lookup"><span data-stu-id="9b302-157">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="9b302-158">Чтобы установить и настроить параметры РАСШИРЕНного конфигурирования, необходимо выполнить описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="9b302-158">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="9b302-159">Шаг 1: Установка сервера РАСШИРЕНного набора элементов</span><span class="sxs-lookup"><span data-stu-id="9b302-159">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="9b302-160">Шаг 2. Установка клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="9b302-160">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="9b302-161">Шаг 3: Настройка подключения к серверу с РАСШИРЕНным интерфейсом</span><span class="sxs-lookup"><span data-stu-id="9b302-161">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="9b302-162">Шаг 4: Настройка уведомления по электронной почте</span><span class="sxs-lookup"><span data-stu-id="9b302-162">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="9b302-163">Шаг 5: передача прав доступа</span><span class="sxs-lookup"><span data-stu-id="9b302-163">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="9b302-164">Шаг 1: Установка сервера РАСШИРЕНного набора элементов</span><span class="sxs-lookup"><span data-stu-id="9b302-164">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="9b302-165">На этом этапе необходимо установить сервер РАСШИРЕНного управления правами на рядовом сервере или контроллере домена, который будет запускать службу расширенного управления групповыми политиками, и настроить этот архив.</span><span class="sxs-lookup"><span data-stu-id="9b302-165">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="9b302-166">Все операции РАСШИРЕНного управления правами обрабатываются в этой службе Windows и выполняются с учетными данными службы.</span><span class="sxs-lookup"><span data-stu-id="9b302-166">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="9b302-167">Архивация, управляемая сервером расширенного управления групповыми политиками, может быть размещена на этом сервере или на другом сервере в том же лесе.</span><span class="sxs-lookup"><span data-stu-id="9b302-167">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="9b302-168">Установка сервера расширенного управления групповыми политиками на компьютере, на котором будет размещена служба РАСШИРЕНного управления</span><span class="sxs-lookup"><span data-stu-id="9b302-168">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="9b302-169">Войдите в систему под учетной записью, которая входит в группу "Администраторы домена".</span><span class="sxs-lookup"><span data-stu-id="9b302-169">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="9b302-170">Запустите компакт-диск с пакетом оптимизации рабочей среды Microsoft и следуйте инструкциям на экране, чтобы выбрать **Расширенное управление групповыми политиками — сервер**.</span><span class="sxs-lookup"><span data-stu-id="9b302-170">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="9b302-171">В диалоговом окне **Добро пожаловать** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9b302-171">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="9b302-172">В диалоговом окне **условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт** подтвердите условия и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9b302-172">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="9b302-173">В диалоговом окне **путь к приложению** выберите расположение, в которое нужно установить сервер расширенного набора.</span><span class="sxs-lookup"><span data-stu-id="9b302-173">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="9b302-174">На компьютере, на котором установлен сервер расширенного управления групповыми политиками, будет размещена служба и Управление архивом.</span><span class="sxs-lookup"><span data-stu-id="9b302-174">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="9b302-175">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9b302-175">Click **Next**.</span></span>

6.  <span data-ttu-id="9b302-176">В диалоговом окне **Архивировать путь** выберите расположение для архива относительно сервера расширенного поиска.</span><span class="sxs-lookup"><span data-stu-id="9b302-176">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="9b302-177">Путь к архиву может указывать на папку на сервере расширенного управления групповыми политиками или в другом месте, но необходимо выбрать расположение, в котором достаточно свободного места для хранения всех объектов групповой политики и данных журнала, управляемых этим сервером управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="9b302-177">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="9b302-178">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9b302-178">Click **Next**.</span></span>

7.  <span data-ttu-id="9b302-179">В диалоговом окне **учетная запись службы расширенного** выбора параметров выберите учетную запись службы, под которой будет выполняться служба расширенного выбора и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9b302-179">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="9b302-180">В диалоговом окне **Владелец архива** выберите учетную запись или группу, которой необходимо назначить роль администратора расширенного доступа (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="9b302-180">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="9b302-181">Этот администратор может назначать роли и разрешения РАСШИРЕНного доступа другим администраторам групповой политики (в том числе к роли администратора РАСШИРЕНного доступа к данным).</span><span class="sxs-lookup"><span data-stu-id="9b302-181">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="9b302-182">Для этого сценария выберите учетную запись, которая будет использоваться в роли администратора РАСШИРЕНного администрирования.</span><span class="sxs-lookup"><span data-stu-id="9b302-182">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="9b302-183">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9b302-183">Click **Next**.</span></span>

9.  <span data-ttu-id="9b302-184">В диалоговом окне **Настройка порта** введите порт для прослушивания службой расширенного выбора ключа.</span><span class="sxs-lookup"><span data-stu-id="9b302-184">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="9b302-185">Не снимайте флажок **Добавить исключение для порта в брандмауэр** , если только вы не настраиваете исключения для порта вручную или не используйте правила для настройки исключений.</span><span class="sxs-lookup"><span data-stu-id="9b302-185">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="9b302-186">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9b302-186">Click **Next**.</span></span>

10. <span data-ttu-id="9b302-187">В диалоговом окне **языки** выберите один или несколько языков интерфейса, которые нужно установить для сервера с расширенным интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="9b302-187">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="9b302-188">Нажмите кнопку **установить**, а затем — **Готово** , чтобы завершить работу мастера установки.</span><span class="sxs-lookup"><span data-stu-id="9b302-188">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="9b302-189">**Внимание!**  Не изменяйте параметры службы РАСШИРЕНного **управления правами с помощью средств администрирования** и **служб** в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="9b302-189">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="9b302-190">Это может привести к невозможности запуска службы РАСШИРЕНного настольных служб.</span><span class="sxs-lookup"><span data-stu-id="9b302-190">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="9b302-191">Сведения о том, как изменить параметры службы, приведены в разделе Справка по расширенному управлению групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="9b302-191">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="9b302-192">Шаг 2. Установка клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="9b302-192">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="9b302-193">Каждый администратор групповой политики — любой пользователь, который создает, редактирует, развертывает или удаляет GPO, должен установить на компьютеры, которые они используют, для управления объектами групповой политики, клиент с РАСШИРЕНными правами.</span><span class="sxs-lookup"><span data-stu-id="9b302-193">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="9b302-194">Для этого сценария необходимо установить клиентская версия с РАСШИРЕНным Управлением по крайней мере на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9b302-194">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="9b302-195">На компьютерах конечных пользователей, которые не выполняют администрирование групповой политики, вам не нужно устанавливать клиент с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="9b302-195">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="9b302-196">Установка клиента с расширенным управлением групповыми политиками на компьютере администратора групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-196">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="9b302-197">Запустите компакт-диск с пакетом оптимизации рабочей среды Microsoft и следуйте инструкциям на экране, чтобы выбрать **Расширенное управление групповыми политиками — клиент**.</span><span class="sxs-lookup"><span data-stu-id="9b302-197">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="9b302-198">В диалоговом окне **Добро пожаловать** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9b302-198">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="9b302-199">В диалоговом окне **условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт** подтвердите условия и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9b302-199">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="9b302-200">В диалоговом окне **путь к приложению** выберите расположение для установки клиента с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="9b302-200">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="9b302-201">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9b302-201">Click **Next**.</span></span>

5.  <span data-ttu-id="9b302-202">В диалоговом окне **сервер с расширенным** управлением разкрывающимся списком введите полное имя компьютера для сервера расширенного выбора ключа и порт, к которому нужно подключиться.</span><span class="sxs-lookup"><span data-stu-id="9b302-202">In the **AGPM Server** dialog box, type the fully-qualified computer name for the AGPM Server and the port to which to connect.</span></span> <span data-ttu-id="9b302-203">Портом по умолчанию для службы РАСШИРЕНного обслуживания не является 4600.</span><span class="sxs-lookup"><span data-stu-id="9b302-203">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="9b302-204">Не снимайте флажок **Разрешить использование консоли управления Майкрософт через брандмауэр** , если только вы не настраиваете исключения для порта вручную или не используйте правила для настройки исключений.</span><span class="sxs-lookup"><span data-stu-id="9b302-204">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="9b302-205">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9b302-205">Click **Next**.</span></span>

6.  <span data-ttu-id="9b302-206">В диалоговом окне **языки** выберите один или несколько языков интерфейса, которые нужно установить для клиента с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="9b302-206">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="9b302-207">Нажмите кнопку **установить**, а затем — **Готово** , чтобы завершить работу мастера установки.</span><span class="sxs-lookup"><span data-stu-id="9b302-207">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="9b302-208">Шаг 3: Настройка подключения к серверу с РАСШИРЕНным интерфейсом</span><span class="sxs-lookup"><span data-stu-id="9b302-208">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="9b302-209">В разделе управления ГРУППОВыми политиками сохраняются все версии всех управляемых объектов групповой политики (GPO), для которых Управление изменениями обеспечивается в центральном архиве, поэтому администраторы групповой политики могут просматривать и изменять GPO в автономном режиме без немедленного воздействия на развернутую версию каждого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-209">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="9b302-210">На этом этапе необходимо настроить соединение с сервером РАСШИРЕНного администрирования и убедиться, что все администраторы групповой политики подключаются к одному и тому же серверу.</span><span class="sxs-lookup"><span data-stu-id="9b302-210">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="9b302-211">(Дополнительные сведения о настройке нескольких серверов РАСШИРЕНной конфигурации см. в разделе Справка по расширенному управлению групповыми политиками.)</span><span class="sxs-lookup"><span data-stu-id="9b302-211">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="9b302-212">Настройка подключения к серверу РАСШИРЕНного конфигурирования для всех администраторов групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-212">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="9b302-213">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которую выбрали в качестве владельца архива.</span><span class="sxs-lookup"><span data-stu-id="9b302-213">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="9b302-214">У этого пользователя есть роль администратора управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="9b302-214">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="9b302-215">Нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем — **Управление групповой политикой** , чтобы открыть консоль управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="9b302-215">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="9b302-216">Изменение объекта групповой политики, применяемого ко всем администраторам групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-216">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="9b302-217">В окне **редактора управления групповыми политиками** дважды щелкните элемент **Конфигурация пользователя**, **политики**, **Административные шаблоны**, **компоненты Windows**и управление **групповыми**политиками.</span><span class="sxs-lookup"><span data-stu-id="9b302-217">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="9b302-218">В области сведений дважды щелкните элемент расширенной настройки и выберите **сервер по умолчанию (все домены)**.</span><span class="sxs-lookup"><span data-stu-id="9b302-218">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="9b302-219">В окне **Свойства** выберите пункт **включена** и введите полное имя компьютера и порт (например, **Server.contoso.com:4600**) для сервера, на котором размещается Архив.</span><span class="sxs-lookup"><span data-stu-id="9b302-219">In the **Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="9b302-220">По умолчанию служба РАСШИРЕНного использования порта использует порт 4600.</span><span class="sxs-lookup"><span data-stu-id="9b302-220">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="9b302-221">Нажмите кнопку **ОК**, а затем закройте окно **редактора управления групповыми политиками** .</span><span class="sxs-lookup"><span data-stu-id="9b302-221">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="9b302-222">После обновления групповой политики соединение с сервером РАСШИРЕНного политики для каждого администратора будет настроено.</span><span class="sxs-lookup"><span data-stu-id="9b302-222">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="9b302-223">Шаг 4: Настройка уведомления по электронной почте</span><span class="sxs-lookup"><span data-stu-id="9b302-223">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="9b302-224">Как Администратор расширенного управления групповыми политиками (полный доступ) вы указываете адреса электронной почты утверждающих и администраторов РАСШИРЕНного доступа, которым будет отправлено сообщение электронной почты с запросом, когда редактор попытается создать, развернуть или удалить объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-224">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="9b302-225">Кроме того, вы можете определить псевдоним, из которого отправляются эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="9b302-225">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="9b302-226">Настройка уведомления по электронной почте для РАСШИРЕНного</span><span class="sxs-lookup"><span data-stu-id="9b302-226">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="9b302-227">В области сведений откройте вкладку **Делегирование домена** .</span><span class="sxs-lookup"><span data-stu-id="9b302-227">In the details pane, click the **Domain Delegation** tab.</span></span>

2.  <span data-ttu-id="9b302-228">В поле **из адреса электронной почты** введите псевдоним электронной почты для расширенного вида, из которого нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="9b302-228">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

3.  <span data-ttu-id="9b302-229">В поле **адрес электронной почты** введите адрес электронной почты учетной записи пользователя, которому вы хотите назначить роль утверждающего.</span><span class="sxs-lookup"><span data-stu-id="9b302-229">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

4.  <span data-ttu-id="9b302-230">В поле **SMTP-сервер** введите допустимый почтовый SMTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="9b302-230">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

5.  <span data-ttu-id="9b302-231">В полях **имя пользователя** и **пароль** введите учетные данные пользователя, у которого есть доступ к службе SMTP.</span><span class="sxs-lookup"><span data-stu-id="9b302-231">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span> <span data-ttu-id="9b302-232">Нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="9b302-232">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="9b302-233">Шаг 5: передача прав доступа</span><span class="sxs-lookup"><span data-stu-id="9b302-233">Step 5: Delegate access</span></span>

<span data-ttu-id="9b302-234">Как Администратор расширенного управления групповыми политиками (режим полного доступа) вы делегируйте доступ к объектам GPO на уровне домена, назначая роли учетной записи каждого администратора групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-234">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="9b302-235">**Примечание**  Вы также можете делегировать доступ на уровне объекта групповой политики, а не на уровне домена.</span><span class="sxs-lookup"><span data-stu-id="9b302-235">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="9b302-236">Подробные сведения можно найти в разделе Справка по расширенному управлению групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="9b302-236">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="9b302-237">**Важно!**  Вы должны ограничивать членство в группе "владельцы" владельца групповой политики, поэтому ее нельзя использовать для обхода управления доступом к GPO.</span><span class="sxs-lookup"><span data-stu-id="9b302-237">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="9b302-238">(В **консоли управления групповыми политиками**щелкните **объекты групповой политики** в лесу и домене, в которых вы хотите управлять объектами GPO, выберите пункт **Делегирование**и настройте параметры в соответствии с потребностями Организации.)</span><span class="sxs-lookup"><span data-stu-id="9b302-238">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="9b302-239">Передача доступа ко всем объектам групповой политики внутри домена</span><span class="sxs-lookup"><span data-stu-id="9b302-239">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="9b302-240">На вкладке **доменное делегирование** нажмите кнопку **Добавить** , выберите учетную запись администратора групповой политики, которая будет использоваться в качестве утверждающего, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-240">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="9b302-241">В диалоговом окне **Добавление группы или пользователя** выберите роль **утверждающего** , чтобы назначить ей роль учетной записи, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-241">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="9b302-242">(Эта роль включает в себя роль проверяющего.)</span><span class="sxs-lookup"><span data-stu-id="9b302-242">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="9b302-243">Нажмите кнопку **Добавить** , выберите учетную запись пользователя администратора групповой политики, которая будет использоваться в качестве редактора, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-243">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="9b302-244">В диалоговом окне **Добавление группы или пользователя** выберите роль " **Редактор** ", чтобы назначить эту роль учетной записи, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-244">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="9b302-245">(Эта роль включает в себя роль проверяющего.)</span><span class="sxs-lookup"><span data-stu-id="9b302-245">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="9b302-246">Нажмите кнопку **Добавить** , выберите учетную запись администратора групповой политики, которая будет использоваться в качестве рецензента, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-246">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="9b302-247">В диалоговом окне **Добавление группы или пользователя** выберите роль **проверяющего** , чтобы назначить учетной записи только эту роль.</span><span class="sxs-lookup"><span data-stu-id="9b302-247">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="9b302-248">Инструкции по управлению объектами групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-248">Steps for managing GPOs</span></span>


<span data-ttu-id="9b302-249">Для создания, изменения, проверки и развертывания объектов групповой политики с помощью РАСШИРЕНного использования функций необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9b302-249">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="9b302-250">Кроме того, вы создадите шаблон, удалите объект групповой политики и восстановите удаленный объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-250">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="9b302-251">Действие 1: создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-251">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="9b302-252">Действие 2: изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-252">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="9b302-253">Шаг 3: Проверка и развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-253">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="9b302-254">Шаг 4: использование шаблона для создания объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-254">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="9b302-255">Шаг 5: удаление и восстановление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-255">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="9b302-256">Действие 1: создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-256">Step 1: Create a GPO</span></span>

<span data-ttu-id="9b302-257">В среде с несколькими администраторами групповой политики у пользователей с ролью "редактор" есть возможность запросить создание новых объектов GPO, но такой запрос должен быть утвержден участником роли утверждающего, поскольку создание нового объекта групповой политики влияет на производственную среду.</span><span class="sxs-lookup"><span data-stu-id="9b302-257">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="9b302-258">На этом этапе вы используете учетную запись с ролью "редактор" для запроса создания нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-258">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="9b302-259">С помощью учетной записи, в которой находится роль утверждающего, вы утверждаете этот запрос и завершаете создание объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-259">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="9b302-260">Запрос на создание нового объекта групповой политики, управляемого с помощью расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="9b302-260">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="9b302-261">На компьютере, на котором установлен клиент с РАСШИРЕНным управлением правами, войдите в систему с помощью учетной записи пользователя, которой назначена роль "редактор" в расширенном управлении учетными записями.</span><span class="sxs-lookup"><span data-stu-id="9b302-261">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="9b302-262">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-262">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="9b302-263">Щелкните правой кнопкой мыши узел **контроль изменений** и выберите команду **создать управляемый объект групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="9b302-263">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="9b302-264">В диалоговом окне **новый управляемый объект групповой политики** :</span><span class="sxs-lookup"><span data-stu-id="9b302-264">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="9b302-265">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="9b302-265">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="9b302-266">Введите **MyGPO** в качестве имени нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-266">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="9b302-267">Введите Примечание для нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-267">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="9b302-268">Нажмите кнопку **создать Live** , чтобы новый объект групповой политики был развернут в рабочей среде сразу после утверждения.</span><span class="sxs-lookup"><span data-stu-id="9b302-268">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="9b302-269">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="9b302-269">Click **Submit**.</span></span>

5.  <span data-ttu-id="9b302-270">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-270">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9b302-271">Новый объект групповой политики появится на вкладке **ожидающие** .</span><span class="sxs-lookup"><span data-stu-id="9b302-271">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="9b302-272">Утверждение ожидающего запроса на создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-272">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="9b302-273">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которой назначена роль утверждающего в РАСШИРЕНном.</span><span class="sxs-lookup"><span data-stu-id="9b302-273">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="9b302-274">Откройте папку "Входящие" электронной почты для учетной записи и обратите внимание на то, что вы получили сообщение электронной почты от псевдонима с помощью запроса редактора, чтобы создать объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-274">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="9b302-275">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-275">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="9b302-276">На вкладке **содержание** откройте вкладку **ожидается** , чтобы отобразить ожидающие GPO.</span><span class="sxs-lookup"><span data-stu-id="9b302-276">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="9b302-277">Щелкните правой кнопкой мыши **MyGPO**и выберите команду **утвердить**.</span><span class="sxs-lookup"><span data-stu-id="9b302-277">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="9b302-278">Нажмите кнопку **Да** , чтобы подтвердить утверждение создания объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-278">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="9b302-279">Объект групповой политики перемещается на вкладку **Управление** .</span><span class="sxs-lookup"><span data-stu-id="9b302-279">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="9b302-280">Действие 2: изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-280">Step 2: Edit a GPO</span></span>

<span data-ttu-id="9b302-281">С помощью объектов групповой политики можно настраивать параметры компьютера или пользователя и развертывать их на нескольких компьютерах или в других пользователей.</span><span class="sxs-lookup"><span data-stu-id="9b302-281">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="9b302-282">На этом этапе вы используете учетную запись с ролью "редактор" для извлечения GPO из архива, изменения GPO в автономном режиме, проверки GPO в архиве и запроса развертывания объекта групповой политики в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="9b302-282">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="9b302-283">В этом сценарии вы можете настроить параметр в объекте групповой политики таким образом, чтобы пароль имел длину не менее восьми символов.</span><span class="sxs-lookup"><span data-stu-id="9b302-283">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="9b302-284">Извлечение GPO из архива для редактирования</span><span class="sxs-lookup"><span data-stu-id="9b302-284">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="9b302-285">На компьютере, на котором установлен клиент с РАСШИРЕНным управлением правами, войдите в систему с помощью учетной записи пользователя, которой назначена роль редактора в РАСШИРЕНном наборе данных.</span><span class="sxs-lookup"><span data-stu-id="9b302-285">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="9b302-286">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-286">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="9b302-287">На вкладке **содержание** в области сведений откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-287">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="9b302-288">Щелкните правой кнопкой мыши **MyGPO**и выберите пункт **извлечь.**</span><span class="sxs-lookup"><span data-stu-id="9b302-288">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="9b302-289">Введите Примечание, которое будет отображаться в истории объекта групповой политики, когда он извлечен, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-289">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="9b302-290">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-290">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9b302-291">На вкладке **Управление** состоянием GPO считается **извлеченным**.</span><span class="sxs-lookup"><span data-stu-id="9b302-291">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="9b302-292">Изменение GPO в автономном режиме и Настройка минимальной длины пароля</span><span class="sxs-lookup"><span data-stu-id="9b302-292">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="9b302-293">На вкладке **Управление** , щелкните правой кнопкой мыши **MyGPO**и выберите команду **изменить** , чтобы открыть окно **редактора управления групповыми политиками** и внести изменения в автономную копию объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-293">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="9b302-294">Для этого сценария настройте минимальную длину пароля:</span><span class="sxs-lookup"><span data-stu-id="9b302-294">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="9b302-295">В разделе **Конфигурация компьютера**дважды щелкните **политики**, **Параметры Windows**, **Параметры безопасности**, **политики учетных записей**и **политики паролей**.</span><span class="sxs-lookup"><span data-stu-id="9b302-295">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="9b302-296">В области сведений дважды щелкните элемент **Минимальная длина пароля**.</span><span class="sxs-lookup"><span data-stu-id="9b302-296">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="9b302-297">В окне "Свойства" установите флажок **определить этот параметр политики** , укажите число символов **8**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-297">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="9b302-298">Закройте окно **редактора управления групповыми политиками** .</span><span class="sxs-lookup"><span data-stu-id="9b302-298">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="9b302-299">Проверка GPO в архиве</span><span class="sxs-lookup"><span data-stu-id="9b302-299">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="9b302-300">На вкладке **Управление** , щелкните правой кнопкой мыши **MyGPO** и выберите команду **вернуть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-300">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="9b302-301">Введите примечание и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-301">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="9b302-302">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-302">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9b302-303">На вкладке **Управление** состоянием объекта групповой политики считается **возвращенное**.</span><span class="sxs-lookup"><span data-stu-id="9b302-303">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="9b302-304">Запрос развертывания объекта групповой политики в рабочей среде</span><span class="sxs-lookup"><span data-stu-id="9b302-304">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="9b302-305">На вкладке **Управление** , щелкните правой кнопкой мыши **MyGPO** и выберите команду **развернуть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-305">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="9b302-306">Поскольку эта учетная запись не является администратором утверждения или РАСШИРЕНного администрирования, необходимо отправить запрос на развертывание.</span><span class="sxs-lookup"><span data-stu-id="9b302-306">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="9b302-307">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="9b302-307">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="9b302-308">Введите Примечание, которое будет отображаться в журнале объекта групповой политики, а затем нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="9b302-308">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="9b302-309">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-309">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9b302-310">**MyGPO** отображается в списке объектов групповой политики на вкладке **ожидающие** .</span><span class="sxs-lookup"><span data-stu-id="9b302-310">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="9b302-311">Шаг 3: Проверка и развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-311">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="9b302-312">На этом этапе вы действуете как утверждающий, создавая отчеты и анализируя параметры и изменяя параметры в объекте групповой политики, чтобы определить, нужно ли их утверждать.</span><span class="sxs-lookup"><span data-stu-id="9b302-312">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="9b302-313">После того как вы выберете объект групповой политики, вы развернете его в производственную среду и свяжите его с доменом или подразделением (OU), чтобы оно запустилось при обновлении групповой политики для компьютеров в этом домене или OU.</span><span class="sxs-lookup"><span data-stu-id="9b302-313">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="9b302-314">Просмотр параметров в объекте групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-314">To review settings in the GPO</span></span>**

1. <span data-ttu-id="9b302-315">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которой назначена роль утверждающего в РАСШИРЕНном.</span><span class="sxs-lookup"><span data-stu-id="9b302-315">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="9b302-316">(Любой администратор групповой политики с ролью рецензента, включенный во все другие роли, может просматривать параметры в объекте групповой политики.)</span><span class="sxs-lookup"><span data-stu-id="9b302-316">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2. <span data-ttu-id="9b302-317">Откройте папку "Входящие" электронной почты для учетной записи и обратите внимание на то, что вы получили сообщение электронной почты от псевдонима РАСШИРЕНного использования запроса редактора для развертывания объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-317">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="9b302-318">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-318">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="9b302-319">На вкладке **содержание** в области сведений откройте вкладку **ожидается** .</span><span class="sxs-lookup"><span data-stu-id="9b302-319">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="9b302-320">Дважды щелкните **MyGPO** , чтобы отобразить историю.</span><span class="sxs-lookup"><span data-stu-id="9b302-320">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="9b302-321">Проверьте параметры в последней версии MyGPO:</span><span class="sxs-lookup"><span data-stu-id="9b302-321">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="9b302-322">В окне " **Журнал** " щелкните правой кнопкой мыши версию объекта групповой политики с последней меткой времени, выберите пункт **Параметры**, а затем — **отчет HTML** , чтобы отобразить сводку по параметрам объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-322">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="9b302-323">В веб-браузере нажмите кнопку **Показать все** , чтобы отобразить все параметры в объекте групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-323">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span> <span data-ttu-id="9b302-324">Закройте браузер.</span><span class="sxs-lookup"><span data-stu-id="9b302-324">Close the browser.</span></span>

7. <span data-ttu-id="9b302-325">Сравните последнюю версию MyGPO с первой версией, возвращенной в Архив:</span><span class="sxs-lookup"><span data-stu-id="9b302-325">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="9b302-326">В окне " **Журнал** " выберите версию объекта групповой политики с последней меткой времени.</span><span class="sxs-lookup"><span data-stu-id="9b302-326">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="9b302-327">Нажмите клавишу CTRL и выберите самую старую версию GPO \*\*, которой не является \*\*\* \* \ \ \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="9b302-327">Press CTRL and click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="9b302-328">Нажмите кнопку **различия** .</span><span class="sxs-lookup"><span data-stu-id="9b302-328">Click the **Differences** button.</span></span> <span data-ttu-id="9b302-329">Раздел **политики учетных записей и политика паролей** выделены зеленым цветом и предшествует **\ [+ \]**, что указывает на то, что этот параметр настроен только в последней версии GPO.</span><span class="sxs-lookup"><span data-stu-id="9b302-329">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="9b302-330">Выберите политики **учетных записей и политика паролей**.</span><span class="sxs-lookup"><span data-stu-id="9b302-330">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="9b302-331">Параметр **минимальной длины пароля** также выделяется зеленым цветом и предшествует **\ [+ \]**, что указывает на то, что оно настроено только в последней версии GPO.</span><span class="sxs-lookup"><span data-stu-id="9b302-331">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="9b302-332">Закройте веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="9b302-332">Close the Web browser.</span></span>

**<span data-ttu-id="9b302-333">Развертывание объекта групповой политики в рабочей среде</span><span class="sxs-lookup"><span data-stu-id="9b302-333">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="9b302-334">На вкладке **Ожидание** щелкните правой кнопкой мыши **MyGPO** и выберите команду **утвердить**.</span><span class="sxs-lookup"><span data-stu-id="9b302-334">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="9b302-335">Введите Примечание для включения в историю объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-335">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="9b302-336">Щелкните **Да**.</span><span class="sxs-lookup"><span data-stu-id="9b302-336">Click **Yes**.</span></span> <span data-ttu-id="9b302-337">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-337">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9b302-338">Объект групповой политики развернут в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="9b302-338">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="9b302-339">Связывание объекта групповой политики с доменом или подразделением</span><span class="sxs-lookup"><span data-stu-id="9b302-339">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="9b302-340">В консоли управления групповыми политиками щелкните правой кнопкой мыши домен или подразделение, к которому вы хотите применить настраиваемый объект групповой политики, а затем выберите команду **связать существующий объект групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="9b302-340">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="9b302-341">В диалоговом окне **Выбор объекта групповой политики** щелкните **MyGPO**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-341">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="9b302-342">Шаг 4: использование шаблона для создания объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-342">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="9b302-343">На этом этапе вы используете учетную запись с ролью "редактор", чтобы создать шаблон — нередактируемую статическую версию GPO для использования в качестве отправной точки для создания новых объектов групповой политики, а затем Создай новый объект групповой политики на основе этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="9b302-343">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="9b302-344">Шаблоны полезны для быстрого создания нескольких GPO, включающих множество одинаковых параметров.</span><span class="sxs-lookup"><span data-stu-id="9b302-344">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="9b302-345">Создание шаблона на основе существующего объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-345">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="9b302-346">На компьютере, на котором установлен клиент с РАСШИРЕНным управлением правами, войдите в систему с помощью учетной записи пользователя, которой назначена роль редактора в РАСШИРЕНном наборе данных.</span><span class="sxs-lookup"><span data-stu-id="9b302-346">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="9b302-347">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-347">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="9b302-348">На вкладке **содержание** в области сведений откройте вкладку **Управление** .</span><span class="sxs-lookup"><span data-stu-id="9b302-348">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="9b302-349">Щелкните правой кнопкой мыши **MyGPO**и выберите команду **Сохранить как шаблон** , чтобы создать шаблон, включающий все параметры, в настоящее время находящиеся в MyGPO.</span><span class="sxs-lookup"><span data-stu-id="9b302-349">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="9b302-350">Введите **MyTemplate** в качестве имени шаблона и примечания, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-350">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="9b302-351">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-351">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9b302-352">Новый шаблон появится на вкладке **шаблоны** .</span><span class="sxs-lookup"><span data-stu-id="9b302-352">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="9b302-353">Запрос на создание нового объекта групповой политики, управляемого с помощью расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="9b302-353">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="9b302-354">Откройте вкладку **Управление** .</span><span class="sxs-lookup"><span data-stu-id="9b302-354">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="9b302-355">Щелкните правой кнопкой мыши узел **контроль изменений** и выберите команду **создать управляемый объект групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="9b302-355">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="9b302-356">В диалоговом окне **новый управляемый объект групповой политики** :</span><span class="sxs-lookup"><span data-stu-id="9b302-356">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="9b302-357">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="9b302-357">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="9b302-358">Введите **MyOtherGPO** в качестве имени нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-358">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="9b302-359">Введите Примечание для нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-359">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="9b302-360">Нажмите кнопку **создать в реальном времени**, чтобы новый объект групповой политики был развернут в рабочей среде сразу после утверждения.</span><span class="sxs-lookup"><span data-stu-id="9b302-360">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="9b302-361">**В шаблоне из GPO**выберите **MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="9b302-361">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="9b302-362">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="9b302-362">Click **Submit**.</span></span>

4.  <span data-ttu-id="9b302-363">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-363">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9b302-364">Новый объект групповой политики появится на вкладке **ожидающие** .</span><span class="sxs-lookup"><span data-stu-id="9b302-364">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="9b302-365">Используйте учетную запись, которой назначена роль утверждающего, чтобы утвердить ожидающий запрос на создание объекта групповой политики, как на [этапе 1: Создайте объект групповой политики](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="9b302-365">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="9b302-366">MyTemplate все параметры, настроенные в MyGPO.</span><span class="sxs-lookup"><span data-stu-id="9b302-366">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="9b302-367">Поскольку MyOtherGPO был создан с помощью MyTemplate, он первоначально содержит все параметры, MyGPO содержащиеся на момент создания MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="9b302-367">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="9b302-368">Чтобы подтвердить это, вы можете создать отчет о разнице, чтобы сравнить MyOtherGPO с MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="9b302-368">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="9b302-369">Извлечение GPO из архива для редактирования</span><span class="sxs-lookup"><span data-stu-id="9b302-369">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="9b302-370">На компьютере, на котором установлен клиент с РАСШИРЕНным управлением правами, войдите в систему с помощью учетной записи пользователя, которой назначена роль редактора в РАСШИРЕНном наборе данных.</span><span class="sxs-lookup"><span data-stu-id="9b302-370">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="9b302-371">Щелкните правой кнопкой мыши **MyOtherGPO**и выберите пункт **извлечь.**</span><span class="sxs-lookup"><span data-stu-id="9b302-371">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="9b302-372">Введите Примечание, которое будет отображаться в истории объекта групповой политики, когда он извлечен, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-372">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="9b302-373">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-373">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9b302-374">На вкладке **Управление** состоянием GPO считается **извлеченным**.</span><span class="sxs-lookup"><span data-stu-id="9b302-374">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="9b302-375">Изменение GPO в автономном режиме и Настройка длительности блокировки учетной записи</span><span class="sxs-lookup"><span data-stu-id="9b302-375">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="9b302-376">На вкладке **Управление** , щелкните правой кнопкой мыши **MyOtherGPO**и выберите команду **изменить** , чтобы открыть окно **редактора управления групповыми политиками** и внести изменения в автономную копию объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-376">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="9b302-377">Для этого сценария настройте минимальную длину пароля:</span><span class="sxs-lookup"><span data-stu-id="9b302-377">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="9b302-378">В разделе **Конфигурация компьютера**дважды щелкните **политики**, **Параметры Windows**, **Параметры безопасности**, **политики учетных записей**и **политики блокировки учетных записей**.</span><span class="sxs-lookup"><span data-stu-id="9b302-378">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="9b302-379">В области сведений дважды щелкните **Продолжительность блокировки учетной записи**.</span><span class="sxs-lookup"><span data-stu-id="9b302-379">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="9b302-380">В окне "Свойства" установите флажок **задать этот параметр политики**, задайте для параметра продолжительность **30** минут и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-380">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="9b302-381">Закройте окно **редактора управления групповыми политиками** .</span><span class="sxs-lookup"><span data-stu-id="9b302-381">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="9b302-382">Проверьте MyOtherGPO в архиве и запросите развертывание в том виде, в котором вы делали в MyGPO на [этапе 2. Измените объект групповой политики](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="9b302-382">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="9b302-383">Вы можете сравнить MyOtherGPO с MyGPO или с MyTemplate с помощью отчетов о различиях.</span><span class="sxs-lookup"><span data-stu-id="9b302-383">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="9b302-384">Любая учетная запись, включающая в себя роль рецензента (Управление групповыми политиками \ [полный доступ \], утверждающая, редактор или рецензент), может создавать отчеты.</span><span class="sxs-lookup"><span data-stu-id="9b302-384">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="9b302-385">Сравнение GPO с другим GPO и с шаблоном</span><span class="sxs-lookup"><span data-stu-id="9b302-385">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="9b302-386">Чтобы сравнить MyGPO и MyOtherGPO, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="9b302-386">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="9b302-387">На вкладке **Управление** нажмите кнопку **MyGPO**.</span><span class="sxs-lookup"><span data-stu-id="9b302-387">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="9b302-388">Нажмите клавишу CTRL, а затем — **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="9b302-388">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="9b302-389">Щелкните правой кнопкой мыши **MyOtherGPO**, наведите указатель на пункт **отличия**и выберите пункт **отчет в формате HTML**.</span><span class="sxs-lookup"><span data-stu-id="9b302-389">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="9b302-390">Чтобы сравнить MyOtherGPO и MyTemplate, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="9b302-390">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="9b302-391">На вкладке **Управление** нажмите кнопку **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="9b302-391">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="9b302-392">Щелкните правой кнопкой мыши **MyOtherGPO**, наведите указатель на пункт **отличия**и выберите пункт **шаблон**.</span><span class="sxs-lookup"><span data-stu-id="9b302-392">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="9b302-393">Выберите **MyTemplate** и **HTML-отчет**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-393">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="9b302-394">Шаг 5: удаление и восстановление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-394">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="9b302-395">На этом этапе вы действуете как утверждающий для удаления GPO.</span><span class="sxs-lookup"><span data-stu-id="9b302-395">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="9b302-396">Удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-396">To delete a GPO</span></span>**

1.  <span data-ttu-id="9b302-397">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которой назначена роль утверждающего.</span><span class="sxs-lookup"><span data-stu-id="9b302-397">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="9b302-398">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-398">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="9b302-399">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-399">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="9b302-400">Щелкните правой кнопкой мыши **MyGPO**и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="9b302-400">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="9b302-401">Выберите команду **удалить объект групповой политики из архива и производства** , чтобы удалить версию в архиве, а также версию объекта групповой политики, развернутую в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="9b302-401">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="9b302-402">Введите Примечание, которое будет отображаться в контрольной записи для объекта групповой политики, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-402">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="9b302-403">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9b302-404">Объект групповой политики удаляется с вкладки " **управляемые** " и отображается на вкладке " **Корзина** ", в которой ее можно восстановить или уничтожить.</span><span class="sxs-lookup"><span data-stu-id="9b302-404">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="9b302-405">Иногда вы обнаружите, что после удаления объекта групповой политики он по-прежнему нужен.</span><span class="sxs-lookup"><span data-stu-id="9b302-405">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="9b302-406">На этом этапе вы выступаете в качестве утверждающего для восстановления удаляемого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-406">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="9b302-407">Восстановление удаленного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b302-407">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="9b302-408">На вкладке " **содержимое** " щелкните вкладку " **Корзина** ", чтобы отобразить удаленные GPO.</span><span class="sxs-lookup"><span data-stu-id="9b302-408">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="9b302-409">Щелкните правой кнопкой мыши **MyGPO**и выберите команду **восстановить**.</span><span class="sxs-lookup"><span data-stu-id="9b302-409">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="9b302-410">Введите Примечание, которое будет отображаться в журнале объекта групповой политики, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b302-410">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="9b302-411">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-411">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9b302-412">Объект групповой политики удаляется из вкладки " **Корзина** " и отображается на вкладке " **управляемые** ".</span><span class="sxs-lookup"><span data-stu-id="9b302-412">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="9b302-413">**Примечание**  Восстановление GPO в архиве не приводит к его повторному развертыванию в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="9b302-413">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="9b302-414">Чтобы вернуть GPO в производственную среду, разверните объект групповой политики, как на [шаге 3: Проверка и развертывание объекта групповой политики](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="9b302-414">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="9b302-415">После изменения и развертывания объекта групповой политики, возможно, вы обнаружите, что последние изменения в объекте групповой политики приводят к возникновению проблемы.</span><span class="sxs-lookup"><span data-stu-id="9b302-415">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="9b302-416">На этом этапе вы выполняете роль утверждающего, чтобы вернуться к предыдущей версии GPO.</span><span class="sxs-lookup"><span data-stu-id="9b302-416">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="9b302-417">Вы можете вернуться к любой версии в истории объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-417">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="9b302-418">С помощью примечаний и подписей вы можете определить известные хорошие версии и внести определенные изменения.</span><span class="sxs-lookup"><span data-stu-id="9b302-418">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="9b302-419">Чтобы вернуться к предыдущей версии GPO,</span><span class="sxs-lookup"><span data-stu-id="9b302-419">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="9b302-420">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9b302-420">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="9b302-421">Дважды щелкните **MyGPO** , чтобы отобразить историю.</span><span class="sxs-lookup"><span data-stu-id="9b302-421">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="9b302-422">Щелкните правой кнопкой мыши версию, которую нужно развернуть, и выберите команду **развернуть**, а затем — **Да**.</span><span class="sxs-lookup"><span data-stu-id="9b302-422">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="9b302-423">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-423">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9b302-424">В окне **журнала** нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9b302-424">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="9b302-425">**Примечание**  Чтобы убедиться в том, что версия, которая была повторно обновлена, предназначена для версии, проверьте отчет о различиях для двух версий.</span><span class="sxs-lookup"><span data-stu-id="9b302-425">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="9b302-426">В окне **журнала** для объекта групповой политики выберите две версии, щелкните их правой кнопкой мыши, наведите указатель на пункт **разница**и выберите **отчет HTML** или **отчет XML**.</span><span class="sxs-lookup"><span data-stu-id="9b302-426">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





