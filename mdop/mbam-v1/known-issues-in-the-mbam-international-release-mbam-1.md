---
title: Известные проблемы, связанные с международным выпуском MBAM
description: Известные проблемы, связанные с международным выпуском MBAM
author: dansimp
ms.assetid: bbf888dc-93c1-4323-b43c-0ded098e9b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af32551135ff297d25930f94b40bf04c0fcaaafe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825789"
---
# <span data-ttu-id="86538-103">Известные проблемы, связанные с международным выпуском MBAM</span><span class="sxs-lookup"><span data-stu-id="86538-103">Known Issues in the MBAM International Release</span></span>

<span data-ttu-id="86538-104">В этом разделе содержатся известные проблемы, возникающие при работе с международной выпуском Microsoft BitLocker (Администрирование и мониторинг) (MBAM).</span><span class="sxs-lookup"><span data-stu-id="86538-104">This section contains known issues for Microsoft BitLocker Administration and Monitoring (MBAM) International Release.</span></span>

## <span data-ttu-id="86538-105">Известные проблемы, связанные с международным выпуском MBAM</span><span class="sxs-lookup"><span data-stu-id="86538-105">Known Issues in the MBAM International Release</span></span>

### <span data-ttu-id="86538-106">В процессе установки не указывается обновление</span><span class="sxs-lookup"><span data-stu-id="86538-106">The Installation Process Does Not Specify Update</span></span>

<span data-ttu-id="86538-107">После обновления серверов и серверов мониторинга Microsoft BitLocker программа установки не будет находиться в состоянии установки обновления.</span><span class="sxs-lookup"><span data-stu-id="86538-107">Upon updating the Microsoft BitLocker Administration and Monitoring server or servers, the Setup program does not state that an update is being installed.</span></span>

<span data-ttu-id="86538-108">**Временное решение**: нет.</span><span class="sxs-lookup"><span data-stu-id="86538-108">**Workaround**: None.</span></span>

### <span data-ttu-id="86538-109">Сертификаты, используемые для роли сервера администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="86538-109">Certificates Used for the Administration and Monitoring Server Role</span></span>

<span data-ttu-id="86538-110">Если вы используете сертификат для проверки подлинности между серверами MBAM, после обновления сервера администрирования и мониторинга MBAM вы должны убедиться, что сертификат действителен, а не отозван или срок его действия истек.</span><span class="sxs-lookup"><span data-stu-id="86538-110">If you are using a certificate for authentication between MBAM servers, after updating the MBAM Administration and Monitoring server you must ensure that the certificate is valid and not revoked or expired.</span></span>

<span data-ttu-id="86538-111">**Временное решение**: нет.</span><span class="sxs-lookup"><span data-stu-id="86538-111">**Workaround**: None.</span></span>

### <span data-ttu-id="86538-112">MBAM SVCLOG файл, заполнение места на диске</span><span class="sxs-lookup"><span data-stu-id="86538-112">MBAM Svclog File Filling Disk Space</span></span>

<span data-ttu-id="86538-113">Если вы следовали [статье базы знаний 2668170](https://go.microsoft.com/fwlink/?LinkID=247277), возможно, потребуется повторить эти действия после установки этого обновления.</span><span class="sxs-lookup"><span data-stu-id="86538-113">If you have followed [Knowledge Base article 2668170](https://go.microsoft.com/fwlink/?LinkID=247277), you might have to repeat the KB steps after you install this update.</span></span>

<span data-ttu-id="86538-114">**Временное решение**: нет.</span><span class="sxs-lookup"><span data-stu-id="86538-114">**Workaround**: None.</span></span>

## <span data-ttu-id="86538-115">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="86538-115">Related topics</span></span>

[<span data-ttu-id="86538-116">Развертывание обновления языковой версии MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="86538-116">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





