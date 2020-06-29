---
title: Новые возможности AGPM4.0
description: Новые возможности AGPM4.0
author: dansimp
ms.assetid: 31775f7f-a59c-4e64-a875-0adc9f5bc835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 82b4445a7d22fb7c1ef4f42d896f11908a22f2f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820102"
---
# <span data-ttu-id="902d0-103">Новые возможности AGPM4.0</span><span class="sxs-lookup"><span data-stu-id="902d0-103">What's New in AGPM 4.0</span></span>


<span data-ttu-id="902d0-104">Расширенное управление групповыми политиками Microsoft 4.0 включает в себя новые функции, позволяющие искать объекты групповой политики (GPO), фильтровать список GPO, экспортировать и импортировать их в другой лес, а также устанавливать параметры расширенного управления групповыми политиками на компьютерах с операционной системой Windows7 и Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="902d0-104">Microsoft Advanced Group Policy Management (AGPM)4.0 includes new features that let you search for Group Policy Objects (GPOs), filter the list of GPOs displayed, export and import a GPO to a different forest, and install AGPM on computers running Windows7 and Windows Server2008R2.</span></span>

## <span data-ttu-id="902d0-105">Поиск и фильтрация GPO</span><span class="sxs-lookup"><span data-stu-id="902d0-105">Search and filter GPOs</span></span>


<span data-ttu-id="902d0-106">В расширенном управлении групповыми политиками 4,0 вы можете искать определенные атрибуты в списке объектов групповой политики, чтобы отфильтровать список объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="902d0-106">In AGPM 4.0, you can search the list of GPOs for specific attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="902d0-107">Например, можно выполнить поиск объектов групповой политики с определенным именем, состоянием или примечанием.</span><span class="sxs-lookup"><span data-stu-id="902d0-107">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="902d0-108">Вы также можете искать объекты GPO, которые были изменены администратором групповой политики или определенной датой.</span><span class="sxs-lookup"><span data-stu-id="902d0-108">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

<span data-ttu-id="902d0-109">Вы можете создать строку сложного поиска с помощью атрибута "формат *GPO 1": Поиск текста 1, атрибут 2: Поиск текста 2...*, где атрибут GPO — это заголовок любого столбца в списке объектов групповой политики в расширенном форматировании.</span><span class="sxs-lookup"><span data-stu-id="902d0-109">You can create a complex search string by using the format *GPO attribute 1: search text 1 GPO attribute 2: search text 2…*, where a GPO attribute is any column heading in the list of GPOs in AGPM.</span></span> <span data-ttu-id="902d0-110">Например, чтобы найти все GPO с именами, в том числе возвращаемым текстом "MyGPO", и Дата последнего изменения пользователем Editor03, введите в поле поиска следующее: **Имя: MyGPO состояние:\*\*\*\*возвращено\*\*\*\*Изменено: Editor03**.</span><span class="sxs-lookup"><span data-stu-id="902d0-110">For example, to search for all GPOs with names including the text "MyGPO" that are checked in and were last changed by the user Editor03, you would type the following in the Search box: **name: MyGPO state:\*\*\*\*checked in\*\*\*\*changed by: Editor03**.</span></span> <span data-ttu-id="902d0-111">Поиск вернет частичные совпадения, чтобы можно было ввести часть имени или имени объекта групповой политики, а также просмотреть список всех GPO, включающих этот текст в свое имя.</span><span class="sxs-lookup"><span data-stu-id="902d0-111">The search returns partial matches so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="902d0-112">Кроме того, вы можете использовать те же специальные термины, которые доступны при поиске в Windows для поиска объектов групповой политики, измененных на определенную дату или диапазон дат.</span><span class="sxs-lookup"><span data-stu-id="902d0-112">Additionally, you can use the same special terms available when you search in Windows to search for GPOs changed on a specific date or range of dates.</span></span> <span data-ttu-id="902d0-113">Например, **изменить дату:\*\*\*\*lastmonth** или **изменить дату:\*\*\*\*thisweek**.</span><span class="sxs-lookup"><span data-stu-id="902d0-113">For example, **change date:\*\*\*\*lastmonth** or **change date:\*\*\*\*thisweek**.</span></span>

## <span data-ttu-id="902d0-114">Экспорт и импорт объектов групповой политики в различные леса</span><span class="sxs-lookup"><span data-stu-id="902d0-114">Export and import GPOs to different forests</span></span>


<span data-ttu-id="902d0-115">С помощью расширенного управления групповыми политиками 4,0 можно скопировать управляемый объект групповой политики из домена в одном лесе в домен во втором лесе.</span><span class="sxs-lookup"><span data-stu-id="902d0-115">Using AGPM 4.0, you can copy a controlled GPO from a domain in one forest to a domain in a second forest.</span></span> <span data-ttu-id="902d0-116">Например, вы можете экспортировать объект групповой политики из домена в одном лесе в CAB-файл с помощью функции РАСШИРЕНного использования ключа, скопировать этот CAB-файл на устройство USB, подключить его к компьютеру в домене во втором лесе и импортировать объект групповой политики в многоключную версию домена во втором лесе.</span><span class="sxs-lookup"><span data-stu-id="902d0-116">For example, you can export a GPO from a domain in one forest to a CAB file by using AGPM, copy that CAB file to a USB drive, plug the USB drive into a computer in a domain in a second forest, and import the GPO into AGPM in a domain in the second forest.</span></span> <span data-ttu-id="902d0-117">Вы можете импортировать объект групповой политики как новый управляемый объект групповой политики или импортировать его, чтобы заменить параметры существующего объекта групповой политики, который извлечен.</span><span class="sxs-lookup"><span data-stu-id="902d0-117">You can either import the GPO as a new controlled GPO, or import it to replace the settings of an existing GPO that is checked out.</span></span>

## <span data-ttu-id="902d0-118">Поддержка для Windows Server 2008 R2 и Windows 7</span><span class="sxs-lookup"><span data-stu-id="902d0-118">Support for Windows Server 2008 R2 and Windows 7</span></span>


<span data-ttu-id="902d0-119">4,0 РАСШИРЕНная поддержка Server2008R2 и Windows7 поддерживается для Windows Server2008 и WindowsVista® с поддержкой служб Pack1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="902d0-119">AGPM 4.0 supports Windows Server2008R2 and Windows7, yet still supports Windows Server2008 and WindowsVista® with Service Pack1 (SP1).</span></span> <span data-ttu-id="902d0-120">Тем не менее, в смешанной среде есть ограничения, включающие более новые и более ранние операционные системы, как показано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="902d0-120">However, there are limitations in a mixed environment that includes both the newer and older operating systems, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="902d0-121">Операционная система, на которой работает сервер РАСШИРЕНного выбора 4,0</span><span class="sxs-lookup"><span data-stu-id="902d0-121">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="902d0-122">Операционная система, в которой работает клиентская служба РАСШИРЕНного выбора 4,0</span><span class="sxs-lookup"><span data-stu-id="902d0-122">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="902d0-123">Состояние поддержки РАСШИРЕНной версии 4,0</span><span class="sxs-lookup"><span data-stu-id="902d0-123">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="902d0-124">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="902d0-124">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="902d0-125">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="902d0-125">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="902d0-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="902d0-126">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="902d0-127">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="902d0-127">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="902d0-128">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="902d0-128">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="902d0-129">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="902d0-129">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="902d0-130">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="902d0-130">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="902d0-131">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="902d0-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="902d0-132">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="902d0-132">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="902d0-133">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="902d0-133">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="902d0-134">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="902d0-134">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="902d0-135">Поддерживается, но не может сообщать или изменять параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="902d0-135">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





