---
title: Настройка "нередактируемого" кэша в клиенте App-V (RDS)
description: Настройка "нередактируемого" кэша в клиенте App-V (RDS)
author: dansimp
ms.assetid: b6607fe2-6f92-4567-99f1-d8e3c8a591e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a44844ae9ffc3497151be7713f6a43fda0ccd8fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817949"
---
# <span data-ttu-id="bd366-103">Настройка "нередактируемого" кэша в клиенте App-V (RDS)</span><span class="sxs-lookup"><span data-stu-id="bd366-103">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>


<span data-ttu-id="bd366-104">**Важно!**  Для использования этой процедуры необходимо запустить App-V 4,6, SP1.</span><span class="sxs-lookup"><span data-stu-id="bd366-104">**Important** You must be running App-V 4.6, SP1 to use this procedure.</span></span>

 

<span data-ttu-id="bd366-105">Вы можете развернуть клиент App-V с помощью общего кэша, заполняемого всеми приложениями, необходимыми для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="bd366-105">You can deploy the App-V client by using a shared cache that is populated with all the applications required for all users.</span></span> <span data-ttu-id="bd366-106">Затем вы настраиваете клиентов служб удаленных рабочих столов App-V (RDS) для использования одного и того же файла кэша.</span><span class="sxs-lookup"><span data-stu-id="bd366-106">Then you configure the App-V Remote Desktop Services (RDS) Clients to use the same cache file.</span></span> <span data-ttu-id="bd366-107">Пользователи получают доступ к определенным приложениям с помощью процесса публикации App-V.</span><span class="sxs-lookup"><span data-stu-id="bd366-107">Users are granted access to specific applications by using the App-V publishing process.</span></span> <span data-ttu-id="bd366-108">Поскольку кэш уже предварительно загружен со всеми приложениями, потоковая передача не происходит, когда пользователь запускает приложение.</span><span class="sxs-lookup"><span data-stu-id="bd366-108">Because the cache is already preloaded with all applications, no streaming occurs when a user starts an application.</span></span> <span data-ttu-id="bd366-109">Однако пакеты, используемые для предварительного заполнения кэша, должны быть помещены на сервер App-V, поддерживающий потоковую передачу по протоколу RTSP (Real Time Streaming Protocol) и предоставляющий разрешения на доступ клиентам App-V.</span><span class="sxs-lookup"><span data-stu-id="bd366-109">However, the packages used to prepopulate the cache must be put on an App-V server that supports Real Time Streaming Protocol (RTSP) streaming and that grants access permissions to the App-V Clients.</span></span> <span data-ttu-id="bd366-110">Если вы публикуете приложения с помощью сервера управления App-V, вы можете использовать его для предоставления этой функции потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="bd366-110">If you publish the applications by using an App-V Management Server, you can use it to provide this streaming function.</span></span>

<span data-ttu-id="bd366-111">**Примечание**  Сведения, описанные в этих процедурах, предназначены только для примера.</span><span class="sxs-lookup"><span data-stu-id="bd366-111">**Note** The details outlined in these procedures are intended as examples only.</span></span> <span data-ttu-id="bd366-112">Вы можете использовать различные методы для выполнения всего процесса.</span><span class="sxs-lookup"><span data-stu-id="bd366-112">You might use different methods to complete the overall process.</span></span>

 

## <span data-ttu-id="bd366-113">Развертывание клиента App-V в сценарии RDS</span><span class="sxs-lookup"><span data-stu-id="bd366-113">Deploying the App-V Client in an RDS Scenario</span></span>


<span data-ttu-id="bd366-114">Процесс развертывания состоит из четырех основных задач:</span><span class="sxs-lookup"><span data-stu-id="bd366-114">The deployment process consists of four primary tasks:</span></span>

-   <span data-ttu-id="bd366-115">Создание и заполнение основного файла общего кэша</span><span class="sxs-lookup"><span data-stu-id="bd366-115">Creating and populating the master shared cache file</span></span>

-   <span data-ttu-id="bd366-116">Копирование файла общего кэша на серверное хранилище</span><span class="sxs-lookup"><span data-stu-id="bd366-116">Copying the shared cache file to the server storage</span></span>

-   <span data-ttu-id="bd366-117">Настройка клиентского программного обеспечения App-V</span><span class="sxs-lookup"><span data-stu-id="bd366-117">Configuring the App-V client software</span></span>

