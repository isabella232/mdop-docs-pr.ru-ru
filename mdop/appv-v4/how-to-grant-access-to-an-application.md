---
title: Предоставление доступа к приложению
description: Предоставление доступа к приложению
author: dansimp
ms.assetid: e54d9e84-21f5-488f-b040-25f374d9289f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9cd3dfe4661f09bb7e7d3514a397955cb892be81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817432"
---
# <span data-ttu-id="39bb5-103">Предоставление доступа к приложению</span><span class="sxs-lookup"><span data-stu-id="39bb5-103">How to Grant Access to an Application</span></span>


<span data-ttu-id="39bb5-104">Администратор может использовать консоль управления сервером Application Virtualization, чтобы определить, какие пользователи могут получать доступ к приложениям.</span><span class="sxs-lookup"><span data-stu-id="39bb5-104">As the administrator, you can use the Application Virtualization Server Management Console to determine which users can access which applications.</span></span> <span data-ttu-id="39bb5-105">Это можно сделать при импорте проекта секвенсора (SPRJ) или открытого файла дескриптора программного обеспечения (OSD) или в любое время с помощью диалогового окна **Свойства** приложения.</span><span class="sxs-lookup"><span data-stu-id="39bb5-105">You can do this when you import the Sequencer Project (SPRJ) or Open Software Descriptor (OSD) file or at anytime using the application's **Properties** dialog box.</span></span> <span data-ttu-id="39bb5-106">В обоих методах добавьте пользователей с помощью параметров **разрешений на доступ** .</span><span class="sxs-lookup"><span data-stu-id="39bb5-106">With both methods, use the **Access Permissions** options to add users.</span></span>

**<span data-ttu-id="39bb5-107">Предоставление доступа к приложению</span><span class="sxs-lookup"><span data-stu-id="39bb5-107">To grant access to an application</span></span>**

1.  <span data-ttu-id="39bb5-108">Для существующего приложения щелкните узел **приложения** на левой панели.</span><span class="sxs-lookup"><span data-stu-id="39bb5-108">For an existing application, click the **Applications** node in the left pane.</span></span> <span data-ttu-id="39bb5-109">Щелкните правой кнопкой мыши приложение на правой панели и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="39bb5-109">Right-click an application in the right pane, and choose **Properties**.</span></span>

2.  <span data-ttu-id="39bb5-110">Откройте вкладку **разрешения на доступ** .</span><span class="sxs-lookup"><span data-stu-id="39bb5-110">Select the **Access Permissions** tab.</span></span>

3.  <span data-ttu-id="39bb5-111">Чтобы добавить группы пользователей, нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="39bb5-111">To add user groups, click **Add**.</span></span>

4.  <span data-ttu-id="39bb5-112">В диалоговом окне **Добавление и изменение группы пользователей** перейдите к группе Пользователи.</span><span class="sxs-lookup"><span data-stu-id="39bb5-112">In the **Add/Edit User Group** dialog box, navigate to the user group.</span></span> <span data-ttu-id="39bb5-113">Вы также можете указать домен и группу, введя данные в соответствующие поля.</span><span class="sxs-lookup"><span data-stu-id="39bb5-113">You can also enter the domain and group by typing the information in the respective fields.</span></span>

5.  <span data-ttu-id="39bb5-114">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="39bb5-114">Click **OK**.</span></span> <span data-ttu-id="39bb5-115">Вы можете добавить другие группы с одинаковыми страницами.</span><span class="sxs-lookup"><span data-stu-id="39bb5-115">You can add other groups with the same pages.</span></span>

6.  <span data-ttu-id="39bb5-116">После появления мастера нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="39bb5-116">When the wizard reappears, click **OK**.</span></span>

    <span data-ttu-id="39bb5-117">**Примечание**  Прежде чем приступить к предоставлению доступа к приложениям, необходимо настроить группы в доменных службах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="39bb5-117">**Note** You must set up your groups in Active Directory Domain Services before you attempt to grant access to applications.</span></span>

     

## <span data-ttu-id="39bb5-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="39bb5-118">Related topics</span></span>


[<span data-ttu-id="39bb5-119">Запрет доступа к приложению</span><span class="sxs-lookup"><span data-stu-id="39bb5-119">How to Deny Access to an Application</span></span>](how-to-deny-access-to-an-application.md)

[<span data-ttu-id="39bb5-120">Управление группами приложений на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="39bb5-120">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="39bb5-121">Управление лицензиями приложений на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="39bb5-121">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="39bb5-122">Добавление приложения вручную</span><span class="sxs-lookup"><span data-stu-id="39bb5-122">How to Manually Add an Application</span></span>](how-to-manually-add-an-application.md)

 

 





