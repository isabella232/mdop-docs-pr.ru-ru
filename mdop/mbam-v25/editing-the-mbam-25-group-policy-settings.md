---
title: Изменение параметров групповой политики MBAM 2.5
description: Изменение параметров групповой политики MBAM 2.5
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812597"
---
# Изменение параметров групповой политики MBAM 2.5


Чтобы успешно развернуть администрирование и мониторинг Microsoft BitLocker (MBAM), необходимо выполнить указанные ниже действия.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Задача</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Скопируйте шаблоны групповой политики MBAM 2,5.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Копирование шаблонов групповой политики MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Определите объекты групповой политики (GPO), которые вы хотите использовать в реализации MBAM. В зависимости от потребностей Организации может потребоваться настроить дополнительные параметры групповой политики.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)">Планирование требований к групповой политике MBAM 2,5 </a> — включает в себя описания объектов групповой политики.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Настройте параметры групповой политики для своей организации.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**Важно!**  Не изменяйте параметры групповой политики в разделе " **Шифрование диска BitLocker** " или MBAM будут работать неправильно. При настройке параметров групповой политики на узле **MDOP MBAM (Управление BitLocker)** MBAM автоматически настраивает параметры **шифрования диска для BitLocker** .

 

**Изменение параметров групповой политики клиента MBAM**

1.  Убедитесь, что на компьютере, на котором установлены шаблоны групповой политики MBAM, включены службы MBAM Services.

2.  С помощью консоли управления групповыми политиками (GPMC. msc) или расширенного управления групповыми политиками Майкрософт на компьютере с установленными шаблонами групповой политики MBAM выберите политики **конфигурации компьютера** : &gt; **Policies** &gt; **Административные шаблоны** &gt; **компоненты Windows** &gt; **MDOP MBAM (Управление BitLocker)**.

3.  Измените параметры групповой политики, необходимые для включения клиентских служб MBAM на клиентских компьютерах. Для каждой политики, описанной в следующей таблице, выберите **Группа политики**, выберите нужную **политику** и настройте параметры.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Группа политики</th>
    <th align="left">Политика</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Управление клиентами</p></td>
    <td align="left"><p>Настройка служб MBAM</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Диск операционной системы</p></td>
    <td align="left"><p>Параметры шифрования диска операционной системы</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Съемный диск</p></td>
    <td align="left"><p>Управление использованием BitLocker на съемных дисках</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Несъемный диск</p></td>
    <td align="left"><p>Управление использованием BitLocker на съемных дисках</p></td>
    </tr>
    </tbody>
    </table>

     

## Статьи по теме


[Планирование требований групповой политики MBAM 2.5](planning-for-mbam-25-group-policy-requirements.md)

[Копирование шаблонов групповой политики MBAM 2.5](copying-the-mbam-25-group-policy-templates.md)

 
## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





