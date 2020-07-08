---
title: Настройка необходимых компонентов среды
description: Настройка необходимых компонентов среды
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826449"
---
# Настройка необходимых компонентов среды


Прежде чем вы сможете развернуть и запустить виртуализацию классической версии Microsoft Enterprise (MED-V) 2,0, убедитесь, что ваша среда отвечает указанным ниже минимальным требованиям.

**Windows 7;**

Агент хоста MED-V и диспетчер рабочих областей MED-V поддерживаются только в Windows 7 и более поздних версиях.

**Windows XP SP3**

Гостевой агент MED-V поддерживается только в Windows XP с пакетом обновления 3 (SP3).

**.NET Framework 3,5 SP1**

Для агентов и виртуальных машин MED-V и "гость" и для диспетчера рабочих областей MED-V требуется Microsoft .NET Framework 3,5 с пакетом обновления 1 (SP1).

**Важно!**  Кроме того, необходимо установить обновление [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) , которое предназначено для устранения нескольких известных проблем с совместимостью приложений.

 

**Примечание**  Необходимо вручную установить .NET Framework 3,5 SP1 и Update KB959209 в образ Windows Virtual PC, подготовленный для использования с MED-V. Однако по умолчанию платформа Microsoft .NET Framework 3,5 с пакетом обновления 1 (SP1) и обновление включается при установке Windows 7 на главном компьютере.

 

**Инфраструктура службы каталогов Active Directory**

Групповая политика обеспечивает централизованное управление и настройку операционных систем, приложений и параметров пользователей в среде Active Directory.

## Статьи по теме


[Настройка необходимых компонентов для установки](configure-installation-prerequisites.md)

[Высокоуровневая архитектура](high-level-architecturemedv2.md)

[Поддерживаемые конфигурации MED-V 2.0](med-v-20-supported-configurations.md)

 

 





