---
title: Перенос точек расширения из пакета App-V 4.6 в App-V 5.0 для конкретного пользователя
description: Перенос точек расширения из пакета App-V 4.6 в App-V 5.0 для конкретного пользователя
ms.assetid: dad25992-3c75-4b7d-b4c6-c2edf43baaea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a17d9dad11092a4c8356983b70bea3c18da1be04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813877"
---
# Перенос точек расширения из пакета App-V 4.6 в App-V 5.0 для конкретного пользователя

*Примечание:** App-V 4,6 вышел из основной поддержки.

Чтобы перенести пакеты, созданные с помощью App-V, с использованием файла конфигурации пользователя, выполните указанные ниже действия.

**Преобразование пакета**

1. Найдите файл конфигурации пользователя для пакета, который вы хотите преобразовать. Чтобы настроить политику, выполните следующие обновления в разделе **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID &gt; пакета**.

   Ниже приведен пример файла конфигурации пользователя.

   &lt;? XML Version = "1.0"?&gt;

   &lt;UserConfiguration PackageId = &lt; ИД пакета &gt; DisplayName = &lt; имя пакета&gt;

   xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "истина"

   PackageName = &lt; ИД пакета&gt;

   &lt;/UserConfiguration&gt;

2. Чтобы добавить пакет App-V 5,0, введите в командной строке с повышенными привилегиями PowerShell следующее:

   PS &gt; **$pkg = Add-AppvClientPackage —** путь к &lt; расположению пакета&gt;

   &gt;**DynamicUserConfiguration Publish-AppVClientPackage $pkg —** &lt; путь к файлу конфигурации пользователя&gt;

3. Откройте приложение с помощью FTAs или ярлыков прямо сейчас. Приложение должно открыться с помощью App-V 5,0.

   Пакет обновления 2 (SP2) для App-V и преобразованный пакет App-V 5,0 публикуются для пользователя, но FTAs и сочетания клавиш для приложений предполагались пакетом App-V 5,0.

   **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.0](operations-for-app-v-50.md)

 

 





