---
title: Восстановление перемещенного диска
description: Восстановление перемещенного диска
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812928"
---
# <span data-ttu-id="0713e-103">Восстановление перемещенного диска</span><span class="sxs-lookup"><span data-stu-id="0713e-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="0713e-104">При перемещении диска операционной системы, который ранее был зашифрован с помощью администрирования и мониторинга Microsoft BitLocker (MBAM), необходимо решить определенные проблемы.</span><span class="sxs-lookup"><span data-stu-id="0713e-104">When you move an operating system drive that has been previously encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), you must resolve certain issues.</span></span> <span data-ttu-id="0713e-105">После того как ПИН-код подключен к новому компьютеру, он не будет использовать ПИН-код запуска, который использовался на предыдущем компьютере.</span><span class="sxs-lookup"><span data-stu-id="0713e-105">After a PIN is attached to the new computer, the drive will not accept the start-up PIN that was used in previous computer.</span></span> <span data-ttu-id="0713e-106">Система считает этот PIN-код недействительным вследствие изменения микросхемы доверенного платформенного модуля (TPM).</span><span class="sxs-lookup"><span data-stu-id="0713e-106">The system considers the PIN to be invalid because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="0713e-107">Чтобы получить пароль восстановления, необходимо получить идентификатор ключа восстановления, чтобы использовать перемещенный диск.</span><span class="sxs-lookup"><span data-stu-id="0713e-107">You must obtain a recovery key ID to retrieve the recovery password in order to use the moved drive.</span></span> <span data-ttu-id="0713e-108">Для этого выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="0713e-108">To do this, use the following procedure.</span></span>

**<span data-ttu-id="0713e-109">Восстановление перемещенного диска</span><span class="sxs-lookup"><span data-stu-id="0713e-109">To recover a moved drive</span></span>**

1.  <span data-ttu-id="0713e-110">На компьютере, на котором находится перемещенный диск, запустите режим среды восстановления Windows (WinRE) или загрузите компьютер с помощью набора средств диагностики и восстановления Microsoft (DaRT).</span><span class="sxs-lookup"><span data-stu-id="0713e-110">On the computer that contains the moved drive, start in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="0713e-111">После того как компьютер будет запущен с помощью WinRE или DaRT, MBAM проведет диск операционной системы как диск с данными.</span><span class="sxs-lookup"><span data-stu-id="0713e-111">Once the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="0713e-112">В MBAM будет отображен идентификатор пароля восстановления устройства и запрос пароля восстановления.</span><span class="sxs-lookup"><span data-stu-id="0713e-112">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="0713e-113">**Примечание**  В некоторых случаях, чтобы войти в режим восстановления, вы можете нажать в процессе запуска кнопку " **забыть"** .</span><span class="sxs-lookup"><span data-stu-id="0713e-113">**Note** In some cases, you might be able to click **I forget the PIN** during the startup process to enter the recovery mode.</span></span> <span data-ttu-id="0713e-114">Здесь также отображается идентификатор ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="0713e-114">This also displays the recovery key ID.</span></span>

     

3.  <span data-ttu-id="0713e-115">На веб-сайте администрирования MBAM с помощью идентификатора ключа восстановления извлеките пароль восстановления и разблокируйте диск.</span><span class="sxs-lookup"><span data-stu-id="0713e-115">On the MBAM administration website, use the recovery key ID to retrieve the recovery password and unlock the drive.</span></span>

4.  <span data-ttu-id="0713e-116">Если перемещенный диск был настроен на использование микросхемы TPM на исходном компьютере, необходимо выполнить дополнительные действия, после того как вы разблокируете диск и завершите процесс запуска.</span><span class="sxs-lookup"><span data-stu-id="0713e-116">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after you unlock the drive and complete the start process.</span></span> <span data-ttu-id="0713e-117">В режиме WinRE откройте командную строки и воспользуйтесь средством **Manage-bde** для расшифровки диска.</span><span class="sxs-lookup"><span data-stu-id="0713e-117">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="0713e-118">Использование этого средства — это единственный способ удалить защиту доверенного платформенного модуля без первоначальной микросхемы TPM.</span><span class="sxs-lookup"><span data-stu-id="0713e-118">The use of this tool is the only way to remove the TPM-plus-PIN protection without the original TPM chip.</span></span>

5.  <span data-ttu-id="0713e-119">Завершив удаление, запустите систему в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="0713e-119">After the removal is complete, start the system normally.</span></span> <span data-ttu-id="0713e-120">Агент MBAM продолжит принудительное применение политики для шифрования диска с помощью ПИН-кода нового компьютера.</span><span class="sxs-lookup"><span data-stu-id="0713e-120">The MBAM agent will proceed to enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="0713e-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0713e-121">Related topics</span></span>


[<span data-ttu-id="0713e-122">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="0713e-122">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





