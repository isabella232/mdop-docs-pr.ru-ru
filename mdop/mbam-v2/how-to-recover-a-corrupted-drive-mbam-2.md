---
title: Восстановление поврежденного диска
description: Восстановление поврежденного диска
author: dansimp
ms.assetid: b0457a00-f72e-4ad8-ab3b-7701851ca87e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5bbd4c2a1f5ef3fde78a9f72c1f77ccb0cdea377
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822872"
---
# <span data-ttu-id="d8586-103">Восстановление поврежденного диска</span><span class="sxs-lookup"><span data-stu-id="d8586-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="d8586-104">Чтобы восстановить поврежденный диск, защищенный BitLocker, пользователь службы поддержки Microsoft BitLocker (MBAM) должен создать файл пакета ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="d8586-104">To recover a corrupted drive protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) Help Desk user will need to create a recovery key package file.</span></span> <span data-ttu-id="d8586-105">После этого файл пакета можно будет скопировать на компьютер, на котором находится поврежденный диск, и затем использовать его для восстановления диска.</span><span class="sxs-lookup"><span data-stu-id="d8586-105">This package file can then be copied to the computer that contains the corrupted drive, and then used to recover the drive.</span></span> <span data-ttu-id="d8586-106">Для этого выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d8586-106">Use the following procedure for the steps needed to do this.</span></span>

<span data-ttu-id="d8586-107">**Важно!**  Чтобы избежать возможной потери данных, настоятельно рекомендуется прочитать справку "Repair-bde" и ясно понять, как использовать эту команду перед выполнением указанных ниже инструкций.</span><span class="sxs-lookup"><span data-stu-id="d8586-107">**Important** To avoid a potential loss of data, it is strongly recommended that you read the “repair-bde” help and clearly understand how to use the command before completing the following instructions.</span></span>

 

**<span data-ttu-id="d8586-108">Восстановление поврежденного диска</span><span class="sxs-lookup"><span data-stu-id="d8586-108">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="d8586-109">Чтобы создать пакет ключа восстановления, необходимый для восстановления поврежденного диска, запустите веб-браузер и откройте веб-сайт администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8586-109">To create the recovery key package necessary to recover a corrupted drive, start a web browser and open the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="d8586-110">В области навигации слева выберите пункт **Восстановление дисков** .</span><span class="sxs-lookup"><span data-stu-id="d8586-110">Select **Drive Recovery** from the left navigation pane.</span></span> <span data-ttu-id="d8586-111">Введите доменное имя пользователя, имя пользователя, причину разблокировки диска и ИД пароля восстановления пользователя.</span><span class="sxs-lookup"><span data-stu-id="d8586-111">Enter the user’s domain name, user name, reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="d8586-112">**Примечание**  Если вы являетесь участником роли администраторов службы поддержки, вам не нужно вводить доменное имя пользователя или имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="d8586-112">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="d8586-113">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="d8586-113">Click **Submit**.</span></span> <span data-ttu-id="d8586-114">Появится ключ восстановления.</span><span class="sxs-lookup"><span data-stu-id="d8586-114">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="d8586-115">Нажмите кнопку **сохранить**, а затем выберите **пакет ключей восстановления**.</span><span class="sxs-lookup"><span data-stu-id="d8586-115">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="d8586-116">Пакет ключа восстановления будет создан на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="d8586-116">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="d8586-117">Скопируйте пакет ключа восстановления на компьютер с поврежденным диском.</span><span class="sxs-lookup"><span data-stu-id="d8586-117">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="d8586-118">Откройте командную строку с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="d8586-118">Open an elevated command prompt.</span></span> <span data-ttu-id="d8586-119">Для этого нажмите кнопку **Пуск** и введите `cmd` в **поле Найти программы и файлы**.</span><span class="sxs-lookup"><span data-stu-id="d8586-119">To do this, click **Start** and type `cmd` in the **Search programs and files box**.</span></span> <span data-ttu-id="d8586-120">Щелкните **cmd.exe** правой кнопкой мыши и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="d8586-120">Right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="d8586-121">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d8586-121">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="d8586-122">**Примечание**  Замените &lt; фиксированный диск &gt; на свободный диск, на котором свободно больше или превышает объем данных на поврежденном диске.</span><span class="sxs-lookup"><span data-stu-id="d8586-122">**Note** Replace &lt;fixed drive&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="d8586-123">Данные поврежденного диска будут восстановлены и перемещены на указанный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="d8586-123">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     

## <span data-ttu-id="d8586-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d8586-124">Related topics</span></span>


[<span data-ttu-id="d8586-125">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="d8586-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





