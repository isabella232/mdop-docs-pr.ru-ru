---
title: Создание связывающей группы с опубликованными пользователями и глобально опубликованными пакетами
description: Создание связывающей группы с опубликованными пользователями и глобально опубликованными пакетами
author: dansimp
ms.assetid: 851b8742-0283-4aa6-b3a3-f7f6289824c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 230e687360920c05a214624750eba54dc84b5731
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814365"
---
# Создание связывающей группы с опубликованными пользователями и глобально опубликованными пакетами


Вы можете создавать группы подключений пользователей, которые содержат как опубликованные пользователями, так и глобально опубликованные пакеты, используя один из указанных ниже способов.

-   [Использование командлетов PowerShell для создания групп подключений пользователей](#bkmk-posh-userentitled-cg)

-   [Использование сервера App-V для создания групп подключений пользователей](#bkmk-appvserver-userentitled-cg)

**Что нужно знать перед началом работы:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Неподдерживаемые сценарии и потенциальные проблемы</th>
<th align="left">Результат</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Вы не можете включать опубликованные пользователем пакеты в глобальных группах подключений.</p></td>
<td align="left"><p>Не удается выполнить группу подключения.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Если вы публикуете пакет глобально и затем создаете пользовательскую группу подключения, в которой вы сделали этот пакет необязательными, вы по-прежнему можете выполнить команду <strong> UNPUBLISH-AppvClientPackage &lt; &gt; -Global, </strong> чтобы отменить публикацию пакета, даже если этот пакет используется в другой группе подключения.</p></td>
<td align="left"><p>Если какие бы то ни было другие группы соединения использовали этот пакет, пакет не будет работать в этих группах подключения.</p>
<p>Чтобы избежать непреднамеренной отмены публикации необязательного пакета, который используется в другой группе подключения, мы рекомендуем отслеживать группы, в которых вы использовали необязательный пакет.</p></td>
</tr>
</tbody>
</table>

<a href="" id="bkmk-posh-userentitled-cg"></a>**Использование командлетов PowerShell для создания групп подключений пользователей**

1.  Добавьте и опубликуйте пакеты с помощью следующих команд:

    **Add-AppvClientPackage Package1 \ _AppV \ _file \ _Path**

    **Add-AppvClientPackage Package2 \ _AppV \ _file \ _Path**

    **Publish-AppvClientPackage-PackageId Package1 \ _ID-VersionId Package1 \ _Version ID-Global**

    **Publish-AppvClientPackage-PackageId Package2 \ _ID-VersionIdPackage2 \ _ID**

2.  Создайте XML-файл группы подключения. Дополнительные сведения можно найти [в разделе о файле группы подключения](about-the-connection-group-file51.md).

3.  Добавьте и опубликуйте группу подключений с помощью следующих команд:

    **Подключение Add-AppvClientConnectionGroup _Group \ _XML \ _file \ _Path**

    **Enable-AppvClientConnectionGroup-GroupId CG \ _Group \ _ID-VersionId CG \ _Version \ _ID**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**Создание групп подключений пользователей с помощью App-V Server**

1.  Откройте консоль управления App-V 5,1.

2.  Следуйте инструкциям по [публикации пакета с помощью консоли управления](how-to-publish-a-package-by-using-the-management-console-51.md) , чтобы опубликовать пакеты глобально и с учетной записью пользователя.

3.  Следуйте инструкциям, [чтобы](how-to-create-a-connection-group51.md) создать группу подключения для создания группы подключения и добавить опубликованные пользователем и глобально опубликованные пакеты.

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Управление связывающими группами](managing-connection-groups51.md)

[Использование дополнительных пакетов в группах соединений](how-to-use-optional-packages-in-connection-groups51.md)

 

 





