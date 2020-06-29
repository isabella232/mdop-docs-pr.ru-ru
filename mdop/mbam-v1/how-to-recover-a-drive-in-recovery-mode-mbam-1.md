---
title: Восстановление диска в режиме восстановления
description: Восстановление диска в режиме восстановления
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812952"
---
# <span data-ttu-id="0fe17-103">Восстановление диска в режиме восстановления</span><span class="sxs-lookup"><span data-stu-id="0fe17-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="0fe17-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) включает возможности восстановления зашифрованных дисков.</span><span class="sxs-lookup"><span data-stu-id="0fe17-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes Encrypted Drive Recovery features.</span></span> <span data-ttu-id="0fe17-105">Эти функции гарантируют сбор и хранение данных и доступность средств, необходимых для доступа к тому, защищенному с помощью BitLocker, при появлении тома в режиме восстановления.</span><span class="sxs-lookup"><span data-stu-id="0fe17-105">These features ensure the capture and storage of data and availability of tools that are required to access a BitLocker-protected volume when BitLocker puts that volume into recovery mode.</span></span> <span data-ttu-id="0fe17-106">Защищенный BitLocker том переходит в режим восстановления, если ПИН-код или пароль утеряны или утрачены, или если микросхема доверенного платформенного модуля (TPM) обнаруживает изменение BIOS или файлов загрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="0fe17-106">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects a change to the computer's BIOS or startup files.</span></span>

<span data-ttu-id="0fe17-107">Используйте эту процедуру, чтобы получить доступ к централизованной системе данных восстановления ключей, которая может предоставить пароль восстановления при предоставлении идентификатора пароля восстановления и соответствующего идентификатора пользователя.</span><span class="sxs-lookup"><span data-stu-id="0fe17-107">Use this procedure to access the centralized Key Recovery data system that can provide a recovery password when a recovery password ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="0fe17-108">**Важно!**  MBAM создает ключи восстановления с одним использованием.</span><span class="sxs-lookup"><span data-stu-id="0fe17-108">**Important** MBAM generates single-use recovery keys.</span></span> <span data-ttu-id="0fe17-109">В рамках этого ограничения ключ восстановления можно использовать только один раз, и он больше не является действительным.</span><span class="sxs-lookup"><span data-stu-id="0fe17-109">Under this limitation, a recovery key can be used only once and then it is no longer valid.</span></span> <span data-ttu-id="0fe17-110">Один из способов использования пароля восстановления автоматически применяется к дискам операционной системы и жестким дискам.</span><span class="sxs-lookup"><span data-stu-id="0fe17-110">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="0fe17-111">На съемных носителях используется единая функция, когда диск удаляется, а затем снова вставляется и разблокируется на компьютере, на котором активированы параметры групповой политики для управления съемными дисками.</span><span class="sxs-lookup"><span data-stu-id="0fe17-111">On removable drives, the single use is applied when the drive is removed and then re-inserted and unlocked on a computer that has the group policy settings activated to manage removable drives.</span></span>

 

**<span data-ttu-id="0fe17-112">Восстановление диска в режиме восстановления</span><span class="sxs-lookup"><span data-stu-id="0fe17-112">To recover a drive in Recovery Mode</span></span>**

1.  <span data-ttu-id="0fe17-113">Откройте веб-сайт MBAM.</span><span class="sxs-lookup"><span data-stu-id="0fe17-113">Open the MBAM website.</span></span>

2.  <span data-ttu-id="0fe17-114">В области навигации нажмите кнопку **Восстановление диска**.</span><span class="sxs-lookup"><span data-stu-id="0fe17-114">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="0fe17-115">Откроется веб-страница **зашифрованного диска** с правом восстановления.</span><span class="sxs-lookup"><span data-stu-id="0fe17-115">The **Recover access to an encrypted drive** webpage opens.</span></span>

3.  <span data-ttu-id="0fe17-116">Чтобы получить список возможных ключей восстановления, введите имя пользователя и домен для входа в Windows и первые восемь цифр идентификатора ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="0fe17-116">Enter the user's Windows Logon domain and user name and the first eight digits of the recovery key ID, to receive a list of possible matching recovery keys.</span></span> <span data-ttu-id="0fe17-117">Кроме того, можно ввести весь код ключа восстановления, чтобы получить точный ключ восстановления.</span><span class="sxs-lookup"><span data-stu-id="0fe17-117">Alternatively, enter the entire recovery key ID to receive the exact recovery key.</span></span> <span data-ttu-id="0fe17-118">Выберите один из предопределенных параметров из раскрывающегося списка **Причина для разблокировки диска** и нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="0fe17-118">Select one of the predefined options in the **Reason for Drive Unlock** drop-down list, and then click **Submit**.</span></span>

    <span data-ttu-id="0fe17-119">**Примечание**  Если вы являетесь пользователем расширенной службы поддержки MBAM, то не требуется домен пользователя и идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="0fe17-119">**Note** If you are an MBAM Advanced Helpdesk User, the user domain and user ID entries are not required.</span></span>

     

4.  <span data-ttu-id="0fe17-120">MBAM возвращает следующее:</span><span class="sxs-lookup"><span data-stu-id="0fe17-120">MBAM returns the following:</span></span>

    1.  <span data-ttu-id="0fe17-121">Сообщение об ошибке, если соответствующий пароль для восстановления не найден</span><span class="sxs-lookup"><span data-stu-id="0fe17-121">An error message if no matching recovery password is found</span></span>

    2.  <span data-ttu-id="0fe17-122">Несколько возможных совпадений, если у пользователя есть несколько совпадающих паролей восстановления</span><span class="sxs-lookup"><span data-stu-id="0fe17-122">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    3.  <span data-ttu-id="0fe17-123">Пароль восстановления и пакет восстановления для отправленного пользователя</span><span class="sxs-lookup"><span data-stu-id="0fe17-123">The recovery password and recovery package for the submitted user</span></span>

        <span data-ttu-id="0fe17-124">**Примечание**  Если вы восстанавливаете поврежденный диск, параметр пакета восстановления предоставляет BitLocker важные сведения, необходимые для восстановления.</span><span class="sxs-lookup"><span data-stu-id="0fe17-124">**Note** If you are recovering a damaged drive, the recovery package option provides BitLocker with the critical information necessary to attempt the recovery.</span></span>

         

5.  <span data-ttu-id="0fe17-125">После извлечения пароля восстановления и пакета восстановления отображается пароль восстановления.</span><span class="sxs-lookup"><span data-stu-id="0fe17-125">After the recovery password and recovery package are retrieved, the recovery password is displayed.</span></span> <span data-ttu-id="0fe17-126">Чтобы скопировать пароль, нажмите кнопку **Копировать раздел**, а затем вставьте пароль восстановления в сообщение электронной почты или другой текстовый файл для временного хранилища.</span><span class="sxs-lookup"><span data-stu-id="0fe17-126">To copy the password, click **Copy Key**, and then paste the recovery password into an email or other text file for temporary storage.</span></span> <span data-ttu-id="0fe17-127">Чтобы сохранить пароль восстановления в файле, нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0fe17-127">Or, to save the recovery password to a file, click **Save**.</span></span>

6.  <span data-ttu-id="0fe17-128">Когда пользователь вводит пароль восстановления в систему или использует пакет восстановления, диск разблокируется.</span><span class="sxs-lookup"><span data-stu-id="0fe17-128">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="0fe17-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0fe17-129">Related topics</span></span>


[<span data-ttu-id="0fe17-130">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="0fe17-130">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





