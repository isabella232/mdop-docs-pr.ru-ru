---
title: Установка программного обеспечения MBAM 2.5 Server
description: Установка программного обеспечения MBAM 2.5 Server
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823392"
---
# <span data-ttu-id="ec464-103">Установка программного обеспечения MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="ec464-103">Installing the MBAM 2.5 Server Software</span></span>


<span data-ttu-id="ec464-104">В этой статье описано, как установить серверное программное обеспечение Microsoft BitLocker Administration и Monitoring (MBAM) 2,5 с помощью мастера настройки администрирования и мониторинга Microsoft BitLocker либо с помощью параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="ec464-104">This topic describes how to install the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard or by using command-line parameters.</span></span> <span data-ttu-id="ec464-105">Повторите процесс установки сервера для каждого сервера, на котором вы настраиваете MBAM 2,5 компонентов сервера.</span><span class="sxs-lookup"><span data-stu-id="ec464-105">Repeat the server installation process for each server on which you are configuring MBAM 2.5 Server features.</span></span> <span data-ttu-id="ec464-106">После завершения установки ознакомьтесь со статьей [Настройка сервера MBAM 2,5](configuring-the-mbam-25-server-features.md) для настройки функций сервера.</span><span class="sxs-lookup"><span data-stu-id="ec464-106">After you finish the installation, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md) for steps about configuring the Server features.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ec464-107">Прежде чем начать</span><span class="sxs-lookup"><span data-stu-id="ec464-107">Before you start</span></span></th>
<th align="left"><span data-ttu-id="ec464-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ec464-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec464-109">Ознакомьтесь со сведениями о планировании MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="ec464-109">Review the MBAM 2.5 planning information</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="ec464-110">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="ec464-110">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="ec464-111">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ec464-111">MBAM 2.5 Supported Configurations</span></span></a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="ec464-112">Высокоуровневая архитектура для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ec464-112">High-Level Architecture for MBAM 2.5</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec464-113">Сведения о получении файлов журнала</span><span class="sxs-lookup"><span data-stu-id="ec464-113">Read how to get log files</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec464-114">По умолчанию файлы журнала создаются в папке% Temp% локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="ec464-114">By default, log files are created in the local computer’s %temp% folder.</span></span> <span data-ttu-id="ec464-115">Чтобы создать файлы журнала в определенном месте, а не в <strong> папке% temp </strong> %, используйте <strong> </strong> &lt; <em> аргумент расположение/log </em> &gt; .</span><span class="sxs-lookup"><span data-stu-id="ec464-115">To write the log files to a specific location rather than to the <strong>%temp</strong>% folder, use the <strong>/log</strong> &lt;<em>location</em>&gt; argument.</span></span></p>
<p><span data-ttu-id="ec464-116">В журнале событий приложений и служб в Microsoft Windows регистрируются дополнительные события, которые могут быть занесены в журнал в <strong> MBAM- </strong> или <strong> MBAM-веб- </strong> узлы <strong> &gt; &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="ec464-116">Additional events might be logged in Event Viewer in the <strong>MBAM-Setup</strong> or <strong>MBAM-Web</strong> nodes under <strong>Applications and Services Logs &gt; Microsoft &gt; Windows</strong>.</span></span> <span data-ttu-id="ec464-117">Например, если вы удалите MBAM, программа удаления также удалит журналы MBAM-Setup и MBAM-Web в EventViewer.</span><span class="sxs-lookup"><span data-stu-id="ec464-117">For example, if you uninstall MBAM, the uninstaller will also uninstall the MBAM-Setup and MBAM-Web logs in EventViewer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ec464-118">Установка программного обеспечения сервера MBAM 2,5 с помощью мастера настройки администрирования и мониторинга Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="ec464-118">Installing the MBAM 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard</span></span>


<span data-ttu-id="ec464-119">Выполните указанные ниже действия, чтобы установить программное обеспечение сервера MBAM с помощью мастера настройки администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ec464-119">Use these steps to install the MBAM Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="ec464-120">Установка программного обеспечения сервера MBAM 2,5 с помощью мастера</span><span class="sxs-lookup"><span data-stu-id="ec464-120">To install the MBAM 2.5 Server software by using the wizard</span></span>**

1.  <span data-ttu-id="ec464-121">На сервере, на котором вы хотите установить MBAM, запустите мастер настройки администрирования и наблюдения за помощью **MBAMserversetup.exe** Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ec464-121">On the server where you want to install MBAM, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="ec464-122">На странице **приветствия** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ec464-122">On the **Welcome** page, click **Next**.</span></span>

3.  <span data-ttu-id="ec464-123">Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="ec464-123">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="ec464-124">Укажите, следует ли использовать Microsoft Update при проверке обновлений, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ec464-124">Choose whether to use Microsoft Update when you check for updates, and then click **Next**.</span></span>

5.  <span data-ttu-id="ec464-125">Укажите, нужно ли принимать участие в программе улучшения качества программного обеспечения, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ec464-125">Choose whether to participate in the Customer Experience Improvement Program, and then click **Next**.</span></span>

