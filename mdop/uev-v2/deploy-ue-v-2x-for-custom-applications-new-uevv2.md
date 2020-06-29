---
title: Развертывание UE-V 2. x для настраиваемых приложений
description: Развертывание UE-V 2. x для настраиваемых приложений
author: dansimp
ms.assetid: f7cb089f-d764-4a93-82b6-926fe0385a23
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/19/2016
ms.openlocfilehash: 217f647d948df016c4a6b72736669c2b3305b705
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824402"
---
# <span data-ttu-id="7247f-103">Развертывание UE-V 2. x для настраиваемых приложений</span><span class="sxs-lookup"><span data-stu-id="7247f-103">Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="7247f-104">Microsoft User Experience Virtualization (UE-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="7247f-104">Microsoft User Experience Virtualization (UE-V) 2.0.</span></span> <span data-ttu-id="7247f-105">2,1 и 2,1 SP1 используют XML-файлы, которые называются **шаблонами расположения параметров** для отслеживания и синхронизации параметров классического приложения и рабочего стола Windows между компьютерами пользователя.</span><span class="sxs-lookup"><span data-stu-id="7247f-105">2.1, and 2.1 SP1 use XML files called **settings location templates** to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="7247f-106">По умолчанию в состав UE-V входит несколько шаблонов расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-106">By default, some settings location templates are included in UE-V.</span></span> <span data-ttu-id="7247f-107">Но если вы хотите синхронизировать параметры для классических приложений, отличных от тех, что используются в шаблонах по умолчанию, вы можете создать собственные шаблоны расположения пользовательских параметров с помощью генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="7247f-107">But if you want to synchronize settings for desktop applications other than those included in the default templates, you can create your own custom settings location templates by using the UE-V Generator.</span></span>

<span data-ttu-id="7247f-108">После того как вы прочитали материал по планированию для [подготовки к развертыванию UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md) и решили синхронизировать параметры для настраиваемых приложений (сторонние, строчные и т. д.), вы будете развертывать компоненты UE-V, как описано в этой статье.</span><span class="sxs-lookup"><span data-stu-id="7247f-108">Once you have read through the planning material in [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md) and have decided that you want to synchronize settings for custom applications (third-party, line-of-business, etc.), you will deploy the features of UE-V as described in this topic.</span></span> <span data-ttu-id="7247f-109">Ниже приведены основные действия, которые необходимо выполнить, чтобы синхронизировать параметры для настраиваемых приложений.</span><span class="sxs-lookup"><span data-stu-id="7247f-109">To start, here are the main steps required to synchronize settings for custom applications:</span></span>

