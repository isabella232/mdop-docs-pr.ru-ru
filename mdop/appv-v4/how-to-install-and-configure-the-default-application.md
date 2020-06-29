---
title: Установка и настройка приложения по умолчанию
description: Установка и настройка приложения по умолчанию
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817369"
---
# <span data-ttu-id="12194-103">Установка и настройка приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="12194-103">How to Install and Configure the Default Application</span></span>


<span data-ttu-id="12194-104">Приложение по умолчанию предоставляется в рамках установки и автоматически копируется на сервер управления Microsoft Application Virtualization (App-V) Management Server во время установки.</span><span class="sxs-lookup"><span data-stu-id="12194-104">The default application is provided as part of the installation and is automatically copied to the Microsoft Application Virtualization (App-V) Management Server during installation.</span></span> <span data-ttu-id="12194-105">Он используется для проверки правильности установки и настройки сервера управления, но его необходимо опубликовать в клиенте Microsoft Application Virtualization (App-V), чтобы пользователь мог получить к нему доступ.</span><span class="sxs-lookup"><span data-stu-id="12194-105">It is used to verify that the Management Server was installed and configured correctly, but it has to be published to the Microsoft Application Virtualization (App-V) Client so that the user can access it.</span></span>

<span data-ttu-id="12194-106">Выполните указанные ниже действия, чтобы опубликовать приложение по умолчанию и выполнить его потоковую передачу.</span><span class="sxs-lookup"><span data-stu-id="12194-106">Use the following procedures to publish the default application and to stream it.</span></span>

**<span data-ttu-id="12194-107">Публикация приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="12194-107">To publish the default application</span></span>**

1.  <span data-ttu-id="12194-108">Войдите на сервер управления App-V с помощью учетной записи, которая входит в группу администраторов App-V, указанную во время установки.</span><span class="sxs-lookup"><span data-stu-id="12194-108">Log on to the App-V Management Server by using an account that is a member of the App-V Administrators group specified during installation.</span></span>

2.  <span data-ttu-id="12194-109">На сервере управления App-V нажмите кнопку **Пуск**и выберите пункт **Администрирование**, а затем — **консоль управления Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="12194-109">On the App-V Management Server, click **Start**, click **Administrative Tools**, and then click **Application Virtualization Management Console**.</span></span>

3.  <span data-ttu-id="12194-110">В консоли управления App-V нажмите кнопку **действия**и выберите команду **подключиться к системе виртуализации приложений**.</span><span class="sxs-lookup"><span data-stu-id="12194-110">In the App-V Management Console, click **Actions**, and then click **Connect to Application Virtualization System**.</span></span>

4.  <span data-ttu-id="12194-111">На странице " **Настройка подключения** " снимите флажок **использовать безопасное соединение** .</span><span class="sxs-lookup"><span data-stu-id="12194-111">On the **Configure Connection** page, clear the **Use Secure Connection** check box.</span></span>

5.  <span data-ttu-id="12194-112">В поле **имя узла веб-службы** введите полное доменное имя (FQDN) сервера управления App-V и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="12194-112">In the **Web Service Host Name** box, type the fully qualified domain name (FQDN) of the App-V Management Server, and then click **OK**.</span></span>

    <span data-ttu-id="12194-113">**Примечание**  Вы также можете использовать **localhost** для имени узла веб-службы, если оно установлено на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="12194-113">**Note** You can also use **localhost** for the Web Service Host name if it is installed on the Management Server.</span></span>

     

6.  <span data-ttu-id="12194-114">В консоли управления App-V щелкните правой кнопкой мыши узел **сервера** и выберите пункт **Параметры системы**.</span><span class="sxs-lookup"><span data-stu-id="12194-114">In the App-V Management Console, right-click the **Server** node, and click **System Options**.</span></span>

7.  <span data-ttu-id="12194-115">На вкладке **Общие** в поле **путь к содержимому по умолчанию** введите путь в формате UNC к папке содержимого, созданной на сервере во время установки; Например, \ \ \ \ &lt; имя сервера &gt; \\Content и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="12194-115">On the **General** tab, in the **Default Content Path** box, enter the Universal Naming Convention (UNC) path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and then click **OK**.</span></span>

    <span data-ttu-id="12194-116">**Важно!**  Используйте полное доменное имя для имени сервера, чтобы клиент мог правильно разрешить его имя.</span><span class="sxs-lookup"><span data-stu-id="12194-116">**Important** Use the FQDN for the server name so that the client can resolve the name correctly.</span></span>

     

8.  <span data-ttu-id="12194-117">В консоли управления App-V в области навигации разверните узел **сервер** и выберите пункт **приложения**.</span><span class="sxs-lookup"><span data-stu-id="12194-117">In the App-V Management Console, in the navigation pane, expand the **Server** node, and then click **Applications**.</span></span>

9.  <span data-ttu-id="12194-118">В области разделов выберите пункт **приложение по умолчанию**, а затем в области **действия** нажмите кнопку **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="12194-118">In the topic pane, click **Default Application**, and then, in the **Actions** pane, click **Properties**.</span></span>

10. <span data-ttu-id="12194-119">В диалоговом окне **Свойства** рядом с полем **путь к OSD** нажмите кнопку **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="12194-119">In the **Properties** dialog box, next to the **OSD Path** box, click **Browse**.</span></span>

