---
title: Настройка разрешений для пользователей
description: Настройка разрешений для пользователей
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817732"
---
# <span data-ttu-id="4e071-103">Настройка разрешений для пользователей</span><span class="sxs-lookup"><span data-stu-id="4e071-103">How to Configure User Permissions</span></span>


<span data-ttu-id="4e071-104">Вы можете включить и отключить некоторые действия для пользователей, не обладающих правами администратора, изменив значения ключа в разделе " **разрешения** " (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions).</span><span class="sxs-lookup"><span data-stu-id="4e071-104">You can enable and disable some actions for users who do not have administrative rights by editing the key values under the **Permissions** registry key (HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions).</span></span> <span data-ttu-id="4e071-105">Этот раздел главным образом предназначен для предотвращения ошибок пользователей, а не для обеспечения какой-либо особой защиты, так как пользователи с правами администратора могут изменять любые из этих значений ключа.</span><span class="sxs-lookup"><span data-stu-id="4e071-105">This key is primarily designed to help prevent users from making mistakes rather than to provide any special security, because users with administrative rights can edit any of these key values.</span></span> <span data-ttu-id="4e071-106">Ниже приведены инструкции по изменению значений клавиш.</span><span class="sxs-lookup"><span data-stu-id="4e071-106">The following procedures are examples of how to change the key values.</span></span> <span data-ttu-id="4e071-107">Дополнительные сведения о ключах и значениях реестра клиента Application Virtualization (App-V) можно найти в разделе <https://go.microsoft.com/fwlink/?LinkId=121528> .</span><span class="sxs-lookup"><span data-stu-id="4e071-107">For more information about the Application Virtualization (App-V) Client registry keys and values, see <https://go.microsoft.com/fwlink/?LinkId=121528>.</span></span>

**<span data-ttu-id="4e071-108">Изменение разрешений пользователей</span><span class="sxs-lookup"><span data-stu-id="4e071-108">To change user permissions</span></span>**

1.  <span data-ttu-id="4e071-109">Чтобы разрешить пользователям запускать клиент в автономном режиме, задайте для параметра реестра значение 1:</span><span class="sxs-lookup"><span data-stu-id="4e071-109">To enable the users to choose to run the client in offline mode, set the following key value to 1:</span></span>

    <span data-ttu-id="4e071-110">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="4e071-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span></span>

2.  <span data-ttu-id="4e071-111">Чтобы разрешить пользователям просматривать все приложения с помощью пользовательского интерфейса, задайте для параметра значение 1.</span><span class="sxs-lookup"><span data-stu-id="4e071-111">To enable the users to view all applications through the user interface, set the following key value to 1.</span></span> <span data-ttu-id="4e071-112">Если задать для этого параметра значение 0 (ноль), пользователи смогут видеть только те приложения, которые доступны для них.</span><span class="sxs-lookup"><span data-stu-id="4e071-112">Setting the value to 0 (zero) allows the users to see only the applications that are available to them.</span></span>

    <span data-ttu-id="4e071-113">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="4e071-113">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span></span>

## <span data-ttu-id="4e071-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4e071-114">Related topics</span></span>


[<span data-ttu-id="4e071-115">Настройка параметров реестра клиента App-V с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="4e071-115">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[<span data-ttu-id="4e071-116">Разрешения на доступ пользователей в клиенте Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="4e071-116">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





