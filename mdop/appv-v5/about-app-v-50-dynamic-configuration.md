---
title: Сведения о динамической конфигурации App-V 5.0
description: Сведения о динамической конфигурации App-V 5.0
author: dansimp
ms.assetid: 88afaca1-68c5-45c4-a074-9371c56b5804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0294a60570d6dea99193c8bd411639c4888ae6b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815032"
---
# <span data-ttu-id="3c395-103">Сведения о динамической конфигурации App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3c395-103">About App-V 5.0 Dynamic Configuration</span></span>


<span data-ttu-id="3c395-104">Вы можете использовать динамическую конфигурацию для настройки пакета App-V 5,0 для пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c395-104">You can use the dynamic configuration to customize an App-V 5.0 package for a user.</span></span> <span data-ttu-id="3c395-105">Используйте следующие сведения для создания или изменения существующего файла динамической конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3c395-105">Use the following information to create or edit an existing dynamic configuration file.</span></span>

<span data-ttu-id="3c395-106">При изменении файла динамической конфигурации выполняется настройка того, как будет выполняться пакет App-V 5,0 для пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="3c395-106">When you edit the dynamic configuration file it customizes how an App-V 5.0 package will run for a user or group.</span></span> <span data-ttu-id="3c395-107">Это поможет вам создать более удобный способ для настройки пакета, изменив необходимость повторной последовательности пакетов с использованием нужных параметров и обеспечивая независимый способ хранения содержимого пакета и пользовательских параметров.</span><span class="sxs-lookup"><span data-stu-id="3c395-107">This helps to provide a more convenient method for package customization by removing the need to re-sequence packages using the desired settings, and provides a way to keep package content and custom settings independent.</span></span>

## <span data-ttu-id="3c395-108">Дополнительно: Динамическая настройка</span><span class="sxs-lookup"><span data-stu-id="3c395-108">Advanced: Dynamic Configuration</span></span>


<span data-ttu-id="3c395-109">Пакеты виртуальных приложений содержат манифест, который предоставляет все основные сведения о пакете.</span><span class="sxs-lookup"><span data-stu-id="3c395-109">Virtual application packages contain a manifest that provides all the core information for the package.</span></span> <span data-ttu-id="3c395-110">Эти сведения включают значения по умолчанию для параметров пакета и определяют параметры в самой простой форме (без дополнительной настройки).</span><span class="sxs-lookup"><span data-stu-id="3c395-110">This information includes the defaults for the package settings and determines settings in the most basic form (with no additional customization).</span></span> <span data-ttu-id="3c395-111">Если вы хотите изменить эти значения по умолчанию для определенного пользователя или группы, вы можете создавать и изменять следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="3c395-111">If you want to adjust these defaults for a particular user or group, you can create and edit the following files:</span></span>

-   <span data-ttu-id="3c395-112">Файл конфигурации пользователя</span><span class="sxs-lookup"><span data-stu-id="3c395-112">User Configuration file</span></span>

-   <span data-ttu-id="3c395-113">Файл конфигурации развертывания</span><span class="sxs-lookup"><span data-stu-id="3c395-113">Deployment configuration file</span></span>

<span data-ttu-id="3c395-114">В предыдущих XML-файлах задаются параметры пакета и разрешаются настраиваемые пакеты, не влияя на пакеты напрямую.</span><span class="sxs-lookup"><span data-stu-id="3c395-114">The previous .xml files specify package settings and allow for packages to be customized without directly affecting the packages.</span></span> <span data-ttu-id="3c395-115">При создании пакета секвенсор автоматически создает XML-файлы развертывания и конфигурации пользователя по умолчанию с помощью данных манифеста пакета.</span><span class="sxs-lookup"><span data-stu-id="3c395-115">When a package is created, the sequencer automatically generates default deployment and user configuration .xml files using the package manifest data.</span></span> <span data-ttu-id="3c395-116">Таким образом, эти автоматически создаваемые файлы конфигурации отражают параметры по умолчанию, которые пакет по определению не так, как элементы были настроены во время последовательности.</span><span class="sxs-lookup"><span data-stu-id="3c395-116">Therefore, these automatically generated configuration files simply reflect the default settings that the package innately as from how things were configured during sequencing.</span></span> <span data-ttu-id="3c395-117">Если вы применяете эти файлы конфигурации к пакету в форме, созданной секвенсором, пакеты будут иметь те же параметры по умолчанию, которые поставляются из манифеста.</span><span class="sxs-lookup"><span data-stu-id="3c395-117">If you apply these configuration files to a package in the form generated by the sequencer, the packages will have the same default settings that came from their manifest.</span></span> <span data-ttu-id="3c395-118">Таким образом, вы получите шаблон для определенного пакета, чтобы приступить к работе, если нужно изменить любое из значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c395-118">This provides you with a package-specific template to get started if any of the defaults must be changed.</span></span>

<span data-ttu-id="3c395-119">**Примечание**  Приведенные ниже сведения можно использовать только для настройки файлов конфигурации секвенсоров, чтобы настроить пакеты для обеспечения конкретных требований пользователей или групп.</span><span class="sxs-lookup"><span data-stu-id="3c395-119">**Note** The following information can only be used to modify sequencer generated configuration files to customize packages to meet specific user or group requirements.</span></span>

 

### <span data-ttu-id="3c395-120">Содержимое файла динамической конфигурации</span><span class="sxs-lookup"><span data-stu-id="3c395-120">Dynamic Configuration file contents</span></span>

<span data-ttu-id="3c395-121">Все добавления, удаления и обновления в файлах конфигурации должны быть связаны со значениями по умолчанию, заданными в манифесте пакета.</span><span class="sxs-lookup"><span data-stu-id="3c395-121">All of the additions, deletions, and updates in the configuration files need to be made in relation to the default values specified by the package's manifest information.</span></span> <span data-ttu-id="3c395-122">Ознакомьтесь с приведенной ниже таблицей.</span><span class="sxs-lookup"><span data-stu-id="3c395-122">Review the following table:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c395-123">Файл Configuration. XML пользователя</span><span class="sxs-lookup"><span data-stu-id="3c395-123">User Configuration .xml file</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c395-124">XML-файл конфигурации развертывания</span><span class="sxs-lookup"><span data-stu-id="3c395-124">Deployment Configuration .xml file</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c395-125">Манифест пакета</span><span class="sxs-lookup"><span data-stu-id="3c395-125">Package Manifest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3c395-126">В предыдущей таблице показано, как будут прочитаны файлы.</span><span class="sxs-lookup"><span data-stu-id="3c395-126">The previous table represents how the files will be read.</span></span> <span data-ttu-id="3c395-127">Первый элемент показывает, что будет считаться последним, поэтому его содержимое имеет приоритет.</span><span class="sxs-lookup"><span data-stu-id="3c395-127">The first entry represents what will be read last, therefore, its content takes precedence.</span></span> <span data-ttu-id="3c395-128">Таким образом, все пакеты по сути содержат параметры по умолчанию из манифеста пакета.</span><span class="sxs-lookup"><span data-stu-id="3c395-128">Therefore, all packages inherently contain and provide default settings from the package manifest.</span></span> <span data-ttu-id="3c395-129">Если применяется XML-файл конфигурации развертывания с настроенными параметрами, он будет переопределять параметры манифеста пакета по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c395-129">If a deployment configuration .xml file with customized settings is applied, it will override the package manifest defaults.</span></span> <span data-ttu-id="3c395-130">Если файл Configuration. XML с настроенными параметрами применяется до этого, он переопределит конфигурацию развертывания и параметры манифеста пакета по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c395-130">If a user configuration .xml file with customized settings is applied prior to that, it will override both the deployment configuration and the package manifest defaults.</span></span>

<span data-ttu-id="3c395-131">В списке ниже приведены дополнительные сведения о двух типах файлов.</span><span class="sxs-lookup"><span data-stu-id="3c395-131">The following list displays more information about the two file types:</span></span>

-   <span data-ttu-id="3c395-132">**Файл конфигурации пользователя (UserConfig)** — позволяет указать или изменить пользовательские параметры для пакета.</span><span class="sxs-lookup"><span data-stu-id="3c395-132">**User Configuration File (UserConfig)** – Allows you to specify or modify custom settings for a package.</span></span> <span data-ttu-id="3c395-133">Эти параметры будут применяться к определенному пользователю при развертывании пакета на компьютере, на котором запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3c395-133">These settings will be applied for a specific user when the package is deployed to a computer running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="3c395-134">**Файл конфигурации развертывания (DEPLOYMENTCONFIG)** — позволяет указать или изменить параметры пакета по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c395-134">**Deployment Configuration File (DeploymentConfig)** – Allows you to specify or modify the default settings for a package.</span></span> <span data-ttu-id="3c395-135">Эти параметры будут применяться ко всем пользователям при развертывании пакета на компьютере с клиентским приложением App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3c395-135">These settings will be applied for all users when a package is deployed to a computer running the App-V 5.0 client.</span></span>

