---
title: Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для конкретного пользователя
description: Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для конкретного пользователя
author: dansimp
ms.assetid: bd53c5d6-7fd2-4816-b03b-d59da0a35819
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a69d6fb5b180161f39aa89e03b52227f32ce4879
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813733"
---
# Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для конкретного пользователя


Чтобы вернуть пакет App-V 5,1 в формат файла App-V с помощью файла конфигурации пользователя, выполните описанные ниже действия.

**Отмена пакета**

1.  Убедитесь в том, что пакет App-V 4,6 опубликован для пользователей, но FTAs и сочетания клавиш предполагались пакетом App-V 5,1 с помощью следующего метода миграции, [как переносить точки расширения из пакета App-v 4,6 в приложение App-v 5,1 для определенного пользователя](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).

    В разделе **userConfiguration** файла конфигурации развертывания для преобразованного пакета, чтобы настроить политику, сделайте следующее обновление в разделе **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "ложь" PackageName = &lt; ИД &gt; пакета**

2.  В командной строке с повышенными привилегиями введите:

    PS &gt; **Publish-AppVClientPackage $pkg — DynamicUserConfigurationPath** &lt; путь к файлу конфигурации пользователя&gt;

3.  Выполните обновление публикации или дождитесь следующего запланированного обновления публикации для App-V 4,6. Откройте приложение с помощью FTAs или сочетаний клавиш. Теперь приложение должно открываться с помощью App-V 4,6.

    **Примечание.**  
    Если вы больше не хотите использовать пакет App-V 5,1, вы можете отменить публикацию пакета App-V 5,1, а точки расширения будут автоматически возвращены в приложение App-V 4,6.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.1](operations-for-app-v-51.md)









