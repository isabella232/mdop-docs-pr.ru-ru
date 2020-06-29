---
title: Настройка системы безопасности сервера управления после установки
description: Настройка системы безопасности сервера управления после установки
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817939"
---
# <span data-ttu-id="08d3c-103">Настройка системы безопасности сервера управления после установки</span><span class="sxs-lookup"><span data-stu-id="08d3c-103">How to Configure Management Server Security Post-Installation</span></span>


<span data-ttu-id="08d3c-104">С помощью консоли управления App-V добавьте сертификат и настройте сервер управления App-V для усиления безопасности.</span><span class="sxs-lookup"><span data-stu-id="08d3c-104">Use the App-V Management Console to add the certificate and configure the App-V Management Server for enhanced security.</span></span> <span data-ttu-id="08d3c-105">Вы можете использовать описанную ниже процедуру, чтобы настроить параметры безопасности после установки.</span><span class="sxs-lookup"><span data-stu-id="08d3c-105">You can use the following procedure to configure security post-installation.</span></span>

**<span data-ttu-id="08d3c-106">Настройка системы безопасности сервера управления после установки</span><span class="sxs-lookup"><span data-stu-id="08d3c-106">To configure Management Server security post-installation</span></span>**

1.  <span data-ttu-id="08d3c-107">Откройте консоль управления App-V и подключитесь к **службе управления** с правами администратора App-v.</span><span class="sxs-lookup"><span data-stu-id="08d3c-107">Open the App-V Management Console, and connect to the **Management Service** with App-V administrator privileges.</span></span>

2.  <span data-ttu-id="08d3c-108">Разверните сервер, разверните группу **серверов**, а затем выберите соответствующую группу серверов, с которой был зарегистрирован сервер управления.</span><span class="sxs-lookup"><span data-stu-id="08d3c-108">Expand the server, expand **Server Groups**, and then select the appropriate server group with which the Management Server was registered.</span></span>

3.  <span data-ttu-id="08d3c-109">Щелкните объект сервера управления правой кнопкой мыши и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="08d3c-109">Right-click the Management Server object, and select **Properties**.</span></span>

4.  <span data-ttu-id="08d3c-110">На вкладке " **порты** " выберите " **сертификат сервера** " и завершите работу мастера для выбора надежного сертификата.</span><span class="sxs-lookup"><span data-stu-id="08d3c-110">On the **Ports** tab, click **Server Certificate** and complete the wizard to select the properly provisioned certificate.</span></span>

    <span data-ttu-id="08d3c-111">**Примечание**  Если в мастере не отображаются сертификаты, значит сертификат не подготовлен или сертификат не отвечает требованиям приложения-V.</span><span class="sxs-lookup"><span data-stu-id="08d3c-111">**Note** If no certificates are displayed in the wizard, a certificate has not been provisioned or the certificate does meet the requirements of App-V.</span></span>

     

5.  <span data-ttu-id="08d3c-112">Нажмите кнопку **Далее** , чтобы перейти к странице " **Добро пожаловать в мастер сертификатов** ".</span><span class="sxs-lookup"><span data-stu-id="08d3c-112">Click **Next** to continue on to the **Welcome To Certificate Wizard** page.</span></span>

6.  <span data-ttu-id="08d3c-113">Выберите правильный сертификат на экране **Доступные сертификаты** .</span><span class="sxs-lookup"><span data-stu-id="08d3c-113">Select the correct certificate in the **Available Certificates** screen.</span></span>

7.  <span data-ttu-id="08d3c-114">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="08d3c-114">Click **Finish**.</span></span>

8.  <span data-ttu-id="08d3c-115">После завершения работы мастера Удалите протокол **RTSP** в качестве доступного порта для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="08d3c-115">After completing the wizard, clear **RTSP** as an available listening port.</span></span> <span data-ttu-id="08d3c-116">Это предотвратит подключение к небезопасному каналу связи.</span><span class="sxs-lookup"><span data-stu-id="08d3c-116">This prevents connections from being made over a non-secure communication channel.</span></span>

9.  <span data-ttu-id="08d3c-117">Нажмите кнопку **Применить**и перезапустите службу **виртуального сервера приложений Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="08d3c-117">Click **Apply**, and restart the **Microsoft Virtual Application Server** service.</span></span> <span data-ttu-id="08d3c-118">Для выполнения этой задачи используйте оснастку MMC службы.</span><span class="sxs-lookup"><span data-stu-id="08d3c-118">Use the service’s MMC snap-in to accomplish this task.</span></span>

## <span data-ttu-id="08d3c-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="08d3c-119">Related topics</span></span>


[<span data-ttu-id="08d3c-120">Настройка системы безопасности сервера потоковой передачи после установки</span><span class="sxs-lookup"><span data-stu-id="08d3c-120">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)

[<span data-ttu-id="08d3c-121">Устранение проблем с разрешениями сертификатов</span><span class="sxs-lookup"><span data-stu-id="08d3c-121">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





