---
title: Рекомендации по безопасности для UE-V 1.0
description: Рекомендации по безопасности для UE-V 1.0
author: dansimp
ms.assetid: c5cdf9ff-dc96-4491-98e9-0eada898ffe0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b503028ae327f92759fe0f64f33fe0cffc62b05c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823999"
---
# <span data-ttu-id="0a10c-103">Рекомендации по безопасности для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="0a10c-103">UE-V 1.0 Security Considerations</span></span>


<span data-ttu-id="0a10c-104">В этой статье содержится краткий обзор учетных записей и групп, файлов журналов и других вопросов, связанных с безопасностью, для Microsoft User Experience Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="0a10c-104">This topic contains a brief overview of accounts and groups, log files, and other security-related considerations for Microsoft User Experience Virtualization (UE-V).</span></span> <span data-ttu-id="0a10c-105">Чтобы получить дополнительные сведения, воспользуйтесь приведенными ниже ссылками.</span><span class="sxs-lookup"><span data-stu-id="0a10c-105">For more information, follow the links that are provided here.</span></span>

## <span data-ttu-id="0a10c-106">Рекомендации по безопасности для конфигурации UE-V</span><span class="sxs-lookup"><span data-stu-id="0a10c-106">Security considerations for UE-V configuration</span></span>


**<span data-ttu-id="0a10c-107">При создании общего доступа к хранилищу параметров Ограничьте доступ пользователей к общему доступу.</span><span class="sxs-lookup"><span data-stu-id="0a10c-107">When you create the settings storage share, limit the share access to users that need access.</span></span>**

<span data-ttu-id="0a10c-108">Так как пакеты параметров могут содержать персональные данные, необходимо соблюдать осторожность и защитить их.</span><span class="sxs-lookup"><span data-stu-id="0a10c-108">Because settings packages may contain personal information, you should take care to protect them as well as possible.</span></span> <span data-ttu-id="0a10c-109">Как правило, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="0a10c-109">In general, do the following:</span></span>

-   <span data-ttu-id="0a10c-110">Ограничьте общий доступ только для тех пользователей, которым нужен доступ.</span><span class="sxs-lookup"><span data-stu-id="0a10c-110">Restrict the share to only the users that need access.</span></span> <span data-ttu-id="0a10c-111">Создайте группу безопасности для пользователей с перенаправленными папками в определенном общем доступе и ограничьте доступ только для тех пользователей.</span><span class="sxs-lookup"><span data-stu-id="0a10c-111">Create a security group for users that have redirected folders on a particular share, and limit access to only those users.</span></span>

-   <span data-ttu-id="0a10c-112">После создания общего доступа Скройте общий доступ, указав $ после имени общего доступа.</span><span class="sxs-lookup"><span data-stu-id="0a10c-112">When you create the share, hide the share by putting a $ after the share name.</span></span> <span data-ttu-id="0a10c-113">Это приведет к скрытию общего доступа в обычных браузерах, и общий доступ не будет виден в окне Сетевое окружение.</span><span class="sxs-lookup"><span data-stu-id="0a10c-113">This will hide the share from casual browsers, and the share will not be visible in My Network Places.</span></span>

-   <span data-ttu-id="0a10c-114">Предоставление пользователям минимального количества необходимых разрешений.</span><span class="sxs-lookup"><span data-stu-id="0a10c-114">Only give users the minimum amount of permissions needed.</span></span> <span data-ttu-id="0a10c-115">Необходимые разрешения показаны в таблицах ниже.</span><span class="sxs-lookup"><span data-stu-id="0a10c-115">The permissions needed are shown in the tables below.</span></span>

    1.  <span data-ttu-id="0a10c-116">Установите следующие разрешения на уровне общего доступа (SMB) для папки "Настройка места хранения":</span><span class="sxs-lookup"><span data-stu-id="0a10c-116">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><span data-ttu-id="0a10c-117">Учетная запись пользователя</span><span class="sxs-lookup"><span data-stu-id="0a10c-117">User account</span></span></th>
        <th align="left"><span data-ttu-id="0a10c-118">Рекомендуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="0a10c-118">Recommended permissions</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="0a10c-119">Все пользователи</span><span class="sxs-lookup"><span data-stu-id="0a10c-119">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="0a10c-120">Нет разрешений</span><span class="sxs-lookup"><span data-stu-id="0a10c-120">No Permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="0a10c-121">Группа безопасности UE-V</span><span class="sxs-lookup"><span data-stu-id="0a10c-121">Security group of UE-V</span></span></p></td>
        <td align="left"><p><span data-ttu-id="0a10c-122">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="0a10c-122">Full Control</span></span></p></td>
        </tr>
        </tbody>
        </table>



