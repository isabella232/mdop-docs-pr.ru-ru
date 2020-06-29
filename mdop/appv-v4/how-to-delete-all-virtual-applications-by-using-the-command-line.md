---
title: Удаление всех виртуальных приложений с помощью командной строки
description: Удаление всех виртуальных приложений с помощью командной строки
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817539"
---
# <span data-ttu-id="0863b-103">Удаление всех виртуальных приложений с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="0863b-103">How to Delete All Virtual Applications by Using the Command Line</span></span>


<span data-ttu-id="0863b-104">Вы можете удалить все виртуальные приложения с определенного компьютера с помощью описанной ниже процедуры.</span><span class="sxs-lookup"><span data-stu-id="0863b-104">You can use the following procedure to delete all virtual applications from a specific computer.</span></span>

<span data-ttu-id="0863b-105">**Примечание**  Когда все приложения удаляются из пакета, клиент Application Virtualization (App-V) также удаляет пакет.</span><span class="sxs-lookup"><span data-stu-id="0863b-105">**Note** When all applications are deleted from a package, the Application Virtualization (App-V) Client also deletes the package.</span></span>

 

**<span data-ttu-id="0863b-106">Удаление всех приложений</span><span class="sxs-lookup"><span data-stu-id="0863b-106">To delete all applications</span></span>**

-   <span data-ttu-id="0863b-107">Чтобы удалить все приложения для учетной записи пользователя, для которой выполняется команда, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0863b-107">Run the following command to delete all applications for the user account under which the command is run.</span></span> <span data-ttu-id="0863b-108">Если вы выполняете команду с дополнительным параметром/GLOBAL, используя учетную запись с правами администратора, все приложения удаляются для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="0863b-108">If you run the command with the optional /GLOBAL switch, using an account with administrative rights, all applications are deleted for all users.</span></span>

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    <span data-ttu-id="0863b-109">**Примечание**  Когда все приложения удаляются из пакета, клиент Application Virtualization (App-V) также удаляет пакет.</span><span class="sxs-lookup"><span data-stu-id="0863b-109">**Note** When all applications are deleted from a package, the Application Virtualization (App-V) Client also deletes the package.</span></span>

     

## <span data-ttu-id="0863b-110">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0863b-110">Related topics</span></span>


[<span data-ttu-id="0863b-111">Добавление пакета с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="0863b-111">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="0863b-112">Удаление пакета с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="0863b-112">How to Remove a Package by Using the Command Line</span></span>](how-to-remove-a-package-by-using-the-command-line.md)

 

 





