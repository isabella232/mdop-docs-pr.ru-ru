---
title: Новые возможности в AGPM 4.0 с пакетом обновления 2 (SP2)
description: Новые возможности в AGPM 4.0 с пакетом обновления 2 (SP2)
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818149"
---
# <span data-ttu-id="ea9ce-103">Новые возможности в AGPM 4.0 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ea9ce-103">What's New in AGPM 4.0 SP2</span></span>


<span data-ttu-id="ea9ce-104">В этом разделе описаны усовершенствования и поддерживаемые конфигурации расширенного управления групповыми политиками (Pack2) 4.0 Service Management (SP2).</span><span class="sxs-lookup"><span data-stu-id="ea9ce-104">This content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="ea9ce-105">Если существует разница между этим содержимым и другой документацией по РАСШИРЕНным анализом, рассматривайте это содержимое как удостоверяющее и представим, что оно заменяет другую документацию.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-105">If there is a difference between this content and other AGPM documentation, consider this content authoritative and assume that it supersedes the other documentation.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="ea9ce-106">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="ea9ce-106">What’s new</span></span>


<span data-ttu-id="ea9ce-107">В РАСШИРЕНном наборе функций, версия 4.0 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ea9ce-107">AGPM4.0 SP2 supports the following features and functionality.</span></span>

### <span data-ttu-id="ea9ce-108">Поддержка Windows 8.1 и Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="ea9ce-108">Support for Windows8.1 and Windows Server2012 R2</span></span>

<span data-ttu-id="ea9ce-109">С помощью РАСШИРЕНного пакета обновления для Windows 8.1 и Windows Server2012 R2 добавляется поддержка операционных систем.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-109">AGPM4.0 SP2 adds support for the Windows8.1 and Windows Server2012 R2 operating systems.</span></span>

### <span data-ttu-id="ea9ce-110">Новые и измененные клиентские расширения</span><span class="sxs-lookup"><span data-stu-id="ea9ce-110">New and changed client-side extensions</span></span>

<span data-ttu-id="ea9ce-111">Клиентские расширения групповой политики добавлены или изменены для РАСШИРЕНного изменения параметров политики в Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-111">Group Policy client-side extensions have been added or changed for AGPM to support new policy settings in Windows8.1.</span></span> <span data-ttu-id="ea9ce-112">Эти параметры политики позволяют администраторам групповых политик управлять и отслеживать конкретные параметры политики, которые меняются между двумя объектами групповой политики (GPO) или шаблонами.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-112">These policy settings enable Group Policy administrators to manage and track Windows8.1–specific policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="ea9ce-113">Чтобы просмотреть клиентские расширения, используйте отчеты параметров и различий, доступные в клиенте РАСШИРЕНного доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-113">To view your client-side extensions, use the settings and difference reports that are available in the AGPM Client.</span></span>

<span data-ttu-id="ea9ce-114">Ниже перечислены новые и измененные клиентские расширения групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-114">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="ea9ce-115">**Укажите параметры рабочих папок**.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-115">**Specify Work Folders settings**.</span></span> <span data-ttu-id="ea9ce-116">Если вы включите этот параметр политики, ИТ администраторы смогут настроить автоматическое создание рабочих папок.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-116">If you enable this policy setting, IT administrators can configure Work Folders to be created automatically.</span></span> <span data-ttu-id="ea9ce-117">Функция рабочих папок позволяет конечным пользователям синхронизировать файлы с настольными устройствами Windows с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-117">The Work Folders feature enables end users to synchronize files from their Windows desktop devices to their other devices.</span></span> <span data-ttu-id="ea9ce-118">Используйте этот параметр политики для создания отношения синхронизации на устройствах конечного пользователя и для настройки того, как определить файловый сервер, хранящий рабочие папки пользователя.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-118">Use this policy setting to create the synchronization relationship on an end user’s devices and to configure how to identify the file server that stores the user’s Work Folders.</span></span> <span data-ttu-id="ea9ce-119">Если вы выберете флажок **Синхронизация автоматической подготовки** , связь синхронизации будет создана без ввода пользователя, и данные будут автоматически запускаться для синхронизации с устройством пользователя.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-119">If you select the **Auto provision synchronization** check box, the synchronization partnership will be created without user input, and data will automatically start synchronizing to the user’s device.</span></span> <span data-ttu-id="ea9ce-120">Если флажок **Синхронизация автоматической подготовки** не установлен, пользователи должны вводить входные данные, чтобы начать синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-120">If you do not select the **Auto provision synchronization** check box, users must provide input to start the synchronization.</span></span>

