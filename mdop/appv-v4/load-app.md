---
title: LOAD APP (ЗАГРУЗИТЬ ПРИЛОЖЕНИЕ)
description: LOAD APP (ЗАГРУЗИТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: 7b727d0c-5423-419d-92ef-7ebbc6343e79
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02bd6e35da898f5b34f7efc21cbc01a72d555b8d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816249"
---
# <span data-ttu-id="7ac70-103">LOAD APP (ЗАГРУЗИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="7ac70-103">LOAD APP</span></span>


<span data-ttu-id="7ac70-104">Загружает указанное приложение и все другие приложения в пакете в кэш файловой системы.</span><span class="sxs-lookup"><span data-stu-id="7ac70-104">Loads the specified application and all other applications in the package into the file system cache.</span></span>

<span data-ttu-id="7ac70-105">**Примечание**  Команда **загрузить приложение** запускает процесс загрузки, а индикатор выполнения отображается в области уведомлений на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="7ac70-105">**Note** The **LOAD APP** command starts the load process and a progress bar is displayed in the Desktop Notification Area.</span></span> <span data-ttu-id="7ac70-106">Команда выполняется сразу после запуска этого процесса, поэтому все ошибки загрузки отображаются в одном и том же месте.</span><span class="sxs-lookup"><span data-stu-id="7ac70-106">The command exits immediately after starting this process, so any load errors are displayed in the same location.</span></span> <span data-ttu-id="7ac70-107">Если вы хотите запустить процесс загрузки из командной строки, не используя область уведомлений на рабочем столе, используйте команду **загрузить пакет** .</span><span class="sxs-lookup"><span data-stu-id="7ac70-107">Use the **LOAD PACKAGE** command if you want to start the load process from the command line without using the Desktop Notification Area.</span></span>

 

`SFTMIME LOAD APP:application [/LOG log-pathname | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ac70-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="7ac70-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="7ac70-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7ac70-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ac70-110">Приложение: &lt; приложение&gt;</span><span class="sxs-lookup"><span data-stu-id="7ac70-110">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ac70-111">Имя и версия (необязательно) загружаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="7ac70-111">The name and version (optional) of the application to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ac70-112">/LOG</span><span class="sxs-lookup"><span data-stu-id="7ac70-112">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ac70-113">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="7ac70-113">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ac70-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="7ac70-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ac70-115">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="7ac70-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7ac70-116">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="7ac70-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ac70-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="7ac70-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ac70-118">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="7ac70-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7ac70-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7ac70-119">Related topics</span></span>


[<span data-ttu-id="7ac70-120">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="7ac70-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





