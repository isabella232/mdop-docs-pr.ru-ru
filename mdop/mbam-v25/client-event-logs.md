---
title: Журналы событий клиента
description: Журналы событий клиента
author: dansimp
ms.assetid: d5c2f270-db6a-45f1-8557-8c6fb28fd568
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7324d07bf018944fcbe24168bba2e9abea9cea41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824192"
---
# Журналы событий клиента

Журналы событий клиента MBAM находятся в окне просмотра событий — Журналы приложений и служб — путь Microsoft – Windows – MBAM-Operational.
В приведенной ниже таблице указаны коды событий, которые могут возникать в клиенте MBAM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Идентификатор события</th>
<th align="left">Канал</th>
<th align="left">Символ события</th>
<th align="left">Сообщение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>1,1</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>VolumeEnactmentSuccessful</p></td>
<td align="left"><p>Политики MBAM были успешно применены.</p></td>
</tr>
<tr class="even">
<td align="left"><p>2</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>VolumeEnactmentFailed</p></td>
<td align="left"><p>При применении политик MBAM произошла ошибка.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Трехконтактный</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>TransferStatusDataSuccessful</p></td>
<td align="left"><p>Данные о состоянии шифрования успешно отправлены.</p></td>
</tr>
<tr class="even">
<td align="left"><p>четырехпроцессорном</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TransferStatusDataFailed</p></td>
<td align="left"><p>Произошла ошибка при отправке данных о состоянии шифрования.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>No8</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>SystemVolumeNotFound</p></td>
<td align="left"><p>Системный том отсутствует. SystemVolume требуется для шифрования диска с операционной системой.</p></td>
</tr>
<tr class="even">
<td align="left"><p>@</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TPMNotFound</p></td>
<td align="left"><p>Отсутствует оборудование доверенного платформенного модуля. TPM нужен, чтобы зашифровать диск операционной системы с помощью любого предохранителя доверенного платформенного модуля.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>5-10</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>MachineHWExempted</p></td>
<td align="left"><p>Компьютер исключен из шифрования. Состояние оборудования компьютера: исключено</p></td>
</tr>
<tr class="even">
<td align="left"><p>11</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>MachineHWUnknown</p></td>
<td align="left"><p>Компьютер исключен из шифрования. Состояние оборудования компьютера: неизвестно</p></td>
</tr>
<tr class="odd">
<td align="left"><p>12</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>HWCheckFailed</p></td>
<td align="left"><p>Проверка аппаратного освобождения не пройдена.</p></td>
</tr>
<tr class="even">
<td align="left"><p>рис</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserIsExempted</p></td>
<td align="left"><p>Пользователь исключен из шифрования.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>дюймов</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserIsWaiting</p></td>
<td align="left"><p>Пользователь запросил исключение.</p></td>
</tr>
<tr class="even">
<td align="left"><p>10-15</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserExemptionCheckFailed</p></td>
<td align="left"><p>Проверка освобождения пользователей завершилась сбоем.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>шестнадцат</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserPostponed</p></td>
<td align="left"><p>Пользователь отложил процесс шифрования.</p></td>
</tr>
<tr class="even">
<td align="left"><p>18</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TPMInitializationFailed</p></td>
<td align="left"><p>Инициализация TPM завершилась сбоем. Пользователь отклонил изменения в BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>18</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>CoreServiceDown</p></td>
<td align="left"><p>Не удается подключиться к службе восстановления MBAM и оборудования.</p></td>
</tr>
<tr class="even">
<td align="left"><p>19</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>CoreServiceUp</p></td>
<td align="left"><p>Успешно подключено к службе восстановления MBAM и оборудования.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>средняя</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>PolicyMismatch</p></td>
<td align="left"><p>Политика MBAM в конфликте или повреждена.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Порт</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>ConflictingOSVolumePolicies</p></td>
<td align="left"><p>Обнаружен конфликт политик шифрования тома операционной системы. Проверьте политики BitLocker и MBAM, связанные с защитой диска ОС.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>максималь</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>ConflictingFDDVolumePolicies</p></td>
<td align="left"><p>Обнаружены неисправленные политики шифрования тома для диска с данными. Проверьте политики BitLocker и MBAM, связанные с защитой ФЛОППИ стример.</p></td>
</tr>
<tr class="even">
<td align="left"><p>отображал</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>EncryptionFailedNoDra</p></td>
<td align="left"><p>При шифровании произошла ошибка. В режиме FIPS для предустановленных компьютеров с Windows 8,1 требуется предохранитель агента восстановления данных (DRA).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Плот</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>TpmOwnerAuthEscrowed</p></td>
<td align="left"><p>OwnerAuth доверенного платформенного модуля.</p></td>
</tr>
<tr class="even">
<td align="left"><p>составляет</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>RecoveryKeyEscrowed</p></td>
<td align="left"><p>Ключ восстановления BitLocker для тома был заблокирован.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>30</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>RecoveryKeyReset</p></td>
<td align="left"><p>Раздел восстановления BitLocker для тома обновлен.</p></td>
</tr>
<tr class="even">
<td align="left"><p>31</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>EnforcePolicyDateSet</p></td>
<td align="left"><p><em> &lt; &gt; </em> Установленная для тома Дата политики принудительного применения</p></td>
</tr>
<tr class="odd">
<td align="left"><p>32</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>EnforcePolicyDateCleared</p></td>
<td align="left"><p><em> &lt; &gt; </em> Для тома была очищена Дата политики принудительного применения.</p></td>
</tr>
<tr class="even">
<td align="left"><p>33</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>TpmLockOutResetSucceeded</p></td>
<td align="left"><p>Сброс блокировки доверенного платформенного модуля выполнен успешно.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>34</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TpmLockOutResetFailed</p></td>
<td align="left"><p>Не удалось сбросить блокировку доверенного платформенного модуля.</p></td>
</tr>
<tr class="even">
<td align="left"><p>35</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalSucceeded</p></td>
<td align="left"><p>OwnerAuth доверенного платформенного модуля из MBAM Services успешно получено.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>36</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalFailed</p></td>
<td align="left"><p>Не удалось получить OwnerAuth TPM из служб MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>37</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>WmiProviderDllSearchPathUpdateFailed</p></td>
<td align="left"><p>Не удалось обновить путь поиска DLL для поставщика WMI.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>38</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TimedOutWaitingForWmiProvider</p></td>
<td align="left"><p>Прекращение ожидания агента — ожидается экземпляр поставщика WMI MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>39</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>RemovableDriveMounted</p></td>
<td align="left"><p>Съемный диск был подключен.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>40</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>RemovableDriveDismounted</p></td>
<td align="left"><p>Съемный диск был отсоединен.</p></td>
</tr>
<tr class="even">
<td align="left"><p>41</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>FailedToEnactEndpointUnreachable</p></td>
<td align="left"><p>Не удалось подключиться к MBAM восстановления и службе оборудования, поскольку MBAM политики не будут успешно применены к тому.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>42</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>FailedToEnactLockedVolume</p></td>
<td align="left"><p>Состояние заблокированного тома не позволило успешно применить политики MBAM к тому.</p></td>
</tr>
<tr class="even">
<td align="left"><p>43</p></td>
<td align="left"><p>Действующие</p></td>
<td align="left"><p>TransferStatusDataFailedEndpointUnreachable</p></td>
<td align="left"><p>Не удалось подключиться к службе соответствия требованиям MBAM, так как она не позволила передать данные о состоянии шифрования.</p></td>
</tr>
</tbody>
</table>

 


## Статьи по теме
[Технический справочник по MBAM 2.5](technical-reference-for-mbam-25.md)

[Журналы событий сервера](server-event-logs.md)

 


## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





