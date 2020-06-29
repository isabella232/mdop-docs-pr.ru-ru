---
title: Администрирование MBAM 2.0 с помощью PowerShell
description: Администрирование MBAM 2.0 с помощью PowerShell
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823502"
---
# <span data-ttu-id="e52bf-103">Администрирование MBAM 2.0 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="e52bf-103">Administering MBAM 2.0 Using PowerShell</span></span>


<span data-ttu-id="e52bf-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) предоставляет перечисленные ниже наборы командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e52bf-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="e52bf-105">Администраторы могут использовать эти командлеты PowerShell для выполнения различных задач администрирования Microsoft BitLocker и наблюдения за серверами из командной строки, а не с веб-сайта администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="e52bf-105">Administrators can use these PowerShell cmdlets to perform various Microsoft BitLocker Administration and Monitoring server tasks from the command line rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="e52bf-106">Администрирование MBAM с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="e52bf-106">How to Administer MBAM Using PowerShell</span></span>


<span data-ttu-id="e52bf-107">Используйте командлеты PowerShell, описанные в этой статье, чтобы администрировать MBAM.</span><span class="sxs-lookup"><span data-stu-id="e52bf-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e52bf-108">Имя</span><span class="sxs-lookup"><span data-stu-id="e52bf-108">Name</span></span></th>
<th align="left"><span data-ttu-id="e52bf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e52bf-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e52bf-110">Install-MBAM</span><span class="sxs-lookup"><span data-stu-id="e52bf-110">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="e52bf-111">Установка функций MBAM, обеспечивающих расширенную политику, шифрование, восстановление ключей и отчеты о соответствии требованиям.</span><span class="sxs-lookup"><span data-stu-id="e52bf-111">Installs the MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e52bf-112">Uninstall-MBAM</span><span class="sxs-lookup"><span data-stu-id="e52bf-112">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="e52bf-113">Удаление функций MBAM, обеспечивающих расширенную политику, шифрование, восстановление ключей и средства создания отчетов о соответствии требованиям.</span><span class="sxs-lookup"><span data-stu-id="e52bf-113">Removes the MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e52bf-114">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="e52bf-114">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="e52bf-115">Запрашивает ключ восстановления MBAM, который позволяет пользователям разблокировать компьютер или зашифрованный диск.</span><span class="sxs-lookup"><span data-stu-id="e52bf-115">Requests an MBAM recovery key that will enable users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e52bf-116">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="e52bf-116">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="e52bf-117">Предоставление пользователям пароля владельца TPM, который можно использовать для разблокировки доверенного платформенного модуля (TPM), когда ДОВЕРЕНный платформенный модуль заблокировал их и больше не будет получать PIN-код.</span><span class="sxs-lookup"><span data-stu-id="e52bf-117">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e52bf-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e52bf-118">Related topics</span></span>


[<span data-ttu-id="e52bf-119">Операции MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e52bf-119">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





