---
title: Порядок включения отчетов в клиенте App-V 5.1 с помощью PowerShell
description: Порядок включения отчетов в клиенте App-V 5.1 с помощью PowerShell
author: dansimp
ms.assetid: c4c58be6-cc50-44f6-bf4f-8346fc5d0c0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1d8c0d5e1930020ed1ce354f806f8917a9644e02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814072"
---
# Порядок включения отчетов в клиенте App-V 5.1 с помощью PowerShell


Чтобы настроить приложение App-V 5,1 для создания отчетов, выполните описанные ниже действия.

**Настройка компьютера с клиентским приложением App-V 5,1 для создания отчетов**

1. Установите клиент App-V 5,1. Дополнительные сведения об установке клиента см. в разделе [развертывание клиента App-V](how-to-deploy-the-app-v-client-51gb18030.md).

2. После установки клиента App-V 5,1 с помощью PowerShell **Set-AppvClientConfiguration** настройте соответствующие параметры конфигурации отчетов.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Параметр</th>
   <th align="left">Описание</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>ReportingEnabled</p></td>
   <td align="left"><p>Позволяет клиенту возвращать данные на сервер отчетов. Этот параметр необходим для того, чтобы клиент собирал данные отчета на клиенте.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingServerURL</p></td>
   <td align="left"><p>Задает расположение на сервере отчетов, на котором сохраняются сведения о клиенте. Например, http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt; .</p>
   <div class="alert">
   <strong>Примечание.</strong><br/><p>Номер порта, назначенный во время настройки сервера отчетов</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Время начала отчета</p></td>
   <td align="left"><p>Задается запланировать клиент для автоматической отправки данных на сервер. Этот параметр укажет время, когда данные отчета будут начинаться с начала отправки. Он представлен в 24-часовом формате и займет число от 0-23.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingRandomDelay</p></td>
   <td align="left"><p>Указывает максимальную задержку (в минутах) для данных, отправляемых на сервер отчетов. При запуске запланированной задачи клиент создает произвольную задержку от 0 до ReportingRandomDelay и ждет указанное время перед отправкой данных.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingInterval</p></td>
   <td align="left"><p>Указывает интервал повтора, который будет использоваться клиентом для повторной отправки данных на сервер отчетов.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingDataCacheLimit</p></td>
   <td align="left"><p>Задает максимальный размер кэша XML в мегабайтах (МБ) для хранения сведений о отчетах. Размер применяется к кэшу в памяти. По достижении этого предела файл журнала будет выполнен.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingDataBlockSize</p></td>
   <td align="left"><p>Задает максимальный размер кэша XML в мегабайтах (МБ) для хранения сведений о отчетах. Размер применяется к кэшу в памяти. По достижении этого предела файл журнала будет выполнен.</p></td>
   </tr>
   </tbody>
   </table>



3. После настройки соответствующих параметров компьютер, на котором работает клиент App-V 5,1, будет автоматически собирать данные и отправлять данные обратно на сервер отчетов.

   Кроме того, администраторы могут вручную отправлять данные по запросу с помощью командлета PowerShell **Send-AppvClientReport** .

   **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Администрирование App-V 5.1 с помощью PowerShell](administering-app-v-51-by-using-powershell.md)









