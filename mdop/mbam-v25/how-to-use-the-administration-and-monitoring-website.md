---
title: Использование веб-сайта администрирования и мониторинга
description: Использование веб-сайта администрирования и мониторинга
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813045"
---
# Использование веб-сайта администрирования и мониторинга


Веб-сайт администрирования и наблюдения, также называемый службой поддержки, является интерфейсом администратора для шифрования диска BitLocker. С помощью веб-сайта можно просматривать отчеты, восстанавливать диски конечных пользователей и управлять доверенными платформенными модулями, как описано в следующих разделах.

**Примечание**  Если вы используете MBAM в изолированной топологии, все отчеты будут просматриваться на веб-сайте администрирования и мониторинга. Если вы используете топологию интеграции Configuration Manager, вы будете просматривать все отчеты в Configuration Manager, за исключением отчета аудита восстановления, который вы продолжаете просматривать на веб-сайте администрирования и мониторинга. Дополнительные сведения об отчетах можно найти [в разделе Наблюдение за соответствием и создание отчетов о соответствии BitLocker с помощью MBAM 2,5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).

 

## Роли, необходимые для использования веб-сайта администрирования и мониторинга


Для доступа к определенным областям веб-сайта администрирования и мониторинга необходимо иметь одну из следующих ролей: группы, созданные в службе каталогов Active Directory. Вы можете использовать любое имя для этих групп.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Account</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM опытных пользователей службы поддержки</p></td>
<td align="left"><p>Предоставляет доступ ко всем областям веб-сайта администрирования и мониторинга. Пользователи, которым назначена эта роль, вводят только ключ восстановления, а не домен и имя пользователя конечного пользователя, при помощи которых пользователи смогут восстановить свои диски. Если пользователь является членом обеих групп "Пользователи службы поддержки MBAM" и "Пользователи расширенной справочной службы", то разрешения группы "Пользователи расширенной справочной службы" переопределяют разрешения на доступ к группе "MBAM службы поддержки".</p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Пользователи службы поддержки MBAM</p></td>
<td align="left"><p>Предоставляет доступ к разделу Управление областями восстановления доверенных платформенных устройств и дисков на веб-сайте администрирования и мониторинга. Пользователи, которым назначена эта роль, должны заполнить все поля, включая домен пользователя и имя учетной записи, если они используют любую область.</p>
<p>Если пользователь является членом обеих групп "Пользователи службы поддержки MBAM" и "Пользователи расширенной справочной службы", то разрешения группы "Пользователи расширенной справочной службы" переопределяют разрешения на доступ к группе "MBAM службы поддержки".</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Пользователи отчетов MBAM</p></td>
<td align="left"><p>Предоставляет доступ к отчетам в <strong> области "отчеты </strong> " на веб-сайте администрирования и мониторинга.</p></td>
</tr>
</tbody>
</table>

 

## Задачи, которые можно выполнять на веб-сайте администрирования и наблюдения


В следующей таблице перечислены задачи, которые можно выполнять на веб-сайте администрирования и наблюдения, а также приведены ссылки на дополнительные сведения о каждой задаче.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Задача</th>
<th align="left">Область веб-сайта, на котором можно получить доступ к задаче</th>
<th align="left">Описание</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Просмотр отчетов.</p></td>
<td align="left"><p>Отчеты</p></td>
<td align="left"><p>Позволяет запускать отчеты для мониторинга использования BitLocker, соответствия требованиям и восстановления ключей. В отчетах содержатся данные о требованиях к корпоративному соотношении, отдельных компьютерах и о том, кто запросил ключи восстановления или пакет OwnerAuth доверенного платформенного модуля для определенного компьютера.</p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)">Просмотр отчетов MBAM 2.5 для изолированной топологии</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Определение состояния шифрования BitLocker для потерянных или украденных компьютеров</p></td>
<td align="left"><p>Отчеты</p></td>
<td align="left"><p>Определение того, был ли зашифрован том, если компьютер потерян или украден.</p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)">Определение состояния шифрования BitLocker утерянных компьютеров</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Восстановление потерянных дисков</p></td>
<td align="left"><p>Восстановление диска</p></td>
<td align="left"><p>Восстановите диски, указанные ниже.</p>
<ul>
<li><p>В режиме восстановления</p></li>
<li><p>Были перемещены</p></li>
<li><p>Повреждены</p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)">Восстановление диска в режиме восстановления</a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)">Восстановление перемещенного диска</a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)">Восстановление поврежденного диска</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Сброс блокировки доверенного платформенного модуля</p></td>
<td align="left"><p>Управление TPM</p></td>
<td align="left"><p>Предоставляет доступ к данным доверенного платформенного модуля, собранные клиентом MBAM. В случае блокировки доверенного платформенного модуля с помощью веб-сайта администрирования и наблюдения извлеките необходимый файл пароля, чтобы разблокировать доверенный платформенный модуль.</p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)">Сброс блокировки доверенного платформенного модуля</a></p></td>
</tr>
</tbody>
</table>

 


## Статьи по теме


[Управление BitLocker с помощью MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