6.  <span data-ttu-id="ec464-126">Чтобы начать установку, нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="ec464-126">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="ec464-127">Чтобы настроить компоненты сервера после завершения установки программного обеспечения сервера MBAM, установите флажок **выполнить настройку сервера MBAM после закрытия окна мастера** .</span><span class="sxs-lookup"><span data-stu-id="ec464-127">To configure the server features after the MBAM Server software finishes installing, select the **Run MBAM Server Configuration after the wizard closes** check box.</span></span> <span data-ttu-id="ec464-128">Кроме того, вы можете настроить MBAM позже с помощью ярлыка **конфигурации сервера MBAM** , который будет создан при установке сервера в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="ec464-128">Alternatively, you can configure MBAM later by using the **MBAM Server Configuration** shortcut that the server installation creates on your **Start** menu.</span></span>

8.  <span data-ttu-id="ec464-129">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="ec464-129">Click **Finish**.</span></span>

## <span data-ttu-id="ec464-130">Установка программного обеспечения сервера MBAM 2,5 с помощью окна командной строки</span><span class="sxs-lookup"><span data-stu-id="ec464-130">Installing the MBAM 2.5 Server software by using a Command Prompt window</span></span>


<span data-ttu-id="ec464-131">Чтобы установить программное обеспечение сервера MBAM, в командной строке введите команду примерно так, как показано в следующей команде.</span><span class="sxs-lookup"><span data-stu-id="ec464-131">At a command prompt, type a command similar to the following command to install the MBAM Server software.</span></span>

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

<span data-ttu-id="ec464-132">В приведенной ниже таблице описаны параметры командной строки для установки программного обеспечения сервера MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="ec464-132">The following table describes the command-line parameters for installing the MBAM 2.5 Server software.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ec464-133">Параметр</span><span class="sxs-lookup"><span data-stu-id="ec464-133">Parameter</span></span></th>
<th align="left"><span data-ttu-id="ec464-134">Значение параметра</span><span class="sxs-lookup"><span data-stu-id="ec464-134">Parameter value</span></span></th>
<th align="left"><span data-ttu-id="ec464-135">Описание</span><span class="sxs-lookup"><span data-stu-id="ec464-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec464-136">CEIPENABLED</span><span class="sxs-lookup"><span data-stu-id="ec464-136">CEIPENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec464-137">Истина ложь</span><span class="sxs-lookup"><span data-stu-id="ec464-137">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec464-138">Истина — участие в программе улучшения качества программного обеспечения, которая помогает корпорации Майкрософт определить, какие функции MBAM нужно улучшить.</span><span class="sxs-lookup"><span data-stu-id="ec464-138">True - participate in the Customer Improvement Experience Program, which helps Microsoft identify which MBAM features to improve.</span></span></p>
<p><span data-ttu-id="ec464-139">Ложь – не принимать участие в программе улучшения качества программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="ec464-139">False – do not participate in the Customer Improvement Experience Program.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec464-140">OPTIN_FOR_MICROSOFT_UPDATES</span><span class="sxs-lookup"><span data-stu-id="ec464-140">OPTIN_FOR_MICROSOFT_UPDATES</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec464-141">Истина ложь</span><span class="sxs-lookup"><span data-stu-id="ec464-141">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec464-142">Истина — используйте Microsoft Update для обеспечения безопасности и актуальности вашего компьютера для Windows и других продуктов Майкрософт, включая MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec464-142">True - use Microsoft Update to keep your computer secure and up-to-date for Windows and other Microsoft products, including MBAM.</span></span></p>
<p><span data-ttu-id="ec464-143">False — не использовать центра обновления Майкрософт</span><span class="sxs-lookup"><span data-stu-id="ec464-143">False – do not use Microsoft Update</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec464-144">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="ec464-144">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec464-145">&lt;Путь&gt;</span><span class="sxs-lookup"><span data-stu-id="ec464-145">&lt;Path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec464-146">Расположение, в которое вы хотите установить MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec464-146">Location where you want to install MBAM.</span></span></p>
<p><span data-ttu-id="ec464-147">Пример.</span><span class="sxs-lookup"><span data-stu-id="ec464-147">Example:</span></span></p>
<p><span data-ttu-id="ec464-148">INSTALLDIR = c:\mbaminstall</span><span class="sxs-lookup"><span data-stu-id="ec464-148">INSTALLDIR=c:\mbaminstall</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec464-149">FORCE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="ec464-149">FORCE_UNINSTALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec464-150">Истина ложь</span><span class="sxs-lookup"><span data-stu-id="ec464-150">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec464-151">True-продолжить процесс удаления MBAM, даже если все компоненты не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="ec464-151">True - continue the process of uninstalling MBAM, even if any features fail to be removed.</span></span></p>
<p><span data-ttu-id="ec464-152">False (значение по умолчанию) Если настраиваемое действие по удалению не может удалить добавленный компонент сервера MBAM, удаление завершается сбоем и MBAM остается установленным.</span><span class="sxs-lookup"><span data-stu-id="ec464-152">False (default) if the uninstallation custom action fails to remove an added MBAM Server feature, the uninstallation fails, and MBAM remains installed.</span></span></p>
<p><span data-ttu-id="ec464-153">В обоих случаях все возможности, которые были успешно удалены при попытке удалить MBAM, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="ec464-153">In both instances, any features that were successfully removed during the attempt to uninstall MBAM stay removed.</span></span></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="ec464-154">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ec464-154">Related topics</span></span>


[<span data-ttu-id="ec464-155">Развертывание MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ec464-155">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="ec464-156">Настройка компонентов сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="ec464-156">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="ec464-157">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="ec464-157">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ec464-158">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="ec464-158">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ec464-159">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ec464-159">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





