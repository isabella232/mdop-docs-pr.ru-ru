---
title: Развертывание сервера App-V 5.1 с помощью сценария
description: Развертывание сервера App-V 5.1 с помощью сценария
author: dansimp
ms.assetid: 15c33d7b-9b61-4dbc-8674-399bb33e5f7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/20/2020
ms.openlocfilehash: 579ca685f677aaaa4f5ebb6ac8d2969fdcbe2cd2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814128"
---
# <span data-ttu-id="52cb3-103">Развертывание сервера App-V 5.1 с помощью сценария</span><span class="sxs-lookup"><span data-stu-id="52cb3-103">How to Deploy the App-V 5.1 Server Using a Script</span></span>

<span data-ttu-id="52cb3-104">Для того чтобы завершить настройку сервера **appv\_server\_setup.exe** успешно использовать командную строку, необходимо указать и объединить несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="52cb3-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

## <span data-ttu-id="52cb3-105">Установка сервера App-V 5,1 с помощью сценария</span><span class="sxs-lookup"><span data-stu-id="52cb3-105">Install the App-V 5.1 server using a script</span></span>

- <span data-ttu-id="52cb3-106">Воспользуйтесь следующими сведениями об установке сервера App-V 5,1 с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="52cb3-106">Use the following information about installing the App-V 5.1 server using the command line.</span></span>

    > [!NOTE]
    > <span data-ttu-id="52cb3-107">Сведения из приведенных ниже таблиц также можно вызвать с помощью командной строки, введя следующую команду: **appv\_server\_setup.exe/?**.</span><span class="sxs-lookup"><span data-stu-id="52cb3-107">The information in the following tables can also be accessed using the command line by typing the following command: **appv\_server\_setup.exe /?**.</span></span>

### <span data-ttu-id="52cb3-108">Установка сервера управления и базы данных управления на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="52cb3-108">Install the Management server and Management database on a local machine</span></span>

<span data-ttu-id="52cb3-109">Следующие параметры являются допустимыми и для стандартного, и для настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52cb3-109">The following parameters are valid with both the default and custom instance of Microsoft SQL Server:</span></span>

- <span data-ttu-id="52cb3-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-110">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="52cb3-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-111">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="52cb3-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-112">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="52cb3-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-113">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="52cb3-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="52cb3-114">/DB_PREDEPLOY_MANAGEMENT</span></span>
- <span data-ttu-id="52cb3-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="52cb3-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-116">/MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="52cb3-117">Пример: использование настраиваемого экземпляра Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="52cb3-117">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### <span data-ttu-id="52cb3-118">Установка сервера управления с помощью существующей базы данных управления на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="52cb3-118">Install the Management server using an existing Management database on a local machine</span></span>

<span data-ttu-id="52cb3-119">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).</span><span class="sxs-lookup"><span data-stu-id="52cb3-119">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-120">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-120">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="52cb3-121">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-121">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="52cb3-122">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-122">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="52cb3-123">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-123">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="52cb3-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="52cb3-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="52cb3-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="52cb3-126">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-126">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="52cb3-127">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте указанные ниже параметры (отличия от экземпляра по умолчанию *курсивом*).</span><span class="sxs-lookup"><span data-stu-id="52cb3-127">To use a custom instance of Microsoft SQL Server, use the following parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-128">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-128">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="52cb3-129">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-129">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="52cb3-130">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-130">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="52cb3-131">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-131">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="52cb3-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="52cb3-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="52cb3-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="52cb3-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="52cb3-134">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-134">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="52cb3-135">Пример: использование настраиваемого экземпляра Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="52cb3-135">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="52cb3-136">Установка сервера управления с помощью существующей базы данных управления на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="52cb3-136">Install the Management server using an existing Management database on a remote machine</span></span>

<span data-ttu-id="52cb3-137">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).</span><span class="sxs-lookup"><span data-stu-id="52cb3-137">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-138">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-138">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="52cb3-139">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-139">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="52cb3-140">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-140">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="52cb3-141">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-141">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="52cb3-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="52cb3-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="52cb3-144">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-144">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="52cb3-145">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):</span><span class="sxs-lookup"><span data-stu-id="52cb3-145">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-146">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-146">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="52cb3-147">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-147">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="52cb3-148">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-148">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="52cb3-149">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-149">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="52cb3-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="52cb3-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="52cb3-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="52cb3-152">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-152">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="52cb3-153">Пример: использование настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52cb3-153">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="52cb3-154">Установка базы данных управления и сервера управления на одном и том же компьютере</span><span class="sxs-lookup"><span data-stu-id="52cb3-154">Install the Management database and the Management Server on the same computer</span></span>

