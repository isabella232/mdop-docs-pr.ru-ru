---
title: Настройка пользователя или группы домена
description: Настройка пользователя или группы домена
author: dansimp
ms.assetid: 055aba81-a9c9-4b98-969d-775e603becf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c51da13808df657c1341572767c24860d9d5e8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827199"
---
# <span data-ttu-id="e2883-103">Настройка пользователя или группы домена</span><span class="sxs-lookup"><span data-stu-id="e2883-103">How to Configure a Domain User or Group</span></span>


<span data-ttu-id="e2883-104">С помощью параметров развертывания можно управлять тем, какие пользователи или группы могут получать доступ к рабочей области MED-V, а также как долго использовать рабочую область MED-V и может ли она работать в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="e2883-104">The deployment settings enable you to control which users or groups can access the MED-V workspace, as well as how long the MED-V workspace can be utilized and whether it can be used offline.</span></span> <span data-ttu-id="e2883-105">Вы также можете настроить дополнительные правила для управления доступом между рабочей областью MED-V и узлом.</span><span class="sxs-lookup"><span data-stu-id="e2883-105">You can also configure additional rules to control access between the MED-V workspace and the host.</span></span>

<span data-ttu-id="e2883-106">Все разрешения рабочей области для MED-V настраиваются в модуле **политики** на вкладке " **развертывание** ".</span><span class="sxs-lookup"><span data-stu-id="e2883-106">All MED-V workspace permissions are configured in the **Policy** module, on the **Deployment** tab.</span></span>

<span data-ttu-id="e2883-107">Чтобы разрешить пользователям использовать рабочую область MED-V, необходимо сначала добавить пользователей домена или группы в разрешения рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="e2883-107">To allow users to utilize the MED-V workspace, you must first add domain users or groups to the MED-V workspace permissions.</span></span> <span data-ttu-id="e2883-108">Затем вы можете настроить разрешения для каждого пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="e2883-108">You can then set permissions for each user or group.</span></span>

## <span data-ttu-id="e2883-109">Как добавить пользователя или группу домена</span><span class="sxs-lookup"><span data-stu-id="e2883-109">How to Add a Domain User or Group</span></span>


**<span data-ttu-id="e2883-110">Добавление пользователя или группы домена</span><span class="sxs-lookup"><span data-stu-id="e2883-110">To add a domain user or group</span></span>**

1.  <span data-ttu-id="e2883-111">В окне **Пользователи/группы** нажмите кнопку **Добавить.**</span><span class="sxs-lookup"><span data-stu-id="e2883-111">In the **Users / Groups** window, click **Add.**</span></span>

2.  <span data-ttu-id="e2883-112">В диалоговом окне **Ввод имен пользователей или групп** выберите пункт Пользователи домена или группы, выполнив одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="e2883-112">In the **Enter User or Group names** dialog box, select domain users or groups by doing one of the following:</span></span>

    -   <span data-ttu-id="e2883-113">В поле **Введите имена пользователей или групп** введите пользователя или группу, которые есть в домене или в качестве локальных пользователей или групп на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e2883-113">In the **Enter User or Group names** field, type a user or group that exists in the domain or as a local user or group on the computer.</span></span> <span data-ttu-id="e2883-114">Затем нажмите кнопку **Проверить имена** , чтобы сопоставить их с полностью существующим именем.</span><span class="sxs-lookup"><span data-stu-id="e2883-114">Then click **Check Names** to resolve it to the full existent name.</span></span>

    -   <span data-ttu-id="e2883-115">Нажмите кнопку **найти** , чтобы открыть диалоговое окно Стандартный **Выбор пользователей или групп** .</span><span class="sxs-lookup"><span data-stu-id="e2883-115">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="e2883-116">Затем выберите пункт Пользователи домена или группы.</span><span class="sxs-lookup"><span data-stu-id="e2883-116">Then select domain users or groups.</span></span>

