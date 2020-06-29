---
title: Виртуализация нового приложения с помощью App-V 5.1
description: Виртуализация нового приложения с помощью App-V 5.1
author: dansimp
ms.assetid: 7d7699b1-0cb8-450d-94e7-5af937e16c21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43edd9357e31f4884ed7baec3d35fa01bf2abe54
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813717"
---
# <span data-ttu-id="41105-103">Виртуализация нового приложения с помощью App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="41105-103">How to Sequence a New Application with App-V 5.1</span></span>


**<span data-ttu-id="41105-104">Просмотр и подготовка перед началом последовательности</span><span class="sxs-lookup"><span data-stu-id="41105-104">To review or do before you start sequencing</span></span>**

1.  <span data-ttu-id="41105-105">Определите тип виртуализированного пакета приложения, который вы хотите создать:</span><span class="sxs-lookup"><span data-stu-id="41105-105">Determine the type of virtualized application package you want to create:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="41105-106">Тип приложения</span><span class="sxs-lookup"><span data-stu-id="41105-106">Application type</span></span></th>
    <th align="left"><span data-ttu-id="41105-107">Описание</span><span class="sxs-lookup"><span data-stu-id="41105-107">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="41105-108">Standard</span><span class="sxs-lookup"><span data-stu-id="41105-108">Standard</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41105-109">Создает пакет, содержащий приложение или набор приложений.</span><span class="sxs-lookup"><span data-stu-id="41105-109">Creates a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="41105-110">Этот параметр является предпочтительным для большинства типов приложений.</span><span class="sxs-lookup"><span data-stu-id="41105-110">This is the preferred option for most application types.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="41105-111">Надстройка или плагин</span><span class="sxs-lookup"><span data-stu-id="41105-111">Add-on or plug-in</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41105-112">Создает пакет, который расширяет функциональные возможности стандартного приложения, например плагин для Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="41105-112">Creates a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="41105-113">Кроме того, вы можете использовать подключаемые модули для приложений, установленных в собственном коде, или для другого пакета, связанного с помощью групп подключения.</span><span class="sxs-lookup"><span data-stu-id="41105-113">Additionally, you can use plug-ins for natively installed applications, or for another package that is linked by using connection groups.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="41105-114">Старые</span><span class="sxs-lookup"><span data-stu-id="41105-114">Middleware</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41105-115">Создает пакет, который необходим стандартному приложению, например Java.</span><span class="sxs-lookup"><span data-stu-id="41105-115">Creates a package that is required by a standard application, for example, Java.</span></span> <span data-ttu-id="41105-116">Пакеты по промежуточного слоя используются для связывания с другими пакетами с помощью групп подключений.</span><span class="sxs-lookup"><span data-stu-id="41105-116">Middleware packages are used for linking to other packages by using connection groups.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="41105-117">Скопируйте все необходимые файлы установки на компьютер, на котором работает секвенсор.</span><span class="sxs-lookup"><span data-stu-id="41105-117">Copy all required installation files to the computer that is running the sequencer.</span></span>

3.  <span data-ttu-id="41105-118">Создайте резервную копию виртуальной среды перед виртуализацией приложения, а затем вернитесь к этому образу каждый раз после завершения виртуализации приложения.</span><span class="sxs-lookup"><span data-stu-id="41105-118">Make a backup image of your virtual environment before sequencing an application, and then revert to that image each time after you finish sequencing an application.</span></span>

4.  <span data-ttu-id="41105-119">Просматривайте следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="41105-119">Review the following items:</span></span>

    -   <span data-ttu-id="41105-120">Если установщик приложения изменяет безопасный доступ к новому или существующему файлу или каталогу, эти изменения не фиксируются в пакете.</span><span class="sxs-lookup"><span data-stu-id="41105-120">If an application installer changes the security access to a new or existing file or directory, those changes are not captured in the package.</span></span>

    -   <span data-ttu-id="41105-121">Если для целевого тома виртуализированного пакета отключены короткие пути, необходимо также попытаться поочередно задать пакет для созданного тома, по-прежнему отключены короткие пути.</span><span class="sxs-lookup"><span data-stu-id="41105-121">If short paths have been disabled for the virtualized package’s target volume, you must also sequence the package to a volume that was created and still has short-paths disabled.</span></span> <span data-ttu-id="41105-122">Это не может быть системный том.</span><span class="sxs-lookup"><span data-stu-id="41105-122">It cannot be the system volume.</span></span>

