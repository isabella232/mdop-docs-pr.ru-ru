---
title: Установка программы Sequencer
description: Установка программы Sequencer
author: dansimp
ms.assetid: a122caf0-f408-458c-b119-dc84123c1d58
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8542abfecd7f1d543228ab1a86a59b9ee918947
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813952"
---
# Установка программы Sequencer


Чтобы установить Microsoft Application Virtualization (App-V) 5,0 Sequencer, выполните указанные ниже действия. На компьютере, на котором будет выполняться секвенсор, не должна выполняться какая-либо версия клиента App-V 5,0.

Обновление предыдущей установки секвенсора App-V не поддерживается.

**Важно!**  Полный список требований к секвенсору см. разделы секвенсора, необходимые для [App-v 5,0](app-v-50-prerequisites.md) и [Поддерживаемые конфигурации app-v 5,0](app-v-50-supported-configurations.md).

 

Для установки секвенсора App-V 5,0 также можно использовать командную строку. В следующем списке приведены сведения о параметрах для установки секвенсора с помощью командной строки и **appv\_sequencer\_setup.exe**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Команда</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/INSTALLDIR</p></td>
<td align="left"><p>Указывает каталог установки.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CEIPOPTIN</p></td>
<td align="left"><p>Включает участие в программе улучшения качества программного обеспечения Майкрософт.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Log</p></td>
<td align="left"><p>Указывает место сохранения журнала установки: <strong> % temp% </strong> . Например, <strong> C:\ Журналы — log. log </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>/q</p></td>
<td align="left"><p>Указывает на автоматическую или автоматическую установку.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Uninstall</p></td>
<td align="left"><p>Задает удаление секвенсора.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/ACCEPTEULA</p></td>
<td align="left"><p>Принимает лицензионное соглашение. Это необходимо для автоматической установки. Пример использования: <strong> /ACCEPTEULA </strong> или <strong> /ACCEPTEULA = 1 </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LAYOUT</p></td>
<td align="left"><p>Задает связанное действие макета. Кроме того, приложение App-V 5,0 будет извлечено из файла установщика Windows (MSI) и файлов сценариев в папку. Значение не ожидается.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LAYOUTDIR</p></td>
<td align="left"><p>Указывает каталог макета. Требуется строковое значение. Пример использования: <strong> /LAYOUTDIR = "клиент виртуализации C:\Application" </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/? Или/h или/Help</p></td>
<td align="left"><p>Отображает связанную справку.</p></td>
</tr>
</tbody>
</table>

 

**Установка секвенсора App-V 5,0**

1.  Скопируйте файлы установки программы Sequencer App-V 5,0 на компьютер, на котором он будет установлен. Дважды щелкните **appv\_sequencer\_setup.exe** и нажмите кнопку **установить**.

2.  На странице **условия лицензии на программное обеспечение** ознакомьтесь с условиями лицензионного соглашения. Чтобы согласиться с условиями лицензионного соглашения, выберите **я принимаю условия лицензионного соглашения.** Нажмите кнопку **Далее**.

3.  На странице **Использование центра обновления Майкрософт, чтобы обеспечить безопасность и актуальность** данных на компьютере, чтобы включить обновления Microsoft, выберите **использовать Microsoft Update при проверке обновлений (рекомендуется).** Чтобы отключить обновления Майкрософт, выберите **я не хочу использовать Microsoft Update**. Нажмите кнопку **Далее**.

4.  На странице **программы улучшения качества** программного обеспечения, чтобы принять участие в программе, выберите **присоединиться к программе улучшения качества**программного обеспечения. Это позволит собирать сведения о том, как вы используете App-V 5,0. Если вы не хотите принимать участие в программе, выберите в **настоящее время присоединиться к программе не нужно**. Нажмите кнопку **Установить**.

5.  Чтобы открыть секвенсор, нажмите кнопку **Пуск** , а затем выберите **Microsoft Application Virtualization Sequencer**.

**Устранение неполадок при установке App-V 5,0 Sequencer**

-   Для получения дополнительных сведений об установке программы Sequencer вы можете просмотреть журнал ошибок в папке **% TEMP%** . Чтобы просмотреть файлы журнала, нажмите кнопку **Пуск**, введите **% TEMP%**, а затем найдите **Журнал appv\_**.

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Планирование развертывания App-V](planning-to-deploy-app-v.md)

 

 





