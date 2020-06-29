---
title: Справочник по командной строке установки клиента
description: Справочник по командной строке установки клиента
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826729"
---
# <span data-ttu-id="43b34-103">Справочник по командной строке установки клиента</span><span class="sxs-lookup"><span data-stu-id="43b34-103">Client Installation Command Line Reference</span></span>


**<span data-ttu-id="43b34-104">Установка MED-V из командной строки</span><span class="sxs-lookup"><span data-stu-id="43b34-104">To install MED-V from the command line</span></span>**

1.  <span data-ttu-id="43b34-105">В командной строке запустите пакет MED-V. msi и любые дополнительные параметры, описанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="43b34-105">From the command line, run the MED-V .msi package followed by any of the optional parameters described in the following table.</span></span>

2.  <span data-ttu-id="43b34-106">Пакет для MED-V. msi называется *MED-V\_x.msi*, где *x* — номер версии.</span><span class="sxs-lookup"><span data-stu-id="43b34-106">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="43b34-107">Например, *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="43b34-107">For example, *MED-V\_1.0.65.msi*.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="43b34-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="43b34-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="43b34-109">Значение</span><span class="sxs-lookup"><span data-stu-id="43b34-109">Value</span></span></th>
<th align="left"><span data-ttu-id="43b34-110">Описание</span><span class="sxs-lookup"><span data-stu-id="43b34-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43b34-111">параметрами</span><span class="sxs-lookup"><span data-stu-id="43b34-111">/quiet</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="43b34-112">Автоматическая установка</span><span class="sxs-lookup"><span data-stu-id="43b34-112">Silent installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43b34-113">/log &lt; полный путь к файлу журнала&gt;</span><span class="sxs-lookup"><span data-stu-id="43b34-113">/log &lt;full path to log file&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="43b34-114">Полный путь к файлу журнала.</span><span class="sxs-lookup"><span data-stu-id="43b34-114">The full path to the log file.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43b34-115">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="43b34-115">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="43b34-116">Полный путь к каталогу установки.</span><span class="sxs-lookup"><span data-stu-id="43b34-116">The full path to the installation directory.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43b34-117">VMSFOLDER</span><span class="sxs-lookup"><span data-stu-id="43b34-117">VMSFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="43b34-118">Полный путь к папке виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="43b34-118">The full path to the virtual machine folder.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43b34-119">INSTALL_ADMIN_TOOLS</span><span class="sxs-lookup"><span data-stu-id="43b34-119">INSTALL_ADMIN_TOOLS</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="43b34-120">1, 0</span><span class="sxs-lookup"><span data-stu-id="43b34-120">1,0</span></span></strong></p>
<p><span data-ttu-id="43b34-121">По умолчанию: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="43b34-121">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="43b34-122">Установка средств администрирования для MED-V.</span><span class="sxs-lookup"><span data-stu-id="43b34-122">Installs MED-V administration tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43b34-123">START_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="43b34-123">START_AUTOMATICALLY</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="43b34-124">1, 0</span><span class="sxs-lookup"><span data-stu-id="43b34-124">1,0</span></span></strong></p>
<p><span data-ttu-id="43b34-125">По умолчанию: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="43b34-125">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="43b34-126">Автоматически запускает клиент MED-V при каждом входе пользователя в систему Windows.</span><span class="sxs-lookup"><span data-stu-id="43b34-126">Automatically starts MED-V client every time the user logs on to Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43b34-127">SERVER_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="43b34-127">SERVER_ADDRESS</span></span></p></td>
<td align="left"><p><span data-ttu-id="43b34-128">имя узла или IP-адрес</span><span class="sxs-lookup"><span data-stu-id="43b34-128">host name or IP</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43b34-129">SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="43b34-129">SERVER_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="43b34-130">порт</span><span class="sxs-lookup"><span data-stu-id="43b34-130">port</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43b34-131">SERVER_SSL</span><span class="sxs-lookup"><span data-stu-id="43b34-131">SERVER_SSL</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="43b34-132">1, 0</span><span class="sxs-lookup"><span data-stu-id="43b34-132">1,0</span></span></strong></p>
<p><span data-ttu-id="43b34-133">для <strong> HTTPS </strong> или <strong> http</span><span class="sxs-lookup"><span data-stu-id="43b34-133">for <strong>https</strong> or <strong>http</span></span></strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43b34-134">START_MEDV</span><span class="sxs-lookup"><span data-stu-id="43b34-134">START_MEDV</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="43b34-135">1, 0</span><span class="sxs-lookup"><span data-stu-id="43b34-135">1,0</span></span></strong></p>
<p><span data-ttu-id="43b34-136">По умолчанию: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="43b34-136">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="43b34-137">Запускает MED-V после завершения установки MED-V.</span><span class="sxs-lookup"><span data-stu-id="43b34-137">Starts MED-V at the completion of the MED-V installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="43b34-138">Примечание.</span><span class="sxs-lookup"><span data-stu-id="43b34-138">Note</span></span></strong><br/><p><span data-ttu-id="43b34-139">Рекомендуется устанавливать START_MEDV = 0 в случае, если MED-V установлен системой.</span><span class="sxs-lookup"><span data-stu-id="43b34-139">It is recommended to set START_MEDV=0 in case MED-V is installed by the system.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43b34-140">DESKTOP_SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="43b34-140">DESKTOP_SHORTCUT</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="43b34-141">1, 0</span><span class="sxs-lookup"><span data-stu-id="43b34-141">1,0</span></span></strong></p>
<p><span data-ttu-id="43b34-142">По умолчанию: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="43b34-142">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="43b34-143">Создание ярлыка на рабочем столе, который запускает клиент MED-V.</span><span class="sxs-lookup"><span data-stu-id="43b34-143">Creates a shortcut on the desktop, which starts MED-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43b34-144">MINIMAL_RAM_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="43b34-144">MINIMAL_RAM_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="43b34-145">ОЗУ (МБ)</span><span class="sxs-lookup"><span data-stu-id="43b34-145">RAM in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="43b34-146">При установке MED-V проверяет, не указан ли для компьютера минимальный объем ОЗУ.</span><span class="sxs-lookup"><span data-stu-id="43b34-146">When installing MED-V, checks whether the computer has the minimum amount of RAM specified.</span></span> <span data-ttu-id="43b34-147">В противном случае установка прерывается.</span><span class="sxs-lookup"><span data-stu-id="43b34-147">If not, installation is aborted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43b34-148">SKIP_OS_CHECK</span><span class="sxs-lookup"><span data-stu-id="43b34-148">SKIP_OS_CHECK</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="43b34-149">1, 0</span><span class="sxs-lookup"><span data-stu-id="43b34-149">1,0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="43b34-150">Пропускает проверку операционной системы.</span><span class="sxs-lookup"><span data-stu-id="43b34-150">Omits the operating system validation.</span></span></p></td>
</tr>
</tbody>
</table>











