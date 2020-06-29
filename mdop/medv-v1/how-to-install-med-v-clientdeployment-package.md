---
title: Установка клиента MED-V
description: Установка клиента MED-V
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827192"
---
# Установка клиента MED-V


В сценарии, основанном на пакете развертывания, установка клиента MED-V входит в пакет развертывания и устанавливается непосредственно из пакета.

**Важно.**  
При использовании пакета развертывания, не включающего изображение, убедитесь, что изображение загружено в веб-сайт или помещается в папку предварительной подготовки перед установкой пакета развертывания.



**Установка пакета развертывания**

1.  Выполните одно из следующих действий.

    -   Скачайте пакет MED-V из Интернета.

    -   Вставьте USB-или DVD-диск в развертывание на несущем устройстве.

2.  Если MED-V не запускается автоматически, дважды щелкните MED-VAutoInstaller.exe.

    Откроется диалоговое окно со списком компонентов, которые уже установлены и которые в данный момент устанавливаются.

    **Примечание.**  
    Если на главном компьютере установлена неподдерживаемая версия Microsoft Virtual PC, появится сообщение о том, что вы удалите существующую версию и снова запустите установщик.



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. При необходимости перезагрузите компьютер.

   После завершения установки MED-V запустится и появится сообщение о том, что установка завершена.

4. Войдите в MED-V, используя следующие имя пользователя и пароль:

   -   Введите имя домена и имя пользователя, а затем пароль пользователя домена, которому разрешено работать с MED-V.

       Пример: "Domain \ _name \\user\ _name", "Password"

## Статьи по теме


[Настройка пакета развертывания](how-to-configure-a-deployment-package.md)

[Отправка образа MED-V на сервер](how-to-upload-a-med-v-image-to-the-server.md)

[Справочник по командной строке установки клиента](client-installation-command-line-reference.md)









