---
title: Управление параметрами конфигурации рабочей области MED-V
description: Управление параметрами конфигурации рабочей области MED-V
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826159"
---
# Управление параметрами конфигурации рабочей области MED-V


Microsoft Enterprise Virtualization (MED-V) 2,0 хранит параметры конфигурации в реестре. Данные, которые мы включаем сюда для работы с реестром, могут помочь вам лучше управлять службами MED-V.

При поиске значений результирующих параметров для MED-V используется следующий путь поиска:

MED-V сначала выполняет поиск в политике компьютера.

Если значение не найдено, MED-V выполняет поиск в политике пользователя.

Если значение не найдено, MED-V будет выглядеть в кусте HKEY \ _LOCAL \ _MACHINE \\System.

Если значение не найдено, MED-V будет выглядеть в кусте реестра HKEY \ _CURRENT USER.

Если значение по-прежнему не найдено, для MED-V используется значение по умолчанию.

Общие рекомендации — это установка значения в кусте HKEY \ _LOCAL \ _MACHINE \\System или в политике компьютера. Но если вы хотите, чтобы конечный пользователь мог настроить определенный параметр, его следует оставить.

**Примечание.**  
Перед развертыванием рабочих областей MED-V вы можете использовать редактор сценариев для изменения сценария Windows PowerShell (PS1-файла), созданного с помощью упаковщика рабочих областей для задолженности. Дополнительные сведения можно найти в разделе [Настройка дополнительных параметров с помощью Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

После развертывания рабочих областей MED-V вы можете изменить определенные параметры конфигурации MED-V, изменив записи в реестре.



В этом разделе перечислены все настраиваемые разделы реестра для MED-V и описаны их использование.

## Ключ диагностики


В таблице ниже приведены сведения о значениях реестра, связанных с клавишей HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Имя </th>
<th align="left">Тип </th>
<th align="left">Данные и по умолчанию </th>
<th align="left">Описание </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EventLogLevel </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>По умолчанию = 3</p></td>
<td align="left"><p>Тип данных, которые регистрируются в журнале событий. Ниже указаны уровни: 0 (нет), 1 (ошибка), 2 (предупреждение), 3 (сведения), 4 (Отладка).</p></td>
</tr>
</tbody>
</table>



## Клавиша FTS


В таблице ниже приведены сведения о значениях реестра, связанных с клавишей HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Fts.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Имя</th>
<th align="left">Тип</th>
<th align="left">Данные и по умолчанию</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddUserToAdminGroupEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 0</p></td>
<td align="left"><p>Настройка автоматического добавления конечных пользователей в группу Администратор&#39;s. 0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: при первом запуске программы установки автоматически не добавляется конечный пользователь в группу Администратор&#39;s.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: при первом запуске программа установки автоматически добавляет пользователя в группу Администратор&#39;s.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ComputerNameMask </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>MEDV* </p></td>
<td align="left"><p>Маска имени компьютера, которая используется для создания гостевой виртуальной машины&#39;s имя компьютера.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Маска может содержать тег% username%, чтобы вставить имя пользователя как часть имени компьютера. Аналогичным образом, тег% hostname% вставляет имя главного компьютера.</p>
<p>Каждый &quot; # &quot; символ маски заменяется случайной цифрой. Знак звездочки (*) в конце маски заменяется случайными буквенно-цифровыми символами.</p>
<p>Определенное количество символов из% hostname% и% username% можно записать с помощью квадратных скобок. Например, &quot; % username% [3] &quot; будет использовать первые три символа имени пользователя.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeleteVMStateTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 90</p></td>
<td align="left"><p>Время ожидания (в секундах), по истечении которого при первой попытке установки будет удалена виртуальная машина. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DetachVfdTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 120</p></td>
<td align="left"><p>Время ожидания (в секундах), по истечении которого программа установки пытается отключить виртуальный гибкий диск от виртуальной машины. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogUrl </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Настраиваемый URL-адрес, который связан с внутренней веб-страницей и отображается при первом запуске диалогового окна настройки. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ExplorerTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 900</p></td>
<td align="left"><p>Время ожидания в секундах, в течение которого программа установки ждет первого раза в проводнике Windows. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FailureDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Сообщение обнаружено в файле ресурсов </p></td>
<td align="left"><p>Настраиваемое сообщение, которое отображается для конечного пользователя при первой попытке завершения установки.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GiveUserGroupRightsMaxRetryCount </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>По умолчанию = 3</p></td>
<td align="left"><p>Максимальное количество попыток предоставления прав группе конечных пользователей с помощью MED-V. Превышение указанного значения повтора без возможности успешного предоставления прав доступа к группе конечных пользователей, скорее всего, приводит к сбою подготовки виртуальной машины, для которого он подключается к значению MaxRetryCount. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GiveUserGroupRightsTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 300</p></td>
<td align="left"><p>Время ожидания в секундах, когда вы предоставляете права группы пользователей. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogFilePaths </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Список путей к файлам журнала, собираемых MED-V при первом запуске программы установки. </p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPostponeTime </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 120</p></td>
<td align="left"><p>Максимальное количество часов, которое может быть отложено конечным пользователем при первом запуске программы установки. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxRetryCount </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 3</p></td>
<td align="left"><p>Максимальное количество попыток подготовки виртуальной машины с помощью MED-V, если каждая попытка завершается сбоем, кроме программного обеспечения. Когда подготовка виртуальной машины завершается сбоем и количество попыток настройки при первой попытке будет превышено, приложение MED-V информирует пользователя об ошибке и не дает возможность повторить попытку. Счетчик будет повторно установлен при каждом запуске MED-V. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Режим </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>По умолчанию = автоматическая установка</p></td>
<td align="left"><p>Настройка взаимодействия с пользователем при первом запуске программы. Возможны следующие значения:</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Согласованием.</strong> Конечный пользователь должен ввести данные при первом запуске программы установки.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Если вы создали файл Sysprep. INF, чтобы мини-процесс мог завершить ввод данных пользователем, необходимо выбрать <strong> </strong> режим автоматической установки или проблемы при первом запуске.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Автоматический режим </strong> . Виртуальная машина не отображается для конечных пользователей при первом запуске программы установки, но перед началом первой настройки будет выводиться запрос конечного пользователя.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Автоматическая установка </strong> . Виртуальная машина не отображается для конечного пользователя при первом запуске программы установки.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NonInteractiveRetryTimeoutInc </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 15</p></td>
<td align="left"><p>Время ожидания (в минутах), в течение которого при первой попытке настройки необходимо завершить настройку при первом запуске интерактивного режима. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NonInteractiveTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 45</p></td>
<td align="left"><p>Время ожидания (в минутах), в которое в первый раз при настройке интерактивного режима необходимо завершить настройку. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PostponeUtcDateTimeLimit </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Дата и время в формате UTC DateTime, которое может быть отложено при первом запуске программы установки. Введите формат &quot; гггг-мм-дд чч: мм &quot; с часами, указанными в 24-часовом стандарте часов.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RetryDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Сообщение обнаружено в файле ресурсов </p></td>
<td align="left"><p>Настраиваемое сообщение, которое отображается для конечного пользователя при первой попытке настройки.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetComputerNameEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 0</p></td>
<td align="left"><p>Указывает, следует ли обновлять запись ComputerName в разделе [UserData] файла Sysprep. INF в гостевой системе в соответствии с заданными ComputerNameMask.   0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: запись ComputerName в файле Sysprep. inf не обновляется в соответствии с ComputerNameMask.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = истина: запись ComputerName в файле Sysprep. INF обновлена в соответствии с ComputerNameMask.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetJoinDomainEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 0</p></td>
<td align="left"><p>Указывает, следует ли обновлять параметр JoinDomain в разделе [идентификация] файла Sysprep. INF в гостевой системе в соответствии с параметрами на узле.  0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: параметр JoinDomain в файле Sysprep. inf не обновляется в соответствии с параметрами на узле.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: параметр JoinDomain в файле Sysprep. INF обновляется в соответствии с параметрами на узле.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetMachineObjectOUEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 0</p></td>
<td align="left"><p>Определяет, будет ли параметр MachineObjectOU в разделе [идентификация] файла Sysprep. INF в гостевой системе обновлен в соответствии с узлом.  0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: параметр MachineObjectOU в файле Sysprep. inf не обновляется в соответствии с параметрами на узле.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: параметр MachineObjectOU в файле Sysprep. INF обновляется в соответствии с параметрами на узле.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetRegionalSettingsEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 0</p></td>
<td align="left"><p>Настройка обновления параметров в разделе [RegionalSettings] файла Sysprep. INF в гостевой системе для соответствия узлу.  0 = ложь; 1 = истина.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>По умолчанию параметр TimeZone для гостя всегда синхронизируется с параметром TimeZone в узле.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: параметры в разделе [RegionalSettings] файла Sysprep. INF в гостевой системе не обновляются в соответствии с узлом.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: параметры в разделе [RegionalSettings] файла Sysprep. INF в гостевой системе обновлены в соответствии с узлом.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetUserDataEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 0</p></td>
<td align="left"><p>Настройка обновления параметров FullName и OrgName в разделе [UserData] файла Sysprep. INF в гостевой системе в соответствии с параметрами на узле.  0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: параметры FullName и OrgName в файле Sysprep. inf не обновляются в соответствии с параметрами на узле.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: параметры FullName и OrgName в файле Sysprep. INF обновляются в соответствии с параметрами на узле.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Сообщение обнаружено в файле ресурсов </p></td>
<td align="left"><p>Настраиваемое сообщение, которое отображается для конечного пользователя при первом запуске программы установки. </p></td>
</tr>
<tr class="even">
<td align="left"><p>TaskCancelTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 30</p></td>
<td align="left"><p>Время ожидания в секундах, в течение которого первый раз программа установки ждет ответа от виртуальной машины на операцию отмены. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskVMTurnOffTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 60</p></td>
<td align="left"><p>Время ожидания в секундах, в течение которого первый раз программа установки ждет завершения работы виртуальной машины. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UpgradeTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 600</p></td>
<td align="left"><p>Время, в течение которого вы попытались попытаться обновить программное обеспечение гостевого агента MED-V по истечении времени ожидания. Диапазон от 0 до 2147483647.</p></td>
</tr>
</tbody>
</table>



## Клавиша UserExperience


В таблице ниже приведены сведения о значениях реестра, связанных с клавишами HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience и клавиша HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\UserExperience.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Имя</th>
<th align="left">Тип</th>
<th align="left">Данные и по умолчанию</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AppPublishingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 1</p></td>
<td align="left"><p>Указывает, включена ли публикация приложения на гостевом компьютере.  0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: Отключение публикации приложения от гостя на узле.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: включает публикацию приложения от гостя на узле.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AudioSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 1</p></td>
<td align="left"><p>Настраивает способ совместного использования звукового устройства ввода-вывода между гостевой системой и узлом.  0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: отключает общий доступ к звуковому устройству ввода-вывода между гостевой системой и узлом.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: позволяет предоставлять общий доступ к звуковому устройству ввода-вывода между гостевым и ведущим узлом.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClipboardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 1</p></td>
<td align="left"><p>Определяет, будет ли общий доступ к буферу обмена между гостевой и ведущим приложением включен.  0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: отключает общий доступ к буферу обмена между гостевым и ведущим узлом.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: позволяет предоставлять общий доступ к буферу обмена между гостевой и ведущим узлом.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 300</p></td>
<td align="left"><p>Время, в секундах, до истечения времени первого запуска диалогового окна настройки. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HideVmTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 30</p></td>
<td align="left"><p>Время ожидания (в минутах), в течение которого полноэкранное окно виртуальной машины будет скрыто от конечного пользователя во время длительной попытки входа.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LogonStartEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 1</p></td>
<td align="left"><p>Указывает, следует ли запускать гость, когда пользователь входит в систему на рабочем столе или при запуске первого гостевого приложения.  0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: гость запускается при запуске первой гостевой программы.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: гость запускается, когда пользователь входит в систему на рабочем столе.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PrinterSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 1</p></td>
<td align="left"><p>Определяет, включен ли общий доступ к принтерам между гостевой и ведущим узлом.  0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: отключает общий доступ к принтерам между гостевой и ведущим узлом.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: позволяет предоставлять общий доступ к принтерам между гостевой и ведущим узлом.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RebootAbsoluteDelayTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 1440</p></td>
<td align="left"><p>Время ожидания (в минутах), в течение которого при первом запуске программы установки Ожидается перезагрузка. Диапазон от 0 до 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RedirectUrls </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Указанный список URL-адресов</p></td>
<td align="left"><p>Указывает список URL-адресов, которые нужно перенаправить с узла на гостя. </p></td>
</tr>
<tr class="even">
<td align="left"><p>SmartCardLogonEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 0</p></td>
<td align="left"><p>Определяет, можно ли использовать смарт-карты для проверки подлинности пользователей в MED – V. 0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: не разрешать проверка подлинности конечных пользователей в MED-V на интеллектуальных картах.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: позволяет смарт-картам проверять подлинность конечных пользователей для использования в качестве серверной MED.</p>
<div class="alert">
<strong>Важно.</strong><br/><p>Если включены параметры SmartCardLogonEnabled и CredentialCacheEnabled, SmartCardLogonEnabled переопределяет CredentialCacheEnabled.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>SmartCardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 1</p></td>
<td align="left"><p>Определяет, включен ли общий доступ к смарт-картам между гостевой и ведущим узлом.  0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: отключает общий доступ к смарт-картам между гостевым и ведущим узлом.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: позволяет предоставлять общий доступ к смарт-картам между гостевой и ведущим узлом.</p></td>
</tr>
<tr class="even">
<td align="left"><p>USBDeviceSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 1</p></td>
<td align="left"><p>Определяет, будет ли общий доступ к USB-устройствам между гостевой и ведущим узлом включен.  0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: отключает общий доступ устройств USB между гостевым и ведущим узлом.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: позволяет предоставлять общий доступ к USB-устройствам между гостевой системой и узлом.</p></td>
</tr>
</tbody>
</table>



## Ключ виртуальной машины


В таблице ниже приведены сведения о значениях реестра, связанных с клавишами HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\VM и клавиша HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\VM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Имя</th>
<th align="left">Тип</th>
<th align="left">Данные и по умолчанию</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CloseAction </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>По умолчанию = СПЯЩий режим</p></td>
<td align="left"><p>Действие, выполняемое виртуальной машиной после закрытия последнего работающего приложения. Этот параметр игнорируется, если включен параметр LogonStartEnabled. Возможны следующие варианты:</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>РЕЖИМ ГИБЕРНАЦИи </strong> . Этот параметр освобождает все физические ресурсы, которые использует виртуальная машина, например память и ЦП, и сохраняет состояние всех запущенных приложений и операций.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Завершение работы </strong> . Этот параметр безопасно завершает работу гостевой операционной системы, а затем освобождает все физические ресурсы, которые использует виртуальная машина, например память и ЦП.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>отключение </strong> . Этот параметр может привести к потере данных, так как он аналогичен выключению кнопки питания или выдаче шнура питания на физическом компьютере. Используйте этот параметр только в том случае, если вы не можете использовать один из двух других параметров.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestMemFromHostMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>378, 512, 1024, 1536, 2048 </p></td>
<td align="left"><p>Список значений памяти (МБ) для гостя. Это значение используется для определения объема памяти, доступного для гостя. В сочетании с HostMemToGuestMem создается таблица подстановки, с помощью которой можно определить, сколько памяти нужно выделить на гостевой виртуальной машине. Возможные значения могут быть от 128 до 3712.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GuestUpdateDuration </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 240</p></td>
<td align="left"><p>Количество минут, в течение которых MED-V должен поддерживать функцию "Неспящий режим" на гостевом компьютере для автоматического обновления, начиная с момента, указанного в значении GuestUpdateTime. Диапазон от 0 до 1440. Установка этого значения равным нулю (0) отключает функцию исправлений гостя.</p>
<p>Дополнительные сведения об автоматическом обновлении можно найти в разделе <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Управление автоматическим обновлением для рабочих областей MED-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestUpdateTime </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>По умолчанию = 00:00</p></td>
<td align="left"><p>Час и минута для каждого дня, когда MED-V должен пробудить гостевую систему для автоматического обновления, используя 24-часовой стандарт часов. Укажите время в формате чч: мм  </p>
<p>Дополнительные сведения об автоматическом обновлении можно найти в разделе <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Управление автоматическим обновлением для рабочих областей MED-V </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>HostMemToGuestMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>1024, 2048, 4096, 8192, 16384 </p></td>
<td align="left"><p>Список значений памяти (МБ) для гостя, определяемый объемом ОЗУ, доступном на узле. В сочетании с GuestMemFromHostMem создается таблица подстановки, с помощью которой можно определить, сколько памяти нужно выделить на гостевой виртуальной машине. Возможные значения могут быть от 1024 до 16384.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HostMemToGuestMemCalcEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 1</p></td>
<td align="left"><p>Определяет, будет ли память, выделенная для гостя, рассчитывается на основе памяти, представленной на узле.  0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: память, выделенная для гостя, не рассчитывается на основе памяти, представленной на узле.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: память, выделенная для гостя, рассчитывается на основе памяти, представленной на узле.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Память </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию — 512</p></td>
<td align="left"><p>ОЗУ (МБ), которое должно быть выделено для гостевой виртуальной машины. Этот параметр игнорируется, если включен параметр HostMemToGuestMemEnabled. Диапазон от 128 до 2048.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MultiUserEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 0</p></td>
<td align="left"><p>Настройка общего доступа нескольких пользователей к одной и той же рабочей области MED-V.  0 = ложь; 1 = истина.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: несколько пользователей не могут совместно использовать одну и ту же рабочую область MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: несколько пользователей совместно имеют одну и ту же рабочую область MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NetworkingMode </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>По умолчанию = NAT</p></td>
<td align="left"><p>Сетевое подключение, используемое в качестве гостя. Возможны следующие значения:</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Моста </strong> . Для MED-V имеется собственный сетевой адрес, обычно получаемый с помощью DHCP.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>NAT </strong> . В MED-V используется преобразование сетевых адресов (NAT) для предоставления общего доступа к узлу&#39;s IP для исходящего трафика.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>По умолчанию = 600</p></td>
<td align="left"><p>Общее время ожидания в секундах, в течение которого MED-V ждет завершения задачи, например для перезапуска и завершения работы. Диапазон от 0 до 2147483647.</p></td>
</tr>
</tbody>
</table>



## Параметры реестра гостя


В этом разделе перечислены настраиваемые гостевые разделы реестра MED-V и описаны их использование.

### версии

В таблице ниже приведены сведения о значении реестра гостя, связанном с клавишей HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Имя </th>
<th align="left">Тип </th>
<th align="left">Данные и по умолчанию </th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EnableGPWorkarounds</p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>По умолчанию = 1 </p></td>
<td align="left"><p>Настраивает способ обработки ключей BufferPolicyReads и GroupPolicyMinTransferRate с помощью MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>По умолчанию MED-V задает указанные ниже сочетания клавиш.</p>
<p>BufferPolicyReads = 1 и GroupPolicyMinTransferRate = 0.</p>
<p>Создавайте ключ EnableGPWorkarounds, если это необходимо, и установите для ключа нулевое значение, если не хотите, чтобы MED-V изменил параметры по умолчанию для BufferPolicyReads и GroupPolicyMinTransferRate.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Если Рабочая область MED-V работает в режиме NAT, EnableGPWorkarounds влияет на разделы реестра BufferPolicyReads и GroupPolicyMinTransferRate. Если Рабочая область MED-V работает в режиме моста, EnableGPWorkarounds влияет только на раздел реестра BufferPolicyReads.</p>
</div>
<div>

</div>
<p>1 = true: MED-V задает клавиши BufferPolicyReads = 1 и GroupPolicyMinTransferRate = 0 (при работе в режиме NAT) или просто BufferPolicyReads = 1 (если работает в режиме моста).</p>
<p>0 = false: MED-V не вносит изменения в ключи BufferPolicyReads и GroupPolicyMinTransferRate.</p></td>
</tr>
</tbody>
</table>



## Статьи по теме


[Управление приложениями рабочей области MED-V](manage-med-v-workspace-applications.md)

[Управление перенаправлением URL-адресов MED-V](manage-med-v-url-redirection.md)

[Управление параметрами рабочей области MED-V](manage-med-v-workspace-settings.md)