> [!NOTE]  
> <span data-ttu-id="41105-123">Секвенсор App-V 5. x не может последовательностей в приложениях с именами, соответствующими "CO_ &lt; x &gt; ", где x — любая цифра.</span><span class="sxs-lookup"><span data-stu-id="41105-123">The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="41105-124">Будет сгенерировано сообщение об ошибке 0x8007139F.</span><span class="sxs-lookup"><span data-stu-id="41105-124">Error 0x8007139F will be generated.</span></span>

**<span data-ttu-id="41105-125">Создание последовательности нового стандартного приложения</span><span class="sxs-lookup"><span data-stu-id="41105-125">To sequence a new standard application</span></span>**

1.  <span data-ttu-id="41105-126">На компьютере с программой Sequencer выберите **все программы**, а затем — **Виртуализация приложений**Microsoft, а затем выберите **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="41105-126">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="41105-127">В секвенсоре щелкните **создать новый виртуальный пакет приложения**.</span><span class="sxs-lookup"><span data-stu-id="41105-127">In the sequencer, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="41105-128">Выберите команду **создать пакет (по умолчанию)**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-128">Select **Create Package (default)**, and then click **Next**.</span></span>

3.  <span data-ttu-id="41105-129">На странице **Подготовка компьютера** изучите проблемы, которые могут привести к сбою при создании пакета или привести к тому, что пакет может содержать ненужные данные.</span><span class="sxs-lookup"><span data-stu-id="41105-129">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="41105-130">Прежде чем продолжить, устраните все возможные проблемы.</span><span class="sxs-lookup"><span data-stu-id="41105-130">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="41105-131">После внесения исправлений нажмите кнопку **Обновить** , чтобы отобразить обновленные сведения.</span><span class="sxs-lookup"><span data-stu-id="41105-131">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="41105-132">После устранения всех возможных проблем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-132">After you have resolved all potential issues, click **Next**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="41105-133">Если вы хотите отключить антивирусную программу, необходимо сначала проверить компьютер, на котором работает секвенсор, чтобы убедиться в том, что нежелательные или вредоносные файлы не могут быть добавлены в пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-133">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



~~~
> [!NOTE]  
> There is currently no way to disable Windows Defender in Windows 10. If you receive a warning, you can safely ignore it. It is unlikely that Windows Defender will affect sequencing at all.
~~~



4. <span data-ttu-id="41105-134">На странице **Тип приложения** установите флажок **стандартное приложение (по умолчанию)** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-134">On the **Type of Application** page, click the **Standard Application (default)** check box, and then click **Next**.</span></span>

5. <span data-ttu-id="41105-135">На странице " **Выбор установщика** " нажмите кнопку **Обзор** и укажите файл установки для приложения.</span><span class="sxs-lookup"><span data-stu-id="41105-135">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="41105-136">Если указанный установщик приложения изменяет безопасность доступа к файлу или папке, существующим или новым, связанные изменения не будут записаны в пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-136">If the specified application installer modifies security access to a file or directory, existing or new, the associated changes will not be captured into the package.</span></span>



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. <span data-ttu-id="41105-137">На странице " **имя пакета** " введите имя, которое будет сопоставлено с пакетом.</span><span class="sxs-lookup"><span data-stu-id="41105-137">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="41105-138">Используйте имя, которое помогает идентифицировать цель и версию приложения, которые будут добавлены в пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-138">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="41105-139">Имя пакета отобразится в консоли управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="41105-139">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="41105-140">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-140">Click **Next**.</span></span>

7. <span data-ttu-id="41105-141">На странице **установки** , когда секвенсор и установщик приложения готовы, вы можете продолжить установку приложения, чтобы секвенсор мог отслеживать процесс установки.</span><span class="sxs-lookup"><span data-stu-id="41105-141">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="41105-142">Вы должны всегда устанавливать приложения в безопасном месте и не можете войти в систему на компьютере, на котором запущены программы Sequencer во время наблюдения.</span><span class="sxs-lookup"><span data-stu-id="41105-142">You should always install applications to a secure location and make sure no other users are logged on to the computer running the sequencer during monitoring.</span></span>



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. <span data-ttu-id="41105-143">На странице **установки** подождите, пока секвенсор настроит пакет виртуализированного приложения.</span><span class="sxs-lookup"><span data-stu-id="41105-143">On the **Installation** page, wait while the sequencer configures the virtualized application package.</span></span>

