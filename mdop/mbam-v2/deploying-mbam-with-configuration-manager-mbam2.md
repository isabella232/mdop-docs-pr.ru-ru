---
title: Развертывание MBAM с помощью диспетчера конфигураций
description: Развертывание MBAM с помощью диспетчера конфигураций
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823452"
---
# <span data-ttu-id="70068-103">Развертывание MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="70068-103">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="70068-104">Ниже описано, как развернуть администрирование и мониторинг Microsoft BitLocker (MBAM) в Microsoft System Center Configuration Manager 2007 или MicrosoftSystemCenter2012 ConfigurationManager с помощью usingthe рекомендованной конфигурации, описанной в разделе [Приступая к работе с помощью диспетчера конфигураций](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="70068-104">The following procedures describe how to deploy Microsoft BitLocker Administration and Monitoring (MBAM) with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager by usingthe recommended configuration, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="70068-105">Рекомендуемая конфигурация — Установка функций администрирования и наблюдения на одном или нескольких серверах администрирования и мониторинга Microsoft BitLocker и установка Microsoft System Center Configuration Manager 2007 или MicrosoftSystemCenter2012 ConfigurationManager на отдельном сервере.</span><span class="sxs-lookup"><span data-stu-id="70068-105">The recommended configuration is to install the Administration and Monitoring features on one or more Microsoft BitLocker Administration and Monitoring servers, and install Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager on a separate server.</span></span>

<span data-ttu-id="70068-106">Перед началом установки убедитесь, что у вас есть необходимые условия и требования к оборудованию и программному обеспечению для установки MBAM с помощью Configuration Manager, проверив [Планирование развертывания MBAM с помощью Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="70068-106">Before you start the installation, ensure that you have met the prerequisites and hardware and software requirements for installing MBAM with Configuration Manager by reviewing [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="70068-107">Если вы когда-либо переустанавливаете MBAM с топологией Configuration Manager, необходимо сначала удалить некоторые объекты Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="70068-107">If you ever have to reinstall MBAM with the Configuration Manager topology, you will need to remove certain Configuration Manager objects first.</span></span> <span data-ttu-id="70068-108">Дополнительные сведения читайте в [статье базы знаний](https://go.microsoft.com/fwlink/?LinkId=286306) .</span><span class="sxs-lookup"><span data-stu-id="70068-108">Read the [Knowledge Base article](https://go.microsoft.com/fwlink/?LinkId=286306) for more information.</span></span>

<span data-ttu-id="70068-109">Инструкции по установке MBAM с помощью Configuration Manager сгруппированы по следующим категориям.</span><span class="sxs-lookup"><span data-stu-id="70068-109">The steps to install MBAM with Configuration Manager are grouped into the following categories.</span></span> <span data-ttu-id="70068-110">Выполните эти действия для каждой категории, чтобы завершить установку.</span><span class="sxs-lookup"><span data-stu-id="70068-110">Complete the steps for each category to complete the installation.</span></span>

## <span data-ttu-id="70068-111">Порядок создания или изменения MOF-файлов</span><span class="sxs-lookup"><span data-stu-id="70068-111">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="70068-112">Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker с помощью отчетов Configuration Manager MBAM, необходимо изменить файл **Configuration. mof** , а также изменить или создать файл Sms \ _def. mof в зависимости от того, какая версия Configuration Manager используется.</span><span class="sxs-lookup"><span data-stu-id="70068-112">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the **Configuration.mof** file, and either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

[<span data-ttu-id="70068-113">Порядок создания или изменения MOF-файлов</span><span class="sxs-lookup"><span data-stu-id="70068-113">How to Create or Edit the mof Files</span></span>](how-to-create-or-edit-the-mof-files.md)

## <span data-ttu-id="70068-114">Порядок установки MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="70068-114">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="70068-115">В этом разделе приводятся инструкции по установке следующих параметров: MBAM на сервере Configuration Manager. Базы данных восстановления и аудита на сервере базы данных; а также на сервере администрирования и мониторинга доступны серверные функции администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="70068-115">This section provides steps about how to install the following: MBAM on the Configuration Manager Server; the Recovery and Audit Databases on the Database Server; and the Administration and Monitoring Server features on the Administration and Monitoring Server.</span></span>

[<span data-ttu-id="70068-116">Порядок установки MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="70068-116">How to Install MBAM with Configuration Manager</span></span>](how-to-install-mbam-with-configuration-manager.md)

## <span data-ttu-id="70068-117">Проверка установки компонентов сервера MBAM на сервере Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="70068-117">How to Validate the MBAM Server Feature Installation on the Configuration Manager Server</span></span>


<span data-ttu-id="70068-118">После завершения установки администрирования и наблюдения за помощью Microsoft BitLocker убедитесь, что установка успешно завершила настройку всех необходимых функций MBAM, необходимых для сервера Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="70068-118">When the Microsoft BitLocker Administration and Monitoring installation is complete, validate that the installation has successfully set up all the necessary MBAM features required for the Configuration Manager Server.</span></span>

[<span data-ttu-id="70068-119">Порядок проверки установки MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="70068-119">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## <span data-ttu-id="70068-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="70068-120">Related topics</span></span>


[<span data-ttu-id="70068-121">Использование MBAM с диспетчером конфигураций</span><span class="sxs-lookup"><span data-stu-id="70068-121">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





