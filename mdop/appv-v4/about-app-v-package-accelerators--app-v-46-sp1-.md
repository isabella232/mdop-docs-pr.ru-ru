---
title: Описание ускорителей пакетов App-V (App-V 4.6 с пакетом обновления 1 (SP1))
description: Описание ускорителей пакетов App-V (App-V 4.6 с пакетом обновления 1 (SP1))
author: manikadhiman
ms.assetid: fc2d2375-8f17-4a6d-b374-771cb947cb8c
ms.reviewer: ''
manager: dansimp
ms.author: v-madhi
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cb7b8e6fa9482838283257843caf4b291c03bf2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820092"
---
# <span data-ttu-id="9294b-103">Описание ускорителей пакетов App-V (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="9294b-103">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="9294b-104">Акселераторы пакетов App-V можно использовать для автоматического упорядочения больших и сложных приложений.</span><span class="sxs-lookup"><span data-stu-id="9294b-104">You can use App-V Package Accelerators to automatically sequence large, complex applications.</span></span> <span data-ttu-id="9294b-105">Кроме того, если вы примените ускоритель пакетов App-V, вам не всегда требуется вручную устанавливать приложение, чтобы создать виртуальный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="9294b-105">Additionally, when you apply an App-V Package Accelerator, you are not always required to manually install an application to create the virtual application package.</span></span>

<span data-ttu-id="9294b-106">**Примечание**  В некоторых случаях вам будет предложено установить локальное приложение на компьютере с Windows App-V Sequencer, прежде чем можно будет использовать ускоритель пакетов.</span><span class="sxs-lookup"><span data-stu-id="9294b-106">**Note** In some cases, you are prompted to install an application locally to the computer running the App-V Sequencer before you can use the Package Accelerator.</span></span> <span data-ttu-id="9294b-107">Если необходимо установить приложение, необходимо установить его в расположение по умолчанию для приложения.</span><span class="sxs-lookup"><span data-stu-id="9294b-107">If you have to install an application, you must install the application to the application’s default location.</span></span> <span data-ttu-id="9294b-108">Эта установка не отслеживается секвенсором App-V.</span><span class="sxs-lookup"><span data-stu-id="9294b-108">This installation is not monitored by App-V Sequencer.</span></span> <span data-ttu-id="9294b-109">Когда создается ускоритель пакетов App-V, автор ускорителя пакетов определяет, требуется ли локально устанавливать приложение.</span><span class="sxs-lookup"><span data-stu-id="9294b-109">When the App-V Package Accelerator is created, the author of the Package Accelerator determines whether to install an application locally is required.</span></span>

 

<span data-ttu-id="9294b-110">Секвенсор App-V извлекает необходимые файлы из ускорителя пакетов App-V и соответствующего установочного носителя для создания виртуального пакета без необходимости наблюдения за установкой приложения.</span><span class="sxs-lookup"><span data-stu-id="9294b-110">App-V Sequencer extracts the required files from the App-V Package Accelerator and associated installation media to create a virtual package without having to monitor the installation of the application.</span></span>

<span data-ttu-id="9294b-111">**Важно!**  Заявление об отказе: Microsoft Application Virtualization Sequencer не предоставляет вам никаких прав на лицензирование программного приложения, которое вы используете для создания ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="9294b-111">**Important** Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="9294b-112">Вы обязаны соблюдать все условия лицензии конечных пользователей для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="9294b-112">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="9294b-113">Ответственность за то, что условия лицензионного соглашения на использование программного обеспечения позволяют создать пакетный ускоритель с помощью Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="9294b-113">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>

 

<span data-ttu-id="9294b-114">Акселераторы пакетов App-V и шаблоны проектов отличаются друг от друга.</span><span class="sxs-lookup"><span data-stu-id="9294b-114">App-V Package Accelerators and project templates differ from each other.</span></span> <span data-ttu-id="9294b-115">Ускорители пакетов зависят от приложения.</span><span class="sxs-lookup"><span data-stu-id="9294b-115">Package Accelerators are application-specific.</span></span> <span data-ttu-id="9294b-116">Шаблоны проектов позволяют пользователям сохранять часто используемые параметры, специфичные для Организации, и применять их к нескольким приложениям.</span><span class="sxs-lookup"><span data-stu-id="9294b-116">Project templates enable users to save commonly used settings specific to an organization and apply them to multiple applications.</span></span> <span data-ttu-id="9294b-117">Вы также можете создавать шаблоны проектов в командной строке, в отличие от этого, для создания ускорителей пакетов необходимо использовать консоль секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="9294b-117">You can also create project templates at the command prompt, while in contrast, you must use the App-V Sequencer console to create Package Accelerators.</span></span> <span data-ttu-id="9294b-118">Кроме того, создание пакета с помощью ускорителя пакетов и применение шаблона проекта не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9294b-118">Additionally, creating a package by using a Package Accelerator and applying a project template is not supported.</span></span>

## <span data-ttu-id="9294b-119">Совместное использование ускорителей пакетов App-V</span><span class="sxs-lookup"><span data-stu-id="9294b-119">Sharing App-V Package Accelerators</span></span>


