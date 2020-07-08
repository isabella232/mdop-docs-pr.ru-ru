---
title: Развертывание каталога шаблонов параметров для UE-V 1.0
description: Развертывание каталога шаблонов параметров для UE-V 1.0
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826632"
---
# Развертывание каталога шаблонов параметров для UE-V 1.0


Шаблоны расположений пользовательских параметров можно хранить на пути к папке на компьютерах с Microsoft User Experience Virtualization (UE-V) или в сетевом ресурсе SMB (Server Message Block). Запланированная задача на компьютере проверяет наличие новых или обновленных шаблонов в этом расположении. Задача проверяет это расположение раз в день и обновляет режим синхронизации на основе шаблонов в этой папке. Шаблоны, добавленные или обновленные в этой папке, так как последняя проверка регистрируется агентом UE-V. Агент UE-V отменяет регистрацию шаблонов, которые были удалены из этой папки. Запланированная задача выполняется как система. Как минимум, в сетевом общем доступе должны быть предоставлены разрешения для группы Domain Computers. Кроме того, предоставьте разрешения на доступ к папке "сетевая папка" для администраторов, которые будут управлять сохраненными шаблонами. Дополнительные сведения о шаблонах расположений настраиваемых параметров можно найти в разделе [Планирование развертывания настраиваемого шаблона для UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

**Настройка каталога шаблонов параметров для UE-V**

1.  Создайте на компьютере новую папку, в которой будет храниться каталог шаблонов параметров UE-V.

2.  Установите следующие разрешения на уровне общего доступа (SMB) для папки каталога шаблонов параметров.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Учетная запись пользователя</strong></th>
    <th align="left"><strong>Рекомендации по разрешениям</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Все пользователи</p></td>
    <td align="left"><p>Нет разрешений</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Компьютеры домена</p></td>
    <td align="left"><p>Уровни разрешений "чтение"</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Администраторы</p></td>
    <td align="left"><p>Уровни разрешений на чтение и запись</p></td>
    </tr>
    </tbody>
    </table>

     

3.  Установите следующие разрешения NTFS для папки каталога шаблонов параметров.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Учетная запись пользователя</th>
    <th align="left">Рекомендуемые разрешения</th>
    <th align="left">Применить к</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Создатель/владелец</p></td>
    <td align="left"><p>Полный доступ</p></td>
    <td align="left"><p>Эта папка, вложенные папки и файлы</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Компьютеры домена</p></td>
    <td align="left"><p>Просмотр содержимого папки и чтение</p></td>
    <td align="left"><p>Эта папка, вложенные папки и файлы</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Все пользователи</p></td>
    <td align="left"><p>Нет разрешений</p></td>
    <td align="left"><p>Нет разрешений</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Администраторы</p></td>
    <td align="left"><p>Полный доступ</p></td>
    <td align="left"><p>Эта папка, вложенные папки и файлы</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Нажмите кнопку **ОК** , чтобы закрыть диалоговые окна.

## Статьи по теме


[Развертывание UE-V 1.0](deploying-ue-v-10.md)

[Планирование развертывания пользовательского шаблона для UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





