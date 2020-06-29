---
title: Скрытие элемента шифрования диска BitLocker по умолчанию на панели управления
description: Скрытие элемента шифрования диска BitLocker по умолчанию на панели управления
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823099"
---
# <span data-ttu-id="68f8d-103">Скрытие элемента шифрования диска BitLocker по умолчанию на панели управления</span><span class="sxs-lookup"><span data-stu-id="68f8d-103">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>


<span data-ttu-id="68f8d-104">В этой статье описано, как скрыть элемент панели управления **шифрованием диска BitLocker** , который отображается по умолчанию на панели управления в составе операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="68f8d-104">This topic describes how to hide the **BitLocker Drive Encryption** Control Panel item, which appears by default on Control Panel as part of the Windows operating system.</span></span>

<span data-ttu-id="68f8d-105">**Примечание**  Администрирование и мониторинг Microsoft BitLocker (MBAM) создает дополнительный настраиваемый элемент панели управления, который называется **параметрами шифрования BitLocker**, позволяющим конечным пользователям управлять своим PIN-кодом и паролем, включать BitLocker для диска и проверять шифрование.</span><span class="sxs-lookup"><span data-stu-id="68f8d-105">**Note** Microsoft BitLocker Administration and Monitoring (MBAM) creates an additional, custom Control Panel item, called **BitLocker Encryption Options**, which enables end users to manage their PIN and password, turn on BitLocker for a drive, and check encryption.</span></span>

 

<span data-ttu-id="68f8d-106">Ознакомьтесь [со статьей общие сведения о параметрах шифрования BitLocker и элементах шифрования диска BitLocker на панели управления](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) .</span><span class="sxs-lookup"><span data-stu-id="68f8d-106">See [Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) to read about:</span></span>

-   <span data-ttu-id="68f8d-107">Различия между MBAM и элементами панели управления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="68f8d-107">Differences between the MBAM and the default Control Panel items</span></span>

-   <span data-ttu-id="68f8d-108">**Управление** контекстным меню BitLocker, которое появляется при щелчке диска правой кнопкой мыши в проводнике Windows</span><span class="sxs-lookup"><span data-stu-id="68f8d-108">**Manage BitLocker** shortcut menu that appears when you right-click a drive in Windows Explorer</span></span>

<span data-ttu-id="68f8d-109">**Важно!**  Не изменяйте параметры групповой политики в узле **шифрования диска BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="68f8d-109">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node.</span></span> <span data-ttu-id="68f8d-110">В противном случае MBAM не будет работать правильно.</span><span class="sxs-lookup"><span data-stu-id="68f8d-110">If you do, MBAM will not work correctly.</span></span> <span data-ttu-id="68f8d-111">При настройке параметров групповой политики на узле **MDOP MBAM (Управление BitLocker)** MBAM автоматически настраивает параметры **шифрования диска для BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="68f8d-111">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="68f8d-112">Скрытие элемента шифрования диска BitLocker по умолчанию на панели управления</span><span class="sxs-lookup"><span data-stu-id="68f8d-112">To hide the default BitLocker Drive Encryption item in Control Panel</span></span>**

1.  <span data-ttu-id="68f8d-113">В консоли управления групповыми политиками (GPMC) или в разделе Расширенное управление групповыми политиками перейдите к элементу политики **конфигурации пользователей** &gt; **Policies** &gt; **Administrative Templates** &gt; **панели управления**"Административные шаблоны".</span><span class="sxs-lookup"><span data-stu-id="68f8d-113">In the Group Policy Management Console (GPMC) or in Advanced Group Policy Management, browse to **User configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Control Panel**.</span></span>

2.  <span data-ttu-id="68f8d-114">В области **сведений** дважды щелкните **Скрыть указанные элементы панели управления**, а затем выберите пункт **включена**.</span><span class="sxs-lookup"><span data-stu-id="68f8d-114">In the **Details** pane, double-click **Hide specified Control Panel items**, and then click **Enabled**.</span></span>

3.  <span data-ttu-id="68f8d-115">Нажмите кнопку **Показать**, нажмите кнопку **Добавить**и введите **Microsoft. BitLockerDriveEncryption**.</span><span class="sxs-lookup"><span data-stu-id="68f8d-115">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span>



## <span data-ttu-id="68f8d-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="68f8d-116">Related topics</span></span>


[<span data-ttu-id="68f8d-117">Общие сведения о параметрах шифрования BitLocker и шифровании дисков BitLocker в панели управления</span><span class="sxs-lookup"><span data-stu-id="68f8d-117">Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel</span></span>](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[<span data-ttu-id="68f8d-118">Развертывание объектов групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="68f8d-118">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)

 

## <span data-ttu-id="68f8d-119">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="68f8d-119">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="68f8d-120">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="68f8d-120">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="68f8d-121">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="68f8d-121">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





