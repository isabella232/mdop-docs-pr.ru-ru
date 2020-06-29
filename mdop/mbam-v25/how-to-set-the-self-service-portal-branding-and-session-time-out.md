---
title: Настройка торговой марки и времени ожидания сеанса портала самообслуживания
description: Настройка торговой марки и времени ожидания сеанса портала самообслуживания
author: dansimp
ms.assetid: 031eedfc-fade-4d2f-8771-b329e1d38c0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e222880b2d5557ef15cd7a4efd6421b9972541f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812533"
---
# <span data-ttu-id="a3456-103">Настройка торговой марки и времени ожидания сеанса портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="a3456-103">How to Set the Self-Service Portal Branding and Session Time-out</span></span>


<span data-ttu-id="a3456-104">После настройки портала самообслуживания вы можете использовать в качестве фирменного названия название компании, URL-адрес службы поддержки и текст "Примечание".</span><span class="sxs-lookup"><span data-stu-id="a3456-104">After you configure the Self-Service Portal, you can brand it with your company name, Help Desk URL, and "notice" text.</span></span> <span data-ttu-id="a3456-105">Вы также можете изменить время ожидания сеанса, чтобы завершить сеанс пользователя после определенного периода бездействия.</span><span class="sxs-lookup"><span data-stu-id="a3456-105">You can also change the Session Time-out setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="a3456-106">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a3456-106">Note</span></span>**  
<span data-ttu-id="a3456-107">Вы также можете навести фирменный портал самообслуживания с помощью командлета Windows PowerShell **Enable-MbamWebApplication** или мастера настройки сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="a3456-107">You can also brand the Self-Service Portal by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="a3456-108">Инструкции по использованию мастера приведены [в разделе Настройка веб-приложений MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="a3456-108">For instructions on using the wizard, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>



**<span data-ttu-id="a3456-109">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a3456-109">Note</span></span>**  
<span data-ttu-id="a3456-110">В приведенных ниже инструкциях *Selfservice* является именем виртуального каталога по умолчанию для портала самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="a3456-110">In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="a3456-111">Возможно, вы использовали другое имя, когда вы настроили портал самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="a3456-111">You might have used a different name when you configured the Self-Service Portal.</span></span>



**<span data-ttu-id="a3456-112">Настройка времени ожидания сеанса и фирменной символики для портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="a3456-112">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="a3456-113">Чтобы установить время ожидания для сеанса конечного пользователя, запустите **Диспетчер служб**IIS или запустите **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="a3456-113">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="a3456-114">Перейдите к **сайтам** &gt; **Администрирование и наблюдение за** &gt; **Selfservice** &gt; **ASP.NET** &gt; **сеанса**и измените значение **тайм-аута** в разделе **"Параметры cookie** " на количество минут, по прошествии которого истечет срок действия сеанса портала самообслуживания конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="a3456-114">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session expires.</span></span> <span data-ttu-id="a3456-115">Значением по умолчанию является **5**.</span><span class="sxs-lookup"><span data-stu-id="a3456-115">The default value is **5**.</span></span> <span data-ttu-id="a3456-116">Чтобы отключить этот параметр, чтобы время ожидания не существовало, установите для него значение **0**.</span><span class="sxs-lookup"><span data-stu-id="a3456-116">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="a3456-117">Чтобы настроить элементы фирменной символики для портала самообслуживания, запустите **Диспетчер служб** IIS или запустите **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="a3456-117">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager** or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="a3456-118">Перейдите к **сайтам** &gt; **Администрирование и наблюдение за** &gt; **Selfservice** &gt; **параметрами приложений**Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a3456-118">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="a3456-119">В столбце **имя** выберите элемент, который нужно изменить, и измените значение по умолчанию, чтобы оно отражало имя, которое вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="a3456-119">In the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="a3456-120">В следующей таблице перечислены значения, которые можно установить.</span><span class="sxs-lookup"><span data-stu-id="a3456-120">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="a3456-121">Осторожны</span><span class="sxs-lookup"><span data-stu-id="a3456-121">Caution</span></span>**  
    <span data-ttu-id="a3456-122">Не изменяйте значение в столбце имя (CompanyName \ \*), так как это приведет к прекращению работы портала самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="a3456-122">Do not change the value in the Name column (CompanyName\*), as it will cause Self-Service Portal to stop working.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ClientValidationEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>CompanyName</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DisplayNotice</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText</p></td>
<td align="left"><p>Contact Helpdesk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl</p></td>
<td align="left"><p>#</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, the HelpdeskUrl default value is empty.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390515](//go.microsoft.com/fwlink/?LinkID=390515)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery-1.10.2.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>jQueryValidatePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390516](//go.microsoft.com/fwlink/?LinkID=390516)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryValidateUnobtrusivePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390517](//go.microsoft.com/fwlink/?LinkID=390517)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.unobtrusive.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the notice text either by using the Internet Information Services (IIS) Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>UnobtrusiveJavaScriptEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
</tbody>
</table>
~~~





## <span data-ttu-id="a3456-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a3456-123">Related topics</span></span>


[<span data-ttu-id="a3456-124">Настройка портала самообслуживания для организации</span><span class="sxs-lookup"><span data-stu-id="a3456-124">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)



## <span data-ttu-id="a3456-125">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="a3456-125">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a3456-126">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="a3456-126">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a3456-127">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a3456-127">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





