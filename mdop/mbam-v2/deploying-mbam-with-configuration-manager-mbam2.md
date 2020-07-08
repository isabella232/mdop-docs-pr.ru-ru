---
title: Развертывание MBAM с помощью диспетчера конфигураций
description: Развертывание MBAM с помощью диспетчера конфигураций
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823452"
---
# Развертывание MBAM с помощью диспетчера конфигураций


Ниже описано, как развернуть администрирование и мониторинг Microsoft BitLocker (MBAM) в Microsoft System Center Configuration Manager 2007 или MicrosoftSystemCenter2012 ConfigurationManager с помощью usingthe рекомендованной конфигурации, описанной в разделе [Приступая к работе с помощью диспетчера конфигураций](getting-started---using-mbam-with-configuration-manager.md). Рекомендуемая конфигурация — Установка функций администрирования и наблюдения на одном или нескольких серверах администрирования и мониторинга Microsoft BitLocker и установка Microsoft System Center Configuration Manager 2007 или MicrosoftSystemCenter2012 ConfigurationManager на отдельном сервере.

Перед началом установки убедитесь, что у вас есть необходимые условия и требования к оборудованию и программному обеспечению для установки MBAM с помощью Configuration Manager, проверив [Планирование развертывания MBAM с помощью Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

Если вы когда-либо переустанавливаете MBAM с топологией Configuration Manager, необходимо сначала удалить некоторые объекты Configuration Manager. Дополнительные сведения читайте в [статье базы знаний](https://go.microsoft.com/fwlink/?LinkId=286306) .

Инструкции по установке MBAM с помощью Configuration Manager сгруппированы по следующим категориям. Выполните эти действия для каждой категории, чтобы завершить установку.

## Порядок создания или изменения MOF-файлов


Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker с помощью отчетов Configuration Manager MBAM, необходимо изменить файл **Configuration. mof** , а также изменить или создать файл Sms \ _def. mof в зависимости от того, какая версия Configuration Manager используется.

[Порядок создания или изменения MOF-файлов](how-to-create-or-edit-the-mof-files.md)

## Порядок установки MBAM с помощью диспетчера конфигураций


В этом разделе приводятся инструкции по установке следующих параметров: MBAM на сервере Configuration Manager. Базы данных восстановления и аудита на сервере базы данных; а также на сервере администрирования и мониторинга доступны серверные функции администрирования и мониторинга.

[Порядок установки MBAM с помощью диспетчера конфигураций](how-to-install-mbam-with-configuration-manager.md)

## Проверка установки компонентов сервера MBAM на сервере Configuration Manager


После завершения установки администрирования и наблюдения за помощью Microsoft BitLocker убедитесь, что установка успешно завершила настройку всех необходимых функций MBAM, необходимых для сервера Configuration Manager.

[Порядок проверки установки MBAM с помощью диспетчера конфигураций](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## Статьи по теме


[Использование MBAM с диспетчером конфигураций](using-mbam-with-configuration-manager.md)

 

 





