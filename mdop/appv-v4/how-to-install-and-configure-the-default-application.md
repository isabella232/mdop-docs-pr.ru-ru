---
title: Установка и настройка приложения по умолчанию
description: Установка и настройка приложения по умолчанию
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817369"
---
# Установка и настройка приложения по умолчанию


Приложение по умолчанию предоставляется в рамках установки и автоматически копируется на сервер управления Microsoft Application Virtualization (App-V) Management Server во время установки. Он используется для проверки правильности установки и настройки сервера управления, но его необходимо опубликовать в клиенте Microsoft Application Virtualization (App-V), чтобы пользователь мог получить к нему доступ.

Выполните указанные ниже действия, чтобы опубликовать приложение по умолчанию и выполнить его потоковую передачу.

**Публикация приложения по умолчанию**

1.  Войдите на сервер управления App-V с помощью учетной записи, которая входит в группу администраторов App-V, указанную во время установки.

2.  На сервере управления App-V нажмите кнопку **Пуск**и выберите пункт **Администрирование**, а затем — **консоль управления Application Virtualization**.

3.  В консоли управления App-V нажмите кнопку **действия**и выберите команду **подключиться к системе виртуализации приложений**.

4.  На странице " **Настройка подключения** " снимите флажок **использовать безопасное соединение** .

5.  В поле **имя узла веб-службы** введите полное доменное имя (FQDN) сервера управления App-V и нажмите кнопку **ОК**.

    **Примечание**  Вы также можете использовать **localhost** для имени узла веб-службы, если оно установлено на сервере управления.

     

6.  В консоли управления App-V щелкните правой кнопкой мыши узел **сервера** и выберите пункт **Параметры системы**.

7.  На вкладке **Общие** в поле **путь к содержимому по умолчанию** введите путь в формате UNC к папке содержимого, созданной на сервере во время установки; Например, \ \ \ \ &lt; имя сервера &gt; \\Content и нажмите кнопку **ОК**.

    **Важно!**  Используйте полное доменное имя для имени сервера, чтобы клиент мог правильно разрешить его имя.

     

8.  В консоли управления App-V в области навигации разверните узел **сервер** и выберите пункт **приложения**.

9.  В области разделов выберите пункт **приложение по умолчанию**, а затем в области **действия** нажмите кнопку **Свойства**.

10. В диалоговом окне **Свойства** рядом с полем **путь к OSD** нажмите кнопку **Обзор**.

11. В диалоговом окне **Открытие** файла введите UNC-путь к папке содержимого, созданной на сервере во время установки. Например, \ \ \ \ &lt; имя сервера &gt; \\Content и нажмите клавишу ВВОД. Необходимо использовать фактическое имя сервера и не использовать **localhost** здесь.

    **Важно!**  Убедитесь, что значения в полях **путь к OSD** и **путь к значкам** находятся в формате UNC (например, \ \ \ \ &lt; имя сервера &gt; \\Content\\DefaultApp.ICO), и наведите указатель мыши на папку, созданную при установке сервера. Не используйте **localhost** или путь к файлу, который содержит букву диска, например c:\\program Files Files\\.. \\.. Конфликтов.

     

12. Выберите файл DefaultApp. OSD и нажмите кнопку **Открыть**.

13. Повторите описанные выше действия, чтобы настроить путь значка.

14. Откройте вкладку **разрешения на доступ** и убедитесь в том, что группе Пользователи App-V предоставлены разрешения на доступ к приложению.

15. Откройте вкладку **сочетания клавиш** и нажмите кнопку **опубликовать на рабочем столе пользователя**. Нажмите кнопку **ОК**.

16. Откройте проводник и найдите каталог содержимого.

17. Дважды щелкните файл DefaultApp. OSD и откройте его в блокноте.

18. Найдите строку, содержащую тег **href** , и измените ее на следующий код:

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    Если вы используете протоколы RTSP, выполните указанные ниже действия.

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. Закройте файл DefaultApp. OSD и сохраните изменения.

**Потоковая передача приложения по умолчанию**

1.  На компьютере с установленным клиентом App-V Войдите в систему под учетной записью пользователя, который является членом группы Пользователи Application Virtualization, указанной во время установки сервера.

2.  На рабочем столе появится ярлык **приложения Application Virtualization по умолчанию** . Дважды щелкните ярлык, чтобы запустить приложение.

3.  В строке состояния, которая отображается над областью уведомлений Windows, сообщается о том, что приложение запускается. При успешном запуске приложения отображается окно заголовка для приложения по умолчанию. Нажмите кнопку **ОК** , чтобы закрыть диалоговое окно. Теперь вы подтвердили правильность работы системы App-V.

## Статьи по теме


[Настройка серверов для развертывания на основе сервера](how-to-configure-servers-for-server-based-deployment.md)

 

 




