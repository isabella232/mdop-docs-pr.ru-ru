---
title: Настройка доступа к пакетам с помощью консоли управления
description: Настройка доступа к пакетам с помощью консоли управления
author: dansimp
ms.assetid: 4fd39bc2-d814-46de-a108-1c21fa404e8a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c6c8f930fb1fbd82432f6d43dae8b9bed7a563c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814416"
---
# <span data-ttu-id="44e7e-103">Настройка доступа к пакетам с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="44e7e-103">How to Configure Access to Packages by Using the Management Console</span></span>


<span data-ttu-id="44e7e-104">Перед развертыванием виртуализированного пакета App-V 5,1 необходимо настроить группы безопасности доменных служб Active Directory (AD DS), которым будет разрешен доступ к приложениям и их запуск.</span><span class="sxs-lookup"><span data-stu-id="44e7e-104">Before you deploy an App-V 5.1 virtualized package, you must configure the Active Directory Domain Services (AD DS) security groups that will be allowed to access and run the applications.</span></span> <span data-ttu-id="44e7e-105">Группы безопасности могут содержать компьютеры или пользователей.</span><span class="sxs-lookup"><span data-stu-id="44e7e-105">The security groups may contain computers or users.</span></span> <span data-ttu-id="44e7e-106">Entitling пакеты в группу компьютера публикуют его глобально на всех компьютерах в группе.</span><span class="sxs-lookup"><span data-stu-id="44e7e-106">Entitling a package to a computer group publishes the package globally to all computers in the group.</span></span>

<span data-ttu-id="44e7e-107">Чтобы настроить доступ к виртуализированным пакетам, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="44e7e-107">Use the following procedure to configure access to virtualized packages.</span></span>

**<span data-ttu-id="44e7e-108">Предоставление доступа к пакету App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="44e7e-108">To grant access to an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="44e7e-109">Найдите пакет, который вы хотите настроить:</span><span class="sxs-lookup"><span data-stu-id="44e7e-109">Find the package you want to configure:</span></span>

    1.  <span data-ttu-id="44e7e-110">Откройте консоль управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="44e7e-110">Open the App-V 5.1 Management console.</span></span>

    2.  <span data-ttu-id="44e7e-111">Чтобы отобразить страницу **AD Access** , щелкните правой кнопкой мыши пакет, который нужно настроить, и выберите команду **изменить доступ к Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="44e7e-111">To display the **AD ACCESS** page, right-click the package to be configured, and select **Edit active directory access**.</span></span> <span data-ttu-id="44e7e-112">Кроме того, можно выбрать пакет и нажать кнопку **изменить** на панели **AD Access** .</span><span class="sxs-lookup"><span data-stu-id="44e7e-112">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="44e7e-113">Подготовка группы безопасности для пакета:</span><span class="sxs-lookup"><span data-stu-id="44e7e-113">Provision a security group for the package:</span></span>

    1.  <span data-ttu-id="44e7e-114">Перейдите на страницу **Поиск допустимых имен Active Directory и предоставление доступа** .</span><span class="sxs-lookup"><span data-stu-id="44e7e-114">Go to the **FIND VALID ACTIVE DIRECTORY NAMES AND GRANT ACCESS** page.</span></span>

    2.  <span data-ttu-id="44e7e-115">На странице Формат **mydomain**  \\  **имя_группы**введите имя или часть имени объекта группы Active Directory, а затем нажмите кнопку **проверить**.</span><span class="sxs-lookup"><span data-stu-id="44e7e-115">Using the format **mydomain** \\ **groupname**, type the name or part of the name of an Active Directory group object, and click **Check**.</span></span>

        <span data-ttu-id="44e7e-116">**Примечание**  Убедитесь, что для группы, которую вы ищете, вы предоставляете имя домена, соответствующее домену.</span><span class="sxs-lookup"><span data-stu-id="44e7e-116">**Note** Ensure that you provide an associated domain name for the group that you are searching for.</span></span>

         

3.  <span data-ttu-id="44e7e-117">Чтобы предоставить доступ к пакету, выберите нужную группу и нажмите кнопку **предоставить доступ**.</span><span class="sxs-lookup"><span data-stu-id="44e7e-117">To grant access to the package, select the desired group and click **Grant Access**.</span></span> <span data-ttu-id="44e7e-118">Новая группа отобразится в области " **рекламные сущности" с** областью доступа.</span><span class="sxs-lookup"><span data-stu-id="44e7e-118">The newly added group is displayed in the **AD ENTITIES WITH ACCESS** pane.</span></span>

4.  

    <span data-ttu-id="44e7e-119">Чтобы сохранить параметры конфигурации по умолчанию и закрыть страницу **AD** , нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="44e7e-119">To accept the default configuration settings and close the **AD ACCESS** page, click **Close**.</span></span>

    <span data-ttu-id="44e7e-120">Чтобы настроить конфигурации для определенной группы, щелкните раскрывающийся список **Назначенные конфигурации** и выберите пункт **Настраиваемая**.</span><span class="sxs-lookup"><span data-stu-id="44e7e-120">To customize configurations for a specific group, click the **ASSIGNED CONFIGURATIONS** drop-down and select **Custom**.</span></span> <span data-ttu-id="44e7e-121">Чтобы настроить пользовательские конфигурации, нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="44e7e-121">To configure the custom configurations, click **EDIT**.</span></span> <span data-ttu-id="44e7e-122">После предоставления доступа нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="44e7e-122">After you grant access, click **Close**.</span></span>

**<span data-ttu-id="44e7e-123">Удаление доступа к пакету App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="44e7e-123">To remove access to an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="44e7e-124">Найдите пакет, который вы хотите настроить:</span><span class="sxs-lookup"><span data-stu-id="44e7e-124">Find the package you want to configure:</span></span>

    1.  <span data-ttu-id="44e7e-125">Откройте консоль управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="44e7e-125">Open the App-V 5.1 Management console.</span></span>

    2.  <span data-ttu-id="44e7e-126">Чтобы отобразить страницу **AD Access** , щелкните правой кнопкой мыши пакет, который нужно настроить, и выберите команду **изменить доступ к Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="44e7e-126">To display the **AD ACCESS** page, right-click the package to be configured, and select **Edit active directory access**.</span></span> <span data-ttu-id="44e7e-127">Кроме того, можно выбрать пакет и нажать кнопку **изменить** на панели **AD Access** .</span><span class="sxs-lookup"><span data-stu-id="44e7e-127">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="44e7e-128">Выберите группу, которую вы хотите удалить, и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="44e7e-128">Select the group you want to remove, and click **DELETE**.</span></span>

3.  <span data-ttu-id="44e7e-129">Чтобы закрыть страницу **AD Access** , нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="44e7e-129">To close the **AD ACCESS** page, click **Close**.</span></span>

    <span data-ttu-id="44e7e-130">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="44e7e-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="44e7e-131">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="44e7e-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="44e7e-132">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="44e7e-132">Got an App-V issue?</span></span>** <span data-ttu-id="44e7e-133">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="44e7e-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="44e7e-134">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="44e7e-134">Related topics</span></span>


[<span data-ttu-id="44e7e-135">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="44e7e-135">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





