---
title: Практические рекомендации по работе с программой Application Virtualization Sequencer
description: Практические рекомендации по работе с программой Application Virtualization Sequencer
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821999"
---
# <span data-ttu-id="9c646-103">Практические рекомендации по работе с программой Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="9c646-103">Best Practices for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="9c646-104">В этом разделе приводятся рекомендации по запуску секвенсора Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="9c646-104">This topic provides best practices for running the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="9c646-105">Ознакомьтесь со следующими рекомендациями по планированию и использованию секвенсора в среде.</span><span class="sxs-lookup"><span data-stu-id="9c646-105">Review and consider the following recommendations when planning and using the Sequencer in your environment.</span></span>

## <span data-ttu-id="9c646-106">Упорядочение рекомендаций по конфигурации компьютера</span><span class="sxs-lookup"><span data-stu-id="9c646-106">Sequencing Computer Configuration Best Practices</span></span>


<span data-ttu-id="9c646-107">При настройке компьютера с помощью секвенсора App-V следует учитывать следующие рекомендации:</span><span class="sxs-lookup"><span data-stu-id="9c646-107">The following best practices should be considered when configuring the computer running the App-V Sequencer:</span></span>

-   **<span data-ttu-id="9c646-108">Последовательность на компьютере с аналогичной конфигурацией, на которой работает более ранняя версия операционной системы, чем целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="9c646-108">Sequence on a computer that has a similar configuration and that is running an earlier version of the operating system than the target computers.</span></span>**

    <span data-ttu-id="9c646-109">Убедитесь, что на компьютере, на котором запущен секвенсор, установлена более ранняя версия операционной системы, чем целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="9c646-109">Ensure that the computer that is running the Sequencer is running an earlier version of the operating system than the target computers.</span></span> <span data-ttu-id="9c646-110">Сюда входят пакеты обновления и версии обновлений.</span><span class="sxs-lookup"><span data-stu-id="9c646-110">This includes the service pack and update versions.</span></span> <span data-ttu-id="9c646-111">Например, если целевые компьютеры работают под управлением WindowsVista и WindowsXP, следует поочередно запускать приложения на компьютере, на котором запущено приложение WindowsXP.</span><span class="sxs-lookup"><span data-stu-id="9c646-111">For example, if the target computers are running WindowsVista and WindowsXP, you should sequence applications on a computer that is running WindowsXP.</span></span> <span data-ttu-id="9c646-112">Возможность последовательности в одной операционной системе и запуск виртуализированного приложения в другой операционной системе не гарантируется и зависит от конкретного приложения и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9c646-112">The ability to sequence on one operating system and run the virtualized application on a different operating system is not guaranteed, and depends on the particular application and operating system.</span></span> <span data-ttu-id="9c646-113">Если вы столкнулись с проблемами, вам может потребоваться выполнить последовательность в той же среде операционной системы, в которой работает клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="9c646-113">If you encounter issues, you may be required to sequence on the same operating system environment as the one on which the App-V client is running.</span></span>

-   **<span data-ttu-id="9c646-114">Настройте компьютер под управлением секвенсора с несколькими разделами.</span><span class="sxs-lookup"><span data-stu-id="9c646-114">Configure the computer running the Sequencer with multiple partitions.</span></span>**

    <span data-ttu-id="9c646-115">На компьютере с секвенсором должны быть установлены по крайней мере два основных раздела.</span><span class="sxs-lookup"><span data-stu-id="9c646-115">You should configure the computer running the Sequencer with at least two primary partitions.</span></span> <span data-ttu-id="9c646-116">Первый раздел (**C:**) должен содержать операционную систему, и его следует отформатировать с помощью файловой системы NTFS.</span><span class="sxs-lookup"><span data-stu-id="9c646-116">The first partition (**C:**) should contain the operating system, and it should be formatted using the NTFS file system.</span></span> <span data-ttu-id="9c646-117">Второй раздел (**Q:**) используется в качестве конечного пути для установки виртуального приложения, и его также следует отформатировать с помощью файловой системы NTFS.</span><span class="sxs-lookup"><span data-stu-id="9c646-117">The second partition (**Q:**) is used as the destination path for the virtual application installation and should also be formatted using the NTFS file system.</span></span>

