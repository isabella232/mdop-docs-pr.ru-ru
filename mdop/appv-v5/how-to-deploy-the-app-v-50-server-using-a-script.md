---
title: Развертывание сервера App-V 5.0 с помощью сценария
description: Развертывание сервера App-V 5.0 с помощью сценария
author: dansimp
ms.assetid: b91a35c8-df9e-4065-9187-abafbe565b84
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: aeb16d166fe7b1c4bb418c212024c49f6b151b94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814168"
---
# <span data-ttu-id="35aac-103">Развертывание сервера App-V 5.0 с помощью сценария</span><span class="sxs-lookup"><span data-stu-id="35aac-103">How to Deploy the App-V 5.0 Server Using a Script</span></span>


<span data-ttu-id="35aac-104">Для того чтобы завершить настройку сервера **appv\_server\_setup.exe** успешно использовать командную строку, необходимо указать и объединить несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="35aac-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

<span data-ttu-id="35aac-105">Чтобы получить дополнительные сведения об установке App-V 5,0 Server с помощью командной строки, воспользуйтесь приведенными ниже таблицами.</span><span class="sxs-lookup"><span data-stu-id="35aac-105">Use the following tables for more information about installing the App-V 5.0 server using the command line.</span></span>

>[!NOTE]
> <span data-ttu-id="35aac-106">Сведения из приведенных ниже таблиц также можно вызвать с помощью командной строки, введя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="35aac-106">The information in the following tables can also be accessed using the command line by typing the following command:</span></span>
>```
> appv\_server\_setup.exe /?
>```

