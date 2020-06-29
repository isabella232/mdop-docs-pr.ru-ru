---
title: Установка обновлений языкового пакета MBAM на распределенных серверах
description: Установка обновлений языкового пакета MBAM на распределенных серверах
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825699"
---
# <span data-ttu-id="aab8d-103">Установка обновлений языкового пакета MBAM на распределенных серверах</span><span class="sxs-lookup"><span data-stu-id="aab8d-103">How to Install the MBAM Language Update on Distributed Servers</span></span>


<span data-ttu-id="aab8d-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) включает четыре роли сервера, которые можно запускать на одном или нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="aab8d-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="aab8d-105">Тем не менее, только для двух функций сервера MBAM требуется обновление, поддерживающее установку шаблона политики MBAM для MBAM и языков в версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="aab8d-105">However, only two MBAM Server features require the update to support the installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="aab8d-106">В конфигурациях с функциями сервера MBAM, установленными на нескольких компьютерах, нужно обновить только следующие компоненты сервера:</span><span class="sxs-lookup"><span data-stu-id="aab8d-106">In configurations with the MBAM Server features installed on multiple computers, only the following server features need to be updated:</span></span>

-   <span data-ttu-id="aab8d-107">Отчеты о соответствии MBAM и аудит</span><span class="sxs-lookup"><span data-stu-id="aab8d-107">The MBAM Compliance and Audit Reports</span></span>

-   <span data-ttu-id="aab8d-108">Сервер администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="aab8d-108">The MBAM Administration and Monitoring Server</span></span>

<span data-ttu-id="aab8d-109">**Важно!**  Возможности сервера MBAM необходимо обновлять в следующем порядке: сначала отчеты о соответствии и аудите, а затем на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="aab8d-109">**Important** The MBAM server features must be updated in this order: Compliance and Audit Reports first, and then the Administration and Monitoring Server.</span></span> <span data-ttu-id="aab8d-110">Шаблоны групповой политики MBAM можно обновлять в любое время без возникновения последовательности.</span><span class="sxs-lookup"><span data-stu-id="aab8d-110">The MBAM Group Policy templates can be updated at any time without concern for sequence.</span></span>

 

**<span data-ttu-id="aab8d-111">Установка обновления языка MBAM на компоненте сервера отчетов о соответствии требованиям и аудите MBAM</span><span class="sxs-lookup"><span data-stu-id="aab8d-111">To install the MBAM Language Update on the MBAM Compliance and Audit Report Server feature</span></span>**

1.  <span data-ttu-id="aab8d-112">На компьютере, на котором работает функция проверки соответствия требованиям и аудита MBAM, найдите и запустите мастер настройки обновления на MBAM языке (MBAMsetup.exe).</span><span class="sxs-lookup"><span data-stu-id="aab8d-112">On the computer running the MBAM Compliance and Audit Report feature, locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span>

2.  <span data-ttu-id="aab8d-113">Завершите работу мастера для создания отчетов о соответствии и аудита, а затем закройте окно мастера.</span><span class="sxs-lookup"><span data-stu-id="aab8d-113">Complete the wizard for the Compliance and Audit Reports and then close the wizard.</span></span>

**<span data-ttu-id="aab8d-114">Установка обновления языка MBAM на компоненте администрирования и мониторинга сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="aab8d-114">To install the MBAM Language Update on the MBAM Administration and Monitoring Server feature</span></span>**

1.  <span data-ttu-id="aab8d-115">На компьютере, на котором запущена функция администрирования и мониторинга MBAM, откройте консоль управления службами IIS, перейдите на **сайт**, а затем завершите работу веб-сайта администрирования и наблюдения Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="aab8d-115">On the computer that is running the MBAM Administration and Monitoring feature, open the Internet Information Services (IIS) management console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="aab8d-116">Щелкните, чтобы изменить привязки для веб-сайта MBAM, а затем измените привязки сайта.</span><span class="sxs-lookup"><span data-stu-id="aab8d-116">Choose to edit the bindings for the MBAM website, and then modify the bindings of the site.</span></span> <span data-ttu-id="aab8d-117">Например, измените порт 443 на 9443.</span><span class="sxs-lookup"><span data-stu-id="aab8d-117">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="aab8d-118">Найдите и запустите мастер настройки языкового обновления MBAM (MBAMsetup.exe).</span><span class="sxs-lookup"><span data-stu-id="aab8d-118">Locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span> <span data-ttu-id="aab8d-119">Завершите работу мастера для компонента администрирования и мониторинга сервера, а затем закройте окно мастера.</span><span class="sxs-lookup"><span data-stu-id="aab8d-119">Complete the wizard for the Administration and Monitoring Server feature and then close the wizard.</span></span>

4.  <span data-ttu-id="aab8d-120">После обновления базы данных сервера откройте консоль управления IIS и проверьте привязки на веб-сайте администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="aab8d-120">After you upgrade the server database, open IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="aab8d-121">Удалите старую привязку и убедитесь в том, что оставшаяся привязка имеет правильное имя узла, сертификат и номер порта для конфигурации предприятия MBAM.</span><span class="sxs-lookup"><span data-stu-id="aab8d-121">Delete the old binding and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="aab8d-122">Перезапустите веб-сайт MBAM.</span><span class="sxs-lookup"><span data-stu-id="aab8d-122">Restart the MBAM web site.</span></span>

7.  <span data-ttu-id="aab8d-123">Проверка функциональных возможностей веб-сайта MBAM.</span><span class="sxs-lookup"><span data-stu-id="aab8d-123">Test the MBAM web site functionality:</span></span>

    -   <span data-ttu-id="aab8d-124">Откройте веб-интерфейс MBAM и убедитесь, что вы можете получить ключ восстановления для клиента.</span><span class="sxs-lookup"><span data-stu-id="aab8d-124">Open the MBAM web interface and ensure that you can obtain a recovery key for a client.</span></span>

    -   <span data-ttu-id="aab8d-125">Обеспечивает шифрование нового или вручную расшифрованного клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="aab8d-125">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="aab8d-126">**Примечание**  Клиент MBAM открывается только в том случае, если он может взаимодействовать с базой данных восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="aab8d-126">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="aab8d-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="aab8d-127">Related topics</span></span>


[<span data-ttu-id="aab8d-128">Развертывание обновления языковой версии MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="aab8d-128">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





