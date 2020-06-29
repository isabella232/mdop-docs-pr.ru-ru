---
title: Восстановление перемещенного диска
description: Восстановление перемещенного диска
author: dansimp
ms.assetid: 697cd78d-962c-411e-901a-2e9220ba6552
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bd0d43f2eea95fe71225a50e7fa68d4fb1c35485
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825062"
---
# <span data-ttu-id="1ec62-103">Восстановление перемещенного диска</span><span class="sxs-lookup"><span data-stu-id="1ec62-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="1ec62-104">Когда вы перемещаете диск операционной системы, зашифрованный с помощью администрирования и мониторинга Microsoft BitLocker (MBAM), диск не будет использовать PIN-код, который использовался на предыдущем компьютере, благодаря изменениям микросхемы доверенного платформенного модуля (TPM).</span><span class="sxs-lookup"><span data-stu-id="1ec62-104">When you move an operating system drive that is encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), the drive will not accept the PIN that was used in a previous computer because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="1ec62-105">Для использования перенесенного диска вам потребуется способ получить идентификатор ключа восстановления, чтобы получить пароль восстановления.</span><span class="sxs-lookup"><span data-stu-id="1ec62-105">To use the moved drive, you will need a way to obtain the recovery key ID to retrieve the recovery password.</span></span> <span data-ttu-id="1ec62-106">Чтобы восстановить перемещенный диск, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1ec62-106">Use the following procedure to recover a drive that has moved.</span></span>

**<span data-ttu-id="1ec62-107">Восстановление перемещенного диска</span><span class="sxs-lookup"><span data-stu-id="1ec62-107">To recover a moved drive</span></span>**

1.  <span data-ttu-id="1ec62-108">На компьютере, содержащем перемещенный диск, запустите компьютер в режиме среды восстановления Windows (WinRE) или загрузите компьютер, используя набор средств диагностики и восстановления Microsoft (DaRT).</span><span class="sxs-lookup"><span data-stu-id="1ec62-108">On the computer that contains the moved drive, start the computer in Windows recovery environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="1ec62-109">После того как компьютер будет запущен с помощью WinRE или DaRT, Администрирование и мониторинг Microsoft BitLocker обрабатывают перемещенный диск операционной системы как диск с данными.</span><span class="sxs-lookup"><span data-stu-id="1ec62-109">Once the computer has been started with WinRE or DaRT, Microsoft BitLocker Administration and Monitoring will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="1ec62-110">В MBAM будет отображен идентификатор пароля восстановления устройства и запрос пароля восстановления.</span><span class="sxs-lookup"><span data-stu-id="1ec62-110">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="1ec62-111">**Примечание**  В некоторых случаях вы можете нажать кнопку " **забыли ПИН-код** в процессе запуска", а затем войти в режим восстановления для отображения идентификатора ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="1ec62-111">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="1ec62-112">С помощью идентификатора ключа восстановления извлеките пароль восстановления и разблокируйте диск на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="1ec62-112">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="1ec62-113">Если перемещенный диск был настроен на использование микросхемы TPM на исходном компьютере, необходимо выполнить дополнительные действия после разблокировки диска и завершения процесса запуска.</span><span class="sxs-lookup"><span data-stu-id="1ec62-113">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after unlocking the drive and completing the start process.</span></span> <span data-ttu-id="1ec62-114">В режиме WinRE откройте командную строки и воспользуйтесь средством **Manage-bde** для расшифровки диска.</span><span class="sxs-lookup"><span data-stu-id="1ec62-114">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="1ec62-115">С помощью этого инструмента можно удалить предохранитель доверенного платформенного модуля и без первоначальной микросхемы TPM.</span><span class="sxs-lookup"><span data-stu-id="1ec62-115">Using this tool is the only way to remove the TPM plus PIN protector without the original TPM chip.</span></span>

5.  <span data-ttu-id="1ec62-116">После завершения удаления запустите компьютер в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="1ec62-116">Once the removal is completed, start the computer normally.</span></span> <span data-ttu-id="1ec62-117">Агент MBAM принудительно задаст политике шифрование диска с помощью ПИН-кода нового доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="1ec62-117">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="1ec62-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1ec62-118">Related topics</span></span>


[<span data-ttu-id="1ec62-119">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="1ec62-119">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