<span data-ttu-id="52cb3-155">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).</span><span class="sxs-lookup"><span data-stu-id="52cb3-155">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-156">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="52cb3-156">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="52cb3-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="52cb3-158">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-158">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="52cb3-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="52cb3-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="52cb3-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="52cb3-161">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):</span><span class="sxs-lookup"><span data-stu-id="52cb3-161">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-162">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="52cb3-162">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="52cb3-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="52cb3-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="52cb3-164">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-164">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="52cb3-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="52cb3-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="52cb3-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="52cb3-167">Пример: использование настраиваемого экземпляра Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="52cb3-167">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="52cb3-168">Установка базы данных управления на компьютере, отличном от сервера управления</span><span class="sxs-lookup"><span data-stu-id="52cb3-168">Install the Management database on a different computer than the Management server</span></span>

<span data-ttu-id="52cb3-169">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).</span><span class="sxs-lookup"><span data-stu-id="52cb3-169">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-170">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="52cb3-170">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="52cb3-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="52cb3-172">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-172">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="52cb3-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="52cb3-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="52cb3-175">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):</span><span class="sxs-lookup"><span data-stu-id="52cb3-175">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-176">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="52cb3-176">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="52cb3-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="52cb3-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="52cb3-178">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-178">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="52cb3-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="52cb3-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="52cb3-181">Пример: использование настраиваемого экземпляра Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="52cb3-181">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="52cb3-182">Установка сервера публикаций</span><span class="sxs-lookup"><span data-stu-id="52cb3-182">Install the publishing server</span></span>

<span data-ttu-id="52cb3-183">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="52cb3-183">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span>

- <span data-ttu-id="52cb3-184">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-184">/PUBLISHING_SERVER</span></span>
- <span data-ttu-id="52cb3-185">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-185">/PUBLISHING_MGT_SERVER</span></span>
- <span data-ttu-id="52cb3-186">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-186">/PUBLISHING_WEBSITE_NAME</span></span>
- <span data-ttu-id="52cb3-187">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-187">/PUBLISHING_WEBSITE_PORT</span></span>

**<span data-ttu-id="52cb3-188">Пример: использование настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52cb3-188">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### <span data-ttu-id="52cb3-189">Установка сервера отчетов и базы данных отчетов на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="52cb3-189">Install the Reporting server and Reporting database on a local machine</span></span>

<span data-ttu-id="52cb3-190">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).</span><span class="sxs-lookup"><span data-stu-id="52cb3-190">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-191">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-191">/REPORTING _SERVER</span></span>
- <span data-ttu-id="52cb3-192">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-192">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="52cb3-193">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-193">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="52cb3-194">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="52cb3-194">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="52cb3-195">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-195">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="52cb3-196">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-196">/REPORTING _DB_NAME</span></span>

<span data-ttu-id="52cb3-197">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):</span><span class="sxs-lookup"><span data-stu-id="52cb3-197">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-198">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-198">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="52cb3-199">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-199">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="52cb3-200">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-200">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="52cb3-201">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-201">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="52cb3-202">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="52cb3-202">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="52cb3-203">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="52cb3-203">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="52cb3-204">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-204">/REPORTING _DB_NAME</span></span>

**<span data-ttu-id="52cb3-205">Пример: использование настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52cb3-205">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="52cb3-206">Установка сервера отчетов и использование существующей базы данных отчетов на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="52cb3-206">Install the Reporting server and using an existing Reporting database on a local machine</span></span>

