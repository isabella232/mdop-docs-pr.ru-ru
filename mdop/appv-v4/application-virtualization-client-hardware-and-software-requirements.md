---
title: Требования клиента Application Virtualization к оборудованию и программному обеспечению
description: Требования клиента Application Virtualization к оборудованию и программному обеспечению
author: dansimp
ms.assetid: 8b877a2c-5721-4b22-a47f-e2838d58ab12
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5b828f59ba36099b4f6a545cd5bbcb3c72d24e3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819732"
---
# Требования клиента Application Virtualization к оборудованию и программному обеспечению


В этой статье описаны рекомендованные минимальные конфигурации оборудования и программного обеспечения для установки клиента для настольного компьютера Application Virtualization и клиента Application Virtualization для служб удаленных рабочих столов (ранее — служб терминалов).

## Классическое приложение Application Virtualization


В следующем списке приведены рекомендуемые минимальные требования к оборудованию и программному обеспечению для клиента Application Virtualization для настольных компьютеров. Требования перечислены в первую очередь для Microsoft Application Virtualization (App-V) 4.6 SP2, за которым следуют требования для версий, предшествующих App-V 4.6 SP2.

**Примечание**  Классическое приложение Application Virtualization (App-V) не требует наличия дополнительных ресурсов процессора или ОЗУ сверх требований операционной системы узла.

 

### Требования к оборудованию

Требования к оборудованию применимы ко всем версиям.

-   Процессор — ознакомьтесь с рекомендуемыми системными требованиями для используемой операционной системы.

-   ОЗУ — Рекомендуемые системные требования для используемой операционной системы.

-   Диск — 30MB для установки и 6GB кэша.

### Требования к программному обеспечению для App-V 4,6 SP2

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Архитектура SKU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Профессиональный выпуск</p></td>
<td align="left"><p>ОБНОВЛЕНИЙ</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Бизнес, Корпоративная или максимальная выпускная версия</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Профессиональная, Корпоративная или Максимальная версия</p></td>
<td align="left"><p>Пакет обновления или пакет обновления 1 (SP1) отсутствуют</p></td>
<td align="left"><p>x86 и x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Pro или Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 и x64</p></td>
</tr>
</tbody>
</table>

