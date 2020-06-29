---
title: Использование веб-сайта администрирования и мониторинга
description: Использование веб-сайта администрирования и мониторинга
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813045"
---
# <span data-ttu-id="813ec-103">Использование веб-сайта администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="813ec-103">How to Use the Administration and Monitoring Website</span></span>


<span data-ttu-id="813ec-104">Веб-сайт администрирования и наблюдения, также называемый службой поддержки, является интерфейсом администратора для шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="813ec-104">The Administration and Monitoring Website, also referred to as the Help Desk, is an administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="813ec-105">С помощью веб-сайта можно просматривать отчеты, восстанавливать диски конечных пользователей и управлять доверенными платформенными модулями, как описано в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="813ec-105">Use the website to review reports, recover end users’ drives, and manage end users’ TPMs, as described in the following sections.</span></span>

<span data-ttu-id="813ec-106">**Примечание**  Если вы используете MBAM в изолированной топологии, все отчеты будут просматриваться на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="813ec-106">**Note** If you are using MBAM in the Stand-alone topology, you view all reports from the Administration and Monitoring Website.</span></span> <span data-ttu-id="813ec-107">Если вы используете топологию интеграции Configuration Manager, вы будете просматривать все отчеты в Configuration Manager, за исключением отчета аудита восстановления, который вы продолжаете просматривать на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="813ec-107">If you are using the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit report, which you continue to view from the Administration and Monitoring Website.</span></span> <span data-ttu-id="813ec-108">Дополнительные сведения об отчетах можно найти [в разделе Наблюдение за соответствием и создание отчетов о соответствии BitLocker с помощью MBAM 2,5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="813ec-108">For more information about reports, see [Monitoring and Reporting BitLocker Compliance with MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).</span></span>

 

## <span data-ttu-id="813ec-109">Роли, необходимые для использования веб-сайта администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="813ec-109">Required roles for using the Administration and Monitoring Website</span></span>


<span data-ttu-id="813ec-110">Для доступа к определенным областям веб-сайта администрирования и мониторинга необходимо иметь одну из следующих ролей: группы, созданные в службе каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="813ec-110">To access specific areas of the Administration and Monitoring Website, you must have one of the following roles, which are groups that you create in Active Directory.</span></span> <span data-ttu-id="813ec-111">Вы можете использовать любое имя для этих групп.</span><span class="sxs-lookup"><span data-stu-id="813ec-111">You can use any name for these groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="813ec-112">Account</span><span class="sxs-lookup"><span data-stu-id="813ec-112">Account</span></span></th>
<th align="left"><span data-ttu-id="813ec-113">Описание</span><span class="sxs-lookup"><span data-stu-id="813ec-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="813ec-114">MBAM опытных пользователей службы поддержки</span><span class="sxs-lookup"><span data-stu-id="813ec-114">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="813ec-115">Предоставляет доступ ко всем областям веб-сайта администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="813ec-115">Provides access to all areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="813ec-116">Пользователи, которым назначена эта роль, вводят только ключ восстановления, а не домен и имя пользователя конечного пользователя, при помощи которых пользователи смогут восстановить свои диски.</span><span class="sxs-lookup"><span data-stu-id="813ec-116">Users who have this role enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="813ec-117">Если пользователь является членом обеих групп "Пользователи службы поддержки MBAM" и "Пользователи расширенной справочной службы", то разрешения группы "Пользователи расширенной справочной службы" переопределяют разрешения на доступ к группе "MBAM службы поддержки".</span><span class="sxs-lookup"><span data-stu-id="813ec-117">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users Group permissions.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="813ec-118">Пользователи службы поддержки MBAM</span><span class="sxs-lookup"><span data-stu-id="813ec-118">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="813ec-119">Предоставляет доступ к разделу Управление областями восстановления доверенных платформенных устройств и дисков на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="813ec-119">Provides access to the Manage TPM and Drive Recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="813ec-120">Пользователи, которым назначена эта роль, должны заполнить все поля, включая домен пользователя и имя учетной записи, если они используют любую область.</span><span class="sxs-lookup"><span data-stu-id="813ec-120">Individuals who have this role must fill in all fields, including the end-user’s domain and account name, when they use either area.</span></span></p>
<p><span data-ttu-id="813ec-121">Если пользователь является членом обеих групп "Пользователи службы поддержки MBAM" и "Пользователи расширенной справочной службы", то разрешения группы "Пользователи расширенной справочной службы" переопределяют разрешения на доступ к группе "MBAM службы поддержки".</span><span class="sxs-lookup"><span data-stu-id="813ec-121">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="813ec-122">Пользователи отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="813ec-122">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="813ec-123">Предоставляет доступ к отчетам в <strong> области "отчеты </strong> " на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="813ec-123">Provides access to the reports in the <strong>Reports</strong> area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="813ec-124">Задачи, которые можно выполнять на веб-сайте администрирования и наблюдения</span><span class="sxs-lookup"><span data-stu-id="813ec-124">Tasks you can perform on the Administration and Monitoring Website</span></span>


<span data-ttu-id="813ec-125">В следующей таблице перечислены задачи, которые можно выполнять на веб-сайте администрирования и наблюдения, а также приведены ссылки на дополнительные сведения о каждой задаче.</span><span class="sxs-lookup"><span data-stu-id="813ec-125">The following table summarizes the tasks you can perform on the Administration and Monitoring Website and provides links to more information about each task.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="813ec-126">Задача</span><span class="sxs-lookup"><span data-stu-id="813ec-126">Task</span></span></th>
<th align="left"><span data-ttu-id="813ec-127">Область веб-сайта, на котором можно получить доступ к задаче</span><span class="sxs-lookup"><span data-stu-id="813ec-127">Area of the Website where you access the task</span></span></th>
<th align="left"><span data-ttu-id="813ec-128">Описание</span><span class="sxs-lookup"><span data-stu-id="813ec-128">Description</span></span></th>
<th align="left"><span data-ttu-id="813ec-129">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="813ec-129">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="813ec-130">Просмотр отчетов.</span><span class="sxs-lookup"><span data-stu-id="813ec-130">View reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="813ec-131">Отчеты</span><span class="sxs-lookup"><span data-stu-id="813ec-131">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="813ec-132">Позволяет запускать отчеты для мониторинга использования BitLocker, соответствия требованиям и восстановления ключей.</span><span class="sxs-lookup"><span data-stu-id="813ec-132">Enables you to run reports to monitor BitLocker usage, compliance, and key recovery activity.</span></span> <span data-ttu-id="813ec-133">В отчетах содержатся данные о требованиях к корпоративному соотношении, отдельных компьютерах и о том, кто запросил ключи восстановления или пакет OwnerAuth доверенного платформенного модуля для определенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="813ec-133">Reports provide data about enterprise compliance, individual computers, and who requested recovery keys or the TPM OwnerAuth package for a specific computer.</span></span></p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)"><span data-ttu-id="813ec-134">Просмотр отчетов MBAM 2.5 для изолированной топологии</span><span class="sxs-lookup"><span data-stu-id="813ec-134">Viewing MBAM 2.5 Reports for the Stand-alone Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="813ec-135">Определение состояния шифрования BitLocker для потерянных или украденных компьютеров</span><span class="sxs-lookup"><span data-stu-id="813ec-135">Determine the BitLocker encryption status of lost or stolen computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="813ec-136">Отчеты</span><span class="sxs-lookup"><span data-stu-id="813ec-136">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="813ec-137">Определение того, был ли зашифрован том, если компьютер потерян или украден.</span><span class="sxs-lookup"><span data-stu-id="813ec-137">Determine if a volume was encrypted if the computer is lost or stolen.</span></span></p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)"><span data-ttu-id="813ec-138">Определение состояния шифрования BitLocker утерянных компьютеров</span><span class="sxs-lookup"><span data-stu-id="813ec-138">How to Determine BitLocker Encryption State of Lost Computers</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="813ec-139">Восстановление потерянных дисков</span><span class="sxs-lookup"><span data-stu-id="813ec-139">Recover lost drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="813ec-140">Восстановление диска</span><span class="sxs-lookup"><span data-stu-id="813ec-140">Drive Recovery</span></span></p></td>
<td align="left"><p><span data-ttu-id="813ec-141">Восстановите диски, указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="813ec-141">Recover drives that are:</span></span></p>
<ul>
<li><p><span data-ttu-id="813ec-142">В режиме восстановления</span><span class="sxs-lookup"><span data-stu-id="813ec-142">In recovery mode</span></span></p></li>
<li><p><span data-ttu-id="813ec-143">Были перемещены</span><span class="sxs-lookup"><span data-stu-id="813ec-143">Have been moved</span></span></p></li>
<li><p><span data-ttu-id="813ec-144">Повреждены</span><span class="sxs-lookup"><span data-stu-id="813ec-144">Are corrupted</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)"><span data-ttu-id="813ec-145">Восстановление диска в режиме восстановления</span><span class="sxs-lookup"><span data-stu-id="813ec-145">How to Recover a Drive in Recovery Mode</span></span></a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)"><span data-ttu-id="813ec-146">Восстановление перемещенного диска</span><span class="sxs-lookup"><span data-stu-id="813ec-146">How to Recover a Moved Drive</span></span></a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)"><span data-ttu-id="813ec-147">Восстановление поврежденного диска</span><span class="sxs-lookup"><span data-stu-id="813ec-147">How to Recover a Corrupted Drive</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="813ec-148">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="813ec-148">Reset a TPM lockout</span></span></p></td>
<td align="left"><p><span data-ttu-id="813ec-149">Управление TPM</span><span class="sxs-lookup"><span data-stu-id="813ec-149">Manage TPM</span></span></p></td>
<td align="left"><p><span data-ttu-id="813ec-150">Предоставляет доступ к данным доверенного платформенного модуля, собранные клиентом MBAM.</span><span class="sxs-lookup"><span data-stu-id="813ec-150">Provides access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="813ec-151">В случае блокировки доверенного платформенного модуля с помощью веб-сайта администрирования и наблюдения извлеките необходимый файл пароля, чтобы разблокировать доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="813ec-151">In a TPM lockout, use the Administration and Monitoring Website to retrieve the necessary password file to unlock the TPM.</span></span></p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)"><span data-ttu-id="813ec-152">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="813ec-152">How to Reset a TPM Lockout</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="813ec-153">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="813ec-153">Related topics</span></span>


[<span data-ttu-id="813ec-154">Управление BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="813ec-154">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="813ec-155">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="813ec-155">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="813ec-156">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="813ec-156">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="813ec-157">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="813ec-157">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





