---
title: Microsoft BitLocker Administration and Monitoring 2.5
description: Microsoft BitLocker Administration and Monitoring 2.5
author: dansimp
ms.assetid: fd81d7de-b166-47e8-b6c7-d984830762b6
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 2e5243131853207f0ed3cbb6d0cd8fb8e3d56108
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795890"
---
# Microsoft BitLocker Administration and Monitoring 2.5

Администрирование и мониторинг Microsoft BitLocker (MBAM) 2,5 предоставляет упрощенный интерфейс администрирования, который можно использовать для управления шифрованием диска BitLocker. Вы настраиваете шаблоны групповой политики MBAM, которые позволяют настраивать параметры политики шифрования диска BitLocker, подходящие для вашего предприятия, а затем используйте их для отслеживания соответствия требованиям клиентов этим политикам. Вы также можете сообщить о состоянии шифрования отдельного компьютера и всего предприятия. Кроме того, вы можете получить доступ к сведениям о ключе восстановления, когда пользователь забыл свой PIN-код или пароль, а также при изменении BIOS или загрузочной записи. Более подробное описание MBAM можно найти в разделе [о MBAM 2,5](about-mbam-25.md).

Чтобы получить MBAM, ознакомьтесь со [статьей получение MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).

## Структуры

- <a href="" id="getting-started-with-mbam-2-5"></a>[Начало работы с MBAM 2.5](getting-started-with-mbam-25.md)
  - [О программе MBAM 2.5](about-mbam-25.md)
  - [Заметки о выпуске для MBAM 2.5](release-notes-for-mbam-25.md)
  - [Сведения о программе MBAM 2.5 с пакетом обновления 1 (SP1)](about-mbam-25-sp1.md)
  - [Заметки о выпуске MBAM 2.5 с пакетом обновления 1 (SP1)](release-notes-for-mbam-25-sp1.md)
  - [Оценка MBAM 2.5 в тестовой среде](evaluating-mbam-25-in-a-test-environment.md)
  - [Высокоуровневая архитектура для MBAM 2.5](high-level-architecture-for-mbam-25.md)
  - [Специальные возможности для MBAM 2.5](accessibility-for-mbam-25.md)
- <a href="" id="planning-for-mbam-2-5"></a>[Планирование для MBAM 2.5](planning-for-mbam-25.md)
  - [Подготовка среды для развертывания MBAM 2.5](preparing-your-environment-for-mbam-25.md)
  - [Необходимые условия для развертывания MBAM 2.5](mbam-25-deployment-prerequisites.md)
  - [Планирование требований групповой политики MBAM 2.5](planning-for-mbam-25-group-policy-requirements.md)
  - [Планирование групп и учетных записей MBAM 2.5](planning-for-mbam-25-groups-and-accounts.md)
  - [Планирование защиты веб-сайтов MBAM](planning-how-to-secure-the-mbam-websites.md)
  - [Планирование развертывания MBAM 2.5](planning-to-deploy-mbam-25.md)
  - [Поддерживаемые конфигурации MBAM 2.5](mbam-25-supported-configurations.md)
  - [Планирование высокой доступности MBAM 2.5](planning-for-mbam-25-high-availability.md)
  - [Процедуры безопасности MBAM 2.5](mbam-25-security-considerations.md)
  - [Контрольный список планирования MBAM 2.5](mbam-25-planning-checklist.md)
- <a href="" id="deploying-mbam-2-5"></a>[Развертывание MBAM 2.5](deploying-mbam-25.md)
  - [Развертывание инфраструктуры сервера MBAM 2.5 Server](deploying-the-mbam-25-server-infrastructure.md)
  - [Развертывание объектов групповой политики MBAM 2.5](deploying-mbam-25-group-policy-objects.md)
  - [Развертывание клиента MBAM 2.5](deploying-the-mbam-25-client.md)
  - [Контрольный список необходимых компонентов развертывания MBAM 2.5](mbam-25-deployment-checklist.md)
  - [Обновление с предыдущих версий до MBAM 2.5 или MBAM 2.5 с пакетом обновления 1 (SP1)](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)
  - [Удаление компонентов или программного обеспечения MBAM Server](removing-mbam-server-features-or-software.md)
- <a href="" id="operations-for-mbam-2-5"></a>[Операции MBAM 2.5](operations-for-mbam-25.md)
  - [Администрирование компонентов MBAM 2.5](administering-mbam-25-features.md)
  - [Мониторинг и создание отчетов по соответствию BitLocker с помощью MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)
  - [Управление BitLocker с помощью MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)
  - [Обслуживание MBAM 2.5](maintaining-mbam-25.md)
  - [Использование Windows PowerShell для администрирования MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md)
- <a href="" id="troubleshooting-mbam-2-5"></a>[Устранение неполадок MBAM 2.5](troubleshooting-mbam-25.md)
- <a href="" id="technical-reference-for-mbam-2-5"></a>[Технический справочник по MBAM 2.5](technical-reference-for-mbam-25.md)
  - [Журналы событий клиента](client-event-logs.md)
  - [Журналы событий сервера](server-event-logs.md)

## Дополнительные сведения

- [Информационные функции для MDOP](index.md)

  Ознакомьтесь с документацией, видеороликами и прочими материалами, посвященными технологиям MDOP.

- [Руководство по развертыванию MBAM](https://www.microsoft.com/download/details.aspx?id=38398)

  Получите помощь в выборе метода развертывания для MBAM, в том числе пошаговых инструкций для каждого из этих методов.
    
- [Установка исправлений на сервере MBAM 2,5 с пакетом обновления 1 (SP1)](apply-hotfix-for-mbam-25-sp1.md)

  Руководство по применению исправлений сервера MBAM 2,5 SP1
