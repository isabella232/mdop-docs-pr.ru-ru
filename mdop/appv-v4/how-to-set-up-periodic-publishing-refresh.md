---
title: Настройка периодического обновления публикаций
description: Настройка периодического обновления публикаций
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816552"
---
# <span data-ttu-id="bdf67-103">Настройка периодического обновления публикаций</span><span class="sxs-lookup"><span data-stu-id="bdf67-103">How to Set Up Periodic Publishing Refresh</span></span>


<span data-ttu-id="bdf67-104">Вы можете использовать описанную ниже процедуру, чтобы настроить клиент для периодического обновления сведений о публикации на серверах App-V.</span><span class="sxs-lookup"><span data-stu-id="bdf67-104">You can use the following procedure to configure the client to periodically refresh the publishing information from the App-V servers.</span></span> <span data-ttu-id="bdf67-105">После настройки клиента операция обновления выполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="bdf67-105">After the client is configured, the refresh operation is automatic.</span></span> <span data-ttu-id="bdf67-106">Эти параметры настраивают параметры по умолчанию для клиента, чтобы все пользователи на этом компьютере могли видеть одинаковые параметры.</span><span class="sxs-lookup"><span data-stu-id="bdf67-106">These settings configure the default settings for the client so that all users on this computer will see the same settings.</span></span>

<span data-ttu-id="bdf67-107">**Примечание**  После выполнения этой процедуры публикуемые данные будут обновляться в соответствии с новыми параметрами после первого обновления при входе.</span><span class="sxs-lookup"><span data-stu-id="bdf67-107">**Note** After you have performed this procedure, the publishing information will be refreshed according to the new settings after the first refresh at login.</span></span> <span data-ttu-id="bdf67-108">При первом обновлении сервер может изменить параметры компьютера различными параметрами, в зависимости от того, как оно настроено.</span><span class="sxs-lookup"><span data-stu-id="bdf67-108">When this first refresh occurs, the server might override the computer settings with different settings, depending on how it is configured.</span></span> <span data-ttu-id="bdf67-109">На вкладке " **Обновление** " в диалоговом окне " **свойства** " отображаются локально настроенные параметры клиентского компьютера и все параметры, которые могут быть настроены для пользователя сервером публикации.</span><span class="sxs-lookup"><span data-stu-id="bdf67-109">The **Refresh** tab in the **Properties** dialog box shows the locally configured client computer settings and any settings that might have been configured for the user by the publishing server.</span></span>

 

**<span data-ttu-id="bdf67-110">Периодическое обновление данных публикации с серверов Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="bdf67-110">To periodically refresh the publishing information from the Application Virtualization Servers</span></span>**

1.  <span data-ttu-id="bdf67-111">В области **область** выберите пункт **Серверы публикаций** .</span><span class="sxs-lookup"><span data-stu-id="bdf67-111">Click **Publishing Servers** in the **Scope** pane.</span></span>

2.  <span data-ttu-id="bdf67-112">В области **результатов** щелкните правой кнопкой мыши нужный сервер и выберите в контекстном меню пункт **свойства** .</span><span class="sxs-lookup"><span data-stu-id="bdf67-112">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up-menu.</span></span>

3.  <span data-ttu-id="bdf67-113">В диалоговом окне **Свойства** на вкладке **Обновление** установите флажок **обновлять конфигурацию каждый раз** и введите число, представляющее частоту в поле.</span><span class="sxs-lookup"><span data-stu-id="bdf67-113">In the **Properties** dialog box, on the **Refresh** tab, select the **Refresh configuration every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="bdf67-114">Затем в раскрывающемся меню выберите **минуты**, **часы**и **дни** .</span><span class="sxs-lookup"><span data-stu-id="bdf67-114">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span>

    <span data-ttu-id="bdf67-115">**Примечание**  Этот параметр приведет к тому, что клиент обновит данные публикации каждый раз, когда истечет указанный вами период времени.</span><span class="sxs-lookup"><span data-stu-id="bdf67-115">**Note** This setting will cause the client to refresh publishing information every time the configured period elapses.</span></span> <span data-ttu-id="bdf67-116">Если пользователь не вошел в систему при выполнении обновления, обновление будет происходить при следующем входе пользователя.</span><span class="sxs-lookup"><span data-stu-id="bdf67-116">If the user is not logged in when it's time to do a refresh, the refresh will take place when the user next logs in.</span></span> <span data-ttu-id="bdf67-117">Затем таймер запускается еще раз в течение следующего периода.</span><span class="sxs-lookup"><span data-stu-id="bdf67-117">The timer is then started again for the next period.</span></span>

     

4.  <span data-ttu-id="bdf67-118">Нажмите кнопку **Применить** , чтобы изменить конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="bdf67-118">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="bdf67-119">Завершив настройку сервера, нажмите кнопку **ОК** , чтобы закрыть диалоговое окно и вернуться в консоль управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="bdf67-119">When you finish configuring the server, click **OK** to exit the dialog box and return to the Application Virtualization Client Management Console.</span></span>

## <span data-ttu-id="bdf67-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="bdf67-120">Related topics</span></span>


[<span data-ttu-id="bdf67-121">Настройка клиента в консоли управления клиентом Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="bdf67-121">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





