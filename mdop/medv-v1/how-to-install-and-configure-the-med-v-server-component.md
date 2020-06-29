---
title: Установка и настройка серверного компонента MED-V Server
description: Установка и настройка серверного компонента MED-V Server
author: dansimp
ms.assetid: 2d3c5b15-df2c-4ab6-bf78-f47ef8ae7418
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4fb0cc5c9ffe76e987e316d0285f172dd0b76578
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826979"
---
# <span data-ttu-id="3b64b-103">Установка и настройка серверного компонента MED-V Server</span><span class="sxs-lookup"><span data-stu-id="3b64b-103">How to Install and Configure the MED-V Server Component</span></span>


<span data-ttu-id="3b64b-104">В этом разделе объясняется, как [установить](#bkmk-howtoinstallthemedvserver) и [настроить](#bkmk-howtoconfigurethemedvserver) сервер MED-V.</span><span class="sxs-lookup"><span data-stu-id="3b64b-104">This section explains how to [install](#bkmk-howtoinstallthemedvserver) and [configure](#bkmk-howtoconfigurethemedvserver) the MED-V server.</span></span>

## <a href="" id="bkmk-howtoinstallthemedvserver"></a><span data-ttu-id="3b64b-105">Установка сервера MED-V</span><span class="sxs-lookup"><span data-stu-id="3b64b-105">How to Install the MED-V Server</span></span>


**<span data-ttu-id="3b64b-106">Установка сервера MED-V</span><span class="sxs-lookup"><span data-stu-id="3b64b-106">To install the MED-V server</span></span>**

1.  <span data-ttu-id="3b64b-107">Установите пакет приложения MED-V Server. msi.</span><span class="sxs-lookup"><span data-stu-id="3b64b-107">Install the MED-V Server .msi package.</span></span>

    <span data-ttu-id="3b64b-108">Пакет для MED-V Server. msi называется *MED-V\_Server\_x.msi*, где x — номер версии.</span><span class="sxs-lookup"><span data-stu-id="3b64b-108">The MED-V Server .msi package is called *MED-V\_Server\_x.msi*, where x is the version number.</span></span>

    <span data-ttu-id="3b64b-109">Например, *MED-V\_Server\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="3b64b-109">For example, *MED-V\_Server\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="3b64b-110">После появления экрана **приветствия мастера InstallShield** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-110">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

3.  <span data-ttu-id="3b64b-111">На экране лицензионного **соглашения** ознакомьтесь с лицензионным соглашением, выберите **я принимаю условия лицензионного соглашения**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-111">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

    <span data-ttu-id="3b64b-112">Откроется экран **Конечная папка** с отображаемой папкой "Установка по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="3b64b-112">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="3b64b-113">По умолчанию используется папка для установки *%systemdrive%\\Program Files\\Microsoft Enterprise настольная Virtualization\\*.</span><span class="sxs-lookup"><span data-stu-id="3b64b-113">The default installation folder is *%systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization\\*.</span></span>

    -   <span data-ttu-id="3b64b-114">Чтобы изменить папку, в которой должна быть установлена версия MED-V, нажмите кнопку **изменить** и перейдите к существующей папке.</span><span class="sxs-lookup"><span data-stu-id="3b64b-114">To change the folder where MED-V should be installed, click **Change** and browse to an existing folder.</span></span>

4.  <span data-ttu-id="3b64b-115">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-115">Click **Next**.</span></span>

5.  <span data-ttu-id="3b64b-116">На экране **Готово для установки программы** нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-116">On the **Ready to Install the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="3b64b-117">Запустится установка сервера MED-V.</span><span class="sxs-lookup"><span data-stu-id="3b64b-117">The MED-V server installation starts.</span></span> <span data-ttu-id="3b64b-118">Это может занять несколько минут, и на экране может не отображаться текст.</span><span class="sxs-lookup"><span data-stu-id="3b64b-118">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="3b64b-119">Во время установки появляются несколько экранов хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="3b64b-119">During installation, several progress screens appear.</span></span> <span data-ttu-id="3b64b-120">Если появится сообщение, следуйте инструкциям, приведенным в этой области.</span><span class="sxs-lookup"><span data-stu-id="3b64b-120">If a message appears, follow the instructions provided.</span></span>

6.  <span data-ttu-id="3b64b-121">После появления экрана **мастера InstallShield** нажмите кнопку **Готово** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="3b64b-121">When the **InstallShield Wizard Completed** screen appears, click **Finish** to complete the wizard.</span></span>

**<span data-ttu-id="3b64b-122">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3b64b-122">Note</span></span>**  
<span data-ttu-id="3b64b-123">Если вы устанавливаете сервер MED-V через Microsoft Remote Desktop, используйте следующий синтаксис: **mstsc или Admin**. Убедитесь, что сеанс подключения к удаленному рабочему столу направлен на консоль.</span><span class="sxs-lookup"><span data-stu-id="3b64b-123">If you are installing the MED-V server via Microsoft Remote Desktop, use the following syntax: **mstsc/admin**. Ensure that your RDP session is directed to the console.</span></span>



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a><span data-ttu-id="3b64b-124">Настройка сервера MED-V</span><span class="sxs-lookup"><span data-stu-id="3b64b-124">How to Configure the MED-V Server</span></span>


<span data-ttu-id="3b64b-125">Можно настроить следующие параметры сервера:</span><span class="sxs-lookup"><span data-stu-id="3b64b-125">The following server settings can be configured:</span></span>

-   [<span data-ttu-id="3b64b-126">Подключения</span><span class="sxs-lookup"><span data-stu-id="3b64b-126">Connections</span></span>](#bkmk-configuringconnections)

-   [<span data-ttu-id="3b64b-127">Изображения</span><span class="sxs-lookup"><span data-stu-id="3b64b-127">Images</span></span>](#bkmk-configuringimages)

-   [<span data-ttu-id="3b64b-128">Разрешения</span><span class="sxs-lookup"><span data-stu-id="3b64b-128">Permissions</span></span>](#bkmk-configuringpermissions)

-   [<span data-ttu-id="3b64b-129">Отчеты</span><span class="sxs-lookup"><span data-stu-id="3b64b-129">Reports</span></span>](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a><span data-ttu-id="3b64b-130">Настройка подключений</span><span class="sxs-lookup"><span data-stu-id="3b64b-130">Configuring Connections</span></span>

**<span data-ttu-id="3b64b-131">Настройка подключений</span><span class="sxs-lookup"><span data-stu-id="3b64b-131">To configure connections</span></span>**

1.  <span data-ttu-id="3b64b-132">В меню Пуск Windows выберите **все программы, &gt; &gt; Диспетчер конфигурации сервера**med-v.</span><span class="sxs-lookup"><span data-stu-id="3b64b-132">On the Windows Start menu, select **All Programs &gt; MED-V &gt; MED-V Server Configuration Manager**.</span></span>

    **<span data-ttu-id="3b64b-133">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3b64b-133">Note</span></span>**  
    <span data-ttu-id="3b64b-134">Примечание. Если при установке сервера установлен флажок **запустить диспетчер конфигурации MED-v Server** , диспетчер конфигурации MED-v автоматически запускается после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="3b64b-134">Note: If you selected the **Launch MED-V Server Configuration Manager** check box during the server installation, the MED-V server configuration manager starts automatically after the server installation is complete.</span></span>



~~~
The MED-V Server Configuration Manager appears.
~~~

2. <span data-ttu-id="3b64b-135">На вкладке **подключения** настройте следующие параметры клиентских подключений:</span><span class="sxs-lookup"><span data-stu-id="3b64b-135">On the **Connections** tab, configure the following client connections settings:</span></span>

   -   <span data-ttu-id="3b64b-136">**Включить нешифрованные соединения (http) с помощью порта**— установите этот флажок, чтобы включить незашифрованные подключения с помощью указанного порта.</span><span class="sxs-lookup"><span data-stu-id="3b64b-136">**Enable unencrypted connections (http), using port**—Select this check box to enable unencrypted connections using a specified port.</span></span> <span data-ttu-id="3b64b-137">В поле Port (порт) введите порт сервера, на котором вы хотите использовать незашифрованные соединения (http).</span><span class="sxs-lookup"><span data-stu-id="3b64b-137">In the port box, enter the server port on which to accept unencrypted connections (http).</span></span>

   -   <span data-ttu-id="3b64b-138">**Включить шифрование подключений (HTTPS) с помощью порта**— установите этот флажок, чтобы включить шифрование подключений с помощью указанного порта.</span><span class="sxs-lookup"><span data-stu-id="3b64b-138">**Enable encrypted connections (https), using port**—Select this check box to enable encrypted connections using a specified port.</span></span> <span data-ttu-id="3b64b-139">В поле Port (порт) введите порт сервера, на котором вы хотите использовать зашифрованные подключения (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="3b64b-139">In the port box, enter the server port on which to accept encrypted connections (https).</span></span>

       <span data-ttu-id="3b64b-140">HTTPS — это необязательная конфигурация, с помощью которой можно настроить безопасные транзакции между сервером MED-V и клиентами MED-V.</span><span class="sxs-lookup"><span data-stu-id="3b64b-140">Https is an optional configuration which can be set to ensure secure transactions between the MED-V server and MED-V clients.</span></span> <span data-ttu-id="3b64b-141">Для настройки HTTPS необходимо выполнить описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3b64b-141">To configure https, you must perform the following procedures:</span></span>

       -   <span data-ttu-id="3b64b-142">Настройка сертификата на сервере.</span><span class="sxs-lookup"><span data-stu-id="3b64b-142">Configure a certificate on the server.</span></span>

       -   <span data-ttu-id="3b64b-143">Свяжите сертификат сервера с портом, указанным с помощью команды Netsh.</span><span class="sxs-lookup"><span data-stu-id="3b64b-143">Associate the server certificate with the port specified using netsh.</span></span> <span data-ttu-id="3b64b-144">Дополнительные сведения можно найти в перечисленных ниже случаях.</span><span class="sxs-lookup"><span data-stu-id="3b64b-144">For information, see the following:</span></span>

           -   [<span data-ttu-id="3b64b-145">Команды Netsh для протоколов передачи гипертекста (HTTP)</span><span class="sxs-lookup"><span data-stu-id="3b64b-145">Netsh Commands for Hypertext Transfer Protocol (HTTP)</span></span>](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [<span data-ttu-id="3b64b-146">Инструкции: Настройка порта с помощью SSL-сертификата</span><span class="sxs-lookup"><span data-stu-id="3b64b-146">How to: Configure a Port with an SSL Certificate</span></span>](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [<span data-ttu-id="3b64b-147">Инструкции: Настройка порта с помощью SSL-сертификата</span><span class="sxs-lookup"><span data-stu-id="3b64b-147">How to: Configure a Port with an SSL Certificate</span></span>](https://msdn.microsoft.com/library/ms733791.aspx)

3. <span data-ttu-id="3b64b-148">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-148">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringimages"></a><span data-ttu-id="3b64b-149">Настройка изображений</span><span class="sxs-lookup"><span data-stu-id="3b64b-149">Configuring Images</span></span>

**<span data-ttu-id="3b64b-150">Настройка изображений</span><span class="sxs-lookup"><span data-stu-id="3b64b-150">To configure images</span></span>**

1.  <span data-ttu-id="3b64b-151">Откройте вкладку **изображения** .</span><span class="sxs-lookup"><span data-stu-id="3b64b-151">Click the **Images** tab.</span></span>

2.  <span data-ttu-id="3b64b-152">Настройте следующие параметры управления образами:</span><span class="sxs-lookup"><span data-stu-id="3b64b-152">Configure the following image management settings:</span></span>

    -   <span data-ttu-id="3b64b-153">**Каталог ВМ**— каталог виртуальной машины (каталог, в котором хранятся изображения).</span><span class="sxs-lookup"><span data-stu-id="3b64b-153">**VMs Directory**—The virtual machine directory (the directory where the images are stored).</span></span> <span data-ttu-id="3b64b-154">Это поле имеет UNC-путь к каталогу изображений на сервере распространения изображений, который должен быть доступен на сервере MED-V.</span><span class="sxs-lookup"><span data-stu-id="3b64b-154">This field contains a UNC path to the image directory on the image distribution server that should be accessible from the MED-V server.</span></span>

    -   <span data-ttu-id="3b64b-155">**URL-адрес ВМ**— расположение сервера, на котором хранятся изображения.</span><span class="sxs-lookup"><span data-stu-id="3b64b-155">**VMs URL**—The location of the server where the images are stored.</span></span>

3.  <span data-ttu-id="3b64b-156">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-156">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringpermissions"></a><span data-ttu-id="3b64b-157">Настройка разрешений</span><span class="sxs-lookup"><span data-stu-id="3b64b-157">Configuring Permissions</span></span>

**<span data-ttu-id="3b64b-158">Настройка разрешений</span><span class="sxs-lookup"><span data-stu-id="3b64b-158">To configure permissions</span></span>**

1.  <span data-ttu-id="3b64b-159">Откройте вкладку **разрешения** .</span><span class="sxs-lookup"><span data-stu-id="3b64b-159">Click the **Permissions** tab.</span></span>

2.  <span data-ttu-id="3b64b-160">Предоставляется список всех пользователей, которые могут войти в систему.</span><span class="sxs-lookup"><span data-stu-id="3b64b-160">A list of all users who can log in is provided.</span></span> <span data-ttu-id="3b64b-161">Чтобы применить разрешения на чтение и запись для пользователя, установите флажок рядом с нужным пользователем.</span><span class="sxs-lookup"><span data-stu-id="3b64b-161">To apply read and write permissions to a user, select the check box next to the user.</span></span> <span data-ttu-id="3b64b-162">Чтобы применить к пользователю разрешения только для чтения, снимите флажок.</span><span class="sxs-lookup"><span data-stu-id="3b64b-162">To apply read-only permissions to a user, clear the check box.</span></span>

3.  <span data-ttu-id="3b64b-163">Чтобы добавить пользователей домена или группы, нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-163">To add domain users or groups, click **Add**.</span></span>

    <span data-ttu-id="3b64b-164">Откроется диалоговое окно " **Введите имена пользователей или групп** ".</span><span class="sxs-lookup"><span data-stu-id="3b64b-164">The **Enter User or Group names** dialog box appears.</span></span>

    1.  <span data-ttu-id="3b64b-165">Выберите пункт Пользователи домена или группы, выполнив одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="3b64b-165">Select domain users or groups by doing one of the following:</span></span>

        -   <span data-ttu-id="3b64b-166">В поле **Введите имена пользователей или групп** введите пользователя или группу, которые есть в домене или находятся в качестве локальных пользователей или групп на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3b64b-166">In the **Enter User or Group names** field, type a user or group that exists in the domain or exists as a local user or group on the computer.</span></span> <span data-ttu-id="3b64b-167">Затем нажмите кнопку **Проверить имена** , чтобы сопоставить их с полностью существующим именем.</span><span class="sxs-lookup"><span data-stu-id="3b64b-167">Then click **Check Names** to resolve it to the full existent name.</span></span>

        -   <span data-ttu-id="3b64b-168">Нажмите кнопку **найти** , чтобы открыть диалоговое окно Стандартный **Выбор пользователей или групп** .</span><span class="sxs-lookup"><span data-stu-id="3b64b-168">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="3b64b-169">Затем выберите пункт Пользователи домена или группы.</span><span class="sxs-lookup"><span data-stu-id="3b64b-169">Then select domain users or groups.</span></span>

    2.  <span data-ttu-id="3b64b-170">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-170">Click **OK**.</span></span>

4.  <span data-ttu-id="3b64b-171">Для удаления пользователей или групп домена выберите пользователя или группу и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-171">To remove domain users or groups, select a user or group and click **Remove**.</span></span>

5.  <span data-ttu-id="3b64b-172">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-172">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringreports"></a><span data-ttu-id="3b64b-173">Настройка отчетов</span><span class="sxs-lookup"><span data-stu-id="3b64b-173">Configuring Reports</span></span>

**<span data-ttu-id="3b64b-174">Настройка отчетов</span><span class="sxs-lookup"><span data-stu-id="3b64b-174">To configure reports</span></span>**

1.  <span data-ttu-id="3b64b-175">Откройте вкладку **отчеты** .</span><span class="sxs-lookup"><span data-stu-id="3b64b-175">Click the **Reports** tab.</span></span>

2.  <span data-ttu-id="3b64b-176">Для поддержки отчетов выберите **включить отчеты**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-176">To support reports, select **Enable reports**.</span></span>

3.  <span data-ttu-id="3b64b-177">В поле **строка подключения** введите строку подключения для базы данных MSSQL.</span><span class="sxs-lookup"><span data-stu-id="3b64b-177">In the **Connection String** box, enter a connection string for the MSSQL database.</span></span>

    -   <span data-ttu-id="3b64b-178">При установке SQL Server на удаленном сервере используйте следующую строку подключения:</span><span class="sxs-lookup"><span data-stu-id="3b64b-178">When SQL Server is installed on a remote server, use the following connection string:</span></span>

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **<span data-ttu-id="3b64b-179">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3b64b-179">Note</span></span>**  
        <span data-ttu-id="3b64b-180">Примечание. чтобы подключиться к SQL Express, используйте:</span><span class="sxs-lookup"><span data-stu-id="3b64b-180">Note: To connect to SQL Express, use:</span></span> `Data Source=<ServerName>\sqlexpress.`



4.  <span data-ttu-id="3b64b-181">Чтобы создать базу данных, нажмите кнопку **создать базу данных**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-181">To create the database, click **Create Database**.</span></span>

5.  <span data-ttu-id="3b64b-182">Чтобы проверить подключение, нажмите кнопку **проверить соединение**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-182">To test the connection, click **Test Connection**.</span></span>

6.  <span data-ttu-id="3b64b-183">Чтобы настроить параметры очистки базы данных, нажмите кнопку **очистить параметры**.</span><span class="sxs-lookup"><span data-stu-id="3b64b-183">To configure database clearing options, click **Clear Options**.</span></span>

    <span data-ttu-id="3b64b-184">Откроется диалоговое окно " **Очистка параметров базы данных** ".</span><span class="sxs-lookup"><span data-stu-id="3b64b-184">The **Clear Database Options** dialog box appears.</span></span>

    1.  <span data-ttu-id="3b64b-185">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="3b64b-185">Choose one of the following options:</span></span>

        -   <span data-ttu-id="3b64b-186">**Очистка данных старше**, очистка всех данных, которые старше указанного количества дней; в поле число введите количество дней.</span><span class="sxs-lookup"><span data-stu-id="3b64b-186">**Clear data older than**—Clear all data older than the number of days specified; in the number box, enter a number of days.</span></span>

        -   <span data-ttu-id="3b64b-187">**Очистите все данные из базы данных**— очистите все данные в базе данных.</span><span class="sxs-lookup"><span data-stu-id="3b64b-187">**Clear all data from database**—Clear all existent data in the database.</span></span>

        -   <span data-ttu-id="3b64b-188">**DROP DATABASE**(удалить базу данных) — удаление базы данных.</span><span class="sxs-lookup"><span data-stu-id="3b64b-188">**Drop database**—Delete the database.</span></span>

    2.  <span data-ttu-id="3b64b-189">Нажмите кнопку **ОК** , чтобы применить изменения и закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3b64b-189">Click **OK** to apply changes and close the dialog box.</span></span>

7.  <span data-ttu-id="3b64b-190">Нажмите кнопку **ОК** , чтобы сохранить изменения, или кнопку **Отмена** , чтобы закрыть диалоговое окно без сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="3b64b-190">Click **OK** to save the changes, or click **Cancel** to close the dialog box without saving changes.</span></span>

8.  <span data-ttu-id="3b64b-191">Если будет предложено, перезапустите службу сервера MED-V, чтобы применить изменения к сетевым параметрам.</span><span class="sxs-lookup"><span data-stu-id="3b64b-191">If prompted, restart the MED-V server service to apply changes to the network settings.</span></span>

## <span data-ttu-id="3b64b-192">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3b64b-192">Related topics</span></span>


[<span data-ttu-id="3b64b-193">Поддерживаемые конфигурации</span><span class="sxs-lookup"><span data-stu-id="3b64b-193">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="3b64b-194">Проектирование серверной инфраструктуры MED-V Server</span><span class="sxs-lookup"><span data-stu-id="3b64b-194">Design the MED-V Server Infrastructure</span></span>](design-the-med-v-server-infrastructure.md)









