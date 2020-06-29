---
title: Развертывание клиента MBAM в рамках развертывания Windows
description: Развертывание клиента MBAM в рамках развертывания Windows
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824622"
---
# Развертывание клиента MBAM в рамках развертывания Windows


Клиент администрирования и мониторинга Microsoft BitLocker (MBAM) позволяет администраторам принудительно применять и отслеживать шифрование диска BitLocker на компьютерах предприятия. Если компьютеры с микросхемой доверенного платформенного модуля (TPM), клиент BitLocker можно интегрировать в организацию, включив Управление BitLocker и шифрование на клиентских компьютерах в рамках процесса создания образа и развертывания Windows.

**Примечание.**  
Сведения о требованиях к клиентским системам администрирования и мониторинга Microsoft BitLocker можно найти в разделе [Поддерживаемые конфигурации MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).



Шифрование клиентских компьютеров с помощью BitLocker во время начальной стадии обработки образа в развертывании Windows может снизить затраты на администрирование, необходимые для реализации MBAM в Организации. Кроме того, это гарантирует, что все развернутые компьютеры уже работают с BitLocker и настроены правильно.

**Примечание.**  
В этом разделе описана процедура изменения реестра Windows. Неправильное использование редактора реестра может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows. Корпорация Майкрософт не гарантирует, что проблемы, возникающие в результате неправильного использования редактора реестра, могут быть устранены. Ответственность за использование редактора реестра.



**Шифрование компьютера в рамках развертывания Windows**

1.  Если в вашей организации планируется использовать предохранитель доверенного платформенного модуля (TPM) или параметры предохранителя TPM + PIN-кода в BitLocker, необходимо активировать микросхему TPM перед начальным развертыванием MBAM. После активации микросхемы TPM вы не сможете перезагружаться позже в процессе, и вы убедитесь, что микросхемы TPM правильно настроены в соответствии с требованиями вашей организации. Вы должны активировать микросхему доверенного платформенного модуля вручную в BIOS компьютера.

    **Примечание.**  
    Некоторые поставщики предоставляют средства для включения и активации микросхемы TPM в BIOS в операционной системе. Дополнительные сведения о настройке микросхемы TPM можно найти в документации изготовителя.



2.  Установите агент клиента администрирования и мониторинга Microsoft BitLocker.

3.  Присоединение компьютера к домену (рекомендуется).

    -   Если компьютер не подключен к домену, пароль восстановления не хранится в службе восстановления ключа MBAM. По умолчанию MBAM не поддерживает шифрование, если не удается сохранить ключ восстановления.

    -   Если компьютер запускается в режиме восстановления, прежде чем ключ восстановления будет сохранен на сервере MBAM, необходимо переобразировать компьютер. Метод восстановления недоступен.

4.  Запустите командную строку от имени администратора, остановите службу MBAM и настройте ее **вручную** или **по запросу**, а затем начните с ввода следующих команд:

    **NET STOP mbamagent**

    **SC config mbamagent Start = Demand**

5.  Настройте параметры реестра для агента MBAM, чтобы игнорировать групповую политику и выполнить **шифрование только для операционной системы** , запустив **regedit**, а затем импортируйте шаблон раздела реестра из c:\\program Files Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

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

    0 = Отправка только ключа восстановления

    1 = Отправка ключа восстановления и пакета восстановления ключа (по умолчанию)

    KeyRecoveryServiceEndPoint

    Задайте для этого параметра URL-адрес веб – сервера восстановления ключа (например, http:// &lt; имя компьютера &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.).



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. Агент MBAM перезапускает систему во время развертывания клиента MBAM. Когда вы будете готовы к перезагрузке, выполните в командной строке в качестве администратора следующую команду:

   **NET start mbamagent**

8. После перезапуска компьютера и BIOS, предложит вам изменить доверенный платформенный модуль, подтвердите изменение.

9. В процессе обработки образа операционной системы клиента Windows, когда вы будете готовы начать шифрование, перезапустите службу агента MBAM и установите для параметра автоматический запуск команду **автоматически** , выполнив командную строку от имени администратора и введя следующие команды:

   **SC config mbamagent Start = Auto**

   **NET start mbamagent**

10. Удалите значения из раздела "пропустить", запустив regedit и перейдя к разделу реестра HKLM\\SOFTWARE\\Microsoft. Чтобы удалить узел **MBAM** , щелкните узел правой кнопкой мыши и выберите команду **Удалить**.

## Статьи по теме


[Развертывание клиента MBAM 2.0](deploying-the-mbam-20-client-mbam-2.md)