~~~
2.  Set the following NTFS permissions for the settings storage location folder:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Folder</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Admins</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Security group of UE-V users</p></td>
    <td align="left"><p>List Folder/Read Data, Create Folders/Append Data</p></td>
    <td align="left"><p>This Folder Only</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>Remove all Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    </tbody>
    </table>



3.  Set the following share-level (SMB) permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommend permissions</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>Read Permission Levels</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Read/Write Permission Levels</p></td>
    </tr>
    </tbody>
    </table>



4.  Set the following NTFS permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Apply to</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>List Folder Contents and Read</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    </tbody>
    </table>
~~~



### <span data-ttu-id="0a10c-123">Использование серверов Windows Server 2003 или более поздних версий для размещения перенаправленных файловых ресурсов</span><span class="sxs-lookup"><span data-stu-id="0a10c-123">Use Windows Server 2003 or later servers to host redirected file shares</span></span>

<span data-ttu-id="0a10c-124">Файлы пакета параметров пользователя содержат персональные данные, которые передаются между клиентским компьютером и сервером, на котором хранятся пакеты параметров.</span><span class="sxs-lookup"><span data-stu-id="0a10c-124">User settings package files contain personal information that is transferred between the client computer and the server that stores the settings packages.</span></span> <span data-ttu-id="0a10c-125">По этой причине вы должны убедиться, что данные защищены при пересылке по сети.</span><span class="sxs-lookup"><span data-stu-id="0a10c-125">Because of this, you should ensure that the data is protected while it travels over the network.</span></span>

<span data-ttu-id="0a10c-126">Данные параметров пользователя уязвимы для этих потенциальных угроз: перехват данных по мере их появления в сети; изменения данных, передаваемых по сети; и подмена сервера, на котором размещены данные.</span><span class="sxs-lookup"><span data-stu-id="0a10c-126">User settings data is vulnerable to these potential threats: interception of the data as it passes over the network; tampering with the data as it passes over the network; and spoofing of the server that hosts the data.</span></span>

<span data-ttu-id="0a10c-127">Некоторые функции Windows Server 2003 и более поздних версий помогут защитить пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="0a10c-127">Several features of Windows Server 2003 and above can help to secure user data:</span></span>

-   <span data-ttu-id="0a10c-128">**Kerberos** — Стандартный на всех версиях Windows 2000 и windows Server 2003 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="0a10c-128">**Kerberos** - Kerberos is standard on all versions of Windows 2000 and Windows Server 2003 and later.</span></span> <span data-ttu-id="0a10c-129">Kerberos обеспечивает наивысший уровень безопасности сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a10c-129">Kerberos ensures the highest level of security to network resources.</span></span> <span data-ttu-id="0a10c-130">NTLM проверяет подлинность клиента; Kerberos проверяет подлинность сервера и клиента.</span><span class="sxs-lookup"><span data-stu-id="0a10c-130">NTLM authenticates the client only; Kerberos authenticates the server and the client.</span></span> <span data-ttu-id="0a10c-131">При использовании NTLM клиент не знает, является ли сервер допустимым.</span><span class="sxs-lookup"><span data-stu-id="0a10c-131">When NTLM is used, the client does not know whether the server is valid.</span></span> <span data-ttu-id="0a10c-132">Это особенно важно, если клиент обменивается личными файлами с сервером, как в случае с перемещаемыми профилями.</span><span class="sxs-lookup"><span data-stu-id="0a10c-132">This is particularly important if the client is exchanging personal files with the server, as is the case with Roaming Profiles.</span></span> <span data-ttu-id="0a10c-133">Протокол Kerberos обеспечивает более высокую безопасность, чем NTLM.</span><span class="sxs-lookup"><span data-stu-id="0a10c-133">Kerberos provides better security than NTLM.</span></span> <span data-ttu-id="0a10c-134">Протокол Kerberos недоступен в операционных системах Windows NT версии 4,0 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="0a10c-134">Kerberos is not available on Windows NT version 4.0 or earlier operating systems.</span></span>