-   [<span data-ttu-id="7247f-110">Установка генератора UEV</span><span class="sxs-lookup"><span data-stu-id="7247f-110">Install the UEV Generator</span></span>](#uevgen)

    <span data-ttu-id="7247f-111">Использование генератора UEV для создания настраиваемых шаблонов расположения параметров XML.</span><span class="sxs-lookup"><span data-stu-id="7247f-111">Use the UEV Generator to create custom XML settings location templates.</span></span>

-   [<span data-ttu-id="7247f-112">Настройка каталога шаблонов параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="7247f-112">Configure a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="7247f-113">Вы можете указать этот путь, где хранятся пользовательские шаблоны расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-113">You can define this path where custom settings location templates are stored.</span></span>

-   [<span data-ttu-id="7247f-114">Создание настраиваемых шаблонов расположений параметров</span><span class="sxs-lookup"><span data-stu-id="7247f-114">Create custom settings location templates</span></span>](#createcustomtemplates)

    <span data-ttu-id="7247f-115">Эти пользовательские шаблоны позволяют пользователям синхронизировать параметры пользовательских приложений.</span><span class="sxs-lookup"><span data-stu-id="7247f-115">These custom templates let users sync settings for custom applications.</span></span>

-   [<span data-ttu-id="7247f-116">Развертывание шаблонов расположений настраиваемых параметров</span><span class="sxs-lookup"><span data-stu-id="7247f-116">Deploy the custom settings location templates</span></span>](#deploycustomtemplates)

    <span data-ttu-id="7247f-117">После того как вы протестируете настраиваемый шаблон, чтобы убедиться, что параметры синхронизированы правильно, вы можете развернуть эти шаблоны одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="7247f-117">After you test the custom template to ensure that settings are synced correctly, you can deploy these templates in one of these ways:</span></span>

    -   <span data-ttu-id="7247f-118">С помощью существующей инфраструктуры развертывания, например Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7247f-118">Through your existing deployment infrastructure, such as Configuration Manager</span></span>

    -   <span data-ttu-id="7247f-119">С помощью настроек групповой политики</span><span class="sxs-lookup"><span data-stu-id="7247f-119">By using Group Policy preferences</span></span>

    -   [<span data-ttu-id="7247f-120">Развертывание каталога шаблонов параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="7247f-120">Deploy a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="7247f-121">**Примечание**  Шаблоны, развернутые с помощью ESD или групповой политики, должны быть зарегистрированы в Windows Management Instrumentation (WMI) или Windows PowerShell с UE-V.</span><span class="sxs-lookup"><span data-stu-id="7247f-121">**Note** Templates that are deployed by using ESD or Group Policy must be registered with UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span>

     

## <span data-ttu-id="7247f-122">Подготовка к развертыванию UE-V 2. x для настраиваемых приложений</span><span class="sxs-lookup"><span data-stu-id="7247f-122">Prepare to Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="7247f-123">Прежде чем приступить к развертыванию UE-V Features, обрабатывающего пользовательские приложения, вы можете просмотреть только несколько моментов.</span><span class="sxs-lookup"><span data-stu-id="7247f-123">Before you start deploying the UE-V features that handle custom applications, there are just a couple things to review.</span></span>

### <span data-ttu-id="7247f-124">Генератор UE-V</span><span class="sxs-lookup"><span data-stu-id="7247f-124">The UE-V Generator</span></span>

<span data-ttu-id="7247f-125">Генератор UE-V наблюдает за приложением для выяснения и захвата расположений, в которых приложение сохраняет параметры.</span><span class="sxs-lookup"><span data-stu-id="7247f-125">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="7247f-126">Отслеживаемое приложение должно быть традиционным приложением.</span><span class="sxs-lookup"><span data-stu-id="7247f-126">The application that is monitored must be a traditional application.</span></span> <span data-ttu-id="7247f-127">Вы используете UE-V Generator для создания шаблонов расположений параметров, но не может создать шаблон расположения параметров из этих типов приложений:</span><span class="sxs-lookup"><span data-stu-id="7247f-127">You use the UE-V Generator to create settings location templates, but it cannot create a settings location template from these application types:</span></span>

-   <span data-ttu-id="7247f-128">Виртуализированные приложения</span><span class="sxs-lookup"><span data-stu-id="7247f-128">Virtualized applications</span></span>

-   <span data-ttu-id="7247f-129">Приложения, которые предлагаются в службах терминалов</span><span class="sxs-lookup"><span data-stu-id="7247f-129">Applications that are offered through Terminal Services</span></span>

-   <span data-ttu-id="7247f-130">Приложения Java</span><span class="sxs-lookup"><span data-stu-id="7247f-130">Java applications</span></span>

-   <span data-ttu-id="7247f-131">Приложения для Windows  </span><span class="sxs-lookup"><span data-stu-id="7247f-131">Windows apps</span></span>

<span data-ttu-id="7247f-132">**Примечание**  Шаблоны расположений параметров UE-V нельзя создавать из виртуализированных приложений и приложений служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="7247f-132">**Note** UE-V settings location templates cannot be created from virtualized applications or Terminal Services applications.</span></span> <span data-ttu-id="7247f-133">Однако параметры, синхронизированные с помощью шаблонов, можно применять к этим приложениям.</span><span class="sxs-lookup"><span data-stu-id="7247f-133">However, settings that are synchronized by using the templates can be applied to those applications.</span></span> <span data-ttu-id="7247f-134">Для создания шаблонов, поддерживающих инфраструктуру виртуальных рабочих столов (VDI) и приложений служб терминалов, откройте версию пакета установщика Windows (MSI) для приложения с помощью генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="7247f-134">To create templates that support Virtual Desktop Infrastructure (VDI) and Terminal Services applications, open a version of the Windows Installer (.msi) package of the application by using the UE-V Generator.</span></span> <span data-ttu-id="7247f-135">Дополнительные сведения о синхронизации параметров для виртуальных приложений можно найти в разделе [использование UE-V 2. x с приложениями Application Virtualization](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="7247f-135">For more information about synchronizing settings for virtual applications, see [Using UE-V 2.x with Application Virtualization Applications](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).</span></span>

 

<span data-ttu-id="7247f-136">**Исключенные расположения:** В процессе обнаружения не учитываются места, в которых обычно хранятся файлы программного обеспечения приложения, которые не синхронизируют параметры между компьютерами пользователя или средой.</span><span class="sxs-lookup"><span data-stu-id="7247f-136">**Excluded Locations:** The discovery process excludes locations that commonly store application software files that do not synchronize settings well between user computers or computing environments.</span></span> <span data-ttu-id="7247f-137">По умолчанию эти параметры исключены.</span><span class="sxs-lookup"><span data-stu-id="7247f-137">By default, these are excluded:</span></span>

-   <span data-ttu-id="7247f-138">Раздел HKEY \ _CURRENT \ _USER разделы реестра и файлы, к которым пользователь, выполнивший вход, не может записать значения</span><span class="sxs-lookup"><span data-stu-id="7247f-138">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="7247f-139">Раздел HKEY \ _CURRENT \ _USER разделы реестра и файлы, связанные с основными функциями операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="7247f-139">HKEY\_CURRENT\_USER registry keys and files that are associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="7247f-140">Все разделы реестра, которые находятся в кусте HKEY \ _LOCAL \ _MACHINE</span><span class="sxs-lookup"><span data-stu-id="7247f-140">All registry keys that are located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="7247f-141">Файлы, расположенные в каталогах программных файлов</span><span class="sxs-lookup"><span data-stu-id="7247f-141">Files that are located in Program Files directories</span></span>

-   <span data-ttu-id="7247f-142">Файлы, расположенные в списке Пользователи \ \ \ [имя пользователя \] \ \ AppData \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="7247f-142">Files that are located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="7247f-143">Файлы операционной системы Windows, расположенные в папке% systemroot%</span><span class="sxs-lookup"><span data-stu-id="7247f-143">Windows operating system files that are located in %Systemroot%</span></span>

<span data-ttu-id="7247f-144">Если для синхронизации параметров приложения требуются разделы реестра и файлы, которые хранятся в исключенных расположениях, вы можете вручную добавить их в шаблон расположения параметров в процессе создания шаблона.</span><span class="sxs-lookup"><span data-stu-id="7247f-144">If registry keys and files that are stored in excluded locations are required to synchronize application settings, you can manually add the locations to the settings location template during the template creation process.</span></span>
<span data-ttu-id="7247f-145">Однако только изменения куста HKEY \ _CURRENT \ _USER будут синхронизироваться (ED).</span><span class="sxs-lookup"><span data-stu-id="7247f-145">However, only changes to the HKEY\_CURRENT\_USER hive will be sync-ed.</span></span>

### <span data-ttu-id="7247f-146">Замена шаблонов Microsoft по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7247f-146">Replace the default Microsoft templates</span></span>

<span data-ttu-id="7247f-147">Агент UE-V добавляет стандартную группу шаблонов расположения параметров для распространенных приложений Майкрософт и параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="7247f-147">The UE-V Agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="7247f-148">Если вы настраиваете эти шаблоны или создаете шаблоны расположений параметров для синхронизации параметров для настраиваемых приложений, агент UE-V Agent можно настроить на использование каталога шаблонов параметров для хранения шаблонов.</span><span class="sxs-lookup"><span data-stu-id="7247f-148">If you customize these templates, or create settings location templates to synchronize settings for custom applications, the UE-V Agent can be configured to use a settings template catalog to store the templates.</span></span> <span data-ttu-id="7247f-149">В этом случае вам потребуется включить шаблоны по умолчанию вместе с пользовательскими шаблонами в каталоге шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-149">In this case, you will need to include the default templates along with the custom templates in the settings template catalog.</span></span>

<span data-ttu-id="7247f-150">При [развертывании агента UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent)вы можете использовать параметр командной строки, `RegisterMSTemplates` чтобы отключить регистрацию шаблонов Microsoft по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7247f-150">When you [Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent), you can use the command-line parameter `RegisterMSTemplates` to disable the registration of the default Microsoft templates.</span></span>

<span data-ttu-id="7247f-151">Если вы используете групповую политику для настройки пути к каталогу шаблонов параметров, вы можете заменить стандартные шаблоны Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7247f-151">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="7247f-152">Если вы настроили параметры политики для замены шаблонов Майкрософт по умолчанию, удаляются все шаблоны Microsoft, установленные по умолчанию агентом UE-V, и используются только шаблоны, которые находятся в каталоге шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-152">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V Agent are deleted and only the templates that are located in the settings template catalog are used.</span></span> <span data-ttu-id="7247f-153">Параметр конфигурации агента UE-V `RegisterMSTemplates` должен иметь значение *true* , чтобы переопределить шаблон Microsoft по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7247f-153">The UE-V Agent configuration setting parameter `RegisterMSTemplates` must be set to *true* in order to override the default Microsoft template.</span></span>

<span data-ttu-id="7247f-154">**Примечание**  Если отключить этот параметр политики после включения, агент UE-V Agent не восстановит шаблоны Microsoft по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7247f-154">**Note** If you disable this policy setting after it has been enabled, the UE-V Agent does not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="7247f-155">Если в каталоге шаблонов параметров есть настроенные шаблоны, которые используют тот же идентификатор, что и в шаблонах Microsoft по умолчанию, а агент UE-V не настроен для замены шаблонов Microsoft по умолчанию, шаблоны Microsoft будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="7247f-155">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V Agent is not configured to replace the default Microsoft templates, the Microsoft templates are ignored.</span></span>

<span data-ttu-id="7247f-156">Вы также можете заменить шаблоны по умолчанию с помощью UE-V Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7247f-156">You can also replace the default templates by using the UE-V Windows PowerShell features.</span></span> <span data-ttu-id="7247f-157">Чтобы заменить шаблон Microsoft по умолчанию с помощью Windows PowerShell, отмените регистрацию всех шаблонов Microsoft по умолчанию, а затем зарегистрируйте пользовательские шаблоны.</span><span class="sxs-lookup"><span data-stu-id="7247f-157">To replace the default Microsoft template with Windows PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="7247f-158">**Примечание**  Старые пакеты параметров остаются в местоположении хранения параметров, даже если вы развертываете новые шаблоны расположений параметров для приложения.</span><span class="sxs-lookup"><span data-stu-id="7247f-158">**Note** Old settings packages remain in the settings storage location even if you deploy new settings location templates for an application.</span></span> <span data-ttu-id="7247f-159">Эти пакеты не прочтены агентом, но ни один из них не удаляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="7247f-159">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <a href="" id="uevgen"></a><span data-ttu-id="7247f-160">Установка генератора UEV 2. x</span><span class="sxs-lookup"><span data-stu-id="7247f-160">Install the UEV 2.x Generator</span></span>


<span data-ttu-id="7247f-161">На компьютере, на котором можно создать настраиваемый шаблон расположения параметров, установите для него генератор 2,0 Microsoft Experience Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="7247f-161">Install the Microsoft User Experience Virtualization (UE-V) 2.0 Generator on a computer that you can then use to create a custom settings location template.</span></span> <span data-ttu-id="7247f-162">На этом компьютере должны быть установлены приложения, для которых нужно создать шаблоны расположений с пользовательскими параметрами.</span><span class="sxs-lookup"><span data-stu-id="7247f-162">This computer should have the applications installed for which custom settings location templates are to be generated.</span></span>

**<span data-ttu-id="7247f-163">Установка генератора UE-V</span><span class="sxs-lookup"><span data-stu-id="7247f-163">To install the UE-V Generator</span></span>**

1.  <span data-ttu-id="7247f-164">Как пользователь с правами локального администратора найдите установочный файл генератора UE-V **ToolSetup.exe** , поставляемый с программным обеспечением UE-v.</span><span class="sxs-lookup"><span data-stu-id="7247f-164">As a user with local administrator rights, locate the UE-V Generator installation file **ToolSetup.exe** provided with the UE-V software.</span></span> <span data-ttu-id="7247f-165">Кроме того, если известна архитектура компьютера, вы можете запустить соответствующий файл установщика Windows (MSI), **ToolsSetupx64.msi** или **ToolsSetupx86.msi**.</span><span class="sxs-lookup"><span data-stu-id="7247f-165">Or, if you know the computer architecture, you can run the appropriate Windows Installer (.msi) file, **ToolsSetupx64.msi** or **ToolsSetupx86.msi**.</span></span>

2.  <span data-ttu-id="7247f-166">Дважды щелкните файл установки.</span><span class="sxs-lookup"><span data-stu-id="7247f-166">Double-click the installation file.</span></span> <span data-ttu-id="7247f-167">Откроется мастер настройки генератора виртуализации взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="7247f-167">The User Experience Virtualization Generator Setup wizard opens.</span></span> <span data-ttu-id="7247f-168">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7247f-168">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="7247f-169">Приняв условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7247f-169">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="7247f-170">Выберите параметры обновлений Майкрософт и программы улучшения качества программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="7247f-170">Click the options for Microsoft Updates and the Customer Experience Improvement Program.</span></span>

5.  <span data-ttu-id="7247f-171">Выберите конечную папку, в которую нужно установить генератор UE-V, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7247f-171">Select the destination folder in which to install the UE-V Generator, and then click **Next**.</span></span>

6.  <span data-ttu-id="7247f-172">Нажмите кнопку " **установить** ", чтобы начать установку.</span><span class="sxs-lookup"><span data-stu-id="7247f-172">Click **Install** to begin the installation.</span></span>

    <span data-ttu-id="7247f-173">**Примечание**  Перед установкой приложения появится запрос на **контроль учетной записи пользователя** .</span><span class="sxs-lookup"><span data-stu-id="7247f-173">**Note** A prompt for **User Account Control** appears before the application is installed.</span></span> <span data-ttu-id="7247f-174">Требуется разрешение на установку UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="7247f-174">Permission is required to install the UE-V Generator.</span></span>

     

7.  <span data-ttu-id="7247f-175">Нажмите кнопку **Готово** , чтобы закрыть окно мастера после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="7247f-175">Click **Finish** to close the wizard after the installation is finished.</span></span> <span data-ttu-id="7247f-176">Для запуска UE-V Generator необходимо перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="7247f-176">You must restart your computer before you can run the UE-V Generator.</span></span>

    <span data-ttu-id="7247f-177">Чтобы убедиться, что установка прошла успешно, нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft User Experience Virtualization**и выберите **генератор виртуализации взаимодействия с пользователем Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="7247f-177">To verify that the installation was successful, click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

    <span data-ttu-id="7247f-178">**Примечание**  Генератор UE-V 2 можно использовать только для создания шаблонов для агентов UE-V 2.</span><span class="sxs-lookup"><span data-stu-id="7247f-178">**Note** The UE-V 2 Generator can only be used to create templates for UE-V 2 Agents.</span></span> <span data-ttu-id="7247f-179">В смешанном развертывании агентов UE-V 1,0 и UE-V 2 вы должны продолжать использовать генератор UE-V 1,0, пока не обновите все агенты UE-V.</span><span class="sxs-lookup"><span data-stu-id="7247f-179">In a mixed deployment of UE-V 1.0 Agents and UE-V 2 Agents, you should continue to use the UE-V 1.0 Generator until you have upgraded all UE-V Agents.</span></span>

     

## <a href="" id="deploycatalogue"></a><span data-ttu-id="7247f-180">Развертывание каталога шаблонов параметров</span><span class="sxs-lookup"><span data-stu-id="7247f-180">Deploy a Settings Template Catalog</span></span>


<span data-ttu-id="7247f-181">Каталог шаблонов параметров виртуализации пользователей — это путь к папке на компьютерах UE-V или сетевая папка SMB, в которой хранятся все пользовательские шаблоны расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-181">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="7247f-182">Запланированная задача в агенте UE-V проверяет это расположение один раз в день и обновляет параметры синхронизации в соответствии с шаблонами в этой папке.</span><span class="sxs-lookup"><span data-stu-id="7247f-182">A scheduled task in the UE-V Agent checks this location one time each day and updates its synchronization behavior, based on the templates in this folder.</span></span>

<span data-ttu-id="7247f-183">Агент UE-V регистрирует шаблоны, добавленные или обновленные в этой папке после последнего установления и отмены регистрации шаблонов.</span><span class="sxs-lookup"><span data-stu-id="7247f-183">The UE-V Agent registers templates that were added or updated in this folder after the last time that the folder was checked and unregisters templates that are removed.</span></span> <span data-ttu-id="7247f-184">По умолчанию шаблоны регистрируются и отменяются один раз в день в 3:30 утра.</span><span class="sxs-lookup"><span data-stu-id="7247f-184">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="7247f-185">Локальное время планировщиком задач и при запуске системы.</span><span class="sxs-lookup"><span data-stu-id="7247f-185">local time by the Task Scheduler and at system startup.</span></span> <span data-ttu-id="7247f-186">Чтобы настроить частоту выполнения запланированной задачи, ознакомьтесь [со сведениями об изменении частоты запланированных задач UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="7247f-186">To customize the frequency of this scheduled task, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="7247f-187">Путь к каталогу шаблонов параметров можно настроить с помощью параметров командной строки для установки, групповой политики, WMI или Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7247f-187">You can configure the settings template catalog path by using the installation command-line options, Group Policy, WMI, or Windows PowerShell.</span></span> <span data-ttu-id="7247f-188">Шаблоны, которые хранятся в пути к каталогу шаблонов, автоматически регистрируются и отменяются с помощью запланированной задачи.</span><span class="sxs-lookup"><span data-stu-id="7247f-188">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span>

**<span data-ttu-id="7247f-189">Настройка каталога шаблонов параметров для UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7247f-189">To configure the settings template catalog for UE-V 2.x</span></span>**

1.  <span data-ttu-id="7247f-190">Создайте новую папку на компьютере, в которой хранится каталог шаблонов параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="7247f-190">Create a new folder on the computer that stores the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="7247f-191">Установите следующие разрешения на уровне общего доступа (SMB) для папки каталога шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-191">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="7247f-192">Учетная запись пользователя</span><span class="sxs-lookup"><span data-stu-id="7247f-192">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="7247f-193">Рекомендуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="7247f-193">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7247f-194">Все пользователи</span><span class="sxs-lookup"><span data-stu-id="7247f-194">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7247f-195">Нет разрешений</span><span class="sxs-lookup"><span data-stu-id="7247f-195">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7247f-196">Компьютеры домена</span><span class="sxs-lookup"><span data-stu-id="7247f-196">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7247f-197">Уровни разрешений "чтение"</span><span class="sxs-lookup"><span data-stu-id="7247f-197">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7247f-198">Администраторы</span><span class="sxs-lookup"><span data-stu-id="7247f-198">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7247f-199">Уровни разрешений на чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7247f-199">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="7247f-200">Установите следующие разрешения файловой системы NTFS для папки каталога шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-200">Set the following NTFS file system permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7247f-201">Учетная запись пользователя</span><span class="sxs-lookup"><span data-stu-id="7247f-201">User account</span></span></th>
    <th align="left"><span data-ttu-id="7247f-202">Рекомендуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="7247f-202">Recommended permissions</span></span></th>
    <th align="left"><span data-ttu-id="7247f-203">Применить к</span><span class="sxs-lookup"><span data-stu-id="7247f-203">Apply to</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7247f-204">Создатель/владелец</span><span class="sxs-lookup"><span data-stu-id="7247f-204">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7247f-205">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="7247f-205">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7247f-206">Эта папка, вложенные папки и файлы</span><span class="sxs-lookup"><span data-stu-id="7247f-206">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7247f-207">Компьютеры домена</span><span class="sxs-lookup"><span data-stu-id="7247f-207">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7247f-208">Просмотр содержимого папки и чтение</span><span class="sxs-lookup"><span data-stu-id="7247f-208">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7247f-209">Эта папка, вложенные папки и файлы</span><span class="sxs-lookup"><span data-stu-id="7247f-209">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7247f-210">Все пользователи</span><span class="sxs-lookup"><span data-stu-id="7247f-210">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7247f-211">Нет разрешений</span><span class="sxs-lookup"><span data-stu-id="7247f-211">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7247f-212">Нет разрешений</span><span class="sxs-lookup"><span data-stu-id="7247f-212">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7247f-213">Администраторы</span><span class="sxs-lookup"><span data-stu-id="7247f-213">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7247f-214">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="7247f-214">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7247f-215">Эта папка, вложенные папки и файлы</span><span class="sxs-lookup"><span data-stu-id="7247f-215">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="7247f-216">Нажмите кнопку **ОК** , чтобы закрыть диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="7247f-216">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="7247f-217">Как минимум, в сетевом общем доступе должны быть предоставлены разрешения для группы Domain Computers.</span><span class="sxs-lookup"><span data-stu-id="7247f-217">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="7247f-218">Кроме того, предоставьте разрешения на доступ к папке "сетевая папка" для администраторов, которые могут управлять сохраненными шаблонами.</span><span class="sxs-lookup"><span data-stu-id="7247f-218">In addition, grant access permissions for the network share folder to administrators who are to manage the stored templates.</span></span>

## <a href="" id="createcustomtemplates"></a><span data-ttu-id="7247f-219">Создание настраиваемых шаблонов расположений параметров</span><span class="sxs-lookup"><span data-stu-id="7247f-219">Create Custom Settings Location Templates</span></span>


<span data-ttu-id="7247f-220">Использование генератора UE-V для создания шаблонов расположений параметров для бизнес-приложений или других настраиваемых приложений.</span><span class="sxs-lookup"><span data-stu-id="7247f-220">Use the UE-V Generator to create settings location templates for line-of-business applications or other custom applications.</span></span> <span data-ttu-id="7247f-221">После создания шаблона для приложения его можно развернуть на компьютерах, чтобы синхронизировать параметры для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="7247f-221">After the template for an application is created, you can deploy it to computers so that settings are synchronized for that application.</span></span>

**<span data-ttu-id="7247f-222">Создание шаблона расположения параметров UE-V с помощью UE-V Generator</span><span class="sxs-lookup"><span data-stu-id="7247f-222">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="7247f-223">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft User Experience Virtualization**и выберите **генератор Microsoft Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="7247f-223">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="7247f-224">Нажмите кнопку **создать шаблон расположения параметров**.</span><span class="sxs-lookup"><span data-stu-id="7247f-224">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="7247f-225">Укажите приложение.</span><span class="sxs-lookup"><span data-stu-id="7247f-225">Specify the application.</span></span> <span data-ttu-id="7247f-226">Перейдите к файлу приложения (exe) или ярлыку приложения (. lnk), для которого вы хотите создать шаблон расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-226">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="7247f-227">Укажите аргументы командной строки, если таковые имеются, и рабочий каталог, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="7247f-227">Specify the command-line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="7247f-228">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7247f-228">Click **Next** to continue.</span></span>

    <span data-ttu-id="7247f-229">**Примечание**  Перед запуском приложения система отображает запрос на **контроль учетной записи пользователя**.</span><span class="sxs-lookup"><span data-stu-id="7247f-229">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="7247f-230">Для мониторинга параметров реестра и файлов, используемых приложением, требуется разрешение на их хранение.</span><span class="sxs-lookup"><span data-stu-id="7247f-230">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="7247f-231">После запуска приложения закройте приложение.</span><span class="sxs-lookup"><span data-stu-id="7247f-231">After the application starts, close the application.</span></span> <span data-ttu-id="7247f-232">Генератор UE-V записывает места, в которых приложение хранит параметры.</span><span class="sxs-lookup"><span data-stu-id="7247f-232">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="7247f-233">После завершения процесса нажмите кнопку **Далее** , чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="7247f-233">After the process is completed, click **Next** to continue.</span></span>

6.  <span data-ttu-id="7247f-234">Просмотрите и установите флажки рядом с соответствующими параметрами реестра и расположениями файлов параметров для синхронизации с этим приложением.</span><span class="sxs-lookup"><span data-stu-id="7247f-234">Review and select the check boxes that are next to the appropriate registry settings locations and settings file locations to synchronize for this application.</span></span> <span data-ttu-id="7247f-235">Список содержит две следующие категории для расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-235">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="7247f-236">**Стандартные**: параметры приложения, хранящиеся в реестре в разделах hKey \ _CURRENT \ _USER или в папках с файлами в разделе \ \ **Пользователи** \ \ \ [имя пользователя \] \ \ **AppData**  \\  **роуминг**.</span><span class="sxs-lookup"><span data-stu-id="7247f-236">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="7247f-237">Генератор UE-V включает эти параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7247f-237">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="7247f-238">**Нестандартные**: параметры приложения, которые хранятся за пределами расположений, указаны в разделе Советы и рекомендации по хранению данных параметров (необязательно).</span><span class="sxs-lookup"><span data-stu-id="7247f-238">**Nonstandard**: Application settings that are stored outside the locations are specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="7247f-239">Сюда входят файлы и папки в разделе **Пользователи** \ \ \ [имя пользователя \] \ \ **AppData**  \\  **Local**.</span><span class="sxs-lookup"><span data-stu-id="7247f-239">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="7247f-240">Проверьте эти расположения, чтобы определить, нужно ли включать их в шаблон расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-240">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="7247f-241">Установите флажки расположения, чтобы включить их.</span><span class="sxs-lookup"><span data-stu-id="7247f-241">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="7247f-242">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7247f-242">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="7247f-243">Просмотр и изменение **свойств**, расположений в **реестре** и расположений **файлов** для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-243">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="7247f-244">Измените следующие свойства на вкладке **Свойства** :</span><span class="sxs-lookup"><span data-stu-id="7247f-244">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="7247f-245">**Имя приложения**: имя приложения, которое написано в описании свойств файлов программы.</span><span class="sxs-lookup"><span data-stu-id="7247f-245">**Application Name**: The application name that is written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="7247f-246">**Имя программы**: имя программы, которая берется из свойств файла программы.</span><span class="sxs-lookup"><span data-stu-id="7247f-246">**Program name**: The name of the program that is taken from the program file properties.</span></span> <span data-ttu-id="7247f-247">Обычно это имя имеет расширение имени файла. exe.</span><span class="sxs-lookup"><span data-stu-id="7247f-247">This name usually has the .exe file name extension.</span></span>

        -   <span data-ttu-id="7247f-248">**Версия продукта**: номер версии файла exe приложения.</span><span class="sxs-lookup"><span data-stu-id="7247f-248">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="7247f-249">Это свойство в сочетании с **версией файла**помогает определить, какие приложения предназначены для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-249">This property, in conjunction with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="7247f-250">Это свойство принимает основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="7247f-250">This property accepts a major version number.</span></span> <span data-ttu-id="7247f-251">Если это свойство не задано, шаблон расположения параметров применяется ко всем версиям продукта.</span><span class="sxs-lookup"><span data-stu-id="7247f-251">If this property is empty, the settings location template applies to all versions of the product.</span></span>

        -   <span data-ttu-id="7247f-252">**Версия файла**: номер версии файла exe приложения.</span><span class="sxs-lookup"><span data-stu-id="7247f-252">**File version**: The file version number of the .exe file of the application.</span></span> <span data-ttu-id="7247f-253">Это свойство в сочетании с **версией продукта**помогает определить, какие приложения предназначены для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-253">This property, in conjunction with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="7247f-254">Это свойство принимает основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="7247f-254">This property accepts a major version number.</span></span> <span data-ttu-id="7247f-255">Если это свойство не задано, шаблон расположения параметров применяется ко всем версиям программы.</span><span class="sxs-lookup"><span data-stu-id="7247f-255">If this property is empty, the settings location template applies to all versions of the program.</span></span>

        -   <span data-ttu-id="7247f-256">**Имя автора шаблона** (необязательно): имя автора шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-256">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="7247f-257">**Электронная почта автора шаблона** (необязательно): адрес электронной почты автора шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-257">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="7247f-258">На вкладке " **Реестр** " перечислены разделы **реестра и их** **область** , которые включены в шаблон расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-258">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="7247f-259">Измените расположение реестра с помощью раскрывающегося меню **Tasks (задачи** ).</span><span class="sxs-lookup"><span data-stu-id="7247f-259">Edit the registry locations by using the **Tasks** drop-down menu.</span></span> <span data-ttu-id="7247f-260">С помощью задач вы можете добавлять новые ключи, изменять имена или области существующих клавиш, удалять разделы и просматривать реестр, в котором находятся ключи.</span><span class="sxs-lookup"><span data-stu-id="7247f-260">Tasks enable you to add new keys, edit the name or scope of existing keys, delete keys, and browse the registry where the keys are located.</span></span> <span data-ttu-id="7247f-261">Используйте область " **все параметры** ", чтобы включить все параметры реестра в указанном разделе.</span><span class="sxs-lookup"><span data-stu-id="7247f-261">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="7247f-262">Используйте **все параметры и подразделы** для включения всех параметров реестра в заданные раздел, подразделы и параметры подраздела.</span><span class="sxs-lookup"><span data-stu-id="7247f-262">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="7247f-263">На вкладке " **файлы** " перечислены путь к файлу и его маска для расположения файлов, которые включены в шаблон расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-263">The **Files** tab lists the file path and file mask of the file locations that are included in the settings location template.</span></span> <span data-ttu-id="7247f-264">Измените расположение файлов с помощью раскрывающегося меню **Tasks (задачи** ).</span><span class="sxs-lookup"><span data-stu-id="7247f-264">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="7247f-265">Задачи для расположений файлов позволяют добавлять новые файлы или папки, изменять область существующих файлов и папок, удалять файлы и папки, а также открывать выбранное расположение в проводнике.</span><span class="sxs-lookup"><span data-stu-id="7247f-265">Tasks for file locations enable you to add new files or folder locations, edit the scope of existing files or folders, delete files or folders, and open the selected location in Windows Explorer.</span></span> <span data-ttu-id="7247f-266">Чтобы включить все файлы в указанную папку, оставьте пустую маску файла.</span><span class="sxs-lookup"><span data-stu-id="7247f-266">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="7247f-267">Нажмите кнопку **создать**и выберите команду **сохранить** , чтобы сохранить шаблон расположения параметров на компьютере.</span><span class="sxs-lookup"><span data-stu-id="7247f-267">Click **Create**, and then click **Save** to save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="7247f-268">Нажмите кнопку **Закрыть** , чтобы закрыть окно мастера шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-268">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="7247f-269">Выйдите из приложения генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="7247f-269">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="7247f-270">После создания шаблона расположения параметров для приложения необходимо протестировать этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="7247f-270">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="7247f-271">Разверните шаблон в лабораторной среде перед тем, как перевести его в производственную среду на предприятии.</span><span class="sxs-lookup"><span data-stu-id="7247f-271">Deploy the template in a lab environment before you put it into production in the enterprise.</span></span>

<span data-ttu-id="7247f-272">[Справочник по схемам шаблонов приложений для UE-v —](https://technet.microsoft.com/library/dn763947.aspx) структура XML для шаблона расположения параметров ue-v и руководство по редактированию этих файлов.</span><span class="sxs-lookup"><span data-stu-id="7247f-272">[Application Template Schema Reference for UE-V](https://technet.microsoft.com/library/dn763947.aspx) details the XML structure of the UE-V settings location template and provides guidance for editing these files.</span></span>

## <a href="" id="deploycustomtemplates"></a><span data-ttu-id="7247f-273">Развертывание шаблонов расположений настраиваемых параметров</span><span class="sxs-lookup"><span data-stu-id="7247f-273">Deploy the Custom Settings Location Templates</span></span>


<span data-ttu-id="7247f-274">После создания шаблона расположения параметров с помощью генератора UE-V необходимо проверить его, чтобы убедиться, что параметры приложения синхронизированы правильно.</span><span class="sxs-lookup"><span data-stu-id="7247f-274">After you create a settings location template with the UE-V Generator, you should test it to ensure that the application settings are synchronized correctly.</span></span> <span data-ttu-id="7247f-275">Затем вы можете безопасно развернуть шаблон расположения параметров на компьютерах в предприятии.</span><span class="sxs-lookup"><span data-stu-id="7247f-275">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="7247f-276">Шаблоны расположений параметров можно развернуть с помощью одного из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="7247f-276">Settings location templates can be deployed by using one of these methods:</span></span>

-   <span data-ttu-id="7247f-277">Система распространения корпоративного программного обеспечения (ESD), например System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7247f-277">An enterprise software distribution (ESD) system such as System Center Configuration Manager</span></span>

-   <span data-ttu-id="7247f-278">Предпочтения групповой политики</span><span class="sxs-lookup"><span data-stu-id="7247f-278">Group Policy preferences</span></span>

-   <span data-ttu-id="7247f-279">Каталог шаблонов параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="7247f-279">A UE-V settings template catalog</span></span>

<span data-ttu-id="7247f-280">Шаблоны, развернутые с использованием системы ESD или объектов групповой политики, должны быть зарегистрированы с помощью Windows Management Instrumentation (WMI) или PowerShell для UE-V.</span><span class="sxs-lookup"><span data-stu-id="7247f-280">Templates that are deployed by using an ESD system or Group Policy Objects must be registered through UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span> <span data-ttu-id="7247f-281">Шаблоны, которые хранятся в расположении каталога шаблонов параметров, автоматически регистрируются агентом UE-V.</span><span class="sxs-lookup"><span data-stu-id="7247f-281">Templates that are stored in the settings template catalog location are automatically registered by the UE-V Agent.</span></span>

**<span data-ttu-id="7247f-282">Использование пути к каталогу шаблонов параметров для развертывания шаблонов расположений параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="7247f-282">To use the settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="7247f-283">Перейдите к папке "сетевая папка", которая определена как каталог шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-283">Browse to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="7247f-284">Добавьте, удалите или обновите шаблоны расположений параметров в каталоге шаблонов параметров в соответствии с конфигурацией шаблона агента UE-V, которую вы хотите использовать для компьютеров UE-V.</span><span class="sxs-lookup"><span data-stu-id="7247f-284">Add, remove, or update settings location templates in the settings template catalog to reflect the UE-V Agent template configuration that you want for UE-V computers.</span></span>

    <span data-ttu-id="7247f-285">**Примечание**  Шаблоны на компьютерах обновляются ежедневно.</span><span class="sxs-lookup"><span data-stu-id="7247f-285">**Note** Templates on computers are updated daily.</span></span> <span data-ttu-id="7247f-286">Обновление основано на изменениях в каталоге шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="7247f-286">The update is based on changes to the settings template catalog.</span></span>

     

3.  <span data-ttu-id="7247f-287">Чтобы вручную обновить шаблоны на компьютере, на котором запущен агент UE-V, откройте командную команду с повышенными привилегиями и перейдите в \*\*% Program Files%\\Microsoft User Experience Virtualization \ \ &lt; x86 или x64 &gt; \*\*и запустите **ApplySettingsTemplateCatalog.exe**.</span><span class="sxs-lookup"><span data-stu-id="7247f-287">To manually update templates on a computer that runs the UE-V Agent, open an elevated command prompt, and browse to **%Program Files%\\Microsoft User Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe**.</span></span>

    <span data-ttu-id="7247f-288">**Примечание**  Эта программа запускается автоматически во время запуска компьютера и ежедневно в 3:30 A. M.</span><span class="sxs-lookup"><span data-stu-id="7247f-288">**Note** This program runs automatically during computer startup and daily at 3:30 A. M.</span></span> <span data-ttu-id="7247f-289">для сбора новых шаблонов, которые были недавно добавлены в каталог.</span><span class="sxs-lookup"><span data-stu-id="7247f-289">to gather any new templates that were recently added to the catalog.</span></span>

     






## <span data-ttu-id="7247f-290">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7247f-290">Related topics</span></span>


[<span data-ttu-id="7247f-291">Подготовка к развертыванию UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7247f-291">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="7247f-292">Развертывание необходимых компонентов для UE-v 2.x</span><span class="sxs-lookup"><span data-stu-id="7247f-292">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

 

 





