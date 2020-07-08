---
title: Развертывание Microsoft Office 2010 с помощью App-V
description: Развертывание Microsoft Office 2010 с помощью App-V
author: dansimp
ms.assetid: ae0b0459-c0d6-4946-b62d-ff153f52d1fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90454373e9a1c894eba8cbf1b8642656b986bc94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814624"
---
# Развертывание Microsoft Office 2010 с помощью App-V


Пакеты Office 2010 для Microsoft Application Virtualization (App-V) 5,1 можно создать с помощью одного из следующих способов:

-   Секвенсор Application Virtualization (App-V)

-   Ускоритель пакетов для Application Virtualization (App-V)

## Поддержка App-V для Office 2010


В следующей таблице показаны версии App-V, методы создания пакетов Office, поддерживаемые лицензированные и поддерживаемые развертывания для Office 2010.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Поддерживаемый элемент</th>
<th align="left">Уровень поддержки</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Поддерживаемые версии App-V</p></td>
<td align="left"><ul>
<li><p>4,6</p></li>
<li><p>5.0</p></li>
<li><p>5,1</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Создание пакета</p></td>
<td align="left"><ul>
<li><p>Последовательность</p></li>
<li><p>Ускоритель пакетов</p></li>
<li><p>Комплект средств для развертывания Office</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Поддерживаемое лицензирование</p></td>
<td align="left"><p>Корпоративное лицензирование</p></td>
</tr>
<tr class="even">
<td align="left"><p>Поддерживаемые развертывания</p></td>
<td align="left"><ul>
<li><p>Desktop</p></li>
<li><p>Персональный VDI</p></li>
<li><p>СЛУЖБ</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Создание Office 2010 App-V 5,1 с помощью секвенсора


Виртуализация Office 2010 — это один из основных методов создания пакета Office 2010 на App-V 5,1. Корпорация Майкрософт предоставила подробный рецепт в статье базы знаний. Чтобы создать пакет Office 2010 для App-V 5,1, ознакомьтесь с подробными инструкциями по следующей ссылке:

[Последовательность последовательностей Microsoft Office 2010 в Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## Создание пакетов Office 2010 App-V 5,1 с помощью ускорителей пакетов


Пакеты Office 2010 App-V 5,1 можно создавать с помощью ускорителей пакетов. Корпорация Майкрософт предоставила акселераторы пакетов для создания Office 2010 в Windows 10, Windows 8 и Windows 7. Чтобы создать пакеты Office 2010 в App-V с помощью ускорителей пакетов, просмотрите следующие страницы, чтобы получить доступ к соответствующему ускорительу пакетов:

-   [Ускоритель пакетов для Office профессиональный плюс 2010 — Windows 8 (App-V 5,0)](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [Ускоритель пакетов для Office профессиональный плюс 2010 – Windows 7 (App-V 5,0)](https://go.microsoft.com/fwlink/p/?LinkId=330678)

Подробные инструкции по созданию пакетов виртуальных приложений с помощью ускорителей пакетов App-V можно найти в разделе [Создание виртуального пакета приложения с помощью ускорителя пакетов App-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).

## Развертывание пакета Microsoft Office для App-V 5,1


Пакеты Office 2010 можно развертывать с помощью любого из указанных ниже методов развертывания App-V.

-   System Center Configuration Manager

-   Сервер App-V

-   Самостоятельная работа с помощью команд PowerShell

## Управление пакетами и настройка в Office App-V


Пакеты Office 2010 могут управляться так же, как и любые другие пакеты App-V 5,1 с помощью стандартных механизмов управления пакетами. Специальные инструкции не требуются, например, для добавления, публикации, отмены публикации и удаления пакетов Office.

## Интеграция Microsoft Office с Windows


В таблице ниже приведен полный список поддерживаемых точек интеграции для Office 2010.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Точка расширения</th>
<th align="left">Описание</th>
<th align="left">Office 2010</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Плагин присоединения к собранию Lync для Firefox и Chrome</p></td>
<td align="left"><p>Пользователь может присоединиться к собраниям Lync из Firefox и Chrome</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Отправлено в драйвер печати OneNote</p></td>
<td align="left"><p>Пользователь может печатать в OneNote</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Связанные заметки OneNote</p></td>
<td align="left"><p>Связанные заметки OneNote</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Надстройка "отправить в OneNote" в Internet Explorer</p></td>
<td align="left"><p>Пользователь может отправлять сообщения в OneNote из браузера Internet Explorer</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Исключение брандмауэра для Lync и Outlook</p></td>
<td align="left"><p>Исключение брандмауэра для Lync и Outlook</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Клиент MAPI</p></td>
<td align="left"><p>Встроенные приложения и надстройки могут взаимодействовать с виртуальным приложением Outlook через MAPI</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Подключаемый модуль SharePoint для Firefox</p></td>
<td align="left"><p>Пользователь может использовать возможности SharePoint в Firefox</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Приложение панели управления "почта"</p></td>
<td align="left"><p>Пользователь получает панель управления "почта" в Outlook</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Основные сборки взаимодействия</p></td>
<td align="left"><p>Поддержка управляемых надстроек</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Обработчик кэша документов Office</p></td>
<td align="left"><p>Разрешение кэша документов для приложений Office</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Обработчик поиска протоколов Outlook</p></td>
<td align="left"><p>Пользователь может выполнять поиск в Outlook</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="even">
<td align="left"><p>Элементы управления ActiveX:</p></td>
<td align="left"><p>Дополнительные сведения об элементах ActiveX можно найти в <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> справочнике API элементов ActiveX </a> .</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Groove. SiteClient</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect.PersonalSite</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. openDocument</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. OpenXMLDocuments</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ClipboardCtl</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   WinProj. активатор</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Name. NameCtrl</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   STSUPld.CopyCtl</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx.JoinManager</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Вспомогательное приложение браузера OneDrive Pro</p></td>
<td align="left"><p>Элемент управления ActiveX]</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Наложения значков OneDrive Pro</p></td>
<td align="left"><p>Перекрытие значков оболочки в проводнике Windows при просмотре папок в папках OneDrive Pro</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## Дополнительные ресурсы


**Дополнительные ресурсы в пакетах Office 2013 App-V**

[Поддерживаемые сценарии для развертывания Microsoft Office в последовательном пакете App-V](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**Пакеты приложения Office 2010 App-V**

[Комплект виртуализации Microsoft Office 2010 для Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[Известные проблемы, возникающие при создании или использовании пакета Office 2010 для App-V 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[Последовательность последовательностей Microsoft Office 2010 в Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**Группы подключения**

[Развертывание групп подключений в Microsoft App-V V5](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[Управление связывающими группами](managing-connection-groups51.md)

**Динамическая настройка**

[Сведения о динамической конфигурации App-V 5.1](about-app-v-51-dynamic-configuration.md)






 

 





