---
title: Обзор компонентов системы Application Virtualization
description: Обзор компонентов системы Application Virtualization
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816052"
---
# Обзор компонентов системы Application Virtualization


В приведенной ниже таблице описаны основные компоненты системы управления виртуализацией приложений Microsoft. Дополнительные сведения о том, как развертывать эти компоненты системы, можно найти в разделе [сценарий на сервере Application Virtualization](application-virtualization-server-based-scenario.md).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Компонент</th>
<th align="left">Функция</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Сервер управления виртуализацией приложений Майкрософт</p></td>
<td align="left"><p>Компонент, ответственный за потоковую передачу содержимого пакета и публикацию ярлыков и сопоставлений типов файлов в клиенте Application Virtualization.</p></td>
<td align="left"><p>Сервер управления виртуализацией приложений поддерживает активное обновление, Управление лицензиями и базу данных, которые можно использовать для создания отчетов.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong></strong>Папка содержимого</p></td>
<td align="left"><p>Расположение пакетов Application Virtualization для потоковой передачи.</p></td>
<td align="left"><p>Эту папку можно найти в общем доступе на сервере управления виртуализацией приложений. Эта папка также может находиться в сети хранения данных (SAN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Консоль управления Microsoft Application Virtualization</p></td>
<td align="left"><p>Средство управления оснасткой MMC 3,0 для администрирования сервера виртуализации Microsoft Applications.</p></td>
<td align="left"><p>Этот компонент можно установить на сервере Microsoft Application Virtualization или на отдельной рабочей станции с MMC 3.0 и. Установлено приложение NET 2.0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Веб-служба управления виртуализацией приложений Майкрософт</p></td>
<td align="left"><p>Компонент, который отвечает за взаимодействие запросов на чтение и запись в хранилище данных Application Virtualization.</p></td>
<td align="left"><p>Этот компонент может быть установлен на сервере Microsoft Application Virtualization или на отдельном компьютере, на котором установлены службы IIS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Хранилище данных Microsoft Application Virtualization</p></td>
<td align="left"><p>Компонент, хранящийся в базе данных SQL и ответственный за хранение всей информации, связанной с инфраструктурой виртуализации приложений.</p></td>
<td align="left"><p>Эти сведения включают все записи приложений, назначения приложений и группы, ответственные за управление средой виртуализации приложений.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Сервер потоковой передачи Microsoft Application Virtualization</p></td>
<td align="left"><p>Компонент, ответственный за размещение пакетов Application Virtualization для потоковой передачи клиентам в филиале, где ссылка на сервер управления виртуализацией приложений считается глобальной сетью.</p></td>
<td align="left"><p>Этот сервер содержит только потоковую функциональность и не предоставляет ни консоль управления Application Virtualization, ни веб-службу управления виртуализацией приложений.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Sequencer</p></td>
<td align="left"><p>Компонент, который используется для мониторинга и сохранения установки приложений для создания виртуальных пакетов приложений.</p></td>
<td align="left"><p>Вывод состоит из значков приложения, OSD-файла, содержащего сведения о определении пакета, файла манифеста пакета и SFT-файла, содержащего файлы содержимого программы приложения.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Клиент Microsoft Application Virtualization</p></td>
<td align="left"><p>Компонент, установленный в классическом клиенте Application Virtualization или в клиенте Application Virtualization для служб удаленных рабочих столов (ранее — службы терминалов) и предоставляющий виртуальную среду для виртуализированных приложений.</p></td>
<td align="left"><p>Клиент Microsoft Application Virtualization управляет потоковой передачей пакета в кэш, обновлять публикацию, транспортировку и все взаимодействие с серверами Application Virtualization Server.</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Сценарий на основе использования сервера Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Планирование решения для потоковой передачи при внедрении на основе сервера Application Virtualization Server](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[Публикация виртуальных приложений с помощью серверов Application Virtualization Management Server](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