-   <span data-ttu-id="bd366-118">Управление циклом развертывания обновления для файла общего кэша после первоначального развертывания</span><span class="sxs-lookup"><span data-stu-id="bd366-118">Managing the update deployment cycle for the shared cache file after the initial deployment</span></span>

<span data-ttu-id="bd366-119">Эти задачи требуют тщательного планирования.</span><span class="sxs-lookup"><span data-stu-id="bd366-119">These tasks require careful planning.</span></span> <span data-ttu-id="bd366-120">Мы рекомендуем вам подготовить и документировать methodical, воспроизводимый процесс, который будет подписаться в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="bd366-120">We recommend that you prepare and document a methodical, reproducible process for your organization to follow.</span></span> <span data-ttu-id="bd366-121">Это особенно важно для подготовки и развертывания файла основного общего кэша и для текущего управления обновлениями приложения, для каждого из которых требуется обновление основного общего кэша.</span><span class="sxs-lookup"><span data-stu-id="bd366-121">This is especially important for the preparation and deployment of the master shared cache file, and for the ongoing management of application updates, each of which require an update to the master shared cache.</span></span> <span data-ttu-id="bd366-122">Чтобы выполнить эти основные задачи, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="bd366-122">Use the following procedures to complete these primary tasks.</span></span>

<span data-ttu-id="bd366-123">**Примечание**  Несмотря на то, что вы можете опубликовать приложения с помощью нескольких различных методов, описанные ниже действия основаны на использовании сервера управления App-V для публикации.</span><span class="sxs-lookup"><span data-stu-id="bd366-123">**Note** Although you can publish the applications by using several different methods, the following procedures are based on your using an App-V Management Server for publishing.</span></span>

 

**<span data-ttu-id="bd366-124">Настройка кэша только для чтения для первоначального развертывания</span><span class="sxs-lookup"><span data-stu-id="bd366-124">To configure the read-only cache for initial deployment</span></span>**

1. <span data-ttu-id="bd366-125">Установка и настройка сервера управления App-V для предоставления поддержки проверки подлинности пользователей и публикации.</span><span class="sxs-lookup"><span data-stu-id="bd366-125">Set up and configure an App-V Management Server to provide user authentication and publishing support.</span></span>

2. <span data-ttu-id="bd366-126">Заполните папку содержимого на этом сервере управления всеми пакетами приложений, необходимыми для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="bd366-126">Populate the Content folder of this Management Server with all the application packages required for all users.</span></span>

3. <span data-ttu-id="bd366-127">Настройте промежуточный компьютер, на котором установлен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="bd366-127">Set up a staging computer that has the App-V Client installed.</span></span> <span data-ttu-id="bd366-128">Войдите на промежуточный компьютер, используя учетную запись, которая имеет доступ ко всем приложениям, и вы сможете опубликовать на компьютере весь набор приложений, а затем перепотокировать приложения так, чтобы они были полностью загружены.</span><span class="sxs-lookup"><span data-stu-id="bd366-128">Log on to the staging computer by using an account that has access to all applications so that the complete set of applications are published to the computer, and then stream the applications to cache so that they are fully loaded.</span></span>

   **<span data-ttu-id="bd366-129">Важно.</span><span class="sxs-lookup"><span data-stu-id="bd366-129">Important</span></span>**  
   <span data-ttu-id="bd366-130">На промежуточном компьютере должны использоваться те же тип операционной системы и системная архитектура, что и для виртуальных машин, на которых работает клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="bd366-130">The staging computer must use the same operating system type and system architecture as those used by the VMs on which the App-V Client will run.</span></span>

     

4. <span data-ttu-id="bd366-131">Перезапустите промежуточный компьютер в безопасном режиме, чтобы убедиться, что драйверы не запущены, так как при этом файл кэша будет заблокирован.</span><span class="sxs-lookup"><span data-stu-id="bd366-131">Restart the staging computer in safe mode to make sure that the drivers are not started, because this would lock the cache file.</span></span>

   **<span data-ttu-id="bd366-132">Примечание.</span><span class="sxs-lookup"><span data-stu-id="bd366-132">Note</span></span>**  
   <span data-ttu-id="bd366-133">Кроме того, вы можете остановить и отключить службу Application Virtualization, а затем перезапустить компьютер.</span><span class="sxs-lookup"><span data-stu-id="bd366-133">Or, you can stop and disable the Application Virtualization service, and then restart the computer.</span></span> <span data-ttu-id="bd366-134">После копирования файла не забудьте включить и запустить службу еще раз.</span><span class="sxs-lookup"><span data-stu-id="bd366-134">After the file is copied, remember to enable and start the service again.</span></span>

     

