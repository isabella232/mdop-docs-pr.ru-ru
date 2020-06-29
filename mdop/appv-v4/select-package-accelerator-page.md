---
title: Страница "Выберите ускоритель пакетов"
description: Страница "Выберите ускоритель пакетов"
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815592"
---
# <span data-ttu-id="b3127-103">Страница "Выберите ускоритель пакетов"</span><span class="sxs-lookup"><span data-stu-id="b3127-103">Select Package Accelerator Page</span></span>


<span data-ttu-id="b3127-104">Выберите ускоритель пакетов, который будет использоваться для создания нового виртуального пакета приложений, с помощью страницы **Выбор ускорителя пакетов** .</span><span class="sxs-lookup"><span data-stu-id="b3127-104">Use the **Select Package Accelerator** page to select the Package Accelerator that will be used to create the new virtual application package.</span></span> <span data-ttu-id="b3127-105">Вы должны скопировать ускоритель пакетов в папку на компьютере с секвенсором App-V.</span><span class="sxs-lookup"><span data-stu-id="b3127-105">You must copy the Package Accelerator to a folder on the computer running the App-V Sequencer.</span></span> <span data-ttu-id="b3127-106">Дополнительные сведения можно найти в разделе [акселераторы пакетов App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="b3127-106">For more information, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="b3127-107">Запускать ускорители пакетов только от издателей, которым вы доверяете.</span><span class="sxs-lookup"><span data-stu-id="b3127-107">Only run Package Accelerators from publishers that you trust.</span></span> <span data-ttu-id="b3127-108">Ускорители пакетов обычно включают цифровую подпись.</span><span class="sxs-lookup"><span data-stu-id="b3127-108">Package Accelerators usually include a digital signature.</span></span> <span data-ttu-id="b3127-109">Цифровая подпись — это электронный отметка безопасности, с помощью которой можно обозначить издателя программного обеспечения и узнать, был ли пакет изменен после того, как преобразование было подписано.</span><span class="sxs-lookup"><span data-stu-id="b3127-109">A digital signature is an electronic security mark that can help indicate the publisher of the software, and whether the package has been tampered with after the transform was originally signed.</span></span> <span data-ttu-id="b3127-110">Если вы используете для преобразования цифровую подпись, подписанную издателем, а издатель проверил ее личность с помощью центра сертификации, вы можете быть уверены в том, что преобразование поступает от определенного издателя и не было изменено.</span><span class="sxs-lookup"><span data-stu-id="b3127-110">If you use a transform that has been digitally signed by a publisher and the publisher has verified its identity with a certification authority, you can be more confident that the transform comes from that specific publisher and has not been altered.</span></span>

<span data-ttu-id="b3127-111">Секвенсор App-V уведомляет вас, если выполняется любое из указанных ниже условий.</span><span class="sxs-lookup"><span data-stu-id="b3127-111">The App-V Sequencer notifies you if any of the following conditions are true:</span></span>

-   <span data-ttu-id="b3127-112">Выбранное преобразование не было подписано цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="b3127-112">The selected transform has not been digitally signed.</span></span>

-   <span data-ttu-id="b3127-113">Выбранное преобразование подписано издателем, который не прошел проверку подлинности с центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="b3127-113">The selected transform is signed by a publisher that has not verified its identity with a certification authority.</span></span>

-   <span data-ttu-id="b3127-114">Выбранное преобразование было изменено после того, как оно сопоставлено цифровой подписью и выпущено.</span><span class="sxs-lookup"><span data-stu-id="b3127-114">The selected transform has been altered after it was digitally signed and released.</span></span>

<span data-ttu-id="b3127-115">Если какие-либо из этих сообщений отображаются при использовании ускорителей пакетов, посетите веб-сайт ускорителя пакетов издателя, чтобы получить версию преобразования с цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="b3127-115">If any of these messages are displayed when using a Package Accelerators, visit the Package Accelerators publisher’s website to get a digitally signed version of the transform.</span></span>

<span data-ttu-id="b3127-116">Эта страница включает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="b3127-116">This page contains the following elements:</span></span>

<a href="" id="browse"></a>**<span data-ttu-id="b3127-117">Обзор</span><span class="sxs-lookup"><span data-stu-id="b3127-117">Browse</span></span>**  
<span data-ttu-id="b3127-118">Нажмите кнопку **Обзор** , чтобы указать ускоритель пакетов, который будет использоваться для создания виртуального пакета приложений.</span><span class="sxs-lookup"><span data-stu-id="b3127-118">Click **Browse** to specify the Package Accelerator that you will use to create the virtual application package.</span></span> <span data-ttu-id="b3127-119">Сохраните пакетный ускоритель, указанный на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="b3127-119">Save the Package Accelerator you specified locally on the computer that is running the Sequencer.</span></span>

## <span data-ttu-id="b3127-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b3127-120">Related topics</span></span>


[<span data-ttu-id="b3127-121">Мастер виртуализации— ускоритель пакетов (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="b3127-121">Sequencer Wizard - Package Accelerator (AppV 4.6 SP1)</span></span>](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





