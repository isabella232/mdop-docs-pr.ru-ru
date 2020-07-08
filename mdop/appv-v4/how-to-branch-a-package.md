---
title: Разветвление пакета
description: Разветвление пакета
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818129"
---
# Разветвление пакета


Используйте эту процедуру, чтобы изменить существующий пакет приложения в последовательности, чтобы можно было выполнить его параллельно с исходным пакетом приложения. Этот процесс называется ветвлением. При ветвлении пакета виртуальных приложений вы можете запускать две версии одного пакета. Например, вы можете применить пакет обновления к существующему пакету и выполнить его параллельно с исходным пакетом виртуального приложения.

Используйте описанную ниже процедуру для ветвления упорядоченного виртуального пакета приложения.

**Переход к последовательности виртуальных пакетов приложений**

1.  Откройте секвенсор Microsoft Application Virtualization (App-V). Чтобы указать каталог назначения, содержащий пакет (. SPRJ), выберите пункт **файл**, **Открыть**.

2.  Перейдите в каталог, содержащий виртуализированное приложение, которое вы собираетесь создать, и нажмите кнопку **Открыть**.

3.  Чтобы сохранить копию пакета, в секвенсоре App-V выберите **файл**, **Сохранить как**. Укажите новое уникальное имя и укажите новый уникальный корневой каталог пакета для копии пакета. Нажмите кнопку **Сохранить**.

    **Важно.**  
    Необходимо указать новое имя пакета или перезаписать существующую версию пакета.



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. После сохранения новой версии вы можете применить необходимые изменения конфигурации и сохранить соответствующие файлы ICO, OSD, SFT и SPRJ в правильном расположении на сервере Application Virtualization (App-V).

## Статьи по теме


[Задачи Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)









