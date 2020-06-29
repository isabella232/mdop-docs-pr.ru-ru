---
title: Создание пакета рабочих областей MED-V
description: Создание пакета рабочих областей MED-V
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823262"
---
# <span data-ttu-id="3dc18-103">Создание пакета рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="3dc18-103">Create a MED-V Workspace Package</span></span>


<span data-ttu-id="3dc18-104">Рабочая область MED-V — это настольная среда Windows XP, в которой пользователи взаимодействуют с виртуальной машиной, предоставляемой MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-104">A MED-V workspace is the Windows XP desktop environment where end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="3dc18-105">Администратор создает и настроит рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-105">The administrator creates and customizes the MED-V workspace.</span></span> <span data-ttu-id="3dc18-106">Рабочая область состоит из изображения и групповой политики, определяющей правила и функциональные возможности рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-106">The workspace consists of an image and the Group Policy that defines the rules and functionality of the MED-V workspace.</span></span>

<span data-ttu-id="3dc18-107">Вы можете создать несколько рабочих областей для MED-V, каждый из которых настроен с помощью собственной конфигурации, параметров и правил.</span><span class="sxs-lookup"><span data-stu-id="3dc18-107">You can create multiple MED-V workspaces, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="3dc18-108">Пользователи, группы или несколько пользователей или групп могут быть связаны с каждой рабочей областью MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-108">A user, group, or multiple users or groups can be associated with each MED-V workspace.</span></span> <span data-ttu-id="3dc18-109">Настройка делает рабочую область MED-V доступной только для этого пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="3dc18-109">The customization makes that MED-V workspace available only for that user or group.</span></span>

<span data-ttu-id="3dc18-110">Использование **диспетчера рабочих областей med-v** для создания рабочих областей med-v.</span><span class="sxs-lookup"><span data-stu-id="3dc18-110">Use the **MED-V Workspace Packager** to create MED-V workspaces.</span></span> <span data-ttu-id="3dc18-111">**Диспетчер рабочих областей MED-V** делится на два основных раздела:</span><span class="sxs-lookup"><span data-stu-id="3dc18-111">The **MED-V Workspace Packager** is divided into two main sections:</span></span>

-   <span data-ttu-id="3dc18-112">Главная панель, содержащая три кнопки, которые используются для создания рабочих областей MED-V и управления ими.</span><span class="sxs-lookup"><span data-stu-id="3dc18-112">A main panel that includes three buttons that you use to create and manage MED-V workspaces.</span></span> <span data-ttu-id="3dc18-113">Кнопка " **создать пакет рабочей области для MED-v** " открывает **Мастер создания пакета рабочей области** для MED-v, который используется для создания рабочих областей med-v.</span><span class="sxs-lookup"><span data-stu-id="3dc18-113">The **Create a MED-V Workspace Package** button opens the **Create MED-V Workspace Package Wizard** that you use to create your MED-V workspaces.</span></span>

-   <span data-ttu-id="3dc18-114">**Центр справки** в правой части окна, в котором содержатся сведения и рекомендации по созданию, тестированию и управлению рабочими областями MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-114">A **Help Center** on the right-hand side of the window that provides information and guidance to help you create, test, and manage your MED-V workspaces.</span></span>

**<span data-ttu-id="3dc18-115">Важно.</span><span class="sxs-lookup"><span data-stu-id="3dc18-115">Important</span></span>**  
<span data-ttu-id="3dc18-116">Прежде чем вы сможете использовать **Диспетчер рабочих областей MED-V**, сначала убедитесь, что для политики выполнения Windows PowerShell задано значение "неограниченный".</span><span class="sxs-lookup"><span data-stu-id="3dc18-116">Before you can use the **MED-V Workspace Packager**, you must first make sure that the Windows PowerShell execution policy is set to Unrestricted.</span></span>

`Set-ExecutionPolicy Unrestricted`

<span data-ttu-id="3dc18-117">Кроме того, политика SAN для компьютера, на котором запускается **Диспетчер рабочих областей MED-V** , должна иметь значение "в сети".</span><span class="sxs-lookup"><span data-stu-id="3dc18-117">In addition, the SAN policy for the computer on which the **MED-V Workspace Packager** is run must be set to “Online All”.</span></span> <span data-ttu-id="3dc18-118">Чтобы проверить настройку политики SAN, выполните следующие команды в командной строке с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="3dc18-118">To check the setting of the SAN policy, run the following commands at a command prompt with administrative credentials:</span></span>

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

