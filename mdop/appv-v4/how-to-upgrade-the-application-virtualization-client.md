---
title: Обновление клиента Application Virtualization Client
description: Обновление клиента Application Virtualization Client
author: dansimp
ms.assetid: 2a75d8b5-da88-456c-85bb-f5bd3d470f7f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9748fbdba7c8d2777a06c93295e4582be784dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816452"
---
# <span data-ttu-id="0ac03-103">Обновление клиента Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="0ac03-103">How to Upgrade the Application Virtualization Client</span></span>


<span data-ttu-id="0ac03-104">Вы можете использовать следующие процедуры для обновления настольного клиента Application Virtualization (App-V) или клиента App-V для служб удаленных рабочих столов (ранее — служб терминалов).</span><span class="sxs-lookup"><span data-stu-id="0ac03-104">You can use the following procedures to upgrade the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="0ac03-105">Вы обновляете клиент, устанавливая новую версию по сравнению с ранее установленной старой версией.</span><span class="sxs-lookup"><span data-stu-id="0ac03-105">You upgrade the client by installing a new version over the previously installed older version.</span></span> <span data-ttu-id="0ac03-106">Когда вы обновляете клиенты, программное обеспечение установщика автоматически сохраняет и переносит параметры пользователя для виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="0ac03-106">When you upgrade the clients, the installer software automatically preserves and migrates the user’s settings for virtual applications.</span></span> <span data-ttu-id="0ac03-107">Для запуска программы установки требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="0ac03-107">Administrative rights are required to run the setup program.</span></span>

<span data-ttu-id="0ac03-108">**Примечание**  При обновлении до Application Virtualization (App-V) 4.5 или более поздней версии разрешения на раздел реестра HKCU изменяются.</span><span class="sxs-lookup"><span data-stu-id="0ac03-108">**Note** During the upgrade to Application Virtualization (App-V)4.5 or later versions, the permissions to the HKCU registry key are changed.</span></span> <span data-ttu-id="0ac03-109">Из-за этого пользователи будут терять пользовательские конфигурации, которые ранее были установлены, например настроенные пользователем параметры режима отключения.</span><span class="sxs-lookup"><span data-stu-id="0ac03-109">Because of this, users will lose user configurations that were set previously, such as user-configured Disconnected Mode settings.</span></span> <span data-ttu-id="0ac03-110">Если пользователю запрещено настраивать поведение пользовательского интерфейса клиента с помощью блокировки разрешений, пользователь может сбросить эти параметры после обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="0ac03-110">If the user is not actively restricted from configuring client user interface behavior through a permission lockdown, the user can reset these preferences after a publishing refresh.</span></span>

 

<span data-ttu-id="0ac03-111">**Важно!**  При обновлении до версии 4.6 или более поздней версии клиента App-V необходимо использовать правильный установщик для операционной системы компьютера, 32-bit или 64-bit.</span><span class="sxs-lookup"><span data-stu-id="0ac03-111">**Important** When upgrading to version4.6 or a later version of the App-V Client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="0ac03-112">Установка завершится сбоем и появится сообщение об ошибке, если вы используете неправильный установщик.</span><span class="sxs-lookup"><span data-stu-id="0ac03-112">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

 

**<span data-ttu-id="0ac03-113">Обновление классической версии клиента Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0ac03-113">To upgrade the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="0ac03-114">Завершите работу всех виртуальных приложений, щелкните правой кнопкой мыши значок клиента App-V на рабочем столе в области уведомлений рабочего стола Windows и выберите команду **выход** , чтобы завершить работу существующего клиента.</span><span class="sxs-lookup"><span data-stu-id="0ac03-114">Shut down all virtual applications, right-click the App-V Desktop Client icon displayed in the Windows desktop notification area, and select **Exit** to shut down the existing client.</span></span>

2.  <span data-ttu-id="0ac03-115">После того как вы получили правильный архивный файл установщика и сохранили его на своем компьютере, дважды щелкните его, чтобы развернуть архив.</span><span class="sxs-lookup"><span data-stu-id="0ac03-115">After you have obtained the correct installer archive file and saved it to your computer, double-click it to expand the archive.</span></span>

3.  <span data-ttu-id="0ac03-116">Найдите файл setup.exe и дважды щелкните setup.exe, чтобы начать установку.</span><span class="sxs-lookup"><span data-stu-id="0ac03-116">Browse to find the setup.exe file, and double-click setup.exe to start the installation.</span></span>

