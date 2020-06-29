---
title: Планирование защиты веб-сайтов MBAM
description: Планирование защиты веб-сайтов MBAM
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825022"
---
# <span data-ttu-id="30017-103">Планирование защиты веб-сайтов MBAM</span><span class="sxs-lookup"><span data-stu-id="30017-103">Planning How to Secure the MBAM Websites</span></span>


<span data-ttu-id="30017-104">В этой статье описаны следующие методы обеспечения безопасности администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5 и веб-сайта мониторинга и самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="30017-104">This topic describes the following methods for securing the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Administration and Monitoring Website and Self-Service Portal:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30017-105">Метод</span><span class="sxs-lookup"><span data-stu-id="30017-105">Method</span></span></th>
<th align="left"><span data-ttu-id="30017-106">Обязательный или необязательный?</span><span class="sxs-lookup"><span data-stu-id="30017-106">Required or optional?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30017-107">Использование сертификатов для обеспечения безопасности веб-сайтов MBAM</span><span class="sxs-lookup"><span data-stu-id="30017-107">Using certificates to secure MBAM websites</span></span></p></td>
<td align="left"><p><span data-ttu-id="30017-108">Необязательно, но настоятельно рекомендуется</span><span class="sxs-lookup"><span data-stu-id="30017-108">Optional, but highly recommended</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30017-109">Регистрация имен участников-служб (SPN) для учетной записи пула приложений</span><span class="sxs-lookup"><span data-stu-id="30017-109">Registering Service Principal Names (SPN) for the application pool account</span></span></p></td>
<td align="left"><p><span data-ttu-id="30017-110">Обязательный</span><span class="sxs-lookup"><span data-stu-id="30017-110">Required</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="30017-111">Дополнительные сведения о том, как защитить развертывание MBAM, можно найти в статьях [вопросы безопасности в MBAM 2,5](mbam-25-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="30017-111">For more information about how to secure your MBAM deployment, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md).</span></span>

## <span data-ttu-id="30017-112">Использование сертификатов для обеспечения безопасности веб-сайтов MBAM</span><span class="sxs-lookup"><span data-stu-id="30017-112">Using certificates to secure MBAM websites</span></span>


<span data-ttu-id="30017-113">Мы рекомендуем использовать сертификат для обеспечения взаимодействия между абонентами:</span><span class="sxs-lookup"><span data-stu-id="30017-113">We recommend that you use a certificate to secure the communication between the:</span></span>

-   <span data-ttu-id="30017-114">Клиент MBAM и веб-службы</span><span class="sxs-lookup"><span data-stu-id="30017-114">MBAM Client and the web services</span></span>

-   <span data-ttu-id="30017-115">Браузер и веб-сайт администрирования и мониторинга и веб-сайты портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="30017-115">Browser and the Administration and Monitoring Website and the Self-Service Portal websites</span></span>

