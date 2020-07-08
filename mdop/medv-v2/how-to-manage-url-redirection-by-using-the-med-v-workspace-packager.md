---
title: Управление перенаправлением URL-адресов с помощью упаковщика рабочих областей MED-V
description: Управление перенаправлением URL-адресов с помощью упаковщика рабочих областей MED-V
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824819"
---
# Управление перенаправлением URL-адресов с помощью упаковщика рабочих областей MED-V


Вы можете использовать диспетчер рабочих областей MED-V для управления перенаправлением URL-адресов в рабочей области MED-V.

**Управление перенаправлением веб-адресов в рабочей области MED-V**

1.  Чтобы открыть **Диспетчер рабочих областей MED-V**, нажмите **кнопку Пуск**, выберите **все программы**, а затем — **Microsoft Enterprise Virtualization**, а затем — **Диспетчер рабочих областей med-v**.

2.  На главной панели **диспетчера рабочих областей MED-V** выберите пункт **Управление перенаправлением веб-сайта**.

3.  В окне **Управление веб-перенаправлением** можно вводить, вставлять и импортировать список URL-адресов, перенаправленных в Internet Explorer в рабочей области MED-V.

    **Примечание.**  
    Перенаправление URL-адресов в MED-V поддерживает только протоколы HTTP и HTTPS. MED-V не обеспечивает поддержку FTP или других протоколов.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. Нажмите кнопку **Сохранить как...** чтобы сохранить обновленные файлы перенаправления URL-адресов в указанной папке. MED-V создает файл реестра, содержащий обновленные сведения о перенаправлении URL-адреса. Разверните обновленный раздел реестра с помощью групповой политики. Дополнительные сведения об использовании групповой политики можно найти в разделе [Установка программного обеспечения групповой политики](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

   В заданной папке MED-V также создается сценарий Windows PowerShell, который можно использовать для повторного создания обновленного пакета рабочей области для MED-V.

## Статьи по теме


[Добавление или удаление сведений о перенаправлении URL-адресов в развернутой рабочей области MED-V](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[Управление перенаправлением URL-адресов MED-V](manage-med-v-url-redirection.md)









