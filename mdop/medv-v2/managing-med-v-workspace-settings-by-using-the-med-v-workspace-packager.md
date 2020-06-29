---
title: Управление параметрами рабочей области MED-V с помощью упаковщика рабочих областей MED-V
description: Управление параметрами рабочей области MED-V с помощью упаковщика рабочих областей MED-V
author: dansimp
ms.assetid: e4b2c516-b9f8-44f9-9eae-caac6c2af3e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9905c8da0f1f0678cce9587296526e8f04493c20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826122"
---
# <span data-ttu-id="03ffc-103">Управление параметрами рабочей области MED-V с помощью упаковщика рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="03ffc-103">Managing MED-V Workspace Settings by Using the MED-V Workspace Packager</span></span>


<span data-ttu-id="03ffc-104">Вы можете использовать диспетчер рабочих областей MED-V для управления определенными параметрами в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="03ffc-104">You can use the MED-V Workspace Packager to manage certain settings in the MED-V workspace.</span></span>

**<span data-ttu-id="03ffc-105">Управление параметрами в рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="03ffc-105">To manage settings in a MED-V workspace</span></span>**

1. <span data-ttu-id="03ffc-106">Чтобы открыть **Диспетчер рабочих областей MED-V**, нажмите **кнопку Пуск**, выберите **все программы**, а затем — **Microsoft Enterprise Virtualization**, а затем — **Диспетчер рабочих областей med-v**.</span><span class="sxs-lookup"><span data-stu-id="03ffc-106">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2. <span data-ttu-id="03ffc-107">На главной панели **диспетчера рабочих областей MED-V** щелкните **Управление параметрами**.</span><span class="sxs-lookup"><span data-stu-id="03ffc-107">On the **MED-V Workspace Packager** main panel, click **Manage Settings**.</span></span>

