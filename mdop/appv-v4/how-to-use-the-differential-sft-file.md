---
title: Использование разностного SFT-файла
description: Использование разностного SFT-файла
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816389"
---
# <span data-ttu-id="7324f-103">Использование разностного SFT-файла</span><span class="sxs-lookup"><span data-stu-id="7324f-103">How to Use the Differential SFT File</span></span>


<span data-ttu-id="7324f-104">При виртуализации приложения секвенсор Microsoft Application Virtualization (App-V) создает файлы SFT (SFT), в которых хранятся все содержимое файлов виртуального приложения и сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="7324f-104">When sequencing an application, the Microsoft Application Virtualization (App-V) Sequencer creates SFT files (.sft) to store all of the virtual application’s files content and configuration information.</span></span> <span data-ttu-id="7324f-105">В версии 4.5 App-V появился Разностный SFT-файл (dsft).</span><span class="sxs-lookup"><span data-stu-id="7324f-105">In version4.5 of App-V, the Differential SFT (.dsft) file has been introduced.</span></span> <span data-ttu-id="7324f-106">После использования программы Sequencer для создания обновления существующего пакета вы можете создать этот файл, чтобы сохранить только различия между исходным пакетом приложения и новой версией.</span><span class="sxs-lookup"><span data-stu-id="7324f-106">After using the Sequencer to create an upgrade for an existing package, you can choose to generate this file to store only the differences between the original sequenced application package and the new version.</span></span> <span data-ttu-id="7324f-107">Таким образом, этот файл значительно меньше полного SFT-файла для новой версии приложения и уменьшает влияние отправки обновлений пакетов по сетевым подключениям с низкой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="7324f-107">It is therefore much smaller than the full SFT file would be for the new version of the application and reduces the impact of sending package updates over low-bandwidth network connections.</span></span> <span data-ttu-id="7324f-108">Тем не менее, его использование поддерживается только в определенных ситуациях, использующих определенные ограничения.</span><span class="sxs-lookup"><span data-stu-id="7324f-108">However, its use is supported only in certain restricted situations.</span></span> <span data-ttu-id="7324f-109">Эта функция предназначена специально для тех случаев, когда вы используете систему электронной рассылки программного обеспечения (ESD) для управления группой пользователей с помощью локального файлового сервера в соединении с низким пропускной способностью и не используете потоковые серверы App-V.</span><span class="sxs-lookup"><span data-stu-id="7324f-109">This feature was intended to be used specifically where you are using an electronic software distribution (ESD) system to manage a group of users with a local file server over a low-bandwidth connection and you are not using App-V streaming servers.</span></span>

<span data-ttu-id="7324f-110">Если вы используете конфигурацию Manager2007 для управления пользователями, вам не нужно использовать Разностный SFT-файл, так как Configuration Manager поддерживает развертывания с низким пропускной способностью, которые уже встроены.</span><span class="sxs-lookup"><span data-stu-id="7324f-110">You do not need to use the Differential SFT file if you are using Configuration Manager2007 to manage the users, because Configuration Manager has support for low-bandwidth deployments already built in.</span></span> <span data-ttu-id="7324f-111">Это также не требуется, если вы используете сервер Application Virtualization (App-V) или Streaming Servers с активной модернизацией, так как клиент извлекает только различия между старыми и новыми версиями пакетов.</span><span class="sxs-lookup"><span data-stu-id="7324f-111">It is also not required if you are using Application Virtualization (App-V) Management or Streaming Servers with Active Upgrade because the client will retrieve only the differences between the old and new package versions.</span></span>

<span data-ttu-id="7324f-112">В приведенной ниже процедуре показано, как использовать mkdiffpkg.exe, включенный в установку Sequencer, для создания разностного SFT, после завершения обновления виртуального пакета приложения, а также для развертывания разностного SFT файла.</span><span class="sxs-lookup"><span data-stu-id="7324f-112">The following procedure shows how to use the mkdiffpkg.exe that is included in the Sequencer installation to create the Differential SFT file, after completing the upgrade of the virtual application package, and to deploy the Differential SFT file.</span></span> <span data-ttu-id="7324f-113">Выполнение этой процедуры гарантирует, что если пакет будет выгружен с клиентского компьютера, то при следующем запуске приложения клиент вернется к URL-адресу переопределения, который задается потоком для полного пакета v2. SFT из локального общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="7324f-113">Completing this procedure helps ensure that if the package is somehow unloaded from the client computer, the next time the user tries to run the application, the client will fall back to the override URL, which is set to stream the full package V2.sft from the local file share.</span></span> <span data-ttu-id="7324f-114">Это позволит избежать сбоев для пользователя при запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="7324f-114">This will avoid any failure for the user when starting the application.</span></span> <span data-ttu-id="7324f-115">Если весь клиент поврежден или удален, рекомендуется настроить систему ESD на развертывание полной версии обновленного пакета (для версии v2. SFT) для клиента.</span><span class="sxs-lookup"><span data-stu-id="7324f-115">If the entire client becomes corrupted or is uninstalled, it is recommended that the ESD system be configured to deploy the full version of the upgraded package, V2.sft, to the client.</span></span>

