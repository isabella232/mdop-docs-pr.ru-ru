---
title: Применение параметров сети к рабочей области MED-V
description: Применение параметров сети к рабочей области MED-V
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826519"
---
# <span data-ttu-id="ac2d7-103">Применение параметров сети к рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="ac2d7-103">How to Apply Network Settings to a MED-V Workspace</span></span>


<span data-ttu-id="ac2d7-104">Администраторы могут задавать сетевые параметры для каждой рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-104">Administrators can define the network settings for each MED-V workspace.</span></span>

<span data-ttu-id="ac2d7-105">Все параметры сети настраиваются в модуле **политики** на вкладке **сеть** .</span><span class="sxs-lookup"><span data-stu-id="ac2d7-105">All network settings are configured in the **Policy** module, on the **Network** tab.</span></span>

**<span data-ttu-id="ac2d7-106">Применение параметров сети к рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="ac2d7-106">To apply network settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="ac2d7-107">Щелкните рабочую область MED-V, которую нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-107">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="ac2d7-108">В области **Network (сеть** ) настройте параметры, как описано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-108">In the **Network** pane, configure the settings as described in the following table.</span></span>

3.  <span data-ttu-id="ac2d7-109">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-109">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="ac2d7-110">Свойства сети для рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="ac2d7-110">MED-V Workspace Network Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ac2d7-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="ac2d7-111">Property</span></span></th>
<th align="left"><span data-ttu-id="ac2d7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ac2d7-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac2d7-113">Свойства TCP/IP</span><span class="sxs-lookup"><span data-stu-id="ac2d7-113">TCP/IP Properties</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="ac2d7-114">Использование IP-адреса узла (NAT) </strong> — Рабочая область будет использовать NAT для предоставления доступа к IP-адресу узла для исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-114">Use host's IP address (NAT)</strong>—The workspace will use NAT to share the host's IP for outgoing traffic.</span></span></p></li>
<li><p><strong><span data-ttu-id="ac2d7-115">Использовать IP-адрес, отличный от Host (мост) </strong> — Рабочая область MED-V будет иметь собственный сетевой адрес, обычно получаемый через DHCP.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-115">Use different IP address than host (Bridge)</strong>—The MED-V workspace will have its own network address, usually obtained via DHCP.</span></span></p></li>
</ul>
<p><span data-ttu-id="ac2d7-116">Установите <strong> флажок сопоставить несколько адаптеров с рабочей областью </strong> , когда на главном компьютере есть несколько адаптеров.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-116">Select the <strong>Map multiple adapters into Workspace</strong> check box when the host computer has multiple adapters.</span></span> <span data-ttu-id="ac2d7-117">Рекомендуется использовать эту конфигурацию, когда узел перемещается между различными сетями, использующими различные адаптеры.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-117">It is recommended to use this configuration when the host moves between different networks using different adapters.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac2d7-118">DNS-сервер</span><span class="sxs-lookup"><span data-stu-id="ac2d7-118">DNS Server</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="ac2d7-119">Не изменяйте </strong> — параметры DNS, заданные в виртуальной машине MED-V, не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-119">Don't change</strong>—DNS settings that are set within the MED-V workspace virtual machine will not be changed.</span></span></p></li>
<li><p><strong><span data-ttu-id="ac2d7-120">Использование DNS-адреса узла </strong> — параметры DNS для рабочей области MED-V будут синхронизированы в соответствии с параметрами узла.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-120">Use Host's DNS address</strong>—MED-V workspace DNS settings will be synchronized to match the host's settings.</span></span> <span data-ttu-id="ac2d7-121">Синхронизация DNS является динамической.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-121">The DNS synchronization is dynamic.</span></span> <span data-ttu-id="ac2d7-122">Оно периодически синхронизируется с основным приложением, так что если оно изменилось на узле, оно будет динамически изменено в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-122">It is synchronized periodically with the host so that if it is changed on the host, it will change dynamically in the MED-V workspace.</span></span></p></li>
<li><p><strong><span data-ttu-id="ac2d7-123">Использование определенных DNS-адресов </strong> : в рабочей области MED-V используется КОНКРЕТНЫЙ DNS, как указано.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-123">Use specific DNS addresses</strong>—The MED-V workspace will use a specific DNS, as specified.</span></span></p>
<p><span data-ttu-id="ac2d7-124">В <strong> полях основной </strong> и <strong> дополнительный </strong> введите основной и дополнительный DNS-адреса.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-124">In the <strong>Primary</strong> and <strong>Secondary</strong> fields, enter the primary and secondary DNS addresses.</span></span></p>
<p><span data-ttu-id="ac2d7-125">Установите <strong> флажок DNS-адреса узла добавления, </strong> чтобы добавить узел к НАСТРОЕННЫМ DNS-адресам.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-125">Select the <strong>Append Host's DNS addresses</strong> check box to append the host to the configured DNS addresses.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac2d7-126">Назначение суффиксов DNS</span><span class="sxs-lookup"><span data-stu-id="ac2d7-126">Assign DNS Suffixes</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="ac2d7-127">Назначьте следующие суффиксы </strong> : Установите этот флажок, чтобы назначить конкретные DNS-суффиксы; в поле введите суффикс или несколько суффиксов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-127">Assign the following suffixes</strong>—Select this check box to assign specific DNS suffixes; in the box, enter a suffix or multiple suffixes separated by commas.</span></span></p></li>
<li><p><strong><span data-ttu-id="ac2d7-128">Добавление суффиксов узлов </strong> — установите этот флажок, чтобы добавить суффиксы узлов в DNS-адрес.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-128">Append host suffixes</strong>—Select this check box to append the host suffixes to the DNS address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ac2d7-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ac2d7-129">Related topics</span></span>


[<span data-ttu-id="ac2d7-130">Создание рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="ac2d7-130">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="ac2d7-131">Использование пользовательского интерфейса консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="ac2d7-131">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





