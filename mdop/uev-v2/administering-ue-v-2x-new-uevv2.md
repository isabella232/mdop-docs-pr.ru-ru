---
title: Администрирование UE-V 2. x
description: Администрирование UE-V 2. x
author: dansimp
ms.assetid: 996e4797-8383-4627-b714-24a84c907798
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2674f6ace80672c1e89bb4f9c765b56f260c3bc0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825672"
---
# <span data-ttu-id="85506-103">Администрирование UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-103">Administering UE-V 2.x</span></span>


<span data-ttu-id="85506-104">После развертывания Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 или 2,1 SP1 вы должны иметь возможность выполнять различные задачи администрирования, такие как управление конфигурацией агента UE-V и восстановление утерянных настроек.</span><span class="sxs-lookup"><span data-stu-id="85506-104">After you have deployed Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you must be able to perform various ongoing administrative tasks, such as managing the configuration of the UE-V Agent and recovering lost settings.</span></span> <span data-ttu-id="85506-105">Эти задачи, описанные после установки, описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="85506-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="85506-106">Управление конфигурациями UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-106">Managing UE-V 2.x configurations</span></span>


<span data-ttu-id="85506-107">В ходе жизненного цикла UE-V вы должны управлять конфигурацией агента UE-V и управлять местами хранения для ресурсов, таких как файлы пакета параметров.</span><span class="sxs-lookup"><span data-stu-id="85506-107">In the course of the UE-V lifecycle, you have to manage the configuration of the UE-V Agent and also manage storage locations for resources such as settings package files.</span></span>

[<span data-ttu-id="85506-108">Управление конфигурациями UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="85506-108">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

## <span data-ttu-id="85506-109">Работа с пользовательскими шаблонами UE-V и генератором UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-109">Working with custom UE-V templates and the UE-V 2.x Generator</span></span>


<span data-ttu-id="85506-110">В этом разделе приводятся инструкции по использованию генератора UE-V и управлению пользовательскими шаблонами расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="85506-110">This topic provides instructions for how to use the UE-V Generator and manage custom settings location templates.</span></span>

[<span data-ttu-id="85506-111">Работа с пользовательскими шаблонами UE-V 2. x и генератором UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-111">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

## <span data-ttu-id="85506-112">Резервное копирование и восстановление параметров приложения и Windows, синхронизированных с UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-112">Backup and restore application and Windows settings that are synchronized with UE-V 2.x</span></span>


<span data-ttu-id="85506-113">Инструментарий управления Windows (WMI) и функции Windows PowerShell для UE-V предоставляют возможность восстанавливать пакеты параметров.</span><span class="sxs-lookup"><span data-stu-id="85506-113">Windows Management Instrumentation (WMI) and Windows PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="85506-114">Используя команды WMI и Windows PowerShell, вы можете восстановить исходное состояние приложений и Windows, а также восстановить дополнительные параметры, когда пользователь применяет новое устройство.</span><span class="sxs-lookup"><span data-stu-id="85506-114">By using WMI and Windows PowerShell commands, you can restore application and Windows settings to their original state and restore additional settings when a user adopts a new device.</span></span>

[<span data-ttu-id="85506-115">Управление административными резервными копиями и восстановлением в UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-115">Manage Administrative Backup and Restore in UE-V 2.x</span></span>](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md)

## <span data-ttu-id="85506-116">Изменение частоты выполнения запланированных задач UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-116">Changing the frequency of UE-V 2.x scheduled tasks</span></span>


<span data-ttu-id="85506-117">Вы можете настроить запланированные задачи, которые управляют тем, как UE-V проверяет новые или обновленные параметры или обновляет пользовательские шаблоны расположения параметров в каталоге шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="85506-117">You can configure the scheduled tasks that manage when UE-V checks for new or updated settings or for updated custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="85506-118">Изменение частоты выполнения запланированных задач UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-118">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

## <span data-ttu-id="85506-119">Миграция пакетов параметров UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-119">Migrating UE-V 2.x settings packages</span></span>


<span data-ttu-id="85506-120">Вы можете переместить пакеты параметров пользователя при переходе на новый сервер или в целях резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="85506-120">You can relocate the user settings packages either when they migrate to a new server or for backup purposes.</span></span>

[<span data-ttu-id="85506-121">Миграция пакетов параметров UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-121">Migrating UE-V 2.x Settings Packages</span></span>](migrating-ue-v-2x-settings-packages-both-uevv2.md)

## <span data-ttu-id="85506-122">Использование UE-V 2. x с приложениями Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="85506-122">Using UE-V 2.x with Application Virtualization applications</span></span>


<span data-ttu-id="85506-123">С помощью UE-V с Microsoft Application Virtualization (App-V) можно обмениваться параметрами между виртуальными приложениями и установленными приложениями на нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="85506-123">You can use UE-V with Microsoft Application Virtualization (App-V) to share settings between virtual applications and installed applications across multiple computers.</span></span>

[<span data-ttu-id="85506-124">Использование UE-V 2. x с приложениями Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="85506-124">Using UE-V 2.x with Application Virtualization Applications</span></span>](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md)

## <span data-ttu-id="85506-125">Другие ресурсы для этого продукта</span><span class="sxs-lookup"><span data-stu-id="85506-125">Other resources for this product</span></span>


-   [<span data-ttu-id="85506-126">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-126">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="85506-127">Начало работы с UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="85506-127">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="85506-128">Подготовка к развертыванию UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-128">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="85506-129">Устранение неполадок UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85506-129">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="85506-130">Технический справочник по UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="85506-130">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





