---
title: Аутентификация конечных пользователей MED-V
description: Аутентификация конечных пользователей MED-V
author: dansimp
ms.assetid: aaf96eb6-91d1-4f4d-9854-5fc73c7ae7ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14c1e95a94f2da76b6b6c5ebd9d4cf14dcf839a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824889"
---
# <span data-ttu-id="e90d2-103">Аутентификация конечных пользователей MED-V</span><span class="sxs-lookup"><span data-stu-id="e90d2-103">Authentication of MED-V End Users</span></span>


<span data-ttu-id="e90d2-104">Проверка подлинности конечных пользователей Microsoft Enterprise Virtualization (MED-V) 2,0 для конечного пользователя является важной проблемой системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="e90d2-104">The authentication of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 end users is a very important security issue.</span></span> <span data-ttu-id="e90d2-105">В этом контексте проверка подлинности — проверка удостоверения конечного пользователя MED-V.</span><span class="sxs-lookup"><span data-stu-id="e90d2-105">In this context, authentication refers to verifying the identity of the MED-V end user.</span></span>

<span data-ttu-id="e90d2-106">В следующем разделе представлена информация и руководство по проверке подлинности конечными пользователями в MED-V.</span><span class="sxs-lookup"><span data-stu-id="e90d2-106">The following section provides information and guidance about end-user authentication in MED-V.</span></span>

## <span data-ttu-id="e90d2-107">Проверка подлинности пользователей в MED-V</span><span class="sxs-lookup"><span data-stu-id="e90d2-107">User Authentication in MED-V</span></span>


<span data-ttu-id="e90d2-108">Проверка подлинности в MED-V обычно выполняется на двух уровнях: когда пользователь впервые получает доступ к MED-V и каждый раз при изменении пароля.</span><span class="sxs-lookup"><span data-stu-id="e90d2-108">Authentication in MED-V generally occurs at two levels: when a user first accesses MED-V and every time that they change their password.</span></span>

<span data-ttu-id="e90d2-109">В зависимости от того, как вы настроили параметры для проверки подлинности в службах MED-V, конечные пользователи обычно запрашиваются в какой-либо момент для ввода пароля либо при первом запуске MED-V или при первом попытке открыть опубликованное приложение.</span><span class="sxs-lookup"><span data-stu-id="e90d2-109">Depending on how you have configured MED-V settings for authentication, the end user is typically prompted at some point to enter their password, either the first time MED-V is started or the first time that they try to open a published application.</span></span>

<span data-ttu-id="e90d2-110">Есть несколько аспектов проверки подлинности конечных пользователей, которые можно контролировать, включая указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="e90d2-110">There are several aspects of end-user authentication that you can control, including the following:</span></span>

<span data-ttu-id="e90d2-111">Хранятся ли в диспетчере учетных данных учетные данные, которые пользователь вводит.</span><span class="sxs-lookup"><span data-stu-id="e90d2-111">Whether the credentials the end user enters are stored in Credential Manager</span></span>

<span data-ttu-id="e90d2-112">В каком способе отображается конечный пользователь с возможностью ввода и сохранения пароля</span><span class="sxs-lookup"><span data-stu-id="e90d2-112">In what manner the end user is presented with the option of entering and saving their password</span></span>

<span data-ttu-id="e90d2-113">В зависимости от предпочтительного процесса для управления проверкой подлинности конечными пользователями вы можете указать, следует ли выполнять кэширование учетных данных для конкретной рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="e90d2-113">Depending on your company’s preferred process for managing end-user authentication, you can specify whether credential caching occurs for a particular MED-V workspace.</span></span> <span data-ttu-id="e90d2-114">Кэширование учетных данных конечного пользователя полезно, так как они запрашиваются только один раз для ввода пароля.</span><span class="sxs-lookup"><span data-stu-id="e90d2-114">Caching the credentials of an end user is helpful because they are only prompted one time for their password.</span></span> <span data-ttu-id="e90d2-115">Если пользователю не разрешено сохранять пароль или это не решит, что каждый раз при запуске нового сеанса MED-V нужно будет ввести его еще раз.</span><span class="sxs-lookup"><span data-stu-id="e90d2-115">If the end user is not allowed to save their password or they decide not to, every time that they start a new MED-V session, they must enter it again.</span></span> <span data-ttu-id="e90d2-116">Например, если MED-V настроен на запуск при входе пользователя в систему, но проверка подлинности отключена, конечные пользователи будут запрашиваться только один раз во время входа.</span><span class="sxs-lookup"><span data-stu-id="e90d2-116">For example, if MED-V is configured to start when the end user logs on to the host but Authentication is disabled, the end user is only prompted one time during logon.</span></span> <span data-ttu-id="e90d2-117">В этом случае учетные данные действительны до тех пор, пока пользователь не завершит сеанс с компьютера.</span><span class="sxs-lookup"><span data-stu-id="e90d2-117">In this case, credentials are valid until the end user logs off from the host.</span></span>

<span data-ttu-id="e90d2-118">При необходимости вы можете использовать диспетчер учетных данных для удаления всех сохраненных учетных данных для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="e90d2-118">If it is necessary, you can use Credential Manager to remove any stored end-user credentials.</span></span>

