---
title: Устранение неполадок при развертывании
description: Устранение неполадок при развертывании
author: dansimp
ms.assetid: 9ee980f2-4e77-4020-9f0e-8c2ffdc390ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe9677175c9538bc070d2adea17a96351397d9a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822899"
---
# <span data-ttu-id="6be4d-103">Устранение неполадок при развертывании</span><span class="sxs-lookup"><span data-stu-id="6be4d-103">Deployment Troubleshooting</span></span>


<span data-ttu-id="6be4d-104">В этой статье приведены сведения, которые помогут вам устранить проблемы с развертыванием в Microsoft Enterprise Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="6be4d-104">This topic includes information to help you troubleshoot deployment issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="6be4d-105">Проблемы, связанные с устранением неполадок при развертывании MED-V</span><span class="sxs-lookup"><span data-stu-id="6be4d-105">Troubleshooting Issues in MED-V Deployment</span></span>


<span data-ttu-id="6be4d-106">При развертывании MED-V может возникнуть следующая ошибка.</span><span class="sxs-lookup"><span data-stu-id="6be4d-106">The following issue might occur when you deploy MED-V.</span></span> <span data-ttu-id="6be4d-107">Решение поможет устранить эту проблему.</span><span class="sxs-lookup"><span data-stu-id="6be4d-107">The solution helps troubleshoot this issue.</span></span>

**<span data-ttu-id="6be4d-108">Проблемы, возникающие при установке MED-V только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="6be4d-108">Problems Occur if Installing MED-V for Current User Only.</span></span>** <span data-ttu-id="6be4d-109">В целях MED-V для всех пользователей поддерживается только установка диспетчера рабочих областей MED-V, агента хоста MED-v и рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="6be4d-109">MED-V only supports the installation of the MED-V Workspace Packager, the MED-V Host Agent, and the MED-V workspace for all users.</span></span> <span data-ttu-id="6be4d-110">Установка для текущего пользователя приводит к сбоям при установке компонентов и настройке рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="6be4d-110">Installing for the current user only causes failures in the installation of the components and in the setup of the MED-V workspace.</span></span>

**<span data-ttu-id="6be4d-111">Решение</span><span class="sxs-lookup"><span data-stu-id="6be4d-111">Solution</span></span>**

<span data-ttu-id="6be4d-112">Никогда не используйте параметр **ALLUSERS = ""** при установке компонентов MED-V.</span><span class="sxs-lookup"><span data-stu-id="6be4d-112">Never use the option **ALLUSERS=””** when installing the MED-V components.</span></span>

**<span data-ttu-id="6be4d-113">Для MED-V требуется эксклюзивное использование стека виртуализации.</span><span class="sxs-lookup"><span data-stu-id="6be4d-113">MED-V Requires Exclusive Use of the Virtualization Stack.</span></span>** <span data-ttu-id="6be4d-114">На компьютере может выполняться только один стек виртуализации.</span><span class="sxs-lookup"><span data-stu-id="6be4d-114">Only one virtualization stack can be run at a time on a computer.</span></span> <span data-ttu-id="6be4d-115">Для Windows Virtual PC требуется виртуальная стопка, а MED-V — для Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="6be4d-115">Windows Virtual PC must use the virtual stack, and MED-V depends on Windows Virtual PC.</span></span> <span data-ttu-id="6be4d-116">Таким образом, если вы попытаетесь развернуть или использовать MED-V, когда запущены другие приложения, использующие виртуальный стек, MED-V не удается запустить или установить его успешно.</span><span class="sxs-lookup"><span data-stu-id="6be4d-116">Therefore, if you try to deploy or use MED-V when other applications are running that use the virtual stack, MED-V cannot run or be successfully installed.</span></span>

**<span data-ttu-id="6be4d-117">Решение</span><span class="sxs-lookup"><span data-stu-id="6be4d-117">Solution</span></span>**

<span data-ttu-id="6be4d-118">Закройте все запущенные приложения, использующие стек виртуализации, прежде чем устанавливать или запускать MED-V.</span><span class="sxs-lookup"><span data-stu-id="6be4d-118">Close any application that is running that uses the virtualization stack before you install or run MED-V.</span></span>

**<span data-ttu-id="6be4d-119">После удаления остались сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="6be4d-119">Shortcuts Remain after Uninstall.</span></span>** <span data-ttu-id="6be4d-120">По умолчанию при удалении MED-V удаляются сочетания клавиш в меню " **Пуск** " конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="6be4d-120">By default, when you uninstall MED-V, shortcuts in the end user’s **Start** menu are removed.</span></span> <span data-ttu-id="6be4d-121">Тем не менее, в некоторых ситуациях, например, для конечных пользователей, использующих перемещаемые профили, ярлыки опубликованных приложений для MED-V остаются в меню " **Пуск** " конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="6be4d-121">However, in certain situations, such as for end users who are running roaming profiles, shortcuts to MED-V published applications remain in the end user’s **Start** menu.</span></span>

**<span data-ttu-id="6be4d-122">Решение</span><span class="sxs-lookup"><span data-stu-id="6be4d-122">Solution</span></span>**

<span data-ttu-id="6be4d-123">Чтобы вручную удалить оставшиеся ярлыки в меню " **Пуск** ", щелкните их правой кнопкой мыши и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="6be4d-123">To manually delete the remaining shortcuts on the **Start** menu, right-click the shortcuts, and then click **Remove**.</span></span>

**<span data-ttu-id="6be4d-124">Отключить параметр групповой политики сообщений при входе в рабочую область для MED-V.</span><span class="sxs-lookup"><span data-stu-id="6be4d-124">Disable Logon Message Group Policy Setting in the MED-V Workspace.</span></span>** <span data-ttu-id="6be4d-125">Если в рабочей области MED-V включено сообщение для входа в Windows XP, конечный пользователь должен войти в систему каждый раз, когда требуется открыть виртуальное приложение MED-V.</span><span class="sxs-lookup"><span data-stu-id="6be4d-125">If the Windows XP logon message is enabled in the MED-V workspace, the end user must log on every time they want to open a MED-V virtual application.</span></span> <span data-ttu-id="6be4d-126">Это приведет к плохому взаимодействию с пользователем.</span><span class="sxs-lookup"><span data-stu-id="6be4d-126">This creates a poor user experience.</span></span>

**<span data-ttu-id="6be4d-127">Решение</span><span class="sxs-lookup"><span data-stu-id="6be4d-127">Solution</span></span>**

<span data-ttu-id="6be4d-128">Отключите следующие параметры групповой политики на виртуальной машине MED-V:</span><span class="sxs-lookup"><span data-stu-id="6be4d-128">Disable the following Group Policy settings in the MED-V virtual machine:</span></span>

**<span data-ttu-id="6be4d-129">Интерактивный вход в систему: текст сообщения для пользователей при входе в систему</span><span class="sxs-lookup"><span data-stu-id="6be4d-129">Interactive logon: Message text for users attempting to log on</span></span>**

**<span data-ttu-id="6be4d-130">Интерактивный вход в систему: заголовок сообщения для пользователей при входе в систему</span><span class="sxs-lookup"><span data-stu-id="6be4d-130">Interactive logon: Message title for users attempting to log on</span></span>**

## <span data-ttu-id="6be4d-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="6be4d-131">Related topics</span></span>


[<span data-ttu-id="6be4d-132">Устранение неполадок в операциях</span><span class="sxs-lookup"><span data-stu-id="6be4d-132">Operations Troubleshooting</span></span>](operations-troubleshooting-medv2.md)

 

 





