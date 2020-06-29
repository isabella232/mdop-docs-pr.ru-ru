---
title: Скрытие оснастки шифрования BitLocker по умолчанию в панели управления Windows
description: Скрытие оснастки шифрования BitLocker по умолчанию в панели управления Windows
author: dansimp
ms.assetid: 6674aa51-2b5d-4e4a-8b43-2cc18d008285
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eda8fafbd7b3ebf414520354eba6def2e97f6237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824082"
---
# <span data-ttu-id="72a1b-103">Скрытие оснастки шифрования BitLocker по умолчанию в панели управления Windows</span><span class="sxs-lookup"><span data-stu-id="72a1b-103">How to Hide Default BitLocker Encryption in the Windows Control Panel</span></span>


<span data-ttu-id="72a1b-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) включает в себя настроенную панель управления для администрирования Microsoft BitLocker и наблюдения за клиентскими компьютерами, которые называются параметрами шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="72a1b-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for Microsoft BitLocker Administration and Monitoring client computers, called BitLocker Encryption Options.</span></span> <span data-ttu-id="72a1b-105">Эта настраиваемая панель управления может заменить стандартную панель управления Windows BitLocker, которая называется шифрованием диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="72a1b-105">This customized control panel can replace the default Windows BitLocker control panel, which is called BitLocker Drive Encryption.</span></span> <span data-ttu-id="72a1b-106">Настраиваемая панель управления, которая находится в панели управления в разделе система и безопасность, позволяет пользователям управлять их PIN-кодом и паролями, а также скрывать интерфейс, позволяющий администраторам расшифровывать диски и приостанавливать шифрование диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="72a1b-106">The customized control panel, which is in Control Panel under System and Security, enables users to manage their PIN and passwords and to unlock drives, and hides the interface that enables administrators to decrypt a drive or to suspend or resume BitLocker drive encryption.</span></span>

**<span data-ttu-id="72a1b-107">Скрытие шифрования диска BitLocker по умолчанию на панели управления Windows</span><span class="sxs-lookup"><span data-stu-id="72a1b-107">To hide default BitLocker drive encryption in Windows Control Panel</span></span>**

1.  <span data-ttu-id="72a1b-108">В консоли управления групповыми политиками (GPMC), расширенном управлении групповыми политиками или редактором локальной групповой политики на компьютере групповых политик BitLocker перейдите к элементу **Конфигурация пользователя**.</span><span class="sxs-lookup"><span data-stu-id="72a1b-108">In the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer, browse to **User configuration**.</span></span>

2.  <span data-ttu-id="72a1b-109">Затем выберите **политики**, выберите **Административные шаблоны**и щелкните **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="72a1b-109">Next, click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="72a1b-110">Дважды щелкните команду **Скрыть указанные элементы панели управления** в области **сведений** и выберите пункт **включена**.</span><span class="sxs-lookup"><span data-stu-id="72a1b-110">Double-click **Hide specified Control Panel items** in the **Details** pane, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="72a1b-111">Нажмите кнопку **Показать**, нажмите кнопку **Добавить**и введите **Microsoft. BitLockerDriveEncryption**.</span><span class="sxs-lookup"><span data-stu-id="72a1b-111">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span> <span data-ttu-id="72a1b-112">Эта политика скрывает средство управления Windows BitLocker по умолчанию с помощью панели управления Windows и, в панели управления, позволяет пользователю открывать обновленное средство MBAM шифрования BitLocker в разделе "система и безопасность".</span><span class="sxs-lookup"><span data-stu-id="72a1b-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and, in Control Panel, lets the user open the updated MBAM BitLocker Encryption Options tool under System and Security.</span></span>

## <span data-ttu-id="72a1b-113">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="72a1b-113">Related topics</span></span>


[<span data-ttu-id="72a1b-114">Развертывание объектов групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="72a1b-114">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





