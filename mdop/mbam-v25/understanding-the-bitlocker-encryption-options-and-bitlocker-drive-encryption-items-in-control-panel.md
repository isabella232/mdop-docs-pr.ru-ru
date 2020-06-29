---
title: Общие сведения о параметрах шифрования BitLocker и шифровании дисков BitLocker в панели управления
description: Общие сведения о параметрах шифрования BitLocker и шифровании дисков BitLocker в панели управления
author: dansimp
ms.assetid: f8a01cc2-0c77-48b9-8351-8194e80b0cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739b65680ebfdf19f006ee8f3079f7c7e602f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812773"
---
# <span data-ttu-id="665d0-103">Общие сведения о параметрах шифрования BitLocker и шифровании дисков BitLocker в панели управления</span><span class="sxs-lookup"><span data-stu-id="665d0-103">Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel</span></span>


<span data-ttu-id="665d0-104">В этой статье описаны **Параметры шифрования BitLocker** и элементы панели управления **Шифрование дисков BitLocker** , а также рассматриваются следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="665d0-104">This topic describes the **BitLocker Encryption Options** and **BitLocker Drive Encryption** Control Panel items and explains the following:</span></span>

-   <span data-ttu-id="665d0-105">Создание элементов</span><span class="sxs-lookup"><span data-stu-id="665d0-105">How these items are created</span></span>

-   <span data-ttu-id="665d0-106">Задачи, которые они позволят вам выполнять</span><span class="sxs-lookup"><span data-stu-id="665d0-106">Tasks they enable you to perform</span></span>

-   <span data-ttu-id="665d0-107">**Управление BitLocker** контекстное меню "контекстный щелчок", если оно видимо и скрыто, и как сделать его видимым по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="665d0-107">**Manage BitLocker** “right-click” shortcut menu, when it is visible versus hidden, and how to set it to be visible by default</span></span>

## <span data-ttu-id="665d0-108">Параметры шифрования BitLocker и элементы панели управления "шифрование диска" BitLocker</span><span class="sxs-lookup"><span data-stu-id="665d0-108">BitLocker Encryption Options and BitLocker Drive Encryption Control Panel items</span></span>


<span data-ttu-id="665d0-109">В таблице ниже перечислены задачи, которые можно выполнять в каждом элементе панели управления, и описаны способы их создания.</span><span class="sxs-lookup"><span data-stu-id="665d0-109">The following table lists the tasks you can perform from each Control Panel item and describes how these items are created.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="665d0-110">Параметры шифрования BitLocker (MBAM)</span><span class="sxs-lookup"><span data-stu-id="665d0-110">BitLocker Encryption Options (MBAM)</span></span></th>
<th align="left"><span data-ttu-id="665d0-111">Шифрование диска BitLocker (Windows)</span><span class="sxs-lookup"><span data-stu-id="665d0-111">BitLocker Drive Encryption (Windows)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="665d0-112">Задачи, которые можно выполнить</span><span class="sxs-lookup"><span data-stu-id="665d0-112">Tasks you can do</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="665d0-113">Изменение ПИН-кода или пароля</span><span class="sxs-lookup"><span data-stu-id="665d0-113">Change your PIN or password</span></span></p></li>
<li><p><span data-ttu-id="665d0-114">Проверка состояния шифрования для диска</span><span class="sxs-lookup"><span data-stu-id="665d0-114">Check encryption status for a drive</span></span></p></li>
<li><p><span data-ttu-id="665d0-115">Открытие консоли управления TPM</span><span class="sxs-lookup"><span data-stu-id="665d0-115">Open the TPM Management console</span></span></p></li>
<li><p><span data-ttu-id="665d0-116">"Включить BitLocker"</span><span class="sxs-lookup"><span data-stu-id="665d0-116">Turn on BitLocker</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="665d0-117">Приостановить защиту диска</span><span class="sxs-lookup"><span data-stu-id="665d0-117">Suspend protection for a drive</span></span></p></li>
<li><p><span data-ttu-id="665d0-118">Создание резервной копии ключа восстановления</span><span class="sxs-lookup"><span data-stu-id="665d0-118">Back up your recovery key</span></span></p></li>
<li><p><span data-ttu-id="665d0-119">Изменение ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="665d0-119">Change your PIN</span></span></p></li>
<li><p><span data-ttu-id="665d0-120">Отключение BitLocker для диска</span><span class="sxs-lookup"><span data-stu-id="665d0-120">Turn off BitLocker for a drive</span></span></p></li>
<li><p><span data-ttu-id="665d0-121">Включение BitLocker для диска</span><span class="sxs-lookup"><span data-stu-id="665d0-121">Turn on BitLocker for a drive</span></span></p></li>
<li><p><span data-ttu-id="665d0-122">Открытие консоли управления TPM</span><span class="sxs-lookup"><span data-stu-id="665d0-122">Open the TPM Management console</span></span></p></li>
<li><p><span data-ttu-id="665d0-123">Расшифровка диска (отображается только в том случае, если клиент MBAM не установлен)</span><span class="sxs-lookup"><span data-stu-id="665d0-123">Decrypt a drive (appears only if the MBAM Client is NOT installed)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="665d0-124">Создание элемента панели управления</span><span class="sxs-lookup"><span data-stu-id="665d0-124">How the Control Panel item is created</span></span></p></td>
<td align="left"><p><span data-ttu-id="665d0-125">Создается на панели управления при установке клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="665d0-125">Created in Control Panel when you install the MBAM Client.</span></span> <span data-ttu-id="665d0-126">Этот элемент нельзя скрыть.</span><span class="sxs-lookup"><span data-stu-id="665d0-126">This item cannot be hidden.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="665d0-127">Примечание.</span><span class="sxs-lookup"><span data-stu-id="665d0-127">Note</span></span></strong><br/><p><span data-ttu-id="665d0-128">Этот элемент отображается не только в том случае, но и не заменяется элементом панели управления шифрованием диска BitLocker по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="665d0-128">This item appears in addition to, but does not replace, the default BitLocker Drive Encryption Control Panel item.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="665d0-129">По умолчанию отображается на панели управления как часть операционной системы Windows, но ее можно скрыть.</span><span class="sxs-lookup"><span data-stu-id="665d0-129">Appears by default in Control Panel as part of the Windows operating system, but you can hide it.</span></span></p>
<p><span data-ttu-id="665d0-130">Чтобы скрыть его, ознакомьтесь со разделом <a href="hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md" data-raw-source="[Hiding the Default BitLocker Drive Encryption Item in Control Panel](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)"> Скрытие элемента шифрования диска BitLocker по умолчанию на панели управления </a> .</span><span class="sxs-lookup"><span data-stu-id="665d0-130">To hide it, see <a href="hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md" data-raw-source="[Hiding the Default BitLocker Drive Encryption Item in Control Panel](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)">Hiding the Default BitLocker Drive Encryption Item in Control Panel</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="-manage-bitlocker--shortcut-menu"></a><span data-ttu-id="665d0-131">Контекстное меню "Управление BitLocker"</span><span class="sxs-lookup"><span data-stu-id="665d0-131">“Manage BitLocker” shortcut menu</span></span>


