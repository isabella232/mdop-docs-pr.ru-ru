---
title: Установка консоли управления
description: Установка консоли управления
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817302"
---
# Установка консоли управления


Вы можете использовать описанную ниже процедуру, чтобы установить консоль управления Application Virtualization на целевом компьютере в сети. Необходимо использовать сетевую учетную запись с правами администратора на целевом компьютере. Вы можете использовать консоль для настройки и управления платформой системы виртуализации приложений.

Перед выполнением этой процедуры необходимо установить веб-службу управления виртуализацией приложений на этом или другом компьютере. Веб-служба управления позволяет получать доступ к хранилищу данных и контроллеру домена. Дополнительные сведения об установке веб-службы можно найти [в разделе Установка веб-службы управления](how-to-install-the-management-web-service.md).

**Установка консоли управления**

1.  Убедитесь, что на целевом компьютере не установлены предыдущие версии консоли управления.

2.  Перейдите к расположению программы установки системы Application Virtualization в сети, запустите эту программу из сети или скопируйте ее каталог на конечный компьютер, а затем дважды щелкните **Setup.exe**.

3.  На **странице приветствия**нажмите кнопку **Далее**.

4.  На странице Лицензионное **соглашение** для подтверждения лицензионного соглашения установите флажок **я принимаю условия лицензии**и нажмите кнопку **Далее**.

5.  На странице **регистрационные данные** укажите **имя пользователя** и сведения об **Организации** , а затем нажмите кнопку **Далее**.

6.  На странице **Настройка типа** выберите пункт **Настраиваемая** и нажмите кнопку **Далее**.

7.  На странице **Выборочная настройка** отмените выбор всех компонентов системы Application Virtualization, кроме **консоли управления**, и нажмите кнопку **Далее**.

    **Примечание**  Если компонент уже установлен на компьютере, то после его выбора на экране выборочной настройки он будет автоматически удален.

     

8.  На экране **Готово для изменения программы** нажмите кнопку **установить**.

    **Примечание**  Если вы устанавливаете первый устанавливаемый компонент, появится страница **Готово для установки программы** . Чтобы начать установку, нажмите кнопку **установить**.

     

9.  На экране **завершения мастера установки** нажмите кнопку **Готово**. Нажмите кнопку **ОК** , чтобы перезагрузить компьютер и завершить установку.

10. На панели управления Windows дважды щелкните элемент **Администрирование** , а затем выберите **консоль управления Application Virtualization** , чтобы отобразить консоль управления.

11. Щелкните значок **подключения** или щелкните правой кнопкой мыши контейнер **системы Application Virtualization** и выберите пункт **подключиться к системе виртуализации приложений**.

12. На экране **Подключение к системе виртуализации приложений** введите имя узла и порт компьютера веб-службы управления, измените сведения о безопасности и учетные данные для входа, если это необходимо, и нажмите кнопку **ОК**.

13. После подключения к компьютеру веб-службы управления выберите в меню **консоль** пункт **файл** , а затем — команду **выход**. Нажмите кнопку **Да** , чтобы сохранить параметры консоли.

## Статьи по теме


[Установка серверов и компонентов системы](how-to-install-the-servers-and-system-components.md)

 

 




