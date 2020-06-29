---
title: Определение количества и типов рабочих областей MED-V
description: Определение количества и типов рабочих областей MED-V
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827262"
---
# <span data-ttu-id="aac13-103">Определение количества и типов рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="aac13-103">Identifying the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="aac13-104">MED-V создает виртуальную среду для работающих приложений, которым требуется Windows XP или которой требуется версия Internet Explorer, отличающаяся от версии на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="aac13-104">MED-V creates a virtual environment for running applications that require Windows XP or that require a version of Internet Explorer that differs from the version on the host computer.</span></span> <span data-ttu-id="aac13-105">Эта виртуальная среда называется рабочей областью MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-105">This virtual environment is known as a MED-V workspace.</span></span>

<span data-ttu-id="aac13-106">В зависимости от требований к совместимости приложений, которые сталкиваются вашей организацией при переходе на Windows 7, для некоторых пользователей и отделов может потребоваться Рабочая область MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-106">Depending on the application compatibility requirements faced by your organization as you migrate to Windows 7, only certain users or departments might require MED-V workspaces.</span></span> <span data-ttu-id="aac13-107">При планировании развертывания необходимо определить количество рабочих областей MED-V, необходимых для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="aac13-107">As you plan your deployment, you have to determine the number of MED-V workspaces required in your enterprise.</span></span> <span data-ttu-id="aac13-108">Кроме того, необходимо определить требования для каждой рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-108">You also have to define the requirements of each MED-V workspace.</span></span>

## <span data-ttu-id="aac13-109">Определение числа и типов рабочих областей для MED-V</span><span class="sxs-lookup"><span data-stu-id="aac13-109">Identify the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="aac13-110">Определите компьютеры и группы в Организации, для которых будут создаваться рабочие области MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-110">Identify the computers and groups in your enterprise for which you will be creating MED-V workspaces.</span></span> <span data-ttu-id="aac13-111">Обычно это пользователи, которым требуется доступ к приложениям, которые не могут быть перенесены в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aac13-111">Typically, these are the users who require access to those applications that cannot be migrated to Windows 7.</span></span> <span data-ttu-id="aac13-112">Определите приложения, которые не могут быть подвергнуты миграции, и пользователи, которым требуется рабочая область MED-V для выполнения этих приложений.</span><span class="sxs-lookup"><span data-stu-id="aac13-112">Identify those applications that cannot be migrated and the users who require a MED-V workspace to run these applications.</span></span>

<span data-ttu-id="aac13-113">Кроме того, вы также можете использовать адреса интрасети, которые еще не были оптимизированы для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aac13-113">You might also have intranet addresses that have not yet been optimized for Windows 7.</span></span> <span data-ttu-id="aac13-114">Рабочая область MED-V обеспечивает браузер Internet Explorer, с помощью которого конечные пользователи смогут лучше получить доступ к веб-адресам, которые еще не готовы к переходу на Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aac13-114">The MED-V workspace provides an Internet Explorer browser through which end users can better access those web addresses that are not yet ready for the migration to Windows 7.</span></span> <span data-ttu-id="aac13-115">По мере подготовки и планирования развертывания MED-V вам потребуется идентифицировать и скомпилировать список URL-адресов, чтобы перенаправить его из Internet Explorer на главный компьютер в Internet Explorer в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-115">As you are preparing and planning your MED-V deployment, you will have to identify and compile a list of the URL addresses to redirect from Internet Explorer on the host computer to Internet Explorer in the MED-V workspace.</span></span>

<span data-ttu-id="aac13-116">Наконец, необходимо оценить требования к дисковому пространству.</span><span class="sxs-lookup"><span data-stu-id="aac13-116">Finally, you have to evaluate your disk space requirements.</span></span> <span data-ttu-id="aac13-117">Большинство рабочих областей MED-V — 2 гигабайта (ГБ) или больше.</span><span class="sxs-lookup"><span data-stu-id="aac13-117">Most MED-V workspaces are 2 gigabytes (GB) or larger.</span></span> <span data-ttu-id="aac13-118">Свободное место на диске системы может быть быстро потреблено в зависимости от количества пользователей и конфигурации MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-118">The available disk space on a system can be consumed quickly, depending on the number of users and the configuration of MED-V.</span></span> <span data-ttu-id="aac13-119">Кроме того, предпочтительный способ распространения для вашей компании может потребовать дополнительного места.</span><span class="sxs-lookup"><span data-stu-id="aac13-119">Also, your company’s preferred method of distribution can require additional space.</span></span> <span data-ttu-id="aac13-120">Как правило, вы должны освободить не менее 10 ГБ места на диске для рабочей области MED-V, но это может сильно различаться в зависимости от размера изображения.</span><span class="sxs-lookup"><span data-stu-id="aac13-120">Generally, you should free a minimum of 10 GB of disk space for a MED-V workspace, but this varies greatly, depending on the size of the image.</span></span>

### <span data-ttu-id="aac13-121">Расчет требований к дисковому пространству для рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="aac13-121">Calculate the Disk Space Requirements for MED-V Workspaces</span></span>

