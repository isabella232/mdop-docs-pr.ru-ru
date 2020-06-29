---
title: Настройка сервера для разрешения делегирования
description: Настройка сервера для разрешения делегирования
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817749"
---
# <span data-ttu-id="81664-103">Настройка сервера для разрешения делегирования</span><span class="sxs-lookup"><span data-stu-id="81664-103">How to Configure the Server to be Trusted for Delegation</span></span>


<span data-ttu-id="81664-104">При установке серверного программного обеспечения Microsoft Application Virtualization (App-V) Management Server вы можете установить его с помощью архитектуры распределенной системы.</span><span class="sxs-lookup"><span data-stu-id="81664-104">When you install the Microsoft Application Virtualization (App-V) Management Server software, you can choose to install it by using a distributed system architecture.</span></span> <span data-ttu-id="81664-105">Если вы установили консоль, веб-службу управления и базу данных на разных компьютерах, необходимо настроить сервер служб IIS таким образом, чтобы он был доверен для делегирования.</span><span class="sxs-lookup"><span data-stu-id="81664-105">If you install the console, the Management Web Service, and the database on different computers, you must configure the Internet Information Services (IIS) server to be trusted for delegation.</span></span> <span data-ttu-id="81664-106">Это необходимо, поскольку веб-служба управления пытается подключиться к хранилищу данных App-V с помощью учетных данных администратора App-V, использующего консоль.</span><span class="sxs-lookup"><span data-stu-id="81664-106">This is necessary because the Management Web Service will attempt to connect to the App-V data store by using the credentials of the App-V administrator who is using the console.</span></span> <span data-ttu-id="81664-107">Сервер базы данных, на котором установлен хранилище данных, не будет принимать учетные данные администратора сервера IIS, если только сервер IIS не настроен для делегирования, поэтому веб-служба управления не сможет подключаться к хранилищу данных App-V.</span><span class="sxs-lookup"><span data-stu-id="81664-107">The database server on which the data store is installed will not accept the administrator’s credentials from the IIS server unless the IIS server is configured to be trusted for delegation, and so the Management Web Service will not be able to connect to the App-V data store.</span></span>

<span data-ttu-id="81664-108">**Примечание**  Если вы установили программное обеспечение сервера управления App-V на одном сервере и размещаете хранилище данных на отдельном сервере, существует ситуация, когда необходимо настроить сервер для делегирования, даже если веб-служба управления и консоль управления находятся на одном и том же сервере.</span><span class="sxs-lookup"><span data-stu-id="81664-108">**Note** If you install the App-V Management Server software on a single server and place the data store on a separate server, there is one situation in which you must still configure the server to be trusted for delegation even though the Management Web Service and Management Console are on the same server.</span></span> <span data-ttu-id="81664-109">Эта ситуация возникает, если вам нужно подключиться к веб-службе управления на консоли с помощью параметра **использовать альтернативные учетные данные** .</span><span class="sxs-lookup"><span data-stu-id="81664-109">This situation occurs if you need to connect to the Management Web Service in the console by using the **Use Alternate Credentials** option.</span></span>

 

