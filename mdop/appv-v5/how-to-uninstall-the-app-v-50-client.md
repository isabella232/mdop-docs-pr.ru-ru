---
title: Удаление клиента App-V 5.0
description: Удаление клиента App-V 5.0
author: dansimp
ms.assetid: 7566fb19-8d52-439a-be42-e004d95fed6f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3794707b9342009b14eca37882c20873c38e522e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813661"
---
# Удаление клиента App-V 5.0


Чтобы удалить клиент App-V 5,0 с компьютера, выполните описанные ниже действия. При удалении клиента App-V 5,0 все пакеты, опубликованные на компьютере, на котором запущен клиент, также удаляются. Если операция удаления не завершится, нужно будет повторно опубликовать пакеты на компьютере с клиентом App-V 5,0.

**Важно.**  
Перед выполнением процедуры удаления необходимо убедиться, что клиентская служба App-V 5,0 запущена.



**Удаление клиента App-V 5,0**

1.  На панели управления дважды щелкните пункт **программы**  /  ,**Удаление программы**, а затем дважды щелкните **клиент Microsoft Application Virtualization**.

2.  В появившемся диалоговом окне нажмите кнопку **Да** , чтобы продолжить процесс удаления.

    **Важно.**  
    Процесс удаления не может быть отменен или прерван.



3.  Индикатор выполнения показывает оставшееся время. После завершения этого действия необходимо перезагрузить компьютер, чтобы все связанные с ним драйверы были остановлены для завершения процесса удаления.

    **Примечание.**  
    Вы также можете использовать командную строку для удаления клиента App-V 5,0 со следующим переключателем: **/uninstall**.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Статьи по теме


[Развертывание App-V 5.0](deploying-app-v-50.md)









