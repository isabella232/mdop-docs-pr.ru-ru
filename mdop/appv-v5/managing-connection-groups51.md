---
title: Управление связывающими группами
description: Управление связывающими группами
author: dansimp
ms.assetid: 22c9d3cb-7246-4173-9742-4ba1c24b0a6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c89fab70fa13a66c2c27b8d014a5bac034f21bd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813573"
---
# <span data-ttu-id="1aa22-103">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="1aa22-103">Managing Connection Groups</span></span>


<span data-ttu-id="1aa22-104">Группы подключений позволяют приложениям в пакете взаимодействовать друг с другом в виртуальной среде, в то время как они остаются изолированными от остальной части системы.</span><span class="sxs-lookup"><span data-stu-id="1aa22-104">Connection groups enable the applications within a package to interact with each other in the virtual environment, while remaining isolated from the rest of the system.</span></span> <span data-ttu-id="1aa22-105">С помощью групп подключений администраторы могут управлять пакетами независимо друг от друга и могут не добавлять одно и то же приложение несколько повторов на клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="1aa22-105">By using connection groups, administrators can manage packages independently and can avoid having to add the same application multiple times to a client computer.</span></span>

<span data-ttu-id="1aa22-106">**Примечание**  В некоторых предыдущих версиях App-V группы соединений назывались разкомпозицией динамических наборов.</span><span class="sxs-lookup"><span data-stu-id="1aa22-106">**Note** In some previous versions of App-V, connection groups were referred to as Dynamic Suite Composition.</span></span>

 

**<span data-ttu-id="1aa22-107">В этой статье:</span><span class="sxs-lookup"><span data-stu-id="1aa22-107">In this topic:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="about-the-connection-group-virtual-environment51.md" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment51.md)"><span data-ttu-id="1aa22-108">О виртуальной среде связывающей группы</span><span class="sxs-lookup"><span data-stu-id="1aa22-108">About the Connection Group Virtual Environment</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="1aa22-109">Описывает виртуальную среду "Группа подключений".</span><span class="sxs-lookup"><span data-stu-id="1aa22-109">Describes the connection group virtual environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="about-the-connection-group-file51.md" data-raw-source="[About the Connection Group File](about-the-connection-group-file51.md)"><span data-ttu-id="1aa22-110">О файле связывающей группы</span><span class="sxs-lookup"><span data-stu-id="1aa22-110">About the Connection Group File</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="1aa22-111">Описание файла группы подключения.</span><span class="sxs-lookup"><span data-stu-id="1aa22-111">Describes the connection group file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-create-a-connection-group51.md" data-raw-source="[How to Create a Connection Group](how-to-create-a-connection-group51.md)"><span data-ttu-id="1aa22-112">Создание связывающей группы</span><span class="sxs-lookup"><span data-stu-id="1aa22-112">How to Create a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="1aa22-113">В этой статье объясняется, как создать новую группу подключения.</span><span class="sxs-lookup"><span data-stu-id="1aa22-113">Explains how to create a new connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages51.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages51.md)"><span data-ttu-id="1aa22-114">Создание связывающей группы с опубликованными пользователями и глобально опубликованными пакетами</span><span class="sxs-lookup"><span data-stu-id="1aa22-114">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="1aa22-115">В этой статье объясняется, как создать новую группу подключений, которая содержит смесь пакетов, опубликованных для пользователя и опубликованных глобально.</span><span class="sxs-lookup"><span data-stu-id="1aa22-115">Explains how to create a new connection group that contains a mix of packages that are published to the user and published globally.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-delete-a-connection-group51.md" data-raw-source="[How to Delete a Connection Group](how-to-delete-a-connection-group51.md)"><span data-ttu-id="1aa22-116">Удаление связывающей группы</span><span class="sxs-lookup"><span data-stu-id="1aa22-116">How to Delete a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="1aa22-117">В этой статье объясняется, как удалить группу подключения.</span><span class="sxs-lookup"><span data-stu-id="1aa22-117">Explains how to delete a connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-publish-a-connection-group51.md" data-raw-source="[How to Publish a Connection Group](how-to-publish-a-connection-group51.md)"><span data-ttu-id="1aa22-118">Публикация группы соединений</span><span class="sxs-lookup"><span data-stu-id="1aa22-118">How to Publish a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="1aa22-119">В этой статье объясняется, как опубликовать группу подключения.</span><span class="sxs-lookup"><span data-stu-id="1aa22-119">Explains how to publish a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="1aa22-120">Другие ресурсы для групп соединения App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="1aa22-120">Other resources for App-V 5.1 connection groups</span></span>


-   [<span data-ttu-id="1aa22-121">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="1aa22-121">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