-   <span data-ttu-id="ea9ce-121">**Принудительная автоматическая настройка для всех пользователей**.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-121">**Force automatic setup for all users**.</span></span> <span data-ttu-id="ea9ce-122">Если вы включите этот параметр политики, ИТ-администраторы смогут определять необходимость автоматического создания партнерства рабочих папок на устройствах конечных пользователей без ввода данных конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-122">If you enable this policy setting, IT administrators can determine whether to create the Work Folders partnership automatically on end-user devices without input from end users.</span></span> <span data-ttu-id="ea9ce-123">Если вы включите этот параметр политики, синхронизация будет настроена в соответствии с настройкой параметра политики " **задать параметры рабочих папок** ".</span><span class="sxs-lookup"><span data-stu-id="ea9ce-123">If you enable this policy setting, the synchronization will be set up according to how you configure the **Specify Work Folders settings** policy setting.</span></span> <span data-ttu-id="ea9ce-124">Если установить параметр **Принудительная автоматическая настройка политики для всех пользователей** в положение **отключено** или **не задано**, то настройка партнерства рабочих папок будет настроена в соответствии с тем, как вы настроили функцию **автоматического наполнения** в параметрах политики " **указать параметры рабочих папок** ".</span><span class="sxs-lookup"><span data-stu-id="ea9ce-124">If you set the **Force automatic setup for all users** policy setting to **Disabled** or **Not configured**, the Work Folders partnership will be configured according to how you set the **Automatic Provisioning** option in the **Specify Work Folders settings** policy setting.</span></span>

