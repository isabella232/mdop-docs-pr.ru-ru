---
title: Контрольный список пост-установки App-V
description: Контрольный список пост-установки App-V
author: dansimp
ms.assetid: 74db297e-a744-4287-bcc6-0e096ca8b57a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79728bd2043076b20eb37ba0b1fa6f834a0d94bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819802"
---
# <span data-ttu-id="fd966-103">Контрольный список пост-установки App-V</span><span class="sxs-lookup"><span data-stu-id="fd966-103">App-V Postinstallation Checklist</span></span>


<span data-ttu-id="fd966-104">В приведенном ниже контрольном списке представлен высокоуровневый список элементов, которые необходимо учитывать и описаны действия, которые необходимо выполнить после установки сервера управления Microsoft Application Virtualization (App-V), потокового сервера App-V и настольного клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="fd966-104">The following checklist provides a high-level list of items to consider and outlines the steps you should take after you have completed the installation of the Microsoft Application Virtualization (App-V) Management Server, App-V Streaming Server, and the App-V Desktop Client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fd966-105">Шаг</span><span class="sxs-lookup"><span data-stu-id="fd966-105">Step</span></span></th>
<th align="left"><span data-ttu-id="fd966-106">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="fd966-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fd966-107">Создание исключений брандмауэра для серверного сервера управления App-V или служб потокового сервера.</span><span class="sxs-lookup"><span data-stu-id="fd966-107">Create firewall exceptions for the App-V Management Server or Streaming Server services.</span></span></p></td>
<td align="left"><p><a href="configuring-the-firewall-for-the-app-v-servers.md" data-raw-source="[Configuring the Firewall for the App-V Servers](configuring-the-firewall-for-the-app-v-servers.md)"><span data-ttu-id="fd966-108">Настройка брандмауэра для серверов App-V Server</span><span class="sxs-lookup"><span data-stu-id="fd966-108">Configuring the Firewall for the App-V Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fd966-109">Убедитесь, что система App-V работает правильно, публикуя, проstreaming и проверяя приложение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fd966-109">Verify that the App-V system is functioning correctly by publishing, streaming, and testing the default application.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-the-default-application.md" data-raw-source="[How to Install and Configure the Default Application](how-to-install-and-configure-the-default-application.md)"><span data-ttu-id="fd966-110">Установка и настройка приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fd966-110">How to Install and Configure the Default Application</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fd966-111">Настройте клиент App-V на использование потокового сервера App-V или другого сервера для потоковой передачи данных с помощью <strong> </strong> параметров APPLICATIONSOURCEROOT, <strong> IconSourceRoot </strong> и <strong> OSDSourceRoot </strong> .</span><span class="sxs-lookup"><span data-stu-id="fd966-111">Configure the App-V Client to use the App-V Streaming Server or other server for streaming by means of the <strong>ApplicationSourceRoot</strong>, <strong>IconSourceRoot</strong>, and <strong>OSDSourceRoot</strong> settings.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-client-for-application-package-retrieval.md" data-raw-source="[How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md)"><span data-ttu-id="fd966-112">Настройка клиента для получения пакетов приложений</span><span class="sxs-lookup"><span data-stu-id="fd966-112">How to Configure the Client for Application Package Retrieval</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fd966-113">Узнайте, как использовать файл. msi для упорядоченных пакетов приложений для автономного развертывания.</span><span class="sxs-lookup"><span data-stu-id="fd966-113">Understand how to use the .msi file version of sequenced application packages for offline deployment.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-virtual-application-on-the-client.md" data-raw-source="[How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md)"><span data-ttu-id="fd966-114">Публикация виртуального приложения на клиенте</span><span class="sxs-lookup"><span data-stu-id="fd966-114">How to Publish a Virtual Application on the Client</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fd966-115">Необязательно Настройте зеркальное отображение базы данных SQL Server для базы данных App-V.</span><span class="sxs-lookup"><span data-stu-id="fd966-115">(Optional) Configure SQL Server database mirroring for the App-V database.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md" data-raw-source="[How to Configure Microsoft SQL Server Mirroring Support for App-V](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)"><span data-ttu-id="fd966-116">Настройка поддержки зеркального отображения Microsoft SQL Server для App-V</span><span class="sxs-lookup"><span data-stu-id="fd966-116">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fd966-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="fd966-117">Related topics</span></span>


[<span data-ttu-id="fd966-118">Контрольные списки развертывания и обновления Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="fd966-118">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





