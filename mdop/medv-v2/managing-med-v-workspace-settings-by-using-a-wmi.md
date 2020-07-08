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
# Управление параметрами рабочей области MED-V с помощью инструментария WMI


Вы можете использовать инструментарий управления Windows (WMI) в Microsoft Enterprise Virtualization (MED-V) 2,0 для управления текущими параметрами конфигурации.

## Управление параметрами рабочей области для MED-V с помощью WMI


С помощью средства обзора WMI вы можете просматривать и изменять параметры в рабочей области MED-V. Поставщик WMI реализуется с помощью инфраструктуры расширения поставщика WMI из Microsoft .NET Framework 3,5.

Поставщик WMI реализован в пространстве имен **root\\microsoft\\medv** и реализует **параметр**класса. **Параметр** класса включает в себя свойства, соответствующие параметрам в системном реестре в разделе HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv в реестре.

**Внимание!**  Средства обзора WMI можно использовать для удаления и изменения классов и экземпляров. Удаление или изменение определенных классов и экземпляров может привести к потере ценных данных, а также привести к непредсказуемому функционированию MED-V.

 

Для просмотра и редактирования параметров конфигурации для MED-V можно использовать предпочтительный инструмент обзора WMI, выполнив указанные ниже действия.

1.  Откройте предпочтительный инструмент обзора WMI с разрешениями администратора.

2.  Подключитесь к пространству имен **root\\microsoft\\medv**.

3.  Перечислите экземпляры, чтобы подключиться к запущенному экземпляру. Вы хотите подключиться к экземпляру **параметра**класса.

    Откроется окно **редактора объектов** . Параметры конфигурации для MED-V перечислены в разделе **Свойства**.

Выполните указанные ниже действия, чтобы изменить параметры конфигурации MED-V в WMI.

1.  В списке **свойств** в окне **редактора объектов** дважды щелкните имя параметра конфигурации, который вы хотите изменить. Например, чтобы изменить параметры перенаправления URL-адресов для MED-V, дважды щелкните свойство **UxRedirectUrls**.

    Откроется окно **редактора свойств** .

2.  Измените значение, чтобы обновить сведения о конфигурации. Например, чтобы изменить параметры перенаправления URL-адресов для MED-V, добавьте или удалите веб-адрес в списке.

3.  Сохраните обновленные параметры свойств.

После того как вы закончите просмотр или редактирование параметров конфигурации для MED-V, закройте средство просмотра WMI.

**Важно!**  В некоторых случаях для вступления в силу изменений параметров конфигурации для MED-V необходимо перезапустить рабочую область MED-V.

 

В следующем коде показан MOF-файл, который определяет класс **параметров** .

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

Класс **Setting** наследуется от класса **ConfigValueProvider** . В следующем коде показан MOF-файл, который определяет класс **ConfigValueProvider** .

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

## Статьи по теме


[Управление параметрами конфигурации рабочей области MED-V](managing-med-v-workspace-configuration-settings.md)

[Управление параметрами рабочей области MED-V](manage-med-v-workspace-settings.md)

 

 





