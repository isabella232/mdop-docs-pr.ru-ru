---
title: Установка и настройка консоли управления App-V для организации более безопасной среды
description: Установка и настройка консоли управления App-V для организации более безопасной среды
author: dansimp
ms.assetid: 9d89ef09-cdbf-48fc-99da-b24fc987ef8f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9887787d1e203410b5517439d897260305d7526e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817372"
---
# <span data-ttu-id="b512b-103">Установка и настройка консоли управления App-V для организации более безопасной среды</span><span class="sxs-lookup"><span data-stu-id="b512b-103">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>


<span data-ttu-id="b512b-104">Установка консоли управления App-V по умолчанию включает поддержку безопасной связи.</span><span class="sxs-lookup"><span data-stu-id="b512b-104">The default installation of the App-V Management Console includes support for secure communications.</span></span> <span data-ttu-id="b512b-105">Каждая консоль управления настраивается отдельно для каждого подключения при запуске консоли в первый раз или при подключении к дополнительной службе веб-управления App-V.</span><span class="sxs-lookup"><span data-stu-id="b512b-105">Each Management Console is configured on a per-connection basis when the console is started for the first time or when connecting to an additional App-V Web Management Service.</span></span> <span data-ttu-id="b512b-106">Конфигурация по умолчанию использует SSL через TCP-порт 443.</span><span class="sxs-lookup"><span data-stu-id="b512b-106">The default configuration uses SSL over TCP port 443.</span></span> <span data-ttu-id="b512b-107">Вы можете изменить номер порта, если номер порта изменился на сервере.</span><span class="sxs-lookup"><span data-stu-id="b512b-107">You can change the port number if the port number was modified on the server.</span></span> <span data-ttu-id="b512b-108">Вы можете использовать описанную ниже процедуру, чтобы подключиться к службе веб-управления App-V с помощью безопасного соединения.</span><span class="sxs-lookup"><span data-stu-id="b512b-108">You can use the following procedure to connect to an App-V Web Management Service by using a secure connection.</span></span>

**<span data-ttu-id="b512b-109">Подключение к службе управления App-V с помощью соединения SSL</span><span class="sxs-lookup"><span data-stu-id="b512b-109">How to Connect to an App-V Management Service by Using an SSL Connection</span></span>**

1.  <span data-ttu-id="b512b-110">Запустите консоль управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="b512b-110">Start the Application Virtualization Management Console.</span></span>

2.  <span data-ttu-id="b512b-111">Нажмите кнопку **Настройка соединения** в области действия консоли.</span><span class="sxs-lookup"><span data-stu-id="b512b-111">Click **Configure Connection** in the actions pane of the console.</span></span>

3.  <span data-ttu-id="b512b-112">Введите **имя узла веб-службы**и установите флажок **использовать безопасное соединение** .</span><span class="sxs-lookup"><span data-stu-id="b512b-112">Type the **Web Service Host Name**, and ensure that **Use Secure Connection** is selected.</span></span>

    <span data-ttu-id="b512b-113">**Важно!**  Имя, указанное в имени узла веб-службы, должно совпадать с общим именем в сертификате, иначе соединение не будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="b512b-113">**Important** The name provided in the Web Service Host Name must match the common name on the certificate, or the connection will fail.</span></span>

     

4.  <span data-ttu-id="b512b-114">Выберите нужные учетные данные и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b512b-114">Select the appropriate login credentials, and click **OK**.</span></span>

## <span data-ttu-id="b512b-115">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b512b-115">Related topics</span></span>


[<span data-ttu-id="b512b-116">Настройка сертификатов для обеспечения поддержки службы веб-управления App-V</span><span class="sxs-lookup"><span data-stu-id="b512b-116">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)

 

 





