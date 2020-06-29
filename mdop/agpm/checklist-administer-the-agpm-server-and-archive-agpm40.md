---
title: Контрольный список для управления сервером и архивацией в РАСШИРЕНном
description: Контрольный список для управления сервером и архивацией в РАСШИРЕНном
author: dansimp
ms.assetid: d9c60203-90c2-48a7-9318-197e0ec5038b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0e464dafa68b9d93c5a1051c986a0efde4702c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819122"
---
# <span data-ttu-id="3422c-103">Контрольный список: администрирование сервера и архива AGPM</span><span class="sxs-lookup"><span data-stu-id="3422c-103">Checklist: Administer the AGPM Server and Archive</span></span>


<span data-ttu-id="3422c-104">В расширенном средстве управления групповыми политиками службы и архивация управляются администраторами РАСШИРЕНного управления правами (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="3422c-104">In Advanced Group Policy Management (AGPM), both the AGPM Service and the archive are managed by AGPM Administrators (Full Control).</span></span> <span data-ttu-id="3422c-105">Ниже приведены типичные задачи для администратора РАСШИРЕНного администрирования.</span><span class="sxs-lookup"><span data-stu-id="3422c-105">The following are typical tasks for an AGPM Administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3422c-106">Часто выполняемые задачи</span><span class="sxs-lookup"><span data-stu-id="3422c-106">Frequent Task</span></span></th>
<th align="left"><span data-ttu-id="3422c-107">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="3422c-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3422c-108">Передача доступа к объектам групповой политики (GPO) в архиве.</span><span class="sxs-lookup"><span data-stu-id="3422c-108">Delegate access to Group Policy Objects (GPOs) in the archive.</span></span></p></td>
<td align="left"><p><a href="delegate-domain-level-access-to-the-archive-agpm40.md" data-raw-source="[Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm40.md)"><span data-ttu-id="3422c-109">Предоставление доступа на уровне домена к архиву</span><span class="sxs-lookup"><span data-stu-id="3422c-109">Delegate Domain-Level Access to the Archive</span></span></a></p>
<p><a href="delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md" data-raw-source="[Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md)"><span data-ttu-id="3422c-110">Передача прав доступа для отдельного объекта групповой политики в архиве</span><span class="sxs-lookup"><span data-stu-id="3422c-110">Delegate Access to an Individual GPO in the Archive</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3422c-111">Создавайте резервные копии архива для обеспечения возможности восстановления после аварии.</span><span class="sxs-lookup"><span data-stu-id="3422c-111">Back up the archive to enable disaster recovery.</span></span></p></td>
<td align="left"><p><a href="back-up-the-archive-agpm40.md" data-raw-source="[Back Up the Archive](back-up-the-archive-agpm40.md)"><span data-ttu-id="3422c-112">Резервное копирование архива</span><span class="sxs-lookup"><span data-stu-id="3422c-112">Back Up the Archive</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3422c-113">Нечастые задачи</span><span class="sxs-lookup"><span data-stu-id="3422c-113">Infrequent Task</span></span></th>
<th align="left"><span data-ttu-id="3422c-114">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="3422c-114">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3422c-115">Восстановите архив из резервной копии, чтобы восстановить ее после аварии.</span><span class="sxs-lookup"><span data-stu-id="3422c-115">Restore the archive from a backup to recover from a disaster.</span></span></p></td>
<td align="left"><p><a href="restore-the-archive-from-a-backup-agpm40.md" data-raw-source="[Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md)"><span data-ttu-id="3422c-116">Восстановление архива из резервной копии</span><span class="sxs-lookup"><span data-stu-id="3422c-116">Restore the Archive from a Backup</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3422c-117">Переместите службу РАСШИРЕНного (или) архивации на другой сервер.</span><span class="sxs-lookup"><span data-stu-id="3422c-117">Move the AGPM Service, the archive, or both to a different server.</span></span></p></td>
<td align="left"><p><a href="move-the-agpm-server-and-the-archive-agpm40.md" data-raw-source="[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md)"><span data-ttu-id="3422c-118">Перемещение сервера и архива AGPM</span><span class="sxs-lookup"><span data-stu-id="3422c-118">Move the AGPM Server and the Archive</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3422c-119">Измените путь к архиву, учетную запись службы РАСШИРЕНного поиска и порт, на котором прослушивается служба РАСШИРЕНного выбора.</span><span class="sxs-lookup"><span data-stu-id="3422c-119">Change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span></p></td>
<td align="left"><p><a href="modify-the-agpm-service-agpm40.md" data-raw-source="[Modify the AGPM Service](modify-the-agpm-service-agpm40.md)"><span data-ttu-id="3422c-120">Изменение службы AGPM</span><span class="sxs-lookup"><span data-stu-id="3422c-120">Modify the AGPM Service</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3422c-121">Устранение распространенных проблем с сервером РАСШИРЕНного поиска.</span><span class="sxs-lookup"><span data-stu-id="3422c-121">Troubleshoot common problems with the AGPM Server.</span></span></p></td>
<td align="left"><p><a href="troubleshooting-agpm-agpm40.md" data-raw-source="[Troubleshooting AGPM](troubleshooting-agpm-agpm40.md)"><span data-ttu-id="3422c-122">Устранение неполадок AGPM</span><span class="sxs-lookup"><span data-stu-id="3422c-122">Troubleshooting AGPM</span></span></a></p>
<p><a href="configure-logging-and-tracing-agpm40.md" data-raw-source="[Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md)"><span data-ttu-id="3422c-123">Настройка ведения журнала и трассировки</span><span class="sxs-lookup"><span data-stu-id="3422c-123">Configure Logging and Tracing</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3422c-124">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="3422c-124">Additional references</span></span>

-   [<span data-ttu-id="3422c-125">Средство расширенного управления групповыми политиками 4.0</span><span class="sxs-lookup"><span data-stu-id="3422c-125">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





