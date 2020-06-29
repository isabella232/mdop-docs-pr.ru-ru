---
title: Удаление версии пакета
description: Удаление версии пакета
author: dansimp
ms.assetid: a55adb9d-ffa6-4df3-a2d1-5e0c73c35e1b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc77e60ac9745033ae8f074ae71db0cb8517a202
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817562"
---
# <span data-ttu-id="b69a6-103">Удаление версии пакета</span><span class="sxs-lookup"><span data-stu-id="b69a6-103">How to Delete a Package Version</span></span>


<span data-ttu-id="b69a6-104">В консоли управления сервером виртуализации приложений для пакета с несколькими версиями вы можете использовать описанную ниже процедуру для удаления одной или нескольких версий и по-прежнему передавать оставшиеся версии пакета.</span><span class="sxs-lookup"><span data-stu-id="b69a6-104">From the Application Virtualization Server Management Console, for a package that has multiple versions, you can use the following procedure to delete one or more versions and still stream the remaining versions of the package.</span></span> <span data-ttu-id="b69a6-105">Это можно сделать для более эффективного управления файлами на сервере или для удаления устаревшей версии.</span><span class="sxs-lookup"><span data-stu-id="b69a6-105">You might do this to more effectively manage files on the server or to remove an obsolete version.</span></span>

<span data-ttu-id="b69a6-106">**Примечание**  Когда вы решите удалить версию, в поле подтверждения появится напоминание о том, что клиентские компьютеры по-прежнему могут использовать его.</span><span class="sxs-lookup"><span data-stu-id="b69a6-106">**Note** When you choose to delete a version, a confirmation box reminds you that client computers might still be using it.</span></span> <span data-ttu-id="b69a6-107">Перед удалением версии, которая используется, необходимо рекомендовать пользователям выйти и выгрузить все приложения.</span><span class="sxs-lookup"><span data-stu-id="b69a6-107">You should advise users to exit and unload any applications before you remove a version that is in use.</span></span>

 

**<span data-ttu-id="b69a6-108">Удаление версии пакета</span><span class="sxs-lookup"><span data-stu-id="b69a6-108">To delete a package version</span></span>**

1.  <span data-ttu-id="b69a6-109">На левой панели консоли управления сервером виртуализации приложений разверните раздел **пакеты**.</span><span class="sxs-lookup"><span data-stu-id="b69a6-109">In the left panel of the Application Virtualization Server Management Console, expand **Packages**.</span></span>

2.  <span data-ttu-id="b69a6-110">Щелкните пакет, содержащий версию, которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="b69a6-110">Click the package that contains the version you want to delete.</span></span>

3.  <span data-ttu-id="b69a6-111">В центральной области щелкните правой кнопкой мыши версию пакета, которую вы хотите удалить, и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="b69a6-111">In the center pane, right-click the version of the package you want to delete and choose **Delete**.</span></span>

4.  <span data-ttu-id="b69a6-112">Прочтите окно подтверждения и нажмите кнопку **Да** , чтобы завершить действие.</span><span class="sxs-lookup"><span data-stu-id="b69a6-112">Read the confirmation window, and click **Yes** to complete the action.</span></span>

    <span data-ttu-id="b69a6-113">**Примечание**  Если у вас есть пользователи в отключенной операции, их приложения будут заменены новыми версиями при следующем подключении к серверам.</span><span class="sxs-lookup"><span data-stu-id="b69a6-113">**Note** If you have users in disconnected operation, their applications will be replaced with the new versions the next time they connect to the servers.</span></span> <span data-ttu-id="b69a6-114">После того как вы убедитесь в том, что все пользователи обновили приложения, вы можете удалить старые версии.</span><span class="sxs-lookup"><span data-stu-id="b69a6-114">After you are sure all users have updated applications, you can delete old versions.</span></span>

     

## <span data-ttu-id="b69a6-115">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b69a6-115">Related topics</span></span>


[<span data-ttu-id="b69a6-116">Удаление пакета</span><span class="sxs-lookup"><span data-stu-id="b69a6-116">How to Delete a Package</span></span>](how-to-delete-a-packageserver.md)

[<span data-ttu-id="b69a6-117">Управление пакетами на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="b69a6-117">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





