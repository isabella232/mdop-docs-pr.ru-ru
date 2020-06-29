---
title: Изменение параметров объектов групповой политики MBAM 1.0
description: Изменение параметров объектов групповой политики MBAM 1.0
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824282"
---
# <span data-ttu-id="19b2c-103">Изменение параметров объектов групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="19b2c-103">How to Edit MBAM 1.0 GPO Settings</span></span>


<span data-ttu-id="19b2c-104">Чтобы успешно развернуть администрирование и мониторинг Microsoft BitLocker (MBAM), необходимо сначала определить групповые политики, которые будут использоваться при реализации администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="19b2c-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="19b2c-105">Более подробную информацию о различных доступных политиках можно найти в разделе [планирование для MBAM 1,0, предъявляемых групповой политикой](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="19b2c-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="19b2c-106">После определения политик, которые вы собираетесь использовать, необходимо изменить один или несколько объектов групповой политики (GPO), которые содержат параметры политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="19b2c-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the MBAM policy settings.</span></span>

<span data-ttu-id="19b2c-107">Ниже описаны действия, которые необходимо выполнить, чтобы настроить основные и рекомендуемые параметры объектов групповой политики (GPO), чтобы разрешить MBAM управлять шифрованием BitLocker для клиентских компьютеров организации.</span><span class="sxs-lookup"><span data-stu-id="19b2c-107">The following steps describe how to configure the basic, recommended Group Policy object (GPO) settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="19b2c-108">Изменение параметров объекта групповой политики клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="19b2c-108">To edit the MBAM Client GPO settings</span></span>**

