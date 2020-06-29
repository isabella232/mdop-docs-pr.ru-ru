---
title: Сброс блокировки доверенного платформенного модуля
description: Сброс блокировки доверенного платформенного модуля
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812920"
---
# <span data-ttu-id="2104f-103">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="2104f-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="2104f-104">Функция восстановления зашифрованных дисков в Microsoft BitLocker Administration и Monitoring (MBAM) включает в себя захват и хранение данных, а также доступность средств, необходимых для управления доверенным платформенным модулем (TPM).</span><span class="sxs-lookup"><span data-stu-id="2104f-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are required to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="2104f-105">В этой статье описано, как получить доступ к системе данных восстановления централизованного ключа на веб-сайте _admmon \ _tlanextref администрирования.</span><span class="sxs-lookup"><span data-stu-id="2104f-105">This topic covers how to access the centralized Key Recovery data system in the bit\_admmon\_tlanextref administration website.</span></span> <span data-ttu-id="2104f-106">Система данных восстановления ключа может предоставить файл пароля владельца TPM при предоставлении идентификации компьютера и соответствующего идентификатора пользователя.</span><span class="sxs-lookup"><span data-stu-id="2104f-106">The Key Recovery data system can provide a TPM owner password file when the computer identity and the associated user identifier are supplied.</span></span>

<span data-ttu-id="2104f-107">Блокировка доверенного платформенного модуля может возникнуть, если пользователь ввел неверный ПИН-код слишком много раз.</span><span class="sxs-lookup"><span data-stu-id="2104f-107">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="2104f-108">Количество ситуаций, в которых пользователь может ввести неверный ПИН-код, прежде чем блокировка доверенного платформенного модуля будет основана на спецификации изготовителя компьютера.</span><span class="sxs-lookup"><span data-stu-id="2104f-108">The number of times that a user can enter an incorrect PIN before the TPM lockout is based on the computer manufacturer's specification.</span></span>

**<span data-ttu-id="2104f-109">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="2104f-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="2104f-110">Откройте веб-сайт администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="2104f-110">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="2104f-111">В области навигации выберите **Управление TPM**.</span><span class="sxs-lookup"><span data-stu-id="2104f-111">In the navigation pane, select **Manage TPM**.</span></span> <span data-ttu-id="2104f-112">Откроется страница **Manage TPM** .</span><span class="sxs-lookup"><span data-stu-id="2104f-112">This opens the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="2104f-113">Введите полное доменное имя (FQDN) компьютера и имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="2104f-113">Enter the fully qualified domain name (FQDN) for the computer and the computer name.</span></span> <span data-ttu-id="2104f-114">Введите домен пользователя Windows и имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="2104f-114">Enter the user’s Windows Logon domain and the user’s user name.</span></span> <span data-ttu-id="2104f-115">Выберите один из предопределенных параметров в поле **Причина для запроса файла пароля владельца доверенного платформенного модуля** .</span><span class="sxs-lookup"><span data-stu-id="2104f-115">Select one of the predefined options in the **Reason for requesting TPM owner password file** drop-down menu.</span></span> <span data-ttu-id="2104f-116">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="2104f-116">Click **Submit**.</span></span>

4.  <span data-ttu-id="2104f-117">MBAM будет возвращать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2104f-117">MBAM will return one of the following:</span></span>

    -   <span data-ttu-id="2104f-118">Сообщение об ошибке, если не удается найти соответствующий файл пароля владельца доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="2104f-118">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="2104f-119">Файл пароля владельца доверенного платформенного модуля для отправленного компьютера</span><span class="sxs-lookup"><span data-stu-id="2104f-119">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="2104f-120">**Примечание**  Если вы являетесь дополнительным пользователем службы поддержки, поля "домен пользователя" и "ИД пользователя" не требуются.</span><span class="sxs-lookup"><span data-stu-id="2104f-120">**Note** If you are an Advanced Helpdesk User, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="2104f-121">При извлечении появится пароль владельца.</span><span class="sxs-lookup"><span data-stu-id="2104f-121">Upon retrieval, the owner password is displayed.</span></span> <span data-ttu-id="2104f-122">Чтобы сохранить этот пароль в файле. TPM, нажмите кнопку **сохранить** .</span><span class="sxs-lookup"><span data-stu-id="2104f-122">To save this password to a .tpm file, click the **Save** button.</span></span>

6.  <span data-ttu-id="2104f-123">Пользователь запустит консоль управления TPM и выберет параметр **сброса блокировки TPM** и предоставит файл пароля владельца доверенного платформенного модуля для сброса блокировки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="2104f-123">The user will run the TPM management console and select the **Reset TPM lockout** option and provide the TPM owner password file to reset the TPM lockout.</span></span>

## <span data-ttu-id="2104f-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2104f-124">Related topics</span></span>


[<span data-ttu-id="2104f-125">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="2104f-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





