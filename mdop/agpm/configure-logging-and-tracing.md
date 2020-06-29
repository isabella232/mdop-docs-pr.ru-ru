---
title: Настройка ведения журнала и трассировки
description: Настройка ведения журнала и трассировки
author: dansimp
ms.assetid: 419231f9-e9db-4f91-a7cf-a0a73db25256
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa3dfa71edb25f6641ade595cd4469e846410ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818972"
---
# <span data-ttu-id="fcd77-103">Настройка ведения журнала и трассировки</span><span class="sxs-lookup"><span data-stu-id="fcd77-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="fcd77-104">Вы можете централизованно настроить дополнительные функции ведения журнала и трассировки для расширенного управления групповыми политиками (ГРУППОВое Управлениеми) с помощью административных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="fcd77-104">You can centrally configure optional logging and tracing for Advanced Group Policy Management (AGPM) using Administrative templates.</span></span>

<span data-ttu-id="fcd77-105">Для выполнения этих процедур требуется учетная запись пользователя с ролью администратора расширенного управления групповыми политиками (полного доступа), учетной записи пользователя утверждающего, который создал объект групповой политики, который использовался в этих процедурах, или учетной записи пользователя с необходимыми разрешениями для расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="fcd77-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures.</span></span> <span data-ttu-id="fcd77-106">Кроме того, для запуска ведения журнала на сервере с РАСШИРЕНным доступом к данным требуется учетная запись пользователя, имеющего доступ к серверу РАСШИРЕНного доступа.</span><span class="sxs-lookup"><span data-stu-id="fcd77-106">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="fcd77-107">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="fcd77-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="fcd77-108">Настройка ведения журнала и трассировки для РАСШИРЕНного протоколирования</span><span class="sxs-lookup"><span data-stu-id="fcd77-108">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="fcd77-109">В дереве **консоли управления групповыми политиками** измените объект групповой политики, который применяется ко всем администраторам групповых политик, для которых вы хотите включить ведение журнала и трассировку.</span><span class="sxs-lookup"><span data-stu-id="fcd77-109">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="fcd77-110">(Дополнительные сведения можно найти [в разделе изменение объекта групповой политики](editing-a-gpo.md).)</span><span class="sxs-lookup"><span data-stu-id="fcd77-110">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="fcd77-111">В **редакторе объектов групповой политики**выберите элементы **Конфигурация компьютера**, **Шаблоны администрирования**и **компоненты Windows**.</span><span class="sxs-lookup"><span data-stu-id="fcd77-111">In the **Group Policy Object Editor**, click **Computer Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="fcd77-112">Если в разделе **компоненты Windows**отсутствует **Расширенное** руководство, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="fcd77-112">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="fcd77-113">Щелкните правой кнопкой мыши **Административные шаблоны** и выберите команду **Добавить или удалить шаблоны**.</span><span class="sxs-lookup"><span data-stu-id="fcd77-113">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="fcd77-114">Нажмите кнопку **Добавить**, выберите элемент **расширенного формата ADMX** или для **расширенного**расширения (ADM), нажмите кнопку **Открыть**, а затем — **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="fcd77-114">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="fcd77-115">В разделе **компоненты Windows**дважды щелкните элемент **расширенной**учетной записью.</span><span class="sxs-lookup"><span data-stu-id="fcd77-115">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="fcd77-116">В области сведений дважды щелкните **ведение журнала расширенного протоколирования**.</span><span class="sxs-lookup"><span data-stu-id="fcd77-116">In the details pane, double-click **AGPM Logging**.</span></span>

6.  <span data-ttu-id="fcd77-117">В окне **Свойства ведения журнала расширенного протоколирования** выберите пункт **включена**и настройте уровень детализации для записи в журналах.</span><span class="sxs-lookup"><span data-stu-id="fcd77-117">In the **AGPM Logging Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

7.  <span data-ttu-id="fcd77-118">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fcd77-118">Click **OK**.</span></span>

8.  <span data-ttu-id="fcd77-119">Закройте **Редактор объектов групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="fcd77-119">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="fcd77-120">(Дополнительные сведения можно найти [в разделе Развертывание объекта групповой политики](deploy-a-gpo.md).) После обновления групповой политики необходимо перезапустить службу РАСШИРЕНного протоколирования, чтобы начать ведение журнала на сервере РАСШИРЕНного выбора.</span><span class="sxs-lookup"><span data-stu-id="fcd77-120">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) After Group Policy is updated, you must restart the AGPM Service to begin logging on the AGPM Server.</span></span> <span data-ttu-id="fcd77-121">Администраторы групповой политики должны закрыть и перезапустить консоль GPMC, чтобы начать ведение журнала на своих компьютерах.</span><span class="sxs-lookup"><span data-stu-id="fcd77-121">Group Policy administrators must close and restart the GPMC to begin logging on their computers.</span></span>

    <span data-ttu-id="fcd77-122">**Расположение файлов трассировки**:</span><span class="sxs-lookup"><span data-stu-id="fcd77-122">**Trace file locations**:</span></span>

    -   <span data-ttu-id="fcd77-123">Клиент:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="fcd77-123">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="fcd77-124">Сервер:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="fcd77-124">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="fcd77-125">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="fcd77-125">Additional considerations</span></span>

-   <span data-ttu-id="fcd77-126">Вы должны иметь возможность редактирования и развертывания объекта групповой политики, чтобы настроить ведение журнала и трассировку в РАСШИРЕНном состоянии.</span><span class="sxs-lookup"><span data-stu-id="fcd77-126">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="fcd77-127">Дополнительные сведения: [редактирование GPO](editing-a-gpo.md) и [Развертывание объекта групповой политики](deploy-a-gpo.md) .</span><span class="sxs-lookup"><span data-stu-id="fcd77-127">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

### <span data-ttu-id="fcd77-128">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="fcd77-128">Additional references</span></span>

-   [<span data-ttu-id="fcd77-129">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="fcd77-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





