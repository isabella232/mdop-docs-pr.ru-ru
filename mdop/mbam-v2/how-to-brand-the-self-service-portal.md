---
title: Настройка фирменной символики для портала самообслуживания
description: Настройка фирменной символики для портала самообслуживания
author: dansimp
ms.assetid: 3ef9e951-7c42-4f7f-b131-3765d39b3207
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe4f4efc5852042671711ba5780cc78055957ba8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825149"
---
# <span data-ttu-id="54c6f-103">Настройка фирменной символики для портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="54c6f-103">How to Brand the Self-Service Portal</span></span>


<span data-ttu-id="54c6f-104">После установки портала самообслуживания Microsoft BitLocker Administration и Monitoring вы можете использовать портал самообслуживания с названием компании, URL-адресом службы поддержки и текстом "Примечание".</span><span class="sxs-lookup"><span data-stu-id="54c6f-104">After you install the Microsoft BitLocker Administration and Monitoring (MBAM) Self-Service Portal, you can brand the Self-Service Portal with your company name, Help Desk URL, and “notice” text.</span></span> <span data-ttu-id="54c6f-105">Вы также можете изменить параметр тайм-аута сеанса, чтобы завершить сеанс конечного пользователя по истечении определенного периода бездействия.</span><span class="sxs-lookup"><span data-stu-id="54c6f-105">You can also change the Session Timeout setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="54c6f-106">Настройка времени ожидания сеанса и фирменной символики для портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="54c6f-106">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="54c6f-107">Чтобы установить время ожидания для сеанса конечного пользователя, запустите **Диспетчер служб**IIS или запустите **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="54c6f-107">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="54c6f-108">Перейдите к **сайтам** &gt; **Администрирование и наблюдение за** &gt; **Selfservice** &gt; **ASP.NET** &gt; **сеанса**и измените значение **времени ожидания** в разделе **"Параметры cookie** " на количество минут, после которого заканчивается срок действия сеанса портала самообслуживания конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="54c6f-108">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session will expire.</span></span> <span data-ttu-id="54c6f-109">Значение по умолчанию — 5.</span><span class="sxs-lookup"><span data-stu-id="54c6f-109">The default is 5.</span></span> <span data-ttu-id="54c6f-110">Чтобы отключить этот параметр, чтобы время ожидания не существовало, установите для него значение **0**.</span><span class="sxs-lookup"><span data-stu-id="54c6f-110">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="54c6f-111">Чтобы настроить элементы фирменной символики для портала самообслуживания, запустите **Диспетчер служб**IIS или запустите **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="54c6f-111">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="54c6f-112">Перейдите к **сайтам** &gt; **Администрирование и наблюдение за** &gt; **Selfservice** &gt; **параметрами приложений**Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="54c6f-112">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="54c6f-113">В столбце **имя** выберите элемент, который нужно изменить, и измените значение по умолчанию, чтобы оно отражало имя, которое вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="54c6f-113">From the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="54c6f-114">В следующей таблице перечислены значения, которые можно установить.</span><span class="sxs-lookup"><span data-stu-id="54c6f-114">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="54c6f-115">Осторожны</span><span class="sxs-lookup"><span data-stu-id="54c6f-115">Caution</span></span>**  
    <span data-ttu-id="54c6f-116">Не изменяйте значение в столбце имя (CompanyName), так как это приводит к прекращению работы портала самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="54c6f-116">Do not change the value in the Name column (CompanyName\*), as it will cause the Self-Service Portal to stop working.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CompanyName*</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText*</p></td>
<td align="left"><p>Contact Help Desk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl*</p></td>
<td align="left"><p>Http://www.microsoft.com</p></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/jQuery/jquery-1.7.2.min.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MicrosoftAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/3.5/MicrosoftAjax.js</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftMvcAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/mvc/2.0/MicrosoftMvcValidation.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the Notice text either by using the IIS Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>
~~~



## <span data-ttu-id="54c6f-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="54c6f-117">Related topics</span></span>


[<span data-ttu-id="54c6f-118">Развертывание инфраструктуры сервера MBAM 2.0 Server</span><span class="sxs-lookup"><span data-stu-id="54c6f-118">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









