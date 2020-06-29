---
title: Администрирование MBAM 1.0 с помощью PowerShell
description: Администрирование MBAM 1.0 с помощью PowerShell
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825139"
---
# <span data-ttu-id="4723a-103">Администрирование MBAM 1.0 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="4723a-103">Administering MBAM 1.0 by Using PowerShell</span></span>


<span data-ttu-id="4723a-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) предоставляет перечисленные ниже наборы командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4723a-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="4723a-105">Администраторы могут использовать эти командлеты PowerShell для выполнения различных задач сервера MBAM в командной строке, а не на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="4723a-105">Administrators can use these PowerShell cmdlets to perform various MBAM server tasks from the command prompt rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="4723a-106">Администрирование MBAM с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="4723a-106">How to administer MBAM by using PowerShell</span></span>


<span data-ttu-id="4723a-107">Используйте командлеты PowerShell, описанные в этой статье, чтобы администрировать MBAM.</span><span class="sxs-lookup"><span data-stu-id="4723a-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4723a-108">Имя</span><span class="sxs-lookup"><span data-stu-id="4723a-108">Name</span></span></th>
<th align="left"><span data-ttu-id="4723a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4723a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4723a-110">Add-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="4723a-110">Add-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="4723a-111">Добавляет новую аппаратную модель в инвентаризацию оборудования MBAM.</span><span class="sxs-lookup"><span data-stu-id="4723a-111">Adds a new hardware model to the MBAM hardware inventory.</span></span> <span data-ttu-id="4723a-112">Этот командлет также может определять, поддерживается ли оборудование и не поддерживается шифрованием диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4723a-112">This cmdlet can also specify whether the hardware is supported or unsupported for BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4723a-113">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="4723a-113">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="4723a-114">Запрашивает ключ восстановления MBAM, который позволяет пользователю разблокировать компьютер или зашифрованный диск.</span><span class="sxs-lookup"><span data-stu-id="4723a-114">Requests an MBAM recovery key that will enable a user to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4723a-115">Get-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="4723a-115">Get-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="4723a-116">Возвращает основное инвентаризацию оборудования, которая содержит данные, указывающие, совместимы ли модели оборудования с шифрованием диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4723a-116">Gets a master hardware inventory that contains data that indicates whether hardware models are compatible or incompatible with BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4723a-117">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="4723a-117">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="4723a-118">Предоставление пользователю пароля владельца доверенного платформенного модуля для управления доступом TPM (доверенный платформенный модуль).</span><span class="sxs-lookup"><span data-stu-id="4723a-118">Provides a TPM owner password for a user to manage their TPM (Trusted Platform Module) access.</span></span> <span data-ttu-id="4723a-119">Помогает пользователям, когда доверенный платформенный модуль заблокировал их и больше не будет получать PIN-код.</span><span class="sxs-lookup"><span data-stu-id="4723a-119">Helps users when TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4723a-120">Install-MBAM</span><span class="sxs-lookup"><span data-stu-id="4723a-120">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="4723a-121">Устанавливает функции MBAM, обеспечивающие расширенную групповую политику, шифрование, восстановление ключей и средства создания отчетов о соответствии требованиям.</span><span class="sxs-lookup"><span data-stu-id="4723a-121">Installs MBAM features that provide advanced group policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4723a-122">Remove-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="4723a-122">Remove-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="4723a-123">Удаление моделей оборудования из инвентаризации оборудования.</span><span class="sxs-lookup"><span data-stu-id="4723a-123">Removes the hardware models from the hardware inventory.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4723a-124">Set-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="4723a-124">Set-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="4723a-125">Позволяет управлять оборудованием основного оборудования, чтобы определить, поддерживаются ли модели оборудования или не могут выполнять шифрование BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4723a-125">Allows management of a master hardware inventory to designate whether or not hardware models are capable or incapable to perform BitLocker encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4723a-126">Uninstall-MBAM</span><span class="sxs-lookup"><span data-stu-id="4723a-126">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="4723a-127">Удаление ранее установленных функций MBAM, которые обеспечивают расширенные политики, шифрование, восстановление ключей и средства создания отчетов о соответствии требованиям.</span><span class="sxs-lookup"><span data-stu-id="4723a-127">Removes previously installed MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4723a-128">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4723a-128">Related topics</span></span>


[<span data-ttu-id="4723a-129">Операции MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="4723a-129">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





