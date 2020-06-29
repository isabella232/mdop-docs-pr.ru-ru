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
# Настройка торговой марки и времени ожидания сеанса портала самообслуживания


После настройки портала самообслуживания вы можете использовать в качестве фирменного названия название компании, URL-адрес службы поддержки и текст "Примечание". Вы также можете изменить время ожидания сеанса, чтобы завершить сеанс пользователя после определенного периода бездействия.

**Примечание.**  
Вы также можете навести фирменный портал самообслуживания с помощью командлета Windows PowerShell **Enable-MbamWebApplication** или мастера настройки сервера MBAM. Инструкции по использованию мастера приведены [в разделе Настройка веб-приложений MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).



**Примечание.**  
В приведенных ниже инструкциях *Selfservice* является именем виртуального каталога по умолчанию для портала самообслуживания. Возможно, вы использовали другое имя, когда вы настроили портал самообслуживания.



**Настройка времени ожидания сеанса и фирменной символики для портала самообслуживания**

1.  Чтобы установить время ожидания для сеанса конечного пользователя, запустите **Диспетчер служб**IIS или запустите **inetmgr.exe**.

2.  Перейдите к **сайтам** &gt; **Администрирование и наблюдение за** &gt; **Selfservice** &gt; **ASP.NET** &gt; **сеанса**и измените значение **тайм-аута** в разделе **"Параметры cookie** " на количество минут, по прошествии которого истечет срок действия сеанса портала самообслуживания конечных пользователей. Значением по умолчанию является **5**. Чтобы отключить этот параметр, чтобы время ожидания не существовало, установите для него значение **0**.

3.  Чтобы настроить элементы фирменной символики для портала самообслуживания, запустите **Диспетчер служб** IIS или запустите **inetmgr.exe**.

4.  Перейдите к **сайтам** &gt; **Администрирование и наблюдение за** &gt; **Selfservice** &gt; **параметрами приложений**Microsoft BitLocker.

5.  В столбце **имя** выберите элемент, который нужно изменить, и измените значение по умолчанию, чтобы оно отражало имя, которое вы хотите использовать. В следующей таблице перечислены значения, которые можно установить.

    **Осторожны**  
    Не изменяйте значение в столбце имя (CompanyName \ *), так как это приведет к прекращению работы портала самообслуживания.



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





## Статьи по теме


[Настройка портала самообслуживания для организации](customizing-the-self-service-portal-for-your-organization.md)



## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





