---
title: Устранение неполадок средства расширенного управления групповыми политиками
description: Устранение неполадок средства расширенного управления групповыми политиками
author: dansimp
ms.assetid: f58849cf-6c5b-44d8-b356-0ed7a5b24cee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c22b9a0983b26252ee0d9c8d99b63cd4ab5dc2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818252"
---
# <span data-ttu-id="542e3-103">Устранение неполадок средства расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="542e3-103">Troubleshooting Advanced Group Policy Management</span></span>


<span data-ttu-id="542e3-104">В этом разделе перечислены некоторые распространенные проблемы, которые могут возникнуть при использовании расширенного управления групповыми политиками для управления объектами групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="542e3-104">This section lists a few common issues you may encounter when using Advanced Group Policy Management (AGPM) to manage Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="542e3-105">Какие неполадки возникают?</span><span class="sxs-lookup"><span data-stu-id="542e3-105">What problems are you having?</span></span>


-   [<span data-ttu-id="542e3-106">Не удается получить доступ к архиву</span><span class="sxs-lookup"><span data-stu-id="542e3-106">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="542e3-107">Состояние GPO меняется для разных администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="542e3-107">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="542e3-108">Не удается изменить соединение с сервером РАСШИРЕНного разрешения</span><span class="sxs-lookup"><span data-stu-id="542e3-108">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="542e3-109">Не удается изменить шаблон или представление по умолчанию, создать, изменить, переименовать, развернуть или удалить GPO</span><span class="sxs-lookup"><span data-stu-id="542e3-109">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="542e3-110">Я не могу использовать имя определенного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="542e3-110">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="542e3-111">Я не получаю уведомления по электронной почте для РАСШИРЕНного разгрузки</span><span class="sxs-lookup"><span data-stu-id="542e3-111">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="542e3-112">Я не могу использовать порт 4600 для службы РАСШИРЕНного использования.</span><span class="sxs-lookup"><span data-stu-id="542e3-112">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="542e3-113">Служба РАСШИРЕНного обслуживания не запускается</span><span class="sxs-lookup"><span data-stu-id="542e3-113">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="542e3-114">Установка программного обеспечения для групповой политики не может установить программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="542e3-114">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="542e3-115">Не удается получить доступ к архиву</span><span class="sxs-lookup"><span data-stu-id="542e3-115">I am unable to access an archive</span></span>

-   <span data-ttu-id="542e3-116">**Причина**: вы не выбрали правильный сервер и порт для архива.</span><span class="sxs-lookup"><span data-stu-id="542e3-116">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="542e3-117">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="542e3-117">**Solution**:</span></span>

    -   <span data-ttu-id="542e3-118">Если вы являетесь администратором РАСШИРЕНного разрешения: ознакомьтесь [с Разстройкой подключения сервера расширенного](configure-the-agpm-server-connection.md)администрирования.</span><span class="sxs-lookup"><span data-stu-id="542e3-118">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="542e3-119">Если вы не являетесь администратором РАСШИРЕНного разрешения, выполните запрос сведений о подключении для сервера РАСШИРЕНного администрирования с помощью администратора РАСШИРЕНного разрешения.</span><span class="sxs-lookup"><span data-stu-id="542e3-119">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="542e3-120">См.: [Настройка подключения к серверу расширенного конфигурирования](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="542e3-120">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

-   <span data-ttu-id="542e3-121">**Причина**: служба расширенного управления групповыми политиками не запущена.</span><span class="sxs-lookup"><span data-stu-id="542e3-121">**Cause**: The Advanced Group Policy Management Service is not running.</span></span>

-   <span data-ttu-id="542e3-122">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="542e3-122">**Solution**:</span></span>

    -   <span data-ttu-id="542e3-123">Если вы являетесь администратором РАСШИРЕНного разрешения, запустите службу РАСШИРЕНного администрирования.</span><span class="sxs-lookup"><span data-stu-id="542e3-123">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="542e3-124">Дополнительные сведения можно найти в разделе [Запуск и остановка службы расширенного](start-and-stop-the-agpm-service.md)просмотра.</span><span class="sxs-lookup"><span data-stu-id="542e3-124">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).</span></span>

    -   <span data-ttu-id="542e3-125">Если вы не являетесь администратором РАСШИРЕНного разрешения, обратитесь за помощью к администратору РАСШИРЕНного администрирования.</span><span class="sxs-lookup"><span data-stu-id="542e3-125">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="542e3-126">Состояние GPO меняется для разных администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="542e3-126">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="542e3-127">**Причина**: различные администраторы групповой политики выбрали различные серверы расширенного доменных служб для одного и того же архива.</span><span class="sxs-lookup"><span data-stu-id="542e3-127">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="542e3-128">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="542e3-128">**Solution**:</span></span>

    -   <span data-ttu-id="542e3-129">Если вы являетесь администратором РАСШИРЕНного разрешения: ознакомьтесь [с Разстройкой подключения сервера расширенного](configure-the-agpm-server-connection.md)администрирования.</span><span class="sxs-lookup"><span data-stu-id="542e3-129">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="542e3-130">Если вы не являетесь администратором РАСШИРЕНного разрешения, выполните запрос сведений о подключении для сервера РАСШИРЕНного администрирования с помощью администратора РАСШИРЕНного разрешения.</span><span class="sxs-lookup"><span data-stu-id="542e3-130">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="542e3-131">См.: [Настройка подключения к серверу расширенного конфигурирования](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="542e3-131">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="542e3-132">Не удается изменить соединение с сервером РАСШИРЕНного разрешения</span><span class="sxs-lookup"><span data-stu-id="542e3-132">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="542e3-133">**Причина**: Если параметры на вкладке " **сервер расширенного управления групповыми политиками** " недоступны, сервер расширенного доступа к данным был централизованно настроен с помощью административного шаблона.</span><span class="sxs-lookup"><span data-stu-id="542e3-133">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="542e3-134">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="542e3-134">**Solution**:</span></span>

    -   <span data-ttu-id="542e3-135">Если вы являетесь администратором РАСШИРЕНного доступа к сети: Если параметры на вкладке **сервер расширенного** доступа к данным недоступны, ознакомьтесь [с Разстройкой подключения сервера расширенного](configure-the-agpm-server-connection.md)доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="542e3-135">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="542e3-136">Если вы не являетесь администратором РАСШИРЕНного доступа: Если параметры на вкладке **сервер расширенного** доступа к сети недоступны, вам не нужно изменять сервер расширенного доступа.</span><span class="sxs-lookup"><span data-stu-id="542e3-136">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="542e3-137">Не удается изменить шаблон или представление по умолчанию, создать, изменить, переименовать, развернуть или удалить GPO</span><span class="sxs-lookup"><span data-stu-id="542e3-137">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="542e3-138">**Причина**: вам не назначена роль с разрешениями, необходимыми для выполнения задачи или задач.</span><span class="sxs-lookup"><span data-stu-id="542e3-138">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="542e3-139">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="542e3-139">**Solution**:</span></span>

    -   <span data-ttu-id="542e3-140">Если вы являетесь администратором РАСШИРЕНного доступа к [доменным](delegate-domain-level-access.md) [ресурсам](delegate-access-to-an-individual-gpo.md), сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="542e3-140">If you are an AGPM Administrator: See [Delegate Domain-Level Access](delegate-domain-level-access.md) and [Delegate Access to an Individual GPO](delegate-access-to-an-individual-gpo.md).</span></span> <span data-ttu-id="542e3-141">Разрешения РАСШИРЕНного доступа к доменным объектам будут каскадными из домена на все GPO в архиве.</span><span class="sxs-lookup"><span data-stu-id="542e3-141">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="542e3-142">По мере добавления администраторов новой групповой политики на уровне домена их разрешения должны быть заданы для применения к **объекту и вложенным объектам**.</span><span class="sxs-lookup"><span data-stu-id="542e3-142">As new Group Policy administrators are added at the domain level, their permissions must be set to apply to **This object and nested objects**.</span></span> <span data-ttu-id="542e3-143">Сведения о ролях, которые могут выполнять задачи, и о том, какие разрешения необходимы для выполнения задачи, можно найти в справке по этой задаче.</span><span class="sxs-lookup"><span data-stu-id="542e3-143">For details about which roles can perform a task and what permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="542e3-144">Если вы не являетесь администратором РАСШИРЕНного доступа и вам требуются дополнительные роли или разрешения: обратитесь за помощью к администратору РАСШИРЕНного администрирования.</span><span class="sxs-lookup"><span data-stu-id="542e3-144">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="542e3-145">Обратите внимание, что если вы являетесь редактором, вы можете начать процесс создания объекта групповой политики, развертывания объекта групповой политики или удаления объекта групповой политики из рабочей среды, но необходимо утвердить запрос с помощью администратора утверждающего или РАСШИРЕНного анализа.</span><span class="sxs-lookup"><span data-stu-id="542e3-145">Note that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="542e3-146">Я не могу использовать имя определенного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="542e3-146">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="542e3-147">**Причина**: либо имя GPO уже используется, либо отсутствует разрешение на перечисление объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="542e3-147">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="542e3-148">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="542e3-148">**Solution**:</span></span>

    -   <span data-ttu-id="542e3-149">Если имя объекта групповой политики отображается на вкладке " **управляемый**", " **неуправляемый**" или " **ожидающий** ", выберите другое имя.</span><span class="sxs-lookup"><span data-stu-id="542e3-149">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="542e3-150">Если развернутый объект групповой политики переименован, но еще не повторно установлен, он будет отображаться под его старым именем в рабочей среде, поэтому старое имя по-прежнему используется.</span><span class="sxs-lookup"><span data-stu-id="542e3-150">If a GPO that has been deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment—therefore, the old name is still in use.</span></span> <span data-ttu-id="542e3-151">Повторно разверните объект групповой политики, чтобы обновить его имя в рабочей среде, и отпустите это имя для другого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="542e3-151">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="542e3-152">Если имя GPO не отображается на вкладке **управляемые**, **неуправляемые**или **ожидающие утверждения** , возможно, у вас отсутствует разрешение на перечисление объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="542e3-152">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="542e3-153">Чтобы запросить разрешение, обратитесь к администратору РАСШИРЕНного доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="542e3-153">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="542e3-154">Я не получаю уведомления по электронной почте для РАСШИРЕНного разгрузки</span><span class="sxs-lookup"><span data-stu-id="542e3-154">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="542e3-155">**Причина**: допустимый SMTP-сервер электронной почты и адрес электронной почты не предоставлены либо никаких действий, которые создают уведомление по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="542e3-155">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="542e3-156">**Решение**:</span><span class="sxs-lookup"><span data-stu-id="542e3-156">**Solution**:</span></span>

    -   <span data-ttu-id="542e3-157">Если вы являетесь администратором РАСШИРЕНного доступа к сети: для уведомлений по электронной почте о действиях, которые должны отправляться службой РАСШИРЕНного доступа к учетной записи, администратором РАСШИРЕНного **Domain Delegation** доступа к сети должны быть указаны допустимые SMTP-сервер электронной почты и адреса электронной почты утверждающих Дополнительные сведения можно найти в разделе [Настройка уведомлений по электронной почте](configure-e-mail-notification.md).</span><span class="sxs-lookup"><span data-stu-id="542e3-157">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification.md).</span></span>

    -   <span data-ttu-id="542e3-158">Уведомления по электронной почте генерируются только в том случае, если редактор, рецензент или другой администратор групповых политик не имеет разрешения, необходимого для создания, развертывания или удаления объекта групповой политики, который отправляет запрос на выполнение одного из этих действий.</span><span class="sxs-lookup"><span data-stu-id="542e3-158">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="542e3-159">Автоматическое уведомление о том, что утверждение или отклонение запроса не существует.</span><span class="sxs-lookup"><span data-stu-id="542e3-159">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="542e3-160">Я не могу использовать порт 4600 для службы РАСШИРЕНного использования.</span><span class="sxs-lookup"><span data-stu-id="542e3-160">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="542e3-161">**Причина**: по умолчанию порт, на который прослушивается служба расширенного выбора, является портом 4600.</span><span class="sxs-lookup"><span data-stu-id="542e3-161">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="542e3-162">**Решение**: Если для службы расширенного доступа к сети недоступен порт 4600, измените каждый файл индекса архива так, чтобы он использовал другой порт, а затем обновите сервер расширенного доступа для всех администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="542e3-162">**Solution**: If port 4600 is not available for the AGPM Service, modify each archive index file to use another port and then update the AGPM Server for all Group Policy administrators.</span></span> <span data-ttu-id="542e3-163">Дополнительные сведения можно найти [в разделе Изменение порта, прослушиваемого службой расширенного выбора](modify-the-port-on-which-the-agpm-service-listens.md).</span><span class="sxs-lookup"><span data-stu-id="542e3-163">For more information, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="542e3-164">Служба РАСШИРЕНного обслуживания не запускается</span><span class="sxs-lookup"><span data-stu-id="542e3-164">The AGPM Service will not start</span></span>

-   <span data-ttu-id="542e3-165">**Причина**: вы изменили параметры для службы расширенного **управления правами** в операционной системе в разделе Администрирование и **службы**.</span><span class="sxs-lookup"><span data-stu-id="542e3-165">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="542e3-166">**Решение**: измените параметры **расширенного управления групповыми политиками Microsoft — сервера** в разделе " **Установка и удаление программ**".</span><span class="sxs-lookup"><span data-stu-id="542e3-166">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Add or Remove Programs**.</span></span> <span data-ttu-id="542e3-167">Дополнительные сведения можно найти [в разделе Изменение учетной записи службы расширенного](modify-the-agpm-service-account.md)редактирования.</span><span class="sxs-lookup"><span data-stu-id="542e3-167">For more information, see [Modify the AGPM Service Account](modify-the-agpm-service-account.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="542e3-168">Установка программного обеспечения для групповой политики не может установить программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="542e3-168">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="542e3-169">**Причина**: с помощью функции пересылки обеспечивается целостность пакетов установки программного обеспечения групповой политики.</span><span class="sxs-lookup"><span data-stu-id="542e3-169">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="542e3-170">Несмотря на то, что объекты групповой политики редактируются в автономном режиме, ссылки между пакетами, а также кэшированные данные клиента сохраняются.</span><span class="sxs-lookup"><span data-stu-id="542e3-170">Although GPOs are edited offline, links between packages as well as cached client information are preserved.</span></span> <span data-ttu-id="542e3-171">Это сделано намеренно.</span><span class="sxs-lookup"><span data-stu-id="542e3-171">This is by design.</span></span>

-   <span data-ttu-id="542e3-172">**Решение**: при работе с групповой политикой в автономном режиме с помощью групповой политики настройте обновление пакета в другом GPO для ссылки на развернутый объект GPO, а не извлеченную копию.</span><span class="sxs-lookup"><span data-stu-id="542e3-172">**Solution**: When editing a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="542e3-173">Редактор должен иметь разрешение на **Чтение** для развернутого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="542e3-173">The Editor must have **Read** permission for the deployed GPO.</span></span>

 

 