-   <span data-ttu-id="0a10c-135">**IPSec** — протокол IP-безопасности (IPSec) обеспечивает проверку подлинности на уровне сети, целостность данных и шифрование.</span><span class="sxs-lookup"><span data-stu-id="0a10c-135">**IPsec** - The IP Security Protocol (IPsec) provides network-level authentication, data integrity, and encryption.</span></span> <span data-ttu-id="0a10c-136">IPsec обеспечивает следующее:</span><span class="sxs-lookup"><span data-stu-id="0a10c-136">IPsec ensures the following:</span></span>

    -   <span data-ttu-id="0a10c-137">Перемещаемые данные изменяются при изменении данных во время прохождения по пути.</span><span class="sxs-lookup"><span data-stu-id="0a10c-137">Roamed data is safe from data modification while en route.</span></span>

    -   <span data-ttu-id="0a10c-138">Перемещенные данные можно безопасно отсекать, просматривать и копировать.</span><span class="sxs-lookup"><span data-stu-id="0a10c-138">Roamed data is safe from interception, viewing, or copying.</span></span>

    -   <span data-ttu-id="0a10c-139">Перемещаемые данные безопасно получать от пользователей, не прошедших проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="0a10c-139">Roamed data is safe from being accessed by unauthenticated parties.</span></span>

-   <span data-ttu-id="0a10c-140">**Подписывание SMB** — протокол проверки подлинности сообщений сервера (SMB) поддерживает проверку подлинности, что предотвращает запуск активного сообщения и атаки "злоумышленник в середине".</span><span class="sxs-lookup"><span data-stu-id="0a10c-140">**SMB Signing** - The Server Message Block (SMB) authentication protocol supports message authentication which prevents active message and "man-in-the-middle" attacks.</span></span> <span data-ttu-id="0a10c-141">Подписывание SMB обеспечивает такую проверку подлинности, помещая цифровую подпись в каждый из протоколов SMB.</span><span class="sxs-lookup"><span data-stu-id="0a10c-141">SMB signing provides this authentication by placing a digital signature into each SMB.</span></span> <span data-ttu-id="0a10c-142">После этого цифровая подпись будет проверяться клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="0a10c-142">The digital signature is then verified by both the client and the server.</span></span> <span data-ttu-id="0a10c-143">Чтобы использовать подписывание SMB, необходимо сначала включить его или потребовать его для клиента SMB и сервера SMB.</span><span class="sxs-lookup"><span data-stu-id="0a10c-143">In order to use SMB signing, you must first either enable it or require it on both the SMB client and the SMB server.</span></span> <span data-ttu-id="0a10c-144">Обратите внимание, что при подписывании SMB накладывается снижение производительности.</span><span class="sxs-lookup"><span data-stu-id="0a10c-144">Note that the SMB signing imposes a performance penalty.</span></span> <span data-ttu-id="0a10c-145">Она не потребляет больше пропускной способности сети, но использует больше тактов ЦП на стороне клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="0a10c-145">It does not consume any more network bandwidth, but it uses more CPU cycles on the client and server side.</span></span>

