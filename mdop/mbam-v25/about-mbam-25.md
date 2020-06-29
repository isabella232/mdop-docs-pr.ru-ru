---
title: О программе MBAM 2.5
description: О программе MBAM 2.5
author: dansimp
ms.assetid: 1ce218ec-4d2e-4a75-8d1a-68d737a8f3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d4c9ff0bc5ee3f7dc51a56cc428081a7c3783694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824212"
---
# <span data-ttu-id="dd0c7-103">О программе MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dd0c7-103">About MBAM 2.5</span></span>


<span data-ttu-id="dd0c7-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) 2,5 обеспечивает упрощенный интерфейс администрирования для шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 provides a simplified administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="dd0c7-105">BitLocker поддерживает улучшенную защиту от кражи данных и уязвимости данных для потерянных или похищенных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-105">BitLocker offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="dd0c7-106">BitLocker шифрует все данные, хранящиеся на томах и дисках операционной системы Windows, а также на настроенных дисках данных.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-106">BitLocker encrypts all data that is stored on the Windows operating system volumes and drives and configured data drives.</span></span>

## <span data-ttu-id="dd0c7-107">Общие сведения о MBAM</span><span class="sxs-lookup"><span data-stu-id="dd0c7-107">Overview of MBAM</span></span>


<span data-ttu-id="dd0c7-108">MBAM 2,5 обладает следующими возможностями:</span><span class="sxs-lookup"><span data-stu-id="dd0c7-108">MBAM 2.5 has the following features:</span></span>

-   <span data-ttu-id="dd0c7-109">позволяет администраторам автоматизировать процедуру шифрования томов на клиентских компьютерах в организации;</span><span class="sxs-lookup"><span data-stu-id="dd0c7-109">Enables administrators to automate the process of encrypting volumes on client computers across the enterprise.</span></span>

-   <span data-ttu-id="dd0c7-110">позволяет специалистам по безопасности быстро определять состояние соответствия требованиям отдельных компьютеров или всей организации;</span><span class="sxs-lookup"><span data-stu-id="dd0c7-110">Enables security officers to quickly determine the compliance state of individual computers or even of the enterprise itself.</span></span>

-   <span data-ttu-id="dd0c7-111">обеспечивает возможность централизованного составления отчетности и управления оборудованием с использованием Microsoft System Center Configuration Manager;</span><span class="sxs-lookup"><span data-stu-id="dd0c7-111">Provides centralized reporting and hardware management with Microsoft System Center Configuration Manager.</span></span>

-   <span data-ttu-id="dd0c7-112">Сокращает рабочую нагрузку на службу поддержки, чтобы помочь конечным пользователям использовать ПИН-код BitLocker и ключи восстановления.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-112">Reduces the workload on the Help Desk to assist end users with BitLocker PIN and recovery key requests.</span></span>

-   <span data-ttu-id="dd0c7-113">позволяет конечным пользователям восстанавливать зашифрованные устройства независимо, используя портал самообслуживания;</span><span class="sxs-lookup"><span data-stu-id="dd0c7-113">Enables end users to recover encrypted devices independently by using the Self-Service Portal.</span></span>

-   <span data-ttu-id="dd0c7-114">Позволяет подвергать аудиту безопасности доступ к восстановлению сведений о ключе.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-114">Enables security officers to easily audit access to recover key information.</span></span>

-   <span data-ttu-id="dd0c7-115">позволяет пользователям Windows Корпоративная продолжать работать в любом месте, не беспокоясь о защите данных организации;</span><span class="sxs-lookup"><span data-stu-id="dd0c7-115">Empowers Windows Enterprise users to continue working anywhere with the assurance that their corporate data is protected.</span></span>

<span data-ttu-id="dd0c7-116">MBAM применяет параметры политики шифрования BitLocker, заданные для Организации, отслеживает соответствие клиентских компьютеров этим политикам и сообщает о состоянии шифрования компьютеров предприятия и индивидуальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-116">MBAM enforces the BitLocker encryption policy options that you set for your enterprise, monitors the compliance of client computers with those policies, and reports on the encryption status of the enterprise’s and individual’s computers.</span></span> <span data-ttu-id="dd0c7-117">Кроме того, MBAM позволяет получить доступ к сведениям о ключе восстановления, когда пользователь забыл свой PIN-код или пароль, а также при изменении BIOS или загрузочных записей.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-117">In addition, MBAM lets you access the recovery key information when users forget their PIN or password, or when their BIOS or boot records change.</span></span>

<span data-ttu-id="dd0c7-118">Управление BitLocker может заинтересовать следующие группы: MBAM</span><span class="sxs-lookup"><span data-stu-id="dd0c7-118">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="dd0c7-119">Администраторы, ИТ-специалисты и руководителей соответствия требованиям, ответственные за обеспечение того, что конфиденциальные данные не будут закрыты без авторизации.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-119">Administrators, IT security professionals, and compliance officers who are responsible for ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="dd0c7-120">Администраторы, ответственные за безопасность компьютеров в удаленных и филиалах</span><span class="sxs-lookup"><span data-stu-id="dd0c7-120">Administrators who are responsible for computer security in remote or branch offices</span></span>

-   <span data-ttu-id="dd0c7-121">Администраторы, ответственные за клиентские компьютеры под управлением Windows</span><span class="sxs-lookup"><span data-stu-id="dd0c7-121">Administrators who are responsible for client computers that are running Windows</span></span>

<span data-ttu-id="dd0c7-122">**Примечание**  BitLocker не подробно описан в этой MBAM документации.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-122">**Note** BitLocker is not explained in detail in this MBAM documentation.</span></span> <span data-ttu-id="dd0c7-123">Дополнительные сведения можно найти в разделе [Обзор шифрования диска BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-123">For more information, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

## <a href="" id="what-s-new-in-mbam-2-5"></a><span data-ttu-id="dd0c7-124">Новые возможности MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="dd0c7-124">What’s new in MBAM 2.5</span></span>


