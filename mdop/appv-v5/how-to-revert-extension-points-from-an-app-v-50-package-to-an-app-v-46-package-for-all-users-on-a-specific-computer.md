---
title: Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для всех пользователей на указанном компьютере
description: Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для всех пользователей на указанном компьютере
ms.assetid: 2a43ca1b-6847-4dd1-ade2-336ac4ac6af0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 62542e5cd0b9dcb55f6e8f3db4d4f43c011a2839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813728"
---
# Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для всех пользователей на указанном компьютере

*Примечание:** App-V 4,6 вышел из основной поддержки. В следующем примере предполагается, что клиент App-V 4,6 с пакетом обновления 3 (SP3) уже установлен.

Используйте описанную ниже процедуру, чтобы вернуть точки расширения из пакета App-V 5,0 в формат файлов App-V 4,6 с помощью файла конфигурации развертывания.

**Отмена пакета**

1.  Убедитесь в том, что пакет App-V 4,6 опубликован для пользователей, но FTAs и сочетания клавиш предполагаются пакетом App-V 5,0 с помощью следующего метода миграции, [чтобы переносить точки расширения из пакета App-v 4,6 в преобразованный пакет App-v 5,0 для всех пользователей на определенном компьютере](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).

    В разделе **userConfiguration** файла конфигурации развертывания для преобразованного пакета, чтобы настроить политику, сделайте следующее обновление в разделе **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "ложь" PackageName = &lt; ИД &gt; пакета**

2.  В командной строке с повышенными привилегиями введите:

    PS &gt; **Set-AppvClientPackage $pkg – DynamicDeploymentConfiguration** &lt; путь к файлу конфигурации развертывания&gt;

    PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfigurationType useDeploymentConfiguration**

3.  Выполните обновление публикации или дождитесь следующего запланированного обновления публикации для пакета App-V 4,6 SP2.

    Откройте приложение с помощью FTAs или сочетаний клавиш. Теперь приложение должно открываться с помощью App-V 4,6.

    **Примечание.**  
    Если вы больше не хотите использовать пакет App-V 5,0, вы можете отменить публикацию пакета App-V 5,0, а точки расширения будут автоматически возвращены в приложение App-V 4,6.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.0](operations-for-app-v-50.md)









