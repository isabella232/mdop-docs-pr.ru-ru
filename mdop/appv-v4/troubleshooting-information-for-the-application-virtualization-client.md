---
title: Сведения об устранении неполадок в клиенте Application Virtualization
description: Сведения об устранении неполадок в клиенте Application Virtualization
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815192"
---
# <span data-ttu-id="c5c70-103">Сведения об устранении неполадок в клиенте Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c5c70-103">Troubleshooting Information for the Application Virtualization Client</span></span>


<span data-ttu-id="c5c70-104">Этот раздел содержит сведения, которые можно использовать для устранения различных проблем в клиенте Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="c5c70-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Client.</span></span>

## <span data-ttu-id="c5c70-105">Обновление публикации происходит очень медленно</span><span class="sxs-lookup"><span data-stu-id="c5c70-105">Publishing Refresh Is Very Slow</span></span>


<span data-ttu-id="c5c70-106">Если обновление публикации на определенном компьютере занимает больше времени, чем ожидалось, и если клиент настроен на использование параметра **IconSourceRoot** , определите, содержит ли **IconSourceRoot** недопустимый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="c5c70-106">If publishing refresh on a specific computer takes much longer than expected and if the client is configured to use the **IconSourceRoot** setting, determine whether **IconSourceRoot** contains a nonvalid URL.</span></span> <span data-ttu-id="c5c70-107">Недопустимый URL-адрес приведет к очень долгой задержке при обновлении публикации.</span><span class="sxs-lookup"><span data-stu-id="c5c70-107">A nonvalid URL will cause very long delays during publishing refresh.</span></span>

## <span data-ttu-id="c5c70-108">Пользователи не могут подключаться к серверу и переходить в режим разъединенных операций</span><span class="sxs-lookup"><span data-stu-id="c5c70-108">Users Cannot Connect to the Server and Go into Disconnected Operations Mode</span></span>


<span data-ttu-id="c5c70-109">Если вы используете сервер управления App-V, настроенный по протоколу RTSP, если пользователи не могут подключиться к сети и они переходят в режим отключенных операций, определите, является ли сертификат, используемый на сервере, действительным.</span><span class="sxs-lookup"><span data-stu-id="c5c70-109">When you are using an App-V Management Server configured with the RTSPS protocol, if the users are unable to connect and they go into disconnected operations mode, determine whether the certificate that is being used on the server is valid.</span></span> <span data-ttu-id="c5c70-110">Недействительный сертификат не позволит пользователям подключаться к сети и приведет к переходу в режим разъединенных операций.</span><span class="sxs-lookup"><span data-stu-id="c5c70-110">A nonvalid certificate will prevent users from connecting and will cause them to go into disconnected operations mode.</span></span>

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a><span data-ttu-id="c5c70-111">Производительность пользователей снижается, если приложения не полностью кэшируются</span><span class="sxs-lookup"><span data-stu-id="c5c70-111">Users Experience Slow Performance When Applications Are Not Fully Cached</span></span>


<span data-ttu-id="c5c70-112">Если приложения не были полностью кэшированы, при запуске или использовании приложения пользователи могут иногда испытывать временную задержку или периодический доступ к производительности.</span><span class="sxs-lookup"><span data-stu-id="c5c70-112">When applications are not fully cached, users might occasionally experience temporary slow or intermittent performance when they start or use the application.</span></span> <span data-ttu-id="c5c70-113">Есть несколько причин, по которым это может произойти, например, когда клиент App-V находится в процессе автоматической загрузки приложения или при обработке запроса вне последовательности.</span><span class="sxs-lookup"><span data-stu-id="c5c70-113">There are several possible reasons this can occur—for example, when the App-V Client is in the process of auto-loading an application or when an Out Of Sequence request is being processed.</span></span> <span data-ttu-id="c5c70-114">Если приложения полностью кэшируются, эти проблемы больше не возникнут.</span><span class="sxs-lookup"><span data-stu-id="c5c70-114">When the applications are fully cached, these problems will no longer occur.</span></span>

## <a href="" id="error-displayed-after-an-update-is-removed-"></a><span data-ttu-id="c5c70-115">После удаления обновления появляется сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="c5c70-115">Error Displayed After an Update Is Removed</span></span>


<span data-ttu-id="c5c70-116">Для удаления обновления из клиента App-V необходимо использовать правильный формат команды Windows Installer 3,1, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="c5c70-116">You must use the correct Windows Installer 3.1 command format to remove an update from the App-V Client, as follows:</span></span>

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