<span data-ttu-id="665d0-132">В следующей таблице описано, как зависят от того, установлен ли клиент MBAM в контекстном меню **Manage BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="665d0-132">The following table describes how the **Manage BitLocker** shortcut menu differs depending on whether the MBAM Client is installed.</span></span> <span data-ttu-id="665d0-133">Термин "контекстное меню" обозначает параметры, которые отображаются при щелчке правой кнопкой мыши по диску в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="665d0-133">The term “shortcut menu” refers to options that appear when you right-click a drive in Windows Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="665d0-134">При установке клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="665d0-134">When MBAM Client is installed</span></span></th>
<th align="left"><span data-ttu-id="665d0-135">Если клиент MBAM не установлен</span><span class="sxs-lookup"><span data-stu-id="665d0-135">When MBAM Client is not installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="665d0-136">Видимость контекстного меню</span><span class="sxs-lookup"><span data-stu-id="665d0-136">Visibility of shortcut menu</span></span></p></td>
<td align="left"><p><span data-ttu-id="665d0-137">Параметр "Управление BitLocker" скрыт.</span><span class="sxs-lookup"><span data-stu-id="665d0-137">The Manage BitLocker option is hidden.</span></span></p>
<p><span data-ttu-id="665d0-138">Чтобы сделать параметр Управление BitLocker видимым в контекстном меню, которое выводит на экран параметр для расшифровки диска, удалите следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="665d0-138">To make the Manage BitLocker option visible on the shortcut menu, which displays the option to decrypt a drive, delete the following registry key:</span></span></p>
<pre class="syntax" space="preserve"><code>HKEY_CLASSES_ROOT\Drive\Shell\manage-bde \REG_SZ LegacyDisable</code></pre></td>
<td align="left"><p><span data-ttu-id="665d0-139">В контекстном меню появится параметр Управление BitLocker.</span><span class="sxs-lookup"><span data-stu-id="665d0-139">The Manage BitLocker option appears on the shortcut menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="665d0-140">Возможности пользователей</span><span class="sxs-lookup"><span data-stu-id="665d0-140">What users can do</span></span></p></td>
<td align="left"><p><span data-ttu-id="665d0-141">Если ярлык скрыт, пользователи могут открыть элемент панели управления шифрованием диска BitLocker, но параметр для расшифровки диска недоступен.</span><span class="sxs-lookup"><span data-stu-id="665d0-141">With the shortcut hidden, users can open the BitLocker Drive Encryption Control Panel item, but the option to decrypt a drive is not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="665d0-142">После того как откроется контекстное меню, нажмите кнопку <strong> Управление BitLocker, </strong> чтобы открыть элемент панели управления шифрованием диска BitLocker, на котором выводится параметр для расшифровки диска.</span><span class="sxs-lookup"><span data-stu-id="665d0-142">With the shortcut visible, selecting the <strong>Manage BitLocker</strong> option opens the BitLocker Drive Encryption Control Panel item, which displays the option to decrypt a drive.</span></span></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="665d0-143">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="665d0-143">Related topics</span></span>


[<span data-ttu-id="665d0-144">Администрирование компонентов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="665d0-144">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)



## <span data-ttu-id="665d0-145">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="665d0-145">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="665d0-146">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="665d0-146">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="665d0-147">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="665d0-147">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