<span data-ttu-id="52cb3-207">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).</span><span class="sxs-lookup"><span data-stu-id="52cb3-207">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-208">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-208">/REPORTING _SERVER</span></span>
- <span data-ttu-id="52cb3-209">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-209">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="52cb3-210">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-210">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="52cb3-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="52cb3-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="52cb3-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="52cb3-213">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-213">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="52cb3-214">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):</span><span class="sxs-lookup"><span data-stu-id="52cb3-214">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-215">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-215">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="52cb3-216">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-216">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="52cb3-217">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-217">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="52cb3-218">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-218">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="52cb3-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="52cb3-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="52cb3-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="52cb3-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="52cb3-221">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-221">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="52cb3-222">Пример: использование настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52cb3-222">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="52cb3-223">Установка сервера отчетов с помощью существующей базы данных отчетов на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="52cb3-223">Install the Reporting server using an existing Reporting database on a remote machine</span></span>

<span data-ttu-id="52cb3-224">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).</span><span class="sxs-lookup"><span data-stu-id="52cb3-224">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-225">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-225">/REPORTING _SERVER</span></span>
- <span data-ttu-id="52cb3-226">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-226">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="52cb3-227">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-227">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="52cb3-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="52cb3-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="52cb3-230">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-230">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="52cb3-231">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):</span><span class="sxs-lookup"><span data-stu-id="52cb3-231">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-232">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-232">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="52cb3-233">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-233">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="52cb3-234">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-234">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="52cb3-235">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-235">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="52cb3-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="52cb3-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="52cb3-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="52cb3-238">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-238">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="52cb3-239">Пример: использование настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52cb3-239">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="52cb3-240">Установка базы данных отчетов на том же компьютере, что и сервер отчетов</span><span class="sxs-lookup"><span data-stu-id="52cb3-240">Install the Reporting database on the same computer as the Reporting server</span></span>

<span data-ttu-id="52cb3-241">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).</span><span class="sxs-lookup"><span data-stu-id="52cb3-241">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-242">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="52cb3-242">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="52cb3-243">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-243">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="52cb3-244">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-244">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="52cb3-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="52cb3-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="52cb3-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="52cb3-247">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):</span><span class="sxs-lookup"><span data-stu-id="52cb3-247">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-248">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="52cb3-248">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="52cb3-249">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="52cb3-249">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="52cb3-250">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-250">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="52cb3-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="52cb3-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="52cb3-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="52cb3-253">Пример: использование настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52cb3-253">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="52cb3-254">Установка базы данных отчетов на компьютере, отличном от сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="52cb3-254">Install the Reporting database on a different computer than the Reporting server</span></span>

<span data-ttu-id="52cb3-255">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).</span><span class="sxs-lookup"><span data-stu-id="52cb3-255">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-256">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="52cb3-256">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="52cb3-257">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-257">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="52cb3-258">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-258">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="52cb3-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="52cb3-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="52cb3-261">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):</span><span class="sxs-lookup"><span data-stu-id="52cb3-261">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="52cb3-262">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="52cb3-262">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="52cb3-263">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="52cb3-263">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>
- <span data-ttu-id="52cb3-264">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-264">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="52cb3-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="52cb3-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="52cb3-267">Пример: использование настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52cb3-267">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="52cb3-268">Определения параметров</span><span class="sxs-lookup"><span data-stu-id="52cb3-268">Parameter Definitions</span></span>

#### <span data-ttu-id="52cb3-269">Общие параметры</span><span class="sxs-lookup"><span data-stu-id="52cb3-269">General Parameters</span></span>

