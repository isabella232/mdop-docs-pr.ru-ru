---
title: Управление виртуальными приложениями вручную
description: Управление виртуальными приложениями вручную
author: dansimp
ms.assetid: 583c5255-d3f4-4197-85cd-2a59868d85de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8dd5bb9d62950ac1a03ad0ec14802d9e0ff56e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817112"
---
# <span data-ttu-id="9e44e-103">Управление виртуальными приложениями вручную</span><span class="sxs-lookup"><span data-stu-id="9e44e-103">How to Manage Virtual Applications Manually</span></span>


<span data-ttu-id="9e44e-104">Вы можете использовать консоль управления клиентом Application Virtualization (App-V) для управления виртуальными приложениями в классическом клиенте App-V или клиент App-V для служб удаленных рабочих столов (ранее — служб терминалов).</span><span class="sxs-lookup"><span data-stu-id="9e44e-104">You can use the Application Virtualization (App-V) Client Management Console to manage virtual applications in the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="9e44e-105">Администраторы App-V могут выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="9e44e-105">App-V administrators can use perform the following tasks:</span></span>

## <span data-ttu-id="9e44e-106">Загрузка и выгрузка приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-106">How to Load or Unload an App-V Application</span></span>


<span data-ttu-id="9e44e-107">С помощью описанных ниже процедур можно загрузить или выгрузить приложение из кэша прямо из области **результатов** узла **приложения** на консоли управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="9e44e-107">You can use the following procedures to load or unload an application from the cache, directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="9e44e-108">При выборе этого узла в области **результатов** отображается список приложений.</span><span class="sxs-lookup"><span data-stu-id="9e44e-108">When you select this node, the **Results** pane displays a list of applications.</span></span>

