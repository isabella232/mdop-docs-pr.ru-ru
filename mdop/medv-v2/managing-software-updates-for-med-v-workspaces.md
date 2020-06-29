---
title: Управление обновлениями программного обеспечения для рабочих областей MED-V
description: Управление обновлениями программного обеспечения для рабочих областей MED-V
author: dansimp
ms.assetid: a28d6dcd-cb9f-46ba-8dac-1d990837a3a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 696238a2f5ad9b7e5120f75f6cd09d890d12519b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824812"
---
# <span data-ttu-id="258e1-103">Управление обновлениями программного обеспечения для рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="258e1-103">Managing Software Updates for MED-V Workspaces</span></span>


<span data-ttu-id="258e1-104">Есть несколько различных параметров, которые можно использовать для предоставления обновлений программного обеспечения для приложений в развернутой рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="258e1-104">You have several different options available to you for providing software updates for the applications in the deployed MED-V workspace.</span></span>

<span data-ttu-id="258e1-105">**Примечание**  Сведения о том, как указать параметры конфигурации, определяющие способ получения автоматических обновлений в MED-V, приведены в разделе [Управление автоматическим обновлением для рабочих областей MED-V](managing-automatic-updates-for-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="258e1-105">**Note** For information about how to specify the configuration settings that define how MED-V receives automatic updates, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

 

**<span data-ttu-id="258e1-106">Обновление программного обеспечения в рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="258e1-106">Updating Software in a MED-V Workspace</span></span>**

1.  **<span data-ttu-id="258e1-107">Использование электронной системы распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="258e1-107">Using an Electronic Software Distribution System</span></span>**

    <span data-ttu-id="258e1-108">Если в вашей организации используется система электронной системы распространения программного обеспечения для развертывания программного обеспечения, вы можете использовать ее для предоставления обновлений программного обеспечения для приложений в рабочих областях MED-V точно так же, как и в случае обновлений приложений на физических компьютерах.</span><span class="sxs-lookup"><span data-stu-id="258e1-108">If your organization uses an Electronic Software Distribution System (ESD) system to deploy software, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

2.  **<span data-ttu-id="258e1-109">Использование групповой политики</span><span class="sxs-lookup"><span data-stu-id="258e1-109">Using Group Policy</span></span>**

    <span data-ttu-id="258e1-110">Если в вашей организации развертывание программного обеспечения осуществляется с помощью групповой политики, вы можете использовать его для предоставления обновлений программного обеспечения для приложений в рабочих областях MED-V так же, как и в случае обновлений приложений на физических компьютерах.</span><span class="sxs-lookup"><span data-stu-id="258e1-110">If your organization deploys software by using Group Policy, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

3.  **<span data-ttu-id="258e1-111">Использование Application Virtualization (APP-V)</span><span class="sxs-lookup"><span data-stu-id="258e1-111">Using Application Virtualization (APP-V)</span></span>**

    <span data-ttu-id="258e1-112">Если вы используете MED-V вместе с App-v, вы можете предоставить обновления программного обеспечения приложениям в рабочей области для MED-V, выполнив действия, которые необходимы приложению App-V для обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="258e1-112">If you use MED-V together with App-V, you can provide software updates to applications in the MED-V workspace by following the steps that are required by App-V for updating software.</span></span> <span data-ttu-id="258e1-113">Дополнительные сведения можно найти в разделе [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) ...).</span><span class="sxs-lookup"><span data-stu-id="258e1-113">For more information, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

4.  **<span data-ttu-id="258e1-114">Обновление программного обеспечения на центральном изображении</span><span class="sxs-lookup"><span data-stu-id="258e1-114">Updating Software in the Core Image</span></span>**

    <span data-ttu-id="258e1-115">Несмотря на то что не рассматривается в качестве оптимальной методики для MED-V, вы можете установить обновления программного обеспечения для приложений на базовом образе.</span><span class="sxs-lookup"><span data-stu-id="258e1-115">Although not considered a MED-V best practice, you can install software updates to applications on the core image.</span></span> <span data-ttu-id="258e1-116">После установки обновлений вы можете снова развернуть рабочую область MED-V в корпоративной среде так же, как если бы вы развернули ее первоначально.</span><span class="sxs-lookup"><span data-stu-id="258e1-116">After you have installed the updates, you can then redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

    <span data-ttu-id="258e1-117">**Важно!**  Мы не рекомендуем использовать этот метод для управления обновлениями программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="258e1-117">**Important** We do not recommend this method of managing software updates.</span></span> <span data-ttu-id="258e1-118">Кроме того, если вы обновите программное обеспечение в базовом образе и повторно разверните рабочее пространство MED-V в своей организации, сначала необходимо запустить настройку, а все данные, сохраненные на виртуальной машине, будут утрачены.</span><span class="sxs-lookup"><span data-stu-id="258e1-118">In addition, if you update software in the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="258e1-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="258e1-119">Related topics</span></span>


[<span data-ttu-id="258e1-120">Управление автоматическими обновлениями для рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="258e1-120">Managing Automatic Updates for MED-V Workspaces</span></span>](managing-automatic-updates-for-med-v-workspaces.md)

[<span data-ttu-id="258e1-121">Проверка публикации приложений</span><span class="sxs-lookup"><span data-stu-id="258e1-121">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="258e1-122">Публикация и отмена публикации приложения в рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="258e1-122">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





