---
title: Настройка UE-V 2. x с помощью System Center Configuration Manager 2012
description: Настройка UE-V 2. x с помощью System Center Configuration Manager 2012
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824409"
---
# <span data-ttu-id="447ae-103">Настройка UE-V 2. x с помощью System Center Configuration Manager 2012</span><span class="sxs-lookup"><span data-stu-id="447ae-103">Configuring UE-V 2.x with System Center Configuration Manager 2012</span></span>


<span data-ttu-id="447ae-104">После установки Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 или 2,1 SP1 и их обязательных функций необходимо настроить UE-V.</span><span class="sxs-lookup"><span data-stu-id="447ae-104">After you install Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 and their required features, UE-V must be configured.</span></span> <span data-ttu-id="447ae-105">Пакет конфигурации UE-V позволяет администраторам использовать параметры соответствия требованиям компонента System Center Configuration Manager 2012 или более поздней версии для применения согласованных конфигураций на сайтах, где установлены UE-V и Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="447ae-105">The UE-V Configuration Pack provides a way for administrators to use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

## <span data-ttu-id="447ae-106">Поддерживаемые функции пакета конфигурации UE-V</span><span class="sxs-lookup"><span data-stu-id="447ae-106">UE-V Configuration Pack supported features</span></span>


<span data-ttu-id="447ae-107">Пакет конфигурации UE-V содержит инструменты для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="447ae-107">The UE-V Configuration Pack includes tools to perform the following tasks:</span></span>

-   <span data-ttu-id="447ae-108">Создание или обновление шаблонов расположений параметров для UE-V.</span><span class="sxs-lookup"><span data-stu-id="447ae-108">Create or update UE-V settings location template distribution baselines.</span></span>

    -   <span data-ttu-id="447ae-109">Определение шаблонов UE-V для регистрации и отмены регистрации</span><span class="sxs-lookup"><span data-stu-id="447ae-109">Define UE-V templates to be registered or unregistered</span></span>

    -   <span data-ttu-id="447ae-110">Обновление элементов конфигурации шаблонов UE-V и базовых планов по мере добавления или обновления шаблонов</span><span class="sxs-lookup"><span data-stu-id="447ae-110">Update UE-V template configuration items and baselines as templates are added or updated</span></span>

    -   <span data-ttu-id="447ae-111">Распространение и регистрация шаблонов UE-V с помощью стандартных исправлений элементов конфигурации</span><span class="sxs-lookup"><span data-stu-id="447ae-111">Distribute and register UE-V templates using standard Configuration Item remediation</span></span>

