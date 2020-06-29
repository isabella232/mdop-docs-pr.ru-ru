---
title: Настройка "нередактируемого" кэша в клиенте App-V (VDI)
description: Настройка "нередактируемого" кэша в клиенте App-V (VDI)
author: dansimp
ms.assetid: 7a41e017-9e23-4a6a-a659-04d23f008b83
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 114f9dfbf55a3f62b6bc8bec6b37a659ffbfaf56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817942"
---
# <span data-ttu-id="5bf01-103">Настройка "нередактируемого" кэша в клиенте App-V (VDI)</span><span class="sxs-lookup"><span data-stu-id="5bf01-103">How to Configure a Read-only Cache on the App-V Client (VDI)</span></span>


<span data-ttu-id="5bf01-104">В Microsoft Application Virtualization (App-V) 4,6 клиент поддерживает использование общего кэша, доступного только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5bf01-104">In Microsoft Application Virtualization (App-V) 4.6 the Client supports using a shared read-only cache.</span></span> <span data-ttu-id="5bf01-105">Общий доступ только для чтения позволяет клиенту эффективно использовать дисковое пространство в системе инфраструктуры виртуальных рабочих столов (VDI), где пользователи выполняют приложения на виртуальных машинах (ВМ), которые размещаются в среде центра обработки данных и совместно используют сетевое хранилище в сети SAN.</span><span class="sxs-lookup"><span data-stu-id="5bf01-105">The shared read-only cache enables the Client to use disk space efficiently in a Virtual Desktop Infrastructure (VDI) system, where users run applications on Virtual Machines (VM) that are hosted in a data center server environment and share network storage on a Storage Area Network (SAN).</span></span> <span data-ttu-id="5bf01-106">Ниже описаны действия, которые необходимо выполнить для реализации клиента App-V в одной из основных архитектур VDI, называемой "poold VM" или "static VM".</span><span class="sxs-lookup"><span data-stu-id="5bf01-106">The following procedures provide an overview of the process that is required to implement the App-V Client in either of the primary VDI architectures, known as “Pooled VM” or “Static VM”.</span></span> <span data-ttu-id="5bf01-107">Предполагается, что вы знакомы с планированием, развертыванием и эксплуатацией системы App-V и ее компонентов, а также работой и управлением сервером VDI.</span><span class="sxs-lookup"><span data-stu-id="5bf01-107">It is assumed that you are familiar with the planning, deployment, and operation of the App-V system and its components, and also the operation and management of the VDI server.</span></span> <span data-ttu-id="5bf01-108">Дополнительные сведения о приложении App-V можно найти в разделе [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939)</span><span class="sxs-lookup"><span data-stu-id="5bf01-108">For more information about App-V, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939)</span></span>

<span data-ttu-id="5bf01-109">**Примечание**  Сведения, описанные в этих процедурах, предназначены только для примера.</span><span class="sxs-lookup"><span data-stu-id="5bf01-109">**Note** The details outlined in these procedures are intended as examples only.</span></span> <span data-ttu-id="5bf01-110">Вы можете использовать различные методы для выполнения всего процесса.</span><span class="sxs-lookup"><span data-stu-id="5bf01-110">You might use different methods to complete the overall process.</span></span>

 

## <span data-ttu-id="5bf01-111">Развертывание клиента App-V в сценарии VDI</span><span class="sxs-lookup"><span data-stu-id="5bf01-111">Deploying the App-V Client in a VDI Scenario</span></span>


