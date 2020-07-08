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
# Настройка фирменной символики для портала самообслуживания


После установки портала самообслуживания Microsoft BitLocker Administration и Monitoring вы можете использовать портал самообслуживания с названием компании, URL-адресом службы поддержки и текстом "Примечание". Вы также можете изменить параметр тайм-аута сеанса, чтобы завершить сеанс конечного пользователя по истечении определенного периода бездействия.

**Настройка времени ожидания сеанса и фирменной символики для портала самообслуживания**

1.  Чтобы установить время ожидания для сеанса конечного пользователя, запустите **Диспетчер служб**IIS или запустите **inetmgr.exe**.

2.  Перейдите к **сайтам** &gt; **Администрирование и наблюдение за** &gt; **Selfservice** &gt; **ASP.NET** &gt; **сеанса**и измените значение **времени ожидания** в разделе **"Параметры cookie** " на количество минут, после которого заканчивается срок действия сеанса портала самообслуживания конечных пользователей. Значение по умолчанию — 5. Чтобы отключить этот параметр, чтобы время ожидания не существовало, установите для него значение **0**.

3.  Чтобы настроить элементы фирменной символики для портала самообслуживания, запустите **Диспетчер служб**IIS или запустите **inetmgr.exe**.

4.  Перейдите к **сайтам** &gt; **Администрирование и наблюдение за** &gt; **Selfservice** &gt; **параметрами приложений**Microsoft BitLocker.

5.  В столбце **имя** выберите элемент, который нужно изменить, и измените значение по умолчанию, чтобы оно отражало имя, которое вы хотите использовать. В следующей таблице перечислены значения, которые можно установить.

    **Осторожны**  
    Не изменяйте значение в столбце имя (CompanyName), так как это приводит к прекращению работы портала самообслуживания.



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



## Статьи по теме


[Развертывание инфраструктуры сервера MBAM 2.0 Server](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









