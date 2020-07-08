---
title: Настройка параметров виртуальной машины для рабочей области MED-V
description: Настройка параметров виртуальной машины для рабочей области MED-V
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827072"
---
# Настройка параметров виртуальной машины для рабочей области MED-V


Все параметры конфигурации настройки виртуальной машины настраиваются в модуле **политики** на вкладке " **Настройка виртуальной** машины".

## Настройка параметров виртуальной машины для постоянной рабочей области MED-V


**Настройка настройки виртуальной машины для постоянной рабочей области MED-V**

1.  Щелкните постоянную рабочую область MED-V, которую нужно настроить.

2.  В разделе **Постоянная настройка виртуальной машины** настройте свойства, как описано в приведенной ниже таблице.

    **Примечание.**  
    Параметры постоянной настройки виртуальной машины включены только для постоянной рабочей области MED-V.



3.  В меню **Политика** выберите команду **сохранить**.

**Свойства настройки постоянной виртуальной машины**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Свойство</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Запуск настройки виртуальной машины</p></td>
<td align="left"><p>Установите этот флажок, чтобы запустить сценарий настройки при первом запуске рабочей области для MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Редактор сценариев</p></td>
<td align="left"><p>Щелкните, чтобы настроить сценарий настройки. Дополнительные сведения <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> можно найти в разделе Настройка действий сценария </a> .</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Эта кнопка доступна только в том случае <strong> , если выбран параметр запустить сценарий настройки ВМ </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Сообщение, отображаемое при запуске сценария</p></td>
<td align="left"><p>Сообщение, которое будет отображаться при выполнении сценария. Если оставить это поле пустым, появится сообщение по умолчанию.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Это поле доступно только в том случае <strong> , если установлен флажок Запустить сценарий настройки ВМ </strong> .</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Настройка параметров виртуальной машины для рабочей Revertible MED-V


**Настройка настройки виртуальной машины для рабочей области revertible MED-V**

1.  Щелкните рабочую область revertible MED-V для настройки.

2.  В разделе **Настройка виртуальной машины Revertible** настройте свойства, как описано в приведенной ниже таблице.

    **Примечание.**  
    Параметры настройки виртуальной машины revertible включены только для рабочей области revertible MED-V.



3.  В меню **Политика** выберите команду **сохранить**.

**Свойства настройки виртуальной машины Revertible**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Свойство</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Переименование виртуальной машины на основе шаблона имени компьютера</p></td>
<td align="left"><p>Установите этот флажок, чтобы назначить каждому компьютеру уникальное имя с помощью рабочей области MED-V, чтобы можно было различать несколько компьютеров с помощью одной и той же рабочей области MED-V.</p>
<p>Дополнительные сведения о настройке имен компьютеров можно найти в разделе <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> Настройка свойств шаблона имени компьютера виртуальной машины </a> .</p></td>
</tr>
</tbody>
</table>



## Статьи по теме


[Использование пользовательского интерфейса консоли управления MED-V](using-the-med-v-management-console-user-interface.md)

[Создание рабочей области MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Примеры конфигураций виртуальной машины](examples-of-virtual-machine-configurationsv2.md)









