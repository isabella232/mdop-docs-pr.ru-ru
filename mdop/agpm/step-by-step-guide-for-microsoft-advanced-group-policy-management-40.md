---
title: Пошаговое руководство по средству расширенного управления групповыми политиками Майкрософт4.0
description: Пошаговое руководство по средству расширенного управления групповыми политиками Майкрософт4.0
author: dansimp
ms.assetid: dc6f9b16-b1d4-48f3-88bb-f29301f0131c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 819d536451095d23080115799016aa0ac5242dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820199"
---
# <span data-ttu-id="73dfe-103">Пошаговое руководство по средству расширенного управления групповыми политиками Майкрософт4.0</span><span class="sxs-lookup"><span data-stu-id="73dfe-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="73dfe-104">В этом пошаговом руководстве показаны сложные методики для управления групповыми политиками, которые используют консоль управления групповыми политиками (GPMC) и расширенные возможности управления групповыми политиками (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="73dfe-104">This step-by-step guide demonstrates advanced techniques for Group Policy management that use the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="73dfe-105">Функция расширенного управления групповыми политиками расширяет возможности GPMC, обеспечивая:</span><span class="sxs-lookup"><span data-stu-id="73dfe-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="73dfe-106">Стандартные роли для делегирования разрешений на управление объектами групповой политики (GPO) нескольким администраторам групповых политик в дополнение к возможности делегирования доступа к GPO в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="73dfe-106">Standard roles for delegating permissions to manage Group Policy Objects (GPOs) to multiple Group Policy administrators, in addition to the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="73dfe-107">Архив, позволяющий администраторам групповых политик создавать и изменять GPO в автономном режиме перед развертыванием объектов GPO в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="73dfe-107">An archive to enable Group Policy administrators to create and modify GPOs offline before the GPOs are deployed into a production environment.</span></span>

-   <span data-ttu-id="73dfe-108">Возможность вернуться к предыдущей версии GPO и ограничить количество версий, сохраненных в архиве.</span><span class="sxs-lookup"><span data-stu-id="73dfe-108">The ability to roll back to any earlier version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="73dfe-109">Возможность возврата и извлечения объектов GPO, чтобы администраторы групповых политик не случайно перезаписывали работу друг друга.</span><span class="sxs-lookup"><span data-stu-id="73dfe-109">Check-in and check-out capability for GPOs to make sure that Group Policy administrators do not unintentionally overwrite each other's work.</span></span>

-   <span data-ttu-id="73dfe-110">Возможность поиска объектов групповой политики с определенными атрибутами и фильтрации списка объектов групповой политики, отображаемых в списке.</span><span class="sxs-lookup"><span data-stu-id="73dfe-110">The ability to search for GPOs with specific attributes and to filter the list of GPOs displayed.</span></span>

## <span data-ttu-id="73dfe-111">Общие сведения о сценарии РАСШИРЕНного использования функций</span><span class="sxs-lookup"><span data-stu-id="73dfe-111">AGPM scenario overview</span></span>


<span data-ttu-id="73dfe-112">В этом сценарии для каждой роли в разделе управления ГРУППОВыми политиками используется отдельная учетная запись, чтобы показать, как можно управлять групповой политикой в среде с несколькими администраторами групповой политики с разными уровнями разрешений.</span><span class="sxs-lookup"><span data-stu-id="73dfe-112">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment that has multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="73dfe-113">В частности, вы будете выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="73dfe-113">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="73dfe-114">Используя учетную запись, которая входит в группу "Администраторы домена", установите сервер доменных групп и назначьте роль администратора РАСШИРЕНной учетной записи или группе.</span><span class="sxs-lookup"><span data-stu-id="73dfe-114">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="73dfe-115">Используя учетные записи, которым будут назначаться роли для РАСШИРЕНного использования функций, установите Клиентская политика</span><span class="sxs-lookup"><span data-stu-id="73dfe-115">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="73dfe-116">С помощью учетной записи, которая имеет роль администратора РАСШИРЕНного доступа к данным, настройте для них доступ к объектам групповой политики, назначая роли другим учетным записям.</span><span class="sxs-lookup"><span data-stu-id="73dfe-116">Using an account that has the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="73dfe-117">Из учетной записи, в которой находится роль редактора, необходимо запросить создание нового объекта групповой политики, который затем утверждается с помощью учетной записи, которая имеет роль утверждающего.</span><span class="sxs-lookup"><span data-stu-id="73dfe-117">From an account that has the Editor role, request that a new GPO be created that you then approve by using an account that has the Approver role.</span></span> <span data-ttu-id="73dfe-118">С помощью учетной записи редактора извлеките GPO из архива, измените объект групповой политики, проверьте GPO в архиве и запросите развертывание.</span><span class="sxs-lookup"><span data-stu-id="73dfe-118">Use the Editor account to check the GPO out of the archive, edit the GPO, check the GPO into the archive, and then request deployment.</span></span>

-   <span data-ttu-id="73dfe-119">С помощью учетной записи, которая имеет роль утверждающего, проверьте объект групповой политики и разверните его в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="73dfe-119">Using an account that has the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="73dfe-120">С помощью учетной записи, в которой находится роль редактора, создайте шаблон GPO и используйте его в качестве отправной точки для создания нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-120">Using an account that has the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="73dfe-121">С помощью учетной записи, в которой находится роль утверждающего, удалите и восстановите объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-121">Using an account that has the Approver role, delete and restore a GPO.</span></span>

