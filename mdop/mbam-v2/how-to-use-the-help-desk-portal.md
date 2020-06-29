---
title: Использование портала службы поддержки
description: Использование портала службы поддержки
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826329"
---
# <span data-ttu-id="d8d84-103">Использование портала службы поддержки</span><span class="sxs-lookup"><span data-stu-id="d8d84-103">How to Use the Help Desk Portal</span></span>


<span data-ttu-id="d8d84-104">Веб-сайт администрирования и мониторинга MBAM, также называемый порталом службы поддержки, — это административный интерфейс для шифрования диска BitLocker, установленный как часть инфраструктуры сервера администрирования Microsoft BitLocker и мониторинга (MBAM).</span><span class="sxs-lookup"><span data-stu-id="d8d84-104">The MBAM Administration and Monitoring website, also referred to as the Help Desk Portal, is an administrative interface to BitLocker drive encryption that is installed as part of the Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure.</span></span> <span data-ttu-id="d8d84-105">В следующих разделах описано, как с помощью этого веб-сайта можно просматривать отчеты, восстанавливать диски конечных пользователей и управлять доверенными платформенными модулями конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d8d84-105">The following sections describe how you can use this website to review reports, recover end users’ drives, and manage end users’ TPMs.</span></span>

## <a href="" id="bkmk-reports"></a><span data-ttu-id="d8d84-106">Отчеты</span><span class="sxs-lookup"><span data-stu-id="d8d84-106">Reports</span></span>


<span data-ttu-id="d8d84-107">MBAM собирает данные из службы каталогов Active Directory и клиентских компьютеров, что позволяет запускать различные отчеты для мониторинга использования и соответствия требованиям BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d8d84-107">MBAM collects information from Active Directory and client computers, which enables you to run different reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="d8d84-108">С помощью раздела **отчеты** на веб-сайте администрирования и мониторинга вы можете создавать отчеты о соответствии требованиям предприятия, отдельных компьютерах и действиях по восстановлению ключей.</span><span class="sxs-lookup"><span data-stu-id="d8d84-108">Using the **Reports** section of the Administration and Monitoring website, you can generate reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="d8d84-109">Описание каждого отчета можно найти в разделе [Общие сведения о MBAM](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d8d84-109">For a description of each report, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

**<span data-ttu-id="d8d84-110">Получение доступа к отчетам</span><span class="sxs-lookup"><span data-stu-id="d8d84-110">To access reports</span></span>**

1.  <span data-ttu-id="d8d84-111">Откройте веб-браузер и перейдите на веб-сайт администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8d84-111">Open a web browser and navigate to the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="d8d84-112">В левой области выберите пункт **отчеты** .</span><span class="sxs-lookup"><span data-stu-id="d8d84-112">Select **Reports** in the left pane.</span></span>

3.  <span data-ttu-id="d8d84-113">В верхней строке меню выберите тип отчета, который вы хотите создать.</span><span class="sxs-lookup"><span data-stu-id="d8d84-113">From the top menu bar, select the report type you want to generate.</span></span> <span data-ttu-id="d8d84-114">Чтобы сохранить отчет, нажмите кнопку " **Экспорт** " в строке меню "отчеты".</span><span class="sxs-lookup"><span data-stu-id="d8d84-114">To save reports, click the **Export** button on the Reports menu bar.</span></span>