5. <span data-ttu-id="bd366-135">Скопируйте файл кэша Sftfs. FSD в сеть хранения данных, в которой все серверы RDS смогут получать к ним доступ, например в общую папку.</span><span class="sxs-lookup"><span data-stu-id="bd366-135">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="bd366-136">Настройте разрешения на доступ к папке "только для чтения" для групп "все" и "полный доступ" для администраторов, которые будут управлять обновлением файлов в кэше.</span><span class="sxs-lookup"><span data-stu-id="bd366-136">Set the folder access permissions to Read-only for the group Everyone and to Full Control for administrators who will manage the cache file updates.</span></span> <span data-ttu-id="bd366-137">Расположение файла кэша можно получить в реестре AppFS\\FileName.</span><span class="sxs-lookup"><span data-stu-id="bd366-137">The location of the cache file can be obtained from the registry AppFS\\FileName.</span></span>

   **<span data-ttu-id="bd366-138">Важно.</span><span class="sxs-lookup"><span data-stu-id="bd366-138">Important</span></span>**  
   <span data-ttu-id="bd366-139">Файл FSD необходимо разместить в том месте, где есть скорость отклика и надежность, равная локально подключенному хранилищу, например SAN.</span><span class="sxs-lookup"><span data-stu-id="bd366-139">You must put the FSD file in a location that has the responsiveness and reliability equal to locally attached storage performance, for example, a SAN.</span></span>

     

6. <span data-ttu-id="bd366-140">Установите клиентскую RDS App-V на каждом сервере RDS и настройте его на использование кэша только для чтения, добавив следующие значения раздела реестра в раздел AppFS на клиенте.</span><span class="sxs-lookup"><span data-stu-id="bd366-140">Install the App-V RDS Client on each RDS server, and then configure it to use the read-only cache by adding the following registry key values to the AppFS key on the client.</span></span> <span data-ttu-id="bd366-141">Клавиша AppFS расположена на странице HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS для 32-разрядных компьютеров и на странице HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS для 64-разрядных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="bd366-141">The AppFS key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\]Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 32-bit computers and at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 64-bit computers.</span></span>

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="bd366-142">Ключ</span><span class="sxs-lookup"><span data-stu-id="bd366-142">Key</span></span></th>
   <th align="left"><span data-ttu-id="bd366-143">Тип</span><span class="sxs-lookup"><span data-stu-id="bd366-143">Type</span></span></th>
   <th align="left"><span data-ttu-id="bd366-144">Значение</span><span class="sxs-lookup"><span data-stu-id="bd366-144">Value</span></span></th>
   <th align="left"><span data-ttu-id="bd366-145">Описание</span><span class="sxs-lookup"><span data-stu-id="bd366-145">Purpose</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="bd366-146">FileName</span><span class="sxs-lookup"><span data-stu-id="bd366-146">FileName</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd366-147">Строка</span><span class="sxs-lookup"><span data-stu-id="bd366-147">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd366-148">путь к FSD</span><span class="sxs-lookup"><span data-stu-id="bd366-148">path of FSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd366-149">Задает путь к файлу общего кэша (например, \RDSServername\Sharefolder\SFTFS.). FSD (обязательный аргумент).</span><span class="sxs-lookup"><span data-stu-id="bd366-149">Specifies the path of the shared cache file, for example, \RDSServername\Sharefolder\SFTFS.FSD (Required).</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="bd366-150">ReadOnlyFSD</span><span class="sxs-lookup"><span data-stu-id="bd366-150">ReadOnlyFSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd366-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd366-151">DWORD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd366-152">1,1</span><span class="sxs-lookup"><span data-stu-id="bd366-152">1</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd366-153">Настраивает Клиент для работы в режиме "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="bd366-153">Configures the client to operate in Read-Only mode.</span></span> <span data-ttu-id="bd366-154">Это гарантирует, что клиент не попытается попытаться перенаправит обновления в кэш пакетов.</span><span class="sxs-lookup"><span data-stu-id="bd366-154">This ensures that the client will not try to stream updates to the package cache.</span></span> <span data-ttu-id="bd366-155">(Обязательно)</span><span class="sxs-lookup"><span data-stu-id="bd366-155">(Required)</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="bd366-156">ErrorLogLocation</span><span class="sxs-lookup"><span data-stu-id="bd366-156">ErrorLogLocation</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd366-157">Строка</span><span class="sxs-lookup"><span data-stu-id="bd366-157">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd366-158">путь к файлу журнала ошибок (ETL-файла)</span><span class="sxs-lookup"><span data-stu-id="bd366-158">path of error log (.etl) file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd366-159">Элемент, с помощью которого можно указать путь к журналу ошибок.</span><span class="sxs-lookup"><span data-stu-id="bd366-159">Entry used to specify the path of the error log.</span></span> <span data-ttu-id="bd366-160">Рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="bd366-160">(Recommended.</span></span> <span data-ttu-id="bd366-161">Используйте локальный путь (например, C:\Logs\Sftfs.etl).</span><span class="sxs-lookup"><span data-stu-id="bd366-161">Use a local path such as C:\Logs\Sftfs.etl).</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="bd366-162">Настройте каждый сервер RDS в ферме на использование сервера публикации и используйте обновление публикации при входе пользователей.</span><span class="sxs-lookup"><span data-stu-id="bd366-162">Configure each RDS server in the farm to use the publishing server and to use publishing update when users log on.</span></span> <span data-ttu-id="bd366-163">Когда пользователи входят на серверы RDS, происходит цикл обновления публикации и публикуются все приложения, для которых их учетная запись авторизована.</span><span class="sxs-lookup"><span data-stu-id="bd366-163">As users log on to the RDS servers, a publishing update cycle occurs and publishes all the applications for which their account is authorized.</span></span> <span data-ttu-id="bd366-164">Эти приложения выполняются из общего кэша.</span><span class="sxs-lookup"><span data-stu-id="bd366-164">These applications are run from the shared cache.</span></span>

