---
title: Отправка образа MED-V на сервер
description: Отправка образа MED-V на сервер
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825702"
---
# Отправка образа MED-V на сервер


После тестирования образа MED-V его можно упаковывать, а затем отправлять на сервер. Сведения о настройке веб-сервера изображений можно найти в разделе [Настройка образа веб-сервера распространения](how-to-configure-the-image-web-distribution-server.md).

После того как изображение MED-V будет упаковано и загружено на сервер, оно может быть распределено между пользователями с помощью корпоративного центра распространения программного обеспечения или может быть загружено пользователями с помощью пакета развертывания. Сведения о развертывании с помощью корпоративного центра распространения программного обеспечения можно найти в разделе [Развертывание рабочей области MED-V с помощью корпоративной системы распространения программного обеспечения](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md). Сведения о развертывании с помощью пакета можно найти в разделе [Развертывание рабочей области MED-V с помощью пакета развертывания](deploying-a-med-v-workspace-using-a-deployment-package.md).

**Примечание.**  
Перед отправкой изображения убедитесь в том, что веб-прокси не определен в параметрах браузера, и что служба Windows Update не работает в данный момент.



**Отправка изображения MED-V на сервер**

1.  В области **локальные Упакованные изображения** выберите созданное изображение.

2.  Нажмите кнопку **Отправить**.

    Изображение будет отправлено на сервер. Это может занять значительно немного времени.

    Изображения на сервере определяются с помощью свойств, перечисленных в приведенной ниже таблице.

**Упакованные изображения в свойствах сервера**

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

[Упаковка образа MED-V](how-to-pack-a-med-v-image.md)









