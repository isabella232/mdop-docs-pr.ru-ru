---
title: Планирование миграции из предыдущей версии App-V
description: Планирование миграции из предыдущей версии App-V
author: dansimp
ms.assetid: 4a058047-9674-41bc-8050-c58c97a80a9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: d7f2496b355aee6a598fee44c84e7e8c0f755c4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813469"
---
# <span data-ttu-id="8d131-103">Планирование миграции из предыдущей версии App-V</span><span class="sxs-lookup"><span data-stu-id="8d131-103">Planning for Migrating from a Previous Version of App-V</span></span>


<span data-ttu-id="8d131-104">Используйте следующие сведения, чтобы спланировать переход на Microsoft Application Virtualization (App-V) 5,1 из предыдущих версий App-V.</span><span class="sxs-lookup"><span data-stu-id="8d131-104">Use the following information to plan how to migrate to Microsoft Application Virtualization (App-V) 5.1 from previous versions of App-V.</span></span>

## <span data-ttu-id="8d131-105">Требования к миграции</span><span class="sxs-lookup"><span data-stu-id="8d131-105">Migration requirements</span></span>


<span data-ttu-id="8d131-106">Прежде чем приступать к обновлению, ознакомьтесь с приведенными ниже требованиями.</span><span class="sxs-lookup"><span data-stu-id="8d131-106">Before you start any upgrades, review the following requirements:</span></span>

-   <span data-ttu-id="8d131-107">Если вы выполняете обновление до версии App-V 4,6 SP2, перед обновлением до App-V 5,1 или более поздней версии обновите версию App-V 4,6 SP3.</span><span class="sxs-lookup"><span data-stu-id="8d131-107">If you are upgrading from a version earlier than App-V 4.6 SP2, upgrade to version App-V 4.6 SP3 first before upgrading to App-V 5.1 or later.</span></span> <span data-ttu-id="8d131-108">В этом случае сначала обновите клиенты App-V, а затем обновите серверные компоненты.</span><span class="sxs-lookup"><span data-stu-id="8d131-108">In this scenario, upgrade the App-V clients first, and then upgrade the server components.</span></span>
<span data-ttu-id="8d131-109">**Примечание.** Приложение App-V 4,6 завершило работу базовой поддержки.</span><span class="sxs-lookup"><span data-stu-id="8d131-109">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

-   <span data-ttu-id="8d131-110">Приложение App-V 5,1 поддерживает только пакеты, созданные с помощью App-V 5,0 или App-V 5,1, или пакетов, преобразованных в **AppV** -формат.</span><span class="sxs-lookup"><span data-stu-id="8d131-110">App-V 5.1 supports only packages that are created using App-V 5.0 or App-V 5.1, or packages that have been converted to the **.appv** format.</span></span>

-   <span data-ttu-id="8d131-111">Если вы обновляете сервер App-v 5,0 с пакетом обновления 1 (SP1), ознакомьтесь с инструкциями по использованию [App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51) .</span><span class="sxs-lookup"><span data-stu-id="8d131-111">If you are upgrading the App-V Server from App-V 5.0 SP1, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51) for instructions.</span></span>

## <span data-ttu-id="8d131-112">Одновременное выполнение клиента App-V 5,1 с приложением-V 4,6</span><span class="sxs-lookup"><span data-stu-id="8d131-112">Running the App-V 5.1 client concurrently with App-V 4.6</span></span>


<span data-ttu-id="8d131-113">Клиент App-V 5,1 может одновременно выполняться на том же компьютере, что и клиент App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="8d131-113">You can run the App-V 5.1 client concurrently on the same computer with the App-V4.6SP3 client.</span></span>

<span data-ttu-id="8d131-114">При запуске существующих клиентов App-V вы можете:</span><span class="sxs-lookup"><span data-stu-id="8d131-114">When you run coexisting App-V clients, you can:</span></span>

-   <span data-ttu-id="8d131-115">Преобразуйте пакет обновления 3 (SP3) для App-v 4,6 в формат App-V 5,1 и опубликуйте оба пакета, если оба клиента запущены.</span><span class="sxs-lookup"><span data-stu-id="8d131-115">Convert an App-V 4.6 SP3 package to the App-V 5.1 format and publish both packages, when you have both clients running.</span></span>

