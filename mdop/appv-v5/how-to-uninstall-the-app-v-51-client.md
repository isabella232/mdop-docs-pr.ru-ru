---
title: Удаление клиента App-V 5.1
description: Удаление клиента App-V 5.1
author: dansimp
ms.assetid: 21f2d946-fc9f-4cd3-899b-ac52b3fbc306
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9338bef6b8a3123f9b8f49036427121987e7aa9f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813656"
---
# Удаление клиента App-V 5.1


Чтобы удалить клиент Microsoft Application Virtualization (App-V) 5,1 с компьютера, выполните описанные ниже действия. При удалении клиента App-V 5,1 все пакеты, опубликованные на компьютере, на котором запущен клиент, также удаляются. Если операция удаления не завершится, нужно будет повторно опубликовать пакеты на компьютере с клиентом App-V 5,1.

**Важно.**  
Перед выполнением процедуры удаления необходимо убедиться, что клиентская служба App-V 5,1 запущена.



**Удаление клиента App-V 5,1**

1.  На панели управления дважды щелкните пункт **программы**  /  ,**Удаление программы**, а затем дважды щелкните **клиент Microsoft Application Virtualization**.

2.  В появившемся диалоговом окне нажмите кнопку **Да** , чтобы продолжить процесс удаления.

    **Важно.**  
    Процесс удаления не может быть отменен или прерван.



3.  Индикатор выполнения показывает оставшееся время. После завершения этого действия необходимо перезагрузить компьютер, чтобы все связанные с ним драйверы были остановлены для завершения процесса удаления.

    **Примечание.**  
    Вы также можете использовать командную строку для удаления клиента App-V 5,1 со следующим переключателем: **/uninstall**.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Статьи по теме


[Развертывание App-V 5.1](deploying-app-v-51.md)