### <span data-ttu-id="0a10c-146">Всегда используйте файловую систему NTFS для томов, содержащих данные пользователей.</span><span class="sxs-lookup"><span data-stu-id="0a10c-146">Always use the NTFS File system for volumes holding users data</span></span>

<span data-ttu-id="0a10c-147">Для наиболее безопасной конфигурации настройте серверы, на которых размещены файлы параметров UE-V, для использования файловой системы NTFS.</span><span class="sxs-lookup"><span data-stu-id="0a10c-147">For the most secure configuration, configure servers that host the UE-V settings files to use the NTFS File System.</span></span> <span data-ttu-id="0a10c-148">В отличие от файловой системы FAT, NTFS поддерживает избирательные списки управления доступом (DACL) и списки управления доступом системы (SACL).</span><span class="sxs-lookup"><span data-stu-id="0a10c-148">Unlike FAT, NTFS supports Discretionary access control lists (DACLs) and system access control lists (SACLs).</span></span> <span data-ttu-id="0a10c-149">Списки DACL и SACL управляют тем, кто может выполнять операции с файлом, а также события, которые будут запускать ведение журнала действий, выполняемых с файлом.</span><span class="sxs-lookup"><span data-stu-id="0a10c-149">DACLs and SACLs control who can perform operations on a file and what events will trigger the logging of actions performed on a file.</span></span>

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a><span data-ttu-id="0a10c-150">Не полагаться на шифрование EFS для шифрования файлов пользователей при передаче по сети</span><span class="sxs-lookup"><span data-stu-id="0a10c-150">Do not rely on EFS to encrypt users’ files when transmitted over the network</span></span>

<span data-ttu-id="0a10c-151">При использовании шифрованной файловой системы (EFS) для шифрования файлов на удаленном сервере зашифрованные данные не шифруются при передаче по сети; Оно шифруется только при сохранении на диске.</span><span class="sxs-lookup"><span data-stu-id="0a10c-151">When you use Encrypting File System (EFS) to encrypt files on a remote server, the encrypted data is not encrypted during transit over the network; It only becomes encrypted when stored on disk.</span></span>

<span data-ttu-id="0a10c-152">Исключением является тот момент, когда система включает IP-безопасность (IPsec) или веб-сайт для создания и управления версиями (WebDAV).</span><span class="sxs-lookup"><span data-stu-id="0a10c-152">The exceptions to this are when your system includes Internet Protocol security (IPsec) or Web Distributed Authoring and Versioning (WebDAV).</span></span> <span data-ttu-id="0a10c-153">IPsec шифрует данные при транспортировке в сети TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0a10c-153">IPsec encrypts data while it is transported over a TCP/IP network.</span></span> <span data-ttu-id="0a10c-154">Если файл зашифрован и не копируется в папку WebDAV на сервере, он останется зашифрованным во время передачи и хранится на сервере.</span><span class="sxs-lookup"><span data-stu-id="0a10c-154">If the file is encrypted before being copied or moved to a WebDAV folder on a server, it will remain encrypted during the transmission and while it is stored on the server.</span></span>

### <span data-ttu-id="0a10c-155">Шифрование кэша автономных файлов</span><span class="sxs-lookup"><span data-stu-id="0a10c-155">Encrypt the Offline Files cache</span></span>

<span data-ttu-id="0a10c-156">По умолчанию кэш автономных файлов защищен для разделов NTFS с помощью ACL, но шифрование кэша дополнительно повышает безопасность на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="0a10c-156">By default, the Offline Files cache is protected on NTFS partitions by ACLs, but encrypting the cache further enhances security on a local computer.</span></span> <span data-ttu-id="0a10c-157">По умолчанию кэш на локальном компьютере не зашифрован, поэтому любые зашифрованные файлы, кэшированные из сети, не будут зашифрованы на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="0a10c-157">By default, the cache on the local computer is not encrypted, so any encrypted files cached from the network will not be encrypted on the local computer.</span></span> <span data-ttu-id="0a10c-158">Это может представлять угрозу безопасности в некоторых средах.</span><span class="sxs-lookup"><span data-stu-id="0a10c-158">This may pose a security risk in some environments.</span></span>

