---
title: Контрольный список обновления App-V
description: Контрольный список обновления App-V
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819739"
---
# Контрольный список обновления App-V


Перед обновлением до приложения Microsoft Application Virtualization (App-V) 4,5 или более поздней версии все версии, предшествующие App-V 4,1, должны быть обновлены до App-V 4,1. Прежде чем обновлять серверные компоненты, необходимо предварительно запланировать обновление клиентов. Клиенты App-V, обновленные до App-V 4,5, продолжают работать с серверами App-V, которые еще не были обновлены. Более ранние версии клиента не поддерживаются на серверах, которые были обновлены до версии App-V 4,5.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Шаг</th>
<th align="left">Справочные материалы</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Обновите клиенты App-V.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)">Обновление клиента Application Virtualization Client</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Обновите серверы и базу данных App-V.</p>
<div class="alert">
<strong>Важно.</strong><br/><p>Если у вас больше одного сервера, доступ к базе данных App-V, то во время обновления базы данных все эти серверы должны быть переведены в автономный режим. Вы должны следовать обычным бизнес-рекомендациям по обновлению базы данных, но мы рекомендуем проверить ее на использование резервной копии базы данных на тестовом сервере. Затем необходимо выбрать один из серверов для первого обновления, который обновит схему базы данных. После успешного обновления рабочей базы данных вы можете обновить программное обеспечение App-V на других серверах.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Обновление серверов и компонентов системы</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Обновите веб-службу управления App-V.</p>
<p>Это действие применяется только в том случае, если веб-служба управления находится на отдельном сервере, для обновления веб-службы управления требуется запустить программу установщика сервера на отдельном сервере. В противном случае Предыдущая операция обновления сервера будет автоматически обновлять веб-службу управления.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Обновление серверов и компонентов системы</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Обновите консоль управления App-V.</p>
<p>Это действие применимо только в том случае, если консоль управления находится на отдельном компьютере, для обновления консоли которого требуется запустить программу установщика сервера на отдельном компьютере. В противном случае предыдущий шаг обновления сервера обновит консоль управления.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Обновление серверов и компонентов системы</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Обновите секвенсор App-V.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)">Обновление программы Application Virtualization Sequencer</a></p></td>
</tr>
</tbody>
</table>



## Дополнительные вопросы по обновлению


-   Любые виртуальные пакеты приложения, упорядоченные в версии 4,2, не должны повторно использоваться для использования с версией 4,5. Однако рекомендуется обновить виртуальные пакеты до формата Microsoft Application Virtualization 4,5, если вы хотите применить стандартные списки управления доступом (ACL) или создать файл установщика Windows. Это простой процесс, и необходимо, чтобы в приложении App-V 4,5 был открыт и сохранен существующий пакет виртуального приложения. Это можно автоматизировать с помощью интерфейса командной строки App-VSequencer. Дополнительные сведения [можно найти в разделе Создание и обновление виртуальных приложений с помощью секвенсора App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md) .

-   Одной из функций секвенсора 4,5 является возможность создания файлов установщика Windows (MSI) как контрольных точек для обеспечения взаимодействия виртуальных пакетов приложений с помощью электронных средств распространения программного обеспечения (например, Microsoft Endpoint Configuration Manager). Предыдущие файлы установщика Windows, созданные с помощью средства MSI для виртуализации приложений, которые были установлены в клиенте App-V 4,1 или 4,2, которые впоследствии будут обновлены до версии App-V 4,5, продолжают работать, но не могут быть установлены в клиенте App-V 4,5. Тем не менее, они не могут быть удалены или обновлены, если они не были обновлены в секвенсоре App-V 4,5. Исходный пакет App-V, более ранний, чем 4,5, должен быть открыт в секвенсоре App-V 4,5, а затем сохранен как файл установщика Windows.

    **Примечание.**  
    Если клиент App-V 4,2 уже обновлен до App-V 4,5, возможно, вы можете создать сценарий временного решения, чтобы сохранить пакеты версии 4,2 на клиентах версии 4,5 и позволить им управлять ими. Этот сценарий должен скопировать два файла, msvcp71.dll и msvcr71.dll в папку установки App-V и указать следующие значения в разделе реестра: \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:

    "ClientVersion" = "4.2.1.20"

    "GlobalDataDirectory" = "C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (доступное для записи глобальное расположение)



