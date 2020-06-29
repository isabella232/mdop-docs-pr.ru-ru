---
title: Сведения о параметрах конфигурации клиента
description: Сведения о параметрах конфигурации клиента
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814941"
---
# <span data-ttu-id="87752-103">Сведения о параметрах конфигурации клиента</span><span class="sxs-lookup"><span data-stu-id="87752-103">About Client Configuration Settings</span></span>


<span data-ttu-id="87752-104">Клиент Microsoft Application Virtualization (App-V) 5,0 хранит свою конфигурацию в реестре.</span><span class="sxs-lookup"><span data-stu-id="87752-104">The Microsoft Application Virtualization (App-V) 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="87752-105">Вы можете собрать полезные сведения о клиенте, если вы понимаете формат данных в реестре.</span><span class="sxs-lookup"><span data-stu-id="87752-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="87752-106">Вы также можете настроить множество клиентских действий, изменяя записи в реестре.</span><span class="sxs-lookup"><span data-stu-id="87752-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="87752-107">В этом разделе перечислены параметры конфигурации клиента App-V 5,0 и описаны их использование.</span><span class="sxs-lookup"><span data-stu-id="87752-107">This topic lists the App-V 5.0 Client configuration settings and explains their uses.</span></span> <span data-ttu-id="87752-108">Вы можете изменить параметры конфигурации клиента с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="87752-108">You can use PowerShell to modify the client configuration settings.</span></span> <span data-ttu-id="87752-109">Дополнительные сведения об использовании PowerShell и App-V 5,0 можно найти [в разделе Администрирование App-V с помощью PowerShell](administering-app-v-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="87752-109">For more information about using PowerShell and App-V 5.0 see [Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md).</span></span>

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> <span data-ttu-id="87752-110">Параметры конфигурации клиента App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="87752-110">App-V 5.0 Client Configuration Settings</span></span>


<span data-ttu-id="87752-111">В следующей таблице приведены сведения о параметрах конфигурации клиента App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="87752-111">The following table displays information about the App-V 5.0 client configuration settings:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87752-112">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="87752-112">Setting Name</span></span></th>
<th align="left"><span data-ttu-id="87752-113">Флажок настройки</span><span class="sxs-lookup"><span data-stu-id="87752-113">Setup Flag</span></span></th>
<th align="left"><span data-ttu-id="87752-114">Описание</span><span class="sxs-lookup"><span data-stu-id="87752-114">Description</span></span></th>
<th align="left"><span data-ttu-id="87752-115">Настройка параметров</span><span class="sxs-lookup"><span data-stu-id="87752-115">Setting Options</span></span></th>
<th align="left"><span data-ttu-id="87752-116">Значение раздела реестра</span><span class="sxs-lookup"><span data-stu-id="87752-116">Registry Key Value</span></span></th>
<th align="left"><span data-ttu-id="87752-117">Отключенные ключи и значения состояния политики</span><span class="sxs-lookup"><span data-stu-id="87752-117">Disabled Policy State Keys and Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-118">PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="87752-118">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-119">PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="87752-119">PACKAGEINSTALLATIONROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-120">Указывает каталог, в котором будут установлены все новые приложения и обновления.</span><span class="sxs-lookup"><span data-stu-id="87752-120">Specifies directory where all new applications and updates will be installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-121">Строка</span><span class="sxs-lookup"><span data-stu-id="87752-121">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-122">Streaming\PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="87752-122">Streaming\PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-123">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-123">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-124">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="87752-124">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-125">PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="87752-125">PACKAGESOURCEROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-126">Переопределяет расположение источника для загрузки содержимого пакета.</span><span class="sxs-lookup"><span data-stu-id="87752-126">Overrides source location for downloading package content.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-127">Строка</span><span class="sxs-lookup"><span data-stu-id="87752-127">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-128">Streaming\PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="87752-128">Streaming\PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-129">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-129">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-130">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="87752-130">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-131">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-131">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-132">Этот параметр определяет, будут ли виртуализированные приложения запускаться на компьютерах с Windows 8, подключенных через лимитное сетевое подключение (например, 4G).</span><span class="sxs-lookup"><span data-stu-id="87752-132">This setting controls whether virtualized applications are launched on Windows 8 machines connected via a metered network connection (For example, 4G).</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-133">Истина (включена); False (отключенное состояние)</span><span class="sxs-lookup"><span data-stu-id="87752-133">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-134">Streaming\AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="87752-134">Streaming\AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-135">до</span><span class="sxs-lookup"><span data-stu-id="87752-135">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-136">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="87752-136">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-137">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-137">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-138">Задает количество повторений прерванного сеанса.</span><span class="sxs-lookup"><span data-stu-id="87752-138">Specifies the number of times to retry a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-139">Integer (0-99)</span><span class="sxs-lookup"><span data-stu-id="87752-139">Integer (0-99)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-140">Streaming\ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="87752-140">Streaming\ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-141">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-141">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-142">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="87752-142">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-143">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-143">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-144">Задает количество секунд между попытками повторного установления прерванного сеанса.</span><span class="sxs-lookup"><span data-stu-id="87752-144">Specifies the number of seconds between attempts to reestablish a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-145">Integer (0-3600)</span><span class="sxs-lookup"><span data-stu-id="87752-145">Integer (0-3600)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-146">Streaming\ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="87752-146">Streaming\ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-147">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-147">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-148">AutoLoad</span><span class="sxs-lookup"><span data-stu-id="87752-148">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-149">AUTOLOAD</span><span class="sxs-lookup"><span data-stu-id="87752-149">AUTOLOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-150">Определяет способ автоматической загрузки новых пакетов приложением App-V на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="87752-150">Specifies how new packages should be loaded automatically by App-V on a specific computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-151">(0x0) None; (0x1) ранее использованный; (0x2) все</span><span class="sxs-lookup"><span data-stu-id="87752-151">(0x0) None; (0x1) Previously used; (0x2) All</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-152">Streaming\AutoLoad</span><span class="sxs-lookup"><span data-stu-id="87752-152">Streaming\AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-153">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-153">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-154">LocationProvider</span><span class="sxs-lookup"><span data-stu-id="87752-154">LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-155">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-155">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-156">Задает CLSID для совместимой реализации интерфейса IAppvPackageLocationProvider.</span><span class="sxs-lookup"><span data-stu-id="87752-156">Specifies the CLSID for a compatible implementation of the IAppvPackageLocationProvider interface.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-157">Строка</span><span class="sxs-lookup"><span data-stu-id="87752-157">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-158">Streaming\LocationProvider</span><span class="sxs-lookup"><span data-stu-id="87752-158">Streaming\LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-159">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-159">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-160">CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="87752-160">CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-161">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-161">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-162">Указывает путь к действительному сертификату в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="87752-162">Specifies the path to a valid certificate in the certificate store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-163">Строка</span><span class="sxs-lookup"><span data-stu-id="87752-163">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-164">Streaming\CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="87752-164">Streaming\CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-165">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-165">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-166">VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="87752-166">VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-167">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-167">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-168">Проверка состояния отзыва сертификата сервера перед Steaming с помощью HTTPS.</span><span class="sxs-lookup"><span data-stu-id="87752-168">Verifies Server certificate revocation status before steaming using HTTPS.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-169">Истина (включена); False (отключенное состояние)</span><span class="sxs-lookup"><span data-stu-id="87752-169">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-170">Streaming\VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="87752-170">Streaming\VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-171">до</span><span class="sxs-lookup"><span data-stu-id="87752-171">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-172">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="87752-172">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-173">SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="87752-173">SHAREDCONTENTSTOREMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-174">Указывает на то, что содержимое потокового пакета не будет сохранено на локальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="87752-174">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-175">Истина (включена); False (отключенное состояние)</span><span class="sxs-lookup"><span data-stu-id="87752-175">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-176">Streaming\SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="87752-176">Streaming\SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-177">до</span><span class="sxs-lookup"><span data-stu-id="87752-177">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-178">Имя</span><span class="sxs-lookup"><span data-stu-id="87752-178">Name</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-179">Примечание.</span><span class="sxs-lookup"><span data-stu-id="87752-179">Note</span></span></strong><br/><p><span data-ttu-id="87752-180">Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-180">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="87752-181">Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-181">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-182">PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="87752-182">PUBLISHINGSERVERNAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-183">Отображает имя сервера публикации.</span><span class="sxs-lookup"><span data-stu-id="87752-183">Displays the name of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-184">Строка</span><span class="sxs-lookup"><span data-stu-id="87752-184">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-185">Publishing\Servers {serverId} \ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="87752-185">Publishing\Servers{serverId}\FriendlyName</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-186">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-186">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-187">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="87752-187">URL</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-188">Примечание.</span><span class="sxs-lookup"><span data-stu-id="87752-188">Note</span></span></strong><br/><p><span data-ttu-id="87752-189">Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-189">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="87752-190">Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-190">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-191">PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="87752-191">PUBLISHINGSERVERURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-192">Отображает URL-адрес сервера публикации.</span><span class="sxs-lookup"><span data-stu-id="87752-192">Displays the URL of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-193">Строка</span><span class="sxs-lookup"><span data-stu-id="87752-193">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-194">Publishing\Servers {serverId} \ URL-адрес</span><span class="sxs-lookup"><span data-stu-id="87752-194">Publishing\Servers{serverId}\URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-195">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-195">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-196">GlobalRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="87752-196">GlobalRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-197">Примечание.</span><span class="sxs-lookup"><span data-stu-id="87752-197">Note</span></span></strong><br/><p><span data-ttu-id="87752-198">Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-198">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="87752-199">Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-199">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-200">GLOBALREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="87752-200">GLOBALREFRESHENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-201">Включает глобальное обновление публикации (логическое значение)</span><span class="sxs-lookup"><span data-stu-id="87752-201">Enables global publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-202">Истина (включена); False (отключенное состояние)</span><span class="sxs-lookup"><span data-stu-id="87752-202">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-203">Publishing\Servers{serverId}\GlobalEnabled</span><span class="sxs-lookup"><span data-stu-id="87752-203">Publishing\Servers{serverId}\GlobalEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-204">False</span><span class="sxs-lookup"><span data-stu-id="87752-204">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-205">GlobalRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="87752-205">GlobalRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-206">Примечание.</span><span class="sxs-lookup"><span data-stu-id="87752-206">Note</span></span></strong><br/><p><span data-ttu-id="87752-207">Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-207">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="87752-208">Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-208">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-209">GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="87752-209">GLOBALREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-210">Запускает глобальное обновление публикации при входе.</span><span class="sxs-lookup"><span data-stu-id="87752-210">Triggers a global publishing refresh on logon.</span></span> <span data-ttu-id="87752-211">Значением</span><span class="sxs-lookup"><span data-stu-id="87752-211">( Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-212">Истина (включена); False (отключенное состояние)</span><span class="sxs-lookup"><span data-stu-id="87752-212">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-213">Publishing\Servers{serverId}\GlobalLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="87752-213">Publishing\Servers{serverId}\GlobalLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-214">False</span><span class="sxs-lookup"><span data-stu-id="87752-214">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-215">GlobalRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="87752-215">GlobalRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-216">Примечание.</span><span class="sxs-lookup"><span data-stu-id="87752-216">Note</span></span></strong><br/><p><span data-ttu-id="87752-217">Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-217">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="87752-218">Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-218">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-219">GLOBALREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="87752-219">GLOBALREFRESHINTERVAL</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="87752-220">Задает интервал обновления публикации с помощью GlobalRefreshIntervalUnit.</span><span class="sxs-lookup"><span data-stu-id="87752-220">Specifies the publishing refresh interval using the GlobalRefreshIntervalUnit.</span></span> <span data-ttu-id="87752-221">Чтобы отключить обновление пакета, выберите значение 0.</span><span class="sxs-lookup"><span data-stu-id="87752-221">To disable package refresh, select 0.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-222">Integer (0-744</span><span class="sxs-lookup"><span data-stu-id="87752-222">Integer (0-744</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-223">Publishing\Servers{serverId}\GlobalPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="87752-223">Publishing\Servers{serverId}\GlobalPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-224">до</span><span class="sxs-lookup"><span data-stu-id="87752-224">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-225">GlobalRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="87752-225">GlobalRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-226">Примечание.</span><span class="sxs-lookup"><span data-stu-id="87752-226">Note</span></span></strong><br/><p><span data-ttu-id="87752-227">Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-227">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="87752-228">Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-228">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-229">GLOBALREFRESHINTERVALUNI</span><span class="sxs-lookup"><span data-stu-id="87752-229">GLOBALREFRESHINTERVALUNI</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-230">Указывает единицу интервала (час 0-23, день 0-31).</span><span class="sxs-lookup"><span data-stu-id="87752-230">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="87752-231">0 для часа, 1 — для дня</span><span class="sxs-lookup"><span data-stu-id="87752-231">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-232">Publishing\Servers{serverId}\GlobalPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="87752-232">Publishing\Servers{serverId}\GlobalPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-233">1,1</span><span class="sxs-lookup"><span data-stu-id="87752-233">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-234">UserRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="87752-234">UserRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-235">Примечание.</span><span class="sxs-lookup"><span data-stu-id="87752-235">Note</span></span></strong><br/><p><span data-ttu-id="87752-236">Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-236">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="87752-237">Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-237">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-238">USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="87752-238">USERREFRESHENABLED</span></span> </p></td>
<td align="left"><p><span data-ttu-id="87752-239">Включает обновление публикации пользователей (логическое значение).</span><span class="sxs-lookup"><span data-stu-id="87752-239">Enables user publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-240">Истина (включена); False (отключенное состояние)</span><span class="sxs-lookup"><span data-stu-id="87752-240">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-241">Publishing\Servers {serverId} \ UserEnabled</span><span class="sxs-lookup"><span data-stu-id="87752-241">Publishing\Servers{serverId}\UserEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-242">False</span><span class="sxs-lookup"><span data-stu-id="87752-242">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-243">UserRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="87752-243">UserRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-244">Примечание.</span><span class="sxs-lookup"><span data-stu-id="87752-244">Note</span></span></strong><br/><p><span data-ttu-id="87752-245">Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-245">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="87752-246">Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-246">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-247">USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="87752-247">USERREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-248">Запускает входное обновление публикации пользователя.</span><span class="sxs-lookup"><span data-stu-id="87752-248">Triggers a user publishing refresh onlogon.</span></span> <span data-ttu-id="87752-249">Значением</span><span class="sxs-lookup"><span data-stu-id="87752-249">( Boolean)</span></span></p>
<p><span data-ttu-id="87752-250">Подсчет слов (с пробелами): 60</span><span class="sxs-lookup"><span data-stu-id="87752-250">Word count (with spaces): 60</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-251">Истина (включена); False (отключенное состояние)</span><span class="sxs-lookup"><span data-stu-id="87752-251">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-252">Publishing\Servers{serverId}\UserLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="87752-252">Publishing\Servers{serverId}\UserLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-253">False</span><span class="sxs-lookup"><span data-stu-id="87752-253">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-254">UserRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="87752-254">UserRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-255">Примечание.</span><span class="sxs-lookup"><span data-stu-id="87752-255">Note</span></span></strong><br/><p><span data-ttu-id="87752-256">Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-256">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="87752-257">Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-257">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-258">USERREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="87752-258">USERREFRESHINTERVAL</span></span>     </p></td>
<td align="left"><p><span data-ttu-id="87752-259">Задает интервал обновления публикации с помощью UserRefreshIntervalUnit.</span><span class="sxs-lookup"><span data-stu-id="87752-259">Specifies the publishing refresh interval using the UserRefreshIntervalUnit.</span></span> <span data-ttu-id="87752-260">Чтобы отключить обновление пакета, выберите значение 0.</span><span class="sxs-lookup"><span data-stu-id="87752-260">To disable package refresh, select 0.</span></span></p>
<p><span data-ttu-id="87752-261">Подсчет слов (с пробелами): 85</span><span class="sxs-lookup"><span data-stu-id="87752-261">Word count (with spaces): 85</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-262">Integer (0-744 часов)</span><span class="sxs-lookup"><span data-stu-id="87752-262">Integer (0-744 Hours)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-263">Publishing\Servers{serverId}\UserPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="87752-263">Publishing\Servers{serverId}\UserPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-264">до</span><span class="sxs-lookup"><span data-stu-id="87752-264">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-265">UserRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="87752-265">UserRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-266">Примечание.</span><span class="sxs-lookup"><span data-stu-id="87752-266">Note</span></span></strong><br/><p><span data-ttu-id="87752-267">Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-267">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="87752-268">Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="87752-268">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-269">USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="87752-269">USERREFRESHINTERVALUNIT</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="87752-270">Указывает единицу интервала (час 0-23, день 0-31).</span><span class="sxs-lookup"><span data-stu-id="87752-270">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="87752-271">0 для часа, 1 — для дня</span><span class="sxs-lookup"><span data-stu-id="87752-271">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-272">Publishing\Servers{serverId}\UserPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="87752-272">Publishing\Servers{serverId}\UserPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-273">1,1</span><span class="sxs-lookup"><span data-stu-id="87752-273">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-274">MigrationMode</span><span class="sxs-lookup"><span data-stu-id="87752-274">MigrationMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-275">MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="87752-275">MIGRATIONMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-276">Режим миграции позволяет клиенту App-V изменять сочетания клавиш и FTA для пакетов, созданных с помощью более ранней версии App-V.</span><span class="sxs-lookup"><span data-stu-id="87752-276">Migration mode allows the App-V client to modify shortcuts and FTA’s for packages created using a previous version of App-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-277">True (включенное состояние); False (отключенное состояние)</span><span class="sxs-lookup"><span data-stu-id="87752-277">True(enabled state); False (disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-278">Coexistence\MigrationMode</span><span class="sxs-lookup"><span data-stu-id="87752-278">Coexistence\MigrationMode</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-279">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="87752-279">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-280">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="87752-280">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-281">Позволяет компьютеру с клиентом App-V 5,0 собирать и возвращать определенные сведения об использовании, чтобы помочь нам усовершенствовать приложение.</span><span class="sxs-lookup"><span data-stu-id="87752-281">Allows the computer running the App-V 5.0 Client to collect and return certain usage information to help allow us to further improve the application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-282">0 для отключения; 1 для включения</span><span class="sxs-lookup"><span data-stu-id="87752-282">0 for disabled; 1 for enabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-283">Программное обеспечение/Microsoft/AppV/CEIP/CEIPEnable</span><span class="sxs-lookup"><span data-stu-id="87752-283">SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-284">до</span><span class="sxs-lookup"><span data-stu-id="87752-284">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-285">EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="87752-285">EnablePackageScripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-286">ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="87752-286">ENABLEPACKAGESCRIPTS</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-287">Включает сценарии, определенные в манифесте пакета для файлов конфигурации, которые должны выполняться.</span><span class="sxs-lookup"><span data-stu-id="87752-287">Enables scripts defined in the package manifest of configuration files that should run.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-288">Истина (включена); False (отключенное состояние)</span><span class="sxs-lookup"><span data-stu-id="87752-288">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-289">\Scripting\EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="87752-289">\Scripting\EnablePackageScripts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-290">RoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="87752-290">RoamingFileExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-291">ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="87752-291">ROAMINGFILEEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-292">Указывает пути к файлам относительно% UserProfile%, которые не перемещаются с помощью профиля пользователя&#39;s.</span><span class="sxs-lookup"><span data-stu-id="87752-292">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="87752-293">Пример использования:/ROAMINGFILEEXCLUSIONS =&#39;Desktop; мои рисунки&#39;</span><span class="sxs-lookup"><span data-stu-id="87752-293">Example usage:  /ROAMINGFILEEXCLUSIONS=&#39;desktop;my pictures&#39;</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-294">RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="87752-294">RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-295">ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="87752-295">ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-296">Указывает пути в реестре, которые не перемещаются вместе с профилем пользователя.</span><span class="sxs-lookup"><span data-stu-id="87752-296">Specifies the registry paths that do not roam with a user profile.</span></span> <span data-ttu-id="87752-297">Пример использования:/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</span><span class="sxs-lookup"><span data-stu-id="87752-297">Example usage: /ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-298">Строка</span><span class="sxs-lookup"><span data-stu-id="87752-298">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-299">Integration\RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="87752-299">Integration\RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-300">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-300">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-301">IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="87752-301">IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-302">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-302">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-303">Указывает место для создания символьных ссылок, связанных с текущей версией опубликованного пакета для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="87752-303">Specifies the location to create symbolic links associated with the current version of a per-user published package.</span></span> <span data-ttu-id="87752-304">все виртуальные расширения приложения, например сочетания клавиш и сопоставления типов файлов, будут указывать на этот путь.</span><span class="sxs-lookup"><span data-stu-id="87752-304">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="87752-305">Если путь не указан, символические ссылки не будут использоваться при публикации пакета.</span><span class="sxs-lookup"><span data-stu-id="87752-305">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="87752-306">Например:%localappdata%\Microsoft\AppV\Client\Integration.</span><span class="sxs-lookup"><span data-stu-id="87752-306">For example: %localappdata%\Microsoft\AppV\Client\Integration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-307">Строка</span><span class="sxs-lookup"><span data-stu-id="87752-307">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-308">Integration\IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="87752-308">Integration\IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-309">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-309">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-310">IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="87752-310">IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-311">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-311">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-312">Указывает место для создания символьных ссылок, связанных с текущей версией глобально опубликованного пакета.</span><span class="sxs-lookup"><span data-stu-id="87752-312">Specifies the location to create symbolic links associated with the current version of a globally published package.</span></span> <span data-ttu-id="87752-313">все виртуальные расширения приложения, например сочетания клавиш и сопоставления типов файлов, будут указывать на этот путь.</span><span class="sxs-lookup"><span data-stu-id="87752-313">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="87752-314">Если путь не указан, символические ссылки не будут использоваться при публикации пакета.</span><span class="sxs-lookup"><span data-stu-id="87752-314">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="87752-315">Например:%allusersprofile%\Microsoft\AppV\Client\Integration</span><span class="sxs-lookup"><span data-stu-id="87752-315">For example: %allusersprofile%\Microsoft\AppV\Client\Integration</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-316">Строка</span><span class="sxs-lookup"><span data-stu-id="87752-316">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-317">Integration\IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="87752-317">Integration\IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-318">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-318">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-319">VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="87752-319">VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-320">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-320">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-321">Разделенный запятыми список расширений имен файлов, которые можно использовать, чтобы определить, может ли локально установленное приложение выполняться в виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="87752-321">A comma -delineated list of file name extensions that can be used to determine if a locally installed application can be run in the virtual environment.</span></span></p>
<p><span data-ttu-id="87752-322">Когда при публикации создаются ярлыки, FTAs и другие точки расширения, App-V сравнивает расширение имени файла со списком, если приложение, связанное с точкой расширения, будет установлено локально.</span><span class="sxs-lookup"><span data-stu-id="87752-322">When shortcuts, FTAs, and other extension points are created during publishing, App-V will compare the file name extension to the list if the application that is associated with the extension point is locally installed.</span></span> <span data-ttu-id="87752-323">Если расширение найдено, <strong> </strong> будет добавлен параметр командной строки RunVirtual, и приложение будет выполняться практически.</span><span class="sxs-lookup"><span data-stu-id="87752-323">If the extension is located, the <strong>RunVirtual</strong> command line parameter will be added, and the application will run virtually.</span></span></p>
<p><span data-ttu-id="87752-324">Дополнительные сведения о <strong> </strong> параметре RunVirtual можно найти в разделе <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> выполнение локально установленного приложения в виртуальной среде с виртуализированными приложениями </a> .</span><span class="sxs-lookup"><span data-stu-id="87752-324">For more information about the <strong>RunVirtual</strong> parameter, see <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</a>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-325">Строка</span><span class="sxs-lookup"><span data-stu-id="87752-325">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-326">Integration\VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="87752-326">Integration\VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-327">Значение политики не написано</span><span class="sxs-lookup"><span data-stu-id="87752-327">Policy value not written</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-328">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="87752-328">ReportingEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-329">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-329">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-330">Позволяет клиенту возвращать данные на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="87752-330">Enables the client to return information to a reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-331">Истина (включена); False (отключенное состояние)</span><span class="sxs-lookup"><span data-stu-id="87752-331">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-332">Reporting\EnableReporting</span><span class="sxs-lookup"><span data-stu-id="87752-332">Reporting\EnableReporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-333">False</span><span class="sxs-lookup"><span data-stu-id="87752-333">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-334">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="87752-334">ReportingServerURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-335">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-335">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-336">Задает расположение на сервере отчетов, на котором сохраняются сведения о клиенте.</span><span class="sxs-lookup"><span data-stu-id="87752-336">Specifies the location on the reporting server where client information is saved.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-337">Строка</span><span class="sxs-lookup"><span data-stu-id="87752-337">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-338">Reporting\ReportingServer</span><span class="sxs-lookup"><span data-stu-id="87752-338">Reporting\ReportingServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-339">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-339">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-340">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="87752-340">ReportingDataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-341">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-341">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-342">Задает максимальный размер кэша XML в мегабайтах (МБ) для хранения сведений о отчетах.</span><span class="sxs-lookup"><span data-stu-id="87752-342">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="87752-343">Размер применяется к кэшу в памяти.</span><span class="sxs-lookup"><span data-stu-id="87752-343">The size applies to the cache in memory.</span></span> <span data-ttu-id="87752-344">По достижении этого предела файл журнала будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="87752-344">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="87752-345">Устанавливается значение от 0 до 1024.</span><span class="sxs-lookup"><span data-stu-id="87752-345">Set between 0 and 1024.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-346">Integer [0-1024]</span><span class="sxs-lookup"><span data-stu-id="87752-346">Integer [0-1024]</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-347">Reporting\DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="87752-347">Reporting\DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-348">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-348">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-349">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="87752-349">ReportingDataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-350">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-350">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-351">Задает максимальный размер (в байтах), который должен отправляться серверу для отправки запросов на передачу.</span><span class="sxs-lookup"><span data-stu-id="87752-351">Specifies the maximum size in bytes to transmit to the server for reporting upload requests.</span></span> <span data-ttu-id="87752-352">Это поможет избежать сбоев при неустранимой передаче данных, если журнал достигает значительного размера.</span><span class="sxs-lookup"><span data-stu-id="87752-352">This can help avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="87752-353">Настройка между 1024 и без ограничений.</span><span class="sxs-lookup"><span data-stu-id="87752-353">Set between 1024 and unlimited.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-354">Integer [1024-без ограничений]</span><span class="sxs-lookup"><span data-stu-id="87752-354">Integer [1024 - Unlimited]</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-355">Reporting\DataBlockSize</span><span class="sxs-lookup"><span data-stu-id="87752-355">Reporting\DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-356">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-356">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-357">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="87752-357">ReportingStartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-358">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-358">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-359">Указывает время, в течение которого клиент отправляет данные на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="87752-359">Specifies the time to initiate the client to send data to the reporting server.</span></span> <span data-ttu-id="87752-360">Необходимо указать допустимое целое число в диапазоне от 0-23, соответствующее часу дня.</span><span class="sxs-lookup"><span data-stu-id="87752-360">You must specify a valid integer between 0-23 corresponding to the hour of the day.</span></span> <span data-ttu-id="87752-361">По умолчанию <strong> ReportingStartTime </strong> начнется с текущего дня по 10 P. M. или 22.</span><span class="sxs-lookup"><span data-stu-id="87752-361">By default the <strong>ReportingStartTime</strong> will start on the current day at 10 P.M.or 22.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-362">Примечание.</span><span class="sxs-lookup"><span data-stu-id="87752-362">Note</span></span></strong><br/><p><span data-ttu-id="87752-363">Этот параметр следует настроить на время, когда компьютеры, на которых работает клиент App-V 5,0, не будут работать в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="87752-363">You should configure this setting to a time when computers running the App-V 5.0 client are least likely to be offline.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-364">Целое число (от 0 до 23).</span><span class="sxs-lookup"><span data-stu-id="87752-364">Integer (0 – 23)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-365">Отчетность \ время начала</span><span class="sxs-lookup"><span data-stu-id="87752-365">Reporting\ StartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-366">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-366">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-367">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="87752-367">ReportingInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-368">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-368">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-369">Указывает интервал повтора, который будет использоваться клиентом для повторной отправки данных на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="87752-369">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-370">целое число</span><span class="sxs-lookup"><span data-stu-id="87752-370">Integer</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-371">Reporting\RetryInterval</span><span class="sxs-lookup"><span data-stu-id="87752-371">Reporting\RetryInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-372">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-372">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-373">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="87752-373">ReportingRandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-374">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-374">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-375">Указывает максимальную задержку (в минутах) для данных, отправляемых на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="87752-375">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="87752-376">При запуске запланированной задачи клиент создает произвольную задержку от 0 до <strong> ReportingRandomDelay </strong> и ждет указанное время перед отправкой данных.</span><span class="sxs-lookup"><span data-stu-id="87752-376">When the scheduled task is started, the client generates a random delay between 0 and <strong>ReportingRandomDelay</strong> and will wait the specified duration before sending data.</span></span> <span data-ttu-id="87752-377">Это поможет предотвратить конфликты на сервере.</span><span class="sxs-lookup"><span data-stu-id="87752-377">This can help to prevent collisions on the server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-378">Integer [0-ReportingRandomDelay]</span><span class="sxs-lookup"><span data-stu-id="87752-378">Integer [0 - ReportingRandomDelay]</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-379">Reporting\RandomDelay</span><span class="sxs-lookup"><span data-stu-id="87752-379">Reporting\RandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-380">Значение политики не написано (то же, что и не задано)</span><span class="sxs-lookup"><span data-stu-id="87752-380">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-381">EnableDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="87752-381">EnableDynamicVirtualization</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-382">Важно.</span><span class="sxs-lookup"><span data-stu-id="87752-382">Important</span></span></strong><br/><p><span data-ttu-id="87752-383">Этот параметр доступен только в приложении App-V 5,0 SP2 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="87752-383">This setting is available only with App-V 5.0 SP2 or later.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-384">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-384">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-385">Включает в себя поддерживаемые расширения оболочки, вспомогательные объекты браузера и элементы управления ActiveX, которые должны быть виртуализированы и запущены с виртуальными приложениями.</span><span class="sxs-lookup"><span data-stu-id="87752-385">Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-386">1 (включена), 0 (отключено)</span><span class="sxs-lookup"><span data-stu-id="87752-386">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-387">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization</span><span class="sxs-lookup"><span data-stu-id="87752-387">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Virtualization</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-388">EnablePublishingRefreshUI</span><span class="sxs-lookup"><span data-stu-id="87752-388">EnablePublishingRefreshUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-389">Важно.</span><span class="sxs-lookup"><span data-stu-id="87752-389">Important</span></span></strong><br/><p><span data-ttu-id="87752-390">Этот параметр доступен только для App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="87752-390">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-391">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-391">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-392">Включает индикатор выполнения обновления публикации для компьютера, на котором запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="87752-392">Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-393">1 (включена), 0 (отключено)</span><span class="sxs-lookup"><span data-stu-id="87752-393">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-394">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing</span><span class="sxs-lookup"><span data-stu-id="87752-394">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Publishing</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87752-395">HideUI</span><span class="sxs-lookup"><span data-stu-id="87752-395">HideUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87752-396">Важно.</span><span class="sxs-lookup"><span data-stu-id="87752-396">Important</span></span></strong><br/><p><span data-ttu-id="87752-397">Этот параметр доступен только для App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="87752-397">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87752-398">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-398">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-399">Скрывает индикатор выполнения обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="87752-399">Hides the publishing refresh progress bar.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-400">1 (включена), 0 (отключено)</span><span class="sxs-lookup"><span data-stu-id="87752-400">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87752-401">ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="87752-401">ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-402">Недоступен.</span><span class="sxs-lookup"><span data-stu-id="87752-402">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-403">Указывает список путей процессов (которые могут содержать подстановочные знаки), которые являются кандидатами на использование динамической виртуализации (поддерживаемые расширения оболочки, вспомогательные объекты браузера и элементы ActiveX).</span><span class="sxs-lookup"><span data-stu-id="87752-403">Specifies a list of process paths (that may contain wildcards), which are candidates for using dynamic virtualization (supported shell extensions, browser helper objects, and ActiveX controls).</span></span> <span data-ttu-id="87752-404">Динамическая виртуализация может использовать только процессы, полный путь к которой соответствует одному из этих элементов.</span><span class="sxs-lookup"><span data-stu-id="87752-404">Only processes whose full path matches one of these items can use dynamic virtualization.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-405">Строка</span><span class="sxs-lookup"><span data-stu-id="87752-405">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-406">Virtualization\ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="87752-406">Virtualization\ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="87752-407">Пустая строка.</span><span class="sxs-lookup"><span data-stu-id="87752-407">Empty string.</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="87752-408">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="87752-408">Related topics</span></span>


[<span data-ttu-id="87752-409">Развертывание программы Sequencer и клиента App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="87752-409">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

[<span data-ttu-id="87752-410">Изменение конфигурации клиента App-V 5.0 с помощью шаблона ADMX и групповой политики</span><span class="sxs-lookup"><span data-stu-id="87752-410">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[<span data-ttu-id="87752-411">Развертывание клиента App-V</span><span class="sxs-lookup"><span data-stu-id="87752-411">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)









