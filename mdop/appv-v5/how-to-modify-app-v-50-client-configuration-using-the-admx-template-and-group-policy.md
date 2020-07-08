---
title: Изменение конфигурации клиента App-V 5.0 с помощью шаблона ADMX и групповой политики
description: Изменение конфигурации клиента App-V 5.0 с помощью шаблона ADMX и групповой политики
author: dansimp
ms.assetid: 79d03a2b-2586-4ca7-bbaa-bdeb0a694279
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cd257691bf223baa5e2919d83fdbf53d34f271ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813840"
---
# Изменение конфигурации клиента App-V 5.0 с помощью шаблона ADMX и групповой политики


Используйте шаблон App-V 5,0 ADMX для настройки клиента App-V 5,0 с помощью шаблона ADMX и групповой политики.

**Изменение конфигурации клиента App-V 5,0 с помощью групповой политики**

1.  Чтобы изменить конфигурацию клиента App-V 5,0, найдите файлы **ADMXTemplate** , доступные в приложении App-v 5,0.

    **Примечание**  Чтобы скачать шаблоны App-V 5,0 **ADMX**, воспользуйтесь следующей ссылкой: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .

     

2.  На компьютере, на котором вы управляете групповой политикой (обычно это контроллер домена), скопируйте файл template **. ADMX** в следующий каталог: ** &lt; установочный диск &gt; \ \ Windows \ \ PolicyDefinitions**.

    Затем на том же компьютере скопируйте файл **ADML** в следующий каталог: ** &lt; InstallationDrive &gt; \ \ Windows \ \ POLICYDEFINITIONS \ \ en-US**.

3.  После копирования файлов откройте консоль управления групповыми политиками, чтобы изменить политики, связанные с вашими клиентами App-V 5,0, перейдите к политикам **конфигурации компьютера**  /  **Policies**  /  **Administrative Templates**  /  **. System**  /  **App-v**.

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Развертывание App-V 5.0](deploying-app-v-50.md)

[Сведения о параметрах конфигурации клиента](about-client-configuration-settings.md)

 

 





