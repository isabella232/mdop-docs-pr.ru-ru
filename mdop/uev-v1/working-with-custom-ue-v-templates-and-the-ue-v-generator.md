---
title: Работа с пользовательскими шаблонами UE-V и генератором UE-V
description: Работа с пользовательскими шаблонами UE-V и генератором UE-V
author: dansimp
ms.assetid: 7bb2583a-b032-4800-9bf9-eb33528e1d0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: db5387254842bfdcf3898089bc12a8e929e3813a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823979"
---
# <span data-ttu-id="b7e25-103">Работа с пользовательскими шаблонами UE-V и генератором UE-V</span><span class="sxs-lookup"><span data-stu-id="b7e25-103">Working with Custom UE-V Templates and the UE-V Generator</span></span>


<span data-ttu-id="b7e25-104">Чтобы перемещать приложения между компьютерами пользователя, в Microsoft User Experience Virtualization (UE-V) используются *шаблоны расположений параметров*.</span><span class="sxs-lookup"><span data-stu-id="b7e25-104">In order to roam applications between user computers, Microsoft User Experience Virtualization (UE-V) uses *settings location templates*.</span></span> <span data-ttu-id="b7e25-105">Некоторые шаблоны расположений параметров входят в состав виртуализации взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="b7e25-105">Some settings location templates are included with User Experience Virtualization.</span></span> <span data-ttu-id="b7e25-106">Вы также можете создавать, изменять и проверять шаблоны расположений настраиваемых параметров с помощью генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="b7e25-106">You can also create, edit, or validate custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="b7e25-107">Генератор UE-V наблюдает за приложением для выяснения и захвата расположений, в которых приложение сохраняет параметры.</span><span class="sxs-lookup"><span data-stu-id="b7e25-107">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="b7e25-108">Отслеживаемое приложение должно быть традиционным приложением.</span><span class="sxs-lookup"><span data-stu-id="b7e25-108">The application being monitored must be a traditional application.</span></span> <span data-ttu-id="b7e25-109">Генератор UE-V не может создать шаблон расположения параметров для следующих типов приложений:</span><span class="sxs-lookup"><span data-stu-id="b7e25-109">The UE-V Generator cannot create a settings location template for the following application types:</span></span>

-   <span data-ttu-id="b7e25-110">Виртуализированные приложения</span><span class="sxs-lookup"><span data-stu-id="b7e25-110">Virtualized applications</span></span>

-   <span data-ttu-id="b7e25-111">Приложение, предлагаемое в службах терминалов</span><span class="sxs-lookup"><span data-stu-id="b7e25-111">Application offered through terminal services</span></span>

-   <span data-ttu-id="b7e25-112">Приложения Java</span><span class="sxs-lookup"><span data-stu-id="b7e25-112">Java applications</span></span>

-   <span data-ttu-id="b7e25-113">Приложения для Windows 8</span><span class="sxs-lookup"><span data-stu-id="b7e25-113">Windows 8 applications</span></span>

## <span data-ttu-id="b7e25-114">Создайте шаблонов расположения параметров UE-V с помощью генератора UE-V</span><span class="sxs-lookup"><span data-stu-id="b7e25-114">Create UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="b7e25-115">Использование генераторов UE-V для создания шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="b7e25-115">How to use the UE-V Generator to create settings location templates.</span></span>

