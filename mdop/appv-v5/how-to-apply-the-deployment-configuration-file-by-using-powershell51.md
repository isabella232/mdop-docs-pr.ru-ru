---
title: Применение файла конфигурации развертывания с помощью PowerShell
description: Применение файла конфигурации развертывания с помощью PowerShell
author: dansimp
ms.assetid: 78fe0f15-4a36-41e3-96d6-7d5aa77c1e06
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49beb7ea4afe46c9b0f1640152c786d7c6ba8663
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814440"
---
# <span data-ttu-id="93990-103">Применение файла конфигурации развертывания с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="93990-103">How to Apply the Deployment Configuration File by Using PowerShell</span></span>


<span data-ttu-id="93990-104">Файл динамической конфигурации развертывания применяется при добавлении пакета или задан на компьютере, на котором запущен клиент App-V 5,1 перед публикацией пакета.</span><span class="sxs-lookup"><span data-stu-id="93990-104">The dynamic deployment configuration file is applied when a package is added or set to a computer running the App-V 5.1 client before the package has been published.</span></span> <span data-ttu-id="93990-105">Файл настраивает параметры по умолчанию для пакета для всех пользователей на компьютере, на котором запущен клиент App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="93990-105">The file configures the default settings for package for all users on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="93990-106">В этом разделе описаны действия, которые необходимо выполнить для использования файла конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="93990-106">This section describes the steps used to use a deployment configuration file.</span></span> <span data-ttu-id="93990-107">Процедура основывается на следующем примере и предполагает, что на компьютере существуют следующие файлы пакета и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="93990-107">The procedure is based on the following example and assumes the following package and configuration files exist on a computer:</span></span>

**<span data-ttu-id="93990-108">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="93990-108">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="93990-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="93990-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

**<span data-ttu-id="93990-110">Применение файла конфигурации развертывания с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="93990-110">To Apply the Deployment Configuration File Using PowerShell</span></span>**

-   <span data-ttu-id="93990-111">Чтобы указать новый набор конфигураций по умолчанию для всех пользователей, которые будут запускать пакет на определенном компьютере, используйте следующую консоль:</span><span class="sxs-lookup"><span data-stu-id="93990-111">To specify a new default set of configurations for all users who will run the package on a specific computer, using a PowerShell console type the following:</span></span>

    **<span data-ttu-id="93990-112">Add-AppVClientPackage — path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="93990-112">Add-AppVClientPackage –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

    **<span data-ttu-id="93990-113">Примечание.</span><span class="sxs-lookup"><span data-stu-id="93990-113">Note</span></span>**  
    <span data-ttu-id="93990-114">Эта команда перехватывает полученный объект в $pkg.</span><span class="sxs-lookup"><span data-stu-id="93990-114">This command captures the resulting object into $pkg.</span></span> <span data-ttu-id="93990-115">Если пакет уже присутствует на компьютере, можно использовать командлет **Set-AppVclientPackage** , чтобы применить документ конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="93990-115">If the package is already present on the computer, the **Set-AppVclientPackage** cmdlet can be used to apply the deployment configuration document:</span></span>

    **<span data-ttu-id="93990-116">Set-AppVClientPackage-Name MyApp — путь c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="93990-116">Set-AppVClientPackage –Name Myapp –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="93990-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="93990-117">Related topics</span></span>


[<span data-ttu-id="93990-118">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="93990-118">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









