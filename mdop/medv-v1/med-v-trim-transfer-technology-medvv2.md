---
title: Технология передачи усеченных данных MED-V
description: Технология передачи усеченных данных MED-V
author: dansimp
ms.assetid: 2744e855-a486-4028-9606-f0084794ec65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa11c8036954070bbff465a6ad78992fdd52f3a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826189"
---
# <span data-ttu-id="a2a3b-103">Технология передачи усеченных данных MED-V</span><span class="sxs-lookup"><span data-stu-id="a2a3b-103">MED-V Trim Transfer Technology</span></span>


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


<span data-ttu-id="a2a3b-104">Улучшенная технология отмены и дублирования данных в MED-V ускоряет загрузку первоначальных и обновленных образов виртуальных машин через ЛОКАЛЬную сеть или глобальную сеть, тем самым уменьшая пропускную способность сети для передачи виртуальной машины MED-V Workspace нескольким конечным пользователям.</span><span class="sxs-lookup"><span data-stu-id="a2a3b-104">The MED-V advanced Trim Transfer de-duplication technology accelerates the download of initial and updated virtual machine images over the LAN or WAN, thereby reducing the network bandwidth needed to transport a MED-V workspace virtual machine to multiple end users.</span></span>

<span data-ttu-id="a2a3b-105">Эта революционная технология использует существующие локальные данные для создания образа виртуальной машины, используя тот факт, что в большинстве случаев большинство виртуальных машин (например, системы и файлы приложений) уже есть на диске конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="a2a3b-105">This breakthrough technology uses existing local data to build the virtual machine image, leveraging the fact that in many cases, much of the virtual machine (for example, system and application files) already exists on the end user's disk.</span></span> <span data-ttu-id="a2a3b-106">Например, если виртуальная машина, содержащая WindowsXP, доставляется клиенту с локальной копией WindowsXP, MED-V автоматически удалит избыточные элементы WindowsXP из передачи.</span><span class="sxs-lookup"><span data-stu-id="a2a3b-106">For example, if a virtual machine containing WindowsXP is delivered to a client running a local copy of WindowsXP, MED-V will automatically remove the redundant WindowsXP elements from the transfer.</span></span> <span data-ttu-id="a2a3b-107">Для обеспечения правильной и функциональной рабочей области клиент MED-V криптографически проверяет целостность локальных данных перед использованием, гарантируя, что локальные блоки данных находятся в незашифрованном виде, точно так же, как и в нужном образе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a2a3b-107">To ensure a valid and functional workspace, the MED-V client cryptographically verifies the integrity of local data before it is utilized, guaranteeing that the local blocks of data are absolutely bit-by-bit identical to those in the desired virtual machine image.</span></span> <span data-ttu-id="a2a3b-108">Несовпадающие блоки не используются.</span><span class="sxs-lookup"><span data-stu-id="a2a3b-108">Blocks that do not match are not used.</span></span>

<span data-ttu-id="a2a3b-109">Процесс — это эффективная и прозрачная пропускная способность и передача данных в фоновом режиме с использованием неиспользуемых ресурсов сети и ЦП.</span><span class="sxs-lookup"><span data-stu-id="a2a3b-109">The process is bandwidth-efficient and transparent, and transfers run in the background, utilizing unused network and CPU resources.</span></span>

<span data-ttu-id="a2a3b-110">При переходе к новой версии изображения (например, когда администраторы хотят распространять новое приложение или исправление) загружаются только те элементы, которые были изменены ("Разное"), а не вся виртуальная машина, что значительно уменьшает требуемую пропускную способность сети и время доставки.</span><span class="sxs-lookup"><span data-stu-id="a2a3b-110">When updating to a new image version (for example, when administrators want to distribute a new application or patch), only the elements that have changed ("deltas") are downloaded, and not the entire virtual machine, significantly reducing the required network bandwidth and delivery time.</span></span>

<span data-ttu-id="a2a3b-111">Вы можете настроить Индексирование папок на узле в рамках протокола передачи обрезки, зависящего от операционной системы узла.</span><span class="sxs-lookup"><span data-stu-id="a2a3b-111">You can configure which folders are indexed on the host as part of the Trim Transfer protocol, based on the host operating system.</span></span> <span data-ttu-id="a2a3b-112">Эти параметры задаются в файле *ClientSettings.xml* , который можно найти в папке **Server\\ Servers\\Configuration** .</span><span class="sxs-lookup"><span data-stu-id="a2a3b-112">These settings are configured in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="a2a3b-113">При применении новых параметров службу необходимо перезапустить.</span><span class="sxs-lookup"><span data-stu-id="a2a3b-113">When applying new settings, the service must be restarted.</span></span>

```xml
<HostIndexingXP type="System.String[]"> 
- <ArrayOfString>
<string>%WINDIR%</string> 
<string>%ProgramFiles%\Common Files</string> 
<string>%ProgramFiles%\Internet Explorer</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
<string>%ProgramFiles%\Windows NT</string> 
<string>%ProgramFiles%\Messenger</string> 
<string>%ProgramFiles%\Adobe</string> 
<string>%ProgramFiles%\Outlook Express</string> 
</ArrayOfString> 
</HostIndexingXP> 
- <HostIndexingVista type="System.String[]"> 
- <ArrayOfString> 
<string>%WINDIR%\MSAgent</string> 
<string>%WINDIR%\winsxs</string> 
<string>%WINDIR%\system</string> 
<string>%WINDIR%\system32</string> 
<string>%WINDIR%\Microsoft.NET</string> 
<string>%WINDIR%\SoftwareDistribution</string> 
<string>%WINDIR%\L2Schemas</string> 
<string>%WINDIR%\Cursors</string> 
<string>%WINDIR%\Boot</string> 
<string>%WINDIR%\Help</string> 
<string>%WINDIR%\assembly</string> 
<string>%WINDIR%\inf</string> 
<string>%WINDIR%\fonts</string> 
<string>%WINDIR%\Installer</string> 
<string>%WINDIR%\IME</string> 
<string>%WINDIR%\Resources</string> 
<string>%WINDIR%\servicing</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
</ArrayOfString> 
</HostIndexingVista>
```

 

 





