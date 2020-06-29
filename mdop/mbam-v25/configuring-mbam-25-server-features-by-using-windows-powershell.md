---
title: Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell
description: Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822839"
---
# <span data-ttu-id="3233d-103">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3233d-103">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>


<span data-ttu-id="3233d-104">После установки программного обеспечения сервера MBAM 2,5 вы можете настроить серверные компоненты MBAM 2,5 с помощью командлетов Windows PowerShell или мастера конфигурации сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="3233d-104">After you install the MBAM 2.5 Server software, you can use configure MBAM 2.5 Server features by using Windows PowerShell cmdlets or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="3233d-105">В этой статье описано, как настроить MBAM 2,5 с помощью командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3233d-105">This topic describes how to configure MBAM 2.5 by using the Windows PowerShell cmdlets.</span></span> <span data-ttu-id="3233d-106">Чтобы использовать мастер, ознакомьтесь с [Разстройкой функций сервера MBAM 2,5](configuring-the-mbam-25-server-features.md).</span><span class="sxs-lookup"><span data-stu-id="3233d-106">To use the wizard instead, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md).</span></span>

## <span data-ttu-id="3233d-107">В этой статье</span><span class="sxs-lookup"><span data-stu-id="3233d-107">In this topic</span></span>


<span data-ttu-id="3233d-108">В этой статье приведены сведения об использовании Windows PowerShell для настройки MBAM:</span><span class="sxs-lookup"><span data-stu-id="3233d-108">This topic includes the following information about using Windows PowerShell to configure MBAM:</span></span>

