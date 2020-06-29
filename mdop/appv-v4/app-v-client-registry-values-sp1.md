---
title: Значения реестра клиента App-V
description: Значения реестра клиента App-V
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819809"
---
# <span data-ttu-id="f4657-103">Значения реестра клиента App-V</span><span class="sxs-lookup"><span data-stu-id="f4657-103">App-V Client Registry Values</span></span>


<span data-ttu-id="f4657-104">Клиент Microsoft Application Virtualization (App-V) хранит свою конфигурацию в реестре.</span><span class="sxs-lookup"><span data-stu-id="f4657-104">The Microsoft Application Virtualization (App-V) client stores its configuration in the registry.</span></span> <span data-ttu-id="f4657-105">Вы можете собрать полезные сведения о клиенте, если вы понимаете формат данных в реестре.</span><span class="sxs-lookup"><span data-stu-id="f4657-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="f4657-106">Вы также можете настроить множество клиентских действий, изменяя записи в реестре.</span><span class="sxs-lookup"><span data-stu-id="f4657-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="f4657-107">В этом разделе перечислены все разделы реестра клиента Application Virtualization (App-V) и способы их использования.</span><span class="sxs-lookup"><span data-stu-id="f4657-107">This topic lists all the Application Virtualization (App-V) client registry keys and explains their uses.</span></span>

**<span data-ttu-id="f4657-108">Важно.</span><span class="sxs-lookup"><span data-stu-id="f4657-108">Important</span></span>**  
<span data-ttu-id="f4657-109">На компьютере под управлением 64-разрядной операционной системы разделы и значения, описанные в следующих разделах, будут находиться в разделе HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span><span class="sxs-lookup"><span data-stu-id="f4657-109">On a computer running a 64-bit operating system, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>



## <span data-ttu-id="f4657-110">Конфигурационный ключ</span><span class="sxs-lookup"><span data-stu-id="f4657-110">Configuration Key</span></span>


