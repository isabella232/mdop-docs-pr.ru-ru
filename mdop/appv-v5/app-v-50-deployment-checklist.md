---
title: Контрольный список по развертыванию App-V 5.0
description: Контрольный список по развертыванию App-V 5.0
author: dansimp
ms.assetid: d6d93152-82b4-4b02-8b11-ed21d3331f00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f213271a6d4b90961846b49553c07f1eb6e4c03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814845"
---
# <span data-ttu-id="60bb8-103">Контрольный список по развертыванию App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="60bb8-103">App-V 5.0 Deployment Checklist</span></span>


<span data-ttu-id="60bb8-104">Этот контрольный список можно использовать для помощи при развертывании приложений Microsoft Application Virtualization (App-V) 5,0.</span><span class="sxs-lookup"><span data-stu-id="60bb8-104">This checklist can be used to help you during Microsoft Application Virtualization (App-V) 5.0 deployment.</span></span>

**<span data-ttu-id="60bb8-105">Примечание.</span><span class="sxs-lookup"><span data-stu-id="60bb8-105">Note</span></span>**  
<span data-ttu-id="60bb8-106">В этом контрольном списке описаны рекомендуемые шаги и высокоуровневый список элементов, которые следует принимать во время развертывания функций App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="60bb8-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying App-V 5.0 features.</span></span> <span data-ttu-id="60bb8-107">Рекомендуется скопировать этот контрольный список в программу для работы с электронными таблицами и настроить ее для использования.</span><span class="sxs-lookup"><span data-stu-id="60bb8-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



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
<th align="left"><span data-ttu-id="60bb8-108">Задача</span><span class="sxs-lookup"><span data-stu-id="60bb8-108">Task</span></span></th>
<th align="left"><span data-ttu-id="60bb8-109">Ссылки</span><span class="sxs-lookup"><span data-stu-id="60bb8-109">References</span></span></th>
<th align="left"><span data-ttu-id="60bb8-110">Заметки</span><span class="sxs-lookup"><span data-stu-id="60bb8-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="60bb8-111">Заполните этап планирования для подготовки вычислительной среды к развертыванию App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="60bb8-111">Complete the planning phase to prepare the computing environment for App-V 5.0 deployment.</span></span></p></td>
<td align="left"><p><a href="app-v-50-planning-checklist.md" data-raw-source="[App-V 5.0 Planning Checklist](app-v-50-planning-checklist.md)"><span data-ttu-id="60bb8-112">Контрольный список по планированию использования App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="60bb8-112">App-V 5.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="60bb8-113">Ознакомьтесь со сведениями о конфигурациях, поддерживаемых приложением App-V 5,0, чтобы убедиться, что выбранные клиентские и серверные компьютеры поддерживаются для установки компонента App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="60bb8-113">Review the App-V 5.0 supported configurations information to make sure selected client and server computers are supported for App-V 5.0 feature installation.</span></span></p></td>
<td align="left"><p><a href="app-v-50-supported-configurations.md" data-raw-source="[App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md)"><span data-ttu-id="60bb8-114">Поддерживаемые конфигурации в App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="60bb8-114">App-V 5.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="60bb8-115">Запустите программу установки App-V 5,0, чтобы развернуть необходимые компоненты App-V 5,0 для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="60bb8-115">Run App-V 5.0 Setup to deploy the required App-V 5.0 features for your environment.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="60bb8-116">Примечание.</span><span class="sxs-lookup"><span data-stu-id="60bb8-116">Note</span></span></strong><br/><p><span data-ttu-id="60bb8-117">Следите за именами серверов и связанного URL-адреса, созданного во время установки.</span><span class="sxs-lookup"><span data-stu-id="60bb8-117">Keep track of the names of the servers and associated URL’s created during installation.</span></span> <span data-ttu-id="60bb8-118">Эти сведения будут использоваться во время установки.</span><span class="sxs-lookup"><span data-stu-id="60bb8-118">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p></p>
<ul>
<li><p><a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"><span data-ttu-id="60bb8-119">Установка программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="60bb8-119">How to Install the Sequencer</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"><span data-ttu-id="60bb8-120">Развертывание клиента App-V</span><span class="sxs-lookup"><span data-stu-id="60bb8-120">How to Deploy the App-V Client</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"><span data-ttu-id="60bb8-121">Порядок развертывания сервера App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="60bb8-121">How to Deploy the App-V 5.0 Server</span></span></a></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="60bb8-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="60bb8-122">Related topics</span></span>


[<span data-ttu-id="60bb8-123">Развертывание App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="60bb8-123">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)









