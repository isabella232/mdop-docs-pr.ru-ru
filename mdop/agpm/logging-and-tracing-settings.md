---
title: Параметры ведения журнала и трассировки
description: Параметры ведения журнала и трассировки
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820589"
---
# Параметры ведения журнала и трассировки


Параметры шаблона администрирования для расширенного управления групповыми политиками позволяют централизованно настраивать параметры ведения журнала и трассировки для серверов и клиентов, которым применяется объект групповой политики (GPO) с этими параметрами.

Следующий параметр доступен в разделе Computer Configuration\\Administrative Templates\\Windows Components\\AGPM в **редакторе объектов групповой политики** при редактировании GPO в консоли управления групповыми политиками (GPMC). Если этот путь не отображается, щелкните правой кнопкой мыши папку **Административные шаблоны**и добавьте шаблон для расширенного управления групповыми политиками (, ADMX. adm).

**Расположение файлов трассировки**:

-   Клиент:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

-   Сервер:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log

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
<td align="left"><p><strong>Ведение журнала РАСШИРЕНного протоколирования</strong></p></td>
<td align="left"><p>Если включено, этот параметр определяет, включена ли трассировка, и уровень детализации. Этот параметр влияет на клиентские и серверные компоненты с расширенным управлением групповыми политиками.</p>
<p>Если отключено или не задано, этот параметр не действует.</p></td>
</tr>
</tbody>
</table>

 

### Дополнительные ссылки

-   [Параметры административных шаблонов](administrative-template-settings.md)

 

 





