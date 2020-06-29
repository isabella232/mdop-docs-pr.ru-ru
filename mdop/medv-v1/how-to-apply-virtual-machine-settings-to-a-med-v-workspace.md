---
title: Применение параметров виртуальной машины к рабочей области MED-V
description: Применение параметров виртуальной машины к рабочей области MED-V
author: dansimp
ms.assetid: b50d0dfb-8d61-4543-9607-a29bbb1ed45f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9662bb8202285d51971eeea8beaef938b98ed6b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825972"
---
# <span data-ttu-id="d68da-103">Применение параметров виртуальной машины к рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="d68da-103">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>


<span data-ttu-id="d68da-104">Каждая Рабочая область MED-V должна иметь связанный с ней образ Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="d68da-104">Every MED-V workspace must have a Microsoft Virtual PC image associated with it.</span></span> <span data-ttu-id="d68da-105">С помощью параметров виртуальной машины вы можете назначить образ виртуального компьютера и задать другие свойства виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d68da-105">The virtual machine settings enable you to assign a Virtual PC image as well as set other virtual machine properties.</span></span>

<span data-ttu-id="d68da-106">Все параметры виртуальных машин настроены в модуле **политики** на вкладке " **Параметры виртуальной машины** ".</span><span class="sxs-lookup"><span data-stu-id="d68da-106">All virtual machine settings are configured in the **Policy** module, on the **Virtual Machine Settings** tab.</span></span>

**<span data-ttu-id="d68da-107">Применение параметров виртуальной машины к рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="d68da-107">To apply virtual machine settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="d68da-108">Щелкните рабочую область MED-V, которую нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="d68da-108">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="d68da-109">Настройте свойства виртуальной машины, как описано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d68da-109">Configure the virtual machine properties as described in the following table.</span></span>

3.  <span data-ttu-id="d68da-110">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d68da-110">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="d68da-111">Свойства виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d68da-111">Virtual Machine Properties</span></span>**

<span data-ttu-id="d68da-112">Описание свойства *Параметры виртуальной машины*</span><span class="sxs-lookup"><span data-stu-id="d68da-112">Property Description *Virtual Machine Settings*</span></span>

<span data-ttu-id="d68da-113">Назначенное изображение</span><span class="sxs-lookup"><span data-stu-id="d68da-113">Assigned Image</span></span>

<span data-ttu-id="d68da-114">Фактический образ Virtual PC (Майкрософт), назначенный рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="d68da-114">The actual Microsoft Virtual PC image assigned to the MED-V workspace.</span></span> <span data-ttu-id="d68da-115">В меню содержится список всех доступных изображений виртуальных ПК.</span><span class="sxs-lookup"><span data-stu-id="d68da-115">The menu provides a list of all available Virtual PC images.</span></span> <span data-ttu-id="d68da-116">В списке **активных** изображений находятся следующие типы изображений:</span><span class="sxs-lookup"><span data-stu-id="d68da-116">The following image types are in the **Active** image list:</span></span>

-   <span data-ttu-id="d68da-117">**Образы локальных тестов**— изображения на локальном компьютере, которые еще не были упакованы.</span><span class="sxs-lookup"><span data-stu-id="d68da-117">**Local test images**—Images on the local computer that are not yet packed.</span></span> <span data-ttu-id="d68da-118">Имена этих изображений следуют слову "тест" в круглых скобках (тестовом) и предназначены исключительно для тестирования.</span><span class="sxs-lookup"><span data-stu-id="d68da-118">These image names are followed by the word “test” in parentheses (test) and are for testing purposes only.</span></span>

-   <span data-ttu-id="d68da-119">**Локальные Упакованные изображения**— Упакованные изображения на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d68da-119">**Local packed images**—Packed images on the local computer.</span></span> <span data-ttu-id="d68da-120">За этими изображениями следует слово "Местная" в круглых скобках (локально), которое не может быть загружено клиентами до тех пор, пока администратор не отгрузит их на сервер.</span><span class="sxs-lookup"><span data-stu-id="d68da-120">These images are followed by the word “local” in parentheses (local) and cannot be downloaded by clients until the administrator uploads them to the server.</span></span>

    <span data-ttu-id="d68da-121">Локальное изображение можно выбрать при создании пакета, который будет распространяться на клиент с помощью съемных носителей (например, USB-или DVD-дисков).</span><span class="sxs-lookup"><span data-stu-id="d68da-121">A local image can be selected if you are creating a package that will be distributed to the client via removable media (such as USB or DVD).</span></span>

