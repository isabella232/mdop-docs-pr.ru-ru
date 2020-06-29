---
title: Восстановление перемещенного диска
description: Восстановление перемещенного диска
author: dansimp
ms.assetid: 0d38ce7e-bc64-473e-ae85-99b7099ca758
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 9e7e03846e0a94902b699377043237c651939a07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823342"
---
# <span data-ttu-id="452a8-103">Восстановление перемещенного диска</span><span class="sxs-lookup"><span data-stu-id="452a8-103">How to Recover a Moved Drive</span></span>
<span data-ttu-id="452a8-104">В этой статье объясняется, как использовать веб-сайт администрирования и наблюдения (также называемый службой поддержки) для восстановления диска операционной системы, который был перемещен после того, как он зашифрован службой Microsoft BitLocker Administration и мониторингом (MBAM).</span><span class="sxs-lookup"><span data-stu-id="452a8-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to recover an operating system drive that was moved after being encrypted by Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="452a8-105">При перемещении диска он больше не принимает PIN-код, который использовался на предыдущем компьютере, так как изменилась микросхема доверенного платформенного модуля (TPM).</span><span class="sxs-lookup"><span data-stu-id="452a8-105">When a drive is moved, it no longer accepts the PIN that was used in the previous computer because the Trusted Platform Module (TPM) chip has changed.</span></span> <span data-ttu-id="452a8-106">Чтобы восстановить перемещенный диск, необходимо получить ИД ключа восстановления, чтобы получить пароль восстановления.</span><span class="sxs-lookup"><span data-stu-id="452a8-106">To recover the moved drive, you must obtain the recovery key ID to retrieve the recovery password.</span></span>

<span data-ttu-id="452a8-107">Чтобы восстановить перемещенный диск, необходимо использовать область **восстановления диска** на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="452a8-107">To recover a moved drive, you must use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="452a8-108">Для доступа к области **восстановления диска** необходимо назначить роль "Пользователи службы поддержки MBAM" или "Пользователи расширенной справочной службы" MBAM.</span><span class="sxs-lookup"><span data-stu-id="452a8-108">To access the **Drive Recovery** area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="452a8-109">Дополнительные сведения об этих ролях можно найти в разделе [планирование для групп и учетных записей MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="452a8-109">For more information about these roles, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

**<span data-ttu-id="452a8-110">Восстановление перемещенного диска</span><span class="sxs-lookup"><span data-stu-id="452a8-110">To recover a moved drive</span></span>**
1.  <span data-ttu-id="452a8-111">На компьютере, содержащем перемещенный диск, запустите компьютер в режиме среды восстановления Windows (WinRE) или загрузите компьютер, используя набор средств диагностики и восстановления Microsoft (DaRT).</span><span class="sxs-lookup"><span data-stu-id="452a8-111">On the computer that contains the moved drive, start the computer in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="452a8-112">После того как компьютер будет запущен с помощью WinRE или DaRT, MBAM проведет диск операционной системы как фиксированный диск с данными.</span><span class="sxs-lookup"><span data-stu-id="452a8-112">After the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a fixed data drive.</span></span> <span data-ttu-id="452a8-113">В MBAM будет отображен идентификатор пароля восстановления устройства и запрос пароля восстановления.</span><span class="sxs-lookup"><span data-stu-id="452a8-113">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="452a8-114">**Примечание**  В некоторых случаях вы можете нажать кнопку " **забыли ПИН-код** в процессе запуска", а затем войти в режим восстановления для отображения идентификатора ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="452a8-114">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="452a8-115">С помощью идентификатора ключа восстановления извлеките пароль восстановления и разблокируйте диск на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="452a8-115">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring Website.</span></span> <span data-ttu-id="452a8-116">Инструкции можно найти [в разделе Восстановление диска в режиме восстановления](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="452a8-116">For instructions, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).</span></span>

    <span data-ttu-id="452a8-117">Если перемещенный диск был настроен на использование микросхемы TPM на исходном компьютере, выполните следующие дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="452a8-117">If the moved drive was configured to use a TPM chip on the original computer, complete the following additional steps.</span></span> <span data-ttu-id="452a8-118">В противном случае процесс восстановления завершится.</span><span class="sxs-lookup"><span data-stu-id="452a8-118">Otherwise, the recovery process is complete.</span></span>

4.  <span data-ttu-id="452a8-119">После разблокировки диска и завершения процесса запуска откройте командную запись в режиме WinRE и используйте `manage-bde` команду для расшифровки диска.</span><span class="sxs-lookup"><span data-stu-id="452a8-119">After unlocking the drive and completing the start process, open a command prompt in WinRE mode and use the `manage-bde` command to decrypt the drive.</span></span> <span data-ttu-id="452a8-120">С помощью этого инструмента можно удалить доверенный платформенный модуль и предохранитель PIN-кода без первоначальной микросхемы TPM.</span><span class="sxs-lookup"><span data-stu-id="452a8-120">Using this tool is the only way to remove the TPM plus the PIN protector without the original TPM chip.</span></span> <span data-ttu-id="452a8-121">Сведения о `manage-bde` команде можно найти в разделе [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).</span><span class="sxs-lookup"><span data-stu-id="452a8-121">For information about the `manage-bde` command, see [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).</span></span>

5.  <span data-ttu-id="452a8-122">Когда удаление завершится, запустите компьютер в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="452a8-122">When the removal is completed, start the computer normally.</span></span> <span data-ttu-id="452a8-123">Кроме того, агент MBAM будет принудительно применять политику для шифрования диска с помощью доверенного платформенного модуля и ПИН-кода нового компьютера.</span><span class="sxs-lookup"><span data-stu-id="452a8-123">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus the PIN.</span></span>



## <span data-ttu-id="452a8-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="452a8-124">Related topics</span></span>


[<span data-ttu-id="452a8-125">Управление BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="452a8-125">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="452a8-126">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="452a8-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="452a8-127">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="452a8-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="452a8-128">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="452a8-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





