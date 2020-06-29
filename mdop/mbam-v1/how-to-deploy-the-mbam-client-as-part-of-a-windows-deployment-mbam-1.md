---
title: Развертывание клиента MBAM в рамках развертывания Windows
description: Развертывание клиента MBAM в рамках развертывания Windows
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824912"
---
# Развертывание клиента MBAM в рамках развертывания Windows


Клиент администрирования и мониторинга Microsoft BitLocker (MBAM) позволяет администраторам принудительно применять и отслеживать шифрование диска BitLocker на компьютерах предприятия. Клиент BitLocker можно интегрировать в организацию, включив Управление BitLocker и шифрование на клиентских компьютерах во время создания образа компьютера и процесса развертывания Windows.

**Примечание.**  
Сведения о требованиях к системе клиента MBAM можно найти в разделе [Поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md).



Шифрование клиентских компьютеров с помощью BitLocker во время начальной стадии обработки образа в развертывании Windows может снизить затраты на администрирование MBAM реализации. Этот подход также гарантирует, что все развернутые компьютеры уже работают с BitLocker и настроены правильно.

**Warning**  
В этой статье описано, как изменить реестр Windows с помощью редактора реестра. Если изменить реестр Windows некорректно, это может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows. Перед изменением реестра необходимо создать резервную копию файлов реестра (System. dat и User. dat). Корпорация Майкрософт не несет ответственности за то, что проблемы, которые могут возникнуть при изменении реестра, могут быть устранены. Изменение реестра на свой страх и риск.



**Шифрование компьютера в рамках развертывания Windows**

1.  Если в вашей организации планируется использовать предохранитель доверенного платформенного модуля (TPM) или параметры предохранителя TPM + PIN-кода в BitLocker, необходимо активировать микросхему TPM перед начальным развертыванием MBAM. После активации микросхемы TPM вы не сможете перезагружаться позже в процессе, и вы убедитесь, что микросхемы TPM правильно настроены в соответствии с требованиями вашей организации. Микросхемы TPM необходимо активировать вручную в BIOS компьютера. Дополнительные сведения о настройке микросхемы TPM можно найти в документации изготовителя.

2.  Установите агент клиента MBAM.

3.  Мы рекомендуем присоединить компьютер к домену...

    -   Если компьютер не подключен к домену, пароль восстановления не хранится в службе восстановления ключа MBAM. По умолчанию MBAM не поддерживает шифрование, если не удается сохранить ключ восстановления.

    -   Если компьютер запускается в режиме восстановления, прежде чем ключ восстановления будет сохранен на сервере MBAM, необходимо переобразировать компьютер. Метод восстановления недоступен.

4.  Откройте командную команду от имени администратора, остановите службу MBAM и настройте ее на **ручной** или **по запросу**. Затем выполните следующие команды:

    **NET STOP mbamagent**

    **SC config mbamagent Start = Demand**

5.  Настройка параметров реестра для агента MBAM, чтобы игнорировать групповую политику и запустить доверенный платформенный модуль для **шифрования только** для этого, запустите **regedit**, а затем импортируйте шаблон раздела реестра из c:\\program Files Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

6.  В regedit перейдите на HKLM\\SOFTWARE\\Microsoft\\MBAM и настройте параметры, указанные в приведенной ниже таблице.

    Запись реестра

    Параметры конфигурации

    DeploymentTime

    0 = ВЫКЛ.

    1 = Использование параметров политики времени развертывания (по умолчанию)

    UseKeyRecoveryService

    0 = не использовать криптоключ ключа (в этом случае следующие два элемента реестра не требуются).

    1 = использование депонирования ключа в системе восстановления ключей (по умолчанию)

    Рекомендуется: компьютер должен поддерживать связь с службой восстановления ключей. Убедитесь, что компьютер может взаимодействовать со службой, прежде чем продолжить.

    KeyRecoveryOptions

    0 = загрузить только ключ восстановления

    1 = Отправка ключа восстановления и пакета восстановления ключа (по умолчанию)

    KeyRecoveryServiceEndPoint

    Задайте для этого параметра URL-адрес веб – сервера восстановления ключей.

    Пример: http:// &lt; имя компьютера &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. Агент MBAM перезапускает систему во время развертывания клиента MBAM. Когда вы будете готовы к перезагрузке, выполните в командной строке в качестве администратора следующую команду:

   **NET start mbamagent**

8. После перезапуска компьютера и BIOS, предложит вам изменить доверенный платформенный модуль, подтвердите изменение.

9. Когда вы будете готовы начать шифрование, перезапустите службу агента MBAM на этапе обработки образа операционной системы клиента Windows. Затем, чтобы установить **Автоматический**запуск, откройте командную команду от имени администратора и выполните следующие команды:

   **SC config mbamagent Start = Auto**

   **NET start mbamagent**

10. Удалите значения из раздела "пропустить". Для этого запустите regedit, перейдите в раздел реестра HKLM\\SOFTWARE\\Microsoft, щелкните правой кнопкой мыши узел **MBAM** и выберите команду **Удалить**.

## Статьи по теме


[Развертывание клиента MBAM 1.0](deploying-the-mbam-10-client.md)








