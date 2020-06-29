---
title: Изменение конфигурации клиента App-V 5.1 с помощью шаблона ADMX и групповой политики
description: Изменение конфигурации клиента App-V 5.1 с помощью шаблона ADMX и групповой политики
author: dansimp
ms.assetid: 0d9cf13a-b29c-4c87-a776-15fea34027dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 18363b4fb904d995862ac30634be1350c972d918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813824"
---
# Изменение конфигурации клиента App-V 5.1 с помощью шаблона ADMX и групповой политики


Используйте шаблон Microsoft Application Virtualization (App-V) 5,1 ADMX, чтобы настроить параметры клиента App-V 5,1 с помощью шаблона ADMX и групповой политики.

**Изменение конфигурации клиента App-V 5,1 с помощью групповой политики**

1.  Чтобы изменить конфигурацию клиента App-V 5,1, найдите файлы **ADMXTemplate** , доступные в приложении App-v 5,1.

    **Примечание**  Чтобы скачать шаблоны App-V 5,1 **ADMX**, воспользуйтесь следующей ссылкой: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .

     

2.  На компьютере, на котором вы управляете групповой политикой (обычно это контроллер домена), скопируйте файл template **. ADMX** в следующий каталог: ** &lt; установочный диск &gt; \ \ Windows \ \ PolicyDefinitions**.

    Затем на том же компьютере скопируйте файл **ADML** в следующий каталог: ** &lt; InstallationDrive &gt; \ \ Windows \ \ POLICYDEFINITIONS \ \ en-US**.

3.  После копирования файлов откройте консоль управления групповыми политиками, чтобы изменить политики, связанные с вашими клиентами App-V 5,1, перейдите к политикам **конфигурации компьютера**  /  **Policies**  /  **Administrative Templates**  /  **. System**  /  **App-v**.

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Развертывание App-V 5.1](deploying-app-v-51.md)

[Сведения о параметрах конфигурации клиента](about-client-configuration-settings51.md)

 

 





