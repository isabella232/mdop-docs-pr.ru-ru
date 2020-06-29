---
title: Настройка уведомлений по электронной почте
description: Настройка уведомлений по электронной почте
author: dansimp
ms.assetid: b32ce395-d1b9-4c5b-b765-97cdbf455f9e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0204f2bd3430fa47b785d13a73b107e311990b82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819002"
---
# <span data-ttu-id="e0441-103">Настройка уведомлений по электронной почте</span><span class="sxs-lookup"><span data-stu-id="e0441-103">Configure E-Mail Notification</span></span>


<span data-ttu-id="e0441-104">Когда редактор или рецензент пытается создать, развернуть или удалить объект групповой политики (GPO), запрос на это действие отправляется на заданный адрес электронной почты или адрес, чтобы утверждающий мог оценить запрос и реализовать или отменить его.</span><span class="sxs-lookup"><span data-stu-id="e0441-104">When an Editor or a Reviewer attempts to create, deploy, or delete a Group Policy Object (GPO), a request for this action is sent to a designated e-mail address or addresses so that an Approver can evaluate the request and implement or deny it.</span></span> <span data-ttu-id="e0441-105">Вы определяете адрес электронной почты или адрес, на который отправляются уведомления, а также псевдоним, на который отправляются уведомления.</span><span class="sxs-lookup"><span data-stu-id="e0441-105">You determine the e-mail address or addresses to which notifications are sent, as well as the alias from which notifications are sent.</span></span>

<span data-ttu-id="e0441-106">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора РАСШИРЕНного управления правами (полного доступа) или необходимых разрешений в расширенном управлении групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="e0441-106">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="e0441-107">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="e0441-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="e0441-108">Настройка уведомления по электронной почте для РАСШИРЕНного</span><span class="sxs-lookup"><span data-stu-id="e0441-108">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="e0441-109">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="e0441-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e0441-110">В области сведений откройте вкладку **Делегирование домена** .</span><span class="sxs-lookup"><span data-stu-id="e0441-110">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="e0441-111">В поле **из адреса электронной почты** введите псевдоним электронной почты для расширенного вида, из которого нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="e0441-111">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="e0441-112">В поле **адрес электронной почты** введите разделенный запятыми список адресов электронной почты утверждающих, которые должны принимать запросы на утверждение.</span><span class="sxs-lookup"><span data-stu-id="e0441-112">In the **To e-mail address** field, type a comma-delimited list of e-mail addresses of Approvers who should receive requests for approval.</span></span>

5.  <span data-ttu-id="e0441-113">В поле **SMTP-сервер** введите допустимый почтовый SMTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="e0441-113">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="e0441-114">В полях **имя пользователя** и **пароль** введите учетные данные пользователя, у которого есть доступ к службе SMTP.</span><span class="sxs-lookup"><span data-stu-id="e0441-114">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="e0441-115">Нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="e0441-115">Click **Apply**.</span></span>

### <span data-ttu-id="e0441-116">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="e0441-116">Additional considerations</span></span>

-   <span data-ttu-id="e0441-117">По умолчанию для выполнения этой процедуры необходимо быть администратором РАСШИРЕНной версии (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="e0441-117">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="e0441-118">В частности, необходимо иметь **содержимое списка** и разрешения на **изменение параметров** домена.</span><span class="sxs-lookup"><span data-stu-id="e0441-118">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="e0441-119">Уведомление по электронной почте для РАСШИРЕНного доменных прав — это параметр уровня домена.</span><span class="sxs-lookup"><span data-stu-id="e0441-119">E-mail notification for AGPM is a domain-level setting.</span></span> <span data-ttu-id="e0441-120">Вы можете предоставить различные адреса электронной почты утверждающего или РАСШИРЕНного доступа к ним на вкладке **доменного делегирования** домена или использовать одни и те же адреса электронной почты во всей среде.</span><span class="sxs-lookup"><span data-stu-id="e0441-120">You can provide different Approver e-mail addresses or AGPM e-mail aliases on each domain's **Domain Delegation** tab, or use the same e-mail addresses throughout your environment.</span></span>

-   <span data-ttu-id="e0441-121">По умолчанию сообщения электронной почты, отправленные в результате действий с помощью расширенного управления групповыми политиками, не шифруются.</span><span class="sxs-lookup"><span data-stu-id="e0441-121">By default, e-mail messages sent as a result of actions in Advanced Group Policy Management (AGPM) are not encrypted.</span></span> <span data-ttu-id="e0441-122">Однако вы можете настроить параметры безопасности электронной почты для РАСШИРЕНного доступа с помощью параметров реестра, чтобы указать, нужно ли использовать шифрование SSL (Secure Sockets Layer) и какой порт SMTP использовать.</span><span class="sxs-lookup"><span data-stu-id="e0441-122">However, you can configure e-mail security for AGPM using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span> <span data-ttu-id="e0441-123">Дополнительные сведения можно найти в разделе [Настройка безопасности электронной почты для расширенного доступа к](configure-e-mail-security-for-agpm-agpm30ops.md) данным</span><span class="sxs-lookup"><span data-stu-id="e0441-123">For more information, see [Configure E-Mail Security for AGPM](configure-e-mail-security-for-agpm-agpm30ops.md)</span></span>

### <span data-ttu-id="e0441-124">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="e0441-124">Additional references</span></span>

-   [<span data-ttu-id="e0441-125">Настройка средства расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="e0441-125">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





