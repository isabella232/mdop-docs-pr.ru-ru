---
title: Развертывание DaRT 7.0
description: Развертывание DaRT 7.0
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813048"
---
# <span data-ttu-id="a7970-103">Развертывание DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="a7970-103">How to Deploy DaRT 7.0</span></span>


<span data-ttu-id="a7970-104">В этом разделе приводятся инструкции по развертыванию набора средств диагностики и восстановления Microsoft (DaRT) 7 в среде.</span><span class="sxs-lookup"><span data-stu-id="a7970-104">This topic provides instructions to deploy Microsoft Diagnostics and Recovery Toolset (DaRT)7 in your environment.</span></span> <span data-ttu-id="a7970-105">В первой процедуре, описанной в этом разделе, предполагается, что вы устанавливаете все возможности на одном компьютере администратора.</span><span class="sxs-lookup"><span data-stu-id="a7970-105">The first procedure in this topic assumes that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="a7970-106">Если вам нужно развернуть или удалить DaRT на нескольких компьютерах, используя электронную систему распространения программного обеспечения, например, можно использовать параметры установки из командной строки.</span><span class="sxs-lookup"><span data-stu-id="a7970-106">When you need to deploy or uninstall DaRT on multiple computers, using an electronic software distribution system for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="a7970-107">Эти параметры определяются во второй процедуре в этом разделе, в которой приводится пример использования доступных параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="a7970-107">Those options are defined in the second procedure in this topic which provides example usage for the available command line options.</span></span>

<span data-ttu-id="a7970-108">**Важно!**  Перед установкой DaRT убедитесь, что компьютер соответствует минимальным требованиям к системе, указанным в разделе [DaRT 7,0 поддерживаемые конфигурации](dart-70-supported-configurations-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="a7970-108">**Important** Before you install DaRT, ensure that the computer meets the minimum system requirements listed in [DaRT 7.0 Supported Configurations](dart-70-supported-configurations-dart-7.md).</span></span>

 

**<span data-ttu-id="a7970-109">Установка DaRT на компьютере администратора</span><span class="sxs-lookup"><span data-stu-id="a7970-109">To install DaRT on an administrator computer</span></span>**

1.  <span data-ttu-id="a7970-110">Найдите файлы установки DaRT, полученные в ходе загрузки программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="a7970-110">Locate the DaRT installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="a7970-111">Дважды щелкните файл установки DaRT, соответствующий вашим требованиям к системе: с 32 или 64-бит.</span><span class="sxs-lookup"><span data-stu-id="a7970-111">Double-click the DaRT installation file that corresponds to your system requirements, either 32-bit or 64-bit.</span></span> <span data-ttu-id="a7970-112">Файл установки DaRT назван **MSDaRT70.msi**.</span><span class="sxs-lookup"><span data-stu-id="a7970-112">The DaRT installation file is named **MSDaRT70.msi**.</span></span>

3.  <span data-ttu-id="a7970-113">Приняв условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="a7970-113">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="a7970-114">Выберите конечную папку для установки DaRT, укажите, следует ли устанавливать DaRT для всех пользователей или только для текущего пользователя, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="a7970-114">Select the destination folder for installing DaRT, select whether DaRT should be installed for all users or just the current user, and then click **Next**.</span></span>

5.  <span data-ttu-id="a7970-115">Укажите, должна ли установка быть **обычной**, **настраиваемой**или **завершенной**, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="a7970-115">Select whether the installation should be **Typical**, **Custom**, or **Complete**, and then click **Next**.</span></span>

    -   <span data-ttu-id="a7970-116">**Обычно** устанавливаются наиболее часто используемые инструменты.</span><span class="sxs-lookup"><span data-stu-id="a7970-116">**Typical** installs the tools that are most frequently used.</span></span> <span data-ttu-id="a7970-117">Этот метод рекомендуется для большинства пользователей.</span><span class="sxs-lookup"><span data-stu-id="a7970-117">This method is recommended for most users.</span></span>

    -   <span data-ttu-id="a7970-118">" **Настраиваемый** " — позволяет выбрать установленные инструменты и их там, где они будут установлены.</span><span class="sxs-lookup"><span data-stu-id="a7970-118">**Custom** lets you select the tools that are installed and where they will be installed.</span></span> <span data-ttu-id="a7970-119">Это рекомендовано для опытных пользователей, особенно если вы устанавливаете различные инструменты DaRT на разных компьютерах службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="a7970-119">This is recommended for advanced users, especially if you are installing different DaRT tools on different helpdesk computers.</span></span>

    -   <span data-ttu-id="a7970-120">**Полная** установка всех инструментов DaRT и требует наибольшего свободного места на диске.</span><span class="sxs-lookup"><span data-stu-id="a7970-120">**Complete** installs all DaRT tools and requires the most disk space.</span></span>

    <span data-ttu-id="a7970-121">После выбора способа установки нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="a7970-121">After you have selected your method of installation, click **Next**.</span></span>

6.  <span data-ttu-id="a7970-122">Чтобы начать установку, нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="a7970-122">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="a7970-123">После успешного завершения установки нажмите кнопку **Готово** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="a7970-123">After the installation is completed successfully, click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="a7970-124">Установка DaRT в командной строке</span><span class="sxs-lookup"><span data-stu-id="a7970-124">To install DaRT at the command prompt</span></span>**

1.  <span data-ttu-id="a7970-125">В следующем примере показано, как установить все функции DaRT.</span><span class="sxs-lookup"><span data-stu-id="a7970-125">The following example shows how to install all DaRT functionality.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  <span data-ttu-id="a7970-126">В следующем примере показано, как установить только **Мастер переноса изображений для восстановления DaRT**.</span><span class="sxs-lookup"><span data-stu-id="a7970-126">The following example shows how to install only the **DaRT Recovery Image Wizard**.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  <span data-ttu-id="a7970-127">В следующем примере показано, как установить только анализатор аварийного восстановления и средство просмотра удаленных подключений DaRT.</span><span class="sxs-lookup"><span data-stu-id="a7970-127">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  <span data-ttu-id="a7970-128">В следующем примере создается журнал установки для установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="a7970-128">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="a7970-129">Это полезно для отладки.</span><span class="sxs-lookup"><span data-stu-id="a7970-129">This is valuable for debugging.</span></span>

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

<span data-ttu-id="a7970-130">**Примечание**  Вы можете добавить/Qn или/QB к любому из параметров командной строки для установки DaRT, чтобы выполнить автоматическую установку.</span><span class="sxs-lookup"><span data-stu-id="a7970-130">**Note** You can add /qn or /qb to any of the DaRT installation command prompt options to perform a silent installation.</span></span>

 

## <span data-ttu-id="a7970-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a7970-131">Related topics</span></span>


[<span data-ttu-id="a7970-132">Развертывание DaRT 7.0 на компьютерах администраторов</span><span class="sxs-lookup"><span data-stu-id="a7970-132">Deploying DaRT 7.0 to Administrator Computers</span></span>](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 





