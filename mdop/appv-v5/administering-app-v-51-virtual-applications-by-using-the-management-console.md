---
title: Администрирование виртуальных приложений App-V 5.1 с помощью консоли управления
description: Администрирование виртуальных приложений App-V 5.1 с помощью консоли управления
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814864"
---
# Администрирование виртуальных приложений App-V 5.1 с помощью консоли управления


Используйте сервер управления Microsoft Application Virtualization (App-V) 5,1 для управления пакетами, группами подключений и доступом к пакетам в среде. Сервер публикует значки, ярлыки и сопоставления типов файлов на авторизованных компьютерах, на которых запущен клиент App-V 5,1. Как правило, один или несколько серверов управления совместно имеют общее хранилище данных для конфигурации и сведений о пакете.

Сервер управления использует группы доменных служб Active Directory (AD DS) для управления авторизацией пользователей и установленный SQL Server для управления базой данных и хранилищем данных.

Так как серверы управления потоками приложений для конечных пользователей по запросу, эти серверы лучше всего подходят для конфигураций системы, которые обладают надежной и высокоскоростной ЛВС. Сервер управления состоит из следующих компонентов:

-   Сервер управления — используйте сервер управления для управления пакетами и группами подключений.

-   Сервер публикации — используйте сервер публикации для развертывания пакетов на компьютерах, на которых запущен клиент App-V 5,1.

-   База данных управления — используйте базу данных управления для управления доступом к пакету и публикации синхронизации сервера с сервером управления.

## Задачи консоли управления


Ниже перечислены наиболее распространенные задачи, которые можно выполнять с помощью консоли управления App-V 5,1.

-   [Подключение к консоли управления](how-to-connect-to-the-management-console-51.md)

-   [Добавление или обновление пакетов с помощью консоли управления](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [Настройка доступа к пакетам с помощью консоли управления](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [Публикация пакета с помощью консоли управления](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [Удаление пакета в консоли управления](how-to-delete-a-package-in-the-management-console-51.md)

-   [Добавление или удаление администратора с помощью консоли управления](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [Регистрация и отмена регистрации сервера публикации с помощью консоли управления](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [Создание пользовательского файла конфигурации с помощью консоли управления App-V 5.1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [Передача прав доступа и конфигураций в другую версию пакета с помощью консоли управления](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [Настройка расширений виртуальных приложений для определенной группы AD с помощью консоли управления](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [Просмотр и настройка приложений и расширений виртуальных приложений по умолчанию с помощью консоли управления](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

Основные элементы консоли управления App-V 5,1:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Вкладка консоли управления</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Вкладка "пакеты"</p></td>
<td align="left"><p>С помощью <strong> </strong> вкладки "пакеты" можно добавлять и обновлять пакеты.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Вкладка "группы подключения"</p></td>
<td align="left"><p><strong>Вкладка "группы подключения </strong> " используется для управления группами подключений.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Вкладка "серверы"</p></td>
<td align="left"><p>С помощью <strong> </strong> вкладки серверы зарегистрируйте новый сервер.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Вкладка "Администраторы"</p></td>
<td align="left"><p>С помощью <strong> </strong> вкладки администраторы можно зарегистрировать, добавить или удалить администраторов в среде App-V 5,1.</p></td>
</tr>
</tbody>
</table>

 

**Важно!**  На веб-сайте, на котором открывается консоль управления Веба, должен быть включен JavaScript.

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a>Другие ресурсы для развертывания приложения-V 5,1


-   [Руководство администратора Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)

-   [Операции, связанные с администрированием и использованием App-V 5.1](operations-for-app-v-51.md)

 

 





