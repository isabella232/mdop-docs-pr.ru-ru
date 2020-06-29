---
title: Вкладка "Общие" свойств Application Virtualization
description: Вкладка "Общие" свойств Application Virtualization
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819689"
---
# Свойства Application Virtualization: вкладка "Общие"


Вкладка " **Общие** " в диалоговом окне " **свойства Application Virtualization** " используется для изменения параметров журнала и местоположений данных.

На этой вкладке есть указанные ниже элементы.

<a href="" id="log-level"></a>**Уровень ведения журнала**  
Выберите уровень из раскрывающегося списка. Уровень по умолчанию — **сведения**.

<a href="" id="reset-log"></a>**Сброс журнала**  
Нажмите эту кнопку, чтобы создать резервную копию текущего файла журнала и сразу же запустить новый файл.

<a href="" id="location"></a>**Location**  
Введите или перейдите в папку, в которой вы хотите сохранить файл журнала sftlog.txt. Ниже указаны расположения по умолчанию.

-   Для WindowsXP, Windows server2003 —*C:\\Documents и Settings\\All Users\\Application Data\\Microsoft\\Application виртуализация*

-   Для Windows Vista, Windows 7, Windows Server2008 —*клиент виртуализации C:\\ProgramData\\Microsoft\\Application*

<a href="" id="system-log-level"></a>**Уровень ведения журнала системы**  
Выберите уровень из раскрывающегося списка. Уровень по умолчанию — **предупреждение**.

**Примечание**  Параметр **уровня системного журнала** определяет уровень сообщений, отправляемых в журнал событий системы. Журнальные сообщения идентичны сообщениям, которые регистрируются в журнале событий клиента, но сохраняются в другом расположении, не имеющем ограничений на место в журнале событий клиента. Поскольку системный журнал событий не имеет ограничений на место, лучше подходит для случаев, когда требуется подробный журнал.

 

<a href="" id="global-data-directory"></a>**Глобальный каталог данных**  
Введите или перейдите в папку, в которой находится файл журнала. Ниже указаны расположения по умолчанию.

-   Для WindowsXP, Windows server2003 —*C:\\Documents и Settings\\All Users\\Application Data\\Microsoft\\Application виртуализация*

-   Для Windows Vista, Windows 7, Windows Server2008 —*клиент виртуализации C:\\ProgramData\\Microsoft\\Application*

<a href="" id="user-data-directory"></a>**Каталог данных пользователя**  
Введите путь к каталогу, в котором хранятся пользовательские данные, или перейдите к нему. Значением по умолчанию является% APPDATA%. Этот путь должен быть действительной переменной среды на клиентском компьютере.

## Статьи по теме


[Консоль управления клиентами: свойства Application Virtualization](client-management-console-application-virtualization-properties.md)

 

 





