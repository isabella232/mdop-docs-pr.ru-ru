---
title: Сведения об App-V 5.0 с пакетом обновления 3 (SP3)
description: Сведения об App-V 5.0 с пакетом обновления 3 (SP3)
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814972"
---
# <span data-ttu-id="3c9fc-103">Сведения об App-V 5.0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="3c9fc-103">About App-V 5.0 SP3</span></span>


<span data-ttu-id="3c9fc-104">В следующих разделах приведены сведения о значительных изменениях, которые относятся к Microsoft Application Virtualization (App-V) 5,0 SP3:</span><span class="sxs-lookup"><span data-stu-id="3c9fc-104">Use the following sections to review information about significant changes that apply to Microsoft Application Virtualization (App-V) 5.0 SP3:</span></span>

-   [<span data-ttu-id="3c9fc-105">Требования к программному обеспечению для App-V 5,0 SP3 и поддерживаемые конфигурации</span><span class="sxs-lookup"><span data-stu-id="3c9fc-105">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>](#bkmk-sp3-prereq-configs)

-   [<span data-ttu-id="3c9fc-106">Переход на App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="3c9fc-106">Migrating to App-V 5.0 SP3</span></span>](#bkmk-migrate-to-50sp3)

-   [<span data-ttu-id="3c9fc-107">Для созданного вручную XML-файла группы подключения требуется обновление схемы</span><span class="sxs-lookup"><span data-stu-id="3c9fc-107">Manually created connection group xml file requires update to schema</span></span>](#bkmk-update-schema-cg)

-   [<span data-ttu-id="3c9fc-108">Усовершенствования групп соединений</span><span class="sxs-lookup"><span data-stu-id="3c9fc-108">Improvements to connection groups</span></span>](#bkmk-cg-improvements)

-   [<span data-ttu-id="3c9fc-109">Администраторы могут публиковать и отменять публикацию пакетов для определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="3c9fc-109">Administrators can publish and unpublish packages for a specific user</span></span>](#bkmk-usersid-pub-pkgs-specf-user)

-   [<span data-ttu-id="3c9fc-110">Разрешение только администраторам публиковать и отменять публикацию пакетов</span><span class="sxs-lookup"><span data-stu-id="3c9fc-110">Enable only administrators to publish and unpublish packages</span></span>](#bkmk-admins-only-pub-unpub-pkgs)

-   [<span data-ttu-id="3c9fc-111">Раздел реестра RunVirtual поддерживает пакеты, опубликованные для пользователя</span><span class="sxs-lookup"><span data-stu-id="3c9fc-111">RunVirtual registry key supports packages that are published to the user</span></span>](#bkmk-runvirtual-reg-key)

-   [<span data-ttu-id="3c9fc-112">Новые командлеты PowerShell и Справка по обновляемым командлетам</span><span class="sxs-lookup"><span data-stu-id="3c9fc-112">New PowerShell cmdlets and updateable cmdlet help</span></span>](#bkmk-posh-cmdlets-help)

-   [<span data-ttu-id="3c9fc-113">Основной каталог виртуального приложения (PVAD) является скрытым, но его можно включить</span><span class="sxs-lookup"><span data-stu-id="3c9fc-113">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>](#bkmk-pvad-hidden)

-   [<span data-ttu-id="3c9fc-114">ClientVersion требуется для просмотра метаданных публикации App-V</span><span class="sxs-lookup"><span data-stu-id="3c9fc-114">ClientVersion is required to view App-V publishing metadata</span></span>](#bkmk-pub-metadata-clientversion)

-   [<span data-ttu-id="3c9fc-115">Журналы событий App-V объединены</span><span class="sxs-lookup"><span data-stu-id="3c9fc-115">App-V event logs have been consolidated</span></span>](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a><span data-ttu-id="3c9fc-116">Требования к программному обеспечению для App-V 5,0 SP3 и поддерживаемые конфигурации</span><span class="sxs-lookup"><span data-stu-id="3c9fc-116">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>


<span data-ttu-id="3c9fc-117">Ниже приведены ссылки на дополнительные требования к программному обеспечению App-V 5,0 SP3 и поддерживаемые конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-117">See the following links for the App-V 5.0 SP3 software prerequisites and supported configurations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-118">Ссылки на предварительные и поддерживаемые конфигурации</span><span class="sxs-lookup"><span data-stu-id="3c9fc-118">Links to prerequisites and supported configurations</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-119">Описание</span><span class="sxs-lookup"><span data-stu-id="3c9fc-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)"><span data-ttu-id="3c9fc-120">Необходимые условия для App-V 5.0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="3c9fc-120">App-V 5.0 SP3 Prerequisites</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-121">Необходимое программное обеспечение, которое необходимо установить перед началом установки App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="3c9fc-121">Prerequisite software that you must install before starting the App-V 5.0 SP3 installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"><span data-ttu-id="3c9fc-122">Поддерживаемые конфигурации App-V 5.0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="3c9fc-122">App-V 5.0 SP3 Supported Configurations</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-123">Поддерживаемые операционные системы и требования к оборудованию для серверов App-V, секвенсоров и клиентских компонентов</span><span class="sxs-lookup"><span data-stu-id="3c9fc-123">Supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client components</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a><span data-ttu-id="3c9fc-124">Переход на App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="3c9fc-124">Migrating to App-V 5.0 SP3</span></span>


<span data-ttu-id="3c9fc-125">Воспользуйтесь приведенными ниже сведениями, чтобы перейти на версию App-V 5,0 SP3 из более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-125">Use the following information to upgrade to App-V 5.0 SP3 from earlier versions.</span></span>

### <span data-ttu-id="3c9fc-126">Перед началом обновления</span><span class="sxs-lookup"><span data-stu-id="3c9fc-126">Before you start the upgrade</span></span>

<span data-ttu-id="3c9fc-127">Прежде чем приступить к обновлению, ознакомьтесь с приведенными ниже сведениями.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-127">Review the following information before you start the upgrade:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-128">Элементы для проверки перед обновлением</span><span class="sxs-lookup"><span data-stu-id="3c9fc-128">Items to review before upgrading</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-129">Описание</span><span class="sxs-lookup"><span data-stu-id="3c9fc-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-130">Компоненты для обновления</span><span class="sxs-lookup"><span data-stu-id="3c9fc-130">Components to upgrade</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="3c9fc-131">Сервер App-V</span><span class="sxs-lookup"><span data-stu-id="3c9fc-131">App-V Server</span></span></p></li>
<li><p><span data-ttu-id="3c9fc-132">Секвенсор</span><span class="sxs-lookup"><span data-stu-id="3c9fc-132">Sequencer</span></span></p></li>
<li><p><span data-ttu-id="3c9fc-133">Клиент App-V или клиент служб удаленных рабочих столов (RDS) для App-V</span><span class="sxs-lookup"><span data-stu-id="3c9fc-133">App-V client or App-V Remote Desktop Services (RDS) client</span></span></p></li>
<li><p><span data-ttu-id="3c9fc-134">Группы подключения</span><span class="sxs-lookup"><span data-stu-id="3c9fc-134">Connection groups</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="3c9fc-135">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-135">Note</span></span></strong><br/><p><span data-ttu-id="3c9fc-136">Чтобы использовать пользовательский интерфейс клиента App-V, скачайте текущую версию из <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> приложения пользовательского интерфейса клиента Microsoft Application Virtualization 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-136">To use the App-V client user interface, download the existing version from <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)">Microsoft Application Virtualization 5.0 Client UI Application</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-137">Обновление для App-V 4. x</span><span class="sxs-lookup"><span data-stu-id="3c9fc-137">Upgrading from App-V 4.x</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-138">Сначала необходимо выполнить обновление до версии App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-138">You must first upgrade to App-V 5.0.</span></span> <span data-ttu-id="3c9fc-139">Вы не можете выполнить обновление непосредственно из App-V 4. x в App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-139">You cannot upgrade directly from App-V 4.x to App-V 5.0 SP3.</span></span></p>
<p><span data-ttu-id="3c9fc-140">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="3c9fc-140">For more information, see:</span></span></p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"><span data-ttu-id="3c9fc-141">Сведения о App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3c9fc-141">About App-V 5.0</span></span></a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)"><span data-ttu-id="3c9fc-142">Планирование миграции из предыдущей версии App-V</span><span class="sxs-lookup"><span data-stu-id="3c9fc-142">Planning for Migrating from a Previous Version of App-V</span></span></a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-143">Обновление для App-V 5,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3c9fc-143">Upgrading from App-V 5.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-144">Вы можете выполнить обновление до версии App-V 5,0 SP3 прямо из любой из указанных ниже версий.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-144">You can upgrade to App-V 5.0 SP3 directly from any of the following versions:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c9fc-145">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3c9fc-145">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="3c9fc-146">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="3c9fc-146">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="3c9fc-147">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="3c9fc-147">App-V 5.0 SP2</span></span></p></li>
</ul>
<p><span data-ttu-id="3c9fc-148">Чтобы перейти на версию App-V 5,0 SP3, выполните действия, приведенные в остальных разделах этой статьи.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-148">To upgrade to App-V 5.0 SP3, follow the steps in the remaining sections of this article.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-149">Изменения, необходимые для пакетов и групп подключений после обновления</span><span class="sxs-lookup"><span data-stu-id="3c9fc-149">Required changes to packages and connection groups after upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-150">Нет.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-150">None.</span></span> <span data-ttu-id="3c9fc-151">Пакеты и группы соединений продолжат работать, как в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-151">Packages and connection groups will continue to work as they currently do.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a><span data-ttu-id="3c9fc-152">Инструкции по обновлению инфраструктуры App-V</span><span class="sxs-lookup"><span data-stu-id="3c9fc-152">Steps to upgrade the App-V infrastructure</span></span>

<span data-ttu-id="3c9fc-153">Выполните описанные ниже действия, чтобы обновить каждый компонент инфраструктуры App-V до версии App-v 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-153">Complete the following steps to upgrade each component of the App-V infrastructure to App-V 5.0 SP3.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-154">Шаг</span><span class="sxs-lookup"><span data-stu-id="3c9fc-154">Step</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-155">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3c9fc-155">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-156">Шаг 1. Обновите сервер App-V.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-156">Step 1: Upgrade the App-V Server.</span></span></p>
<p><span data-ttu-id="3c9fc-157">Если вы не используете сервер App-V, пропустите этот шаг и перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-157">If you are not using the App-V Server, skip this step and go to the next step.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3c9fc-158">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-158">Note</span></span></strong><br/><p><span data-ttu-id="3c9fc-159">Клиент App-V 5,0 с пакетом обновления 3 (SP3) совместим с сервером App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-159">The App-V 5.0 SP3 client is compatible with the App-V 5.0 SP1 Server.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3c9fc-160">Выполните следующие действия: </span><span class="sxs-lookup"><span data-stu-id="3c9fc-160">Follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="3c9fc-161">Ознакомьтесь с <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> заметками о выпуске для App-v 5,0 SP3 </a> для устранения проблем, которые могут повлиять на установку сервера App-v.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-161">Review the <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)">Release Notes for App-V 5.0 SP3</a> for issues that may affect the App-V Server installation.</span></span></p></li>
<li><p><span data-ttu-id="3c9fc-162">Выполните одно из указанных ниже действий в зависимости от того, какой метод вы используете для обновления базы данных управления и (или) базы данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-162">Do one of the following, depending on the method you are using to upgrade the Management database and/or Reporting database:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-163">Метод обновления базы данных</span><span class="sxs-lookup"><span data-stu-id="3c9fc-163">Database upgrade method</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-164">Шаг</span><span class="sxs-lookup"><span data-stu-id="3c9fc-164">Step</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-165">Установщик Windows</span><span class="sxs-lookup"><span data-stu-id="3c9fc-165">Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-166">Пропустите этот шаг и перейдите к шагу 3, "Если вы обновляете сервер App-V..."</span><span class="sxs-lookup"><span data-stu-id="3c9fc-166">Skip this step and go to step 3, “If you are upgrading the App-V Server...”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-167">Скрипты SQL</span><span class="sxs-lookup"><span data-stu-id="3c9fc-167">SQL scripts</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3c9fc-168">База данных управления</span><span class="sxs-lookup"><span data-stu-id="3c9fc-168">Management database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-169">Для установки или обновления ознакомьтесь со <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> сценариями SQL, чтобы установить или обновить базу данных сервера управления App-V 5,0 с пакетом обновления 3 (SP3) не удалось </a> .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-169">To install or upgrade, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3c9fc-170">База данных отчетов</span><span class="sxs-lookup"><span data-stu-id="3c9fc-170">Reporting database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-171">Выполните действия, описанные в разделе <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> развертывание баз данных App-V с помощью сценариев SQL </a> .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-171">Follow the steps in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">How to Deploy the App-V Databases by Using SQL Scripts</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p><span data-ttu-id="3c9fc-172">Если вы обновляете приложение App-V 5,0 с пакетом обновления 1 (SP1) или более поздней версии, выполните действия, описанные в разделе <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> Проверка разделов реестра после установки приложения App-v 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-172">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in section <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)">Check registry keys after installing the App-V 5.0 SP3 Server</a>.</span></span></p></li>
<li><p><span data-ttu-id="3c9fc-173">Выполните действия, описанные в статье <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> развертывание сервера App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-173">Follow the steps in <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">How to Deploy the App-V 5.0 Server</a>.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-174">Шаг 2. Обновите секвенсор App-V.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-174">Step 2: Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-175">Узнайте <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> , как установить секвенсор </a> .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-175">See <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">How to Install the Sequencer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-176">Шаг 3. Обновите клиент App-V или клиентское приложение RDS-V.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-176">Step 3: Upgrade the App-V client or App-V RDS client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-177">Узнайте <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> , как развернуть клиент App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-177">See <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a><span data-ttu-id="3c9fc-178">Проверка разделов реестра перед установкой сервера App-V 5,0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="3c9fc-178">Check registry keys before installing the App-V 5.0 SP3 Server</span></span>

<span data-ttu-id="3c9fc-179">Это шаг 3 из предыдущей таблицы.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-179">This is step 3 from the previous table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3c9fc-180">Если это действие является обязательным</span><span class="sxs-lookup"><span data-stu-id="3c9fc-180">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-181">Вы обновляете версию App-V с пакетом обновления 1 (SP1), используя любые последующие пакеты исправлений, которые вы установили с помощью MSP-файла.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-181">You are upgrading from App-V SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3c9fc-182">В каких компонентах требуется выполнить это действие</span><span class="sxs-lookup"><span data-stu-id="3c9fc-182">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-183">Только обновляемые серверные компоненты App-V.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-183">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3c9fc-184">Если вам понадобится это действие</span><span class="sxs-lookup"><span data-stu-id="3c9fc-184">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-185">Перед обновлением сервера App-V до версии App-V 5,0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="3c9fc-185">Before you upgrade the App-V Server to App-V 5.0 SP3</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3c9fc-186">Что вам нужно сделать?</span><span class="sxs-lookup"><span data-stu-id="3c9fc-186">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-187">С помощью сведений, указанных в приведенных ниже таблицах, обновите значение каждого раздела реестра в соответствии <code>HKLM\Software\Microsoft\AppV\Server</code> со значением, которое вы указали при первоначальной установке сервера.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-187">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="3c9fc-188">При выполнении этого шага восстанавливаются значения реестра, которые могут быть удалены при установке пакетов исправлений для App-V SP1.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-188">Completing this step restores registry values that may have been removed when App-V SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="3c9fc-189">Клавиша ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="3c9fc-189">ManagementDatabase key</span></span>**

<span data-ttu-id="3c9fc-190">Если вы устанавливаете базу данных управления, настройте эти разделы реестра в разделе `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-190">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-191">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="3c9fc-191">Key name</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-192">Описание</span><span class="sxs-lookup"><span data-stu-id="3c9fc-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="3c9fc-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-194">Указывает, требуется ли учетной записи Public Access для доступа к нелокальным базам данных управления.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-194">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="3c9fc-195">Если требуется, для параметра value задано значение "1".</span><span class="sxs-lookup"><span data-stu-id="3c9fc-195">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-196">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="3c9fc-196">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-197">Имя базы данных управления.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-197">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="3c9fc-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-199">Учетная запись, используемая для чтения (общедоступной) доступа к базе данных управления.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-199">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="3c9fc-200">Используется, если <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-200">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="3c9fc-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-202">Идентификатор безопасности (SID) учетной записи, используемой для чтения (общедоступного) доступа к базе данных управления.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-202">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="3c9fc-203">Используется, если <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-203">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-204">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="3c9fc-204">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-205">Экземпляр SQL Server для базы данных управления.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-205">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="3c9fc-206">Если значение пусто, используется экземпляр базы данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-206">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="3c9fc-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-208">Учетная запись, используемая для доступа на запись (администратора) к базе данных управления.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-208">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="3c9fc-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-210">Идентификатор безопасности (SID) учетной записи, используемой для доступа записи (администратора) к базе данных управления.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-210">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="3c9fc-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-212">Учетная запись удаленного компьютера сервера управления (домен \ учетная_запись).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-212">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="3c9fc-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-214">Учетная запись администратора установки для сервера управления (домен \ учетная_запись).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-214">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="3c9fc-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-216">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3c9fc-216">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="3c9fc-217">1 </strong> – Служба управления находится на локальном компьютере, то есть MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT пуста.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-217">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="3c9fc-218">0 </strong> - Служба управления находится на другом компьютере, а не на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-218">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="3c9fc-219">Клавиша ManagementService</span><span class="sxs-lookup"><span data-stu-id="3c9fc-219">ManagementService key</span></span>**

<span data-ttu-id="3c9fc-220">Если вы устанавливаете сервер управления, настройте эти разделы реестра в разделе `HKLM\Software\Microsoft\AppV\Server\ManagementService` .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-220">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-221">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="3c9fc-221">Key name</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-222">Описание</span><span class="sxs-lookup"><span data-stu-id="3c9fc-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-223">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="3c9fc-223">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-224">Группа доменных служб Active Directory (AD DS) или учетная запись, которой разрешено управлять App-V (домен \ учетная_запись).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-224">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-225">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="3c9fc-225">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-226">Экземпляр SQL Server, содержащий базу данных управления.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-226">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="3c9fc-227">Если значение пусто, используется экземпляр базы данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-227">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-228">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="3c9fc-228">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-229">Имя удаленного сервера SQL Server с базой данных управления.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-229">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="3c9fc-230">Если значение пусто, используется локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-230">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="3c9fc-231">Клавиша ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="3c9fc-231">ReportingDatabase key</span></span>**

<span data-ttu-id="3c9fc-232">Если вы устанавливаете базу данных отчетов, настройте эти разделы реестра в разделе `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-232">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-233">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="3c9fc-233">Key name</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-234">Описание</span><span class="sxs-lookup"><span data-stu-id="3c9fc-234">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="3c9fc-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-236">Указывает, требуется ли учетной записи Public Access для доступа к нелокальным базам данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-236">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="3c9fc-237">Если требуется, для параметра value задано значение "1".</span><span class="sxs-lookup"><span data-stu-id="3c9fc-237">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-238">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="3c9fc-238">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-239">Имя базы данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-239">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="3c9fc-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-241">Учетная запись, используемая для чтения (общего доступа) к базе данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-241">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="3c9fc-242">Используется, если <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-242">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="3c9fc-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-244">Идентификатор безопасности (SID) учетной записи, используемой для чтения (общедоступного) доступа к базе данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-244">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="3c9fc-245">Используется, если <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-245">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-246">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="3c9fc-246">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-247">Экземпляр SQL Server для базы данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-247">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="3c9fc-248">Если значение пусто, используется экземпляр базы данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-248">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="3c9fc-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="3c9fc-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="3c9fc-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-252">Учетная запись удаленного компьютера сервера отчетов (домен \ учетная_запись).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-252">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="3c9fc-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-254">Учетная запись администратора установки для сервера отчетов (домен \ учетная_запись).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-254">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="3c9fc-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-256">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3c9fc-256">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="3c9fc-257">1 </strong> – Служба отчетов находится на локальном компьютере, то есть REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT пустая.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-257">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="3c9fc-258">0 </strong> - Служба отчетов находится на другом компьютере, а не на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-258">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="3c9fc-259">Клавиша ReportingService</span><span class="sxs-lookup"><span data-stu-id="3c9fc-259">ReportingService key</span></span>**

<span data-ttu-id="3c9fc-260">Если вы устанавливаете сервер отчетов, настройте эти разделы реестра в разделе `HKLM\Software\Microsoft\AppV\Server\ReportingService` .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-260">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-261">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="3c9fc-261">Key name</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-262">Описание</span><span class="sxs-lookup"><span data-stu-id="3c9fc-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-263">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="3c9fc-263">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-264">Экземпляр SQL Server для базы данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-264">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="3c9fc-265">Если значение пусто, используется экземпляр базы данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-265">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-266">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="3c9fc-266">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-267">Имя удаленного сервера SQL Server с базой данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-267">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="3c9fc-268">Если значение пусто, используется локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-268">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-update-schema-cg"></a><span data-ttu-id="3c9fc-269">Для созданного вручную XML-файла группы подключения требуется обновление схемы</span><span class="sxs-lookup"><span data-stu-id="3c9fc-269">Manually created connection group xml file requires update to schema</span></span>


<span data-ttu-id="3c9fc-270">Если вы вручную создаете XML-файл группы подключений и хотите использовать новые возможности, описанные в разделе [улучшения для групп подключения](#bkmk-cg-improvements), в XML-файле, необходимо указать следующую схему:</span><span class="sxs-lookup"><span data-stu-id="3c9fc-270">If you are manually creating the connection group XML file, and want to use the new “optional packages” and “use any version” features that are described in [Improvements to connection groups](#bkmk-cg-improvements), you must specify the following schema in the XML file:</span></span>

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

<span data-ttu-id="3c9fc-271">Примеры и дополнительные сведения можно найти [в разделе о файле группы подключения](about-the-connection-group-file.md).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-271">For examples and more information, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

## <a href="" id="bkmk-cg-improvements"></a><span data-ttu-id="3c9fc-272">Усовершенствования групп соединений</span><span class="sxs-lookup"><span data-stu-id="3c9fc-272">Improvements to connection groups</span></span>


<span data-ttu-id="3c9fc-273">Для упрощения управления группами подключений можно использовать дополнительные пакеты и другие улучшения, добавленные в App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-273">You can manage connection groups more easily by using optional packages and other improvements that have been added in App-V 5.0 SP3.</span></span> <span data-ttu-id="3c9fc-274">В следующей таблице перечислены задачи, которые можно выполнять с помощью новых функций групп подключений, а также ссылки на более подробные сведения о каждой задаче.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-274">The following table summarizes the tasks that you can perform by using the new connection group features, and links to more detailed information about each task.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-275">Задача или компонент</span><span class="sxs-lookup"><span data-stu-id="3c9fc-275">Task/feature</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-276">Описание</span><span class="sxs-lookup"><span data-stu-id="3c9fc-276">Description</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-277">Ссылки на дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3c9fc-277">Links to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-278">Включение дополнительных пакетов в группу подключения</span><span class="sxs-lookup"><span data-stu-id="3c9fc-278">Enable a connection group to include optional packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-279">Включение необязательных пакетов в группу подключения позволяет динамически определять, какие приложения будут включены в виртуальную среду группы подключений, в зависимости от того, для каких пользователей они предназначены.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-279">Including optional packages in a connection group enables you to dynamically determine which applications will be included in the connection group’s virtual environment, based on the applications that users are entitled to.</span></span></p>
<p><span data-ttu-id="3c9fc-280">Управлять количеством групп подключений не требуется, так как вы можете смешивать необязательные и ненужные пакеты в одной группе подключения.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-280">You don’t need to manage as many connection groups because you can mix optional and non-optional packages in the same connection group.</span></span> <span data-ttu-id="3c9fc-281">Смешивание пакетов позволяет разным группам пользователей использовать одну и ту же группу подключений, несмотря на то, что у пользователей может быть только один общий пакет.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-281">Mixing packages allows different groups of users to use the same connection group, even though users might have only one package in common.</span></span></p>
<p><strong><span data-ttu-id="3c9fc-282">Пример </strong> . Вы можете включить пакет для Microsoft Office для всех пользователей, но включить различные дополнительные пакеты, которые содержат различные подключаемые модули Office, для разных подмножества пользователей.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-282">Example</strong>: You can enable a package with Microsoft Office for all users, but enable different optional packages, which contain different Office plug-ins, to different subsets of users.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="3c9fc-283">Использование дополнительных пакетов в группах соединений</span><span class="sxs-lookup"><span data-stu-id="3c9fc-283">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-284">Отмена публикации или удаление необязательного пакета без изменения группы подключения</span><span class="sxs-lookup"><span data-stu-id="3c9fc-284">Unpublish or delete an optional package without changing the connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-285">Отменять публикацию или удаление, а также отменять публикацию и повторно публиковать необязательный пакет, который находится в группе подключений, не отключая и не возвращающую в клиенте App-V группу подключения.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-285">Unpublish or delete, or unpublish and republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V client.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="3c9fc-286">Использование дополнительных пакетов в группах соединений</span><span class="sxs-lookup"><span data-stu-id="3c9fc-286">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-287">Публикация групп подключений, которые содержат опубликованные пользователями и публикуемые глобально пакеты</span><span class="sxs-lookup"><span data-stu-id="3c9fc-287">Publish connection groups that contain user-published and globally published packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-288">Создайте опубликованную пользователем группу подключений, которая включает опубликованные пользователем и глобально опубликованные пакеты.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-288">Create a user-published connection group that contains user-published and globally published packages.</span></span></p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="3c9fc-289">Создание связывающей группы с опубликованными пользователями и глобально опубликованными пакетами</span><span class="sxs-lookup"><span data-stu-id="3c9fc-289">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-290">Как сделать так, чтобы группа соединений не проигнорировала версию пакета</span><span class="sxs-lookup"><span data-stu-id="3c9fc-290">Make a connection group ignore the package version</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-291">Настройте группу подключений таким образом, чтобы она принимала любую версию пакета, которая позволяет обновить пакет, не отключая группу подключения.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-291">Configure a connection group to accept any version of a package, which enables you to upgrade a package without having to disable the connection group.</span></span> <span data-ttu-id="3c9fc-292">Кроме того, если в группе подключения есть дополнительный пакет с неверной версией, пакет игнорируется и не блокирует создание виртуальной среды группы подключения.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-292">In addition, if there is an optional package with an incorrect version in the connection group, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)"><span data-ttu-id="3c9fc-293">Настройка игнорирования версии пакета группой соединений</span><span class="sxs-lookup"><span data-stu-id="3c9fc-293">How to Make a Connection Group Ignore the Package Version</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-294">Ограничение возможностей публикации конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="3c9fc-294">Limit end users’ publishing capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-295">Разрешите публиковать пакеты и включать группы подключений только для администраторов (не конечных пользователей).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-295">Enable only administrators (not end users) to publish packages and to enable connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-296">Сведения о группах подключений можно найти <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> в разделе разрешение включения групп подключения только администраторам.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-296">For information about connection groups, see <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)">How to Allow Only Administrators to Enable Connection Groups</span></span></a></p>
<p><span data-ttu-id="3c9fc-297">Сведения о пакетах можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="3c9fc-297">For information about packages, see the following articles:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-298">Метод</span><span class="sxs-lookup"><span data-stu-id="3c9fc-298">Method</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-299">Ссылка на дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3c9fc-299">Link to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-300">Консоль управления</span><span class="sxs-lookup"><span data-stu-id="3c9fc-300">Management console</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)"><span data-ttu-id="3c9fc-301">Публикация пакета с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="3c9fc-301">How to Publish a Package by Using the Management Console</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-302">PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c9fc-302">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="3c9fc-303">Управление группами соединений на отдельном компьютере с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c9fc-303">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-304">Почтовая система электронной почты от сторонних разработчиков</span><span class="sxs-lookup"><span data-stu-id="3c9fc-304">Third-party electronic software delivery system</span></span></p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)"><span data-ttu-id="3c9fc-305">Настройка публикации пакетов с помощью ESD только для администраторов</span><span class="sxs-lookup"><span data-stu-id="3c9fc-305">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-306">Включение и отключение группы подключений для определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="3c9fc-306">Enable or disable a connection group for a specific user</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-307">Администраторы могут включать и отключать группу подключений для определенного пользователя с помощью необязательного <strong> </strong> параметра – параметр с указанными ниже командлетами.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-307">Administrators can enable or disable a connection group for a specific user by using the optional <strong>–UserSID</strong> parameter with the following cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c9fc-308">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="3c9fc-308">Enable-AppVClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="3c9fc-309">Disable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="3c9fc-309">Disable-AppVClientConnectionGroup</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)"><span data-ttu-id="3c9fc-310">Управление группами соединений на отдельном компьютере с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c9fc-310">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-311">Слияние одинаковых путей к пакетам в один виртуальный каталог в группах подключений</span><span class="sxs-lookup"><span data-stu-id="3c9fc-311">Merging identical package paths into one virtual directory in connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-312">Если несколько пакетов в группе подключения содержат одинаковые пути к каталогам, они объединяются в один виртуальный каталог в виртуальной среде "Группа подключения".</span><span class="sxs-lookup"><span data-stu-id="3c9fc-312">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span></p>
<p><span data-ttu-id="3c9fc-313">Это объединение путей позволяет приложению в одном пакете получить доступ к файлам в другом пакете.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-313">This merging of paths allows an application in one package to access files that are in a different package.</span></span></p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)"><span data-ttu-id="3c9fc-314">О виртуальной среде связывающей группы</span><span class="sxs-lookup"><span data-stu-id="3c9fc-314">About the Connection Group Virtual Environment</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a><span data-ttu-id="3c9fc-315">Администраторы могут публиковать и отменять публикацию пакетов для определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="3c9fc-315">Administrators can publish and unpublish packages for a specific user</span></span>


<span data-ttu-id="3c9fc-316">Администраторы могут использовать следующие командлеты для публикации и отмены публикации пакетов для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-316">Administrators can use the following cmdlets to publish or unpublish packages for a specific user.</span></span> <span data-ttu-id="3c9fc-317">Чтобы использовать командлеты, введите параметр **–** , а затем идентификатор безопасности пользователя (SID).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-317">To use the cmdlets, enter the **–UserSID** parameter, followed by the user’s security identifier (SID).</span></span> <span data-ttu-id="3c9fc-318">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="3c9fc-318">For more information, see:</span></span>

-   [<span data-ttu-id="3c9fc-319">Управление пакетами App-V 5.0, работающими на автономном компьютере, с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c9fc-319">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="3c9fc-320">Управление пакетами App-V 5.0, работающими на автономном компьютере, с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c9fc-320">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-321">Командлет</span><span class="sxs-lookup"><span data-stu-id="3c9fc-321">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-322">Примеры:</span><span class="sxs-lookup"><span data-stu-id="3c9fc-322">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-323">Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="3c9fc-323">Publish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-324">Publish-AppvClientPackage "ContosoApplication"-в чем заключается S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="3c9fc-324">Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-325">Отмена публикации — AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="3c9fc-325">Unpublish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-326">Отмена публикации-AppvClientPackage "ContosoApplication"-от S до 1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="3c9fc-326">Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a><span data-ttu-id="3c9fc-327">Разрешение только администраторам публиковать и отменять публикацию пакетов</span><span class="sxs-lookup"><span data-stu-id="3c9fc-327">Enable only administrators to publish and unpublish packages</span></span>


<span data-ttu-id="3c9fc-328">Вы можете включить только администраторов (не конечных пользователей) для публикации и отмены публикации пакетов с помощью одного из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-328">You can enable only administrators (not end users) to publish and unpublish packages by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-329">Метод</span><span class="sxs-lookup"><span data-stu-id="3c9fc-329">Method</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-330">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3c9fc-330">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-331">Параметр групповой политики</span><span class="sxs-lookup"><span data-stu-id="3c9fc-331">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-332">Перейдите к следующему узлу объекта групповой политики:</span><span class="sxs-lookup"><span data-stu-id="3c9fc-332">Navigate to the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="3c9fc-333">Политики конфигурации &gt; компьютера &gt; . Административные &gt; шаблоны &gt; Публикация System App-V &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-333">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</strong>.</span></span></p>
<p><span data-ttu-id="3c9fc-334">Включите <strong> параметр требуется опубликовать как </strong> групповую политику администратора.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-334">Enable the <strong>Require publish as administrator</strong> Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-335">PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c9fc-335">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)"><span data-ttu-id="3c9fc-336">Управление пакетами App-V 5.0, работающими на автономном компьютере, с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c9fc-336">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a><span data-ttu-id="3c9fc-337">Раздел реестра RunVirtual поддерживает пакеты, опубликованные для пользователя</span><span class="sxs-lookup"><span data-stu-id="3c9fc-337">RunVirtual registry key supports packages that are published to the user</span></span>


<span data-ttu-id="3c9fc-338">App-V 5,0 SP3 добавляет поддержку использования раздела реестра **RunVirtual** с виртуализированными приложениями, которые находятся в опубликованных пользователем пакетах.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-338">App-V 5.0 SP3 adds support for using the **RunVirtual** registry key with virtualized applications that are in user-published packages.</span></span> <span data-ttu-id="3c9fc-339">Раздел реестра **RunVirtual** позволяет запускать локально установленное приложение в виртуальной среде вместе с приложениями, виртуализованными с помощью App-V.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-339">The **RunVirtual** registry key lets you run a locally installed application in a virtual environment, along with applications that have been virtualized by using App-V.</span></span>

<span data-ttu-id="3c9fc-340">Ранее виртуализированные приложения в пакетах App-V были опубликованы глобально.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-340">Previously, the virtualized applications in App-V packages had to be published globally.</span></span> <span data-ttu-id="3c9fc-341">Дополнительные сведения о **RunVirtual** и других методах выполнения локально установленных приложений в виртуальной среде с виртуализированными приложениями можно найти в разделе [выполнение локально установленного приложения в виртуальной среде с виртуализированными приложениями](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-341">For more about **RunVirtual** and about other methods of running locally installed applications in a virtual environment with virtualized applications, see [Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span></span>

## <a href="" id="bkmk-posh-cmdlets-help"></a><span data-ttu-id="3c9fc-342">Новые командлеты PowerShell и Справка по обновляемым командлетам</span><span class="sxs-lookup"><span data-stu-id="3c9fc-342">New PowerShell cmdlets and updateable cmdlet help</span></span>


<span data-ttu-id="3c9fc-343">Новые командлеты PowerShell и Справка по обновляемым командлетам включены в App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-343">New PowerShell cmdlets and updateable cmdlet help are included in App-V 5.0 SP3.</span></span> <span data-ttu-id="3c9fc-344">Чтобы скачать модули командлетов, Узнайте, [как загрузить командлеты PowerShell и получить справку по командлетам](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-344">To download the cmdlet modules, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span></span>

### <span data-ttu-id="3c9fc-345">Новые командлеты PowerShell для App-V 5,0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="3c9fc-345">New App-V 5.0 SP3 Server PowerShell cmdlets</span></span>

<span data-ttu-id="3c9fc-346">Добавлены новые командлеты Windows PowerShell для сервера App-V, помогающие управлять группами подключений.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-346">New Windows PowerShell cmdlets for the App-V Server have been added to help you manage connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-347">Командлет</span><span class="sxs-lookup"><span data-stu-id="3c9fc-347">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-348">Описание</span><span class="sxs-lookup"><span data-stu-id="3c9fc-348">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-349">Add-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="3c9fc-349">Add-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-350">Добавляет пакет в конец группы подключения&#39;s и позволяет настроить пакет как необязательный и/или без версии в группе подключения.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-350">Appends a package to the end of a connection group&#39;s package list and enables you to configure the package as optional and/or with no version within the connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-351">Set-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="3c9fc-351">Set-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-352">Позволяет изменять сведения о пакете группы подключения, например, является ли это необязательным.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-352">Enables you to edit details about the connection group package, such as whether it is optional.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-353">Remove-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="3c9fc-353">Remove-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-354">Удаление пакета из группы подключения.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-354">Removes a package from a connection group.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="3c9fc-355">Вызов справки по командлетам PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c9fc-355">Getting help for the PowerShell cmdlets</span></span>

<span data-ttu-id="3c9fc-356">Справка по командлетам доступна в следующих форматах:</span><span class="sxs-lookup"><span data-stu-id="3c9fc-356">Cmdlet help is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-357">Формат</span><span class="sxs-lookup"><span data-stu-id="3c9fc-357">Format</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-358">Описание</span><span class="sxs-lookup"><span data-stu-id="3c9fc-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-359">Как загружаемый модуль</span><span class="sxs-lookup"><span data-stu-id="3c9fc-359">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-360">Чтобы получить последнюю справку после загрузки модуля командлета, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-360">To get the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="3c9fc-361">Откройте Windows PowerShell или интегрированную среду сценариев Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-361">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="3c9fc-362">Чтобы загрузить командлеты для нужного модуля, введите одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="3c9fc-362">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-363">Компонент App-V</span><span class="sxs-lookup"><span data-stu-id="3c9fc-363">App-V component</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-364">Команда для ввода</span><span class="sxs-lookup"><span data-stu-id="3c9fc-364">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-365">Сервер App-V</span><span class="sxs-lookup"><span data-stu-id="3c9fc-365">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-366">Update-Help-Module AppvServer</span><span class="sxs-lookup"><span data-stu-id="3c9fc-366">Update-Help-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-367">Секвенсор App-V</span><span class="sxs-lookup"><span data-stu-id="3c9fc-367">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-368">Update-Help-Module AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="3c9fc-368">Update-Help-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-369">Клиент App-V</span><span class="sxs-lookup"><span data-stu-id="3c9fc-369">App-V client</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-370">Update-Help-Module AppvClient</span><span class="sxs-lookup"><span data-stu-id="3c9fc-370">Update-Help-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-371">На веб-страницах TechNet</span><span class="sxs-lookup"><span data-stu-id="3c9fc-371">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-372">Ознакомьтесь с разделом App-V в разделе <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> Автоматизация пакета оптимизации рабочей среды Microsoft для Windows PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-372">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="3c9fc-373">Дополнительные сведения можно найти [в разделе как загрузить командлеты PowerShell и получить справку по командлетам](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-373">For more information, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span></span>

## <a href="" id="bkmk-pvad-hidden"></a><span data-ttu-id="3c9fc-374">Основной каталог виртуального приложения (PVAD) является скрытым, но его можно включить</span><span class="sxs-lookup"><span data-stu-id="3c9fc-374">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>


<span data-ttu-id="3c9fc-375">Основной каталог виртуальных приложений (PVAD) будет скрыт в App-V 5,0 SP3, но его можно снова включить и сделать видимым с помощью одного из указанных ниже методов.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-375">The primary virtual application directory (PVAD) is hidden in App-V 5.0 SP3, but you can turn it back on and make it visible by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-376">Метод</span><span class="sxs-lookup"><span data-stu-id="3c9fc-376">Method</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-377">Действия</span><span class="sxs-lookup"><span data-stu-id="3c9fc-377">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c9fc-378">Использование параметра командной строки</span><span class="sxs-lookup"><span data-stu-id="3c9fc-378">Use a command line parameter</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-379">Передайте <strong> параметр – EnablePVADControl в </strong> <strong>Sequencer.exe</strong> .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-379">Pass the <strong>–EnablePVADControl</strong> parameter to the <strong>Sequencer.exe</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c9fc-380">Создание подраздела реестра</span><span class="sxs-lookup"><span data-stu-id="3c9fc-380">Create a registry subkey</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="3c9fc-381">В редакторе реестра перейдите к разделу:</span><span class="sxs-lookup"><span data-stu-id="3c9fc-381">In the Registry Editor, navigate to:</span></span> <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong><span data-ttu-id="3c9fc-382">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-382">Note</span></span></strong><br/><p><span data-ttu-id="3c9fc-383">Если <code>Compatibility</code> подраздел не существует, его необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-383">If the <code>Compatibility</code> subkey doesn’t exist, you must create it.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="3c9fc-384">Создайте параметр DWORD с именем <strong> EnablePVADControl </strong> и установите для него значение <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3c9fc-384">Create a DWORD Value named <strong>EnablePVADControl</strong>, and set the value to <strong>1</strong>.</span></span></p>
<p><span data-ttu-id="3c9fc-385"><strong>Нулевое значение </strong> означает, что PVAD является скрытым.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-385">A value of <strong>0</strong> means that PVAD is hidden.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>



<span data-ttu-id="3c9fc-386">**Дополнительные сведения о PVAD:** При использовании секвенсора для создания пакета можно указать любой путь установки пакета.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-386">**More about PVAD:** When you use the Sequencer to create a package, you can enter any installation path for the package.</span></span> <span data-ttu-id="3c9fc-387">В предыдущих версиях App-V вам требовалось указать основной каталог виртуальных приложений (PVAD) для приложения в качестве пути.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-387">In past versions of App-V, you were required to specify the primary virtual application directory (PVAD) of the application as the path.</span></span> <span data-ttu-id="3c9fc-388">PVAD — это каталог, в который вы обычно устанавливаете приложение на локальном компьютере, если вы не используете App-V.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-388">PVAD is the directory to which you would typically install an application on your local computer if you weren’t using App-V.</span></span> <span data-ttu-id="3c9fc-389">Например, если вы устанавливаете Office на компьютере, PVAD, как правило, C:\\program Files Files\\Microsoft Office\\.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-389">For example, if you were installing Office on a computer, the PVAD typically would be C:\\Program Files\\Microsoft Office\\.</span></span>

## <a href="" id="bkmk-pub-metadata-clientversion"></a><span data-ttu-id="3c9fc-390">ClientVersion требуется для просмотра метаданных публикации App-V</span><span class="sxs-lookup"><span data-stu-id="3c9fc-390">ClientVersion is required to view App-V publishing metadata</span></span>


<span data-ttu-id="3c9fc-391">В приложении App-V 5,0 с пакетом обновления 3 (SP3) при выполнении запроса метаданных на сервере публикации App-V необходимо указать указанные ниже значения.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-391">In App-V 5.0 SP3, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c9fc-392">Значение</span><span class="sxs-lookup"><span data-stu-id="3c9fc-392">Value</span></span></th>
<th align="left"><span data-ttu-id="3c9fc-393">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3c9fc-393">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3c9fc-394">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="3c9fc-394">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-395">Если вы пропускаете <strong> </strong> параметр ClientVersion из запроса, метаданные не включают новую функциональность App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-395">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the new App-V 5.0 SP3 features.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3c9fc-396">ClientOS</span><span class="sxs-lookup"><span data-stu-id="3c9fc-396">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3c9fc-397">Это значение нужно указывать только в том случае, если в качестве последовательности пакетов выбраны определенные клиентские операционные системы.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-397">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="3c9fc-398">Если вы выбрали вариант по умолчанию (все операционные системы), не указывайте это значение в запросе.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-398">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="3c9fc-399">Если вы пропускаете <strong> </strong> параметр ClientOS из запроса, только пакеты, упорядоченные для поддержки любой операционной системы, отображаются в метаданных.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-399">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="3c9fc-400">Синтаксис и примеры этого запроса приведены в разделе [Просмотр метаданных публикации сервера App-V Server](viewing-app-v-server-publishing-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-400">For syntax and examples of this query, see [Viewing App-V Server Publishing Metadata](viewing-app-v-server-publishing-metadata.md).</span></span>

## <a href="" id="bkmk-event-logs-moved"></a><span data-ttu-id="3c9fc-401">Журналы событий App-V объединены</span><span class="sxs-lookup"><span data-stu-id="3c9fc-401">App-V event logs have been consolidated</span></span>


<span data-ttu-id="3c9fc-402">Перечисленные ниже журналы событий, ранее размещенные в \*\* &lt; компонентах &gt; журналов приложений и служб/Microsoft/AppV/App-V\*\*, были перемещены в **журналы приложений и служб/Microsoft/AppV/ServiceLog**.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-402">The following event logs, previously located at **Applications and Services Logs/Microsoft/AppV/&lt;App-V component&gt;**, have been moved to **Applications and Services Logs/Microsoft/AppV/ServiceLog**.</span></span>

<span data-ttu-id="3c9fc-403">Чтобы просмотреть журналы, выберите **вид** &gt; **Показать аналитические и отладочные журналы** в приложении "Просмотр событий".</span><span class="sxs-lookup"><span data-stu-id="3c9fc-403">To view the logs, select **View** &gt; **Show Analytic and Debug Logs** in the Event Viewer application.</span></span>

<span data-ttu-id="3c9fc-404">Клиентский каталог клиент-клиент — клиент клиента для интеграции: клиент клиент-службы клиента-PackageConfig Client-Vemgr Client-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary подсистемы-подсистемы ActiveX-AppPath подсистем</span><span class="sxs-lookup"><span data-stu-id="3c9fc-404">Client-Catalog Client-Integration Client-Orchestration Client-PackageConfig Client-Scripting Client-Service Client-Vemgr Client-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary Subsystems-ActiveX Subsystems-AppPath Subsystems-Com Subsystems-fta</span></span>

## <span data-ttu-id="3c9fc-405">Получение технологий для MDOP</span><span class="sxs-lookup"><span data-stu-id="3c9fc-405">How to Get MDOP Technologies</span></span>


<span data-ttu-id="3c9fc-406">App-V входит в состав пакета оптимизации рабочего стола Майкрософт (MDOP).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-406">App-V is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="3c9fc-407">MDOP входит в состав Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="3c9fc-407">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="3c9fc-408">Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в [статьях получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="3c9fc-408">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="3c9fc-409">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3c9fc-409">Related topics</span></span>


[<span data-ttu-id="3c9fc-410">Заметки о выпуске для App-V 5.0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="3c9fc-410">Release Notes for App-V 5.0 SP3</span></span>](release-notes-for-app-v-50-sp3.md)









