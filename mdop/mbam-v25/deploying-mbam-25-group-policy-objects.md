---
title: Развертывание объектов групповой политики MBAM 2.5
description: Развертывание объектов групповой политики MBAM 2.5
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824389"
---
# <span data-ttu-id="27436-103">Развертывание объектов групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="27436-103">Deploying MBAM 2.5 Group Policy Objects</span></span>


<span data-ttu-id="27436-104">Чтобы развернуть MBAM, необходимо задать параметры групповой политики, определяющие параметры реализации MBAM для шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="27436-104">To deploy MBAM, you have to set Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="27436-105">Для выполнения этой задачи необходимо скопировать шаблоны групповой политики MBAM на сервер или рабочую станцию, которые могут выполнять консоль управления групповыми политиками (GPMC) или расширенное управление групповыми политиками, а затем изменить параметры.</span><span class="sxs-lookup"><span data-stu-id="27436-105">To complete this task, you must copy the MBAM Group Policy Templates to a server or workstation that are capable of running Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM), and then edit the settings.</span></span>

<span data-ttu-id="27436-106">**Важно!**  Не изменяйте параметры групповой политики в разделе " **Шифрование диска BitLocker** " или MBAM будут работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="27436-106">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="27436-107">При настройке параметров групповой политики на узле **MDOP MBAM (Управление BitLocker)** MBAM автоматически настраивает параметры **шифрования диска для BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="27436-107">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

## <span data-ttu-id="27436-108">Копирование шаблонов групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="27436-108">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="27436-109">Перед установкой клиента MBAM необходимо скопировать MBAM-специфические объекты групповой политики (GPO) на рабочую станцию управления.</span><span class="sxs-lookup"><span data-stu-id="27436-109">Before you install the MBAM Client, you must copy MBAM-specific Group Policy Objects (GPOs) to the Management Workstation.</span></span> <span data-ttu-id="27436-110">Эти GPO определяют параметры реализации MBAM для шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="27436-110">These GPOs define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="27436-111">Вы можете скопировать шаблоны групповой политики на любой сервер или рабочую станцию, которые поддерживаются в Windows Server или на клиентском компьютере, и смогли запустить консоль управления групповыми политиками или расширенное управление групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="27436-111">You can copy the Group Policy templates to any server or workstation that is a supported Windows server or client computer and that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="27436-112">Копирование шаблонов групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="27436-112">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

## <span data-ttu-id="27436-113">Изменение параметров объекта групповой политики MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="27436-113">Editing MBAM 2.0 GPO settings</span></span>


<span data-ttu-id="27436-114">После создания необходимых GPO необходимо развернуть параметры групповой политики MBAM на клиентских компьютерах своей организации.</span><span class="sxs-lookup"><span data-stu-id="27436-114">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span> <span data-ttu-id="27436-115">Для просмотра и создания объектов групповой политики необходимо установить консоль управления групповыми политиками (GPMC) или расширенное управление групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="27436-115">To view and create GPOs, you must have Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) installed.</span></span>

[<span data-ttu-id="27436-116">Изменение параметров групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="27436-116">Editing the MBAM 2.5 Group Policy Settings</span></span>](editing-the-mbam-25-group-policy-settings.md)

## <span data-ttu-id="27436-117">Отображение и скрытие панели управления MBAM на панели управления Windows</span><span class="sxs-lookup"><span data-stu-id="27436-117">Showing or hiding the MBAM Control Panel in Windows Control Panel</span></span>


<span data-ttu-id="27436-118">Поскольку MBAM позволяет настроить панель управления Windows BitLocker по умолчанию, вы также можете отобразить или скрыть панель управления по умолчанию для конечных пользователей с помощью параметров групповой политики.</span><span class="sxs-lookup"><span data-stu-id="27436-118">Since MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to show or hide the default BitLocker Control Panel from end users by using Group Policy settings.</span></span>

[<span data-ttu-id="27436-119">Скрытие элемента шифрования диска BitLocker по умолчанию на панели управления</span><span class="sxs-lookup"><span data-stu-id="27436-119">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## <span data-ttu-id="27436-120">Другие ресурсы по развертыванию объектов групповой политики MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="27436-120">Other Resources for deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="27436-121">Развертывание MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="27436-121">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

## <span data-ttu-id="27436-122">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="27436-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="27436-123">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="27436-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="27436-124">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="27436-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





