---
title: Восстановление диска в режиме восстановления
description: Восстановление диска в режиме восстановления
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823369"
---
# <span data-ttu-id="a4e17-103">Восстановление диска в режиме восстановления</span><span class="sxs-lookup"><span data-stu-id="a4e17-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="a4e17-104">В этой статье объясняется, как использовать веб-сайт администрирования и наблюдения (также называемый службой поддержки), чтобы получить пароль восстановления для конечных пользователей, если диск, защищенный BitLocker, перейдет в режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="a4e17-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to get a recovery password to give to end users if their BitLocker-protected drive goes into recovery mode.</span></span> <span data-ttu-id="a4e17-105">Диски переходят в режим восстановления, если пользователь теряет или забывает свой PIN-код или пароль или если микросхема доверенного платформенного модуля (TPM) обнаруживает изменения в BIOS и на загрузочном файле компьютера.</span><span class="sxs-lookup"><span data-stu-id="a4e17-105">Drives go into recovery mode if users lose or forget their PIN or password or if the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="a4e17-106">Чтобы получить пароль восстановления, используйте область **восстановления диска** на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="a4e17-106">To get a recovery password, use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="a4e17-107">Для доступа к этой области веб-сайта необходимо назначить роль "Пользователи службы поддержки MBAM" или "Пользователи расширенной справочной службы MBAM".</span><span class="sxs-lookup"><span data-stu-id="a4e17-107">You must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role to access this area of the website.</span></span>

**<span data-ttu-id="a4e17-108">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a4e17-108">Note</span></span>**  
<span data-ttu-id="a4e17-109">Возможно, вы предоставили эти роли имена при их создании.</span><span class="sxs-lookup"><span data-stu-id="a4e17-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="a4e17-110">Дополнительные сведения можно найти в разделе [планирование для групп MBAM 2,5 и учетных записей](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="a4e17-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>



**<span data-ttu-id="a4e17-111">Важно.</span><span class="sxs-lookup"><span data-stu-id="a4e17-111">Important</span></span>**  
<span data-ttu-id="a4e17-112">Срок действия паролей восстановления истекает после одного использования.</span><span class="sxs-lookup"><span data-stu-id="a4e17-112">Recovery passwords expire after a single use.</span></span> <span data-ttu-id="a4e17-113">На дисках операционной системы и несъемных дисках с данными правило однократного использования применяется автоматически.</span><span class="sxs-lookup"><span data-stu-id="a4e17-113">On operating system drives and fixed data drives, the single-use rule is applied automatically.</span></span> <span data-ttu-id="a4e17-114">На съемных носителях он применяется, когда диск удаляется, а затем снова вставляется и разблокируется на компьютере, на котором активированы параметры групповой политики для управления съемными дисками.</span><span class="sxs-lookup"><span data-stu-id="a4e17-114">On removable drives, it is applied when the drive is removed and then reinserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="a4e17-115">Восстановление диска в режиме восстановления</span><span class="sxs-lookup"><span data-stu-id="a4e17-115">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="a4e17-116">Откройте веб-браузер и перейдите на **веб-сайт администрирования и мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="a4e17-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="a4e17-117">На левой панели выберите **Восстановление диска** , чтобы открыть страницу **Восстановление доступа к зашифрованному диску** .</span><span class="sxs-lookup"><span data-stu-id="a4e17-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="a4e17-118">Чтобы просмотреть сведения о восстановлении, введите имя пользователя и домен для входа в Windows для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="a4e17-118">Enter the end user’s Windows log-on domain and user name to view recovery information.</span></span>

    **<span data-ttu-id="a4e17-119">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a4e17-119">Note</span></span>**  
    <span data-ttu-id="a4e17-120">Если вы используете группу пользователей расширенной поддержки MBAM, домен пользователя и поле идентификатора пользователя не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="a4e17-120">If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>



4.  <span data-ttu-id="a4e17-121">Введите первые восемь цифр идентификатора ключа восстановления, чтобы просмотреть список возможных совпадающих ключей восстановления, или введите полный ИД ключа восстановления, чтобы получить точный ключ восстановления.</span><span class="sxs-lookup"><span data-stu-id="a4e17-121">Enter the first eight digits of the recovery key ID to see a list of possible matching recovery keys, or enter the entire recovery key ID to get the exact recovery key.</span></span>

5.  <span data-ttu-id="a4e17-122">В списке **Причина разблокировки диска** выберите один из предопределенных параметров и нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="a4e17-122">From the **Reason for Drive Unlock** list, select one of the predefined options, and then click **Submit**.</span></span>

    <span data-ttu-id="a4e17-123">MBAM возвращает следующее:</span><span class="sxs-lookup"><span data-stu-id="a4e17-123">MBAM returns the following:</span></span>

    -   <span data-ttu-id="a4e17-124">Сообщение об ошибке, если соответствующий пароль для восстановления не найден</span><span class="sxs-lookup"><span data-stu-id="a4e17-124">An error message if no matching recovery password is found</span></span>

    -   <span data-ttu-id="a4e17-125">Несколько возможных совпадений, если у пользователя есть несколько совпадающих паролей восстановления</span><span class="sxs-lookup"><span data-stu-id="a4e17-125">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    -   <span data-ttu-id="a4e17-126">Пароль восстановления и пакет восстановления для отправленного пользователя</span><span class="sxs-lookup"><span data-stu-id="a4e17-126">The recovery password and recovery package for the submitted user</span></span>

        **<span data-ttu-id="a4e17-127">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a4e17-127">Note</span></span>**  
        <span data-ttu-id="a4e17-128">Если вы восстанавливаете поврежденный диск, параметр пакета восстановления предоставляет BitLocker важные сведения, необходимые для восстановления диска.</span><span class="sxs-lookup"><span data-stu-id="a4e17-128">If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.</span></span>



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. <span data-ttu-id="a4e17-129">Чтобы скопировать пароль, нажмите кнопку **Копировать ключ**и вставьте пароль восстановления в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a4e17-129">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="a4e17-130">Вы также можете нажать кнопку **сохранить** , чтобы сохранить пароль восстановления в файле.</span><span class="sxs-lookup"><span data-stu-id="a4e17-130">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="a4e17-131">Когда пользователь вводит пароль восстановления в систему или использует пакет восстановления, диск разблокируется.</span><span class="sxs-lookup"><span data-stu-id="a4e17-131">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>



## <span data-ttu-id="a4e17-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a4e17-132">Related topics</span></span>


[<span data-ttu-id="a4e17-133">Управление BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a4e17-133">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)



## <span data-ttu-id="a4e17-134">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="a4e17-134">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a4e17-135">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="a4e17-135">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a4e17-136">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a4e17-136">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





