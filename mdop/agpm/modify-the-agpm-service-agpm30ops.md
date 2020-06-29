---
title: Изменение службы AGPM
description: Изменение службы AGPM
author: dansimp
ms.assetid: 3485f85f-59d1-48dc-8748-36826214dcb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f6111a2713fcbe59ffb4336fc84bfa4697ffdeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820502"
---
# <span data-ttu-id="1e609-103">Изменение службы AGPM</span><span class="sxs-lookup"><span data-stu-id="1e609-103">Modify the AGPM Service</span></span>


<span data-ttu-id="1e609-104">Служба управления групповыми политиками — это служба Windows, которая выступает в качестве прокси-сервера, управляет доступом клиентов к объектам групповой политики (GPO) в архивной и рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="1e609-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="1e609-105">Если эта служба остановлена или отключена, клиенты с РАСШИРЕНным управлением разрешениями не смогут выполнять операции через сервер.</span><span class="sxs-lookup"><span data-stu-id="1e609-105">If this service is stopped or disabled, AGPM Clients cannot perform operations through the server.</span></span> <span data-ttu-id="1e609-106">Вы можете изменить путь к архиву, учетную запись службы РАСШИРЕНного поиска и порт, на котором прослушивается служба РАСШИРЕНного выбора.</span><span class="sxs-lookup"><span data-stu-id="1e609-106">You can modify the archive path, the AGPM Service Account, and the port on which the AGPM Service listens.</span></span>

<span data-ttu-id="1e609-107">**Внимание!**  Не изменяйте параметры службы РАСШИРЕНного **управления правами с помощью средств администрирования** и **служб** в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="1e609-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="1e609-108">Это может привести к невозможности запуска службы РАСШИРЕНного настольных служб.</span><span class="sxs-lookup"><span data-stu-id="1e609-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="1e609-109">Учетная запись пользователя, которая входит в группу администраторов домена и имеет доступ к серверу расширенного управления групповыми политиками (на компьютере, на котором установлен компонент Advanced Group Policy Management), для выполнения этой процедуры требуется.</span><span class="sxs-lookup"><span data-stu-id="1e609-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span> <span data-ttu-id="1e609-110">Кроме того, для выполнения этой процедуры необходимо указать учетные данные для учетной записи службы РАСШИРЕНного доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="1e609-110">Additionally, you must provide credentials for the AGPM Service Account to complete this procedure.</span></span>

**<span data-ttu-id="1e609-111">Изменение службы РАСШИРЕНного редактирования</span><span class="sxs-lookup"><span data-stu-id="1e609-111">To modify the AGPM Service</span></span>**

1.  <span data-ttu-id="1e609-112">На компьютере, на котором установлен сервер расширенного управления групповыми политиками (Майкрософт):</span><span class="sxs-lookup"><span data-stu-id="1e609-112">On the computer on which Microsoft Advanced Group Policy Management - Server is installed:</span></span>

    -   <span data-ttu-id="1e609-113">Для WindowsServer2008 нажмите кнопку **Пуск**, выберите **Панель управления**, а затем — **программы и компоненты**.</span><span class="sxs-lookup"><span data-stu-id="1e609-113">For WindowsServer2008, click **Start**, **Control Panel**, and **Programs and Features**.</span></span>

    -   <span data-ttu-id="1e609-114">Для WindowsVista нажмите кнопку **Пуск**, выберите **Панель управления**, **программы**и **программы и компоненты**.</span><span class="sxs-lookup"><span data-stu-id="1e609-114">For WindowsVista, click **Start**, **Control Panel**, **Programs**, and **Programs and Features**.</span></span>

