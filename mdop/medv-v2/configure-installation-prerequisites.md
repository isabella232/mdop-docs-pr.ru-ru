---
title: Настройка необходимых компонентов для установки
description: Настройка необходимых компонентов для установки
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819309"
---
# Настройка необходимых компонентов для установки


Ниже приведены рекомендации по установке и использованию виртуализации классической версии Microsoft Enterprise (MED-V) 2,0:

[Windows Virtual PC](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[Обновление для Windows Virtual PC](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[Конфигурация программного обеспечения для защиты от вирусов и резервного копирования](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a>Установка и настройка Windows Virtual PC


**Важно!**  Если на главном компьютере уже есть версия Virtual PC для Windows, необходимо удалить ее, прежде чем устанавливать Virtual PC для Windows.

 

**Установка Virtual PC для Windows**

1.  Скачайте [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) из центра загрузки Майкрософт ( https://go.microsoft.com/fwlink/?LinkId=195918) .

2.  Запустите установочный файл на главном компьютере и следуйте инструкциям мастера.

**Важно!**  В Windows Virtual PC есть пакет компонентов интеграции, который предоставляет возможности, повышающие взаимодействие между виртуальной средой и физическим компьютером. Например, это позволяет перемещать указатель мыши между узлом и гостевым компьютером. Для работы MED-V требуется установка пакета компонентов интеграции.

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a>Установка и Настройка обновления для Windows Virtual PC


Обновление Майкрософт, связанное со статьей KB977206, включает режим Windows XP для компьютеров без технологии виртуализации с аппаратной поддержкой (HAV). Рекомендуется установить это обновление, так как некоторые возможности интеграции могут работать неправильно, если пакет компонентов интеграции в гостевой операционной системе не совпадает с версией Virtual PC, установленной на главном компьютере.

**Важно!**  При установке MED-V на узловые компьютеры под управлением Windows 7 с пакетом обновления 1 (SP1) вам не нужно устанавливать это обновление.

 

**Совет**  В дополнение к описанному здесь обновлению рекомендуется ознакомиться со всеми доступными обновлениями Virtual PC для Windows и применить соответствующие или необходимые обновления для вашей среды.

 

**Установка обновления для Windows Virtual PC**

1.  Скачайте нужное обновление для Windows Virtual PC из центра загрузки Майкрософт.

    [32-разрядное обновление](https://go.microsoft.com/fwlink/?LinkId=195919) ( https://go.microsoft.com/fwlink/?LinkId=195919) .

    [64-разрядное обновление](https://go.microsoft.com/fwlink/?LinkId=195920) ( https://go.microsoft.com/fwlink/?LinkId=195920) .

2.  Запустите установочный файл на главном компьютере в режиме с повышенными привилегиями и следуйте инструкциям мастера.

    Дополнительные сведения о пакете исправлений для Virtual PC для Windows можно найти в [статье 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ( https://go.microsoft.com/fwlink/?LinkId=195921) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>Настройка программного обеспечения для защиты от вирусов и резервного копирования


Чтобы предотвратить влияние антивирусной программы на производительность виртуального рабочего стола, мы рекомендуем, где вы можете исключить следующие типы файлов виртуальных машин из антивирусной программы или процесса резервного копирования, запущенного на главном компьютере:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. VHD

## Статьи по теме


[Настройка необходимых компонентов среды](configure-environment-prerequisites.md)

[Высокоуровневая архитектура](high-level-architecturemedv2.md)

[Поддерживаемые конфигурации MED-V 2.0](med-v-20-supported-configurations.md)

 

 





