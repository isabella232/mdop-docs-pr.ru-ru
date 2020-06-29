---
title: Изменение размера кэша и букв дисков
description: Изменение размера кэша и букв дисков
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818039"
---
# Изменение размера кэша и букв дисков


Изменить размер кэша и букву диска можно непосредственно из узла **Application Virtualization** в консоли управления клиентом Application Virtualization.

**Примечание.**  
После установки размера кэша его нельзя уменьшить.



**Изменение размера кэша**

1.  Щелкните правой кнопкой мыши узел **Application Virtualization** и во всплывающем меню выберите пункт **свойства** .

2.  Выберите вкладку **Файловая система** в диалоговом окне **свойства** . В разделе **Параметры конфигурации кэша клиента** выберите один из указанных ниже переключателей, чтобы выбрать способ управления пространством кэша.

    **Важно.**  
    Если вы выберете параметр " **использовать порог свободного места на диске** ", введенное значение будет указывать на общий размер кэша, а не на указанный вами порог свободного места на диске. Если вы хотите вернуться к использованию параметра **использовать максимальный размер кэша** , необходимо указать большее значение, чем существующий размер кэша. В противном случае появится сообщение об ошибке "новый размер должен быть больше существующего кэша".



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. Нажмите кнопку **ОК** или **Применить** , чтобы изменить параметр.

**Изменение обозначения диска**

1.  Щелкните правой кнопкой мыши узел **Application Virtualization** и во всплывающем меню выберите пункт **свойства** .

2.  На вкладке **Файловая система** в диалоговом окне **свойства** в поле **диск для использования** выберите нужную букву диска из раскрывающегося списка доступных букв дисков. Этот параметр вступает в силу после перезагрузки компьютера.

3.  Нажмите кнопку **ОК** или **Применить** , чтобы изменить параметр.

## Статьи по теме


[Настройка клиента в консоли управления клиентом Application Virtualization](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)









