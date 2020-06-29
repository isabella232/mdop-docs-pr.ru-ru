---
title: Настройка сервера веб-распространения образов
description: Настройка сервера веб-распространения образов
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825159"
---
# <span data-ttu-id="7280c-103">Настройка сервера веб-распространения образов</span><span class="sxs-lookup"><span data-stu-id="7280c-103">How to Configure the Image Web Distribution Server</span></span>


<span data-ttu-id="7280c-104">Репозиторий изображений — это необязательный сервер, который используется для распространения изображений (когда администраторы загружают новые образы и клиентские компьютеры проверяют сервер каждые 15 минут и обновляют свое изображение, если доступно новое).</span><span class="sxs-lookup"><span data-stu-id="7280c-104">An image repository is an optional server that is used for image distribution (where administrators upload new images and client computers check the server every 15 minutes and update their image if a new one is available).</span></span>

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


<span data-ttu-id="7280c-105">Для сервера распространения изображений требуются указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="7280c-105">An image distribution server requires the following:</span></span>

-   <span data-ttu-id="7280c-106">Сведения о службах IIS, которые можно найти в разделе Информационные [службы Интернета](https://go.microsoft.com/fwlink/?LinkId=142995).</span><span class="sxs-lookup"><span data-stu-id="7280c-106">Internet Information Services (IIS)—For information, see [Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=142995).</span></span>

    <span data-ttu-id="7280c-107">Во время установки IIS при добавлении служб ролей выберите следующие поддерживаемые методы проверки подлинности:</span><span class="sxs-lookup"><span data-stu-id="7280c-107">During the IIS installation, when adding role services, select the following supported authentication methods:</span></span>

    -   **<span data-ttu-id="7280c-108">Обычная проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="7280c-108">Basic Authentication</span></span>**

    -   **<span data-ttu-id="7280c-109">Проверка подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="7280c-109">Windows Authentication</span></span>**

    -   **<span data-ttu-id="7280c-110">Проверка подлинности сопоставления сертификатов клиентов</span><span class="sxs-lookup"><span data-stu-id="7280c-110">Client Certificate Mapping Authentication</span></span>**

    <span data-ttu-id="7280c-111">При настройке IIS Включите указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="7280c-111">When configuring IIS, include the following:</span></span>

    -   <span data-ttu-id="7280c-112">Добавьте виртуальный каталог с псевдонимом с именем **MEDVImages**.</span><span class="sxs-lookup"><span data-stu-id="7280c-112">Add a virtual directory, with the alias named **MEDVImages**.</span></span> <span data-ttu-id="7280c-113">Физический путь должен указывать на расположение изображений.</span><span class="sxs-lookup"><span data-stu-id="7280c-113">The physical path should point to the location of the images.</span></span>

    -   <span data-ttu-id="7280c-114">Включите функцию BITS.</span><span class="sxs-lookup"><span data-stu-id="7280c-114">Enable BITS.</span></span>

    -   <span data-ttu-id="7280c-115">Добавьте следующие типы MIME.</span><span class="sxs-lookup"><span data-stu-id="7280c-115">Add the following MIME types:</span></span>

        -   **<span data-ttu-id="7280c-116">. ckm (приложение/октет — поток)</span><span class="sxs-lookup"><span data-stu-id="7280c-116">.ckm (application/octet-stream)</span></span>**

        -   <span data-ttu-id="7280c-117">**. index (приложение/октет — поток**)</span><span class="sxs-lookup"><span data-stu-id="7280c-117">**.index (application/octet-stream**)</span></span>

    -   <span data-ttu-id="7280c-118">На сайте MED-V добавьте разрешения на чтение для **всех**.</span><span class="sxs-lookup"><span data-stu-id="7280c-118">On the MED-V site, add read permissions to **Everyone**.</span></span>

    -   <span data-ttu-id="7280c-119">Перезапустите IIS.</span><span class="sxs-lookup"><span data-stu-id="7280c-119">Restart IIS.</span></span>

-   <span data-ttu-id="7280c-120">Серверные расширения BITS для IIS — дополнительные сведения можно найти в разделе [Установка серверных РАСШИРЕНИЙ BITS](https://go.microsoft.com/fwlink/?LinkId=142996).</span><span class="sxs-lookup"><span data-stu-id="7280c-120">BITS Server Extensions for IIS—For information, see [Install BITS Server Extensions](https://go.microsoft.com/fwlink/?LinkId=142996).</span></span>

## <span data-ttu-id="7280c-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7280c-121">Related topics</span></span>


[<span data-ttu-id="7280c-122">Поддерживаемые конфигурации</span><span class="sxs-lookup"><span data-stu-id="7280c-122">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="7280c-123">Проектирование репозиториев образа MED-V</span><span class="sxs-lookup"><span data-stu-id="7280c-123">Design the MED-V Image Repositories</span></span>](design-the-med-v-image-repositories.md)

 

 