<span data-ttu-id="81664-110">Тип делегирования, который можно использовать, зависит от функционального уровня домена, настроенного в инфраструктуре доменных служб Active Directory (ADDS).</span><span class="sxs-lookup"><span data-stu-id="81664-110">The type of delegation that you can use depends on the Domain Functional Level that you have configured in your Active Directory Domain Services (ADDS) infrastructure.</span></span> <span data-ttu-id="81664-111">В следующей таблице перечислены типы делегирования, которые можно настроить для каждого функционального уровня для App-V.</span><span class="sxs-lookup"><span data-stu-id="81664-111">The following table lists the types of delegation that can be configured for each Domain Functional Level for App-V.</span></span> <span data-ttu-id="81664-112">Подробные инструкции следуют за таблицей.</span><span class="sxs-lookup"><span data-stu-id="81664-112">Detailed instructions follow the table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="81664-113">Функциональный уровень домена</span><span class="sxs-lookup"><span data-stu-id="81664-113">Domain Functional Level</span></span></th>
<th align="left"><span data-ttu-id="81664-114">Доступные уровни делегирования</span><span class="sxs-lookup"><span data-stu-id="81664-114">Delegation Levels Available</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81664-115">Windows 2000 Native</span><span class="sxs-lookup"><span data-stu-id="81664-115">Windows 2000 native</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="81664-116">Без делегирования (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81664-116">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="81664-117">Неограниченное делегирование</span><span class="sxs-lookup"><span data-stu-id="81664-117">Unconstrained delegation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81664-118">Windows Server 2003, Windows Server 2008 или Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="81664-118">Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="81664-119">Без делегирования (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81664-119">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="81664-120">Неограниченное делегирование ¹</span><span class="sxs-lookup"><span data-stu-id="81664-120">Unconstrained delegation¹</span></span></p></li>
<li><p><span data-ttu-id="81664-121">Ограниченное делегирование (использование протоколов Kerberos)</span><span class="sxs-lookup"><span data-stu-id="81664-121">Constrained delegation (Use Kerberos Only Protocols)</span></span></p></li>
<li><p><span data-ttu-id="81664-122">Ограниченное делегирование (использование любого протокола проверки подлинности) ¹</span><span class="sxs-lookup"><span data-stu-id="81664-122">Constrained delegation (Use any authentication protocol) ¹</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="81664-123">¹ не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="81664-123">¹ Not recommended.</span></span>

## <span data-ttu-id="81664-124">Настройка неограниченного делегирования при использовании режима работы домена в Windows 2000 Native</span><span class="sxs-lookup"><span data-stu-id="81664-124">To configure unconstrained delegation when the Domain Functional Level is Windows 2000 native</span></span>


<span data-ttu-id="81664-125">На контроллере домена вашего веб-сервера выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="81664-125">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="81664-126">Нажмите кнопку **Пуск**и выберите пункт **средства администрирования**, а затем — **Пользователи и компьютеры Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="81664-126">Click **Start**, **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="81664-127">Разверните домен, а затем разверните папку компьютеры.</span><span class="sxs-lookup"><span data-stu-id="81664-127">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="81664-128">На правой панели щелкните правой кнопкой мыши имя компьютера для веб-сервера и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="81664-128">In the right pane, right-click the computer name for the Web server, and then click **Properties**.</span></span>

4.  <span data-ttu-id="81664-129">Убедитесь, что на вкладке **Общие** установлен флажок **доверенный компьютер для делегирования** .</span><span class="sxs-lookup"><span data-stu-id="81664-129">On the **General** tab, ensure that the **Trust computer for delegation** check box is selected.</span></span>

5.  <span data-ttu-id="81664-130">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="81664-130">Click **OK**.</span></span>

## <span data-ttu-id="81664-131">Настройка неограниченного делегирования при установленном функциональном уровне домена Windows Server 2003, Windows Server 2008 или Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="81664-131">To configure unconstrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="81664-132">На контроллере домена вашего веб-сервера выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="81664-132">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="81664-133">Нажмите кнопку **Пуск**и выберите пункт **Администрирование**, а затем — **Пользователи и компьютеры Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="81664-133">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="81664-134">Разверните домен и разверните папку компьютеры.</span><span class="sxs-lookup"><span data-stu-id="81664-134">Expand domain, and expand the Computers folder.</span></span>

3.  <span data-ttu-id="81664-135">На правой панели щелкните правой кнопкой мыши имя компьютера для веб-сервера, выберите пункт **Свойства**, а затем откройте вкладку **Делегирование** .</span><span class="sxs-lookup"><span data-stu-id="81664-135">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="81664-136">Щелкните, чтобы выбрать параметр **доверять этому компьютеру для делегирования служб (только Kerberos)**.</span><span class="sxs-lookup"><span data-stu-id="81664-136">Click to select **Trust this computer for delegation to any service (Kerberos only)**.</span></span>

5.  <span data-ttu-id="81664-137">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="81664-137">Click **OK**.</span></span>

