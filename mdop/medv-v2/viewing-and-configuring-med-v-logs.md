---
title: Просмотр и настройка журналов MED-V
description: Просмотр и настройка журналов MED-V
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823729"
---
# <span data-ttu-id="515e4-103">Просмотр и настройка журналов MED-V</span><span class="sxs-lookup"><span data-stu-id="515e4-103">Viewing and Configuring MED-V Logs</span></span>


<span data-ttu-id="515e4-104">При устранении неполадок и проблем, связанных с MED-V, может возникнуть необходимость в доступе к журналам событий MED-V или получить необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="515e4-104">When you are troubleshooting MED-V issues and problems, you may find it helpful or necessary to access the MED-V event logs.</span></span> <span data-ttu-id="515e4-105">Вы можете открыть средство просмотра событий для главного компьютера и гостевой виртуальной машины с помощью набора средств администрирования MED-V.</span><span class="sxs-lookup"><span data-stu-id="515e4-105">You can open Event Viewer for the host computer and the guest virtual machine by using the MED-V Administration Toolkit.</span></span> <span data-ttu-id="515e4-106">Вы также можете использовать инструментарий администрирования MED-V для настройки уровня ведения журнала событий MED-v.</span><span class="sxs-lookup"><span data-stu-id="515e4-106">You can also use the MED-V Administration Toolkit to set the logging level at which the MED-V event logs report MED-V events.</span></span>

<span data-ttu-id="515e4-107">Сведения о том, как открыть набор средств администрирования для MED-V, можно найти в разделе [Устранение неполадок с помощью средства администрирования для MED-v](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="515e4-107">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

## <span data-ttu-id="515e4-108">Просмотр журналов событий для MED-V</span><span class="sxs-lookup"><span data-stu-id="515e4-108">Viewing MED-V Event Logs</span></span>


<span data-ttu-id="515e4-109">В окне **набор средств администрирования для MED-V** щелкните элемент **события узла** , чтобы открыть окно просмотра событий на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="515e4-109">On the **MED-V Administration Toolkit** window, click **Host Events** to open the event viewer for the host computer.</span></span> <span data-ttu-id="515e4-110">Вы также можете щелкнуть элемент " **Гостевые мероприятия** ", чтобы открыть средство просмотра событий для гостевой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="515e4-110">Or, click **Guest Events** to open Event Viewer for the guest virtual machine.</span></span>

<span data-ttu-id="515e4-111">Откроется окно просмотра событий, в котором отображаются журналы событий, которые можно использовать для устранения проблем, которые могут возникнуть при развертывании и управлении MED-V.</span><span class="sxs-lookup"><span data-stu-id="515e4-111">Event Viewer opens and displays the corresponding event logs that you can use to troubleshoot the issues that you might encounter when you deploy or manage MED-V.</span></span> <span data-ttu-id="515e4-112">По умолчанию отображаются только ошибки и предупреждения.</span><span class="sxs-lookup"><span data-stu-id="515e4-112">By default, only errors and warnings are displayed.</span></span> <span data-ttu-id="515e4-113">Дополнительные сведения об определенных кодах событий и сообщениях можно найти в разделе [сообщения журнала событий MED-V](med-v-event-log-messages.md).</span><span class="sxs-lookup"><span data-stu-id="515e4-113">For more information about specific event IDs and messages, see [MED-V Event Log Messages](med-v-event-log-messages.md).</span></span>

<span data-ttu-id="515e4-114">**Примечание**  Конечные пользователи могут сохранять файлы журнала событий только в гостевой учетной записи только в том случае, если у них есть разрешения администратора.</span><span class="sxs-lookup"><span data-stu-id="515e4-114">**Note** End users can only save event log files in the guest if they have administrative permissions.</span></span>

 

### <span data-ttu-id="515e4-115">Открытие средства просмотра событий вручную на главном компьютере</span><span class="sxs-lookup"><span data-stu-id="515e4-115">To manually open the Event Viewer in the host computer</span></span>

1.  <span data-ttu-id="515e4-116">Нажмите кнопку **Пуск**и выберите пункт **Панель управления**, а затем — **Администрирование**.</span><span class="sxs-lookup"><span data-stu-id="515e4-116">Click **Start**, click **Control Panel**, and then click **Administrative Tools**.</span></span>

2.  <span data-ttu-id="515e4-117">Дважды щелкните **окно просмотра событий**и выберите пункт **журналы приложений и служб**.</span><span class="sxs-lookup"><span data-stu-id="515e4-117">Double-click **Event Viewer**, and then click **Applications and Services Logs**.</span></span>

3.  <span data-ttu-id="515e4-118">Дважды щелкните **MEDV**.</span><span class="sxs-lookup"><span data-stu-id="515e4-118">Double-click **MEDV**.</span></span>

## <span data-ttu-id="515e4-119">Настройка журналов событий для MED-V</span><span class="sxs-lookup"><span data-stu-id="515e4-119">Configuring MED-V Event Logs</span></span>


<span data-ttu-id="515e4-120">Вы можете задать уровень ведения журнала событий MED-V, выбрав соответствующий переключатель в средстве администрирования MED-V.</span><span class="sxs-lookup"><span data-stu-id="515e4-120">You can specify the MED-V event logging level by selecting the corresponding option button on the MED-V Administration Toolkit.</span></span> <span data-ttu-id="515e4-121">Вы можете решить, включают ли ведение журнала событий только ошибки, ошибки и предупреждения, а также ошибки, предупреждения и информационные сообщения.</span><span class="sxs-lookup"><span data-stu-id="515e4-121">You can decide whether event logging includes errors only, errors and warnings, or errors, warnings and informational messages.</span></span> <span data-ttu-id="515e4-122">Указанный уровень ведения журнала событий задается как на главном компьютере, так и на гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="515e4-122">The event logging level specified is set for both the host computer and the guest virtual machine.</span></span>

<span data-ttu-id="515e4-123">Вы также можете задать уровень ведения журнала событий, изменив значение в реестре EventLogLevel.</span><span class="sxs-lookup"><span data-stu-id="515e4-123">You can also specify the event logging level by editing the EventLogLevel registry value.</span></span> <span data-ttu-id="515e4-124">Дополнительные сведения можно найти в разделе [Управление параметрами конфигурации в рабочей области для MED-V](managing-med-v-workspace-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="515e4-124">For more information, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="515e4-125">**Примечание**  Уровень, указанный в окне **набора средств администрирования для MED-v** , применим для будущего ведения журнала событий MED-v.</span><span class="sxs-lookup"><span data-stu-id="515e4-125">**Note** The level you specify on the **MED-V Administration Toolkit** window applies to future MED-V event logging.</span></span> <span data-ttu-id="515e4-126">Если вы установили уровень захвата всех ошибок, предупреждений и информационных сообщений, журналы событий заполняются быстрее, а старые события удаляются.</span><span class="sxs-lookup"><span data-stu-id="515e4-126">If you set the level to capture all errors, warnings, and informational messages, then the event logs fill more quickly and older events are removed.</span></span>

 

## <span data-ttu-id="515e4-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="515e4-127">Related topics</span></span>


[<span data-ttu-id="515e4-128">Перезапуск и сброс рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="515e4-128">Restarting and Resetting a MED-V Workspace</span></span>](restarting-and-resetting-a-med-v-workspace.md)

[<span data-ttu-id="515e4-129">Просмотр конфигураций рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="515e4-129">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