<span data-ttu-id="e90d2-119">По умолчанию хранение учетных данных отключено, но вы можете изменить этот параметр, выполнив одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="e90d2-119">By default, credential storing is disabled, but you can change this setting through one of the following methods:</span></span>

<span data-ttu-id="e90d2-120">**При создании пакета рабочей области для MED-V**.</span><span class="sxs-lookup"><span data-stu-id="e90d2-120">**While you are creating the MED-V workspace package**.</span></span> <span data-ttu-id="e90d2-121">Дополнительные сведения можно найти [в разделе Создание пакета рабочей области для MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="e90d2-121">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="e90d2-122">**После развертывания рабочей области MED-V**.</span><span class="sxs-lookup"><span data-stu-id="e90d2-122">**After you have deployed the MED-V workspace**.</span></span> <span data-ttu-id="e90d2-123">Измените параметр командлета MED-V UxCredentialCacheEnabled, чтобы установить раздел реестра служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="e90d2-123">Edit the MED-V cmdlet parameter UxCredentialCacheEnabled to set the Terminal Services registry key.</span></span> <span data-ttu-id="e90d2-124">Дополнительные сведения можно найти в справке Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e90d2-124">For more information, see Windows PowerShell Help.</span></span>

<span data-ttu-id="e90d2-125">После развертывания рабочей области MED-V вы можете настроить параметры проверки подлинности для конечных пользователей, изменив политику служб терминалов с именем DisablePasswordSaving.</span><span class="sxs-lookup"><span data-stu-id="e90d2-125">After MED-V workspace deployment, you can set your preference for end-user authentication by modifying the Terminal Services policy named DisablePasswordSaving.</span></span> <span data-ttu-id="e90d2-126">DisablePasswordSaving определяет, отображается ли флажок Сохранить пароль в диалоговом окне клиента RDP и отображается ли запрос учетных данных MED-V.</span><span class="sxs-lookup"><span data-stu-id="e90d2-126">DisablePasswordSaving controls whether the password saving check box appears on the RDP client dialog window and whether the MED-V credential prompt is displayed.</span></span>

<span data-ttu-id="e90d2-127">Ниже указан путь политики для политики служб терминалов с именем DisablePasswordSaving.</span><span class="sxs-lookup"><span data-stu-id="e90d2-127">Following is the policy path for the Terminal Services policy named DisablePasswordSaving.</span></span>

**<span data-ttu-id="e90d2-128">Программа</span><span class="sxs-lookup"><span data-stu-id="e90d2-128">Regedit:</span></span>**

<span data-ttu-id="e90d2-129">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="e90d2-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span></span>

**<span data-ttu-id="e90d2-130">Примечание.</span><span class="sxs-lookup"><span data-stu-id="e90d2-130">Note</span></span>**  
<span data-ttu-id="e90d2-131">Изменения, вносимые в DisablePasswordSaving, влияют только на запрос RDP для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e90d2-131">The changes that you make to DisablePasswordSaving only affect the RDP prompt to a virtual machine.</span></span>



<span data-ttu-id="e90d2-132">В следующей таблице перечислены различные способы настройки параметров для хранения учетных данных и изменения различных конфигураций.</span><span class="sxs-lookup"><span data-stu-id="e90d2-132">The following table lists the different ways you can configure your settings for credential storing and the effects of the different configurations:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e90d2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e90d2-133">Value</span></span></th>
<th align="left"><span data-ttu-id="e90d2-134">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="e90d2-134">Configuration</span></span></th>
<th align="left"><span data-ttu-id="e90d2-135">Результат</span><span class="sxs-lookup"><span data-stu-id="e90d2-135">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e90d2-136">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="e90d2-136">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="e90d2-137">Отключено</span><span class="sxs-lookup"><span data-stu-id="e90d2-137">Disabled</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e90d2-138">Появится запрос на запуск MED-V и флажок для подтверждения доступен и снят.</span><span class="sxs-lookup"><span data-stu-id="e90d2-138">The MED-V prompt is presented and a check box to accept is available and cleared.</span></span> <span data-ttu-id="e90d2-139">Если пользователь устанавливает этот флажок, учетные данные кэшируются для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="e90d2-139">If the end user selects the check box, credentials are cached for subsequent use.</span></span> <span data-ttu-id="e90d2-140">У конечного пользователя также есть преимущество только после истечения срока действия пароля.</span><span class="sxs-lookup"><span data-stu-id="e90d2-140">The end user also has the benefit of only being prompted when the password expires.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="e90d2-141">Если пользователь не выберет этот флажок, вместо запроса MED-V будет выводиться запрос клиента для подключения к удаленному рабочему столу (RDC), а флажок "Сохранить" снят.</span><span class="sxs-lookup"><span data-stu-id="e90d2-141">If the end user does not select the check box, the Remote Desktop Connection (RDC) Client prompt is presented instead of the MED-V prompt, and the check box to accept is cleared.</span></span> <span data-ttu-id="e90d2-142">Если пользователь выберет этот флажок, учетные данные клиента RDC будут сохранены для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="e90d2-142">If the end user selects the check box, the RDC Client credential is stored for later use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e90d2-143">Важно.</span><span class="sxs-lookup"><span data-stu-id="e90d2-143">Important</span></span></strong><br/><p><span data-ttu-id="e90d2-144">Подключение к удаленному рабочему столу не проверяет учетные данные, когда пользователь вводит их.</span><span class="sxs-lookup"><span data-stu-id="e90d2-144">RDC does not validate credentials when the end user enters them.</span></span> <span data-ttu-id="e90d2-145">Если конечный пользователь кэширует учетные данные с помощью запроса RDC, существует риск, что могут храниться неверные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e90d2-145">If the end user caches the credentials through the RDC prompt, there is a risk that incorrect credentials might be stored.</span></span> <span data-ttu-id="e90d2-146">В этом случае в диспетчере учетных данных Windows необходимо удалить неверные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e90d2-146">In this case, the incorrect credentials must be deleted in the Windows Credential Manager.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e90d2-147">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="e90d2-147">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="e90d2-148">Включено</span><span class="sxs-lookup"><span data-stu-id="e90d2-148">Enabled</span></span></strong></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="e90d2-149">Примечание.</span><span class="sxs-lookup"><span data-stu-id="e90d2-149">Note</span></span></strong><br/><p><span data-ttu-id="e90d2-150">Эта конфигурация более безопасна, так как она не разрешает кэширование учетных данных конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="e90d2-150">This configuration is more secure because it does not allow end user credentials to be cached.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="e90d2-151">По умолчанию установка MED-V устанавливает раздел реестра гостя, чтобы отключить приглашение "срок действия пароля истек".</span><span class="sxs-lookup"><span data-stu-id="e90d2-151">By default, the MED-V installation sets a registry key in the guest to suppress the "password about to expire" prompt.</span></span> <span data-ttu-id="e90d2-152">Пользователю будет предложено только сменить пароль на узле.</span><span class="sxs-lookup"><span data-stu-id="e90d2-152">The end user is only prompted for a password change on the host.</span></span> <span data-ttu-id="e90d2-153">Учетные данные, обновленные на узле, передаются на гость.</span><span class="sxs-lookup"><span data-stu-id="e90d2-153">Credentials that are updated on the host are passed to the guest.</span></span>

**<span data-ttu-id="e90d2-154">Осторожны</span><span class="sxs-lookup"><span data-stu-id="e90d2-154">Caution</span></span>**  
<span data-ttu-id="e90d2-155">Если в вашей среде используется групповая политика, необходимо знать, что она может переопределять раздел реестра, что приводит к появлении запроса на ввод пароля от гостя.</span><span class="sxs-lookup"><span data-stu-id="e90d2-155">If you use Group Policy in your environment, know that it can override the registry key causing the password prompts from the guest to reappear.</span></span>



### <span data-ttu-id="e90d2-156">Вопросы безопасности при проверке подлинности</span><span class="sxs-lookup"><span data-stu-id="e90d2-156">Security Concerns with Authentication</span></span>

<span data-ttu-id="e90d2-157">Несмотря на то, что кэширование учетных данных конечного пользователя обеспечивает наилучшее взаимодействие с пользователем, необходимо учитывать риски, связанные с этим.</span><span class="sxs-lookup"><span data-stu-id="e90d2-157">Even though caching the end user’s credentials provides the best user experience, you must be aware of the risks involved.</span></span>

<span data-ttu-id="e90d2-158">Если включено кэширование учетных данных, учетные данные домена конечного пользователя хранятся в диспетчере учетных данных Windows в виде обратимого формата.</span><span class="sxs-lookup"><span data-stu-id="e90d2-158">When credential caching is enabled, the end user’s domain credential is stored in a reversible format within the Windows Credential Manager.</span></span> <span data-ttu-id="e90d2-159">В результате злоумышленник может написать средство, работающее как процесс системного уровня или процесс конечного пользователя, и получить учетные данные конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="e90d2-159">As a result, an attacker could write a tool that runs as either a system level process or an end user process and that retrieves the end user's credentials.</span></span> <span data-ttu-id="e90d2-160">Вы можете уменьшить этот риск, установив для DisablePasswordSaving значение **Enabled**.</span><span class="sxs-lookup"><span data-stu-id="e90d2-160">You can only lessen this risk by setting DisablePasswordSaving to **Enabled**.</span></span>

<span data-ttu-id="e90d2-161">Эта проблема возникает, когда проверка подлинности MED-V отключена, но параметр политики служб терминалов включен.</span><span class="sxs-lookup"><span data-stu-id="e90d2-161">This same concern exists when MED-V authentication is disabled but the Terminal Services policy setting is enabled.</span></span>

## <span data-ttu-id="e90d2-162">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e90d2-162">Related topics</span></span>


[<span data-ttu-id="e90d2-163">Рекомендации по обеспечению безопасности операций MED-V</span><span class="sxs-lookup"><span data-stu-id="e90d2-163">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)









