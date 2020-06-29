---
title: Проверка публикации приложений
description: Проверка публикации приложений
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826912"
---
# <span data-ttu-id="27297-103">Проверка публикации приложений</span><span class="sxs-lookup"><span data-stu-id="27297-103">How to Test Application Publishing</span></span>


<span data-ttu-id="27297-104">После завершения первоначальной настройки вы можете проверить, правильно ли работают функции публикации приложения, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="27297-104">After your test of first time setup finishes, you can verify that the application publishing functionality is working as expected by performing the following tasks.</span></span>

<a href="" id="bkmk-apppub"></a>**<span data-ttu-id="27297-105">Тестирование публикации приложения</span><span class="sxs-lookup"><span data-stu-id="27297-105">To test application publishing</span></span>**

1.  <span data-ttu-id="27297-106">Убедитесь в том, что приложения, которые вы указали для публикации, видимы.</span><span class="sxs-lookup"><span data-stu-id="27297-106">Verify that the applications that you specified for publishing are visible.</span></span>

    <span data-ttu-id="27297-107">Нажмите кнопку **Пуск** и выберите пункт **все программы** , а затем найдите указанные приложения.</span><span class="sxs-lookup"><span data-stu-id="27297-107">Click **Start** and then click **All Programs** and search for the specified applications.</span></span>

    <span data-ttu-id="27297-108">В некоторых случаях одно и то же приложение может быть установлено два раза один раз на главном компьютере и один раз на гостевой.</span><span class="sxs-lookup"><span data-stu-id="27297-108">In some cases, you might have the same application installed two times, one time on the host computer and one time on the guest.</span></span> <span data-ttu-id="27297-109">Если опубликованное приложение с таким же именем Опубликовано в главном меню " **Пуск** ", оно будет отличаться от ярлыка ведущего приложения, добавив имя виртуальной машины к имени ярлыка.</span><span class="sxs-lookup"><span data-stu-id="27297-109">If a published application that has the same name is published to the same location on the host **Start** menu, it is distinguished from the host application shortcut by adding the virtual machine name to the shortcut name.</span></span> <span data-ttu-id="27297-110">Например, для виртуальной машины с именем "MEDVHost1" ведущее приложение может быть "Блокнотом", а опубликованное приложение — "Notepad (MEDVHost1)".</span><span class="sxs-lookup"><span data-stu-id="27297-110">For example, for a virtual machine named “MEDVHost1”, a host application might be "Notepad" and a published application might be "Notepad (MEDVHost1)".</span></span>

2.  <span data-ttu-id="27297-111">Убедитесь в том, что функции приложений используются должным образом.</span><span class="sxs-lookup"><span data-stu-id="27297-111">Verify that the applications function as intended.</span></span>

    <span data-ttu-id="27297-112">На главном компьютере запустите опубликованные приложения и убедитесь, что они открыты в Windows XP с пакетом обновления 3 (SP3) на гостевой машине.</span><span class="sxs-lookup"><span data-stu-id="27297-112">On the host computer, start the applications that you published and verify that they open in Windows XP SP3 on the guest.</span></span> <span data-ttu-id="27297-113">Приложение должно отображаться в окне стиля Windows XP на рабочем столе главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="27297-113">The application must appear in a Windows XP-style window on the host computer desktop.</span></span>

3.  <span data-ttu-id="27297-114">При необходимости убедитесь, что функции перенаправления документов должным образом.</span><span class="sxs-lookup"><span data-stu-id="27297-114">If applicable, verify that document redirection functions as intended.</span></span>

    <span data-ttu-id="27297-115">Если опубликованное приложение на гостевой машине должно открыть папку на системном диске узла, убедитесь, что она может открыть указанную папку.</span><span class="sxs-lookup"><span data-stu-id="27297-115">If a published application on the guest has to open a folder on the host system drive, ensure that it can open the specified folder.</span></span>

    <span data-ttu-id="27297-116">**Важно!**  Так как Virtual PC для Windows не поддерживает создание общего доступа из папки, которая уже есть в общем доступе, перенаправление не происходит для документов, которые открываются из общей папки, например из папки Мои документы, которая находится в сети.</span><span class="sxs-lookup"><span data-stu-id="27297-116">**Important** Because Windows Virtual PC does not support creating a share from a folder that is already shared, redirection does not occur for any documents that open from a shared folder, such as a My Documents folder that is located on the network.</span></span> <span data-ttu-id="27297-117">Дополнительные сведения можно найти в разделе [Устранение неполадок, возникающих](operations-troubleshooting-medv2.md)при выполнении операций.</span><span class="sxs-lookup"><span data-stu-id="27297-117">For more information, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="27297-118">После проверки того, что опубликованные приложения установлены и работают правильно, вы можете проверить, можно ли добавлять или удалять приложения из рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="27297-118">After you have verified that published applications are installed and functioning correctly, you can test whether applications can be added or removed from the MED-V workspace.</span></span>

**<span data-ttu-id="27297-119">Проверка возможности добавления или удаления приложения</span><span class="sxs-lookup"><span data-stu-id="27297-119">To test that an application can be added or removed</span></span>**

1.  <span data-ttu-id="27297-120">Добавьте или удалите приложение из рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="27297-120">Add or remove an application from the MED-V workspace.</span></span>

    <span data-ttu-id="27297-121">Сведения о том, как добавлять и удалять приложения из рабочей области MED-V, приведены [в разделе Управление приложениями, развернутыми в рабочих областях med-v](managing-applications-deployed-to-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="27297-121">For information about how to add and remove applications from a MED-V workspace, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

2.  <span data-ttu-id="27297-122">Если вы добавили приложение, повторите действия, описанные в статье [Проверка публикации приложения](#bkmk-apppub) , чтобы убедиться в том, что новое приложение функционирует надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="27297-122">If you added an application, repeat the steps in [To Test Application Publishing](#bkmk-apppub) to verify that the new application functions as intended.</span></span>

3.  <span data-ttu-id="27297-123">Если вы удалили приложение, нажмите кнопку **Пуск** , а затем выберите пункт **все программы** и убедитесь, что удаленные приложения больше не указаны в списке.</span><span class="sxs-lookup"><span data-stu-id="27297-123">If you removed an application, click **Start** and then click **All Programs** and verify that any applications that you removed are no longer listed.</span></span>

<span data-ttu-id="27297-124">**Примечание**  Если вы столкнулись с проблемами при проверке параметров публикации приложения, ознакомьтесь с разделом [Устранение неполадок](operations-troubleshooting-medv2.md)с помощью операций.</span><span class="sxs-lookup"><span data-stu-id="27297-124">**Note** If you encounter any problems when verifying your application publication settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="27297-125">После того как вы закончите тестирование публикации приложения, вы можете протестировать другие конфигурации рабочей области MED-V, чтобы убедиться, что они правильно выполняются.</span><span class="sxs-lookup"><span data-stu-id="27297-125">After you have completed testing application publishing, you can test other MED-V workspace configurations to verify that they function as intended.</span></span>

<span data-ttu-id="27297-126">После завершения тестирования пакета рабочей области для MED-V и проверки его работоспособности вы можете развернуть рабочую область MED-V в своей организации.</span><span class="sxs-lookup"><span data-stu-id="27297-126">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="27297-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="27297-127">Related topics</span></span>

[<span data-ttu-id="27297-128">Проверка перенаправления URL-адресов</span><span class="sxs-lookup"><span data-stu-id="27297-128">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="27297-129">Проверка параметров первой установки</span><span class="sxs-lookup"><span data-stu-id="27297-129">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="27297-130">Развертывание пакета рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="27297-130">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





