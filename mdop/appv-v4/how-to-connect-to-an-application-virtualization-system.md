---
title: Подключение к системе Application Virtualization System
description: Подключение к системе Application Virtualization System
author: dansimp
ms.assetid: ac38216c-5464-4c0b-a4d3-3949ba6358ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 30d60e187e1b7595fd0dce6641fa027a1df68f3d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817712"
---
# <span data-ttu-id="85ae9-103">Подключение к системе Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="85ae9-103">How to Connect to an Application Virtualization System</span></span>


<span data-ttu-id="85ae9-104">Вы должны подключить консоль управления сервера виртуализации приложений к системе виртуализации приложений, прежде чем использовать консоль управления для управления приложениями, связями с типами файлов, пакетами, лицензиями на приложения, группами серверов, политиками поставщиков и администраторами.</span><span class="sxs-lookup"><span data-stu-id="85ae9-104">You must connect the Application Virtualization Server Management Console to an Application Virtualization System before you can use the management console to manage applications, file type associations, packages, application licenses, server groups, provider policies and administrators.</span></span> <span data-ttu-id="85ae9-105">Ниже описаны действия, которые необходимо выполнить, чтобы подключить консоль к системе виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="85ae9-105">The following procedure outlines the steps you must follow to connect the console to an Application Virtualization System.</span></span>

**<span data-ttu-id="85ae9-106">Подключение к системе виртуализации приложений</span><span class="sxs-lookup"><span data-stu-id="85ae9-106">To connect to an Application Virtualization System</span></span>**