-   **<span data-ttu-id="9c646-118">Настройте временный каталог на достаточное свободное место на диске.</span><span class="sxs-lookup"><span data-stu-id="9c646-118">Configure the temp directory with enough free disk space.</span></span>**

    <span data-ttu-id="9c646-119">Для хранения временных файлов программа Sequencer использует каталог **% tmp%** или **% TEMP%** и каталог **вычерчивания** .</span><span class="sxs-lookup"><span data-stu-id="9c646-119">The Sequencer uses the **%TMP%** or **%TEMP%** directory and the **Scratch** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="9c646-120">Вы должны настроить эти каталоги на компьютере, на котором запущены программы Sequencer, и получить доступ к предполагаемым требованиям к установке приложения.</span><span class="sxs-lookup"><span data-stu-id="9c646-120">You should configure these directories on the computer running the Sequencer with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="9c646-121">Вы можете проверить расположение **вспомогательной** папки, открыв консоль секвенсор и выбрав **инструменты**, **Параметры**, а затем вкладку **пути** . Настройка временных папок и **вспомогательного** каталога для разных разделов жесткого диска может повысить производительность при выполнении последовательности.</span><span class="sxs-lookup"><span data-stu-id="9c646-121">You can verify the location of the **Scratch** directory by opening the Sequencer console and selecting **Tools**, **Options**, and then selecting the **Paths** tab. Configuring the temp directories and the **Scratch** directory on different hard drive partitions can improve performance during sequencing.</span></span>

-   **<span data-ttu-id="9c646-122">Последовательное приложение с помощью Microsoft VirtualPC.</span><span class="sxs-lookup"><span data-stu-id="9c646-122">Sequence applications by using Microsoft VirtualPC.</span></span>**

    <span data-ttu-id="9c646-123">Вы будете чаще последовательной последовательности приложений.</span><span class="sxs-lookup"><span data-stu-id="9c646-123">You will sequence most applications more than once.</span></span> <span data-ttu-id="9c646-124">Для упрощения этой работы следует предусмотреть последовательность на компьютере, работающем в виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="9c646-124">To help facilitate this, you should consider sequencing on a computer running in a virtual environment.</span></span> <span data-ttu-id="9c646-125">Это позволит вам последовательное выполнение приложения и вернуться в исходное состояние с минимальной переконфигурацией на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="9c646-125">This will allow you to sequence an application and revert to a clean state, with minimal reconfiguration, on the computer that is running the Sequencer.</span></span>

    <span data-ttu-id="9c646-126">Если вы используете Microsoft Hyper-V в своей среде, программа Sequencer App-v будет запускаться при запуске виртуального компьютера Hyper-V:</span><span class="sxs-lookup"><span data-stu-id="9c646-126">If you are running Microsoft Hyper-V in your environment the App-V sequencer will run when the Hyper-V virtual computer it is running on is:</span></span>

    -   <span data-ttu-id="9c646-127">приостанавливается и возобновляется.</span><span class="sxs-lookup"><span data-stu-id="9c646-127">paused and resumed.</span></span>

    -   <span data-ttu-id="9c646-128">состояние сохранено и восстановлено.</span><span class="sxs-lookup"><span data-stu-id="9c646-128">has its state saved and restored.</span></span>

    -   <span data-ttu-id="9c646-129">сохранено как моментальный снимок и восстанавливается.</span><span class="sxs-lookup"><span data-stu-id="9c646-129">saved as a snapshot and is restored.</span></span>

    -   <span data-ttu-id="9c646-130">перенесены на разные аппаратные средства в рамках динамической миграции.</span><span class="sxs-lookup"><span data-stu-id="9c646-130">migrated to different hardware as part of a live migration.</span></span>

