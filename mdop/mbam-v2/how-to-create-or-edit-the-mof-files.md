---
title: Порядок создания или изменения MOF-файлов
description: Порядок создания или изменения MOF-файлов
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825322"
---
# <span data-ttu-id="9779a-103">Порядок создания или изменения MOF-файлов</span><span class="sxs-lookup"><span data-stu-id="9779a-103">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="9779a-104">Перед установкой средства администрирования и мониторинга Microsoft BitLocker (MBAM) с помощью Configuration Manager необходимо изменить файл Configuration. mof.</span><span class="sxs-lookup"><span data-stu-id="9779a-104">Before you install Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, you need to edit the Configuration.mof file.</span></span> <span data-ttu-id="9779a-105">Кроме того, необходимо либо изменить, либо создать файл SMS \ _def. mof в зависимости от используемой версии Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9779a-105">You also need to either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

## <span data-ttu-id="9779a-106">Изменение файла Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="9779a-106">Edit the Configuration.mof File</span></span>


<span data-ttu-id="9779a-107">Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker с помощью отчетов Configuration Manager MBAM, необходимо изменить файл Configuration. mof для Microsoft System Center Configuration Manager 2007 и SystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="9779a-107">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file for Microsoft System Center Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span>

[<span data-ttu-id="9779a-108">Изменение файла Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="9779a-108">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="9779a-109">Создание и изменение файла SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="9779a-109">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="9779a-110">Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker в отчетах Configuration Manager MBAM, необходимо создать или изменить файл SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="9779a-110">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="9779a-111">В Configuration Manager 2007 файл уже существует, поэтому вы должны изменить существующий файл, но не перезаписать его.</span><span class="sxs-lookup"><span data-stu-id="9779a-111">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span> <span data-ttu-id="9779a-112">Если вы используете SystemCenter2012 ConfigurationManager, необходимо создать файл.</span><span class="sxs-lookup"><span data-stu-id="9779a-112">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span>

[<span data-ttu-id="9779a-113">Создание и изменение файла SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="9779a-113">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file.md)

## <span data-ttu-id="9779a-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9779a-114">Related topics</span></span>


[<span data-ttu-id="9779a-115">Развертывание MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="9779a-115">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





