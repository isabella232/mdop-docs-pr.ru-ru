---
title: Добавление пакета с помощью командной строки
description: Добавление пакета с помощью командной строки
author: dansimp
ms.assetid: e75af49e-811a-407a-a7f0-6de8562b9188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab418017a075300f308d4ef4c6eceb4f623a05c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821409"
---
# <span data-ttu-id="29ecf-103">Добавление пакета с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="29ecf-103">How to Add a Package by Using the Command Line</span></span>


<span data-ttu-id="29ecf-104">Ниже описаны действия, которые необходимо выполнить, чтобы добавить виртуальный пакет приложения в клиент Application Virtualization (App-V) на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="29ecf-104">The following procedures list the steps that are necessary to add a virtual application package to the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="29ecf-105">Добавление виртуального пакета приложения для определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="29ecf-105">To add a virtual application package for a specific user</span></span>**

-   <span data-ttu-id="29ecf-106">Выполните следующую команду под учетной записью пользователя, который должен получить пакет.</span><span class="sxs-lookup"><span data-stu-id="29ecf-106">Run the following command under the user account of the person who is to get the package.</span></span> <span data-ttu-id="29ecf-107">Команда добавляет и публикует пакет для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="29ecf-107">The command adds and publishes the package for that user.</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

**<span data-ttu-id="29ecf-108">Добавление виртуального пакета приложений для всех пользователей</span><span class="sxs-lookup"><span data-stu-id="29ecf-108">To add a virtual application package for all users</span></span>**

-   <span data-ttu-id="29ecf-109">Выполните следующую команду под учетной записью с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="29ecf-109">Run the following command under an account that has administrator rights.</span></span> <span data-ttu-id="29ecf-110">Пакеты добавляются и публикуются для всех пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="29ecf-110">The package is added and published for all users on the computer.</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

**<span data-ttu-id="29ecf-111">Добавление пакета с помощью электронной системы распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="29ecf-111">To add a package using an electronic software distribution system</span></span>**

1.  <span data-ttu-id="29ecf-112">Если вы используете электронную систему распространения программного обеспечения, которая выполняет команды в **системной** учетной записи компьютера, пакет публикуется только для этой учетной записи, если не используется параметр/Global.</span><span class="sxs-lookup"><span data-stu-id="29ecf-112">If you are using an electronic software distribution system that runs the commands under the computer’s **SYSTEM** account, the package is published for that account only, unless you use the /GLOBAL switch.</span></span> <span data-ttu-id="29ecf-113">Чтобы добавить и опубликовать пакет для всех пользователей на компьютере, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="29ecf-113">Run the following command to add and publish the package for all users on the computer:</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

2.  

    <span data-ttu-id="29ecf-114">Если вы хотите добавить пакет только для определенных пользователей, выполните команду **Add Package (добавить пакет** ), а затем явно опубликуйте пакет для каждого пользователя, выполнив следующую команду **публикации** в соответствии с учетной записью каждого пользователя:</span><span class="sxs-lookup"><span data-stu-id="29ecf-114">If you want to add the package for specific users only, run the **ADD PACKAGE** command, and then explicitly publish the package for each user by running the following **PUBLISH PACKAGE** command under each person’s user account:</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

    `SFTMIME PUBLISH PACKAGE:”name” /MANIFEST <manifest-path>`

    <span data-ttu-id="29ecf-115">Публикация пакета без глобального параметра предоставляет пользователю доступ к приложениям в пакете и публикует типы файлов и ярлыки, указанные в манифесте, в профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="29ecf-115">Publishing the package without the GLOBAL parameter grants the user access to the applications in the package and publishes the file types and shortcuts that are listed in the manifest to the user’s profile.</span></span> <span data-ttu-id="29ecf-116">Требуются разрешения: "Управление сопоставлениями типов файлов" (**ManageTypes**) и "ярлыки публикации" (**PublishShortcut**).</span><span class="sxs-lookup"><span data-stu-id="29ecf-116">Permissions required are “Manage file type associations” (**ManageTypes**) and “Publish shortcuts” (**PublishShortcut**).</span></span>

## <span data-ttu-id="29ecf-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="29ecf-117">Related topics</span></span>


[<span data-ttu-id="29ecf-118">Удаление всех виртуальных приложений с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="29ecf-118">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

[<span data-ttu-id="29ecf-119">Удаление пакета с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="29ecf-119">How to Remove a Package by Using the Command Line</span></span>](how-to-remove-a-package-by-using-the-command-line.md)

 

 





