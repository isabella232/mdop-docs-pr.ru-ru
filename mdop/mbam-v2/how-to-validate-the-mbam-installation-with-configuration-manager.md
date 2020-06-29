---
title: Порядок проверки установки MBAM с помощью диспетчера конфигураций
description: Порядок проверки установки MBAM с помощью диспетчера конфигураций
author: dansimp
ms.assetid: 8e268539-91c3-4e8a-baae-faf3605da818
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 500c6f6ee5138b5677bf1fa20e2627a56981df1f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822639"
---
# <span data-ttu-id="54e99-103">Порядок проверки установки MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="54e99-103">How to Validate the MBAM Installation with Configuration Manager</span></span>


<span data-ttu-id="54e99-104">После установки службы администрирования и мониторинга Microsoft BitLocker (MBAM) с помощью Configuration Manager убедитесь, что установка успешно завершила настройку всех необходимых функций для MBAM, выполнив описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="54e99-104">After installing Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, validate that the installation has successfully set up all the necessary features for MBAM by completing the following steps.</span></span>

**<span data-ttu-id="54e99-105">Проверка установки компонента сервера MBAM с помощью Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="54e99-105">To validate the MBAM Server feature installation with Configuration Manager</span></span>**

1.  <span data-ttu-id="54e99-106">На сервере, на котором развернут Диспетчер конфигураций System Center Configuration Manager, откройте **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="54e99-106">On the server where System Center Configuration Manager is deployed, open **Control Panel**.</span></span> <span data-ttu-id="54e99-107">Выберите программу, которая использовалась для удаления или изменения программы.</span><span class="sxs-lookup"><span data-stu-id="54e99-107">Select the program that is used to uninstall or change a program.</span></span> <span data-ttu-id="54e99-108">Убедитесь в том, что в списке программ и компонентов отображаются элементы **управления и наблюдения Microsoft BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="54e99-108">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the list of programs and features.</span></span>

    <span data-ttu-id="54e99-109">**Примечание**  Для проверки установки необходимо использовать учетную запись домена, которая содержит учетные данные администратора локального компьютера на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="54e99-109">**Note** To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>

     

2.  <span data-ttu-id="54e99-110">С помощью консоли Configuration Manager убедитесь, что на экране появится новая коллекция под названием "MBAM поддерживаемые компьютеры".</span><span class="sxs-lookup"><span data-stu-id="54e99-110">Use the Configuration Manager console to confirm that a new collection, called “MBAM Supported Computers,” is displayed.</span></span>

    <span data-ttu-id="54e99-111">Чтобы просмотреть коллекцию в Configuration Manager 2007: щелкните **база данных сайта** ( &lt; **SiteCode** &gt;  -  &lt; **ServerName** &gt; , &lt; **SiteName** &gt; ), **Управление компьютером**.</span><span class="sxs-lookup"><span data-stu-id="54e99-111">To view the collection with Configuration Manager 2007: Click **Site Database** (&lt;**SiteCode**&gt; - &lt;**ServerName**&gt;, &lt;**SiteName**&gt;), **Computer Management**.</span></span>

    <span data-ttu-id="54e99-112">Чтобы просмотреть коллекцию с помощью SystemCenter2012 ConfigurationManager: щелкните рабочую область **ресурсы и соответствия** , **семейства устройств**.</span><span class="sxs-lookup"><span data-stu-id="54e99-112">To view the collection with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Device Collections**.</span></span>