<span data-ttu-id="30017-116">Сведения о том, как запросить и установить сертификат, приведены в разделе [Настройка сертификатов Интернет-сервера](https://technet.microsoft.com/library/cc731977.aspx).</span><span class="sxs-lookup"><span data-stu-id="30017-116">For information about requesting and installing a certificate, see [Configuring Internet Server Certificates](https://technet.microsoft.com/library/cc731977.aspx).</span></span>

**<span data-ttu-id="30017-117">Примечание.</span><span class="sxs-lookup"><span data-stu-id="30017-117">Note</span></span>**  
<span data-ttu-id="30017-118">Вы можете настроить веб-сайты и веб-службы на разных серверах только в том случае, если вы используете Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30017-118">You can configure the websites and web services on different servers only if you are using Windows PowerShell.</span></span> <span data-ttu-id="30017-119">Если вы используете мастер настройки сервера MBAM для настройки сайтов, необходимо настроить веб-сайты и веб-службы на одном и том же сервере.</span><span class="sxs-lookup"><span data-stu-id="30017-119">If you use the MBAM Server Configuration wizard to configure the websites, you must configure the websites and the web services on the same server.</span></span>



<span data-ttu-id="30017-120">Для обеспечения безопасности связи между веб-службами и базами данных мы также рекомендуем принудительно использовать шифрование в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="30017-120">To secure the communication between the web services and the databases, we also recommend that you force encryption in SQL Server.</span></span> <span data-ttu-id="30017-121">Сведения о защите всех подключений к SQL Server, в том числе о связи между веб-службами и SQL Server, можно найти в разделе [вопросы безопасности в MBAM 2,5](mbam-25-security-considerations.md#bkmk-secure-databases).</span><span class="sxs-lookup"><span data-stu-id="30017-121">For information about securing all connections to SQL Server, including communication between the web services and SQL Server, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-secure-databases).</span></span>

## <span data-ttu-id="30017-122">Регистрация SPN для учетной записи пула приложений</span><span class="sxs-lookup"><span data-stu-id="30017-122">Registering SPNs for the application pool account</span></span>


<span data-ttu-id="30017-123">Чтобы разрешить серверам MBAM возможность проверки подлинности связи на веб-сайте администрирования и мониторинга и на портале самообслуживания, необходимо зарегистрировать имя участника-службы (SPN) для имени узла в учетной записи домена, которую вы используете для работы с этим пулом приложений.</span><span class="sxs-lookup"><span data-stu-id="30017-123">To enable the MBAM Servers to authenticate communication from the Administration and Monitoring Website and the Self-Service Portal, you must register a Service Principal Name (SPN) for the host name under the domain account that you are using for the web application pool.</span></span>

<span data-ttu-id="30017-124">В этой статье приведены инструкции по регистрации SPN для следующих типов имен узлов.</span><span class="sxs-lookup"><span data-stu-id="30017-124">This topic contains instructions on how to register SPNs for the following types of host names:</span></span>

-   <span data-ttu-id="30017-125">Полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="30017-125">Fully qualified domain name</span></span>

-   <span data-ttu-id="30017-126">Имя NetBIOS</span><span class="sxs-lookup"><span data-stu-id="30017-126">NetBIOS name</span></span>

-   <span data-ttu-id="30017-127">Виртуальное имя</span><span class="sxs-lookup"><span data-stu-id="30017-127">Virtual name</span></span>

### <span data-ttu-id="30017-128">Перед созданием SPN для начальной установки MBAM</span><span class="sxs-lookup"><span data-stu-id="30017-128">Before you create SPNs for an initial MBAM installation</span></span>

<span data-ttu-id="30017-129">Прежде чем приступить к созданию SPN, ознакомьтесь со сведениями в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="30017-129">Review the information in the following table before you start creating SPNs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30017-130">Задача или элемент</span><span class="sxs-lookup"><span data-stu-id="30017-130">Task or item</span></span></th>
<th align="left"><span data-ttu-id="30017-131">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="30017-131">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30017-132">Создание учетной записи службы в доменных службах Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="30017-132">Create a service account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="30017-133">Учетная запись службы — это учетная запись пользователя, созданная в доменных СЛУЖБах Active Directory для обеспечения безопасности веб-сайтов MBAM.</span><span class="sxs-lookup"><span data-stu-id="30017-133">The service account is a user account that you create in AD DS to provide security for the MBAM websites.</span></span> <span data-ttu-id="30017-134">Веб-сайты MBAM выполняются в пуле приложений, удостоверением которого является имя учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="30017-134">The MBAM websites run under an application pool, whose identity is the name of the service account.</span></span> <span data-ttu-id="30017-135">Затем SPN регистрируются в учетной записи пула приложений.</span><span class="sxs-lookup"><span data-stu-id="30017-135">The SPNs are then registered in the application pool account.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="30017-136">Примечание.</span><span class="sxs-lookup"><span data-stu-id="30017-136">Note</span></span></strong><br/><p><span data-ttu-id="30017-137">Для всех веб-серверов необходимо использовать одну и ту же учетную запись пула приложений.</span><span class="sxs-lookup"><span data-stu-id="30017-137">You must use the same application pool account for all web servers.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30017-138">Убедитесь в том, что учетной записи группы IIS-IUSR или учетной записи пула приложений предоставлены необходимые права.</span><span class="sxs-lookup"><span data-stu-id="30017-138">Verify that either the IIS-IUSRS group account or the application pool account has been granted the necessary rights.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30017-139">Чтобы проверить это, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="30017-139">To check this, follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="30017-140">Откройте <strong> Редактор локальной политики безопасности </strong> и разверните <strong> узел Локальные политики </strong> .</span><span class="sxs-lookup"><span data-stu-id="30017-140">Open the <strong>Local Security Policy editor</strong> and expand the <strong>Local Policies</strong> node.</span></span></p></li>
<li><p><span data-ttu-id="30017-141">Выберите <strong> узел Назначение прав пользователей </strong> и дважды щелкните <strong> олицетворение клиента после проверки подлинности и войдите в систему в </strong> <strong> качестве параметров групповой политики для пакетного задания </strong> в области справа.</span><span class="sxs-lookup"><span data-stu-id="30017-141">Select the <strong>User Rights Assignment</strong> node, and double-click the <strong>Impersonate a client after authentication</strong> and <strong>Log on as a batch job</strong> Group Policy settings in the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30017-142">Если вы настроили веб-сайты MBAM с помощью учетной записи администратора домена, MBAM создаст SPN.</span><span class="sxs-lookup"><span data-stu-id="30017-142">If you configure the MBAM websites by using a domain administrative account, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30017-143">Если вы настроили веб-сайты MBAM с помощью учетной записи администратора домена, выполните действия, описанные в этой статье, чтобы зарегистрировать SPN вручную для типа имени узла, которое вы используете.</span><span class="sxs-lookup"><span data-stu-id="30017-143">If you configure the MBAM websites by using a domain administrative account, follow the steps in this topic to register SPNs manually for the type of host name that you are using.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="30017-144">Регистрация SPN при использовании полного доменного имени узла</span><span class="sxs-lookup"><span data-stu-id="30017-144">Registering SPNs when you use a fully qualified domain host name</span></span>

<span data-ttu-id="30017-145">Если вы используете полное доменное имя узла при настройке MBAM, вам нужно зарегистрировать только одно SPN, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="30017-145">If you use a fully qualified domain host name when you configure MBAM, you have to register only one SPN, as shown in the following example.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30017-146">Что вам нужно сделать?</span><span class="sxs-lookup"><span data-stu-id="30017-146">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="30017-147">Примеры и дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="30017-147">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30017-148">Зарегистрируйте имя SPN для полного доменного имени.</span><span class="sxs-lookup"><span data-stu-id="30017-148">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="30017-149">Полное имя узла — <strong> mybitlockerrecovery.contoso.com </strong> , а учетная запись домена, используемая для пула веб-приложений, — <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="30017-149">The fully qualified host name is <strong>mybitlockerrecovery.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30017-150">Настройка ограниченного делегирования для SPN, регистрируемого для учетной записи пула приложений.</span><span class="sxs-lookup"><span data-stu-id="30017-150">Configure constrained delegation for the SPN that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="30017-151">Настройка ограниченного делегирования</span><span class="sxs-lookup"><span data-stu-id="30017-151">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="30017-152">Это требование применимо только к MBAM 2,5; Это не обязательно в MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="30017-152">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="30017-153">Регистрация SPN при использовании имени узла NetBIOS</span><span class="sxs-lookup"><span data-stu-id="30017-153">Registering SPNs when you use a NetBIOS host name</span></span>

<span data-ttu-id="30017-154">Если вы используете имя узла NetBIOS при настройке MBAM, зарегистрируйте одно SPN для имени NetBIOS и другое имя SPN для полного доменного имени, как показано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="30017-154">If you use a NetBIOS host name when you configure MBAM, register one SPN for the NetBIOS name, and another SPN for the fully qualified domain name, as shown in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30017-155">Что вам нужно сделать?</span><span class="sxs-lookup"><span data-stu-id="30017-155">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="30017-156">Примеры и дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="30017-156">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30017-157">Зарегистрируйте имя участника-службы для имени узла NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="30017-157">Register an SPN for the NetBIOS host name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="30017-158">Имя узла NetBIOS — <strong> nbname01 </strong> , а учетная запись домена, используемая для пула веб-приложений, — <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="30017-158">The NetBIOS host name is <strong>nbname01</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30017-159">Зарегистрируйте имя SPN для полного доменного имени.</span><span class="sxs-lookup"><span data-stu-id="30017-159">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="30017-160">Полное доменное имя — <strong> nbname01.contoso.com </strong> , а учетная запись домена, используемая для пула веб-приложений, — <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="30017-160">The fully qualified domain name is <strong>nbname01.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30017-161">Настройте ограниченное делегирование для имен участников, которые регистрируются для учетной записи пула приложений.</span><span class="sxs-lookup"><span data-stu-id="30017-161">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="30017-162">Настройка ограниченного делегирования</span><span class="sxs-lookup"><span data-stu-id="30017-162">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="30017-163">Это требование применимо только к MBAM 2,5; Это не обязательно в MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="30017-163">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a><span data-ttu-id="30017-164">Регистрация SPN при использовании имени виртуального узла</span><span class="sxs-lookup"><span data-stu-id="30017-164">Registering SPNs when you use a virtual host name</span></span>

<span data-ttu-id="30017-165">Если вы настроили MBAM с помощью имени виртуального узла, которое является полным доменным именем, зарегистрируйте только одно SPN для имени виртуального узла.</span><span class="sxs-lookup"><span data-stu-id="30017-165">If you configure MBAM with a virtual host name that is a fully qualified domain name, register only one SPN for the virtual host name.</span></span> <span data-ttu-id="30017-166">Если настраиваемое имя виртуального узла не является полным доменным именем, необходимо создать второе SPN, которое указывает полное доменное имя, как описано в приведенных ниже примерах.</span><span class="sxs-lookup"><span data-stu-id="30017-166">If the virtual host name that you configure is not a fully qualified domain name, you must create a second SPN that specifies the fully qualified domain name, as described in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30017-167">Что вам нужно сделать?</span><span class="sxs-lookup"><span data-stu-id="30017-167">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="30017-168">Примеры и дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="30017-168">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30017-169">Если имя виртуального узла является полным доменным именем, как показано в этом примере, зарегистрируйте только одно SPN.</span><span class="sxs-lookup"><span data-stu-id="30017-169">If your virtual host name is a fully qualified domain name, as in this example, register only one SPN.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="30017-170">В примере именем виртуального узла является <strong> mbamvirtual.contoso.com </strong> , а учетная запись домена, используемая для пула веб-приложений, — <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="30017-170">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30017-171">Зарегистрируйте это дополнительное SPN, если имя виртуального узла не является полным доменным именем.</span><span class="sxs-lookup"><span data-stu-id="30017-171">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="30017-172">В примере именем виртуального узла является <strong> mbamvirtual </strong> , а учетная запись домена, используемая для пула веб-приложений, — <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="30017-172">In the example, the virtual host name is <strong>mbamvirtual</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30017-173">Зарегистрируйте это дополнительное SPN, если имя виртуального узла не является полным доменным именем.</span><span class="sxs-lookup"><span data-stu-id="30017-173">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="30017-174">В примере именем виртуального узла является <strong> mbamvirtual.contoso.com </strong> , а учетная запись домена, используемая для пула веб-приложений, — <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="30017-174">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30017-175">На сервере доменных имен (DNS) создайте запись "A Record" для имени пользовательского узла и укажите его веб-серверу или подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="30017-175">On the Domain Name Server (DNS) server, create an “A record” for the custom host name and point it to a web server or a load balancer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30017-176">Ознакомьтесь с разделом "Настройка DNS HOST A Records" для <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> настройки записей узлов DNS </a> .</span><span class="sxs-lookup"><span data-stu-id="30017-176">See the “To configure DNS Host A Records” section in <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)">Configure DNS Host Records</a>.</span></span></p>
<p><span data-ttu-id="30017-177">Мы рекомендуем использовать записи вместо CNAME.</span><span class="sxs-lookup"><span data-stu-id="30017-177">We recommend that you use A records instead of CNAMES.</span></span> <span data-ttu-id="30017-178">Если вы используете CNAME для указания на адрес домена, необходимо также зарегистрировать SPN для имени веб-сервера в учетной записи пула приложений.</span><span class="sxs-lookup"><span data-stu-id="30017-178">If you use CNAMES to point to the domain address, you must also register SPNs for the web server name in the application pool account.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30017-179">Настройте ограниченное делегирование для имен участников, которые регистрируются для учетной записи пула приложений.</span><span class="sxs-lookup"><span data-stu-id="30017-179">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="30017-180">Настройка ограниченного делегирования</span><span class="sxs-lookup"><span data-stu-id="30017-180">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="30017-181">Это требование применимо только к MBAM 2,5; Это не обязательно в MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="30017-181">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a><span data-ttu-id="30017-182">Регистрация SPN при обновлении предыдущей версии MBAM</span><span class="sxs-lookup"><span data-stu-id="30017-182">Registering an SPN when you upgrade from previous versions of MBAM</span></span>

<span data-ttu-id="30017-183">Выполните действия, описанные в этом разделе, только в том случае, если вы хотите:</span><span class="sxs-lookup"><span data-stu-id="30017-183">Complete the steps in this section only if you want to:</span></span>

-   <span data-ttu-id="30017-184">Переход с предыдущей версии MBAM.</span><span class="sxs-lookup"><span data-stu-id="30017-184">Upgrade from a previous version of MBAM.</span></span>

-   <span data-ttu-id="30017-185">Запустите веб-сайты в MBAM 2,5 в сбалансированной или распределенной конфигурации, и вы работаете в конфигурации, которая не сбалансирована в нагрузки.</span><span class="sxs-lookup"><span data-stu-id="30017-185">Run the websites in MBAM 2.5 in a load-balanced or distributed configuration, and you are currently running in a configuration that is not load balanced.</span></span>

<span data-ttu-id="30017-186">Если вы уже зарегистрировали SPN в учетной записи компьютера, а не в учетной записи пула приложений, MBAM использует существующие SPN, и вы не сможете настроить веб-сайты в балансировке нагрузки или распределенной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="30017-186">If you already registered SPNs on the machine account rather than in an application pool account, MBAM uses the existing SPNs, and you cannot configure the websites in a load-balanced or distributed configuration.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30017-187">Что вам нужно сделать?</span><span class="sxs-lookup"><span data-stu-id="30017-187">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="30017-188">Примеры и дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="30017-188">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30017-189">Создайте учетную запись пула приложений в доменных службах Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="30017-189">Create an application pool account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30017-190">Удалите установленные веб-сайты и веб-службы.</span><span class="sxs-lookup"><span data-stu-id="30017-190">Remove the currently installed websites and web services.</span></span></p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)"><span data-ttu-id="30017-191">Удаление компонентов или программного обеспечения MBAM Server</span><span class="sxs-lookup"><span data-stu-id="30017-191">Removing MBAM Server Features or Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30017-192">Удалите SPN из учетной записи компьютера.</span><span class="sxs-lookup"><span data-stu-id="30017-192">Remove SPNs from the machine account.</span></span></p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30017-193">Зарегистрируйте SPN в учетной записи пула приложений.</span><span class="sxs-lookup"><span data-stu-id="30017-193">Register SPNs in the application pool account.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30017-194">Следуйте указаниям для <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)"> регистрации SPN при использовании имени виртуального узла </a> .</span><span class="sxs-lookup"><span data-stu-id="30017-194">Follow the steps for <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)">Registering SPNs when you use a virtual host name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30017-195">Перенастройте веб-приложения и веб-службы.</span><span class="sxs-lookup"><span data-stu-id="30017-195">Reconfigure the web applications and web services.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="30017-196">Настройка веб-приложений MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="30017-196">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30017-197">Выполните одно из указанных ниже действий в зависимости от того, какой метод вы используете для настройки.</span><span class="sxs-lookup"><span data-stu-id="30017-197">Do one of the following, depending on the method you use for the configuration:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30017-198">Способ</span><span class="sxs-lookup"><span data-stu-id="30017-198">Method</span></span></th>
<th align="left"><span data-ttu-id="30017-199">Подробности</span><span class="sxs-lookup"><span data-stu-id="30017-199">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="30017-200">Мастер настройки сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="30017-200">MBAM Server Configuration wizard</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="30017-201">Введите учетную запись пула приложений в <strong> поле Учетная запись домена пула приложений веб-службы </strong> .</span><span class="sxs-lookup"><span data-stu-id="30017-201">Enter the application pool account in the <strong>Web service application pool domain account</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> <span data-ttu-id="30017-202">Командлет Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="30017-202">Windows PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="30017-203">Введите учетную запись в <code>WebServiceApplicationPoolCredential</code> параметре.</span><span class="sxs-lookup"><span data-stu-id="30017-203">Enter the account in the <code>WebServiceApplicationPoolCredential</code> parameter.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="30017-204">Важно.</span><span class="sxs-lookup"><span data-stu-id="30017-204">Important</span></span></strong><br/><p><span data-ttu-id="30017-205">Имя узла, которое вы ввели, должно совпадать с именем виртуального узла, для которого создаются SPN.</span><span class="sxs-lookup"><span data-stu-id="30017-205">The host name that you enter must be the same name as the virtual host name for which you are creating the SPNs.</span></span> <span data-ttu-id="30017-206">Кроме того, в веб-ферме имена узлов и учетные данные пула приложений должны быть одинаковыми на каждом сервере, который вы настраиваете.</span><span class="sxs-lookup"><span data-stu-id="30017-206">Also, in your web farm, the host names and the application pool credentials must be the same on every server that you are configuring.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="30017-207">Когда MBAM настраивает веб-приложения, он попытается зарегистрировать SPN, но это может сделать только если у вас есть права администратора домена на сервере, на котором выполняется установка MBAM.</span><span class="sxs-lookup"><span data-stu-id="30017-207">When MBAM configures the web applications, it will try to register the SPNs for you, but it can do so only if you have Domain Admin rights on the server on which you are installing MBAM.</span></span> <span data-ttu-id="30017-208">Если у вас нет этих прав, вы можете завершить настройку, но вам придется задать имена участников службы до или после настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="30017-208">If you do not have these rights, you can complete the configuration, but you will have to set the SPNs before or after you configure MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="30017-209">Обязательные параметры фильтрации запросов</span><span class="sxs-lookup"><span data-stu-id="30017-209">Required Request Filtering Settings</span></span>

 <span data-ttu-id="30017-210">"Разрешить неуказанные расширения имен файлов" требуется, чтобы приложение работало надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="30017-210">'Allow unlisted file name extensions' is required for the application to operate as expected.</span></span>  <span data-ttu-id="30017-211">Это можно найти в разделе Фильтрация запросов на администрирование и мониторинг Microsoft BitLocker — > > изменить параметры компонента.</span><span class="sxs-lookup"><span data-stu-id="30017-211">This can be found by navigating to the 'Microsoft BitLocker Administration and Monitoring' -> Request Filtering -> Edit Feature Settings.</span></span>


## <span data-ttu-id="30017-212">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="30017-212">Related topics</span></span>


[<span data-ttu-id="30017-213">Подготовка среды для развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="30017-213">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="30017-214">Необходимые условия для развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="30017-214">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)





## <span data-ttu-id="30017-215">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="30017-215">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="30017-216">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="30017-216">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="30017-217">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="30017-217">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



