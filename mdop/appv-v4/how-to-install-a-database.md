---
title: Установка базы данных
description: Установка базы данных
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817379"
---
# <span data-ttu-id="23614-103">Установка базы данных</span><span class="sxs-lookup"><span data-stu-id="23614-103">How to Install a Database</span></span>


<span data-ttu-id="23614-104">Вы можете использовать описанную ниже процедуру, чтобы установить базу данных для серверного развертывания виртуализации приложений, если база данных еще не доступна.</span><span class="sxs-lookup"><span data-stu-id="23614-104">You can use the following procedure to install a database for your server-based deployment of Application Virtualization if a database is not already available.</span></span> <span data-ttu-id="23614-105">Как правило, в рабочей среде вы будете подключаться к существующей базе данных.</span><span class="sxs-lookup"><span data-stu-id="23614-105">Typically, in a production environment, you will connect to an existing database.</span></span>

<span data-ttu-id="23614-106">**Важно!**  Чтобы установить базу данных, необходимо использовать учетную запись сети с соответствующими разрешениями.</span><span class="sxs-lookup"><span data-stu-id="23614-106">**Important** To install the database, you must use a network account with the appropriate permissions.</span></span> <span data-ttu-id="23614-107">Если в вашей организации требуется, чтобы только администраторы базы данных могли создавать и выполнять обновления баз данных, можно использовать сценарии, позволяющие выполнить эту задачу.</span><span class="sxs-lookup"><span data-stu-id="23614-107">If your organization requires that only database administrators are allowed to create and conduct database upgrades, scripts are available that allow this task to be performed.</span></span>

 

**<span data-ttu-id="23614-108">Установка базы данных</span><span class="sxs-lookup"><span data-stu-id="23614-108">To install a database</span></span>**

1.  <span data-ttu-id="23614-109">Перейдите к расположению программы установки системы Application Virtualization в сети, запустите эту программу из сети или скопируйте ее каталог на конечный компьютер, а затем дважды щелкните **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="23614-109">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

2.  <span data-ttu-id="23614-110">На **странице приветствия**нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="23614-110">On the **Welcome Page**, click **Next**.</span></span>

3.  <span data-ttu-id="23614-111">На странице Лицензионное **соглашение** для подтверждения лицензии выберите **я принимаю условия лицензионного**соглашения и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="23614-111">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and click **Next**.</span></span>

4.  <span data-ttu-id="23614-112">На странице **зарегистрировать сведения** укажите **имя пользователя** и сведения об **Организации** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="23614-112">On the **Registering Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

5.  <span data-ttu-id="23614-113">На странице **Настройка типа** выберите пункт **Настраиваемая** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="23614-113">On the **Setup Type** page, select **Custom** and then click **Next**.</span></span>

6.  <span data-ttu-id="23614-114">На странице **Выборочная настройка** отмените выбор всех компонентов системы Application Virtualization, кроме **сервера Application Virtualization**, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="23614-114">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    <span data-ttu-id="23614-115">**Примечание**  Если компонент уже установлен на компьютере, отмените его выбор на экране **выборочной установки** , и он будет автоматически удален.</span><span class="sxs-lookup"><span data-stu-id="23614-115">**Note** If a component is already installed on the computer, by deselecting it on the **Custom Setup** screen it will automatically be uninstalled.</span></span>

     

7.  <span data-ttu-id="23614-116">На странице **сервер базы данных** введите пароли, назначьте путь установки, сохраните данные и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="23614-116">On the **Database Server** page, type the passwords, assign an installation path, save the information, and click **Next**.</span></span>

