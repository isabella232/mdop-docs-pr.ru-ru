---
title: Импорт приложения
description: Импорт приложения
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817402"
---
# <span data-ttu-id="7ded2-103">Импорт приложения</span><span class="sxs-lookup"><span data-stu-id="7ded2-103">How to Import an Application</span></span>


<span data-ttu-id="7ded2-104">Как правило, импортируйте приложения, чтобы они были доступны для потоковой передачи с сервера управления Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="7ded2-104">Typically, you import applications to make them available to stream from an Application Virtualization Management Server.</span></span> <span data-ttu-id="7ded2-105">Вы также можете добавить приложение вручную, но для этого необходимо предоставить точную детальную информацию о приложении.</span><span class="sxs-lookup"><span data-stu-id="7ded2-105">You can also add an application manually, but you must provide precise, detailed information about the application to do so.</span></span> <span data-ttu-id="7ded2-106">Дополнительные сведения [можно найти в разделе Добавление приложения вручную](how-to-manually-add-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="7ded2-106">For more information, see [How to Manually Add an Application](how-to-manually-add-an-application.md).</span></span>

<span data-ttu-id="7ded2-107">**Примечание**  Чтобы импортировать приложение, необходимо, чтобы на сервере была доступна программа последовательности Open Software descriptor (OSD) или файл проекта секвенсора (SPRJ).</span><span class="sxs-lookup"><span data-stu-id="7ded2-107">**Note** To import an application, you must have its sequenced Open Software Descriptor (OSD) file or its Sequencer Project (SPRJ) file available on the server.</span></span>

 

<span data-ttu-id="7ded2-108">При импорте приложения необходимо убедиться, что на сервере в поле " **путь содержимого по умолчанию** " на вкладке " **Общие** " в диалоговом окне " **Параметры** " (доступ к нему щелкните правой кнопкой мыши узел **системы Application Virtualization** на консоли App-V Server).</span><span class="sxs-lookup"><span data-stu-id="7ded2-108">When importing an application, you should make sure the server is configured with a value in the **Default Content Path** field on the **General** tab of the **System Options** dialog (accessible by right-clicking the **Application Virtualization System** node in the App-V Server Console).</span></span> <span data-ttu-id="7ded2-109">Значение Path по умолчанию определяет, где будут импортироваться приложения, и в процессе импорта это значение используется для изменения путей, определенных в OSD файле для SFT и для ярлыков значков.</span><span class="sxs-lookup"><span data-stu-id="7ded2-109">The default content path value defines where the applications will be imported, and during the import process, this value is used to modify the paths defined in the OSD file for the SFT file and for the icon shortcuts.</span></span> <span data-ttu-id="7ded2-110">В OSD — путь к SFT – файлу указан в записи HREF в базе кода, а путь к значкам указан в поле "ЯРЛЫКи".</span><span class="sxs-lookup"><span data-stu-id="7ded2-110">In the OSD file, the path for the SFT file is specified in the CODEBASE HREF entry and the path for the icons is specified in the SHORTCUTS entry.</span></span>

<span data-ttu-id="7ded2-111">В процессе импорта протокол, сервер и, если он есть, порт, указанный в этих двух путях в OSD, будет заменен значением из пути содержимого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ded2-111">During the import process, the protocol, server, and, if present, port specified in these two paths in the OSD file will be replaced with the value from the default content path.</span></span> <span data-ttu-id="7ded2-112">В таблице ниже представлен пример того, как будет использоваться путь импорта.</span><span class="sxs-lookup"><span data-stu-id="7ded2-112">The following table provides an example of how the import path will be affected.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ded2-113">Путь к содержимому по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7ded2-113">Default Content Path</span></span></th>
<th align="left"><span data-ttu-id="7ded2-114">HREF в базе кода файла OSD</span><span class="sxs-lookup"><span data-stu-id="7ded2-114">OSD File CODEBASE HREF</span></span></th>
<th align="left"><span data-ttu-id="7ded2-115">Результирующее значение</span><span class="sxs-lookup"><span data-stu-id="7ded2-115">Resulting Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ded2-116">\server\content &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="7ded2-116">\server\content&lt;/p&gt;</span></span></td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p><span data-ttu-id="7ded2-117">\server\content\myFolder\package.sft</span><span class="sxs-lookup"><span data-stu-id="7ded2-117">\server\content\myFolder\package.sft</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="7ded2-118">Импорт приложения</span><span class="sxs-lookup"><span data-stu-id="7ded2-118">To import an application</span></span>**

1.  <span data-ttu-id="7ded2-119">Щелкните правой кнопкой мыши узел **приложения** в левой области и выберите пункт **Импорт приложений**.</span><span class="sxs-lookup"><span data-stu-id="7ded2-119">Right-click the **Applications** node in the left pane, and choose **Import Applications**.</span></span>

2.  <span data-ttu-id="7ded2-120">В диалоговом окне **Открыть** перейдите в файл SPRJ или OSD приложения.</span><span class="sxs-lookup"><span data-stu-id="7ded2-120">In the **Open** dialog box, navigate to the application's SPRJ or OSD file.</span></span> <span data-ttu-id="7ded2-121">Выделите файл и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="7ded2-121">Highlight the file and click **Open**.</span></span>

3.  <span data-ttu-id="7ded2-122">В **мастере создания приложений**убедитесь, что выбрано поле **включена** для приложений, которые вы хотите пропотокировать.</span><span class="sxs-lookup"><span data-stu-id="7ded2-122">In the **New Application Wizard**, be sure the **Enabled** box is selected for applications you want to stream.</span></span> <span data-ttu-id="7ded2-123">Здесь также можно ввести описание и проверить путь к серверу и файлам.</span><span class="sxs-lookup"><span data-stu-id="7ded2-123">There you can also enter a description and verify the server and file paths.</span></span> <span data-ttu-id="7ded2-124">Кроме того, если вы настроили лицензии и группы серверов, вы можете выбрать их.</span><span class="sxs-lookup"><span data-stu-id="7ded2-124">Also, if you have set up license and server groups, you can select those.</span></span>

4.  <span data-ttu-id="7ded2-125">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7ded2-125">Click **Next**.</span></span>

5.  <span data-ttu-id="7ded2-126">На экране **опубликованные ярлыки** установите флажки для расположений, в которых вы хотите отображать ярлыки приложений на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="7ded2-126">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers.</span></span>

6.  <span data-ttu-id="7ded2-127">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7ded2-127">Click **Next**.</span></span>

7.  <span data-ttu-id="7ded2-128">В окне **сопоставления файлов** вы можете добавить в приложение новые сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="7ded2-128">In the **File Associations** screen, you can add new file associations to this application.</span></span> <span data-ttu-id="7ded2-129">Для этого нажмите кнопку **Добавить**, введите расширение (без предшествующей точки), введите описание и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7ded2-129">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

    <span data-ttu-id="7ded2-130">**Примечание**  Приложения, упорядоченные с помощью секвенсора 4,0. Заполните диалоговое окно **сопоставления файлов** при импорте или создании с помощью консоли управления.</span><span class="sxs-lookup"><span data-stu-id="7ded2-130">**Note** Applications sequenced with Sequencer 4.0 populate the **File Associations** dialog box when you import or create them through the management console.</span></span> <span data-ttu-id="7ded2-131">Приложения с более ранними версиями программы Sequencer не выполняют никаких задач.</span><span class="sxs-lookup"><span data-stu-id="7ded2-131">Applications with previous Sequencer version packages do not.</span></span>

     

8.  <span data-ttu-id="7ded2-132">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7ded2-132">Click **Next**.</span></span>

9.  <span data-ttu-id="7ded2-133">На экране **разрешения на доступ** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="7ded2-133">In the **Access Permissions** screen, click **Add**.</span></span>

10. <span data-ttu-id="7ded2-134">Заполните диалоговое окно " **Выбор групп** ".</span><span class="sxs-lookup"><span data-stu-id="7ded2-134">Complete the **Select Groups** dialog box.</span></span> <span data-ttu-id="7ded2-135">По завершении нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7ded2-135">When you finish, click **OK**.</span></span>

11. <span data-ttu-id="7ded2-136">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7ded2-136">Click **Next**.</span></span>

12. <span data-ttu-id="7ded2-137">На экране **Сводка** вы можете просмотреть настройки импорта.</span><span class="sxs-lookup"><span data-stu-id="7ded2-137">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="7ded2-138">Нажмите кнопку **Готово**или кнопку **назад** , чтобы изменить импорт, или кнопку **Отмена** , чтобы отменить импорт.</span><span class="sxs-lookup"><span data-stu-id="7ded2-138">Click **Finish**, or click **Back** to change the import or click **Cancel** to cancel the import.</span></span>

## <span data-ttu-id="7ded2-139">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7ded2-139">Related topics</span></span>


[<span data-ttu-id="7ded2-140">Управление группами приложений на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="7ded2-140">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="7ded2-141">Управление приложениями на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="7ded2-141">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="7ded2-142">Добавление приложения вручную</span><span class="sxs-lookup"><span data-stu-id="7ded2-142">How to Manually Add an Application</span></span>](how-to-manually-add-an-application.md)

 

 





