---
title: Обновление виртуального приложения с помощью командной строки
description: Обновление виртуального приложения с помощью командной строки
author: dansimp
ms.assetid: 83c97767-6ea1-42aa-b411-ccc9fa61cf81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8612deb31a1692dd85cfee88ca4b18cbc5ac2ab2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816462"
---
# <span data-ttu-id="41e40-103">Обновление виртуального приложения с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="41e40-103">How to Upgrade a Virtual Application by Using the Command Line</span></span>


<span data-ttu-id="41e40-104">Выполните описанные ниже действия, чтобы обновить виртуальное приложение с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="41e40-104">Use the following procedure to upgrade a virtual application by using a command line.</span></span>

**<span data-ttu-id="41e40-105">Обновление виртуального приложения</span><span class="sxs-lookup"><span data-stu-id="41e40-105">To upgrade a virtual application</span></span>**

1.  <span data-ttu-id="41e40-106">На компьютере, на котором запущено приложение Application Virtualization (App-V), чтобы открыть командную команду, выберите **Пуск**, **выполнить**и введите **cmd**.</span><span class="sxs-lookup"><span data-stu-id="41e40-106">On the computer that is running the Application Virtualization (App-V) Sequencer, to open the command prompt, select **Start**, **Run**, and type **cmd**.</span></span> <span data-ttu-id="41e40-107">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="41e40-107">Click **OK**.</span></span>

2.  <span data-ttu-id="41e40-108">В командной строке укажите расположение, в котором установлен секвенсор App-V.</span><span class="sxs-lookup"><span data-stu-id="41e40-108">At the command prompt, specify the location where the App-V Sequencer is installed.</span></span> <span data-ttu-id="41e40-109">Например, в командной строке введите следующую команду: **C:\\program Files Files\\Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="41e40-109">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="41e40-110">В командной строке введите следующую команду, заменив текст в кавычках на значения:</span><span class="sxs-lookup"><span data-stu-id="41e40-110">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="41e40-111">Примечание.</span><span class="sxs-lookup"><span data-stu-id="41e40-111">Note</span></span>**  
    <span data-ttu-id="41e40-112">Вы можете указать дополнительные параметры, используя командную строку в зависимости от сложности обновляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="41e40-112">You can specify additional parameters by using the command line, depending on the complexity of the application you are upgrading.</span></span> <span data-ttu-id="41e40-113">Полный список параметров, которые можно использовать с секвенсором App-V, приведен в разделе [Параметры командной строки программы Sequencer](sequencer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="41e40-113">For a complete list of parameters that are available for use with the App-V Sequencer, see [Sequencer Command-Line Parameters](sequencer-command-line-parameters.md).</span></span>



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



4. <span data-ttu-id="41e40-114">Нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="41e40-114">Press **Enter**.</span></span>

## <span data-ttu-id="41e40-115">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="41e40-115">Related topics</span></span>


[<span data-ttu-id="41e40-116">Создание и обновление виртуальных приложений с помощью секвенсора App-V</span><span class="sxs-lookup"><span data-stu-id="41e40-116">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[<span data-ttu-id="41e40-117">Коды ошибок командной строки программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="41e40-117">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

[<span data-ttu-id="41e40-118">Параметры командной строки программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="41e40-118">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)