**<span data-ttu-id="bd366-165">Настройка клиента RDS для обновления пакета</span><span class="sxs-lookup"><span data-stu-id="bd366-165">To configure the RDS client for package upgrade</span></span>**

1.  <span data-ttu-id="bd366-166">Завершите обновление и тестирование пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="bd366-166">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="bd366-167">Обновите пакет на сервере App-V.</span><span class="sxs-lookup"><span data-stu-id="bd366-167">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="bd366-168">Затем опубликуйте и поработайте в потоке новую версию приложения с клиентом на промежуточном компьютере, чтобы они были полностью загружены в кэш.</span><span class="sxs-lookup"><span data-stu-id="bd366-168">Then, publish and stream the new version of the applications to the client on the staging computer so that they are fully loaded into cache.</span></span>

3.  <span data-ttu-id="bd366-169">Перезапустите промежуточный компьютер в безопасном режиме, чтобы убедиться, что драйверы не запущены.</span><span class="sxs-lookup"><span data-stu-id="bd366-169">Restart the staging computer in safe mode to ensure the drivers are not started.</span></span>

    <span data-ttu-id="bd366-170">**Примечание**  Кроме того, вы можете сначала остановить и отключить службу Application Virtualization в службах Services. msc, а затем перезапустить компьютер.</span><span class="sxs-lookup"><span data-stu-id="bd366-170">**Note** Or, you can first stop and then disable the Application Virtualization service in the Services.msc, and restart the computer.</span></span> <span data-ttu-id="bd366-171">После копирования файла не забудьте включить и запустить службу еще раз.</span><span class="sxs-lookup"><span data-stu-id="bd366-171">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="bd366-172">Скопируйте файл кэша Sftfs. FSD в сеть хранения данных, в которой все серверы RDS смогут получать к ним доступ, например в общую папку.</span><span class="sxs-lookup"><span data-stu-id="bd366-172">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="bd366-173">Вы можете использовать другое имя файла, например SFTFS \ _V2. FSD, чтобы отличать новую версию.</span><span class="sxs-lookup"><span data-stu-id="bd366-173">You can use a different file name, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="bd366-174">Чтобы настроить клиентские RDS App-V на каждом сервере RDS в ферме для использования обновленного файла общего кэша, измените значение FILENAME для раздела реестра AppFS таким образом, чтобы оно указывало на расположение обновленного файла, например \\\\RDSServername\\Sharefolder\\SFTFS\ _V2. FSD.</span><span class="sxs-lookup"><span data-stu-id="bd366-174">To configure the App-V RDS Client on each RDS server in the farm to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\RDSServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="bd366-175">Это гарантирует, что каждый сервер RDS получает обновленную копию кэша при перезапуске драйверов App-vClient.</span><span class="sxs-lookup"><span data-stu-id="bd366-175">This guarantees that each RDS server receives the updated copy of the cache when the App-Vclient drivers restart.</span></span>

    <span data-ttu-id="bd366-176">**Важно!**  Для использования обновленного файла общего кэша необходимо перезапустить серверы RDS.</span><span class="sxs-lookup"><span data-stu-id="bd366-176">**Important** You must restart the RDS servers in order to use the updated shared cache file.</span></span>

     

