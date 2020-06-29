---
title: Настройка уведомлений по электронной почте
description: Настройка уведомлений по электронной почте
author: dansimp
ms.assetid: 6e152de0-4376-4963-8d1a-3e7f5866d30f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e8d00c2446a0185de30bbd1f39a7e3eaf90080
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818979"
---
# <span data-ttu-id="b668a-103">Настройка уведомлений по электронной почте</span><span class="sxs-lookup"><span data-stu-id="b668a-103">Configure E-Mail Notification</span></span>


<span data-ttu-id="b668a-104">Когда редактор или рецензент пытается создать, развернуть или удалить объект групповой политики (GPO), запрос на это действие отправляется на заданный адрес электронной почты или адрес, чтобы утверждающий мог оценить запрос и реализовать или отменить его.</span><span class="sxs-lookup"><span data-stu-id="b668a-104">When an Editor or a Reviewer attempts to create, deploy, or delete a Group Policy object (GPO), a request for this action is sent to a designated e-mail address or addresses so that an Approver can evaluate the request and implement or deny it.</span></span> <span data-ttu-id="b668a-105">Вы определяете адрес электронной почты или адрес, на который отправляются уведомления, а также псевдоним, на который отправляются уведомления.</span><span class="sxs-lookup"><span data-stu-id="b668a-105">You determine the e-mail address or addresses to which notifications are sent, as well as the alias from which notifications are sent.</span></span>

<span data-ttu-id="b668a-106">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора РАСШИРЕНного управления правами (полного доступа) или необходимых разрешений в расширенном управлении групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="b668a-106">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="b668a-107">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="b668a-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="b668a-108">Настройка уведомления по электронной почте для РАСШИРЕНного</span><span class="sxs-lookup"><span data-stu-id="b668a-108">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="b668a-109">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="b668a-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="b668a-110">В области сведений откройте вкладку **Делегирование домена** .</span><span class="sxs-lookup"><span data-stu-id="b668a-110">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="b668a-111">В поле **от** введите псевдоним электронной почты для расширенного ключа, из которого нужно отправить уведомления.</span><span class="sxs-lookup"><span data-stu-id="b668a-111">In the **From** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="b668a-112">В поле **Кому** введите разделенный запятыми список адресов электронной почты утверждающих, которые должны принимать запросы на утверждение.</span><span class="sxs-lookup"><span data-stu-id="b668a-112">In the **To** field, type a comma-delimited list of e-mail addresses of Approvers who should receive requests for approval.</span></span>

5.  <span data-ttu-id="b668a-113">В поле **SMTP-сервер** введите допустимый почтовый SMTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="b668a-113">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="b668a-114">В полях **имя пользователя** и **пароль** введите учетные данные пользователя, у которого есть доступ к службе SMTP.</span><span class="sxs-lookup"><span data-stu-id="b668a-114">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="b668a-115">Нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="b668a-115">Click **Apply**.</span></span>

### <span data-ttu-id="b668a-116">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="b668a-116">Additional considerations</span></span>

-   <span data-ttu-id="b668a-117">По умолчанию для выполнения этой процедуры необходимо быть администратором РАСШИРЕНной версии (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="b668a-117">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="b668a-118">В частности, необходимо иметь **содержимое списка** и разрешения на **изменение параметров** домена.</span><span class="sxs-lookup"><span data-stu-id="b668a-118">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="b668a-119">Уведомление по электронной почте для РАСШИРЕНного доменных прав — это параметр уровня домена.</span><span class="sxs-lookup"><span data-stu-id="b668a-119">E-mail notification for AGPM is a domain-level setting.</span></span> <span data-ttu-id="b668a-120">Вы можете предоставить различные адреса электронной почты утверждающего или РАСШИРЕНного доступа к ним на вкладке **доменного делегирования** домена или использовать одни и те же адреса электронной почты во всей среде.</span><span class="sxs-lookup"><span data-stu-id="b668a-120">You can provide different Approver e-mail addresses or AGPM e-mail aliases on each domain's **Domain Delegation** tab, or use the same e-mail addresses throughout your environment.</span></span>

### <span data-ttu-id="b668a-121">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="b668a-121">Additional references</span></span>

-   [<span data-ttu-id="b668a-122">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="b668a-122">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





