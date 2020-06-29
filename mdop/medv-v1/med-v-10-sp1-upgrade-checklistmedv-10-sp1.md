---
title: Контрольный список обновления MED-V 1.0 с пакетом обновления 1 (SP1)
description: Контрольный список обновления MED-V 1.0 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827269"
---
# Контрольный список обновления MED-V 1.0 с пакетом обновления 1 (SP1)


Чтобы обновить версию Microsoft Enterprise Virtualization (MED-V) 1.0 до MED-V 1.0 Service Pack1 (SP1), необходимо обновить клиент. При необходимости можно обновить сервер.

## Обновление сервера


**Обновление сервера MED-V 1.0 до версии MED-V 1.0 SP1**

1.  Создавайте резервные копии следующих файлов, расположенных в каталоге * &lt; installDir &gt; /Servers/ConfigurationServer* :

    -   OrganizationalPolicy.XML

    -   ClientPolicy.XML

    -   WorkspaceKeys.XML

2.  Создавайте резервные копии файлов * &lt; installDir &gt; /servers/ServerSettings.xml* .

3.  Удалите сервер MED-V 1.0.

4.  Установите сервер MED-V 1.0 с пакетом обновления 1 (SP1).

5.  Восстановите резервные копии файлов в соответствующих каталогах.

6.  Перезапустите службу сервера MED-V.

**Примечание**  Если конфигурация сервера была изменена по умолчанию, файлы могут храниться в другом расположении.

 

## Обновление клиента


Чтобы обновить клиент MED-V 1.0 до версии MED-v 1.0 с пакетом обновления 1 (SP1), установите файл MSP в клиенте MED-V 1.0. Клиент и MED-V обновляются автоматически.

 

 





