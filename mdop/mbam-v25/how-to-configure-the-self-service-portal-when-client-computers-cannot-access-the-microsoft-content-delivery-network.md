---
title: Настройка портала самообслуживания при отсутствии у клиентских компьютеров доступа к сети доставки содержимого корпорации Майкрософт
description: Настройка портала самообслуживания при отсутствии у клиентских компьютеров доступа к сети доставки содержимого корпорации Майкрософт
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824492"
---
# Настройка портала самообслуживания при отсутствии у клиентских компьютеров доступа к сети доставки содержимого корпорации Майкрософт


Следуйте этим инструкциям, если клиентские компьютеры в вашей организации не имеют доступа к сети доставки содержимого (CDN) Microsoft AJAX.

**Зачем нужно настраивать это:**

Клиентские компьютеры нуждаются в доступе к сети CDN, который предоставляет порталу самообслуживания необходимый доступ к определенным файлам JavaScript. Если вы не настраиваете портал самообслуживания, когда клиентские компьютеры не могут получить доступ к сети CDN, будет отображаться только название компании и учетная запись, под которой входит конечный пользователь. Сообщение об ошибке не выводится.

**Примечание**  В MBAM 2,5 с пакетом обновления 1 (SP1) файлы JavaScript включены в продукт, и вам не нужно выполнять инструкции, описанные в этом разделе, для настройки поставщика общих служб на поддержку клиентов, которые не могут получить доступ к Интернету.

 

**Настройка портала самообслуживания, когда клиентские компьютеры не могут получить доступ к сети CDN**

1. Скачайте следующие файлы JavaScript из сети CDN:

   -   [jQuery-1.10.2.min.js](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [jQuery.validate.min.js](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [jQuery.validate.unobtrusive.min.js](https://go.microsoft.com/fwlink/?LinkID=390517)

2. Скопируйте файлы JavaScript в каталог **Scripts** на портале самообслуживания. Этот каталог находится в службе самообслуживания <em> &lt; MBAM в каталогах самостоятельной установки &gt; \\ </em> Website\\Scripts.

3. Откройте диспетчер информационных служб Интернета (IIS).

4. Разверните **сайты** &gt; **Администрирование и мониторинг Microsoft BitLocker**и выберите **Selfservice**.

   **Примечание.**  
   *Selfservice* — имя виртуального каталога по умолчанию. Если во время настройки вы выбрали другое имя для этого каталога, не забудьте заменить *Selfservice* в этих инструкциях на выбранное вами имя.

     

5. В средней области дважды щелкните **Параметры приложения**.

6. Для каждого элемента в списке ниже измените параметры приложения, чтобы они ссылались на новое расположение, заменив/ &lt; *виртуальные каталоги* &gt; /с/Selfservice/(или любым именем, которое вы выбрали при настройке). Например, путь к виртуальному каталогу будет похож на/selfservice/Scripts/jQuery-1.10.2.min.js.

   -   jQueryPath:/ &lt; *virtual directory* &gt; /Scripts/jQuery-1.10.2.min.js

   -   jQueryValidatePath:/ &lt; *virtual directory* &gt; /Scripts/jQuery.validate.min.js

   -   jQueryValidateUnobtrusivePath:/ &lt; *virtual directory* &gt; /Scripts/jQuery.validate.unobtrusive.min.js



## Статьи по теме


[Настройка веб-приложений MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

 

## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





