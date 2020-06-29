---
title: Описание этапов виртуализации
description: Описание этапов виртуализации
author: dansimp
ms.assetid: c1cb7b6c-204c-48f2-848c-4bd5a3d5ecb6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e3d1504f0af82f3d21806b38bb4640b6f7ebc45
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820002"
---
# <span data-ttu-id="d0949-103">Описание этапов виртуализации</span><span class="sxs-lookup"><span data-stu-id="d0949-103">About Sequencing Phases</span></span>


<span data-ttu-id="d0949-104">Последовательность — это процесс, в ходе которого вы создаете последовательный пакет приложения с помощью Microsoft Application Virtualization (App-V) Sequencer.</span><span class="sxs-lookup"><span data-stu-id="d0949-104">Sequencing is the process by which you create a sequenced application package by using the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="d0949-105">Во время виртуализации секвенсор отслеживает и записывает все процессы установки и настройки для приложения и создает следующие файлы: ICO, OSD, SFT и SPRJ.</span><span class="sxs-lookup"><span data-stu-id="d0949-105">During sequencing, the Sequencer monitors and records all installation and setup processes for an application and creates the following files: ICO, OSD, SFT, and SPRJ.</span></span> <span data-ttu-id="d0949-106">Эти файлы содержат все необходимые сведения о приложении, и они позволяют запускать это приложение в виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="d0949-106">These files contain all the necessary information about an application, and they allow that application to run in a virtual environment.</span></span>

<span data-ttu-id="d0949-107">Четыре фазы для упорядочивания приложения и создания виртуального пакета приложения — Установка, запуск, Настройка и сохранение.</span><span class="sxs-lookup"><span data-stu-id="d0949-107">The four phases to sequencing an application and creating a virtual application package are installation, launch, customization, and save.</span></span> <span data-ttu-id="d0949-108">В списке ниже приведены сведения о каждом из фаз.</span><span class="sxs-lookup"><span data-stu-id="d0949-108">The following list provides information about each of the phases:</span></span>

1.  <span data-ttu-id="d0949-109">**Этап установки**— на этапе установки вы указываете имя пакета и дополнительный связанный комментарий, который будет связан с пакетом.</span><span class="sxs-lookup"><span data-stu-id="d0949-109">**Installation phase**—During the installation phase, you specify the package name and an optional associated comment that will be associated with the package.</span></span> <span data-ttu-id="d0949-110">На этом этапе вы также можете настроить дополнительные параметры наблюдения.</span><span class="sxs-lookup"><span data-stu-id="d0949-110">You can also configure advanced monitoring options during this phase.</span></span> <span data-ttu-id="d0949-111">Расширенные возможности наблюдения включают в себя указание размера блока и возможность установки автоматических обновлений во время наблюдения.</span><span class="sxs-lookup"><span data-stu-id="d0949-111">Advanced monitoring options include specifying the block size and whether you will install automatic updates during monitoring.</span></span> <span data-ttu-id="d0949-112">Секвенсор записывает все необходимые сведения и конфигурации, необходимые для создания виртуального пакета приложения и связанного файла и параметров реестра.</span><span class="sxs-lookup"><span data-stu-id="d0949-112">The sequencer records all necessary information and configurations required to create a virtual application package and the associated file and registry settings.</span></span>

    <span data-ttu-id="d0949-113">**Важно!**  Чтобы просмотреть дополнительные параметры, нажмите кнопку **Показать дополнительные параметры наблюдения** на странице **сведения о пакете** .</span><span class="sxs-lookup"><span data-stu-id="d0949-113">**Important** To view the advanced options select **Show Advanced Monitoring Options** on the **Package Information** page.</span></span>

     

2.  <span data-ttu-id="d0949-114">**Этап запуска**— на этапе запуска вы можете указать необходимые сопоставления файлов и дескрипторы безопасности, которые следует настроить для пакета.</span><span class="sxs-lookup"><span data-stu-id="d0949-114">**Launch phase**—During the launch phase, you can specify any required file associations and security descriptors that should be configured with the package.</span></span> <span data-ttu-id="d0949-115">Вы должны открыть приложение столько, сколько нужно, чтобы обеспечить работу приложения и стабильность.</span><span class="sxs-lookup"><span data-stu-id="d0949-115">You should open the application as many times as necessary to ensure application functionality and stability.</span></span>

3.  <span data-ttu-id="d0949-116">**Этап настройки**— на этапе настройки вы можете настроить пакет с помощью связанных OSD-файлов.</span><span class="sxs-lookup"><span data-stu-id="d0949-116">**Customization phase**—During the customization phase, you can configure your package by using the associated .osd files.</span></span> <span data-ttu-id="d0949-117">Вы можете указать, должны ли какие-либо связанные сценарии выполняться внутри или вне виртуальной среды, указать дополнительные действия, которые нужно выполнить, указать, как выполняются связанные сценарии (синхронные или асинхронные), и указать любые дополнительные сценарии, которые должны выполняться в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="d0949-117">You can specify whether any associated scripts should run inside or outside of the virtual environment, specify additional actions that should be performed, specify how associated scripts run (synchronously or asynchronously), and specify any additional scripts that should be run under the user context.</span></span>

4.  <span data-ttu-id="d0949-118">**Этап сохранения**— на этапе сохранения создаются все необходимые файлы для виртуального пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="d0949-118">**Save phase**—During the save phase, all required files for the virtual application package are created.</span></span> <span data-ttu-id="d0949-119">Созданы файлы. SPRJ, SFT, OSD, ICO, XML и файла установщика Windows (MSI).</span><span class="sxs-lookup"><span data-stu-id="d0949-119">The files created are .sprj, .sft, .osd, .ico, .xml manifest, and the Windows installer (.msi) file.</span></span>

## <span data-ttu-id="d0949-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d0949-120">Related topics</span></span>


[<span data-ttu-id="d0949-121">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="d0949-121">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