## <span data-ttu-id="35aac-107">Общие параметры и примеры</span><span class="sxs-lookup"><span data-stu-id="35aac-107">Common parameters and Examples</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-108">Установка сервера управления и базы данных управления на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="35aac-108">To Install the Management server and Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-109">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="35aac-109">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-110">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-111">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-112">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-113">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="35aac-114">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-116">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-117">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="35aac-117">To use a custom instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-118">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-118">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-119">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-119">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-120">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-120">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-121">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-121">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-122">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="35aac-122">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="35aac-124">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-124">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-125">Пример использования настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-125">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="35aac-126">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="35aac-126">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="35aac-127">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-127">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="35aac-128">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="35aac-128">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="35aac-129">/MANAGEMENT_WEBSITE_NAME = "Служба управления Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="35aac-129">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="35aac-130">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="35aac-130">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="35aac-131">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="35aac-131">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="35aac-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="35aac-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="35aac-133">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="35aac-133">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>
     
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-134">Установка сервера управления с помощью существующей базы данных управления на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="35aac-134">To Install the Management server using an existing Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-135">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="35aac-135">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-136">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-136">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-137">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-137">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-138">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-138">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-139">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-139">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="35aac-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-142">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-142">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-143">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="35aac-143">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-144">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-144">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-145">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-145">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-146">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-146">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-147">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-147">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="35aac-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="35aac-150">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-150">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-151">Пример использования настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-151">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="35aac-152">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="35aac-152">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="35aac-153">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-153">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="35aac-154">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="35aac-154">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="35aac-155">/MANAGEMENT_WEBSITE_NAME = "Служба управления Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="35aac-155">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="35aac-156">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="35aac-156">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="35aac-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="35aac-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="35aac-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="35aac-159">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="35aac-159">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>  

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-160">Установка сервера управления с помощью существующей базы данных управления на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="35aac-160">To install the Management server using an existing Management database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-161">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="35aac-161">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-162">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-162">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-163">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-163">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-164">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-164">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-165">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-165">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-168">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-168">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-169">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="35aac-169">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-170">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-170">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-171">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-171">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-172">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-172">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-173">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-173">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="35aac-176">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-176">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-177">Пример использования настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-177">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="35aac-178">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="35aac-178">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="35aac-179">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-179">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="35aac-180">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="35aac-180">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="35aac-181">/MANAGEMENT_WEBSITE_NAME = "Служба управления Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="35aac-181">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="35aac-182">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="35aac-182">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="35aac-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "SqlServermachine. имя_домена"</span><span class="sxs-lookup"><span data-stu-id="35aac-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME=”SqlServermachine.domainName”</span></span></p>
    <p><span data-ttu-id="35aac-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="35aac-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="35aac-185">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="35aac-185">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-186">Установка базы данных управления и сервера управления на одном и том же компьютере.</span><span class="sxs-lookup"><span data-stu-id="35aac-186">To Install the Management database and the Management Server on the same computer.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-187">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="35aac-187">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-188">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="35aac-188">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-190">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-190">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="35aac-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-193">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="35aac-193">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-194">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="35aac-194">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="35aac-196">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-196">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="35aac-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-199">Пример использования настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-199">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="35aac-200">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="35aac-200">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="35aac-201">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="35aac-201">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="35aac-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="35aac-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="35aac-203">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="35aac-203">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="35aac-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="35aac-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="35aac-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-206">Чтобы установить базу данных управления на компьютере, отличном от сервера управления.</span><span class="sxs-lookup"><span data-stu-id="35aac-206">To install the Management database on a different computer than the Management server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-207">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="35aac-207">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-208">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="35aac-208">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-210">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-210">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-213">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="35aac-213">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-214">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="35aac-214">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="35aac-216">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-216">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-219">Пример использования настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-219">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="35aac-220">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="35aac-220">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="35aac-221">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="35aac-221">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="35aac-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="35aac-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="35aac-223">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="35aac-223">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="35aac-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="35aac-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="35aac-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="35aac-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-226">Установка сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="35aac-226">To Install the publishing server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-227">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="35aac-227">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-228">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-228">/PUBLISHING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-229">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-229">/PUBLISHING_MGT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-230">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-230">/PUBLISHING_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-231">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-231">/PUBLISHING_WEBSITE_PORT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-232">Пример использования настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-232">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="35aac-233">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="35aac-233">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="35aac-234">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-234">/PUBLISHING_SERVER</span></span></p>
    <p><span data-ttu-id="35aac-235">/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</span><span class="sxs-lookup"><span data-stu-id="35aac-235">/PUBLISHING_MGT_SERVER=”http://ManagementServerName:ManagementPort”</span></span></p>
    <p><span data-ttu-id="35aac-236">/PUBLISHING_WEBSITE_NAME = "Служба публикации Microsoft AppV Service"</span><span class="sxs-lookup"><span data-stu-id="35aac-236">/PUBLISHING_WEBSITE_NAME=”Microsoft AppV Publishing Service”</span></span></p>
    <p><span data-ttu-id="35aac-237">/PUBLISHING_WEBSITE_PORT = "8081"</span><span class="sxs-lookup"><span data-stu-id="35aac-237">/PUBLISHING_WEBSITE_PORT=”8081”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-238">Установка сервера отчетов и базы данных отчетов на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="35aac-238">To Install the Reporting server and Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-239">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="35aac-239">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-240">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-240">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-241">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-241">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-242">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-242">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-243">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="35aac-243">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="35aac-244">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-244">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-245">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-245">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-246">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="35aac-246">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-247">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-247">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-248">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-248">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-249">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-249">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-250">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-250">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-251">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="35aac-251">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="35aac-252">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-252">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="35aac-253">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-253">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-254">Пример использования настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-254">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-255">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="35aac-255">/appv_server_setup.exe /QUIET</span></span></p></li>
    <li><p><span data-ttu-id="35aac-256">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-256">/REPORTING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-257">/REPORTING_WEBSITE_NAME = "Служба Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="35aac-257">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p></li>
    <li><p><span data-ttu-id="35aac-258">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="35aac-258">/REPORTING_WEBSITE_PORT=”8082”</span></span></p></li>
    <li><p><span data-ttu-id="35aac-259">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="35aac-259">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="35aac-260">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="35aac-260">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p></li>
    <li><p><span data-ttu-id="35aac-261">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="35aac-261">/REPORTING_DB_NAME=”AppVReporting”</span></span></p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-262">Установка сервера отчетов и использование существующей базы данных отчетов на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="35aac-262">To Install the Reporting server and using an existing Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-263">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="35aac-263">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-264">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-264">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-265">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-265">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-266">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-266">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="35aac-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-269">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-269">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-270">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="35aac-270">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-271">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-271">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-272">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-272">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-273">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-273">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-274">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-274">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="35aac-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="35aac-277">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-277">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-278">Пример использования настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-278">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="35aac-279">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="35aac-279">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="35aac-280">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-280">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="35aac-281">/REPORTING_WEBSITE_NAME = "Служба Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="35aac-281">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="35aac-282">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="35aac-282">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="35aac-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="35aac-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="35aac-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="35aac-285">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="35aac-285">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-286">Установка сервера отчетов с помощью существующей базы данных отчетов на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="35aac-286">To Install the Reporting server using an existing Reporting database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-287">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="35aac-287">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-288">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-288">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-289">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-289">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-290">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-290">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-293">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-293">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-294">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="35aac-294">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-295">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-295">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="35aac-296">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-296">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-297">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-297">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-298">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-298">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="35aac-301">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-301">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-302">Пример использования настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-302">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="35aac-303">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="35aac-303">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="35aac-304">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-304">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="35aac-305">/REPORTING_WEBSITE_NAME = "Служба Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="35aac-305">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="35aac-306">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="35aac-306">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="35aac-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "SqlServerMachine. имя_домена"</span><span class="sxs-lookup"><span data-stu-id="35aac-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME=”SqlServerMachine.DomainName”</span></span></p>
    <p><span data-ttu-id="35aac-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="35aac-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="35aac-309">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="35aac-309">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-310">Чтобы установить базу данных отчетов на том же компьютере, что и сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="35aac-310">To install the Reporting database on the same computer as the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-311">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="35aac-311">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-312">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="35aac-312">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="35aac-313">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-313">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-314">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-314">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="35aac-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-317">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="35aac-317">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-318">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="35aac-318">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="35aac-319">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-319">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="35aac-320">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-320">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="35aac-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-323">Пример использования настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-323">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="35aac-324">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="35aac-324">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="35aac-325">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="35aac-325">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="35aac-326">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="35aac-326">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="35aac-327">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="35aac-327">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="35aac-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="35aac-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="35aac-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-330">Чтобы установить базу данных отчетов на компьютере, отличном от сервера отчетов.</span><span class="sxs-lookup"><span data-stu-id="35aac-330">To install the Reporting database on a different computer than the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-331">Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="35aac-331">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-332">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="35aac-332">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="35aac-333">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-333">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-334">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-334">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-337">Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="35aac-337">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="35aac-338">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="35aac-338">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="35aac-339">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-339">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="35aac-340">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-340">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="35aac-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="35aac-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="35aac-343">Пример использования настраиваемого экземпляра Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-343">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="35aac-344">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="35aac-344">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="35aac-345">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="35aac-345">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="35aac-346">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="35aac-346">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="35aac-347">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="35aac-347">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="35aac-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="35aac-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="35aac-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="35aac-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

