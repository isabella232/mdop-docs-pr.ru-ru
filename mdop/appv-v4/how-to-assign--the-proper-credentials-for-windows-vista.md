---
title: Назначение правильных учетных данных для Windows Vista
description: Назначение правильных учетных данных для Windows Vista
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821369"
---
# <span data-ttu-id="f2134-103">Назначение правильных учетных данных для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2134-103">How to Assign the Proper Credentials for Windows Vista</span></span>


<span data-ttu-id="f2134-104">Чтобы настроить клиент App-V для настольных учетных данных WindowsVista, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f2134-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsVista credentials.</span></span>

<span data-ttu-id="f2134-105">**Примечание**  Эту процедуру необходимо выполнить на всех компьютерах, не подключенных к домену.</span><span class="sxs-lookup"><span data-stu-id="f2134-105">**Note** This procedure must be completed on each non-domain joined computer.</span></span> <span data-ttu-id="f2134-106">В зависимости от количества компьютеров, не подключенных к домену, в вашей среде это может быть очень утомительным действием.</span><span class="sxs-lookup"><span data-stu-id="f2134-106">Depending on the number of non-domain joined computers in your environment, this could be a very tedious operation.</span></span> <span data-ttu-id="f2134-107">Вы можете использовать сценарии и интерфейс командной строки для диспетчера учетных данных, чтобы помочь администраторам автоматизировать этот процесс.</span><span class="sxs-lookup"><span data-stu-id="f2134-107">You can use scripts and the command-line interface for Credential Manager to help administrators automate this process.</span></span>

 

**<span data-ttu-id="f2134-108">Назначение правильных учетных данных для клиентов App-V, работающих под управлением Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2134-108">To assign the proper credentials for App-V clients running Windows Vista</span></span>**

1.  <span data-ttu-id="f2134-109">С правами администратора на клиентском компьютере App-V, работающем под управлением Windows Vista, откройте панель управления **учетные записи пользователей** (классическая панель управления).</span><span class="sxs-lookup"><span data-stu-id="f2134-109">With administrator privileges on the App-V Desktop Client running Windows Vista, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="f2134-110">Выберите " **Управление сетевыми паролями** " для **учетных записей пользователей** в области "оставшиеся задачи".</span><span class="sxs-lookup"><span data-stu-id="f2134-110">Select **Manage your network passwords** from **User Accounts** in the left tasks pane.</span></span>

3.  <span data-ttu-id="f2134-111">На экране "Добавление **сохраненных имен пользователей и паролей** " нажмите кнопку **Добавить** .</span><span class="sxs-lookup"><span data-stu-id="f2134-111">Select **Add** on the **Stored User Names and Passwords** screen.</span></span>

4.  <span data-ttu-id="f2134-112">На экране **Свойства сохраненных учетных данных** укажите сведения о инфраструктуре App-V.</span><span class="sxs-lookup"><span data-stu-id="f2134-112">On the **Stored Credential Properties** screen, provide the information for the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="f2134-113">**Вход в учетную запись:** Внешнее имя сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="f2134-113">**Log on to:** External name of the publishing server.</span></span>

    2.  <span data-ttu-id="f2134-114">**Имя пользователя:** Имя пользователя для внешнего пользователя в форме Domain\\Username.</span><span class="sxs-lookup"><span data-stu-id="f2134-114">**User name:** User name for the external user in the form Domain\\Username.</span></span>

    3.  <span data-ttu-id="f2134-115">**Password (пароль):** Пароль учетной записи пользователя, введенной в поле **имя пользователя** .</span><span class="sxs-lookup"><span data-stu-id="f2134-115">**Password:** Password for the user account entered in the **User name** field.</span></span>

    4.  <span data-ttu-id="f2134-116">Оставьте выбранный **тип учетных данных** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2134-116">Leave **Credential Type** selected, and click **OK**.</span></span>

5.  <span data-ttu-id="f2134-117">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="f2134-117">Click **Close**.</span></span> <span data-ttu-id="f2134-118">Учетные данные хранятся в хранилище учетных данных для надлежащей проверки подлинности в инфраструктуре App-V.</span><span class="sxs-lookup"><span data-stu-id="f2134-118">The credentials are stored in the credential store for proper authentication to the App-V infrastructure.</span></span>

## <span data-ttu-id="f2134-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f2134-119">Related topics</span></span>


[<span data-ttu-id="f2134-120">Присоединенные к домену и не присоединенные к домену клиенты</span><span class="sxs-lookup"><span data-stu-id="f2134-120">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="f2134-121">Назначение правильных учетных данных для Windows XP</span><span class="sxs-lookup"><span data-stu-id="f2134-121">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





