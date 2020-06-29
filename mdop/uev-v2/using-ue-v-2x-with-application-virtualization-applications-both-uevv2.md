---
title: Использование UE-V 2. x с приложениями Application Virtualization
description: Использование UE-V 2. x с приложениями Application Virtualization
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827272"
---
# <span data-ttu-id="c7f66-103">Использование UE-V 2. x с приложениями Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c7f66-103">Using UE-V 2.x with Application Virtualization Applications</span></span>


<span data-ttu-id="c7f66-104">Виртуализация взаимодействия с пользователем Microsoft (UE-V) 2,0, 2,1 и 2,1 SP1 поддерживает приложения Microsoft Application Virtualization (App-V) без каких-либо необходимых изменений в пакете App-V или UE-V Template.</span><span class="sxs-lookup"><span data-stu-id="c7f66-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 support Microsoft Application Virtualization (App-V) applications without any required modifications to either the App-V package or the UE-V template.</span></span> <span data-ttu-id="c7f66-105">Тем не менее, требуется дополнительный шаг, так как вы не можете запускать генератор UE-V непосредственно в виртуализованном приложении App-V.</span><span class="sxs-lookup"><span data-stu-id="c7f66-105">However, an additional step is required because you cannot run the UE-V Generator directly on a virtualized App-V application.</span></span> <span data-ttu-id="c7f66-106">Вместо этого необходимо установить локальное приложение, создать шаблон, а затем применить шаблон к виртуализированному приложению.</span><span class="sxs-lookup"><span data-stu-id="c7f66-106">Instead, you must install the application locally, generate the template, and then apply the template to the virtualized application.</span></span> <span data-ttu-id="c7f66-107">UE-V поддерживает пакеты App-V 4,5, App-V 4,6 и App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c7f66-107">UE-V supports App-V 4.5, App-V 4.6, and App-V 5.0 packages.</span></span>

## <span data-ttu-id="c7f66-108">Синхронизация параметров UE-V с приложениями App-V</span><span class="sxs-lookup"><span data-stu-id="c7f66-108">UE-V settings synchronization for App-V applications</span></span>


<span data-ttu-id="c7f66-109">UE-V следит за тем, как приложение открывается по имени программы и (необязательно) по номерам и номерам версий, независимо от того, установлено ли приложение локально или виртуально с помощью App-V.</span><span class="sxs-lookup"><span data-stu-id="c7f66-109">UE-V monitors when an application opens by the program name and, optionally, by file version numbers and product version numbers, whether the application is installed locally or virtually by using App-V.</span></span> <span data-ttu-id="c7f66-110">Когда приложение запускается, UE-V отслеживает процесс App-V, применяет все параметры, которые хранятся в пути к хранилищу параметров пользователя, а затем запускает приложение в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="c7f66-110">When the application starts, UE-V monitors the App-V process, applies any settings that are stored in the user's settings storage path, and then enables the application to start normally.</span></span> <span data-ttu-id="c7f66-111">UE-V наблюдает за приложениями App-V и автоматически переводит необходимые пути к файлу и реестру в виртуализированное расположение, а не на физическое место, которое находится за пределами вычислительной среды App-V.</span><span class="sxs-lookup"><span data-stu-id="c7f66-111">UE-V monitors App-V applications and automatically translates the relevant file and registry paths to the virtualized location as opposed to the physical location outside the App-V computing environment.</span></span>

 **<span data-ttu-id="c7f66-112">Реализация синхронизации параметров для виртуализированного приложения</span><span class="sxs-lookup"><span data-stu-id="c7f66-112">To implement settings synchronization for a virtualized application</span></span>**

1.  <span data-ttu-id="c7f66-113">Запустите генератор UE-V для сбора параметров локально установленного приложения, параметры которого нужно синхронизировать между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="c7f66-113">Run the UE-V Generator to collect the settings of the locally installed application whose settings you want to synchronize between computers.</span></span> <span data-ttu-id="c7f66-114">В ходе этого процесса создается шаблон расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="c7f66-114">This process creates a settings location template.</span></span> <span data-ttu-id="c7f66-115">Если вы используете встроенный шаблон, например, шаблон Microsoft Office 2010, пропустите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="c7f66-115">If you use a built-in template such as the Microsoft Office 2010 template, skip this step.</span></span> <span data-ttu-id="c7f66-116">Дополнительные сведения о том, как запустить генератор UE-V, можно найти в разделе [развертывание UE-v 2. x для настраиваемых приложений](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span><span class="sxs-lookup"><span data-stu-id="c7f66-116">For more information about running the UE-V Generator, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span></span>

2.  <span data-ttu-id="c7f66-117">Установите пакет приложения App-V, если вы еще не сделали этого.</span><span class="sxs-lookup"><span data-stu-id="c7f66-117">Install the App-V application package if you have not already done so.</span></span>

3.  <span data-ttu-id="c7f66-118">Опубликуйте шаблон в расположение каталога шаблонов параметров или установите его вручную с помощью `Register-UEVTemplate` командлета Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c7f66-118">Publish the template to the location of your settings template catalog or manually install the template by using the `Register-UEVTemplate` Windows PowerShell cmdlet.</span></span>

    <span data-ttu-id="c7f66-119">**Примечание**  Если вы публикуете созданный шаблон в каталоге шаблонов параметров, клиент не получает шаблон до тех пор, пока поставщик синхронизации не обновит параметры.</span><span class="sxs-lookup"><span data-stu-id="c7f66-119">**Note** If you publish the newly created template to the settings template catalog, the client does not receive the template until the sync provider updates the settings.</span></span> <span data-ttu-id="c7f66-120">Чтобы вручную запустить этот процесс, запустите **планировщик заданий**, разверните **библиотеку планировщика заданий**, разверните **Microsoft**и разверните **UE-V**.</span><span class="sxs-lookup"><span data-stu-id="c7f66-120">To manually start this process, open **Task Scheduler**, expand **Task Scheduler Library**, expand **Microsoft**, and expand **UE-V**.</span></span> <span data-ttu-id="c7f66-121">В области результатов щелкните правой кнопкой мыши **шаблон автоматическое обновление**, а затем выберите команду **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="c7f66-121">In the results pane, right-click **Template Auto Update**, and then click **Run**.</span></span>

     

4.  <span data-ttu-id="c7f66-122">Запустите пакет App-V.</span><span class="sxs-lookup"><span data-stu-id="c7f66-122">Start the App-V package.</span></span>






## <span data-ttu-id="c7f66-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c7f66-123">Related topics</span></span>


[<span data-ttu-id="c7f66-124">Администрирование UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c7f66-124">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





