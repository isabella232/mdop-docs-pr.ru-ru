---
title: Настройка ведения журнала и трассировки
description: Настройка ведения журнала и трассировки
author: dansimp
ms.assetid: 2418cb6a-7189-4080-8fe2-9c8d47dec62c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bfc56d418ae83cbc5db24246bfac057305629df7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818969"
---
# <span data-ttu-id="42beb-103">Настройка ведения журнала и трассировки</span><span class="sxs-lookup"><span data-stu-id="42beb-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="42beb-104">Вы можете централизованно настраивать дополнительные функции ведения журнала и трассировки с помощью административных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="42beb-104">You can centrally configure optional logging and tracing using Administrative templates.</span></span> <span data-ttu-id="42beb-105">Это может быть полезно при диагностике проблем, связанных с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="42beb-105">This may be helpful when diagnosing any problems related to Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="42beb-106">Для выполнения этих процедур требуется учетная запись пользователя с ролью администратора расширенного управления групповыми политиками (полного доступа), учетная запись пользователя утверждающего, который создал объект групповой политики (GPO) или учетную запись пользователя с необходимыми разрешениями для управления ГРУППОВыми политиками.</span><span class="sxs-lookup"><span data-stu-id="42beb-106">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account with the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="42beb-107">Кроме того, для запуска ведения журнала на сервере с РАСШИРЕНным доступом к данным требуется учетная запись пользователя, имеющего доступ к серверу РАСШИРЕНного доступа.</span><span class="sxs-lookup"><span data-stu-id="42beb-107">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="42beb-108">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="42beb-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="42beb-109">Настройка ведения журнала и трассировки для РАСШИРЕНного протоколирования</span><span class="sxs-lookup"><span data-stu-id="42beb-109">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="42beb-110">В дереве **консоли управления групповыми политиками** измените объект групповой политики, который применяется ко всем администраторам групповых политик, для которых вы хотите включить ведение журнала и трассировку.</span><span class="sxs-lookup"><span data-stu-id="42beb-110">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="42beb-111">(Дополнительные сведения можно найти [в разделе изменение объекта групповой политики](editing-a-gpo-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="42beb-111">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="42beb-112">В окне **редактора управления групповыми политиками** выберите пункты **Конфигурация компьютера**, **политики**, **Административные шаблоны**, **компоненты Windows**и **Расширенное**управление правами.</span><span class="sxs-lookup"><span data-stu-id="42beb-112">In the **Group Policy Management Editor** window, click **Computer Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="42beb-113">В области сведений дважды щелкните элемент **расширенного протоколирования: Настройка ведения журнала**.</span><span class="sxs-lookup"><span data-stu-id="42beb-113">In the details pane, double-click **AGPM: Configure logging**.</span></span>

4.  <span data-ttu-id="42beb-114">В окне **Свойства** щелкните **включить**и настройте уровень детализации для записи в журналах.</span><span class="sxs-lookup"><span data-stu-id="42beb-114">In the **Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

5.  <span data-ttu-id="42beb-115">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="42beb-115">Click **OK**.</span></span>

6.  <span data-ttu-id="42beb-116">Закройте окно **редактора управления групповыми политиками** .</span><span class="sxs-lookup"><span data-stu-id="42beb-116">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="42beb-117">(Дополнительные сведения можно найти [в разделе Развертывание объекта групповой политики](deploy-a-gpo-agpm40.md).) После обновления групповой политики необходимо перезапустить службу РАСШИРЕНного редактирования, чтобы запустить, изменить или остановить ведение журнала на сервере РАСШИРЕНного выбора.</span><span class="sxs-lookup"><span data-stu-id="42beb-117">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) After Group Policy is updated, you must restart the AGPM Service to start, modify, or stop logging on the AGPM Server.</span></span> <span data-ttu-id="42beb-118">Администраторы групповой политики должны закрыть и перезапустить GPMC, чтобы начать, изменить или прекратить ведение журнала на своих компьютерах.</span><span class="sxs-lookup"><span data-stu-id="42beb-118">Group Policy administrators must close and restart the GPMC to start, modify, or stop logging on their computers.</span></span>

    <span data-ttu-id="42beb-119">**Расположение файлов трассировки**:</span><span class="sxs-lookup"><span data-stu-id="42beb-119">**Trace file locations**:</span></span>

    -   <span data-ttu-id="42beb-120">Клиент:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="42beb-120">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="42beb-121">Сервер:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="42beb-121">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="42beb-122">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="42beb-122">Additional considerations</span></span>

-   <span data-ttu-id="42beb-123">Вы должны иметь возможность редактирования и развертывания объекта групповой политики, чтобы настроить ведение журнала и трассировку в РАСШИРЕНном состоянии.</span><span class="sxs-lookup"><span data-stu-id="42beb-123">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="42beb-124">Дополнительные сведения: [редактирование GPO](editing-a-gpo-agpm40.md) и [Развертывание объекта групповой политики](deploy-a-gpo-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="42beb-124">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

### <span data-ttu-id="42beb-125">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="42beb-125">Additional references</span></span>

-   [<span data-ttu-id="42beb-126">Настройка средства расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="42beb-126">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





