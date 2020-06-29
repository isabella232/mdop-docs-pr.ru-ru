---
title: Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций
description: Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812565"
---
# Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций


Если вы устанавливаете администрирование и мониторинг Microsoft BitLocker (MBAM) 2,5 с помощью функции интеграции System Center Configuration Manager, необходимо выполнить предварительные требования, описанные в этой статье, в дополнение к [требованиям для топологии интеграции с отдельными службами и топологией Configuration Manager для MBAM 2,5 Server](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md). Кроме того, необходимо создать или изменить файлы. mof, необходимые для топологии интеграции Configuration Manager.

## Необходимые условия для компонента интеграции диспетчера конфигураций


Если вы настраиваете MBAM с помощью топологии интеграции System Center Configuration Manager, необходимо выполнить дополнительные требования, необходимые для Configuration Manager.

[Необходимые условия для компонента интеграции диспетчера конфигураций](prerequisites-for-the-configuration-manager-integration-feature.md)

## Изменение файла Configuration. mof


Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker с помощью отчетов Configuration Manager MBAM, необходимо изменить файл Configuration. mof для SystemCenter2012 ConfigurationManager и Microsoft System Center Configuration Manager 2007.

[Изменение файла Configuration.mof](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Создание и изменение файла SMS \ _def. mof


Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker в отчетах Configuration Manager MBAM, необходимо создать или изменить файл SMS \ _def. mof. Если вы используете SystemCenter2012 ConfigurationManager, необходимо создать файл. В Configuration Manager 2007 файл уже существует, поэтому вы должны изменить существующий файл, но не перезаписать его.

[Создание и изменение файла SMS \ _def. mof](create-or-edit-the-sms-defmof-file-mbam-25.md)


## Статьи по теме


[Подготовка среды для развертывания MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Поддерживаемые конфигурации MBAM 2.5](mbam-25-supported-configurations.md)

[Планирование развертывания MBAM 2.5](planning-to-deploy-mbam-25.md)

 

 
## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




