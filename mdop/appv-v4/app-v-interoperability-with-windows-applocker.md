---
title: Совместимость App-V с Windows AppLocker
description: Совместимость App-V с Windows AppLocker
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822312"
---
# Совместимость App-V с Windows AppLocker


Версия 4,5 с пакетом обновления 1 (SP1) для клиента Microsoft Application Virtualization (App-V) поддерживает функцию AppLocker операционной системы Windows 7. Функция AppLocker позволяет ИТ – администраторам указывать, какие приложения запрещено запускать на компьютерах. В этом документе описано, как настроить правила AppLocker для работы с виртуальной средой App-V и виртуализированными приложениями.

**Примечание**  Прежде чем настраивать правила Windows AppLocker для виртуальных приложений, сначала необходимо включить Windows AppLocker. Дополнительные сведения о включении Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .

 

## Настройка правил Windows AppLocker для виртуальных приложений


Локальные администраторы могут создавать правила Windows AppLocker, которые ограничивают выполнение исполняемых файлов программ (exe), файлов установщика Windows (MSI-и MSP-файлов) и сценариев (файлы. PS,. bat,. cmd,. vbs и. js). Администратор делает это с помощью эталонного компьютера, на котором установлен клиент App-V, и всех необходимых виртуальных приложений, передаваемым в клиентский кэш. Для создания правил администратор использует раздел Windows AppLocker локальной политики безопасности Microsoft Management Console (MMC) на компьютере-образце.

При просмотре пути к каталогу или определенному файлу, для которого вы хотите создать правило, вы можете получить доступ к диску App-V, указав путь к скрытому общему доступу. Например, вы можете перейти на \\\\localhost\\Q $, где диск App-V — это диск Q. Тем не менее, чтобы создать правило, необходимо изменить путь, чтобы удалить ссылку на \\\\localhost\\Q $ и использовать Q:\\. Чтобы получить доступ к файлам приложения, необходимо запускать каждое приложение на компьютере-образце, а для перехода на \\\\localhost\\Q $ требуются права администратора.

 

 





