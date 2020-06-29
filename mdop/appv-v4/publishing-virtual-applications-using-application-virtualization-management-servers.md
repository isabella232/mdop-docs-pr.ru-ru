---
title: Публикация виртуальных приложений с помощью серверов Application Virtualization Management Server
description: Публикация виртуальных приложений с помощью серверов Application Virtualization Management Server
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815769"
---
# Публикация виртуальных приложений с помощью серверов Application Virtualization Management Server


В развертывании на базе сервера Application Virtualization пакеты виртуальных приложений, которые были последовательно, проверены и обнаружены, будут скопированы в основную доступную для использования сервер управления Application Virtualization. После импорта пакетов на сервер управления Application Virtualization они могут быть опубликованы для конечных пользователей.

**Примечание**  Общий доступ к КОНТЕНТу должен находиться на дисках, подключенных к серверу. Использование сетевого запоминающего устройства, такого как сеть хранения данных или общий доступ к распределенной файловой сети DFS, должно быть тщательно рассмотрено из-за воздействия на сеть.

 

Приложения загружаются в группы Active Directory. Обычно администратор Application Virtualization создает группы Active Directory для каждого виртуального приложения, которые нужно опубликовать, а затем добавляет в них соответствующих пользователей. Когда пользователи выполняют вход на рабочие станции, клиент Application Virtualization по умолчанию выполняет обновление публикации с использованием учетных данных пользователя, выполнившего вход. После этого пользователь сможет запускать приложения из любой точки, куда вы находились сочетания клавиш. Администратор Application Virtualization определяет, где и сколько сочетаний клавиш находится на клиентском компьютере во время последовательного выполнения приложения.

**Примечание**  *Обновление публикации* — это звонок на сервер Application Virtualization, который определен в клиенте Application Virtualization, чтобы определить, какие из виртуальных приложений отправляются клиенту для использования конечным пользователем.

 

## Статьи по теме


[Сценарий на основе использования сервера Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Публикация виртуального приложения на клиенте](how-to-publish-a-virtual-application-on-the-client.md)

[Обзор компонентов системы Application Virtualization](overview-of-the-application-virtualization-system-components.md)

[Планирование решения для потоковой передачи при внедрении на основе сервера Application Virtualization Server](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 





