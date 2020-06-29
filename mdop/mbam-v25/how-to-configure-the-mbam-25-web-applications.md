---
title: Настройка веб-приложений MBAM 2.5
description: Настройка веб-приложений MBAM 2.5
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824499"
---
# <span data-ttu-id="d5d36-103">Настройка веб-приложений MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d5d36-103">How to Configure the MBAM 2.5 Web Applications</span></span>


<span data-ttu-id="d5d36-104">В этой статье объясняется, как настроить веб-приложения Microsoft BitLocker Administration и Monitoring (MBAM) 2,5 для рекомендованной [высокоуровневой архитектуры для MBAM 2,5](high-level-architecture-for-mbam-25.md) с помощью одного из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="d5d36-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 web applications for the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md) by using one of the following methods:</span></span>

-   <span data-ttu-id="d5d36-105">Командлет Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d5d36-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="d5d36-106">Мастер настройки сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="d5d36-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="d5d36-107">Веб-приложения состоят из указанных ниже веб-служб и соответствующих им.</span><span class="sxs-lookup"><span data-stu-id="d5d36-107">The web applications comprise the following websites and their corresponding web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d5d36-108">Веб-сайт</span><span class="sxs-lookup"><span data-stu-id="d5d36-108">Website</span></span></th>
<th align="left"><span data-ttu-id="d5d36-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d5d36-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5d36-110">Веб-сайт администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="d5d36-110">Administration and Monitoring Website</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5d36-111">Веб-сайт, на котором пользователи могут просматривать отчеты и помогать пользователям восстанавливать свои компьютеры после того, как они забывают PIN-код или пароль</span><span class="sxs-lookup"><span data-stu-id="d5d36-111">Website where specified users can view reports and help end users recover their computers when they forget their PIN or password</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d5d36-112">Портал самообслуживания</span><span class="sxs-lookup"><span data-stu-id="d5d36-112">Self-Service Portal</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5d36-113">Веб-сайт, с которого конечные пользователи могут получить доступ к своим компьютерам независимо от того, забыли ли вы свой PIN-код или пароль</span><span class="sxs-lookup"><span data-stu-id="d5d36-113">Website that end users can access to independently regain access to their computers if they forget their PIN or password</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="d5d36-114">Прежде чем приступить к настройке, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d5d36-114">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d5d36-115">Шаг</span><span class="sxs-lookup"><span data-stu-id="d5d36-115">Step</span></span></th>
<th align="left"><span data-ttu-id="d5d36-116">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="d5d36-116">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5d36-117">Изучите рекомендованную архитектуру для MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5d36-117">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="d5d36-118">Высокоуровневая архитектура для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d5d36-118">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d5d36-119">Проверка поддерживаемых конфигураций для MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5d36-119">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="d5d36-120">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d5d36-120">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5d36-121">Заполните необходимые условия на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="d5d36-121">Complete the required prerequisites on each server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d5d36-122">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d5d36-122">Note</span></span></strong><br/><p><span data-ttu-id="d5d36-123">Убедитесь, что вы настроили службы SQL ServerReporting (SSRS) для использования протокола SSL (Secure Sockets Layer) перед настройкой веб-сайта администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="d5d36-123">Ensure that you configure SQL ServerReporting Services (SSRS) to use the Secure Sockets Layer (SSL) before you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="d5d36-124">В противном случае функция "отчеты" будет использовать HTTP вместо HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d5d36-124">Otherwise, the Reports feature will use HTTP instead of HTTPS.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="d5d36-125">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="d5d36-125">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="d5d36-126">Требования к серверу MBAM 2,5, применимые только к топологии интеграции Configuration Manager </a> (если применимо)</span><span class="sxs-lookup"><span data-stu-id="d5d36-126">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d5d36-127">Зарегистрируйте имена участников службы (SPN) для учетной записи пула приложений для веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="d5d36-127">Register service principal names (SPNs) for the application pool account for the websites.</span></span> <span data-ttu-id="d5d36-128">Этот шаг необходимо выполнить только в том случае, если у вас нет прав администратора домена в доменных службах Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="d5d36-128">You need to do this step only if you do not have administrative domain rights in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="d5d36-129">Если у вас есть эти права в доменных СЛУЖБах Active Directory, MBAM создаст SPN.</span><span class="sxs-lookup"><span data-stu-id="d5d36-129">If you do have these rights in AD DS, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)"><span data-ttu-id="d5d36-130">Планирование защиты веб-сайтов MBAM</span><span class="sxs-lookup"><span data-stu-id="d5d36-130">Planning How to Secure the MBAM Websites</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5d36-131">Установка программного обеспечения сервера MBAM на каждый сервер, на котором будет настроена функция сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5d36-131">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d5d36-132">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d5d36-132">Note</span></span></strong><br/><p><span data-ttu-id="d5d36-133">Если вы планируете установить сайты на одном сервере и веб-службах на другом, вы сможете настроить их только с помощью <strong> </strong> командлета Windows PowerShell Enable-MbamWebApplication.</span><span class="sxs-lookup"><span data-stu-id="d5d36-133">If you plan to install the websites on one server and the web services on another, you will be able to configure them only by using the <strong>Enable-MbamWebApplication</strong> Windows PowerShell cmdlet.</span></span> <span data-ttu-id="d5d36-134">Мастер настройки сервера MBAM не поддерживает настройку этих элементов на отдельных серверах.</span><span class="sxs-lookup"><span data-stu-id="d5d36-134">The MBAM Server Configuration wizard does not support configuring these items on separate servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="d5d36-135">Установка программного обеспечения MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="d5d36-135">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d5d36-136">Если вы планируете использовать командлеты для настройки функций сервера MBAM, изучите необходимые условия для использования Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5d36-136">Review the prerequisites for using Windows PowerShell if you plan to use cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="d5d36-137">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d5d36-137">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="d5d36-138">Настройка веб-приложений с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d5d36-138">To configure the web applications by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="d5d36-139">Прежде чем приступить к настройке, прочтите раздел [Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) , чтобы просмотреть предварительные требования для использования Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5d36-139">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="d5d36-140">Используйте командлет **Enable-MbamWebApplication** , чтобы настроить веб-приложения с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5d36-140">Use the **Enable-MbamWebApplication** cmdlet to configure the web applications using Windows PowerShell.</span></span> <span data-ttu-id="d5d36-141">Чтобы получить сведения об этом командлете, введите **Get-Help Enable-MbamWebApplication**.</span><span class="sxs-lookup"><span data-stu-id="d5d36-141">To get information about this cmdlet, type **Get-Help Enable-MbamWebApplication**.</span></span>