-   <span data-ttu-id="8d131-116">Определите политику миграции для преобразованного пакета, который позволяет преобразованному пакету App-V 5,1 предполагать сопоставления типов файлов и ярлыки из пакета App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="8d131-116">Define the migration policy for the converted package, which allows the converted App-V 5.1 package to assume the file type associations and shortcuts from the App-V 4.6 package.</span></span>

### <span data-ttu-id="8d131-117">Поддерживаемые сценарии сосуществования</span><span class="sxs-lookup"><span data-stu-id="8d131-117">Supported coexistence scenarios</span></span>

<span data-ttu-id="8d131-118">В следующей таблице показаны поддерживаемые сценарии сосуществования App-V.</span><span class="sxs-lookup"><span data-stu-id="8d131-118">The following table shows the supported App-V coexistence scenarios.</span></span> <span data-ttu-id="8d131-119">Мы рекомендуем установить последние доступные обновления определенного выпуска, если вы используете соуже существующие клиенты.</span><span class="sxs-lookup"><span data-stu-id="8d131-119">We recommend that you install the latest available updates of a given release when you are running coexisting clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d131-120">Тип клиента App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="8d131-120">App-V 4.6 client type</span></span></th>
<th align="left"><span data-ttu-id="8d131-121">Тип клиента App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="8d131-121">App-V 5.1 client type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d131-122">App-V 4,6 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="8d131-122">App-V 4.6 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d131-123">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="8d131-123">App-V 5.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d131-124">RDS-V 4,6 SP3</span><span class="sxs-lookup"><span data-stu-id="8d131-124">App-V 4.6 SP3 RDS</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d131-125">App-V 5,1 RDS</span><span class="sxs-lookup"><span data-stu-id="8d131-125">App-V 5.1 RDS</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="8d131-126">Требования для запуска существующих клиентов</span><span class="sxs-lookup"><span data-stu-id="8d131-126">Requirements for running coexisting clients</span></span>

<span data-ttu-id="8d131-127">Для работы с существующими клиентами необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="8d131-127">To run coexisting clients, you must:</span></span>

-   <span data-ttu-id="8d131-128">Установите клиент App-V 4.6 перед установкой клиента App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8d131-128">Install the App-V4.6 client before you install the App-V 5.1 client.</span></span>

