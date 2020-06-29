---
title: Новые возможности в AGPM 4.0 с пакетом обновления 1 (SP1)
description: Новые возможности в AGPM 4.0 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818152"
---
# <span data-ttu-id="313fb-103">Новые возможности в AGPM 4.0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="313fb-103">What's New in AGPM 4.0 SP1</span></span>


<span data-ttu-id="313fb-104">Этот "новые возможности" содержит описание улучшений и поддерживаемых конфигураций для расширенного управления групповыми политиками Microsoft 4,0 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="313fb-104">This “What’s New” content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="313fb-105">Если существует разница между этим содержимым и другой документацией по РАСШИРЕНным режимом, это содержимое должно считаться полномочным и должно заменять контент, включенный в этот продукт.</span><span class="sxs-lookup"><span data-stu-id="313fb-105">If there is a difference between this content and other AGPM documentation, this content should be considered authoritative and should supersede the content included with this product.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="313fb-106">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="313fb-106">What’s new</span></span>


<span data-ttu-id="313fb-107">Расширенные возможности 4,0 с пакетом обновления 1 (SP1) поддерживают следующее:</span><span class="sxs-lookup"><span data-stu-id="313fb-107">AGPM 4.0 SP1 supports the following enhancements:</span></span>

### <span data-ttu-id="313fb-108">Новые и измененные клиентские расширения</span><span class="sxs-lookup"><span data-stu-id="313fb-108">New and changed client-side extensions</span></span>

<span data-ttu-id="313fb-109">Клиентские расширения групповой политики (CSEs) добавлены или изменены для поддержки новой групповой политики в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="313fb-109">Group Policy client-side extensions (CSEs) have been added or changed for AGPM to support new Group Policies in Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="313fb-110">Эти групповые политики позволяют администраторам групповых политик управлять параметрами групповой политики на основе Windows 8, которые меняются между двумя объектами групповой политики (GPO) или шаблонами.</span><span class="sxs-lookup"><span data-stu-id="313fb-110">These group policies enable Group Policy administrators to manage and track Windows 8-specific Group Policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="313fb-111">Кроме того, можно создавать пользовательские объекты групповой политики, а также настраивать и сохранять их в качестве шаблонов с помощью параметров, определенных для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="313fb-111">You can also create custom GPOs, with Windows 8-specific settings, and configure and save the GPOs as a template.</span></span> <span data-ttu-id="313fb-112">Для просмотра CSEs используйте отчеты "Параметры" и "разница", доступные в клиенте РАСШИРЕНного доступа к 4,0 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="313fb-112">To view your CSEs, use the settings and difference reports that are available in the AGPM 4.0 SP1 client.</span></span>

<span data-ttu-id="313fb-113">Ниже перечислены новые и измененные клиентские расширения групповой политики.</span><span class="sxs-lookup"><span data-stu-id="313fb-113">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="313fb-114">**Централизованная политика доступа.** Позволяет администраторам групповых политик указывать централизованные политики доступа на серверах групповой политики, например на файловых серверах.</span><span class="sxs-lookup"><span data-stu-id="313fb-114">**Central Access Policy:** Enables Group Policy administrators to specify Central Access Policies on Group Policy servers, for example, file servers.</span></span> <span data-ttu-id="313fb-115">Централизованная политика доступа — это политика авторизации, определенная элементом GPO и применяемая к целевым объектам политики для облегчения централизованного доступа к ресурсам и управления ресурсами.</span><span class="sxs-lookup"><span data-stu-id="313fb-115">Central Access Policy is an authorization policy that is specified by a GPO item and applied to policy targets to facilitate centralized access and control of resources.</span></span> <span data-ttu-id="313fb-116">Эти централизованные политики доступа должны быть настроены на клиентском компьютере групповой политики в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="313fb-116">These Central Access Policies must be configured on a Group Policy client computer from within Active Directory.</span></span> <span data-ttu-id="313fb-117">Групповая политика распространяет знания соответствующей централизованной политики доступа на компьютеры, которые должны применять ее.</span><span class="sxs-lookup"><span data-stu-id="313fb-117">A Group Policy distributes the knowledge of an applicable Central Access Policy to the computers that have to enforce it.</span></span>

