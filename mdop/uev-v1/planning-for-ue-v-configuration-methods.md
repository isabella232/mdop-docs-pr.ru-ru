---
title: Планирование методов конфигурации UE-V
description: Планирование методов конфигурации UE-V
author: dansimp
ms.assetid: 57bce7ab-1be5-434b-9ee5-c96026bbe010
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4894644d72392ae984d0de290bf634e137d5b85e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827092"
---
# <span data-ttu-id="cc944-103">Планирование методов конфигурации UE-V</span><span class="sxs-lookup"><span data-stu-id="cc944-103">Planning for UE-V Configuration Methods</span></span>


<span data-ttu-id="cc944-104">Конфигурации Microsoft User Experience Virtualization (UE-V) определяют, как синхронизируются параметры в рамках всего предприятия.</span><span class="sxs-lookup"><span data-stu-id="cc944-104">Microsoft User Experience Virtualization (UE-V) configurations determine how settings are synchronized throughout the enterprise.</span></span> <span data-ttu-id="cc944-105">В этой статье объясняется, как создавать конфигурации UE-V, чтобы помочь вам сформулировать план конфигурации, который наилучшим образом соответствует вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="cc944-105">This topic describes how UE-V configurations are created to help you formulate a configuration plan that best meets your business requirements.</span></span>

## <span data-ttu-id="cc944-106">Методы настройки для UE-V</span><span class="sxs-lookup"><span data-stu-id="cc944-106">Configuration methods for UE-V</span></span>


<span data-ttu-id="cc944-107">Агенты UE-V можно настроить до, во время и после установки агента в зависимости от используемого метода конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cc944-107">You can configure UE-V before, during, or after agent installation, depending on the configuration method that you use.</span></span>

<span data-ttu-id="cc944-108">**Групповая политика:** существующая инфраструктура групповой политики может использоваться для настройки UE-v до или после развертывания агента UE-v.</span><span class="sxs-lookup"><span data-stu-id="cc944-108">**Group Policy:** existing Group Policy infrastructure can be used to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="cc944-109">Шаблон UE-V ADMX обеспечивает централизованное управление общими параметрами конфигурации агента UE-V и включает параметры для настройки синхронизации UE-V.</span><span class="sxs-lookup"><span data-stu-id="cc944-109">The UE-V ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span> <span data-ttu-id="cc944-110">Сетевые среды, использующие групповую политику, могут предварительно настроить UE-V в предустановке агента.</span><span class="sxs-lookup"><span data-stu-id="cc944-110">Network environments that use Group Policy can preconfigure UE-V in anticipation of agent deployment.</span></span>

