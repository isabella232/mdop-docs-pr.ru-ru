---
title: Настройка сервера MED-V Server в режиме кластера
description: Настройка сервера MED-V Server в режиме кластера
author: dansimp
ms.assetid: 41f0b2a3-4ce9-48e1-a6fb-4c13c4228515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddb7dd5af65d8a465c5c1884bb27a3027621bac1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826719"
---
# Настройка сервера MED-V Server в режиме кластера


Сервер MED-V можно настроить в кластерном режиме. В режиме кластеризации используются два сервера, и все файлы, определенные как взаимозависимые с обоими серверами, размещаются в файловой системе. Сервер обращается к файлам из файловой системы вместо того, чтобы хранить их локально.

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**Настройка сервера MED-V в кластерном режиме**

1.  Установите и настройте MED-V на одном из серверов.

2.  Создавайте общую сеть в централизованном расположении, где все серверы смогут получать к нему доступ.

3.  Скопируйте содержимое папки * &lt; installDir &gt; /Servers/ConfigurationServer* в общую сеть.

4.  Установите сервер MED-V на всех назначенных серверах.

5.  В общей сети назначьте полный доступ всем системным учетным записям на сервере MED-V.

6.  На каждом сервере выполните указанные ниже действия.

    1.  В файле * &lt; InstallDir &gt; /Servers/ServerConfiguration.xml* задайте для параметра * &lt; StorePath &gt; * значение "общий сетевой путь".

    2.  Скопируйте файл * &lt; InstsallDir &gt; /Servers/KeyPair.xml* с исходного сервера на все серверы MED-V.

    3.  Перезапустите службу MED-V.

**Примечание**  Если у всех серверов есть одинаковые локальные параметры (такие как порты для прослушивания, сервер IIS, разрешения на управление, база данных отчетов и т. д.), * &lt; &gt; ServerSettings.xml/Servers/installDir* также могут совместно использовать все серверы.

 

## Статьи по теме


[Планирование и проектирование инфраструктуры MED-V](med-v-infrastructure-planning-and-design.md)

 

 





