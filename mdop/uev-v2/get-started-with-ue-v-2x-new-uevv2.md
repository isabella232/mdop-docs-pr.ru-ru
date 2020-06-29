---
title: Начало работы с UE-V 2.x
description: Начало работы с UE-V 2.x
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823289"
---
# <span data-ttu-id="c2c52-103">Начало работы с UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="c2c52-103">Get Started with UE-V 2.x</span></span>


<span data-ttu-id="c2c52-104">Выполните действия, описанные в этом руководстве, для быстрого развертывания Microsoft User Experience Virtualization (UE-V) 2,0 или 2,1 в маленькой тестовой среде.</span><span class="sxs-lookup"><span data-stu-id="c2c52-104">Follow the steps in this guide to quickly deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 in a small test environment.</span></span> <span data-ttu-id="c2c52-105">Это поможет вам определить, является ли UE-V правильным решением для управления параметрами пользователей на нескольких устройствах в Организации.</span><span class="sxs-lookup"><span data-stu-id="c2c52-105">This helps you determine whether UE-V is the right solution to manage user settings across multiple devices within your enterprise.</span></span>

<span data-ttu-id="c2c52-106">**Примечание**  Информация в этом разделе более детально повторяется в оставшейся части документации.</span><span class="sxs-lookup"><span data-stu-id="c2c52-106">**Note** The information in this section is repeated in greater detail throughout the rest of the documentation.</span></span> <span data-ttu-id="c2c52-107">Таким образом, если вы уже знаете, что UE-V 2 является правильным решением и вам не нужно его оценивать, вы можете просто перейти вправо, чтобы [подготовить развертывание UE-v 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="c2c52-107">So if you already know that UE-V 2 is the right solution and you don’t need to evaluate it, you can just go right to [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span></span>

 

<span data-ttu-id="c2c52-108">Стандартная установка UE-V синхронизирует параметры Microsoft Windows и Office, заданные по умолчанию, и многие параметры приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="c2c52-108">The standard installation of UE-V synchronizes the default Microsoft Windows and Office settings and many Windows app settings.</span></span> <span data-ttu-id="c2c52-109">Убедитесь в том, что в тестовой среде есть два или более компьютеров, использующих доступ к сети, и вы будете оценивать UE-V всего за короткий период времени.</span><span class="sxs-lookup"><span data-stu-id="c2c52-109">Make sure your test environment includes two or more user computers that share network access and you’ll be evaluating UE-V in just a short time.</span></span>

-   <span data-ttu-id="c2c52-110">[Действие 1: Подтвердите необходимые требования](#step1): Убедитесь в том, что ваша среда может выполнять UE-V, в том числе сведения о поддерживаемых конфигурациях.</span><span class="sxs-lookup"><span data-stu-id="c2c52-110">[Step 1: Confirm Prerequisites](#step1): Make sure your environment is able to run UE-V, including details about supported configurations.</span></span>

-   <span data-ttu-id="c2c52-111">[Шаг 2: развертывание расположения хранилища параметров для UE-v 2](#step2). для всех развертываний UE-v требуется расположение для пакетов параметров, которые содержат синхронизированные значения параметров.</span><span class="sxs-lookup"><span data-stu-id="c2c52-111">[Step 2: Deploy the Settings Storage Location for UE-V 2](#step2): All UE-V deployments require a location for settings packages that contain the synchronized setting values.</span></span>

-   <span data-ttu-id="c2c52-112">[Шаг 3: развертывание агента UE-v 2](#step3). для синхронизации параметров с помощью UE-v устройства должны иметь установленный и запущенный агент UE-v.</span><span class="sxs-lookup"><span data-stu-id="c2c52-112">[Step 3: Deploy the UE-V 2 Agent](#step3): To synchronize settings using UE-V, devices must have the UE-V Agent installed and running.</span></span>

-   <span data-ttu-id="c2c52-113">[Шаг 4: Проверка развертывания пробных версий UE-v 2](#step4): выполнение нескольких тестов на двух компьютерах с установленным агентом UE-v и Узнайте, как работает UE-v.</span><span class="sxs-lookup"><span data-stu-id="c2c52-113">[Step 4: Test Your UE-V 2 Evaluation Deployment](#step4): Run a few tests on two computers that have the UE-V Agent installed and see how UE-V works.</span></span>

<span data-ttu-id="c2c52-114">Ну вот!</span><span class="sxs-lookup"><span data-stu-id="c2c52-114">That’s it!</span></span> <span data-ttu-id="c2c52-115">После выполнения этих действий вы сможете оценить, как UE-V может работать в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="c2c52-115">Once you follow the steps, you’ll be able to evaluate how UE-V can work in your enterprise.</span></span>

<span data-ttu-id="c2c52-116">**Дальнейшая оценка:** Вы также можете выполнить дополнительные действия, чтобы настроить некоторые бизнес-приложения третьих лиц и приложений для синхронизации параметров с помощью UE-V, как описано в статье [развертывание UE-v 2. x для настраиваемых приложений](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="c2c52-116">**Further evaluation:** You can also perform additional steps to configure some third-party and line-of-business applications to synchronize their settings using UE-V as detailed in [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <a href="" id="step1"></a><span data-ttu-id="c2c52-117">Действие 1: подтверждение предварительных требований</span><span class="sxs-lookup"><span data-stu-id="c2c52-117">Step 1: Confirm Prerequisites</span></span>


<span data-ttu-id="c2c52-118">Прежде чем продолжить, убедитесь в том, что в вашей среде есть требования для выполнения UE-V.</span><span class="sxs-lookup"><span data-stu-id="c2c52-118">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="c2c52-119">Операционная система</span><span class="sxs-lookup"><span data-stu-id="c2c52-119">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c2c52-120">Выпуск</span><span class="sxs-lookup"><span data-stu-id="c2c52-120">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c2c52-121">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="c2c52-121">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c2c52-122">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="c2c52-122">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c2c52-123">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c2c52-123">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c2c52-124">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="c2c52-124">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2c52-125">Windows7</span><span class="sxs-lookup"><span data-stu-id="c2c52-125">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-126">Лучшая, Корпоративная или профессиональная версия</span><span class="sxs-lookup"><span data-stu-id="c2c52-126">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-127">SP1</span><span class="sxs-lookup"><span data-stu-id="c2c52-127">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-128">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c2c52-128">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-129">Windows PowerShell 3,0 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="c2c52-129">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-130">.NET Framework 4 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="c2c52-130">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2c52-131">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="c2c52-131">Windows Server2008R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-132">Стандартная, Корпоративная, для центра обработки данных или веб-сервера</span><span class="sxs-lookup"><span data-stu-id="c2c52-132">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-133">SP1</span><span class="sxs-lookup"><span data-stu-id="c2c52-133">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-134">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c2c52-134">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-135">Windows PowerShell 3,0 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="c2c52-135">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-136">.NET Framework 4 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="c2c52-136">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2c52-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c2c52-137">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-138">Enterprise или Pro</span><span class="sxs-lookup"><span data-stu-id="c2c52-138">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-139">Нет</span><span class="sxs-lookup"><span data-stu-id="c2c52-139">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-140">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c2c52-140">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-141">Windows PowerShell 3,0 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="c2c52-141">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-142">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="c2c52-142">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2c52-143">Windows Server 2012 или Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c2c52-143">Windows Server 2012 or Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-144">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="c2c52-144">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-145">Нет</span><span class="sxs-lookup"><span data-stu-id="c2c52-145">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-146">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c2c52-146">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-147">Windows PowerShell 3,0 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="c2c52-147">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-148">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="c2c52-148">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2c52-149">Windows 10, до 1607 verison</span><span class="sxs-lookup"><span data-stu-id="c2c52-149">Windows 10, pre-1607 verison</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-150">Enterprise или Pro</span><span class="sxs-lookup"><span data-stu-id="c2c52-150">Enterprise or Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c2c52-151">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c2c52-151">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-152">Windows PowerShell 3,0 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="c2c52-152">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-153">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="c2c52-153">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2c52-154">Windows Server2016</span><span class="sxs-lookup"><span data-stu-id="c2c52-154">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-155">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="c2c52-155">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-156">Нет</span><span class="sxs-lookup"><span data-stu-id="c2c52-156">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-157">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c2c52-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-158">Windows PowerShell 3,0 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="c2c52-158">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2c52-159">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="c2c52-159">.NET Framework 4.5</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2c52-160">**Примечание.** Начиная с Windows 10 версии 1607, UE-V входит в [Windows 10 для предприятий](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) и больше не входит в пакет оптимизации рабочей среды Майкрософт</span><span class="sxs-lookup"><span data-stu-id="c2c52-160">**Note:** Starting with Windows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack</span></span>

<span data-ttu-id="c2c52-161">Также...</span><span class="sxs-lookup"><span data-stu-id="c2c52-161">Also…</span></span>

-   <span data-ttu-id="c2c52-162">**Лицензия для MDOP:** Эта технология является частью пакета оптимизации рабочего стола Майкрософт (MDOP).</span><span class="sxs-lookup"><span data-stu-id="c2c52-162">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="c2c52-163">Корпоративные пользователи могут получить MDOP с помощью программы Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="c2c52-163">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="c2c52-164">Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в статьях получение MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="c2c52-164">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="c2c52-165">**Учетные данные администратора** для компьютера, на котором вы хотите установить</span><span class="sxs-lookup"><span data-stu-id="c2c52-165">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

## <a href="" id="step2"></a><span data-ttu-id="c2c52-166">Шаг 2: развертывание места хранения параметров для UE-V 2</span><span class="sxs-lookup"><span data-stu-id="c2c52-166">Step 2: Deploy the Settings Storage Location for UE-V 2</span></span>


<span data-ttu-id="c2c52-167">Вам потребуется развернуть расположение хранилища параметров, стандартную сетевую папку, в которой хранятся параметры пользователя в файле пакета параметров.</span><span class="sxs-lookup"><span data-stu-id="c2c52-167">You’ll need to deploy a settings storage location, a standard network share where user settings are stored in a settings package file.</span></span> <span data-ttu-id="c2c52-168">При создании общего доступа к хранилищу параметров Ограничьте доступ для пользователей, которым он необходим.</span><span class="sxs-lookup"><span data-stu-id="c2c52-168">When you create the settings storage share, you should limit access to users that require it.</span></span> <span data-ttu-id="c2c52-169">[Развертывание расположения хранилища параметров](https://technet.microsoft.com/library/dn458891.aspx#ssl) содержит более подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="c2c52-169">[Deploy a Settings Storage Location](https://technet.microsoft.com/library/dn458891.aspx#ssl) provides more detailed information.</span></span>

**<span data-ttu-id="c2c52-170">Создание сетевого общего доступа</span><span class="sxs-lookup"><span data-stu-id="c2c52-170">Create a network share</span></span>**

1.  <span data-ttu-id="c2c52-171">Создайте новую группу безопасности и добавьте в нее пользователей UE-V.</span><span class="sxs-lookup"><span data-stu-id="c2c52-171">Create a new security group and add UE-V users to it.</span></span>

2.  <span data-ttu-id="c2c52-172">Создайте новую папку на центральном компьютере, где хранятся пакеты параметров UE-V, а затем предоставьте пользователям UE-V доступ к папке с разрешениями группы.</span><span class="sxs-lookup"><span data-stu-id="c2c52-172">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="c2c52-173">Администратору, который поддерживает UE-V, должны быть предоставлены разрешения на доступ к этой общей папке.</span><span class="sxs-lookup"><span data-stu-id="c2c52-173">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="c2c52-174">Назначение пользователям UE-V разрешения на создание каталога при подключении.</span><span class="sxs-lookup"><span data-stu-id="c2c52-174">Assign UE-V users permission to create a directory when they connect.</span></span> <span data-ttu-id="c2c52-175">Предоставьте разрешение на полный доступ ко всем подкаталогам в этом каталоге, но заблокируйте для него все указанные выше данные.</span><span class="sxs-lookup"><span data-stu-id="c2c52-175">Grant full permission to all subdirectories of that directory, but block access to anything above.</span></span>

    1.  <span data-ttu-id="c2c52-176">Установите следующие разрешения на доступ к блоку сообщений сервера уровня ресурсов (SMB) для папки "Параметры хранилища".</span><span class="sxs-lookup"><span data-stu-id="c2c52-176">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="c2c52-177">Учетная запись пользователя</span><span class="sxs-lookup"><span data-stu-id="c2c52-177">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="c2c52-178">Рекомендуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="c2c52-178">Recommended permissions</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="c2c52-179">Все пользователи</span><span class="sxs-lookup"><span data-stu-id="c2c52-179">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="c2c52-180">Нет разрешений</span><span class="sxs-lookup"><span data-stu-id="c2c52-180">No permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="c2c52-181">Группа безопасности пользователей UE-V</span><span class="sxs-lookup"><span data-stu-id="c2c52-181">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="c2c52-182">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="c2c52-182">Full control</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

    2.  <span data-ttu-id="c2c52-183">Установите следующие разрешения файловой системы NTFS для папки "место хранения параметров".</span><span class="sxs-lookup"><span data-stu-id="c2c52-183">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="c2c52-184">Учетная запись пользователя</span><span class="sxs-lookup"><span data-stu-id="c2c52-184">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="c2c52-185">Рекомендуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="c2c52-185">Recommended permissions</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="c2c52-186">Папка</span><span class="sxs-lookup"><span data-stu-id="c2c52-186">Folder</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="c2c52-187">Создатель/владелец</span><span class="sxs-lookup"><span data-stu-id="c2c52-187">Creator/owner</span></span></p></td>
        <td align="left"><p><span data-ttu-id="c2c52-188">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="c2c52-188">Full control</span></span></p></td>
        <td align="left"><p><span data-ttu-id="c2c52-189">Только для вложенных папок и файлов</span><span class="sxs-lookup"><span data-stu-id="c2c52-189">Subfolders and files only</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="c2c52-190">Группа безопасности пользователей UE-V</span><span class="sxs-lookup"><span data-stu-id="c2c52-190">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="c2c52-191">Просмотр папки/Чтение данных, создание папок и добавление данных</span><span class="sxs-lookup"><span data-stu-id="c2c52-191">List folder/read data, create folders/append data</span></span></p></td>
        <td align="left"><p><span data-ttu-id="c2c52-192">Только для этой папки</span><span class="sxs-lookup"><span data-stu-id="c2c52-192">This folder only</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

**<span data-ttu-id="c2c52-193">Примечание о безопасности.</span><span class="sxs-lookup"><span data-stu-id="c2c52-193">Security Note:</span></span>**

<span data-ttu-id="c2c52-194">Если вы создаете общий доступ к хранилищу параметров на компьютере под управлением операционной системы Windows Server, настройте UE-V, чтобы убедиться в том, что локальная группа администраторов или текущий пользователь является владельцем папки, в которой хранятся пакеты параметров.</span><span class="sxs-lookup"><span data-stu-id="c2c52-194">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="c2c52-195">Чтобы включить эту дополнительную защиту, укажите этот параметр в редакторе реестра Windows Server.</span><span class="sxs-lookup"><span data-stu-id="c2c52-195">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="c2c52-196">Добавьте раздел реестра **reg \ _DWORD** с именем **"RepositoryOwnerCheckEnabled"** в раздел **hKey \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.</span><span class="sxs-lookup"><span data-stu-id="c2c52-196">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="c2c52-197">Установите для раздела реестра значение *1*.</span><span class="sxs-lookup"><span data-stu-id="c2c52-197">Set the registry key value to *1*.</span></span>

## <a href="" id="step3"></a><span data-ttu-id="c2c52-198">Шаг 3: развертывание агента UE-V 2</span><span class="sxs-lookup"><span data-stu-id="c2c52-198">Step 3: Deploy the UE-V 2 Agent</span></span>


<span data-ttu-id="c2c52-199">Агент UE-V синхронизирует параметры приложения и Windows между компьютерами и устройствами пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2c52-199">The UE-V Agent synchronizes application and Windows settings between users’ computers and devices.</span></span> <span data-ttu-id="c2c52-200">В целях оценки установите агент по крайней мере на двух компьютерах в тестовой среде, которые принадлежат тому же пользователю.</span><span class="sxs-lookup"><span data-stu-id="c2c52-200">For evaluation purposes, install the agent on at least two computers in your test environment that belong to the same user.</span></span>

<span data-ttu-id="c2c52-201">Запустите файл AgentSetup.exe из командной строки, чтобы установить агент UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c2c52-201">Run the AgentSetup.exe file from the command line to install the UE-V Agent.</span></span> <span data-ttu-id="c2c52-202">Установка производится как в 32, так и в 64-разрядной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="c2c52-202">It installs on both 32-bit and 64-bit operating systems.</span></span>

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

<span data-ttu-id="c2c52-203">Параметр командной строки SettingsStoragePath должен быть указан в качестве сетевого общего доступа на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="c2c52-203">You must specify the SettingsStoragePath command line parameter as the network share from Step 2.</span></span> <span data-ttu-id="c2c52-204">[Развертывание агента UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) содержит более подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="c2c52-204">[Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more detailed information.</span></span>

## <a href="" id="step4"></a><span data-ttu-id="c2c52-205">Шаг 4: Проверка развертывания для оценки UE-V 2</span><span class="sxs-lookup"><span data-stu-id="c2c52-205">Step 4: Test Your UE-V 2 Evaluation Deployment</span></span>


<span data-ttu-id="c2c52-206">Теперь вы можете выполнить несколько тестов для пробной версии UE-V и узнать, как работает UE-V.</span><span class="sxs-lookup"><span data-stu-id="c2c52-206">You can now run a few tests on your UE-V evaluation deployment to see how UE-V works.</span></span>

****

1.  <span data-ttu-id="c2c52-207">На первом компьютере (на компьютере A) сделайте одно или несколько из указанных ниже изменений.</span><span class="sxs-lookup"><span data-stu-id="c2c52-207">On the first computer (Computer A), make one or more of these changes:</span></span>

    1.  <span data-ttu-id="c2c52-208">Открыть на рабочем столе Windows и переместить панель задач в другое место в окне.</span><span class="sxs-lookup"><span data-stu-id="c2c52-208">Open to Windows Desktop and move the taskbar to a different location in the window.</span></span>

    2.  <span data-ttu-id="c2c52-209">Измените шрифты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c2c52-209">Change the default fonts.</span></span>

    3.  <span data-ttu-id="c2c52-210">Откройте Калькулятор и установите для него значение **экспоненциальный**.</span><span class="sxs-lookup"><span data-stu-id="c2c52-210">Open Calculator and set to **scientific**.</span></span>

    4.  <span data-ttu-id="c2c52-211">Измените поведение любого приложения для Windows, как описано в разделе [Управление шаблонами расположений параметров ue-V 2. x с помощью Windows PowerShell и WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="c2c52-211">Change the behavior of any Windows app, as detailed in [Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    5.  <span data-ttu-id="c2c52-212">Отключите синхронизацию с параметрами учетной записи Майкрософт и перемещаемые профили.</span><span class="sxs-lookup"><span data-stu-id="c2c52-212">Disable Microsoft Account settings synchronization and Roaming Profiles.</span></span>

2.  <span data-ttu-id="c2c52-213">Выход из системы. параметры сохраняются в пакете параметров UE-V, когда пользователь блокирует, выходит из него, выключает приложение или при запуске поставщика синхронизации (каждые 30 минут по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="c2c52-213">Log off Computer A. Settings are saved in a UE-V settings package when users lock, logoff, exit an application, or when the sync provider runs (every 30 minutes by default).</span></span>

3.  <span data-ttu-id="c2c52-214">Войдите на второй компьютер (на компьютере B) в качестве того же пользователя, что и у компьютера A.</span><span class="sxs-lookup"><span data-stu-id="c2c52-214">Log in to the second computer (Computer B) as the same user as Computer A.</span></span>

4.  <span data-ttu-id="c2c52-215">Откройте на рабочем столе Windows и убедитесь, что расположение панели задач соответствует положению компьютера а. Убедитесь, что шрифты по умолчанию совпадают и для калькулятора задано значение " **экспоненциальный**".</span><span class="sxs-lookup"><span data-stu-id="c2c52-215">Open to Windows Desktop and verify that the taskbar location matches that of Computer A. Verify that the default fonts match and that Calculator is set to **scientific**.</span></span> <span data-ttu-id="c2c52-216">Также проверьте, какие изменения были внесены в любое приложение для Windows.</span><span class="sxs-lookup"><span data-stu-id="c2c52-216">Also verify the change you made to any Windows app.</span></span>

<span data-ttu-id="c2c52-217">Вы можете вернуться к исходным параметрам на компьютере B, применив параметры.</span><span class="sxs-lookup"><span data-stu-id="c2c52-217">You can change the settings in Computer B back to the original Computer A settings.</span></span> <span data-ttu-id="c2c52-218">Затем выйдите из системы на компьютере B и войдите в систему на компьютере A, чтобы проверить изменения.</span><span class="sxs-lookup"><span data-stu-id="c2c52-218">Then log off Computer B and log in to Computer A to verify the changes.</span></span>

## <span data-ttu-id="c2c52-219">Другие ресурсы для этого продукта</span><span class="sxs-lookup"><span data-stu-id="c2c52-219">Other resources for this product</span></span>


-   [<span data-ttu-id="c2c52-220">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="c2c52-220">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="c2c52-221">Подготовка к развертыванию UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c2c52-221">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="c2c52-222">Администрирование UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c2c52-222">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="c2c52-223">Устранение неполадок UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c2c52-223">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="c2c52-224">Технический справочник по UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="c2c52-224">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





