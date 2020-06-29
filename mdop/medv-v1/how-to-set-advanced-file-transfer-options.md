---
title: Настройка дополнительных параметров передачи файлов
description: Настройка дополнительных параметров передачи файлов
author: dansimp
ms.assetid: 5e9f8749-a5a9-48c6-9bfc-6b8e0cbe6cab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7319374c9a79d42c5d2e668eb8431a2c083fb40d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824652"
---
# <span data-ttu-id="32278-103">Настройка дополнительных параметров передачи файлов</span><span class="sxs-lookup"><span data-stu-id="32278-103">How to Set Advanced File Transfer Options</span></span>


**<span data-ttu-id="32278-104">Настройка дополнительных параметров передачи файлов</span><span class="sxs-lookup"><span data-stu-id="32278-104">To set advanced file transfer options</span></span>**

1.  <span data-ttu-id="32278-105">На панели **развертывания** нажмите кнопку **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="32278-105">In the **Deployment** pane, click **Advanced**.</span></span>

2.  <span data-ttu-id="32278-106">В диалоговом окне " **Параметры передачи файлов** " настройте параметры, как описано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="32278-106">In the **File Transfer Options** dialog box, configure the parameters as described in the following table.</span></span>

3.  <span data-ttu-id="32278-107">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="32278-107">Click **OK**.</span></span>

**<span data-ttu-id="32278-108">Свойства параметров передачи файлов</span><span class="sxs-lookup"><span data-stu-id="32278-108">File Transfer Options Properties</span></span>**

<span data-ttu-id="32278-109">*Рабочая область описания свойств для размещения*</span><span class="sxs-lookup"><span data-stu-id="32278-109">Property Description *Workspace to Host*</span></span>

<span data-ttu-id="32278-110">Команда "выполнить" на полученных файлах</span><span class="sxs-lookup"><span data-stu-id="32278-110">Run command on received files</span></span>

<span data-ttu-id="32278-111">Установите этот флажок, чтобы выполнить командную строку для всех файлов, передаваемых на узел.</span><span class="sxs-lookup"><span data-stu-id="32278-111">Select this check box to run a command line on all files transferred to the host.</span></span> <span data-ttu-id="32278-112">В поле "Командная строка" введите командную строку, которую нужно выполнить для всех полученных файлов.</span><span class="sxs-lookup"><span data-stu-id="32278-112">In the command-line box, enter the command line to run on all received files.</span></span>

<span data-ttu-id="32278-113">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="32278-113">File types</span></span>

-   <span data-ttu-id="32278-114">**Разрешить все расширения файлов**— выберите этот параметр, чтобы разрешить передачу файлов любого расширения имени файла из рабочей области MED-V на узел.</span><span class="sxs-lookup"><span data-stu-id="32278-114">**Allow all file extensions**—Click to enable transferring files of any file name extension from the MED-V workspace to the host.</span></span>

-   <span data-ttu-id="32278-115">**Разрешать следующие расширения файлов**— включение и использование только файлов с указанными расширениями имен файлов.</span><span class="sxs-lookup"><span data-stu-id="32278-115">**Allow the following file extensions**—Click to enable only files with specified file name extensions to be transferred.</span></span> <span data-ttu-id="32278-116">В пустом поле Введите имена всех допустимых расширений файлов, разделяя их запятыми.</span><span class="sxs-lookup"><span data-stu-id="32278-116">In the empty field, enter all file name extensions allowed, separated by commas.</span></span>

*<span data-ttu-id="32278-117">Узел в рабочую область</span><span class="sxs-lookup"><span data-stu-id="32278-117">Host to Workspace</span></span>*

<span data-ttu-id="32278-118">Команда "выполнить" на полученных файлах</span><span class="sxs-lookup"><span data-stu-id="32278-118">Run command on received files</span></span>

<span data-ttu-id="32278-119">Установите этот флажок, чтобы выполнить командную строку для всех файлов, передаваемых в рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="32278-119">Select this check box to run a command line on all files transferred to the MED-V workspace.</span></span> <span data-ttu-id="32278-120">В поле "Командная строка" введите командную строку, которую нужно выполнить для всех передаваемых файлов.</span><span class="sxs-lookup"><span data-stu-id="32278-120">In the command-line box, enter the command line to run on all transferred files.</span></span>

<span data-ttu-id="32278-121">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="32278-121">File types</span></span>

-   <span data-ttu-id="32278-122">**Разрешить все расширения имен файлов**— включение передачи файлов любого расширения.</span><span class="sxs-lookup"><span data-stu-id="32278-122">**Allow all file extensions**—Click to enable transferring files of any file name extension.</span></span>

-   <span data-ttu-id="32278-123">**Разрешить следующие расширения файлов**— щелкните, чтобы включить передачу только файлов с указанными расширениями файлов из узла в рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="32278-123">**Allow the following file extensions**—Click to enable only files with specified file name extensions to be transferred from the host to the MED-V workspace.</span></span> <span data-ttu-id="32278-124">В пустом поле введите все расширения имен файлов, разделенные двоеточиями.</span><span class="sxs-lookup"><span data-stu-id="32278-124">In the empty field, enter all file name extensions allowed, separated by colons.</span></span>

 

## <span data-ttu-id="32278-125">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="32278-125">Related topics</span></span>


[<span data-ttu-id="32278-126">Настройка пользователя или группы домена</span><span class="sxs-lookup"><span data-stu-id="32278-126">How to Configure a Domain User or Group</span></span>](how-to-configure-a-domain-user-or-groupmedvv2.md)

 

 





