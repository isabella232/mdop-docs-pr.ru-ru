---
title: Устранение неполадок AGPM
description: Устранение неполадок AGPM
author: dansimp
ms.assetid: bedcd817-beb2-47bf-aebd-e3923c4fd06f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b44612cb9e3737a8d8f3109f76b0c9325d183383
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820152"
---
# <span data-ttu-id="76099-103">Устранение неполадок AGPM</span><span class="sxs-lookup"><span data-stu-id="76099-103">Troubleshooting AGPM</span></span>


<span data-ttu-id="76099-104">В этом разделе перечислены распространенные проблемы, которые могут возникнуть при использовании расширенного управления групповыми политиками для управления объектами групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="76099-104">This section lists common issues that you may encounter when you use Advanced Group Policy Management (AGPM) to manage Group Policy Objects (GPOs).</span></span> <span data-ttu-id="76099-105">Для диагностики проблем, которых нет в списке, может быть полезно администратор РАСШИРЕНного управления правами (полный доступ) для использования функции ведения журнала и трассировки.</span><span class="sxs-lookup"><span data-stu-id="76099-105">To diagnose issues not listed here, it may be helpful for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="76099-106">Дополнительные сведения можно найти в разделе [Настройка ведения журнала и трассировки](configure-logging-and-tracing-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="76099-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md).</span></span>

**<span data-ttu-id="76099-107">Примечание.</span><span class="sxs-lookup"><span data-stu-id="76099-107">Note</span></span>**  
-   <span data-ttu-id="76099-108">Сведения о переходе к более ранней версии объекта групповой политики в случае возникновения проблем см. [в разделе откат к более ранней версии объекта групповой политики](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="76099-108">For information about rolling back to an earlier version of a GPO if there are problems, see [Roll Back to an Earlier Version of a GPO](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).</span></span>

-   <span data-ttu-id="76099-109">Сведения о том, как восстановить после аварии восстановление из резервной копии, можно найти в разделе [Восстановление архива из](restore-the-archive-from-a-backup-agpm40.md)резервной копии.</span><span class="sxs-lookup"><span data-stu-id="76099-109">For information about how to recover from a disaster by restoring the complete archive from a backup, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md).</span></span>

 

## <span data-ttu-id="76099-110">Какие неполадки возникают?</span><span class="sxs-lookup"><span data-stu-id="76099-110">What problems are you having?</span></span>


-   [<span data-ttu-id="76099-111">Не удается получить доступ к архиву</span><span class="sxs-lookup"><span data-stu-id="76099-111">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="76099-112">Состояние GPO меняется для разных администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="76099-112">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="76099-113">Не удается изменить соединение с сервером РАСШИРЕНного разрешения</span><span class="sxs-lookup"><span data-stu-id="76099-113">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="76099-114">Не удается изменить шаблон или представление по умолчанию, создать, изменить, переименовать, развернуть или удалить GPO</span><span class="sxs-lookup"><span data-stu-id="76099-114">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="76099-115">Я не могу использовать имя определенного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="76099-115">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="76099-116">Я не получаю уведомления по электронной почте для РАСШИРЕНного разгрузки</span><span class="sxs-lookup"><span data-stu-id="76099-116">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="76099-117">Я не могу использовать порт 4600 для службы РАСШИРЕНного использования.</span><span class="sxs-lookup"><span data-stu-id="76099-117">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="76099-118">Служба РАСШИРЕНного обслуживания не запускается</span><span class="sxs-lookup"><span data-stu-id="76099-118">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="76099-119">Установка программного обеспечения для групповой политики не может установить программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="76099-119">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

-   [<span data-ttu-id="76099-120">Произошла ошибка при восстановлении архива на новом сервере РАСШИРЕНного шаблона</span><span class="sxs-lookup"><span data-stu-id="76099-120">An error occurred when I restored the archive to a new AGPM Server</span></span>](#bkmk-error-on-restore)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="76099-121">Не удается получить доступ к архиву</span><span class="sxs-lookup"><span data-stu-id="76099-121">I am unable to access an archive</span></span>

-   <span data-ttu-id="76099-122">**Причина**: вы не выбрали правильный сервер и порт для архива.</span><span class="sxs-lookup"><span data-stu-id="76099-122">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="76099-123">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="76099-123">**Solution**:</span></span>

    -   <span data-ttu-id="76099-124">Если вы являетесь администратором РАСШИРЕНного разрешения: Ознакомьтесь с [Разстройкой подключения к серверам](configure-agpm-server-connections-agpm40.md)расширенного разрешения.</span><span class="sxs-lookup"><span data-stu-id="76099-124">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

    -   <span data-ttu-id="76099-125">Если вы не являетесь администратором РАСШИРЕНного разрешения, выполните запрос сведений о подключении для сервера РАСШИРЕНного администрирования с помощью администратора РАСШИРЕНного разрешения.</span><span class="sxs-lookup"><span data-stu-id="76099-125">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="76099-126">Посмотрите [, как настроить соединение с сервером расширенного конфигурирования](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="76099-126">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

-   <span data-ttu-id="76099-127">**Причина**: служба расширенного использования не запущена.</span><span class="sxs-lookup"><span data-stu-id="76099-127">**Cause**: The AGPM Service is not running.</span></span>

-   <span data-ttu-id="76099-128">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="76099-128">**Solution**:</span></span>

    -   <span data-ttu-id="76099-129">Если вы являетесь администратором РАСШИРЕНного разрешения, запустите службу РАСШИРЕНного администрирования.</span><span class="sxs-lookup"><span data-stu-id="76099-129">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="76099-130">Дополнительные сведения можно найти в разделе [Запуск и остановка службы расширенного](start-and-stop-the-agpm-service-agpm40.md)просмотра.</span><span class="sxs-lookup"><span data-stu-id="76099-130">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

    -   <span data-ttu-id="76099-131">Если вы не являетесь администратором РАСШИРЕНного разрешения, обратитесь за помощью к администратору РАСШИРЕНного администрирования.</span><span class="sxs-lookup"><span data-stu-id="76099-131">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="76099-132">Состояние GPO меняется для разных администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="76099-132">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="76099-133">**Причина**: различные администраторы групповой политики выбрали различные серверы расширенного доменных служб для одного и того же архива.</span><span class="sxs-lookup"><span data-stu-id="76099-133">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="76099-134">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="76099-134">**Solution**:</span></span>

    -   <span data-ttu-id="76099-135">Если вы являетесь администратором РАСШИРЕНного разрешения: Ознакомьтесь с [Разстройкой подключения к серверам](configure-agpm-server-connections-agpm40.md)расширенного разрешения.</span><span class="sxs-lookup"><span data-stu-id="76099-135">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

    -   <span data-ttu-id="76099-136">Если вы не являетесь администратором РАСШИРЕНного разрешения, выполните запрос сведений о подключении для сервера РАСШИРЕНного администрирования с помощью администратора РАСШИРЕНного разрешения.</span><span class="sxs-lookup"><span data-stu-id="76099-136">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="76099-137">Посмотрите [, как настроить соединение с сервером расширенного конфигурирования](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="76099-137">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="76099-138">Не удается изменить соединение с сервером РАСШИРЕНного разрешения</span><span class="sxs-lookup"><span data-stu-id="76099-138">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="76099-139">**Причина**: Если параметры на вкладке " **сервер расширенного управления групповыми политиками** " недоступны, сервер расширенного доступа к данным был централизованно настроен с помощью административного шаблона.</span><span class="sxs-lookup"><span data-stu-id="76099-139">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="76099-140">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="76099-140">**Solution**:</span></span>

    -   <span data-ttu-id="76099-141">Если вы являетесь администратором РАСШИРЕНного доступа к сети: Если параметры на вкладке **сервер расширенного** доступа к данным недоступны, ознакомьтесь с разделами [Настройка подключений сервера расширенного](configure-agpm-server-connections-agpm40.md)доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="76099-141">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

    -   <span data-ttu-id="76099-142">Если вы не являетесь администратором РАСШИРЕНного доступа: Если параметры на вкладке **сервер расширенного** доступа к сети недоступны, вам не нужно изменять сервер расширенного доступа.</span><span class="sxs-lookup"><span data-stu-id="76099-142">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="76099-143">Не удается изменить шаблон или представление по умолчанию, создать, изменить, переименовать, развернуть или удалить GPO</span><span class="sxs-lookup"><span data-stu-id="76099-143">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="76099-144">**Причина**: вам не назначена роль с разрешениями, необходимыми для выполнения задачи или задач.</span><span class="sxs-lookup"><span data-stu-id="76099-144">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="76099-145">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="76099-145">**Solution**:</span></span>

    -   <span data-ttu-id="76099-146">Если вы являетесь администратором РАСШИРЕНного доступа к сети: Ознакомьтесь с [Разпредставителем доступ на уровне домена к архиву](delegate-domain-level-access-to-the-archive-agpm40.md) и [Делегирование доступа к отдельному объекту групповой политики в архиве](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="76099-146">If you are an AGPM Administrator: See [Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm40.md) and [Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md).</span></span> <span data-ttu-id="76099-147">Разрешения РАСШИРЕНного доступа к доменным объектам будут каскадными из домена на все GPO в архиве.</span><span class="sxs-lookup"><span data-stu-id="76099-147">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="76099-148">Сведения о ролях, которые могут выполнять задачи, и о том, какие разрешения необходимы для выполнения задачи, можно найти в справке по этой задаче.</span><span class="sxs-lookup"><span data-stu-id="76099-148">For details about which roles can perform a task and which permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="76099-149">Если вы не являетесь администратором РАСШИРЕНного доступа и вам требуются дополнительные роли или разрешения: обратитесь за помощью к администратору РАСШИРЕНного администрирования.</span><span class="sxs-lookup"><span data-stu-id="76099-149">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="76099-150">Имейте в виду, что, если вы являетесь редактором, вы можете начать процесс создания объекта групповой политики, развертывания объекта групповой политики или удаления объекта групповой политики из рабочей среды домена, но для подтверждения запроса требуется администратор.</span><span class="sxs-lookup"><span data-stu-id="76099-150">Be aware that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment of the domain, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="76099-151">Я не могу использовать имя определенного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="76099-151">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="76099-152">**Причина**: либо имя GPO уже используется, либо отсутствует разрешение на перечисление объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="76099-152">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="76099-153">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="76099-153">**Solution**:</span></span>

    -   <span data-ttu-id="76099-154">Если имя объекта групповой политики отображается на вкладке " **управляемый**", " **неуправляемый**" или " **ожидающий** ", выберите другое имя.</span><span class="sxs-lookup"><span data-stu-id="76099-154">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="76099-155">Если развернутый объект групповой политики переименован, но еще не повторно установлен, он будет отображаться под его старым именем в рабочей среде домена.</span><span class="sxs-lookup"><span data-stu-id="76099-155">If a GPO that was deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment of the domain.</span></span> <span data-ttu-id="76099-156">Таким образом, старое имя по-прежнему используется.</span><span class="sxs-lookup"><span data-stu-id="76099-156">Therefore, the old name is still being used.</span></span> <span data-ttu-id="76099-157">Повторно разверните объект групповой политики, чтобы обновить его имя в рабочей среде, и отпустите это имя для другого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="76099-157">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="76099-158">Если имя GPO не отображается на вкладке **управляемые**, **неуправляемые**или **ожидающие утверждения** , возможно, у вас отсутствует разрешение на перечисление объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="76099-158">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="76099-159">Чтобы запросить разрешение, обратитесь к администратору РАСШИРЕНного доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="76099-159">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="76099-160">Я не получаю уведомления по электронной почте для РАСШИРЕНного разгрузки</span><span class="sxs-lookup"><span data-stu-id="76099-160">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="76099-161">**Причина**: допустимый SMTP-сервер электронной почты и адрес электронной почты не предоставлены либо никаких действий, которые создают уведомление по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="76099-161">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="76099-162">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="76099-162">**Solution**:</span></span>

    -   <span data-ttu-id="76099-163">Если вы являетесь администратором РАСШИРЕНного доступа к сети: для уведомлений по электронной почте о действиях, которые должны отправляться службой РАСШИРЕНного доступа к учетной записи, администратором РАСШИРЕНного **Domain Delegation** доступа к сети должны быть указаны допустимые SMTP-сервер электронной почты и адреса электронной почты утверждающих Дополнительные сведения можно найти в разделе [Настройка уведомлений по электронной почте](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="76099-163">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

    -   <span data-ttu-id="76099-164">Уведомления по электронной почте генерируются только в том случае, если редактор, рецензент или другой администратор групповых политик не имеет разрешения, необходимого для создания, развертывания или удаления объекта групповой политики, который отправляет запрос на выполнение одного из этих действий.</span><span class="sxs-lookup"><span data-stu-id="76099-164">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="76099-165">Автоматическое уведомление о том, что утверждение или отклонение запроса не существует.</span><span class="sxs-lookup"><span data-stu-id="76099-165">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="76099-166">Я не могу использовать порт 4600 для службы РАСШИРЕНного использования.</span><span class="sxs-lookup"><span data-stu-id="76099-166">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="76099-167">**Причина**: по умолчанию порт, на который прослушивается служба расширенного выбора, является портом 4600.</span><span class="sxs-lookup"><span data-stu-id="76099-167">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="76099-168">**Решение**: Если для службы расширенного доступа к аналитике недоступен порт 4600, измените конфигурацию порта на сервере расширенного доступа, чтобы использовать другой порт, а затем обновите порт в соединении с сервером расширенного доступа для клиентов расширенного доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="76099-168">**Solution**: If port 4600 is not available for the AGPM Service, modify the port configuration on the AGPM Server to use another port and then update the port in the AGPM Server connection for AGPM Clients.</span></span> <span data-ttu-id="76099-169">Дополнительные сведения можно найти в разделе [изменение службы расширенного редактирования](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="76099-169">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="76099-170">Служба РАСШИРЕНного обслуживания не запускается</span><span class="sxs-lookup"><span data-stu-id="76099-170">The AGPM Service will not start</span></span>

-   <span data-ttu-id="76099-171">**Причина**: вы изменили параметры для службы расширенного **управления правами** в операционной системе в разделе Администрирование и **службы**.</span><span class="sxs-lookup"><span data-stu-id="76099-171">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="76099-172">**Решение**: измените параметры **расширенного управления групповыми политиками Майкрософт — сервер** в разделе " **программы и компоненты** " на панели управления.</span><span class="sxs-lookup"><span data-stu-id="76099-172">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Programs and Features** in Control Panel.</span></span> <span data-ttu-id="76099-173">Дополнительные сведения можно найти в разделе [изменение службы расширенного редактирования](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="76099-173">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="76099-174">Установка программного обеспечения для групповой политики не может установить программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="76099-174">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="76099-175">**Причина**: с помощью функции пересылки обеспечивается целостность пакетов установки программного обеспечения групповой политики.</span><span class="sxs-lookup"><span data-stu-id="76099-175">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="76099-176">Несмотря на то, что объекты групповой политики редактируются в автономном режиме, ссылки между пакетами Помимо кэшированных данных клиента сохраняются.</span><span class="sxs-lookup"><span data-stu-id="76099-176">Although GPOs are edited offline, links between packages in addition to cached client information are preserved.</span></span> <span data-ttu-id="76099-177">Это сделано намеренно.</span><span class="sxs-lookup"><span data-stu-id="76099-177">This is by design.</span></span>

-   <span data-ttu-id="76099-178">**Решение**: когда вы ИЗМЕНЯЕТе GPO в автономном режиме с помощью групповой политики, настройте обновление пакета в другом GPO для ссылки на развернутый объект GPO, а не извлеченную копию.</span><span class="sxs-lookup"><span data-stu-id="76099-178">**Solution**: When you edit a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="76099-179">Редактор должен иметь разрешение на **Чтение** для развернутого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="76099-179">The Editor must have **Read** permission for the deployed GPO.</span></span>

### <a href="" id="bkmk-error-on-restore"></a><span data-ttu-id="76099-180">Произошла ошибка при восстановлении архива на новом сервере РАСШИРЕНного шаблона</span><span class="sxs-lookup"><span data-stu-id="76099-180">An error occurred when I restored the archive to a new AGPM Server</span></span>

-   <span data-ttu-id="76099-181">**Причина**: в целях обеспечения безопасности шифрование, защищающее пароль, введенное на вкладке " **Делегирование домена** ", приводит к сбою пароля при перемещении архива на другой компьютер.</span><span class="sxs-lookup"><span data-stu-id="76099-181">**Cause**: For security reasons, the encryption protecting the password entered on the **Domain Delegation** tab causes the password to fail if the archive is moved to another computer.</span></span>

-   <span data-ttu-id="76099-182">**Решение**: повторно введите пароль и подтвердите его на вкладке **Делегирование домена** . Дополнительные сведения можно найти в разделе [Настройка уведомлений по электронной почте](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="76099-182">**Solution**: Re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

 

 