<span data-ttu-id="5bf01-112">Вы можете развернуть клиент App-V в сценарии VDI с помощью общего кэша, доступного только для чтения, который заполнен всеми необходимыми приложениями для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="5bf01-112">You can deploy the App-V Client in a VDI scenario by using a shared read-only cache that has been populated with all the applications required for all users.</span></span> <span data-ttu-id="5bf01-113">Затем настройте основной образ виртуальной машины VDI таким образом, чтобы все клиенты App-V использовали один и тот же кэш-файл.</span><span class="sxs-lookup"><span data-stu-id="5bf01-113">You then configure the VDI Master VM Image so that all the App-V Clients use the same cache file.</span></span> <span data-ttu-id="5bf01-114">Пользователи получают доступ к определенным приложениям с помощью процесса публикации App-V.</span><span class="sxs-lookup"><span data-stu-id="5bf01-114">Users are granted access to specific applications by using the App-V publishing process.</span></span> <span data-ttu-id="5bf01-115">Поскольку кэш уже предварительно загружен со всеми приложениями, потоковая передача не происходит, когда пользователь запускает приложение.</span><span class="sxs-lookup"><span data-stu-id="5bf01-115">Since the cache is already preloaded with all applications, no streaming occurs when a user starts an application.</span></span> <span data-ttu-id="5bf01-116">Однако пакеты, используемые для предварительного заполнения кэша, должны быть помещены на сервер App-V, поддерживающий потоковую передачу по протоколу RTSP (Real Time Streaming Protocol) и предоставляющий разрешения на доступ клиентам App-V.</span><span class="sxs-lookup"><span data-stu-id="5bf01-116">However, the packages used to prepopulate the cache must be put on an App-V server that supports Real Time Streaming Protocol (RTSP) streaming and that grants access permissions to the App-V Clients.</span></span> <span data-ttu-id="5bf01-117">Если вы публикуете приложения с помощью сервера управления App-V, вы можете использовать его для предоставления этой функции потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="5bf01-117">If you publish the applications by using an App-V Management Server, you can use it to provide this streaming function.</span></span>

<span data-ttu-id="5bf01-118">Процесс развертывания состоит из четырех основных задач:</span><span class="sxs-lookup"><span data-stu-id="5bf01-118">The deployment process consists of four primary tasks:</span></span>

-   <span data-ttu-id="5bf01-119">Создание и заполнение основного файла общего кэша</span><span class="sxs-lookup"><span data-stu-id="5bf01-119">Creating and populating the master shared cache file</span></span>

-   <span data-ttu-id="5bf01-120">Копирование файла общего кэша в хранилище сервера VDI</span><span class="sxs-lookup"><span data-stu-id="5bf01-120">Copying the shared cache file to the VDI server storage</span></span>

-   <span data-ttu-id="5bf01-121">Настройка клиентского программного обеспечения App-V на эталонном образе VDI</span><span class="sxs-lookup"><span data-stu-id="5bf01-121">Configuring the App-V client software on the VDI Master Image</span></span>

-   <span data-ttu-id="5bf01-122">Управление циклом развертывания обновления для файла общего кэша после первоначального развертывания</span><span class="sxs-lookup"><span data-stu-id="5bf01-122">Managing the update deployment cycle for the shared cache file after the initial deployment</span></span>

<span data-ttu-id="5bf01-123">Эти задачи требуют тщательного планирования.</span><span class="sxs-lookup"><span data-stu-id="5bf01-123">These tasks require careful planning.</span></span> <span data-ttu-id="5bf01-124">Мы рекомендуем вам подготовить и документировать methodical, воспроизводимый процесс, который будет подписаться в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="5bf01-124">We recommend that you prepare and document a methodical, reproducible process for your organization to follow.</span></span> <span data-ttu-id="5bf01-125">Это особенно важно для первоначальной подготовки и развертывания файла основного общего кэша, а также для управления обновлениями приложения, для каждого из которых требуется обновление основного общего кэша.</span><span class="sxs-lookup"><span data-stu-id="5bf01-125">This is especially important for the initial preparation and deployment of the master shared cache file, and for the on-going management of application updates, each of which require an update to the master shared cache.</span></span> <span data-ttu-id="5bf01-126">Чтобы выполнить эти основные задачи, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5bf01-126">Use the following procedures to complete these primary tasks.</span></span>

<span data-ttu-id="5bf01-127">**Примечание**  Несмотря на то, что вы можете публиковать приложения несколькими различными способами, описанные ниже процедуры основываются на использовании сервера управления App-V для публикации.</span><span class="sxs-lookup"><span data-stu-id="5bf01-127">**Note** Although you can publish the applications by using several different methods, the following procedures are based on the use of an App-V Management Server for publishing.</span></span>

 

**<span data-ttu-id="5bf01-128">Настройка кэша только для чтения для первоначального развертывания в сценарии объединения виртуальной машины в составе пула или статической виртуальной машины в VDI</span><span class="sxs-lookup"><span data-stu-id="5bf01-128">To configure the read-only cache for initial deployment in a Pooled VM VDI or Static VM VDI scenario</span></span>**

