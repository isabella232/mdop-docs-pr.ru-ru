---
title: Обслуживание MBAM 1.0
description: Обслуживание MBAM 1.0
author: dansimp
ms.assetid: 02ffb093-c364-4837-bbe8-23d4c09fbd3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7eecef4e82680b08fde1b1bef88487a6fc156fe4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825772"
---
# Обслуживание MBAM 1.0


После того как вы закончите все необходимое планирование, а затем развернуть администрирование и мониторинг Microsoft BitLocker (MBAM), вы можете настроить MBAM для работы в высокодоступном режиме, а затем использовать его для управления операциями шифрования в корпоративной среде BitLocker. В этом разделе описаны параметры высокой доступности MBAM, а также способы перемещения функций сервера MBAM при необходимости.

## Пакет управления MBAM


Пакет управления MicrosoftSystemCenterOperationsManager для MBAM доступен для загрузки в центре загрузки Майкрософт.

Этот пакет управления отслеживает критические взаимодействия в серверной инфраструктуре, например соединения между веб-службами и базами данных, а также операционные вызовы между сайтами и поддержкой веб-службы. Кроме того, он отправляет запросы между настольными клиентами и соответствующими конечными точками веб-служб.

[Пакет управления для администрирования и мониторинга Microsoft BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=258390)

## Обеспечение высокой доступности для MBAM 1,0


MBAM разработана для обеспечения отказоустойчивости. Если сервер становится недоступен, пользователи не должны иметь негативных изменений. Данные в этом разделе можно использовать для настройки установки MBAM с высокой доступностью.

[Высокая доступность для MBAM 1.0](high-availability-for-mbam-10.md)

## Перемещение функций 1,0 MBAM на другой сервер


Если вам нужно переместить компонент сервера MBAM на другой компьютер, необходимо выполнить определенные действия, чтобы избежать потери производительности или данных. В этом разделе описаны действия, которые необходимо выполнить, чтобы переместить один или несколько функций сервера MBAM на другой компьютер.

[Перемещение компонентов MBAM 1.0 на другой компьютер](how-to-move-mbam-10-features-to-another-computer.md)

## Другие ресурсы для обслуживания MBAM


[Операции MBAM 1.0](operations-for-mbam-10.md)

 

 




