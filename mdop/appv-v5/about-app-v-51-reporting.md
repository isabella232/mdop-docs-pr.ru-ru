---
title: Сведения об отчетности в App-V 5.1
description: Сведения об отчетности в App-V 5.1
author: dansimp
ms.assetid: 385dca00-7178-4e35-8d86-c58867ebd65c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 827343d538238ca638b57a74ae5d2d74bc6c5968
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814952"
---
# <span data-ttu-id="4f8b0-103">Сведения об отчетности в App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4f8b0-103">About App-V 5.1 Reporting</span></span>

<span data-ttu-id="4f8b0-104">Microsoft Application Virtualization (App-V) 5,1 включает встроенную функцию для создания отчетов, которая позволяет собирать сведения о компьютерах, на которых работает клиент App-V 5,1, а также сведения об использовании виртуальных пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-104">Microsoft Application Virtualization (App-V) 5.1 includes a built-in reporting feature that helps you collect information about computers running the App-V 5.1 client as well as information about virtual application package usage.</span></span> <span data-ttu-id="4f8b0-105">Эти сведения можно использовать для создания отчетов из централизованной базы данных.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-105">You can use this information to generate reports from a centralized database.</span></span>

## <a href="" id="---------app-v-5-1-reporting-overview"></a> <span data-ttu-id="4f8b0-106">Общие сведения о создании отчетов для App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="4f8b0-106">App-V 5.1 Reporting Overview</span></span>

<span data-ttu-id="4f8b0-107">В списке ниже представлен рабочий процесс верхнего уровня для создания отчетов в приложении App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-107">The following list displays the end–to-end high-level workflow for reporting in App-V 5.1.</span></span>

1. <span data-ttu-id="4f8b0-108">У сервера отчетов App-V 5,1 есть следующие предварительные требования:</span><span class="sxs-lookup"><span data-stu-id="4f8b0-108">The App-V 5.1 Reporting server has the following prerequisites:</span></span>

    - <span data-ttu-id="4f8b0-109">Роль веб-сервера информационных служб Интернета (IIS)</span><span class="sxs-lookup"><span data-stu-id="4f8b0-109">Internet Information Service (IIS) web server role</span></span>

    - <span data-ttu-id="4f8b0-110">Роль проверки подлинности Windows (в разделе **IIS/безопасность**)</span><span class="sxs-lookup"><span data-stu-id="4f8b0-110">Windows Authentication role (under **IIS / Security**)</span></span>

    - <span data-ttu-id="4f8b0-111">SQL Server установлен и запущен с помощью служб SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="4f8b0-111">SQL Server installed and running with SQL Server Reporting Services (SSRS)</span></span>

    <span data-ttu-id="4f8b0-112">Чтобы убедиться в том, что службы SQL Server Reporting Services запущены, просмотрите `http://localhost/Reports` веб-браузер с правами администратора на сервере, на котором будут размещены отчеты App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-112">To confirm SQL Server Reporting Services is running, view `http://localhost/Reports` in a web browser as administrator on the server that will host App-V 5.1 Reporting.</span></span> <span data-ttu-id="4f8b0-113">Должна отобразиться домашняя страница служб SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-113">The SQL Server Reporting Services Home page should display.</span></span>

2. <span data-ttu-id="4f8b0-114">Установите сервер отчетов App-V 5,1 и связанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-114">Install the App-V 5.1 reporting server and associated database.</span></span> <span data-ttu-id="4f8b0-115">Дополнительные сведения об установке сервера отчетов можно найти в разделе [Установка сервера отчетов на отдельном компьютере и его подключение к базе данных](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md).</span><span class="sxs-lookup"><span data-stu-id="4f8b0-115">For more information about installing the reporting server see [How to install the Reporting Server on a Standalone Computer and Connect it to the Database](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md).</span></span> <span data-ttu-id="4f8b0-116">Настройте время, когда компьютер, на котором работает клиент App-V 5,1, должен отправлять данные на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-116">Configure the time when the computer running the App-V 5.1 client should send data to the reporting server.</span></span>

3. <span data-ttu-id="4f8b0-117">Если вы не используете электронную систему распространения программного обеспечения, например Configuration Manager для просмотра отчетов, вы можете определить отчеты в службе SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-117">If you are not using an electronic software distribution system such as Configuration Manager to view reports then you can define reports in SQL Server Reporting Service.</span></span> <span data-ttu-id="4f8b0-118">Загрузите предопределенные отчеты SSRS из [центра загрузки](https://go.microsoft.com/fwlink/?LinkId=397255).</span><span class="sxs-lookup"><span data-stu-id="4f8b0-118">Download predefined SSRS Reports from the [Download Center](https://go.microsoft.com/fwlink/?LinkId=397255).</span></span>

    > [!NOTE]
    > <span data-ttu-id="4f8b0-119">При использовании интеграции Configuration Manager с App-V 5,1 большинство отчетов создаются из Configuration Manager, а не из App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-119">If you are using the Configuration Manager integration with App-V 5.1, most reports are generated from Configuration Manager rather than from App-V 5.1.</span></span>

