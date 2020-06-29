---
title: Развертывание клиента MBAM на настольных компьютерах и ноутбуках
description: Развертывание клиента MBAM на настольных компьютерах и ноутбуках
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824479"
---
# Развертывание клиента MBAM на настольных компьютерах и ноутбуках


В этой статье объясняется, как развернуть клиент MBAM на компьютерах конечных пользователей. Вы можете развернуть клиент MBAM с помощью электронной системы распространения программного обеспечения, например доменных служб Active Directory или MicrosoftSystemCenterConfiguration Manager.

Чтобы развернуть клиент MBAM в рамках развертывания Windows, Узнайте, [как включить BitLocker с помощью MBAM в составе развертывания Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).

Прежде чем приступить к развертыванию клиента MBAM, проверьте [конфигурации, поддерживаемые MBAM 2,5](mbam-25-supported-configurations.md).

**Развертывание клиента MBAM на настольном компьютере или ноутбуке**

1.  Найдите установочные файлы клиента MBAM, которые предоставляются вместе с программным обеспечением MBAM.

2.  Использование доменных служб Active Directory или средства корпоративного развертывания программного обеспечения, например диспетчера MicrosoftSystemCenterConfiguration Manager, для развертывания пакета установщика Windows на целевые компьютеры.

3.  Настройте параметры распространения или параметры групповой политики, чтобы запустить установочный файл клиента MBAM.

    После успешной установки клиент MBAM применяет параметры групповой политики, полученные от контроллера домена, для запуска функций шифрования диска BitLocker и управления ими.

    **Важно!**  Клиент MBAM не запускает действия по шифрованию диска BitLocker при активном соединении с протоколом удаленного рабочего стола. Чтобы начать шифрование диска BitLocker, необходимо закрыть все соединения с удаленной консолью и войти в систему с помощью физического сеанса консоли.

     


## Статьи по теме
[Развертывание клиента MBAM 2.5](deploying-the-mbam-25-client.md)

[Планирование развертывания клиента MBAM 2.5](planning-for-mbam-25-client-deployment.md)

 

## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





