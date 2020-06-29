---
title: Определение типа приложения для последовательной последовательности (App-V 4,6 SP1)
description: Определение типа приложения для последовательной последовательности (App-V 4,6 SP1)
author: dansimp
ms.assetid: 936abee2-98f1-45fb-9f0d-786e1d7464b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 001f6afa36ca28eb1b8e0cc2ccc161cef4194d24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817489"
---
# Определение типа приложения для последовательной последовательности (App-V 4,6 SP1)


Вы можете поочередно использовать три основных типа приложений с помощью секвенсора Microsoft Application Virtualization (App-V).

## Определение типа приложения для последовательной последовательности


Ниже приведена таблица, в которой определяется тип приложения, который нужно последовательное, а также приведены дополнительные сведения о том, как последовательное приложение.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Тип приложения</th>
<th align="left">Описание</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Standard</p></td>
<td align="left"><p>Выберите этот параметр, чтобы создать пакет, который будет содержать приложение или набор приложений. Этот параметр необходимо выбрать для большинства приложений, которые планируется поочередно.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-standard-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Standard Application (App-V 4.6 SP1)](how-to-sequence-a-new-standard-application--app-v-46-sp1-.md)">Виртуализация нового стандартного приложения (App-V 4.6 с пакетом обновления 1 (SP1))</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Надстройка или плагин</p></td>
<td align="left"><p>Выберите этот параметр, чтобы создать пакет, который расширяет функциональные возможности стандартного приложения, например плагин для Microsoft Excel. Кроме того, вы можете использовать подключаемые модули для приложений, установленных в собственном коде, или другой пакет, связанный с помощью динамической композиции наборов. Дополнительные сведения о композиции динамических наборов вы узнаете, <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> как использовать динамическую композицию набора </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)](how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md)">Виртуализация нового надстройки или подключаемого модуля (App-V 4.6 с пакетом обновления 1 (SP1))</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Старые</p></td>
<td align="left"><p>Выберите этот параметр, чтобы создать пакет, который необходим стандартному приложению, например Microsoft .NET Framework. Пакеты по промежуточного слоя используются для связывания с другими пакетами с помощью композиции динамических наборов. Дополнительные сведения о композиции динамических наборов вы узнаете, <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> как использовать динамическую композицию набора </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Middleware Application (App-V 4.6 SP1)](how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md)">Виртуализация нового ПО промежуточного слоя (App-V 4.6 с пакетом обновления 1 (SP1))</a></p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Задачи для Application Virtualization Sequencer (App-V 4.6 с пакетом обновления 1 (SP1))](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





