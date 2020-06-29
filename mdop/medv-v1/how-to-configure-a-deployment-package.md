---
title: Настройка пакета развертывания
description: Настройка пакета развертывания
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825949"
---
# <span data-ttu-id="b1919-103">Настройка пакета развертывания</span><span class="sxs-lookup"><span data-stu-id="b1919-103">How to Configure a Deployment Package</span></span>


<span data-ttu-id="b1919-104">Мастер упаковки поможет вам создать пакет, создав папку на локальном компьютере и передавая все необходимые файлы установки в одну папку.</span><span class="sxs-lookup"><span data-stu-id="b1919-104">The Packaging wizard walks you through the creation of a package by creating a folder on your local computer and transferring all the required installation files to the single folder.</span></span> <span data-ttu-id="b1919-105">Содержимое папки может быть перенесено на несколько съемных носителей для распространения.</span><span class="sxs-lookup"><span data-stu-id="b1919-105">The contents of the folder can then be moved to multiple removable media drives for distribution.</span></span>

**<span data-ttu-id="b1919-106">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b1919-106">Note</span></span>**  
<span data-ttu-id="b1919-107">Один пакет не может содержать файлы установки для систем x86 и x64.</span><span class="sxs-lookup"><span data-stu-id="b1919-107">A single package cannot contain installation files for both x86 and x64 systems.</span></span>



## <span data-ttu-id="b1919-108">Создание пакета развертывания</span><span class="sxs-lookup"><span data-stu-id="b1919-108">How to Create a Deployment Package</span></span>


**<span data-ttu-id="b1919-109">Создание пакета развертывания</span><span class="sxs-lookup"><span data-stu-id="b1919-109">To create a deployment package</span></span>**

1. <span data-ttu-id="b1919-110">Убедитесь в том, что в модуле **Images** создано по крайней мере один локальный упакованный образ.</span><span class="sxs-lookup"><span data-stu-id="b1919-110">Verify in the **Images** module that you have created at least one local packed image.</span></span>

2. <span data-ttu-id="b1919-111">В меню **Сервис** выберите **Мастер упаковки**.</span><span class="sxs-lookup"><span data-stu-id="b1919-111">On the **Tools** menu, select **Packaging wizard**.</span></span>

3. <span data-ttu-id="b1919-112">На странице приветствия **мастера упаковки** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b1919-112">On the **Packaging wizard** welcome page, click **Next**.</span></span>

4. <span data-ttu-id="b1919-113">На странице **изображение рабочей области** установите флажок **включить изображение в пакет** , чтобы включить в него изображение.</span><span class="sxs-lookup"><span data-stu-id="b1919-113">On the **Workspace Image** page, select the **Include image in the package** check box to include an image in the package.</span></span>

   <span data-ttu-id="b1919-114">Поле **изображения** включено.</span><span class="sxs-lookup"><span data-stu-id="b1919-114">The **Image** field is enabled.</span></span>

   **<span data-ttu-id="b1919-115">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b1919-115">Note</span></span>**  
   <span data-ttu-id="b1919-116">В пакете MED-V изображение не требуется. пакет можно создать без изображения.</span><span class="sxs-lookup"><span data-stu-id="b1919-116">An image is not required in a MED-V package; the package can be created without an image.</span></span> <span data-ttu-id="b1919-117">В таком случае изображение должно быть загружено на сервер, чтобы позднее его можно было загрузить по сети на клиент или отправить в папку, предваряя изображение.</span><span class="sxs-lookup"><span data-stu-id="b1919-117">In such a case, the image should be uploaded to the server so that it can later be downloaded over the network to the client, or pushed to an image pre-stage folder.</span></span>



5. <span data-ttu-id="b1919-118">Щелкните список **изображений** , чтобы просмотреть все доступные изображения.</span><span class="sxs-lookup"><span data-stu-id="b1919-118">Click the **Image** list to view all available images.</span></span> <span data-ttu-id="b1919-119">Выберите изображение, которое нужно скопировать в пакет.</span><span class="sxs-lookup"><span data-stu-id="b1919-119">Select the image to be copied to the package.</span></span> <span data-ttu-id="b1919-120">Нажмите кнопку **Обновить** , чтобы обновить список доступных изображений.</span><span class="sxs-lookup"><span data-stu-id="b1919-120">Click **Refresh** to refresh the list of available images.</span></span>

6. <span data-ttu-id="b1919-121">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b1919-121">Click **Next**.</span></span>

