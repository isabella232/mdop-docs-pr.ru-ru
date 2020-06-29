---
title: Развертывание баз данных App-V с помощью сценариев SQL
description: Развертывание баз данных App-V с помощью сценариев SQL
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814112"
---
# <span data-ttu-id="1a0a4-103">Развертывание баз данных App-V с помощью сценариев SQL</span><span class="sxs-lookup"><span data-stu-id="1a0a4-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>


<span data-ttu-id="1a0a4-104">Чтобы использовать сценарии SQL, а не установщик Windows, выполните указанные ниже инструкции.</span><span class="sxs-lookup"><span data-stu-id="1a0a4-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

-   <span data-ttu-id="1a0a4-105">Установка баз данных App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1a0a4-105">Install the App-V 5.0 databases</span></span>

-   <span data-ttu-id="1a0a4-106">Обновление баз данных 5,0 до более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1a0a4-106">Upgrade the 5.0 databases to a later version</span></span>

**<span data-ttu-id="1a0a4-107">Установка баз данных App-V с помощью сценариев SQL</span><span class="sxs-lookup"><span data-stu-id="1a0a4-107">How to install the App-V databases by using SQL scripts</span></span>**

1. <span data-ttu-id="1a0a4-108">Прежде чем устанавливать сценарии базы данных, ознакомьтесь с условиями лицензионного соглашения App-V и сохраните их.</span><span class="sxs-lookup"><span data-stu-id="1a0a4-108">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="1a0a4-109">Запустив сценарии базы данных, вы соглашаетесь с условиями лицензионного соглашения.</span><span class="sxs-lookup"><span data-stu-id="1a0a4-109">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="1a0a4-110">Если вы не согласны, не используйте это программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="1a0a4-110">If you do not accept them, you should not use this software.</span></span>

2. <span data-ttu-id="1a0a4-111">Скопируйте **appv\_server\_setup.exe** из среды выпуска App-V в временное расположение.</span><span class="sxs-lookup"><span data-stu-id="1a0a4-111">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>

3. <span data-ttu-id="1a0a4-112">В командной строке запустите **appv\_server\_setup.exe** и укажите временное расположение для извлечения сценариев базы данных.</span><span class="sxs-lookup"><span data-stu-id="1a0a4-112">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

   <span data-ttu-id="1a0a4-113">Пример: appv\_server\_setup.exe/Layout c:\\ &lt; Temporary Location (путь)&gt;</span><span class="sxs-lookup"><span data-stu-id="1a0a4-113">Example: appv\_server\_setup.exe /layout c:\\&lt;temporary location path&gt;</span></span>

4. <span data-ttu-id="1a0a4-114">Перейдите к созданному временному расположению, откройте папку извлеченные **DatabaseScripts** и просмотрите инструкции в соответствующем файле Readme.txt.</span><span class="sxs-lookup"><span data-stu-id="1a0a4-114">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="1a0a4-115">База данных</span><span class="sxs-lookup"><span data-stu-id="1a0a4-115">Database</span></span></th>
   <th align="left"><span data-ttu-id="1a0a4-116">Расположение используемого файла Readme.txt</span><span class="sxs-lookup"><span data-stu-id="1a0a4-116">Location of Readme.txt file to use</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="1a0a4-117">База данных управления</span><span class="sxs-lookup"><span data-stu-id="1a0a4-117">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1a0a4-118">Вложенная папка ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="1a0a4-118">ManagementDatabase subfolder</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="1a0a4-119">Важно.</span><span class="sxs-lookup"><span data-stu-id="1a0a4-119">Important</span></span></strong><br/><p><span data-ttu-id="1a0a4-120">Если вы обновляете или устанавливаете базу данных управления App-V 5,0 SP3, ознакомьтесь со <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> сценариями SQL для установки или обновления базы данных сервера управления для App-v 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="1a0a4-120">If you are upgrading to or installing the App-V 5.0 SP3 Management database, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="1a0a4-121">База данных отчетов</span><span class="sxs-lookup"><span data-stu-id="1a0a4-121">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1a0a4-122">Вложенная папка ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="1a0a4-122">ReportingDatabase subfolder</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="1a0a4-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1a0a4-123">Related topics</span></span>


[<span data-ttu-id="1a0a4-124">Развертывание сервера App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="1a0a4-124">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

[<span data-ttu-id="1a0a4-125">Порядок развертывания сервера App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="1a0a4-125">How to Deploy the App-V 5.0 Server</span></span>](how-to-deploy-the-app-v-50-server-50sp3.md)