-   <span data-ttu-id="313fb-118">**Изменения политики разрешения имен:** Позволяет администраторам групповых политик настраивать параметры безопасности DNS и DirectAccess на клиентских компьютерах DNS.</span><span class="sxs-lookup"><span data-stu-id="313fb-118">**Name Resolution Policy changes:** Enables Group Policy administrators to configure settings for DNS security and DirectAccess on DNS client computers.</span></span> <span data-ttu-id="313fb-119">Добавлены новые вкладки для настройки универсальных параметров DNS-сервера и параметров кодировки.</span><span class="sxs-lookup"><span data-stu-id="313fb-119">New tabs for configuring Generic DNS Server settings and Encoding settings have been added.</span></span>

-   <span data-ttu-id="313fb-120">**Изменения предпочтения групповой политики:** Добавлена поддержка настройки и управления параметрами Internet Explorer 10, добавленными в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="313fb-120">**Group Policy Preference changes:** Adds support for the configuration and management of Internet Explorer 10 settings that were added for Windows 8.</span></span>

-   <span data-ttu-id="313fb-121">**Удаленные приложения и подключения к рабочему столу:** Позволяет администраторам групповых политик указывать URL-адрес подключения по умолчанию, который используется для удаленных приложений и подключений к рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="313fb-121">**Remote Application and Desktop Connections:** Lets Group Policy administrators specify the default connection URL that is used for Remote Application and Desktop Connections.</span></span>

-   <span data-ttu-id="313fb-122">**Варианты запуска Windows To Go:** Позволяет администраторам групповых политик настраивать компьютер для Windows To Go, если подключено USB-устройство, содержащее рабочую область Windows to go.</span><span class="sxs-lookup"><span data-stu-id="313fb-122">**Windows To Go Startup Options:** Lets Group Policy administrators configure whether the computer will boot to Windows To Go if a USB device that contains a Windows To Go workspace is connected.</span></span>

-   <span data-ttu-id="313fb-123">**Параметры спящего режима Windows To Go:** Позволяет администраторам групповых политик настроить, может ли компьютер использовать состояние сна спящего режима (S4) при запуске компьютера из рабочего пространства Windows to go.</span><span class="sxs-lookup"><span data-stu-id="313fb-123">**Windows To Go Hibernate Options:** Lets Group Policy administrators configure whether a computer can use the hibernation sleep state (S4) when the computer is started from a Windows To Go workspace.</span></span>

### <span data-ttu-id="313fb-124">Отзывы и наборы исправлений пользователей</span><span class="sxs-lookup"><span data-stu-id="313fb-124">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="313fb-125">РАСШИРЕНное обновление данных 4,0 включает в себя свертку исправлений, устраняющих проблемы, обнаруженные с момента выпуска РАСШИРЕНного обновления для 4,0.</span><span class="sxs-lookup"><span data-stu-id="313fb-125">AGPM 4.0 SP1 includes a rollup of fixes to address issues found since the AGPM 4.0 release.</span></span> <span data-ttu-id="313fb-126">Расширенный поиск с пакетом обновления 1 (SP1) содержит последние исправления до и включенных исправлений 1 для управления групповыми политиками (Майкрософт) 4,0.4,0</span><span class="sxs-lookup"><span data-stu-id="313fb-126">AGPM 4.0 SP1 contains the latest fixes up to and including Microsoft Advanced Group Policy Management 4.0 Hotfix 1.</span></span>

### <span data-ttu-id="313fb-127">Отчеты о параметрах и различиях. Просмотр новых расширений групповой политики</span><span class="sxs-lookup"><span data-stu-id="313fb-127">Settings and difference reports show new Group Policy extensions</span></span>

<span data-ttu-id="313fb-128">Новые расширения групповой политики добавлены в отчеты параметров и различий.</span><span class="sxs-lookup"><span data-stu-id="313fb-128">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="313fb-129">Изменения и поддержка установщика</span><span class="sxs-lookup"><span data-stu-id="313fb-129">Installer changes and support</span></span>

<span data-ttu-id="313fb-130">Изменения и поддержка установщика РАСШИРЕНного обновления для 4,0 SP1 описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="313fb-130">The changes and support for the AGPM 4.0 SP1 installer are:</span></span>

