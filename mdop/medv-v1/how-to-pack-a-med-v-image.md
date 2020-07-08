---
title: Упаковка образа MED-V
description: Упаковка образа MED-V
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824679"
---
# Упаковка образа MED-V


Образ MED-V необходимо упаковать, прежде чем его можно будет добавить в пакет развертывания или отправить на сервер.

**Создание упакованного изображения MED-V**

1.  Нажмите кнопку Управление **изображениями** .

2.  В области **Images (изображения** в **локальных упакованных изображениях** ) нажмите кнопку **создать**.

3.  В диалоговом окне **Создание упакованных изображений** выберите образ виртуальной машины, выполнив одно из указанных ниже действий.

    -   В поле **базовый файл изображения** введите полный путь к каталогу, в котором находится образ Microsoft Virtual PC, подготовленный для MED-V.

    -   Нажмите кнопку **Обзор** , чтобы перейти к каталогу, в котором находится изображение Microsoft Virtual PC, подготовленное для MED-V.

4.  Укажите имя нового изображения, выполнив одно из указанных ниже действий.

    -   В поле **имя изображения** введите нужное имя.

        **Примечание.**  
        Следующие символы не могут быть включены в имя изображения: Space " &lt; &gt; | \\ / : \* ?



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. Нажмите кнопку **ОК**.

   На главном компьютере будет создано новое упакованное изображение MED-V со свойствами, определенными в приведенной ниже таблице.

**Примечание.**  
В **локальных упакованных изображениях** и **упакованных изображениях на** панелях сервера самая последняя версия каждого изображения отображается как родительский узел. Щелкните родительский узел, чтобы просмотреть все существующие версии изображения.



**Свойства локальных упакованных изображений**

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
<td align="left"><p>Имя изображения</p></td>
<td align="left"><p>Имя упакованного изображения в том виде, в каком оно было определено при создании изображения администратором.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Версия</p></td>
<td align="left"><p>Версия отображаемого изображения.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Все предыдущие версии сохраняются, если не удаляется.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Размер файла (сжатый)</p></td>
<td align="left"><p>Физический размер изображения в сжатом виде.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Размер изображения (без сжатия)</p></td>
<td align="left"><p>Физический размер изображения в несжатом виде.</p></td>
</tr>
</tbody>
</table>



## Статьи по теме


[Установка клиента MED-V и консоли управления MED-V](how-to-install-med-v-client-and-med-v-management-console.md)

[Использование пользовательского интерфейса консоли управления MED-V](using-the-med-v-management-console-user-interface.md)

[Создание образа Virtual PC для MED-V](creating-a-virtual-pc-image-for-med-v.md)









