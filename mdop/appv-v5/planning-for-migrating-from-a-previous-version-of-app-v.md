---
title: Планирование миграции из предыдущей версии App-V
description: Планирование миграции из предыдущей версии App-V
author: dansimp
ms.assetid: d4ca8f09-86fd-456f-8ec2-242ff94ae9a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2242f58a29473e116506ec013b94a79d1bb814a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813472"
---
# <span data-ttu-id="e34ad-103">Планирование миграции из предыдущей версии App-V</span><span class="sxs-lookup"><span data-stu-id="e34ad-103">Planning for Migrating from a Previous Version of App-V</span></span>


<span data-ttu-id="e34ad-104">Ниже приведены сведения о том, как выполнить миграцию в App-V 5,0 из предыдущих версий App-V.</span><span class="sxs-lookup"><span data-stu-id="e34ad-104">Use the following information to plan how to migrate to App-V 5.0 from previous versions of App-V.</span></span>

## <span data-ttu-id="e34ad-105">Требования к миграции</span><span class="sxs-lookup"><span data-stu-id="e34ad-105">Migration requirements</span></span>


<span data-ttu-id="e34ad-106">Прежде чем приступать к обновлению, ознакомьтесь с приведенными ниже требованиями.</span><span class="sxs-lookup"><span data-stu-id="e34ad-106">Before you start any upgrades, review the following requirements:</span></span>

-   <span data-ttu-id="e34ad-107">Если вы выполняете обновление до версии App-V 4,6 SP2, перед обновлением до App-V 5,0 или более поздней версии обновите версию App-V 4,6 SP3.</span><span class="sxs-lookup"><span data-stu-id="e34ad-107">If you are upgrading from a version earlier than App-V 4.6 SP2, upgrade to version App-V 4.6 SP3 first before upgrading to App-V 5.0 or later.</span></span> <span data-ttu-id="e34ad-108">В этом случае сначала обновите клиенты App-V, а затем обновите серверные компоненты.</span><span class="sxs-lookup"><span data-stu-id="e34ad-108">In this scenario, upgrade the App-V clients first, and then upgrade the server components.</span></span>
<span data-ttu-id="e34ad-109">**Примечание.** Приложение App-V 4,6 завершило работу базовой поддержки.</span><span class="sxs-lookup"><span data-stu-id="e34ad-109">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

-   <span data-ttu-id="e34ad-110">Приложение App-V 5,0 поддерживает только пакеты, созданные с помощью App-V 5,0, или пакеты, которые были преобразованы в формат App-V 5,0 (**. AppV**).</span><span class="sxs-lookup"><span data-stu-id="e34ad-110">App-V 5.0 supports only packages that are created using App-V 5.0, or packages that have been converted to the App-V 5.0 (**.appv**) format.</span></span>

-   <span data-ttu-id="e34ad-111">Только для App-v 5,0 SP3: Если вы обновляете сервер App-v 5,0 SP1, ознакомьтесь с инструкциями по установке [App-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3) .</span><span class="sxs-lookup"><span data-stu-id="e34ad-111">App-V 5.0 SP3 only: If you are upgrading the App-V Server from App-V 5.0 SP1, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3) for instructions.</span></span>

## <span data-ttu-id="e34ad-112">Одновременное выполнение клиента App-V 5,0 с приложением-V 4,6</span><span class="sxs-lookup"><span data-stu-id="e34ad-112">Running the App-V 5.0 client concurrently with App-V 4.6</span></span>


<span data-ttu-id="e34ad-113">Клиент App-V 5,0 может одновременно выполняться на том же компьютере, что и клиент App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="e34ad-113">You can run the App-V 5.0 client concurrently on the same computer with the App-V4.6SP3 client.</span></span>

<span data-ttu-id="e34ad-114">При запуске существующих клиентов App-V вы можете:</span><span class="sxs-lookup"><span data-stu-id="e34ad-114">When you run coexisting App-V clients, you can:</span></span>