3.  <span data-ttu-id="e2883-117">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e2883-117">Click **OK**.</span></span>

    <span data-ttu-id="e2883-118">Добавляются пользователи домена или группы.</span><span class="sxs-lookup"><span data-stu-id="e2883-118">The domain users or groups are added.</span></span>

    **<span data-ttu-id="e2883-119">Примечание.</span><span class="sxs-lookup"><span data-stu-id="e2883-119">Note</span></span>**  
    <span data-ttu-id="e2883-120">Пользователи из доверенных доменов следует добавлять вручную.</span><span class="sxs-lookup"><span data-stu-id="e2883-120">Users from trusted domains should be added manually.</span></span>



~~~
**Warning**  
Do not run the management application from a computer that is part of a domain that is not trusted by the domain the server is installed on.
~~~



## <span data-ttu-id="e2883-121">Удаление пользователя или группы домена</span><span class="sxs-lookup"><span data-stu-id="e2883-121">How to Remove a Domain User or Group</span></span>


**<span data-ttu-id="e2883-122">Удаление пользователя или группы домена</span><span class="sxs-lookup"><span data-stu-id="e2883-122">To remove a domain user or group</span></span>**

1.  <span data-ttu-id="e2883-123">В окне **Пользователи/группы** выберите пользователя или группу.</span><span class="sxs-lookup"><span data-stu-id="e2883-123">In the **Users / Groups** window, select a user or group.</span></span>

2.  <span data-ttu-id="e2883-124">Нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e2883-124">Click **Remove**.</span></span>

    <span data-ttu-id="e2883-125">Пользователь или группа будет удалена.</span><span class="sxs-lookup"><span data-stu-id="e2883-125">The user or group is deleted.</span></span>

## <span data-ttu-id="e2883-126">Настройка разрешений для пользователя или группы</span><span class="sxs-lookup"><span data-stu-id="e2883-126">How to Set Permissions for a User or a Group</span></span>


**<span data-ttu-id="e2883-127">Настройка разрешений для пользователя или группы</span><span class="sxs-lookup"><span data-stu-id="e2883-127">To set permissions for a user or a group</span></span>**

1.  <span data-ttu-id="e2883-128">Выберите пользователя или группу, для которых вы хотите настроить разрешения.</span><span class="sxs-lookup"><span data-stu-id="e2883-128">Click the user or group for which you are setting the permissions.</span></span>

2.  <span data-ttu-id="e2883-129">Настройте свойства рабочей области для MED-V, как описано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="e2883-129">Configure the MED-V workspace properties as described in the following table.</span></span>

3.  <span data-ttu-id="e2883-130">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e2883-130">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="e2883-131">Свойства развертывания рабочей области</span><span class="sxs-lookup"><span data-stu-id="e2883-131">Workspace Deployment Properties</span></span>**

<span data-ttu-id="e2883-132">Описание свойства " *Общие* "</span><span class="sxs-lookup"><span data-stu-id="e2883-132">Property Description *General*</span></span>

<span data-ttu-id="e2883-133">Включение рабочей области для &lt; пользователя или группы&gt;</span><span class="sxs-lookup"><span data-stu-id="e2883-133">Enable Workspace for &lt;user or group&gt;</span></span>

<span data-ttu-id="e2883-134">Установите этот флажок, чтобы включить рабочую область MED-V для этого пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="e2883-134">Select this check box to enable the MED-V workspace for this user or group.</span></span>

<span data-ttu-id="e2883-135">Срок действия рабочей области истекает на эту дату</span><span class="sxs-lookup"><span data-stu-id="e2883-135">Workspace expires on this date</span></span>

<span data-ttu-id="e2883-136">Установите этот флажок, чтобы назначить дату окончания срока действия разрешений для этого пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="e2883-136">Select this check box to assign an expiration date for the permissions set for this user or group.</span></span>

<span data-ttu-id="e2883-137">Если выбрать этот параметр, поле Дата становится активным.</span><span class="sxs-lookup"><span data-stu-id="e2883-137">When selected, the date box is enabled.</span></span> <span data-ttu-id="e2883-138">Установите дату, после чего срок действия разрешений будет истекает в конце указанной даты.</span><span class="sxs-lookup"><span data-stu-id="e2883-138">Set the date, and permissions will expire at the end of the date specified.</span></span>

<span data-ttu-id="e2883-139">Автономная работа ограничена</span><span class="sxs-lookup"><span data-stu-id="e2883-139">Offline work is restricted to</span></span>