| <span data-ttu-id="52cb3-270">Параметр</span><span class="sxs-lookup"><span data-stu-id="52cb3-270">Parameter</span></span> | <span data-ttu-id="52cb3-271">Сведения</span><span class="sxs-lookup"><span data-stu-id="52cb3-271">Information</span></span> |
|--|--|
| <span data-ttu-id="52cb3-272">Параметрами</span><span class="sxs-lookup"><span data-stu-id="52cb3-272">/QUIET</span></span> | <span data-ttu-id="52cb3-273">Указывает на автоматическую установку.</span><span class="sxs-lookup"><span data-stu-id="52cb3-273">Specifies silent install.</span></span> |
| <span data-ttu-id="52cb3-274">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="52cb3-274">/UNINSTALL</span></span> | <span data-ttu-id="52cb3-275">Указывает на удаление.</span><span class="sxs-lookup"><span data-stu-id="52cb3-275">Specifies an uninstall.</span></span> |
| <span data-ttu-id="52cb3-276">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="52cb3-276">/LAYOUT</span></span> | <span data-ttu-id="52cb3-277">Задает действие макета.</span><span class="sxs-lookup"><span data-stu-id="52cb3-277">Specifies layout action.</span></span> <span data-ttu-id="52cb3-278">Файлы MSI и Script будут извлечены в папку без фактического их установки.</span><span class="sxs-lookup"><span data-stu-id="52cb3-278">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="52cb3-279">Значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="52cb3-279">No value is expected.</span></span> |
| <span data-ttu-id="52cb3-280">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="52cb3-280">/LAYOUTDIR</span></span> | <span data-ttu-id="52cb3-281">Указывает каталог макета.</span><span class="sxs-lookup"><span data-stu-id="52cb3-281">Specifies the layout directory.</span></span> <span data-ttu-id="52cb3-282">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="52cb3-282">Takes a string.</span></span> <span data-ttu-id="52cb3-283">Пример использования: **/LAYOUTDIR = "сервер виртуализации C:\\Application"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-283">Example usage: **/LAYOUTDIR="C:\\Application Virtualization Server"**</span></span> |
| <span data-ttu-id="52cb3-284">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="52cb3-284">/INSTALLDIR</span></span> | <span data-ttu-id="52cb3-285">Указывает каталог установки.</span><span class="sxs-lookup"><span data-stu-id="52cb3-285">Specifies the installation directory.</span></span> <span data-ttu-id="52cb3-286">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="52cb3-286">Takes a string.</span></span> <span data-ttu-id="52cb3-287">Пример использования: **/INSTALLDIR = "C:\\program Files Files\\Application Virtualization\\Server"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-287">Example usage: **/INSTALLDIR="C:\\Program Files\\Application Virtualization\\Server"**</span></span> |
| <span data-ttu-id="52cb3-288">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="52cb3-288">/MUOPTIN</span></span> | <span data-ttu-id="52cb3-289">Включение центра обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="52cb3-289">Enables Microsoft Update.</span></span> <span data-ttu-id="52cb3-290">Значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="52cb3-290">No value is expected.</span></span> |
| <span data-ttu-id="52cb3-291">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="52cb3-291">/ACCEPTEULA</span></span> | <span data-ttu-id="52cb3-292">Принимает лицензионное соглашение.</span><span class="sxs-lookup"><span data-stu-id="52cb3-292">Accepts the license agreement.</span></span> <span data-ttu-id="52cb3-293">Это необходимо для автоматической установки.</span><span class="sxs-lookup"><span data-stu-id="52cb3-293">This is required for an unattended installation.</span></span> <span data-ttu-id="52cb3-294">Пример использования: **/ACCEPTEULA** или **/ACCEPTEULA = 1**</span><span class="sxs-lookup"><span data-stu-id="52cb3-294">Example usage: **/ACCEPTEULA** or **/ACCEPTEULA=1**</span></span> |

#### <span data-ttu-id="52cb3-295">Параметры установки сервера управления</span><span class="sxs-lookup"><span data-stu-id="52cb3-295">Management Server Installation Parameters</span></span>