**<span data-ttu-id="d5d36-142">Настройка параметров для всех веб-приложений с помощью мастера</span><span class="sxs-lookup"><span data-stu-id="d5d36-142">To configure the settings for all web applications using the wizard</span></span>**

1. <span data-ttu-id="d5d36-143">На сервере, на котором вы хотите настроить веб-приложения, запустите мастер настройки сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5d36-143">On the server where you want to configure the web applications, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="d5d36-144">Чтобы открыть мастер, вы можете выбрать **MBAM конфигурации сервера** в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="d5d36-144">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="d5d36-145">Нажмите кнопку **Добавить новые функции**, выберите **Администрирование и мониторинг на веб-сайте администрирования** и **на портале самообслуживания**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d5d36-145">Click **Add New Features**, select **Administration and Monitoring Website** and **Self-Service Portal**, and then click **Next**.</span></span> <span data-ttu-id="d5d36-146">Мастер проверяет, выполнены ли все необходимые условия для веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="d5d36-146">The wizard checks that all prerequisites for the web applications have been met.</span></span>

3. <span data-ttu-id="d5d36-147">Если проверка готовности к установке выполнена успешно, нажмите кнопку **Далее** , чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="d5d36-147">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="d5d36-148">В противном случае устраните недостающие необходимые компоненты и нажмите кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="d5d36-148">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="d5d36-149">Чтобы ввести значения полей в мастере, воспользуйтесь приведенными ниже описаниями.</span><span class="sxs-lookup"><span data-stu-id="d5d36-149">Use the following descriptions to enter the field values in the wizard.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong><span data-ttu-id="d5d36-150">Поле</span><span class="sxs-lookup"><span data-stu-id="d5d36-150">Field</span></span></strong></th>
   <th align="left"><span data-ttu-id="d5d36-151">Описание</span><span class="sxs-lookup"><span data-stu-id="d5d36-151">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="d5d36-152">Сертификат безопасности</span><span class="sxs-lookup"><span data-stu-id="d5d36-152">Security certificate</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-153">Выберите ранее созданный сертификат, чтобы дополнительно зашифровать связь между веб-службами и сервером, на котором вы настраиваете веб-сайты.</span><span class="sxs-lookup"><span data-stu-id="d5d36-153">Select a previously created certificate to optionally encrypt the communication between the web services and the server on which you are configuring the websites.</span></span> <span data-ttu-id="d5d36-154">Если вы выберете параметр <strong> не использовать сертификат </strong> , ваш веб-канал может быть небезопасным.</span><span class="sxs-lookup"><span data-stu-id="d5d36-154">If you choose <strong>Do not use a certificate</strong>, your web communication may not be secure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="d5d36-155">Имя узла</span><span class="sxs-lookup"><span data-stu-id="d5d36-155">Host name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-156">Имя главного компьютера, на котором вы настраиваете веб-сайты.</span><span class="sxs-lookup"><span data-stu-id="d5d36-156">Name of the host computer where you are configuring the websites.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="d5d36-157">Путь установки</span><span class="sxs-lookup"><span data-stu-id="d5d36-157">Installation path</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-158">Путь к папке, в которую устанавливаются веб-сайты.</span><span class="sxs-lookup"><span data-stu-id="d5d36-158">Path where you are installing the websites.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="d5d36-159">Port</span><span class="sxs-lookup"><span data-stu-id="d5d36-159">Port</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-160">Номер порта, используемый для связи с веб-сайтом и службами.</span><span class="sxs-lookup"><span data-stu-id="d5d36-160">Port number to use for website and service communication.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="d5d36-161">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d5d36-161">Note</span></span></strong><br/><p><span data-ttu-id="d5d36-162">Необходимо настроить исключение брандмауэра, чтобы разрешить связь через указанный порт.</span><span class="sxs-lookup"><span data-stu-id="d5d36-162">You must set a firewall exception to enable communication through the specified port.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="d5d36-163">Учетная запись домена и пароль для пула приложений веб-службы</span><span class="sxs-lookup"><span data-stu-id="d5d36-163">Web service application pool domain account and password</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-164">Учетная запись пользователя домена и пароль для пула приложений веб-службы.</span><span class="sxs-lookup"><span data-stu-id="d5d36-164">Domain user account and password for the web service application pool.</span></span></p>
   <p><span data-ttu-id="d5d36-165">Если вы ввели имя пользователя в поле " <strong> пользователь или группа домена доступа для чтения и записи" </strong> на <strong> странице "Настройка баз данных" </strong> , необходимо ввести это же значение в это поле.</span><span class="sxs-lookup"><span data-stu-id="d5d36-165">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="d5d36-166">Если вы ввели имя группы в <strong> поле пользователя или группы домена "доступ для чтения и записи" </strong> на <strong> странице "Настройка баз данных" </strong> , то значение, введенное в этом поле, должно быть членом этой группы.</span><span class="sxs-lookup"><span data-stu-id="d5d36-166">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="d5d36-167">Если вы не указали учетные данные, будет использоваться учетная запись, указанная для любого ранее включенного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d5d36-167">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="d5d36-168">Все веб-приложения должны использовать одни и те же учетные данные пула приложений.</span><span class="sxs-lookup"><span data-stu-id="d5d36-168">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="d5d36-169">Если вы укажете разные учетные данные для разных веб-приложений, будет использоваться Последнее указанное значение.</span><span class="sxs-lookup"><span data-stu-id="d5d36-169">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="d5d36-170">Важно.</span><span class="sxs-lookup"><span data-stu-id="d5d36-170">Important</span></span></strong><br/><p><span data-ttu-id="d5d36-171">Для повышения безопасности настройте учетную запись, указанную в учетных данных, с ограниченными правами пользователя.</span><span class="sxs-lookup"><span data-stu-id="d5d36-171">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span> <span data-ttu-id="d5d36-172">Кроме того, установите для пароля учетной записи значение бессрочной.</span><span class="sxs-lookup"><span data-stu-id="d5d36-172">Also, set the password of the account to never expire.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="d5d36-173">Убедитесь в том, что встроенная учетная запись IIS \ _IUSRS или учетная запись пула приложений добавлена в средство **олицетворения клиента после проверки подлинности** и локальных параметров безопасности для **входа в качестве пакетного задания** .</span><span class="sxs-lookup"><span data-stu-id="d5d36-173">Verify that the built-in IIS\_IUSRS account or the application pool account has been added to the **Impersonate a client after authentication** and the **Log on as a batch job** local security settings.</span></span>

   <span data-ttu-id="d5d36-174">Чтобы убедиться в том, что он был добавлен к локальным параметрам безопасности, откройте **Редактор локальной политики безопасности**, разверните узел **Локальные политики** , щелкните узел **Назначение прав пользователя** и дважды щелкните команду **Олицетворять клиента после проверки подлинности** и войдите в систему **как правила пакетных заданий** в области справа.</span><span class="sxs-lookup"><span data-stu-id="d5d36-174">To check whether it has been added to the local security settings, open the **Local Security Policy editor**, expand the **Local Policies** node, click the **User Rights Assignment** node, and double-click **Impersonate a client after authentication** and **Log on as a batch job** policies in the right pane.</span></span>

