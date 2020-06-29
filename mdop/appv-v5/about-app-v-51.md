---
title: Сведения об App-V 5.1
description: Сведения об App-V 5.1
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4f2404dcd431b32f5d9a4ae7c49f1e376979e04e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814949"
---
# <span data-ttu-id="a9444-103">Сведения об App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a9444-103">About App-V 5.1</span></span>


<span data-ttu-id="a9444-104">В следующих разделах приведены сведения о значительных изменениях, применимых к Application Virtualization (App-V) 5,1:</span><span class="sxs-lookup"><span data-stu-id="a9444-104">Use the following sections to review information about significant changes that apply to Application Virtualization (App-V) 5.1:</span></span>

[<span data-ttu-id="a9444-105">Требования к программному обеспечению для App-V 5,1 и поддерживаемые конфигурации</span><span class="sxs-lookup"><span data-stu-id="a9444-105">App-V 5.1 software prerequisites and supported configurations</span></span>](#bkmk-51-prereq-configs)

[<span data-ttu-id="a9444-106">Переход на App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-106">Migrating to App-V 5.1</span></span>](#bkmk-migrate-to-51)

[<span data-ttu-id="a9444-107">Новые возможности App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-107">What’s New in App-V 5.1</span></span>](#bkmk-whatsnew)

[<span data-ttu-id="a9444-108">Поддержка App-V для Windows 10</span><span class="sxs-lookup"><span data-stu-id="a9444-108">App-V support for Windows 10</span></span>](#bkmk-win10support)

[<span data-ttu-id="a9444-109">Изменения в консоли управления App-V</span><span class="sxs-lookup"><span data-stu-id="a9444-109">App-V Management Console Changes</span></span>](#bkmk-mgmtconsole)

[<span data-ttu-id="a9444-110">Усовершенствования программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="a9444-110">Sequencer Improvements</span></span>](#bkmk-seqimprove)

[<span data-ttu-id="a9444-111">Улучшенные возможности конвертера пакетов</span><span class="sxs-lookup"><span data-stu-id="a9444-111">Improvements to Package Converter</span></span>](#bkmk-pkgconvimprove)

[<span data-ttu-id="a9444-112">Поддержка нескольких сценариев для одного триггера событий</span><span class="sxs-lookup"><span data-stu-id="a9444-112">Support for multiple scripts on a single event trigger</span></span>](#bkmk-supmultscripts)

[<span data-ttu-id="a9444-113">Жестко закодированный путь к папке установки перенаправляется в корневой каталог виртуальной файловой системы</span><span class="sxs-lookup"><span data-stu-id="a9444-113">Hardcoded path to installation folder is redirected to virtual file system root</span></span>](#bkmk-hardcodepath)

## <a href="" id="bkmk-51-prereq-configs"></a><span data-ttu-id="a9444-114">Требования к программному обеспечению для App-V 5,1 и поддерживаемые конфигурации</span><span class="sxs-lookup"><span data-stu-id="a9444-114">App-V 5.1 software prerequisites and supported configurations</span></span>


<span data-ttu-id="a9444-115">Ниже приведены ссылки на дополнительные требования к программному обеспечению App-V 5,1 и поддерживаемые конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a9444-115">See the following links for the App-V 5.1 software prerequisites and supported configurations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9444-116">Ссылки на предварительные и поддерживаемые конфигурации</span><span class="sxs-lookup"><span data-stu-id="a9444-116">Links to prerequisites and supported configurations</span></span></th>
<th align="left"><span data-ttu-id="a9444-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a9444-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-51-prerequisites.md" data-raw-source="[App-V 5.1 Prerequisites](app-v-51-prerequisites.md)"><span data-ttu-id="a9444-118">Предварительные требования App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a9444-118">App-V 5.1 Prerequisites</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="a9444-119">Необходимое программное обеспечение, которое необходимо установить перед установкой App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-119">Prerequisite software that you must install before starting the App-V 5.1 installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"><span data-ttu-id="a9444-120">Поддерживаемые конфигурации в App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a9444-120">App-V 5.1 Supported Configurations</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="a9444-121">Поддерживаемые операционные системы и требования к оборудованию для серверов App-V, секвенсоров и клиентских компонентов</span><span class="sxs-lookup"><span data-stu-id="a9444-121">Supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client components</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="a9444-122">**Поддержка с помощью Configuration Manager для App-V:** App-V 5,1 поддерживает System Center 2012 R2 Configuration Manager SP1.</span><span class="sxs-lookup"><span data-stu-id="a9444-122">**Support for using Configuration Manager with App-V:** App-V 5.1 supports System Center 2012 R2 Configuration Manager SP1.</span></span> <span data-ttu-id="a9444-123">Сведения о том, как интегрировать среду App-V с Configuration Manager и Configuration Manager, можно найти в разделе [Планирование интеграции App-v с Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a9444-123">See [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) for information about integrating your App-V environment with Configuration Manager and Configuration Manager.</span></span>

## <a href="" id="bkmk-migrate-to-51"></a><span data-ttu-id="a9444-124">Переход на App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-124">Migrating to App-V 5.1</span></span>


<span data-ttu-id="a9444-125">Воспользуйтесь приведенными ниже сведениями, чтобы перейти на версию App-V 5,1 с более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="a9444-125">Use the following information to upgrade to App-V 5.1 from earlier versions.</span></span> <span data-ttu-id="a9444-126">Дополнительные сведения [можно найти в разделе Переход на версию App-V 5,1 из предыдущей версии](migrating-to-app-v-51-from-a-previous-version.md) .</span><span class="sxs-lookup"><span data-stu-id="a9444-126">See [Migrating to App-V 5.1 from a Previous Version](migrating-to-app-v-51-from-a-previous-version.md) for more information.</span></span>

### <span data-ttu-id="a9444-127">Перед началом обновления</span><span class="sxs-lookup"><span data-stu-id="a9444-127">Before you start the upgrade</span></span>

<span data-ttu-id="a9444-128">Прежде чем приступить к обновлению, ознакомьтесь с приведенными ниже сведениями.</span><span class="sxs-lookup"><span data-stu-id="a9444-128">Review the following information before you start the upgrade:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9444-129">Элементы для проверки перед обновлением</span><span class="sxs-lookup"><span data-stu-id="a9444-129">Items to review before upgrading</span></span></th>
<th align="left"><span data-ttu-id="a9444-130">Описание</span><span class="sxs-lookup"><span data-stu-id="a9444-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9444-131">Компоненты для обновления в любом порядке</span><span class="sxs-lookup"><span data-stu-id="a9444-131">Components to upgrade, in any order</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="a9444-132">Сервер App-V</span><span class="sxs-lookup"><span data-stu-id="a9444-132">App-V Server</span></span></p></li>
<li><p><span data-ttu-id="a9444-133">Секвенсор</span><span class="sxs-lookup"><span data-stu-id="a9444-133">Sequencer</span></span></p></li>
<li><p><span data-ttu-id="a9444-134">Клиент App-V или клиент служб удаленных рабочих столов (RDS) для App-V</span><span class="sxs-lookup"><span data-stu-id="a9444-134">App-V Client or App-V Remote Desktop Services (RDS) Client</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="a9444-135">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a9444-135">Note</span></span></strong><br/><p><span data-ttu-id="a9444-136">До версии App-V 5,0 с пакетом обновления 2 (SP2) в клиенте App-V был предоставлен пользовательский интерфейс управления клиентом.</span><span class="sxs-lookup"><span data-stu-id="a9444-136">Prior to App-V 5.0 SP2, the Client Management User Interface (UI) was provided with the App-V Client installation.</span></span> <span data-ttu-id="a9444-137">Для установки пакета обновления 2 (SP2) для App-V 5,0 (или более поздней версии) можно использовать пользовательский интерфейс управления клиентом, загрузив <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> приложение из клиентского интерфейса клиента Application Virtualization 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="a9444-137">For App-V 5.0 SP2 installations (or later), you can use the Client Management UI by downloading from <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)">Application Virtualization 5.0 Client UI Application</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9444-138">Обновление для App-V 4. x</span><span class="sxs-lookup"><span data-stu-id="a9444-138">Upgrading from App-V 4.x</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-139">Сначала необходимо выполнить обновление до версии App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9444-139">You must first upgrade to App-V 5.0.</span></span> <span data-ttu-id="a9444-140">Вы не можете выполнить обновление непосредственно из App-V 4. x в App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a9444-140">You cannot upgrade directly from App-V 4.x to App-V 5.1.</span></span> <span data-ttu-id="a9444-141">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a9444-141">For more information, see:</span></span></p>
<ul>
<li><p><span data-ttu-id="a9444-142">"Различия между App-V 4,6 и App-V 5,0" в <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"> App-v 5,0</span><span class="sxs-lookup"><span data-stu-id="a9444-142">“Differences between App-V 4.6 and App-V 5.0” in <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)">About App-V 5.0</span></span></a></p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)"><span data-ttu-id="a9444-143">Планирование миграции из предыдущей версии App-V</span><span class="sxs-lookup"><span data-stu-id="a9444-143">Planning for Migrating from a Previous Version of App-V</span></span></a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9444-144">Обновление для App-V 5,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a9444-144">Upgrading from App-V 5.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-145">Вы можете выполнить обновление до версии App-V 5,1 прямо из любой из указанных ниже версий.</span><span class="sxs-lookup"><span data-stu-id="a9444-145">You can upgrade to App-V 5.1 directly from any of the following versions:</span></span></p>
<ul>
<li><p><span data-ttu-id="a9444-146">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a9444-146">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="a9444-147">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="a9444-147">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="a9444-148">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="a9444-148">App-V 5.0 SP2</span></span></p></li>
<li><p><span data-ttu-id="a9444-149">App-V 5,0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="a9444-149">App-V 5.0 SP3</span></span></p></li>
</ul>
<p><span data-ttu-id="a9444-150">Чтобы выполнить обновление до версии App-V 5,1, выполните действия, приведенные в остальных разделах этой статьи.</span><span class="sxs-lookup"><span data-stu-id="a9444-150">To upgrade to App-V 5.1, follow the steps in the remaining sections of this topic.</span></span></p>
<p><span data-ttu-id="a9444-151">Пакеты и группы соединений продолжат работать с приложением-V 5,1 в том виде, в каком они в настоящее время работают.</span><span class="sxs-lookup"><span data-stu-id="a9444-151">Packages and connection groups will continue to work with App-V 5.1 as they currently do.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a><span data-ttu-id="a9444-152">Инструкции по обновлению инфраструктуры App-V</span><span class="sxs-lookup"><span data-stu-id="a9444-152">Steps to upgrade the App-V infrastructure</span></span>

<span data-ttu-id="a9444-153">Выполните описанные ниже действия, чтобы обновить каждый компонент инфраструктуры App-V до App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a9444-153">Complete the following steps to upgrade each component of the App-V infrastructure to App-V 5.1.</span></span> <span data-ttu-id="a9444-154">Приведенный ниже порядок является единственным предложением. Вы можете обновить компоненты в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="a9444-154">The following order is only a suggestion; you may upgrade components in any order.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9444-155">Шаг</span><span class="sxs-lookup"><span data-stu-id="a9444-155">Step</span></span></th>
<th align="left"><span data-ttu-id="a9444-156">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="a9444-156">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9444-157">Шаг 1. Обновите сервер App-V.</span><span class="sxs-lookup"><span data-stu-id="a9444-157">Step 1: Upgrade the App-V Server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a9444-158">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a9444-158">Note</span></span></strong><br/><p><span data-ttu-id="a9444-159">Если вы не используете сервер App-V, пропустите этот шаг и перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="a9444-159">If you are not using the App-V Server, skip this step and go to the next step.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="a9444-160">Выполните следующие действия: </span><span class="sxs-lookup"><span data-stu-id="a9444-160">Follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="a9444-161">Выполните одно из указанных ниже действий в зависимости от того, какой метод вы используете для обновления базы данных управления и (или) базы данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="a9444-161">Do one of the following, depending on the method you are using to upgrade the Management database and/or Reporting database:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9444-162">Метод обновления базы данных</span><span class="sxs-lookup"><span data-stu-id="a9444-162">Database upgrade method</span></span></th>
<th align="left"><span data-ttu-id="a9444-163">Шаг</span><span class="sxs-lookup"><span data-stu-id="a9444-163">Step</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9444-164">Установщик Windows</span><span class="sxs-lookup"><span data-stu-id="a9444-164">Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-165">Пропустите этот шаг и перейдите к шагу 2, если вы обновляете сервер App-V...</span><span class="sxs-lookup"><span data-stu-id="a9444-165">Skip this step and go to step 2, “If you are upgrading the App-V Server...”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9444-166">Скрипты SQL</span><span class="sxs-lookup"><span data-stu-id="a9444-166">SQL scripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-167">Выполните действия, описанные в разделе <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> развертывание баз данных App-V с помощью сценариев SQL </a> .</span><span class="sxs-lookup"><span data-stu-id="a9444-167">Follow the steps in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">How to Deploy the App-V Databases by Using SQL Scripts</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<li><p><span data-ttu-id="a9444-168">Если вы обновляете приложение App-V 5,0 с пакетом обновления 1 (SP1) или более поздней версии, выполните действия, описанные в разделе <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)"> Проверка разделов реестра после установки приложения App-v 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="a9444-168">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in section <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)">Check registry keys after installing the App-V 5.0 SP3 Server</a>.</span></span></p></li>
<li><p><span data-ttu-id="a9444-169">Выполните действия, описанные в статье <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> развертывание сервера App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-169">Follow the steps in <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">How to Deploy the App-V 5.1 Server</span></span></a></p></li>
<p> </p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9444-170">Шаг 2. Обновите секвенсор App-V.</span><span class="sxs-lookup"><span data-stu-id="a9444-170">Step 2: Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-171">Узнайте <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> , как установить секвенсор </a> .</span><span class="sxs-lookup"><span data-stu-id="a9444-171">See <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">How to Install the Sequencer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9444-172">Шаг 3. Обновите клиент App-V или клиентское приложение RDS-V.</span><span class="sxs-lookup"><span data-stu-id="a9444-172">Step 3: Upgrade the App-V Client or App-V RDS Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-173">Узнайте <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> , как развернуть клиент App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="a9444-173">See <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a9444-174">Преобразование пакетов, созданных с помощью более ранней версии App-V</span><span class="sxs-lookup"><span data-stu-id="a9444-174">Converting packages created using a prior version of App-V</span></span>

<span data-ttu-id="a9444-175">Используйте служебную программу преобразователя пакетов для обновления пакетов виртуальных приложений, созданных с помощью версий App-V, предшествующих приложению App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9444-175">Use the package converter utility to upgrade virtual application packages created using versions of App-V prior to App-V 5.0.</span></span> <span data-ttu-id="a9444-176">Преобразователь пакетов использует PowerShell для преобразования пакетов и может помочь автоматизировать процесс, если у вас много пакетов, требующих преобразования.</span><span class="sxs-lookup"><span data-stu-id="a9444-176">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

**<span data-ttu-id="a9444-177">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a9444-177">Note</span></span>**  
<span data-ttu-id="a9444-178">Пакеты App-V 5,1 точно так же, как пакеты App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9444-178">App-V 5.1 packages are exactly the same as App-V 5.0 packages.</span></span> <span data-ttu-id="a9444-179">В форматах пакетов между версиями не было изменений, поэтому нет необходимости преобразовывать пакеты 5,0 для App-V в пакеты приложения App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a9444-179">There has been no change in the package format between the versions and so there is no need to convert App-V 5.0 packages to App-V 5.1 packages.</span></span>



## <a href="" id="bkmk-whatsnew"></a><span data-ttu-id="a9444-180">Новые возможности App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-180">What’s New in App-V 5.1</span></span>


<span data-ttu-id="a9444-181">Эти разделы предназначены для пользователей, которые уже знакомы с приложением-V и хотят узнать, что изменилось в App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a9444-181">These sections are for users who are already familiar with App-V and want to know what has changed in App-V 5.1.</span></span> <span data-ttu-id="a9444-182">Если вы еще не знакомы с приложением-V, вы должны ознакомиться с [планированием для App-v 5,1](planning-for-app-v-51.md).</span><span class="sxs-lookup"><span data-stu-id="a9444-182">If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.1](planning-for-app-v-51.md).</span></span>

### <a href="" id="bkmk-win10support"></a><span data-ttu-id="a9444-183">Поддержка App-V для Windows 10</span><span class="sxs-lookup"><span data-stu-id="a9444-183">App-V support for Windows 10</span></span>

<span data-ttu-id="a9444-184">В таблице ниже перечислены сведения о поддержке Windows 10 для App-V.</span><span class="sxs-lookup"><span data-stu-id="a9444-184">The following table lists the Windows 10 support for App-V.</span></span> <span data-ttu-id="a9444-185">Windows 10 не поддерживается в версиях App-V, предшествующих версии приложения 5,1.</span><span class="sxs-lookup"><span data-stu-id="a9444-185">Windows 10 is not supported in versions of App-V prior to App-V 5.1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9444-186">Компонент</span><span class="sxs-lookup"><span data-stu-id="a9444-186">Component</span></span></th>
<th align="left"><span data-ttu-id="a9444-187">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a9444-187">App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="a9444-188">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a9444-188">App-V 5.0</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9444-189">Клиент App-V</span><span class="sxs-lookup"><span data-stu-id="a9444-189">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-190">Да</span><span class="sxs-lookup"><span data-stu-id="a9444-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-191">Нет</span><span class="sxs-lookup"><span data-stu-id="a9444-191">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9444-192">Клиент RDS для App-V</span><span class="sxs-lookup"><span data-stu-id="a9444-192">App-V RDS Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-193">Да</span><span class="sxs-lookup"><span data-stu-id="a9444-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-194">Нет</span><span class="sxs-lookup"><span data-stu-id="a9444-194">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9444-195">Секвенсор App-V</span><span class="sxs-lookup"><span data-stu-id="a9444-195">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-196">Да</span><span class="sxs-lookup"><span data-stu-id="a9444-196">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-197">Нет</span><span class="sxs-lookup"><span data-stu-id="a9444-197">No</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-mgmtconsole"></a><span data-ttu-id="a9444-198">Изменения в консоли управления App-V</span><span class="sxs-lookup"><span data-stu-id="a9444-198">App-V Management Console Changes</span></span>

<span data-ttu-id="a9444-199">В этом разделе сравнивается текущая и Предыдущая функциональность консоли управления App-V.</span><span class="sxs-lookup"><span data-stu-id="a9444-199">This section compares the App-V Management Console’s current and previous functionality.</span></span>

### <span data-ttu-id="a9444-200">Silverlight больше не требуется</span><span class="sxs-lookup"><span data-stu-id="a9444-200">Silverlight is no longer required</span></span>

<span data-ttu-id="a9444-201">Пользовательскому интерфейсу консоли управления больше не требуется Silverlight.</span><span class="sxs-lookup"><span data-stu-id="a9444-201">The Management Console UI no longer requires Silverlight.</span></span> <span data-ttu-id="a9444-202">Консоль управления 5,1 строится на HTML5 и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a9444-202">The 5.1 Management Console is built on HTML5 and Javascript.</span></span>

### <span data-ttu-id="a9444-203">Уведомления и сообщения по отдельности отображаются в диалоговом окне</span><span class="sxs-lookup"><span data-stu-id="a9444-203">Notifications and messages are displayed individually in a dialog box</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9444-204">Новые возможности App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-204">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="a9444-205">До версии App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-205">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a9444-206">Индикатор количества сообщений:</span><span class="sxs-lookup"><span data-stu-id="a9444-206">Number of messages indicator:</span></span></strong></p>
<p><span data-ttu-id="a9444-207">В строке заголовка консоли управления App-V рядом со значком флага появится номер, указывающий количество сообщений, которые ожидают чтения.</span><span class="sxs-lookup"><span data-stu-id="a9444-207">On the title bar of the App-V Management Console, a number is now displayed next to a flag icon to indicate the number of messages that are waiting to be read.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-208">В каждый момент времени вы можете отобразить только одно сообщение или ошибку, и вы не можете определить, сколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="a9444-208">You could see only one message or error at a time, and you were unable to determine how many messages there were.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a9444-209">Внешний вид сообщения:</span><span class="sxs-lookup"><span data-stu-id="a9444-209">Message appearance:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="a9444-210">Сообщения, требующие ввода данных пользователем, отображаются в отдельном диалоговом окне, которое отображается в верхней части текущей страницы, и требует ответа, прежде чем вы сможете их закрыть.</span><span class="sxs-lookup"><span data-stu-id="a9444-210">Messages that require user input appear in a separate dialog box that displays on top of the current page that you were viewing, and require a response before you can dismiss them.</span></span></p></li>
<li><p><span data-ttu-id="a9444-211">Сообщения и ошибки отображаются в списке вместе с одним из них под другим.</span><span class="sxs-lookup"><span data-stu-id="a9444-211">Messages and errors appear in a list, with one beneath the other.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="a9444-212">В каждый момент времени может быть выведено только одно сообщение или ошибка.</span><span class="sxs-lookup"><span data-stu-id="a9444-212">You could see only one message or error at a time.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a9444-213">Сообщения для закрытия:</span><span class="sxs-lookup"><span data-stu-id="a9444-213">Dismissing messages:</span></span></strong></p>
<p><span data-ttu-id="a9444-214">Используйте <strong> ссылку прекратить все </strong> , чтобы закрыть все сообщения и ошибки за один раз, или закрыть их по одному за раз.</span><span class="sxs-lookup"><span data-stu-id="a9444-214">Use the <strong>Dismiss All</strong> link to dismiss all messages and errors at one time, or dismiss them one at a time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-215">Вы можете отклонить сообщения и ошибки только по одному за раз.</span><span class="sxs-lookup"><span data-stu-id="a9444-215">You could dismiss messages and errors only one at a time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a9444-216">Страницы консоли теперь являются отдельными URL-адресами</span><span class="sxs-lookup"><span data-stu-id="a9444-216">Console pages are now separate URLs</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9444-217">Новые возможности App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-217">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="a9444-218">До версии App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-218">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9444-219">Каждая страница консоли имеет другой URL-адрес, который позволяет закладкам для быстрого доступа к определенным страницам в будущем.</span><span class="sxs-lookup"><span data-stu-id="a9444-219">Each page in the console has a different URL, which enables you to bookmark specific pages for quick access in the future.</span></span></p>
<p><span data-ttu-id="a9444-220">Число, которое отображается в некоторых URL-адресах, обозначает конкретный пакет.</span><span class="sxs-lookup"><span data-stu-id="a9444-220">The number that appears in some URLs indicates the specific package.</span></span> <span data-ttu-id="a9444-221">Эти номера уникальны.</span><span class="sxs-lookup"><span data-stu-id="a9444-221">These numbers are unique.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-222">Доступ ко всем страницам консоли осуществляется с помощью одного и того же URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="a9444-222">All console pages are accessed through the same URL.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a9444-223">Страница "создать", отдельная группа "подключения" и пункт меню</span><span class="sxs-lookup"><span data-stu-id="a9444-223">New, separate CONNECTION GROUPS page and menu option</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9444-224">Новые возможности App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-224">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="a9444-225">До версии App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-225">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9444-226">Страница "группы подключения" теперь является частью главного меню на том же уровне, что и страница пакеты.</span><span class="sxs-lookup"><span data-stu-id="a9444-226">The CONNECTION GROUPS page is now part of the main menu, at the same level as the PACKAGES page.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-227">Чтобы открыть страницу "группы подключения", перейдите на страницу "пакеты".</span><span class="sxs-lookup"><span data-stu-id="a9444-227">To open the CONNECTION GROUPS page, you navigate through the PACKAGES page.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a9444-228">Параметры меню для пакетов изменились</span><span class="sxs-lookup"><span data-stu-id="a9444-228">Menu options for packages have changed</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9444-229">Новые возможности App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-229">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="a9444-230">До версии App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a9444-230">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9444-231">Ниже перечислены параметры, которые отображаются в нижней части страницы пакеты.</span><span class="sxs-lookup"><span data-stu-id="a9444-231">The following options are now buttons that appear at the bottom of the PACKAGES page:</span></span></p>
<ul>
<li><p><span data-ttu-id="a9444-232">Добавление или обновление</span><span class="sxs-lookup"><span data-stu-id="a9444-232">Add or Upgrade</span></span></p></li>
<li><p><span data-ttu-id="a9444-233">Публикация</span><span class="sxs-lookup"><span data-stu-id="a9444-233">Publish</span></span></p></li>
<li><p><span data-ttu-id="a9444-234">Отмена публикации</span><span class="sxs-lookup"><span data-stu-id="a9444-234">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="a9444-235">Delete</span><span class="sxs-lookup"><span data-stu-id="a9444-235">Delete</span></span></p></li>
</ul>
<p><span data-ttu-id="a9444-236">При щелчке правой кнопкой мыши пакета, который открывается из раскрывающегося меню, по-прежнему будут выводиться следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="a9444-236">The following options will still appear when you right-click a package to open the drop-down context menu:</span></span></p>
<ul>
<li><p><span data-ttu-id="a9444-237">Публикация</span><span class="sxs-lookup"><span data-stu-id="a9444-237">Publish</span></span></p></li>
<li><p><span data-ttu-id="a9444-238">Отмена публикации</span><span class="sxs-lookup"><span data-stu-id="a9444-238">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="a9444-239">Изменение РЕКЛАМного доступа</span><span class="sxs-lookup"><span data-stu-id="a9444-239">Edit AD Access</span></span></p></li>
<li><p><span data-ttu-id="a9444-240">Изменение конфигурации развертывания</span><span class="sxs-lookup"><span data-stu-id="a9444-240">Edit Deployment Config</span></span></p></li>
<li><p><span data-ttu-id="a9444-241">Пересылка конфигурации развертывания из...</span><span class="sxs-lookup"><span data-stu-id="a9444-241">Transfer deployment configuration from…</span></span></p></li>
<li><p><span data-ttu-id="a9444-242">Передача доступа и конфигурации из...</span><span class="sxs-lookup"><span data-stu-id="a9444-242">Transfer access and configuration from…</span></span></p></li>
<li><p><span data-ttu-id="a9444-243">Delete</span><span class="sxs-lookup"><span data-stu-id="a9444-243">Delete</span></span></p></li>
</ul>
<p><span data-ttu-id="a9444-244">Если нажать кнопку <strong> удалить </strong> , чтобы удалить пакет, откроется диалоговое окно с запросом подтверждения удаления пакета.</span><span class="sxs-lookup"><span data-stu-id="a9444-244">When you click <strong>Delete</strong> to remove a package, a dialog box opens and asks you to confirm that you want to delete the package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9444-245"><strong>Функция добавления или обновления </strong> была нажата кнопка в правом верхнем углу страницы пакеты.</span><span class="sxs-lookup"><span data-stu-id="a9444-245">The <strong>Add or Upgrade</strong> option was a button at the top right of the PACKAGES page.</span></span></p>
<p><span data-ttu-id="a9444-246">Параметры "опубликовать", "отменить <strong> </strong> <strong> публикацию" </strong> и "Удалить" <strong> </strong> доступны только в том случае, если вы щелкните правой кнопкой мыши имя пакета в списке пакеты.</span><span class="sxs-lookup"><span data-stu-id="a9444-246">The <strong>Publish</strong>, <strong>Unpublish</strong>, and <strong>Delete</strong> options were available only if you right-clicked a package name in the packages list.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9444-247">На странице сведения о пакете для каждого пакета отображаются следующие операции с пакетами:</span><span class="sxs-lookup"><span data-stu-id="a9444-247">The following package operations are now buttons on the package details page for each package:</span></span></p>
<ul>
<li><p><span data-ttu-id="a9444-248">Пересылка (раскрывающееся меню со следующими параметрами):</span><span class="sxs-lookup"><span data-stu-id="a9444-248">Transfer (drop-down menu with the following options):</span></span></p>
<ul>
<li><p><span data-ttu-id="a9444-249">Пересылка конфигурации развертывания из...</span><span class="sxs-lookup"><span data-stu-id="a9444-249">Transfer deployment configuration from…</span></span></p></li>
<li><p><span data-ttu-id="a9444-250">Передача доступа и конфигурации из...</span><span class="sxs-lookup"><span data-stu-id="a9444-250">Transfer access and configuration from…</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="a9444-251">Изменить (группы подключения и AD Access)</span><span class="sxs-lookup"><span data-stu-id="a9444-251">Edit (connection groups and AD Access)</span></span></p></li>
<li><p><span data-ttu-id="a9444-252">Отмена публикации</span><span class="sxs-lookup"><span data-stu-id="a9444-252">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="a9444-253">Delete</span><span class="sxs-lookup"><span data-stu-id="a9444-253">Delete</span></span></p></li>
<li><p><span data-ttu-id="a9444-254">Изменение конфигурации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a9444-254">Edit Default Configuration</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="a9444-255">Эти параметры пакета были доступны только в том случае, если вы щелкните правой кнопкой мыши имя пакета в списке пакеты.</span><span class="sxs-lookup"><span data-stu-id="a9444-255">These package options were available only if you right-clicked a package name in the packages list.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a9444-256">Значки в левой области имеют новые цвета и текст</span><span class="sxs-lookup"><span data-stu-id="a9444-256">Icons in left pane have new colors and text</span></span>

<span data-ttu-id="a9444-257">Изменились цвета значков в левой области и добавлен текст, чтобы обеспечить соответствие значков другим продуктам Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a9444-257">The colors of the icons in the left pane have been changed, and text added, to make the icons consistent with other Microsoft products.</span></span>

### <span data-ttu-id="a9444-258">Страница обзора удалена</span><span class="sxs-lookup"><span data-stu-id="a9444-258">Overview page has been removed</span></span>

<span data-ttu-id="a9444-259">В левой области консоли управления был удален параметр меню "Обзор" и связанная с ним страница обзора.</span><span class="sxs-lookup"><span data-stu-id="a9444-259">In the left pane of the Management Console, the OVERVIEW menu option and its associated OVERVIEW page have been removed.</span></span>

### <a href="" id="bkmk-seqimprove"></a><span data-ttu-id="a9444-260">Усовершенствования программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="a9444-260">Sequencer Improvements</span></span>

<span data-ttu-id="a9444-261">В редактор пакетов в секвенсоре App-V 5,1 были внесены следующие улучшения.</span><span class="sxs-lookup"><span data-stu-id="a9444-261">The following improvements have been made to the package editor in the App-V 5.1 Sequencer.</span></span>

### <span data-ttu-id="a9444-262">Импорт и экспорт файла манифеста</span><span class="sxs-lookup"><span data-stu-id="a9444-262">Import and export the manifest file</span></span>

<span data-ttu-id="a9444-263">Файл AppxManifest.xml можно импортировать и экспортировать.</span><span class="sxs-lookup"><span data-stu-id="a9444-263">You can import and export the AppxManifest.xml file.</span></span> <span data-ttu-id="a9444-264">Чтобы экспортировать файл манифеста, откройте вкладку **Дополнительно** и в поле файл манифеста выберите пункт **экспорт..**.. Вы можете вносить изменения в файл манифеста, такие как удаление расширений оболочки или изменение сопоставлений типов файлов.</span><span class="sxs-lookup"><span data-stu-id="a9444-264">To export the manifest file, select the **Advanced** tab and in the Manifest File box, click **Export...**. You can make changes to the manifest file, such as removing shell extensions or editing file type associations.</span></span>

<span data-ttu-id="a9444-265">После внесения изменений нажмите кнопку **Импорт...** и выберите измененный файл.</span><span class="sxs-lookup"><span data-stu-id="a9444-265">After you make your changes, click **Import...** and select the file you edited.</span></span> <span data-ttu-id="a9444-266">После успешного импорта файл манифеста будет немедленно обновлен в редакторе пакетов.</span><span class="sxs-lookup"><span data-stu-id="a9444-266">After you successfully import it back in, the manifest file is immediately updated within the package editor.</span></span>

**<span data-ttu-id="a9444-267">Осторожны</span><span class="sxs-lookup"><span data-stu-id="a9444-267">Caution</span></span>**  
<span data-ttu-id="a9444-268">При импорте файла ваши изменения проверяются на соответствие схеме XML.</span><span class="sxs-lookup"><span data-stu-id="a9444-268">When you import the file, your changes are validated against the XML schema.</span></span> <span data-ttu-id="a9444-269">Если файл не является допустимым, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a9444-269">If the file is not valid, you will receive an error.</span></span> <span data-ttu-id="a9444-270">Имейте в виду, что вы можете импортировать файл, проверяемый на соответствие схеме XML, но это может по-прежнему не выполняться по другим причинам.</span><span class="sxs-lookup"><span data-stu-id="a9444-270">Be aware that it is possible to import a file that is validated against the XML schema, but that might still fail to run for other reasons.</span></span>



### <span data-ttu-id="a9444-271">Добавление в список операционных систем Windows 10</span><span class="sxs-lookup"><span data-stu-id="a9444-271">Addition of Windows 10 to operating systems list</span></span>

<span data-ttu-id="a9444-272">На вкладке Развертывание в список операционных систем, для которых вы можете последовательное обновление, добавлены Windows 10 32-bit и Windows 10-64 bit.</span><span class="sxs-lookup"><span data-stu-id="a9444-272">In the Deployment tab, Windows 10 32-bit and Windows 10-64 bit have been added to the list of operating systems for which you can sequence a package.</span></span> <span data-ttu-id="a9444-273">Если вы выбрали **операционную систему**Windows 10, она автоматически включается в операционные системы, которые будут поддерживаться последовательными пакетами.</span><span class="sxs-lookup"><span data-stu-id="a9444-273">If you select **Any Operating System**, Windows 10 is automatically included among the operating systems that the sequenced package will support.</span></span>

### <span data-ttu-id="a9444-274">Текущий путь отображается в нижней части окна "редактор виртуальных разделов реестра"</span><span class="sxs-lookup"><span data-stu-id="a9444-274">Current path displays at bottom of virtual registry editor</span></span>

<span data-ttu-id="a9444-275">На вкладке Виртуальный реестр путь теперь отображается в нижней части окна "редактор виртуальных разделов реестра", который позволяет определить текущий выбранный раздел.</span><span class="sxs-lookup"><span data-stu-id="a9444-275">In the Virtual Registry tab, the path now displays at the bottom of the virtual registry editor, which enables you to determine the currently selected key.</span></span> <span data-ttu-id="a9444-276">Ранее вам пришлось прокручивать структуру реестра для поиска текущего раздела.</span><span class="sxs-lookup"><span data-stu-id="a9444-276">Previously, you had to scroll through the registry tree to find the currently selected key.</span></span>

### <a href="" id="combined--find-and-replace--dialog-box-and-shortcut-keys-added-in-virtual-registry-editor"></a><span data-ttu-id="a9444-277">Комбинированное диалоговое окно "Поиск и замена" и сочетания клавиш, добавленные в виртуальном редакторе реестра</span><span class="sxs-lookup"><span data-stu-id="a9444-277">Combined “find and replace” dialog box and shortcut keys added in virtual registry editor</span></span>

<span data-ttu-id="a9444-278">В редакторе виртуальных реестров добавлены сочетания клавиш для параметра "найти" (Ctrl + F), а также добавлена возможность поиска и замены значений и данных в диалоговом окне, объединяющем задачи "найти" и "заменить".</span><span class="sxs-lookup"><span data-stu-id="a9444-278">In the virtual registry editor, shortcut keys have been added for the Find option (Ctrl+F), and a dialog box that combines the “find” and “replace” tasks has been added to enable you to find and replace values and data.</span></span> <span data-ttu-id="a9444-279">Чтобы открыть это комбинированное диалоговое окно, выберите раздел и выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="a9444-279">To access this combined dialog box, select a key and do one of the following:</span></span>

-   <span data-ttu-id="a9444-280">Нажмите клавиши **CTRL + H**</span><span class="sxs-lookup"><span data-stu-id="a9444-280">Press **Ctrl+H**</span></span>

-   <span data-ttu-id="a9444-281">Щелкните правой кнопкой мыши клавишу и выберите команду **заменить**.</span><span class="sxs-lookup"><span data-stu-id="a9444-281">Right-click a key and select **Replace**.</span></span>

-   <span data-ttu-id="a9444-282">Нажмите кнопку **Просмотреть** &gt; **виртуальный реестр** &gt; **заменить**.</span><span class="sxs-lookup"><span data-stu-id="a9444-282">Select **View** &gt; **Virtual Registry** &gt; **Replace**.</span></span>

<span data-ttu-id="a9444-283">Ранее диалоговое окно "заменить" не существовало и вам пришлось внести изменения вручную.</span><span class="sxs-lookup"><span data-stu-id="a9444-283">Previously, the “Replace” dialog box did not exist, and you had to make changes manually.</span></span>

### <span data-ttu-id="a9444-284">Переименование разделов реестра и файлов пакетов успешно</span><span class="sxs-lookup"><span data-stu-id="a9444-284">Rename registry keys and package files successfully</span></span>

<span data-ttu-id="a9444-285">Вы можете переименовывать разделы реестра и файлы, не выполняя проблем программы Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a9444-285">You can rename virtual registry keys and files without experiencing Sequencer issues.</span></span> <span data-ttu-id="a9444-286">Ранее программа Sequencer перестала работать при попытке переименования ключа.</span><span class="sxs-lookup"><span data-stu-id="a9444-286">Previously, the Sequencer stopped working if you tried to rename a key.</span></span>

### <span data-ttu-id="a9444-287">Импорт и экспорт виртуальных разделов реестра</span><span class="sxs-lookup"><span data-stu-id="a9444-287">Import and export virtual registry keys</span></span>

<span data-ttu-id="a9444-288">Вы можете импортировать и экспортировать виртуальные разделы реестра.</span><span class="sxs-lookup"><span data-stu-id="a9444-288">You can import and export virtual registry keys.</span></span> <span data-ttu-id="a9444-289">Чтобы импортировать раздел, щелкните правой кнопкой мыши узел, в котором нужно импортировать ключ, и выберите команду **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="a9444-289">To import a key, right-click the node under which to import the key, navigate to the key you want to import, and then click **Import**.</span></span> <span data-ttu-id="a9444-290">Чтобы экспортировать раздел, щелкните его правой кнопкой мыши и выберите пункт **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="a9444-290">To export a key, right-click the key and select **Export**.</span></span>

### <span data-ttu-id="a9444-291">Импорт каталога в виртуальную файловую систему</span><span class="sxs-lookup"><span data-stu-id="a9444-291">Import a directory into the virtual file system</span></span>

<span data-ttu-id="a9444-292">Вы можете импортировать каталог в VFS.</span><span class="sxs-lookup"><span data-stu-id="a9444-292">You can import a directory into the VFS.</span></span> <span data-ttu-id="a9444-293">Чтобы импортировать каталог, откройте вкладку **файлы пакета** и выберите пункт **Просмотреть** &gt; Каталог импорта **виртуальной файловой системы** &gt; **Import Directory**.</span><span class="sxs-lookup"><span data-stu-id="a9444-293">To import a directory, click the **Package Files** tab, and then click **View** &gt; **Virtual File System** &gt; **Import Directory**.</span></span> <span data-ttu-id="a9444-294">При попытке импортировать каталог, содержащий файлы, которые уже находятся в VFS, Импорт завершается сбоем, и на экране появляется пояснительное сообщение.</span><span class="sxs-lookup"><span data-stu-id="a9444-294">If you try to import a directory that contains files that are already in the VFS, the import fails, and an explanatory message is displayed.</span></span> <span data-ttu-id="a9444-295">До версии App-V 5,1 нельзя импортировать каталоги.</span><span class="sxs-lookup"><span data-stu-id="a9444-295">Prior to App-V 5.1, you could not import directories.</span></span>

### <span data-ttu-id="a9444-296">Импортируйте или экспортируйте файл VFS, не удаляя его, а затем добавляйте его обратно в пакет.</span><span class="sxs-lookup"><span data-stu-id="a9444-296">Import or export a VFS file without having to delete and then add it back to the package</span></span>

<span data-ttu-id="a9444-297">Вы можете импортировать и экспортировать файлы из VFS, не удаляя их, а затем добавлять их обратно в пакет.</span><span class="sxs-lookup"><span data-stu-id="a9444-297">You can import files to or export files from the VFS without having to delete the file and then add it back to the package.</span></span> <span data-ttu-id="a9444-298">Например, вы можете использовать эту функцию для экспорта журнала изменений на локальный диск, редактирования файла с помощью внешнего редактора и повторного импорта файла в VFS.</span><span class="sxs-lookup"><span data-stu-id="a9444-298">For example, you might use this feature to export a change log to a local drive, edit the file using an external editor, and then re-import the file into the VFS.</span></span>

<span data-ttu-id="a9444-299">Чтобы экспортировать файл, откройте вкладку **файлы пакета** , щелкните правой кнопкой мыши файл в VFS, выберите команду **Экспорт**, а затем — расположение для экспорта, из которого вы сможете вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="a9444-299">To export a file, select the **Package Files** tab, right-click the file in the VFS, click **Export**, and choose an export location from which you can make your edits.</span></span>

<span data-ttu-id="a9444-300">Чтобы импортировать файл, перейдите на вкладку **файлы пакета** и щелкните правой кнопкой мыши файл, который вы экспортировали.</span><span class="sxs-lookup"><span data-stu-id="a9444-300">To import a file, select the **Package Files** tab and right-click the file that you had exported.</span></span> <span data-ttu-id="a9444-301">Перейдите к файлу, который вы редактировали, и нажмите кнопку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="a9444-301">Browse to the file that you edited, and then click **Import**.</span></span> <span data-ttu-id="a9444-302">Импортированный файл переопределит существующий файл.</span><span class="sxs-lookup"><span data-stu-id="a9444-302">The imported file will overwrite the existing file.</span></span>

<span data-ttu-id="a9444-303">После импорта файла необходимо сохранить его, нажав кнопку **File** &gt; **сохранить**файл.</span><span class="sxs-lookup"><span data-stu-id="a9444-303">After you import a file, you must save the package by clicking **File** &gt; **Save**.</span></span>

### <span data-ttu-id="a9444-304">Меню для добавления файла пакета</span><span class="sxs-lookup"><span data-stu-id="a9444-304">Menu for adding a package file has moved</span></span>

<span data-ttu-id="a9444-305">Команда меню для добавления файла пакета была перемещена.</span><span class="sxs-lookup"><span data-stu-id="a9444-305">The menu option for adding a package file has been moved.</span></span> <span data-ttu-id="a9444-306">Чтобы найти параметр Добавить, откройте вкладку **файлы пакета** и выберите команду **Просмотреть** &gt; файл в **файловой системе** " &gt; **Добавление файла**".</span><span class="sxs-lookup"><span data-stu-id="a9444-306">To find the Add option, select the **Package Files** tab, then click **View** &gt; **Virtual File System** &gt; **Add File**.</span></span> <span data-ttu-id="a9444-307">Ранее вы щелкните правой кнопкой мыши папку под узлом VFS и выберите команду **Добавить файл**.</span><span class="sxs-lookup"><span data-stu-id="a9444-307">Previously, you right-clicked a folder under the VFS node, and chose **Add File**.</span></span>

### <span data-ttu-id="a9444-308">Раздел виртуального реестра, по умолчанию развернутый под кустами компьютеров и пользователей</span><span class="sxs-lookup"><span data-stu-id="a9444-308">Virtual registry node expands MACHINE and USER hives by default</span></span>

<span data-ttu-id="a9444-309">Когда вы открываете виртуальный реестр, кусты компьютеров и пользователей отображаются под узлом реестра верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="a9444-309">When you open the virtual registry, the MACHINE and USER hives are shown below the top-level REGISTRY node.</span></span> <span data-ttu-id="a9444-310">Ранее вам пришлось расширить раздел реестра, чтобы отобразить кусты ниже.</span><span class="sxs-lookup"><span data-stu-id="a9444-310">Previously, you had to expand the REGISTRY node to show the hives beneath.</span></span>

### <span data-ttu-id="a9444-311">Включение и отключение вспомогательных объектов браузера</span><span class="sxs-lookup"><span data-stu-id="a9444-311">Enable or disable Browser Helper Objects</span></span>

<span data-ttu-id="a9444-312">Вы можете включить или отключить вспомогательные объекты браузера, установив новый флажок, включить вспомогательные объекты браузера на вкладке Дополнительно пользовательского интерфейса Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a9444-312">You can enable or disable Browser Helper Objects by selecting a new check box, Enable Browser Helper Objects, on the Advanced tab of the Sequencer user interface.</span></span> <span data-ttu-id="a9444-313">Если вспомогательные объекты браузера:</span><span class="sxs-lookup"><span data-stu-id="a9444-313">If Browser Helper Objects:</span></span>

-   <span data-ttu-id="a9444-314">Существуют в пакете и включены, флажок устанавливается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a9444-314">Exist in the package and are enabled, the check box is selected by default.</span></span>

-   <span data-ttu-id="a9444-315">Существуют в пакете и отключены, флажок по умолчанию снят.</span><span class="sxs-lookup"><span data-stu-id="a9444-315">Exist in the package and are disabled, the check box is clear by default.</span></span>

-   <span data-ttu-id="a9444-316">Существует в пакете, где один или несколько активированы и один или несколько отключены, флажок по умолчанию имеет значение "неопределенный".</span><span class="sxs-lookup"><span data-stu-id="a9444-316">Exist in the package, with one or more enabled and one or more disabled, the check box is set to indeterminate by default.</span></span>

-   <span data-ttu-id="a9444-317">Не существуют в пакете, флажок недоступен.</span><span class="sxs-lookup"><span data-stu-id="a9444-317">Do not exist in the package, the check box is disabled.</span></span>

### <a href="" id="bkmk-pkgconvimprove"></a><span data-ttu-id="a9444-318">Улучшенные возможности конвертера пакетов</span><span class="sxs-lookup"><span data-stu-id="a9444-318">Improvements to Package Converter</span></span>

<span data-ttu-id="a9444-319">Теперь можно использовать конвертер пакетов для преобразования пакетов приложений App-V 4,6, содержащих сценарии, а также сведений реестра и сценариев из исходного OSD-файлов, которые теперь включены в выходные данные преобразователя пакетов.</span><span class="sxs-lookup"><span data-stu-id="a9444-319">You can now use the package converter to convert App-V 4.6 packages that contain scripts, and registry information and scripts from source .osd files are now included in package converter output.</span></span>

<span data-ttu-id="a9444-320">Дополнительные сведения, в том числе примеры, приведены [в разделе Переход на App-V 5,1 из предыдущей версии](migrating-to-app-v-51-from-a-previous-version.md).</span><span class="sxs-lookup"><span data-stu-id="a9444-320">For more information including examples, see [Migrating to App-V 5.1 from a Previous Version](migrating-to-app-v-51-from-a-previous-version.md).</span></span>

### <a href="" id="bkmk-supmultscripts"></a><span data-ttu-id="a9444-321">Поддержка нескольких сценариев для одного триггера событий</span><span class="sxs-lookup"><span data-stu-id="a9444-321">Support for multiple scripts on a single event trigger</span></span>

<span data-ttu-id="a9444-322">Приложение App-V 5,1 поддерживает использование нескольких сценариев для одного триггера событий для пакетов App-V, включая пакеты, которые преобразуются из App-V 4,6 в App-V 5,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a9444-322">App-V 5.1 supports the use of multiple scripts on a single event trigger for App-V packages, including packages that you are converting from App-V 4.6 to App-V 5.0 or later.</span></span> <span data-ttu-id="a9444-323">Чтобы включить использование нескольких сценариев, App-V 5,1 использует приложение для запуска сценариев, именуемое ScriptRunner.exe, которое устанавливается как часть установки клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="a9444-323">To enable the use of multiple scripts, App-V 5.1 uses a script launcher application, named ScriptRunner.exe, which is installed as part of the App-V client installation.</span></span>

<span data-ttu-id="a9444-324">Дополнительные сведения, в том числе список триггеров событий и контекст, в котором можно запускать сценарии, приведены в разделе сценарии [о динамической конфигурации App-V 5,1](about-app-v-51-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="a9444-324">For more information, including a list of event triggers and the context under which scripts can be run, see the Scripts section in [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md).</span></span>

### <a href="" id="bkmk-hardcodepath"></a><span data-ttu-id="a9444-325">Жестко закодированный путь к папке установки перенаправляется в корневой каталог виртуальной файловой системы</span><span class="sxs-lookup"><span data-stu-id="a9444-325">Hardcoded path to installation folder is redirected to virtual file system root</span></span>

<span data-ttu-id="a9444-326">При преобразовании пакетов из App-V 4,6 в 5,1 пакет App-V 5,1 может получить доступ к жестко закодированному диску, который требуется использовать при создании пакетов 4,6.</span><span class="sxs-lookup"><span data-stu-id="a9444-326">When you convert packages from App-V 4.6 to 5.1, the App-V 5.1 package can access the hardcoded drive that you were required to use when you created 4.6 packages.</span></span> <span data-ttu-id="a9444-327">Буква диска — это диск, выбранный в качестве установочного диска на компьютере с установленной последовательностью 4,6.</span><span class="sxs-lookup"><span data-stu-id="a9444-327">The drive letter will be the drive you selected as the installation drive on the 4.6 sequencing machine.</span></span> <span data-ttu-id="a9444-328">(Буква диска по умолчанию — Q:\\.).</span><span class="sxs-lookup"><span data-stu-id="a9444-328">(The default drive letter is Q:\\.)</span></span>

<span data-ttu-id="a9444-329">Ранее корневая папка 4,6 не была распознана и недоступна для пакетов App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9444-329">Previously, the 4.6 root folder was not recognized and could not be accessed by App-V 5.0 packages.</span></span> <span data-ttu-id="a9444-330">Пакеты App-V 5,1 могут получать доступ к жестким файлам по их полным путям или могут программно перечислять файлы в корневом каталоге установки App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="a9444-330">App-V 5.1 packages can access hardcoded files by their full path or can programmatically enumerate files under the App-V 4.6 installation root.</span></span>

<span data-ttu-id="a9444-331">**Технические сведения.** Преобразователь пакета App-V 5,1 сохранит корневую папку установки App-V 4,6 и короткие имена папок в FilesystemMetadata.xmlном файле в элементе FileSystem.</span><span class="sxs-lookup"><span data-stu-id="a9444-331">**Technical Details:** The App-V 5.1 package converter will save the App-V 4.6 installation root folder and short folder names in the FilesystemMetadata.xml file in the Filesystem element.</span></span> <span data-ttu-id="a9444-332">Когда клиент App-V 5,1 создает виртуальный процесс, он будет сопоставлять запросы из корневой папки установки app-4,6 V с корнем виртуальной файловой системы.</span><span class="sxs-lookup"><span data-stu-id="a9444-332">When the App-V 5.1 client creates the virtual process, it will map requests from the App-V 4.6 installation root to the virtual file system root.</span></span>

## <span data-ttu-id="a9444-333">Получение технологий для MDOP</span><span class="sxs-lookup"><span data-stu-id="a9444-333">How to Get MDOP Technologies</span></span>


<span data-ttu-id="a9444-334">App-V входит в состав пакета оптимизации рабочего стола Майкрософт (MDOP).</span><span class="sxs-lookup"><span data-stu-id="a9444-334">App-V is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="a9444-335">MDOP входит в состав Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="a9444-335">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="a9444-336">Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в [статьях получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="a9444-336">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="a9444-337">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a9444-337">Related topics</span></span>


[<span data-ttu-id="a9444-338">Заметки о выпуске App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a9444-338">Release Notes for App-V 5.1</span></span>](release-notes-for-app-v-51.md)









