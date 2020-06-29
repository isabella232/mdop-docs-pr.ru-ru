---
title: Управление параметрами рабочей области MED-V с помощью инструментария WMI
description: Управление параметрами рабочей области MED-V с помощью инструментария WMI
author: dansimp
ms.assetid: 05a665a3-2309-46c1-babb-a3e3bbb0b1f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e74e6fa4944ce0dacd5503baec73044b231abe83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826132"
---
# <span data-ttu-id="da587-103">Управление параметрами рабочей области MED-V с помощью инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="da587-103">Managing MED-V Workspace Settings by Using a WMI</span></span>


<span data-ttu-id="da587-104">Вы можете использовать инструментарий управления Windows (WMI) в Microsoft Enterprise Virtualization (MED-V) 2,0 для управления текущими параметрами конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da587-104">You can use Windows Management Instrumentation (WMI) in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 to manage your current configuration settings.</span></span>

## <span data-ttu-id="da587-105">Управление параметрами рабочей области для MED-V с помощью WMI</span><span class="sxs-lookup"><span data-stu-id="da587-105">To manage MED-V workspace settings with a WMI</span></span>


<span data-ttu-id="da587-106">С помощью средства обзора WMI вы можете просматривать и изменять параметры в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="da587-106">A WMI browsing tool lets you view and edit the settings in a MED-V workspace.</span></span> <span data-ttu-id="da587-107">Поставщик WMI реализуется с помощью инфраструктуры расширения поставщика WMI из Microsoft .NET Framework 3,5.</span><span class="sxs-lookup"><span data-stu-id="da587-107">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span>

<span data-ttu-id="da587-108">Поставщик WMI реализован в пространстве имен **root\\microsoft\\medv** и реализует **параметр**класса.</span><span class="sxs-lookup"><span data-stu-id="da587-108">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **Setting**.</span></span> <span data-ttu-id="da587-109">**Параметр** класса включает в себя свойства, соответствующие параметрам в системном реестре в разделе HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv в реестре.</span><span class="sxs-lookup"><span data-stu-id="da587-109">The class **Setting** contains properties that correspond to the settings in the system registry under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv registry key.</span></span>

<span data-ttu-id="da587-110">**Внимание!**  Средства обзора WMI можно использовать для удаления и изменения классов и экземпляров.</span><span class="sxs-lookup"><span data-stu-id="da587-110">**Caution** WMI browsing tools can be used to delete or modify classes and instances.</span></span> <span data-ttu-id="da587-111">Удаление или изменение определенных классов и экземпляров может привести к потере ценных данных, а также привести к непредсказуемому функционированию MED-V.</span><span class="sxs-lookup"><span data-stu-id="da587-111">Deleting or modifying certain classes and instances can result in the loss of valuable data and cause MED-V to function unpredictably.</span></span>

 

<span data-ttu-id="da587-112">Для просмотра и редактирования параметров конфигурации для MED-V можно использовать предпочтительный инструмент обзора WMI, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="da587-112">You can use your preferred WMI browsing tool to view and edit MED-V configuration settings by following these steps.</span></span>

1.  <span data-ttu-id="da587-113">Откройте предпочтительный инструмент обзора WMI с разрешениями администратора.</span><span class="sxs-lookup"><span data-stu-id="da587-113">Open your preferred WMI browsing tool with administrator permissions.</span></span>

2.  <span data-ttu-id="da587-114">Подключитесь к пространству имен **root\\microsoft\\medv**.</span><span class="sxs-lookup"><span data-stu-id="da587-114">Connect to the namespace **root\\microsoft\\medv**.</span></span>

3.  <span data-ttu-id="da587-115">Перечислите экземпляры, чтобы подключиться к запущенному экземпляру.</span><span class="sxs-lookup"><span data-stu-id="da587-115">Enumerate the instances to connect to the running instance.</span></span> <span data-ttu-id="da587-116">Вы хотите подключиться к экземпляру **параметра**класса.</span><span class="sxs-lookup"><span data-stu-id="da587-116">You want to connect to the instance of the class **Setting**.</span></span>

    <span data-ttu-id="da587-117">Откроется окно **редактора объектов** .</span><span class="sxs-lookup"><span data-stu-id="da587-117">An **Object Editor** window opens.</span></span> <span data-ttu-id="da587-118">Параметры конфигурации для MED-V перечислены в разделе **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="da587-118">The MED-V configuration settings are listed as **Properties**.</span></span>

<span data-ttu-id="da587-119">Выполните указанные ниже действия, чтобы изменить параметры конфигурации MED-V в WMI.</span><span class="sxs-lookup"><span data-stu-id="da587-119">Perform the following steps to edit a MED-V configuration setting in the WMI.</span></span>

1.  <span data-ttu-id="da587-120">В списке **свойств** в окне **редактора объектов** дважды щелкните имя параметра конфигурации, который вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="da587-120">In the list of **Properties** on the **Object Editor** window, double-click the name of the configuration setting you want to edit.</span></span> <span data-ttu-id="da587-121">Например, чтобы изменить параметры перенаправления URL-адресов для MED-V, дважды щелкните свойство **UxRedirectUrls**.</span><span class="sxs-lookup"><span data-stu-id="da587-121">For example, to edit MED-V URL redirection information, double-click the property **UxRedirectUrls**.</span></span>

    <span data-ttu-id="da587-122">Откроется окно **редактора свойств** .</span><span class="sxs-lookup"><span data-stu-id="da587-122">A **Property Editor** window opens.</span></span>

