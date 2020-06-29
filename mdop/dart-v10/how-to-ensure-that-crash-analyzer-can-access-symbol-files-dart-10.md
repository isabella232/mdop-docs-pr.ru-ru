---
title: Обеспечение доступа к файлам символов для средства анализа сбоев Crash Analyzer
description: Обеспечение доступа к файлам символов для средства анализа сбоев Crash Analyzer
author: dansimp
ms.assetid: 39e307bd-5d21-4e44-bed6-bf532f580775
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8e0ba2fa777039e1c6ffb91dd997438d8ea50616
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822609"
---
# <span data-ttu-id="cc0ec-103">Обеспечение доступа к файлам символов для средства анализа сбоев Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="cc0ec-103">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>


<span data-ttu-id="cc0ec-104">Обычно отладочная информация хранится в файле символов, отдельном от программы.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-104">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="cc0ec-105">При отладке приложения, которое перестало отвечать, необходимо иметь доступ к сведениям о символах.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-105">You must have access to the symbol information when you debug an application that has stopped responding.</span></span>

<span data-ttu-id="cc0ec-106">Файлы символов загружаются автоматически при запуске **анализатора аварийного**восстановления.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-106">Symbol files are automatically downloaded when you run **Crash Analyzer**.</span></span> <span data-ttu-id="cc0ec-107">Если у компьютера нет подключения к Интернету или в сети требуется, чтобы компьютер имел доступ к прокси-серверу HTTP, Загрузка файлов символов невозможна.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-107">If the computer does not have an Internet connection or the network requires the computer to access an HTTP proxy server, the symbol files cannot be downloaded.</span></span>

**<span data-ttu-id="cc0ec-108">Проверка того, что анализатор аварийного восстановления может получить доступ к файлам символов</span><span class="sxs-lookup"><span data-stu-id="cc0ec-108">To ensure that Crash Analyzer can access symbol files</span></span>**

1.  **<span data-ttu-id="cc0ec-109">Скопируйте файл дампа на другой компьютер.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-109">Copy the dump file to another computer.</span></span>** <span data-ttu-id="cc0ec-110">Если не удается загрузить символы из-за отсутствия подключения к Интернету, скопируйте файл дампа памяти на компьютер с подключением к Интернету и запустите на нем мастер автономной **анализатора сбоев** .</span><span class="sxs-lookup"><span data-stu-id="cc0ec-110">If the symbols cannot be downloaded because of a lack of an Internet connection, copy the memory dump file to a computer that does have an Internet connection and run the stand-alone **Crash Analyzer Wizard** on that computer.</span></span>

2.  **<span data-ttu-id="cc0ec-111">Доступ к файлам символов с другого компьютера.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-111">Access the symbol files from another computer.</span></span>** <span data-ttu-id="cc0ec-112">Если не удается загрузить символы из-за отсутствия подключения к Интернету, вы можете скачать символы с компьютера, на котором установлено подключение к Интернету, а затем скопировать его на компьютер, на котором нет подключения к Интернету, или вы можете подключить сетевой диск к расположению, в котором символы доступны в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-112">If the symbols cannot be downloaded because of a lack of an Internet connection, you can download the symbols from a computer that does have an Internet connection and then copy them to the computer that does not have an Internet connection, or you can map a network drive to a location where the symbols are available on the local network.</span></span> <span data-ttu-id="cc0ec-113">Если запустить **анализатор аварийных сбоев** в среде восстановления Windows (WindowsRE), вы можете добавить файлы символов в образ восстановления для Microsoft Diagnostics и средств восстановления (DART) 10.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-113">If you run the **Crash Analyzer** in a Windows Recovery Environment (WindowsRE), you can include the symbol files on the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

