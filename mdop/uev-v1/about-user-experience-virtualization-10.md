---
title: Сведения о User Experience Virtualization 1.0
description: Сведения о User Experience Virtualization 1.0
author: dansimp
ms.assetid: 3758b100-35a8-4e10-ac08-f583fb8ddbd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6010f9c4ebc260eec0324fb880dc2c92fd675130
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822712"
---
# <span data-ttu-id="31961-103">Сведения о User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="31961-103">About User Experience Virtualization 1.0</span></span>


<span data-ttu-id="31961-104">Microsoft User Experience Virtualization (UE-V) отслеживает изменения, внесенные пользователями в параметры приложения и параметры операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="31961-104">Microsoft User Experience Virtualization (UE-V) monitors the changes that are made by users to application settings and Windows operating system settings.</span></span> <span data-ttu-id="31961-105">Пользовательские параметры записываются и централизовано в хранилище параметров.</span><span class="sxs-lookup"><span data-stu-id="31961-105">The user settings are captured and centralized to a settings storage location.</span></span> <span data-ttu-id="31961-106">Эти параметры затем можно применить к разным компьютерам, к которым пользователь обращается, включая настольные компьютеры, Ноутбуки и сеансы инфраструктуры виртуальных рабочих столов (VDI).</span><span class="sxs-lookup"><span data-stu-id="31961-106">These settings can then be applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="31961-107">Виртуализация взаимодействия с пользователем использует шаблоны расположений параметров, чтобы указать, какие приложения и параметры Windows на компьютерах пользователей будут отслеживаться и централизовано.</span><span class="sxs-lookup"><span data-stu-id="31961-107">User Experience Virtualization uses settings location templates to specify what applications and Windows settings on the user computers are monitored and centralized.</span></span> <span data-ttu-id="31961-108">Шаблон расположения параметров — это XML-файл, который указывает, какие расположения файлов и реестра связаны с каждым приложением или параметром операционной системы.</span><span class="sxs-lookup"><span data-stu-id="31961-108">The settings location template is an XML file that specifies which file and registry locations are associated with each application or operating system setting.</span></span> <span data-ttu-id="31961-109">Шаблон не содержит значений для параметров; Он будет содержать только расположения параметров, которые нужно отслеживать.</span><span class="sxs-lookup"><span data-stu-id="31961-109">The template does not contain values for the settings; it contains only the locations of the settings that are to be monitored.</span></span>

<span data-ttu-id="31961-110">Параметры приложения и параметры Windows контролируются UE-V, когда пользователи работают на своих компьютерах.</span><span class="sxs-lookup"><span data-stu-id="31961-110">The application settings and Windows settings are monitored by UE-V when users are working on their computers.</span></span> <span data-ttu-id="31961-111">Значения параметров приложения хранятся на сервере хранилища параметров, когда пользователь закрывает приложение.</span><span class="sxs-lookup"><span data-stu-id="31961-111">The values for the application settings are stored on the settings storage server when the user closes the application.</span></span> <span data-ttu-id="31961-112">Значения параметров Windows сохраняются, когда пользователь выходит из системы, блокируется или отключается удаленно с компьютера.</span><span class="sxs-lookup"><span data-stu-id="31961-112">The values for the Windows settings are stored when the user logs off, when the computer is locked, or when they disconnect remotely from a computer.</span></span>

<span data-ttu-id="31961-113">Администратор может создать шаблон расположения параметров UE-V, чтобы указать, какие параметры корпоративного приложения будут перемещаться.</span><span class="sxs-lookup"><span data-stu-id="31961-113">An administrator can create a UE-V settings location template to specify which enterprise application settings will roam.</span></span> <span data-ttu-id="31961-114">UE-V включает набор шаблонов расположений параметров для некоторых приложений Майкрософт и параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="31961-114">UE-V includes a set of settings location templates for some Microsoft applications and Windows settings.</span></span> <span data-ttu-id="31961-115">Список приложений и параметров по умолчанию в UE-V вы можете найти в разделе [Планирование приложений для синхронизации с UE-v 1,0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="31961-115">For a list of default applications and settings in UE-V, see [Planning Which Applications to Synchronize with UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span></span>

## <span data-ttu-id="31961-116">Заметки о выпуске UEV 1,0</span><span class="sxs-lookup"><span data-stu-id="31961-116">UEV 1.0 Release Notes</span></span>


<span data-ttu-id="31961-117">Дополнительные сведения и последние новости, которые не были внесены в документацию, можно найти в статье сведения [о Microsoft User Experience Virtualization (UE-V) 1,0](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="31961-117">For more information, and for late-breaking news that did not make it into the documentation, see [Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span></span>

## <span data-ttu-id="31961-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="31961-118">Related topics</span></span>


[<span data-ttu-id="31961-119">Начало работы с User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="31961-119">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="31961-120">Microsoft User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="31961-120">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="31961-121">Высокоуровневая архитектура для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="31961-121">High-Level Architecture for UE-V 1.0</span></span>](high-level-architecture-for-ue-v-10.md)

 

 





