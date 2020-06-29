---
title: Планирование решения для потоковой передачи при внедрении на основе сервера Application Virtualization Server
description: Планирование решения для потоковой передачи при внедрении на основе сервера Application Virtualization Server
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815869"
---
# Планирование решения для потоковой передачи при внедрении на основе сервера Application Virtualization Server


Если вы хотите использовать потоки управления виртуализацией приложений в сочетании с серверной реализацией Application Virtualization, вы можете выбрать один из нескольких альтернативных вариантов и воспользоваться преимуществами какой-либо инфраструктуры уже на месте. Например, если у вас уже есть серверы в офисах филиалов, вы можете поместить на них \\CONTENT виртуализации приложений, а затем настроить клиенты таким образом, чтобы они использовали этот контент в качестве источника контента приложения. Если вы выбрали только серверы управления виртуализацией приложений (например, если у вас есть только один набор Office), клиенты смогут передавать содержимое из этого сервера.

Поддерживаемые параметры включают использование файлового сервера, сервера IIS или потокового сервера Application Virtualization. Вы также можете установить потоковый сервер Application Virtualization на существующем файловом сервере или сервере IIS. Характеристики этих параметров описаны в таблице ниже.

**Примечание**  Функция активного обновления позволяет добавить новую версию приложения на сервер управления App-V или потоковый сервер, не затрагивая пользователей, которые в данный момент запускают приложение. Клиенты App-V будут автоматически получать последнюю версию приложения с сервера управления App-V или потокового сервера, когда пользователь в следующий раз запускает приложение. Для этой функции требуется использовать протокол RTSP (S).

 

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
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)">Настройка серверов Application Virtualization Streaming Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Сервер управления виртуализацией приложений</p></td>
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


[Сценарий на основе использования сервера Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Обзор компонентов системы Application Virtualization](overview-of-the-application-virtualization-system-components.md)

[Публикация виртуальных приложений с помощью серверов Application Virtualization Management Server](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





