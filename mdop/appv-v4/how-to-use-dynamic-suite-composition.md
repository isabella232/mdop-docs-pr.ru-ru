---
title: Использование функции формирования динамических пакетов
description: Использование функции формирования динамических пакетов
author: dansimp
ms.assetid: 24147feb-a0a8-4791-a8e5-cbe5fe13c762
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bff4c9721352785cf6db5c497234ceaa3c5e448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816419"
---
# <span data-ttu-id="7b8ae-103">Использование функции формирования динамических пакетов</span><span class="sxs-lookup"><span data-stu-id="7b8ae-103">How To Use Dynamic Suite Composition</span></span>


<span data-ttu-id="7b8ae-104">Композиция динамических наборов в Application Virtualization позволяет определять приложение как зависящее от другого приложения, например по промежуточному по или с помощью плагина.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-104">Dynamic Suite Composition in Application Virtualization enables you to define an application as being dependent on another application, such as middleware or a plug-in.</span></span> <span data-ttu-id="7b8ae-105">Это позволяет приложению взаимодействовать с промежуточным по или плагином в виртуальной среде, где обычно это запрещено.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-105">This enables the application to interact with the middleware or plug-in in the virtual environment, where typically this is prevented.</span></span> <span data-ttu-id="7b8ae-106">Это полезно, так как дополнительный пакет приложения можно использовать с несколькими другими приложениями, которые называются *основными приложениями*, что позволяет каждому основному приложению ссылаться на один и тот же дополнительный пакет.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-106">This is useful because a secondary application package can be used with several other applications, referred to as the *primary applications*, which enables each primary application to reference the same secondary package.</span></span>

