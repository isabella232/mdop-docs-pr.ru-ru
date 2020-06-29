---
title: Запрет доступа к приложению
description: Запрет доступа к приложению
author: dansimp
ms.assetid: 14f5e201-7265-462c-b738-57938dc3fc30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a89669ea8c6323023b585d6d58620cd203fc00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817519"
---
# <span data-ttu-id="07d10-103">Запрет доступа к приложению</span><span class="sxs-lookup"><span data-stu-id="07d10-103">How to Deny Access to an Application</span></span>


<span data-ttu-id="07d10-104">Для загрузки и использования приложения пользователи должны находиться в списке **разрешений на доступ** к приложению.</span><span class="sxs-lookup"><span data-stu-id="07d10-104">Users must be in an application's **Access Permissions** list to load and use the application.</span></span> <span data-ttu-id="07d10-105">Несмотря на то, что консоль управления сервером Application Virtualization не поддерживает явное запрещение доступа группы пользователей к приложению, вы можете удалить группы пользователей из свойств приложения, чтобы добиться этого.</span><span class="sxs-lookup"><span data-stu-id="07d10-105">Although the Application Virtualization Server Management Console does not support explicitly denying a user group access to an application, you can remove the user groups from an application’s properties to achieve this.</span></span>

**<span data-ttu-id="07d10-106">Отказ в доступе к приложению</span><span class="sxs-lookup"><span data-stu-id="07d10-106">To deny access to an application</span></span>**

1.  <span data-ttu-id="07d10-107">Для существующего приложения щелкните узел **приложения** на левой панели.</span><span class="sxs-lookup"><span data-stu-id="07d10-107">For an existing application, click the **Applications** node in the left pane.</span></span>

2.  <span data-ttu-id="07d10-108">Щелкните правой кнопкой мыши приложение на правой панели и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="07d10-108">Right-click an application in the right pane, and choose **Properties**.</span></span> <span data-ttu-id="07d10-109">Затем перейдите на вкладку **разрешения доступа** .</span><span class="sxs-lookup"><span data-stu-id="07d10-109">Then select the **Access Permissions** tab.</span></span>

3.  <span data-ttu-id="07d10-110">Чтобы удалить доступ к группе пользователей, выделите группу пользователей и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="07d10-110">To remove access for a user group, highlight the user group and click **Remove**.</span></span>

4.  <span data-ttu-id="07d10-111">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="07d10-111">Click **OK**.</span></span>

    <span data-ttu-id="07d10-112">**Примечание**  Для управления доступом к приложениям вы также можете ограничить число лицензий приложения.</span><span class="sxs-lookup"><span data-stu-id="07d10-112">**Note** To control access to applications, you can also limit the application licenses.</span></span> <span data-ttu-id="07d10-113">Настройка соответствующих групп пользователей в доменных службах Active Directory предоставляет самый простой способ предоставления и запрета доступа к определенным группам пользователей.</span><span class="sxs-lookup"><span data-stu-id="07d10-113">Setting up the proper user groups in Active Directory Domain Services provides the easiest way to grant and deny access to specific sets of users.</span></span>

     

## <span data-ttu-id="07d10-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="07d10-114">Related topics</span></span>


[<span data-ttu-id="07d10-115">Предоставление доступа к приложению</span><span class="sxs-lookup"><span data-stu-id="07d10-115">How to Grant Access to an Application</span></span>](how-to-grant-access-to-an-application.md)

[<span data-ttu-id="07d10-116">Управление лицензиями приложений на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="07d10-116">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="07d10-117">Управление приложениями на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="07d10-117">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





