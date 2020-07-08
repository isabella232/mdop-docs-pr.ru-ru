---
title: Необходимые условия для установки MED-V
description: Необходимые условия для установки MED-V
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824969"
---
# Необходимые условия для установки MED-V


Ниже приведены условия, необходимые для установки MED-V.

[Требования к службе каталогов Active Directory](#bkmk-activedirectoryrequirements)

[База данных отчетов](#bkmk-howtoinstallthereportdatabase)

[Конфигурация программного обеспечения для защиты от вирусов и резервного копирования](#bkmk-antivirusbackupsoftwareconfiguration)

[Microsoft Virtual PC 2007 с пакетом обновления 1 (SP1)](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a>Требования к службе каталогов Active Directory


При настройке сервера MED-V, если пользователи не являются частью того же домена, которому принадлежит сервер, необходимо установить доверие между доменами.

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a>Установка базы данных отчета


Для хранения всех журналов рабочей области для MED-V требуется база данных отчета. Затем база данных журнала используется для создания отчетов MED-V. Сведения об отчетах можно найти в разделе [отчетность по MED-V](med-v-reporting.md).

SQL Server можно установить на том же сервере, что и сервер MED-V, или на удаленном сервере. Если установка выполняется на удаленном сервере, ознакомьтесь со сведениями о том, [как установить SQL Server на удаленном сервере](#bkmk-installingsqlserveronaremoteserver).

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a>Установка SQL Server на удаленном сервере

**Установка SQL Server на удаленном сервере**

1.  На удаленном сервере настройте следующие параметры:

    -   Имя экземпляра — экземпляр по умолчанию

    -   Режим проверки подлинности — смешанный режим

    -   User (пользователь по умолчанию — "SA")

    -   Password (пароль) — желаемый пароль

    -   Параметры сортировки — по умолчанию

    -   Ошибка в параметрах отчета об использовании — по умолчанию

2.  Установите на сервер MED-V следующие файлы:

    -   Чтобы установить необходимые компоненты для коллекции объектов пакета управления для Microsoft SQL Server2008, скачайте [собственный клиент Microsoft SQL Server2008](https://go.microsoft.com/fwlink/?LinkId=164039) из центра загрузки Майкрософт.

    -   Чтобы установить необходимые компоненты для коллекции объектов пакета управления для Microsoft SQL Server2005, скачайте [собственный клиент Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=164038) из центра загрузки Майкрософт.

    -   Чтобы установить необходимые файлы DLL для Microsoft SQL Server2008, скачайте [коллекцию управляющих объектов Microsoft SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=164041) из центра загрузки Майкрософт.

    -   Чтобы установить необходимые файлы DLL для Microsoft SQL Server2005, скачайте [объекты управления Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=164040) из центра загрузки Майкрософт.

    -   Чтобы установить отдельные пакеты установки, предоставляющие дополнительные значения для SQL Server2008, скачайте [пакет дополнительных компонентов Microsoft SQL Server2008](https://go.microsoft.com/fwlink/?LinkId=163960) из центра загрузки Майкрософт.

    -   Чтобы установить отдельные пакеты установки, предоставляющие дополнительные значения для SQL Server2005, скачайте [пакет дополнительных компонентов для Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) из центра загрузки Майкрософт.

    Дополнительные сведения об этих файлах можно найти в [пакете дополнительных компонентов Microsoft SQL Server2008](https://go.microsoft.com/fwlink/?LinkId=163960) в центре загрузки Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163960) или в [пакете дополнительных компонентов для Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) на веб-странице центра загрузки Майкрософт () https://go.microsoft.com/fwlink/?LinkId=163961) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>Конфигурация программного обеспечения для защиты от вирусов и резервного копирования


Чтобы предотвратить влияние антивирусной программы на производительность виртуального рабочего стола, рекомендуется исключить следующие типы файлов виртуальных машин из антивирусной программы или обработки резервного копирования, запущенной на узле.

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. CKM

-   \*. EVHD

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a>Установка и настройка Microsoft Virtual PC2007 с пакетом обновления 1 (SP1)


**Важно!**  Если Virtual PC для Windows существует на главном компьютере, удалите его перед установкой Virtual PC2007 SP1.

 

**Установка Microsoft Virtual PC2007 SP1**

1.  Загрузите виртуальный PC2007 пакет обновления 1 (SP1) с [Virtual PC 2007](https://go.microsoft.com/fwlink/?LinkId=142994)с помощью центра загрузки Майкрософт.

2.  Запустите установочный файл на главном компьютере и следуйте инструкциям мастера.

3.  Установите виртуальную версию PC2007 SP1 на главном компьютере в режиме с повышенными привилегиями.

    Дополнительные сведения можно найти [в описании исправления для Virtual PC 2007 с пакетом обновления 1 (SP1)](https://go.microsoft.com/fwlink/?LinkId=150575).

    **Примечание**  Для запуска Virtual PC2007 SP1 требуется обновление виртуальных PC2007 SP1.

     

## Статьи по теме


[Поддерживаемые конфигурации](supported-configurationsmedv-orientation.md)

 

 