-   **<span data-ttu-id="9c646-131">Перед выполнением последовательности нового приложения закройте другие запущенные программы.</span><span class="sxs-lookup"><span data-stu-id="9c646-131">Before you sequence a new application, shut down other running programs.</span></span>**

    <span data-ttu-id="9c646-132">Процессы и запланированные задачи, которые обычно выполняются на компьютере виртуализации, могут замедлить процесс упорядочения и привести к сбору ненужных данных во время последовательности.</span><span class="sxs-lookup"><span data-stu-id="9c646-132">Processes and scheduled tasks that normally run on the sequencing computer can slow down the sequencing process and cause irrelevant data to be gathered during sequencing.</span></span> <span data-ttu-id="9c646-133">Все ненужные приложения и программы должны быть закрыты до начала последовательности.</span><span class="sxs-lookup"><span data-stu-id="9c646-133">All unnecessary applications and programs should be shut down before you begin sequencing.</span></span>

-   **<span data-ttu-id="9c646-134">Последовательность на компьютере, на котором запущены службы терминалов</span><span class="sxs-lookup"><span data-stu-id="9c646-134">Sequence on a computer that is running Terminal Services</span></span>**

    <span data-ttu-id="9c646-135">Перед установкой секвенсора не настраивайте режим установки на компьютере, на котором запущены службы терминалов.</span><span class="sxs-lookup"><span data-stu-id="9c646-135">You should not configure the install mode on a computer that is running Terminal Services before you install the sequencer.</span></span>

## <span data-ttu-id="9c646-136">Рекомендации по упорядочиванию</span><span class="sxs-lookup"><span data-stu-id="9c646-136">Sequencing Best Practices</span></span>


<span data-ttu-id="9c646-137">Ниже перечислены рекомендации, которые следует учитывать при упорядочении нового приложения.</span><span class="sxs-lookup"><span data-stu-id="9c646-137">The following best practices should be considered when sequencing a new application:</span></span>

-   

    <span data-ttu-id="9c646-138">**Примечание**  Если вы используете App-V 4,6 с пакетом обновления 1 (SP1), вам не нужно последовательностей в каталог, следующий за соглашением об именовании 8,3.</span><span class="sxs-lookup"><span data-stu-id="9c646-138">**Note** If you are running App-V 4.6 SP1 you do not need to sequence to a directory that follows the 8.3 naming convention.</span></span>

     

-   **<span data-ttu-id="9c646-139">Порядковый номер в уникальный каталог, следующий за соглашением об именовании 8,3.</span><span class="sxs-lookup"><span data-stu-id="9c646-139">Sequence to a unique directory that follows the 8.3 naming convention.</span></span>**

    <span data-ttu-id="9c646-140">Для всех приложений следует последовательно указать каталог, следующий за соглашением об именовании 8,3.</span><span class="sxs-lookup"><span data-stu-id="9c646-140">You should sequence all applications to a directory that follows the 8.3 naming convention.</span></span> <span data-ttu-id="9c646-141">Указанное имя каталога не может содержать более восьми символов, за которым следует расширение имени файла в три символа (например, Q:\\MYAPP.). \*\* ABC\*\*.</span><span class="sxs-lookup"><span data-stu-id="9c646-141">The specified directory name cannot contain more than eight characters, followed by a three-character file name extension—for example, **Q:\\MYAPP.ABC**.</span></span>

-   **<span data-ttu-id="9c646-142">Последовательности в конечную папку в корне диска, а не в подкаталог.</span><span class="sxs-lookup"><span data-stu-id="9c646-142">Sequence to a destination folder on the root of the drive, not to a subdirectory.</span></span>**

    <span data-ttu-id="9c646-143">Если набор приложений состоит из нескольких частей, установите каждое приложение в подкаталог основного каталога.</span><span class="sxs-lookup"><span data-stu-id="9c646-143">If the application suite has multiple parts, install each application to a subdirectory of the main directory.</span></span> <span data-ttu-id="9c646-144">Например, если пакет включает приложение вместе с клиентом, используйте **Q:\\AppSuite** в качестве основного каталога и поочередное применение основного приложения к **Q:\\AppSuite\\Main**и последовательное использование клиента с **Q:\\AppSuite\\Client**.</span><span class="sxs-lookup"><span data-stu-id="9c646-144">For example, if a package contains an application along with a client, use **Q:\\AppSuite** as the main directory and sequence the main application to **Q:\\AppSuite\\Main**, and sequence the client to **Q:\\AppSuite\\Client**.</span></span>

