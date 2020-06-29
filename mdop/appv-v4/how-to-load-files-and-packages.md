---
title: Загрузка файлов и пакетов
description: Загрузка файлов и пакетов
author: dansimp
ms.assetid: f86f5bf1-99a4-44d7-ae2f-e6049c482f68
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9427fd8089ec9c22d7d379b15ae94bf421ca2d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817239"
---
# <span data-ttu-id="db3de-103">Загрузка файлов и пакетов</span><span class="sxs-lookup"><span data-stu-id="db3de-103">How to Load Files and Packages</span></span>


<span data-ttu-id="db3de-104">Вы можете использовать описанную ниже процедуру для загрузки файлов и пакетов на серверах Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="db3de-104">You can use the following procedure to load files and packages on Application Virtualization Servers.</span></span>

<span data-ttu-id="db3de-105">**Примечание**  В процессе установки вы указали расположение каталога \\Content на странице **путь содержимого** .</span><span class="sxs-lookup"><span data-stu-id="db3de-105">**Note** During the installation process, you specified the location of the \\Content directory on the **Content Path** page.</span></span> <span data-ttu-id="db3de-106">Этот каталог нужно создать и настроить как стандартный файловый ресурс, прежде чем указывать на его расположение.</span><span class="sxs-lookup"><span data-stu-id="db3de-106">This directory should be created and configured as a standard file share before you point to its location.</span></span>

 

**<span data-ttu-id="db3de-107">Загрузка файлов и пакетов</span><span class="sxs-lookup"><span data-stu-id="db3de-107">To load files and packages</span></span>**

1.  <span data-ttu-id="db3de-108">На компьютере, с которого вы хотите передавать приложения, перейдите в расположение, указанное для каталога \\Content.</span><span class="sxs-lookup"><span data-stu-id="db3de-108">On the computer from which you will stream applications, navigate to the location that you specified for the \\Content directory.</span></span> <span data-ttu-id="db3de-109">При необходимости создайте каталог и настройте его в виде стандартной общей папки.</span><span class="sxs-lookup"><span data-stu-id="db3de-109">If necessary, create the directory and configure it as a standard file share.</span></span>

2.  <span data-ttu-id="db3de-110">Переместите файлы SFT для виртуальных приложений и пакетов в каталог \\Content.</span><span class="sxs-lookup"><span data-stu-id="db3de-110">Move the SFT files for the virtual applications and packages to the \\Content directory.</span></span> <span data-ttu-id="db3de-111">Чтобы сохранить структуру SFT файлов и избежать путаницы, разместите приложения и пакеты в выделенных вложенных папках.</span><span class="sxs-lookup"><span data-stu-id="db3de-111">To keep the SFT files organized and to avoid confusion, put applications and packages in dedicated subfolders.</span></span>

3.  <span data-ttu-id="db3de-112">Загрузите приложения и пакеты в соответствии с требованиями вашего сценария и конфигурации, учитывая указанные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="db3de-112">Load the applications and packages according to the requirements of your scenario and configuration, considering the following conditions:</span></span>

    -   <span data-ttu-id="db3de-113">Если приложения и пакеты хранятся на сервере Application Virtualization (App-V) Management Server, загрузите их с помощью консоли управления.</span><span class="sxs-lookup"><span data-stu-id="db3de-113">If your applications and packages are stored on an Application Virtualization (App-V) Management Server, load them through the Management Console.</span></span> <span data-ttu-id="db3de-114">Дополнительные сведения можно найти [в разделе как загрузить или выгрузить приложение](how-to-load-or-unload-an-application.md) или [загрузить виртуальные приложения из области уведомлений на рабочем столе](how-to-load-virtual-applications-from-the-desktop-notification-area.md).</span><span class="sxs-lookup"><span data-stu-id="db3de-114">For more information, see [How to Load or Unload an Application](how-to-load-or-unload-an-application.md) or [How to Load Virtual Applications from the Desktop Notification Area](how-to-load-virtual-applications-from-the-desktop-notification-area.md).</span></span>

    -   <span data-ttu-id="db3de-115">Если ваши приложения хранятся на сервере потоковой передачи App-V, веб-сервере или компьютере, настроенном как файловый сервер, эти приложения можно загрузить автоматически.</span><span class="sxs-lookup"><span data-stu-id="db3de-115">If your applications are stored on an App-V Streaming Server, a Web server, or a computer configured as a file server, the applications can be automatically loaded.</span></span>

        <span data-ttu-id="db3de-116">**Примечание**  Потоковый сервер App-V автоматически опрашивает каталог \\Content для приложений и пакетов и помещает эти данные в запросы приложений обслуживания в память.</span><span class="sxs-lookup"><span data-stu-id="db3de-116">**Note** The App-V Streaming Server automatically polls the \\Content directory for applications and packages and puts this information in RAM to service application requests.</span></span>

        <span data-ttu-id="db3de-117">Клиенты App-V должны быть правильно настроены для извлечения приложений и пакетов с веб-серверов и файловых серверов.</span><span class="sxs-lookup"><span data-stu-id="db3de-117">The App-V Clients must be properly configured to retrieve applications and packages from Web servers and file servers.</span></span> <span data-ttu-id="db3de-118">Дополнительные сведения можно найти [в разделе Настройка клиента для извлечения пакета приложения](how-to-configure-the-client-for-application-package-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="db3de-118">For more information, see [How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md).</span></span>

         

## <span data-ttu-id="db3de-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="db3de-119">Related topics</span></span>


[<span data-ttu-id="db3de-120">Сервер Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="db3de-120">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





