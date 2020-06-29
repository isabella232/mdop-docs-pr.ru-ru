---
title: Сброс блокировки доверенного платформенного модуля
description: Сброс блокировки доверенного платформенного модуля
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823322"
---
# <span data-ttu-id="ea39f-103">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="ea39f-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="ea39f-104">В этой статье объясняется, как использовать веб-сайт администрирования и наблюдения (также называемый службой поддержки) для сброса блокировки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="ea39f-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to reset a TPM lockout.</span></span> <span data-ttu-id="ea39f-105">Блокировка доверенного платформенного модуля может возникнуть в том случае, если конечный пользователь ввел неверный ПИН-код слишком много раз.</span><span class="sxs-lookup"><span data-stu-id="ea39f-105">TPM lockouts can occur if an end user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="ea39f-106">Количество случаев, когда пользователь может ввести неверный ПИН-код, прежде чем блокировки доверенного платформенного модуля будут различаться от производителя к изготовителю.</span><span class="sxs-lookup"><span data-stu-id="ea39f-106">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="ea39f-107">В области **Управление доверенными платформенными модулями** на веб-сайте администрирования и мониторинга вы можете получить доступ к системе данных для восстановления с помощью централизованного ключа, которая предоставляет файл пароля владельца доверенного платформенного модуля при указании идентификатора компьютера и связанного идентификатора пользователя.</span><span class="sxs-lookup"><span data-stu-id="ea39f-107">From the **Manage TPM** area of the Administration and Monitoring Website, you can access the centralized Key Recovery data system, which provides a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

<span data-ttu-id="ea39f-108">Для доступа к области Управление доверенным платформенным модулем на веб-сайте администрирования и мониторинга необходимо назначить роль "Пользователи службы поддержки MBAM" или "Пользователи расширенной справочной службы" MBAM.</span><span class="sxs-lookup"><span data-stu-id="ea39f-108">To access the Manage TPM area of the Administration and Monitoring Website, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="ea39f-109">Эти роли — это группы, которые администраторы создают в службе каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea39f-109">These roles are groups that administrators create in Active Directory.</span></span> <span data-ttu-id="ea39f-110">Вы можете использовать любое имя для этих групп.</span><span class="sxs-lookup"><span data-stu-id="ea39f-110">You can use any name for these groups.</span></span> <span data-ttu-id="ea39f-111">Дополнительные сведения можно найти в разделе [планирование для групп MBAM 2,5 и учетных записей](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="ea39f-111">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="ea39f-112">Сведения о владении MBAM и TPM можно найти в разделе [рекомендации по безопасности в MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).</span><span class="sxs-lookup"><span data-stu-id="ea39f-112">For information about MBAM and TPM ownership, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm).</span></span>

**<span data-ttu-id="ea39f-113">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="ea39f-113">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="ea39f-114">Откройте веб-браузер и перейдите на **веб-сайт администрирования и мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="ea39f-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="ea39f-115">В левой области щелкните **Управление доверенным платформенным модулем** , чтобы открыть страницу **Управление TPM** .</span><span class="sxs-lookup"><span data-stu-id="ea39f-115">In the left pane, click **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="ea39f-116">Введите полное доменное имя компьютера и имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="ea39f-116">Enter the fully qualified domain name for the computer and the computer name.</span></span>

4.  <span data-ttu-id="ea39f-117">Введите имя пользователя и домен для входа в Windows для конечного пользователя, чтобы получить файл пароля владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="ea39f-117">Enter the end user’s Windows log-on domain and user name to retrieve the TPM owner password file.</span></span>

    <span data-ttu-id="ea39f-118">**Примечание**  Если вы используете группу пользователей расширенной поддержки MBAM, домен пользователя и поле идентификатора пользователя не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="ea39f-118">**Note** If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="ea39f-119">В списке **Причина для запроса пароля владельца доверенного платформенного модуля** выберите причину и нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="ea39f-119">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="ea39f-120">MBAM возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ea39f-120">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="ea39f-121">Сообщение об ошибке, если не удается найти соответствующий файл пароля владельца доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="ea39f-121">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="ea39f-122">Файл пароля владельца доверенного платформенного модуля для отправленного компьютера</span><span class="sxs-lookup"><span data-stu-id="ea39f-122">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="ea39f-123">После извлечения пароля владельца доверенного платформенного модуля отображается пароль владельца.</span><span class="sxs-lookup"><span data-stu-id="ea39f-123">After the TPM owner password is retrieved, the owner password is displayed.</span></span>

6.  <span data-ttu-id="ea39f-124">Чтобы сохранить пароль в файле. доверенный платформенный модуль, нажмите кнопку **сохранить** .</span><span class="sxs-lookup"><span data-stu-id="ea39f-124">To save the password to a .tpm file, click the **Save** button.</span></span>

7.  <span data-ttu-id="ea39f-125">В области **Управление доверенными платформенными модулями** на **веб-сайте администрирования и мониторинга**выберите параметр **сбросить блокировки доверенного платформенного** модуля и укажите файл пароля владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="ea39f-125">In the **Manage TPM** area of the **Administration and Monitoring Website**, select the **Reset TPM lockout** option and provide the TPM owner password file.</span></span>

    <span data-ttu-id="ea39f-126">Блокировка доверенного платформенного модуля сбрасывается и восстанавливается доступ конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="ea39f-126">The TPM lockout is reset and the end user’s access is restored.</span></span>

    <span data-ttu-id="ea39f-127">**Важно!**  Не выдавайте для конечных пользователей хэш-значения доверенного платформенного модуля или владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="ea39f-127">**Important** Do not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="ea39f-128">Поскольку данные доверенного платформенного модуля не изменяются, предоставление доступа к файлу для конечных пользователей создает угрозу безопасности.</span><span class="sxs-lookup"><span data-stu-id="ea39f-128">Because the TPM information does not change, giving the file to end users creates a security risk.</span></span>

     



## <span data-ttu-id="ea39f-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ea39f-129">Related topics</span></span>


[<span data-ttu-id="ea39f-130">Управление BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ea39f-130">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="ea39f-131">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="ea39f-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ea39f-132">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="ea39f-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ea39f-133">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ea39f-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





