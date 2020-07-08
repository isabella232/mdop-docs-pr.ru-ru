---
title: Настройка клиента для получения пакетов приложений
description: Настройка клиента для получения пакетов приложений
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817829"
---
# Настройка клиента для получения пакетов приложений


Если клиент настроен на использование сервера управления Application Virtualization (App-V) в качестве сервера публикации, по умолчанию в следующем цикле обновления публикации клиент извлекает файлы дескриптора программного обеспечения (OSD) и манифеста пакета для каждого пакета, который пользователь уполномочен использовать. Клиент использует данные об источнике пакета, определенные в этих файлах, чтобы определить, где найти содержимое пакета, значки и сопоставления типов файлов.

Если вы хотите, чтобы клиент получал содержимое пакета (SFT-файл) с локального серверного потокового или иного другого источника, такого как веб-сервер или файл на сервере, а не с сервера управления App-V, вы можете настроить значение раздела реестра ApplicationSourceRoot на компьютере таким образом, чтобы он указывал на локальную общую информацию о содержимом на другом сервере. Файл OSD по-прежнему определяет исходный исходный путь для содержимого пакета. Тем не менее, клиент использует значение параметра ApplicationSourceRoot вместо сервера и общего доступа, указанных в пути содержимого в OSD файле. Это перенаправляет клиент для получения содержимого с другого сервера.

Кроме того, вы можете настроить значения ключа реестра OSDSourceRoot и IconSourceRoot, если вы хотите переопределить эти параметры в файле манифеста пакета или пути, отправленные сервером публикации. OSDSourceRoot указывает местонахождение источника для извлечения файла OSD для пакета приложения во время публикации. IconSourceRoot указывает исходное расположение для получения значка для пакета приложения во время публикации.

**Примечание.**  
-   Параметры IconSourceRoot и OSDSourceRoot переопределяют значения в файле манифеста пакета, поэтому при попытке развернуть пакет с помощью метода файла установщика Windows (MSI) он также переопределит значения в файле манифеста пакета, который содержится в этом MSI-файле.

-   При выполнении операций публикации и передачи данных по HTTP (S) клиенты App-V 4,5 с пакетом обновления 1 (SP1) используют параметры прокси-сервера, настроенные в Internet Explorer на компьютере пользователя.



**Настройка значения раздела реестра ApplicationSourceRoot**

-   Настройте ApplicationSourceRoot в следующем значении раздела реестра, указав либо путь UNC, либо URL-адрес.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot

    Правильным форматом UNC-пути является **\\\\computername\\sharefolder\\\ [Folder \] \ [\ \ \]**, где **Папка** является необязательной. **ComputerName** может быть полным доменным именем (FQDN) или IP-адресом, а **sharefolder** — буквой диска. Заменяется только часть **\\\\computername\\sharedfolder** или буква диска в пути OSD.

    Правильным форматом URL-пути является **протокол://ServerName: \ [Port \] \ [/path\] \ [/\]**, где **порт** и **путь** являются необязательными. Если **порт** не указан, используется порт по умолчанию для протокола. Заменяется только часть **Protocol://Server: Port** URL-адреса OSD.

    **Важно.**  
    Переменные среды не поддерживаются в определении ApplicationSourceRoot.



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**Настройка значения OSDSourceRoot**

-   Настройте OSDSourceRoot в следующем значении раздела реестра, указав либо путь UNC, либо URL-адрес.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot

    Допустимые форматы для OSDSourceRoot включают пути UNC и URL-адреса, как показано в следующем примере:

    **\\\\computername\\sharefolder\\resource** или **\\\\computername\\content** или ** &lt; диск &gt; : \\foldername**

    **http://computername/productivity/**/**https://computername/productivity/**

**Настройка значения IconSourceRoot**

-   Настройте IconSourceRoot в следующем значении раздела реестра, указав либо путь UNC, либо URL-адрес.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot

    Допустимые форматы для IconSourceRoot включают пути UNC и URL-адреса, как показано в следующем примере:

    **\\\\computername\\sharefolder\\resource** или **\\\\computername\\content** или ** &lt; диск &gt; : \\foldername**

    **http://computername/productivity/**/**https://computername/productivity/**

## Статьи по теме


[Настройка параметров реестра клиента App-V с помощью командной строки](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)









