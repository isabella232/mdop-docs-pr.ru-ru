---
title: Совместимость App-V с Windows AppLocker
description: Совместимость App-V с Windows AppLocker
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822312"
---
# <span data-ttu-id="23c43-103">Совместимость App-V с Windows AppLocker</span><span class="sxs-lookup"><span data-stu-id="23c43-103">App-V Interoperability with Windows AppLocker</span></span>


<span data-ttu-id="23c43-104">Версия 4,5 с пакетом обновления 1 (SP1) для клиента Microsoft Application Virtualization (App-V) поддерживает функцию AppLocker операционной системы Windows 7.</span><span class="sxs-lookup"><span data-stu-id="23c43-104">Version 4.5 SP1 of the Microsoft Application Virtualization (App-V) client supports the AppLocker feature of Windows 7.</span></span> <span data-ttu-id="23c43-105">Функция AppLocker позволяет ИТ – администраторам указывать, какие приложения запрещено запускать на компьютерах.</span><span class="sxs-lookup"><span data-stu-id="23c43-105">The AppLocker feature enables IT administrators to specify which applications are restricted from running on computers.</span></span> <span data-ttu-id="23c43-106">В этом документе описано, как настроить правила AppLocker для работы с виртуальной средой App-V и виртуализированными приложениями.</span><span class="sxs-lookup"><span data-stu-id="23c43-106">This document describes how to configure the AppLocker rules to work with the App-V virtual environment and virtualized applications.</span></span>

<span data-ttu-id="23c43-107">**Примечание**  Прежде чем настраивать правила Windows AppLocker для виртуальных приложений, сначала необходимо включить Windows AppLocker.</span><span class="sxs-lookup"><span data-stu-id="23c43-107">**Note** Windows AppLocker must first be enabled before configuring Windows AppLocker rules for virtual applications.</span></span> <span data-ttu-id="23c43-108">Дополнительные сведения о включении Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .</span><span class="sxs-lookup"><span data-stu-id="23c43-108">For more information about enabling Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) (https://go.microsoft.com/fwlink/?LinkId=156732).</span></span>

 

## <span data-ttu-id="23c43-109">Настройка правил Windows AppLocker для виртуальных приложений</span><span class="sxs-lookup"><span data-stu-id="23c43-109">Configuring Windows AppLocker Rules for Virtual Applications</span></span>


<span data-ttu-id="23c43-110">Локальные администраторы могут создавать правила Windows AppLocker, которые ограничивают выполнение исполняемых файлов программ (exe), файлов установщика Windows (MSI-и MSP-файлов) и сценариев (файлы. PS,. bat,. cmd,. vbs и. js).</span><span class="sxs-lookup"><span data-stu-id="23c43-110">Local administrators can create Windows AppLocker rules that restrict the running of program executables (.exe files), Windows Installer files (.msi and .msp files), and scripts (.ps, .bat, .cmd, .vbs and .js files).</span></span> <span data-ttu-id="23c43-111">Администратор делает это с помощью эталонного компьютера, на котором установлен клиент App-V, и всех необходимых виртуальных приложений, передаваемым в клиентский кэш.</span><span class="sxs-lookup"><span data-stu-id="23c43-111">The administrator does this by using a reference computer that has the App-V client installed and that has all the relevant virtual applications streamed to the client cache.</span></span> <span data-ttu-id="23c43-112">Для создания правил администратор использует раздел Windows AppLocker локальной политики безопасности Microsoft Management Console (MMC) на компьютере-образце.</span><span class="sxs-lookup"><span data-stu-id="23c43-112">The administrator then uses the Windows AppLocker section of the Local Security Policy Microsoft Management Console (MMC) snap-in on the reference computer to create the rules.</span></span>

<span data-ttu-id="23c43-113">При просмотре пути к каталогу или определенному файлу, для которого вы хотите создать правило, вы можете получить доступ к диску App-V, указав путь к скрытому общему доступу.</span><span class="sxs-lookup"><span data-stu-id="23c43-113">When you browse to find a directory path or specific file for which you want to create a rule, you can access the App-V drive by using the path to the hidden share.</span></span> <span data-ttu-id="23c43-114">Например, вы можете перейти на \\\\localhost\\Q $, где диск App-V — это диск Q. Тем не менее, чтобы создать правило, необходимо изменить путь, чтобы удалить ссылку на \\\\localhost\\Q $ и использовать Q:\\.</span><span class="sxs-lookup"><span data-stu-id="23c43-114">For example, you can browse to \\\\localhost\\Q$, where the App-V drive is drive Q. However, to create the rule, you must edit the path to remove the reference to \\\\localhost\\Q$ and use Q:\\ instead.</span></span> <span data-ttu-id="23c43-115">Чтобы получить доступ к файлам приложения, необходимо запускать каждое приложение на компьютере-образце, а для перехода на \\\\localhost\\Q $ требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="23c43-115">You must start each application on the reference computer to access the application’s files, and administrative rights are required to browse to \\\\localhost\\Q$.</span></span>

 

 