[<span data-ttu-id="b7e25-116">Создайте шаблонов расположения параметров UE-V с помощью генератора UE-V</span><span class="sxs-lookup"><span data-stu-id="b7e25-116">Create UE-V Settings Location Templates with the UE-V Generator</span></span>](create-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## <span data-ttu-id="b7e25-117">Изменение шаблонов расположения параметров UE-V с помощью генератора UE-V</span><span class="sxs-lookup"><span data-stu-id="b7e25-117">Edit UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="b7e25-118">Инструкции по использованию UE-V Generator для изменения шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="b7e25-118">How to use the UE-V Generator to edit settings location templates.</span></span>

[<span data-ttu-id="b7e25-119">Изменение шаблонов расположения параметров UE-V с помощью генератора UE-V</span><span class="sxs-lookup"><span data-stu-id="b7e25-119">Edit UE-V Settings Location Templates with the UE-V Generator</span></span>](edit-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## <span data-ttu-id="b7e25-120">Проверка шаблонов расположения параметров UE-V с помощью генератора UE-V</span><span class="sxs-lookup"><span data-stu-id="b7e25-120">Validate UE-V Settings Location Templates with UE-V Generator</span></span>


<span data-ttu-id="b7e25-121">Как использовать генератор UE-V для проверки шаблонов расположений параметров, измененных вне генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="b7e25-121">How to use the UE-V Generator to validate settings location templates modified outside the UE-V Generator.</span></span>

[<span data-ttu-id="b7e25-122">Проверка шаблонов расположения параметров UE-V с помощью генератора UE-V</span><span class="sxs-lookup"><span data-stu-id="b7e25-122">Validate UE-V Settings Location Templates with UE-V Generator</span></span>](validate-ue-v-settings-location-templates-with-ue-v-generator.md)

## <a href="" id="bkmk-standardnonstandardsettingslocations"></a><span data-ttu-id="b7e25-123">Расположение стандартных и нестандартных параметров</span><span class="sxs-lookup"><span data-stu-id="b7e25-123">Standard and Nonstandard settings locations</span></span>


<span data-ttu-id="b7e25-124">Генератор UE-V помогает определить, где приложения будут искать файлы параметров и параметры реестра, которые используются приложениями для хранения сведений о параметрах.</span><span class="sxs-lookup"><span data-stu-id="b7e25-124">The UE-V Generator helps you identify where applications look for settings files and registry settings that applications use to store settings information.</span></span> <span data-ttu-id="b7e25-125">Вы можете использовать генератор UE-V для открытия приложения в процессе обнаружения, чтобы зафиксировать параметры в стандартных каталогах.</span><span class="sxs-lookup"><span data-stu-id="b7e25-125">You can use the UE-V Generator to open the application as part of the discovery process to capture settings in standard locations.</span></span> <span data-ttu-id="b7e25-126">Стандартные расположения включают в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="b7e25-126">Standard locations include the following:</span></span>

-   <span data-ttu-id="b7e25-127">**Параметры реестра** — расположение в реестре в разделе **hKey \ _CURRENT \ _USER**</span><span class="sxs-lookup"><span data-stu-id="b7e25-127">**Registry Settings** – Registry locations under **HKEY\_CURRENT\_USER**</span></span>

-   <span data-ttu-id="b7e25-128">**Файлы параметров приложения** : файлы, сохраненные в разделе \ \ **Пользователи** \ \ \ [имя пользователя \] \ \ **AppData**  \\  **роуминг**</span><span class="sxs-lookup"><span data-stu-id="b7e25-128">**Application Settings Files** – Files stored under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**</span></span>

<span data-ttu-id="b7e25-129">Генератор UE-V исключает расположения, в которых обычно хранятся файлы программного обеспечения приложений, не предназначенные для пользователей и сред.</span><span class="sxs-lookup"><span data-stu-id="b7e25-129">The UE-V Generator excludes locations which commonly store application software files do not roam well between user computers or environments.</span></span> <span data-ttu-id="b7e25-130">Генератор UE-V исключает указанные ниже места.</span><span class="sxs-lookup"><span data-stu-id="b7e25-130">The UE-V Generator excludes these locations.</span></span> <span data-ttu-id="b7e25-131">Исключенные расположения описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="b7e25-131">Excluded locations are as follows:</span></span>

-   <span data-ttu-id="b7e25-132">Раздел HKEY \ _CURRENT \ _USER разделы реестра и файлы, к которым пользователь, выполнивший вход, не может записать значения</span><span class="sxs-lookup"><span data-stu-id="b7e25-132">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="b7e25-133">Раздел HKEY \ _CURRENT \ _USER разделы реестра и файлы, связанные с основными функциями операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="b7e25-133">HKEY\_CURRENT\_USER registry keys and files that are associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="b7e25-134">Все разделы реестра, которые находятся в кусте HKEY \ _LOCAL \ _MACHINE (требуются права администратора и для них может потребоваться соглашение UAC)</span><span class="sxs-lookup"><span data-stu-id="b7e25-134">All registry keys that are located in the HKEY\_LOCAL\_MACHINE hive (Requires Administrator rights and might require UAC agreement to set)</span></span>

-   <span data-ttu-id="b7e25-135">Файлы, расположенные в каталогах программных файлов (требуются права администратора, и для них может потребоваться настройка соглашения UAC)</span><span class="sxs-lookup"><span data-stu-id="b7e25-135">Files that are located in Program Files directories (Requires Administrator rights and might require UAC agreement to set)</span></span>

-   <span data-ttu-id="b7e25-136">Файлы, находящиеся в списке Пользователи \ \ \ [имя пользователя \] \ \ AppData \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="b7e25-136">Files located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="b7e25-137">Файлы операционной системы Windows, расположенные в папке% systemroot% (требуются права администратора, и может потребоваться настройка соглашения UAC)</span><span class="sxs-lookup"><span data-stu-id="b7e25-137">Windows operating system files that are located in %systemroot% (Requires Administrator rights and might require UAC agreement to set)</span></span>

<span data-ttu-id="b7e25-138">Если для перемещения параметров приложения требуются разделы реестра и файлы, хранящиеся в этих расположениях, вы можете вручную добавить Исключенные расположения в шаблон расположения параметров в процессе создания шаблона.</span><span class="sxs-lookup"><span data-stu-id="b7e25-138">If registry keys and files stored in these locations are required in order to roam application settings, you can manually add the excluded locations to the settings location template during the template creation process.</span></span>

## <span data-ttu-id="b7e25-139">Другие ресурсы для этого продукта</span><span class="sxs-lookup"><span data-stu-id="b7e25-139">Other resources for this product</span></span>


[<span data-ttu-id="b7e25-140">Операции в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="b7e25-140">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

[<span data-ttu-id="b7e25-141">Администрирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="b7e25-141">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

 

 