<span data-ttu-id="9294b-120">В этом разделе приведены рекомендации по предоставлению общего доступа к ускорителям пакетов.</span><span class="sxs-lookup"><span data-stu-id="9294b-120">This section provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="9294b-121">Если вы планируете совместное использование ускорителей пакетов, такие сведения, как имена компьютеров, сведения об учетных записях пользователей и информация о них, могут быть включены в ускорители пакетов. в приведенном ниже списке описаны методы, которые следует учитывать при создании ускорителей пакетов.</span><span class="sxs-lookup"><span data-stu-id="9294b-121">If you plan to share Package Accelerators, information such as computer names, user account information, and information about the associated applications might be included in the Package Accelerators.The following list describes methods you should consider when creating Package Accelerators:</span></span>

-   <span data-ttu-id="9294b-122">**Имя пользователя**.</span><span class="sxs-lookup"><span data-stu-id="9294b-122">**User name**.</span></span> <span data-ttu-id="9294b-123">При входе в систему на компьютере с запущенным секвенсором App-V следует использовать универсальную учетную запись пользователя, например встроенную учетную запись **администратора** для администрирования компьютера или домена.</span><span class="sxs-lookup"><span data-stu-id="9294b-123">When you log on to the computer running App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account for administering the computer / domain.</span></span> <span data-ttu-id="9294b-124">Не следует использовать учетную запись, которая основывается на существующем имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="9294b-124">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="9294b-125">**Имя компьютера**.</span><span class="sxs-lookup"><span data-stu-id="9294b-125">**Computer Name**.</span></span> <span data-ttu-id="9294b-126">Укажите общее неидентифицирующее имя для компьютера, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="9294b-126">Specify a general, non-identifying name for the computer running the Sequencer.</span></span>

-   <span data-ttu-id="9294b-127">**URL-адрес сервера**.</span><span class="sxs-lookup"><span data-stu-id="9294b-127">**Server URL**.</span></span> <span data-ttu-id="9294b-128">На вкладке " **развертывание** " консоли Sequencer используйте параметры по умолчанию для данных конфигурации URL-адреса сервера.</span><span class="sxs-lookup"><span data-stu-id="9294b-128">In the Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="9294b-129">**Приложения**.</span><span class="sxs-lookup"><span data-stu-id="9294b-129">**Applications**.</span></span> <span data-ttu-id="9294b-130">Если вы не хотите предоставлять общий доступ к списку приложений, установленных на компьютере, на котором запущены программы Sequencer при создании ускорителя пакетов, необходимо удалить файл **appv\_manifest.xml** .</span><span class="sxs-lookup"><span data-stu-id="9294b-130">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="9294b-131">Этот файл находится в корневом каталоге пакета виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="9294b-131">This file is located in the package root directory of the virtual application package.</span></span>

<span data-ttu-id="9294b-132">Кроме того, необходимо проверить все параметры и файлы конфигурации, связанные с виртуальным пакетом приложения, чтобы убедиться, что они не содержат персональных данных.</span><span class="sxs-lookup"><span data-stu-id="9294b-132">You should also review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.</span></span>

## <span data-ttu-id="9294b-133">Защита ускорителей пакетов App-V</span><span class="sxs-lookup"><span data-stu-id="9294b-133">Securing App-V Package Accelerators</span></span>


<span data-ttu-id="9294b-134">Всегда сохраняйте ускорители пакетов App-V и любые связанные установочные носители в безопасном месте в сети для защиты ускорителей пакетов App-V и установочных файлов, которые были изменены или повреждены.</span><span class="sxs-lookup"><span data-stu-id="9294b-134">Always save App-V Package Accelerators and any associated installation media in a secure location on the network to protect the App-V Package Accelerators and the installation files from being tampered with or becoming corrupted.</span></span> <span data-ttu-id="9294b-135">Так как акселераторы пакетов могут также содержать данные пароля и сведения о пользователе, необходимо сохранять ускорители пакетов App-V в безопасном месте, а после создания и повторной подписи пакета ускорителя, чтобы издатель мог быть проверен при применении ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="9294b-135">Because Package Accelerators can also contain password and user-specific information, you must save App-V Package Accelerators in a secure location, and you must digitally sign the Package Accelerator after you create it so that the publisher can be verified when the Package Accelerator is applied.</span></span> <span data-ttu-id="9294b-136">Дополнительные сведения о цифровых подписях можно найти [в разделе рекомендации по применению параметров цифровой подписи для общих условий безопасности](https://go.microsoft.com/fwlink/?LinkId=204705) ( https://go.microsoft.com/fwlink/?LinkId=204705) .</span><span class="sxs-lookup"><span data-stu-id="9294b-136">For more information about digital signatures, see [Application Guidelines on Digital Signature Practices for Common Criteria Security](https://go.microsoft.com/fwlink/?LinkId=204705) (https://go.microsoft.com/fwlink/?LinkId=204705).</span></span>

## <span data-ttu-id="9294b-137">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9294b-137">Related topics</span></span>


[<span data-ttu-id="9294b-138">Создание ускорителей пакетов App-V (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="9294b-138">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)

[<span data-ttu-id="9294b-139">Применение ускорителя пакетов для создания виртуального пакета приложения (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="9294b-139">How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)</span></span>](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)

 

 





