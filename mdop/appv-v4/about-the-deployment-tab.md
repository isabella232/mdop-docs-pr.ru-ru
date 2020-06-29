---
title: Вкладка "Сведения о развертывании"
description: Вкладка "Сведения о развертывании"
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819962"
---
# <span data-ttu-id="27d30-103">Вкладка "Сведения о развертывании"</span><span class="sxs-lookup"><span data-stu-id="27d30-103">About the Deployment Tab</span></span>


<span data-ttu-id="27d30-104">Используйте вкладку " **развертывание** " в консоли Application Virtualization Sequencer для изменения сведений о приложении, которое вы собираетесь поочередно.</span><span class="sxs-lookup"><span data-stu-id="27d30-104">Use the **Deployment** tab in the Application Virtualization Sequencer Console to change the information for an application you are about to sequence.</span></span> <span data-ttu-id="27d30-105">На этой вкладке есть указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="27d30-105">This tab contains the following elements.</span></span>

## <span data-ttu-id="27d30-106">URL-адрес сервера</span><span class="sxs-lookup"><span data-stu-id="27d30-106">Server URL</span></span>


<span data-ttu-id="27d30-107">Используйте элементы управления **URL-адресом сервера** , чтобы указать параметры конфигурации сервера виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="27d30-107">Use the **Server URL** controls to specify the virtual application server configuration settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27d30-108">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="27d30-108">Control</span></span></th>
<th align="left"><span data-ttu-id="27d30-109">Описание</span><span class="sxs-lookup"><span data-stu-id="27d30-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="27d30-110">Используемый протокол</span><span class="sxs-lookup"><span data-stu-id="27d30-110">Protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27d30-111">Позволяет выбрать протокол для потоковой передачи пакета упорядоченного приложения с виртуального сервера приложений на Настольный клиент виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="27d30-111">Enables you to select the protocol that will stream the sequenced application package from a virtual application server to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="27d30-112">Доступны следующие протоколы:</span><span class="sxs-lookup"><span data-stu-id="27d30-112">The following protocols are available:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="27d30-113">RTSP </strong> — это значение по умолчанию, которое указывает на то, что протокол потоковой передачи данных в реальном времени управляет обменом приложений, поддерживающих виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="27d30-113">RTSP</strong>—The default, it specifies that the Real-Time Streaming Protocol controls the exchange of virtualization-enabled applications.</span></span></p></li>
<li><p><strong><span data-ttu-id="27d30-114">RTSP </strong> — указывает на то, что протокол потоковой передачи данных в реальном времени с защитой транспортного уровня управляет обменом серийного пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="27d30-114">RTSPS</strong>—Specifies that the Real-Time Streaming Protocol with Transport Layer Security controls the exchange of a sequenced application package.</span></span></p></li>
<li><p><strong><span data-ttu-id="27d30-115">FILE </strong> (файл) — указывает на то, что последовательное приложение будет перечислено из общей.</span><span class="sxs-lookup"><span data-stu-id="27d30-115">File</strong>—Specifies that the sequenced application will be streamed from a file share.</span></span></p></li>
<li><p><strong><span data-ttu-id="27d30-116">HTTPS </strong> — указывает, что протокол Secure HTTP-транспорта управляет обменом пакетами.</span><span class="sxs-lookup"><span data-stu-id="27d30-116">HTTPS</strong>—Specifies that Secure Hypertext Transport Protocol controls the exchange of a package.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="27d30-117">Имена</span><span class="sxs-lookup"><span data-stu-id="27d30-117">Hostname</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27d30-118">Позволяет выбрать виртуальный сервер приложений или подсистему балансировки нагрузки перед группой виртуальных серверов приложений, которая будет передавать пакеты программного обеспечения в классическое приложение Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="27d30-118">Enables you to select the virtual application server or the load balancer in front of a group of virtual application servers that will stream the software package to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="27d30-119">Необходимо завершить этот элемент, чтобы создать последовательный пакет приложения, но вы можете изменить значение переменной среды% SFT_SOFTGRIDSERVER% на фактическое имя узла или IP-адрес виртуального сервера приложений.</span><span class="sxs-lookup"><span data-stu-id="27d30-119">You must complete this item to create a sequenced application package, but you can change from the default %SFT_SOFTGRIDSERVER% environment variable to the actual hostname or IP address of a virtual application server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="27d30-120">Примечание.</span><span class="sxs-lookup"><span data-stu-id="27d30-120">Note</span></span></strong><br/><p><span data-ttu-id="27d30-121">Если вы решили не указывать статическое имя узла или IP-адрес, на каждом клиентском компьютере Application Virtualization необходимо настроить переменную среды с именем SFT_SOFTGRIDSERVER.</span><span class="sxs-lookup"><span data-stu-id="27d30-121">If you choose not to specify a static hostname or IP address, on each Application Virtualization Desktop Client you must set up an environment variable called SFT_SOFTGRIDSERVER.</span></span> <span data-ttu-id="27d30-122">Это значение должно быть именем узла или IP-адресом виртуального сервера приложений или подсистемы балансировки нагрузки, который является клиентом&#39;s из источника приложений.</span><span class="sxs-lookup"><span data-stu-id="27d30-122">Its value must be the hostname or IP address of the virtual application server or load balancer that is this client&#39;s source of applications.</span></span> <span data-ttu-id="27d30-123">В этой переменной среды следует использовать системную переменную, а не пользовательскую переменную.</span><span class="sxs-lookup"><span data-stu-id="27d30-123">You should make this environment variable a system variable rather than a user variable.</span></span> <span data-ttu-id="27d30-124">Любой клиентский сеанс для виртуализации приложений, запущенный на этом компьютере во время назначения этой переменной, должен быть закрыт, а затем открыт для того, чтобы возобновленный сеанс знал о новом источнике приложения.</span><span class="sxs-lookup"><span data-stu-id="27d30-124">Any Application Virtualization Desktop Client session that is running on this computer during your assignment of this variable must be closed and then opened so that the resumed session will be aware of its new application source.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="27d30-125">Port</span><span class="sxs-lookup"><span data-stu-id="27d30-125">Port</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27d30-126">Позволяет указать порт, на котором виртуальный сервер приложений или служба балансировки нагрузки будет прослушивать клиентское приложение Application Virtualization для настольных систем&#39;s запрос для пакета.</span><span class="sxs-lookup"><span data-stu-id="27d30-126">Enables you to specify the port on which the virtual application server or the load balancer will listen for an Application Virtualization Desktop Client&#39;s request for the package.</span></span> <span data-ttu-id="27d30-127">Эти сведения необходимы для создания пакета, но его можно изменить.</span><span class="sxs-lookup"><span data-stu-id="27d30-127">This information is required to create a package, but you can change it.</span></span> <span data-ttu-id="27d30-128">Порт по умолчанию — 554.</span><span class="sxs-lookup"><span data-stu-id="27d30-128">The default port is 554.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="27d30-129">Путь</span><span class="sxs-lookup"><span data-stu-id="27d30-129">Path</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27d30-130">Позволяет указать относительный путь на виртуальном сервере приложений, где хранится пакет программного обеспечения и из которого он будет передаваться в поток.</span><span class="sxs-lookup"><span data-stu-id="27d30-130">Enables you to specify the relative path on the virtual application server where the software package is stored and from which it will be streamed.</span></span> <span data-ttu-id="27d30-131">Эти сведения необходимы для создания пакета, если SFT-файл будет храниться в подкаталоге содержимого; в противном случае эта информация не является обязательной.</span><span class="sxs-lookup"><span data-stu-id="27d30-131">This information is required to create a package if the SFT file will be stored in a subdirectory of CONTENT; otherwise, this information is not required.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="27d30-132">Операционные системы</span><span class="sxs-lookup"><span data-stu-id="27d30-132">Operating Systems</span></span>


