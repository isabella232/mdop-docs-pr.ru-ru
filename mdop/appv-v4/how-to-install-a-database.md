---
title: Установка базы данных
description: Установка базы данных
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817379"
---
# Установка базы данных


Вы можете использовать описанную ниже процедуру, чтобы установить базу данных для серверного развертывания виртуализации приложений, если база данных еще не доступна. Как правило, в рабочей среде вы будете подключаться к существующей базе данных.

**Важно!**  Чтобы установить базу данных, необходимо использовать учетную запись сети с соответствующими разрешениями. Если в вашей организации требуется, чтобы только администраторы базы данных могли создавать и выполнять обновления баз данных, можно использовать сценарии, позволяющие выполнить эту задачу.

 

**Установка базы данных**

1.  Перейдите к расположению программы установки системы Application Virtualization в сети, запустите эту программу из сети или скопируйте ее каталог на конечный компьютер, а затем дважды щелкните **Setup.exe**.

2.  На **странице приветствия**нажмите кнопку **Далее**.

3.  На странице Лицензионное **соглашение** для подтверждения лицензии выберите **я принимаю условия лицензионного**соглашения и нажмите кнопку **Далее**.

4.  На странице **зарегистрировать сведения** укажите **имя пользователя** и сведения об **Организации** , а затем нажмите кнопку **Далее**.

5.  На странице **Настройка типа** выберите пункт **Настраиваемая** и нажмите кнопку **Далее**.

6.  На странице **Выборочная настройка** отмените выбор всех компонентов системы Application Virtualization, кроме **сервера Application Virtualization**, и нажмите кнопку **Далее**.

    **Примечание**  Если компонент уже установлен на компьютере, отмените его выбор на экране **выборочной установки** , и он будет автоматически удален.

     

7.  На странице **сервер базы данных** введите пароли, назначьте путь установки, сохраните данные и нажмите кнопку **Далее**.

8.  Выберите имя базы данных и нажмите кнопку **Далее**.

    **Примечание**  Если при попытке выполнить это действие появляется сообщение об ошибке 25109, вы неправильно настроили разрешения, необходимые для установки базы данных. Подробные сведения о настройке необходимых разрешений SQL можно найти в разделе <https://go.microsoft.com/fwlink/?LinkId=132144> .

     

9.  На экране **сервер службы каталогов** введите имя домена и учетные данные, которые будут использоваться серверами Application Virtualization и веб-службой управления, чтобы получить доступ к контроллеру домена, сохраните эти данные, а затем нажмите кнопку **Далее**.

    **Примечание**  При установке по умолчанию будет использоваться домен текущего компьютера.

     

10. На странице " **Группа администраторов** " введите имя группы, обладающей правами администратора, сохраните эти данные, а затем нажмите кнопку **Далее**.

    **Примечание**  Вы также можете ввести несколько первых символов имени группы, у которой есть права на администрирование, нажмите кнопку **Далее**, а затем на экране **Выбор группы администраторов** выберите группу из полученного списка. Затем сохраните эти данные и нажмите кнопку **Далее**.

     

11. На странице " **Группа поставщика по умолчанию** " введите полное имя группы, которая будет управлять доступом к приложениям, сохраните эти данные, а затем нажмите кнопку **Далее**.

    **Примечание**  Вы также можете ввести первые несколько символов имени группы, которая будет управлять доступом к приложениям, нажмите кнопку **Далее**, а затем на экране **Выбор группы поставщика по умолчанию** выберите группу в списке. Затем сохраните эти данные и нажмите кнопку **Далее**.

     

12. На странице **завершения работы мастера установки** нажмите кнопку **Готово**, чтобы закрыть окно мастера.

    **Важно!**  Для завершения установки может потребоваться несколько минут. Сообщение о состоянии будет мигать над областью уведомлений на рабочем столе Windows, указывая, успешно ли была выполнена установка.

     

## Статьи по теме


[Установка серверов и компонентов системы](how-to-install-the-servers-and-system-components.md)

 

 




