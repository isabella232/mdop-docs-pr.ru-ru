---
title: Развертывание клиента MBAM на настольных компьютерах и ноутбуках
description: Развертывание клиента MBAM на настольных компьютерах и ноутбуках
author: dansimp
ms.assetid: f32927a2-4c05-4da8-acca-1108d1dfdb7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4f8597cc182c037983a89efd60c5ef935712ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825542"
---
# <span data-ttu-id="570c0-103">Развертывание клиента MBAM на настольных компьютерах и ноутбуках</span><span class="sxs-lookup"><span data-stu-id="570c0-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="570c0-104">Клиент администрирования и мониторинга Microsoft BitLocker (MBAM) позволяет администраторам принудительно применять и отслеживать шифрование диска BitLocker на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="570c0-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="570c0-105">Клиент MBAM можно интегрировать в организацию, развертывая клиент с помощью средств, например доменных служб Active Directory или средства корпоративного развертывания программного обеспечения, например MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="570c0-105">The MBAM Client can be integrated into an organization by deploying the client through tools, such as Active Directory Domain Services or an enterprise software deployment tool such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

<span data-ttu-id="570c0-106">**Примечание**  Сведения о требованиях к системе клиента MBAM можно найти в разделе [Поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="570c0-106">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

**<span data-ttu-id="570c0-107">Развертывание клиента MBAM на настольном компьютере или ноутбуке</span><span class="sxs-lookup"><span data-stu-id="570c0-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="570c0-108">Найдите установочные файлы клиента MBAM, которые предоставляются вместе с программным обеспечением MBAM.</span><span class="sxs-lookup"><span data-stu-id="570c0-108">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="570c0-109">Развертывание пакета установщика Windows на целевые компьютеры с помощью доменных служб Active Directory или средства корпоративного развертывания программного обеспечения, например MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="570c0-109">Deploy the Windows Installer package to target computers by using Active Directory Domain Services or an enterprise software deployment tool, such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

    <span data-ttu-id="570c0-110">**Примечание**  Для развертывания пакета установщика Windows не следует использовать групповую политику.</span><span class="sxs-lookup"><span data-stu-id="570c0-110">**Note** You should not use Group Policy to deploy the Windows Installer package.</span></span>

     

3.  <span data-ttu-id="570c0-111">Настройте параметры распространения или групповую политику для запуска установочного файла клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="570c0-111">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="570c0-112">После успешной установки клиент MBAM применяет параметры групповой политики, полученные от контроллера домена, для запуска функций шифрования и управления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="570c0-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="570c0-113">Дополнительные сведения о параметрах групповой политики MBAM можно найти в разделе [планирование MBAM 1,0 групповых политик](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="570c0-113">For more information about MBAM Group Policy settings, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

    <span data-ttu-id="570c0-114">**Важно!**  Клиент MBAM не будет запускать действия по шифрованию BitLocker, если активно подключение по протоколу удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="570c0-114">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="570c0-115">Прежде чем начнется шифрование BitLocker, необходимо закрыть все соединения с удаленной консолью.</span><span class="sxs-lookup"><span data-stu-id="570c0-115">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="570c0-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="570c0-116">Related topics</span></span>


[<span data-ttu-id="570c0-117">Развертывание клиента MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="570c0-117">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





