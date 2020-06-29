---
title: Администрирование MBAM 1.0 с помощью PowerShell
description: Администрирование MBAM 1.0 с помощью PowerShell
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825139"
---
# Администрирование MBAM 1.0 с помощью PowerShell


Администрирование и мониторинг Microsoft BitLocker (MBAM) предоставляет перечисленные ниже наборы командлетов Windows PowerShell. Администраторы могут использовать эти командлеты PowerShell для выполнения различных задач сервера MBAM в командной строке, а не на веб-сайте администрирования MBAM.

## Администрирование MBAM с помощью PowerShell


Используйте командлеты PowerShell, описанные в этой статье, чтобы администрировать MBAM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Имя</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Add-MbamHardwareType</p></td>
<td align="left"><p>Добавляет новую аппаратную модель в инвентаризацию оборудования MBAM. Этот командлет также может определять, поддерживается ли оборудование и не поддерживается шифрованием диска BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Запрашивает ключ восстановления MBAM, который позволяет пользователю разблокировать компьютер или зашифрованный диск.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamHardwareType</p></td>
<td align="left"><p>Возвращает основное инвентаризацию оборудования, которая содержит данные, указывающие, совместимы ли модели оборудования с шифрованием диска BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Предоставление пользователю пароля владельца доверенного платформенного модуля для управления доступом TPM (доверенный платформенный модуль). Помогает пользователям, когда доверенный платформенный модуль заблокировал их и больше не будет получать PIN-код.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Install-MBAM</p></td>
<td align="left"><p>Устанавливает функции MBAM, обеспечивающие расширенную групповую политику, шифрование, восстановление ключей и средства создания отчетов о соответствии требованиям.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Remove-MbamHardwareType</p></td>
<td align="left"><p>Удаление моделей оборудования из инвентаризации оборудования.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Set-MbamHardwareType</p></td>
<td align="left"><p>Позволяет управлять оборудованием основного оборудования, чтобы определить, поддерживаются ли модели оборудования или не могут выполнять шифрование BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Uninstall-MBAM</p></td>
<td align="left"><p>Удаление ранее установленных функций MBAM, которые обеспечивают расширенные политики, шифрование, восстановление ключей и средства создания отчетов о соответствии требованиям.</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Операции MBAM 1.0](operations-for-mbam-10.md)

 

 





