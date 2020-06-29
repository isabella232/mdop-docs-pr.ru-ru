---
title: Настройка сервера MED-V Server в режиме кластера
description: Настройка сервера MED-V Server в режиме кластера
author: dansimp
ms.assetid: 41f0b2a3-4ce9-48e1-a6fb-4c13c4228515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddb7dd5af65d8a465c5c1884bb27a3027621bac1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826719"
---
# <span data-ttu-id="bd2bb-103">Настройка сервера MED-V Server в режиме кластера</span><span class="sxs-lookup"><span data-stu-id="bd2bb-103">Configuring MED-V Server for Cluster Mode</span></span>


<span data-ttu-id="bd2bb-104">Сервер MED-V можно настроить в кластерном режиме.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-104">You can configure the MED-V server in cluster mode.</span></span> <span data-ttu-id="bd2bb-105">В режиме кластеризации используются два сервера, и все файлы, определенные как взаимозависимые с обоими серверами, размещаются в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-105">In cluster mode, two servers are used and all files identified as mutual to both servers are placed on a file system.</span></span> <span data-ttu-id="bd2bb-106">Сервер обращается к файлам из файловой системы вместо того, чтобы хранить их локально.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-106">The server accesses the files from the file system rather than storing the files locally.</span></span>

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**<span data-ttu-id="bd2bb-107">Настройка сервера MED-V в кластерном режиме</span><span class="sxs-lookup"><span data-stu-id="bd2bb-107">To configure the MED-V server in cluster mode</span></span>**

1.  <span data-ttu-id="bd2bb-108">Установите и настройте MED-V на одном из серверов.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-108">Install and configure MED-V on one of the servers.</span></span>

2.  <span data-ttu-id="bd2bb-109">Создавайте общую сеть в централизованном расположении, где все серверы смогут получать к нему доступ.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-109">Create a shared network in a central location where all of the servers can access it.</span></span>

3.  <span data-ttu-id="bd2bb-110">Скопируйте содержимое папки \* &lt; installDir &gt; /Servers/ConfigurationServer\* в общую сеть.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-110">Copy the contents of the *&lt;InstallDir&gt;/Servers/ConfigurationServer* folder to the shared network.</span></span>

4.  <span data-ttu-id="bd2bb-111">Установите сервер MED-V на всех назначенных серверах.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-111">Install MED-V server on all designated servers.</span></span>

5.  <span data-ttu-id="bd2bb-112">В общей сети назначьте полный доступ всем системным учетным записям на сервере MED-V.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-112">On the shared network, assign full access to all MED-V server system accounts.</span></span>

6.  <span data-ttu-id="bd2bb-113">На каждом сервере выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-113">On each server, do the following:</span></span>

    1.  <span data-ttu-id="bd2bb-114">В файле \* &lt; InstallDir &gt; /Servers/ServerConfiguration.xml\* задайте для параметра \* &lt; StorePath &gt; \* значение "общий сетевой путь".</span><span class="sxs-lookup"><span data-stu-id="bd2bb-114">In the *&lt;InstallDir&gt;/Servers/ServerConfiguration.xml* file, set the value of *&lt;StorePath&gt;* to the shared network path.</span></span>

    2.  <span data-ttu-id="bd2bb-115">Скопируйте файл \* &lt; InstsallDir &gt; /Servers/KeyPair.xml\* с исходного сервера на все серверы MED-V.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-115">Copy the *&lt;InstsallDir&gt;/Servers/KeyPair.xml* file from the original server to all MED-V servers.</span></span>

    3.  <span data-ttu-id="bd2bb-116">Перезапустите службу MED-V.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-116">Restart the MED-V service.</span></span>

<span data-ttu-id="bd2bb-117">**Примечание**  Если у всех серверов есть одинаковые локальные параметры (такие как порты для прослушивания, сервер IIS, разрешения на управление, база данных отчетов и т. д.), \* &lt; &gt; ServerSettings.xml/Servers/installDir\* также могут совместно использовать все серверы.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-117">**Note** If all servers have the same local settings (such as listening ports, IIS server, management permissions, report database, and so on), the *&lt;InstallDir&gt;/Servers/ServerSettings.xml* can be shared by all servers as well.</span></span>

 

## <span data-ttu-id="bd2bb-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="bd2bb-118">Related topics</span></span>


[<span data-ttu-id="bd2bb-119">Планирование и проектирование инфраструктуры MED-V</span><span class="sxs-lookup"><span data-stu-id="bd2bb-119">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 