<span data-ttu-id="3c395-136">Чтобы настроить параметры для пакета для определенного набора пользователей на компьютере или внести изменения, которые будут применяться к локальным расположениям пользователей, таким как HKCU, следует использовать файл UserConfig.</span><span class="sxs-lookup"><span data-stu-id="3c395-136">To customize the settings for a package for a specific set of users on a computer or to make changes that will be applied to local user locations such as HKCU, the UserConfig file should be used.</span></span> <span data-ttu-id="3c395-137">Чтобы изменить параметры пакета по умолчанию для всех пользователей на компьютере или внести изменения, которые будут применяться к глобальным расположениям, например HKEY \ _LOCAL \ _MACHINE и папке All Users, следует использовать файл DeploymentConfig.</span><span class="sxs-lookup"><span data-stu-id="3c395-137">To modify the default settings of a package for all users on a machine or to make changes that will be applied to global locations such as HKEY\_LOCAL\_MACHINE and the all users folder, the DeploymentConfig file should be used.</span></span>

<span data-ttu-id="3c395-138">Файл UserConfig предоставляет параметры конфигурации, которые можно применять для одного пользователя, не затрагивая других пользователей на клиенте:</span><span class="sxs-lookup"><span data-stu-id="3c395-138">The UserConfig file provides configuration settings that can be applied to a single user without affecting any other users on a client:</span></span>

-   <span data-ttu-id="3c395-139">Расширения, которые будут интегрированы в собственную систему на каждого пользователя:-сочетания, типы файлов, протоколы URL-адресов, AppPaths, клиенты и COM</span><span class="sxs-lookup"><span data-stu-id="3c395-139">Extensions that will be integrated into the native system per user:- shortcuts, File-Type associations, URL Protocols, AppPaths, Software Clients and COM</span></span>

-   <span data-ttu-id="3c395-140">Виртуальные подсистемы: объекты приложения, переменные среды, изменения в реестре, службы и шрифты</span><span class="sxs-lookup"><span data-stu-id="3c395-140">Virtual Subsystems:- Application Objects, Environment variables, Registry modifications, Services and Fonts</span></span>

-   <span data-ttu-id="3c395-141">Сценарии (только для контекста пользователя)</span><span class="sxs-lookup"><span data-stu-id="3c395-141">Scripts (User context only)</span></span>