4. <span data-ttu-id="4f8b0-120">После импорта модуля PowerShell App-V 5,1 с помощью `Import-Module AppvClient` учетной записи администратора включите клиент App-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-120">After importing the App-V 5.1 PowerShell module using `Import-Module AppvClient` as administrator, enable the App-V 5.1 client.</span></span> <span data-ttu-id="4f8b0-121">Этот образец командлета PowerShell включает отчетность App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="4f8b0-121">This sample PowerShell cmdlet enables App-V 5.1 reporting:</span></span>

    ```powershell
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    <span data-ttu-id="4f8b0-122">Чтобы немедленно отправить данные отчета App-V 5,1, запустите `Send-AppvClientReport` клиент App-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-122">To immediately send App-V 5.1 report data, run `Send-AppvClientReport` on the App-V 5.1 client.</span></span>

    <span data-ttu-id="4f8b0-123">Дополнительные сведения об установке клиента App-V 5,1 с поддержкой отчетов можно найти в разделе [Параметры конфигурации клиента](about-client-configuration-settings51.md).</span><span class="sxs-lookup"><span data-stu-id="4f8b0-123">For more information about installing the App-V 5.1 client with reporting enabled see [About Client Configuration Settings](about-client-configuration-settings51.md).</span></span> <span data-ttu-id="4f8b0-124">Чтобы настроить отчеты App-V 5,1 с помощью Windows PowerShell, ознакомьтесь со [сведениями о том, как включить отчеты в клиенте App-v 5,1 с использованием PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="4f8b0-124">To administer App-V 5.1 Reporting with Windows PowerShell, see [How to Enable Reporting on the App-V 5.1 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md).</span></span>

5. <span data-ttu-id="4f8b0-125">После того как сервер отчетов получает данные из клиента App-V 5,1, он отправляет данные в базу данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-125">After the reporting server receives the data from the App-V 5.1 client it sends the data to the reporting database.</span></span> <span data-ttu-id="4f8b0-126">Когда база данных получает и обрабатывает данные клиента, успешный ответ отправляется на сервер отчетов, а затем на клиент App-V 5,1 отправляется уведомление.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-126">When the database receives and processes the client data, a successful reply is sent to the reporting server and then a notification is sent to the App-V 5.1 client.</span></span>

6. <span data-ttu-id="4f8b0-127">Когда клиент App-V 5,1 получает уведомление об успешном завершении, оно очищает кэш данных для экономии места.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-127">When the App-V 5.1 client receives the success notification, it empties the data cache to conserve space.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4f8b0-128">По умолчанию кэш очищается после того, как сервер подтвердит получение данных.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-128">By default the cache is cleared after the server confirms receipt of data.</span></span> <span data-ttu-id="4f8b0-129">Вы можете вручную настроить клиент для сохранения кэша данных.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-129">You can manually configure the client to save the data cache.</span></span>

<span data-ttu-id="4f8b0-130">Если клиентское устройство App-V 5,1 не получает уведомление об успешном завершении с сервера, оно сохраняет данные в кэше и пытается повторно отправить данные в течение следующего настроенного интервала.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-130">If the App-V 5.1 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval.</span></span> <span data-ttu-id="4f8b0-131">Клиенты продолжат собирать данные и добавлять их в кэш.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-131">Clients continue to collect data and add it to the cache.</span></span>

### <a href="" id="-------------app-v-5-1-reporting-server-frequently-asked-questions"></a> <span data-ttu-id="4f8b0-132">Ответы на часто задаваемые вопросы о приложении App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="4f8b0-132">App-V 5.1 reporting server frequently asked questions</span></span>

<span data-ttu-id="4f8b0-133">В следующей таблице приведены ответы на часто задаваемые вопросы об использовании отчетов App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-133">The following table displays answers to common questions about App-V 5.1 reporting</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4f8b0-134">Вопрос</span><span class="sxs-lookup"><span data-stu-id="4f8b0-134">Question</span></span></th>
<th align="left"><span data-ttu-id="4f8b0-135">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="4f8b0-135">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f8b0-136">Какова частота отправки данных отчетов в базу данных отчетов?</span><span class="sxs-lookup"><span data-stu-id="4f8b0-136">What is the frequency that reporting information is sent to the reporting database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f8b0-137">Частота зависит от того, как настроена задача создания отчетов на компьютере, на котором запущен клиент App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-137">The frequency depends on how the reporting task is configured on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="4f8b0-138">Вы должны настроить частоту и интервал для отправки данных отчета.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-138">You must configure the frequency / interval for sending the reporting data.</span></span> <span data-ttu-id="4f8b0-139">Служба отчетов App-V 5,1 по умолчанию не включена.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-139">App-V 5.1 Reporting is not enabled by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f8b0-140">Какие данные хранятся в базе данных сервера отчетов?</span><span class="sxs-lookup"><span data-stu-id="4f8b0-140">What information is stored in the reporting server database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f8b0-141">В следующем списке приведены сведения, хранящиеся в базе данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-141">The following list displays what is stored in the reporting database:</span></span></p>
<ul>
<li><p><span data-ttu-id="4f8b0-142">Операционная система, запущенная на компьютере с клиентским приложением App-V 5,1: имя узла, версия, пакет обновления, тип-клиент, сервер, архитектура процессора.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-142">The operating system running on the computer running the App-V 5.1 client: host name, version, service pack, type - client/server, processor architecture.</span></span></p></li>
<li><p><span data-ttu-id="4f8b0-143">Сведения о клиенте App-V 5,1: Version.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-143">App-V 5.1 Client information: version.</span></span></p></li>
<li><p><span data-ttu-id="4f8b0-144">Список опубликованных пакетов: GUID, версия GUID, имя.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-144">Published package list: GUID, version GUID, name.</span></span></p></li>
<li><p><span data-ttu-id="4f8b0-145">Сведения об использовании приложения: имя, версия, потоковый сервер, пользователь (domain\alias), версия пакета, состояние и время завершения работы.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-145">Application usage information: name, version, streaming server, user (domain\alias), package version GUID, launch status and time, shutdown time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f8b0-146">Каков средний объем данных, отправляемых на сервер отчетов?</span><span class="sxs-lookup"><span data-stu-id="4f8b0-146">What is the average volume of information that is sent to the reporting server?</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f8b0-147">Смотря как.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-147">It depends.</span></span> <span data-ttu-id="4f8b0-148">В списке ниже перечислены три набора данных, отправляемых на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-148">The following list displays the three sets of the data sent to the reporting server:</span></span></p>
<ol>
<li><p><span data-ttu-id="4f8b0-149">Сведения об операционной системе и клиенте App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-149">Operating system, and App-V 5.1 client information.</span></span> <span data-ttu-id="4f8b0-150">~ 150 байт, каждый раз, когда эти данные отправляются.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-150">~150 Bytes, every time this data is sent.</span></span></p></li>
<li><p><span data-ttu-id="4f8b0-151">Список опубликованных пакетов.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-151">Published package list.</span></span> <span data-ttu-id="4f8b0-152">~ 7 КБ для 30 пакетов.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-152">~7 KB for 30 packages.</span></span> <span data-ttu-id="4f8b0-153">Это сообщение отправляется только в том случае, если список пакетов обновляется с обновлением публикации, которое выполняется нечасто. При отсутствии изменений эти сведения не отправляются.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-153">This is sent only when the package list is updated with a publishing refresh, which is done infrequently; if there is no change, this information is not sent.</span></span></p></li>
<li><p><span data-ttu-id="4f8b0-154">Сведения об использовании виртуальных приложений — около 0,25 КБ на каждое событие.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-154">Virtual application usage information – about 0.25KB per event.</span></span> <span data-ttu-id="4f8b0-155">Открываются и закрываются как одно событие, которое выполняется, прежде чем отправлять информацию.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-155">Opening and closing count as one event if both occur before sending the information.</span></span> <span data-ttu-id="4f8b0-156">При отправке с помощью запланированной задачи данные отправляются на сервер только с момента последней успешной отправки.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-156">When sending using a scheduled task, only the data since the last successful upload is sent to the server.</span></span> <span data-ttu-id="4f8b0-157">При отправке вручную с помощью командлета PowerShell есть необязательный аргумент, который определяет, нужно ли повторно отправлять данные в следующий раз — этот аргумент является <strong> DeleteOnSuccess </strong> .</span><span class="sxs-lookup"><span data-stu-id="4f8b0-157">If sending manually through the PowerShell cmdlet, there is an optional argument that controls if the data needs to be re-sent next time around – that argument is <strong>DeleteOnSuccess</strong>.</span></span></p>
<p></p>
<p><span data-ttu-id="4f8b0-158">Например, если у вас есть двадцать приложений и вы закрыли данные отчетов, а отчеты будут отправляться ежедневно, то типичный ежедневный трафик должен составлять примерно 0.15 KB + 20 x 0,25 КБ или около 5KB/User.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-158">So for example, if twenty applications are opened and closed and reporting information is scheduled to be sent daily, the typical daily traffic should be about 0.15KB + 20 x 0.25KB, or about 5KB/user</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f8b0-159">Можно ли планировать отчетность?</span><span class="sxs-lookup"><span data-stu-id="4f8b0-159">Can reporting be scheduled?</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f8b0-160">Да.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-160">Yes.</span></span> <span data-ttu-id="4f8b0-161">Помимо отправки отчетов вручную с помощью командлетов PowerShell ( <strong> Send-AppvClientReport </strong> ), задачу можно запланировать таким образом, чтобы она выполнялась автоматически.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-161">Besides manually sending reporting using PowerShell Cmdlets (<strong>Send-AppvClientReport</strong>), the task can be scheduled so it will happen automatically.</span></span> <span data-ttu-id="4f8b0-162">Существует два способа планирования создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-162">There are two ways to schedule the reporting:</span></span></p>
<ol>
<li><p><span data-ttu-id="4f8b0-163">С помощью командлетов PowerShell — <strong> Set-AppvClientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="4f8b0-163">Using PowerShell cmdlets - <strong>Set-AppvClientConfiguration</strong>.</span></span> <span data-ttu-id="4f8b0-164">Пример</span><span class="sxs-lookup"><span data-stu-id="4f8b0-164">For example:</span></span></p>
<p><span data-ttu-id="4f8b0-165">Set-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span><span class="sxs-lookup"><span data-stu-id="4f8b0-165">Set-AppvClientConfiguration -ReportingEnabled 1 - ReportingServerURL <a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span></span></a></p>
<p></p>
<p><span data-ttu-id="4f8b0-166">Полный список параметров конфигурации клиента можно найти в разделе <a href="about-client-configuration-settings51.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings51.md)"> Параметры конфигурации клиента </a> и найти следующие элементы: <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay, ReportingInterval </strong> <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="4f8b0-166">For a complete list of client configuration settings see <a href="about-client-configuration-settings51.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings51.md)">About Client Configuration Settings</a> and look for the following entries: <strong>ReportingEnabled</strong>, <strong>ReportingServerURL</strong>, <strong>ReportingDataCacheLimit</strong>, <strong>ReportingDataBlockSize</strong>, <strong>ReportingStartTime</strong>, <strong>ReportingRandomDelay</strong>, <strong>ReportingInterval</strong>.</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="4f8b0-167">С помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-167">By using Group Policy.</span></span> <span data-ttu-id="4f8b0-168">При распределении с помощью контроллера домена эти параметры совпадают с указанными выше.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-168">If distributed using the domain controller, the settings are the same as previously listed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4f8b0-169">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-169">Note</span></span></strong><br/><p><span data-ttu-id="4f8b0-170">Параметры групповой политики переопределяют локальные параметры, настроенные с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-170">Group Policy settings override local settings configured using PowerShell.</span></span></p>
</div>
<div>
</div></li>
</ol></td>
</tr>
</tbody>
</table>

## <a href="" id="---------app-v-5-1-client-reporting"></a> <span data-ttu-id="4f8b0-171">Создание отчетов о клиентах для App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="4f8b0-171">App-V 5.1 Client Reporting</span></span>

<span data-ttu-id="4f8b0-172">Для использования отчетов App-V 5,1 необходимо установить и настроить клиент App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-172">To use App-V 5.1 reporting you must install and configure the App-V 5.1 client.</span></span> <span data-ttu-id="4f8b0-173">После установки клиента используйте командлет PowerShell **Set-AppVClientConfiguration** или **шаблон ADMX** для настройки отчетов.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-173">After the client has been installed, use the **Set-AppVClientConfiguration** PowerShell cmdlet or the **ADMX Template** to configure reporting.</span></span> <span data-ttu-id="4f8b0-174">Командлеты функций для отчетов можно получить, перейдя по следующей ссылке и предваряя их **отчетами**.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-174">The reporting feature cmdlets are available by using the following link and are prefaced by **Reporting**.</span></span> <span data-ttu-id="4f8b0-175">Полный список параметров конфигурации клиента см. в разделе [Параметры конфигурации клиента](about-client-configuration-settings51.md).</span><span class="sxs-lookup"><span data-stu-id="4f8b0-175">For a complete list of client configuration settings see [About Client Configuration Settings](about-client-configuration-settings51.md).</span></span> <span data-ttu-id="4f8b0-176">В следующем разделе приведены примеры конфигурации отчетов клиента App-V 5,1 с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-176">The following section provides examples of App-V 5.1 client reporting configuration using PowerShell.</span></span>

### <span data-ttu-id="4f8b0-177">Настройка отчетов клиента App-V с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f8b0-177">Configuring App-V Client reporting using PowerShell</span></span>

<span data-ttu-id="4f8b0-178">В приведенных ниже примерах показано, как параметры PowerShell могут настраивать функции отчетов в клиенте App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-178">The following examples show how PowerShell parameters can configure the reporting features of the App-V 5.1 client.</span></span>

> [!NOTE]
> <span data-ttu-id="4f8b0-179">Кроме того, с помощью параметров групповой политики в шаблоне App-V 5,1 ADMX можно настроить следующую задачу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-179">The following configuration task can also be configured using Group Policy settings in the App-V 5.1 ADMX template.</span></span> <span data-ttu-id="4f8b0-180">Дополнительные сведения об использовании шаблона ADMX приведены [в разделе изменение конфигурации клиента App-V 5,1 с помощью шаблона ADMX и групповой политики](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md).</span><span class="sxs-lookup"><span data-stu-id="4f8b0-180">For more information about using the ADMX template, see [How to Modify App-V 5.1 Client Configuration Using the ADMX Template and Group Policy](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md).</span></span>

<span data-ttu-id="4f8b0-181">**Чтобы включить создание отчетов и инициировать сбор данных на компьютере с клиентом App-V 5,1,** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-181">**To enable reporting and to initiate data collection on the computer running the App-V 5.1 client**:</span></span>

```powershell
Set-AppVClientConfiguration –ReportingEnabled 1
```

<span data-ttu-id="4f8b0-182">**Чтобы настроить клиент на автоматическую отправку данных на определенный сервер отчетов**, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-182">**To configure the client to automatically send data to a specific reporting server**:</span></span>

```powershell
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30 -ReportingInterval 1 -ReportingRandomDelay 30
```

<span data-ttu-id="4f8b0-183">В этом примере клиент настраивается на автоматическую отправку данных отчетов по URL-адресу сервера отчетов **http://MyReportingServer:MyPort/** .</span><span class="sxs-lookup"><span data-stu-id="4f8b0-183">This example configures the client to automatically send the reporting data to the reporting server URL **http://MyReportingServer:MyPort/**.</span></span> <span data-ttu-id="4f8b0-184">Кроме того, данные отчетов будут отправляться ежедневно между 8:00 и 8:30 PM в зависимости от случайной задержки, созданной для сеанса.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-184">Additionally, the reporting data will be sent daily between 8:00 and 8:30 PM, depending on the random delay generated for the session.</span></span>

<span data-ttu-id="4f8b0-185">**Чтобы ограничить размер кэша данных на клиентском компьютере,** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-185">**To limit the size of the data cache on the client**:</span></span>

```powershell
Set-AppvClientConfiguration –ReportingDataCacheLimit 100
```

<span data-ttu-id="4f8b0-186">Настройка максимального размера кэша отчетов на компьютере с клиентом App-V 5,1 и 100 МБ.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-186">Configures the maximum size of the reporting cache on the computer running the App-V 5.1 client to 100 MB.</span></span> <span data-ttu-id="4f8b0-187">Если достигнут предел кэша до отправки данных на сервер, Журнал переводится и данные при необходимости будут перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-187">If the cache limit is reached before the data is sent to the server, then the log rolls over and data will be overwritten as necessary.</span></span>

<span data-ttu-id="4f8b0-188">**Чтобы настроить размер блока данных, передаваемый по сети между клиентом и сервером**:</span><span class="sxs-lookup"><span data-stu-id="4f8b0-188">**To configure the data block size transmitted across the network between the client and the server**:</span></span>

```powershell
Set-AppvClientConfiguration –ReportingDataBlockSize 10240
```

<span data-ttu-id="4f8b0-189">Указывает максимальный блок данных, отправляемый клиентом в 10240 МБ.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-189">Specifies the maximum data block that the client sends to 10240 MB.</span></span>

### <span data-ttu-id="4f8b0-190">Типы собираемых данных</span><span class="sxs-lookup"><span data-stu-id="4f8b0-190">Types of data collected</span></span>

<span data-ttu-id="4f8b0-191">В следующей таблице представлены типы данных, которые можно собирать с помощью отчетов App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-191">The following table displays the types of information you can collect by using App-V 5.1 reporting.</span></span>

|<span data-ttu-id="4f8b0-192">Сведения о клиенте</span><span class="sxs-lookup"><span data-stu-id="4f8b0-192">Client Information</span></span>  |<span data-ttu-id="4f8b0-193">Сведения о пакете</span><span class="sxs-lookup"><span data-stu-id="4f8b0-193">Package Information</span></span>  |<span data-ttu-id="4f8b0-194">Использование приложения</span><span class="sxs-lookup"><span data-stu-id="4f8b0-194">Application Usage</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="4f8b0-195">Имя узла</span><span class="sxs-lookup"><span data-stu-id="4f8b0-195">Host Name</span></span> |<span data-ttu-id="4f8b0-196">Имя пакета</span><span class="sxs-lookup"><span data-stu-id="4f8b0-196">Package Name</span></span>|<span data-ttu-id="4f8b0-197">Временем начала и окончания</span><span class="sxs-lookup"><span data-stu-id="4f8b0-197">Start and End Times</span></span>|
|<span data-ttu-id="4f8b0-198">Версия клиента App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="4f8b0-198">App-V 5.1 Client Version</span></span> |<span data-ttu-id="4f8b0-199">Версия пакета</span><span class="sxs-lookup"><span data-stu-id="4f8b0-199">Package Version</span></span>|<span data-ttu-id="4f8b0-200">Состояние выполнения</span><span class="sxs-lookup"><span data-stu-id="4f8b0-200">Run Status</span></span>|
|<span data-ttu-id="4f8b0-201">Архитектура процессора</span><span class="sxs-lookup"><span data-stu-id="4f8b0-201">Processor Architecture</span></span> |<span data-ttu-id="4f8b0-202">Источник пакета</span><span class="sxs-lookup"><span data-stu-id="4f8b0-202">Package Source</span></span>|<span data-ttu-id="4f8b0-203">Состояние завершения работы</span><span class="sxs-lookup"><span data-stu-id="4f8b0-203">Shutdown State</span></span>|
|<span data-ttu-id="4f8b0-204">Версия операционной системы</span><span class="sxs-lookup"><span data-stu-id="4f8b0-204">Operating System Version</span></span>|<span data-ttu-id="4f8b0-205">Процент кэшированных данных</span><span class="sxs-lookup"><span data-stu-id="4f8b0-205">Percent Cached</span></span>|<span data-ttu-id="4f8b0-206">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="4f8b0-206">Application Name</span></span>|
|<span data-ttu-id="4f8b0-207">Уровень пакета обновления</span><span class="sxs-lookup"><span data-stu-id="4f8b0-207">Service Pack Level</span></span>| |<span data-ttu-id="4f8b0-208">Версия приложения</span><span class="sxs-lookup"><span data-stu-id="4f8b0-208">Application Version</span></span>|
|<span data-ttu-id="4f8b0-209">Тип операционной системы</span><span class="sxs-lookup"><span data-stu-id="4f8b0-209">Operating System Type</span></span>| |<span data-ttu-id="4f8b0-210">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="4f8b0-210">Username</span></span>|
| | |<span data-ttu-id="4f8b0-211">Группа "соединение"</span><span class="sxs-lookup"><span data-stu-id="4f8b0-211">Connection Group</span></span>|

<span data-ttu-id="4f8b0-212">Клиент собирает и сохраняет эти данные в формате **XML** .</span><span class="sxs-lookup"><span data-stu-id="4f8b0-212">The client collects and saves this data in an **.xml** format.</span></span> <span data-ttu-id="4f8b0-213">Кэш данных скрыт по умолчанию и требует наличия прав администратора для открытия XML-файла.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-213">The data cache is hidden by default and requires administrator rights to open the XML file.</span></span>

### <span data-ttu-id="4f8b0-214">Отправка данных на сервер</span><span class="sxs-lookup"><span data-stu-id="4f8b0-214">Sending data to the server</span></span>

<span data-ttu-id="4f8b0-215">Вы можете настроить компьютер, на котором запущен клиент App-V 5,1, для автоматической отправки данных на указанный сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-215">You can configure the computer that is running the App-V 5.1 client to automatically send data to the specified reporting server.</span></span> <span data-ttu-id="4f8b0-216">Чтобы указать сервер, используйте командлет **Set-AppvClientConfiguration** со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="4f8b0-216">To specify the server use the **Set-AppvClientConfiguration** cmdlet with the following settings:</span></span>

- <span data-ttu-id="4f8b0-217">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="4f8b0-217">ReportingEnabled</span></span>
- <span data-ttu-id="4f8b0-218">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="4f8b0-218">ReportingServerURL</span></span>
- <span data-ttu-id="4f8b0-219">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="4f8b0-219">ReportingStartTime</span></span>
- <span data-ttu-id="4f8b0-220">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="4f8b0-220">ReportingInterval</span></span>
- <span data-ttu-id="4f8b0-221">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="4f8b0-221">ReportingRandomDelay</span></span>

<span data-ttu-id="4f8b0-222">После настройки предыдущих параметров необходимо создать запланированную задачу.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-222">After you configure the previous settings, you must create a scheduled task.</span></span> <span data-ttu-id="4f8b0-223">Запланированная задача будет обращаться к серверу, указанному в параметре **ReportingServerURL** , и начнет передачу.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-223">The scheduled task will contact the server specified by the **ReportingServerURL** setting and will initiate the transfer.</span></span> <span data-ttu-id="4f8b0-224">Если вы хотите отправить данные вручную за пределами запланированного времени, используйте следующий командлет PowerShell:</span><span class="sxs-lookup"><span data-stu-id="4f8b0-224">If you want to manually send data outside of the scheduled times, use the following PowerShell cmdlet:</span></span>

```powershell
Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess
```

<span data-ttu-id="4f8b0-225">Если сервер отчетов уже настроен, параметр **– URL** можно опустить.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-225">If the reporting server has been previously configured, then the **–URL** parameter can be omitted.</span></span> <span data-ttu-id="4f8b0-226">Кроме того, если данные должны отправляться в альтернативное расположение, укажите другой URL-адрес для переопределения настроенного **ReportingServerURL** для этого набора данных.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-226">Alternatively, if the data should be sent to an alternate location, specify a different URL to override the configured **ReportingServerURL** for this data collection.</span></span>

<span data-ttu-id="4f8b0-227">Параметр **-DeleteOnSuccess** указывает на то, что при успешном передаче кэш данных очищается.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-227">The **-DeleteOnSuccess** parameter indicates that if the transfer is successful, then the data cache is cleared.</span></span> <span data-ttu-id="4f8b0-228">Если этот элемент не указан, кэш не будет очищен.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-228">If this is not specified, then the cache will not be cleared.</span></span>

### <span data-ttu-id="4f8b0-229">Сбор данных вручную</span><span class="sxs-lookup"><span data-stu-id="4f8b0-229">Manual Data Collection</span></span>

<span data-ttu-id="4f8b0-230">Вы также можете использовать командлет **Send-AppVClientReport** , чтобы вручную собирать данные.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-230">You can also use the **Send-AppVClientReport** cmdlet to manually collect data.</span></span> <span data-ttu-id="4f8b0-231">Это решение полезно с существующим сервером отчетов или без него.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-231">This solution is helpful with or without an existing reporting server.</span></span> <span data-ttu-id="4f8b0-232">В следующем списке приведены сведения о сборе данных с сервера отчетов или без него.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-232">The following list displays information about collecting data with or without a reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4f8b0-233">С сервером отчетов</span><span class="sxs-lookup"><span data-stu-id="4f8b0-233">With a Reporting Server</span></span></th>
<th align="left"><span data-ttu-id="4f8b0-234">Без сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="4f8b0-234">Without a Reporting Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f8b0-235">Если у вас уже есть сервер отчетов App-V 5,1, создайте настраиваемое запланированное задание или сценарий.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-235">If you have an existing App-V 5.1 reporting Server, create a customized scheduled task or script.</span></span> <span data-ttu-id="4f8b0-236">Указывает, что клиент отправляет данные в указанное расположение с нужной частотой.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-236">Specify that the client send the data to the specified location with the desired frequency.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f8b0-237">Если у вас нет существующего сервера отчетов App-V 5,1, используйте <strong> параметр – URL-адрес </strong> для отправки данных в указанный общий доступ.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-237">If you do not have an existing App-V 5.1 reporting Server, use the <strong>–URL</strong> parameter to send the data to a specified share.</span></span> <span data-ttu-id="4f8b0-238">Пример</span><span class="sxs-lookup"><span data-stu-id="4f8b0-238">For example:</span></span></p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p><span data-ttu-id="4f8b0-239">В предыдущем примере данные отчетов отправляются в <strong> Расположение \MyShare\MyData/strong, которое &lt; &gt; определяется <strong> </strong> параметром-URL.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-239">The previous example will send the reporting data to <strong>\MyShare\MyData&lt;/strong&gt; location indicated by the <strong>-URL</strong> parameter.</span></span> <span data-ttu-id="4f8b0-240">После отправки данных кэш очищается.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-240">After the data has been sent, the cache is cleared.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4f8b0-241">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-241">Note</span></span></strong><br/><p><span data-ttu-id="4f8b0-242">Если задано расположение, отличное от сервера отчетов, данные отправляются в <strong> формате XML без </strong> дополнительной обработки.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-242">If a location other than the Reporting Server is specified, the data is sent using <strong>.xml</strong> format with no additional processing.</span></span></p>
</div>
<div>
</div></td>
</tr>
</tbody>
</table>

### <span data-ttu-id="4f8b0-243">Создание отчетов</span><span class="sxs-lookup"><span data-stu-id="4f8b0-243">Creating Reports</span></span>

<span data-ttu-id="4f8b0-244">Для получения сведений о отчете и создания отчетов с помощью App-V 5,1 необходимо использовать один из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-244">To retrieve report information and create reports using App-V 5.1 you must use one of the following methods:</span></span>

- <span data-ttu-id="4f8b0-245">**Службы Microsoft SQL Server Reporting Services (SSRS)** — Microsoft SQL Server Reporting Services доступны в Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-245">**Microsoft SQL Server Reporting Services (SSRS)** - Microsoft SQL Server Reporting Services is available with Microsoft SQL Server.</span></span> <span data-ttu-id="4f8b0-246">Служба SSRS не устанавливается при установке сервера отчетов App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-246">SSRS is not installed when you install the App-V 5.1 reporting server.</span></span> <span data-ttu-id="4f8b0-247">Он должен быть развернут отдельно для создания связанных отчетов.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-247">It must be deployed separately to generate the associated reports.</span></span>

    <span data-ttu-id="4f8b0-248">Для получения дополнительных сведений об использовании [служб Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596)воспользуйтесь следующей ссылкой.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-248">Use the following link for more information about using [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).</span></span>

- <span data-ttu-id="4f8b0-249">**Написание сценариев** — вы можете создавать отчеты, используя сценарии непосредственно для базы данных отчетов App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-249">**Scripting** – You can generate reports by scripting directly against the App-V 5.1 reporting database.</span></span> <span data-ttu-id="4f8b0-250">Пример</span><span class="sxs-lookup"><span data-stu-id="4f8b0-250">For example:</span></span>

    **<span data-ttu-id="4f8b0-251">Хранимая процедура:</span><span class="sxs-lookup"><span data-stu-id="4f8b0-251">Stored Procedure:</span></span>**

    <span data-ttu-id="4f8b0-252">для **spProcessClientReport** запланировано выполнение в полночь или 12:00 AM.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-252">**spProcessClientReport** is scheduled to run at midnight or 12:00 AM.</span></span>

    <span data-ttu-id="4f8b0-253">Для выполнения запланированной хранимой процедуры Microsoft SQL Server необходимо, чтобы был запущен агент Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-253">To run the Microsoft SQL Server Scheduled Stored procedure, the Microsoft SQL Server Agent must be running.</span></span> <span data-ttu-id="4f8b0-254">Убедитесь, что для агента Microsoft SQL Server задано значение " **Автозагрузка**".</span><span class="sxs-lookup"><span data-stu-id="4f8b0-254">You should ensure that the Microsoft SQL Server Agent is set to **AutoStart**.</span></span> <span data-ttu-id="4f8b0-255">Дополнительные сведения см. в разделе [автозапуска агента SQL Server (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span><span class="sxs-lookup"><span data-stu-id="4f8b0-255">For more information see [Autostart SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span></span>

    <span data-ttu-id="4f8b0-256">Хранимая процедура также создается при использовании скриптов базы данных App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-256">The stored procedure is also created when using the App-V 5.1 database scripts.</span></span>

<span data-ttu-id="4f8b0-257">Кроме того, необходимо убедиться в том, что **Максимальное количество одновременных подключений** веб-службы сервера отчетов установлено равным значению, которое может управлять сервер без воздействия на доступность.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-257">You should also ensure that the reporting server web service's **Maximum Concurrent Connections** is set to a value that the server will be able to manage without impacting availability.</span></span> <span data-ttu-id="4f8b0-258">Рекомендуемое количество **одновременных подключений** для **веб-службы отчетов** — **10 000**.</span><span class="sxs-lookup"><span data-stu-id="4f8b0-258">The recommended number of **Maximum Concurrent Connections** for the **Reporting Web Service** is **10,000**.</span></span>

## <span data-ttu-id="4f8b0-259">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4f8b0-259">Related topics</span></span>

[<span data-ttu-id="4f8b0-260">Развертывание сервера App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4f8b0-260">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

[<span data-ttu-id="4f8b0-261">Установка сервера отчетности на отдельном компьютере и подключение его к базе данных</span><span class="sxs-lookup"><span data-stu-id="4f8b0-261">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)