<span data-ttu-id="dd0c7-125">В этом разделе описаны новые возможности в MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-125">This section describes the new features in MBAM 2.5.</span></span>

### <span data-ttu-id="dd0c7-126">Поддержка Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="dd0c7-126">Support for Microsoft SQL Server 2014</span></span>

<span data-ttu-id="dd0c7-127">MBAM добавляет поддержку для Microsoft SQL Server 2014 в дополнение к тому же программному обеспечению, которое поддерживается в более ранних версиях MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-127">MBAM adds support for Microsoft SQL Server 2014, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

### <a href="" id="-------------mbam-group-policy-templates-downloaded-separately"></a> <span data-ttu-id="dd0c7-128">Шаблоны групповой политики MBAM скачаны отдельно</span><span class="sxs-lookup"><span data-stu-id="dd0c7-128">MBAM Group Policy Templates downloaded separately</span></span>

<span data-ttu-id="dd0c7-129">Шаблоны групповой политики MBAM должны быть загружены отдельно из установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-129">The MBAM Group Policy Templates must be downloaded separately from the MBAM installation.</span></span> <span data-ttu-id="dd0c7-130">В предыдущих версиях MBAM установщик MBAM включил шаблон политики MBAM, который содержал необходимые MBAM объекты групповой политики (GPO), которые определяют параметры MBAM реализации для шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-130">In previous versions of MBAM, the MBAM installer included an MBAM Policy Template, which contained the required MBAM-specific Group Policy Objects (GPOs) that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="dd0c7-131">Эти GPO были удалены из MBAM установщика.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-131">These GPOs have been removed from the MBAM installer.</span></span> <span data-ttu-id="dd0c7-132">Теперь вы можете скачать объекты групповой [политики (ADMX)](https://go.microsoft.com/fwlink/p/?LinkId=393941) и скопировать их на сервер или рабочую станцию, прежде чем приступить к установке клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-132">You now download the GPOs from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation before you begin the MBAM Client installation.</span></span> <span data-ttu-id="dd0c7-133">Вы можете скопировать шаблоны групповой политики на любой сервер или рабочую станцию, на которой работает поддерживаемая версия операционной системы Windows Server или Windows.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-133">You can copy the Group Policy Templates to any server or workstation that is running a supported version of the Windows Server or Windows operating system.</span></span>

<span data-ttu-id="dd0c7-134">**Важно!**  Не изменяйте параметры групповой политики в разделе " **Шифрование диска BitLocker** " или MBAM будут работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-134">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="dd0c7-135">При настройке параметров групповой политики на узле **MDOP MBAM (Управление BitLocker)** MBAM автоматически настраивает параметры шифрования диска для BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-135">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the BitLocker Drive Encryption settings for you.</span></span>

 

<span data-ttu-id="dd0c7-136">Файлы шаблонов, которые необходимо скопировать на сервер или на рабочую станцию:</span><span class="sxs-lookup"><span data-stu-id="dd0c7-136">The template files that you need to copy to a server or workstation are:</span></span>

-   <span data-ttu-id="dd0c7-137">BitLockerManagement. ADML</span><span class="sxs-lookup"><span data-stu-id="dd0c7-137">BitLockerManagement.adml</span></span>

-   <span data-ttu-id="dd0c7-138">BitLockerManagement. ADMX</span><span class="sxs-lookup"><span data-stu-id="dd0c7-138">BitLockerManagement.admx</span></span>

-   <span data-ttu-id="dd0c7-139">BitLockerUserManagement. ADML</span><span class="sxs-lookup"><span data-stu-id="dd0c7-139">BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="dd0c7-140">BitLockerUserManagement. ADMX</span><span class="sxs-lookup"><span data-stu-id="dd0c7-140">BitLockerUserManagement.admx</span></span>

<span data-ttu-id="dd0c7-141">Скопируйте файлы шаблонов в то место, которое наилучшим образом соответствует вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-141">Copy the template files to the location that best meets your needs.</span></span> <span data-ttu-id="dd0c7-142">Для файлов, относящихся к определенному языку, которые необходимо скопировать в папку для определенного языка, для просмотра файлов требуется консоль управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-142">For the language-specific files, which must be copied to a language-specific folder, the Group Policy Management Console is required to view the files.</span></span>

- <span data-ttu-id="dd0c7-143">Чтобы установить файлы шаблонов локально на сервер или рабочую станцию, скопируйте их в одно из указанных ниже расположений.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-143">To install the template files locally on a server or workstation, copy the files to one of the following locations.</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left"><span data-ttu-id="dd0c7-144">Тип файла</span><span class="sxs-lookup"><span data-stu-id="dd0c7-144">File type</span></span></th>
  <th align="left"><span data-ttu-id="dd0c7-145">Расположение файла</span><span class="sxs-lookup"><span data-stu-id="dd0c7-145">File location</span></span></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="dd0c7-146">язык, не зависящий от языка (ADMX)</span><span class="sxs-lookup"><span data-stu-id="dd0c7-146">language neutral (.admx)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="dd0c7-147">% SystemRoot% </em> \policyDefinitions</span><span class="sxs-lookup"><span data-stu-id="dd0c7-147">%systemroot%</em>\policyDefinitions</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="dd0c7-148">специфичный для определенного языка (ADML)</span><span class="sxs-lookup"><span data-stu-id="dd0c7-148">language specific (.adml)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="dd0c7-149">% SystemRoot% </em> \policyDefinitions [ <em> MUIculture </em> ] (например, файл в формате для английского языка (США) будет храниться в <em> каталоге% systemroot% &lt; /EM &gt; policyDefinitions\en-US)</span><span class="sxs-lookup"><span data-stu-id="dd0c7-149">%systemroot%</em>\policyDefinitions[<em>MUIculture</em>] (for example, the U.S. English language specific file will be stored in <em>%systemroot%&lt;/em&gt;policyDefinitions\en-us)</span></span></p></td>
  </tr>
  </tbody>
  </table>

     

