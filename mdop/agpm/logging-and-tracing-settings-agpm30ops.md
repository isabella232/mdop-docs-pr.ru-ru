---
title: Параметры ведения журнала и трассировки
description: Параметры ведения журнала и трассировки
author: dansimp
ms.assetid: 858b6fbf-65b4-42fa-95a9-69b04e5734d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 078bda16b5fcf968d45e0c4890487471105e8c44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820592"
---
# Параметры ведения журнала и трассировки


Параметры шаблона администрирования для расширенного управления групповыми политиками позволяют централизованно настраивать параметры ведения журнала и трассировки для серверов и клиентов, которым применяется объект групповой политики (GPO) с этими параметрами.

Следующий параметр доступен в разделе Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM при редактировании объекта групповой политики.

**Расположение файлов трассировки**:

-   Клиент:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

-   Сервер:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Параметр</th>
<th align="left">Эффект</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ГРУППОВое протоколирование: Настройка ведения журнала</strong></p></td>
<td align="left"><p>Этот параметр политики позволяет включить и настроить ведение журнала для РАСШИРЕНного протоколирования. Этот параметр влияет на клиентские и серверные компоненты с расширенным управлением групповыми политиками.</p></td>
</tr>
</tbody>
</table>

 

### Дополнительные ссылки

-   [Папка административных шаблонов](administrative-templates-folder-agpm30ops.md)

 

 





