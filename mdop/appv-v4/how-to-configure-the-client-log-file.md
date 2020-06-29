---
title: Настройка файла журнала клиента
description: Настройка файла журнала клиента
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817799"
---
# <span data-ttu-id="442c3-103">Настройка файла журнала клиента</span><span class="sxs-lookup"><span data-stu-id="442c3-103">How to Configure the Client Log File</span></span>


<span data-ttu-id="442c3-104">Вы можете использовать следующие процедуры для настройки файла журнала клиента Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="442c3-104">You can use the following procedures to configure the Application Virtualization (App-V) Client log file.</span></span>

**<span data-ttu-id="442c3-105">Изменение расположения файла журнала</span><span class="sxs-lookup"><span data-stu-id="442c3-105">To change the log file location</span></span>**

-   <span data-ttu-id="442c3-106">Измените значение в следующем разделе реестра, чтобы указать новый путь для файла журнала.</span><span class="sxs-lookup"><span data-stu-id="442c3-106">Edit the following registry key value to specify the new path for the log file.</span></span> <span data-ttu-id="442c3-107">После изменения этого значения необходимо перезапустить службу **sftlist** .</span><span class="sxs-lookup"><span data-stu-id="442c3-107">You must restart the **sftlist** service after changing this value.</span></span> <span data-ttu-id="442c3-108">Это расположение также может быть изменено в интерактивном режиме после установки.</span><span class="sxs-lookup"><span data-stu-id="442c3-108">This location can also be changed interactively after installation.</span></span>

    <span data-ttu-id="442c3-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span><span class="sxs-lookup"><span data-stu-id="442c3-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span></span>

**<span data-ttu-id="442c3-110">Изменение уровня ведения журнала</span><span class="sxs-lookup"><span data-stu-id="442c3-110">To change the log reporting level</span></span>**

-   <span data-ttu-id="442c3-111">По умолчанию для сообщений, которые записываются в журнал, включаются все события уровня серьезности 4 (информационные) и выше.</span><span class="sxs-lookup"><span data-stu-id="442c3-111">By default, the type of messages that are written to the log include all events of severity level 4 (Informational) or higher.</span></span> <span data-ttu-id="442c3-112">Уровень серьезности хранится в следующем значении ключа.</span><span class="sxs-lookup"><span data-stu-id="442c3-112">The severity level is stored in the following key value.</span></span> <span data-ttu-id="442c3-113">Установите для этого параметра значение 5, чтобы включить ведение подробного журнала.</span><span class="sxs-lookup"><span data-stu-id="442c3-113">Set this key value to 5 to enable verbose logging.</span></span> <span data-ttu-id="442c3-114">Используйте подробный журнал только для коротких периодов при устранении неполадок, так как это приводит к созданию большого объема сообщений и приводит к быстрому заполнению журнала.</span><span class="sxs-lookup"><span data-stu-id="442c3-114">Use verbose logging only for short periods during troubleshooting because it will generate a very large volume of messages and cause the log to fill up quickly.</span></span>

    <span data-ttu-id="442c3-115">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span><span class="sxs-lookup"><span data-stu-id="442c3-115">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span></span>

**<span data-ttu-id="442c3-116">Изменение размера журнала</span><span class="sxs-lookup"><span data-stu-id="442c3-116">To change the log size</span></span>**

-   <span data-ttu-id="442c3-117">В Application Virtualization (App-V) 4,5 размер журнала управляется следующим значением раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="442c3-117">In Application Virtualization (App-V) 4.5, the log size is controlled by the following registry key value.</span></span> <span data-ttu-id="442c3-118">Это значение по умолчанию равно 256 МБ и определяет максимальный размер (в МЕГАБАЙТах), в течение которого журнал может увеличиваться до сброса.</span><span class="sxs-lookup"><span data-stu-id="442c3-118">This value defaults to 256MB and defines the maximum size, in MB, that the log can grow to before being reset.</span></span>

    <span data-ttu-id="442c3-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span><span class="sxs-lookup"><span data-stu-id="442c3-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span></span>

    <span data-ttu-id="442c3-120">**Внимание!**  Для этого значения раздела реестра должно быть задано значение больше нуля, что приводит к сбросу файла журнала.</span><span class="sxs-lookup"><span data-stu-id="442c3-120">**Caution** This registry key value must be set to a value greater than zero to ensure the log file does get reset.</span></span>

     

