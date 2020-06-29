---
title: Развертывание клиента MBAM на настольных компьютерах и ноутбуках
description: Развертывание клиента MBAM на настольных компьютерах и ноутбуках
author: dansimp
ms.assetid: 56744922-bfdd-48f6-ae01-645ff53b64a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49340ae970dafc9d263f5564e7981a402da40f19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813008"
---
# <span data-ttu-id="f7b1f-103">Развертывание клиента MBAM на настольных компьютерах и ноутбуках</span><span class="sxs-lookup"><span data-stu-id="f7b1f-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="f7b1f-104">Клиент администрирования и мониторинга Microsoft BitLocker (MBAM) позволяет администраторам принудительно применять и отслеживать шифрование диска BitLocker на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-104">The Microsoft BitLocker Administration and Monitoring (MBAM) client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="f7b1f-105">Клиент BitLocker может быть интегрирован в организацию путем развертывания клиента с помощью электронной системы распространения программного обеспечения, например доменных служб Active Directory или MicrosoftSystemCenterConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfigurationManager.</span></span>

<span data-ttu-id="f7b1f-106">**Примечание**  Сведения о требованиях к клиентским системам администрирования и мониторинга Microsoft BitLocker можно найти в разделе [Поддерживаемые конфигурации MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="f7b1f-106">**Note** To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

 

**<span data-ttu-id="f7b1f-107">Развертывание клиента MBAM на настольном компьютере или ноутбуке</span><span class="sxs-lookup"><span data-stu-id="f7b1f-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="f7b1f-108">Найдите установочные файлы клиента MBAM, которые предоставляются вместе с программным обеспечением MBAM.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-108">Locate the MBAM client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="f7b1f-109">Использование доменных служб Active Directory или средства корпоративного развертывания программного обеспечения, например MicrosoftSystemCenterConfigurationManager, для развертывания пакета установщика Windows на целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-109">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfigurationManager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="f7b1f-110">Настройте параметры распространения или групповую политику для запуска установочного файла клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-110">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="f7b1f-111">После успешной установки клиент MBAM применяет параметры групповой политики, полученные от контроллера домена, для запуска функций шифрования и управления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-111">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="f7b1f-112">Дополнительные сведения о параметрах групповой политики MBAM можно найти в разделе [планирование MBAM 2,0 групповых политик](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="f7b1f-112">For more information about MBAM group policy settings, see [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span></span>

    <span data-ttu-id="f7b1f-113">**Важно!**  Клиент MBAM не будет запускать действия по шифрованию BitLocker, если активно подключение по протоколу удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-113">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="f7b1f-114">Прежде чем начнется шифрование BitLocker, необходимо закрыть все соединения с удаленной консолью.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-114">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="f7b1f-115">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f7b1f-115">Related topics</span></span>


[<span data-ttu-id="f7b1f-116">Развертывание клиента MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f7b1f-116">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





