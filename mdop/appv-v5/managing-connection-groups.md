---
title: Управление связывающими группами
description: Управление связывающими группами
author: dansimp
ms.assetid: 1a9c8f26-f421-4b70-b7e2-da8118e8198c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2e57b9dbe56072e6049e8fabef5705c374d022c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813581"
---
# <span data-ttu-id="3296a-103">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="3296a-103">Managing Connection Groups</span></span>


<span data-ttu-id="3296a-104">Группы подключений позволяют приложениям в пакете взаимодействовать друг с другом в виртуальной среде, в то время как они остаются изолированными от остальной части системы.</span><span class="sxs-lookup"><span data-stu-id="3296a-104">Connection groups enable the applications within a package to interact with each other in the virtual environment, while remaining isolated from the rest of the system.</span></span> <span data-ttu-id="3296a-105">С помощью групп подключений администраторы могут управлять пакетами независимо друг от друга и могут не добавлять одно и то же приложение несколько повторов на клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="3296a-105">By using connection groups, administrators can manage packages independently and can avoid having to add the same application multiple times to a client computer.</span></span>

<span data-ttu-id="3296a-106">**Примечание**  В предыдущих версиях App-V 5,0 группы соединений назывались динамическим набором.</span><span class="sxs-lookup"><span data-stu-id="3296a-106">**Note** In previous versions of App-V 5.0, connection groups were referred to as Dynamic Suite Composition.</span></span>

 

**<span data-ttu-id="3296a-107">В этой статье:</span><span class="sxs-lookup"><span data-stu-id="3296a-107">In this topic:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md)"><span data-ttu-id="3296a-108">О виртуальной среде связывающей группы</span><span class="sxs-lookup"><span data-stu-id="3296a-108">About the Connection Group Virtual Environment</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="3296a-109">Описывает виртуальную среду "Группа подключений".</span><span class="sxs-lookup"><span data-stu-id="3296a-109">Describes the connection group virtual environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="about-the-connection-group-file.md" data-raw-source="[About the Connection Group File](about-the-connection-group-file.md)"><span data-ttu-id="3296a-110">О файле связывающей группы</span><span class="sxs-lookup"><span data-stu-id="3296a-110">About the Connection Group File</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="3296a-111">Описание файла группы подключения.</span><span class="sxs-lookup"><span data-stu-id="3296a-111">Describes the connection group file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-create-a-connection-group.md" data-raw-source="[How to Create a Connection Group](how-to-create-a-connection-group.md)"><span data-ttu-id="3296a-112">Создание связывающей группы</span><span class="sxs-lookup"><span data-stu-id="3296a-112">How to Create a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="3296a-113">В этой статье объясняется, как создать новую группу подключения.</span><span class="sxs-lookup"><span data-stu-id="3296a-113">Explains how to create a new connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="3296a-114">Создание связывающей группы с опубликованными пользователями и глобально опубликованными пакетами</span><span class="sxs-lookup"><span data-stu-id="3296a-114">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="3296a-115">В этой статье объясняется, как создать новую группу подключений, которая содержит смесь пакетов, опубликованных для пользователя и опубликованных глобально.</span><span class="sxs-lookup"><span data-stu-id="3296a-115">Explains how to create a new connection group that contains a mix of packages that are published to the user and published globally.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-delete-a-connection-group.md" data-raw-source="[How to Delete a Connection Group](how-to-delete-a-connection-group.md)"><span data-ttu-id="3296a-116">Удаление связывающей группы</span><span class="sxs-lookup"><span data-stu-id="3296a-116">How to Delete a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="3296a-117">В этой статье объясняется, как удалить группу подключения.</span><span class="sxs-lookup"><span data-stu-id="3296a-117">Explains how to delete a connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-publish-a-connection-group.md" data-raw-source="[How to Publish a Connection Group](how-to-publish-a-connection-group.md)"><span data-ttu-id="3296a-118">Публикация группы соединений</span><span class="sxs-lookup"><span data-stu-id="3296a-118">How to Publish a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="3296a-119">В этой статье объясняется, как опубликовать группу подключения.</span><span class="sxs-lookup"><span data-stu-id="3296a-119">Explains how to publish a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="3296a-120">Другие ресурсы для групп соединения App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3296a-120">Other resources for App-V 5.0 connection groups</span></span>


-   [<span data-ttu-id="3296a-121">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3296a-121">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





