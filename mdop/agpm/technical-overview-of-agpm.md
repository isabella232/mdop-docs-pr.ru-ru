---
title: Технический обзор AGPM
description: Технический обзор AGPM
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818299"
---
# <span data-ttu-id="63807-103">Технический обзор AGPM</span><span class="sxs-lookup"><span data-stu-id="63807-103">Technical Overview of AGPM</span></span>


<span data-ttu-id="63807-104">Расширенное управление групповыми политиками Microsoft — это клиентское и серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="63807-104">Microsoft Advanced Group Policy Management (AGPM) is a client/server application.</span></span> <span data-ttu-id="63807-105">Сервер политики доменных групп (в том есть не в архиве), который создается с помощью РАСШИРЕНного использования файловой системы сервера.</span><span class="sxs-lookup"><span data-stu-id="63807-105">The AGPM Server stores Group Policy Objects (GPOs) offline in the archive that AGPM creates on the server's file system.</span></span> <span data-ttu-id="63807-106">Администраторы групповых политик используют оснастку РАСШИРЕНного управления групповыми политиками для работы с объектами групповой политики на сервере, на котором размещается Архив.</span><span class="sxs-lookup"><span data-stu-id="63807-106">Group Policy administrators use the AGPM snap-in for the Group Policy Management Console (GPMC) to work with GPOs on the server that hosts the archive.</span></span> <span data-ttu-id="63807-107">Общие сведения об элементах управления групповыми политиками и связанных с ними элементах, о том, как они хранят объекты групповой политики в файловой системе, а также о том, как разрешения на доступ к действиям для каждой роли пользователей могут улучшить эффективность администраторов групповых политик.</span><span class="sxs-lookup"><span data-stu-id="63807-107">Understanding the parts of AGPM and related items, how they store GPOs in the file system, and how permissions control the actions available to each user role can improve Group Policy administrators' effectiveness with AGPM.</span></span>

## <span data-ttu-id="63807-108">Терминология</span><span class="sxs-lookup"><span data-stu-id="63807-108">Terminology</span></span>


<span data-ttu-id="63807-109">Ниже описаны основные термины РАСШИРЕНного использования.</span><span class="sxs-lookup"><span data-stu-id="63807-109">The following explains the basic AGPM terms.</span></span>

-   <span data-ttu-id="63807-110">**Клиент с расширенными политиками.** Компьютер, на котором запущена оснастка расширенного управления групповыми политиками (GPMC), и администраторы групповых политик управляют объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-110">**AGPM Client:** A computer that runs the AGPM snap-in for the Group Policy Management Console (GPMC) and from which Group Policy administrators manage GPOs.</span></span>

-   <span data-ttu-id="63807-111">**Оснастка "расширенная работа с групповыми политиками"** Программный компонент расширенного управления групповыми политиками, установленный на клиентах с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="63807-111">**AGPM snap-in:** The software component of AGPM installed on AGPM Clients so that they can manage GPOs.</span></span>

-   <span data-ttu-id="63807-112">**Сервер расширенного на:** Сервер, на котором запущена служба управления групповыми политиками и управляющий Архив.</span><span class="sxs-lookup"><span data-stu-id="63807-112">**AGPM Server:** A server that runs the AGPM Service and manages an archive.</span></span> <span data-ttu-id="63807-113">Каждый сервер расширенного управления групповыми политиками может управлять только одним архивом, но один из них может управлять архивными данными для нескольких доменов в одном архиве.</span><span class="sxs-lookup"><span data-stu-id="63807-113">Each AGPM Server can manage only one archive, but one AGPM Server can manage archive data for multiple domains in one archive.</span></span> <span data-ttu-id="63807-114">Архив может быть размещен на компьютере, отличном от сервера с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="63807-114">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="63807-115">**Служба расширенного обслуживания:** Программный компонент, который выполняется на сервере РАСШИРЕНного использования в качестве службы.</span><span class="sxs-lookup"><span data-stu-id="63807-115">**AGPM Service:** The software component of AGPM that runs on an AGPM Server as a service.</span></span> <span data-ttu-id="63807-116">Служба управляет объектами групповой политики в архиве и в рабочей среде в этом лесу.</span><span class="sxs-lookup"><span data-stu-id="63807-116">The service manages GPOs in the archive and in the production environment in that forest.</span></span>