4.  <span data-ttu-id="0ac03-117">Мастер проверяет систему, чтобы убедиться, что все необходимое программное обеспечение установлено, и предложит установить любое из указанных ниже действий, если оно отсутствует.</span><span class="sxs-lookup"><span data-stu-id="0ac03-117">The wizard checks the system to ensure that all prerequisite software is installed and will prompt you to install any of the following, if missing:</span></span>

    -   <span data-ttu-id="0ac03-118">Распространяемый пакет Microsoft VisualC + + 2005SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="0ac03-118">Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>

    -   <span data-ttu-id="0ac03-119">Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="0ac03-119">Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

    -   <span data-ttu-id="0ac03-120">Отчеты об ошибках в приложениях Майкрософт</span><span class="sxs-lookup"><span data-stu-id="0ac03-120">Microsoft Application Error Reporting</span></span>

    <span data-ttu-id="0ac03-121">**Примечание**  Для версии 4.6 и выше мастер также установит следующие предварительные требования к программному обеспечению:</span><span class="sxs-lookup"><span data-stu-id="0ac03-121">**Note** For version4.6 and higher, the wizard will also install the following software prerequisite:</span></span>

    -   <span data-ttu-id="0ac03-122">Распространяемый пакет Microsoft VisualC + + 2008SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="0ac03-122">Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

     

5.  <span data-ttu-id="0ac03-123">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="0ac03-123">Click **Install**.</span></span> <span data-ttu-id="0ac03-124">Отобразится ход выполнения установки, после чего состояние изменится с " **Ожидание** " на **Установка**.</span><span class="sxs-lookup"><span data-stu-id="0ac03-124">Installation progress is displayed, and the status changes from **Pending** to **Installing**.</span></span> <span data-ttu-id="0ac03-125">Состояние установки изменится на " **успешно** " при успешном завершении каждого шага.</span><span class="sxs-lookup"><span data-stu-id="0ac03-125">Installation status changes to **Succeeded** as each step is completed successfully.</span></span>

6.  <span data-ttu-id="0ac03-126">После появления диалогового окна " **клиент виртуализации приложений** " и выводит сообщение о том, что на компьютере обнаружена старая версия клиента, нажмите кнопку **Далее** , чтобы перейти к новой версии.</span><span class="sxs-lookup"><span data-stu-id="0ac03-126">When the **Application Virtualization Desktop Client** dialog appears and displays a message stating that an older version of the client has been found on the computer, click **Next** to upgrade to the new version.</span></span>

7.  <span data-ttu-id="0ac03-127">Когда появится экран лицензионного **соглашения** , ознакомьтесь с лицензионным соглашением и, если вы согласны, выберите **я принимаю условия лицензионного соглашения**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="0ac03-127">When the **License Agreement** screen is displayed, read the license agreement, and if you agree, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

8.  <span data-ttu-id="0ac03-128">Когда мастер InstallShield отобразит окно **Готово для обновления** экрана, нажмите кнопку **Обновить** , чтобы начать обновление.</span><span class="sxs-lookup"><span data-stu-id="0ac03-128">When the InstallShield Wizard displays the **Ready to Upgrade the Program** dialog screen, click **Upgrade** to begin the upgrade.</span></span> <span data-ttu-id="0ac03-129">На следующем экране показано, что клиент установлен.</span><span class="sxs-lookup"><span data-stu-id="0ac03-129">The next screen indicates that the client is being installed.</span></span>

    <span data-ttu-id="0ac03-130">**Предупреждение**  Если вы не запустили клиентскую программу на этапе 1, вы можете увидеть предупреждение " **используется уже использованные файлы** ".</span><span class="sxs-lookup"><span data-stu-id="0ac03-130">**Warning** If you did not shut down the client program in step 1, you might see a **Files In Use** warning displayed.</span></span> <span data-ttu-id="0ac03-131">Если это случится, щелкните правой кнопкой мыши значок клиента App-V в области уведомлений на рабочем столе и выберите команду **выход** , чтобы завершить работу существующего клиента.</span><span class="sxs-lookup"><span data-stu-id="0ac03-131">If this happens, right-click the App-V Client icon displayed in the desktop notification area and select **Exit** to shut down the existing client.</span></span> <span data-ttu-id="0ac03-132">Затем нажмите кнопку **"повторить"** , чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="0ac03-132">Then click **Retry** to continue.</span></span>

     

9.  <span data-ttu-id="0ac03-133">После того как установка завершится успешно, вам будет предложено перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="0ac03-133">When the installation completes successfully, you will be prompted to restart the computer.</span></span> <span data-ttu-id="0ac03-134">Чтобы завершить установку, вам нужно перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="0ac03-134">You need to restart the computer to complete the installation.</span></span>

    <span data-ttu-id="0ac03-135">**Внимание!**  Если по какой – либо причине обновление завершится сбоем, перед повторной попыткой обновления вам потребуется перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="0ac03-135">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

**<span data-ttu-id="0ac03-136">Обновление клиента Application Virtualization с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="0ac03-136">To upgrade the Application Virtualization Client by Using the Command Line</span></span>**

