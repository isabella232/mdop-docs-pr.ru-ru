---
title: Необходимые условия для клиентов MBAM 2.5
description: Необходимые условия для клиентов MBAM 2.5
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826969"
---
# Необходимые условия для клиентов MBAM 2.5


Перед установкой клиентского программного обеспечения MBAM на компьютерах конечных пользователей убедитесь, что ваша среда и клиентские компьютеры соответствуют следующим требованиям.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Предварительные</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Корпоративный домен должен содержать по крайней мере один контроллер домена Windows Server 2008 (или более поздней версии).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Клиентский компьютер должен войти в корпоративную интрасеть.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Только для клиентских компьютеров с Windows 7: каждый клиент должен иметь возможность доверенного платформенного модуля (TPM) (TPM 1,2 или более поздней версии).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Для Windows 8,1, Windows 10 RTM или Windows 10 версии 1511 только на клиентских компьютерах: Если вы хотите, чтобы MBAM мог хранить ключи восстановления доверенного платформенного модуля и управлять ими, необходимо отключить автоматическое наполнение TPM и MBAM, который должен быть указан в качестве владельца доверенного платформенного модуля перед развертыванием MBAM.</p>
<p>В MBAM 2,5 с пакетом обновления 1 (SP1) вам больше не нужно включать автоматическое предоставление TPM, но необходимо убедиться в том, что для объектов групповой политики доверенного платформенного модуля не задано криптоключ OwnerAuth в Active Directory.</p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)">Процедуры безопасности MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>В Windows 10 версии 1607 или более поздней права собственности на этот доверенный платформенный модуль могут получить только Windows. В addiiton при подготовке доверенного платформенного модуля Windows не сохранит пароль владельца доверенного платформенного модуля.</p>
<p>В MBAM 2,5 с пакетом обновления 1 (SP1) необходимо включить функцию автоматического конфигурирования.</p>
</p></td>
<td align="left"><p>Дополнительные <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> сведения приведены в разделе пароль владельца доверенного платформенного модуля </a> .
</p></td>
</tr>
<tr class="even">
<td align="left"><p>Микросхема TPM должна быть включена в BIOS и может быть переустановлена из операционной системы.</p></td>
<td align="left"><p>Дополнительные сведения приведены в документации по BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>На жестком диске компьютера должны быть по крайней мере два раздела, которые необходимо отформатировать с помощью файловой системы NTFS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>На жестком диске компьютера должна быть установлена BIOS, совместимая с TPM и поддерживающая USB-устройства во время запуска компьютера.</p></td>
<td align="left"><div class="alert">
<strong>Примечание.</strong><br/><p>Убедитесь, что клавиатура, видео или мышь подключены напрямую и не управляются с помощью клавиатуры, видео или мыши (KVM) Switch. КВМ-коммутатор может взаимодействовать с возможностями компьютера, чтобы обнаружить физическое присутствие оборудования.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Если вы используете прокси-сервер, он должен быть видимым в контексте системы. MBAM выполняется под контекстом системы, а не контекстом пользователя.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**Важно.**  
Если вы используете BitLocker без MBAM, то MBAM можно установить и использовать существующие данные TPM.




## Статьи по теме


[Поддерживаемые конфигурации MBAM 2.5](mbam-25-supported-configurations.md)

[Планирование развертывания MBAM 2.5](planning-to-deploy-mbam-25.md)


## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






