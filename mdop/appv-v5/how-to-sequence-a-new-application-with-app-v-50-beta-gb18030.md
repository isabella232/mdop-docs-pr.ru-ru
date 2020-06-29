---
title: Виртуализация нового приложения с помощью App-V 5.0
description: Виртуализация нового приложения с помощью App-V 5.0
author: dansimp
ms.assetid: a263fa84-cd6d-4219-a5c2-eb6a553b826c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 13fdda066f79d918da1970e0cab6c1d6e60f6585
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813720"
---
# <span data-ttu-id="9e959-103">Виртуализация нового приложения с помощью App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="9e959-103">How to Sequence a New Application with App-V 5.0</span></span>


**<span data-ttu-id="9e959-104">Просмотр и подготовка перед началом последовательности</span><span class="sxs-lookup"><span data-stu-id="9e959-104">To review or do before you start sequencing</span></span>**

1.  <span data-ttu-id="9e959-105">Определите тип виртуализированного пакета приложения, который вы хотите создать:</span><span class="sxs-lookup"><span data-stu-id="9e959-105">Determine the type of virtualized application package you want to create:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="9e959-106">Тип приложения</span><span class="sxs-lookup"><span data-stu-id="9e959-106">Application type</span></span></th>
    <th align="left"><span data-ttu-id="9e959-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9e959-107">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9e959-108">Standard</span><span class="sxs-lookup"><span data-stu-id="9e959-108">Standard</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9e959-109">Создает пакет, содержащий приложение или набор приложений.</span><span class="sxs-lookup"><span data-stu-id="9e959-109">Creates a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="9e959-110">Этот параметр является предпочтительным для большинства типов приложений.</span><span class="sxs-lookup"><span data-stu-id="9e959-110">This is the preferred option for most application types.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9e959-111">Надстройка или плагин</span><span class="sxs-lookup"><span data-stu-id="9e959-111">Add-on or plug-in</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9e959-112">Создает пакет, который расширяет функциональные возможности стандартного приложения, например плагин для Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="9e959-112">Creates a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="9e959-113">Кроме того, вы можете использовать подключаемые модули для приложений, установленных в собственном коде, или для другого пакета, связанного с помощью групп подключения.</span><span class="sxs-lookup"><span data-stu-id="9e959-113">Additionally, you can use plug-ins for natively installed applications, or for another package that is linked by using connection groups.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9e959-114">Старые</span><span class="sxs-lookup"><span data-stu-id="9e959-114">Middleware</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9e959-115">Создает пакет, который необходим стандартному приложению, например Java.</span><span class="sxs-lookup"><span data-stu-id="9e959-115">Creates a package that is required by a standard application, for example, Java.</span></span> <span data-ttu-id="9e959-116">Пакеты по промежуточного слоя используются для связывания с другими пакетами с помощью групп подключений.</span><span class="sxs-lookup"><span data-stu-id="9e959-116">Middleware packages are used for linking to other packages by using connection groups.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="9e959-117">Скопируйте все необходимые файлы установки на компьютер, на котором работает секвенсор.</span><span class="sxs-lookup"><span data-stu-id="9e959-117">Copy all required installation files to the computer that is running the sequencer.</span></span>

3.  <span data-ttu-id="9e959-118">Создайте резервную копию виртуальной среды перед виртуализацией приложения, а затем вернитесь к этому образу каждый раз после завершения виртуализации приложения.</span><span class="sxs-lookup"><span data-stu-id="9e959-118">Make a backup image of your virtual environment before sequencing an application, and then revert to that image each time after you finish sequencing an application.</span></span>

