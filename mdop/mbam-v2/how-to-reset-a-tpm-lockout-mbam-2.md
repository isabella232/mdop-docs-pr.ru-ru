---
title: Сброс блокировки доверенного платформенного модуля
description: Сброс блокировки доверенного платформенного модуля
author: dansimp
ms.assetid: 20719ab2-18ae-4d3b-989a-539341909816
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6453473ec09c2033346c7e464c08dbfdfe046d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825052"
---
# <span data-ttu-id="ed799-103">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="ed799-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="ed799-104">Функция восстановления зашифрованных дисков в Microsoft BitLocker Administration и Monitoring (MBAM) включает в себя захват и хранение данных и доступность средств, необходимых для управления доверенным платформенным модулем (TPM).</span><span class="sxs-lookup"><span data-stu-id="ed799-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are needed to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="ed799-105">В этой статье объясняется, как получить доступ к системе данных для восстановления централизованного ключа на веб-сайте администрирования и наблюдения, который может предоставить файл пароля владельца TPM при предоставлении идентификатора компьютера и соответствующего идентификатора пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed799-105">This topic covers how to access the centralized Key Recovery data system in the Administration and Monitoring website, which can provide a TPM owner password file when a computer ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="ed799-106">Блокировка доверенного платформенного модуля может возникнуть, если пользователь ввел неверный ПИН-код слишком много раз.</span><span class="sxs-lookup"><span data-stu-id="ed799-106">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="ed799-107">Количество случаев, когда пользователь может ввести неверный ПИН-код, прежде чем блокировки доверенного платформенного модуля будут различаться от производителя к изготовителю.</span><span class="sxs-lookup"><span data-stu-id="ed799-107">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="ed799-108">Вы можете сбросить блокировку доверенного платформенного модуля только в том случае, если MBAM владеет TPM.</span><span class="sxs-lookup"><span data-stu-id="ed799-108">You can reset a TPM lockout only if MBAM owns the TPM.</span></span>

**<span data-ttu-id="ed799-109">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="ed799-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="ed799-110">Откройте веб-браузер и перейдите на веб-сайт администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="ed799-110">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="ed799-111">В области навигации слева выберите **Управление TPM** , чтобы открыть страницу **Управление TPM** .</span><span class="sxs-lookup"><span data-stu-id="ed799-111">In the left navigation pane, select **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="ed799-112">Введите полное доменное имя компьютера и имя компьютера, а затем введите домен входа в Windows и имя пользователя, чтобы получить файл пароля владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="ed799-112">Enter the fully qualified domain name for the computer and the computer name, and enter the user’s Windows logon domain and the user’s user name to retrieve the TPM owner password file.</span></span>

4.  <span data-ttu-id="ed799-113">В списке **Причина для запроса пароля владельца доверенного платформенного модуля** выберите причину и нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="ed799-113">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="ed799-114">MBAM возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ed799-114">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="ed799-115">Сообщение об ошибке, если не удается найти соответствующий файл пароля владельца доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="ed799-115">An error message, if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="ed799-116">Файл пароля владельца доверенного платформенного модуля для отправленного компьютера</span><span class="sxs-lookup"><span data-stu-id="ed799-116">The TPM owner password file for the submitted computer</span></span>

    **<span data-ttu-id="ed799-117">Примечание.</span><span class="sxs-lookup"><span data-stu-id="ed799-117">Note</span></span>**  
    <span data-ttu-id="ed799-118">Если вы являетесь дополнительным пользователем службы поддержки, поля "домен пользователя" и "ИД пользователя" не требуются.</span><span class="sxs-lookup"><span data-stu-id="ed799-118">If you are an Advanced Helpdesk user, the user domain and user ID fields are not required.</span></span>



~~~
After the TPM owner password is retrieved, the owner password is displayed.
~~~

5. <span data-ttu-id="ed799-119">Чтобы сохранить пароль в файле. доверенный платформенный модуль, нажмите кнопку **сохранить** .</span><span class="sxs-lookup"><span data-stu-id="ed799-119">To save the password to a .tpm file, click the **Save** button.</span></span>

   <span data-ttu-id="ed799-120">Пользователь запустит консоль управления TPM, выберет параметр **сброса блокировки TPM** и предоставит файл пароля владельца доверенного платформенного модуля для сброса блокировки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="ed799-120">The user will run the TPM management console, select the **Reset TPM lockout** option, and provide the TPM owner password file to reset the TPM lockout.</span></span>

   **<span data-ttu-id="ed799-121">Важно.</span><span class="sxs-lookup"><span data-stu-id="ed799-121">Important</span></span>**  
   <span data-ttu-id="ed799-122">Администраторы службы поддержки не должны предоставлять конечным пользователям файл пароля доверенного платформенного модуля или владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="ed799-122">Help Desk administrators should not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="ed799-123">Данные доверенного платформенного модуля не изменяются, поэтому они могут представлять угрозу безопасности, если файл предоставлен конечным пользователям.</span><span class="sxs-lookup"><span data-stu-id="ed799-123">The TPM information does not change, so it could pose a security risk if the file is given to end users.</span></span>



## <span data-ttu-id="ed799-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ed799-124">Related topics</span></span>


[<span data-ttu-id="ed799-125">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="ed799-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









