---
title: Установка языкового обновления MBAM на отдельном сервере
description: Установка языкового обновления MBAM на отдельном сервере
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824752"
---
# <span data-ttu-id="b30f7-103">Установка языкового обновления MBAM на отдельном сервере</span><span class="sxs-lookup"><span data-stu-id="b30f7-103">How to Install the MBAM Language Update on a Single Server</span></span>


<span data-ttu-id="b30f7-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) включает четыре роли сервера, которые можно запускать на одном или нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="b30f7-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="b30f7-105">Тем не менее, только для двух функций сервера MBAM требуется обновление для поддержки установки MBAM языка и шаблона политики MBAM в версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="b30f7-105">However, only two MBAM Server features require the update to support installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="b30f7-106">Чтобы обновить все три обязательных компонента MBAM, которые должны быть установлены на одном компьютере, выполните действия, описанные в этой статье.</span><span class="sxs-lookup"><span data-stu-id="b30f7-106">To update all three of the required MBAM features to be installed on one computer, perform the steps described in this topic.</span></span>

**<span data-ttu-id="b30f7-107">Установка языкового обновления MBAM на одном сервере</span><span class="sxs-lookup"><span data-stu-id="b30f7-107">To install the MBAM language update on a single server</span></span>**

1.  <span data-ttu-id="b30f7-108">Откройте консоль управления службами IIS, перейдите на **сайт**, а затем завершите работу веб-сайта администрирования Microsoft BitLocker и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="b30f7-108">Open the Internet Information Services (IIS) Management Console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="b30f7-109">Измените привязки для веб-сайта MBAM и временно измените привязки сайта.</span><span class="sxs-lookup"><span data-stu-id="b30f7-109">Edit the bindings for the MBAM website, and then temporarily modify the bindings of the site.</span></span> <span data-ttu-id="b30f7-110">Например, измените порт 443 на 9443.</span><span class="sxs-lookup"><span data-stu-id="b30f7-110">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="b30f7-111">Найдите и запустите мастер настройки MBAM (MBAMsetup.exe) и выберите указанные ниже три функции.</span><span class="sxs-lookup"><span data-stu-id="b30f7-111">Locate and run the MBAM setup wizard (MBAMsetup.exe) and select the following three features:</span></span>

    1.  <span data-ttu-id="b30f7-112">Отчеты о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="b30f7-112">Compliance and Audit Reports</span></span>

    2.  <span data-ttu-id="b30f7-113">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="b30f7-113">Administration and Monitoring Server</span></span>

    3.  <span data-ttu-id="b30f7-114">Шаблоны групповой политики</span><span class="sxs-lookup"><span data-stu-id="b30f7-114">Group Policy Templates</span></span>

    <span data-ttu-id="b30f7-115">**Важно!**  Возможности сервера MBAM необходимо обновлять в следующем порядке: отчеты о соответствии и аудите сначала, затем на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="b30f7-115">**Important** The MBAM server features must be updated in the following order: Compliance and Audit Reports first, then Administration and Monitoring Server.</span></span> <span data-ttu-id="b30f7-116">Вы можете в любое время обновить шаблоны групповой политики, не заботясь о последовательностях.</span><span class="sxs-lookup"><span data-stu-id="b30f7-116">The Group Policy templates can be updated at any time without concern for sequence.</span></span>

     

4.  <span data-ttu-id="b30f7-117">После обновления базы данных сервера откройте консоль управления IIS и проверьте привязки на веб-сайте администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b30f7-117">After you upgrade the server database, open the IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="b30f7-118">Удалите одну из привязок и убедитесь в том, что оставшаяся привязка имеет правильное имя узла, сертификат и номер порта для конфигурации предприятия MBAM.</span><span class="sxs-lookup"><span data-stu-id="b30f7-118">Delete one of the bindings and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="b30f7-119">Перезапустите веб-сайт MBAM.</span><span class="sxs-lookup"><span data-stu-id="b30f7-119">Restart the MBAM website.</span></span>

7.  <span data-ttu-id="b30f7-120">Проверка функционирования веб-сайта MBAM:</span><span class="sxs-lookup"><span data-stu-id="b30f7-120">Test the MBAM website functionality:</span></span>

    -   <span data-ttu-id="b30f7-121">Откройте веб-интерфейс MBAM и убедитесь, что вы можете выбрать ключ восстановления для клиента.</span><span class="sxs-lookup"><span data-stu-id="b30f7-121">Open the MBAM web interface and ensure you can fetch a recovery key for a client.</span></span>

    -   <span data-ttu-id="b30f7-122">Обеспечивает шифрование нового или вручную расшифрованного клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="b30f7-122">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="b30f7-123">**Примечание**  Клиент MBAM открывается только в том случае, если он может взаимодействовать с базой данных восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="b30f7-123">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="b30f7-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b30f7-124">Related topics</span></span>


[<span data-ttu-id="b30f7-125">Развертывание обновления языковой версии MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="b30f7-125">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