|<span data-ttu-id="52cb3-296">Параметр</span><span class="sxs-lookup"><span data-stu-id="52cb3-296">Parameter</span></span> |<span data-ttu-id="52cb3-297">Сведения</span><span class="sxs-lookup"><span data-stu-id="52cb3-297">Information</span></span> |
|--|--|
| <span data-ttu-id="52cb3-298">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-298">/MANAGEMENT_SERVER</span></span> | <span data-ttu-id="52cb3-299">Указывает, что сервер управления будет установлен.</span><span class="sxs-lookup"><span data-stu-id="52cb3-299">Specifies that the management server will be installed.</span></span> <span data-ttu-id="52cb3-300">Значение не ожидается</span><span class="sxs-lookup"><span data-stu-id="52cb3-300">No value is expected</span></span> |
| <span data-ttu-id="52cb3-301">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-301">/MANAGEMENT_ADMINACCOUNT</span></span> | <span data-ttu-id="52cb3-302">Указывает учетную запись, которая будет разрешена правами администратора на доступ к серверу управления.</span><span class="sxs-lookup"><span data-stu-id="52cb3-302">Specifies the account that will be allowed Administrator access to the management server.</span></span> <span data-ttu-id="52cb3-303">Это может быть учетная запись пользователя или группа.</span><span class="sxs-lookup"><span data-stu-id="52cb3-303">This can be a user account or a group.</span></span> <span data-ttu-id="52cb3-304">Пример использования: **/MANAGEMENT_ADMINACCOUNT = "mydomain\\admin"**.</span><span class="sxs-lookup"><span data-stu-id="52cb3-304">Example usage: **/MANAGEMENT_ADMINACCOUNT="mydomain\\admin"**.</span></span> <span data-ttu-id="52cb3-305">Если не задано **/MANAGEMENT_SERVER** , это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="52cb3-305">If **/MANAGEMENT_SERVER** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="52cb3-306">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-306">/MANAGEMENT_WEBSITE_NAME</span></span> | <span data-ttu-id="52cb3-307">Указывает имя веб-сайта, который будет создан для службы управления.</span><span class="sxs-lookup"><span data-stu-id="52cb3-307">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="52cb3-308">Пример использования: **/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V Management Service"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-308">Example usage: **/MANAGEMENT_WEBSITE_NAME="Microsoft App-V Management Service"**</span></span> |
| <span data-ttu-id="52cb3-309">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-309">MANAGEMENT_WEBSITE_PORT</span></span> | <span data-ttu-id="52cb3-310">Указывает номер порта, который будет использоваться службой управления.</span><span class="sxs-lookup"><span data-stu-id="52cb3-310">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="52cb3-311">Пример использования: **/MANAGEMENT_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="52cb3-311">Example usage: **/MANAGEMENT_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="52cb3-312">Параметры для базы данных сервера управления</span><span class="sxs-lookup"><span data-stu-id="52cb3-312">Parameters for the Management Server Database</span></span>

| <span data-ttu-id="52cb3-313">Параметр</span><span class="sxs-lookup"><span data-stu-id="52cb3-313">Parameter</span></span> | <span data-ttu-id="52cb3-314">Сведения</span><span class="sxs-lookup"><span data-stu-id="52cb3-314">Information</span></span> |
|--|--|
| <span data-ttu-id="52cb3-315">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="52cb3-315">/DB_PREDEPLOY_MANAGEMENT</span></span> | <span data-ttu-id="52cb3-316">Указывает, что база данных управления будет установлена.</span><span class="sxs-lookup"><span data-stu-id="52cb3-316">Specifies that the management database will be installed.</span></span> <span data-ttu-id="52cb3-317">Чтобы завершить установку, необходимо иметь разрешения, достаточные для базы данных.</span><span class="sxs-lookup"><span data-stu-id="52cb3-317">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="52cb3-318">Значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="52cb3-318">No value is expected.</span></span> |
| <span data-ttu-id="52cb3-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="52cb3-320">Указывает, что необходимо использовать экземпляр SQL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52cb3-320">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="52cb3-321">Значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="52cb3-321">No value is expected.</span></span> |
| <span data-ttu-id="52cb3-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="52cb3-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="52cb3-323">Указывает имя настраиваемого экземпляра SQL, который должен использоваться для создания новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="52cb3-323">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="52cb3-324">Пример использования: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"**.</span><span class="sxs-lookup"><span data-stu-id="52cb3-324">Example usage: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**.</span></span> <span data-ttu-id="52cb3-325">Если не задано **/DB_PREDEPLOY_MANAGEMENT** , это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="52cb3-325">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="52cb3-326">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-326">/MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="52cb3-327">Указывает имя новой базы данных управления, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="52cb3-327">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="52cb3-328">Пример использования: **/MANAGEMENT_DB_NAME = "AppVMgmtDB"**.</span><span class="sxs-lookup"><span data-stu-id="52cb3-328">Example usage: **/MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="52cb3-329">Если не задано **/DB_PREDEPLOY_MANAGEMENT** , это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="52cb3-329">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="52cb3-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="52cb3-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="52cb3-331">Указывает, установлен ли на локальном сервере сервер управления, который будет получать доступ к базе данных.</span><span class="sxs-lookup"><span data-stu-id="52cb3-331">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="52cb3-332">Параметр switched, поэтому значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="52cb3-332">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="52cb3-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="52cb3-334">Учетная запись удаленного компьютера, на котором будет установлен сервер управления.</span><span class="sxs-lookup"><span data-stu-id="52cb3-334">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="52cb3-335">Пример использования: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\\computername"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-335">Example usage: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="domain\\computername"**</span></span> |
| <span data-ttu-id="52cb3-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="52cb3-337">Учетная запись администратора, которая будет использоваться для установки сервера управления.</span><span class="sxs-lookup"><span data-stu-id="52cb3-337">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="52cb3-338">Пример использования: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-338">Example usage: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT ="domain\\alias"**</span></span> |

