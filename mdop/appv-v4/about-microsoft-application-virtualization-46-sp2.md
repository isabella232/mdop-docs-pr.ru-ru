---
title: Сведения о системе Microsoft Application Virtualization 4.6 с пакетом обновления 2 (SP2)
description: Сведения о системе Microsoft Application Virtualization 4.6 с пакетом обновления 2 (SP2)
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820019"
---
# <span data-ttu-id="001d1-103">Сведения о системе Microsoft Application Virtualization 4.6 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="001d1-103">About Microsoft Application Virtualization 4.6 SP2</span></span>


<span data-ttu-id="001d1-104">Microsoft Application Virtualization (App-V) 4.6 SP2 предлагает несколько улучшений и новых функций, описанных в этой статье.</span><span class="sxs-lookup"><span data-stu-id="001d1-104">Microsoft Application Virtualization (App-V)4.6 SP2 provides several enhancements and new features, which are described in this topic.</span></span>

<span data-ttu-id="001d1-105">**Внимание!**  В этой статье описано, как изменить реестр Windows с помощью редактора реестра.</span><span class="sxs-lookup"><span data-stu-id="001d1-105">**Caution** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="001d1-106">Если изменить реестр Windows некорректно, это может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows.</span><span class="sxs-lookup"><span data-stu-id="001d1-106">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="001d1-107">Перед изменением реестра необходимо создать резервную копию файлов реестра (System. dat и User. dat).</span><span class="sxs-lookup"><span data-stu-id="001d1-107">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="001d1-108">Корпорация Майкрософт не несет ответственности за то, что проблемы, которые могут возникнуть при изменении реестра, могут быть устранены.</span><span class="sxs-lookup"><span data-stu-id="001d1-108">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="001d1-109">Изменение реестра на свой страх и риск.</span><span class="sxs-lookup"><span data-stu-id="001d1-109">Change the registry at your own risk.</span></span>

 

**<span data-ttu-id="001d1-110">Поддержка Windows 8 и Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="001d1-110">Support for Windows 8 and Windows Server 2012</span></span>**

<span data-ttu-id="001d1-111">App-V 4.6 SP2 добавляет поддержку служб удаленных рабочих столов для Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="001d1-111">App-V4.6SP2 adds support for Windows 8 and Windows Server 2012 Remote Desktop Services.</span></span>

**<span data-ttu-id="001d1-112">Поддержка сосуществования с помощью клиента App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="001d1-112">Support for coexistence with App-V 5.0 client</span></span>**

<span data-ttu-id="001d1-113">Приложение App-V 4.6 SP2 обеспечивает поддержку сосуществования с помощью клиента Microsoft Application Virtualization 5,0.</span><span class="sxs-lookup"><span data-stu-id="001d1-113">App-V4.6SP2 provides support for coexistence with the Microsoft Application Virtualization 5.0 client.</span></span> <span data-ttu-id="001d1-114">Ознакомьтесь с документацией по App-V 5,0, чтобы узнать о том, как настроить клиент App-V 5,0 для сосуществования с помощью клиента App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="001d1-114">Review the App-V 5.0 documentation for instructions on how to configure the App-V 5.0 client for coexistence with the App-V4.6SP2 client.</span></span> <span data-ttu-id="001d1-115">Дополнительные сведения о App-V 5,0 можно найти в разделе [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) в TechNet.</span><span class="sxs-lookup"><span data-stu-id="001d1-115">For more information about App-V 5.0, see [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) on TechNet.</span></span>

**<span data-ttu-id="001d1-116">Возможность виртуализации Adobe Reader X с использованием защищенного режима</span><span class="sxs-lookup"><span data-stu-id="001d1-116">Ability to virtualize Adobe Reader X with Protected Mode</span></span>**

<span data-ttu-id="001d1-117">Вы можете виртуализировать приложение Adobe Reader X с включенным параметром защищенного режима, выполнив описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="001d1-117">You can virtualize Adobe Reader X with its Protected Mode feature turned on by using the following procedures.</span></span> <span data-ttu-id="001d1-118">Прежде чем приходилось отключить защищенный режим, чтобы виртуализировать приложение Adobe Reader X.</span><span class="sxs-lookup"><span data-stu-id="001d1-118">Previously you had to disable Protected Mode in order to virtualize Adobe Reader X.</span></span>

