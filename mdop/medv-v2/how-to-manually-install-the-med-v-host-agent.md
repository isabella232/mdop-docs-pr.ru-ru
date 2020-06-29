---
title: Ручная установка агента узла MED-V
description: Ручная установка агента узла MED-V
author: dansimp
ms.assetid: 4becc90b-6481-4e1f-a4d3-aec74c8821ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a7fb44b23a390cf394af2331152955afc2d8eba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812896"
---
# <span data-ttu-id="de015-103">Ручная установка агента узла MED-V</span><span class="sxs-lookup"><span data-stu-id="de015-103">How to Manually Install the MED-V Host Agent</span></span>


<span data-ttu-id="de015-104">Существует два отдельных, но связанных компонентов для решения Microsoft Enterprise Virtualization (MED-V) 2,0: агент узла MED-V и гостевой агент.</span><span class="sxs-lookup"><span data-stu-id="de015-104">There are two separate but related components to the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="de015-105">Агент узла находится на главном компьютере (на компьютере пользователя под управлением Windows 7) и предоставляет канал для связи с гостевой службой MED-v (виртуальная машина MED-V, запущенная на главном компьютере).</span><span class="sxs-lookup"><span data-stu-id="de015-105">The Host Agent resides on the host computer (a user’s computer that is running Windows 7) and provides a channel to communicate with the MED-V guest (the MED-V virtual machine running in the host computer).</span></span> <span data-ttu-id="de015-106">Кроме того, она предоставляет определенные функциональные возможности, связанные с MED-V, например публикация приложений.</span><span class="sxs-lookup"><span data-stu-id="de015-106">It also provides certain MED-V related functionality, such as application publishing.</span></span>

<span data-ttu-id="de015-107">Как правило, вы развертываете и устанавливаете агент узла MED-V, используя предпочтительный метод программного обеспечения для подготовки вашей компании.</span><span class="sxs-lookup"><span data-stu-id="de015-107">Typically, you deploy and install the MED-V Host Agent by using your company’s preferred method of provisioning software.</span></span> <span data-ttu-id="de015-108">Тем не менее, перед развертыванием MED-V на предприятии может потребоваться установить агент узла локально для тестирования.</span><span class="sxs-lookup"><span data-stu-id="de015-108">However, before deploying MED-V across your enterprise, you might prefer to install the Host Agent locally for testing.</span></span> <span data-ttu-id="de015-109">В этом разделе приведены пошаговые инструкции по установке агента узла MED-V вручную.</span><span class="sxs-lookup"><span data-stu-id="de015-109">This section provides step-by-step instructions for manually installing the MED-V Host Agent.</span></span>

<span data-ttu-id="de015-110">**Примечание**  Гостевой агент MED-V устанавливается автоматически при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="de015-110">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<span data-ttu-id="de015-111">**Важно!**  Перед установкой агента узла MED-V закройте Internet Explorer, в противном случае конфликты могут возникать позже с перенаправлением URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="de015-111">**Important** Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="de015-112">Вы также можете сделать это, указав компьютер во время распространения.</span><span class="sxs-lookup"><span data-stu-id="de015-112">You can also do this by specifying a computer restart during a distribution.</span></span>

 

**<span data-ttu-id="de015-113">Установка агента узла MED-V</span><span class="sxs-lookup"><span data-stu-id="de015-113">To install the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="de015-114">Найдите файлы установки для MED-V, полученные в ходе загрузки программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="de015-114">Locate the MED-V installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="de015-115">Дважды щелкните установочный файл MED-V \ _HostAgent \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="de015-115">Double-click the MED-V\_HostAgent\_Setup installation file.</span></span>

    <span data-ttu-id="de015-116">Откроется мастер **настройки агента узла Microsoft Enterprise Virtualization (MED-V)** .</span><span class="sxs-lookup"><span data-stu-id="de015-116">The **Microsoft Enterprise Desktop Virtualization (MED-V) Host Agent Setup** wizard opens.</span></span> <span data-ttu-id="de015-117">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="de015-117">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="de015-118">Приняв условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="de015-118">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="de015-119">Выберите папку назначения для установки агента узла MED-V.</span><span class="sxs-lookup"><span data-stu-id="de015-119">Select the destination folder for installing the MED-V Host Agent.</span></span> <span data-ttu-id="de015-120">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="de015-120">Click **Next**.</span></span>

5.  <span data-ttu-id="de015-121">Чтобы начать установку агента узла, нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="de015-121">To begin the Host Agent installation, click **Install**.</span></span>

6.  <span data-ttu-id="de015-122">После успешного завершения установки нажмите кнопку **Готово** , чтобы закрыть окно мастера.</span><span class="sxs-lookup"><span data-stu-id="de015-122">After the installation is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="de015-123">Чтобы убедиться, что установка агента узла была выполнена успешно, нажмите кнопку **Пуск**, выберите пункт **все программы**, затем — **Microsoft Enterprise Virtualization**, а затем — **Агент хоста MED-V**.</span><span class="sxs-lookup"><span data-stu-id="de015-123">To verify that the installation of the Host Agent was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="de015-124">**Примечание**  Пока не установлена рабочая область MED-V, агент узла MED-V может запускаться и работать, но не обеспечивает никаких функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="de015-124">**Note** Until a MED-V workspace is installed, the MED-V Host Agent can be started and runs, but provides no functionality.</span></span>

 

## <span data-ttu-id="de015-125">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="de015-125">Related topics</span></span>


[<span data-ttu-id="de015-126">Развертывание компонентов MED-V с помощью системы электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="de015-126">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="de015-127">Установка средства упаковки рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="de015-127">How to Install the MED-V Workspace Packager</span></span>](how-to-install-the-med-v-workspace-packager.md)

[<span data-ttu-id="de015-128">Удаление компонентов MED-V</span><span class="sxs-lookup"><span data-stu-id="de015-128">How to Uninstall the MED-V Components</span></span>](how-to-uninstall-the-med-v-components.md)

 

 