7. <span data-ttu-id="b1919-122">На странице **Параметры установки для MED-v** выберите установочный файл med-v, выполнив одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="b1919-122">On the **MED-V Installation Settings** page, select the MED-V installation file by doing one of the following:</span></span>

   -   <span data-ttu-id="b1919-123">В поле **установочный файл MED-V** введите полный путь к каталогу, в котором находится установочный файл.</span><span class="sxs-lookup"><span data-stu-id="b1919-123">In the **MED-V installation file** field, type the full path to the directory where the installation file is located.</span></span>

   -   <span data-ttu-id="b1919-124">Нажмите кнопку **...** , чтобы перейти к каталогу, в котором находится файл установки.</span><span class="sxs-lookup"><span data-stu-id="b1919-124">Click **...** to browse to the directory where the installation file is located.</span></span>

   **<span data-ttu-id="b1919-125">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b1919-125">Note</span></span>**  
   <span data-ttu-id="b1919-126">Это поле является обязательным, и мастер не продолжит работу без правильного имени файла.</span><span class="sxs-lookup"><span data-stu-id="b1919-126">This field is mandatory, and the wizard will not continue without a valid file name.</span></span>



8. <span data-ttu-id="b1919-127">В поле **Server Address (адрес сервера** ) введите имя сервера или IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="b1919-127">In the **Server address** field, type the server name or IP address.</span></span>

9. <span data-ttu-id="b1919-128">В поле **порт сервера** введите порт сервера.</span><span class="sxs-lookup"><span data-stu-id="b1919-128">In the **Server port** field, type the server port.</span></span>

10. <span data-ttu-id="b1919-129">Установите флажок **доступ к серверу по протоколу HTTPS используется** для подключения к серверу по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b1919-129">Select the **Server is accessed using https** check box to require an https connection to connect to the server.</span></span>

11. <span data-ttu-id="b1919-130">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="b1919-130">Do one of the following:</span></span>

    -   <span data-ttu-id="b1919-131">Щелкните **Параметры установки по умолчанию**, а затем нажмите кнопку **Далее** , чтобы продолжить, а затем оставьте параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1919-131">Click **Default installation settings**, and then click **Next** to continue and leave the default settings.</span></span>

    -   <span data-ttu-id="b1919-132">Выберите **Параметры выборочной установки**и нажмите кнопку **Далее** , чтобы настроить параметры установки.</span><span class="sxs-lookup"><span data-stu-id="b1919-132">Click **Custom installation settings**, and then click **Next** to customize the installation settings.</span></span>

        1.  <span data-ttu-id="b1919-133">На странице **пользовательские параметры установки для MED-V** в поле **Папка установки** введите путь к папке, в которой будут установлены файлы med-v на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="b1919-133">On the **MED-V Installation Custom Settings** page, in the **Installation folder** field, type the path of the folder where the MED-V files will be installed on the host computer.</span></span>

            **<span data-ttu-id="b1919-134">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b1919-134">Note</span></span>**  
            <span data-ttu-id="b1919-135">Рекомендуется использовать переменные в пути, а не константы, которые могут быть различными для разных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="b1919-135">It is recommended to use variables in the path rather than constants, which might vary from computer to computer.</span></span>

            <span data-ttu-id="b1919-136">Например, используйте *%ProgramFiles%\\MED-V* вместо *c:\\MED-V*.</span><span class="sxs-lookup"><span data-stu-id="b1919-136">For example, use *%ProgramFiles%\\MED-V* instead of *c:\\MED-V*.</span></span>



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. <span data-ttu-id="b1919-137">На странице " **Дополнительные установки** " установите флажок **включить программное обеспечение для виртуализации** , чтобы включить в пакет установку Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="b1919-137">On the **Additional Installations** page, select the **Include installation of virtualization software** check box to include the Virtual PC installation in the package.</span></span>

    <span data-ttu-id="b1919-138">Поле " **файл установки** " включено.</span><span class="sxs-lookup"><span data-stu-id="b1919-138">The **Installation file** field is enabled.</span></span> <span data-ttu-id="b1919-139">Введите полный путь к файлу установки программного обеспечения для виртуализации или нажмите кнопку **...** , чтобы перейти к каталогу.</span><span class="sxs-lookup"><span data-stu-id="b1919-139">Type the full path of the virtualization software installation file, or click **...** to browse to the directory.</span></span>

13. <span data-ttu-id="b1919-140">Установите флажок **включить установку Virtual PC QFE** , чтобы включить в пакет установку обновления Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="b1919-140">Select the **Include installation of Virtual PC QFE** check box to include Virtual PC update installation in the package.</span></span>

    <span data-ttu-id="b1919-141">Поле " **файл установки** " включено.</span><span class="sxs-lookup"><span data-stu-id="b1919-141">The **Installation file** field is enabled.</span></span> <span data-ttu-id="b1919-142">Введите полный путь установочного файла виртуального компьютера или нажмите кнопку **...** , чтобы перейти к каталогу.</span><span class="sxs-lookup"><span data-stu-id="b1919-142">Type the full path of the Virtual PC update installation file, or click **...** to browse to the directory.</span></span>

