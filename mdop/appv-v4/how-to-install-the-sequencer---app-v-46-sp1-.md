---
title: Установка секвенсора (App-V 4,6 SP1)
description: Установка секвенсора (App-V 4,6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817272"
---
# <span data-ttu-id="add0a-103">Установка секвенсора (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="add0a-103">How to Install the Sequencer (App-V 4.6 SP1)</span></span>


<span data-ttu-id="add0a-104">Секвенсор Microsoft Application Virtualization (App-V) отслеживает и записывает процесс установки и настройки для приложений, чтобы приложение могло быть запущено как виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="add0a-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="add0a-105">Необходимо установить секвенсор App-V на компьютере с установленной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="add0a-105">You should install the App-V Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="add0a-106">Кроме того, программа Sequencer может быть установлена на компьютере, работающем в виртуальной среде, например виртуальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="add0a-106">Alternatively, you can install the Sequencer on a computer running in a virtual environment, for example, a virtual computer.</span></span> <span data-ttu-id="add0a-107">Этот метод полезен, так как проще поддерживать чистую последовательность, которую можно повторно использовать с минимальной дополнительной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="add0a-107">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span>

<span data-ttu-id="add0a-108">Вы должны иметь учетные данные администратора на компьютере, который вы используете для последовательного применения, и на компьютере не должна выполняться ни одной версии клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="add0a-108">You must have administrative credentials on the computer you are using to sequence the application, and the computer must not be running any version of App-V client.</span></span> <span data-ttu-id="add0a-109">Для создания виртуального приложения с помощью секвенсора App-V требуется несколько операций, поэтому важно установить секвенсор на компьютере, который удовлетворяет [требованиям к оборудованию и программному обеспечению Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="add0a-109">Creating a virtual application by using the App-V Sequencer requires multiple operations, so it is important that you install the Sequencer on a computer that meets or exceeds the [Application Virtualization Sequencer Hardware and Software Requirements](application-virtualization-sequencer-hardware-and-software-requirements.md).</span></span>

**<span data-ttu-id="add0a-110">Примечание.</span><span class="sxs-lookup"><span data-stu-id="add0a-110">Note</span></span>**  
<span data-ttu-id="add0a-111">Выполнение секвенсора App-V в безопасном режиме не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="add0a-111">Running the App-V sequencer in Safe Mode is not supported.</span></span>



**<span data-ttu-id="add0a-112">Установка Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="add0a-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="add0a-113">Скопируйте установочные файлы Microsoft Application Sequencer на компьютер, на котором вы хотите установить его.</span><span class="sxs-lookup"><span data-stu-id="add0a-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer on which you want to install it.</span></span>

2.  <span data-ttu-id="add0a-114">Чтобы запустить мастер установки Microsoft Application Virtualization Sequencer, дважды щелкните **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="add0a-114">To start the Microsoft Application Virtualization Sequencer installation wizard, double-click **Setup.exe**.</span></span> <span data-ttu-id="add0a-115">Если **распространяемый пакет Microsoft Visual C++ с пакетом обновления 1 (x86)** не обнаружен перед установкой, нажмите кнопку **установить** , чтобы установить необходимый предварительный компонент.</span><span class="sxs-lookup"><span data-stu-id="add0a-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, click **Install** to install the required prerequisite.</span></span>

3.  <span data-ttu-id="add0a-116">Чтобы продолжить установку, на странице **приветствия** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="add0a-116">To continue the installation, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="add0a-117">На странице Лицензионное **соглашение** для подтверждения условий лицензионного соглашения выберите **я принимаю условия лицензионного соглашения**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="add0a-117">On the **License Agreement** page, to accept the terms of the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

5.  <span data-ttu-id="add0a-118">На странице **Конечная папка** чтобы сохранить папку установки по умолчанию, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="add0a-118">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="add0a-119">Чтобы указать другую конечную папку, нажмите кнопку **изменить** и укажите папку установки, которая будет использоваться для установки.</span><span class="sxs-lookup"><span data-stu-id="add0a-119">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="add0a-120">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="add0a-120">Click **Next**.</span></span>

6.  <span data-ttu-id="add0a-121">На странице " **виртуальный диск** ", чтобы настроить сервер виртуализации приложений по умолчанию **Q:\\** (по умолчанию) как диск, с которого будут запускаться все приложения из серии, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="add0a-121">On the **Virtual Drive** page, to configure the Application Virtualization default drive **Q:\\** (default) as the drive that all sequenced applications will run from, click **Next**.</span></span> <span data-ttu-id="add0a-122">Если вы хотите указать другую букву диска, выберите нужную букву диска в списке и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="add0a-122">If you want to specify a different drive letter, use the list and select the drive letter that you want to use by selecting the appropriate drive letter, and then click **Next**.</span></span>

    **<span data-ttu-id="add0a-123">Важно.</span><span class="sxs-lookup"><span data-stu-id="add0a-123">Important</span></span>**  
    <span data-ttu-id="add0a-124">Буква диска Application Virtualization, указанная на этом этапе, — это буква диска, на которой будут запускаться виртуальные приложения на конечных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="add0a-124">The Application Virtualization drive letter specified with this step is the drive letter that virtual applications will be run from on target computers.</span></span> <span data-ttu-id="add0a-125">Указанная буква диска должна быть доступна, и в настоящее время не используется на компьютерах с клиентом App-V.</span><span class="sxs-lookup"><span data-stu-id="add0a-125">The drive letter specified must be available, and not currently in use on the computers running the App-V client.</span></span> <span data-ttu-id="add0a-126">Если указанный диск уже используется, виртуальное приложение на целевом компьютере завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="add0a-126">If the specified drive is already in use, the virtual application fails on the target computer.</span></span>



7.  <span data-ttu-id="add0a-127">Чтобы начать установку, на странице **готовность к установке программы** нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="add0a-127">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

8.  <span data-ttu-id="add0a-128">На странице **завершения работы мастера InstallShield** нажмите кнопку **Готово**, чтобы закрыть мастер установки и открыть секвенсор App-V.</span><span class="sxs-lookup"><span data-stu-id="add0a-128">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the App-V Sequencer, click **Finish**.</span></span> <span data-ttu-id="add0a-129">Чтобы закрыть мастер установки, не открывая секвенсор, снимите флажок **запустить программу**и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="add0a-129">To close the installation wizard without opening the Sequencer, clear **Launch the program**, and then click **Finish**.</span></span>

    **<span data-ttu-id="add0a-130">Примечание.</span><span class="sxs-lookup"><span data-stu-id="add0a-130">Note</span></span>**  
    <span data-ttu-id="add0a-131">Если вы установили секвенсор App-V на компьютере с виртуальной средой, например виртуальной машине, вы должны сделать снимок.</span><span class="sxs-lookup"><span data-stu-id="add0a-131">If you installed the App-V Sequencer on a computer running a virtual environment, for example a virtual machine, you must now take a snapshot.</span></span> <span data-ttu-id="add0a-132">После того как вы перейдете к приложению, вы можете вернуться к этому изображению, чтобы можно было выполнить последовательное выполнение следующего приложения.</span><span class="sxs-lookup"><span data-stu-id="add0a-132">After you sequence an application, you can revert to this image, so you can sequence the next application.</span></span>



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## <span data-ttu-id="add0a-133">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="add0a-133">Related topics</span></span>


[<span data-ttu-id="add0a-134">Настройка Application Virtualization Sequencer (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="add0a-134">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)









