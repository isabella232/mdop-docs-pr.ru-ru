---
title: Параметры командной строки
description: Параметры командной строки
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819402"
---
# Параметры командной строки


Используйте следующие параметры Sequencer Application Virtualization для последовательного приложения и для обновления серийного пакета приложения в командной строке. В каталоге Microsoft Application Virtualization Sequencer введите **SFTSequencer**, а затем соответствующий параметр.

<a href="" id="-help-or---"></a>*/Help* или */?*  
Используется для отображения списка параметров, доступных для последовательностей командной строки.

<a href="" id="-installpackage-or--i"></a>*/INSTALLPACKAGE* или */i*  
Используется для указания установщика или пакетного файла для упорядочения приложения.

<a href="" id="-installpath-or--p"></a>*/INSTALLPATH* или */p*  
Используется для указания корневого каталога пакета.

<a href="" id="-outputfile-or--o"></a>*/OutputFile* или */o*  
Позволяет указать путь и имя файла SPRJ, который будет создан.

**Важно!**  Параметр */OutputFile* недоступен при открытии пакета, который вы не планируете обновлять.

 

<a href="" id="-fullload-or--f"></a>*/FULLLOAD* или */f*  
Используется, чтобы указать, нужно ли размещать все в основном блоке функций.

<a href="" id="-packagename-or--k"></a>*/PACKAGENAME* или */k*  
Используется для указания имени пакета для упорядоченного приложения.

<a href="" id="-blocksize"></a>*/BLOCKSIZE*  
Указывает размер блока SFT файла, который будет использоваться для потоковой передачи пакета на клиентские компьютеры. Вы можете выбрать одно из следующих значений:

-   4 КБ

-   16 КБ

-   32 КБ

-   64 КБ

При указании размера блока вы должны оценить размер SFT – файла. Файл с меньшим размером блока занимает больше времени для потоковой передачи по сети, но менее интенсивно использует пропускную способность. Файлы с более крупными размерами блоков используют дополнительную пропускную способность сети.

<a href="" id="-compression"></a>*/COMPRESSION*  
Используется для указания метода сжатия SFT файла в процессе его потоковой передачи клиенту.

<a href="" id="-msi-or--m"></a>*/MSI* или */m*  
Используется для указания создания пакета установщика Microsoft Windows для упорядоченного приложения.

<a href="" id="-default"></a>*/DEFAULT*  
Указывает файл SPRJ по умолчанию, который будет использоваться при создании виртуального пакета приложения. Этот файл используется в качестве шаблона. SPRJ, когда приложение выполняется в первый раз.

<a href="" id="-upgrade"></a>*/UPGRADE*  
Указывает путь и имя файла SPRJ, который будет обновлен.

<a href="" id="-decodepath"></a>*/DECODEPATH*  
Указывает каталог на компьютере виртуализации, на котором установлены файлы, связанные с пакетом упорядоченного приложения. При указании каталога используйте один из следующих форматов:

-   /DECODEPATH: Q:

-   /decodepath:Q:.

-   /decodepath:"Q:."

-   /DECODEPATH: "Q:"

## Статьи по теме


[Сведения об использовании командной строки программы Sequencer](about-using-the-sequencer-command-line.md)

[Открытие виртуализированного приложения с помощью командной строки](how-to-open-a-sequenced-application-using-the-command-line.md)

[Обновление пакета с помощью команды "Открыть пакет"](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 




