---
title: Управление конфигурациями UE-V 2.x
description: Управление конфигурациями UE-V 2.x
author: dansimp
ms.assetid: e2332eca-a9cd-4446-8f7c-d17058b03466
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20d5d2942dbd805a4054a9431b237c821cbb70fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827382"
---
# <span data-ttu-id="9b643-103">Управление конфигурациями UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="9b643-103">Manage Configurations for UE-V 2.x</span></span>


<span data-ttu-id="9b643-104">На протяжении всего жизненного цикла Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 или 2,1 SP1 вы должны управлять конфигурацией агента UE-V и управлять местами хранения для ресурсов, таких как файлы пакета параметров.</span><span class="sxs-lookup"><span data-stu-id="9b643-104">In the course of the Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 lifecycle, you have to manage the configuration of the UE-V Agent and also manage storage locations for resources such as settings package files.</span></span> <span data-ttu-id="9b643-105">Возможно, потребуется выполнить другие задачи, например настроить центр настройки компании, чтобы определить способ взаимодействия пользователей с UE-V.</span><span class="sxs-lookup"><span data-stu-id="9b643-105">You might have to perform other tasks, for example, configuring the Company Settings Center to define how users interact with UE-V.</span></span> <span data-ttu-id="9b643-106">В следующих разделах приведены рекомендации по управлению этими ресурсами UE-V.</span><span class="sxs-lookup"><span data-stu-id="9b643-106">The following topics provide guidance for managing these UE-V resources.</span></span>

## <span data-ttu-id="9b643-107">Настройка UE-V 2. x с помощью объектов групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b643-107">Configuring UE-V 2.x by using Group Policy Objects</span></span>


<span data-ttu-id="9b643-108">Вы можете использовать объекты групповой политики для изменения параметров, определяющих способ синхронизации параметров UE-V на компьютерах.</span><span class="sxs-lookup"><span data-stu-id="9b643-108">You can use Group Policy Objects to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="9b643-109">Настройка UE-V 2. x с объектами групповой политики</span><span class="sxs-lookup"><span data-stu-id="9b643-109">Configuring UE-V 2.x with Group Policy Objects</span></span>](configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)

## <span data-ttu-id="9b643-110">Настройка UE-V 2. x с помощью System Center Configuration Manager 2012</span><span class="sxs-lookup"><span data-stu-id="9b643-110">Configuring UE-V 2.x with System Center Configuration Manager 2012</span></span>


<span data-ttu-id="9b643-111">Вы можете использовать SystemCenter2012 ConfigurationManager для управления агентом UE-V с помощью пакета конфигурации UE-V 2.</span><span class="sxs-lookup"><span data-stu-id="9b643-111">You can use SystemCenter2012 ConfigurationManager to manage the UE-V Agent by using the UE-V 2 Configuration Pack.</span></span>

[<span data-ttu-id="9b643-112">Настройка UE-V 2. x с помощью System Center Configuration Manager 2012</span><span class="sxs-lookup"><span data-stu-id="9b643-112">Configuring UE-V 2.x with System Center Configuration Manager 2012</span></span>](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)

## <span data-ttu-id="9b643-113">Администрирование UE-V 2. x с помощью PowerShell и WMI</span><span class="sxs-lookup"><span data-stu-id="9b643-113">Administering UE-V 2.x with PowerShell and WMI</span></span>


<span data-ttu-id="9b643-114">UE-V предоставляет командлеты Windows PowerShell, которые помогают администраторам выполнять различные задачи UE-V.</span><span class="sxs-lookup"><span data-stu-id="9b643-114">UE-V provides Windows PowerShell cmdlets, which can help administrators perform various UE-V tasks.</span></span>