## <span data-ttu-id="81664-138">Настройка ограниченного делегирования при использовании функционального уровня домена Windows Server 2003, Windows Server 2008 или Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="81664-138">To configure constrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="81664-139">На контроллере домена вашего веб-сервера выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="81664-139">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="81664-140">Нажмите кнопку **Пуск**и выберите пункт **Администрирование**, а затем — **Пользователи и компьютеры Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="81664-140">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="81664-141">Разверните домен, а затем разверните папку компьютеры.</span><span class="sxs-lookup"><span data-stu-id="81664-141">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="81664-142">На правой панели щелкните правой кнопкой мыши имя компьютера для веб-сервера, выберите пункт **Свойства**, а затем откройте вкладку **Делегирование** .</span><span class="sxs-lookup"><span data-stu-id="81664-142">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="81664-143">Выберите этот пункт, чтобы сделать **этот компьютер доверенным для делегирования указанных служб**.</span><span class="sxs-lookup"><span data-stu-id="81664-143">Click to select **Trust this computer for delegation to specified services only**.</span></span>

5.  <span data-ttu-id="81664-144">Убедитесь, что установлен флажок **использовать только Kerberos** , и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="81664-144">Ensure that **Use Kerberos only** is selected, and then click **OK**.</span></span>

6.  <span data-ttu-id="81664-145">Нажмите кнопку **Добавить** .</span><span class="sxs-lookup"><span data-stu-id="81664-145">Click the **Add** button.</span></span> <span data-ttu-id="81664-146">В диалоговом окне **Добавление служб** выберите пункт **Пользователи или компьютеры**, найдите или введите имя сервера Microsoft SQL Server, на котором находится хранилище данных App-V, и получите учетные данные пользователей из IIS.</span><span class="sxs-lookup"><span data-stu-id="81664-146">In the **Add Services** dialog box, click **Users or Computers**, and then browse to or type the name of the Microsoft SQL server that has the App-V data store and is to receive the users credentials from IIS.</span></span> <span data-ttu-id="81664-147">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="81664-147">Click **OK**.</span></span>

7.  <span data-ttu-id="81664-148">В списке **Доступные службы** выберите службу MSSQLSvc, которая содержит номер порта, на котором Microsoft SQL Server принимает соединения для базы данных App-V (порт по умолчанию — 1433).</span><span class="sxs-lookup"><span data-stu-id="81664-148">In the **Available Services** list, select the MSSQLSvc service that lists port number on which the Microsoft SQL Server is accepting connections for the App-V database (the default port is 1433).</span></span> <span data-ttu-id="81664-149">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="81664-149">Click **OK**.</span></span>

### <span data-ttu-id="81664-150">Дополнительные действия по настройке служб IIS 7 для ограниченного делегирования</span><span class="sxs-lookup"><span data-stu-id="81664-150">Additional steps to configure IIS 7 for constrained delegation</span></span>

<span data-ttu-id="81664-151">Если вы используете веб-службу управления на сервере IIS 7, необходимо выполнить описанные ниже действия, чтобы установить для переменной IIS 7 *UseAppPoolCredentials* значение true.</span><span class="sxs-lookup"><span data-stu-id="81664-151">If you are running the Management Web Service on an IIS 7 server, you must complete the following steps to set the IIS 7 *useAppPoolCredentials* variable to True.</span></span>

1.  <span data-ttu-id="81664-152">Откройте окно командной строки с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="81664-152">Open an elevated Command Prompt window.</span></span> <span data-ttu-id="81664-153">Чтобы открыть окно командной строки с повышенными привилегиями, нажмите кнопку **Пуск**, выберите **все программы**, затем **стандартные**, щелкните правой кнопкой мыши **Командная строка**и выберите пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="81664-153">To open an elevated Command Prompt window, click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="81664-154">Переход к%WINDIR%\\system32\\inetsrv.</span><span class="sxs-lookup"><span data-stu-id="81664-154">Navigate to %windir%\\system32\\inetsrv.</span></span>

3.  <span data-ttu-id="81664-155">Введите **appcmd.exe set config-Section: System. Web Server/Security/Authentication/windowsAuthentication-useAppPoolCredentials: true**, а затем нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="81664-155">Type **appcmd.exe set config -section:system.webServer/security/authentication/windowsAuthentication -useAppPoolCredentials:true**, and then press ENTER.</span></span>

 

 





