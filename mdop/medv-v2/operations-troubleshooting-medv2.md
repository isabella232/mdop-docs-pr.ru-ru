---
title: Устранение неполадок в операциях
description: Устранение неполадок в операциях
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812741"
---
# Устранение неполадок в операциях


Этот раздел содержит сведения, которые можно использовать для устранения общих проблем, связанных с рабочим столом в Microsoft Enterprise Virtualization (MED-V) 2,0.

## Устранение неполадок, связанных с работой в MED-V


Ниже перечислены некоторые проблемы, с которыми пользователи могут столкнуться при использовании MED-V и решений для устранения этих проблем.

**Не удается перенаправление документации**. Как правило, эта проблема возникает, если папка Мои документы конечного пользователя указывает на расположение в сети. Windows не поддерживает создание общего доступа из другой общей папки. Когда диск или папка перенаправляется на гость, RDP\\Windows Virtual PC создает для нее общий доступ. Таким образом, если папка Мои документы на узле уже указывает на общий доступ, RDP\\Windows Virtual PC не может создать общий доступ к общему доступу.

Другая возможная причина этой проблемы заключается в том, что учетные данные, необходимые для подключения к сетевому ресурсу, могут отличаться от учетных данных пользователя домена. MED-V может обнаружить, что документы перенаправлены на узел, отправить эту информацию на гость и попытаться восстановить подключение к сетевому ресурсу. Если учетная запись пользователя не проходит проверку подлинности, при попытке выполнить проверку подлинности в MED-V может возникнуть ошибка.

**Решение**

Чтобы устранить эту проблему, попробуйте выполнить одно из указанных ниже действий.

-   Настройте корневой каталог пользователя в Active Directory. После этого гость и узел должны подключаться к тому же сетевому ресурсу.

-   Вместо того чтобы перенаправлять папку "Мои документы" в путь UNC, сопоставьте ей букву диска (на узле сопоставьте диск, который указывает на ресурс сети). После этого в папке Мои документы можно настроить использование буквы диска вместо пути в формате UNC. Гость перейдет к тому же подключенному диску, как и предполагалось.

-   Создайте в гостевой системе сценарий, который перенаправляет папку "Мои документы" сетевому ресурсу, и при необходимости предоставляет дополнительные учетные данные.

**Перенаправление URL-адреса не выполняется**. URL-адрес, указанный для переадресации с узла на гость, не перенаправляется надлежащим образом или возвращает сообщение об ошибке, указывающее на то, что веб-сайт не существует.

**Решение**

Эта ошибка может возникать, если в сведениях о переадресации URL-адреса есть ошибки или неправильное использование знаков, например звездочки (\ *). Проверьте значение реестра для перенаправления URL-адреса и исправьте ошибки.

Раздел реестра называется `RedirectUrls` и обычно находится по адресу:

Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

**Значок на панели задач**. По умолчанию, значок, который отображается на панели задач конечного пользователя для опубликованных приложений и перенаправленные URL-адреса, — это значок для Windows Virtual PC. Если конечный пользователь не знает это поведение по умолчанию, он может стать запутанным при просмотре панели задач, чтобы найти их приложение.

**Решение**

Единственный способ избежать этого поведения по умолчанию — изменить параметры пользователя для свойств панели задач, как описано ниже.

1.  Щелкните панель задач правой кнопкой мыши и выберите пункт **Свойства**.

2.  На **панели задач и** в диалоговом окне Свойства: меню "Пуск" щелкните вкладку на **панели задач** .

3.  В раскрывающемся списке **кнопок на панели задач** выберите параметр **не объединять**.

4.  Нажмите кнопку **ОК**.

Отображаются ожидаемые значки опубликованных приложений и перенаправленные URL-адреса.

**Предупреждение, выданное при попытке входа в систему с помощью второй учетной записи пользователя или виртуальной машины**. Предупреждающее сообщение выдается, когда второй пользователь входит в рабочую область MED-V, когда первый пользователь по-прежнему работает под управлением MED-V. Предупреждение также выводится, если при использовании виртуальной машины была запущена система MED-V, например, если виртуальная машина была запущена с помощью Windows Virtual PC в меню " **Пуск** ". Когда пользователь принимает предупреждающее сообщение, MED-V завершает работу.

**Решение**

Конечный пользователь должен проверить, что все остальные пользователи вошли в систему, прежде чем пытаться войти в систему. Это гарантирует, что другие экземпляры MED-V не запущены, и что Virtual PC не отвечает за контроль виртуальных машин в Windows.

