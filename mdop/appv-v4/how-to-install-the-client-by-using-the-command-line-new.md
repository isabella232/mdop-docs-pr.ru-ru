---
title: Установка клиента с помощью командной строки
description: Установка клиента с помощью командной строки
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817322"
---
# Установка клиента с помощью командной строки


В этом разделе приведены процедуры для установки клиентского клиента Application Virtualization (App-V) или клиента App-V для служб удаленных рабочих столов (ранее — служб терминалов) с помощью либо setup.exe, либо setup.msi. Для запуска программы установки необходимо иметь права администратора.

Вы можете использовать дополнительные параметры командной строки, чтобы применить определенные параметры конфигурации к клиенту App-V во время установки. Дополнительные сведения об использовании параметров можно найти в разделе [Параметры командной строки установщика клиента Application Virtualization](application-virtualization-client-installer-command-line-parameters.md). Если вы применили параметры реестра на компьютере перед развертыванием клиента (например, с помощью групповой политики), эти параметры сохраняются, а все дополнительные параметры командной строки применяются. Значения параметров командной строки будут заменять все существующие значения для этого параметра.

**Примечание**  При установке клиента App-V на использование кэша, доступного только для чтения (например, с реализацией сервера VDI), необходимо установить для параметра *AUTOLOADTARGET* значение None, чтобы клиент не мог обновить приложения, если кэш доступен только для чтения.

 

Дополнительные сведения об установке этих значений параметров после установки можно найти в разделе [Настройка параметров реестра клиента App-v с помощью командной строки](https://go.microsoft.com/fwlink/?LinkId=169355) ( https://go.microsoft.com/fwlink/?LinkId=169355) в руководстве по работе с Application Virtualization (App-v).

**Примечание**  Если параметры конфигурации на компьютере пользователя зависят от пути установки клиента, обратите внимание на то, что клиент Application Virtualization (App-V) 4.5 копирует установочные файлы в папку, отличную от предыдущих версий. По умолчанию новый экземпляр клиента App-V 4.5 копирует установочные файлы в папку клиента Application Virtualization \\Program Files\\Microsoft. Если на компьютере уже установлена более ранняя версия клиента, при запуске установщика клиента App-V 4,5 будет выполнено обновление существующего клиента с помощью существующей папки установки.

 

\ [Значение маркера шаблона \]

**Примечание**  Для App-V версии 4.6 и более поздних версий при установке клиента App-V SFTLDR.DLL копируется в каталог Windows\\system32. Если клиент App-V установлен на 64-разрядной системе, SFTLDR\_WOW64.DLL копируется в каталог Windows\\SysWOW64.

 

\ [Значение маркера шаблона \]

## В этом разделе


В следующих разделах описано, как установить клиентское приложение Application Virtualization (App-V) или клиент App-V для служб удаленных рабочих столов (ранее — службы терминалов), используя либо setup.exe, либо setup.msi.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[Установка клиента App-V с помощью Setup.exe](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
В этой статье приведены пошаговые инструкции по установке клиента App-V с помощью программы setup.exe.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[Установка клиента App-V с помощью Setup.msi](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
В этой статье приведены пошаговые инструкции по установке любого программного обеспечения, а также клиента App-V с помощью программы setup.msi.

## Статьи по теме


[Параметры командной строки установщика клиента Application Virtualization](application-virtualization-client-installer-command-line-parameters.md)

[Установка клиента Application Virtualization Client вручную](how-to-manually-install-the-application-virtualization-client.md)

[Публикация виртуального приложения на клиенте](how-to-publish-a-virtual-application-on-the-client.md)

[Удаление клиента App-V](how-to-uninstall-the-app-v-client.md)

 

 





