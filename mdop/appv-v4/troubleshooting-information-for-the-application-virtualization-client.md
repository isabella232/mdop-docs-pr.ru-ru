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
# Сведения об устранении неполадок в клиенте Application Virtualization


Этот раздел содержит сведения, которые можно использовать для устранения различных проблем в клиенте Application Virtualization (App-V).

## Обновление публикации происходит очень медленно


Если обновление публикации на определенном компьютере занимает больше времени, чем ожидалось, и если клиент настроен на использование параметра **IconSourceRoot** , определите, содержит ли **IconSourceRoot** недопустимый URL-адрес. Недопустимый URL-адрес приведет к очень долгой задержке при обновлении публикации.

## Пользователи не могут подключаться к серверу и переходить в режим разъединенных операций


Если вы используете сервер управления App-V, настроенный по протоколу RTSP, если пользователи не могут подключиться к сети и они переходят в режим отключенных операций, определите, является ли сертификат, используемый на сервере, действительным. Недействительный сертификат не позволит пользователям подключаться к сети и приведет к переходу в режим разъединенных операций.

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a>Производительность пользователей снижается, если приложения не полностью кэшируются


Если приложения не были полностью кэшированы, при запуске или использовании приложения пользователи могут иногда испытывать временную задержку или периодический доступ к производительности. Есть несколько причин, по которым это может произойти, например, когда клиент App-V находится в процессе автоматической загрузки приложения или при обработке запроса вне последовательности. Если приложения полностью кэшируются, эти проблемы больше не возникнут.

## <a href="" id="error-displayed-after-an-update-is-removed-"></a>После удаления обновления появляется сообщение об ошибке


Для удаления обновления из клиента App-V необходимо использовать правильный формат команды Windows Installer 3,1, как описано ниже.

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

Использование старого формата команд `msiexec /package <GUID> /uninstall <GUID>` вызовет ошибку 6003 "не удается запустить клиент Application Virtualization".

## Код ошибки 0A-0000E01E появляется при попытке запустить приложение


Код ошибки 0A-0000E01E указывает на то, что последовательный пакет приложения может быть поврежден. Решением является Переупорядочение пакета.

## Пользователи не могут получить доступ к созданным ими файлам на диске Q:


Если пользователи сохраняют файлы на диск **Q:** , они не смогут получить их, так как у них нет прав на чтение. Пользователи не должны сохранять файлы на диске **Q:** .

## У пользователя появляется сообщение об ошибке 1D1


Если URL-адрес потоковой передачи файлов задан неправильно в файле Open Software descriptor (OSD), клиент App-V возвращает ошибку 1d1 вместо ошибки "файл не найден". Эта ошибка указывает на то, что при запуске приложения произошел сбой, и пользователь принудительно переключается в режим разъединенных операций. Исправьте URL-адрес потоковой передачи файла.

## Неверные значки, связанные с некоторыми приложениями


Когда в операции публикации используется значок, клиент App-V сначала определяет, есть ли у него кэшированная копия значка, путем поиска в кэше значков для элемента, исходный путь которого совпадает с путем к значку, указанному в операции публикации. Если клиент App-V находит соответствие, он будет использовать уже кэшированный значок; в противном случае в кэш будет загружен новый значок. Если путь к значку является каталогом временных файлов или он повторно используется для новых значков или пакетов, поиск в кэше может выбрать неверный значок из предыдущей операции.

## Пользователи получают запрос на ввод учетных данных при запуске приложения.


Если пользователь попытается запустить виртуальное приложение, доступ к которому у системного администратора ограничен, пользователю может быть предложено ввести учетные данные. Пользователь должен ввести имя пользователя и пароль для учетной записи, у которой есть разрешение на запуск приложения, и нажать клавишу ВВОД.

## Обновление публикации завершается сбоем после обновления клиента App-V до версии 4,5


Если каталог данных пользователя был ранее помещен в нестандартное расположение (%*AllUsersProfile*%\\Documents\\SoftGrid Client\\Users\\%*username*%), пользователи, у которых нет прав администратора на компьютере, обнаружит, что обновление публикации завершается сбоем после обновления клиента App-V. Во время обновления каталог глобальных данных клиента App-V и все его подкаталоги настраиваются с ограниченными правами доступа только для администраторов. Вы можете избежать этой проблемы, изменив каталог данных пользователя перед обновлением, чтобы он не был подкаталогом глобального каталога данных.

## После сбоя установки требуется перезагрузка


Если по какой – либо причине не удается установить клиент и при последующих попытках установить клиент, проверьте, отображается ли в журнале установщика Windows сообщение об ошибке "sftplay Failed, Error = 1072". Если это так, перезагрузите компьютер, прежде чем пытаться установить клиент еще раз.

## Восстановление поврежденного виртуального приложения


Если по какой-либо причине виртуальный пакет приложения, установленный с использованием файла установщика Windows (MSI), повреждается, переустановите пакет. Функция восстановления, доступная в установщике Windows, не обновляет тома пользователей.

## Статьи по теме


[Справка по клиенту Application Virtualization](application-virtualization-client-reference.md)

 

 




