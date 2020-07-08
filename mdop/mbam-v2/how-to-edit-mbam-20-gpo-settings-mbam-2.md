---
title: Изменение параметров объектов групповой политики MBAM 2.0
description: Изменение параметров объектов групповой политики MBAM 2.0
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824089"
---
# Изменение параметров объектов групповой политики MBAM 2.0


Чтобы успешно развернуть администрирование и мониторинг Microsoft BitLocker (MBAM), необходимо сначала определить групповые политики, которые будут использоваться при реализации администрирования и мониторинга Microsoft BitLocker. Более подробную информацию о различных доступных политиках можно найти в разделе [планирование MBAM 2,0 с учетом требований к групповой политике](planning-for-mbam-20-group-policy-requirements-mbam-2.md) . Определив политики, которые вы собираетесь использовать, необходимо изменить один или несколько объектов групповой политики (GPO), которые содержат параметры политики для MBAM.

Чтобы настроить основные и рекомендуемые параметры GPO, выполните указанные ниже действия, чтобы включить MBAM для управления шифрованием BitLocker на клиентских компьютерах организации.

**Изменение параметров объекта групповой политики клиента MBAM**

1.  На компьютере, на котором установлен шаблон групповой политики MBAM, убедитесь в том, что службы MBAM включены.

2.  С помощью консоли управления групповыми политиками (GPMC. msc) или расширенного продукта MDOP на компьютере с установленным шаблоном групповой политики MBAM выберите **Конфигурация компьютера**, выберите пункт **политики**, щелкните **Административные шаблоны**, выберите пункт **компоненты Windows**и нажмите кнопку **MDOP MBAM (Управление BitLocker)**.

3.  Измените параметры объекта групповой политики, необходимые для включения клиентских служб MBAM на клиентских компьютерах. Для каждой политики в приведенной ниже таблице выберите **Группа политики**, щелкните **политику**и настройте **параметр**.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Группа политики</th>
    <th align="left">Политика</th>
    <th align="left">Параметр</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Управление клиентами</p></td>
    <td align="left"><p>Настройка служб MBAM</p></td>
    <td align="left"><p>Включено. Настройте <strong> конечную точку для восстановления MBAM и службы оборудования </strong> и <strong> выберите данные восстановления BitLocker для хранения </strong> . Установите <strong> конечную точку службы соответствия MBAM </strong> и введите частоту отчета о состоянии (в минутах).</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Диск операционной системы</p></td>
    <td align="left"><p>Параметры шифрования диска операционной системы</p></td>
    <td align="left"><p>Включено. Установите <strong> переключатель выбрать предохранитель для диска операционной системы </strong> . Требуется для сохранения данных на диске операционной системы на сервере восстановления MBAMKey.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Съемный диск</p></td>
    <td align="left"><p>Управление использованием BitLocker на съемных дисках</p></td>
    <td align="left"><p>Включено. Обязательно, если MBAM сохранит съемные данные на сервере восстановления ключа MBAM.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Несъемный диск</p></td>
    <td align="left"><p>Управление использованием BitLocker на съемных дисках</p></td>
    <td align="left"><p>Включено. Обязательно, если MBAM сохранит данные фиксированного диска на сервере восстановления ключа MBAM.</p>
    <p>Укажите <strong> , как можно восстановить диски, защищенные с помощью BitLocker </strong> , и <strong> разрешите агент восстановления данных </strong> .</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## Статьи по теме


[Развертывание объектов групповой политики MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)









