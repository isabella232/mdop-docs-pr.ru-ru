---
title: Установка клиента MED-V и консоли управления MED-V
description: Установка клиента MED-V и консоли управления MED-V
author: dansimp
ms.assetid: 8a5f3010-3a50-487e-99d8-e352e5cb51c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a486cc7cf5534171f80b08dc93742e03cd4a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826982"
---
# <span data-ttu-id="277c6-103">Установка клиента MED-V и консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="277c6-103">How to Install MED-V Client and MED-V Management Console</span></span>


<span data-ttu-id="277c6-104">В пакет Client. msi включены следующие компоненты MED-V:</span><span class="sxs-lookup"><span data-stu-id="277c6-104">The following MED-V components are included in the client .msi package:</span></span>

-   <span data-ttu-id="277c6-105">Клиент MED-v — программное обеспечение для MED-v, которое должно быть установлено на клиентских компьютерах для работы с рабочими областями MED-V.</span><span class="sxs-lookup"><span data-stu-id="277c6-105">MED-V client—The MED-V software that must be installed on client computers for running MED-V workspaces.</span></span>

-   <span data-ttu-id="277c6-106">Консоль управления MED-V — средство администрирования, которое администраторы могут использовать для создания и обслуживания изображений, рабочих областей MED-V и политик.</span><span class="sxs-lookup"><span data-stu-id="277c6-106">MED-V management console—The administrative tool that administrators can use to create and maintain images, MED-V workspaces, and policies.</span></span>

<span data-ttu-id="277c6-107">Консоль управления MED-V и клиент MED-V устанавливаются из пакета Client. msi для MED-v.</span><span class="sxs-lookup"><span data-stu-id="277c6-107">The MED-V management console and the MED-V client are both installed from the MED-V client .msi package.</span></span> <span data-ttu-id="277c6-108">Однако клиент MED-V может устанавливаться независимо без консоли управления MED-V, сняв флажок **установить приложение управления med-v** во время установки.</span><span class="sxs-lookup"><span data-stu-id="277c6-108">The MED-V client, however, can be installed independently without the MED-V management console by clearing the **Install the MED-V Management application** check box during installation.</span></span>

**<span data-ttu-id="277c6-109">Примечание.</span><span class="sxs-lookup"><span data-stu-id="277c6-109">Note</span></span>**  
<span data-ttu-id="277c6-110">Клиент MED-V и консоль управления MED-V можно установить только на компьютерах с Windows 7, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="277c6-110">The MED-V client and MED-V management console can only be installed on Windows 7-, Windows Vista-, and Windows XP-based computers.</span></span> <span data-ttu-id="277c6-111">Они не могут быть установлены на серверные продукты.</span><span class="sxs-lookup"><span data-stu-id="277c6-111">They cannot be installed on server products.</span></span>



**<span data-ttu-id="277c6-112">Примечание.</span><span class="sxs-lookup"><span data-stu-id="277c6-112">Note</span></span>**  
<span data-ttu-id="277c6-113">Не устанавливайте клиент MED-V с помощью команды Windows **runas** .</span><span class="sxs-lookup"><span data-stu-id="277c6-113">Do not install the MED-V client using the Windows **runas** command.</span></span>



**<span data-ttu-id="277c6-114">Установка клиента MED-V</span><span class="sxs-lookup"><span data-stu-id="277c6-114">To install the MED-V client</span></span>**

1.  <span data-ttu-id="277c6-115">Войдите в систему как пользователь с правами локального администратора на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="277c6-115">Log in as a user with local administrator rights on the local computer.</span></span>

2.  <span data-ttu-id="277c6-116">Запустите пакет для MED-V. msi.</span><span class="sxs-lookup"><span data-stu-id="277c6-116">Run the MED-V .msi package.</span></span>

    <span data-ttu-id="277c6-117">Пакет для MED-V. msi называется *MED-V\_x.msi*, где *x* — номер версии.</span><span class="sxs-lookup"><span data-stu-id="277c6-117">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="277c6-118">Например, *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="277c6-118">For example, *MED-V\_1.0.65.msi*.</span></span>

3.  <span data-ttu-id="277c6-119">После появления экрана **приветствия мастера InstallShield** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="277c6-119">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

