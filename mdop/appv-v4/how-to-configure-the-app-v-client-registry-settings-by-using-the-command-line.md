---
title: Настройка параметров реестра клиента App-V с помощью командной строки
description: Настройка параметров реестра клиента App-V с помощью командной строки
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817899"
---
# <span data-ttu-id="23d6c-103">Настройка параметров реестра клиента App-V с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="23d6c-103">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>


<span data-ttu-id="23d6c-104">После того как клиент Application Virtualization (App-V) развернут и настроен во время установки с помощью командной строки, может потребоваться изменить один или несколько параметров конфигурации клиента.</span><span class="sxs-lookup"><span data-stu-id="23d6c-104">After the Application Virtualization (App-V) Client has been deployed and configured during the installation by using the command line, it might be necessary to change one or more client configuration settings.</span></span> <span data-ttu-id="23d6c-105">Для этого нужно изменить соответствующие разделы реестра, выполнив одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="23d6c-105">This is accomplished by editing the appropriate registry keys, using one of the following methods:</span></span>

-   <span data-ttu-id="23d6c-106">Использование редактора реестра непосредственно</span><span class="sxs-lookup"><span data-stu-id="23d6c-106">Using the Registry Editor directly</span></span>

-   <span data-ttu-id="23d6c-107">Использование REG-файла</span><span class="sxs-lookup"><span data-stu-id="23d6c-107">Using a .reg file</span></span>

-   <span data-ttu-id="23d6c-108">Использование языка сценариев, например VBScript или Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="23d6c-108">Using a scripting language such as VBScript or Windows PowerShell</span></span>

<span data-ttu-id="23d6c-109">Кроме того, существует шаблон ADM, который можно использовать.</span><span class="sxs-lookup"><span data-stu-id="23d6c-109">There is also an ADM template that you can use.</span></span> <span data-ttu-id="23d6c-110">Дополнительные сведения о шаблоне ADM можно найти в разделе <https://go.microsoft.com/fwlink/?LinkId=121835> .</span><span class="sxs-lookup"><span data-stu-id="23d6c-110">For more information about the ADM template, see <https://go.microsoft.com/fwlink/?LinkId=121835>.</span></span>

<span data-ttu-id="23d6c-111">**Внимание!**  Будьте внимательны при редактировании реестра, так как ошибки могут привести к неработоспособности компьютера.</span><span class="sxs-lookup"><span data-stu-id="23d6c-111">**Caution** Use care when you edit the registry because errors can leave the computer in an unusable state.</span></span> <span data-ttu-id="23d6c-112">Не забудьте соблюдать стандартные деловые рекомендации, связанные с изменениями в реестре.</span><span class="sxs-lookup"><span data-stu-id="23d6c-112">Be sure to follow your standard business practices that relate to registry edits.</span></span> <span data-ttu-id="23d6c-113">Тщательно протестируйте все предлагаемые изменения в тестовой среде, прежде чем развертывать их на реальных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="23d6c-113">Thoroughly test all proposed changes in a test environment before you deploy them to production computers.</span></span>

 

## <span data-ttu-id="23d6c-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="23d6c-114">In This Section</span></span>


<span data-ttu-id="23d6c-115">**Важно!**  В 64-разрядных компьютерах разделы и значения, описанные в следующих разделах, находятся в разделе HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span><span class="sxs-lookup"><span data-stu-id="23d6c-115">**Important** On a 64-bit computer, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[<span data-ttu-id="23d6c-116">Сброс параметров кэша файловой системы</span><span class="sxs-lookup"><span data-stu-id="23d6c-116">How to Reset the FileSystem Cache</span></span>](how-to-reset-the-filesystem-cache.md)  
<span data-ttu-id="23d6c-117">Предоставляет сведения, необходимые для сброса кэша файловой системы.</span><span class="sxs-lookup"><span data-stu-id="23d6c-117">Provides the information that is required to reset the FileSystem cache.</span></span>

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[<span data-ttu-id="23d6c-118">Изменение размера кэша файловой системы</span><span class="sxs-lookup"><span data-stu-id="23d6c-118">How to Change the Size of the FileSystem Cache</span></span>](how-to-change-the-size-of-the-filesystem-cache.md)  
<span data-ttu-id="23d6c-119">В этой статье объясняется, как можно изменить размер кэша.</span><span class="sxs-lookup"><span data-stu-id="23d6c-119">Explains how you can change the size of the cache.</span></span>

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[<span data-ttu-id="23d6c-120">Использование функции управления размером кэша</span><span class="sxs-lookup"><span data-stu-id="23d6c-120">How to Use the Cache Space Management Feature</span></span>](how-to-use-the-cache-space-management-feature.md)  
<span data-ttu-id="23d6c-121">В этой статье описано, как настроить функцию управления пространством кэша.</span><span class="sxs-lookup"><span data-stu-id="23d6c-121">Describes how you can configure the cache space management feature.</span></span>

