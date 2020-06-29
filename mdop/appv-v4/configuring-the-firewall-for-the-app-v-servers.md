---
title: Настройка брандмауэра для серверов App-V Server
description: Настройка брандмауэра для серверов App-V Server
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821819"
---
# Настройка брандмауэра для серверов App-V Server


После установки сервера управления Microsoft Application Virtualization (App-V) или попотокового сервера в конфигурации для использования протокола RTSP или RTSP вы должны создать исключения брандмауэра для программ App-V.

## Настройка исключений брандмауэра для сервера управления виртуализацией приложений


Создайте исключение брандмауэра для **sghwdsptr.exe** и **sghwsvr.exe**. Эти программы находятся в папке C:\\program Files Files\\Microsoft System Center приложения virt Server\\App virt управление Server\\bin в 32-разрядной операционной системе. Если вы используете 64-разрядную версию операционной системы, она расположена в разделе C:\\program Files Files (x86) \\Microsoft System Center App Virt Management Server\\App virt Management Server\\bin.

## Настройка исключений брандмауэра для потокового сервера Application Virtualization


Создайте исключение брандмауэра для **sglwdsptr.exe** и **sglwsvr.exe**. Эти программы находятся в папке C:\\program Files Files\\Microsoft System Center приложения virt Streaming Server\\App virt Streaming Server\\bin в 32-разрядной операционной системе. Если вы используете 64-разрядную версию операционной системы, она расположена в разделе C:\\program Files Files (x86) \\Microsoft System Center App Virt Streaming Server\\App virt Streaming Server\\bin.

## Статьи по теме


[Настройка серверов для развертывания на основе сервера](how-to-configure-servers-for-server-based-deployment.md)

[Установка и настройка приложения по умолчанию](how-to-install-and-configure-the-default-application.md)

 

 





