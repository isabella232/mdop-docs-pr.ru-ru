---
title: Планирование развертывания сервера MBAM 2.5 Server
description: Планирование развертывания сервера MBAM 2.5 Server
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826212"
---
# Планирование развертывания сервера MBAM 2.5 Server


В этом разделе описаны возможности, которые вы развертываете для изолированных топологий MBAM и топологии Configuration Manager, и перечислены заказы, в которых они должны развертываться. Рекомендуемая конфигурация для каждой топологии. Однако вы можете настроить базы данных и компоненты сервера MBAM в различных конфигурациях и на нескольких серверах, в зависимости от требований к масштабируемости.

## Важные вопросы планирования для обеих топологий


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Довод</th>
<th align="left">Сведения или цель</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Прежде чем приступить к развертыванию, проверьте следующее:</p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Поддерживаемые конфигурации MBAM 2.5</a></p></li>
</ul></td>
<td align="left"><p>Каждая функция MBAM имеет определенные предварительные требования, которые должны быть выполнены перед началом установки MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ключи восстановления BitLocker в MBAM истекает после одного использования.</p></td>
<td align="left"><p>Это означает, что ключ восстановления был получен с помощью веб-сайта администрирования и мониторинга (также известного как служба поддержки), портала самообслуживания или с помощью <strong> </strong> командлета Windows PowerShell Get-MbamBitLockerRecoveryKey.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Следите за именами компьютеров, на которых настраивается каждая из этих функций. Эти сведения будут использоваться в ходе настройки.</p></td>
<td align="left"><p>Вы можете использовать <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"> Контрольный список развертывания MBAM 2,5 </a> для этой цели.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Настройте только параметры групповой политики на узле MDOP MBAM (Управление BitLocker). Не изменяйте параметры групповой политики в узле шифрования диска BitLocker.</p></td>
<td align="left"><p>Если изменить параметры групповой политики в узле шифрования диска BitLocker, MBAM не будет работать.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a>Планирование развертывания сервера MBAM — изолированная топология


Для изолированной топологии рекомендуется использовать конфигурацию из двух серверов для рабочих сред, несмотря на то, что могут использоваться конфигурации с тремя и четырьмя серверами.

Инфраструктура сервера для изолированной топологии MBAM включает следующие функции, которые должны быть настроены в указанном порядке:

1.  Базы данных (соответствие требованиям и база данных для проверки соответствия и базы данных восстановления)

2.  Отчеты

3.  Веб-приложения (и соответствующие им веб-службы)

    -   Веб-сайт администрирования и мониторинга

    -   Портал самообслуживания

Описание этих функций приведено в разделе [архитектура высокого уровня MBAM 2,5 с изолированной топологией](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a>Планирование развертывания сервера MBAM — топология Configuration Manager


Для топологии интеграции Configuration Manager для рабочих сред рекомендуется настроить конфигурацию с тремя серверами, но можно использовать настройки дополнительных серверов.

Серверная инфраструктура для топологии Configuration Manager MBAM включает следующие функции, которые необходимо настроить или выполнить в указанном порядке.

1.  Базы данных (соответствие требованиям и база данных для проверки соответствия и базы данных восстановления)

2.  Отчеты

3.  Веб-приложения (и соответствующие им веб-службы)

    -   Веб-сайт администрирования и мониторинга

    -   Портал самообслуживания

4.  Интеграция System Center Configuration Manager

Описание этих функций приведено в разделе [архитектура высокого уровня MBAM 2,5 с топологией интеграции Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).



## Статьи по теме


[Планирование развертывания MBAM 2.5](planning-to-deploy-mbam-25.md)

[Развертывание инфраструктуры сервера MBAM 2.5 Server](deploying-the-mbam-25-server-infrastructure.md)

 

## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





