---
title: Установка и удаление приложения в рабочей области MED-V
description: Установка и удаление приложения в рабочей области MED-V
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827219"
---
# <span data-ttu-id="23f6d-103">Установка и удаление приложения в рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="23f6d-103">Installing and Removing an Application on the MED-V Workspace</span></span>


<span data-ttu-id="23f6d-104">Приложения, несовместимые с операционной системой узла, можно запускать в рабочей области MED-V и открывать в рабочей области MED-V таким же образом, как и при их открытии на главном компьютере, **а также с** помощью ярлыка localhost.</span><span class="sxs-lookup"><span data-stu-id="23f6d-104">Applications that are incompatible with the host operating system can be run in the MED-V workspace and opened in the MED-V workspace in the same manner in which they are opened from the host computer, on the **Start** menu or by using a localhost shortcut.</span></span>

<span data-ttu-id="23f6d-105">После развертывания рабочей области MED-V вы можете использовать несколько различных параметров для установки и удаления приложений в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="23f6d-105">After you have deployed a MED-V workspace, you have several different options available to you for installing and removing applications in the MED-V workspace.</span></span> <span data-ttu-id="23f6d-106">Ниже указаны эти параметры.</span><span class="sxs-lookup"><span data-stu-id="23f6d-106">These options include the following:</span></span>

