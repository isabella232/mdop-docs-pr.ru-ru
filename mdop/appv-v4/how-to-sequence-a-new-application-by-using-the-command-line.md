---
title: Виртуализация нового приложения с помощью командной строки
description: Виртуализация нового приложения с помощью командной строки
author: dansimp
ms.assetid: c3b5c842-6a91-4d0a-9a22-c7b8d1aeb09a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea7b1222dc00a0a4649cb342ac1ba41338484889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816689"
---
# Виртуализация нового приложения с помощью командной строки


Вы можете использовать командную строку для последовательного создания нового приложения. Командная строка полезна, если вам нужно создать большое количество виртуальных приложений или при необходимости создавать последовательные приложения на регулярной основе.

**Важно.**  
Последовательность команд в командной строке позволяет выполнять последовательности только по умолчанию. Если необходимо изменить параметры установки по умолчанию для упорядоченного приложения, необходимо либо вручную изменить виртуальное приложение, либо обновить виртуальное приложение с помощью секвенсора Application Virtualization (App-V). Дополнительные сведения об обновлении виртуального приложения с помощью секвенсора App-V вы узнаете, [как обновить существующее виртуальное приложение](how-to-upgrade-an-existing-virtual-application.md).



Чтобы создать виртуальное приложение с помощью командной строки, выполните указанные ниже действия.

**Упорядочение приложения с помощью командной строки**

1.  На компьютере с секвенсором App-V откройте командную команду, выбрав **Пуск**, **выполнить**, а затем введите **cmd**. Нажмите кнопку **ОК**.

2.  С помощью командной строки укажите расположение, где установлен секвенсор App-V. Например, в командной строке введите следующую команду: **C:\\program Files Files\\Microsoft Application Virtualization Sequencer**.

3.  В командной строке введите следующую команду, заменив текст в кавычках на значения:

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **Примечание.**  
    Вы можете указать дополнительные параметры, используя командную строку, в зависимости от сложности приложения, которое вы собираетесь поочередно. Полный список параметров, которые можно использовать с секвенсором App-V, приведен в разделе [Параметры командной строки программы Sequencer](sequencer-command-line-parameters.md).



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specify the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. Нажмите клавишу **Ввод**.

## Статьи по теме


[Создание и обновление виртуальных приложений с помощью секвенсора App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[Коды ошибок командной строки программы Sequencer](sequencer-command-line-error-codes.md)

[Параметры командной строки программы Sequencer](sequencer-command-line-parameters.md)