-   <span data-ttu-id="d68da-122">**Упакованные изображения на сервере**— образы, которые находятся на сервере, и доступны для загрузки клиентами.</span><span class="sxs-lookup"><span data-stu-id="d68da-122">**Packed images on server**—Images that are on the server and are available for download by clients.</span></span> <span data-ttu-id="d68da-123">Нажмите кнопку обновить, чтобы обновить список изображений.</span><span class="sxs-lookup"><span data-stu-id="d68da-123">Click Refresh to refresh the images list.</span></span>

    <span data-ttu-id="d68da-124">**Примечание**  Каждый образ рабочей области MED-V может использоваться только одним пользователем Windows.</span><span class="sxs-lookup"><span data-stu-id="d68da-124">**Note** Each MED-V workspace image can only be used by one Windows user.</span></span>

     

<span data-ttu-id="d68da-125">Рабочая область является постоянной</span><span class="sxs-lookup"><span data-stu-id="d68da-125">Workspace is persistent</span></span>

<span data-ttu-id="d68da-126">Установите этот флажок, чтобы настроить постоянную рабочую область для MED-V.</span><span class="sxs-lookup"><span data-stu-id="d68da-126">Select this check box to configure the MED-V workspace as persistent.</span></span> <span data-ttu-id="d68da-127">В постоянной рабочей области MED-V при остановке рабочей области MED-v изменения и дополнения к рабочей области MED-V сохраняются в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="d68da-127">In a persistent MED-V workspace, when the MED-V workspace is stopped, changes and additions to the MED-V workspace are saved in the MED-V workspace.</span></span>

<span data-ttu-id="d68da-128">Для рабочей области домена MED-V этот параметр должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="d68da-128">For a Domain MED-V workspace, this option must be selected.</span></span>

<span data-ttu-id="d68da-129">**Примечание**  Этот параметр не следует изменять после развертывания рабочей области MED-V для пользователей.</span><span class="sxs-lookup"><span data-stu-id="d68da-129">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="d68da-130">Завершение работы виртуальной машины при остановке рабочей области</span><span class="sxs-lookup"><span data-stu-id="d68da-130">Shut down the VM when stopping the Workspace</span></span>

<span data-ttu-id="d68da-131">Установите этот флажок, чтобы завершить работу виртуальной машины при остановке рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="d68da-131">Select this check box to shut down the virtual machine when stopping the MED-V workspace.</span></span> <span data-ttu-id="d68da-132">Если этот флажок не установлен, при завершении сеанса виртуальная машина не закрывается, а вместо этого создает снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d68da-132">If this check box is cleared, at the completion of each session, the virtual machine is not shut down but instead takes a snapshot of the virtual machine.</span></span> <span data-ttu-id="d68da-133">При запуске нового сеанса Windows запускается из него (это значит, что Windows не перезапускается, а вход не требуется).</span><span class="sxs-lookup"><span data-stu-id="d68da-133">Upon the initiation of a new session, Windows starts from the snapshot (that is, Windows does not restart and no login is required).</span></span>

<span data-ttu-id="d68da-134">**Примечание**  Это свойство доступно только в том случае, если выбран параметр **Рабочая область является постоянной** .</span><span class="sxs-lookup"><span data-stu-id="d68da-134">**Note** This property is enabled only if **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="d68da-135">Вход в Windows в виртуальной машине с использованием учетных данных MED-V (SSO)</span><span class="sxs-lookup"><span data-stu-id="d68da-135">Logon to Windows in VM using MED-V credentials (SSO)</span></span>

<span data-ttu-id="d68da-136">Установите этот флажок, чтобы войти в Windows на виртуальной машине с использованием учетных данных MED-V, введенных при входе в клиент MED-V.</span><span class="sxs-lookup"><span data-stu-id="d68da-136">Select this check box to log in to Windows on the virtual machine by using the MED-V credentials entered when logging in to MED-V client.</span></span>

