---
title: Развертывание приложения App-V 4,6 и клиента App-V 5,0 на том же компьютере
description: Развертывание приложения App-V 4,6 и клиента App-V 5,0 на том же компьютере
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.openlocfilehash: 38e77ce6ce6c0dba7c67f6c0dfa5c9e263e07e20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814181"
---
# <span data-ttu-id="6f67e-103">Развертывание приложения App-V 4,6 и клиента App-V 5,0 на том же компьютере</span><span class="sxs-lookup"><span data-stu-id="6f67e-103">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>

<span data-ttu-id="6f67e-104">**Примечание.** Приложение App-V 4,6 завершило работу базовой поддержки.</span><span class="sxs-lookup"><span data-stu-id="6f67e-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="6f67e-105">В следующем примере предполагается, что клиент App-V 4,6 с пакетом обновления 3 (SP3) уже установлен.</span><span class="sxs-lookup"><span data-stu-id="6f67e-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="6f67e-106">Используйте следующие сведения, чтобы установить клиент App-V 5,0 (предпочтительно, с последними пакетами обновления и исправлениями), а клиент App-V 4.6 SP3 — на том же компьютере.</span><span class="sxs-lookup"><span data-stu-id="6f67e-106">Use the following information to install the App-V 5.0 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP3 client on the same computer.</span></span> <span data-ttu-id="6f67e-107">Поддерживаемые версии, требования и другие сведения о планировании можно найти в разделе [Планирование миграции с предыдущей версии App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="6f67e-107">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span></span>

**<span data-ttu-id="6f67e-108">Развертывание клиента App-V 5,0 и Client App-V 4,6 на одном компьютере</span><span class="sxs-lookup"><span data-stu-id="6f67e-108">To deploy the App-V 5.0 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="6f67e-109">Установите клиент App-V 5,0 с пакетом обновления 3 (SP3) на компьютере, на котором запущена версия App-V 4,6 клиента.</span><span class="sxs-lookup"><span data-stu-id="6f67e-109">Install the App-V 5.0 SP3 client on the computer that is running the App-V 4.6 version of the client.</span></span> <span data-ttu-id="6f67e-110">Для достижения наилучших результатов мы рекомендуем установить все доступные обновления в клиенте App-V 5,0 с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="6f67e-110">For best results, we recommend that you install all available updates to the App-V 5.0 SP3 client.</span></span>

2.  <span data-ttu-id="6f67e-111">Преобразуйте и повторно поочередность пакетов.</span><span class="sxs-lookup"><span data-stu-id="6f67e-111">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="6f67e-112">Чтобы преобразовать пакеты, используйте конвертер пакета App-V 5,0 и преобразуйте необходимые пакеты в формат файлов App-V 5,0 (**. AppV**).</span><span class="sxs-lookup"><span data-stu-id="6f67e-112">To convert the packages, use the App-V 5.0 package converter and convert the required packages to the App-V 5.0 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="6f67e-113">Для повторной нумерации пакетов рекомендуется использовать последнюю версию секвенсора для наилучших результатов.</span><span class="sxs-lookup"><span data-stu-id="6f67e-113">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="6f67e-114">Дополнительные сведения о публикации пакетов можно найти в разделе [Публикация пакета с помощью консоли управления](how-to-publish-a-package-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="6f67e-114">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

3.  <span data-ttu-id="6f67e-115">Развертывание пакетов на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="6f67e-115">Deploy packages to the client computers.</span></span>

4.  <span data-ttu-id="6f67e-116">При необходимости преобразуйте точки расширения.</span><span class="sxs-lookup"><span data-stu-id="6f67e-116">Convert extension points, as needed.</span></span> <span data-ttu-id="6f67e-117">Подробнее:</span><span class="sxs-lookup"><span data-stu-id="6f67e-117">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="6f67e-118">Перенос точек расширения из пакета App-V 4.6 в преобразованный пакет App-V 5.0 для всех пользователей на указанном компьютере</span><span class="sxs-lookup"><span data-stu-id="6f67e-118">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="6f67e-119">Перенос точек расширения из пакета App-V 4.6 в App-V 5.0 для конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="6f67e-119">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [<span data-ttu-id="6f67e-120">Преобразование пакета, созданного в предыдущей версии App-V</span><span class="sxs-lookup"><span data-stu-id="6f67e-120">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  <span data-ttu-id="6f67e-121">Убедитесь, что пакеты приложения-V 5,0 выполнены успешно, а затем удалите пакеты 4,6.</span><span class="sxs-lookup"><span data-stu-id="6f67e-121">Test that your App-V 5.0 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="6f67e-122">Для проверки состояния пользователя клиентских компьютеров рекомендуется использовать [виртуализацию взаимодействия с пользователем](https://technet.microsoft.com/library/dn458947.aspx) или другое средство управления средой пользователя.</span><span class="sxs-lookup"><span data-stu-id="6f67e-122">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="6f67e-123">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="6f67e-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="6f67e-124">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="6f67e-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="6f67e-125">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="6f67e-125">Got an App-V issue?</span></span>** <span data-ttu-id="6f67e-126">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="6f67e-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="6f67e-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="6f67e-127">Related topics</span></span>


[<span data-ttu-id="6f67e-128">Планирование миграции из предыдущей версии App-V</span><span class="sxs-lookup"><span data-stu-id="6f67e-128">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v.md)

[<span data-ttu-id="6f67e-129">Развертывание программы Sequencer и клиента App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="6f67e-129">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 





