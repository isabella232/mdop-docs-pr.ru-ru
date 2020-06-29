---
title: Копирование шаблонов групповой политики MBAM 2.5
description: Копирование шаблонов групповой политики MBAM 2.5
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825222"
---
# <span data-ttu-id="287be-103">Копирование шаблонов групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="287be-103">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="287be-104">Перед развертыванием установки клиента MBAM необходимо скачать шаблоны групповой политики MBAM, которые содержат параметры настройки реализации MBAM для шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="287be-104">Before deploying the MBAM Client installation, you must download the MBAM Group Policy Templates, which contain Group Policy settings that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="287be-105">После загрузки шаблонов вы можете настроить параметры групповой политики для реализации в масштабах всего предприятия.</span><span class="sxs-lookup"><span data-stu-id="287be-105">After downloading the templates, you then set the Group Policy settings to implement across your enterprise.</span></span>

## <span data-ttu-id="287be-106">Загрузка и развертывание шаблонов групповой политики MDOP</span><span class="sxs-lookup"><span data-stu-id="287be-106">Downloading and deploying the MDOP Group Policy templates</span></span>


<span data-ttu-id="287be-107">Шаблоны групповой политики MDOP можно загрузить в виде самораспаковывающегося распакованного сжатого файла, сгруппированных по технологиям и версиям.</span><span class="sxs-lookup"><span data-stu-id="287be-107">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

**<span data-ttu-id="287be-108">Загрузка и развертывание шаблонов групповой политики MDOP</span><span class="sxs-lookup"><span data-stu-id="287be-108">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="287be-109">Скачайте шаблоны групповой политики MDOP из [административных шаблонов в групповой политике пакета оптимизации рабочей среды Майкрософт](https://www.microsoft.com/download/details.aspx?id=55531).</span><span class="sxs-lookup"><span data-stu-id="287be-109">Download the MDOP Group Policy templates from [Microsoft Desktop Optimization Pack Group Policy Administrative Templates](https://www.microsoft.com/download/details.aspx?id=55531).</span></span>

2. <span data-ttu-id="287be-110">Запустите загруженный файл, чтобы извлечь папки шаблонов.</span><span class="sxs-lookup"><span data-stu-id="287be-110">Run the downloaded file to extract the template folders.</span></span>

   **<span data-ttu-id="287be-111">Warning</span><span class="sxs-lookup"><span data-stu-id="287be-111">Warning</span></span>**  
   <span data-ttu-id="287be-112">Не извлекайте шаблоны прямо в каталог развертывания групповой политики.</span><span class="sxs-lookup"><span data-stu-id="287be-112">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="287be-113">В этом файле объединены различные технологии и версии.</span><span class="sxs-lookup"><span data-stu-id="287be-113">Multiple technologies and versions are bundled in this file.</span></span>



3. <span data-ttu-id="287be-114">В извлеченной папке найдите ADMX-файл с поддержкой технологии и версии.</span><span class="sxs-lookup"><span data-stu-id="287be-114">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="287be-115">В некоторых технологиях MDOP есть несколько наборов объектов групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="287be-115">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="287be-116">Например, MBAM включает параметры управления MBAM и параметры пользователя MBAM.</span><span class="sxs-lookup"><span data-stu-id="287be-116">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="287be-117">Найдите соответствующий файл. ADML с помощью языка и региональных параметров ( *EN* для английского (США)).</span><span class="sxs-lookup"><span data-stu-id="287be-117">Locate the appropriate .adml file by language-culture (that is, *en* for English-United States).</span></span>

5. <span data-ttu-id="287be-118">Скопируйте файлы ADMX и ADML в папку определение политики.</span><span class="sxs-lookup"><span data-stu-id="287be-118">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="287be-119">В зависимости от того, где хранятся шаблоны, вы можете настроить параметры групповой политики на локальном устройстве или на любом компьютере домена.</span><span class="sxs-lookup"><span data-stu-id="287be-119">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   **<span data-ttu-id="287be-120">Локальные файлы.</span><span class="sxs-lookup"><span data-stu-id="287be-120">Local files.</span></span>** <span data-ttu-id="287be-121">Чтобы настроить параметры групповой политики на локальном устройстве, скопируйте файлы шаблонов в указанные ниже места.</span><span class="sxs-lookup"><span data-stu-id="287be-121">To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="287be-122">Тип файла</span><span class="sxs-lookup"><span data-stu-id="287be-122">File type</span></span></th>
   <th align="left"><span data-ttu-id="287be-123">Расположение файла</span><span class="sxs-lookup"><span data-stu-id="287be-123">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="287be-124">Шаблон групповой политики (ADMX)</span><span class="sxs-lookup"><span data-stu-id="287be-124">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="287be-125">&lt;strong &gt; PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="287be-125">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="287be-126">Языковой файл групповой политики (ADML)</span><span class="sxs-lookup"><span data-stu-id="287be-126">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="287be-127">&lt;strong &gt; PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="287be-127">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. <span data-ttu-id="287be-128">Измените параметры групповой политики с помощью консоли управления групповыми политиками (GPMC) или расширенного управления групповыми политиками, чтобы настроить параметры групповой политики для технологии MDOP.</span><span class="sxs-lookup"><span data-stu-id="287be-128">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span> <span data-ttu-id="287be-129">Дополнительные сведения [MBAM в разделе Изменение параметров групповой политики в 2,5](editing-the-mbam-25-group-policy-settings.md) .</span><span class="sxs-lookup"><span data-stu-id="287be-129">See [Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md) for more information.</span></span>

   <span data-ttu-id="287be-130">Описание параметров групповой политики приведено в разделе [Планирование требований к групповой политике MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="287be-130">For descriptions of the Group Policy settings, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>


## <span data-ttu-id="287be-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="287be-131">Related topics</span></span>


[<span data-ttu-id="287be-132">Развертывание объектов групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="287be-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)


## <span data-ttu-id="287be-133">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="287be-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="287be-134">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="287be-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="287be-135">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="287be-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






