---
title: Установка баз данных управления и отчетности отдельно от служб управления и отчетности
description: Установка баз данных управления и отчетности отдельно от служб управления и отчетности
author: dansimp
ms.assetid: 02afd6d6-4c33-4c0b-bd88-ae167b786fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1522045fced411164ac4fd36af41d46ab61ad6f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814024"
---
# <span data-ttu-id="d3b23-103">Установка баз данных управления и отчетности отдельно от служб управления и отчетности</span><span class="sxs-lookup"><span data-stu-id="d3b23-103">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>


<span data-ttu-id="d3b23-104">Чтобы установить сервер баз данных и сервер управления на разных компьютерах, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d3b23-104">Use the following procedure to install the database server and management server on different computers.</span></span> <span data-ttu-id="d3b23-105">На компьютере, на котором вы планируете установить сервер базы данных, должна быть установлена поддерживаемая версия Microsoft SQL, или установка завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="d3b23-105">The computer you plan to install the database server on must be running a supported version of Microsoft SQL or the installation will fail.</span></span>

**<span data-ttu-id="d3b23-106">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d3b23-106">Note</span></span>**  
<span data-ttu-id="d3b23-107">После того как вы закончите развертывание, администратору, устанавливающему службу для подключения к этим базам данных, потребуется имя **сервера Microsoft SQL Server**, **имя экземпляра** и **имя базы данных** .</span><span class="sxs-lookup"><span data-stu-id="d3b23-107">After you complete the deployment, the **Microsoft SQL Server name**, **instance name** and **database name** will be required by the administrator installing the service to be able to connect to these databases.</span></span>



**<span data-ttu-id="d3b23-108">Установка базы данных управления и сервера управления на разных компьютерах</span><span class="sxs-lookup"><span data-stu-id="d3b23-108">To install the management database and the management server on separate computers</span></span>**

1.  <span data-ttu-id="d3b23-109">Скопируйте файлы установки сервера App-V 5,0 на компьютер, на котором вы хотите установить его.</span><span class="sxs-lookup"><span data-stu-id="d3b23-109">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="d3b23-110">Чтобы запустить установку App-V 5,0 Server, щелкните правой кнопкой мыши и запустите **appv\_server\_setup.exe** с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="d3b23-110">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="d3b23-111">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-111">Click **Install**.</span></span>

2.  <span data-ttu-id="d3b23-112">На странице **Приступая к работе** проверьте и принимайте условия лицензии и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-112">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="d3b23-113">На странице **Использование центра обновления Майкрософт, чтобы обеспечить безопасность и актуальность** данных на компьютере, чтобы включить обновления Майкрософт, установите флажок **использовать Microsoft Update при проверке обновлений (рекомендуется).**</span><span class="sxs-lookup"><span data-stu-id="d3b23-113">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="d3b23-114">Чтобы отключить обновления Майкрософт, выберите **я не хочу использовать Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-114">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="d3b23-115">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-115">Click **Next**.</span></span>

4.  <span data-ttu-id="d3b23-116">На странице **Выбор** компонентов выберите компоненты, которые вы хотите установить, установив флажок **база данных сервера управления** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-116">On the **Feature Selection** page, select the components you want to install by selecting the **Management Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="d3b23-117">На странице **расположение для установки** подтвердите расположение по умолчанию и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-117">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="d3b23-118">На начальной **странице Создание базы данных нового сервера управления**при необходимости подтвердите параметры по умолчанию, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-118">On the initial **Create New Management Server Database page**, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="d3b23-119">Если вы используете настраиваемый экземпляр SQL Server, выберите **использовать настраиваемый экземпляр** и введите имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d3b23-119">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="d3b23-120">Если вы используете настраиваемое имя базы данных, выберите пункт **Настраиваемая конфигурация** и введите имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d3b23-120">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="d3b23-121">На следующей странице **Создание базы данных нового сервера управления** выберите **использовать удаленный компьютер**и введите учетную запись удаленного компьютера в следующем формате: **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-121">On the next **Create New Management Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="d3b23-122">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d3b23-122">Note</span></span>**  
    <span data-ttu-id="d3b23-123">Если вы планируете развернуть сервер управления на том же компьютере, необходимо выбрать параметр **использовать этот локальный компьютер**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-123">If you plan to deploy the management server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the management server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="d3b23-124">Чтобы начать установку, нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-124">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="d3b23-125">Установка базы данных отчетов и сервера отчетов на разных компьютерах</span><span class="sxs-lookup"><span data-stu-id="d3b23-125">To install the reporting database and the reporting server on separate computers</span></span>**

1.  <span data-ttu-id="d3b23-126">Скопируйте файлы установки сервера App-V 5,0 на компьютер, на котором вы хотите установить его.</span><span class="sxs-lookup"><span data-stu-id="d3b23-126">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="d3b23-127">Чтобы запустить установку App-V 5,0 Server, щелкните правой кнопкой мыши и запустите **appv\_server\_setup.exe** с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="d3b23-127">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="d3b23-128">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-128">Click **Install**.</span></span>

