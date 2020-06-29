---
title: Публикация виртуального приложения на клиенте
description: Публикация виртуального приложения на клиенте
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816872"
---
# Публикация виртуального приложения на клиенте


При развертывании виртуализации приложений с помощью электронной системы распространения программного обеспечения можно использовать одну из описанных ниже процедур для публикации пакета приложения для пользователей.

**Публикация пакета в отдельном файле установщика Windows**

1.  Клиент должен быть установлен с параметром *REQUIREAUTHORIZATIONIFCACHED* , равным 0 (нулю). Дополнительные сведения об установке этого параметра можно найти в разделе [Параметры командной строки установщика клиента Application Virtualization](application-virtualization-client-installer-command-line-parameters.md)

2.  Скопируйте файл установщика Windows и SFT – файл в ту же папку на целевом компьютере.

3.  На компьютере выполните следующую команду:

    `Msiexec.exe /I "packagename.msi" /q`

**Публикация пакета с помощью установщика Windows и манифеста пакета**

1.  Скопируйте файл установщика Windows на целевой компьютер и SFT — в общую папку содержимого на потоковый сервер.

2.  На каждом компьютере пользователя выполните следующую команду:

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    **Важно!**  Для OVERRIDEURL все символы обратной косой черты должны быть escape-символами с помощью предшествующей обратной косой черты или путь OVERRIDEURL не будет анализироваться должным образом. Кроме того, свойства и значения должны быть введены прописными буквами, за исключением случаев, когда значение является путем к файлу.

     

**Публикация пакета с помощью SFTMIME**

-   Например, чтобы опубликовать приложение для всех пользователей на компьютере, выполните на компьютере пользователя следующую команду:

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    Дополнительные сведения об этих и других командах SFTMIME можно найти в разделе [Справочник по командам SFTMIME](sftmime--command-reference.md).

## Статьи по теме


[Определение способа публикации](determine-your-publishing-method.md)

[Сценарий на основе электронного распространения программного обеспечения](electronic-software-distribution-based-scenario.md)

[Справочник по командам SFTMIME](sftmime--command-reference.md)

[Сценарий изолированной доставки для клиентов Application Virtualization](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





