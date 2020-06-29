---
title: Сведения о системе Microsoft Application Virtualization 4.6 с пакетом обновления 2 (SP2)
description: Сведения о системе Microsoft Application Virtualization 4.6 с пакетом обновления 2 (SP2)
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820019"
---
# Сведения о системе Microsoft Application Virtualization 4.6 с пакетом обновления 2 (SP2)


Microsoft Application Virtualization (App-V) 4.6 SP2 предлагает несколько улучшений и новых функций, описанных в этой статье.

**Внимание!**  В этой статье описано, как изменить реестр Windows с помощью редактора реестра. Если изменить реестр Windows некорректно, это может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows. Перед изменением реестра необходимо создать резервную копию файлов реестра (System. dat и User. dat). Корпорация Майкрософт не несет ответственности за то, что проблемы, которые могут возникнуть при изменении реестра, могут быть устранены. Изменение реестра на свой страх и риск.

 

**Поддержка Windows 8 и Windows Server 2012**

App-V 4.6 SP2 добавляет поддержку служб удаленных рабочих столов для Windows 8 и Windows Server 2012.

**Поддержка сосуществования с помощью клиента App-V 5,0**

Приложение App-V 4.6 SP2 обеспечивает поддержку сосуществования с помощью клиента Microsoft Application Virtualization 5,0. Ознакомьтесь с документацией по App-V 5,0, чтобы узнать о том, как настроить клиент App-V 5,0 для сосуществования с помощью клиента App-V 4.6 SP2. Дополнительные сведения о App-V 5,0 можно найти в разделе [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) в TechNet.

**Возможность виртуализации Adobe Reader X с использованием защищенного режима**

Вы можете виртуализировать приложение Adobe Reader X с включенным параметром защищенного режима, выполнив описанные ниже действия. Прежде чем приходилось отключить защищенный режим, чтобы виртуализировать приложение Adobe Reader X.

Перед запуском программы Sequencer App-V создайте следующий параметр реестра в разделе HKEY \ _LOCAL \ _MACHINE \\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Имя</p></td>
<td align="left"><p>Тип</p></td>
<td align="left"><p>Данные</p></td>
<td align="left"><p>Описание</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableVFSPassthrough</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>1,1</p></td>
<td align="left"><p>Установите для этого параметра значение <strong> 1, </strong> чтобы запустить Adobe Reader X в защищенном режиме на этапе запуска.</p></td>
</tr>
</tbody>
</table>

 

**Примечание**  На компьютере под управлением 64-разрядной операционной системы Создайте значение реестра в разделе HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.

 

Для каждого OSD-файла в пакете Adobe Reader X добавьте в &lt; элемент POLICIES следующие элементы &gt; :

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**Новый параметр командной строки Sequencer**

Когда вы создаете ускоритель пакетов (PA) через графический интерфейс секвенсора, вы можете выбрать файл RTF или TXT, который содержит инструкции по упаковке и развертыванию для администраторов, которые будут применять ускоритель пакетов. Теперь эта функция доступна с помощью CLI Sequencer.

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

Укажите путь к файлу RTF или TXT, который содержит инструкции по упаковке и развертыванию при создании ускорителя пакетов.

**Сообщения об ошибках приложений Microsoft больше не нужно устанавливать**

При установке клиента App-V 4.6 SP2 с помощью setup.msi вам больше не нужно устанавливать отчеты об ошибках приложений Microsoft (dw20shared.msi). Приложение App-V 4.6 SP2 теперь использует отчеты об ошибках Microsoft. Дополнительные сведения можно найти [в разделе Установка клиента App-V с помощью Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).

**Отзывы и наборы исправлений пользователей**

Приложение App-V 4.6 SP2 содержит свертку исправлений, устраняющих проблемы, обнаруженные с момента выпуска App-V 4,6 с пакетом обновления 1 (SP1). В состав пакета обновления 2 (SP2) для App-V 4.6 установлены последние исправления до и включая Microsoft Application Virtualization 4,6 с исправлением 6 (SP1).

## В этом разделе


<a href="" id="app-v-4-6-sp2-release-notes"></a>[Заметки о выпуске App-V 4.6 с пакетом обновления 2 (SP2)](https://go.microsoft.com/fwlink/?LinkId=267600)  
Предоставляет актуальные сведения об известных проблемах, возникающих при использовании App-V 4.6 SP2.

 

 