[<span data-ttu-id="9b643-115">Администрирование UE-V 2. x с помощью Windows PowerShell и WMI</span><span class="sxs-lookup"><span data-stu-id="9b643-115">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

## <span data-ttu-id="9b643-116">Настройка центра параметров компании для UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="9b643-116">Configuring the Company Settings Center for UE-V 2.x</span></span>


<span data-ttu-id="9b643-117">Вы можете настроить центр параметров компании, установленный с помощью UE-V Agent, чтобы определить способ взаимодействия пользователей с UE-V.</span><span class="sxs-lookup"><span data-stu-id="9b643-117">You can configure the Company Settings Center that is installed by using the UE-V Agent to define how users interact with UE-V.</span></span>

[<span data-ttu-id="9b643-118">Настройка центра параметров компании для UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="9b643-118">Configuring the Company Settings Center for UE-V 2.x</span></span>](configuring-the-company-settings-center-for-ue-v-2x-both-uevv2.md)

## <span data-ttu-id="9b643-119">Примеры параметров конфигурации для UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="9b643-119">Examples of configuration settings for UE-V 2.x</span></span>


<span data-ttu-id="9b643-120">Ниже приведены некоторые примеры параметров конфигурации UE-V.</span><span class="sxs-lookup"><span data-stu-id="9b643-120">Here are some examples of UE-V configuration settings:</span></span>

-   <span data-ttu-id="9b643-121">**Путь к хранилищу параметров:** Указывает расположение общей папки, в которой хранятся параметры UE-V.</span><span class="sxs-lookup"><span data-stu-id="9b643-121">**Settings Storage Path:** Specifies the location of the file share that stores the UE-V settings.</span></span>

-   <span data-ttu-id="9b643-122">**Путь к каталогу шаблонов параметров:** Указывает путь в формате UNC (Universal Naming Convention), определяющий расположение, которое было проверено для новых шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="9b643-122">**Settings Template Catalog Path:** Specifies the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span>

-   <span data-ttu-id="9b643-123">**Зарегистрируйте шаблоны Microsoft:** Указывает, следует ли регистрировать шаблоны Microsoft по умолчанию во время установки.</span><span class="sxs-lookup"><span data-stu-id="9b643-123">**Register Microsoft Templates:** Specifies whether the default Microsoft templates should be registered during installation.</span></span>

-   <span data-ttu-id="9b643-124">**Метод синхронизации:** Указывает, использует ли UE-V поставщик синхронизации, или "нет".</span><span class="sxs-lookup"><span data-stu-id="9b643-124">**Synchronization Method:** Specifies whether UE-V uses the sync provider or "none".</span></span> <span data-ttu-id="9b643-125">"SyncProvider" поддерживает компьютеры, отключенные от сети.</span><span class="sxs-lookup"><span data-stu-id="9b643-125">The "SyncProvider" supports computers that are disconnected from the network.</span></span> <span data-ttu-id="9b643-126">"Нет" применяется, если компьютер всегда подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="9b643-126">"None" applies when the computer is always connected to the network.</span></span> <span data-ttu-id="9b643-127">Дополнительные сведения о методе Sync можно найти в статьях [методы синхронизации для UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="9b643-127">For more information about the Sync Method, see [Sync Methods for UE-V 2.x](sync-methods-for-ue-v-2x-both-uevv2.md).</span></span>

-   <span data-ttu-id="9b643-128">**Время ожидания синхронизации:** Указывает время ожидания компьютера (в миллисекундах), по истечении которого приложение извлекает пользовательские параметры из места хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="9b643-128">**Synchronization Timeout:** Specifies the number of milliseconds that the computer waits before time-out when it retrieves the user settings from the settings storage location.</span></span>

-   <span data-ttu-id="9b643-129">**Включение синхронизации:** Указывает, включена или отключена синхронизация параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="9b643-129">**Synchronization Enable:** Specifies whether the UE-V settings synchronization is enabled or disabled.</span></span>

-   <span data-ttu-id="9b643-130">**Максимальный размер пакета:** Задает размер порогового значения файла пакета параметров в байтах, по пропуске которого агент UE-V сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9b643-130">**Maximum Package Size:** Specifies a settings package file threshold size in bytes at which the UE-V Agent reports a warning.</span></span>

-   <span data-ttu-id="9b643-131">**Не синхронизировать параметры приложения для Windows:** Указывает, что UE-V не должен синхронизировать приложения для Windows.</span><span class="sxs-lookup"><span data-stu-id="9b643-131">**Don’t Sync Windows App Settings:** Specifies that UE-V should not synchronize Windows apps.</span></span>

-   <span data-ttu-id="9b643-132">**Включение и отключение уведомления о первом использовании:** Указывает, будет ли UE-v выводить диалоговое окно при первом запуске агента UE-V на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="9b643-132">**Enable/Disable First Use Notification:** Specifies whether UE-V displays a dialog box the first time that the UE-V Agent runs on a user’s computer.</span></span>

-   <span data-ttu-id="9b643-133">**Значок включения и отключения панели задач:** Указывает, отображается ли UE-V значок в области уведомлений и каких-либо связанных с ним уведомлений.</span><span class="sxs-lookup"><span data-stu-id="9b643-133">**Enable/Disable Tray Icon:** Specifies whether UE-V displays an icon in the notification area and any notifications associated with it.</span></span> <span data-ttu-id="9b643-134">Значок содержит ссылку на центр параметров компании.</span><span class="sxs-lookup"><span data-stu-id="9b643-134">The icon provides a link to the Company Settings Center.</span></span>

-   <span data-ttu-id="9b643-135">**Гиперссылка для настраиваемого контакта:** Определяет путь, текст и описание для гиперссылки на **контактные данные** в центре параметров компании.</span><span class="sxs-lookup"><span data-stu-id="9b643-135">**Custom Contact IT Hyperlink:** Defines the path, text, and description for the **Contact IT** hyperlink in the Company Settings Center.</span></span>






## <span data-ttu-id="9b643-136">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9b643-136">Related topics</span></span>


[<span data-ttu-id="9b643-137">Администрирование UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="9b643-137">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="9b643-138">Развертывание необходимых компонентов для UE-v 2.x</span><span class="sxs-lookup"><span data-stu-id="9b643-138">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="9b643-139">Развертывание UE-V 2. x для настраиваемых приложений</span><span class="sxs-lookup"><span data-stu-id="9b643-139">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





