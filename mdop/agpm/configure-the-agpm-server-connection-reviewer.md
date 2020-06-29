---
title: Настройка подключения к серверу AGPM
description: Настройка подключения к серверу AGPM
author: dansimp
ms.assetid: 74e8f348-a8ed-4d69-a8e0-9c974aaeca2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83a2437ee8c2fe562141ff167cb85c6a06b7cefe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818919"
---
# <span data-ttu-id="06c1d-103">Настройка подключения к серверу AGPM</span><span class="sxs-lookup"><span data-stu-id="06c1d-103">Configure the AGPM Server Connection</span></span>


<span data-ttu-id="06c1d-104">Чтобы убедиться в том, что вы подключены к правильному центральному архиву, проверьте конфигурацию подключения сервера расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="06c1d-104">To ensure that you are connected to the correct central archive, review the configuration of the AGPM Server connection.</span></span> <span data-ttu-id="06c1d-105">Если Администратор расширенного управления групповыми политиками (полный доступ) не настроил подключение к серверу РАСШИРЕНного доступа, его необходимо настроить вручную.</span><span class="sxs-lookup"><span data-stu-id="06c1d-105">If an AGPM Administrator (Full Control) has not configured the AGPM Server connection for you, then you must manually configure it.</span></span>

**<span data-ttu-id="06c1d-106">Выбор сервера РАСШИРЕНного выбора</span><span class="sxs-lookup"><span data-stu-id="06c1d-106">To select an AGPM Server</span></span>**

1.  <span data-ttu-id="06c1d-107">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="06c1d-107">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="06c1d-108">В области сведений перейдите на вкладку **сервер расширенного сервера** :</span><span class="sxs-lookup"><span data-stu-id="06c1d-108">In the details pane, click the **AGPM Server** tab:</span></span>

    -   <span data-ttu-id="06c1d-109">Если параметры на вкладке **сервер расширенного управления групповыми политиками** недоступны, они были централизованно настроены АДМИНИСТРАТОРом расширенного управления правами.</span><span class="sxs-lookup"><span data-stu-id="06c1d-109">If the options on the **AGPM Server** tab are unavailable, they have been centrally configured by an AGPM Administrator.</span></span>

    -   <span data-ttu-id="06c1d-110">Если доступны параметры на вкладке **сервер расширенного** доступа к сети, введите полное имя компьютера для сервера расширенного доступа (например, Server.contoso.com) и порт, прослушиваемый службой расширенного доступа (по умолчанию используется порт 4600).</span><span class="sxs-lookup"><span data-stu-id="06c1d-110">If the options on the **AGPM Server** tab are available, type the fully-qualified computer name for the AGPM Server (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span> <span data-ttu-id="06c1d-111">Нажмите кнопку **Применить**, а затем — **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="06c1d-111">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="06c1d-112">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="06c1d-112">Additional considerations</span></span>

-   <span data-ttu-id="06c1d-113">Выбранные серверы РАСШИРЕНного доступа определяют, какие GPO отображаются на вкладке " **содержимое** " и к чему применяются параметры вкладки **делегирования домена** .</span><span class="sxs-lookup"><span data-stu-id="06c1d-113">The AGPM Servers selected determine which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="06c1d-114">Если вы не управляете централизованно с помощью административного шаблона, каждый администратор групповой политики должен настроить этот параметр таким образом, чтобы он указывал на сервер РАСШИРЕНного управления правами для домена.</span><span class="sxs-lookup"><span data-stu-id="06c1d-114">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

### <span data-ttu-id="06c1d-115">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="06c1d-115">Additional references</span></span>

-   [<span data-ttu-id="06c1d-116">Выполнение задач редактора</span><span class="sxs-lookup"><span data-stu-id="06c1d-116">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="06c1d-117">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="06c1d-117">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="06c1d-118">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="06c1d-118">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 





