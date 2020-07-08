---
title: Использование приложения App-V 4,6 из приложения App-V 5,1
description: Использование приложения App-V 4,6 из приложения App-V 5,1
author: dansimp
ms.assetid: 909b4391-762b-4988-b0cf-32b67f1fcf0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: c0d308dcae33b02c089c101ffcd5041b2e665f59
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813637"
---
# Использование приложения App-V 4,6 из приложения App-V 5,1

*Примечание:** App-V 4,6 вышел из основной поддержки. Указанные ниже инструкции относятся к пакету приложения App-V 4,6 с пакетом обновления 3 (SP3).

Чтобы запустить приложение App-V 4.6 с приложениями App-V 5,1 на отдельном клиенте, выполните указанные ниже действия.

**Примечание**  В этой процедуре предполагается, что вы используете последнюю версию App-V 4,6.

**Запуск приложений на автономном клиенте**

1.  Выберите в среде два приложения, которые можно открывать друг от друга. Например, Microsoft Outlook и Adobe Acrobat Reader. Вы можете получить доступ к вложению электронной почты, созданному с помощью Adobe Acrobat.

2.  Преобразуйте пакеты или создайте новый пакет для любого из приложений, использующих формат App-V 5,1. Дополнительные сведения о преобразовании пакетов можно найти в разделе [как переносить точки расширения из пакета App-v 4,6 в преобразованный пакет App-v 5,1 для всех пользователей на определенном компьютере](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md) или [переносить точки расширения из пакета app-v 4,6 в приложение app-v 5,1 для определенного пользователя](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).

3.  Добавьте и подготовьте пакет с помощью консоли управления App-V 5,1. Дополнительные сведения о добавлении и подготовке пакетов можно найти в разделе [Добавление и обновление пакетов с помощью консоли управления](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) и [Настройка доступа к пакетам с помощью консоли управления](how-to-configure-access-to-packages-by-using-the-management-console-51.md).

4.  Преобразованное приложение теперь запускается с помощью App-V 5,1, и вы можете открыть одно приложение из другого. Например, если вы преобразовали пакет Microsoft Office в пакет App-V 5,1, а приложение Adobe Acrobat по-прежнему работает как пакет App-V 4.6, вы можете открыть вложение Adobe Acrobat Reader с помощью Microsoft Outlook.

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.1](operations-for-app-v-51.md)

 

 





