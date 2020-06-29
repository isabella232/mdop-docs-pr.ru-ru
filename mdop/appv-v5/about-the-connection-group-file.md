---
title: О файле связывающей группы
description: О файле связывающей группы
author: dansimp
ms.assetid: bfeb6013-a7ca-4e36-9fe3-229702e83f0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e5cb93326ce182d71de0f0f89cc569823d6154e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814933"
---
# <span data-ttu-id="47af4-103">О файле связывающей группы</span><span class="sxs-lookup"><span data-stu-id="47af4-103">About the Connection Group File</span></span>


**<span data-ttu-id="47af4-104">В этой статье:</span><span class="sxs-lookup"><span data-stu-id="47af4-104">In this topic:</span></span>**

-   [<span data-ttu-id="47af4-105">Назначение и расположение файла в группе подключения</span><span class="sxs-lookup"><span data-stu-id="47af4-105">Connection group file purpose and location</span></span>](#bkmk-cg-purpose-loc)

-   [<span data-ttu-id="47af4-106">Структура XML-файла группы подключения</span><span class="sxs-lookup"><span data-stu-id="47af4-106">Structure of the connection group XML file</span></span>](#bkmk-define-cg-5-0sp3)

-   [<span data-ttu-id="47af4-107">Настройка приоритета пакетов в группе подключения</span><span class="sxs-lookup"><span data-stu-id="47af4-107">Configuring the priority of packages in a connection group</span></span>](#bkmk-config-pkg-priority-incg)

-   [<span data-ttu-id="47af4-108">Поддерживаемые конфигурации подключений виртуальных приложений</span><span class="sxs-lookup"><span data-stu-id="47af4-108">Supported virtual application connection configurations</span></span>](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a><span data-ttu-id="47af4-109">Назначение и расположение файла в группе подключения</span><span class="sxs-lookup"><span data-stu-id="47af4-109">Connection group file purpose and location</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47af4-110">Назначение группы соединения</span><span class="sxs-lookup"><span data-stu-id="47af4-110">Connection group purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="47af4-111">Группа подключений — это функция App-V, позволяющая группировать пакеты вместе, чтобы создать виртуальную среду, в которой приложения в этих пакетах могут взаимодействовать друг с другом.</span><span class="sxs-lookup"><span data-stu-id="47af4-111">A connection group is an App-V feature that enables you to group packages together to create a virtual environment in which the applications in those packages can interact with each other.</span></span></p>
<p><span data-ttu-id="47af4-112">Пример: вы хотите использовать подключаемые модули в Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="47af4-112">Example: You want to use plug-ins with Microsoft Office.</span></span> <span data-ttu-id="47af4-113">Вы можете создать пакет, содержащий подключаемые модули, и создать другой пакет, содержащий Office, а затем добавить оба пакета в группу подключения, чтобы позволить Office использовать эти подключаемые модули.</span><span class="sxs-lookup"><span data-stu-id="47af4-113">You can create a package that contains the plug-ins, and create another package that contains Office, and then add both packages to a connection group to enable Office to use those plug-ins.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47af4-114">Как работает файл группы подключения</span><span class="sxs-lookup"><span data-stu-id="47af4-114">How the connection group file works</span></span></p></td>
<td align="left"><p><span data-ttu-id="47af4-115">При применении файла группы подключения Application Virtualization 5,0 пакеты, перечисленные в файле, будут объединяться во время выполнения в одну виртуальную среду.</span><span class="sxs-lookup"><span data-stu-id="47af4-115">When you apply an Application Virtualization 5.0 connection group file, the packages that are enumerated in the file will be combined at runtime into a single virtual environment.</span></span> <span data-ttu-id="47af4-116">С помощью файла группы подключения Microsoft Application Virtualization (App-V) 5,0 можно настроить существующие группы соединений для Application Virtualization 5,0.</span><span class="sxs-lookup"><span data-stu-id="47af4-116">Use the Microsoft Application Virtualization (App-V) 5.0 connection group file to configure existing Application Virtualization 5.0 connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47af4-117">Пример пути к файлу</span><span class="sxs-lookup"><span data-stu-id="47af4-117">Example file path</span></span></p></td>
<td align="left"><p><span data-ttu-id="47af4-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span><span class="sxs-lookup"><span data-stu-id="47af4-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups{6CCC7575-162E-4152-9407-ED411DA138F4}{4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a><span data-ttu-id="47af4-119">Структура XML-файла группы подключения</span><span class="sxs-lookup"><span data-stu-id="47af4-119">Structure of the connection group XML file</span></span>


**<span data-ttu-id="47af4-120">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="47af4-120">In this section:</span></span>**

-   [<span data-ttu-id="47af4-121">Параметры, определяющие группу соединения</span><span class="sxs-lookup"><span data-stu-id="47af4-121">Parameters that define the connection group</span></span>](#bkmk-params-define-cg)

-   [<span data-ttu-id="47af4-122">Параметры, определяющие пакеты в группе "соединение"</span><span class="sxs-lookup"><span data-stu-id="47af4-122">Parameters that define the packages in the connection group</span></span>](#bkmk-params-define-pkgs-incg)

-   [<span data-ttu-id="47af4-123">Пример XML-файла для группы подключения приложения (SP3) 5,0</span><span class="sxs-lookup"><span data-stu-id="47af4-123">App-V 5.0 SP3 example connection group XML file</span></span>](#bkmk-50sp3-exp-cg-xml)

-   [<span data-ttu-id="47af4-124">Приложение App-V 5,0 с помощью App-V 5,0 SP2 пример XML-файла группы подключения</span><span class="sxs-lookup"><span data-stu-id="47af4-124">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a><span data-ttu-id="47af4-125">Параметры, определяющие группу соединения</span><span class="sxs-lookup"><span data-stu-id="47af4-125">Parameters that define the connection group</span></span>

<span data-ttu-id="47af4-126">В приведенной ниже таблице описаны параметры XML-файла, в котором определена сама группа подключения, а не пакеты.</span><span class="sxs-lookup"><span data-stu-id="47af4-126">The following table describes the parameters in the XML file that define the connection group itself, not the packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47af4-127">Поле</span><span class="sxs-lookup"><span data-stu-id="47af4-127">Field</span></span></th>
<th align="left"><span data-ttu-id="47af4-128">Описание</span><span class="sxs-lookup"><span data-stu-id="47af4-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47af4-129">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="47af4-129">Schema name</span></span></p></td>
<td align="left"><p><span data-ttu-id="47af4-130">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="47af4-130">Name of the schema.</span></span></p>
<p><strong><span data-ttu-id="47af4-131">Применимо, начиная с версии App-V 5,0 SP3 </strong> : Если вы хотите использовать новые функции "дополнительные пакеты" и "использовать любую версию", описанные в этой таблице, необходимо указать в XML-файле следующую схему:</span><span class="sxs-lookup"><span data-stu-id="47af4-131">Applicable starting in App-V 5.0 SP3</strong>: If you want to use the new “optional packages” and “use any version” features that are described in this table, you must specify the following schema in the XML file:</span></span></p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47af4-132">AppConnectionGroupId</span><span class="sxs-lookup"><span data-stu-id="47af4-132">AppConnectionGroupId</span></span></p></td>
<td align="left"><p><span data-ttu-id="47af4-133">Уникальный идентификатор GUID для этой группы подключения.</span><span class="sxs-lookup"><span data-stu-id="47af4-133">Unique GUID identifier for this connection group.</span></span> <span data-ttu-id="47af4-134">Состояние группы подключения сопоставлено с этим идентификатором.</span><span class="sxs-lookup"><span data-stu-id="47af4-134">The connection group state is associated with this identifier.</span></span> <span data-ttu-id="47af4-135">Указывайте этот идентификатор только при создании группы подключения.</span><span class="sxs-lookup"><span data-stu-id="47af4-135">Specify this identifier only when you create the connection group.</span></span></p>
<p><span data-ttu-id="47af4-136">Вы можете создать новый идентификатор GUID, введя: <strong>[Guid]::NewGuid()</strong> .</span><span class="sxs-lookup"><span data-stu-id="47af4-136">You can create a new GUID by typing: <strong>[Guid]::NewGuid()</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47af4-137">VersionId</span><span class="sxs-lookup"><span data-stu-id="47af4-137">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="47af4-138">Идентификатор GUID версии для этой версии группы подключения.</span><span class="sxs-lookup"><span data-stu-id="47af4-138">Version GUID identifier for this version of the connection group.</span></span></p>
<p><span data-ttu-id="47af4-139">При обновлении группы подключения (например, при добавлении или обновлении нового пакета) необходимо обновить GUID версии, чтобы он отражал новую версию.</span><span class="sxs-lookup"><span data-stu-id="47af4-139">When you update a connection group (for example, by adding or updating a new package), you must update the version GUID to reflect the new version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47af4-140">DisplayName</span><span class="sxs-lookup"><span data-stu-id="47af4-140">DisplayName</span></span></p></td>
<td align="left"><p><span data-ttu-id="47af4-141">Отображаемое имя группы подключения.</span><span class="sxs-lookup"><span data-stu-id="47af4-141">Display name of the connection group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47af4-142">Priority</span><span class="sxs-lookup"><span data-stu-id="47af4-142">Priority</span></span></p></td>
<td align="left"><p><span data-ttu-id="47af4-143">Необязательное поле приоритета для группы подключения.</span><span class="sxs-lookup"><span data-stu-id="47af4-143">Optional priority field for the connection group.</span></span></p>
<p><strong><span data-ttu-id="47af4-144">0 </strong> - указывает высший приоритет.</span><span class="sxs-lookup"><span data-stu-id="47af4-144">“0”</strong> - indicates the highest priority.</span></span></p>
<p><span data-ttu-id="47af4-145">Если требуется задать приоритет, но он не настроен, произойдет сбой пакета, так как не будет определена нужная группа подключения.</span><span class="sxs-lookup"><span data-stu-id="47af4-145">If a priority is required, but has not been configured, the package will fail because the correct connection group to use cannot be determined.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a><span data-ttu-id="47af4-146">Параметры, определяющие пакеты в группе "соединение"</span><span class="sxs-lookup"><span data-stu-id="47af4-146">Parameters that define the packages in the connection group</span></span>

<span data-ttu-id="47af4-147">В &lt; разделе Packages &gt; XML-файла группы подключения вы перечислите пакеты участников в группе подключение, указав уникальный идентификатор пакета и идентификатор версии каждого пакета, как описано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="47af4-147">In the &lt;Packages&gt; section of the connection group XML file, you list the member packages in the connection group by specifying each package’s unique package identifier and version identifier, as described in the following table.</span></span> <span data-ttu-id="47af4-148">Первый пакет в списке имеет наивысший приоритет.</span><span class="sxs-lookup"><span data-stu-id="47af4-148">The first package in the list has the highest precedence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47af4-149">Поле</span><span class="sxs-lookup"><span data-stu-id="47af4-149">Field</span></span></th>
<th align="left"><span data-ttu-id="47af4-150">Описание</span><span class="sxs-lookup"><span data-stu-id="47af4-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47af4-151">PackageId</span><span class="sxs-lookup"><span data-stu-id="47af4-151">PackageId</span></span></p></td>
<td align="left"><p><span data-ttu-id="47af4-152">Уникальный идентификатор GUID для этого пакета.</span><span class="sxs-lookup"><span data-stu-id="47af4-152">Unique GUID identifier for this package.</span></span> <span data-ttu-id="47af4-153">Этот идентификатор GUID не меняется, когда публикуются более новые версии пакета.</span><span class="sxs-lookup"><span data-stu-id="47af4-153">This GUID doesn’t change when newer versions of the package are published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47af4-154">VersionId</span><span class="sxs-lookup"><span data-stu-id="47af4-154">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="47af4-155">Уникальный идентификатор GUID для версии пакета.</span><span class="sxs-lookup"><span data-stu-id="47af4-155">Unique GUID identifier for the version of the package.</span></span></p>
<p><strong><span data-ttu-id="47af4-156">Применимо начиная с App-V 5,0 SP3 </strong> : Если вы задаете <strong> "\*" </strong> для версии пакета, динамически вставляется идентификатор GUID последней доступной версии пакета.</span><span class="sxs-lookup"><span data-stu-id="47af4-156">Applicable starting in App-V 5.0 SP3</strong>: If you specify <strong>“\*”</strong> for the package version, the GUID of the latest available package version is dynamically inserted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47af4-157">Функция "переключатель"</span><span class="sxs-lookup"><span data-stu-id="47af4-157">IsOptional</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="47af4-158">Применимо в App-V 5,0 SP3 </strong> : параметр, который позволяет сделать пакет необязательным в группе подключения.</span><span class="sxs-lookup"><span data-stu-id="47af4-158">Applicable starting in App-V 5.0 SP3</strong>: Parameter that enables you to make a package optional within the connection group.</span></span> <span data-ttu-id="47af4-159">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="47af4-159">Valid entries are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="47af4-160">"истина" </strong> — пакет является необязательным в группе "соединение"</span><span class="sxs-lookup"><span data-stu-id="47af4-160">“true”</strong> – package is optional in the connection group</span></span></p></li>
<li><p><strong><span data-ttu-id="47af4-161">"ложь" </strong> — в группе "соединение" требуется пакет</span><span class="sxs-lookup"><span data-stu-id="47af4-161">“false”</strong> – package is required in the connection group</span></span></p></li>
</ul>
<p><span data-ttu-id="47af4-162">Узнайте <a href="how-to-use-optional-packages-in-connection-groups.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md)"> , как использовать дополнительные пакеты в группах соединений </a> .</span><span class="sxs-lookup"><span data-stu-id="47af4-162">See <a href="how-to-use-optional-packages-in-connection-groups.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md)">How to Use Optional Packages in Connection Groups</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a><span data-ttu-id="47af4-163">Пример XML-файла для группы подключения приложения (SP3) 5,0</span><span class="sxs-lookup"><span data-stu-id="47af4-163">App-V 5.0 SP3 example connection group XML file</span></span>

<span data-ttu-id="47af4-164">Ниже приведен пример XML-файла группы подключения, в котором показаны примеры полей в предыдущих таблицах, а также выделены новые элементы для App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="47af4-164">The following example connection group XML file shows examples of the fields in the previous tables and highlights the items that are new for App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup 
   xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"  
   Priority="0"  
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="*"
         IsOptional=”true”
      />    
     <appv:Package
        PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
        VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
        IsOptional="false"
     />  
   </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a><span data-ttu-id="47af4-165">Приложение App-V 5,0 с помощью App-V 5,0 SP2 пример XML-файла группы подключения</span><span class="sxs-lookup"><span data-stu-id="47af4-165">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>

<span data-ttu-id="47af4-166">Следующий пример XML-файла группы подключения применим к приложению App-V 5,0 с помощью App-v 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="47af4-166">The following example connection group XML file applies to App-V 5.0 through App-V 5.0 SP2.</span></span> <span data-ttu-id="47af4-167">В нем показаны примеры полей в предыдущей таблице, но исключены описанные выше изменения для App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="47af4-167">It shows examples of the fields in the previous table, but it excludes the changes described above for App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup
   xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
   Priority="0"
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package``      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
      />
      <appv:Package
         PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
         VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      />
   </appv:Packages>
</appv:AppConnectionGroup
 ```

## <a href="" id="bkmk-config-pkg-priority-incg"></a><span data-ttu-id="47af4-168">Настройка приоритета пакетов в группе подключения</span><span class="sxs-lookup"><span data-stu-id="47af4-168">Configuring the priority of packages in a connection group</span></span>


<span data-ttu-id="47af4-169">Приоритет пакета настраивается с помощью порядка списка пакетов.</span><span class="sxs-lookup"><span data-stu-id="47af4-169">Package precedence is configured using the package list order.</span></span> <span data-ttu-id="47af4-170">Первый пакет в документе имеет наивысший приоритет.</span><span class="sxs-lookup"><span data-stu-id="47af4-170">The first package in the document has the highest precedence.</span></span> <span data-ttu-id="47af4-171">Последующие пакеты в списке имеют убывающий приоритет.</span><span class="sxs-lookup"><span data-stu-id="47af4-171">Subsequent packages in the list have descending priority.</span></span>

<span data-ttu-id="47af4-172">Приоритет пакета — это разрешение, которое может быть ненеизбежным конфликтом ресурсов при инициализации виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="47af4-172">Package precedence is the resolution for otherwise inevitable resource collisions during virtual environment initialization.</span></span> <span data-ttu-id="47af4-173">Например, если два пакета, открываемые в одной виртуальной среде, имеют одинаковый параметр Registry, то пакет с наивысшим приоритетом определяет значение, которое задается.</span><span class="sxs-lookup"><span data-stu-id="47af4-173">For example, if two packages that are opening in the same virtual environment define the same registry DWORD value, the package with the highest precedence determines the value that is set.</span></span>

<span data-ttu-id="47af4-174">С помощью файла группы подключения можно настроить каждую группу подключений, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="47af4-174">You can use the connection group file to configure each connection group by using the following methods:</span></span>

-   <span data-ttu-id="47af4-175">Укажите приоритеты выполнения для групп подключения.</span><span class="sxs-lookup"><span data-stu-id="47af4-175">Specify runtime priorities for connection groups.</span></span>

    <span data-ttu-id="47af4-176">**Примечание**  Priority требуется только в том случае, если пакет связан с несколькими группами соединений.</span><span class="sxs-lookup"><span data-stu-id="47af4-176">**Note** Priority is required only if the package is associated with more than one connection group.</span></span>

     

-   <span data-ttu-id="47af4-177">Укажите приоритет пакета в группе подключение.</span><span class="sxs-lookup"><span data-stu-id="47af4-177">Specify package precedence within the connection group.</span></span>

<span data-ttu-id="47af4-178">Поле «приоритет» является обязательным, если запущенное виртуальное приложение запускается из запроса собственного приложения, например проводник Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="47af4-178">The priority field is required when a running virtual application initiates from a native application request, for example, Microsoft Windows Explorer.</span></span> <span data-ttu-id="47af4-179">Клиент App-V использует приоритет, чтобы определить, в какой группе подключения должна выполняться приложение.</span><span class="sxs-lookup"><span data-stu-id="47af4-179">The App-V client uses the priority to determine which connection group virtual environment the application should run in.</span></span> <span data-ttu-id="47af4-180">Такая ситуация возникает, если виртуальное приложение входит в состав нескольких групп подключения.</span><span class="sxs-lookup"><span data-stu-id="47af4-180">This situation occurs if a virtual application is part of multiple connection groups.</span></span>

<span data-ttu-id="47af4-181">Если виртуальное приложение открыто с помощью другого виртуального приложения, будет использоваться виртуальная среда исходного виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="47af4-181">If a virtual application is opened using another virtual application the virtual environment of the original virtual application will be used.</span></span> <span data-ttu-id="47af4-182">В этом случае поле «приоритет» не используется.</span><span class="sxs-lookup"><span data-stu-id="47af4-182">The priority field is not used in this case.</span></span>

**<span data-ttu-id="47af4-183">Пример.</span><span class="sxs-lookup"><span data-stu-id="47af4-183">Example:</span></span>**

<span data-ttu-id="47af4-184">Виртуальное приложение Microsoft Outlook работает в виртуальной среде **XYZ**.</span><span class="sxs-lookup"><span data-stu-id="47af4-184">The virtual application Microsoft Outlook is running in virtual environment **XYZ**.</span></span> <span data-ttu-id="47af4-185">Когда вы открываете прикрепленный документ Microsoft Word, в виртуальной среде **XYZ**открывается виртуализированная версия Microsoft Word, независимо от того, какие из виртуализированных групп подключений и приоритетов среды выполнения соответствует Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="47af4-185">When you open an attached Microsoft Word document, a virtualized version Microsoft Word opens in the virtual environment **XYZ**, regardless of the virtualized Microsoft Word’s associated connection groups or runtime priorities.</span></span>

## <a href="" id="bkmk-va-conn-configs"></a><span data-ttu-id="47af4-186">Поддерживаемые конфигурации подключений виртуальных приложений</span><span class="sxs-lookup"><span data-stu-id="47af4-186">Supported virtual application connection configurations</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47af4-187">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="47af4-187">Configuration</span></span></th>
<th align="left"><span data-ttu-id="47af4-188">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="47af4-188">Example scenario</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47af4-189">Массив.</span><span class="sxs-lookup"><span data-stu-id="47af4-189">An.</span></span> <span data-ttu-id="47af4-190">EXE-файл и надстройка (DLL)</span><span class="sxs-lookup"><span data-stu-id="47af4-190">exe file and plug-in (.dll)</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="47af4-191">Вы хотите распространить Microsoft Office для всех пользователей, но распространите плагин Microsoft Excel только на подмножество пользователей.</span><span class="sxs-lookup"><span data-stu-id="47af4-191">You want to distribute Microsoft Office to all users, but distribute a Microsoft Excel plug-in to only a subset of users.</span></span></p></li>
<li><p><span data-ttu-id="47af4-192">Включите группу подключения для соответствующих пользователей.</span><span class="sxs-lookup"><span data-stu-id="47af4-192">Enable the connection group for the appropriate users.</span></span></p></li>
<li><p><span data-ttu-id="47af4-193">Обновляйте каждый пакет по отдельности по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="47af4-193">Update each package individually as required.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47af4-194">Массив.</span><span class="sxs-lookup"><span data-stu-id="47af4-194">An.</span></span> <span data-ttu-id="47af4-195">EXE-файл и приложение по промежуточного слоя</span><span class="sxs-lookup"><span data-stu-id="47af4-195">exe file and a middleware application</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="47af4-196">Для работы приложения требуется приложение по промежуточного слоя или несколько приложений, которые зависят от одной и той же версии среды выполнения промежуточного слоя.</span><span class="sxs-lookup"><span data-stu-id="47af4-196">You have an application requires a middleware application, or several applications that all depend on the same middleware runtime version.</span></span></p></li>
<li><p><span data-ttu-id="47af4-197">Все компьютеры, на которых требуется одно или несколько приложений, получают группы подключений с приложением и средой выполнения приложения по промежуточного слоя.</span><span class="sxs-lookup"><span data-stu-id="47af4-197">All computers that require one or more of the applications receive the connection groups with the application and middleware application runtime.</span></span></p></li>
<li><p><span data-ttu-id="47af4-198">При необходимости вы можете объединить несколько приложений по промежуточного слоя в одну группу подключения.</span><span class="sxs-lookup"><span data-stu-id="47af4-198">You can optionally combine multiple middleware applications into a single connection group.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47af4-199">Пример.</span><span class="sxs-lookup"><span data-stu-id="47af4-199">Example</span></span></th>
<th align="left"><span data-ttu-id="47af4-200">Пример описания</span><span class="sxs-lookup"><span data-stu-id="47af4-200">Example description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47af4-201">Группа виртуальных подключений приложений для финансового подразделения</span><span class="sxs-lookup"><span data-stu-id="47af4-201">Virtual application connection group for the financial division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="47af4-202">Приложение по промежуточного слоя 1</span><span class="sxs-lookup"><span data-stu-id="47af4-202">Middleware application 1</span></span></p></li>
<li><p><span data-ttu-id="47af4-203">Приложение по промежуточного слоя 2</span><span class="sxs-lookup"><span data-stu-id="47af4-203">Middleware application 2</span></span></p></li>
<li><p><span data-ttu-id="47af4-204">Приложение по промежуточного слоя 3</span><span class="sxs-lookup"><span data-stu-id="47af4-204">Middleware application 3</span></span></p></li>
<li><p><span data-ttu-id="47af4-205">Среда выполнения приложения по промежуточного слоя</span><span class="sxs-lookup"><span data-stu-id="47af4-205">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47af4-206">Группа подключений виртуальных приложений для отдела кадров</span><span class="sxs-lookup"><span data-stu-id="47af4-206">Virtual application connection group for HR division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="47af4-207">Приложение по промежуточного слоя 5</span><span class="sxs-lookup"><span data-stu-id="47af4-207">Middleware application 5</span></span></p></li>
<li><p><span data-ttu-id="47af4-208">Приложение по слоям 6</span><span class="sxs-lookup"><span data-stu-id="47af4-208">Middleware application 6</span></span></p></li>
<li><p><span data-ttu-id="47af4-209">Среда выполнения приложения по промежуточного слоя</span><span class="sxs-lookup"><span data-stu-id="47af4-209">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47af4-210">Массив.</span><span class="sxs-lookup"><span data-stu-id="47af4-210">An.</span></span> <span data-ttu-id="47af4-211">EXE файл и exe</span><span class="sxs-lookup"><span data-stu-id="47af4-211">exe file and an .exe file</span></span></p></td>
<td align="left"><p><span data-ttu-id="47af4-212">У вас есть приложение, которое использует другое приложение и хотите, чтобы пакеты были разделены для эффективности работы, ограничения лицензирования или развертывания временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="47af4-212">You have an application that relies on another application, and you want to keep the packages separate for operational efficiencies, licensing restrictions, or rollout timelines.</span></span></p>
<p><strong><span data-ttu-id="47af4-213">Пример.</span><span class="sxs-lookup"><span data-stu-id="47af4-213">Example:</span></span></strong></p>
<p><span data-ttu-id="47af4-214">Если вы развертываете Microsoft Lync 2010, вы можете использовать три пакета:</span><span class="sxs-lookup"><span data-stu-id="47af4-214">If you are deploying Microsoft Lync 2010, you can use three packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="47af4-215">Microsoft Office2010</span><span class="sxs-lookup"><span data-stu-id="47af4-215">Microsoft Office2010</span></span></p></li>
<li><p><span data-ttu-id="47af4-216">Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="47af4-216">Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="47af4-217">Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="47af4-217">Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="47af4-218">Вы можете управлять развертыванием с помощью следующих групп соединений:</span><span class="sxs-lookup"><span data-stu-id="47af4-218">You can manage the deployment using the following connection groups:</span></span></p>
<ul>
<li><p><span data-ttu-id="47af4-219">Microsoft Office2010 и Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="47af4-219">Microsoft Office2010 and Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="47af4-220">Microsoft Office2010 и Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="47af4-220">Microsoft Office2010 and Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="47af4-221">После завершения развертывания вы можете либо создать один новый пакет Microsoft Office2010 + Microsoft Lync2010, либо сохранить и сохранить его в виде отдельных пакетов и развернуть с помощью группы подключения.</span><span class="sxs-lookup"><span data-stu-id="47af4-221">When the deployment has completed, you can either create a single new Microsoft Office2010 + Microsoft Lync2010 package, or keep and maintain them as separate packages and deploy them by using a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="47af4-222">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="47af4-222">Related topics</span></span>


[<span data-ttu-id="47af4-223">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="47af4-223">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