1.  <span data-ttu-id="0ac03-137">Если вы обновите клиент App-V с помощью программы setup.msi, убедитесь, что установлены все необходимые программные компоненты.</span><span class="sxs-lookup"><span data-stu-id="0ac03-137">If upgrading the App-V client using the setup.msi program, ensure that any necessary prerequisite software has been installed.</span></span>

    **<span data-ttu-id="0ac03-138">Важно.</span><span class="sxs-lookup"><span data-stu-id="0ac03-138">Important</span></span>**  
    -   <span data-ttu-id="0ac03-139">В версии 4.6 и более поздних версий клиента App-V программа setup.msi проверяет систему и завершает работу с сообщением об ошибке, указывающий на то, что установка не может быть продолжена, если необходимое программное обеспечение не установлено.</span><span class="sxs-lookup"><span data-stu-id="0ac03-139">For version4.6 and later of the App-V client, the setup.msi program checks the system and will fail with an error message indicating that installation cannot continue if prerequisite software is not installed.</span></span>

    -   <span data-ttu-id="0ac03-140">Для App-V версии 4.6 параметры командной строки нельзя использовать во время обновления и будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="0ac03-140">For App-V version4.6, command-line parameters cannot be used during an upgrade and will be ignored.</span></span>

     

2.  <span data-ttu-id="0ac03-141">В приведенном ниже примере командной строки для обновления клиента App-V используется файл setup.msi.</span><span class="sxs-lookup"><span data-stu-id="0ac03-141">The following command-line example uses the setup.msi file to upgrade the App-V Client.</span></span> <span data-ttu-id="0ac03-142">Вам потребуется программа установщика клиента в зависимости от того, что вы обновляете: клиент App-V для настольных компьютеров или клиент App-V для служб удаленных рабочих столов (ранее — службы терминалов).</span><span class="sxs-lookup"><span data-stu-id="0ac03-142">You will need to use the correct client installer program depending on whether you are upgrading the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span>

    **<span data-ttu-id="0ac03-143">msiexec.exe/i "setup.msi"</span><span class="sxs-lookup"><span data-stu-id="0ac03-143">msiexec.exe /i "setup.msi"</span></span>**

    <span data-ttu-id="0ac03-144">**Важно!**  Кавычки необходимы только в том случае, если значение состоит из пробела.</span><span class="sxs-lookup"><span data-stu-id="0ac03-144">**Important** The quotation marks are required only when the value contains a space.</span></span> <span data-ttu-id="0ac03-145">Для обеспечения единообразия все вхождения в предыдущем примере отображаются в виде кавычек.</span><span class="sxs-lookup"><span data-stu-id="0ac03-145">For consistency, all instances in the preceding example are shown as having quotation marks.</span></span>

     

**<span data-ttu-id="0ac03-146">Обновление клиента Application Virtualization для служб удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="0ac03-146">To upgrade the Application Virtualization Client for Remote Desktop Services</span></span>**

1.  <span data-ttu-id="0ac03-147">Следуйте стандартным политикам организации, чтобы установить или обновить приложения на сервере сеансов удаленных рабочих столов (узла RDSession).</span><span class="sxs-lookup"><span data-stu-id="0ac03-147">Follow your organization’s standard policies for installing or upgrading applications on the Remote Desktop Session Host (RDSession Host) server.</span></span> <span data-ttu-id="0ac03-148">Если система входит в ферму, удалите узел RDSession из фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="0ac03-148">If the system is part of a farm, remove the RDSession Host from the server farm.</span></span>

2.  <span data-ttu-id="0ac03-149">Чтобы обновить клиент App-V для служб удаленных рабочих столов (ранее — служб терминалов), необходимо использовать командную строку, так как вы не можете обновить клиент вручную на узле RDSession.</span><span class="sxs-lookup"><span data-stu-id="0ac03-149">To upgrade the App-V Client for Remote Desktop Services (formerly Terminal Services), you must use the command line because you cannot upgrade the client manually on the RDSession Host.</span></span>

    <span data-ttu-id="0ac03-150">**Примечание**  В приложении App-V версии 4,6 и более поздних версий помимо использования командной строки для обновления клиента вы также можете использовать сеанс подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="0ac03-150">**Note** In App-V version 4.6 and later, in addition to using the command line to upgrade the client, you can also use a Remote Desktop session.</span></span> <span data-ttu-id="0ac03-151">Для запуска сеанса подключения к удаленному рабочему столу не требуется никаких специальных параметров.</span><span class="sxs-lookup"><span data-stu-id="0ac03-151">No special parameters are required to start the Remote Desktop session.</span></span>

     

3.  <span data-ttu-id="0ac03-152">После завершения обновления служб удаленных рабочих столов перезапустите узел RDSession и войдите в него.</span><span class="sxs-lookup"><span data-stu-id="0ac03-152">After the Client for Remote Desktop Services upgrade is complete, restart and log in to the RDSession Host.</span></span>

4.  <span data-ttu-id="0ac03-153">После перезапуска системы добавьте сервер в ферму серверов.</span><span class="sxs-lookup"><span data-stu-id="0ac03-153">After the system is restarted, add the server to the server farm.</span></span>

    <span data-ttu-id="0ac03-154">**Внимание!**  Если по какой – либо причине обновление завершится сбоем, перед повторной попыткой обновления вам потребуется перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="0ac03-154">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

## <span data-ttu-id="0ac03-155">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0ac03-155">Related topics</span></span>


[<span data-ttu-id="0ac03-156">Рекомендации перед развертыванием и обновлением Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0ac03-156">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





