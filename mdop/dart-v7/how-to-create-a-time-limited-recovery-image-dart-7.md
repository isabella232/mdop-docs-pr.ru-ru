---
title: Создание образа для восстановления с ограничением по времени
description: Создание образа для восстановления с ограничением по времени
author: dansimp
ms.assetid: d2e29cac-c24c-4239-997f-0320b8a830ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a11891753f80d41f0089311771b906865950337c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812632"
---
# <span data-ttu-id="08672-103">Создание образа для восстановления с ограничением по времени</span><span class="sxs-lookup"><span data-stu-id="08672-103">How to Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="08672-104">Вы можете создать изображение для восстановления DaRT, которое может быть использовано только в течение определенного количества дней после его создания.</span><span class="sxs-lookup"><span data-stu-id="08672-104">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="08672-105">Для этого необходимо запустить **Мастер создания образа для восстановления DaRT** в командной строке и указать количество дней.</span><span class="sxs-lookup"><span data-stu-id="08672-105">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

**<span data-ttu-id="08672-106">Создание образа восстановления с ограничением по времени</span><span class="sxs-lookup"><span data-stu-id="08672-106">To create a recovery image that has a time limit</span></span>**

1.  <span data-ttu-id="08672-107">Откройте командную строка с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="08672-107">Open a Command Prompt with administrator credentials.</span></span>

2.  <span data-ttu-id="08672-108">Перейдите в папку, в которой находится программа ERDC.exe.</span><span class="sxs-lookup"><span data-stu-id="08672-108">Change the directory to the location of the ERDC.exe program.</span></span>

3.  <span data-ttu-id="08672-109">С помощью приведенного ниже синтаксиса запустите **Мастер создания образа для восстановления DaRT**.</span><span class="sxs-lookup"><span data-stu-id="08672-109">Using the following syntax, run the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="08672-110">*NumberOfDays* — это положительное целое число, представляющее количество дней, в течение которых будет использоваться изображение для восстановления DART.</span><span class="sxs-lookup"><span data-stu-id="08672-110">*NumberOfDays* is a positive integer that represents the number of days that the DaRT recovery image will be usable.</span></span>

    ``` syntax
    ERDC /e NumberOfDays
    ```

## <span data-ttu-id="08672-111">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="08672-111">Related topics</span></span>


[<span data-ttu-id="08672-112">Создание образа для восстановления DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="08672-112">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





