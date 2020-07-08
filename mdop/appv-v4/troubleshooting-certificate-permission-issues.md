---
title: Устранение проблем с разрешениями сертификатов
description: Устранение проблем с разрешениями сертификатов
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815209"
---
# Устранение проблем с разрешениями сертификатов


После установки приложения App-V 4.5 в том случае, если в качестве закрытого ключа не указана соответствующая таблица ACL для сетевой службы, событие заносится в журнал событий NT и в файл помещается запись `Sft-server.log` .

## Сообщения об ошибках


### Windows server2003

Event ID 36870 — произошла неустранимая ошибка при попытке доступа к закрытому ключу учетных данных SSL-сервера. Код ошибки, возвращенный из криптографического модуля, — 0x80090016.

### Windows Server2008

Event ID 36870 — произошла неустранимая ошибка при попытке доступа к закрытому ключу учетных данных SSL-сервера. Код ошибки, возвращенный из криптографического модуля, — 0x8009030d.

## SFT-Server. log


В `sft-server.log` файле, расположенном в каталоге, помещается следующее сообщение об ошибке `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` :

Не удалось загрузить сертификат. Код ошибки \ [-2146893043 \]. Убедитесь в том, что учетная запись Network Service имеет надлежащий доступ к сертификату и соответствующему файлу закрытого ключа.

 

 





