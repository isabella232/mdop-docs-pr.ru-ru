---
title: Настройка клиента для включения режима изолированной работы
description: Настройка клиента для включения режима изолированной работы
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817819"
---
# Настройка клиента для включения режима изолированной работы


Режим разъединенных операций включает клиентское приложение Application Virtualization (App-V) или клиент Application Virtualization (App-V) для служб удаленных рабочих столов (ранее — служб терминалов) для запуска приложений, которые хранятся в кэше файловой системы клиента, когда клиент не может подключиться к серверу управления App-V.

**Важно!**  В крупной организации, где несколько серверов сеансов удаленных рабочих столов (на которых раньше настольных серверов) подключены к ферме для поддержки множества пользователей, использование единого сервера управления App-V для поддержки фермы представляет единственную точку сбоя. Для обеспечения высокого уровня доступности для поддержки фермы узла RDSession рассматривайте возможность связывания двух или более серверов управления App-V для использования одной базы данных.

 

**Включение режима разъединенных операций**

-   Установите для следующего раздела реестра значение 1, чтобы включить режим разъединенных операций:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation

**Чтобы установить ограничение по времени в режиме отключенной операции, используйте**

1.  Задайте для следующего раздела реестра значение 1:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation

2.  Задайте для значения в следующем разделе реестра количество минут, в течение которых вы хотите ограничить режим автономной работы. Допустимый диапазон значений: 1 – 999999. Значение по умолчанию — 90 дней или 129 600 минут.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes

**Настройка клиента для служб удаленных рабочих столов для отключения режима работы**

1.  Установите для следующего раздела реестра значение 1, чтобы включить режим отключенной работы.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation

2.  Установите для следующего параметра реестра значение 0 (ноль), чтобы разрешить неограниченный режим работы отключенной операции:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation

3.  Убедитесь, что все пакеты предварительно загружены в кэш для повышения производительности.

## Статьи по теме


[Режим изолированной работы](disconnected-operation-mode.md)

[Настройка параметров реестра клиента App-V с помощью командной строки](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





