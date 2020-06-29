---
title: Публикация и отмена публикации приложения в рабочей области MED-V
description: Публикация и отмена публикации приложения в рабочей области MED-V
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826922"
---
# <span data-ttu-id="b3daf-103">Публикация и отмена публикации приложения в рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="b3daf-103">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>


<span data-ttu-id="b3daf-104">Несмотря на то что приложение установлено в рабочей области MED-V, вам также может потребоваться опубликовать приложение, прежде чем оно станет доступно конечному пользователю.</span><span class="sxs-lookup"><span data-stu-id="b3daf-104">Even though an application is installed in a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="b3daf-105">По умолчанию большинство приложений публикуются на момент их установки, а также для создания и включения сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="b3daf-105">By default, most applications are published at the time that they are installed and shortcuts are created and enabled.</span></span>

<span data-ttu-id="b3daf-106">В некоторых случаях вам может потребоваться установить приложения в рабочую область для MED-V, не открывая их пользователям, например антивирусному программному обеспечению.</span><span class="sxs-lookup"><span data-stu-id="b3daf-106">In some cases, you might want to install applications on the MED-V workspace without making them available to the end user, for example, virus-scanning software.</span></span> <span data-ttu-id="b3daf-107">Кроме того, существуют ситуации, в которых вы хотите опубликовать приложение, установленное в рабочей области MED-V, которое ранее было недоступно для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b3daf-107">Similarly, there are occasions in which you want to publish an application that is installed on the MED-V workspace that was previously unavailable to the end user.</span></span> <span data-ttu-id="b3daf-108">Например, может потребоваться опубликовать установленное приложение, если в меню " **Пуск** " не был автоматически создан ярлык.</span><span class="sxs-lookup"><span data-stu-id="b3daf-108">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span>

<span data-ttu-id="b3daf-109">**Важно!**  Если вы публикуете приложение, которое не поддерживает пути UNC, рекомендуется сопоставить приложение с диском.</span><span class="sxs-lookup"><span data-stu-id="b3daf-109">**Important** If you publish an application that does not support UNC paths, we recommend that you map the application to a drive.</span></span>

 

<span data-ttu-id="b3daf-110">Вы можете опубликовать или отменить публикацию приложений в развернутой рабочей области для MED-V, выполнив одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="b3daf-110">You can publish or unpublish applications to a deployed MED-V workspace by performing one of the following tasks:</span></span>

**<span data-ttu-id="b3daf-111">Публикация и Отмена публикации установленного приложения</span><span class="sxs-lookup"><span data-stu-id="b3daf-111">To publish or unpublish an installed application</span></span>**

1.  <span data-ttu-id="b3daf-112">Чтобы опубликовать приложение в развернутой рабочей области MED-V, Скопируйте ярлык этого приложения в следующую папку на виртуальной машине:</span><span class="sxs-lookup"><span data-stu-id="b3daf-112">To publish an application on a deployed MED-V workspace, copy a shortcut for that application to the following folder on the virtual machine:</span></span>

    <span data-ttu-id="b3daf-113">Меню C:\\Documents и Settings\\All Users\\Start</span><span class="sxs-lookup"><span data-stu-id="b3daf-113">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="b3daf-114">При необходимости используйте групповую политику или систему ESD, чтобы развернуть сценарий, который копирует ярлык для этого приложения в папку "все" в меню "все" Users\\Start.</span><span class="sxs-lookup"><span data-stu-id="b3daf-114">If it is necessary, use Group Policy or an ESD system to deploy a script that copies the shortcut for that application to the All Users\\Start Menu folder.</span></span>

