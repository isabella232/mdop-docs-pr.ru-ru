---
title: Использование тестовой среды
description: Использование тестовой среды
author: dansimp
ms.assetid: 86295084-b39e-4040-bb3f-15c3c1e99b1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1264d9fe6f922a7e61bcd069581c7bd5e39b7787
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818239"
---
# Использование тестовой среды


Если вы используете проверочное подразделение (OU) для тестирования объектов групповой политики (GPO) перед развертыванием в рабочей среде, для доступа к тестовому подразделению необходимы соответствующие разрешения. Использование тестового подразделений является необязательным.

**Использование тестового подразделения**

1.  Несмотря на то, что объект групповой политики извлечен для редактирования, в **консоли управления групповыми политиками**нажмите кнопку **объекты групповой политики** в лесу и домене, в которых вы управляете объектами GPO.

2.  Щелкните извлеченную копию объекта групповой политики, который нужно протестировать. Имя будет начинаться с **\ [извлечено \]**. (Если он не указан в списке, нажмите кнопку **действие**, а затем — **Обновить**. Сортировка имен в алфавитном порядке и **\ [извлечено \]** GPO обычно отображаются в верхней части списка.)

3.  Перетащите GPO в проверочное подразделение.

4.  Нажмите кнопку **ОК** в диалоговом окне с вопросом, нужно ли создать ссылку на объект групповой политики в тестовом подразделении.

### Дополнительные рекомендации

-   После того как тестирование будет завершено, при возврате объекта групповой политики автоматически удаляется ссылка на извлеченную копию объекта групповой политики.

### Дополнительные ссылки

-   [Изменение объекта групповой политики](editing-a-gpo-agpm30ops.md)

 

 