-   <span data-ttu-id="313fb-131">Если вы установили РАСШИРЕНную версию для 4,0 SP1 в Windows 8 или Windows Server 2012, установщик расширенного управления групповыми политиками проверяет, установлен ли необходимый программный обеспеченный компонент (консоль "Управление групповой политикой" и платформа .NET 3,5 Framework).</span><span class="sxs-lookup"><span data-stu-id="313fb-131">If you install AGPM 4.0 SP1 on Windows 8 or Windows Server 2012, the AGPM installer verifies that the required prerequisite software (Group Policy Management Console and the .NET 3.5 Framework) is installed.</span></span> <span data-ttu-id="313fb-132">Если эти компоненты не установлены, установка РАСШИРЕНного набора Office 4,0 с пакетом обновления 1 (SP1) заблокирована.</span><span class="sxs-lookup"><span data-stu-id="313fb-132">If these prerequisites are not installed, the AGPM 4.0 SP1 installation is blocked.</span></span>

-   <span data-ttu-id="313fb-133">При установке с 4,0 РАСШИРЕНным управлением пакетом обновления 1 (SP1) Активация WCF, отключение активации по протоколу HTTP и служба активации процессов Windows автоматически включаются.</span><span class="sxs-lookup"><span data-stu-id="313fb-133">When you install AGPM 4.0 SP1, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="313fb-134">В операционных системах Windows Vista, Windows 7 и Windows 8 Загрузите соответствующую версию средства администрирования удаленной системы для своей операционной системы, прежде чем устанавливать их с помощью РАСШИРЕНного набора функций 4,0 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="313fb-134">On Windows Vista, Windows 7, and Windows 8 client operating systems, download the appropriate version of the Remote System Administration Toolkit for your operating system before you install AGPM 4.0 SP1.</span></span>

-   <span data-ttu-id="313fb-135">Поддерживается обратная совместимость с более ранними поддерживаемыми операционными системами.</span><span class="sxs-lookup"><span data-stu-id="313fb-135">Backward compatibility with older supported operating systems is supported.</span></span>

### <span data-ttu-id="313fb-136">Возможность обновления и обновления до РАСШИРЕНного уровня для 4,0 с пакетом обновления 1 (SP1) без повторного ввода параметров конфигурации</span><span class="sxs-lookup"><span data-stu-id="313fb-136">Ability to upgrade or update to AGPM 4.0 SP1 without re-entering configuration parameters</span></span>