<span data-ttu-id="d68da-137">**Примечание**  Это свойство доступно только в том случае, если выбран параметр **Рабочая область является постоянной** .</span><span class="sxs-lookup"><span data-stu-id="d68da-137">**Note** This property is enabled only when **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="d68da-138">Рабочая область — revertible</span><span class="sxs-lookup"><span data-stu-id="d68da-138">Workspace is revertible</span></span>

<span data-ttu-id="d68da-139">Установите этот флажок, чтобы настроить рабочую область MED-V как revertible.</span><span class="sxs-lookup"><span data-stu-id="d68da-139">Select this check box to configure the MED-V workspace as revertible.</span></span> <span data-ttu-id="d68da-140">В рабочей области revertible MED-V по завершении каждого сеанса (то есть когда пользователь останавливает рабочую область MED-V), в рабочей области MED-V возвращается исходное состояние, в котором она находилась во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="d68da-140">In a revertible MED-V workspace, at the completion of each session (that is, when the user stops the MED-V workspace), the MED-V workspace reverts to the original state it was in during deployment.</span></span> <span data-ttu-id="d68da-141">Изменения и дополнения, внесенные пользователем, сохраняются в рабочей области MED-V между сеансами.</span><span class="sxs-lookup"><span data-stu-id="d68da-141">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span>

<span data-ttu-id="d68da-142">**Примечание**  Этот параметр не следует изменять после развертывания рабочей области MED-V для пользователей.</span><span class="sxs-lookup"><span data-stu-id="d68da-142">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="d68da-143">Синхронизация часового пояса рабочей области с узлом</span><span class="sxs-lookup"><span data-stu-id="d68da-143">Synchronize Workspace time zone with host</span></span>

<span data-ttu-id="d68da-144">Установите этот флажок, чтобы синхронизировать часовой пояс в рабочей области MED-V с узлом.</span><span class="sxs-lookup"><span data-stu-id="d68da-144">Select this check box to synchronize the time zone in the MED-V workspace with the host.</span></span>

<span data-ttu-id="d68da-145">Синхронизация работает по-разному в зависимости от того, является ли Рабочая область MED-V постоянной или revertible, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="d68da-145">The synchronization works differently depending on whether the MED-V workspace is persistent or revertible, as follows:</span></span>

-   <span data-ttu-id="d68da-146">В постоянной рабочей области MED-V часовой пояс сначала пытается выполнить синхронизацию с сервером.</span><span class="sxs-lookup"><span data-stu-id="d68da-146">In a persistent MED-V workspace, the time zone first tries to synchronize with the server.</span></span> <span data-ttu-id="d68da-147">Если это не удается, оно синхронизируется с узлом.</span><span class="sxs-lookup"><span data-stu-id="d68da-147">If that fails, it synchronizes with the host.</span></span>

-   <span data-ttu-id="d68da-148">В рабочей области revertible MED-V часовой пояс синхронизируется с ведущим узлом.</span><span class="sxs-lookup"><span data-stu-id="d68da-148">In a revertible MED-V workspace, the time zone synchronizes with the host.</span></span>

*<span data-ttu-id="d68da-149">Параметры блокировки</span><span class="sxs-lookup"><span data-stu-id="d68da-149">Lock Settings</span></span>*

<span data-ttu-id="d68da-150">Блокировка рабочей области в спящем режиме</span><span class="sxs-lookup"><span data-stu-id="d68da-150">Lock the Workspace on host standby/hibernate event</span></span>

<span data-ttu-id="d68da-151">Установите этот флажок, чтобы автоматически блокировать рабочую область MED-V при переходе на главный компьютер в ждущий или спящий режим.</span><span class="sxs-lookup"><span data-stu-id="d68da-151">Select this check box to automatically lock the MED-V workspace when the host computer goes into standby or hibernate.</span></span>

<span data-ttu-id="d68da-152">Блокировка рабочей области после</span><span class="sxs-lookup"><span data-stu-id="d68da-152">Lock the Workspace after</span></span>

<span data-ttu-id="d68da-153">Установите этот флажок, чтобы заблокировать рабочую область MED-V, когда Рабочая область MED-V бездействует в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="d68da-153">Select this check box to lock the MED-V workspace when the MED-V workspace is idle for a specified period of time.</span></span> <span data-ttu-id="d68da-154">Если выбрано, поле "число" доступно.</span><span class="sxs-lookup"><span data-stu-id="d68da-154">When selected, the number box is enabled.</span></span> <span data-ttu-id="d68da-155">Введите количество минут бездействия, прежде чем блокировать рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="d68da-155">Enter the number of minutes of idle time before locking the MED-V workspace.</span></span>