## <span data-ttu-id="bd366-177">Использование символьных ссылок при обновлении кэша</span><span class="sxs-lookup"><span data-stu-id="bd366-177">How to Use Symbolic Links when Upgrading the Cache</span></span>


<span data-ttu-id="bd366-178">Вместо того, чтобы изменять значение имени файла ключа AppFS каждый раз при развертывании нового файла кэша, содержащего новые или обновленные пакеты, можно использовать символьную ссылку в следующих операционных системах: Windows Vista, Windows 7 и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="bd366-178">Instead of changing the AppFS key FILENAME value every time that a new cache file is deployed that contains new or upgraded packages, you can use a symbolic link in the following operating systems: Windows Vista, Windows 7, and Windows Server 2008.</span></span> <span data-ttu-id="bd366-179">Дополнительные сведения о символических [ссылках см](https://go.microsoft.com/fwlink/?LinkId=157626) https://go.microsoft.com/fwlink/?LinkId=157626) .</span><span class="sxs-lookup"><span data-stu-id="bd366-179">For more information about symbolic links, see [Symbolic Links](https://go.microsoft.com/fwlink/?LinkId=157626) (https://go.microsoft.com/fwlink/?LinkId=157626).</span></span> <span data-ttu-id="bd366-180">В отличие от этого, Windows XP не поддерживает использование символических ссылок, поэтому вместо них следует использовать точки соединения.</span><span class="sxs-lookup"><span data-stu-id="bd366-180">In contrast, Windows XP does not support the use of symbolic links, and you must use junction points instead.</span></span> <span data-ttu-id="bd366-181">Дополнительные сведения о соединениях можно найти в [статье 205524](https://go.microsoft.com/fwlink/?LinkId=182553) в базе знаний Майкрософт ( https://go.microsoft.com/fwlink/?LinkId=182553) а также на [1.05е](https://go.microsoft.com/fwlink/?LinkId=182554) с помощью средства v https://go.microsoft.com/fwlink/?LinkId=182554) .</span><span class="sxs-lookup"><span data-stu-id="bd366-181">For more information about junctions, see [article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=182553), and also the tool [Junction v1.05](https://go.microsoft.com/fwlink/?LinkId=182554) (https://go.microsoft.com/fwlink/?LinkId=182554).</span></span>

**<span data-ttu-id="bd366-182">Настройка символьной ссылки для ссылки на кэш</span><span class="sxs-lookup"><span data-stu-id="bd366-182">To configure a symbolic link to reference the cache</span></span>**

1.  <span data-ttu-id="bd366-183">На начальном этапе развертывания откройте окно командной строки в качестве локального администратора в операционной системе узла RDS-сервера.</span><span class="sxs-lookup"><span data-stu-id="bd366-183">During the initial deployment stage, open a Command Prompt window as a local administrator on the RDS server host operating system.</span></span>

2.  <span data-ttu-id="bd366-184">Создайте символьную ссылку с помощью команды MKLINK и настройте ее так, чтобы она указывала на файл Sftfs. fsd.</span><span class="sxs-lookup"><span data-stu-id="bd366-184">Create a symbolic link by using the MKLINK command, and then configure it to point to the Sftfs.fsd file.</span></span>

    **     <span data-ttu-id="bd366-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="bd366-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd</span></span>**

3.  <span data-ttu-id="bd366-186">В образе эталонной виртуальной машины VDI откройте окно командной строки с помощью команды " **Запуск от имени администратора** " и предоставьте разрешения удаленной ссылки таким образом, чтобы виртуальная машина могла получить доступ к символической ссылке в операционной системе сервера VDI.</span><span class="sxs-lookup"><span data-stu-id="bd366-186">On the VDI Master VM Image, open a Command Prompt window by using the **Run as administrator** option and grant remote link permissions so that the VM can access the symbolic link on the VDI Host operating system.</span></span> <span data-ttu-id="bd366-187">По умолчанию разрешения для удаленной ссылки отключены.</span><span class="sxs-lookup"><span data-stu-id="bd366-187">By default, remote link permissions are disabled.</span></span>

    **<span data-ttu-id="bd366-188">fsutil behavior Set SymlinkEvaluation R2R: 1</span><span class="sxs-lookup"><span data-stu-id="bd366-188">fsutil behavior set SymlinkEvaluation R2R:1</span></span>**

    <span data-ttu-id="bd366-189">**Примечание**  На сервере хранилища должны быть включены соответствующие разрешения на ссылки.</span><span class="sxs-lookup"><span data-stu-id="bd366-189">**Note** On the storage server, appropriate link permissions must be enabled.</span></span> <span data-ttu-id="bd366-190">В зависимости от расположения ссылки и файла Sftfs. FSD разрешениями являются **L2L: 1** или **L2R: 1** или **r2l:** **1 или**.</span><span class="sxs-lookup"><span data-stu-id="bd366-190">Depending on the location of link and the Sftfs.fsd file, the permissions are **L2L:1** or **L2R:1** or **R2L:1** or **R2R:1**.</span></span>

     

4.  <span data-ttu-id="bd366-191">При настройке клиента App-V RDS задайте значение FILENAME для AppFS Key, равное UNC-пути к файлу FSD, использующему символьную ссылку.</span><span class="sxs-lookup"><span data-stu-id="bd366-191">When you configure the App-V RDS Client, set the AppFS key FILENAME value equal to the UNC path of the FSD file that is using the symbolic link.</span></span> <span data-ttu-id="bd366-192">Например, задайте для имени файла \\\\VDIHostserver\\Symlinkname.</span><span class="sxs-lookup"><span data-stu-id="bd366-192">For example, set the file name to \\\\VDIHostserver\\Symlinkname.</span></span> <span data-ttu-id="bd366-193">Когда клиент App-V сначала пытается получить доступ к кэшу, символическая ссылка передает клиенту дескриптор файлу кэша.</span><span class="sxs-lookup"><span data-stu-id="bd366-193">When the App-V client first accesses the cache, the symbolic link passes to the client a handle to the cache file.</span></span> <span data-ttu-id="bd366-194">Клиент продолжает использовать этот дескриптор, пока клиент запущен.</span><span class="sxs-lookup"><span data-stu-id="bd366-194">The client continues to use that handle as long as the client is running.</span></span> <span data-ttu-id="bd366-195">Значение символьной ссылки может безопасно обновляться даже в том случае, если для существующих клиентов открыт старый общий кэш.</span><span class="sxs-lookup"><span data-stu-id="bd366-195">The value of the symbolic link can safely be updated even if existing clients have the old shared cache open.</span></span>

5.  <span data-ttu-id="bd366-196">Если необходимо обновить пакет или добавить новый пакет в кэш, выполните действия 1 – 4 процедуры обновления.</span><span class="sxs-lookup"><span data-stu-id="bd366-196">When you must upgrade a package or to add a new package to the cache, follow steps 1 through 4 of the upgrade procedure.</span></span> <span data-ttu-id="bd366-197">Затем удалите символьную ссылку и повторно создайте ее, чтобы она указывала на новую версию общего файла кэша.</span><span class="sxs-lookup"><span data-stu-id="bd366-197">Then, delete the symbolic link and re-create it to point to the new version of the shared cache file.</span></span> <span data-ttu-id="bd366-198">Это гарантирует, что каждый сервер RDS будет получать обновленную копию кэша при перезапуске клиентских драйверов App-V.</span><span class="sxs-lookup"><span data-stu-id="bd366-198">This guarantees that each RDS server receives the updated copy of the cache when the App-V client drivers restart.</span></span> <span data-ttu-id="bd366-199">После перезапуска сервера RDS клиент App-V получает дескриптор обновленной копии кэша, так как клиент использует путь, который содержит обновленную символьную ссылку.</span><span class="sxs-lookup"><span data-stu-id="bd366-199">When the RDS server is restarted, the App-V client receives a handle to the updated copy of the cache because the client uses the path that contains the updated symbolic link.</span></span> <span data-ttu-id="bd366-200">Затем пользователи смогут получить доступ к новым и обновленным приложениям.</span><span class="sxs-lookup"><span data-stu-id="bd366-200">Then, the users have access to the new and updated applications.</span></span>

## <span data-ttu-id="bd366-201">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="bd366-201">Related topics</span></span>


[<span data-ttu-id="bd366-202">Установка сервера Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="bd366-202">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

[<span data-ttu-id="bd366-203">Установка клиента Application Virtualization Client вручную</span><span class="sxs-lookup"><span data-stu-id="bd366-203">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="bd366-204">Установка клиента с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="bd366-204">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





