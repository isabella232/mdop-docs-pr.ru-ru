---
title: Настройка файла журнала клиента
description: Настройка файла журнала клиента
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817799"
---
# Настройка файла журнала клиента


Вы можете использовать следующие процедуры для настройки файла журнала клиента Application Virtualization (App-V).

**Изменение расположения файла журнала**

-   Измените значение в следующем разделе реестра, чтобы указать новый путь для файла журнала. После изменения этого значения необходимо перезапустить службу **sftlist** . Это расположение также может быть изменено в интерактивном режиме после установки.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName

**Изменение уровня ведения журнала**

-   По умолчанию для сообщений, которые записываются в журнал, включаются все события уровня серьезности 4 (информационные) и выше. Уровень серьезности хранится в следующем значении ключа. Установите для этого параметра значение 5, чтобы включить ведение подробного журнала. Используйте подробный журнал только для коротких периодов при устранении неполадок, так как это приводит к созданию большого объема сообщений и приводит к быстрому заполнению журнала.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity

**Изменение размера журнала**

-   В Application Virtualization (App-V) 4,5 размер журнала управляется следующим значением раздела реестра. Это значение по умолчанию равно 256 МБ и определяет максимальный размер (в МЕГАБАЙТах), в течение которого журнал может увеличиваться до сброса.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize

    **Внимание!**  Для этого значения раздела реестра должно быть задано значение больше нуля, что приводит к сбросу файла журнала.

     

**Изменение количества резервных копий**

-   Когда файл журнала достигнет максимального размера, он принудительно сбрасывается, когда происходит следующая запись в журнал. Сброс приводит к созданию нового файла журнала, а старый файл переименовывается в качестве резервной копии. Следующий параметр реестра задает количество резервных копий файла журнала, которые сохраняются при сбросе файла. Значение по умолчанию — 4.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount

    Формат имени файла журнала резервной копии: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** и зависит от времени сброса в формате UTC. В таблице ниже перечислены символы, используемые для создания имен файлов и их описания.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Символ</th>
    <th align="left">Описание</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>ГГГГ</p></td>
    <td align="left"><p>4-значный год</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>ММ</p></td>
    <td align="left"><p>2-значный месяц (01 – 12)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>ДД</p></td>
    <td align="left"><p>2-значный день месяца (01 – 31)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>чч</p></td>
    <td align="left"><p>час (00 – 23)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>мм</p></td>
    <td align="left"><p>минуты (00 – 59)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>ss</p></td>
    <td align="left"><p>секунд (00 – 59)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>uuu</p></td>
    <td align="left"><p>мсек (000 – 999)</p></td>
    </tr>
    </tbody>
    </table>

     

## Статьи по теме


[Настройка параметров реестра клиента App-V с помощью командной строки](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





