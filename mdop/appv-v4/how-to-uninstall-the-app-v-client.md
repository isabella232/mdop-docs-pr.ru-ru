---
title: Удаление клиента App-V
description: Удаление клиента App-V
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816522"
---
# Удаление клиента App-V


Выполните описанные ниже действия, чтобы удалить клиент Application Virtualization с компьютера.

**Удаление клиентского компьютера Application Virtualization**

1.  На панели управления дважды щелкните элемент **Установка и удаление программ** (или в Windows Vista, **программы и компоненты**), а затем дважды щелкните **клиентское приложение Microsoft Application Virtualization для настольных систем**.

2.  В появившемся диалоговом окне нажмите кнопку **Да** , чтобы продолжить процесс удаления.

    **Важно!**  Процесс удаления не может быть отменен или прерван.

     

3.  Когда появится сообщение о том, что приложение клиентской панели Microsoft Application Virtualization должно быть закрыто, прежде чем продолжить работу, щелкните правой кнопкой мыши значок App-V в области уведомлений и выберите команду **выход** , чтобы закрыть приложение. Затем нажмите кнопку **"повторить"** , чтобы продолжить процесс удаления.

    **Важно!**  Может появиться сообщение о том, что одно или несколько виртуальных приложений используются. Закройте все открытые приложения и сохраните данные, прежде чем продолжить. Затем нажмите кнопку **ОК** , чтобы продолжить процесс удаления.

     

4.  Индикатор выполнения показывает оставшееся время. После завершения этого действия необходимо перезагрузить компьютер, чтобы все связанные с ним драйверы были остановлены для завершения процесса удаления.

    **Примечание**  После завершения процесса удаления остались следующие разделы реестра:

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard "клиент" = DWORD: 00000000

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey

     

## Статьи по теме


[Установка клиента с помощью командной строки](how-to-install-the-client-by-using-the-command-line-new.md)

[Установка клиента Application Virtualization Client вручную](how-to-manually-install-the-application-virtualization-client.md)

[Публикация виртуального приложения на клиенте](how-to-publish-a-virtual-application-on-the-client.md)

 

 





