---
title: Резервное копирование и восстановление сервера MED-V Server
description: Резервное копирование и восстановление сервера MED-V Server
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823089"
---
# Резервное копирование и восстановление сервера MED-V Server


XML-файлы, расположенные на сервере, могут быть архивированы, а затем восстановлены в случае потери данных на сервере.

**Создание резервной копии сервера MED-V**

-   Создавайте резервные копии следующих файлов, расположенных в * &lt; installDir &gt; \\Servers\\ConfigurationServer*:

    **Примечание**  Если конфигурация по умолчанию была изменена, файлы могут храниться в другом расположении.

     

    -   ClientPolicy.xml

    -   ClientSettings.xml

    -   ConfigurationFiles.xml

    -   OrganizationPolicy.xml

    -   WorkspaceKeys.xml

    **Примечание**  Файл ServerSettings.xml также можно архивировать. Тем не менее, если определенная конфигурация была изменена (например, на исходном сервере, каталог виртуальных машин MED-V расположен в разделе "*C:\\Vms*", а такой каталог не существует на новом сервере), это может привести к возникновению ошибки.

     

**Восстановление сервера MED-V**

1.  Установите новый сервер MED-V.

2.  Скопируйте файлы резервной копии в следующий каталог:

    *&lt;InstallDir &gt; \\Servers\\ConfigurationServer*

3.  Перезапустите службу MED-V.

 

 





