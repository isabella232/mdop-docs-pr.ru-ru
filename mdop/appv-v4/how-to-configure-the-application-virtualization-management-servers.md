---
title: Настройка серверов Application Virtualization Management Server
description: Настройка серверов Application Virtualization Management Server
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817842"
---
# Настройка серверов Application Virtualization Management Server


Перед тем, как виртуализированные приложения будут передаваться в клиентское приложение Application Virtualization или клиент для служб удаленных рабочих столов (ранее — службы терминалов), необходимо настроить сервер управления виртуализацией приложений. При настройке сервера вы настраиваете *каталог содержимого* , в котором загружаются и сохраняются файлы SFT. SFT-файлы содержат виртуализированное приложение (или приложения).

**Важно!**  Серверы Application Virtualization поменяют SFT на Настольный клиент и клиент для служб удаленных рабочих столов, используя только протоколы RTSP или RTSP. Файл ICO (значок) и файл OSD (открыть программный дескриптор) можно настроить для потоковой передачи с другого файла или HTTP-сервера.

 

**Настройка сервера управления виртуализацией приложений**

1.  Выполните описанные ниже действия.

    [Установка сервера Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)

    **Примечание**  Во время процедуры установки вы указываете расположение каталога \\Content на экране " **путь к содержимому** ".

     

2.  Перейдите в расположение, указанное для каталога \\Content, и при необходимости создайте каталог.

3.  Когда создается каталог содержимого, настройте этот каталог как стандартный файловый общий доступ.

## Статьи по теме


[Сценарий на основе использования сервера Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Требования к системе при работе с Application Virtualization](application-virtualization-system-requirements.md)

[Сценарий на основе электронного распространения программного обеспечения](electronic-software-distribution-based-scenario.md)

[Настройка серверов для развертывания на основе сервера](how-to-configure-servers-for-server-based-deployment.md)

 

 





