---
title: Новые возможности в UE-V 2.1
description: Новые возможности в UE-V 2.1
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826262"
---
# <span data-ttu-id="0a802-103">Новые возможности в UE-V 2.1</span><span class="sxs-lookup"><span data-stu-id="0a802-103">What's New in UE-V 2.1</span></span>


<span data-ttu-id="0a802-104">Виртуализация взаимодействия с пользователем 2,1 предоставляет эти новые функции и возможности по сравнению с UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="0a802-104">User Experience Virtualization 2.1 provides these new features and functionality compared to UE-V 2.0.</span></span> <span data-ttu-id="0a802-105">В [заметках о выпуске Microsoft User Experience Virtualization (UE-v) 2,1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) содержатся дополнительные сведения о выпуске UE-v 2,1.</span><span class="sxs-lookup"><span data-stu-id="0a802-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) provide more information about the UE-V 2.1 release.</span></span>

## <span data-ttu-id="0a802-106">Шаблон расположения параметров в Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a802-106">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="0a802-107">UE-V 2,1 включает шаблон расположений параметров Microsoft Office 2013 с улучшенной поддержкой подписи Outlook.</span><span class="sxs-lookup"><span data-stu-id="0a802-107">UE-V 2.1 includes the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="0a802-108">В UE-V 2,1 данные подписи синхронизируются между пользовательскими устройствами.</span><span class="sxs-lookup"><span data-stu-id="0a802-108">In UE-V 2.1, the signature data synchronizes between user devices.</span></span> <span data-ttu-id="0a802-109">Добавлена синхронизация параметров подписи по умолчанию для новых, ответных и пересылаемых сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0a802-109">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="0a802-110">Пользователям больше не нужно выбирать параметры подписи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0a802-110">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="0a802-111">**Примечание**  Профиль Outlook должен быть создан для любого устройства, на котором пользователь хочет синхронизировать свою подпись Outlook.</span><span class="sxs-lookup"><span data-stu-id="0a802-111">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="0a802-112">Если профиль еще не создан, пользователь может создать его, а затем перезапустить Outlook на этом устройстве, чтобы включить синхронизацию подписей.</span><span class="sxs-lookup"><span data-stu-id="0a802-112">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="0a802-113">Ранее UE-V содержал шаблоны расположений параметров Microsoft Office 2010, которые были автоматически распределены и зарегистрированы в агенте UE-V.</span><span class="sxs-lookup"><span data-stu-id="0a802-113">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="0a802-114">UE-V 2,1 работает с Office 365, чтобы определить, будут ли параметры Office 2013 перемещены в Office 365.</span><span class="sxs-lookup"><span data-stu-id="0a802-114">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="0a802-115">Если параметры перемещаются в Office 365, они не перемещаются UE-V.</span><span class="sxs-lookup"><span data-stu-id="0a802-115">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="0a802-116">[Общие сведения о параметрах пользователей и роуминга для Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) .</span><span class="sxs-lookup"><span data-stu-id="0a802-116">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="0a802-117">Чтобы включить синхронизацию параметров с помощью UE-V 2,1, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="0a802-117">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="0a802-118">Отключение синхронизации Office 365 с помощью групповой политики</span><span class="sxs-lookup"><span data-stu-id="0a802-118">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="0a802-119">Не включайте процесс синхронизации Office 365 во время установки Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a802-119">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="0a802-120">UE-V 2,1 поставляется с [шаблонами office 2013 и office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="0a802-120">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="0a802-121">В этом выпуске удаляются шаблоны Office 2007.</span><span class="sxs-lookup"><span data-stu-id="0a802-121">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="0a802-122">Пользователи по-прежнему могут использовать шаблоны Office 2007 с UE-V 2,0 или более ранней версии, но по-прежнему смогут получать шаблоны из галереи шаблонов UE-V, расположенной [здесь](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="0a802-122">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>

## <span data-ttu-id="0a802-123">Исправление для пользователей пространства имен распределенной файловой системы</span><span class="sxs-lookup"><span data-stu-id="0a802-123">Fix for Distributed File System Namespace Users</span></span>