- <span data-ttu-id="dd0c7-150">Чтобы шаблоны были доступны всем администраторам групповых политик в домене, скопируйте файлы в одно из указанных ниже расположений на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-150">To make the templates available to all Group Policy administrators in a domain, copy the files to one of the following locations on a domain controller.</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left"><span data-ttu-id="dd0c7-151">Тип файла</span><span class="sxs-lookup"><span data-stu-id="dd0c7-151">File type</span></span></th>
  <th align="left"><span data-ttu-id="dd0c7-152">Расположение файла контроллера домена</span><span class="sxs-lookup"><span data-stu-id="dd0c7-152">Domain controller file location</span></span></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="dd0c7-153">Язык, не зависящий от языка (ADMX)</span><span class="sxs-lookup"><span data-stu-id="dd0c7-153">Language neutral (.admx)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="dd0c7-154">% SystemRoot% </em> sysvol\domain\policies\PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="dd0c7-154">%systemroot%</em>sysvol\domain\policies\PolicyDefinitions</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="dd0c7-155">Специфичный для определенного языка (ADML)</span><span class="sxs-lookup"><span data-stu-id="dd0c7-155">Language specific (.adml)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="dd0c7-156">% SystemRoot% </em> \sysvol\domain\policies\PolicyDefinitions [ <em> MUIculture </em> ] (например, файл, зависящий от английского языка, будет храниться в <em> папке% systemroot% </em> \sysvol\domain\policies\PolicyDefinitions\en-US)</span><span class="sxs-lookup"><span data-stu-id="dd0c7-156">%systemroot%</em>\sysvol\domain\policies\PolicyDefinitions[<em>MUIculture</em>] (for example, the U.S. English language-specific file will be stored in <em>%systemroot%</em>\sysvol\domain\policies\PolicyDefinitions\en-us)</span></span></p></td>
  </tr>
  </tbody>
  </table>

     