<span data-ttu-id="c5c70-117">Использование старого формата команд `msiexec /package <GUID> /uninstall <GUID>` вызовет ошибку 6003 "не удается запустить клиент Application Virtualization".</span><span class="sxs-lookup"><span data-stu-id="c5c70-117">Using the older command format `msiexec /package <GUID> /uninstall <GUID>` will cause error 6003 "Application Virtualization client could not be started".</span></span>

## <span data-ttu-id="c5c70-118">Код ошибки 0A-0000E01E появляется при попытке запустить приложение</span><span class="sxs-lookup"><span data-stu-id="c5c70-118">Error Code 0A-0000E01E Occurs When You Try to Start an Application</span></span>


<span data-ttu-id="c5c70-119">Код ошибки 0A-0000E01E указывает на то, что последовательный пакет приложения может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="c5c70-119">Error code 0A-0000E01E indicates that the sequenced application package might be corrupt.</span></span> <span data-ttu-id="c5c70-120">Решением является Переупорядочение пакета.</span><span class="sxs-lookup"><span data-stu-id="c5c70-120">The solution is to resequence the package.</span></span>

## <span data-ttu-id="c5c70-121">Пользователи не могут получить доступ к созданным ими файлам на диске Q:</span><span class="sxs-lookup"><span data-stu-id="c5c70-121">Users Cannot Access Files They Have Created on the Q: Drive</span></span>


<span data-ttu-id="c5c70-122">Если пользователи сохраняют файлы на диск **Q:** , они не смогут получить их, так как у них нет прав на чтение.</span><span class="sxs-lookup"><span data-stu-id="c5c70-122">If users save files to the **Q:** drive, they cannot retrieve them because they do not have read rights to the drive.</span></span> <span data-ttu-id="c5c70-123">Пользователи не должны сохранять файлы на диске **Q:** .</span><span class="sxs-lookup"><span data-stu-id="c5c70-123">Users should not save files to the **Q:** drive.</span></span>

## <span data-ttu-id="c5c70-124">У пользователя появляется сообщение об ошибке 1D1</span><span class="sxs-lookup"><span data-stu-id="c5c70-124">User Is Prompted with a 1D1 Error</span></span>


<span data-ttu-id="c5c70-125">Если URL-адрес потоковой передачи файлов задан неправильно в файле Open Software descriptor (OSD), клиент App-V возвращает ошибку 1d1 вместо ошибки "файл не найден".</span><span class="sxs-lookup"><span data-stu-id="c5c70-125">When the file streaming URL is incorrectly set in the Open Software Descriptor (OSD) file, the App-V Client returns a 1d1 error instead of a “file not found” error.</span></span> <span data-ttu-id="c5c70-126">Эта ошибка указывает на то, что при запуске приложения произошел сбой, и пользователь принудительно переключается в режим разъединенных операций.</span><span class="sxs-lookup"><span data-stu-id="c5c70-126">This error indicates that the application start failed and the user has been forced into disconnected operations mode.</span></span> <span data-ttu-id="c5c70-127">Исправьте URL-адрес потоковой передачи файла.</span><span class="sxs-lookup"><span data-stu-id="c5c70-127">Correct the file streaming URL.</span></span>

## <span data-ttu-id="c5c70-128">Неверные значки, связанные с некоторыми приложениями</span><span class="sxs-lookup"><span data-stu-id="c5c70-128">Incorrect Icons Associated with Some Applications</span></span>


<span data-ttu-id="c5c70-129">Когда в операции публикации используется значок, клиент App-V сначала определяет, есть ли у него кэшированная копия значка, путем поиска в кэше значков для элемента, исходный путь которого совпадает с путем к значку, указанному в операции публикации.</span><span class="sxs-lookup"><span data-stu-id="c5c70-129">When an icon is to be used in a publishing operation, the App-V Client first determines whether it already has a cached copy of the icon, by looking in the icon cache for an item whose original source path matches the path of the icon given to the publishing operation.</span></span> <span data-ttu-id="c5c70-130">Если клиент App-V находит соответствие, он будет использовать уже кэшированный значок; в противном случае в кэш будет загружен новый значок.</span><span class="sxs-lookup"><span data-stu-id="c5c70-130">If the App-V Client finds a match, it will use the already-cached icon; otherwise, it will download the new icon into the cache.</span></span> <span data-ttu-id="c5c70-131">Если путь к значку является каталогом временных файлов или он повторно используется для новых значков или пакетов, поиск в кэше может выбрать неверный значок из предыдущей операции.</span><span class="sxs-lookup"><span data-stu-id="c5c70-131">If the path to the icon is a scratch directory or if it gets reused for new icons or packages, the lookup in the cache might pick the wrong icon from a previous operation.</span></span>