1. <span data-ttu-id="5bf01-129">Установка и настройка сервера управления App-V в виртуальной машине на сервере VDI для предоставления поддержки проверки подлинности пользователей и публикации.</span><span class="sxs-lookup"><span data-stu-id="5bf01-129">Set up and configure an App-V Management Server in a VM on the VDI server to provide user authentication and publishing support.</span></span>

2. <span data-ttu-id="5bf01-130">Заполните папку содержимого на этом сервере управления всеми пакетами приложений, необходимыми для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="5bf01-130">Populate the Content folder of this Management Server with all the application packages required for all users.</span></span>

3. <span data-ttu-id="5bf01-131">Настройте промежуточный компьютер, на котором установлен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="5bf01-131">Set up a staging computer that has the App-V Client installed.</span></span> <span data-ttu-id="5bf01-132">Войдите на промежуточный компьютер с учетной записью, у которой есть доступ ко всем приложениям, чтобы на компьютере были опубликованы все необходимые приложения, а затем перезапустите кэширование приложений, чтобы они были полностью загружены.</span><span class="sxs-lookup"><span data-stu-id="5bf01-132">Log on to the staging computer with an account that has access to all applications so that the complete set of applications are published to the computer, and then stream the applications to cache so that they are fully loaded.</span></span>

   **<span data-ttu-id="5bf01-133">Важно.</span><span class="sxs-lookup"><span data-stu-id="5bf01-133">Important</span></span>**  
   <span data-ttu-id="5bf01-134">На промежуточном компьютере должны использоваться те же тип операционной системы и системная архитектура, что и для виртуальных машин, на которых работает клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="5bf01-134">The staging computer must use the same operating system type and system architecture as those used by the VMs on which the App-V Client will run.</span></span>

     

4. <span data-ttu-id="5bf01-135">Перезапустите промежуточный компьютер в безопасном режиме, чтобы убедиться, что драйверы не запущены, и файл кэша блокируется.</span><span class="sxs-lookup"><span data-stu-id="5bf01-135">Restart the staging computer in Safe Mode to ensure the drivers are not started, which would lock the cache file.</span></span>

   **<span data-ttu-id="5bf01-136">Примечание.</span><span class="sxs-lookup"><span data-stu-id="5bf01-136">Note</span></span>**  
   <span data-ttu-id="5bf01-137">Кроме того, вы можете остановить и отключить службу Application Virtualization, а затем перезапустить компьютер.</span><span class="sxs-lookup"><span data-stu-id="5bf01-137">Alternatively, you can stop and disable the Application Virtualization service, and then restart the computer.</span></span> <span data-ttu-id="5bf01-138">После копирования файла не забудьте включить и запустить службу еще раз.</span><span class="sxs-lookup"><span data-stu-id="5bf01-138">After the file has been copied, remember to enable and start the service again.</span></span>

     

5. <span data-ttu-id="5bf01-139">Скопируйте файл кэша Sftfs. FSD в сеть хранения данных сервера VDI, в которой все виртуальные компьютеры смогут получать к ним доступ, например в общую папку.</span><span class="sxs-lookup"><span data-stu-id="5bf01-139">Copy the Sftfs.fsd cache file to the VDI server’s SAN where all the VMs can access it, such as in a shared folder.</span></span> <span data-ttu-id="5bf01-140">Настройте разрешения на доступ к папке "только для чтения" для групп "все" и "полный доступ" для администраторов, которые будут управлять обновлением файлов в кэше.</span><span class="sxs-lookup"><span data-stu-id="5bf01-140">Set the folder access permissions to Read-only for the group Everyone and to Full Control for administrators who will manage the cache file updates.</span></span> <span data-ttu-id="5bf01-141">Расположение файла кэша можно получить в реестре AppFS\\FileName.</span><span class="sxs-lookup"><span data-stu-id="5bf01-141">The location of the cache file can be obtained from the registry AppFS\\FileName.</span></span>

   **<span data-ttu-id="5bf01-142">Важно.</span><span class="sxs-lookup"><span data-stu-id="5bf01-142">Important</span></span>**  
   <span data-ttu-id="5bf01-143">Файл FSD необходимо разместить в том месте, где есть скорость ответа и надежность, эквивалентные локальному подключению хранилища (например, сети SAN).</span><span class="sxs-lookup"><span data-stu-id="5bf01-143">You must put the FSD file in a location that has the responsiveness and reliability equivalent to locally attached storage performance, for example, a SAN.</span></span>

     

