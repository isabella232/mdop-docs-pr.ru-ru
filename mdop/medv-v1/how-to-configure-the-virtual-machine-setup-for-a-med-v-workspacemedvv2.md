---
title: Настройка параметров виртуальной машины для рабочей области MED-V
description: Настройка параметров виртуальной машины для рабочей области MED-V
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827072"
---
# <span data-ttu-id="4fc3a-103">Настройка параметров виртуальной машины для рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="4fc3a-103">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>


<span data-ttu-id="4fc3a-104">Все параметры конфигурации настройки виртуальной машины настраиваются в модуле **политики** на вкладке " **Настройка виртуальной** машины".</span><span class="sxs-lookup"><span data-stu-id="4fc3a-104">All virtual machine setup configuration settings are configured in the **Policy** module, on the **VM Setup** tab.</span></span>

## <span data-ttu-id="4fc3a-105">Настройка параметров виртуальной машины для постоянной рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="4fc3a-105">How to Configure the Virtual Machine Setup for a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="4fc3a-106">Настройка настройки виртуальной машины для постоянной рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="4fc3a-106">To configure the virtual machine setup for a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="4fc3a-107">Щелкните постоянную рабочую область MED-V, которую нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-107">Click a persistent MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="4fc3a-108">В разделе **Постоянная настройка виртуальной машины** настройте свойства, как описано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-108">In the **Persistent VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="4fc3a-109">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-109">Note</span></span>**  
    <span data-ttu-id="4fc3a-110">Параметры постоянной настройки виртуальной машины включены только для постоянной рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-110">The persistent VM setup properties are enabled only for a persistent MED-V workspace.</span></span>



3.  <span data-ttu-id="4fc3a-111">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-111">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="4fc3a-112">Свойства настройки постоянной виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="4fc3a-112">Persistent VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4fc3a-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="4fc3a-113">Property</span></span></th>
<th align="left"><span data-ttu-id="4fc3a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4fc3a-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4fc3a-115">Запуск настройки виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="4fc3a-115">Run VM Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="4fc3a-116">Установите этот флажок, чтобы запустить сценарий настройки при первом запуске рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-116">Select this check box to run a setup script the first time the MED-V workspace is run.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4fc3a-117">Редактор сценариев</span><span class="sxs-lookup"><span data-stu-id="4fc3a-117">Script Editor</span></span></p></td>
<td align="left"><p><span data-ttu-id="4fc3a-118">Щелкните, чтобы настроить сценарий настройки.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-118">Click to configure the setup script.</span></span> <span data-ttu-id="4fc3a-119">Дополнительные сведения <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> можно найти в разделе Настройка действий сценария </a> .</span><span class="sxs-lookup"><span data-stu-id="4fc3a-119">For more information, see <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)">How to Set Up Script Actions</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4fc3a-120">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-120">Note</span></span></strong><br/><p><span data-ttu-id="4fc3a-121">Эта кнопка доступна только в том случае <strong> , если выбран параметр запустить сценарий настройки ВМ </strong> .</span><span class="sxs-lookup"><span data-stu-id="4fc3a-121">This button is enabled only when <strong>Run VM Setup script</strong> is selected.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4fc3a-122">Сообщение, отображаемое при запуске сценария</span><span class="sxs-lookup"><span data-stu-id="4fc3a-122">Message displayed when script is running</span></span></p></td>
<td align="left"><p><span data-ttu-id="4fc3a-123">Сообщение, которое будет отображаться при выполнении сценария.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-123">A message to be displayed while the script is running.</span></span> <span data-ttu-id="4fc3a-124">Если оставить это поле пустым, появится сообщение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-124">If left blank, the default message is displayed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4fc3a-125">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-125">Note</span></span></strong><br/><p><span data-ttu-id="4fc3a-126">Это поле доступно только в том случае <strong> , если установлен флажок Запустить сценарий настройки ВМ </strong> .</span><span class="sxs-lookup"><span data-stu-id="4fc3a-126">This field is enabled only when <strong>Run VM Setup script</strong> is checked.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4fc3a-127">Настройка параметров виртуальной машины для рабочей Revertible MED-V</span><span class="sxs-lookup"><span data-stu-id="4fc3a-127">How to Configure the Virtual Machine Setup for a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="4fc3a-128">Настройка настройки виртуальной машины для рабочей области revertible MED-V</span><span class="sxs-lookup"><span data-stu-id="4fc3a-128">To configure the virtual machine setup for a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="4fc3a-129">Щелкните рабочую область revertible MED-V для настройки.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-129">Click a revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="4fc3a-130">В разделе **Настройка виртуальной машины Revertible** настройте свойства, как описано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-130">In the **Revertible VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="4fc3a-131">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-131">Note</span></span>**  
    <span data-ttu-id="4fc3a-132">Параметры настройки виртуальной машины revertible включены только для рабочей области revertible MED-V.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-132">The revertible VM setup properties are enabled only for a revertible MED-V workspace.</span></span>



3.  <span data-ttu-id="4fc3a-133">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-133">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="4fc3a-134">Свойства настройки виртуальной машины Revertible</span><span class="sxs-lookup"><span data-stu-id="4fc3a-134">Revertible VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4fc3a-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="4fc3a-135">Property</span></span></th>
<th align="left"><span data-ttu-id="4fc3a-136">Описание</span><span class="sxs-lookup"><span data-stu-id="4fc3a-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4fc3a-137">Переименование виртуальной машины на основе шаблона имени компьютера</span><span class="sxs-lookup"><span data-stu-id="4fc3a-137">Rename the VM based on the computer name pattern</span></span></p></td>
<td align="left"><p><span data-ttu-id="4fc3a-138">Установите этот флажок, чтобы назначить каждому компьютеру уникальное имя с помощью рабочей области MED-V, чтобы можно было различать несколько компьютеров с помощью одной и той же рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="4fc3a-138">Select this check box to assign a unique name to each computer using the MED-V workspace so that you can differentiate between multiple computers using the same MED-V workspace.</span></span></p>
<p><span data-ttu-id="4fc3a-139">Дополнительные сведения о настройке имен компьютеров можно найти в разделе <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> Настройка свойств шаблона имени компьютера виртуальной машины </a> .</span><span class="sxs-lookup"><span data-stu-id="4fc3a-139">For more information on configuring computer image names, see <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)">How to Configure VM Computer Name Pattern Properties</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4fc3a-140">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4fc3a-140">Related topics</span></span>


[<span data-ttu-id="4fc3a-141">Использование пользовательского интерфейса консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="4fc3a-141">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="4fc3a-142">Создание рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="4fc3a-142">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="4fc3a-143">Примеры конфигураций виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="4fc3a-143">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