<span data-ttu-id="7b8ae-107">Вы можете использовать композицию динамического набора при последовательной последовательности приложений, зависящих от подключаемых модулей, таких как элементы ActiveX, или для приложений, которые зависят от этого по (например, OLE DB или среды выполнения Java (JRE).</span><span class="sxs-lookup"><span data-stu-id="7b8ae-107">You can use Dynamic Suite Composition when you sequence applications that depend on plug-ins such as ActiveX controls or for applications that depend on middleware such as OLE DB or the Java Runtime Environment (JRE).</span></span> <span data-ttu-id="7b8ae-108">Если каждому приложению, использующему эти зависимые компоненты, требуется виртуализация, в том числе компоненты, для обновления этих компонентов потребуется повторная последовательность всех основных приложений.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-108">If each application that used these dependent components required sequencing, including the components, updates to those components would require re-sequencing all the primary applications.</span></span> <span data-ttu-id="7b8ae-109">Если вы выполняете последовательность основных приложений без компонентов, а затем поочередно полагатье промежуточный план или плагин в качестве дополнительного пакета, необходимо обновить только дополнительный пакет.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-109">If you sequence the primary applications without the components and then sequence the middleware or plug-in as a secondary package, then only the secondary package must be updated.</span></span>

<span data-ttu-id="7b8ae-110">Одним из преимуществ такого подхода является снижение размера основных пакетов.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-110">One advantage of this approach is that it reduces the size of the primary packages.</span></span> <span data-ttu-id="7b8ae-111">Другое преимущество заключается в том, что он обеспечивает более эффективное управление разрешениями на доступ к дополнительным приложениям.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-111">Another advantage is that it provides you with better control of access permissions on the secondary applications.</span></span> <span data-ttu-id="7b8ae-112">Обратите внимание, что дополнительное приложение может быть помещено в поток обычным образом и не должно быть полностью кэшировано для выполнения.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-112">Note that the secondary application can be streamed in the regular way and does not have to be fully cached to run.</span></span>

<span data-ttu-id="7b8ae-113">У основного пакета может быть несколько вспомогательных пакетов.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-113">A primary package can have more than one secondary package.</span></span> <span data-ttu-id="7b8ae-114">Однако поддерживается только один уровень зависимостей, поэтому вы не можете определить дополнительный пакет, как зависимый от другого вспомогательного пакета.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-114">However, only one level of dependency is supported, so you cannot define a secondary package as dependent on another secondary package.</span></span> <span data-ttu-id="7b8ae-115">Кроме того, дополнительное приложение может быть только вспомогательным по по уровням или плагином и не может быть другим полноценным продуктом программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-115">Also the secondary application can only be middleware or a plug-in and cannot be another full software product.</span></span>

<span data-ttu-id="7b8ae-116">Если вы планируете сделать несколько основных приложений зависимыми от одного промежуточного продукта, убедитесь, что вы протестируете эту конфигурацию, чтобы определить потенциальный эффект для производительности системы перед его развертыванием.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-116">If you plan to make several primary applications dependent on a single middleware product, make sure that you test this configuration to determine the potential effect on system performance before you deploy it.</span></span>

<span data-ttu-id="7b8ae-117">**Важно!**  Зависимости пакетов можно задать в качестве обязательных для основного приложения.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-117">**Important** Package dependencies can be specified as mandatory for a primary application.</span></span> <span data-ttu-id="7b8ae-118">Если дополнительный пакет помечен как обязательный и недоступен по какой-либо причине при загрузке, загрузка дополнительного пакета завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-118">If a secondary package is flagged as mandatory and it cannot be accessed for some reason during loading, the load of the secondary package will fail.</span></span> <span data-ttu-id="7b8ae-119">Кроме того, если пользователь попытается запустить его, происходит сбой основного приложения.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-119">Also, the primary application will fail when the user tries to start it.</span></span>

 

<span data-ttu-id="7b8ae-120">С помощью описанных ниже процедур вы можете создать дополнительный пакет для плагина или компонента по промежуточного по, а затем с помощью финальной процедуры можно определить зависимость в OSD-файле дополнительного пакета.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-120">You can use the following procedures to create a secondary package, for either a plug-in or a middleware component, and then you can use the final procedure to define the dependency in the OSD file of the secondary package.</span></span>

**<span data-ttu-id="7b8ae-121">Создание дополнительного пакета для надстройки с помощью композиции динамического набора</span><span class="sxs-lookup"><span data-stu-id="7b8ae-121">To create a secondary package for a plug-in by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="7b8ae-122">На компьютере, на котором установлен образ с чистым изображением, установите Application Virtualization Sequencer и сохраните состояние компьютера.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-122">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="7b8ae-123">Поочередное применение основного приложения и сохранение пакета в папке содержимого на сервере.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-123">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

3.  <span data-ttu-id="7b8ae-124">Восстановите состояние компьютера, на котором установлен виртуализация, в действии 1.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-124">Restore the sequencing computer to its saved state from step 1.</span></span>

4.  <span data-ttu-id="7b8ae-125">Установка и Настройка основного приложения локально на компьютере, на котором установлен виртуализация.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-125">Install and configure the primary application locally on the sequencing computer.</span></span>

    <span data-ttu-id="7b8ae-126">**Важно!**  Необходимо указать новый корневой каталог пакета для вторичного пакета.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-126">**Important** You must specify a new package root for the secondary package.</span></span>

     

5.  <span data-ttu-id="7b8ae-127">Запустите этап мониторинга Sequencer.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-127">Start the sequencer monitoring phase.</span></span>

6.  <span data-ttu-id="7b8ae-128">Установите плагин на компьютере виртуализации и настройте его нужным образом.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-128">Install the plug-in on the sequencing computer and configure it as needed.</span></span>

7.  <span data-ttu-id="7b8ae-129">Откройте основное приложение и убедитесь, что плагин работает правильно.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-129">Open the primary application, and confirm that the plug-in is working correctly.</span></span>

8.  <span data-ttu-id="7b8ae-130">На консоли Sequencer создайте фиктивное приложение, представляющее дополнительный пакет, который будет содержать плагин, и щелкните значок.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-130">In the sequencer console, create a dummy application to represent the secondary package that will contain the plug-in and select an icon.</span></span>

9.  <span data-ttu-id="7b8ae-131">Сохраните пакет в папке содержимого на сервере.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-131">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="7b8ae-132">**Примечание**  Для упрощения управления вспомогательными пакетами рекомендуется, чтобы имя пакета включало термин "дополнительный пакет", чтобы подчеркнуть, что это пакет, который не будет работать как автономное приложение (например, **\ [имя подсистемы]] дополнительный пакет**).</span><span class="sxs-lookup"><span data-stu-id="7b8ae-132">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Plug In Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="7b8ae-133">Создание дополнительного пакета для промежуточного слоя с помощью композиции динамического набора</span><span class="sxs-lookup"><span data-stu-id="7b8ae-133">To create a secondary package for middleware by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="7b8ae-134">На компьютере, на котором установлен образ с чистым изображением, установите Application Virtualization Sequencer и сохраните состояние компьютера.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-134">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="7b8ae-135">Установка промежуточного слоя локально на компьютере виртуализации и его настройка.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-135">Install the middleware locally on the sequencing computer, and configure it.</span></span>

3.  <span data-ttu-id="7b8ae-136">Поочередное применение основного приложения и сохранение пакета в папке содержимого на сервере.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-136">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

4.  <span data-ttu-id="7b8ae-137">Восстановите состояние компьютера, на котором установлен виртуализация, в действии 1.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-137">Restore the sequencing computer to its saved state from step 1.</span></span>

5.  <span data-ttu-id="7b8ae-138">Запустите секвенсор, чтобы создать новый пакет.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-138">Start the sequencer to create a new package.</span></span>

6.  <span data-ttu-id="7b8ae-139">Запустите этап мониторинга Sequencer.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-139">Start the sequencer monitoring phase.</span></span>

7.  <span data-ttu-id="7b8ae-140">Установите приложение промежуточного слоя на компьютере виртуализации и настройте его как обычную установку.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-140">Install the middleware application on the sequencing computer, and configure it as in a typical installation.</span></span>

8.  <span data-ttu-id="7b8ae-141">Завершите процесс упорядочивания.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-141">Complete the sequencing process.</span></span>

9.  <span data-ttu-id="7b8ae-142">Сохраните пакет в папке содержимого на сервере.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-142">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="7b8ae-143">**Примечание**  Для упрощения управления вспомогательными пакетами рекомендуется, чтобы имя пакета включало термин "дополнительный пакет", чтобы подчеркнуть, что это пакет, который не будет работать как автономное приложение (например, **\ [название промежуточного по]] дополнительный пакет**.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-143">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Middleware Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="7b8ae-144">Определение зависимости в основном пакете</span><span class="sxs-lookup"><span data-stu-id="7b8ae-144">To define the dependency in the primary package</span></span>**

1. <span data-ttu-id="7b8ae-145">На сервере откройте OSD файл дополнительного пакета для редактирования.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-145">On the server, open the OSD file of the secondary package for editing.</span></span> <span data-ttu-id="7b8ae-146">(Рекомендуется использовать редактор XML для внесения изменений в файл OSD, но в качестве альтернативы можно использовать Блокнот).</span><span class="sxs-lookup"><span data-stu-id="7b8ae-146">(It is a good idea to use an XML editor to make changes to the OSD file; however, you can use Notepad as an alternative.)</span></span>

2. <span data-ttu-id="7b8ae-147">Скопируйте строку **href** из этого файла.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-147">Copy the **CODEBASE HREF** line from that file.</span></span>

3. <span data-ttu-id="7b8ae-148">Откройте OSD файл основного пакета для редактирования.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-148">Open the OSD file of the primary package for editing.</span></span>

4. <span data-ttu-id="7b8ae-149">Вставьте <strong> &lt; тег Dependencies &gt; </strong> после закрывающего тега \*\* &lt; /ENVLIST &gt; \*\* в конце раздела \*\* &lt; VIRTUALENV &gt; \*\* прямо перед тегом \*\* &lt; /VIRTUALENV &gt; \*\* .</span><span class="sxs-lookup"><span data-stu-id="7b8ae-149">Insert the <strong>&lt;DEPENDENCIES&gt;</strong>tag after the close of **&lt;/ENVLIST&gt;** tag at the end of the **&lt;VIRTUALENV&gt;** section just before the **&lt;/VIRTUALENV&gt;** tag.</span></span>

5. <span data-ttu-id="7b8ae-150">Вставьте строку **href в базу кода** из дополнительного пакета после только что созданного тега \*\* &lt; зависимостей &gt; \*\* .</span><span class="sxs-lookup"><span data-stu-id="7b8ae-150">Paste the **CODEBASE HREF** line from the secondary package after the **&lt;DEPENDENCIES&gt;** tag you just created.</span></span>

6. <span data-ttu-id="7b8ae-151">Если дополнительный пакет является обязательным, это означает, что он должен быть запущен до начала основного пакета, добавьте в тег **CodeBase** свойство **обязательно = "true"** .</span><span class="sxs-lookup"><span data-stu-id="7b8ae-151">If the secondary package is a mandatory package, which means that it must be started before the primary package is started, add the **MANDATORY=”TRUE”** property inside the **CODEBASE** tag.</span></span> <span data-ttu-id="7b8ae-152">Если это свойство не является обязательным, его можно опустить.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-152">If it is not mandatory, the property can be omitted.</span></span>

7. <span data-ttu-id="7b8ae-153">Закройте тег \*\* &lt; зависимостей &gt; \*\* , вставив указанные ниже сведения.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-153">Close the **&lt;DEPENDENCIES&gt;** tag by inserting the following:</span></span>

   **<span data-ttu-id="7b8ae-154">&lt;/DEPENDENCIES&gt;</span><span class="sxs-lookup"><span data-stu-id="7b8ae-154">&lt;/DEPENDENCIES&gt;</span></span>**

8. <span data-ttu-id="7b8ae-155">Просмотрите изменения, внесенные в OSD файл, а затем сохраните и закройте файл.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-155">Review the changes that you made to the OSD file, and then save and close the file.</span></span> <span data-ttu-id="7b8ae-156">В следующем примере показано, как должен выглядеть добавленный раздел.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-156">The following example shows how the added section should appear.</span></span> <span data-ttu-id="7b8ae-157">Указанные здесь значения тега предназначены только для примера.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-157">The tag values shown here are for example only.</span></span>

   **<span data-ttu-id="7b8ae-158">&lt;VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="7b8ae-158">&lt;VIRTUALENV&gt;</span></span>**

        **&lt;ENVLIST&gt;**

   **<span data-ttu-id="7b8ae-159">…</span><span class="sxs-lookup"><span data-stu-id="7b8ae-159">…</span></span>**

        **&lt;/ENVLIST&gt;**

        **&lt;DEPENDENCIES&gt;**

             **&lt;CODEBASE HREF="rtsp://virt\_apps/package.1/package.1.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.1\\osguard.cp"/&gt;**

             **&lt;CODEBASE HREF="rtsp://sample\_apps/package.2/sample.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.2\\osguard.cp" MANDATORY="TRUE" /&gt;**

        **&lt;/DEPENDENCIES&gt;**

   **<span data-ttu-id="7b8ae-160">&lt;/VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="7b8ae-160">&lt;/VIRTUALENV&gt;</span></span>**

9. <span data-ttu-id="7b8ae-161">Если дополнительный пакет содержит какие – либо записи в разделе \*\* &lt; ENVLIST &gt; \*\* файла OSD, необходимо скопировать эти записи в тот же раздел основного пакета.</span><span class="sxs-lookup"><span data-stu-id="7b8ae-161">If the secondary package has any entries in the **&lt;ENVLIST&gt;** section of the OSD file, you must copy those entries to the same section in the primary package.</span></span>

## <span data-ttu-id="7b8ae-162">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7b8ae-162">Related topics</span></span>


[<span data-ttu-id="7b8ae-163">Создание и обновление виртуальных приложений с помощью секвенсора App-V</span><span class="sxs-lookup"><span data-stu-id="7b8ae-163">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





