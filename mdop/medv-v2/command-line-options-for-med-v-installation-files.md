---
title: Параметры командной строки для файлов установки MED-V
description: Параметры командной строки для файлов установки MED-V
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826469"
---
# Параметры командной строки для файлов установки MED-V


При установке или удалении Microsoft Enterprise Virtualization (MED-V) 2,0 вы сможете запускать установочные файлы в командной строке. В этом разделе описаны различные параметры, которые можно задать при установке или удалении MED-V из командной строки.

### Аргументы командной строки

Вы можете использовать указанные ниже аргументы командной строки вместе с соответствующими файлами установки для MED-V.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Файл установки</th>
<th align="left">Аргумент</th>
<th align="left">Допустимые значения</th>
<th align="left">Тип</th>
<th align="left">Описание</th>
<th align="left">По умолчанию</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Агент узла</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;путь установки&gt;</p></td>
<td align="left"><p>Установка</p></td>
<td align="left"><p>Изменение установленного каталога</p></td>
<td align="left"><p>При установке программы Files\Microsoft Корпоративная виртуализация рабочих столов.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Диспетчер рабочих областей для MED-V</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;путь установки&gt;</p></td>
<td align="left"><p>Установка</p></td>
<td align="left"><p>Изменение установленного каталога</p></td>
<td align="left"><p>При установке программы Files\Microsoft Корпоративная виртуализация рабочих столов.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Рабочая область MED-V</p></td>
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;путь установки&gt;</p></td>
<td align="left"><p>Установка</p></td>
<td align="left"><p>Изменение установленного каталога</p></td>
<td align="left"><p>Установка переходит на ProgramData\Microsoft\Medv\Workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Рабочая область MED-V</p></td>
<td align="left"><p>ПЕРЕЗАПИСАТЬ VHD</p></td>
<td align="left"><p>0или1</p></td>
<td align="left"><p>Установка</p></td>
<td align="left"><p>Установка завершается сбоем, если существует VHD (0) или перезаписать существующий виртуальный жесткий диск (1).</p></td>
<td align="left"><p>Перезапись не происходит, и установка завершается сбоем, если виртуальный жесткий диск (VHD) уже существует.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Рабочая область MED-V</p></td>
<td align="left"><p>SUPPRESSMEDVLAUNCH</p></td>
<td align="left"><p>0или1</p></td>
<td align="left"><p>Установка</p></td>
<td align="left"><p>Начало (0) или не запускается (1) MED-V после установки рабочей области для MED-V.</p></td>
<td align="left"><p>Если Рабочая область MED-V была установлена с пользовательским интерфейсом, флажок на <strong> странице "Готово" определяет, </strong> следует ли запускать med-v.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Рабочая область MED-V</p></td>
<td align="left"><p>DELETEDIFFDISKS</p></td>
<td align="left"><p>0или1</p></td>
<td align="left"><p>Удаление</p></td>
<td align="left"><p>Сохранить (0) или удалить (1) виртуальные жесткие диски, созданные MED-V</p></td>
<td align="left"><p>Виртуальные жесткие диски не удаляются.</p></td>
</tr>
</tbody>
</table>

 

### Примеры аргументов командной строки

В следующем примере выполняется установка рабочей области MED-V, созданной с помощью диспетчера рабочих областей MED-V. Файл установки создает файл журнала в каталоге TEMP и запускает установочный файл в тихом режиме, но не запускает агент узла MED-V по завершении. Установочный файл перезаписывает все VHD-файлы, оставшиеся после предыдущей установки с тем же именем.

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

В следующем примере удаляется Рабочая область MED-V, которая ранее была установлена. Файл установки создает файл журнала в каталоге TEMP и запускает установочный файл в тихом режиме. Установочный файл удаляет все оставшиеся файлы виртуального жесткого диска из файловой системы.

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## Статьи по теме


[Развертывание компонентов MED-V](deploy-the-med-v-components.md)

[Технический справочник по MED-V](technical-reference-for-med-v.md)

 

 





