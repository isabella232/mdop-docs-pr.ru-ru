---
title: Заметки о выпуске для App-V 5.0 с пакетом обновления 3 (SP3)
description: Заметки о выпуске для App-V 5.0 с пакетом обновления 3 (SP3)
author: dansimp
ms.assetid: bc4806e0-2aba-4c7b-9ecc-1b2cc54af1d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b6d5834e4d0c953365f955922403c1a7a2058b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813325"
---
# <span data-ttu-id="2d1f6-103">Заметки о выпуске для App-V 5.0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="2d1f6-103">Release Notes for App-V 5.0 SP3</span></span>


<span data-ttu-id="2d1f6-104">Ниже описаны известные проблемы, возникающие в Microsoft Application Virtualization (App-V) 5,0 с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="2d1f6-104">The following are known issues in Microsoft Application Virtualization (App-V) 5.0 SP3.</span></span>

## <span data-ttu-id="2d1f6-105">После установки нового сервера App-V 5,0 SP3 на сервер файлы сервера не удаляются</span><span class="sxs-lookup"><span data-stu-id="2d1f6-105">Server files fail to get deleted after a new App-V 5.0 SP3 Server installation</span></span>


<span data-ttu-id="2d1f6-106">Если вы удалите сервер App-V 5,0 SP1, а затем установите приложение App-V 5,0 SP3, установка завершится сбоем и на нем будет установлена неправильная версия сервера управления.</span><span class="sxs-lookup"><span data-stu-id="2d1f6-106">If you uninstall the App-V 5.0 SP1 Server and then install the App-V 5.0 SP3 Server, the installation fails and the wrong version of the Management server is installed.</span></span> <span data-ttu-id="2d1f6-107">На экране появятся указанные ниже ошибки.</span><span class="sxs-lookup"><span data-stu-id="2d1f6-107">The following errors are displayed:</span></span>

`[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {bee44f0f-05be-48e4-81dd-d34a83600b95}, type: Upgrade, scope: PerMachine, version: 5.0.1218.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.``[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {e1ca9d65-0ebf-4fd5-98e5-00d6453967a4}, type: Upgrade, scope: PerMachine, version: 5.0.1224.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.`

<span data-ttu-id="2d1f6-108">Проблема возникает из-за того, что файлы сервера не удаляются при удалении App-V 5,0 с пакетом обновления 1 (SP1), поэтому при установке App-V 5,0 SP3 вместо новой установки происходит обновление.</span><span class="sxs-lookup"><span data-stu-id="2d1f6-108">The issue occurs because the Server files are not being deleted when you uninstall App-V 5.0 SP1, so the App-V 5.0 SP3 installation process erroneously does an upgrade instead of a new installation.</span></span>

<span data-ttu-id="2d1f6-109">**Временное решение**: перед установкой App-V 5,0 SP3 удалите следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="2d1f6-109">**Workaround**: Delete the following registry key before you start installing App-V 5.0 SP3:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall`

## <span data-ttu-id="2d1f6-110">Запросы доменных служб Active Directory могут привести к неправильной работе некоторых приложений</span><span class="sxs-lookup"><span data-stu-id="2d1f6-110">Querying AD DS can cause some applications to work incorrectly</span></span>


<span data-ttu-id="2d1f6-111">При получении обновленных пакетов с помощью запроса доменных служб Active Directory для обновленных членств в группах может возникнуть ошибка, так как некоторые приложения будут работать неправильно, если приложения зависят от маркера доступа пользователя.</span><span class="sxs-lookup"><span data-stu-id="2d1f6-111">When you receive updated packages by querying Active Directory Domain Services for updated group memberships, it can cause some applications to work incorrectly if the applications depend on the user’s access token.</span></span> <span data-ttu-id="2d1f6-112">Кроме того, частые запросы на членство в группах могут привести к перегрузке контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="2d1f6-112">In addition, frequent group membership queries can cause the domain controller to overload.</span></span> <span data-ttu-id="2d1f6-113">Дополнительные сведения о маркерах доступа пользователей можно найти в разделе [маркеры доступа](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).</span><span class="sxs-lookup"><span data-stu-id="2d1f6-113">For more information about user access tokens, see [Access Tokens](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).</span></span>

<span data-ttu-id="2d1f6-114">**Временное решение**: дождитесь, пока пользователь не выйдет из системы, а затем снова войдите в систему, прежде чем запрашивать обновленные сведения о группах.</span><span class="sxs-lookup"><span data-stu-id="2d1f6-114">**Workaround**: Wait until the user logs off and then logs back on before you query for updated group memberships.</span></span> <span data-ttu-id="2d1f6-115">Не используйте раздел реестра, описанный в [пакете исправлений 2 для Microsoft Application Virtualization 5,0 с пакетом обновления 1](https://support.microsoft.com/kb/2897087)(SP1), для запроса обновленных сведений о членстве в группах.</span><span class="sxs-lookup"><span data-stu-id="2d1f6-115">Do not use the registry key, described in [Hotfix Package 2 for Microsoft Application Virtualization 5.0 Service Pack 1](https://support.microsoft.com/kb/2897087), to query for updated group memberships.</span></span>






## <span data-ttu-id="2d1f6-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2d1f6-116">Related topics</span></span>


[<span data-ttu-id="2d1f6-117">Сведения об App-V 5.0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="2d1f6-117">About App-V 5.0 SP3</span></span>](about-app-v-50-sp3.md)

 

 





