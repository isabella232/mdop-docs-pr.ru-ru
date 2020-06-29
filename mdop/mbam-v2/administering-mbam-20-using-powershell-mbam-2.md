---
title: Администрирование MBAM 2.0 с помощью PowerShell
description: Администрирование MBAM 2.0 с помощью PowerShell
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823502"
---
# Администрирование MBAM 2.0 с помощью PowerShell


Администрирование и мониторинг Microsoft BitLocker (MBAM) предоставляет перечисленные ниже наборы командлетов Windows PowerShell. Администраторы могут использовать эти командлеты PowerShell для выполнения различных задач администрирования Microsoft BitLocker и наблюдения за серверами из командной строки, а не с веб-сайта администрирования MBAM.

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
<td align="left"><p>Install-MBAM</p></td>
<td align="left"><p>Установка функций MBAM, обеспечивающих расширенную политику, шифрование, восстановление ключей и отчеты о соответствии требованиям.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Uninstall-MBAM</p></td>
<td align="left"><p>Удаление функций MBAM, обеспечивающих расширенную политику, шифрование, восстановление ключей и средства создания отчетов о соответствии требованиям.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Запрашивает ключ восстановления MBAM, который позволяет пользователям разблокировать компьютер или зашифрованный диск.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Предоставление пользователям пароля владельца TPM, который можно использовать для разблокировки доверенного платформенного модуля (TPM), когда ДОВЕРЕНный платформенный модуль заблокировал их и больше не будет получать PIN-код.</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Операции MBAM 2.0](operations-for-mbam-20-mbam-2.md)

 

 