9. <span data-ttu-id="41105-144">На странице **Настройка программного обеспечения** при необходимости запустите программы, содержащиеся в пакете.</span><span class="sxs-lookup"><span data-stu-id="41105-144">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="41105-145">Этот шаг позволяет выполнить необходимые задачи лицензирования или настройки перед развертыванием и запуском пакета на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="41105-145">This step allows you to complete any necessary license or configuration tasks before you deploy and run the package on target computers.</span></span> <span data-ttu-id="41105-146">Чтобы запустить все программы за один раз, выберите хотя бы одну программу, а затем нажмите кнопку **выполнить все**.</span><span class="sxs-lookup"><span data-stu-id="41105-146">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="41105-147">Чтобы запустить определенные программы, выберите программу или программы, а затем выберите команду **выполнить выбрано**.</span><span class="sxs-lookup"><span data-stu-id="41105-147">To run specific programs, select the program or programs, and then click **Run Selected**.</span></span> <span data-ttu-id="41105-148">Заполните необходимые задачи настройки и закройте приложения.</span><span class="sxs-lookup"><span data-stu-id="41105-148">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="41105-149">Возможно, потребуется подождать несколько минут, пока все программы не будут запущены.</span><span class="sxs-lookup"><span data-stu-id="41105-149">You may need to wait several minutes for all programs to run.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="41105-150">Чтобы выполнить задачи при первом использовании для любого приложения, которое не доступно в списке, откройте приложение.</span><span class="sxs-lookup"><span data-stu-id="41105-150">To run first-use tasks for any application that is not available in the list, open the application.</span></span> <span data-ttu-id="41105-151">На этом этапе будут собраны соответствующие сведения.</span><span class="sxs-lookup"><span data-stu-id="41105-151">The associated information will be captured during this step.</span></span>



~~~
Click **Next**.
~~~

10. <span data-ttu-id="41105-152">На странице **отчета об установке** можно просмотреть сведения о виртуализированном пакете приложения, который вы только что посвящены.</span><span class="sxs-lookup"><span data-stu-id="41105-152">On the **Installation Report** page, you can review information about the virtualized application package you have just sequenced.</span></span> <span data-ttu-id="41105-153">В **дополнительных сведениях**дважды щелкните событие, чтобы получить более подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="41105-153">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="41105-154">Чтобы продолжить, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-154">To proceed, click **Next**.</span></span>

11. <span data-ttu-id="41105-155">Откроется страница **настройки** .</span><span class="sxs-lookup"><span data-stu-id="41105-155">The **Customize** page is displayed.</span></span> <span data-ttu-id="41105-156">Если вы закончите установку и настройку виртуального приложения, нажмите кнопку **остановить сейчас** и перейдите к шагу 14 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="41105-156">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="41105-157">Чтобы выполнить любое из указанных ниже действий, нажмите кнопку **настроить**.</span><span class="sxs-lookup"><span data-stu-id="41105-157">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="41105-158">Подготовьте виртуальный пакет для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="41105-158">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="41105-159">Потоковая передача повышает удобство работы с виртуальным пакетом приложения на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="41105-159">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="41105-160">Укажите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-160">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="41105-161">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-161">Click **Next**.</span></span>

12. <span data-ttu-id="41105-162">На странице **потоковой передачи** запустите каждую программу, чтобы ее можно было оптимизировать и эффективно работать на конечных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="41105-162">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="41105-163">Выполнение всех приложений может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="41105-163">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="41105-164">После запуска всех приложений закройте все приложения и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-164">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="41105-165">Если вы не откроете какие-либо приложения на этом этапе, потоковая передача по умолчанию будет доставлять по запросу.</span><span class="sxs-lookup"><span data-stu-id="41105-165">If you do not open any applications during this step, the default streaming method is on-demand streaming delivery.</span></span> <span data-ttu-id="41105-166">Это означает, что приложения будут загружаться по битам, пока он не будет открыт, а затем, в зависимости от того, как настроена Фоновая загрузка, будет загружаться оставшаяся часть приложения.</span><span class="sxs-lookup"><span data-stu-id="41105-166">This means applications will be downloaded bit by bit until it can be opened, and then depending on how the background loading is configured, will load the rest of the application.</span></span>