-   <span data-ttu-id="447ae-112">Создание или обновление элемента конфигурации политики агента UE-V для задания или отмены этих параметров.</span><span class="sxs-lookup"><span data-stu-id="447ae-112">Create or update a UE-V Agent policy configuration item to set or clear these settings.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="447ae-113">Максимальный размер пакета</span><span class="sxs-lookup"><span data-stu-id="447ae-113">Max package size</span></span></p></td>
    <td align="left"><p><span data-ttu-id="447ae-114">Включение и отключение синхронизации приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="447ae-114">Enable/disable Windows app sync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="447ae-115">Ожидание синхронизации при запуске приложения</span><span class="sxs-lookup"><span data-stu-id="447ae-115">Wait for sync on application start</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="447ae-116">Настройка задержки импорта</span><span class="sxs-lookup"><span data-stu-id="447ae-116">Setting import delay</span></span></p></td>
    <td align="left"><p><span data-ttu-id="447ae-117">Синхронизация приложений для Windows, не имеющих списка</span><span class="sxs-lookup"><span data-stu-id="447ae-117">Sync unlisted Windows apps</span></span></p></td>
    <td align="left"><p><span data-ttu-id="447ae-118">Ожидание синхронизации при входе</span><span class="sxs-lookup"><span data-stu-id="447ae-118">Wait for sync on logon</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="447ae-119">Уведомление о импорте параметров</span><span class="sxs-lookup"><span data-stu-id="447ae-119">Settings import notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="447ae-120">URL-адрес контакта</span><span class="sxs-lookup"><span data-stu-id="447ae-120">IT contact URL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="447ae-121">Ожидание тайм-аута синхронизации</span><span class="sxs-lookup"><span data-stu-id="447ae-121">Wait for sync timeout</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="447ae-122">Путь к хранилищу параметров</span><span class="sxs-lookup"><span data-stu-id="447ae-122">Settings storage path</span></span></p></td>
    <td align="left"><p><span data-ttu-id="447ae-123">Описательный текст для контакта</span><span class="sxs-lookup"><span data-stu-id="447ae-123">IT contact descriptive text</span></span></p></td>
    <td align="left"><p><span data-ttu-id="447ae-124">Путь к каталогу шаблонов параметров</span><span class="sxs-lookup"><span data-stu-id="447ae-124">Settings template catalog path</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="447ae-125">Включение синхронизации</span><span class="sxs-lookup"><span data-stu-id="447ae-125">Sync enablement</span></span></p></td>
    <td align="left"><p><span data-ttu-id="447ae-126">Значок панели включен</span><span class="sxs-lookup"><span data-stu-id="447ae-126">Tray icon enabled</span></span></p></td>
    <td align="left"><p><span data-ttu-id="447ae-127">Запуск и остановка службы агента UE-V</span><span class="sxs-lookup"><span data-stu-id="447ae-127">Start/Stop UE-V agent service</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="447ae-128">Метод синхронизации</span><span class="sxs-lookup"><span data-stu-id="447ae-128">Sync method</span></span></p></td>
    <td align="left"><p><span data-ttu-id="447ae-129">Уведомление о первом использовании</span><span class="sxs-lookup"><span data-stu-id="447ae-129">First use notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="447ae-130">Укажите, какие приложения Windows будут перемещаться по параметрам</span><span class="sxs-lookup"><span data-stu-id="447ae-130">Define which Windows apps will roam settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="447ae-131">Время ожидания синхронизации</span><span class="sxs-lookup"><span data-stu-id="447ae-131">Sync timeout</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="447ae-132">Проверьте соответствие, убедившись в том, что UE-V запущен.</span><span class="sxs-lookup"><span data-stu-id="447ae-132">Verify compliance by confirming that UE-V is running.</span></span>

## <span data-ttu-id="447ae-133">Создание элемента конфигурации политики агента UE-V</span><span class="sxs-lookup"><span data-stu-id="447ae-133">Generate a UE-V Agent Policy Configuration Item</span></span>


<span data-ttu-id="447ae-134">Все политики и конфигурации агента UE-V распространяются через один элемент конфигурации, созданный с помощью средства UevAgentPolicyGenerator.exe.</span><span class="sxs-lookup"><span data-stu-id="447ae-134">All UE-V Agent policy and configuration is distributed through a single configuration item that is generated using the UevAgentPolicyGenerator.exe tool.</span></span> <span data-ttu-id="447ae-135">Это средство считывает необходимую конфигурацию из XML-файла конфигурации и создает CI, содержащий настройки обнаружения и устранения неполадок, необходимые для обеспечения соответствия компьютеру.</span><span class="sxs-lookup"><span data-stu-id="447ae-135">This tool reads the desired configuration from an XML configuration file and creates a CI containing the discovery and remediation settings needed to bring the machine into compliance.</span></span>

<span data-ttu-id="447ae-136">CAB-файл, созданный UevTemplateBaselineGenerator.exe с помощью средства командной строки "Настройка политики агента (UE) Agent", имеет следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="447ae-136">The UE-V Agent policy configuration item CAB file is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="447ae-137">&lt;Код сайта сайта&gt;</span><span class="sxs-lookup"><span data-stu-id="447ae-137">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="447ae-138">PolicyName &lt; ( &gt; необязательно): по умолчанию используется значение "политика агента UE-V", если оно отсутствует</span><span class="sxs-lookup"><span data-stu-id="447ae-138">PolicyName &lt;name&gt; Optional: Defaults to “UE-V Agent Policy” if not present</span></span>

-   <span data-ttu-id="447ae-139">PolicyDescription &lt; Описание ( &gt; необязательно): предоставляется описание, если оно отсутствует</span><span class="sxs-lookup"><span data-stu-id="447ae-139">PolicyDescription &lt;description&gt; Optional: A description is provided if not present</span></span>