<span data-ttu-id="3dc18-119">При необходимости измените политику SAN на "в сети", введя указанные ниже команды в командной строке с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="3dc18-119">If it is necessary, change the SAN policy to "Online All" by typing the following commands at the command prompt with administrative credentials:</span></span>

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**<span data-ttu-id="3dc18-120">Важно.</span><span class="sxs-lookup"><span data-stu-id="3dc18-120">Important</span></span>**  
<span data-ttu-id="3dc18-121">Если на компьютере, с которого вы подключаетесь к виртуальному жесткому диску и собрано приложение MED-V, необходимо отключить автоматическое шифрование дисков, прежде чем приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="3dc18-121">If automatic disk encryption software is installed on the computer that you use to mount the virtual hard disk and build the MED-V workspace package, you must disable the software before you start.</span></span> <span data-ttu-id="3dc18-122">В противном случае вы не сможете использовать рабочую область MED-V на любом другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="3dc18-122">Otherwise, you cannot use the MED-V workspace on any other computer.</span></span>



<span data-ttu-id="3dc18-123">Предоставленные здесь сведения помогут вам создать пакет развертывания рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-123">The information we provide here can help you create your MED-V workspace deployment package.</span></span>

## <a href="" id="bkmk-prereq"></a><span data-ttu-id="3dc18-124">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="3dc18-124">Prerequisites</span></span>


<span data-ttu-id="3dc18-125">Прежде чем приступить к созданию пакета развертывания рабочей области для MED-V, убедитесь в том, что у вас есть доступ к следующим элементам:</span><span class="sxs-lookup"><span data-stu-id="3dc18-125">Before you start to build your MED-V workspace deployment package, verify that you have access to the following items:</span></span>

