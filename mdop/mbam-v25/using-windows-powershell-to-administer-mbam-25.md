---
title: Использование Windows PowerShell для администрирования MBAM 2.5
description: Использование Windows PowerShell для администрирования MBAM 2.5
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812736"
---
# Использование Windows PowerShell для администрирования MBAM 2.5


В этом разделе описаны командлеты Windows PowerShell для администрирования и мониторинга Microsoft BitLocker (MBAM), которые относятся к восстановлению компьютеров и дисков, когда пользователи заблокированы.

Для командлетов, которые вы используете для настройки функций сервера MBAM, ознакомьтесь [с Разстройкой функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a>Командлеты для восстановления компьютеров или дисков, управляемых MBAM


Используйте указанные ниже командлеты Windows PowerShell для восстановления компьютеров или дисков, управляемых MBAM.

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
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Запрашивает ключ восстановления MBAM, который позволяет пользователям разблокировать компьютер или зашифрованный диск.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Предоставление пользователям пароля владельца TPM, который можно использовать для разблокировки доверенного платформенного модуля (TPM), когда ДОВЕРЕНный платформенный модуль заблокировал их и больше не будет получать PIN-код.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> Справка по командлету MBAM


Справка по Windows PowerShell для командлетов MBAM доступна в следующих форматах:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Формат справки Windows PowerShell</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>В командной строке Windows PowerShell введите <strong> </strong> &lt; <em> командлет Get-Help</em>&gt;</p></td>
<td align="left"><p>Чтобы загрузить последние командлеты Windows PowerShell, следуйте инструкциям, приведенным в разделе <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell.</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>На веб-страницах TechNet.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>В центре загрузки как файл Word. docx</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>В центре загрузки в виде PDF-файла</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## Статьи по теме


[Администрирование компонентов MBAM 2.5](administering-mbam-25-features.md)

[Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





