---
title: Скачивание и развертывание шаблонов групповой политики MDOP (ADMX-файл)
description: Скачивание и развертывание шаблонов групповой политики MDOP (ADMX-файл)
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826919"
---
# <span data-ttu-id="5b13d-103">Скачивание и развертывание шаблонов групповой политики MDOP (ADMX-файл)</span><span class="sxs-lookup"><span data-stu-id="5b13d-103">How to Download and Deploy MDOP Group Policy (.admx) Templates</span></span>


<span data-ttu-id="5b13d-104">С помощью шаблонов групповых политик, файлов ADMX и ADML можно управлять параметрами некоторых технологий пакета оптимизации рабочего стола (MDOP) (например, App-V, UE-V или MBAM).</span><span class="sxs-lookup"><span data-stu-id="5b13d-104">You can manage the feature settings of certain Microsoft Desktop Optimization Pack (MDOP) technologies (for example, App-V, UE-V, or MBAM) by using Group Policy templates, the .admx and .adml files.</span></span> <span data-ttu-id="5b13d-105">Шаблоны групповой политики MDOP можно загрузить в виде самораспаковывающегося распакованного сжатого файла, сгруппированных по технологиям и версиям.</span><span class="sxs-lookup"><span data-stu-id="5b13d-105">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

## <span data-ttu-id="5b13d-106">Шаблоны групповой политики MDOP</span><span class="sxs-lookup"><span data-stu-id="5b13d-106">MDOP Group Policy templates</span></span>