2.  <span data-ttu-id="da587-123">Измените значение, чтобы обновить сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da587-123">Edit the value to update the configuration information.</span></span> <span data-ttu-id="da587-124">Например, чтобы изменить параметры перенаправления URL-адресов для MED-V, добавьте или удалите веб-адрес в списке.</span><span class="sxs-lookup"><span data-stu-id="da587-124">For example, to edit MED-V URL redirection information, add or remove a web address in the list.</span></span>

3.  <span data-ttu-id="da587-125">Сохраните обновленные параметры свойств.</span><span class="sxs-lookup"><span data-stu-id="da587-125">Save the updated property settings.</span></span>

<span data-ttu-id="da587-126">После того как вы закончите просмотр или редактирование параметров конфигурации для MED-V, закройте средство просмотра WMI.</span><span class="sxs-lookup"><span data-stu-id="da587-126">After you have finished viewing or editing MED-V configuration settings, close the WMI browsing tool.</span></span>

<span data-ttu-id="da587-127">**Важно!**  В некоторых случаях для вступления в силу изменений параметров конфигурации для MED-V необходимо перезапустить рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="da587-127">**Important** In some cases, a restart of the MED-V workspace is required for changes to MED-V configuration settings to take effect.</span></span>

 

<span data-ttu-id="da587-128">В следующем коде показан MOF-файл, который определяет класс **параметров** .</span><span class="sxs-lookup"><span data-stu-id="da587-128">The following code shows the Managed Object Format (MOF) file that defines the **Setting** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

<span data-ttu-id="da587-129">Класс **Setting** наследуется от класса **ConfigValueProvider** .</span><span class="sxs-lookup"><span data-stu-id="da587-129">The **Setting** class inherits from the **ConfigValueProvider** class.</span></span> <span data-ttu-id="da587-130">В следующем коде показан MOF-файл, который определяет класс **ConfigValueProvider** .</span><span class="sxs-lookup"><span data-stu-id="da587-130">The following code shows the Managed Object Format (MOF) file that defines the **ConfigValueProvider** class.</span></span>

``` syntax
[abstract]
class ConfigValueProvider
{
                [write] string DiagEventLogLevel;
                [write] boolean FtsAddUserToAdminGroupEnabled;
                [write] string FtsComputerNameMask;
                [write] sint32 FtsDeleteVMStateTimeout;
                [write] sint32 FtsDetachVfdTimeout;
                [write] string FtsDialogUrl;
                [write] sint32 FtsExplorerTimeout;
                [write] string FtsFailureDialogMsg;
                [write] string FtsLogFilePaths[];
                [write] sint32 FtsMaxPostponeTime;
                [write] sint32 FtsMaxRetryCount;
                [write] string FtsMode;
                [write] sint32 FtsNonInteractiveRetryTimeoutInc;
                [write] sint32 FtsNonInteractiveTimeout;
                [write] string FtsPostponeUtcDateTimeLimit;
                [write] string FtsRetryDialogMsg;
                [write] boolean FtsSetComputerNameEnabled;
                [write] boolean FtsSetJoinDomainEnabled;
                [write] boolean FtsSetMachineObjectOUEnabled;
                [write] boolean FtsSetRegionalSettingsEnabled;
                [write] boolean FtsSetUserDataEnabled;
                [write] string FtsStartDialogMsg;
                [write] sint32 FtsTaskCancelTimeout;
                [write] sint32 FtsTaskVMTurnOffTimeout;
                [write] sint32 FtsUpgradeTimeout;
                [write] boolean UxAppPublishingEnabled;
                [write] boolean UxAudioSharingEnabled;
                [write] boolean UxClipboardSharingEnabled;
                [write] boolean UxCredentialCacheEnabled;
                [write] sint32 UxDialogTimeout;
                [write] sint32 UxHideVmTimeout;
                [write] boolean UxLogonStartEnabled;
                [write] boolean UxPrinterSharingEnabled;
                [write] sint32 UxRebootAbsoluteDelayTimeout;
                [write] string UxRedirectUrls[];
                [write] boolean UxShowExit;
                [write] boolean UxSmartCardLogonEnabled;
                [write] boolean UxSmartCardSharingEnabled;
                [write] boolean UxUSBDeviceSharingEnabled;
                [write] string VmCloseAction;
                [write] sint32 VmGuestMemFromHostMem[];
                [write] sint32 VmGuestUpdateDuration;
                [write] string VmGuestUpdateTime;
                [write] sint32 VmHostMemToGuestMem[];
                [write] boolean VmHostMemToGuestMemCalcEnabled;
                [write] sint32 VmMemory;
                [write] boolean VmMultiUserEnabled;
                [write] string VmNetworkingMode;
                [write] sint32 VmTaskTimeout;
};
```

## <span data-ttu-id="da587-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="da587-131">Related topics</span></span>


[<span data-ttu-id="da587-132">Управление параметрами конфигурации рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="da587-132">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="da587-133">Управление параметрами рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="da587-133">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