[<span data-ttu-id="cc944-111">Настройка UE-V с помощью объектов групповой политики</span><span class="sxs-lookup"><span data-stu-id="cc944-111">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

[<span data-ttu-id="cc944-112">Установка шаблонов ADMX групповой политики UE-V</span><span class="sxs-lookup"><span data-stu-id="cc944-112">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="cc944-113">**Установка командной строки или пакетного сценария:** параметры, которые используются вместе с развертыванием агента UE-v, позволяют настраивать многие параметры UE-v.</span><span class="sxs-lookup"><span data-stu-id="cc944-113">**Command-line or Batch Script Installation:** parameters that are used with the deployment of the UE-V Agent allow the configuration of many UE-V settings.</span></span> <span data-ttu-id="cc944-114">Электронные системы распространения программного обеспечения, такие как System Center Configuration Manager, используют эти параметры для настройки клиентов при развертывании и установке программного обеспечения агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="cc944-114">Electronic software distribution systems, such as System Center Configuration Manager, use these parameters to configure their clients when deploying and installing the UE-V Agent software.</span></span> <span data-ttu-id="cc944-115">Список параметров установки и примеров сценариев установки можно найти в разделе [развертывание агента UE-V](deploying-the-ue-v-agent.md).</span><span class="sxs-lookup"><span data-stu-id="cc944-115">For a list of installation parameters and sample installation scripts, see [Deploying the UE-V Agent](deploying-the-ue-v-agent.md).</span></span>

<span data-ttu-id="cc944-116">**PowerShell и WMI:** команды с сценариями с помощью POWERSHELL или WMI можно использовать для изменения конфигураций после установки UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="cc944-116">**PowerShell and WMI:** scripted commands using PowerShell or WMI can be used to modify configurations after the UE-V Agent has been installed.</span></span> <span data-ttu-id="cc944-117">Список команд PowerShell и WMI можно найти в разделе [Управление агентом UE-V 1,0 и пакетами с помощью PowerShell и WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="cc944-117">For a list of PowerShell and WMI commands, see [Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span></span>

<span data-ttu-id="cc944-118">**Изменение параметров реестра.** Параметры UE-V сохраняются в реестре и могут быть изменены с помощью любого средства, которое может изменять параметры реестра, например regedit.</span><span class="sxs-lookup"><span data-stu-id="cc944-118">**Edit Registry Settings:** UE-V settings are stored in the registry and can be modified by using any tool that can modify registry settings, such as RegEdit.</span></span>

<span data-ttu-id="cc944-119">**Примечание**  Изменение реестра может привести к потере данных или перестает отвечать на запросы компьютера.</span><span class="sxs-lookup"><span data-stu-id="cc944-119">**Note** Registry modification can result in data loss or the computer becoming unresponsive.</span></span> <span data-ttu-id="cc944-120">Мы рекомендуем использовать другие методы настройки.</span><span class="sxs-lookup"><span data-stu-id="cc944-120">We recommend that you use other configuration methods.</span></span>

 

### <span data-ttu-id="cc944-121">Параметры конфигурации UE-V</span><span class="sxs-lookup"><span data-stu-id="cc944-121">UE-V configuration settings</span></span>

<span data-ttu-id="cc944-122">Ниже приведены примеры параметров конфигурации UE-V.</span><span class="sxs-lookup"><span data-stu-id="cc944-122">The following are examples of UE-V configuration settings:</span></span>

-   <span data-ttu-id="cc944-123">**Параметр путь к хранилищу:** определяет расположение общей папки, в которой ХРАНЯТСЯ параметры UE-V.</span><span class="sxs-lookup"><span data-stu-id="cc944-123">**Setting Storage Path:** specifies the location of the file share that stores the UE-V settings.</span></span>

-   <span data-ttu-id="cc944-124">**Путь к каталогу шаблонов параметров:** определяет путь в формате UNC, определяющий расположение, которое было проверено для новых шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="cc944-124">**Settings Template Catalog Path:** specifies the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span>

-   <span data-ttu-id="cc944-125">**Зарегистрируйте Microsoft Templates:** определяет, следует ли регистрировать шаблоны Microsoft по умолчанию во время установки.</span><span class="sxs-lookup"><span data-stu-id="cc944-125">**Register Microsoft Templates:** specifies whether the default Microsoft templates should be registered during installation.</span></span>

-   <span data-ttu-id="cc944-126">**Метод синхронизации:** определяет, используется ли функция автономных файлов Windows для поддержки в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="cc944-126">**Synchronization Method:** specifies whether the Windows Offline Files feature is used for offline support.</span></span>

-   <span data-ttu-id="cc944-127">**Время ожидания синхронизации:** определяет время ожидания (в миллисекундах), по истечении которого компьютер будет получать данные о пользователях из места хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="cc944-127">**Synchronization Timeout:** specifies the number of milliseconds that the computer waits before timeout when retrieving the user settings from the settings storage location.</span></span>

-   <span data-ttu-id="cc944-128">**Включение синхронизации:** определяет, включена или отключена синхронизация параметров ue-V.</span><span class="sxs-lookup"><span data-stu-id="cc944-128">**Synchronization Enable:** specifies whether the UE-V settings synchronization is enabled or disabled.</span></span>

-   <span data-ttu-id="cc944-129">**Максимальный размер пакета:** определяет размер порогового значения файла пакета параметров в байтах, при которых агент UE-V выводит предупреждение.</span><span class="sxs-lookup"><span data-stu-id="cc944-129">**Maximum Package Size:** specifies a settings package file threshold size in bytes at which the UE-V Agent reports a warning.</span></span>

## <span data-ttu-id="cc944-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="cc944-130">Related topics</span></span>


[<span data-ttu-id="cc944-131">Планирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="cc944-131">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="cc944-132">Планирование конфигурации UE-V</span><span class="sxs-lookup"><span data-stu-id="cc944-132">Planning for UE-V Configuration</span></span>](planning-for-ue-v-configuration.md)

 

 





