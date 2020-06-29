---
title: Обновление пакета виртуализированного приложения с помощью командной строки
description: Обновление пакета виртуализированного приложения с помощью командной строки
author: dansimp
ms.assetid: 682fac46-c71d-4731-831b-81bfd5032764
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eade2ced43852419176f635918f0a6b7c3444aee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816489"
---
# <span data-ttu-id="f19f8-103">Обновление пакета виртуализированного приложения с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="f19f8-103">How to Upgrade a Sequenced Application Package Using the Command Line</span></span>


<span data-ttu-id="f19f8-104">Выполните описанные ниже действия, чтобы обновить виртуальное приложение с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="f19f8-104">Use the following procedure to upgrade a virtual application by using a command line.</span></span> <span data-ttu-id="f19f8-105">При обновлении существующего виртуального пакета приложения с помощью командной строки первоначальная версия sftового файла удаляется.</span><span class="sxs-lookup"><span data-stu-id="f19f8-105">When you upgrade an existing virtual application package by using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="f19f8-106">Перед обновлением пакета с помощью командной строки необходимо создать резервную копию соответствующего SFT — файла.</span><span class="sxs-lookup"><span data-stu-id="f19f8-106">You should back up the associated .sft file before upgrading the package by using the command line.</span></span>

**<span data-ttu-id="f19f8-107">Обновление виртуального приложения</span><span class="sxs-lookup"><span data-stu-id="f19f8-107">To upgrade a virtual application</span></span>**

1.  <span data-ttu-id="f19f8-108">На компьютере, на котором запущено приложение Application Virtualization (App-V), чтобы открыть командную команду, выберите **Пуск**, **выполнить**и введите **cmd**.</span><span class="sxs-lookup"><span data-stu-id="f19f8-108">On the computer that is running the Application Virtualization (App-V) Sequencer, to open the command prompt, select **Start**, **Run**, and type **cmd**.</span></span> <span data-ttu-id="f19f8-109">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f19f8-109">Click **OK**.</span></span>

2.  <span data-ttu-id="f19f8-110">В командной строке укажите расположение, в котором установлен секвенсор App-V.</span><span class="sxs-lookup"><span data-stu-id="f19f8-110">At the command prompt, specify the location where the App-V Sequencer is installed.</span></span> <span data-ttu-id="f19f8-111">Например, в командной строке введите следующую команду: **C:\\program Files Files\\Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="f19f8-111">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="f19f8-112">В командной строке введите следующую команду, заменив текст в кавычках на значения:</span><span class="sxs-lookup"><span data-stu-id="f19f8-112">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="f19f8-113">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f19f8-113">Note</span></span>**  
    <span data-ttu-id="f19f8-114">Вы можете указать дополнительные параметры, используя командную строку в зависимости от сложности обновляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="f19f8-114">You can specify additional parameters by using the command line, depending on the complexity of the application you are upgrading.</span></span> <span data-ttu-id="f19f8-115">Полный список параметров, доступных для использования с секвенсором App-V, можно найти в разделе [Параметры командной строки](command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f19f8-115">For a complete list of parameters that are available for use with the App-V Sequencer, see [Command-Line Parameters](command-line-parameters.md).</span></span>



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
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="f19f8-116">Нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="f19f8-116">Press **Enter**.</span></span>

## <span data-ttu-id="f19f8-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f19f8-117">Related topics</span></span>


[<span data-ttu-id="f19f8-118">Управление виртуальными приложениями с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="f19f8-118">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)