2.  <span data-ttu-id="d3b23-129">На странице **Приступая к работе** проверьте и принимайте условия лицензии и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-129">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="d3b23-130">На странице **Использование центра обновления Майкрософт, чтобы обеспечить безопасность и актуальность** данных на компьютере, чтобы включить обновления Майкрософт, установите флажок **использовать Microsoft Update при проверке обновлений (рекомендуется).**</span><span class="sxs-lookup"><span data-stu-id="d3b23-130">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="d3b23-131">Чтобы отключить обновления Майкрософт, выберите **я не хочу использовать Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-131">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="d3b23-132">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-132">Click **Next**.</span></span>

4.  <span data-ttu-id="d3b23-133">На странице **Выбор** компонентов выберите компоненты, которые вы хотите установить, установив флажок **база данных сервера отчетов** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-133">On the **Feature Selection** page, select the components you want to install by selecting the **Reporting Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="d3b23-134">На странице **расположение для установки** подтвердите расположение по умолчанию и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-134">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="d3b23-135">На начальной странице **Создание базы данных сервера отчетов** при необходимости подтвердите параметры по умолчанию, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-135">On the initial **Create New Reporting Server Database** page, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="d3b23-136">Если вы используете настраиваемый экземпляр SQL Server, выберите **использовать настраиваемый экземпляр** и введите имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d3b23-136">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="d3b23-137">Если вы используете настраиваемое имя базы данных, выберите пункт **Настраиваемая конфигурация** и введите имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d3b23-137">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="d3b23-138">На следующей странице **Создание базы данных сервера отчетов** выберите **Использование удаленного компьютера**и введите учетную запись удаленного компьютера, используя следующий формат: **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-138">On the next **Create New Reporting Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="d3b23-139">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d3b23-139">Note</span></span>**  
    <span data-ttu-id="d3b23-140">Если вы планируете развернуть сервер отчетов на том же компьютере, необходимо выбрать параметр **использовать этот локальный компьютер**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-140">If you plan to deploy the reporting server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the reporting server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="d3b23-141">Чтобы начать установку, нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-141">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="d3b23-142">Установка баз данных управления и отчетов с помощью сценариев баз данных App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="d3b23-142">To install the management and reporting databases using App-V 5.0 database scripts</span></span>**

1.  <span data-ttu-id="d3b23-143">Скопируйте файлы установки сервера App-V 5,0 на компьютер, на котором вы хотите установить его.</span><span class="sxs-lookup"><span data-stu-id="d3b23-143">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span>

2.  <span data-ttu-id="d3b23-144">Чтобы извлечь сценарии базы данных App-V 5,0, откройте командную строке и укажите расположение для сохранения файлов установки и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d3b23-144">To extract the App-V 5.0 database scripts, open a command prompt and specify the location where the installation files are saved and run the following command:</span></span>

    <span data-ttu-id="d3b23-145">**appv\_server\_setup.exe** **/Layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-145">**appv\_server\_setup.exe** **/LAYOUT** **/LAYOUTDIR=”InstallationExtractionLocation”**.</span></span>

3.  <span data-ttu-id="d3b23-146">Чтобы получить доступ к сценариям баз данных App-V 5,0 и инструкции в файле readme, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d3b23-146">After the extraction has been completed, to access the App-V 5.0 database scripts and instructions readme file:</span></span>

    -   <span data-ttu-id="d3b23-147">Сценарии базы данных управления App-V 5,0 и инструкции в файле readme находятся в следующей папке: **InstallationExtractionLocation**базы данных  \\  **управления сценариями базы данных**  \\  **Management Database**.</span><span class="sxs-lookup"><span data-stu-id="d3b23-147">The App-V 5.0 Management Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Management Database**.</span></span>

    -   <span data-ttu-id="d3b23-148">Сценарии баз данных и инструкции для отчетов приложения App-V 5,0 находятся в следующей папке: **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Создание отчетов о**сценариях баз данных.</span><span class="sxs-lookup"><span data-stu-id="d3b23-148">The App-V 5.0 Reporting Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Reporting Database**.</span></span>

4.  <span data-ttu-id="d3b23-149">Для каждой базы данных скопируйте сценарии в общий доступ и измените их, следуя инструкциям в файле readme.</span><span class="sxs-lookup"><span data-stu-id="d3b23-149">For each database, copy the scripts to a share and modify them following the instructions in the readme file.</span></span>

    **<span data-ttu-id="d3b23-150">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d3b23-150">Note</span></span>**  
    <span data-ttu-id="d3b23-151">Дополнительные сведения об изменении необходимых SID, содержащихся в сценариях, можно найти в разделе [Установка баз данных App-V и преобразование сопоставленных идентификаторов безопасности с помощью PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="d3b23-151">For more information about modifying the required SIDs contained in the scripts see, [How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span></span>



5.  <span data-ttu-id="d3b23-152">Запустите сценарии на компьютере с Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d3b23-152">Run the scripts on the computer running Microsoft SQL Server.</span></span>

    <span data-ttu-id="d3b23-153">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="d3b23-153">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="d3b23-154">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="d3b23-154">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="d3b23-155">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="d3b23-155">Got an App-V issue?</span></span>** <span data-ttu-id="d3b23-156">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="d3b23-156">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="d3b23-157">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d3b23-157">Related topics</span></span>


[<span data-ttu-id="d3b23-158">Развертывание App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="d3b23-158">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)









