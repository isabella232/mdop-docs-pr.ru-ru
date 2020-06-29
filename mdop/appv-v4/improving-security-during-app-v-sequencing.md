---
title: Повышение уровня безопасности во время виртуализации App-V
description: Повышение уровня безопасности во время виртуализации App-V
author: dansimp
ms.assetid: f30206dd-5749-4a27-bbaf-61fc21b9c663
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba97c334c4ac9a928fee3d69c265c12e82e43619
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816359"
---
# <span data-ttu-id="37d63-103">Повышение уровня безопасности во время виртуализации App-V</span><span class="sxs-lookup"><span data-stu-id="37d63-103">Improving Security During App-V Sequencing</span></span>


<span data-ttu-id="37d63-104">Упаковка приложений для последовательности — это самая крупная задача в инфраструктуре App-V.</span><span class="sxs-lookup"><span data-stu-id="37d63-104">Packaging applications for sequencing is the largest ongoing task in an App-V infrastructure.</span></span> <span data-ttu-id="37d63-105">Так как эта задача будет продолжена, следует тщательно рассмотреть вопрос создания политик и процедур для выполнения виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="37d63-105">Because this task is ongoing, you should carefully consider creating policies and procedures to follow when sequencing applications.</span></span> <span data-ttu-id="37d63-106">В App-V 4.5 в процессе последовательности можно записывать списки управления доступом (ACL) для файлов ресурсов виртуализированного приложения.</span><span class="sxs-lookup"><span data-stu-id="37d63-106">In App-V4.5, during sequencing, you can capture Access Control Lists (ACLs) on the file assets of the virtualized application.</span></span>

## <span data-ttu-id="37d63-107">Поиск вирусов в секвенсоре</span><span class="sxs-lookup"><span data-stu-id="37d63-107">Virus Scanning on the Sequencer</span></span>


<span data-ttu-id="37d63-108">Рекомендуется установить программное обеспечение для сканирования на компьютер виртуализации, а затем проверить компьютер на наличие вирусов и вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="37d63-108">It is a best practice to install the scanning software on the sequencing computer and then scan the computer for viruses and malware.</span></span> <span data-ttu-id="37d63-109">После того как компьютер, на котором ведется виртуализация, просканирует и освобождает любые вирусы или вредоносные программы, отключите антивирусную программу, в том числе все программы обнаружения вирусов и вредоносных программ, на компьютере виртуализации, прежде чем выполнять виртуализацию приложений.</span><span class="sxs-lookup"><span data-stu-id="37d63-109">After the sequencing computer is scanned and free of any viruses or malware, disable the scanning software, including all antivirus and malware detection software, on the sequencing computer before sequencing any applications.</span></span> <span data-ttu-id="37d63-110">Это ускоряет процесс упорядочивания и предотвращает обнаружение компонентов программного обеспечения сканирования во время их последовательного и включенного в виртуальный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="37d63-110">This speeds the sequencing process and prevents the scanning software components from being detected during sequencing and included in the virtual application package.</span></span>

## <span data-ttu-id="37d63-111">Сбор списков ACL для файлов (NTFS)</span><span class="sxs-lookup"><span data-stu-id="37d63-111">Capturing ACLs on Files (NTFS)</span></span>


<span data-ttu-id="37d63-112">Секвенсор захватывает разрешения NTFS для файлов, отслеживаемых на этапе установки виртуализации (ACL).</span><span class="sxs-lookup"><span data-stu-id="37d63-112">The Sequencer captures NTFS permissions (the ACLs) for the files that are monitored during the sequencing installation phase.</span></span> <span data-ttu-id="37d63-113">(Перед выпуском приложения App-V 4.5 списки ACL не были собраны как часть процесса упорядочения.) Эта новая функция позволяет запускать определенные приложения для пользователей с низким уровнем разрешений, которые обычно требуют прав администратора.</span><span class="sxs-lookup"><span data-stu-id="37d63-113">(Before the release of App-V4.5, ACLs were not captured as part of the sequencing process.) This new feature enables certain applications to run for users with a low level of permission that would normally require Administrative privileges.</span></span>

<span data-ttu-id="37d63-114">Эта функция также позволяет инженеру по виртуализации фиксировать параметры безопасности, определенные поставщиком.</span><span class="sxs-lookup"><span data-stu-id="37d63-114">This feature also enables the sequencing engineer to capture the security settings identified by the vendor.</span></span> <span data-ttu-id="37d63-115">Невозможность применения параметров, рекомендованных поставщиком, может оставить приложение открытым для атак или несанкционированного использования пользователями.</span><span class="sxs-lookup"><span data-stu-id="37d63-115">Failing to apply the settings recommended by the vendor could leave the application open to attack or misuse by users.</span></span> <span data-ttu-id="37d63-116">Сведения о том, следует ли развертывать приложение с открытыми ACL, можно получить в группе поддержка приложений или поставщик программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="37d63-116">For information about whether or not you should deploy an application with open ACLs, refer to your application support group or the software vendor.</span></span>

<span data-ttu-id="37d63-117">**Важно!**  Несмотря на то, что секвенсор захватывает списки ACL NTFS при наблюдении за фазой установки последовательности, она не захватывает ACL для реестра.</span><span class="sxs-lookup"><span data-stu-id="37d63-117">**Important** Although the sequencer captures the NTFS ACLs while monitoring the installation phase of sequencing, it does not capture the ACLs for the registry.</span></span> <span data-ttu-id="37d63-118">Пользователи имеют полный доступ ко всем разделам реестра для виртуальных приложений, кроме служб.</span><span class="sxs-lookup"><span data-stu-id="37d63-118">Users have full access to all registry keys for virtual applications except for services.</span></span> <span data-ttu-id="37d63-119">Тем не менее, если пользователь изменяет реестр виртуального приложения, это изменение хранится в определенном месте ( `uservol_sftfs_v1.pkg` ) и не влияет на других пользователей.</span><span class="sxs-lookup"><span data-stu-id="37d63-119">However, if a user modifies the registry of a virtual application, that change is stored in a specific location (`uservol_sftfs_v1.pkg`) and won’t affect other users.</span></span>

 

<span data-ttu-id="37d63-120">На этапе установки инженер по виртуализации может при необходимости изменить разрешения файлов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="37d63-120">During the installation phase, a sequencing engineer can modify the default permissions of the files if necessary.</span></span> <span data-ttu-id="37d63-121">После того как процесс упорядочивания завершится, но перед сохранением пакета инженер по виртуализации сможет выбрать дескрипторы безопасности, захваченные на этапе установки.</span><span class="sxs-lookup"><span data-stu-id="37d63-121">After the sequencing process is complete, but before saving the package, the sequencing engineer can then choose to enforce security descriptors that were captured during the installation phase.</span></span> <span data-ttu-id="37d63-122">Рекомендуется применять дескрипторы безопасности, если ни одно из других решений не позволяет приложению правильно работать после виртуализированного.</span><span class="sxs-lookup"><span data-stu-id="37d63-122">It is a best practice to enforce security descriptors if no other solution allows the application to run properly once virtualized.</span></span>

 

 