<span data-ttu-id="d68da-156">**Примечание**  Время простоя ссылается на приложения для рабочей области MED-V (но не ведущие приложения).</span><span class="sxs-lookup"><span data-stu-id="d68da-156">**Note** The idle time refers to the MED-V workspace applications (not the host applications).</span></span>

 

*<span data-ttu-id="d68da-157">Параметры обновления изображения</span><span class="sxs-lookup"><span data-stu-id="d68da-157">Image Update Settings</span></span>*

<span data-ttu-id="d68da-158">Сохранить только</span><span class="sxs-lookup"><span data-stu-id="d68da-158">Keep only</span></span>

<span data-ttu-id="d68da-159">Установите этот флажок, чтобы ограничить количество старых версий изображений, которые нужно сохранить.</span><span class="sxs-lookup"><span data-stu-id="d68da-159">Select this check box to limit the number of old image versions to keep.</span></span>

<span data-ttu-id="d68da-160">Если выбрано, поле "число" доступно.</span><span class="sxs-lookup"><span data-stu-id="d68da-160">When selected, the number box is enabled.</span></span> <span data-ttu-id="d68da-161">Введите число старых версий, которые нужно сохранить.</span><span class="sxs-lookup"><span data-stu-id="d68da-161">Enter the number of old versions to keep.</span></span>

<span data-ttu-id="d68da-162">Предлагать обновление, если доступна новая версия</span><span class="sxs-lookup"><span data-stu-id="d68da-162">Suggest update when a new version is available</span></span>

<span data-ttu-id="d68da-163">Установите этот флажок, чтобы предложить (но не принудительно) обновление при наличии новой версии изображения.</span><span class="sxs-lookup"><span data-stu-id="d68da-163">Select this check box to suggest (but not force) an update when a new version of the image is available.</span></span>

<span data-ttu-id="d68da-164">Клиенты должны использовать отрезку при загрузке изображений для этой рабочей области</span><span class="sxs-lookup"><span data-stu-id="d68da-164">Clients should use Trim Transfer when downloading images for this Workspace</span></span>

<span data-ttu-id="d68da-165">Установите этот флажок, чтобы включить перенос обрезки (Дополнительные сведения можно найти в разделе [технология передачи обрезки med-v](med-v-trim-transfer-technology-medvv2.md)) при загрузке изображений, связанных с этой рабочей областью для MED-v.</span><span class="sxs-lookup"><span data-stu-id="d68da-165">Select this check box to enable Trim Transfer (for more information, see [MED-V Trim Transfer Technology](med-v-trim-transfer-technology-medvv2.md)) when downloading images associated with this MED-V workspace.</span></span> <span data-ttu-id="d68da-166">Если этот флажок снят, будет загружено полное изображение.</span><span class="sxs-lookup"><span data-stu-id="d68da-166">If this check box is cleared, the full image will be downloaded.</span></span>

<span data-ttu-id="d68da-167">**Примечание**  Для монтажа обрезки требуется индексирование жесткого диска, который может занять значительное количество времени.</span><span class="sxs-lookup"><span data-stu-id="d68da-167">**Note** Trim Transfer requires indexing the hard drive, which might take a considerable amount of time.</span></span> <span data-ttu-id="d68da-168">Рекомендуется использовать передачу усечения, если индексирование жесткого диска более эффективно, чем при загрузке новой версии изображения, например при загрузке версии изображения, похожей на текущую версию.</span><span class="sxs-lookup"><span data-stu-id="d68da-168">It is recommended to use Trim Transfer when indexing the hard drive is more efficient than downloading the new image version, such as when downloading an image version that is similar to the existing version.</span></span>

 

 

## <span data-ttu-id="d68da-169">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d68da-169">Related topics</span></span>


[<span data-ttu-id="d68da-170">Создание образа MED-V</span><span class="sxs-lookup"><span data-stu-id="d68da-170">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="d68da-171">Использование пользовательского интерфейса консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="d68da-171">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="d68da-172">Создание рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="d68da-172">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





