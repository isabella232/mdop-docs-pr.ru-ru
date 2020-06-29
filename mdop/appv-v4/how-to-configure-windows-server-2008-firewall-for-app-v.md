---
title: Настройка брандмауэра Windows Server 2008 для App-V
description: Настройка брандмауэра Windows Server 2008 для App-V
author: dansimp
ms.assetid: 57f4ed17-0651-4a3c-be1e-29d9520c6aeb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 19e4cda9ac3b908f68e4f69b9663033d8a21ae41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817719"
---
# <span data-ttu-id="b05fb-103">Настройка брандмауэра Windows Server 2008 для App-V</span><span class="sxs-lookup"><span data-stu-id="b05fb-103">How to Configure Windows Server 2008 Firewall for App-V</span></span>


<span data-ttu-id="b05fb-104">С появлением Windows Server2008 брандмауэр и компоненты IPsec были объединены в одну службу, и возможности этой службы были улучшены.</span><span class="sxs-lookup"><span data-stu-id="b05fb-104">With the introduction of Windows Server2008, the firewall and IPsec components were merged into one service, and the capabilities of this service were enhanced.</span></span> <span data-ttu-id="b05fb-105">Новая служба брандмауэра поддерживает входящие и исходящие проверки состояния.</span><span class="sxs-lookup"><span data-stu-id="b05fb-105">The new firewall service supports incoming and outgoing stateful inspection.</span></span> <span data-ttu-id="b05fb-106">Кроме того, вы можете настроить особые правила брандмауэра и политики IPsec с помощью групповых политик.</span><span class="sxs-lookup"><span data-stu-id="b05fb-106">Also, you can configure specific firewall rules and IPsec policies through group policies.</span></span> <span data-ttu-id="b05fb-107">Дополнительные сведения о брандмауэре Windows в Windows Server2008 можно найти в статьях <https://go.microsoft.com/fwlink/?LinkId=151980> .</span><span class="sxs-lookup"><span data-stu-id="b05fb-107">For additional information about the Windows firewall in Windows Server2008, see <https://go.microsoft.com/fwlink/?LinkId=151980>.</span></span>

<span data-ttu-id="b05fb-108">Описанные ниже действия не включают Добавление исключений для публикаций ICO и OSD с помощью протокола SMB или HTTP/HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b05fb-108">The following procedure does not include adding an exception for ICO and OSD publishing through SMB or HTTP/HTTPS.</span></span> <span data-ttu-id="b05fb-109">Эти исключения автоматически добавляются в соответствии с сетевым профилем и ролями, установленными на брандмауэре Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b05fb-109">Those exceptions are automatically added based on the network profile and roles installed on the Windows Server 2008 firewall.</span></span>

<span data-ttu-id="b05fb-110">**Примечание**  Если сервер управления настроен на использование RTSP, повторите эту процедуру, чтобы добавить программу в `sghwsvr.exe` качестве исключения.</span><span class="sxs-lookup"><span data-stu-id="b05fb-110">**Note** If the Management Server is configured to use RTSP, repeat this procedure to add the `sghwsvr.exe` program as an exception.</span></span>

<span data-ttu-id="b05fb-111">Потоковый сервер App-V требует исключений программы `sglwdsptr.exe` для связи с помощью RTSP.</span><span class="sxs-lookup"><span data-stu-id="b05fb-111">The App-V Streaming Server requires the program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="b05fb-112">Для потокового сервера App-V, использующего протокол RTSP для обмена информацией, также требуется программное исключение `sglwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="b05fb-112">An App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

 

**<span data-ttu-id="b05fb-113">Настройка брандмауэра Windows Server2008 для App-V</span><span class="sxs-lookup"><span data-stu-id="b05fb-113">To configure Windows Server2008 firewall for App-V</span></span>**

1.  <span data-ttu-id="b05fb-114">Откройте консоль " **Брандмауэр Windows" с** помощью панели управления "Расширенное управление безопасностью" или введите текст `wf.msc` в строке "выполнить".</span><span class="sxs-lookup"><span data-stu-id="b05fb-114">Open the **Windows Firewall with Advanced Security** management console through the Control Panel or by typing `wf.msc` on the Run line.</span></span>

2.  <span data-ttu-id="b05fb-115">Создайте новое правило для входящего подключения и выберите пункт **Программа**.</span><span class="sxs-lookup"><span data-stu-id="b05fb-115">Create a new inbound rule, and select **Program**.</span></span>

3.  <span data-ttu-id="b05fb-116">Выберите путь к программе и перейдите на него по `sghwdsptr.exe` умолчанию `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="b05fb-116">Select the program path, and browse to `sghwdsptr.exe`, which is located by default at `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

4.  <span data-ttu-id="b05fb-117">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b05fb-117">Click **Next**.</span></span>

5.  <span data-ttu-id="b05fb-118">На странице **действия** выберите **Разрешить подключение**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b05fb-118">On the **Action** page, select **Allow the connection**, and then click **Next**.</span></span>

6.  <span data-ttu-id="b05fb-119">Выберите нужные **Профили** , которые нужно применить к правилу для входящего трафика.</span><span class="sxs-lookup"><span data-stu-id="b05fb-119">Select the appropriate **Profiles** to apply to the inbound rule.</span></span>

7.  <span data-ttu-id="b05fb-120">Укажите имя и описание правила, а затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="b05fb-120">Provide a name and description for the rule, and click **Finish**.</span></span>

## <span data-ttu-id="b05fb-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b05fb-121">Related topics</span></span>


[<span data-ttu-id="b05fb-122">Настройка брандмауэра Windows Server 2003 для App-V</span><span class="sxs-lookup"><span data-stu-id="b05fb-122">How to Configure Windows Server 2003 Firewall for App-V</span></span>](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





