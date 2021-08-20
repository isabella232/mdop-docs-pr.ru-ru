---
title: Развертывание приложения-V 4.6 и клиента App-V 5.0 на одном компьютере
description: Развертывание приложения-V 4.6 и клиента App-V 5.0 на одном компьютере
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.prod: w10
ms.openlocfilehash: f10f3d159c4724f3b486215b1169825bb029316d
ms.sourcegitcommit: 0132cd232b9c030820d95d91b71c4def0184400a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "11907232"
---
# <a name="how-to-deploy-the-app-v-46-and-the-app-v-50-client-on-the-same-computer"></a>Развертывание приложения-V 4.6 и клиента App-V 5.0 на одном компьютере

**Примечание:** App-V 4.6 вышел из основной поддержки. Далее предполагается, что клиент App-V 4.6 SP3 уже установлен.

Используйте следующую информацию для установки клиента App-V 5.0 (желательно, с последними пакетами и хот-фиксами) и клиента SP3 App-V 4.6 на том же компьютере. Для поддерживаемых версий, требований и других сведений о планировании см. в приложении [Planning for Migrating from a Previous Version of App-V.](planning-for-migrating-from-a-previous-version-of-app-v.md)

**Развертывание клиента App-V 5.0 и клиента App-V 4.6 на одном компьютере**

1.  Установите клиент App-V 5.0 SP3 на компьютере с версией App-V 4.6 клиента. Для наилучших результатов рекомендуется установить все доступные обновления для клиента App-V 5.0 SP3.

2.  Преобразование или переоформка пакетов постепенно.

    -   Чтобы преобразовать пакеты, используйте конвертер пакетов App-V 5.0 и конвертировать необходимые пакеты в формат файла App-V 5.0 **(.appv).**

    -   Чтобы повторно последовательность пакетов, рассмотрите возможность использования последней версии секвенсора для достижения наилучших результатов.

    Дополнительные сведения о публикации пакетов см. в публикации пакета с [помощью консоли управления.](how-to-publish-a-package-by-using-the-management-console-50.md)

3.  Развертывание пакетов на клиентских компьютерах.

4.  Преобразование точек расширения при необходимости. Для получения дополнительных сведений см. следующие ресурсы.

    -   [Перенос точек расширения из пакета App-V 4.6 в преобразованный пакет App-V 5.0 для всех пользователей на указанном компьютере](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [Перенос точек расширения из пакета App-V 4.6 в App-V 5.0 для конкретного пользователя](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [Преобразование пакета, созданного в предыдущей версии App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  Проверьте, успешно ли ваши пакеты App-V 5.0, а затем удалите пакеты 4.6. Чтобы проверить состояние пользователя на клиентских компьютерах, [](https://technet.microsoft.com/library/dn458947.aspx) рекомендуется использовать виртуализацию пользовательских интерфейсов или другой инструмент управления пользовательской средой.

    **Есть предложение для App-V?** Добавьте или проголосуйте по [предложениям здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Есть проблема с App-V?** Используйте [форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## <a name="related-topics"></a>Статьи по теме


[Планирование миграции из предыдущей версии App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)

[Развертывание программы Sequencer и клиента App-V 5.0](deploying-the-app-v-50-sequencer-and-client.md)

 

 