-   <span data-ttu-id="447ae-140">CabFilePath &lt; полный путь к элементу конфигурации. CAB-файл&gt;</span><span class="sxs-lookup"><span data-stu-id="447ae-140">CabFilePath &lt;full path to configuration item .CAB file&gt;</span></span>

-   <span data-ttu-id="447ae-141">ConfigurationFile &lt; полный путь к XML-файлу конфигурации агента&gt;</span><span class="sxs-lookup"><span data-stu-id="447ae-141">ConfigurationFile &lt;full path to agent configuration XML file&gt;</span></span>

<span data-ttu-id="447ae-142">**Примечание**  Возможно, потребуется изменить политику выполнения PowerShell, чтобы разрешить выполнение этих сценариев в среде.</span><span class="sxs-lookup"><span data-stu-id="447ae-142">**Note** It might be necessary to change the PowerShell execution policy to allow these scripts to run in your environment.</span></span> <span data-ttu-id="447ae-143">В консоли Configuration Manager выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="447ae-143">Perform these steps in the Configuration Manager console:</span></span>

1.  <span data-ttu-id="447ae-144">Выбор \*\* &gt; &gt; свойств параметров клиента администрирования\*\*</span><span class="sxs-lookup"><span data-stu-id="447ae-144">Select **Administration &gt; Client Settings &gt; Properties**</span></span>

2.  <span data-ttu-id="447ae-145">На вкладке **Агент пользователя** установите для **политики выполнения PowerShell** значение **минуя**</span><span class="sxs-lookup"><span data-stu-id="447ae-145">In the **User Agent** tab, set the **PowerShell Execution Policy** to **Bypass**</span></span>

