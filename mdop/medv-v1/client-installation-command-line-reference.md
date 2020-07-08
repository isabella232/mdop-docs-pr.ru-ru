---
title: Справочник по командной строке установки клиента
description: Справочник по командной строке установки клиента
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826729"
---
# Справочник по командной строке установки клиента


**Установка MED-V из командной строки**

1.  В командной строке запустите пакет MED-V. msi и любые дополнительные параметры, описанные в приведенной ниже таблице.

2.  Пакет для MED-V. msi называется *MED-V\_x.msi*, где *x* — номер версии.

    Например, *MED-V\_1.0.65.msi*.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Параметр</th>
<th align="left">Значение</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>параметрами</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Автоматическая установка</p></td>
</tr>
<tr class="even">
<td align="left"><p>/log &lt; полный путь к файлу журнала&gt;</p></td>
<td align="left"><p>Полный путь к файлу журнала.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>Полный путь к каталогу установки.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>VMSFOLDER</p></td>
<td align="left"><p>Полный путь к папке виртуальной машины.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALL_ADMIN_TOOLS</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>По умолчанию: <strong> 0</strong></p></td>
<td align="left"><p>Установка средств администрирования для MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>START_AUTOMATICALLY</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>По умолчанию: <strong> 0</strong></p></td>
<td align="left"><p>Автоматически запускает клиент MED-V при каждом входе пользователя в систему Windows.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_ADDRESS</p></td>
<td align="left"><p>имя узла или IP-адрес</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SERVER_PORT</p></td>
<td align="left"><p>порт</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_SSL</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>для <strong> HTTPS </strong> или <strong> http</strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>START_MEDV</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>По умолчанию: <strong> 1</strong></p></td>
<td align="left"><p>Запускает MED-V после завершения установки MED-V.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Рекомендуется устанавливать START_MEDV = 0 в случае, если MED-V установлен системой.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>DESKTOP_SHORTCUT</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>По умолчанию: <strong> 1</strong></p></td>
<td align="left"><p>Создание ярлыка на рабочем столе, который запускает клиент MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MINIMAL_RAM_REQUIRED</p></td>
<td align="left"><p>ОЗУ (МБ)</p></td>
<td align="left"><p>При установке MED-V проверяет, не указан ли для компьютера минимальный объем ОЗУ. В противном случае установка прерывается.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SKIP_OS_CHECK</p></td>
<td align="left"><p><strong>1, 0</strong></p></td>
<td align="left"><p>Пропускает проверку операционной системы.</p></td>
</tr>
</tbody>
</table>











