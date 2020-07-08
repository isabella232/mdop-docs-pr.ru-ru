---
title: Развертывание клиента MBAM с помощью командной строки
description: Развертывание клиента MBAM с помощью командной строки
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824489"
---
# Развертывание клиента MBAM с помощью командной строки


Вы можете использовать командную строку для развертывания программного обеспечения клиента администрирования и мониторинга Microsoft BitLocker (MBAM).

## Командная строка для развертывания программного обеспечения клиента MBAM


Введите в командной строке следующую команду, чтобы автоматически присвоить лицензионное соглашение с конечным пользователем при развертывании клиентского программного обеспечения MBAM.

**MBAMClientSetup.exe/acceptEula = Yes**

**Примечание**  Параметры командной строки **/Ju** и **/JM** не поддерживаются, и их нельзя использовать для установки клиентского программного обеспечения MBAM.

 

Чтобы извлечь и установить MSP, введите в командной строке следующую команду:

**MBAMClientSetup.exe/Extract &lt; путь для извлечения MSI &gt; /AcceptEula = да**

Затем установите пакет MSI автоматически, выполнив следующую команду:

**msiexec/i &lt; путь к извлеченному пакету MSI &gt; /QB ALLUSERS = 1 REBOOT = REALLYSUPPRESS**

**Примечание**  Начиная с MBAM 2,5 с пакетом обновления 1 (SP1), отдельный MSI больше не входит в состав продукта MBAM. Тем не менее, после принятия условий лицензионного соглашения вы можете извлечь MSI-файл из исполняемого файла (exe), который входит в состав продукта.

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a>OPTIN \ _FOR \ _MICROSOFT \ _UPDATES = 1 параметр командной строки


При необходимости вы можете указать параметр командной строки `OPTIN_FOR_MICROSOFT_UPDATES=1` во время установки клиентского программного обеспечения, чтобы автоматически установить обновления Microsoft на клиентских компьютерах. При указании этого параметра автоматически запускается Microsoft Update и производится поиск доступных обновлений для установки после завершения установки клиентского программного обеспечения.

Этот параметр командной строки можно использовать в одном из указанных ниже способов установки.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Установите клиентское программное обеспечение MBAM с помощью</th>
<th align="left">Пример.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>MBAMClientSetup.exe</strong></p></td>
<td align="left"><p><strong>MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>msiexec/i MBAMClient.msi</strong></p></td>
<td align="left"><p><strong>msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</strong></p></td>
</tr>
</tbody>
</table>

 


## Статьи по теме


[Развертывание клиента MBAM 2.5](deploying-the-mbam-25-client.md)

 

 
## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




