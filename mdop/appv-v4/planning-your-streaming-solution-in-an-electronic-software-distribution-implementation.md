---
title: Планирование решения для потоковой передачи при внедрении с помощью электронного распространения программного обеспечения
description: Планирование решения для потоковой передачи при внедрении с помощью электронного распространения программного обеспечения
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815859"
---
# Планирование решения для потоковой передачи при внедрении с помощью электронного распространения программного обеспечения


Если вы решили использовать потоковые серверы в сочетании с системой ESD, чтобы сделать содержимое приложения доступным для компьютеров конечных пользователей, вы можете выбрать один из нескольких вариантов и воспользоваться преимуществами какой бы то или другой инфраструктуры уже на своем компьютере. Например, если в системе ESD есть общий доступ к программному обеспечению на серверах в офисах филиалов, вы можете поместить \\CONTENT Application Virtualization на эти серверы и настроить клиенты таким образом, чтобы они использовали этот контент в качестве источника контента приложения. Поддерживаемые параметры включают использование файлового сервера или сервера IIS. Вы также можете установить потоковый сервер Application Virtualization на существующем файловом сервере или сервере IIS.

Потоковый сервер Application Virtualization обеспечивает поддержку функции активного обновления в Application Virtualization. Функция активного обновления позволяет добавить новую версию приложения на сервер управления App-V или потоковый сервер, не затрагивая пользователей, которые в данный момент запускают приложение. Клиенты App-V будут автоматически получать последнюю версию приложения с сервера управления App-V или потокового сервера, когда пользователь в следующий раз запускает приложение. Для этой функции требуется использовать протокол RTSP (S). Если вы решили не использовать потоковый сервер Application Virtualization, вам потребуется явно управлять обновлением пакета приложения с помощью системы ESD.

**Примечание**  Управление доступом к приложениям осуществляется с помощью групп безопасности доменных служб Active Directory, поэтому вам потребуется планировать процесс настройки группы безопасности для каждого виртуального приложения и для управления добавлением пользователей в каждую группу. Системный администратор Application Virtualization настраивает каждый потоковый сервер для использования этих групп Active Directory, применяя списки ACL к каталогам приложений в рамках общего доступа к СОДЕРЖИМому, которое управляет доступом к пакетам на основе членства в группе Active Directory.

 

Характеристики доступных потоковых параметров описаны в таблице ниже.

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
<th align="left">Тип сервера</th>
<th align="left">Используемый протокол</th>
<th align="left">Преимущества</th>
<th align="left">Недостатки</th>
<th align="left">Ссылки</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Файловый сервер</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><ul>
<li><p>Простое решение недорогих ресурсов для настройки существующего файлового сервера с \CONTENT</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Нет активного обновления</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)">Настройка файлового сервера</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Сервер IIS</p></td>
<td align="left"><p>HTTP/HTTPS</p></td>
<td align="left"><ul>
<li><p>Поддерживает улучшенную безопасность по протоколу HTTPS</p></li>
<li><p>Поддерживает потоковую передачу на удаленные компьютеры через Интернет</p></li>
<li><p>Только один порт в брандмауэре, чтобы открыть</p></li>
<li><p>Возможностью</p></li>
<li><p>Знакомый протокол</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Требуется управление IIS</p></li>
<li><p>Нет активного обновления</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)">Настройка сервера для служб IIS</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Потоковый сервер Application Virtualization</p></td>
<td align="left"><p>RTSP/RTSP</p></td>
<td align="left"><ul>
<li><p>Активное обновление</p></li>
<li><p>Поддержка расширенной защиты с помощью протокола RTSP</p></li>
<li><p>Только один порт в брандмауэре, чтобы открыть</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Двойная инфраструктура</p></li>
<li><p>Требование для администрирования сервера</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Настройка серверов Application Virtualization Management Server</a></p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Настройка серверов для развертывания на основе ESD](how-to-configure-servers-for-esd-based-deployment.md)

[Обзор защиты и безопасности](security-and-protection-overview.md)

[Публикация виртуальных приложений с помощью электронного распространения программного обеспечения](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