## <span data-ttu-id="35aac-350">Определения параметров</span><span class="sxs-lookup"><span data-stu-id="35aac-350">Parameter Definitions</span></span>

### <span data-ttu-id="35aac-351">Общие параметры</span><span class="sxs-lookup"><span data-stu-id="35aac-351">General Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="35aac-352">Параметр</span><span class="sxs-lookup"><span data-stu-id="35aac-352">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="35aac-353">Сведения</span><span class="sxs-lookup"><span data-stu-id="35aac-353">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-354">Параметрами</span><span class="sxs-lookup"><span data-stu-id="35aac-354">/QUIET</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-355">Указывает на автоматическую установку.</span><span class="sxs-lookup"><span data-stu-id="35aac-355">Specifies silent install.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-356">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="35aac-356">/UNINSTALL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-357">Указывает на удаление.</span><span class="sxs-lookup"><span data-stu-id="35aac-357">Specifies an uninstall.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-358">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="35aac-358">/LAYOUT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-359">Задает действие макета.</span><span class="sxs-lookup"><span data-stu-id="35aac-359">Specifies layout action.</span></span> <span data-ttu-id="35aac-360">Файлы MSI и Script будут извлечены в папку без фактического их установки.</span><span class="sxs-lookup"><span data-stu-id="35aac-360">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="35aac-361">Значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="35aac-361">No value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-362">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="35aac-362">/LAYOUTDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-363">Указывает каталог макета.</span><span class="sxs-lookup"><span data-stu-id="35aac-363">Specifies the layout directory.</span></span> <span data-ttu-id="35aac-364">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="35aac-364">Takes a string.</span></span> <span data-ttu-id="35aac-365">Например,/LAYOUTDIR = "сервер виртуализации C:\Application"</span><span class="sxs-lookup"><span data-stu-id="35aac-365">For example, /LAYOUTDIR=”C:\Application Virtualization Server”</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-366">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="35aac-366">/INSTALLDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-367">Указывает каталог установки.</span><span class="sxs-lookup"><span data-stu-id="35aac-367">Specifies the installation directory.</span></span> <span data-ttu-id="35aac-368">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="35aac-368">Takes a string.</span></span> <span data-ttu-id="35aac-369">Например:</span><span class="sxs-lookup"><span data-stu-id="35aac-369">E.g.</span></span> <span data-ttu-id="35aac-370">/INSTALLDIR = "C:\Program Files\Application Virtualization\Server"</span><span class="sxs-lookup"><span data-stu-id="35aac-370">/INSTALLDIR=”C:\Program Files\Application Virtualization\Server”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-371">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="35aac-371">/MUOPTIN</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-372">Включение центра обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="35aac-372">Enables Microsoft Update.</span></span> <span data-ttu-id="35aac-373">Значение не ожидается</span><span class="sxs-lookup"><span data-stu-id="35aac-373">No value is expected</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-374">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="35aac-374">/ACCEPTEULA</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-375">Принимает лицензионное соглашение.</span><span class="sxs-lookup"><span data-stu-id="35aac-375">Accepts the license agreement.</span></span> <span data-ttu-id="35aac-376">Это необходимо для автоматической установки.</span><span class="sxs-lookup"><span data-stu-id="35aac-376">This is required for an unattended installation.</span></span> <span data-ttu-id="35aac-377">Пример использования: <strong> /ACCEPTEULA </strong> или <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="35aac-377">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="35aac-378">Параметры установки сервера управления</span><span class="sxs-lookup"><span data-stu-id="35aac-378">Management Server Installation Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="35aac-379">Параметр</span><span class="sxs-lookup"><span data-stu-id="35aac-379">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="35aac-380">Сведения</span><span class="sxs-lookup"><span data-stu-id="35aac-380">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-381">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-381">/MANAGEMENT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-382">Указывает, что сервер управления будет установлен.</span><span class="sxs-lookup"><span data-stu-id="35aac-382">Specifies that the management server will be installed.</span></span> <span data-ttu-id="35aac-383">Значение не ожидается</span><span class="sxs-lookup"><span data-stu-id="35aac-383">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-384">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-384">/MANAGEMENT_ADMINACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-385">Указывает учетную запись, которой будет разрешено администратору получить доступ к серверу управления. Эта учетная запись может быть отдельной учетной записью пользователя или группой.</span><span class="sxs-lookup"><span data-stu-id="35aac-385">Specifies the account that will be allowed to Administrator access to the management server This account can be an individual user account or a group.</span></span> <span data-ttu-id="35aac-386">Пример использования: <strong> /MANAGEMENT_ADMINACCOUNT = "mydomain\admin" </strong> .</span><span class="sxs-lookup"><span data-stu-id="35aac-386">Example usage: <strong>/MANAGEMENT_ADMINACCOUNT=”mydomain\admin”</strong>.</span></span> <span data-ttu-id="35aac-387">Если <strong> </strong> не задано/MANAGEMENT_SERVER, это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="35aac-387">If <strong>/MANAGEMENT_SERVER</strong> is not specified, this will be ignored.</span></span> <span data-ttu-id="35aac-388">Указывает учетную запись, которой будет разрешено администратору получить доступ к серверу управления.</span><span class="sxs-lookup"><span data-stu-id="35aac-388">Specifies the account that will be allowed to Administrator access to the management server.</span></span> <span data-ttu-id="35aac-389">Это может быть учетная запись пользователя или группа.</span><span class="sxs-lookup"><span data-stu-id="35aac-389">This can be a user account or a group.</span></span> <span data-ttu-id="35aac-390">Например, <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</span><span class="sxs-lookup"><span data-stu-id="35aac-390">For example, <strong>/MANAGEMENT_ADMINACCOUNT=&quot;mydomain\admin&quot;</strong>.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-391">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-391">/MANAGEMENT_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-392">Указывает имя веб-сайта, который будет создан для службы управления.</span><span class="sxs-lookup"><span data-stu-id="35aac-392">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="35aac-393">Например,/MANAGEMENT_WEBSITE_NAME = "Служба управления Microsoft App-V"</span><span class="sxs-lookup"><span data-stu-id="35aac-393">For example, /MANAGEMENT_WEBSITE_NAME=”Microsoft App-V Management Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-394">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-394">MANAGEMENT_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-395">Указывает номер порта, который будет использоваться службой управления.</span><span class="sxs-lookup"><span data-stu-id="35aac-395">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="35aac-396">Например,/MANAGEMENT_WEBSITE_PORT = 82.</span><span class="sxs-lookup"><span data-stu-id="35aac-396">For example, /MANAGEMENT_WEBSITE_PORT=82.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="35aac-397">Параметры для базы данных сервера управления</span><span class="sxs-lookup"><span data-stu-id="35aac-397">Parameters for the Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="35aac-398">Параметр</span><span class="sxs-lookup"><span data-stu-id="35aac-398">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="35aac-399">Сведения</span><span class="sxs-lookup"><span data-stu-id="35aac-399">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-400">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="35aac-400">/DB_PREDEPLOY_MANAGEMENT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-401">Указывает, что база данных управления будет установлена.</span><span class="sxs-lookup"><span data-stu-id="35aac-401">Specifies that the management database will be installed.</span></span> <span data-ttu-id="35aac-402">Чтобы завершить установку, необходимо иметь разрешения, достаточные для базы данных.</span><span class="sxs-lookup"><span data-stu-id="35aac-402">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="35aac-403">Значение не ожидается</span><span class="sxs-lookup"><span data-stu-id="35aac-403">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-405">Указывает, что необходимо использовать экземпляр SQL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="35aac-405">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="35aac-406">Значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="35aac-406">No value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-408">Указывает имя настраиваемого экземпляра SQL, который должен использоваться для создания новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="35aac-408">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="35aac-409">Пример использования: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER" </strong> .</span><span class="sxs-lookup"><span data-stu-id="35aac-409">Example usage: <strong>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”MYSQLSERVER”</strong>.</span></span> <span data-ttu-id="35aac-410">Если не задано/DB_PREDEPLOY_MANAGEMENT, это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="35aac-410">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-411">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-411">/MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-412">Указывает имя новой базы данных управления, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="35aac-412">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="35aac-413">Пример использования: <strong> /MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> .</span><span class="sxs-lookup"><span data-stu-id="35aac-413">Example usage: <strong>/MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="35aac-414">Если не задано/DB_PREDEPLOY_MANAGEMENT, это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="35aac-414">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-416">Указывает, установлен ли на локальном сервере сервер управления, который будет получать доступ к базе данных.</span><span class="sxs-lookup"><span data-stu-id="35aac-416">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="35aac-417">Параметр switched, поэтому значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="35aac-417">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-419">Учетная запись удаленного компьютера, на котором будет установлен сервер управления.</span><span class="sxs-lookup"><span data-stu-id="35aac-419">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="35aac-420">Пример использования: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"</span><span class="sxs-lookup"><span data-stu-id="35aac-420">Example usage: <strong>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”domain\computername”</span></span></strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-422">Учетная запись администратора, которая будет использоваться для установки сервера управления.</span><span class="sxs-lookup"><span data-stu-id="35aac-422">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="35aac-423">Пример использования: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\alias"</span><span class="sxs-lookup"><span data-stu-id="35aac-423">Example usage: <strong>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT =”domain\alias”</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="35aac-424">Параметры для установки сервера публикаций</span><span class="sxs-lookup"><span data-stu-id="35aac-424">Parameters for Installing Publishing Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="35aac-425">Параметр</span><span class="sxs-lookup"><span data-stu-id="35aac-425">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="35aac-426">Сведения</span><span class="sxs-lookup"><span data-stu-id="35aac-426">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-427">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-427">/PUBLISHING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-428">Указывает, что сервер публикаций будет установлен.</span><span class="sxs-lookup"><span data-stu-id="35aac-428">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="35aac-429">Значение не ожидается</span><span class="sxs-lookup"><span data-stu-id="35aac-429">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-430">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-430">/PUBLISHING_MGT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-431">Указывает URL-адрес службы управления, к которой будет подключаться сервер публикации.</span><span class="sxs-lookup"><span data-stu-id="35aac-431">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="35aac-432">Пример использования: <strong> &lt; имя сервера управления http:// &gt; : &lt; номер порта сервера управления &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="35aac-432">Example usage: <strong>http://&lt;management server name&gt;:&lt;Management server port number&gt;</strong>.</span></span> <span data-ttu-id="35aac-433">Если/PUBLISHING_SERVER не используется, этот параметр будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="35aac-433">If /PUBLISHING_SERVER is not used, this parameter will be ignored</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-434">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-434">/PUBLISHING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-435">Указывает имя веб-сайта, который будет создан для службы публикации.</span><span class="sxs-lookup"><span data-stu-id="35aac-435">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="35aac-436">Например,/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing Service"</span><span class="sxs-lookup"><span data-stu-id="35aac-436">For example, /PUBLISHING_WEBSITE_NAME=”Microsoft App-V Publishing Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-437">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-437">/PUBLISHING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-438">Указывает номер порта, используемого службой публикации.</span><span class="sxs-lookup"><span data-stu-id="35aac-438">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="35aac-439">Например,/PUBLISHING_WEBSITE_PORT = 83</span><span class="sxs-lookup"><span data-stu-id="35aac-439">For example, /PUBLISHING_WEBSITE_PORT=83</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="35aac-440">Параметры сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="35aac-440">Parameters for Reporting Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="35aac-441">Параметр</span><span class="sxs-lookup"><span data-stu-id="35aac-441">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="35aac-442">Сведения</span><span class="sxs-lookup"><span data-stu-id="35aac-442">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-443">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="35aac-443">/REPORTING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-444">Указывает, что сервер отчетов будет установлен.</span><span class="sxs-lookup"><span data-stu-id="35aac-444">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="35aac-445">Значение не ожидается</span><span class="sxs-lookup"><span data-stu-id="35aac-445">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-446">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-446">/REPORTING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-447">Указывает имя веб-сайта, который будет создан для службы отчетов.</span><span class="sxs-lookup"><span data-stu-id="35aac-447">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="35aac-448">Например:</span><span class="sxs-lookup"><span data-stu-id="35aac-448">E.g.</span></span> <span data-ttu-id="35aac-449">/REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</span><span class="sxs-lookup"><span data-stu-id="35aac-449">/REPORTING_WEBSITE_NAME=&quot;Microsoft App-V ReportingService&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-450">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="35aac-450">/REPORTING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-451">Задает номер порта, который будет использоваться службой отчетов.</span><span class="sxs-lookup"><span data-stu-id="35aac-451">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="35aac-452">Например:</span><span class="sxs-lookup"><span data-stu-id="35aac-452">E.g.</span></span> <span data-ttu-id="35aac-453">/REPORTING_WEBSITE_PORT = 82</span><span class="sxs-lookup"><span data-stu-id="35aac-453">/REPORTING_WEBSITE_PORT=82</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