<span data-ttu-id="e2883-140">Установите этот флажок, чтобы назначить период времени, в течение которого политика должна обновляться для этого пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="e2883-140">Select this check box to assign a time period in which the policy must be refreshed for this user or group.</span></span> <span data-ttu-id="e2883-141">Если этот флажок установлен, в поле "период времени" включена.</span><span class="sxs-lookup"><span data-stu-id="e2883-141">When selected, the time period box is enabled.</span></span> <span data-ttu-id="e2883-142">Задать количество дней и часов, а в конце определенного периода пользователь или группа не смогут подключаться в случае, если эта политика не будет обновлена.</span><span class="sxs-lookup"><span data-stu-id="e2883-142">Set the number of days or hours, and at the end of the specified time period, the user or group will not be able to connect if the policy is not refreshed.</span></span>

<span data-ttu-id="e2883-143">Варианты удаления рабочей области</span><span class="sxs-lookup"><span data-stu-id="e2883-143">Workspace deletion options</span></span>

<span data-ttu-id="e2883-144">Щелкните, чтобы настроить параметры удаления рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="e2883-144">Click to set the MED-V workspace deletion options.</span></span> <span data-ttu-id="e2883-145">Дополнительные сведения можно найти [в разделе Настройка параметров удаления рабочих областей MED-V](how-to-set-med-v-workspace-deletion-options.md).</span><span class="sxs-lookup"><span data-stu-id="e2883-145">For more information, see [How to Set MED-V Workspace Deletion Options](how-to-set-med-v-workspace-deletion-options.md).</span></span>

*<span data-ttu-id="e2883-146">Передача данных</span><span class="sxs-lookup"><span data-stu-id="e2883-146">Data Transfer</span></span>*

<span data-ttu-id="e2883-147">Поддержка буфера обмена между узлом и рабочей областью</span><span class="sxs-lookup"><span data-stu-id="e2883-147">Support clipboard between host and Workspace</span></span>

<span data-ttu-id="e2883-148">Установите этот флажок, чтобы включить копирование и вставку между узлом и рабочей областью MED-V.</span><span class="sxs-lookup"><span data-stu-id="e2883-148">Select this check box to enable copying and pasting between the host and the MED-V workspace.</span></span>

<span data-ttu-id="e2883-149">Поддержка передачи файлов между узлом и рабочей областью</span><span class="sxs-lookup"><span data-stu-id="e2883-149">Support file transfer between the host and Workspace</span></span>

<span data-ttu-id="e2883-150">Установите этот флажок, чтобы включить передачу файлов между узлом и рабочей областью MED-V.</span><span class="sxs-lookup"><span data-stu-id="e2883-150">Select this check box to enable transferring files between the host and MED-V workspace.</span></span> <span data-ttu-id="e2883-151">В поле **Передача файлов** выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="e2883-151">Select one of the following options from the **File Transfer** box:</span></span>

-   <span data-ttu-id="e2883-152">**Оба**— позволяют передавать файлы между узлом и рабочей областью MED-V.</span><span class="sxs-lookup"><span data-stu-id="e2883-152">**Both**—Enable transferring files between the host and the MED-V workspace.</span></span>

-   <span data-ttu-id="e2883-153">**Узел в рабочую область**— позволяет передавать файлы с узла в рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="e2883-153">**Host to Workspace**—Enable transferring files from the host to the MED-V workspace.</span></span>

-   <span data-ttu-id="e2883-154">**Рабочую область для размещения**— позволяет передавать файлы из рабочей области MED-V на узел.</span><span class="sxs-lookup"><span data-stu-id="e2883-154">**Workspace to Host**—Enable transferring files from the MED-V workspace to the host.</span></span>

**<span data-ttu-id="e2883-155">Примечание.</span><span class="sxs-lookup"><span data-stu-id="e2883-155">Note</span></span>**  
<span data-ttu-id="e2883-156">Если пользователь без разрешений пытается передать файлы, появится окно с запросом на ввод учетных данных пользователя с разрешениями на выполнение передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="e2883-156">If a user without permissions attempts to transfer files, a window will appear prompting him to enter the credentials of a user with permissions to perform the file transfer.</span></span>



