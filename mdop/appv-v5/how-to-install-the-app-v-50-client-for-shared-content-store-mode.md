---
title: Установка клиента App-V 5.0 для режима хранилища общего содержимого
description: Установка клиента App-V 5.0 для режима хранилища общего содержимого
author: dansimp
ms.assetid: 88f09e6f-19e7-48ea-965a-907052d1a02f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 704ea6c1e4b1ba4670a4e52d754b8e6e5a9fb8f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814056"
---
# Установка клиента App-V 5.0 для режима хранилища общего содержимого


Выполните указанные ниже действия, чтобы установить клиент Microsoft Application Virtualization (App-V) 5,0 таким образом, чтобы он использовал режим хранилища общего содержимого App-V 5,0 (SCS). Убедитесь, что все необходимые компоненты установлены на компьютере, на который планируется установить приложение. Чтобы получить [необходимые требования для App-V 5,0](app-v-50-prerequisites.md), используйте следующую ссылку:

**Примечание**  Перед выполнением этой процедуры при необходимости удалите любую существующую версию клиента App-V 5,0.

 

Дополнительные сведения о режиме SCS можно найти [в разделе Общий доступ к хранилищу содержимого в Microsoft App-V 5,0 за сценой](https://go.microsoft.com/fwlink/?LinkId=316879) ( https://go.microsoft.com/fwlink/?LinkId=316879) .

**Установка и Настройка клиента App-V 5,0 для режима SCS**

1.  Скопируйте установочные файлы клиента App-V 5,0 на компьютер, на котором он будет установлен. Откройте командную строку и в каталоге, в котором хранятся файлы установки, введите один из указанных ниже вариантов в зависимости от версии устанавливаемого клиента.

    -   Чтобы установить версию RDS клиента App-V 5,0, введите: **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**

    -   Чтобы установить стандартную версию App-V 5,0 Client Type: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**

        **Важно!**  Вы должны выполнить автоматическую установку, или установка завершится сбоем.

         

2.  После завершения установки вы можете развернуть пакеты на компьютере, на котором запущен клиент, и все содержимое пакета будет передаваться в потоке в сети.

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Развертывание программы Sequencer и клиента App-V 5.0](deploying-the-app-v-50-sequencer-and-client.md)

 

 





