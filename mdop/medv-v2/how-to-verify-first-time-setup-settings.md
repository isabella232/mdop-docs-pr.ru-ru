---
title: Проверка параметров первой установки
description: Проверка параметров первой установки
author: dansimp
ms.assetid: e8a07d4c-5786-4455-ac43-2deac4042efd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859d627ec90fbc26d18019062d5e316f907cec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813024"
---
# <span data-ttu-id="13228-103">Проверка параметров первой установки</span><span class="sxs-lookup"><span data-stu-id="13228-103">How to Verify First Time Setup Settings</span></span>


<span data-ttu-id="13228-104">При первом запуске или после завершения установки вы можете проверить параметры, настроенные в рабочей области для MED-V, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="13228-104">While your test of first time setup is running or after it finishes, you can verify the settings that you configured in your MED-V workspace by performing the following tasks.</span></span>

<span data-ttu-id="13228-105">**Примечание**  Сведения о том, как отслеживать успешное выполнение первой настройки при первом запуске в рамках всего предприятия после развертывания, можно найти в разделе [наблюдение за развертыванием рабочих областей MED-V](monitoring-med-v-workspace-deployments.md).</span><span class="sxs-lookup"><span data-stu-id="13228-105">**Note** For information about how to monitor the successful completion of first time setup throughout your enterprise after deployment, see [Monitoring MED-V Workspace Deployments](monitoring-med-v-workspace-deployments.md).</span></span>

 

**<span data-ttu-id="13228-106">Проверка параметров при первом запуске программы установки</span><span class="sxs-lookup"><span data-stu-id="13228-106">To verify settings during first time setup</span></span>**

1.  <span data-ttu-id="13228-107">При первом запуске программы установки проверьте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="13228-107">While first time setup is running, verify the following:</span></span>

    <span data-ttu-id="13228-108">Если вы указали **Автоматический** режим, проверьте, отображается ли виртуальная машина при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="13228-108">If you specified **Unattended** mode, verify that the virtual machine does not appear when first time setup is running.</span></span>

    <span data-ttu-id="13228-109">Если вы указали режим "в режиме автоматической проверки", убедитесь, что виртуальная машина отображается и все поля, требующие ввода данных, отображаются.</span><span class="sxs-lookup"><span data-stu-id="13228-109">If you specified attended mode, verify that the virtual machine appears and that all fields that require user input are displayed.</span></span>

2.  <span data-ttu-id="13228-110">Вы также можете просмотреть полную настройку первого раза, просмотрев виртуальную машину при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="13228-110">You can also monitor the complete first time setup process by viewing the virtual machine when first time setup is running.</span></span> <span data-ttu-id="13228-111">Для этого выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="13228-111">To do this, follow these steps:</span></span>

    1.  <span data-ttu-id="13228-112">Откройте консоль Virtual PC для Windows.</span><span class="sxs-lookup"><span data-stu-id="13228-112">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="13228-113">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Windows Virtual PC**и **Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="13228-113">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="13228-114">Запустите MED-V, если он еще не запущен.</span><span class="sxs-lookup"><span data-stu-id="13228-114">Start MED-V if it is not already running.</span></span>

        <span data-ttu-id="13228-115">Если это еще не сделано, в списке виртуальных машин появится виртуальная машина с именем развернутой рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="13228-115">If not already present, in a short time, a virtual machine with the name of the deployed MED-V workspace appears in the list of virtual machines.</span></span>

    3.  <span data-ttu-id="13228-116">Дважды щелкните виртуальную машину MED-V, чтобы открыть ее.</span><span class="sxs-lookup"><span data-stu-id="13228-116">Double-click the MED-V virtual machine to open it.</span></span>

        <span data-ttu-id="13228-117">Вы можете наблюдать за виртуальной машиной MED-V при ее настройке, а также можете устранить неполадки, связанные с мини-установкой.</span><span class="sxs-lookup"><span data-stu-id="13228-117">You can observe the MED-V virtual machine when it is being set up, and you can troubleshoot the Mini-Setup procedure.</span></span> <span data-ttu-id="13228-118">Убедитесь, что информация на разных экранах пройдет, например, Настройка сетевых параметров, сведения о присоединении к домену компьютера, Настройка гостевого агента, Настройка личных параметров и завершение работы.</span><span class="sxs-lookup"><span data-stu-id="13228-118">Verify the information in the different screens as they go by, such as configuring networking settings, computer domain join information, configuring of the Guest Agent, set up of personal settings, and shutdown.</span></span>

    4.  <span data-ttu-id="13228-119">Виртуальная машина закрывается автоматически при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="13228-119">The virtual machine closes automatically when first time setup finishes.</span></span>

        <span data-ttu-id="13228-120">**Примечание**  Вы можете закрыть окно виртуальной машины в любое время и при первом запуске программы установки продолжить.</span><span class="sxs-lookup"><span data-stu-id="13228-120">**Note** You can close the virtual machine window at any time and first time setup continues.</span></span>

         