**Звуковой сигнал, который слышен при первом запуске программы установки**. Иногда звуковые сигналы слышны, а MED-V запускается при первом запуске программы установки. Это может привести к путанице с конечным пользователем. Звуковые сигналы исходят с виртуальной машины при выполнении определенных действий, например при завершении работы.

**Решение**

Вы можете остановить службу звукового сигнала, указав команду "net stop Beep" в начале каждой последовательности запуска виртуальных машин. Кроме того, вы можете отключить звуковую службу, указав команду "SC config Beep Start = Disabled". Эти команды можно задать перед запечатыванием изображения или в составе программы Sysprep.

**Несколько сетевых подключений, созданных для рабочих областей MED-V в режиме моста**. Если при первом запуске программы установки создается рабочая область MED-V, настроенная для режима NAT, она создает только одно сетевое подключение в Windows Virtual PC. Тем не менее, если при первой настройке будет создана Рабочая область MED-V, настроенная для режима моста, создается отдельное сетевое подключение для каждого сетевого адаптера, установленного на компьютере, так как MED-V не может определить, какой именно сетевой адаптер является активным. Кроме того, это гарантирует, что для проводных и беспроводных подключений для перемещаемых пользователей всегда будет использоваться сетевой адаптер.

**Решение**

Нет.

**Приложение MED-V не отвечает на запросы слишком долго при закрытии**. В некоторых случаях приложение MED-V перестает отвечать на запросы при попытке закрыть его.

**Решение**

Вы можете указать продолжительность времени, в течение которого MED-V ждет закрытия приложений, не отвечающих на запросы, установив раздел реестра WaitToKillAppTimeout на гостевой виртуальной машине. Дополнительные сведения о том, [как увеличить время завершения работы программы, чтобы правильно завершить процесс в Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) ( https://go.microsoft.com/fwlink/?LinkId=206819) .

**Переименование опубликованного ярлыка приложения на гостевой виртуальной машине не изменяет опубликованное имя на узле**. При публикации приложения с помощью создания ярлыка и переименования ярлыка на гостевой виртуальной машине имя исходного приложения сохраняется в меню " **Пуск** " узла. Программа продолжает работать должным образом, но программа всегда сохранит исходное имя.

**Решение**

Нет. Это известное поведение Virtual PC для Windows.

**При перемещении ярлыка на гостевой виртуальной машине это расположение не обновляется в меню "Пуск" главного компьютера**. Сочетания клавиш для работы с приложением MED-V, опубликованные в **главном меню компьютера** , находятся в реестре. Если переместить ярлык приложения во вложенную папку, реестр не будет обновляться, чтобы отразить изменения.

**Решение**

Чтобы изменить расположение сочетания клавиш для приложения MED-V, выполните указанные ниже действия.

1.  После запуска MED-V откройте проводник Windows на гостевой виртуальной машине MED-V.

2.  Перейдите к каталогу "%ALLUSERSPROFILE%\\Start Menu\\Programs".

3.  Перемещение ярлыков приложения из папок StartMenu или программы.

4.  После около 30 секунд убедитесь, что ярлыки удаляются из меню **Пуск** главного компьютера.

5.  Переместите ярлыки приложений обратно в новые папки программы в каталоге Start Menu\\Programs.

6.  После примерно 30 секунд убедитесь в том, что ярлыки обновлены в главном **меню главного** компьютера.

**Опубликованные приложения могут**исключаться из периода простоя. В некоторых случаях опубликованные приложения будут иметь время ожидания, если они не простаивают в течение некоторого времени. Это происходит только в том случае, если включена безопасность IPsec и в режиме NAT настроена Рабочая область MED-V. Такая ситуация не возникает при работе в режиме моста.

**Решение**

Отключите IPsec при запуске рабочей области MED-V в режиме NAT.

**Закрепление опубликованного приложения на панели задач обходит MED-V**. Если пользователь зафиксирует опубликованное приложение на панели задач, а затем закроет приложение, то MED-V обходится при следующем открытии приложения из значка на панели задач. Вместо этого приложение откроется прямо в окне VMSAL.

**Решение**

Не закрепите приложения, опубликованные в MED-V, на панели задач.

## Статьи по теме


[Рекомендации по обеспечению безопасности операций MED-V](security-best-practices-for-med-v-operations.md)

[Устранение неполадок при развертывании](deployment-troubleshooting.md)

 

 