3.  <span data-ttu-id="54e99-113">С помощью консоли Configuration Manager убедитесь в том, что в папке **MBAM** указаны следующие отчеты:</span><span class="sxs-lookup"><span data-stu-id="54e99-113">Use the Configuration Manager console to verify that the following reports are listed in the **MBAM** folder:</span></span>

    -   <span data-ttu-id="54e99-114">Соответствие требованиям компьютера BitLocker</span><span class="sxs-lookup"><span data-stu-id="54e99-114">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="54e99-115">Панель мониторинга соответствия требованиям для предприятия BitLocker</span><span class="sxs-lookup"><span data-stu-id="54e99-115">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="54e99-116">Сведения о соответствии требованиям BitLocker для предприятий</span><span class="sxs-lookup"><span data-stu-id="54e99-116">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="54e99-117">Сводка по соответствию требованиям для предприятий BitLocker</span><span class="sxs-lookup"><span data-stu-id="54e99-117">BitLocker Enterprise Compliance Summary</span></span>

    <span data-ttu-id="54e99-118">Для просмотра отчетов в Configuration Manager 2007: выберите **отчеты**, **службы отчетов**, \ \ \ \ &lt; **ИмяСервера** &gt; , **папки отчетов** .</span><span class="sxs-lookup"><span data-stu-id="54e99-118">To view the reports with Configuration Manager 2007: Click **Reporting**, **Reporting Services**, \\\\&lt;**ServerName**&gt;, **Report Folders**</span></span>

    <span data-ttu-id="54e99-119">Чтобы просмотреть отчеты с помощью SystemCenter2012 ConfigurationManager, выберите рабочую **Monitoring** область "Мониторинг **", а**также **отчеты**.</span><span class="sxs-lookup"><span data-stu-id="54e99-119">To view the reports with SystemCenter2012 ConfigurationManager: Click the **Monitoring** workspace, **Reporting**, **Reports**.</span></span>

4.  <span data-ttu-id="54e99-120">С помощью консоли Configuration Manager убедитесь, что в списке указан шаблон базовой конфигурации "Защита BitLocker".</span><span class="sxs-lookup"><span data-stu-id="54e99-120">Use the Configuration Manager console to confirm that the configuration baseline “BitLocker Protection” is listed.</span></span>

    <span data-ttu-id="54e99-121">Для просмотра шаблонов базовой конфигурации с помощью Configuration Manager 2007: щелкните **Управление требуемой конфигурацией**, **шаблоны базовой конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="54e99-121">To view the configuration baselines with Configuration Manager 2007: Click **Desired Configuration Management**, **Configuration Baselines**.</span></span>

    <span data-ttu-id="54e99-122">Чтобы просмотреть шаблоны базовой конфигурации с помощью SystemCenter2012 ConfigurationManager: щелкните рабочую область **ресурсы и соответствие требованиям** , **Параметры соответствия требованиям**, **шаблоны базовой конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="54e99-122">To view the configuration baselines with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Compliance Settings**, **Configuration Baselines**.</span></span>

5.  <span data-ttu-id="54e99-123">С помощью консоли Configuration Manager убедитесь в том, что отображаются следующие новые элементы конфигурации:</span><span class="sxs-lookup"><span data-stu-id="54e99-123">Use the Configuration Manager console to confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="54e99-124">Защита фиксированных дисков с данными BitLocker</span><span class="sxs-lookup"><span data-stu-id="54e99-124">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="54e99-125">Защита диска операционной системы BitLocker</span><span class="sxs-lookup"><span data-stu-id="54e99-125">BitLocker Operating System Drive Protection</span></span>

    <span data-ttu-id="54e99-126">Для просмотра элементов конфигурации с помощью Configuration Manager 2007: щелкните **Управление требуемой конфигурацией**, **элементы конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="54e99-126">To view the configuration items with Configuration Manager 2007: Click **Desired Configuration Management**, **Configuration Items**.</span></span>

    <span data-ttu-id="54e99-127">Чтобы просмотреть элементы конфигурации с помощью SystemCenter2012 ConfigurationManager: щелкните рабочую область **ресурсы и соответствие** , **Параметры соответствия требованиям**, **элементы конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="54e99-127">To view the configuration items with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Compliance Settings**, **Configuration Items**.</span></span>

## <span data-ttu-id="54e99-128">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="54e99-128">Related topics</span></span>


[<span data-ttu-id="54e99-129">Развертывание MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="54e99-129">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





