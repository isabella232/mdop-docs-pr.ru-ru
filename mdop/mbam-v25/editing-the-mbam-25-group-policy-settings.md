---
title: Изменение параметров групповой политики MBAM 2.5
description: Изменение параметров групповой политики MBAM 2.5
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812597"
---
# <span data-ttu-id="d37e7-103">Изменение параметров групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d37e7-103">Editing the MBAM 2.5 Group Policy Settings</span></span>


<span data-ttu-id="d37e7-104">Чтобы успешно развернуть администрирование и мониторинг Microsoft BitLocker (MBAM), необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d37e7-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d37e7-105">Задача</span><span class="sxs-lookup"><span data-stu-id="d37e7-105">Task</span></span></th>
<th align="left"><span data-ttu-id="d37e7-106">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="d37e7-106">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d37e7-107">Скопируйте шаблоны групповой политики MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="d37e7-107">Copy the MBAM 2.5 Group Policy Templates.</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="d37e7-108">Копирование шаблонов групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d37e7-108">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d37e7-109">Определите объекты групповой политики (GPO), которые вы хотите использовать в реализации MBAM.</span><span class="sxs-lookup"><span data-stu-id="d37e7-109">Determine which Group Policy Objects (GPOs) you want to use in your MBAM implementation.</span></span> <span data-ttu-id="d37e7-110">В зависимости от потребностей Организации может потребоваться настроить дополнительные параметры групповой политики.</span><span class="sxs-lookup"><span data-stu-id="d37e7-110">Based on the needs of your organization, you might have to configure additional Group Policy settings.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="d37e7-111">Планирование требований к групповой политике MBAM 2,5 </a> — включает в себя описания объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="d37e7-111">Planning for MBAM 2.5 Group Policy Requirements</a> – contains descriptions of the GPOs</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d37e7-112">Настройте параметры групповой политики для своей организации.</span><span class="sxs-lookup"><span data-stu-id="d37e7-112">Set the Group Policy settings for your organization.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d37e7-113">**Важно!**  Не изменяйте параметры групповой политики в разделе " **Шифрование диска BitLocker** " или MBAM будут работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="d37e7-113">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="d37e7-114">При настройке параметров групповой политики на узле **MDOP MBAM (Управление BitLocker)** MBAM автоматически настраивает параметры **шифрования диска для BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="d37e7-114">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="d37e7-115">Изменение параметров групповой политики клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="d37e7-115">To edit MBAM Client Group Policy settings</span></span>**

1.  <span data-ttu-id="d37e7-116">Убедитесь, что на компьютере, на котором установлены шаблоны групповой политики MBAM, включены службы MBAM Services.</span><span class="sxs-lookup"><span data-stu-id="d37e7-116">On a computer that has the MBAM Group Policy Templates installed, make sure that MBAM Services are enabled.</span></span>

2.  <span data-ttu-id="d37e7-117">С помощью консоли управления групповыми политиками (GPMC. msc) или расширенного управления групповыми политиками Майкрософт на компьютере с установленными шаблонами групповой политики MBAM выберите политики **конфигурации компьютера** : &gt; **Policies** &gt; **Административные шаблоны** &gt; **компоненты Windows** &gt; **MDOP MBAM (Управление BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="d37e7-117">Using the Group Policy Management Console (GPMC.msc) or the Microsoft Advanced Group Policy Management MDOP product on a computer with the MBAM Group Policy Templates installed, select **Computer configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="d37e7-118">Измените параметры групповой политики, необходимые для включения клиентских служб MBAM на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="d37e7-118">Edit the Group Policy settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="d37e7-119">Для каждой политики, описанной в следующей таблице, выберите **Группа политики**, выберите нужную **политику** и настройте параметры.</span><span class="sxs-lookup"><span data-stu-id="d37e7-119">For each policy in the following table, select **Policy Group**, click the **Policy** you want, and then configure the settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="d37e7-120">Группа политики</span><span class="sxs-lookup"><span data-stu-id="d37e7-120">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="d37e7-121">Политика</span><span class="sxs-lookup"><span data-stu-id="d37e7-121">Policy</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d37e7-122">Управление клиентами</span><span class="sxs-lookup"><span data-stu-id="d37e7-122">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d37e7-123">Настройка служб MBAM</span><span class="sxs-lookup"><span data-stu-id="d37e7-123">Configure MBAM Services</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d37e7-124">Диск операционной системы</span><span class="sxs-lookup"><span data-stu-id="d37e7-124">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d37e7-125">Параметры шифрования диска операционной системы</span><span class="sxs-lookup"><span data-stu-id="d37e7-125">Operating system drive encryption settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d37e7-126">Съемный диск</span><span class="sxs-lookup"><span data-stu-id="d37e7-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d37e7-127">Управление использованием BitLocker на съемных дисках</span><span class="sxs-lookup"><span data-stu-id="d37e7-127">Control use of BitLocker on removable drives</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d37e7-128">Несъемный диск</span><span class="sxs-lookup"><span data-stu-id="d37e7-128">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d37e7-129">Управление использованием BitLocker на съемных дисках</span><span class="sxs-lookup"><span data-stu-id="d37e7-129">Control use of BitLocker on fixed drives</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="d37e7-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d37e7-130">Related topics</span></span>


[<span data-ttu-id="d37e7-131">Планирование требований групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d37e7-131">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)

[<span data-ttu-id="d37e7-132">Копирование шаблонов групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d37e7-132">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

 
## <span data-ttu-id="d37e7-133">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="d37e7-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d37e7-134">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="d37e7-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d37e7-135">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="d37e7-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





