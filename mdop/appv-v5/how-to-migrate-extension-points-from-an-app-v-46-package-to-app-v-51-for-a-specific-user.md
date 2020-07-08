---
title: Перенос точек расширения из пакета App-V 4.6 в App-V 5.1 для конкретного пользователя
description: Перенос точек расширения из пакета App-V 4.6 в App-V 5.1 для конкретного пользователя
author: dansimp
ms.assetid: 19da3776-5ebe-41e1-9890-12b84ef3c1c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: e2166b0f280153ad62709b21bb3477d0c4277fcd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813869"
---
# Перенос точек расширения из пакета App-V 4.6 в App-V 5.1 для конкретного пользователя


Чтобы перенести пакеты, созданные с помощью App-V, с использованием файла конфигурации пользователя, выполните указанные ниже действия.

**Примечание**  В этой процедуре предполагается, что вы используете последнюю версию App-V 4,6.

**Преобразование пакета**

1. Найдите файл конфигурации пользователя для пакета, который вы хотите преобразовать. Чтобы настроить политику, выполните следующие обновления в разделе **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID &gt; пакета**.

   Ниже приведен пример файла конфигурации пользователя.

   &lt;? XML Version = "1.0"?&gt;

   &lt;UserConfiguration PackageId = &lt; ИД пакета &gt; DisplayName = &lt; имя пакета&gt;

   xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "истина"

   PackageName = &lt; ИД пакета&gt;

   &lt;/UserConfiguration&gt;

2. Чтобы добавить пакет App-V 5,1, введите следующую команду в окне командной строки PowerShell с повышенными привилегиями:

   PS &gt; **$pkg = Add-AppvClientPackage —** путь к &lt; расположению пакета&gt;

   &gt;**DynamicUserConfiguration Publish-AppVClientPackage $pkg —** &lt; путь к файлу конфигурации пользователя&gt;

3. Откройте приложение с помощью FTAs или ярлыков прямо сейчас. Приложение должно открыться с помощью App-V 5,1.

   Пакет App-V 4,6 и преобразованный пакет приложения App-V 5,1 публикуются для пользователя, но FTAs и сочетания клавиш для приложений предполагались в пакете App-V 5,1.

   **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.1](operations-for-app-v-51.md)

[Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для конкретного пользователя](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)

 

 