<span data-ttu-id="313fb-137">Вы можете обновить клиент (или сервер РАСШИРЕНного ключа) до 4,0 РАСШИРЕНного уровня с пакетом обновления (SP1) только с помощью РАСШИРЕНного обновления для 4,0 без запроса на повторное ввод параметров конфигурации (так называемых интеллектуальных обновлений), как показано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="313fb-137">You can upgrade the AGPM client or server to AGPM 4.0 SP1 only from AGPM 4.0 without being prompted to re-enter configuration parameters (called “Smart Upgrade”), as shown in the following table.</span></span> <span data-ttu-id="313fb-138">Если вы выполняете обновление до версии 4,0 SP1 из других версий РАСШИРЕНного использования, как показано в таблице, необходимо использовать "Классический переход", требующий повторного ввода параметров конфигурации.</span><span class="sxs-lookup"><span data-stu-id="313fb-138">If you are upgrading to AGPM 4.0 SP1 from other versions of AGPM, as shown in the table, you must use the “Classic Upgrade,” which requires you to re-enter the configuration parameters.</span></span> <span data-ttu-id="313fb-139">Так как каждая версия расширенного управления групповыми политиками связана с определенной операционной системой, ознакомьтесь со статьей [Выбор версии для установки с помощью расширенного управления](https://go.microsoft.com/fwlink/?LinkId=254350)правами, а также обязательное обновление операционной системы перед выполнением обновления.</span><span class="sxs-lookup"><span data-stu-id="313fb-139">Since each version of AGPM is associated with a particular operating system, refer to [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350), and be sure to upgrade your operating system as appropriate before performing an upgrade.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="313fb-140">Версия расширенного управления групповыми политиками, из которой можно выполнить обновление</span><span class="sxs-lookup"><span data-stu-id="313fb-140">AGPM Version From Which You Can Upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="313fb-141">2,5</span><span class="sxs-lookup"><span data-stu-id="313fb-141">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="313fb-142">3,0</span><span class="sxs-lookup"><span data-stu-id="313fb-142">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="313fb-143">4,0</span><span class="sxs-lookup"><span data-stu-id="313fb-143">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="313fb-144">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="313fb-144">4.0 SP1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="313fb-145">2,5</span><span class="sxs-lookup"><span data-stu-id="313fb-145">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-146">Не применяется</span><span class="sxs-lookup"><span data-stu-id="313fb-146">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-147">Классический переход</span><span class="sxs-lookup"><span data-stu-id="313fb-147">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-148">Классический переход</span><span class="sxs-lookup"><span data-stu-id="313fb-148">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-149">Установка заблокирована</span><span class="sxs-lookup"><span data-stu-id="313fb-149">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="313fb-150">3,0</span><span class="sxs-lookup"><span data-stu-id="313fb-150">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-151">Не применяется</span><span class="sxs-lookup"><span data-stu-id="313fb-151">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-152">Не применяется</span><span class="sxs-lookup"><span data-stu-id="313fb-152">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-153">Классический переход</span><span class="sxs-lookup"><span data-stu-id="313fb-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-154">Установка заблокирована</span><span class="sxs-lookup"><span data-stu-id="313fb-154">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="313fb-155">4,0</span><span class="sxs-lookup"><span data-stu-id="313fb-155">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-156">Не применяется</span><span class="sxs-lookup"><span data-stu-id="313fb-156">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-157">Не применяется</span><span class="sxs-lookup"><span data-stu-id="313fb-157">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-158">Не применяется</span><span class="sxs-lookup"><span data-stu-id="313fb-158">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-159">Интеллектуальное обновление</span><span class="sxs-lookup"><span data-stu-id="313fb-159">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="313fb-160">Поддерживаемые конфигурации</span><span class="sxs-lookup"><span data-stu-id="313fb-160">Supported configurations</span></span>


<span data-ttu-id="313fb-161">Параметры РАСШИРЕНного отслеживания и поддержки поддерживают конфигурации, указанные в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="313fb-161">AGPM supports the configurations in the following table.</span></span> <span data-ttu-id="313fb-162">Несмотря на то что с помощью РАСШИРЕНных конфигураций поддерживается смешанные конфигурации, настоятельно рекомендуется запускать клиент и сервер с РАСШИРЕНным управлением правами в одном семействе операционной системы, например Windows 8 с Windows Server 2012, Windows 7 с Windows Server 2008 R2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="313fb-162">Although AGPM supports mixed configurations, it is strongly recommended that you run the AGPM client and server on the same operating system family, for example, Windows 8 with Windows Server 2012, Windows 7 with Windows Server 2008 R2, and so on.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="313fb-163">Поддерживаемые конфигурации для РАСШИРЕНного 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="313fb-163">Supported Configurations for AGPM 4.0 SP1 Server</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="313fb-164">Поддерживаемые конфигурации для клиента с РАСШИРЕНным управлением конфигурацией (SP1) 4,0</span><span class="sxs-lookup"><span data-stu-id="313fb-164">Supported Configurations for AGPM 4.0 SP1 Client</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="313fb-165">Поддержка РАСШИРЕНных возможностей 4,0 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="313fb-165">AGPM 4.0 SP1 Support</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="313fb-166">Windows 8 или Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="313fb-166">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-167">Windows 8 или Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="313fb-167">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-168">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="313fb-168">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="313fb-169">Windows Server 2008 R2 или Windows 7</span><span class="sxs-lookup"><span data-stu-id="313fb-169">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-170">Windows Server 2008 R2 или Windows 7</span><span class="sxs-lookup"><span data-stu-id="313fb-170">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-171">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8</span><span class="sxs-lookup"><span data-stu-id="313fb-171">Supported, but cannot edit policy settings or preference items that exist only in Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="313fb-172">Windows Server 2008 R2 или Windows 7 или Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="313fb-172">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-173">Windows Server 2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="313fb-173">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-174">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server 2008 R2 или Windows 7 или Windows 8.</span><span class="sxs-lookup"><span data-stu-id="313fb-174">Supported, but cannot edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="313fb-175">Windows Server 2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="313fb-175">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-176">Windows Server 2008 R2 или Windows 7 или Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="313fb-176">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-177">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="313fb-177">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="313fb-178">Windows Server 2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="313fb-178">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-179">Windows Server 2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="313fb-179">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="313fb-180">Поддерживается, но не может сообщать о параметрах политики или предпочтениях, существующих в Windows Server 2008 R2, Windows 7 или Windows 8, и изменять их.</span><span class="sxs-lookup"><span data-stu-id="313fb-180">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="313fb-181">Предварительные требования для установки РАСШИРЕНного обновления для 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="313fb-181">Prerequisites for installing AGPM 4.0 SP1</span></span>


<span data-ttu-id="313fb-182">В приведенной ниже таблице описаны действия, которые выполняются при использовании установщика .NET 3,5 или консоли управления групповыми политиками в средствах удаленного администрирования сервера (RSAT) для Windows 8 с РАСШИРЕНным управлением пакетом обновления данных 4,0 и сервером.</span><span class="sxs-lookup"><span data-stu-id="313fb-182">The following table describes the behavior on Windows 8 of AGPM 4.0 SP1 client and server installers when .NET 3.5 or the Group Policy Management Console in the Remote Server Administration Tools (RSAT) is missing.</span></span>

**<span data-ttu-id="313fb-183">Клиентская политика расширенного обновления для 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="313fb-183">AGPM Client 4.0 SP1</span></span>**

**<span data-ttu-id="313fb-184">Сервер РАСШИРЕНного обновления для 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="313fb-184">AGPM Server 4.0 SP1</span></span>**

**<span data-ttu-id="313fb-185">Операционная система</span><span class="sxs-lookup"><span data-stu-id="313fb-185">Operating System</span></span>**

**<span data-ttu-id="313fb-186">.NET</span><span class="sxs-lookup"><span data-stu-id="313fb-186">.NET</span></span>**

**<span data-ttu-id="313fb-187">RSAT</span><span class="sxs-lookup"><span data-stu-id="313fb-187">RSAT</span></span>**

**<span data-ttu-id="313fb-188">.NET</span><span class="sxs-lookup"><span data-stu-id="313fb-188">.NET</span></span>**

**<span data-ttu-id="313fb-189">RSAT</span><span class="sxs-lookup"><span data-stu-id="313fb-189">RSAT</span></span>**

**<span data-ttu-id="313fb-190">Windows 8</span><span class="sxs-lookup"><span data-stu-id="313fb-190">Windows 8</span></span>**

<span data-ttu-id="313fb-191">Если платформа .NET 3,5 не включена или не установлена, установщик блокирует установку.</span><span class="sxs-lookup"><span data-stu-id="313fb-191">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="313fb-192">Если консоль GPMC не включена или не установлена в системе, установщик блокирует установку.</span><span class="sxs-lookup"><span data-stu-id="313fb-192">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

<span data-ttu-id="313fb-193">Если платформа .NET 3,5 не включена или не установлена, установщик блокирует установку.</span><span class="sxs-lookup"><span data-stu-id="313fb-193">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="313fb-194">Если консоль GPMC не включена или не установлена в системе, установщик блокирует установку.</span><span class="sxs-lookup"><span data-stu-id="313fb-194">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

**<span data-ttu-id="313fb-195">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="313fb-195">Windows Server 2012</span></span>**

<span data-ttu-id="313fb-196">Если платформа .NET 3,5 не включена или не установлена, установщик блокирует установку.</span><span class="sxs-lookup"><span data-stu-id="313fb-196">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="313fb-197">Если консоль GPMC не включена, установщик включит ее во время установки.</span><span class="sxs-lookup"><span data-stu-id="313fb-197">If GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="313fb-198">Если платформа .NET 3,5 не включена или не установлена, установщик блокирует установку.</span><span class="sxs-lookup"><span data-stu-id="313fb-198">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="313fb-199">Если консоль GPMC не включена, установщик включит ее во время установки.</span><span class="sxs-lookup"><span data-stu-id="313fb-199">If GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="313fb-200">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="313fb-200">Related topics</span></span>


[<span data-ttu-id="313fb-201">Расширенное управление групповыми политиками (AGPM)</span><span class="sxs-lookup"><span data-stu-id="313fb-201">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="313fb-202">Заметки о выпуске для средства расширенного управления групповыми политиками Майкрософт4.0 с пакетом обновления1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="313fb-202">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 