<span data-ttu-id="0a802-124">UE-V имеет улучшенную поддержку пространства имен распределенной файловой системы (DFSN) путем добавления конфигурации UE-V с именем SyncProviderPingEnabled.</span><span class="sxs-lookup"><span data-stu-id="0a802-124">UE-V has improved Distributed File System Namespace (DFSN) support by adding a UE-V configuration called SyncProviderPingEnabled.</span></span> <span data-ttu-id="0a802-125">Отключение этой конфигурации с помощью PowerShell или WMI позволяет пользователям отключить UE-V ping.</span><span class="sxs-lookup"><span data-stu-id="0a802-125">Disabling this configuration using PowerShell or WMI allows users to disable the UE-V ping.</span></span> <span data-ttu-id="0a802-126">Проверка связи UE-V вызывает ошибку при использовании серверов DFSN, так как эти серверы не отвечают на команды ping.</span><span class="sxs-lookup"><span data-stu-id="0a802-126">The UE-V ping causes an error when using DFSN servers because these servers do not respond to pings.</span></span> <span data-ttu-id="0a802-127">Неответные сообщения не допускает UE-V с параметрами синхронизации.</span><span class="sxs-lookup"><span data-stu-id="0a802-127">The non-response prevents UE-V from synchronizing settings.</span></span> <span data-ttu-id="0a802-128">Отключение команды UE-V ping обеспечивает синхронизацию UE-V для работы в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="0a802-128">Disabling the UE-V ping allows UE-V synchronization to work normally.</span></span>

<span data-ttu-id="0a802-129">Чтобы отключить команду ping для UE-V, используйте следующий командлет PowerShell:</span><span class="sxs-lookup"><span data-stu-id="0a802-129">To disable UE-V ping, use this PowerShell cmdlet:</span></span>

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## <span data-ttu-id="0a802-130">Синхронизация для учетных данных</span><span class="sxs-lookup"><span data-stu-id="0a802-130">Synchronization for Credentials</span></span>