-   <span data-ttu-id="63807-117">**Архивировать:** В разделе управления групповыми политиками — центральное хранилище, содержащее управляемые объекты групповой политики, которые управляются с помощью соответствующего сервера РАСШИРЕНных данных, в дополнение к журналу для каждого из этих объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-117">**Archive:** In AGPM, a central store that contains the controlled GPOs that the associated AGPM Server manages, in addition to the history for each of those GPOs.</span></span> <span data-ttu-id="63807-118">Сюда входят все предыдущие контрольные версии каждого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-118">This includes all previous controlled versions of each GPO.</span></span> <span data-ttu-id="63807-119">Архив состоит из архивного индекса и связанных с ними архивных данных, которые могут содержать данные для GPO в нескольких доменах.</span><span class="sxs-lookup"><span data-stu-id="63807-119">An archive consists of an archive index file and associated archive data that may include data for GPOs in multiple domains.</span></span> <span data-ttu-id="63807-120">Архив может быть размещен на компьютере, отличном от сервера с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="63807-120">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="63807-121">**Управляемый объект групповой политики:** Объект групповой политики, управляемый с помощью расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="63807-121">**Controlled GPO:** A GPO that is being managed by AGPM.</span></span> <span data-ttu-id="63807-122">Управление групповыми политиками управляет журналом и разрешениями управляемых объектов групповой политики, которые хранятся в архиве.</span><span class="sxs-lookup"><span data-stu-id="63807-122">AGPM manages the history and permissions of controlled GPOs, which it stores in the archive.</span></span>

-   <span data-ttu-id="63807-123">**Неконтрольный объект групповой политики:** Объект групповой политики в рабочей среде для домена и не управляется с помощью расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="63807-123">**Uncontrolled GPO:** A GPO in the production environment for a domain and not managed by AGPM.</span></span>

## <span data-ttu-id="63807-124">Как выполняется установка, создание и влияние на</span><span class="sxs-lookup"><span data-stu-id="63807-124">What AGPM installs, creates, and affects</span></span>


<span data-ttu-id="63807-125">На сервере с РАСШИРЕНным интерфейсом, программа установки РАСШИРЕНного обновления Windows устанавливает службу РАСШИРЕНного включения.</span><span class="sxs-lookup"><span data-stu-id="63807-125">On an AGPM Server, the AGPM Setup program installs the AGPM Service.</span></span> <span data-ttu-id="63807-126">РАСШИРЕНная аналитика не изменяет службу каталогов Active Directory® или схему.</span><span class="sxs-lookup"><span data-stu-id="63807-126">AGPM does not alter the Active Directory® directory service or the schema.</span></span> <span data-ttu-id="63807-127">По умолчанию файлы программного сервера с РАСШИРЕНным языком и установленными в%ProgramFiles%\\Microsoft\\AGPM\\Server.</span><span class="sxs-lookup"><span data-stu-id="63807-127">By default, the AGPM Server program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Server.</span></span> <span data-ttu-id="63807-128">Вы можете установить на контроллере домена службу расширенного управления групповыми политиками, если это необходимо; Тем не менее, мы рекомендуем установить службу РАСШИРЕНного разрешения на рядовой сервер.</span><span class="sxs-lookup"><span data-stu-id="63807-128">You can install the AGPM Service on a domain controller if you have to; however, we recommend that you install the AGPM Service on a member server.</span></span>

<span data-ttu-id="63807-129">В клиенте расширенного управления групповыми политиками программа установки расширенного управления групповыми политиками устанавливает оснастку " **Управление** групповыми политиками", добавляя к каждому домену, который отображается в GPMC, папку</span><span class="sxs-lookup"><span data-stu-id="63807-129">On an AGPM Client, the AGPM Setup program installs the AGPM snap-in, adding a **Change Control** folder to each domain that appears in the GPMC.</span></span> <span data-ttu-id="63807-130">По умолчанию файлы клиентской программы с РАСШИРЕНным управлением разрядом установлены в%ProgramFiles%\\Microsoft\\AGPM\\Client.</span><span class="sxs-lookup"><span data-stu-id="63807-130">By default, the AGPM Client program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Client.</span></span>

<span data-ttu-id="63807-131">В таблице 1 описаны элементы, которые вы устанавливаете и создаете с помощью РАСШИРЕНного вида, и компоненты операционной системы, влияющие на работу с помощью РАСШИРЕНного вида.</span><span class="sxs-lookup"><span data-stu-id="63807-131">Table 1 describes both the items that AGPM installs or creates and the parts of the operating system that affect AGPM operation.</span></span>