### <span data-ttu-id="35aac-454">Параметры для использования существующей базы данных сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="35aac-454">Parameters for using an Existing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="35aac-455">Параметр</span><span class="sxs-lookup"><span data-stu-id="35aac-455">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="35aac-456">Сведения</span><span class="sxs-lookup"><span data-stu-id="35aac-456">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-458">Указывает на то, что Microsoft SQL Server установлен на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="35aac-458">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="35aac-459">Параметр switched, поэтому значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="35aac-459">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-461">Указывает имя удаленного компьютера, на котором установлен SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-461">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="35aac-462">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="35aac-462">Takes a string.</span></span> <span data-ttu-id="35aac-463">Например:</span><span class="sxs-lookup"><span data-stu-id="35aac-463">E.g.</span></span> <span data-ttu-id="35aac-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="35aac-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-465">EXISTING_ создание отчетов <em> DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-465">/EXISTING_ REPORTING <em>DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-466">Указывает на то, что используется экземпляр SQL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="35aac-466">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="35aac-467">Параметр switched, поэтому значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="35aac-467">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-468">/EXISTING </em> REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-468">/EXISTING</em> REPORTING_DB_CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-469">Указывает имя настраиваемого экземпляра SQL, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="35aac-469">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="35aac-470">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="35aac-470">Takes a string.</span></span> <span data-ttu-id="35aac-471">Например:</span><span class="sxs-lookup"><span data-stu-id="35aac-471">E.g.</span></span> <span data-ttu-id="35aac-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYSQLSERVER&quot;</span><span class="sxs-lookup"><span data-stu-id="35aac-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-473">EXISTING_ СОЗДАНИЕ ОТЧЕТОВ _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-473">/EXISTING_ REPORTING _DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-474">Указывает имя существующей базы данных отчетов, которую следует использовать.</span><span class="sxs-lookup"><span data-stu-id="35aac-474">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="35aac-475">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="35aac-475">Takes a string.</span></span> <span data-ttu-id="35aac-476">Например:</span><span class="sxs-lookup"><span data-stu-id="35aac-476">E.g.</span></span> <span data-ttu-id="35aac-477">/EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</span><span class="sxs-lookup"><span data-stu-id="35aac-477">/EXISTING_REPORTING_DB_NAME=&quot;AppVReporting&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="35aac-478">Параметры для установки базы данных сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="35aac-478">Parameters for installing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="35aac-479">Параметр</span><span class="sxs-lookup"><span data-stu-id="35aac-479">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="35aac-480">Сведения</span><span class="sxs-lookup"><span data-stu-id="35aac-480">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-481">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="35aac-481">/DB_PREDEPLOY_REPORTING</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-482">Указывает, что база данных отчетов будет установлена.</span><span class="sxs-lookup"><span data-stu-id="35aac-482">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="35aac-483">Для этой установки требуются разрешения администратора баз данных.</span><span class="sxs-lookup"><span data-stu-id="35aac-483">DBA permissions are required for this installation.</span></span> <span data-ttu-id="35aac-484">Значение не ожидается</span><span class="sxs-lookup"><span data-stu-id="35aac-484">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-486">Указывает имя настраиваемого экземпляра SQL, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="35aac-486">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="35aac-487">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="35aac-487">Takes a string.</span></span> <span data-ttu-id="35aac-488">Например:</span><span class="sxs-lookup"><span data-stu-id="35aac-488">E.g.</span></span> <span data-ttu-id="35aac-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYSQLSERVER&quot;</span><span class="sxs-lookup"><span data-stu-id="35aac-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-490">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-490">/REPORTING_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-491">Указывает имя новой базы данных отчетов, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="35aac-491">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="35aac-492">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="35aac-492">Takes a string.</span></span> <span data-ttu-id="35aac-493">Например:</span><span class="sxs-lookup"><span data-stu-id="35aac-493">E.g.</span></span> <span data-ttu-id="35aac-494">/REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</span><span class="sxs-lookup"><span data-stu-id="35aac-494">/REPORTING_DB_NAME=&quot;AppVMgmtDB&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-496">Указывает на то, что сервер отчетов, на котором будет выполняться доступ к базе данных, установлен на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="35aac-496">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="35aac-497">Параметр switched, поэтому значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="35aac-497">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-499">Указывает учетную запись компьютера на удаленном компьютере, на котором будет установлен сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="35aac-499">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="35aac-500">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="35aac-500">Takes a string.</span></span> <span data-ttu-id="35aac-501">Например:</span><span class="sxs-lookup"><span data-stu-id="35aac-501">E.g.</span></span> <span data-ttu-id="35aac-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; DOMAIN\COMPUTERNAME&quot;</span><span class="sxs-lookup"><span data-stu-id="35aac-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot;domain\computername&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="35aac-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-504">Указывает учетную запись администратора, которая будет использоваться для установки сервера отчетов App-V.</span><span class="sxs-lookup"><span data-stu-id="35aac-504">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="35aac-505">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="35aac-505">Takes a string.</span></span> <span data-ttu-id="35aac-506">Например:</span><span class="sxs-lookup"><span data-stu-id="35aac-506">E.g.</span></span> <span data-ttu-id="35aac-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; domain\alias&quot;</span><span class="sxs-lookup"><span data-stu-id="35aac-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot;domain\alias&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="35aac-508">Параметры для использования существующей базы данных сервера управления</span><span class="sxs-lookup"><span data-stu-id="35aac-508">Parameters for using an existing Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="35aac-509">Параметр</span><span class="sxs-lookup"><span data-stu-id="35aac-509">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="35aac-510">Сведения</span><span class="sxs-lookup"><span data-stu-id="35aac-510">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="35aac-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-512">Указывает на то, что сервер SQL Server установлен на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="35aac-512">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="35aac-513">Параметр switched, поэтому значение не ожидается. Если указан/DB_PREDEPLOY_MANAGEMENT, это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="35aac-513">Switch parameter so no value is expected.If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-515">Указывает имя удаленного компьютера, на котором установлен SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35aac-515">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="35aac-516">Принимает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="35aac-516">Takes a string.</span></span> <span data-ttu-id="35aac-517">Например:</span><span class="sxs-lookup"><span data-stu-id="35aac-517">E.g.</span></span> <span data-ttu-id="35aac-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="35aac-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="35aac-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-520">Указывает на то, что используется экземпляр SQL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="35aac-520">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="35aac-521">Параметр switched, поэтому значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="35aac-521">Switch parameter so no value is expected.</span></span> <span data-ttu-id="35aac-522">Если указан/DB_PREDEPLOY_MANAGEMENT, это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="35aac-522">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="35aac-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="35aac-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-524">Указывает имя настраиваемого экземпляра SQL, который будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="35aac-524">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="35aac-525">Пример использования <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> .</span><span class="sxs-lookup"><span data-stu-id="35aac-525">Example usage <strong>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”AppVManagement”</strong>.</span></span> <span data-ttu-id="35aac-526">Если указан/DB_PREDEPLOY_MANAGEMENT, это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="35aac-526">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="35aac-527">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="35aac-527">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="35aac-528">Указывает имя существующей базы данных управления, которую следует использовать.</span><span class="sxs-lookup"><span data-stu-id="35aac-528">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="35aac-529">Пример использования: <strong> /EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> .</span><span class="sxs-lookup"><span data-stu-id="35aac-529">Example usage: <strong>/EXISTING_MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="35aac-530">Если указан/DB_PREDEPLOY_MANAGEMENT, это будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="35aac-530">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p>
    <p></p>
    <p><strong><span data-ttu-id="35aac-531">У вас есть предложение App-V </strong> ?</span><span class="sxs-lookup"><span data-stu-id="35aac-531">Got a suggestion for App-V</strong>?</span></span> <span data-ttu-id="35aac-532">Здесь вы можете добавить предложения и проголосовать <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> здесь </a> .</span><span class="sxs-lookup"><span data-stu-id="35aac-532">Add or vote on suggestions <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)">here</a>.</span></span> <strong><span data-ttu-id="35aac-533">У вас есть приложение-V issu </strong> e?</span><span class="sxs-lookup"><span data-stu-id="35aac-533">Got an App-V issu</strong>e?</span></span> <span data-ttu-id="35aac-534">Используйте <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)"> Форум TechNet App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="35aac-534">Use the <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)">App-V TechNet Forum</a>.</span></span></p></td>
</tr>
</tbody>
</table>
  

## <span data-ttu-id="35aac-535">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="35aac-535">Related topics</span></span>

[<span data-ttu-id="35aac-536">Развертывание сервера App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="35aac-536">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

 

 