-   [<span data-ttu-id="3233d-109">Как загрузить справку по Windows PowerShell для MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="3233d-109">How to load Windows PowerShell Help for MBAM 2.5</span></span>](#bkmk-load-posh-help)

-   [<span data-ttu-id="3233d-110">Получение справки о командлете Windows PowerShell MBAM</span><span class="sxs-lookup"><span data-stu-id="3233d-110">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>](#bkmk-help-specific-cmdlet)

-   [<span data-ttu-id="3233d-111">Конфигурации, которые можно выполнять только с Windows PowerShell, но не с помощью мастера конфигурации сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="3233d-111">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>](#bkmk-config-only-posh)

-   [<span data-ttu-id="3233d-112">Необходимые условия и требования для использования Windows PowerShell для настройки функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="3233d-112">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>](#bkmk-prereqs-posh-mbamsvr)

-   [<span data-ttu-id="3233d-113">Настройка MBAM на удаленном компьютере с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3233d-113">Using Windows PowerShell to configure MBAM on a remote computer</span></span>](#bkmk-remote-config)

-   [<span data-ttu-id="3233d-114">Обязательные учетные записи и соответствующие параметры командлета Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3233d-114">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>](#bkmk-reqd-posh-accts)

<span data-ttu-id="3233d-115">Дополнительные сведения о командлетах Windows PowerShell **Get-MbamBitLockerRecoveryKey** и **Get-MbamTPMOwnerPassword** , которые используются для управления MBAM, приведены в разделе [Использование Windows PowerShell для администрирования MBAM 2,5](using-windows-powershell-to-administer-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="3233d-115">For information about the **Get-MbamBitLockerRecoveryKey** and **Get-MbamTPMOwnerPassword** Windows PowerShell cmdlets, which are used to administer MBAM, see [Using Windows PowerShell to Administer MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md).</span></span>

## <a href="" id="bkmk-load-posh-help"></a><span data-ttu-id="3233d-116">Как загрузить справку по Windows PowerShell для MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="3233d-116">How to load Windows PowerShell Help for MBAM 2.5</span></span>


<span data-ttu-id="3233d-117">Список командлетов Windows PowerShell на веб-сайте TechNet можно найти в разделе [Автоматизация пакета оптимизации рабочей среды Microsoft для Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span><span class="sxs-lookup"><span data-stu-id="3233d-117">For a list of the Windows PowerShell cmdlets on TechNet, see [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span></span>

**<span data-ttu-id="3233d-118">Загрузка справки по MBAM 2,5 для командлетов Windows PowerShell после установки серверного программного обеспечения MBAM</span><span class="sxs-lookup"><span data-stu-id="3233d-118">To load the MBAM 2.5 Help for Windows PowerShell cmdlets after installing the MBAM Server software</span></span>**

1.  <span data-ttu-id="3233d-119">Откройте Windows PowerShell или интегрированную среду сценариев Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="3233d-119">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="3233d-120">Введите **Update-Help-Module Microsoft. MBAM**.</span><span class="sxs-lookup"><span data-stu-id="3233d-120">Type **Update-Help –Module Microsoft.MBAM**.</span></span>

## <a href="" id="bkmk-help-specific-cmdlet"></a><span data-ttu-id="3233d-121">Получение справки о командлете Windows PowerShell MBAM</span><span class="sxs-lookup"><span data-stu-id="3233d-121">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>


<span data-ttu-id="3233d-122">Справка по Windows PowerShell для MBAM доступна в следующих форматах:</span><span class="sxs-lookup"><span data-stu-id="3233d-122">Windows PowerShell Help for MBAM is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3233d-123">Формат справки Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3233d-123">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="3233d-124">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3233d-124">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3233d-125">В командной строке Windows PowerShell введите <strong> </strong> &lt; <em> командлет Get-Help</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="3233d-125">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="3233d-126">Чтобы загрузить последние командлеты Windows PowerShell, следуйте инструкциям, приведенным в предыдущем разделе о том, как загрузить справку Windows PowerShell для MBAM.</span><span class="sxs-lookup"><span data-stu-id="3233d-126">To upload the latest Windows PowerShell cmdlets, follow the instructions in the previous section on how to load Windows PowerShell Help for MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3233d-127">На веб-страницах TechNet.</span><span class="sxs-lookup"><span data-stu-id="3233d-127">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3233d-128">В центре загрузки как файл Word. docx</span><span class="sxs-lookup"><span data-stu-id="3233d-128">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3233d-129">В центре загрузки в виде PDF-файла</span><span class="sxs-lookup"><span data-stu-id="3233d-129">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a><span data-ttu-id="3233d-130">Конфигурации, которые можно выполнять только с Windows PowerShell, но не с помощью мастера конфигурации сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="3233d-130">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3233d-131">Конфигурации, которые можно выполнять только с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3233d-131">Configurations that you can do only by using Windows PowerShell</span></span></th>
<th align="left"><span data-ttu-id="3233d-132">Сведения</span><span class="sxs-lookup"><span data-stu-id="3233d-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3233d-133">Установите веб-службы на отдельном компьютере из веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="3233d-133">Install the web services on a separate computer from the web applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3233d-134">С помощью мастера необходимо установить веб-службы и веб-приложения на одном и том же компьютере.</span><span class="sxs-lookup"><span data-stu-id="3233d-134">Using the wizard, you must install the web services and web applications on the same computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3233d-135">Разрешите отчеты на отдельной точке служб Reporting Services, не устанавливая все объекты Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3233d-135">Enable reports on a separate reporting services point without installing all of the Configuration Manager objects.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3233d-136">Удалите все объекты из Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3233d-136">Delete all of the objects from Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3233d-137">В свою очередь, удаление объектов приводит к удалению всех данных о соответствии из Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3233d-137">Deleting the objects in turn deletes all of the compliance data from Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3233d-138">Введите специальную строку подключения для баз данных.</span><span class="sxs-lookup"><span data-stu-id="3233d-138">Enter a custom connection string for the databases.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3233d-139">Пример: чтобы настроить веб-приложения для работы с зеркальным отображением, необходимо использовать <strong> командлет Enable-MbamWebApplication, </strong> чтобы указать в строке соединения соответствующий синтаксис для резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3233d-139">Example: To configure the web applications to work with mirroring, you must use the <strong>Enable-MbamWebApplication</strong> cmdlet to specify the appropriate failover partner syntax in the connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3233d-140">Пропустить проверку и настроить функцию, несмотря на то, что проверка готовности к установке завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="3233d-140">Skip validation and configure a feature even though the prerequisite check failed.</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3233d-141">**Примечание**  Вы не можете отключить базы данных MBAM с помощью командлета Windows PowerShell или мастера настройки сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="3233d-141">**Note** You cannot disable the MBAM databases with a Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="3233d-142">Чтобы предотвратить случайное удаление данных о соответствии и аудите, администраторы баз данных должны удалить базы данных вручную.</span><span class="sxs-lookup"><span data-stu-id="3233d-142">To prevent the accidental removal of your compliance and audit data, database administrators must remove databases manually.</span></span>

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a><span data-ttu-id="3233d-143">Необходимые условия и требования для использования Windows PowerShell для настройки функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="3233d-143">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>


<span data-ttu-id="3233d-144">Перед началом настройки выполните следующие предварительные требования.</span><span class="sxs-lookup"><span data-stu-id="3233d-144">Before starting the configuration, complete the following prerequisites.</span></span>

**<span data-ttu-id="3233d-145">Необходимые для учетной записи требования</span><span class="sxs-lookup"><span data-stu-id="3233d-145">Account-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3233d-146">Предварительные</span><span class="sxs-lookup"><span data-stu-id="3233d-146">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="3233d-147">Сведения или дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3233d-147">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3233d-148">Создайте необходимые учетные записи.</span><span class="sxs-lookup"><span data-stu-id="3233d-148">Create the required accounts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3233d-149">Ознакомьтесь с <strong> необходимыми учетными записями и соответствующими параметрами командлета Windows PowerShell </strong> позже в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="3233d-149">See section <strong>Required accounts and corresponding Windows PowerShell cmdlet parameters</strong> later in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3233d-150">Учетные записи пользователей и группы, передаваемые в качестве параметров командлетам Windows PowerShell, должны быть действительными учетными записями домена.</span><span class="sxs-lookup"><span data-stu-id="3233d-150">User accounts and groups that you pass as parameters to the Windows PowerShell cmdlets must be valid accounts in the domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3233d-151">Нельзя использовать локальные учетные записи.</span><span class="sxs-lookup"><span data-stu-id="3233d-151">You cannot use local accounts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3233d-152">Укажите учетные записи в формате нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="3233d-152">Specify accounts in the down-level format.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3233d-153">Примеры:</span><span class="sxs-lookup"><span data-stu-id="3233d-153">Examples:</span></span></p>
<p><span data-ttu-id="3233d-154">domainNetBiosName\userdomainNetBiosName\group</span><span class="sxs-lookup"><span data-stu-id="3233d-154">domainNetBiosName\userdomainNetBiosName\group</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="3233d-155">Требования, связанные с разрешениями</span><span class="sxs-lookup"><span data-stu-id="3233d-155">Permission-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3233d-156">Предварительные</span><span class="sxs-lookup"><span data-stu-id="3233d-156">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="3233d-157">Сведения или дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3233d-157">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3233d-158">Вы должны быть администратором на локальном компьютере, на котором вы настраиваете функцию MBAM.</span><span class="sxs-lookup"><span data-stu-id="3233d-158">You must be an administrator on the local computer where you are configuring the MBAM feature.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3233d-159">Используйте командную команду Windows PowerShell с повышенными привилегиями, чтобы выполнить все командлеты Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3233d-159">Use an elevated Windows PowerShell command prompt to run all Windows PowerShell cmdlets.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3233d-160">Только для <strong> командлета Enable-MbamDatabase </strong> :</span><span class="sxs-lookup"><span data-stu-id="3233d-160">For the <strong>Enable-MbamDatabase</strong> cmdlet only:</span></span></p>
<p><span data-ttu-id="3233d-161">Вы должны иметь &quot; разрешения на создание всех баз данных &quot; для экземпляра целевой базы данных Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3233d-161">You must have &quot;create any database&quot; permissions on the instance of the target Microsoft SQL Server database.</span></span></p>
<p><span data-ttu-id="3233d-162">Эта учетная запись пользователя должна входить в локальную группу администраторов или группу "операторы резервного копирования", чтобы зарегистрировать средство записи MBAM (VSS) Service Writer (служба теневого копирования тома).</span><span class="sxs-lookup"><span data-stu-id="3233d-162">This user account must be a part of the local administrators group or the Backup Operators group to register the MBAM Volume Shadow Copy Service (VSS) Writer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3233d-163">По умолчанию администратор базы данных или системный администратор обладает необходимыми &quot; разрешениями на создание баз данных &quot; .</span><span class="sxs-lookup"><span data-stu-id="3233d-163">By default, the database administrator or system administrator has the required &quot;create any database&quot; permissions.</span></span></p>
<p></p>
<p><span data-ttu-id="3233d-164">Дополнительные сведения о средстве записи VSS можно найти в разделе <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> Служба теневого копирования тома </a> .</span><span class="sxs-lookup"><span data-stu-id="3233d-164">For more information about VSS Writer, see <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)">Volume Shadow Copy Service</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3233d-165">Для <strong> компонента интеграции System Center Configuration Manager </strong> :</span><span class="sxs-lookup"><span data-stu-id="3233d-165">For the <strong>System Center Configuration Manager Integration</strong> feature only:</span></span></p>
<p><span data-ttu-id="3233d-166">У пользователя, который включает эту функцию, должны быть следующие права в Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="3233d-166">The user who enables this feature must have these rights in Configuration Manager:</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3233d-167">Тип прав в Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="3233d-167">Type of rights in Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="3233d-168">Необходимые права</span><span class="sxs-lookup"><span data-stu-id="3233d-168">Required rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3233d-169">Права сайтов Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="3233d-169">Configuration Manager Site rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="3233d-170">Read</span><span class="sxs-lookup"><span data-stu-id="3233d-170">Read</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3233d-171">Права на сбор Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="3233d-171">Configuration Manager Collection rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="3233d-172">Создание, удаление, изменение и развертывание элементов конфигурации</span><span class="sxs-lookup"><span data-stu-id="3233d-172">Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3233d-173">Разрешения элемента конфигурации Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="3233d-173">Configuration Manager Configuration item rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="3233d-174">Создание-удаление — чтение</span><span class="sxs-lookup"><span data-stu-id="3233d-174">Create- Delete- Read</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a><span data-ttu-id="3233d-175">Настройка MBAM на удаленном компьютере с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3233d-175">Using Windows PowerShell to configure MBAM on a remote computer</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3233d-176">Когда следует использовать эту возможность</span><span class="sxs-lookup"><span data-stu-id="3233d-176">When to use this capability</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3233d-177">Если вы хотите настроить серверные компоненты MBAM 2,5 на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3233d-177">When you want to configure the MBAM 2.5 Server features on a remote computer.</span></span> <span data-ttu-id="3233d-178">Командлеты Windows PowerShell выполняются на одном компьютере, и вы настраиваете эти функции на другом удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3233d-178">The Windows PowerShell cmdlets are running on one computer, and you are configuring the features on a different, remote computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3233d-179">Что вам нужно сделать?</span><span class="sxs-lookup"><span data-stu-id="3233d-179">What you have to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3233d-180">Чтобы использовать Windows PowerShell для настройки функций сервера MBAM 2,5 на удаленном компьютере, необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3233d-180">To use Windows PowerShell to configure MBAM 2.5 Server features on a remote computer, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="3233d-181">Убедитесь, что на удаленном компьютере установлено программное обеспечение сервера MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="3233d-181">Ensure that the MBAM 2.5 Server software has been installed on the remote computer.</span></span></p></li>
<li><p><span data-ttu-id="3233d-182">Используйте протокол службы поддержки безопасности учетных данных (CredSSP) для открытия сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3233d-182">Use the Credential Security Support Provider (CredSSP) Protocol to open the Windows PowerShell session.</span></span></p></li>
<li><p><span data-ttu-id="3233d-183">Включите удаленное управление Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="3233d-183">Enable Windows Remote Management (WinRM).</span></span> <span data-ttu-id="3233d-184">Если вы не запустили службу WinRM и хотите правильно настроить ее, в <strong> командлете New-PSSession </strong> , описанный в этой таблице, появится сообщение об ошибке и инструкции по устранению этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="3233d-184">If you fail to enable WinRM and to configure it correctly, the <strong>New-PSSession</strong> cmdlet that is described in this table displays an error and describes how to fix the issue.</span></span> <span data-ttu-id="3233d-185">Дополнительные сведения об WinRM можно найти <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> в разделе Использование удаленного управления Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="3233d-185">For more information about WinRM, see <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)">Using Windows Remote Management</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3233d-186">Зачем это нужно сделать</span><span class="sxs-lookup"><span data-stu-id="3233d-186">Why you have to do it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3233d-187">Этот протокол позволяет командлетам Windows PowerShell подключаться к доменным службам Active Directory с помощью учетных данных администратора пользователя.</span><span class="sxs-lookup"><span data-stu-id="3233d-187">This protocol enables the Windows PowerShell cmdlets to connect to Active Directory Domain Services by using the user’s administrative credentials.</span></span> <span data-ttu-id="3233d-188">При запуске сеанса Windows PowerShell без этого протокола может возникнуть ошибка проверки.</span><span class="sxs-lookup"><span data-stu-id="3233d-188">You might get a validation error if you start the Windows PowerShell session without this protocol.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3233d-189">Запуск сеанса Windows PowerShell с протоколом CredSSP</span><span class="sxs-lookup"><span data-stu-id="3233d-189">How to start a Windows PowerShell session with the CredSSP protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3233d-190">Введите следующий код в командной строке Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="3233d-190">Type the following code at the Windows PowerShell prompt:</span></span></p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p><span data-ttu-id="3233d-191">Следующий код демонстрирует пример.</span><span class="sxs-lookup"><span data-stu-id="3233d-191">The following code shows an example.</span></span></p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a><span data-ttu-id="3233d-192">Обязательные учетные записи и соответствующие параметры командлета Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3233d-192">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>


<span data-ttu-id="3233d-193">В следующей таблице описаны учетные записи, необходимые для настройки функций сервера MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="3233d-193">The following table describes the accounts that are required to configure MBAM 2.5 Server features.</span></span> <span data-ttu-id="3233d-194">В нем также перечислены соответствующие командлеты и параметры Windows PowerShell, для которых необходимо указать учетную запись во время настройки.</span><span class="sxs-lookup"><span data-stu-id="3233d-194">It also lists the corresponding Windows PowerShell cmdlet and parameter for which you have to specify the account during configuration.</span></span>

<span data-ttu-id="3233d-195">Тип параметра командлета (пользователь или группа) описание Enable-MBAMDatabase</span><span class="sxs-lookup"><span data-stu-id="3233d-195">Cmdlet Parameter Type (User or Group) Description Enable-MBAMDatabase</span></span>

<span data-ttu-id="3233d-196">AccessAccount</span><span class="sxs-lookup"><span data-stu-id="3233d-196">AccessAccount</span></span>

<span data-ttu-id="3233d-197">Пользователь или группа</span><span class="sxs-lookup"><span data-stu-id="3233d-197">User or Group</span></span>

<span data-ttu-id="3233d-198">Укажите пользователя или группу домена, у которых есть разрешение на чтение и запись в эту базу данных, чтобы предоставить веб-приложениям доступ к данным и отчетам в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="3233d-198">Specify a domain user or group that has read/write permission to this database to give the web applications access to data and reports in this database.</span></span> <span data-ttu-id="3233d-199">Если значением является пользователь домена, параметр **WebServiceApplicationPoolCredential** , который используется при запуске командлета **Enable-MbamWebApplication** , должен использовать одну и ту же учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="3233d-199">If the value is a domain user, then the **WebServiceApplicationPoolCredential** parameter that is used when running the **Enable-MbamWebApplication** cmdlet must use the same user account.</span></span> <span data-ttu-id="3233d-200">Если значением является группа "Пользователи домена", учетная запись домена, используемая параметром **WebServiceApplicationPoolCredential** , должна быть членом этой группы.</span><span class="sxs-lookup"><span data-stu-id="3233d-200">If the value is a domain Users group, then the domain account that is used by the **WebServiceApplicationPoolCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="3233d-201">ReportAccount</span><span class="sxs-lookup"><span data-stu-id="3233d-201">ReportAccount</span></span>

<span data-ttu-id="3233d-202">Пользователь или группа</span><span class="sxs-lookup"><span data-stu-id="3233d-202">User or Group</span></span>

<span data-ttu-id="3233d-203">Укажите группу пользователей или пользователей домена с разрешением только на чтение в эту базу данных, чтобы предоставить MBAM отчеты для доступа к данным о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="3233d-203">Specify a domain user or Users group that has read-only permission to this database to provide the MBAM reports access to the compliance and audit data.</span></span> <span data-ttu-id="3233d-204">Если значением является пользователь домена, параметр **ComplianceAndAuditDBCredential** командлета **Enable-MbamReport** должен использовать одну и ту же учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="3233d-204">If the value is a domain user, then the **ComplianceAndAuditDBCredential** parameter of the **Enable-MbamReport** cmdlet must use the same user account.</span></span> <span data-ttu-id="3233d-205">Если значением является группа "Пользователи домена", учетная запись домена, используемая параметром **ComplianceAndAuditDBCredential** , должна быть членом этой группы.</span><span class="sxs-lookup"><span data-stu-id="3233d-205">If the value is a domain Users group, then the domain account that is used by the **ComplianceAndAuditDBCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="3233d-206">Enable-MbamReport</span><span class="sxs-lookup"><span data-stu-id="3233d-206">Enable-MbamReport</span></span>

<span data-ttu-id="3233d-207">ComplianceAndAuditDBCredential</span><span class="sxs-lookup"><span data-stu-id="3233d-207">ComplianceAndAuditDBCredential</span></span>

<span data-ttu-id="3233d-208">Пользователь</span><span class="sxs-lookup"><span data-stu-id="3233d-208">User</span></span>

<span data-ttu-id="3233d-209">Указывает учетные данные администратора, которые использует локальный экземпляр служб SSRS для подключения к базе данных соответствия MBAM и аудита.</span><span class="sxs-lookup"><span data-stu-id="3233d-209">Specifies the administrative credential that the local SSRS instance uses to connect to the MBAM Compliance and Audit Database.</span></span> <span data-ttu-id="3233d-210">Пользователь домена в учетных данных администратора должен совпадать с учетной записью пользователя, используемой для параметра **ReportAccount** , который используется при запуске командлета **Enable-MbamDatabase** .</span><span class="sxs-lookup"><span data-stu-id="3233d-210">The domain user in the administrative credential must be the same as the user account that is used for the **ReportAccount** parameter, which is used while running the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="3233d-211">Если в качестве параметра **ReportAccount** используется группа "Пользователи домена", эта учетная запись должна быть членом этой группы.</span><span class="sxs-lookup"><span data-stu-id="3233d-211">If a domain Users group was used with the **ReportAccount** parameter, this account should be a member of that group.</span></span>

<span data-ttu-id="3233d-212">**Важно!**  Учетная запись, указанная в учетных данных администратора, должна иметь ограниченные права для повышения безопасности.</span><span class="sxs-lookup"><span data-stu-id="3233d-212">**Important** The account specified in the administrative credentials should have limited user rights for improved security.</span></span> <span data-ttu-id="3233d-213">Кроме того, пароль учетной записи должен быть установлен в значение "не ограничен".</span><span class="sxs-lookup"><span data-stu-id="3233d-213">Also, the password of the account should be set to not expire.</span></span>

 

<span data-ttu-id="3233d-214">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="3233d-214">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="3233d-215">Группа</span><span class="sxs-lookup"><span data-stu-id="3233d-215">Group</span></span>

<span data-ttu-id="3233d-216">Указывает группу пользователей домена с разрешениями на чтение для отчетов.</span><span class="sxs-lookup"><span data-stu-id="3233d-216">Specifies the domain user group that has read permissions to the reports.</span></span> <span data-ttu-id="3233d-217">Указанная группа должна находиться в той же группе, которая используется для параметра **ReportsReadOnlyAccessGroup** в командлете **Enable-MbamWebApplication** .</span><span class="sxs-lookup"><span data-stu-id="3233d-217">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamWebApplication** cmdlet.</span></span>

<span data-ttu-id="3233d-218">Enable-MBAMWebApplication</span><span class="sxs-lookup"><span data-stu-id="3233d-218">Enable-MBAMWebApplication</span></span>

<span data-ttu-id="3233d-219">AdvancedHelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="3233d-219">AdvancedHelpdeskAccessGroup</span></span>

<span data-ttu-id="3233d-220">Группа</span><span class="sxs-lookup"><span data-stu-id="3233d-220">Group</span></span>

<span data-ttu-id="3233d-221">Указывает группу "Пользователи домена", которая имеет доступ ко всем областям веб-сайта администрирования и мониторинга, кроме области "отчеты".</span><span class="sxs-lookup"><span data-stu-id="3233d-221">Specifies the domain Users group that has access to all areas of the Administration and Monitoring Website except the Reports area.</span></span>

<span data-ttu-id="3233d-222">HelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="3233d-222">HelpdeskAccessGroup</span></span>

<span data-ttu-id="3233d-223">Группа</span><span class="sxs-lookup"><span data-stu-id="3233d-223">Group</span></span>

<span data-ttu-id="3233d-224">Указывает группу "Пользователи домена", которая имеет доступ к разделу " **Управление TPM** и **восстановлением диска** " на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3233d-224">Specifies the domain Users group that has access to the **Manage TPM** and **Drive Recovery** areas of the Administration and Monitoring Website.</span></span>

<span data-ttu-id="3233d-225">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="3233d-225">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="3233d-226">Группа</span><span class="sxs-lookup"><span data-stu-id="3233d-226">Group</span></span>

<span data-ttu-id="3233d-227">Указывает группу "Пользователи домена", которая имеет разрешение на чтение в области " **отчеты** " на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3233d-227">Specifies the domain Users group that has read permission to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="3233d-228">Указанная группа должна находиться в той же группе, которая используется для параметра **ReportsReadOnlyAccessGroup** в командлете **Enable-MbamReport** .</span><span class="sxs-lookup"><span data-stu-id="3233d-228">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamReport** cmdlet.</span></span>

<span data-ttu-id="3233d-229">WebServiceApplicationPoolCredential</span><span class="sxs-lookup"><span data-stu-id="3233d-229">WebServiceApplicationPoolCredential</span></span>

<span data-ttu-id="3233d-230">Пользователь</span><span class="sxs-lookup"><span data-stu-id="3233d-230">User</span></span>

<span data-ttu-id="3233d-231">Указывает пользователя домена, который будет использоваться пулом приложений для веб-приложений MBAM.</span><span class="sxs-lookup"><span data-stu-id="3233d-231">Specifies the domain user to be used by the application pool for the MBAM web applications.</span></span> <span data-ttu-id="3233d-232">Она должна быть той же учетной записью пользователя домена, которая указана в параметре **AccessAccount** командлета **Enable-MbamDatabase** .</span><span class="sxs-lookup"><span data-stu-id="3233d-232">It must be the same domain user account that is specified in the **AccessAccount** parameter of the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="3233d-233">Если при запуске командлета **Enable-MbamDatabase** в качестве параметра **AccessAccount** используется группа "Пользователи домена", пользователь домена, указанный здесь, должен быть членом этой группы.</span><span class="sxs-lookup"><span data-stu-id="3233d-233">If a domain Users group was used by the **AccessAccount** parameter when running the **Enable-MbamDatabase** cmdlet, the domain user that is specified here must be a member of that group.</span></span> <span data-ttu-id="3233d-234">Если вы не указали учетные данные администратора, используются учетные данные администратора, которые были указаны в предыдущем включенном веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="3233d-234">If you do not specify the administrative credentials, the administrative credentials that were specified by any previously enabled web application are used.</span></span> <span data-ttu-id="3233d-235">Все веб-приложения используют один и тот же идентификатор пула приложений.</span><span class="sxs-lookup"><span data-stu-id="3233d-235">All of the web applications use the same application pool identity.</span></span> <span data-ttu-id="3233d-236">Если задано несколько значений, используется последнее указанное значение.</span><span class="sxs-lookup"><span data-stu-id="3233d-236">If it is specified multiple times, the most recently specified value is used.</span></span>

<span data-ttu-id="3233d-237">**Важно!**  Для повышения безопасности укажите учетную запись, указанную в разделе Учетные данные администратора, для ограничения прав пользователя.</span><span class="sxs-lookup"><span data-stu-id="3233d-237">**Important** For improved security, set the account that is specified in the administrative credentials to limited user rights.</span></span> <span data-ttu-id="3233d-238">Кроме того, установите для пароля учетной записи значение бессрочной.</span><span class="sxs-lookup"><span data-stu-id="3233d-238">Also, set the password of the account to never expire.</span></span> <span data-ttu-id="3233d-239">Убедитесь в том, что встроенная учетная запись IIS \ _IUSRS или учетная запись, используемая для параметра **WebServiceApplicationPoolCredential** , была добавлена в "олицетворение" клиента после настройки локальной безопасности для **проверки подлинности** .</span><span class="sxs-lookup"><span data-stu-id="3233d-239">Ensure that either the built-in IIS\_IUSRS account or the account that is used for the **WebServiceApplicationPoolCredential** parameter has been added to the **Impersonate a client after authentication** local security setting.</span></span>

<span data-ttu-id="3233d-240">Чтобы просмотреть локальные параметры безопасности, откройте **Редактор локальной политики безопасности**, разверните узел **Локальные политики** , выберите узел **Назначение прав пользователя** , а затем дважды щелкните **олицетворение клиента после проверки подлинности** и войдите в систему в качестве параметров групповой политики **для пакетного задания** в области сведений.</span><span class="sxs-lookup"><span data-stu-id="3233d-240">To view the local security setting, open the **Local Security Policy editor**, expand the **Local Policies** node, select the **User Rights Assignment** node, and then double-click the **Impersonate a client after authentication** and **Log on as a batch job** Group Policy settings in the details pane.</span></span>

 

 




## <span data-ttu-id="3233d-241">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3233d-241">Related topics</span></span>


[<span data-ttu-id="3233d-242">Настройка компонентов сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="3233d-242">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="3233d-243">Проверка конфигурации компонентов MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="3233d-243">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)

[<span data-ttu-id="3233d-244">Использование Windows PowerShell для администрирования MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3233d-244">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)

 
## <span data-ttu-id="3233d-245">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="3233d-245">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3233d-246">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="3233d-246">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="3233d-247">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="3233d-247">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