<span data-ttu-id="0a10c-159">Если включено шифрование, все файлы в кэше автономных файлов шифруются.</span><span class="sxs-lookup"><span data-stu-id="0a10c-159">When encryption is enabled, all files in the Offline Files cache are encrypted.</span></span> <span data-ttu-id="0a10c-160">Сюда входит шифрование существующих файлов и файлов, которые были добавлены позже.</span><span class="sxs-lookup"><span data-stu-id="0a10c-160">This includes encrypting existing files as well as files that are added later.</span></span> <span data-ttu-id="0a10c-161">На локальном компьютере влияет кэшированная копия, но связанная с ней сетевая копия отсутствует.</span><span class="sxs-lookup"><span data-stu-id="0a10c-161">The cached copy on the local computer is affected, but the associated network copy is not.</span></span>

<span data-ttu-id="0a10c-162">Кэш можно зашифровать одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="0a10c-162">The cache can be encrypted in one of two ways:</span></span>

1.  <span data-ttu-id="0a10c-163">С помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="0a10c-163">Via Group Policy.</span></span> <span data-ttu-id="0a10c-164">-Включите параметр **шифрование кэша автономных файлов** , расположенный на компьютере Configuration\\Administrative Templates\\Network\\Offline Files в редакторе групповой политики.</span><span class="sxs-lookup"><span data-stu-id="0a10c-164">- Enable the **Encrypt the Offline Files Cache** setting, located at Computer Configuration\\Administrative Templates\\Network\\Offline Files, in the Group Policy editor.</span></span>

2.  <span data-ttu-id="0a10c-165">Устанавливать.</span><span class="sxs-lookup"><span data-stu-id="0a10c-165">Manually.</span></span> <span data-ttu-id="0a10c-166">-Выберите Инструменты, а затем — Параметры папки в меню команд проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="0a10c-166">- Select Tools and then Folder Options in the command menu of Windows Explorer.</span></span> <span data-ttu-id="0a10c-167">Выберите вкладку Автономные файлы, а затем установите флажок **Шифровать автономные файлы для защиты данных** .</span><span class="sxs-lookup"><span data-stu-id="0a10c-167">Select the Offline Files tab, and then select the **Encrypt offline files to secure data** check box.</span></span>

### <span data-ttu-id="0a10c-168">Разрешите агенту UE-V создавать папки для каждого пользователя</span><span class="sxs-lookup"><span data-stu-id="0a10c-168">Let the UE-V Agent create folders for each user</span></span>

<span data-ttu-id="0a10c-169">Чтобы обеспечить оптимальное функционирование UE-V, создайте только корневой общий доступ на сервере и предоставьте агенту UE-V создание папок для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a10c-169">To ensure that UE-V works optimally, create only the root share on the server, and let the UE-V Agent create the folders for each user.</span></span> <span data-ttu-id="0a10c-170">UE-V создаст эти папки пользователей с соответствующей защитой.</span><span class="sxs-lookup"><span data-stu-id="0a10c-170">UE-V will create these user folders with the appropriate security.</span></span>

<span data-ttu-id="0a10c-171">С помощью этой конфигурации разрешений пользователи могут создавать папки для хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="0a10c-171">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="0a10c-172">Агент UE-V создает и защищает папку settingspackage во время работы в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a10c-172">The UE-V agent creates and secures a settingspackage folder while running in the context of the user.</span></span> <span data-ttu-id="0a10c-173">Пользователь получает полный доступ к своей папке settingspackage.</span><span class="sxs-lookup"><span data-stu-id="0a10c-173">The user receives full control to their settingspackage folder.</span></span> <span data-ttu-id="0a10c-174">Другие пользователи не наследуют доступ к этой папке.</span><span class="sxs-lookup"><span data-stu-id="0a10c-174">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="0a10c-175">Вам не нужно создавать и защищать отдельные каталоги пользователей.</span><span class="sxs-lookup"><span data-stu-id="0a10c-175">You do not need to create and secure individual user directories.</span></span> <span data-ttu-id="0a10c-176">Это будет выполнено автоматически агентом, который запускается в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a10c-176">This will be done automatically by the agent that runs in the context of the user.</span></span>

