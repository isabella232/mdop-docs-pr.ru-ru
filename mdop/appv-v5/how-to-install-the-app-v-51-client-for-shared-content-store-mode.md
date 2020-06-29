---
title: Установка клиента App-V 5.1 для режима хранилища общего содержимого
description: Установка клиента App-V 5.1 для режима хранилища общего содержимого
author: dansimp
ms.assetid: 6f3ecb1b-b5b5-4ae0-8de9-b4ffdfd2c216
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7ce8114a44762180bf9bb0240913dca50c55d31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814053"
---
# Установка клиента App-V 5.1 для режима хранилища общего содержимого


Выполните указанные ниже действия, чтобы установить клиент Microsoft Application Virtualization (App-V) 5,1 таким образом, чтобы он использовал режим хранилища общего содержимого App-V 5,1 (SCS). Убедитесь, что все необходимые компоненты установлены на компьютере, на который планируется установить приложение. Чтобы увидеть [требования к приложению App-V 5,1](app-v-51-prerequisites.md), воспользуйтесь следующей ссылкой.

**Примечание**  Перед выполнением этой процедуры при необходимости удалите любую существующую версию клиента App-V 5,1.

 

Дополнительные сведения о режиме SCS можно найти [в разделе Общий доступ к хранилищу содержимого в Microsoft App-V 5,0 за сценой](https://go.microsoft.com/fwlink/?LinkId=316879) ( https://go.microsoft.com/fwlink/?LinkId=316879) .

**Установка и Настройка клиента App-V 5,1 для режима SCS**

1.  Скопируйте установочные файлы клиента App-V 5,1 на компьютер, на котором он будет установлен. Откройте командную строку и в каталоге, в котором хранятся файлы установки, введите один из указанных ниже вариантов в зависимости от версии устанавливаемого клиента.

    -   Чтобы установить версию RDS клиента App-V 5,1, введите: **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**

    -   Чтобы установить стандартную версию App-V 5,1 Client Type: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**

        **Важно!**  Вы должны выполнить автоматическую установку, или установка завершится сбоем.

         

2.  После завершения установки вы можете развернуть пакеты на компьютере, на котором запущен клиент, и все содержимое пакета будет передаваться в потоке в сети.

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Развертывание Sequencer и клиента App-V 5.1](deploying-the-app-v-51-sequencer-and-client.md)

 

 





