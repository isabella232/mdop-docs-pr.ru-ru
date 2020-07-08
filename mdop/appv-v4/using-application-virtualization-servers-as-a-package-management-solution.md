---
title: Использование серверов Application Virtualization Server в качестве решения по управлению пакетами
description: Использование серверов Application Virtualization Server в качестве решения по управлению пакетами
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815122"
---
# Использование серверов Application Virtualization Server в качестве решения по управлению пакетами


Если у вас нет существующей системы ESD для развертывания решения Application Virtualization или вы не хотите использовать его, вам потребуется установить один или несколько серверов управления виртуализацией приложений в качестве ядра архитектуры системы. Для сервера управления Application Virtualization требуется выделенный серверный компьютер и нужна база данных Microsoft SQL Server. База данных может находиться на том же сервере или быть настроена на корпоративном сервере базы данных, доступном для сервера управления виртуализацией приложений по высокоскоростному подключению к локальной сети. Кроме того, вам потребуется установить консоль управления виртуализации приложений (Майкрософт) либо на сервере управления виртуализацией приложений, либо на назначенной рабочей станции управления, и вам потребуется установить веб-службу Microsoft Application Virtualization, которая также может быть установлена на сервере управления виртуализацией приложений или на отдельном сервере IIS. Консоль управления виртуализацией приложений используется для подключения к веб-службе управления виртуализацией приложений, что позволяет системному администратору взаимодействовать с сервером управления виртуализацией приложений.

**Примечание**  Управление доступом к приложениям осуществляется с помощью групп безопасности доменных служб Active Directory, поэтому вам потребуется планировать процесс настройки группы безопасности для каждого виртуализированного приложения и для управления добавлением пользователей в каждую группу. Администратор сервера управления виртуализацией приложений настраивает сервер для использования этих групп Active Directory, а затем сервер автоматически контролирует доступ к пакетам на основе членства в группе Active Directory.

 

## В этом разделе


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[Обзор компонентов системы Application Virtualization](overview-of-the-application-virtualization-system-components.md)  
Список и описание основных компонентов системы управления виртуализацией приложений Microsoft.

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[Публикация виртуальных приложений с помощью серверов Application Virtualization Management Server](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
В этом кратком обзоре описаны способы публикации виртуальных приложений в сценарии развертывания на основе сервера Application Virtualization.

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[Планирование решения для потоковой передачи при внедрении на основе сервера Application Virtualization Server](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
В этой статье описаны доступные параметры для использования серверных потоков виртуализации приложений вместе с реализацией на основе сервера управления виртуализацией приложений.

## Статьи по теме


[Сценарий на основе использования сервера Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Планирование развертывания системы виртуализации приложений](planning-for-application-virtualization-system-deployment.md)

 

 





