---
title: Виртуализация нового приложения с помощью командной строки
description: Виртуализация нового приложения с помощью командной строки
author: dansimp
ms.assetid: c3b5c842-6a91-4d0a-9a22-c7b8d1aeb09a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea7b1222dc00a0a4649cb342ac1ba41338484889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816689"
---
# <span data-ttu-id="992ae-103">Виртуализация нового приложения с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="992ae-103">How to Sequence a New Application by Using the Command Line</span></span>


<span data-ttu-id="992ae-104">Вы можете использовать командную строку для последовательного создания нового приложения.</span><span class="sxs-lookup"><span data-stu-id="992ae-104">You can use a command line to sequence a new application.</span></span> <span data-ttu-id="992ae-105">Командная строка полезна, если вам нужно создать большое количество виртуальных приложений или при необходимости создавать последовательные приложения на регулярной основе.</span><span class="sxs-lookup"><span data-stu-id="992ae-105">Using a command line is useful when you have to create a large number of virtual applications or when you need to create sequenced applications on a recurring basis.</span></span>

**<span data-ttu-id="992ae-106">Важно.</span><span class="sxs-lookup"><span data-stu-id="992ae-106">Important</span></span>**  
<span data-ttu-id="992ae-107">Последовательность команд в командной строке позволяет выполнять последовательности только по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="992ae-107">Command-line sequencing allows for default sequencing only.</span></span> <span data-ttu-id="992ae-108">Если необходимо изменить параметры установки по умолчанию для упорядоченного приложения, необходимо либо вручную изменить виртуальное приложение, либо обновить виртуальное приложение с помощью секвенсора Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="992ae-108">If you need to change default installation settings for the application you are sequencing, you must either manually modify the virtual application or update the virtual application by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="992ae-109">Дополнительные сведения об обновлении виртуального приложения с помощью секвенсора App-V вы узнаете, [как обновить существующее виртуальное приложение](how-to-upgrade-an-existing-virtual-application.md).</span><span class="sxs-lookup"><span data-stu-id="992ae-109">For more information about updating a virtual application by using the App-V Sequencer, see [How to Upgrade an Existing Virtual Application](how-to-upgrade-an-existing-virtual-application.md).</span></span>



<span data-ttu-id="992ae-110">Чтобы создать виртуальное приложение с помощью командной строки, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="992ae-110">Use the following procedure to create a virtual application by using the command line.</span></span>

**<span data-ttu-id="992ae-111">Упорядочение приложения с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="992ae-111">To sequence an application by using the command line</span></span>**

1.  <span data-ttu-id="992ae-112">На компьютере с секвенсором App-V откройте командную команду, выбрав **Пуск**, **выполнить**, а затем введите **cmd**.</span><span class="sxs-lookup"><span data-stu-id="992ae-112">On the computer that is running the App-V Sequencer, open the command prompt by selecting **Start**, **Run**, and then type **cmd**.</span></span> <span data-ttu-id="992ae-113">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="992ae-113">Click **OK**.</span></span>

2.  <span data-ttu-id="992ae-114">С помощью командной строки укажите расположение, где установлен секвенсор App-V.</span><span class="sxs-lookup"><span data-stu-id="992ae-114">Use the command prompt to specify the location of where the App-V Sequencer is installed.</span></span> <span data-ttu-id="992ae-115">Например, в командной строке введите следующую команду: **C:\\program Files Files\\Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="992ae-115">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="992ae-116">В командной строке введите следующую команду, заменив текст в кавычках на значения:</span><span class="sxs-lookup"><span data-stu-id="992ae-116">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="992ae-117">Примечание.</span><span class="sxs-lookup"><span data-stu-id="992ae-117">Note</span></span>**  
    <span data-ttu-id="992ae-118">Вы можете указать дополнительные параметры, используя командную строку, в зависимости от сложности приложения, которое вы собираетесь поочередно.</span><span class="sxs-lookup"><span data-stu-id="992ae-118">You can specify additional parameters by using the command line, depending on the complexity of the application you are sequencing.</span></span> <span data-ttu-id="992ae-119">Полный список параметров, которые можно использовать с секвенсором App-V, приведен в разделе [Параметры командной строки программы Sequencer](sequencer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="992ae-119">For a complete list of parameters that are available for use with the App-V Sequencer, see [Sequencer Command-Line Parameters](sequencer-command-line-parameters.md).</span></span>



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
<td align="left"><p>Specify the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="992ae-120">Нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="992ae-120">Press **Enter**.</span></span>

## <span data-ttu-id="992ae-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="992ae-121">Related topics</span></span>


[<span data-ttu-id="992ae-122">Создание и обновление виртуальных приложений с помощью секвенсора App-V</span><span class="sxs-lookup"><span data-stu-id="992ae-122">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[<span data-ttu-id="992ae-123">Коды ошибок командной строки программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="992ae-123">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

[<span data-ttu-id="992ae-124">Параметры командной строки программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="992ae-124">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)