<span data-ttu-id="0a802-131">UE-V 2,1 предоставляет клиентам возможность синхронизировать учетные данные и сертификаты, хранящиеся в диспетчере учетных данных Windows.</span><span class="sxs-lookup"><span data-stu-id="0a802-131">UE-V 2.1 gives customers the ability to synchronize credentials and certificates stored in the Windows Credential Manager.</span></span> <span data-ttu-id="0a802-132">Этот компонент отключен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0a802-132">This component is disabled by default.</span></span> <span data-ttu-id="0a802-133">Если включить этот компонент, пользователи смогут синхронизировать свои учетные данные и сертификаты домена. Пользователи могут выполнять вход на устройстве один раз, и эти учетные данные будут перемещаться для этого пользователя на всех устройствах, поддерживающих UE-V.</span><span class="sxs-lookup"><span data-stu-id="0a802-133">Enabling this component lets users keep their domain credentials and certificates in sync. Users can sign in one time on a device, and these credentials will roam for that user across all of their UE-V enabled devices.</span></span> <span data-ttu-id="0a802-134">[Управление учетными данными с помощью UE-V 2,1](https://technet.microsoft.com/library/dn458932.aspx#creds) предоставляет дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0a802-134">[Manage Credentials with UE-V 2.1](https://technet.microsoft.com/library/dn458932.aspx#creds) provides more information.</span></span>

<span data-ttu-id="0a802-135">**Примечание**  В Windows 8 и более поздних версиях Диспетчер учетных данных включает веб-учетные данные.</span><span class="sxs-lookup"><span data-stu-id="0a802-135">**Note** In Windows 8 and later, Credential Manager contains web credentials.</span></span> <span data-ttu-id="0a802-136">Эти учетные данные не синхронизируются между устройствами пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a802-136">These credentials are not synchronized between users’ devices.</span></span>

 

## <span data-ttu-id="0a802-137">Синхронизация с учетной записью UE-V и Microsoft</span><span class="sxs-lookup"><span data-stu-id="0a802-137">UE-V and Microsoft Account Synchronization</span></span>


<span data-ttu-id="0a802-138">UE-V определяет, включено ли "Синхронизация параметров с OneDrive", также называемая синхронизацией учетных записей Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0a802-138">UE-V detects if “Sync settings with OneDrive”, also known as Microsoft Account synchronization, is on.</span></span> <span data-ttu-id="0a802-139">Если учетная запись Майкрософт не настроена для синхронизации параметров, UE-V синхронизирует приложения для Windows, пакеты AppX и параметры рабочего стола Windows между устройствами.</span><span class="sxs-lookup"><span data-stu-id="0a802-139">If the Microsoft Account is not configured to synchronize settings, UE-V synchronizes Windows apps, AppX packages, and Windows desktop settings between devices.</span></span> <span data-ttu-id="0a802-140">Это позволит пользователям получать доступ к своим приложениям магазина, музыке, изображениям и другим приложениям, поддерживающим учетные записи Майкрософт, без синхронизации за пределами брандмауэра предприятия.</span><span class="sxs-lookup"><span data-stu-id="0a802-140">This lets users access their Store apps, music, pictures and other Microsoft Account-enabled applications without syncing outside of the enterprise firewall.</span></span> <span data-ttu-id="0a802-141">UE-V проверяет, будет ли групповая политика прекратить синхронизацию параметров с OneDrive, или, если пользователь отключает **синхронизацию параметров на этом компьютере** в пользовательских элементах управления.</span><span class="sxs-lookup"><span data-stu-id="0a802-141">UE-V checks whether Group Policy will stop synchronizing settings with OneDrive or if the user disables **Sync your settings on this computer** in the user controls.</span></span>

## <span data-ttu-id="0a802-142">Поддержка внешних PowerSchool</span><span class="sxs-lookup"><span data-stu-id="0a802-142">Support for the SyncMethod External</span></span>


<span data-ttu-id="0a802-143">Новая [Конфигурация PowerSchool](https://technet.microsoft.com/library/dn554321.aspx) с именем **External** указывает на то, что если параметры UE-V записываются в локальную папку на компьютере пользователя, можно использовать любые внешние обработчики синхронизации (например, OneDrive для бизнеса, рабочие папки, SharePoint или Dropbox) для применения этих параметров к разным компьютерам, к которым пользователи обращаются.</span><span class="sxs-lookup"><span data-stu-id="0a802-143">A new [SyncMethod configuration](https://technet.microsoft.com/library/dn554321.aspx) called **External** specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

## <span data-ttu-id="0a802-144">Улучшенная поддержка режима VDI</span><span class="sxs-lookup"><span data-stu-id="0a802-144">Enhanced Support for VDI Mode</span></span>


<span data-ttu-id="0a802-145">UE-V 2,1 включает [поддержку сеансов VDI](https://technet.microsoft.com/library/dn458932.aspx#vdi) , которые являются общими для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="0a802-145">UE-V 2.1 includes [support for VDI sessions](https://technet.microsoft.com/library/dn458932.aspx#vdi) that are shared among end users.</span></span> <span data-ttu-id="0a802-146">Администратор может зарегистрировать и настроить специальный шаблон VDI, который гарантирует, что в UE-V все возможности остаются неизменными для неустойчивых сеансов VDI.</span><span class="sxs-lookup"><span data-stu-id="0a802-146">As an administrator, you can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

<span data-ttu-id="0a802-147">**Примечание**  Если вы не включите режим VDI для непостоянных сеансов VDI, некоторые функции не работают, такие как резервное копирование/восстановление и LKG.</span><span class="sxs-lookup"><span data-stu-id="0a802-147">**Note** If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as back-up/restore and LKG.</span></span>

 

## <span data-ttu-id="0a802-148">Административное резервное копирование и восстановление</span><span class="sxs-lookup"><span data-stu-id="0a802-148">Administrative Backup and Restore</span></span>


<span data-ttu-id="0a802-149">Вы можете восстановить дополнительные параметры, когда пользователь применяет новое устройство, поместив шаблон расположения параметров в профиль **резервного копирования** или **перемещения (по умолчанию)** с помощью командлета PowerShell Set-UevTemplateProfile.</span><span class="sxs-lookup"><span data-stu-id="0a802-149">You can restore additional settings when a user adopts a new device by putting a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="0a802-150">Это позволит синхронизировать параметры компьютера с новым компьютером в дополнение к параметрам пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a802-150">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="0a802-151">Шаблоны, назначенные профилю резервного копирования, заархивированы для этого устройства и настроены отдельно для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="0a802-151">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="0a802-152">[Управление административными резервными копиями и восстановлением в UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) содержит дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0a802-152">[Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) provides more information.</span></span>

## <span data-ttu-id="0a802-153">Синхронизация для дополнительных параметров Windows</span><span class="sxs-lookup"><span data-stu-id="0a802-153">Synchronization for Additional Windows Settings</span></span>


<span data-ttu-id="0a802-154">UE-V теперь синхронизирует настройки сенсорной клавиатуры, словарь проверки орфографии и позволяет переключаться между последними приложениями и параметрами экрана для синхронизации между устройствами Windows 8 и Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="0a802-154">UE-V now synchronizes touch keyboard personalization, the spelling dictionary, and enables the App Switching for recent apps and screen edge settings to synchronize between Windows 8 and Windows 8.1 devices.</span></span>






## <span data-ttu-id="0a802-155">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0a802-155">Related topics</span></span>


[<span data-ttu-id="0a802-156">Начало работы с UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="0a802-156">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="0a802-157">Подготовка к развертыванию UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="0a802-157">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="0a802-158">Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.1</span><span class="sxs-lookup"><span data-stu-id="0a802-158">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