-   **<span data-ttu-id="3dc18-126">Подготовленный образ Windows XP</span><span class="sxs-lookup"><span data-stu-id="3dc18-126">A prepared Windows XP image</span></span>**

    <span data-ttu-id="3dc18-127">Дополнительные сведения о том, как создать образ Windows XP для использования в MED-V, можно найти в статье [Подготовка образа MED-v](prepare-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="3dc18-127">For more information about how to create a Windows XP image for use with MED-V, see [Prepare a MED-V Image](prepare-a-med-v-image.md).</span></span>

-   **<span data-ttu-id="3dc18-128">Текстовый файл или список, содержащий сведения о перенаправлении URL-адреса</span><span class="sxs-lookup"><span data-stu-id="3dc18-128">A text file or list that contains URL redirection information</span></span>**

    <span data-ttu-id="3dc18-129">В текстовом файле или списке перенаправления URL-адресов находятся URL-адреса, которые нужно перенаправлять с главного компьютера в Internet Explorer в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-129">Your URL redirection text file or list contains those URLs that you want redirected from the host computer to Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="3dc18-130">Если вы используете мастер упаковки для создания рабочей области для MED-V, импортируйте, введите (или скопируйте и вставьте) эти сведения о перенаправлении как один из шагов процесса создания пакета.</span><span class="sxs-lookup"><span data-stu-id="3dc18-130">When you are using the packaging wizard to create your MED-V workspace, you import, type, or copy and paste this redirection information as one of the steps in the package creation process.</span></span>

    **<span data-ttu-id="3dc18-131">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3dc18-131">Note</span></span>**  
    <span data-ttu-id="3dc18-132">Перенаправление URL-адресов в MED-V поддерживает только протоколы HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3dc18-132">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="3dc18-133">MED-V не обеспечивает поддержку FTP или других протоколов.</span><span class="sxs-lookup"><span data-stu-id="3dc18-133">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## <span data-ttu-id="3dc18-134">Упаковка рабочей области для MED-V на язык, отличный от языка компьютера с диспетчером рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="3dc18-134">Packaging a MED-V Workspace for a Language Other than the Language of the MED-V Workspace Packager Computer</span></span>


<span data-ttu-id="3dc18-135">По умолчанию в рабочей области MED-V поддерживаются символы как на языке компьютера, так и на английском.</span><span class="sxs-lookup"><span data-stu-id="3dc18-135">By default, the MED-V workspace supports characters in both the language of the computer and in English.</span></span> <span data-ttu-id="3dc18-136">Чтобы создать рабочую область для MED-V на языке, отличном от установленного на компьютере, в сценарии PowerShell (PS1) после имени рабочей области для MED-V введите **-Loc \ [locale \]** .</span><span class="sxs-lookup"><span data-stu-id="3dc18-136">To create a MED-V workspace for a language other than the one installed on the computer, specify **-loc \[locale\]** in the PowerShell script (.ps1) after the MED-V workspace name.</span></span>

<span data-ttu-id="3dc18-137">Чтобы создать пакет рабочей области для MED-V на языке, отличном от языка по умолчанию на компьютере с диспетчером рабочих областей MED-V, создайте сценарий на языке по умолчанию, запустив диспетчер рабочих областей MED-V и изменив сценарий вывода нужным образом для вашего языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="3dc18-137">To create a MED-V workspace package in a language other than the default language of the MED-V Workspace Packager computer, generate a script in the default language by running the MED-V Workspace Packager and then modifying the output script as required for your locale.</span></span> <span data-ttu-id="3dc18-138">Сценарий находится в каталоге выходных данных рабочей области MED-V, который был указан во время упаковки.</span><span class="sxs-lookup"><span data-stu-id="3dc18-138">The script is located in the MED-V workspace output directory that was specified during packaging.</span></span> <span data-ttu-id="3dc18-139">Названия региональных параметров находятся в. WXL файлы в следующем каталоге:</span><span class="sxs-lookup"><span data-stu-id="3dc18-139">The names of the locale settings are on the .WXL files in the following directory:</span></span>

<span data-ttu-id="3dc18-140">C:\\program Files Files\\Microsoft Enterprise для настольных компьютеров Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale</span><span class="sxs-lookup"><span data-stu-id="3dc18-140">C:\\Program Files\\Microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale</span></span>

## <span data-ttu-id="3dc18-141">Создание пакета рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="3dc18-141">Creating a MED-V Workspace Package</span></span>


<span data-ttu-id="3dc18-142">Чтобы создать пакет рабочей области для MED-V, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3dc18-142">To create a MED-V workspace package, follow these steps:</span></span>

****

1.  <span data-ttu-id="3dc18-143">Чтобы открыть **Диспетчер рабочих областей MED-V**, нажмите **кнопку Пуск**, выберите **все программы**, а затем — **Microsoft Enterprise Virtualization**, а затем — **Диспетчер рабочих областей med-v**.</span><span class="sxs-lookup"><span data-stu-id="3dc18-143">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="3dc18-144">На главной панели **диспетчера рабочих областей med-v** щелкните **создать пакет рабочей области для MED-v**.</span><span class="sxs-lookup"><span data-stu-id="3dc18-144">On the **MED-V Workspace Packager** main panel, click **Create a MED-V Workspace Package**.</span></span>

    <span data-ttu-id="3dc18-145">Откроется **Мастер создания пакета рабочей области для MED** -v (MED).</span><span class="sxs-lookup"><span data-stu-id="3dc18-145">The MED-V **Create MED-V Workspace Package Wizard** appears.</span></span> <span data-ttu-id="3dc18-146">Мастер состоит из следующих страниц:</span><span class="sxs-lookup"><span data-stu-id="3dc18-146">The wizard consists of the following pages:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="3dc18-147">Сведения о пакете</span><span class="sxs-lookup"><span data-stu-id="3dc18-147">Package Information</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="3dc18-148">Укажите имя рабочей области MED-V и выберите папку, в которой хранятся файлы пакета рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-148">Specify a name for the MED-V workspace and select a folder where the MED-V workspace package files are saved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="3dc18-149">Выбор образа Windows XP</span><span class="sxs-lookup"><span data-stu-id="3dc18-149">Select Windows XP Image</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="3dc18-150">Укажите свой подготовленный образ Virtual PC для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3dc18-150">Specify your prepared Windows XP Virtual PC image.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="3dc18-151">Установка первого раза</span><span class="sxs-lookup"><span data-stu-id="3dc18-151">First Time Setup</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="3dc18-152">Укажите процесс настройки, заданный для MED-V, при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="3dc18-152">Specify the setup process that MED-V follows during first time setup.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="3dc18-153">Сообщения MED-V</span><span class="sxs-lookup"><span data-stu-id="3dc18-153">MED-V Messages</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="3dc18-154">Укажите сообщения и Необязательный URL-адрес для справочной информации, которую конечный пользователь видит при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="3dc18-154">Specify the messages and optional URL for Help information that the end user sees during first time setup.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="3dc18-155">Именование компьютеров</span><span class="sxs-lookup"><span data-stu-id="3dc18-155">Naming Computers</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="3dc18-156">Укажите, как называется виртуальная машина MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-156">Specify how the MED-V virtual machine is named.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="3dc18-157">Копирование параметров с узла</span><span class="sxs-lookup"><span data-stu-id="3dc18-157">Copy Settings from Host</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="3dc18-158">Укажите, как определяются параметры рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-158">Specify how the settings for the MED-V workspace are defined.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="3dc18-159">Запуск и работа в сети</span><span class="sxs-lookup"><span data-stu-id="3dc18-159">Startup and Networking</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="3dc18-160">Укажите параметры для запуска рабочей области MED-V, сети и учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="3dc18-160">Specify the settings for starting the MED-V workspace, networking, and user credentials.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="3dc18-161">Перенаправление веб-сайта</span><span class="sxs-lookup"><span data-stu-id="3dc18-161">Web Redirection</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="3dc18-162">Укажите текстовый файл или список URL-адресов, которые нужно перенаправлять в Internet Explorer в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-162">Specify a text file or a list of the URLs you want redirected to Internet Explorer in the MED-V workspace.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="3dc18-163">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3dc18-163">Summary</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="3dc18-164">Проверьте параметры рабочей области для MED-V и начните создавать пакет развертывания для рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-164">Verify your MED-V workspace settings and start to build your MED-V workspace deployment package.</span></span></p></td>
    </tr>
    </tbody>
    </table>



3.  <span data-ttu-id="3dc18-165">На странице **сведения о пакете** введите имя рабочей области MED-v и выберите папку, в которой хранятся файлы пакета рабочей области для MED-v.</span><span class="sxs-lookup"><span data-stu-id="3dc18-165">On the **Package Information** page, enter a name for the MED-V workspace and select a folder where the MED-V workspace package files are saved.</span></span>

    **<span data-ttu-id="3dc18-166">Warning</span><span class="sxs-lookup"><span data-stu-id="3dc18-166">Warning</span></span>**  
    <span data-ttu-id="3dc18-167">Необходимо присвоить имя рабочей области MED-V и указать папку для продолжения.</span><span class="sxs-lookup"><span data-stu-id="3dc18-167">You must name the MED-V workspace and specify a folder to continue.</span></span>



~~~
After you have finished, click **Next**.
~~~

4. <span data-ttu-id="3dc18-168">На странице " **Выбор образа Windows XP** " укажите расположение готового образа виртуального компьютера для Windows XP (VHD-файла).</span><span class="sxs-lookup"><span data-stu-id="3dc18-168">On the **Select Windows XP Image** page, specify the location of your prepared MED-V Windows XP Virtual PC image (.vhd file).</span></span>

   **<span data-ttu-id="3dc18-169">Warning</span><span class="sxs-lookup"><span data-stu-id="3dc18-169">Warning</span></span>**  
   <span data-ttu-id="3dc18-170">Чтобы продолжить, необходимо задать VHD-образ Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3dc18-170">You must specify a Windows XP VHD image to continue.</span></span>



~~~
After you have finished, click **Next**.
~~~

5. <span data-ttu-id="3dc18-171">На странице "Настройка" в **первый раз** выберите, нужно ли запускать программу установки при входе в систему, а также в том случае, если вы хотите использовать рабочую область MED-V отдельно или для всех конечных пользователей на компьютере с общим доступом.</span><span class="sxs-lookup"><span data-stu-id="3dc18-171">On the **First Time Setup** page, select whether you want first time setup to run while attended or unattended and whether you want the MED-V workspace used separately or used by all end users on a shared computer.</span></span>

   <span data-ttu-id="3dc18-172">Если вы выберете параметр **Автоматическая установка без уведомления**, конечные пользователи не уведомляются, пока не будет запущена программа установки, и виртуальная машина не отображается для конечных пользователей при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="3dc18-172">If you select **Unattended setup, without any notification**, the end user is not informed before first time setup is run and the virtual machine is not shown to the end user during first time setup.</span></span> <span data-ttu-id="3dc18-173">Кроме того, страница " **Сообщения MED-V** " мастера скрыта, так как при первом запуске программы установки в автоматическом режиме не требуется никаких сообщений.</span><span class="sxs-lookup"><span data-stu-id="3dc18-173">In addition, the **MED-V Messages** page of the wizard is hidden because no messages are required if first time setup runs in a completely unattended mode.</span></span>

   <span data-ttu-id="3dc18-174">Если вы выберете параметр **Автоматическая установка, но уведомлять конечных пользователей перед первой попыткой настройки**, конечные пользователи будут уведомлены до начала настройки.</span><span class="sxs-lookup"><span data-stu-id="3dc18-174">If you select **Unattended setup, but notify end users before first time setup begins**, the end user is informed before first time setup is run.</span></span> <span data-ttu-id="3dc18-175">Однако виртуальная машина не отображается для конечного пользователя при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="3dc18-175">However, the virtual machine is not shown to the end user during first time setup.</span></span>

   <span data-ttu-id="3dc18-176">Выберите пункт **Ручная настройка** , если пользователь должен ввести данные при первом запуске программы.</span><span class="sxs-lookup"><span data-stu-id="3dc18-176">Select **Attended setup** if the end user must enter information during first time setup.</span></span>

   <span data-ttu-id="3dc18-177">По умолчанию используется **Автоматическая установка, но уведомление конечных пользователей перед первой повременной настройкой**.</span><span class="sxs-lookup"><span data-stu-id="3dc18-177">The default behavior is **Unattended setup, but notify end users before first time setup begins**.</span></span>

   **<span data-ttu-id="3dc18-178">Осторожны</span><span class="sxs-lookup"><span data-stu-id="3dc18-178">Caution</span></span>**  
   <span data-ttu-id="3dc18-179">Если файл Sysprep. INF создан таким образом, что для завершения работы мини-установки требуется ввод данных пользователем, необходимо выбрать параметр невозможная **Настройка** или проблемы при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="3dc18-179">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, you must select **Attended setup** or problems might occur during first time setup.</span></span>



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. <span data-ttu-id="3dc18-180">На странице **Сообщения MED-V** укажите следующие сообщения, которые будет видеть конечный пользователь при первом запуске программы установки:</span><span class="sxs-lookup"><span data-stu-id="3dc18-180">On the **MED-V Messages** page, specify the following messages that the end user sees during first time setup:</span></span>

   -   <span data-ttu-id="3dc18-181">Сообщение, которое пользователь видит при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="3dc18-181">The message that the end user sees when first time setup starts.</span></span>

   -   <span data-ttu-id="3dc18-182">Сообщение, которое пользователь видит при возникновении ошибки при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="3dc18-182">The message that the end user sees if first time setup fails or an error occurs.</span></span>

   **<span data-ttu-id="3dc18-183">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3dc18-183">Note</span></span>**  
   <span data-ttu-id="3dc18-184">Страница **сообщений MED-V** в мастере скрыта, если вы выбрали параметр **Автоматическая установка без уведомления** на странице **настройки в первый раз** .</span><span class="sxs-lookup"><span data-stu-id="3dc18-184">The **MED-V Messages** page of the wizard is hidden if you selected **Unattended setup, without any notification** on the **First Time Setup** page.</span></span>



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. <span data-ttu-id="3dc18-185">На странице **именование компьютеров** вы можете указать, следует ли управлять именованием компьютеров с помощью MED-V или с помощью средства управления системой (например, Sysprep).</span><span class="sxs-lookup"><span data-stu-id="3dc18-185">On the **Naming Computers** page, you can specify whether computer naming is managed by MED-V or by a system management tool, such as Sysprep.</span></span> <span data-ttu-id="3dc18-186">По умолчанию имя компьютера управляется средством управления системой.</span><span class="sxs-lookup"><span data-stu-id="3dc18-186">The default is that computer naming is managed by a system management tool.</span></span>

   <span data-ttu-id="3dc18-187">Если вы указали, что именование компьютеров управляется MED-V, выберите в раскрывающемся списке предопределенное соглашение об именовании компьютеров (маска).</span><span class="sxs-lookup"><span data-stu-id="3dc18-187">If you specify that computer naming is managed by MED-V, select a predefined computer naming convention (mask) from the drop-down list.</span></span> <span data-ttu-id="3dc18-188">На экране появится образец имени компьютера, основанный на компьютере, который вы используете для создания пакета рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-188">A preview of a sample computer name appears that is based on the computer that you are using to build the MED-V workspace package.</span></span>

   <span data-ttu-id="3dc18-189">Если вы выбрали один из настраиваемых соглашений об именовании, поля, которые можно указать, ограничиваются следующими символами:</span><span class="sxs-lookup"><span data-stu-id="3dc18-189">If you select one of the custom naming conventions, the fields you can specify are limited to the following characters:</span></span>

   -   <span data-ttu-id="3dc18-190">Поля "префикс" и "суффикс" ограничены символами A-Z, a-z, 0-9 и специальными знаками!</span><span class="sxs-lookup"><span data-stu-id="3dc18-190">The prefix and suffix fields are limited to the characters A-Z, a-z, 0-9, and the special characters !</span></span> <span data-ttu-id="3dc18-191">@ \ # $% ^ & ()-\ _ ' {}.</span><span class="sxs-lookup"><span data-stu-id="3dc18-191">@ \# $ % ^ & ( ) - \_ ' { } .</span></span> <span data-ttu-id="3dc18-192">и ~.</span><span class="sxs-lookup"><span data-stu-id="3dc18-192">and ~.</span></span>

   -   <span data-ttu-id="3dc18-193">Поля hostname и username ограничены цифрами от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="3dc18-193">The hostname and username fields are limited to the digits 0 through 9.</span></span>

   **<span data-ttu-id="3dc18-194">Важно.</span><span class="sxs-lookup"><span data-stu-id="3dc18-194">Important</span></span>**  
   <span data-ttu-id="3dc18-195">Имена компьютеров должны быть уникальными и содержать не более 15 символов.</span><span class="sxs-lookup"><span data-stu-id="3dc18-195">Computer names must be unique and are limited to a maximum of 15 characters.</span></span> <span data-ttu-id="3dc18-196">Если вы решите наименование компьютеров, разрешите конечные пользователи, у которых есть несколько компьютеров или общий доступ к компьютеру, и не используйте маски имен компьютеров, которые могут привести к конфликтам в сети.</span><span class="sxs-lookup"><span data-stu-id="3dc18-196">When you decide on your computer naming method, consider end users who have multiple computers or that share a computer, and avoid using computer name masks that could cause a collision on the network.</span></span>



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. <span data-ttu-id="3dc18-197">На странице " **копирование параметров с узла** " можно выбрать следующие параметры, чтобы указать, как настроена Рабочая область MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-197">On the **Copy Settings from Host** page, you can select the following settings to specify how the MED-V workspace is configured:</span></span>

   **<span data-ttu-id="3dc18-198">Осторожны</span><span class="sxs-lookup"><span data-stu-id="3dc18-198">Caution</span></span>**  
   <span data-ttu-id="3dc18-199">Параметры, которые вы задаете на этой странице, копируются из главного компьютера в рабочую область MED-V, переопределяя те из них, которые указаны в файле ответов Sysprep. INF.</span><span class="sxs-lookup"><span data-stu-id="3dc18-199">The settings that you specify on this page that are copied from the host computer to the MED-V workspace override those specified in the Sysprep.inf answer file.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. <span data-ttu-id="3dc18-200">На странице **Загрузка и** работа с сетью вы можете изменить поведение по умолчанию для указанных ниже параметров.</span><span class="sxs-lookup"><span data-stu-id="3dc18-200">On the **Startup and Networking** page, you can change the default behavior for the following settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="3dc18-201">Запуск рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="3dc18-201">Start MED-V workspace</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3dc18-202">Укажите, следует ли запускать рабочую область MED-V при входе пользователя в систему, при первом использовании или разрешить конечному пользователю при запуске рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-202">Choose whether to start the MED-V workspace at user logon, at first use, or to let the end user decide when the MED-V workspace starts.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="3dc18-203">Рабочая область MED-V запускается одним из двух способов: при входе пользователя в систему или при первом запуске действия, требующего MED-V (например, при открытии опубликованного приложения или вводе URL-адреса, требующего перенаправления).</span><span class="sxs-lookup"><span data-stu-id="3dc18-203">The MED-V workspace starts in one of two ways: either when the end user logs on or when they first start an action that requires MED-V, such as opening a published application or entering a URL that requires redirection.</span></span></p>
   <p><span data-ttu-id="3dc18-204">Вы можете задать этот параметр для конечного пользователя или позволить конечному пользователю управлять тем, как запустится MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-204">You can either define this setting for the end user or let the end user control how MED-V starts.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="3dc18-205">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3dc18-205">Note</span></span></strong><br/><p><span data-ttu-id="3dc18-206">Если вы указали, что конечный пользователь решает проблему, поведение по умолчанию — Рабочая область MED-V запускается при входе в систему.</span><span class="sxs-lookup"><span data-stu-id="3dc18-206">If you specify that the end user decides, the default behavior they experience is that the MED-V workspace starts when they log on.</span></span> <span data-ttu-id="3dc18-207">Они могут изменить значение по умолчанию, щелкнув правой кнопкой мыши значок MED-V в области уведомлений и выбрав пункт <strong> Параметры пользователя MED-v </strong> .</span><span class="sxs-lookup"><span data-stu-id="3dc18-207">They can change the default by right-clicking the MED-V icon in the notification area and selecting <strong>MED-V User Settings</strong>.</span></span> <span data-ttu-id="3dc18-208">Если вы определили этот параметр для конечного пользователя, он не сможет изменить способ запуска MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-208">If you define this setting for the end user, they cannot change how MED-V starts.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="3dc18-209">Сеть</span><span class="sxs-lookup"><span data-stu-id="3dc18-209">Networking</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3dc18-210">Выберите <strong> параметр Общий доступ </strong> или <strong> мост </strong> для сети.</span><span class="sxs-lookup"><span data-stu-id="3dc18-210">Select <strong>Shared</strong> or <strong>Bridged</strong> for your networking setting.</span></span> <span data-ttu-id="3dc18-211">Значение по умолчанию — <strong> Shared </strong> .</span><span class="sxs-lookup"><span data-stu-id="3dc18-211">The default is <strong>Shared</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong><span data-ttu-id="3dc18-212">Общая </strong> - Рабочая область для MED-V использует преобразование сетевых адресов (NAT) для предоставления общего доступа к узлу&#39;s IP для исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="3dc18-212">Shared</strong> - The MED-V workspace uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p>
   <p><strong><span data-ttu-id="3dc18-213">В мост </strong> - для рабочей области MED-V есть собственный сетевой адрес, обычно получаемый с помощью DHCP.</span><span class="sxs-lookup"><span data-stu-id="3dc18-213">Bridged</strong> - The MED-V workspace has its own network address, typically obtained through DHCP.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="3dc18-214">Хранение учетных данных</span><span class="sxs-lookup"><span data-stu-id="3dc18-214">Store credentials</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3dc18-215">Укажите, нужно ли хранить учетные данные конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3dc18-215">Choose whether you want to store the end user credentials.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="3dc18-216">По умолчанию хранение учетных данных отключено, так что конечный пользователь должен пройти проверку подлинности при каждом входе.</span><span class="sxs-lookup"><span data-stu-id="3dc18-216">The default behavior is that credential storing is disabled so that the end user must be authenticated every time that they log on.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="3dc18-217">Важно.</span><span class="sxs-lookup"><span data-stu-id="3dc18-217">Important</span></span></strong><br/><p><span data-ttu-id="3dc18-218">Несмотря на то, что кэширование учетных данных конечного пользователя обеспечивает наилучшее взаимодействие с пользователем, следует учитывать риски, связанные с этим.</span><span class="sxs-lookup"><span data-stu-id="3dc18-218">Even though caching the end user’s credentials provides the best user experience, you should be aware of the risks involved.</span></span></p>
   <p><span data-ttu-id="3dc18-219">Учетные данные домена конечного пользователя хранятся в диспетчере учетных данных Windows в обратимом формате.</span><span class="sxs-lookup"><span data-stu-id="3dc18-219">The end user’s domain credential is stored in a reversible format in the Windows Credential Manager.</span></span> <span data-ttu-id="3dc18-220">В результате злоумышленник может написать программу, которая извлекает пароль и может получить доступ к учетным данным пользователя.</span><span class="sxs-lookup"><span data-stu-id="3dc18-220">As a result, an attacker could write a program that retrieves the password and could gain access to the user’s credentials.</span></span> <span data-ttu-id="3dc18-221">Вы можете уменьшить этот риск, отключив хранение учетных данных конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3dc18-221">You can only lessen this risk by disabling the storing of end-user credentials.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. <span data-ttu-id="3dc18-222">На странице **Переадресация веб-сайта** можно ввести, вставить или импортировать список URL-адресов, перенаправленных в Internet Explorer в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-222">On the **Web Redirection** page, you can enter, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="3dc18-223">Дополнительные сведения о том, как настроить перенаправление URL-адресов, можно найти в разделе [Предварительные требования](#bkmk-prereq).</span><span class="sxs-lookup"><span data-stu-id="3dc18-223">For more information about how to configure your URL redirection information, see [Prerequisites](#bkmk-prereq).</span></span>

   <span data-ttu-id="3dc18-224">Вы также можете указать, как Internet Explorer в рабочей области MED-V настроен для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="3dc18-224">You can also specify how Internet Explorer in the MED-V workspace is configured for end users.</span></span> <span data-ttu-id="3dc18-225">По умолчанию для зоны Интернета установлен высокий уровень безопасности.</span><span class="sxs-lookup"><span data-stu-id="3dc18-225">By default, the Internet zone security level is set to High.</span></span> <span data-ttu-id="3dc18-226">Кроме того, некоторые возможности просмотра по умолчанию, такие как адресная строка, удаляются.</span><span class="sxs-lookup"><span data-stu-id="3dc18-226">Also, certain default browsing capabilities, such as the address bar, are removed.</span></span> <span data-ttu-id="3dc18-227">Эта конфигурация Internet Explorer по умолчанию в рабочей области MED-V обеспечивает более безопасную среду просмотра для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="3dc18-227">This default configuration of Internet Explorer in the MED-V workspace provides a more secure browsing environment for end users.</span></span>

   **<span data-ttu-id="3dc18-228">Осторожны</span><span class="sxs-lookup"><span data-stu-id="3dc18-228">Caution</span></span>**  
   <span data-ttu-id="3dc18-229">Изменяя параметры по умолчанию, вы можете настроить Internet Explorer в рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-229">By changing the default settings, you can customize Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="3dc18-230">Тем не менее, если вы измените параметры по умолчанию так, чтобы они были менее надежными, вы можете предоставить своей организации угрозу безопасности, которые присутствуют в более ранних версиях Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3dc18-230">However, realize that if you change the default settings so as to make them less secure, you can expose your organization to those security risks that are present in older versions of Internet Explorer.</span></span> <span data-ttu-id="3dc18-231">Дополнительные сведения можно найти в разделе Советы и [рекомендации по обеспечению безопасности при работе с MED-V](security-best-practices-for-med-v-operations.md).</span><span class="sxs-lookup"><span data-stu-id="3dc18-231">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>



~~~
After you have finished, click **Next**.
~~~

11. <span data-ttu-id="3dc18-232">На странице **сводки** вы можете просмотреть параметры упаковки для этой рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dc18-232">On the **Summary** page, you can review the packaging settings for this MED-V workspace.</span></span> <span data-ttu-id="3dc18-233">Если вы хотите изменить параметры, нажмите кнопку " **назад** ", чтобы вернуться к нужной странице.</span><span class="sxs-lookup"><span data-stu-id="3dc18-233">If you want to change any settings, click the **Previous** button to return to the relevant page.</span></span> <span data-ttu-id="3dc18-234">После того как вы закончите просмотр параметров, нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="3dc18-234">After you have finished reviewing the settings, click **Create**.</span></span>

   <span data-ttu-id="3dc18-235">Откроется страница **завершения** **мастера создания пакета рабочей области для MED-V** , чтобы показать ход выполнения создания пакета.</span><span class="sxs-lookup"><span data-stu-id="3dc18-235">The **Completion** page of the **Create MED-V Workspace Package Wizard** opens to show the progress of the package creation.</span></span>

   **<span data-ttu-id="3dc18-236">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3dc18-236">Note</span></span>**  
   <span data-ttu-id="3dc18-237">Процесс создания пакета рабочей области MED-V может занять несколько минут в зависимости от размера указанного виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="3dc18-237">The MED-V workspace package creation process might take several minutes to complete, depending on the size of the VHD specified.</span></span>



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. <span data-ttu-id="3dc18-238">Нажмите кнопку **Закрыть** , чтобы закрыть мастер упаковки и вернуться в **Диспетчер рабочих областей MED-V**.</span><span class="sxs-lookup"><span data-stu-id="3dc18-238">Click **Close** to close the packaging wizard and return to the **MED-V Workspace Packager**.</span></span>

<span data-ttu-id="3dc18-239">Пакет рабочей области для MED-V теперь готов к тестированию перед развертыванием.</span><span class="sxs-lookup"><span data-stu-id="3dc18-239">Your MED-V workspace package is now ready for testing before deployment.</span></span>

## <span data-ttu-id="3dc18-240">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3dc18-240">Related topics</span></span>


[<span data-ttu-id="3dc18-241">Настройка дополнительных параметров с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3dc18-241">Configuring Advanced Settings by Using Windows PowerShell</span></span>](configuring-advanced-settings-by-using-windows-powershell.md)

[<span data-ttu-id="3dc18-242">Тестирование пакета рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="3dc18-242">Testing the MED-V Workspace Package</span></span>](testing-the-med-v-workspace-package.md)

[<span data-ttu-id="3dc18-243">Подготовка образа MED-V</span><span class="sxs-lookup"><span data-stu-id="3dc18-243">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)









