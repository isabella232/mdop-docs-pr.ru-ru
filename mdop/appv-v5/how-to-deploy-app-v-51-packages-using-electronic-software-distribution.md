---
title: Развертывание пакетов App-V 5.1 с помощью системы электронного распространения программного обеспечения
description: Развертывание пакетов App-V 5.1 с помощью системы электронного распространения программного обеспечения
author: dansimp
ms.assetid: e1957a5a-1f18-42da-b2c1-a5ae5a4cca7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a9ed5fbb264f8fb9676d7fa18fe4de8019ea8e79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814184"
---
# Развертывание пакетов App-V 5.1 с помощью системы электронного распространения программного обеспечения


Вы можете использовать систему электронной рассылки программного обеспечения (ESD) для развертывания виртуальных приложений App-V 5,1 для клиентов App-V. Дополнительные сведения можно найти в документации, которая поддерживается с помощью ESD.

Требования к компонентам и параметры для развертывания пакетов App-V можно найти [в разделе Планирование развертывания App-v 5,1 с помощью электронной системы распространения программного обеспечения](planning-to-deploy-app-v-51-with-an-electronic-software-distribution-system.md).

Чтобы опубликовать пакеты на клиентских компьютерах App-V с помощью ESD, воспользуйтесь одним из указанных ниже способов.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Метод</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Функциональные возможности, предоставляемые сторонним электростатическим</p></td>
<td align="left"><p>Использование функций в независимых от друга функциях ESD.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Самостоятельный установщик Windows</p></td>
<td align="left"><p>Установите приложение на целевом клиентском компьютере, используя соответствующий файл установщика Windows (MSI), созданный при первоначальной последовательности приложения. Файл установщика Windows включает соответствующие сведения о файле App-V 5,1, используемые для настройки пакета, и копирует необходимые файлы пакета на клиент.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>Используйте командлеты PowerShell для развертывания виртуализированных приложений. Дополнительные сведения об использовании PowerShell и App-V 5,1 можно найти в разделе <a href="administering-app-v-51-by-using-powershell.md" data-raw-source="[Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md)"> Администрирование App-v 5,1 с помощью PowerShell </a> .</p></td>
</tr>
</tbody>
</table>

 

**Развертывание пакетов App-V 5,1 с помощью ESD**

1.  Установите секвенсор App-V 5,1 на компьютере в среде. Дополнительные сведения об установке секвенсора вы узнаете, [как установить секвенсор](how-to-install-the-sequencer-51beta-gb18030.md).

2.  Используйте секвенсор App-V 5,1, чтобы создать виртуальное приложение. Сведения о создании виртуального приложения можно найти в разделе [Создание виртуальных приложений для App-V 5,1 и управление ими](creating-and-managing-app-v-51-virtualized-applications.md).

3.  После создания виртуального приложения разверните пакет с помощью решения ESD.

    Если вы используете System Center Configuration Manager, начните с обзора " [Введение в Управление приложениями" в Configuration Manager, чтобы](https://go.microsoft.com/fwlink/?LinkId=281816) получить сведения об использовании App-V 5,1 и System Center2012 Configuration Manager.

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.1](operations-for-app-v-51.md)

 

 





