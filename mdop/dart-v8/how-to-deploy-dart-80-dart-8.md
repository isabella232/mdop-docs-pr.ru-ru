---
title: Развертывание DaRT 8.0
description: Развертывание DaRT 8.0
author: dansimp
ms.assetid: ab772e7a-c02f-4847-acdf-8bd362769a77
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e7d64297f7687ebc0a23add3aa749ee4719beee4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824299"
---
# <span data-ttu-id="39de0-103">Развертывание DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="39de0-103">How to Deploy DaRT 8.0</span></span>


<span data-ttu-id="39de0-104">Ниже приведены инструкции по развертыванию набора средств диагностики и восстановления Microsoft (DaRT) 8,0 в среде.</span><span class="sxs-lookup"><span data-stu-id="39de0-104">The following instructions explain how to deploy Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 in your environment.</span></span> <span data-ttu-id="39de0-105">Для получения программного обеспечения DaRT ознакомьтесь [со статьей получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="39de0-105">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span> <span data-ttu-id="39de0-106">Предполагается, что все возможности устанавливаются на одном компьютере администратора.</span><span class="sxs-lookup"><span data-stu-id="39de0-106">It is assumed that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="39de0-107">Если вам нужно развернуть или удалить DaRT 8,0 на нескольких компьютерах, используя электронную систему распространения программного обеспечения, например, вы можете использовать параметры установки из командной строки.</span><span class="sxs-lookup"><span data-stu-id="39de0-107">If you need to deploy or uninstall DaRT 8.0 on multiple computers, using an electronic software distribution system, for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="39de0-108">В этом разделе приведены описания и примеры доступных параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="39de0-108">Descriptions and examples of the available command line options are provided in this section.</span></span>

<span data-ttu-id="39de0-109">**Важно!**  Перед установкой DaRT ознакомьтесь с разрядом [конфигураций dart 8,0](dart-80-supported-configurations-dart-8.md) , чтобы убедиться, что вы установили все необходимое программное обеспечение и что компьютер отвечает минимальным требованиям к системе.</span><span class="sxs-lookup"><span data-stu-id="39de0-109">**Important** Before you install DaRT, see [DaRT 8.0 Supported Configurations](dart-80-supported-configurations-dart-8.md) to ensure that you have installed all of the prerequisite software and that the computer meets the minimum system requirements.</span></span> <span data-ttu-id="39de0-110">На компьютере, на котором вы хотите установить DaRT, должна быть установлена операционная система Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="39de0-110">The computer onto which you install DaRT must be running Windows 8 or Windows Server 2012.</span></span>

 

<span data-ttu-id="39de0-111">Вы можете установить DaRT с помощью одной из двух различных конфигураций.</span><span class="sxs-lookup"><span data-stu-id="39de0-111">You can install DaRT using one of two different configurations:</span></span>

-   <span data-ttu-id="39de0-112">Установите DaRT и все инструменты DaRT на компьютере администратора.</span><span class="sxs-lookup"><span data-stu-id="39de0-112">Install DaRT and all of the DaRT tools on the administrator computer.</span></span>

-   <span data-ttu-id="39de0-113">Установите на компьютере администратора только те инструменты, которые необходимы для создания изображения для восстановления DaRT, а затем установите **средство просмотра удаленных подключений** и, при необходимости, **анализатор аварийных сбоев** на компьютере службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="39de0-113">Install on the administrator computer only the tools that you need to create the DaRT recovery image, and then install the **Remote Connection Viewer** and, optionally, **Crash Analyzer** on a help desk computer.</span></span>

<span data-ttu-id="39de0-114">Файл установки DaRT доступен как в 32-, так и в 64-разрядных версиях.</span><span class="sxs-lookup"><span data-stu-id="39de0-114">The DaRT installation file is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="39de0-115">Установите версию, совпадающую с архитектурой компьютера, на котором запущен мастер изображений для восстановления DaRT, а не архитектурой компьютера для создаваемого образа восстановления.</span><span class="sxs-lookup"><span data-stu-id="39de0-115">Install the version that matches the architecture of the computer on which you are running the DaRT Recovery Image wizard, not the computer architecture of the recovery image that you are creating.</span></span>

<span data-ttu-id="39de0-116">Вы можете использовать любую из версий установочного файла DaRT для создания образа восстановления для 32 или 64-разрядных компьютеров, но вы не можете создать один образ восстановления как для 32, так и для 64-разрядных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="39de0-116">You can use either version of the DaRT installation file to create a recovery image for either 32-bit or 64-bit computers, but you cannot create one recovery image for both 32-bit and 64-bit computers.</span></span>

**<span data-ttu-id="39de0-117">Установка и удаление DaRT и всех инструментов DaRT на компьютере администратора</span><span class="sxs-lookup"><span data-stu-id="39de0-117">To install DaRT and all DaRT tools on an administrator computer</span></span>**

1.  <span data-ttu-id="39de0-118">Загрузите файл установщика DaRT 8,0 (32-разрядная версия или 64-разр.).</span><span class="sxs-lookup"><span data-stu-id="39de0-118">Download the 32-bit or 64-bit version of the DaRT 8.0 installer file.</span></span> <span data-ttu-id="39de0-119">Выберите архитектуру, соответствующую компьютеру, на котором вы хотите установить DaRT, и запустите мастер переноса изображений с помощью DaRT Recovery.</span><span class="sxs-lookup"><span data-stu-id="39de0-119">Choose the architecture that matches the computer on which you are installing DaRT and running the DaRT Recovery Image wizard.</span></span>

2.  <span data-ttu-id="39de0-120">В папке, в которую вы загрузили DaRT 8,0, запустите установочный файл **MSDaRT80.msi** , соответствующий вашим требованиям к системе.</span><span class="sxs-lookup"><span data-stu-id="39de0-120">From the folder into which you downloaded DaRT 8.0, run the **MSDaRT80.msi** installation file that corresponds to your system requirements.</span></span>

3.  <span data-ttu-id="39de0-121">На странице **Добро пожаловать на страницу мастера настройки Microsoft DaRT 8,0** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="39de0-121">On the **Welcome to the Microsoft DaRT 8.0 Setup Wizard** page, click **Next**.</span></span>

4.  <span data-ttu-id="39de0-122">Приняв условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="39de0-122">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

5.  <span data-ttu-id="39de0-123">На странице **центра обновления Майкрософт** установите флажок **использовать Microsoft Update после проверки обновлений**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="39de0-123">On the **Microsoft Update** page, select **Use Microsoft Update when I check for updates**, and then click **Next**.</span></span>

6.  <span data-ttu-id="39de0-124">На странице " **Выбор папки для установки** " выберите папку или нажмите кнопку " **Далее** ", чтобы установить DART в папке для установки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="39de0-124">On the **Select Installation Folder** page, select a folder, or click **Next** to install DaRT in the default installation location.</span></span>

7.  <span data-ttu-id="39de0-125">На странице **Параметры настройки** выберите компоненты DART, которые вы хотите установить, или нажмите кнопку **Далее** , чтобы установить DART вместе со всеми функциями.</span><span class="sxs-lookup"><span data-stu-id="39de0-125">On the **Setup Options** page, select the DaRT features that you want to install, or click **Next** to install DaRT with all of the features.</span></span>

8.  <span data-ttu-id="39de0-126">Чтобы начать установку, нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="39de0-126">To start the installation, click **Install**.</span></span>

9.  <span data-ttu-id="39de0-127">После успешного завершения установки нажмите кнопку **Готово** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="39de0-127">After the installation has completed successfully, click **Finish** to exit the wizard.</span></span>

## <span data-ttu-id="39de0-128">Установка и удаление DaRT и всех инструментов DaRT на компьютере с администратором с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="39de0-128">To install DaRT and all DaRT tools on an administrator computer by using a command prompt</span></span>


<span data-ttu-id="39de0-129">При установке или удалении DaRT вы сможете запускать установочные файлы в командной строке.</span><span class="sxs-lookup"><span data-stu-id="39de0-129">When you install or uninstall DaRT, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="39de0-130">В этом разделе описаны некоторые примеры различных параметров, которые можно указать при установке или удалении DaRT в командной строке.</span><span class="sxs-lookup"><span data-stu-id="39de0-130">This section describes some examples of different options that you can specify when you install or uninstall DaRT at the command prompt.</span></span>

<span data-ttu-id="39de0-131">В следующем примере показано, как установить все функции DaRT.</span><span class="sxs-lookup"><span data-stu-id="39de0-131">The following example shows how to install all DaRT functionality.</span></span>

``` syntax
msiexec /i MSDaRT80.msi ADDLOCAL=CommonFiles, DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="39de0-132">В следующем примере показано, как установить только мастер переноса изображений для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="39de0-132">The following example shows how to install only the DaRT Recovery Image wizard.</span></span>

``` syntax
msiexec /i MSDaRT80.msi ADDLOCAL=CommonFiles, ,DaRTRecoveryImage
```

<span data-ttu-id="39de0-133">В следующем примере показано, как установить только анализатор аварийного восстановления и средство просмотра удаленных подключений DaRT.</span><span class="sxs-lookup"><span data-stu-id="39de0-133">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

``` syntax
msiexec /i MSDaRT80.msi ADDLOCAL=CommonFiles,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="39de0-134">В следующем примере создается журнал установки для установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="39de0-134">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="39de0-135">Это полезно для отладки.</span><span class="sxs-lookup"><span data-stu-id="39de0-135">This is valuable for debugging.</span></span>

``` syntax
msiexec.exe /i MSDaRT80.msi /l*v log.txt 
```

<span data-ttu-id="39de0-136">**Примечание**  Вы можете добавить/Qn или/QB для выполнения автоматической установки.</span><span class="sxs-lookup"><span data-stu-id="39de0-136">**Note** You can add /qn or /qb to perform a silent installation.</span></span>

 

**<span data-ttu-id="39de0-137">Проверка установки DaRT</span><span class="sxs-lookup"><span data-stu-id="39de0-137">To validate the DaRT installation</span></span>**

1.  <span data-ttu-id="39de0-138">Нажмите кнопку **Пуск**и выберите **набор средств диагностики и восстановления**.</span><span class="sxs-lookup"><span data-stu-id="39de0-138">Click **Start**, and select **Diagnostics and Recovery Toolset**.</span></span>

    <span data-ttu-id="39de0-139">Откроется окно **инструментов Диагностика и восстановление** .</span><span class="sxs-lookup"><span data-stu-id="39de0-139">The **Diagnostics and Recovery Toolset** window opens.</span></span>

2.  <span data-ttu-id="39de0-140">Убедитесь, что все инструменты DaRT, выбранные для установки, успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="39de0-140">Check that all of the DaRT tools that you selected for installation were successfully installed.</span></span>

## <span data-ttu-id="39de0-141">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="39de0-141">Related topics</span></span>


[<span data-ttu-id="39de0-142">Развертывание DaRT 8.0 на компьютерах администраторов</span><span class="sxs-lookup"><span data-stu-id="39de0-142">Deploying DaRT 8.0 to Administrator Computers</span></span>](deploying-dart-80-to-administrator-computers-dart-8.md)

 

 





