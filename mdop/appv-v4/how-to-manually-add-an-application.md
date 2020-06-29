---
title: Добавление приложения вручную
description: Добавление приложения вручную
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817099"
---
# <span data-ttu-id="b8875-103">Добавление приложения вручную</span><span class="sxs-lookup"><span data-stu-id="b8875-103">How to Manually Add an Application</span></span>


<span data-ttu-id="b8875-104">При добавлении приложения на сервер управления Application Virtualization рекомендуется его импортировать.</span><span class="sxs-lookup"><span data-stu-id="b8875-104">When adding an application to the Application Virtualization Management Server, it is recommended that you import it.</span></span> <span data-ttu-id="b8875-105">Вы можете добавить приложение вручную, но вы должны предоставить точную детальную информацию о приложении, вызываемом в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="b8875-105">You can add an application manually, but you must provide the precise, detailed information about the application called for in this section.</span></span>

**<span data-ttu-id="b8875-106">Добавление нового приложения вручную</span><span class="sxs-lookup"><span data-stu-id="b8875-106">To manually add a new application</span></span>**

1.  <span data-ttu-id="b8875-107">В левой области щелкните правой кнопкой мыши узел **приложения** и выберите команду **создать приложение**.</span><span class="sxs-lookup"><span data-stu-id="b8875-107">In the left pane, right-click the **Applications** node and choose **New Application**.</span></span>

2.  <span data-ttu-id="b8875-108">В **мастере создания приложений**заполните диалоговое окно " **Общие сведения** ".</span><span class="sxs-lookup"><span data-stu-id="b8875-108">In the **New Application Wizard**, complete the **General Information** dialog box:</span></span>

    1.  <span data-ttu-id="b8875-109">**Имя приложения**— введите имя, которое будут видеть пользователи.</span><span class="sxs-lookup"><span data-stu-id="b8875-109">**Application Name**—Type the name you want the users to see.</span></span>

    2.  <span data-ttu-id="b8875-110">**Version (версия**) — введите версию приложения.</span><span class="sxs-lookup"><span data-stu-id="b8875-110">**Version**—Type the application version.</span></span>

    3.  <span data-ttu-id="b8875-111">**Enabled (включено**) — это поле должно быть выбрано для потоковой передачи приложения после его создания.</span><span class="sxs-lookup"><span data-stu-id="b8875-111">**Enabled**—This box must be selected to stream the application after you create it.</span></span>

    4.  <span data-ttu-id="b8875-112">**Описание**— необязательное описание для административного использования.</span><span class="sxs-lookup"><span data-stu-id="b8875-112">**Description**—Type an optional description for administrative use.</span></span>

    5.  <span data-ttu-id="b8875-113">**Путь к OSD**— просмотр сети в файле дескриптора программного обеспечения (OSD) приложения.</span><span class="sxs-lookup"><span data-stu-id="b8875-113">**OSD Path**—Browse the network to the application's Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="b8875-114">Этот файл должен находиться в общей сетевой папке.</span><span class="sxs-lookup"><span data-stu-id="b8875-114">This file must be in a shared network folder.</span></span>

    6.  <span data-ttu-id="b8875-115">**Путь к значку**— найдите ICO-файл приложения.</span><span class="sxs-lookup"><span data-stu-id="b8875-115">**Icon Path**—Browse to the application's ICO file.</span></span>

    7.  <span data-ttu-id="b8875-116">**Группа лицензирования приложений**— если вы настроили группы лицензий, вы можете назначить приложение, выбрав его в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="b8875-116">**Application License Group**—If you have set up license groups, you can assign the application to one by selecting it in the pull-down list.</span></span>

    8.  <span data-ttu-id="b8875-117">**Группа серверов**: если у вас несколько серверов Application Virtualization, вы можете назначить приложение одним из них, выбрав его в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="b8875-117">**Server Group**—If you have multiple Application Virtualization Servers, you can assign the application to one by selecting it in the pull-down list.</span></span>

3.  <span data-ttu-id="b8875-118">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b8875-118">Click **Next**.</span></span>

4.  <span data-ttu-id="b8875-119">В диалоговом окне **Выбор пакета** выберите связанный пакет и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b8875-119">In the **Select Package** dialog box, select the related package and click **Next**.</span></span>

5.  <span data-ttu-id="b8875-120">На экране **опубликованные ярлыки** установите флажки для расположений, в которых вы хотите отображать ярлыки приложений на клиентских компьютерах, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b8875-120">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers and click **Next**.</span></span>

6.  <span data-ttu-id="b8875-121">В окне **сопоставления файлов** можно добавлять в приложение новые сопоставления файлов типов.</span><span class="sxs-lookup"><span data-stu-id="b8875-121">In the **File Associations** screen, you can add new type file associations to this application.</span></span> <span data-ttu-id="b8875-122">Для этого нажмите кнопку **Добавить**, введите расширение (без предшествующей точки), введите описание и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b8875-122">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

7.  <span data-ttu-id="b8875-123">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b8875-123">Click **Next**.</span></span>

8.  <span data-ttu-id="b8875-124">В диалоговом окне **разрешения на доступ** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="b8875-124">In the **Access Permissions** dialog box, click **Add**.</span></span>

9.  <span data-ttu-id="b8875-125">В диалоговом окне **Добавление и изменение группы пользователей** перейдите к группе Пользователи.</span><span class="sxs-lookup"><span data-stu-id="b8875-125">In the **Add/Edit User Group** dialog box, navigate to the user group.</span></span> <span data-ttu-id="b8875-126">Вы также можете указать домен и группу, введя данные в соответствующие поля.</span><span class="sxs-lookup"><span data-stu-id="b8875-126">You can also enter the domain and group by typing the information in the respective fields.</span></span> <span data-ttu-id="b8875-127">По завершении нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b8875-127">When you finish, click **OK**.</span></span> <span data-ttu-id="b8875-128">Вы можете добавить другие группы с одинаковыми страницами.</span><span class="sxs-lookup"><span data-stu-id="b8875-128">You can add other groups with the same pages.</span></span>

10. <span data-ttu-id="b8875-129">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b8875-129">Click **Next**.</span></span>

11. <span data-ttu-id="b8875-130">На экране **Сводка** вы можете просмотреть настройки импорта.</span><span class="sxs-lookup"><span data-stu-id="b8875-130">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="b8875-131">Нажмите кнопку **Готово** , чтобы добавить приложение, нажмите кнопку **назад** , чтобы изменить данные, или кнопку **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="b8875-131">Click **Finish** to add the application, click **Back** to change the information, or click **Cancel**.</span></span>

## <span data-ttu-id="b8875-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b8875-132">Related topics</span></span>


[<span data-ttu-id="b8875-133">Управление приложениями на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="b8875-133">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





