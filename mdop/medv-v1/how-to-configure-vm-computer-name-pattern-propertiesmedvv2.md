---
title: Настройка свойств шаблона имени компьютера виртуальной машины
description: Настройка свойств шаблона имени компьютера виртуальной машины
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827079"
---
# <span data-ttu-id="d3668-103">Настройка свойств шаблона имени компьютера виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d3668-103">How to Configure VM Computer Name Pattern Properties</span></span>


<span data-ttu-id="d3668-104">Шаблон имени компьютера виртуальной машины может быть назначен для revertible и для постоянных рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="d3668-104">A virtual machine computer name pattern can be assigned both for revertible and for persistent MED-V workspaces.</span></span>

-   <span data-ttu-id="d3668-105">Revertible — администраторы могут назначать уникальное имя каждому экземпляру рабочей области Revertible MED-V для различения нескольких компьютеров с помощью одной и той же рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="d3668-105">Revertible—Administrators can assign a unique name to each revertible MED-V workspace instance to differentiate between multiple computers using the same MED-V workspace.</span></span>

-   <span data-ttu-id="d3668-106">Persistent — в постоянной рабочей области MED-V администраторы могут настроить компьютер для переименования во время выполнения сценария настройки.</span><span class="sxs-lookup"><span data-stu-id="d3668-106">Persistent—In a persistent MED-V workspace, administrators can set a computer to be renamed during a setup script.</span></span>

## <span data-ttu-id="d3668-107">Назначение шаблона имени компьютера виртуальной машины в рабочую область Revertible MED-V</span><span class="sxs-lookup"><span data-stu-id="d3668-107">How to Assign a Virtual Machine Computer Name Pattern to a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="d3668-108">Назначение шаблона имени компьютера виртуальной машины в рабочую область revertible MED-V</span><span class="sxs-lookup"><span data-stu-id="d3668-108">To assign a virtual machine computer name pattern to a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="d3668-109">Щелкните рабочую область revertible MED-V для настройки.</span><span class="sxs-lookup"><span data-stu-id="d3668-109">Click the revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="d3668-110">В разделе **Настройка виртуальной машины Revertible** выберите **ПЕРЕИМЕНОВАНие виртуальной машины на основе шаблона "имя компьютера** ".</span><span class="sxs-lookup"><span data-stu-id="d3668-110">In the **Revertible VM Setup** section, select the **Rename the VM based on the computer name pattern** check box.</span></span>

3.  <span data-ttu-id="d3668-111">В разделе **шаблон имени компьютера виртуальной** машины введите шаблон, который будет использоваться для именования образов виртуальных машин, используя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="d3668-111">In the **VM Computer Name Pattern** section, enter the pattern to use for naming virtual machine images, using the following options:</span></span>

    -   <span data-ttu-id="d3668-112">**Constant (константа**) — введите произвольный текст, который будет постоянным на всех компьютерах, использующих рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="d3668-112">**Constant**—Enter free text that will be constant on all computers using the MED-V workspace.</span></span>

    -   <span data-ttu-id="d3668-113">**Переменная**— введите переменную, нажав кнопку **Вставить переменную**и выбрав один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="d3668-113">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="d3668-114">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="d3668-114">User name</span></span>**

        -   **<span data-ttu-id="d3668-115">Доменное имя</span><span class="sxs-lookup"><span data-stu-id="d3668-115">Domain name</span></span>**

        -   **<span data-ttu-id="d3668-116">Имя узла</span><span class="sxs-lookup"><span data-stu-id="d3668-116">Host name</span></span>**

        -   **<span data-ttu-id="d3668-117">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="d3668-117">Workspace name</span></span>**

        -   **<span data-ttu-id="d3668-118">Имя виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d3668-118">Virtual machine name</span></span>**

        <span data-ttu-id="d3668-119">Выбранная Вами переменная будет определена для компьютера с помощью рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="d3668-119">The variable selected will be specific to the computer using the MED-V workspace.</span></span> <span data-ttu-id="d3668-120">Например, если выбрано **имя домена** , уникальное имя каждого компьютера будет содержать доменное имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="d3668-120">For example, if **Domain name** is selected, the unique name for each computer will include the computer's domain name.</span></span>

    -   <span data-ttu-id="d3668-121">**Случайные символы**— введите "\ #" для каждого случайного символа, который нужно включить в шаблон.</span><span class="sxs-lookup"><span data-stu-id="d3668-121">**Random characters**—Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="d3668-122">Каждый компьютер, использующий рабочую область MED-V, имеет суффикс указанной длины, который генерируется случайным образом.</span><span class="sxs-lookup"><span data-stu-id="d3668-122">Each computer using the MED-V workspace will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="d3668-123">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d3668-123">Note</span></span>**  
    <span data-ttu-id="d3668-124">Длина имени компьютера ограничена 15 символами.</span><span class="sxs-lookup"><span data-stu-id="d3668-124">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="d3668-125">Если шаблон превышает предельное значение, оно будет усечено.</span><span class="sxs-lookup"><span data-stu-id="d3668-125">If the pattern exceeds the limit, it will be truncated.</span></span>



