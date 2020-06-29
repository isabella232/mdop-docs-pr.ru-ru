---
title: Администрирование UE-V 1.0
description: Администрирование UE-V 1.0
author: dansimp
ms.assetid: c399ae8d-c839-4f84-9bfc-adacd8f89f34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4dcafd1949dcedd195569dabb7540ce55a2f1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822699"
---
# <span data-ttu-id="14b9f-103">Администрирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="14b9f-103">Administering UE-V 1.0</span></span>


<span data-ttu-id="14b9f-104">После развертывания Microsoft User Experience Virtualization (UE-V) вы должны иметь возможность выполнять различные задачи администрирования.</span><span class="sxs-lookup"><span data-stu-id="14b9f-104">After you have deployed Microsoft User Experience Virtualization (UE-V), you must be able to perform various ongoing administrative tasks.</span></span> <span data-ttu-id="14b9f-105">Эти задачи, описанные после установки, описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="14b9f-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="14b9f-106">Управление ресурсами UE-V</span><span class="sxs-lookup"><span data-stu-id="14b9f-106">Managing UE-V resources</span></span>


<span data-ttu-id="14b9f-107">В ходе жизненного цикла UE-V вам потребуется управлять конфигурацией агента UE-V, а также управлять местами хранения для ресурсов, таких как пакеты параметров.</span><span class="sxs-lookup"><span data-stu-id="14b9f-107">In the course of the UE-V lifecycle, you will need to manage the configuration of the UE-V agent and also manage storage locations for resources such as settings packages.</span></span> <span data-ttu-id="14b9f-108">Для восстановления потерянных настроек может потребоваться выполнить другие задачи, такие как восстановление параметров пользователя в исходном состоянии с момента установки UE-V.</span><span class="sxs-lookup"><span data-stu-id="14b9f-108">You might need to perform other tasks such as to restore a user’s settings to their original state from before UE-V was installed in order to recover lost settings.</span></span> <span data-ttu-id="14b9f-109">В следующих разделах приведены рекомендации по управлению ресурсами UE-V.</span><span class="sxs-lookup"><span data-stu-id="14b9f-109">The following topics provide guidance for managing UE-V resources.</span></span>

### <span data-ttu-id="14b9f-110">Изменение частоты запланированных задач UE-V</span><span class="sxs-lookup"><span data-stu-id="14b9f-110">Changing the Frequency of UE-V Scheduled Tasks</span></span>

<span data-ttu-id="14b9f-111">Вы можете настроить запланированные задачи, которые управляют тем, как UE-V проверяет наличие новых, обновленных или удаленных настраиваемых шаблонов расположений параметров в каталоге шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="14b9f-111">You can configure the scheduled tasks that manage when UE-V checks for new, updated, or removed custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="14b9f-112">Изменение частоты выполнения запланированных задач UE-V</span><span class="sxs-lookup"><span data-stu-id="14b9f-112">Changing the Frequency of UE-V Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-scheduled-tasks.md)

### <a href="" id="sharing-settings-location-templates-with-the-ue-v-template-gallery-"></a><span data-ttu-id="14b9f-113">Отправка шаблонов расположения параметров в галерею шаблонов UE-V</span><span class="sxs-lookup"><span data-stu-id="14b9f-113">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>

<span data-ttu-id="14b9f-114">Коллекция шаблонов UE-V упрощает общий доступ к шаблонам расположений параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="14b9f-114">The UE-V template gallery facilitates the sharing of UE-V settings location templates.</span></span> <span data-ttu-id="14b9f-115">С помощью коллекции вы можете добавить шаблоны расположения параметров, чтобы поделиться ими с другими людьми и загрузить шаблоны, созданные другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="14b9f-115">The gallery enables you to upload your settings location templates to share with other people and to download templates that other people have created.</span></span>

[<span data-ttu-id="14b9f-116">Отправка шаблонов расположения параметров в галерею шаблонов UE-V</span><span class="sxs-lookup"><span data-stu-id="14b9f-116">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>](sharing-settings-location-templates-with-the-ue-v-template-gallery.md)

### <span data-ttu-id="14b9f-117">Восстановление параметров приложений и Windows, синхронизированных с UE-V 1,0</span><span class="sxs-lookup"><span data-stu-id="14b9f-117">Restoring application and Windows settings synchronized with UE-V 1.0</span></span>

<span data-ttu-id="14b9f-118">Функции WMI и PowerShell в UE-V предоставляют возможность восстанавливать пакеты параметров.</span><span class="sxs-lookup"><span data-stu-id="14b9f-118">WMI and PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="14b9f-119">Команды WMI и PowerShell позволяют восстановить параметры приложения и параметры Windows для значений параметров, которые были на компьютере при первом запуске приложения после запуска агента UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="14b9f-119">WMI and PowerShell commands allow you to restore application settings and Windows settings to the settings values that were on the computer the first time the application was started after the UE-V agent was launched.</span></span>

[<span data-ttu-id="14b9f-120">Восстановление параметров приложений и системы Windows, синхронизированных с UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="14b9f-120">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)

### <span data-ttu-id="14b9f-121">Настройка UE-V с помощью объектов групповой политики</span><span class="sxs-lookup"><span data-stu-id="14b9f-121">Configuring UE-V with Group Policy Objects</span></span>

<span data-ttu-id="14b9f-122">Вы можете использовать групповую политику для изменения параметров, определяющих способ синхронизации параметров UE-V на компьютерах.</span><span class="sxs-lookup"><span data-stu-id="14b9f-122">You can use Group Policy to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="14b9f-123">Настройка UE-V с помощью объектов групповой политики</span><span class="sxs-lookup"><span data-stu-id="14b9f-123">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

### <span data-ttu-id="14b9f-124">Администрирование UE-V с помощью PowerShell и инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="14b9f-124">Administering UE-V with PowerShell and WMI</span></span>

<span data-ttu-id="14b9f-125">PowerShell и WMI можно использовать для изменения параметров, определяющих способ синхронизации параметров на компьютерах с помощью UE-V.</span><span class="sxs-lookup"><span data-stu-id="14b9f-125">You can use PowerShell and WMI to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="14b9f-126">Управление агентом и пакетами UE-V 1.0 с помощью PowerShell и инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="14b9f-126">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

### <span data-ttu-id="14b9f-127">Перенос пакетов параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="14b9f-127">Migrating UE-V Settings Packages</span></span>

<span data-ttu-id="14b9f-128">Вы можете переместить пакеты параметров пользователя при переходе на новый сервер или в целях резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="14b9f-128">You can relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span>

[<span data-ttu-id="14b9f-129">Перенос пакетов параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="14b9f-129">Migrating UE-V Settings Packages</span></span>](migrating-ue-v-settings-packages.md)

## <span data-ttu-id="14b9f-130">Другие ресурсы для этого продукта</span><span class="sxs-lookup"><span data-stu-id="14b9f-130">Other resources for this product</span></span>


[<span data-ttu-id="14b9f-131">Операции в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="14b9f-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





