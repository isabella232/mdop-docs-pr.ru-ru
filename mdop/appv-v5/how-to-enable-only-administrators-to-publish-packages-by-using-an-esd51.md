---
title: Настройка публикации пакетов с помощью ESD только для администраторов
description: Настройка публикации пакетов с помощью ESD только для администраторов
author: dansimp
ms.assetid: bbc9fda2-fc09-4d72-8d9a-e83d2fcfe234
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22de7f62f540ceff274862c3f16b1f89d9459093
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814093"
---
# Настройка публикации пакетов с помощью ESD только для администраторов


Начиная с версии App-V 5,0 SP3, вы можете настроить клиент App-V таким образом, чтобы только администраторы (не конечные пользователи) могли публиковать и отменять публикацию пакетов. В более ранних версиях приложения App-V вы не смогли предотвратить выполнение этих задач конечными пользователями.

**Разрешение администраторам публиковать и отменять публикацию пакетов**

1.  Перейдите к следующему узлу объекта групповой политики:

    **Конфигурация &gt; компьютера Политики. &gt; административные &gt; шаблоны &gt; &gt; Публикация системы App-V**.

2.  Включите параметр **требуется опубликовать как** групповую политику администратора.

    Кроме того, чтобы настроить этот элемент с помощью PowerShell, Узнайте, [как управлять пакетами App-V 5,1, запущенными на отдельном компьютере, с помощью PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





