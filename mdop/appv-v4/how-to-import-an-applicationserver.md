---
title: Импорт приложения
description: Импорт приложения
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817402"
---
# Импорт приложения


Как правило, импортируйте приложения, чтобы они были доступны для потоковой передачи с сервера управления Application Virtualization. Вы также можете добавить приложение вручную, но для этого необходимо предоставить точную детальную информацию о приложении. Дополнительные сведения [можно найти в разделе Добавление приложения вручную](how-to-manually-add-an-application.md).

**Примечание**  Чтобы импортировать приложение, необходимо, чтобы на сервере была доступна программа последовательности Open Software descriptor (OSD) или файл проекта секвенсора (SPRJ).

 

При импорте приложения необходимо убедиться, что на сервере в поле " **путь содержимого по умолчанию** " на вкладке " **Общие** " в диалоговом окне " **Параметры** " (доступ к нему щелкните правой кнопкой мыши узел **системы Application Virtualization** на консоли App-V Server). Значение Path по умолчанию определяет, где будут импортироваться приложения, и в процессе импорта это значение используется для изменения путей, определенных в OSD файле для SFT и для ярлыков значков. В OSD — путь к SFT – файлу указан в записи HREF в базе кода, а путь к значкам указан в поле "ЯРЛЫКи".

В процессе импорта протокол, сервер и, если он есть, порт, указанный в этих двух путях в OSD, будет заменен значением из пути содержимого по умолчанию. В таблице ниже представлен пример того, как будет использоваться путь импорта.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Путь к содержимому по умолчанию</th>
<th align="left">HREF в базе кода файла OSD</th>
<th align="left">Результирующее значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\server\content &lt; /p&gt;</td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p>\server\content\myFolder\package.sft</p></td>
</tr>
</tbody>
</table>

 

**Импорт приложения**

1.  Щелкните правой кнопкой мыши узел **приложения** в левой области и выберите пункт **Импорт приложений**.

2.  В диалоговом окне **Открыть** перейдите в файл SPRJ или OSD приложения. Выделите файл и нажмите кнопку **Открыть**.

3.  В **мастере создания приложений**убедитесь, что выбрано поле **включена** для приложений, которые вы хотите пропотокировать. Здесь также можно ввести описание и проверить путь к серверу и файлам. Кроме того, если вы настроили лицензии и группы серверов, вы можете выбрать их.

4.  Нажмите кнопку **Далее**.

5.  На экране **опубликованные ярлыки** установите флажки для расположений, в которых вы хотите отображать ярлыки приложений на клиентских компьютерах.

6.  Нажмите кнопку **Далее**.

7.  В окне **сопоставления файлов** вы можете добавить в приложение новые сопоставления файлов. Для этого нажмите кнопку **Добавить**, введите расширение (без предшествующей точки), введите описание и нажмите кнопку **ОК**.

    **Примечание**  Приложения, упорядоченные с помощью секвенсора 4,0. Заполните диалоговое окно **сопоставления файлов** при импорте или создании с помощью консоли управления. Приложения с более ранними версиями программы Sequencer не выполняют никаких задач.

     

8.  Нажмите кнопку **Далее**.

9.  На экране **разрешения на доступ** нажмите кнопку **Добавить**.

10. Заполните диалоговое окно " **Выбор групп** ". По завершении нажмите кнопку **ОК**.

11. Нажмите кнопку **Далее**.

12. На экране **Сводка** вы можете просмотреть настройки импорта. Нажмите кнопку **Готово**или кнопку **назад** , чтобы изменить импорт, или кнопку **Отмена** , чтобы отменить импорт.

## Статьи по теме


[Управление группами приложений на консоли управления серверами](how-to-manage-application-groups-in-the-server-management-console.md)

[Управление приложениями на консоли управления серверами](how-to-manage-applications-in-the-server-management-console.md)

[Добавление приложения вручную](how-to-manually-add-an-application.md)

 

 




