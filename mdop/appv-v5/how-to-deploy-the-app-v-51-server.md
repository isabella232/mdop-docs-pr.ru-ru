---
title: Порядок развертывания сервера App-V 5.1
description: Порядок развертывания сервера App-V 5.1
author: dansimp
ms.assetid: 4729beda-b98f-481b-ae74-ad71c59b1d69
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a367be7db4cea1835124657dbdfa3375474228e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814133"
---
# <span data-ttu-id="83bae-103">Порядок развертывания сервера App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="83bae-103">How to Deploy the App-V 5.1 Server</span></span>


<span data-ttu-id="83bae-104">Чтобы установить сервер Microsoft Application Virtualization (App-V) 5,1, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="83bae-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 server.</span></span> <span data-ttu-id="83bae-105">Сведения о развертывании сервера App-V 5,1 можно найти в разделе [о приложении App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51).</span><span class="sxs-lookup"><span data-stu-id="83bae-105">For information about deploying the App-V 5.1 Server, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51).</span></span>

**<span data-ttu-id="83bae-106">Прежде чем начать, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="83bae-106">Before you start:</span></span>**

-   <span data-ttu-id="83bae-107">Убедитесь, что вы установили необходимое программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="83bae-107">Ensure that you’ve installed prerequisite software.</span></span> <span data-ttu-id="83bae-108">Ознакомьтесь [с требованиями для App-V 5,1](app-v-51-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="83bae-108">See [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

-   <span data-ttu-id="83bae-109">Ознакомьтесь с разделом "сервер" в разделе "безопасность" для [App-V 5,1](app-v-51-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="83bae-109">Review the server section of [App-V 5.1 Security Considerations](app-v-51-security-considerations.md).</span></span>

-   <span data-ttu-id="83bae-110">Укажите порт, на котором будет размещен каждый из компонентов.</span><span class="sxs-lookup"><span data-stu-id="83bae-110">Specify a port where each component will be hosted.</span></span>

-   <span data-ttu-id="83bae-111">Добавьте правила брандмауэра, разрешающие входящим запросам доступ к указанным портам.</span><span class="sxs-lookup"><span data-stu-id="83bae-111">Add firewall rules to allow incoming requests to access the specified ports.</span></span>

-   <span data-ttu-id="83bae-112">Если вы используете скрипты SQL вместо установщика Windows, чтобы настроить базу данных управления или базу данных отчетов, необходимо выполнить сценарии SQL перед установкой сервера управления или сервера отчетов.</span><span class="sxs-lookup"><span data-stu-id="83bae-112">If you use SQL scripts, instead of the Windows Installer, to set up the Management database or Reporting database, you must run the SQL scripts before installing the Management Server or Reporting Server.</span></span> <span data-ttu-id="83bae-113">Узнайте, [как развертывать базы данных App-V с помощью сценариев SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span><span class="sxs-lookup"><span data-stu-id="83bae-113">See [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span></span>

**<span data-ttu-id="83bae-114">Установка сервера App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="83bae-114">To install the App-V 5.1 server</span></span>**

1. <span data-ttu-id="83bae-115">Скопируйте файлы установки сервера App-V 5,1 на компьютер, на котором вы хотите установить его.</span><span class="sxs-lookup"><span data-stu-id="83bae-115">Copy the App-V 5.1 server installation files to the computer on which you want to install it.</span></span>

2. <span data-ttu-id="83bae-116">Запустите установку сервера App-V 5,1, щелкнув правой кнопкой мыши **appv\_server\_setup.exe** с помощью учетной записи администратора, а затем выберите команду **установить**.</span><span class="sxs-lookup"><span data-stu-id="83bae-116">Start the App-V 5.1 server installation by right-clicking and running **appv\_server\_setup.exe** as an administrator, and then click **Install**.</span></span>

3. <span data-ttu-id="83bae-117">Проверьте и приняв условия лицензионного соглашения и выберите, нужно ли включать обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="83bae-117">Review and accept the license terms, and choose whether to enable Microsoft updates.</span></span>

4. <span data-ttu-id="83bae-118">На странице **Выбор компонентов** выберите все следующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="83bae-118">On the **Feature Selection** page, select all of the following components.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="83bae-119">Компонент</span><span class="sxs-lookup"><span data-stu-id="83bae-119">Component</span></span></th>
   <th align="left"><span data-ttu-id="83bae-120">Описание</span><span class="sxs-lookup"><span data-stu-id="83bae-120">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="83bae-121">Сервер управления</span><span class="sxs-lookup"><span data-stu-id="83bae-121">Management server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="83bae-122">Предоставляет общую функциональность управления для инфраструктуры App-V.</span><span class="sxs-lookup"><span data-stu-id="83bae-122">Provides overall management functionality for the App-V infrastructure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="83bae-123">База данных управления</span><span class="sxs-lookup"><span data-stu-id="83bae-123">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="83bae-124">Упрощает предварительное развертывание баз данных для управления App-V.</span><span class="sxs-lookup"><span data-stu-id="83bae-124">Facilitates database predeployments for App-V management.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="83bae-125">Сервер публикаций</span><span class="sxs-lookup"><span data-stu-id="83bae-125">Publishing server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="83bae-126">Обеспечивает функции размещения и потоковой передачи для виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="83bae-126">Provides hosting and streaming functionality for virtual applications.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="83bae-127">Сервер отчетов</span><span class="sxs-lookup"><span data-stu-id="83bae-127">Reporting server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="83bae-128">Предоставляет службы отчетов App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="83bae-128">Provides App-V 5.1 reporting services.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="83bae-129">База данных отчетов</span><span class="sxs-lookup"><span data-stu-id="83bae-129">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="83bae-130">Упрощает предварительное развертывание баз данных для отчетов App-V.</span><span class="sxs-lookup"><span data-stu-id="83bae-130">Facilitates database predeployments for App-V reporting.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

5. <span data-ttu-id="83bae-131">На странице **Расположение установки** выберите расположение по умолчанию, в котором будут установлены выбранные компоненты, или измените его расположение, указав новый путь в строке **расположения установки** .</span><span class="sxs-lookup"><span data-stu-id="83bae-131">On the **Installation Location** page, accept the default location where the selected components will be installed, or change the location by typing a new path on the **Installation Location** line.</span></span>

6. <span data-ttu-id="83bae-132">На начальной странице **Создание новой базы данных для управления** настройте **экземпляр Microsoft SQL Server** и **базу данных сервера управления** , выбрав соответствующие параметры ниже.</span><span class="sxs-lookup"><span data-stu-id="83bae-132">On the initial **Create New Management Database** page, configure the **Microsoft SQL Server instance** and **Management Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="83bae-133">Метод</span><span class="sxs-lookup"><span data-stu-id="83bae-133">Method</span></span></th>
   <th align="left"><span data-ttu-id="83bae-134">Что вам нужно сделать?</span><span class="sxs-lookup"><span data-stu-id="83bae-134">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="83bae-135">Вы используете настраиваемый экземпляр Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="83bae-135">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="83bae-136">Выберите <strong> использовать настраиваемый экземпляр </strong> и введите имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="83bae-136">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="83bae-137">Используйте формат <strong> instanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="83bae-137">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="83bae-138">Предполагается, что путь установлен на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="83bae-138">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="83bae-139">Не поддерживается: имя сервера с использованием <strong> </strong> &lt; строгого экземпляра формата &gt; ServerName </strong> .</span><span class="sxs-lookup"><span data-stu-id="83bae-139">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="83bae-140">Вы используете настраиваемое имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="83bae-140">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="83bae-141">Выберите пункт <strong> Настраиваемая конфигурация </strong> и введите имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="83bae-141">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="83bae-142">Имя базы данных должно быть уникальным, иначе установка завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="83bae-142">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="83bae-143">На странице **Настройка** подтвердите значение по умолчанию, **используя этот локальный компьютер**.</span><span class="sxs-lookup"><span data-stu-id="83bae-143">On the **Configure** page, accept the default value **Use this local computer**.</span></span>

   **<span data-ttu-id="83bae-144">Примечание.</span><span class="sxs-lookup"><span data-stu-id="83bae-144">Note</span></span>**  
   <span data-ttu-id="83bae-145">Если вы устанавливаете сервер управления и базу данных управления рядом, некоторые параметры на этой странице недоступны.</span><span class="sxs-lookup"><span data-stu-id="83bae-145">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="83bae-146">В этом случае соответствующие параметры выбраны по умолчанию и не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="83bae-146">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

8. <span data-ttu-id="83bae-147">На начальной странице **Создание новой базы данных отчетов** настройте **экземпляр Microsoft SQL Server** и **базу данных сервера отчетов** , выбрав соответствующие параметры ниже.</span><span class="sxs-lookup"><span data-stu-id="83bae-147">On the initial **Create New Reporting Database** page, configure the **Microsoft SQL Server instance** and **Reporting Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="83bae-148">Метод</span><span class="sxs-lookup"><span data-stu-id="83bae-148">Method</span></span></th>
   <th align="left"><span data-ttu-id="83bae-149">Что вам нужно сделать?</span><span class="sxs-lookup"><span data-stu-id="83bae-149">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="83bae-150">Вы используете настраиваемый экземпляр Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="83bae-150">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="83bae-151">Выберите <strong> использовать настраиваемый экземпляр </strong> и введите имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="83bae-151">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="83bae-152">Используйте формат <strong> instanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="83bae-152">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="83bae-153">Предполагается, что путь установлен на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="83bae-153">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="83bae-154">Не поддерживается: имя сервера с использованием <strong> </strong> &lt; строгого экземпляра формата &gt; ServerName </strong> .</span><span class="sxs-lookup"><span data-stu-id="83bae-154">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="83bae-155">Вы используете настраиваемое имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="83bae-155">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="83bae-156">Выберите пункт <strong> Настраиваемая конфигурация </strong> и введите имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="83bae-156">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="83bae-157">Имя базы данных должно быть уникальным, иначе установка завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="83bae-157">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

9. <span data-ttu-id="83bae-158">На странице **Настройка** подтвердите значение по умолчанию: **Используйте этот локальный компьютер**.</span><span class="sxs-lookup"><span data-stu-id="83bae-158">On the **Configure** page, accept the default value: **Use this local computer**.</span></span>

   **<span data-ttu-id="83bae-159">Примечание.</span><span class="sxs-lookup"><span data-stu-id="83bae-159">Note</span></span>**  
   <span data-ttu-id="83bae-160">Если вы устанавливаете сервер управления и базу данных управления рядом, некоторые параметры на этой странице недоступны.</span><span class="sxs-lookup"><span data-stu-id="83bae-160">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="83bae-161">В этом случае соответствующие параметры выбраны по умолчанию и не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="83bae-161">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

10. <span data-ttu-id="83bae-162">На странице **Configure** (Настройка сервера управления) укажите следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="83bae-162">On the **Configure** (Management Server Configuration) page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="83bae-163">Элемент для настройки</span><span class="sxs-lookup"><span data-stu-id="83bae-163">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="83bae-164">Описание и примеры</span><span class="sxs-lookup"><span data-stu-id="83bae-164">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="83bae-165">Введите РЕКЛАМную группу с достаточными разрешениями для управления средой App-V.</span><span class="sxs-lookup"><span data-stu-id="83bae-165">Type the AD group with sufficient permissions to manage the App-V environment.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="83bae-166">Пример: MyDomain\MyUser</span><span class="sxs-lookup"><span data-stu-id="83bae-166">Example: MyDomain\MyUser</span></span></p>
    <p><span data-ttu-id="83bae-167">После установки вы можете добавить дополнительных пользователей или группы с помощью консоли управления.</span><span class="sxs-lookup"><span data-stu-id="83bae-167">After installation, you can add additional users or groups by using the Management console.</span></span> <span data-ttu-id="83bae-168">Однако глобальные группы безопасности и группы рассылки доменных служб Active Directory (AD DS) не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="83bae-168">However, global security groups and Active Directory Domain Services (AD DS) distribution groups are not supported.</span></span> <span data-ttu-id="83bae-169"><strong> </strong> <strong> Для выполнения этого действия необходимо использовать локальные или универсальные </strong> группы домена.</span><span class="sxs-lookup"><span data-stu-id="83bae-169">You must use <strong>Domain local</strong> or <strong>Universal</strong> groups are required to perform this action.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="83bae-170">Имя веб-сайта </strong> : укажите настраиваемое имя, которое будет использоваться для запуска службы публикации.</span><span class="sxs-lookup"><span data-stu-id="83bae-170">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="83bae-171">Если у вас нет настраиваемого имени, не вносите никаких изменений.</span><span class="sxs-lookup"><span data-stu-id="83bae-171">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="83bae-172">Привязка порта </strong> : укажите уникальный номер порта, который будет использоваться приложением App-V.</span><span class="sxs-lookup"><span data-stu-id="83bae-172">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="83bae-173">Пример: <strong> 12345</span><span class="sxs-lookup"><span data-stu-id="83bae-173">Example: <strong>12345</span></span></strong></p>
    <p><span data-ttu-id="83bae-174">Убедитесь, что указанный порт не используется другим веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="83bae-174">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

11. <span data-ttu-id="83bae-175">На странице **Настройка** **конфигурации сервера публикаций** укажите следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="83bae-175">On the **Configure** **Publishing Server Configuration** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="83bae-176">Элемент для настройки</span><span class="sxs-lookup"><span data-stu-id="83bae-176">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="83bae-177">Описание и примеры</span><span class="sxs-lookup"><span data-stu-id="83bae-177">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="83bae-178">Укажите URL-адрес для службы управления.</span><span class="sxs-lookup"><span data-stu-id="83bae-178">Specify the URL for the management service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="83bae-179">Образом<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span><span class="sxs-lookup"><span data-stu-id="83bae-179">Example: <a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span></span></a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="83bae-180">Имя веб-сайта </strong> : укажите настраиваемое имя, которое будет использоваться для запуска службы публикации.</span><span class="sxs-lookup"><span data-stu-id="83bae-180">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="83bae-181">Если у вас нет настраиваемого имени, не вносите никаких изменений.</span><span class="sxs-lookup"><span data-stu-id="83bae-181">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="83bae-182">Привязка порта </strong> : укажите уникальный номер порта, который будет использоваться приложением App-V.</span><span class="sxs-lookup"><span data-stu-id="83bae-182">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="83bae-183">Пример: 54321</span><span class="sxs-lookup"><span data-stu-id="83bae-183">Example: 54321</span></span></p>
    <p><span data-ttu-id="83bae-184">Убедитесь, что указанный порт не используется другим веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="83bae-184">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

12. <span data-ttu-id="83bae-185">На странице **сервера отчетов** укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="83bae-185">On the **Reporting Server** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="83bae-186">Элемент для настройки</span><span class="sxs-lookup"><span data-stu-id="83bae-186">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="83bae-187">Описание и примеры</span><span class="sxs-lookup"><span data-stu-id="83bae-187">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="83bae-188">Имя веб-сайта </strong> : укажите настраиваемое имя, которое будет использоваться для запуска службы отчетов.</span><span class="sxs-lookup"><span data-stu-id="83bae-188">Website name</strong>: Specify the custom name that will be used to run the Reporting Service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="83bae-189">Если у вас нет настраиваемого имени, не вносите никаких изменений.</span><span class="sxs-lookup"><span data-stu-id="83bae-189">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="83bae-190">Привязка порта </strong> : укажите уникальный номер порта, который будет использоваться приложением App-V.</span><span class="sxs-lookup"><span data-stu-id="83bae-190">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="83bae-191">Пример: 55555</span><span class="sxs-lookup"><span data-stu-id="83bae-191">Example: 55555</span></span></p>
    <p><span data-ttu-id="83bae-192">Убедитесь, что указанный порт не используется другим веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="83bae-192">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

13. <span data-ttu-id="83bae-193">Чтобы начать установку, на странице **готовности** нажмите кнопку **установить** , а затем нажмите кнопку **Закрыть** на **странице Готово** .</span><span class="sxs-lookup"><span data-stu-id="83bae-193">To start the installation, click **Install** on the **Ready** page, and then click **Close** on the **Finished** page.</span></span>

14. <span data-ttu-id="83bae-194">Чтобы убедиться, что настройка выполнена успешно, откройте веб-браузер и введите следующий URL-адрес:</span><span class="sxs-lookup"><span data-stu-id="83bae-194">To verify that the setup completed successfully, open a web browser, and type the following URL:</span></span>

    <span data-ttu-id="83bae-195">**http:// &lt; Имя компьютера сервера управления &gt; : &lt; номер порта службы управления &gt; или Console.html**.</span><span class="sxs-lookup"><span data-stu-id="83bae-195">**http://&lt;Management server machine name&gt;:&lt;Management service port number&gt;/Console.html**.</span></span>

    <span data-ttu-id="83bae-196">Пример: **http://localhost:12345/console.html** .</span><span class="sxs-lookup"><span data-stu-id="83bae-196">Example: **http://localhost:12345/console.html**.</span></span> <span data-ttu-id="83bae-197">Если установка прошла успешно, отображается консоль управления App-V без ошибок.</span><span class="sxs-lookup"><span data-stu-id="83bae-197">If the installation succeeded, the App-V Management console is displayed with no errors.</span></span>

    <span data-ttu-id="83bae-198">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="83bae-198">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="83bae-199">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="83bae-199">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="83bae-200">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="83bae-200">Got an App-V issue?</span></span>** <span data-ttu-id="83bae-201">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="83bae-201">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="83bae-202">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="83bae-202">Related topics</span></span>


[<span data-ttu-id="83bae-203">Развертывание App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="83bae-203">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="83bae-204">Установка баз данных управления и отчетности отдельно от служб управления и отчетности</span><span class="sxs-lookup"><span data-stu-id="83bae-204">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)

[<span data-ttu-id="83bae-205">Установка сервера публикации на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="83bae-205">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer51.md)

[<span data-ttu-id="83bae-206">Развертывание сервера App-V 5.1 с помощью сценария</span><span class="sxs-lookup"><span data-stu-id="83bae-206">How to Deploy the App-V 5.1 Server Using a Script</span></span>](how-to-deploy-the-app-v-51-server-using-a-script.md)

 

 





