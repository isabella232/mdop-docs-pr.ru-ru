---
title: Планирование совместимости приложений и операционной системы
description: Планирование совместимости приложений и операционной системы
author: dansimp
ms.assetid: cdb0a7f0-9da4-4562-8277-12972eb0fea8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b10da2c870e5ddc32098136225515cdd0523809
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825469"
---
# <span data-ttu-id="0d92d-103">Планирование совместимости приложений и операционной системы</span><span class="sxs-lookup"><span data-stu-id="0d92d-103">Planning for Application Operating System Compatibility</span></span>


<span data-ttu-id="0d92d-104">В этой статье описано, как устранить проблемы с совместимостью операционной системы приложения, а также определить, как работает виртуализация классической версии Microsoft Enterprise для настольных систем (MED-V) 2,0, как решение для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="0d92d-104">This topic helps determine how to resolve application operating system compatibility issues, and discusses how Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 works as a solution for your organization.</span></span>

<span data-ttu-id="0d92d-105">В этой статье обсуждаются бизнес-требования для MED-V и сравниваются режимы MED-V — Windows XP и Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="0d92d-105">This topic discusses the business requirements for MED-V and compares MED-V to Windows XP Mode and Microsoft Application Virtualization (App-V):</span></span>

-   [<span data-ttu-id="0d92d-106">Бизнес-требования для MED-V</span><span class="sxs-lookup"><span data-stu-id="0d92d-106">Business Requirements for MED-V</span></span>](#bkmk-whenmedv)

-   [<span data-ttu-id="0d92d-107">Преимущества режима MED-V и Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d92d-107">Benefits of MED-V versus Windows XP Mode</span></span>](#bkmk-medvvsxp)

-   [<span data-ttu-id="0d92d-108">Преимущества, предоставляемые MED-V и App-V</span><span class="sxs-lookup"><span data-stu-id="0d92d-108">Benefits of MED-V versus App-V</span></span>](#bkmk-medvvsappv)

## <a href="" id="bkmk-whenmedv"></a><span data-ttu-id="0d92d-109">Бизнес-требования для MED-V</span><span class="sxs-lookup"><span data-stu-id="0d92d-109">Business Requirements for MED-V</span></span>


<span data-ttu-id="0d92d-110">Когда ИТ-отдел вашей компании определяет, нужно ли переходить на Windows 7, необходимо уделять особое внимание корпоративным приложениям и веб-бизнес-приложениям, чтобы убедиться, что они могут выполняться в новой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="0d92d-110">When your company’s IT department is determining whether to upgrade to Windows 7, it must pay attention to its line-of-business applications and web-based line-of-business applications to make certain that these can run on the new operating system.</span></span> <span data-ttu-id="0d92d-111">Часто эти приложения и URL-адреса были созданы для работы в более ранней версии Windows или Internet Explorer, и при попытке использовать их в новой операционной системе могут возникать проблемы.</span><span class="sxs-lookup"><span data-stu-id="0d92d-111">Often, these applications and URLs were created to work specifically with an older version of Windows or Internet Explorer, and problems can occur when trying to use them in the new operating system.</span></span> <span data-ttu-id="0d92d-112">Корпорация Майкрософт выпускает различные методы для решения проблем с совместимостью, которые могут возникнуть при обновлении, например набора средств для обеспечения совместимости приложений (ACT) и помощника по совместимости программ для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0d92d-112">Microsoft offers many different methods for handling the various compatibility issues that can occur when you upgrade, such as the Application Compatibility Toolkit (ACT) and the Windows 7 Program Compatibility Assistant.</span></span> <span data-ttu-id="0d92d-113">Но даже после того как все приложения были проверены на совместимость и были обнаружены исправления, некоторые приложения по-прежнему работают неправильно в Windows 7 или слишком дороги для их устранения.</span><span class="sxs-lookup"><span data-stu-id="0d92d-113">But even after all applications have been tested for compatibility and fixes have been determined, some applications still do not work correctly on Windows 7 or are too costly to resolve.</span></span>

<span data-ttu-id="0d92d-114">С помощью MED-V вы можете запускать эти старые приложения с помощью виртуальной среды Windows, работающей под управлением Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0d92d-114">By using MED-V, you can run these legacy applications through a Windows Virtual PC environment that is running Windows XP.</span></span> <span data-ttu-id="0d92d-115">Так как вам больше не нужно тестировать и проверять эти проблемные приложения в новой операционной системе перед обновлением, переход на Windows 7 будет гораздо более плавен и быстрее.</span><span class="sxs-lookup"><span data-stu-id="0d92d-115">Because you no longer have to test and validate these problem applications on the new operating system before upgrading, your migration to Windows 7 is much smoother and quicker.</span></span>

### <span data-ttu-id="0d92d-116">Использование контрольного списка для MED-V</span><span class="sxs-lookup"><span data-stu-id="0d92d-116">Using MED-V Checklist</span></span>

<span data-ttu-id="0d92d-117">Если к вам применимы следующие сценарии:</span><span class="sxs-lookup"><span data-stu-id="0d92d-117">Consider MED-V if any of the following scenarios apply to you:</span></span>

-   <span data-ttu-id="0d92d-118">Это крупная организация (например, 500 пользователей и т. д.), Корпоративное соглашение с корпорацией Майкрософт и планирование обновления до Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0d92d-118">You are a large organization (for example, 500 users and more), have an Enterprise Agreement with Microsoft, and plan to upgrade to Windows 7.</span></span>

-   <span data-ttu-id="0d92d-119">Вы протестировали бизнес-приложения и нашли некоторые из них, несовместимые с Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0d92d-119">You have tested your line-of-business applications and have found some that are incompatible with Windows 7.</span></span>

-   <span data-ttu-id="0d92d-120">Вы решили проблемы совместимости для некоторых из этих проблемных приложений, обновив приложение или используя оболочку, предоставленную корпорацией Майкрософт, например, набор средств для обеспечения совместимости приложений (ACT), но для некоторых приложений проблемы совместимости остаются.</span><span class="sxs-lookup"><span data-stu-id="0d92d-120">You have resolved the compatibility issues for some of these problem applications by upgrading the application or by using a Microsoft-provided shim, such as the Application Compatibility Toolkit (ACT), but compatibility issues remain for some applications.</span></span>

-   <span data-ttu-id="0d92d-121">Вы рассматривали приложение App-V как вариант для доставки несовместимых приложений и действительно, что даже после реализации App-V, вы все равно можете устранить проблемы совместимости с операционной системой приложения, которые необходимо решить.</span><span class="sxs-lookup"><span data-stu-id="0d92d-121">You have considered App-V as an option for delivering the incompatible applications and have concluded that even after you implement App-V, you still have application operating system compatibility issues that you must address.</span></span>

-   <span data-ttu-id="0d92d-122">Вы рассматривали режим Windows XP как решение и определили, что он не является эффективным из-за следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="0d92d-122">You have considered Windows XP Mode as a solution and have determined that it is not an efficient option because:</span></span>

    -   <span data-ttu-id="0d92d-123">Вы хотите, чтобы все конечные пользователи одновременно могли развертывать виртуальные образы, которые содержат проблемные приложения, а не по отдельности, а виртуальные образы автоматически присоединены к этому домену.</span><span class="sxs-lookup"><span data-stu-id="0d92d-123">You want to be able to deploy virtual images that contain the problem applications to all end users at the same time, instead of individually, and have the virtual images automatically joined to the domain.</span></span>

    -   <span data-ttu-id="0d92d-124">Вы решили, что это значительно выгодно для управления этими старыми приложениями (которые будут доставляться практически) и управления параметрами виртуальных ПК Windows в централизованном расположении, а не на рабочем столе каждого конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="0d92d-124">You have decided it is much more cost effective to manage these legacy applications (that are delivered virtually) and control the Windows Virtual PC settings from a centralized location instead of on each end user’s desktop.</span></span>

    -   <span data-ttu-id="0d92d-125">Вы хотите иметь возможность обновлять и поддерживать виртуальные машины в масштабе, а не на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="0d92d-125">You want to be able to update and support the virtual machines in scale instead of per desktop.</span></span>

    -   <span data-ttu-id="0d92d-126">Вы хотите предоставить возможность перенаправления URL-адресов, которые лучше всего работают в более ранней версии Internet Explorer, на виртуальные машины и легко управлять перенаправлением URL-адресов позже.</span><span class="sxs-lookup"><span data-stu-id="0d92d-126">You want the ability to redirect URLs that run better on an older version of Internet Explorer to the virtual machines and to easily manage URL redirection later.</span></span>

-   <span data-ttu-id="0d92d-127">Вы определили, что это было бы более выгодным и полезным для немедленного перехода на Windows 7, и решили отложить решение проблем, связанных с совместимостью приложений, до более поздней даты, зная о том, что у вас есть решения в MED-V.</span><span class="sxs-lookup"><span data-stu-id="0d92d-127">You have determined that it would be more cost effective and helpful to upgrade to Windows 7 as soon as possible and have decided to postpone resolving your remaining application compatibility issues until a later date, knowing that you have a solution available in MED-V.</span></span>

## <a href="" id="bkmk-medvvsxp"></a> <span data-ttu-id="0d92d-128">Преимущества режима MED-V и Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d92d-128">Benefits of MED-V versus Windows XP Mode</span></span>


<span data-ttu-id="0d92d-129">Windows Virtual PC для Windows 7 позволяет одновременно работать с различными версиями операционной системы на одном устройстве и включены в Windows 7 Профессиональная Edition и более позднюю версию.</span><span class="sxs-lookup"><span data-stu-id="0d92d-129">Windows Virtual PC for Windows 7 lets you run different versions of an operating system at the same time on a single device and is included in Windows 7 Professional Edition and higher.</span></span>

<span data-ttu-id="0d92d-130">Функция режима Windows XP использует преимущества Virtual PC для Windows, предоставляя предварительно настроенные образы Windows XP, позволяющие создавать виртуальные среды Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0d92d-130">Windows XP Mode functionality takes advantage of Windows Virtual PC by providing a preconfigured Windows XP image that lets you create a virtual Windows XP environment.</span></span> <span data-ttu-id="0d92d-131">В этой виртуальной среде вы можете вручную устанавливать приложения, несовместимые с Windows 7, и работать с ними без проблем с рабочим столом в Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="0d92d-131">In this virtual environment, you can manually install applications that are incompatible with Windows 7 and that run seamlessly from your desktop through Windows Virtual PC.</span></span>

**<span data-ttu-id="0d92d-132">В режиме Windows XP вы можете сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="0d92d-132">By using Windows XP Mode, you can do the following:</span></span>**

-   <span data-ttu-id="0d92d-133">Запускайте приложения, совместимые с Windows XP, в виртуальной машине, работающей в Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="0d92d-133">Run applications that are compatible with Windows XP inside a virtual machine that runs in Windows Virtual PC.</span></span>

-   <span data-ttu-id="0d92d-134">Опубликуйте эти приложения на рабочем столе или в меню программы узла.</span><span class="sxs-lookup"><span data-stu-id="0d92d-134">Publish these applications to the host’s desktop or Program menu.</span></span>

<span data-ttu-id="0d92d-135">Если вы хотите, чтобы эти виртуальные машины в крупном масштабе были включены в корпоративную миграцию на Windows 7, вы должны иметь возможность быстро развернуть виртуальные машины, подготовить и настроить их, управлять параметрами и легко поддерживать их.</span><span class="sxs-lookup"><span data-stu-id="0d92d-135">When you want to deliver these virtual machines on a large scale as part of an enterprise migration to Windows 7, you must be able to deploy the virtual machines quickly, provision, and customize them efficiently, control their settings, and support them easily.</span></span>

<span data-ttu-id="0d92d-136">В Windows XP для обеспечения совместимости приложений в масштабах предприятия используются службы MED-V.</span><span class="sxs-lookup"><span data-stu-id="0d92d-136">MED-V builds upon Windows XP Mode to deliver enterprise-wide application compatibility.</span></span> <span data-ttu-id="0d92d-137">В то время как режим Windows XP ограничивает возможности виртуальных приложений для пользователей и малых предприятий, MED-V обеспечивает крупномасштабное развертывание предварительно настроенных изображений Windows XP в корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="0d92d-137">Whereas Windows XP mode is limited to providing virtual application functionality to individuals and small businesses, MED-V allows for large-scale deployments of preconfigured Windows XP images throughout your corporate network.</span></span> <span data-ttu-id="0d92d-138">Она предоставляет решение для управления конфигурацией, развертыванием и обслуживанием этих виртуальных рабочих областей MED-V в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="0d92d-138">It gives you an enterprise-ready management solution for the configuration, deployment, and maintenance of these virtual MED-V workspaces.</span></span> <span data-ttu-id="0d92d-139">MED-V также предоставляет enterpriseadministrators набор политик для управления использованием изображений.</span><span class="sxs-lookup"><span data-stu-id="0d92d-139">MED-V also gives enterpriseadministrators a set of policies to control image use.</span></span> <span data-ttu-id="0d92d-140">Сюда входят пользователи, у которых есть доступ к определенным приложениям в этих изображениях.</span><span class="sxs-lookup"><span data-stu-id="0d92d-140">This includes which users will have access to which specific applications within these images.</span></span>

**<span data-ttu-id="0d92d-141">С помощью MED-V вы можете сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="0d92d-141">By using MED-V, you can do the following:</span></span>**

-   <span data-ttu-id="0d92d-142">Обновите операционную систему до новой операционной системы, не требуя проверки и устранения всех несовместимых приложений и URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="0d92d-142">Upgrade to your new operating system without having to test and resolve every incompatible application and URL.</span></span>

-   <span data-ttu-id="0d92d-143">Развертывайте образы виртуальных Windows XP, которые автоматически присоединены к домену и настроены для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="0d92d-143">Deploy virtual Windows XP images that are automatically domain-joined and customized per user.</span></span>

-   <span data-ttu-id="0d92d-144">Подготовка к работе приложений и перенаправления URL-адресов для пользователей.</span><span class="sxs-lookup"><span data-stu-id="0d92d-144">Provision applications and URL redirection information to users.</span></span>

-   <span data-ttu-id="0d92d-145">Управление параметрами виртуальных ПК в Windows.</span><span class="sxs-lookup"><span data-stu-id="0d92d-145">Control the Windows Virtual PC settings.</span></span>

-   <span data-ttu-id="0d92d-146">Поддерживать и поддерживать конечные точки с помощью наблюдения и устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="0d92d-146">Maintain and support endpoints through monitoring and troubleshooting.</span></span>

-   <span data-ttu-id="0d92d-147">Убедитесь, что гостевые компьютеры обновлены, даже если приостановлено.</span><span class="sxs-lookup"><span data-stu-id="0d92d-147">Ensure that guest computers are patched, even if in a suspended state.</span></span>

-   <span data-ttu-id="0d92d-148">Автоматизация создания виртуальных машин для пользователей и инициализации Sysprep.</span><span class="sxs-lookup"><span data-stu-id="0d92d-148">Automate per-user virtual machine creation and sysprep initialization.</span></span>

-   <span data-ttu-id="0d92d-149">Легко диагностировать проблемы на главном и гостевых компьютерах.</span><span class="sxs-lookup"><span data-stu-id="0d92d-149">Easily diagnose issues on the host and guest computers.</span></span>

-   <span data-ttu-id="0d92d-150">Беспроблемное Управление гостевыми компьютерами, подключенными через режим NAT в виртуальной машине Windows.</span><span class="sxs-lookup"><span data-stu-id="0d92d-150">Seamlessly manage guest computers that are connected through Windows Virtual PC NAT mode.</span></span>

## <a href="" id="bkmk-medvvsappv"></a><span data-ttu-id="0d92d-151">Преимущества, предоставляемые MED-V и App-V</span><span class="sxs-lookup"><span data-stu-id="0d92d-151">Benefits of MED-V versus App-V</span></span>


<span data-ttu-id="0d92d-152">MED-V и App-V — это две самые разные технологии, которые могут легко работать вместе для решения проблем с совместимостью с операционной системой приложения.</span><span class="sxs-lookup"><span data-stu-id="0d92d-152">MED-V and App-V are two very different technologies that can easily work together to solve your application operating system compatibility issues.</span></span> <span data-ttu-id="0d92d-153">С помощью App-V вы создаете отдельный пакет для каждого приложения, каждый из которых затем сохраняется отдельно от остальных.</span><span class="sxs-lookup"><span data-stu-id="0d92d-153">By using App-V, you create an individualized package for each application, each of which is then kept separate from the others.</span></span> <span data-ttu-id="0d92d-154">Каждое виртуальное приложение может сразу же быть доставлено конечному пользователю, что очень полезно для стратегии развертывания Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0d92d-154">Each virtual application can then be immediately delivered to the end user, which is very useful for a Windows 7 deployment strategy.</span></span>

<span data-ttu-id="0d92d-155">В MED-V приложения не обрабатываются по отдельности.</span><span class="sxs-lookup"><span data-stu-id="0d92d-155">MED-V does not handle applications individually.</span></span> <span data-ttu-id="0d92d-156">Вместо этого он создает дополнительный экземпляр Windows XP на том же компьютере, на котором работает Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0d92d-156">Instead, it creates an additional instance of Windows XP on the same desktop that is running Windows 7.</span></span> <span data-ttu-id="0d92d-157">Вы можете установить столько приложений, сколько необходимо, и управлять этим изображением так же, как и любым другим настольным компьютером в Организации.</span><span class="sxs-lookup"><span data-stu-id="0d92d-157">You can install as many applications as necessary into this virtual image and manage the image just as you would any other desktop in your organization.</span></span>

<span data-ttu-id="0d92d-158">Кроме того, вы можете использовать MED-V вместе с App-V для установки, публикации и управления виртуальными приложениями, упорядоченными в App-V, с помощью MED-V.</span><span class="sxs-lookup"><span data-stu-id="0d92d-158">In addition, you can use MED-V together with App-V so that virtual applications that are sequenced through App-V are installed, published, and managed by using MED-V.</span></span>

## <span data-ttu-id="0d92d-159">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0d92d-159">Related topics</span></span>


[<span data-ttu-id="0d92d-160">Определение и планирование развертывания MED-V</span><span class="sxs-lookup"><span data-stu-id="0d92d-160">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

 

 





