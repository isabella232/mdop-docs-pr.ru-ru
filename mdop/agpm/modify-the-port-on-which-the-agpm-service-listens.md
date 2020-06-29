---
title: Изменения порта, который прослушивает служба AGPM
description: Изменения порта, который прослушивает служба AGPM
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820489"
---
# <span data-ttu-id="ee5e3-103">Изменения порта, который прослушивает служба AGPM</span><span class="sxs-lookup"><span data-stu-id="ee5e3-103">Modify the Port on Which the AGPM Service Listens</span></span>


<span data-ttu-id="ee5e3-104">Служба управления групповыми политиками — это служба Windows, которая выступает в качестве прокси-сервера, управляет доступом клиентов к объектам групповой политики (GPO) в архивной и рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="ee5e3-105">По умолчанию служба РАСШИРЕНного отслеживания, прослушивает порт 4600.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-105">By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="ee5e3-106">Вы можете изменить этот порт, изменив файл с индексом в файле расширенного управления групповыми политиками (групповой политики) для каждого архива.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-106">You can change this port by modifying the Advanced Group Policy Management (AGPM) archive index file for each archive.</span></span>

<span data-ttu-id="ee5e3-107">**Примечание**  Перед изменением порта, прослушиваемого службой РАСШИРЕНного выбора, рекомендуется создать резервную копию индексируемого файла в формате РАСШИРЕНного (gpostate.xml).</span><span class="sxs-lookup"><span data-stu-id="ee5e3-107">**Note** Before modifying the port on which the AGPM Service listens, it is recommended that you back up the AGPM archive index file (gpostate.xml).</span></span> <span data-ttu-id="ee5e3-108">Этот файл находится в папке, указанной в качестве пути к архиву, во время установки расширенного управления групповыми политиками — сервера.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-108">This file is located in the folder entered as the archive path during the installation of Advanced Group Policy Management - Server.</span></span> <span data-ttu-id="ee5e3-109">По умолчанию этот файл имеет следующий адрес:% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml на сервере РАСШИРЕНного использования.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-109">By default, this location of this file is %CommonAppData%\\Microsoft\\AGPM\\gpostate.xml on the AGPM Server.</span></span> <span data-ttu-id="ee5e3-110">Если вы не знаете, на каком компьютере находится архив, вы можете выполнить описанные ниже действия, чтобы изменить путь к архиву, чтобы отобразить текущий путь к архиву.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-110">If you do not know which computer hosts the archive, you can follow the procedure for modifying the archive path to display the current archive path.</span></span> <span data-ttu-id="ee5e3-111">Дополнительные сведения можно найти [в разделе изменение пути к архиву](modify-the-archive-path.md).</span><span class="sxs-lookup"><span data-stu-id="ee5e3-111">For more information, see [Modify the Archive Path](modify-the-archive-path.md).</span></span>

 

<span data-ttu-id="ee5e3-112">Для выполнения этой процедуры необходимо использовать учетную запись пользователя, на которой установлен доступ к серверу РАСШИРЕНного доступа (на компьютере, на котором установлена служба РАСШИРЕНного доступа к данным), и архивный файл индекса.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-112">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) and the archive index file is required to complete this procedure.</span></span>

**<span data-ttu-id="ee5e3-113">Изменение порта, прослушиваемого службой РАСШИРЕНного выбора</span><span class="sxs-lookup"><span data-stu-id="ee5e3-113">To modify the port on which the AGPM Service listens</span></span>**

1.  <span data-ttu-id="ee5e3-114">На компьютере, на котором размещается Архив, откройте файл индекса архивации (gpostate.xml) в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-114">On the computer hosting the archive, open the archive index file (gpostate.xml) in a text editor.</span></span>

2.  <span data-ttu-id="ee5e3-115">В файле выполните поиск по **расширению: Port = "4600"**.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-115">In the file, search for **agpm:port="4600"**.</span></span>

3.  <span data-ttu-id="ee5e3-116">Замените **4600** на порт, на который должна прослушиваться служба расширенного выбора. затем сохраните и закройте файл.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-116">Replace **4600** with the port on which the AGPM Service should listen; then, save and close the file.</span></span>

4.  <span data-ttu-id="ee5e3-117">На сервере с РАСШИРЕНным языком, перезапустите службу РАСШИРЕНного включения.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-117">On the AGPM Server, restart the AGPM Service.</span></span> <span data-ttu-id="ee5e3-118">(Дополнительные сведения можно найти в разделе [Запуск и остановка службы расширенного](start-and-stop-the-agpm-service.md)просмотра данных.)</span><span class="sxs-lookup"><span data-stu-id="ee5e3-118">(For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).)</span></span>

5.  <span data-ttu-id="ee5e3-119">Измените порт в соединении с сервером РАСШИРЕНного администрирования для каждого администратора групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-119">Modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="ee5e3-120">(Дополнительные сведения можно найти [в разделе Настройка подключения к серверу расширенного конфигурирования](configure-the-agpm-server-connection.md).)</span><span class="sxs-lookup"><span data-stu-id="ee5e3-120">(For more information, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).)</span></span>

6.  <span data-ttu-id="ee5e3-121">Повторите эти действия для каждого сервера архивации и РАСШИРЕНного.</span><span class="sxs-lookup"><span data-stu-id="ee5e3-121">Repeat for each archive and AGPM Server.</span></span>

### <span data-ttu-id="ee5e3-122">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="ee5e3-122">Additional references</span></span>

-   [<span data-ttu-id="ee5e3-123">Управление службой AGPM</span><span class="sxs-lookup"><span data-stu-id="ee5e3-123">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





