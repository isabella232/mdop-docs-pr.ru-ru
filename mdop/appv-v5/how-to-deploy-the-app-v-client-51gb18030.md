---
title: Развертывание клиента App-V
description: Развертывание клиента App-V
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814125"
---
# <span data-ttu-id="a88c2-103">Развертывание клиента App-V</span><span class="sxs-lookup"><span data-stu-id="a88c2-103">How to Deploy the App-V Client</span></span>


<span data-ttu-id="a88c2-104">Чтобы установить клиент служб Microsoft Application Virtualization (App-V) 5,1 и клиент службы удаленных рабочих столов, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a88c2-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 client and Remote Desktop Services client.</span></span> <span data-ttu-id="a88c2-105">Необходимо установить версию клиента, соответствующую операционной системе целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="a88c2-105">You must install the version of the client that matches the operating system of the target computer.</span></span>

<a href="" id="bkmk-clt-install-prereqs"></a>**<span data-ttu-id="a88c2-106">Что необходимо сделать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="a88c2-106">What to do before you start</span></span>**

1. <span data-ttu-id="a88c2-107">Проверьте и установите необходимые компоненты программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="a88c2-107">Review and install the software prerequisites:</span></span>

   <span data-ttu-id="a88c2-108">Установите необходимое программное обеспечение, соответствующее версии App-V, которую вы устанавливаете:</span><span class="sxs-lookup"><span data-stu-id="a88c2-108">Install the prerequisite software that corresponds to the version of App-V that you are installing:</span></span>

   -   [<span data-ttu-id="a88c2-109">Сведения об App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a88c2-109">About App-V 5.1</span></span>](about-app-v-51.md)

   -   [<span data-ttu-id="a88c2-110">Предварительные требования App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a88c2-110">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)

2. <span data-ttu-id="a88c2-111">Проверка сосуществования клиентов и неподдерживаемых сценариев, применимых к установке:</span><span class="sxs-lookup"><span data-stu-id="a88c2-111">Review the client coexistence and unsupported scenarios, as applicable to your installation:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-112">Развертывание существующих клиентов App-V</span><span class="sxs-lookup"><span data-stu-id="a88c2-112">Deploying coexisting App-V clients</span></span></p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)"><span data-ttu-id="a88c2-113">Планирование развертывания программы Sequencer и клиента App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a88c2-113">Planning for the App-V 5.1 Sequencer and Client Deployment</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-114">Неподдерживаемые или ограниченные сценарии установки</span><span class="sxs-lookup"><span data-stu-id="a88c2-114">Unsupported or limited installation scenarios</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-115"><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">Поддерживаемые конфигурации App-V 5,1 см. в разделе "клиент"</span><span class="sxs-lookup"><span data-stu-id="a88c2-115">See the client section in <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-V 5.1 Supported Configurations</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="a88c2-116">Ознакомьтесь со сведениями о поиске и устранении неполадок в реестре клиента.</span><span class="sxs-lookup"><span data-stu-id="a88c2-116">Review the locations for client registry, log, and troubleshooting information:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a88c2-117">Сведения о клиентском реестре</span><span class="sxs-lookup"><span data-stu-id="a88c2-117">Client registry information</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a88c2-118">По умолчанию после установки клиента App-V 5,1 сведения о клиенте хранятся в реестре в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="a88c2-118">By default, after you install the App-V 5.1 client, the client information is stored in the registry in the following registry key:</span></span></p>
<p><strong><span data-ttu-id="a88c2-119">HKEY_LOCAL_MACHINE \ ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ \ MICROSOFT \ APPV \ КЛИЕНТ</span><span class="sxs-lookup"><span data-stu-id="a88c2-119">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT</span></span></strong></p></li>
<li><p><span data-ttu-id="a88c2-120">При развертывании виртуализированного пакета на компьютере, на котором запущен клиент App-V, связанные данные пакета хранятся в следующем расположении:</span><span class="sxs-lookup"><span data-stu-id="a88c2-120">When you deploy a virtualized package to a computer that is running the App-V client, the associated package data is stored in the following location:</span></span></p>
<p><strong><span data-ttu-id="a88c2-121">C: \ ProgramData \ App-V</span><span class="sxs-lookup"><span data-stu-id="a88c2-121">C: \ ProgramData \ App-V</span></span></strong></p>
<p><span data-ttu-id="a88c2-122">Однако вы можете изменить это расположение с помощью следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="a88c2-122">However, you can reconfigure this location with the following registry key:</span></span></p>
<p><strong><span data-ttu-id="a88c2-123">HKEY_LOCAL_MACHINE \ ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ \ MICROSOFT \ ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ \ MICROSOFT \ APPV \ КЛИЕНТ \ STREAMING \ PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="a88c2-123">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a88c2-124">Файлы журнала клиента</span><span class="sxs-lookup"><span data-stu-id="a88c2-124">Client log files</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a88c2-125">Сведения о файле журнала, связанном с клиентом App-V 5,1, можно найти в следующем журнале:</span><span class="sxs-lookup"><span data-stu-id="a88c2-125">For log file information that is associated with the App-V 5.1 Client, search in the following log:</span></span></p>
<p><strong><span data-ttu-id="a88c2-126">Журналы событий, журналы приложений и служб/Microsoft/AppV</span><span class="sxs-lookup"><span data-stu-id="a88c2-126">Event logs / Applications and Services Logs / Microsoft / AppV</span></span></strong></p></li>
<li><p><span data-ttu-id="a88c2-127">В приложении App-V 5,0 с пакетом обновления 3 (SP3) некоторые журналы были консолидированы и перемещены в следующее расположение:</span><span class="sxs-lookup"><span data-stu-id="a88c2-127">In App-V 5.0 SP3, some logs were consolidated and moved to the following location:</span></span></p>
<p><strong><span data-ttu-id="a88c2-128">Журналы событий, журналы приложений и служб (Microsoft/AppV/ServiceLog)</span><span class="sxs-lookup"><span data-stu-id="a88c2-128">Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog</span></span></strong></p>
<p><span data-ttu-id="a88c2-129">Список перемещенных журналов можно найти в разделе <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> о приложении App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="a88c2-129">For a list of the moved logs, see <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)">About App-V 5.0 SP3</a>.</span></span></p></li>
<li><p><span data-ttu-id="a88c2-130">Пакеты, которые в настоящее время хранятся на компьютерах, на которых запущен клиент App-V 5,1, сохраняются в следующем расположении:</span><span class="sxs-lookup"><span data-stu-id="a88c2-130">Packages that are currently stored on computers that run the App-V 5.1 Client are saved to the following location:</span></span></p>
<p><strong><span data-ttu-id="a88c2-131">C:\ProgramData\App-V &amp; lt; код пакета &gt; &amp; lt; ИД версии&gt;</span><span class="sxs-lookup"><span data-stu-id="a88c2-131">C:\ProgramData\App-V&amp;lt;package id&gt;&amp;lt;version id&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a88c2-132">Сведения об устранении неполадок при установке клиента</span><span class="sxs-lookup"><span data-stu-id="a88c2-132">Client installation troubleshooting information</span></span></p></td>
<td align="left"><p><span data-ttu-id="a88c2-133">Просмотрите журнал ошибок в <strong> папке% temp% </strong> .</span><span class="sxs-lookup"><span data-stu-id="a88c2-133">See the error log in the <strong>%temp%</strong> folder.</span></span> <span data-ttu-id="a88c2-134">Чтобы просмотреть файлы журнала, нажмите кнопку <strong> Пуск </strong> , введите <strong> % temp% </strong> , а затем найдите <strong> Журнал appv_ </strong> .</span><span class="sxs-lookup"><span data-stu-id="a88c2-134">To review the log files, click <strong>Start</strong>, type <strong>%temp%</strong>, and then look for the <strong>appv_ log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="a88c2-135">Установка клиента App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a88c2-135">To install the App-V 5.1 Client</span></span>**

1.  <span data-ttu-id="a88c2-136">Скопируйте установочный файл для клиента App-V 5,1 на компьютер, на котором он будет установлен.</span><span class="sxs-lookup"><span data-stu-id="a88c2-136">Copy the App-V 5.1 client installation file to the computer on which it will be installed.</span></span> <span data-ttu-id="a88c2-137">Выберите один из следующих типов клиентов:</span><span class="sxs-lookup"><span data-stu-id="a88c2-137">Choose from the following client types:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a88c2-138">Тип клиента</span><span class="sxs-lookup"><span data-stu-id="a88c2-138">Client type</span></span></th>
    <th align="left"><span data-ttu-id="a88c2-139">Файл для использования</span><span class="sxs-lookup"><span data-stu-id="a88c2-139">File to use</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a88c2-140">Стандартная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a88c2-140">Standard version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="a88c2-141">appv_client_setup.exe</span><span class="sxs-lookup"><span data-stu-id="a88c2-141">appv_client_setup.exe</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a88c2-142">Версия клиента служб удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="a88c2-142">Remote Desktop Services version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="a88c2-143">appv_client_setup_rds.exe</span><span class="sxs-lookup"><span data-stu-id="a88c2-143">appv_client_setup_rds.exe</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="a88c2-144">Дважды щелкните файл установки и нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="a88c2-144">Double-click the installation file, and click **Install**.</span></span> <span data-ttu-id="a88c2-145">Перед началом установки установщик проверяет на компьютере отсутствие [необходимых предварительных требований для App-V 5,1](app-v-51-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="a88c2-145">Before the installation begins, the installer checks the computer for any missing [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

3.  <span data-ttu-id="a88c2-146">Прочтите и примите условия лицензионного соглашения на использование программного обеспечения, выберите, нужно ли использовать Microsoft Update и нужно ли принимать участие в программе улучшения качества по Майкрософт, и нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="a88c2-146">Review and accept the Software License Terms, choose whether to use Microsoft Update and whether to participate in the Microsoft Customer Experience Improvement Program, and click **Install**.</span></span>

4.  <span data-ttu-id="a88c2-147">На странице **Настройка успешно завершена** нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="a88c2-147">On the **Setup completed successfully** page, click **Close**.</span></span>

    <span data-ttu-id="a88c2-148">При установке создаются следующие записи для клиента App-V в **приложениях**.</span><span class="sxs-lookup"><span data-stu-id="a88c2-148">The installation creates the following entries for the App-V client in **Programs**:</span></span>

    -   **<span data-ttu-id="a88c2-149">.exe</span><span class="sxs-lookup"><span data-stu-id="a88c2-149">.exe</span></span>**

    -   **<span data-ttu-id="a88c2-150">.msi</span><span class="sxs-lookup"><span data-stu-id="a88c2-150">.msi</span></span>**

    -   **<span data-ttu-id="a88c2-151">языковой пакет</span><span class="sxs-lookup"><span data-stu-id="a88c2-151">language pack</span></span>**

        **<span data-ttu-id="a88c2-152">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a88c2-152">Note</span></span>**  
        <span data-ttu-id="a88c2-153">После установки можно удалить только exe – файл.</span><span class="sxs-lookup"><span data-stu-id="a88c2-153">After the installation, only the .exe file can be uninstalled.</span></span>



**<span data-ttu-id="a88c2-154">Установка клиента App-V 5,1 с помощью сценария</span><span class="sxs-lookup"><span data-stu-id="a88c2-154">To install the App-V 5.1 client using a script</span></span>**

1. <span data-ttu-id="a88c2-155">Установите все необходимое программное обеспечение на целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="a88c2-155">Install all of the required prerequisite software on the target computers.</span></span> <span data-ttu-id="a88c2-156">Узнайте, [что необходимо сделать перед](#bkmk-clt-install-prereqs)началом работы.</span><span class="sxs-lookup"><span data-stu-id="a88c2-156">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="a88c2-157">Если вы установили клиент с помощью MSI-файла, то при отсутствии необходимых условий установка завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="a88c2-157">If you install the client by using an .msi file, the installation will fail if any prerequisites are missing.</span></span>

2. <span data-ttu-id="a88c2-158">Чтобы использовать сценарий для установки клиента App-V 5,1, используйте следующие параметры с **appv\_client\_setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="a88c2-158">To use a script to install the App-V 5.1 client, use the following parameters with **appv\_client\_setup.exe**.</span></span>

   **<span data-ttu-id="a88c2-159">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a88c2-159">Note</span></span>**  
   <span data-ttu-id="a88c2-160">Клиентский установщик Windows (MSI) поддерживает один и тот же набор переключателей, за исключением параметра **/log** .</span><span class="sxs-lookup"><span data-stu-id="a88c2-160">The client Windows Installer (.msi) supports the same set of switches, except for the **/LOG** parameter.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-161">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="a88c2-161">/INSTALLDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-162">Указывает каталог установки.</span><span class="sxs-lookup"><span data-stu-id="a88c2-162">Specifies the installation directory.</span></span> <span data-ttu-id="a88c2-163">Пример использования: <strong> /INSTALLDIR = C:\Program Files\AppV Client</span><span class="sxs-lookup"><span data-stu-id="a88c2-163">Example usage: <strong>/INSTALLDIR=C:\Program Files\AppV Client</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-164">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="a88c2-164">/CEIPOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-165">Включает участие в программе улучшения качества программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="a88c2-165">Enables participation in the Customer Experience Improvement Program.</span></span> <span data-ttu-id="a88c2-166">Пример использования: <strong> /CEIPOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a88c2-166">Example usage: <strong>/CEIPOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-167">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="a88c2-167">/MUOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-168">Включение центра обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a88c2-168">Enables Microsoft Update.</span></span> <span data-ttu-id="a88c2-169">Пример использования: <strong> /MUOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a88c2-169">Example usage: <strong>/MUOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-170">/PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="a88c2-170">/PACKAGEINSTALLATIONROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-171">Задает каталог, в который устанавливаются все новые приложения и обновления.</span><span class="sxs-lookup"><span data-stu-id="a88c2-171">Specifies the directory in which to install all new applications and updates.</span></span> <span data-ttu-id="a88c2-172">Пример использования: <strong> /PACKAGEINSTALLATIONROOT =&#39;C:\App-V packages&#39;</span><span class="sxs-lookup"><span data-stu-id="a88c2-172">Example usage: <strong>/PACKAGEINSTALLATIONROOT=&#39;C:\App-V Packages&#39;</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-173">/PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="a88c2-173">/PACKAGESOURCEROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-174">Переопределяет исходное расположение для загрузки содержимого пакета.</span><span class="sxs-lookup"><span data-stu-id="a88c2-174">Overrides the source location for downloading package content.</span></span> <span data-ttu-id="a88c2-175">Пример использования: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</span><span class="sxs-lookup"><span data-stu-id="a88c2-175">Example usage: <strong>/PACKAGESOURCEROOT=&#39;<a href="http://packageStore" data-raw-source="http://packageStore">http://packageStore</a>&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-176">/AUTOLOAD</span><span class="sxs-lookup"><span data-stu-id="a88c2-176">/AUTOLOAD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-177">Указывает, как приложение App-V 5,1 будет загружать новые пакеты для определенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="a88c2-177">Specifies how new packages will be loaded by App-V 5.1 on a specific computer.</span></span> <span data-ttu-id="a88c2-178">Доступны следующие параметры: [1]; Автоматическая загрузка всех пакетов [2]; или автоматически загружает пакеты [0]. <strong> Пример использования:/AUTOLOAD = [0 | 1 | 2]</span><span class="sxs-lookup"><span data-stu-id="a88c2-178">The following options are enabled: [1]; automatically load all packages [2]; or automatically load no packages [0].<strong>Example usage: /AUTOLOAD=[0|1|2]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-179">/SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="a88c2-179">/SHAREDCONTENTSTOREMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-180">Указывает на то, что содержимое потокового пакета не будет сохранено на локальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="a88c2-180">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span> <span data-ttu-id="a88c2-181">Пример использования: <strong> /SHAREDCONTENTSTOREMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a88c2-181">Example usage: <strong>/SHAREDCONTENTSTOREMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-182">/MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="a88c2-182">/MIGRATIONMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-183">Позволяет клиенту App-V 5,1 изменять сочетания клавиш и FTAs, связанные с пакетами, созданными с помощью более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="a88c2-183">Allows the App-V 5.1 client to modify the shortcuts and FTAs that are associated with the packages that are created with a previous version.</span></span> <span data-ttu-id="a88c2-184">Пример использования: <strong> /MIGRATIONMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a88c2-184">Example usage: <strong>/MIGRATIONMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-185">/ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="a88c2-185">/ENABLEPACKAGESCRIPTS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-186">Включает сценарии, определенные в файле манифеста пакета или файлах конфигурации, которые должны выполняться.</span><span class="sxs-lookup"><span data-stu-id="a88c2-186">Enables the scripts that are defined in the package manifest file or configuration files that should run.</span></span> <span data-ttu-id="a88c2-187">Пример использования: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a88c2-187">Example usage: <strong>/ENABLEPACKAGESCRIPTS=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-188">/ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="a88c2-188">/ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-189">Указывает пути реестра, которые не будут перемещаться с помощью профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="a88c2-189">Specifies the registry paths that will not roam with a user profile.</span></span> <span data-ttu-id="a88c2-190">Пример использования: <strong> /ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</span><span class="sxs-lookup"><span data-stu-id="a88c2-190">Example usage: <strong>/ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-191">/ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="a88c2-191">/ROAMINGFILEEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-192">Указывает пути к файлам относительно% UserProfile%, которые не перемещаются с помощью профиля пользователя&#39;s.</span><span class="sxs-lookup"><span data-stu-id="a88c2-192">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="a88c2-193">Пример использования: <strong> /ROAMINGFILEEXCLUSIONS &#39;Desktop; мои рисунки&#39;</span><span class="sxs-lookup"><span data-stu-id="a88c2-193">Example usage: <strong>/ROAMINGFILEEXCLUSIONS &#39;desktop;my pictures&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-194">/S [1-5] PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="a88c2-194">/S[1-5]PUBLISHINGSERVERNAME</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-195">Отображает имя сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="a88c2-195">Displays the name of the publishing server.</span></span> <span data-ttu-id="a88c2-196">Пример использования: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</span><span class="sxs-lookup"><span data-stu-id="a88c2-196">Example usage: <strong>/S2PUBLISHINGSERVERNAME=MyPublishingServer</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-197">/S [1-5] PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="a88c2-197">/S[1-5]PUBLISHINGSERVERURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-198">Отображает URL-адрес сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="a88c2-198">Displays the URL of the publishing server.</span></span> <span data-ttu-id="a88c2-199">Пример использования: <strong> /S2PUBLISHINGSERVERURL = \pubserver</span><span class="sxs-lookup"><span data-stu-id="a88c2-199">Example usage: <strong>/S2PUBLISHINGSERVERURL=\pubserver</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-200">/S [1-5] GLOBALREFRESHENABLED-</span><span class="sxs-lookup"><span data-stu-id="a88c2-200">/S[1-5]GLOBALREFRESHENABLED -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-201">Включает глобальное обновление публикации.</span><span class="sxs-lookup"><span data-stu-id="a88c2-201">Enables a global publishing refresh.</span></span> <span data-ttu-id="a88c2-202">Пример использования: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a88c2-202">Example usage: <strong>/S2GLOBALREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-203">/S [1-5] GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="a88c2-203">/S[1-5]GLOBALREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-204">Инициирует глобальное обновление публикации при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="a88c2-204">Initiates a global publishing refresh when a user logs on.</span></span> <span data-ttu-id="a88c2-205">Пример использования: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a88c2-205">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-206">/S [1-5] GLOBALREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="a88c2-206">/S[1-5]GLOBALREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-207">Указывает интервал обновления публикации, где <strong> 0 </strong> означает, что обновление не выполняется периодически.</span><span class="sxs-lookup"><span data-stu-id="a88c2-207">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="a88c2-208">Пример использования: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="a88c2-208">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-209">/S [1-5] GLOBALREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="a88c2-209">/S[1-5]GLOBALREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-210">Указывает единицу интервала (часы [0], дни [1]).</span><span class="sxs-lookup"><span data-stu-id="a88c2-210">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="a88c2-211">Пример использования: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a88c2-211">Example usage: <strong>/S2GLOBALREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-212">/S [1-5] USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="a88c2-212">/S[1-5]USERREFRESHENABLED</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-213">Включает обновление публикации пользователей.</span><span class="sxs-lookup"><span data-stu-id="a88c2-213">Enables user publishing refresh.</span></span> <span data-ttu-id="a88c2-214">Пример использования: <strong> /S2USERREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a88c2-214">Example usage: <strong>/S2USERREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-215">/S [1-5] USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="a88c2-215">/S[1-5]USERREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-216">Инициирует обновление публикации пользователя, когда пользователь входит в систему.</span><span class="sxs-lookup"><span data-stu-id="a88c2-216">Initiates a user publishing refresh when a user logs on.</span></span> <span data-ttu-id="a88c2-217">Пример использования: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a88c2-217">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-218">/S [1-5] USERREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="a88c2-218">/S[1-5]USERREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-219">Указывает интервал обновления публикации, где <strong> 0 </strong> означает, что обновление не выполняется периодически.</span><span class="sxs-lookup"><span data-stu-id="a88c2-219">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="a88c2-220">Пример использования: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="a88c2-220">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-221">/S [1-5] USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="a88c2-221">/S[1-5]USERREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-222">Указывает единицу интервала (часы [0], дни [1]).</span><span class="sxs-lookup"><span data-stu-id="a88c2-222">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="a88c2-223">Пример использования: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a88c2-223">Example usage: <strong>/S2USERREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-224">/Log</span><span class="sxs-lookup"><span data-stu-id="a88c2-224">/Log</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-225">Задает расположение, в котором сохраняются данные журнала.</span><span class="sxs-lookup"><span data-stu-id="a88c2-225">Specifies a location where the log information is saved.</span></span> <span data-ttu-id="a88c2-226">По умолчанию используется расположение% Temp%.</span><span class="sxs-lookup"><span data-stu-id="a88c2-226">The default location is %Temp%.</span></span> <span data-ttu-id="a88c2-227">Пример использования: <strong> /log C:\logs\log.log</span><span class="sxs-lookup"><span data-stu-id="a88c2-227">Example usage: <strong>/log C:\logs\log.log</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-228">/q</span><span class="sxs-lookup"><span data-stu-id="a88c2-228">/q</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-229">Указывает на автоматическую установку.</span><span class="sxs-lookup"><span data-stu-id="a88c2-229">Specifies an unattended installation.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-230">/REPAIR</span><span class="sxs-lookup"><span data-stu-id="a88c2-230">/REPAIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-231">Восстановление предыдущей версии клиента.</span><span class="sxs-lookup"><span data-stu-id="a88c2-231">Repairs a previous client installation.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-232">/NORESTART</span><span class="sxs-lookup"><span data-stu-id="a88c2-232">/NORESTART</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-233">Предотвращает перезагрузку компьютера после установки клиента.</span><span class="sxs-lookup"><span data-stu-id="a88c2-233">Prevents the computer from rebooting after the client installation.</span></span></p>
   <p><span data-ttu-id="a88c2-234">Этот параметр предотвращает перезагрузку компьютера конечного пользователя после установки каждого обновления и позволяет запланировать перезагрузку в удобное для вас время.</span><span class="sxs-lookup"><span data-stu-id="a88c2-234">The parameter prevents the end-user computer from rebooting after each update is installed and lets you schedule the reboot at your convenience.</span></span> <span data-ttu-id="a88c2-235">Например, можно установить приложение App-V 5,1, а затем установить пакет исправлений Y без перезагрузки после установки пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="a88c2-235">For example, you can install App-V 5.1 and then install Hotfix Package Y without rebooting after the Service Pack installation.</span></span> <span data-ttu-id="a88c2-236">После установки необходимо перезагрузить компьютер, прежде чем приступить к работе с приложением-V.</span><span class="sxs-lookup"><span data-stu-id="a88c2-236">After the installation, you must reboot before you start using App-V.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-237">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="a88c2-237">/UNINSTALL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-238">Удаление клиента.</span><span class="sxs-lookup"><span data-stu-id="a88c2-238">Uninstalls the client.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-239">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="a88c2-239">/ACCEPTEULA</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-240">Принимает лицензионное соглашение.</span><span class="sxs-lookup"><span data-stu-id="a88c2-240">Accepts the license agreement.</span></span> <span data-ttu-id="a88c2-241">Это необходимо для автоматической установки.</span><span class="sxs-lookup"><span data-stu-id="a88c2-241">This is required for an unattended installation.</span></span> <span data-ttu-id="a88c2-242">Пример использования: <strong> /ACCEPTEULA </strong> или <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="a88c2-242">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-243">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="a88c2-243">/LAYOUT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-244">Задает связанное действие макета.</span><span class="sxs-lookup"><span data-stu-id="a88c2-244">Specifies the associated layout action.</span></span> <span data-ttu-id="a88c2-245">Кроме того, приложение App-V 5,1 будет извлечено из файла установщика Windows (MSI) и файлов сценариев в папку.</span><span class="sxs-lookup"><span data-stu-id="a88c2-245">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.1.</span></span> <span data-ttu-id="a88c2-246">Значение не ожидается.</span><span class="sxs-lookup"><span data-stu-id="a88c2-246">No value is expected.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a88c2-247">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="a88c2-247">/LAYOUTDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-248">Указывает каталог макета.</span><span class="sxs-lookup"><span data-stu-id="a88c2-248">Specifies the layout directory.</span></span> <span data-ttu-id="a88c2-249">Требуется строковое значение.</span><span class="sxs-lookup"><span data-stu-id="a88c2-249">Requires a string value.</span></span> <span data-ttu-id="a88c2-250">Пример использования: <strong> /LAYOUTDIR = "клиент виртуализации C:\Application" </strong> .</span><span class="sxs-lookup"><span data-stu-id="a88c2-250">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a88c2-251">/?,/h,/Help</span><span class="sxs-lookup"><span data-stu-id="a88c2-251">/?, /h, /help</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a88c2-252">Запросы на помощь по предыдущим параметрам установки.</span><span class="sxs-lookup"><span data-stu-id="a88c2-252">Requests help about the previous installation parameters.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="a88c2-253">Установка клиента App-V 5,1 с помощью файла установщика Windows (MSI)</span><span class="sxs-lookup"><span data-stu-id="a88c2-253">To install the App-V 5.1 client by using the Windows Installer (.msi) file</span></span>**

1.  <span data-ttu-id="a88c2-254">Установите необходимые компоненты на целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="a88c2-254">Install the required prerequisites on the target computers.</span></span> <span data-ttu-id="a88c2-255">Узнайте, [что необходимо сделать перед](#bkmk-clt-install-prereqs)началом работы.</span><span class="sxs-lookup"><span data-stu-id="a88c2-255">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="a88c2-256">Если какие – либо условия не выполняются, установка завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="a88c2-256">If any prerequisites are not met, the installation will fail.</span></span>

2.  <span data-ttu-id="a88c2-257">Убедитесь, что на конечных компьютерах нет отложенных перезапусков перед установкой клиента с помощью файлов установщика Windows App-V 5,1 (MSI).</span><span class="sxs-lookup"><span data-stu-id="a88c2-257">Ensure that the target computers do not have any pending restarts before you install the client using the App-V 5.1 Windows Installer (.msi) files.</span></span> <span data-ttu-id="a88c2-258">Файлы установщика Windows не помечают отложенный перезапуск.</span><span class="sxs-lookup"><span data-stu-id="a88c2-258">The Windows Installer files do not flag a pending restart.</span></span>

3.  <span data-ttu-id="a88c2-259">Развернуть один из указанных ниже файлов установщика Windows на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="a88c2-259">Deploy one of the following Windows Installer files to the target computer.</span></span> <span data-ttu-id="a88c2-260">Указанный вами файл должен соответствовать конфигурации целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="a88c2-260">The file that you specify must match the configuration of the target computer.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a88c2-261">Тип развертывания</span><span class="sxs-lookup"><span data-stu-id="a88c2-261">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="a88c2-262">Развертывание файла</span><span class="sxs-lookup"><span data-stu-id="a88c2-262">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a88c2-263">Компьютер работает под управлением 32-разрядной операционной системы Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="a88c2-263">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a88c2-264">appv_client_MSI_x86.msi</span><span class="sxs-lookup"><span data-stu-id="a88c2-264">appv_client_MSI_x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a88c2-265">Компьютер работает под управлением 64-разрядной операционной системы Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="a88c2-265">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a88c2-266">appv_client_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="a88c2-266">appv_client_MSI_x64.msi</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a88c2-267">Вы разворачиваете клиент служб удаленных рабочих столов App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a88c2-267">You are deploying the App-V 5.1 Remote Desktop Services client</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a88c2-268">appv_client_rds_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="a88c2-268">appv_client_rds_MSI_x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="a88c2-269">В соответствии с приведенной ниже таблицей выберите соответствующий языковой пакет **. msi** для установки на основе нужного языка для целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="a88c2-269">Using the information in the following table, select the appropriate language pack **.msi** to install, based on the desired language for the target computer.</span></span> <span data-ttu-id="a88c2-270">**XXXX** в таблице указывает целевой языковой стандарт для языкового пакета.</span><span class="sxs-lookup"><span data-stu-id="a88c2-270">The **xxxx** in the table refers to the target locale of the language pack.</span></span>

    **<span data-ttu-id="a88c2-271">Что нужно знать перед началом работы:</span><span class="sxs-lookup"><span data-stu-id="a88c2-271">What to know before you start:</span></span>**

    -   <span data-ttu-id="a88c2-272">Языковые пакеты являются общими для стандартного клиента App-V 5,1 и версии служб удаленных рабочих столов клиента App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a88c2-272">The language packs are common to both the standard App-V 5.1 client and the Remote Desktop Services version of the App-V 5.1 client.</span></span>

    -   <span data-ttu-id="a88c2-273">Если вы установили клиент App-V 5,1 с помощью **exe**, установщик развернет только языковой пакет, соответствующий операционной системе, работающей на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="a88c2-273">If you install the App-V 5.1 client using the **.exe**, the installer will deploy only the language pack that matches the operating system running on the target computer.</span></span>

    -   <span data-ttu-id="a88c2-274">Чтобы развернуть дополнительные языковые пакеты на целевом компьютере, выполните описанные ниже действия, **чтобы установить клиент App-V 5,1 с помощью файла установщика Windows (MSI)**.</span><span class="sxs-lookup"><span data-stu-id="a88c2-274">To deploy additional language packs on a target computer, use the procedure **To install the App-V 5.1 client by using Windows Installer (.msi) file**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a88c2-275">Тип развертывания</span><span class="sxs-lookup"><span data-stu-id="a88c2-275">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="a88c2-276">Развертывание файла</span><span class="sxs-lookup"><span data-stu-id="a88c2-276">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a88c2-277">Компьютер работает под управлением 32-разрядной операционной системы Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="a88c2-277">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a88c2-278">appv_client_LP_xxxx_ x86.msi</span><span class="sxs-lookup"><span data-stu-id="a88c2-278">appv_client_LP_xxxx_ x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a88c2-279">Компьютер работает под управлением 64-разрядной операционной системы Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="a88c2-279">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a88c2-280">appv_client_LP_xxxx_ x64.msi</span><span class="sxs-lookup"><span data-stu-id="a88c2-280">appv_client_LP_xxxx_ x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="a88c2-281">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a88c2-281">Related topics</span></span>


[<span data-ttu-id="a88c2-282">Развертывание App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a88c2-282">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="a88c2-283">Сведения о параметрах конфигурации клиента</span><span class="sxs-lookup"><span data-stu-id="a88c2-283">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

[<span data-ttu-id="a88c2-284">Удаление клиента App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a88c2-284">How to Uninstall the App-V 5.1 Client</span></span>](how-to-uninstall-the-app-v-51-client.md)









