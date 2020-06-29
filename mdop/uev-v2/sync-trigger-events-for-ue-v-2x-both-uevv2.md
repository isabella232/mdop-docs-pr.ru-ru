---
title: Синхронизация событий-триггеров для UE-V 2.x
description: Синхронизация событий-триггеров для UE-V 2.x
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826799"
---
# Синхронизация событий-триггеров для UE-V 2.x


Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 и 2,1 SP1 позволяет синхронизировать приложение и параметры Windows для всех устройств, подключенных к домену. *События триггеров синхронизации* определяют, когда агент UE-V синхронизирует эти параметры с расположением хранения параметров. UE-V 2 представляет новый *метод синхронизации* с именем *SyncProvider*. Дополнительные сведения о конфигурации метода синхронизации см. в разделе [методы синхронизации для UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).

## События триггеров синхронизации UE-V 2


В приведенной ниже таблице описаны события триггеров для классических приложений и параметры Windows.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Событие триггера UE-V 2</strong></p></td>
<td align="left"><p><strong>PowerSchool = SyncProvider</strong></p></td>
<td align="left"><p><strong>PowerSchool = None</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Вход в Windows</strong></p></td>
<td align="left"><ul>
<li><p>Параметры приложений и Windows импортируются в локальный кэш из места хранения параметров.</p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)">Применяются асинхронные параметры Windows </a> .</p></li>
<li><p>Синхронные параметры Windows будут применены при следующем входе в Windows.</p></li>
<li><p>Параметры приложения будут применены при запуске приложения.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Параметры приложений и Windows считываются непосредственно из места хранения параметров.</p></li>
<li><p>Применяются асинхронные и синхронные параметры Windows.</p></li>
<li><p>Параметры приложения будут применены при запуске приложения.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Выход из Windows</strong></p></td>
<td align="left"><p>Локальное сохранение изменений и кэширование и копирование параметров асинхронных и синхронных файлов Windows на сервер расположений хранилища параметров, если он доступен.</p></td>
<td align="left"><p>Сохранение изменений, внесенных в асинхронные и синхронные места хранения параметров Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows Connect (RDP)/разблокировка</strong></p></td>
<td align="left"><p>Синхронизация всех асинхронных параметров Windows из хранилища параметров расположение в локальном кэше (если оно доступно).</p>
<p>Применение кэшированных параметров Windows</p></td>
<td align="left"><p>Скачивание и применение асинхронных параметров Windows из места хранения параметров</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Отключение Windows (RDP)/блокировка</strong></p></td>
<td align="left"><p>Сохранение изменений параметров в локальном кэше для асинхронной настройки Windows.</p>
<p>Синхронизация всех асинхронных параметров Windows из локального кэша с расположением хранения параметров, если оно доступно</p></td>
<td align="left"><p>Сохранение изменений параметров Windows в местоположении хранения параметров</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Запуск приложения</strong></p></td>
<td align="left"><p>Применение параметров приложения из локального кэша при запуске приложения</p></td>
<td align="left"><p>Применение параметров приложения из хранилища параметров при запуске приложения</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Приложение закрывается</strong></p></td>
<td align="left"><p>Сохранение всех параметров приложения в локальном кэше и копирование параметров в место хранения параметров (при наличии)</p></td>
<td align="left"><p>Сохранить изменения параметров приложения в местоположении хранения параметров</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Запланированная задача контроллера синхронизации или "Синхронизация сейчас" запускается из центра параметров компании</strong></p>
<p></p></td>
<td align="left"><p>Параметры приложений и Windows синхронизируются между местом хранения параметров и локальным кэшем.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Изменения параметров не кэшируются локально, пока приложение не закроется. Этот триггер не будет экспортировать изменения, внесенные в приложение, которое выполняется в данный момент.</p>
<p>Для параметров Windows это означает, что любые изменения не будут кэшироваться локально и экспортированы до следующей блокировки (асинхронной) или выхода из нее (асинхронный и синхронный).</p>
</div>
<div>

</div>
<p>Параметры применяются в следующих случаях:</p>
<ul>
<li><p>Асинхронные параметры Windows применяются непосредственно.</p></li>
<li><p>Параметры приложения применяются при запуске приложения.</p></li>
<li><p>При следующем входе в Windows применяются как асинхронные, так и синхронные параметры Windows.</p></li>
<li><p>Параметры приложения Windows (AppX) применяются при следующем обновлении. <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Дополнительные сведения приведены в разделе мониторинг параметров приложения </a> .</p></li>
</ul></td>
<td align="left"><p>Отсутствует</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Асинхронные параметры, обновленные в удаленном магазине *</strong></p></td>
<td align="left"><p>Загрузка и применение новых асинхронных параметров из кэша.</p></td>
<td align="left"><p>Загрузка и применение параметров из центрального сервера</p></td>
</tr>
</tbody>
</table>








## Статьи по теме


[Технический справочник по UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

[Изменение частоты выполнения запланированных задач UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[Выберите метод конфигурации для UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#config)