<span data-ttu-id="dd0c7-157">Дополнительные сведения о файлах шаблонов можно найти [в статье Управление файлами ADMX с](https://go.microsoft.com/fwlink/?LinkId=392818)пошаговыми инструкциями.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-157">For more information about template files, see [Managing Group Policy ADMX Files Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=392818).</span></span>

### <span data-ttu-id="dd0c7-158">Возможность применять политики шифрования для операционной системы и несъемных дисков с данными</span><span class="sxs-lookup"><span data-stu-id="dd0c7-158">Ability to enforce encryption policies on operating system and fixed data drives</span></span>

<span data-ttu-id="dd0c7-159">MBAM 2.5 позволяет применять политики шифрования на операционных системах и фиксированных дисках с данными для компьютеров в вашей организации, а также ограничивать количество дней, в течение которых конечные пользователи могут запрашивать отсрочку требования для обеспечения соответствия требованиям политик шифрования MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-159">MBAM2.5 enables you to enforce encryption policies on operating system and fixed data drives for computers in your organization and limit the number of days that end users can request a postponement of the requirement to comply with MBAM encryption policies.</span></span>

<span data-ttu-id="dd0c7-160">Чтобы включить настройку принудительного применения политики шифрования, для дисков операционной системы и несъемных дисков с данными была добавлена новая настройка групповой политики, называемая параметрами применения политики шифрования.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-160">To enable you to configure encryption policy enforcement, a new Group Policy setting, called Encryption Policy Enforcement Settings, has been added for operating system drives and fixed data drives.</span></span> <span data-ttu-id="dd0c7-161">Эта политика описана в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-161">This policy is described in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dd0c7-162">Параметр групповой политики</span><span class="sxs-lookup"><span data-stu-id="dd0c7-162">Group Policy setting</span></span></th>
<th align="left"><span data-ttu-id="dd0c7-163">Описание</span><span class="sxs-lookup"><span data-stu-id="dd0c7-163">Description</span></span></th>
<th align="left"><span data-ttu-id="dd0c7-164">Узел групповой политики, используемый для настройки этого параметра</span><span class="sxs-lookup"><span data-stu-id="dd0c7-164">Group Policy node used to configure this setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd0c7-165">Параметры применения политики шифрования (диск операционной системы)</span><span class="sxs-lookup"><span data-stu-id="dd0c7-165">Encryption Policy Enforcement Settings (Operating System Drive)</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd0c7-166">Для этого параметра с помощью параметра <strong> Настройте количество дней льготного периода несоответствия для дисков операционной системы </strong> , чтобы настроить льготный период.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-166">For this setting, use the option <strong>Configure the number of noncompliance grace period days for operating system drives</strong> to configure a grace period.</span></span></p>
<p><span data-ttu-id="dd0c7-167">Льготный период определяет количество дней, в течение которых конечные пользователи могут откладывать соответствие требованиям с помощью политик MBAM для жесткого диска операционной системы после того, как диск впервые обнаружен как несоответствующий.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-167">The grace period specifies the number of days that end users can postpone compliance with MBAM policies for their operating system drive after the drive is first detected as noncompliant.</span></span></p>
<p><span data-ttu-id="dd0c7-168">По истечении настроенного льготного периода пользователи не могут откладывать необходимые действия или запрашивать исключение от него.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-168">After the configured grace period expires, users cannot postpone the required action or request an exemption from it.</span></span></p>
<p><span data-ttu-id="dd0c7-169">Если требуется вмешательство пользователя (например, при использовании доверенного платформенного модуля (TPM) + PIN-кода или с помощью предохранителя пароля), появится диалоговое окно, и пользователи не смогут закрыть его, пока не предоставит нужные сведения.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-169">If user interaction is required (for example, if you are using the Trusted Platform Module (TPM) + PIN or using a password protector), a dialog box appears, and users cannot close it until they provide the required information.</span></span> <span data-ttu-id="dd0c7-170">Если предохранитель является исключительно TPM, шифрование начинается немедленно в фоновом режиме без ввода данных пользователем.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-170">If the protector is TPM only, encryption begins immediately in the background without user input.</span></span></p>
<p><span data-ttu-id="dd0c7-171">Пользователи не могут запрашивать исключения с помощью мастера шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-171">Users cannot request exemptions through the BitLocker encryption wizard.</span></span> <span data-ttu-id="dd0c7-172">Вместо этого они должны обратиться в службу технической поддержки или использовать любой процесс, используемый их организациями для запросов на освобождение.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-172">Instead, they must contact their Help Desk or use whatever process their organization uses for exemption requests.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd0c7-173">Политики конфигурации компьютера: &gt; &gt; Административные шаблоны &gt; компоненты &gt; Windows MDOP MBAM (Управление BitLocker) &gt; диск операционной системы</span><span class="sxs-lookup"><span data-stu-id="dd0c7-173">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; Windows Components &gt; MDOP MBAM (BitLocker Management) &gt; Operating System Drive</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dd0c7-174">Параметры принудительного применения политики шифрования (несъемные диски с данными)</span><span class="sxs-lookup"><span data-stu-id="dd0c7-174">Encryption Policy Enforcement Settings (Fixed Data Drives)</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd0c7-175">Для этого параметра с помощью параметра <strong> Настройте количество дней льготного периода несоответствия для фиксированных дисков </strong> , чтобы настроить льготный период.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-175">For this setting, use the option <strong>Configure the number of noncompliance grace period days for fixed drives</strong> to configure a grace period.</span></span></p>
<p><span data-ttu-id="dd0c7-176">Льготный период определяет количество дней, в течение которых конечные пользователи могут откладывать соответствие требованиям с помощью политик MBAM для фиксированных дисков, после того как диск впервые обнаружен как несоответствующий.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-176">The grace period specifies the number of days that end users can postpone compliance with MBAM policies for their fixed drive after the drive is first detected as noncompliant.</span></span></p>
<p><span data-ttu-id="dd0c7-177">Льготный период начинается, когда фиксированный диск определен как несоответствующий.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-177">The grace period begins when the fixed drive is determined to be noncompliant.</span></span> <span data-ttu-id="dd0c7-178">Если вы используете автоматическое снятие блокировки, политика не будет применяться, пока диск операционной системы не станет совместимым.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-178">If you are using auto-unlock, the policy will not be enforced until the operating system drive is compliant.</span></span> <span data-ttu-id="dd0c7-179">Тем не менее, если вы не используете автоматическое снятие блокировки, шифрование фиксированного диска с данными может начаться, прежде чем диск операционной системы полностью шифруется.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-179">However, if you are not using auto-unlock, encryption of the fixed data drive can begin before the operating system drive is fully encrypted.</span></span></p>
<p><span data-ttu-id="dd0c7-180">По истечении настроенного льготного периода пользователи не могут откладывать необходимые действия или запрашивать исключение от него.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-180">After the configured grace period expires, users cannot postpone the required action or request an exemption from it.</span></span> <span data-ttu-id="dd0c7-181">Если требуется вмешательство пользователя, появится диалоговое окно, и пользователи не смогут закрыть его, пока он не предоставит нужные сведения.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-181">If user interaction is required, a dialog box appears and users cannot close it until they provide the required information.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd0c7-182">Политики конфигурации компьютера: &gt; &gt; Административные шаблоны &gt; компоненты Windows &gt; MBAM (Управление BitLocker) &gt; съемный диск</span><span class="sxs-lookup"><span data-stu-id="dd0c7-182">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; Windows Components &gt; MDOP MBAM (BitLocker Management) &gt; Fixed Drive</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="dd0c7-183">Возможность предоставления URL-адреса в мастере шифрования диска BitLocker для указания на политику безопасности</span><span class="sxs-lookup"><span data-stu-id="dd0c7-183">Ability to provide a URL in the BitLocker Drive Encryption wizard to point to your security policy</span></span>

<span data-ttu-id="dd0c7-184">Новый параметр групповой политики: **URL-адрес ссылки на политику безопасности**позволяет настроить URL-адрес, который будет использоваться для конечных пользователей в качестве ссылки, которая называется **политикой безопасности компании**.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-184">A new Group Policy setting, **Provide the URL for the Security Policy link**, enables you to configure a URL that will be presented to end users as a link called **Company Security Policy**.</span></span> <span data-ttu-id="dd0c7-185">Эта ссылка появится в том случае, если MBAM предложит пользователям зашифровать том.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-185">This link will appear when MBAM prompts users to encrypt a volume.</span></span>

<span data-ttu-id="dd0c7-186">Если вы включаете этот параметр политики, вы можете настроить URL-адрес ссылки на **политику безопасности компании** .</span><span class="sxs-lookup"><span data-stu-id="dd0c7-186">If you enable this policy setting, you can configure the URL for the **Company Security Policy** link.</span></span> <span data-ttu-id="dd0c7-187">Если вы отключаете или не настраиваете этот параметр политики, ссылка " **Политика безопасности Организации** " не отображается для пользователей.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-187">If you disable or do not configure this policy setting, the **Company Security Policy** link is not displayed to users.</span></span>

<span data-ttu-id="dd0c7-188">Параметр "Новая групповая политика" находится на следующем узле GPO: **политики конфигурации компьютера** . &gt; **Policies** &gt; **Административные шаблоны** &gt; **компоненты Windows** &gt; **MBAM (Управление BitLocker) &gt; MDOP**.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-188">The new Group Policy setting is located in the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management) &gt; Client Management**.</span></span>

### <span data-ttu-id="dd0c7-189">Поддержка ключей восстановления, совместимых с FIPS</span><span class="sxs-lookup"><span data-stu-id="dd0c7-189">Support for FIPS-compliant recovery keys</span></span>

<span data-ttu-id="dd0c7-190">MBAM 2.5 поддерживает ключи восстановления, совместимые со стандартом FIPS, на устройствах под управлением операционной системы Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-190">MBAM2.5 supports Federal Information Processing Standard (FIPS)-compliant BitLocker recovery keys on devices that are running the Windows8.1 operating system.</span></span> <span data-ttu-id="dd0c7-191">Ключ восстановления не соответствует требованиям FIPS в более ранних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-191">The recovery key was not FIPS compliant in earlier versions of Windows.</span></span> <span data-ttu-id="dd0c7-192">Это расширение улучшает процесс восстановления диска в организациях, требующих соответствия требованиям FIPS, так как позволяет конечным пользователям использовать портал самообслуживания и веб-сайт администрирования и наблюдения (служба поддержки) для восстановления дисков в случае утери ПИН-кода или пароля, а также для блокировки компьютеров.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-192">This enhancement improves the drive recovery process in organizations that require FIPS compliance because it enables end users to use the Self-Service Portal or Administration and Monitoring Website (Help Desk) to recover their drives if they forget their PIN or password or get locked out of their computers.</span></span> <span data-ttu-id="dd0c7-193">Новая функция соответствия требованиям FIPS не распространяется на предохранители пароля.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-193">The new FIPS compliance feature does not extend to password protectors.</span></span>

<span data-ttu-id="dd0c7-194">Чтобы включить соответствие требованиям FIPS в вашей организации, необходимо настроить параметры групповой политики для федеральной обработки информации (FIPS).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-194">To enable FIPS compliance in your organization, you must configure the Federal Information Processing Standard (FIPS) Group Policy settings.</span></span> <span data-ttu-id="dd0c7-195">Инструкции по настройке можно найти в разделе [Параметры групповой политики BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-195">For configuration instructions, see [BitLocker Group Policy Settings](https://go.microsoft.com/fwlink/?LinkId=393560).</span></span>

<span data-ttu-id="dd0c7-196">Для клиентских компьютеров, использующих операционные системы Windows8 или Windows7 без [установленного исправления BitLocker](https://support.microsoft.com/kb/3015477), ИТ-администраторы продолжат использовать предохранитель агента восстановления данных (DRA) в средах, совместимых с FIPS.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-196">For client computers that are running the Windows8 or Windows7 operating systems without the [installed BitLocker hotfix](https://support.microsoft.com/kb/3015477), IT administrators will continue to use the Data Recovery Agents (DRA) protector in FIPS-compliant environments.</span></span> <span data-ttu-id="dd0c7-197">Сведения о DRA см. в разделе [использование агентов восстановления данных с помощью BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-197">For information about DRA, see [Using Data Recovery Agents with BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span></span>

<span data-ttu-id="dd0c7-198">Чтобы скачать и установить исправление BitLocker для Windows 7 и Windows 8, ознакомьтесь с [пакетом исправлений 2 для администрирования BitLocker и мониторинга 2,5](https://support.microsoft.com/kb/3015477) .</span><span class="sxs-lookup"><span data-stu-id="dd0c7-198">See [Hotfix Package 2 for BitLocker Administration and Monitoring 2.5](https://support.microsoft.com/kb/3015477) to download and install the BitLocker hotfix for Windows 7 and Windows 8 computers.</span></span>

### <span data-ttu-id="dd0c7-199">Поддержка развертываний с высокой степенью доступности</span><span class="sxs-lookup"><span data-stu-id="dd0c7-199">Support for high availability deployments</span></span>

<span data-ttu-id="dd0c7-200">MBAM поддерживает следующие сценарии высокой доступности в дополнение к стандартным топологиям интеграции двух серверов и Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="dd0c7-200">MBAM supports the following high-availability scenarios in addition to the standard two-server and Configuration Manager Integration topologies:</span></span>

-   <span data-ttu-id="dd0c7-201">Группы доступности SQL Server AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="dd0c7-201">SQL Server AlwaysOn availability groups</span></span>

-   <span data-ttu-id="dd0c7-202">Кластеризация SQL Server</span><span class="sxs-lookup"><span data-stu-id="dd0c7-202">SQL Server clustering</span></span>

-   <span data-ttu-id="dd0c7-203">Балансировка сетевой нагрузки (NLB)</span><span class="sxs-lookup"><span data-stu-id="dd0c7-203">Network load balancing (NLB)</span></span>

-   <span data-ttu-id="dd0c7-204">Зеркальное отображение SQL Server</span><span class="sxs-lookup"><span data-stu-id="dd0c7-204">SQL Server mirroring</span></span>

-   <span data-ttu-id="dd0c7-205">Резервное копирование службы теневого копирования тома (VSS)</span><span class="sxs-lookup"><span data-stu-id="dd0c7-205">Volume Shadow Copy Service (VSS) Backup</span></span>

<span data-ttu-id="dd0c7-206">Подробнее об этих функциях смотрите в разделе [планирование MBAM 2,5 высокой доступности](planning-for-mbam-25-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-206">For more information about these features, see [Planning for MBAM 2.5 High Availability](planning-for-mbam-25-high-availability.md).</span></span>

### <a href="" id="management-of-roles-for-administration-and-monitoring-website-changed-"></a><span data-ttu-id="dd0c7-207">Изменилось управление ролями для администрирования и веб-сайта наблюдения</span><span class="sxs-lookup"><span data-stu-id="dd0c7-207">Management of roles for Administration and Monitoring Website changed</span></span>

<span data-ttu-id="dd0c7-208">В MBAM 2.5 для управления ролями, которые предоставляют права доступа к веб-сайту администрирования и мониторинга, необходимо создать группы безопасности в доменных службах Active Directory (ADDS).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-208">In MBAM2.5, you must create security groups in Active Directory Domain Services (ADDS) to manage the roles that provide access rights to the Administration and Monitoring Website.</span></span> <span data-ttu-id="dd0c7-209">Роли позволяют пользователям, которые относятся к определенным группам безопасности, выполнять различные задачи на веб-сайте, например просматривать отчеты или помогать пользователям восстанавливать зашифрованные диски.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-209">Roles enable users who are in specific security groups to perform different tasks in the website such as viewing reports or helping end users recover encrypted drives.</span></span> <span data-ttu-id="dd0c7-210">В предыдущих версиях MBAM для управления ролями использовалась локальная группа.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-210">In previous versions of MBAM, roles were managed by using local groups.</span></span>

<span data-ttu-id="dd0c7-211">В MBAM 2.5 термин "роли" заменяет термин "роли администратора", который использовался в более ранних версиях MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-211">In MBAM2.5, the term “roles” replaces the term “administrator roles,” which was used in earlier versions of MBAM.</span></span> <span data-ttu-id="dd0c7-212">Кроме того, в MBAM 2.5 роль "Администраторы системы" была удалена.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-212">In addition, in MBAM2.5 the “MBAM System Administrators” role has been removed.</span></span>

<span data-ttu-id="dd0c7-213">В следующей таблице перечислены группы безопасности, которые необходимо создать в доменных СЛУЖБах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-213">The following table lists the security groups that you must create in AD DS.</span></span> <span data-ttu-id="dd0c7-214">Вы можете использовать любое имя для групп безопасности.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-214">You can use any name for the security groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dd0c7-215">Роль</span><span class="sxs-lookup"><span data-stu-id="dd0c7-215">Role</span></span></th>
<th align="left"><span data-ttu-id="dd0c7-216">Права доступа для этой роли на веб-сайте администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="dd0c7-216">Access rights for this role on the Administration and Monitoring Website</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd0c7-217">Пользователи службы поддержки MBAM</span><span class="sxs-lookup"><span data-stu-id="dd0c7-217">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd0c7-218">Предоставляет доступ к разделу Управление областями восстановления доверенных платформенных устройств и дисков на веб-сайте администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-218">Provides access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="dd0c7-219">Пользователи, у которых есть доступ к этим областям, должны заполнить все поля при использовании любой области.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-219">Users who have access to these areas must fill in all fields when they use either area.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dd0c7-220">Пользователи отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="dd0c7-220">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd0c7-221">Предоставляет доступ к отчетам на веб-сайте администрирования и наблюдения.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-221">Provides access to the Reports in the Administration and Monitoring Website.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd0c7-222">MBAM опытных пользователей службы поддержки</span><span class="sxs-lookup"><span data-stu-id="dd0c7-222">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd0c7-223">Предоставляет доступ ко всем областям на веб-сайте администрирования и наблюдения.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-223">Provides access to all areas in the Administration and Monitoring Website.</span></span> <span data-ttu-id="dd0c7-224">Пользователи в этой группе должны вводить только ключ восстановления, а не домен и имя пользователя конечного пользователя, при помощи которых пользователи будут восстанавливать свои диски.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-224">Users in this group have to enter only the recovery key, not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="dd0c7-225">Если пользователь является членом группы "Пользователи службы поддержки MBAM" и "Пользователи расширенной справочной службы MBAM", то разрешения группы "Пользователи расширенной справочной службы" переопределяют разрешения на доступ к группе "MBAM" для пользователей службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-225">If a user is a member of the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users group permissions.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="dd0c7-226">После создания групп безопасности в разделе "Добавление" Назначьте пользователям и (или) группам соответствующую группу безопасности, чтобы обеспечить соответствующий уровень доступа к веб-сайту администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-226">After you create the security groups in ADDS, assign users and/or groups to the appropriate security group to enable the corresponding level of access to the Administration and Monitoring Website.</span></span> <span data-ttu-id="dd0c7-227">Чтобы разрешить отдельным пользователям ролей доступ к веб-сайту администрирования и наблюдения, необходимо также указать каждую группу безопасности при настройке веб-сайта администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-227">To enable individuals with each role to access the Administration and Monitoring Website, you must also specify each security group when you are configuring the Administration and Monitoring Website.</span></span>

### <span data-ttu-id="dd0c7-228">Командлеты Windows PowerShell для настройки функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="dd0c7-228">Windows PowerShell cmdlets for configuring MBAM Server features</span></span>

<span data-ttu-id="dd0c7-229">Командлеты Windows PowerShell для MBAM 2.5 позволяют настраивать и управлять функциями сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-229">Windows PowerShell cmdlets for MBAM2.5 enable you to configure and manage the MBAM Server features.</span></span> <span data-ttu-id="dd0c7-230">Каждый компонент имеет соответствующий командлет Windows PowerShell, который можно использовать для включения или отключения функций, а также для получения сведений о компоненте.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-230">Each feature has a corresponding Windows PowerShell cmdlet that you can use to enable or disable features, or to get information about the feature.</span></span>

<span data-ttu-id="dd0c7-231">Необходимые условия и необходимые условия для использования Windows PowerShell приведены в разделе [Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-231">For prerequisites and prerequisites for using Windows PowerShell, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

**<span data-ttu-id="dd0c7-232">Загрузка справки по MBAM 2,5 для командлетов Windows PowerShell после установки серверного программного обеспечения MBAM</span><span class="sxs-lookup"><span data-stu-id="dd0c7-232">To load the MBAM 2.5 Help for Windows PowerShell cmdlets after installing the MBAM Server software</span></span>**

1.  <span data-ttu-id="dd0c7-233">Откройте Windows PowerShell или интегрированную среду сценариев Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-233">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="dd0c7-234">Введите **Update-Help-Module Microsoft. MBAM**.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-234">Type **Update-Help –Module Microsoft.MBAM**.</span></span>

<span data-ttu-id="dd0c7-235">Справка по Windows PowerShell для MBAM доступна в следующих форматах:</span><span class="sxs-lookup"><span data-stu-id="dd0c7-235">Windows PowerShell Help for MBAM is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dd0c7-236">Формат справки Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dd0c7-236">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="dd0c7-237">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="dd0c7-237">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd0c7-238">В командной строке Windows PowerShell введите <strong> </strong> &lt; <em> командлет Get-Help</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="dd0c7-238">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd0c7-239">Чтобы загрузить последние командлеты Windows PowerShell, следуйте инструкциям, приведенным в предыдущем разделе о том, как загрузить справку Windows PowerShell для MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-239">To upload the latest Windows PowerShell cmdlets, follow the instructions in the previous section on how to load Windows PowerShell Help for MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dd0c7-240">На веб-страницах TechNet.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-240">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd0c7-241">В центре загрузки как файл Word. docx</span><span class="sxs-lookup"><span data-stu-id="dd0c7-241">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dd0c7-242">В центре загрузки в виде PDF-файла</span><span class="sxs-lookup"><span data-stu-id="dd0c7-242">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="dd0c7-243">Поддержка ПИН-кодов и расширенных контактов и возможность предотвращения последовательного и повторяющегося символа</span><span class="sxs-lookup"><span data-stu-id="dd0c7-243">Support for ASCII-only and enhanced PINs and ability to prevent sequential and repeating characters</span></span>

**<span data-ttu-id="dd0c7-244">Разрешить расширенные контакты для параметра групповой политики автозагрузки</span><span class="sxs-lookup"><span data-stu-id="dd0c7-244">Allow enhanced PINs for startup Group Policy setting</span></span>**

<span data-ttu-id="dd0c7-245">Параметр групповой политики, **разрешающий Расширенные ПИН-коды для запуска**, позволяет настроить использование расширенных ПИН-кодов при запуске BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-245">The Group Policy setting, **Allow enhanced PINs for startup**, enables you to configure whether enhanced startup PINs are used with BitLocker.</span></span> <span data-ttu-id="dd0c7-246">Улучшенные ПИН-коды запуска позволяют пользователям вводить клавиши на полных клавиатурах, в том числе прописные и строчные буквы, символы, цифры и пробелы.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-246">Enhanced startup PINs permit users to enter any keys on a full keyboard, including uppercase and lowercase letters, symbols, numbers, and spaces.</span></span> <span data-ttu-id="dd0c7-247">Если вы включаете этот параметр политики, все новые ПИН-коды запуска BitLocker, заданные в качестве контактов, будут расширены.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-247">If you enable this policy setting, all new BitLocker startup PINs that are set will be enhanced PINs.</span></span> <span data-ttu-id="dd0c7-248">Если вы отключаете или не настраиваете этот параметр политики, расширенные контакты использовать нельзя.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-248">If you disable or do not configure this policy setting, enhanced PINs cannot be used.</span></span>

<span data-ttu-id="dd0c7-249">Не все компьютеры поддерживают ввод расширенных контактов в среде предзагрузочной среды выполнения (PXE).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-249">Not all computers support the entry of enhanced PINs in the Pre-Boot Execution Environment (PXE).</span></span> <span data-ttu-id="dd0c7-250">Прежде чем включать этот параметр групповой политики для Организации, запустите проверку системы во время процесса настройки BitLocker, чтобы убедиться, что BIOS компьютера поддерживает использование полной клавиатуры в среде PXE.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-250">Before you enable this Group Policy setting for your organization, run a system check during the BitLocker setup process to ensure that the computer’s BIOS supports the use of the full keyboard in PXE.</span></span> <span data-ttu-id="dd0c7-251">Дополнительные сведения можно найти в разделе [Планирование требований к групповой политике MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-251">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

**<span data-ttu-id="dd0c7-252">Флажок "Запрашивать ПИН-коды только для ASCII"</span><span class="sxs-lookup"><span data-stu-id="dd0c7-252">Require ASCII-only PINs check box</span></span>**

<span data-ttu-id="dd0c7-253">Кроме того, параметр **Allowed Pins для** групповой политики автозагрузки включает в себя флажок **требовать ПИН-коды только для ASCII** .</span><span class="sxs-lookup"><span data-stu-id="dd0c7-253">The **Allow enhanced PINs for startup** Group Policy setting also contains a **Require ASCII-only PINs** check box.</span></span> <span data-ttu-id="dd0c7-254">Если компьютеры в вашей организации не поддерживают использование полной клавиатуры в PXE, вы можете включить параметр **Allowed Pins для** групповой политики, а затем установить флажок **требовать ввода ПИН-кодов только** для тех, для которых расширенные контакты должны использовать только печатаемые символы ASCII.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-254">If the computers in your organization do not support the use of the full keyboard in PXE, you can enable the **Allow enhanced PINs for startup** Group Policy setting, and then select the **Require ASCII-only PINs** check box to require that enhanced PINs use only printable ASCII characters.</span></span>

**<span data-ttu-id="dd0c7-255">Принудительное использование непоследовательных и неповторяющихся знаков</span><span class="sxs-lookup"><span data-stu-id="dd0c7-255">Enforced use of nonsequential and nonrepeating characters</span></span>**

<span data-ttu-id="dd0c7-256">MBAM 2.5 предотвращает создание контактных данных для конечных пользователей, состоящих из повторяющихся номеров (например, 1111) или последовательных номеров (например, 1234).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-256">MBAM2.5 prevents end users from creating PINs that consist of repeating numbers (such as 1111) or sequential numbers (such as 1234).</span></span> <span data-ttu-id="dd0c7-257">Если конечные пользователи пытаются ввести пароль с тремя или более повторяющимися или последовательными числами, мастер шифрования диска BitLocker отобразит сообщение об ошибке и не позволит пользователям вводить PIN-код с запрещенными символами.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-257">If end users try to enter a password that contains three or more repeating or sequential numbers, the Bitlocker Drive Encryption wizard displays an error message and prevents users from entering a PIN with the prohibited characters.</span></span>

### <span data-ttu-id="dd0c7-258">Добавление сертификата DRA в отчет о соответствии требованиям компьютера BitLocker</span><span class="sxs-lookup"><span data-stu-id="dd0c7-258">Addition of DRA Certificate to BitLocker Computer Compliance report</span></span>

<span data-ttu-id="dd0c7-259">Новый тип предохранителя, сертификат агента восстановления данных (DRA), добавлен в отчет о соответствии компьютера BitLocker в Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-259">A new protector type, the Data Recovery Agent (DRA) Certificate, has been added to the BitLocker Computer Compliance Report in Configuration Manager.</span></span> <span data-ttu-id="dd0c7-260">Этот тип предохранителя применим к дискам операционной системы и отображается в разделе **тома компьютера** в столбце **типы предохранителей** .</span><span class="sxs-lookup"><span data-stu-id="dd0c7-260">This protector type applies to operating system drives, and it appears in the **Computer Volume(s)** section in the **Protector Types** column.</span></span>

### <span data-ttu-id="dd0c7-261">Поддержка развертывания с несколькими лесами</span><span class="sxs-lookup"><span data-stu-id="dd0c7-261">Support for multi-forest support deployments</span></span>

<span data-ttu-id="dd0c7-262">MBAM 2,5 поддерживает следующие типы развертываний с несколькими лесами:</span><span class="sxs-lookup"><span data-stu-id="dd0c7-262">MBAM 2.5 supports the following types of multi-forest deployments:</span></span>

-   <span data-ttu-id="dd0c7-263">Один лес с одним доменом</span><span class="sxs-lookup"><span data-stu-id="dd0c7-263">Single forest with single domain</span></span>

-   <span data-ttu-id="dd0c7-264">Один лес с одним деревом и несколькими доменами</span><span class="sxs-lookup"><span data-stu-id="dd0c7-264">Single forest with a single tree and multiple domains</span></span>

-   <span data-ttu-id="dd0c7-265">Один лес с несколькими деревьями и непересекающимися пространствами имен</span><span class="sxs-lookup"><span data-stu-id="dd0c7-265">Single forest with multiple trees and disjoint namespaces</span></span>

-   <span data-ttu-id="dd0c7-266">Несколько лесов в топологии центрального леса</span><span class="sxs-lookup"><span data-stu-id="dd0c7-266">Multiple forests in a central forest topology</span></span>

-   <span data-ttu-id="dd0c7-267">Несколько лесов в топологии леса ресурсов</span><span class="sxs-lookup"><span data-stu-id="dd0c7-267">Multiple forests in a resource forest topology</span></span>

<span data-ttu-id="dd0c7-268">Не поддерживается миграция лесов (от одного до нескольких, с разными ресурсами в лесу и т. д.) или обновление или переход на предыдущую версию.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-268">There is no support for forest migration (going from single to multiple, multiple to single, resource to across the forest, etc.), or upgrade or downgrade.</span></span>

<span data-ttu-id="dd0c7-269">Для развертывания MBAM в нескольких лесах используются следующие требования:</span><span class="sxs-lookup"><span data-stu-id="dd0c7-269">The prerequisites for deploying MBAM in multi-forest deployments are:</span></span>

-   <span data-ttu-id="dd0c7-270">Лес должен работать на поддерживаемых версиях Windows Server.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-270">Forest must be running on supported versions of Windows Server.</span></span>

-   <span data-ttu-id="dd0c7-271">Требуется двухстороннее или одностороннее отношение доверия.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-271">A two-way or one-way trust is required.</span></span> <span data-ttu-id="dd0c7-272">Односторонние доверительные отношения требуют, чтобы домен сервера доверял домену клиента.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-272">One-way trusts require that the server’s domain trusts the client’s domain.</span></span> <span data-ttu-id="dd0c7-273">Другими словами, домен сервера указывает на домен клиента.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-273">In other words, the server’s domain is pointed at the client’s domain.</span></span>

### <span data-ttu-id="dd0c7-274">Поддержка зашифрованных жестких дисков в клиенте MBAM</span><span class="sxs-lookup"><span data-stu-id="dd0c7-274">MBAM Client support for Encrypted Hard Drives</span></span>

<span data-ttu-id="dd0c7-275">MBAM поддерживает BitLocker на зашифрованных жестких дисках, отвечающих требованиям к спецификации TCG для Opalis и стандарту IEEE 1667.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-275">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="dd0c7-276">Если на этих устройствах включена функция BitLocker, она будет создавать ключи и выполнять функции управления на зашифрованном диске.</span><span class="sxs-lookup"><span data-stu-id="dd0c7-276">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="dd0c7-277">Более подробную информацию вы видите на [жестком диске с шифрованием](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="dd0c7-277">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>

## <span data-ttu-id="dd0c7-278">Получение технологий для MDOP</span><span class="sxs-lookup"><span data-stu-id="dd0c7-278">How to Get MDOP Technologies</span></span>


<span data-ttu-id="dd0c7-279">MBAM является частью пакета оптимизации рабочего стола Майкрософт (MDOP).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-279">MBAM is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="dd0c7-280">MDOP является частью программы Software Assurance (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-280">MDOP is part of the Microsoft Software Assurance program.</span></span> <span data-ttu-id="dd0c7-281">Дополнительные сведения о программе Microsoft Software Assurance и о том, как приобрести MDOP, приведены в [статье как получить MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-281">For more information about the Microsoft Software Assurance program and how to acquire the MDOP, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <a href="" id="---------mbam-2-5-release-notes"></a> <span data-ttu-id="dd0c7-282">Заметки о выпуске MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="dd0c7-282">MBAM 2.5 Release Notes</span></span>


<span data-ttu-id="dd0c7-283">Чтобы получить дополнительные сведения и последние новости, не включенные в эту документацию, ознакомьтесь с [заметками о выпуске для MBAM 2,5](release-notes-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-283">For more information and late-breaking news that is not included in this documentation, see [Release Notes for MBAM 2.5](release-notes-for-mbam-25.md).</span></span>

## <span data-ttu-id="dd0c7-284">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="dd0c7-284">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="dd0c7-285">Отправьте свой отзыв [здесь](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-285">Send your feedback [here](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub).</span></span> 
- <span data-ttu-id="dd0c7-286">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="dd0c7-286">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="dd0c7-287">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="dd0c7-287">Related topics</span></span>


[<span data-ttu-id="dd0c7-288">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="dd0c7-288">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="dd0c7-289">Начало работы с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dd0c7-289">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

 

 





