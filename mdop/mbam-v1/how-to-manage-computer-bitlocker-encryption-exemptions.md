---
title: Управление исключениями шифрования BitLocker для компьютера
description: Управление исключениями шифрования BitLocker для компьютера
author: dansimp
ms.assetid: d4400a0d-b36b-4cf5-a294-1f53ec47f9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51b93061468508900eaee7fce8a7827e2db61d19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825679"
---
# <span data-ttu-id="dbf00-103">Управление исключениями шифрования BitLocker для компьютера</span><span class="sxs-lookup"><span data-stu-id="dbf00-103">How to Manage Computer BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="dbf00-104">Вы можете использовать администрирование и мониторинг Microsoft BitLocker (MBAM), чтобы исключить определенные компьютеры из системы защиты BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dbf00-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to exempt certain computers from BitLocker protection.</span></span> <span data-ttu-id="dbf00-105">Например, в Организации может быть решено управлять исключением BitLocker на отдельном компьютере.</span><span class="sxs-lookup"><span data-stu-id="dbf00-105">For example, an organization may decide to control BitLocker exemption on a computer-by-computer basis.</span></span>

<span data-ttu-id="dbf00-106">Чтобы исключить компьютер из шифрования BitLocker, необходимо добавить его в группу безопасности в ActiveDirectoryDomainServices, чтобы обойти любые правила защиты BitLocker на основе компьютеров.</span><span class="sxs-lookup"><span data-stu-id="dbf00-106">To exempt a computer from BitLocker encryption, you must add the computer to a security group in ActiveDirectoryDomainServices in order to bypass any computer-based BitLocker protection rules.</span></span>

<span data-ttu-id="dbf00-107">**Примечание**  Если на компьютере уже установлена защита с помощью BitLocker, политика исключения компьютера не действует.</span><span class="sxs-lookup"><span data-stu-id="dbf00-107">**Note** If the computer is already BitLocker-protected, the computer exemption policy has no effect.</span></span>

 

**<span data-ttu-id="dbf00-108">Исключение компьютера из шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="dbf00-108">To exempt a computer from BitLocker encryption</span></span>**

1.  <span data-ttu-id="dbf00-109">Добавьте учетную запись компьютера, которая должна быть исключена в группу безопасности в ActiveDirectoryDomainServices.</span><span class="sxs-lookup"><span data-stu-id="dbf00-109">Add the computer account that you want to be exempted to a security group in ActiveDirectoryDomainServices.</span></span> <span data-ttu-id="dbf00-110">Это позволяет обойти любые правила защиты BitLocker на основе компьютеров.</span><span class="sxs-lookup"><span data-stu-id="dbf00-110">This allows you to bypass any computer-based BitLocker protection rules.</span></span>

2.  <span data-ttu-id="dbf00-111">Создайте объект групповой политики с помощью шаблона групповой политики MBAM и свяжите объект групповой политики с группой Active Directory, созданной на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="dbf00-111">Create a Group Policy Object by using the MBAM Group Policy template, then associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="dbf00-112">Дополнительные сведения о создании необходимых объектов групповой политики можно найти в разделе [Развертывание объектов групповой политики MBAM 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="dbf00-112">For more information about creating the necessary Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

3.  <span data-ttu-id="dbf00-113">При запуске исключенного компьютера клиент MBAM проверяет параметр политики освобождения компьютера и приостанавливает защиту в зависимости от того, входит ли компьютер в группу безопасности исключений BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dbf00-113">When an exempted computer starts, the MBAM client checks the Computer Exemption Policy setting and suspends protection based on whether the computer is part of the BitLocker exemption security group.</span></span>

## <span data-ttu-id="dbf00-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="dbf00-114">Related topics</span></span>


[<span data-ttu-id="dbf00-115">Администрирование компонентов MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="dbf00-115">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