## <span data-ttu-id="c5c70-132">Пользователи получают запрос на ввод учетных данных при запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="c5c70-132">Users Are Prompted for Credentials When Starting an Application</span></span>


<span data-ttu-id="c5c70-133">Если пользователь попытается запустить виртуальное приложение, доступ к которому у системного администратора ограничен, пользователю может быть предложено ввести учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c5c70-133">If a user attempts to start a virtual application to which the system administrator has restricted access, the user might be prompted to enter credentials.</span></span> <span data-ttu-id="c5c70-134">Пользователь должен ввести имя пользователя и пароль для учетной записи, у которой есть разрешение на запуск приложения, и нажать клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="c5c70-134">The user should type the user name and password for an account that has permission to launch the application and then press ENTER.</span></span>

## <span data-ttu-id="c5c70-135">Обновление публикации завершается сбоем после обновления клиента App-V до версии 4,5</span><span class="sxs-lookup"><span data-stu-id="c5c70-135">Publishing Refresh Fails After Upgrading the App-V Client to Version 4.5</span></span>


<span data-ttu-id="c5c70-136">Если каталог данных пользователя был ранее помещен в нестандартное расположение (%*AllUsersProfile*%\\Documents\\SoftGrid Client\\Users\\%*username*%), пользователи, у которых нет прав администратора на компьютере, обнаружит, что обновление публикации завершается сбоем после обновления клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="c5c70-136">If the user data directory was previously placed in a non-standard location (%*AllUsersProfile*%\\Documents\\SoftGrid Client\\Users\\%*username*%), users who do not have administrator privileges on the computer will find that publishing refresh fails after the App-V Client is upgraded.</span></span> <span data-ttu-id="c5c70-137">Во время обновления каталог глобальных данных клиента App-V и все его подкаталоги настраиваются с ограниченными правами доступа только для администраторов.</span><span class="sxs-lookup"><span data-stu-id="c5c70-137">During the upgrade, the App-V Client global data directory and all its subdirectories are configured with restricted access rights for administrators only.</span></span> <span data-ttu-id="c5c70-138">Вы можете избежать этой проблемы, изменив каталог данных пользователя перед обновлением, чтобы он не был подкаталогом глобального каталога данных.</span><span class="sxs-lookup"><span data-stu-id="c5c70-138">You can avoid this problem by changing the user data directory before upgrading so that it is not a subdirectory of the global data directory.</span></span>

## <span data-ttu-id="c5c70-139">После сбоя установки требуется перезагрузка</span><span class="sxs-lookup"><span data-stu-id="c5c70-139">Reboot Required After Install Failure</span></span>


<span data-ttu-id="c5c70-140">Если по какой – либо причине не удается установить клиент и при последующих попытках установить клиент, проверьте, отображается ли в журнале установщика Windows сообщение об ошибке "sftplay Failed, Error = 1072".</span><span class="sxs-lookup"><span data-stu-id="c5c70-140">If the client install fails for any reason and if subsequent attempts to install the client also fail, check the Windows Installer log to see whether it shows an error “sftplay failed, error=1072”.</span></span> <span data-ttu-id="c5c70-141">Если это так, перезагрузите компьютер, прежде чем пытаться установить клиент еще раз.</span><span class="sxs-lookup"><span data-stu-id="c5c70-141">If so, restart the computer before trying to install the client again.</span></span>

## <span data-ttu-id="c5c70-142">Восстановление поврежденного виртуального приложения</span><span class="sxs-lookup"><span data-stu-id="c5c70-142">Repairing a Corrupted Virtual Application</span></span>


<span data-ttu-id="c5c70-143">Если по какой-либо причине виртуальный пакет приложения, установленный с использованием файла установщика Windows (MSI), повреждается, переустановите пакет.</span><span class="sxs-lookup"><span data-stu-id="c5c70-143">If for any reason a virtual application package installed using a Windows Installer Package (MSI) file becomes corrupted, reinstall the package.</span></span> <span data-ttu-id="c5c70-144">Функция восстановления, доступная в установщике Windows, не обновляет тома пользователей.</span><span class="sxs-lookup"><span data-stu-id="c5c70-144">The Repair function available in the Windows Installer will not update the user volumes.</span></span>

## <span data-ttu-id="c5c70-145">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c5c70-145">Related topics</span></span>


[<span data-ttu-id="c5c70-146">Справка по клиенту Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c5c70-146">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)

 

 





