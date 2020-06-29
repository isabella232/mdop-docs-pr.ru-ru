---
title: Развертывание клиента MBAM на настольных компьютерах и ноутбуках
description: Развертывание клиента MBAM на настольных компьютерах и ноутбуках
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824479"
---
# <span data-ttu-id="11488-103">Развертывание клиента MBAM на настольных компьютерах и ноутбуках</span><span class="sxs-lookup"><span data-stu-id="11488-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="11488-104">В этой статье объясняется, как развернуть клиент MBAM на компьютерах конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="11488-104">This topic explains how to deploy the MBAM Client to end users’ computers.</span></span> <span data-ttu-id="11488-105">Вы можете развернуть клиент MBAM с помощью электронной системы распространения программного обеспечения, например доменных служб Active Directory или MicrosoftSystemCenterConfiguration Manager.</span><span class="sxs-lookup"><span data-stu-id="11488-105">You can deploy the MBAM Client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfiguration Manager.</span></span>

<span data-ttu-id="11488-106">Чтобы развернуть клиент MBAM в рамках развертывания Windows, Узнайте, [как включить BitLocker с помощью MBAM в составе развертывания Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="11488-106">To deploy the MBAM Client as part of a Windows deployment, see [How to Enable BitLocker by Using MBAM as Part of a Windows Deployment](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span></span>

<span data-ttu-id="11488-107">Прежде чем приступить к развертыванию клиента MBAM, проверьте [конфигурации, поддерживаемые MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="11488-107">Before you start the MBAM Client deployment, review the [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="11488-108">Развертывание клиента MBAM на настольном компьютере или ноутбуке</span><span class="sxs-lookup"><span data-stu-id="11488-108">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="11488-109">Найдите установочные файлы клиента MBAM, которые предоставляются вместе с программным обеспечением MBAM.</span><span class="sxs-lookup"><span data-stu-id="11488-109">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="11488-110">Использование доменных служб Active Directory или средства корпоративного развертывания программного обеспечения, например диспетчера MicrosoftSystemCenterConfiguration Manager, для развертывания пакета установщика Windows на целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="11488-110">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfiguration Manager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="11488-111">Настройте параметры распространения или параметры групповой политики, чтобы запустить установочный файл клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="11488-111">Configure the distribution settings or Group Policy settings to run the MBAM Client installation file.</span></span>

    <span data-ttu-id="11488-112">После успешной установки клиент MBAM применяет параметры групповой политики, полученные от контроллера домена, для запуска функций шифрования диска BitLocker и управления ими.</span><span class="sxs-lookup"><span data-stu-id="11488-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker Drive Encryption and management functions.</span></span>

    <span data-ttu-id="11488-113">**Важно!**  Клиент MBAM не запускает действия по шифрованию диска BitLocker при активном соединении с протоколом удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="11488-113">**Important** The MBAM Client does not start BitLocker Drive Encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="11488-114">Чтобы начать шифрование диска BitLocker, необходимо закрыть все соединения с удаленной консолью и войти в систему с помощью физического сеанса консоли.</span><span class="sxs-lookup"><span data-stu-id="11488-114">All remote console connections must be closed and a user must be logged on to a physical console session before BitLocker Drive Encryption begins.</span></span>

     


## <span data-ttu-id="11488-115">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="11488-115">Related topics</span></span>
[<span data-ttu-id="11488-116">Развертывание клиента MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="11488-116">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="11488-117">Планирование развертывания клиента MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="11488-117">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

 

## <span data-ttu-id="11488-118">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="11488-118">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="11488-119">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="11488-119">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="11488-120">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="11488-120">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





