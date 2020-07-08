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
# Технология передачи усеченных данных MED-V


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


Улучшенная технология отмены и дублирования данных в MED-V ускоряет загрузку первоначальных и обновленных образов виртуальных машин через ЛОКАЛЬную сеть или глобальную сеть, тем самым уменьшая пропускную способность сети для передачи виртуальной машины MED-V Workspace нескольким конечным пользователям.

Эта революционная технология использует существующие локальные данные для создания образа виртуальной машины, используя тот факт, что в большинстве случаев большинство виртуальных машин (например, системы и файлы приложений) уже есть на диске конечного пользователя. Например, если виртуальная машина, содержащая WindowsXP, доставляется клиенту с локальной копией WindowsXP, MED-V автоматически удалит избыточные элементы WindowsXP из передачи. Для обеспечения правильной и функциональной рабочей области клиент MED-V криптографически проверяет целостность локальных данных перед использованием, гарантируя, что локальные блоки данных находятся в незашифрованном виде, точно так же, как и в нужном образе виртуальной машины. Несовпадающие блоки не используются.

Процесс — это эффективная и прозрачная пропускная способность и передача данных в фоновом режиме с использованием неиспользуемых ресурсов сети и ЦП.

При переходе к новой версии изображения (например, когда администраторы хотят распространять новое приложение или исправление) загружаются только те элементы, которые были изменены ("Разное"), а не вся виртуальная машина, что значительно уменьшает требуемую пропускную способность сети и время доставки.

Вы можете настроить Индексирование папок на узле в рамках протокола передачи обрезки, зависящего от операционной системы узла. Эти параметры задаются в файле *ClientSettings.xml* , который можно найти в папке **Server\\ Servers\\Configuration** .

При применении новых параметров службу необходимо перезапустить.

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

 

 





