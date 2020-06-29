---
title: Создание пользовательского файла конфигурации с помощью консоли управления App-V 5.0
description: Создание пользовательского файла конфигурации с помощью консоли управления App-V 5.0
author: dansimp
ms.assetid: 0d1f6768-be30-4682-8eeb-aa95918b24c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d54e68caa380025b2ff6f3ea79d30f275b589b30
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814328"
---
# <span data-ttu-id="69610-103">Создание пользовательского файла конфигурации с помощью консоли управления App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="69610-103">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>


<span data-ttu-id="69610-104">Вы можете использовать динамическую конфигурацию для настройки пакета App-V 5,0 для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="69610-104">You can use a dynamic configuration to customize an App-V 5.0 package for a specific user.</span></span> <span data-ttu-id="69610-105">Тем не менее, прежде чем можно будет использовать файлы, необходимо сначала создать файл динамической конфигурации (XML) или динамической конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="69610-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="69610-106">Создание файла является расширенной операцией вручную.</span><span class="sxs-lookup"><span data-stu-id="69610-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="69610-107">Общие сведения о файлах динамической конфигурации пользователей можно найти в разделе [сведения о динамической конфигурации App-V 5,0](about-app-v-50-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="69610-107">For general information about dynamic user configuration files, see, [About App-V 5.0 Dynamic Configuration](about-app-v-50-dynamic-configuration.md).</span></span>

<span data-ttu-id="69610-108">Выполните описанные ниже действия, чтобы создать файл динамической конфигурации пользователя с помощью консоли управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="69610-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.0 Management console.</span></span>

**<span data-ttu-id="69610-109">Создание файла динамической конфигурации пользователя</span><span class="sxs-lookup"><span data-stu-id="69610-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="69610-110">Щелкните правой кнопкой мыши имя пакета, который вы хотите просмотреть, и выберите команду **изменить доступ к Active Directory** , чтобы просмотреть конфигурацию, назначенную данной группе пользователей.</span><span class="sxs-lookup"><span data-stu-id="69610-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="69610-111">Кроме того, можно выбрать пакет и нажать кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="69610-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="69610-112">С помощью списка **сущностей AD с Access**выберите группу AD, которую вы хотите настроить.</span><span class="sxs-lookup"><span data-stu-id="69610-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="69610-113">В раскрывающемся списке выберите пункт **другой** , если он еще не выбран.</span><span class="sxs-lookup"><span data-stu-id="69610-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="69610-114">Будет показана ссылка " **изменить** ".</span><span class="sxs-lookup"><span data-stu-id="69610-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="69610-115">Нажмите кнопку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="69610-115">Click **Edit**.</span></span> <span data-ttu-id="69610-116">Появится динамическая конфигурация пользователя, назначенная группе AD.</span><span class="sxs-lookup"><span data-stu-id="69610-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="69610-117">Нажмите кнопку **Дополнительно**и выберите пункт **Экспорт конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="69610-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="69610-118">Введите имя файла и нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="69610-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="69610-119">Теперь вы можете изменить файл, чтобы настроить пакет для пользователя.</span><span class="sxs-lookup"><span data-stu-id="69610-119">Now you can edit the file to configure a package for a user.</span></span>

    <span data-ttu-id="69610-120">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="69610-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="69610-121">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="69610-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="69610-122">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="69610-122">Got an App-V issue?</span></span>** <span data-ttu-id="69610-123">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="69610-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="69610-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="69610-124">Related topics</span></span>


[<span data-ttu-id="69610-125">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="69610-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





