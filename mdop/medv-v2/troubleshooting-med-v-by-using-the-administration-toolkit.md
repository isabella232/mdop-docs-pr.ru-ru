---
title: Устранение неполадок в работе MED-V с помощью набора средств администрирования
description: Устранение неполадок в работе MED-V с помощью набора средств администрирования
author: dansimp
ms.assetid: 6c096a1c-b9ce-4ec7-8dfd-5286e3b9a617
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1eaa493e5603e8a1275a6ff5f189739b168f319
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825372"
---
# <span data-ttu-id="69ff0-103">Устранение неполадок в работе MED-V с помощью набора средств администрирования</span><span class="sxs-lookup"><span data-stu-id="69ff0-103">Troubleshooting MED-V by Using the Administration Toolkit</span></span>


<span data-ttu-id="69ff0-104">С помощью средства администрирования MED-V вы можете устранить некоторые проблемы в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="69ff0-104">Use the MED-V Administration Toolkit to troubleshoot certain problems in a MED-V workspace.</span></span> <span data-ttu-id="69ff0-105">Набор средств администрирования для MED-V позволяет получать доступ к журналам событий и настраивать их, перезапускать или сбрасывать рабочую область MED-V, а также просматривать опубликованные приложения и перенаправленные веб-адреса в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="69ff0-105">The MED-V Administration Toolkit lets you access and configure event logs, restart or reset the MED-V workspace, and view the published applications and redirected web addresses in the MED-V workspace.</span></span> <span data-ttu-id="69ff0-106">Вы также можете использовать набор средств администрирования MED-V, чтобы открыть виртуальную машину рабочей области MED-V в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="69ff0-106">You can also use the MED-V Administration Toolkit to open the MED-V workspace virtual machine in full-screen mode.</span></span>

## <span data-ttu-id="69ff0-107">Открытие набора средств администрирования для MED-V</span><span class="sxs-lookup"><span data-stu-id="69ff0-107">To Open the MED-V Administration Toolkit</span></span>


<span data-ttu-id="69ff0-108">Чтобы открыть набор средств администрирования для MED-V, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="69ff0-108">Perform the following steps to open the MED-V Administration Toolkit:</span></span>

1.  <span data-ttu-id="69ff0-109">Откройте окно командной строки на главном компьютере, содержащем рабочую область MED-V, в которой вы хотите устранить неполадки.</span><span class="sxs-lookup"><span data-stu-id="69ff0-109">On the host computer that contains the MED-V workspace you are troubleshooting, open a Command Prompt window.</span></span>

2.  <span data-ttu-id="69ff0-110">Перейдите на%systemdrive%\\Program Files\\Microsoft предприятия виртуализация рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="69ff0-110">Browse to %systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization.</span></span>

3.  <span data-ttu-id="69ff0-111">В командной строке введите **MedvHost/Toolkit**.</span><span class="sxs-lookup"><span data-stu-id="69ff0-111">At the command prompt, type **MedvHost /toolkit**.</span></span>

<span data-ttu-id="69ff0-112">После открытия набора средств администрирования MED-V вы можете использовать его для устранения проблем, возникающих при устранении неполадок в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="69ff0-112">After the MED-V Administration Toolkit opens, you can use the toolkit to help resolve issues in the MED-V workspace found during troubleshooting.</span></span>

## <span data-ttu-id="69ff0-113">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="69ff0-113">In this Section</span></span>


<a href="" id="viewing-and-configuring-med-v-logs"></a>[<span data-ttu-id="69ff0-114">Просмотр и настройка журналов MED-V</span><span class="sxs-lookup"><span data-stu-id="69ff0-114">Viewing and Configuring MED-V Logs</span></span>](viewing-and-configuring-med-v-logs.md)  
<span data-ttu-id="69ff0-115">В этой статье описано, как использовать инструментарий администрирования MED-V для сбора журналов событий MED-V и управления ими на ведущем компьютере и гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="69ff0-115">Describes how to use the MED-V Administration Toolkit to collect and manage MED-V event logs in the host computer and the guest virtual machine.</span></span>

<a href="" id="restarting-and-resetting-a-med-v-workspace"></a>[<span data-ttu-id="69ff0-116">Перезапуск и сброс рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="69ff0-116">Restarting and Resetting a MED-V Workspace</span></span>](restarting-and-resetting-a-med-v-workspace.md)  
<span data-ttu-id="69ff0-117">В этой статье описано, как перезапустить и сбросить рабочие области MED-V с помощью средства администрирования MED-V.</span><span class="sxs-lookup"><span data-stu-id="69ff0-117">Describes how to restart and reset MED-V workspaces by using the MED-V Administration Toolkit.</span></span>

<a href="" id="viewing-med-v-workspace-configurations"></a>[<span data-ttu-id="69ff0-118">Просмотр конфигураций рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="69ff0-118">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)  
<span data-ttu-id="69ff0-119">В этой статье описано, как использовать инструментарий администрирования MED-V для просмотра опубликованных приложений и перенаправленных веб-адресов в рабочей области MED-V и открытия виртуальной машины MED-V Workspace в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="69ff0-119">Describes how to use the MED-V Administration Toolkit to view the published applications and redirected web addresses in a MED-V workspace and how to open the MED-V workspace virtual machine in full-screen mode.</span></span>

## <span data-ttu-id="69ff0-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="69ff0-120">Related topics</span></span>


[<span data-ttu-id="69ff0-121">Сообщения журнала событий MED-V</span><span class="sxs-lookup"><span data-stu-id="69ff0-121">MED-V Event Log Messages</span></span>](med-v-event-log-messages.md)

[<span data-ttu-id="69ff0-122">Устранение неполадок MED-V</span><span class="sxs-lookup"><span data-stu-id="69ff0-122">Troubleshooting MED-V</span></span>](troubleshooting-med-vmedv2.md)

 

 





