---
title: Установка программы Application Virtualization Sequencer
description: Установка программы Application Virtualization Sequencer
author: dansimp
ms.assetid: 89cdf60d-18b0-4204-aa9f-b402610f8f0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a6fe03f2149504b6c34c70b2b82ce2ba0b55ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817309"
---
# <span data-ttu-id="fca02-103">Установка программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="fca02-103">How to Install the Application Virtualization Sequencer</span></span>


<span data-ttu-id="fca02-104">Microsoft Application Virtualization Sequencer отслеживает и записывает процесс установки и настройки для приложений, чтобы приложение могло быть запущено как виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="fca02-104">The Microsoft Application Virtualization Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="fca02-105">Секвенсор необходимо установить на компьютере с установленной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="fca02-105">You should install the Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="fca02-106">Кроме того, программа Sequencer может быть установлена на компьютере под управлением виртуальной среды (например, Microsoft Virtual PC).</span><span class="sxs-lookup"><span data-stu-id="fca02-106">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="fca02-107">Этот метод полезен, поскольку проще поддерживать чистую последовательность, которую можно повторно использовать с минимальной дополнительной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="fca02-107">This method is useful because it is easier to maintain a clean sequencing environment that can be reused with minimal additional configuration.</span></span>

<span data-ttu-id="fca02-108">У вас должны быть права администратора на компьютере, который вы используете для упорядочения приложения, и на компьютере не должна выполняться ни одна из версий клиента Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="fca02-108">You must have administrative rights on the computer you are using to sequence the application and the computer must not be running any version of the Application Virtualization (App-V) client.</span></span> <span data-ttu-id="fca02-109">Создание виртуального приложения с помощью секвенсора занимает очень много ресурсов, поэтому важно установить секвенсор на компьютер, удовлетворяющий рекомендуемому или превышающему рекомендуемые требования.</span><span class="sxs-lookup"><span data-stu-id="fca02-109">Creating a virtual application by using the Sequencer is very resource intensive, so it is important that you install the Sequencer on a computer that meets or exceeds the recommended requirements.</span></span> <span data-ttu-id="fca02-110">Выполнение секвенсора App-V в безопасном режиме не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fca02-110">Running the App-V sequencer in Safe Mode is not supported.</span></span> <span data-ttu-id="fca02-111">Дополнительные сведения о требованиях к системе описаны в разделе [требования к системе Application Virtualization](application-virtualization-system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fca02-111">For more information about the system requirements, see [Application Virtualization System Requirements](application-virtualization-system-requirements.md).</span></span>

<span data-ttu-id="fca02-112">**Важно!**  После упорядочения приложения для правильной последовательности нового приложения необходимо переустановить операционную систему и секвенсор на компьютере, который вы используете для последовательного приложения.</span><span class="sxs-lookup"><span data-stu-id="fca02-112">**Important** After you have sequenced an application, before you can properly sequence a new application you must reinstall the operating system and the Sequencer on the computer you are using to sequence applications.</span></span>

 

**<span data-ttu-id="fca02-113">Установка Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="fca02-113">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="fca02-114">Скопируйте установочные файлы Microsoft Application Sequencer на компьютер, на котором вы хотите установить его.</span><span class="sxs-lookup"><span data-stu-id="fca02-114">Copy the Microsoft Application Virtualization Sequencer installation files to the computer that you want to install it on.</span></span>

2.  <span data-ttu-id="fca02-115">Чтобы запустить мастер установки Microsoft Application Virtualization Sequencer, выберите **setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="fca02-115">To start the Microsoft Application Virtualization Sequencer installation wizard, select **setup.exe**.</span></span> <span data-ttu-id="fca02-116">Если **распространяемый пакет Microsoft Visual C++ с пакетом обновления 1 (x86)** не обнаружен перед установкой, **setup.exe** будет устанавливать его.</span><span class="sxs-lookup"><span data-stu-id="fca02-116">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, **setup.exe** will install it.</span></span>

3.  <span data-ttu-id="fca02-117">На странице **приветствия** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fca02-117">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="fca02-118">На странице Лицензионное **соглашение** для подтверждения условий лицензионного соглашения установите флажок **я принимаю условия лицензионного**соглашения.</span><span class="sxs-lookup"><span data-stu-id="fca02-118">On the **License Agreement** page, to accept the terms of the license agreement, select **I accept the terms in the license agreement**.</span></span> <span data-ttu-id="fca02-119">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fca02-119">Click **Next**.</span></span>

5.  <span data-ttu-id="fca02-120">На странице **Конечная папка** чтобы сохранить папку установки по умолчанию, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fca02-120">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="fca02-121">Чтобы указать другую конечную папку, нажмите кнопку **изменить** и укажите папку установки, которая будет использоваться для установки.</span><span class="sxs-lookup"><span data-stu-id="fca02-121">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="fca02-122">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fca02-122">Click **Next**.</span></span>

6.  <span data-ttu-id="fca02-123">Чтобы начать установку, на странице **готовность к установке программы** нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="fca02-123">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="fca02-124">На странице **завершения работы мастера InstallShield** нажмите кнопку **Готово**, чтобы закрыть мастер установки и открыть секвенсор.</span><span class="sxs-lookup"><span data-stu-id="fca02-124">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the Sequencer, click **Finish**.</span></span> <span data-ttu-id="fca02-125">Чтобы закрыть мастер установки, не открывая секвенсор, снимите флажок **запустить программу** и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="fca02-125">To close the installation wizard without opening the Sequencer, deselect **Launch the program** and click **Finish**.</span></span>

## <span data-ttu-id="fca02-126">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="fca02-126">Related topics</span></span>


[<span data-ttu-id="fca02-127">Обновление программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="fca02-127">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

[<span data-ttu-id="fca02-128">Требования при развертывании Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="fca02-128">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

 

 