-   <span data-ttu-id="e34ad-115">Преобразуйте пакет обновления 3 (SP3) для App-v 4,6 в формат App-V 5,0 и опубликуйте оба пакета, если оба клиента запущены.</span><span class="sxs-lookup"><span data-stu-id="e34ad-115">Convert an App-V 4.6 SP3 package to the App-V 5.0 format and publish both packages, when you have both clients running.</span></span>

-   <span data-ttu-id="e34ad-116">Определите политику миграции для преобразованного пакета, который позволяет преобразованному пакету App-V 5,0 предполагать сопоставления типов файлов и ярлыки из пакета App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="e34ad-116">Define the migration policy for the converted package, which allows the converted App-V 5.0 package to assume the file type associations and shortcuts from the App-V 4.6 package.</span></span>

### <span data-ttu-id="e34ad-117">Поддерживаемые сценарии сосуществования</span><span class="sxs-lookup"><span data-stu-id="e34ad-117">Supported coexistence scenarios</span></span>

<span data-ttu-id="e34ad-118">В следующей таблице показаны поддерживаемые сценарии сосуществования App-V.</span><span class="sxs-lookup"><span data-stu-id="e34ad-118">The following table shows the supported App-V coexistence scenarios.</span></span> <span data-ttu-id="e34ad-119">Мы рекомендуем установить последние доступные обновления определенного выпуска, если вы используете соуже существующие клиенты.</span><span class="sxs-lookup"><span data-stu-id="e34ad-119">We recommend that you install the latest available updates of a given release when you are running coexisting clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e34ad-120">Тип клиента App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="e34ad-120">App-V 4.6 client type</span></span></th>
<th align="left"><span data-ttu-id="e34ad-121">Тип клиента App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e34ad-121">App-V 5.0 client type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e34ad-122">App-V 4,6 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="e34ad-122">App-V 4.6 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="e34ad-123">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e34ad-123">App-V 5.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e34ad-124">RDS-V 4,6 SP3</span><span class="sxs-lookup"><span data-stu-id="e34ad-124">App-V 4.6 SP3 RDS</span></span></p></td>
<td align="left"><p><span data-ttu-id="e34ad-125">App-V 5,0 RDS</span><span class="sxs-lookup"><span data-stu-id="e34ad-125">App-V 5.0 RDS</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="e34ad-126">Требования для запуска существующих клиентов</span><span class="sxs-lookup"><span data-stu-id="e34ad-126">Requirements for running coexisting clients</span></span>

<span data-ttu-id="e34ad-127">Для работы с существующими клиентами необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e34ad-127">To run coexisting clients, you must:</span></span>

-   <span data-ttu-id="e34ad-128">Установите клиент App-V 4.6 перед установкой клиента App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e34ad-128">Install the App-V4.6 client before you install the App-V 5.0 client.</span></span>