#### <span data-ttu-id="52cb3-339">Параметры для установки сервера публикаций</span><span class="sxs-lookup"><span data-stu-id="52cb3-339">Parameters for Installing Publishing Server</span></span>

| <span data-ttu-id="52cb3-340">Параметр</span><span class="sxs-lookup"><span data-stu-id="52cb3-340">Parameter</span></span> | <span data-ttu-id="52cb3-341">Сведения</span><span class="sxs-lookup"><span data-stu-id="52cb3-341">Information</span></span> |
|--|--|
| <span data-ttu-id="52cb3-342">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-342">/PUBLISHING_SERVER</span></span> | <span data-ttu-id="52cb3-343">Указывает, что сервер публикаций будет установлен.</span><span class="sxs-lookup"><span data-stu-id="52cb3-343">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="52cb3-344">Значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="52cb3-344">No value is expected.</span></span> |
| <span data-ttu-id="52cb3-345">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-345">/PUBLISHING_MGT_SERVER</span></span> | <span data-ttu-id="52cb3-346">Указывает URL-адрес службы управления, к которой будет подключаться сервер публикации.</span><span class="sxs-lookup"><span data-stu-id="52cb3-346">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="52cb3-347">Пример использования: \*\* &lt; имя сервера управления http:// &gt; : &lt; номер &gt; порта сервера управления\*\*.</span><span class="sxs-lookup"><span data-stu-id="52cb3-347">Example usage: **http://&lt;management server name&gt;:&lt;Management server port number&gt;**.</span></span> <span data-ttu-id="52cb3-348">Если **/PUBLISHING_SERVER** не используется, этот параметр будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="52cb3-348">If **/PUBLISHING_SERVER** is not used, this parameter will be ignored.</span></span> |
| <span data-ttu-id="52cb3-349">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-349">/PUBLISHING_WEBSITE_NAME</span></span> | <span data-ttu-id="52cb3-350">Указывает имя веб-сайта, который будет создан для службы публикации.</span><span class="sxs-lookup"><span data-stu-id="52cb3-350">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="52cb3-351">Пример использования: **/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing Service"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-351">Example usage: **/PUBLISHING_WEBSITE_NAME="Microsoft App-V Publishing Service"**</span></span> |
| <span data-ttu-id="52cb3-352">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-352">/PUBLISHING_WEBSITE_PORT</span></span> | <span data-ttu-id="52cb3-353">Указывает номер порта, используемого службой публикации.</span><span class="sxs-lookup"><span data-stu-id="52cb3-353">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="52cb3-354">Пример использования: **/PUBLISHING_WEBSITE_PORT = 83**</span><span class="sxs-lookup"><span data-stu-id="52cb3-354">Example usage: **/PUBLISHING_WEBSITE_PORT=83**</span></span> |

#### <span data-ttu-id="52cb3-355">Параметры сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="52cb3-355">Parameters for Reporting Server</span></span>

| <span data-ttu-id="52cb3-356">Параметр</span><span class="sxs-lookup"><span data-stu-id="52cb3-356">Parameter</span></span> | <span data-ttu-id="52cb3-357">Сведения</span><span class="sxs-lookup"><span data-stu-id="52cb3-357">Information</span></span> |
|--|--|
| <span data-ttu-id="52cb3-358">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="52cb3-358">/REPORTING_SERVER</span></span> | <span data-ttu-id="52cb3-359">Указывает, что сервер отчетов будет установлен.</span><span class="sxs-lookup"><span data-stu-id="52cb3-359">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="52cb3-360">Значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="52cb3-360">No value is expected.</span></span> |
| <span data-ttu-id="52cb3-361">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-361">/REPORTING_WEBSITE_NAME</span></span> | <span data-ttu-id="52cb3-362">Указывает имя веб-сайта, который будет создан для службы отчетов.</span><span class="sxs-lookup"><span data-stu-id="52cb3-362">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="52cb3-363">Пример использования: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-363">Example usage: **/REPORTING_WEBSITE_NAME="Microsoft App-V ReportingService"**</span></span> |
| <span data-ttu-id="52cb3-364">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="52cb3-364">/REPORTING_WEBSITE_PORT</span></span> | <span data-ttu-id="52cb3-365">Задает номер порта, который будет использоваться службой отчетов.</span><span class="sxs-lookup"><span data-stu-id="52cb3-365">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="52cb3-366">Пример использования: **/REPORTING_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="52cb3-366">Example usage: **/REPORTING_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="52cb3-367">Параметры для использования существующей базы данных сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="52cb3-367">Parameters for using an Existing Reporting Server Database</span></span>

