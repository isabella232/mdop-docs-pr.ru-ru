---
title: Скрытие элемента шифрования диска BitLocker по умолчанию на панели управления
description: Скрытие элемента шифрования диска BitLocker по умолчанию на панели управления
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823099"
---
# Скрытие элемента шифрования диска BitLocker по умолчанию на панели управления


В этой статье описано, как скрыть элемент панели управления **шифрованием диска BitLocker** , который отображается по умолчанию на панели управления в составе операционной системы Windows.

**Примечание**  Администрирование и мониторинг Microsoft BitLocker (MBAM) создает дополнительный настраиваемый элемент панели управления, который называется **параметрами шифрования BitLocker**, позволяющим конечным пользователям управлять своим PIN-кодом и паролем, включать BitLocker для диска и проверять шифрование.

 

Ознакомьтесь [со статьей общие сведения о параметрах шифрования BitLocker и элементах шифрования диска BitLocker на панели управления](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) .

-   Различия между MBAM и элементами панели управления по умолчанию

-   **Управление** контекстным меню BitLocker, которое появляется при щелчке диска правой кнопкой мыши в проводнике Windows

**Важно!**  Не изменяйте параметры групповой политики в узле **шифрования диска BitLocker** . В противном случае MBAM не будет работать правильно. При настройке параметров групповой политики на узле **MDOP MBAM (Управление BitLocker)** MBAM автоматически настраивает параметры **шифрования диска для BitLocker** .

 

**Скрытие элемента шифрования диска BitLocker по умолчанию на панели управления**

1.  В консоли управления групповыми политиками (GPMC) или в разделе Расширенное управление групповыми политиками перейдите к элементу политики **конфигурации пользователей** &gt; **Policies** &gt; **Administrative Templates** &gt; **панели управления**"Административные шаблоны".

2.  В области **сведений** дважды щелкните **Скрыть указанные элементы панели управления**, а затем выберите пункт **включена**.

3.  Нажмите кнопку **Показать**, нажмите кнопку **Добавить**и введите **Microsoft. BitLockerDriveEncryption**.



## Статьи по теме


[Общие сведения о параметрах шифрования BitLocker и шифровании дисков BitLocker в панели управления](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[Развертывание объектов групповой политики MBAM 2.5](deploying-mbam-25-group-policy-objects.md)

 

## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





