---
title: Обнаружение изменений в сети, которые влияют на MED-V
description: Обнаружение изменений в сети, которые влияют на MED-V
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823372"
---
# Обнаружение изменений в сети, которые влияют на MED-V


В решении Microsoft Enterprise Virtualization (MED-V) 2,0 можно настроить среду для обнаружения некоторых изменений в сети, которые могут возникать после развертывания рабочих областей MED-V и которые могут повлиять на работу MED-V.

Эта функция включает компонент, который работает в операционной системе на виртуальной машине и уведомлен об изменениях конфигурации сети на главном компьютере. Она позволяет использовать нестандартное или другое приложение, работающее в гостевой учетной записи, для устранения проблем с конечными точками сети, к которым они разрешаются с помощью ESD или приложения.

**Примечание**  Эта функция доступна только в том случае, если виртуальная машина настроена для режима преобразования сетевых адресов (NAT). Если виртуальная машина настроена для режима моста, никакие изменения не генерируются.

 

В этом разделе приводятся сведения и инструкции, которые помогут вам отслеживать изменения в сети, которые могут повлиять на работу MED-V.

## Определение сетевых изменений для MED-V


После развертывания рабочих областей MED-V вы можете отслеживать изменения в некоторых конфигурациях сети, выполнив следующие действия:

1. Создайте MOF-файл, который будет искать изменения конфигурации сети, которые вы хотите отслеживать. В следующем коде показан пример MOF-файла, который можно создать.

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. Скомпилируйте MOF-файл.

3. Установите MOF-файл в гостевой учетной запись.

После установки MOF-файла вы можете создать подписку на события, подписку на создание, изменение или удаление событий инструментария управления Windows (WMI) для класса **CCM \ _NetworkAdapters** . Это обнаруживает следующие изменения узла:

Есть ли в сети изменения конфигурации, например изменения IP-адреса или сетевого адаптера?

Доступна ли сеть или недоступна?

Была ли сетевая настройка изменена с режима моста на режим NAT?

Была ли сетевая настройка изменена из режима преобразования сетевых адресов в режим моста?

Компонент MED-V на главном компьютере отслеживает эти изменения в сети и оповещает гостя об изменении. Компонент в гостевой системе создает экземпляр WMI для отслеживания изменений в рабочей области MED-V.

Созданная подписка на события обеспечивает уведомление в системе WMI, если выполняется одно или несколько из этих сетевых изменений: создание, изменение или удаление.

## Статьи по теме


[Мониторинг рабочих областей MED-V](monitor-med-v-workspaces.md)

[Управление параметрами рабочей области MED-V](manage-med-v-workspace-settings.md)

 

 