13. <span data-ttu-id="41105-167">На странице **Целевая операционная** система укажите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-167">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="41105-168">Чтобы разрешить запуск этого пакета для всех поддерживаемых операционных систем в среде, установите флажок **Разрешить запуск этого пакета в любой операционной системе**.</span><span class="sxs-lookup"><span data-stu-id="41105-168">To allow all supported operating systems in your environment to run this package, select **Allow this package to run on any operating system**.</span></span> <span data-ttu-id="41105-169">Чтобы настроить выполнение этого пакета только в определенных операционных системах, установите флажок **Разрешить запуск этого пакета только в указанных ниже операционных системах** и выберите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-169">To configure this package to run only on specific operating systems, select **Allow this package to run only on the following operating systems** and select the operating systems that can run this package.</span></span> <span data-ttu-id="41105-170">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-170">Click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="41105-171">Убедитесь в том, что указанные здесь операционные системы поддерживаются в приложении, которое вы используете в качестве последовательности.</span><span class="sxs-lookup"><span data-stu-id="41105-171">Make sure that the operating systems you specify here are supported by the application you are sequencing.</span></span>



14. <span data-ttu-id="41105-172">Откроется страница " **Создание пакета** ".</span><span class="sxs-lookup"><span data-stu-id="41105-172">The **Create Package** page is displayed.</span></span> <span data-ttu-id="41105-173">Чтобы изменить пакет, не сохраняя его, нажмите кнопку **продолжить, чтобы изменить пакет без сохранения с помощью редактора пакетов**.</span><span class="sxs-lookup"><span data-stu-id="41105-173">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="41105-174">Этот параметр открывает пакет на консоли секвенсор, чтобы можно было изменить пакет перед сохранением.</span><span class="sxs-lookup"><span data-stu-id="41105-174">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="41105-175">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-175">Click **Next**.</span></span>

   <span data-ttu-id="41105-176">Чтобы сохранить пакет немедленно, выберите **сохранить пакет** (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="41105-176">To save the package immediately, select **Save the package now** (default).</span></span> <span data-ttu-id="41105-177">Добавьте **Комментарии** , которые должны быть связаны с пакетом.</span><span class="sxs-lookup"><span data-stu-id="41105-177">Add optional **Comments** to be associated with the package.</span></span> <span data-ttu-id="41105-178">Комментарии полезны для определения версии программы и другой информации о пакете.</span><span class="sxs-lookup"><span data-stu-id="41105-178">Comments are useful for identifying the program version and other information about the package.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="41105-179">Система не поддерживает непечатаемые символы в **комментариях** и **описаниях**.</span><span class="sxs-lookup"><span data-stu-id="41105-179">The system does not support non-printable characters in **Comments** and **Descriptions**.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. <span data-ttu-id="41105-180">Откроется страница **завершения** .</span><span class="sxs-lookup"><span data-stu-id="41105-180">The **Completion** page is displayed.</span></span> <span data-ttu-id="41105-181">При необходимости просмотрите сведения в области **отчета о пакетах виртуальных приложений** и нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="41105-181">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="41105-182">Эти сведения также доступны в файле **Report.xml** , который находится в каталоге, в котором был создан пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-182">This information is also available in the **Report.xml** file that is located in the directory where the package was created.</span></span>

   <span data-ttu-id="41105-183">Пакет теперь доступен в секвенсоре.</span><span class="sxs-lookup"><span data-stu-id="41105-183">The package is now available in the sequencer.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="41105-184">После того как вы успешно создадите виртуальный пакет приложения, вы не сможете запустить виртуальный пакет приложения на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="41105-184">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



**<span data-ttu-id="41105-185">Упорядочение надстройки или внешнего приложения</span><span class="sxs-lookup"><span data-stu-id="41105-185">To sequence an add-on or plug-in application</span></span>**

1. > [!NOTE]  
   > <span data-ttu-id="41105-186">Перед выполнением описанной ниже процедуры установите родительское приложение локально на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="41105-186">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="41105-187">Или, если у вас есть виртуализированное родительское приложение, вы можете выполнить действия, описанные в рабочем процессе надстройки или плагина, чтобы распаковать родительское приложение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="41105-187">Or if you have the parent application virtualized, you can follow the steps in the add-on or plug-in workflow to unpack the parent application on the computer.</span></span>
   >
   > <span data-ttu-id="41105-188">Например, если вы подключаете плагин для Microsoft Excel, установите Microsoft Excel локально на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="41105-188">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="41105-189">Также установите родительское приложение в том же каталоге, где установлен приложение на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="41105-189">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="41105-190">Если плагин или надстройка будут использоваться с существующим пакетом виртуального приложения, установите приложение на тот же виртуальный диск, который использовался при создании родительского пакета виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="41105-190">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="41105-191">\*<strong><em>В секвенсоре щелкните \* </em> создать новый виртуальный пакет приложения </strong> .</span><span class="sxs-lookup"><span data-stu-id="41105-191">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="41105-192">Выберите команду **создать пакет (по умолчанию)**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-192">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="41105-193">На странице **Подготовка компьютера** изучите проблемы, которые могут привести к сбою при создании пакета или привести к тому, что пакет может содержать ненужные данные.</span><span class="sxs-lookup"><span data-stu-id="41105-193">On the **Prepare Computer** page, review the issues that might cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="41105-194">Прежде чем продолжить, устраните все возможные проблемы.</span><span class="sxs-lookup"><span data-stu-id="41105-194">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="41105-195">После внесения исправлений нажмите кнопку **Обновить** , чтобы отобразить обновленные сведения.</span><span class="sxs-lookup"><span data-stu-id="41105-195">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="41105-196">После устранения всех возможных проблем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-196">After you have resolved all potential issues, click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="41105-197">Если вы хотите отключить антивирусную программу, необходимо сначала проверить компьютер, на котором работает секвенсор, чтобы убедиться в том, что нежелательные или вредоносные файлы не могут быть добавлены в пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-197">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4. <span data-ttu-id="41105-198">На странице " **Тип приложения** " выберите **надстройку или плагин**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-198">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="41105-199">На странице " **Выбор установщика** " нажмите кнопку **Обзор** и укажите установочный файл для надстройки или плагина.</span><span class="sxs-lookup"><span data-stu-id="41105-199">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="41105-200">Если у надстройки нет связанного файла установщика и вы планируете выполнить все инструкции по установке вручную, установите флажок **выбрать этот параметр, чтобы выполнить выборочную установку** , и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-200">If the add-on or plug-in does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="41105-201">На **главной странице установки** убедитесь, что на компьютере, на котором запущена программа Sequencer, установлено основное приложение.</span><span class="sxs-lookup"><span data-stu-id="41105-201">On the **Install Primary** page, ensure that the primary application is installed on the computer that runs the sequencer.</span></span> <span data-ttu-id="41105-202">Кроме того, вы можете расширить существующий пакет, сохраненный локально на компьютере, на котором работает секвенсор.</span><span class="sxs-lookup"><span data-stu-id="41105-202">Alternatively, you can expand an existing package that has been saved locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="41105-203">Для этого щелкните **развернуть пакет**и выберите пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-203">To do this, click **Expand Package**, and then select the package.</span></span> <span data-ttu-id="41105-204">После развертывания или установки родительской программы установите флажок **я установил основную родительскую программу**.</span><span class="sxs-lookup"><span data-stu-id="41105-204">After you have expanded or installed the parent program, select **I have installed the primary parent program**.</span></span>

   <span data-ttu-id="41105-205">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-205">Click **Next**.</span></span>

7. <span data-ttu-id="41105-206">На странице " **имя пакета** " введите имя, которое будет сопоставлено с пакетом.</span><span class="sxs-lookup"><span data-stu-id="41105-206">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="41105-207">Используйте имя, которое помогает идентифицировать цель и версию приложения, которые будут добавлены в пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-207">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="41105-208">Имя пакета будет отображаться в консоли управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="41105-208">The package name will be displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="41105-209">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-209">Click **Next**.</span></span>

8. <span data-ttu-id="41105-210">На странице **установки** , когда секвенсор и установщик приложения готовы, вы можете продолжить установку плагина или надстройки, чтобы программа Sequencer могла отслеживать процесс установки.</span><span class="sxs-lookup"><span data-stu-id="41105-210">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="41105-211">Используйте процесс установки приложения для выполнения установки.</span><span class="sxs-lookup"><span data-stu-id="41105-211">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="41105-212">Если в процессе установки необходимо запустить дополнительные файлы установки, нажмите кнопку **выполнить** , найдите и запустите дополнительные файлы установки.</span><span class="sxs-lookup"><span data-stu-id="41105-212">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="41105-213">Когда вы закончите установку, выберите параметр **Установка завершена**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-213">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="41105-214">На странице **отчета об установке** можно просмотреть сведения о пакете виртуального приложения, который вы только что посвящены.</span><span class="sxs-lookup"><span data-stu-id="41105-214">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="41105-215">Чтобы получить более подробное описание сведений, отображаемых в **дополнительных сведениях**, дважды щелкните событие.</span><span class="sxs-lookup"><span data-stu-id="41105-215">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="41105-216">После того как вы проверили данные, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-216">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="41105-217">Откроется страница **настройки** .</span><span class="sxs-lookup"><span data-stu-id="41105-217">The **Customize** page is displayed.</span></span> <span data-ttu-id="41105-218">Если вы закончите установку и настройку виртуального приложения, нажмите кнопку **остановить сейчас** и перейдите к шагу 12 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="41105-218">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 12 of this procedure.</span></span> <span data-ttu-id="41105-219">Чтобы выполнить любое из указанных ниже действий, нажмите кнопку **настроить**.</span><span class="sxs-lookup"><span data-stu-id="41105-219">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="41105-220">Оптимизируйте работу пакета в медленной или ненадежной сети.</span><span class="sxs-lookup"><span data-stu-id="41105-220">Optimize how the package will run across a slow or unreliable network.</span></span>

    -   <span data-ttu-id="41105-221">Укажите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-221">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="41105-222">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-222">Click **Next**.</span></span>

11. <span data-ttu-id="41105-223">На странице **потоковой передачи** запустите каждую программу, чтобы ее можно было оптимизировать и эффективно работать на конечных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="41105-223">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="41105-224">Потоковая передача повышает удобство работы с виртуальным пакетом приложений на конечных компьютерах в сетях с большим временем задержки.</span><span class="sxs-lookup"><span data-stu-id="41105-224">Streaming improves the experience when the virtual application package is run on target computers on high-latency networks.</span></span> <span data-ttu-id="41105-225">Выполнение всех приложений может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="41105-225">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="41105-226">После запуска всех приложений закройте каждое из них.</span><span class="sxs-lookup"><span data-stu-id="41105-226">After all applications have run, close each of the applications.</span></span> <span data-ttu-id="41105-227">Кроме того, вы можете настроить пакет так, чтобы он был полностью скачан перед открытием, выбрав флажок **заставлять приложения для загрузки** .</span><span class="sxs-lookup"><span data-stu-id="41105-227">You can also configure the package to be required to be fully downloaded before opening by selecting the **Force applications to be downloaded** check-box.</span></span> <span data-ttu-id="41105-228">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-228">Click **Next**.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="41105-229">При необходимости вы можете остановить загрузку приложения на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="41105-229">If necessary, you can stop an application from loading during this step.</span></span> <span data-ttu-id="41105-230">В диалоговом окне **Запуск приложения** нажмите кнопку **остановить** и установите один из флажков: **остановить все приложения** или **остановить только это приложение**.</span><span class="sxs-lookup"><span data-stu-id="41105-230">In the **Application Launch** dialog box, click **Stop** and select one of the check boxes: **Stop all applications** or **Stop this application only**.</span></span>



12. <span data-ttu-id="41105-231">На странице **Целевая операционная** система укажите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-231">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="41105-232">Чтобы разрешить запуск этого пакета для всех поддерживаемых операционных систем в вашей среде, установите флажок **Разрешить выполнение этого пакета для любой операционной системы** .</span><span class="sxs-lookup"><span data-stu-id="41105-232">To allow all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="41105-233">Чтобы настроить запуск этого пакета только в определенных операционных системах, установите флажок **Разрешить запуск этого пакета только на указанных ниже операционных системах** и выберите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-233">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="41105-234">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-234">Click **Next**.</span></span>

13. <span data-ttu-id="41105-235">Откроется страница " **Создание пакета** ".</span><span class="sxs-lookup"><span data-stu-id="41105-235">The **Create Package** page is displayed.</span></span> <span data-ttu-id="41105-236">Чтобы изменить пакет, не сохраняя его, установите флажок **продолжить изменение пакета без сохранения с помощью редактора пакетов** .</span><span class="sxs-lookup"><span data-stu-id="41105-236">To modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="41105-237">Этот параметр открывает пакет на консоли секвенсор, чтобы можно было изменить пакет перед сохранением.</span><span class="sxs-lookup"><span data-stu-id="41105-237">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="41105-238">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-238">Click **Next**.</span></span>

    <span data-ttu-id="41105-239">Чтобы сохранить пакет немедленно, выберите **сохранить пакет прямо сейчас**.</span><span class="sxs-lookup"><span data-stu-id="41105-239">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="41105-240">При необходимости добавьте **Описание** , которое будет сопоставлено с пакетом.</span><span class="sxs-lookup"><span data-stu-id="41105-240">Optionally, add a **Description** that will be associated with the package.</span></span> <span data-ttu-id="41105-241">Описания полезны для идентификации версии и других сведений о пакете.</span><span class="sxs-lookup"><span data-stu-id="41105-241">Descriptions are useful for identifying the version and other information about the package.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="41105-242">Система не поддерживает непечатаемые символы в комментариях и описаниях.</span><span class="sxs-lookup"><span data-stu-id="41105-242">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**<span data-ttu-id="41105-243">Упорядочение приложения по промежуточного слоя</span><span class="sxs-lookup"><span data-stu-id="41105-243">To sequence a middleware application</span></span>**

1. <span data-ttu-id="41105-244">На компьютере с программой Sequencer выберите **все программы**, а затем — **Виртуализация приложений**Microsoft, а затем выберите **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="41105-244">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="41105-245">\*<strong><em>В секвенсоре щелкните \* </em> создать новый виртуальный пакет приложения </strong> .</span><span class="sxs-lookup"><span data-stu-id="41105-245">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="41105-246">Выберите команду **создать пакет (по умолчанию)**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-246">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="41105-247">На странице **Подготовка компьютера** изучите проблемы, которые могут привести к сбою при создании пакета или привести к тому, что пакет может содержать ненужные данные.</span><span class="sxs-lookup"><span data-stu-id="41105-247">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="41105-248">Прежде чем продолжить, устраните все возможные проблемы.</span><span class="sxs-lookup"><span data-stu-id="41105-248">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="41105-249">После внесения исправлений нажмите кнопку **Обновить** , чтобы отобразить обновленные сведения.</span><span class="sxs-lookup"><span data-stu-id="41105-249">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="41105-250">После устранения всех возможных проблем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-250">After you have resolved all potential issues, click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="41105-251">Если вы хотите отключить антивирусную программу, необходимо сначала проверить компьютер, на котором работает секвенсор App-V 5,0, чтобы убедиться в том, что нежелательные или вредоносные файлы не могут быть добавлены в пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-251">If you are required to disable virus scanning software, you should first scan the computer that runs the App-V 5.0 Sequencer in order to ensure that no unwanted or malicious files can be added to the package.</span></span>



4. <span data-ttu-id="41105-252">На странице **Тип приложения** выберите **промежуточный**по, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-252">On the **Type of Application** page, select **Middleware**, and then click **Next**.</span></span>

5. <span data-ttu-id="41105-253">На странице " **Выбор установщика** " нажмите кнопку **Обзор** и укажите файл установки для приложения.</span><span class="sxs-lookup"><span data-stu-id="41105-253">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="41105-254">Если у приложения нет связанного файла установщика и вы планируете выполнить все инструкции по установке вручную, установите флажок **выбрать этот параметр, чтобы выполнить выборочную установку** , и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-254">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="41105-255">На странице " **имя пакета** " введите имя, которое будет сопоставлено с пакетом.</span><span class="sxs-lookup"><span data-stu-id="41105-255">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="41105-256">Используйте имя, которое помогает идентифицировать цель и версию приложения, которые будут добавлены в пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-256">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="41105-257">Имя пакета отобразится в консоли управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="41105-257">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="41105-258">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-258">Click **Next**.</span></span>

7. <span data-ttu-id="41105-259">На странице **установки** , когда программа Sequencer и установщик приложения по промежуточного слоя готовы, вы можете продолжить установку приложения, чтобы секвенсор мог отслеживать процесс установки.</span><span class="sxs-lookup"><span data-stu-id="41105-259">On the **Installation** page, when the sequencer and middleware application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="41105-260">Используйте процесс установки приложения для выполнения установки.</span><span class="sxs-lookup"><span data-stu-id="41105-260">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="41105-261">Если в процессе установки требуется выполнить дополнительные установочные файлы, нажмите кнопку **выполнить**, чтобы найти и запустить дополнительные файлы установки.</span><span class="sxs-lookup"><span data-stu-id="41105-261">If additional installation files must be run as part of the installation, click **Run**, to locate and run the additional installation files.</span></span> <span data-ttu-id="41105-262">После завершения установки установите флажок **Установка завершена** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-262">When you are finished with the installation, select the **I am finished installing** check box, and then click **Next**.</span></span>

8. <span data-ttu-id="41105-263">На странице **установки** подождите, пока секвенсор настроит пакет виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="41105-263">On the **Installation** page, wait while the sequencer configures the virtual application package.</span></span>

9. <span data-ttu-id="41105-264">На странице **отчета об установке** можно просмотреть сведения о пакете виртуального приложения, который был только что упорядочен.</span><span class="sxs-lookup"><span data-stu-id="41105-264">On the **Installation Report** page, you can review information about the virtual application package that you have just sequenced.</span></span> <span data-ttu-id="41105-265">В **дополнительных сведениях**дважды щелкните событие, чтобы получить более подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="41105-265">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="41105-266">Чтобы продолжить, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-266">To proceed, click **Next**.</span></span>

10. <span data-ttu-id="41105-267">На странице **Целевая операционная** система укажите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-267">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="41105-268">Чтобы включить этот пакет для всех поддерживаемых операционных систем в среде, установите флажок **Разрешить выполнение этого пакета для любой операционной системы** .</span><span class="sxs-lookup"><span data-stu-id="41105-268">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="41105-269">Чтобы настроить запуск этого пакета только в определенных операционных системах, установите флажок **Разрешить запуск этого пакета только на указанных ниже операционных системах** и выберите операционные системы, которые могут запускать этот пакет.</span><span class="sxs-lookup"><span data-stu-id="41105-269">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box and select the operating systems that can run this package.</span></span> <span data-ttu-id="41105-270">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-270">Click **Next**.</span></span>

11. <span data-ttu-id="41105-271">Откроется страница **Создание пакета** .</span><span class="sxs-lookup"><span data-stu-id="41105-271">On the **Create Package** page is displayed.</span></span> <span data-ttu-id="41105-272">Чтобы изменить пакет, не сохраняя его, нажмите кнопку **продолжить, чтобы изменить пакет без сохранения с помощью редактора пакетов**.</span><span class="sxs-lookup"><span data-stu-id="41105-272">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="41105-273">Этот параметр открывает пакет на консоли секвенсор, чтобы можно было изменить пакет перед сохранением.</span><span class="sxs-lookup"><span data-stu-id="41105-273">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="41105-274">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41105-274">Click **Next**.</span></span>

    <span data-ttu-id="41105-275">Чтобы сохранить пакет немедленно, выберите **сохранить пакет прямо сейчас**.</span><span class="sxs-lookup"><span data-stu-id="41105-275">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="41105-276">При необходимости добавьте **Описание** , которое должно быть связано с пакетом.</span><span class="sxs-lookup"><span data-stu-id="41105-276">Optionally, add a **Description** to be associated with the package.</span></span> <span data-ttu-id="41105-277">Описания полезны для идентификации версии программы и других сведений о пакете.</span><span class="sxs-lookup"><span data-stu-id="41105-277">Descriptions are useful for identifying the program version and other information about the package.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="41105-278">Система не поддерживает непечатаемые символы в комментариях и описаниях.</span><span class="sxs-lookup"><span data-stu-id="41105-278">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. <span data-ttu-id="41105-279">Откроется страница **завершения** .</span><span class="sxs-lookup"><span data-stu-id="41105-279">The **Completion** page is displayed.</span></span> <span data-ttu-id="41105-280">При необходимости просмотрите сведения в области **отчета о пакетах виртуальных приложений** и нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="41105-280">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="41105-281">Эти сведения также доступны в файле **Report.xml** , который находится в каталоге, указанном в действии 11 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="41105-281">This information is also available in the **Report.xml** file that is located in the directory specified in step 11 of this procedure.</span></span>

   <span data-ttu-id="41105-282">Пакет теперь доступен в секвенсоре.</span><span class="sxs-lookup"><span data-stu-id="41105-282">The package is now available in the sequencer.</span></span> <span data-ttu-id="41105-283">Чтобы изменить свойства пакета, нажмите **изменить \ [имя пакета \]**.</span><span class="sxs-lookup"><span data-stu-id="41105-283">To edit the package properties, click **Edit \[Package Name\]**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="41105-284">После того как вы успешно создадите виртуальный пакет приложения, вы не сможете запустить виртуальный пакет приложения на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="41105-284">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="41105-285">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="41105-285">Related topics</span></span>


[<span data-ttu-id="41105-286">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="41105-286">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









