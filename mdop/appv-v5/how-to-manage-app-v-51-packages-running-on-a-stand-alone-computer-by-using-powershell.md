---
title: Управление пакетами App-V 5.1, работающими на автономном компьютере, с помощью PowerShell
description: Управление пакетами App-V 5.1, работающими на автономном компьютере, с помощью PowerShell
author: dansimp
ms.assetid: c3fd06f6-102f-43d1-a577-d5ced6ac537d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b454014da4e5f349af913d3fea8ea3837598a039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813917"
---
# Управление пакетами App-V 5.1, работающими на автономном компьютере, с помощью PowerShell


В следующих разделах объясняется, как выполнять различные задачи управления на отдельном клиентском компьютере с помощью PowerShell.

-   [Возврат списка пакетов](#bkmk-return-pkgs-standalone-posh)

-   [Добавление пакета](#bkmk-add-pkgs-standalone-posh)

-   [Публикация пакета](#bkmk-pub-pkg-standalone-posh)

-   [Публикация пакета для определенного пользователя](#bkmk-pub-pkg-a-user-standalone-posh)

-   [Добавление и Публикация пакета](#bkmk-add-pub-pkg-standalone-posh)

-   [Отмена публикации существующего пакета](#bkmk-unpub-pkg-standalone-posh)

-   [Отмена публикации пакета для определенного пользователя](#bkmk-unpub-pkg-specfc-use)

-   [Удаление существующего пакета](#bkmk-remove-pkg-standalone-posh)

-   [Разрешение администраторам публиковать и отменять публикацию пакетов](#bkmk-admins-pub-pkgs)

-   [Основные сведения о ожидающих пакетах (UserPending и GlobalPending)](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a>Возврат списка пакетов


Используйте следующие сведения, чтобы вернуть список пакетов, которые имеют право определенного пользователя:

**Командлет**: Get-AppvClientPackage

**Параметры**:-Name-Version-PackageID-VersionID

**Пример**: Get-AppvClientPackage-Name "ContosoApplication"-версия 2

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a>Добавление пакета


Чтобы добавить пакет на компьютер, воспользуйтесь приведенными ниже сведениями.

**Важно!**  В этом примере добавляется только пакет. Он не публикует пакет для пользователя или компьютера.

 

**Командлет**: Add-AppvClientPackage

**Пример**: $contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a>Публикация пакета


Используйте следующие сведения для публикации пакета, который был добавлен к определенному пользователю или глобально любому пользователю на компьютере.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Метод публикации</th>
<th align="left">Командлет и пример</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Публикация для пользователя</p></td>
<td align="left"><p><strong>Командлет </strong> : Publish-AppvClientPackage</p>
<p><strong>Пример </strong> : Publish-AppvClientPackage "ContosoApplication"</p></td>
</tr>
<tr class="even">
<td align="left"><p>Глобальная публикация</p></td>
<td align="left"><p><strong>Командлет </strong> : Publish-AppvClientPackage</p>
<p><strong>Пример </strong> : Publish-AppvClientPackage "ContosoApplication"-Global</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a>Публикация пакета для определенного пользователя


**Примечание**  Чтобы использовать этот параметр, необходимо воспользоваться пакетом обновления 2 (SP2) для App-V 5,0 или более поздней версии.

 

Администратор может опубликовать пакет для определенного пользователя, указав дополнительный параметр **–** кодом в командлете **Publish-AppvClientPackage** , где **-** то есть идентификатора безопасности (SID) конечного пользователя.

Чтобы использовать этот параметр, выполните указанные ниже действия.

-   Вы можете запустить этот командлет из сеанса пользователя или администратора.

-   Для использования параметра необходимо войти в систему с помощью учетных данных администратора.

-   Конечный пользователь должен войти в систему.

-   Необходимо указать идентификатор безопасности (SID) конечного пользователя.

**Командлет**: Publish-AppvClientPackage

**Пример**: Publish-AppvClientPackage "ContosoApplication"-от S до 1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a>Добавление и Публикация пакета


Используйте следующие сведения, чтобы добавить пакет на компьютер и опубликовать его для пользователя.

**Командлет**: Add-AppvClientPackage

**Пример**: Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV | Publish-AppvClientPackage

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a>Отмена публикации существующего пакета


Используйте указанные ниже сведения, чтобы отменить публикацию пакета, которому был предоставлен доступ пользователю, но не удалять пакет с компьютера.

**Командлет**: unpublishing-AppvClientPackage

**Пример**: unpublishing-AppvClientPackage "ContosoApplication"

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a>Отмена публикации пакета для определенного пользователя


**Примечание**  Чтобы использовать этот параметр, необходимо воспользоваться пакетом обновления 2 (SP2) для App-V 5,0 или более поздней версии.

 

Администратор может отменить публикацию пакета для определенного пользователя с помощью необязательного параметра **–** кодом в командлете **UNPUBLISH-AppvClientPackage** , где-то есть **—** идентификатора безопасности (SID) конечного пользователя.

Чтобы использовать этот параметр, выполните указанные ниже действия.

-   Вы можете запустить этот командлет из сеанса пользователя или администратора.

-   Для использования параметра необходимо войти в систему с помощью учетных данных администратора.

-   Конечный пользователь должен войти в систему.

-   Необходимо указать идентификатор безопасности (SID) конечного пользователя.

**Командлет**: unpublishing-AppvClientPackage

**Пример**: unpublishing-AppvClientPackage "ContosoApplication"-от S до 1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a>Удаление существующего пакета


Используйте следующие сведения для удаления пакета с компьютера.

**Командлет**: Remove-AppvClientPackage

**Пример**: Remove-AppvClientPackage "ContosoApplication"

**Примечание**  Командлетам App-V назначены переменные для более понятной версии, а не только для ясности, но и для более ранних. назначение не является обязательным. Большинство командлетов можно сочетать так, как показано в этой панели, [чтобы добавить и опубликовать пакет](#bkmk-add-pub-pkg-standalone-posh). Подробные сведения можно найти в подробном руководстве по Windows [App-V 5,0 для клиента PowerShell](https://go.microsoft.com/fwlink/?LinkId=324466).

 

## <a href="" id="bkmk-admins-pub-pkgs"></a>Разрешение администраторам публиковать и отменять публикацию пакетов


**Примечание** 
 **Эта функция поддерживается начиная с версии App-V 5,0 SP3.**

 

Используйте следующий командлет и параметр для разрешения публикации и отмены публикации пакетов только для администраторов (не конечных пользователей).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Командлет</strong></p></td>
<td align="left"><p>Set-AppvClientConfiguration</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Параметр</strong></p></td>
<td align="left"><p>-RequirePublishAsAdmin</p>
<p>Значения параметров:</p>
<ul>
<li><p>0 – ложь</p></li>
<li><p>1 — истина</p></li>
</ul>
<p><strong>Пример: </strong> Set-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

Чтобы использовать консоль управления App-V для настройки этой конфигурации, ознакомьтесь со [сведениями о том, как опубликовать пакет с помощью консоли управления](how-to-publish-a-package-by-using-the-management-console-51.md).

## <a href="" id="bkmk-understd-pend-pkgs"></a>Основные сведения о ожидающих пакетах (UserPending и GlobalPending)


**Начиная с версии App-V 5,0 с пакетом обновления 2 (SP2)**: Если вы запускаете командлет PowerShell, который влияет на пакет, который в данный момент используется, задача, которую вы пытаетесь выполнить, помещается в состояние ожидания. Например, если вы пытаетесь опубликовать пакет, если используется приложение из этого пакета, а затем выполнить **Get-AppvClientPackage**, в выходных данных командлета появится состояние ожидания, как показано ниже.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Элемент вывода командлета</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>UserPending</p></td>
<td align="left"><p>Указывает, имеет ли список в списке ожидающие задачи, которые применяются к пользователю:</p>
<ul>
<li><p>True</p></li>
<li><p>False</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalPending</p></td>
<td align="left"><p>Указывает, имеет ли указанный пакет отложенную задачу, которая будет применена к компьютеру глобально.</p>
<ul>
<li><p>True</p></li>
<li><p>False</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Задача, ожидающая обработки, будет выполнена позже в соответствии с приведенными ниже правилами.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Тип задачи</th>
<th align="left">Применимое правило</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Пользовательская задача, например Публикация пакета для пользователя</p></td>
<td align="left"><p>Задача будет выполнена после того, как пользователь войдет в систему, а затем снова войдите в нее.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Глобально на основе задач, например включение глобальной группы подключения</p></td>
<td align="left"><p>Задача, ожидающая выполнения, будет выполнена после отключения компьютера и повторного запуска.</p></td>
</tr>
</tbody>
</table>

 

Дополнительные сведения о незавершенных задачах можно найти в разделе [о приложении App-V 5,0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).

**У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.1](operations-for-app-v-51.md)

[Администрирование App-V 5.1 с помощью PowerShell](administering-app-v-51-by-using-powershell.md)

 

 





