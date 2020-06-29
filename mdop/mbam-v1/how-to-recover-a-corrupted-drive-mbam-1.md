---
title: Восстановление поврежденного диска
description: Восстановление поврежденного диска
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812944"
---
# Восстановление поврежденного диска


Чтобы восстановить поврежденный диск, защищенный BitLocker, пользователь службы поддержки администрирования и мониторинга Microsoft BitLocker (MBAM) должен создать файл пакета ключей восстановления. Этот файл пакета можно скопировать на компьютер, на котором находится поврежденный диск, а затем использовать для восстановления диска. Чтобы сделать это, выполните указанные ниже действия.

**Восстановление поврежденного диска**

1.  Откройте веб-сайт администрирования MBAM.

2.  В области навигации выберите **Восстановление дисков** . Введите доменное имя пользователя и имя пользователя, причины разблокировки диска и ИД пароля для восстановления пользователя.

    **Примечание**  Если вы являетесь участником роли администраторов службы поддержки, вам не нужно вводить доменное имя пользователя или имя пользователя.

     

3.  Нажмите кнопку **Отправить**. Появится ключ восстановления.

4.  Нажмите кнопку **сохранить**, а затем выберите **пакет ключей восстановления**. Пакет ключа восстановления будет создан на вашем компьютере.

5.  Скопируйте пакет ключа восстановления на компьютер с поврежденным диском.

6.  Откройте командную строку с повышенными привилегиями. Для этого нажмите кнопку **Пуск** и введите `cmd` в поле **Найти программы и файлы** . В списке результатов поиска щелкните **cmd.exe** правой кнопкой мыши и выберите команду **Запуск от имени администратора**.

7.  В командной строке введите следующую команду:

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    **Примечание**  Для &lt; жесткого диска &gt; в команде Укажите доступное запоминающее устройство, которое имеет свободное место, равное или больше, чем данные на поврежденном диске. Данные поврежденного диска будут восстановлены и перемещены на указанный жесткий диск.

     

## Статьи по теме


[Управление BitLocker с помощью MBAM](performing-bitlocker-management-with-mbam.md)

 

 




