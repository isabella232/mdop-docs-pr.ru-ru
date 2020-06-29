---
title: Настройка подключения к серверу AGPM
description: Настройка подключения к серверу AGPM
author: dansimp
ms.assetid: ae78dc74-111d-4509-b0a6-e8b8b451c22a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 50968d8b1b1eb5d464c6dbdb251354a9dc691d62
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819009"
---
# <span data-ttu-id="4dfbf-103">Настройка подключения к серверу AGPM</span><span class="sxs-lookup"><span data-stu-id="4dfbf-103">Configure an AGPM Server Connection</span></span>


<span data-ttu-id="4dfbf-104">Чтобы убедиться в том, что вы подключены к правильному центральному архиву, проверьте конфигурацию подключения сервера расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="4dfbf-104">To ensure that you are connected to the correct central archive, review the configuration of the AGPM Server connection.</span></span> <span data-ttu-id="4dfbf-105">Если Администратор расширенного управления групповыми политиками (полный доступ) не настроил соединение с сервером РАСШИРЕНного доступа, необходимо настроить его вручную.</span><span class="sxs-lookup"><span data-stu-id="4dfbf-105">If an AGPM Administrator (Full Control) has not configured an AGPM Server connection for you, then you must manually configure it.</span></span>

**<span data-ttu-id="4dfbf-106">Выбор сервера РАСШИРЕНного выбора</span><span class="sxs-lookup"><span data-stu-id="4dfbf-106">To select an AGPM Server</span></span>**

1.  <span data-ttu-id="4dfbf-107">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="4dfbf-107">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="4dfbf-108">В области сведений перейдите на вкладку **сервер расширенного сервера** :</span><span class="sxs-lookup"><span data-stu-id="4dfbf-108">In the details pane, click the **AGPM Server** tab:</span></span>

    -   <span data-ttu-id="4dfbf-109">Если параметры на вкладке **сервер расширенного управления групповыми политиками** недоступны, они были централизованно настроены АДМИНИСТРАТОРом расширенного управления правами.</span><span class="sxs-lookup"><span data-stu-id="4dfbf-109">If the options on the **AGPM Server** tab are unavailable, they have been centrally configured by an AGPM Administrator.</span></span>

    -   <span data-ttu-id="4dfbf-110">Если доступны параметры на вкладке **сервер расширенного** доступа к сети, введите полное имя компьютера для сервера расширенного доступа (например, Server.contoso.com) и порт, прослушиваемый службой расширенного доступа (по умолчанию используется порт 4600).</span><span class="sxs-lookup"><span data-stu-id="4dfbf-110">If the options on the **AGPM Server** tab are available, type the fully-qualified computer name for the AGPM Server (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span> <span data-ttu-id="4dfbf-111">Нажмите кнопку **Применить**, а затем — **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4dfbf-111">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="4dfbf-112">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="4dfbf-112">Additional considerations</span></span>

-   <span data-ttu-id="4dfbf-113">Выбранные серверы РАСШИРЕНного доступа определяют, какие GPO отображаются на вкладке " **содержимое** " и к чему применяются параметры вкладки **делегирования домена** .</span><span class="sxs-lookup"><span data-stu-id="4dfbf-113">The AGPM Servers selected determine which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="4dfbf-114">Если вы не управляете централизованно с помощью административного шаблона, каждый администратор групповой политики должен настроить этот параметр таким образом, чтобы он указывал на сервер РАСШИРЕНного управления правами для домена.</span><span class="sxs-lookup"><span data-stu-id="4dfbf-114">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

### <span data-ttu-id="4dfbf-115">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="4dfbf-115">Additional references</span></span>

-   [<span data-ttu-id="4dfbf-116">Выполнение задач редактора</span><span class="sxs-lookup"><span data-stu-id="4dfbf-116">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="4dfbf-117">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="4dfbf-117">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="4dfbf-118">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="4dfbf-118">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





