---
title: Развертывание приложения App-V 4,6 и клиента App-V 5,1 на том же компьютере
description: Развертывание приложения App-V 4,6 и клиента App-V 5,1 на том же компьютере
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814173"
---
# Развертывание приложения App-V 4,6 и клиента App-V 5,1 на том же компьютере

**Примечание.** Приложение App-V 4,6 завершило работу базовой поддержки.

Используйте следующие сведения для установки клиента Microsoft Application Virtualization (App-V) 5,1 (предпочтительный с последними пакетами обновления и исправлениями), а также клиента App-v 4.6 SP2 или клиента App-V 4.6 S3 на том же компьютере. Поддерживаемые версии, требования и другие сведения о планировании можно найти в разделе [Планирование миграции с предыдущей версии App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).

**Развертывание клиента App-V 5,1 и Client App-V 4,6 на одном компьютере**

1.  Установите следующую версию клиента App-V на компьютере под управлением App-V 4,6.

    -   [Microsoft Application Virtualization 4,6 с пакетом обновления 3 (SP3)](https://www.microsoft.com/download/details.aspx?id=41187)

2.  Установите клиент App-V 5,1 на компьютере, на котором запущена версия App-V 4,6 SP3. Для достижения наилучших результатов мы рекомендуем установить все доступные обновления для клиента App-V 5,1.

3.  Преобразуйте и повторно поочередность пакетов.

    -   Чтобы преобразовать пакеты, используйте конвертер пакета App-V 5,1 и преобразуйте необходимые пакеты в формат файлов App-V 5,1 (**. AppV**).

    -   Для повторной нумерации пакетов рекомендуется использовать последнюю версию секвенсора для наилучших результатов.

    Дополнительные сведения о публикации пакетов можно найти в разделе [Публикация пакета с помощью консоли управления](how-to-publish-a-package-by-using-the-management-console-51.md).

4.  Развертывание пакетов на клиентских компьютерах.

5.  При необходимости преобразуйте точки расширения. Подробнее:

    -   [Перенос точек расширения из пакета App-V 4.6 в преобразованный пакет App-V 5.1 для всех пользователей на указанном компьютере](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [Перенос точек расширения из пакета App-V 4.6 в App-V 5.1 для конкретного пользователя](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [Преобразование пакета, созданного в предыдущей версии App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  Убедитесь, что пакеты приложения-V 5,1 выполнены успешно, а затем удалите пакеты 4,6. Для проверки состояния пользователя клиентских компьютеров рекомендуется использовать [виртуализацию взаимодействия с пользователем](https://technet.microsoft.com/library/dn458947.aspx) или другое средство управления средой пользователя.

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Планирование миграции из предыдущей версии App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[Развертывание Sequencer и клиента App-V 5.1](deploying-the-app-v-51-sequencer-and-client.md)

 

 