-   <span data-ttu-id="e34ad-129">Включите параметр групповой политики **включения режима миграции** , который находится в узле досуществования клиента **App-V** &gt; **Client Coexistence** .</span><span class="sxs-lookup"><span data-stu-id="e34ad-129">Enable the **Enable Migration Mode** Group Policy setting, which is in the **App-V** &gt; **Client Coexistence** node.</span></span> <span data-ttu-id="e34ad-130">Чтобы получить шаблон развертывания ADMX, ознакомьтесь со статьей [скачивание и развертывание шаблонов групповой политики MDOP](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="e34ad-130">To get the deploy the .admx template, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

### <span data-ttu-id="e34ad-131">Загрузка и документация для клиента</span><span class="sxs-lookup"><span data-stu-id="e34ad-131">Client downloads and documentation</span></span>

<span data-ttu-id="e34ad-132">В приведенной ниже таблице содержится ссылка на документацию по выпускам TechNet.</span><span class="sxs-lookup"><span data-stu-id="e34ad-132">The following table provides link to the TechNet documentation about the releases.</span></span> <span data-ttu-id="e34ad-133">Документация TechNet о клиенте App-V применима к обоим клиентам, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="e34ad-133">The TechNet documentation about the App-V client applies to both clients, unless stated otherwise.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e34ad-134">Версия App-V</span><span class="sxs-lookup"><span data-stu-id="e34ad-134">App-V version</span></span></th>
<th align="left"><span data-ttu-id="e34ad-135">Ссылка на документацию TechNet</span><span class="sxs-lookup"><span data-stu-id="e34ad-135">Link to TechNet documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e34ad-136">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="e34ad-136">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)"><span data-ttu-id="e34ad-137">Сведения о системе Microsoft Application Virtualization 4.6 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="e34ad-137">About Microsoft Application Virtualization 4.6 SP3</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e34ad-138">App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="e34ad-138">App-V 5.0SP3</span></span></p></td>
<td align="left"><p><a href="about-app-v-50-sp3.md" data-raw-source="[About Microsoft Application Virtualization 5.0 SP3](about-app-v-50-sp3.md)"><span data-ttu-id="e34ad-139">Сведения о Microsoft Application Virtualization 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="e34ad-139">About Microsoft Application Virtualization 5.0 SP3</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e34ad-140">Дополнительные сведения о настройке сосуществования клиента App-V 5,0 можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="e34ad-140">For more information about how to configure App-V 5.0 client coexistence, see:</span></span>

-   [<span data-ttu-id="e34ad-141">Развертывание приложения App-V 4,6 и клиента App-V 5,0 на том же компьютере</span><span class="sxs-lookup"><span data-stu-id="e34ad-141">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

-   [<span data-ttu-id="e34ad-142">Сосуществование и миграция App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e34ad-142">App-V 5.0 Coexistence and Migration</span></span>](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a><span data-ttu-id="e34ad-143">Преобразование пакетов предыдущей версии с помощью преобразователя пакетов</span><span class="sxs-lookup"><span data-stu-id="e34ad-143">Converting “previous-version” packages using the package converter</span></span>


<span data-ttu-id="e34ad-144">Перед переносом пакета, созданного с помощью App-V 4.6 SP3 или более ранней версии, в App-V 5,0, ознакомьтесь с приведенными ниже требованиями.</span><span class="sxs-lookup"><span data-stu-id="e34ad-144">Before migrating a package, created using App-V4.6SP3 or earlier, to App-V 5.0, review the following requirements:</span></span>

-   <span data-ttu-id="e34ad-145">Вы должны преобразовать пакет в файл формата **. AppV** .</span><span class="sxs-lookup"><span data-stu-id="e34ad-145">You must convert the package to the **.appv** file format.</span></span>

-   <span data-ttu-id="e34ad-146">Преобразователь пакетов поддерживает только прямое преобразование пакетов, созданных с помощью App-V 4,5 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e34ad-146">The Package Converter supports only the direct conversion of packages that were created by using App-V 4.5 and later.</span></span> <span data-ttu-id="e34ad-147">Чтобы использовать преобразователь пакетов для пакета, созданного с помощью предыдущей версии, необходимо использовать приложение App-V версии 4.5 или более поздней для обновления пакета, а затем можно выполнить преобразование пакета.</span><span class="sxs-lookup"><span data-stu-id="e34ad-147">To use the package converter on a package that was created using a previous version, you must use an App-V4.5 or later version of the sequencer to upgrade the package, and then you can perform the package conversion.</span></span>

<span data-ttu-id="e34ad-148">Дополнительные сведения об использовании конвертера пакетов для преобразования пакета приведены в разделе [Преобразование пакета, созданного в предыдущей версии App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="e34ad-148">For more information about using the package converter to convert a package, see [How to Convert a Package Created in a Previous Version of App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md).</span></span> <span data-ttu-id="e34ad-149">После преобразования файла вы можете развернуть его на целевые компьютеры, на которых запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e34ad-149">After you convert the file, you can deploy it to target computers that run the App-V 5.0 client.</span></span>






## <span data-ttu-id="e34ad-150">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e34ad-150">Related topics</span></span>


[<span data-ttu-id="e34ad-151">Планирование развертывания App-V</span><span class="sxs-lookup"><span data-stu-id="e34ad-151">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