<span data-ttu-id="f4657-111">В таблице ниже приведены сведения о значениях реестра, связанных с клавишей HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span><span class="sxs-lookup"><span data-stu-id="f4657-111">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4657-112">Имя</span><span class="sxs-lookup"><span data-stu-id="f4657-112">Name</span></span></th>
<th align="left"><span data-ttu-id="f4657-113">Тип</span><span class="sxs-lookup"><span data-stu-id="f4657-113">Type</span></span></th>
<th align="left"><span data-ttu-id="f4657-114">Данные (примеры)</span><span class="sxs-lookup"><span data-stu-id="f4657-114">Data (Examples)</span></span></th>
<th align="left"><span data-ttu-id="f4657-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f4657-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-116">ProductName</span><span class="sxs-lookup"><span data-stu-id="f4657-116">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-117">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-117">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-118">Классическое приложение Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f4657-118">Microsoft Application Virtualization Desktop Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-119">Не изменяйте.</span><span class="sxs-lookup"><span data-stu-id="f4657-119">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-120">Версия</span><span class="sxs-lookup"><span data-stu-id="f4657-120">Version</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-121">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-121">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-122">4.5.0.xxx</span><span class="sxs-lookup"><span data-stu-id="f4657-122">4.5.0.xxx</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-123">Не изменяйте.</span><span class="sxs-lookup"><span data-stu-id="f4657-123">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-124">Драйверы</span><span class="sxs-lookup"><span data-stu-id="f4657-124">Drivers</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-125">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-125">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-126">Sftfs.sys</span><span class="sxs-lookup"><span data-stu-id="f4657-126">Sftfs.sys</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-127">Если задано значение этого параметра, оно содержит имя драйвера, вызвавшего неустранимую ошибку при последнем запуске ядра.</span><span class="sxs-lookup"><span data-stu-id="f4657-127">If this key value is present, it contains the name of the driver that caused a stop error the last time the core was starting.</span></span> <span data-ttu-id="f4657-128">После устранения ошибки Stop необходимо удалить это значение ключа, чтобы sftlist можно было запустить.</span><span class="sxs-lookup"><span data-stu-id="f4657-128">After you have fixed the stop error, you must delete this key value so that sftlist can start.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-129">InstallPath</span><span class="sxs-lookup"><span data-stu-id="f4657-129">InstallPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-130">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-130">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-131">По умолчанию = C:\Program Files\Microsoft Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="f4657-131">Default=C:\Program Files\Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-132">Расположение, в котором установлен клиент.</span><span class="sxs-lookup"><span data-stu-id="f4657-132">The location where the client is installed.</span></span> <span data-ttu-id="f4657-133">Не изменяйте.</span><span class="sxs-lookup"><span data-stu-id="f4657-133">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-134">LogFileName</span><span class="sxs-lookup"><span data-stu-id="f4657-134">LogFileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-135">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-135">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-136">CSIDL_COMMON_APPDATA по умолчанию Client\sftlog.txt виртуализация \Microsoft\Application</span><span class="sxs-lookup"><span data-stu-id="f4657-136">Default=CSIDL_COMMON_APPDATA\Microsoft\Application Virtualization Client\sftlog.txt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-137">Путь и имя файла журнала клиента.</span><span class="sxs-lookup"><span data-stu-id="f4657-137">The path and name for the client log file.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f4657-138">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f4657-138">Note</span></span></strong><br/><p><span data-ttu-id="f4657-139">Если вы используете более раннюю версию приложения, чем App-V 4,6, SP1 и хотите изменить имя или расположение файла журнала, необходимо перезапустить службу sftlist, чтобы изменения вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="f4657-139">If you are running an earlier version than App-V 4.6, SP1 and you modify the log file name or location, you must restart the sftlist service for the change to take effect.</span></span></p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-140">LogMinSeverity</span><span class="sxs-lookup"><span data-stu-id="f4657-140">LogMinSeverity</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-141">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-141">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-142">По умолчанию = 4, информационные</span><span class="sxs-lookup"><span data-stu-id="f4657-142">Default=4, Informational</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-143">Определяет, какие сообщения записываются в журнал.</span><span class="sxs-lookup"><span data-stu-id="f4657-143">Controls which messages are written to the log.</span></span> <span data-ttu-id="f4657-144">Это значение указывает на порог, который заносится в журнал — все, что меньше или равно указанному значению.</span><span class="sxs-lookup"><span data-stu-id="f4657-144">The value indicates a threshold of what is logged—everything less than or equal to that value is logged.</span></span> <span data-ttu-id="f4657-145">Например, значение 0x3 (предупреждение) указывает на то, что в журнал записываются предупреждения (0x3), ошибки (0x2) и критические ошибки (0x1).</span><span class="sxs-lookup"><span data-stu-id="f4657-145">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="f4657-146">Диапазон значений: 0x0 = None, 0x1 = Critical, 0x2 = ошибка, 0x3 = предупреждение, 0x4 = Information (по умолчанию), 0x5 = подробный.</span><span class="sxs-lookup"><span data-stu-id="f4657-146">Value Range: 0x0 = None, 0x1 = Critical, 0x2 = Error, 0x3 = Warning, 0x4 = Information (Default), 0x5 = Verbose.</span></span></p>
<p><span data-ttu-id="f4657-147">Уровень журнала можно настроить с помощью клиентской консоли Application Virtualization (App-V) и из командной строки.</span><span class="sxs-lookup"><span data-stu-id="f4657-147">The log level is configurable from the Application Virtualization (App-V) client console and from the command prompt.</span></span> <span data-ttu-id="f4657-148">В командной строке команда sftlist.exe/verboselog увеличит уровень ведения журнала на подробный.</span><span class="sxs-lookup"><span data-stu-id="f4657-148">At a command prompt, the command sftlist.exe /verboselog will increase the log level to verbose.</span></span> <span data-ttu-id="f4657-149">Дополнительные сведения о командной строке см.</span><span class="sxs-lookup"><span data-stu-id="f4657-149">For more information on command-line details see</span></span></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p><span data-ttu-id="f4657-150">.</span><span class="sxs-lookup"><span data-stu-id="f4657-150">.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-151">LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="f4657-151">LogRolloverCount</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-152">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-152">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-153">По умолчанию = 4</span><span class="sxs-lookup"><span data-stu-id="f4657-153">Default=4</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-154">Определяет количество резервных копий файла журнала, которые сохраняются при сбросе.</span><span class="sxs-lookup"><span data-stu-id="f4657-154">Defines the number of backup copies of the log file that are kept when it is reset.</span></span> <span data-ttu-id="f4657-155">Допустимый диапазон: от 0 до 9999.</span><span class="sxs-lookup"><span data-stu-id="f4657-155">The valid range is 0–9999.</span></span> <span data-ttu-id="f4657-156">Значение по умолчанию — 4.</span><span class="sxs-lookup"><span data-stu-id="f4657-156">The default is 4.</span></span> <span data-ttu-id="f4657-157">Нулевое значение означает, что копии не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="f4657-157">A value of 0 means no copies will be kept.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-158">LogMaxSize</span><span class="sxs-lookup"><span data-stu-id="f4657-158">LogMaxSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-160">По умолчанию = 256</span><span class="sxs-lookup"><span data-stu-id="f4657-160">Default=256</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-161">Максимальный размер (в мегабайтах), в течение которого файл журнала может расти до сброса.</span><span class="sxs-lookup"><span data-stu-id="f4657-161">Defines the maximum size in megabytes (MB) that the log file can grow before being reset.</span></span> <span data-ttu-id="f4657-162">Размер по умолчанию составляет 256 МБ.</span><span class="sxs-lookup"><span data-stu-id="f4657-162">The default size is 256 MB.</span></span> <span data-ttu-id="f4657-163">По достижении этого размера, сброс журнала будет принудительно выполнен при следующей попытке записи.</span><span class="sxs-lookup"><span data-stu-id="f4657-163">When this size is reached, a log reset will be forced on the next write attempt.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-164">SystemEventLogLevel</span><span class="sxs-lookup"><span data-stu-id="f4657-164">SystemEventLogLevel</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-165">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-165">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-166">По умолчанию = 0x4 (App-V 4,5)</span><span class="sxs-lookup"><span data-stu-id="f4657-166">Default=0x4 (App-V 4.5)</span></span></p>
<p><span data-ttu-id="f4657-167">По умолчанию = 0x3 (App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="f4657-167">Default=0x3 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-168">Уровень ведения журнала, на котором сообщения журнала записываются в журнал событий NT.</span><span class="sxs-lookup"><span data-stu-id="f4657-168">Indicates the logging level at which log messages are written to the NT event log.</span></span> <span data-ttu-id="f4657-169">Это значение указывает порог, который заносится в журнал, то есть все, что равно или меньше этого значения, заносится в журнал.</span><span class="sxs-lookup"><span data-stu-id="f4657-169">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="f4657-170">Например, значение 0x3 (предупреждение) указывает на то, что в журнал записываются предупреждения (0x3), ошибки (0x2) и критические ошибки (0x1).</span><span class="sxs-lookup"><span data-stu-id="f4657-170">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="f4657-171">Диапазон значений</span><span class="sxs-lookup"><span data-stu-id="f4657-171">Value Range</span></span></p>
<p><span data-ttu-id="f4657-172">0x0 = None (нет)</span><span class="sxs-lookup"><span data-stu-id="f4657-172">0x0 = None</span></span></p>
<p><span data-ttu-id="f4657-173">0x1 = критический</span><span class="sxs-lookup"><span data-stu-id="f4657-173">0x1 = Critical</span></span></p>
<p><span data-ttu-id="f4657-174">0x2 = ошибка</span><span class="sxs-lookup"><span data-stu-id="f4657-174">0x2 = Error</span></span></p>
<p><span data-ttu-id="f4657-175">0x3 = предупреждение</span><span class="sxs-lookup"><span data-stu-id="f4657-175">0x3 = Warning</span></span></p>
<p><span data-ttu-id="f4657-176">0x4 = Information (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4657-176">0x4 = Information (Default)</span></span></p>
<p><span data-ttu-id="f4657-177">0x5 = подробный</span><span class="sxs-lookup"><span data-stu-id="f4657-177">0x5 = Verbose</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-178">AllowIndependentFileStreaming</span><span class="sxs-lookup"><span data-stu-id="f4657-178">AllowIndependentFileStreaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-179">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-179">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-180">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-180">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-181">Указывает, будет ли включена потоковая передача из файла независимо от того, как был настроен клиент с помощью параметра APPLICATIONSOURCEROOT.</span><span class="sxs-lookup"><span data-stu-id="f4657-181">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the APPLICATIONSOURCEROOT parameter.</span></span> <span data-ttu-id="f4657-182">Если задано значение FALSE, транспорт не включит потоковую передачу из файлов даже в том случае, если в качестве параметра APPLICATIONSOURCEROOT в OSD есть путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="f4657-182">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the APPLICATIONSOURCEROOT parameter contains a file path.</span></span></p>
<p><span data-ttu-id="f4657-183">0x0 = False (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4657-183">0x0=False (default)</span></span></p>
<p><span data-ttu-id="f4657-184">0x1 = истина</span><span class="sxs-lookup"><span data-stu-id="f4657-184">0x1=True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-185">ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="f4657-185">ApplicationSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-186">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-186">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-187">rtsps://mainserver:322/prodapps</span><span class="sxs-lookup"><span data-stu-id="f4657-187">rtsps://mainserver:322/prodapps</span></span></p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p><span data-ttu-id="f4657-188">файл://\uncserver\share\prodapps</span><span class="sxs-lookup"><span data-stu-id="f4657-188">file://\uncserver\share\prodapps</span></span></p>
<p><span data-ttu-id="f4657-189">файл://\uncserver\share</span><span class="sxs-lookup"><span data-stu-id="f4657-189">file://\uncserver\share</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-190">Позволяет администратору или электронному каналу программного обеспечения (ESD) обеспечить выполнение загрузки приложения в соответствии со схемой управления топологией.</span><span class="sxs-lookup"><span data-stu-id="f4657-190">Enables an administrator or electronic software distribution (ESD) system to ensure application loading is performed according to the topology management scheme.</span></span> <span data-ttu-id="f4657-191">Используйте это значение ключа для переопределения кода OSD для элемента HREF (например, исходного расположения) для приложения.</span><span class="sxs-lookup"><span data-stu-id="f4657-191">Use this key value to override the OSD CODEBASE for the HREF element (for example, the source location) for an application.</span></span> <span data-ttu-id="f4657-192">Корневой источник приложения поддерживает URL-адреса и форматы путей в формате UNC.</span><span class="sxs-lookup"><span data-stu-id="f4657-192">Application Source Root supports URLs and Universal Naming Convention (UNC) path formats.</span></span></p>
<p><span data-ttu-id="f4657-193">Правильным форматом URL-пути является протокол://ServerName: [порт] [/path] [/], где порт и путь являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="f4657-193">The correct format for the URL path is protocol://servername:[port][/path][/], where port and path are optional.</span></span> <span data-ttu-id="f4657-194">Если порт не указан, используется порт по умолчанию для протокола.</span><span class="sxs-lookup"><span data-stu-id="f4657-194">If a port is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="f4657-195">Заменяется только часть Protocol://Server: Port URL-адреса OSD.</span><span class="sxs-lookup"><span data-stu-id="f4657-195">Only the protocol://server:port portion of the OSD URL is replaced.</span></span> </p>
<p><span data-ttu-id="f4657-196">Правильным форматом UNC-пути является \computername\sharefolder [Folder] [], где папка является необязательной.</span><span class="sxs-lookup"><span data-stu-id="f4657-196">The correct format for the UNC path is \computername\sharefolder[folder][], where folder is optional.</span></span> <span data-ttu-id="f4657-197">Именем компьютера может быть полное доменное имя (FQDN) или IP-адрес, а sharefolder может быть буквой диска.</span><span class="sxs-lookup"><span data-stu-id="f4657-197">The computer name can be a fully qualified domain name (FQDN) or an IP address, and sharefolder can be a drive letter.</span></span> <span data-ttu-id="f4657-198">Заменяется только часть \computername\sharefolder или буква диска в пути OSD.</span><span class="sxs-lookup"><span data-stu-id="f4657-198">Only the \computername\sharefolder or drive letter portion of the OSD path is replaced.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-199">OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="f4657-199">OSDSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-200">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-200">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-201">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="f4657-201">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="f4657-202">\computername\content</span><span class="sxs-lookup"><span data-stu-id="f4657-202">\computername\content</span></span></p>
<p><span data-ttu-id="f4657-203">C:\foldername</span><span class="sxs-lookup"><span data-stu-id="f4657-203">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="f4657-204">Позволяет администратору указать расположение источника для получения файла OSD для последовательного пакета приложения во время публикации.</span><span class="sxs-lookup"><span data-stu-id="f4657-204">Enables an administrator to specify a source location for OSD file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="f4657-205">Допустимые форматы для OSDSourceRoot включают пути UNC и URL-адреса (HTTP или HTTPS).</span><span class="sxs-lookup"><span data-stu-id="f4657-205">Acceptable formats for the OSDSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-206">IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="f4657-206">IconSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-207">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-207">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-208">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="f4657-208">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="f4657-209">\computername\content</span><span class="sxs-lookup"><span data-stu-id="f4657-209">\computername\content</span></span></p>
<p><span data-ttu-id="f4657-210">C:\foldername</span><span class="sxs-lookup"><span data-stu-id="f4657-210">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="f4657-211">Позволяет администратору указать исходное расположение для извлечения файла значка для последовательного пакета приложения во время публикации.</span><span class="sxs-lookup"><span data-stu-id="f4657-211">Enables an administrator to specify a source location for icon file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="f4657-212">Допустимые форматы для IconSourceRoot включают пути UNC и URL-адреса (HTTP или HTTPS).</span><span class="sxs-lookup"><span data-stu-id="f4657-212">Acceptable formats for the IconSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-213">AutoLoadTriggers</span><span class="sxs-lookup"><span data-stu-id="f4657-213">AutoLoadTriggers</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-214">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-214">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-215">По умолчанию = 5</span><span class="sxs-lookup"><span data-stu-id="f4657-215">Default=5</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-216">AutoLoad — это параметр конфигурации политики клиентской среды, который позволяет автоматически передавать дополнительный блок функций виртуализированному приложению клиенту в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="f4657-216">AutoLoad is a client runtime policy configuration parameter that enables the secondary feature block of a virtualized application to be streamed to the client automatically in the background.</span></span> <span data-ttu-id="f4657-217">Триггеры AutoLoad — это флаги, указывающие на события, инициирующие автоматическую загрузку приложений.</span><span class="sxs-lookup"><span data-stu-id="f4657-217">The AutoLoad triggers are flags to indicate events that initiate auto-loading of applications.</span></span> <span data-ttu-id="f4657-218">AutoLoad неявно использует фоновую потоковую передачу для обеспечения полной загрузки приложения в кэш.</span><span class="sxs-lookup"><span data-stu-id="f4657-218">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span> <span data-ttu-id="f4657-219">Основной блок функций будет загружаться, а остальные блоки функций будут загружены в фоновом режиме, чтобы активировать выполнение операций переднего плана, таких как взаимодействие пользователей с приложениями, и обеспечить оптимальную производительность.</span><span class="sxs-lookup"><span data-stu-id="f4657-219">The primary feature block will be loaded first, and the remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take place and provide optimal perceived performance.</span></span></p>
<p><span data-ttu-id="f4657-220">Значения битовой маски:</span><span class="sxs-lookup"><span data-stu-id="f4657-220">Bit mask values:</span></span></p>
<p><span data-ttu-id="f4657-221">(0) никогда: не заданы биты (значение равно 0), автоматическая загрузка не выполняется, так как не заданы триггеры.</span><span class="sxs-lookup"><span data-stu-id="f4657-221">(0) Never: No bits are set (value is 0), no auto loading will be performed, because there are no triggers set.</span></span></p>
<p><span data-ttu-id="f4657-222">(1) OnLaunch: Загрузка начинается, когда пользователь запускает приложение.</span><span class="sxs-lookup"><span data-stu-id="f4657-222">(1) OnLaunch: Loading starts when a user starts an application.</span></span></p>
<p><span data-ttu-id="f4657-223">(2) OnRefresh: Загрузка начинается при публикации приложения.</span><span class="sxs-lookup"><span data-stu-id="f4657-223">(2) OnRefresh: Loading starts when the application is published.</span></span> <span data-ttu-id="f4657-224">Это происходит при каждом добавлении или обновлении записи пакета (например, при обновлении публикации).</span><span class="sxs-lookup"><span data-stu-id="f4657-224">This occurs whenever the package record is added or updated—for example, when a publishing refresh occurs.</span></span></p>
<p><span data-ttu-id="f4657-225">(4) OnLogin: Загрузка начинается, когда пользователь входит в систему.</span><span class="sxs-lookup"><span data-stu-id="f4657-225">(4) OnLogin: Loading starts when a user logs in.</span></span></p>
<p><span data-ttu-id="f4657-226">(5) для запуска и OnLaunch: Default.</span><span class="sxs-lookup"><span data-stu-id="f4657-226">(5) OnLaunch and OnLogin: Default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-227">AutoLoadTarget</span><span class="sxs-lookup"><span data-stu-id="f4657-227">AutoLoadTarget</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-228">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-228">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-229">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="f4657-229">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-230">Указывает, что будет автоматически загружаться при возникновении любого определенного триггера AutoLoad.</span><span class="sxs-lookup"><span data-stu-id="f4657-230">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span> <span data-ttu-id="f4657-231">Значения битовой маски:</span><span class="sxs-lookup"><span data-stu-id="f4657-231">Bit mask values:</span></span></p>
<p><span data-ttu-id="f4657-232">(0) None: без автоматической загрузки, независимо от того, какие триггеры могут быть установлены.</span><span class="sxs-lookup"><span data-stu-id="f4657-232">(0) None: No auto-loading, regardless of what triggers may be set.</span></span></p>
<p><span data-ttu-id="f4657-233">(1) PreviouslyUsed (по умолчанию): Если включен какой-либо триггер AutoLoad, загрузите только те пакеты, в которых ранее использовалось хотя бы одно приложение в пакете, то есть запущены или предварительно кэшированы.</span><span class="sxs-lookup"><span data-stu-id="f4657-233">(1) PreviouslyUsed (default): If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used—that is, started or precached.</span></span></p>
<p><span data-ttu-id="f4657-234">(2) все: Если включен какой-либо триггер AutoLoad, все приложения в пакете (на пакет) или все пакеты (заданные для клиента) будут автоматически загружены независимо от того, были ли они запущены.</span><span class="sxs-lookup"><span data-stu-id="f4657-234">(2) All: If any AutoLoad trigger is enabled, all applications in the package (per package) or all packages (set for client) will be automatically loaded, whether or not they have ever been started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-235">RequireAuthorizationIfCached</span><span class="sxs-lookup"><span data-stu-id="f4657-235">RequireAuthorizationIfCached</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-236">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-236">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-237">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="f4657-237">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-238">Указывает, что авторизация всегда требуется, независимо от того, уже находится ли приложение в кэше.</span><span class="sxs-lookup"><span data-stu-id="f4657-238">Indicates that authorization is always required, whether or not an application is already in cache.</span></span> <span data-ttu-id="f4657-239">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="f4657-239">Possible values:</span></span></p>
<p><span data-ttu-id="f4657-240">0 = false: всегда пытайтесь подключиться к серверу.</span><span class="sxs-lookup"><span data-stu-id="f4657-240">0=False: Always try to connect to the server.</span></span> <span data-ttu-id="f4657-241">Если не удается установить соединение с сервером, клиент по-прежнему позволяет пользователю запустить приложение, которое ранее было загружено в кэш.</span><span class="sxs-lookup"><span data-stu-id="f4657-241">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p>
<p><span data-ttu-id="f4657-242">1 = истина (по умолчанию): приложение всегда должно быть авторизовано при запуске.</span><span class="sxs-lookup"><span data-stu-id="f4657-242">1=True (default): Application always must be authorized at startup.</span></span> <span data-ttu-id="f4657-243">Для потоковых приложений RTSP маркер авторизации пользователя отправляется на сервер для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f4657-243">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="f4657-244">Для приложений, использующих файлы, списки ACL для файлов определяют, может ли пользователь получить доступ к приложению.</span><span class="sxs-lookup"><span data-stu-id="f4657-244">For file-based applications, file ACLs control whether a user may access the application.</span></span></p>
<p><span data-ttu-id="f4657-245">Чтобы изменения вступили в силу, перезапустите службу sftlist.</span><span class="sxs-lookup"><span data-stu-id="f4657-245">Restart the sftlist service for the change to take effect.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-246">UserDataDirectory</span><span class="sxs-lookup"><span data-stu-id="f4657-246">UserDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-247">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-247">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-248">AppData</span><span class="sxs-lookup"><span data-stu-id="f4657-248">%APPDATA%</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-249">Расположение, в котором хранятся кэш значков и параметры пользователя.</span><span class="sxs-lookup"><span data-stu-id="f4657-249">Location where the icon cache and user settings are stored.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-250">GlobalDataDirectory</span><span class="sxs-lookup"><span data-stu-id="f4657-250">GlobalDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-251">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-251">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-252">C:\Users\Public\Documents</span><span class="sxs-lookup"><span data-stu-id="f4657-252">C:\Users\Public\Documents</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-253">Каталог, используемый для глобальных данных App-V, включая кэши для файлов OSD, файлов значков, сведений о сочетаниях клавиш и SystemGuard ресурсов, таких как ini-файлы.</span><span class="sxs-lookup"><span data-stu-id="f4657-253">Directory to use for global App-V data, including caches for OSD files, icon files, shortcut information, and SystemGuard resources such as .ini files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-254">AllowCrashes</span><span class="sxs-lookup"><span data-stu-id="f4657-254">AllowCrashes</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-255">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-255">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-256">0или1</span><span class="sxs-lookup"><span data-stu-id="f4657-256">0 or 1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-257">По умолчанию = 0: нулевое значение означает, что клиент пытается перехватить внутренние исключения программы, чтобы другие пользовательские приложения могли восстановить и продолжить работу, когда происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="f4657-257">Default=0: A value of 0 means that the client tries to catch internal program exceptions so that other user applications can recover and continue when a crash happens.</span></span> <span data-ttu-id="f4657-258">Значение, равное 1, означает, что клиент разрешает выполнение внутренних исключений программы, чтобы их можно было записать в отладчик.</span><span class="sxs-lookup"><span data-stu-id="f4657-258">A value of 1 means that the client allows the internal program exceptions to occur so that they can be captured in a debugger.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-259">CoreInternalTimeout</span><span class="sxs-lookup"><span data-stu-id="f4657-259">CoreInternalTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-260">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-260">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-261">60</span><span class="sxs-lookup"><span data-stu-id="f4657-261">60</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-262">Время ожидания (в секундах) внутренних запросов IPC между ядром и клиентским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="f4657-262">Time-out in seconds for internal IPC requests between core and front-end.</span></span> <span data-ttu-id="f4657-263">Не изменяйте.</span><span class="sxs-lookup"><span data-stu-id="f4657-263">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-264">DefaultSuiteCombineTime</span><span class="sxs-lookup"><span data-stu-id="f4657-264">DefaultSuiteCombineTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-265">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-265">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-266">5-10</span><span class="sxs-lookup"><span data-stu-id="f4657-266">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-267">Это значение используется, чтобы указать, как вскоре будет запущено, что программа может завершить работу и не будет создавать сообщения об ошибках при запуске другого приложения в том же наборе.</span><span class="sxs-lookup"><span data-stu-id="f4657-267">This value is used to indicate how soon after being started that a program can shut down and not generate any error messages when another application in the same suite is running.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-268">SerializedSuiteLaunchTimeout</span><span class="sxs-lookup"><span data-stu-id="f4657-268">SerializedSuiteLaunchTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-269">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-269">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-270">По умолчанию = 60 000</span><span class="sxs-lookup"><span data-stu-id="f4657-270">Default=60000</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-271">Определяет, сколько времени в миллисекундах клиент будет ждать, так как при попытке сериализации программы запускается в одном и том же наборе.</span><span class="sxs-lookup"><span data-stu-id="f4657-271">Defines how long in milliseconds the client will wait as it tries to serialize program starts in the same suite.</span></span> <span data-ttu-id="f4657-272">Если время ожидания клиента истекает, программа начнет выполняться, но не будет сериализована.</span><span class="sxs-lookup"><span data-stu-id="f4657-272">If the client times out, the program start will continue but it will not be serialized.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-273">ScriptTimeout</span><span class="sxs-lookup"><span data-stu-id="f4657-273">ScriptTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-274">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-275">300</span><span class="sxs-lookup"><span data-stu-id="f4657-275">300</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-276">Время ожидания по умолчанию в секундах для сценариев в OSD-файле, если WAIT = TRUE.</span><span class="sxs-lookup"><span data-stu-id="f4657-276">Default time-out in seconds for scripts in OSD file if WAIT=TRUE.</span></span> <span data-ttu-id="f4657-277">Вы можете задать время ожидания для каждого сценария с задержкой, а не ждать.</span><span class="sxs-lookup"><span data-stu-id="f4657-277">You can specify per-script time-outs with TIMEOUT instead of WAIT.</span></span> <span data-ttu-id="f4657-278">Нулевое значение означает бессрочное ожидание, а 0xFFFFFFFF — ожидание.</span><span class="sxs-lookup"><span data-stu-id="f4657-278">A value of 0 means no wait, and 0xFFFFFFFF means wait forever.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-279">LaunchRecordLogPath</span><span class="sxs-lookup"><span data-stu-id="f4657-279">LaunchRecordLogPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-280">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-280">String</span></span> </p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f4657-281">Если в разделе HKLM или HKCU этот параметр имеет допустимый путь к файлу журнала, SFTTray будет записываться в этот журнал при запуске, завершении работы, запуске и переходе в режим отключения и выхода из него.</span><span class="sxs-lookup"><span data-stu-id="f4657-281">If, under either HKLM or HKCU, this value contains a valid path to a log file, SFTTray will write to this log when programs start, shut down, fail to launch, and enter or exit disconnected mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-282">LaunchRecordMask</span><span class="sxs-lookup"><span data-stu-id="f4657-282">LaunchRecordMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-283">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-283">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-284">0x1A (26) ошибки при запуске журнала и активность входа и выхода в отключенном режиме.</span><span class="sxs-lookup"><span data-stu-id="f4657-284">0x1A (26) log launch errors and disconnected mode entry and exit activity.</span></span></p>
<p><span data-ttu-id="f4657-285">0x1F (31) регистрирует все.</span><span class="sxs-lookup"><span data-stu-id="f4657-285">0x1F (31) logs everything.</span></span></p>
<p><span data-ttu-id="f4657-286">0x0 (0) не записывает ничего.</span><span class="sxs-lookup"><span data-stu-id="f4657-286">0x0 (0) logs nothing.</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-287">Указывает, какие из пяти событий регистрируются в журнале (значения битовых масок).</span><span class="sxs-lookup"><span data-stu-id="f4657-287">Specifies which of the five events are logged (bitmask values):</span></span></p>
<p><span data-ttu-id="f4657-288">1 для запуска программы</span><span class="sxs-lookup"><span data-stu-id="f4657-288">1 for program starts</span></span></p>
<p><span data-ttu-id="f4657-289">2 для ошибок при запуске</span><span class="sxs-lookup"><span data-stu-id="f4657-289">2 for launch failure errors</span></span></p>
<p><span data-ttu-id="f4657-290">4 — для завершения работы</span><span class="sxs-lookup"><span data-stu-id="f4657-290">4 for shutdowns</span></span></p>
<p><span data-ttu-id="f4657-291">8 Переход в автономный режим</span><span class="sxs-lookup"><span data-stu-id="f4657-291">8 for entering disconnected mode</span></span></p>
<p><span data-ttu-id="f4657-292">16 для выхода из отключенного режима для повторного подключения к серверу</span><span class="sxs-lookup"><span data-stu-id="f4657-292">16 for exiting disconnected mode to reconnect to a server</span></span></p>
<p><span data-ttu-id="f4657-293">Чтобы включить соответствующие сообщения, добавьте любое сочетание этих номеров.</span><span class="sxs-lookup"><span data-stu-id="f4657-293">Add any combination of those numbers to turn on the respective messages.</span></span> <span data-ttu-id="f4657-294">По умолчанию используется 0x1F, если в реестре нет.</span><span class="sxs-lookup"><span data-stu-id="f4657-294">Defaults to 0x1F if not in registry.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-295">LaunchRecordWriteTimeout</span><span class="sxs-lookup"><span data-stu-id="f4657-295">LaunchRecordWriteTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-296">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-296">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-297">По умолчанию = 3000</span><span class="sxs-lookup"><span data-stu-id="f4657-297">Default=3000</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-298">Указывает в миллисекундах, как долго область будет ждать при попытке записи в журнал записи запуска, если он используется другим процессом.</span><span class="sxs-lookup"><span data-stu-id="f4657-298">Specifies in milliseconds how long the tray will wait when trying to write to the launch record log if another process is using it.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-299">ImportSearchPath</span><span class="sxs-lookup"><span data-stu-id="f4657-299">ImportSearchPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-300">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-300">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-301">d:\files; C:\Documents and settings\user1\SFTs</span><span class="sxs-lookup"><span data-stu-id="f4657-301">d:\files;C:\documents and settings\user1\SFTs</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-302">Список с разделителями-запятыми (до пяти каталогов) для поиска переносимых SFT-файлов перед тем, как пользователю будет предложено выбрать каталог.</span><span class="sxs-lookup"><span data-stu-id="f4657-302">A semicolon delimited list of up to five directories to search for portable SFT files before prompting the user to select a directory.</span></span> <span data-ttu-id="f4657-303">Конечная обратная косая черта в пути не является обязательной.</span><span class="sxs-lookup"><span data-stu-id="f4657-303">Trailing backslash in paths is optional.</span></span> <span data-ttu-id="f4657-304">Это значение по умолчанию отсутствует и должно быть задано вручную.</span><span class="sxs-lookup"><span data-stu-id="f4657-304">This value is not present by default and must be set manually.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-305">UserImportPath</span><span class="sxs-lookup"><span data-stu-id="f4657-305">UserImportPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-306">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-306">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-307">D:\SFTs</span><span class="sxs-lookup"><span data-stu-id="f4657-307">D:\SFTs</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="f4657-308">Действительно только в HKCU.</span><span class="sxs-lookup"><span data-stu-id="f4657-308">Valid only under HKCU.</span></span> <span data-ttu-id="f4657-309">Последнее расположение, на которое пользователь просматривает найденный SFT-файл для импорта пакета.</span><span class="sxs-lookup"><span data-stu-id="f4657-309">The last location the user browsed to while finding a SFT file for package import.</span></span> <span data-ttu-id="f4657-310">Задается автоматически, если SFT найден успешно.</span><span class="sxs-lookup"><span data-stu-id="f4657-310">Set automatically if the SFT is found successfully.</span></span> <span data-ttu-id="f4657-311">Этот способ используется при последовательных импортах при попытке автоматического обнаружения файлов SFT.</span><span class="sxs-lookup"><span data-stu-id="f4657-311">This is used on successive imports when trying to automatically locate SFT files.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f4657-312">Общий ключ</span><span class="sxs-lookup"><span data-stu-id="f4657-312">Shared Key</span></span>


<span data-ttu-id="f4657-313">Клавиши HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared используются для управления значениями, которые используются в компонентах App-V.</span><span class="sxs-lookup"><span data-stu-id="f4657-313">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared key controls values that are shared across App-V components.</span></span> <span data-ttu-id="f4657-314">В таблице ниже приведены сведения о значениях реестра, связанных с общим ключом.</span><span class="sxs-lookup"><span data-stu-id="f4657-314">The following table provides information about the registry values associated with the Shared key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4657-315">Имя</span><span class="sxs-lookup"><span data-stu-id="f4657-315">Name</span></span> </th>
<th align="left"><span data-ttu-id="f4657-316">Тип</span><span class="sxs-lookup"><span data-stu-id="f4657-316">Type</span></span> </th>
<th align="left"><span data-ttu-id="f4657-317">Данные (примеры)</span><span class="sxs-lookup"><span data-stu-id="f4657-317">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="f4657-318">Описание</span><span class="sxs-lookup"><span data-stu-id="f4657-318">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-319">DumpPath</span><span class="sxs-lookup"><span data-stu-id="f4657-319">DumpPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-320">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-320">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-321">Default = C:</span><span class="sxs-lookup"><span data-stu-id="f4657-321">Default=C:</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="f4657-322">Путь по умолчанию для создания файлов дампа при создании минидампа в исключении.</span><span class="sxs-lookup"><span data-stu-id="f4657-322">Default path to create dump files when generating a minidump on an exception.</span></span> <span data-ttu-id="f4657-323">По умолчанию используется значение C:\ Если не указано.</span><span class="sxs-lookup"><span data-stu-id="f4657-323">This defaults to C:\ if not specified.</span></span> <span data-ttu-id="f4657-324">Установщик клиента задает этот ключ для &lt; каталога глобальных данных в \Dumps. виртуализации приложений. &gt;</span><span class="sxs-lookup"><span data-stu-id="f4657-324">The Client installer sets this key to the &lt;App Virtualization global data directory&gt;\Dumps.</span></span> <span data-ttu-id="f4657-325">Программа Sequencer устанавливает этот раздел в каталог установки.</span><span class="sxs-lookup"><span data-stu-id="f4657-325">The Sequencer installer sets this key to the installation directory.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-326">DumpPathSizeLimit</span><span class="sxs-lookup"><span data-stu-id="f4657-326">DumpPathSizeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-327">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-327">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-328">1000</span><span class="sxs-lookup"><span data-stu-id="f4657-328">1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-329">Указывает максимальный общий объем дискового пространства в мегабайтах, который можно использовать для хранения минидампа.</span><span class="sxs-lookup"><span data-stu-id="f4657-329">Specifies the maximum total amount of disk space in megabytes that can be used to store minidumps.</span></span> <span data-ttu-id="f4657-330">По умолчанию = 1000 МБ.</span><span class="sxs-lookup"><span data-stu-id="f4657-330">Default = 1000 MB.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f4657-331">Ключ сети</span><span class="sxs-lookup"><span data-stu-id="f4657-331">Network Key</span></span>


<span data-ttu-id="f4657-332">Раздел HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network управляет различными параметрами, связанными с сетью.</span><span class="sxs-lookup"><span data-stu-id="f4657-332">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network key controls a variety of network-related parameters.</span></span> <span data-ttu-id="f4657-333">Этот ключ преимущественно используется агентом транспорта сети.</span><span class="sxs-lookup"><span data-stu-id="f4657-333">This key is primarily used by the network transport agent.</span></span> <span data-ttu-id="f4657-334">В таблице ниже приведены сведения о значениях реестра, связанных с ключом сети.</span><span class="sxs-lookup"><span data-stu-id="f4657-334">The following table provides information about the registry values associated with the Network key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4657-335">Имя</span><span class="sxs-lookup"><span data-stu-id="f4657-335">Name</span></span> </th>
<th align="left"><span data-ttu-id="f4657-336">Тип</span><span class="sxs-lookup"><span data-stu-id="f4657-336">Type</span></span> </th>
<th align="left"><span data-ttu-id="f4657-337">Данные (примеры)</span><span class="sxs-lookup"><span data-stu-id="f4657-337">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="f4657-338">Описание</span><span class="sxs-lookup"><span data-stu-id="f4657-338">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-339">Online</span><span class="sxs-lookup"><span data-stu-id="f4657-339">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-340">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-340">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-341">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="f4657-341">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-342">Включение или отключение автономного режима.</span><span class="sxs-lookup"><span data-stu-id="f4657-342">Enables or disables offline mode.</span></span> <span data-ttu-id="f4657-343">Если для него установлено значение 0, клиент не будет взаимодействовать с серверами управления App-V или серверами публикации.</span><span class="sxs-lookup"><span data-stu-id="f4657-343">If set to 0, the client will not communicate with App-V Management Servers or publishing servers.</span></span> <span data-ttu-id="f4657-344">В отключенных операциях клиент может запустить загруженное приложение, даже если оно не подключено к серверу управления App-V.</span><span class="sxs-lookup"><span data-stu-id="f4657-344">In disconnected operations, the client can start a loaded application even when it is not connected to an App-V Management Server.</span></span> <span data-ttu-id="f4657-345">В автономном режиме клиент не пытается подключиться к серверу управления App-V или серверу публикации.</span><span class="sxs-lookup"><span data-stu-id="f4657-345">In offline mode, the client does not attempt to connect to an App-V Management Server or publishing server.</span></span> <span data-ttu-id="f4657-346">Чтобы отключить возможность работы в автономном режиме, необходимо разрешить отключенные операции.</span><span class="sxs-lookup"><span data-stu-id="f4657-346">You must allow disconnected operations to be able to work offline.</span></span> <span data-ttu-id="f4657-347">По умолчанию используется значение 1 (в сети), а 0 — отключено (в автономном режиме).</span><span class="sxs-lookup"><span data-stu-id="f4657-347">Default value is 1 enabled (online), and 0 is disabled (offline).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-348">AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="f4657-348">AllowDisconnectedOperation</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-349">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-349">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-350">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="f4657-350">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-351">Включение или отключение отключенной операции.</span><span class="sxs-lookup"><span data-stu-id="f4657-351">Enables or disables disconnected operation.</span></span> <span data-ttu-id="f4657-352">Значение по умолчанию: 1 включено, а 0 — отключено.</span><span class="sxs-lookup"><span data-stu-id="f4657-352">Default value is 1 enabled, and 0 is disabled.</span></span> <span data-ttu-id="f4657-353">Если отключенные операции включены, клиент App-V может запустить загруженное приложение, даже если оно не подключено к серверу управления App-V.</span><span class="sxs-lookup"><span data-stu-id="f4657-353">When disconnected operations are enabled, the App-V client can start a loaded application even when it is not connected to an App-V Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-354">FastConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="f4657-354">FastConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-356">По умолчанию = 1000</span><span class="sxs-lookup"><span data-stu-id="f4657-356">Default=1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-357">Это значение определяет время ожидания TCP-соединения (в миллисекундах), чтобы определить, когда нужно перейти в режим разъединенных операций.</span><span class="sxs-lookup"><span data-stu-id="f4657-357">This value specifies the TCP connect time-out in milliseconds to determine when to go into disconnected operations mode.</span></span> <span data-ttu-id="f4657-358">Это значение можно использовать для переопределения значения по умолчанию ConnectTimeout, которое составляет 20 секунд (время ожидания для приложения-V-соединения для сетевых транзакций), или время ожидания TCP, которое составляет около 25 секунд.</span><span class="sxs-lookup"><span data-stu-id="f4657-358">This value can be used to override the default ConnectTimeout of 20 seconds (App-V connect time-out for network transactions) or the system’s TCP time-out of approximately 25 seconds.</span></span> <span data-ttu-id="f4657-359">Это позволяет быстро переключаться между клиентом в режиме отключенных операций.</span><span class="sxs-lookup"><span data-stu-id="f4657-359">This brings the client into disconnected operations mode quickly.</span></span> <span data-ttu-id="f4657-360">Применяется к следующему подключению.</span><span class="sxs-lookup"><span data-stu-id="f4657-360">Applied on the next connect.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-361">LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="f4657-361">LimitDisconnectedOperation</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-363">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="f4657-363">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-364">Применимо только в том случае, если AllowDisconnectedOperation является 1, а включено.</span><span class="sxs-lookup"><span data-stu-id="f4657-364">Applicable only if AllowDisconnectedOperation is 1, enabled.</span></span> <span data-ttu-id="f4657-365">Это значение определяет, ограничивается ли время, в течение которого клиент может работать в отключенных операциях.</span><span class="sxs-lookup"><span data-stu-id="f4657-365">This value determines whether there will be a time limit for how long the client will be allowed to operate in disconnected operations.</span></span> <span data-ttu-id="f4657-366">1 = ограничено.</span><span class="sxs-lookup"><span data-stu-id="f4657-366">1=limited.</span></span> <span data-ttu-id="f4657-367">0 = без ограничений.</span><span class="sxs-lookup"><span data-stu-id="f4657-367">0=unlimited.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-368">DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="f4657-368">DOTimeoutMinutes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-369">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-369">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-370">По умолчанию = 129600</span><span class="sxs-lookup"><span data-stu-id="f4657-370">Default=129,600</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-371">Указывает количество минут, в течение которых приложение может использоваться в режиме разъединенных операций.</span><span class="sxs-lookup"><span data-stu-id="f4657-371">Indicates how many minutes an application may be used in disconnected operation mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f4657-372">Допустимые значения: 1 – 999999 в днях (1 – 1439998560 минут).</span><span class="sxs-lookup"><span data-stu-id="f4657-372">The valid values are 1–999,999 in days expressed in minutes (1–1,439,998,560 minutes).</span></span> <span data-ttu-id="f4657-373">Значение по умолчанию — 90 дней или 129 600 минут.</span><span class="sxs-lookup"><span data-stu-id="f4657-373">The default value is 90 days or 129,600 minutes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-374">Используемый протокол</span><span class="sxs-lookup"><span data-stu-id="f4657-374">Protocol</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-375">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-375">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-376">По умолчанию = 8</span><span class="sxs-lookup"><span data-stu-id="f4657-376">Default=8</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-377">Используемый по умолчанию протокол (TCP и SSL).</span><span class="sxs-lookup"><span data-stu-id="f4657-377">Default protocol to use (TCP vs SSL).</span></span> <span data-ttu-id="f4657-378">Настройка в диалоговом окне "Параметры".</span><span class="sxs-lookup"><span data-stu-id="f4657-378">Configure in Options Dialog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-379">ReadTimeout</span><span class="sxs-lookup"><span data-stu-id="f4657-379">ReadTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-380">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-380">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-381">средняя</span><span class="sxs-lookup"><span data-stu-id="f4657-381">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-382">Время ожидания чтения сетевых транзакций (в секундах).</span><span class="sxs-lookup"><span data-stu-id="f4657-382">Read time-out for network transactions, in seconds.</span></span> <span data-ttu-id="f4657-383">Не изменяйте.</span><span class="sxs-lookup"><span data-stu-id="f4657-383">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-384">WriteTimeout</span><span class="sxs-lookup"><span data-stu-id="f4657-384">WriteTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-385">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-385">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-386">средняя</span><span class="sxs-lookup"><span data-stu-id="f4657-386">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-387">Время ожидания в секундах для транзакции на запись в сети.</span><span class="sxs-lookup"><span data-stu-id="f4657-387">Write time-out for network transactions, in seconds.</span></span> <span data-ttu-id="f4657-388">Не изменяйте.</span><span class="sxs-lookup"><span data-stu-id="f4657-388">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-389">ConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="f4657-389">ConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-390">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-390">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-391">средняя</span><span class="sxs-lookup"><span data-stu-id="f4657-391">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-392">Время ожидания подключения к сетевым транзакциям (в секундах).</span><span class="sxs-lookup"><span data-stu-id="f4657-392">Connect time-out for network transactions, in seconds.</span></span> <span data-ttu-id="f4657-393">Не изменяйте.</span><span class="sxs-lookup"><span data-stu-id="f4657-393">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-394">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="f4657-394">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-396">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="f4657-396">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-397">Количество попыток повторного установления прерванного сеанса.</span><span class="sxs-lookup"><span data-stu-id="f4657-397">The number of times to try to reestablish a dropped session.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-398">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="f4657-398">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-399">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-399">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-400">10-15</span><span class="sxs-lookup"><span data-stu-id="f4657-400">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-401">Число секунд ожидания между попытками восстановления прерванного сеанса.</span><span class="sxs-lookup"><span data-stu-id="f4657-401">The number of seconds to wait between tries to reestablish a dropped session.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f4657-402">Ключ HTTP</span><span class="sxs-lookup"><span data-stu-id="f4657-402">Http Key</span></span>


<span data-ttu-id="f4657-403">Раздел HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http определяет параметры, связанные с потоковой передачей HTTP.</span><span class="sxs-lookup"><span data-stu-id="f4657-403">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http key controls the parameters that are related to Http streaming.</span></span> <span data-ttu-id="f4657-404">Этот ключ используется преимущественно агентом транспорта сети.</span><span class="sxs-lookup"><span data-stu-id="f4657-404">This key is used primarily by the network transport agent.</span></span> <span data-ttu-id="f4657-405">В таблице ниже приведены сведения о значениях реестра, связанных с ключом http.</span><span class="sxs-lookup"><span data-stu-id="f4657-405">The following table provides information about the registry values that are associated with the Http key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4657-406">Имя</span><span class="sxs-lookup"><span data-stu-id="f4657-406">Name</span></span> </th>
<th align="left"><span data-ttu-id="f4657-407">Тип</span><span class="sxs-lookup"><span data-stu-id="f4657-407">Type</span></span> </th>
<th align="left"><span data-ttu-id="f4657-408">Данные (примеры)</span><span class="sxs-lookup"><span data-stu-id="f4657-408">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="f4657-409">Описание</span><span class="sxs-lookup"><span data-stu-id="f4657-409">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-410">LaunchIfNotFound</span><span class="sxs-lookup"><span data-stu-id="f4657-410">LaunchIfNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-411">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-411">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-412">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-412">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-413">Управляет поведением потоковой передачи HTTP, когда может быть установлено подключение к HTTP-серверу, и файл пакета больше не существует на HTTP-сервере.</span><span class="sxs-lookup"><span data-stu-id="f4657-413">Controls the behavior of HTTP streaming when a connection to the HTTP server can be established and the package file no longer exists on the HTTP server.</span></span> <span data-ttu-id="f4657-414">Если значение не существует или не равно 1, клиент App-V не позволяет запускать приложение, которое ранее было загружено в кэш.</span><span class="sxs-lookup"><span data-stu-id="f4657-414">If the value does not exist or if it is not set to 1, the App-V client does not let you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f4657-415">1,1</span><span class="sxs-lookup"><span data-stu-id="f4657-415">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-416">Если для этого параметра установлено значение 1, клиент App-V позволяет запускать приложение, которое ранее было загружено в кэш.</span><span class="sxs-lookup"><span data-stu-id="f4657-416">If this value is set to 1, the App-V client lets you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f4657-417">Ключ файловой системы</span><span class="sxs-lookup"><span data-stu-id="f4657-417">File System Key</span></span>


<span data-ttu-id="f4657-418">Значения, которые содержатся в разделе HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS, управляют параметрами файловой системы для App-V.</span><span class="sxs-lookup"><span data-stu-id="f4657-418">The values that are contained under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS key control the file system parameters for App-V.</span></span> <span data-ttu-id="f4657-419">В таблице ниже приведены сведения о значениях реестра, связанных с ключом AppFS.</span><span class="sxs-lookup"><span data-stu-id="f4657-419">The following table provides information about the registry values associated with the AppFS key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4657-420">Имя</span><span class="sxs-lookup"><span data-stu-id="f4657-420">Name</span></span> </th>
<th align="left"><span data-ttu-id="f4657-421">Тип</span><span class="sxs-lookup"><span data-stu-id="f4657-421">Type</span></span> </th>
<th align="left"><span data-ttu-id="f4657-422">Данные (примеры)</span><span class="sxs-lookup"><span data-stu-id="f4657-422">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="f4657-423">Описание</span><span class="sxs-lookup"><span data-stu-id="f4657-423">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-424">FileSize</span><span class="sxs-lookup"><span data-stu-id="f4657-424">FileSize</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-425">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-425">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-426">4096</span><span class="sxs-lookup"><span data-stu-id="f4657-426">4096</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-427">Максимальный размер файла кэша файловой системы (в мегабайтах).</span><span class="sxs-lookup"><span data-stu-id="f4657-427">Maximum size in megabytes of file system cache file.</span></span> <span data-ttu-id="f4657-428">Если изменить это значение в реестре, необходимо установить для параметра Состояние значение 0 и перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="f4657-428">If you change this value in the registry, you must set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-429">FileName</span><span class="sxs-lookup"><span data-stu-id="f4657-429">FileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-430">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-430">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-431">C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="f4657-431">C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-432">Расположение файла кэша файловой системы.</span><span class="sxs-lookup"><span data-stu-id="f4657-432">Location of file system cache file.</span></span> <span data-ttu-id="f4657-433">Если изменить это значение в реестре, необходимо оставить FileSize таким же, чтобы перезапустить или установить состояние 0 и перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="f4657-433">If you change this value in the registry, you must either leave FileSize the same and reboot or set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-434">Буква_диска</span><span class="sxs-lookup"><span data-stu-id="f4657-434">DriveLetter</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-435">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-435">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-436">Вопрос.</span><span class="sxs-lookup"><span data-stu-id="f4657-436">Q:</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-437">Диск, на котором будет смонтирована файловая система App-V (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="f4657-437">Drive where App-V file system will be mounted, if it is available.</span></span> <span data-ttu-id="f4657-438">Это значение задается либо прослушивателем, либо установщиком, и оно читается в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="f4657-438">This value is set either by the listener or the installer, and it is read by the file system.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-439">Состояние</span><span class="sxs-lookup"><span data-stu-id="f4657-439">State</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-440">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-440">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-441">0x100</span><span class="sxs-lookup"><span data-stu-id="f4657-441">0x100</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-442">Состояние файловой системы.</span><span class="sxs-lookup"><span data-stu-id="f4657-442">State of file system.</span></span> <span data-ttu-id="f4657-443">Установите значение 0 и перезагрузите компьютер, чтобы полностью очистить кэш файловой системы.</span><span class="sxs-lookup"><span data-stu-id="f4657-443">Set to 0 and reboot to completely clear the file system cache.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-444">FileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="f4657-444">FileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-445">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-445">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-446">C:\Profiles\Joe\SG</span><span class="sxs-lookup"><span data-stu-id="f4657-446">C:\Profiles\Joe\SG</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-447">Путь для symlinks, заданный в разделе HKCU.</span><span class="sxs-lookup"><span data-stu-id="f4657-447">Path for symlinks, set under HKCU.</span></span> <span data-ttu-id="f4657-448">Не изменяйте (используйте каталог данных в разделе Конфигурация для изменения).</span><span class="sxs-lookup"><span data-stu-id="f4657-448">Do not modify (use data directory under Configuration to change).</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-449">GlobalFileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="f4657-449">GlobalFileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-450">Строка</span><span class="sxs-lookup"><span data-stu-id="f4657-450">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-451">Хранилище C:\Users\Public\Documents\SoftGrid Client\AppFS</span><span class="sxs-lookup"><span data-stu-id="f4657-451">C:\Users\Public\Documents\SoftGrid Client\AppFS Storage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-452">Путь для данных глобальной файловой системы.</span><span class="sxs-lookup"><span data-stu-id="f4657-452">Path for global file system data.</span></span> <span data-ttu-id="f4657-453">Не изменяйте.</span><span class="sxs-lookup"><span data-stu-id="f4657-453">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-454">MaxPercentToLockInCache</span><span class="sxs-lookup"><span data-stu-id="f4657-454">MaxPercentToLockInCache</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-455">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-455">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-456">По умолчанию = 90</span><span class="sxs-lookup"><span data-stu-id="f4657-456">Default=90</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-457">Задает максимальный процент файла кэша файловой системы, который может быть заблокирован.</span><span class="sxs-lookup"><span data-stu-id="f4657-457">Specifies the maximum percentage of the file system cache file that can be locked.</span></span> <span data-ttu-id="f4657-458">Не изменяйте.</span><span class="sxs-lookup"><span data-stu-id="f4657-458">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-459">UnloadLeastRecentlyUsed</span><span class="sxs-lookup"><span data-stu-id="f4657-459">UnloadLeastRecentlyUsed</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-460">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-460">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-461">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="f4657-461">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-462">Функция управления пространством кэша файловой системы использует самый последний использованный алгоритм (LRU) и включен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4657-462">The file system cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="f4657-463">Если пространство, необходимое для нового пакета, превысит доступное свободное пространство в кэше, клиент App-V использует эту функцию, чтобы определить, какие из существующих пакетов можно удалить из кэша, чтобы освободить место для нового пакета.</span><span class="sxs-lookup"><span data-stu-id="f4657-463">If the space that is required for a new package would exceed the available free space in the cache, the App-V Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="f4657-464">Клиент удаляет пакет с самой ранней датой последнего доступа, если он старше значения, указанного в параметре реестра MinPkgAge.</span><span class="sxs-lookup"><span data-stu-id="f4657-464">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="f4657-465">Значения: 0 (отключено) и 1 (по умолчанию, включено).</span><span class="sxs-lookup"><span data-stu-id="f4657-465">Values are 0 (disabled) and 1 (default, enabled).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-466">MinPackageAge</span><span class="sxs-lookup"><span data-stu-id="f4657-466">MinPackageAge</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-467">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-467">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-468">1,1</span><span class="sxs-lookup"><span data-stu-id="f4657-468">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-469">Чтобы определить, когда можно выбрать пакет для удаления, установите для этого параметра реестра минимальное число дней, которое вы хотите пропройти с момента последнего доступа к пакету.</span><span class="sxs-lookup"><span data-stu-id="f4657-469">To determine when the package can be selected for discard, set this registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="f4657-470">Пакеты, которые использовались в последнее время, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="f4657-470">Packages that have been used more recently are not discarded.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f4657-471">Ключ разрешений</span><span class="sxs-lookup"><span data-stu-id="f4657-471">Permissions Key</span></span>


<span data-ttu-id="f4657-472">Чтобы запретить пользователям вносить ошибки, администраторы могут использовать клавишу HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions для управления доступом к определенным действиям для пользователей, не являющихся администраторами, например, чтобы предотвратить случайную выгрузку программ.</span><span class="sxs-lookup"><span data-stu-id="f4657-472">To help to prevent users from making mistakes, administrators can use the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions key to control access to some actions for non-administrative users—for example, to prevent users from accidentally unloading programs.</span></span> <span data-ttu-id="f4657-473">Пользователи с правами администратора могут предоставлять любые из этих разрешений.</span><span class="sxs-lookup"><span data-stu-id="f4657-473">Users with administrative rights can give themselves any of these permissions.</span></span> <span data-ttu-id="f4657-474">В общедоступных системах, таких как сервер сеанса удаленных рабочих столов (сервер сеансов удаленных рабочих столов) (ранее — сервера терминалов), будьте внимательны при предоставлении пользователям дополнительных разрешений, так как некоторые из этих разрешений позволяют пользователям управлять приложениями, используемыми всеми пользователями системы.</span><span class="sxs-lookup"><span data-stu-id="f4657-474">On shared systems, such as a Remote Desktop Session Host (RD Session Host) server (formerly Terminal Server) system, be careful when granting additional permissions to users because some of these permissions would enable users to control the applications used by all users on the system.</span></span> <span data-ttu-id="f4657-475">Возможные значения для этих параметров: 1 (разрешить) и 0 (запретить).</span><span class="sxs-lookup"><span data-stu-id="f4657-475">Possible values for these settings are 1 (allow) and 0 (disallow).</span></span>

<span data-ttu-id="f4657-476">Параметры ключа разрешений управляют всеми интерфейсами, которые включают указанные действия.</span><span class="sxs-lookup"><span data-stu-id="f4657-476">The Permissions key settings control all interfaces that enable the named actions.</span></span> <span data-ttu-id="f4657-477">Это относится к диалоговому окну Параметры, SFTTray и SFTMime.</span><span class="sxs-lookup"><span data-stu-id="f4657-477">This includes the Options Dialog, SFTTray, and SFTMime.</span></span> <span data-ttu-id="f4657-478">Эти параметры не влияют на администраторов.</span><span class="sxs-lookup"><span data-stu-id="f4657-478">These settings do not affect administrators.</span></span> <span data-ttu-id="f4657-479">В таблице ниже приведены сведения о значениях реестра, связанных с ключом "разрешения".</span><span class="sxs-lookup"><span data-stu-id="f4657-479">The following table provides information about the registry values associated with the Permissions key.</span></span>

<span data-ttu-id="f4657-480">Name Type Data (примеры) Description ChangeFSDrive</span><span class="sxs-lookup"><span data-stu-id="f4657-480">Name Type Data (Examples) Description ChangeFSDrive</span></span>

<span data-ttu-id="f4657-481">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-481">DWORD</span></span>

<span data-ttu-id="f4657-482">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-482">Default=0</span></span>

<span data-ttu-id="f4657-483">Значение 1 позволяет пользователям выбрать другую букву диска для использования в качестве диска файловой системы.</span><span class="sxs-lookup"><span data-stu-id="f4657-483">A value of 1 allows users to pick a different drive letter to be used as the file system drive.</span></span>

<span data-ttu-id="f4657-484">ChangeCacheSize</span><span class="sxs-lookup"><span data-stu-id="f4657-484">ChangeCacheSize</span></span>

<span data-ttu-id="f4657-485">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-485">DWORD</span></span>

<span data-ttu-id="f4657-486">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-486">Default=0</span></span>

<span data-ttu-id="f4657-487">Значение 1 позволяет пользователям изменять размер кэша.</span><span class="sxs-lookup"><span data-stu-id="f4657-487">A value of 1 allows users to change the cache size.</span></span>

<span data-ttu-id="f4657-488">ChangeLogSettings</span><span class="sxs-lookup"><span data-stu-id="f4657-488">ChangeLogSettings</span></span>

<span data-ttu-id="f4657-489">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-489">DWORD</span></span>

<span data-ttu-id="f4657-490">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-490">Default=0</span></span>

<span data-ttu-id="f4657-491">Значение 1 позволяет пользователям изменять уровень журнала, изменять его расположение и сбрасывать его через пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f4657-491">A value of 1 allows users to modify the log level, change its location, and reset it through the user interface.</span></span>

<span data-ttu-id="f4657-492">AddApp</span><span class="sxs-lookup"><span data-stu-id="f4657-492">AddApp</span></span>

<span data-ttu-id="f4657-493">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-493">DWORD</span></span>

<span data-ttu-id="f4657-494">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-494">Default=0</span></span>

<span data-ttu-id="f4657-495">Значение 1 позволяет пользователям явно добавлять приложения.</span><span class="sxs-lookup"><span data-stu-id="f4657-495">A value of 1 allows users to add applications explicitly.</span></span> <span data-ttu-id="f4657-496">Это не повлияет на приложения, которые были добавлены с помощью публикации и не допускают запуск (и поэтому неявно добавляет) приложения, которые еще не были добавлены.</span><span class="sxs-lookup"><span data-stu-id="f4657-496">This does not affect applications that are added through publishing refresh nor does it prevent users from starting (and thereby implicitly adding) applications that have not already been added.</span></span> <span data-ttu-id="f4657-497">Значения 0 и 1.</span><span class="sxs-lookup"><span data-stu-id="f4657-497">Values are 0 or 1.</span></span>

<span data-ttu-id="f4657-498">LoadApp</span><span class="sxs-lookup"><span data-stu-id="f4657-498">LoadApp</span></span> 

<span data-ttu-id="f4657-499">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-499">DWORD</span></span> 

<span data-ttu-id="f4657-500">до</span><span class="sxs-lookup"><span data-stu-id="f4657-500">0</span></span>

<span data-ttu-id="f4657-501">Не позволяет пользователю загрузить приложение.</span><span class="sxs-lookup"><span data-stu-id="f4657-501">Does not allow a user to load an application.</span></span> <span data-ttu-id="f4657-502">Это значение по умолчанию для узлов сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f4657-502">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="f4657-503">Если вы являетесь мобильным пользователем, вам может потребоваться полностью загрузить в кэш приложения, чтобы использовать их во время отключенной операции или автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="f4657-503">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="f4657-504">Для потоковой передачи приложений с сервера управления App-V или потокового сервера App-V необходимо подключение к серверу для загрузки приложений.</span><span class="sxs-lookup"><span data-stu-id="f4657-504">To stream applications from the App-V Management Server or the App-V Streaming Server, you must be connected to a server to load applications.</span></span>

<span data-ttu-id="f4657-505">1,1</span><span class="sxs-lookup"><span data-stu-id="f4657-505">1</span></span>

<span data-ttu-id="f4657-506">Позволяет пользователю загрузить приложение.</span><span class="sxs-lookup"><span data-stu-id="f4657-506">Allows a user to load an application.</span></span> <span data-ttu-id="f4657-507">Это значение по умолчанию для настольных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="f4657-507">This is the default for Windows desktops.</span></span> 

<span data-ttu-id="f4657-508">UnloadApp</span><span class="sxs-lookup"><span data-stu-id="f4657-508">UnloadApp</span></span> 

<span data-ttu-id="f4657-509">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-509">DWORD</span></span> 

<span data-ttu-id="f4657-510">до</span><span class="sxs-lookup"><span data-stu-id="f4657-510">0</span></span>

<span data-ttu-id="f4657-511">Запрещает пользователю выгрузить приложение.</span><span class="sxs-lookup"><span data-stu-id="f4657-511">Does not allow a user to unload an application.</span></span> <span data-ttu-id="f4657-512">При загрузке или выгрузке пакета все приложения в пакете загружаются в кэш или удаляются из него.</span><span class="sxs-lookup"><span data-stu-id="f4657-512">When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span>

<span data-ttu-id="f4657-513">1,1</span><span class="sxs-lookup"><span data-stu-id="f4657-513">1</span></span>

<span data-ttu-id="f4657-514">Позволяет пользователю выгрузить приложение.</span><span class="sxs-lookup"><span data-stu-id="f4657-514">Allows a user to unload an application.</span></span> 

<span data-ttu-id="f4657-515">LockApp</span><span class="sxs-lookup"><span data-stu-id="f4657-515">LockApp</span></span> 

<span data-ttu-id="f4657-516">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-516">DWORD</span></span> 

<span data-ttu-id="f4657-517">до</span><span class="sxs-lookup"><span data-stu-id="f4657-517">0</span></span>

<span data-ttu-id="f4657-518">Запрещает пользователю блокировать и разблокировать приложение.</span><span class="sxs-lookup"><span data-stu-id="f4657-518">Does not allow a user to lock and unlock an application.</span></span> <span data-ttu-id="f4657-519">Это значение по умолчанию для узлов сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f4657-519">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="f4657-520">Заблокированное приложение не может быть удалено из кэша, чтобы освободить место для новых приложений.</span><span class="sxs-lookup"><span data-stu-id="f4657-520">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="f4657-521">Чтобы удалить заблокированное приложение с компьютера App-V или клиента для кэша служб удаленных рабочих столов (ранее служб терминалов), необходимо разблокировать его.</span><span class="sxs-lookup"><span data-stu-id="f4657-521">To remove a locked application from the App-V Desktop or Client for Remote Desktop Services (formerly Terminal Services) cache, you must unlock it.</span></span>

<span data-ttu-id="f4657-522">1,1</span><span class="sxs-lookup"><span data-stu-id="f4657-522">1</span></span>

<span data-ttu-id="f4657-523">Позволяет пользователю блокировать и разблокировать приложение.</span><span class="sxs-lookup"><span data-stu-id="f4657-523">Allows a user to lock and unlock an application.</span></span> <span data-ttu-id="f4657-524">Это значение по умолчанию для настольных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="f4657-524">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="f4657-525">ManageTypes</span><span class="sxs-lookup"><span data-stu-id="f4657-525">ManageTypes</span></span> 

<span data-ttu-id="f4657-526">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-526">DWORD</span></span> 

<span data-ttu-id="f4657-527">до</span><span class="sxs-lookup"><span data-stu-id="f4657-527">0</span></span>

<span data-ttu-id="f4657-528">Пользователи не смогут добавлять, изменять и удалять сопоставления типов файлов для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="f4657-528">Does not allow a user to add, edit, or remove file type associations for that User alone.</span></span> <span data-ttu-id="f4657-529">Это значение по умолчанию для узлов сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f4657-529">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="f4657-530">1,1</span><span class="sxs-lookup"><span data-stu-id="f4657-530">1</span></span>

<span data-ttu-id="f4657-531">Позволяет пользователю добавлять, изменять и удалять сопоставления типов файлов только для этого пользователя, а не глобально.</span><span class="sxs-lookup"><span data-stu-id="f4657-531">Allows a user to add, edit, and remove file type associations for that user only and not globally.</span></span> <span data-ttu-id="f4657-532">Это значение по умолчанию для настольных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="f4657-532">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="f4657-533">RefreshServer</span><span class="sxs-lookup"><span data-stu-id="f4657-533">RefreshServer</span></span> 

<span data-ttu-id="f4657-534">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-534">DWORD</span></span> 

<span data-ttu-id="f4657-535">до</span><span class="sxs-lookup"><span data-stu-id="f4657-535">0</span></span>

<span data-ttu-id="f4657-536">Не позволяет пользователю инициировать обновление параметров MIME.</span><span class="sxs-lookup"><span data-stu-id="f4657-536">Does not allow a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="f4657-537">Это значение по умолчанию для узлов сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f4657-537">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="f4657-538">1,1</span><span class="sxs-lookup"><span data-stu-id="f4657-538">1</span></span>

<span data-ttu-id="f4657-539">Позволяет пользователю инициировать обновление параметров MIME.</span><span class="sxs-lookup"><span data-stu-id="f4657-539">Enables a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="f4657-540">Это значение по умолчанию для настольных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="f4657-540">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="f4657-541">UpdateOSDFile</span><span class="sxs-lookup"><span data-stu-id="f4657-541">UpdateOSDFile</span></span>

<span data-ttu-id="f4657-542">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-542">DWORD</span></span>

<span data-ttu-id="f4657-543">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-543">Default= 0</span></span>

<span data-ttu-id="f4657-544">Значение 1 позволяет пользователю использовать модифицированный OSD-файл.</span><span class="sxs-lookup"><span data-stu-id="f4657-544">A value of 1 enables a user to use a modified OSD file.</span></span>

<span data-ttu-id="f4657-545">ImportApp</span><span class="sxs-lookup"><span data-stu-id="f4657-545">ImportApp</span></span> 

<span data-ttu-id="f4657-546">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-546">DWORD</span></span> 

<span data-ttu-id="f4657-547">до</span><span class="sxs-lookup"><span data-stu-id="f4657-547">0</span></span>

<span data-ttu-id="f4657-548">Запрещает пользователю импортировать приложения в кэш.</span><span class="sxs-lookup"><span data-stu-id="f4657-548">Does not allow a user to import applications into cache.</span></span> <span data-ttu-id="f4657-549">Разница между загрузкой и импортом заключается в том, что при срабатывании нагрузки клиент получает пакет из расположения, заданного в настоящее время, которое содержится в этом URL-адресе: OSD, ASR или override.</span><span class="sxs-lookup"><span data-stu-id="f4657-549">The difference between Load and Import is that when a Load is triggered, the client gets the package from the currently configured location contained in the OSD, ASR, or Override URL.</span></span> <span data-ttu-id="f4657-550">При использовании функции Импорт необходимо указать расположение, в котором нужно получить пакет.</span><span class="sxs-lookup"><span data-stu-id="f4657-550">When using Import, a location to get the package from must be specified.</span></span> 

<span data-ttu-id="f4657-551">1,1</span><span class="sxs-lookup"><span data-stu-id="f4657-551">1</span></span>

<span data-ttu-id="f4657-552">Позволяет пользователю импортировать приложения в кэш.</span><span class="sxs-lookup"><span data-stu-id="f4657-552">Allows a user to import applications into cache.</span></span> 

<span data-ttu-id="f4657-553">ChangeRefreshSettings</span><span class="sxs-lookup"><span data-stu-id="f4657-553">ChangeRefreshSettings</span></span>

<span data-ttu-id="f4657-554">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-554">DWORD</span></span>

<span data-ttu-id="f4657-555">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-555">Default=0</span></span>

<span data-ttu-id="f4657-556">Значение 1 позволяет пользователям изменять параметры обновления серверов (обновление при входе и периодическое обновление).</span><span class="sxs-lookup"><span data-stu-id="f4657-556">A value of 1 allows users to modify the refresh settings for servers (refresh on login and periodic refresh).</span></span> <span data-ttu-id="f4657-557">Это не означает, что пользователь может изменить другие параметры сервера (путь, узел и т. д.).</span><span class="sxs-lookup"><span data-stu-id="f4657-557">This does not imply that the user can modify other server settings (path, host, and so on).</span></span>

<span data-ttu-id="f4657-558">ManageServers</span><span class="sxs-lookup"><span data-stu-id="f4657-558">ManageServers</span></span>

<span data-ttu-id="f4657-559">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-559">DWORD</span></span>

<span data-ttu-id="f4657-560">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-560">Default=0</span></span>

<span data-ttu-id="f4657-561">Значение 1 позволяет пользователю добавлять, изменять и удалять серверы, за исключением редактирования параметров обновления, который управляется разрешением ChangeRefreshSettings.</span><span class="sxs-lookup"><span data-stu-id="f4657-561">A value of 1 allows the user to add, edit, and remove servers, except for editing the refresh settings, which is controlled by the ChangeRefreshSettings permission.</span></span>

<span data-ttu-id="f4657-562">PublishShortcut</span><span class="sxs-lookup"><span data-stu-id="f4657-562">PublishShortcut</span></span>

<span data-ttu-id="f4657-563">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-563">DWORD</span></span>

<span data-ttu-id="f4657-564">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-564">Default=0</span></span>

<span data-ttu-id="f4657-565">Значение 1 позволяет пользователям публиковать сочетания клавиш через пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f4657-565">A value of 1 allows users to publish shortcuts through the user interface.</span></span> <span data-ttu-id="f4657-566">Это не влияет на сочетания клавиш, которые публикуются при обновлении публикации.</span><span class="sxs-lookup"><span data-stu-id="f4657-566">This does not affect shortcuts that are published during a publishing refresh.</span></span>

<span data-ttu-id="f4657-567">ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="f4657-567">ViewAllApplications</span></span>

<span data-ttu-id="f4657-568">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-568">DWORD</span></span>

<span data-ttu-id="f4657-569">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-569">Default=0</span></span>

<span data-ttu-id="f4657-570">Значение 1 отображает все приложения с помощью пользовательского интерфейса; в противном случае отображаются только приложения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f4657-570">A value of 1 displays all applications through the user interface; otherwise, only the user’s applications are displayed.</span></span>

<span data-ttu-id="f4657-571">RepairApp</span><span class="sxs-lookup"><span data-stu-id="f4657-571">RepairApp</span></span>

<span data-ttu-id="f4657-572">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-572">DWORD</span></span>

<span data-ttu-id="f4657-573">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="f4657-573">Default=1</span></span>

<span data-ttu-id="f4657-574">Значение 1 позволяет пользователю использовать действие по восстановлению для приложений в SFTMime или консоли управления клиентом.</span><span class="sxs-lookup"><span data-stu-id="f4657-574">A value of 1 allows the user to use the Repair action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="f4657-575">При восстановлении приложения удаляются все пользовательские настройки и восстанавливаются параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4657-575">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="f4657-576">Это действие не приводит к изменению или удалению ярлыков и сопоставлений типов файлов, но не удаляет приложение из кэша.</span><span class="sxs-lookup"><span data-stu-id="f4657-576">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

<span data-ttu-id="f4657-577">ClearApp</span><span class="sxs-lookup"><span data-stu-id="f4657-577">ClearApp</span></span>

<span data-ttu-id="f4657-578">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-578">DWORD</span></span>

<span data-ttu-id="f4657-579">По умолчанию = 1</span><span class="sxs-lookup"><span data-stu-id="f4657-579">Default=1</span></span>

<span data-ttu-id="f4657-580">Значение 1 позволяет пользователю использовать действие Clear в приложениях в SFTMime или консоли управления клиентом.</span><span class="sxs-lookup"><span data-stu-id="f4657-580">A value of 1 allows the user to use the Clear action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="f4657-581">Когда вы удаляете приложение с консоли, вы больше не сможете пользоваться этим приложением.</span><span class="sxs-lookup"><span data-stu-id="f4657-581">When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="f4657-582">Однако приложение остается в кэше и по-прежнему доступно другим пользователям в той же системе.</span><span class="sxs-lookup"><span data-stu-id="f4657-582">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="f4657-583">После обновления публикации удаленные приложения станут доступны вам.</span><span class="sxs-lookup"><span data-stu-id="f4657-583">After a publishing refresh, the cleared applications will again become available to you.</span></span>

<span data-ttu-id="f4657-584">DeleteApp</span><span class="sxs-lookup"><span data-stu-id="f4657-584">DeleteApp</span></span>

<span data-ttu-id="f4657-585">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-585">DWORD</span></span>

<span data-ttu-id="f4657-586">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-586">Default=0</span></span>

<span data-ttu-id="f4657-587">Значение 1 позволяет пользователю использовать действие DELETE для приложений в SFTMime или консоли управления клиентом.</span><span class="sxs-lookup"><span data-stu-id="f4657-587">A value of 1 allows the user to use the Delete action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="f4657-588">Когда вы удаляете приложение, выбранное приложение больше не будет доступно для всех пользователей на этом клиенте.</span><span class="sxs-lookup"><span data-stu-id="f4657-588">When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="f4657-589">Сочетания клавиш и сопоставления типов файлов удаляются, а приложение удаляется из кэша.</span><span class="sxs-lookup"><span data-stu-id="f4657-589">Shortcuts and file type associations are deleted and the application is deleted from cache.</span></span> <span data-ttu-id="f4657-590">Тем не менее, если другое приложение ссылается на данные в кэше файловой системы или данные параметров для выбранного приложения, эти элементы не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="f4657-590">However, if another application refers to data in the file system cache or settings data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="f4657-591">После обновления публикации удаленные приложения станут доступны вам.</span><span class="sxs-lookup"><span data-stu-id="f4657-591">After a publishing refresh, the deleted applications will again become available to you.</span></span>

<span data-ttu-id="f4657-592">ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="f4657-592">ToggleOfflineMode</span></span>

<span data-ttu-id="f4657-593">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-593">DWORD</span></span>

<span data-ttu-id="f4657-594">Если выбрано значение 1, пользователи могут запускать клиент в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="f4657-594">A value of 1 allows the users to select to run the client in Offline Mode.</span></span> <span data-ttu-id="f4657-595">В автономном режиме клиент Application Virtualization может запустить загруженное приложение, даже если оно не подключено к серверу Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f4657-595">In Offline Mode, the Application Virtualization client can start a loaded application even when it is not connected to an Application Virtualization Server.</span></span>



## <span data-ttu-id="f4657-596">Пользовательские параметры</span><span class="sxs-lookup"><span data-stu-id="f4657-596">Custom Settings</span></span>


<span data-ttu-id="f4657-597">Раздел HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings содержат значения, относящиеся к интерфейсным компонентам.</span><span class="sxs-lookup"><span data-stu-id="f4657-597">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings key contains values specific to front-end components.</span></span> <span data-ttu-id="f4657-598">Все пользовательские параметры хранятся как строки.</span><span class="sxs-lookup"><span data-stu-id="f4657-598">All custom settings are stored as strings.</span></span> <span data-ttu-id="f4657-599">В таблице ниже приведены сведения о значениях реестра, связанных с ключом CustomSettings.</span><span class="sxs-lookup"><span data-stu-id="f4657-599">The following table provides information about the registry values associated with the CustomSettings key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4657-600">Имя</span><span class="sxs-lookup"><span data-stu-id="f4657-600">Name</span></span> </th>
<th align="left"><span data-ttu-id="f4657-601">Тип</span><span class="sxs-lookup"><span data-stu-id="f4657-601">Type</span></span> </th>
<th align="left"><span data-ttu-id="f4657-602">Данные (примеры)</span><span class="sxs-lookup"><span data-stu-id="f4657-602">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="f4657-603">Описание</span><span class="sxs-lookup"><span data-stu-id="f4657-603">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-604">TrayErrorDelay</span><span class="sxs-lookup"><span data-stu-id="f4657-604">TrayErrorDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-605">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-605">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-606">По умолчанию = 30</span><span class="sxs-lookup"><span data-stu-id="f4657-606">Default=30</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-607">Время в секундах, в течение которого область уведомлений Application Virtualization выведет сообщения об ошибках, например &quot; Запуск не удался &quot; .</span><span class="sxs-lookup"><span data-stu-id="f4657-607">Time in seconds that the Application Virtualization notification area will display error messages like &quot;Launch failed&quot;.</span></span> <span data-ttu-id="f4657-608">Минимальное значение, равное 1.</span><span class="sxs-lookup"><span data-stu-id="f4657-608">Minimum value of 1.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-609">TraySuccessDelay</span><span class="sxs-lookup"><span data-stu-id="f4657-609">TraySuccessDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-610">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-610">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-611">По умолчанию = 10</span><span class="sxs-lookup"><span data-stu-id="f4657-611">Default=10</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4657-612">Время в секундах, в течение которого в области уведомлений appvmed отображаются сообщения об успешном завершении работы, такие как &quot; Word запущены &quot; или &quot; Excel &quot; .</span><span class="sxs-lookup"><span data-stu-id="f4657-612">Time in seconds that the appvmed notification area will display success messages like &quot;Word launched&quot; or &quot;Excel shut down&quot;.</span></span> <span data-ttu-id="f4657-613">Если 0, эти сообщения будут подавлены.</span><span class="sxs-lookup"><span data-stu-id="f4657-613">If 0, those messages will be suppressed.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-614">TrayVisibility</span><span class="sxs-lookup"><span data-stu-id="f4657-614">TrayVisibility</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-615">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-615">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-616">По умолчанию = 0</span><span class="sxs-lookup"><span data-stu-id="f4657-616">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-617">0 = показывать лоток, если виртуализированные приложения используются.</span><span class="sxs-lookup"><span data-stu-id="f4657-617">0=Show Tray when virtualized applications are in use.</span></span></p>
<p><span data-ttu-id="f4657-618">1 = отображать лоток всегда.</span><span class="sxs-lookup"><span data-stu-id="f4657-618">1=Show Tray always.</span></span></p>
<p><span data-ttu-id="f4657-619">2 = не показывать лоток.</span><span class="sxs-lookup"><span data-stu-id="f4657-619">2=Never show Tray.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-620">TrayShowRefresh</span><span class="sxs-lookup"><span data-stu-id="f4657-620">TrayShowRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-621">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-621">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f4657-622">Если задано значение 1, элемент меню позволяет обновить приложения, чтобы они отображались в меню табло и были доступны пользователю.</span><span class="sxs-lookup"><span data-stu-id="f4657-622">When present and set to a value of 1, allows menu item Refresh Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-623">TrayShowLoad</span><span class="sxs-lookup"><span data-stu-id="f4657-623">TrayShowLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-624">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-624">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f4657-625">Если присвоено значение 1, элемент меню позволяет загружать приложения в меню области задач и доступен пользователю.</span><span class="sxs-lookup"><span data-stu-id="f4657-625">When present and set to a value of 1, allows menu item Load Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f4657-626">Параметры отчетов</span><span class="sxs-lookup"><span data-stu-id="f4657-626">Reporting Settings</span></span>


<span data-ttu-id="f4657-627">Раздел HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting содержат значения, относящиеся к отправке отчетов на сервер управления App-V.</span><span class="sxs-lookup"><span data-stu-id="f4657-627">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting key contains values specific to reporting to an App-V Management Server.</span></span> <span data-ttu-id="f4657-628">В таблице ниже приведены сведения о значениях реестра, связанных с ключом Reporting.</span><span class="sxs-lookup"><span data-stu-id="f4657-628">The following table provides information about the registry values associated with the Reporting key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4657-629">Имя</span><span class="sxs-lookup"><span data-stu-id="f4657-629">Name</span></span> </th>
<th align="left"><span data-ttu-id="f4657-630">Тип</span><span class="sxs-lookup"><span data-stu-id="f4657-630">Type</span></span> </th>
<th align="left"><span data-ttu-id="f4657-631">Данные (примеры)</span><span class="sxs-lookup"><span data-stu-id="f4657-631">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="f4657-632">Описание</span><span class="sxs-lookup"><span data-stu-id="f4657-632">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4657-633">DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="f4657-633">DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-634">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-634">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-635">По умолчанию = 20</span><span class="sxs-lookup"><span data-stu-id="f4657-635">Default=20</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-636">Это значение определяет максимальный размер кэша XML в мегабайтах (МБ) для хранения данных отчета.</span><span class="sxs-lookup"><span data-stu-id="f4657-636">This value specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="f4657-637">Размер применяется к кэшу в памяти.</span><span class="sxs-lookup"><span data-stu-id="f4657-637">The size applies to the cache in memory.</span></span> <span data-ttu-id="f4657-638">По достижении этого предела файл журнала будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="f4657-638">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="f4657-639">При добавлении новой записи (нижней части списка) одна или несколько самых ранних записей (вверху списка) будут удалены, чтобы освободить место.</span><span class="sxs-lookup"><span data-stu-id="f4657-639">When a new record is added (bottom of the list), one or more of the oldest records (top of the list) will be deleted to make room.</span></span> <span data-ttu-id="f4657-640">Предупреждение будет записано в журнал клиента, а в первый раз — в журнал событий, и он не будет регистрироваться повторно до тех пор, пока не завершится успешный повторный вызов кэша, после чего журнал снова станет заполнен.</span><span class="sxs-lookup"><span data-stu-id="f4657-640">A warning will be logged to the Client log and the event log the first time this occurs, and it will not be logged again until after the cache has been successfully cleared on transmission and the log has filled up again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4657-641">DataBlockSize</span><span class="sxs-lookup"><span data-stu-id="f4657-641">DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-642">DWORD</span><span class="sxs-lookup"><span data-stu-id="f4657-642">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-643">По умолчанию = 65 536</span><span class="sxs-lookup"><span data-stu-id="f4657-643">Default=65536</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4657-644">Это значение задает максимальный размер (в байтах), который должен быть передан на сервер одновременно при обновлении публикации, чтобы избежать сбоев при неустранимой передаче журнала при значительном размере.</span><span class="sxs-lookup"><span data-stu-id="f4657-644">This value specifies the maximum size in bytes to transmit to the server at once on publishing refresh, to avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="f4657-645">Значение по умолчанию — 65536.</span><span class="sxs-lookup"><span data-stu-id="f4657-645">The default value is 65536.</span></span> <span data-ttu-id="f4657-646">При передаче данных отчета на сервер один блок записей приложения, не превышающий размер блока в байтах данных XML, будет удален из кэша и отправлен на сервер.</span><span class="sxs-lookup"><span data-stu-id="f4657-646">When transmitting report data to the server, one block of application records—less than or equal to the block size in bytes of XML data—will be removed from the cache and sent to the server.</span></span> <span data-ttu-id="f4657-647">Каждому блоку будут присвоены общие клиентские данные и данные списка глобальных пакетов, и они не будут учитываться при вычислении размера блоков. Это может быть вызвано очень большим списком пакетов, что приводит к сбоям передачи при низкой пропускной способности или ненадежных соединениях.</span><span class="sxs-lookup"><span data-stu-id="f4657-647">Each block will have the general Client data and global package list data prepended, and these will not factor into the block size calculations; the potential exists for an extremely large package list to result in transmission failures over low bandwidth or unreliable connections.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f4657-648">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f4657-648">Related topics</span></span>


[<span data-ttu-id="f4657-649">Справка по клиенту Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f4657-649">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)