6. <span data-ttu-id="5bf01-144">Установите классическое приложение App-V на основной образ виртуальной машины VDI и настройте его на использование кэша только для чтения, добавив следующие значения раздела реестра в раздел AppFS на клиенте.</span><span class="sxs-lookup"><span data-stu-id="5bf01-144">Install the App-V Desktop Client on the VDI Master VM Image, and then configure it to use the read-only cache by adding the following registry key values to the AppFS key on the client.</span></span> <span data-ttu-id="5bf01-145">Клавиша AppFS находится в разделе HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS.</span><span class="sxs-lookup"><span data-stu-id="5bf01-145">The AppFS key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\[Wow6432Node\\\]Microsoft\\SoftGrid\\4.5\\Client\\AppFS.</span></span>

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5bf01-146">Ключ</span><span class="sxs-lookup"><span data-stu-id="5bf01-146">Key</span></span></th>
   <th align="left"><span data-ttu-id="5bf01-147">Тип</span><span class="sxs-lookup"><span data-stu-id="5bf01-147">Type</span></span></th>
   <th align="left"><span data-ttu-id="5bf01-148">Значение</span><span class="sxs-lookup"><span data-stu-id="5bf01-148">Value</span></span></th>
   <th align="left"><span data-ttu-id="5bf01-149">Описание</span><span class="sxs-lookup"><span data-stu-id="5bf01-149">Purpose</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5bf01-150">FileName</span><span class="sxs-lookup"><span data-stu-id="5bf01-150">FileName</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5bf01-151">Строка</span><span class="sxs-lookup"><span data-stu-id="5bf01-151">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5bf01-152">путь к FSD</span><span class="sxs-lookup"><span data-stu-id="5bf01-152">path to FSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5bf01-153">Задает путь к файлу общего кэша (например, \VDIServername\Sharefolder\SFTFS.). FSD (обязательный аргумент).</span><span class="sxs-lookup"><span data-stu-id="5bf01-153">Specifies the path to the shared cache file, for example, \VDIServername\Sharefolder\SFTFS.FSD (Required).</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5bf01-154">ReadOnlyFSD</span><span class="sxs-lookup"><span data-stu-id="5bf01-154">ReadOnlyFSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5bf01-155">DWORD</span><span class="sxs-lookup"><span data-stu-id="5bf01-155">DWORD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5bf01-156">1,1</span><span class="sxs-lookup"><span data-stu-id="5bf01-156">1</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5bf01-157">Настраивает Клиент для работы в режиме "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="5bf01-157">Configures the client to operate in Read-Only mode.</span></span> <span data-ttu-id="5bf01-158">Это гарантирует, что клиент не попытается попытаться передать обновления в кэш пакетов.</span><span class="sxs-lookup"><span data-stu-id="5bf01-158">This ensures that the client will not attempt to stream updates to the package cache.</span></span> <span data-ttu-id="5bf01-159">(Обязательно)</span><span class="sxs-lookup"><span data-stu-id="5bf01-159">(Required)</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5bf01-160">ErrorLogLocation</span><span class="sxs-lookup"><span data-stu-id="5bf01-160">ErrorLogLocation</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5bf01-161">Строка</span><span class="sxs-lookup"><span data-stu-id="5bf01-161">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5bf01-162">путь к файлу журнала ошибок (ETL)</span><span class="sxs-lookup"><span data-stu-id="5bf01-162">path to error log (.etl) file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5bf01-163">Элемент, с помощью которого можно указать путь к журналу ошибок.</span><span class="sxs-lookup"><span data-stu-id="5bf01-163">Entry used to specify the path to the error log.</span></span> <span data-ttu-id="5bf01-164">Рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5bf01-164">(Recommended.</span></span> <span data-ttu-id="5bf01-165">Используйте локальный путь (например, C:\Logs\Sftfs.etl).</span><span class="sxs-lookup"><span data-stu-id="5bf01-165">Use a local path such as C:\Logs\Sftfs.etl).</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="5bf01-166">Настройте основной клиент образов виртуальных машин на использование сервера публикации и используйте обновление публикации при входе.</span><span class="sxs-lookup"><span data-stu-id="5bf01-166">Configure the Master VM Image client to use the publishing server and to use publishing refresh at logon.</span></span> <span data-ttu-id="5bf01-167">Когда пользователи входят в систему VDI и их виртуальные машины строятся на основе главного образа виртуальной машины, происходит цикл обновления публикации и публикуются все приложения, для которых их учетная запись авторизована.</span><span class="sxs-lookup"><span data-stu-id="5bf01-167">As users log on to the VDI system and their VM is built from the Master VM Image, a publishing refresh cycle occurs and publishes all the applications for which their account is authorized.</span></span> <span data-ttu-id="5bf01-168">Эти приложения выполняются из общего кэша.</span><span class="sxs-lookup"><span data-stu-id="5bf01-168">These applications are run from the shared cache.</span></span>

