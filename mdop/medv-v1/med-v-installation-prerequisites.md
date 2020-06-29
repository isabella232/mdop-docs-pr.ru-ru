---
title: Необходимые условия для установки MED-V
description: Необходимые условия для установки MED-V
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824969"
---
# <span data-ttu-id="5cd0a-103">Необходимые условия для установки MED-V</span><span class="sxs-lookup"><span data-stu-id="5cd0a-103">MED-V Installation Prerequisites</span></span>


<span data-ttu-id="5cd0a-104">Ниже приведены условия, необходимые для установки MED-V.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-104">The following are prerequisites for installing MED-V:</span></span>

[<span data-ttu-id="5cd0a-105">Требования к службе каталогов Active Directory</span><span class="sxs-lookup"><span data-stu-id="5cd0a-105">Active Directory Requirements</span></span>](#bkmk-activedirectoryrequirements)

[<span data-ttu-id="5cd0a-106">База данных отчетов</span><span class="sxs-lookup"><span data-stu-id="5cd0a-106">Report Database</span></span>](#bkmk-howtoinstallthereportdatabase)

[<span data-ttu-id="5cd0a-107">Конфигурация программного обеспечения для защиты от вирусов и резервного копирования</span><span class="sxs-lookup"><span data-stu-id="5cd0a-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

[<span data-ttu-id="5cd0a-108">Microsoft Virtual PC 2007 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="5cd0a-108">Microsoft Virtual PC 2007 SP1</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a><span data-ttu-id="5cd0a-109">Требования к службе каталогов Active Directory</span><span class="sxs-lookup"><span data-stu-id="5cd0a-109">Active Directory Requirements</span></span>


<span data-ttu-id="5cd0a-110">При настройке сервера MED-V, если пользователи не являются частью того же домена, которому принадлежит сервер, необходимо установить доверие между доменами.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-110">When configuring the MED-V server, if users are not part of the same domain the server belongs to, a trust must be set between the domains.</span></span>

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a><span data-ttu-id="5cd0a-111">Установка базы данных отчета</span><span class="sxs-lookup"><span data-stu-id="5cd0a-111">How to Install the Report Database</span></span>


<span data-ttu-id="5cd0a-112">Для хранения всех журналов рабочей области для MED-V требуется база данных отчета.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-112">The report database is required for storing all MED-V workspace logs.</span></span> <span data-ttu-id="5cd0a-113">Затем база данных журнала используется для создания отчетов MED-V.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-113">The log database is then used for generating MED-V reports.</span></span> <span data-ttu-id="5cd0a-114">Сведения об отчетах можно найти в разделе [отчетность по MED-V](med-v-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="5cd0a-114">For information about reports, see [MED-V Reporting](med-v-reporting.md).</span></span>

<span data-ttu-id="5cd0a-115">SQL Server можно установить на том же сервере, что и сервер MED-V, или на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-115">SQL Server can be installed on the same server as the MED-V server or on a remote server.</span></span> <span data-ttu-id="5cd0a-116">Если установка выполняется на удаленном сервере, ознакомьтесь со сведениями о том, [как установить SQL Server на удаленном сервере](#bkmk-installingsqlserveronaremoteserver).</span><span class="sxs-lookup"><span data-stu-id="5cd0a-116">If installing on a remote server, see [Installing SQL Server on a Remote Server](#bkmk-installingsqlserveronaremoteserver).</span></span>

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a><span data-ttu-id="5cd0a-117">Установка SQL Server на удаленном сервере</span><span class="sxs-lookup"><span data-stu-id="5cd0a-117">Installing SQL Server on a Remote Server</span></span>

**<span data-ttu-id="5cd0a-118">Установка SQL Server на удаленном сервере</span><span class="sxs-lookup"><span data-stu-id="5cd0a-118">To install SQL Server on a remote server</span></span>**

1.  <span data-ttu-id="5cd0a-119">На удаленном сервере настройте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5cd0a-119">Configure the following on the remote server:</span></span>

    -   <span data-ttu-id="5cd0a-120">Имя экземпляра — экземпляр по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5cd0a-120">Instance name—Default instance</span></span>

    -   <span data-ttu-id="5cd0a-121">Режим проверки подлинности — смешанный режим</span><span class="sxs-lookup"><span data-stu-id="5cd0a-121">Authentication mode—Mixed mode</span></span>

    -   <span data-ttu-id="5cd0a-122">User (пользователь по умолчанию — "SA")</span><span class="sxs-lookup"><span data-stu-id="5cd0a-122">User—The default user created is “sa”</span></span>

    -   <span data-ttu-id="5cd0a-123">Password (пароль) — желаемый пароль</span><span class="sxs-lookup"><span data-stu-id="5cd0a-123">Password—Desired password</span></span>

    -   <span data-ttu-id="5cd0a-124">Параметры сортировки — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5cd0a-124">Collation Settings—Default</span></span>

    -   <span data-ttu-id="5cd0a-125">Ошибка в параметрах отчета об использовании — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5cd0a-125">Error in usage report settings—Default</span></span>

2.  <span data-ttu-id="5cd0a-126">Установите на сервер MED-V следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="5cd0a-126">Install the following files on the MED-V server:</span></span>

    -   <span data-ttu-id="5cd0a-127">Чтобы установить необходимые компоненты для коллекции объектов пакета управления для Microsoft SQL Server2008, скачайте [собственный клиент Microsoft SQL Server2008](https://go.microsoft.com/fwlink/?LinkId=164039) из центра загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-127">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2008, download [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="5cd0a-128">Чтобы установить необходимые компоненты для коллекции объектов пакета управления для Microsoft SQL Server2005, скачайте [собственный клиент Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=164038) из центра загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-128">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="5cd0a-129">Чтобы установить необходимые файлы DLL для Microsoft SQL Server2008, скачайте [коллекцию управляющих объектов Microsoft SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=164041) из центра загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-129">To install the required dll files for Microsoft SQL Server2008, download [Microsoft SQL Server 2008 Management Objects Collection](https://go.microsoft.com/fwlink/?LinkId=164041) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="5cd0a-130">Чтобы установить необходимые файлы DLL для Microsoft SQL Server2005, скачайте [объекты управления Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=164040) из центра загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-130">To install the required dll files for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164040) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="5cd0a-131">Чтобы установить отдельные пакеты установки, предоставляющие дополнительные значения для SQL Server2008, скачайте [пакет дополнительных компонентов Microsoft SQL Server2008](https://go.microsoft.com/fwlink/?LinkId=163960) из центра загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-131">To install the stand-alone install packages that provide additional value for SQL Server2008, download the [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="5cd0a-132">Чтобы установить отдельные пакеты установки, предоставляющие дополнительные значения для SQL Server2005, скачайте [пакет дополнительных компонентов для Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) из центра загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-132">To install the stand-alone install packages that provide additional value for SQL Server2005, download the [Feature Pack for Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) from the Microsoft Download Center.</span></span>

    <span data-ttu-id="5cd0a-133">Дополнительные сведения об этих файлах можно найти в [пакете дополнительных компонентов Microsoft SQL Server2008](https://go.microsoft.com/fwlink/?LinkId=163960) в центре загрузки Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163960) или в [пакете дополнительных компонентов для Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) на веб-странице центра загрузки Майкрософт () https://go.microsoft.com/fwlink/?LinkId=163961) .</span><span class="sxs-lookup"><span data-stu-id="5cd0a-133">For more information about these files, see [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163960) or [Feature Pack for Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163961).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="5cd0a-134">Конфигурация программного обеспечения для защиты от вирусов и резервного копирования</span><span class="sxs-lookup"><span data-stu-id="5cd0a-134">Antivirus/Backup Software Configuration</span></span>


<span data-ttu-id="5cd0a-135">Чтобы предотвратить влияние антивирусной программы на производительность виртуального рабочего стола, рекомендуется исключить следующие типы файлов виртуальных машин из антивирусной программы или обработки резервного копирования, запущенной на узле.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-135">To prevent antivirus activity from affecting the performance of the virtual desktop, it is recommended where possible to exclude the following virtual machine file types from any antivirus or backup processing running on the host:</span></span>

-   <span data-ttu-id="5cd0a-136">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="5cd0a-136">\*.VMC</span></span>

-   <span data-ttu-id="5cd0a-137">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="5cd0a-137">\*.VUD</span></span>

-   <span data-ttu-id="5cd0a-138">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="5cd0a-138">\*.VSV</span></span>

-   <span data-ttu-id="5cd0a-139">\*. CKM</span><span class="sxs-lookup"><span data-stu-id="5cd0a-139">\*.CKM</span></span>

-   <span data-ttu-id="5cd0a-140">\*. EVHD</span><span class="sxs-lookup"><span data-stu-id="5cd0a-140">\*.EVHD</span></span>

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a><span data-ttu-id="5cd0a-141">Установка и настройка Microsoft Virtual PC2007 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="5cd0a-141">How to Install and Configure Microsoft Virtual PC2007 SP1</span></span>


<span data-ttu-id="5cd0a-142">**Важно!**  Если Virtual PC для Windows существует на главном компьютере, удалите его перед установкой Virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-142">**Important** If Virtual PC for Windows exists on the host computer, uninstall it before installing Virtual PC2007 SP1.</span></span>

 

**<span data-ttu-id="5cd0a-143">Установка Microsoft Virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="5cd0a-143">To install Microsoft Virtual PC2007 SP1</span></span>**

1.  <span data-ttu-id="5cd0a-144">Загрузите виртуальный PC2007 пакет обновления 1 (SP1) с [Virtual PC 2007](https://go.microsoft.com/fwlink/?LinkId=142994)с помощью центра загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-144">Download Virtual PC2007 SP1 from the Microsoft Download Center [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).</span></span>

2.  <span data-ttu-id="5cd0a-145">Запустите установочный файл на главном компьютере и следуйте инструкциям мастера.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-145">Run the installation file on the host computer, and follow the wizard.</span></span>

3.  <span data-ttu-id="5cd0a-146">Установите виртуальную версию PC2007 SP1 на главном компьютере в режиме с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-146">Install Virtual PC2007 SP1 update on the host computer in elevated mode.</span></span>

    <span data-ttu-id="5cd0a-147">Дополнительные сведения можно найти [в описании исправления для Virtual PC 2007 с пакетом обновления 1 (SP1)](https://go.microsoft.com/fwlink/?LinkId=150575).</span><span class="sxs-lookup"><span data-stu-id="5cd0a-147">For more information, see [the description of the hotfix package for Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).</span></span>

    <span data-ttu-id="5cd0a-148">**Примечание**  Для запуска Virtual PC2007 SP1 требуется обновление виртуальных PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="5cd0a-148">**Note** The Virtual PC2007 SP1 update is required for running Virtual PC2007 SP1.</span></span>

     

## <span data-ttu-id="5cd0a-149">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5cd0a-149">Related topics</span></span>


[<span data-ttu-id="5cd0a-150">Поддерживаемые конфигурации</span><span class="sxs-lookup"><span data-stu-id="5cd0a-150">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

 

 





