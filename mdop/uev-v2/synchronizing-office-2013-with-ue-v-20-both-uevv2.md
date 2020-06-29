---
title: Синхронизация Office 2013 с UE-V 2,0
description: Синхронизация Office 2013 с UE-V 2,0
author: dansimp
ms.assetid: c46feb6d-28a8-4799-888d-053531dc5842
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9b079d3f21e6ced689fa2101f5321fa9b1406c8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826889"
---
# Синхронизация Office 2013 с UE-V 2,0


Microsoft User Experience Virtualization (UE-V) 2,0 поддерживает синхронизацию параметров приложений Microsoft Office 2013 с помощью шаблона, доступного из коллекции шаблонов UE-V. Сочетание поддержки UE-V 2 и App-V 5,0 с пакетом обновления 2 (SP2) для Office 2013 профессиональный плюс обеспечивает одинаковый интерфейс для виртуализированного экземпляра Office 2013 с любого устройства или виртуального рабочего стола с поддержкой UE-V.

Чтобы активировать поддержку параметров приложений UE-V в Office 2013, вы можете скачать официальные шаблоны UE-V Office 2013 из [коллекции шаблонов Microsoft User Experience Virtualization (UE-v) 2](https://go.microsoft.com/fwlink/p/?LinkId=246589). Этот ресурс предоставляет шаблоны расположений параметров Microsoft, разработанные корпорацией Майкрософт, а также шаблоны расположений параметров в сообществе.

## Поддержка Microsoft Office в UE-V


UE-V 1,0 и UE-V 2 содержат шаблоны расположений параметров для Microsoft Office 2010. Эти шаблоны распространяются и регистрируются в рамках процесса установки UE-V Agent. Эти шаблоны помогают синхронизировать взаимодействие пользователей между устройствами. Шаблоны UE-V для Office 2013 предоставляют очень похожие параметры для шаблонов Office 2010. Параметры Microsoft Office 2013, перемещенные с помощью Office 365, не включаются в эти параметры. Список параметров, относящихся к Office 365, можно найти в статье [Обзор параметров пользователей и роуминга для Office 2013](https://go.microsoft.com/fwlink/p/?LinkId=391220).

## Синхронизированные параметры Office 2013


В следующих таблицах содержатся сведения о поддержке Office 2013 в UE-V:

### Поддерживаемые шаблоны UE-V для Microsoft Office

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Шаблоны Office 2013 (UE-V 2,0, доступные в коллекции UE-V):</th>
<th align="left">Шаблоны Office 2010 (UE-V 1,0 &amp; 1,0 SP1):</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftOffice2013Win32.xml</p>
<p>MicrosoftOffice2013Win64.xml</p>
<p>MicrosoftLync2013Win32.xml</p>
<p>MicrosoftLync2013Win64.xml</p></td>
<td align="left"><p>MicrosoftOffice2010Win32.xml</p>
<p>MicrosoftOffice2010Win64.xml</p>
<p>MicrosoftLync2010.xml</p>
<p></p></td>
</tr>
</tbody>
</table>

 

### Приложения Microsoft Office, поддерживаемые шаблонами UE-V

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Access 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft Word 2013</p>
<p>Диспетчер отправки Microsoft Office</p></td>
<td align="left"><p>Microsoft Access 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft SharePoint Designer 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft Word 2010</p>
<p></p></td>
</tr>
</tbody>
</table>

 

## Развертывание шаблонов Office 2013


Вы можете развернуть шаблон расположения параметров UE-V следующими способами:

-   **Регистрация шаблона с помощью PowerShell**. Если вы используете Windows PowerShell для управления компьютерами, выполните следующую команду Windows PowerShell открыть в качестве администратора, чтобы зарегистрировать этот шаблон расположения параметров.

    ``` syntax
    Register-UevTemplate -Path <Path_to_Template>
    ```

    Дополнительные сведения об использовании UE-V и Windows PowerShell см. [в разделе Управление шаблонами расположений параметров ue-v 2. x с помощью Windows PowerShell и WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).

-   **Зарегистрируйте шаблон с помощью пути к каталогу шаблонов**. Если вы используете путь к каталогу шаблонов параметров для управления шаблонами на компьютерах пользователей, скопируйте шаблон Office 2013 в папку, определенную в агенте UE-V Agent. В следующий раз при выполнении запланированной задачи шаблона "автоматическое обновление" (ApplySettingsCatalog.exe) на устройстве будет зарегистрирован шаблон расположения параметров. Дополнительные сведения можно найти [в разделе развертывание каталога шаблонов параметров для UE-V 2](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue).

-   **Регистрация шаблона с помощью Configuration Manager**. Если вы используете Configuration Manager для управления шаблонами хранилища параметров UE-V, создайте CAB шаблона, импортируйте его в Configuration Manager, а затем выполните развертывание базового плана для клиентов. Дополнительные сведения можно найти в руководстве, приведенном в документации по [пакету конфигурации System Center 2012 для Microsoft User Experience Virtualization 2](https://go.microsoft.com/fwlink/?LinkId=317263).






 

 





