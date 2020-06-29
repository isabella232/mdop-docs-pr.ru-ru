---
title: Страница "Информация о совместном доступе к ускорителям пакетов"
description: Страница "Информация о совместном доступе к ускорителям пакетов"
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819992"
---
# <span data-ttu-id="bbbd9-103">Страница "Информация о совместном доступе к ускорителям пакетов"</span><span class="sxs-lookup"><span data-stu-id="bbbd9-103">About Sharing Package Accelerators Page</span></span>


<span data-ttu-id="bbbd9-104">Ниже приведены сведения о том, как совместно использовать ускорители пакетов.</span><span class="sxs-lookup"><span data-stu-id="bbbd9-104">This following information provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="bbbd9-105">Если вы планируете совместное использование файлов ускорителей пакетов, такие сведения, как имена компьютеров, сведения об учетных записях пользователей и сведения о приложениях, включенных в эти преобразования, могут быть включены в файл ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="bbbd9-105">If you plan to share Package Accelerators files, information such as computer names, user account information, and information about applications included in the transforms might be included in the Package Accelerators file.</span></span> <span data-ttu-id="bbbd9-106">Вы должны просмотреть все параметры и файлы конфигурации, связанные с виртуальным пакетом приложения, чтобы убедиться, что они не содержат персональных данных. Эта страница включает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="bbbd9-106">You should review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.This page contains the following elements.</span></span>

-   <span data-ttu-id="bbbd9-107">**Имя пользователя**.</span><span class="sxs-lookup"><span data-stu-id="bbbd9-107">**Username**.</span></span> <span data-ttu-id="bbbd9-108">При входе в систему на компьютере, на котором запущен Microsoft App-V Sequencer, следует использовать универсальную учетную запись пользователя, например встроенную учетную запись **администратора** .</span><span class="sxs-lookup"><span data-stu-id="bbbd9-108">When you log on to the computer running the Microsoft App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account.</span></span> <span data-ttu-id="bbbd9-109">Не следует использовать учетную запись, которая основывается на существующем имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="bbbd9-109">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="bbbd9-110">**Имя компьютера**.</span><span class="sxs-lookup"><span data-stu-id="bbbd9-110">**Computer Name**.</span></span> <span data-ttu-id="bbbd9-111">Укажите общее неидентифицирующее имя компьютера, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="bbbd9-111">Specify a general, non-identifying name of the computer running the Sequencer.</span></span>

-   <span data-ttu-id="bbbd9-112">**URL-адрес сервера**.</span><span class="sxs-lookup"><span data-stu-id="bbbd9-112">**Server URL**.</span></span> <span data-ttu-id="bbbd9-113">На вкладке " **развертывание** " консоли секвенсора App-V используйте параметры по умолчанию для данных конфигурации URL-адреса сервера.</span><span class="sxs-lookup"><span data-stu-id="bbbd9-113">In the App-V Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="bbbd9-114">**Приложения**.</span><span class="sxs-lookup"><span data-stu-id="bbbd9-114">**Applications**.</span></span> <span data-ttu-id="bbbd9-115">Если вы не хотите предоставлять общий доступ к списку приложений, установленных на компьютере, на котором запущены программы Sequencer при создании ускорителя пакетов, необходимо удалить файл **appv\_manifest.xml** .</span><span class="sxs-lookup"><span data-stu-id="bbbd9-115">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="bbbd9-116">Этот файл находится в корневом каталоге пакета виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="bbbd9-116">This file is located in the package root directory of the virtual application package.</span></span>

## <span data-ttu-id="bbbd9-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="bbbd9-117">Related topics</span></span>


[<span data-ttu-id="bbbd9-118">Мастер создания ускорителя пакетов (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="bbbd9-118">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

[<span data-ttu-id="bbbd9-119">Описание ускорителей пакетов App-V (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="bbbd9-119">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 