<a href="" id="how-to-configure-the-client-log-file"></a>[<span data-ttu-id="23d6c-122">Настройка файла журнала клиента</span><span class="sxs-lookup"><span data-stu-id="23d6c-122">How to Configure the Client Log File</span></span>](how-to-configure-the-client-log-file.md)  
<span data-ttu-id="23d6c-123">В этой статье описаны различные значения разделов реестра, которые контролируют файл журнала клиента и как его можно изменить.</span><span class="sxs-lookup"><span data-stu-id="23d6c-123">Describes the various registry key values that control the client log file and how you can change them.</span></span>

<a href="" id="how-to-configure-user-permissions"></a>[<span data-ttu-id="23d6c-124">Настройка разрешений для пользователей</span><span class="sxs-lookup"><span data-stu-id="23d6c-124">How to Configure User Permissions</span></span>](how-to-configure-user-permissions.md)  
<span data-ttu-id="23d6c-125">Определяет раздел реестра, управляющий разрешениями пользователя, и приводятся примеры изменения некоторых разрешений.</span><span class="sxs-lookup"><span data-stu-id="23d6c-125">Identifies the registry key that controls the user permissions and gives examples of how you can change some permissions.</span></span>

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[<span data-ttu-id="23d6c-126">Настройка клиента для получения пакетов приложений</span><span class="sxs-lookup"><span data-stu-id="23d6c-126">How to Configure the Client for Application Package Retrieval</span></span>](how-to-configure-the-client-for-application-package-retrieval.md)  
<span data-ttu-id="23d6c-127">В этой статье объясняется, как настроить клиент для извлечения содержимого, значков и сопоставлений типов файлов из разных источников, а также несколько примеров правильного формата пути.</span><span class="sxs-lookup"><span data-stu-id="23d6c-127">Explains how to configure the client to retrieve package content, icons, and file type associations from different sources, and provides several examples of the correct path format.</span></span>

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[<span data-ttu-id="23d6c-128">Настройка клиента для включения режима изолированной работы</span><span class="sxs-lookup"><span data-stu-id="23d6c-128">How to Configure the Client for Disconnected Operation Mode</span></span>](how-to-configure-the-client-for-disconnected-operation-mode.md)  
<span data-ttu-id="23d6c-129">Сведения о том, как настроить различные параметры, связанные с режимом отключенных операций.</span><span class="sxs-lookup"><span data-stu-id="23d6c-129">Provides information about how to configure the various settings associated with disconnected operations mode.</span></span>

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[<span data-ttu-id="23d6c-130">Настройка работы ярлыков и сопоставлений типов файлов</span><span class="sxs-lookup"><span data-stu-id="23d6c-130">How to Configure Shortcut and File Type Association Behavior</span></span>](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
<span data-ttu-id="23d6c-131">В этой статье описаны значения разделов реестра, управляющие сочетаниями клавиш и сопоставлением типов файлов в клиенте App-V, а также сведения о том, как их настроить.</span><span class="sxs-lookup"><span data-stu-id="23d6c-131">Describes the registry key values that control shortcuts and file type associations in the App-V client, and provides details on how to configure them.</span></span>

## <span data-ttu-id="23d6c-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="23d6c-132">Related topics</span></span>


[<span data-ttu-id="23d6c-133">Клиент Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="23d6c-133">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





