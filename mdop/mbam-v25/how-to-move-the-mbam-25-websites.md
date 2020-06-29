---
title: Перенос веб-сайтов MBAM 2.5
description: Перенос веб-сайтов MBAM 2.5
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825749"
---
# <span data-ttu-id="a0157-103">Перенос веб-сайтов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a0157-103">How to Move the MBAM 2.5 Websites</span></span>


<span data-ttu-id="a0157-104">Используйте эти процедуры для перемещения указанных ниже веб-сайтов MBAM с одного компьютера на другой, а также для перемещения указанных ниже функций с сервера A на сервер B:</span><span class="sxs-lookup"><span data-stu-id="a0157-104">Use these procedures to move the following MBAM websites from one computer to another, that is, to move the following features from Server A to Server B:</span></span>

-   <span data-ttu-id="a0157-105">Веб-сайт администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="a0157-105">Administration and Monitoring Website</span></span>

-   <span data-ttu-id="a0157-106">Портал самообслуживания</span><span class="sxs-lookup"><span data-stu-id="a0157-106">Self-Service Portal</span></span>

<span data-ttu-id="a0157-107">**Важно!**  Во время настройки обоих сайтов вы должны предоставить одну и ту же строку подключения, URL-адрес, учетные записи групп и доменную учетную запись пула приложений веб-службы, как и те, которые вы используете в данный момент.</span><span class="sxs-lookup"><span data-stu-id="a0157-107">**Important** During the configuration of both websites, you must provide the same connection string, Reports URL, group accounts, and web service application pool domain account as the ones that you are currently using.</span></span> <span data-ttu-id="a0157-108">Если вы не используете одни и те же значения, вы не сможете получить доступ к некоторым серверам.</span><span class="sxs-lookup"><span data-stu-id="a0157-108">If you don’t use the same values, you cannot access some of the servers.</span></span> <span data-ttu-id="a0157-109">Чтобы получить текущие значения, используйте командлет Windows PowerShell **Get-MbamWebApplication** .</span><span class="sxs-lookup"><span data-stu-id="a0157-109">To get the current values, use the **Get-MbamWebApplication** Windows PowerShell cmdlet.</span></span>

 

**<span data-ttu-id="a0157-110">Перемещение веб-сайта администрирования и мониторинга на другой сервер</span><span class="sxs-lookup"><span data-stu-id="a0157-110">To move the Administration and Monitoring Website to another server</span></span>**

1.  <span data-ttu-id="a0157-111">На сервере B Установите серверное программное обеспечение MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="a0157-111">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="a0157-112">Инструкции можно найти [в разделе Установка серверного программного обеспечения MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="a0157-112">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="a0157-113">На сервере B запустите мастер настройки сервера MBAM, выберите команду **Добавить новые функции**, а затем выберите только **веб-сайт администрирования и мониторинга** .</span><span class="sxs-lookup"><span data-stu-id="a0157-113">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Administration and Monitoring Website** feature.</span></span>

    <span data-ttu-id="a0157-114">Кроме того, вы можете использовать командлет Windows PowerShell **Enable-MbamWebApplication** , чтобы настроить веб-сайт администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="a0157-114">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="a0157-115">Инструкции по настройке веб-сайта администрирования и мониторинга приведены [в разделе Настройка веб-приложений MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="a0157-115">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

**<span data-ttu-id="a0157-116">Перемещение портала самообслуживания на другой сервер</span><span class="sxs-lookup"><span data-stu-id="a0157-116">To move the Self-Service Portal to another server</span></span>**

1.  <span data-ttu-id="a0157-117">На сервере B Установите серверное программное обеспечение MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="a0157-117">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="a0157-118">Инструкции можно найти [в разделе Установка серверного программного обеспечения MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="a0157-118">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="a0157-119">На сервере B запустите мастер настройки сервера MBAM, выберите команду **Добавить новые функции**и выберите только один из **порталов самообслуживания** .</span><span class="sxs-lookup"><span data-stu-id="a0157-119">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Self-Service Portal** feature.</span></span>

    <span data-ttu-id="a0157-120">Кроме того, можно использовать командлет Windows PowerShell **Enable-MbamWebApplication** , чтобы настроить портал самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="a0157-120">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Self-Service Portal.</span></span>

    <span data-ttu-id="a0157-121">Инструкции по настройке веб-сайта администрирования и мониторинга приведены [в разделе Настройка веб-приложений MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="a0157-121">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

3.  <span data-ttu-id="a0157-122">Если клиентские компьютеры в вашей организации не имеют доступа к сети доставки содержимого Майкрософт, вам также придется переместить файлы JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a0157-122">If the client computers in your organization do not have access to the Microsoft Content Delivery Network, you also have to move the JavaScript files.</span></span> <span data-ttu-id="a0157-123">Узнайте, [как настроить портал самообслуживания, когда клиентские компьютеры не могут получить доступ к сети доставки содержимого Майкрософт](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="a0157-123">See [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) for more information.</span></span>

4.  <span data-ttu-id="a0157-124">Настройте портал самообслуживания для своей организации.</span><span class="sxs-lookup"><span data-stu-id="a0157-124">Customize the Self-Service Portal for your organization.</span></span> <span data-ttu-id="a0157-125">Воспользуйтесь инструкциями, приведенными в разделе [Настройка портала самообслуживания для Организации](customizing-the-self-service-portal-for-your-organization.md) , чтобы просмотреть текущие настройки и настроить пользовательские параметры на портале самосервер на сервере B.</span><span class="sxs-lookup"><span data-stu-id="a0157-125">Use the instructions in [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md) to review your current customizations and to configure custom settings on the Self-Server Portal on Server B.</span></span>



## <span data-ttu-id="a0157-126">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a0157-126">Related topics</span></span>


[<span data-ttu-id="a0157-127">Настройка веб-приложений MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a0157-127">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="a0157-128">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a0157-128">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="a0157-129">Перенос компонентов MBAM 2.5 на другой сервер</span><span class="sxs-lookup"><span data-stu-id="a0157-129">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 

## <span data-ttu-id="a0157-130">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="a0157-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a0157-131">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="a0157-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a0157-132">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a0157-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





