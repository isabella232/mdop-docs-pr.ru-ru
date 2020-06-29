---
title: Изменение параметров объектов групповой политики MBAM 2.0
description: Изменение параметров объектов групповой политики MBAM 2.0
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824089"
---
# <span data-ttu-id="c1df3-103">Изменение параметров объектов групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c1df3-103">How to Edit MBAM 2.0 GPO Settings</span></span>


<span data-ttu-id="c1df3-104">Чтобы успешно развернуть администрирование и мониторинг Microsoft BitLocker (MBAM), необходимо сначала определить групповые политики, которые будут использоваться при реализации администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c1df3-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="c1df3-105">Более подробную информацию о различных доступных политиках можно найти в разделе [планирование MBAM 2,0 с учетом требований к групповой политике](planning-for-mbam-20-group-policy-requirements-mbam-2.md) .</span><span class="sxs-lookup"><span data-stu-id="c1df3-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="c1df3-106">Определив политики, которые вы собираетесь использовать, необходимо изменить один или несколько объектов групповой политики (GPO), которые содержат параметры политики для MBAM.</span><span class="sxs-lookup"><span data-stu-id="c1df3-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the policy settings for MBAM.</span></span>

<span data-ttu-id="c1df3-107">Чтобы настроить основные и рекомендуемые параметры GPO, выполните указанные ниже действия, чтобы включить MBAM для управления шифрованием BitLocker на клиентских компьютерах организации.</span><span class="sxs-lookup"><span data-stu-id="c1df3-107">You can use the following steps to configure the basic, recommended GPO settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="c1df3-108">Изменение параметров объекта групповой политики клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="c1df3-108">To Edit MBAM Client GPO Settings</span></span>**

1.  <span data-ttu-id="c1df3-109">На компьютере, на котором установлен шаблон групповой политики MBAM, убедитесь в том, что службы MBAM включены.</span><span class="sxs-lookup"><span data-stu-id="c1df3-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="c1df3-110">С помощью консоли управления групповыми политиками (GPMC. msc) или расширенного продукта MDOP на компьютере с установленным шаблоном групповой политики MBAM выберите **Конфигурация компьютера**, выберите пункт **политики**, щелкните **Административные шаблоны**, выберите пункт **компоненты Windows**и нажмите кнопку **MDOP MBAM (Управление BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="c1df3-110">Using the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product on a computer with the MBAM Group Policy template installed, select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="c1df3-111">Измените параметры объекта групповой политики, необходимые для включения клиентских служб MBAM на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="c1df3-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="c1df3-112">Для каждой политики в приведенной ниже таблице выберите **Группа политики**, щелкните **политику**и настройте **параметр**.</span><span class="sxs-lookup"><span data-stu-id="c1df3-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c1df3-113">Группа политики</span><span class="sxs-lookup"><span data-stu-id="c1df3-113">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="c1df3-114">Политика</span><span class="sxs-lookup"><span data-stu-id="c1df3-114">Policy</span></span></th>
    <th align="left"><span data-ttu-id="c1df3-115">Параметр</span><span class="sxs-lookup"><span data-stu-id="c1df3-115">Setting</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c1df3-116">Управление клиентами</span><span class="sxs-lookup"><span data-stu-id="c1df3-116">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c1df3-117">Настройка служб MBAM</span><span class="sxs-lookup"><span data-stu-id="c1df3-117">Configure MBAM Services</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c1df3-118">Включено.</span><span class="sxs-lookup"><span data-stu-id="c1df3-118">Enabled.</span></span> <span data-ttu-id="c1df3-119">Настройте <strong> конечную точку для восстановления MBAM и службы оборудования </strong> и <strong> выберите данные восстановления BitLocker для хранения </strong> .</span><span class="sxs-lookup"><span data-stu-id="c1df3-119">Set <strong>MBAM Recovery and Hardware service endpoint</strong> and <strong>Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="c1df3-120">Установите <strong> конечную точку службы соответствия MBAM </strong> и введите частоту отчета о состоянии (в минутах).</span><span class="sxs-lookup"><span data-stu-id="c1df3-120">Set <strong>MBAM compliance service endpoint</strong> and Enter status report frequency in (minutes).</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c1df3-121">Диск операционной системы</span><span class="sxs-lookup"><span data-stu-id="c1df3-121">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c1df3-122">Параметры шифрования диска операционной системы</span><span class="sxs-lookup"><span data-stu-id="c1df3-122">Operating system drive encryption settings</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c1df3-123">Включено.</span><span class="sxs-lookup"><span data-stu-id="c1df3-123">Enabled.</span></span> <span data-ttu-id="c1df3-124">Установите <strong> переключатель выбрать предохранитель для диска операционной системы </strong> .</span><span class="sxs-lookup"><span data-stu-id="c1df3-124">Set <strong>Select protector for operating system drive</strong>.</span></span> <span data-ttu-id="c1df3-125">Требуется для сохранения данных на диске операционной системы на сервере восстановления MBAMKey.</span><span class="sxs-lookup"><span data-stu-id="c1df3-125">Required to save operating system drive data to the MBAMKey Recovery server.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c1df3-126">Съемный диск</span><span class="sxs-lookup"><span data-stu-id="c1df3-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c1df3-127">Управление использованием BitLocker на съемных дисках</span><span class="sxs-lookup"><span data-stu-id="c1df3-127">Control Use of BitLocker on removable drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c1df3-128">Включено.</span><span class="sxs-lookup"><span data-stu-id="c1df3-128">Enabled.</span></span> <span data-ttu-id="c1df3-129">Обязательно, если MBAM сохранит съемные данные на сервере восстановления ключа MBAM.</span><span class="sxs-lookup"><span data-stu-id="c1df3-129">Required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c1df3-130">Несъемный диск</span><span class="sxs-lookup"><span data-stu-id="c1df3-130">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c1df3-131">Управление использованием BitLocker на съемных дисках</span><span class="sxs-lookup"><span data-stu-id="c1df3-131">Control Use of BitLocker on fixed drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c1df3-132">Включено.</span><span class="sxs-lookup"><span data-stu-id="c1df3-132">Enabled.</span></span> <span data-ttu-id="c1df3-133">Обязательно, если MBAM сохранит данные фиксированного диска на сервере восстановления ключа MBAM.</span><span class="sxs-lookup"><span data-stu-id="c1df3-133">Required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span></p>
    <p><span data-ttu-id="c1df3-134">Укажите <strong> , как можно восстановить диски, защищенные с помощью BitLocker </strong> , и <strong> разрешите агент восстановления данных </strong> .</span><span class="sxs-lookup"><span data-stu-id="c1df3-134">Set <strong>Choose how BitLocker-protected drives can be recovered</strong> and <strong>Allow data recovery agent</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="c1df3-135">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c1df3-135">Related topics</span></span>


[<span data-ttu-id="c1df3-136">Развертывание объектов групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c1df3-136">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)









