---
title: Установка клиента App-V с помощью Setup.exe
description: Установка клиента App-V с помощью Setup.exe
author: dansimp
ms.assetid: 106a5d97-b5f6-4a16-bf52-a84f4d558c74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60f79a2d2f74848ab121ba13cdf8c215088d54db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817339"
---
# <span data-ttu-id="b64c2-103">Установка клиента App-V с помощью Setup.exe</span><span class="sxs-lookup"><span data-stu-id="b64c2-103">How to Install the App-V Client by Using Setup.exe</span></span>


<span data-ttu-id="b64c2-104">В этой статье описано, как установить клиент App-V с помощью программы setup.exe.</span><span class="sxs-lookup"><span data-stu-id="b64c2-104">This topic describes how to install the App-V client by using the setup.exe program.</span></span> <span data-ttu-id="b64c2-105">При установке клиента App-V с помощью программы setup.exe установщик определит, какое необходимое программное обеспечение потребуется, и установит его автоматически перед установкой клиента.</span><span class="sxs-lookup"><span data-stu-id="b64c2-105">When you install the App-V client using the setup.exe program, the installer determines which prerequisite software is needed and installs it automatically before it installs the client.</span></span>

**<span data-ttu-id="b64c2-106">Установка клиента Application Virtualization с помощью Setup.exe</span><span class="sxs-lookup"><span data-stu-id="b64c2-106">To install the Application Virtualization Client by Using Setup.exe</span></span>**

1.  <span data-ttu-id="b64c2-107">Убедитесь в том, что вы вошли в систему под учетной записью, обладающей правами администратора на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b64c2-107">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="b64c2-108">Откройте окно командной строки и измените каталог на папку, содержащую файлы установки.</span><span class="sxs-lookup"><span data-stu-id="b64c2-108">Open a Command Prompt window, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="b64c2-109">При установке версии 4.6 или более поздней версии клиента App-V необходимо использовать правильный установщик для операционной системы компьютера, 32-bit или 64-bit.</span><span class="sxs-lookup"><span data-stu-id="b64c2-109">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="b64c2-110">Установка завершится сбоем и появится сообщение об ошибке, если вы используете неправильный установщик.</span><span class="sxs-lookup"><span data-stu-id="b64c2-110">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="b64c2-111">Введите командную строку установки в командной строке.</span><span class="sxs-lookup"><span data-stu-id="b64c2-111">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="b64c2-112">Кроме того, вы можете создать командный файл и запустить его из командной строки.</span><span class="sxs-lookup"><span data-stu-id="b64c2-112">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="b64c2-113">Вы также можете использовать для выполнения команды язык сценариев, например VBScript или Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b64c2-113">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="b64c2-114">В приведенном ниже примере кода показано, как setup.exe можно использовать с несколькими необязательными параметрами.</span><span class="sxs-lookup"><span data-stu-id="b64c2-114">The following command-line example shows how setup.exe can be used with a number of optional parameters.</span></span> <span data-ttu-id="b64c2-115">Дополнительные сведения об этих параметрах можно найти в разделе [Параметры командной строки установщика клиента Application Virtualization](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b64c2-115">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="b64c2-116">"setup.exe"/s/v "/Qn SWICACHESIZE = \ \" 10240 \ \ "SWIPUBSVRDISPLAY = \ \" System\\ "SWIPUBSVRTYPE = \ \" HTTP/secure\\ "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \" 443 \ \ "" SWIPUBSVRPATH = \ \ "/AppVirt/appsntype.xml \ \" SWIPUBSVRREFRESH = \ \ "on\\" SWIGLOBALDATA = \ \ "D:\\AppVirt\\Global\\" SWIUSERDATA = \ \ "^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\" SWIFSDRIVE ""</span><span class="sxs-lookup"><span data-stu-id="b64c2-116">"setup.exe" /s /v"/qn SWICACHESIZE=\\"10240\\" SWIPUBSVRDISPLAY=\\"Production System\\" SWIPUBSVRTYPE=\\"HTTP /secure\\" SWIPUBSVRHOST=\\"PRODSYS\\" SWIPUBSVRPORT=\\"443\\" SWIPUBSVRPATH=\\"/AppVirt/appsntype.xml\\" SWIPUBSVRREFRESH=\\"on\\" SWIGLOBALDATA=\\"D:\\AppVirt\\Global\\" SWIUSERDATA=\\"^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\" SWIFSDRIVE=\\"Q\\""</span></span>**

    **<span data-ttu-id="b64c2-117">Важно.</span><span class="sxs-lookup"><span data-stu-id="b64c2-117">Important</span></span>**  
    -   <span data-ttu-id="b64c2-118">Кавычки, которые выводятся в разделе "**/v**", должны обрабатываться как специальные символы и вводиться с помощью предшествующего " **\\** ".</span><span class="sxs-lookup"><span data-stu-id="b64c2-118">The quotation marks that appear in the "**/v**" section must be treated as special characters and entered with a preceding "**\\**".</span></span> <span data-ttu-id="b64c2-119">Кавычки необходимы только в том случае, если в значении содержится пробел; Однако для обеспечения согласованности все экземпляры в предыдущем примере отображаются в виде кавычек.</span><span class="sxs-lookup"><span data-stu-id="b64c2-119">The quotation marks are required only when the value contains a space; however, for consistency, all the instances in the preceding example are shown as having quotation marks.</span></span>

    -   <span data-ttu-id="b64c2-120">**%** Символу ""**% HomeDrive%**"должен предшествовать **^** знак" "".</span><span class="sxs-lookup"><span data-stu-id="b64c2-120">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="b64c2-121">В противном случае Командная оболочка Windows задает значение для пользователя, который выполняет установку.</span><span class="sxs-lookup"><span data-stu-id="b64c2-121">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="b64c2-122">Для этой автоматической установки требуются переключатели **InstallShield** **/s** и **/qn** .</span><span class="sxs-lookup"><span data-stu-id="b64c2-122">The **InstallShield** switches **/s** and **/qn** are needed to make this a silent install.</span></span> <span data-ttu-id="b64c2-123">Ключ **/qn** должен следовать за параметром **/v** , отделенным символом кавычек и без пробелов.</span><span class="sxs-lookup"><span data-stu-id="b64c2-123">The **/qn** switch must follow the **/v** switch, separated by only a quote character with no intervening spaces.</span></span>

    -   <span data-ttu-id="b64c2-124">Папка, указанная в значении **SWIGLOBALDATA** , должна быть уже создана.</span><span class="sxs-lookup"><span data-stu-id="b64c2-124">The folder specified in the **SWIGLOBALDATA** value must already exist.</span></span>

     

5.  <span data-ttu-id="b64c2-125">После завершения установки рекомендуется запустить проверку Центра обновления Майкрософт, чтобы убедиться в том, что установлены последние обновления.</span><span class="sxs-lookup"><span data-stu-id="b64c2-125">When the installation is complete, we recommend that you run a Microsoft Update scan to ensure the latest updates are installed.</span></span>

## <span data-ttu-id="b64c2-126">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b64c2-126">Related topics</span></span>


[<span data-ttu-id="b64c2-127">Установка клиента с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="b64c2-127">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





