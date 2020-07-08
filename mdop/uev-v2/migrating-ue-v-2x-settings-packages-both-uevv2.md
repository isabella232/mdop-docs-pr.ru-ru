---
title: Миграция пакетов параметров UE-V 2. x
description: Миграция пакетов параметров UE-V 2. x
author: dansimp
ms.assetid: f79381f4-e142-405c-b728-5c048502aa70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0aa1f1c36594d69de40306dfa70a4a0cf5c86dbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825519"
---
# Миграция пакетов параметров UE-V 2. x


В жизненном цикле приложения Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 или 2,1 SP1, возможно, потребуется переместить пакеты параметров пользователя при переходе на новый сервер или при выполнении резервного копирования. Возможно, требуется миграция пакетов параметров в следующих сценариях.

-   Обновление существующего серверного оборудования на более современный сервер.

-   Миграция местоположения хранилища параметров с тестового сервера на рабочий сервер.

При копировании файлов и папок не сохраняются параметры безопасности и разрешения. Ниже описаны действия, которые необходимо выполнить, чтобы правильно скопировать пакет параметров вместе с разрешениями файловой системы NTFS на новый общий доступ.

**Сохранение пакетов параметров UE-V 2 при переходе на новый сервер**

1.  В новом расположении на другом сервере создайте новую папку, например MySettings.

2.  Отключите общий доступ для старой папки на старом сервере.

3.  Копирование существующих пакетов параметров на новый сервер с помощью средства Robocopy

    ``` syntax
    C:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    **Примечание**  Для наблюдения за ходом копирования откройте MySettings.txt с помощью средства просмотра журнала, например Trace32.

     

4.  Предоставьте разрешения на доступ к новому общему доступу. Оставьте разрешения на доступ к файловой системе NTFS, так как они были установлены программой Robocopy.

    На компьютерах, на которых запущен агент UE-V, обновите параметр конфигурации **SettingsStoragePath** , указав путь к новому общему ресурсу в формате UNC (Universal Naming Convention).

    **У вас есть предложение UE-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **У вас возникла ошибка UE-V**? Воспользуйтесь [форумом на сайте UE-V TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Статьи по теме


[Администрирование UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

 

 