1.  <span data-ttu-id="19b2c-109">На компьютере, на котором установлен шаблон групповой политики MBAM, убедитесь в том, что службы MBAM включены.</span><span class="sxs-lookup"><span data-stu-id="19b2c-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="19b2c-110">С помощью консоли управления групповыми политиками (GPMC. msc) или расширенной программы для управления групповыми политиками (для Windows) MDOP выполните указанные ниже действия. Выберите **Конфигурация компьютера**, выберите пункт **политики**, щелкните **Административные шаблоны**, выберите пункт **компоненты Windows**, а затем — пакет **MDOP MBAM (Управление BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="19b2c-110">Use the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product for these actions: Select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="19b2c-111">Измените параметры объекта групповой политики, необходимые для включения клиентских служб MBAM на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="19b2c-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="19b2c-112">Для каждой политики в приведенной ниже таблице выберите **Группа политики**, щелкните **политику**и настройте **параметр**.</span><span class="sxs-lookup"><span data-stu-id="19b2c-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**.</span></span>

    <span data-ttu-id="19b2c-113">Группа политики</span><span class="sxs-lookup"><span data-stu-id="19b2c-113">Policy Group</span></span>

    <span data-ttu-id="19b2c-114">Политика</span><span class="sxs-lookup"><span data-stu-id="19b2c-114">Policy</span></span>

    <span data-ttu-id="19b2c-115">Параметр</span><span class="sxs-lookup"><span data-stu-id="19b2c-115">Setting</span></span>

    <span data-ttu-id="19b2c-116">Управление клиентами</span><span class="sxs-lookup"><span data-stu-id="19b2c-116">Client Management</span></span>

    <span data-ttu-id="19b2c-117">Настройка служб MBAM</span><span class="sxs-lookup"><span data-stu-id="19b2c-117">Configure MBAM Services</span></span>

    <span data-ttu-id="19b2c-118">Включено.</span><span class="sxs-lookup"><span data-stu-id="19b2c-118">Enabled.</span></span> <span data-ttu-id="19b2c-119">Настройте **конечную точку для восстановления MBAM и службы оборудования** и **выберите данные восстановления BitLocker для хранения**.</span><span class="sxs-lookup"><span data-stu-id="19b2c-119">Set **MBAM Recovery and Hardware service endpoint** and **Select BitLocker recovery information to store**.</span></span>

    <span data-ttu-id="19b2c-120">Установите **конечную точку службы соответствия MBAM** и **Введите частоту отчета о состоянии (в минутах)**.</span><span class="sxs-lookup"><span data-stu-id="19b2c-120">Set **MBAM compliance service endpoint** and **Enter status report frequency in (minutes)**.</span></span>

    <span data-ttu-id="19b2c-121">Разрешение проверки совместимости оборудования</span><span class="sxs-lookup"><span data-stu-id="19b2c-121">Allow hardware compatibility checking</span></span>

    <span data-ttu-id="19b2c-122">Служба отключена.</span><span class="sxs-lookup"><span data-stu-id="19b2c-122">Disabled.</span></span> <span data-ttu-id="19b2c-123">Эта политика включена по умолчанию, но не требуется для базовой реализации MBAM.</span><span class="sxs-lookup"><span data-stu-id="19b2c-123">This policy is enabled by default, but is not needed for a basic MBAM implementation.</span></span>

    <span data-ttu-id="19b2c-124">Диск операционной системы</span><span class="sxs-lookup"><span data-stu-id="19b2c-124">Operating System Drive</span></span>

    <span data-ttu-id="19b2c-125">Параметры шифрования диска операционной системы</span><span class="sxs-lookup"><span data-stu-id="19b2c-125">Operating system drive encryption settings</span></span>

    <span data-ttu-id="19b2c-126">Включено.</span><span class="sxs-lookup"><span data-stu-id="19b2c-126">Enabled.</span></span> <span data-ttu-id="19b2c-127">Установите **переключатель выбрать предохранитель для диска операционной системы**.</span><span class="sxs-lookup"><span data-stu-id="19b2c-127">Set **Select protector for operating system drive**.</span></span> <span data-ttu-id="19b2c-128">Это необходимо для сохранения данных на диске операционной системы на сервере восстановления ключа MBAM.</span><span class="sxs-lookup"><span data-stu-id="19b2c-128">This is required to save operating system drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="19b2c-129">Съемный диск</span><span class="sxs-lookup"><span data-stu-id="19b2c-129">Removable Drive</span></span>

    <span data-ttu-id="19b2c-130">Управление использованием BitLocker на съемных дисках</span><span class="sxs-lookup"><span data-stu-id="19b2c-130">Control Use of BitLocker on removable drives</span></span>

    <span data-ttu-id="19b2c-131">Включено.</span><span class="sxs-lookup"><span data-stu-id="19b2c-131">Enabled.</span></span> <span data-ttu-id="19b2c-132">Это необходимо, если MBAM сохранит съемные данные на сервере восстановления ключа MBAM.</span><span class="sxs-lookup"><span data-stu-id="19b2c-132">This is required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="19b2c-133">Несъемный диск</span><span class="sxs-lookup"><span data-stu-id="19b2c-133">Fixed Drive</span></span>

    <span data-ttu-id="19b2c-134">Управление использованием BitLocker на съемных дисках</span><span class="sxs-lookup"><span data-stu-id="19b2c-134">Control Use of BitLocker on fixed drives</span></span>

    <span data-ttu-id="19b2c-135">Включено.</span><span class="sxs-lookup"><span data-stu-id="19b2c-135">Enabled.</span></span> <span data-ttu-id="19b2c-136">Это необходимо, если MBAM сохранит данные фиксированного диска на сервере восстановления ключа MBAM.</span><span class="sxs-lookup"><span data-stu-id="19b2c-136">This is required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="19b2c-137">Укажите, **как можно восстановить диски, защищенные с помощью BitLocker** , и **разрешите агент восстановления данных**.</span><span class="sxs-lookup"><span data-stu-id="19b2c-137">Set **Choose how BitLocker-protected drives can be recovered** and **Allow data recovery agent**.</span></span>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="19b2c-138">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="19b2c-138">Related topics</span></span>


[<span data-ttu-id="19b2c-139">Развертывание объектов групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="19b2c-139">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)









