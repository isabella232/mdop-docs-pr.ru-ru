---
title: Определение того, почему устройство получает сообщение о несоответствии
description: Определение того, почему устройство получает сообщение о несоответствии
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824572"
---
# Определение того, почему устройство получает сообщение о несоответствии


Следующие коды несоответствия предоставлены WMI и описывают причины, по которым в MBAM, как несоответствующие требованиям, сообщается о конкретном устройстве.

Для просмотра WMI можно использовать предпочтительный метод. Если вы используете PowerShell, запустите программу `gwmi -class mbam_volume -Namespace root\microsoft\mbam` из командной строке PowerShell и выполните поиск по запросу ReasonsForNoncompliance.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Код без соответствия требованиям</th>
<th align="left">Причина, по которой не удается получить соответствие</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>до</p></td>
<td align="left"><p>Стойкость шифра не является AES 256.</p></td>
</tr>
<tr class="even">
<td align="left"><p>1,1</p></td>
<td align="left"><p>Для MBAM политики требуется, чтобы этот том был зашифрован, но это не так.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>2</p></td>
<td align="left"><p>Для политики MBAM требуется, чтобы этот том не был зашифрован, но это так.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Трехконтактный</p></td>
<td align="left"><p>Для политики MBAM требуется, чтобы этот том использовал предохранитель доверенного платформенного модуля, но это не так.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>четырехпроцессорном</p></td>
<td align="left"><p>Для политики MBAM требуется, чтобы этот том использовал предохранитель TPM + PIN-код, но это не так.</p></td>
</tr>
<tr class="even">
<td align="left"><p>5</p></td>
<td align="left"><p>Политика MBAM не позволяет компьютерам доверенного платформенного модуля сообщать о том, что он не соответствует требованиям.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>152</p></td>
<td align="left"><p>У тома есть предохранитель доверенного платформенного модуля, но доверенный платформенный модуль не отображается (загружен с ключом восстановления после отключения TPM в BIOS).</p></td>
</tr>
<tr class="even">
<td align="left"><p>5-7</p></td>
<td align="left"><p>Для политики MBAM требуется, чтобы этот том использовал предохранитель пароля, но у него нет такого тома.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>No8</p></td>
<td align="left"><p>Для политики MBAM требуется, чтобы этот том не использовал предохранитель пароля, но у него есть один из них.</p></td>
</tr>
<tr class="even">
<td align="left"><p>@</p></td>
<td align="left"><p>Для политики MBAM требуется, чтобы этот том использовал предохранитель автоматического разблокировки, но у него нет такого тома.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>5-10</p></td>
<td align="left"><p>Для политики MBAM требуется, чтобы этот том не использовал предохранитель автоматического разблокировки, но у него есть один из них.</p></td>
</tr>
<tr class="even">
<td align="left"><p>11</p></td>
<td align="left"><p>Конфликт политики обнаружен, так как MBAM сообщил о том, что этот том соответствует требованиям.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>12</p></td>
<td align="left"><p>Системный том необходим для шифрования тома операционной системы, но отсутствует.</p></td>
</tr>
<tr class="even">
<td align="left"><p>рис</p></td>
<td align="left"><p>Защита тома приостановлена.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>дюймов</p></td>
<td align="left"><p>Автоматическое снятие блокировки в небезопасном режиме без шифрования тома операционной системы.</p></td>
</tr>
<tr class="even">
<td align="left"><p>10-15</p></td>
<td align="left"><p>Для политики требуется минимальная Cypher сила — XTS-AES-128 bit, фактическая Cypher сила является менее надежной.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>шестнадцат</p></td>
<td align="left"><p>Для политики требуется минимальная Cypher сила — XTS-AES-256 bit, фактическая Cypher сила является менее надежной.</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Технический справочник по MBAM 2.5](technical-reference-for-mbam-25.md)

[Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