4.  <span data-ttu-id="d3668-126">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d3668-126">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="d3668-127">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d3668-127">Note</span></span>**  
    <span data-ttu-id="d3668-128">Шаблон имени компьютера виртуальной машины revertible можно назначить только в том случае, если вы **переименуете VM на основе шаблонов имен компьютеров** (в разделе **Настройка revertible VM** ).</span><span class="sxs-lookup"><span data-stu-id="d3668-128">A revertible VM computer name pattern can be assigned only when **Rename the VM based on the computer name patterns** (in the **Revertible VM Setup** section) is checked.</span></span>



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## <span data-ttu-id="d3668-129">Назначение шаблона имени компьютера виртуальной машины сохраняемой рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="d3668-129">How to Assign a Virtual Machine Computer Name Pattern to a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="d3668-130">Назначение шаблона имени компьютера виртуальной машины сохраняемой рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="d3668-130">To assign a virtual machine computer name pattern to a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="d3668-131">Щелкните постоянную рабочую область MED-V, чтобы настроить ее.</span><span class="sxs-lookup"><span data-stu-id="d3668-131">Click the persistent MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="d3668-132">В разделе **Постоянная настройка виртуальной машины** нажмите кнопку **Редактор скриптов**.</span><span class="sxs-lookup"><span data-stu-id="d3668-132">In the **Persistent VM Setup** section, click **Script Editor**.</span></span>

3.  <span data-ttu-id="d3668-133">В диалоговом окне **действия со сценарием** нажмите кнопку **Добавить**, а затем в подменю выберите команду **переименовать компьютер**.</span><span class="sxs-lookup"><span data-stu-id="d3668-133">In the **Script Actions** dialog box, click **Add**, and on the submenu, click **Rename Computer**.</span></span>

4.  <span data-ttu-id="d3668-134">Нажмите кнопку **ОК** , чтобы закрыть диалоговое окно **действия со сценарием** .</span><span class="sxs-lookup"><span data-stu-id="d3668-134">Click **OK** to close the **Script Actions** dialog box.</span></span>

5.  <span data-ttu-id="d3668-135">На вкладке **Настройка виртуальной машины** в разделе **шаблон имени компьютера виртуальной машины** введите шаблон, который будет использоваться для переименования компьютера, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d3668-135">On the **VM Setup** tab, in the **VM Computer Name Pattern** section, enter the pattern to use for renaming the computer, using the following:</span></span>

    -   <span data-ttu-id="d3668-136">**Constant (константа**) — введите произвольный текст, который будет включен в имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="d3668-136">**Constant**— Enter free text that will be included in the computer name.</span></span>

    -   <span data-ttu-id="d3668-137">**Переменная**— введите переменную, нажав кнопку **Вставить переменную**и выбрав один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="d3668-137">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="d3668-138">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="d3668-138">User name</span></span>**

        -   **<span data-ttu-id="d3668-139">Доменное имя</span><span class="sxs-lookup"><span data-stu-id="d3668-139">Domain name</span></span>**

        -   **<span data-ttu-id="d3668-140">Имя узла</span><span class="sxs-lookup"><span data-stu-id="d3668-140">Host name</span></span>**

        -   **<span data-ttu-id="d3668-141">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="d3668-141">Workspace name</span></span>**

        -   **<span data-ttu-id="d3668-142">Имя виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d3668-142">Virtual machine name</span></span>**

        <span data-ttu-id="d3668-143">Выбранная переменная будет определена для переименованного компьютера.</span><span class="sxs-lookup"><span data-stu-id="d3668-143">The variable selected will be specific to the computer that is being renamed.</span></span> <span data-ttu-id="d3668-144">Например, если выбрано **имя домена** , имя компьютера будет включать доменное имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="d3668-144">For example, if **Domain name** is selected, the computer name will include the computer's domain name.</span></span>

    -   <span data-ttu-id="d3668-145">**Случайные символы**— введите "\ #" для каждого случайного символа, который нужно включить в шаблон.</span><span class="sxs-lookup"><span data-stu-id="d3668-145">**Random characters**— Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="d3668-146">У компьютера будет суффикс указанной длины, который генерируется случайным образом.</span><span class="sxs-lookup"><span data-stu-id="d3668-146">The computer will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="d3668-147">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d3668-147">Note</span></span>**  
    <span data-ttu-id="d3668-148">Длина имени компьютера ограничена 15 символами.</span><span class="sxs-lookup"><span data-stu-id="d3668-148">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="d3668-149">Если шаблон превышает предельное значение, оно будет усечено.</span><span class="sxs-lookup"><span data-stu-id="d3668-149">If the pattern exceeds the limit, it will be truncated.</span></span>



6.  <span data-ttu-id="d3668-150">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d3668-150">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="d3668-151">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d3668-151">Note</span></span>**  
    <span data-ttu-id="d3668-152">Переименование компьютера будет выполняться только в том случае, если оно задано в качестве действия в диалоговом окне **действия со сценарием** .</span><span class="sxs-lookup"><span data-stu-id="d3668-152">The computer will be renamed only if it is set as an action in the **Script Actions** dialog box.</span></span> <span data-ttu-id="d3668-153">Подробные сведения можно найти [в разделе Настройка действий сценария](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d3668-153">For detailed information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>



## <span data-ttu-id="d3668-154">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d3668-154">Related topics</span></span>


[<span data-ttu-id="d3668-155">Использование пользовательского интерфейса консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="d3668-155">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="d3668-156">Создание рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="d3668-156">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="d3668-157">Настройка действий сценариев</span><span class="sxs-lookup"><span data-stu-id="d3668-157">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

[<span data-ttu-id="d3668-158">Примеры конфигураций виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d3668-158">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









