---
title: Установка клиента App-V 5.0 для режима хранилища общего содержимого
description: Установка клиента App-V 5.0 для режима хранилища общего содержимого
author: dansimp
ms.assetid: 88f09e6f-19e7-48ea-965a-907052d1a02f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 704ea6c1e4b1ba4670a4e52d754b8e6e5a9fb8f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814056"
---
# <span data-ttu-id="96841-103">Установка клиента App-V 5.0 для режима хранилища общего содержимого</span><span class="sxs-lookup"><span data-stu-id="96841-103">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>


<span data-ttu-id="96841-104">Выполните указанные ниже действия, чтобы установить клиент Microsoft Application Virtualization (App-V) 5,0 таким образом, чтобы он использовал режим хранилища общего содержимого App-V 5,0 (SCS).</span><span class="sxs-lookup"><span data-stu-id="96841-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 client so that it uses the App-V 5.0 Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="96841-105">Убедитесь, что все необходимые компоненты установлены на компьютере, на который планируется установить приложение.</span><span class="sxs-lookup"><span data-stu-id="96841-105">You should ensure that all required prerequisites are installed on the computer you plan to install to.</span></span> <span data-ttu-id="96841-106">Чтобы получить [необходимые требования для App-V 5,0](app-v-50-prerequisites.md), используйте следующую ссылку:</span><span class="sxs-lookup"><span data-stu-id="96841-106">Use the following link for a [App-V 5.0 Prerequisites](app-v-50-prerequisites.md).</span></span>

<span data-ttu-id="96841-107">**Примечание**  Перед выполнением этой процедуры при необходимости удалите любую существующую версию клиента App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="96841-107">**Note** Before performing this procedure if necessary uninstall any existing version of the App-V 5.0 client.</span></span>

 

<span data-ttu-id="96841-108">Дополнительные сведения о режиме SCS можно найти [в разделе Общий доступ к хранилищу содержимого в Microsoft App-V 5,0 за сценой](https://go.microsoft.com/fwlink/?LinkId=316879) ( https://go.microsoft.com/fwlink/?LinkId=316879) .</span><span class="sxs-lookup"><span data-stu-id="96841-108">For more information about SCS mode, see [Shared Content Store in Microsoft App-V 5.0 – Behind the Scenes](https://go.microsoft.com/fwlink/?LinkId=316879) (https://go.microsoft.com/fwlink/?LinkId=316879).</span></span>

**<span data-ttu-id="96841-109">Установка и Настройка клиента App-V 5,0 для режима SCS</span><span class="sxs-lookup"><span data-stu-id="96841-109">Install and configure the App-V 5.0 client for SCS mode</span></span>**

1.  <span data-ttu-id="96841-110">Скопируйте установочные файлы клиента App-V 5,0 на компьютер, на котором он будет установлен.</span><span class="sxs-lookup"><span data-stu-id="96841-110">Copy the App-V 5.0 client installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="96841-111">Откройте командную строку и в каталоге, в котором хранятся файлы установки, введите один из указанных ниже вариантов в зависимости от версии устанавливаемого клиента.</span><span class="sxs-lookup"><span data-stu-id="96841-111">Open a command line and from the directory where the installation files are saved type one of the following options depending on the version of the client you are installing:</span></span>

    -   <span data-ttu-id="96841-112">Чтобы установить версию RDS клиента App-V 5,0, введите: **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="96841-112">To install the RDS version of the App-V 5.0 client type: **appv\_client\_setup\_rds.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

    -   <span data-ttu-id="96841-113">Чтобы установить стандартную версию App-V 5,0 Client Type: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="96841-113">To install the standard version of the App-V 5.0 client type: **appv\_client\_setup.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

        <span data-ttu-id="96841-114">**Важно!**  Вы должны выполнить автоматическую установку, или установка завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="96841-114">**Important** You must perform a silent installation or the installation will fail.</span></span>

         

2.  <span data-ttu-id="96841-115">После завершения установки вы можете развернуть пакеты на компьютере, на котором запущен клиент, и все содержимое пакета будет передаваться в потоке в сети.</span><span class="sxs-lookup"><span data-stu-id="96841-115">After you have completed the installation you can deploy packages to the computer running the client and all package contents will be streamed across the network.</span></span>

    <span data-ttu-id="96841-116">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="96841-116">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="96841-117">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="96841-117">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="96841-118">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="96841-118">Got an App-V issue?</span></span>** <span data-ttu-id="96841-119">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="96841-119">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="96841-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="96841-120">Related topics</span></span>


[<span data-ttu-id="96841-121">Развертывание программы Sequencer и клиента App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="96841-121">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 





