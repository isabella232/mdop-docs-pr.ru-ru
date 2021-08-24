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
ms.openlocfilehash: c95fab4b2b4f402df4ff0f82f2f346c9bd226e00
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910484"
---
# <a name="configuring-app-v-for-secure-administration"></a>Настройка App-V для обеспечения безопасного администрирования


В среде, в которой важно обеспечить безопасность административных операций, App-V позволяет обеспечить безопасную связь между службой веб-управления App-V и консолью управления App-V. Поскольку служба управления — это веб-приложение, она требует обеспечения безопасности приложения App-V Management Server на веб-сервере, на котором размещена служба управления. Как показано на следующей иллюстрации, этот процесс включает использование HTTPS для связи и настройку сервера IIS для Windows комплексной проверки подлинности.

![Конфигурация сети веб-служб app-v.](images/appvmgmtwebservice.gif)

Служба веб-управления App-V устанавливается в качестве веб-приложения на iiS. Службе управления Веб-службой для поддержки безопасных (SSL) подключений между консолью управления App-V и службой управления Веб-службой необходимо настроить сервер IIS, на котором установлена служба управления веб-сайтом, и настроить консоль управления App-V.

## <a name="in-this-section"></a>В этом разделе


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[Настройка сертификатов для обеспечения поддержки службы веб-управления App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)  
Предоставляет полезные сведения о настройке сертификатов для поддержки подключений на основе SSL для обеспечения безопасности связи для службы веб-управления App-V.

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[Установка и настройка консоли управления App-V для организации более безопасной среды](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
Обеспечивает пошаговую процедуру подключения к службе веб-управления App-V с помощью безопасного подключения.

 

 