-   <span data-ttu-id="3c395-142">Управление полномочиями (для управления сосуществованием пакета с помощью App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="3c395-142">Managing Authority (for controlling co-existence of package with App-V 4.6)</span></span>

<span data-ttu-id="3c395-143">Файл DeploymentConfig предоставляет параметры конфигурации в двух разделах, один из которых относится к контексту компьютера, а другой — к контексту пользователя, который предоставляет те же возможности, которые указаны в списке UserConfig выше:</span><span class="sxs-lookup"><span data-stu-id="3c395-143">The DeploymentConfig file provides configuration settings in two sections, one relative to the machine context and one relative to the user context providing the same capabilities listed in the UserConfig list above:</span></span>

-   <span data-ttu-id="3c395-144">Все указанные выше параметры UserConfig</span><span class="sxs-lookup"><span data-stu-id="3c395-144">All UserConfig settings above</span></span>

-   <span data-ttu-id="3c395-145">Расширения, применимые только глобально для всех пользователей</span><span class="sxs-lookup"><span data-stu-id="3c395-145">Extensions that can only be applied globally for all users</span></span>

-   <span data-ttu-id="3c395-146">Виртуальные подсистемы, которые можно настроить для глобальных компьютеров, например Registry</span><span class="sxs-lookup"><span data-stu-id="3c395-146">Virtual Subsystems that can be configured for global machine locations e.g. registry</span></span>

-   <span data-ttu-id="3c395-147">URL-адрес источника продукта</span><span class="sxs-lookup"><span data-stu-id="3c395-147">Product Source URL</span></span>

-   <span data-ttu-id="3c395-148">Сценарии (только для контекста компьютера)</span><span class="sxs-lookup"><span data-stu-id="3c395-148">Scripts (Machine context only)</span></span>

-   <span data-ttu-id="3c395-149">Элементы управления для завершения дочерних процессов</span><span class="sxs-lookup"><span data-stu-id="3c395-149">Controls to Terminate Child Processes</span></span>

### <span data-ttu-id="3c395-150">Структура файла</span><span class="sxs-lookup"><span data-stu-id="3c395-150">File structure</span></span>

<span data-ttu-id="3c395-151">Структура файла динамической конфигурации App-V 5,0 описана в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="3c395-151">The structure of the App-V 5.0 Dynamic Configuration file is explained in the following section.</span></span>

### <span data-ttu-id="3c395-152">Файл динамической конфигурации пользователя</span><span class="sxs-lookup"><span data-stu-id="3c395-152">Dynamic User Configuration file</span></span>

<span data-ttu-id="3c395-153">**Заголовок** — заголовок динамического пользовательского файла конфигурации выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3c395-153">**Header** - the header of a dynamic user configuration file is as follows:</span></span>

<span data-ttu-id="3c395-154">&lt;? XML Version = "1.0" Encoding = "UTF-8"? &gt; &lt; UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="3c395-154">&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

<span data-ttu-id="3c395-155">**PackageId** имеет то же значение, которое существует в файле манифеста.</span><span class="sxs-lookup"><span data-stu-id="3c395-155">The **PackageId** is the same value as exists in the Manifest file.</span></span>

<span data-ttu-id="3c395-156">**Body** — тело файла динамической конфигурации пользователя может включать все точки расширения приложения, определенные в файле манифеста, а также данные для настройки виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="3c395-156">**Body** - the body of the Dynamic User Configuration file can include all the app extension points that are defined in the Manifest file, as well as information to configure virtual applications.</span></span> <span data-ttu-id="3c395-157">В тексте сообщения можно использовать четыре подраздела.</span><span class="sxs-lookup"><span data-stu-id="3c395-157">There are four subsections allowed in the body:</span></span>

1. <span data-ttu-id="3c395-158">**Приложения** — все расширения приложения, которые содержатся в файле манифеста в пакете, НАЗНАЧАЮТся идентификатору приложения, который также определен в файле манифеста.</span><span class="sxs-lookup"><span data-stu-id="3c395-158">**Applications** - All app-extensions that are contained in the Manifest file within a package are assigned with an Application ID, which is also defined in the manifest file.</span></span> <span data-ttu-id="3c395-159">Это позволяет включать или отключать все расширения для данного приложения в пакете.</span><span class="sxs-lookup"><span data-stu-id="3c395-159">This allows you to enable or disable all the extensions for a given application within a package.</span></span> <span data-ttu-id="3c395-160">**Идентификатор приложения** должен существовать в файле манифеста, или он будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="3c395-160">The **Application ID** must exist in the Manifest file or it will be ignored.</span></span>

   <span data-ttu-id="3c395-161">&lt;UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="3c395-161">&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

   <span data-ttu-id="3c395-162">&lt;Приложения&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-162">&lt;Applications&gt;</span></span>

   <span data-ttu-id="3c395-163">&lt;!--В политике не может быть определено новое приложение.</span><span class="sxs-lookup"><span data-stu-id="3c395-163">&lt;!-- No new application can be defined in policy.</span></span> <span data-ttu-id="3c395-164">Клиент службы AppV будет игнорировать любые ИДЕНТИФИКАТОРы приложения, которые также не находятся в файле манифеста--&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-164">AppV Client will ignore any application ID that is not also in the Manifest file --&gt;</span></span>

   <span data-ttu-id="3c395-165">&lt;Приложение ID = "{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled = "false"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-165">&lt;Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false"&gt;</span></span>

   <span data-ttu-id="3c395-166">&lt;/Application&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-166">&lt;/Application&gt;</span></span>

   <span data-ttu-id="3c395-167">&lt;/Applications&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-167">&lt;/Applications&gt;</span></span>

   <span data-ttu-id="3c395-168">…</span><span class="sxs-lookup"><span data-stu-id="3c395-168">…</span></span>

   <span data-ttu-id="3c395-169">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-169">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="3c395-170">**Подсистемы** — AppExtensions и другие подсистемы размещаются как подузлы в &lt; подсистемах &gt; .</span><span class="sxs-lookup"><span data-stu-id="3c395-170">**Subsystems** - AppExtensions and other subsystems are arranged as subnodes under the &lt;Subsystems&gt;:</span></span>

   <span data-ttu-id="3c395-171">&lt;UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="3c395-171">&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

   <span data-ttu-id="3c395-172">&lt;Подсистем&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-172">&lt;Subsystems&gt;</span></span>

   <span data-ttu-id="3c395-173">..</span><span class="sxs-lookup"><span data-stu-id="3c395-173">..</span></span>

   <span data-ttu-id="3c395-174">&lt;/Subsystems&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-174">&lt;/Subsystems&gt;</span></span>

   <span data-ttu-id="3c395-175">..</span><span class="sxs-lookup"><span data-stu-id="3c395-175">..</span></span>

   <span data-ttu-id="3c395-176">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-176">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="3c395-177">Каждая подсистема может быть включена или отключена с помощью атрибута**Enabled**.</span><span class="sxs-lookup"><span data-stu-id="3c395-177">Each subsystem can be enabled/disabled using the “**Enabled**” attribute.</span></span> <span data-ttu-id="3c395-178">Ниже указаны различные подсистемы и примеры использования.</span><span class="sxs-lookup"><span data-stu-id="3c395-178">Below are the various subsystems and usage samples.</span></span>

   **<span data-ttu-id="3c395-179">MIME</span><span class="sxs-lookup"><span data-stu-id="3c395-179">Extensions:</span></span>**

   <span data-ttu-id="3c395-180">Некоторые подсистемы (расширения элементов управления доподсистемой).</span><span class="sxs-lookup"><span data-stu-id="3c395-180">Some subsystems (Extension Subsystems) control Extensions.</span></span> <span data-ttu-id="3c395-181">К этим подсистемам присвоены следующие подсистемы: сочетания клавиш, сопоставления типов файлов, протоколы URL-адресов, AppPaths, клиенты программного обеспечения и COM</span><span class="sxs-lookup"><span data-stu-id="3c395-181">Those subsystems are:- shortcuts, File-Type associations, URL Protocols, AppPaths, Software Clients and COM</span></span>

   <span data-ttu-id="3c395-182">Подсистемы расширения можно включать и отключать независимо от содержимого.</span><span class="sxs-lookup"><span data-stu-id="3c395-182">Extension Subsystems can be enabled and disabled independently of the content.</span></span>  <span data-ttu-id="3c395-183">Таким образом, если включены сочетания клавиш, клиент будет по умолчанию использовать сочетания клавиш, содержащиеся в манифесте.</span><span class="sxs-lookup"><span data-stu-id="3c395-183">Thus if Shortcuts are enabled, The client will use the shortcuts contained within the manifest by default.</span></span> <span data-ttu-id="3c395-184">Каждая подсистема расширения может содержать &lt; узел Extensions &gt; .</span><span class="sxs-lookup"><span data-stu-id="3c395-184">Each Extension Subsystem can contain an &lt;Extensions&gt; node.</span></span> <span data-ttu-id="3c395-185">Если этот дочерний элемент присутствует, клиент будет игнорировать содержимое файла манифеста для этой подсистемы и использовать только содержимое в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3c395-185">If this child element is present, the client will ignore the content in the Manifest file for that subsystem and only use the content in the configuration file.</span></span>

   <span data-ttu-id="3c395-186">Пример использования подсистемы сочетаний клавиш:</span><span class="sxs-lookup"><span data-stu-id="3c395-186">Example using the shortcuts subsystem:</span></span>

   1.  <span data-ttu-id="3c395-187">Если пользователь задали это значение в динамическом файле конфигурации:</span><span class="sxs-lookup"><span data-stu-id="3c395-187">If the user defined this in either the dynamic or deployment config file:</span></span>

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  <span data-ttu-id="3c395-188">Если пользователь задали следующие данные:</span><span class="sxs-lookup"><span data-stu-id="3c395-188">If the user defined only the following:</span></span>

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  <span data-ttu-id="3c395-189">Если пользователь определяет указанные ниже</span><span class="sxs-lookup"><span data-stu-id="3c395-189">If the user defines the following</span></span>

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   <span data-ttu-id="3c395-190">В этом случае все сочетания клавиш в манифесте будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="3c395-190">Then all the shortcuts within the manifest will still be ignored.</span></span> <span data-ttu-id="3c395-191">Сочетания клавиш не будут интегрированы.</span><span class="sxs-lookup"><span data-stu-id="3c395-191">There will be no shortcuts integrated.</span></span>

   <span data-ttu-id="3c395-192">Поддерживаются следующие подсистемы расширения.</span><span class="sxs-lookup"><span data-stu-id="3c395-192">The supported Extension Subsystems are:</span></span>

   <span data-ttu-id="3c395-193">**Сочетания клавиш:** Этот элемент управления определяет сочетания клавиш, которые будут интегрированы в локальную систему.</span><span class="sxs-lookup"><span data-stu-id="3c395-193">**Shortcuts:** This controls shortcuts that will be integrated into the local system.</span></span> <span data-ttu-id="3c395-194">Ниже приведен пример с двумя сочетаниями клавиш:</span><span class="sxs-lookup"><span data-stu-id="3c395-194">Below is a sample with 2 shortcuts:</span></span>

   <span data-ttu-id="3c395-195">&lt;Подсистем&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-195">&lt;Subsystems&gt;</span></span>

   <span data-ttu-id="3c395-196">&lt;Сочетания клавиш включены = "истина"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-196">&lt;Shortcuts Enabled="true"&gt;</span></span>

     <span data-ttu-id="3c395-197">&lt;Расширения&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-197">&lt;Extensions&gt;</span></span>

       &lt;Extension Category="AppV.Shortcut"&gt;

         &lt;Shortcut&gt;

           &lt;File&gt;\[{Common Programs}\]\\Microsoft Contoso\\Microsoft ContosoApp Filler 2010.lnk&lt;/File&gt;

           &lt;Target&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/Target&gt;

           &lt;Icon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\inficon.exe&lt;/Icon&gt;

           &lt;Arguments /&gt;

           &lt;WorkingDirectory /&gt;

           &lt;AppUserModelId&gt;ContosoApp.Filler.3&lt;/AppUserModelId&gt;

           &lt;Description&gt;Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.&lt;/Description&gt;

           &lt;Hotkey&gt;0&lt;/Hotkey&gt;

           &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

           &lt;ApplicationId&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/ApplicationId&gt;

         &lt;/Shortcut&gt;

     <span data-ttu-id="3c395-198">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-198">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="3c395-199">&lt;Extension Category = "AppV. shortcut"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-199">&lt;Extension Category="AppV.Shortcut"&gt;</span></span>

       &lt;Shortcut&gt;

         &lt;File&gt;\[{AppData}\]\\Microsoft\\Contoso\\Recent\\Templates.LNK&lt;/File&gt;

         &lt;Target&gt;\[{AppData}\]\\Microsoft\\Templates&lt;/Target&gt;

         &lt;Icon /&gt;

         &lt;Arguments /&gt;

         &lt;WorkingDirectory /&gt;

         &lt;AppUserModelId /&gt;

         &lt;Description /&gt;

         &lt;Hotkey&gt;0&lt;/Hotkey&gt;

         &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

         &lt;!-- Note the ApplicationId is optional --&gt;

       &lt;/Shortcut&gt;

     <span data-ttu-id="3c395-200">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-200">&lt;/Extension&gt;</span></span>

    <span data-ttu-id="3c395-201">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-201">&lt;/Extensions&gt;</span></span>

   <span data-ttu-id="3c395-202">&lt;/Shortcuts&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-202">&lt;/Shortcuts&gt;</span></span>

   <span data-ttu-id="3c395-203">**Сопоставления типов файлов:** Связывает типы файлов с программами, которые можно открывать по умолчанию, а также настройкой контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="3c395-203">**File-Type Associations:** Associates File-types with programs to open by default as well as setup the context menu.</span></span> <span data-ttu-id="3c395-204">(Типы MIME также можно настроить с помощью этого susbsystem).</span><span class="sxs-lookup"><span data-stu-id="3c395-204">(MIME types can also be setup using this susbsystem).</span></span> <span data-ttu-id="3c395-205">Пример сопоставления типов файлов ниже:</span><span class="sxs-lookup"><span data-stu-id="3c395-205">Sample File-type Association is below:</span></span>

   <span data-ttu-id="3c395-206">&lt;FileTypeAssociations Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-206">&lt;FileTypeAssociations Enabled="true"&gt;</span></span>

   <span data-ttu-id="3c395-207">&lt;Расширения&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-207">&lt;Extensions&gt;</span></span>

     <span data-ttu-id="3c395-208">&lt;Расширение Category = "AppV. FileTypeAssociation"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-208">&lt;Extension Category="AppV.FileTypeAssociation"&gt;</span></span>

       &lt;FileTypeAssociation&gt;

         &lt;FileExtension MimeAssociation="true"&gt;

         &lt;Name&gt;.docm&lt;/Name&gt;

         &lt;ProgId&gt;contosowordpad.DocumentMacroEnabled.12&lt;/ProgId&gt;

         &lt;PerceivedType&gt;document&lt;/PerceivedType&gt;

         &lt;ContentType&gt;application/vnd.ms-contosowordpad.document.macroEnabled.12&lt;/ContentType&gt;

         &lt;OpenWithList&gt;

           &lt;ApplicationName&gt;wincontosowordpad.exe&lt;/ApplicationName&gt;

         &lt;/OpenWithList&gt;

        &lt;OpenWithProgIds&gt;

           &lt;ProgId&gt;contosowordpad.8&lt;/ProgId&gt;

         &lt;/OpenWithProgIds&gt;

         &lt;ShellNew&gt;

           &lt;Command /&gt;

           &lt;DataBinary /&gt;

           &lt;DataText /&gt;

           &lt;FileName /&gt;

           &lt;NullFile&gt;true&lt;/NullFile&gt;

           &lt;ItemName /&gt;

           &lt;IconPath /&gt;

           &lt;MenuText /&gt;

           &lt;Handler /&gt;

         &lt;/ShellNew&gt;

       &lt;/FileExtension&gt;

       &lt;ProgId&gt;

          &lt;Name&gt;contosowordpad.DocumentMacroEnabled.12&lt;/Name&gt;

           &lt;DefaultIcon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\contosowordpadicon.exe,15&lt;/DefaultIcon&gt;

           &lt;Description&gt;Blah Blah Blah&lt;/Description&gt;

           &lt;FriendlyTypeName&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,9182&lt;/FriendlyTypeName&gt;

           &lt;InfoTip&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,1424&lt;/InfoTip&gt;

           &lt;EditFlags&gt;0&lt;/EditFlags&gt;

           &lt;ShellCommands&gt;

             &lt;DefaultCommand&gt;Open&lt;/DefaultCommand&gt;

             &lt;ShellCommand&gt;

                &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

                &lt;Name&gt;Edit&lt;/Name&gt;

                &lt;FriendlyName&gt;&Edit&lt;/FriendlyName&gt;

                &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /vu "%1"&lt;/CommandLine&gt;

             &lt;/ShellCommand&gt;

             &lt;/ShellCommand&gt;

               &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

               &lt;Name&gt;Open&lt;/Name&gt;

               &lt;FriendlyName&gt;&Open&lt;/FriendlyName&gt;

               &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /n "%1"&lt;/CommandLine&gt;

               &lt;DropTargetClassId /&gt;

               &lt;DdeExec&gt;

                 &lt;Application&gt;mscontosowordpad&lt;/Application&gt;

                 &lt;Topic&gt;ShellSystem&lt;/Topic&gt;

                 &lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;

                 &lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;

               &lt;/DdeExec&gt;

             &lt;/ShellCommand&gt;

           &lt;/ShellCommands&gt;

         &lt;/ProgId&gt;

        &lt;/FileTypeAssociation&gt;

      <span data-ttu-id="3c395-209">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-209">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="3c395-210">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-210">&lt;/Extensions&gt;</span></span>

     <span data-ttu-id="3c395-211">&lt;/FileTypeAssociations&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-211">&lt;/FileTypeAssociations&gt;</span></span>

   <span data-ttu-id="3c395-212">**URL-протоколы**: управляет протоколами URL-адресов, которые интегрируются в локальный реестр клиентского компьютера, например "mailto:".</span><span class="sxs-lookup"><span data-stu-id="3c395-212">**URL Protocols**: This controls the URL Protocols that are integrated into the local registry of the client machine e.g. “mailto:”.</span></span>

   <span data-ttu-id="3c395-213">&lt;URLProtocols Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-213">&lt;URLProtocols Enabled="true"&gt;</span></span>

   <span data-ttu-id="3c395-214">&lt;Расширения&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-214">&lt;Extensions&gt;</span></span>

   <span data-ttu-id="3c395-215">&lt;Расширение Category = "AppV. URLProtocol"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-215">&lt;Extension Category="AppV.URLProtocol"&gt;</span></span>

   <span data-ttu-id="3c395-216">&lt;URLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-216">&lt;URLProtocol&gt;</span></span>

     <span data-ttu-id="3c395-217">&lt;Name &gt; mailto &lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-217">&lt;Name&gt;mailto&lt;/Name&gt;</span></span>

     <span data-ttu-id="3c395-218">&lt;ApplicationURLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-218">&lt;ApplicationURLProtocol&gt;</span></span>

     <span data-ttu-id="3c395-219">&lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /defaultIcon&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-219">&lt;DefaultIcon&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403&lt;/DefaultIcon&gt;</span></span>

     <span data-ttu-id="3c395-220">&lt;EditFlags &gt; 2 &lt; /EditFlags&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-220">&lt;EditFlags&gt;2&lt;/EditFlags&gt;</span></span>

     <span data-ttu-id="3c395-221">&lt;Nописание&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-221">&lt;Description /&gt;</span></span>

     <span data-ttu-id="3c395-222">&lt;AppUserModelId&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-222">&lt;AppUserModelId /&gt;</span></span>

     <span data-ttu-id="3c395-223">&lt;FriendlyTypeName /&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-223">&lt;FriendlyTypeName /&gt;</span></span>

     <span data-ttu-id="3c395-224">&lt;Плыв&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-224">&lt;InfoTip /&gt;</span></span>

   <span data-ttu-id="3c395-225">&lt;SourceFilter /&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-225">&lt;SourceFilter /&gt;</span></span>

     <span data-ttu-id="3c395-226">&lt;ShellFolder /&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-226">&lt;ShellFolder /&gt;</span></span>

     <span data-ttu-id="3c395-227">&lt;WebNavigableCLSID /&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-227">&lt;WebNavigableCLSID /&gt;</span></span>

     <span data-ttu-id="3c395-228">&lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-228">&lt;ExplorerFlags&gt;2&lt;/ExplorerFlags&gt;</span></span>

     <span data-ttu-id="3c395-229">&lt;CLSID&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-229">&lt;CLSID /&gt;</span></span>

     <span data-ttu-id="3c395-230">&lt;ShellCommands&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-230">&lt;ShellCommands&gt;</span></span>

     <span data-ttu-id="3c395-231">&lt;DefaultCommand &gt; Open &lt; /DefaultCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-231">&lt;DefaultCommand&gt;open&lt;/DefaultCommand&gt;</span></span>

     <span data-ttu-id="3c395-232">&lt;ShellCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-232">&lt;ShellCommand&gt;</span></span>

     <span data-ttu-id="3c395-233">&lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /applicationId&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-233">&lt;ApplicationId&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationId&gt;</span></span>

     <span data-ttu-id="3c395-234">&lt;Имя &gt; Open &lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-234">&lt;Name&gt;open&lt;/Name&gt;</span></span>

     <span data-ttu-id="3c395-235">&lt;CommandLine &gt; \ [{ProgramFilesX86} \\Microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. Примечание/m "%1" &lt; /commandline&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-235">&lt;CommandLine&gt;\[{ProgramFilesX86}\\Microsoft Contoso\\Contoso\\contosomail.EXE" -c OEP.Note /m "%1"&lt;/CommandLine&gt;</span></span>

     <span data-ttu-id="3c395-236">&lt;DropTargetClassId /&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-236">&lt;DropTargetClassId /&gt;</span></span>

     <span data-ttu-id="3c395-237">&lt;Понятно&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-237">&lt;FriendlyName /&gt;</span></span>

     <span data-ttu-id="3c395-238">&lt;Расширенная &gt; 0 &lt; /Extended&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-238">&lt;Extended&gt;0&lt;/Extended&gt;</span></span>

     <span data-ttu-id="3c395-239">&lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-239">&lt;LegacyDisable&gt;0&lt;/LegacyDisable&gt;</span></span>

     <span data-ttu-id="3c395-240">&lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-240">&lt;SuppressionPolicy&gt;2&lt;/SuppressionPolicy&gt;</span></span>

      <span data-ttu-id="3c395-241">&lt;DdeExec&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-241">&lt;DdeExec&gt;</span></span>

     <span data-ttu-id="3c395-242">&lt;NoActivateHandler /&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-242">&lt;NoActivateHandler /&gt;</span></span>

     <span data-ttu-id="3c395-243">&lt;Приложение &gt; contosomail &lt; /Application&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-243">&lt;Application&gt;contosomail&lt;/Application&gt;</span></span>

     <span data-ttu-id="3c395-244">&lt;Тема &gt; ShellSystem &lt; /Topic&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-244">&lt;Topic&gt;ShellSystem&lt;/Topic&gt;</span></span>

     <span data-ttu-id="3c395-245">&lt;IfExec &gt; \ [SHELLNOOP \] &lt; /IfExec&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-245">&lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;</span></span>

     <span data-ttu-id="3c395-246">&lt;DdeCommand &gt; \ [SetForeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-246">&lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;</span></span>

     <span data-ttu-id="3c395-247">&lt;/DdeExec&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-247">&lt;/DdeExec&gt;</span></span>

     <span data-ttu-id="3c395-248">&lt;/ShellCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-248">&lt;/ShellCommand&gt;</span></span>

     <span data-ttu-id="3c395-249">&lt;/ShellCommands&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-249">&lt;/ShellCommands&gt;</span></span>

     <span data-ttu-id="3c395-250">&lt;/ApplicationURLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-250">&lt;/ApplicationURLProtocol&gt;</span></span>

     <span data-ttu-id="3c395-251">&lt;/URLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-251">&lt;/URLProtocol&gt;</span></span>

     <span data-ttu-id="3c395-252">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-252">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="3c395-253">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-253">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="3c395-254">&lt;/URLProtocols&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-254">&lt;/URLProtocols&gt;</span></span>

   <span data-ttu-id="3c395-255">**Клиенты программного обеспечения**: позволяет приложению регистрироваться как клиент электронной почты, средство чтения новостей, проигрыватель мультимедиа и делает приложение видимым в пользовательском интерфейсе "Настройка доступа к программам и параметров по умолчанию для компьютера".</span><span class="sxs-lookup"><span data-stu-id="3c395-255">**Software Clients**: Allows the app to register as an Email client, news reader, media player and makes the app visible in the Set Program Access and Computer Defaults UI.</span></span> <span data-ttu-id="3c395-256">В большинстве случаев вам нужно только включить и отключить его.</span><span class="sxs-lookup"><span data-stu-id="3c395-256">In most cases you should only need to enable and disable it.</span></span> <span data-ttu-id="3c395-257">Кроме того, есть элемент управления для включения и отключения клиента электронной почты в специальном варианте, если вы хотите, чтобы другие клиенты по-прежнему были включены только для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="3c395-257">There is also a control to enable and disable the email client specifically if you want the other clients still enabled except for that client.</span></span>

   <span data-ttu-id="3c395-258">&lt;SoftwareClients Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-258">&lt;SoftwareClients Enabled="true"&gt;</span></span>

     <span data-ttu-id="3c395-259">&lt;ClientConfiguration EmailEnabled = "ложь"/&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-259">&lt;ClientConfiguration EmailEnabled="false" /&gt;</span></span>

   <span data-ttu-id="3c395-260">&lt;/SoftwareClients&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-260">&lt;/SoftwareClients&gt;</span></span>

   <span data-ttu-id="3c395-261">AppPaths: — Если приложение, например contoso.exe зарегистрировано с именем AppPath "MyApp", оно позволяет ввести "MyApp" в меню "выполнить", и оно откроется contoso.exe.</span><span class="sxs-lookup"><span data-stu-id="3c395-261">AppPaths:- If an application for example contoso.exe is registered with an apppath name of “myapp”, it allows you type “myapp” under the run menu and it will open contoso.exe.</span></span>

   <span data-ttu-id="3c395-262">&lt;AppPaths Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-262">&lt;AppPaths Enabled="true"&gt;</span></span>

   <span data-ttu-id="3c395-263">&lt;Расширения&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-263">&lt;Extensions&gt;</span></span>

   <span data-ttu-id="3c395-264">&lt;Расширение Category = "AppV. AppPath"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-264">&lt;Extension Category="AppV.AppPath"&gt;</span></span>

   <span data-ttu-id="3c395-265">&lt;AppPath&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-265">&lt;AppPath&gt;</span></span>

     <span data-ttu-id="3c395-266">&lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /applicationId&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-266">&lt;ApplicationId&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationId&gt;</span></span>

     <span data-ttu-id="3c395-267">&lt;Name &gt;contosomail.exe&lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-267">&lt;Name&gt;contosomail.exe&lt;/Name&gt;</span></span>

     <span data-ttu-id="3c395-268">&lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationPath&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-268">&lt;ApplicationPath&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationPath&gt;</span></span>

     <span data-ttu-id="3c395-269">&lt;PATHEnvironmentVariablePrefix /&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-269">&lt;PATHEnvironmentVariablePrefix /&gt;</span></span>

     <span data-ttu-id="3c395-270">&lt;CanAcceptUrl &gt; ложь &lt; /CanAcceptUrl&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-270">&lt;CanAcceptUrl&gt;false&lt;/CanAcceptUrl&gt;</span></span>

     <span data-ttu-id="3c395-271">&lt;SaveUrl /&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-271">&lt;SaveUrl /&gt;</span></span>

   <span data-ttu-id="3c395-272">&lt;/AppPath&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-272">&lt;/AppPath&gt;</span></span>

   <span data-ttu-id="3c395-273">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-273">&lt;/Extension&gt;</span></span>

   <span data-ttu-id="3c395-274">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-274">&lt;/Extensions&gt;</span></span>

   <span data-ttu-id="3c395-275">&lt;/AppPaths&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-275">&lt;/AppPaths&gt;</span></span>

   <span data-ttu-id="3c395-276">**Com**: позволяет приложению регистрировать локальные COM-серверы.</span><span class="sxs-lookup"><span data-stu-id="3c395-276">**COM**: Allows an Application register Local COM servers.</span></span> <span data-ttu-id="3c395-277">Режим может быть интегрированным, изолированным или отключенным.</span><span class="sxs-lookup"><span data-stu-id="3c395-277">Mode can be Integration, Isolated or Off.</span></span> <span data-ttu-id="3c395-278">Когда Isol.</span><span class="sxs-lookup"><span data-stu-id="3c395-278">When Isol.</span></span>

   <span data-ttu-id="3c395-279">&lt;Режим COM = "изолированный"/&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-279">&lt;COM Mode="Isolated"/&gt;</span></span>

   <span data-ttu-id="3c395-280">**Другие параметры**:</span><span class="sxs-lookup"><span data-stu-id="3c395-280">**Other Settings**:</span></span>

   <span data-ttu-id="3c395-281">Помимо расширений, другие подсистемы можно включать и отключать и изменять.</span><span class="sxs-lookup"><span data-stu-id="3c395-281">In addition to Extensions, other subsystems can be enabled/disabled and edited:</span></span>

   <span data-ttu-id="3c395-282">**Виртуальные объекты ядра**:</span><span class="sxs-lookup"><span data-stu-id="3c395-282">**Virtual Kernel Objects**:</span></span>

   <span data-ttu-id="3c395-283">&lt;Объекты включены = "ложь"/&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-283">&lt;Objects Enabled="false" /&gt;</span></span>

   <span data-ttu-id="3c395-284">**Виртуальный реестр**: используется, если вы хотите настроить реестр в виртуальном реестре в HKCU</span><span class="sxs-lookup"><span data-stu-id="3c395-284">**Virtual Registry**: Used if you want to set a registry in the Virtual Registry within HKCU</span></span>

   <span data-ttu-id="3c395-285">&lt;Параметр Registry Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-285">&lt;Registry Enabled="true"&gt;</span></span>

   <span data-ttu-id="3c395-286">&lt;Включить&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-286">&lt;Include&gt;</span></span>

   <span data-ttu-id="3c395-287">&lt;Key путь = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-287">&lt;Key Path="\\REGISTRY\\USER\\\[{AppVCurrentUserSID}\]\\Software\\ABC"&gt;</span></span>

   <span data-ttu-id="3c395-288">&lt;Тип значения = "REG \ _SZ" Name = "Bar" Data = "NewValue"/&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-288">&lt;Value Type="REG\_SZ" Name="Bar" Data="NewValue" /&gt;</span></span>

    <span data-ttu-id="3c395-289">&lt;/Key&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-289">&lt;/Key&gt;</span></span>

     <span data-ttu-id="3c395-290">&lt;Key путь = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-290">&lt;Key Path="\\REGISTRY\\USER\\\[{AppVCurrentUserSID}\]\\Software\\EmptyKey" /&gt;</span></span>

    <span data-ttu-id="3c395-291">&lt;/Include&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-291">&lt;/Include&gt;</span></span>

   <span data-ttu-id="3c395-292">&lt;Удаление&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-292">&lt;Delete&gt;</span></span>

     <span data-ttu-id="3c395-293">&lt;/Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-293">&lt;/Registry&gt;</span></span>

   **<span data-ttu-id="3c395-294">Виртуальная файловая система</span><span class="sxs-lookup"><span data-stu-id="3c395-294">Virtual File System</span></span>**

         &lt;FileSystem Enabled="true" /&gt;

   **<span data-ttu-id="3c395-295">Виртуальные шрифты</span><span class="sxs-lookup"><span data-stu-id="3c395-295">Virtual Fonts</span></span>**

         &lt;Fonts Enabled="false" /&gt;

   **<span data-ttu-id="3c395-296">Переменные виртуальных сред</span><span class="sxs-lookup"><span data-stu-id="3c395-296">Virtual Environment Variables</span></span>**

   <span data-ttu-id="3c395-297">&lt;EnvironmentVariables Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-297">&lt;EnvironmentVariables Enabled="true"&gt;</span></span>

   <span data-ttu-id="3c395-298">&lt;Включить&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-298">&lt;Include&gt;</span></span>

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **<span data-ttu-id="3c395-299">Виртуальные службы</span><span class="sxs-lookup"><span data-stu-id="3c395-299">Virtual services</span></span>**

         &lt;Services Enabled="false" /&gt;

3. <span data-ttu-id="3c395-300">**UserScripts** — сценарии можно использовать для настройки или изменения виртуальной среды, а также для выполнения сценариев во время развертывания или удаления, перед выполнением приложения, а также для "очистки" среды после завершения работы приложения.</span><span class="sxs-lookup"><span data-stu-id="3c395-300">**UserScripts** – Scripts can be used to setup or alter the virtual environment as well as execute scripts at time of deployment or removal, before an application executes, or they can be used to “clean up” the environment after the application terminates.</span></span> <span data-ttu-id="3c395-301">Составьте ссылку на пример файла пользовательской конфигурации, выводимым секвенсором, чтобы просмотреть пример сценария.</span><span class="sxs-lookup"><span data-stu-id="3c395-301">Please reference a sample User configuration file that is output by the sequencer to see a sample script.</span></span> <span data-ttu-id="3c395-302">В разделе "сценарии" ниже приведены дополнительные сведения о различных триггерах, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="3c395-302">The Scripts section below provides more information on the various triggers that can be used.</span></span>

4. <span data-ttu-id="3c395-303">**ManagingAuthority** — можно использовать в том случае, если на одном и том же компьютере установлены две версии пакета, один из которых развернут в App-v 4,6, а другой — на App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="3c395-303">**ManagingAuthority** – Can be used when 2 versions of your package are co-existing on the same machine, one deployed to App-V 4.6 and the other deployed on App-V 5.0.</span></span> <span data-ttu-id="3c395-304">Чтобы разрешить приложению App-V vNext дополнительные точки расширения App-V 4,6 для именованного пакета, введите в файл UserConfig следующие элементы (где PackageName — идентификатор GUID пакета в App-V 4,6:</span><span class="sxs-lookup"><span data-stu-id="3c395-304">To Allow App-V vNext to take over App-V 4.6 extension points for the named package enter the following in the UserConfig file (where PackageName is the Package GUID in App-V 4.6:</span></span>

   <span data-ttu-id="3c395-305">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = "032630c0-b8e2-417c-acef-76fc5297fe81"/&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-305">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" /&gt;</span></span>

### <span data-ttu-id="3c395-306">Файл динамической конфигурации развертывания</span><span class="sxs-lookup"><span data-stu-id="3c395-306">Dynamic Deployment Configuration file</span></span>

<span data-ttu-id="3c395-307">**Заголовок** — заголовок файла конфигурации развертывания выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3c395-307">**Header** - The header of a Deployment Configuration file is as follows:</span></span>

<span data-ttu-id="3c395-308">&lt;? XML Version = "1.0" Encoding = "UTF-8"? &gt; &lt; DeploymentConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="3c395-308">&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;DeploymentConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt>;</span></span>

<span data-ttu-id="3c395-309">**PackageId** имеет то же значение, которое существует в файле манифеста.</span><span class="sxs-lookup"><span data-stu-id="3c395-309">The **PackageId** is the same value as exists in the manifest file.</span></span>

<span data-ttu-id="3c395-310">**Body** — тело файла конфигурации развертывания включает два раздела:</span><span class="sxs-lookup"><span data-stu-id="3c395-310">**Body** - The body of the deployment configuration file includes two sections:</span></span>

-   <span data-ttu-id="3c395-311">Раздел "Конфигурация пользователя" — допускает то же содержимое, что и файл конфигурации пользователя, описанный в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="3c395-311">User Configuration section –allows the same content as the User Configuration file described in the previous section.</span></span> <span data-ttu-id="3c395-312">Когда пакет публикуется для пользователя, любые параметры конфигурации appextensions в этом разделе будут переопределять соответствующие параметры в манифесте пакета, если не указан также файл конфигурации пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c395-312">When the package is published to a user, any appextensions configuration settings in this section will override corresponding settings in the Manifest within the package unless a user configuration file is also provided.</span></span> <span data-ttu-id="3c395-313">Если указан также файл UserConfig, он будет использоваться вместо параметров пользователя в файле конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="3c395-313">If a UserConfig file is also provided, it will be used instead of the User settings in the deployment configuration file.</span></span> <span data-ttu-id="3c395-314">Если пакет опубликован глобально, в сочетании с манифестом будет использоваться только содержимое файла конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="3c395-314">If the package is published globally, then only the contents of the deployment configuration file will be used in combination with the manifest.</span></span>

-   <span data-ttu-id="3c395-315">Раздел "Конфигурация компьютера" — содержат данные, которые можно настроить только для всего компьютера, а не для определенного пользователя на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3c395-315">Machine Configuration section–contains information that can be configured only for an entire machine, not for a specific user on the machine.</span></span> <span data-ttu-id="3c395-316">Например, Раздел HKEY \ _LOCAL \ _MACHINE разделов реестра в VFS.</span><span class="sxs-lookup"><span data-stu-id="3c395-316">For example, HKEY\_LOCAL\_MACHINE registry keys in the VFS.</span></span>

<span data-ttu-id="3c395-317">&lt;DeploymentConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="3c395-317">&lt;DeploymentConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt>;</span></span>

<span data-ttu-id="3c395-318">&lt;UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-318">&lt;UserConfiguration&gt;</span></span>

  <span data-ttu-id="3c395-319">..</span><span class="sxs-lookup"><span data-stu-id="3c395-319">..</span></span>

<span data-ttu-id="3c395-320">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-320">&lt;/UserConfiguration&gt;</span></span>

<span data-ttu-id="3c395-321">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-321">&lt;MachineConfiguration&gt;</span></span>

<span data-ttu-id="3c395-322">..</span><span class="sxs-lookup"><span data-stu-id="3c395-322">..</span></span>

<span data-ttu-id="3c395-323">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-323">&lt;/MachineConfiguration&gt;</span></span>

<span data-ttu-id="3c395-324">..</span><span class="sxs-lookup"><span data-stu-id="3c395-324">..</span></span>

<span data-ttu-id="3c395-325">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-325">&lt;/MachineConfiguration&gt;</span></span>

<span data-ttu-id="3c395-326">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-326">&lt;/DeploymentConfiguration&gt;</span></span>

<span data-ttu-id="3c395-327">**Конфигурация пользователя** — используйте предыдущий раздел **файла динамической конфигурации пользователя** для получения сведений о параметрах, которые содержатся в разделе "Конфигурация пользователя" файла конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="3c395-327">**User Configuration** - use the previous **Dynamic User Configuration file** section for information on settings that are provided in the user configuration section of the Deployment Configuration file.</span></span>

<span data-ttu-id="3c395-328">Конфигурация компьютера: раздел "Конфигурация компьютера" файла конфигурации развертывания используется для настройки сведений, которые можно задать только для всего компьютера, а не для определенного пользователя на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3c395-328">Machine Configuration - the Machine configuration section of the Deployment Configuration File is used to configure information that can be set only for an entire machine, not for a specific user on the computer.</span></span> <span data-ttu-id="3c395-329">Например, Раздел HKEY \ _LOCAL \ _MACHINE разделы реестра в виртуальном реестре.</span><span class="sxs-lookup"><span data-stu-id="3c395-329">For example, HKEY\_LOCAL\_MACHINE registry keys in the Virtual Registry.</span></span> <span data-ttu-id="3c395-330">Для этого элемента разрешены четыре подраздела.</span><span class="sxs-lookup"><span data-stu-id="3c395-330">There are four subsections allowed in under this element</span></span>

1.  <span data-ttu-id="3c395-331">**Подсистемы** — AppExtensions и другие подсистемы размещаются как подузлы в &lt; подсистемах &gt; .</span><span class="sxs-lookup"><span data-stu-id="3c395-331">**Subsystems** - AppExtensions and other subsystems are arranged as subnodes under &lt;Subsystems&gt;:</span></span>

    <span data-ttu-id="3c395-332">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-332">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="3c395-333">&lt;Подсистем&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-333">&lt;Subsystems&gt;</span></span>

      <span data-ttu-id="3c395-334">..</span><span class="sxs-lookup"><span data-stu-id="3c395-334">..</span></span>

      <span data-ttu-id="3c395-335">&lt;/Subsystems&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-335">&lt;/Subsystems&gt;</span></span>

    <span data-ttu-id="3c395-336">..</span><span class="sxs-lookup"><span data-stu-id="3c395-336">..</span></span>

    <span data-ttu-id="3c395-337">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-337">&lt;/MachineConfiguration&gt;</span></span>

    <span data-ttu-id="3c395-338">В следующем разделе показаны различные подсистемы и примеры использования.</span><span class="sxs-lookup"><span data-stu-id="3c395-338">The following section displays the various subsystems and usage samples.</span></span>

    <span data-ttu-id="3c395-339">**Расширениями**:</span><span class="sxs-lookup"><span data-stu-id="3c395-339">**Extensions**:</span></span>

    <span data-ttu-id="3c395-340">Некоторые подсистемы (расширения подсистем), которые могут применяться только ко всем пользователям.</span><span class="sxs-lookup"><span data-stu-id="3c395-340">Some subsystems (Extension Subsystems) control Extensions which can only apply to all users.</span></span> <span data-ttu-id="3c395-341">Подсистема — это возможности приложения.</span><span class="sxs-lookup"><span data-stu-id="3c395-341">The subsystem is application capabilities.</span></span> <span data-ttu-id="3c395-342">Так как это применимо только для всех пользователей, пакет должен быть опубликован глобально для интеграции этого типа расширений в локальную систему.</span><span class="sxs-lookup"><span data-stu-id="3c395-342">Because this can only apply to all users, the package must be published globally in order for this type of extension to be integrated into the local system.</span></span> <span data-ttu-id="3c395-343">Те же правила для элементов управления и параметров, применимые к расширениям в конфигурации пользователя, также применяются к параметрам в разделе MachineConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3c395-343">The same rules for controls and settings that apply to the Extensions in the User Configuration also apply to those in the MachineConfiguration section.</span></span>

    <span data-ttu-id="3c395-344">**Возможности приложения**: используется программами по умолчанию в интерфейсе операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="3c395-344">**Application Capabilities**: Used by default programs in windows operating system Interface.</span></span> <span data-ttu-id="3c395-345">Позволяет приложению регистрироваться так, как если бы можно было открывать определенные расширения файлов, как это происходит при открытии определенных типов MIME Windows в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="3c395-345">Allows an application to register itself as capable of opening certain file extensions, as a contender for the start menu internet browser slot, as capable of opening certain windows MIME types.</span></span><span data-ttu-id="3c395-346">Это расширение также делает виртуальное приложение видимым в пользовательском интерфейсе "Настройка программ по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="3c395-346"> This extension also makes the virtual application visible in the Set Default Programs UI.:</span></span>

    <span data-ttu-id="3c395-347">&lt;ApplicationCapabilities Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-347">&lt;ApplicationCapabilities Enabled="true"&gt;</span></span>

      <span data-ttu-id="3c395-348">&lt;Расширения&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-348">&lt;Extensions&gt;</span></span>

       <span data-ttu-id="3c395-349">&lt;Расширение Category = "AppV. ApplicationCapabilities"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-349">&lt;Extension Category="AppV.ApplicationCapabilities"&gt;</span></span>

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       <span data-ttu-id="3c395-350">&lt;CapabilityGroup&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-350">&lt;CapabilityGroup&gt;</span></span>

        &lt;Capabilities&gt;

         &lt;Name&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12345&lt;/Name&gt;

         &lt;Description&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12346&lt;/Description&gt;

         &lt;Hidden&gt;0&lt;/Hidden&gt;

         &lt;EMailSoftwareClient&gt;Lit View E-Mail Client&lt;/EMailSoftwareClient&gt;

         &lt;FileAssociationList&gt;

          &lt;FileAssociation Extension=".htm" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".html" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".shtml" ProgID="LitViewHTML" /&gt;

         &lt;/FileAssociationList&gt;

         &lt;MIMEAssociationList&gt;

          &lt;MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" /&gt;

          &lt;MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" /&gt;

         &lt;/MIMEAssociationList&gt;

        &lt;URLAssociationList&gt;

          &lt;URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" /&gt;

         &lt;/URLAssociationList&gt;

         &lt;/Capabilities&gt;

      <span data-ttu-id="3c395-351">&lt;/CapabilityGroup&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-351">&lt;/CapabilityGroup&gt;</span></span>

       <span data-ttu-id="3c395-352">&lt;/ApplicationCapabilities&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-352">&lt;/ApplicationCapabilities&gt;</span></span>

      <span data-ttu-id="3c395-353">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-353">&lt;/Extension&gt;</span></span>

    <span data-ttu-id="3c395-354">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-354">&lt;/Extensions&gt;</span></span>

    <span data-ttu-id="3c395-355">&lt;/ApplicationCapabilities&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-355">&lt;/ApplicationCapabilities&gt;</span></span>

    <span data-ttu-id="3c395-356">**Другие параметры**:</span><span class="sxs-lookup"><span data-stu-id="3c395-356">**Other Settings**:</span></span>

    <span data-ttu-id="3c395-357">В дополнение к расширениям можно редактировать и другие подсистемы:</span><span class="sxs-lookup"><span data-stu-id="3c395-357">In addition to Extensions, other subsystems can be edited:</span></span>

    <span data-ttu-id="3c395-358">**Виртуальный реестр для всего компьютера**: используется, если вы хотите установить раздел реестра в виртуальном реестре в HKEY \ _Local \ _Machine</span><span class="sxs-lookup"><span data-stu-id="3c395-358">**Machine Wide Virtual Registry**: Used when you want to set a registry key in the virtual registry within HKEY\_Local\_Machine</span></span>

    <span data-ttu-id="3c395-359">&lt;Реестр&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-359">&lt;Registry&gt;</span></span>

    <span data-ttu-id="3c395-360">&lt;Включить&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-360">&lt;Include&gt;</span></span>

      <span data-ttu-id="3c395-361">&lt;Key Path = "\\REGISTRY\\Machine\\Software\\ABC"&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-361">&lt;Key Path="\\REGISTRY\\Machine\\Software\\ABC"&gt;</span></span>

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       <span data-ttu-id="3c395-362">&lt;/Key&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-362">&lt;/Key&gt;</span></span>

      <span data-ttu-id="3c395-363">&lt;Key Path = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-363">&lt;Key Path="\\REGISTRY\\Machine\\Software\\EmptyKey" /&gt;</span></span>

     <span data-ttu-id="3c395-364">&lt;/Include&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-364">&lt;/Include&gt;</span></span>

    <span data-ttu-id="3c395-365">&lt;Удаление&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-365">&lt;Delete&gt;</span></span>

    <span data-ttu-id="3c395-366">&lt;/Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-366">&lt;/Registry&gt;</span></span>

    **<span data-ttu-id="3c395-367">Виртуальные объекты ядра на уровне компьютера</span><span class="sxs-lookup"><span data-stu-id="3c395-367">Machine Wide Virtual Kernel Objects</span></span>**

    <span data-ttu-id="3c395-368">&lt;Object&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-368">&lt;Objects&gt;</span></span>

    <span data-ttu-id="3c395-369">&lt;NotIsolate&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-369">&lt;NotIsolate&gt;</span></span>

       <span data-ttu-id="3c395-370">&lt;Object Name = "testObject"/&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-370">&lt;Object Name="testObject" /&gt;</span></span>

     <span data-ttu-id="3c395-371">&lt;/NotIsolate&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-371">&lt;/NotIsolate&gt;</span></span>

    <span data-ttu-id="3c395-372">&lt;/Objects&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-372">&lt;/Objects&gt;</span></span>

2.  <span data-ttu-id="3c395-373">**ProductSourceURLOptOut**: указывает, можно ли глобально изменить URL-адрес пакета с помощью PackageSourceRoot (для поддержки сценариев филиалов).</span><span class="sxs-lookup"><span data-stu-id="3c395-373">**ProductSourceURLOptOut**: Indicates whether the URL for the package can be modified globally through PackageSourceRoot (to support branch office scenarios).</span></span> <span data-ttu-id="3c395-374">Значение по умолчанию — false, и изменения параметров вступят в силу при следующем запуске.</span><span class="sxs-lookup"><span data-stu-id="3c395-374">Default is false and the setting change takes effect on the next launch.</span></span>  

    <span data-ttu-id="3c395-375">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-375">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="3c395-376">..</span><span class="sxs-lookup"><span data-stu-id="3c395-376">..</span></span> 

      <span data-ttu-id="3c395-377">&lt;ProductSourceURLOptOut Enabled = "true"/&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-377">&lt;ProductSourceURLOptOut Enabled="true" /&gt;</span></span>

      <span data-ttu-id="3c395-378">..</span><span class="sxs-lookup"><span data-stu-id="3c395-378">..</span></span>

    <span data-ttu-id="3c395-379">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-379">&lt;/MachineConfiguration&gt;</span></span>

3.  <span data-ttu-id="3c395-380">**MachineScripts** — пакет можно настроить для выполнения сценариев во время развертывания, публикации или удаления.</span><span class="sxs-lookup"><span data-stu-id="3c395-380">**MachineScripts** – Package can be configured to execute scripts at time of deployment, publishing or removal.</span></span> <span data-ttu-id="3c395-381">Составьте ссылку на пример файла конфигурации развертывания, который создается секвенсором, чтобы просмотреть пример сценария.</span><span class="sxs-lookup"><span data-stu-id="3c395-381">Please reference a sample deployment configuration file that is generated by the sequencer to see a sample script.</span></span> <span data-ttu-id="3c395-382">В разделе "сценарии" приведены дополнительные сведения о различных триггерах, которые можно использовать</span><span class="sxs-lookup"><span data-stu-id="3c395-382">The Scripts section below provides more information on the various triggers that can be used</span></span>

4.  <span data-ttu-id="3c395-383">**TerminateChildProcess**: — можно указать исполняемый файл приложения, дочерние процессы которого будут завершаться после завершения процесса exe-файла приложения.</span><span class="sxs-lookup"><span data-stu-id="3c395-383">**TerminateChildProcess**:- An application executable can be specified, whose child processes will be terminated when the application exe process is terminated.</span></span>

    <span data-ttu-id="3c395-384">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-384">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="3c395-385">..</span><span class="sxs-lookup"><span data-stu-id="3c395-385">..</span></span>   

      <span data-ttu-id="3c395-386">&lt;TerminateChildProcesses&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-386">&lt;TerminateChildProcesses&gt;</span></span>

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      <span data-ttu-id="3c395-387">&lt;/TerminateChildProcesses&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-387">&lt;/TerminateChildProcesses&gt;</span></span>

      <span data-ttu-id="3c395-388">..</span><span class="sxs-lookup"><span data-stu-id="3c395-388">..</span></span>

    <span data-ttu-id="3c395-389">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="3c395-389">&lt;/MachineConfiguration&gt;</span></span>

### <span data-ttu-id="3c395-390">Скрипты</span><span class="sxs-lookup"><span data-stu-id="3c395-390">Scripts</span></span>

<span data-ttu-id="3c395-391">В приведенной ниже таблице описаны различные события сценария и контекст, в котором они могут быть запущены.</span><span class="sxs-lookup"><span data-stu-id="3c395-391">The following table describes the various script events and the context under which they can be run.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c395-392">Время выполнения сценария</span><span class="sxs-lookup"><span data-stu-id="3c395-392">Script Execution Time</span></span></th>
<th align="left"><span data-ttu-id="3c395-393">Может быть указано в конфигурации развертывания</span><span class="sxs-lookup"><span data-stu-id="3c395-393">Can be specified in Deployment Configuration</span></span></th>
<th align="left"><span data-ttu-id="3c395-394">Может быть указано в конфигурации пользователя</span><span class="sxs-lookup"><span data-stu-id="3c395-394">Can be specified in User Configuration</span></span></th>
<th align="left"><span data-ttu-id="3c395-395">Может выполняться в виртуальной среде пакета</span><span class="sxs-lookup"><span data-stu-id="3c395-395">Can run in the Virtual Environment of the package</span></span></th>
<th align="left"><span data-ttu-id="3c395-396">Может выполняться в контексте определенного приложения.</span><span class="sxs-lookup"><span data-stu-id="3c395-396">Can be run in the context of a specific application</span></span></th>
<th align="left"><span data-ttu-id="3c395-397">Работа в контексте системы и пользователя: (конфигурация развертывания, Конфигурация пользователя)</span><span class="sxs-lookup"><span data-stu-id="3c395-397">Runs in system/user context: (Deployment Configuration, User Configuration)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c395-398">AddPackage</span><span class="sxs-lookup"><span data-stu-id="3c395-398">AddPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-399">X</span><span class="sxs-lookup"><span data-stu-id="3c395-399">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3c395-400">(СИСТЕМА, Н/Д)</span><span class="sxs-lookup"><span data-stu-id="3c395-400">(SYSTEM, N/A)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c395-401">PublishPackage</span><span class="sxs-lookup"><span data-stu-id="3c395-401">PublishPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-402">X</span><span class="sxs-lookup"><span data-stu-id="3c395-402">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-403">X</span><span class="sxs-lookup"><span data-stu-id="3c395-403">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3c395-404">(Система, пользователь)</span><span class="sxs-lookup"><span data-stu-id="3c395-404">(SYSTEM, User)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c395-405">UnpublishPackage</span><span class="sxs-lookup"><span data-stu-id="3c395-405">UnpublishPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-406">X</span><span class="sxs-lookup"><span data-stu-id="3c395-406">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-407">X</span><span class="sxs-lookup"><span data-stu-id="3c395-407">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3c395-408">(Система, пользователь)</span><span class="sxs-lookup"><span data-stu-id="3c395-408">(SYSTEM, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c395-409">RemovePackage</span><span class="sxs-lookup"><span data-stu-id="3c395-409">RemovePackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-410">X</span><span class="sxs-lookup"><span data-stu-id="3c395-410">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3c395-411">(СИСТЕМА, Н/Д)</span><span class="sxs-lookup"><span data-stu-id="3c395-411">(SYSTEM, N/A)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c395-412">StartProcess</span><span class="sxs-lookup"><span data-stu-id="3c395-412">StartProcess</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-413">X</span><span class="sxs-lookup"><span data-stu-id="3c395-413">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-414">X</span><span class="sxs-lookup"><span data-stu-id="3c395-414">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-415">X</span><span class="sxs-lookup"><span data-stu-id="3c395-415">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-416">X</span><span class="sxs-lookup"><span data-stu-id="3c395-416">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-417">(Пользователь, пользователь)</span><span class="sxs-lookup"><span data-stu-id="3c395-417">(User, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c395-418">ExitProcess</span><span class="sxs-lookup"><span data-stu-id="3c395-418">ExitProcess</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-419">X</span><span class="sxs-lookup"><span data-stu-id="3c395-419">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-420">X</span><span class="sxs-lookup"><span data-stu-id="3c395-420">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3c395-421">X</span><span class="sxs-lookup"><span data-stu-id="3c395-421">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-422">(Пользователь, пользователь)</span><span class="sxs-lookup"><span data-stu-id="3c395-422">(User, User)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c395-423">StartVirtualEnvironment</span><span class="sxs-lookup"><span data-stu-id="3c395-423">StartVirtualEnvironment</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-424">X</span><span class="sxs-lookup"><span data-stu-id="3c395-424">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-425">X</span><span class="sxs-lookup"><span data-stu-id="3c395-425">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-426">X</span><span class="sxs-lookup"><span data-stu-id="3c395-426">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3c395-427">(Пользователь, пользователь)</span><span class="sxs-lookup"><span data-stu-id="3c395-427">(User, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c395-428">TerminateVirtualEnvironment</span><span class="sxs-lookup"><span data-stu-id="3c395-428">TerminateVirtualEnvironment</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-429">X</span><span class="sxs-lookup"><span data-stu-id="3c395-429">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c395-430">X</span><span class="sxs-lookup"><span data-stu-id="3c395-430">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3c395-431">(Пользователь, пользователь)</span><span class="sxs-lookup"><span data-stu-id="3c395-431">(User, User)</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3c395-432">Создание динамического файла конфигурации с помощью файла манифеста App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3c395-432">Create a Dynamic Configuration file using an App-V 5.0 Manifest file</span></span>

<span data-ttu-id="3c395-433">Вы можете создать файл динамической конфигурации с помощью одного из трех методов: либо вручную, с помощью консоли управления App-V 5,0, либо последовательности пакета, который будет создан с помощью 2 примеров файлов.</span><span class="sxs-lookup"><span data-stu-id="3c395-433">You can create the Dynamic Configuration file using one of three methods: either manually, using the App-V 5.0 Management Console or sequencing a package, which will be generated with 2 sample files.</span></span>

<span data-ttu-id="3c395-434">Дополнительные сведения о том, как создать файл с помощью консоли управления App-V 5,0, можно найти в разделе [Создание настраиваемого файла конфигурации с помощью консоли управления App-v 5,0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span><span class="sxs-lookup"><span data-stu-id="3c395-434">For more information about how to create the file using the App-V 5.0 Management Console see, [How to Create a Custom Configuration File by Using the App-V 5.0 Management Console](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span></span>

<span data-ttu-id="3c395-435">Чтобы создать файл вручную, данные, приведенные выше в предыдущих разделах, можно объединить в один файл.</span><span class="sxs-lookup"><span data-stu-id="3c395-435">To create the file manually, the information above in previous sections can be combined into a single file.</span></span> <span data-ttu-id="3c395-436">Мы рекомендуем использовать файлы, созданные секвенсором.</span><span class="sxs-lookup"><span data-stu-id="3c395-436">We recommend you use files generated by the sequencer.</span></span>






## <span data-ttu-id="3c395-437">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3c395-437">Related topics</span></span>


[<span data-ttu-id="3c395-438">Применение файла конфигурации развертывания с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c395-438">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[<span data-ttu-id="3c395-439">Применение файла конфигурации пользователя с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c395-439">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[<span data-ttu-id="3c395-440">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3c395-440">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





