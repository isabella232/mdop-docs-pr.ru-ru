---
title: Настройка сервера для служб IIS
description: Настройка сервера для служб IIS
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817742"
---
# Настройка сервера для служб IIS


Прежде чем виртуальные приложения будут передаваться в клиентское приложение Application Virtualization и клиент для служб удаленных рабочих столов (ранее — службы терминалов), необходимо настроить серверы IIS. При настройке серверов вы настраиваете каталог содержимого, в котором загружаются и сохраняются файлы SFT. SFT-файлы содержат виртуальное приложение (или приложения).

**Настройка каталога содержимого на сервере IIS**

1.  На сервере, на котором запущены службы IIS, найдите каталог, который вы хотите использовать в качестве каталога содержимого, или создайте каталог, если он не существует. Настройте этот каталог как стандартный файловый общий доступ.

2.  На сервере, на котором запущены службы IIS, откройте **Диспетчер IIS**и на веб-сайте по умолчанию создайте виртуальный каталог, соответствующий каталогу содержимого, созданному на сервере. Убедитесь, что флажок **Read (чтение** ) установлен.

3.  Присвойте созданному виртуальному каталогу **содержимое**псевдонимов.

4.  Подтвердите все другие параметры по умолчанию для этого виртуального каталога.

5.  Настройте разрешения файловой системы NTFS для каталога содержимого и папок пакета в каталоге содержимого с помощью групп безопасности в доменных службах Active Directory, определенных ранее.

**Примечание**  Если для публикации ICO-и OSD-файлов используется IIS, необходимо настроить тип MIME для OSD = TXT; в противном случае службы IIS не будут обрабатывать файлы ICO и OSD для клиентов. Если вы используете IIS для публикации пакетов (SFT-файлов), необходимо настроить тип MIME для SFT = binary. в противном случае службы IIS не будут обрабатывать файлы SFT для клиентов.

 

## Статьи по теме


[Сценарий на основе использования сервера Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Сценарий на основе электронного распространения программного обеспечения](electronic-software-distribution-based-scenario.md)

[Настройка серверов Application Virtualization Management Server](how-to-configure-the-application-virtualization-management-servers.md)

[Настройка серверов Application Virtualization Streaming Server](how-to-configure-the-application-virtualization-streaming-servers.md)

[Настройка файлового сервера](how-to-configure-the-file-server.md)

 

 





