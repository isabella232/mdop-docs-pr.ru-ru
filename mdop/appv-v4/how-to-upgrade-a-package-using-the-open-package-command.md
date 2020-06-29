---
title: Обновление пакета с помощью команды "Открыть пакет"
description: Обновление пакета с помощью команды "Открыть пакет"
author: dansimp
ms.assetid: 67c10440-de8a-4547-a34b-f83206d0cc3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cca438fe90373e8f934d1d790246544cdf46fa18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816519"
---
# <span data-ttu-id="a1178-103">Обновление пакета с помощью команды "Открыть пакет"</span><span class="sxs-lookup"><span data-stu-id="a1178-103">How to Upgrade a Package Using the Open Package Command</span></span>


<span data-ttu-id="a1178-104">С помощью команды Open Package обновите или установите обновление для серийного пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="a1178-104">Use the Open Package command to upgrade or apply an update to a sequenced application package.</span></span> <span data-ttu-id="a1178-105">При обновлении существующего виртуального пакета приложения с помощью командной строки первоначальная версия sftового файла удаляется.</span><span class="sxs-lookup"><span data-stu-id="a1178-105">When you upgrade an existing virtual application package using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="a1178-106">Перед обновлением пакета с помощью командной строки необходимо создать резервную копию соответствующего SFT — файла.</span><span class="sxs-lookup"><span data-stu-id="a1178-106">You should backup the associated .sft file before upgrading the package using the command line.</span></span>

**<span data-ttu-id="a1178-107">Обновление пакета с помощью команды "открыть пакет"</span><span class="sxs-lookup"><span data-stu-id="a1178-107">To upgrade a package using the Open Package command</span></span>**

1.  <span data-ttu-id="a1178-108">Чтобы открыть пакет, который будет обновлен, на консоли Application Virtualization (App-V) выберите **файл**, **Открыть пакет для обновления**.</span><span class="sxs-lookup"><span data-stu-id="a1178-108">To open the package that will be upgraded, in the Application Virtualization (App-V) console select **File**, **Open Package for Upgrade**.</span></span> <span data-ttu-id="a1178-109">В диалоговом окне **Открытие** файла выберите пакет, который будет обновлен.</span><span class="sxs-lookup"><span data-stu-id="a1178-109">In the **Open** dialog box, select the package that will be upgraded.</span></span>

2.  <span data-ttu-id="a1178-110">Чтобы запустить мастер **виртуализации** , выберите **инструменты**, **Мастер упорядочивания**.</span><span class="sxs-lookup"><span data-stu-id="a1178-110">To start the **Sequencing** wizard, select **Tools**, **Sequencing Wizard**.</span></span> <span data-ttu-id="a1178-111">Завершите работу мастера и примените изменения конфигурации, чтобы сохранить новое упорядоченное приложение, выберите **файл**, **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a1178-111">Complete the wizard applying the configuration changes, to save the new sequenced application, select **File**, **Save**.</span></span>

3.  <span data-ttu-id="a1178-112">Чтобы добавить номер версии в имя пакета, на консоли секвенсор выберите **Сервис**, **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="a1178-112">To append the version number to the package name, in the Sequencer console, select **Tools**, **Options**.</span></span> <span data-ttu-id="a1178-113">Выберите **Добавить версию пакета в имя файла**.</span><span class="sxs-lookup"><span data-stu-id="a1178-113">Select **Append Package Version to Filename**.</span></span> <span data-ttu-id="a1178-114">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1178-114">Click **OK**.</span></span>

    <span data-ttu-id="a1178-115">**Важно!**  Обновление имени файла с использованием версии пакета является обязательным для успешного завершения обновления.</span><span class="sxs-lookup"><span data-stu-id="a1178-115">**Important** Updating the file name with the package version is essential to successfully completing the upgrade.</span></span>

     

## <span data-ttu-id="a1178-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a1178-116">Related topics</span></span>


[<span data-ttu-id="a1178-117">Управление виртуальными приложениями с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="a1178-117">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





