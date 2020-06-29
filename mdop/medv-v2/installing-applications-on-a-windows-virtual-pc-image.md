---
title: Установка приложений в образе Windows Virtual PC
description: Установка приложений в образе Windows Virtual PC
author: dansimp
ms.assetid: 32651eff-e3c6-4ef4-947d-2beddc695eac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bf73fec0b33b37c2553dfe6f923917aa926b8e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826832"
---
# <span data-ttu-id="72970-103">Установка приложений в образе Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="72970-103">Installing Applications on a Windows Virtual PC Image</span></span>


<span data-ttu-id="72970-104">После создания образа Virtual PC для Windows для работы с Microsoft Enterprise Virtualization (MED-V) 2,0 вы можете установить другие компоненты, которые полезны при работе с MED-V, например с электронной системой распространения программного обеспечения (ESD) и антивирусным программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="72970-104">After you have created a Windows Virtual PC image for use with Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you can install other components that are helpful when running MED-V, such as an electronic software distribution (ESD) system and antivirus software.</span></span>

<span data-ttu-id="72970-105">В следующем разделе приведены сведения, которые помогут вам установить программное обеспечение на изображении MED-V.</span><span class="sxs-lookup"><span data-stu-id="72970-105">The following section provides information to help you install software on the MED-V image.</span></span>

<span data-ttu-id="72970-106">**Внимание!**  Для упрощения управления рабочими областями MED-V после развертывания мы рекомендуем ограничить количество компонентов, устанавливаемых на изображении MED-V, до тех компонентов, которые являются обязательными или полезны при использовании MED-V.</span><span class="sxs-lookup"><span data-stu-id="72970-106">**Caution** For ease of MED-V workspace management after deployment, we recommend that you limit the number of components that you install on the MED-V image to those components that are required or that are helpful when using MED-V.</span></span> <span data-ttu-id="72970-107">Например, несмотря на то, что для использования MED-V не требуется, вы можете установить систему ESD для более поздней установки приложений в рабочую область и антивирусную программу MED-V для обеспечения безопасности на этом изображении.</span><span class="sxs-lookup"><span data-stu-id="72970-107">For example, although they are not required to run MED-V, you can install an ESD system to use later for installing applications to a MED-V workspace and antivirus software for security on the image.</span></span>

 

**<span data-ttu-id="72970-108">Установка программного обеспечения на изображениях MED-V</span><span class="sxs-lookup"><span data-stu-id="72970-108">Installing Software on a MED-V Image</span></span>**

1.  <span data-ttu-id="72970-109">Откройте виртуальную машину MED-V, если она еще не запущена.</span><span class="sxs-lookup"><span data-stu-id="72970-109">If it is not currently running, open your MED-V virtual machine.</span></span>

    1.  <span data-ttu-id="72970-110">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Virtual PC** и **Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="72970-110">Click **Start**, click **All Programs**, click **Windows Virtual PC** and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="72970-111">Дважды щелкните виртуальную машину MED-V.</span><span class="sxs-lookup"><span data-stu-id="72970-111">Double-click your MED-V virtual machine.</span></span>

2.  <span data-ttu-id="72970-112">В операционной системе виртуальной машины найдите файлы установки для программного обеспечения, которое вы хотите установить.</span><span class="sxs-lookup"><span data-stu-id="72970-112">From inside the virtual machine operating system, locate the installation files for the software that you want to install.</span></span>

3.  <span data-ttu-id="72970-113">Следуйте инструкциям по установке, предоставленным поставщиком программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="72970-113">Follow the installation instructions that are provided by the software vendor.</span></span>

    <span data-ttu-id="72970-114">**Примечание**  После завершения установки может потребоваться закрыть и перезапустить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="72970-114">**Note** After installation is complete, you might have to close and then restart the virtual machine.</span></span>

     

<span data-ttu-id="72970-115">Повторите эти действия для любого программного обеспечения или приложения, которое вы хотите установить в образе MED-V.</span><span class="sxs-lookup"><span data-stu-id="72970-115">Repeat these steps for any software or application that you want to install on the MED-V image.</span></span> <span data-ttu-id="72970-116">Рекомендуем ограничить количество приложений, предварительно устанавливаемых на образ.</span><span class="sxs-lookup"><span data-stu-id="72970-116">We recommend that you limit the number of applications that you preinstall on the image.</span></span> <span data-ttu-id="72970-117">Рекомендуемая процедура установки приложений и другого программного обеспечения на изображении состоит в том, чтобы предварительно установить систему ESD и использовать ее позднее для развертывания программного обеспечения на изображении.</span><span class="sxs-lookup"><span data-stu-id="72970-117">The recommended process for installing applications and other software on the image is to preinstall an ESD system now and to use it later to deploy software to the image.</span></span> <span data-ttu-id="72970-118">Кроме того, вы также можете использовать групповую политику или App-V для добавления или удаления приложений в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="72970-118">Alternately, you can also use Group Policy or App-V to add or remove applications on a MED-V workspace.</span></span> <span data-ttu-id="72970-119">Дополнительные сведения можно найти [в разделе Управление приложениями, развернутыми в рабочих областях MED-V](managing-applications-deployed-to-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="72970-119">For more information, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

<span data-ttu-id="72970-120">Дополнительные сведения о том, как установить программное обеспечение на виртуальном изображении, можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="72970-120">For more information about how to install software on a virtual image, see the following articles:</span></span>

-   <span data-ttu-id="72970-121">[Публикация и использование виртуальных приложений](https://go.microsoft.com/fwlink/?LinkId=195926) ( https://go.microsoft.com/fwlink/?LinkId=195926) .</span><span class="sxs-lookup"><span data-stu-id="72970-121">[Publish and Use Virtual Applications](https://go.microsoft.com/fwlink/?LinkId=195926) (https://go.microsoft.com/fwlink/?LinkId=195926).</span></span>

-   <span data-ttu-id="72970-122">[Справка по Virtual PC для Windows](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="72970-122">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="72970-123">После установки всех нужных программных средств в образе MED-V ваше изображение будет готово к упаковке.</span><span class="sxs-lookup"><span data-stu-id="72970-123">After you have installed all of the software that you want on the MED-V image, your image is ready to be packaged.</span></span>

## <span data-ttu-id="72970-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="72970-124">Related topics</span></span>


[<span data-ttu-id="72970-125">Настройка образа Windows Virtual PC для MED-V</span><span class="sxs-lookup"><span data-stu-id="72970-125">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="72970-126">Подготовка образа MED-V</span><span class="sxs-lookup"><span data-stu-id="72970-126">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)

 

 





