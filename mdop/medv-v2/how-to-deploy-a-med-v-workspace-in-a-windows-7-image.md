---
title: Развертывание рабочей области MED-V в образе Windows 7
description: Развертывание рабочей области MED-V в образе Windows 7
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827282"
---
# <span data-ttu-id="cefab-103">Развертывание рабочей области MED-V в образе Windows 7</span><span class="sxs-lookup"><span data-stu-id="cefab-103">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>


<span data-ttu-id="cefab-104">Все компоненты MED-V можно установить в образ Windows 7, распространяемый в рамках всего предприятия, так же, как и в любой новой версии Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cefab-104">You can install all the MED-V components into a Windows 7 image that you distribute throughout your enterprise just as you would any new installation of Windows 7.</span></span> <span data-ttu-id="cefab-105">Конечный пользователь затем завершает установку рабочей области MED-V, щелкнув ярлык меню " **Пуск** ", который вы настроили на запуск med-v.</span><span class="sxs-lookup"><span data-stu-id="cefab-105">The end user then finishes the installation of the MED-V workspace by clicking a **Start** menu shortcut that you configure to start MED-V.</span></span> <span data-ttu-id="cefab-106">При первом запуске программы установки для завершения настройки выполняются инструкции конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="cefab-106">First time setup starts and the end user follows the instructions to complete the configuration.</span></span>

<span data-ttu-id="cefab-107">В следующем разделе содержатся сведения и инструкции, которые помогут вам развернуть рабочую область MED-V в рамках всего предприятия с помощью образа Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cefab-107">The following section provides information and instructions to help you deploy the MED-V workspace throughout your enterprise by using a Windows 7 image.</span></span>

**<span data-ttu-id="cefab-108">Развертывание рабочей области MED-V в образе Windows 7</span><span class="sxs-lookup"><span data-stu-id="cefab-108">To deploy a MED-V workspace in a Windows 7 image</span></span>**

1.  <span data-ttu-id="cefab-109">Создание стандартного изображения Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cefab-109">Create a standard image of Windows 7.</span></span> <span data-ttu-id="cefab-110">Дополнительные сведения можно найти в [статье Создание стандартного образа Windows 7: пошаговое руководство](https://go.microsoft.com/fwlink/?LinkId=204843) ( https://go.microsoft.com/fwlink/?LinkId=204843) .</span><span class="sxs-lookup"><span data-stu-id="cefab-110">For more information, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=204843) (https://go.microsoft.com/fwlink/?LinkId=204843).</span></span>

2.  <span data-ttu-id="cefab-111">В образе Windows 7 Установите Windows Virtual PC и обновления виртуальных компьютеров с Windows.</span><span class="sxs-lookup"><span data-stu-id="cefab-111">In the Windows 7 image, install Windows Virtual PC and the Windows Virtual PC updates.</span></span> <span data-ttu-id="cefab-112">Дополнительные сведения можно найти в разделе [Настройка предварительных требований для установки](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="cefab-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

3.  <span data-ttu-id="cefab-113">Установите агент узла MED-V с помощью установочного файла MED-V \ _HostAgent \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="cefab-113">Install the MED-V Host Agent by using the MED-V\_HostAgent\_Setup installation file.</span></span> <span data-ttu-id="cefab-114">Дополнительные сведения [можно найти в разделе Установка агента узла MED-V вручную](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="cefab-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    <span data-ttu-id="cefab-115">**Предупреждение**  Internet Explorer необходимо закрыть перед установкой агента узла MED-V, в противном случае конфликты могут возникать позже с перенаправлением URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="cefab-115">**Warning** Internet Explorer must be closed before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="cefab-116">Вы также можете сделать это, указав компьютер во время распространения.</span><span class="sxs-lookup"><span data-stu-id="cefab-116">You can also do this by specifying a computer restart during a distribution.</span></span>

     

4.  <span data-ttu-id="cefab-117">Скопируйте файлы пакета рабочей области для MED-V в образ Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cefab-117">Copy the MED-V workspace package files to the Windows 7 image.</span></span> <span data-ttu-id="cefab-118">Файлы пакета рабочей области для MED-V — это файл установщика рабочей области MED-V, MEDV и файл setup.exe, созданный с помощью **диспетчера рабочих областей med-v**.</span><span class="sxs-lookup"><span data-stu-id="cefab-118">The MED-V workspace package files are the MED-V workspace installer, .medv file, and setup.exe file that you created by using the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="cefab-119">**Важно!**  Файл. MEDV и setup.exe должен находиться в той же папке, что и программа установки рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="cefab-119">**Important** The .medv and setup.exe file must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="cefab-120">Затем установите рабочую область MED-V, запустив setup.exe.</span><span class="sxs-lookup"><span data-stu-id="cefab-120">Then, install the MED-V workspace by running setup.exe.</span></span>

     

5.  <span data-ttu-id="cefab-121">Настройте ярлык в меню " **Пуск** ", чтобы открыть пакет рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="cefab-121">Configure a shortcut on the **Start** menu to open the MED-V workspace package installation.</span></span>

    <span data-ttu-id="cefab-122">Создание ярлыка меню " **Пуск** " для файла setup.exe, позволяющего конечному пользователю ЗАПУСКАТЬ установку MED-V по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="cefab-122">Create a **Start** menu shortcut to the setup.exe file that lets the end user start a MED-V installation as required.</span></span>

6.  <span data-ttu-id="cefab-123">Используя стандартный процесс развертывания образа компании, вы можете распространять его на компьютеры в вашей организации, требующие MED-V.</span><span class="sxs-lookup"><span data-stu-id="cefab-123">By using your company’s standard image deployment process, distribute the Windows 7 image to computers in your enterprise that require MED-V.</span></span>

<span data-ttu-id="cefab-124">Когда конечный пользователь должен получить доступ к приложению, опубликованному в рабочей области MED-V, он может щелкнуть ярлык меню " **Пуск** ", чтобы установить рабочую область "med-v".</span><span class="sxs-lookup"><span data-stu-id="cefab-124">When the end user has to access an application published in the MED-V workspace, they can click the **Start** menu shortcut to install the MED-V workspace.</span></span> <span data-ttu-id="cefab-125">Это автоматически запускается при первом запуске программы установки и завершает настройку MED-V.</span><span class="sxs-lookup"><span data-stu-id="cefab-125">This automatically starts first time setup and completes the configuration of MED-V.</span></span> <span data-ttu-id="cefab-126">После того как вы закончите настройку, конечный пользователь сможет получить доступ к приложениям для MED-V в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="cefab-126">After first time setup is complete, the end user can access the MED-V applications on the **Start** menu.</span></span>

## <span data-ttu-id="cefab-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="cefab-127">Related topics</span></span>


[<span data-ttu-id="cefab-128">Обзор развертывания MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="cefab-128">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="cefab-129">Развертывание рабочей области MED-V с помощью системы электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="cefab-129">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