4.  <span data-ttu-id="277c6-120">На экране лицензионного **соглашения** ознакомьтесь с лицензионным соглашением, выберите **я принимаю условия лицензионного соглашения**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="277c6-120">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and click **Next**.</span></span>

    <span data-ttu-id="277c6-121">Откроется экран **Конечная папка** с отображаемой папкой "Установка по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="277c6-121">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="277c6-122">По умолчанию выбрана папка, в которой установлена операционная система.</span><span class="sxs-lookup"><span data-stu-id="277c6-122">The default installation folder is the directory where the operating system is installed.</span></span>

    -   <span data-ttu-id="277c6-123">Чтобы изменить папку, в которой должна быть установлена версия MED-V, нажмите кнопку **изменить**и перейдите к существующей папке.</span><span class="sxs-lookup"><span data-stu-id="277c6-123">To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.</span></span>

5.  <span data-ttu-id="277c6-124">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="277c6-124">Click **Next**.</span></span>

6.  <span data-ttu-id="277c6-125">На экране **Параметры med-v** Настройте установку med-v следующим образом:</span><span class="sxs-lookup"><span data-stu-id="277c6-125">On the **MED-V Settings** screen, configure the MED-V installation as follows:</span></span>

    -   <span data-ttu-id="277c6-126">Установите флажок **установить приложение для управления MED-V** , чтобы включить в установку компонент управления.</span><span class="sxs-lookup"><span data-stu-id="277c6-126">Select the **Install the MED-V management application** check box to include the management component in the installation.</span></span>

        **<span data-ttu-id="277c6-127">Примечание.</span><span class="sxs-lookup"><span data-stu-id="277c6-127">Note</span></span>**  
        <span data-ttu-id="277c6-128">Администраторам виртуализации корпоративных рабочих столов следует установить приложение для управления MED-V.</span><span class="sxs-lookup"><span data-stu-id="277c6-128">Enterprise Desktop Virtualization administrators should install the MED-V management application.</span></span> <span data-ttu-id="277c6-129">Это приложение требуется для настройки настольных образов и рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="277c6-129">This application is required for configuring desktop images and MED-V workspaces.</span></span>



~~~
-   Select the **Load MED-V when Windows starts** check box to start MED-V automatically on startup.

-   Select the **Add a MED-V shortcut to my desktop** check box to create a MED-V shortcut on your desktop.

-   In the **Server address** field, type the server address.

-   In the **Server port** field, type the server's port.

-   Select the **Server requires encrypted connections (https)** check box to work with https.

-   The default virtual machine images folder is displayed. The default installation folder is *%systemdrive%\\MED-V Images\\*. To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.
~~~

7. <span data-ttu-id="277c6-130">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="277c6-130">Click **Next**.</span></span>

8. <span data-ttu-id="277c6-131">На экране **Готово для установки программы** нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="277c6-131">On the **Ready to Install the Program** screen, click **Install**.</span></span>

   <span data-ttu-id="277c6-132">Запустится установка клиента MED-V.</span><span class="sxs-lookup"><span data-stu-id="277c6-132">The MED-V client installation starts.</span></span> <span data-ttu-id="277c6-133">Это может занять несколько минут, и на экране может не отображаться текст.</span><span class="sxs-lookup"><span data-stu-id="277c6-133">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="277c6-134">Во время установки появляются несколько экранов хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="277c6-134">During installation, several progress screens appear.</span></span> <span data-ttu-id="277c6-135">Если появится сообщение, следуйте инструкциям, приведенным в этой области.</span><span class="sxs-lookup"><span data-stu-id="277c6-135">If a message appears, follow the instructions provided.</span></span>

   <span data-ttu-id="277c6-136">После успешной установки появится окно **мастера InstallShield с заполненным** экраном.</span><span class="sxs-lookup"><span data-stu-id="277c6-136">Upon successful installation, the **InstallShield Wizard Completed** screen appears.</span></span>

9. <span data-ttu-id="277c6-137">Нажмите кнопку **Готово** , чтобы закрыть окно мастера.</span><span class="sxs-lookup"><span data-stu-id="277c6-137">Click **Finish** to close the wizard.</span></span>

## <span data-ttu-id="277c6-138">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="277c6-138">Related topics</span></span>


[<span data-ttu-id="277c6-139">Поддерживаемые конфигурации</span><span class="sxs-lookup"><span data-stu-id="277c6-139">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="277c6-140">Контрольные списки установки и обновления</span><span class="sxs-lookup"><span data-stu-id="277c6-140">Installation and Upgrade Checklists</span></span>](installation-and-upgrade-checklists.md)









