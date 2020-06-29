---
title: Восстановление диска в режиме восстановления
description: Восстановление диска в режиме восстановления
author: dansimp
ms.assetid: 8b792bc8-b671-4345-9d37-0208db3e5b03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d5ce509599d0eb800a71360e3be9d0fa3b33f4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825059"
---
# <span data-ttu-id="563c4-103">Восстановление диска в режиме восстановления</span><span class="sxs-lookup"><span data-stu-id="563c4-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="563c4-104">Возможности восстановления зашифрованных дисков в Microsoft BitLocker: Администрирование и мониторинг (MBAM) обеспечивают сбор и хранение данных и доступность средств, необходимых для доступа к тому, защищенному BitLocker, при переходе BitLocker в режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="563c4-104">The encrypted drive recovery features of Microsoft BitLocker Administration and Monitoring (MBAM) ensure the capture and storage of data and availability of tools required to access a BitLocker-protected volume when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="563c4-105">Защищенный BitLocker том переходит в режим восстановления при утере или закрытии PIN-кода или пароля, а также при обнаружении изменений в BIOS или на загрузочном файле компьютера.</span><span class="sxs-lookup"><span data-stu-id="563c4-105">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="563c4-106">Используйте эту процедуру, чтобы получить доступ к системе данных для восстановления централизованного ключа, которая может предоставить пароль восстановления, если указаны идентификатор пароля восстановления и соответствующий идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="563c4-106">Use this procedure to access the centralized key recovery data system, which can provide a recovery password if a recovery password ID and associated user identifier are supplied.</span></span>

**<span data-ttu-id="563c4-107">Важно.</span><span class="sxs-lookup"><span data-stu-id="563c4-107">Important</span></span>**  
<span data-ttu-id="563c4-108">Администрирование и мониторинг Microsoft BitLocker использует одноразовые ключи восстановления, срок действия которых истекает.</span><span class="sxs-lookup"><span data-stu-id="563c4-108">Microsoft BitLocker Administration and Monitoring uses single-use recovery keys that expire upon use.</span></span> <span data-ttu-id="563c4-109">Один из способов использования пароля восстановления автоматически применяется к дискам операционной системы и жестким дискам.</span><span class="sxs-lookup"><span data-stu-id="563c4-109">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="563c4-110">На съемных носителях этот диск применяется при удалении и повторном добавлении и разблокировке на компьютере, на котором активированы параметры групповой политики для управления съемными дисками.</span><span class="sxs-lookup"><span data-stu-id="563c4-110">On removable drives, it is applied when the drive is removed and then re-inserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="563c4-111">Восстановление диска в режиме восстановления</span><span class="sxs-lookup"><span data-stu-id="563c4-111">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="563c4-112">Откройте веб-браузер и перейдите на веб-сайт администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="563c4-112">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="563c4-113">В области навигации нажмите кнопку **Восстановление диска**.</span><span class="sxs-lookup"><span data-stu-id="563c4-113">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="563c4-114">Откроется веб-страница "восстановление доступа к зашифрованному диску".</span><span class="sxs-lookup"><span data-stu-id="563c4-114">The “Recover access to an encrypted drive” webpage opens.</span></span>

3.  <span data-ttu-id="563c4-115">Введите домен входа Windows и имя пользователя пользователя, чтобы просмотреть сведения о восстановлении, и первые восемь цифр идентификатора ключа восстановления, чтобы получить список возможных совпадающих ключей восстановления или весь ИД ключа восстановления для получения точного ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="563c4-115">Enter the Windows Logon domain and user name of the user to view recovery information and the first eight digits of the recovery key ID to receive a list of possible matching recovery keys or the entire recovery key ID to receive the exact recovery key.</span></span>

4.  <span data-ttu-id="563c4-116">Выберите один из предопределенных вариантов из списка **Причина разблокировки диска** , а затем нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="563c4-116">Select one of the predefined options from the **Reason for Drive Unlock** list, and then click **Submit**.</span></span>

    **<span data-ttu-id="563c4-117">Примечание.</span><span class="sxs-lookup"><span data-stu-id="563c4-117">Note</span></span>**  
    <span data-ttu-id="563c4-118">Если вы являетесь пользователем расширенной службы поддержки MBAM, то не требуется домен пользователя и идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="563c4-118">If you are an MBAM Advanced Helpdesk user, the user domain and user ID entries are not required.</span></span>



~~~
MBAM returns the following:

-   An error message if no matching recovery password is found

-   Multiple possible matches if the user has multiple matching recovery passwords

-   The recovery password and recovery package for the submitted user

    **Note**  
    If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.



After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

5. <span data-ttu-id="563c4-119">Чтобы скопировать пароль, нажмите кнопку **Копировать ключ**и вставьте пароль восстановления в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="563c4-119">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="563c4-120">Вы также можете нажать кнопку **сохранить** , чтобы сохранить пароль восстановления в файле.</span><span class="sxs-lookup"><span data-stu-id="563c4-120">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="563c4-121">Когда пользователь вводит пароль восстановления в систему или использует пакет восстановления, диск разблокируется.</span><span class="sxs-lookup"><span data-stu-id="563c4-121">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="563c4-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="563c4-122">Related topics</span></span>


[<span data-ttu-id="563c4-123">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="563c4-123">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