**<span data-ttu-id="63807-132">Таблица 1: элементы, установленные, созданные и затрагиваемые РАСШИРЕНным пользователем.</span><span class="sxs-lookup"><span data-stu-id="63807-132">Table 1: Items installed, created, or affected by AGPM</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="63807-133">Элемент</span><span class="sxs-lookup"><span data-stu-id="63807-133">Item</span></span></th>
<th align="left"><span data-ttu-id="63807-134">Описание</span><span class="sxs-lookup"><span data-stu-id="63807-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63807-135">Служба РАСШИРЕНного обслуживания</span><span class="sxs-lookup"><span data-stu-id="63807-135">AGPM Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-136">Служба РАСШИРЕНного выполнения операций выполняется на сервере с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="63807-136">The AGPM Service runs on the AGPM Server.</span></span> <span data-ttu-id="63807-137">Служба управляет архивом, который включает автономные объекты групповой политики, а также управляемые объекты групповой политики в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="63807-137">The service manages the archive, which contains offline GPOs, and controlled GPOs in the production environment.</span></span> <span data-ttu-id="63807-138">По умолчанию в качестве конфигурации службы РАСШИРЕНной настройки используется следующее:</span><span class="sxs-lookup"><span data-stu-id="63807-138">The default configuration of the AGPM Service is as follows:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="63807-139">Имя службы: </strong> Служба расширенного</span><span class="sxs-lookup"><span data-stu-id="63807-139">Service name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="63807-140">Отображаемое имя: </strong> Служба расширенного просмотра</span><span class="sxs-lookup"><span data-stu-id="63807-140">Display name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="63807-141">Путь к исполняемому файлу: </strong> % ProgramFiles% \Microsoft\AGPM\Server\Agpm.exe</span><span class="sxs-lookup"><span data-stu-id="63807-141">Path to executable:</strong> %ProgramFiles%\Microsoft\AGPM\Server\Agpm.exe</span></span></p></li>
<li><p><strong><span data-ttu-id="63807-142">Автозапуск: </strong> Автоматический</span><span class="sxs-lookup"><span data-stu-id="63807-142">Startup:</strong> Automatic</span></span></p></li>
<li><p><strong><span data-ttu-id="63807-143">Вход в </strong> учетную запись службы расширенного управления групповыми политиками, заданной во время установки сервера с расширенным доступом, который можно изменить с помощью <strong> программ и компонентов </strong> на <strong> панели управления </strong> .</span><span class="sxs-lookup"><span data-stu-id="63807-143">Log on as:</strong> AGPM Service Account specified during installation of AGPM Server, which can be changed using <strong>Programs and Features</strong> in the <strong>Control Panel</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63807-144">Архивация в РАСШИРЕНном</span><span class="sxs-lookup"><span data-stu-id="63807-144">AGPM archive</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-145">По умолчанию в расширенном управлении групповыми политиками создается архив на%ProgramData%\Microsoft\AGPM на сервере РАСШИРЕНного включения.</span><span class="sxs-lookup"><span data-stu-id="63807-145">By default, AGPM creates the archive in %ProgramData%\Microsoft\AGPM on the AGPM Server.</span></span> <span data-ttu-id="63807-146">Архив предоставляет хранилище для автономных объектов групповой политики и может хранить несколько версий каждого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-146">The archive provides storage for offline GPOs, and it can store multiple versions of each GPO.</span></span> <span data-ttu-id="63807-147">Изменения, вносимые в параметры РАСШИРЕНного использования групповой политики в архиве, не влияют на производственную среду, пока администратор и утверждающий не развернут объект групповой политики в рабочей среде и не связывает GPO с подразделением (OU).</span><span class="sxs-lookup"><span data-stu-id="63807-147">Changes that AGPM makes to GPOs in the archive do not affect the production environment until an AGPM Administrator or Approver deploys the GPO to the production environment and links the GPO to an organizational unit (OU).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63807-148">Брандмауэр Windows</span><span class="sxs-lookup"><span data-stu-id="63807-148">Windows Firewall</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-149">Во время установки с помощью РАСШИРЕНного ключа политики для Windows можно настроить для него связь с сервером с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="63807-149">During installation, AGPM enables an inbound Windows Firewall rule that allows the AGPM Client to communicate with the AGPM Server.</span></span> <span data-ttu-id="63807-150">Правило брандмауэра Windows по умолчанию имеет следующие значения:</span><span class="sxs-lookup"><span data-stu-id="63807-150">The default Windows Firewall rule is the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="63807-151">Name (имя): </strong> Служба расширенного обслуживания</span><span class="sxs-lookup"><span data-stu-id="63807-151">Name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="63807-152">Действие: </strong> Разрешить подключение</span><span class="sxs-lookup"><span data-stu-id="63807-152">Action:</strong> Allow the connection</span></span></p></li>
<li><p><strong><span data-ttu-id="63807-153">Программы: </strong> все программы, отвечающие заданным условиям</span><span class="sxs-lookup"><span data-stu-id="63807-153">Programs:</strong> All programs that meet the specified conditions</span></span></p></li>
<li><p><strong><span data-ttu-id="63807-154">Тип протокола: </strong> TCP</span><span class="sxs-lookup"><span data-stu-id="63807-154">Protocol type:</strong> TCP</span></span></p></li>
<li><p><strong><span data-ttu-id="63807-155">Локальный порт: </strong> 4600</span><span class="sxs-lookup"><span data-stu-id="63807-155">Local port:</strong> 4600</span></span></p></li>
<li><p><strong><span data-ttu-id="63807-156">Удаленный порт: </strong> все порты</span><span class="sxs-lookup"><span data-stu-id="63807-156">Remote port:</strong> All ports</span></span></p></li>
<li><p><strong><span data-ttu-id="63807-157">Локальный IP-адрес: </strong> любой</span><span class="sxs-lookup"><span data-stu-id="63807-157">Local IP address:</strong> Any</span></span></p></li>
<li><p><strong><span data-ttu-id="63807-158">Удаленный IP-адрес: </strong> любой</span><span class="sxs-lookup"><span data-stu-id="63807-158">Remote IP address:</strong> Any</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63807-159">Сервер электронной почты</span><span class="sxs-lookup"><span data-stu-id="63807-159">E-mail server</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-160">Функция РАСШИРЕНного доступа к данным использует протокол SMTP для отправки запросов по электронной почте на адреса, настроенные на <strong> вкладке "Делегирование домена </strong> ". Например, когда редактор запрашивает создание объекта групповой политики, он уведомляет каждый адрес электронной почты, указанный на <strong> вкладке "Делегирование домена </strong> ".</span><span class="sxs-lookup"><span data-stu-id="63807-160">AGPM uses Simple Mail Transfer Protocol (SMTP) to send e-mail requests to the addresses configured on the <strong>Domain Delegation</strong> tab. For example, when an Editor requests that a new GPO be created, AGPM notifies each e-mail address specified on the <strong>Domain Delegation</strong> tab.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63807-161">Оснастка РАСШИРЕНного режима</span><span class="sxs-lookup"><span data-stu-id="63807-161">AGPM snap-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-162">Оснастка управления ГРУППОВыми политиками для GPMC работает на клиентах с РАСШИРЕНными правами и используется администраторами групповых политик для управления объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-162">The AGPM snap-in for the GPMC runs on AGPM Clients and is used by Group Policy administrators to manage GPOs.</span></span> <span data-ttu-id="63807-163">Эта оснастка появится в консоли управления групповыми политиками в качестве <strong> папки для контроля изменений </strong> в каждом домене.</span><span class="sxs-lookup"><span data-stu-id="63807-163">The snap-in appears in the GPMC as a <strong>Change Control</strong> folder in each domain.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="63807-164">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="63807-164">Additional references</span></span>

