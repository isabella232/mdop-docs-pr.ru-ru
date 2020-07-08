---
title: Упорядочение пакета с помощью PowerShell
description: Упорядочение пакета с помощью PowerShell
author: dansimp
ms.assetid: b41feed9-d1c5-48a3-940c-9a21d594f4f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbb9641ba75eda4d190892fa2bd0043c92ed9006
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813701"
---
# Упорядочение пакета с помощью PowerShell


Чтобы создать новый пакет App-V 5,0 с помощью PowerShell, выполните указанные ниже действия.

**Примечание**  Прежде чем использовать эту процедуру, необходимо скопировать соответствующие файлы установщика на компьютер, на котором работает программа Sequencer, и ознакомиться с разделом секвенсор, описанным в разделе [планирование для приложения App-V 5,0 Sequencer и Client Deployment](planning-for-the-app-v-50-sequencer-and-client-deployment.md).

 

**Создание нового виртуального приложения с помощью PowerShell**

1.  Установите секвенсор App-V 5,0. Дополнительные сведения об установке секвенсора вы узнаете, [как установить секвенсор](how-to-install-the-sequencer-beta-gb18030.md).

2.  Чтобы открыть консоль PowerShell, нажмите кнопку **Пуск** и введите **PowerShell**. Щелкните правой кнопкой мыши элемент **Windows PowerShell** и выберите пункт **Запуск от имени администратора**.

3.  С помощью консоли PowerShell введите следующую команду: **Import-Module appvsequencer**.

4.  Чтобы создать пакет, используйте командлет **New-AppvSequencerPackage** . Для создания пакета необходимы следующие параметры:

    -   **Name (имя** ) — задает имя пакета.

    -   **PrimaryVirtualApplicationDirectory** — задает путь к каталогу, который будет использоваться для установки приложения. Этот путь должен существовать.

    -   **Installer (установщик** ) — задает путь к соответствующему установщику приложения.

    -   **Path** — задает выходной каталог для пакета.

    Пример

    **New-AppvSequencerPackage-Name (имя &lt; пакета &gt; -PrimaryVirtualApplicationDirectory) путь к &lt; корневому &gt; &lt; каталогу пакета — путь к исполняемому файлу установщика &gt; -OutputPath для &lt; пути вывода.&gt;**

    Дождитесь, пока секвенсор создаст пакет. Создание пакета с помощью PowerShell может занять некоторое время. Если пакет не был создан успешно, будет возвращено сообщение об ошибке.

    В следующем списке приведены дополнительные параметры, которые можно использовать с командлетом **New-AppvSequencerPackage** :

    -   AcceleratorFilePath — задает путь к CAB-файлу ускорителя для создания пакета.

    -   InstalledFilesPath — задает путь к папке, в которой сохраняются локальные файлы приложения.

    -   InstallMediaPath — задает путь к установочному носителю.

    -   TemplateFilePath — путь к файлу шаблона, если вы хотите настроить процесс упорядочения.

    -   FullLoad — указывает на то, что пакет должен быть полностью загружен на компьютер, на котором запущено приложение App-V 5,0, прежде чем его можно будет открыть.

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Администрирование App-V с помощью PowerShell](administering-app-v-by-using-powershell.md)

 

 





