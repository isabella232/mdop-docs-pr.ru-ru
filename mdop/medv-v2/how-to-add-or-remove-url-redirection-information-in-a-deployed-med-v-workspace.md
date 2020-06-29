---
title: Добавление или удаление сведений о перенаправлении URL-адресов в развернутой рабочей области MED-V
description: Добавление или удаление сведений о перенаправлении URL-адресов в развернутой рабочей области MED-V
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826442"
---
# <span data-ttu-id="3882b-103">Добавление или удаление сведений о перенаправлении URL-адресов в развернутой рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="3882b-103">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>


<span data-ttu-id="3882b-104">Чтобы изменить сведения о перенаправлении URL-адреса в развернутой рабочей области MED-V, рекомендуется обновить системный реестр с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="3882b-104">To edit URL redirection information in a deployed MED-V workspace, we recommend that you update the system registry by using Group Policy.</span></span> <span data-ttu-id="3882b-105">Несмотря на то что мы не рекомендуем, вы также можете перестроить и повторно развернуть рабочую область MED-V с обновленными сведениями о перенаправлении URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="3882b-105">Although we do not recommend it, you can also rebuild and redeploy the MED-V workspace with the updated URL redirection information.</span></span>

<span data-ttu-id="3882b-106">Раздел реестра обычно находится по адресу:</span><span class="sxs-lookup"><span data-stu-id="3882b-106">The registry key is usually located at:</span></span>

<span data-ttu-id="3882b-107">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="3882b-107">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="3882b-108">Должно быть указано следующее многострочное значение:</span><span class="sxs-lookup"><span data-stu-id="3882b-108">The following multi-string value must be present:</span></span> `RedirectUrls`

<span data-ttu-id="3882b-109">Данные о значении `RedirectUrls` — это список всех URL-адресов, указанных для перенаправления при создании пакета рабочей области MED-v с помощью **диспетчера рабочих областей med-v**.</span><span class="sxs-lookup"><span data-stu-id="3882b-109">The value data for `RedirectUrls` is a list of all of the URLs that you specified for redirection when you built the MED-V workspace package by using the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="3882b-110">Дополнительные сведения можно найти [в разделе Создание пакета рабочей области для MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="3882b-110">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="3882b-111">Вы можете добавлять и удалять сведения о перенаправлении URL-адреса, выполнив одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="3882b-111">You can add and remove URL redirection information by performing one of the following tasks:</span></span>

-   [<span data-ttu-id="3882b-112">Изменение раздела реестра для перенаправления URL-адреса и развертывание с помощью групповой политики</span><span class="sxs-lookup"><span data-stu-id="3882b-112">Edit the URL Redirection Registry Key and Deploy Using Group Policy</span></span>](#bkmk-editreg)

-   [<span data-ttu-id="3882b-113">Изменение текстового файла перенаправления URL-адресов и повторное построение рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="3882b-113">Edit the URL Redirection Text File and Rebuild the MED-V Workspace</span></span>](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**<span data-ttu-id="3882b-114">Обновление сведений о перенаправлении URL-адреса с помощью групповой политики</span><span class="sxs-lookup"><span data-stu-id="3882b-114">To update URL Redirection information by using Group Policy</span></span>**

1.  <span data-ttu-id="3882b-115">Измените значение из нескольких строк в разделе реестра с именем `RedirectUrls` .</span><span class="sxs-lookup"><span data-stu-id="3882b-115">Edit the registry key multi-string value that is named `RedirectUrls`.</span></span> <span data-ttu-id="3882b-116">Обычно это значение находится по адресу:</span><span class="sxs-lookup"><span data-stu-id="3882b-116">This value is typically located at:</span></span>

    <span data-ttu-id="3882b-117">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="3882b-117">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

    <span data-ttu-id="3882b-118">Если вы добавляете URL-адреса в раздел реестра, введите по одному для каждой строки, как при создании пакета рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="3882b-118">If you are adding URLs to the registry key, enter them one per line, as was required when you built the MED-V workspace package.</span></span> <span data-ttu-id="3882b-119">Дополнительные сведения можно найти [в разделе Создание пакета рабочей области для MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="3882b-119">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

2.  <span data-ttu-id="3882b-120">Разверните обновленный раздел реестра с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="3882b-120">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="3882b-121">Дополнительные сведения об использовании групповой политики можно найти в разделе [Установка программного обеспечения групповой политики](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="3882b-121">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

<span data-ttu-id="3882b-122">**Примечание**  Этот метод изменения сведений о перенаправлении URL-адреса — наилучший подход для MED-V.</span><span class="sxs-lookup"><span data-stu-id="3882b-122">**Note** This method of editing URL redirection information is a MED-V best practice.</span></span>

 

<a href="" id="bkmk-edittext"></a>**<span data-ttu-id="3882b-123">Повторное создание рабочей области для MED-V с помощью обновленного текстового файла URL-адреса</span><span class="sxs-lookup"><span data-stu-id="3882b-123">To rebuild the MED-V workspace by using an updated URL text file</span></span>**

-   <span data-ttu-id="3882b-124">Еще один способ добавить URL-адреса из списка перенаправления — обновить текстовый файл перенаправления URL-адресов, а затем использовать его для создания новой рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="3882b-124">Another method of adding and removing URLs from the redirection list is to update the URL redirection text file and then use it to build a new MED-V workspace.</span></span> <span data-ttu-id="3882b-125">Затем вы можете повторно развернуть рабочую область MED-V, как раньше, с помощью стандартного процесса развертывания, например системы ESD.</span><span class="sxs-lookup"><span data-stu-id="3882b-125">You can then redeploy the MED-V workspace as before, by using your standard process of deployment, such as an ESD system.</span></span>

    <span data-ttu-id="3882b-126">**Важно!**  Мы не рекомендуем использовать этот метод редактирования перенаправления URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="3882b-126">**Important** We do not recommend this method of editing URL redirection information.</span></span> <span data-ttu-id="3882b-127">Кроме того, при повторном развертывании рабочей области MED-V в корпоративной среде сначала необходимо выполнить настройку, а все данные, сохраненные на виртуальной машине, будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="3882b-127">In addition, any time that you redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="3882b-128">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3882b-128">Related topics</span></span>


[<span data-ttu-id="3882b-129">Проверка перенаправления URL-адресов</span><span class="sxs-lookup"><span data-stu-id="3882b-129">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="3882b-130">Управление приложениями, развернутыми в рабочих областях MED-V</span><span class="sxs-lookup"><span data-stu-id="3882b-130">Managing Applications Deployed to MED-V Workspaces</span></span>](managing-applications-deployed-to-med-v-workspaces.md)

[<span data-ttu-id="3882b-131">Создание пакета рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="3882b-131">Create a MED-V Workspace Package</span></span>](create-a-med-v-workspace-package.md)

 

 





