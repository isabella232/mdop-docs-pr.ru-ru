---
title: Настройка системы безопасности сервера потоковой передачи после установки
description: Настройка системы безопасности сервера потоковой передачи после установки
author: dansimp
ms.assetid: 9bde3677-d1aa-4dcc-904e-bb49a268d748
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1945b38da5dd50c0bd2fb0c741bd92012e78586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817902"
---
# <span data-ttu-id="38c34-103">Настройка системы безопасности сервера потоковой передачи после установки</span><span class="sxs-lookup"><span data-stu-id="38c34-103">How to Configure Streaming Server Security Post-Installation</span></span>


<span data-ttu-id="38c34-104">Настройте потоковый сервер App-V для усиления безопасности в реестре.</span><span class="sxs-lookup"><span data-stu-id="38c34-104">Configure the App-V Streaming Server for enhanced security through the registry.</span></span> <span data-ttu-id="38c34-105">Как и в случае с сервером управления App-V, сертификат должен быть правильно настроен с правильным идентификатором EKU для проверки подлинности сервера, прежде чем выполнять описанную ниже процедуру после установки.</span><span class="sxs-lookup"><span data-stu-id="38c34-105">As with the App-V Management Server, a certificate must be correctly provisioned with the correct EKU identifier for Server Authentication before you complete the following post-installation procedure.</span></span>

**<span data-ttu-id="38c34-106">Настройка безопасности серверного потока после установки</span><span class="sxs-lookup"><span data-stu-id="38c34-106">To configure Streaming Server security post-installation</span></span>**

1.  <span data-ttu-id="38c34-107">Создайте консоль MMC, добавьте оснастку « **Сертификаты** » и выберите пункт **хранилище сертификатов на локальном компьютере**.</span><span class="sxs-lookup"><span data-stu-id="38c34-107">Create an MMC, add the **Certificates** snap-in, and select **Local Machine certificate store**.</span></span>

2.  <span data-ttu-id="38c34-108">Откройте **Личные** сертификаты для компьютера и откройте сертификат, подготовленный для App-V.</span><span class="sxs-lookup"><span data-stu-id="38c34-108">Open the **Personal** certificates for the computer, and open the certificate provisioned for App-V.</span></span>

3.  <span data-ttu-id="38c34-109">На вкладке **сведения** прокрутите вниз до отпечатка и скопируйте хэш-код в область сведений.</span><span class="sxs-lookup"><span data-stu-id="38c34-109">On the **Details** tab, scroll down to the thumbprint and copy the hash in the details pane.</span></span>

4.  <span data-ttu-id="38c34-110">Откройте редактор реестра и перейдите к разделу `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server` .</span><span class="sxs-lookup"><span data-stu-id="38c34-110">Open the registry editor, and navigate to `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server`.</span></span>

5.  <span data-ttu-id="38c34-111">Измените `X509CertHash` значение, вставьте хэш-код отпечатка в поле значения и удалите все пробелы.</span><span class="sxs-lookup"><span data-stu-id="38c34-111">Edit the `X509CertHash` value, paste the thumbprint hash in the value field, and remove all spaces.</span></span> <span data-ttu-id="38c34-112">Нажмите кнопку **ОК** , чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="38c34-112">Click **OK** to accept the edit.</span></span>

6.  <span data-ttu-id="38c34-113">В редакторе реестра перейдите к `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts` .</span><span class="sxs-lookup"><span data-stu-id="38c34-113">In the registry editor, navigate to `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts`.</span></span>

7.  <span data-ttu-id="38c34-114">Создайте новый параметр **DWORD** с именем "322", а затем введите десятичное значение в формате 322 или шестнадцатеричное значение как 142.</span><span class="sxs-lookup"><span data-stu-id="38c34-114">Create a new **DWORD** value named "322," and then enter the decimal value as 322 or the hexadecimal value as 142.</span></span>

8.  <span data-ttu-id="38c34-115">Перезапустите службу потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="38c34-115">Restart the streaming service.</span></span>

## <span data-ttu-id="38c34-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="38c34-116">Related topics</span></span>


[<span data-ttu-id="38c34-117">Настройка системы безопасности сервера управления после установки</span><span class="sxs-lookup"><span data-stu-id="38c34-117">How to Configure Management Server Security Post-Installation</span></span>](how-to-configure-management-server-security-post-installation.md)

[<span data-ttu-id="38c34-118">Устранение проблем с разрешениями сертификатов</span><span class="sxs-lookup"><span data-stu-id="38c34-118">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





