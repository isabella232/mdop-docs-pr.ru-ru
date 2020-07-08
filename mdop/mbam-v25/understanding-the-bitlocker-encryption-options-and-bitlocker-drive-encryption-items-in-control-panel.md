---
title: Общие сведения о параметрах шифрования BitLocker и шифровании дисков BitLocker в панели управления
description: Общие сведения о параметрах шифрования BitLocker и шифровании дисков BitLocker в панели управления
author: dansimp
ms.assetid: f8a01cc2-0c77-48b9-8351-8194e80b0cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739b65680ebfdf19f006ee8f3079f7c7e602f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812773"
---
# Общие сведения о параметрах шифрования BitLocker и шифровании дисков BitLocker в панели управления


В этой статье описаны **Параметры шифрования BitLocker** и элементы панели управления **Шифрование дисков BitLocker** , а также рассматриваются следующие вопросы:

-   Создание элементов

-   Задачи, которые они позволят вам выполнять

-   **Управление BitLocker** контекстное меню "контекстный щелчок", если оно видимо и скрыто, и как сделать его видимым по умолчанию.

## Параметры шифрования BitLocker и элементы панели управления "шифрование диска" BitLocker


В таблице ниже перечислены задачи, которые можно выполнять в каждом элементе панели управления, и описаны способы их создания.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Параметры шифрования BitLocker (MBAM)</th>
<th align="left">Шифрование диска BitLocker (Windows)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Задачи, которые можно выполнить</p></td>
<td align="left"><ul>
<li><p>Изменение ПИН-кода или пароля</p></li>
<li><p>Проверка состояния шифрования для диска</p></li>
<li><p>Открытие консоли управления TPM</p></li>
<li><p>"Включить BitLocker"</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Приостановить защиту диска</p></li>
<li><p>Создание резервной копии ключа восстановления</p></li>
<li><p>Изменение ПИН-кода</p></li>
<li><p>Отключение BitLocker для диска</p></li>
<li><p>Включение BitLocker для диска</p></li>
<li><p>Открытие консоли управления TPM</p></li>
<li><p>Расшифровка диска (отображается только в том случае, если клиент MBAM не установлен)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Создание элемента панели управления</p></td>
<td align="left"><p>Создается на панели управления при установке клиента MBAM. Этот элемент нельзя скрыть.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот элемент отображается не только в том случае, но и не заменяется элементом панели управления шифрованием диска BitLocker по умолчанию.</p>
</div>
<div>

</div></td>
<td align="left"><p>По умолчанию отображается на панели управления как часть операционной системы Windows, но ее можно скрыть.</p>
<p>Чтобы скрыть его, ознакомьтесь со разделом <a href="hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md" data-raw-source="[Hiding the Default BitLocker Drive Encryption Item in Control Panel](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)"> Скрытие элемента шифрования диска BitLocker по умолчанию на панели управления </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="-manage-bitlocker--shortcut-menu"></a>Контекстное меню "Управление BitLocker"


В следующей таблице описано, как зависят от того, установлен ли клиент MBAM в контекстном меню **Manage BitLocker** . Термин "контекстное меню" обозначает параметры, которые отображаются при щелчке правой кнопкой мыши по диску в проводнике Windows.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">При установке клиента MBAM</th>
<th align="left">Если клиент MBAM не установлен</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Видимость контекстного меню</p></td>
<td align="left"><p>Параметр "Управление BitLocker" скрыт.</p>
<p>Чтобы сделать параметр Управление BitLocker видимым в контекстном меню, которое выводит на экран параметр для расшифровки диска, удалите следующий раздел реестра:</p>
<pre class="syntax" space="preserve"><code>HKEY_CLASSES_ROOT\Drive\Shell\manage-bde \REG_SZ LegacyDisable</code></pre></td>
<td align="left"><p>В контекстном меню появится параметр Управление BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Возможности пользователей</p></td>
<td align="left"><p>Если ярлык скрыт, пользователи могут открыть элемент панели управления шифрованием диска BitLocker, но параметр для расшифровки диска недоступен.</p></td>
<td align="left"><p>После того как откроется контекстное меню, нажмите кнопку <strong> Управление BitLocker, </strong> чтобы открыть элемент панели управления шифрованием диска BitLocker, на котором выводится параметр для расшифровки диска.</p></td>
</tr>
</tbody>
</table>




## Статьи по теме


[Администрирование компонентов MBAM 2.5](administering-mbam-25-features.md)



## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