![процесс разработки объектов групповой политики](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="73dfe-123">Требования</span><span class="sxs-lookup"><span data-stu-id="73dfe-123">Requirements</span></span>


<span data-ttu-id="73dfe-124">Компьютеры, на которых вы хотите установить многопользовательскую версию, должны удовлетворять следующим требованиям, и вы должны создать учетные записи для использования в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="73dfe-124">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="73dfe-125">**Примечание**  Если вы установили службу 2,5 РАСШИРЕНного обновления Windows Server® 2003 на Windows Server2008R2 или Windows Server2008 или обновляете версию WindowsVista, но не установили пакеты обновления для Windows7 или WindowsVista® с пакетом обновления Pack1 (SP1), необходимо обновить операционную систему перед обновлением до версии РАСШИРЕНного сервера.</span><span class="sxs-lookup"><span data-stu-id="73dfe-125">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008R2 or Windows Server2008, or are upgrading from WindowsVista with no service packs installed to Windows7 or WindowsVista® with Service Pack1 (SP1), you must upgrade the operating system before you can upgrade to AGPM4.0.</span></span>

<span data-ttu-id="73dfe-126">Если на вашем компьютере установлен компонент РАСШИРЕНного обновления (3,0), вам не нужно обновлять операционную систему перед обновлением до РАСШИРЕНного уровня 4,0</span><span class="sxs-lookup"><span data-stu-id="73dfe-126">If you have AGPM 3.0 installed, you do not have to upgrade the operating system before you upgrade to AGPM 4.0</span></span>

 

<span data-ttu-id="73dfe-127">В смешанной среде, включающей как более новые, так и более старые операционные системы, существует ряд ограничений функциональности, как показано в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="73dfe-127">In a mixed environment that includes both newer and older operating systems, there are some limitations to functionality, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="73dfe-128">Операционная система, на которой работает сервер РАСШИРЕНного выбора 4,0</span><span class="sxs-lookup"><span data-stu-id="73dfe-128">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="73dfe-129">Операционная система, в которой работает клиентская служба РАСШИРЕНного выбора 4,0</span><span class="sxs-lookup"><span data-stu-id="73dfe-129">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="73dfe-130">Состояние поддержки РАСШИРЕНной версии 4,0</span><span class="sxs-lookup"><span data-stu-id="73dfe-130">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="73dfe-131">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="73dfe-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="73dfe-132">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="73dfe-132">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="73dfe-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="73dfe-133">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="73dfe-134">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="73dfe-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="73dfe-135">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="73dfe-135">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="73dfe-136">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="73dfe-136">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="73dfe-137">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="73dfe-137">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="73dfe-138">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="73dfe-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="73dfe-139">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="73dfe-139">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="73dfe-140">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="73dfe-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="73dfe-141">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="73dfe-141">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="73dfe-142">Поддерживается, но не может сообщать или изменять параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="73dfe-142">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="73dfe-143">Требования к серверу для РАСШИРЕНного сервера</span><span class="sxs-lookup"><span data-stu-id="73dfe-143">AGPM Server requirements</span></span>

<span data-ttu-id="73dfe-144">Для работы сервера расширенного управления групповыми политиками требуется Windows Server2008R2, Windows Server2008, Windows7 и GPMC из средств удаленного администрирования сервера (RSAT) или Windows Vista с установленным пакетом обновления 1 (SP1) и GPMC из RSAT.</span><span class="sxs-lookup"><span data-stu-id="73dfe-144">AGPM Server4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from Remote Server Administration Tools (RSAT), or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="73dfe-145">Поддерживаются как 32, так и 64-разрядные версии.</span><span class="sxs-lookup"><span data-stu-id="73dfe-145">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="73dfe-146">Перед установкой сервера РАСШИРЕНного доменных прав необходимо быть членом группы администраторов домена и следующими функциями Windows, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="73dfe-146">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="73dfe-147">ПОЛИТИКОЙ</span><span class="sxs-lookup"><span data-stu-id="73dfe-147">GPMC</span></span>

    -   <span data-ttu-id="73dfe-148">Windows Server2008R2 или Windows Server2008: Если консоль GPMC не отображается, она будет автоматически установлена с помощью расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-148">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="73dfe-149">Windows7: перед установкой многоэлементного управления групповыми политиками необходимо установить GPMC из RSAT.</span><span class="sxs-lookup"><span data-stu-id="73dfe-149">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="73dfe-150">Дополнительные сведения можно найти в разделе [средства администрирования сервера удаленного доступа для Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="73dfe-150">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="73dfe-151">Windows Vista с пакетом обновления 1 (SP1): перед установкой расширенного управления групповыми политиками необходимо установить GPMC из RSAT.</span><span class="sxs-lookup"><span data-stu-id="73dfe-151">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="73dfe-152">Дополнительные сведения можно найти [в разделе средства удаленного администрирования сервера для Windows Vista с пакетом обновления 1](https://go.microsoft.com/fwlink/?LinkID=116179) (SP1) ( https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="73dfe-152">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="73dfe-153">Платформа .NET Framework 3,5 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="73dfe-153">The .NET Framework 3.5 or later versions</span></span>

    -   <span data-ttu-id="73dfe-154">Windows Server2008R2 или Windows7: Если версия .NET Framework 3,5 или более поздней версии отсутствует, .NET Framework 3,5 автоматически устанавливается с помощью расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-154">Windows Server2008R2 or Windows7: If the .NET Framework 3.5 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="73dfe-155">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1): перед установкой расширенного управления групповыми политиками необходимо установить .NET Framework 3,5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="73dfe-155">Windows Server2008 or Windows Vista with SP1: You must install the .NET Framework 3.5 or a later version before you install AGPM.</span></span>

<span data-ttu-id="73dfe-156">Следующие компоненты Windows необходимы для сервера РАСШИРЕНного отслеживания и автоматически устанавливаются, если они отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="73dfe-156">The following Windows features are required by AGPM Server and will be automatically installed if they are not present:</span></span>

-   <span data-ttu-id="73dfe-157">Активация WCF; Активация не по протоколу HTTP</span><span class="sxs-lookup"><span data-stu-id="73dfe-157">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="73dfe-158">Служба активации процессов Windows</span><span class="sxs-lookup"><span data-stu-id="73dfe-158">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="73dfe-159">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="73dfe-159">Process Model</span></span>

    -   <span data-ttu-id="73dfe-160">Среда .NET</span><span class="sxs-lookup"><span data-stu-id="73dfe-160">The .NET Environment</span></span>

    -   <span data-ttu-id="73dfe-161">API конфигурации</span><span class="sxs-lookup"><span data-stu-id="73dfe-161">Configuration APIs</span></span>

### <span data-ttu-id="73dfe-162">Требования клиента к РАСШИРЕНным требованиям</span><span class="sxs-lookup"><span data-stu-id="73dfe-162">AGPM Client requirements</span></span>

<span data-ttu-id="73dfe-163">Для клиента РАСШИРЕНного управления учетными данными требуется Windows Server2008R2, Windows Server2008, Windows7 и GPMC из RSAT или Windows Vista с пакетом обновления 1 (SP1) и консоль GPMC из RSAT.</span><span class="sxs-lookup"><span data-stu-id="73dfe-163">AGPM Client4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from RSAT, or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="73dfe-164">Поддерживаются как 32, так и 64-разрядные версии.</span><span class="sxs-lookup"><span data-stu-id="73dfe-164">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="73dfe-165">На компьютере, на котором запущен сервер с расширенным управлением групповыми политиками, может быть установлен клиент РАСШИРЕНного набора</span><span class="sxs-lookup"><span data-stu-id="73dfe-165">AGPM Client can be installed on a computer that is running AGPM Server.</span></span>

<span data-ttu-id="73dfe-166">Следующие возможности Windows необходимы для клиента с РАСШИРЕНными возможностями, и если не указано иное, они автоматически не установлены.</span><span class="sxs-lookup"><span data-stu-id="73dfe-166">The following Windows features are required by AGPM Client and unless otherwise noted are automatically installed if they are not present:</span></span>

-   <span data-ttu-id="73dfe-167">ПОЛИТИКОЙ</span><span class="sxs-lookup"><span data-stu-id="73dfe-167">GPMC</span></span>

    -   <span data-ttu-id="73dfe-168">Windows Server2008R2 или Windows Server2008: Если консоль GPMC не отображается, она будет автоматически установлена с помощью расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-168">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="73dfe-169">Windows7: перед установкой многоэлементного управления групповыми политиками необходимо установить GPMC из RSAT.</span><span class="sxs-lookup"><span data-stu-id="73dfe-169">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="73dfe-170">Дополнительные сведения можно найти в разделе [средства администрирования сервера удаленного доступа для Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="73dfe-170">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="73dfe-171">Windows Vista с пакетом обновления 1 (SP1): перед установкой расширенного управления групповыми политиками необходимо установить GPMC из RSAT.</span><span class="sxs-lookup"><span data-stu-id="73dfe-171">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="73dfe-172">Дополнительные сведения можно найти [в разделе средства удаленного администрирования сервера для Windows Vista с пакетом обновления 1](https://go.microsoft.com/fwlink/?LinkID=116179) (SP1) ( https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="73dfe-172">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="73dfe-173">Платформа .NET Framework 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="73dfe-173">The .NET Framework 3.0 or later version</span></span>

    -   <span data-ttu-id="73dfe-174">Windows Server2008R2 или Windows7: Если версия .NET Framework 3,0 или более поздней версии отсутствует, .NET Framework 3,5 автоматически устанавливается с помощью расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-174">Windows Server2008R2 or Windows7: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="73dfe-175">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1): Если версия .NET Framework 3,0 или более поздней версии отсутствует, .NET Framework 3,0 автоматически устанавливается с помощью расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-175">Windows Server2008 or Windows Vista with SP1: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.0 is automatically installed by AGPM.</span></span>

### <span data-ttu-id="73dfe-176">Требования к сценарию</span><span class="sxs-lookup"><span data-stu-id="73dfe-176">Scenario requirements</span></span>

<span data-ttu-id="73dfe-177">Перед тем как приступить к созданию этого сценария, создайте четыре учетных записи пользователей.</span><span class="sxs-lookup"><span data-stu-id="73dfe-177">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="73dfe-178">Во время сценария вы будете назначать одну из следующих ролей РАСШИРЕНного управления правами на доступ каждому из этих учетных записей: администратор РАСШИРЕНного доступа (полный доступ), утверждающий, редактор и рецензент.</span><span class="sxs-lookup"><span data-stu-id="73dfe-178">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="73dfe-179">Эти учетные записи должны быть доступны для отправки и получения сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="73dfe-179">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="73dfe-180">Назначьте **объектам GPO** разрешение на доступ к учетным записям, имеющим администратора, утверждающего и (необязательно) РОЛЕЙ редактора расширенного доступа.</span><span class="sxs-lookup"><span data-stu-id="73dfe-180">Assign **Link GPOs** permission to the accounts that have the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="73dfe-181">**Примечание** 
 Разрешение " **связывание объектов GPO** " назначается членам группы администраторов домена и администраторов предприятия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73dfe-181">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="73dfe-182">Чтобы назначить разрешение на доступ к **объектам GPO** для дополнительных пользователей или групп (например, для учетных записей, которые обладают ролями администратора или утверждающего), щелкните узел **домена, а**затем откройте вкладку **Делегирование** , нажмите кнопку **Добавить**, а затем выберите пункт Пользователи или группы, которым нужно назначить разрешение.</span><span class="sxs-lookup"><span data-stu-id="73dfe-182">To assign **Link GPOs** permission to additional users or groups (such as accounts that have the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which you want to assign the permission.</span></span>

 

## <span data-ttu-id="73dfe-183">Инструкции по установке и настройке РАСШИРЕНного изменения параметров</span><span class="sxs-lookup"><span data-stu-id="73dfe-183">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="73dfe-184">Чтобы установить и настроить параметры РАСШИРЕНного конфигурирования, необходимо выполнить описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="73dfe-184">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="73dfe-185">Шаг 1: Установка сервера РАСШИРЕНного набора элементов</span><span class="sxs-lookup"><span data-stu-id="73dfe-185">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="73dfe-186">Шаг 2. Установка клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="73dfe-186">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="73dfe-187">Шаг 3: Настройка подключения к серверу с РАСШИРЕНным интерфейсом</span><span class="sxs-lookup"><span data-stu-id="73dfe-187">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="73dfe-188">Шаг 4: Настройка уведомления по электронной почте</span><span class="sxs-lookup"><span data-stu-id="73dfe-188">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="73dfe-189">Шаг 5: передача прав доступа</span><span class="sxs-lookup"><span data-stu-id="73dfe-189">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="73dfe-190">Шаг 1: Установка сервера РАСШИРЕНного набора элементов</span><span class="sxs-lookup"><span data-stu-id="73dfe-190">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="73dfe-191">На этом этапе необходимо установить сервер РАСШИРЕНного управления правами на рядовом сервере или контроллере домена, который будет запускать службу расширенного управления групповыми политиками, и настроить этот архив.</span><span class="sxs-lookup"><span data-stu-id="73dfe-191">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="73dfe-192">Все операции РАСШИРЕНного управления правами обрабатываются в этой службе Windows и выполняются с учетными данными службы.</span><span class="sxs-lookup"><span data-stu-id="73dfe-192">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="73dfe-193">Архивация, управляемая сервером расширенного управления групповыми политиками, может быть размещена на этом сервере или на другом сервере в том же лесе.</span><span class="sxs-lookup"><span data-stu-id="73dfe-193">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="73dfe-194">Установка сервера расширенного управления групповыми политиками на компьютере, на котором будет размещена служба РАСШИРЕНного управления</span><span class="sxs-lookup"><span data-stu-id="73dfe-194">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="73dfe-195">Войдите в систему под учетной записью, которая входит в группу "Администраторы домена".</span><span class="sxs-lookup"><span data-stu-id="73dfe-195">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="73dfe-196">Запустите компакт-диск с пакетом оптимизации рабочей среды Microsoft и следуйте инструкциям на экране, чтобы выбрать **Расширенное управление групповыми политиками — сервер**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-196">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="73dfe-197">В диалоговом окне **Добро пожаловать** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-197">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="73dfe-198">В диалоговом окне **условия лицензионного соглашения на использование программного обеспечения Microsoft** подтвердите условия и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-198">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

5.  <span data-ttu-id="73dfe-199">В диалоговом окне **путь к приложению** выберите расположение, в которое нужно установить сервер расширенного набора.</span><span class="sxs-lookup"><span data-stu-id="73dfe-199">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="73dfe-200">На компьютере, на котором установлен сервер расширенного управления групповыми политиками, будет размещена служба и Управление архивом.</span><span class="sxs-lookup"><span data-stu-id="73dfe-200">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="73dfe-201">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-201">Click **Next**.</span></span>

6.  <span data-ttu-id="73dfe-202">В диалоговом окне " **архивный путь** " выберите расположение для архива относительно сервера расширенного поиска.</span><span class="sxs-lookup"><span data-stu-id="73dfe-202">In the **Archive Path** dialog box, select a location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="73dfe-203">Путь к архиву может указывать на папку на сервере РАСШИРЕНного поиска и в других местах.</span><span class="sxs-lookup"><span data-stu-id="73dfe-203">The archive path can point to a folder on the AGPM Server or elsewhere.</span></span> <span data-ttu-id="73dfe-204">Тем не менее, необходимо выбрать расположение, в котором достаточно свободного места для хранения всех объектов групповой политики и данных журнала, управляемых этим сервером управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-204">However, you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="73dfe-205">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-205">Click **Next**.</span></span>

7.  <span data-ttu-id="73dfe-206">В диалоговом окне **учетная запись службы расширенного** выбора параметров выберите учетную запись службы, под которой будет выполняться служба расширенного выбора и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-206">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

    <span data-ttu-id="73dfe-207">Эта учетная запись должна входить в группу "Администраторы домена" или, в случае наименее привилегий, в следующих группах каждого домена, управляемых сервером управления групповыми политиками:</span><span class="sxs-lookup"><span data-stu-id="73dfe-207">This account must be a member of the either the Domain Admins group or, for a least-privilege configuration, the following groups in each domain managed by the AGPM Server:</span></span>

    -   <span data-ttu-id="73dfe-208">Владельцы создателей групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-208">Group Policy Creator Owners</span></span>

    -   <span data-ttu-id="73dfe-209">Операторы архива</span><span class="sxs-lookup"><span data-stu-id="73dfe-209">Backup Operators</span></span>

    <span data-ttu-id="73dfe-210">Кроме того, для этой учетной записи требуется разрешение полного доступа для следующих папок:</span><span class="sxs-lookup"><span data-stu-id="73dfe-210">Additionally, this account requires Full Control permission for the following folders:</span></span>

    -   <span data-ttu-id="73dfe-211">Папка архива РАСШИРЕНного доступа к данным, для которой это разрешение автоматически предоставляется во время установки сервера с РАСШИРЕНными правами, если он установлен на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="73dfe-211">The AGPM archive folder, for which this permission is automatically granted during the installation of AGPM Server if it is installed on a local drive.</span></span>

    -   <span data-ttu-id="73dfe-212">Папка Local System Temp, обычно%windir%\\Temp.</span><span class="sxs-lookup"><span data-stu-id="73dfe-212">The local system temp folder, typically %windir%\\temp.</span></span>

8.  <span data-ttu-id="73dfe-213">В диалоговом окне **Владелец архива** выберите учетную запись или группу, которой назначена роль администратора расширенного управления правами (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="73dfe-213">In the **Archive Owner** dialog box, select an account or group to which you assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="73dfe-214">Администраторы РАСШИРЕНного доступа к учетным группам могут назначать роли и разрешения РАСШИРЕНных групповых политик другим администраторам групповой политики, чтобы позже можно было назначить роль администратора с помощью функции РАСШИРЕНного администрирования дополнительным администраторам групповых политик.</span><span class="sxs-lookup"><span data-stu-id="73dfe-214">AGPM Administrators can assign AGPM roles and permissions to other Group Policy administrators, so that later you can assign the role of AGPM Administrator to additional Group Policy administrators.</span></span> <span data-ttu-id="73dfe-215">Для этого сценария выберите учетную запись, которая будет использоваться в роли администратора РАСШИРЕНного администрирования.</span><span class="sxs-lookup"><span data-stu-id="73dfe-215">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="73dfe-216">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-216">Click **Next**.</span></span>

9.  <span data-ttu-id="73dfe-217">В диалоговом окне **Настройка порта** введите порт для прослушивания службой расширенного выбора ключа.</span><span class="sxs-lookup"><span data-stu-id="73dfe-217">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="73dfe-218">Не снимайте флажок **Добавить исключение для порта в брандмауэр** , если только вы не настраиваете исключения для порта вручную или не используйте правила для настройки исключений.</span><span class="sxs-lookup"><span data-stu-id="73dfe-218">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="73dfe-219">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-219">Click **Next**.</span></span>

10. <span data-ttu-id="73dfe-220">В диалоговом окне **языки** выберите один или несколько языков интерфейса, которые нужно установить для сервера с расширенным интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="73dfe-220">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="73dfe-221">Нажмите кнопку **установить**, а затем — **Готово** , чтобы завершить работу мастера установки.</span><span class="sxs-lookup"><span data-stu-id="73dfe-221">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="73dfe-222">**Внимание!**  Не изменяйте параметры службы РАСШИРЕНного **управления правами с помощью средств администрирования** и **служб** в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="73dfe-222">**Caution** Do not change settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="73dfe-223">Это может привести к невозможности запуска службы РАСШИРЕНного рассчета.</span><span class="sxs-lookup"><span data-stu-id="73dfe-223">Doing this can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="73dfe-224">Сведения о том, как изменить параметры службы, приведены в разделе Справка по расширенному управлению групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-224">For information about how to change settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="73dfe-225">Шаг 2. Установка клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="73dfe-225">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="73dfe-226">Каждый администратор групповой политики — любой пользователь, который создает, редактирует, развертывает или удаляет GPO, должен установить на компьютеры, которые они используют, для управления объектами групповой политики, клиент с РАСШИРЕНными правами.</span><span class="sxs-lookup"><span data-stu-id="73dfe-226">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="73dfe-227">Узел контрольных изменений, который вы используете для выполнения многих задач управления GPO, отображается в консоли управления групповыми политиками только в том случае, если вы установили клиент РАСШИРЕНного управления правами.</span><span class="sxs-lookup"><span data-stu-id="73dfe-227">The Change Control node, which you use to perform many of the GPO management tasks, appears in the Group Policy Management Console only if you install the AGPM Client.</span></span> <span data-ttu-id="73dfe-228">Для этого сценария необходимо установить клиентская версия с РАСШИРЕНным Управлением по крайней мере на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="73dfe-228">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="73dfe-229">На компьютерах конечных пользователей, которые не выполняют администрирование групповой политики, вам не нужно устанавливать клиент с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-229">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="73dfe-230">Установка клиента с расширенным управлением групповыми политиками на компьютере администратора групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-230">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="73dfe-231">Запустите компакт-диск с пакетом оптимизации рабочей среды Microsoft и следуйте инструкциям на экране, чтобы выбрать **Расширенное управление групповыми политиками — клиент**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-231">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="73dfe-232">В диалоговом окне **Добро пожаловать** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-232">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="73dfe-233">В диалоговом окне **условия лицензионного соглашения на использование программного обеспечения Microsoft** подтвердите условия и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-233">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

4.  <span data-ttu-id="73dfe-234">В диалоговом окне **путь к приложению** выберите расположение для установки клиента с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-234">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="73dfe-235">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-235">Click **Next**.</span></span>

5.  <span data-ttu-id="73dfe-236">В диалоговом окне **сервер расширенного выбора сервера** введите DNS-имя или IP-адрес сервера расширенного выбора и порта, к которому вы хотите подключиться.</span><span class="sxs-lookup"><span data-stu-id="73dfe-236">In the **AGPM Server** dialog box, type the DNS name or IP address for the AGPM Server and the port to which you want to connect.</span></span> <span data-ttu-id="73dfe-237">Портом по умолчанию для службы РАСШИРЕНного обслуживания не является 4600.</span><span class="sxs-lookup"><span data-stu-id="73dfe-237">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="73dfe-238">Не снимайте флажок **Разрешить использование консоли управления Майкрософт через брандмауэр** , если только вы не настраиваете исключения для порта вручную или не используйте правила для настройки исключений.</span><span class="sxs-lookup"><span data-stu-id="73dfe-238">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="73dfe-239">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-239">Click **Next**.</span></span>

6.  <span data-ttu-id="73dfe-240">В диалоговом окне **языки** выберите один или несколько языков интерфейса, которые нужно установить для клиента с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-240">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="73dfe-241">Нажмите кнопку **установить**, а затем — **Готово** , чтобы завершить работу мастера установки.</span><span class="sxs-lookup"><span data-stu-id="73dfe-241">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="73dfe-242">Шаг 3: Настройка подключения к серверу с РАСШИРЕНным интерфейсом</span><span class="sxs-lookup"><span data-stu-id="73dfe-242">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="73dfe-243">Управление ГРУППОВыми политиками сохраняет все версии каждого управляемого объекта групповой политики (GPO), то есть каждый GPO, для которого в РАСШИРЕНном архиве находятся элементы управления изменениями.</span><span class="sxs-lookup"><span data-stu-id="73dfe-243">AGPM stores all versions of each controlled Group Policy Object (GPO), that is, each GPO for which AGPM provides change control, in a central archive.</span></span> <span data-ttu-id="73dfe-244">Это позволяет администраторам групповых политик просматривать и изменять GPO в автономном режиме без немедленного воздействия на развернутую версию каждого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-244">This lets Group Policy administrators view and change GPOs offline without immediately affecting the deployed version of each GPO.</span></span>

<span data-ttu-id="73dfe-245">На этом этапе необходимо настроить соединение с сервером РАСШИРЕНного администрирования и убедиться, что все администраторы групповой политики подключаются к одному и тому же серверу.</span><span class="sxs-lookup"><span data-stu-id="73dfe-245">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="73dfe-246">(Сведения о настройке нескольких серверов расширенного управления групповыми политиками см. в разделе Справка по расширенному управлению групповой политикой.)</span><span class="sxs-lookup"><span data-stu-id="73dfe-246">(For information about how to configure multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="73dfe-247">Настройка подключения к серверу РАСШИРЕНного конфигурирования для всех администраторов групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-247">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="73dfe-248">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которую выбрали в качестве владельца архива.</span><span class="sxs-lookup"><span data-stu-id="73dfe-248">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="73dfe-249">У этого пользователя есть роль администратора управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="73dfe-249">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="73dfe-250">Нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем — **Управление групповой политикой** , чтобы открыть консоль управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-250">Click **Start**, point to **Administrative Tools**, and then click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="73dfe-251">Изменение объекта групповой политики, применяемого ко всем администраторам групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-251">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="73dfe-252">В окне **редактора управления групповыми политиками** дважды щелкните элемент **Конфигурация пользователя**, **политики**, **Административные шаблоны**, **компоненты Windows**и управление **групповыми**политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-252">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="73dfe-253">В области сведений дважды щелкните элемент расширенной настройки и выберите **сервер по умолчанию (все домены)**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-253">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="73dfe-254">В окне **Свойства** выберите параметр **включена** и введите DNS-имя или IP-адрес и порт (например, **Server.contoso.com:4600**) для сервера, на котором размещается Архив.</span><span class="sxs-lookup"><span data-stu-id="73dfe-254">In the **Properties** window, select **Enabled** and type the DNS name or IP address and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="73dfe-255">По умолчанию служба РАСШИРЕНного использования порта использует порт 4600.</span><span class="sxs-lookup"><span data-stu-id="73dfe-255">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="73dfe-256">Нажмите кнопку **ОК**, а затем закройте окно **редактора управления групповыми политиками** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-256">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="73dfe-257">После обновления групповой политики соединение с сервером РАСШИРЕНного политики для каждого администратора будет настроено.</span><span class="sxs-lookup"><span data-stu-id="73dfe-257">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="73dfe-258">Шаг 4: Настройка уведомления по электронной почте</span><span class="sxs-lookup"><span data-stu-id="73dfe-258">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="73dfe-259">Как Администратор расширенного управления групповыми политиками (полный доступ) вы указываете адреса электронной почты утверждающих и администраторов РАСШИРЕНного доступа, которым будет отправлено сообщение электронной почты с запросом, когда редактор попытается создать, развернуть или удалить объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-259">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message that contains a request is sent when an Editor tries to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="73dfe-260">Кроме того, вы можете определить псевдоним, из которого отправляются эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="73dfe-260">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="73dfe-261">Настройка уведомления по электронной почте для РАСШИРЕНного</span><span class="sxs-lookup"><span data-stu-id="73dfe-261">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="73dfe-262">В **редакторе управления групповыми политиками** перейдите к папке " **Управление изменениями** ".</span><span class="sxs-lookup"><span data-stu-id="73dfe-262">In **Group Policy Management Editor** , navigate to the **Change Control** folder</span></span> 

2.  <span data-ttu-id="73dfe-263">В области сведений откройте вкладку **Делегирование домена** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-263">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="73dfe-264">В поле **из адреса электронной почты** введите псевдоним электронной почты для расширенного вида, из которого нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="73dfe-264">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="73dfe-265">В поле **адрес электронной почты** введите адрес электронной почты учетной записи пользователя, которому вы хотите назначить роль утверждающего.</span><span class="sxs-lookup"><span data-stu-id="73dfe-265">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="73dfe-266">В поле **SMTP-сервер** введите допустимый почтовый SMTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="73dfe-266">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="73dfe-267">В полях **имя пользователя** и **пароль** введите учетные данные пользователя, у которого есть доступ к службе SMTP.</span><span class="sxs-lookup"><span data-stu-id="73dfe-267">In the **User name** and **Password** fields, type the credentials of a user who has access to the SMTP service.</span></span> <span data-ttu-id="73dfe-268">Нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-268">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="73dfe-269">Шаг 5: передача прав доступа</span><span class="sxs-lookup"><span data-stu-id="73dfe-269">Step 5: Delegate access</span></span>

<span data-ttu-id="73dfe-270">Как Администратор расширенного управления групповыми политиками (режим полного доступа) вы делегируйте доступ к объектам GPO на уровне домена, назначая роли учетной записи каждого администратора групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-270">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="73dfe-271">**Примечание**  Вы также можете делегировать доступ на уровне объекта групповой политики, а не на уровне домена.</span><span class="sxs-lookup"><span data-stu-id="73dfe-271">**Note** You can also delegate access at the GPO level instead of the domain level.</span></span> <span data-ttu-id="73dfe-272">Дополнительные сведения можно найти в разделе Справка по расширенному управлению групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="73dfe-272">For more information, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="73dfe-273">**Важно!**  Вы должны ограничить членство в группе Владельцы создателей групповой политики, чтобы не использовать управление правами на доступ к объектам GPO.</span><span class="sxs-lookup"><span data-stu-id="73dfe-273">**Important** You should restrict membership in the Group Policy Creator Owners group so that it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="73dfe-274">(В **консоли управления групповыми политиками**щелкните **объекты групповой политики** в лесу и домене, в которых вы хотите управлять объектами GPO, выберите пункт **Делегирование**и настройте параметры в соответствии с потребностями Организации.)</span><span class="sxs-lookup"><span data-stu-id="73dfe-274">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="73dfe-275">Передача доступа ко всем объектам групповой политики внутри домена</span><span class="sxs-lookup"><span data-stu-id="73dfe-275">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="73dfe-276">На вкладке **доменное делегирование** нажмите кнопку **Добавить** , выберите учетную запись администратора групповой политики, которая будет использоваться в качестве утверждающего, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-276">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="73dfe-277">В диалоговом окне **Добавление группы или пользователя** выберите роль **утверждающего** , чтобы назначить ей роль учетной записи, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-277">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="73dfe-278">(Эта роль включает в себя роль проверяющего.)</span><span class="sxs-lookup"><span data-stu-id="73dfe-278">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="73dfe-279">Нажмите кнопку **Добавить** , выберите учетную запись пользователя администратора групповой политики, которая будет использоваться в качестве редактора, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-279">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="73dfe-280">В диалоговом окне **Добавление группы или пользователя** выберите роль " **Редактор** ", чтобы назначить эту роль учетной записи, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-280">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="73dfe-281">(Эта роль включает в себя роль проверяющего.)</span><span class="sxs-lookup"><span data-stu-id="73dfe-281">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="73dfe-282">Нажмите кнопку **Добавить** , выберите учетную запись администратора групповой политики, которая будет использоваться в качестве рецензента, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-282">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="73dfe-283">В диалоговом окне **Добавление группы или пользователя** выберите роль **проверяющего** , чтобы назначить учетной записи только эту роль.</span><span class="sxs-lookup"><span data-stu-id="73dfe-283">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="73dfe-284">Инструкции по управлению объектами групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-284">Steps for managing GPOs</span></span>


<span data-ttu-id="73dfe-285">Для создания, изменения, проверки и развертывания объектов групповой политики с помощью РАСШИРЕНного использования функций необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="73dfe-285">You must complete the following steps to create, edit, review, and deploy GPOs by using AGPM.</span></span> <span data-ttu-id="73dfe-286">Кроме того, вы создадите шаблон, удалите объект групповой политики и восстановите удаленный объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-286">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="73dfe-287">Действие 1: создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-287">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="73dfe-288">Действие 2: изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-288">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="73dfe-289">Шаг 3: Проверка и развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-289">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="73dfe-290">Шаг 4: использование шаблона для создания объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-290">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="73dfe-291">Шаг 5: удаление и восстановление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-291">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="73dfe-292">Действие 1: создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-292">Step 1: Create a GPO</span></span>

<span data-ttu-id="73dfe-293">В среде с несколькими администраторами групповой политики пользователи, которым назначена роль редактора, могут запросить создание новых GPO.</span><span class="sxs-lookup"><span data-stu-id="73dfe-293">In an environment that has multiple Group Policy administrators, those with the Editor role can request that new GPOs be created.</span></span> <span data-ttu-id="73dfe-294">Тем не менее, этот запрос должен быть утвержден участником с ролью утверждающего.</span><span class="sxs-lookup"><span data-stu-id="73dfe-294">However, that request must be approved by someone with the Approver role.</span></span>

<span data-ttu-id="73dfe-295">На этом этапе вы используете учетную запись с ролью редактора, чтобы запросить создание нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-295">In this step, you use an account that has the Editor role to request that a new GPO be created.</span></span> <span data-ttu-id="73dfe-296">С помощью учетной записи, которая имеет роль утверждающего, вы утверждаете этот запрос для создания объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-296">Using an account that has the Approver role, you approve this request to create the GPO.</span></span>

**<span data-ttu-id="73dfe-297">Запрос создания нового объекта групповой политики с помощью расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="73dfe-297">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="73dfe-298">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которой назначена роль "редактор".</span><span class="sxs-lookup"><span data-stu-id="73dfe-298">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="73dfe-299">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-299">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="73dfe-300">Щелкните правой кнопкой мыши узел **контроль изменений** и выберите команду **создать управляемый объект групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-300">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="73dfe-301">В диалоговом окне **новый управляемый объект групповой политики** :</span><span class="sxs-lookup"><span data-stu-id="73dfe-301">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="73dfe-302">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-302">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="73dfe-303">Введите **MyGPO** в качестве имени нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-303">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="73dfe-304">Введите Примечание для нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-304">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="73dfe-305">Нажмите кнопку **создать в реальном времени** , чтобы новый объект групповой политики развернут в рабочей среде сразу после утверждения.</span><span class="sxs-lookup"><span data-stu-id="73dfe-305">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="73dfe-306">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-306">Click **Submit**.</span></span>

5.  <span data-ttu-id="73dfe-307">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-307">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="73dfe-308">Новый объект групповой политики появится на вкладке **ожидающие** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-308">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="73dfe-309">Утверждение ожидающего запроса на создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-309">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="73dfe-310">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которая имеет роль утверждающего в РАСШИРЕНном.</span><span class="sxs-lookup"><span data-stu-id="73dfe-310">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="73dfe-311">Откройте папку "Входящие" электронной почты для учетной записи и обратите внимание на то, что вы получили сообщение электронной почты от псевдонима с помощью запроса редактора, чтобы создать объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-311">Open the e-mail inbox for the account, and notice that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="73dfe-312">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-312">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="73dfe-313">На вкладке **содержание** откройте вкладку **ожидается** , чтобы отобразить ожидающие GPO.</span><span class="sxs-lookup"><span data-stu-id="73dfe-313">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="73dfe-314">Щелкните правой кнопкой мыши **MyGPO**и выберите команду **утвердить**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-314">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="73dfe-315">Нажмите кнопку **Да** , чтобы подтвердить утверждение, и переместите объект групповой политики на вкладку **Управление** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-315">Click **Yes** to confirm approval and move the GPO to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="73dfe-316">Действие 2: изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-316">Step 2: Edit a GPO</span></span>

<span data-ttu-id="73dfe-317">С помощью объектов групповой политики можно настраивать параметры компьютера или пользователя и развертывать их на нескольких компьютерах или в других пользователей.</span><span class="sxs-lookup"><span data-stu-id="73dfe-317">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="73dfe-318">На этом этапе вы используете учетную запись с ролью "редактор" для извлечения объекта групповой политики из архива, изменения объекта групповой политики в автономном режиме, проверки редактируемого GPO в архиве и запроса развертывания объекта групповой политики в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="73dfe-318">In this step, you use an account that has the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="73dfe-319">В этом сценарии вы можете настроить параметр в объекте групповой политики таким образом, чтобы пароль имел длину не менее восьми символов.</span><span class="sxs-lookup"><span data-stu-id="73dfe-319">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters long.</span></span>

**<span data-ttu-id="73dfe-320">Извлечение GPO из архива для редактирования</span><span class="sxs-lookup"><span data-stu-id="73dfe-320">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="73dfe-321">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которая имеет роль редактора в РАСШИРЕНном наборе элементов.</span><span class="sxs-lookup"><span data-stu-id="73dfe-321">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="73dfe-322">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="73dfe-323">На вкладке **содержание** в области сведений откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-323">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="73dfe-324">Щелкните правой кнопкой мыши **MyGPO**и выберите пункт **извлечь.**</span><span class="sxs-lookup"><span data-stu-id="73dfe-324">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="73dfe-325">Введите Примечание, которое будет отображаться в истории объекта групповой политики, когда он извлечен, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-325">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="73dfe-326">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-326">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="73dfe-327">На вкладке **Управление** состоянием GPO считается **извлеченным**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-327">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="73dfe-328">Изменение GPO в автономном режиме и Настройка минимальной длины пароля</span><span class="sxs-lookup"><span data-stu-id="73dfe-328">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="73dfe-329">На вкладке **управляемые** щелкните правой кнопкой мыши **MyGPO**и выберите команду **изменить** , чтобы открыть окно **редактора управления групповыми политиками** и изменить автономную копию объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-329">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="73dfe-330">Для этого сценария настройте минимальную длину пароля:</span><span class="sxs-lookup"><span data-stu-id="73dfe-330">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="73dfe-331">В разделе **Конфигурация компьютера**дважды щелкните **политики**, **Параметры Windows**, **Параметры безопасности**, **политики учетных записей**и **политики паролей**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-331">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="73dfe-332">В области сведений дважды щелкните элемент **Минимальная длина пароля**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-332">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="73dfe-333">В окне "Свойства" установите флажок **определить этот параметр политики** , укажите число символов **8**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-333">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="73dfe-334">Закройте окно **редактора управления групповыми политиками** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-334">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="73dfe-335">Проверка GPO в архиве</span><span class="sxs-lookup"><span data-stu-id="73dfe-335">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="73dfe-336">На вкладке **Управление** , щелкните правой кнопкой мыши **MyGPO** и выберите команду **вернуть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-336">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="73dfe-337">Введите примечание и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-337">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="73dfe-338">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-338">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="73dfe-339">На вкладке **Управление** состоянием объекта групповой политики считается **возвращенное**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-339">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="73dfe-340">Запрос развертывания объекта групповой политики в рабочей среде</span><span class="sxs-lookup"><span data-stu-id="73dfe-340">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="73dfe-341">На вкладке **Управление** , щелкните правой кнопкой мыши **MyGPO** и выберите команду **развернуть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-341">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="73dfe-342">Поскольку эта учетная запись не является администратором утверждения или РАСШИРЕНного администрирования, необходимо отправить запрос на развертывание.</span><span class="sxs-lookup"><span data-stu-id="73dfe-342">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="73dfe-343">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-343">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="73dfe-344">Введите Примечание, которое будет отображаться в журнале объекта групповой политики, а затем нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-344">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="73dfe-345">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-345">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="73dfe-346">**MyGPO** отображается в списке объектов групповой политики на вкладке **ожидающие** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-346">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="73dfe-347">Шаг 3: Проверка и развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-347">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="73dfe-348">На этом этапе вы действуете как утверждающий, создавая отчеты и анализируя параметры и изменяя параметры в объекте групповой политики, чтобы определить, нужно ли их утверждать.</span><span class="sxs-lookup"><span data-stu-id="73dfe-348">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="73dfe-349">После того как вы оцените объект групповой политики, вы развернете его в производственную среду и свяжите объект групповой политики с доменом или подразделением (OU).</span><span class="sxs-lookup"><span data-stu-id="73dfe-349">After you evaluate the GPO, you deploy it to the production environment and link the GPO to a domain or an organizational unit (OU).</span></span> <span data-ttu-id="73dfe-350">GPO вступает в силу, когда групповая политика обновляется на компьютерах в этом домене или OU.</span><span class="sxs-lookup"><span data-stu-id="73dfe-350">The GPO takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="73dfe-351">Просмотр параметров в объекте групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-351">To review settings in the GPO</span></span>**

1. <span data-ttu-id="73dfe-352">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему под учетной записью пользователя, которому назначена роль утверждающего в расширенном управлении правами.</span><span class="sxs-lookup"><span data-stu-id="73dfe-352">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="73dfe-353">Любой администратор групповой политики с ролью проверяющего, который входит в состав других ролей, может просматривать параметры в объекте групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-353">Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.</span></span>

2. <span data-ttu-id="73dfe-354">Откройте папку "Входящие" электронной почты для учетной записи и обратите внимание на то, что вы получили сообщение электронной почты от псевдонима РАСШИРЕНного использования запроса редактора для развертывания объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-354">Open the e-mail inbox for the account and notice that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="73dfe-355">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-355">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="73dfe-356">На вкладке **содержание** в области сведений откройте вкладку **ожидается** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-356">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="73dfe-357">Дважды щелкните **MyGPO** , чтобы отобразить историю.</span><span class="sxs-lookup"><span data-stu-id="73dfe-357">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="73dfe-358">Проверьте параметры в последней версии MyGPO:</span><span class="sxs-lookup"><span data-stu-id="73dfe-358">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="73dfe-359">В окне " **Журнал** " щелкните правой кнопкой мыши версию объекта групповой политики с последней меткой времени, выберите пункт **Параметры**, а затем — **отчет HTML** , чтобы отобразить сводку по параметрам объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-359">In the **History** window, right-click the GPO version with the most recent time stamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="73dfe-360">В веб-браузере нажмите кнопку **Показать все** , чтобы отобразить все параметры в объекте групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-360">In the Web browser, click **show all** to display all the settings in the GPO.</span></span> <span data-ttu-id="73dfe-361">Закройте браузер.</span><span class="sxs-lookup"><span data-stu-id="73dfe-361">Close the browser.</span></span>

7. <span data-ttu-id="73dfe-362">Сравните последнюю версию MyGPO с первой версией, возвращенной в Архив:</span><span class="sxs-lookup"><span data-stu-id="73dfe-362">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="73dfe-363">В окне " **Журнал** " выберите версию объекта групповой политики с последней меткой времени.</span><span class="sxs-lookup"><span data-stu-id="73dfe-363">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="73dfe-364">Нажмите клавишу CTRL, а затем выберите самую старую версию \*\*GPO, которой не является \*\*\* \* \ \ \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="73dfe-364">Press CTRL and then click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="73dfe-365">Нажмите кнопку **различия** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-365">Click the **Differences** button.</span></span> <span data-ttu-id="73dfe-366">Раздел **политики учетных записей и политика паролей** выделены зеленым цветом и предшествует " **\ [+ \]**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-366">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**.</span></span> <span data-ttu-id="73dfe-367">Это указывает на то, что параметр настроен только в последней версии GPO.</span><span class="sxs-lookup"><span data-stu-id="73dfe-367">This indicates that the setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="73dfe-368">Выберите политики **учетных записей и политика паролей**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-368">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="73dfe-369">Параметр **минимальной длины пароля** также выделяется зеленым цветом и предшествует **\ [+ \]**, что указывает на то, что оно настроено только в последней версии GPO.</span><span class="sxs-lookup"><span data-stu-id="73dfe-369">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="73dfe-370">Закройте веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="73dfe-370">Close the Web browser.</span></span>

**<span data-ttu-id="73dfe-371">Развертывание объекта групповой политики в рабочей среде</span><span class="sxs-lookup"><span data-stu-id="73dfe-371">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="73dfe-372">На вкладке **Ожидание** щелкните правой кнопкой мыши **MyGPO** и выберите команду **утвердить**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-372">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="73dfe-373">Введите Примечание для включения в историю объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-373">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="73dfe-374">Щелкните **Да**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-374">Click **Yes**.</span></span> <span data-ttu-id="73dfe-375">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-375">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="73dfe-376">Объект групповой политики развернут в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="73dfe-376">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="73dfe-377">Связывание объекта групповой политики с доменом или подразделением</span><span class="sxs-lookup"><span data-stu-id="73dfe-377">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="73dfe-378">В консоли управления групповыми политиками щелкните правой кнопкой мыши домен или подразделение (OU), к которому вы хотите применить настраиваемый объект групповой политики, а затем выберите команду **связать существующий объект групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-378">In the GPMC, right-click either the domain or an organizational unit (OU) to which you want to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="73dfe-379">В диалоговом окне **Выбор объекта групповой политики** щелкните **MyGPO**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-379">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="73dfe-380">Шаг 4: использование шаблона для создания объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-380">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="73dfe-381">На этом этапе вы используете учетную запись с ролью "редактор" для создания и использования шаблона.</span><span class="sxs-lookup"><span data-stu-id="73dfe-381">In this step, you use an account that has the Editor role to create and use a template.</span></span> <span data-ttu-id="73dfe-382">Этот шаблон — это статическая версия GPO, которая используется в качестве отправной точки для создания новых объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-382">That template is a static version of a GPO for use as a starting point for creating new GPOs.</span></span> <span data-ttu-id="73dfe-383">Несмотря на то, что вы не можете изменять шаблон, вы можете создать новый объект групповой политики на основе шаблона.</span><span class="sxs-lookup"><span data-stu-id="73dfe-383">Although you cannot edit a template, you can create a new GPO based on a template.</span></span> <span data-ttu-id="73dfe-384">Шаблоны полезны для быстрого создания нескольких GPO, включающих в себя множество одинаковых параметров политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-384">Templates are useful for quickly creating multiple GPOs that include many of the same policy settings.</span></span>

**<span data-ttu-id="73dfe-385">Создание шаблона на основе существующего объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-385">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="73dfe-386">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которой назначена роль редактора в РАСШИРЕНном наборе данных.</span><span class="sxs-lookup"><span data-stu-id="73dfe-386">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="73dfe-387">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-387">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="73dfe-388">На вкладке **содержание** в области сведений откройте вкладку **Управление** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-388">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="73dfe-389">Щелкните правой кнопкой мыши **MyGPO**и выберите команду **Сохранить как шаблон** , чтобы создать шаблон, включающий все параметры, в настоящее время находящиеся в MyGPO.</span><span class="sxs-lookup"><span data-stu-id="73dfe-389">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="73dfe-390">Введите **MyTemplate** в качестве имени шаблона и примечания, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-390">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="73dfe-391">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-391">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="73dfe-392">Новый шаблон появится на вкладке **шаблоны** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-392">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="73dfe-393">Запрос создания нового объекта групповой политики с помощью расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="73dfe-393">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="73dfe-394">Откройте вкладку **Управление** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-394">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="73dfe-395">Щелкните правой кнопкой мыши узел **контроль изменений** и выберите команду **создать управляемый объект групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-395">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="73dfe-396">В диалоговом окне **новый управляемый объект групповой политики** :</span><span class="sxs-lookup"><span data-stu-id="73dfe-396">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="73dfe-397">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-397">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="73dfe-398">Введите **MyOtherGPO** в качестве имени нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-398">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="73dfe-399">Введите Примечание для нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-399">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="73dfe-400">Нажмите кнопку **создать в реальном времени** , чтобы новый объект групповой политики развернут в рабочей среде сразу после утверждения.</span><span class="sxs-lookup"><span data-stu-id="73dfe-400">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="73dfe-401">**В шаблоне из GPO**выберите **MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-401">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="73dfe-402">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-402">Click **Submit**.</span></span>

4.  <span data-ttu-id="73dfe-403">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="73dfe-404">Новый объект групповой политики появится на вкладке **ожидающие** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-404">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="73dfe-405">Используйте учетную запись, которой назначена роль утверждающего, чтобы утвердить ожидающий запрос на создание объекта групповой политики, как на [этапе 1: Создайте объект групповой политики](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="73dfe-405">Use an account that is assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="73dfe-406">MyTemplate включает все параметры, настроенные в MyGPO.</span><span class="sxs-lookup"><span data-stu-id="73dfe-406">MyTemplate incorporates all the settings that you configured in MyGPO.</span></span> <span data-ttu-id="73dfe-407">Поскольку MyOtherGPO был создан с помощью MyTemplate, он сначала содержит все параметры, MyGPO содержащиеся на момент создания MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="73dfe-407">Because MyOtherGPO was created using MyTemplate, it at first contains all the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="73dfe-408">Чтобы подтвердить это, вы можете создать отчет о разнице, чтобы сравнить MyOtherGPO с MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="73dfe-408">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="73dfe-409">Извлечение GPO из архива для редактирования</span><span class="sxs-lookup"><span data-stu-id="73dfe-409">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="73dfe-410">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему с помощью учетной записи пользователя, которой назначена роль редактора в РАСШИРЕНном наборе данных.</span><span class="sxs-lookup"><span data-stu-id="73dfe-410">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="73dfe-411">Щелкните правой кнопкой мыши **MyOtherGPO**и выберите пункт **извлечь.**</span><span class="sxs-lookup"><span data-stu-id="73dfe-411">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="73dfe-412">Введите Примечание, которое будет отображаться в истории объекта групповой политики, когда он извлечен, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-412">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="73dfe-413">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-413">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="73dfe-414">На вкладке **Управление** состоянием GPO считается **извлеченным**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-414">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="73dfe-415">Изменение GPO в автономном режиме и Настройка длительности блокировки учетной записи</span><span class="sxs-lookup"><span data-stu-id="73dfe-415">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="73dfe-416">На вкладке **управляемые** щелкните правой кнопкой мыши **MyOtherGPO**и выберите команду **изменить** , чтобы открыть окно **редактора управления групповыми политиками** и изменить автономную копию объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-416">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="73dfe-417">Для этого сценария настройте минимальную длину пароля:</span><span class="sxs-lookup"><span data-stu-id="73dfe-417">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="73dfe-418">В разделе **Конфигурация компьютера**дважды щелкните **политики**, **Параметры Windows**, **Параметры безопасности**, **политики учетных записей**и **политики блокировки учетных записей**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-418">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="73dfe-419">В области сведений дважды щелкните **Продолжительность блокировки учетной записи**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-419">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="73dfe-420">В окне "Свойства" установите флажок **задать этот параметр политики**, задайте для параметра продолжительность **30** минут и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-420">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="73dfe-421">Закройте окно **редактора управления групповыми политиками** .</span><span class="sxs-lookup"><span data-stu-id="73dfe-421">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="73dfe-422">Проверьте MyOtherGPO в архиве и запросите развертывание в том виде, в котором вы делали в MyGPO на [этапе 2. Измените объект групповой политики](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="73dfe-422">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="73dfe-423">Вы можете сравнить MyOtherGPO с MyGPO или с MyTemplate с помощью отчетов о различиях.</span><span class="sxs-lookup"><span data-stu-id="73dfe-423">You can compare MyOtherGPO to MyGPO or to MyTemplate by using difference reports.</span></span> <span data-ttu-id="73dfe-424">Любая учетная запись, включающая в себя роль рецензента (Управление групповыми политиками \ [полный доступ \], утверждающая, редактор или рецензент), может создавать отчеты.</span><span class="sxs-lookup"><span data-stu-id="73dfe-424">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="73dfe-425">Сравнение GPO с другим GPO и с шаблоном</span><span class="sxs-lookup"><span data-stu-id="73dfe-425">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="73dfe-426">Чтобы сравнить MyGPO и MyOtherGPO, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="73dfe-426">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="73dfe-427">На вкладке **Управление** нажмите кнопку **MyGPO**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-427">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="73dfe-428">Нажмите клавишу CTRL, а затем — **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-428">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="73dfe-429">Щелкните правой кнопкой мыши **MyOtherGPO**, наведите указатель на пункт **отличия**и выберите пункт **отчет в формате HTML**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-429">Right-click **MyOtherGPO**, point to **Differences**, and then click **HTML Report**.</span></span>

2.  <span data-ttu-id="73dfe-430">Чтобы сравнить MyOtherGPO и MyTemplate, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="73dfe-430">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="73dfe-431">На вкладке **Управление** нажмите кнопку **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-431">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="73dfe-432">Щелкните правой кнопкой мыши **MyOtherGPO**, наведите указатель на пункт **отличия**и выберите пункт **шаблон**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-432">Right-click **MyOtherGPO**, point to **Differences**, and then click **Template**.</span></span>

    3.  <span data-ttu-id="73dfe-433">Выберите **MyTemplate** и **HTML-отчет**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-433">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="73dfe-434">Шаг 5: удаление и восстановление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-434">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="73dfe-435">На этом этапе вы действуете как утверждающий для удаления GPO.</span><span class="sxs-lookup"><span data-stu-id="73dfe-435">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="73dfe-436">Удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-436">To delete a GPO</span></span>**

1.  <span data-ttu-id="73dfe-437">На компьютере с установленным клиентским управлением групповыми политиками Войдите в систему под учетной записью пользователя, которому назначена роль утверждающего.</span><span class="sxs-lookup"><span data-stu-id="73dfe-437">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver.</span></span>

2.  <span data-ttu-id="73dfe-438">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-438">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="73dfe-439">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-439">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="73dfe-440">Щелкните правой кнопкой мыши **MyGPO**и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-440">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="73dfe-441">Выберите команду **удалить объект групповой политики из архива и производства** , чтобы удалить версию в архиве и развернутую версию объекта групповой политики в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="73dfe-441">Click **Delete GPO from archive and production** to delete both the version in the archive and the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="73dfe-442">Введите Примечание, которое будет отображаться в контрольной записи для объекта групповой политики, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-442">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="73dfe-443">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-443">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="73dfe-444">Объект групповой политики удаляется с вкладки " **управляемые** " и отображается на вкладке " **Корзина** ", в которой ее можно восстановить или уничтожить.</span><span class="sxs-lookup"><span data-stu-id="73dfe-444">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="73dfe-445">Иногда, когда вы удаляете объект групповой политики, он может потребоваться.</span><span class="sxs-lookup"><span data-stu-id="73dfe-445">Occasionally you may discover after you delete a GPO that it is still needed.</span></span> <span data-ttu-id="73dfe-446">На этом этапе вы действуете как утверждающее, чтобы восстановить удаленный объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-446">In this step, you act as an Approver to restore a GPO that was deleted.</span></span>

**<span data-ttu-id="73dfe-447">Восстановление удаленного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-447">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="73dfe-448">На вкладке " **содержимое** " щелкните вкладку " **Корзина** ", чтобы отобразить удаленные GPO.</span><span class="sxs-lookup"><span data-stu-id="73dfe-448">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="73dfe-449">Щелкните правой кнопкой мыши **MyGPO**и выберите команду **восстановить**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-449">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="73dfe-450">Введите Примечание, которое будет отображаться в журнале объекта групповой политики, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-450">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="73dfe-451">После того как в окне **ход выполнения работы с расширенным** состоянием работы с пределами будут завершены, нажмите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-451">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="73dfe-452">Объект групповой политики удаляется из вкладки " **Корзина** " и отображается на вкладке " **управляемые** ".</span><span class="sxs-lookup"><span data-stu-id="73dfe-452">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="73dfe-453">**Примечание**  Восстановление GPO в архиве не приводит к его повторному развертыванию в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="73dfe-453">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="73dfe-454">Чтобы вернуть GPO в производственную среду, разверните объект групповой политики, как на [шаге 3: Проверка и развертывание объекта групповой политики](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="73dfe-454">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="73dfe-455">После изменения и развертывания объекта групповой политики, возможно, вы обнаружите, что последние изменения в объекте групповой политики приводят к возникновению проблемы.</span><span class="sxs-lookup"><span data-stu-id="73dfe-455">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="73dfe-456">На этом этапе вы выполняете роль утверждающего для отката к более ранней версии объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-456">In this step, you act as an Approver to roll back to an earlier version of the GPO.</span></span> <span data-ttu-id="73dfe-457">Вы можете вернуться к любой версии в истории объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-457">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="73dfe-458">С помощью примечаний и подписей вы можете определить известные хорошие версии и внести определенные изменения.</span><span class="sxs-lookup"><span data-stu-id="73dfe-458">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="73dfe-459">Чтобы вернуться к более ранней версии объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="73dfe-459">To roll back to an earlier version of a GPO</span></span>**

1.  <span data-ttu-id="73dfe-460">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="73dfe-460">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="73dfe-461">Дважды щелкните **MyGPO** , чтобы отобразить историю.</span><span class="sxs-lookup"><span data-stu-id="73dfe-461">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="73dfe-462">Щелкните правой кнопкой мыши версию, которую нужно развернуть, и выберите команду **развернуть**, а затем — **Да**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-462">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="73dfe-463">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-463">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="73dfe-464">В окне **журнала** нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-464">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="73dfe-465">**Примечание**  Чтобы убедиться в том, что версия, которая была повторно установлена, предназначена для проверки, просмотрите отчет о различиях для двух версий.</span><span class="sxs-lookup"><span data-stu-id="73dfe-465">**Note** To verify that the version that was redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="73dfe-466">В окне **журнала** для объекта групповой политики выберите две версии, щелкните их правой кнопкой мыши, наведите указатель на пункт **разница**и выберите **отчет HTML** или **отчет XML**.</span><span class="sxs-lookup"><span data-stu-id="73dfe-466">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