<span data-ttu-id="ea9ce-125">Дополнительные сведения о функциях рабочих папок можно найти в разделе [Общие сведения о рабочих папках](https://go.microsoft.com/fwlink/?LinkId=330444).</span><span class="sxs-lookup"><span data-stu-id="ea9ce-125">For more information about the Work Folders feature, see [Work Folders Overview](https://go.microsoft.com/fwlink/?LinkId=330444).</span></span>

### <span data-ttu-id="ea9ce-126">Отзывы и наборы исправлений пользователей</span><span class="sxs-lookup"><span data-stu-id="ea9ce-126">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="ea9ce-127">В пакете обновления для РАСШИРЕНного набора исправлений (SP1) входит накопительное исправление для устранения проблем, обнаруженных с момента выпуска службы РАСШИРЕНного обслуживания (Pack1) версии 4.0 Service.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-127">AGPM4.0 SP2 includes a rollup of hotfixes to address issues found since the AGPM4.0 Service Pack1 (SP1) release.</span></span> <span data-ttu-id="ea9ce-128">Расширенный набор исправлений (SP1) для расширенного управления групповыми политиками (Hotfix1) содержит последние исправления до и включительно.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-128">AGPM4.0 SP2 contains the latest fixes up to and including Microsoft Advanced Group Policy Management4.0 SP1 Hotfix1.</span></span> <span data-ttu-id="ea9ce-129">Дополнительные сведения можно найти в статье базы знаний [2873472](https://go.microsoft.com/fwlink/?LinkId=325400).</span><span class="sxs-lookup"><span data-stu-id="ea9ce-129">For more information, see Knowledge Base article [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)).</span></span>

### <span data-ttu-id="ea9ce-130">Новые расширения групповой политики в отчетах параметров и различий</span><span class="sxs-lookup"><span data-stu-id="ea9ce-130">New Group Policy extensions in settings and difference reports</span></span>

<span data-ttu-id="ea9ce-131">Новые расширения групповой политики добавлены в отчеты параметров и различий.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-131">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="ea9ce-132">Изменения и поддержка установщика</span><span class="sxs-lookup"><span data-stu-id="ea9ce-132">Installer changes and support</span></span>

<span data-ttu-id="ea9ce-133">Ниже приведены изменения и поддержка установщика РАСШИРЕНного обновления для версии 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-133">The changes and support for the AGPM4.0 SP2 installer are:</span></span>

-   <span data-ttu-id="ea9ce-134">Если установить пакет обновления 2 (SP2) для Windows 8 или Windows Server 2012 или более поздней версии, установщик расширенного управления групповыми политиками проверяет, установлено ли необходимое программное обеспечение (GPMC) и Microsoft .NET Framework 3.5.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-134">If you install AGPM4.0 SP2 on the Windows 8 or Windows Server 2012 operating system or later operating systems, the AGPM installer verifies that the required prerequisite software (the Group Policy Management Console (GPMC) and the Microsoft .NET Framework3.5) is installed.</span></span> <span data-ttu-id="ea9ce-135">Если необходимое программное обеспечение не установлено, установка РАСШИРЕНного набора Office 4.0 с пакетом обновления 2 (SP2) заблокирована.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-135">If this prerequisite software is not installed, the AGPM4.0 SP2 installation is blocked.</span></span>

-   <span data-ttu-id="ea9ce-136">При установке сервера РАСШИРЕНного анализа, активация WCF, активация по протоколу не HTTP и служба активации Windows автоматически включаются.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-136">When you install the AGPM Server, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="ea9ce-137">В операционной системе клиента WindowsVista и более поздних версиях операционных систем загрузите соответствующую версию средств администрирования удаленной системы для операционной системы, прежде чем устанавливать пакет управления ГРУППОВыми характеристиками версии 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-137">On the WindowsVista client operating system and later operating systems, download the appropriate version of the Remote System Administration Tools for your operating system before you install AGPM4.0 SP2.</span></span>

-   <span data-ttu-id="ea9ce-138">Функция РАСШИРЕНного обновления для версии 4.0 SP2 поддерживает обратную совместимость с более ранними поддерживаемыми операционными системами</span><span class="sxs-lookup"><span data-stu-id="ea9ce-138">AGPM4.0 SP2 supports backward compatibility with older supported operating systems.</span></span>

### <span data-ttu-id="ea9ce-139">Возможность обновления до РАСШИРЕНного уровня с пакетом обновления 2 (SP2) без повторного ввода параметров конфигурации</span><span class="sxs-lookup"><span data-stu-id="ea9ce-139">Ability to upgrade to AGPM4.0 SP2 without reentering configuration parameters</span></span>

<span data-ttu-id="ea9ce-140">Вы можете обновить клиент или сервер РАСШИРЕНного использования РАСШИРЕНного ключа до РАСШИРЕНного уровня с пакетом обновления для более новой версии 4.0 без запроса на повторное указание параметров конфигурации (так называемое интеллектуальное обновление) только с помощью РАСШИРЕНной версии 4.0, как показано в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-140">You can upgrade the AGPM Client or AGPM Server to AGPM4.0 SP2 without being prompted to reenter configuration parameters (called the Smart Upgrade) only from AGPM4.0 onward, as shown in the following table.</span></span> <span data-ttu-id="ea9ce-141">Если вы выполняете обновление до версии с пакетом обновления 2 (SP2) для других версий, как показано в таблице, необходимо использовать классический процесс обновления, который требует повторного ввода параметров конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-141">If you are upgrading to AGPM4.0 SP2 from other versions of AGPM, as shown in the table, you must use the Classic Upgrade, which requires you to reenter the configuration parameters.</span></span> <span data-ttu-id="ea9ce-142">Так как каждая версия РАСШИРЕНного управления правами связана с определенной операционной системой, Узнайте, как [выбрать версию для установки](https://go.microsoft.com/fwlink/?LinkId=254350) и убедиться, что операционная система была обновлена до обновления расширенного управления правами.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-142">Because each version of AGPM is associated with a particular operating system, see [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350) and make sure that you upgrade your operating system as appropriate before you upgrade AGPM.</span></span>

**<span data-ttu-id="ea9ce-143">Поддерживаемые обновления с расширенным управлением групповыми политиками 4,0</span><span class="sxs-lookup"><span data-stu-id="ea9ce-143">AGPM 4.0 SP2 supported upgrades</span></span>**

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ea9ce-144">Версия расширенного управления групповыми политиками, из которой можно выполнить обновление</span><span class="sxs-lookup"><span data-stu-id="ea9ce-144">AGPM version from which you can upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="ea9ce-145">2,5</span><span class="sxs-lookup"><span data-stu-id="ea9ce-145">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="ea9ce-146">3,0</span><span class="sxs-lookup"><span data-stu-id="ea9ce-146">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="ea9ce-147">4,0</span><span class="sxs-lookup"><span data-stu-id="ea9ce-147">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="ea9ce-148">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ea9ce-148">4.0 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="ea9ce-149">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="ea9ce-149">4.0 SP2</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea9ce-150">2,5</span><span class="sxs-lookup"><span data-stu-id="ea9ce-150">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-151">Не применяются</span><span class="sxs-lookup"><span data-stu-id="ea9ce-151">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-152">Классический переход</span><span class="sxs-lookup"><span data-stu-id="ea9ce-152">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-153">Классический переход</span><span class="sxs-lookup"><span data-stu-id="ea9ce-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-154">Установка заблокирована</span><span class="sxs-lookup"><span data-stu-id="ea9ce-154">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-155">Установка заблокирована</span><span class="sxs-lookup"><span data-stu-id="ea9ce-155">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea9ce-156">3,0</span><span class="sxs-lookup"><span data-stu-id="ea9ce-156">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-157">Не применяются</span><span class="sxs-lookup"><span data-stu-id="ea9ce-157">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-158">Не применяются</span><span class="sxs-lookup"><span data-stu-id="ea9ce-158">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-159">Классический переход</span><span class="sxs-lookup"><span data-stu-id="ea9ce-159">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-160">Установка заблокирована</span><span class="sxs-lookup"><span data-stu-id="ea9ce-160">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-161">Установка заблокирована</span><span class="sxs-lookup"><span data-stu-id="ea9ce-161">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea9ce-162">4,0</span><span class="sxs-lookup"><span data-stu-id="ea9ce-162">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-163">Не применяются</span><span class="sxs-lookup"><span data-stu-id="ea9ce-163">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-164">Не применяются</span><span class="sxs-lookup"><span data-stu-id="ea9ce-164">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-165">Не применяются</span><span class="sxs-lookup"><span data-stu-id="ea9ce-165">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-166">Интеллектуальное обновление</span><span class="sxs-lookup"><span data-stu-id="ea9ce-166">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-167">Интеллектуальное обновление</span><span class="sxs-lookup"><span data-stu-id="ea9ce-167">Smart Upgrade</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea9ce-168">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ea9ce-168">4.0 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-169">Не применяются</span><span class="sxs-lookup"><span data-stu-id="ea9ce-169">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-170">Не применяются</span><span class="sxs-lookup"><span data-stu-id="ea9ce-170">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-171">Не применяются</span><span class="sxs-lookup"><span data-stu-id="ea9ce-171">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-172">Не применяются</span><span class="sxs-lookup"><span data-stu-id="ea9ce-172">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-173">Интеллектуальное обновление</span><span class="sxs-lookup"><span data-stu-id="ea9ce-173">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ea9ce-174">Поддерживаемые конфигурации</span><span class="sxs-lookup"><span data-stu-id="ea9ce-174">Supported configurations</span></span>


<span data-ttu-id="ea9ce-175">Параметры РАСШИРЕНного обновления (SP2) 4.0 поддерживают конфигурации, указанные в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-175">AGPM4.0 SP2 supports the configurations in the following table.</span></span> <span data-ttu-id="ea9ce-176">Несмотря на то что с помощью РАСШИРЕНных конфигураций поддерживается смешанные конфигурации, настоятельно рекомендуется запускать клиент и сервер РАСШИРЕНного доменных типов в той же строке операционной системы (например, Windows 8.1 в Windows Server2012 R2, Windows 8 и Windows Server 2012 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="ea9ce-176">Although AGPM supports mixed configurations, we strongly recommend that you run the AGPM Client and AGPM Server on the same operating system line—for example, Windows8.1 with Windows Server2012 R2, Windows 8 with Windows Server 2012, and so on.</span></span>

**<span data-ttu-id="ea9ce-177">Поддерживаемые операционные системы и параметры политики для РАСШИРЕНного обновления, версия 4.0 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ea9ce-177">AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="ea9ce-178">Поддерживаемые конфигурации для сервера РАСШИРЕНного языка</span><span class="sxs-lookup"><span data-stu-id="ea9ce-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ea9ce-179">Поддерживаемые конфигурации для клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="ea9ce-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ea9ce-180">Поддержка РАСШИРЕНных возможностей</span><span class="sxs-lookup"><span data-stu-id="ea9ce-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea9ce-181">Windows Server2012 R2 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ea9ce-181">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-182">Windows Server2012 R2 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ea9ce-182">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-183">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ea9ce-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea9ce-184">Windows Server2012 R2, Windows Server 2012, Windows 8.1 или Windows 8</span><span class="sxs-lookup"><span data-stu-id="ea9ce-184">Windows Server2012 R2, Windows Server 2012, Windows8.1, or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-185">Windows Server 2012 или Windows 8</span><span class="sxs-lookup"><span data-stu-id="ea9ce-185">Windows Server 2012 or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-186">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ea9ce-186">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea9ce-187">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="ea9ce-187">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-188">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="ea9ce-188">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-189">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1 или Windows 8</span><span class="sxs-lookup"><span data-stu-id="ea9ce-189">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1 or Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea9ce-190">Windows Server 2012, Windows Server2008R2, Windows 8 и Windows7</span><span class="sxs-lookup"><span data-stu-id="ea9ce-190">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-191">Windows Server2008 или WindowsVista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ea9ce-191">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-192">Поддерживается, но не может изменить параметры политики или элементы предпочтений, которые существуют только в Windows Server2012 R2, Windows Server 2012, Windows 8, Windows 8.1 или Windows7</span><span class="sxs-lookup"><span data-stu-id="ea9ce-192">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea9ce-193">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ea9ce-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-194">Windows Server 2012, Windows Server2008R2, Windows 8 и Windows7</span><span class="sxs-lookup"><span data-stu-id="ea9ce-194">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-195">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-195">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea9ce-196">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ea9ce-196">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-197">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ea9ce-197">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea9ce-198">Поддерживается, но не может сообщать или изменять параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows 8, Windows 8.1 или Windows7</span><span class="sxs-lookup"><span data-stu-id="ea9ce-198">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ea9ce-199">Предварительные условия для установки РАСШИРЕНного обновления для NT 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="ea9ce-199">Prerequisites for installing AGPM4.0 SP2</span></span>


<span data-ttu-id="ea9ce-200">В приведенной ниже таблице описаны действия, которые можно найти в клиентской и серверной среде для Windows 8.1 с помощью установщиков с РАСШИРЕНным управлением пакетом обновления 2 (SP2), если платформа .NET Framework 3.5 или GPMC отсутствует в средствах администрирования</span><span class="sxs-lookup"><span data-stu-id="ea9ce-200">The following table describes the behavior of AGPM4.0 SP2 Client and Server installers on Windows8.1 when the .NET Framework3.5 or the GPMC in the Remote Server Administration Tools is missing.</span></span>

**<span data-ttu-id="ea9ce-201">Клиент с расширенными политиками</span><span class="sxs-lookup"><span data-stu-id="ea9ce-201">AGPM Client</span></span>**

**<span data-ttu-id="ea9ce-202">Сервер РАСШИРЕНного нав</span><span class="sxs-lookup"><span data-stu-id="ea9ce-202">AGPM Server</span></span>**

**<span data-ttu-id="ea9ce-203">Операционная система</span><span class="sxs-lookup"><span data-stu-id="ea9ce-203">Operating system</span></span>**

**<span data-ttu-id="ea9ce-204">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="ea9ce-204">.NET Framework</span></span>**

**<span data-ttu-id="ea9ce-205">Средства удаленного администрирования сервера</span><span class="sxs-lookup"><span data-stu-id="ea9ce-205">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="ea9ce-206">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="ea9ce-206">.NET Framework</span></span>**

**<span data-ttu-id="ea9ce-207">Средства удаленного администрирования сервера</span><span class="sxs-lookup"><span data-stu-id="ea9ce-207">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="ea9ce-208">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ea9ce-208">Windows8.1</span></span>**

<span data-ttu-id="ea9ce-209">Если платформа .NET Framework 3.5 не включена или не установлена, установщик блокирует установку.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-209">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="ea9ce-210">Если консоль GPMC не включена или не установлена, установщик блокирует установку.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-210">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="ea9ce-211">Если платформа .NET Framework 3.5 не включена или не установлена, установщик блокирует установку.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-211">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="ea9ce-212">Если консоль GPMC не включена или не установлена, установщик блокирует установку.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-212">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

**<span data-ttu-id="ea9ce-213">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="ea9ce-213">Windows Server2012 R2</span></span>**

<span data-ttu-id="ea9ce-214">Если платформа .NET Framework 3.5 не включена или не установлена, установщик блокирует установку.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-214">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="ea9ce-215">Если консоль GPMC не включена, установщик включит ее во время установки.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-215">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="ea9ce-216">Если платформа .NET Framework 3.5 не включена или не установлена, установщик блокирует установку.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-216">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="ea9ce-217">Если консоль GPMC не включена, установщик включит ее во время установки.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-217">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="ea9ce-218">Получение технологий для MDOP</span><span class="sxs-lookup"><span data-stu-id="ea9ce-218">How to Get MDOP Technologies</span></span>


<span data-ttu-id="ea9ce-219">Компонент РАСШИРЕНной оптимизации для настольных систем (MDOP) 4,0 входит в состав пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-219">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="ea9ce-220">MDOP входит в состав Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="ea9ce-220">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="ea9ce-221">Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в [статьях получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="ea9ce-221">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="ea9ce-222">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ea9ce-222">Related topics</span></span>


[<span data-ttu-id="ea9ce-223">Расширенное управление групповыми политиками (AGPM)</span><span class="sxs-lookup"><span data-stu-id="ea9ce-223">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="ea9ce-224">Заметки о выпуске для средства расширенного управления групповыми политиками Майкрософт4.0 с пакетом обновления2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ea9ce-224">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[<span data-ttu-id="ea9ce-225">Выбор версии AGPM для установки</span><span class="sxs-lookup"><span data-stu-id="ea9ce-225">Choosing Which Version of AGPM to Install</span></span>](choosing-which-version-of-agpm-to-install.md)

 

 





