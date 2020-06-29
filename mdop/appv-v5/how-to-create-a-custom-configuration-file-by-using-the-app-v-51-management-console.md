---
title: Создание пользовательского файла конфигурации с помощью консоли управления App-V 5.1
description: Создание пользовательского файла конфигурации с помощью консоли управления App-V 5.1
author: dansimp
ms.assetid: f5ab426a-f49a-47b3-93f3-b9d60aada8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 282207b5424442950e88c40a372194e9def768cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814325"
---
# <span data-ttu-id="0c857-103">Создание пользовательского файла конфигурации с помощью консоли управления App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="0c857-103">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>


<span data-ttu-id="0c857-104">Вы можете использовать динамическую конфигурацию для настройки пакета App-V 5,1 для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c857-104">You can use a dynamic configuration to customize an App-V 5.1 package for a specific user.</span></span> <span data-ttu-id="0c857-105">Тем не менее, прежде чем можно будет использовать файлы, необходимо сначала создать файл динамической конфигурации (XML) или динамической конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="0c857-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="0c857-106">Создание файла является расширенной операцией вручную.</span><span class="sxs-lookup"><span data-stu-id="0c857-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="0c857-107">Общие сведения о файлах динамической конфигурации пользователей можно найти в разделе [сведения о динамической конфигурации App-V 5,1](about-app-v-51-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="0c857-107">For general information about dynamic user configuration files, see, [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md).</span></span>

<span data-ttu-id="0c857-108">Выполните описанные ниже действия, чтобы создать файл динамической конфигурации пользователя с помощью консоли управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="0c857-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.1 Management console.</span></span>

**<span data-ttu-id="0c857-109">Создание файла динамической конфигурации пользователя</span><span class="sxs-lookup"><span data-stu-id="0c857-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="0c857-110">Щелкните правой кнопкой мыши имя пакета, который вы хотите просмотреть, и выберите команду **изменить доступ к Active Directory** , чтобы просмотреть конфигурацию, назначенную данной группе пользователей.</span><span class="sxs-lookup"><span data-stu-id="0c857-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="0c857-111">Кроме того, можно выбрать пакет и нажать кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="0c857-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="0c857-112">С помощью списка **сущностей AD с Access**выберите группу AD, которую вы хотите настроить.</span><span class="sxs-lookup"><span data-stu-id="0c857-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="0c857-113">В раскрывающемся списке выберите пункт **другой** , если он еще не выбран.</span><span class="sxs-lookup"><span data-stu-id="0c857-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="0c857-114">Будет показана ссылка " **изменить** ".</span><span class="sxs-lookup"><span data-stu-id="0c857-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="0c857-115">Нажмите кнопку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="0c857-115">Click **Edit**.</span></span> <span data-ttu-id="0c857-116">Появится динамическая конфигурация пользователя, назначенная группе AD.</span><span class="sxs-lookup"><span data-stu-id="0c857-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="0c857-117">Нажмите кнопку **Дополнительно**и выберите пункт **Экспорт конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="0c857-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="0c857-118">Введите имя файла и нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0c857-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="0c857-119">Теперь вы можете изменить файл, чтобы настроить пакет для пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c857-119">Now you can edit the file to configure a package for a user.</span></span>

    **<span data-ttu-id="0c857-120">Примечание.</span><span class="sxs-lookup"><span data-stu-id="0c857-120">Note</span></span>**  
    <span data-ttu-id="0c857-121">Чтобы экспортировать конфигурацию во время работы на компьютере с Windows Server, необходимо отключить параметр "Конфигурация усиленной безопасности Internet Explorer".</span><span class="sxs-lookup"><span data-stu-id="0c857-121">To export a configuration while running on Windows Server, you must disable "IE Enhanced Security Configuration".</span></span> <span data-ttu-id="0c857-122">Если этот параметр включен и настроен для блокировки загрузок, вы не сможете загрузить ничего из сервера App-V.</span><span class="sxs-lookup"><span data-stu-id="0c857-122">If this is enabled and set to block downloads, you cannot download anything from the App-V Server.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="0c857-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0c857-123">Related topics</span></span>


[<span data-ttu-id="0c857-124">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="0c857-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









