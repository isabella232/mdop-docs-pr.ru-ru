---
title: Обновление виртуального приложения с помощью командной строки
description: Обновление виртуального приложения с помощью командной строки
author: dansimp
ms.assetid: 83c97767-6ea1-42aa-b411-ccc9fa61cf81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8612deb31a1692dd85cfee88ca4b18cbc5ac2ab2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816462"
---
# Обновление виртуального приложения с помощью командной строки


Выполните описанные ниже действия, чтобы обновить виртуальное приложение с помощью командной строки.

**Обновление виртуального приложения**

1.  На компьютере, на котором запущено приложение Application Virtualization (App-V), чтобы открыть командную команду, выберите **Пуск**, **выполнить**и введите **cmd**. Нажмите кнопку **ОК**.

2.  В командной строке укажите расположение, в котором установлен секвенсор App-V. Например, в командной строке введите следующую команду: **C:\\program Files Files\\Microsoft Application Virtualization Sequencer**.

3.  В командной строке введите следующую команду, заменив текст в кавычках на значения:

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **Примечание.**  
    Вы можете указать дополнительные параметры, используя командную строку в зависимости от сложности обновляемого приложения. Полный список параметров, которые можно использовать с секвенсором App-V, приведен в разделе [Параметры командной строки программы Sequencer](sequencer-command-line-parameters.md).



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
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
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