| <span data-ttu-id="52cb3-368">Параметр</span><span class="sxs-lookup"><span data-stu-id="52cb3-368">Parameter</span></span> | <span data-ttu-id="52cb3-369">Сведения</span><span class="sxs-lookup"><span data-stu-id="52cb3-369">Information</span></span> |
|--|--|
| <span data-ttu-id="52cb3-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="52cb3-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="52cb3-371">Указывает на то, что Microsoft SQL Server установлен на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="52cb3-371">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="52cb3-372">Параметр switched, поэтому значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="52cb3-372">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="52cb3-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="52cb3-374">Указывает имя удаленного компьютера, на котором установлен SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52cb3-374">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="52cb3-375">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="52cb3-375">Takes a string.</span></span> <span data-ttu-id="52cb3-376">Пример использования: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-376">Example usage: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="52cb3-377">EXISTING_ СОЗДАНИЕ ОТЧЕТОВ _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-377">/EXISTING_ REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="52cb3-378">Указывает на то, что используется экземпляр SQL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52cb3-378">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="52cb3-379">Параметр switched, поэтому значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="52cb3-379">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="52cb3-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="52cb3-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="52cb3-381">Указывает имя настраиваемого экземпляра SQL, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="52cb3-381">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="52cb3-382">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="52cb3-382">Takes a string.</span></span> <span data-ttu-id="52cb3-383">Пример использования: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-383">Example usage: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="52cb3-384">EXISTING_ СОЗДАНИЕ ОТЧЕТОВ _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-384">/EXISTING_ REPORTING _DB_NAME</span></span> | <span data-ttu-id="52cb3-385">Указывает имя существующей базы данных отчетов, которую следует использовать.</span><span class="sxs-lookup"><span data-stu-id="52cb3-385">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="52cb3-386">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="52cb3-386">Takes a string.</span></span> <span data-ttu-id="52cb3-387">Пример использования: **/EXISTING_REPORTING_DB_NAME = "AppVReporting"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-387">Example usage: **/EXISTING_REPORTING_DB_NAME="AppVReporting"**</span></span> |

#### <span data-ttu-id="52cb3-388">Параметры для установки базы данных сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="52cb3-388">Parameters for installing Reporting Server Database</span></span>