-   <span data-ttu-id="8d131-129">Включите параметр групповой политики **включения режима миграции** , который находится в узле досуществования клиента **App-V** &gt; **Client Coexistence** .</span><span class="sxs-lookup"><span data-stu-id="8d131-129">Enable the **Enable Migration Mode** Group Policy setting, which is in the **App-V** &gt; **Client Coexistence** node.</span></span> <span data-ttu-id="8d131-130">Чтобы развернуть шаблон ADMX, ознакомьтесь [со сведениями о том, как скачать и развернуть шаблоны групповой политики MDOP (ADMX)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="8d131-130">To deploy the .admx template, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

<span data-ttu-id="8d131-131">**Примечание**  Пакеты App-V 5,1 могут работать параллельно с пакетами App-V 4,6, если вы уже уже установлены приложения App-V 5,1 и 4,6.</span><span class="sxs-lookup"><span data-stu-id="8d131-131">**Note** App-V 5.1 packages can run side by side with App-V 4.6 packages if you have coexisting installations of App-V 5.1 and 4.6.</span></span> <span data-ttu-id="8d131-132">Однако пакеты App-V 5,1 не могут взаимодействовать с пакетами App-V 4,6 в той же виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="8d131-132">However, App-V 5.1 packages cannot interact with App-V 4.6 packages in the same virtual environment.</span></span>

 

### <span data-ttu-id="8d131-133">Загрузка и документация для клиента</span><span class="sxs-lookup"><span data-stu-id="8d131-133">Client downloads and documentation</span></span>

<span data-ttu-id="8d131-134">В следующей таблице приведены ссылки на загружаемые файлы для клиента App-V 4,6 и в документацию TechNet о выпусках.</span><span class="sxs-lookup"><span data-stu-id="8d131-134">The following table provides links to the App-V 4.6 client downloads and to the TechNet documentation about the releases.</span></span> <span data-ttu-id="8d131-135">Загружаемые файлы включают в себя клиенты App-V "регулярные" и RDS.</span><span class="sxs-lookup"><span data-stu-id="8d131-135">The downloads include the App-V “regular” and RDS clients.</span></span> <span data-ttu-id="8d131-136">Документация TechNet о клиенте App-V применима к обоим клиентам, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="8d131-136">The TechNet documentation about the App-V client applies to both clients, unless stated otherwise.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d131-137">Версия App-V</span><span class="sxs-lookup"><span data-stu-id="8d131-137">App-V version</span></span></th>
<th align="left"><span data-ttu-id="8d131-138">Ссылка на документацию TechNet</span><span class="sxs-lookup"><span data-stu-id="8d131-138">Link to TechNet documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d131-139">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="8d131-139">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)"><span data-ttu-id="8d131-140">Сведения о системе Microsoft Application Virtualization 4.6 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="8d131-140">About Microsoft Application Virtualization 4.6 SP3</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d131-141">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="8d131-141">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="about-app-v-51.md" data-raw-source="[About Microsoft Application Virtualization 5.1](about-app-v-51.md)"><span data-ttu-id="8d131-142">О программе Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="8d131-142">About Microsoft Application Virtualization 5.1</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8d131-143">Дополнительные сведения о настройке сосуществования клиента App-V 5,1 можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="8d131-143">For more information about how to configure App-V 5.1 client coexistence, see:</span></span>

-   [<span data-ttu-id="8d131-144">Развертывание приложения App-V 4,6 и клиента App-V 5,1 на том же компьютере</span><span class="sxs-lookup"><span data-stu-id="8d131-144">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

-   [<span data-ttu-id="8d131-145">Сосуществование и миграция App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="8d131-145">App-V 5.0 Coexistence and Migration</span></span>](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a><span data-ttu-id="8d131-146">Преобразование пакетов предыдущей версии с помощью преобразователя пакетов</span><span class="sxs-lookup"><span data-stu-id="8d131-146">Converting “previous-version” packages using the package converter</span></span>


<span data-ttu-id="8d131-147">Перед переносом пакета, созданного с помощью App-4.6 SP2 или более ранней версии, в App-V 5,1, ознакомьтесь с приведенными ниже требованиями.</span><span class="sxs-lookup"><span data-stu-id="8d131-147">Before migrating a package, created using App-4.6SP2 or earlier, to App-V 5.1, review the following requirements:</span></span>

-   <span data-ttu-id="8d131-148">Вы должны преобразовать пакет в файл формата **. AppV** .</span><span class="sxs-lookup"><span data-stu-id="8d131-148">You must convert the package to the **.appv** file format.</span></span>

-   <span data-ttu-id="8d131-149">Преобразователь пакетов поддерживает только прямое преобразование пакетов, созданных с помощью App-V 4,5 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="8d131-149">The Package Converter supports only the direct conversion of packages that were created by using App-V 4.5 and later.</span></span> <span data-ttu-id="8d131-150">Чтобы использовать преобразователь пакетов для пакета, созданного с помощью предыдущей версии, необходимо использовать приложение App-V версии 4.5 или более поздней для обновления пакета, а затем можно выполнить преобразование пакета.</span><span class="sxs-lookup"><span data-stu-id="8d131-150">To use the package converter on a package that was created using a previous version, you must use an App-V4.5 or later version of the sequencer to upgrade the package, and then you can perform the package conversion.</span></span>

<span data-ttu-id="8d131-151">Дополнительные сведения об использовании конвертера пакетов для преобразования пакета приведены в разделе [Преобразование пакета, созданного в предыдущей версии App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="8d131-151">For more information about using the package converter to convert a package, see [How to Convert a Package Created in a Previous Version of App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md).</span></span> <span data-ttu-id="8d131-152">После преобразования файла вы можете развернуть его на целевые компьютеры, на которых запущен клиент App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8d131-152">After you convert the file, you can deploy it to target computers that run the App-V 5.1 client.</span></span>






## <span data-ttu-id="8d131-153">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8d131-153">Related topics</span></span>


[<span data-ttu-id="8d131-154">Планирование развертывания App-V</span><span class="sxs-lookup"><span data-stu-id="8d131-154">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





