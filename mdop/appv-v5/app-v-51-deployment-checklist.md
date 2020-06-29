---
title: Контрольный список по развертыванию App-V 5.1
description: Контрольный список по развертыванию App-V 5.1
author: dansimp
ms.assetid: 44bed85a-e4f5-49d7-a308-a2b681f76372
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0864335e505996a3ea379b09de6a1aaa7fbe1676
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814773"
---
# <span data-ttu-id="372de-103">Контрольный список по развертыванию App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="372de-103">App-V 5.1 Deployment Checklist</span></span>


<span data-ttu-id="372de-104">Этот контрольный список можно использовать для помощи при развертывании приложений Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="372de-104">This checklist can be used to help you during Microsoft Application Virtualization (App-V) 5.1 deployment.</span></span>

**<span data-ttu-id="372de-105">Примечание.</span><span class="sxs-lookup"><span data-stu-id="372de-105">Note</span></span>**  
<span data-ttu-id="372de-106">В этом контрольном списке описаны рекомендуемые шаги и высокоуровневый список элементов, которые следует принимать во время развертывания функций App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="372de-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying App-V 5.1 features.</span></span> <span data-ttu-id="372de-107">Рекомендуется скопировать этот контрольный список в программу для работы с электронными таблицами и настроить ее для использования.</span><span class="sxs-lookup"><span data-stu-id="372de-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="372de-108">Задача</span><span class="sxs-lookup"><span data-stu-id="372de-108">Task</span></span></th>
<th align="left"><span data-ttu-id="372de-109">Ссылки</span><span class="sxs-lookup"><span data-stu-id="372de-109">References</span></span></th>
<th align="left"><span data-ttu-id="372de-110">Заметки</span><span class="sxs-lookup"><span data-stu-id="372de-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="372de-111">Заполните этап планирования для подготовки вычислительной среды к развертыванию App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="372de-111">Complete the planning phase to prepare the computing environment for App-V 5.1 deployment.</span></span></p></td>
<td align="left"><p><a href="app-v-51-planning-checklist.md" data-raw-source="[App-V 5.1 Planning Checklist](app-v-51-planning-checklist.md)"><span data-ttu-id="372de-112">Контрольный список по планированию использования App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="372de-112">App-V 5.1 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="372de-113">Ознакомьтесь со сведениями о конфигурациях, поддерживаемых приложением App-V 5,1, чтобы убедиться, что выбранные клиентские и серверные компьютеры поддерживаются для установки компонента App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="372de-113">Review the App-V 5.1 supported configurations information to make sure selected client and server computers are supported for App-V 5.1 feature installation.</span></span></p></td>
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"><span data-ttu-id="372de-114">Поддерживаемые конфигурации в App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="372de-114">App-V 5.1 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="372de-115">Запустите программу установки App-V 5,1, чтобы развернуть необходимые компоненты App-V 5,1 для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="372de-115">Run App-V 5.1 Setup to deploy the required App-V 5.1 features for your environment.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="372de-116">Примечание.</span><span class="sxs-lookup"><span data-stu-id="372de-116">Note</span></span></strong><br/><p><span data-ttu-id="372de-117">Следите за именами серверов и связанного URL-адреса, созданного во время установки.</span><span class="sxs-lookup"><span data-stu-id="372de-117">Keep track of the names of the servers and associated URL’s created during installation.</span></span> <span data-ttu-id="372de-118">Эти сведения будут использоваться во время установки.</span><span class="sxs-lookup"><span data-stu-id="372de-118">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p></p>
<ul>
<li><p><a href="how-to-install-the-sequencer-51beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md)"><span data-ttu-id="372de-119">Установка программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="372de-119">How to Install the Sequencer</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)"><span data-ttu-id="372de-120">Развертывание клиента App-V</span><span class="sxs-lookup"><span data-stu-id="372de-120">How to Deploy the App-V Client</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"><span data-ttu-id="372de-121">Порядок развертывания сервера App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="372de-121">How to Deploy the App-V 5.1 Server</span></span></a></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="372de-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="372de-122">Related topics</span></span>


[<span data-ttu-id="372de-123">Развертывание App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="372de-123">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)