14. <span data-ttu-id="b1919-143">Установите флажок **включить установку Microsoft .NET framework 2,0** , чтобы включить в пакет установку Microsoft .net Framework 2,0.</span><span class="sxs-lookup"><span data-stu-id="b1919-143">Select the **Include installation of Microsoft .NET Framework 2.0** check box to include the Microsoft .NET Framework 2.0 installation in the package.</span></span>

    <span data-ttu-id="b1919-144">Поле " **файл установки** " включено.</span><span class="sxs-lookup"><span data-stu-id="b1919-144">The **Installation file** field is enabled.</span></span> <span data-ttu-id="b1919-145">Введите полный путь установочного файла Microsoft .NET Framework 2,0 или нажмите **...** , чтобы перейти к каталогу.</span><span class="sxs-lookup"><span data-stu-id="b1919-145">Type the full path of the Microsoft .NET Framework 2.0 installation file, or click **...** to browse to the directory.</span></span>

15. <span data-ttu-id="b1919-146">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b1919-146">Click **Next**.</span></span>

16. <span data-ttu-id="b1919-147">На странице **финализировать** выберите расположение, в котором нужно сохранить пакет, выполнив одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="b1919-147">On the **Finalize** page, select the location where the package should be saved by doing one of the following:</span></span>

    -   <span data-ttu-id="b1919-148">В поле **Destination (назначение пакета** ) введите полный путь к каталогу, в котором нужно сохранить пакет.</span><span class="sxs-lookup"><span data-stu-id="b1919-148">In the **Package destination** field, type the full path to the directory where the package should be saved.</span></span>

    -   <span data-ttu-id="b1919-149">Нажмите кнопку **...** , чтобы перейти к каталогу, в котором нужно сохранить файлы установки.</span><span class="sxs-lookup"><span data-stu-id="b1919-149">Click **...** to browse to the directory where the installation files should be saved.</span></span>

    **<span data-ttu-id="b1919-150">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b1919-150">Note</span></span>**  
    <span data-ttu-id="b1919-151">Создание пакета может занять больше места, чем фактический размер пакета.</span><span class="sxs-lookup"><span data-stu-id="b1919-151">Building the package might consume more space than the actual package size.</span></span> <span data-ttu-id="b1919-152">Поэтому рекомендуется создать пакет на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="b1919-152">It is therefore recommended to build the package on the hard drive.</span></span> <span data-ttu-id="b1919-153">После создания пакета его можно будет скопировать на USB-порт.</span><span class="sxs-lookup"><span data-stu-id="b1919-153">After the package is created, it can then be copied to the USB.</span></span>



17. <span data-ttu-id="b1919-154">В поле **имя пакета** введите имя пакета.</span><span class="sxs-lookup"><span data-stu-id="b1919-154">In the **Package name** field, enter a name for the package.</span></span>

18. <span data-ttu-id="b1919-155">Нажмите кнопку **Готово** , чтобы создать пакет.</span><span class="sxs-lookup"><span data-stu-id="b1919-155">Click **Finish** to create the package.</span></span>

    <span data-ttu-id="b1919-156">Пакет создан.</span><span class="sxs-lookup"><span data-stu-id="b1919-156">The package is created.</span></span> <span data-ttu-id="b1919-157">Это может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="b1919-157">This might take several minutes.</span></span>

    <span data-ttu-id="b1919-158">После создания пакета появится сообщение о том, что оно было успешно завершено.</span><span class="sxs-lookup"><span data-stu-id="b1919-158">After the package is created, a message appears notifying you that it has been completed successfully.</span></span>

**<span data-ttu-id="b1919-159">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b1919-159">Note</span></span>**  
<span data-ttu-id="b1919-160">Если вы сохранили все файлы локально, а не непосредственно на съемном носителе, убедитесь, что вы копируете только содержимое папки, а не саму папку на съемный носитель.</span><span class="sxs-lookup"><span data-stu-id="b1919-160">If you saved all the files locally, and not directly on the removable media, ensure that you copy only the contents of the folder and not the folder itself to the removable media.</span></span>



**<span data-ttu-id="b1919-161">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b1919-161">Note</span></span>**  
<span data-ttu-id="b1919-162">Съемные носители должны быть достаточно большими, чтобы содержимое пакета затратило не более трех кварталов из памяти съемных носителей.</span><span class="sxs-lookup"><span data-stu-id="b1919-162">The removable media must be large enough so that the package contents consume a maximum of only three-quarters of the removable media's memory.</span></span>



**<span data-ttu-id="b1919-163">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b1919-163">Note</span></span>**  
<span data-ttu-id="b1919-164">При создании пакета при завершении сборки может потребоваться до двойного размера файла фактического размера пакета.</span><span class="sxs-lookup"><span data-stu-id="b1919-164">When creating the package, up to double the size of the actual package size might be required when the build is complete.</span></span>



## <span data-ttu-id="b1919-165">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b1919-165">Related topics</span></span>


[<span data-ttu-id="b1919-166">Создание образа MED-V</span><span class="sxs-lookup"><span data-stu-id="b1919-166">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)









