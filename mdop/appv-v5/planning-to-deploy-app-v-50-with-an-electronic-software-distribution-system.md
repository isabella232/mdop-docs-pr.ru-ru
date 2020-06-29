---
title: Планирование развертывания App-V 5.0 с помощью системы электронного распространения программного обеспечения
description: Планирование развертывания App-V 5.0 с помощью системы электронного распространения программного обеспечения
author: dansimp
ms.assetid: 8cd3f1fb-b84e-4260-9e72-a14d01e7cadf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ca441820be7e6759e65902aea18b2db7f989e8f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813405"
---
# <span data-ttu-id="c629c-103">Планирование развертывания App-V 5.0 с помощью системы электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="c629c-103">Planning to Deploy App-V 5.0 with an Electronic Software Distribution System</span></span>


<span data-ttu-id="c629c-104">Если вы используете электронную систему распространения программного обеспечения для развертывания пакетов App-V, ознакомьтесь с приведенными ниже замечаниями по планированию.</span><span class="sxs-lookup"><span data-stu-id="c629c-104">If you are using an electronic software distribution system to deploy App-V packages, review the following planning considerations.</span></span> <span data-ttu-id="c629c-105">Дополнительные сведения об использовании System Center Configuration Manager для развертывания App-V можно найти [в разделе Общие сведения об управлении приложениями в Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).</span><span class="sxs-lookup"><span data-stu-id="c629c-105">For information about using System Center Configuration Manager to deploy App-V, see [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).</span></span>

<span data-ttu-id="c629c-106">Ознакомьтесь со следующими параметрами требований к компонентам и архитектуре, которые применяются при использовании ESD для развертывания пакетов App-V.</span><span class="sxs-lookup"><span data-stu-id="c629c-106">Review the following component and architecture requirements options that apply when you use an ESD to deploy App-V packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c629c-107">Требования к развертыванию или параметр</span><span class="sxs-lookup"><span data-stu-id="c629c-107">Deployment requirement or option</span></span></th>
<th align="left"><span data-ttu-id="c629c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c629c-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c629c-109">Сервер управления App-V, база данных управления и сервер публикаций не требуются.</span><span class="sxs-lookup"><span data-stu-id="c629c-109">The App-V Management server, Management database, and Publishing server are not required.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c629c-110">Эти функции обрабатываются реализованным решением ESD.</span><span class="sxs-lookup"><span data-stu-id="c629c-110">These functions are handled by the implemented ESD solution.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c629c-111">Вы можете развернуть сервер отчетов App-V и базу данных отчетов рядом друг с другом с помощью ESD.</span><span class="sxs-lookup"><span data-stu-id="c629c-111">You can deploy the App-V Reporting server and Reporting database side by side with the ESD.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c629c-112">Параллельное развертывание позволяет собирать данные и создавать отчеты.</span><span class="sxs-lookup"><span data-stu-id="c629c-112">The side-by-side deployment lets you to collect data and generate reports.</span></span></p>
<p><span data-ttu-id="c629c-113">Если вы включите клиент App-V для отправки сведений о отчете и не используете сервер отчетов App-V, данные отчетов хранятся в связанных XML-файлах.</span><span class="sxs-lookup"><span data-stu-id="c629c-113">If you enable the App-V client to send report information, and you are not using the App-V Reporting server, the reporting data is stored in associated .xml files.</span></span></p></td>
</tr>
</tbody>
</table>

 






 

 





