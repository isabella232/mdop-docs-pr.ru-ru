---
title: Создание образа Windows Virtual PC для MED-V
description: Создание образа Windows Virtual PC для MED-V
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812685"
---
# <span data-ttu-id="c0c75-103">Создание образа Windows Virtual PC для MED-V</span><span class="sxs-lookup"><span data-stu-id="c0c75-103">Creating a Windows Virtual PC Image for MED-V</span></span>


<span data-ttu-id="c0c75-104">Прежде чем вы сможете использовать рабочую область MED-V для пользователей, необходимо сначала подготовить виртуальный жесткий диск, который вы используете для создания пакета установщика рабочей области MED-V для Microsoft Enterprise Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="c0c75-104">Before you can deliver a MED-V workspace to users, you have to first prepare a virtual hard disk that you use to build the MED-V workspace installer package for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span> <span data-ttu-id="c0c75-105">Для подготовки необходимого виртуального жесткого диска необходимо создать образ виртуальных компьютеров Windows, содержащий необходимую операционную систему, обновления и программное обеспечение, которое позволит позже развертывать приложения и сведения о перенаправлении URL-адреса для пользователей.</span><span class="sxs-lookup"><span data-stu-id="c0c75-105">To prepare the necessary virtual hard disk, you must create a Windows Virtual PC image that contains the required operating system, updates, and software to let you later deploy applications and URL redirection information to users.</span></span> <span data-ttu-id="c0c75-106">В этом разделе приведены рекомендации о том, как создавать виртуальные жесткие диски.</span><span class="sxs-lookup"><span data-stu-id="c0c75-106">This section provides guidance about how to create the virtual hard disk.</span></span>

<span data-ttu-id="c0c75-107">Чтобы создать виртуальный образ для MED-V, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c0c75-107">To create a virtual image for MED-V, you must follow these steps.</span></span>

