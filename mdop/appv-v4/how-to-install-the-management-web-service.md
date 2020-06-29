---
title: Установка веб-службы управления
description: Установка веб-службы управления
author: dansimp
ms.assetid: cac296f5-8ca0-4ce7-afdb-859ae207d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b8cc1b4821cb4041d75003cf7e6ff592e1c5039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817279"
---
# <span data-ttu-id="61fe3-103">Установка веб-службы управления</span><span class="sxs-lookup"><span data-stu-id="61fe3-103">How to Install the Management Web Service</span></span>


<span data-ttu-id="61fe3-104">Выполните указанные ниже действия, чтобы установить веб-службу управления виртуализацией приложений на целевом компьютере в сети с учетной записью, обладающей локальными правами администратора.</span><span class="sxs-lookup"><span data-stu-id="61fe3-104">Use the following procedure to install the Application Virtualization Management Web Service on a target computer on the network, with a logon account having local administrative privileges.</span></span> <span data-ttu-id="61fe3-105">Несмотря на то, что это не обязательно, рекомендуется установить этот компонент на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="61fe3-105">Although it is not required, we recommended that you install this component on your Web server.</span></span>

**<span data-ttu-id="61fe3-106">Установка веб-службы управления</span><span class="sxs-lookup"><span data-stu-id="61fe3-106">To install the Management Web Service</span></span>**

1.  <span data-ttu-id="61fe3-107">Убедитесь, что на целевом компьютере не установлены предыдущие версии веб-службы Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="61fe3-107">Verify that no previous versions of the Application Virtualization Web Service are installed on your target computer.</span></span>

2.  <span data-ttu-id="61fe3-108">Перейдите к расположению программы установки системы Application Virtualization в сети, запустите эту программу из сети или скопируйте ее каталог на конечный компьютер, а затем дважды щелкните **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-108">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="61fe3-109">После открытия мастера установки на странице **приветствия** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-109">After the Installation Wizard opens, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="61fe3-110">На странице Лицензионное **соглашение** для подтверждения лицензионного соглашения установите флажок **я принимаю условия лицензии**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-110">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="61fe3-111">На странице **регистрационные данные** укажите **имя пользователя** и сведения об организации, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-111">On the **Registration Information** page, specify the **User Name** and organization information, and then click **Next**.</span></span>

6.  <span data-ttu-id="61fe3-112">На странице **тип установки** нажмите кнопку **Настраиваемая**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-112">On the **Setup Type** page, click **Custom**, and then click **Next**.</span></span>

    <span data-ttu-id="61fe3-113">**Примечание**  Если это не первый компонент, установленный на этом компьютере, отображается страница **обслуживание программы** .</span><span class="sxs-lookup"><span data-stu-id="61fe3-113">**Note** If this is not the first component you installed on this computer, the **Program Maintenance** page is displayed.</span></span> <span data-ttu-id="61fe3-114">На странице **обслуживание программы** нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-114">On the **Program Maintenance** page, click **Modify**.</span></span>

     

7.  <span data-ttu-id="61fe3-115">На странице **Выборочная настройка** удалите все компоненты системы Application Virtualization, кроме **службы управления virt**, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-115">On the **Custom Setup** page, clear all Application Virtualization System components except **App Virt Management Service**, and then click **Next**.</span></span>

    <span data-ttu-id="61fe3-116">**Примечание**  Если компонент уже установлен на компьютере, его можно будет удалить автоматически, сняв его на странице **выборочной настройки** .</span><span class="sxs-lookup"><span data-stu-id="61fe3-116">**Note** If a component is already installed on the computer, by clearing it on the **Custom Setup** page, you will automatically uninstall it.</span></span>

     

8.  <span data-ttu-id="61fe3-117">На странице **сервер базы данных** нажмите кнопку **подключиться к доступной базе данных**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-117">On the **Database Server** page, click **Connect to available database**, and then click **Next**.</span></span>

    <span data-ttu-id="61fe3-118">**Примечание**  В производственной среде Корпорация Майкрософт считает, что вы будете подключаться к существующей базе данных.</span><span class="sxs-lookup"><span data-stu-id="61fe3-118">**Note** In a production environment, Microsoft assumes that you will connect to an existing database.</span></span> <span data-ttu-id="61fe3-119">Если вы хотите установить базу данных, ознакомьтесь [со сведениями о том, как установить базу данных](how-to-install-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="61fe3-119">If you want to install a database, see [How to Install a Database](how-to-install-a-database.md).</span></span> <span data-ttu-id="61fe3-120">После установки базы данных перейдите к шагу 13.</span><span class="sxs-lookup"><span data-stu-id="61fe3-120">After installing the database, continue with step 13.</span></span>

     

9.  <span data-ttu-id="61fe3-121">На странице **Тип сервера базы данных** выберите из списка тип базы данных и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-121">On the **Database Server Type** page, select a database type from the list, and then click **Next**.</span></span>

10. <span data-ttu-id="61fe3-122">На странице **расположение сервера базы данных** выберите сервер базы данных из списка доступных серверов или добавьте сервер, установив флажок **использовать следующее имя узла** и введя данные в полях **имя сервера** и **номер порта** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-122">On the **Database Server Location** page, select a database server from the list of available servers or add a server by selecting the **Use the following host name** check box and entering information in the **Server Name** and **Port Number** boxes, and then click **Next**.</span></span>

11. <span data-ttu-id="61fe3-123">На странице **Выбор базы данных** выберите нужную базу данных, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-123">On the **Select Database** page, select the database you want, and then click **Next**.</span></span>

12. <span data-ttu-id="61fe3-124">На странице **Конфигурация пользователя базы данных** введите учетные данные, которые веб-служба управления будет использовать для доступа к хранилищу данных, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-124">On the **Database User Configuration** page, enter the credentials that the Management Web Service will use to access the data store, and then click **Next**.</span></span>

13. <span data-ttu-id="61fe3-125">На странице **готовность к изменению программы** нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-125">On the **Ready to Modify the Program** page, click **Install**.</span></span>

    <span data-ttu-id="61fe3-126">**Примечание**  Если вы устанавливаете первый устанавливаемый компонент, появится страница **Готово для установки программы** .</span><span class="sxs-lookup"><span data-stu-id="61fe3-126">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="61fe3-127">На странице нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-127">On the page, click **Install**.</span></span>

     

14. <span data-ttu-id="61fe3-128">На странице " **Мастер установки завершен** " нажмите кнопку **"Готово"**.</span><span class="sxs-lookup"><span data-stu-id="61fe3-128">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

## <span data-ttu-id="61fe3-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="61fe3-129">Related topics</span></span>


[<span data-ttu-id="61fe3-130">Установка серверов и компонентов системы</span><span class="sxs-lookup"><span data-stu-id="61fe3-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





