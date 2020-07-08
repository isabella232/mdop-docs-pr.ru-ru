---
title: Обновление выпуска обновления для MBAM 2,5 до MBAM 2,5 SP1
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812768"
---
# Переход с MBAM 2,5 на MBAM 2,5 SP1 обслуживание выпуск обновление

В этой статье приведены пошаговые инструкции по обновлению администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5 для MBAM 2,5 с пакетом обновления 1 (SP1), а также [пакетом Microsoft Desktop Optimization (MDOP) может 2019 обновление обслуживания](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) в автономной конфигурации.

В этом руководстве мы будем использовать конфигурацию с двумя серверами. Один сервер является сервером баз данных, на котором работает Microsoft SQL Server 2016. На этом сервере будут размещены базы данных и отчеты MBAM. Другой сервер будет веб-сервером Windows Server 2012 R2. Этот сервер будет размещать "Администрирование и мониторинг" и "Портал самообслуживания".

## Подготовка к обновлению MBAM 2,5 SP1

### Знакомство с серверами MBAM в вашей среде

1. Ядро СУБД SQL Server: сервер, на котором размещены базы данных MBAM.
2. Службы SQL Server Reporting Services: сервер, на котором размещаются отчеты MBAM.
3. Веб-серверы служб IIS: сервер, на котором размещены веб-приложения MBAM и службы MBAM.
4. Необязательно Сервер основного сайта Microsoft System Center Configuration Manager: приложение конфигурации MBAM запущено на этом сервере для интеграции MBAM отчетов с Configuration Manager. Эти отчеты затем объединяются с существующими отчетами Configuration Manager в экземпляре служб SQL Server Reporting Services (SSRS).

### Определение учетных записей служб, групп, имени сервера и URL-адреса отчетов

1. Укажите учетную запись службы пула приложений MBAM, которая используется веб-серверами IIS для чтения и записи данных в MBAM базах данных.
2. Определите группы, которые используются при настройке веб-компонентов MBAM и URL-адресе.
3. Определение имени сервера SQL Server и имени экземпляра. Просмотрите это видео, чтобы узнать больше.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. Укажите учетную запись служб SQL Server Reporting Services, которая используется для чтения данных соответствия в базе данных соответствия требованиям и аудита. Просмотрите это видео, чтобы узнать больше.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## Обновление инфраструктуры MBAM до последней доступной версии

Установка или обновление инфраструктуры сервера MBAM всегда выполняется в указанном ниже порядке:

- Ядро СУБД SQL Server: базы данных
- Службы SQL Server Reporting Services: отчеты
- Веб-сервер: веб-приложения
- Сервер SCCM: интегрированные отчеты SCCM (если применимо)
- Клиенты: агент MBAM или клиентское обновление
- Шаблоны групповой политики: обновление существующей групповой политики с помощью новых шаблонов и включение новых параметров для существующей групповой политики MBAM

> [!NOTE]
> Перед запуском обновлений рекомендуется создать полную резервную копию базы данных MBAM.

### Обновление сервера SQL Server MBAM

Просмотрите этот видеоролик, чтобы получить сведения о том, как обновить SQL Server MBAM:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### Обновление веб-сервера MBAM

Просмотрите этот видеоролик, чтобы получить сведения о том, как обновить веб-сервер MBAM:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## Дополнительные сведения

Дополнительные сведения об известных проблемах в MBAM 2,5 с пакетом обновления 1 (SP1) можно найти в разделе [заметки о выпуске для MBAM 2,5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).
