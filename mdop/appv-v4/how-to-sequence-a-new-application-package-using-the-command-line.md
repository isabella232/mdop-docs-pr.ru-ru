---
title: Виртуализация нового пакета приложений с помощью командной строки
description: Виртуализация нового пакета приложений с помощью командной строки
author: dansimp
ms.assetid: de72912b-d9e7-45b5-a601-12528f1a4cac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2dd638a7e4765cedbf1d8050626fb8cc54b2ce8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816679"
---
# <span data-ttu-id="899cb-103">Виртуализация нового пакета приложений с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="899cb-103">How to Sequence a New Application Package Using the Command Line</span></span>


<span data-ttu-id="899cb-104">Вы можете использовать командную строку для последовательного создания нового приложения.</span><span class="sxs-lookup"><span data-stu-id="899cb-104">You can use a command line to sequence a new application.</span></span> <span data-ttu-id="899cb-105">Командная строка полезна, если вам нужно создать большое количество виртуальных приложений или при необходимости создавать последовательные приложения на регулярной основе.</span><span class="sxs-lookup"><span data-stu-id="899cb-105">Using a command line is useful when you have to create a large number of virtual applications or when you need to create sequenced applications on a recurring basis.</span></span>

**<span data-ttu-id="899cb-106">Важно.</span><span class="sxs-lookup"><span data-stu-id="899cb-106">Important</span></span>**  
<span data-ttu-id="899cb-107">Последовательность команд в командной строке позволяет выполнять последовательности только по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="899cb-107">Command-line sequencing allows for default sequencing only.</span></span> <span data-ttu-id="899cb-108">Если необходимо изменить параметры установки по умолчанию для упорядоченного приложения, необходимо либо вручную изменить виртуальное приложение, либо обновить виртуальное приложение с помощью секвенсора Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="899cb-108">If you need to change default installation settings for the application you are sequencing, you must either manually modify the virtual application or update the virtual application by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="899cb-109">Дополнительные сведения об обновлении виртуального приложения с помощью секвенсора App-V вы узнаете, [как обновить существующее виртуальное приложение](how-to-upgrade-an-existing-virtual-application.md).</span><span class="sxs-lookup"><span data-stu-id="899cb-109">For more information about updating a virtual application by using the App-V Sequencer, see [How to Upgrade an Existing Virtual Application](how-to-upgrade-an-existing-virtual-application.md).</span></span>



<span data-ttu-id="899cb-110">Чтобы создать виртуальное приложение с помощью командной строки, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="899cb-110">Use the following procedure to create a virtual application by using the command line.</span></span>

**<span data-ttu-id="899cb-111">Упорядочение приложения с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="899cb-111">To sequence an application by using the command line</span></span>**

1.  <span data-ttu-id="899cb-112">На компьютере с секвенсором App-V откройте командную команду, выбрав **Пуск**, **выполнить**, а затем введите **cmd**.</span><span class="sxs-lookup"><span data-stu-id="899cb-112">On the computer that is running the App-V Sequencer, open the command prompt by selecting **Start**, **Run**, and then type **cmd**.</span></span> <span data-ttu-id="899cb-113">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="899cb-113">Click **OK**.</span></span>

2.  <span data-ttu-id="899cb-114">С помощью командной строки укажите расположение, где установлен секвенсор App-V.</span><span class="sxs-lookup"><span data-stu-id="899cb-114">Use the command prompt to specify the location of where the App-V Sequencer is installed.</span></span> <span data-ttu-id="899cb-115">Например, в командной строке введите следующую команду: **C:\\program Files Files\\Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="899cb-115">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="899cb-116">В командной строке введите следующую команду, заменив текст в кавычках на значения:</span><span class="sxs-lookup"><span data-stu-id="899cb-116">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="899cb-117">Примечание.</span><span class="sxs-lookup"><span data-stu-id="899cb-117">Note</span></span>**  
    <span data-ttu-id="899cb-118">Вы можете указать дополнительные параметры, используя командную строку, в зависимости от сложности приложения, которое вы собираетесь поочередно.</span><span class="sxs-lookup"><span data-stu-id="899cb-118">You can specify additional parameters by using the command line, depending on the complexity of the application you are sequencing.</span></span> <span data-ttu-id="899cb-119">Полный список параметров, доступных для использования с секвенсором App-V, можно найти в разделе [Командная строка Application Virtualization Sequencer](application-virtualization-sequencer-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="899cb-119">For a complete list of parameters that are available for use with the App-V Sequencer, see [Application Virtualization Sequencer Command Line](application-virtualization-sequencer-command-line.md).</span></span>



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specifies the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="899cb-120">Нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="899cb-120">Press **Enter**.</span></span>

## <span data-ttu-id="899cb-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="899cb-121">Related topics</span></span>


[<span data-ttu-id="899cb-122">Управление виртуальными приложениями с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="899cb-122">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)