**<span data-ttu-id="5b13d-107">Загрузка и развертывание шаблонов групповой политики MDOP</span><span class="sxs-lookup"><span data-stu-id="5b13d-107">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="5b13d-108">Скачайте последние [шаблоны групповой политики MDOP](https://www.microsoft.com/download/details.aspx?id=55531)</span><span class="sxs-lookup"><span data-stu-id="5b13d-108">Download the latest [MDOP Group Policy templates](https://www.microsoft.com/download/details.aspx?id=55531)</span></span> 

2. <span data-ttu-id="5b13d-109">Разверните загруженный CAB-файл, выполнив</span><span class="sxs-lookup"><span data-stu-id="5b13d-109">Expand the downloaded .cab file by running</span></span> `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **<span data-ttu-id="5b13d-110">Warning</span><span class="sxs-lookup"><span data-stu-id="5b13d-110">Warning</span></span>**  
   <span data-ttu-id="5b13d-111">Не извлекайте шаблоны прямо в каталог развертывания групповой политики.</span><span class="sxs-lookup"><span data-stu-id="5b13d-111">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="5b13d-112">В этом файле объединены различные технологии и версии.</span><span class="sxs-lookup"><span data-stu-id="5b13d-112">Multiple technologies and versions are bundled in this file.</span></span>

3. <span data-ttu-id="5b13d-113">В извлеченной папке найдите ADMX-файл с поддержкой технологии и версии.</span><span class="sxs-lookup"><span data-stu-id="5b13d-113">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="5b13d-114">В некоторых технологиях MDOP есть несколько наборов объектов групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="5b13d-114">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="5b13d-115">Например, MBAM включает параметры управления MBAM и параметры пользователя MBAM.</span><span class="sxs-lookup"><span data-stu-id="5b13d-115">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="5b13d-116">Найдите соответствующий файл. ADML по языку и региональным параметрам ( *en-US* для английских США).</span><span class="sxs-lookup"><span data-stu-id="5b13d-116">Locate the appropriate .adml file by language-culture (that is, *en-us* for English-United States).</span></span>

5. <span data-ttu-id="5b13d-117">Скопируйте файлы ADMX и ADML в папку определение политики.</span><span class="sxs-lookup"><span data-stu-id="5b13d-117">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="5b13d-118">В зависимости от того, где хранятся шаблоны, вы можете настроить параметры групповой политики на локальном устройстве или на любом компьютере домена.</span><span class="sxs-lookup"><span data-stu-id="5b13d-118">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   - <span data-ttu-id="5b13d-119">**Локальные файлы:** Чтобы настроить параметры групповой политики на локальном устройстве, скопируйте файлы шаблонов в указанные ниже места.</span><span class="sxs-lookup"><span data-stu-id="5b13d-119">**Local files:** To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5b13d-120">Тип файла</span><span class="sxs-lookup"><span data-stu-id="5b13d-120">File type</span></span></th>
   <th align="left"><span data-ttu-id="5b13d-121">Расположение файла</span><span class="sxs-lookup"><span data-stu-id="5b13d-121">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b13d-122">Шаблон групповой политики (ADMX)</span><span class="sxs-lookup"><span data-stu-id="5b13d-122">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="5b13d-123">&lt;strong &gt; PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="5b13d-123">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5b13d-124">Языковой файл групповой политики (ADML)</span><span class="sxs-lookup"><span data-stu-id="5b13d-124">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="5b13d-125">&lt;strong &gt; PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="5b13d-125">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>

   - <span data-ttu-id="5b13d-126">**Центральное хранилище домена:** Чтобы включить настройку параметров групповой политики администратором групповой политики с любого компьютера домена, скопируйте файлы в указанные ниже места на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="5b13d-126">**Domain central store:** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5b13d-127">Тип файла</span><span class="sxs-lookup"><span data-stu-id="5b13d-127">File type</span></span></th>
   <th align="left"><span data-ttu-id="5b13d-128">Расположение файла</span><span class="sxs-lookup"><span data-stu-id="5b13d-128">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b13d-129">Шаблон групповой политики (ADMX)</span><span class="sxs-lookup"><span data-stu-id="5b13d-129">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="5b13d-130">&lt;strong &gt; sysvol\domain\policies\PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="5b13d-130">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5b13d-131">Языковой файл групповой политики (ADML)</span><span class="sxs-lookup"><span data-stu-id="5b13d-131">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="5b13d-132">&lt;strong &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</span><span class="sxs-lookup"><span data-stu-id="5b13d-132">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions[MUIculture]</span></span></strong><code>[MUIculture]</code></p>
   <p><span data-ttu-id="5b13d-133">Например, файл, зависящий от языковой версии для американского английского, будет храниться в%systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</span><span class="sxs-lookup"><span data-stu-id="5b13d-133">For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</span></span></p></td>
   </tr>
   </tbody>
   </table>

6. <span data-ttu-id="5b13d-134">Измените параметры групповой политики с помощью консоли управления групповыми политиками (GPMC) или расширенного управления групповыми политиками, чтобы настроить параметры групповой политики для технологии MDOP.</span><span class="sxs-lookup"><span data-stu-id="5b13d-134">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span>

### <span data-ttu-id="5b13d-135">Групповая политика MDOP по технологиям</span><span class="sxs-lookup"><span data-stu-id="5b13d-135">MDOP Group Policy by technology</span></span>

<span data-ttu-id="5b13d-136">Дополнительные сведения о поддерживаемой групповой политике MDOP можно найти в документации по технологии.</span><span class="sxs-lookup"><span data-stu-id="5b13d-136">For more information about supported MDOP Group Policy, see the specific documentation for the technology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5b13d-137">Технология MDOP</span><span class="sxs-lookup"><span data-stu-id="5b13d-137">MDOP Technology</span></span></th>
<th align="left"><span data-ttu-id="5b13d-138">Наборы версий</span><span class="sxs-lookup"><span data-stu-id="5b13d-138">Version bundles</span></span></th>
<th align="left"><span data-ttu-id="5b13d-139">Заметки</span><span class="sxs-lookup"><span data-stu-id="5b13d-139">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5b13d-140">Виртуализация приложений (App-V)</span><span class="sxs-lookup"><span data-stu-id="5b13d-140">Application Virtualization (App-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5b13d-141">Пакеты обновления для App-V 5,0 и App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="5b13d-141">App-V 5.0 and App-V 5.0 Service Packs</span></span></p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)"><span data-ttu-id="5b13d-142">Изменение конфигурации клиента App-V 5.0 с помощью шаблона ADMX и групповой политики</span><span class="sxs-lookup"><span data-stu-id="5b13d-142">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5b13d-143">Виртуализация взаимодействия с пользователем (UE-V)</span><span class="sxs-lookup"><span data-stu-id="5b13d-143">User Experience Virtualization (UE-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5b13d-144">UE-V 2,0 и UE-V 2,1</span><span class="sxs-lookup"><span data-stu-id="5b13d-144">UE-V 2.0 and UE-V 2.1</span></span></p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)"><span data-ttu-id="5b13d-145">Настройка UE-V 2. x с объектами групповой политики</span><span class="sxs-lookup"><span data-stu-id="5b13d-145">Configuring UE-V 2.x with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5b13d-146">UE-V 1,0, включая 1,0 SP1</span><span class="sxs-lookup"><span data-stu-id="5b13d-146">UE-V 1.0 including 1.0 SP1</span></span></p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)"><span data-ttu-id="5b13d-147">Настройка UE-V с помощью объектов групповой политики</span><span class="sxs-lookup"><span data-stu-id="5b13d-147">Configuring UE-V with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5b13d-148">Администрирование и мониторинг Microsoft BitLocker (MBAM)</span><span class="sxs-lookup"><span data-stu-id="5b13d-148">Microsoft BitLocker Administration and Monitoring (MBAM)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5b13d-149">MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="5b13d-149">MBAM 2.5</span></span></p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="5b13d-150">Планирование требований групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5b13d-150">Planning for MBAM 2.5 Group Policy Requirements</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5b13d-151">MBAM 2,0, включая 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="5b13d-151">MBAM 2.0 including 2.0 SP1</span></span></p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="5b13d-152">Планирование требований групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5b13d-152">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="5b13d-153">Развертывание объектов групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5b13d-153">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5b13d-154">MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="5b13d-154">MBAM 1.0</span></span></p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)"><span data-ttu-id="5b13d-155">Изменение параметров объектов групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5b13d-155">How to Edit MBAM 1.0 GPO Settings</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





