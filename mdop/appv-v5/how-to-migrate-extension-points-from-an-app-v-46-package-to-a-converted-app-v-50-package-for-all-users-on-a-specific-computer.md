---
title: Перенос точек расширения из пакета App-V 4.6 в преобразованный пакет App-V 5.0 для всех пользователей на указанном компьютере
description: Перенос точек расширения из пакета App-V 4.6 в преобразованный пакет App-V 5.0 для всех пользователей на указанном компьютере
ms.assetid: 3ae9996f-71d9-4ca1-9aab-25b599158e55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3c53104907448edeb894cf4eb9dbb0a24d3229e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813885"
---
# Перенос точек расширения из пакета App-V 4.6 в преобразованный пакет App-V 5.0 для всех пользователей на указанном компьютере

**Примечание.** Приложение App-V 4,6 завершило работу базовой поддержки.

Чтобы перенести точки расширения из пакета App-V версии 4.6 в пакет App-V 5,0 с помощью файла конфигурации развертывания, выполните описанные ниже действия.

**Примечание**  Для следующей процедуры не требуется сервер управления App-V 5,0.

 

**Миграция точек расширения из пакета App-V 4.6 в преобразованный пакет App-v 5,0 с помощью файла конфигурации развертывания**

1. Найдите каталог, содержащий файл конфигурации развертывания для пакета, который требуется перенести. Чтобы настроить политику, сделайте следующее обновление в разделе **userConfiguration** :

   **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ИД пакета&gt;**

   Ниже приведен пример содержимого из файла конфигурации развертывания.

   &lt;? XML Version = "1.0"?&gt;

   &lt;DeploymentConfiguration

   xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageId = &lt; ИД пакета &gt; DisplayName = &lt; Отображаемое имя&gt;

   &lt;MachineConfiguration/&gt;

   &lt;UserConfiguration&gt;

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "истина"

   PackageName = &lt; ИД пакета&gt;

   &lt;/UserConfiguration&gt;

   &lt;/DeploymentConfiguration&gt;

2. Чтобы добавить пакет App-V 5,0, введите в командной строке с повышенными привилегиями PowerShell:

   PS &gt; **$pkg = Add-AppvClientPackage** **—** путь к &lt; местоположению пакета &gt;  - **DynamicDeploymentConfiguration** &lt; путь к файлу конфигурации развертывания&gt;

   PS &gt; **AppVClientPackage $pkg**

3. Чтобы протестировать миграцию, откройте виртуальное приложение с помощью связанного FTAs или сочетаний клавиш. Приложение откроется с приложением-V 5,0. Оба: пакет App-V 4,6 и преобразованный пакет App-V 5,0 публикуются для пользователя, но FTAs и сочетания клавиш для приложений предполагались в пакете App-V 5,0.

   **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для всех пользователей на указанном компьютере](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Операции, связанные с администрированием и использованием App-V 5.0](operations-for-app-v-50.md)

 

 