**<span data-ttu-id="13228-121">Проверка параметров после первого запуска программы установки</span><span class="sxs-lookup"><span data-stu-id="13228-121">To verify settings after first time setup finishes</span></span>**

1.  <span data-ttu-id="13228-122">Убедитесь, что в первый раз программа установки успешно завершила работу.</span><span class="sxs-lookup"><span data-stu-id="13228-122">Ensure that first time setup finished successfully.</span></span>

2.  <span data-ttu-id="13228-123">Убедитесь, что рабочее пространство MED-V настроено правильно.</span><span class="sxs-lookup"><span data-stu-id="13228-123">Verify that the MED-V workspace is set up correctly.</span></span>

    1.  <span data-ttu-id="13228-124">Откройте консоль Virtual PC для Windows.</span><span class="sxs-lookup"><span data-stu-id="13228-124">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="13228-125">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Windows Virtual PC**и **Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="13228-125">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="13228-126">Дважды щелкните установленную рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="13228-126">Double-click your installed MED-V workspace.</span></span>

        <span data-ttu-id="13228-127">Если Рабочая область MED-V уже работает с виртуальным приложением, вам может быть предложено закрыть приложение, прежде чем можно будет открыть виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="13228-127">If the MED-V workspace is already running a virtual application, you might be prompted to close the application before you can open the virtual machine.</span></span>

    3.  <span data-ttu-id="13228-128">В рабочей области MED-V щелкните правой кнопкой мыши **Мой компьютер**и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="13228-128">In the MED-V workspace, right-click **My Computer**, and then click **Properties**.</span></span>

    4.  <span data-ttu-id="13228-129">Убедитесь в том, что Рабочая область MED-V подключена к нужному домену.</span><span class="sxs-lookup"><span data-stu-id="13228-129">Verify that the MED-V workspace joined the correct domain.</span></span> <span data-ttu-id="13228-130">Если это применимо к вашей организации, протестируйте доменное соединение, указав два разных домена, чтобы убедиться в том, что гостевой домен переопределен доменом узла.</span><span class="sxs-lookup"><span data-stu-id="13228-130">If applicable to your organization, test domain joining by specifying two different domains to verify that the guest domain is overridden by the host domain.</span></span>

    5.  <span data-ttu-id="13228-131">Убедитесь, что Рабочая область MED-V входит в указанное организационное подразделение домена.</span><span class="sxs-lookup"><span data-stu-id="13228-131">Verify that the MED-V workspace joined the domain organizational unit that you specified.</span></span>

    6.  <span data-ttu-id="13228-132">Если вы указали маску имени компьютера, убедитесь, что новое имя компьютера соответствует указанному.</span><span class="sxs-lookup"><span data-stu-id="13228-132">If you specified the computer name mask, verify that the new computer name matches what was specified.</span></span>

3.  <span data-ttu-id="13228-133">Убедитесь, что параметры языковых стандартов заданы правильно.</span><span class="sxs-lookup"><span data-stu-id="13228-133">Verify that the locale settings that you specified are correct.</span></span>

    1.  <span data-ttu-id="13228-134">В рабочей области MED-V нажмите кнопку **Пуск** и выберите пункт **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="13228-134">In the MED-V workspace, click **Start** and then click **Control Panel**.</span></span>

    2.  <span data-ttu-id="13228-135">Проверьте указанные параметры конфигурации, например **дату и время** , а затем язык и **региональные стандарты**.</span><span class="sxs-lookup"><span data-stu-id="13228-135">Verify your specified configuration settings, for example, **Date and Time** and **Regional and Language**.</span></span>

<span data-ttu-id="13228-136">**Примечание**  Если вы столкнулись с проблемами при проверке параметров настройки в первый раз, ознакомьтесь с разделом [Устранение неполадок](operations-troubleshooting-medv2.md)с помощью операций.</span><span class="sxs-lookup"><span data-stu-id="13228-136">**Note** If you encounter any problems when verifying your first time setup settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

 

<span data-ttu-id="13228-137">Убедившись в том, что параметры настройки первоначально установлены правильно, вы можете протестировать другие конфигурации рабочей области MED-V, чтобы убедиться в том, что они работают должным образом, например опубликовать приложение и перенаправление URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="13228-137">After you have verified that your first time setup settings are correct, you can test other MED-V workspace configurations to verify that they function as intended, such as application publishing and URL redirection.</span></span>

<span data-ttu-id="13228-138">После того как вы завершите тестирование пакета MED-V Workspace и убедитесь, что он работает правильно, вы можете развернуть рабочую область MED-V в своей организации.</span><span class="sxs-lookup"><span data-stu-id="13228-138">After you have completed all testing of your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="13228-139">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="13228-139">Related topics</span></span>


[<span data-ttu-id="13228-140">Проверка публикации приложений</span><span class="sxs-lookup"><span data-stu-id="13228-140">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="13228-141">Проверка перенаправления URL-адресов</span><span class="sxs-lookup"><span data-stu-id="13228-141">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="13228-142">Развертывание пакета рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="13228-142">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

[<span data-ttu-id="13228-143">Управление параметрами рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="13228-143">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





