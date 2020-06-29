---
title: Изменение учетной записи службы AGPM
description: Изменение учетной записи службы AGPM
author: dansimp
ms.assetid: 0d8d8c7b-f299-4fee-8414-406492156942
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0672ceed2fba17060e17d2ffcfa264da458b9897
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820522"
---
# <span data-ttu-id="64842-103">Изменение учетной записи службы AGPM</span><span class="sxs-lookup"><span data-stu-id="64842-103">Modify the AGPM Service Account</span></span>


<span data-ttu-id="64842-104">Служба управления групповыми политиками — это служба Windows, которая выступает в качестве прокси-сервера, управляет доступом клиентов к объектам групповой политики (GPO) в архивной и рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="64842-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="64842-105">Если эта служба остановлена или отключена, клиенты с РАСШИРЕНным управлением разрешениями не смогут выполнять операции через сервер.</span><span class="sxs-lookup"><span data-stu-id="64842-105">If this service is stopped or disabled, AGPM clients cannot perform operations through the server.</span></span>

<span data-ttu-id="64842-106">Учетная запись "путь к архиву и служба РАСШИРЕНного поиска" настраивается во время установки сервера РАСШИРЕНного использования и может быть изменена в дальнейшем с помощью **добавления или удаления программ** на сервере расширенного использования.</span><span class="sxs-lookup"><span data-stu-id="64842-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="64842-107">**Внимание!**  Не изменяйте параметры службы РАСШИРЕНного **управления правами с помощью средств администрирования** и **служб** в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="64842-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="64842-108">Это может привести к невозможности запуска службы РАСШИРЕНного настольных служб.</span><span class="sxs-lookup"><span data-stu-id="64842-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="64842-109">Учетная запись пользователя, которая входит в группу администраторов домена и имеет доступ к серверу расширенного управления групповыми политиками (на компьютере, на котором установлен компонент Advanced Group Policy Management), для выполнения этой процедуры требуется.</span><span class="sxs-lookup"><span data-stu-id="64842-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

<span data-ttu-id="64842-110">**Важно!**  Учетная запись службы РАСШИРЕНного доступа должна иметь полный доступ к объектам групповой политики, которым он управляет, и будет предоставлять **Вход в качестве разрешения на доступ к службам** .</span><span class="sxs-lookup"><span data-stu-id="64842-110">**Important** The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="64842-111">Если вы будете управлять объектами групповой политики в одном домене, вы можете создать учетную запись локальной системы для основного контроллера домена в службе расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="64842-111">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

<span data-ttu-id="64842-112">Если вы будете управлять объектами групповой политики в нескольких доменах или рядовым сервером является сервер управления групповыми политиками, вы должны настроить другую учетную запись в качестве учетной записи службы РАСШИРЕНного доступа, так как учетная запись локальной системы для одного контроллера домена не может получить доступ к объектам групповой политики в других доменах.</span><span class="sxs-lookup"><span data-stu-id="64842-112">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

 

**<span data-ttu-id="64842-113">Изменение учетной записи службы РАСШИРЕНного редактирования</span><span class="sxs-lookup"><span data-stu-id="64842-113">To modify the AGPM Service Account</span></span>**

1.  <span data-ttu-id="64842-114">На компьютере, на котором установлен сервер расширенного управления групповыми политиками (Microsoft), нажмите кнопку **Пуск**, выберите пункт **Панель управления**, а затем — **Установка и удаление программ**.</span><span class="sxs-lookup"><span data-stu-id="64842-114">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="64842-115">**На вкладке Advanced Group Management (Microsoft) выберите Server (сервер**), а затем нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="64842-115">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="64842-116">Нажмите кнопку **Далее**, а затем — **изменить**.</span><span class="sxs-lookup"><span data-stu-id="64842-116">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="64842-117">Следуйте инструкциям на экране, чтобы настроить параметры для службы РАСШИРЕНного выбора.</span><span class="sxs-lookup"><span data-stu-id="64842-117">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="64842-118">В качестве пути к архиву подтвердите или измените расположение архива относительно сервера РАСШИРЕНного поиска.</span><span class="sxs-lookup"><span data-stu-id="64842-118">For the archive path, confirm or change the location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="64842-119">Путь к архиву может указывать на папку на сервере расширенного управления групповыми политиками или в другом месте, но в расположении должно быть достаточно места для хранения всех объектов групповой политики и данных журнала, управляемых этим сервером управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="64842-119">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="64842-120">Введите новые учетные данные для учетной записи службы РАСШИРЕНного доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="64842-120">Enter new credentials for the AGPM Service Account.</span></span>

    3.  <span data-ttu-id="64842-121">Для владельца архива введите учетные данные администратора РАСШИРЕНного управления правами (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="64842-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="64842-122">Нажмите кнопку **изменить**, после завершения установки нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="64842-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="64842-123">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="64842-123">Additional references</span></span>

-   [<span data-ttu-id="64842-124">Управление службой AGPM</span><span class="sxs-lookup"><span data-stu-id="64842-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





