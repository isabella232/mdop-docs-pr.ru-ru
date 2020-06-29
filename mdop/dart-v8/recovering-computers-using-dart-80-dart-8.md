---
title: Восстановление компьютеров с помощью DaRT 8.0
description: Восстановление компьютеров с помощью DaRT 8.0
author: dansimp
ms.assetid: 0caeb7d9-c1e6-4f32-bc27-157b91630989
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39bab02488252b53deb971d35bc6872c0a2df73b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824869"
---
# <span data-ttu-id="b533d-103">Восстановление компьютеров с помощью DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="b533d-103">Recovering Computers Using DaRT 8.0</span></span>


<span data-ttu-id="b533d-104">После развертывания набора средств диагностики и восстановления Microsoft (DaRT) 8,0 для восстановления компьютеров вы можете использовать DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="b533d-104">After deploying the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image, you can use DaRT 8.0 to recover computers.</span></span> <span data-ttu-id="b533d-105">Данные в этом разделе описывают задачи восстановления, которые можно выполнить.</span><span class="sxs-lookup"><span data-stu-id="b533d-105">The information in this section describes the recovery tasks that you can perform.</span></span>

<span data-ttu-id="b533d-106">В зависимости от того, как вы развертываете изображение для переноса DaRT, вы можете выбрать один из нескольких различных способов.</span><span class="sxs-lookup"><span data-stu-id="b533d-106">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="b533d-107">Вставьте на проблемный компьютер CD, DVD-диск или USB-накопитель с изображением восстановления с помощью функции "DaRT" и загрузите его с компьютера.</span><span class="sxs-lookup"><span data-stu-id="b533d-107">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="b533d-108">Загрузите элемент DaRT из раздела восстановления на компьютере с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b533d-108">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="b533d-109">Загрузите элемент DaRT из удаленной секции в сети.</span><span class="sxs-lookup"><span data-stu-id="b533d-109">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="b533d-110">Сведения о преимуществах и недостатках каждого из этих методов можно найти в разделе [Планирование сохранения и развертывания образа восстановления DaRT 8,0](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="b533d-110">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 8.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="b533d-111">Какой бы метод вы использовали для загрузки в DaRT, необходимо включить загрузочное устройство в BIOS для варианта загрузки или параметров, которые должны быть доступны для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b533d-111">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="b533d-112">**Примечание**  Настройка BIOS является уникальной в зависимости от типа жесткого диска, сетевых адаптеров и другого оборудования, которое используется в Организации.</span><span class="sxs-lookup"><span data-stu-id="b533d-112">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

## <span data-ttu-id="b533d-113">Восстановление локального компьютера с помощью средства для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="b533d-113">Recover a local computer by using the DaRT recovery image</span></span>


<span data-ttu-id="b533d-114">Для восстановления локального компьютера с помощью DaRT вы должны быть физически представлены на компьютере конечного пользователя, на котором возникают проблемы, требующие DaRT.</span><span class="sxs-lookup"><span data-stu-id="b533d-114">To recover a local computer by using DaRT, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

[<span data-ttu-id="b533d-115">Восстановление локальных компьютеров с помощью образа для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="b533d-115">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md)

## <span data-ttu-id="b533d-116">Восстановление удаленного компьютера с помощью средства для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="b533d-116">Recover a remote computer by using the DaRT recovery image</span></span>


<span data-ttu-id="b533d-117">Функция "удаленное подключение" в DaRT позволяет ИТ-администратору запускать инструменты DaRT удаленно на компьютере с конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="b533d-117">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="b533d-118">После того как конечным пользователем предоставлены определенные сведения (или специалист службы технической поддержки, работающий на компьютере пользователя), ИТ-администратор или сотрудник Отдела помощи могут управлять компьютером конечного пользователя и запускать необходимые инструменты DaRT удаленно.</span><span class="sxs-lookup"><span data-stu-id="b533d-118">After certain information is provided by the end user (or by a help desk professional working on the end-user computer), the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="b533d-119">**Важно!**  Два компьютера, на которых установлено удаленное подключение, должны входить в одну и ту же сеть.</span><span class="sxs-lookup"><span data-stu-id="b533d-119">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="b533d-120">Окно **инструментов "Диагностика и восстановление** " содержит параметр, позволяющий удаленно запустить DART на компьютере с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="b533d-120">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="b533d-121">Конечный пользователь откроет инструменты DaRT на компьютере с неполадками и начнет удаленный сеанс, щелкнув **удаленное подключение**.</span><span class="sxs-lookup"><span data-stu-id="b533d-121">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="b533d-122">Функция удаленного подключения на компьютере конечного пользователя создает следующие сведения о подключении: номер билета, порт и список всех доступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b533d-122">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="b533d-123">Номер и порт билета генерируются случайным образом.</span><span class="sxs-lookup"><span data-stu-id="b533d-123">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="b533d-124">ИТ-администратор или сотрудник службы поддержки вводит эти данные в **средство удаленного подключения DART** , чтобы установить подключение к службам терминалов для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b533d-124">The IT administrator or help desk worker enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="b533d-125">Установленное подключение служб терминалов позволяет ИТ-администратору удаленно взаимодействовать с инструментами DaRT на компьютере конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b533d-125">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="b533d-126">Затем компьютер пользователя обрабатывает сведения о подключении, предоставляет доступ к своему экрану и отвечает на инструкции на компьютере администратора.</span><span class="sxs-lookup"><span data-stu-id="b533d-126">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="b533d-127">Восстановление удаленных компьютеров с помощью образа для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="b533d-127">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md)

## <span data-ttu-id="b533d-128">Другие ресурсы для восстановления компьютеров с помощью DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="b533d-128">Other resources for recovering computers using DaRT 8.0</span></span>


[<span data-ttu-id="b533d-129">Операции DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="b533d-129">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





