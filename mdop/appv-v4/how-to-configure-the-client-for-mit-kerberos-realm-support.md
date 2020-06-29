---
title: Настройка клиента для поддержки сфер MIT Kerberos
description: Настройка клиента для поддержки сфер MIT Kerberos
author: dansimp
ms.assetid: 46102f4c-270c-4115-8eb4-7ff5ae3be32d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ae5cd73d00f340bc50070fdd0a5fd3e038cc3789
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817812"
---
# <span data-ttu-id="54601-103">Настройка клиента для поддержки сфер MIT Kerberos</span><span class="sxs-lookup"><span data-stu-id="54601-103">How to Configure the Client for MIT Kerberos Realm Support</span></span>


<span data-ttu-id="54601-104">В Application Virtualization (App-V) 4,5 с пакетом обновления 1 (SP1) добавлена поддержка для сферы Kerberos MIT.</span><span class="sxs-lookup"><span data-stu-id="54601-104">In Application Virtualization (App-V) 4.5 SP1, support was added for MIT Kerberos realms.</span></span> <span data-ttu-id="54601-105">В этой статье приведены подробные сведения о том, как включить эту поддержку.</span><span class="sxs-lookup"><span data-stu-id="54601-105">This topic provides detailed information on how to enable that support.</span></span>

**<span data-ttu-id="54601-106">Включение поддержки сфер Kerberos MIT</span><span class="sxs-lookup"><span data-stu-id="54601-106">To enable support for MIT Kerberos Realms</span></span>**

-   <span data-ttu-id="54601-107">Создайте новый раздел реестра с именем **UseMitKerberos** типа DWORD, как описано ниже, и установите для него значение 1.</span><span class="sxs-lookup"><span data-stu-id="54601-107">Create a new registry key named **UseMitKerberos** of type DWORD, as follows, and then set it to a value of 1.</span></span>

    <span data-ttu-id="54601-108">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos</span><span class="sxs-lookup"><span data-stu-id="54601-108">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos</span></span>

 

 





