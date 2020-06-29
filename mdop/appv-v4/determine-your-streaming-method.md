---
title: Определение способа потоковой передачи
description: Определение способа потоковой передачи
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821669"
---
# Определение способа потоковой передачи


При первом нажатии пользователем значка, который был размещен на компьютере с помощью процесса публикации, клиент Application Virtualization получит содержимое пакета виртуального приложения из расположения для потоковой передачи.

**Примечание** 
 *Потоковая передача* — это термин, используемый для описания процесса получения содержимого из упорядоченного пакета приложения, начиная с основного блока функций и получая дополнительные блоки по мере необходимости.

 

Расположение исходного потока обычно является сервером, доступным для компьютера пользователя; Однако некоторые электронные системы рассылки, такие как диспетчер конфигурации конечной точки Майкрософт, могут распространять SFT-файл на компьютер пользователя, а затем передавать виртуальный пакет виртуального приложения локально из кэша этого компьютера.

**Примечание**  Расположение источника потока для виртуальных пакетов можно настроить на компьютере, который не является сервером. Это особенно удобно в небольших офисах филиалов без сервера.

 

В следующей таблице описаны источники потоков, которые можно использовать для хранения упорядоченных приложений.

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
<td align="left"><p>Файл</p></td>
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
<li><p>Поддерживает улучшенную безопасность по протоколу HTTPS.</p></li>
<li><p>Поддерживает потоковую передачу на удаленные компьютеры через Интернет</p></li>
<li><p>Только один порт в брандмауэре, чтобы открыть</p></li>
<li><p>Высоко масштабируемый</p></li>
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
<li><p>Только один порт в брандмауэре для открытия (только для RTSP)</p></li>
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


[Сценарий на основе электронного распространения программного обеспечения](electronic-software-distribution-based-scenario.md)

[Обзор сценария на основе электронного распространения программного обеспечения](electronic-software-distribution-based-scenario-overview.md)

[Определение способа публикации](determine-your-publishing-method.md)

 

 