1.  [<span data-ttu-id="c0c75-108">Создание образа виртуального компьютера с Windows</span><span class="sxs-lookup"><span data-stu-id="c0c75-108">Create a Windows Virtual PC image</span></span>](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [<span data-ttu-id="c0c75-109">Установка Windows XP на образ</span><span class="sxs-lookup"><span data-stu-id="c0c75-109">Install Windows XP on the image</span></span>](#bkmk-installingwindowsxpontovpc)

3.  [<span data-ttu-id="c0c75-110">Установка .NET Framework на образ</span><span class="sxs-lookup"><span data-stu-id="c0c75-110">Install the .NET Framework on the image</span></span>](#bkmk-installingnet)

4.  [<span data-ttu-id="c0c75-111">Применение обновлений к изображению</span><span class="sxs-lookup"><span data-stu-id="c0c75-111">Apply updates to the image</span></span>](#bkmk-applypatchestovpc)

5.  [<span data-ttu-id="c0c75-112">Установка компонентов интеграции</span><span class="sxs-lookup"><span data-stu-id="c0c75-112">Install Integration Components</span></span>](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="c0c75-113">Создание образа виртуального компьютера с Windows</span><span class="sxs-lookup"><span data-stu-id="c0c75-113">Creating a Windows Virtual PC Image</span></span>


<span data-ttu-id="c0c75-114">Чтобы создать образ Virtual PC для Windows, ознакомьтесь с документацией по виртуальным ПК Windows.</span><span class="sxs-lookup"><span data-stu-id="c0c75-114">To create a Windows Virtual PC image, see the Windows Virtual PC documentation:</span></span>

-   <span data-ttu-id="c0c75-115">[Домашняя страница Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .</span><span class="sxs-lookup"><span data-stu-id="c0c75-115">[Windows Virtual PC Home Page](https://go.microsoft.com/fwlink/?LinkId=148103) (https://go.microsoft.com/fwlink/?LinkId=148103).</span></span>

-   <span data-ttu-id="c0c75-116">[Справка по Virtual PC для Windows](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="c0c75-116">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="c0c75-117">Кроме того, если у вас уже есть файл образов Windows (WIM), который вы хотите использовать в качестве основы для виртуального образа, вы можете преобразовать его в VHD, который вы используете для создания рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="c0c75-117">Alternately, if you already have a Windows Imaging (WIM) file that you want to use as the basis for your virtual image, you can convert it to a VHD that you use to build the MED-V workspace.</span></span> <span data-ttu-id="c0c75-118">Дополнительные сведения о преобразовании WIM-данных на виртуальный жесткий диск можно найти в разделе [Поддержка встроенного виртуального жесткого диска в Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) ( https://go.microsoft.com/fwlink/?LinkId=195922) .</span><span class="sxs-lookup"><span data-stu-id="c0c75-118">For more information about how to convert a WIM to a virtual hard disk, see [Native VHD Support in Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) (https://go.microsoft.com/fwlink/?LinkId=195922).</span></span>

<span data-ttu-id="c0c75-119">**Важно!**  MED-V поддерживает только один виртуальный жесткий диск для каждой виртуальной машины и только один раздел на каждом виртуальном диске.</span><span class="sxs-lookup"><span data-stu-id="c0c75-119">**Important** MED-V only supports one virtual hard disk per virtual machine and only one partition on each virtual disk.</span></span>

 

<span data-ttu-id="c0c75-120">После создания виртуального жесткого диска установите Windows XP на образ.</span><span class="sxs-lookup"><span data-stu-id="c0c75-120">After you have created your virtual hard disk, install Windows XP on the image.</span></span>

## <a href="" id="bkmk-installingwindowsxpontovpc"></a><span data-ttu-id="c0c75-121">Установка Windows XP в образе виртуального компьютера с Windows</span><span class="sxs-lookup"><span data-stu-id="c0c75-121">Installing Windows XP on a Windows Virtual PC Image</span></span>


<span data-ttu-id="c0c75-122">Для работы MED-V требуется установка Windows XP с пакетом обновления 3 (SP3) на компьютере с Windows Virtual PC, прежде чем создавать рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="c0c75-122">MED-V requires that Windows XP SP3 is installed on the Windows Virtual PC image before you build the MED-V workspace.</span></span>

<span data-ttu-id="c0c75-123">Дополнительные сведения о том, как установить Windows XP, можно найти [в разделе Создание виртуальной машины и установка гостевой операционной системы](https://go.microsoft.com/fwlink/?LinkId=182379) ( https://go.microsoft.com/fwlink/?LinkId=182379) .</span><span class="sxs-lookup"><span data-stu-id="c0c75-123">For more information about how to install Windows XP, see [Create a virtual machine and install a guest operating system](https://go.microsoft.com/fwlink/?LinkId=182379) (https://go.microsoft.com/fwlink/?LinkId=182379).</span></span>

## <a href="" id="bkmk-installingnet"></a><span data-ttu-id="c0c75-124">Установка .NET Framework 3,5 с пакетом обновления 1 (SP1) на виртуальный компьютер с Windows</span><span class="sxs-lookup"><span data-stu-id="c0c75-124">Installing the .NET Framework 3.5 SP1 on a Windows Virtual PC Image</span></span>


<span data-ttu-id="c0c75-125">Необходимо вручную установить .NET Framework 3,5 SP1 и Update KB959209 в образ Windows Virtual PC, подготовленный для использования с MED-V.</span><span class="sxs-lookup"><span data-stu-id="c0c75-125">You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="c0c75-126">Обновление [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) устраняет несколько известных проблем с совместимостью приложений.</span><span class="sxs-lookup"><span data-stu-id="c0c75-126">The update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950) addresses several known application compatibility issues.</span></span>

## <a href="" id="bkmk-applypatchestovpc"></a><span data-ttu-id="c0c75-127">Применение обновлений к образу Virtual PC для Windows</span><span class="sxs-lookup"><span data-stu-id="c0c75-127">Applying Updates to the Windows Virtual PC Image</span></span>


<span data-ttu-id="c0c75-128">После установки Windows XP на виртуальной машине установите необходимые на нем обновления для Windows XP, например пакет обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="c0c75-128">After you have installed Windows XP on your virtual machine, install any required Windows XP updates on the image, such as SP3.</span></span> <span data-ttu-id="c0c75-129">Вы также можете установить определенные дополнительные обновления для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="c0c75-129">You can also install certain optional updates for better performance.</span></span>

<span data-ttu-id="c0c75-130">**Важно!**  Для работы MED-V требуется, чтобы в операционной системе на виртуальной машине выполнялось Windows XP SP3.</span><span class="sxs-lookup"><span data-stu-id="c0c75-130">**Important** MED-V requires that Windows XP SP3 be running on the guest operating system.</span></span>

 

<span data-ttu-id="c0c75-131">**Предупреждение**  При установке обновлений для Windows XP убедитесь в том, что в гостевой системе, которую вы планируете использовать в рабочей области MED-V, вы не сохранили версию Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c0c75-131">**Warning** When you install updates to Windows XP, make sure that you remain on the version of Internet Explorer in the guest that you intend to use in the MED-V workspace.</span></span> <span data-ttu-id="c0c75-132">Например, если вы хотите запустить Internet Explorer 6 в рабочей области MED-V, убедитесь в том, что все устанавливаемые вами обновления не включают браузер Internet Explorer 7 или Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="c0c75-132">For example, if you intend to run Internet Explorer 6 in the MED-V workspace, make sure that any updates that you install now do not include Internet Explorer 7 or Internet Explorer 8.</span></span> <span data-ttu-id="c0c75-133">Кроме того, рекомендуется настроить реестр, чтобы запретить автоматическое обновление Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c0c75-133">In addition, we recommend that you configure the registry to prevent automatic updates from upgrading Internet Explorer.</span></span>

 

### <span data-ttu-id="c0c75-134">Установка дополнительного обновления производительности</span><span class="sxs-lookup"><span data-stu-id="c0c75-134">Installing an Optional Performance Update</span></span>

<span data-ttu-id="c0c75-135">Хотя это необязательно, мы рекомендуем установить следующее обновление для [исправления KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ( https://go.microsoft.com/fwlink/?LinkId=201077) .</span><span class="sxs-lookup"><span data-stu-id="c0c75-135">Although it is optional, we recommend that you install the following update for [hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) (https://go.microsoft.com/fwlink/?LinkId=201077).</span></span> <span data-ttu-id="c0c75-136">Это обновление повышает производительность общих папок в сеансе служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="c0c75-136">This update increases the performance of shared folders in a Terminal Services session:</span></span>

<span data-ttu-id="c0c75-137">**Примечание**  Обновление доступно для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c0c75-137">**Note** The update is publicly available.</span></span> <span data-ttu-id="c0c75-138">Тем не менее, вам может быть предложено принимать условия соглашения для служб Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c0c75-138">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="c0c75-139">Следуйте указаниям на последовательных страницах, чтобы получить это исправление.</span><span class="sxs-lookup"><span data-stu-id="c0c75-139">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>

 

### <span data-ttu-id="c0c75-140">Настройка обновления производительности групповой политики</span><span class="sxs-lookup"><span data-stu-id="c0c75-140">Configuring a Group Policy Performance Update</span></span>

<span data-ttu-id="c0c75-141">По умолчанию групповая политика загружается на компьютер по одному байту за раз.</span><span class="sxs-lookup"><span data-stu-id="c0c75-141">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="c0c75-142">Это приводит к задержке, а MED-V присоединяется к домену.</span><span class="sxs-lookup"><span data-stu-id="c0c75-142">This causes delays while MED-V is being joined to the domain.</span></span> <span data-ttu-id="c0c75-143">Для повышения производительности групповой политики установите для реестра следующий параметр реестра:</span><span class="sxs-lookup"><span data-stu-id="c0c75-143">To increase the performance of Group Policy, set the following registry key value to the registry:</span></span>

<span data-ttu-id="c0c75-144">Подраздел реестра: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="c0c75-144">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="c0c75-145">Entry (запись): BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="c0c75-145">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="c0c75-146">Type (тип): DWORD</span><span class="sxs-lookup"><span data-stu-id="c0c75-146">Type: DWORD</span></span>

<span data-ttu-id="c0c75-147">Значение: 1</span><span class="sxs-lookup"><span data-stu-id="c0c75-147">Value: 1</span></span>

## <a href="" id="bkmk-installintegration"></a><span data-ttu-id="c0c75-148">Установка интеграционных компонентов</span><span class="sxs-lookup"><span data-stu-id="c0c75-148">Installing Integration Components</span></span>


<span data-ttu-id="c0c75-149">В Windows Virtual PC есть пакет интеграционных компонентов.</span><span class="sxs-lookup"><span data-stu-id="c0c75-149">Windows Virtual PC includes the Integration Components package.</span></span> <span data-ttu-id="c0c75-150">Это предоставляет функции, повышающие взаимодействие между виртуальной средой и физическим компьютером.</span><span class="sxs-lookup"><span data-stu-id="c0c75-150">This provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="c0c75-151">Например, пакет компонентов интеграции позволяет перемещать указатель мыши между узлом и гостевым компьютером.</span><span class="sxs-lookup"><span data-stu-id="c0c75-151">For example, the Integration Components package lets your mouse move between the host and the guest computers.</span></span>

<span data-ttu-id="c0c75-152">**Важно!**  Для работы MED-V требуется установка пакета компонентов интеграции.</span><span class="sxs-lookup"><span data-stu-id="c0c75-152">**Important** MED-V requires the installation of the Integration Components package.</span></span>

 

<span data-ttu-id="c0c75-153">При настройке виртуального образа для работы с MED-V для обеспечения доступности функций интеграции необходимо вручную установить пакет компонентов интеграции в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="c0c75-153">When you configure the virtual image to work with MED-V, you must manually install the Integration Components package on the guest operating system to make the integration features that are available.</span></span>

<span data-ttu-id="c0c75-154">Дополнительные сведения о том, как установить и использовать пакет интеграционных компонентов, можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="c0c75-154">For more information about how to install and use the Integration Components package, see the following:</span></span>

-   <span data-ttu-id="c0c75-155">[Установка или обновление пакета компонентов интеграции](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .</span><span class="sxs-lookup"><span data-stu-id="c0c75-155">[Install or Upgrade the Integration Components Package](https://go.microsoft.com/fwlink/?LinkId=195923) (https://go.microsoft.com/fwlink/?LinkId=195923).</span></span>

-   <span data-ttu-id="c0c75-156">[Сведения о функциях интеграции](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .</span><span class="sxs-lookup"><span data-stu-id="c0c75-156">[About Integration Features](https://go.microsoft.com/fwlink/?LinkId=195924) (https://go.microsoft.com/fwlink/?LinkId=195924).</span></span>

### <span data-ttu-id="c0c75-157">Установка обновления для удаленного приложения RemoteApp</span><span class="sxs-lookup"><span data-stu-id="c0c75-157">Installing RemoteApp Update</span></span>

<span data-ttu-id="c0c75-158">После установки пакета интеграционных компонентов вам будет предложено установить следующее обновление: Обновление для Windows XP с пакетом обновления 3 (SP3) для включения RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c0c75-158">After you install the Integration Components package, you are prompted to install the following update: "Update for Windows XP SP3 to enable RemoteApp."</span></span> <span data-ttu-id="c0c75-159">Это обязательный компонент для MED-V.</span><span class="sxs-lookup"><span data-stu-id="c0c75-159">This is a required component for MED-V.</span></span>

<span data-ttu-id="c0c75-160">**Важно!**  Если вам не будет предложено установить обновление для удаленного приложения RemoteApp, необходимо загрузить и установить его вручную.</span><span class="sxs-lookup"><span data-stu-id="c0c75-160">**Important** If you are not prompted to install the RemoteApp update, you must download and install it manually.</span></span> <span data-ttu-id="c0c75-161">Дополнительные сведения и инструкции по загрузке этого обновления можно найти в статьях [Обновление для Windows XP с пакетом обновления 3 (SP3), чтобы включить RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) ( https://go.microsoft.com/fwlink/?LinkId=195925) .</span><span class="sxs-lookup"><span data-stu-id="c0c75-161">For more information and instructions about how to download this update, see [Update for Windows XP SP3 to enable RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) (https://go.microsoft.com/fwlink/?LinkId=195925).</span></span>

 

### <span data-ttu-id="c0c75-162">Включение удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="c0c75-162">Enabling Remote Desktop</span></span>

<span data-ttu-id="c0c75-163">По умолчанию удаленный рабочий стол включен после установки пакета интеграционных компонентов.</span><span class="sxs-lookup"><span data-stu-id="c0c75-163">By default, Remote Desktop is enabled after you install the Integration Components package.</span></span> <span data-ttu-id="c0c75-164">Для функционирования MED-V убедитесь, что удаленный рабочий стол включен и не распространяет групповую политику, которая отключает ее.</span><span class="sxs-lookup"><span data-stu-id="c0c75-164">For MED-V to be operational, ensure that Remote Desktop is enabled, and do not distribute any Group Policy that disables it.</span></span>

<span data-ttu-id="c0c75-165">Сведения о том, как включить удаленный доступ к рабочему столу, можно найти в разделе [Включение и отключение удаленного рабочего стола](https://go.microsoft.com/fwlink/?LinkId=201162) ( https://go.microsoft.com/fwlink/?LinkId=201162) .</span><span class="sxs-lookup"><span data-stu-id="c0c75-165">For information about how to enable Remote Desktop, see [Enable or disable Remote Desktop](https://go.microsoft.com/fwlink/?LinkId=201162) (https://go.microsoft.com/fwlink/?LinkId=201162).</span></span>

## <span data-ttu-id="c0c75-166">Настройка Internet Explorer с помощью пакета администрирования Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c0c75-166">Customizing Internet Explorer by Using the Internet Explorer Administration Kit</span></span>


<span data-ttu-id="c0c75-167">При желании вы можете настроить Internet Explorer в операционной системе на виртуальной машине с помощью пакета администрирования Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c0c75-167">If you want, you can use the Internet Explorer Administration Kit to customize Internet Explorer on the guest operating system.</span></span> <span data-ttu-id="c0c75-168">Дополнительные сведения можно найти в [пакете администрирования Internet Explorer 6 и руководстве по развертыванию](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.Microsoft.com/fwlink/?LinkId=200007).</span><span class="sxs-lookup"><span data-stu-id="c0c75-168">For more information, see the [Internet Explorer 6 Administration Kit and Deployment Guide](https://go.microsoft.com/fwlink/?LinkId=200007) (http:// go.microsoft.com/fwlink/?LinkId=200007).</span></span>

<span data-ttu-id="c0c75-169">**Предупреждение**  Следует предусмотреть вопросы безопасности, связанные с настройкой Internet Explorer в рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="c0c75-169">**Warning** You should consider security concerns associated with customizing Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="c0c75-170">Дополнительные сведения можно найти в разделе Советы и [рекомендации по обеспечению безопасности при работе с MED-V](security-best-practices-for-med-v-operations.md).</span><span class="sxs-lookup"><span data-stu-id="c0c75-170">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>

 

<span data-ttu-id="c0c75-171">После установки виртуального жесткого диска с помощью последней версии гостевой операционной системы вы можете установить на нем приложения.</span><span class="sxs-lookup"><span data-stu-id="c0c75-171">After your virtual hard disk is installed with an up-to-date guest operating system, you can install applications on the image.</span></span>

## <span data-ttu-id="c0c75-172">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c0c75-172">Related topics</span></span>


[<span data-ttu-id="c0c75-173">Установка приложений в образе Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c0c75-173">Installing Applications on a Windows Virtual PC Image</span></span>](installing-applications-on-a-windows-virtual-pc-image.md)

[<span data-ttu-id="c0c75-174">Настройка образа Windows Virtual PC для MED-V</span><span class="sxs-lookup"><span data-stu-id="c0c75-174">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 