| <span data-ttu-id="52cb3-389">Параметр</span><span class="sxs-lookup"><span data-stu-id="52cb3-389">Parameter</span></span> | <span data-ttu-id="52cb3-390">Сведения</span><span class="sxs-lookup"><span data-stu-id="52cb3-390">Information</span></span> |
|--|--|
| <span data-ttu-id="52cb3-391">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="52cb3-391">/DB_PREDEPLOY_REPORTING</span></span> | <span data-ttu-id="52cb3-392">Указывает, что база данных отчетов будет установлена.</span><span class="sxs-lookup"><span data-stu-id="52cb3-392">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="52cb3-393">Для этой установки требуются разрешения администратора баз данных.</span><span class="sxs-lookup"><span data-stu-id="52cb3-393">DBA permissions are required for this installation.</span></span> <span data-ttu-id="52cb3-394">Значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="52cb3-394">No value is expected.</span></span> |
| <span data-ttu-id="52cb3-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="52cb3-396">Указывает имя настраиваемого экземпляра SQL, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="52cb3-396">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="52cb3-397">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="52cb3-397">Takes a string.</span></span> <span data-ttu-id="52cb3-398">Пример использования: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-398">Example usage: **/REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="52cb3-399">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-399">/REPORTING_DB_NAME</span></span> | <span data-ttu-id="52cb3-400">Указывает имя новой базы данных отчетов, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="52cb3-400">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="52cb3-401">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="52cb3-401">Takes a string.</span></span> <span data-ttu-id="52cb3-402">Пример использования: **/REPORTING_DB_NAME = "AppVMgmtDB"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-402">Example usage: **/REPORTING_DB_NAME="AppVMgmtDB"**</span></span> |
| <span data-ttu-id="52cb3-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="52cb3-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="52cb3-404">Указывает на то, что сервер отчетов, на котором будет выполняться доступ к базе данных, установлен на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="52cb3-404">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="52cb3-405">Параметр switched, поэтому значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="52cb3-405">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="52cb3-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="52cb3-407">Указывает учетную запись компьютера на удаленном компьютере, на котором будет установлен сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="52cb3-407">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="52cb3-408">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="52cb3-408">Takes a string.</span></span> <span data-ttu-id="52cb3-409">Пример использования: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-409">Example usage: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="domain\computername"**</span></span> |
| <span data-ttu-id="52cb3-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="52cb3-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="52cb3-411">Указывает учетную запись администратора, которая будет использоваться для установки сервера отчетов App-V.</span><span class="sxs-lookup"><span data-stu-id="52cb3-411">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="52cb3-412">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="52cb3-412">Takes a string.</span></span> <span data-ttu-id="52cb3-413">Пример использования: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-413">Example usage: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="domain\\alias"**</span></span> |

#### <span data-ttu-id="52cb3-414">Параметры для использования существующей базы данных сервера управления</span><span class="sxs-lookup"><span data-stu-id="52cb3-414">Parameters for using an existing Management Server Database</span></span>

| <span data-ttu-id="52cb3-415">Параметр</span><span class="sxs-lookup"><span data-stu-id="52cb3-415">Parameter</span></span> | <span data-ttu-id="52cb3-416">Сведения</span><span class="sxs-lookup"><span data-stu-id="52cb3-416">Information</span></span> |
|--|--|
| <span data-ttu-id="52cb3-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="52cb3-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="52cb3-418">Указывает на то, что сервер SQL Server установлен на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="52cb3-418">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="52cb3-419">Параметр switched, поэтому значение не ожидается. Если указан **/DB_PREDEPLOY_MANAGEMENT** , это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="52cb3-419">Switch parameter so no value is expected.If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="52cb3-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="52cb3-421">Указывает имя удаленного компьютера, на котором установлен SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52cb3-421">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="52cb3-422">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="52cb3-422">Takes a string.</span></span> <span data-ttu-id="52cb3-423">Пример использования: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="52cb3-423">Example usage: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="52cb3-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52cb3-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="52cb3-425">Указывает на то, что используется экземпляр SQL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52cb3-425">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="52cb3-426">Параметр switched, поэтому значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="52cb3-426">Switch parameter so no value is expected.</span></span> <span data-ttu-id="52cb3-427">Если указан **/DB_PREDEPLOY_MANAGEMENT** , это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="52cb3-427">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="52cb3-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="52cb3-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="52cb3-429">Указывает имя настраиваемого экземпляра SQL, который будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="52cb3-429">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="52cb3-430">Пример использования **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**.</span><span class="sxs-lookup"><span data-stu-id="52cb3-430">Example usage **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="AppVManagement"**.</span></span> <span data-ttu-id="52cb3-431">Если указан **/DB_PREDEPLOY_MANAGEMENT** , это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="52cb3-431">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="52cb3-432">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="52cb3-432">/EXISTING_MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="52cb3-433">Указывает имя существующей базы данных управления, которую следует использовать.</span><span class="sxs-lookup"><span data-stu-id="52cb3-433">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="52cb3-434">Пример использования: **/EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB"**.</span><span class="sxs-lookup"><span data-stu-id="52cb3-434">Example usage: **/EXISTING_MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="52cb3-435">Если указан **/DB_PREDEPLOY_MANAGEMENT** , это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="52cb3-435">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |

<span data-ttu-id="52cb3-436">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="52cb3-436">Got an App-V issue?</span></span> <span data-ttu-id="52cb3-437">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="52cb3-437">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="52cb3-438">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="52cb3-438">Related topics</span></span>

[<span data-ttu-id="52cb3-439">Развертывание сервера App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="52cb3-439">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)