<span data-ttu-id="27d30-133">С помощью элементов управления **операционной системы** Определите требования к операционной системе для приложения.</span><span class="sxs-lookup"><span data-stu-id="27d30-133">Use the **Operating Systems** controls to specify the application's operating system requirements.</span></span> <span data-ttu-id="27d30-134">Если клиент для классической версии Application Virtualization не может поддерживать ни одну из выбранных операционных систем, приложение не запустится.</span><span class="sxs-lookup"><span data-stu-id="27d30-134">If an Application Virtualization Desktop Client cannot support any of the selected operating systems, the application will not start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27d30-135">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="27d30-135">Controls</span></span></th>
<th align="left"><span data-ttu-id="27d30-136">Описание</span><span class="sxs-lookup"><span data-stu-id="27d30-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="27d30-137">Доступные операционные системы</span><span class="sxs-lookup"><span data-stu-id="27d30-137">Available Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27d30-138">Отображает список операционных систем, которые могут поддерживать приложения в пакете.</span><span class="sxs-lookup"><span data-stu-id="27d30-138">Displays a list of operating systems that can support the applications in the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="27d30-139">Выбранные операционные системы</span><span class="sxs-lookup"><span data-stu-id="27d30-139">Selected Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27d30-140">Отображает список выбранных операционных систем, которые поддерживают приложения в пакете.</span><span class="sxs-lookup"><span data-stu-id="27d30-140">Displays a list of selected operating systems that support the applications in the package.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="27d30-141">Параметры вывода</span><span class="sxs-lookup"><span data-stu-id="27d30-141">Output Options</span></span>


