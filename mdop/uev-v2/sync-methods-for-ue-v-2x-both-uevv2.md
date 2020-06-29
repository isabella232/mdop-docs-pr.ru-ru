---
title: Способы синхронизации в UE-V 2.x
description: Способы синхронизации в UE-V 2.x
author: dansimp
ms.assetid: af0ae894-dfdc-41d2-927b-c2ab1b355ffe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a163442e2ab3dbd777aca133b13b0086cdb8ae1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823579"
---
# <span data-ttu-id="fe9dc-103">Способы синхронизации в UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="fe9dc-103">Sync Methods for UE-V 2.x</span></span>


<span data-ttu-id="fe9dc-104">Агент Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 и 2,1 с пакетом обновления 1 (SP1) позволяет синхронизировать параметры приложений и Windows для пользователей с местом хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent lets you synchronize users’ application and Windows settings with the settings storage location.</span></span> <span data-ttu-id="fe9dc-105">Конфигурация *метода Sync* определяет, как агент UE-V отправляет и загружает эти параметры в место хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-105">The *Sync Method* configuration defines how the UE-V Agent uploads and downloads those settings to the settings storage location.</span></span> <span data-ttu-id="fe9dc-106">UE-V 2. x представляет новый PowerSchool, который называется *SyncProvider*.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-106">UE-V 2.x introduces a new SyncMethod called the *SyncProvider*.</span></span> <span data-ttu-id="fe9dc-107">Дополнительные сведения о событиях триггеров, в которых начинается синхронизация параметров приложения и Windows, приведены в разделе [события триггера синхронизации для UE-V 2. x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="fe9dc-107">For more information about trigger events that start the synchronization of application and Windows settings, see [Sync Trigger Events for UE-V 2.x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="fe9dc-108">Настройка PowerSchool</span><span class="sxs-lookup"><span data-stu-id="fe9dc-108">SyncMethod Configuration</span></span>


<span data-ttu-id="fe9dc-109">В этой таблице описаны изменения, внесенные в PowerSchool с UE-V v 1.0 на v 2.1, а также параметры для каждой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-109">This table explains the changes to SyncMethod from UE-V v1.0 to v2.0 to v2.1, as well as the settings for each configuration:</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fe9dc-110">Настройка PowerSchool</span><span class="sxs-lookup"><span data-stu-id="fe9dc-110">SyncMethod Configuration</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="fe9dc-111">Версия 1.0</span><span class="sxs-lookup"><span data-stu-id="fe9dc-111">V1.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="fe9dc-112">Версия 2.0</span><span class="sxs-lookup"><span data-stu-id="fe9dc-112">V2.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="fe9dc-113">Версия 2.1 и версия 2.1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="fe9dc-113">V2.1 and V2.1 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="fe9dc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="fe9dc-114">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe9dc-115">SyncProvider</span><span class="sxs-lookup"><span data-stu-id="fe9dc-115">SyncProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-116">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fe9dc-116">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-117">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe9dc-117">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-118">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe9dc-118">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-119">Изменения параметров для определенного приложения или для глобальных параметров рабочего стола Windows сохраняются локально в папке кэша.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-119">Settings changes for a specific application or for global Windows desktop settings are saved locally to a cache folder.</span></span> <span data-ttu-id="fe9dc-120">Эти изменения затем синхронизируются с расположением хранилища параметров, когда происходит событие триггера синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-120">These changes are then synchronized with the settings storage location when a synchronization trigger event takes place.</span></span> <span data-ttu-id="fe9dc-121">При отправке изменений локальные изменения будут сохранены в пути к хранилищу параметров.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-121">Pushing out changes will save the local changes to the settings storage path.</span></span></p>
<p><span data-ttu-id="fe9dc-122">Этот параметр по умолчанию является стандартом Gold для компьютеров.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-122">This default setting is the gold standard for computers.</span></span> <span data-ttu-id="fe9dc-123">Этот параметр пытается синхронизировать параметр и истекает время после короткой задержки, чтобы предотвратить задержку запуска приложения или операционной системы в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-123">This option attempts to synchronize the setting and times out after a short delay to ensure that the application or operating system startup isn’t delayed for a long period of time.</span></span></p>
<p><span data-ttu-id="fe9dc-124">Эта функция также привязана к приложению запланированной задачи — контроллеру синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-124">This functionality is also tied to the Scheduled task – Sync Controller Application.</span></span> <span data-ttu-id="fe9dc-125">Администратор управляет частотой запланированной задачи.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-125">The administrator controls the frequency of the Scheduled task.</span></span> <span data-ttu-id="fe9dc-126">По умолчанию компьютеры синхронизируют параметры каждые 30 минут после входа.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-126">By default, computers synchronize their settings every 30 min after logging on.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe9dc-127">OfflineFiles</span><span class="sxs-lookup"><span data-stu-id="fe9dc-127">OfflineFiles</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-128">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe9dc-128">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-129">Не рекомендуется</span><span class="sxs-lookup"><span data-stu-id="fe9dc-129">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-130">Не рекомендуется</span><span class="sxs-lookup"><span data-stu-id="fe9dc-130">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-131">Имеет тот же SyncProvider, что и в версии 2.0.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-131">Behaves the same as SyncProvider in V2.0.</span></span></p>
<p><span data-ttu-id="fe9dc-132">Если автономные файлы включены, а папка закреплена, то UE-V открепить эту папку и будет синхронизироваться непосредственно с центральным каталогом SMB.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-132">If Offline files are enabled and the folder is pinned then UE-V will unpin this folder and sync directly to the central SMB directory.</span></span></p>
<p><strong><span data-ttu-id="fe9dc-133">Примечание. </strong> в версии 1.0 если вы хотите использовать UE-V в корпоративной сети (как и в поездках), вы можете использовать автономные файлы, чтобы убедиться в том, что параметры перемещены.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-133">NOTE:</strong> In V1.0 if you wanted to use UE-V in a CorpNet disconnected manner (aka traveling with a Laptop), then the guidance is to use Offline Files to ensure that your settings roamed.</span></span><span data-ttu-id="fe9dc-134">Мы получили достаточно отзывов клиентов о том, что включение автономных файлов является нетривиальным корпоративным блоком.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-134"> We received sufficient customer feedback that turning on Offline files is a non-trivial enterprise blocker.</span></span> <span data-ttu-id="fe9dc-135">Итак, в UE-V 2 мы создали тесно связанный обработчик синхронизации для локального кэширования ваших данных и синхронизации параметров на центральном сервере.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-135">So in UE-V 2, we created a tightly coupled synchronization engine to cache your data locally and synchronize the settings to the central server.</span></span> <span data-ttu-id="fe9dc-136">Эта область функций не заменяет перенаправление автономных файлов и папок.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-136">This feature area does not replace Offline Files or Folder Redirection.</span></span></p>
<p><span data-ttu-id="fe9dc-137">UE-V 2 не работает с автономными папками, поэтому не следует задавать путь к хранилищу параметров для закрепленной автономной папки или в папке CSC.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-137">UE-V 2 does not work well with Offline folders so the guidance is not to set the settings storage path to a pinned Offline or CSC folder.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe9dc-138">Внешний</span><span class="sxs-lookup"><span data-stu-id="fe9dc-138">External</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-139">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fe9dc-139">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-140">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fe9dc-140">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-141">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fe9dc-141">Supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-142">Новые возможности UE-V 2,1. Этот метод конфигурации указывает на то, что если параметры UE-V записываются в локальную папку на компьютере пользователя, можно использовать любой внешний модуль синхронизации (например, OneDrive для бизнеса, рабочие папки, SharePoint или Dropbox), чтобы применить эти параметры для разных компьютеров, к которым пользователи обращаются.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-142">New in UE-V 2.1, this configuration method specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe9dc-143">Нет</span><span class="sxs-lookup"><span data-stu-id="fe9dc-143">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-144">Да</span><span class="sxs-lookup"><span data-stu-id="fe9dc-144">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-145">Да</span><span class="sxs-lookup"><span data-stu-id="fe9dc-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-146">Да</span><span class="sxs-lookup"><span data-stu-id="fe9dc-146">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe9dc-147">Этот параметр конфигурации предназначен для использования в инфраструктуре виртуальных рабочих столов (VDI) и потоковой работе приложения в основном.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-147">This configuration setting is designed for the Virtual Desktop Infrastructure (VDI) and Streamed Application experience primarily.</span></span> <span data-ttu-id="fe9dc-148">Этот параметр используется в полях Windows Server, используемых в центре обработки данных, в которых подключение всегда будет доступно.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-148">This setting should be used on Windows Server boxes used in a datacenter, where the connection will always be available.</span></span></p>
<p><span data-ttu-id="fe9dc-149">Изменения параметров сохраняются непосредственно на сервере.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-149">Any settings changes are saved directly to the server.</span></span> <span data-ttu-id="fe9dc-150">Если сетевое подключение к пути к хранилищу параметров недоступно, изменения параметров кэшируются на устройстве и синхронизируются при следующем запуске поставщика синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-150">If the network connection to the settings storage path is not available, then the settings changes are cached on the device and are synchronized the next time that the Sync Provider runs.</span></span> <span data-ttu-id="fe9dc-151">Если путь к хранилищу параметров не найден и профиль пользователя удален из среды VDI из пула при выходе из системы, эти параметры теряются, и пользователь должен повторно применить изменения, когда компьютер снова сможет получить доступ к пути к хранилищу параметров.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-151">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, then these settings changes are lost, and the user must reapply the change when the computer can again reach the settings storage path.</span></span></p>
<p><span data-ttu-id="fe9dc-152">Приложения и ОС будут ждать в течение неограниченного времени, пока не будет указано нужное расположение.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-152">Apps and OS will wait indefinitely for the location to be present.</span></span> <span data-ttu-id="fe9dc-153">Это может привести к тому, что загрузка приложения или время входа в операционную систему значительно увеличиваются в том случае, если расположение не найдено.</span><span class="sxs-lookup"><span data-stu-id="fe9dc-153">This could cause App load or OS logon time to dramatically increase if the location is not found.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fe9dc-154">Метод синхронизации можно настроить следующими способами:</span><span class="sxs-lookup"><span data-stu-id="fe9dc-154">You can configure the sync method in these ways:</span></span>

-   <span data-ttu-id="fe9dc-155">При [развертывании агента UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) с помощью параметра командной строки или пакетного сценария</span><span class="sxs-lookup"><span data-stu-id="fe9dc-155">When you [Deploy the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="fe9dc-156">С помощью параметров [групповой политики](https://technet.microsoft.com/library/dn458893.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe9dc-156">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="fe9dc-157">С помощью [пакета конфигурации System Center](https://technet.microsoft.com/library/dn458917.aspx) для UE-V</span><span class="sxs-lookup"><span data-stu-id="fe9dc-157">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="fe9dc-158">После установки агента UE-V с помощью [Windows PowerShell или инструментария управления Windows (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe9dc-158">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>






## <span data-ttu-id="fe9dc-159">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="fe9dc-159">Related topics</span></span>


[<span data-ttu-id="fe9dc-160">Развертывание необходимых компонентов для UE-v 2.x</span><span class="sxs-lookup"><span data-stu-id="fe9dc-160">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#ssl)

[<span data-ttu-id="fe9dc-161">Развертывание необходимых компонентов для UE-v 2.x</span><span class="sxs-lookup"><span data-stu-id="fe9dc-161">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#config)

[<span data-ttu-id="fe9dc-162">Технический справочник по UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="fe9dc-162">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





