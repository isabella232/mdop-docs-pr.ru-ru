---
title: Примеры конфигураций виртуальной машины
description: Примеры конфигураций виртуальной машины
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824589"
---
# <span data-ttu-id="cf601-103">Примеры конфигураций виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="cf601-103">Examples of Virtual Machine Configurations</span></span>


<span data-ttu-id="cf601-104">Ниже приведены примеры типичных конфигураций виртуальных машин: один в постоянной рабочей области MED-V и другой в рабочей области revertible MED-V.</span><span class="sxs-lookup"><span data-stu-id="cf601-104">The following are examples of typical virtual machine configurations: one in a persistent MED-V workspace and one in a revertible MED-V workspace.</span></span>

<span data-ttu-id="cf601-105">**Примечание**  Эти примеры не предназначены для использования во всех средах.</span><span class="sxs-lookup"><span data-stu-id="cf601-105">**Note** These examples are not intended for use in all environments.</span></span> <span data-ttu-id="cf601-106">Настройте конфигурацию в соответствии с вашей средой.</span><span class="sxs-lookup"><span data-stu-id="cf601-106">Adjust the configuration according to your environment.</span></span>

 

**<span data-ttu-id="cf601-107">Настройка типичной настройки домена в постоянной рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="cf601-107">To configure a typical domain setup in a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="cf601-108">Настройте Sysprep на базовом образе, чтобы создать уникальный ИД безопасности.</span><span class="sxs-lookup"><span data-stu-id="cf601-108">Configure Sysprep on the base image to create a unique SID.</span></span> <span data-ttu-id="cf601-109">Дополнительные сведения можно найти [в разделе Создание образа Virtual PC для MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span><span class="sxs-lookup"><span data-stu-id="cf601-109">For more information, see [Creating a Virtual PC Image for MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span></span>

2.  <span data-ttu-id="cf601-110">На вкладке **Настройка виртуальной машины** установите флажок **запустить настройку виртуальной машины** .</span><span class="sxs-lookup"><span data-stu-id="cf601-110">On the **VM Setup** tab, select the **Run VM Setup** check box.</span></span>

3.  <span data-ttu-id="cf601-111">В разделе **шаблон имени компьютера виртуальной машины** настройте шаблон для имени образа компьютера.</span><span class="sxs-lookup"><span data-stu-id="cf601-111">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="cf601-112">Дополнительные сведения [можно найти в разделе Настройка свойств шаблона имени компьютера виртуальной машины](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="cf601-112">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

4.  <span data-ttu-id="cf601-113">Нажмите кнопку **Редактор сценариев**и в диалоговом окне " **Редактор скриптов настройки виртуальной машины** " настройте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cf601-113">Click **Script Editor**, and in the **VM Setup Script Editor** dialog box, configure the following actions:</span></span>

    1.  **<span data-ttu-id="cf601-114">Переименование компьютера</span><span class="sxs-lookup"><span data-stu-id="cf601-114">Rename Computer</span></span>**

    2.  **<span data-ttu-id="cf601-115">Перезагрузка Windows</span><span class="sxs-lookup"><span data-stu-id="cf601-115">Restart Windows</span></span>**

    3.  **<span data-ttu-id="cf601-116">Проверка подключения</span><span class="sxs-lookup"><span data-stu-id="cf601-116">Check Connectivity</span></span>**

    4.  **<span data-ttu-id="cf601-117">Присоединение к домену</span><span class="sxs-lookup"><span data-stu-id="cf601-117">Join Domain</span></span>**

    5.  **<span data-ttu-id="cf601-118">Отключение автоматического входа</span><span class="sxs-lookup"><span data-stu-id="cf601-118">Disable Auto-Logon</span></span>**

    <span data-ttu-id="cf601-119">Дополнительные сведения [можно найти в разделе Настройка действий сценария](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="cf601-119">For more information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

5.  <span data-ttu-id="cf601-120">В меню **Политика** выберите команду **зафиксировать**.</span><span class="sxs-lookup"><span data-stu-id="cf601-120">On the **Policy** menu, click **Commit**.</span></span>

**<span data-ttu-id="cf601-121">Настройка типичной настройки в рабочей области revertible</span><span class="sxs-lookup"><span data-stu-id="cf601-121">To configure a typical setup in a revertible workspace</span></span>**

1.  <span data-ttu-id="cf601-122">На вкладке **Настройка виртуальной машины** установите флажок **Переименовать виртуальную машину на основе шаблона "имя компьютера** ".</span><span class="sxs-lookup"><span data-stu-id="cf601-122">On the **VM Setup** tab, select the **Rename the VM based on the computer name pattern** check box.</span></span>

2.  <span data-ttu-id="cf601-123">В разделе **шаблон имени компьютера виртуальной машины** настройте шаблон для имени образа компьютера.</span><span class="sxs-lookup"><span data-stu-id="cf601-123">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="cf601-124">Дополнительные сведения [можно найти в разделе Настройка свойств шаблона имени компьютера виртуальной машины](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="cf601-124">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

3.  <span data-ttu-id="cf601-125">В меню **Политика** выберите команду **зафиксировать**.</span><span class="sxs-lookup"><span data-stu-id="cf601-125">On the **Policy** menu, click **Commit**.</span></span>

## <span data-ttu-id="cf601-126">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="cf601-126">Related topics</span></span>


[<span data-ttu-id="cf601-127">Настройка параметров виртуальной машины для рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="cf601-127">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="cf601-128">Настройка свойств шаблона имени компьютера виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="cf601-128">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[<span data-ttu-id="cf601-129">Настройка действий сценариев</span><span class="sxs-lookup"><span data-stu-id="cf601-129">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

 

 





