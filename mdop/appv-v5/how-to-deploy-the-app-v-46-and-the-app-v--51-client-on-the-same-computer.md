---
title: Развертывание приложения App-V 4,6 и клиента App-V 5,1 на том же компьютере
description: Развертывание приложения App-V 4,6 и клиента App-V 5,1 на том же компьютере
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814173"
---
# <span data-ttu-id="b9b0c-103">Развертывание приложения App-V 4,6 и клиента App-V 5,1 на том же компьютере</span><span class="sxs-lookup"><span data-stu-id="b9b0c-103">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>

<span data-ttu-id="b9b0c-104">**Примечание.** Приложение App-V 4,6 завершило работу базовой поддержки.</span><span class="sxs-lookup"><span data-stu-id="b9b0c-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="b9b0c-105">Используйте следующие сведения для установки клиента Microsoft Application Virtualization (App-V) 5,1 (предпочтительный с последними пакетами обновления и исправлениями), а также клиента App-v 4.6 SP2 или клиента App-V 4.6 S3 на том же компьютере.</span><span class="sxs-lookup"><span data-stu-id="b9b0c-105">Use the following information to install the Microsoft Application Virtualization (App-V) 5.1 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP2 client or the App-V 4.6S3 client on the same computer.</span></span> <span data-ttu-id="b9b0c-106">Поддерживаемые версии, требования и другие сведения о планировании можно найти в разделе [Планирование миграции с предыдущей версии App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="b9b0c-106">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).</span></span>

**<span data-ttu-id="b9b0c-107">Развертывание клиента App-V 5,1 и Client App-V 4,6 на одном компьютере</span><span class="sxs-lookup"><span data-stu-id="b9b0c-107">To deploy the App-V 5.1 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="b9b0c-108">Установите следующую версию клиента App-V на компьютере под управлением App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="b9b0c-108">Install the following version of the App-V client on the computer that is running App-V 4.6.</span></span>

    -   [<span data-ttu-id="b9b0c-109">Microsoft Application Virtualization 4,6 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="b9b0c-109">Microsoft Application Virtualization 4.6 Service Pack 3</span></span>](https://www.microsoft.com/download/details.aspx?id=41187)

2.  <span data-ttu-id="b9b0c-110">Установите клиент App-V 5,1 на компьютере, на котором запущена версия App-V 4,6 SP3.</span><span class="sxs-lookup"><span data-stu-id="b9b0c-110">Install the App-V 5.1 client on the computer that is running the App-V 4.6 SP3 version of the client.</span></span> <span data-ttu-id="b9b0c-111">Для достижения наилучших результатов мы рекомендуем установить все доступные обновления для клиента App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b9b0c-111">For best results, we recommend that you install all available updates to the App-V 5.1 client.</span></span>

3.  <span data-ttu-id="b9b0c-112">Преобразуйте и повторно поочередность пакетов.</span><span class="sxs-lookup"><span data-stu-id="b9b0c-112">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="b9b0c-113">Чтобы преобразовать пакеты, используйте конвертер пакета App-V 5,1 и преобразуйте необходимые пакеты в формат файлов App-V 5,1 (**. AppV**).</span><span class="sxs-lookup"><span data-stu-id="b9b0c-113">To convert the packages, use the App-V 5.1 package converter and convert the required packages to the App-V 5.1 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="b9b0c-114">Для повторной нумерации пакетов рекомендуется использовать последнюю версию секвенсора для наилучших результатов.</span><span class="sxs-lookup"><span data-stu-id="b9b0c-114">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="b9b0c-115">Дополнительные сведения о публикации пакетов можно найти в разделе [Публикация пакета с помощью консоли управления](how-to-publish-a-package-by-using-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="b9b0c-115">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md).</span></span>

4.  <span data-ttu-id="b9b0c-116">Развертывание пакетов на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="b9b0c-116">Deploy packages to the client computers.</span></span>

5.  <span data-ttu-id="b9b0c-117">При необходимости преобразуйте точки расширения.</span><span class="sxs-lookup"><span data-stu-id="b9b0c-117">Convert extension points, as needed.</span></span> <span data-ttu-id="b9b0c-118">Подробнее:</span><span class="sxs-lookup"><span data-stu-id="b9b0c-118">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="b9b0c-119">Перенос точек расширения из пакета App-V 4.6 в преобразованный пакет App-V 5.1 для всех пользователей на указанном компьютере</span><span class="sxs-lookup"><span data-stu-id="b9b0c-119">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="b9b0c-120">Перенос точек расширения из пакета App-V 4.6 в App-V 5.1 для конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="b9b0c-120">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [<span data-ttu-id="b9b0c-121">Преобразование пакета, созданного в предыдущей версии App-V</span><span class="sxs-lookup"><span data-stu-id="b9b0c-121">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  <span data-ttu-id="b9b0c-122">Убедитесь, что пакеты приложения-V 5,1 выполнены успешно, а затем удалите пакеты 4,6.</span><span class="sxs-lookup"><span data-stu-id="b9b0c-122">Test that your App-V 5.1 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="b9b0c-123">Для проверки состояния пользователя клиентских компьютеров рекомендуется использовать [виртуализацию взаимодействия с пользователем](https://technet.microsoft.com/library/dn458947.aspx) или другое средство управления средой пользователя.</span><span class="sxs-lookup"><span data-stu-id="b9b0c-123">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="b9b0c-124">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="b9b0c-124">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="b9b0c-125">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="b9b0c-125">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="b9b0c-126">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="b9b0c-126">Got an App-V issue?</span></span>** <span data-ttu-id="b9b0c-127">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="b9b0c-127">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="b9b0c-128">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b9b0c-128">Related topics</span></span>


[<span data-ttu-id="b9b0c-129">Планирование миграции из предыдущей версии App-V</span><span class="sxs-lookup"><span data-stu-id="b9b0c-129">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[<span data-ttu-id="b9b0c-130">Развертывание Sequencer и клиента App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b9b0c-130">Deploying the App-V 5.1 Sequencer and Client</span></span>](deploying-the-app-v-51-sequencer-and-client.md)

 

 





