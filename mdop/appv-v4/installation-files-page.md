---
title: Страница "Установочные файлы"
description: Страница "Установочные файлы"
author: dansimp
ms.assetid: b0aad26f-b143-4f09-87a1-9f016a23cb62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08a2e7318271503f072298ca137a1e65e16c0178
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816342"
---
# <span data-ttu-id="55758-103">Страница "Установочные файлы"</span><span class="sxs-lookup"><span data-stu-id="55758-103">Installation Files Page</span></span>


<span data-ttu-id="55758-104">На странице " **файлы установки** " можно указать файлы установки, которые использовались для создания виртуального пакета приложений, указанного на странице " **Выбор пакета** " этого мастера.</span><span class="sxs-lookup"><span data-stu-id="55758-104">Use the **Installation Files** page to specify the installation files that were used to create the virtual application package specified on the **Select Package** page of this wizard.</span></span> <span data-ttu-id="55758-105">Если вы создали виртуальный пакет приложения, содержащий несколько приложений, необходимо скопировать все необходимые файлы установки в одну папку на компьютере, на котором запущен Microsoft Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="55758-105">If you created a virtual application package that contains multiple applications, you should copy all required installation files to a single folder on the computer running the Microsoft Application Virtualization Sequencer.</span></span>

<span data-ttu-id="55758-106">Эта страница включает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="55758-106">This page contains the following elements:</span></span>

<a href="" id="original-installation-files"></a>**<span data-ttu-id="55758-107">Исходные файлы установки</span><span class="sxs-lookup"><span data-stu-id="55758-107">Original Installation Files</span></span>**  
<span data-ttu-id="55758-108">Нажмите кнопку **Обзор** , чтобы указать файлы установки, которые изначально использовались для создания виртуального пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="55758-108">Click **Browse** to specify the installation files that were originally used to create the virtual application package.</span></span> <span data-ttu-id="55758-109">Указанный родительский каталог должен быть сохранен на компьютере, на котором запущены программы Sequencer, и должен содержать все необходимые файлы установки или вложенные папки, содержащие установочные файлы.</span><span class="sxs-lookup"><span data-stu-id="55758-109">The parent directory you specify should be saved locally to the computer running the Sequencer and must contain all required installation files or subfolders that contain the installation files.</span></span> <span data-ttu-id="55758-110">Файлы установки могут содержаться в родительской папке или в любой из вложенных папок указанной родительской папки.</span><span class="sxs-lookup"><span data-stu-id="55758-110">The installation files can be contained in the parent folder or in any of the subfolders of the specified parent folder.</span></span>

<a href="" id="files-installed-on-local-system"></a>**<span data-ttu-id="55758-111">Файлы, установленные в локальной системе</span><span class="sxs-lookup"><span data-stu-id="55758-111">Files installed on local system</span></span>**  
<span data-ttu-id="55758-112">Нажмите кнопку **Обзор** , чтобы указать установочные файлы, которые были установлены локально на компьютере под управлением секвенсора.</span><span class="sxs-lookup"><span data-stu-id="55758-112">Click **Browse** to specify the installation files that have been installed locally on the computer running the Sequencer.</span></span> <span data-ttu-id="55758-113">Этот параметр можно выбрать только в том случае, если файлы установки приложения были установлены в расположение по умолчанию для приложения.</span><span class="sxs-lookup"><span data-stu-id="55758-113">You can only select this option if the application installation files have been installed to the application’s default location.</span></span>

<span data-ttu-id="55758-114">**Примечание**  Расположение для установки по умолчанию зависит от указанных ниже условий.</span><span class="sxs-lookup"><span data-stu-id="55758-114">**Note** The default installation location you provide depends on the following conditions:</span></span>

 

-   <span data-ttu-id="55758-115">Корневой каталог пакета, указанный при первоначальном создании пакета.</span><span class="sxs-lookup"><span data-stu-id="55758-115">The package root specified when the package was originally created.</span></span>

-   <span data-ttu-id="55758-116">Место установки, указанное в установщике Windows при первоначальном создании пакета.</span><span class="sxs-lookup"><span data-stu-id="55758-116">The installation location specified in the Windows Installer when the package was originally created.</span></span>

-   <span data-ttu-id="55758-117">Путь по умолчанию для установки приложения.</span><span class="sxs-lookup"><span data-stu-id="55758-117">The default application installation path.</span></span>

<span data-ttu-id="55758-118">Например, если заданный корневой каталог пакета — **Q:\\Office12** и во время установки, по умолчанию в качестве расположения для установки будет изменено **C:\\program Files Files\\Office12** на **Q:\\Office12**, тогда путь, указанный в процессе обновления, должен быть **c:\\program Files Files\\Office 12**.</span><span class="sxs-lookup"><span data-stu-id="55758-118">For example, if the package root specified is **Q:\\Office12** and during installation, the default installation location is changed from **C:\\Program Files\\Office12** to **Q:\\Office12**, then the path specified during dehydration must be **C:\\Program Files\\Office 12**.</span></span>

<span data-ttu-id="55758-119">Если заданный корневой каталог пакета — **Q:\\Microsoft** и во время установки, расположение для установки по умолчанию будет изменено с **C:\\program Files Files\\Office12** на **Q:\\Microsoft\\Office12**, а путь, указанный в процессе обновления, должен быть **c:\\program Files файлами**.</span><span class="sxs-lookup"><span data-stu-id="55758-119">If the package root specified is **Q:\\Microsoft** and during installation, the default installation location is changed from **C:\\Program Files\\Office12** to **Q:\\Microsoft\\Office12**, then the path specified during dehydration must be **C:\\Program Files**.</span></span>

<span data-ttu-id="55758-120">Когда вы создаете пакет с помощью ускорителя пакетов, каждый файл в пакете, например **Q:\\Office12\\file.txt** , обнаруживается на локальном компьютере, заменяя корневой **Q:\\Office12** пакета расположением по умолчанию, которое задается при создании ускорителя пакетов (например, **c:\\program Files Files\\Office12**).</span><span class="sxs-lookup"><span data-stu-id="55758-120">When you create a package using a package accelerator, each file in the package, for example **Q:\\Office12\\file.txt** is found on the local computer by replacing the package root **Q:\\Office12** with the default location specified when the Package Accelerator was created, for example, **C:\\Program Files\\Office12**.</span></span> <span data-ttu-id="55758-121">В предыдущем примере файл должен располагаться в **c:\\program files Files\\Office12\\file.txt**.</span><span class="sxs-lookup"><span data-stu-id="55758-121">In the previous example, the file should be located in **C:\\Program Files\\Office12\\file.txt**.</span></span>

## <span data-ttu-id="55758-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="55758-122">Related topics</span></span>


[<span data-ttu-id="55758-123">Мастер создания ускорителя пакетов (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="55758-123">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





