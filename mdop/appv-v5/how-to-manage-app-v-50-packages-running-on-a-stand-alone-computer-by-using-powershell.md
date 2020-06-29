---
title: Управление пакетами App-V 5.0, работающими на автономном компьютере, с помощью PowerShell
description: Управление пакетами App-V 5.0, работающими на автономном компьютере, с помощью PowerShell
author: dansimp
ms.assetid: 1d6c2d25-81ec-4ff8-9262-6b4cf484a376
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b7af1781a7a443a4fcfc8e7d4a92525b34986763
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813920"
---
# <span data-ttu-id="c19f0-103">Управление пакетами App-V 5.0, работающими на автономном компьютере, с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="c19f0-103">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>


<span data-ttu-id="c19f0-104">В следующих разделах объясняется, как выполнять различные задачи управления на отдельном клиентском компьютере с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c19f0-104">The following sections explain how to perform various management tasks on a stand-alone client computer by using PowerShell:</span></span>

-   [<span data-ttu-id="c19f0-105">Возврат списка пакетов</span><span class="sxs-lookup"><span data-stu-id="c19f0-105">To return a list of packages</span></span>](#bkmk-return-pkgs-standalone-posh)

-   [<span data-ttu-id="c19f0-106">Добавление пакета</span><span class="sxs-lookup"><span data-stu-id="c19f0-106">To add a package</span></span>](#bkmk-add-pkgs-standalone-posh)

-   [<span data-ttu-id="c19f0-107">Публикация пакета</span><span class="sxs-lookup"><span data-stu-id="c19f0-107">To publish a package</span></span>](#bkmk-pub-pkg-standalone-posh)

-   [<span data-ttu-id="c19f0-108">Публикация пакета для определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="c19f0-108">To publish a package to a specific user</span></span>](#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="c19f0-109">Добавление и Публикация пакета</span><span class="sxs-lookup"><span data-stu-id="c19f0-109">To add and publish a package</span></span>](#bkmk-add-pub-pkg-standalone-posh)

-   [<span data-ttu-id="c19f0-110">Отмена публикации существующего пакета</span><span class="sxs-lookup"><span data-stu-id="c19f0-110">To unpublish an existing package</span></span>](#bkmk-unpub-pkg-standalone-posh)

-   [<span data-ttu-id="c19f0-111">Отмена публикации пакета для определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="c19f0-111">To unpublish a package for a specific user</span></span>](#bkmk-unpub-pkg-specfc-use)

-   [<span data-ttu-id="c19f0-112">Удаление существующего пакета</span><span class="sxs-lookup"><span data-stu-id="c19f0-112">To remove an existing package</span></span>](#bkmk-remove-pkg-standalone-posh)

-   [<span data-ttu-id="c19f0-113">Разрешение администраторам публиковать и отменять публикацию пакетов</span><span class="sxs-lookup"><span data-stu-id="c19f0-113">To enable only administrators to publish or unpublish packages</span></span>](#bkmk-admins-pub-pkgs)

-   [<span data-ttu-id="c19f0-114">Основные сведения о ожидающих пакетах (UserPending и GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="c19f0-114">Understanding pending packages (UserPending and GlobalPending)</span></span>](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a><span data-ttu-id="c19f0-115">Возврат списка пакетов</span><span class="sxs-lookup"><span data-stu-id="c19f0-115">To return a list of packages</span></span>


<span data-ttu-id="c19f0-116">Используйте следующие сведения, чтобы вернуть список пакетов, которые имеют право определенного пользователя:</span><span class="sxs-lookup"><span data-stu-id="c19f0-116">Use the following information to return a list of packages that are entitled to a specific user:</span></span>

<span data-ttu-id="c19f0-117">**Командлет**: Get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c19f0-117">**Cmdlet**: Get-AppvClientPackage</span></span>

<span data-ttu-id="c19f0-118">**Параметры**:-Name-Version-PackageID-VersionID</span><span class="sxs-lookup"><span data-stu-id="c19f0-118">**Parameters**: -Name -Version -PackageID -VersionID</span></span>

<span data-ttu-id="c19f0-119">**Пример**: Get-AppvClientPackage-Name "ContosoApplication"-версия 2</span><span class="sxs-lookup"><span data-stu-id="c19f0-119">**Example**: Get-AppvClientPackage –Name “ContosoApplication” -Version 2</span></span>

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a><span data-ttu-id="c19f0-120">Добавление пакета</span><span class="sxs-lookup"><span data-stu-id="c19f0-120">To add a package</span></span>


<span data-ttu-id="c19f0-121">Чтобы добавить пакет на компьютер, воспользуйтесь приведенными ниже сведениями.</span><span class="sxs-lookup"><span data-stu-id="c19f0-121">Use the following information to add a package to a computer.</span></span>

<span data-ttu-id="c19f0-122">**Важно!**  В этом примере добавляется только пакет.</span><span class="sxs-lookup"><span data-stu-id="c19f0-122">**Important** This example only adds a package.</span></span> <span data-ttu-id="c19f0-123">Он не публикует пакет для пользователя или компьютера.</span><span class="sxs-lookup"><span data-stu-id="c19f0-123">It does not publish the package to the user or the computer.</span></span>

 

<span data-ttu-id="c19f0-124">**Командлет**: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c19f0-124">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="c19f0-125">**Пример**: $contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV</span><span class="sxs-lookup"><span data-stu-id="c19f0-125">**Example**: $Contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.appv</span></span>

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a><span data-ttu-id="c19f0-126">Публикация пакета</span><span class="sxs-lookup"><span data-stu-id="c19f0-126">To publish a package</span></span>


<span data-ttu-id="c19f0-127">Используйте следующие сведения для публикации пакета, который был добавлен к определенному пользователю или глобально любому пользователю на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c19f0-127">Use the following information to publish a package that has been added to a specific user or globally to any user on the computer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c19f0-128">Метод публикации</span><span class="sxs-lookup"><span data-stu-id="c19f0-128">Publishing method</span></span></th>
<th align="left"><span data-ttu-id="c19f0-129">Командлет и пример</span><span class="sxs-lookup"><span data-stu-id="c19f0-129">Cmdlet and example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c19f0-130">Публикация для пользователя</span><span class="sxs-lookup"><span data-stu-id="c19f0-130">Publishing to the user</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="c19f0-131">Командлет </strong> : Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c19f0-131">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="c19f0-132">Пример </strong> : Publish-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="c19f0-132">Example</strong>: Publish-AppvClientPackage “ContosoApplication”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c19f0-133">Глобальная публикация</span><span class="sxs-lookup"><span data-stu-id="c19f0-133">Publishing globally</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="c19f0-134">Командлет </strong> : Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c19f0-134">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="c19f0-135">Пример </strong> : Publish-AppvClientPackage "ContosoApplication"-Global</span><span class="sxs-lookup"><span data-stu-id="c19f0-135">Example</strong>: Publish-AppvClientPackage “ContosoApplication” -Global</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a><span data-ttu-id="c19f0-136">Публикация пакета для определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="c19f0-136">To publish a package to a specific user</span></span>


<span data-ttu-id="c19f0-137">**Примечание**  Чтобы использовать этот параметр, необходимо воспользоваться пакетом обновления 2 (SP2) для App-V 5,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c19f0-137">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="c19f0-138">Администратор может опубликовать пакет для определенного пользователя, указав дополнительный параметр **–** кодом в командлете **Publish-AppvClientPackage** , где **-** то есть идентификатора безопасности (SID) конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="c19f0-138">An administrator can publish a package to a specific user by specifying the optional **–UserSID** parameter with the **Publish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="c19f0-139">Чтобы использовать этот параметр, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c19f0-139">To use this parameter:</span></span>

-   <span data-ttu-id="c19f0-140">Вы можете запустить этот командлет из сеанса пользователя или администратора.</span><span class="sxs-lookup"><span data-stu-id="c19f0-140">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="c19f0-141">Для использования параметра необходимо войти в систему с помощью учетных данных администратора.</span><span class="sxs-lookup"><span data-stu-id="c19f0-141">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="c19f0-142">Конечный пользователь должен войти в систему.</span><span class="sxs-lookup"><span data-stu-id="c19f0-142">The end user must be logged in.</span></span>

-   <span data-ttu-id="c19f0-143">Необходимо указать идентификатор безопасности (SID) конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="c19f0-143">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="c19f0-144">**Командлет**: Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c19f0-144">**Cmdlet**: Publish-AppvClientPackage</span></span>

<span data-ttu-id="c19f0-145">**Пример**: Publish-AppvClientPackage "ContosoApplication"-от S до 1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="c19f0-145">**Example**: Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a><span data-ttu-id="c19f0-146">Добавление и Публикация пакета</span><span class="sxs-lookup"><span data-stu-id="c19f0-146">To add and publish a package</span></span>


<span data-ttu-id="c19f0-147">Используйте следующие сведения, чтобы добавить пакет на компьютер и опубликовать его для пользователя.</span><span class="sxs-lookup"><span data-stu-id="c19f0-147">Use the following information to add a package to a computer and publish it to the user.</span></span>

<span data-ttu-id="c19f0-148">**Командлет**: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c19f0-148">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="c19f0-149">**Пример**: Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV | Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c19f0-149">**Example**: Add-AppvClientPackage \\\\path\\to\\appv\\package.appv | Publish-AppvClientPackage</span></span>

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a><span data-ttu-id="c19f0-150">Отмена публикации существующего пакета</span><span class="sxs-lookup"><span data-stu-id="c19f0-150">To unpublish an existing package</span></span>


<span data-ttu-id="c19f0-151">Используйте указанные ниже сведения, чтобы отменить публикацию пакета, которому был предоставлен доступ пользователю, но не удалять пакет с компьютера.</span><span class="sxs-lookup"><span data-stu-id="c19f0-151">Use the following information to unpublish a package which has been entitled to a user but not remove the package from the computer.</span></span>

<span data-ttu-id="c19f0-152">**Командлет**: unpublishing-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c19f0-152">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="c19f0-153">**Пример**: unpublishing-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="c19f0-153">**Example**: Unpublish-AppvClientPackage “ContosoApplication”</span></span>

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a><span data-ttu-id="c19f0-154">Отмена публикации пакета для определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="c19f0-154">To unpublish a package for a specific user</span></span>


<span data-ttu-id="c19f0-155">**Примечание**  Чтобы использовать этот параметр, необходимо воспользоваться пакетом обновления 2 (SP2) для App-V 5,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c19f0-155">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="c19f0-156">Администратор может отменить публикацию пакета для определенного пользователя с помощью необязательного параметра **–** кодом в командлете **UNPUBLISH-AppvClientPackage** , где-то есть **—** идентификатора безопасности (SID) конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="c19f0-156">An administrator can unpublish a package for a specific user by using the optional **–UserSID** parameter with the **Unpublish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="c19f0-157">Чтобы использовать этот параметр, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c19f0-157">To use this parameter:</span></span>

-   <span data-ttu-id="c19f0-158">Вы можете запустить этот командлет из сеанса пользователя или администратора.</span><span class="sxs-lookup"><span data-stu-id="c19f0-158">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="c19f0-159">Для использования параметра необходимо войти в систему с помощью учетных данных администратора.</span><span class="sxs-lookup"><span data-stu-id="c19f0-159">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="c19f0-160">Конечный пользователь должен войти в систему.</span><span class="sxs-lookup"><span data-stu-id="c19f0-160">The end user must be logged in.</span></span>

-   <span data-ttu-id="c19f0-161">Необходимо указать идентификатор безопасности (SID) конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="c19f0-161">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="c19f0-162">**Командлет**: unpublishing-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c19f0-162">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="c19f0-163">**Пример**: unpublishing-AppvClientPackage "ContosoApplication"-от S до 1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="c19f0-163">**Example**: Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a><span data-ttu-id="c19f0-164">Удаление существующего пакета</span><span class="sxs-lookup"><span data-stu-id="c19f0-164">To remove an existing package</span></span>


<span data-ttu-id="c19f0-165">Используйте следующие сведения для удаления пакета с компьютера.</span><span class="sxs-lookup"><span data-stu-id="c19f0-165">Use the following information to remove a package from the computer.</span></span>

<span data-ttu-id="c19f0-166">**Командлет**: Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c19f0-166">**Cmdlet**: Remove-AppvClientPackage</span></span>

<span data-ttu-id="c19f0-167">**Пример**: Remove-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="c19f0-167">**Example**: Remove-AppvClientPackage “ContosoApplication”</span></span>

<span data-ttu-id="c19f0-168">**Примечание**  Командлетам App-V назначены переменные для более понятной версии, а не только для ясности, но и для более ранних. назначение не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c19f0-168">**Note** App-V cmdlets have been assigned to variables for the previous examples for clarity only; assignment is not a requirement.</span></span> <span data-ttu-id="c19f0-169">Большинство командлетов можно сочетать так, как показано в этой панели, [чтобы добавить и опубликовать пакет](#bkmk-add-pub-pkg-standalone-posh).</span><span class="sxs-lookup"><span data-stu-id="c19f0-169">Most cmdlets can be combined as displayed in [To add and publish a package](#bkmk-add-pub-pkg-standalone-posh).</span></span> <span data-ttu-id="c19f0-170">Подробные сведения можно найти в подробном руководстве по Windows [App-V 5,0 для клиента PowerShell](https://go.microsoft.com/fwlink/?LinkId=324466).</span><span class="sxs-lookup"><span data-stu-id="c19f0-170">For a detailed tutorial, see [App-V 5.0 Client PowerShell Deep Dive](https://go.microsoft.com/fwlink/?LinkId=324466).</span></span>

 

## <a href="" id="bkmk-admins-pub-pkgs"></a><span data-ttu-id="c19f0-171">Разрешение администраторам публиковать и отменять публикацию пакетов</span><span class="sxs-lookup"><span data-stu-id="c19f0-171">To enable only administrators to publish or unpublish packages</span></span>


<span data-ttu-id="c19f0-172">**Примечание** 
 **Эта функция поддерживается начиная с версии App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="c19f0-172">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="c19f0-173">Используйте следующий командлет и параметр для разрешения публикации и отмены публикации пакетов только для администраторов (не конечных пользователей).</span><span class="sxs-lookup"><span data-stu-id="c19f0-173">Use the following cmdlet and parameter to enable only administrators (not end users) to publish or unpublish packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c19f0-174">Командлет</span><span class="sxs-lookup"><span data-stu-id="c19f0-174">Cmdlet</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c19f0-175">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="c19f0-175">Set-AppvClientConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c19f0-176">Параметр</span><span class="sxs-lookup"><span data-stu-id="c19f0-176">Parameter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c19f0-177">-RequirePublishAsAdmin</span><span class="sxs-lookup"><span data-stu-id="c19f0-177">-RequirePublishAsAdmin</span></span></p>
<p><span data-ttu-id="c19f0-178">Значения параметров:</span><span class="sxs-lookup"><span data-stu-id="c19f0-178">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="c19f0-179">0 – ложь</span><span class="sxs-lookup"><span data-stu-id="c19f0-179">0 - False</span></span></p></li>
<li><p><span data-ttu-id="c19f0-180">1 — истина</span><span class="sxs-lookup"><span data-stu-id="c19f0-180">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c19f0-181">Пример: </strong> Set-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="c19f0-181">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c19f0-182">Чтобы использовать консоль управления App-V для настройки этой конфигурации, ознакомьтесь со [сведениями о том, как опубликовать пакет с помощью консоли управления](how-to-publish-a-package-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="c19f0-182">To use the App-V Management console to set this configuration, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

## <a href="" id="bkmk-understd-pend-pkgs"></a><span data-ttu-id="c19f0-183">Основные сведения о ожидающих пакетах (UserPending и GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="c19f0-183">Understanding pending packages (UserPending and GlobalPending)</span></span>


<span data-ttu-id="c19f0-184">**Начиная с версии App-V 5,0 с пакетом обновления 2 (SP2)**: Если вы запускаете командлет PowerShell, который влияет на пакет, который в данный момент используется, задача, которую вы пытаетесь выполнить, помещается в состояние ожидания.</span><span class="sxs-lookup"><span data-stu-id="c19f0-184">**Starting in App-V 5.0 SP2**: If you run a PowerShell cmdlet that affects a package that is currently in use, the task that you are trying to perform is placed in a pending state.</span></span> <span data-ttu-id="c19f0-185">Например, если вы пытаетесь опубликовать пакет, если используется приложение из этого пакета, а затем выполнить **Get-AppvClientPackage**, в выходных данных командлета появится состояние ожидания, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="c19f0-185">For example, if you try to publish a package when an application in that package is being used, and then run **Get-AppvClientPackage**, the pending status appears in the cmdlet output as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c19f0-186">Элемент вывода командлета</span><span class="sxs-lookup"><span data-stu-id="c19f0-186">Cmdlet output item</span></span></th>
<th align="left"><span data-ttu-id="c19f0-187">Описание</span><span class="sxs-lookup"><span data-stu-id="c19f0-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c19f0-188">UserPending</span><span class="sxs-lookup"><span data-stu-id="c19f0-188">UserPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="c19f0-189">Указывает, имеет ли список в списке ожидающие задачи, которые применяются к пользователю:</span><span class="sxs-lookup"><span data-stu-id="c19f0-189">Indicates whether the listed package has a pending task that is being applied to the user:</span></span></p>
<ul>
<li><p><span data-ttu-id="c19f0-190">True</span><span class="sxs-lookup"><span data-stu-id="c19f0-190">True</span></span></p></li>
<li><p><span data-ttu-id="c19f0-191">False</span><span class="sxs-lookup"><span data-stu-id="c19f0-191">False</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c19f0-192">GlobalPending</span><span class="sxs-lookup"><span data-stu-id="c19f0-192">GlobalPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="c19f0-193">Указывает, имеет ли указанный пакет отложенную задачу, которая будет применена к компьютеру глобально.</span><span class="sxs-lookup"><span data-stu-id="c19f0-193">Indicates whether the listed package has a pending task that is being applied globally to the computer:</span></span></p>
<ul>
<li><p><span data-ttu-id="c19f0-194">True</span><span class="sxs-lookup"><span data-stu-id="c19f0-194">True</span></span></p></li>
<li><p><span data-ttu-id="c19f0-195">False</span><span class="sxs-lookup"><span data-stu-id="c19f0-195">False</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c19f0-196">Задача, ожидающая обработки, будет выполнена позже в соответствии с приведенными ниже правилами.</span><span class="sxs-lookup"><span data-stu-id="c19f0-196">The pending task will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c19f0-197">Тип задачи</span><span class="sxs-lookup"><span data-stu-id="c19f0-197">Task type</span></span></th>
<th align="left"><span data-ttu-id="c19f0-198">Применимое правило</span><span class="sxs-lookup"><span data-stu-id="c19f0-198">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c19f0-199">Пользовательская задача, например Публикация пакета для пользователя</span><span class="sxs-lookup"><span data-stu-id="c19f0-199">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="c19f0-200">Задача будет выполнена после того, как пользователь войдет в систему, а затем снова войдите в нее.</span><span class="sxs-lookup"><span data-stu-id="c19f0-200">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c19f0-201">Глобально на основе задач, например включение глобальной группы подключения</span><span class="sxs-lookup"><span data-stu-id="c19f0-201">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="c19f0-202">Задача, ожидающая выполнения, будет выполнена после отключения компьютера и повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="c19f0-202">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c19f0-203">Дополнительные сведения о незавершенных задачах можно найти в разделе [о приложении App-V 5,0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span><span class="sxs-lookup"><span data-stu-id="c19f0-203">For more information about pending tasks, see [About App-V 5.0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span></span>

<span data-ttu-id="c19f0-204">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="c19f0-204">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="c19f0-205">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="c19f0-205">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="c19f0-206">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="c19f0-206">Got an App-V issue?</span></span>** <span data-ttu-id="c19f0-207">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="c19f0-207">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="c19f0-208">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c19f0-208">Related topics</span></span>


[<span data-ttu-id="c19f0-209">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c19f0-209">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="c19f0-210">Администрирование App-V с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="c19f0-210">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 