-   **<span data-ttu-id="9c646-145">Настройте и протестируйте приложение на этапе установки.</span><span class="sxs-lookup"><span data-stu-id="9c646-145">Configure and test the application during the installation phase.</span></span>**

    <span data-ttu-id="9c646-146">Для завершения установки приложения часто требуется выполнить несколько действий вручную, которые не являются частью процесса установки приложения.</span><span class="sxs-lookup"><span data-stu-id="9c646-146">Completing the installation of an application often requires performing several manual steps that are not part of the application installation process.</span></span> <span data-ttu-id="9c646-147">Эти действия могут включать в себя настройку подключения к базе данных или копирование обновленных файлов.</span><span class="sxs-lookup"><span data-stu-id="9c646-147">These steps can involve configuring a connection to a database or copying updated files.</span></span> <span data-ttu-id="9c646-148">Вы должны выполнить эти настройки на этапе установки, а затем запустить приложение, чтобы убедиться, что он работает.</span><span class="sxs-lookup"><span data-stu-id="9c646-148">You should perform these configurations during the installation phase and then run the application to make sure it works.</span></span>

-   **<span data-ttu-id="9c646-149">Запустите приложение, если это необходимо, несколько минут, пока приложение не будет стабильным.</span><span class="sxs-lookup"><span data-stu-id="9c646-149">Run the application, multiple times if necessary, until the program is stable.</span></span>**

    <span data-ttu-id="9c646-150">Во время установки приложение должно быть запущено многократно, чтобы убедиться в том, что все связанные настройки регистрации и диалогового окна завершены.</span><span class="sxs-lookup"><span data-stu-id="9c646-150">You should run the application multiple times during the installation to ensure all associated registration and dialog box configurations have been completed.</span></span> <span data-ttu-id="9c646-151">Одновременное открытие приложения во время установки гарантирует, что в **основной блок функций**будут загружены только необходимые функции приложения.</span><span class="sxs-lookup"><span data-stu-id="9c646-151">Opening the application multiple times during installation will ensure that only the relevant application features are loaded into the **primary feature block**.</span></span>

-   **<span data-ttu-id="9c646-152">Отключите все функции автоматического обновления, связанные с приложением.</span><span class="sxs-lookup"><span data-stu-id="9c646-152">Disable all automatic update features associated with the application.</span></span>**

    <span data-ttu-id="9c646-153">Некоторые приложения имеют возможность автоматически проверять наличие последних обновлений во время установки.</span><span class="sxs-lookup"><span data-stu-id="9c646-153">Some applications have the ability to check for the latest updates automatically during installation.</span></span> <span data-ttu-id="9c646-154">Для упрощения управления версиями виртуальных пакетов приложений следует отключить эту функцию во время последовательности.</span><span class="sxs-lookup"><span data-stu-id="9c646-154">To assist with versioning of virtual application packages, you should disable this feature during sequencing.</span></span> <span data-ttu-id="9c646-155">Если есть необходимые обновления, вы должны поочередно использовать новый виртуальный пакет приложения с установленными связанными обновлениями.</span><span class="sxs-lookup"><span data-stu-id="9c646-155">If there are required updates, you should sequence a new virtual application package with the associated updates installed.</span></span>

## <span data-ttu-id="9c646-156">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9c646-156">Related topics</span></span>


[<span data-ttu-id="9c646-157">Планирование развертывания системы виртуализации приложений</span><span class="sxs-lookup"><span data-stu-id="9c646-157">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