<span data-ttu-id="aac13-122">Для рабочей области MED-V требуется объем памяти и места на диске на компьютере, на котором установлен этот сервер.</span><span class="sxs-lookup"><span data-stu-id="aac13-122">A MED-V workspace requires memory and disk space from the host computer on which it is installed.</span></span> <span data-ttu-id="aac13-123">На узле должны быть не менее 2 ГБ свободного места на диске.</span><span class="sxs-lookup"><span data-stu-id="aac13-123">At a minimum, 2 GB of disk space are required on the host.</span></span> <span data-ttu-id="aac13-124">Место на диске — переменная, зависящая от количества приложений и данных в рабочей области для пользователей MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-124">Disk space is variable and depends on the number of applications and the data in a user’s MED-V workspace.</span></span>

<span data-ttu-id="aac13-125">Рекомендуем вам не менее 10 ГБ места на диске для MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-125">We recommend a minimum of 10 GB of disk space for MED-V.</span></span> <span data-ttu-id="aac13-126">Это значение позволяет создать базовую рабочую область Windows XP и некоторые базовые установленные приложения и перенаправление веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="aac13-126">This amount allows for a basic Windows XP workspace and some basic installed applications and web redirection.</span></span> <span data-ttu-id="aac13-127">Кроме того, он предоставляет доступное пространство для основного диска подкачки.</span><span class="sxs-lookup"><span data-stu-id="aac13-127">It also provides available space for the host swap drive.</span></span> <span data-ttu-id="aac13-128">В базовой конфигурации MED-V и единая развернутая Рабочая область MED-V потребляет от 6 до 8 ГБ.</span><span class="sxs-lookup"><span data-stu-id="aac13-128">In a basic configuration, MED-V and a single deployed MED-V workspace consume as much as 6 to 8 GB.</span></span> <span data-ttu-id="aac13-129">Если вы включите большое количество приложений в рабочую область MED-V или используете несколько пользователей на компьютере, вы можете использовать указанные ниже вычисления для более точного определения места на диске, требуемого для рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-129">If you include lots of applications on the MED-V workspace or have more than one user per computer, then you can use the following calculation to more accurately determine the disk space your MED-V workspace requires:</span></span>

*<span data-ttu-id="aac13-130">Базовый VHD + (пользователь на компьютере x (разница с диском + сохраненное состояние))</span><span class="sxs-lookup"><span data-stu-id="aac13-130">Base VHD + (User per computer x (Difference Disk + Saved State))</span></span>*

<span data-ttu-id="aac13-131">Чтобы вычислить требуемое место на диске, определите следующее:</span><span class="sxs-lookup"><span data-stu-id="aac13-131">To calculate the required disk space, determine the following:</span></span>

-   <span data-ttu-id="aac13-132">**Размер базового** виртуального жесткого диска, который использовался для создания рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-132">**Size of the base VHD** – the virtual hard disk that was used to create the MED-V workspace.</span></span>

    <span data-ttu-id="aac13-133">**Важно!**  Не используйте размер MEDV-файла для вычисления, так как файл MEDV сжимается.</span><span class="sxs-lookup"><span data-stu-id="aac13-133">**Important** Do not use the .medv file size for your calculation because the .medv file is compressed.</span></span>

     

-   <span data-ttu-id="aac13-134">**Пользователи на компьютере** — med-v создают рабочую область MED-v для каждого пользователя на компьютере; Рабочая область MED-V потребляет место на диске, пока каждый пользователь входит в систему, и создается рабочая область MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-134">**Users per computer** – MED-V creates a MED-V workspace for each user on a computer; the MED-V workspace consumes disk space as each user logs on and the MED-V workspace is created.</span></span>

-   <span data-ttu-id="aac13-135">**Размер разностного диска** , который используется для отслеживания различий между базовыми и VHD-дисками.</span><span class="sxs-lookup"><span data-stu-id="aac13-135">**Size of the differencing disk** – used to track the difference from the base VHD.</span></span> <span data-ttu-id="aac13-136">Этот размер меняется при добавлении приложений и обновлений программного обеспечения на виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="aac13-136">This size varies as you add applications and software updates to the virtual hard disk.</span></span> <span data-ttu-id="aac13-137">Разностный диск создается для каждого пользователя MED-V в первый раз при запуске MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-137">A differencing disk is created for each MED-V user when they start MED-V for the first time.</span></span>

-   <span data-ttu-id="aac13-138">**Размер сохраненного файла состояния** — используется для сохранения состояния виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aac13-138">**Size of the Saved State file** – used to maintain state in the virtual machine.</span></span> <span data-ttu-id="aac13-139">Как правило, это немного больше, чем выделенный объем ОЗУ для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aac13-139">Typically, this is just a bit larger than the allocated RAM for the virtual machine.</span></span> <span data-ttu-id="aac13-140">Например, 1 ГБ выделения ОЗУ создает файл размером около 1 081 000 КБ.</span><span class="sxs-lookup"><span data-stu-id="aac13-140">For example, 1 GB of RAM allocated creates a file about 1,081,000 KB.</span></span>