<span data-ttu-id="27d30-142">С помощью элементов управления **параметрами вывода** укажите параметры вывода для устанавливаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="27d30-142">Use the **Output Options** controls to specify the output options for the application to be installed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27d30-143">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="27d30-143">Control</span></span></th>
<th align="left"><span data-ttu-id="27d30-144">Описание</span><span class="sxs-lookup"><span data-stu-id="27d30-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="27d30-145">Алгоритм сжатия</span><span class="sxs-lookup"><span data-stu-id="27d30-145">Compression Algorithm</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27d30-146">Используется для выбора метода сжатия SFT-файла при потоковой передаче по сети.</span><span class="sxs-lookup"><span data-stu-id="27d30-146">Use to select the method for compressing the SFT file for streaming across a network.</span></span> <span data-ttu-id="27d30-147">Выберите один из указанных ниже методов сжатия.</span><span class="sxs-lookup"><span data-stu-id="27d30-147">Select one of the following compression methods:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="27d30-148">Сжатый </strong> — файл SFT сжимается в <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> </a> формате zlib.</span><span class="sxs-lookup"><span data-stu-id="27d30-148">Compressed</strong>—Specifies that the SFT file be compressed in the <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)">ZLIB</a> format.</span></span></p></li>
<li><p><strong><span data-ttu-id="27d30-149">Не сжимается </strong> (значение по умолчанию); указывает на то, что файл SFT не сжимается.</span><span class="sxs-lookup"><span data-stu-id="27d30-149">Not Compressed</strong>—The default; specifies that the SFT file not be compressed.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="27d30-150">Применение дескрипторов безопасности</span><span class="sxs-lookup"><span data-stu-id="27d30-150">Enforce Security Descriptors</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27d30-151">Установите этот флажок, чтобы применить дескрипторы безопасности приложений в пакете после его развертывания на клиенте.</span><span class="sxs-lookup"><span data-stu-id="27d30-151">Select to enforce security descriptors of the applications in the package after it is deployed to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="27d30-152">Создание пакета установщика Microsoft Windows (MSI)</span><span class="sxs-lookup"><span data-stu-id="27d30-152">Generate Microsoft Windows Installer (MSI) Package</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27d30-153">Выберите, чтобы установить или развернуть последовательный пакет приложения с помощью установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="27d30-153">Select to install or deploy a sequenced application package with the Windows Installer.</span></span> <span data-ttu-id="27d30-154">Если вы внесли какие – либо изменения с помощью секвенсора, изменения не будут включены в файл установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="27d30-154">If you have made any changes using the sequencer the changes will not be included with the Windows Installer file.</span></span> <span data-ttu-id="27d30-155">Файл установщика Windows всегда будет создан с помощью SFT – файла, сохраненного на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="27d30-155">The Windows Installer file will always be created using the .sft file saved on the hard disk.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="27d30-156">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="27d30-156">Related topics</span></span>


[<span data-ttu-id="27d30-157">Изменение свойств развертывания</span><span class="sxs-lookup"><span data-stu-id="27d30-157">How to Change Deployment Properties</span></span>](how-to-change-deployment-properties.md)

[<span data-ttu-id="27d30-158">Консоль Sequencer</span><span class="sxs-lookup"><span data-stu-id="27d30-158">Sequencer Console</span></span>](sequencer-console.md)