**<span data-ttu-id="5bf01-169">Настройка клиента для обновления пакета в сценарии для виртуальной машины из пула</span><span class="sxs-lookup"><span data-stu-id="5bf01-169">To configure the client for package upgrade in a Pooled VM scenario</span></span>**

1.  <span data-ttu-id="5bf01-170">Завершите обновление и тестирование пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="5bf01-170">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="5bf01-171">Обновите пакет на сервере App-V.</span><span class="sxs-lookup"><span data-stu-id="5bf01-171">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="5bf01-172">Затем опубликуйте и поработайте в потоке новую версию приложения с клиентом на промежуточном компьютере, чтобы они были полностью загружены в кэш.</span><span class="sxs-lookup"><span data-stu-id="5bf01-172">Then, publish and stream the new version of the applications to the client on the staging computer so that they are fully loaded into cache.</span></span>

3.  <span data-ttu-id="5bf01-173">Перезапустите промежуточный компьютер в безопасном режиме, чтобы убедиться, что драйверы не запущены.</span><span class="sxs-lookup"><span data-stu-id="5bf01-173">Restart the staging computer in Safe Mode to ensure the drivers are not started.</span></span>

    <span data-ttu-id="5bf01-174">**Примечание**  Кроме того, вы можете остановить и отключить службу Application Virtualization в службах Services. msc, а затем перезапустить компьютер.</span><span class="sxs-lookup"><span data-stu-id="5bf01-174">**Note** Alternatively, you can stop and disable the Application Virtualization service in the Services.msc, and then restart the computer.</span></span> <span data-ttu-id="5bf01-175">После копирования файла не забудьте включить и запустить службу еще раз.</span><span class="sxs-lookup"><span data-stu-id="5bf01-175">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="5bf01-176">Скопируйте файл кэша Sftfs. FSD в сеть хранения данных сервера VDI, в которой все виртуальные компьютеры смогут получать к ним доступ, например в общую папку.</span><span class="sxs-lookup"><span data-stu-id="5bf01-176">Copy the Sftfs.fsd cache file to the VDI server’s SAN where all the VMs can access it, such as in a shared folder.</span></span> <span data-ttu-id="5bf01-177">Вы можете использовать другое имя файла, например SFTFS \ _V2. FSD, чтобы отличать новую версию.</span><span class="sxs-lookup"><span data-stu-id="5bf01-177">You can use a different filename, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="5bf01-178">Чтобы настроить клиент App-V для настольных компьютеров на образе виртуальной машины VDI для использования обновленного файла общего кэша, измените значение FILENAME для раздела реестра AppFS таким образом, чтобы он указывал на расположение обновленного файла, например \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD.</span><span class="sxs-lookup"><span data-stu-id="5bf01-178">To configure the App-V Desktop Client on the VDI Master VM Image to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\VDIServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="5bf01-179">Когда пользователь выходит из системы и снова входит в систему, для них создается новая виртуальная машина с помощью обновленного основного образа.</span><span class="sxs-lookup"><span data-stu-id="5bf01-179">When users log off and then log on again, a new VM is created for them by using the updated Master Image.</span></span> <span data-ttu-id="5bf01-180">Все параметры пользователя будут сохранены и применены к новой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5bf01-180">All their user settings will be retained and applied to the new VM.</span></span> <span data-ttu-id="5bf01-181">У них есть доступ к обновленным приложениям.</span><span class="sxs-lookup"><span data-stu-id="5bf01-181">Then they have access to the updated applications.</span></span>

