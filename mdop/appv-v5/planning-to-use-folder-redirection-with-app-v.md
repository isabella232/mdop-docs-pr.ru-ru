---
title: Планирование использования перенаправления папок с App-V
description: Планирование использования перенаправления папок с App-V
author: dansimp
ms.assetid: 2a4deeed-fdc0-465c-b88a-3a2fbbf27436
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b25b3531faa495275bf4e478389f44790d8eed9a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813381"
---
# Планирование использования перенаправления папок с App-V


App-V 5,0 SP2 поддерживает использование перенаправления папок — функции, которая позволяет пользователям и администраторам перенаправлять путь к папке в новое расположение.

Этот раздел включает в себя следующие разделы:

-   [Требования для использования перенаправления папок](#bkmk-folder-redir-reqs)

-   [Настройка перенаправления папок для использования с App-V](#bkmk-folder-redir-cfg)

-   [Как работает перенаправление папок в App-V](#bkmk-folder-redir-works)

-   [Общие сведения о перенаправлении папок](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a>Требования и неподдерживаемые сценарии использования перенаправления папок


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Требования</p></td>
<td align="left"><p>Чтобы использовать перенаправление папок% AppData%, необходимо выполнить указанные ниже действия.</p>
<ul>
<li><p>У вас есть пакет App-V с папкой виртуальной файловой системы AppData (VFS).</p></li>
<li><p>Включить перенаправление папок и перенаправить папки пользователей в общую папку (обычно это сетевая папка).</p></li>
<li><p>Перемещайте оба или ни один из указанных ниже вариантов.</p>
<ul>
<li><p>Файлы в разделе%appdata%\Microsoft\AppV\Client\Catalog</p></li>
<li><p>Параметры реестра в разделе HKEY_CURRENT_USER \Software\Microsoft\AppV\Client\Packages</p>
<p>Более подробную информацию можно найти в разделе <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> Публикация приложений и взаимодействие с клиентами </a> .</p></li>
</ul></li>
<li><p>Убедитесь, что следующие папки доступны каждому пользователю, который входит в систему на компьютере, на котором запущен клиент App-V 5,0 SP2 или более поздней версии.</p>
<ul>
<li><p>% AppData% настроено на нужное сетевое расположение (с <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> поддержкой автономных файлов или без нее </a> ).</p></li>
<li><p>% LocalAppData% настроен на нужную локальную папку.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Неподдерживаемые сценарии</p></td>
<td align="left"><ul>
<li><p>Настройка% LocalAppData% в качестве сетевого диска.</p></li>
<li><p>Перенаправление меню "Пуск" в одну папку для нескольких пользователей.</p></li>
<li><p>Если перемещаемая папка AppData (% AppData%) перенаправляется на недоступную сетевую ошибку, приложения App-V не будут запускаться следующим образом:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Версия App-V</th>
<th align="left">Описание сценария</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>В App-V 5,0 с помощью App-V 5,0 SP2 и исправлений</p></td>
<td align="left"><p>Этот сбой будет происходить независимо от того, включены ли автономные файлы.</p></td>
</tr>
<tr class="even">
<td align="left"><p>В App-V 5,0 с пакетом обновления 3 (SP3)</p></td>
<td align="left"><p>Если для автономных файлов отключена доступная сетевая доступная, приложение App-V запустится успешно.</p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a>Настройка перенаправления папок для использования с App-V


Перенаправление папок можно применять к различным папкам, таким как "Рабочий стол", "Мои документы", "Мои рисунки" и т. д. Тем не менее, единственная папка, влияющая на использование приложений App-V, — это папка для перемещаемой AppData пользователя (% AppData%). Перенаправление папок можно применить ко всем другим поддерживаемым папкам, не влияя на App-V.

## <a href="" id="bkmk-folder-redir-works"></a>Как работает перенаправление папок в App-V


В приведенной ниже таблице показано, как работает перенаправление папок, когда пользователь% AppData% перенаправляется в сеть и после того, как вы удовлетворены требованиями, описанными выше в этой статье.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Состояние виртуальной среды</th>
<th align="left">Выполняемое действие</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>При запуске виртуальной среды</p></td>
<td align="left"><p>Папка AppData виртуальной файловой системы (VFS) сопоставлена с локальной папкой AppData (% LocalAppData%) вместо ссылки на перемещаемую папку AppData пользователя (% AppData%).</p>
<ul>
<li><p>LocalAppData включает локальный кэш папки с перемещаемой AppData пользователя для используемого пакета. Локальный кэш находится в разделе:</p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p>Последние данные из папки перемещаемой оснастки пользователя копируются в и заменяют данные в локальном кэше.</p></li>
<li><p>При запуске виртуальной среды данные сохраняются в локальном кэше. Данные выдаются только из% LocalAppData% и не перемещаются или синхронизируются с помощью% AppData%, пока конечный пользователь не завершит работу компьютера.</p></li>
<li><p>Элементы в папку AppData выполняются с помощью контекста пользователя, а не контекста системы.</p></li>
</ul>
<div class="alert">
<strong>Примечание.</strong><br/><p>Иногда перенаправление папки клиента App-V не может переносить файлы из% AppData% в% LocalAppData%. Ознакомьтесь <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)"> с заметками о выпуске для App-V 5,0 SP2 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>При завершении работы виртуальной среды</p></td>
<td align="left"><p>Локальные кэшированные данные в AppData (роуминге) заархивированы и скопированы в папку "Real" перемещаемой папки AppData в% AppData%. Метка времени, указывающая на последнюю известную отправку, одновременно сохраняется как раздел реестра в разделе:</p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p>Для обеспечения избыточности приложение App-V 5,0 сохраняет три последние копии сжатых данных в разделе% AppData%.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a>Общие сведения о перенаправлении папок


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Описание</p></td>
<td align="left"><p>Позволяет конечным пользователям работать с файлами, которые были перенаправлены в другую папку, как если бы они находились на локальном диске.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Описание</p></td>
<td align="left"><p>Перенаправление папок позволяет пользователям и администраторам перенаправлять путь к папке в сетевое расположение. Документы в папке доступны для пользователя на любом компьютере в сети.</p>
<ul>
<li><p>Перенаправление папок позволяет пользователям и администраторам перенаправлять путь к папке в сетевое расположение. Документы в папке доступны для пользователя на любом компьютере в сети.</p></li>
<li><p>Новое расположение может представлять собой папку на локальном компьютере или в общей сетевой папке.</p></li>
<li><p>Перенаправление папок немедленно обновляет файлы, а перемещаемые данные обычно синхронизируются, когда пользователь входит в систему или выходит из нее.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Пример использования</p></td>
<td align="left"><p>Вы можете перенаправить папку "документы", которая обычно хранится на локальном жестком диске компьютера&#39;s, в сетевое расположение. Пользователь может получить доступ к документам в папке с любого компьютера в сети.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Дополнительные ресурсы</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)">Общие сведения о перенаправлении папок</a></p></td>
</tr>
</tbody>
</table>
















