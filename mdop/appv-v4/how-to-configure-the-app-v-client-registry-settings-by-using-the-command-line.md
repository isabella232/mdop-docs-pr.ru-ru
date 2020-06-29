---
title: Настройка параметров реестра клиента App-V с помощью командной строки
description: Настройка параметров реестра клиента App-V с помощью командной строки
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817899"
---
# Настройка параметров реестра клиента App-V с помощью командной строки


После того как клиент Application Virtualization (App-V) развернут и настроен во время установки с помощью командной строки, может потребоваться изменить один или несколько параметров конфигурации клиента. Для этого нужно изменить соответствующие разделы реестра, выполнив одно из указанных ниже действий.

-   Использование редактора реестра непосредственно

-   Использование REG-файла

-   Использование языка сценариев, например VBScript или Windows PowerShell

Кроме того, существует шаблон ADM, который можно использовать. Дополнительные сведения о шаблоне ADM можно найти в разделе <https://go.microsoft.com/fwlink/?LinkId=121835> .

**Внимание!**  Будьте внимательны при редактировании реестра, так как ошибки могут привести к неработоспособности компьютера. Не забудьте соблюдать стандартные деловые рекомендации, связанные с изменениями в реестре. Тщательно протестируйте все предлагаемые изменения в тестовой среде, прежде чем развертывать их на реальных компьютерах.

 

## В этом разделе


**Важно!**  В 64-разрядных компьютерах разделы и значения, описанные в следующих разделах, находятся в разделе HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[Сброс параметров кэша файловой системы](how-to-reset-the-filesystem-cache.md)  
Предоставляет сведения, необходимые для сброса кэша файловой системы.

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[Изменение размера кэша файловой системы](how-to-change-the-size-of-the-filesystem-cache.md)  
В этой статье объясняется, как можно изменить размер кэша.

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[Использование функции управления размером кэша](how-to-use-the-cache-space-management-feature.md)  
В этой статье описано, как настроить функцию управления пространством кэша.

<a href="" id="how-to-configure-the-client-log-file"></a>[Настройка файла журнала клиента](how-to-configure-the-client-log-file.md)  
В этой статье описаны различные значения разделов реестра, которые контролируют файл журнала клиента и как его можно изменить.

<a href="" id="how-to-configure-user-permissions"></a>[Настройка разрешений для пользователей](how-to-configure-user-permissions.md)  
Определяет раздел реестра, управляющий разрешениями пользователя, и приводятся примеры изменения некоторых разрешений.

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[Настройка клиента для получения пакетов приложений](how-to-configure-the-client-for-application-package-retrieval.md)  
В этой статье объясняется, как настроить клиент для извлечения содержимого, значков и сопоставлений типов файлов из разных источников, а также несколько примеров правильного формата пути.

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[Настройка клиента для включения режима изолированной работы](how-to-configure-the-client-for-disconnected-operation-mode.md)  
Сведения о том, как настроить различные параметры, связанные с режимом отключенных операций.

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[Настройка работы ярлыков и сопоставлений типов файлов](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
В этой статье описаны значения разделов реестра, управляющие сочетаниями клавиш и сопоставлением типов файлов в клиенте App-V, а также сведения о том, как их настроить.

## Статьи по теме


[Клиент Application Virtualization](application-virtualization-client.md)

 

 