3. <span data-ttu-id="03ffc-108">В окне **Управление параметрами** можно настроить следующие параметры рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="03ffc-108">In the **Manage Settings** window, you can configure the following MED-V workspace settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="03ffc-109">Запуск рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="03ffc-109">Start MED-V workspace</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="03ffc-110">Укажите, следует ли запускать рабочую область MED-V при входе пользователя в систему, при первом использовании или разрешить конечному пользователю при запуске рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="03ffc-110">Choose whether to start the MED-V workspace at user logon, at first use, or to let the end user decide when the MED-V workspace starts.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="03ffc-111">Рабочая область MED-V начинается одним из двух способов: при входе пользователя в систему или при первом выполнении действия, требующего MED-V (например, при открытии опубликованного приложения или вводе URL-адреса, для которого требуется перенаправление).</span><span class="sxs-lookup"><span data-stu-id="03ffc-111">The MED-V workspace starts in one of two ways: either when the end user logs on or when they first perform an action that requires MED-V, such as opening a published application or entering a URL that requires redirection.</span></span></p>
   <p><span data-ttu-id="03ffc-112">Вы можете задать этот параметр для конечного пользователя или позволить конечному пользователю управлять тем, как запустится MED-V.</span><span class="sxs-lookup"><span data-stu-id="03ffc-112">You can either define this setting for the end user or let the end user control how MED-V starts.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="03ffc-113">Примечание.</span><span class="sxs-lookup"><span data-stu-id="03ffc-113">Note</span></span></strong><br/><p><span data-ttu-id="03ffc-114">Если вы указали, что конечный пользователь решает проблему, поведение по умолчанию — Рабочая область MED-V запускается при входе в систему.</span><span class="sxs-lookup"><span data-stu-id="03ffc-114">If you specify that the end user decides, the default behavior they experience is that the MED-V workspace starts when they log on.</span></span> <span data-ttu-id="03ffc-115">Они могут изменить значение по умолчанию, щелкнув правой кнопкой мыши значок MED-V в области уведомлений и выбрав пункт <strong> Параметры пользователя MED-v </strong> .</span><span class="sxs-lookup"><span data-stu-id="03ffc-115">They can change the default by right-clicking the MED-V icon in the notification area and selecting <strong>MED-V User Settings</strong>.</span></span> <span data-ttu-id="03ffc-116">Если вы определили этот параметр для конечного пользователя, он не сможет изменить способ запуска MED-V.</span><span class="sxs-lookup"><span data-stu-id="03ffc-116">If you define this setting for the end user, they cannot change the way in which MED-V starts.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="03ffc-117">Сеть</span><span class="sxs-lookup"><span data-stu-id="03ffc-117">Networking</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="03ffc-118">Выберите <strong> параметр Общий доступ </strong> или <strong> мост </strong> для сети.</span><span class="sxs-lookup"><span data-stu-id="03ffc-118">Select <strong>Shared</strong> or <strong>Bridged</strong> for your networking setting.</span></span> <span data-ttu-id="03ffc-119">Значение по умолчанию — <strong> Shared </strong> .</span><span class="sxs-lookup"><span data-stu-id="03ffc-119">The default is <strong>Shared</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong><span data-ttu-id="03ffc-120">Общая </strong> - Рабочая область для MED-V использует преобразование сетевых адресов (NAT) для предоставления общего доступа к узлу&#39;s IP для исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="03ffc-120">Shared</strong> - The MED-V workspace uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p>
   <p><strong><span data-ttu-id="03ffc-121">В мост </strong> - для рабочей области MED-V есть собственный сетевой адрес, обычно получаемый с помощью DHCP.</span><span class="sxs-lookup"><span data-stu-id="03ffc-121">Bridged</strong> - The MED-V workspace has its own network address, typically obtained through DHCP.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="03ffc-122">Хранение учетных данных</span><span class="sxs-lookup"><span data-stu-id="03ffc-122">Store credentials</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="03ffc-123">Укажите, нужно ли хранить учетные данные конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="03ffc-123">Choose whether you want to store the end user credentials.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="03ffc-124">По умолчанию хранение учетных данных отключено, так что конечный пользователь должен пройти проверку подлинности при каждом входе.</span><span class="sxs-lookup"><span data-stu-id="03ffc-124">The default behavior is that credential storing is disabled so that the end user must be authenticated every time that they log on.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="03ffc-125">Важно.</span><span class="sxs-lookup"><span data-stu-id="03ffc-125">Important</span></span></strong><br/><p><span data-ttu-id="03ffc-126">Несмотря на то, что кэширование учетных данных конечного пользователя обеспечивает наилучшее взаимодействие с пользователем, следует учитывать риски, связанные с этим.</span><span class="sxs-lookup"><span data-stu-id="03ffc-126">Even though caching the end user’s credentials provides the best user experience, you should be aware of the risks involved.</span></span></p>
   <p><span data-ttu-id="03ffc-127">Учетные данные домена конечного пользователя хранятся в диспетчере учетных данных Windows в обратимом формате.</span><span class="sxs-lookup"><span data-stu-id="03ffc-127">The end user’s domain credential is stored in a reversible format in the Windows Credential Manager.</span></span> <span data-ttu-id="03ffc-128">Злоумышленник может написать программу, которая получает пароль и таким образом получить доступ к учетным данным пользователя.</span><span class="sxs-lookup"><span data-stu-id="03ffc-128">An attacker could write a program that retrieves the password and thus gain access to the user’s credentials.</span></span> <span data-ttu-id="03ffc-129">Вы можете уменьшить этот риск, отключив хранение учетных данных конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="03ffc-129">You can only lessen this risk by disabling the storing of end user credentials.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



4. <span data-ttu-id="03ffc-130">Нажмите кнопку **Сохранить как...**</span><span class="sxs-lookup"><span data-stu-id="03ffc-130">Click **Save as…**</span></span> <span data-ttu-id="03ffc-131">чтобы сохранить обновленные параметры конфигурации в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="03ffc-131">to save the updated configuration settings in the specified folder.</span></span> <span data-ttu-id="03ffc-132">MED-V создает файл реестра, содержащий обновленные параметры.</span><span class="sxs-lookup"><span data-stu-id="03ffc-132">MED-V creates a registry file that contains the updated settings.</span></span> <span data-ttu-id="03ffc-133">Разверните обновленный файл реестра с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="03ffc-133">Deploy the updated registry file by using Group Policy.</span></span> <span data-ttu-id="03ffc-134">Дополнительные сведения об использовании групповой политики можно найти в разделе [Установка программного обеспечения групповой политики](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="03ffc-134">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

   <span data-ttu-id="03ffc-135">В заданной папке MED-V также создается сценарий Windows PowerShell, который можно использовать для повторного создания обновленного файла реестра.</span><span class="sxs-lookup"><span data-stu-id="03ffc-135">MED-V also creates a Windows PowerShell script in the specified folder that you can use to re-create this updated registry file.</span></span>

## <span data-ttu-id="03ffc-136">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="03ffc-136">Related topics</span></span>


[<span data-ttu-id="03ffc-137">Управление параметрами конфигурации рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="03ffc-137">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="03ffc-138">Управление параметрами рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="03ffc-138">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)