<span data-ttu-id="aac13-141">В следующем примере показан расчет на основе трех пользователей рабочей области MED-V с виртуальным жестким диском 2,6 ГБ.</span><span class="sxs-lookup"><span data-stu-id="aac13-141">The following example shows a calculation based on three users of a MED-V workspace that has a 2.6 GB virtual hard disk:</span></span>

*<span data-ttu-id="aac13-142">2,6 ГБ + (3 x (1,5 ГБ + 1 ГБ)) = 10,1 ГБ</span><span class="sxs-lookup"><span data-stu-id="aac13-142">2.6gb + (3 x (1.5gb + 1gb)) = 10.1gb</span></span>*

<span data-ttu-id="aac13-143">**Примечание**  Для проверки требований в среде MED-V рекомендуется вычислять требуемое пространство с помощью лабораторного развертывания.</span><span class="sxs-lookup"><span data-stu-id="aac13-143">**Note** A MED-V best practice is to calculate the required space by using a lab deployment to validate the requirements.</span></span>

 

### <span data-ttu-id="aac13-144">Поиск файлов для определения размера файла</span><span class="sxs-lookup"><span data-stu-id="aac13-144">Locate the Files to Determine File Size</span></span>

<span data-ttu-id="aac13-145">Следующие расположения содержат файлы для компьютера и параметры пользователя.</span><span class="sxs-lookup"><span data-stu-id="aac13-145">The following locations contain the files for the computer and user settings:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aac13-146">Тип</span><span class="sxs-lookup"><span data-stu-id="aac13-146">Type</span></span></th>
<th align="left"><span data-ttu-id="aac13-147">Location</span><span class="sxs-lookup"><span data-stu-id="aac13-147">Location</span></span></th>
<th align="left"><span data-ttu-id="aac13-148">Файлы</span><span class="sxs-lookup"><span data-stu-id="aac13-148">Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aac13-149">Базовый виртуальный жесткий диск</span><span class="sxs-lookup"><span data-stu-id="aac13-149">Base VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="aac13-150">%ProgramData%\Microsoft\Medv\Workspace</span><span class="sxs-lookup"><span data-stu-id="aac13-150">%ProgramData%\Microsoft\Medv\Workspace</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="aac13-151">InternalName </em> . VHD — где <em> internalname </em> — это имя виртуального жесткого диска, выбранного в упаковщике рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="aac13-151">InternalName</em>.vhd - Where <em>InternalName</em> is the name of the virtual hard disk that you selected in the MED-V Workspace Packager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aac13-152">Разностный диск</span><span class="sxs-lookup"><span data-stu-id="aac13-152">Differencing Disk</span></span></p></td>
<td align="left"><p><span data-ttu-id="aac13-153">%LocalAppData%\Microsoft\MEDV\v2\Virtual машины</span><span class="sxs-lookup"><span data-stu-id="aac13-153">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="aac13-154">WorkspaceName </em> . VHD</span><span class="sxs-lookup"><span data-stu-id="aac13-154">WorkspaceName</em>.vhd</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aac13-155">Файл сохраненного состояния</span><span class="sxs-lookup"><span data-stu-id="aac13-155">Saved State File</span></span></p></td>
<td align="left"><p><span data-ttu-id="aac13-156">%LocalAppData%\Microsoft\MEDV\v2\Virtual машины</span><span class="sxs-lookup"><span data-stu-id="aac13-156">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="aac13-157">WorkspaceName </em> . VSV</span><span class="sxs-lookup"><span data-stu-id="aac13-157">WorkspaceName</em>.vsv</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="aac13-158">Расчет требований к дисковому пространству для общих рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="aac13-158">Calculate the Disk Space Requirements for Shared MED-V Workspaces</span></span>

<span data-ttu-id="aac13-159">Если вы вычисляете общую рабочую область для MED-V на одном компьютере, число пользователей на компьютере всегда будет равно 1, поскольку MED-V настраивает только один разностный диск для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="aac13-159">If you are calculating for a shared MED-V workspace deployment on a single computer, then the number of users per computer in your calculation is always “1” because MED-V only configures a single differencing disk for all users.</span></span>

<span data-ttu-id="aac13-160">Вы можете найти разностный диск и файл сохраненного состояния для общих рабочих областей MED-V в%ProgramData%\\Microsoft\\Medv\\AllUsers.</span><span class="sxs-lookup"><span data-stu-id="aac13-160">You can find the differencing disk and the saved state file for shared MED-V workspaces in %ProgramData%\\Microsoft\\Medv\\AllUsers.</span></span>

## <span data-ttu-id="aac13-161">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="aac13-161">Related topics</span></span>


[<span data-ttu-id="aac13-162">Определение и планирование развертывания MED-V</span><span class="sxs-lookup"><span data-stu-id="aac13-162">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

[<span data-ttu-id="aac13-163">Планирование MED-V</span><span class="sxs-lookup"><span data-stu-id="aac13-163">Planning for MED-V</span></span>](planning-for-med-v.md)

 

 





