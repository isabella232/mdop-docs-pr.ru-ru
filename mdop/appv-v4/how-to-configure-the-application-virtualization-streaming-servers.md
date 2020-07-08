---
title: Настройка серверов Application Virtualization Streaming Server
description: Настройка серверов Application Virtualization Streaming Server
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817822"
---
# Настройка серверов Application Virtualization Streaming Server


Прежде чем виртуальные приложения можно будет передаваться в клиентское приложение Application Virtualization или клиент для служб удаленных рабочих столов (ранее — службы терминалов), необходимо настроить серверы потоковой виртуализации приложений. При настройке серверов вы настраиваете *каталог содержимого* , в котором загружаются и сохраняются файлы SFT. SFT-файлы содержат виртуальное приложение (или приложения).

**Важно!**  Серверы Application Virtualization поменяют SFT на Настольный клиент и клиент для служб удаленных рабочих столов, используя только протоколы RTSP или RTSP. Файл ICO (значок) и файл OSD (открыть программный дескриптор) можно настроить для потоковой передачи с другого файла или HTTP-сервера.

 

**Настройка серверов потоковой передачи Application Virtualization**

1.  Выполните процедуру установки для сервера потоковой передачи Application Virtualization. Во время процедуры установки вы указываете расположение каталога \\Content на экране " **путь к содержимому** ".

2.  Перейдите в расположение, указанное для каталога \\Content, и при необходимости создайте каталог.

3.  Когда создается каталог содержимого, настройте этот каталог как стандартный файловый общий доступ.

4.  Настройте разрешения файловой системы NTFS для каталога содержимого и папок пакета в каталоге содержимого. В доменных службах Active Directory следует использовать группы безопасности, определяющие, какие пользователи могут получать доступ к каждому приложению.

## Статьи по теме


[Сценарий на основе использования сервера Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Сценарий на основе электронного распространения программного обеспечения](electronic-software-distribution-based-scenario.md)

[Настройка серверов Application Virtualization Management Server](how-to-configure-the-application-virtualization-management-servers.md)

[Настройка файлового сервера](how-to-configure-the-file-server.md)

[Настройка сервера для служб IIS](how-to-configure-the-server-for-iis.md)

 

 





