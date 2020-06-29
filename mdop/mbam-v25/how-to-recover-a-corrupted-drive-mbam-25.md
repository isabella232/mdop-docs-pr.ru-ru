---
title: Восстановление поврежденного диска
description: Восстановление поврежденного диска
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822552"
---
# <span data-ttu-id="5a5d1-103">Восстановление поврежденного диска</span><span class="sxs-lookup"><span data-stu-id="5a5d1-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="5a5d1-104">Эту процедуру можно использовать с веб-сайтом администрирования и мониторинга (также называемым веб-службой поддержки) для восстановления поврежденного диска, защищенного с помощью BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-104">You can use this procedure with the Administration and Monitoring Website (also referred to as the Help Desk) Website to recover a corrupted drive that is protected by BitLocker.</span></span> <span data-ttu-id="5a5d1-105">Для этого вам предстоит выполнить задачи, описанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-105">To do this, you will complete the tasks outlined in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a5d1-106">Задача</span><span class="sxs-lookup"><span data-stu-id="5a5d1-106">Task</span></span></th>
<th align="left"><span data-ttu-id="5a5d1-107">Сведения и дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="5a5d1-107">Details and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a5d1-108">Создайте файл пакета ключей восстановления, выполнив доступ к <strong> области восстановления диска </strong> на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-108">Create a recovery key package file by accessing the <strong>Drive Recovery</strong> area of the Administration and Monitoring Website.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a5d1-109">Для доступа к <strong> области восстановления диска </strong> необходимо назначить роль "Пользователи службы поддержки MBAM" или "Пользователи расширенной справочной службы" MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-109">To access the <strong>Drive Recovery</strong> area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="5a5d1-110">Возможно, вы предоставили эти роли имена при их создании.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-110">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="5a5d1-111">Дополнительные сведения можно найти в разделе <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> планирование для групп MBAM 2,5 и учетных записей </a> .</span><span class="sxs-lookup"><span data-stu-id="5a5d1-111">For more information, see <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)">Planning for MBAM 2.5 Groups and Accounts</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a5d1-112">Скопируйте файл пакета на компьютер, на котором находится поврежденный диск.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-112">Copy the package file to the computer that contains the corrupted drive.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a5d1-113"><code>repair-bde</code>Для завершения процесса восстановления используйте команду.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-113">Use the <code>repair-bde</code> command to complete the recovery process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a5d1-114">Чтобы избежать возможной потери данных, настоятельно рекомендуется проанализировать <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> команду Manage-bde </a> перед ее использованием.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-114">To avoid a potential loss of data, it is strongly recommended that you review the <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)">Manage-bde</a> command before using it.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="5a5d1-115">Восстановление поврежденного диска</span><span class="sxs-lookup"><span data-stu-id="5a5d1-115">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="5a5d1-116">Откройте веб-браузер и перейдите на **веб-сайт администрирования и мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="5a5d1-117">На левой панели выберите **Восстановление диска** , чтобы открыть страницу **Восстановление доступа к зашифрованному диску** .</span><span class="sxs-lookup"><span data-stu-id="5a5d1-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="5a5d1-118">Введите домен и имя пользователя для входа в Windows для конечного пользователя, причины разблокировки диска и идентификатора пароля восстановления для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-118">Enter the end user’s Windows log-on domain and user name, the reason for unlocking the drive, and the end user’s recovery password ID.</span></span>

    <span data-ttu-id="5a5d1-119">**Примечание**  Если вы являетесь членом группы расширенного доступа пользователей службы поддержки, вам не нужно вводить доменное имя пользователя или имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-119">**Note** If you are a member of the Advanced Helpdesk Users access group, you do not have to enter the user’s domain name or user name.</span></span>

     

4.  <span data-ttu-id="5a5d1-120">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-120">Click **Submit**.</span></span> <span data-ttu-id="5a5d1-121">Появится ключ восстановления.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-121">The recovery key will be displayed.</span></span>

5.  <span data-ttu-id="5a5d1-122">Нажмите кнопку **сохранить**, а затем выберите **пакет ключей восстановления**.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-122">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="5a5d1-123">Пакет ключа восстановления будет создан на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-123">The recovery key package will be created on your computer.</span></span>

6.  <span data-ttu-id="5a5d1-124">Скопируйте пакет ключа восстановления на компьютер с поврежденным диском.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-124">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

7.  <span data-ttu-id="5a5d1-125">Откройте командную строку с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-125">Open an elevated command prompt.</span></span> <span data-ttu-id="5a5d1-126">Для этого нажмите кнопку **Пуск** и введите `cmd` текст в поле **Найти программы и файлы** .</span><span class="sxs-lookup"><span data-stu-id="5a5d1-126">To do this, click **Start** and type `cmd` in the **Search programs and files** text box.</span></span> <span data-ttu-id="5a5d1-127">Щелкните **cmd.exe**правой кнопкой мыши и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-127">Right-click **cmd.exe**, and select **Run as Administrator**.</span></span>

8.  <span data-ttu-id="5a5d1-128">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5a5d1-128">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="5a5d1-129">**Примечание**  Замените &lt; *фиксированный диск* &gt; на свободный диск, на котором свободно больше или превышает объем данных на поврежденном диске.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-129">**Note** Replace &lt;*fixed drive*&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="5a5d1-130">Данные поврежденного диска будут восстановлены и перемещены на указанный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-130">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     


## <span data-ttu-id="5a5d1-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5a5d1-131">Related topics</span></span>


[<span data-ttu-id="5a5d1-132">Управление BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5a5d1-132">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="5a5d1-133">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="5a5d1-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5a5d1-134">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="5a5d1-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5a5d1-135">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5a5d1-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





