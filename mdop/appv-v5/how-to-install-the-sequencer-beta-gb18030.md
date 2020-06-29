---
title: Установка программы Sequencer
description: Установка программы Sequencer
author: dansimp
ms.assetid: a122caf0-f408-458c-b119-dc84123c1d58
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8542abfecd7f1d543228ab1a86a59b9ee918947
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813952"
---
# <span data-ttu-id="cd968-103">Установка программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="cd968-103">How to Install the Sequencer</span></span>


<span data-ttu-id="cd968-104">Чтобы установить Microsoft Application Virtualization (App-V) 5,0 Sequencer, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cd968-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 sequencer.</span></span> <span data-ttu-id="cd968-105">На компьютере, на котором будет выполняться секвенсор, не должна выполняться какая-либо версия клиента App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="cd968-105">The computer that will run the sequencer must not be running any version of the App-V 5.0 client.</span></span>

<span data-ttu-id="cd968-106">Обновление предыдущей установки секвенсора App-V не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cd968-106">Upgrading a previous installation of the App-V sequencer is not supported.</span></span>

<span data-ttu-id="cd968-107">**Важно!**  Полный список требований к секвенсору см. разделы секвенсора, необходимые для [App-v 5,0](app-v-50-prerequisites.md) и [Поддерживаемые конфигурации app-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="cd968-107">**Important** For a full list of the sequencer requirements see sequencer sections of [App-V 5.0 Prerequisites](app-v-50-prerequisites.md) and [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

 

<span data-ttu-id="cd968-108">Для установки секвенсора App-V 5,0 также можно использовать командную строку.</span><span class="sxs-lookup"><span data-stu-id="cd968-108">You can also use the command line to install the App-V 5.0 sequencer.</span></span> <span data-ttu-id="cd968-109">В следующем списке приведены сведения о параметрах для установки секвенсора с помощью командной строки и **appv\_sequencer\_setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="cd968-109">The following list displays information about options for installing the sequencer using the command line and **appv\_sequencer\_setup.exe**:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd968-110">Команда</span><span class="sxs-lookup"><span data-stu-id="cd968-110">Command</span></span></th>
<th align="left"><span data-ttu-id="cd968-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cd968-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd968-112">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="cd968-112">/INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd968-113">Указывает каталог установки.</span><span class="sxs-lookup"><span data-stu-id="cd968-113">Specifies the installation directory.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd968-114">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="cd968-114">/CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd968-115">Включает участие в программе улучшения качества программного обеспечения Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="cd968-115">Enables participation in the Microsoft Customer Experience Improvement Program.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd968-116">/Log</span><span class="sxs-lookup"><span data-stu-id="cd968-116">/Log</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd968-117">Указывает место сохранения журнала установки: <strong> % temp% </strong> .</span><span class="sxs-lookup"><span data-stu-id="cd968-117">Specifies where the installation log will be saved, the default location is <strong>%Temp%</strong>.</span></span> <span data-ttu-id="cd968-118">Например, <strong> C:\ Журналы — log. log </strong> .</span><span class="sxs-lookup"><span data-stu-id="cd968-118">For example, <strong>C:\ Logs \ log.log</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd968-119">/q</span><span class="sxs-lookup"><span data-stu-id="cd968-119">/q</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd968-120">Указывает на автоматическую или автоматическую установку.</span><span class="sxs-lookup"><span data-stu-id="cd968-120">Specifies a quiet or silent installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd968-121">/Uninstall</span><span class="sxs-lookup"><span data-stu-id="cd968-121">/Uninstall</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd968-122">Задает удаление секвенсора.</span><span class="sxs-lookup"><span data-stu-id="cd968-122">Specifies the removal of the sequencer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd968-123">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="cd968-123">/ACCEPTEULA</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd968-124">Принимает лицензионное соглашение.</span><span class="sxs-lookup"><span data-stu-id="cd968-124">Accepts the license agreement.</span></span> <span data-ttu-id="cd968-125">Это необходимо для автоматической установки.</span><span class="sxs-lookup"><span data-stu-id="cd968-125">This is required for an unattended installation.</span></span> <span data-ttu-id="cd968-126">Пример использования: <strong> /ACCEPTEULA </strong> или <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="cd968-126">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd968-127">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="cd968-127">/LAYOUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd968-128">Задает связанное действие макета.</span><span class="sxs-lookup"><span data-stu-id="cd968-128">Specifies the associated layout action.</span></span> <span data-ttu-id="cd968-129">Кроме того, приложение App-V 5,0 будет извлечено из файла установщика Windows (MSI) и файлов сценариев в папку.</span><span class="sxs-lookup"><span data-stu-id="cd968-129">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.0.</span></span> <span data-ttu-id="cd968-130">Значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="cd968-130">No value is expected.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd968-131">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="cd968-131">/LAYOUTDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd968-132">Указывает каталог макета.</span><span class="sxs-lookup"><span data-stu-id="cd968-132">Specifies the layout directory.</span></span> <span data-ttu-id="cd968-133">Требуется строковое значение.</span><span class="sxs-lookup"><span data-stu-id="cd968-133">Requires a string value.</span></span> <span data-ttu-id="cd968-134">Пример использования: <strong> /LAYOUTDIR = "клиент виртуализации C:\Application" </strong> .</span><span class="sxs-lookup"><span data-stu-id="cd968-134">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd968-135">/?</span><span class="sxs-lookup"><span data-stu-id="cd968-135">/?</span></span> <span data-ttu-id="cd968-136">Или/h или/Help</span><span class="sxs-lookup"><span data-stu-id="cd968-136">Or /h or /help</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd968-137">Отображает связанную справку.</span><span class="sxs-lookup"><span data-stu-id="cd968-137">Displays associated help.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="cd968-138">Установка секвенсора App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="cd968-138">To install the App-V 5.0 sequencer</span></span>**

1.  <span data-ttu-id="cd968-139">Скопируйте файлы установки программы Sequencer App-V 5,0 на компьютер, на котором он будет установлен.</span><span class="sxs-lookup"><span data-stu-id="cd968-139">Copy the App-V 5.0 sequencer installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="cd968-140">Дважды щелкните **appv\_sequencer\_setup.exe** и нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="cd968-140">Double-click **appv\_sequencer\_setup.exe** and then click **Install**.</span></span>

2.  <span data-ttu-id="cd968-141">На странице **условия лицензии на программное обеспечение** ознакомьтесь с условиями лицензионного соглашения.</span><span class="sxs-lookup"><span data-stu-id="cd968-141">On the **Software License Terms** page, you should review the license terms.</span></span> <span data-ttu-id="cd968-142">Чтобы согласиться с условиями лицензионного соглашения, выберите **я принимаю условия лицензионного соглашения.**</span><span class="sxs-lookup"><span data-stu-id="cd968-142">To accept the license terms select **I accept the license terms.**</span></span> <span data-ttu-id="cd968-143">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cd968-143">Click **Next**.</span></span>

3.  <span data-ttu-id="cd968-144">На странице **Использование центра обновления Майкрософт, чтобы обеспечить безопасность и актуальность** данных на компьютере, чтобы включить обновления Microsoft, выберите **использовать Microsoft Update при проверке обновлений (рекомендуется).**</span><span class="sxs-lookup"><span data-stu-id="cd968-144">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="cd968-145">Чтобы отключить обновления Майкрософт, выберите **я не хочу использовать Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="cd968-145">To disable Microsoft updates from running select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="cd968-146">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cd968-146">Click **Next**.</span></span>

4.  <span data-ttu-id="cd968-147">На странице **программы улучшения качества** программного обеспечения, чтобы принять участие в программе, выберите **присоединиться к программе улучшения качества**программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="cd968-147">On the **Customer Experience Improvement Program** page, to participate in the program select **Join the Customer Experience Improvement Program**.</span></span> <span data-ttu-id="cd968-148">Это позволит собирать сведения о том, как вы используете App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="cd968-148">This will allow information to be collected about how you are using App-V 5.0.</span></span> <span data-ttu-id="cd968-149">Если вы не хотите принимать участие в программе, выберите в **настоящее время присоединиться к программе не нужно**.</span><span class="sxs-lookup"><span data-stu-id="cd968-149">If you don’t want to participate in the program select **I don’t want to join the program at this time**.</span></span> <span data-ttu-id="cd968-150">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="cd968-150">Click **Install**.</span></span>

5.  <span data-ttu-id="cd968-151">Чтобы открыть секвенсор, нажмите кнопку **Пуск** , а затем выберите **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="cd968-151">To open the sequencer, click **Start** and then click **Microsoft Application Virtualization Sequencer**.</span></span>

**<span data-ttu-id="cd968-152">Устранение неполадок при установке App-V 5,0 Sequencer</span><span class="sxs-lookup"><span data-stu-id="cd968-152">To troubleshoot the App-V 5.0 sequencer installation</span></span>**

-   <span data-ttu-id="cd968-153">Для получения дополнительных сведений об установке программы Sequencer вы можете просмотреть журнал ошибок в папке **% TEMP%** .</span><span class="sxs-lookup"><span data-stu-id="cd968-153">For more information regarding the sequencer installation, you can view the error log in the **%temp%** folder.</span></span> <span data-ttu-id="cd968-154">Чтобы просмотреть файлы журнала, нажмите кнопку **Пуск**, введите **% TEMP%**, а затем найдите **Журнал appv\_**.</span><span class="sxs-lookup"><span data-stu-id="cd968-154">To review the log files, click **Start**, type **%temp%**, and then look for the **appv\_ log**.</span></span>

    <span data-ttu-id="cd968-155">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="cd968-155">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="cd968-156">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="cd968-156">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="cd968-157">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="cd968-157">Got an App-V issue?</span></span>** <span data-ttu-id="cd968-158">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="cd968-158">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="cd968-159">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="cd968-159">Related topics</span></span>


[<span data-ttu-id="cd968-160">Планирование развертывания App-V</span><span class="sxs-lookup"><span data-stu-id="cd968-160">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





