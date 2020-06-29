---
title: Развертывание клиента MBAM с помощью командной строки
description: Развертывание клиента MBAM с помощью командной строки
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824489"
---
# <span data-ttu-id="3d64d-103">Развертывание клиента MBAM с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="3d64d-103">How to Deploy the MBAM Client by Using a Command Line</span></span>


<span data-ttu-id="3d64d-104">Вы можете использовать командную строку для развертывания программного обеспечения клиента администрирования и мониторинга Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="3d64d-104">You can use a command line to deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software.</span></span>

## <span data-ttu-id="3d64d-105">Командная строка для развертывания программного обеспечения клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="3d64d-105">Command Line to deploy the MBAM Client software</span></span>


<span data-ttu-id="3d64d-106">Введите в командной строке следующую команду, чтобы автоматически присвоить лицензионное соглашение с конечным пользователем при развертывании клиентского программного обеспечения MBAM.</span><span class="sxs-lookup"><span data-stu-id="3d64d-106">Type the following command at the command prompt to automatically accept the end user license agreement when deploying the MBAM Client software.</span></span>

**<span data-ttu-id="3d64d-107">MBAMClientSetup.exe/acceptEula = Yes</span><span class="sxs-lookup"><span data-stu-id="3d64d-107">MBAMClientSetup.exe /acceptEula=Yes</span></span>**

<span data-ttu-id="3d64d-108">**Примечание**  Параметры командной строки **/Ju** и **/JM** не поддерживаются, и их нельзя использовать для установки клиентского программного обеспечения MBAM.</span><span class="sxs-lookup"><span data-stu-id="3d64d-108">**Note** The **/ju** and **/jm** command-line options are not supported and cannot be used to install the MBAM Client software.</span></span>

 

<span data-ttu-id="3d64d-109">Чтобы извлечь и установить MSP, введите в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d64d-109">Type the following command at the command prompt to extract and install the MSP:</span></span>

**<span data-ttu-id="3d64d-110">MBAMClientSetup.exe/Extract &lt; путь для извлечения MSI &gt; /AcceptEula = да</span><span class="sxs-lookup"><span data-stu-id="3d64d-110">MBAMClientSetup.exe /extract &lt;path to extract MSI&gt; /acceptEula=Yes</span></span>**

<span data-ttu-id="3d64d-111">Затем установите пакет MSI автоматически, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d64d-111">Then, install the MSI silently by running the following command:</span></span>

**<span data-ttu-id="3d64d-112">msiexec/i &lt; путь к извлеченному пакету MSI &gt; /QB ALLUSERS = 1 REBOOT = REALLYSUPPRESS</span><span class="sxs-lookup"><span data-stu-id="3d64d-112">msiexec /i &lt;path to extracted MSI&gt; /qb ALLUSERS=1 REBOOT=ReallySuppress</span></span>**

<span data-ttu-id="3d64d-113">**Примечание**  Начиная с MBAM 2,5 с пакетом обновления 1 (SP1), отдельный MSI больше не входит в состав продукта MBAM.</span><span class="sxs-lookup"><span data-stu-id="3d64d-113">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="3d64d-114">Тем не менее, после принятия условий лицензионного соглашения вы можете извлечь MSI-файл из исполняемого файла (exe), который входит в состав продукта.</span><span class="sxs-lookup"><span data-stu-id="3d64d-114">However, you can extract the MSI from the executable file (.exe) that is included with the product, after accepting the EULA.</span></span>

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a><span data-ttu-id="3d64d-115">OPTIN \ _FOR \ _MICROSOFT \ _UPDATES = 1 параметр командной строки</span><span class="sxs-lookup"><span data-stu-id="3d64d-115">OPTIN\_FOR\_MICROSOFT\_UPDATES=1 command-line option</span></span>


<span data-ttu-id="3d64d-116">При необходимости вы можете указать параметр командной строки `OPTIN_FOR_MICROSOFT_UPDATES=1` во время установки клиентского программного обеспечения, чтобы автоматически установить обновления Microsoft на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="3d64d-116">You can optionally specify the command-line option `OPTIN_FOR_MICROSOFT_UPDATES=1` during the Client software installation to automatically install Microsoft Updates on client computers.</span></span> <span data-ttu-id="3d64d-117">При указании этого параметра автоматически запускается Microsoft Update и производится поиск доступных обновлений для установки после завершения установки клиентского программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="3d64d-117">Specifying this option makes Microsoft Update automatically start and search for available updates to install after the Client software installation finishes.</span></span>

<span data-ttu-id="3d64d-118">Этот параметр командной строки можно использовать в одном из указанных ниже способов установки.</span><span class="sxs-lookup"><span data-stu-id="3d64d-118">You can use this command-line option with either of the following installation methods.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d64d-119">Установите клиентское программное обеспечение MBAM с помощью</span><span class="sxs-lookup"><span data-stu-id="3d64d-119">Install the MBAM Client software by using</span></span></th>
<th align="left"><span data-ttu-id="3d64d-120">Пример.</span><span class="sxs-lookup"><span data-stu-id="3d64d-120">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3d64d-121">MBAMClientSetup.exe</span><span class="sxs-lookup"><span data-stu-id="3d64d-121">MBAMClientSetup.exe</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="3d64d-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="3d64d-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3d64d-123">msiexec/i MBAMClient.msi</span><span class="sxs-lookup"><span data-stu-id="3d64d-123">msiexec /i MBAMClient.msi</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="3d64d-124">msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="3d64d-124">msiexec /i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="3d64d-125">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3d64d-125">Related topics</span></span>


[<span data-ttu-id="3d64d-126">Развертывание клиента MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3d64d-126">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="3d64d-127">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="3d64d-127">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3d64d-128">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="3d64d-128">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="3d64d-129">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="3d64d-129">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




