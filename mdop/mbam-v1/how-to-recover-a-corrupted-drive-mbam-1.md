---
title: Восстановление поврежденного диска
description: Восстановление поврежденного диска
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812944"
---
# <span data-ttu-id="d918c-103">Восстановление поврежденного диска</span><span class="sxs-lookup"><span data-stu-id="d918c-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="d918c-104">Чтобы восстановить поврежденный диск, защищенный BitLocker, пользователь службы поддержки администрирования и мониторинга Microsoft BitLocker (MBAM) должен создать файл пакета ключей восстановления.</span><span class="sxs-lookup"><span data-stu-id="d918c-104">To recover a corrupted drive that has been protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) help desk user must create a recovery key package file.</span></span> <span data-ttu-id="d918c-105">Этот файл пакета можно скопировать на компьютер, на котором находится поврежденный диск, а затем использовать для восстановления диска.</span><span class="sxs-lookup"><span data-stu-id="d918c-105">This package file can be copied to the computer that contains the corrupted drive and then used to recover the drive.</span></span> <span data-ttu-id="d918c-106">Чтобы сделать это, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d918c-106">To accomplish this, use the following procedure.</span></span>

**<span data-ttu-id="d918c-107">Восстановление поврежденного диска</span><span class="sxs-lookup"><span data-stu-id="d918c-107">To Recover a Corrupted Drive</span></span>**

1.  <span data-ttu-id="d918c-108">Откройте веб-сайт администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="d918c-108">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="d918c-109">В области навигации выберите **Восстановление дисков** .</span><span class="sxs-lookup"><span data-stu-id="d918c-109">Select **Drive Recovery** from the navigation pane.</span></span> <span data-ttu-id="d918c-110">Введите доменное имя пользователя и имя пользователя, причины разблокировки диска и ИД пароля для восстановления пользователя.</span><span class="sxs-lookup"><span data-stu-id="d918c-110">Enter the user’s domain name and user name, the reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="d918c-111">**Примечание**  Если вы являетесь участником роли администраторов службы поддержки, вам не нужно вводить доменное имя пользователя или имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="d918c-111">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="d918c-112">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="d918c-112">Click **Submit**.</span></span> <span data-ttu-id="d918c-113">Появится ключ восстановления.</span><span class="sxs-lookup"><span data-stu-id="d918c-113">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="d918c-114">Нажмите кнопку **сохранить**, а затем выберите **пакет ключей восстановления**.</span><span class="sxs-lookup"><span data-stu-id="d918c-114">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="d918c-115">Пакет ключа восстановления будет создан на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="d918c-115">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="d918c-116">Скопируйте пакет ключа восстановления на компьютер с поврежденным диском.</span><span class="sxs-lookup"><span data-stu-id="d918c-116">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="d918c-117">Откройте командную строку с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="d918c-117">Open an elevated command prompt.</span></span> <span data-ttu-id="d918c-118">Для этого нажмите кнопку **Пуск** и введите `cmd` в поле **Найти программы и файлы** .</span><span class="sxs-lookup"><span data-stu-id="d918c-118">To do this, click **Start** and type `cmd` in the **Search programs and files** box.</span></span> <span data-ttu-id="d918c-119">В списке результатов поиска щелкните **cmd.exe** правой кнопкой мыши и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="d918c-119">In the search results list, right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="d918c-120">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d918c-120">At the command prompt, type the following:</span></span>

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="d918c-121">**Примечание**  Для &lt; жесткого диска &gt; в команде Укажите доступное запоминающее устройство, которое имеет свободное место, равное или больше, чем данные на поврежденном диске.</span><span class="sxs-lookup"><span data-stu-id="d918c-121">**Note** For the &lt;fixed drive&gt; in the command, specify an available storage device that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="d918c-122">Данные поврежденного диска будут восстановлены и перемещены на указанный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="d918c-122">Data on the corrupted drive is recovered and moved to the specified fixed drive.</span></span>

     

## <span data-ttu-id="d918c-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d918c-123">Related topics</span></span>


[<span data-ttu-id="d918c-124">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="d918c-124">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