8.  <span data-ttu-id="23614-117">Выберите имя базы данных и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="23614-117">Select a name for the database, and then click **Next**.</span></span>

    <span data-ttu-id="23614-118">**Примечание**  Если при попытке выполнить это действие появляется сообщение об ошибке 25109, вы неправильно настроили разрешения, необходимые для установки базы данных.</span><span class="sxs-lookup"><span data-stu-id="23614-118">**Note** If error 25109 is displayed when you try to complete this step, you have incorrectly set up the permissions necessary to install the database.</span></span> <span data-ttu-id="23614-119">Подробные сведения о настройке необходимых разрешений SQL можно найти в разделе <https://go.microsoft.com/fwlink/?LinkId=132144> .</span><span class="sxs-lookup"><span data-stu-id="23614-119">For details on setting up the necessary SQL permissions, please see <https://go.microsoft.com/fwlink/?LinkId=132144>.</span></span>

     

9.  <span data-ttu-id="23614-120">На экране **сервер службы каталогов** введите имя домена и учетные данные, которые будут использоваться серверами Application Virtualization и веб-службой управления, чтобы получить доступ к контроллеру домена, сохраните эти данные, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="23614-120">On the **Directory Server** screen, enter a domain name and credentials that Application Virtualization Servers and the Management Web Service will use to access your domain controller, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="23614-121">**Примечание**  При установке по умолчанию будет использоваться домен текущего компьютера.</span><span class="sxs-lookup"><span data-stu-id="23614-121">**Note** The installation will default to the domain of the current computer.</span></span>

     

10. <span data-ttu-id="23614-122">На странице " **Группа администраторов** " введите имя группы, обладающей правами администратора, сохраните эти данные, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="23614-122">On the **Administrator Group** page, enter the name of a group that will have Administrator privileges, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="23614-123">**Примечание**  Вы также можете ввести несколько первых символов имени группы, у которой есть права на администрирование, нажмите кнопку **Далее**, а затем на экране **Выбор группы администраторов** выберите группу из полученного списка.</span><span class="sxs-lookup"><span data-stu-id="23614-123">**Note** You can also enter the first few characters of the name of a group that will have Administration privileges, click **Next**, and on the **Select Administrator Group** screen, select the group from the resulting list.</span></span> <span data-ttu-id="23614-124">Затем сохраните эти данные и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="23614-124">Then save this information and click **Next**.</span></span>

     

11. <span data-ttu-id="23614-125">На странице " **Группа поставщика по умолчанию** " введите полное имя группы, которая будет управлять доступом к приложениям, сохраните эти данные, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="23614-125">On the **Default Provider Group** page, enter the complete name of a group that will control access to applications, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="23614-126">**Примечание**  Вы также можете ввести первые несколько символов имени группы, которая будет управлять доступом к приложениям, нажмите кнопку **Далее**, а затем на экране **Выбор группы поставщика по умолчанию** выберите группу в списке.</span><span class="sxs-lookup"><span data-stu-id="23614-126">**Note** You can also enter the first few characters of the name of a group that will control access to applications, click **Next**, and on the **Select Default Provider Group** screen, select the group in the list.</span></span> <span data-ttu-id="23614-127">Затем сохраните эти данные и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="23614-127">Then save this information and click **Next**.</span></span>

     

12. <span data-ttu-id="23614-128">На странице **завершения работы мастера установки** нажмите кнопку **Готово**, чтобы закрыть окно мастера.</span><span class="sxs-lookup"><span data-stu-id="23614-128">On the **Installation Wizard Completed** page, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="23614-129">**Важно!**  Для завершения установки может потребоваться несколько минут.</span><span class="sxs-lookup"><span data-stu-id="23614-129">**Important** The installation can take a few minutes to finish.</span></span> <span data-ttu-id="23614-130">Сообщение о состоянии будет мигать над областью уведомлений на рабочем столе Windows, указывая, успешно ли была выполнена установка.</span><span class="sxs-lookup"><span data-stu-id="23614-130">A status message will flash above the Windows desktop notification area, indicating whether the installation succeeded.</span></span>

     

## <span data-ttu-id="23614-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="23614-131">Related topics</span></span>


[<span data-ttu-id="23614-132">Установка серверов и компонентов системы</span><span class="sxs-lookup"><span data-stu-id="23614-132">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





