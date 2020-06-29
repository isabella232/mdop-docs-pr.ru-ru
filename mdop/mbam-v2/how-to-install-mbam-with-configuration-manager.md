---
title: Порядок установки MBAM с помощью диспетчера конфигураций
description: Порядок установки MBAM с помощью диспетчера конфигураций
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825129"
---
# <span data-ttu-id="3b19c-103">Порядок установки MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="3b19c-103">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="3b19c-104">В этом разделе описаны действия, которые необходимо выполнить, чтобы установить MBAM с помощью Configuration Manager, используя рекомендованную конфигурацию, которая проиллюстрирована в разделе [Приступая к работе с помощью Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="3b19c-104">This section describes the steps to install MBAM with Configuration Manager by using the recommended configuration, which is illustrated in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="3b19c-105">Инструкции делятся на следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="3b19c-105">The steps are divided into the following tasks:</span></span>

-   <span data-ttu-id="3b19c-106">Установка и настройка MBAM на сервере Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="3b19c-106">Install and configure MBAM on the Configuration Manager Server</span></span>

-   <span data-ttu-id="3b19c-107">Установка баз данных восстановления и аудита на сервере</span><span class="sxs-lookup"><span data-stu-id="3b19c-107">Install the Recovery and Audit Databases on the Database Server</span></span>

-   <span data-ttu-id="3b19c-108">Установка функций сервера администрирования и мониторинга на сервере администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="3b19c-108">Install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>

