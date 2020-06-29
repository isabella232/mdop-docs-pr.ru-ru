---
title: Список исключений приложения Windows Virtual PC
description: Список исключений приложения Windows Virtual PC
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823692"
---
# <span data-ttu-id="1382c-103">Список исключений приложения Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1382c-103">Windows Virtual PC Application Exclude List</span></span>


<span data-ttu-id="1382c-104">В некоторых случаях вы не хотите, чтобы приложения, установленные в рабочей области MED-V, были опубликованы в **главном меню главного** компьютера.</span><span class="sxs-lookup"><span data-stu-id="1382c-104">In some instances, you might not want applications that are installed in the MED-V workspace to be published to the host computer **Start** menu.</span></span> <span data-ttu-id="1382c-105">Чтобы отменить публикацию этих приложений, следуйте инструкциям, приведенным в разделе [Публикация и Отмена публикации приложения в рабочей области MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="1382c-105">You can unpublish these applications by following the instructions at [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span> <span data-ttu-id="1382c-106">Тем не менее, если программа автоматически обновляется, она также может быть автоматически повторно опубликована.</span><span class="sxs-lookup"><span data-stu-id="1382c-106">However, if the program ever automatically updates, it might also be automatically republished.</span></span> <span data-ttu-id="1382c-107">Это приведет к тому, что вам потребуется повторно опубликовать приложение.</span><span class="sxs-lookup"><span data-stu-id="1382c-107">This causes you to have to unpublish the application again.</span></span>

<span data-ttu-id="1382c-108">В Windows Virtual PC есть функция, известная как "список исключений", позволяющая указывать некоторые установленные приложения, которые не нужно публиковать в **главном меню.**</span><span class="sxs-lookup"><span data-stu-id="1382c-108">Windows Virtual PC includes a feature known as the "Exclude List" that lets you specify certain installed applications that you do not want published to the host **Start** menu.</span></span> <span data-ttu-id="1382c-109">"Список исключений" находится в гостевом реестре в разделе HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList и перечисляет приложения, которые не опубликованы в **главном меню главного** приложения.</span><span class="sxs-lookup"><span data-stu-id="1382c-109">The "Exclude List" is located in the guest registry in the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList key and lists those applications that are not published to the host **Start** menu.</span></span> <span data-ttu-id="1382c-110">Вы можете представить "список исключений", чтобы окончательно отменить публикацию указанных приложений, так как в этом случае автоматические обновления приложений не будут автоматически публиковаться.</span><span class="sxs-lookup"><span data-stu-id="1382c-110">You can think of the “Exclude List” as permanently unpublishing the specified applications because any automatic updates to the applications that are listed will not cause them to be automatically republished.</span></span>

## <span data-ttu-id="1382c-111">Управление приложениями с помощью списка исключений в Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1382c-111">Managing Applications by Using the Exclude List in Windows Virtual PC</span></span>


****

1.  <span data-ttu-id="1382c-112">Откройте рабочую область MED-V в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="1382c-112">Open the MED-V workspace in full screen.</span></span>

    <span data-ttu-id="1382c-113">Сведения о том, как открыть рабочую область MED-V в полноэкранном режиме с помощью средства администрирования MED-V, приведены в разделе [Просмотр конфигураций рабочих областей med-v](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span><span class="sxs-lookup"><span data-stu-id="1382c-113">For information about opening the MED-V workspace in full-screen mode by using the MED-V Administration Toolkit, see [Viewing MED-V Workspace Configurations](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span></span> <span data-ttu-id="1382c-114">Кроме того, вы можете вручную открыть его в полноэкранном режиме, нажав кнопку **Пуск**, выберите **все программы**, а затем — **виртуальный компьютер Windows**, выберите **Windows Virtual PC**и дважды щелкните рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="1382c-114">Or you can manually open it in full screen by clicking **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, and then double-click the MED-V workspace.</span></span>

2.  <span data-ttu-id="1382c-115">В окне Virtual PC рабочей области для Windows для MED-V откройте редактор реестра.</span><span class="sxs-lookup"><span data-stu-id="1382c-115">In the MED-V workspace Windows Virtual PC window, open Registry Editor.</span></span>

    <span data-ttu-id="1382c-116">Нажмите кнопку **Пуск**, выберите команду **выполнить**и введите regedit.</span><span class="sxs-lookup"><span data-stu-id="1382c-116">Click **Start**, click **Run**, and then type regedit.</span></span> <span data-ttu-id="1382c-117">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1382c-117">Then click **OK**.</span></span>

3.  <span data-ttu-id="1382c-118">В редакторе реестра найдите раздел реестра HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList.</span><span class="sxs-lookup"><span data-stu-id="1382c-118">In Registry Editor, locate the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList registry key.</span></span>

4.  <span data-ttu-id="1382c-119">Создайте новое значение реестра для установленного приложения, которое вы не хотите публиковать в меню " **Пуск** " главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="1382c-119">Create a new registry value for the installed application that you do not want published to the host computer **Start** menu.</span></span> <span data-ttu-id="1382c-120">Например, если вы хотите отменить публикацию автоматически опубликованной программы Microsoft Silverlight, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1382c-120">For example, if you want to unpublish the automatically published program Microsoft Silverlight, follow these steps:</span></span>

    1.  <span data-ttu-id="1382c-121">Выделив раздел реестра VPCVAppExcludeList, выберите команду **изменить**, а затем — команду **создать**, а затем — **строковое значение**.</span><span class="sxs-lookup"><span data-stu-id="1382c-121">With the VPCVAppExcludeList registry key highlighted, click **Edit**, click **New**, and then click **String Value**.</span></span>

    2.  <span data-ttu-id="1382c-122">Введите имя нового значения реестра.</span><span class="sxs-lookup"><span data-stu-id="1382c-122">Enter the name for the new registry value.</span></span> <span data-ttu-id="1382c-123">Например, для Microsoft Silverlight вы можете ввести sllauncher.exe.</span><span class="sxs-lookup"><span data-stu-id="1382c-123">For example, for Microsoft Silverlight, you might enter sllauncher.exe.</span></span>

    3.  <span data-ttu-id="1382c-124">Дважды щелкните новый параметр реестра и введите значение данных.</span><span class="sxs-lookup"><span data-stu-id="1382c-124">Double-click the new registry value and enter the value data.</span></span>

        <span data-ttu-id="1382c-125">Значение — это полный путь к команде, публикацию которой нужно отменить.</span><span class="sxs-lookup"><span data-stu-id="1382c-125">The value data is the full path for the command that you want to unpublish.</span></span> <span data-ttu-id="1382c-126">Полный путь можно найти, щелкнув правой кнопкой мыши ярлык в меню " **Пуск** " для приложения, которое вы не хотите публиковать, и выбрав пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="1382c-126">You can find the full path by right-clicking on the shortcut on the **Start** menu for the application that you do not want published and then clicking **Properties**.</span></span> <span data-ttu-id="1382c-127">Полный путь появится на вкладке **ярлык** в разделе **Целевая**.</span><span class="sxs-lookup"><span data-stu-id="1382c-127">The full path is listed in the **Shortcut** tab under **Target**.</span></span>

        <span data-ttu-id="1382c-128">Например, для программы Microsoft Silverlight полный путь может быть "C:\\program Files Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe".</span><span class="sxs-lookup"><span data-stu-id="1382c-128">For example, for the program Microsoft Silverlight, the full path might be "C:\\Program Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe."</span></span>

        <span data-ttu-id="1382c-129">**Важно!**  Если применимо, удалите знаки кавычек из полного пути при вводе в поле данных значения.</span><span class="sxs-lookup"><span data-stu-id="1382c-129">**Important** If applicable, remove the quotation marks from the full path when you enter it into the value data field.</span></span>

         

5.  <span data-ttu-id="1382c-130">Закройте редактор реестра и перезапустите виртуальную машину MED-V Workspace.</span><span class="sxs-lookup"><span data-stu-id="1382c-130">Close Registry Editor and restart the MED-V workspace virtual machine.</span></span>

    <span data-ttu-id="1382c-131">Приложение по-прежнему устанавливается в рабочую область MED-V, но теперь удаляется из меню **Пуск** главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="1382c-131">The application is still installed in the MED-V workspace but is now removed from the host computer **Start** menu.</span></span>

<span data-ttu-id="1382c-132">Кроме того, вы можете повторно опубликовать исключенное приложение в меню " **Пуск** ", удалив соответствующее значение из ключа VPCVAppExcludeList.</span><span class="sxs-lookup"><span data-stu-id="1382c-132">You can also republish an excluded application to the host **Start** menu by deleting the corresponding value from the VPCVAppExcludeList key.</span></span> <span data-ttu-id="1382c-133">Например, чтобы повторно опубликовать Microsoft Silverlight, щелкните правой кнопкой мыши значение реестра sllauncher.exe и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="1382c-133">For example, to republish Microsoft Silverlight, right-click the registry value sllauncher.exe and select **Delete**.</span></span>

## <span data-ttu-id="1382c-134">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1382c-134">Related topics</span></span>


[<span data-ttu-id="1382c-135">Технический справочник по MED-V</span><span class="sxs-lookup"><span data-stu-id="1382c-135">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

[<span data-ttu-id="1382c-136">Публикация и отмена публикации приложения в рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="1382c-136">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