11. <span data-ttu-id="12194-120">В диалоговом окне **Открытие** файла введите UNC-путь к папке содержимого, созданной на сервере во время установки. Например, \ \ \ \ &lt; имя сервера &gt; \\Content и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="12194-120">In the **Open** dialog box, enter the UNC path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and press ENTER.</span></span> <span data-ttu-id="12194-121">Необходимо использовать фактическое имя сервера и не использовать **localhost** здесь.</span><span class="sxs-lookup"><span data-stu-id="12194-121">You must use the actual server name and cannot use the **localhost** here.</span></span>

    <span data-ttu-id="12194-122">**Важно!**  Убедитесь, что значения в полях **путь к OSD** и **путь к значкам** находятся в формате UNC (например, \ \ \ \ &lt; имя сервера &gt; \\Content\\DefaultApp.ICO), и наведите указатель мыши на папку, созданную при установке сервера.</span><span class="sxs-lookup"><span data-stu-id="12194-122">**Important** Ensure that the values in both the **OSD Path** and **Icon Path** boxes are in UNC format (for example, \\\\&lt;Server Name&gt;\\Content\\DefaultApp.ico), and point to the Content folder you created when installing the server.</span></span> <span data-ttu-id="12194-123">Не используйте **localhost** или путь к файлу, который содержит букву диска, например c:\\program Files Files\\.. \\.. Конфликтов.</span><span class="sxs-lookup"><span data-stu-id="12194-123">Do not use **localhost** or a file path containing a drive letter such as C:\\Program Files\\..\\..\\Content.</span></span>

     

12. <span data-ttu-id="12194-124">Выберите файл DefaultApp. OSD и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="12194-124">Select the DefaultApp.osd file, and click **Open**.</span></span>

13. <span data-ttu-id="12194-125">Повторите описанные выше действия, чтобы настроить путь значка.</span><span class="sxs-lookup"><span data-stu-id="12194-125">Repeat the previous steps to configure the icon path.</span></span>

14. <span data-ttu-id="12194-126">Откройте вкладку **разрешения на доступ** и убедитесь в том, что группе Пользователи App-V предоставлены разрешения на доступ к приложению.</span><span class="sxs-lookup"><span data-stu-id="12194-126">Click the **Access Permissions** tab, and confirm that the App-V Users group has access permissions to the application.</span></span>

15. <span data-ttu-id="12194-127">Откройте вкладку **сочетания клавиш** и нажмите кнопку **опубликовать на рабочем столе пользователя**.</span><span class="sxs-lookup"><span data-stu-id="12194-127">Click the **Shortcuts** tab, and then click **Publish to User’s Desktop**.</span></span> <span data-ttu-id="12194-128">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="12194-128">Click **OK**.</span></span>

16. <span data-ttu-id="12194-129">Откройте проводник и найдите каталог содержимого.</span><span class="sxs-lookup"><span data-stu-id="12194-129">Open Windows Explorer, and locate the Content directory.</span></span>

17. <span data-ttu-id="12194-130">Дважды щелкните файл DefaultApp. OSD и откройте его в блокноте.</span><span class="sxs-lookup"><span data-stu-id="12194-130">Double-click the DefaultApp.osd file, and open it with Notepad.</span></span>

18. <span data-ttu-id="12194-131">Найдите строку, содержащую тег **href** , и измените ее на следующий код:</span><span class="sxs-lookup"><span data-stu-id="12194-131">Locate the line that contains the **HREF** tag, and change it to the following code:</span></span>

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    <span data-ttu-id="12194-132">Если вы используете протоколы RTSP, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="12194-132">Or, if you are using RTSPS:</span></span>

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. <span data-ttu-id="12194-133">Закройте файл DefaultApp. OSD и сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="12194-133">Close the DefaultApp.osd file, and save the changes.</span></span>

**<span data-ttu-id="12194-134">Потоковая передача приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="12194-134">To stream the default application</span></span>**

1.  <span data-ttu-id="12194-135">На компьютере с установленным клиентом App-V Войдите в систему под учетной записью пользователя, который является членом группы Пользователи Application Virtualization, указанной во время установки сервера.</span><span class="sxs-lookup"><span data-stu-id="12194-135">On the computer that has the App-V Client installed, log on as a user who is a member of the Application Virtualization Users group specified during server installation.</span></span>

2.  <span data-ttu-id="12194-136">На рабочем столе появится ярлык **приложения Application Virtualization по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="12194-136">On the desktop, the **Default Application Virtualization Application** shortcut appears.</span></span> <span data-ttu-id="12194-137">Дважды щелкните ярлык, чтобы запустить приложение.</span><span class="sxs-lookup"><span data-stu-id="12194-137">Double-click the shortcut to start the application.</span></span>

3.  <span data-ttu-id="12194-138">В строке состояния, которая отображается над областью уведомлений Windows, сообщается о том, что приложение запускается.</span><span class="sxs-lookup"><span data-stu-id="12194-138">A status bar, displayed above the Windows notification area, reports that the application is starting.</span></span> <span data-ttu-id="12194-139">При успешном запуске приложения отображается окно заголовка для приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="12194-139">If the application startup is successful, the title screen for the default application is displayed.</span></span> <span data-ttu-id="12194-140">Нажмите кнопку **ОК** , чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="12194-140">Click **OK** to close the dialog box.</span></span> <span data-ttu-id="12194-141">Теперь вы подтвердили правильность работы системы App-V.</span><span class="sxs-lookup"><span data-stu-id="12194-141">You have now confirmed that the App-V system is running correctly.</span></span>

## <span data-ttu-id="12194-142">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="12194-142">Related topics</span></span>


[<span data-ttu-id="12194-143">Настройка серверов для развертывания на основе сервера</span><span class="sxs-lookup"><span data-stu-id="12194-143">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