3.  **<span data-ttu-id="cc0ec-114">Доступ к файлам символов через прокси-сервер HTTP.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-114">Access symbol files through an HTTP proxy server.</span></span>** <span data-ttu-id="cc0ec-115">Если не удается загрузить символы, так как требуется доступ к прокси-серверу HTTP, выполните указанные ниже действия, чтобы получить доступ к прокси-серверу HTTP.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-115">If the symbols cannot be downloaded because an HTTP proxy server must be accessed, use the following steps to access an HTTP proxy server.</span></span> <span data-ttu-id="cc0ec-116">На DaRT 10 у **мастера анализатора сбоев** обнаружен параметр, указанный в диалоговом окне " **укажите расположение файлов символов** ", которое помечено **прокси-сервером меток (необязательно, используя формат "сервер: порт")**.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-116">In DaRT 10, the **Crash Analyzer Wizard** has a setting available on the **Specify Symbol Files Location** dialog page, marked with the label **Proxy server (optional, using the format "server:port")**.</span></span> <span data-ttu-id="cc0ec-117">Вы можете использовать это текстовое поле, чтобы указать прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-117">You can use this text box to specify a proxy server.</span></span> <span data-ttu-id="cc0ec-118">Введите адрес прокси-сервера в формате \*\* &lt; HostName &gt; : &lt; порт &gt; \*\*, где &lt; **имя узла** &gt; — это DNS-имя или IP-адрес, а &lt; **порт** &gt; — номер порта TCP.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-118">Enter the proxy address in the form **&lt;hostname&gt;:&lt;port&gt;**, where the &lt;**hostname**&gt; is a DNS name or IP address, and the &lt;**port**&gt; is a TCP port number.</span></span> <span data-ttu-id="cc0ec-119">**Анализатор сбоев** может работать в двух режимах.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-119">There are two modes in which the **Crash Analyzer** can be run.</span></span> <span data-ttu-id="cc0ec-120">Ниже показано, как использовать параметры прокси-сервера в каждом из этих режимов.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-120">Following is how you use the proxy setting in each of these modes:</span></span>

    -   <span data-ttu-id="cc0ec-121">**Режим Online:** В этом режиме, если поле прокси-сервер оставлено пустым, мастер использует параметры прокси-сервера из свойств браузера на панели управления.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-121">**Online mode:** In this mode, if the proxy server field is left blank, the wizard uses the proxy settings from Internet Options in Control Panel.</span></span> <span data-ttu-id="cc0ec-122">Если в текстовом поле введен адрес прокси-сервера, будет использоваться этот адрес и он будет переопределен в параметрах браузера.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-122">If you enter a proxy address in the text box which is provided, that address will be used, and it will override the setting in the Internet Options.</span></span>

    -   <span data-ttu-id="cc0ec-123">Среда восстановления Windows (WindowsRE): когда вы запускаете **аварийный анализ** в окне " **инструменты диагностики и восстановления** ", отсутствует адрес прокси-сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-123">Windows Recovery Environment (WindowsRE): When you run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window, there is no default proxy address.</span></span> <span data-ttu-id="cc0ec-124">Если компьютер напрямую подключен к Интернету, адрес прокси-сервера не требуется.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-124">If the computer is directly connected to the Internet, a proxy address is not required.</span></span> <span data-ttu-id="cc0ec-125">Таким образом, вы можете оставить это поле пустым в настройке мастера.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-125">Therefore, you can leave this field blank in the wizard setting.</span></span> <span data-ttu-id="cc0ec-126">Если компьютер не подключен к Интернету напрямую и находится в сетевой среде с прокси-сервером, для доступа к хранилищу символов необходимо настроить поле прокси-сервера в мастере.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-126">If the computer is not directly connected to the Internet, and it is in a network environment that has a proxy server, you must set the proxy field in the wizard to access the symbol store.</span></span> <span data-ttu-id="cc0ec-127">Адрес прокси-сервера можно получить у администратора сети.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-127">The proxy address can be obtained from the network administrator.</span></span> <span data-ttu-id="cc0ec-128">Настройка прокси-сервера важна только в том случае, если хранилище общедоступных символов подключено к Интернету.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-128">Setting the proxy server is important only when the public symbol store is connected to the Internet.</span></span> <span data-ttu-id="cc0ec-129">Если символы уже находятся на рисунке восстановления DaRT или они доступны локально, Настройка прокси-сервера не требуется.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-129">If the symbols are already on the DaRT recovery image, or if they are available locally, setting the proxy server is not required.</span></span>

## <span data-ttu-id="cc0ec-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="cc0ec-130">Related topics</span></span>


[<span data-ttu-id="cc0ec-131">Диагностика ошибок системы с помощью средства анализа сбоев Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="cc0ec-131">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer-dart-10.md)

[<span data-ttu-id="cc0ec-132">Операции DaRT 10</span><span class="sxs-lookup"><span data-stu-id="cc0ec-132">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

 

 





