---
title: Удаление клиента App-V
description: Удаление клиента App-V
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816522"
---
# <span data-ttu-id="3c391-103">Удаление клиента App-V</span><span class="sxs-lookup"><span data-stu-id="3c391-103">How to Uninstall the App-V Client</span></span>


<span data-ttu-id="3c391-104">Выполните описанные ниже действия, чтобы удалить клиент Application Virtualization с компьютера.</span><span class="sxs-lookup"><span data-stu-id="3c391-104">Use the following procedure to uninstall the Application Virtualization Client from the computer.</span></span>

**<span data-ttu-id="3c391-105">Удаление клиентского компьютера Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="3c391-105">To uninstall the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="3c391-106">На панели управления дважды щелкните элемент **Установка и удаление программ** (или в Windows Vista, **программы и компоненты**), а затем дважды щелкните **клиентское приложение Microsoft Application Virtualization для настольных систем**.</span><span class="sxs-lookup"><span data-stu-id="3c391-106">In Control Panel, double-click **Add or Remove Programs** (or in Windows Vista, **Programs and Features**), and then double-click **Microsoft Application Virtualization Desktop Client**.</span></span>

2.  <span data-ttu-id="3c391-107">В появившемся диалоговом окне нажмите кнопку **Да** , чтобы продолжить процесс удаления.</span><span class="sxs-lookup"><span data-stu-id="3c391-107">In the dialog box that appears, click **Yes** to continue with the uninstall process.</span></span>

    <span data-ttu-id="3c391-108">**Важно!**  Процесс удаления не может быть отменен или прерван.</span><span class="sxs-lookup"><span data-stu-id="3c391-108">**Important** The uninstall process cannot be canceled or interrupted.</span></span>

     

3.  <span data-ttu-id="3c391-109">Когда появится сообщение о том, что приложение клиентской панели Microsoft Application Virtualization должно быть закрыто, прежде чем продолжить работу, щелкните правой кнопкой мыши значок App-V в области уведомлений и выберите команду **выход** , чтобы закрыть приложение.</span><span class="sxs-lookup"><span data-stu-id="3c391-109">When a message stating that the Microsoft Application Virtualization Client Tray application must be closed before continuing appears, right-click the App-V icon in the notification area and select **Exit** to close the application.</span></span> <span data-ttu-id="3c391-110">Затем нажмите кнопку **"повторить"** , чтобы продолжить процесс удаления.</span><span class="sxs-lookup"><span data-stu-id="3c391-110">Then click **Retry** to continue with the uninstall process.</span></span>

    <span data-ttu-id="3c391-111">**Важно!**  Может появиться сообщение о том, что одно или несколько виртуальных приложений используются.</span><span class="sxs-lookup"><span data-stu-id="3c391-111">**Important** You might see a message stating that one or more virtual applications are in use.</span></span> <span data-ttu-id="3c391-112">Закройте все открытые приложения и сохраните данные, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="3c391-112">Close any open applications and save your data before you continue.</span></span> <span data-ttu-id="3c391-113">Затем нажмите кнопку **ОК** , чтобы продолжить процесс удаления.</span><span class="sxs-lookup"><span data-stu-id="3c391-113">Then click **OK** to continue with the uninstall process.</span></span>

     

4.  <span data-ttu-id="3c391-114">Индикатор выполнения показывает оставшееся время.</span><span class="sxs-lookup"><span data-stu-id="3c391-114">A progress bar shows the time remaining.</span></span> <span data-ttu-id="3c391-115">После завершения этого действия необходимо перезагрузить компьютер, чтобы все связанные с ним драйверы были остановлены для завершения процесса удаления.</span><span class="sxs-lookup"><span data-stu-id="3c391-115">When this step finishes, you must restart the computer so that all associated drivers can be stopped to complete the uninstall process.</span></span>

    <span data-ttu-id="3c391-116">**Примечание**  После завершения процесса удаления остались следующие разделы реестра:</span><span class="sxs-lookup"><span data-stu-id="3c391-116">**Note** The following registry keys remain after the uninstall process is complete:</span></span>

    -   <span data-ttu-id="3c391-117">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span><span class="sxs-lookup"><span data-stu-id="3c391-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span></span>

    -   <span data-ttu-id="3c391-118">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span><span class="sxs-lookup"><span data-stu-id="3c391-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span></span>

    -   <span data-ttu-id="3c391-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard "клиент" = DWORD: 00000000</span><span class="sxs-lookup"><span data-stu-id="3c391-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard"Client"=dword:00000000</span></span>

    -   <span data-ttu-id="3c391-120">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span><span class="sxs-lookup"><span data-stu-id="3c391-120">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span></span>

     

## <span data-ttu-id="3c391-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3c391-121">Related topics</span></span>


[<span data-ttu-id="3c391-122">Установка клиента с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="3c391-122">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="3c391-123">Установка клиента Application Virtualization Client вручную</span><span class="sxs-lookup"><span data-stu-id="3c391-123">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="3c391-124">Публикация виртуального приложения на клиенте</span><span class="sxs-lookup"><span data-stu-id="3c391-124">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 