**<span data-ttu-id="5bf01-182">Настройка клиента для обновления пакета в сценарии статической виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5bf01-182">To configure the client for package upgrade in a Static VM scenario</span></span>**

1.  <span data-ttu-id="5bf01-183">Завершите обновление и тестирование пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="5bf01-183">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="5bf01-184">Обновите пакет на сервере App-V.</span><span class="sxs-lookup"><span data-stu-id="5bf01-184">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="5bf01-185">Затем опубликуйте и поработайте в потоке новую версию приложения на тестовом компьютере, чтобы приложения были полностью загружены в кэш.</span><span class="sxs-lookup"><span data-stu-id="5bf01-185">Then, publish and stream the new version of the applications to the client on the staging computer so that the applications are fully loaded into cache.</span></span>

3.  <span data-ttu-id="5bf01-186">Перезапустите промежуточный компьютер в безопасном режиме, чтобы убедиться, что драйверы не запущены.</span><span class="sxs-lookup"><span data-stu-id="5bf01-186">Restart the staging computer in Safe Mode to ensure that the drivers are not started.</span></span>

    <span data-ttu-id="5bf01-187">**Примечание**  Кроме того, вы можете остановить и отключить службу Application Virtualization в службах Services. msc, а затем перезапустить компьютер.</span><span class="sxs-lookup"><span data-stu-id="5bf01-187">**Note** Alternatively, you can stop and disable the Application Virtualization service in the Services.msc, and then restart the computer.</span></span> <span data-ttu-id="5bf01-188">После копирования файла не забудьте включить и запустить службу еще раз.</span><span class="sxs-lookup"><span data-stu-id="5bf01-188">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="5bf01-189">Скопируйте файл кэша Sftfs. FSD в сеть хранения данных сервера VDI, в которой все виртуальные компьютеры смогут получать к ним доступ, например в общую папку.</span><span class="sxs-lookup"><span data-stu-id="5bf01-189">Copy the Sftfs.fsd cache file to the VDI server’s SAN where all the VMs can access it, such as in a shared folder.</span></span> <span data-ttu-id="5bf01-190">Вы можете использовать другое имя файла, например SFTFS \ _V2. FSD, чтобы отличать новую версию.</span><span class="sxs-lookup"><span data-stu-id="5bf01-190">You can use a different filename, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="5bf01-191">Чтобы настроить клиент App-V для настольных компьютеров на образе виртуальной машины VDI для использования обновленного файла общего кэша, измените значение FILENAME для раздела реестра AppFS таким образом, чтобы он указывал на расположение обновленного файла, например \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD.</span><span class="sxs-lookup"><span data-stu-id="5bf01-191">To configure the App-V Desktop Client on the VDI Master VM Image to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\VDIServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="5bf01-192">Это гарантирует, что новые пользователи получат новую версию.</span><span class="sxs-lookup"><span data-stu-id="5bf01-192">This ensures that new users get the new version.</span></span>

6.  <span data-ttu-id="5bf01-193">Создайте сценарий, который редактирует значение имени файла ключа AppFS, чтобы задать для него расположение обновленного кэша, например \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD.</span><span class="sxs-lookup"><span data-stu-id="5bf01-193">Create a script that edits the AppFS key FILENAME value to set it to the location of the updated cache, for example, \\\\VDIServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="5bf01-194">Настройте этот сценарий, чтобы он выполнялся, когда пользователь выходит из системы или входит в систему, чтобы он выполнялся перед запуском клиентских драйверов App-V, например с помощью параметров групповой политики.</span><span class="sxs-lookup"><span data-stu-id="5bf01-194">Configure this script to run when the user logs off or logs on so that it runs before the App-V client drivers start, for example, by using Group Policy settings.</span></span> <span data-ttu-id="5bf01-195">Когда пользователь выходит из системы и снова входит в систему, будет обновлена Текущая виртуальная машина, и они будут использовать обновленную копию кэша.</span><span class="sxs-lookup"><span data-stu-id="5bf01-195">When users log off and log on again, their existing VM is updated, and they will use the updated copy of the cache.</span></span> <span data-ttu-id="5bf01-196">После этого у них будет доступ к обновленным приложениям.</span><span class="sxs-lookup"><span data-stu-id="5bf01-196">Then, they have access to the updated applications.</span></span>