<span data-ttu-id="3b19c-109">Прежде чем приступить к установке, убедитесь в том, что вы изменили или создали необходимые MOF-файлы.</span><span class="sxs-lookup"><span data-stu-id="3b19c-109">Before you begin the installation, ensure that you have edited or created the necessary mof files.</span></span> <span data-ttu-id="3b19c-110">Инструкции можно найти в разделе [Создание и редактирование MOF-файлов](how-to-create-or-edit-the-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="3b19c-110">For instructions, see [How to Create or Edit the mof Files](how-to-create-or-edit-the-mof-files.md).</span></span>

<span data-ttu-id="3b19c-111">**Важно!**  Если вы используете экземпляр служб SQL Server Reporting Services (SSRS), не используемый по умолчанию, необходимо запустить настройку MBAM, используя следующую командную строку, чтобы указать именованный экземпляр SSRS:</span><span class="sxs-lookup"><span data-stu-id="3b19c-111">**Important** If you are using a non-default SQL Server Reporting Services (SSRS) instance, you must start the MBAM Setup by using the following command line to specify the SSRS named instance:</span></span>

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**<span data-ttu-id="3b19c-112">Установка MBAM на сервере Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="3b19c-112">To install MBAM on the Configuration Manager Server</span></span>**

1.  <span data-ttu-id="3b19c-113">На сервере Configuration Manager выполните **MBAMSetup.exe** , чтобы запустить мастер установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="3b19c-113">On the Configuration Manager Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

    <span data-ttu-id="3b19c-114">**Примечание**  Чтобы получить файлы журнала установки, необходимо использовать пакет msiexec и параметр **/l** &lt; Location &gt; для установки Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3b19c-114">**Note** To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install Configuration Manager.</span></span> <span data-ttu-id="3b19c-115">Файлы журнала создаются в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="3b19c-115">Log files are created in the location that you specify.</span></span>

    <span data-ttu-id="3b19c-116">Дополнительные файлы журнала установки создаются в папке% Temp% на компьютере пользователя, устанавливающего Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3b19c-116">Additional setup log files are created in the %temp% folder on the computer of the user who is installing Configuration Manager.</span></span>

     

2.  <span data-ttu-id="3b19c-117">На странице **приветствия** при необходимости выберите **программу улучшения качества программного**обеспечения, а затем нажмите кнопку **начать**.</span><span class="sxs-lookup"><span data-stu-id="3b19c-117">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="3b19c-118">Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="3b19c-118">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="3b19c-119">На странице **Выбор топологии** выберите **Интеграция System Center Configuration Manager**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3b19c-119">On the **Topology Selection** page, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

5.  <span data-ttu-id="3b19c-120">На странице **выберите устанавливаемые компоненты** выберите **Интеграция System Center Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="3b19c-120">On the **Select features to install** page, select **System Center Configuration Manager Integration**.</span></span>

    <span data-ttu-id="3b19c-121">**Примечание**  На странице **Проверка готовности** нажмите кнопку **Далее** после того, как мастер установки проверит предварительные требования для установки и подтвердит, что ничего не найдено.</span><span class="sxs-lookup"><span data-stu-id="3b19c-121">**Note** On the **Checking Prerequisites** page, click **Next** after the installation wizard checks the prerequisites for your installation and confirms that none are missing.</span></span> <span data-ttu-id="3b19c-122">Если обнаружен отсутствующий предварительный компонент, необходимо устранить недостающие необходимые компоненты и нажать кнопку **проверить необходимые компоненты еще раз.**</span><span class="sxs-lookup"><span data-stu-id="3b19c-122">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again.**</span></span>

     

6.  <span data-ttu-id="3b19c-123">Укажите, следует ли использовать обновления Microsoft, чтобы обеспечить безопасность компьютера, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3b19c-123">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="3b19c-124">Использование обновлений Майкрософт не включает автоматические обновления в Windows.</span><span class="sxs-lookup"><span data-stu-id="3b19c-124">Using Microsoft Updates does not turn on Automatic Updates in Windows.</span></span>

7.  <span data-ttu-id="3b19c-125">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3b19c-125">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="3b19c-126">На странице **Сводка по установке** ознакомьтесь со списком компонентов, которые будут установлены, и нажмите кнопку **установить** , чтобы начать установку функций MBAM.</span><span class="sxs-lookup"><span data-stu-id="3b19c-126">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="3b19c-127">Нажмите кнопку " **назад** ", чтобы вернуться к мастеру, чтобы просмотреть или изменить параметры установки, или кнопку **"Отмена"** , чтобы выйти из программы установки.</span><span class="sxs-lookup"><span data-stu-id="3b19c-127">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="3b19c-128">Программа установки устанавливает функции MBAM и уведомляет о том, что установка завершена.</span><span class="sxs-lookup"><span data-stu-id="3b19c-128">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

9.  <span data-ttu-id="3b19c-129">Нажмите кнопку **Готово** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="3b19c-129">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="3b19c-130">Установка баз данных для восстановления и аудита на сервере</span><span class="sxs-lookup"><span data-stu-id="3b19c-130">To install the Recovery and Audit Databases on the Database Server</span></span>**

1.  <span data-ttu-id="3b19c-131">На сервере базы данных выполните **MBAMSetup.exe** , чтобы запустить мастер установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="3b19c-131">On the Database Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="3b19c-132">На странице **приветствия** при необходимости выберите **программу улучшения качества программного**обеспечения, а затем нажмите кнопку **начать**.</span><span class="sxs-lookup"><span data-stu-id="3b19c-132">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="3b19c-133">Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="3b19c-133">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="3b19c-134">На странице **выбора топологии** выберите топологию **интеграции System Center Configuration Manager** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3b19c-134">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="3b19c-135">В списке устанавливаемых компонентов выберите **база данных восстановления** и **база данных аудита**, а затем снимите оставшиеся возможности.</span><span class="sxs-lookup"><span data-stu-id="3b19c-135">From the list of features to install, select **Recovery Database** and **Audit Database**, and clear the remaining features.</span></span>

    <span data-ttu-id="3b19c-136">**Примечание**  Мастер установки проверяет предварительные требования для установки и выводит недостающие необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="3b19c-136">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="3b19c-137">Если все необходимые условия выполнены, установка будет продолжена.</span><span class="sxs-lookup"><span data-stu-id="3b19c-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="3b19c-138">Если обнаружен отсутствующий предварительный компонент, необходимо устранить недостающие необходимые компоненты и нажать кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="3b19c-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="3b19c-139">Если все необходимые условия выполнены, установка возобновляется.</span><span class="sxs-lookup"><span data-stu-id="3b19c-139">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="3b19c-140">На странице **Настройка базы данных восстановления** укажите имена компьютеров, на которых будет работать Сервер администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3b19c-140">On the **Configure the Recovery Database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="3b19c-141">После развертывания компонента администрирования и сервера мониторинга для подключения к базе данных используется учетная запись домена.</span><span class="sxs-lookup"><span data-stu-id="3b19c-141">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

7.  <span data-ttu-id="3b19c-142">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3b19c-142">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="3b19c-143">Укажите имя экземпляра SQL Server и имя базы данных, в которой будут храниться данные для восстановления.</span><span class="sxs-lookup"><span data-stu-id="3b19c-143">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="3b19c-144">Кроме того, необходимо указать, где будет находиться база данных и где будут храниться данные журнала.</span><span class="sxs-lookup"><span data-stu-id="3b19c-144">You must also specify both where the database will be located and where the log information will be located.</span></span>

9.  <span data-ttu-id="3b19c-145">Нажмите кнопку **Далее** , чтобы продолжить работу с мастером установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="3b19c-145">Click **Next** to continue with the MBAM Setup installation wizard.</span></span>

10. <span data-ttu-id="3b19c-146">На странице **Настройка базы данных аудита** укажите учетную запись пользователя, которая будет использоваться для доступа к базе данных для отчетов.</span><span class="sxs-lookup"><span data-stu-id="3b19c-146">On the **Configure the Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

11. <span data-ttu-id="3b19c-147">Укажите имена компьютеров, на которых будут работать Сервер администрирования и мониторинга, а также отчеты об аудите.</span><span class="sxs-lookup"><span data-stu-id="3b19c-147">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Audit Reports.</span></span> <span data-ttu-id="3b19c-148">После развертывания функций администрирования и мониторинга, а также для подключения к базам данных используются учетные записи домена.</span><span class="sxs-lookup"><span data-stu-id="3b19c-148">After the Administration and Monitoring and the Audit Reports features are deployed, their domain accounts will be used to connect to the databases.</span></span>

    <span data-ttu-id="3b19c-149">**Примечание**  Если вы устанавливаете базу данных аудита без функции "отчеты об аудите", необходимо добавить на компьютер с базой данных аудита исключение для включения входящего трафика на порт Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3b19c-149">**Note** If you are installing the Audit Database without the Audit Reports feature, you must add an exception on the Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="3b19c-150">Номер порта по умолчанию — 1433.</span><span class="sxs-lookup"><span data-stu-id="3b19c-150">The default port number is 1433.</span></span>

     

12. <span data-ttu-id="3b19c-151">Укажите имя экземпляра SQL Server и имя базы данных, в которой будут храниться данные аудита.</span><span class="sxs-lookup"><span data-stu-id="3b19c-151">Specify the SQL Server instance name and the name of the database that will store the audit data.</span></span> <span data-ttu-id="3b19c-152">Кроме того, необходимо указать, где будут храниться сведения о базе данных и журнале.</span><span class="sxs-lookup"><span data-stu-id="3b19c-152">You must also specify where the database and log information will be located.</span></span>

13. <span data-ttu-id="3b19c-153">Нажмите кнопку " **установить** ", чтобы запустить установку, а затем нажмите кнопку **"Готово"** , чтобы завершить установку.</span><span class="sxs-lookup"><span data-stu-id="3b19c-153">Click **Install** to start the installation, and then click **Finish** to complete the installation.</span></span>

**<span data-ttu-id="3b19c-154">Установка функций сервера администрирования и мониторинга на сервере администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="3b19c-154">To install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="3b19c-155">На сервере администрирования и мониторинга запустите **MBAMSetup.exe** , чтобы запустить мастер установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="3b19c-155">On the Administration and Monitoring Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="3b19c-156">На странице **приветствия** при необходимости выберите **программу улучшения качества программного**обеспечения, а затем нажмите кнопку **начать**.</span><span class="sxs-lookup"><span data-stu-id="3b19c-156">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="3b19c-157">Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="3b19c-157">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="3b19c-158">На странице **выбора топологии** выберите топологию **интеграции System Center Configuration Manager** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3b19c-158">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="3b19c-159">В списке устанавливаемых компонентов выберите элемент **Администрирование и сервер мониторинга** и **портал самообслуживания**и снимите оставшиеся возможности.</span><span class="sxs-lookup"><span data-stu-id="3b19c-159">From the list of features to install, select **Administration and Monitoring Server** and **Self-Service Portal**, and clear the remaining features.</span></span>

    <span data-ttu-id="3b19c-160">**Примечание**  Мастер установки проверяет предварительные требования для установки и выводит недостающие необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="3b19c-160">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="3b19c-161">Если все необходимые условия выполнены, установка будет продолжена.</span><span class="sxs-lookup"><span data-stu-id="3b19c-161">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="3b19c-162">Если обнаружен отсутствующий предварительный компонент, необходимо устранить недостающие необходимые компоненты и нажать кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="3b19c-162">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="3b19c-163">Если все необходимые условия выполнены, установка возобновляется.</span><span class="sxs-lookup"><span data-stu-id="3b19c-163">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="3b19c-164">Установите Портал самообслуживания, выполнив действия, описанные в разделе **Установка портала самообслуживания для** [установки и настройки MBAM на распределенных серверах](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="3b19c-164">Install the Self-Service Portal by following the steps in the **To install the Self-Service Portal** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

    <span data-ttu-id="3b19c-165">**Примечание**  Если клиентские компьютеры не будут иметь доступ к сети доставки содержимого (CDN) Microsoft Content, который предоставляет порталу самообслуживания требуемый доступ к определенным файлам JavaScript, выполните действия, описанные в разделе **Настройка портала самообслуживания, когда конечные пользователи не могут получить доступ к разделу "сеть доставки содержимого"** , [как установить и настроить MBAM на распределенных серверах](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) , чтобы настроить портал самообслуживания для ссылок на файлы JavaScript из доступного источника.</span><span class="sxs-lookup"><span data-stu-id="3b19c-165">**Note** If the client computers will not have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, complete the steps in the **To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network** section [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

     

7.  <span data-ttu-id="3b19c-166">Установите компоненты сервера администрирования и мониторинга, выполнив действия, описанные в разделе **Установка компонентов сервера администрирования и мониторинга** для [установки и настройки MBAM на распределенных серверах](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="3b19c-166">Install the Administration and Monitoring Server features by following the steps in the **To install the Administration and Monitoring Server feature** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

8.  <span data-ttu-id="3b19c-167">Нажмите кнопку **Готово** , чтобы завершить установку.</span><span class="sxs-lookup"><span data-stu-id="3b19c-167">Click **Finish** to complete the installation.</span></span>

## <span data-ttu-id="3b19c-168">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3b19c-168">Related topics</span></span>


[<span data-ttu-id="3b19c-169">Порядок проверки установки MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="3b19c-169">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[<span data-ttu-id="3b19c-170">Развертывание MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="3b19c-170">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





