---
title: Удаление компонентов или программного обеспечения MBAM Server
description: Удаление компонентов или программного обеспечения MBAM Server
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824979"
---
# <span data-ttu-id="72dcd-103">Удаление компонентов или программного обеспечения MBAM Server</span><span class="sxs-lookup"><span data-stu-id="72dcd-103">Removing MBAM Server Features or Software</span></span>


<span data-ttu-id="72dcd-104">В этой статье объясняется, как удалить программное обеспечение и компоненты из Microsoft BitLocker Administration и Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="72dcd-104">These instructions explain how to remove software and features from Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="72dcd-105">При удалении функций сервера MBAM на сервере удаляются только те из них, которые были настроены, а не программное обеспечение сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="72dcd-105">If you remove MBAM Server features, only the configured features are removed from the server, not the MBAM Server software.</span></span> <span data-ttu-id="72dcd-106">При удалении программного обеспечения сервера MBAM на нем удаляются программное обеспечение и все функции сервера MBAM, которые вы настроили для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="72dcd-106">If you remove the MBAM Server software, the software and any MBAM Server features that you configured on that server are removed.</span></span>

<span data-ttu-id="72dcd-107">**Примечание**  Чтобы предотвратить случайное удаление данных, MBAM не предоставляет механизма для удаления баз данных. Это необходимо сделать вручную.</span><span class="sxs-lookup"><span data-stu-id="72dcd-107">**Note** To prevent the accidental removal of data, MBAM provides no mechanism for removing the databases; you must do that manually.</span></span>

 

## <a href="" id="bkmk-removeserverfeatures"></a><span data-ttu-id="72dcd-108">Удаление функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="72dcd-108">Removing MBAM Server features</span></span>


<span data-ttu-id="72dcd-109">Для удаления настроенных функций сервера MBAM можно использовать один из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="72dcd-109">You can use either of the following methods to remove MBAM Server features that you have configured:</span></span>

-   <span data-ttu-id="72dcd-110">Мастер настройки сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="72dcd-110">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="72dcd-111">Командлеты Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="72dcd-111">Windows PowerShell cmdlets</span></span>

### <span data-ttu-id="72dcd-112">Удаление функций с помощью мастера конфигурации сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="72dcd-112">Using the MBAM Server Configuration wizard to remove features</span></span>

<span data-ttu-id="72dcd-113">Следуйте этим инструкциям, чтобы с помощью мастера конфигурации сервера MBAM удалить из сервера настроенные компоненты сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="72dcd-113">Follow these instructions to use the MBAM Server Configuration wizard to remove configured MBAM Server features from a server.</span></span>

**<span data-ttu-id="72dcd-114">Удаление функций MBAM с помощью мастера</span><span class="sxs-lookup"><span data-stu-id="72dcd-114">To remove MBAM features by using the wizard</span></span>**

1.  <span data-ttu-id="72dcd-115">На сервере, на котором вы хотите удалить компоненты, выберите **Конфигурация сервера MBAM** , чтобы открыть мастер настройки.</span><span class="sxs-lookup"><span data-stu-id="72dcd-115">On the server where you want to remove features, select **MBAM Server Configuration** to open the configuration wizard.</span></span>

2.  <span data-ttu-id="72dcd-116">Нажмите кнопку **удалить компоненты**, выберите компоненты, которые нужно удалить, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="72dcd-116">Click **Remove Features**, select the features to remove, and then click **Next**.</span></span> <span data-ttu-id="72dcd-117">На странице **сводки** отображаются компоненты, выбранные для удаления.</span><span class="sxs-lookup"><span data-stu-id="72dcd-117">A **Summary** page displays the features you selected for removal.</span></span>

3.  <span data-ttu-id="72dcd-118">Нажмите кнопку **Удалить** , чтобы начать удаление функций, а затем нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="72dcd-118">Click **Remove** to start removing the features, and then click **Close**.</span></span>

### <span data-ttu-id="72dcd-119">Удаление функций с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="72dcd-119">Using Windows PowerShell to remove features</span></span>

<span data-ttu-id="72dcd-120">Ниже описаны действия, которые можно использовать в качестве общего руководства по удалению функций сервера MBAM с помощью командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="72dcd-120">Use the following steps as a general guide to remove MBAM Server features by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="72dcd-121">Удаление функций MBAM с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="72dcd-121">To remove MBAM features by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="72dcd-122">Перед удалением функций прочтите раздел [Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) , чтобы просмотреть предварительные требования для использования Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="72dcd-122">Before removing any features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="72dcd-123">Используйте следующие командлеты для удаления функций сервера MBAM:</span><span class="sxs-lookup"><span data-stu-id="72dcd-123">Use the following cmdlets to remove MBAM Server features:</span></span>

    -   <span data-ttu-id="72dcd-124">Disable-MbamReport</span><span class="sxs-lookup"><span data-stu-id="72dcd-124">Disable-MbamReport</span></span>

    -   <span data-ttu-id="72dcd-125">Disable-MbamWebApplication</span><span class="sxs-lookup"><span data-stu-id="72dcd-125">Disable-MbamWebApplication</span></span>

    -   <span data-ttu-id="72dcd-126">Disable-MbamCMIntegration</span><span class="sxs-lookup"><span data-stu-id="72dcd-126">Disable-MbamCMIntegration</span></span>

    <span data-ttu-id="72dcd-127">Чтобы получить справку по командлетам Windows PowerShell, введите командлет **Get-Help** &lt; *cmdlet* &gt; или ознакомьтесь [со статьей автоматизации пакетов оптимизации рабочей среды Microsoft](https://go.microsoft.com/fwlink/?LinkId=393498) для MBAM командлетов Windows PowerShell на странице Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="72dcd-127">To get help with Windows PowerShell cmdlets, type **Get-Help** &lt;*cmdlet*&gt; or see the [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) page for the MBAM Windows PowerShell cmdlets.</span></span>

## <span data-ttu-id="72dcd-128">Удаление программного обеспечения сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="72dcd-128">Removing MBAM Server software</span></span>


<span data-ttu-id="72dcd-129">Выполните описанные ниже действия, чтобы удалить программное обеспечение сервера MBAM и любые функции сервера MBAM, которые вы настроили для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="72dcd-129">Use the following steps to remove the MBAM Server software and any MBAM Server features that you configured on that server.</span></span>

**<span data-ttu-id="72dcd-130">Удаление программного обеспечения сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="72dcd-130">To remove the MBAM Server software</span></span>**

1.  <span data-ttu-id="72dcd-131">На сервере, на котором нужно удалить программное обеспечение сервера MBAM, **MBAMserversetup.exe** запустите мастер настройки администрирования и наблюдения за Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="72dcd-131">On the server where you want to uninstall the MBAM Server software, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="72dcd-132">Нажмите кнопку **Удалить**и следуйте дальнейшим инструкциям, чтобы завершить процедуру удаления серверного программного обеспечения MBAM.</span><span class="sxs-lookup"><span data-stu-id="72dcd-132">Select **Uninstall**, and follow the remaining prompts to complete the process of uninstalling the MBAM Server software.</span></span>



## <span data-ttu-id="72dcd-133">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="72dcd-133">Related topics</span></span>


[<span data-ttu-id="72dcd-134">Развертывание MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="72dcd-134">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

 

 

## <span data-ttu-id="72dcd-135">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="72dcd-135">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="72dcd-136">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="72dcd-136">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="72dcd-137">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="72dcd-137">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



