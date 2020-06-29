---
title: Восстановление компьютеров с помощью DaRT 7.0
description: Восстановление компьютеров с помощью DaRT 7.0
author: dansimp
ms.assetid: bcded7ca-237b-4971-ac34-4394b05cbc50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44dd48146155294bd8013b4b5a9bf23ffb3e8316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822769"
---
# <span data-ttu-id="815dc-103">Восстановление компьютеров с помощью DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="815dc-103">Recovering Computers Using DaRT 7.0</span></span>


<span data-ttu-id="815dc-104">Существует два способа восстановления компьютеров с помощью набора средств диагностики и восстановления Microsoft (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="815dc-104">There are two methods available to recover computers using Microsoft Diagnostics and Recovery Toolset (DaRT)7.</span></span> <span data-ttu-id="815dc-105">Вы можете либо запустить образ восстановления DaRT7 локально, либо использовать функцию удаленного подключения, доступную в DaRT7, чтобы восстановить удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="815dc-105">You can either run the DaRT7 recovery image locally or use The Remote Connection feature available in DaRT7 to recover a remote computer.</span></span> <span data-ttu-id="815dc-106">Оба способа подробно описаны в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="815dc-106">Both methods are described in more detail in this section.</span></span>

## <span data-ttu-id="815dc-107">Восстановление локальных компьютеров с помощью средства для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="815dc-107">Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="815dc-108">Чтобы восстановить локальный компьютер с помощью DaRT7, необходимо физически присутствовать на компьютере конечного пользователя, где возникают проблемы, требующие DaRT.</span><span class="sxs-lookup"><span data-stu-id="815dc-108">To recover a local computer by using DaRT7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

<span data-ttu-id="815dc-109">В зависимости от того, как вы развертываете изображение для переноса DaRT, вы можете выбрать один из нескольких различных способов.</span><span class="sxs-lookup"><span data-stu-id="815dc-109">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="815dc-110">Вставьте на проблемный компьютер CD, DVD-диск или USB-накопитель с изображением восстановления с помощью функции "DaRT" и загрузите его с компьютера.</span><span class="sxs-lookup"><span data-stu-id="815dc-110">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="815dc-111">Загрузите элемент DaRT из раздела восстановления на компьютере с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="815dc-111">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="815dc-112">Загрузите элемент DaRT из удаленной секции в сети.</span><span class="sxs-lookup"><span data-stu-id="815dc-112">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="815dc-113">Сведения о преимуществах и недостатках каждого из этих методов можно найти в разделе [Планирование сохранения и развертывания образа восстановления DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="815dc-113">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

<span data-ttu-id="815dc-114">Какой бы метод вы использовали для загрузки в DaRT, необходимо включить загрузочное устройство в BIOS для варианта загрузки или параметров, которые должны быть доступны для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="815dc-114">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="815dc-115">**Примечание**  Настройка BIOS является уникальной в зависимости от типа жесткого диска, сетевых адаптеров и другого оборудования, которое используется в Организации.</span><span class="sxs-lookup"><span data-stu-id="815dc-115">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

[<span data-ttu-id="815dc-116">Восстановление локальных компьютеров с помощью образа для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="815dc-116">How to Recover Local Computers Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)

## <span data-ttu-id="815dc-117">Восстановление удаленных компьютеров с помощью DaRT для восстановления</span><span class="sxs-lookup"><span data-stu-id="815dc-117">Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="815dc-118">Функция "удаленное подключение" в DaRT позволяет ИТ-администратору запускать инструменты DaRT удаленно на компьютере с конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="815dc-118">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="815dc-119">После того как конечные пользователи предоставляют определенную информацию (или специалист службы поддержки, работающий на компьютере пользователя), он может управлять компьютером конечного пользователя и запускать необходимые инструменты DaRT удаленно.</span><span class="sxs-lookup"><span data-stu-id="815dc-119">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="815dc-120">**Важно!**  Два компьютера, на которых установлено удаленное подключение, должны входить в одну и ту же сеть.</span><span class="sxs-lookup"><span data-stu-id="815dc-120">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="815dc-121">Окно **инструментов "Диагностика и восстановление** " содержит параметр, позволяющий удаленно запустить DART на компьютере с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="815dc-121">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="815dc-122">Конечный пользователь откроет инструменты DaRT на компьютере с неполадками и начнет удаленный сеанс, щелкнув **удаленное подключение**.</span><span class="sxs-lookup"><span data-stu-id="815dc-122">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="815dc-123">Функция удаленного подключения на компьютере конечного пользователя создает следующие сведения о подключении: номер билета, порт и список всех доступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="815dc-123">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="815dc-124">Номер и порт билета генерируются случайным образом.</span><span class="sxs-lookup"><span data-stu-id="815dc-124">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="815dc-125">ИТ-администратор или специалист службы поддержки вводит эти данные в **средство удаленного подключения DART** , чтобы установить подключение к службам терминалов для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="815dc-125">The IT administrator or helpdesk agent enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="815dc-126">Установленное подключение служб терминалов позволяет ИТ-администратору удаленно взаимодействовать с инструментами DaRT на компьютере конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="815dc-126">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="815dc-127">Затем компьютер пользователя обрабатывает сведения о подключении, предоставляет доступ к своему экрану и отвечает на инструкции на компьютере администратора.</span><span class="sxs-lookup"><span data-stu-id="815dc-127">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="815dc-128">Восстановление удаленных компьютеров с помощью образа для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="815dc-128">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)

## <span data-ttu-id="815dc-129">Другие ресурсы для восстановления компьютеров с помощью DaRT7</span><span class="sxs-lookup"><span data-stu-id="815dc-129">Other resources for recovering computers using DaRT7</span></span>


[<span data-ttu-id="815dc-130">Операции DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="815dc-130">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