<span data-ttu-id="63807-165">Дополнительные сведения о файлах, установленных с помощью РАСШИРЕНного администрирования, можно найти в [руководстве по планированию для расширенного](https://go.microsoft.com/fwlink/?LinkId=160060)набора данных.</span><span class="sxs-lookup"><span data-stu-id="63807-165">For more information about the files installed by AGPM, see the [Planning Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).</span></span>

## <span data-ttu-id="63807-166">Archive</span><span class="sxs-lookup"><span data-stu-id="63807-166">Archive</span></span>


<span data-ttu-id="63807-167">По умолчанию при установке сервера РАСШИРЕНного анализа данных на локальном жестком диске сервера с РАСШИРЕНным набором (%ProgramData%\\Microsoft\\AGPM.) создается архив.</span><span class="sxs-lookup"><span data-stu-id="63807-167">By default, the AGPM Server installation process creates the archive on the local hard disk of the AGPM Server at %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="63807-168">Однако вы можете изменить путь во время установки и даже создать его на сервере, отличном от сервера РАСШИРЕНного поиска.</span><span class="sxs-lookup"><span data-stu-id="63807-168">However, you can change the path during installation and even create the archive on a server other than the AGPM Server.</span></span>

<span data-ttu-id="63807-169">Архив имеет вложенную папку для каждой версии каждого объекта групповой политики, содержащегося в архиве.</span><span class="sxs-lookup"><span data-stu-id="63807-169">The archive contains a subfolder for each version of each GPO the archive contains.</span></span> <span data-ttu-id="63807-170">Имя каждой вложенной папки — идентификатор GUID, обозначающий версию объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-170">The name of each subfolder is a GUID that identifies a version of the GPO.</span></span>

<span data-ttu-id="63807-171">Файл gpostate.xml записывает состояние каждого объекта групповой политики в архиве.</span><span class="sxs-lookup"><span data-stu-id="63807-171">The gpostate.xml file records the state of each GPO in the archive.</span></span> <span data-ttu-id="63807-172">Файл — это манифест, описывающий содержимое архива.</span><span class="sxs-lookup"><span data-stu-id="63807-172">The file is a manifest that describes the contents of the archive.</span></span> <span data-ttu-id="63807-173">Например, объект GPO может иметь много версий, и каждая версия находится в своей собственной папке в архиве.</span><span class="sxs-lookup"><span data-stu-id="63807-173">For example, a GPO can have many versions, and each version is in its own subfolder in the archive.</span></span> <span data-ttu-id="63807-174">Файл gpostate.xml указывает, какие вложенные папки содержат различные версии одного объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-174">The gpostate.xml file indicates which subfolders contain different versions of a single GPO.</span></span> <span data-ttu-id="63807-175">Кроме того, у шаблонов объектов групповой политики есть вложенные папки в архиве, но gpostate.xml указывает на то, что они являются шаблонами, а не управляемыми объектами GPO.</span><span class="sxs-lookup"><span data-stu-id="63807-175">Additionally, GPO templates have subfolders in the archive, but gpostate.xml indicates that these are templates and not controlled GPOs.</span></span> <span data-ttu-id="63807-176">Аналогичным образом, когда администраторы групповой политики удаляют GPO, они изменяют состояние в gpostate.xml, чтобы показать, что они находятся в **корзине** , но фактически не удаляют вложенные папки GPO из архива.</span><span class="sxs-lookup"><span data-stu-id="63807-176">Similarly, when Group Policy administrators delete GPOs, AGPM changes their states in gpostate.xml to indicate that they are in the **Recycle Bin** but does not actually remove the GPOs' subfolders from the archive.</span></span>

<span data-ttu-id="63807-177">**Внимание!**  Не изменяйте вручную gpostate.xml или объекты групповой политики, которые содержатся в архиве.</span><span class="sxs-lookup"><span data-stu-id="63807-177">**Caution** Do not manually edit gpostate.xml or the GPOs the archive contains.</span></span> <span data-ttu-id="63807-178">Эта информация предоставляется только для понимания того, как будет расширено общее представление о архиве РАСШИРЕНного анализа данных.</span><span class="sxs-lookup"><span data-stu-id="63807-178">This information is provided only to enhance understanding of the AGPM archive.</span></span> <span data-ttu-id="63807-179">Вместо этого используйте оснастку "ГРУППОВое преобразование" для изменения GPO.</span><span class="sxs-lookup"><span data-stu-id="63807-179">Instead, use the AGPM snap-in to change GPOs.</span></span>

 

<span data-ttu-id="63807-180">Если вы создаете архив с помощью РАСШИРЕНного управления правами, он предоставляет полный контроль над системой, администраторами и учетной записью службы РАСШИРЕНного доступа (указанной в разделе Настройка сервера управления групповыми политиками).</span><span class="sxs-lookup"><span data-stu-id="63807-180">When AGPM creates the archive, it gives Full Control to SYSTEM, Administrators, and the AGPM Service Account (specified in the setup of AGPM Server).</span></span> <span data-ttu-id="63807-181">Изменение разрешений на доступ к архиву с помощью пользовательского интерфейса с расширенным управлением групповыми политиками не влияет на эти разрешения, так как учетная запись службы РАСШИРЕНного доступа выполняет все операции от имени пользователя, выполнившего вход.</span><span class="sxs-lookup"><span data-stu-id="63807-181">Changing permissions by using the AGPM user interface on the AGPM snap-in does not alter permissions on the archive, because the AGPM Service Account performs all operations on behalf of the logged-on user.</span></span>

### <span data-ttu-id="63807-182">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="63807-182">Additional references</span></span>

<span data-ttu-id="63807-183">Сведения о том, как создать резервную копию архива, восстановить архив из резервной копии или переместить оба сервера РАСШИРЕНного использования (и архивов), можно найти в разделе "выполнение задач администратора РАСШИРЕНного администрирования для расширенного состояния" в руководстве по управлению [групповыми политиками](https://go.microsoft.com/fwlink/?LinkId=160061).</span><span class="sxs-lookup"><span data-stu-id="63807-183">For information about how to back up the archive, restore the archive from a backup, or move both the AGPM Server and the archive, see the "Performing AGPM Administrator Tasks" section in the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

## <span data-ttu-id="63807-184">Роли и разрешения</span><span class="sxs-lookup"><span data-stu-id="63807-184">Roles and permissions</span></span>


<span data-ttu-id="63807-185">Роли упрощают делегирование.</span><span class="sxs-lookup"><span data-stu-id="63807-185">Roles simplify delegation.</span></span> <span data-ttu-id="63807-186">Вместо того чтобы назначать администраторам группового политики детальные разрешения, администраторы РАСШИРЕНного доступа могут назначить одной из четырех ролей администраторам групповой политики, чтобы они могли выполнять задачи, связанные с этой ролью.</span><span class="sxs-lookup"><span data-stu-id="63807-186">Instead of assigning detailed permissions to Group Policy administrators, AGPM Administrators can assign one of four roles to Group Policy administrators to let them perform work related to that role:</span></span>

-   <span data-ttu-id="63807-187">**Администратор расширенного администрирования:** Администраторы групповой политики, которым назначена роль администратора РАСШИРЕНного доступа (полный доступ), могут выполнять любые задачи в РАСШИРЕНном режимах.</span><span class="sxs-lookup"><span data-stu-id="63807-187">**AGPM Administrator:** Group Policy administrators assigned the AGPM Administrator (Full Control) role can perform any task in AGPM.</span></span> <span data-ttu-id="63807-188">Администраторы РАСШИРЕНного доступа к данным могут настраивать параметры уровня домена и делегировать разрешения другим администраторам групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-188">AGPM Administrators can configure domain-wide options and delegate permissions to other Group Policy administrators.</span></span>

-   <span data-ttu-id="63807-189">**Утверждающий:** Администраторы групповой политики, которым назначена роль утверждающего, могут развернуть GPO в рабочей среде домена.</span><span class="sxs-lookup"><span data-stu-id="63807-189">**Approver:** Group Policy administrators assigned the Approver role can deploy GPOs to the production environment for a domain.</span></span> <span data-ttu-id="63807-190">Кроме того, утверждающие могут создавать и удалять объекты групповой политики, а также утверждать и отклонять запросы от редакторов.</span><span class="sxs-lookup"><span data-stu-id="63807-190">Approvers can also create and delete GPOs and approve or reject requests from Editors.</span></span> <span data-ttu-id="63807-191">Утверждающие могут просматривать список объектов групповой политики в домене, просматривать параметры политики в GPO и создавать и просматривать отчеты о параметрах политики в объекте групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-191">Approvers can view the list of GPOs in a domain, view the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="63807-192">Они не могут изменять параметры политики в GPO, если им не назначена роль редактора.</span><span class="sxs-lookup"><span data-stu-id="63807-192">They cannot edit the policy settings in GPOs unless they are also assigned the Editor role.</span></span>

-   <span data-ttu-id="63807-193">**Редактор:** Администраторы групповой политики, которым назначена роль "редактор", могут просматривать список GPO в домене, просматривать параметры политики в объектах GPO, изменять параметры политики в GPO, а также создавать и просматривать отчеты о параметрах политики в GPO.</span><span class="sxs-lookup"><span data-stu-id="63807-193">**Editor:** Group Policy administrators assigned the Editor role can view the list of GPOs in a domain, view the policy settings in GPOs, edit the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="63807-194">Если им не назначена роль утверждающего, редакторы не могут создавать, развертывать и удалять GPO.</span><span class="sxs-lookup"><span data-stu-id="63807-194">Unless they are also assigned the Approver role, Editors cannot create, deploy, or delete GPOs.</span></span> <span data-ttu-id="63807-195">Однако они могут запрашивать создание, развертывание и удаление объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-195">However, they can request that GPOs be created, deployed, or deleted.</span></span>

-   <span data-ttu-id="63807-196">**Рецензент:** Администраторы групповой политики, которым назначена роль рецензента, могут просматривать список GPO в домене и создавать и просматривать отчеты о параметрах политики в объекте групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-196">**Reviewer:** Group Policy administrators assigned the Reviewer role can view the list of GPOs in a domain and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="63807-197">Если им не назначена роль редактора, они не могут изменять параметры политики в объекте групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-197">Unless they are also assigned the Editor role, they cannot edit policy settings in a GPO.</span></span>

<span data-ttu-id="63807-198">С помощью оснастки РАСШИРЕНного доступа администраторы не смогут настраивать разрешения на более подробном уровне, чем роли.</span><span class="sxs-lookup"><span data-stu-id="63807-198">AGPM gives AGPM Administrators the flexibility to configure permissions at a more detailed level than roles by using the AGPM snap-in.</span></span> <span data-ttu-id="63807-199">В таблице 2 описаны эти разрешения и указаны разрешения, предоставленные каждой роли по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="63807-199">Table 2 describes these permissions and indicates the permissions granted to each role by default.</span></span>

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
<th align="left"><span data-ttu-id="63807-200">Разрешение</span><span class="sxs-lookup"><span data-stu-id="63807-200">Permission</span></span></th>
<th align="left"><span data-ttu-id="63807-201">Описание</span><span class="sxs-lookup"><span data-stu-id="63807-201">Description</span></span></th>
<th align="left"><span data-ttu-id="63807-202">Администратор РАСШИРЕНного администрирования</span><span class="sxs-lookup"><span data-stu-id="63807-202">AGPM Administrator</span></span></th>
<th align="left"><span data-ttu-id="63807-203">Утверждающий</span><span class="sxs-lookup"><span data-stu-id="63807-203">Approver</span></span></th>
<th align="left"><span data-ttu-id="63807-204">Editor</span><span class="sxs-lookup"><span data-stu-id="63807-204">Editor</span></span></th>
<th align="left"><span data-ttu-id="63807-205">Рецензента</span><span class="sxs-lookup"><span data-stu-id="63807-205">Reviewer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63807-206">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="63807-206">Full Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63807-207">У вас есть все разрешения.</span><span class="sxs-lookup"><span data-stu-id="63807-207">Have all permissions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-208">Да</span><span class="sxs-lookup"><span data-stu-id="63807-208">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63807-209">Создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="63807-209">Create GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63807-210">Создание объектов групповой политики в домене.</span><span class="sxs-lookup"><span data-stu-id="63807-210">Create GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-211">Да</span><span class="sxs-lookup"><span data-stu-id="63807-211">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-212">Да</span><span class="sxs-lookup"><span data-stu-id="63807-212">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63807-213">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="63807-213">List Contents</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63807-214">Перечислите объекты GPO в домене.</span><span class="sxs-lookup"><span data-stu-id="63807-214">List the GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-215">Да</span><span class="sxs-lookup"><span data-stu-id="63807-215">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-216">Да</span><span class="sxs-lookup"><span data-stu-id="63807-216">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-217">Да</span><span class="sxs-lookup"><span data-stu-id="63807-217">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-218">Да</span><span class="sxs-lookup"><span data-stu-id="63807-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63807-219">Чтение параметров</span><span class="sxs-lookup"><span data-stu-id="63807-219">Read Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63807-220">Чтение параметров политики в объекте групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-220">Read the policy settings within a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-221">Да</span><span class="sxs-lookup"><span data-stu-id="63807-221">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-222">Да</span><span class="sxs-lookup"><span data-stu-id="63807-222">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-223">Да</span><span class="sxs-lookup"><span data-stu-id="63807-223">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-224">Да</span><span class="sxs-lookup"><span data-stu-id="63807-224">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63807-225">Изменить параметры</span><span class="sxs-lookup"><span data-stu-id="63807-225">Edit Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63807-226">Изменение параметров политики в объекте групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-226">Change the policy settings in a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-227">Да</span><span class="sxs-lookup"><span data-stu-id="63807-227">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="63807-228">Да</span><span class="sxs-lookup"><span data-stu-id="63807-228">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63807-229">Удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="63807-229">Delete GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63807-230">Удаление объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-230">Delete a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-231">Да</span><span class="sxs-lookup"><span data-stu-id="63807-231">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-232">Да</span><span class="sxs-lookup"><span data-stu-id="63807-232">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63807-233">Изменение параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="63807-233">Modify Security</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63807-234">Передача доступа на уровне домена, делегирование доступа к одному GPO и передача доступа в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="63807-234">Delegate domain-level access, delegate access to a single GPO, and delegate access to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-235">Да</span><span class="sxs-lookup"><span data-stu-id="63807-235">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63807-236">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="63807-236">Deploy GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63807-237">Развертывание объекта групповой политики из архива в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="63807-237">Deploy a GPO from the archive to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-238">Да</span><span class="sxs-lookup"><span data-stu-id="63807-238">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-239">Да</span><span class="sxs-lookup"><span data-stu-id="63807-239">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63807-240">Создание шаблона</span><span class="sxs-lookup"><span data-stu-id="63807-240">Create Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63807-241">Создание шаблона GPO в РАСШИРЕНном наборе групповой политики.</span><span class="sxs-lookup"><span data-stu-id="63807-241">Create a GPO template in AGPM.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-242">Да</span><span class="sxs-lookup"><span data-stu-id="63807-242">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="63807-243">Да</span><span class="sxs-lookup"><span data-stu-id="63807-243">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63807-244">Изменение параметров</span><span class="sxs-lookup"><span data-stu-id="63807-244">Modify Options</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63807-245">Настройте уведомления по электронной почте с помощью РАСШИРЕНного задания и ограничьте версии GPO, хранящиеся в архиве.</span><span class="sxs-lookup"><span data-stu-id="63807-245">Configure AGPM e-mail notification and limit the GPO versions stored in the archive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-246">Да</span><span class="sxs-lookup"><span data-stu-id="63807-246">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63807-247">Экспорт GPO</span><span class="sxs-lookup"><span data-stu-id="63807-247">Export GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63807-248">Экспортируйте объект групповой политики в файл.</span><span class="sxs-lookup"><span data-stu-id="63807-248">Export a GPO to a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-249">Да</span><span class="sxs-lookup"><span data-stu-id="63807-249">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="63807-250">Да</span><span class="sxs-lookup"><span data-stu-id="63807-250">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63807-251">Импорт объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="63807-251">Import GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63807-252">Импорт объекта групповой политики из файла.</span><span class="sxs-lookup"><span data-stu-id="63807-252">Import a GPO from a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63807-253">Да</span><span class="sxs-lookup"><span data-stu-id="63807-253">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="63807-254">Да</span><span class="sxs-lookup"><span data-stu-id="63807-254">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="63807-255">**Примечание** 
 Разрешения на **Экспорт GPO** и **импорт GPO** недоступны в расширенном расположении, 3,0 или 2,5.</span><span class="sxs-lookup"><span data-stu-id="63807-255">**Note**
**Export GPO** and **Import GPO** permissions are not available in AGPM 3.0 or 2.5.</span></span>

<span data-ttu-id="63807-256">Возможность делегирования доступа к GPO в рабочей среде для домена и возможность ограничения количества сохраненных версий GPO недоступны в РАСШИРЕНном расположении 2,5.</span><span class="sxs-lookup"><span data-stu-id="63807-256">The ability to delegate access to GPOs in the production environment for a domain and the ability to limit the number of GPO versions stored are not available in AGPM 2.5.</span></span>

 

### <span data-ttu-id="63807-257">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="63807-257">Additional references</span></span>

<span data-ttu-id="63807-258">Сведения о том, какие задачи могут выполнять администраторы групповой политики, которым назначена определенная роль, или о том, какие разрешения необходимы для выполнения конкретной задачи, можно найти в [руководстве по эксплуатации для расширенного](https://go.microsoft.com/fwlink/?LinkId=160061)доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="63807-258">For information about what tasks can be performed by Group Policy administrators assigned a particular role or about which permissions are required to perform a specific task, see the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

 

 