2.  <span data-ttu-id="1e609-115">Щелкните правой кнопкой мыши пункт **Advanced Group Management (сервер**), а затем выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="1e609-115">Right-click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="1e609-116">Нажмите кнопку **Далее**, а затем — **изменить**.</span><span class="sxs-lookup"><span data-stu-id="1e609-116">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="1e609-117">Следуйте инструкциям по настройке службы РАСШИРЕНного выбора:</span><span class="sxs-lookup"><span data-stu-id="1e609-117">Follow the instructions to configure the AGPM Service:</span></span>

    1.  <span data-ttu-id="1e609-118">В диалоговом окне **Архивация пути** введите новое расположение для архива относительно сервера расширенного поиска и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1e609-118">In the **Archive Path** dialog box, enter a new location for the archive relative to the AGPM Server, or confirm the current archive path, and then click **Next**.</span></span>

        <span data-ttu-id="1e609-119">**Важно!**  Путь к архиву может указывать на папку на сервере расширенного управления групповыми политиками или в другом месте, но в расположении должно быть достаточно места для хранения всех объектов групповой политики и данных журнала, управляемых этим сервером управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="1e609-119">**Important** The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

         

    2.  <span data-ttu-id="1e609-120">В диалоговом окне **учетная запись службы расширенного** доступа к аналитике введите учетные данные для учетной записи службы, под которой будет выполняться служба расширенного доступа, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1e609-120">In the **AGPM Service Account** dialog box, enter credentials for a service account under which the AGPM Service will run, and click **Next**.</span></span>

        <span data-ttu-id="1e609-121">**Важно!**  При изменении установки удаляются учетные данные учетной записи службы РАСШИРЕНного доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="1e609-121">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="1e609-122">Вы должны повторно ввести учетные данные, но они не должны совпадать с учетными данными, используемыми при первоначальной установке.</span><span class="sxs-lookup"><span data-stu-id="1e609-122">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="1e609-123">Учетная запись службы РАСШИРЕНного доступа должна иметь полный доступ к объектам групповой политики, которым он управляет, и будет предоставлять **Вход в качестве разрешения на доступ к службам** .</span><span class="sxs-lookup"><span data-stu-id="1e609-123">The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="1e609-124">Если вы будете управлять объектами групповой политики в одном домене, вы можете создать учетную запись локальной системы для основного контроллера домена в службе расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="1e609-124">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="1e609-125">Если вы будете управлять объектами групповой политики в нескольких доменах или рядовым сервером является сервер управления групповыми политиками, вы должны настроить другую учетную запись в качестве учетной записи службы РАСШИРЕНного доступа, так как учетная запись локальной системы для одного контроллера домена не может получить доступ к объектам групповой политики в других доменах.</span><span class="sxs-lookup"><span data-stu-id="1e609-125">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="1e609-126">В диалоговом окне **Владелец архива** введите имя пользователя (полный доступ) или группу администраторов групповой управления групповыми политиками, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1e609-126">In the **Archive Owner** dialog box, enter the user name of an AGPM Administrator (Full Control) or group of AGPM Administrators, and click **Next**.</span></span>

        <span data-ttu-id="1e609-127">**Примечание**  Изменение установки удаляет учетные данные владельца архива.</span><span class="sxs-lookup"><span data-stu-id="1e609-127">**Note** Modifying the installation clears the credentials for the Archive Owner.</span></span> <span data-ttu-id="1e609-128">Вы должны повторно ввести учетные данные, но они не должны совпадать с учетными данными, используемыми при первоначальной установке.</span><span class="sxs-lookup"><span data-stu-id="1e609-128">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

         

    4.  <span data-ttu-id="1e609-129">В диалоговом окне **Настройка порта** введите новый порт, на котором служба расширенного выбора должна прослушать или подтвердить текущий порт, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1e609-129">In the **Port Configuration** dialog box, type a new port on which the AGPM Service should listen or confirm the port currently selected, and click **Next**.</span></span>

        <span data-ttu-id="1e609-130">**Примечание**  По умолчанию служба РАСШИРЕНного отслеживания, прослушивает порт 4600.</span><span class="sxs-lookup"><span data-stu-id="1e609-130">**Note** By default, the AGPM Service listens on port 4600.</span></span>

        <span data-ttu-id="1e609-131">Если вы вручную настроили исключения для порта или у них есть правила настройки исключений для порта, вы можете снять флажок **Добавить исключение для порта в брандмауэр** .</span><span class="sxs-lookup"><span data-stu-id="1e609-131">If you manually configure port exceptions or have rules configuring port exceptions, you can clear the **Add port exception to firewall** check box.</span></span>

         

5.  <span data-ttu-id="1e609-132">Нажмите кнопку **изменить**, после завершения установки нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="1e609-132">Click **Change**, and when the installation is complete click **Finish**.</span></span>

6.  <span data-ttu-id="1e609-133">Если вы изменили порт, прослушиваемый службой РАСШИРЕНного редактирования, измените порт в соединении с сервером РАСШИРЕНного администрирования для каждого администратора групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1e609-133">If you have changed the port on which the AGPM Service listens, modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="1e609-134">(Дополнительные сведения можно найти в разделе [Настройка подключений к серверам с расширенным](configure-agpm-server-connections-agpm30ops.md)доступом.)</span><span class="sxs-lookup"><span data-stu-id="1e609-134">(For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).)</span></span>

7.  <span data-ttu-id="1e609-135">Повторите эти действия для каждого сервера РАСШИРЕНного конфигурирования, к которому необходимо применить изменения.</span><span class="sxs-lookup"><span data-stu-id="1e609-135">Repeat for each AGPM Server to which the configuration changes should be applied.</span></span>

### <span data-ttu-id="1e609-136">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="1e609-136">Additional references</span></span>

-   [<span data-ttu-id="1e609-137">Управление службой AGPM</span><span class="sxs-lookup"><span data-stu-id="1e609-137">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm30ops.md)

 

 