**<span data-ttu-id="442c3-121">Изменение количества резервных копий</span><span class="sxs-lookup"><span data-stu-id="442c3-121">To change the number of backup copies</span></span>**

-   <span data-ttu-id="442c3-122">Когда файл журнала достигнет максимального размера, он принудительно сбрасывается, когда происходит следующая запись в журнал.</span><span class="sxs-lookup"><span data-stu-id="442c3-122">When the log file reaches the maximum size, a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="442c3-123">Сброс приводит к созданию нового файла журнала, а старый файл переименовывается в качестве резервной копии.</span><span class="sxs-lookup"><span data-stu-id="442c3-123">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span> <span data-ttu-id="442c3-124">Следующий параметр реестра задает количество резервных копий файла журнала, которые сохраняются при сбросе файла.</span><span class="sxs-lookup"><span data-stu-id="442c3-124">The following registry setting controls the number of backup copies of the log file that are kept when the file is reset.</span></span> <span data-ttu-id="442c3-125">Значение по умолчанию — 4.</span><span class="sxs-lookup"><span data-stu-id="442c3-125">The default value is 4.</span></span>

    <span data-ttu-id="442c3-126">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="442c3-126">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span></span>

    <span data-ttu-id="442c3-127">Формат имени файла журнала резервной копии: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** и зависит от времени сброса в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="442c3-127">The format of the backup log file names is: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** and is based on the reset time, in Universal Coordinated Time (UTC).</span></span> <span data-ttu-id="442c3-128">В таблице ниже перечислены символы, используемые для создания имен файлов и их описания.</span><span class="sxs-lookup"><span data-stu-id="442c3-128">The following table lists the symbols used in creating the file names and their descriptions.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="442c3-129">Символ</span><span class="sxs-lookup"><span data-stu-id="442c3-129">Symbol</span></span></th>
    <th align="left"><span data-ttu-id="442c3-130">Описание</span><span class="sxs-lookup"><span data-stu-id="442c3-130">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="442c3-131">ГГГГ</span><span class="sxs-lookup"><span data-stu-id="442c3-131">YYYY</span></span></p></td>
    <td align="left"><p><span data-ttu-id="442c3-132">4-значный год</span><span class="sxs-lookup"><span data-stu-id="442c3-132">4-digit year</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="442c3-133">ММ</span><span class="sxs-lookup"><span data-stu-id="442c3-133">MM</span></span></p></td>
    <td align="left"><p><span data-ttu-id="442c3-134">2-значный месяц (01 – 12)</span><span class="sxs-lookup"><span data-stu-id="442c3-134">2-digit month (01–12)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="442c3-135">ДД</span><span class="sxs-lookup"><span data-stu-id="442c3-135">DD</span></span></p></td>
    <td align="left"><p><span data-ttu-id="442c3-136">2-значный день месяца (01 – 31)</span><span class="sxs-lookup"><span data-stu-id="442c3-136">2-digit day of the month (01–31)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="442c3-137">чч</span><span class="sxs-lookup"><span data-stu-id="442c3-137">hh</span></span></p></td>
    <td align="left"><p><span data-ttu-id="442c3-138">час (00 – 23)</span><span class="sxs-lookup"><span data-stu-id="442c3-138">hour (00–23)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="442c3-139">мм</span><span class="sxs-lookup"><span data-stu-id="442c3-139">mm</span></span></p></td>
    <td align="left"><p><span data-ttu-id="442c3-140">минуты (00 – 59)</span><span class="sxs-lookup"><span data-stu-id="442c3-140">minutes (00–59)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="442c3-141">ss</span><span class="sxs-lookup"><span data-stu-id="442c3-141">ss</span></span></p></td>
    <td align="left"><p><span data-ttu-id="442c3-142">секунд (00 – 59)</span><span class="sxs-lookup"><span data-stu-id="442c3-142">seconds (00–59)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="442c3-143">uuu</span><span class="sxs-lookup"><span data-stu-id="442c3-143">uuu</span></span></p></td>
    <td align="left"><p><span data-ttu-id="442c3-144">мсек (000 – 999)</span><span class="sxs-lookup"><span data-stu-id="442c3-144">milliseconds (000–999)</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="442c3-145">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="442c3-145">Related topics</span></span>


[<span data-ttu-id="442c3-146">Настройка параметров реестра клиента App-V с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="442c3-146">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