## <span data-ttu-id="5bf01-197">Использование символьных ссылок при обновлении кэша</span><span class="sxs-lookup"><span data-stu-id="5bf01-197">How to Use Symbolic Links when Upgrading the Cache</span></span>


<span data-ttu-id="5bf01-198">Вместо того чтобы изменять значение имени файла ключа AppFS каждый раз при развертывании нового файла кэша, содержащего новые или обновленные пакеты, можно использовать символьную ссылку в следующих операционных системах: Windows Vista, Windows 7 и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5bf01-198">Instead of modifying the AppFS key FILENAME value every time that a new cache file is deployed that contains new or upgraded packages, you can use a symbolic link in the following operating systems: Windows Vista, Windows 7, and Windows Server 2008.</span></span> <span data-ttu-id="5bf01-199">Дополнительные сведения о символических [ссылках см](https://go.microsoft.com/fwlink/?LinkId=157626) https://go.microsoft.com/fwlink/?LinkId=157626) .</span><span class="sxs-lookup"><span data-stu-id="5bf01-199">For more information about symbolic links, see [Symbolic Links](https://go.microsoft.com/fwlink/?LinkId=157626) (https://go.microsoft.com/fwlink/?LinkId=157626).</span></span> <span data-ttu-id="5bf01-200">В отличие от этого, Windows XP не поддерживает использование символических ссылок, поэтому вместо них следует использовать точки соединения.</span><span class="sxs-lookup"><span data-stu-id="5bf01-200">In contrast, Windows XP does not support the use of symbolic links, and you must use junction points instead.</span></span> <span data-ttu-id="5bf01-201">Дополнительные сведения о соединениях можно найти в [статье 205524](https://go.microsoft.com/fwlink/?LinkId=182553) в базе знаний Майкрософт ( https://go.microsoft.com/fwlink/?LinkId=182553) а также на [1.05е](https://go.microsoft.com/fwlink/?LinkId=182554) с помощью средства v https://go.microsoft.com/fwlink/?LinkId=182554) .</span><span class="sxs-lookup"><span data-stu-id="5bf01-201">For more information about junctions, see [article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=182553), and also the tool [Junction v1.05](https://go.microsoft.com/fwlink/?LinkId=182554) (https://go.microsoft.com/fwlink/?LinkId=182554).</span></span>

**<span data-ttu-id="5bf01-202">Настройка символьной ссылки для ссылки на кэш</span><span class="sxs-lookup"><span data-stu-id="5bf01-202">To configure a symbolic link to reference the cache</span></span>**

1.  <span data-ttu-id="5bf01-203">На начальном этапе развертывания откройте окно командной строки как локальный администратор в операционной системе сервера VDI.</span><span class="sxs-lookup"><span data-stu-id="5bf01-203">During the initial deployment stage, open a Command Prompt window as a local administrator on the VDI server host operating system.</span></span>

2.  <span data-ttu-id="5bf01-204">Создайте символьную ссылку с помощью команды MKLINK и настройте ее так, чтобы она указывала на файл Sftfs. fsd.</span><span class="sxs-lookup"><span data-stu-id="5bf01-204">Create a symbolic link by using the MKLINK command, and then configure it to point to the Sftfs.fsd file.</span></span>

    **     <span data-ttu-id="5bf01-205">mklink symlinkname \\\\vdihostserver\\sharefolder\\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="5bf01-205">mklink symlinkname \\\\vdihostserver\\sharefolder\\sftfs.fsd</span></span>**