4.  <span data-ttu-id="9e959-119">Просматривайте следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="9e959-119">Review the following items:</span></span>

    -   <span data-ttu-id="9e959-120">Если установщик приложения изменяет безопасный доступ к новому или существующему файлу или каталогу, эти изменения не фиксируются в пакете.</span><span class="sxs-lookup"><span data-stu-id="9e959-120">If an application installer changes the security access to a new or existing file or directory, those changes are not captured in the package.</span></span>

    -   <span data-ttu-id="9e959-121">Если для целевого тома виртуализированного пакета отключены короткие пути, необходимо также попытаться поочередно задать пакет для созданного тома, по-прежнему отключены короткие пути.</span><span class="sxs-lookup"><span data-stu-id="9e959-121">If short paths have been disabled for the virtualized package’s target volume, you must also sequence the package to a volume that was created and still has short-paths disabled.</span></span> <span data-ttu-id="9e959-122">Это не может быть системный том.</span><span class="sxs-lookup"><span data-stu-id="9e959-122">It cannot be the system volume.</span></span>

    -   <span data-ttu-id="9e959-123">Начиная с версии App-V 5,0 SP3, основной каталог виртуального приложения (PVAD) скрыт, но вы можете включить его снова.</span><span class="sxs-lookup"><span data-stu-id="9e959-123">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="9e959-124">Дополнительные [сведения о приложении App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="9e959-124">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>

**<span data-ttu-id="9e959-125">Создание последовательности нового стандартного приложения</span><span class="sxs-lookup"><span data-stu-id="9e959-125">To sequence a new standard application</span></span>**

1.  <span data-ttu-id="9e959-126">На компьютере с программой Sequencer выберите **все программы**, а затем — **Виртуализация приложений**Microsoft, а затем выберите **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="9e959-126">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="9e959-127">В секвенсоре щелкните **создать новый виртуальный пакет приложения**.</span><span class="sxs-lookup"><span data-stu-id="9e959-127">In the sequencer, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="9e959-128">Выберите команду **создать пакет (по умолчанию)**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-128">Select **Create Package (default)**, and then click **Next**.</span></span>

3.  <span data-ttu-id="9e959-129">На странице **Подготовка компьютера** изучите проблемы, которые могут привести к сбою при создании пакета или привести к тому, что пакет может содержать ненужные данные.</span><span class="sxs-lookup"><span data-stu-id="9e959-129">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="9e959-130">Прежде чем продолжить, устраните все возможные проблемы.</span><span class="sxs-lookup"><span data-stu-id="9e959-130">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="9e959-131">После внесения исправлений нажмите кнопку **Обновить** , чтобы отобразить обновленные сведения.</span><span class="sxs-lookup"><span data-stu-id="9e959-131">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="9e959-132">После устранения всех возможных проблем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-132">After you have resolved all potential issues, click **Next**.</span></span>

    **<span data-ttu-id="9e959-133">Важно.</span><span class="sxs-lookup"><span data-stu-id="9e959-133">Important</span></span>**  
    <span data-ttu-id="9e959-134">Если вы хотите отключить антивирусную программу, необходимо сначала проверить компьютер, на котором работает секвенсор, чтобы убедиться в том, что нежелательные или вредоносные файлы не могут быть добавлены в пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-134">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4.  <span data-ttu-id="9e959-135">На странице **Тип приложения** установите флажок **стандартное приложение (по умолчанию)** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-135">On the **Type of Application** page, click the **Standard Application (default)** check box, and then click **Next**.</span></span>

5.  <span data-ttu-id="9e959-136">На странице " **Выбор установщика** " нажмите кнопку **Обзор** и укажите файл установки для приложения.</span><span class="sxs-lookup"><span data-stu-id="9e959-136">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span>

    **<span data-ttu-id="9e959-137">Примечание.</span><span class="sxs-lookup"><span data-stu-id="9e959-137">Note</span></span>**  
    <span data-ttu-id="9e959-138">Если указанный установщик приложения изменяет безопасность доступа к файлу или папке, существующим или новым, связанные изменения не будут записаны в пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-138">If the specified application installer modifies security access to a file or directory, existing or new, the associated changes will not be captured into the package.</span></span>



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. <span data-ttu-id="9e959-139">На странице " **имя пакета** " введите имя, которое будет сопоставлено с пакетом.</span><span class="sxs-lookup"><span data-stu-id="9e959-139">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="9e959-140">Используйте имя, которое помогает идентифицировать цель и версию приложения, которые будут добавлены в пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-140">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="9e959-141">Имя пакета отобразится в консоли управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9e959-141">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="9e959-142">**Основной каталог виртуальных приложений** отображает путь, по которому приложение будет установлено на конечных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="9e959-142">The **Primary Virtual Application Directory** displays the path where the application will be installed on target computers.</span></span> <span data-ttu-id="9e959-143">Чтобы указать это расположение, нажмите кнопку **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="9e959-143">To specify this location, select **Browse**.</span></span>

   **<span data-ttu-id="9e959-144">Примечание.</span><span class="sxs-lookup"><span data-stu-id="9e959-144">Note</span></span>**  
   <span data-ttu-id="9e959-145">Начиная с версии App-V 5,0 SP3, основной каталог виртуального приложения (PVAD) скрыт, но вы можете включить его снова.</span><span class="sxs-lookup"><span data-stu-id="9e959-145">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="9e959-146">Дополнительные [сведения о приложении App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="9e959-146">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>



~~~
**Important**  
The primary application virtual directory should match the installation location for the application that is being sequenced. For example, if you install Notepad to **C:\\Program Files\\Notepad**; you should configure **C:\\Program Files\\Notepad** as your primary virtual directory. Alternatively, you can choose to set **C:\\Notepad** as the primary virtual application directory, as long as during installation time, you configure the installer to install to **C:\\Notepad**. Editing the Application Virtualization path is an advanced configuration task. For most applications, the default path is recommended for the following reasons:

-   Application Compatibility. Some virtualized applications will not function correctly, or will fail to open if the directories are not configured with identical virtual directory paths.

-   Performance. Since no file system redirection is required, the runtime performance can improve.



**Tip**  
It is recommended that prior to Sequencing an application, you open the associated installer to determine the default installation directory, and then configure that location as the **Primary Virtual Application Directory**.



Click **Next**.
~~~

7. <span data-ttu-id="9e959-147">На странице **установки** , когда секвенсор и установщик приложения готовы, вы можете продолжить установку приложения, чтобы секвенсор мог отслеживать процесс установки.</span><span class="sxs-lookup"><span data-stu-id="9e959-147">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span>

   **<span data-ttu-id="9e959-148">Важно.</span><span class="sxs-lookup"><span data-stu-id="9e959-148">Important</span></span>**  
   <span data-ttu-id="9e959-149">Вы должны всегда устанавливать приложения в безопасном месте и не можете войти в систему на компьютере, на котором запущены программы Sequencer во время наблюдения.</span><span class="sxs-lookup"><span data-stu-id="9e959-149">You should always install applications to a secure location and make sure no other users are logged on to the computer running the sequencer during monitoring.</span></span>



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. <span data-ttu-id="9e959-150">На странице **установки** подождите, пока секвенсор настроит пакет виртуализированного приложения.</span><span class="sxs-lookup"><span data-stu-id="9e959-150">On the **Installation** page, wait while the sequencer configures the virtualized application package.</span></span>

9. <span data-ttu-id="9e959-151">На странице **Настройка программного обеспечения** при необходимости запустите программы, содержащиеся в пакете.</span><span class="sxs-lookup"><span data-stu-id="9e959-151">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="9e959-152">Этот шаг позволяет выполнить необходимые задачи лицензирования или настройки перед развертыванием и запуском пакета на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="9e959-152">This step allows you to complete any necessary license or configuration tasks before you deploy and run the package on target computers.</span></span> <span data-ttu-id="9e959-153">Чтобы запустить все программы за один раз, выберите хотя бы одну программу, а затем нажмите кнопку **выполнить все**.</span><span class="sxs-lookup"><span data-stu-id="9e959-153">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="9e959-154">Чтобы запустить определенные программы, выберите программу или программы, а затем выберите команду **выполнить выбрано**.</span><span class="sxs-lookup"><span data-stu-id="9e959-154">To run specific programs, select the program or programs, and then click **Run Selected**.</span></span> <span data-ttu-id="9e959-155">Заполните необходимые задачи настройки и закройте приложения.</span><span class="sxs-lookup"><span data-stu-id="9e959-155">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="9e959-156">Возможно, потребуется подождать несколько минут, пока все программы не будут запущены.</span><span class="sxs-lookup"><span data-stu-id="9e959-156">You may need to wait several minutes for all programs to run.</span></span>

   **<span data-ttu-id="9e959-157">Примечание.</span><span class="sxs-lookup"><span data-stu-id="9e959-157">Note</span></span>**  
   <span data-ttu-id="9e959-158">Чтобы выполнить задачи при первом использовании для любого приложения, которое не доступно в списке, откройте приложение.</span><span class="sxs-lookup"><span data-stu-id="9e959-158">To run first-use tasks for any application that is not available in the list, open the application.</span></span> <span data-ttu-id="9e959-159">На этом этапе будут собраны соответствующие сведения.</span><span class="sxs-lookup"><span data-stu-id="9e959-159">The associated information will be captured during this step.</span></span>



~~~
Click **Next**.
~~~

10. <span data-ttu-id="9e959-160">На странице **отчета об установке** можно просмотреть сведения о виртуализированном пакете приложения, который вы только что посвящены.</span><span class="sxs-lookup"><span data-stu-id="9e959-160">On the **Installation Report** page, you can review information about the virtualized application package you have just sequenced.</span></span> <span data-ttu-id="9e959-161">В **дополнительных сведениях**дважды щелкните событие, чтобы получить более подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="9e959-161">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="9e959-162">Чтобы продолжить, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-162">To proceed, click **Next**.</span></span>

11. <span data-ttu-id="9e959-163">Откроется страница **настройки** .</span><span class="sxs-lookup"><span data-stu-id="9e959-163">The **Customize** page is displayed.</span></span> <span data-ttu-id="9e959-164">Если вы закончите установку и настройку виртуального приложения, нажмите кнопку **остановить сейчас** и перейдите к шагу 14 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="9e959-164">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="9e959-165">Чтобы выполнить любое из указанных ниже действий, нажмите кнопку **настроить**.</span><span class="sxs-lookup"><span data-stu-id="9e959-165">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="9e959-166">Подготовьте виртуальный пакет для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="9e959-166">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="9e959-167">Потоковая передача повышает удобство работы с виртуальным пакетом приложения на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="9e959-167">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="9e959-168">Укажите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-168">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="9e959-169">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-169">Click **Next**.</span></span>

12. <span data-ttu-id="9e959-170">На странице **потоковой передачи** запустите каждую программу, чтобы ее можно было оптимизировать и эффективно работать на конечных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="9e959-170">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="9e959-171">Выполнение всех приложений может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="9e959-171">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="9e959-172">После запуска всех приложений закройте все приложения и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-172">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   **<span data-ttu-id="9e959-173">Примечание.</span><span class="sxs-lookup"><span data-stu-id="9e959-173">Note</span></span>**  
   <span data-ttu-id="9e959-174">Если вы не откроете какие-либо приложения на этом этапе, потоковая передача по умолчанию будет доставлять по запросу.</span><span class="sxs-lookup"><span data-stu-id="9e959-174">If you do not open any applications during this step, the default streaming method is on-demand streaming delivery.</span></span> <span data-ttu-id="9e959-175">Это означает, что приложения будут загружаться по битам, пока он не будет открыт, а затем, в зависимости от того, как настроена Фоновая загрузка, будет загружаться оставшаяся часть приложения.</span><span class="sxs-lookup"><span data-stu-id="9e959-175">This means applications will be downloaded bit by bit until it can be opened, and then depending on how the background loading is configured, will load the rest of the application.</span></span>



13. <span data-ttu-id="9e959-176">На странице **Целевая операционная** система укажите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-176">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="9e959-177">Чтобы разрешить запуск этого пакета для всех поддерживаемых операционных систем в среде, установите флажок **Разрешить запуск этого пакета в любой операционной системе**.</span><span class="sxs-lookup"><span data-stu-id="9e959-177">To allow all supported operating systems in your environment to run this package, select **Allow this package to run on any operating system**.</span></span> <span data-ttu-id="9e959-178">Чтобы настроить выполнение этого пакета только в определенных операционных системах, установите флажок **Разрешить запуск этого пакета только в указанных ниже операционных системах** и выберите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-178">To configure this package to run only on specific operating systems, select **Allow this package to run only on the following operating systems** and select the operating systems that can run this package.</span></span> <span data-ttu-id="9e959-179">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-179">Click **Next**.</span></span>

   **<span data-ttu-id="9e959-180">Важно.</span><span class="sxs-lookup"><span data-stu-id="9e959-180">Important</span></span>**  
   <span data-ttu-id="9e959-181">Убедитесь в том, что указанные здесь операционные системы поддерживаются в приложении, которое вы используете в качестве последовательности.</span><span class="sxs-lookup"><span data-stu-id="9e959-181">Make sure that the operating systems you specify here are supported by the application you are sequencing.</span></span>



14. <span data-ttu-id="9e959-182">Откроется страница " **Создание пакета** ".</span><span class="sxs-lookup"><span data-stu-id="9e959-182">The **Create Package** page is displayed.</span></span> <span data-ttu-id="9e959-183">Чтобы изменить пакет, не сохраняя его, нажмите кнопку **продолжить, чтобы изменить пакет без сохранения с помощью редактора пакетов**.</span><span class="sxs-lookup"><span data-stu-id="9e959-183">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="9e959-184">Этот параметр открывает пакет на консоли секвенсор, чтобы можно было изменить пакет перед сохранением.</span><span class="sxs-lookup"><span data-stu-id="9e959-184">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="9e959-185">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-185">Click **Next**.</span></span>

   <span data-ttu-id="9e959-186">Чтобы сохранить пакет немедленно, выберите **сохранить пакет** (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="9e959-186">To save the package immediately, select **Save the package now** (default).</span></span> <span data-ttu-id="9e959-187">Добавьте **Комментарии** , которые должны быть связаны с пакетом.</span><span class="sxs-lookup"><span data-stu-id="9e959-187">Add optional **Comments** to be associated with the package.</span></span> <span data-ttu-id="9e959-188">Комментарии полезны для определения версии программы и другой информации о пакете.</span><span class="sxs-lookup"><span data-stu-id="9e959-188">Comments are useful for identifying the program version and other information about the package.</span></span>

   **<span data-ttu-id="9e959-189">Важно.</span><span class="sxs-lookup"><span data-stu-id="9e959-189">Important</span></span>**  
   <span data-ttu-id="9e959-190">Система не поддерживает непечатаемые символы в **комментариях** и **описаниях**.</span><span class="sxs-lookup"><span data-stu-id="9e959-190">The system does not support non-printable characters in **Comments** and **Descriptions**.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. <span data-ttu-id="9e959-191">Откроется страница **завершения** .</span><span class="sxs-lookup"><span data-stu-id="9e959-191">The **Completion** page is displayed.</span></span> <span data-ttu-id="9e959-192">При необходимости просмотрите сведения в области **отчета о пакетах виртуальных приложений** и нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9e959-192">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="9e959-193">Эти сведения также доступны в файле **Report.xml** , который находится в каталоге, в котором был создан пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-193">This information is also available in the **Report.xml** file that is located in the directory where the package was created.</span></span>

   <span data-ttu-id="9e959-194">Пакет теперь доступен в секвенсоре.</span><span class="sxs-lookup"><span data-stu-id="9e959-194">The package is now available in the sequencer.</span></span>

   **<span data-ttu-id="9e959-195">Важно.</span><span class="sxs-lookup"><span data-stu-id="9e959-195">Important</span></span>**  
   <span data-ttu-id="9e959-196">После того как вы успешно создадите виртуальный пакет приложения, вы не сможете запустить виртуальный пакет приложения на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="9e959-196">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



**<span data-ttu-id="9e959-197">Упорядочение надстройки или внешнего приложения</span><span class="sxs-lookup"><span data-stu-id="9e959-197">To sequence an add-on or plug-in application</span></span>**

1.  

    **<span data-ttu-id="9e959-198">Примечание.</span><span class="sxs-lookup"><span data-stu-id="9e959-198">Note</span></span>**  
    <span data-ttu-id="9e959-199">Перед выполнением описанной ниже процедуры установите родительское приложение локально на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="9e959-199">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="9e959-200">Или, если у вас есть виртуализированное родительское приложение, вы можете выполнить действия, описанные в рабочем процессе надстройки или плагина, чтобы распаковать родительское приложение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="9e959-200">Or if you have the parent application virtualized, you can follow the steps in the add-on or plug-in workflow to unpack the parent application on the computer.</span></span>

    <span data-ttu-id="9e959-201">Например, если вы подключаете плагин для Microsoft Excel, установите Microsoft Excel локально на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="9e959-201">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="9e959-202">Также установите родительское приложение в том же каталоге, где установлен приложение на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="9e959-202">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="9e959-203">Если плагин или надстройка будут использоваться с существующим пакетом виртуального приложения, установите приложение на тот же виртуальный диск, который использовался при создании родительского пакета виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="9e959-203">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="9e959-204">\*<strong><em>В секвенсоре щелкните \* </em> создать новый виртуальный пакет приложения </strong> .</span><span class="sxs-lookup"><span data-stu-id="9e959-204">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="9e959-205">Выберите команду **создать пакет (по умолчанию)**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-205">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="9e959-206">На странице **Подготовка компьютера** изучите проблемы, которые могут привести к сбою при создании пакета или привести к тому, что пакет может содержать ненужные данные.</span><span class="sxs-lookup"><span data-stu-id="9e959-206">On the **Prepare Computer** page, review the issues that might cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="9e959-207">Прежде чем продолжить, устраните все возможные проблемы.</span><span class="sxs-lookup"><span data-stu-id="9e959-207">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="9e959-208">После внесения исправлений нажмите кнопку **Обновить** , чтобы отобразить обновленные сведения.</span><span class="sxs-lookup"><span data-stu-id="9e959-208">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="9e959-209">После устранения всех возможных проблем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-209">After you have resolved all potential issues, click **Next**.</span></span>

   **<span data-ttu-id="9e959-210">Важно.</span><span class="sxs-lookup"><span data-stu-id="9e959-210">Important</span></span>**  
   <span data-ttu-id="9e959-211">Если вы хотите отключить антивирусную программу, необходимо сначала проверить компьютер, на котором работает секвенсор, чтобы убедиться в том, что нежелательные или вредоносные файлы не могут быть добавлены в пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-211">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4. <span data-ttu-id="9e959-212">На странице " **Тип приложения** " выберите **надстройку или плагин**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-212">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="9e959-213">На странице " **Выбор установщика** " нажмите кнопку **Обзор** и укажите установочный файл для надстройки или плагина.</span><span class="sxs-lookup"><span data-stu-id="9e959-213">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="9e959-214">Если у надстройки нет связанного файла установщика и вы планируете выполнить все инструкции по установке вручную, установите флажок **выбрать этот параметр, чтобы выполнить выборочную установку** , и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-214">If the add-on or plug-in does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="9e959-215">На **главной странице установки** убедитесь, что на компьютере, на котором запущена программа Sequencer, установлено основное приложение.</span><span class="sxs-lookup"><span data-stu-id="9e959-215">On the **Install Primary** page, ensure that the primary application is installed on the computer that runs the sequencer.</span></span> <span data-ttu-id="9e959-216">Кроме того, вы можете расширить существующий пакет, сохраненный локально на компьютере, на котором работает секвенсор.</span><span class="sxs-lookup"><span data-stu-id="9e959-216">Alternatively, you can expand an existing package that has been saved locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="9e959-217">Для этого щелкните **развернуть пакет**и выберите пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-217">To do this, click **Expand Package**, and then select the package.</span></span> <span data-ttu-id="9e959-218">После развертывания или установки родительской программы установите флажок **я установил основную родительскую программу**.</span><span class="sxs-lookup"><span data-stu-id="9e959-218">After you have expanded or installed the parent program, select **I have installed the primary parent program**.</span></span>

   <span data-ttu-id="9e959-219">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-219">Click **Next**.</span></span>

7. <span data-ttu-id="9e959-220">На странице " **имя пакета** " введите имя, которое будет сопоставлено с пакетом.</span><span class="sxs-lookup"><span data-stu-id="9e959-220">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="9e959-221">Используйте имя, которое помогает идентифицировать цель и версию приложения, которые будут добавлены в пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-221">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="9e959-222">Имя пакета будет отображаться в консоли управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9e959-222">The package name will be displayed in the App-V 5.0 Management Console.</span></span> <span data-ttu-id="9e959-223">**Основной каталог виртуальных приложений** отображает путь, по которому будет установлено приложение.</span><span class="sxs-lookup"><span data-stu-id="9e959-223">The **Primary Virtual Application Directory** displays the path where the application will be installed.</span></span> <span data-ttu-id="9e959-224">Чтобы указать это расположение, введите путь или нажмите кнопку **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="9e959-224">To specify this location, type the path, or click **Browse**.</span></span>

   **<span data-ttu-id="9e959-225">Примечание.</span><span class="sxs-lookup"><span data-stu-id="9e959-225">Note</span></span>**  
   <span data-ttu-id="9e959-226">Начиная с версии App-V 5,0 SP3, основной каталог виртуального приложения (PVAD) скрыт, но вы можете включить его снова.</span><span class="sxs-lookup"><span data-stu-id="9e959-226">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="9e959-227">Дополнительные [сведения о приложении App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="9e959-227">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>



~~~
Click **Next**.
~~~

8. <span data-ttu-id="9e959-228">На странице **установки** , когда секвенсор и установщик приложения готовы, вы можете продолжить установку плагина или надстройки, чтобы программа Sequencer могла отслеживать процесс установки.</span><span class="sxs-lookup"><span data-stu-id="9e959-228">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="9e959-229">Используйте процесс установки приложения для выполнения установки.</span><span class="sxs-lookup"><span data-stu-id="9e959-229">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="9e959-230">Если в процессе установки необходимо запустить дополнительные файлы установки, нажмите кнопку **выполнить** , найдите и запустите дополнительные файлы установки.</span><span class="sxs-lookup"><span data-stu-id="9e959-230">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="9e959-231">Когда вы закончите установку, выберите параметр **Установка завершена**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-231">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="9e959-232">На странице **отчета об установке** можно просмотреть сведения о пакете виртуального приложения, который вы только что посвящены.</span><span class="sxs-lookup"><span data-stu-id="9e959-232">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="9e959-233">Чтобы получить более подробное описание сведений, отображаемых в **дополнительных сведениях**, дважды щелкните событие.</span><span class="sxs-lookup"><span data-stu-id="9e959-233">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="9e959-234">После того как вы проверили данные, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-234">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="9e959-235">Откроется страница **настройки** .</span><span class="sxs-lookup"><span data-stu-id="9e959-235">The **Customize** page is displayed.</span></span> <span data-ttu-id="9e959-236">Если вы закончите установку и настройку виртуального приложения, нажмите кнопку **остановить сейчас** и перейдите к шагу 12 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="9e959-236">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 12 of this procedure.</span></span> <span data-ttu-id="9e959-237">Чтобы выполнить любое из указанных ниже действий, нажмите кнопку **настроить**.</span><span class="sxs-lookup"><span data-stu-id="9e959-237">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="9e959-238">Оптимизируйте работу пакета в медленной или ненадежной сети.</span><span class="sxs-lookup"><span data-stu-id="9e959-238">Optimize how the package will run across a slow or unreliable network.</span></span>

    -   <span data-ttu-id="9e959-239">Укажите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-239">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="9e959-240">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-240">Click **Next**.</span></span>

11. <span data-ttu-id="9e959-241">На странице **потоковой передачи** запустите каждую программу, чтобы ее можно было оптимизировать и эффективно работать на конечных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="9e959-241">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="9e959-242">Потоковая передача повышает удобство работы с виртуальным пакетом приложений на конечных компьютерах в сетях с большим временем задержки.</span><span class="sxs-lookup"><span data-stu-id="9e959-242">Streaming improves the experience when the virtual application package is run on target computers on high-latency networks.</span></span> <span data-ttu-id="9e959-243">Выполнение всех приложений может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="9e959-243">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="9e959-244">После запуска всех приложений закройте каждое из них.</span><span class="sxs-lookup"><span data-stu-id="9e959-244">After all applications have run, close each of the applications.</span></span> <span data-ttu-id="9e959-245">Кроме того, вы можете настроить пакет так, чтобы он был полностью скачан перед открытием, выбрав флажок **заставлять приложения для загрузки** .</span><span class="sxs-lookup"><span data-stu-id="9e959-245">You can also configure the package to be required to be fully downloaded before opening by selecting the **Force applications to be downloaded** check-box.</span></span> <span data-ttu-id="9e959-246">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-246">Click **Next**.</span></span>

   **<span data-ttu-id="9e959-247">Примечание.</span><span class="sxs-lookup"><span data-stu-id="9e959-247">Note</span></span>**  
   <span data-ttu-id="9e959-248">При необходимости вы можете остановить загрузку приложения на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="9e959-248">If necessary, you can stop an application from loading during this step.</span></span> <span data-ttu-id="9e959-249">В диалоговом окне **Запуск приложения** нажмите кнопку **остановить** и установите один из флажков: **остановить все приложения** или **остановить только это приложение**.</span><span class="sxs-lookup"><span data-stu-id="9e959-249">In the **Application Launch** dialog box, click **Stop** and select one of the check boxes: **Stop all applications** or **Stop this application only**.</span></span>



12. <span data-ttu-id="9e959-250">На странице **Целевая операционная** система укажите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-250">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="9e959-251">Чтобы разрешить запуск этого пакета для всех поддерживаемых операционных систем в вашей среде, установите флажок **Разрешить выполнение этого пакета для любой операционной системы** .</span><span class="sxs-lookup"><span data-stu-id="9e959-251">To allow all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="9e959-252">Чтобы настроить запуск этого пакета только в определенных операционных системах, установите флажок **Разрешить запуск этого пакета только на указанных ниже операционных системах** и выберите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-252">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="9e959-253">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-253">Click **Next**.</span></span>

13. <span data-ttu-id="9e959-254">Откроется страница " **Создание пакета** ".</span><span class="sxs-lookup"><span data-stu-id="9e959-254">The **Create Package** page is displayed.</span></span> <span data-ttu-id="9e959-255">Чтобы изменить пакет, не сохраняя его, установите флажок **продолжить изменение пакета без сохранения с помощью редактора пакетов** .</span><span class="sxs-lookup"><span data-stu-id="9e959-255">To modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="9e959-256">Этот параметр открывает пакет на консоли секвенсор, чтобы можно было изменить пакет перед сохранением.</span><span class="sxs-lookup"><span data-stu-id="9e959-256">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="9e959-257">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-257">Click **Next**.</span></span>

   <span data-ttu-id="9e959-258">Чтобы сохранить пакет немедленно, выберите **сохранить пакет прямо сейчас**.</span><span class="sxs-lookup"><span data-stu-id="9e959-258">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="9e959-259">При необходимости добавьте **Описание** , которое будет сопоставлено с пакетом.</span><span class="sxs-lookup"><span data-stu-id="9e959-259">Optionally, add a **Description** that will be associated with the package.</span></span> <span data-ttu-id="9e959-260">Описания полезны для идентификации версии и других сведений о пакете.</span><span class="sxs-lookup"><span data-stu-id="9e959-260">Descriptions are useful for identifying the version and other information about the package.</span></span>

   **<span data-ttu-id="9e959-261">Важно.</span><span class="sxs-lookup"><span data-stu-id="9e959-261">Important</span></span>**  
   <span data-ttu-id="9e959-262">Система не поддерживает непечатаемые символы в комментариях и описаниях.</span><span class="sxs-lookup"><span data-stu-id="9e959-262">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**<span data-ttu-id="9e959-263">Упорядочение приложения по промежуточного слоя</span><span class="sxs-lookup"><span data-stu-id="9e959-263">To sequence a middleware application</span></span>**

1. <span data-ttu-id="9e959-264">На компьютере с программой Sequencer выберите **все программы**, а затем — **Виртуализация приложений**Microsoft, а затем выберите **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="9e959-264">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="9e959-265">\*<strong><em>В секвенсоре щелкните \* </em> создать новый виртуальный пакет приложения </strong> .</span><span class="sxs-lookup"><span data-stu-id="9e959-265">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="9e959-266">Выберите команду **создать пакет (по умолчанию)**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-266">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="9e959-267">На странице **Подготовка компьютера** изучите проблемы, которые могут привести к сбою при создании пакета или привести к тому, что пакет может содержать ненужные данные.</span><span class="sxs-lookup"><span data-stu-id="9e959-267">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="9e959-268">Прежде чем продолжить, устраните все возможные проблемы.</span><span class="sxs-lookup"><span data-stu-id="9e959-268">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="9e959-269">После внесения исправлений нажмите кнопку **Обновить** , чтобы отобразить обновленные сведения.</span><span class="sxs-lookup"><span data-stu-id="9e959-269">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="9e959-270">После устранения всех возможных проблем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-270">After you have resolved all potential issues, click **Next**.</span></span>

   **<span data-ttu-id="9e959-271">Важно.</span><span class="sxs-lookup"><span data-stu-id="9e959-271">Important</span></span>**  
   <span data-ttu-id="9e959-272">Если вы хотите отключить антивирусную программу, необходимо сначала проверить компьютер, на котором работает секвенсор App-V 5,0, чтобы убедиться в том, что нежелательные или вредоносные файлы не могут быть добавлены в пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-272">If you are required to disable virus scanning software, you should first scan the computer that runs the App-V 5.0 Sequencer in order to ensure that no unwanted or malicious files can be added to the package.</span></span>



4. <span data-ttu-id="9e959-273">На странице **Тип приложения** выберите **промежуточный**по, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-273">On the **Type of Application** page, select **Middleware**, and then click **Next**.</span></span>

5. <span data-ttu-id="9e959-274">На странице " **Выбор установщика** " нажмите кнопку **Обзор** и укажите файл установки для приложения.</span><span class="sxs-lookup"><span data-stu-id="9e959-274">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="9e959-275">Если у приложения нет связанного файла установщика и вы планируете выполнить все инструкции по установке вручную, установите флажок **выбрать этот параметр, чтобы выполнить выборочную установку** , и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-275">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="9e959-276">На странице " **имя пакета** " введите имя, которое будет сопоставлено с пакетом.</span><span class="sxs-lookup"><span data-stu-id="9e959-276">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="9e959-277">Используйте имя, которое помогает идентифицировать цель и версию приложения, которые будут добавлены в пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-277">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="9e959-278">Имя пакета отобразится в консоли управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9e959-278">The package name is displayed in the App-V 5.0 Management Console.</span></span> <span data-ttu-id="9e959-279">**Основной каталог виртуальных приложений** отображает путь, по которому будет установлено приложение.</span><span class="sxs-lookup"><span data-stu-id="9e959-279">The **Primary Virtual Application Directory** displays the path where the application will be installed.</span></span> <span data-ttu-id="9e959-280">Чтобы указать это расположение, введите путь к файлу или нажмите кнопку **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="9e959-280">To specify this location, type the path or click **Browse**.</span></span>

   <span data-ttu-id="9e959-281">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-281">Click **Next**.</span></span>

7. <span data-ttu-id="9e959-282">На странице **установки** , когда программа Sequencer и установщик приложения по промежуточного слоя готовы, вы можете продолжить установку приложения, чтобы секвенсор мог отслеживать процесс установки.</span><span class="sxs-lookup"><span data-stu-id="9e959-282">On the **Installation** page, when the sequencer and middleware application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="9e959-283">Используйте процесс установки приложения для выполнения установки.</span><span class="sxs-lookup"><span data-stu-id="9e959-283">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="9e959-284">Если в процессе установки требуется выполнить дополнительные установочные файлы, нажмите кнопку **выполнить**, чтобы найти и запустить дополнительные файлы установки.</span><span class="sxs-lookup"><span data-stu-id="9e959-284">If additional installation files must be run as part of the installation, click **Run**, to locate and run the additional installation files.</span></span> <span data-ttu-id="9e959-285">После завершения установки установите флажок **Установка завершена** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-285">When you are finished with the installation, select the **I am finished installing** check box, and then click **Next**.</span></span>

8. <span data-ttu-id="9e959-286">На странице **установки** подождите, пока секвенсор настроит пакет виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="9e959-286">On the **Installation** page, wait while the sequencer configures the virtual application package.</span></span>

9. <span data-ttu-id="9e959-287">На странице **отчета об установке** можно просмотреть сведения о пакете виртуального приложения, который был только что упорядочен.</span><span class="sxs-lookup"><span data-stu-id="9e959-287">On the **Installation Report** page, you can review information about the virtual application package that you have just sequenced.</span></span> <span data-ttu-id="9e959-288">В **дополнительных сведениях**дважды щелкните событие, чтобы получить более подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="9e959-288">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="9e959-289">Чтобы продолжить, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-289">To proceed, click **Next**.</span></span>

10. <span data-ttu-id="9e959-290">На странице **Целевая операционная** система укажите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-290">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="9e959-291">Чтобы включить этот пакет для всех поддерживаемых операционных систем в среде, установите флажок **Разрешить выполнение этого пакета для любой операционной системы** .</span><span class="sxs-lookup"><span data-stu-id="9e959-291">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="9e959-292">Чтобы настроить запуск этого пакета только в определенных операционных системах, установите флажок **Разрешить запуск этого пакета только на указанных ниже операционных системах** и выберите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="9e959-292">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box and select the operating systems that can run this package.</span></span> <span data-ttu-id="9e959-293">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-293">Click **Next**.</span></span>

11. <span data-ttu-id="9e959-294">Откроется страница **Создание пакета** .</span><span class="sxs-lookup"><span data-stu-id="9e959-294">On the **Create Package** page is displayed.</span></span> <span data-ttu-id="9e959-295">Чтобы изменить пакет, не сохраняя его, нажмите кнопку **продолжить, чтобы изменить пакет без сохранения с помощью редактора пакетов**.</span><span class="sxs-lookup"><span data-stu-id="9e959-295">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="9e959-296">Этот параметр открывает пакет на консоли секвенсор, чтобы можно было изменить пакет перед сохранением.</span><span class="sxs-lookup"><span data-stu-id="9e959-296">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="9e959-297">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e959-297">Click **Next**.</span></span>

    <span data-ttu-id="9e959-298">Чтобы сохранить пакет немедленно, выберите **сохранить пакет прямо сейчас**.</span><span class="sxs-lookup"><span data-stu-id="9e959-298">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="9e959-299">При необходимости добавьте **Описание** , которое должно быть связано с пакетом.</span><span class="sxs-lookup"><span data-stu-id="9e959-299">Optionally, add a **Description** to be associated with the package.</span></span> <span data-ttu-id="9e959-300">Описания полезны для идентификации версии программы и других сведений о пакете.</span><span class="sxs-lookup"><span data-stu-id="9e959-300">Descriptions are useful for identifying the program version and other information about the package.</span></span>

    **<span data-ttu-id="9e959-301">Важно.</span><span class="sxs-lookup"><span data-stu-id="9e959-301">Important</span></span>**  
    <span data-ttu-id="9e959-302">Система не поддерживает непечатаемые символы в комментариях и описаниях.</span><span class="sxs-lookup"><span data-stu-id="9e959-302">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. <span data-ttu-id="9e959-303">Откроется страница **завершения** .</span><span class="sxs-lookup"><span data-stu-id="9e959-303">The **Completion** page is displayed.</span></span> <span data-ttu-id="9e959-304">При необходимости просмотрите сведения в области **отчета о пакетах виртуальных приложений** и нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9e959-304">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="9e959-305">Эти сведения также доступны в файле **Report.xml** , который находится в каталоге, указанном в действии 11 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="9e959-305">This information is also available in the **Report.xml** file that is located in the directory specified in step 11 of this procedure.</span></span>

   <span data-ttu-id="9e959-306">Пакет теперь доступен в секвенсоре.</span><span class="sxs-lookup"><span data-stu-id="9e959-306">The package is now available in the sequencer.</span></span> <span data-ttu-id="9e959-307">Чтобы изменить свойства пакета, нажмите **изменить \ [имя пакета \]**.</span><span class="sxs-lookup"><span data-stu-id="9e959-307">To edit the package properties, click **Edit \[Package Name\]**.</span></span>

   **<span data-ttu-id="9e959-308">Важно.</span><span class="sxs-lookup"><span data-stu-id="9e959-308">Important</span></span>**  
   <span data-ttu-id="9e959-309">После того как вы успешно создадите виртуальный пакет приложения, вы не сможете запустить виртуальный пакет приложения на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="9e959-309">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="9e959-310">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9e959-310">Related topics</span></span>


[<span data-ttu-id="9e959-311">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="9e959-311">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









