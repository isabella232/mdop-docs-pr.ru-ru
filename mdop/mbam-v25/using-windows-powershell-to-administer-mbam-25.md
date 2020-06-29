---
title: Использование Windows PowerShell для администрирования MBAM 2.5
description: Использование Windows PowerShell для администрирования MBAM 2.5
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812736"
---
# <span data-ttu-id="bf071-103">Использование Windows PowerShell для администрирования MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="bf071-103">Using Windows PowerShell to Administer MBAM 2.5</span></span>


<span data-ttu-id="bf071-104">В этом разделе описаны командлеты Windows PowerShell для администрирования и мониторинга Microsoft BitLocker (MBAM), которые относятся к восстановлению компьютеров и дисков, когда пользователи заблокированы.</span><span class="sxs-lookup"><span data-stu-id="bf071-104">This topic describes Windows PowerShell cmdlets for Microsoft BitLocker Administration and Monitoring (MBAM) that relate to recovering computers or drives when users get locked out.</span></span>

<span data-ttu-id="bf071-105">Для командлетов, которые вы используете для настройки функций сервера MBAM, ознакомьтесь [с Разстройкой функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="bf071-105">For cmdlets that you use to configure MBAM Server features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a><span data-ttu-id="bf071-106">Командлеты для восстановления компьютеров или дисков, управляемых MBAM</span><span class="sxs-lookup"><span data-stu-id="bf071-106">Cmdlets for recovering computers or drives that are managed by MBAM</span></span>


<span data-ttu-id="bf071-107">Используйте указанные ниже командлеты Windows PowerShell для восстановления компьютеров или дисков, управляемых MBAM.</span><span class="sxs-lookup"><span data-stu-id="bf071-107">Use the following Windows PowerShell cmdlets to recover computers or drives that are managed by MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bf071-108">Имя</span><span class="sxs-lookup"><span data-stu-id="bf071-108">Name</span></span></th>
<th align="left"><span data-ttu-id="bf071-109">Описание</span><span class="sxs-lookup"><span data-stu-id="bf071-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bf071-110">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="bf071-110">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf071-111">Запрашивает ключ восстановления MBAM, который позволяет пользователям разблокировать компьютер или зашифрованный диск.</span><span class="sxs-lookup"><span data-stu-id="bf071-111">Requests an MBAM recovery key that enables users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bf071-112">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="bf071-112">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf071-113">Предоставление пользователям пароля владельца TPM, который можно использовать для разблокировки доверенного платформенного модуля (TPM), когда ДОВЕРЕНный платформенный модуль заблокировал их и больше не будет получать PIN-код.</span><span class="sxs-lookup"><span data-stu-id="bf071-113">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> <span data-ttu-id="bf071-114">Справка по командлету MBAM</span><span class="sxs-lookup"><span data-stu-id="bf071-114">MBAM cmdlet Help</span></span>


<span data-ttu-id="bf071-115">Справка по Windows PowerShell для командлетов MBAM доступна в следующих форматах:</span><span class="sxs-lookup"><span data-stu-id="bf071-115">Windows PowerShell Help for MBAM cmdlets is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bf071-116">Формат справки Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf071-116">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="bf071-117">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="bf071-117">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bf071-118">В командной строке Windows PowerShell введите <strong> </strong> &lt; <em> командлет Get-Help</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="bf071-118">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf071-119">Чтобы загрузить последние командлеты Windows PowerShell, следуйте инструкциям, приведенным в разделе <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf071-119">To upload the latest Windows PowerShell cmdlets, follow the instructions in <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bf071-120">На веб-страницах TechNet.</span><span class="sxs-lookup"><span data-stu-id="bf071-120">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bf071-121">В центре загрузки как файл Word. docx</span><span class="sxs-lookup"><span data-stu-id="bf071-121">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bf071-122">В центре загрузки в виде PDF-файла</span><span class="sxs-lookup"><span data-stu-id="bf071-122">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="bf071-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="bf071-123">Related topics</span></span>


[<span data-ttu-id="bf071-124">Администрирование компонентов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="bf071-124">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="bf071-125">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf071-125">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## <span data-ttu-id="bf071-126">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="bf071-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="bf071-127">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="bf071-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="bf071-128">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="bf071-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