<a href="" id="create"></a>**<span data-ttu-id="447ae-146">Создание первого элемента конфигурации политики UE-V</span><span class="sxs-lookup"><span data-stu-id="447ae-146">Create the First UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="447ae-147">Скопируйте файл конфигурации по умолчанию из каталога установки UE-V config в расположение, которое видно на консоли администрирования Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="447ae-147">Copy the default settings configuration file from the UE-V Config Pack installation directory to a location visible to your ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    <span data-ttu-id="447ae-148">Файл конфигурации по умолчанию состоит из пяти разделов.</span><span class="sxs-lookup"><span data-stu-id="447ae-148">The default configuration file contains five sections:</span></span>

    <a href="" id="computer-policy"></a>**<span data-ttu-id="447ae-149">Политика компьютера</span><span class="sxs-lookup"><span data-stu-id="447ae-149">Computer Policy</span></span>**  
    <span data-ttu-id="447ae-150">Все параметры уровня компьютера UE-V.</span><span class="sxs-lookup"><span data-stu-id="447ae-150">All UE-V machine level settings.</span></span> <span data-ttu-id="447ae-151">Атрибут DesiredState можно</span><span class="sxs-lookup"><span data-stu-id="447ae-151">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="447ae-152">**Назначение значения** в реестре</span><span class="sxs-lookup"><span data-stu-id="447ae-152">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="447ae-153">**Снимите флажки** , чтобы удалить параметр.</span><span class="sxs-lookup"><span data-stu-id="447ae-153">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="447ae-154">**Неуправляемый** , чтобы элемент конфигурации остался в текущем состоянии</span><span class="sxs-lookup"><span data-stu-id="447ae-154">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="447ae-155">Не удаляйте строки из этого раздела.</span><span class="sxs-lookup"><span data-stu-id="447ae-155">Do not remove lines from this section.</span></span> <span data-ttu-id="447ae-156">Вместо этого установите для DesiredState значение "неуправляемая", если Configuration Manager не нужно изменять текущие или значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="447ae-156">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="currentcomputeruserpolicy"></a>**<span data-ttu-id="447ae-157">CurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="447ae-157">CurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="447ae-158">Все параметры пользовательского уровня UE-V.</span><span class="sxs-lookup"><span data-stu-id="447ae-158">All UE-V user level settings.</span></span> <span data-ttu-id="447ae-159">Эти записи переопределяют параметры компьютера для пользователя.</span><span class="sxs-lookup"><span data-stu-id="447ae-159">These entries override the machine settings for a user.</span></span> <span data-ttu-id="447ae-160">Атрибут DesiredState можно</span><span class="sxs-lookup"><span data-stu-id="447ae-160">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="447ae-161">**Назначение значения** в реестре</span><span class="sxs-lookup"><span data-stu-id="447ae-161">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="447ae-162">**Снимите флажки** , чтобы удалить параметр.</span><span class="sxs-lookup"><span data-stu-id="447ae-162">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="447ae-163">**Неуправляемый** , чтобы элемент конфигурации остался в текущем состоянии</span><span class="sxs-lookup"><span data-stu-id="447ae-163">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="447ae-164">Не удаляйте строки из этого раздела.</span><span class="sxs-lookup"><span data-stu-id="447ae-164">Do not remove lines from this section.</span></span> <span data-ttu-id="447ae-165">Вместо этого установите для DesiredState значение "неуправляемая", если Configuration Manager не нужно изменять текущие или значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="447ae-165">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="services"></a>**<span data-ttu-id="447ae-166">Службы</span><span class="sxs-lookup"><span data-stu-id="447ae-166">Services</span></span>**  
    <span data-ttu-id="447ae-167">Операции в этом разделе: Служба управления.</span><span class="sxs-lookup"><span data-stu-id="447ae-167">Entries in this section control service operation.</span></span> <span data-ttu-id="447ae-168">Файл конфигурации по умолчанию состоит из одной записи для UevAgentService.</span><span class="sxs-lookup"><span data-stu-id="447ae-168">The default configuration file contains a single entry for the UevAgentService.</span></span> <span data-ttu-id="447ae-169">Для атрибута DesiredState можно установить значение " **выполняется** " или " **остановлено**".</span><span class="sxs-lookup"><span data-stu-id="447ae-169">The DesiredState attribute can be set to **Running** or **Stopped**.</span></span>

    <a href="" id="windows8appscomputerpolicy"></a>**<span data-ttu-id="447ae-170">Windows8AppsComputerPolicy</span><span class="sxs-lookup"><span data-stu-id="447ae-170">Windows8AppsComputerPolicy</span></span>**  
    <span data-ttu-id="447ae-171">Все параметры синхронизации приложений для Windows на уровне компьютера.</span><span class="sxs-lookup"><span data-stu-id="447ae-171">All machine level Windows app synchronization settings.</span></span> <span data-ttu-id="447ae-172">Каждому PackageFamilyName, указанному в этом разделе, можно назначить DesiredState</span><span class="sxs-lookup"><span data-stu-id="447ae-172">Each PackageFamilyName listed in this section can be assigned a DesiredState of</span></span>

    -   <span data-ttu-id="447ae-173">**Включение** перемещения параметров</span><span class="sxs-lookup"><span data-stu-id="447ae-173">**Enabled** to have settings roam</span></span>

    -   <span data-ttu-id="447ae-174">**Отключено** для предотвращения перемещения параметров</span><span class="sxs-lookup"><span data-stu-id="447ae-174">**Disabled** to prevent settings from roaming</span></span>

    -   <span data-ttu-id="447ae-175">**Очищено** , что элемент удален из элемента управления UE-V</span><span class="sxs-lookup"><span data-stu-id="447ae-175">**Cleared** to have the entry removed from UE-V control</span></span>

    <span data-ttu-id="447ae-176">В этот раздел можно добавить дополнительные строки на основе списка установленных приложений для Windows, которые можно просмотреть с помощью командлета PowerShell GetAppxPackage.</span><span class="sxs-lookup"><span data-stu-id="447ae-176">Additional lines can be added to this section based on the list of installed Windows apps that can be viewed using the PowerShell cmdlet GetAppxPackage.</span></span>

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**<span data-ttu-id="447ae-177">Windows8AppsCurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="447ae-177">Windows8AppsCurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="447ae-178">Идентичен Windows8AppsComputerPolicy с параметрами, переопределяющими параметры компьютера для отдельного пользователя.</span><span class="sxs-lookup"><span data-stu-id="447ae-178">Identical to the Windows8AppsComputerPolicy with settings that override machine settings for an individual user.</span></span>

