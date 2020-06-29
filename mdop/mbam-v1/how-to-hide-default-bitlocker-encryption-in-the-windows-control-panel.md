---
title: Скрытие оснастки шифрования BitLocker по умолчанию в панели управления Windows
description: Скрытие оснастки шифрования BitLocker по умолчанию в панели управления Windows
author: dansimp
ms.assetid: c8503743-220c-497c-9785-e2feeca484d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67a61763e556f8c3b93825220dbbd61a14b7d6f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824509"
---
# <span data-ttu-id="70285-103">Скрытие оснастки шифрования BitLocker по умолчанию в панели управления Windows</span><span class="sxs-lookup"><span data-stu-id="70285-103">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>


<span data-ttu-id="70285-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) включает настроенную панель управления для клиентских компьютеров MBAM с именем, именуемым параметрами шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="70285-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for MBAM client computers that is named called BitLocker Encryption Options.</span></span> <span data-ttu-id="70285-105">Эта настраиваемая панель управления может заменить стандартную панель управления Windows BitLocker, которая называется шифрованием диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="70285-105">This customized control panel can replace the default Windows BitLocker control panel that is named BitLocker Drive Encryption.</span></span> <span data-ttu-id="70285-106">Панель управления "параметры шифрования BitLocker", расположенная в разделе "система и безопасность" в панели управления Windows, позволяет пользователям управлять их ПИН-кодом и паролями, разблокируя диски и скрывает интерфейс, позволяющий администраторам расшифровывать диск, а также приостанавливать шифрование BitLocker и возобновлять его.</span><span class="sxs-lookup"><span data-stu-id="70285-106">The BitLocker Encryption Options control panel, located under System and Security in the Windows control panel, enables users to manage their PIN and passwords, unlock drives, and hides the interface that allows administrators to decrypt a drive or to suspend or resume BitLocker encryption.</span></span>

**<span data-ttu-id="70285-107">Скрытие шифрования BitLocker по умолчанию на панели управления Windows</span><span class="sxs-lookup"><span data-stu-id="70285-107">To hide default BitLocker Encryption in the Windows Control Panel</span></span>**

1.  <span data-ttu-id="70285-108">Перейдите к странице **Конфигурация пользователя** с помощью консоли управления групповыми политиками (GPMC), расширенного управления групповыми политиками или редактора локальной групповой политики на компьютере групповой политики BitLocker.</span><span class="sxs-lookup"><span data-stu-id="70285-108">Browse to **User configuration** by using the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer.</span></span>

2.  <span data-ttu-id="70285-109">Нажмите **политики**, выберите **Административные шаблоны**и щелкните **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="70285-109">Click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="70285-110">В области **сведений** дважды щелкните **Скрыть указанные элементы панели управления**и выберите пункт **включена**.</span><span class="sxs-lookup"><span data-stu-id="70285-110">In the **Details** pane, double-click **Hide specified Control Panel items**, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="70285-111">Нажмите кнопку **Показать**, а затем **— кнопку Добавить...**, а затем введите Microsoft. BitLockerDriveEncryption.</span><span class="sxs-lookup"><span data-stu-id="70285-111">Click **Show**, **click Add…**, and then type Microsoft.BitLockerDriveEncryption.</span></span> <span data-ttu-id="70285-112">Эта политика скрывает средство управления Windows BitLocker по умолчанию с помощью панели управления Windows и позволяет пользователю открывать обновленные параметры шифрования BitLocker MBAM с помощью панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="70285-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and allows the user to open the updated MBAM BitLocker Encryption Options tool from the Windows Control Panel.</span></span>

## <span data-ttu-id="70285-113">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="70285-113">Related topics</span></span>


[<span data-ttu-id="70285-114">Развертывание объектов групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="70285-114">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 





