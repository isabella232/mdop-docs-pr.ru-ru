---
title: Порядок создания или изменения MOF-файлов
description: Порядок создания или изменения MOF-файлов
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825322"
---
# Порядок создания или изменения MOF-файлов


Перед установкой средства администрирования и мониторинга Microsoft BitLocker (MBAM) с помощью Configuration Manager необходимо изменить файл Configuration. mof. Кроме того, необходимо либо изменить, либо создать файл SMS \ _def. mof в зависимости от используемой версии Configuration Manager.

## Изменение файла Configuration.mof


Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker с помощью отчетов Configuration Manager MBAM, необходимо изменить файл Configuration. mof для Microsoft System Center Configuration Manager 2007 и SystemCenter2012 ConfigurationManager.

[Изменение файла Configuration.mof](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Создание и изменение файла SMS \ _def. mof


Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker в отчетах Configuration Manager MBAM, необходимо создать или изменить файл SMS \ _def. mof. В Configuration Manager 2007 файл уже существует, поэтому вы должны изменить существующий файл, но не перезаписать его. Если вы используете SystemCenter2012 ConfigurationManager, необходимо создать файл.

[Создание и изменение файла SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md)

## Статьи по теме


[Развертывание MBAM с помощью диспетчера конфигураций](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