2.  <span data-ttu-id="b3daf-115">Чтобы отменить публикацию приложения в развернутой рабочей области MED-V, удалите ярлык для этого приложения из следующей папки на виртуальной машине:</span><span class="sxs-lookup"><span data-stu-id="b3daf-115">To unpublish an application on a deployed MED-V workspace, delete the shortcut for that application from the following folder on the virtual machine:</span></span>

    <span data-ttu-id="b3daf-116">Меню C:\\Documents и Settings\\All Users\\Start</span><span class="sxs-lookup"><span data-stu-id="b3daf-116">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="b3daf-117">При необходимости используйте групповую политику или систему ESD для развертывания сценария, который удаляет сочетание клавиш для этого приложения, из папки "все" в меню "все Users\\Start".</span><span class="sxs-lookup"><span data-stu-id="b3daf-117">If it is necessary, use Group Policy or an ESD system to deploy a script that deletes the shortcut for that application from the All Users\\Start Menu folder.</span></span>

    <span data-ttu-id="b3daf-118">**Примечание**  Часто этот ярлык автоматически удаляется из меню **Пуск** главного компьютера при удалении приложения.</span><span class="sxs-lookup"><span data-stu-id="b3daf-118">**Note** Frequently, the shortcut is automatically deleted from the host computer **Start** menu when you uninstall the application.</span></span> <span data-ttu-id="b3daf-119">Тем не менее, в некоторых случаях, например, для рабочей области MED-V, настроенной для всех пользователей общего компьютера, может потребоваться вручную удалить ярлык в меню " **Пуск** " после удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="b3daf-119">However, in some cases, such as for a MED-V workspace that is configured for all users of a shared computer, you might have to manually delete the shortcut on the **Start** menu after the application is uninstalled.</span></span> <span data-ttu-id="b3daf-120">Это можно сделать, щелкнув ярлык правой кнопкой мыши и выбрав команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="b3daf-120">The end-user can do this by right-clicking the shortcut and selecting **Delete**.</span></span>

     

<span data-ttu-id="b3daf-121">Чтобы убедиться в том, что приложение опубликовано или не опубликовано, проверьте, доступен ли соответствующий ярлык в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="b3daf-121">To test that the application was published or unpublished, verify on the MED-V workspace whether the corresponding shortcut is available or not.</span></span>

<span data-ttu-id="b3daf-122">**Примечание**  Приложения, которые включены в пакет обновления 3 (SP3) для Windows XP и находятся в папке меню "Пуск" виртуальной машины, не публикуются автоматически на узле.</span><span class="sxs-lookup"><span data-stu-id="b3daf-122">**Note** Applications that are included in Windows XP SP3 and are located in the virtual machine Start Menu folder are not automatically published to the host.</span></span> <span data-ttu-id="b3daf-123">Они управляются параметрами реестра, которые блокируют автоматическую публикацию.</span><span class="sxs-lookup"><span data-stu-id="b3daf-123">They are controlled by registry settings that block automatic publishing.</span></span> <span data-ttu-id="b3daf-124">Дополнительные сведения можно найти в разделе [список исключений приложений для Windows Virtual PC](windows-virtual-pc-application-exclude-list.md).</span><span class="sxs-lookup"><span data-stu-id="b3daf-124">For more information, see [Windows Virtual PC Application Exclude List](windows-virtual-pc-application-exclude-list.md).</span></span>

 

**<span data-ttu-id="b3daf-125">Публикация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="b3daf-125">To publish Control Panel items</span></span>**

1.  <span data-ttu-id="b3daf-126">Создайте на виртуальной машине ярлык, на котором целевым объектом является имя элемента, например C:\\WINDOWS\\system32\\appwiz.cpl.</span><span class="sxs-lookup"><span data-stu-id="b3daf-126">Create a shortcut on the virtual machine where the target is the name of the item, such as C:\\WINDOWS\\system32\\appwiz.cpl.</span></span>

    <span data-ttu-id="b3daf-127">Сочетание клавиш должно быть либо создано в папку "%ALLUSERSPROFILE%\\Start Menu\\", либо в одной из вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="b3daf-127">The shortcut must be either created in or moved to the "%ALLUSERSPROFILE%\\Start Menu\\" folder or one of its subfolders.</span></span>

    <span data-ttu-id="b3daf-128">Элемент будет опубликован на главном компьютере в соответствующем месте в папке главного меню.</span><span class="sxs-lookup"><span data-stu-id="b3daf-128">The item will be published to the host computer in the corresponding location in the host Start Menu folder.</span></span>

2.  <span data-ttu-id="b3daf-129">Начните с ярлыка для элемента на узле.</span><span class="sxs-lookup"><span data-stu-id="b3daf-129">Start the shortcut for the item in the host.</span></span>

<span data-ttu-id="b3daf-130">**Внимание!**  При создании ярлыка не указывайте% SystemRoot% \\control.exe.</span><span class="sxs-lookup"><span data-stu-id="b3daf-130">**Caution** When you create the shortcut, do not specify %SystemRoot%\\control.exe.</span></span> <span data-ttu-id="b3daf-131">Это приложение не будет опубликовано, так как оно содержится в параметрах реестра, которые блокируют автоматическую публикацию.</span><span class="sxs-lookup"><span data-stu-id="b3daf-131">This application will not be published because it is contained in the registry settings that block automatic publishing.</span></span>

 

