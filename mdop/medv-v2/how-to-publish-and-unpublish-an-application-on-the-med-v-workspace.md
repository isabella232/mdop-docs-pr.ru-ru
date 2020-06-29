---
title: Публикация и отмена публикации приложения в рабочей области MED-V
description: Публикация и отмена публикации приложения в рабочей области MED-V
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826922"
---
# Публикация и отмена публикации приложения в рабочей области MED-V


Несмотря на то что приложение установлено в рабочей области MED-V, вам также может потребоваться опубликовать приложение, прежде чем оно станет доступно конечному пользователю. По умолчанию большинство приложений публикуются на момент их установки, а также для создания и включения сочетаний клавиш.

В некоторых случаях вам может потребоваться установить приложения в рабочую область для MED-V, не открывая их пользователям, например антивирусному программному обеспечению. Кроме того, существуют ситуации, в которых вы хотите опубликовать приложение, установленное в рабочей области MED-V, которое ранее было недоступно для конечного пользователя. Например, может потребоваться опубликовать установленное приложение, если в меню " **Пуск** " не был автоматически создан ярлык.

**Важно!**  Если вы публикуете приложение, которое не поддерживает пути UNC, рекомендуется сопоставить приложение с диском.

 

Вы можете опубликовать или отменить публикацию приложений в развернутой рабочей области для MED-V, выполнив одно из указанных ниже действий.

**Публикация и Отмена публикации установленного приложения**

1.  Чтобы опубликовать приложение в развернутой рабочей области MED-V, Скопируйте ярлык этого приложения в следующую папку на виртуальной машине:

    Меню C:\\Documents и Settings\\All Users\\Start

    При необходимости используйте групповую политику или систему ESD, чтобы развернуть сценарий, который копирует ярлык для этого приложения в папку "все" в меню "все" Users\\Start.

2.  Чтобы отменить публикацию приложения в развернутой рабочей области MED-V, удалите ярлык для этого приложения из следующей папки на виртуальной машине:

    Меню C:\\Documents и Settings\\All Users\\Start

    При необходимости используйте групповую политику или систему ESD для развертывания сценария, который удаляет сочетание клавиш для этого приложения, из папки "все" в меню "все Users\\Start".

    **Примечание**  Часто этот ярлык автоматически удаляется из меню **Пуск** главного компьютера при удалении приложения. Тем не менее, в некоторых случаях, например, для рабочей области MED-V, настроенной для всех пользователей общего компьютера, может потребоваться вручную удалить ярлык в меню " **Пуск** " после удаления приложения. Это можно сделать, щелкнув ярлык правой кнопкой мыши и выбрав команду **Удалить**.

     

Чтобы убедиться в том, что приложение опубликовано или не опубликовано, проверьте, доступен ли соответствующий ярлык в рабочей области MED-V.

**Примечание**  Приложения, которые включены в пакет обновления 3 (SP3) для Windows XP и находятся в папке меню "Пуск" виртуальной машины, не публикуются автоматически на узле. Они управляются параметрами реестра, которые блокируют автоматическую публикацию. Дополнительные сведения можно найти в разделе [список исключений приложений для Windows Virtual PC](windows-virtual-pc-application-exclude-list.md).

 

**Публикация элементов панели управления**

1.  Создайте на виртуальной машине ярлык, на котором целевым объектом является имя элемента, например C:\\WINDOWS\\system32\\appwiz.cpl.

    Сочетание клавиш должно быть либо создано в папку "%ALLUSERSPROFILE%\\Start Menu\\", либо в одной из вложенных в нее папок.

    Элемент будет опубликован на главном компьютере в соответствующем месте в папке главного меню.

2.  Начните с ярлыка для элемента на узле.

**Внимание!**  При создании ярлыка не указывайте% SystemRoot% \\control.exe. Это приложение не будет опубликовано, так как оно содержится в параметрах реестра, которые блокируют автоматическую публикацию.

 

**Как MED-V обрабатывает автоматическую публикацию приложений**

1.  Во время публикации приложения MED-V копирует ярлыки с гостевой виртуальной машины на главный компьютер, пытаясь сопоставить ее с иерархией папок, существующей в гостевой системе. Для этого MED-V копирует ярлыки с гостя на узел, выполнив следующие действия:

    1.  MED-V пытается найти папку в разделе Start Menu\\Programs на главном компьютере с именем, совпадающим с папкой гостя, в которой находится сочетание клавиш.

    2.  Если совпадающей папки нет, MED-V затем пытается найти папку в папке главного меню, имя которой совпадает с папкой в гостевой системе, в которой находится сочетание клавиш.

    3.  Если совпадающей папки нет, MED-V копирует ярлык в папку по умолчанию на узле, в папке Start Menu\\Programs.

2.  Пример процесса публикации приложения:

    1.  Если ярлык приложения опубликован в папке Start Menu\\Programs\\AppShortcuts на гостевой машине, то MED-V на главном компьютере в папке Start Menu\\Programs\\ AppShortcuts и, если она найдена, копирует ярлык в эту папку.

    2.  Если папка не найдена, то MED-V обнаруживает папку Start Menu\\AppShortcuts на главном компьютере и, если она найдена, копирует ярлык в эту папку.

    3.  Если папка не найдена, то MED-V копирует ярлык в папку Start Menu\\Programs.

**Примечание**  В папке меню "Пуск" главного компьютера должна быть уже есть папка, в которой вы можете скопировать ярлык с помощью MED-V. В случае, если она еще не создана, MED-V не создает папку.

 

## Статьи по теме


[Установка и удаление приложения в рабочей области MED-V](installing-and-removing-an-application-on-the-med-v-workspace.md)

[Управление обновлениями программного обеспечения для рабочих областей MED-V](managing-software-updates-for-med-v-workspaces.md)

[Список исключений приложения Windows Virtual PC](windows-virtual-pc-application-exclude-list.md)

 

 