2.  <span data-ttu-id="447ae-179">Измените файл конфигурации, изменив нужные поля состояния и значения.</span><span class="sxs-lookup"><span data-stu-id="447ae-179">Edit the configuration file by changing the desired state and value fields.</span></span>

3.  <span data-ttu-id="447ae-180">Выполните эту команду на компьютере, на котором запущена консоль администрирования ConfigMgr:</span><span class="sxs-lookup"><span data-stu-id="447ae-180">Run this command on a machine running the ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  <span data-ttu-id="447ae-181">Импорт CAB-файла с помощью консоли ConfigMgr или импорта PowerShell — CMConfigurationItem</span><span class="sxs-lookup"><span data-stu-id="447ae-181">Import the CAB file using ConfigMgr console or PowerShell Import-CMConfigurationItem</span></span>

**<span data-ttu-id="447ae-182">Обновление элемента конфигурации политики UE-V</span><span class="sxs-lookup"><span data-stu-id="447ae-182">Update a UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="447ae-183">Измените файл конфигурации, изменив нужные поля состояния и значения.</span><span class="sxs-lookup"><span data-stu-id="447ae-183">Edit the configuration file by changing the desired state and value fields.</span></span>

2.  <span data-ttu-id="447ae-184">Выполните команду, указанную на шаге 3, в разделе [Создание первого элемента конфигурации политики UE-V](#create).</span><span class="sxs-lookup"><span data-stu-id="447ae-184">Run the command from Step 3 in [Create the First UE-V Policy Configuration Item](#create).</span></span> <span data-ttu-id="447ae-185">Если вы изменили имя с помощью параметра PolicyName, убедитесь, что вы ввели то же имя.</span><span class="sxs-lookup"><span data-stu-id="447ae-185">If you changed the name with the PolicyName parameter, make sure you enter the same name.</span></span>

3.  <span data-ttu-id="447ae-186">Повторно импортируйте CAB-файл.</span><span class="sxs-lookup"><span data-stu-id="447ae-186">Reimport the CAB file.</span></span> <span data-ttu-id="447ae-187">Версия Configuration Manager будет обновлена.</span><span class="sxs-lookup"><span data-stu-id="447ae-187">The version in ConfigMgr will be updated.</span></span>

## <span data-ttu-id="447ae-188">Создание базового шаблона UE-V</span><span class="sxs-lookup"><span data-stu-id="447ae-188">Generate a UE-V Template Baseline</span></span>
<span data-ttu-id="447ae-189">Шаблоны UE-V распространяются с помощью базового плана, содержащего несколько элементов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="447ae-189">UE-V templates are distributed using a baseline containing multiple configuration items.</span></span> <span data-ttu-id="447ae-190">Каждый элемент конфигурации включает сценарии обнаружения и устранения неполадок, необходимые для установки одного шаблона UE-V.</span><span class="sxs-lookup"><span data-stu-id="447ae-190">Each configuration item contains the discovery and remediation scripts needed to install one UE-V template.</span></span> <span data-ttu-id="447ae-191">Реальный шаблон UE-V внедрен в сценарий исправления для распространения с помощью стандартных функций элемента конфигурации.</span><span class="sxs-lookup"><span data-stu-id="447ae-191">The actual UE-V template is embedded within the remediation script for distribution using standard Configuration Item functionality.</span></span>

<span data-ttu-id="447ae-192">Базовый шаблон UE-V создается с помощью средства командной строки UevTemplateBaselineGenerator.exe, которое имеет следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="447ae-192">The UE-V template baseline is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="447ae-193">&lt;Код сайта сайта&gt;</span><span class="sxs-lookup"><span data-stu-id="447ae-193">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="447ae-194">BaselineName &lt; имя &gt; (необязательно: по умолчанию — "UE-V Template дистрибутив Baseline", если не указано)</span><span class="sxs-lookup"><span data-stu-id="447ae-194">BaselineName &lt;name&gt; (Optional: defaults to “UE-V Template Distribution Baseline” if not present)</span></span>

-   <span data-ttu-id="447ae-195">&lt;Описание BaselineDescription &gt; (необязательно: описание предоставляется, если оно отсутствует)</span><span class="sxs-lookup"><span data-stu-id="447ae-195">BaselineDescription &lt;description&gt; (Optional: a description is provided if not present)</span></span>

-   <span data-ttu-id="447ae-196">&lt;Папка шаблонов UE-V TemplateFolder&gt;</span><span class="sxs-lookup"><span data-stu-id="447ae-196">TemplateFolder &lt;UE-V template folder&gt;</span></span>

-   <span data-ttu-id="447ae-197">Зарегистрировать &lt; список файлов шаблонов, разделенных запятыми&gt;</span><span class="sxs-lookup"><span data-stu-id="447ae-197">Register &lt;comma separated template file list&gt;</span></span>

-   <span data-ttu-id="447ae-198">Отмена регистрации &lt; списка шаблонов, разделенных запятыми&gt;</span><span class="sxs-lookup"><span data-stu-id="447ae-198">Unregister &lt;comma separated template list&gt;</span></span>

-   <span data-ttu-id="447ae-199">CabFilePath &lt; полный путь к создаваемому шаблону CAB-файла&gt;</span><span class="sxs-lookup"><span data-stu-id="447ae-199">CabFilePath &lt;Full path to baseline CAB file to generate&gt;</span></span>

<span data-ttu-id="447ae-200">Результат — это исходный CAB-файл, который готов для импорта в Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="447ae-200">The result is a baseline CAB file that is ready for import into Configuration Manager.</span></span> <span data-ttu-id="447ae-201">Если вы обновляете или добавляете шаблон в будущем, вы можете повторно выполнить команду с тем же именем базового плана.</span><span class="sxs-lookup"><span data-stu-id="447ae-201">If at a future date, you update or add a template, you can rerun the command using the same baseline name.</span></span> <span data-ttu-id="447ae-202">Импорт CAB-файла приводит к обновлению версии CI на измененных шаблонах.</span><span class="sxs-lookup"><span data-stu-id="447ae-202">Importing the CAB results in CI version updates on the changed templates.</span></span>

### <a href="" id="create2"></a><span data-ttu-id="447ae-203">Создание первого базового шаблона для UE-V</span><span class="sxs-lookup"><span data-stu-id="447ae-203">Create the First UE-V Template Baseline</span></span>

1.  <span data-ttu-id="447ae-204">Создайте набор шаблонов UE-V в стабильном расположении папки, видимой для компьютера, на котором работает консоль администратора ConfigMgr.</span><span class="sxs-lookup"><span data-stu-id="447ae-204">Create a “master” set of UE-V templates in a stable folder location visible to the machine running your ConfigMgr Admin Console.</span></span> <span data-ttu-id="447ae-205">По мере добавления или обновления шаблонов в этой папке они будут извлечены для распространения.</span><span class="sxs-lookup"><span data-stu-id="447ae-205">As templates are added or updated, this folder is where they are pulled for distribution.</span></span> <span data-ttu-id="447ae-206">Начальный список шаблонов можно скопировать с компьютера, на котором установлен UE-V.</span><span class="sxs-lookup"><span data-stu-id="447ae-206">The initial list of templates can be copied from a machine with UE-V installed.</span></span> <span data-ttu-id="447ae-207">Расположение шаблона по умолчанию — C:\\program Files Files\\Microsoft взаимодействие с пользователем Virtualization\\Templates.</span><span class="sxs-lookup"><span data-stu-id="447ae-207">The default template location is C:\\Program Files\\Microsoft User Experience Virtualization\\Templates.</span></span>

2.  <span data-ttu-id="447ae-208">Создайте файл text.bat, в который вы можете добавить команду генератора шаблонов.</span><span class="sxs-lookup"><span data-stu-id="447ae-208">Create a text.bat file where you can add the template generator command.</span></span> <span data-ttu-id="447ae-209">Это необязательно, но создание повторного создания будет проще, если сохранить параметры команды.</span><span class="sxs-lookup"><span data-stu-id="447ae-209">This is optional, but will make regeneration simpler if you save the command parameters.</span></span>

3.  <span data-ttu-id="447ae-210">Добавьте команду и параметры в bat – файл, который будет создавать базовый план.</span><span class="sxs-lookup"><span data-stu-id="447ae-210">Add the command and parameters to the .bat file that will generate the baseline.</span></span> <span data-ttu-id="447ae-211">В следующем примере создается базовый план, который распределяет блокноты и калькулятор.</span><span class="sxs-lookup"><span data-stu-id="447ae-211">The following example creates a baseline that distributes Notepad and Calculator:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  <span data-ttu-id="447ae-212">Запустите bat – файл, чтобы создать UevTemplateBaseline.cab готовы для импорта в Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="447ae-212">Run the .bat file to create UevTemplateBaseline.cab ready for import into Configuration Manager.</span></span>

### <span data-ttu-id="447ae-213">Обновление базового шаблона UE-V</span><span class="sxs-lookup"><span data-stu-id="447ae-213">Update a UE-V Template Baseline</span></span>

<span data-ttu-id="447ae-214">Генератор шаблонов использует версию шаблона, чтобы определить, нужно ли обновлять шаблон.</span><span class="sxs-lookup"><span data-stu-id="447ae-214">The template generator uses the template version to determine if a template should be updated.</span></span> <span data-ttu-id="447ae-215">Если вы изменяете шаблон и обновляете версию, базовый генератор сравнивает шаблон в главной папке с шаблоном, который содержится в CI на сервере Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="447ae-215">If you make a template change and update the version, the baseline generator compares the template in your master folder with the template contained in the CI on the ConfigMgr server.</span></span> <span data-ttu-id="447ae-216">При обнаружении разницы обновляются сформированный базовый план и измененные версии CI.</span><span class="sxs-lookup"><span data-stu-id="447ae-216">If a difference is found, the generated baseline and modified CI versions are updated.</span></span>

<span data-ttu-id="447ae-217">Чтобы распространить новый шаблон блокнота, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="447ae-217">To distribute a new Notepad template, you would perform these steps:</span></span>

1.  <span data-ttu-id="447ae-218">Обновите шаблон и версию шаблона, расположенные &lt; в &gt; элементе Version шаблона.</span><span class="sxs-lookup"><span data-stu-id="447ae-218">Update the template and template version located in the &lt;Version&gt; element of the template.</span></span>

2.  <span data-ttu-id="447ae-219">Скопируйте шаблон в основной каталог шаблонов.</span><span class="sxs-lookup"><span data-stu-id="447ae-219">Copy the template to your master template directory.</span></span>

3.  <span data-ttu-id="447ae-220">Выполните команду в файле. bat, созданном на этапе 3, в разделе [Создание первого базового шаблона UE-V](#create2).</span><span class="sxs-lookup"><span data-stu-id="447ae-220">Run the command in the .bat file that you created in Step 3 in [Create the First UE-V Template Baseline](#create2).</span></span>

4.  <span data-ttu-id="447ae-221">Импортируйте созданный CAB-файл в Configuration Manager с помощью консоли или импортной оболочки PowerShell — CMBaseline.</span><span class="sxs-lookup"><span data-stu-id="447ae-221">Import the generated CAB file into ConfigMgr using the console or PowerShell Import-CMBaseline.</span></span>

## <span data-ttu-id="447ae-222">Получение пакета конфигурации UE-V</span><span class="sxs-lookup"><span data-stu-id="447ae-222">Get the UE-V Configuration Pack</span></span>


<span data-ttu-id="447ae-223">Пакет конфигурации UE-V для Configuration Manager 2012 с пакетом обновления 1 (SP1) или более поздней версии можно загрузить [здесь](https://go.microsoft.com/fwlink/?LinkId=317263).</span><span class="sxs-lookup"><span data-stu-id="447ae-223">The UE-V Configuration Pack for Configuration Manager 2012 SP1 or later can be downloaded [here](https://go.microsoft.com/fwlink/?LinkId=317263).</span></span>






## <span data-ttu-id="447ae-224">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="447ae-224">Related topics</span></span>


[<span data-ttu-id="447ae-225">Управление конфигурациями UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="447ae-225">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