Следующие требования к программному обеспечению устанавливаются автоматически при использовании Setup.exe метода. Если вы используете программу установки Setup.msi, сначала необходимо установить следующие продукты.
- **Распространяемый пакет Microsoft Visual c++ 2005 SP1 (x86)**— дополнительные сведения об установке распространяемого пакета Microsoft visual C++ 2005 SP1 (x86) можно найти в [распространяемом пакете microsoft Visual c++ 2005 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) ( https://go.microsoft.com/fwlink/?LinkId=119961) . Для версии 4,5 SP2 клиента App-V Скачайте Vcredist\_x86.exe из [распространяемого пакета Microsoft Visual C++ 2005 с пакетом обновления 1](https://go.microsoft.com/fwlink/?LinkId=169360) (SP1), для которого предназначено обновление безопасности ATL ( https://go.microsoft.com/fwlink/?LinkId=169360) .
  -   **Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)**— дополнительные сведения об установке Microsoft Core XML Services (msxml) 6,0 SP1 (x86) можно найти в статьях [Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) ( https://go.microsoft.com/fwlink/?LinkId=63266) .

Для клиентского клиента Application Virtualization (App-V) 4,6 для настольных компьютеров автоматически устанавливается следующий дополнительный программный компонент, если вы используете метод Setup.exe. Если вы используете программу установки Setup.msi, необходимо также установить другие необходимые условия.

-   **Распространяемый пакет Microsoft VisualC + + 2008SP1 (x86)**— дополнительные сведения об установке Microsoft VisualC + + 2008 SP1 (x86) можно найти в [свободном распространяемом пакете Microsoft VisualC + + 2008 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=150700) ( https://go.microsoft.com/fwlink/?LinkId=150700) .

### Требования к программному обеспечению для версий, предшествующих App-V 4,6 SP2

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Архитектура SKU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Профессиональный выпуск</p></td>
<td align="left"><p>SP2 или 3 (SP3)</p></td>
<td align="left"><p>x86 и x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Бизнес, Корпоративная или максимальная выпускная версия</p></td>
<td align="left"><p>Пакет обновления, пакет обновления 1 (SP1) или пакет обновления 2 (SP2)</p></td>
<td align="left"><p>x86 и x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7 ¹</p></td>
<td align="left"><p>Профессиональная, Корпоративная или Максимальная версия</p></td>
<td align="left"><p>Пакет обновления или пакет обновления 1 (SP1) отсутствуют</p></td>
<td align="left"><p>x86 и x64</p></td>
</tr>
</tbody>
</table>
¹ поддерживается для App-V 4,5 SP1 и SP2, App-V 4,6 и 4,6 SP1.

Классическое приложение Application Virtualization (App-V) 4,6 поддерживает версии x86 и x64 для этих операционных систем.

Следующие требования к программному обеспечению устанавливаются автоматически при использовании Setup.exe метода. Если вы используете программу установки Setup.msi, сначала необходимо установить следующие продукты.

-   <strong>Распространяемый пакет Microsoft Visual C++ 2005 SP1 (x86) </strong> — Дополнительные сведения об установке распространяемого пакета Microsoft Visual c++ 2005 SP1 (x86) можно найти в <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961)"> распространяемом пакете Microsoft visual C++ 2005 SP1 (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=119961"> https://go.microsoft.com/fwlink/?LinkId=119961 </a> ). Для версии 4,5 с пакетом обновления 2 (SP2) для клиента App-V Скачайте Vcredist_x86.exe из <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="[Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360)"> распространяемого пакета Microsoft Visual C++ 2005 с пакетом обновления 1 (SP1), обновление для системы безопасности ATL </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=169360"> https://go.microsoft.com/fwlink/?LinkId=169360 </a> ).

-   <strong>Microsoft Core XML Services (MSXML) 6,0 SP1 (x86) </strong> — Дополнительные сведения об установке Microsoft Core XML Services (MSXML) 6,0 SP1 (x86) можно найти в статьях <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="[Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266)"> Microsoft Core XML Services (msxml) 6,0 SP1 (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=63266"> https://go.microsoft.com/fwlink/?LinkId=63266 </a> ).

-   <strong>Сообщения об ошибках приложений Microsoft </strong> — программа установки для этого программного обеспечения входит <strong> в </strong> папку Support\Watson в самораспаковывающемся архивном файле.

Для клиентского клиента Application Virtualization (App-V) 4,6 для настольных компьютеров автоматически устанавливается следующий дополнительный программный компонент, если вы используете метод Setup.exe. Если вы используете программу установки Setup.msi, необходимо также установить другие необходимые условия.

-   <strong>Распространяемый пакет Microsoft Visual C++ 2008 SP1 (x86) </strong> — Дополнительные сведения об установке распространяемого пакета Microsoft Visual c++ 2008 SP1 (x86) можно найти в <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="[Microsoft Visual C++ 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700)"> распространяемом пакете Microsoft visual C++ 2008 SP1 (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=150700"> https://go.microsoft.com/fwlink/?LinkId=150700 </a> ).

## Клиент Application Virtualization для служб удаленных рабочих столов

Ниже приведены рекомендуемые требования к оборудованию и программному обеспечению для клиента Application Virtualization для служб удаленных рабочих столов. Требования перечислены в первую очередь для appv461_3, а затем требования к версиям, предшествующим App-V 4,6 SP2.

Клиент Application Virtualization (App-V) для служб удаленных рабочих столов не требует дополнительных ресурсов процессора или ОЗУ сверх требований операционной системы узла.

### Требования к оборудованию

Требования к оборудованию применимы ко всем версиям.

-   Процессор — ознакомьтесь с рекомендуемыми системными требованиями для используемой операционной системы.

-   ОЗУ — Рекомендуемые системные требования для используемой операционной системы. Эти требования также зависят от количества пользователей и приложений.

-   Диск — 30MB для установки и 6GB кэша.

### Требования к программному обеспечению для App-V 4,6 SP2

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Архитектура SKU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 и x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 и x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления или пакет обновления 1 (SP1) отсутствуют</p></td>
<td align="left"><p>x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

Следующие требования к программному обеспечению устанавливаются автоматически при использовании Setup.exe метода. Если вы используете программу установки Setup.msi, сначала необходимо установить следующие продукты.

-   **Распространяемый пакет Microsoft VisualC + + 2005SP1 (x86)**— дополнительные сведения об установке Microsoft VisualC + + 2005 SP1 (x86) можно найти в [свободном распространяемом пакете Microsoft VisualC + + 2005 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) ( https://go.microsoft.com/fwlink/?LinkId=119961) . Для версии 4.5 SP2 клиента App-V Скачайте Vcredist\_x86.exe из [распространяемого пакета Microsoft Visual C++ 2005 с пакетом обновления 1 (SP1), обновление для системы безопасности ATL](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360) .

-   **Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)**— дополнительные сведения об установке Microsoft Core XML Services (MSXML) 6.0 SP1 (x86) можно найти в статьях [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) ( https://go.microsoft.com/fwlink/?LinkId=63266) .

-   **Сообщения об ошибках приложений Microsoft**— программа установки для этого программного обеспечения входит в папку **Support\\Watson** в самораспаковывающемся архивном файле.

Для клиентского клиента Application Virtualization (App-V) 4,6 для настольных компьютеров автоматически устанавливается следующий дополнительный программный компонент, если вы используете метод Setup.exe. Если вы используете программу установки Setup.msi, необходимо также установить другие необходимые условия.

-   **Распространяемый пакет Microsoft VisualC + + 2008SP1 (x86)**— дополнительные сведения об установке Microsoft VisualC + + 2008 SP1 (x86) можно найти в [свободном распространяемом пакете Microsoft VisualC + + 2008 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=150700) ( https://go.microsoft.com/fwlink/?LinkId=150700) .

### Требования к программному обеспечению для версий, предшествующих App-V 4,6 SP2

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Архитектура SKU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows server2003</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 и x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>Нет пакета обновления или пакета обновления 2 (SP2)</p></td>
<td align="left"><p>x86 и x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 и x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления или пакет обновления 1 (SP1) отсутствуют</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

Клиент Application Virtualization (App-V) 4,6 для служб удаленных рабочих столов поддерживает конфигурации x86 и x64 для этих операционных систем.

## Статьи по теме
- [Требования программы Application Virtualization Sequencer к оборудованию и программному обеспечению](application-virtualization-sequencer-hardware-and-software-requirements.md)
- [Требования к системе при работе с Application Virtualization](application-virtualization-system-requirements.md)
- [Установка клиента с помощью командной строки](how-to-install-the-client-by-using-the-command-line-new.md)
- [Установка клиента Application Virtualization Client вручную](how-to-manually-install-the-application-virtualization-client.md)
- [Обновление клиента Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)
