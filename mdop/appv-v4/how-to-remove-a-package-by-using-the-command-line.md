---
title: Удаление пакета с помощью командной строки
description: Удаление пакета с помощью командной строки
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816822"
---
# <span data-ttu-id="e8243-103">Удаление пакета с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="e8243-103">How to Remove a Package by Using the Command Line</span></span>


<span data-ttu-id="e8243-104">Вы можете использовать следующие процедуры командной строки, чтобы удалить пакет виртуального приложения из клиента Application Virtualization (App-V) на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e8243-104">You can use the following command-line procedures to delete a virtual application package from the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="e8243-105">Удаление виртуального пакета приложений для всех пользователей</span><span class="sxs-lookup"><span data-stu-id="e8243-105">To delete a virtual application package for all users</span></span>**

-   <span data-ttu-id="e8243-106">Если пакет был ранее добавлен для всех пользователей с помощью ключа/GLOBAL, выполните следующую команду, чтобы удалить пакет и глобальные типы файлов и сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="e8243-106">If the package was previously added for all users by using the /GLOBAL switch, use the following command to delete the package and the global file types and shortcuts.</span></span> <span data-ttu-id="e8243-107">Требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="e8243-107">Administrator rights are required.</span></span> <span data-ttu-id="e8243-108">В данном случае переключатель/GLOBAL не требуется, так как команда всегда выполняет глобальное удаление пакета.</span><span class="sxs-lookup"><span data-stu-id="e8243-108">The /GLOBAL switch is not needed in this case because the command always performs a global deletion of the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

**<span data-ttu-id="e8243-109">Удаление пакета, добавленного ранее для отдельных пользователей</span><span class="sxs-lookup"><span data-stu-id="e8243-109">To delete a package previously added for individual users</span></span>**

1.  <span data-ttu-id="e8243-110">Если пакет был ранее добавлен для отдельных пользователей, у вас есть несколько вариантов.</span><span class="sxs-lookup"><span data-stu-id="e8243-110">If the package was previously added for individual users, you have several options.</span></span>

    <span data-ttu-id="e8243-111">Запустите следующую команду один раз под учетной записью пользователя каждого пользователя, которому был опубликован пакет.</span><span class="sxs-lookup"><span data-stu-id="e8243-111">Run the following command once under the user account of each person the package was published to.</span></span> <span data-ttu-id="e8243-112">Это запрещает пользователю доступ к приложениям, если они перемещаются на другой компьютер.</span><span class="sxs-lookup"><span data-stu-id="e8243-112">This denies the user access to the applications if they roam to another computer.</span></span> <span data-ttu-id="e8243-113">Она удаляет параметры, ярлыки и типы файлов из профиля, а также останавливает фоновую загрузку в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="e8243-113">It deletes the specific user’s settings, shortcuts, and file types from the profile, and it stops background loads under the user’s context.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  <span data-ttu-id="e8243-114">Кроме того, вы можете выполнить следующую команду под учетной записью пользователя каждого пользователя, которому был опубликован пакет.</span><span class="sxs-lookup"><span data-stu-id="e8243-114">Alternatively, run the following command under the user account of each person the package was published to.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    <span data-ttu-id="e8243-115">Затем выполните эту команду для пакета.</span><span class="sxs-lookup"><span data-stu-id="e8243-115">Then run this command for the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

    <span data-ttu-id="e8243-116">Этот пакет полностью удаляется, а в профилях удаляются все параметры пользователя, ярлыки и типы файлов.</span><span class="sxs-lookup"><span data-stu-id="e8243-116">This completely removes the package, and it deletes all user settings, shortcuts, and file types from their profiles.</span></span> <span data-ttu-id="e8243-117">Если пакет добавляется повторно, пользователям потребуется снова задать параметры.</span><span class="sxs-lookup"><span data-stu-id="e8243-117">If the package is subsequently re-added, the users will have to specify their settings again.</span></span> <span data-ttu-id="e8243-118">Для выполнения этой команды требуется только разрешение на удаление приложений (**DeleteApp**).</span><span class="sxs-lookup"><span data-stu-id="e8243-118">Only “Delete applications” (**DeleteApp**) permission is needed to run this command.</span></span>

3.  <span data-ttu-id="e8243-119">В качестве третьего варианта можно просто выполнить команду **удалить пакет** , не выполнив команду Отменить **публикацию пакета** .</span><span class="sxs-lookup"><span data-stu-id="e8243-119">As a third alternative, you can simply run the **DELETE PACKAGE** command without using the **UNPUBLISH PACKAGE** command.</span></span> <span data-ttu-id="e8243-120">В этом случае типы файлов и сочетания клавиш для каждого пользователя скрываются, а не удаляются, а пользовательские параметры сохраняются.</span><span class="sxs-lookup"><span data-stu-id="e8243-120">In this case, file types and shortcuts for each user are hidden rather than deleted, and the user settings are retained.</span></span> <span data-ttu-id="e8243-121">Это означает, что при последующем повторном добавлении пакета для пользователя восстанавливаются типы файлов и сочетания клавиш, а пользовательские параметры применяются повторно.</span><span class="sxs-lookup"><span data-stu-id="e8243-121">This means that if the package is subsequently re-added for the user, the file types and shortcuts are restored, and the user settings are reapplied.</span></span>

## <span data-ttu-id="e8243-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e8243-122">Related topics</span></span>


[<span data-ttu-id="e8243-123">Добавление пакета с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="e8243-123">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="e8243-124">Удаление всех виртуальных приложений с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="e8243-124">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 





