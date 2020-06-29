---
title: Администрирование виртуальных приложений App-V 5.0 с помощью консоли управления
description: Администрирование виртуальных приложений App-V 5.0 с помощью консоли управления
author: dansimp
ms.assetid: e9280dbd-782b-493a-b495-daab25247795
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: 7a71f7c0fd82f8ef9d1efd5b978591b6838a648a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814869"
---
# Администрирование виртуальных приложений App-V 5.0 с помощью консоли управления


Используйте сервер управления Microsoft Application Virtualization (App-V) 5,0 для управления пакетами, группами подключений и доступом к пакетам в среде. Сервер публикует значки, ярлыки и сопоставления типов файлов на авторизованных компьютерах, на которых запущен клиент App-V 5,0. Как правило, один или несколько серверов управления совместно имеют общее хранилище данных для конфигурации и сведений о пакете.

Сервер управления использует группы доменных служб Active Directory (AD DS) для управления авторизацией пользователей и установленный SQL Server для управления базой данных и хранилищем данных.

Так как серверы управления потоками приложений для конечных пользователей по запросу, эти серверы лучше всего подходят для конфигураций системы, которые обладают надежной и высокоскоростной ЛВС. Сервер управления состоит из следующих компонентов:

-   Сервер управления — используйте сервер управления для управления пакетами и группами подключений.

-   Сервер публикации — используйте сервер публикации для развертывания пакетов на компьютерах, на которых запущен клиент App-V 5,0.

-   База данных управления — используйте базу данных управления для управления доступом к пакету и публикации синхронизации сервера с сервером управления.

## Задачи консоли управления


Ниже перечислены наиболее распространенные задачи, которые можно выполнять с помощью консоли управления App-V 5,0.

-   [Подключение к консоли управления](how-to-connect-to-the-management-console-beta.md)

-   [Добавление или обновление пакетов с помощью консоли управления](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)

-   [Настройка доступа к пакетам с помощью консоли управления](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

-   [Публикация пакета с помощью консоли управления](how-to-publish-a-package-by-using-the-management-console-50.md)

-   [Удаление пакета в консоли управления](how-to-delete-a-package-in-the-management-console-beta.md)

-   [Добавление или удаление администратора с помощью консоли управления](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)

-   [Регистрация и отмена регистрации сервера публикации с помощью консоли управления](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console.md)

-   [Создание пользовательского файла конфигурации с помощью консоли управления App-V 5.0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)

-   [Передача прав доступа и конфигураций в другую версию пакета с помощью консоли управления](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console.md)

-   [Настройка расширений виртуальных приложений для определенной группы AD с помощью консоли управления](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console.md)

-   [Настройка приложений и расширений виртуальных приложений по умолчанию в консоли управления](configure-applications-and-default-virtual-application-extensions-in-management-console.md)

Основные элементы консоли управления App-V 5,0:

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
<td align="left"><p>Обзор</p></td>
<td align="left"><p></p>
<ul>
<li><p><strong>Секвенсор App-V </strong> - Выберите этот параметр, чтобы просмотреть общие сведения об использовании секвенсора App-v 5,0.</p></li>
<li><p><strong>Библиотека пакетов приложения </strong> : Выберите этот параметр, чтобы открыть <strong> страницу "пакеты" на </strong> консоли управления. Эта страница служит для просмотра пакетов, которые были добавлены на сервер. Вы также можете управлять группами подключений, а также добавлять и обновлять пакеты.</p></li>
<li><p><strong>СЕРВЕРЫ </strong> : Выберите этот параметр, чтобы открыть <strong> страницу "серверы" </strong> консоли управления. На этой странице можно просмотреть список серверов, зарегистрированных в вашей инфраструктуре App-V 5,0.</p></li>
<li><p><strong>КЛИЕНТЫ </strong> : Выберите этот параметр, чтобы просмотреть общие сведения о клиентах App-V 5,0.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Вкладка "пакеты"</p></td>
<td align="left"><p>С помощью <strong> </strong> вкладки "пакеты" можно добавлять и обновлять пакеты. Вы также можете управлять группами подключений, щелкая <strong> группы подключения </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Вкладка "серверы"</p></td>
<td align="left"><p>С помощью <strong> </strong> вкладки серверы зарегистрируйте новый сервер.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Вкладка "Администраторы"</p></td>
<td align="left"><p>С помощью <strong> </strong> вкладки администраторы можно зарегистрировать, добавить или удалить администраторов в среде App-V 5,0.</p></td>
</tr>
</tbody>
</table>

 






## <a href="" id="other-resources-for-this-app-v-5-0-deployment-"></a>Другие ресурсы для развертывания приложения-V 5,0


-   [Руководство администратора Microsoft Application Virtualization 5,0](microsoft-application-virtualization-50-administrators-guide.md)

-   [Операции, связанные с администрированием и использованием App-V 5.0](operations-for-app-v-50.md)

 

 





