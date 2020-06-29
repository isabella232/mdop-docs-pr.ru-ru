---
title: Восстановление диска в режиме восстановления
description: Восстановление диска в режиме восстановления
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812952"
---
# Восстановление диска в режиме восстановления


Администрирование и мониторинг Microsoft BitLocker (MBAM) включает возможности восстановления зашифрованных дисков. Эти функции гарантируют сбор и хранение данных и доступность средств, необходимых для доступа к тому, защищенному с помощью BitLocker, при появлении тома в режиме восстановления. Защищенный BitLocker том переходит в режим восстановления, если ПИН-код или пароль утеряны или утрачены, или если микросхема доверенного платформенного модуля (TPM) обнаруживает изменение BIOS или файлов загрузки компьютера.

Используйте эту процедуру, чтобы получить доступ к централизованной системе данных восстановления ключей, которая может предоставить пароль восстановления при предоставлении идентификатора пароля восстановления и соответствующего идентификатора пользователя.

**Важно!**  MBAM создает ключи восстановления с одним использованием. В рамках этого ограничения ключ восстановления можно использовать только один раз, и он больше не является действительным. Один из способов использования пароля восстановления автоматически применяется к дискам операционной системы и жестким дискам. На съемных носителях используется единая функция, когда диск удаляется, а затем снова вставляется и разблокируется на компьютере, на котором активированы параметры групповой политики для управления съемными дисками.

 

**Восстановление диска в режиме восстановления**

1.  Откройте веб-сайт MBAM.

2.  В области навигации нажмите кнопку **Восстановление диска**. Откроется веб-страница **зашифрованного диска** с правом восстановления.

3.  Чтобы получить список возможных ключей восстановления, введите имя пользователя и домен для входа в Windows и первые восемь цифр идентификатора ключа восстановления. Кроме того, можно ввести весь код ключа восстановления, чтобы получить точный ключ восстановления. Выберите один из предопределенных параметров из раскрывающегося списка **Причина для разблокировки диска** и нажмите кнопку **Отправить**.

    **Примечание**  Если вы являетесь пользователем расширенной службы поддержки MBAM, то не требуется домен пользователя и идентификатор пользователя.

     

4.  MBAM возвращает следующее:

    1.  Сообщение об ошибке, если соответствующий пароль для восстановления не найден

    2.  Несколько возможных совпадений, если у пользователя есть несколько совпадающих паролей восстановления

    3.  Пароль восстановления и пакет восстановления для отправленного пользователя

        **Примечание**  Если вы восстанавливаете поврежденный диск, параметр пакета восстановления предоставляет BitLocker важные сведения, необходимые для восстановления.

         

5.  После извлечения пароля восстановления и пакета восстановления отображается пароль восстановления. Чтобы скопировать пароль, нажмите кнопку **Копировать раздел**, а затем вставьте пароль восстановления в сообщение электронной почты или другой текстовый файл для временного хранилища. Чтобы сохранить пароль восстановления в файле, нажмите кнопку **сохранить**.

6.  Когда пользователь вводит пароль восстановления в систему или использует пакет восстановления, диск разблокируется.

## Статьи по теме


[Управление BitLocker с помощью MBAM](performing-bitlocker-management-with-mbam.md)

 

 