-   Файлы установщика Windows, созданные с помощью секвенсора App-V 4,5, выводят сообщение об ошибке "для этого пакета требуется клиент Microsoft Application Virtualization 4,5 или более поздней версии при попытке запустить их в клиенте App-V 4,6. Откройте старый пакет с помощью секвенсора App-V 4,5 с пакетом обновления 1 (SP1) или секвенсор App-V 4,6, а затем создайте новый MSI-файл для пакета.

-   Любые созданные и сохраненные отчеты версии 4,2 будут перезаписаны при обновлении сервера до версии 4,5. Если вы хотите сохранить эти отчеты, необходимо сохранить резервную копию файла SftMMC. msc, расположенную в папке консоли управления SoftGrid на сервере, и использовать эту копию для замены нового SftMMC. msc, установленного во время обновления.

-   Дополнительные сведения об обновлении предыдущей версии [можно найти в статье обновление до Microsoft Application Virtualization 4,5 (вопросы и ответы](https://go.microsoft.com/fwlink/?LinkId=120358) ) https://go.microsoft.com/fwlink/?LinkId=120358) .

## <a href="" id="app-v-4-6-client-package-support-"></a>Поддержка пакета клиента App-V 4,6


Вы можете развертывать пакеты, созданные в предыдущих версиях App-V, в клиентах App-V 4,6. Тем не менее, необходимо изменить связанный OSD файл, чтобы он включал соответствующую информацию об операционной системе и архитектуре микросхем. Можно использовать следующие значения:

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Значение ОС</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>&lt;ЗНАЧЕНИЕ ОС = "Win2003TS"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;ЗНАЧЕНИЕ ОС = "Win2003TS64"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;ЗНАЧЕНИЕ ОС = "Win2008TS"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;ЗНАЧЕНИЕ ОС = "Win2008TS64"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;ЗНАЧЕНИЕ ОС = "Win2008R2TS64"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;ЗНАЧЕНИЕ ОС = "Win7"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;ЗНАЧЕНИЕ ОС = "Win764"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;ЗНАЧЕНИЕ ОС = "WinVista"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;ЗНАЧЕНИЕ ОС = "WinVista64"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;ЗНАЧЕНИЕ ОС = "WinXP"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;ЗНАЧЕНИЕ ОС = "WinXP64"/&gt;</p></td>
</tr>
</tbody>
</table>



Чтобы запустить созданный 32-разрядный пакет, необходимо последовательное приложение на компьютере с 32-разрядной операционной системой, с установленным приложением Sequencer App-V 4,6. После упорядочения приложения в консоли секвенсор щелкните вкладку **развертывание** и укажите нужную архитектуру операционной системы и микросхемы.

**Важно.**  
Приложения, упорядоченные на компьютере под управлением 64-разрядной операционной системы, должны развертываться на компьютерах с 64-разрядной операционной системой. Новые 32-разрядные пакеты, созданные с помощью программы Sequencer App-v 4,6, не выполняются на компьютерах, на которых запущен клиент App-V 4,5.



Для выполнения новых 64-разрядных пакетов в клиенте App-V 4,6 необходимо последовательное приложение на компьютере с запущенным приложением Sequencer App-V 4,6 и работающей под управлением 64-разрядной операционной системы. После того как приложение будет упорядочено, откройте вкладку " **развертывание** ", а затем укажите нужную архитектуру операционной системы и микросхемы.

В следующей таблице перечислены клиентские версии, которые будут запускать пакеты, созданные с использованием различных версий секвенсора.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Упорядочение с помощью секвенсора App-V 4,2</th>
<th align="left">Упорядочение с помощью секвенсора App-V 4,5</th>
<th align="left">Последовательное использование 32-разрядного приложения Sequencer-V 4,6</th>
<th align="left">Последовательное использование 64-разрядного приложения Sequencer-V 4,6</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>клиент 4,2</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>Нет</p></td>
</tr>
<tr class="even">
<td align="left"><p>клиент 4,5 ¹</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>Нет</p></td>
</tr>
<tr class="odd">
<td align="left"><p>клиент 4,6 (32-разр.)</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Нет</p></td>
</tr>
<tr class="even">
<td align="left"><p>клиент 4,6 (64-разр.)</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
</tbody>
</table>



¹ применимы ко всем версиям клиента App-V 4,5, включая App-V 4,5, App-v 4,5 CU1 и App-V 4,5 SP1.









