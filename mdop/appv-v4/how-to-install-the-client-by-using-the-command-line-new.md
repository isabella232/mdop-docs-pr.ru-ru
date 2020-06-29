---
title: Установка клиента с помощью командной строки
description: Установка клиента с помощью командной строки
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817322"
---
# <span data-ttu-id="5b723-103">Установка клиента с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="5b723-103">How to Install the Client by Using the Command Line</span></span>


<span data-ttu-id="5b723-104">В этом разделе приведены процедуры для установки клиентского клиента Application Virtualization (App-V) или клиента App-V для служб удаленных рабочих столов (ранее — служб терминалов) с помощью либо setup.exe, либо setup.msi.</span><span class="sxs-lookup"><span data-stu-id="5b723-104">The topics in this section include procedures to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span> <span data-ttu-id="5b723-105">Для запуска программы установки необходимо иметь права администратора.</span><span class="sxs-lookup"><span data-stu-id="5b723-105">Administrative rights are required to run either setup program.</span></span>

<span data-ttu-id="5b723-106">Вы можете использовать дополнительные параметры командной строки, чтобы применить определенные параметры конфигурации к клиенту App-V во время установки.</span><span class="sxs-lookup"><span data-stu-id="5b723-106">You can use optional command-line parameters to apply specific configuration settings to the App-V client during the installation.</span></span> <span data-ttu-id="5b723-107">Дополнительные сведения об использовании параметров можно найти в разделе [Параметры командной строки установщика клиента Application Virtualization](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5b723-107">For more information about using parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span> <span data-ttu-id="5b723-108">Если вы применили параметры реестра на компьютере перед развертыванием клиента (например, с помощью групповой политики), эти параметры сохраняются, а все дополнительные параметры командной строки применяются.</span><span class="sxs-lookup"><span data-stu-id="5b723-108">If you have applied registry settings to a computer before deploying a client—for example, by using Group Policy—these settings are retained and any additional command line parameters are applied.</span></span> <span data-ttu-id="5b723-109">Значения параметров командной строки будут заменять все существующие значения для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="5b723-109">Command line parameter values will replace any existing value for the same setting.</span></span>

<span data-ttu-id="5b723-110">**Примечание**  При установке клиента App-V на использование кэша, доступного только для чтения (например, с реализацией сервера VDI), необходимо установить для параметра *AUTOLOADTARGET* значение None, чтобы клиент не мог обновить приложения, если кэш доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5b723-110">**Note** When you install the App-V client to use with a read-only cache, for example with a VDI server implementation, you must set the *AUTOLOADTARGET* parameter to NONE to prevent the client from trying to update applications when the cache is read-only.</span></span>

 

<span data-ttu-id="5b723-111">Дополнительные сведения об установке этих значений параметров после установки можно найти в разделе [Настройка параметров реестра клиента App-v с помощью командной строки](https://go.microsoft.com/fwlink/?LinkId=169355) ( https://go.microsoft.com/fwlink/?LinkId=169355) в руководстве по работе с Application Virtualization (App-v).</span><span class="sxs-lookup"><span data-stu-id="5b723-111">For more information about setting these parameter values after installation, see [How to Configure the App-V Client Registry Settings by Using the Command Line](https://go.microsoft.com/fwlink/?LinkId=169355) (https://go.microsoft.com/fwlink/?LinkId=169355) in the Application Virtualization (App-V) Operations Guide.</span></span>

<span data-ttu-id="5b723-112">**Примечание**  Если параметры конфигурации на компьютере пользователя зависят от пути установки клиента, обратите внимание на то, что клиент Application Virtualization (App-V) 4.5 копирует установочные файлы в папку, отличную от предыдущих версий.</span><span class="sxs-lookup"><span data-stu-id="5b723-112">**Note** If a configuration setting on the user’s computer depends on the client installation path, note that the Application Virtualization (App-V)4.5 client copies its installation files to a different folder than previous versions did.</span></span> <span data-ttu-id="5b723-113">По умолчанию новый экземпляр клиента App-V 4.5 копирует установочные файлы в папку клиента Application Virtualization \\Program Files\\Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5b723-113">By default, a new installation of the App-V4.5 client will copy its installation files to the \\Program Files\\Microsoft Application Virtualization Client folder.</span></span> <span data-ttu-id="5b723-114">Если на компьютере уже установлена более ранняя версия клиента, при запуске установщика клиента App-V 4,5 будет выполнено обновление существующего клиента с помощью существующей папки установки.</span><span class="sxs-lookup"><span data-stu-id="5b723-114">If an earlier version of the client is already installed, running the App-V 4.5 client installer will perform an upgrade of the existing client using the existing installation folder.</span></span>

 

<span data-ttu-id="5b723-115">\ [Значение маркера шаблона \]</span><span class="sxs-lookup"><span data-stu-id="5b723-115">\[Template Token Value\]</span></span>

<span data-ttu-id="5b723-116">**Примечание**  Для App-V версии 4.6 и более поздних версий при установке клиента App-V SFTLDR.DLL копируется в каталог Windows\\system32.</span><span class="sxs-lookup"><span data-stu-id="5b723-116">**Note** For App-V version4.6 and later, when the App-V client is installed, SFTLDR.DLL is copied to the Windows\\system32 directory.</span></span> <span data-ttu-id="5b723-117">Если клиент App-V установлен на 64-разрядной системе, SFTLDR\_WOW64.DLL копируется в каталог Windows\\SysWOW64.</span><span class="sxs-lookup"><span data-stu-id="5b723-117">If the App-V client is installed on a 64-bit system, SFTLDR\_WOW64.DLL is copied to the Windows\\SysWOW64 directory.</span></span>

 

<span data-ttu-id="5b723-118">\ [Значение маркера шаблона \]</span><span class="sxs-lookup"><span data-stu-id="5b723-118">\[Template Token Value\]</span></span>

## <span data-ttu-id="5b723-119">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="5b723-119">In This Section</span></span>


<span data-ttu-id="5b723-120">В следующих разделах описано, как установить клиентское приложение Application Virtualization (App-V) или клиент App-V для служб удаленных рабочих столов (ранее — службы терминалов), используя либо setup.exe, либо setup.msi.</span><span class="sxs-lookup"><span data-stu-id="5b723-120">The following topics describe how to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[<span data-ttu-id="5b723-121">Установка клиента App-V с помощью Setup.exe</span><span class="sxs-lookup"><span data-stu-id="5b723-121">How to Install the App-V Client by Using Setup.exe</span></span>](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
<span data-ttu-id="5b723-122">В этой статье приведены пошаговые инструкции по установке клиента App-V с помощью программы setup.exe.</span><span class="sxs-lookup"><span data-stu-id="5b723-122">Provides a step-by-step procedure for installing the App-V client by using the setup.exe program.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[<span data-ttu-id="5b723-123">Установка клиента App-V с помощью Setup.msi</span><span class="sxs-lookup"><span data-stu-id="5b723-123">How to Install the App-V Client by Using Setup.msi</span></span>](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
<span data-ttu-id="5b723-124">В этой статье приведены пошаговые инструкции по установке любого программного обеспечения, а также клиента App-V с помощью программы setup.msi.</span><span class="sxs-lookup"><span data-stu-id="5b723-124">Provides step-by-step procedures for installing any prerequisite software and also the App-V client by using the setup.msi program.</span></span>

## <span data-ttu-id="5b723-125">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5b723-125">Related topics</span></span>


[<span data-ttu-id="5b723-126">Параметры командной строки установщика клиента Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="5b723-126">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="5b723-127">Установка клиента Application Virtualization Client вручную</span><span class="sxs-lookup"><span data-stu-id="5b723-127">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="5b723-128">Публикация виртуального приложения на клиенте</span><span class="sxs-lookup"><span data-stu-id="5b723-128">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="5b723-129">Удаление клиента App-V</span><span class="sxs-lookup"><span data-stu-id="5b723-129">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





