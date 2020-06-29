---
title: О виртуальной среде связывающей группы
description: О виртуальной среде связывающей группы
author: dansimp
ms.assetid: 535fa640-cbd9-425e-8437-94650a70c264
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bd93c9e7acbf7bbf3f9da506d5d95b8df09e1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814909"
---
# <span data-ttu-id="276c8-103">О виртуальной среде связывающей группы</span><span class="sxs-lookup"><span data-stu-id="276c8-103">About the Connection Group Virtual Environment</span></span>


**<span data-ttu-id="276c8-104">В этой статье:</span><span class="sxs-lookup"><span data-stu-id="276c8-104">In this topic:</span></span>**

-   [<span data-ttu-id="276c8-105">Определение приоритета пакета</span><span class="sxs-lookup"><span data-stu-id="276c8-105">How package priority is determined</span></span>](#bkmk-pkg-priority-deter)

-   [<span data-ttu-id="276c8-106">Слияние одинаковых путей к пакетам в один виртуальный каталог в группах подключений</span><span class="sxs-lookup"><span data-stu-id="276c8-106">Merging identical package paths into one virtual directory in connection groups</span></span>](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a><span data-ttu-id="276c8-107">Определение приоритета пакета</span><span class="sxs-lookup"><span data-stu-id="276c8-107">How package priority is determined</span></span>


<span data-ttu-id="276c8-108">Виртуальная среда и ее текущее состояние связаны с группой подключения, а не с отдельными пакетами.</span><span class="sxs-lookup"><span data-stu-id="276c8-108">The virtual environment and its current state are associated with the connection group, not with the individual packages.</span></span> <span data-ttu-id="276c8-109">Если пакет App-V удален из группы подключения, то состояние, которое существовало как часть группы соединения, не будет перенесено вместе с пакетом.</span><span class="sxs-lookup"><span data-stu-id="276c8-109">If an App-V package is removed from the connection group, the state that existed as part of the connection group will not migrate with the package.</span></span>

<span data-ttu-id="276c8-110">Если один и тот же пакет входит в две разные группы соединения, необходимо указать, какая группа подключения должна использоваться приложением App-V.</span><span class="sxs-lookup"><span data-stu-id="276c8-110">If the same package is a part of two different connection groups, you have to indicate which connection group App-V should use.</span></span> <span data-ttu-id="276c8-111">Например, в группе подключения может быть два пакета, каждый из которых определяет одинаковый параметр Registry.</span><span class="sxs-lookup"><span data-stu-id="276c8-111">For example, you might have two packages in a connection group that each define the same registry DWORD value.</span></span>

<span data-ttu-id="276c8-112">Используемая Группа соединения основывается на порядке, в котором пакет находится в XML-документе **AppConnectionGroup** :</span><span class="sxs-lookup"><span data-stu-id="276c8-112">The connection group that is used is based on the order in which a package appears inside the **AppConnectionGroup** XML document:</span></span>

-   <span data-ttu-id="276c8-113">Первый пакет имеет наивысший приоритет.</span><span class="sxs-lookup"><span data-stu-id="276c8-113">The first package has the highest precedence.</span></span>

-   <span data-ttu-id="276c8-114">Второй пакет имеет второй наивысший приоритет.</span><span class="sxs-lookup"><span data-stu-id="276c8-114">The second package has the second highest precedence.</span></span>

<span data-ttu-id="276c8-115">Ниже приведен примерный раздел.</span><span class="sxs-lookup"><span data-stu-id="276c8-115">Consider the following example section:</span></span>

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

<span data-ttu-id="276c8-116">Предполагается, что параметр DWORD ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region) определен в первом и третьем пакете, например:</span><span class="sxs-lookup"><span data-stu-id="276c8-116">Assume that same DWORD value ABC (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region) is defined in the first and third package, such as:</span></span>

-   <span data-ttu-id="276c8-117">Пакет 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5</span><span class="sxs-lookup"><span data-stu-id="276c8-117">Package 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5</span></span>

-   <span data-ttu-id="276c8-118">Пакет 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10</span><span class="sxs-lookup"><span data-stu-id="276c8-118">Package 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=10</span></span>

<span data-ttu-id="276c8-119">Поскольку сначала появляется пакет 1, в виртуальной среде AppConnectionGroup будет указано значение 5 (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5).</span><span class="sxs-lookup"><span data-stu-id="276c8-119">Since Package 1 appears first, the AppConnectionGroup's virtual environment will have the single DWORD value of 5 (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5).</span></span> <span data-ttu-id="276c8-120">Это означает, что виртуальные приложения в пакете 1, пакет 2 и пакет 3 будут видеть значение 5 при запросе HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region.</span><span class="sxs-lookup"><span data-stu-id="276c8-120">This means that the virtual applications in Package 1, Package 2, and Package 3 will all see the value 5 when they query for HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region.</span></span>

<span data-ttu-id="276c8-121">Другие виртуальные ресурсы среды разрешаются аналогичным образом, но в обычном случае конфликт происходит в реестре.</span><span class="sxs-lookup"><span data-stu-id="276c8-121">Other virtual environment resources are resolved similarly, but the usual case is that the collisions occur in the registry.</span></span>

## <a href="" id="bkmk-merged-root-ve-exp"></a><span data-ttu-id="276c8-122">Слияние одинаковых путей к пакетам в один виртуальный каталог в группах подключений</span><span class="sxs-lookup"><span data-stu-id="276c8-122">Merging identical package paths into one virtual directory in connection groups</span></span>


<span data-ttu-id="276c8-123">Если несколько пакетов в группе подключения содержат одинаковые пути к каталогам, они объединяются в один виртуальный каталог в виртуальной среде "Группа подключения".</span><span class="sxs-lookup"><span data-stu-id="276c8-123">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span> <span data-ttu-id="276c8-124">Это объединение путей позволяет приложению в одном пакете получить доступ к файлам в другом пакете.</span><span class="sxs-lookup"><span data-stu-id="276c8-124">This merging of paths allows an application in one package to access files that are in a different package.</span></span>

<span data-ttu-id="276c8-125">При удалении пакета из группы подключения приложения, удаленные из этого пакета, больше не смогут получать доступ к файлам в остальных пакетах в группе подключения.</span><span class="sxs-lookup"><span data-stu-id="276c8-125">When you remove a package from a connection group, the applications in that removed package are no longer able to access files in the remaining packages in the connection group.</span></span>

<span data-ttu-id="276c8-126">Порядок, в котором приложение App-V ищет имя файла в группе подключения, определяется порядком, в котором пакеты App-V указаны в файле манифеста группы подключения.</span><span class="sxs-lookup"><span data-stu-id="276c8-126">The order in which App-V looks up a file’s name in the connection group is specified by the order in which the App-V packages are listed in the connection group manifest file.</span></span>

<span data-ttu-id="276c8-127">В следующем примере показан порядок и связь поиска имени файла в группе подключения для **пакета а** и **пакета B**.</span><span class="sxs-lookup"><span data-stu-id="276c8-127">The following example shows the order and relationship of a file name lookup in a connection group for **Package A** and **Package B**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="276c8-128">Упаковка</span><span class="sxs-lookup"><span data-stu-id="276c8-128">Package A</span></span></th>
<th align="left"><span data-ttu-id="276c8-129">Пакет B</span><span class="sxs-lookup"><span data-stu-id="276c8-129">Package B</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="276c8-130">C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="276c8-130">C:\Windows\System32</span></span></p></td>
<td align="left"><p><span data-ttu-id="276c8-131">C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="276c8-131">C:\Windows\System32</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="276c8-132">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="276c8-132">C:\AppTest</span></span></p></td>
<td align="left"><p><span data-ttu-id="276c8-133">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="276c8-133">C:\AppTest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="276c8-134">В приведенном выше примере после того, как виртуализированное приложение пытается найти конкретный файл, сначала выполняется поиск в пакете A для соответствующего пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="276c8-134">In the example above, when a virtualized application tries to find a specific file, Package A is searched first for a matching file path.</span></span> <span data-ttu-id="276c8-135">Если соответствующий путь не найден, выполняется поиск пакета B, используя следующие правила сопоставления.</span><span class="sxs-lookup"><span data-stu-id="276c8-135">If a matching path is not found, Package B is searched, using the following mapping rules:</span></span>

-   <span data-ttu-id="276c8-136">Если файл с именем **test.txt** существует в той же иерархии виртуальных папок в обоих пакетах приложения, используется первый совпадающий файл.</span><span class="sxs-lookup"><span data-stu-id="276c8-136">If a file named **test.txt** exists in the same virtual folder hierarchy in both application packages, the first matching file is used.</span></span>

-   <span data-ttu-id="276c8-137">Если файл с именем **bar.txt** существует в иерархии виртуальных папок одного пакета приложения, но не в другом, используется первый совпадающий файл.</span><span class="sxs-lookup"><span data-stu-id="276c8-137">If a file named **bar.txt** exists in the virtual folder hierarchy of one application package, but not in the other, the first matching file is used.</span></span>






## <span data-ttu-id="276c8-138">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="276c8-138">Related topics</span></span>


[<span data-ttu-id="276c8-139">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="276c8-139">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





