---
title: Настройка App-V для обеспечения безопасного администрирования
description: Настройка App-V для обеспечения безопасного администрирования
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de70c1df734bbf1168fd7dacf9410d3451a8a3c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821902"
---
# Настройка App-V для обеспечения безопасного администрирования


В среде, в которой важна безопасность административных операций, App-V обеспечивает безопасную связь между службой управления веб-приложением App/v и консолью управления App-V. Поскольку служба управления — это веб-приложение, необходимо обеспечить безопасность серверного приложения управления App-V на веб-сервере, на котором размещается служба управления. Как показано на приведенном ниже рисунке, этот процесс включает использование HTTPS для связи и настройку сервера IIS для разрешения только интегрированной проверки подлинности Windows.

![Настройка сети веб-службы App-v](images/appvmgmtwebservice.gif)

Служба веб-управления App-V установлена в службах IIS в виде Интернет-приложения. Чтобы служба управления Интернетом поддерживала безопасные соединения (SSL) между консолью управления App-V и службой управления веб-сайтами, вам потребуется настроить сервер IIS, на котором установлена служба веб-управления, и настроить консоль управления App-V.

## В этом разделе


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[Настройка сертификатов для обеспечения поддержки службы веб-управления App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)  
Справочные сведения о настройке сертификатов для поддержки подключений на основе SSL для обеспечения безопасной связи с веб-службой управления App-V.

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[Установка и настройка консоли управления App-V для организации более безопасной среды](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
В этой статье приведены пошаговые инструкции по подключению к службе веб-управления App-V с помощью безопасного соединения.

 

 





