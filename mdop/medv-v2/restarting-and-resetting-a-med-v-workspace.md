---
title: Перезапуск и сброс рабочей области MED-V
description: Перезапуск и сброс рабочей области MED-V
author: dansimp
ms.assetid: a959cdb3-a727-47c7-967e-e58f224e74de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48a644c2ed1668f87eb6e1a78521e780e8b783dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825422"
---
# <span data-ttu-id="1d4e7-103">Перезапуск и сброс рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="1d4e7-103">Restarting and Resetting a MED-V Workspace</span></span>


<span data-ttu-id="1d4e7-104">Во время устранения неполадок может возникнуть необходимость перезапустить или сбросить рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-104">During troubleshooting, you may sometimes find it necessary to restart or reset the MED-V workspace.</span></span> <span data-ttu-id="1d4e7-105">Перезапускайте рабочую область MED-V практически так же, как и при перезапуске физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-105">Restarting the MED-V workspace is basically the same as restarting a physical computer.</span></span> <span data-ttu-id="1d4e7-106">Сброс рабочей области MED-V повторно приводит к повторной настройке и удаляет все данные, хранящиеся на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-106">Resetting the MED-V workspace reruns first time setup and deletes all data that is stored in the virtual machine.</span></span> <span data-ttu-id="1d4e7-107">Поскольку удаляются все хранящиеся данные, обычно необходимо сбросить рабочую область MED-V, чтобы устранить наиболее существенные проблемы с поиском и восстановить предыдущую рабочую область для MED-V в рабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-107">Because all stored data is deleted, you typically should only reset the MED-V workspace to resolve the most serious troubleshooting issues, or to restore a previously working MED-V workspace back to a working state.</span></span>

<span data-ttu-id="1d4e7-108">Сведения о том, как открыть набор средств администрирования для MED-V, можно найти в разделе [Устранение неполадок с помощью средства администрирования для MED-v](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="1d4e7-108">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

**<span data-ttu-id="1d4e7-109">Перезапуск рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="1d4e7-109">Restarting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="1d4e7-110">В окне **набор средств администрирования для MED-v** нажмите кнопку **перезапустить рабочую область MED-v**.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-110">On the **MED-V Administration Toolkit** window, click **Restart MED-V Workspace**.</span></span> <span data-ttu-id="1d4e7-111">Откроется диалоговое окно, в котором нужно подтвердить необходимость перезапуска рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-111">A dialog window opens in which you must confirm that you want to restart the MED-V workspace.</span></span>

2.  <span data-ttu-id="1d4e7-112">Нажмите кнопку **перезапустить**.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-112">Click **Restart**.</span></span>

    <span data-ttu-id="1d4e7-113">Любые опубликованные приложения, которые запущены или перенаправлены на открытые веб-сайты, будут закрыты при перезапуске рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-113">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace restarts.</span></span>

**<span data-ttu-id="1d4e7-114">Сброс рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="1d4e7-114">Resetting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="1d4e7-115">В окне **набор средств администрирования для MED-v** нажмите кнопку **Сброс рабочей области для MED-v**.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-115">On the **MED-V Administration Toolkit** window, click **Reset MED-V Workspace**.</span></span> <span data-ttu-id="1d4e7-116">Откроется диалоговое окно, в котором нужно подтвердить сброс рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-116">A dialog window opens in which you must confirm that you want to reset the MED-V workspace.</span></span>

    <span data-ttu-id="1d4e7-117">**Предупреждение**  Сброс рабочей области MED-V приводит к первому запуску программы установки и, следовательно, повторной загрузке исходного виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-117">**Warning** Resetting the MED-V workspace causes first time setup to run again, and thus reloads the original virtual hard disk.</span></span> <span data-ttu-id="1d4e7-118">Все данные, которые хранятся в рабочей области MED-V с момента первоначального запуска настройки, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-118">All data that is stored in the MED-V workspace since first time setup was originally run will be deleted.</span></span>

     

2.  <span data-ttu-id="1d4e7-119">Нажмите кнопку **Сбросить**.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-119">Click **Reset**.</span></span>

    <span data-ttu-id="1d4e7-120">Любые опубликованные приложения, которые запущены или перенаправлены на открытые веб-сайты, будут закрыты при сбросе рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d4e7-120">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace resets.</span></span>

## <span data-ttu-id="1d4e7-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1d4e7-121">Related topics</span></span>


[<span data-ttu-id="1d4e7-122">Просмотр и настройка журналов MED-V</span><span class="sxs-lookup"><span data-stu-id="1d4e7-122">Viewing and Configuring MED-V Logs</span></span>](viewing-and-configuring-med-v-logs.md)

[<span data-ttu-id="1d4e7-123">Просмотр конфигураций рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="1d4e7-123">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





