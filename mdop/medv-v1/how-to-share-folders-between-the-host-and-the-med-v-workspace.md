---
title: Предоставление общего доступа к папкам для узла и рабочей области MED-V
description: Предоставление общего доступа к папкам для узла и рабочей области MED-V
author: dansimp
ms.assetid: 3cb295f2-c07e-4ee6-aa3c-ce4c8c45c191
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87f315c9894cd38834413d2549e652a36c5cc16d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825752"
---
# <span data-ttu-id="3ca99-103">Предоставление общего доступа к папкам для узла и рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="3ca99-103">How to Share Folders Between the Host and the MED-V Workspace</span></span>


<span data-ttu-id="3ca99-104">Вы можете предоставлять общий доступ к папкам между узлом и рабочей областью MED-V.</span><span class="sxs-lookup"><span data-stu-id="3ca99-104">You can share folders between the host and the MED-V workspace.</span></span> <span data-ttu-id="3ca99-105">Общие папки можно хранить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3ca99-105">The shared folders can be stored on the following:</span></span>

-   <span data-ttu-id="3ca99-106">Внешний компьютер в сети</span><span class="sxs-lookup"><span data-stu-id="3ca99-106">An external computer on the network</span></span>

-   <span data-ttu-id="3ca99-107">Главный компьютер</span><span class="sxs-lookup"><span data-stu-id="3ca99-107">The host computer</span></span>

<span data-ttu-id="3ca99-108">Ниже описано, как предоставлять общий доступ к папкам между узлом и рабочей областью MED-V.</span><span class="sxs-lookup"><span data-stu-id="3ca99-108">The following procedures demonstrate how to share folders between the host and the MED-V workspace.</span></span>

**<span data-ttu-id="3ca99-109">Предоставление общего доступа к папкам, находящимся в сети</span><span class="sxs-lookup"><span data-stu-id="3ca99-109">To share folders located on the network</span></span>**

1.  <span data-ttu-id="3ca99-110">Настройте MED-V в режиме полного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="3ca99-110">Configure MED-V in full desktop mode.</span></span>

2.  <span data-ttu-id="3ca99-111">В разделе Управление MED-V на вкладке Сеть щелкните **использовать IP-адрес, отличный от узла Host (мост)**.</span><span class="sxs-lookup"><span data-stu-id="3ca99-111">In MED-V management, on the Network tab, click **Use different IP address than host (Bridge)**.</span></span>

3.  <span data-ttu-id="3ca99-112">На главном компьютере выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3ca99-112">Do the following on the host computer:</span></span>

    1.  <span data-ttu-id="3ca99-113">**На панели**управления выберите пункт **Просмотр состояния сети и задачи**, а затем — параметр **Обнаружение сети** .</span><span class="sxs-lookup"><span data-stu-id="3ca99-113">In Control Panel, click **View network status and tasks**, and set **Network discovery** to **On**.</span></span>

    2.  <span data-ttu-id="3ca99-114">В меню "Пуск" щелкните правой кнопкой мыши пункт **компьютер**и выберите пункт **Подключить сетевой диск**.</span><span class="sxs-lookup"><span data-stu-id="3ca99-114">On the Start menu, right-click **Computer**, and click **Map network drive**.</span></span>

    3.  <span data-ttu-id="3ca99-115">В диалоговом окне **Подключить сетевой диск** в поле **диск** выберите диск.</span><span class="sxs-lookup"><span data-stu-id="3ca99-115">In the **Map Network Drive** dialog box, in the **Drive** field, select a drive.</span></span>

        <span data-ttu-id="3ca99-116">**Примечание**  Убедитесь, что на обоих компьютерах не используется одна и та же буква диска.</span><span class="sxs-lookup"><span data-stu-id="3ca99-116">**Note** Ensure that the same drive letter is not in use on both computers.</span></span>

         

    4.  <span data-ttu-id="3ca99-117">Нажмите кнопку **Browse**.</span><span class="sxs-lookup"><span data-stu-id="3ca99-117">Click **Browse**.</span></span>

    5.  <span data-ttu-id="3ca99-118">В диалоговом окне **Поиск папки** перейдите к общему диску и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3ca99-118">In the **Browse For Folder** dialog box, browse to the shared drive, and click **OK**.</span></span>

    6.  <span data-ttu-id="3ca99-119">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="3ca99-119">Click **Finish**.</span></span>

4.  <span data-ttu-id="3ca99-120">Повторите шаг 3 в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="3ca99-120">Repeat step 3 in the MED-V workspace.</span></span> <span data-ttu-id="3ca99-121">Наведите указатель на тот же диск, что и на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3ca99-121">Point to the same drive as on the host computer.</span></span>

**<span data-ttu-id="3ca99-122">Предоставление общего доступа к папкам, размещенным на узле</span><span class="sxs-lookup"><span data-stu-id="3ca99-122">To share folders located on the host</span></span>**

1.  <span data-ttu-id="3ca99-123">Настройте общий доступ к папке с необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="3ca99-123">Configure the folder to be shared with the appropriate permissions.</span></span>

2.  <span data-ttu-id="3ca99-124">В рабочей области MED-V перейдите в раздел **Мое сетевое окружение** и найдите общую папку.</span><span class="sxs-lookup"><span data-stu-id="3ca99-124">From the MED-V workspace, go to **My network places** and locate the shared folder.</span></span>

3.  <span data-ttu-id="3ca99-125">В рабочей области MED-V найдите общую папку.</span><span class="sxs-lookup"><span data-stu-id="3ca99-125">From the MED-V workspace, locate the shared folder.</span></span>

<span data-ttu-id="3ca99-126">**Примечание**  Убедитесь в том, что компьютеры с основным и ведущим рабочими областями находятся в одном домене или рабочей группе.</span><span class="sxs-lookup"><span data-stu-id="3ca99-126">**Note** Ensure that both the host and MED-V workspace computers are in the same domain or workgroup.</span></span>

 

 

 