**<span data-ttu-id="e2883-157">Важно.</span><span class="sxs-lookup"><span data-stu-id="e2883-157">Important</span></span>**  
<span data-ttu-id="e2883-158">Для поддержки передачи файлов в Windows XP с пакетом обновления 3 (SP3) необходимо отключить синхронизацию автономных файлов, изменив реестр следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e2883-158">To support file transfer in Windows XP SP3, you must disable offline file synchronization by editing the registry as follows:</span></span>

`REG ADD HKLM\software\microsoft\windows\currentversion\netcache /V Enabled /T REG_DWORD /F /D 0`



<span data-ttu-id="e2883-159">Дополнительно</span><span class="sxs-lookup"><span data-stu-id="e2883-159">Advanced</span></span>

<span data-ttu-id="e2883-160">Нажмите эту кнопку, чтобы настроить дополнительные параметры передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="e2883-160">Click to set the advanced file transfer options.</span></span> <span data-ttu-id="e2883-161">Дополнительные сведения можно найти [в разделе Настройка дополнительных параметров передачи файлов](how-to-set-advanced-file-transfer-options.md).</span><span class="sxs-lookup"><span data-stu-id="e2883-161">For more information, see [How to Set Advanced File Transfer Options](how-to-set-advanced-file-transfer-options.md).</span></span>

*<span data-ttu-id="e2883-162">Управление устройством</span><span class="sxs-lookup"><span data-stu-id="e2883-162">Device Control</span></span>*

<span data-ttu-id="e2883-163">Включение печати на принтерах, подключенных к узлу</span><span class="sxs-lookup"><span data-stu-id="e2883-163">Enable printing to printers connected to the host</span></span>

<span data-ttu-id="e2883-164">Установите этот флажок, чтобы разрешить пользователям печатать из рабочей области MED-V с помощью принтера узла.</span><span class="sxs-lookup"><span data-stu-id="e2883-164">Select this check box to enable users to print from the MED-V workspace using the host printer.</span></span>

**<span data-ttu-id="e2883-165">Примечание.</span><span class="sxs-lookup"><span data-stu-id="e2883-165">Note</span></span>**  
<span data-ttu-id="e2883-166">Печать выполняется принтерами, определенными на узле.</span><span class="sxs-lookup"><span data-stu-id="e2883-166">The printing is performed by the printers defined on the host.</span></span>



<span data-ttu-id="e2883-167">Разрешение доступа к CD и DVD</span><span class="sxs-lookup"><span data-stu-id="e2883-167">Enable access to CD / DVD</span></span>

<span data-ttu-id="e2883-168">Установите этот флажок, чтобы разрешить доступ к CD или DVD-диску из этой рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="e2883-168">Select this check box to allow access to a CD or DVD drive from this MED-V workspace.</span></span>



**<span data-ttu-id="e2883-169">Несколько членств</span><span class="sxs-lookup"><span data-stu-id="e2883-169">Multiple Memberships</span></span>**

1.  <span data-ttu-id="e2883-170">Если пользователь входит в группу и к ней применяются пользовательские разрешения, а также к группе, в которой он входит, применяются все разрешения.</span><span class="sxs-lookup"><span data-stu-id="e2883-170">If the user is part of a group and permissions are applied to the user as well as to the group they are part of, all permissions are applied.</span></span>

2.  <span data-ttu-id="e2883-171">Если пользователь является членом двух разных групп, применяются наименее ограниченные разрешения.</span><span class="sxs-lookup"><span data-stu-id="e2883-171">If the user is a member of two different groups, the least restrictive permissions are applied.</span></span>

## <span data-ttu-id="e2883-172">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e2883-172">Related topics</span></span>


[<span data-ttu-id="e2883-173">Использование пользовательского интерфейса консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="e2883-173">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="e2883-174">Создание рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="e2883-174">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="e2883-175">Настройка параметров удаления рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="e2883-175">How to Set MED-V Workspace Deletion Options</span></span>](how-to-set-med-v-workspace-deletion-options.md)

[<span data-ttu-id="e2883-176">Настройка дополнительных параметров передачи файлов</span><span class="sxs-lookup"><span data-stu-id="e2883-176">How to Set Advanced File Transfer Options</span></span>](how-to-set-advanced-file-transfer-options.md)









