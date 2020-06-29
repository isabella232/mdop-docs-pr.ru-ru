---
title: Установка консоли управления
description: Установка консоли управления
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817302"
---
# <span data-ttu-id="ba0d5-103">Установка консоли управления</span><span class="sxs-lookup"><span data-stu-id="ba0d5-103">How to Install the Management Console</span></span>


<span data-ttu-id="ba0d5-104">Вы можете использовать описанную ниже процедуру, чтобы установить консоль управления Application Virtualization на целевом компьютере в сети.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-104">You can use the following procedure to install the Application Virtualization Management Console on a target computer on the network.</span></span> <span data-ttu-id="ba0d5-105">Необходимо использовать сетевую учетную запись с правами администратора на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-105">You must use a network account that has administrator privileges on the target computer.</span></span> <span data-ttu-id="ba0d5-106">Вы можете использовать консоль для настройки и управления платформой системы виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-106">You can use the console to configure and manage the Application Virtualization System Platform.</span></span>

<span data-ttu-id="ba0d5-107">Перед выполнением этой процедуры необходимо установить веб-службу управления виртуализацией приложений на этом или другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-107">Before you can complete this procedure, you must install the Application Virtualization Management Web Service on this or a different computer.</span></span> <span data-ttu-id="ba0d5-108">Веб-служба управления позволяет получать доступ к хранилищу данных и контроллеру домена.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-108">The Management Web Service allows you to access the data store and the domain controller.</span></span> <span data-ttu-id="ba0d5-109">Дополнительные сведения об установке веб-службы можно найти [в разделе Установка веб-службы управления](how-to-install-the-management-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="ba0d5-109">For more information about installing the Web service, see [How to Install the Management Web Service](how-to-install-the-management-web-service.md).</span></span>

**<span data-ttu-id="ba0d5-110">Установка консоли управления</span><span class="sxs-lookup"><span data-stu-id="ba0d5-110">To install the Management Console</span></span>**

1.  <span data-ttu-id="ba0d5-111">Убедитесь, что на целевом компьютере не установлены предыдущие версии консоли управления.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-111">Verify that no previous versions of the Management Console are installed on the target computer.</span></span>

2.  <span data-ttu-id="ba0d5-112">Перейдите к расположению программы установки системы Application Virtualization в сети, запустите эту программу из сети или скопируйте ее каталог на конечный компьютер, а затем дважды щелкните **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-112">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="ba0d5-113">На **странице приветствия**нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-113">On the **Welcome Page**, click **Next**.</span></span>

4.  <span data-ttu-id="ba0d5-114">На странице Лицензионное **соглашение** для подтверждения лицензионного соглашения установите флажок **я принимаю условия лицензии**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-114">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="ba0d5-115">На странице **регистрационные данные** укажите **имя пользователя** и сведения об **Организации** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-115">On the **Registration Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

6.  <span data-ttu-id="ba0d5-116">На странице **Настройка типа** выберите пункт **Настраиваемая** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-116">On the **Setup Type** page, click **Custom** and then click **Next**.</span></span>

7.  <span data-ttu-id="ba0d5-117">На странице **Выборочная настройка** отмените выбор всех компонентов системы Application Virtualization, кроме **консоли управления**, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-117">On the **Custom Setup** page, deselect all Application Virtualization System components except **Management Console**, and then click **Next**.</span></span>

    <span data-ttu-id="ba0d5-118">**Примечание**  Если компонент уже установлен на компьютере, то после его выбора на экране выборочной настройки он будет автоматически удален.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-118">**Note** If a component is already installed on the computer, by deselecting it on the Custom Setup screen, it will automatically be uninstalled.</span></span>

     

8.  <span data-ttu-id="ba0d5-119">На экране **Готово для изменения программы** нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-119">On the **Ready to Modify the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="ba0d5-120">**Примечание**  Если вы устанавливаете первый устанавливаемый компонент, появится страница **Готово для установки программы** .</span><span class="sxs-lookup"><span data-stu-id="ba0d5-120">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="ba0d5-121">Чтобы начать установку, нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-121">To start the installation, click **Install**.</span></span>

     

9.  <span data-ttu-id="ba0d5-122">На экране **завершения мастера установки** нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-122">On the **Installation Wizard Completed** screen, click **Finish**.</span></span> <span data-ttu-id="ba0d5-123">Нажмите кнопку **ОК** , чтобы перезагрузить компьютер и завершить установку.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-123">Click **Okay** to restart the computer and complete the installation.</span></span>

10. <span data-ttu-id="ba0d5-124">На панели управления Windows дважды щелкните элемент **Администрирование** , а затем выберите **консоль управления Application Virtualization** , чтобы отобразить консоль управления.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-124">In the Windows Control Panel, double-click **Administrative Tools** and then click **Application Virtualization Management Console** to display the Management Console.</span></span>

11. <span data-ttu-id="ba0d5-125">Щелкните значок **подключения** или щелкните правой кнопкой мыши контейнер **системы Application Virtualization** и выберите пункт **подключиться к системе виртуализации приложений**.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-125">Click the **Connect** icon, or right-click the **Application Virtualization Systems** container, and then click **Connect to Application Virtualization System**.</span></span>

12. <span data-ttu-id="ba0d5-126">На экране **Подключение к системе виртуализации приложений** введите имя узла и порт компьютера веб-службы управления, измените сведения о безопасности и учетные данные для входа, если это необходимо, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-126">On the **Connect to Application Virtualization System** screen, enter the host name and port of the Management Web Service computer, change the security information and login credentials if necessary, and then click **OK**.</span></span>

13. <span data-ttu-id="ba0d5-127">После подключения к компьютеру веб-службы управления выберите в меню **консоль** пункт **файл** , а затем — команду **выход**.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-127">After connecting to the Management Web Service computer, click **File** on the **Console** menu, and then click **Exit**.</span></span> <span data-ttu-id="ba0d5-128">Нажмите кнопку **Да** , чтобы сохранить параметры консоли.</span><span class="sxs-lookup"><span data-stu-id="ba0d5-128">Click **Yes** to save console settings.</span></span>

## <span data-ttu-id="ba0d5-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ba0d5-129">Related topics</span></span>


[<span data-ttu-id="ba0d5-130">Установка серверов и компонентов системы</span><span class="sxs-lookup"><span data-stu-id="ba0d5-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