1. <span data-ttu-id="85ae9-107">Щелкните правой кнопкой мыши узел системы Application Virtualization в области **область** , а затем в контекстном меню выберите пункт **подключиться к системе виртуализации приложений** .</span><span class="sxs-lookup"><span data-stu-id="85ae9-107">Right-click the Application Virtualization System node in the **Scope** pane, and select **Connect to Application Virtualization System** from the pop-up menu.</span></span>

   **<span data-ttu-id="85ae9-108">Примечание.</span><span class="sxs-lookup"><span data-stu-id="85ae9-108">Note</span></span>**  
   <span data-ttu-id="85ae9-109">Управление сервером виртуализации приложений включает три компонента: консоль управления виртуализацией приложений, веб-служба управления и хранилище SQL.</span><span class="sxs-lookup"><span data-stu-id="85ae9-109">There are three components to Application Virtualization server management: the Application Virtualization Management Console, the Management Web Service, and the SQL Datastore.</span></span> <span data-ttu-id="85ae9-110">Если эти компоненты распределены на разных физических компьютерах, необходимо правильно настроить параметры безопасности, чтобы компоненты могли взаимодействовать через систему.</span><span class="sxs-lookup"><span data-stu-id="85ae9-110">If these components are distributed across different physical machines, you must configure security properly for the components to communicate across the system.</span></span> <span data-ttu-id="85ae9-111">Дополнительные сведения можно найти в следующих руководствах и статьях:</span><span class="sxs-lookup"><span data-stu-id="85ae9-111">For more information, see the following manuals and articles:</span></span>

   <span data-ttu-id="85ae9-112">[Настройка доверия сервера для делегирования](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)</span><span class="sxs-lookup"><span data-stu-id="85ae9-112">[How to Configure the Server to be Trusted for Delegation](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)</span></span>

   <span data-ttu-id="85ae9-113">[Руководство по планированию и развертыванию системы виртуализации приложений](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)</span><span class="sxs-lookup"><span data-stu-id="85ae9-113">[Planning and Deployment Guide for the Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)</span></span>

   <span data-ttu-id="85ae9-114">[Руководство по эксплуатации для системы виртуализации приложений](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)</span><span class="sxs-lookup"><span data-stu-id="85ae9-114">[Operations Guide for the Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)</span></span>

   <span data-ttu-id="85ae9-115">[Статья 930472](https://go.microsoft.com/fwlink/?LinkId=114647) базы знаний Майкрософт (https://go.microsoft.com/fwlink/?LinkId=114647)</span><span class="sxs-lookup"><span data-stu-id="85ae9-115">[Article 930472](https://go.microsoft.com/fwlink/?LinkId=114647) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114647)</span></span>

   <span data-ttu-id="85ae9-116">[Статья 930565](https://go.microsoft.com/fwlink/?LinkId=114648) базы знаний Майкрософт (https://go.microsoft.com/fwlink/?LinkId=114648)</span><span class="sxs-lookup"><span data-stu-id="85ae9-116">[Article 930565](https://go.microsoft.com/fwlink/?LinkId=114648) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114648)</span></span>

     

2. <span data-ttu-id="85ae9-117">Заполните поля в диалоговом окне " **Подключение к системе виртуализации приложений** ".</span><span class="sxs-lookup"><span data-stu-id="85ae9-117">Complete the fields in the **Connect to Application Virtualization System** dialog box:</span></span>

   1. <span data-ttu-id="85ae9-118">**Имя узла веб-службы**— введите имя системы виртуализации приложений, к которой вы хотите подключиться, или введите **localhost** для подключения к локальному серверу.</span><span class="sxs-lookup"><span data-stu-id="85ae9-118">**Web Service Host Name**—Enter the name of the Application Virtualization System to which you want to connect, or enter **localhost** to connect to the local server.</span></span>

   2. <span data-ttu-id="85ae9-119">**Использовать безопасное соединение**— установите этот флажок, если вы хотите подключиться к серверу с помощью безопасного соединения.</span><span class="sxs-lookup"><span data-stu-id="85ae9-119">**Use Secure Connection**—Select this check box if you want to connect to the server with a secure connection.</span></span>

   3. <span data-ttu-id="85ae9-120">**Port (порт**) — введите номер порта, который вы хотите использовать для подключения.</span><span class="sxs-lookup"><span data-stu-id="85ae9-120">**Port**—Enter the port number you want to use for the connection.</span></span> <span data-ttu-id="85ae9-121">**80** является стандартным номером порта по умолчанию, а **443** — номер защищенного порта.</span><span class="sxs-lookup"><span data-stu-id="85ae9-121">**80** is the default regular port number, and **443** is the secure-port number.</span></span>

   4. <span data-ttu-id="85ae9-122">**Использовать текущую учетную запись Windows**— выберите этот переключатель, чтобы использовать учетные данные текущей учетной записи Windows.</span><span class="sxs-lookup"><span data-stu-id="85ae9-122">**Use Current Windows Account**—Select this radio button to use the current Windows account credentials.</span></span>

   5. <span data-ttu-id="85ae9-123">**Укажите учетную запись Windows**— выберите этот переключатель, если вы хотите подключиться к серверу в качестве другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="85ae9-123">**Specify Windows Account**—Select this radio button when you want to connect to the server as a different user.</span></span>

   6. <span data-ttu-id="85ae9-124">**Name (имя**) — введите имя нового пользователя, используя либо *DOMAIN\\username* , либо <em> Формат username@domain </em> .</span><span class="sxs-lookup"><span data-stu-id="85ae9-124">**Name**—Enter the name of the new user by using either the *DOMAIN\\username* or the <em>username@domain</em> format.</span></span>

   7. <span data-ttu-id="85ae9-125">**Password (пароль**). Введите пароль, соответствующий новому пользователю.</span><span class="sxs-lookup"><span data-stu-id="85ae9-125">**Password**—Enter the password that corresponds to the new user.</span></span>

3. <span data-ttu-id="85ae9-126">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="85ae9-126">Click **OK**.</span></span>

## <span data-ttu-id="85ae9-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="85ae9-127">Related topics</span></span>


[<span data-ttu-id="85ae9-128">Выполнение задач администрирования на консоли управления серверами Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="85ae9-128">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