**<span data-ttu-id="d5d36-175">Настройка сведений о соединении для баз данных с помощью мастера</span><span class="sxs-lookup"><span data-stu-id="d5d36-175">To configure connection information for the databases by using the wizard</span></span>**

1.  <span data-ttu-id="d5d36-176">Используйте следующие описания полей для настройки сведений о соединении в мастере для базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="d5d36-176">Use the following field descriptions to configure the connection information in the wizard for the Compliance and Audit Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="d5d36-177">Поле</span><span class="sxs-lookup"><span data-stu-id="d5d36-177">Field</span></span></th>
    <th align="left"><span data-ttu-id="d5d36-178">Описание</span><span class="sxs-lookup"><span data-stu-id="d5d36-178">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="d5d36-179">Имя сервера SQL Server</span><span class="sxs-lookup"><span data-stu-id="d5d36-179">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="d5d36-180">Имя сервера, на котором настроена база данных соответствия и аудита.</span><span class="sxs-lookup"><span data-stu-id="d5d36-180">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="d5d36-181">Экземпляр базы данных SQL Server</span><span class="sxs-lookup"><span data-stu-id="d5d36-181">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="d5d36-182">Имя экземпляра SQL Server, на котором настроена конфигурация базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="d5d36-182">SQL Server instance name where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="d5d36-183">Имя базы данных</span><span class="sxs-lookup"><span data-stu-id="d5d36-183">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="d5d36-184">Имя базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="d5d36-184">Name of the Compliance and Audit Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="d5d36-185">Используйте следующие описания полей для настройки сведений о подключении в мастере для базы данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="d5d36-185">Use the following field descriptions to configure the connection information in the wizard for the Recovery Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="d5d36-186">Поле</span><span class="sxs-lookup"><span data-stu-id="d5d36-186">Field</span></span></th>
    <th align="left"><span data-ttu-id="d5d36-187">Описание</span><span class="sxs-lookup"><span data-stu-id="d5d36-187">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="d5d36-188">Имя сервера SQL Server</span><span class="sxs-lookup"><span data-stu-id="d5d36-188">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="d5d36-189">Имя сервера, на котором настроена база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="d5d36-189">Name of the server where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="d5d36-190">Экземпляр базы данных SQL Server</span><span class="sxs-lookup"><span data-stu-id="d5d36-190">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="d5d36-191">Имя экземпляра SQL Server, на котором настроена база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="d5d36-191">SQL Server instance name where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="d5d36-192">Имя базы данных</span><span class="sxs-lookup"><span data-stu-id="d5d36-192">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="d5d36-193">Имя базы данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="d5d36-193">Name of the Recovery Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="d5d36-194">Настройка веб-приложений с помощью мастера</span><span class="sxs-lookup"><span data-stu-id="d5d36-194">To configure the web applications by using the wizard</span></span>**