<span data-ttu-id="001d1-119">Перед запуском программы Sequencer App-V создайте следующий параметр реестра в разделе HKEY \ _LOCAL \ _MACHINE \\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span><span class="sxs-lookup"><span data-stu-id="001d1-119">Before launching the App-V Sequencer, create the following registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="001d1-120">Имя</span><span class="sxs-lookup"><span data-stu-id="001d1-120">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="001d1-121">Тип</span><span class="sxs-lookup"><span data-stu-id="001d1-121">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="001d1-122">Данные</span><span class="sxs-lookup"><span data-stu-id="001d1-122">Data</span></span></p></td>
<td align="left"><p><span data-ttu-id="001d1-123">Описание</span><span class="sxs-lookup"><span data-stu-id="001d1-123">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="001d1-124">EnableVFSPassthrough</span><span class="sxs-lookup"><span data-stu-id="001d1-124">EnableVFSPassthrough</span></span></p></td>
<td align="left"><p><span data-ttu-id="001d1-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="001d1-125">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="001d1-126">1,1</span><span class="sxs-lookup"><span data-stu-id="001d1-126">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="001d1-127">Установите для этого параметра значение <strong> 1, </strong> чтобы запустить Adobe Reader X в защищенном режиме на этапе запуска.</span><span class="sxs-lookup"><span data-stu-id="001d1-127">Set this value to <strong>1</strong> in order to start Adobe Reader X in Protected Mode during the launch phase.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="001d1-128">**Примечание**  На компьютере под управлением 64-разрядной операционной системы Создайте значение реестра в разделе HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.</span><span class="sxs-lookup"><span data-stu-id="001d1-128">**Note** On a computer running a 64-bit operating system, create the registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.</span></span>

 

<span data-ttu-id="001d1-129">Для каждого OSD-файла в пакете Adobe Reader X добавьте в &lt; элемент POLICIES следующие элементы &gt; :</span><span class="sxs-lookup"><span data-stu-id="001d1-129">For each OSD-file in your Adobe Reader X package, add the following items under the &lt;POLICIES&gt; element:</span></span>

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**<span data-ttu-id="001d1-130">Новый параметр командной строки Sequencer</span><span class="sxs-lookup"><span data-stu-id="001d1-130">New Sequencer command-line parameter</span></span>**

<span data-ttu-id="001d1-131">Когда вы создаете ускоритель пакетов (PA) через графический интерфейс секвенсора, вы можете выбрать файл RTF или TXT, который содержит инструкции по упаковке и развертыванию для администраторов, которые будут применять ускоритель пакетов.</span><span class="sxs-lookup"><span data-stu-id="001d1-131">When you create a Package Accelerator (PA) through the Sequencer GUI, you can select an RTF or TXT file that provides packaging and deployment guidance to the administrators who will apply the Package Accelerator.</span></span> <span data-ttu-id="001d1-132">Теперь эта функция доступна с помощью CLI Sequencer.</span><span class="sxs-lookup"><span data-stu-id="001d1-132">This functionality is now available using the Sequencer CLI.</span></span>

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

<span data-ttu-id="001d1-133">Укажите путь к файлу RTF или TXT, который содержит инструкции по упаковке и развертыванию при создании ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="001d1-133">Specify a path to an RTF or TXT file that provides packaging and deployment guidance when creating a Package Accelerator.</span></span>

**<span data-ttu-id="001d1-134">Сообщения об ошибках приложений Microsoft больше не нужно устанавливать</span><span class="sxs-lookup"><span data-stu-id="001d1-134">Microsoft Application Error Reporting no longer needs to be installed</span></span>**

<span data-ttu-id="001d1-135">При установке клиента App-V 4.6 SP2 с помощью setup.msi вам больше не нужно устанавливать отчеты об ошибках приложений Microsoft (dw20shared.msi).</span><span class="sxs-lookup"><span data-stu-id="001d1-135">When you are installing the App-V4.6SP2 client by using setup.msi, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="001d1-136">Приложение App-V 4.6 SP2 теперь использует отчеты об ошибках Microsoft.</span><span class="sxs-lookup"><span data-stu-id="001d1-136">App-V4.6SP2 now uses Microsoft Error Reporting.</span></span> <span data-ttu-id="001d1-137">Дополнительные сведения можно найти [в разделе Установка клиента App-V с помощью Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span><span class="sxs-lookup"><span data-stu-id="001d1-137">For more information, see [How to Install the App-V Client by Using Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span></span>

**<span data-ttu-id="001d1-138">Отзывы и наборы исправлений пользователей</span><span class="sxs-lookup"><span data-stu-id="001d1-138">Customer feedback and hotfix rollup</span></span>**

<span data-ttu-id="001d1-139">Приложение App-V 4.6 SP2 содержит свертку исправлений, устраняющих проблемы, обнаруженные с момента выпуска App-V 4,6 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="001d1-139">App-V4.6SP2 includes a rollup of fixes to address issues found since the App-V 4.6 SP1 release.</span></span> <span data-ttu-id="001d1-140">В состав пакета обновления 2 (SP2) для App-V 4.6 установлены последние исправления до и включая Microsoft Application Virtualization 4,6 с исправлением 6 (SP1).</span><span class="sxs-lookup"><span data-stu-id="001d1-140">App-V4.6SP2 contains the latest fixes up to and including Microsoft Application Virtualization 4.6 SP1 Hotfix 6.</span></span>

## <span data-ttu-id="001d1-141">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="001d1-141">In This Section</span></span>


<a href="" id="app-v-4-6-sp2-release-notes"></a>[<span data-ttu-id="001d1-142">Заметки о выпуске App-V 4.6 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="001d1-142">App-V 4.6 SP2 Release Notes</span></span>](https://go.microsoft.com/fwlink/?LinkId=267600)  
<span data-ttu-id="001d1-143">Предоставляет актуальные сведения об известных проблемах, возникающих при использовании App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="001d1-143">Provides the most up-to-date information about known issues with App-V4.6SP2.</span></span>

 

 