<span data-ttu-id="d8d84-115">Дополнительные сведения о том, как выполнять MBAM отчеты, приведены [в разделе Создание отчетов MBAM](how-to-generate-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d8d84-115">For additional information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

## <a href="" id="bkmk-drirec"></a><span data-ttu-id="d8d84-116">Восстановление диска</span><span class="sxs-lookup"><span data-stu-id="d8d84-116">Drive Recovery</span></span>


<span data-ttu-id="d8d84-117">Функция **восстановления дисков** на веб-сайте администрирования и мониторинга позволяет пользователям с определенными ролями администратора (например, пользователям службы технической поддержки) получать данные ключа восстановления, собранные клиентом MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8d84-117">The **Drive Recovery** feature of the Administration and Monitoring website allows users with specific administrator roles (for example, Help Desk Users) to access recovery key data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="d8d84-118">Эти данные можно использовать для доступа к диску, защищенному BitLocker, при переходе BitLocker в режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="d8d84-118">This data can be used to access a BitLocker-protected drive when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="d8d84-119">Инструкции по восстановлению диска, который находится в режиме восстановления, приведены в разделе [Восстановление диска в режиме восстановления](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d8d84-119">For instructions on how to recover a drive that is in recovery mode, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span></span>

<span data-ttu-id="d8d84-120">Вы также можете восстановить диски, которые были перемещены или повреждены.</span><span class="sxs-lookup"><span data-stu-id="d8d84-120">You can also recover drives that have been moved or that are corrupted:</span></span>

-   [<span data-ttu-id="d8d84-121">Восстановление перемещенного диска</span><span class="sxs-lookup"><span data-stu-id="d8d84-121">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="d8d84-122">Восстановление поврежденного диска</span><span class="sxs-lookup"><span data-stu-id="d8d84-122">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

<span data-ttu-id="d8d84-123">Дополнительные сведения о том, как восстановить защищенный BitLocker диск, можно найти [в разделе Выполнение управления BitLocker с помощью MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d8d84-123">For additional information about how to recover a BitLocker-protected drive, see [Performing BitLocker Management with MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).</span></span>

## <a href="" id="bkmk-manatpm"></a><span data-ttu-id="d8d84-124">Управление TPM</span><span class="sxs-lookup"><span data-stu-id="d8d84-124">Manage TPM</span></span>


<span data-ttu-id="d8d84-125">Функция управления TPM на веб-сайте администрирования и мониторинга позволяет пользователям с определенными ролями администратора (например, "Пользователи службы поддержки MBAM") получать доступ к данным доверенного платформенного модуля, собранным клиентом MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8d84-125">The Manage TPM feature of the Administration and Monitoring website gives users with certain administrator roles (for example, “MBAM Helpdesk Users”) access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="d8d84-126">В случае блокировки доверенного платформенного модуля администратор может использовать веб-сайт администрирования и наблюдения для извлечения необходимого файла пароля, чтобы разблокировать доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="d8d84-126">In a TPM lockout, an administrator can use the Administration and Monitoring website to retrieve the necessary password file to unlock the TPM.</span></span> <span data-ttu-id="d8d84-127">Инструкции по сбросу доверенного платформенного модуля после блокировки ДОВЕРЕНного платформенного модуля приведены [в разделе Сброс блокировки доверенного платформенного](how-to-reset-a-tpm-lockout-mbam-2.md)модуля.</span><span class="sxs-lookup"><span data-stu-id="d8d84-127">For instructions on how to reset a TPM after a TPM lockout, see [How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-2.md).</span></span>

## <a href="" id="bkmk-helpdesk"></a> <span data-ttu-id="d8d84-128">MBAM задач службы поддержки</span><span class="sxs-lookup"><span data-stu-id="d8d84-128">MBAM Help Desk Tasks</span></span>


<span data-ttu-id="d8d84-129">Вы можете использовать веб-сайт администрирования и наблюдения для множества административных задач, таких как управление оборудованием, защищенным с помощью BitLocker, восстановление дисков и запуск отчетов.</span><span class="sxs-lookup"><span data-stu-id="d8d84-129">You can use the Administration and Monitoring website for many administrative tasks, such as managing BitLocker-protected hardware, recovering drives, and running reports.</span></span> <span data-ttu-id="d8d84-130">По умолчанию URL-адрес сайта администрирования и мониторинга — http:// &lt; *MBAMAdministrationServername* &gt; , но его можно настроить в процессе установки.</span><span class="sxs-lookup"><span data-stu-id="d8d84-130">By default, the URL for the Administration and Monitoring website is http://&lt;*MBAMAdministrationServername*&gt;, although you can customize it during the installation process.</span></span>

<span data-ttu-id="d8d84-131">**Примечание**  Для доступа к различным функциям, предоставляемым веб-сайтом администрирования и наблюдения, необходимо иметь соответствующие роли, связанные с вашей учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="d8d84-131">**Note** To access the various features offered by the Administration and Monitoring website, you must have the appropriate roles associated with your user account.</span></span> <span data-ttu-id="d8d84-132">Дополнительные сведения о ролях пользователей можно найти в разделе [Управление ролями администратора MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d8d84-132">For more information about understanding user roles, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

 

<span data-ttu-id="d8d84-133">Ниже приведены ссылки на дополнительные сведения о задачах, которые можно выполнять с помощью веб-сайта администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="d8d84-133">Use the following links to find information about the tasks that you can perform by using the Administration and Monitoring website:</span></span>

-   [<span data-ttu-id="d8d84-134">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="d8d84-134">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [<span data-ttu-id="d8d84-135">Восстановление диска в режиме восстановления</span><span class="sxs-lookup"><span data-stu-id="d8d84-135">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [<span data-ttu-id="d8d84-136">Восстановление перемещенного диска</span><span class="sxs-lookup"><span data-stu-id="d8d84-136">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="d8d84-137">Восстановление поврежденного диска</span><span class="sxs-lookup"><span data-stu-id="d8d84-137">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [<span data-ttu-id="d8d84-138">Определение состояния шифрования BitLocker утерянных компьютеров</span><span class="sxs-lookup"><span data-stu-id="d8d84-138">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





