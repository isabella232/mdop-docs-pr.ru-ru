---
title: Настройка необходимых компонентов для установки
description: Настройка необходимых компонентов для установки
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819309"
---
# <span data-ttu-id="940b1-103">Настройка необходимых компонентов для установки</span><span class="sxs-lookup"><span data-stu-id="940b1-103">Configure Installation Prerequisites</span></span>


<span data-ttu-id="940b1-104">Ниже приведены рекомендации по установке и использованию виртуализации классической версии Microsoft Enterprise (MED-V) 2,0:</span><span class="sxs-lookup"><span data-stu-id="940b1-104">The following instructions are prerequisites for installing and using Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

[<span data-ttu-id="940b1-105">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="940b1-105">Windows Virtual PC</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[<span data-ttu-id="940b1-106">Обновление для Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="940b1-106">Windows Virtual PC Update</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[<span data-ttu-id="940b1-107">Конфигурация программного обеспечения для защиты от вирусов и резервного копирования</span><span class="sxs-lookup"><span data-stu-id="940b1-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a><span data-ttu-id="940b1-108">Установка и настройка Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="940b1-108">How to Install and Configure Windows Virtual PC</span></span>


<span data-ttu-id="940b1-109">**Важно!**  Если на главном компьютере уже есть версия Virtual PC для Windows, необходимо удалить ее, прежде чем устанавливать Virtual PC для Windows.</span><span class="sxs-lookup"><span data-stu-id="940b1-109">**Important** If a version of Virtual PC for Windows already exists on the host computer, you must uninstall it before you install Windows Virtual PC.</span></span>

 

**<span data-ttu-id="940b1-110">Установка Virtual PC для Windows</span><span class="sxs-lookup"><span data-stu-id="940b1-110">To install Windows Virtual PC</span></span>**

1.  <span data-ttu-id="940b1-111">Скачайте [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) из центра загрузки Майкрософт ( https://go.microsoft.com/fwlink/?LinkId=195918) .</span><span class="sxs-lookup"><span data-stu-id="940b1-111">Download [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195918).</span></span>

2.  <span data-ttu-id="940b1-112">Запустите установочный файл на главном компьютере и следуйте инструкциям мастера.</span><span class="sxs-lookup"><span data-stu-id="940b1-112">Run the installation file on the host computer, and follow the steps in the wizard.</span></span>

<span data-ttu-id="940b1-113">**Важно!**  В Windows Virtual PC есть пакет компонентов интеграции, который предоставляет возможности, повышающие взаимодействие между виртуальной средой и физическим компьютером.</span><span class="sxs-lookup"><span data-stu-id="940b1-113">**Important** Windows Virtual PC includes the Integration Components package, which provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="940b1-114">Например, это позволяет перемещать указатель мыши между узлом и гостевым компьютером.</span><span class="sxs-lookup"><span data-stu-id="940b1-114">For example, it lets your mouse move between the host and the guest computers.</span></span> <span data-ttu-id="940b1-115">Для работы MED-V требуется установка пакета компонентов интеграции.</span><span class="sxs-lookup"><span data-stu-id="940b1-115">MED-V requires the installation of the Integration Components package.</span></span>

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a><span data-ttu-id="940b1-116">Установка и Настройка обновления для Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="940b1-116">How to Install and Configure the Windows Virtual PC Update</span></span>


<span data-ttu-id="940b1-117">Обновление Майкрософт, связанное со статьей KB977206, включает режим Windows XP для компьютеров без технологии виртуализации с аппаратной поддержкой (HAV).</span><span class="sxs-lookup"><span data-stu-id="940b1-117">The Microsoft update associated with article KB977206 enables Windows XP Mode for computers without hardware-assisted virtualization (HAV) technology.</span></span> <span data-ttu-id="940b1-118">Рекомендуется установить это обновление, так как некоторые возможности интеграции могут работать неправильно, если пакет компонентов интеграции в гостевой операционной системе не совпадает с версией Virtual PC, установленной на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="940b1-118">We recommended that you install this update because some integration features might not work correctly if the Integration Components package in the guest operating system do not match the version of Windows Virtual PC that is installed on the host computer.</span></span>

<span data-ttu-id="940b1-119">**Важно!**  При установке MED-V на узловые компьютеры под управлением Windows 7 с пакетом обновления 1 (SP1) вам не нужно устанавливать это обновление.</span><span class="sxs-lookup"><span data-stu-id="940b1-119">**Important** You do not have to install this update when you are installing MED-V on host computers that are running Windows 7 with Service Pack 1.</span></span>

 

<span data-ttu-id="940b1-120">**Совет**  В дополнение к описанному здесь обновлению рекомендуется ознакомиться со всеми доступными обновлениями Virtual PC для Windows и применить соответствующие или необходимые обновления для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="940b1-120">**Tip** In addition to the update listed here, we recommend that you review all available Windows Virtual PC updates and apply those updates that are appropriate or necessary for your environment.</span></span>

 

**<span data-ttu-id="940b1-121">Установка обновления для Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="940b1-121">To install the Windows Virtual PC Update</span></span>**

1.  <span data-ttu-id="940b1-122">Скачайте нужное обновление для Windows Virtual PC из центра загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="940b1-122">Download the required Windows Virtual PC update from the Microsoft Download Center.</span></span>

    <span data-ttu-id="940b1-123">[32-разрядное обновление](https://go.microsoft.com/fwlink/?LinkId=195919) ( https://go.microsoft.com/fwlink/?LinkId=195919) .</span><span class="sxs-lookup"><span data-stu-id="940b1-123">[32-bit Update](https://go.microsoft.com/fwlink/?LinkId=195919) (https://go.microsoft.com/fwlink/?LinkId=195919).</span></span>

    <span data-ttu-id="940b1-124">[64-разрядное обновление](https://go.microsoft.com/fwlink/?LinkId=195920) ( https://go.microsoft.com/fwlink/?LinkId=195920) .</span><span class="sxs-lookup"><span data-stu-id="940b1-124">[64-bit Update](https://go.microsoft.com/fwlink/?LinkId=195920) (https://go.microsoft.com/fwlink/?LinkId=195920).</span></span>

2.  <span data-ttu-id="940b1-125">Запустите установочный файл на главном компьютере в режиме с повышенными привилегиями и следуйте инструкциям мастера.</span><span class="sxs-lookup"><span data-stu-id="940b1-125">Run the installation file on the host computer in elevated mode, and follow the steps in the wizard.</span></span>

    <span data-ttu-id="940b1-126">Дополнительные сведения о пакете исправлений для Virtual PC для Windows можно найти в [статье 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ( https://go.microsoft.com/fwlink/?LinkId=195921) .</span><span class="sxs-lookup"><span data-stu-id="940b1-126">For more information about the hotfix package for Windows Virtual PC, see [article 977206](https://go.microsoft.com/fwlink/?LinkId=195921) (https://go.microsoft.com/fwlink/?LinkId=195921).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="940b1-127">Настройка программного обеспечения для защиты от вирусов и резервного копирования</span><span class="sxs-lookup"><span data-stu-id="940b1-127">How to Configure Antivirus/Backup Software</span></span>


<span data-ttu-id="940b1-128">Чтобы предотвратить влияние антивирусной программы на производительность виртуального рабочего стола, мы рекомендуем, где вы можете исключить следующие типы файлов виртуальных машин из антивирусной программы или процесса резервного копирования, запущенного на главном компьютере:</span><span class="sxs-lookup"><span data-stu-id="940b1-128">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend, where you can, to exclude the following virtual machine file types from any antivirus or backup process that is running on the host computer:</span></span>

-   <span data-ttu-id="940b1-129">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="940b1-129">\*.VMC</span></span>

-   <span data-ttu-id="940b1-130">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="940b1-130">\*.VUD</span></span>

-   <span data-ttu-id="940b1-131">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="940b1-131">\*.VSV</span></span>

-   <span data-ttu-id="940b1-132">\*. VHD</span><span class="sxs-lookup"><span data-stu-id="940b1-132">\*.VHD</span></span>

## <span data-ttu-id="940b1-133">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="940b1-133">Related topics</span></span>


[<span data-ttu-id="940b1-134">Настройка необходимых компонентов среды</span><span class="sxs-lookup"><span data-stu-id="940b1-134">Configure Environment Prerequisites</span></span>](configure-environment-prerequisites.md)

[<span data-ttu-id="940b1-135">Высокоуровневая архитектура</span><span class="sxs-lookup"><span data-stu-id="940b1-135">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="940b1-136">Поддерживаемые конфигурации MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="940b1-136">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





