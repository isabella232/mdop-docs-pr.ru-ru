---
title: Изменение конфигурации клиента App-V 5.0 с помощью шаблона ADMX и групповой политики
description: Изменение конфигурации клиента App-V 5.0 с помощью шаблона ADMX и групповой политики
author: dansimp
ms.assetid: 79d03a2b-2586-4ca7-bbaa-bdeb0a694279
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cd257691bf223baa5e2919d83fdbf53d34f271ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813840"
---
# <span data-ttu-id="ae30b-103">Изменение конфигурации клиента App-V 5.0 с помощью шаблона ADMX и групповой политики</span><span class="sxs-lookup"><span data-stu-id="ae30b-103">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>


<span data-ttu-id="ae30b-104">Используйте шаблон App-V 5,0 ADMX для настройки клиента App-V 5,0 с помощью шаблона ADMX и групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ae30b-104">Use the App-V 5.0 ADMX template to configure App-V 5.0 client settings using the ADMX Template and Group Policy.</span></span>

**<span data-ttu-id="ae30b-105">Изменение конфигурации клиента App-V 5,0 с помощью групповой политики</span><span class="sxs-lookup"><span data-stu-id="ae30b-105">To modify App-V 5.0 client configuration using Group Policy</span></span>**

1.  <span data-ttu-id="ae30b-106">Чтобы изменить конфигурацию клиента App-V 5,0, найдите файлы **ADMXTemplate** , доступные в приложении App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="ae30b-106">To modify the App-V 5.0 client configuration, locate the **ADMXTemplate** files that are available with App-V 5.0.</span></span>

    <span data-ttu-id="ae30b-107">**Примечание**  Чтобы скачать шаблоны App-V 5,0 **ADMX**, воспользуйтесь следующей ссылкой: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .</span><span class="sxs-lookup"><span data-stu-id="ae30b-107">**Note** Use the following link to download the App-V 5.0 **ADMX Templates**: <https://go.microsoft.com/fwlink/p/?LinkId=393941>.</span></span>

     

2.  <span data-ttu-id="ae30b-108">На компьютере, на котором вы управляете групповой политикой (обычно это контроллер домена), скопируйте файл template **. ADMX** в следующий каталог: \*\* &lt; установочный диск &gt; \ \ Windows \ \ PolicyDefinitions\*\*.</span><span class="sxs-lookup"><span data-stu-id="ae30b-108">On the computer where you manage group Policy, typically the domain controller, copy the template **.admx** file to the following directory: **&lt;Installation Drive&gt; \\ Windows \\ PolicyDefinitions**.</span></span>

    <span data-ttu-id="ae30b-109">Затем на том же компьютере скопируйте файл **ADML** в следующий каталог: \*\* &lt; InstallationDrive &gt; \ \ Windows \ \ POLICYDEFINITIONS \ \ en-US\*\*.</span><span class="sxs-lookup"><span data-stu-id="ae30b-109">Next, on the same computer, copy the **.adml** file to the following directory: **&lt;InstallationDrive&gt; \\ Windows \\ PolicyDefinitions \\ en-US**.</span></span>

3.  <span data-ttu-id="ae30b-110">После копирования файлов откройте консоль управления групповыми политиками, чтобы изменить политики, связанные с вашими клиентами App-V 5,0, перейдите к политикам **конфигурации компьютера**  /  **Policies**  /  **Administrative Templates**  /  **. System**  /  **App-v**.</span><span class="sxs-lookup"><span data-stu-id="ae30b-110">After you have copied the files open the Group Policy Management Console, to modify the policies associated with your App-V 5.0 clients browse to **Computer Configuration** / **Policies** / **Administrative Templates** / **System** / **App-V**.</span></span>

    <span data-ttu-id="ae30b-111">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="ae30b-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="ae30b-112">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="ae30b-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="ae30b-113">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="ae30b-113">Got an App-V issue?</span></span>** <span data-ttu-id="ae30b-114">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ae30b-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ae30b-115">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ae30b-115">Related topics</span></span>


[<span data-ttu-id="ae30b-116">Развертывание App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ae30b-116">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="ae30b-117">Сведения о параметрах конфигурации клиента</span><span class="sxs-lookup"><span data-stu-id="ae30b-117">About Client Configuration Settings</span></span>](about-client-configuration-settings.md)

 

 





