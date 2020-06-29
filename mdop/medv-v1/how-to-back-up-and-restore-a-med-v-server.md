---
title: Резервное копирование и восстановление сервера MED-V Server
description: Резервное копирование и восстановление сервера MED-V Server
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823089"
---
# <span data-ttu-id="d5a82-103">Резервное копирование и восстановление сервера MED-V Server</span><span class="sxs-lookup"><span data-stu-id="d5a82-103">How to Back Up and Restore a MED-V Server</span></span>


<span data-ttu-id="d5a82-104">XML-файлы, расположенные на сервере, могут быть архивированы, а затем восстановлены в случае потери данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="d5a82-104">XML files located on the server can be backed up and then restored in case of loss of data on the server.</span></span>

**<span data-ttu-id="d5a82-105">Создание резервной копии сервера MED-V</span><span class="sxs-lookup"><span data-stu-id="d5a82-105">To back up a MED-V server</span></span>**

-   <span data-ttu-id="d5a82-106">Создавайте резервные копии следующих файлов, расположенных в \* &lt; installDir &gt; \\Servers\\ConfigurationServer\*:</span><span class="sxs-lookup"><span data-stu-id="d5a82-106">Back up the following files, located in *&lt;InstallDir&gt;\\Servers\\ConfigurationServer*:</span></span>

    <span data-ttu-id="d5a82-107">**Примечание**  Если конфигурация по умолчанию была изменена, файлы могут храниться в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="d5a82-107">**Note** If the configuration has been changed from the default, the files might be stored in a different location.</span></span>

     

    -   <span data-ttu-id="d5a82-108">ClientPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="d5a82-108">ClientPolicy.xml</span></span>

    -   <span data-ttu-id="d5a82-109">ClientSettings.xml</span><span class="sxs-lookup"><span data-stu-id="d5a82-109">ClientSettings.xml</span></span>

    -   <span data-ttu-id="d5a82-110">ConfigurationFiles.xml</span><span class="sxs-lookup"><span data-stu-id="d5a82-110">ConfigurationFiles.xml</span></span>

    -   <span data-ttu-id="d5a82-111">OrganizationPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="d5a82-111">OrganizationPolicy.xml</span></span>

    -   <span data-ttu-id="d5a82-112">WorkspaceKeys.xml</span><span class="sxs-lookup"><span data-stu-id="d5a82-112">WorkspaceKeys.xml</span></span>

    <span data-ttu-id="d5a82-113">**Примечание**  Файл ServerSettings.xml также можно архивировать.</span><span class="sxs-lookup"><span data-stu-id="d5a82-113">**Note** The ServerSettings.xml file can be backed up as well.</span></span> <span data-ttu-id="d5a82-114">Тем не менее, если определенная конфигурация была изменена (например, на исходном сервере, каталог виртуальных машин MED-V расположен в разделе "*C:\\Vms*", а такой каталог не существует на новом сервере), это может привести к возникновению ошибки.</span><span class="sxs-lookup"><span data-stu-id="d5a82-114">However, if a specific configuration has been changed (for example, on the original server, the MED-V VMS directory is located in "*C:\\Vms*" and such a directory does not exist on the new server), it can cause an error.</span></span>

     

**<span data-ttu-id="d5a82-115">Восстановление сервера MED-V</span><span class="sxs-lookup"><span data-stu-id="d5a82-115">To restore a MED-V server</span></span>**

1.  <span data-ttu-id="d5a82-116">Установите новый сервер MED-V.</span><span class="sxs-lookup"><span data-stu-id="d5a82-116">Install a new MED-V server.</span></span>

2.  <span data-ttu-id="d5a82-117">Скопируйте файлы резервной копии в следующий каталог:</span><span class="sxs-lookup"><span data-stu-id="d5a82-117">Copy the backup files to the following directory:</span></span>

    *<span data-ttu-id="d5a82-118">&lt;InstallDir &gt; \\Servers\\ConfigurationServer</span><span class="sxs-lookup"><span data-stu-id="d5a82-118">&lt;InstallDir&gt;\\Servers\\ConfigurationServer</span></span>*

3.  <span data-ttu-id="d5a82-119">Перезапустите службу MED-V.</span><span class="sxs-lookup"><span data-stu-id="d5a82-119">Restart the MED-V service.</span></span>

 

 





