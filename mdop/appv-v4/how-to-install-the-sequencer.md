---
title: Установка программы Sequencer
description: Установка программы Sequencer
author: dansimp
ms.assetid: 2cd16427-a0ba-4870-82d1-3e3c79e1959b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 75a0f987fcc76d1ed92631085a4364ae6e06c9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817269"
---
# <span data-ttu-id="f5f64-103">Установка программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="f5f64-103">How to Install the Sequencer</span></span>


<span data-ttu-id="f5f64-104">Секвенсор Microsoft Application Virtualization (App-V) отслеживает и записывает процесс установки и настройки для приложений, чтобы приложение могло быть запущено как виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="f5f64-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="f5f64-105">Секвенсор необходимо установить на компьютере с установленной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="f5f64-105">You should install the Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="f5f64-106">Кроме того, программа Sequencer может быть установлена на компьютере под управлением виртуальной среды (например, Microsoft Virtual PC).</span><span class="sxs-lookup"><span data-stu-id="f5f64-106">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="f5f64-107">Этот метод полезен, поскольку проще поддерживать чистую последовательность, которую можно повторно использовать с минимальной дополнительной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="f5f64-107">This method is useful because it is easier to maintain a clean sequencing environment that can be reused with minimal additional configuration.</span></span>

<span data-ttu-id="f5f64-108">Вы должны иметь права администратора на компьютере, который вы используете для последовательного приложения, и компьютер должен быть подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="f5f64-108">You must have administrative rights on the computer you are using to sequence the application and the computer must be connected to the network.</span></span> <span data-ttu-id="f5f64-109">На компьютере не должна выполняться ни одна из версий клиента Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="f5f64-109">The computer must not be running any version of the Application Virtualization (App-V) client.</span></span> <span data-ttu-id="f5f64-110">Создание виртуального приложения, использующего секвенсор, занимает много ресурсов, поэтому важно установить секвенсор на компьютер, удовлетворяющий рекомендуемому или превышающему рекомендуемые требования.</span><span class="sxs-lookup"><span data-stu-id="f5f64-110">Creating a virtual application using the Sequencer is very resource intensive, so it is important that you install the Sequencer on a computer that meets or exceeds the recommended requirements.</span></span> <span data-ttu-id="f5f64-111">Дополнительные сведения о требованиях к системе описаны в разделе [требования к оборудованию и программному обеспечению Sequencer](sequencer-hardware-and-software-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f5f64-111">For more information about the system requirements, see [Sequencer Hardware and Software Requirements](sequencer-hardware-and-software-requirements.md)..</span></span>

**<span data-ttu-id="f5f64-112">Установка Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="f5f64-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="f5f64-113">Скопируйте установочные файлы Microsoft Application Sequencer на компьютер, на котором вы хотите установить его.</span><span class="sxs-lookup"><span data-stu-id="f5f64-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer that you want to install it on.</span></span>

2.  <span data-ttu-id="f5f64-114">Чтобы запустить мастер установки Microsoft Application Virtualization Sequencer, выберите **setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="f5f64-114">To start the Microsoft Application Virtualization Sequencer installation wizard, select **setup.exe**.</span></span> <span data-ttu-id="f5f64-115">Если **распространяемый пакет Microsoft Visual C++ с пакетом обновления 1 (x86)** не обнаружен перед установкой, **setup.exe** будет устанавливать его.</span><span class="sxs-lookup"><span data-stu-id="f5f64-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, **setup.exe** will install it.</span></span>

3.  <span data-ttu-id="f5f64-116">На странице **приветствия** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f5f64-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="f5f64-117">На странице Лицензионное **соглашение** для подтверждения условий лицензионного соглашения установите флажок **я принимаю условия лицензионного**соглашения.</span><span class="sxs-lookup"><span data-stu-id="f5f64-117">On the **License Agreement** page, to accept the terms of the license agreement, select **I accept the terms in the license agreement**.</span></span> <span data-ttu-id="f5f64-118">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f5f64-118">Click **Next**.</span></span>

5.  <span data-ttu-id="f5f64-119">На странице **Конечная папка** чтобы сохранить папку установки по умолчанию, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f5f64-119">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="f5f64-120">Чтобы указать другую конечную папку, нажмите кнопку **изменить** и укажите папку установки, которая будет использоваться для установки.</span><span class="sxs-lookup"><span data-stu-id="f5f64-120">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="f5f64-121">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f5f64-121">Click **Next**.</span></span>

6.  <span data-ttu-id="f5f64-122">Чтобы начать установку, на странице **готовность к установке программы** нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="f5f64-122">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="f5f64-123">На странице **завершения работы мастера InstallShield** нажмите кнопку **Готово**, чтобы закрыть мастер установки и открыть секвенсор.</span><span class="sxs-lookup"><span data-stu-id="f5f64-123">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the Sequencer, click **Finish**.</span></span> <span data-ttu-id="f5f64-124">Чтобы закрыть мастер установки, не открывая секвенсор, снимите флажок **запустить программу** и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="f5f64-124">To close the installation wizard without opening the Sequencer, deselect **Launch the program** and click **Finish**.</span></span>

## <span data-ttu-id="f5f64-125">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f5f64-125">Related topics</span></span>


[<span data-ttu-id="f5f64-126">Настройка программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="f5f64-126">Configuring the Application Virtualization Sequencer</span></span>](configuring-the-application-virtualization-sequencer.md)

 

 