1. <span data-ttu-id="d5d36-195">Используйте следующие описания для ввода значений полей в мастере, чтобы настроить веб-сайт администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="d5d36-195">Use the following descriptions to enter the field values in the wizard to configure the Administration and Monitoring Website.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="d5d36-196">Поле</span><span class="sxs-lookup"><span data-stu-id="d5d36-196">Field</span></span></th>
   <th align="left"><span data-ttu-id="d5d36-197">Описание</span><span class="sxs-lookup"><span data-stu-id="d5d36-197">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="d5d36-198">Группа домена "Расширенная роль в справочной службе"</span><span class="sxs-lookup"><span data-stu-id="d5d36-198">Advanced Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-199">Группа пользователей домена, у которой есть доступ ко всем областям на веб-сайте администрирования и наблюдения за исключением области "отчеты".</span><span class="sxs-lookup"><span data-stu-id="d5d36-199">Domain user group whose members have access to all areas of the Administration and Monitoring Website except the Reports area.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="d5d36-200">Группа домена "роль в справочной службе"</span><span class="sxs-lookup"><span data-stu-id="d5d36-200">Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-201">Группа пользователей домена, у которых есть доступ к <strong> </strong> <strong> разделу Управление областями восстановления доверенных платформенных устройств и дисков на </strong> веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="d5d36-201">Domain user group whose members have access to the <strong>Manage TPM</strong> and <strong>Drive Recovery</strong> areas of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="d5d36-202">Использование интеграции System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d5d36-202">Use System Center Configuration Manager Integration</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-203">Установите этот флажок, если вы настраиваете MBAM с помощью топологии интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d5d36-203">Select this check box if you are configuring MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="d5d36-204">При установке этого флажка все отчеты, кроме отчета об аудите восстановления, отображаются в диспетчере конфигураций, а не на веб-сайте администрирования и наблюдения.</span><span class="sxs-lookup"><span data-stu-id="d5d36-204">Selecting this check box makes all reports, except the Recovery Audit report, appear in Configuration Manager instead of in the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="d5d36-205">Группа домена "роль отчета"</span><span class="sxs-lookup"><span data-stu-id="d5d36-205">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-206">Группа пользователей домена, у участников которой есть доступ только для чтения к области "отчеты" на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="d5d36-206">Domain user group whose members have read-only access to the Reports area of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="d5d36-207">URL-адрес служб SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="d5d36-207">SQL Server Reporting Services URL</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-208">URL-адрес сервера служб SSRS, на котором настроены отчеты MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5d36-208">URL for the SSRS server where the MBAM Reports are configured.</span></span></p>
   <p><span data-ttu-id="d5d36-209">Примеры URL-адресов отчета:</span><span class="sxs-lookup"><span data-stu-id="d5d36-209">Examples of report URLs:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="d5d36-210">Тип имени узла</span><span class="sxs-lookup"><span data-stu-id="d5d36-210">Type of host name</span></span></th>
   <th align="left"><span data-ttu-id="d5d36-211">Пример.</span><span class="sxs-lookup"><span data-stu-id="d5d36-211">Example</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="d5d36-212">Пример с полным доменным именем</span><span class="sxs-lookup"><span data-stu-id="d5d36-212">Example with a fully qualified domain name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="d5d36-213">Пример с именем настраиваемого узла</span><span class="sxs-lookup"><span data-stu-id="d5d36-213">Example with a custom host name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="d5d36-214">Виртуальный каталог</span><span class="sxs-lookup"><span data-stu-id="d5d36-214">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-215">Виртуальный каталог на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="d5d36-215">Virtual directory of the Administration and Monitoring Website.</span></span> <span data-ttu-id="d5d36-216">Это имя соответствует физическому каталогу веб-сайта на сервере и добавляется к имени узла веб-сайта, например:</span><span class="sxs-lookup"><span data-stu-id="d5d36-216">This name corresponds to the website’s physical directory on the server and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="d5d36-217">HTTP (s):// &lt; <em> HostName </em> &gt; : &lt; <em> Port </em> &gt; /HelpDesk/</span><span class="sxs-lookup"><span data-stu-id="d5d36-217">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/HelpDesk/</span></span></p>
   <p><span data-ttu-id="d5d36-218">Если вы не укажете виртуальный каталог, <strong> будет использоваться служба поддержки по стоимости </strong> .</span><span class="sxs-lookup"><span data-stu-id="d5d36-218">If you do not specify a virtual directory, the value <strong>HelpDesk</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="d5d36-219">Группа домена роль миграции данных </strong> (необязательный)</span><span class="sxs-lookup"><span data-stu-id="d5d36-219">Data Migration role domain group</strong> (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-220">Группа пользователей домена, у которых есть доступ к данным о восстановлении через эту конечную точку, с помощью командлетов Write-MBAM \* Information.</span><span class="sxs-lookup"><span data-stu-id="d5d36-220">Domain user group whose members have access to use the Write-Mbam\*Information Cmdlets to write recovery information via this endpoint.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="d5d36-221">Для ввода значений полей в мастере для настройки портала самообслуживания используйте следующее описание.</span><span class="sxs-lookup"><span data-stu-id="d5d36-221">Use the following description to enter the field values in the wizard to configure the Self-Service Portal.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="d5d36-222">Поле</span><span class="sxs-lookup"><span data-stu-id="d5d36-222">Field</span></span></th>
   <th align="left"><span data-ttu-id="d5d36-223">Описание</span><span class="sxs-lookup"><span data-stu-id="d5d36-223">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="d5d36-224">Виртуальный каталог</span><span class="sxs-lookup"><span data-stu-id="d5d36-224">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-225">Виртуальный каталог веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d5d36-225">Virtual directory of the web application.</span></span> <span data-ttu-id="d5d36-226">Это имя соответствует физическому каталогу веб-сайта на сервере и добавляется к имени узла веб-сайта, например:</span><span class="sxs-lookup"><span data-stu-id="d5d36-226">This name corresponds to the website’s physical directory on the server, and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="d5d36-227">HTTP (s):// &lt; <em> HostName </em> &gt; : &lt; <em> Port </em> &gt; /Selfservice/</span><span class="sxs-lookup"><span data-stu-id="d5d36-227">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/SelfService/</span></span></p>
   <p><span data-ttu-id="d5d36-228">Если вы не указали виртуальный каталог, <strong> будет использоваться значение Selfservice </strong> .</span><span class="sxs-lookup"><span data-stu-id="d5d36-228">If you do not specify a virtual directory, the value <strong>SelfService</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="d5d36-229">Название организации</span><span class="sxs-lookup"><span data-stu-id="d5d36-229">Company name</span></span></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-230">Укажите название компании для портала самообслуживания, например:</span><span class="sxs-lookup"><span data-stu-id="d5d36-230">Specify a company name for the Self-Service Portal, for example:</span></span></p>
   <p><span data-ttu-id="d5d36-231">Contoso IT</span><span class="sxs-lookup"><span data-stu-id="d5d36-231">Contoso IT</span></span></p>
   <p><span data-ttu-id="d5d36-232">Это название компании отображается для всех пользователей портала самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="d5d36-232">This company name is viewed by all Self-Service Portal users.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="d5d36-233">Текст URL-адреса службы поддержки</span><span class="sxs-lookup"><span data-stu-id="d5d36-233">Helpdesk URL text</span></span></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-234">Укажите текстовую инструкцию, которая направляет пользователей на веб-сайт службы поддержки Организации, например:</span><span class="sxs-lookup"><span data-stu-id="d5d36-234">Specify a text statement that directs users to your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="d5d36-235">Обращение в службу технической поддержки или ИТ-отдел</span><span class="sxs-lookup"><span data-stu-id="d5d36-235">Contact Helpdesk or IT department</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="d5d36-236">URL-адрес службы поддержки</span><span class="sxs-lookup"><span data-stu-id="d5d36-236">Helpdesk URL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-237">Укажите URL-адрес сайта технической поддержки своей организации, например:</span><span class="sxs-lookup"><span data-stu-id="d5d36-237">Specify the URL for your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="d5d36-238">HTTP (s):// &lt; <em> companyHelpdeskURL</em>&gt;/</span><span class="sxs-lookup"><span data-stu-id="d5d36-238">http(s)://&lt;<em>companyHelpdeskURL</em>&gt;/</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="d5d36-239">Текстовый файл с примечанием</span><span class="sxs-lookup"><span data-stu-id="d5d36-239">Notice text file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-240">Выберите файл, содержащий уведомление, которое должно отображаться для пользователей на начальной странице портала самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="d5d36-240">Select a file that contains the notice you want displayed to users on the Self-Service Portal landing page.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="d5d36-241">Не отображать текст уведомления для пользователей</span><span class="sxs-lookup"><span data-stu-id="d5d36-241">Do not display notice text to users</span></span></p></td>
   <td align="left"><p><span data-ttu-id="d5d36-242">Установите этот флажок, чтобы указать, что текст уведомления не отображается для пользователей.</span><span class="sxs-lookup"><span data-stu-id="d5d36-242">Select this check box to specify that the notice text is not displayed to users.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="d5d36-243">Когда вы закончите ввод, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d5d36-243">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="d5d36-244">Мастер проверяет, выполнены ли все необходимые условия для веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="d5d36-244">The wizard checks that all prerequisites for the web applications have been met.</span></span>

4. <span data-ttu-id="d5d36-245">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d5d36-245">Click **Next** to continue.</span></span>

5. <span data-ttu-id="d5d36-246">На странице **сводки** ознакомьтесь с возможностями, которые будут добавлены.</span><span class="sxs-lookup"><span data-stu-id="d5d36-246">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="d5d36-247">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d5d36-247">Note</span></span>**  
   <span data-ttu-id="d5d36-248">Чтобы создать сценарий Windows PowerShell для записей, которые вы создали, нажмите **экспортировать сценарий PowerShell** и сохранить сценарий.</span><span class="sxs-lookup"><span data-stu-id="d5d36-248">To create a Windows PowerShell script for the entries you made, click **Export PowerShell Script** and save the script.</span></span>



6. <span data-ttu-id="d5d36-249">Нажмите кнопку **Добавить** , чтобы добавить веб-приложения на сервер, а затем нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="d5d36-249">Click **Add** to add the web applications to the server, and then click **Close**.</span></span>

   <span data-ttu-id="d5d36-250">Чтобы настроить портал самообслуживания, добавив настраиваемый текст уведомления, название компании, ссылки на дополнительные сведения и т. д., ознакомьтесь с [Разстройкой портала самообслуживания для своей организации](customizing-the-self-service-portal-for-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="d5d36-250">To customize the Self-Service Portal by adding custom notice text, your company name, pointers to more information, and so on, see [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md).</span></span>

**<span data-ttu-id="d5d36-251">Настройка портала самообслуживания, если клиентские компьютеры не могут получить доступ к сети CDN</span><span class="sxs-lookup"><span data-stu-id="d5d36-251">To configure the Self-Service Portal if client computers cannot access the CDN</span></span>**

1.  <span data-ttu-id="d5d36-252">Определите, используете ли вы Microsoft BitLocker администрирование и мониторинг (MBAM) 2,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d5d36-252">Determine whether you are running Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="d5d36-253">Если да, ничего делать не нужно.</span><span class="sxs-lookup"><span data-stu-id="d5d36-253">If so, do nothing.</span></span> <span data-ttu-id="d5d36-254">Настройка портала самообслуживания завершена.</span><span class="sxs-lookup"><span data-stu-id="d5d36-254">Your Self-Service Portal configuration is complete.</span></span>

    **<span data-ttu-id="d5d36-255">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d5d36-255">Note</span></span>**  
    <span data-ttu-id="d5d36-256">Администрирование и мониторинг Microsoft BitLocker (MBAM) 2,5 с пакетом обновления 1 (SP1) устанавливает файлы JavaScript в настройке, поэтому для настройки портала самообслуживания не требуется подключение к сети доставки содержимого Microsoft AJAX.</span><span class="sxs-lookup"><span data-stu-id="d5d36-256">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 installs the JavaScript files in setup, and so does not need to be connected to the Microsoft Ajax Content Delivery Network in order to configure the Self-Service Portal.</span></span> <span data-ttu-id="d5d36-257">Описанные ниже действия необходимы только в том случае, если вы используете версию администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5, предшествующую пакету обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d5d36-257">The following steps are necessary only if you are using a version of Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 previous to SP1.</span></span>



2.  <span data-ttu-id="d5d36-258">Определение того, есть ли у клиентских компьютеров доступ к сети доставки содержимого (CDN) Microsoft AJAX.</span><span class="sxs-lookup"><span data-stu-id="d5d36-258">Determine if your client computers have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

    <span data-ttu-id="d5d36-259">Сеть CDN предоставляет порталу самообслуживания, доступ к которому требуется для определенных файлов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d5d36-259">The CDN gives the Self-Service Portal the access it requires to certain JavaScript files.</span></span> <span data-ttu-id="d5d36-260">Если вы не настраиваете портал самообслуживания, когда клиентские компьютеры не могут получить доступ к сети CDN, будет отображаться только название компании и учетная запись, под которой вошел конечный пользователь.</span><span class="sxs-lookup"><span data-stu-id="d5d36-260">If you don’t configure the Self-Service Portal when client computers cannot access the CDN, only the company name and the account under which the end user signed in will be displayed.</span></span> <span data-ttu-id="d5d36-261">Сообщение об ошибке не выводится.</span><span class="sxs-lookup"><span data-stu-id="d5d36-261">No error message will be shown.</span></span>

3.  <span data-ttu-id="d5d36-262">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="d5d36-262">Do one of the following:</span></span>

    -   <span data-ttu-id="d5d36-263">Если клиентские компьютеры имеют доступ к сети CDN, ничего делать не нужно.</span><span class="sxs-lookup"><span data-stu-id="d5d36-263">If your client computers have access to the CDN, do nothing.</span></span> <span data-ttu-id="d5d36-264">Настройка портала самообслуживания завершена.</span><span class="sxs-lookup"><span data-stu-id="d5d36-264">Your Self-Service Portal configuration is complete.</span></span>

    -   <span data-ttu-id="d5d36-265">Если клиентские компьютеры не имеют доступа к сети CDN, выполните действия, описанные в разделе [Настройка портала самообслуживания, когда клиентские компьютеры не могут получить доступ к Интернету для доставки содержимого](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span><span class="sxs-lookup"><span data-stu-id="d5d36-265">If your client computers do not have access to the CDN, complete the steps in [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>


## <span data-ttu-id="d5d36-266">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d5d36-266">Related topics</span></span>


[<span data-ttu-id="d5d36-267">Журналы событий сервера</span><span class="sxs-lookup"><span data-stu-id="d5d36-267">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="d5d36-268">Настройка компонентов сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="d5d36-268">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="d5d36-269">Настройка портала самообслуживания при отсутствии у клиентских компьютеров доступа к сети доставки содержимого корпорации Майкрософт</span><span class="sxs-lookup"><span data-stu-id="d5d36-269">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[<span data-ttu-id="d5d36-270">Настройка портала самообслуживания для организации</span><span class="sxs-lookup"><span data-stu-id="d5d36-270">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

[<span data-ttu-id="d5d36-271">Проверка конфигурации компонентов MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="d5d36-271">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="d5d36-272">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="d5d36-272">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d5d36-273">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="d5d36-273">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d5d36-274">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="d5d36-274">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