**<span data-ttu-id="0a10c-177">Примечание.</span><span class="sxs-lookup"><span data-stu-id="0a10c-177">Note</span></span>**  
<span data-ttu-id="0a10c-178">Дополнительную защиту можно настроить, когда используется сервер Windows для общего доступа к хранилищу параметров.</span><span class="sxs-lookup"><span data-stu-id="0a10c-178">Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="0a10c-179">UE-V можно настроить так, чтобы убедиться в том, что группа локального администратора или текущий пользователь является владельцем папки, в которой хранятся пакеты параметров.</span><span class="sxs-lookup"><span data-stu-id="0a10c-179">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="0a10c-180">Чтобы включить дополнительную защиту, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0a10c-180">To enable additional security use the following command:</span></span>

1.  <span data-ttu-id="0a10c-181">Добавьте раздел реестра REG \ _DWORD с именем "RepositoryOwnerCheckEnabled" `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="0a10c-181">Add a REG\_DWORD registry key named "RepositoryOwnerCheckEnabled" to `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="0a10c-182">Задайте для раздела реестра значение 1.</span><span class="sxs-lookup"><span data-stu-id="0a10c-182">Set registry key value to 1.</span></span>

<span data-ttu-id="0a10c-183">Если этот параметр конфигурации установлен, агент UE-V Agent удостоверяет, что локальная группа администраторов или текущий пользователь является владельцем папки settingspackage.</span><span class="sxs-lookup"><span data-stu-id="0a10c-183">When this configuration setting is in place, the UE-V agent verifies that the local administrator’s group or current user is the owner of the settingspackage folder.</span></span> <span data-ttu-id="0a10c-184">В противном случае агент UE-V не будет разрешать доступ к папке.</span><span class="sxs-lookup"><span data-stu-id="0a10c-184">If not, then the UE-V agent will not allow access to the folder.</span></span>



<span data-ttu-id="0a10c-185">Если необходимо создать папки для пользователей и убедиться, что у вас установлены правильные разрешения.</span><span class="sxs-lookup"><span data-stu-id="0a10c-185">If you must create folders for the users and ensure that you have the correct permissions set.</span></span>

<span data-ttu-id="0a10c-186">Настоятельно рекомендуется не создавать папки, а это значит, что вы разрешаете агенту UE-V создать папку для пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a10c-186">We strongly recommend that you do not precreate folders and that instead, you allow the UE-V agent to create the folder for the user.</span></span>

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a><span data-ttu-id="0a10c-187">Убедитесь в том, что при сохранении параметров UE-V в основном каталоге пользователя будут заданы правильные разрешения</span><span class="sxs-lookup"><span data-stu-id="0a10c-187">Ensure that correct permissions are set when storing UE-V settings in a user’s home directory</span></span>

<span data-ttu-id="0a10c-188">Если вы перенаправляли параметры UE-V в основной каталог пользователя, проверьте, правильно ли настроены разрешения для основного каталога пользователя в Организации.</span><span class="sxs-lookup"><span data-stu-id="0a10c-188">If you redirect UE-V settings to a user’s home directory, be sure that the permissions on the user's home directory are set appropriately for your organization.</span></span>

## <span data-ttu-id="0a10c-189">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0a10c-189">Related topics</span></span>


[<span data-ttu-id="0a10c-190">Безопасность и конфиденциальность в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="0a10c-190">Security and Privacy for UE-V 1.0</span></span>](security-and-privacy-for-ue-v-10.md)