-   [<span data-ttu-id="23f6d-107">Использование групповой политики</span><span class="sxs-lookup"><span data-stu-id="23f6d-107">Using Group Policy</span></span>](#bkmk-grouppolicy)

-   [<span data-ttu-id="23f6d-108">Использование электронной системы распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="23f6d-108">Using an Electronic Software Distribution System</span></span>](#bkmk-esd)

-   [<span data-ttu-id="23f6d-109">Использование Application Virtualization (APP-V)</span><span class="sxs-lookup"><span data-stu-id="23f6d-109">Using Application Virtualization (APP-V)</span></span>](#bkmk-appv)

-   [<span data-ttu-id="23f6d-110">Обновление основного изображения</span><span class="sxs-lookup"><span data-stu-id="23f6d-110">Updating the Core Image</span></span>](#bkmk-coreimage)

<span data-ttu-id="23f6d-111">**Важно!**  Чтобы убедиться, что установленное приложение будет автоматически Опубликовано на узле, установите его на виртуальной машине для **всех пользователей**.</span><span class="sxs-lookup"><span data-stu-id="23f6d-111">**Important** To make sure that an installed application is automatically published to the host, install the application on the virtual machine for **All Users**.</span></span> <span data-ttu-id="23f6d-112">Дополнительные сведения о публикации приложений можно найти в разделе [Публикация и Отмена публикации приложения в рабочей области MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="23f6d-112">For more information about application publishing, see [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span>

 

<span data-ttu-id="23f6d-113">**Совет**  MED-V не поддерживает перенаправление "гость-узел" для обработки содержимого, например двойным щелчком документа Microsoft Word в Internet Explorer в рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="23f6d-113">**Tip** MED-V does not support guest-to-host redirection for content handling, such as double-clicking a Microsoft Word document in Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="23f6d-114">Поэтому необходимые приложения, такие как Microsoft Word, должны быть установлены в рабочей области MED-V для предоставления функциональных возможностей обработки содержимого по умолчанию, которые могут быть ожидаемы конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="23f6d-114">Therefore, the required applications, such as Microsoft Word, must be installed in MED-V workspace to provide the default content handling functionality that an end user might expect.</span></span>

 

## <a href="" id="bkmk-grouppolicy"></a> <span data-ttu-id="23f6d-115">Добавление и удаление приложений с помощью групповой политики</span><span class="sxs-lookup"><span data-stu-id="23f6d-115">Adding and Removing Applications by Using Group Policy</span></span>


<span data-ttu-id="23f6d-116">Вы можете использовать групповую политику и объекты групповой политики, чтобы назначать и публиковать приложения для всех или некоторых рабочих областей MED-V в Организации.</span><span class="sxs-lookup"><span data-stu-id="23f6d-116">You can use Group Policy and Group Policy objects to assign or publish applications to all or some MED-V workspaces in your enterprise.</span></span> <span data-ttu-id="23f6d-117">Для назначенных приложений, когда пользователь входит в систему на своем компьютере, приложение появляется в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="23f6d-117">For assigned applications, when an end user logs on to their computer, the application appears on the **Start** menu.</span></span> <span data-ttu-id="23f6d-118">Когда приложение выберет новое приложение в первый раз, оно будет установлено и готово к использованию.</span><span class="sxs-lookup"><span data-stu-id="23f6d-118">When they select the new application for the first time, the application installs and is ready for use.</span></span> <span data-ttu-id="23f6d-119">В случае опубликованных приложений приложение не отображается в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="23f6d-119">For published applications, the application does not appear on the **Start** menu.</span></span> <span data-ttu-id="23f6d-120">Это можно сделать только в том случае, если конечным пользователем является установка с помощью средства " **Установка и удаление программ** " на **панели управления** или открытие файла, связанного с приложением.</span><span class="sxs-lookup"><span data-stu-id="23f6d-120">It is only available for the end user to install by using **Add or Remove Programs** in **Control Panel** or by opening a file that is associated with the application.</span></span>

<span data-ttu-id="23f6d-121">Вы также можете использовать групповую политику и объекты групповой политики так же, как и для удаления приложений из рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="23f6d-121">You can also use Group Policy and Group Policy objects in the same manner to remove applications from the MED-V workspace.</span></span>

<span data-ttu-id="23f6d-122">Дополнительные сведения о том, как добавлять и удалять приложения с помощью групповой политики, можно найти в разделе [Установка программного обеспечения групповой политики](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="23f6d-122">For more information about how to add and remove applications by using Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

## <a href="" id="bkmk-esd"></a> <span data-ttu-id="23f6d-123">Добавление и удаление приложений с помощью системы ESD</span><span class="sxs-lookup"><span data-stu-id="23f6d-123">Adding and Removing Applications by Using an ESD System</span></span>


<span data-ttu-id="23f6d-124">Система электронной рассылки программного обеспечения (ESD) разработана для эффективного развертывания программного обеспечения и других сведений на множестве разных компьютеров через сетевые подключения.</span><span class="sxs-lookup"><span data-stu-id="23f6d-124">An electronic software distribution (ESD) system is designed to efficiently deploy software and other information to many different computers over network connections.</span></span> <span data-ttu-id="23f6d-125">Если ваша организация использует систему ESD для развертывания программного обеспечения, вы можете использовать ее для добавления и удаления приложений в рабочих областях MED-V так же, как и при добавлении и удалении приложений на физических компьютерах.</span><span class="sxs-lookup"><span data-stu-id="23f6d-125">If your organization uses an ESD system to deploy software, you can use it to add and remove applications on MED-V workspaces just as you add and remove applications on physical computers.</span></span>

## <a href="" id="bkmk-appv"></a> <span data-ttu-id="23f6d-126">Добавление и удаление приложений с помощью APP-V</span><span class="sxs-lookup"><span data-stu-id="23f6d-126">Adding and Removing Applications by Using APP-V</span></span>


<span data-ttu-id="23f6d-127">Microsoft Application Virtualization (App-V) предоставляет возможности администрирования для обеспечения доступности приложений для конечных пользователей без необходимости устанавливать приложения непосредственно на эти компьютеры.</span><span class="sxs-lookup"><span data-stu-id="23f6d-127">Microsoft Application Virtualization (App-V) provides the administrative capability to make applications available to end-user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="23f6d-128">Вы можете использовать MED-V и App-V вместе, если, например, в вашей организации есть приложения, которые вы передумали с помощью App-V в Windows XP, и их повторная последовательность задерживает переход на Windows 7.</span><span class="sxs-lookup"><span data-stu-id="23f6d-128">You might want to use MED-V and App-V together if, for example, your organization has applications that you sequenced with App-V in Windows XP, and re-sequencing them would delay your migration to Windows 7.</span></span>

<span data-ttu-id="23f6d-129">Для добавления и удаления виртуальных приложений в развернутой рабочей области MED-V вы можете использовать MED-V вместе с App-V.</span><span class="sxs-lookup"><span data-stu-id="23f6d-129">You can use MED-V together with App-V to add and remove virtual applications on a deployed MED-V workspace.</span></span> <span data-ttu-id="23f6d-130">Чтобы управлять приложениями таким образом, необходимо сначала установить агент App-V в гостевой операционной системе MED-V.</span><span class="sxs-lookup"><span data-stu-id="23f6d-130">To manage applications in this manner, you must first install the App-V agent on the MED-V guest operating system.</span></span> <span data-ttu-id="23f6d-131">Затем вы можете использовать App-V в рабочей области MED-V для добавления и удаления виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="23f6d-131">You can then use App-V in the MED-V workspace to add and remove the virtual applications.</span></span>

<span data-ttu-id="23f6d-132">Сведения о том, как установить и использовать App-V, можно найти в разделе [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="23f6d-132">For information about how to install and use App-V, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

<span data-ttu-id="23f6d-133">**Важно!**  В приложениях App-V, опубликованных в рабочей области MED-V, есть сопоставления типов файлов, которые не могут перенаправлять на гостевой виртуальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="23f6d-133">**Important** App-V applications that you publish to the MED-V workspace have file-type associations that cannot redirect from the host computer to the guest virtual machine.</span></span> <span data-ttu-id="23f6d-134">Тем не менее конечный пользователь по-прежнему может получить доступ к этим типам файлов, щелкнув **файл**, а затем нажать кнопку **Открыть** в опубликованном приложении App-V.</span><span class="sxs-lookup"><span data-stu-id="23f6d-134">However, the end user can still access these file types by clicking **File**, and then by clicking **Open** on the published App-V application.</span></span>

<span data-ttu-id="23f6d-135">Чтобы принудительно перенаправлять эти сопоставления типов файлов, запросите приложение App-V для сопоставлений типов файлов, введя следующую команду в командной строке гостевой виртуальной машины: **SFTMIME/Query obj: Type (тип**).</span><span class="sxs-lookup"><span data-stu-id="23f6d-135">To force redirection of those file-type associations, query App-V for mapped file type associations by typing the following at a command prompt in the guest virtual machine: **sftmime /QUERY OBJ:TYPE**.</span></span> <span data-ttu-id="23f6d-136">Затем сопоставьте эти сопоставления типов файлов на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="23f6d-136">Then, map those file type associations in the host computer.</span></span>

 

## <a href="" id="bkmk-coreimage"></a> <span data-ttu-id="23f6d-137">Добавление и удаление приложений на базовом изображении</span><span class="sxs-lookup"><span data-stu-id="23f6d-137">Adding and Removing Applications on the Core Image</span></span>


<span data-ttu-id="23f6d-138">Несмотря на то что не рассматривается рекомендация для MED-V, вы можете добавлять и удалять приложения непосредственно на базовом изображении.</span><span class="sxs-lookup"><span data-stu-id="23f6d-138">Although not considered a MED-V best practice, you can add and remove applications directly on the core image.</span></span> <span data-ttu-id="23f6d-139">После добавления или удаления приложения вы можете повторно развернуть рабочую область MED-V в своей организации, как только вы развернули ее первоначально.</span><span class="sxs-lookup"><span data-stu-id="23f6d-139">After you have added or removed an application, you can redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

<span data-ttu-id="23f6d-140">Дополнительные сведения о том, как добавлять и удалять приложения в базовом образе, можно найти в разделе [Установка приложений в образе виртуального компьютера с Windows](installing-applications-on-a-windows-virtual-pc-image.md).</span><span class="sxs-lookup"><span data-stu-id="23f6d-140">For more information about how to add or remove applications on the core image, see [Installing Applications on a Windows Virtual PC Image](installing-applications-on-a-windows-virtual-pc-image.md).</span></span>

<span data-ttu-id="23f6d-141">**Важно!**  Мы не рекомендуем использовать этот метод управления приложениями.</span><span class="sxs-lookup"><span data-stu-id="23f6d-141">**Important** We do not recommend this method of managing applications.</span></span> <span data-ttu-id="23f6d-142">Если вы добавляете или удаляете приложения на базовом образе и повторно развертываете рабочую область MED-V в своей организации, сначала необходимо выполнить настройку, а все данные, сохраненные на виртуальной машине, будут утрачены.</span><span class="sxs-lookup"><span data-stu-id="23f6d-142">If you add or remove applications on the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved on the virtual machine is lost.</span></span>

 

<span data-ttu-id="23f6d-143">**Примечание**  Несмотря на то что приложение установлено в рабочую область MED-V, вам также может потребоваться опубликовать приложение, прежде чем оно станет доступно конечному пользователю.</span><span class="sxs-lookup"><span data-stu-id="23f6d-143">**Note** Even though an application is installed into a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="23f6d-144">Например, может потребоваться опубликовать установленное приложение, если в меню " **Пуск** " не был автоматически создан ярлык.</span><span class="sxs-lookup"><span data-stu-id="23f6d-144">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span> <span data-ttu-id="23f6d-145">Кроме того, чтобы отменить публикацию приложения, возможно, потребуется вручную удалить ярлык из меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="23f6d-145">Likewise, to unpublish an application, you might have to manually remove a shortcut from the **Start** menu.</span></span>

<span data-ttu-id="23f6d-146">По умолчанию большинство приложений публикуются на момент их установки, когда ярлыки создаются и включаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="23f6d-146">By default, most applications are published at the time that they are installed, when shortcuts are automatically created and enabled.</span></span>

 

## <span data-ttu-id="23f6d-147">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="23f6d-147">Related topics</span></span>


[<span data-ttu-id="23f6d-148">Проверка публикации приложений</span><span class="sxs-lookup"><span data-stu-id="23f6d-148">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="23f6d-149">Публикация и отмена публикации приложения в рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="23f6d-149">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