3.  <span data-ttu-id="5bf01-206">В образе эталонной виртуальной машины VDI откройте окно командной строки с помощью команды " **Запуск от имени администратора** " и предоставьте разрешения удаленной ссылки таким образом, чтобы виртуальная машина могла получить доступ к символической ссылке в операционной системе сервера VDI.</span><span class="sxs-lookup"><span data-stu-id="5bf01-206">On the VDI Master VM Image, open a Command Prompt window by using the **Run as administrator** option and grant remote link permissions so that the VM can access the symbolic link on the VDI Host operating system.</span></span> <span data-ttu-id="5bf01-207">По умолчанию разрешения для удаленной ссылки отключены.</span><span class="sxs-lookup"><span data-stu-id="5bf01-207">By default, remote link permissions are disabled.</span></span>

    **<span data-ttu-id="5bf01-208">fsutil behavior Set SymlinkEvaluation R2R: 1</span><span class="sxs-lookup"><span data-stu-id="5bf01-208">fsutil behavior set SymlinkEvaluation R2R:1</span></span>**

    <span data-ttu-id="5bf01-209">**Примечание**  На сервере хранилища должны быть включены соответствующие разрешения на ссылки.</span><span class="sxs-lookup"><span data-stu-id="5bf01-209">**Note** On the storage server, appropriate link permissions must be enabled.</span></span> <span data-ttu-id="5bf01-210">В зависимости от расположения ссылки и файла Sftfs. FSD разрешениями являются **L2L: 1** или **L2R: 1** или **r2l:** **1 или**.</span><span class="sxs-lookup"><span data-stu-id="5bf01-210">Depending on the location of link and the Sftfs.fsd file, the permissions are **L2L:1** or **L2R:1** or **R2L:1** or **R2R:1**.</span></span>

     

4.  <span data-ttu-id="5bf01-211">Когда вы настраиваете клиент App-V для настольных компьютеров на образе основной виртуальной машины VDI, задайте для AppFS key значение FILENAME, равное UNC-пути к файлу FSD, использующему символьную ссылку. Например, установите для него значение \\\\VDIHostserver\\Symlinkname.</span><span class="sxs-lookup"><span data-stu-id="5bf01-211">When you configure the App-V Desktop Client on the VDI Master VM Image, set the AppFS key FILENAME value equal to the UNC path of the FSD file that is using the symbolic link; for example, set it to \\\\VDIHostserver\\Symlinkname.</span></span> <span data-ttu-id="5bf01-212">Когда клиент App-V сначала пытается получить доступ к кэшу, символическая ссылка передает клиенту дескриптор файлу кэша.</span><span class="sxs-lookup"><span data-stu-id="5bf01-212">When the App-V client first accesses the cache, the symbolic link passes to the client a handle to the cache file.</span></span> <span data-ttu-id="5bf01-213">Клиент продолжает использовать этот дескриптор, пока клиент запущен.</span><span class="sxs-lookup"><span data-stu-id="5bf01-213">The client continues to use that handle as long as the client is running.</span></span> <span data-ttu-id="5bf01-214">Значение символьной ссылки может безопасно обновляться даже в том случае, если для существующих клиентов открыт старый общий кэш.</span><span class="sxs-lookup"><span data-stu-id="5bf01-214">The value of the symbolic link can safely be updated even if existing clients have the old shared cache open.</span></span>

5.  <span data-ttu-id="5bf01-215">Если необходимо обновить пакет или добавить новый пакет в кэш, выполните действия 1 – 5 процедуры обновления для сценария static VM или пула ВМ.</span><span class="sxs-lookup"><span data-stu-id="5bf01-215">When you must upgrade a package or to add a new package to the cache, follow steps 1 through 5 of the upgrade procedure for either the Static VM or Pooled VM scenario.</span></span> <span data-ttu-id="5bf01-216">Затем удалите символьную ссылку и повторно создайте ее, чтобы она указывала на новую версию общего файла кэша.</span><span class="sxs-lookup"><span data-stu-id="5bf01-216">Then, delete the symbolic link and re-create it to point to the new version of the shared cache file.</span></span> <span data-ttu-id="5bf01-217">После перезапуска виртуальной машины клиент получает дескриптор обновленной копии кэша, так как виртуальная машина использует путь, который содержит обновленную символьную ссылку.</span><span class="sxs-lookup"><span data-stu-id="5bf01-217">When the VM is restarted, the client receives a handle to the updated copy of the cache because the VM uses the path that contains the updated symbolic link.</span></span> <span data-ttu-id="5bf01-218">Затем пользователи смогут получить доступ к новым и обновленным приложениям.</span><span class="sxs-lookup"><span data-stu-id="5bf01-218">Then, the users have access to the new and updated applications.</span></span>

## <span data-ttu-id="5bf01-219">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5bf01-219">Related topics</span></span>


[<span data-ttu-id="5bf01-220">Установка сервера Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="5bf01-220">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

[<span data-ttu-id="5bf01-221">Установка клиента Application Virtualization Client вручную</span><span class="sxs-lookup"><span data-stu-id="5bf01-221">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="5bf01-222">Установка клиента с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="5bf01-222">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





