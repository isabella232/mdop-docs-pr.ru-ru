---
title: Проверка перенаправления URL-адресов
description: Проверка перенаправления URL-адресов
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824449"
---
# <span data-ttu-id="4bdb6-103">Проверка перенаправления URL-адресов</span><span class="sxs-lookup"><span data-stu-id="4bdb6-103">How to Test URL Redirection</span></span>


<span data-ttu-id="4bdb6-104">После завершения первоначальной проверки правильности работы функции перенаправления URL-адресов можно проверить, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-104">After your test of first time setup finishes, you can verify that the URL redirection functionality is working as expected by performing the following tasks.</span></span>

<span data-ttu-id="4bdb6-105">**Важно!**  Для правильной работы перенаправления URL-адреса необходимо, чтобы был запущен агент узла MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-105">**Important** The MED-V Host Agent must be running for URL redirection to function correctly.</span></span>

<a href="" id="bkmk-urlredir"></a>**<span data-ttu-id="4bdb6-106">Проверка перенаправления URL-адреса</span><span class="sxs-lookup"><span data-stu-id="4bdb6-106">To test URL Redirection</span></span>**

1.  <span data-ttu-id="4bdb6-107">Откройте браузер Internet Explorer на главном компьютере и введите URL-адрес, указанный для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-107">Open an Internet Explorer browser in the host computer and enter a URL that you specified for redirection.</span></span>

2.  <span data-ttu-id="4bdb6-108">Убедитесь в том, что веб-страница открыта в Internet Explorer на гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-108">Verify that the webpage is opened in Internet Explorer on the guest virtual machine.</span></span>

3.  <span data-ttu-id="4bdb6-109">Повторите эти действия для каждого URL-адреса, который вы хотите протестировать.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-109">Repeat this process for each URL that you want to test.</span></span>

**<span data-ttu-id="4bdb6-110">Проверка возможности добавления или удаления URL-адреса</span><span class="sxs-lookup"><span data-stu-id="4bdb6-110">To test that a URL can be added or removed</span></span>**

1.  <span data-ttu-id="4bdb6-111">Добавьте или удалите URL-адрес из рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-111">Add or remove a URL from the MED-V workspace.</span></span>

    <span data-ttu-id="4bdb6-112">Сведения о том, как добавлять и удалять URL-адреса для перенаправления в рабочей области MED-V, можно найти в разделе [Управление перенаправлением URL-адресов](manage-med-v-url-redirection.md)в MED-v.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-112">For information about how to add and remove URLs for redirection on a MED-V workspace, see [Manage MED-V URL Redirection](manage-med-v-url-redirection.md).</span></span>

2.  <span data-ttu-id="4bdb6-113">Если вы добавили URL-адрес в список перенаправления, повторите действия, описанные в разделе [Проверка перенаправления URL-адреса](#bkmk-urlredir) , чтобы убедиться, что новый URL-адрес перенаправляется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-113">If you added a URL to the redirection list, repeat the steps in [To Test URL Redirection](#bkmk-urlredir) to verify that the new URL redirects as intended.</span></span>

3.  <span data-ttu-id="4bdb6-114">Если вы удалили URL-адрес из списка перенаправления, убедитесь, что он удален, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-114">If you removed a URL from the redirection list, verify that it is removed by following these steps:</span></span>

    1.  <span data-ttu-id="4bdb6-115">Откройте браузер Internet Explorer на главном компьютере и введите URL-адрес, который вы удалили из списка перенаправления.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-115">Open an Internet Explorer browser in the host computer and enter the URL that you removed from the redirection list.</span></span>

    2.  <span data-ttu-id="4bdb6-116">Убедитесь, что веб-страница открыта в Internet Explorer на главном компьютере, а не на гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-116">Verify that the webpage is opened in Internet Explorer on the host computer instead of on the guest virtual machine.</span></span>

        <span data-ttu-id="4bdb6-117">**Примечание**  Изменение перенаправления URL-адреса может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-117">**Note** It can take several seconds for the URL redirection changes to take place.</span></span>

<span data-ttu-id="4bdb6-118">**Примечание**  Если при проверке параметров перенаправления URL-адресов возникли проблемы, ознакомьтесь с разделом [Устранение неполадок](operations-troubleshooting-medv2.md)при использовании операций.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-118">**Note** If you encounter any problems when verifying your URL redirection settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="4bdb6-119">После того как вы закончите тестирование перенаправления URL-адресов в рабочей области MED-V, вы можете протестировать другие конфигурации, чтобы убедиться, что они правильно выполняются.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-119">After you have completed testing URL redirection in your MED-V workspace, you can test other configurations to verify that they function as intended.</span></span>

<span data-ttu-id="4bdb6-120">После завершения тестирования пакета рабочей области для MED-V и проверки его работоспособности вы можете развернуть рабочую область MED-V в своей организации.</span><span class="sxs-lookup"><span data-stu-id="4bdb6-120">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="4bdb6-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4bdb6-121">Related topics</span></span>

[<span data-ttu-id="4bdb6-122">Проверка публикации приложений</span><span class="sxs-lookup"><span data-stu-id="4bdb6-122">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="4bdb6-123">Проверка параметров первой установки</span><span class="sxs-lookup"><span data-stu-id="4bdb6-123">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="4bdb6-124">Развертывание пакета рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="4bdb6-124">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