<span data-ttu-id="7324f-116">Дополнительные сведения об обновлении пакета можно найти в разделе "как обновить существующее виртуальное приложение" в руководстве по эксплуатации App-V 4.5 на странице</span><span class="sxs-lookup"><span data-stu-id="7324f-116">For more information about upgrading a package, see “How to Upgrade an Existing Virtual Application” in the App-V4.5 Operations Guide at</span></span> <https://go.microsoft.com/fwlink/?LinkId=133129>

<span data-ttu-id="7324f-117">**Примечание**  В качестве предварительной версии для всех компьютеров пользователей, для которых требуется использовать ESD, должен быть полностью загружен файл v1. SFT в локальном кэше, а на всех компьютерах должна быть включена потоковая передача файлов.</span><span class="sxs-lookup"><span data-stu-id="7324f-117">**Note** As a prerequisite, all user computers being targeted by the ESD must have the V1.sft file fully loaded into their local cache, and file streaming must be enabled on all computers.</span></span>

 

**<span data-ttu-id="7324f-118">Использование разностного SFT — файла</span><span class="sxs-lookup"><span data-stu-id="7324f-118">To use the Differential SFT file</span></span>**

1.  <span data-ttu-id="7324f-119">Войдите на компьютер секвенсор, используя учетную запись с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="7324f-119">Log on to the Sequencer computer by using an account with administrator rights.</span></span> <span data-ttu-id="7324f-120">Откройте исходный пакет (v1) для обновления в секвенсоре, а затем обновите пакет до новой версии (v2) и сохраните его как новый v2. SFT.</span><span class="sxs-lookup"><span data-stu-id="7324f-120">Open the original package (V1) for upgrade in the Sequencer, and then upgrade the package to the new version (V2) and save it as a new V2.sft.</span></span>

2.  <span data-ttu-id="7324f-121">Откройте окно команд в установочной папке App-V 4.5 и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7324f-121">Open a command window in the App-V4.5 Sequencer installation folder, and run the following command:</span></span>

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  <span data-ttu-id="7324f-122">С помощью системы ESD или другого процесса копирования файлов скопируйте полный файл содержимого пакета версии 2 (SFT) в локальную общую файловую систему, доступную для компьютеров пользователей по надежному подключенному сетевому подключению.</span><span class="sxs-lookup"><span data-stu-id="7324f-122">Using the ESD system or other file copy process, copy the full V2 package content file, V2.sft, to a local file share that is accessible to the user computers on a well-connected network connection.</span></span>

4.  <span data-ttu-id="7324f-123">Используя систему ESD, разместите на каждом компьютере пользователя копию SFT-файла версии 2. dsft.</span><span class="sxs-lookup"><span data-stu-id="7324f-123">Using the ESD system, place a copy of the Differential SFT file, V2.dsft, on each user computer.</span></span>

5.  <span data-ttu-id="7324f-124">Чтобы импортировать файл V2. dsft, выполните следующую команду SFTMIME на каждом компьютере пользователя:</span><span class="sxs-lookup"><span data-stu-id="7324f-124">To import the V2.dsft file, run the following SFTMIME command on each user computer:</span></span>

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  <span data-ttu-id="7324f-125">Выполните следующую команду SFTMIME для каждого компьютера пользователя, чтобы настроить URL-адрес для переопределения файла v2. SFT:</span><span class="sxs-lookup"><span data-stu-id="7324f-125">Run the following SFTMIME command on each user computer to set the override URL to point to the V2.sft file:</span></span>

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**<span data-ttu-id="7324f-126">Примечание.</span><span class="sxs-lookup"><span data-stu-id="7324f-126">Note</span></span>**  
-   <span data-ttu-id="7324f-127">Разностные SFT файлы должны применяться к клиентам в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="7324f-127">Differential SFT files must be applied to clients in the correct order.</span></span> <span data-ttu-id="7324f-128">Например, параметр v2. dsft необходимо применить к приложению v1 перед применением v3. dsft.</span><span class="sxs-lookup"><span data-stu-id="7324f-128">For example, V2.dsft must be applied to a V1 application before V3.dsft is applied.</span></span>

-   <span data-ttu-id="7324f-129">Возможность **создания пакета установщика Microsoft Windows (MSI)** в секвенсоре не может использоваться с РАЗНОСТным SFT-файлом.</span><span class="sxs-lookup"><span data-stu-id="7324f-129">The **Generate Microsoft Windows Installer (MSI) Package** capability in the Sequencer cannot be used with the Differential SFT file.</span></span>

 

## <span data-ttu-id="7324f-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7324f-130">Related topics</span></span>


[<span data-ttu-id="7324f-131">Создание и обновление виртуальных приложений с помощью секвенсора App-V</span><span class="sxs-lookup"><span data-stu-id="7324f-131">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





