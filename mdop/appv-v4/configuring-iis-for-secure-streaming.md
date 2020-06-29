---
title: Настройка IIS для защиты потоковой передачи
description: Настройка IIS для защиты потоковой передачи
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821882"
---
# Настройка IIS для защиты потоковой передачи


С выпуском Microsoft Application Virtualization (App-V) версии 4,5 можно использовать протоколы HTTP и HTTPS для потоковой передачи пакетов приложений клиентам App-V. Этот параметр позволяет организациям использовать дополнительную масштабируемость, предоставляемую IIS, обычно. Если вы используете IIS как потоковый сервер, вы можете защитить связь между клиентом и сервером с помощью HTTPS вместо HTTP.

**Примечание**  Если вы хотите передавать приложения с файлового сервера, необходимо повысить безопасность обмена данными с пакетами приложений. Это может быть достигнуто с помощью IPsec. Дополнительные сведения содержатся в указанных ниже разделах библиотеки TechNet.

-   Для Windows server2003 <https://go.microsoft.com/fwlink/?LinkId=133226>

-   Для Windows Server 2008 <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## Типы MIME


При использовании IIS для потоковой передачи виртуальных приложений с использованием HTTP или HTTPS для поддержки App-V на сервере IIS должны быть добавлены следующие типы MIME:

-   . OSD = TXT

-   . SFT = binary

Ниже указаны статьи базы знаний, в которых приведены рекомендации по добавлению типов MIME.

IIS 6,0: <https://go.microsoft.com/fwlink/?LinkId=151973>

IIS 7,0: <https://go.microsoft.com/fwlink/?LinkId=151977>

## Проверка подлинности Kerberos


При использовании проверки подлинности HTTP или HTTPS и Kerberos для потоковой передачи файлов ICO, OSD и SFT вы повышаете безопасность среды. Тем не менее, чтобы службы IIS поддерживали проверку подлинности Kerberos, необходимо настроить соответствующее имя субъекта-службы (SPN). Это `setspn.exe` средство доступно для Windows server2003 из средств поддержки на установочном компакт-диске и встроено в Windows Server2008.

Чтобы создать SPN, запустите `setspn.exe` из командной строки, войдя в учетную запись администратора домена (например, `setspn.exe –A HTTP/FQDN of Server ServerName` .

## Статьи по теме


[Настройка сервера управления или сервера потоковой передачи для обеспечения защиты подключений после установки](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