**<span data-ttu-id="b3daf-132">Как MED-V обрабатывает автоматическую публикацию приложений</span><span class="sxs-lookup"><span data-stu-id="b3daf-132">How MED-V handles automatic application publishing</span></span>**

1.  <span data-ttu-id="b3daf-133">Во время публикации приложения MED-V копирует ярлыки с гостевой виртуальной машины на главный компьютер, пытаясь сопоставить ее с иерархией папок, существующей в гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="b3daf-133">During application publishing, MED-V copies the shortcuts from the guest virtual machine to the host computer by trying to match the folder hierarchy that exists in the guest.</span></span> <span data-ttu-id="b3daf-134">Для этого MED-V копирует ярлыки с гостя на узел, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b3daf-134">By doing this, MED-V copies shortcuts from the guest to the host by following these steps:</span></span>

    1.  <span data-ttu-id="b3daf-135">MED-V пытается найти папку в разделе Start Menu\\Programs на главном компьютере с именем, совпадающим с папкой гостя, в которой находится сочетание клавиш.</span><span class="sxs-lookup"><span data-stu-id="b3daf-135">MED-V tries to locate a folder under Start Menu\\Programs in the host computer that is named the same as the folder in the guest where the shortcut resides.</span></span>

    2.  <span data-ttu-id="b3daf-136">Если совпадающей папки нет, MED-V затем пытается найти папку в папке главного меню, имя которой совпадает с папкой в гостевой системе, в которой находится сочетание клавиш.</span><span class="sxs-lookup"><span data-stu-id="b3daf-136">If there is no matching folder, MED-V then tries to locate a folder in the host Start Menu folder that is named the same as the folder in the guest where the shortcut resides.</span></span>

    3.  <span data-ttu-id="b3daf-137">Если совпадающей папки нет, MED-V копирует ярлык в папку по умолчанию на узле, в папке Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="b3daf-137">If there is no matching folder, MED-V copies the shortcut to the default folder on the host, the Start Menu\\Programs folder.</span></span>

2.  <span data-ttu-id="b3daf-138">Пример процесса публикации приложения:</span><span class="sxs-lookup"><span data-stu-id="b3daf-138">Example of application publishing process:</span></span>

    1.  <span data-ttu-id="b3daf-139">Если ярлык приложения опубликован в папке Start Menu\\Programs\\AppShortcuts на гостевой машине, то MED-V на главном компьютере в папке Start Menu\\Programs\\ AppShortcuts и, если она найдена, копирует ярлык в эту папку.</span><span class="sxs-lookup"><span data-stu-id="b3daf-139">If an application shortcut is published to the Start Menu\\Programs\\AppShortcuts folder in the guest, then MED-V looks in the host computer for a Start Menu\\Programs\\ AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    2.  <span data-ttu-id="b3daf-140">Если папка не найдена, то MED-V обнаруживает папку Start Menu\\AppShortcuts на главном компьютере и, если она найдена, копирует ярлык в эту папку.</span><span class="sxs-lookup"><span data-stu-id="b3daf-140">If the folder is not found, then MED-V looks in the host computer for a Start Menu\\AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    3.  <span data-ttu-id="b3daf-141">Если папка не найдена, то MED-V копирует ярлык в папку Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="b3daf-141">If the folder is not found, then MED-V copies the shortcut to the Start Menu\\Programs folder.</span></span>

<span data-ttu-id="b3daf-142">**Примечание**  В папке меню "Пуск" главного компьютера должна быть уже есть папка, в которой вы можете скопировать ярлык с помощью MED-V.</span><span class="sxs-lookup"><span data-stu-id="b3daf-142">**Note** A folder must already exist in the host computer Start Menu folder for MED-V to copy the shortcut there.</span></span> <span data-ttu-id="b3daf-143">В случае, если она еще не создана, MED-V не создает папку.</span><span class="sxs-lookup"><span data-stu-id="b3daf-143">MED-V does not create the folder if it does not already exist.</span></span>

 

## <span data-ttu-id="b3daf-144">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b3daf-144">Related topics</span></span>


[<span data-ttu-id="b3daf-145">Установка и удаление приложения в рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="b3daf-145">Installing and Removing an Application on the MED-V Workspace</span></span>](installing-and-removing-an-application-on-the-med-v-workspace.md)

[<span data-ttu-id="b3daf-146">Управление обновлениями программного обеспечения для рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="b3daf-146">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

[<span data-ttu-id="b3daf-147">Список исключений приложения Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b3daf-147">Windows Virtual PC Application Exclude List</span></span>](windows-virtual-pc-application-exclude-list.md)

 

 





