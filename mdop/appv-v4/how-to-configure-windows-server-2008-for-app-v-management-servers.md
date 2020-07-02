---
title: Настройка Windows Server 2008 для серверов App-V Management Server
description: Настройка Windows Server 2008 для серверов App-V Management Server
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817722"
---
# Настройка Windows Server 2008 для серверов App-V Management Server


Сервер Windows Server 2008, на котором вы установили веб-службу Microsoft Application Virtualization (App-V) Management, требует наличия служб IIS для установки в качестве роли на сервере. Чтобы настроить Windows Server 2008 для поддержки установки App-VServer, выполните указанные ниже действия.

**Установка служб IIS на компьютере с Windows Server2008**

1.  На компьютере с Windows Server2008 нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Администрирование**, а затем — **Диспетчер** серверов. В диспетчере серверов щелкните правой кнопкой мыши узел " **роли** " и выберите команду **Добавить роли** , чтобы запустить **Мастер добавления ролей**.

2.  В **мастере добавления ролей**на странице **Выбор ролей сервера** выберите **веб-сервер (IIS)**. При появлении соответствующего запроса нажмите кнопку **Добавить необходимые функции** , чтобы добавить зависимые компоненты.

3.  На странице **Выбор ролей сервера** нажмите кнопку **Далее**, а затем еще раз нажмите кнопку **Далее** .

4.  В **мастере добавления ролей**на странице " **Выбор служб ролей** " выполните указанные ниже действия.

    1.  В разделе **Разработка приложений**выберите **ASP.NET** и при появлении соответствующего запроса нажмите кнопку **Добавить необходимые службы** ролей, чтобы добавить службы и компоненты зависимых ролей.

    2.  В разделе **Безопасность**выберите **Проверка подлинности Windows**.

    3.  В узле **средства управления** выберите **сценарии и средства управления IIS**. Убедитесь, что в разделе **Совместимость управления IIS6**установлены флажки **Совместимость с метабазой IIS6** и **IIS6** , а затем нажмите кнопку **Далее**.

5.  На странице **Подтвердите выбор установки** нажмите кнопку **установить**, а затем завершите работу мастера.

6.  Нажмите кнопку **Закрыть** , чтобы закрыть окно **мастера добавления ролей**, а затем закройте Диспетчер серверов.

## Статьи по теме


[Требования при развертывании Application Virtualization](application-virtualization-deployment-requirements.md)

[Контрольные списки развертывания и обновления Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

 

 




