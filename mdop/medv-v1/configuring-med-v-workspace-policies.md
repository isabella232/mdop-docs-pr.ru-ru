---
title: Настройка политик рабочей области MED-V
description: Настройка политик рабочей области MED-V
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824859"
---
# <span data-ttu-id="1ba7b-103">Настройка политик рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="1ba7b-103">Configuring MED-V Workspace Policies</span></span>


<span data-ttu-id="1ba7b-104">Политика рабочей области MED-V — это группа настраиваемых параметров, определяющих способ выполнения виртуализированной среды и приложений на хост-компьютере.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-104">A MED-V workspace policy is a group of configurable settings that define how the virtualized environment and applications perform on the host machine.</span></span> <span data-ttu-id="1ba7b-105">В этом разделе описаны все настраиваемые параметры в политике рабочей области для MED-V и параметры, влияющие на рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-105">The topics in this section describe all the configurable settings in the MED-V workspace policy as well as how these settings influence the MED-V workspace.</span></span>

<span data-ttu-id="1ba7b-106">Доступны следующие типы рабочих областей MED-V:</span><span class="sxs-lookup"><span data-stu-id="1ba7b-106">The following MED-V workspace types are available:</span></span>

-   <span data-ttu-id="1ba7b-107">**Persistent**— в постоянной рабочей области MED-v все изменения и дополнения, внесенные пользователем в рабочую область MED-v, сохраняются в рабочей области MED-v между сеансами.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-107">**Persistent**—In a persistent MED-V workspace, all changes and additions the user makes to the MED-V workspace are saved in the MED-V workspace between sessions.</span></span> <span data-ttu-id="1ba7b-108">Кроме того, постоянная рабочая область MED-V обычно используется в среде домена.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-108">Additionally, a persistent MED-V workspace is generally used in a domain environment.</span></span>

-   <span data-ttu-id="1ba7b-109">**Revertible**— в рабочей области Revertible med-v по завершении каждого сеанса (то есть при остановке рабочей области MED-v) при развертывании восстанавливается исходное состояние рабочей области MED-v.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-109">**Revertible**—In a revertible MED-V workspace, at the completion of each session (that is, when the MED-V workspace is stopped), the MED-V workspace reverts to its original state during deployment.</span></span> <span data-ttu-id="1ba7b-110">Изменения и дополнения, внесенные пользователем, сохраняются в рабочей области MED-V между сеансами.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-110">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span> <span data-ttu-id="1ba7b-111">Рабочую область revertible MED-V нельзя использовать в среде домена.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-111">A revertible MED-V workspace cannot be used in a domain environment.</span></span>

<span data-ttu-id="1ba7b-112">Важно выбрать тип рабочей области MED-V, которую вы создаете, прежде чем развертывать рабочую область MED-V, так как не рекомендуется перенастраивать тип рабочей области MED-V после развертывания политики для пользователей.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-112">It is important to decide on the type of MED-V workspace you are creating before deploying the MED-V workspace, because it is not recommended to reconfigure the type of MED-V workspace after a policy has been deployed to users.</span></span>

<span data-ttu-id="1ba7b-113">**Примечание**  При настройке политики рядом с полями обязательных полей, которые не заполнены, появляется предупреждающий символ.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-113">**Note** When configuring a policy, a warning symbol appears next to mandatory fields that are not filled in.</span></span> <span data-ttu-id="1ba7b-114">Если обязательное поле не заполнено, на вкладке также отображается символ.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-114">If a mandatory field is not filled in, the symbol appears on the tab as well.</span></span>

 

## <span data-ttu-id="1ba7b-115">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="1ba7b-115">In This Section</span></span>


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="1ba7b-116">Применение общих параметров к рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="1ba7b-116">How to Apply General Settings to a MED-V Workspace</span></span>](how-to-apply-general-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="1ba7b-117">В этой статье описаны общие параметры рабочей области MED-V и способы их применения к политике.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-117">Describes the general settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="1ba7b-118">Применение параметров виртуальной машины к рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="1ba7b-118">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="1ba7b-119">Описание параметров виртуальной машины для рабочей области MED-V и инструкции по его применению к политике.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-119">Describes the virtual machine settings for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[<span data-ttu-id="1ba7b-120">Настройка пользователя или группы домена</span><span class="sxs-lookup"><span data-stu-id="1ba7b-120">How to Configure a Domain User or Group</span></span>](how-to-configure-a-domain-user-or-groupmedvv2.md)  
<span data-ttu-id="1ba7b-121">В этой статье описано, как настроить пользователей и группы домена.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-121">Describes how to configure domain users and groups.</span></span>

<a href="" id="how-to-configure-published-applications"></a>[<span data-ttu-id="1ba7b-122">Настройка опубликованных приложений</span><span class="sxs-lookup"><span data-stu-id="1ba7b-122">How to Configure Published Applications</span></span>](how-to-configure-published-applicationsmedvv2.md)  
<span data-ttu-id="1ba7b-123">В этой статье описаны опубликованные приложения и меню, а также способы их применения к политике.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-123">Describes published applications and menus, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[<span data-ttu-id="1ba7b-124">Настройка веб-параметров для рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="1ba7b-124">How to Configure Web Settings for a MED-V Workspace</span></span>](how-to-configure-web-settings-for-a-med-v-workspace.md)  
<span data-ttu-id="1ba7b-125">В этой статье описаны веб-параметры, доступные для рабочей области MED-V, и способы их применения к политике.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-125">Describes the Web settings available for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[<span data-ttu-id="1ba7b-126">Настройка параметров виртуальной машины для рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="1ba7b-126">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
<span data-ttu-id="1ba7b-127">Описание настройки виртуальной машины для рабочей области MED-V и инструкции по ее применению к политике.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-127">Describes the virtual machine setup for a MED-V workspace, and how to apply it to a policy.</span></span>

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="1ba7b-128">Применение параметров сети к рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="1ba7b-128">How to Apply Network Settings to a MED-V Workspace</span></span>](how-to-apply-network-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="1ba7b-129">В этой статье описаны сетевые параметры рабочей области MED-V и способы их применения к политике.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-129">Describes the network settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="1ba7b-130">Применение параметров производительности к рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="1ba7b-130">How to Apply Performance Settings to a MED-V Workspace</span></span>](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="1ba7b-131">В этой статье описаны параметры производительности рабочей области MED-V и способы их применения к политике.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-131">Describes the performance settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-import-and-export-a-policy"></a>[<span data-ttu-id="1ba7b-132">Импорт и экспорт политики</span><span class="sxs-lookup"><span data-stu-id="1ba7b-132">How to Import and Export a Policy</span></span>](how-to-import-and-export-a-policy.md)  
<span data-ttu-id="1ba7b-133">Инструкции по импорту и экспорту политики.</span><span class="sxs-lookup"><span data-stu-id="1ba7b-133">Describes how to import and export a policy.</span></span>

 

 