<span data-ttu-id="9e44e-109">**Примечание**  При загрузке или выгрузке пакета все приложения в пакете загружаются в кэш или удаляются из него.</span><span class="sxs-lookup"><span data-stu-id="9e44e-109">**Note** When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span> <span data-ttu-id="9e44e-110">Если при загрузке пакета нет достаточного места в кэше для загрузки приложений, увеличите размер кэша.</span><span class="sxs-lookup"><span data-stu-id="9e44e-110">When loading a package, if you do not have adequate space in cache to load the applications, increase your cache size.</span></span> <span data-ttu-id="9e44e-111">Дополнительные сведения о размере кэша вы можете узнать, [как изменить размер кэша и обозначение диска](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span><span class="sxs-lookup"><span data-stu-id="9e44e-111">For more information about cache size, see [How to Change the Cache Size and the Drive Letter Designation](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span></span>

 

**<span data-ttu-id="9e44e-112">Загрузка приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-112">To load an App-V application</span></span>**

1.  <span data-ttu-id="9e44e-113">Переместите курсор в область **результатов** , щелкните нужное приложение правой кнопкой мыши и выберите в контекстном меню пункт **загрузить** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-113">Move the cursor to the **Results** pane, right-click the desired application, and select **Load** from the pop-up menu.</span></span>

2.  <span data-ttu-id="9e44e-114">Приложение загружается автоматически.</span><span class="sxs-lookup"><span data-stu-id="9e44e-114">The application is automatically loaded.</span></span> <span data-ttu-id="9e44e-115">Ход выполнения отслеживается в столбце с названием " **состояние пакета**".</span><span class="sxs-lookup"><span data-stu-id="9e44e-115">The progress is tracked in the column labeled **Package Status**.</span></span> <span data-ttu-id="9e44e-116">Вы должны обновить представление, чтобы убедиться, что загрузка завершена, или просмотреть ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="9e44e-116">You must refresh the view to see that the load is complete or to see the progress.</span></span>

**<span data-ttu-id="9e44e-117">Выгрузка приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-117">To unload an App-V application</span></span>**

1.  <span data-ttu-id="9e44e-118">Переместить курсор в область **результатов** , щелкнуть правой кнопкой мыши нужное приложение и выбрать пункт **выгрузка** из всплывающего меню.</span><span class="sxs-lookup"><span data-stu-id="9e44e-118">Move the cursor to the **Results** pane, right-click the desired application, and select **Unload** from the pop-up menu.</span></span>

2.  <span data-ttu-id="9e44e-119">Приложение будет автоматически выгружено, а столбец " **состояние пакета** " обновится, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="9e44e-119">The application is automatically unloaded, and the **Package Status** column is updated to reflect the change.</span></span>

## <span data-ttu-id="9e44e-120">Очистка приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-120">How to clear an App-V application</span></span>


<span data-ttu-id="9e44e-121">Вы можете удалить приложение из консоли прямо из области **результатов** узла **приложения** на консоли управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="9e44e-121">You can clear an application from the console directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="9e44e-122">Когда вы удаляете приложение, система удаляет параметры, ярлыки и сопоставления типов файлов, соответствующие приложению, а также удаляет приложение из списка приложений пользователя.</span><span class="sxs-lookup"><span data-stu-id="9e44e-122">When you clear an application, the system removes the settings, shortcuts, and file type associations that correspond to the application and also removes the application from the user’s list of applications.</span></span>

<span data-ttu-id="9e44e-123">**Примечание**  Когда вы удаляете приложение с консоли, вы больше не сможете пользоваться этим приложением.</span><span class="sxs-lookup"><span data-stu-id="9e44e-123">**Note** When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="9e44e-124">Однако приложение остается в кэше и по-прежнему доступно другим пользователям в той же системе.</span><span class="sxs-lookup"><span data-stu-id="9e44e-124">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="9e44e-125">После обновления публикации удаленные приложения станут доступны вам.</span><span class="sxs-lookup"><span data-stu-id="9e44e-125">After a publishing refresh, the cleared applications will again become available to you.</span></span> <span data-ttu-id="9e44e-126">Если в пакете несколько приложений, параметры пользователя не удаляются до тех пор, пока не будут очищены все приложения.</span><span class="sxs-lookup"><span data-stu-id="9e44e-126">If there are multiple applications in a package, the user's settings are not removed until all of the applications are cleared.</span></span>

 

**<span data-ttu-id="9e44e-127">Удаление приложения с консоли</span><span class="sxs-lookup"><span data-stu-id="9e44e-127">To clear an application from the console</span></span>**

1.  <span data-ttu-id="9e44e-128">Перемещение курсора в область **результатов** щелкните нужное приложение правой кнопкой мыши и выберите пункт **очистить** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="9e44e-128">Move the cursor to the **Results** pane, right-click the desired application, and select **Clear** from the pop-up menu.</span></span>

2.  <span data-ttu-id="9e44e-129">В строке подтверждения нажмите кнопку **Да** , чтобы удалить приложение, или кнопку **нет** , чтобы отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="9e44e-129">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="9e44e-130">Восстановление приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-130">How to Repair an App-V application</span></span>


<span data-ttu-id="9e44e-131">Чтобы восстановить выбранное приложение, вы можете выполнить описанную ниже процедуру прямо из области **результатов** узла **приложения** на консоли управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="9e44e-131">To repair a selected application, you can perform the following procedure directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="9e44e-132">При восстановлении приложения удаляются все пользовательские настройки и восстанавливаются параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9e44e-132">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="9e44e-133">Это действие не приводит к изменению или удалению ярлыков и сопоставлений типов файлов, но не удаляет приложение из кэша.</span><span class="sxs-lookup"><span data-stu-id="9e44e-133">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

**<span data-ttu-id="9e44e-134">Восстановление приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-134">To repair an App-V application</span></span>**

1.  <span data-ttu-id="9e44e-135">Перемещение курсора в область **результатов** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-135">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="9e44e-136">Щелкните нужное приложение правой кнопкой мыши и выберите в контекстном меню пункт **восстановить** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-136">Right-click the desired application, and select **Repair** from the pop-up menu.</span></span>

3.  <span data-ttu-id="9e44e-137">В ответ на запрос подтверждения нажмите кнопку **Да** , чтобы восстановить приложение, или **нет** , чтобы отменить его.</span><span class="sxs-lookup"><span data-stu-id="9e44e-137">At the confirmation prompt, click **Yes** to repair the application or **No** to cancel.</span></span>

## <span data-ttu-id="9e44e-138">Импорт приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-138">How to import an App-V application</span></span>


<span data-ttu-id="9e44e-139">С помощью описанной ниже процедуры можно импортировать приложение в кэш прямо из области **результатов** узла **приложения** на консоли управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="9e44e-139">You can use the following procedure to import an application into the cache directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="9e44e-140">Импорт приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-140">To import an App-V application</span></span>**

1.  <span data-ttu-id="9e44e-141">Переместите курсор в область **результатов** , щелкните нужное приложение правой кнопкой мыши и выберите пункт **Импорт** из всплывающего меню.</span><span class="sxs-lookup"><span data-stu-id="9e44e-141">Move the cursor to the **Results** pane, right-click the desired application, and select **Import** from the pop-up menu.</span></span>

2.  <span data-ttu-id="9e44e-142">В окне **обзора** перейдите в расположение файла пакета для нужного приложения и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9e44e-142">From the **Browse** window, navigate to the location of the package file for the desired application, and then click **OK**.</span></span>

    <span data-ttu-id="9e44e-143">**Примечание**  Если вы уже настроили путь для импорта или файл SFT находится в том же пути, что и в последнем успешном импорте, шаг 2 не требуется.</span><span class="sxs-lookup"><span data-stu-id="9e44e-143">**Note** If you have already configured an import search path or if the SFT file is in the same path as the last successful import, step 2 is not required.</span></span>

     

## <span data-ttu-id="9e44e-144">Блокировка и разблокировка приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-144">How to lock or unlock an App-V application</span></span>


<span data-ttu-id="9e44e-145">С помощью описанных ниже процедур можно заблокировать или разблокировать любое приложение в кэше клиента для настольных компьютеров Application Virtualization или клиент для кэша служб удаленных рабочих столов (ранее служб терминалов).</span><span class="sxs-lookup"><span data-stu-id="9e44e-145">You can use the following procedures to lock or unlock any application in the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services (formerly Terminal Services) cache.</span></span> <span data-ttu-id="9e44e-146">Заблокированное приложение не может быть удалено из кэша, чтобы освободить место для новых приложений.</span><span class="sxs-lookup"><span data-stu-id="9e44e-146">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="9e44e-147">Чтобы удалить заблокированное приложение из кэша клиентских компьютеров Application Virtualization или клиента для кэша служб удаленных рабочих столов, необходимо сначала разблокировать его.</span><span class="sxs-lookup"><span data-stu-id="9e44e-147">To remove a locked application from the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services cache, you must first unlock it.</span></span>

**<span data-ttu-id="9e44e-148">Блокировка приложения</span><span class="sxs-lookup"><span data-stu-id="9e44e-148">To lock an application</span></span>**

1.  <span data-ttu-id="9e44e-149">Перемещение курсора в область **результатов** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-149">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="9e44e-150">Щелкните нужное приложение правой кнопкой мыши и выберите в контекстном меню пункт **блокировать** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-150">Right-click the desired application, and select **Lock** from the pop-up menu.</span></span> <span data-ttu-id="9e44e-151">Выбранное приложение заблокировано в кэше.</span><span class="sxs-lookup"><span data-stu-id="9e44e-151">The selected application is locked in the cache.</span></span>

**<span data-ttu-id="9e44e-152">Разблокировка приложения</span><span class="sxs-lookup"><span data-stu-id="9e44e-152">To unlock an application</span></span>**

1.  <span data-ttu-id="9e44e-153">Перемещение курсора в область **результатов** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-153">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="9e44e-154">Щелкните нужное приложение правой кнопкой мыши и выберите в контекстном меню команду **разблокировать** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-154">Right-click the desired application, and select **Unlock** from the pop-up menu.</span></span> <span data-ttu-id="9e44e-155">Выбранное приложение разблокировано в кэше и может быть удалено.</span><span class="sxs-lookup"><span data-stu-id="9e44e-155">The selected application is unlocked in the cache and can be removed.</span></span>

## <span data-ttu-id="9e44e-156">Удаление приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-156">How to delete an App-V application</span></span>


<span data-ttu-id="9e44e-157">При выборе узла **приложения** на консоли управления клиентом Application Virtualization в области **результатов** отображается список приложений.</span><span class="sxs-lookup"><span data-stu-id="9e44e-157">When you select the **Application** node in the Application Virtualization Client Management Console, the **Results** pane displays a list of applications.</span></span> <span data-ttu-id="9e44e-158">Вы можете удалить приложение из области **результатов** с помощью описанной ниже процедуры, которое также удаляет приложение из кэша.</span><span class="sxs-lookup"><span data-stu-id="9e44e-158">You can use the following procedure to delete an application from the **Results** pane, which also removes the application from the cache.</span></span>

<span data-ttu-id="9e44e-159">**Примечание**  Когда вы удаляете приложение, выбранное приложение больше не будет доступно для всех пользователей на этом клиенте.</span><span class="sxs-lookup"><span data-stu-id="9e44e-159">**Note** When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="9e44e-160">Ярлыки и сопоставления типов файлов скрыты, а приложение удаляется из кэша.</span><span class="sxs-lookup"><span data-stu-id="9e44e-160">Shortcuts and file type associations are hidden, and the application is deleted from cache.</span></span> <span data-ttu-id="9e44e-161">Тем не менее, если другое приложение ссылается на данные в данных кэша файловой системы для выбранного приложения, эти элементы не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="9e44e-161">However, if another application refers to data in the file system cache data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="9e44e-162">После обновления публикации удаленные приложения станут доступны вам.</span><span class="sxs-lookup"><span data-stu-id="9e44e-162">After a publishing refresh, the deleted applications will again become available to you.</span></span>

 

**<span data-ttu-id="9e44e-163">Удаление приложения</span><span class="sxs-lookup"><span data-stu-id="9e44e-163">To delete an application</span></span>**

1.  <span data-ttu-id="9e44e-164">Переместите курсор в область **результатов** , щелкните нужное приложение правой кнопкой мыши и выберите в контекстном меню пункт **Удалить** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-164">Move the cursor to the **Results** pane, right-click the desired application, and select **Delete** from the pop-up menu.</span></span>

2.  <span data-ttu-id="9e44e-165">В строке подтверждения нажмите кнопку **Да** , чтобы удалить приложение, или кнопку **нет** , чтобы отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="9e44e-165">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="9e44e-166">Изменение значка приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-166">How to change an App-V application icon</span></span>


<span data-ttu-id="9e44e-167">Вы можете использовать описанную ниже процедуру, чтобы изменить значок, связанный с выбранным приложением, прямо из области **результатов** узла **приложения** на консоли управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="9e44e-167">You can use the following procedure to change an icon associated with the selected application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="9e44e-168">Изменение значка приложения</span><span class="sxs-lookup"><span data-stu-id="9e44e-168">To change an application icon</span></span>**

1.  <span data-ttu-id="9e44e-169">Переместите курсор в область **результатов** и щелкните правой кнопкой мыши нужное приложение.</span><span class="sxs-lookup"><span data-stu-id="9e44e-169">Move the cursor to the **Results** pane, and right-click the desired application.</span></span>

2.  <span data-ttu-id="9e44e-170">Выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="9e44e-170">Select **Properties**.</span></span>

3.  <span data-ttu-id="9e44e-171">На вкладке **Общие** нажмите кнопку **изменить значок**.</span><span class="sxs-lookup"><span data-stu-id="9e44e-171">On the **General** tab, click **Change Icon**.</span></span>

4.  <span data-ttu-id="9e44e-172">Выберите нужный значок или перейдите в другое место, чтобы выбрать значок.</span><span class="sxs-lookup"><span data-stu-id="9e44e-172">Select the desired icon, or browse to another location to select the icon.</span></span> <span data-ttu-id="9e44e-173">После того как вы выберете значок, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9e44e-173">After you've selected the icon, click **OK**.</span></span> <span data-ttu-id="9e44e-174">В области **результатов** появится значок "создать".</span><span class="sxs-lookup"><span data-stu-id="9e44e-174">The new icon appears in the **Results** pane.</span></span>

## <span data-ttu-id="9e44e-175">Добавление приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-175">How to add an App-V application</span></span>


<span data-ttu-id="9e44e-176">Вы можете использовать описанную ниже процедуру, чтобы добавить приложение прямо из области **результатов** узла **приложения** на консоли управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="9e44e-176">You can use the following procedure to add an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="9e44e-177">Добавление приложения</span><span class="sxs-lookup"><span data-stu-id="9e44e-177">To add an application</span></span>**

1.  <span data-ttu-id="9e44e-178">В области **результатов** щелкните правой кнопкой мыши и выберите в контекстном меню команду **создать приложение** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-178">In the **Results** pane, right-click and select **New Application** from the pop-up menu.</span></span>

2.  <span data-ttu-id="9e44e-179">На странице мастера можно выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="9e44e-179">On the wizard page, you can perform the following tasks:</span></span>

    1.  <span data-ttu-id="9e44e-180">**Значок "изменить**" — отображает стандартный браузер значков Windows.</span><span class="sxs-lookup"><span data-stu-id="9e44e-180">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="9e44e-181">Перейдите к нужному значку и выберите его.</span><span class="sxs-lookup"><span data-stu-id="9e44e-181">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="9e44e-182">**Путь к файлу OSD или URL-адрес**— введите локальный абсолютный путь, полный путь UNC (общий файл или каталог в сети) или URL-адрес HTTP.</span><span class="sxs-lookup"><span data-stu-id="9e44e-182">**OSD File Path or URL**—Enter a local absolute path, a full UNC path (shared file or directory on a network), or an HTTP URL.</span></span>

    3.  <span data-ttu-id="9e44e-183">**(Кнопка "Обзор" в OSD)**— отображает стандартное диалоговое окно " **Открыть файл** Windows".</span><span class="sxs-lookup"><span data-stu-id="9e44e-183">**(OSD browse button)**—Displays the standard Windows **Open File** dialog box.</span></span> <span data-ttu-id="9e44e-184">Найдите нужный файл.</span><span class="sxs-lookup"><span data-stu-id="9e44e-184">Browse to find the desired file.</span></span>

3.  <span data-ttu-id="9e44e-185">Нажмите кнопку **Готово** , чтобы добавить приложение в область **результатов** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-185">Click **Finish** to add the application to the **Results** pane.</span></span>

## <span data-ttu-id="9e44e-186">Публикация сочетания клавиш для приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-186">How to publish an App-V application shortcut</span></span>


<span data-ttu-id="9e44e-187">С помощью описанной ниже процедуры можно публиковать ярлыки приложений прямо из области **результатов** узла **приложения** на консоли управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="9e44e-187">You can use the following procedure to publish shortcuts to an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="9e44e-188">Публикация сочетаний клавиш для приложений</span><span class="sxs-lookup"><span data-stu-id="9e44e-188">To publish application shortcuts</span></span>**

1.  <span data-ttu-id="9e44e-189">Переместите курсор в область **результатов** , щелкните нужное приложение правой кнопкой мыши и выберите в контекстном меню команду **создать** ярлык, чтобы открыть мастер создания ярлыков.</span><span class="sxs-lookup"><span data-stu-id="9e44e-189">Move the cursor to the **Results** pane, right-click the desired application, and select **New Shortcut** from the pop-up menu to display the New Shortcut Wizard.</span></span>

2.  <span data-ttu-id="9e44e-190">На первой странице мастера создания ярлыков выберите значок и укажите имя для ярлыка.</span><span class="sxs-lookup"><span data-stu-id="9e44e-190">On the first page of the New Shortcut Wizard, select an icon and specify a name for the shortcut.</span></span>

    1.  <span data-ttu-id="9e44e-191">**Значок "изменить**" — отображает стандартный браузер значков Windows.</span><span class="sxs-lookup"><span data-stu-id="9e44e-191">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="9e44e-192">Перейдите к нужному значку и выберите его.</span><span class="sxs-lookup"><span data-stu-id="9e44e-192">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="9e44e-193">**Название ярлыка**: введите имя, которое вы хотите назначить сочетанию клавиш.</span><span class="sxs-lookup"><span data-stu-id="9e44e-193">**Shortcut Title**—Enter the name you want to give the shortcut.</span></span> <span data-ttu-id="9e44e-194">Это поле по умолчанию является существующим именем и версией приложения.</span><span class="sxs-lookup"><span data-stu-id="9e44e-194">This field defaults to the existing name and version of the application.</span></span>

3.  <span data-ttu-id="9e44e-195">На второй странице мастера определите расположение опубликованного ярлыка.</span><span class="sxs-lookup"><span data-stu-id="9e44e-195">On the second page of the wizard, determine the location of the published shortcut.</span></span>

    1.  <span data-ttu-id="9e44e-196">**Рабочий стол**— установите этот флажок, чтобы опубликовать ярлык на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="9e44e-196">**The Desktop**—Select this check box to publish the shortcut to the desktop.</span></span>

    2.  <span data-ttu-id="9e44e-197">**Панель быстрого запуска**— установите этот флажок, чтобы опубликовать ярлык на панели быстрого запуска.</span><span class="sxs-lookup"><span data-stu-id="9e44e-197">**The Quick Launch Toolbar**—Select this check box to publish the shortcut to the Quick Launch toolbar.</span></span>

    3.  <span data-ttu-id="9e44e-198">В **меню "Отправить**" — выберите этот флажок, чтобы опубликовать ярлык в меню " **Отправить** ".</span><span class="sxs-lookup"><span data-stu-id="9e44e-198">**The Send To Menu**—Select this check box to publish the shortcut to the **Send To** menu.</span></span>

    4.  <span data-ttu-id="9e44e-199">**Программы в меню "Пуск**" — это поле становится активным, если установлен флажок **меню "Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="9e44e-199">**Programs in the Start Menu**—When you select the **Start Menu** check box, this field becomes active.</span></span> <span data-ttu-id="9e44e-200">Оставьте это поле пустым, чтобы опубликовать ярлык прямо в корневом каталоге папки программы или введите имя папки или иерархии, например "My \ _Computer \\Officeные приложения".</span><span class="sxs-lookup"><span data-stu-id="9e44e-200">Leave this field blank to publish the shortcut directly to the root of the Programs folder, or enter a folder name or hierarchy—for example, "My\_Computer\\Office Applications."</span></span> <span data-ttu-id="9e44e-201">Сочетания клавиш, созданные таким образом, доступны только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="9e44e-201">Shortcuts created this way are available only for the current user.</span></span>

    5.  <span data-ttu-id="9e44e-202">**Другое расположение** и кнопка **обзора** — при установке **другого местоположения** это поле становится активным.</span><span class="sxs-lookup"><span data-stu-id="9e44e-202">**Another location** and **Browse** button—When you select the **Another location** check box, this field becomes active.</span></span> <span data-ttu-id="9e44e-203">Введите любое допустимое расположение на компьютере или любой доступный UNC-путь (общий файл или каталог в сети).</span><span class="sxs-lookup"><span data-stu-id="9e44e-203">Enter any valid location on the computer or any available UNC path (shared file or directory on a network).</span></span> <span data-ttu-id="9e44e-204">Кнопка " **Обзор** " отображает стандартное диалоговое окно **открытия файла** Windows.</span><span class="sxs-lookup"><span data-stu-id="9e44e-204">The **Browse** button displays a standard Windows **File Open** dialog box.</span></span>

4.  <span data-ttu-id="9e44e-205">На третьей странице мастера введите нужные параметры командной строки.</span><span class="sxs-lookup"><span data-stu-id="9e44e-205">On the third page of the wizard, enter desired command-line parameters.</span></span>

5.  <span data-ttu-id="9e44e-206">Нажмите кнопку **Готово** , чтобы опубликовать ярлыки и выйти в область **результатов** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-206">Click **Finish** to publish the shortcuts and exit to the **Results** pane.</span></span>

## <span data-ttu-id="9e44e-207">Добавление сопоставления типов файлов для приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-207">How to add a file type association for an App-V application</span></span>


<span data-ttu-id="9e44e-208">Вы можете использовать описанную ниже процедуру, чтобы добавить ассоциацию типа файла с помощью узла **сопоставления типов файлов** в консоли управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="9e44e-208">You can use the following procedure to add a file type association, using the **File Type Associations** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="9e44e-209">Добавление сопоставления типов файлов</span><span class="sxs-lookup"><span data-stu-id="9e44e-209">To add a file type association</span></span>**

1.  <span data-ttu-id="9e44e-210">Щелкните правой кнопкой мыши узел **сопоставления типов файлов** и в контекстном меню выберите пункт **создать связь** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-210">Right-click the **File Type Associations** node, and select **New Association** from the pop-up menu.</span></span>

2.  <span data-ttu-id="9e44e-211">Заполните первую часть диалогового окна, заполнив указанные ниже сведения, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e44e-211">Complete the first step of the dialog box by completing the following information, and then click **Next**:</span></span>

    1.  <span data-ttu-id="9e44e-212">**Расширение**— введите новое расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="9e44e-212">**Extension**—Enter a new file name extension.</span></span> <span data-ttu-id="9e44e-213">По умолчанию это поле оставлено пустым.</span><span class="sxs-lookup"><span data-stu-id="9e44e-213">This field is blank by default.</span></span>

    2.  <span data-ttu-id="9e44e-214">**Создайте новый тип файлов с помощью этого описания**: Выберите этот переключатель, чтобы ввести новое описание типа файла в поле активно.</span><span class="sxs-lookup"><span data-stu-id="9e44e-214">**Create a new file type with this description**—Select this radio button to enter a new file type description in the active field.</span></span> <span data-ttu-id="9e44e-215">Эта кнопка выбрана по умолчанию, а активное поле пусто.</span><span class="sxs-lookup"><span data-stu-id="9e44e-215">This button is selected by default, and the active field is blank.</span></span>

    3.  <span data-ttu-id="9e44e-216">**Применить этот тип файла ко всем пользователям**— установите этот флажок, если вы хотите, чтобы эта ассоциация была глобальной для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="9e44e-216">**Apply this file type to all users**—Select this check box when you want this association to be global for all users.</span></span> <span data-ttu-id="9e44e-217">По умолчанию этот флажок снят.</span><span class="sxs-lookup"><span data-stu-id="9e44e-217">By default, this box is cleared.</span></span>

    4.  <span data-ttu-id="9e44e-218">**Свяжите это расширение с существующим типом файлов**— выберите этот переключатель, чтобы связать расширение с существующим типом файла.</span><span class="sxs-lookup"><span data-stu-id="9e44e-218">**Link this extension with an existing file type**—Select this radio button to associate the extension with an existing file type.</span></span> <span data-ttu-id="9e44e-219">Выберите тип файла из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="9e44e-219">Pick a file type from the drop-down list.</span></span> <span data-ttu-id="9e44e-220">Если выбрать этот параметр, команда **Далее** изменится на **"Готово"**.</span><span class="sxs-lookup"><span data-stu-id="9e44e-220">When you choose this option, **Next** is changed to **Finish**.</span></span>

3.  <span data-ttu-id="9e44e-221">Заполните второй шаг диалогового окна, заполнив указанные ниже сведения, и нажмите кнопку **Готово** , чтобы вернуться на консоль управления клиентом.</span><span class="sxs-lookup"><span data-stu-id="9e44e-221">Complete the second step of the dialog box by completing the following information, and then click **Finish** to return to the Client Management Console:</span></span>

    1.  <span data-ttu-id="9e44e-222">**Изменить значок**— нажмите эту кнопку, чтобы изменить значок приложения.</span><span class="sxs-lookup"><span data-stu-id="9e44e-222">**Change Icon**—Click this button to change the application icon.</span></span> <span data-ttu-id="9e44e-223">Выберите один из доступных значков или перейдите к новому расположению и щелкните значок.</span><span class="sxs-lookup"><span data-stu-id="9e44e-223">Select one of the available icons, or browse to a new location and select an icon.</span></span>

    2.  <span data-ttu-id="9e44e-224">**Открытие файлов с помощью выбранного приложения**— выберите этот переключатель, чтобы открыть файл в существующем приложении.</span><span class="sxs-lookup"><span data-stu-id="9e44e-224">**Open files with the selected application**—Select this radio button to open the file with an existing application.</span></span> <span data-ttu-id="9e44e-225">Выберите приложение из раскрывающегося списка доступных приложений.</span><span class="sxs-lookup"><span data-stu-id="9e44e-225">Choose an application from the drop-down list of available applications.</span></span>

    3.  <span data-ttu-id="9e44e-226">**Откройте файл с ассоциацией, описанной в этом OSD-файле**— выберите этот переключатель, чтобы задать файл дескриптора программного обеспечения (OSD), определяющий приложение, которое использовалось для открытия файла.</span><span class="sxs-lookup"><span data-stu-id="9e44e-226">**Open file with the association described in this OSD file**—Select this radio button to specify an Open Software Descriptor (OSD) file that determines the application used to open the file.</span></span> <span data-ttu-id="9e44e-227">Нажмите кнопку Обзор, чтобы выбрать существующее расположение, или введите в это поле путь или URL-адрес в формате HTTP.</span><span class="sxs-lookup"><span data-stu-id="9e44e-227">Use the browse button to select an existing location, or enter a path or HTTP-formatted URL in this field.</span></span>

## <span data-ttu-id="9e44e-228">Удаление сопоставления типов файлов для приложения App-V</span><span class="sxs-lookup"><span data-stu-id="9e44e-228">How to delete a file type association for an App-V application</span></span>


<span data-ttu-id="9e44e-229">Для удаления сопоставления типов файлов можно использовать описанную ниже процедуру.</span><span class="sxs-lookup"><span data-stu-id="9e44e-229">You can use the following procedure to delete a file type association.</span></span> <span data-ttu-id="9e44e-230">Узел " **сопоставления типов файлов** " находится на одном уровне под узлом **Application Virtualization** в области " **область** ".</span><span class="sxs-lookup"><span data-stu-id="9e44e-230">The **File Type Associations** node is one level below the **Application Virtualization** node in the **Scope** pane.</span></span> <span data-ttu-id="9e44e-231">При выборе этого узла в области **результатов** отображается список сопоставлений типов файлов.</span><span class="sxs-lookup"><span data-stu-id="9e44e-231">When you select this node, the **Results** pane displays a list of file type associations.</span></span>

**<span data-ttu-id="9e44e-232">Удаление сопоставления типа файла</span><span class="sxs-lookup"><span data-stu-id="9e44e-232">To remove a file type association</span></span>**

1.  <span data-ttu-id="9e44e-233">В области **результатов** щелкните правой кнопкой мыши расширение сопоставления типа файла, которое вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="9e44e-233">In the **Results** pane, right-click the extension of the file type association you want to delete.</span></span>

2.  <span data-ttu-id="9e44e-234">В раскрывающемся меню выберите команду **Удалить** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-234">Select **Delete** from the pop-up menu.</span></span>

3.  <span data-ttu-id="9e44e-235">Нажмите кнопку **Да** , чтобы удалить связь, или кнопку **нет** , чтобы вернуться в область **результатов** .</span><span class="sxs-lookup"><span data-stu-id="9e44e-235">Click **Yes** to delete the association, or click **No** to return to the **Results** pane.</span></span>

## <span data-ttu-id="9e44e-236">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9e44e-236">Related topics</span></span>


[<span data-ttu-id="9e44e-237">Клиент Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9e44e-237">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





