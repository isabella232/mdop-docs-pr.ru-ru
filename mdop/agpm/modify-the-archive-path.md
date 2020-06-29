---
title: Изменение пути к архиву
description: Изменение пути к архиву
author: dansimp
ms.assetid: 6d90daf9-58db-4166-b5b3-e84bb261164a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1fc6ba2bf415d3d1bc67144d0dec1030c6173026
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820492"
---
# <span data-ttu-id="e0ff3-103">Изменение пути к архиву</span><span class="sxs-lookup"><span data-stu-id="e0ff3-103">Modify the Archive Path</span></span>


<span data-ttu-id="e0ff3-104">Путь к архиву — это расположение архива относительно сервера с РАСШИРЕНным набором элементов.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-104">The archive path is the location of the archive relative to the AGPM Server.</span></span> <span data-ttu-id="e0ff3-105">Путь к архиву может указывать на папку на сервере РАСШИРЕНного поиска и на другом сервере в том же лесе.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-105">The archive path can point to a folder on the AGPM Server or on another server in the same forest.</span></span>

<span data-ttu-id="e0ff3-106">Учетная запись "путь к архиву и служба РАСШИРЕНного поиска" настраивается во время установки сервера РАСШИРЕНного использования и может быть изменена в дальнейшем с помощью **добавления или удаления программ** на сервере расширенного использования.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="e0ff3-107">Учетная запись пользователя, которая входит в группу администраторов домена и имеет доступ к серверу расширенного управления групповыми политиками (на компьютере, на котором установлен компонент Advanced Group Policy Management), для выполнения этой процедуры требуется.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-107">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="e0ff3-108">Изменение пути к архиву</span><span class="sxs-lookup"><span data-stu-id="e0ff3-108">To modify the archive path</span></span>**

1.  <span data-ttu-id="e0ff3-109">На компьютере, на котором установлен сервер расширенного управления групповыми политиками (Microsoft), нажмите кнопку **Пуск**, выберите пункт **Панель управления**, а затем — **Установка и удаление программ**.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-109">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="e0ff3-110">**На вкладке Advanced Group Management (Microsoft) выберите Server (сервер**), а затем нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-110">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="e0ff3-111">Нажмите кнопку **Далее**, а затем — **изменить**.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-111">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="e0ff3-112">Следуйте инструкциям на экране, чтобы настроить параметры для службы РАСШИРЕНного выбора.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-112">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="e0ff3-113">В качестве пути к архиву введите новое расположение для архива относительно сервера РАСШИРЕНного поиска.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-113">For the archive path, enter a new location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="e0ff3-114">Путь к архиву может указывать на папку на сервере расширенного управления групповыми политиками или в другом месте, но в расположении должно быть достаточно места для хранения всех объектов групповой политики и данных журнала, управляемых этим сервером управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-114">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="e0ff3-115">Введите учетные данные для учетной записи службы РАСШИРЕНного доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-115">Enter credentials for the AGPM Service Account.</span></span>

        <span data-ttu-id="e0ff3-116">**Важно!**  При изменении установки удаляются учетные данные учетной записи службы РАСШИРЕНного доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-116">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="e0ff3-117">Вы должны повторно ввести учетные данные, но они не должны совпадать с учетными данными, используемыми при первоначальной установке.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-117">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="e0ff3-118">Учетная запись службы РАСШИРЕНного доступа к данным должна иметь полный доступ к объектам групповой политики, которыми она будет управлять.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-118">The AGPM Service Account must have full access to the GPOs that it will manage.</span></span> <span data-ttu-id="e0ff3-119">Если вы будете управлять объектами групповой политики в одном домене, вы можете создать учетную запись локальной системы для основного контроллера домена в службе расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-119">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="e0ff3-120">Если вы будете управлять объектами групповой политики в нескольких доменах или рядовым сервером является сервер управления групповыми политиками, вы должны настроить другую учетную запись в качестве учетной записи службы РАСШИРЕНного доступа, так как учетная запись локальной системы для одного контроллера домена не может получить доступ к объектам групповой политики в других доменах.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-120">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="e0ff3-121">Для владельца архива введите учетные данные администратора РАСШИРЕНного управления правами (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="e0ff3-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="e0ff3-122">Нажмите кнопку **изменить**, после завершения установки нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="e0ff3-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="e0ff3-123">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="e0ff3-123">Additional references</span></span>

-   [<span data-ttu-id="e0ff3-124">Управление службой AGPM</span><span class="sxs-lookup"><span data-stu-id="e0ff3-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





