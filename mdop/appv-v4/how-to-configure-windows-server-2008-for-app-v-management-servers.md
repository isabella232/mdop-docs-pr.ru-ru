---
title: Настройка Windows Server 2008 для серверов App-V Management Server
description: Настройка Windows Server 2008 для серверов App-V Management Server
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817722"
---
# <span data-ttu-id="489e9-103">Настройка Windows Server 2008 для серверов App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="489e9-103">How to Configure Windows Server 2008 for App-V Management Servers</span></span>


<span data-ttu-id="489e9-104">Сервер Windows Server 2008, на котором вы установили веб-службу Microsoft Application Virtualization (App-V) Management, требует наличия служб IIS для установки в качестве роли на сервере.</span><span class="sxs-lookup"><span data-stu-id="489e9-104">The Windows Server 2008 server on which you install the Microsoft Application Virtualization (App-V) Management Web Service requires Internet Information Services (IIS) to be installed as a role on the server.</span></span> <span data-ttu-id="489e9-105">Чтобы настроить Windows Server 2008 для поддержки установки App-VServer, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="489e9-105">Use the following procedure to configure Windows Server 2008 to support App-Vserver installation.</span></span>

**<span data-ttu-id="489e9-106">Установка служб IIS на компьютере с Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="489e9-106">To install IIS on a Windows Server2008 computer</span></span>**

1.  <span data-ttu-id="489e9-107">На компьютере с Windows Server2008 нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Администрирование**, а затем — **Диспетчер** серверов.</span><span class="sxs-lookup"><span data-stu-id="489e9-107">On the Windows Server2008 computer, click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Server Manager** to start Server Manager.</span></span> <span data-ttu-id="489e9-108">В диспетчере серверов щелкните правой кнопкой мыши узел " **роли** " и выберите команду **Добавить роли** , чтобы запустить **Мастер добавления ролей**.</span><span class="sxs-lookup"><span data-stu-id="489e9-108">In Server Manager, right-click the **Roles** node, and click **Add Roles** to start the **Add Roles Wizard**.</span></span>

2.  <span data-ttu-id="489e9-109">В **мастере добавления ролей**на странице **Выбор ролей сервера** выберите **веб-сервер (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="489e9-109">In the **Add Roles Wizard**, on the **Select Server Roles** page, select **Web Server (IIS)**.</span></span> <span data-ttu-id="489e9-110">При появлении соответствующего запроса нажмите кнопку **Добавить необходимые функции** , чтобы добавить зависимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="489e9-110">When prompted, click **Add Required Features** to add the dependent features.</span></span>

3.  <span data-ttu-id="489e9-111">На странице **Выбор ролей сервера** нажмите кнопку **Далее**, а затем еще раз нажмите кнопку **Далее** .</span><span class="sxs-lookup"><span data-stu-id="489e9-111">On the **Select Server Roles** page, Click **Next**, and then click **Next** again.</span></span>

4.  <span data-ttu-id="489e9-112">В **мастере добавления ролей**на странице " **Выбор служб ролей** " выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="489e9-112">In the **Add Roles Wizard**, on the **Select Role Services** page:</span></span>

    1.  <span data-ttu-id="489e9-113">В разделе **Разработка приложений**выберите **ASP.NET** и при появлении соответствующего запроса нажмите кнопку **Добавить необходимые службы** ролей, чтобы добавить службы и компоненты зависимых ролей.</span><span class="sxs-lookup"><span data-stu-id="489e9-113">Under **Application Development**, select **ASP.NET** and, when prompted, click **Add Required Role Services** to add the dependent roles services and features.</span></span>

    2.  <span data-ttu-id="489e9-114">В разделе **Безопасность**выберите **Проверка подлинности Windows**.</span><span class="sxs-lookup"><span data-stu-id="489e9-114">Under **Security**, select **Windows Authentication**.</span></span>

    3.  <span data-ttu-id="489e9-115">В узле **средства управления** выберите **сценарии и средства управления IIS**.</span><span class="sxs-lookup"><span data-stu-id="489e9-115">In the **Management Tools** node, select **IIS Management Scripts and Tools**.</span></span> <span data-ttu-id="489e9-116">Убедитесь, что в разделе **Совместимость управления IIS6**установлены флажки **Совместимость с метабазой IIS6** и **IIS6** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="489e9-116">Under **IIS6 Management Compatibility**, ensure that both **IIS6 Metabase Compatibility** and **IIS6 WMI Compatibility** are selected, and then click **Next**.</span></span>

5.  <span data-ttu-id="489e9-117">На странице **Подтвердите выбор установки** нажмите кнопку **установить**, а затем завершите работу мастера.</span><span class="sxs-lookup"><span data-stu-id="489e9-117">On the **Confirm Installation Selections** page, click **Install**, and then complete the rest of the wizard.</span></span>

6.  <span data-ttu-id="489e9-118">Нажмите кнопку **Закрыть** , чтобы закрыть окно **мастера добавления ролей**, а затем закройте Диспетчер серверов.</span><span class="sxs-lookup"><span data-stu-id="489e9-118">Click **Close** to exit the **Add Roles Wizard**, and then close Server Manager.</span></span>

## <span data-ttu-id="489e9-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="489e9-119">Related topics</span></span>


[<span data-ttu-id="489e9-120">Требования при развертывании Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="489e9-120">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="489e9-121">Контрольные списки развертывания и обновления Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="489e9-121">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





