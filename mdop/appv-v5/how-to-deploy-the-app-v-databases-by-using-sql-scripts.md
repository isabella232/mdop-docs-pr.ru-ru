---
title: Развертывание баз данных App-V с помощью сценариев SQL
description: Развертывание баз данных App-V с помощью сценариев SQL
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814112"
---
# Развертывание баз данных App-V с помощью сценариев SQL


Чтобы использовать сценарии SQL, а не установщик Windows, выполните указанные ниже инструкции.

-   Установка баз данных App-V 5,0

-   Обновление баз данных 5,0 до более поздней версии

**Установка баз данных App-V с помощью сценариев SQL**

1. Прежде чем устанавливать сценарии базы данных, ознакомьтесь с условиями лицензионного соглашения App-V и сохраните их. Запустив сценарии базы данных, вы соглашаетесь с условиями лицензионного соглашения. Если вы не согласны, не используйте это программное обеспечение.

2. Скопируйте **appv\_server\_setup.exe** из среды выпуска App-V в временное расположение.

3. В командной строке запустите **appv\_server\_setup.exe** и укажите временное расположение для извлечения сценариев базы данных.

   Пример: appv\_server\_setup.exe/Layout c:\\ &lt; Temporary Location (путь)&gt;

4. Перейдите к созданному временному расположению, откройте папку извлеченные **DatabaseScripts** и просмотрите инструкции в соответствующем файле Readme.txt.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">База данных</th>
   <th align="left">Расположение используемого файла Readme.txt</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>База данных управления</p></td>
   <td align="left"><p>Вложенная папка ManagementDatabase</p>
   <div class="alert">
   <strong>Важно.</strong><br/><p>Если вы обновляете или устанавливаете базу данных управления App-V 5,0 SP3, ознакомьтесь со <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> сценариями SQL для установки или обновления базы данных сервера управления для App-v 5,0 SP3 </a> .</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p>База данных отчетов</p></td>
   <td align="left"><p>Вложенная папка ReportingDatabase</p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Статьи по теме


[Развертывание сервера App-V 5.0](deploying-the-app-v-50-server.md)

[Порядок развертывания сервера App-V 5.0](how-to-deploy-the-app-v-50-server-50sp3.md)









