---
title: Высокоуровневая архитектура для MBAM 2.0
description: Высокоуровневая архитектура для MBAM 2.0
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824702"
---
# Высокоуровневая архитектура для MBAM 2.0


Администрирование и мониторинг Microsoft BitLocker (MBAM) — это решение между клиентом и сервером, которое помогает упростить подготовку и развертывание BitLocker, улучшить соответствие требованиям и создавать отчеты на BitLocker и сократить расходы на поддержку. Администрирование и мониторинг Microsoft BitLocker включают функции, описанные в этом разделе.

Администрирование и мониторинг Microsoft BitLocker можно развертывать в изолированной топологии или в топологии, интегрированной с Microsoft System Center Configuration Manager 2007 или MicrosoftSystemCenter2012 ConfigurationManager. В этом разделе описана архитектура изолированной топологии. Сведения о развертывании в топологии интегрированного Configuration Manager можно найти в разделе [Использование MBAM в Configuration Manager](using-mbam-with-configuration-manager.md).

На приведенной ниже схеме показана Рекомендуемая архитектура MBAM для рабочей среды, которая состоит из двух серверов и рабочей станции управления. Эта архитектура поддерживает до 200 000 MBAM клиентов. Серверные функции и базы данных на изображении архитектуры описаны в следующем разделе и указаны в списке под компьютером или сервером, где они рекомендуются для их установки.

**Примечание**  Архитектура с одним сервером следует использовать только в тестовых средах.

 

![MBAM 2 2 — топология развертывания сервера](images/mbam2-3-servers.gif)

## Сервер администрирования и мониторинга


На этом сервере установлены следующие компоненты:

-   **Сервер администрирования и наблюдения**. Сервер администрирования и мониторинга установлен на сервере Windows и включает веб-сайт администрирования и наблюдения, включающий отчеты и портал службы поддержки и веб-службы мониторинга.

-   **Портал самообслуживания**. Портал самообслуживания установлен на сервере Windows. Портал самообслуживания позволяет конечным пользователям на клиентских компьютерах независимо входить на веб-сайт, где они могут получить ключ восстановления для восстановления заблокированного тома BitLocker.

## Сервер базы данных


На этом сервере установлены следующие компоненты:

-   **Базу данных восстановления**. База данных восстановления устанавливается на сервере Windows и поддерживаемом экземпляре Microsoft SQLServer. Эта база данных хранит данные для восстановления, собранные из клиентских компьютеров MBAM.

-   **База данных соответствия требованиям и аудита**. База данных соответствия и аудита установлена на сервере Windows и поддерживаемом экземпляром SQLServer. Эта база данных хранит данные соответствия требованиям для клиентских компьютеров MBAM. Эти данные используются преимущественно для отчетов, которые являются узлами служб SQL Server Reporting Services (SSRS).

-   **Отчеты о соответствии и аудите**. Отчеты о соответствии и аудите устанавливаются на сервере Windows и поддерживаемом экземпляром SQLServer, на котором установлена функция служб SQL Server Reporting Services (SSRS). Эти отчеты предоставляют отчеты MBAM, к которым можно получить доступ с веб-сайта администрирования и мониторинга либо непосредственно с сервера служб SSRS.

## Рабочая станция для управления


Следующий компонент установлен на рабочей станции управления, которая может быть Windows Server или клиентским компьютером.

-   **Шаблон политики**. Шаблон политики состоит из параметров групповой политики, которые определяют параметры реализации MBAM для шифрования диска BitLocker. Вы можете установить шаблон политики на любой сервер или рабочую станцию, но это значит, что он обычно установлен на рабочей станции управления, который является поддерживаемым сервером Windows или клиентским компьютером. Рабочая станция не должна быть выделенным компьютером.

## <a href="" id="---------mbam-client"></a> Клиент MBAM


Клиент MBAM установлен на компьютере с Windows и обладает следующими характеристиками:

-   Использование групповой политики для принудительного шифрования диска BitLocker на клиентских компьютерах в сети.

-   Собирает ключ восстановления для трех типов дисков данных BitLocker: диски операционной системы, несъемные диски с данными и съемные носители данных (USB).

-   Собирает данные о соответствии для компьютера и передает их в систему отчетности.

## Статьи по теме


[Начало работы с MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 




