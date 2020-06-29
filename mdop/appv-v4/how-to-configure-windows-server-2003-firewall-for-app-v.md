---
title: Настройка брандмауэра Windows Server 2003 для App-V
description: Настройка брандмауэра Windows Server 2003 для App-V
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817729"
---
# <span data-ttu-id="aef9a-103">Настройка брандмауэра Windows Server 2003 для App-V</span><span class="sxs-lookup"><span data-stu-id="aef9a-103">How to Configure Windows Server 2003 Firewall for App-V</span></span>


<span data-ttu-id="aef9a-104">Чтобы настроить брандмауэр WindowsServer 2003 для App-V, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="aef9a-104">Use the following procedure to configure the WindowsServer 2003 firewall for App-V.</span></span>

**<span data-ttu-id="aef9a-105">Настройка брандмауэра WindowsServer 2003 для App-V</span><span class="sxs-lookup"><span data-stu-id="aef9a-105">To configure WindowsServer 2003 firewall for App-V</span></span>**

1.  <span data-ttu-id="aef9a-106">На **панели управления**откройте **Брандмауэр Windows**.</span><span class="sxs-lookup"><span data-stu-id="aef9a-106">In **Control Panel**, open the **Windows Firewall**.</span></span>

    <span data-ttu-id="aef9a-107">**Примечание**  Если сервер не настроен для запуска службы межсетевого экрана перед этим шагом, вам будет предложено запустить службу брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="aef9a-107">**Note** If the server has not been configured to run the firewall service before this step, you will be prompted to start the firewall service.</span></span>

     

2.  <span data-ttu-id="aef9a-108">Если файлы ICO и OSD публикуются по протоколу SMB, убедитесь, что на вкладке **исключения** разрешен **общий доступ к файлам и принтерам** .</span><span class="sxs-lookup"><span data-stu-id="aef9a-108">If ICO and OSD files are published through SMB, ensure that **File and Printer Sharing** is enabled on the **Exceptions** tab.</span></span>

    <span data-ttu-id="aef9a-109">**Примечание**  Если файлы ICO и OSD публикуются на сервере управления с помощью HTTP/HTTPS, возможно, потребуется добавить исключение для HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="aef9a-109">**Note** If ICO and OSD files are published through HTTP/HTTPS on the Management Server, you might need to add an exception for HTTP or HTTPS.</span></span> <span data-ttu-id="aef9a-110">Если сервер IIS, на котором размещены файлы ICO и OSD, размещается на компьютере, отличном от сервера управления, необходимо добавить на этот компьютер исключение.</span><span class="sxs-lookup"><span data-stu-id="aef9a-110">If the IIS server hosting the ICO and OSD files is hosted on a computer separate from the Management Server, you need to add the exception to that computer.</span></span> <span data-ttu-id="aef9a-111">Для повышения производительности рекомендуется размещать файлы ICO и OSD на отдельном сервере, отличном от сервера управления.</span><span class="sxs-lookup"><span data-stu-id="aef9a-111">To maximize performance, it is recommended that you host the ICO and OSD files on a separate server from the Management Server.</span></span>

     

3.  <span data-ttu-id="aef9a-112">Добавьте программное исключение `sghwdsptr.exe` , которое является исполняемым файлом службы сервера управления.</span><span class="sxs-lookup"><span data-stu-id="aef9a-112">Add a program exception for `sghwdsptr.exe`, which is the Management Server service executable.</span></span> <span data-ttu-id="aef9a-113">Путь по умолчанию к этому исполняемому файлу — `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="aef9a-113">The default path to this executable is `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

    <span data-ttu-id="aef9a-114">**Примечание**  Если сервер управления использует протокол RTSP для обмена данными, необходимо также добавить программное исключение `sghwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="aef9a-114">**Note** If the Management Server uses RTSP for communication, you must also add a program exception for `sghwsvr.exe`.</span></span>

    <span data-ttu-id="aef9a-115">Потоковый сервер App-V требует исключений программы `sglwdsptr.exe` для связи с помощью RTSP.</span><span class="sxs-lookup"><span data-stu-id="aef9a-115">The App-V Streaming Server requires a program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="aef9a-116">Для потокового сервера App-V, использующего протокол RTSP для обмена информацией, также требуется программное исключение `sglwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="aef9a-116">The App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

     

4.  <span data-ttu-id="aef9a-117">Убедитесь, что для каждого исключения настроена соответствующая область.</span><span class="sxs-lookup"><span data-stu-id="aef9a-117">Ensure that the proper scope is configured for each exception.</span></span> <span data-ttu-id="aef9a-118">Для снижения риска удалите все компьютеры и ограничьте IP-адреса, на которые будет отвечать сервер.</span><span class="sxs-lookup"><span data-stu-id="aef9a-118">To reduce risk, remove any computer and strictly limit the IP addresses to which the server will respond.</span></span>

## <span data-ttu-id="aef9a-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="aef9a-119">Related topics</span></span>


[<span data-ttu-id="aef9a-120">Настройка брандмауэра Windows Server 2008 для App-V</span><span class="sxs-lookup"><span data-stu-id="aef9a-120">How to Configure Windows Server 2008 Firewall for App-V</span></span>](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 





